---
title: 'Configuration du suivi des articles avec les numéros lot, de série et paquet'
description: 'Configurer le suivi des articles avec numéros de série, numéros de lot et numéros de colis'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 08/31/2021
ms.author: edupont
---
# <a name="set-up-item-tracking-with-serial-lot-and-package-numbers" />Configuration du suivi des articles avec les numéros lot, de série et paquet

Effectuez le suivi des articles en inventaire même dans des configurations d'entrepôt complexes avec des numéros spécifiques à chaque article, que ce soit en tant qu'objet individuel, en tant que lot ou en tant que colis. Avec le suivi des articles, vous pouvez suivre les articles à travers les mouvements d'entrepôt internes et les documents sortants et entrants.

Les articles portant des numéros de série et lot peuvent être suivis en amont et en aval de la chaîne d’approvisionnement. Cela est utile pour l'assurance qualité générale et pour les rappels de produit. Pour plus d'informations, voir [Tracer des articles suivis](inventory-how-to-trace-item-tracked-items.md).  

> [!TIP]
> Dans la 1re vague de lancement 2021 et ultérieure, activez la mise à jour de la fonctionnalité *Utiliser le suivi par numéro de colis dans le système de réservation et de suivi* si vous souhaitez travailler avec des numéros de colis ainsi que des numéros de série et de lot. Pour plus d’informations, consultez [Activer les fonctionnalités à venir à l’avance](admin-feature-management.md). Une fois la fonction activée, vous pouvez attribuer des numéros de colis aux documents sortants et entrants de la même manière que vous pouvez travailler avec des numéros de lot.  

## <a name="numbers-and-item-tracking" />Numéros et traçabilité

Dans le cadre de vos processus d′entrepôt, vous pouvez regrouper votre stock dans des emballages, des boîtes, des conteneurs, etc. Mais afin de garder une trace des articles, vous attribuez des numéros uniques comme identification. Par exemple, vous fabriquez et vendez une chaise qui porte le numéro d'article *1900-S*. Chaque chaise individuelle a un numéro de série, *1001*, mais vous regroupez également quatre chaises en un lot, *LOT0001*, et vous livrez les chaises dans un conteneur avec le numéro de colis *CONTENEUR010* qui comprend également d'autres éléments, tels que *LOT0100* avec des tables d'appoint, et *LOT200* avec des lampes.  

En fonction de votre configuration, vous utilisez ces différents numéros pour suivre l'inventaire dans [!INCLUDE [prod_short](includes/prod_short.md)] aux différentes phases des achats, des ventes, des opérations d'entrepôt, etc.

## <a name="to-set-up-item-tracking-codes" />Pour configurer les codes traçabilité

Les codes traçabilité reflètent les différents positionnements d'une compagnie par rapport à l'utilisation des numéros de série et de lot pour les articles qu'elle traite.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Codes traçabilité**, puis choisissez le lien associé.  
2. Sélectionnez l'action **Nouveau**.
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Sur les raccourcis **N° de série**, **N° lot**, et le **N° paquet**, définissez des règles de traçabilité par numéros de série, de lot et de paquet respectivement.  

> [!NOTE]  
> Si vous souhaitez suivre des articles spécifiques ou des lots spécifiques tout au long de leur durée de vie, vous devez sélectionner les champs **NS - Traçabilité spéc.** et **N° lot - Traçabilité spéc.**, respectivement. Par conséquent, lorsque vous gérez une unité sortante d'un article avec ce code traçabilité, vous devez toujours spécifier le numéro de série existant ou le numéro de lot existant à gérer. Ainsi, lorsque vous vendez une unité de cet article, elle doit être associée à un groupe précis de numéros de série ou à un numéro de lot spécifique dans l'inventaire. Autrement dit, le numéro de série ou le numéro de lot affecté à l'article lors de son entrée dans l'inventaire doit suivre ce type d'article lors de sa sortie de l'inventaire.

Comme ce champ de configuration couvre toutes les transactions réalisables avec cet article, les différents champs Enlogement/Désenlogement sont également sélectionnés. Ces champs n'ont toutefois aucun rapport avec une quelconque application dans l'inventaire ; ils définissent simplement le flux de travail de votre compagnie en ce qui concerne le moment de l'affectation des numéros traçabilité.  

> [!NOTE]  
> Pour affecter des numéros traçabilité dans les activités entrepôt, les champs **NS – Traçabilité entrepôt** et **N° lot – Traçabilité entrepôt** doivent être sélectionnés sur la fiche code de la traçabilité de l’article.  

## <a name="to-set-up-expiration-rules-for-serial-or-lot-numbers" />Pour configurer des règles d'expiration pour les numéros de série ou de lot

Pour certains articles, vous pouvez configurer des règles et des dates d'expiration spécifiques dans le code traçabilité. Cette fonctionnalité permet d'effectuer le suivi de la date d'expiration de numéros de série et de lot spécifiques.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Codes traçabilité**, puis choisissez le lien associé.
2. Sélectionnez un code traçabilité existant, puis sélectionnez l'action **Modifier**.  
3. Sur le raccourci **Divers**, sélectionnez les champs suivants :  

    |Champ|Description|  
    |---------------------------------|---------------------------------------|  
    |**Date expiration stricte**|Spécifie qu'une date d'expiration affectée au numéro de traçabilité lors de son entrée dans l'inventaire doit être respectée lors de sa sortie de l'inventaire.|  
    |**Demander une entrée de date expiration**|Spécifie que vous devez saisir une date d’expiration dans la ligne traçabilité.|  
    |**Utiliser les dates d’expiration**|Indique que vous souhaitez calculer les dates d’échéance. |  

## <a name="to-set-up-warranties-for-serial-or-lot-numbers" />Pour configurer des garanties pour les numéros de série ou de lot

Pour certains articles, vous souhaitez peut-être configurer des garanties spécifiques dans le code traçabilité. Cette fonctionnalité vous permet d'effectuer le suivi de la date d'expiration des garanties de numéros de série ou de lot spécifiques de votre inventaire.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Codes traçabilité**, puis choisissez le lien associé.  
2. Sélectionnez un code traçabilité existant, puis sélectionnez l'action **Modifier**.  
3. Sur le raccourci **Divers**, renseignez le champ **Formule date garantie**, puis sélectionnez les champs comme suit :  

    |Champ|Description|  
    |---------------------------------|---------------------------------------|  
    |**Formule date garantie**|Indique le dernier jour de garantie pour l'article.|  
    |**Demander la saisie d’une date de garantie**|Indique que vous devez saisir une date de garantie dans la ligne traçabilité.|  


## <a name="to-set-up-items-for-tracking-with-the-correct-item-tracking-codes" />Pour configurer les articles pour le suivi avec les bons codes traçabilité

Pour activer la traçabilité, vous devez d’abord attribuer les codes traçabilité à un article. Il existe deux façons d’ajouter des codes traçabilité, en sélectionnant le code dans une liste prédéfinie ou en attribuant un nouveau code unique. Positionnez le curseur sur les champs pour lire une brève description.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Article**, puis choisissez le lien associé.
2. Sélectionnez un élément existant dans la liste et ouvrez la page **Fiche article**.  
3. Sur le raccourci **Traçabilité**, attribuez les codes traçabilité appropriés et choisissez les **Code traçabilité**, **N° de série** et **N° lot**.
    1. Vous pouvez également créer un code traçabilité en sélectionnant l’action **Nouveau**.

## <a name="to-specify-opening-balances-for-the-items-you-track" />Pour spécifier les soldes d’ouverture des articles que vous suivez

Vous pouvez créer des soldes d’ouverture pour les articles que vous suivez. Étant donné que vous pouvez choisir différentes configurations d’entrepôt, deux options sont disponibles :

* Activez des lots spécifiques sur la page **Journal article** pour permettre aux utilisateurs de saisir les données de série, de lot et de package directement sur les lignes journal.
* Pour les emplacements où le bouton bascule **Prélèv. et rangement dirigés** est activé, utilisez la page **Journal inventaire entrepôt** pour rendre tous les champs de traçabilité disponibles. Les champs disponibles comprennent les champs **Date garantie** et **Date expiration**.

### <a name="item-journals" />Journaux article

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Journaux article**, puis choisissez le lien associé.
2. Choisissez le champ **Nom** pour ouvrir une liste de lots journal article.
3. Choisissez **Nouveau** pour créer un nouveau lot, puis activez le bouton bascule **Traçabilité sur les lignes**.
4. Choisissez **OK** pour sélectionner le lot que vous avez créé.
5. Renseignez les champs sur la ligne journal article selon vos besoins. Notez que les champs **N° lot**, **N° série**, **Date expiration**, **Date garantie** et **N° paquet** sont disponibles (si la fonctionnalité est activée).
6. Choisissez l’action **Reporter** pour ajuster l’inventaire.

> [!NOTE] 
> [!INCLUDE [prod_short](includes/prod_short.md)] effectue quelques validations mineures lorsque vous saisissez ou importez des données. Une vérification plus complète se produit lorsque vous reportez ou transférez des données des lignes journal vers la **Fenêtre de traçabilité**. Cette dernière se produit automatiquement lorsque vous ouvrez la page **Fenêtre de traçabilité** à partir de la ligne journal article ou si vous choisissez l’option **Mettre à jour les lignes traçabilité**.

### <a name="warehouse-physical-inventory-journal-for-locations-where-directed-pick-and-put-away-is-turned-on" />Journal inventaire entrepôt pour les emplacements où le prélèvement et le rangement dirigés sont activés

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Journal inventaire entrepôt**, puis choisissez le lien associé.
2. Renseignez les champs sur la ligne journal article selon vos besoins. Notez que les champs **N° lot**, **N° série**, **Date expiration**, **Date garantie** et **N° paquet** sont disponibles (si la fonctionnalité est activée).
3. Choisissez l’action **Enregistrer** pour créer des ajustements d’inventaire. N’oubliez pas que vous devez synchroniser les écritures entrepôt ajustées avec les écritures article associées. Pour en savoir plus, consultez [Synchroniser les écritures entrepôt ajustées](/dynamics365/business-central/inventory-how-count-adjust-reclassify#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).

Pour les importations en bloc, utilisez des packages de configuration pour importer des données dans les journaux.

> [!NOTE]
> Vous ne pouvez pas utiliser **Modifier dans Excel** pour créer des lignes journal avec des informations de suivi.

## <a name="see-related-microsoft-trainingtrainingmodulesprepare-item-tracking" />Voir la [formation Microsoft](/training/modules/prepare-item-tracking/) associée

## <a name="see-also" />Voir aussi .

[Utiliser les numéros de lot et de série](inventory-how-work-item-tracking.md)  
[Tracer des articles - Articles suivis](inventory-how-to-trace-item-tracked-items.md)  
[Inventaire](inventory-manage-inventory.md)  
[Détails de conception : traçabilité](design-details-item-tracking.md)  
[Détails de conception : traçabilité et réservations](design-details-item-tracking-and-reservations.md)  
[Réserver des articles](inventory-how-to-reserve-items.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
