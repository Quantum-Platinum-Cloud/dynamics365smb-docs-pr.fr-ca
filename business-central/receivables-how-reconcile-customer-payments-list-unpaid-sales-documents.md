---
title: Affecter des paiements à des documents vente échus
description: 'Vous affectez les montants payés par les clients aux documents vente associés et reportez le paiement pour mettre à jour les écritures client, grand livre et banque.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment process, cash receipts, customer payment'
ms.search.form: '1290, 1294, 1287'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="reconcile-customer-payments-from-a-list-of-unpaid-sales-documents" />Rapprocher les paiements client à partir de la liste des documents vente échus

Une fois que les clients ont effectué des paiements électroniques sur votre compte bancaire, vous devez effectuer les actions suivantes :

* Affecter chaque montant payé au document vente validé lié
* Reportez le paiement pour mettre à jour les écritures de paiement dans les comptes général, bancaire, et client. 

Selon les besoins de votre entreprise, vous pouvez être payé et enregistrer ce paiement de diverses manières : manuellement, automatiquement, et via des services de paiement.  

> [!NOTE]  
> Vous pouvez effectuer les mêmes tâches, y compris les paiements fournisseur sur la page **Journal rapprochement paiement** à l'aide des fonctions dédiées à l'importation de relevés bancaires, à l'affectation automatique et au rapprochement de comptes bancaires. Pour plus d'informations, reportez-vous à [Rapprocher les paiements à l'aide du lettrage automatique](receivables-how-reconcile-payments-auto-application.md).

Utilisez la page **Enregistrer les paiements client** pour réaliser les tâches de contrepartie des comptes internes en utilisant les chiffres de trésorerie réels pour s’assurer que les paiements sont collectés. Vous pouvez rapidement vérifier et reporter les paiements individuels ou forfaitaires, traiter des paiements avec escomptes et trouver les documents impayés.

Les paiements pour des clients différents qui ont des dates d'échéance différentes doivent être reportés en tant que paiements individuels. Les paiements pour le même client qui ont la même date d'échéance peuvent être reportés comme paiement forfaitaire. Les paiements forfaitaires sont utiles, par exemple, lorsqu’un client a effectué un paiement unique qui couvre plusieurs factures vente.

## <a name="to-set-up-the-payment-registration-journal" />Pour configurer le journal enregistrement paiement
Étant donné que vous pouvez reporter différents types de paiement dans différents comptes de contrepartie, vous devez sélectionner un compte de contrepartie sur la page **Configuration de l'enregistrement de paiement** avant de commencer le traitement des paiements client. Si vous reportez toujours sur le même compte de contrepartie, vous pouvez définir ce compte par défaut et éviter cette étape chaque fois que vous ouvrez la page **Enregistrer les paiements client**.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Configuration de l’enregistrement de paiement**, puis choisissez le lien associé. Vous pouvez également choisir l’action **Configurer** sur la page **Enregistrer les paiements client**.
2. Renseignez les champs de la page **Configuration de l'enregistrement de paiement**. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)] Choisissez un champ pour lire une brève description du champ ou du lien des informations connexes.  

> [!TIP]
> Pour faciliter l’identification ultérieure des écritures qui ont été reportées via le journal, vous pouvez affecter une série de numéros spécifique au journal. Ceci est utile si vous utilisez des journaux de rapprochement des paiements pour enregistrer et affecter les paiements.

## <a name="to-register-customer-payments-individually" />Pour enregistrer les paiements client individuellement

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Enregistrer les paiements client**, puis choisissez le lien associé.  

    La page **Enregistrer les paiements client** affiche tous les documents reportés pour lesquels un paiement peut être enregistré. La page peut également être ouverte à partir des pages **Clients** et **Fiche client** dans lesquelles elle sera automatiquement filtrée pour le client spécifié.  
2. Cochez la case **Paiement effectué** de la ligne représentant le document validé pour lequel un paiement a été effectué.

    Si la case **Renseigner automatiquement la date de réception** est cochée sur la page **Configuration de l'enregistrement de paiement**, la date de travail est entrée dans le champ **Date de réception**.  
3. Dans le champ **Date de réception**, entrez la date de réception du paiement. Cette date peut être différent de la date de travail.  
4. Dans le champ **Montant reçu**, saisissez le montant payé.

    Pour les paiements intégraux, le montant est le même que celui du champ **Montant ouvert** de la ligne. Pour les paiements partiels, le montant est inférieur à celui du champ **Montant ouvert** de la ligne.
5. Répétez les phases 2 à 4 pour les autres lignes représentant des documents reportés pour lesquels des paiements sont effectués.  
6. Sélectionnez l'action **Valider les paiements**.  

Les informations de paiement saisies sont validées pour les documents représentés par les lignes dont la case **Paiement effectué** est cochée.  

Les écritures paiement sont reportées sur les comptes grand livre, bancaire et client. Chaque paiement est affecté au document vente reporté lié.  

## <a name="to-reconcile-lump-sum-payments" />Pour rapprocher des paiements forfaitaires
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Enregistrement de paiement**, puis choisissez le lien associé.
2. Cochez la case **Paiement effectué** pour les lignes représentant les documents reportés pour le même client pour lequel un paiement forfaitaire a été effectué.  

    > [!NOTE]  
    >   Le client dans le champ **Nom** doit être identique sur toutes les lignes reportées comme paiement forfaitaire.  

    Si la case **Renseigner automatiquement la date de réception** est cochée sur la page **Configuration de l'enregistrement de paiement**, la date de travail est renseignée dans le champ **Date de réception**.  
3. Dans le champ **Date de réception**, entrez la date de réception du paiement. Cette date peut être différent de la date de travail.  

    > [!NOTE]  
    >   Cette date doit être identique sur toutes les lignes qui seront reportées comme paiement forfaitaire.  
4. Dans le champ **Montant reçu**, entrez les montants sur plusieurs lignes pour obtenir le paiement forfaitaire.  

    > [!TIP]  
    > Essayez de reporter le plus de paiements intégraux possible avec le montant forfaitaire. Entrez des montants identiques au montant du champ **Montant ouvert** sur autant de lignes que possible.  
5. Répétez les étapes 2 à 4 pour les autres lignes représentant les documents reportés pour le même client pour lequel un paiement forfaitaire a été effectué.  
6. Sélectionnez l'action **Reporter comme paiement forfaitaire**. Les informations de paiement saisies sont validées pour les documents représentés par les lignes dont la case **Paiement effectué** est cochée.  

Les écritures paiement sont reportées sur les comptes grand livre, bancaire et client. Chaque paiement est affecté au document vente reporté lié.  

Si un paiement avec la banque n’est pas représenté par une ligne sur la page **Enregistrement de paiement**, cela peut être parce que le document connexe n’a pas encore été reporté. Dans ce cas, vous pouvez utiliser la fonction de recherche pour trouver rapidement le document et le reporter pour traiter le paiement. Pour plus d’informations, voir [Pour rechercher un document vente spécifique qui n’est pas totalement facturé](#to-find-a-specific-sales-document-that-isnt-fully-invoiced).  

Si un paiement avec la banque n’est représenté par aucun document dans [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez ouvrir une ligne journal général préremplie depuis la page **Enregistrement de paiement** pour reporter le paiement directement dans le compte de contrepartie sans lettrer le paiement avec un document. Sinon, vous pouvez enregistrer le paiement dans le journal jusqu'à ce que l'origine du paiement soit résolue. Pour plus d'informations, voir [Pour enregistrer ou reporter un paiement sans document connexe](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-record-or-post-a-payment-without-a-related-document).  

## <a name="to-process-customer-payments-with-discounts-manually" />Pour traiter manuellement les paiements client avec remises
Si vous avez convenu d’un escompte de paiement avec le client, les montants règlement peuvent être inférieurs aux montants facture si le paiement est effectué avant la date d’escompte de paiement convenue.  

Les procédures suivantes expliquent quatre méthodes différentes permettant de reporter des paiements avec escomptes sur la page **Enregistrement de paiement**.  

* Le montant règlement est égal au montant escompté ouvert, et la date d'échéance est antérieure à la date d'escompte. Vous reportez le paiement tel quel.  
* Le montant règlement est égal au montant escompté ouvert, mais la date d'échéance est postérieure à la date d'escompte. Vous reportez le paiement comme partiel. Le document reste ouvert pour collecter/payer le montant ouvert. Vous pouvez également définir la date d’escompte ultérieurement pour permettre la réalisation de la totalité du paiement.  
* Le montant règlement est inférieur au montant avec escompte restant. Vous reportez le paiement comme partiel. Le document reste ouvert pour collecter/payer le montant ouvert.  
* Le montant règlement est supérieur au montant avec escompte restant. Vous reportez les paiements tels quels. Seul le montant ouvert est reporté. Le montant supplémentaire est crédité au client.  

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-and-where-the-payment-date-is-before-the-discount-date" />Pour traiter un montant règlement égal au montant escompté, et lorsque la date d'échéance est antérieure à la date d'escompte
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Enregistrement de paiement**, puis choisissez le lien associé.  
2. Saisissez le montant du paiement dans le champ **Montant reçu**. Le montant est égal au montant du champ **Montant restant après remise**.

    La case **Paiement effectué** est automatiquement cochée, et le champ **Date de réception** contient la date de travail.    
3. Saisissez la date du paiement dans le champ **Date de réception**. La date est antérieure à la date du champ **Date d'escompte**.
4. Vérifiez que le champ **Montant ouvert** indique zéro (0).  
5. Sélectionnez l'action **Valider les paiements** pour valider l'intégralité du paiement sur les comptes général, bancaire et client.

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-but-where-the-payment-date-is-after-the-discount-date" />Pour traiter un montant règlement égal au montant escompté, mais lorsque la date d'échéance est postérieure à la date d'escompte
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Enregistrement de paiement**, puis choisissez le lien associé.  
2. Saisissez le montant du paiement dans le champ **Montant reçu**. Le montant est égal au montant du champ **Montant restant après remise**.

    La case **Paiement effectué** est automatiquement cochée, et le champ **Date de réception** contient la date de travail.
3. Dans le champ **Date de réception**, saisissez une date d'échéance ultérieure à celle indiquée dans le champ **Date d'escompte**. La police des champs de date devient rouge et un message d'erreur s'affiche au bas de la page.

    > [!TIP]  
    >   Si vous voulez créer une exception et accorder l'escompte bien que le paiement soit échu, procédez comme suit :
4. Sélectionnez l'action **Détails**.  
5. Sur la page **Détails de l'enregistrement de paiement**, dans le champ **Date d'escompte de paiement** sur le raccourci **Escompte de paiement**, saisissez une date ultérieure à celle indiquée dans le champ **Date de réception** de la page **Enregistrement de paiement**.  

    Le message d’erreur et la police rouge disparaissent, vous pouvez traiter le paiement escompté.    
6. Vérifiez que le champ **Montant ouvert** indique le montant qui reste à régler pour le montant total de la facture.  
7. Sélectionnez l'action **Valider les paiements** pour valider le paiement partiel sur les comptes général, bancaire et client.  

Le document connexe reste ouvert.

### <a name="to-process-a-payment-that-is-lower-than-the-remaining-discounted-amount" />Pour traiter un paiement inférieur au montant avec escompte restant
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Enregistrement de paiement**, puis choisissez le lien associé.  
2. Saisissez le montant du paiement dans le champ **Montant reçu**. Le montant est inférieur au montant du champ **Montant restant après remise**.

    La case **Paiement effectué** est automatiquement cochée, et le champ **Date de réception** contient la date de travail.  
3. Saisissez la date du paiement dans le champ **Date de réception**. La date est antérieure à la date du champ **Date d'escompte**.
4. Vérifiez que le champ **Montant ouvert** indique le montant qui reste à régler pour le montant escompté.  
5. Sélectionnez l'action **Valider les paiements** pour valider le paiement partiel sur les comptes général, bancaire et client.  

Le document connexe reste ouvert.

### <a name="to-process-a-payment-that-is-more-than-the-remaining-discounted-amount" />Pour traiter un paiement supérieur au montant avec escompte restant
1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Enregistrement de paiement**, puis choisissez le lien associé.  
2. Saisissez le montant du paiement dans le champ **Montant reçu**. Le montant est supérieur au montant du champ **Montant restant après remise**.  

    La case **Paiement effectué** est automatiquement cochée, et le champ **Date de réception** contient la date de travail.    
3. Saisissez la date du paiement dans le champ **Date de réception**. La date est antérieure à la date du champ **Date d'escompte**.
4. Vérifiez que le champ **Montant ouvert** indique zéro (0).  
5. Sélectionnez l'action **Valider les paiements** pour valider l'intégralité du paiement sur les comptes général, bancaire et client.  

Le document associé est fermé, et le client est crédité du montant du paiement excédentaire.  

## <a name="to-find-a-specific-sales-document-that-isnt-fully-invoiced" />Pour rechercher un document vente spécifique qui n’est pas totalement facturé
La page **Enregistrement de paiement** vous aide dans les tâches de contrepartie des comptes internes avec les chiffres réels de règlement pour assurer une collecte efficace auprès des clients et le paiement des sommes dues aux fournisseurs. Elle affiche les paiements entrants en attente sous la forme de lignes représentant les documents vente pour lesquels un montant doit être payé.  

Généralement, lorsqu'un paiement a été effectué, enregistré à la banque ou autre, le document vente ou achat associé est représenté par une ligne sur la page **Enregistrement de paiement** parce que le document en question attend que le paiement soit reporté par rapport au montant ouvert. Cependant, parfois un paiement qui a été effectué n’est pas représenté par une ligne sur la page **Enregistrement de paiement**, généralement parce que la facture du document en question n’a pas encore été totalement reportée.

Sur la page **Recherche de documents**, vous pouvez rechercher parmi les documents qui n’ont pas été entièrement facturés. Vous pouvez effectuer une recherche avec un ou plusieurs des critères suivants :  

* Numéro de document  
* Montant ou plage de montants  

La procédure suivante explique comment trouver un document spécifique à l'aide de deux critères de recherche.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Enregistrement de paiement**, puis choisissez le lien associé.
2. Avec le pointeur sur n'importe quelle ligne, sélectionnez l'action **Rechercher des documents**.
3. Sur la page **Recherche de document**, entrez une valeur de recherche dans le champ **N° document**.  

    > [!NOTE]  
    >   La valeur que vous entrez dans ce champ est indiquée entre caractères génériques masqués. Cela signifie que la fonction recherche tous les numéros de document qui contiennent la valeur saisie.    
4. Dans le champ **Montant**, saisissez le montant spécifique qui figure sur le document que vous recherchez.  
5. Dans le champ **% écart de quantité**, saisissez la valeur du pourcentage pour définir la plage des montants dans laquelle rechercher le document ouvert.  

    Si vous saisissez 10, la fonction recherche les montants d’une plage comprise entre dix pour cent en moins et dix pour cent de plus que la valeur indiquée dans le champ **Montant**.    
6. Sélectionnez l'action **Rechercher**.  

La fonction de recherche effectue une recherche parmi les documents qui n’ont pas été entièrement facturés selon les critères spécifiés.  

Si un ou plusieurs documents correspondent aux critères de recherche, la page **Résultat de la recherche de documents** s'ouvre et affiche les lignes représentant ces documents. Chaque ligne contient un numéro de document, une description et un montant. Ces informations facilitent la recherche d’un document spécifique.

Si un paiement avec la banque n’est représenté par aucun document dans [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez ouvrir une ligne journal général préremplie depuis la page **Enregistrement de paiement** pour reporter le paiement directement dans le compte de contrepartie sans affecter le paiement à un document. Sinon, vous pouvez enregistrer le paiement dans le journal jusqu'à ce que l'origine du paiement soit résolue.  

## <a name="to-record-or-post-a-payment-without-a-related-document" />Pour enregistrer ou reporter un paiement sans document connexe
Si un paiement avec la banque n’est représenté par aucun document dans [!INCLUDE[prod_short](includes/prod_short.md)], vous pouvez ouvrir une ligne journal général préremplie depuis la page **Enregistrement de paiement** pour reporter le paiement directement dans le compte de contrepartie sans affecter le paiement à un document. Sinon, vous pouvez enregistrer le paiement dans le journal jusqu'à ce que l'origine du paiement soit clarifiée.  

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Enregistrement de paiement**, puis choisissez le lien associé.
2. Sélectionnez l'action **Feuille comptabilité**.  

    La page **Journal général** s'ouvre avec une ligne qui contient le compte de contrepartie du lot journal configuré sur la page **Configuration de l’enregistrement de paiement**.  
3. Renseignez les autres champs sur la ligne du journal général. Par exemple, fournissez le montant, le numéro de client ou les informations du relevé bancaire. Pour plus d'informations, voir [Reporter les transactions directement dans le grand livre](finance-how-post-transactions-directly.md).  

Vous pouvez reporter la ligne journal pour mettre à jour le total sur le compte de contrepartie. Sinon, vous pouvez laisser la ligne journal non reportée et ajouter par exemple une note indiquant que le paiement a besoin d’une analyse complémentaire.  

Si vous laissez la ligne journal non reportée, elle s'ajoutera à la valeur du champ **Solde non reporté** au bas de la page **Enregistrement de paiement**.  

## <a name="see-also" />Voir aussi
[Gestion des comptes client](receivables-manage-receivables.md)  
[Vente](sales-manage-sales.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
