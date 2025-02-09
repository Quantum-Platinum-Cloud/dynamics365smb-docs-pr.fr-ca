---
title: Tracer des articles - Articles suivis
description: 'Vous pouvez voir où un article suivi a été utilisé, y compris le mode et le moment de réception, de production ou de retour avec les fonctionnalités de traçabilité et de recherche des écritures.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.forms: '6520,'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="trace-item-tracked-items" />Tracer des articles - Articles suivis

Vous pouvez voir où un article suivi a été utilisé, y compris le mode et le moment de réception ou de production, de transfert, de vente, de consommation ou de retour. Vous pouvez également rechercher toutes les instances d'informations d'un numéro de série ou de lot particulier dans la base de données. Vous procédez à l’aide des fonctionnalités Traçabilité et [Rechercher des écritures](ui-find-entries.md).  

Ces fonctions sont particulièrement utiles pour le contrôle qualité, lorsque vous devez déterminer quels clients ont reçu des produits correspondant à un numéro de lot particulier ou le lot dont provenait une composante défectueuse.  

 Sur la page **Traçabilité article**, vous pouvez effectuer une traçabilité en aval et en amont dans une série de transactions d'inventaire reportées pour le numéro de lot ou de série.  

 Sur la page **Rechercher des écritures**, vous ne pouvez pas voir la séquence de transactions, mais vous pouvez afficher tous les enregistrements des numéros de série ou de lot, à la fois les écritures reportées et les enregistrements ouverts.  

 Les deux fonctions peuvent être utilisées en association en transférant un numéro de série ou de lot suivi sur la page **Rechercher des écritures** pour terminer un scénario complet de suivi. <!-- For more information, see [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md).   -->

## <a name="to-trace-item-tracked-items" />Pour tracer des articles suivis

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Traçabilité**, puis choisissez le lien associé.  
2.  Dans les champs de filtre dans le haut de la page, entrez les numéros d'article spécifiques ou un filtre pour les numéros d'article que vous voulez suivre.  
3.  Dans le champ **Afficher composantes**, sélectionnez si vous voulez aussi voir d’où provenaient les composantes des articles. Le tableau suivant décrit les options.  

    |Champ|Description|  
    |----------------------------------|---------------------------------------|  
    |**Non**|Ne plus afficher les composantes.|  
    |**Avec traçabilité uniquement**|Afficher uniquement les composantes qui ont des numéros de lot ou de série.|  
    |**Tous**|Afficher tous les composantes.|  

4.  Dans le champ **Méthode de suivi**, sélectionnez la méthode à utiliser pour suivre l’article. Le tableau suivant décrit les options.  

    |Champ|Description|  
    |----------------------------------|---------------------------------------|  
    |**Utilisation->origine**|Suivez l’article à l’endroit où il a été utilisé jusqu’à l’endroit d’où il vient. Par exemple, si un article fabriqué a été vendu à un client, la page **Traçabilité** présente ce dernier en montrant d'abord la ligne livraison vente, que vous pouvez développer pour voir le bon de production dont il provenait.|  
    |**Origine->utilisation**|Suivez l’article à partir de l'endroit dont il provient dans l'inventaire jusqu'à l'endroit où il a été utilisé. Par exemple, si un article fabriqué a été vendu à un client, la page **Traçabilité** présente ce dernier en montrant d’abord le bon de production terminé, que vous pouvez développer pour voir les lignes livraison vente où l’article a été utilisé.|  

5.  Sélectionnez l'action **Suivi** pour exécuter le suivi.  

> [!NOTE]  
>  Seules les transactions affectées sont affichées. Si vous avez reçu le même lot sur plusieurs transactions, la page **Traçabilité** peut ne pas afficher toutes les transactions.   

> [!NOTE]  
>  Si l'historique d'une transaction supplémentaire dans une ligne traçabilité a déjà été suivi par une autre ligne au-dessus de celle-ci, la case à cocher **Déjà tracé** est activée. Pour une vue plus simple, ces lignes sous-jacentes ne s'affichent pas.  
>   
>  Pour trouver les lignes traçabilité où l'historique des transactions a déjà été suivi, cliquez sur le bouton **Aller sur déjà tracé**. La ligne traçabilité en question est sélectionnée et toutes les lignes sous-jacentes sont développées.  

## <a name="to-find-item-tracked-items-with-find-entries" />Pour rechercher des articles suivis avec Rechercher des écritures

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Rechercher des écritures**, puis sélectionnez le lien associé.  
2. Choisissez **Actions** > **Rechercher par** > **Rechercher par référence d’article**.
3. Dans les champs **N° de série** et **N° lot**, entrez les numéros traçabilité que vous voulez suivre.  
4. Sélectionnez l'action **Rechercher** pour rechercher toutes les instances du numéro de série ou de lot dans la base de données.  

## <a name="see-related-microsoft-trainingtrainingmodulesprepare-item-tracking" />Voir la [formation Microsoft](/training/modules/prepare-item-tracking/) associée

## <a name="see-also" />Voir aussi .

[Stock](inventory-manage-inventory.md)  
[Utiliser les numéros lot, de série et paquet](inventory-how-work-item-tracking.md)  
[Détails de conception : traçabilité](design-details-item-tracking.md)  
[Détails de conception : traçabilité et réservations](design-details-item-tracking-and-reservations.md)  
[Réserver des articles](inventory-how-to-reserve-items.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
<!-- [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md)   -->
[Rechercher des écritures](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
