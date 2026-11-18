# Compromise Reconstruction Ontology — Technical Report

**Author:** Aisha Khan  
**Date:** November 2026  
**Interactive version:** [Ontology Playground share link](https://microsoft.github.io/Ontology-Playground/#/share/eJylWM1u5EQQfpVSc-Di7O4BCRROQ8IhBwhaIu0BolFPd9lu1u6yusuTNas8ARIS4gG4IK68Go-Aum2P2xNnMjObU1z983V99T8fBVmmiopOXH4UVtYoLsUV1Y2j2niEt6jIenatYkMWbsfNmdDolTNNEItL8bOF5G_cBjk5cMkVtgA1XS4Vm63hLgPcGo1WYTa_x9gtejaFDCg-A43K-P5fhzVqExfiPWQ9SKuhoC06K63CV9NdIhNo2XB31zXoxeVPH4XR4lJIxeRENuq9Gj7nqq2gQefJAjmQSlFrGZRs5KZCoBxYvg9q9W94JTJhVDz2319__C0yoagiJy7FZ2_efPnV9RciE42jBh2b4SEDdnzK2miRCe6aIPHsjC3Chf5Gh-fnBp24ZNfiY7Z3Lh7ZP5ns8tQ6hWuzu8cf2t1v425dS1blWpHNe_NMh4IlalkdOFUjl_RUncf7cCSyrxzGI7KaTHCVyvbt4BtUJjcKapTWB_Jly2XYrnpH2GBFtgjmYAJpIRp0ZpM__znBJtMDzzBMcnjZOhMRHn3w6omFH3eCOQW3FkGRZWNban2qPergpYZ0BhUVxgYCKiqo5fPVH551tO6TQtJ75CSuhs8n9uw8Y52BR7dFl4GWLDfSYxZDrWmq0a5cyhBzwcAhBNF71OfrFV93TqjFcy8ZMyhxu_kFVULAdSp71qtzU2EW06XT4JEjDeE6j7xTG0K-sxAp_QTPJsvSWL92WLRVcJ91AJr02hBVKO0sh6D1pk_Y6wq3WB1KIb0W65gtp33GMhboXnIfi_xA7v11yP02esBE5fdLa3NK35XoEKjlDbVWAzuZB3of0HIGJgdpOy5DkqgwZ-ASYQA8n0_j1_iBQ-GpnnK4r20uK4-zxHkyQ6EiGc8hJ68cm1ym3vbD4uKe240cKIcxe5CDmnRA00O4UVtpKJy0DHnLrRtD7xMCb3jNi-XK4RYdoz7oj8PL1zJxMC0Z2dT4IufLHJ1mBNyiTWj_dvh8mrJ3Ed43CcBd7BiG-pRN4gYzYOmKEPuhmQmqAFOBXOIn1LH40PN6i5D_X7JWeKVnWTcLdnjag_RJ_9B9U7-x9orcUteRpNuhJUyS7STZ93nAD6GoGAb8kJuKXUwgF-QukoACjYyuHrJLBg-GSzDsd00qqFKaeav3-78nmGN88hkW2R19ySZbdNqkPn0WzVniQsPWqPuh-pc05is1z91vF5aemGgMBvkeLUgPEhz6tuLY7sFo3Ax8q8qw7nBLfQcOU8sVKydWyEOgjZlnHkO_ndafH8P7sO2MlE6ukNb8ulfubufSOVt3JYLU1EQtGa20_DqMV9J20PooLBEaR7pV_HX8qNuKzUW_F2J9lK47P7Okjz5e6Wz5fJQd8Cx58x1pTIaF1U7wlBdVSe9D0o13v56c_SI4e-CmDmf7WtdThD5xsM89TGfOJyiCrLchu9BC2GR7G-nBRtKe3ba6Oce3hi5vLxgT2UKi7LsZqLDow2m4g1wHtKmGmXwKQwkbh1KVYIl3tEMlH87nbnr1GZkyOfycX91nwmG_x5emSX8XSAYrv_ITabMFkGEld1TPZjim5JcFJZ02VlaGu-DuFi-YLmppO7EzTutRXy2MwkEOsxl5GWq25Qg8Uqp1DvU7EzrACW-Ux4IXFwa8sc-JaBP4EVANupxcjfqbbsLZCWHTPQNyAnt9u4R6NR85RzGMo-gizLB2Asz1wnS3wwojFNC4uoQ4Gw6PgO1LH-obe-ek9Tm6O5qAx1UI8_6wDkzPYC9OVUe8YeizJ9hJsASzPJoc4ywOFWpMoi2RLCGNH0fc3f8w5FPyBtGMr5l5TnUR3zYNhakldfadcObsSdN6qiZDqZpH1CA7iDFVz2Pc3ZmiQId6v4XbLQx92vN4S33gKZa6dcWSsWCvTxrQx4wRofe2HIHa_2o8Z3WUHWR1VlkPAN0_ZmJjrDa2CHXm_vF_zW8UlA)

## 1. Problem

Breach detection remains slow in many mid-size enterprises because organizations lack a clear, structured model of their own security ecosystem. Without an explicit representation of actors, credentials, sessions, assets, data objects, and the paths that connect them, security teams struggle to reconstruct how a compromise actually unfolded. Industry observation for mid-enterprise environments places average time-to-detect in the range of 5–6 hours. The absence of accurate authentication and security mechanisms compounds the problem: telemetry exists, but the relationships that turn isolated events into a coherent breach narrative are missing. This delays both detection and the subsequent decisions about remediation and regulatory notification.

## 2. Approach

The Compromise Reconstruction Ontology defines 13 entity types and 15 relationships that together allow an investigator (or an automated system) to reconstruct a compromise path from initial credential use through to persistence, data movement, AI-assisted decisions, and regulatory obligations.

### Core entity types

| Entity | Role |
|--------|------|
| Actor | Person or account capable of action |
| Credential | Authentication means belonging to an Actor |
| Session | Continuous authenticated period |
| Asset | System, server, database or application |
| DataObject | File, record set or dataset on an Asset |
| NetworkDestination | Outbound destination of transferred data |
| PersistenceArtifact | Artifact that can grant future access |
| Event | Atomic action linking actor, target and time |
| Decision | Explicit determination (exfiltration / persistence) with evidence chain |
| RemediationAction | Concrete response triggered by a Decision |
| Organization | Multi-tenant boundary |
| AIModel | Model that produces confidence scores for Decisions |
| Regulation | External legal obligation (GDPR, HIPAA, etc.) |

### Why these 13 types

They form the minimal closed set needed to express a complete compromise narrative: who acted (Actor + Credential + Session), what was touched (Asset + DataObject), where data went (NetworkDestination), what was left behind (PersistenceArtifact), how the activity is sequenced (Event with `precedes`), how an AI system evaluates it (AIModel → Decision), what action is taken (RemediationAction), and which legal regime governs the response (Regulation). Adding fewer types would leave gaps in the path; adding more would increase complexity without proportional explanatory power for the core reconstruction task.

### Example breach path

```
Stolen Credential 
  → authenticates as → Session 
  → performed by / occurred within → Event (asset access) 
  → targeted asset / targeted data object → Asset / DataObject 
  → resulted in transfer to → NetworkDestination 
  → created → PersistenceArtifact 
  → supported by → Decision (produced by AIModel) 
  → triggered action → RemediationAction 
  → governed by → Regulation (GDPR / HIPAA)
```

### Modelling of AI decisions

`AIModel` represents the classification or scoring model that emits a confidence value. `Decision` is the explicit determination (verdict + evidence chain + confidence) produced by that model. The relationship `Decision —produced by→ AIModel` records provenance; `Decision —supported by→ Event` records the evidence; `Decision —triggered action→ RemediationAction` records the operational consequence. This design keeps the AI component first-class yet cleanly separated from the raw telemetry and from the final remediation steps.

### Regulatory linkage

Both GDPR and HIPAA are modelled as instances of the `Regulation` entity. A Decision can be linked to the applicable regulation(s) via the `governed by` relationship, enabling downstream compliance checks (notification timelines, data-subject rights, etc.).

## 3. Evaluation

The ontology was authored and published in the Microsoft Ontology Playground. It contains:

- 13 entity types  
- 15 relationships  
- 38 properties  

No formal query evaluation or scenario replay was performed against live telemetry. The design was validated by constructing the entity–relationship graph and confirming that the example compromise path above can be expressed without missing links. The interactive visualisation and natural-language query surface of the Playground were used to inspect connectivity and property coverage.

## 4. Future Work

Future work includes expanding the entity set for cloud and identity-provider specifics, adding sample instance data for end-to-end path queries, measuring reconstruction completeness against public breach reports, and extending regulatory coverage beyond GDPR and HIPAA to additional regimes such as CCPA and sector-specific rules.
