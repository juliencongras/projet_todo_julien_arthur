# Plan de tests

**Nom et prénom :** Julien Congras, Arthur  
**Date :** 05/11/26

Complétez ce fichier avant de coder les tests, puis ajoutez les résultats après leur exécution.

## 1 Les neuf cas à tester

| ID | Page | Situation à vérifier |
| --- | --- | --- |
| INS-01 | /register | Inscription avec des données valides |
| INS-02 | /register | Inscription avec un champ obligatoire vide |
| INS-03 | /register | Inscription avec deux mots de passe différents |
| TACHE-01 | /task/new | Ajout d’une tâche valide avec une catégorie |
| TACHE-02 | /task/new | Ajout avec un champ obligatoire vide |
| TACHE-03 | /task/new | Accès à la page sans être connecté |
| LISTE-01 | /task/activeall | Les tâches actives du compte connecté sont affichées |
| LISTE-02 | /task/activeall | Ses tâches terminées ne sont pas affichées |
| LISTE-03 | /task/activeall | Les tâches d’un autre compte ne sont pas affichées |

### INS-01 Inscription avec des données valides

- **Objectif : Vérifier la réussite d'une tentative d'inscription avec des données valides** [Ce que vous voulez vérifier]
- **Préparation : Compte déconnecté, données: firstname, lastname, email, password, confirm-password** [Compte connecté ou non, données nécessaires, page de départ]
- **Données utilisées :  
firstname="Camille"
lastname="Cypress"
email= "cypress-${Date.now()}@example.test"
password= "Test-Cypress-2026!"
confirm-password="Test-Cypress-2026!"** [Valeurs saisies ou méthode pour les générer]
- **Actions :**
  1. Visiter la page register
  2. Renseigner les informations demandées
  3. Soumettre le formulaire d'inscription
- **Résultat attendu : Le compte doit être créer** [Ce qui doit se produire]
- **Résultat obtenu :** [À compléter après le test]
- **Statut :** non exécuté

### INS-02 Inscription avec un champ obligatoire vide

- **Objectif : Vérifier l'échec' d'une tentative d'inscription avec une donnée obligatoir manquante** [Ce que vous voulez vérifier]
- **Préparation : Compte déconnecté, données: firstname, lastname, email, password, confirm-password** [Compte connecté ou non, données nécessaires, page de départ]
- **Données utilisées :  
firstname="Camille"
lastname="Cypress"
email= ""
password= "Test-Cypress-2026!"
confirm-password="Test-Cypress-2026!"** [Valeurs saisies ou méthode pour les générer]
- **Actions :**
  1. Visiter la page register
  2. Renseigner les informations demandées sauf email
  3. Soumettre le formulaire d'inscription
- **Résultat attendu : La création du compte doit échouer** [Ce qui doit se produire]
- **Résultat obtenu :** [À compléter après le test]
- **Statut :** non exécuté

### INS-03 Inscription avec deux mots de passe différents

- **Objectif : Vérifier l'échec' d'une tentative d'inscription avec 2 mots de passe différents** [Ce que vous voulez vérifier]
- **Préparation : Compte déconnecté, données: firstname, lastname, email, password, confirm-password** [Compte connecté ou non, données nécessaires, page de départ]
- **Données utilisées :  
firstname="Camille"
lastname="Cypress"
email= ""
password= "Test-Cypress-2026!"
confirm-password="Test-Cypress-2026?"** [Valeurs saisies ou méthode pour les générer]
- **Actions :**
  1. Visiter la page register
  2. Renseigner les informations demandées
  3. Soumettre le formulaire d'inscription
- **Résultat attendu : La création du compte doit échouer** [Ce qui doit se produire]
- **Résultat obtenu :** [À compléter après le test]
- **Statut :** non exécuté

### TACHE-01 Ajout d’une tâche valide avec une catégorie

- **Objectif :** Nous voulons vérifier qu'une tâche avec des information valide puisse être ajoutée à notre liste de taches.
- **Préparation :** 
Compte connecté : Oui.
Données nécessaires : Titre de la tache, description de la tache, date d'échéance, répétition pour la tache, catégorie de la tache.
Page de départ : /task/new
- **Données utilisées :** Faire les courses, Allez faire les courses au supermarché en ce servant de la liste de course, 07/11/2026 11:00, Corvée.
- **Actions :**
  1. Cliquer sur l'input "Saisir le titre".
  2. Saisir le titre.
  3. Cliquer sur l'input "Saisir la description".
  4. Saisir la description.
  5. Cliquer sur l'input "Saisir la date d'échéance".
  6. Saisir la date d'échéance.
  7. Cliquer sur la catégorie corespondante à la tache dans la liste des catégories.
  8. Cliquer sur le bouton ajouter.
- **Résultat attendu :** La tache est ajoutée aux taches actives.
- **Résultat obtenu :** [À compléter après le test]
- **Statut :** non exécuté

### TACHE-02 Ajout avec un champ obligatoire vide

- **Objectif :** Nous voulons vérifier qu'une tache avec des informations obligatoire manquante ne s'ajoute pas à notre liste de taches.
- **Préparation :**
Compte connecté : Oui.
Données nécessaires : Description de la tache, date d'échéance, répétition pour la tache, catégorie de la tache.
Page de départ : /task/new
- **Données utilisées :** Faire le ménage dans toute la maison, 10/11/2026 14:30, Corvée.
- **Actions :**
  1. Cliquer sur l'input "Saisir la description".
  2. Saisir la description.
  3. Cliquer sur l'input "Saisir la date d'échéance".
  4. Saisir la date d'échéance.
  5. Cliquer sur la catégorie corespondante à la tache dans la liste des catégories.
  6. Cliquer sur le bouton ajouter.
- **Résultat attendu :** La tache n'est pas ajoutée aux taches actives.
- **Résultat obtenu :** [À compléter après le test]
- **Statut :** non exécuté

### TACHE-03 Accès à la page sans être connecté

- **Objectif :** Nous voulons vérifier qu'un utilisateur non connecté ne puisse pas aller sur la page d'ajout de taches.
- **Préparation :**
Compte connecté : Non.
Données nécessaires : Aucune.
Page de départ : Accueil.
- **Données utilisées :** Aucune.
- **Actions :**
  1. Aller sur la page : /task/new
- **Résultat attendu :** L'utilisateur n'a pas accès à la page.
- **Résultat obtenu :** [À compléter après le test]
- **Statut :** non exécuté
