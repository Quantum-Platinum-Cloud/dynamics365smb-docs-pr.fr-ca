---
title: Configurer et publier des services Web de KPI basés sur des rapports financiers
description: Cet article décrit comment afficher les données de KPI d’rapport financier basées sur des rapports financiers spécifiques.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/16/2022
ms.custom: bap-template
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
---
# <a name="set-up-and-publish-kpi-web-services-based-on-financial-reports" />Configurer et publier des services Web de KPI basés sur des rapports financiers

La page **Rapport financier - Configuration du service web KPI** vous permet de configurer la manière dont les données des KPI (indicateurs de performances clés) des rapports financiers sont affichées, et sur quels rapports financiers spécifiques baser les KPI. Lorsque vous sélectionnez **Publier le service Web**, les données de KPI du rapport financier spécifié sont ajoutées à la liste des services Web publiés sur la page **Services web**.

> [!NOTE]
> Si vous utilisez ce service Web, les dates de fermeture ne sont pas incluses dans votre ensemble de données. Vous pouvez utiliser des filtres dans Power BI pour analyser différentes périodes.

## <a name="set-up-and-publish-a-kpi-web-service-based-on-financial-reports" />Configurer et publier des services Web de KPI basés sur des rapports financiers
  
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Configuration du service Web de KPI des rapports financiers**, puis choisissez le lien associé.
2. Renseignez les champs du raccourci **Général**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Sur le raccourci **Définitions de ligne**, renseignez les champs.
4. Répétez l’étape 3 pour tous les rapports financiers sur lesquels vous souhaitez baser le service Web de KPI des rapports financiers.  
5. Pour visualiser ou modifier le rapport financier sélectionné, sur le raccourci **Définitions de ligne**, choisissez l’action **Modifier la définition de ligne**.
6. Pour afficher les données de KPI du rapport financier que vous avez défini, choisissez l’action **Service Web de KPI des rapports financiers**.
7. Pour publier le service Web de KPI du rapport financier, choisissez l’action **Publier le service Web**.

Vous pouvez désormais créer des rapports financiers dans Power BI basés sur le ou les services Web que vous avez créés.

> [!NOTE]  
> Vous pouvez également publier le service Web de KPI en pointant vers l’objet de page **Configuration du service web de KPI des rapports financiers** à partir de la page **Services web**. Pour plus d’informations, consultez [Publier un service Web](across-how-publish-web-service.md).

## <a name="see-also" />Voir aussi .

[Décisionnel pour le secteur de la finance](bi.md)  
[Finance](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Les écritures comptables et le plan comptable](finance-general-ledger.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
