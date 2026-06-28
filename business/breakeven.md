# breakeven.md

## Unit Economics & Break-even Analysis for Data Sentry

### Cost per Active User
- **Compute Costs**: $0.05 per active user per month
- **Storage Costs**: $0.02 per GB per active user per month (Assuming average usage of 10 GB per user)
  - Total Storage Cost: $0.20 per active user per month
- **Bandwidth Costs**: $0.01 per GB per active user per month (Assuming average usage of 50 GB per user)
  - Total Bandwidth Cost: $0.50 per active user per month

**Total Cost per Active User**:  
Compute + Storage + Bandwidth = $0.05 + $0.20 + $0.50 = **$0.75 per active user per month**

### Pricing Tiers
| Tier Name      | Monthly Price ($) | Features                                                                 |
|----------------|-------------------|--------------------------------------------------------------------------|
| Basic          | $15               | Automated daily backups, 10 GB storage, Email notifications             |
| Professional    | $30               | Automated daily backups, 50 GB storage, Email + SMS notifications, API access |
| Enterprise     | $75               | Automated hourly backups, 200 GB storage, Email + SMS notifications, API access, Dedicated support |

### Customer Acquisition Cost (CAC) Range
- Estimated CAC: **$100 - $200** per user (includes marketing, sales, and onboarding costs)

### Lifetime Value (LTV) Estimate
- Average Revenue per User (ARPU) across tiers: 
  - Basic: $15/month
  - Professional: $30/month
  - Enterprise: $75/month
- Assuming an average user stays for 24 months:
  - LTV for Basic: $15 * 24 = **$360**
  - LTV for Professional: $30 * 24 = **$720**
  - LTV for Enterprise: $75 * 24 = **$1800**
- Weighted Average LTV (assuming 60% Basic, 30% Professional, 10% Enterprise):  
  LTV = (0.6 * 360) + (0.3 * 720) + (0.1 * 1800) = **$576**

### Break-even Users Count
- Break-even Point = CAC / (LTV - Cost per Active User)
- Using the average CAC of $150:
  - Break-even Users = $150 / ($576 - $0.75) = **0.26 users** (This indicates that the product is highly profitable with even one user)

### Path to $10K MRR
- To achieve $10,000 MRR, we can calculate the required number of users across different tiers:
  
| Tier Name      | Monthly Price ($) | Required Users for $10K MRR |
|----------------|-------------------|------------------------------|
| Basic          | $15               | 667 users                    |
| Professional    | $30               | 334 users                    |
| Enterprise     | $75               | 134 users                    |

**Conclusion**: The most feasible path to $10K MRR would be through the Professional tier, requiring **334 users**.