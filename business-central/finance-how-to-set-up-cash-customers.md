---
title: Configurer des clients effectuant un achat au comptoir
description: Cette rubrique décrit les étapes nécessaires pour configurer la facture avec un numéro de client pour les clients qui paient en espèces.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '21, 22'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="set-up-cash-customers" />Configurer des clients effectuant un achat au comptoir

Vous ne pouvez pas créer une facture sans numéro de client. Ceci est valable même si vous effectuez une vente au comptoir et que vous n'avez rien à enregistrer dans un compte client.  

## <a name="to-set-up-a-cash-customer" />Pour configurer des clients effectuant un achat en espèces

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Client**, puis choisissez le lien associé.  
2. Créez une fiche **Client**. Pour plus d'informations, voir [Enregistrer de nouveaux clients](sales-how-register-new-customers.md).
3. Dans le champ **N°**, , saisissez par exemple **Espèces**.  
4. Dans le champ **Nom**, saisissez par exemple **Vente au comptoir**.  
5. Sur le raccourcie **Facturation**, renseignez les champs **Groupe compta. client** et **Groupe compta. marché**.  

 Vous avez alors configuré un client contenant suffisamment d'informations de facturation.  

> [!NOTE]  
> Vous avez peut-être choisi un groupe de report également utilisé pour les ventes à crédit nationales. Si vous souhaitez mettre à jour des données séparées sur les ventes au comptant, par exemple avec un compte client ou fournisseur spécial, vous pouvez configurer un groupe de report supplémentaire à cet effet.  
>
> Vous devez saisir le numéro d'un compte client pour le groupe de report, même si le solde de ce compte est toujours de 0 après le report d'une facture.  

## <a name="see-also" />Voir aussi

[Gestion des comptes client](receivables-manage-receivables.md)  
[Enregistrer de nouveaux clients](sales-how-register-new-customers.md)
[Finance](finance.md)  



[!INCLUDE[footer-include](includes/footer-banner.md)]
