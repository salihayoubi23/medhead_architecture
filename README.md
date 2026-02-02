# 📐 MedHead – Architecture Repository

Ce repository centralise l’ensemble des documents d’architecture relatifs à la preuve de concept (PoC) du système d’intervention d’urgence du consortium **MedHead**.

Il constitue le support documentaire du projet et permet de :

-   comprendre le contexte métier et technique
    
-   regrouper les documents fournis par le consortium
    
-   présenter les choix architecturaux réalisés
    
-   exposer les résultats, limites et enseignements de la PoC
    

----------

## 🎯 Objectifs du repository

Ce repository a pour vocation de :

-   fournir une vision claire de l’architecture mise en œuvre dans la PoC
    
-   démontrer la conformité aux principes d’architecture définis par MedHead
    
-   justifier les choix technologiques backend et frontend
    
-   documenter les performances, la qualité et la sécurité du système
    

----------

## 📂 Structure du repository

### 📁 00_sources

Ce dossier contient les documents sources fournis par le consortium MedHead, notamment :

-   énoncé des travaux d’architecture (référentiel TOGAF)
    
-   principes d’architecture
    
-   document de définition de l’architecture cible
    
-   exigences fonctionnelles et non fonctionnelles de la PoC
    
-   données de référence NHS (spécialités médicales)
    
-   feuille de route du projet
    

Ces documents constituent les entrées officielles du travail d’architecture.

----------

### 📁 01_reporting

Ce dossier contient le **document de reporting de la preuve de concept**.

Il présente :

-   le contexte du projet et les enjeux métier
    
-   les choix architecturaux réalisés
    
-   l’implémentation backend et frontend
    
-   l’intégration du service externe OpenRouteService (ORS)
    
-   la stratégie de qualité et de tests automatisés
    
-   les résultats des tests de performance
    
-   les limites identifiées et recommandations pour l’industrialisation
    

----------

### 📁 02_diagrams

Ce dossier regroupe les schémas et diagrammes d’architecture, notamment :

-   vue d’ensemble de l’architecture applicative
    
-   flux de données
    
-   composants techniques
    
-   interactions entre services
    

----------

## 🔗 Repositories associés

Code complet de la PoC (backend, frontend, tests de performance, CI/CD) :

[https://github.com/salihayoubi23/medhead-code](https://github.com/salihayoubi23/medhead-code)

Repository d’architecture (documents et reporting) :

[https://github.com/salihayoubi23/medhead_architecture](https://github.com/salihayoubi23/medhead_architecture)

----------

## 🧱 Vue d’ensemble de l’architecture

La preuve de concept MedHead repose sur les composants suivants :

-   Frontend React pour l’interface utilisateur
    
-   Backend Spring Boot exposant une API REST
    
-   Base de données PostgreSQL pour la persistance
    
-   Service externe OpenRouteService (ORS) pour le calcul de distance et durée réelles
    
-   Pipeline d’intégration continue via GitHub Actions
    
-   Tests automatisés et tests de charge
    

L’approche retenue est fondée sur :

-   une séparation claire frontend / backend
    
-   une architecture compatible microservices
    
-   l’intégration continue
    
-   la validation par la performance et la qualité
    

----------

## 🔐 Sécurité (approche d’architecture)

Dans le cadre de la PoC, une première couche de sécurité opérationnelle a été mise en œuvre :

-   authentification utilisateur via Spring Security et JWT
    
-   gestion des rôles utilisateurs
    
-   endpoints protégés par token Bearer
    
-   secrets gérés via variables d’environnement
    
-   protection des données sensibles en base (emails chiffrés, mots de passe hashés)
    

Pour une architecture cible industrialisée, les évolutions prévues incluent :

-   généralisation des échanges sécurisés via HTTPS/TLS
    
-   intégration OAuth2 / OpenID Connect
    
-   gestion avancée des identités et autorisations
    
-   audit et traçabilité des accès
    
-   rotation des secrets et clés de chiffrement
    

----------

## 🛡️ RGPD – Privacy by Design

Principes appliqués dans la PoC :

-   minimisation des données stockées
    
-   absence de données personnelles patient
    
-   contrôle d’accès par authentification sécurisée
    
-   protection des données sensibles au repos
    

Évolutions prévues en production :

-   séparation des données d’identité et médicales
    
-   chiffrement généralisé
    
-   anonymisation et pseudonymisation
    
-   politiques de conservation
    
-   droit à l’oubli
    
-   traçabilité des accès
    

----------

## 📊 Performance et qualité

La PoC intègre une démarche complète de qualité logicielle :

-   tests unitaires et d’intégration automatisés (backend Spring Boot)
    
-   isolation des dépendances externes (ORS mocké en tests)
    
-   pipeline CI/CD via GitHub Actions
    
-   tests de charge réalisés avec Apache JMeter
    
-   génération de rapports HTML de performance
    

Objectifs atteints :

-   validation de la robustesse du backend sous charge
    
-   maîtrise des temps de réponse
    
-   détection rapide des régressions
    
-   préparation à une montée en charge future
    

----------

## 👤 Auteur

Saliha Youbi  
Projet OpenClassrooms – Architecte Logiciel