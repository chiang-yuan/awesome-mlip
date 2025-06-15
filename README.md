# Awesome Machine Learning Interatomic Potentials (MLIPs) [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)




```mermaid
%% Mermaid v10+ optimized vertical timeline
%% Enable in compatible Mermaid live editors: https://mermaid-js.github.io/mermaid-live-editor

%% Mermaid v10+ optimized vertical timeline
flowchart TB

    %% === Timeline blocks ===
    subgraph "2007"
        BP["Behler-Parrinello<br/>Atomized Energy"]
    end

    subgraph "2010 - 2019"
        SOAP[SOAP]
        SchNet["SchNet<br/>Filter, RBF"]
        TFN["TFN<br/>Equivariance"]
        ACE["ACE<br/>Many-body Expansion"]
        GDML[GDML]
        DeepMD[DeepMD]

        GAP[GAP]
        SNAP[SNAP]
        MTP[MTP]
        HDNNP[HDNNP]
        ANI[ANI]
    end

    subgraph "2020 - 2023"
        SCN[SCN]
        eSCN[eSCN]
        Equiformer[Equiformer]
        MACE[MACE]
        MACE_MP["MACE-MP"]
        MACE_OFF["MACE-OFF"]
        NequIP[NequIP]
        
        ANI2x[ANI2x]
        AIMNet2[AIMNet2]
        GNoME[GNoME]
        DPA1["DPA-1"]
        M3GNet[M3GNet]
        CHGNet[CHGNet]
        
    end

    subgraph "2024 - "
        GRACE[GRACE]
        eSEN["eSEN<br/>(OMat, OMol)"]
        eqV2["eqV2<br/>(OMat)"]
        MatterSim[MatterSim]
        SevenNet[SevenNet]
        ESCalP[ESCalP]
        ORBs[ORBs]
        DPA3["DPA-3"]
        
    end

    %% === Edges (ordered genealogy) ===
    BP --> ANI --> ANI2x --> AIMNet2
    BP --> HDNNP
    BP --> GAP --> SNAP
    BP --> SchNet --> TFN
    BP --> GDML
    BP --> DeepMD

    GAP --> MTP
    GAP --> SOAP --> ACE --> MACE 
    M3GNet --> MatterSim
    TFN --> SCN --> eSCN
    TFN --> e3nn --> NequIP --> MACE
    MACE --> MACE_MP --> GRACE
    MACE --> MACE_OFF
    NequIP --> GNoME
    NequIP --> SevenNet
    NequIP --> eSEN

    BP --> M3GNet
    MEGNet --> M3GNet --> CHGNet


     
    SCN --> Equiformer
    Equiformer --> eqV2


    
    
    
    
    
    
    %% ACE --> GRACE
    %% TFN --> eSCN
    
    G-CNNs --> TFN
    DeepMD --> DPA1
    Attention --> DPA1 --> DPA3
    Attention --> ESCalP
    Attention --> eqV2
    GNS --> ORBs



    %% === Styling ===
    classDef architecture fill:#1e3a8a,stroke:#1e40af,stroke-width:3px,color:#fff,font-weight:bold
    classDef organic fill:#059669,stroke:#10b981,stroke-width:2px,color:#fff,font-weight:bold
    classDef attention fill:#7c3aed,stroke:#8b5cf6,stroke-width:2px,color:#fff,font-weight:bold
    classDef equivariance fill:#ea580c,stroke:#f97316,stroke-width:2px,color:#fff,font-weight:bold
    classDef universal fill:#be185d,stroke:#ec4899,stroke-width:2px,color:#fff,font-weight:bold

    %% === Class assignments ===
    class BP,ANI,HDNNP,GAP,SNAP,MTP,SchNet,DeepMD,GDML architecture
    class SOAP,TFN,ACE,MACE,NequIP,Equiformer,eqV2,eSCN,eSEN,ORBs,SCN equivariance
    class ANI2x,AIMNet2,MACE_OFF organic
    class GNoME,MACE_MP,CHGNet,M3GNet,MatterSim,GRACE,SevenNet,eqV2,eSEN,ORBs universal
    class DPA1,DPA3,ESCalP attention
