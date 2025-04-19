```mermaid
flowchart LR
    A[IT Contact] -->|Provides Access| B[Partner Project Manager]
    B -->|Sets Up| C[Project Structure]
    B -->|Creates/Defines| D[Project Roles]
    
    D --> E[Standard Roles]
    D --> F[Custom Roles]
    F -->|Example| G[LoB Experts]
    
    B -->|Assigns| H[Team Members to Roles]
    H --> I[Create Teams]
    I -->|Contains| J[Collection of Roles/Users]
    
    style B fill:#0F9D58
```
