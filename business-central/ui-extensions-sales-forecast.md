---
title: Utilisation de l'extension Prévisions de ventes et d'inventaire pour gérer l'inventaire | Microsoft Docs
description: 'Cette extension vous aide à prévoir les ventes, avoir un aperçu clair des ruptures de stock prévues, et même de vous aider à créer des demandes de réapprovisionnement aux fournisseurs.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'app, add-in, manifest, customize, budget'
ms.search.form: '1850, 1851, 1853,'
ms.date: 12/20/2021
ms.author: edupont
---

# <a name="the-sales-and-inventory-forecast-extension" />Extension Prévision des ventes et de l'inventaire

La gestion de l'inventaire est un compromis entre le service client et la gestion de vos coûts. D'une part, un inventaire faible exige un capital de travail inférieur, mais d'autre part, les ruptures d'inventaire mènent potentiellement à des ventes non concrétisées. L'extension Prévision des ventes et de l'inventaire prévoit les ventes potentielles à l'aide des données historiques et donne une présentation claire des ruptures d'inventaire prévues. Selon la prévision, l'extension aide à créer des demandes de réapprovisionnement auprès de vos fournisseurs et vous fait gagner du temps.  

## <a name="setting-up-forecasting" />Paramétrage des prévisions

Dans [!INCLUDE[prod_short](includes/prod_short.md)], connexion à [Azure AI](https://azure.microsoft.com/overview/ai-platform/) est déjà configurée pour vous. Mais vous pouvez configurer les prévisions pour utiliser un autre type de période pour exécuter votre rapport, par exemple en passant des prévisions mensuelles aux prévisions trimestrielles. Vous pouvez également choisir le nombre de périodes à partir desquelles calculer les prévisions, selon le degré de granularité que vous souhaitez accorder à vos prévisions. Nous vous proposons de faire des prévisions mensuelles avec un horizon à 12 mois.

> [!TIP]  
> Tenez compte de la durée des périodes utilisée par le service lors de ses calculs. Plus vous fournissez de données, plus les prévisions seront précises. En outre, soyez prudent en ce qui concerne les grands écarts entre les périodes. Cela aura également un impact sur les prévisions. Si Azure AI ne trouve pas suffisamment de données ou si les données varient considérablement, le service ne fera pas de prévisions.

## <a name="use-the-forecasts" />Utiliser les prévisions

Cette extension utilise Azure AI pour prévoir les ventes futures en fonction de votre historique des ventes pour vous aider à éviter les ruptures d'inventaire. Par exemple, lorsque vous choisissez un article sur la page **Articles**, le graphique du volet **Prévision des articles** affiche les ventes estimées de cet article dans la période à venir. Ainsi vous pouvez voir si vous risquez d'être bientôt en rupture de stock pour l'article.  

Vous pouvez également utiliser l'extension pour suggérer quand réapprovisionner l'inventaire. Par exemple, si vous créez une bon de commande pour Fabrikam, car vous souhaitez acheter sa nouvelle chaise de bureau, l'extension Prévisions de l'inventaire et ventes prévues vous suggèrera également de réapprovisionner la chaise dactylo LONDON que vous achetez généralement auprès de ce fournisseur. En effet, les prévisions de l'extension indiquent que vous allez arriver en rupture de stocks concernant la chaise dactylo LONDON dans les deux prochaines semaines. Aussi, nous vous recommandons de commander davantage de chaises dès à présent.  

## <a name="design-details" />Détails de conception

Les abonnements à [!INCLUDE[prod_short](includes/prod_short.md)] fournissent un accès à plusieurs services web prévisionnels dans toutes les régions où [!INCLUDE[prod_short](includes/prod_short.md)] est disponible. Pour en savoir plus, consultez le guide des licences Microsoft Dynamics 365 Business Central. Le guide est téléchargeable sur le site Internet [Business Central](https://dynamics.microsoft.com/en-us/business-central/overview/). 

Ces services web sont sans état. Autrement dit, ils utilisent des données uniquement pour calculer des prévisions à la demande. Ils ne stockent pas de données.

> [!NOTE]  
>   Vous pouvez également utiliser votre propre service web prévisionnel au lieu du nôtre. Pour en savoir plus, consultez [Créer et utiliser votre propre service web prévisionnel pour les prévisions de l'inventaire et les ventes prévues](#AnchorText). 

### <a name="data-required-for-forecast" />Données requises pour les prévisions

Pour établir des prévisions sur les ventes futures, le service web nécessite des données quantitatives sur les ventes passées. Ces données proviennent des champs **Date de report**, **N° article** et **Quantité** sur la page **Écritures article**, où :

- Le type d'écriture est « Vente ».
- La date de report se situe entre la date calculée sur la base des valeurs dans les champs **Périodes historiques** et **Type de période** sur la page **Configuration des prévisions de l'inventaire et des ventes prévues** et la date de travail.

Avant d'utiliser le service web, [!INCLUDE[prod_short](includes/prod_short.md)] comprime les transactions par **N° article** et **Date de report** sur la base de la valeur dans le champ **Type de période** sur la page **Configuration des prévisions de l'inventaire et des ventes prévues**.

## <a name="a-nameanchortext-acreate-and-use-your-own-predictive-web-service-for-sales-and-inventory-forecasts" /><a name="AnchorText"></a>Créer et utiliser votre propre service web prévisionnel pour les prévisions de l'inventaire et les ventes prévues

Vous pouvez aussi utiliser votre propre service Web prévisionnel basé sur un modèle public intitulé **Modèle de prévision pour Microsoft Business Central**. Ce modèle prévisionnel est disponible en ligne dans la galerie Azure AI. Pour utiliser le modèle, procédez comme suit :  

1. Ouvrez un navigateur et accédez à la [Galerie Azure AI](https://go.microsoft.com/fwlink/?linkid=828352).  
2. Recherchez **Modèle prévisionnel pour Microsoft Business Central**, puis ouvrez-le dans Azure Machine Learning Studio.  
3. Utilisez votre compte Microsoft pour enregistrer un espace de travail, puis copiez le modèle.  
4. Exécutez le modèle, et publiez-le comme service Web.  
5. Notez l'URL d'API et la clé d'API. Vous allez utiliser ces informations d'identification pour une configuration de trésorerie.  
6. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Configuration de la prévision des ventes et de l’inventaire**, puis sélectionnez le lien associé.  
7. Développez le raccourci **Général**, puis renseignez les champs URL d'API et Clé d'API.  

## <a name="see-related-microsoft-trainingtrainingmodulesuse-sales-inventory-forecast-extension" />Voir la [formation Microsoft](/training/modules/use-sales-inventory-forecast-extension/) associée

## <a name="see-also" />Voir aussi .

[Ventes](sales-manage-sales.md)  
[Stock](inventory-manage-inventory.md)  
[Personnalisation de [!INCLUDE[prod_short](includes/prod_short.md)] à l'aide des extensions](ui-extensions.md)  
[Utiliser l’intelligence artificielle dans Microsoft Dynamics 365 Business Central](/training/paths/use-artificial-intelligence/)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
