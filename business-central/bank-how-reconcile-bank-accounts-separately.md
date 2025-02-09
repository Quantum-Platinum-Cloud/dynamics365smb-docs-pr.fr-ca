---
title: Rapprochement des comptes bancaires
description: Découvrez comment rapprocher les transactions dans Business Central avec les transactions dans les relevés de votre banque.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/13/2022
ms.custom: bap-template
---
# Rapprochement des comptes bancaires

Le rapprochement bancaire permet de s’assurer que ce qui se trouve dans vos livres correspond aux relevés que vous recevez de votre banque. Le rapprochement des comptes bancaires compare et fait correspondre les écritures des comptes bancaires que vous avez configurées dans [!INCLUDE[prod_short](includes/prod_short.md)] avec les transactions bancaires au niveau de votre banque. Le rapprochement peut ensuite reporter les soldes sur vos comptes bancaires dans [!INCLUDE[prod_short](includes/prod_short.md)] pour les mettre à la disposition des responsables financiers. Le rapprochement bancaire est également un moyen pratique de découvrir et de résoudre les paiements manquants et les erreurs de comptabilité.

Cet article décrit comment rapprocher les comptes bancaires à partir de la page **Rapprochement bancaire**.

Cependant, vous pouvez également rapprocher des comptes bancaires sur la page **Journal rapprochement bancaire** lorsque vous traitez les paiements. Les écritures de compte bancaire ouvertes associées aux écritures client ou fournisseur affectées sont fermées lorsque vous sélectionnez l’action **Reporter les paiements et rapprocher les comptes bancaires**. Cela rapproche automatiquement le compte bancaire pour les paiements que vous reportez avec le journal. Pour plus d'informations, reportez-vous à [Lettrage automatique des paiements et rapprochement des comptes bancaires](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!NOTE]  
> Dans les versions nord-américaines, vous pouvez également effectuer cette tâche sur la page **Feuille rapprochement bancaire**, qui est mieux adaptée pour les chèques et les acomptes, mais ne vous permet pas d’importer des fichiers de relevé bancaire. Pour utiliser cette page à la place de la page **Rapprochement bancaire**, effacez le champ **Rapprochement bancaire avec correspondance auto.** sur la page **Configuration du grand livre**. Pour plus d'informations, voir [Rapprocher des comptes bancaires](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) sous Fonctionnalité locale, États-Unis.

Les lignes de la page **Rapprochement bancaire** sont réparties sur deux volets. Le volet **Lignes relevé bancaire** indique le volet des transactions bancaires importées ou les écritures comptables comportant des arriérés de paiement. Le volet **Écritures de compte bancaire** affiche les écritures dans le compte bancaire interne.

Le rapprochement des transactions dans les relevés de votre banque avec les écritures bancaires dans [!INCLUDE[prod_short](includes/prod_short.md)] est appelé *correspondance*. Il existe deux façons de faire correspondre les transactions avec les opérations bancaires :

* Automatiquement, à l’aide de l’action **Faire correspondre automatiquement**.
* Manuellement, en sélectionnant des lignes dans les deux volets pour lier chaque ligne relevé bancaire à une ou plusieurs écritures de compte bancaire correspondantes, puis en utilisant l’action **Faire correspondre manuellement**.

La case **Lettré** est cochée sur les lignes pour lesquelles les écritures correspondent. Pour plus d'informations, voir [Configurer des règles pour l'affectation automatique des paiements](receivables-how-set-up-payment-application-rules.md). Si vous saisissez une date de fin de relevé sur le rapprochement bancaire après avoir rapproché ses lignes avec des écritures, [!INCLUDE [prod_short](includes/prod_short.md)] annulera les correspondances pour les lignes et les écritures postérieures à cette date.

> [!NOTE]
> Une fois que vous avez saisi une date dans le champ Date de fin du relevé, la page Rapprochement compte bancaire filtre les écritures bancaires pour n’afficher que les écritures jusqu’à cette date. Vous ne pouvez reporter que des rapprochements bancaires avec des écritures bancaires au plus tard à la date de fin du relevé. Le filtre garantit que votre registre bancaire est équilibré avec votre relevé bancaire à la date de fin du relevé, la différence étant les paiements et les chèques en attente.

Lorsque la valeur du champ **Solde total** du volet **Lignes relevé bancaire** est égale à la valeur totale du champ **Solde à simuler** ainsi que le champ **Solde dernier relevé** du volet **Écritures de compte bancaire**, vous pouvez sélectionner l’action **Reporter**. Toutes les écritures de compte bancaire sans correspondance resteront sur la page, indiquant les différences que vous devez résoudre pour rapprocher le compte bancaire.

Pour revérifier le rapprochement de votre compte bancaire avant de le reporter, utilisez l’action **Rapport de test** pour préparer un aperçu du rapprochement. Le rapport est disponible dans les contextes suivants :

* Lorsque vous préparez un rapprochement bancaire sur la page **Rapprochement bancaire**.
* Lorsque vous rapprochez des paiements sur la page **Journaux rapprochement des paiements**.

Toutes les lignes qui ne peuvent pas être mises en correspondance, indiquées par une valeur dans le champ **Différence**, resteront sur la page **Rapprochement bancaire** après report. Elles représentent une certaine forme de différence que vous devez résoudre avant de pouvoir effectuer le rapprochement des comptes bancaires. Le tableau suivant décrit quelques situations commerciales typiques qui peuvent entraîner des différences.

| Distinction | Motif | Résolution |
|------------|--------|------------|
| Une transaction dans votre compte bancaire dans [!INCLUDE[prod_short](includes/prod_short.md)] ne figure pas sur le relevé bancaire. | La transaction bancaire n’a pas été créée alors qu’un report a été effectué dans [!INCLUDE[prod_short](includes/prod_short.md)]. | Créez la transaction manquante (ou demandez à un débiteur de la faire). Réimportez ensuite le fichier de relevé de compte ou saisissez la transaction manuellement. |
| Une transaction sur le relevé bancaire n’existe pas en tant que ligne journal ou document dans [!INCLUDE[prod_short](includes/prod_short.md)]. | Une transaction bancaire a été effectuée sans report correspondant dans [!INCLUDE[prod_short](includes/prod_short.md)], par exemple le report d'une ligne journal pour une dépense. | Créez et reportez l'écriture manquante. Pour apprendre un moyen rapide de lancer cette opération, consultez [Pour créer des écritures manquantes avec lesquelles faire correspondre des transactions bancaires](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines). |
| Une transaction dans le compte bancaire interne correspond à une transaction bancaire, mais certaines informations sont trop différentes pour établir une correspondance. | Des informations, telles que le montant ou le nom du client, ont été saisies différemment dans la transaction bancaire et le report interne. | Vérifiez les informations, puis faites les correspondre manuellement. Corrigez éventuellement la non-concordance des informations. |

Vous devez corriger les différences, par exemple en créant des écritures manquantes et en corrigeant les informations qui ne correspondent pas, ou en effectuant les transactions d’argent qui n’ont pas eu lieu, jusqu’à ce que le rapprochement du compte bancaire soit terminé et reporté.

Vous pouvez renseigner le volet **Lignes relevé bancaire** de la page **Rapprochement bancaire** des manières suivantes :

* Automatiquement, à l'aide de la fonction **Importer le relevé bancaire** pour renseigner le volet **Lignes relevé bancaire** avec des transactions bancaires en fonction d'un flux ou d'un fichier importé fourni par la banque.
* Manuellement, en utilisant la fonction **Proposer lignes** pour renseigner le volet **Lignes relevé bancaire** en fonction des factures dans [!INCLUDE[prod_short](includes/prod_short.md)] qui comportent des arriérés de paiement.

## Pour ajouter des lignes rapprochement bancaire en important un relevé bancaire

Le volet **Lignes relevé bancaire** sera renseigné avec des transactions bancaires en fonction d'un flux ou d'un fichier importé fourni par la banque.

Pour importer des relevés bancaires en tant que flux bancaires, vous devez configurer le service Envestnet Yodlee Bank Feed. La configuration inclut la liaison de vos comptes bancaires dans [!INCLUDE[prod_short](includes/prod_short.md)] avec les comptes bancaires en ligne associés. Pour plus d'informations, voir [Configurer le service Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).  

> [!TIP]
> Vous pouvez également importer des fichiers de relevés bancaires au format délimité par des virgules ou des points-virgules (.CSV). Utilisez la configuration assistée **Configurer un format de fichier de relevé bancaire** pour définir les formats d'importation des relevés bancaires et attacher le format à un compte bancaire. Vous pouvez ensuite utiliser ces formats lorsque vous importez des relevés bancaires dans la page **Rapprochement des comptes bancaires**.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Rapprochement bancaire**, puis sélectionnez le lien associé.
2. Sélectionnez l'action **Nouveau**.
3. Dans le champ **N° compte bancaire**, sélectionnez le compte bancaire approprié. Les écritures comptables compte bancaire qui existent pour le compte bancaire s'affichent le volet **Écritures comptables compte bancaire**.
4. Dans le champ **Date relevé**, saisissez la date du relevé de banque.
5. Dans le champ **Solde final du relevé**, saisissez le solde du relevé de banque.
6. Si vous avez un fichier de relevé bancaire, sélectionnez l'action **Importer le relevé bancaire**.
7. Localisez le fichier, puis sélectionnez le bouton **Ouvrir** pour importer les transactions bancaires dans le volet **Lignes relevé bancaire** sur la page **Rapprochement bancaire**.

## Pour renseigner les lignes rapprochement bancaire avec l’action Proposer lignes

Le volet **Lignes relevé bancaire** sera renseigné en fonction des factures dans [!INCLUDE[prod_short](includes/prod_short.md)] qui comportent des arriérés de paiement.  

1. Sur la page **Rapprochement bancaire**, sélectionnez l'action **Proposer lignes**.
2. Dans le champ **Date de début**, saisissez la date de validation la plus précoce des écritures comptables à rapprocher.
3. Dans le champ **Date de fin**, saisissez la date de validation la plus tardive des écritures comptables à rapprocher.

    > [!NOTE]
    > En règle générale, la date de fin correspond à la date spécifiée dans le champ **Date du relevé**. Cependant, si vous souhaitez rapprocher des transactions pour une partie seulement d’une période, vous pouvez saisir une date de fin différente.

4. Si vous ne souhaitez pas que les écritures du compte bancaire incluent des écritures inversées ouvertes sans correspondance, activez le bouton à bascule **Exclure les écritures inversées**. Par défaut, la liste des écritures des comptes bancaires inclura les écritures inversées jusqu’à la date du relevé.
5. Cliquez sur le bouton **OK**.

## Pour mettre en correspondance automatiquement des lignes de relevé de compte bancaire avec des écritures de compte bancaire

La page **Rapprochement bancaire** propose une fonctionnalité de correspondance automatique basée sur une correspondance entre le texte d'une ligne relevé bancaire (volet gauche) et celui d'une ou de plusieurs écritures de compte bancaire (volet droit). Vous pouvez remplacer la correspondance automatique suggérée, et vous pouvez choisir de ne pas utiliser du tout la correspondance automatique. Pour plus d'informations, voir [Pour faire correspondre manuellement des lignes relevé bancaire avec des écritures de compte bancaire](bank-how-reconcile-bank-accounts-separately.md#to-match-bank-statement-lines-with-bank-account-ledger-entries-manually).

Vous pouvez rechercher la base des correspondances en utilisant l’action **Détails de correspondance**. Par exemple, les détails incluront les noms des champs qui contenaient des valeurs correspondantes.  

1. Sur la page **Rapprochement bancaire**, sélectionnez l'action **Faire correspondre automatiquement**. La page **Faire correspondre les écritures bancaires** s’ouvre.
2. Dans le champ **Tolérance date transaction (jours)**, spécifiez le nombre de jours avant et après la date de report de l’écriture compte bancaire pendant lesquels l’action recherchera des dates transaction correspondantes dans le relevé bancaire.

    Si vous saisissez 0 ou laissez le champ vide, l’action **Faire correspondre automatiquement** recherchera uniquement les dates de transaction correspondantes sur la date de report de l’écriture compte bancaire.
3. Choisissez le bouton **OK**.

    Les lignes sont codées par couleur pour faciliter la compréhension de ce qu’il faut en faire. Toutes les lignes de relevé bancaire et les écritures de compte bancaire qui peuvent être rapprochées deviennent vertes, et la case **Affecté** est cochée. Les écritures compte bancaire qui sont déjà appariées sur d’autres rapprochements bancaires sont affichées en bleu.
4. Pour supprimer une correspondance, sélectionnez la ligne de relevé bancaire, et sélectionnez l'action **Supprimer correspondance**.

> [!TIP]
> Vous pouvez utiliser un mélange de correspondances manuelles et automatiques. Si vous avez mis en correspondance manuellement des écritures, la correspondance automatique n’écrasera pas vos sélections.

## Pour mettre en correspondance manuellement des lignes de relevé de compte bancaire avec des écritures de compte bancaire

> [!TIP]
> Lors de la mise en correspondance manuelle des lignes et des écritures, les actions **Afficher tout**, **Afficher les écritures inversées**, **Masquer les écritures inversées** et **Afficher non-correspondances** peuvent faciliter l’obtention d’une vue d’ensemble. Par défaut, les écritures du compte bancaire n’incluent pas les écritures inversées sans correspondance. Pour inclure ces écritures dans la liste et les faire correspondre manuellement, sélectionnez l’action **Afficher les écritures inversées**. Si vous choisissez de masquer les écritures inversées après avoir effectué une ou plusieurs correspondances, les écritures correspondantes sont toujours affichées.

1. Sur la page **Rapprochement comptes bancaires**, sélectionnez une ligne non affectée dans le volet **Lignes relevé bancaire**.
2. Dans le volet **Écritures comptables compte bancaire**, sélectionnez une ou plusieurs écritures comptables compte bancaire qui peuvent être mise en correspondance avec la ligne de relevé bancaire sélectionnée. Pour choisir plusieurs lignes, sélectionnez et maintenez la touche <kbd>CTRL</kbd> enfoncée, puis sélectionnez les lignes.

   > [!TIP]
   > Vous pouvez également faire correspondre manuellement plusieurs lignes de relevé bancaire avec une écriture de compte bancaire. Par exemple, cela peut être utile si votre dépôt bancaire contient plusieurs modes de paiement, tels que des cartes de crédit de différents émetteurs, et que votre banque les répertorie sur des lignes distinctes.
3. Sélectionnez l'action **Faire correspondre manuellement**.

    La ligne de relevé bancaire sélectionnée et les écritures compte bancaire sélectionnées deviennent vertes, et la case à cocher **Affecté** du volet de droite est activée.
4. Répétez les étapes 1 à 3 pour toutes les lignes de relevé bancaire qui ne sont pas mises en correspondance.

> [!TIP]
> Pour supprimer une correspondance, sélectionnez la ligne de relevé bancaire, et sélectionnez l'action **Supprimer correspondance**. Si vous avez rapproché plusieurs lignes de relevé bancaire avec une écriture et que vous devez supprimer une ou plusieurs des lignes correspondantes, toutes les correspondances manuelles sont supprimées pour l’écriture lorsque vous choisissez **Supprimer la correspondance**.

## Pour créer des écritures manquantes avec lesquelles faire correspondre des lignes relevé bancaire

Les relevés bancaires comportent parfois des montants correspondant à la facturation d’intérêts ou de frais. Ces lignes relevé bancaire ne peuvent pas être mises en correspondance, car il n’existe aucune écriture associée dans [!INCLUDE[prod_short](includes/prod_short.md)]. Vous devez ensuite reporter une ligne journal pour chaque transaction afin de créer une écriture associée avec laquelle elle peut être mise en correspondance.

1. Sur la page **Rapprochement compte bancaire**, sélectionnez l'action **Transférer vers journal général**.  
2. Sur la page **Tr. rapp. cpte banq.-jrnl gén.**, indiquez le journal général à utiliser, puis cliquez sur le bouton **OK**.

    La page **Journal général** s'ouvre. Elle contient de nouvelles lignes journal pour toutes les lignes de relevé bancaire dont les écritures sont manquantes.
3. Renseignez la ligne journal avec les informations appropriées, comme le compte de contrepartie. Pour plus d'informations, reportez-vous à [Utilisation des feuilles comptabilité](ui-work-general-journals.md).  
4. Pour examiner le résultat du report avant de reporter, choisissez l'action **Rapport de test**. L'état **Relevé de compte bancaire** s'ouvre et affiche les mêmes champs que dans l'en-tête de la page **Rapprochement compte bancaire**.
5. Sélectionnez l'action **Valider**.

    Une fois l’écriture reportée, faites-lui correspondre la ligne de relevé bancaire.
6. Réactualisez ou rouvrez la page **Rapprochement bancaire**. La nouvelle écriture comptable s'affiche dans le volet **Écritures comptables compte bancaire**.
7. Faites correspondre la ligne relevé de compte bancaire avec l'écriture compte bancaire, manuellement ou automatiquement.

## Trouver les transactions en suspens des périodes précédentes

Vous pouvez utiliser le rapport Relevé bancaire pour rechercher les transactions en suspens des périodes précédentes. Les transactions en suspens ont été ouvertes avant la date du relevé et n’ont pas été fermées, ou ont été fermées après la publication du rapprochement bancaire.

Lorsque vous exécutez le rapport Relevé bancaire à partir de la page Liste des relevés bancaires, vous pouvez activer le bouton à bascule **Écritures en suspens** et le rapport inclura une section qui répertorie les écritures en attente.

**Exemple** Nous avons des écritures de compte bancaire A, B et C sur notre compte bancaire pour le mois d’août. Lorsque nous rapprochons notre compte bancaire pour le mois d’août, nous trouvons une ligne de relevé bancaire qui correspond à l’écriture A, mais aucune pour B et C. Nous reportons donc le rapprochement avec l’écriture A rapprochée et les écritures B et C comme écritures en attente.

En septembre, nous recevons un paiement pour l’écriture B et décidons de rapprocher notre compte bancaire. Si nous exécutons le rapport Relevé bancaire avant de publier le rapprochement, nous aurons une transaction rapprochée et une en attente.

Si nous imprimons le rapport pour août, nous aurons des transactions en suspens pour nos écritures B et C, même si nous avons fermé l’écriture B en septembre.

## Annuler un rapprochement bancaire

Si vous découvrez une erreur dans un rapprochement bancaire reporté, vous pouvez utiliser l’action **Annuler** sur la page **Liste des relevés de compte bancaire** pour la corriger. Lorsque vous annulez un rapprochement bancaire reporté, les écritures sont déplacées vers la page **Rapprochement bancaire** et sont marquées comme **Ouvertes**, ce qui signifie qu’elles ne sont pas rapprochées. Vous pouvez ensuite corriger le rapprochement bancaire et le reporter à nouveau.

> [!NOTE]
> Dans la version nord-américaine, pour utiliser la fonction Annuler pour les rapprochements bancaires et les relevés bancaires reportés, vous devez activer le bouton bascule **Rapprochement bancaire avec correspondance automatique** sur la page **Configuration du grand livre**. La fonction Annuler n’est pas disponible pour les relevés bancaires reportés à partir des feuilles de calcul de rapprochement bancaire.

### Réutilisation du numéro de relevé bancaire

Le numéro de relevé bancaire utilisé pour le nouveau rapprochement bancaire est extrait du compte bancaire, tout comme le dernier relevé de solde. Vous pouvez modifier ces valeurs avant de commencer un nouveau rapprochement bancaire. Cependant, lorsque vous créez un nouveau rapprochement bancaire, [!INCLUDE[d365fin](includes/d365fin_md.md)] vérifie si le numéro de relevé est déjà attribué à un relevé bancaire reporté. Si le numéro est utilisé, mais que vous souhaitez que le nouveau relevé bancaire l’utilise à la place, vous pouvez utiliser **Modifier n° relevé** sur la page **Rapprochement bancaire**.

### Exemples

Voici quelques exemples de la façon de corriger une erreur sur un rapprochement bancaire reporté, avec ou sans l’utilisation du même numéro de relevé.

#### Exemple 1

Vous avez effectué des rapprochements bancaires pour janvier, février et mars. Le numéro de relevé bancaire était 100 pour mars. Plus tard, vous découvrez que mars n’a inclus que les entrées jusqu’au 30, ce qui signifie que les entrées pour le 31 sont manquantes. Vous devez donc refaire le rapprochement bancaire pour mars. Dans ce cas, nous allons ouvrir la page **Relevé bancaire**, choisissez le relevé de mars, puis choisissez **Annuler**. 

Le nouveau rapprochement bancaire porte le numéro de relevé 101. Pour réaffecter le nombre 100, choisissez **Modifier n° relevé** et entrez **100**. 

> [!TIP]
> N’oubliez pas de définir la date de fin de relevé appropriée (dans cet exemple, le 31 mars) et de modifier le champ **Solde dernier relevé**. 

#### Exemple 2

Vous avez effectué des rapprochements bancaires pour janvier, février, juin et juillet. Vous découvrez que février était incorrect. Supposons qu’il ait le numéro de déclaration 100. Comme dans l’exemple 1, vous utilisez les actions Annuler et Modifier n° relevé. pour changer le numéro de relevé comme dans l’exemple n° 1 ci-dessus et vous pouvez maintenant refaire le rapprochement bancaire de février.  

Après avoir reporté le rapprochement bancaire corrigé pour février, sur la fiche de compte bancaire correspondante, le champ **Dernier n° relevé** affichera **100**, et le champ **Solde dernier relevé** affichera le solde de fin du relevé de février. 

Si le prochain rapprochement bancaire que vous effectuez est pour mars, [!INCLUDE[d365fin](includes/d365fin_md.md)] attribuera 101 comme numéro de relevé et lui donnera le bon **Solde dernier relevé**.

Si le prochain rapprochement bancaire que vous effectuez concerne le mois d’août, envisagez de modifier les valeurs dans **N° dernier relevé** et **Solde dernier relevé** sur la fiche **Compte bancaire** avant de créer le prochain rapprochement bancaire, ou utilisez l’action **Modifier n° relevé** et modifiez également la valeur dans le champ **Solde dernier relevé** sur la page de rapprochement bancaire.

> [!NOTE]
> Le numéro de relevé est important lorsque vous effectuez des rapprochements bancaires avec des fichiers CAMT importés contenant des numéros de relevé ou lorsque vous effectuez un rapprochement sur la base de relevés bancaires imprimés. Si vous téléchargez simplement une série de transactions bancaires depuis votre banque en ligne, le numéro de relevé n’est généralement pas important.  
>
> Le dernier relevé de solde est conservé sur le compte bancaire pour minimiser les erreurs lors des rapprochements bancaires, mais il est également modifiable, vous permettant d’effectuer vos rapprochements bancaires dans l’ordre de votre choix. Cela signifie également que si vous annulez un relevé bancaire, le nouveau solde de clôture peut ne pas être le dernier relevé du solde sur le prochain relevé bancaire. Il n’y a aucune fonctionnalité qui vous permet de transférer un solde vers tous les relevés bancaires suivants, donc soyez conscient de cela lorsque vous utilisez Annuler.  

## Éviter le report direct

N’utilisez pas de compte GL qui permet le report direct dans votre groupe de report de compte bancaire. Le report direct rompra le lien entre l’écriture compte bancaire et l’écriture compte GL. Lorsque vous rapprochez votre compte bancaire, les écritures reportées directement dans le compte GL ne seront pas incluses et il sera difficile de mener à bien le rapprochement.

Cette erreur se produit souvent lors de la saisie d’un solde d’ouverture pour un compte bancaire. Il est important que vous ne comptabilisiez pas le solde d’ouverture directement dans le grand livre. Les écritures dans le compte GL qui sont reportées directement dans le compte GL causeront des problèmes. Par exemple, ces écritures peuvent vous empêcher de rapprocher votre compte bancaire. Pour les comptes bancaires en devise étrangère, les écritures peuvent entraîner l’accumulation de différences après le report d’autres rapprochements bancaires, en raison des ajustements du taux de change. Souvent, vous reportez le solde bancaire d’ouverture directement sur le compte bancaire, et le montant se retrouve ensuite dans le compte du grand livre. Sinon, inversez-le plus tard sur un compte du grand livre que vous utilisez pour équilibrer le solde d’ouverture du grand livre. Dans les deux cas, vous devez équilibrer toute écriture directe sur le compte du grand livre avant de commencer votre premier rapprochement bancaire, et surtout si le compte bancaire est en devise étrangère.

## Voir la [formation Microsoft](/training/modules/bank-reconciliation-dynamics-365-business-central/index) associée

## Voir aussi
[Rapprochement de comptes bancaires](bank-manage-bank-accounts.md)  
[Lettrage automatique des paiements et rapprochement des comptes bancaires](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Paramétrage des opérations bancaires](bank-setup-banking.md)  
[Configurer des règles pour l'affectation automatique des paiements](receivables-how-set-up-payment-application-rules.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
