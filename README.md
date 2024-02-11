# Guide d'installation et de conception - Base de données Kicéo

Ce guide vous fournira les instructions nécessaires pour installer la base de données Kicéo et comprendre sa conception.

## Installation de la base

### Création
Veuillez exécuter la commande ci-dessous pour initialiser la base :
```bash
mysql -h localhost -u root -p < schema.sql
```

### Ajout des données
Pour intégrer les données, utilisez la commande suivante :
```bash
mysql -h localhost -u root -p < data.sql
```

### Requêtage
Pour effectuer des requêtes, utilisez la commande suivante :
```bash
mysql -h localhost -u root -p < requetes.sql
```

> **Note :** L'utilisateur `root` est un utilisateur par défaut. Veuillez vérifier son existence dans votre système ou vous référer à la liste des utilisateurs de votre base de données.

## Conception

### Dictionnaire de données

| Donnée       | Type                         |
|--------------|------------------------------|
| id_ligne     | `INT AUTO_INCREMENT`          |
| numero_ligne | `INT`                        |
| nom_ligne    | `VARCHAR(50)`                |
| horaire      | `TIME`                       |
| jour         | `ENUM('Lundi', ..., 'Dimanche')` |
| id_station   | `INT AUTO_INCREMENT`          |
| nom_station  | `VARCHAR(50)`                |

### Modèle relationnel de données

| MCD | MLD |
|-----|-----|
| ![MCD](https://kylzo.github.io/Eval sql/images/MCD.png) | ![MLD](https://kylzo.github.io/Eval sql/images/MLD.png) |

## Remarques

La réalisation de cette tâche s'est avérée plus complexe que prévu, notamment en raison de mon manque de pratique en SQL en dehors des cours. Je souhaite que la correction ne soit pas trop fastidieuse.

## Références

- [Documentation MySQL](https://dev.mysql.com/doc/refman/8.0/en/)
- [Merise par Developpez.com](https://ineumann.developpez.com/tutoriels/merise/initiation-merise/)
- [ChatGPT](https://chat.openai.com/)
