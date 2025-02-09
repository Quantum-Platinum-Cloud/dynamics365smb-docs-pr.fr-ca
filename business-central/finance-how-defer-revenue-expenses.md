---
title: Echelonner les recettes et les dépenses
description: 'Pour identifier des recettes ou des dépenses dans des période autres que la période de report de la transaction, vous pouvez utiliser la fonctionnalité pour les échelonner ou les reporter automatiquement selon un calendrier précis.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.search.form: '1700, 1701, 1702, 1703, 1704, 1705, 1706, 1707'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="defer-revenues-and-expenses" />Echelonner les recettes et les dépenses

Pour identifier une recette ou une dépense dans une période autre que la période de report de la transaction, vous pouvez utiliser la fonctionnalité pour échelonner automatiquement les recettes et les dépenses selon un calendrier précis.

Pour répartir les recettes et les dépenses sur les périodes comptables concernées, configurez un modèle d'échelonnement pour la ressource, l'article ou le compte du grand livre pour lequel/laquelle les recettes ou les dépenses seront reportées. Lorsque vous reportez le document vente ou achat concerné, les recettes ou les dépenses sont échelonnées sur les périodes comptables concernées, selon un tableau d'échelonnement régi par des paramètres dans le modèle d'échelonnement et la date de report.

## <a name="to-set-up-a-gl-account-for-deferral" />Pour configurer un compte du grand livre pour échelonnement

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Plan comptable**, puis choisissez le lien associé.
2. Sélectionnez l'action **Nouveau**.
3. Renseignez les champs comme nécessaire afin de créer un compte du grand livre pour les recettes échelonnées Pour plus d'informations, reportez-vous à [Les écritures comptables et le plan comptable](finance-general-ledger.md).
4. Répétez les étapes 2 et 3 pour créer un nouveau compte du grand livre pour les dépenses échelonnées.

Pour les deux types d'échelonnement, sélectionnez **Bilan** dans le champ **Type** et nommez les comptes en conséquence, comme « Revenus comptabilisés d'avance » pour les recettes différées et « Dépenses impayées » pour les dépenses différées.

## <a name="to-set-up-a-deferral-template" />Pour configurer un modèle d'échelonnement

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Modèles échelonnement**, puis sélectionnez le lien associé.
2. Sélectionnez l'action **Nouveau**.
3. Renseignez les champs selon vos besoins.
4. Dans le champ **Méthode de calcul**, précisez comment le champ **Montant** est calculé pour chaque période sur la page **Tableau d'échelonnement**. Les options suivantes vous sont proposées :

   * **Linéaire** : les montants d'échelonnement périodique sont calculés selon le nombre de périodes, réparties en fonction de la durée de la période.
   * **Égal par période** : les montants d'échelonnement périodique sont calculés selon le nombre de périodes, réparties de façon uniforme sur les périodes.
   * **Jours par période** : les montants d'échelonnement périodique sont calculés selon le nombre de jours dans la période.
   * **Défini par l'utilisateur** : les sommes d'échelonnement périodique ne sont pas calculées. Vous devez renseigner manuellement le champ **Montant** pour chaque période sur la page Tableau d'échelonnement. Pour en savoir plus, voir la section « Pour modifier un tableau d'échelonnement à partir d'une facture vente ».
5. Dans le champ **Description période**, spécifiez une description affichée sur les écritures pour le report de l'échelonnement. Vous pouvez saisir les codes d'espace réservé suivants pour les valeurs générales, qui seront insérés automatiquement lorsque la description de la période s'affiche.

   * %1 = le numéro du jour de la date de report de la période
   * %2 = le numéro de la semaine de la date de report de la période
   * %3 = le numéro du mois de la date de report de la période
   * %4 = le nom du mois de la date de report de la période
   * %5 = le nom de la période comptable de la date de report de la période
   * %6 = l'exercice financier de la date de report de la période

Exemple : la date de report est le 06/02/2016. Si vous saisissez « Dépenses échelonnées pour %4 %6 », la description affichée sera « Dépenses échelonnées pour février 2016 ».

## <a name="to-assign-a-deferral-template-to-an-item" />Pour affecter un modèle d'échelonnement à un article

> [!NOTE]  
> Les étapes de cette procédure sont les mêmes que lorsque vous affectez un modèle d'échelonnement à un compte du grand livre ou une ressource.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Article**, puis choisissez le lien associé.
2. Ouvrez la fiche de l'article pour lequel les recettes ou les dépenses doivent être échelonnées selon les périodes comptables lorsque l'article a été vendu ou acheté.
3. Dans le champ **Modèle échelonnement par défaut**, sélectionnez le modèle d'échelonnement pertinent.

## <a name="to-change-a-deferral-schedule-from-a-sales-invoice" />Pour modifier un calendrier d'échelonnement à partir d'une facture vente

> [!NOTE]  
> Les étapes de cette procédure sont identiques lorsque vous modifiez un calendrier d'échelonnement, pour les dépenses, à partir d'une facture achat.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Factures vente**, puis sélectionnez le lien associé.
2. Créez une facture vente pour un article ayant un modèle d'échelonnement attribué. Pour plus d'informations, reportez-vous à [Facturer des ventes](sales-how-invoice-sales.md).

    Notez que dès que vous saisissez l'article (ou la ressource ou le compte général) sur la ligne de facture, le champ **Code d'échelonnement** est complété avec le code du modèle d'échelonnement attribué.
3. Sélectionnez l'action **Tableau d'échelonnement**.
4. Sur la page **Tableau d'échelonnement**, modifiez les paramètres sur l'en-tête ou les valeurs des lignes, par exemple afin d'échelonner le montant sur une autre période comptable.
5. Sélectionnez l'action **Calculer tableau**.
6. Cliquez sur le bouton **OK**. Le tableau d'échelonnement est mis à jour pour la facture vente. Le modèle d'échelonnement associé reste inchangé.

## <a name="to-preview-how-deferred-revenues-or-expenses-will-be-posted-to-the-general-ledger" />Pour obtenir un aperçu de la façon dont les recettes et les dépenses seront reportées dans le grand livre

> [!NOTE]  
> Les étapes de cette procédure sont identiques lorsque vous prévisualisez la manière dont les échelonnements des dépenses sont reportés.

1. Sur la page **Facture vente** sélectionnez l'action **Aperçu report**.
2. Sur la page **Aperçu report**, sélectionnez l'action **Écriture**, puis sélectionnez l'action **Afficher écritures associées**.

Les écritures à reporter vers le compte d'échelonnement spécifié, par exemple, les Revenus comptabilisés d'avance, sont désignées par la description que vous avez saisie dans le champ **Description de la période** du modèle d'échelonnement, par exemple « Dépenses échelonnées pour février 2016 ».

## <a name="to-review-posted-deferrals-in-the-sales-deferral-summary-report" />Pour examiner les échelonnements reportés dans le rapport Résumé échelonnement ventes

> [!NOTE]  
> Les étapes de cette procédure sont identiques lorsque vous passez en revue le rapport Résumé échelonnement achats.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Résumé échelonnement vente**, puis sélectionnez le lien associé.
2. Sur la page **Résumé échelonnement ventes**, dans le champ **Balance au**, saisissez la date à laquelle vous souhaitez voir les recettes échelonnées.
3. Cliquez sur le bouton **Aperçu**.

## <a name="to-specify-a-period-in-which-to-allow-deferral-posting" />Pour spécifier une période au cours de laquelle autoriser le report de l’échelonnement

Vous pouvez spécifier une période au cours de laquelle les personnes peuvent enregistrer des transactions en saisissant des dates dans les champs **Début période report** et **Fin période report**, comme suit :

* Pour tous les utilisateurs, sur la page **Configuration du grand livre** :
* Pour des utilisateurs spécifiques, sur la page **Configuration utilisateur**

Si vous l’avez fait, vous devez faire une exception pour les échelonnements afin de leur permettre d’être reportés en dehors de la période. Pour définir la période, procédez comme suit :

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Configuration du grand livre** ou **Configuration de l'utilisateur**, puis choisissez le lien associé.
2. Dans les champs **Autoriser le report de l'échelonnement à partir de** et **Autoriser le report de l'échelonnement jusqu’à**, entrez une date de début et de fin pour la période.

## <a name="see-related-microsoft-trainingtrainingmodulesprocessing-invoices-dynamics-365-business-central" />Voir la [formation Microsoft](/training/modules/processing-invoices-dynamics-365-business-central/) associée

## <a name="see-also" />Voir aussi .

[Finance](finance.md)  
[Configuration de Finance](finance-setup-finance.md)  
[Utiliser des journaux généraux](ui-work-general-journals.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
