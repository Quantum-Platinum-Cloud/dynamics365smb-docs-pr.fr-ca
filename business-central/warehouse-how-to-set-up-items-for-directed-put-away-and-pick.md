---
title: Configurer le prélèvement et le rangement dirigés
description: Le rangement et le prélèvement dirigés vous permettent de gérer efficacement votre entrepôt.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: null
ms.date: 11/07/2022
ms.author: bholtorf
---
# <a name="set-up-items-and-locations-for-directed-put-away-and-pick" />Configurer des articles et des emplacements pour prélèvement et rangement suggérés

Lorsque vous configurez un emplacement entrepôt pour prélèvement et rangement suggérés, vous disposez de nouvelles fonctionnalités pour vous aider à exploiter l'entrepôt le plus efficacement possible. Afin de pouvoir utiliser pleinement cette fonctionnalité, vous devez fournir des informations supplémentaires concernant les articles, permettant ainsi d'exécuter les calculs nécessaires pour suggérer les méthodes les plus efficaces pour gérer les activités de l'entrepôt. 

## <a name="to-set-up-an-item-for-directed-put-away-and-pick" />Pour configurer l'article pour prélèvement et rangement suggérés

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis choisissez le lien associé.  
2. Ouvrez la fiche de l'article que vous souhaitez configurer pour prélèvement et rangement suggérés.
3. Sur le raccourci **Entrepôt** de la fiche article, renseignez les champs pour définir la façon dont l'article doit être traité dans l'entrepôt.  
4. Choisissez l'action **Unités de mesure**.
5. Sur la page **Unités de mesure de l’article**, définissez les unités de mesure dans lesquelles l’article peut être traité en spécifiant la hauteur, la largeur, la longueur, le cubage et le poids de l’article.
6. Choisissez l'action **Contenus de la zone**.
7. Sur la page **Contenu de la zone**, définissez l'emplacement et la zone auxquels l'article doit être associé. Le champ **Par défaut** n'est pas utilisé lorsque l'emplacement est configuré pour prélèvement et rangement suggérés.  

## <a name="to-start-using-directed-put-away-and-pick" />Pour commencer à utiliser le rangement et le prélèvement dirigés

Les prélèvement et rangement suggérés permettent d'accéder à des fonctionnalités de configuration entrepôt évoluées qui peuvent améliorer considérablement votre efficacité et la fiabilité de vos données. Pour pouvoir utiliser cette fonctionnalité, vous devez tout d'abord définir divers paramètres dans votre entrepôt.  

Pour utiliser la fonctionnalité prélèvement et rangement suggérés, vous devez l'activer dans la fiche emplacement.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Emplacements**, puis choisissez le lien associé.  
2. Sélectionnez l'emplacement dans lequel vous souhaitez utiliser les prélèvement et rangement suggérés, puis choisissez l'action **Modifier**.  
3. Sur le raccourci **Entrepôt**, cochez la case **Prélèv. et rangement suggérés**.  

À ce stade de la configuration, il n'est pas nécessaire de renseigner d'autres champs de la fiche emplacement.  

> [!NOTE]  
> Lorsque l’emplacement possède des écritures articles ouvertes, vous ne pouvez pas configurer l’entrepôt pour qu’il utilise des zones.  

L'étape suivante consiste à définir le type d'emplacement que vous souhaitez exploiter. Pour plus d'informations, voir [Configurer des types de zone](warehouse-how-to-set-up-bin-types.md). Le type de zone définit la manière d'utiliser une zone donnée lors du traitement du flux d'articles dans l'entrepôt. Vous pouvez affecter un type de zone à une zone et à une zone.  

Vous pouvez également définir des codes classe entrepôt si l’entrepôt comprend des articles nécessitant des conditions de stockage particulières. Les codes classe entrepôt sont utilisés lors de la suggestion du placement des articles dans des zones. Vous affectez les codes classe entrepôt à des groupes de produits, qui sont ensuite affectés à des articles et des unités de stock, ou à des zones qui prennent en charge les conditions de stockage requises par ces codes classe entrepôt.  

Vous êtes maintenant prêt à configurer des zones, si vous le souhaitez. L'utilisation de zones réduit le nombre de champs à renseigner lors de la configuration des emplacements, étant donné que les emplacements créés dans une zone héritent de plusieurs propriétés de cette zone. Les zones peuvent également faciliter l'orientation des nouveaux employés ou des intérimaires dans l'entrepôt. Notez que le flux est contrôlé par des emplacements ; vous pouvez donc choisir d'utiliser plusieurs emplacements et une seule zone.  

## <a name="to-set-up-a-zone-in-your-warehouse" />Pour configurer une zone de l'entrepôt

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Emplacements**, puis choisissez le lien associé.  
2. Sélectionnez l'emplacement dans lequel vous souhaitez configurer une zone et ouvrez la fiche emplacement, puis choisissez l'action **Zones**.  
3. Renseignez les champs nécessaires sur la page **Zones**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Lorsque vous modifiez le paramètre d'une zone, tous les emplacements créés par la suite dans cette zone disposent des nouvelles caractéristiques, mais les emplacements d'origine ne sont pas modifiés.  

> [!NOTE]  
> Si vous ne souhaitez pas utiliser de zones, vous devez néanmoins spécifier un code zone non défini, à l'exception du code.  

L’étape suivante consiste à définir des zones. Pour en savoir plus, voir [Configurer des emplacements de sorte qu’ils utilisent des zones](warehouse-how-to-set-up-locations-to-use-bins.md).  

En outre, vous devez créer des modèles et les périodes d'inventaire de rangement. Learn more at [Configurer des modèles rangement](warehouse-how-to-set-up-put-away-templates.md).  

## <a name="see-also" />Voir aussi

[Vue d’ensemble de Warehouse Management](design-details-warehouse-management.md)
[Inventaire](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)     
[Gestion d'assemblage](assembly-assemble-items.md)    
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
