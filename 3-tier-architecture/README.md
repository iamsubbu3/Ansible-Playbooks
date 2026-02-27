                         Internet
                             │
                             ▼
                ┌─────────────────────┐
                │   Application LB    │
                └─────────────────────┘
                             │
                             ▼
        ┌─────────────────────────────────────┐
        │          Public Subnets             │
        │                                     │
        │  Web1 (Apache)     Web2 (Apache)    │
        └─────────────────────────────────────┘
                             │
                             ▼
        ┌─────────────────────────────────────┐
        │         Private Subnets             │
        │                                     │
        │  App1 (Flask)       App2 (Flask)    │
        └─────────────────────────────────────┘
                             │
                             ▼
                  ┌─────────────────┐
                  │     RDS MySQL   │
                  └─────────────────┘

 Bastion Host (Public Subnet)
        │
        ▼
 SSH to Private Instances

 Private Subnets → NAT Gateway → Internet (outbound only)