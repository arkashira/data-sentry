# tech-spec.md

## Stack
- **Language:** Python
- **Framework:** FastAPI
- **Runtime:** Docker

## Hosting
- **Free-tier-first:** Yes
- **Specific Platforms:**
  - Heroku (Free Tier)
  - AWS (Free Tier with Lambda and S3)
  - DigitalOcean (App Platform Free Tier)
  - Vercel (for static front-end components)

## Data Model
### Tables/Collections
1. **Users**
   - **Key Fields:**
     - `user_id` (UUID, Primary Key)
     - `email` (String, Unique)
     - `password_hash` (String)
     - `created_at` (Timestamp)

2. **Backups**
   - **Key Fields:**
     - `backup_id` (UUID, Primary Key)
     - `user_id` (UUID, Foreign Key)
     - `backup_data` (JSON)
     - `status` (String: 'pending', 'completed', 'failed')
     - `created_at` (Timestamp)
     - `updated_at` (Timestamp)

3. **DisasterRecoveryPlans**
   - **Key Fields:**
     - `plan_id` (UUID, Primary Key)
     - `user_id` (UUID, Foreign Key)
     - `backup_id` (UUID, Foreign Key)
     - `schedule` (String: Cron format)
     - `created_at` (Timestamp)

## API Surface
1. **Create User**
   - **Method:** POST
   - **Path:** `/api/users`
   - **Purpose:** Register a new user.

2. **Authenticate User**
   - **Method:** POST
   - **Path:** `/api/auth/login`
   - **Purpose:** Authenticate user and return JWT token.

3. **Create Backup**
   - **Method:** POST
   - **Path:** `/api/backups`
   - **Purpose:** Initiate a new backup process for the authenticated user.

4. **Get Backups**
   - **Method:** GET
   - **Path:** `/api/backups`
   - **Purpose:** Retrieve a list of backups for the authenticated user.

5. **Get Backup Status**
   - **Method:** GET
   - **Path:** `/api/backups/{backup_id}`
   - **Purpose:** Retrieve the status of a specific backup.

6. **Create Disaster Recovery Plan**
   - **Method:** POST
   - **Path:** `/api/recovery-plans`
   - **Purpose:** Create a new disaster recovery plan for the authenticated user.

7. **Get Disaster Recovery Plans**
   - **Method:** GET
   - **Path:** `/api/recovery-plans`
   - **Purpose:** Retrieve a list of disaster recovery plans for the authenticated user.

8. **Execute Recovery Plan**
   - **Method:** POST
   - **Path:** `/api/recovery-plans/{plan_id}/execute`
   - **Purpose:** Execute a specific disaster recovery plan.

## Security Model
- **Authentication:** JWT (JSON Web Tokens)
- **Secrets Management:** Use AWS Secrets Manager or HashiCorp Vault for storing sensitive information (e.g., database credentials).
- **IAM:** Role-based access control (RBAC) for user permissions.

## Observability
- **Logs:** Centralized logging using ELK Stack (Elasticsearch, Logstash, Kibana) or AWS CloudWatch.
- **Metrics:** Prometheus for collecting metrics on API performance and backup success rates.
- **Traces:** OpenTelemetry for distributed tracing to monitor the flow of requests through the system.

## Build/CI
- **CI/CD Tool:** GitHub Actions
- **Build Process:**
  - Linting with Flake8
  - Testing with pytest
  - Docker image build and push to Docker Hub
- **Deployment:** Automated deployment to Heroku or AWS upon merging to the main branch.