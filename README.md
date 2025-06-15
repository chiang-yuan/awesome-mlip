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

    subgraph "2010-2019"
        TFN["TFN<br/>Equivariance"]
        SOAP[SOAP]
        ACE["ACE<br/>Many-body Expansion"]
        GAP[GAP]
        SNAP[SNAP]
        MTP[MTP]
        SchNet["SchNet<br/>Filter, RBF"]
        HDNNP[HDNNP]
    end

    subgraph "2020-2023"
        NequIP[NequIP]
        MACE[MACE]
        MACE_MP["MACE-MP"]
        MACE_OFF["MACE-OFF"]
        M3GNet[M3GNet]
        CHGNet[CHGNet]
        eSCN[eSCN]
        ORBs[ORBs]
        DPA1["DPA-1"]
        Equiformer[Equiformer]
        GNS[GNS]
        GNoME[GNoME]
    end

    subgraph "2024"
        GRACE[GRACE]
        eSEN[eSEN]
        DPA3["DPA-3"]
        ESCalP[ESCalP]
        MatterSim[MatterSim]
        SevenNet[SevenNet]
        eqV2["eqV2<br/>(OMat)"]
    end

    %% === Edges (ordered genealogy) ===
    BP --> ANI --> ANI2x --> AIMNet2
    BP --> HDNNP
    BP --> GAP --> SNAP
    BP --> SchNet --> TFN 
    GAP --> MTP
    GAP --> SOAP --> ACE --> MACE 
    MACE --> MACE_MP --> GRACE
    MACE --> MACE_OFF
    TFN --> e3nn --> NequIP --> MACE
    NequIP --> GNoME
    NequIP --> SevenNet
    NequIP --> eSEN
    M3GNet --> CHGNet
    M3GNet --> MatterSim
    Equiformer --> eqV2
    Attention --> eqV2
    GNS --> ORBs
    Attention --> DPA1 --> DPA3
    Attention --> ESCalP


    %% === Styling ===
    classDef foundation fill:#1e3a8a,stroke:#1e40af,stroke-width:3px,color:#fff,font-weight:bold
    classDef groupTheory fill:#0f766e,stroke:#0d9488,stroke-width:2px,color:#fff,font-weight:bold
    classDef organic fill:#059669,stroke:#10b981,stroke-width:2px,color:#fff,font-weight:bold
    classDef universal fill:#dc2626,stroke:#ef4444,stroke-width:3px,color:#fff,font-weight:bold
    classDef attention fill:#7c3aed,stroke:#8b5cf6,stroke-width:2px,color:#fff,font-weight:bold
    classDef advanced fill:#ea580c,stroke:#f97316,stroke-width:2px,color:#fff,font-weight:bold
    classDef symmetry fill:#be185d,stroke:#ec4899,stroke-width:2px,color:#fff,font-weight:bold

    class BP foundation
    class ANI,HDNNP,GAP,SNAP,MTP,SOAP,SchNet,TFN groupTheory
    class ANI2x,MACE_OFF organic
    class AIMNet2,MACE_MP,CHGNet,M3GNet,MatterSim,GRACE,SevenNet universal
    class GNS,DPA1,DPA3,ESCalP attention
    class ACE,MACE,NequIP,Equiformer advanced
    class GNoME,eqV2,eSCN,eSEN,ORBs symmetry



```
