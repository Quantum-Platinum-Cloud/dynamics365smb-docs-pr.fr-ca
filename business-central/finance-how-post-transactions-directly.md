---
title: Enregistrer les frais ou des revenus directement dans le grand livre
description: 'Pour les activités économiques qui ne sont pas représentées par un document, vous pouvez créer les transactions associées en reportant des lignes de journal sur la page Journal général.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'direct posting, general ledger'
ms.search.form: '39, 251'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="post-transactions-directly-to-the-general-ledger" />Reporter les transactions directement dans le grand livre

Les journaux généraux vous permettent de reporter des transactions financières directement dans les comptes GL et dans d'autres comptes tels que les comptes bancaires, client, fournisseur et employé.  

Une utilisation classique du journal général est de reporter les dépenses des employés avec leurs fonds propres au cours des activités professionnelles, pour un remboursement ultérieur. Pour plus d'informations, voir [Enregistrer et rembourser les frais des employés](finance-how-record-reimburse-employee-expenses.md).

Les journaux généraux reportent les transactions financières directement sur les comptes du grand livre et d'autres comptes tels que les comptes bancaires, clients, fournisseurs et employés. Le report avec un journal général crée toujours des écritures dans les comptes du grand livre. C'est le cas même lorsque, par exemple, vous reportez une ligne journal sur un compte client, parce qu'une écriture est reportée dans un compte client du grand livre via un groupe de report. Vous pouvez personnaliser votre version d'un journal général en configurant un lot ou un modèle journal. Pour plus d'informations, reportez-vous à [Utilisation des feuilles comptabilité](ui-work-general-journals.md).

Contrairement aux écritures qui sont reportées avec des documents qui nécessitent un processus de note de crédit, vous pouvez correctement inverser les écritures reportées avec le journal général. Pour plus d'informations, voir [Inverser des reports journal et annuler des réceptions/livraisons](finance-how-reverse-journal-posting.md).

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account" />Pour reporter une transaction directement dans le compte GL

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Journaux généraux**, puis choisissez le lien associé.
2. Ouvrez le lot journal général approprié. Pour plus d'informations, reportez-vous à [Utilisation des feuilles comptabilité](ui-work-general-journals.md).
3. Sur une nouvelle ligne journal, renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. Répétez l'étape 3 pour toutes les transactions distinctes que vous souhaitez reporter.

    > [!TIP]  
    > Si vous souhaitez saisir plusieurs lignes de transaction au-dessus d'une ligne compte contrepartie, par exemple, pour un compte bancaire, activez la case à cocher **Suggérer le montant contrepartie** de la ligne pour votre lot sur la page **Lots journal général**. Puis le champ **Montant** de la ligne compte contrepartie est automatiquement prérempli avec la valeur requise pour équilibrer les transactions.
5. Choisissez l'action **Valider** pour enregistrer les transactions sur les comptes généraux spécifiés.

## <a name="see-also" />Voir aussi

[Utiliser des journaux généraux](ui-work-general-journals.md)  
[Enregistrer et rembourser les frais des employés](finance-how-record-reimburse-employee-expenses.md)  
[Inverser des reports journal et annuler des réceptions/livraisons](finance-how-reverse-journal-posting.md)  
[Finance](finance.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
