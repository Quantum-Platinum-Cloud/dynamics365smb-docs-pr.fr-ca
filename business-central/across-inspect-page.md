---
title: Inspection des pages dans Business Central
description: Utilisez la fonction Inspection des pages pour en savoir plus sur le format et la source de données des pages. L'inspecteur de page convient parfaitement pour le dépannage de vos données.
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: conceptual
author: jswymer
ms.author: jswymer
ms.date: 04/01/2021
---

# <a name="inspecting-pages-in-business-central" />Inspection des pages dans Business Central

La fonction Inspection des pages vous permet d'obtenir des détails sur une page : elle vous donne ainsi un aperçu du format de la page, des différents éléments qui la constituent ainsi que de la source qui se cache derrière les données qu'elle diffuse. La fonction Inspection des pages est conçue notamment pour les administrateurs, les utilisateurs avancés, le personnel du support technique ainsi que les développeurs. Elle est parfaite pour découvrir quel modèle de données se cache derrière une page et pour le dépannage. Par exemple, si vous rencontrez un problème avec une page, vous pouvez utiliser la fonction d'inspection des pages pour obtenir les informations à transmettre à votre administrateur système ou à votre personnel du support technique.

[!INCLUDE [send-report-excel](includes/send-report-excel.md)]

## <a name="work-with-page-inspection" />Utiliser la fonction Inspection des pages

Vous commencez l'inspection des pages dans la page **Aide et support**. Cliquez sur le point d'interrogation dans le coin supérieur droit, sur **Aide et support**, puis sur **Inspecter les pages et les données**. Sinon, vous pouvez utiliser le raccourci clavier <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>F1</kbd>.

Le volet **Inspection des pages** s'ouvre sur le côté. Lorsque le volet s’ouvre pour la première fois, il affiche les informations qui concernent le principal objet de la page.

Utilisez le clavier ou le dispositif de pointage pour déplacer le focus vers différents éléments de la page. Lorsque vous sélectionnez un élément de type Récapitulatif ou une partie de la page principale, la zone de délimitation est mise en avant par une bordure, et le volet **Inspection des pages** présente les informations relatives à l'élément sélectionné. Par exemple, l'image précédente présente les informations relatives à la partie de la liste sur la page **Document de vente**. Lorsque vous accédez à d'autres pages de l'application, le volet **Contrôle de page** se met automatiquement à jour avec les informations de la page au fur et à mesure de votre navigation.

Pour en savoir plus sur ce que permet d'afficher la fonction d'inspection des pages, reportez-vous à la rubrique [Pages relatives à l'inspection et au dépannage](/dynamics365/business-central/dev-itpro/developer/devenv-inspecting-pages) dans l'aide dédiée aux professionnels de l'informatique et aux développeurs Business Central.

Si vous ne voyez pas les détails auxquels vous vous attendez sur le volet **Inspection des pages**, vous n'avez probablement pas les autorisations requises, comme le décrit la section suivante.

## <a name="controlling-access-to-page-inspection-details" />Contrôle de l’accès aux détails relatifs à l’inspection des pages

En tant qu'administrateur, vous pouvez contrôler l'accès aux détails complets qui s'affichent dans le volet **Inspection des pages** en configurant les autorisations des utilisateurs. Pour accorder une autorisation d'accès aux détails complets à un utilisateur, accordez l'autorisation **Exécuter** à l'utilisateur sur l'objet **Système** **5330**. Vous pouvez accorder cette autorisation à l'aide d'un ensemble d'autorisations (comme **Résolution de D365**) ou d'un groupe d'utilisateurs (comme **Résolution de D365**). Pour en savoir plus sur les autorisations, voir [Attribuer des autorisations aux utilisateurs et aux groupes](ui-define-granular-permissions.md).

Les utilisateurs qui ne disposent pas des autorisations sur **Objet système 5330** peuvent toujours accéder au volet **Inspection des pages**, mais ils n'ont accès qu'aux champs **Page** et **Table**, qui présentent les détails de base qu'ils sont en mesure de transmettre à leur équipe de support technique.

## <a name="see-also" />Voir aussi .

[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
