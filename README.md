# 📐 MedHead – Architecture Repository

Ce repository contient l’ensemble des documents d’architecture relatifs à la preuve de concept (PoC) du système d’intervention d’urgence du consortium **MedHead**.

Il sert de support documentaire pour :

-   comprendre le contexte métier et technique du projet
    
-   centraliser les documents fournis par le consortium
    
-   présenter les choix architecturaux réalisés
    
-   exposer les résultats et enseignements de la PoC
    

----------

## 🎯 Objectifs du repository

-   fournir une vision claire de l’architecture cible
    
-   démontrer la conformité aux principes imposés
    
-   justifier les technologies retenues
    
-   documenter les performances et la qualité de la PoC
    

----------

## 📂 Structure du repository

### 📁 00_sources

Documents sources fournis par MedHead :

-   énoncé des travaux d’architecture (TOGAF)
    
-   principes d’architecture
    
-   document de définition de l’architecture
    
-   exigences de la PoC
    
-   données de référence NHS (spécialités)
    
-   feuille de route du projet
    

Ces documents constituent les entrées officielles du travail d’architecture.

----------

### 📁 01_reporting

Contient le **document de reporting de la PoC**.

Ce document présente :

-   les choix techniques backend et frontend
    
-   la conformité aux principes d’architecture
    
-   l’intégration des services externes (ORS)
    
-   les résultats des tests automatisés
    
-   les résultats des tests de performance
    
-   les limites et recommandations
    

----------

### 📁 02_diagrams

Contient les schémas et diagrammes :

-   architecture applicative
    
-   flux de données
    
-   composants techniques
    
-   interactions microservices
    

----------

## 🔗 Repositories associés

Code complet (backend + frontend + performance + CI) :

[https://github.com/salihayoubi23/medhead-code](https://github.com/salihayoubi23/medhead-code)

Repository architecture :

[https://github.com/salihayoubi23/medhead_architecture](https://github.com/salihayoubi23/medhead_architecture)

----------

## 🧱 Vue d’ensemble de l’architecture

La PoC repose sur :

-   Frontend React (UI utilisateur)
    
-   Backend Spring Boot (API REST)
    
-   PostgreSQL (persistance)
    
-   OpenRouteService (routage réel)
    
-   CI/CD GitHub Actions
    
-   Tests automatisés et de charge
    

Approche :

-   orientée microservices
    
-   découplage front/back
    
-   intégration continue
    
-   validation par la performance
    

----------

## 🔐 Sécurité (approche d’architecture)

Dans le cadre de la PoC :

-   échanges front/back via API REST
    
-   CORS configuré
    
-   secrets externalisés
    

Architecture cible :

-   HTTPS/TLS
    
-   OAuth2 / OpenID Connect
    
-   JWT
    
-   contrôle d’accès par rôles
    
-   audit des accès
    

----------

## 🛡️ RGPD – Privacy by Design

Principes appliqués dans la PoC :

-   minimisation des données
    
-   aucune donnée patient stockée
    

Architecture cible :

-   séparation identité/données médicales
    
-   chiffrement
    
-   anonymisation
    
-   politiques de rétention
    
-   droit à l’oubli
    

----------

## 📊 Performance et qualité

La PoC intègre :

-   tests unitaires et d’intégration automatisés
    
-   pipeline CI/CD
    
-   tests de charge Apache JMeter
    
-   rapports HTML
    

Objectif :

-   démontrer la robustesse sous charge
    
-   valider les temps de réponse
    
-   préparer une montée en charge future
    

----------

## 👤 Auteur

Saliha Youbi  
Projet OpenClassrooms – Architecte Logiciel

----------