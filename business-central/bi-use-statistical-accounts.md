---
title: Utiliser les comptes statistiques pour l’analyse des données non transactionnelles
description: Décrit comment utiliser les comptes statistiques comme autre source de données pour vos analyses.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/07/2023
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, financial report'
ms.search.form: '2632, 2631, 2633, 2623, 2634'
---
# <a name="analyze-data-with-statistical-accounts" />Analyse des données avec les comptes statistiques

Utilisez des comptes statistiques pour compléter les informations dans les rapports financiers. Les comptes statistiques vous permettent d’ajouter des mesures basées sur des données non transactionnelles. Vous ajoutez les données non transactionnelles en tant qu’unités numériques, telles que :

* Effectif des employés
* Pieds carrés
* Le nombre de clients avec des comptes en souffrance

Par exemple, vous pouvez mesurer les revenus ou les coûts en fonction du nombre de personnes dans un service. L’effectif du département est l’unité du compte statistique. L’image suivante montre un exemple de rapport qui utilise un compte statistique pour afficher les revenus par employé.

:::image type="content" source="media/statistical account report example.png" alt-text="Un exemple de rapport qui inclut les données d’un compte statistique.":::

En termes de fonctionnement, les comptes statistiques sont similaires aux comptes de report. Ils stockent les transactions que vous reportez à l’aide de journaux de comptes statistiques, afin que vous puissiez utiliser les transactions comme données pour les rapports financiers. Pour en savoir plus sur les rapports financiers, accédez à [Préparer Financial Reporting avec des données financières et des catégories de compte](bi-how-work-account-schedule.md). 

Il existe quelques différences essentielles entre les comptes statistiques et les comptes de report. Les comptes statistiques sont des entités distinctes et ne sont pas inclus dans les rapports de balance de vérification générale. En outre, vous n’avez pas besoin d’équilibrer les montants débiteurs et créditeurs lorsque vous utilisez des journaux de comptes statistiques pour reporter des écritures sur un compte statistique. Vous venez de reporter le montant.

## <a name="set-up-a-statistical-account" />Configurer un compte statistique

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Comptes statistiques**, puis sélectionnez le lien associé.
1. Renseignez les champs du raccourci **Général**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="post-amounts-to-a-statistical-account" />Reporter des montants sur un compte statistique

1. Pour reporter les montants que vous souhaitez suivre, sur la page **Comptes statistiques**, choisissez l’action **Journal comptes statistiques**.
1. Dans le champ **Date de report**, entrez la dernière date de la période de report pour laquelle vous souhaitez reporter les montants.
1. Facultatif : Si vous souhaitez suivre les montants d’un document spécifique, dans le champ **N° de document**, saisissez le code du document.
1. Dans le champ **N° de compte statistique**, choisissez le compte statistique sur lequel vous reporterez les montants.
1. Dans le champ **Description**, saisissez une brève description de ce que vous mesurez.  
1. Dans le champ **Montant**, entrez le total à reporter. 
1. Facultatif : Si vous souhaitez inclure le compte statistique dans des analyses plus avancées, spécifiez les dimensions dans les champs **Code emplacement immo** et **Code groupe clients**. Pour en savoir plus sur les dimensions, accédez à [Analyser les données par dimensions](bi-how-analyze-data-dimension.md).

## <a name="verify-statistical-account-amounts" />Vérifier les montants sur un compte statistique

Sur la page **Comptes statistiques** , utilisez l’action **Solde des comptes statistiques** pour vérifier que les montants enregistrés sont corrects pour chaque période.  

## <a name="include-the-statistical-account-in-a-financial-report" />Inclure le compte statistique dans un rapport financier

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Rapports financiers**, puis choisissez le lien associé.
1. Créez un rapport financier de l’une des manières suivantes :
    1. Pour recommencer à zéro, choisissez **Nouveau**. Pour en savoir plus sur la création de rapports financiers, accédez à [Créer un rapport financier](bi-how-work-account-schedule.md#create-a-new-financial-report).
    1. Pour utiliser les paramètres d’un rapport similaire que vous possédez déjà, choisissez le rapport à copier, puis choisissez l’action **Copier le rapport financier**. Vous pouvez modifier les paramètres que vous copiez dans votre nouveau rapport.
1. Ajouter le compte statistique :
    1. Si vous partez de zéro, choisissez l’action **Modifier la définition de ligne**.
    1. Pour utiliser une définition de ligne depuis un rapport existant, choisissez le rapport à copier, puis choisissez l’action **Copier la définition de ligne**.
1. Sur la page **Définition de ligne**, dans le champ **N° de ligne**, définissez où la ligne s’affiche dans la séquence de lignes sur le rapport.
1. Dans le champ **Description**, saisissez le texte qui indique ce que vous mesurez.
1. Dans le champ **Type de totalisation**, choisissez **Comptes statistiques**.
1. Dans le champ **Totalisation**, choisissez un compte statistique.
1. Dans le champ **Type de ligne**, choisissez d’afficher le solde à la date de report ou au début de la période de report, ou d’afficher la modification du montant au cours de la période.
1. Renseignez les champs restants. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also" />Voir aussi

[Décisionnel pour le secteur de la finance](bi.md)  
[Rapports et analyses financiers dans Business Central](finance-reports.md)
