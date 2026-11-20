# Data Model & Architecture

## Primary Tables

| Table | Role |
|---|---|
| Properties | Property inventory and property-level attributes |
| Leads | Inquiry and acquisition-channel activity |
| Transactions | Completed lease placement activity |

## Relationships

- Properties[PropertyID] → Transactions[PropertyID]
- Leads[LeadID] → Transactions[LeadID]

## Why This Structure

The model keeps inquiries separate from completed leases. This allows conversion analysis to compare lead generation with actual placement outcomes without inflating transaction counts. PropertyID connects completed business back to neighborhood and property characteristics.
