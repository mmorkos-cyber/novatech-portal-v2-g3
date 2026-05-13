![Illustration projet](https://simplonline.co/_next/image?url=https%3A%2F%2Fsimplonline-v3-prod.s3.eu-west-3.amazonaws.com%2Fmedia%2Fimage%2Fpng%2F973686fb-80c9-4351-b3e7-ff5b2b5481ab-6a0342b26c6c8182220928.png&w=1280&q=75)

# Opération Refonte NovaTech / Interface de gestion de crise

> Le portail interne NovaTech, créé par le service Communication, est devenu ingérable.
> La DSI reprend le relais : stabiliser le projet, structurer Git, corriger les tickets via un workflow professionnel.

---

## Contexte du projet

Le projet existe mais présente plusieurs problèmes :

- Les fichiers HTML contiennent des données en dur
- Une base SQLite existe mais n'est pas clairement exploitée
- Un script Python génère du HTML sans documentation d'usage
- Certains liens sont cassés
- Des informations sensibles sont présentes dans le code
- Aucun workflow Git fiable n'est en place

---

## Objectifs de la journée

- [ ] Auditer l'état actuel du projet
- [ ] Mettre en place une stratégie de branches
- [ ] Travailler uniquement par tickets
- [ ] Utiliser des Pull Requests
- [ ] Documenter les règles de contribution (`CONTRIBUTING.md`)
- [ ] Nettoyer et corriger le portail sans casser le projet

---

## Arborescence du projet

```
NOVATECH-PORTAL-V2-G3/
├── web/
│   ├── index.html
│   ├── methodology.html
│   ├── tickets.html
│   ├── report.html
│   └── style.css
├── scripts/
│   ├── init_db.py
│   └── export_tickets.py
│   └── audit_project.py
├── CONTRIBUTING.md
└── README.md
└── .gitignore
```

---

## Démarche

### 1. Audit général & initialisation Git

Analyse de l'état du projet, identification des problèmes, mise en place de la structure Git.

### 2. Définition du workflow NovaTech

Rédaction du `CONTRIBUTING.md` établissant :
- Les conventions de nommage des commits
- Les conventions de nommage des branches
- Les règles relatives aux Pull Requests

### 3. Création et attribution des tickets

Chaque correctif ou amélioration passe par un ticket dédié, une branche associée et une PR avant merge.

---

## Conventions de style

  --primary-color: #2c3e50;
  --secondary-color: #34495e;
  --accent-color: #3498db;
  --danger-color: #c0392b;
  --warning-color: #f39c12;
  --success-color: #27ae60;
  --light-color: #ecf0f1;
  --dark-color: #1e272e;

  font-family: Arial, sans-serif;
  background: var(--light-color);
  color: var(--dark-color);

## Installation & lancement

```bash
# Initialiser la base de données
python scripts/init_db.py

# Exporter les tickets en HTML
python scripts/export_tickets.py
```

Ouvrir ensuite `web/index.html` dans un navigateur.

---

## Contribution

Consulter [CONTRIBUTING.md](CONTRIBUTING.md) avant toute modification.
