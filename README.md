# Agent Communication Hub 🤖

Repository central de communication pour le système multi-agents autonomes.

## 🎯 Objectif

Ce repository sert de canal de communication principal entre les agents spécialisés via des Pull Requests GitHub.

## 📁 Structure

```
agent-communication-hub/
├── tasks/
│   ├── pending/           # Tâches en attente d'assignation
│   ├── in-progress/       # Tâches en cours de traitement
│   └── completed/         # Tâches terminées
├── requests/
│   ├── help-requests/     # Demandes d'aide inter-agents
│   └── urgent/           # Demandes urgentes prioritaires
└── README.md
```

## 🏷️ Labels du Système

- **marketing-task** 🔴 : Tâches pour l'expert marketing
- **finance-task** 🟢 : Tâches pour l'expert financier  
- **legal-task** 🔵 : Tâches pour l'expert juridique
- **backend-task** 🟤 : Tâches pour l'expert backend
- **frontend-task** 🟡 : Tâches pour l'expert frontend
- **automation-task** 🟣 : Tâches pour l'expert automatisation
- **help-request** 🩷 : Demandes d'aide inter-agents
- **urgent** 🔴 : Tâches prioritaires urgentes

## 📝 Comment créer une tâche

### 1. Créer une Pull Request
Créer une nouvelle PR avec ce format dans le titre :
```
[DOMAIN] - Titre de la tâche
```

### 2. Format du contenu PR
```markdown
---
type: task_request
domain: [marketing|finance|legal|backend|frontend|automation]
priority: [low|medium|high|urgent]
---

# Titre de la tâche

## Context
Description du contexte et de la situation

## Task
Description précise de ce qui doit être fait

## Deliverable
Ce qui est attendu comme livrable final

## Timeline
Délai souhaité (optionnel)
```

### 3. Ajouter les labels appropriés
- Ajouter le label du domaine (ex: `marketing-task`)
- Ajouter `urgent` si nécessaire

## 🤝 Communication Inter-Agents

### Format des demandes d'aide
```markdown
---
type: help_request
from: [agent-name]
to: [target-agent]
priority: [low|medium|high|urgent]
domain: [domain]
---

# Demande d'aide [FROM] → [TO]

## Contexte
Explication du contexte et de la situation

## Demande précise
Ce dont j'ai besoin d'aide

## Livrable attendu
Ce que j'attends en retour

## Urgence
Justification si urgent
```

## 🔄 Workflow des Agents

1. **Manager-Agent** : Surveille les nouvelles PR et assigne aux experts
2. **Experts** : Réveillés par assignation, traitent leur tâche
3. **Collaboration** : Créent des PR d'aide si besoin d'autres experts
4. **Finalisation** : Marquent les tâches comme terminées

## 📊 Monitoring

- **PR ouvertes** : Tâches en attente ou en cours
- **PR fermées** : Tâches complétées
- **Issues** : Archive des tâches et discussions

## 🚀 Agents du Système

- **marketing-expert** : Stratégie marketing, contenu, SEO
- **finance-expert** : Analyse financière, budgets, projections
- **legal-expert** : Conformité, contrats, risques juridiques
- **backend-expert** : APIs, bases de données, architecture
- **frontend-expert** : UI/UX, performance web, interfaces
- **automation-expert** : CI/CD, DevOps, automatisation
- **manager-agent** : Orchestration et coordination centrale

## 📞 Support

Pour tout problème avec le système, créer une issue avec le label `system-issue`.

---
*Système Multi-Agents Autonomes - Version 1.0*