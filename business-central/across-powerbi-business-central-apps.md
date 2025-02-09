---
title: "Utiliser des applications Business\_Central dans Power BI"
description: 'Il est facile d''obtenir des informations exploitables, de la veille économique et des KPI de vos applications Business Central pour Power BI.'
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 04/01/2021
ms.author: jswymer
---
# <a name="use-the-include-prodshortincludesprodshortmd-apps-in-power-bi" />Utiliser les applications [!INCLUDE [prod_short](includes/prod_short.md)] dans Power BI

> **S’APPLIQUE À :** [!INCLUDE [prod_long](includes/prod_long.md)] en ligne 

[!INCLUDE [prod_long](includes/prod_long.md)] publie les applications Power BI suivantes, qui fournissent des tableaux de bord détaillés pour afficher les données :

- [!INCLUDE [prod_long](includes/prod_long.md)] - CRM  
- [!INCLUDE [prod_long](includes/prod_long.md)] - Finance  
- [!INCLUDE [prod_long](includes/prod_long.md)] - Sales

## <a name="overview" />Aperçu

Chaque application comprend plusieurs rapports dans lesquels vous pouvez explorer les données, y compris les fonctionnalités suivantes :

- Sélectionnez un visuel du tableau de bord pour afficher l'un des rapports sous-jacents.  
- Filtrez le rapport ou ajoutez les champs que vous souhaitez contrôler.  
- Épinglez une vue personnalisée au tableau de bord pour continuer à effectuer le suivi.  
  Vous pouvez actualiser les données manuellement, et vous pouvez configurer un calendrier d'actualisation. Pour plus d'informations, voir [Configuration d'une actualisation programmée](/power-bi/refresh-scheduled-refresh).  

Les applications sont conçues pour fonctionner avec les données de toute compagnie dans [!INCLUDE[prod_short](includes/prod_short.md)]. Lorsque vous installez l'application Power BI, spécifiez un ou plusieurs paramètres à connecter à votre [!INCLUDE [prod_short](includes/prod_short.md)].  

> [!NOTE]
> Vous pouvez également générer vos propres rapports et tableaux de bord dans Power BI selon vos données [!INCLUDE[prod_short](includes/prod_short.md)]. Pour plus d'informations, voir [Connexion de vos données métier à Power BI](across-how-use-financials-data-source-powerbi.md). 

## <a name="prerequisites" />Conditions préalables

Les applications Power BI nécessitent des autorisations sur les tables à partir desquelles les données sont extraites et les services Web utilisés pour récupérer les données. La table suivante répertorie les services Web requis pour chaque application Power BI :
    
|Application | Services Web|
|----|-------------|
|[!INCLUDE[prod_short](includes/prod_short.md)] - CRM| <ul><li>Opportunités ventes</li><li>Informations sur le modèle Excel Afficher Compagnie</li><li>Étiquettes de rapport Power BI</li></ul>|
|[!INCLUDE[prod_short](includes/prod_short.md)] - Finance| <ul><li>PowerBIFinance</li><li>Informations sur le modèle Excel Afficher Compagnie</li><li>Étiquettes de rapport Power BI</li></ul>|
|[!INCLUDE[prod_short](includes/prod_short.md)] - Sales| <ul><li>Ventes d'articles par client</li><li>Tableau de bord ventes</li><li>Informations sur le modèle Excel Afficher Compagnie</li><li>Étiquettes de rapport Power BI</li></ul>|

> [!TIP]
> Pour trouver facilement les services Web, il suffit de rechercher *services web* dans [!INCLUDE[prod_short](includes/prod_short.md)]. Sur la page **Services Web**, assurez-vous que le champ **Publier** est sélectionné pour les services Web répertoriés ci-dessus. Pour plus d’informations, voir [Publication d’un service Web](across-how-publish-web-service.md).

## <a name="get-ready" />Mise en route

Inscrivez-vous au service Power BI. Si vous ne vous êtes pas encore inscrit, accédez à [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Au moment de votre inscription, utilisez votre adresse de courriel professionnelle et votre mot de passe.

## <a name="install-a-includeprodshortincludesprodshortmd-app-in-power-bi" />Installer une application [!INCLUDE[prod_short](includes/prod_short.md)] dans Power BI

1. Ouvrez votre navigateur, accédez à [https://powerbi.microsoft.com](https://powerbi.microsoft.com) et connectez-vous à votre compte.
2. Sélectionnez **Extraire les données** en bas du volet de navigation gauche.  

    ![Naviguez pour obtenir des données.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

    Vous pouvez également démarrer depuis [!INCLUDE [prod_short](includes/prod_short.md)]. Depuis votre page d'accueil, accédez à **Sélection de rapport** dans la section Power BI. Sélectionnez **Service** ou **Mon organisation** dans le ruban. Soit la galerie Organisation dans Power BI, soit Microsoft AppSource s’ouvre, filtré pour n’afficher que les applications liées à [!INCLUDE[prod_short](includes/prod_short.md)].

3. Dans la zone **Services**, sélectionnez **Extraire**.

    Cette étape ouvre la page **Applications Power BI**, qui vous permet de rechercher l’application Power BI disponible dans **AppSource**.  

4. Dans la boîte de dialogue **Rechercher**, entrez **Dynamics 365 Business Central**.
5. Sélectionnez l’application que vous souhaitez utiliser, sélectionnez **Obtenir maintenant**, puis **Installer**.  

    Ensuite l’application sera disponible à partir d’**Applications** dans le menu de navigation dans Power BI.

## <a name="connect-the-includeprodshortincludesprodshortmd-app-to-your-data" />Connecter l’application [!INCLUDE[prod_short](includes/prod_short.md)] à vos données

1. Sous **Applications**, sélectionnez l’application Business Central, puis **Connecter**.
2. À l’invite, renseignez les champs **Nom de la compagnie** et **Environnement** avec les informations concernant l’instance [!INCLUDE[prod_short](includes/prod_short.md)] à laquelle vous souhaitez vous connecter.

    - Pour **Nom de la compagnie**, assurez-vous d’utiliser le nom complet et non le nom d’affichage. Vous pourrez trouver le nom de la compagnie dans la page **Compagnies** dans [!INCLUDE[prod_short](includes/prod_short.md)]. 
    - Pour **Environnement**, si vous n’avez pas créé plusieurs environnements, entrez **Production**.

3. Sélectionnez **Suivant**.
4. Sélectionnez **Se connecter**.
5. À l’invite, entrez le nom d’utilisateur et le mot de passe pour vous connecter à [!INCLUDE[prod_short](includes/prod_short.md)].
6. Une fois connecté(e), un tableau de bord et des rapports sont ajoutés à votre espace de travail Power BI. Une fois terminé, les mosaïques affichent les données de votre compagnie [!INCLUDE[prod_short](includes/prod_short.md)].

    ![Sélectionnez Dynamics 365 Business Central et sélectionnez Obtenir maintenant.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="fixing-problems" />Résolution des problèmes

Le tableau de bord Power BI repose sur les services Web publiés répertoriés ci-dessus. Il affiche les données de la compagnie de démonstration ou de votre propre compagnie si vous importez des données à partir de votre solution financière actuelle. Toutefois, si une erreur se produit, cette section fournit une solution de rechange pour les problèmes les plus courants.  

### <a name="you-dont-have-a-power-bi-account" />Vous n’avez pas de compte Power BI

Aucun compte Power BI n’a été créé. Vous devez avoir une licence pour obtenir un compte Power BI valide. De plus, vous devez vous être déjà connecté à Power BI pour créer votre espace de travail Power BI.  

### <a name="message-there-are-no-enabled-reports-choose-select-report-to-see-a-list-of-reports-that-you-can-display" />Message : Aucun rapport n'est activé. Choisissez Sélectionner un rapport pour afficher la liste des rapports disponibles.

Ce message apparaît si le rapport par défaut n’a pas pu être déployé sur votre espace de travail Power BI. Ou le rapport a été déployé, mais n’a pas été actualisé avec succès. Si ce problème se produit, accédez au rapport dans votre espace de travail Power BI, sélectionnez **Ensemble de données**, **Paramètres**, puis mettez à jour les informations d’identification manuellement. Une fois le jeu de données actualisé, revenez dans [!INCLUDE[prod_short](includes/prod_short.md)] et sélectionnez manuellement le rapport dans la page **Sélectionner des rapports**.

### <a name="you-need-a-power-bi-pro-license-to-install-the-includeprodshortincludesprodshortmd-app-in-power-bi" />Vous devez disposer d'une licence Power BI Pro pour installer l'application [!INCLUDE[prod_short](includes/prod_short.md)] dans Power BI

Vous avez besoin d’une [licence Power BI Pro](/power-bi/service-features-license-type) pour partager votre contenu, ainsi que les personnes avec lesquelles vous le partagez. Le contenu doit se trouver dans un espace de travail dans une [Capacité Premium](/power-bi/service-premium-what-is). Pour en savoir plus, consultez [Moyens de partager votre travail dans Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).  

### <a name="parameter-validation-failed-please-make-sure-all-parameters-are-valid" />« Échec de la validation des paramètres, assurez-vous que tous les paramètres sont valides »

Cette erreur indique qu’un ou plusieurs paramètres ne sont pas valides.

- Le paramètre d’environnement spécifié ne correspond à aucun environnement de production ou sandbox [!INCLUDE[prod_short](includes/prod_short.md)] existant.
- Le paramètre de compagnie spécifié ne correspond à aucune compagnie [!INCLUDE[prod_short](includes/prod_short.md)] existante. Vérifiez le nom de la compagnie dans la page **Compagnies** dans [!INCLUDE[prod_short](includes/prod_short.md)].
- Si vous vous connectez à [!INCLUDE[prod_short](includes/prod_short.md)] sur site, vous avez entré une URL qui n’est pas valide. Vous pouvez vérifier l’URL sur la page **Services Web** dans [!INCLUDE[prod_short](includes/prod_short.md)]  
- Un port n’est pas ouvert pour permettre à la demande de passer par votre pare-feu.

### <a name="cant-sign-in" />Connexion impossible

Si vous obtenez un message d’erreur de type échec après avoir utilisé vos informations d’identification utilisateur [!INCLUDE[prod_short](includes/prod_short.md)] pour vous connecter, vous rencontrez peut-être l’un des problèmes suivants :

- Le compte que vous utilisez n’est pas doté des autorisations nécessaires pour récupérer les données [!INCLUDE[prod_short](includes/prod_short.md)] de votre compte. Vérifiez que vous disposez des autorisations pour les données requises dans [!INCLUDE[prod_short](includes/prod_short.md)]et essayez à nouveau.
- Vous avez sélectionné un type d’authentification autre que Basique si vous vous connectez à [!INCLUDE[prod_short](includes/prod_short.md)] sur site.
- Vous n’avez pas entré de nom d’utilisateur ni de mot de passe valide.

### <a name="message-your-data-source-cant-be-refreshed-because-the-credentials-are-invalid-please-update-your-credentials-and-try-again" />Message : Votre source de données ne peut pas être actualisée, car les informations d’identification ne sont pas valides. Veuillez mettre à jour vos informations d’identification et réessayer.

Pour [!INCLUDE[prod_short](includes/prod_short.md)] sur site, le problème peut être que l’URL OData n’est exposée qu’au réseau local.

### <a name="incorrect-company-name" />Nom de compagnie incorrect

Une erreur courante consiste à entrer le nom d'affichage de la compagnie au lieu de son nom. Pour trouver le nom de la compagnie, cherchez dans **Compagnies**. Utilisez ensuite le champ **Nom** au moment de saisir le nom de votre compagnie.

### <a name="the-key-didnt-match-any-rows-in-the-table" />La clé ne correspond à aucune ligne de la table

Si vous entrez un nom de compagnie non valide pendant le processus de connexion, le message d'erreur suivant « La clé ne correspond à aucune ligne de la table » peut s'afficher. Indiquez le nom de compagnie correct, puis reconnectez-vous.

### <a name="historical-data-appears-to-be-missing" />Les données historiques semblent manquer

Une fois que l’application Power BI est installée et que vos données apparaissent dans Power BI, vous remarquerez peut-être que toutes vos données ne s’affichent pas. Les ensembles de données sont filtrés pour ne renvoyer que les 365 derniers jours de données. Cette option par défaut est en place pour accélérer les rapports.  

### <a name="i-only-see-data-for-a-single-company" />Je ne vois que des données pour une seule compagnie

L'application Power BI affichera uniquement les données de la compagnie [!INCLUDE[prod_short](includes/prod_short.md)] qui a été définie lorsque l'application Power BI a été installée. Les données provenant d'autres compagnies peuvent être ajoutées aux rapports en ajoutant de nouvelles requêtes utilisant différentes compagnies en tant que source de données.  

### <a name="what-now" />Et ensuite ?

- Cliquez sur [poser une question dans la zone Q&R](/power-bi/service-q-and-a-tips) en haut du tableau de bord.
- [Modifiez les mosaïques](/power-bi/service-dashboard-edit-tile) du tableau de bord.  
- [Sélectionnez une mosaïque](/power-bi/service-dashboard-tiles) pour ouvrir le rapport sous-jacent.  
- Par défaut, votre ensemble de données n’est pas programmé pour être actualisé. Vous pouvez modifier le calendrier d’actualisation ou essayer de l’actualiser à la demande à l’aide de **Actualiser maintenant**. Pour plus d'informations, voir [Configuration d'une actualisation programmée](/power-bi/refresh-scheduled-refresh).

## <a name="see-related-microsoft-trainingtrainingmodulesconfigure-powerbi-excel-dynamics-365-business-centralindex" />Voir la [formation Microsoft](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index) associée

## <a name="see-also" />Voir aussi

[Business Central et Power BI](admin-powerbi.md)  
[Vue d’ensemble Architecture et composante d’intégration Power BI pour [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Utiliser des données [!INCLUDE [prod_short](includes/prod_short.md)] dans Power BI](across-working-with-business-central-in-powerbi.md)  
[Création de rapports Power BI pour afficher les données [!INCLUDE [prod_long](includes/prod_long.md)]](across-how-use-financials-data-source-powerbi.md)  
[Veille économique](bi.md)  
[Se préparer aux activités commerciales](ui-get-ready-business.md)  
[Importation des données métier à partir d’autres systèmes financiers](across-import-data-configuration-packages.md)  
[Configurer [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)] comme source de données Power BI](across-how-use-financials-data-source-powerbi.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)] comme source de données Power Apps](across-how-use-financials-data-source-powerapps.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)] dans Power Automate](across-how-use-financials-data-source-flow.md)  
[Documentation Power BI](/power-bi/)  
[Qu’est-ce que Power BI ?](/power-bi/fundamentals/power-bi-overview)  
[Démarrage rapide : Se connecter aux données dans Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Présentation des datamarts](/power-bi/transform-model/datamarts/datamarts-overview)  
[Introduction aux flux de données et à la préparation des données en libre-service](/power-bi/transform-model/dataflows/dataflows-introduction-self-service)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
