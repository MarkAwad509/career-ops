# career-ops -- Modes francophones (`modes/fr/`)

Ce dossier contient les traductions francaises des principaux modes career-ops pour les candidats qui ciblent le marché francophone (France, Belgique, Suisse romande, Luxembourg, Quebec).

## Quand utiliser ces modes ?

Utilisez `modes/fr/` si au moins une de ces conditions est applicable à votre situation :

- Vous postulez principalement a des **offres d'emploi en francais** (Welcome to the Jungle, Indeed FR, APEC, Pole emploi / France Travail, LinkedIn FR, sites carrieres)
- Votre **CV est en francais** ou vous alternez entre FR et EN selon l'offre
- Vous avez besoin de reponses et lettres de motivation en **francais tech naturel**, pas traduit par une machine
- Vous devez gerer des **specificites contractuelles francophones** : convention collective, RTT, mutuelle, prevoyance, 13e mois, periode d'essai, preavis, cheques-dejeuner, interessement/participation, portage salarial

Si la plupart de vos offres sont en anglais, restez sur les modes standard dans `modes/`. Les modes anglais fonctionnent pour les offres francophones, mais ne connaissent pas les specificites du marche francophone en detail.

## Comment activer ?

### Option 1 -- Par session

Dites a Claude en debut de session :

> "Utilise les modes francais sous `modes/fr/`."

Claude lira alors les fichiers de ce dossier au lieu de `modes/`.

### Option 2 -- En permanence

Ajoutez dans `config/profile.yml` :

```yaml
language:
  primary: fr
  modes_dir: modes/fr
```

Rappelez-le a Claude lors de votre premiere session ("Regarde dans `profile.yml`, j'ai configure `language.modes_dir`"). Claude utilisera automatiquement les modes francais.

## Quels modes sont traduits ?

Cette premiere iteration couvre les quatre modes a plus fort impact :

| Fichier | Traduit depuis | Role |
|---------|----------------|------|
| `_shared.md` | `modes/_shared.md` (EN) | Contexte partage, archetypes, regles globales, specificites marche francophone |
| `offre.md` | `modes/oferta.md` (ES) | Evaluation complete d'une offre (Blocs A-F) |
| `postuler.md` | `modes/apply.md` (EN) | Assistant live pour remplir les formulaires de candidature |
| `pipeline.md` | `modes/pipeline.md` (ES) | Inbox d'URLs / Second Brain pour les offres collectees |

Les autres modes (`scan`, `batch`, `pdf`, `tracker`, `outcome`, `auto-pipeline`, `deep`, `contacto`, `ofertas`, `project`, `training`) restent en EN/ES. Leur contenu est surtout du tooling, des chemins et des commandes -- il doit rester independant de la langue.

## Ce qui reste en anglais

Volontairement non traduit car vocabulaire tech standard :

- `cv.md`, `pipeline`, `tracker`, `report`, `score`, `archetype`, `proof point`
- Noms d'outils (`Playwright`, `WebSearch`, `WebFetch`, `Read`, `Write`, `Edit`, `Bash`)
- Valeurs de statut dans le tracker (`Evaluated`, `Applied`, `Interview`, `Offer`, `Rejected`)
- Extraits de code, chemins, commandes

Les modes utilisent du francais tech naturel, tel qu'il est parle dans les equipes engineering a Paris, Lyon ou Geneve : texte courant en francais, termes techniques en anglais la ou c'est l'usage. Pas de traduction forcee de "Pipeline" en "Canalisation" ni de "Deploy" en "Deploiement applicatif".

## Lexique de reference

Pour garder un ton coherent si vous modifiez ou etendez les modes :

| Anglais | Francais (dans cette codebase) |
|---------|-------------------------------|
| Job posting | Offre d'emploi / Annonce |
| Application | Candidature |
| Cover letter | Lettre de motivation |
| Resume / CV | CV |
| Salary | Salaire / Remuneration |
| Compensation | Remuneration / Package |
| Skills | Competences |
| Interview | Entretien |
| Hiring manager | Manager recruteur / Hiring manager |
| Recruiter | Recruteur (ou Recruiter) |
| AI | IA (Intelligence Artificielle) |
| Requirements | Prerequis / Exigences |
| Career history | Parcours professionnel |
| Notice period | Preavis |
| Probation | Periode d'essai |
| Vacation | Conges payes (CP) |
| 13th month salary | 13e mois / Prime de fin d'annee |
| Permanent employment | CDI (Contrat a Duree Indeterminee) |
| Fixed-term contract | CDD (Contrat a Duree Determinee) |
| Freelance | Freelance / Independant / Auto-entrepreneur |
| Collective agreement | Convention collective |
| Works council | CSE (Comite Social et Economique) |
| Profit sharing | Interessement / Participation |
| Meal vouchers | Titres-restaurant / Cheques-dejeuner |
| Health insurance | Mutuelle d'entreprise |
| Disability/life insurance | Prevoyance |
| RTT | RTT (Reduction du Temps de Travail) |
| Cadre status | Statut cadre |
| SYNTEC | Convention SYNTEC (IT/consulting) |

## Contribuer

Pour ameliorer une traduction ou ajouter un mode :

1. Ouvrez une Issue avec votre proposition (voir `CONTRIBUTING.md`)
2. Respectez le lexique ci-dessus pour garder le ton coherent
3. Traduisez de maniere idiomatique -- pas de traduction mot a mot
4. Conservez les elements structurels (Blocs A-F, tableaux, blocs de code, instructions outils) a l'identique
5. Testez avec une vraie offre francophone (Welcome to the Jungle, APEC, Indeed FR) avant de soumettre la PR
