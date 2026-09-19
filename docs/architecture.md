# Architecture — HealthGrid

```mermaid
flowchart TB
 U[Patient / professionnel] --> APP[Web / Mobile]
 APP --> API[API]
 API --> AUTH[Identity & permissions]
 API --> REF[Référencement]
 API --> RES[Ressources: centres, médicaments, labos]
 API --> NOTIF[Notifications]
 API --> SYNC[Offline Sync]
 REF --> AUDIT[Audit]
 RES --> AUDIT
```

## Principes

Architecture offline-first, synchronisation explicite, chiffrement, contrôle d'accès par rôle, audit et minimisation des données.

Les données médicales doivent être isolées des données opérationnelles lorsque possible. Toute fonction clinique sensible doit avoir une supervision humaine et une procédure d'évaluation.