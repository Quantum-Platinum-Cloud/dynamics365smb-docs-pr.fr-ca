---
title: FAQ pour les détails techniques
description: Détails d’implémentation liés au connecteur Shopify.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: AndreiPanko
ms.author: andreipa
---

# <a name="faq-for-technical-details" />FAQ pour les détails techniques

Cet article répond aux questions fréquemment posées concernant le connecteur Shopify.

## <a name="what-is-shopify" />Qu’est-ce que Shopify ?

Shopify est un logiciel basé sur un abonnement qui permet à quiconque de créer une boutique en ligne et de vendre ses produits. La plateforme Shopify offre aux détaillants en ligne une suite de services comprenant des outils de paiement, de marketing, d’expédition et d’engagement client. 

## <a name="what-is-the-microsoft-dynamics-365-business-central-shopify-connector" />Qu’est-ce que le connecteur Microsoft Dynamics 365 Business Central Shopify ?

Grâce au connecteur Shopify, les entreprises ont la possibilité de connecter leur magasin (ou leurs magasins) Shopify avec [!INCLUDE[prod_short](../includes/prod_short.md)] pour accroître leur productivité. Le connecteur Shopify leur permet de gérer et d’afficher les informations de leur entreprise et de leur boutique en ligne Shopify comme une seule unité. 

### <a name="capabilities" />Fonctionnalités

- Prise en charge de plusieurs magasins Shopify
  - Chaque magasin a sa propre configuration, y compris un ensemble de produits, d’emplacements utilisés pour calculer l'inventaire et des listes de prix.  
- Synchronisation bidirectionnelle d’articles ou de produits
  - Le connecteur synchronisera les images, les variantes article, les codes-barres, les références fournisseur, les textes étendus et les balises.  
  - Exportez les attribut article dans Shopify.  
  - Utilisez les groupes prix client et les escomptes sélectionnés pour définir les prix exportés vers Shopify.  
  - Décidez si les articles peuvent être créés automatiquement ou n’autorisez que les mises à jour des produits existants.  
- Synchronisation des niveaux d'inventaire
  - Choisissez certains ou tous les emplacements disponibles dans [!INCLUDE [prod_short](../includes/prod_short.md)].  
  - Mettez à jour les niveaux d'inventaire sur plusieurs emplacements dans Shopify.  
- Synchronisation bidirectionnelle des clients
  - Mappez intelligemment les clients par téléphone et courriel.  
  - Utilisez des modèles spécifiques au pays lors de la création de clients, ce qui permet de garantir que les paramètres fiscaux sont corrects.  
- Importer des commandes depuis Shopify
  - Incluez les commandes créées dans différents canaux de vente, tels qu’une boutique en ligne ou d’un **PDV Shopify**. 
  - Frais d’expédition, cartes-cadeaux, pourboires, modes d’expédition et de paiement, transactions et risque de fraude.  
  - Lors de l’importation, vous pouvez créer automatiquement des clients dans [!INCLUDE [prod_short](../includes/prod_short.md)] ou décider de gérer les clients dans Shopify.  
  - Recevez des informations de paiement de Shopify Payments. 
- Suivez les informations d’exécution
  - Choisissez éventuellement de transférer des informations de suivi des articles à partir de [!INCLUDE [prod_short](../includes/prod_short.md)] dans Shopify.  

## <a name="why-did-microsoft-and-shopify-form-this-partnership" />Pourquoi Microsoft et Shopify ont-ils formé ce partenariat ?

[!INCLUDE[prod_short](../includes/prod_long.md)] fait équipe avec Shopify pour aider nos clients à créer une meilleure expérience d’achat. Shopify offre aux commerçants une solution d'e-commerce conviviale et [!INCLUDE[prod_short](../includes/prod_short.md)] offre une solution complète de gestion d’entreprise qui connecte les équipes de finances, de ventes, de services et d’opérations dans une même application. Une connexion transparente entre les deux systèmes synchronise les infos sur les commandes, le stock et les clients, afin que les commerçants puissent exécuter les commandes plus vite et fournissent un meilleur service à leurs clients.

## <a name="which-microsoft-products-are-the-shopify-connector-available-for" />Quels sont les produits Microsoft pour lesquels le connecteur Shopify est disponible ?

Cette fonction est disponible uniquement pour [!INCLUDE[prod_short](../includes/prod_short.md)] en ligne, à partir de la version 20.1. Elle n’est pas disponible pour les déploiements locaux. L’application avec le connecteur est préinstallée pour les nouveaux environnements. Les organisations disposant d’environnements existants peuvent télécharger et installer l’application à partir de AppSource. L’organisation doit disposer à la fois d’une licence Business Central et d’une licence Shopify pour utiliser le connecteur. En savoir plus sur les pays, les langues et les éditions de [!INCLUDE[prod_short](../includes/prod_short.md)] pris en charge, dans la rubrique [Connecteur Shopify sur AppSource](https://go.microsoft.com/fwlink/?linkid=2196238).

Le connecteur Shopify ne fonctionne pas pour [Intégrer les applications](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview), où l’URL du client a le format : `https://[application name].bc.dynamics.com`. 

## <a name="what-support-is-offered-for-the-shopify-connector" />Quel support est proposé pour le connecteur Shopify ?

### <a name="includeprodshortincludesprodshortmd" />[!INCLUDE[prod_short](../includes/prod_short.md)]

Le connecteur Shopify est couvert par le modèle de support actuel. En savoir plus dans la rubrique [Support technique](/dynamics365/business-central/dev-itpro/administration//manage-technical-support) (en anglais uniquement). 

Obtenez l’aide d’un consultant qui connaît le connecteur Shopify pour [!INCLUDE[prod_short](../includes/prod_short.md)], afin de répondre aux exigences spécifiques de votre entreprise.
 
Rechercher dans [Services de conseil](https://aka.ms/BCShopifyConsultant).

### <a name="shopify" />Shopify

Obtenez de l’aide concernant Shopify en commençant par accéder au [Centre d’aide Shopify général](https://help.shopify.com/) ou contactez l’[assistance 24h/24 et 7j/7 pour votre magasin en tant que commerçant Shopify](https://help.shopify.com/questions#/). 

Vous pouvez également explorer la [place de marché Experts](https://experts.shopify.com/) pour trouver les bons experts qui proposent des services aux marchands Shopify.

## <a name="currently-unsupported-features-however-were-tracking-them-and-may-consider-adding-them" />Fonctionnalités actuellement non prises en charge, cependant, nous les suivons et pourrions envisager de les ajouter à l’avenir :

- Fonctionnalités B2B, y compris les compagnies, les listes de prix des compagnies, les modalités de paiement
- Marchés
  - Traductions multiples des données de base. Vous pouvez choisir une langue qui sera utilisée pour l’exportation des informations sur les produits.
  - Prix par pays/région. Une liste de prix est disponible pour la devise sélectionnée. La conversion dans d’autres devises sera gérée par Shopify.

## <a name="is-the-shopify-connector-extensible" />Le connecteur Shopify est-il extensible ?

Actuellement, cette application n’est pas extensible avec des plans pour la rendre extensible en 2023. 

## <a name="is-the-shopify-connector-open-for-contribution" />Le connecteur Shopify est-il ouvert à la participation ?

Oui, cette extension est ouverte à la participation de la communauté. Vous pouvez trouver le [code source](https://github.com/microsoft/ALAppExtensions/tree/main/Apps/W1/Shopify) dans le référentiel des modules complémentaires de l’application Microsoft AL.


## <a name="see-also" />Voir aussi

[Mise en route du connecteur pour Shopify](get-started.md)  
