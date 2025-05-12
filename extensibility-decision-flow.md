```mermaid
%% Diagram 3: Extensibility Decision Flow
flowchart TD
    Target["Target group and consumption"] --> |"Consumer-grade apps Apps for users outside of S/4 Native mobile / freestyle UI"| Target_Yes{YES}
    Target --> |NO| SaaS["SaaS solution?"]
    
    SaaS --> |"Partner SaaS solution (for many customers, for multiple core products, etc.)"| SaaS_Yes{YES}
    SaaS --> |NO| Infra["Infrastructure and operations"]
    
    Infra --> |"Independence of SAP S/4HANA infrastructure and operation (flexible scalability, flexible downtimes, flexible choice of data center required?)"| Infra_Yes{YES}
    Infra --> |NO| System["System of records and transaction"]
    
    System --> |"Tightly coupled extensions"| System_Options["Only small amount of data is added"]
    System --> |"Transactional consistency required"| System_Options
    System --> |"Enabling custom services for side-by-side extensibility"| System_No{NO}
    
    System_Options --> |YES| KeyUser["Key User or Developer Extension"]
    
    KeyUser --> |"Simple 'last mile' extensions (UI flexibility, custom fields, etc.) Analytical key user use cases"| KeyUserOptions
    KeyUserOptions --> |YES| KeyUserExt["Key User Extensibility SAP Fiori-based Key User Tools"]
    KeyUserOptions --> |NO| DevExt["Developer Extensibility ABAP Development Tools in Eclipse"]
    
    Target_Yes --> SideBySide["Side-by-Side Extensibility Developer Tools (Java, Node.js, ABAP)     Low/no-code tools                                      (SAP Build)"]
    SaaS_Yes --> SideBySide
    Infra_Yes --> SideBySide
    System_No --> SideBySide

%% Diagram 4: SAP S/4HANA Extensibility Tiers
flowchart LR
    title4["In-App / On-Stack Extensibility"]
    title5["Side-by-Side Extensibility"]
    
    subgraph S4HANA["SAP S/4HANA Cloud Private Edition"]
        subgraph TIER1["TIER 1"]
            T1_KU["Key User Extensibility (Fiori apps)"]
            T1_Dev["Developer Extensibility (ABAP Cloud)"]
        end
        
        subgraph TIER2["TIER 2"]
            T2["Cloud API enablement"]
        end
        
        subgraph TIER3["TIER 3"]
            T3["Classical ABAP development"]
        end
        
        TIER1 --- TIER2
        TIER2 --- TIER3
        T3 -->|"Adapt"| T3
    end
    
    subgraph BTP["SAP Business Technology Platform"]
        subgraph TIER1_BTP["TIER 1"]
            T1_BTP_Low["Low/No code (SAP Build)"]
            T1_BTP_Dev["Developer (Java, node.js, ABAP Cloud)"]
        end
    end
    
    TIER1 <-->|"Renovate or innovate"| TIER1_BTP
    TIER3 -->|"Retire"| Trash((🗑️))
    
    title4 --- S4HANA
    title5 --- BTP
    
    classDef cleanCore fill:#f5f5f5,stroke-dasharray: 5 5;
    class S4HANA,BTP cleanCore;

%% Diagram 5: SAP S/4HANA Architecture and Extensibility
flowchart TB
    subgraph MainSystem[""]
        subgraph OnStack["ON-STACK EXTENSIONS"]
            S4Apps["SAP S/4HANA Applications"]
            
            InApp["In-app extensibility"]
            PublicInt["Public Interfaces"]
            
            Custom["Custom code"]
            Partner["Partner extensions"]
            
            KeyUser["In-App Key User Extensibility (low/no-code tools)"] -->|"  "| InApp
            InApp --- S4Apps
            S4Apps --- PublicInt
            PublicInt --- Custom
            PublicInt --- Partner
            DevExt["In-App Developer Extensibility (custom ABAP)"] -->|"  "| Custom
            DevExt -->|"  "| Partner
        end
        
        PubInt2["Public interfaces"]
        
        subgraph ABAP["SAP S/4HANA ABAP CLOUD ENVIRONMENT"]
            ABAP1["ABAP RESTful application programming model"]
            ABAP2["Cloud-optimized ABAP language"]
            ABAP3["Released Objects, APIs, BAdIs"]
        end
        
        HANADB[(SAP HANA DB)]
        S4System["SAP S/4HANA System"]
        
        OnStack --- PubInt2
        PubInt2 --- ABAP
        ABAP --- HANADB
        ABAP --- S4System
    end
```
