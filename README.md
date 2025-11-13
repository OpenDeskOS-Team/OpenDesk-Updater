# 🧩 OpenDesk Update Repository

Ce dépôt centralise les **mises à jour officielles** des différents projets du système **OpenDesk**.  
Il contient un fichier `update_index.json` qui sert d’index de versionnement pour tous les composants et sous-projets OpenDesk.

---

## 📘 Sommaire
- [Présentation](#-présentation)
- [Structure du fichier `update_index.json`](#-structure-du-fichier-update_indexjson)
- [Exemple complet](#-exemple-complet)
- [Comment ajouter une mise à jour](#-comment-ajouter-une-mise-à-jour)
- [Bonnes pratiques](#-bonnes-pratiques)
- [Licence](#-licence)

---

## 🧠 Présentation

L’objectif de ce dépôt est de fournir un **point de référence unique** pour les clients OpenDesk (comme *OpenDeskOS*, *PopulaireCoreGL*, etc.) afin qu’ils puissent :
- Vérifier les dernières versions disponibles ;
- Télécharger automatiquement les mises à jour ;
- Consulter l’historique des versions.

Le fichier principal, `update_index.json`, est lu par le système OpenDesk pour détecter et appliquer les mises à jour.

---

## 🧱 Structure du fichier `update_index.json`

Le fichier `update_index.json` contient les informations suivantes :

```json
{
  "projets": {
    "nom_du_projet": {
      "repository": "URL du dépôt GitHub",
      "current_version": "version_actuelle",
      "version_history": {
        "version_numérique": {
          "title": "Titre de la version",
          "description": "Description détaillée des nouveautés ou correctifs",
          "date": "AAAA-MM-JJ",
          "file_url": "Lien direct vers le fichier de mise à jour"
        }
      }
    }
  }
}
```

### 🔍 Champs principaux

| Champ | Description |
|-------|--------------|
| **repository** | Lien vers le dépôt GitHub du projet concerné |
| **current_version** | Numéro de la version la plus récente |
| **version_history** | Historique complet des versions publiées |
| **file_url** | Lien direct vers le fichier exécutable / archive de mise à jour |
| **title** | Titre court décrivant la mise à jour |
| **description** | Détails sur les ajouts, changements ou corrections |
| **date** | Date officielle de publication |

---

## ⚙️ Comment ajouter une mise à jour

1. **Cloner le dépôt :**
```bash
   git clone https://github.com/OpenDesk-Team/update-repo.git  
   cd update-repo
```
2. **Ouvrir le fichier `update_index.json`**  
   Ajouter un nouveau bloc dans la section `version_history` du projet concerné.

3. **Mettre à jour la version actuelle :**  
   Modifier le champ `current_version` pour qu’il corresponde à la dernière version publiée.

4. **Commiter et pousser les changements :**
```bash
   git add update_index.json  
   git commit -m "Ajout de la version 0.0.2 pour OpenDeskOS"  
   git push
```
---

## 🧭 Bonnes pratiques

- Respecter le **versionnement sémantique** (`MAJEUR.MINEUR.PATCH`)  
- Toujours **héberger les fichiers de mise à jour** sur un lien stable et accessible  
- Ajouter des **changements clairs et concis** dans la description  
- Vérifier que le **JSON est valide** avant de pousser la mise à jour  

---

## 📜 Licence

Ce dépôt et le format `update_index.json` sont distribués sous licence **All Right Reserved**.  
© 2025 OpenDesk Team. Tous droits réservés.

---

> 💡 *OpenDesk — un environnement libre et modulaire, conçu pour la performance et la simplicité.*
