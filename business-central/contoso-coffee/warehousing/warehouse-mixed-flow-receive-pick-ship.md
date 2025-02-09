---
title: 'Réception, rangement, prélèvement et expédition dans une configuration d’entrepôt mixte'
description: "Dans Business\_Central, les processus entrants et sortants peuvent être effectués de quatre manières, à l’aide de différentes fonctionnalités en fonction du niveau de complexité de l’entrepôt."
author: andreipanko
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: null
ms.date: 04/01/2021
ms.author: andreipa
---

# <a name="walkthrough-of-inbound-and-outbound-flow-in-mixed-warehouse-configurations" />Procédure pas à pas sur les flux entrants ou sortants dans les configurations entrepôt mixtes

Cette procédure pas à pas montre comment effectuer des flux entrants et sortants dans une configuration mixte, où pour le flux entrant, l’entrepôt est configuré sur De base : commande par commande et pour le flux sortant, la configuration avancée est utilisée. Pour plus d’informations, voir [Présentation des différentes options de configuration](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## <a name="prerequisites" />Conditions préalables
Pour exécuter cette procédure, vous devez faire de vous un employé d’entrepôt sur le site *JAUNE* en procédant comme suit :  
1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me 1.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Employés entrepôt**, puis sélectionnez le lien associé.  
2. Choisissez le champ **Code utilisateur** et sélectionnez votre propre compte utilisateur sur la page **Utilisateurs**.  
3. Dans le champ **Code d’emplacement**, saisissez *JAUNE*.  

## <a name="inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations" />Flux entrant : Réception et rangement dans les configurations de stockage de base

Dans [!INCLUDE[prod_short](../../includes/prod_short.md)], les processus entrants de réception et de rangement peuvent être effectués de quatre manières, à l'aide de différentes fonctionnalités en fonction du niveau de complexité de l'entrepôt.  

|Méthode|Processus entrant|Zones|Reçus|Rangements|Niveau de complexité (Voir [Détails de conception : configuration d'entrepôt](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Report de la réception et du rangement à partir de la ligne commande|X|||2|  
|B|Report de la réception et du rangement à partir d'un document de rangement inventaire|||X|3|  
|C|Report de la réception et du rangement à partir d'un document réception entrepôt||X||4/5/6|  
|J|Report de la réception d'un document réception entrepôt et report du rangement à partir d'un document de rangement entrepôt||X|X|4/5/6|  

Pour plus d'informations, reportez\-vous à [Détails de conception : flux d'enlogement](../../design-details-inbound-warehouse-flow.md).  

La procédure pas à pas suivante illustre la méthode C dans la table précédente.  

### <a name="scenario" />Scénario
Alicia, l’agent achat, crée des bons de commande pour divers grains torréfiés au fur et à mesure que la demande s’affiche. Lorsque la livraison associée arrive à l’entrepôt, Jean, le magasinier, range les articles dans des emplacements par défaut définis pour les articles. Lorsque Jean valide la réception, les articles sont reportés comme étant reçus dans l’inventaire et disponibles à la vente ou pour d’autres demandes.  

### <a name="steps" />Étapes
1. Configurez la page **Fiche emplacement** pour définir les flux d’entrepôt entrants de la compagnie.  

    1.  Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me 2.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , entrez **Emplacements**, puis sélectionnez le lien associé.  
    2.  Ouvrez la fiche emplacement *JAUNE*.  
    3.  Désactivez le bouton à bascule **Rangement requis**.  

2. Traitez les bons de commande à l’entrepôt.  

    1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me 3.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , entrez **Bons de commande**, puis sélectionnez le lien associé.  
    2. Sélectionnez les commandes du fournisseur 10000 pour l’emplacement JAUNE. Les numéros de commande fournisseur sont *Y-1* et *Y-2*. Utilisez les outils de personnalisation si le **N° de commande fournisseur** n’est pas visible. Pour plus d'informations, voir [Personnaliser votre espace de travail](../../ui-personalization-user.md).
    3. Choisissez l’action **Libérer** pour informer l’entrepôt que les bons de commande sélectionnés sont prêts pour l’activité entrepôt lorsque la livraison arrive.  

3. Créer le reçu d’entrepôt pour recevoir et ranger les articles livrés
    1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me 4.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Réceptions entrepôt**, puis choisissez le lien associé.
    2. Sélectionner l’action **Nouveau**
    3. Sur la page du reçu d’entrepôt, appuyez sur Entrée pour qu’un numéro de reçu d’entrepôt soit automatiquement sélectionné
    4. Saisissez le **Code d’emplacement** comme *JAUNE*.
    5. Choisissez l’action **Extraire documents origine**
    6. Sélectionnez les bons de commande émis précédemment par le fournisseur 10000 et cliquez sur le bouton **OK**.
        Les lignes contiendront une nouvelle entrée pour chaque ligne de bon de commande.

4. Ajuster la quantité à la réception en fonction de la quantité reçue et reporter le document
    1. Sélectionnez la ligne avec l’article *WRB-1000*.
    2. Sélectionnez *OVERRCPT10* dans le champ **Code de sur-réception** et modifiez la valeur de **Quantité à recevoir** de *100* vers *110*.
    3. Sélectionnez la ligne avec l’article *WRB-1001* et 
    4. Dans la seconde ligne, changez la valeur du champ **Quantité à recevoir** de *200* à *190*.
    5. Sélectionnez l’action **Reporter la réception**.

### <a name="results" />Résultats
 - les grains torréfiés sont maintenant enregistrés comme rangés
 - la **Réception entrepôt reportée** est créée
 - la **Réception achat reportée** est créée
 - le bon de commande a la **Quantité reçue** mise à jour pour les lignes reçues
 - l’**inventaire** d’articles est augmenté de la quantité choisie
    

## <a name="outbound-flow-picking-and-shipping-in-advanced-warehouse-configurations" />Flux sortant : prélèvement et expédition dans les configurations d’entrepôt avancées

Dans [!INCLUDE[prod_short](../../includes/prod_short.md)], les processus sortants de prélèvement et d'expédition peuvent être effectués de quatre manières, à l'aide de différentes fonctionnalités en fonction du niveau de complexité de l'entrepôt.  

|Méthode|Processus entrant|Zones|Prélèvements|Livraisons|Niveau de complexité (Voir [Détails de conception : configuration d'entrepôt](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Report du prélèvement et de la livraison à partir de la ligne commande|X|||2|  
|B|Report du prélèvement et de la livraison à partir d'un document prélèvement inventaire||X||3|  
|C|Report du prélèvement et de la livraison à partir d'un document livraison entrepôt|||X|4/5/6|  
|J|Report du prélèvement à partir d'un document prélèvement entrepôt et report de la livraison à partir d'un document livraison entrepôt||X|X|4/5/6|  

Pour plus d'informations, reportez\-vous à [Détails de conception : flux de désenlogement](../../design-details-outbound-warehouse-flow.md).  

La procédure pas à pas suivante illustre la méthode D dans la table précédente.

### <a name="scenario" />Scénario
Susan, préparatrice de commandes, crée des documents de vente pour divers grains torréfiés et les transmet à l’entrepôt. Comme toutes les commandes proviennent du même client, Ellen, responsable de l’entrepôt, décide de les livrer ensemble. Jean, le magasinier, doit s'assurer que la livraison est préparée et livrée au client.

### <a name="steps" />Étapes
C’est une suite de [Flux entrant : Réception et rangement dans les configurations de stockage de base](#inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations).

1. Traitez les documents de vente vers l’entrepôt.  

    1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me 5.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Documents de vente**, puis sélectionnez le lien associé.  
    2. Sélectionnez les commandes du client 10000 pour l’emplacement JAUNE. Les numéros de commandes externes sont *Y-3*, *Y-4* et *Y-5*. Utilisez les outils de personnalisation si le **N° de commande externe** n’est pas visible. Pour plus d'informations, voir [Personnaliser votre espace de travail](../../ui-personalization-user.md).
    3. Choisissez l’action **Libérer** pour informer l’entrepôt que les documents de vente sélectionnés sont prêts pour l’activité entrepôt.  

2. Livrer des articles  
    1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me 6.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Livraisons entrepôt**, puis sélectionnez le lien associé.  
    2. Sélectionnez l'action **Nouveau**.  
    3. Dans le champ **Code d’emplacement**, saisissez *JAUNE*.  
    4. Choisissez l'action **Filtrer pour extr. doc. orig.**.  
    5. Dans le champ **Code**, saisissez **CUST10000**.  
    6. Dans le champ **Description**, saisissez **Client 10000**.  
    7. Sélectionnez l'option **Modifier**.  
    8. Dans le raccourci **Vente**, dans le champ **Filtre n° client (débiteur)**, entrez *10000*.  
    9. Sélectionnez l'action **Exécuter**. 
    
    La livraison entrepôt est renseignée avec quatre lignes représentant les lignes commande client pour le client spécifié. Le champ **Quantité à livrer** est vide, car les articles doivent d’abord être prélevés.

3. Créer le prélèvement entrepôt à partir de la livraison entrepôt
    1. Sur la page livraison entrepôt, choisissez l’action **Créer un prélèvement**.
    2. Confirmez un des paramètres de prélèvement requis, par exemple sélectionnez *Article* dans le champ **Méthode de tri pour lignes activité** pour regrouper les mêmes articles. Choisissez le bouton **OK**.
    3. Vous recevrez un message de confirmation avec le numéro de prélèvement. 

4. Ouvrir le prélèvement entrepôt
    1. Utiliser l’icône en forme ![d’Ampoule qui ouvre la fenêtre de recherche 7.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Prélèvements entrepôt**, puis choisissez le lien associé.
    2. Localisez le prélèvement que vous avez créé et ouvrez-le.
    3. Mettez à jour la **Quantité à traiter** si nécessaire.
    4. Choisissez l'action **Enregistrer prélèvement**.
    5. Le prélèvement entrepôt se ferme et est supprimé si toutes les quantités sont traitées.

5. Reporter la livraison entrepôt
   1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me 8.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Livraisons entrepôt**, puis sélectionnez le lien associé.  
   2. Localisez la livraison que vous avez créée précédemment et ouvrez-la.
    Notez que **Quantité à livrer** est renseigné.
    3. Vous pouvez mettre à jour les champs **Date de report**, **Numéro de document externe**, **Code de l’agent d’expédition**, **Mode d’expédition** si nécessaire. Les valeurs non vides sont propagées aux documents source.
    4. Sélectionnez ensuite l’action **Reporter livraison**.
    5. Confirmez l’option **Livrer**.

### <a name="results" />Résultats
 - les grains torréfiés sont maintenant enregistrés comme prélevés 
 - le **Prélèvement entrepôt enreg.** est créé
 - la **Livraison entrepôt reportée** est créée
 - les trois **Livraison vente reportée** sont créées
 - le document de vente a la **Quantité livrée** mise à jour pour les lignes livrées
 - l’**inventaire** d’articles est réduit de la quantité choisie


## <a name="see-also" />Voir aussi
[Recevoir des articles](../../warehouse-how-receive-items.md)
[Configurer des entrepôts de base avec les zones d’opérations](../../warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)
[Détails de conception : flux d’entrepôt entrant](../../design-details-inbound-warehouse-flow.md)
[Livrer les articles](../../warehouse-how-ship-items.md)
[Prélever des articles pour la livraison entrepôt](../../warehouse-how-to-pick-items-for-warehouse-shipment.md)
[Détails de conception : flux d’entrepôt sortant](../../design-details-outbound-warehouse-flow.md)
[Afficher la disponibilité des articles](../../inventory-how-availability-overview.md)
