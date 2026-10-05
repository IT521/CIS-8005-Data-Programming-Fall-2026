# SQL vs MongoDB Comparison

This report compares equivalent analytics performed using SQLite and MongoDB.

## Telco Churn Distribution

### SQLite Result

| Churn Label   |   Customers |
|:--------------|------------:|
| No            |        5174 |
| Yes           |        1869 |

### MongoDB Result

| _id   |   Customers |
|:------|------------:|
| No    |        5174 |
| Yes   |        1869 |

### Observation

- Both systems produced equivalent business results.
- SQLite used SQL GROUP BY statements.
- MongoDB used aggregation pipelines.

---

## Retail Churn Distribution

### SQLite Result

|   Churn |   Customers |
|--------:|------------:|
|       0 |        4682 |
|       1 |         948 |

### MongoDB Result

|   _id |   Customers |
|------:|------------:|
|     1 |         948 |
|     0 |        4682 |

### Observation

- Both systems produced equivalent business results.
- SQLite used SQL GROUP BY statements.
- MongoDB used aggregation pipelines.

---

## Retail Sales Churn Distribution

### SQLite Result

| churned   |   Customers |
|:----------|------------:|
| No        |      500271 |
| Yes       |      499729 |

### MongoDB Result

| _id   |   Customers |
|:------|------------:|
| No    |      500271 |
| Yes   |      499729 |

### Observation

- Both systems produced equivalent business results.
- SQLite used SQL GROUP BY statements.
- MongoDB used aggregation pipelines.

---

## Technology Comparison


| Feature | SQLite | MongoDB |
|----------|----------|----------|
| Database Type | Relational | NoSQL Document |
| Schema | Fixed | Flexible |
| Query Language | SQL | Aggregation Pipeline |
| Joins | Strong Support | Limited |
| JSON Storage | Limited | Native |
| Transaction Data | Excellent | Good |
| Customer Profiles | Good | Excellent |
| Analytics | Excellent | Excellent |
| Scalability | Moderate | High |


## Project Conclusions

- SQLite was well suited for structured customer analytics and reporting.
- MongoDB provided flexible document storage for customer profiles.
- Both technologies produced consistent churn analysis results.
- SQLite was easier for tabular business reporting.
- MongoDB was better suited for semi-structured customer records.
