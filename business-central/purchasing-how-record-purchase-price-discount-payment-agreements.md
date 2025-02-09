---
title: Enregistrer les prix d'achat spéciaux et les escomptes
description: Vous pouvez définir différentes ententes en termes de prix et d'escomptes et les affecter aux documents achat pour les fournisseurs.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.search.form: 26, 1346, 7012, 7014, 7017, 7018, 7189, 7190, 9307
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 2b3914f292ca94770694960d4f202f18408b1191
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: fr-CA
ms.lasthandoff: 09/19/2022
ms.locfileid: "9534572"
---
# <a name="record-special-purchase-prices-and-discounts" /><a name="record-special-purchase-prices-and-discounts"></a>Enregistrer les prix d'achat spéciaux et les escomptes

> [!NOTE]
> Dans la deuxième vague de lancement de 2020, nous avons libéré des processus rationalisés pour la configuration et la gestion des prix et des escomptes. Si vous êtes un nouveau client utilisant cette version, vous utilisez la nouvelle expérience. Si vous êtes un client existant, l’utilisation ou non de la nouvelle expérience dépend du fait que votre administrateur a activé ou non la fonctionnalité **Nouvelle tarification des ventes** dans **Gestion des fonctionnalités**. Pour plus d’informations, consultez [Activer les fonctionnalités à venir à l’avance](/dynamics365/business-central/dev-itpro/administration/feature-management).

Vous devez définir les différentes ententes de prix et d'escompte qui s'appliquent lors d'achats effectués auprès de plusieurs fournisseurs de sorte que les valeurs et règles convenues s'appliquent aux documents achat créés à l'intention des fournisseurs.

Lorsque vous avez enregistré des prix spéciaux et des escomptes de ligne pour les ventes et les achats, [!INCLUDE[prod_short](includes/prod_short.md)] s'assure que votre profit pour l'article est toujours optimal en calculant automatiquement le meilleur prix dans les documents achat et vente, sur les lignes journal article et projet. Pour plus d'informations, voir [Calcul du meilleur prix](purchasing-how-record-purchase-price-discount-payment-agreements.md#best-price-calculation).

En ce qui concerne les prix, un prix d'achat spécial peut être inséré sur les lignes achat s'il existe une certaine combinaison de fournisseur, d'article, de quantité minimum, d'unité de mesure ou de date de début/date de fin.

En ce qui concerne les remises, vous pouvez définir et utiliser deux types de remises achat :

| Type d'escompte | Description |
| --- | --- |
| **Remise ligne achat** |Un escompte sous forme de montant inséré sur les lignes achat s'il existe une certaine combinaison de fournisseur, d'article, de quantité minimum, d'unité de mesure ou de date de début/date de fin. Ce type fonctionne de la même manière que pour les prix d'achat. |
| **Remise facture** |Un escompte sous forme de pourcentage qui est soustrait du total du document si la valeur de toutes les lignes d'un document achat dépasse un montant minimal donné. |

Dans la mesure où les remises ligne achat et les prix achat sont basés sur une combinaison article/fournisseur, vous pouvez également effectuer cette configuration à partir de la fiche article dans laquelle sont définies les règles et valeurs. Pour plus d'informations, reportez vous à [Enregistrer de nouveaux articles](inventory-how-register-new-items.md).

## <a name="to-set-up-a-special-purchase-price-for-a-vendor" /><a name="to-set-up-a-special-purchase-price-for-a-vendor"></a>Pour configurer un prix d'achat spécial pour un fournisseur

#### <a name="current-experience"></a>[Expérience actuelle](#tab/current-experience)

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Fournisseurs**, puis choisissez le lien associé.
2. Ouvrez la fiche fournisseur appropriée, puis sélectionnez l'action **Prix**.
3. Renseignez les champs de la ligne selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Remplissez une ligne pour chaque combinaison pour laquelle le fournisseur vous accorde un escompte ligne achat.

#### <a name="new-experience"></a>[Nouvelle expérience](#tab/new-experience)

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Fournisseurs**, puis choisissez le lien associé.
2. Choisissez le fournisseur, puis sélectionnez l’action **Listes prix vente**.
3. Sélectionnez **Nouveau** pour créer une liste prix achat.
4. Sur les raccourcis **Général** et **Taxes**, complétez les champs, comme nécessaire. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Pour ajouter des éléments à la liste, effectuez l’une des opérations suivantes :
   * Pour ajouter de nombreux éléments, choisissez **Proposer lignes**, puis entrez des critères de filtre pour spécifier les types d’éléments à ajouter. Si vous le souhaitez, vous pouvez également saisir des paramètres supplémentaires pour les articles spécifiques à la liste de prix. Si nécessaire, vous pouvez les modifier ultérieurement.
   * Pour copier des articles d’une autre liste de prix, choisissez **Copier lignes**, puis choisissez la liste de prix à copier.
   * Pour ajouter des éléments manuellement, dans la grille, dans le champ **Type de produit**, choisissez le type de produit auquel la liste de prix est destinée. En fonction de votre sélection, renseignez les champs restants selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Pour commencer à utiliser la liste de prix, dans le champ **État**, choisissez **Actif**.

---

## <a name="to-set-up-a-line-discount-for-a-vendor" /><a name="to-set-up-a-line-discount-for-a-vendor"></a>Pour configurer un escompte ligne pour un fournisseur

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Fournisseurs**, puis choisissez le lien associé.
2. Ouvrez la fiche fournisseur appropriée, puis sélectionnez l'action **Remises ligne**.

   Le champ **N° fournisseur** est prérempli avec le numéro du fournisseur.
3. Renseignez les champs de la ligne selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Remplissez une ligne pour chaque combinaison pour laquelle le fournisseur vous accorde un escompte ligne achat.

## <a name="to-set-up-an-invoice-discount-for-a-vendor" /><a name="to-set-up-an-invoice-discount-for-a-vendor"></a>Pour configurer un escompte facture pour un fournisseur

Une fois que vos fournisseurs vous ont informé des escomptes facture qu'ils accordent, entrez le code escompte facture sur les fiches fournisseur et configurez les conditions pour chaque code.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Fournisseurs**, puis choisissez le lien associé.
2. Ouvrez la fiche fournisseur d'un fournisseur pouvant faire l'objet de remises facture.
3. Dans le champ **Code remise facture**, sélectionnez un code pour les conditions de remise facture appropriées à utiliser pour calculer les remises facture pour le fournisseur.

    > [!NOTE]  
    > Les codes escompte facture sont représentés par les fiches fournisseur existantes. Cela vous permet d'affecter rapidement les conditions d'escompte facture aux fournisseurs en sélectionnant le nom d'autres fournisseurs qui bénéficient des mêmes conditions.

    Configurez de nouvelles conditions d'escompte facture pour les achats.
4. Sur la page **Fiche fournisseur**, sélectionnez l'action **Escomptes facture**. La page **Escomptes facture fournisseur** s'ouvre.
5. Dans le champ **Code devise**, indiquez le code d'une devise à laquelle s'appliquent les conditions de remise facture. Laissez le champ vierge si vous souhaitez configurer des conditions d'escompte facture en USD.
6. Dans le champ **Montant minimum**, entrez le montant minimal qu'une facture doit présenter pour faire l'objet de la remise.
7. Dans le champ **% remise**, entrez la remise facture sous la forme d'un pourcentage du montant de la facture.
8. Répétez les étapes 5 à 7 pour chaque devise pour laquelle le fournisseur recevra un escompte facture différent.

L'escompte facture est désormais configuré et affecté au fournisseur concerné. Lorsque vous sélectionnez le code fournisseur dans le champ **Code escompte facture** dans d’autres fiches fournisseur, le même escompte facture est affecté à ces fournisseurs.

## <a name="to-choose-a-principle-for-posting-purchase-discounts" /><a name="to-choose-a-principle-for-posting-purchase-discounts"></a>Pour sélectionner un principe de report des escomptes achat

Lorsque vous reportez une facture achat qui comprend un ou plusieurs escomptes, vous pouvez choisir entre deux principes de report des montants d'escompte. Vous pouvez reporter des escomptes indépendamment ou les soustraire des escomptes facture.  

Avant cela, vous devez avoir configuré les comptes nécessaires pour reporter des montants d'escompte dans le plan comptable. Vous devez également vérifier que vous avez entré les numéros de compte corrects dans les paramètres comptabilisation des champs **Compte remise ligne achat** et **Compte remise fact. achat**.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Configuration achats et à payer**, puis choisissez le lien associé.
2. Dans le champ **Comptabilisation remise**, sélectionnez l'un des principes de validation des remises suivants.

|**Principe de validation des remises**|**Remise facture**|**Remise ligne**|  
|------------------------------------|--------------------------|-----------------------|  
|**Toutes remises**|Report séparé|Report séparé|  
|**Remises facture**|Report séparé|Soustraction|  
|**Remises ligne**|Soustraction|Report séparé|  
|**Remises déduites**|Soustraction|Soustraction|  

## <a name="purchase-invoice-discounts-and-service-charges" /><a name="purchase-invoice-discounts-and-service-charges"></a>Escomptes facture achat et frais forfaitaires

Si vous avez défini des conditions pour les remises facture avec des fournisseurs, vous pouvez les saisir dans le système. Le programme peut ensuite calculer l'escompte lorsque vous renseignez une facture achat.  

Avant d'utiliser les remises facture pour les achats, vous devez spécifier les fournisseurs qui vous offriront les remises.  

Vous pouvez associer les pourcentages escompte à des montants de facture spécifiques sur les pages **Escomptes facture fournisseur**. Vous pouvez entrer le nombre de pourcentages de votre choix sur chaque page. Chaque fournisseur peut disposer de sa propre page ou vous pouvez associer plusieurs fournisseurs à une même page.  

En plus du pourcentage d'escompte, vous pouvez lier un montant de frais forfaitaires au montant d'une facture.  

Vous pouvez définir des conditions pour les escomptes de paiement facture en devise locale pour les fournisseurs nationaux et en devise pour les fournisseurs étrangers.  

Vous avez la possibilité de choisir si [!INCLUDE[prod_short](includes/prod_short.md)] doit calculer automatiquement les montants de facture pour les devis, les commandes ouvertes, les commandes, les factures ou les avoirs.  

> [!TIP]  
> Avant de saisir ces informations dans le programme, il est conseillé de préparer la structure de l'escompte de paiement à utiliser. Ainsi, vous pouvez visualiser plus facilement les fournisseurs pouvant être liés à la même page d'escompte facture. Plus le nombre de page à configurer est faible, plus vous pouvez saisir rapidement les informations de base.

## <a name="best-price-calculation" /><a name="best-price-calculation"></a>Calcul du meilleur prix

Lorsque vous avez enregistré des prix spéciaux et des escomptes de ligne pour les ventes et les achats, [!INCLUDE[prod_short](includes/prod_short.md)] s'assure que votre profit pour l'article est toujours optimal en calculant automatiquement le meilleur prix dans les documents achat et vente, sur les lignes journal article et projet.

Le meilleur prix est le prix le plus bas autorisé associé à l'escompte ligne le plus élevé autorisé à une date donnée. [!INCLUDE[prod_short](includes/prod_short.md)] calcule automatiquement ce prix lorsqu’il insère le prix unitaire et le pourcentage d’escompte de ligne pour des articles dans le nouveau document et les lignes journal.

> [!NOTE]  
> Voici une description du calcul du meilleur prix pour la vente. Le calcul est le même pour les achats.

1. [!INCLUDE[prod_short](includes/prod_short.md)] vérifie la combinaison client facturé et article, et calcule le prix unitaire applicable et le pourcentage remise de ligne à l'aide des critères suivants :

    - Ce client a-t-il une entente pour des prix ou des escomptes ou appartient-il à un groupe bénéficiant d'un telle entente?
    - L'article ou le groupe escompte article sur la ligne est-il inclus dans l'une ou l'autre de ces ententes prix/escompte?
    - La date de commande (ou la date de report pour la facture et la note de crédit) est-elle comprise entre les dates début et de fin de l'entente prix/escompte?
    - Un code unité de mesure est-il spécifié? Si c'est le cas, [!INCLUDE[prod_short](includes/prod_short.md)] recherche des prix/remises possédant le même code unité, et des prix/remises sans code unité.

2. [!INCLUDE[prod_short](includes/prod_short.md)] vérifie si des accords prix/remise s'appliquent à des informations sur le document ou la ligne feuille, puis insère le prix unitaire applicable et le pourcentage remise de ligne, à l'aide des critères suivants :

    - Existe-t-il une quantité minimum à respecter dans l'entente de prix/escompte?
    - Existe-t-il une exigence en matière de devise à respecter dans l'entente de prix/escompte? Si c'est le cas, le prix le plus bas et l'escompte de ligne le plus élevé pour cette devise sont insérés, même si la devise locale permettrait d'offrir un meilleur prix. S'il n'existe aucun accord de prix/remise dans le code devise indiqué, [!INCLUDE[prod_short](includes/prod_short.md)] insère le prix le plus bas et la remise de ligne la plus élevée en DS.

Si aucun prix spécial ne peut être calculé pour l'article de la ligne, alors soit le coût unitaire direct, soit le prix unitaire à partir de la fiche article est inséré.

## <a name="see-related-microsoft-trainingtrainingmodulesset-up-prices-discounts-dynamics-365-business-centralindex" /><a name="see-related-microsoft-training"></a>Voir la [formation Microsoft](/training/modules/set-up-prices-discounts-dynamics-365-business-central/index) associée

## <a name="see-also" /><a name="see-also"></a>Voir aussi .

[Définition des achats](purchasing-setup-purchasing.md)  
[Procédure d'achat](purchasing-manage-purchasing.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
