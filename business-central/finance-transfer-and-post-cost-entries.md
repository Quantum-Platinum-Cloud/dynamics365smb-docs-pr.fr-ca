---
title: Transfert et report des écritures de coûts
description: 'Avant de définir des affectations de coûts, vous devez comprendre les différentes sources d’où proviennent les écritures de coûts.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '1100, 1103, 1104, 1108, 1113, 1135'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="transferring-and-posting-cost-entries" />Transfert et report des écritures de coûts

Avant de définir des affectations de coûts, vous devez comprendre comment les écritures de coûts proviennent des sources suivantes :  

- Transfert automatique des écritures.  
- Report manuel de coûts pour les écritures de coûts, les frais internes et les affectations manuelles.  
- Validation automatique de l'affectation de coûts réels.  
- Transfert des écritures budgétées vers les écritures réelles.

## <a name="criteria-for-transferring-general-ledger-entries-to-cost-entries" />Critères de transfert des écritures vers les écritures de coûts

Il est important de comprendre les critères pour le transfert des écritures aux écritures de coûts. Lors du transfert, le traitement par lots pour **Transférer les écritures comptables vers CA** applique les critères suivants pour déterminer si les écritures comptables sont transférées et comment.  

Les écritures sont transférées si :  

- Les écritures ont des valeurs de dimension correspondant à un centre de coûts ou à un objet de coûts.  
- Les écritures ont des valeurs de dimension correspondant à un centre de coûts et à un objet de coûts. Pour ces écritures, le centre de coûts est prioritaire. Vous pouvez ainsi éviter qu'un type de coût apparaisse à la fois dans un objet de coûts et dans un centre de coûts, ce qui le comptabiliserait deux fois dans les statistiques.  
- Le numéro de document dans les écritures est vide. C'est pourquoi, il s'affichera avec le numéro de document 0000 dans les écritures de coûts.  
- Les écritures sont transférées vers un type de coût qui autorise les écritures combinées. Ces écritures sont transférées ainsi sur une base mensuelle ou journalière.  

Les écritures ne sont pas transférées si :  

- Les écritures ont des valeurs de dimension ne correspondant ni à un centre de coûts ni à un objet de coûts.  
- Les écritures sont égales à zéro.  
- Les écritures ont un compte du grand livre qui a été supprimé.  
- Les écritures ont un compte général qui n'est pas du type **Comptes de gestion**.  
- Les écritures ont un compte du grand livre sans type de coût affecté.  
- La date de report des écritures est antérieure à la **Date début pour transfert grand livre**.  
- Les écritures ont été reportées avec une date de fermeture. Il s'agit généralement des écritures qui redéfinissent le solde des états des résultats sur la fin de l'exercice.

## <a name="transferring-general-ledger-entries-to-cost-entries" />Transfert des écritures GL vers les écritures de coûts

Vous pouvez transférer les écritures vers les écritures de coûts.  

Avant d'exécuter le transfert des écritures vers des écritures de coûts, vous devez vous y préparer pour éviter tout report manuel de correction.  

### <a name="to-prepare-the-transfer" />Pour préparer le transfert

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Configuration comptabilité analytique**, puis choisissez le lien associé.  
2.  Sur la page **Configuration comptabilité analytique**, vérifiez que le champ **Date début pour transfert GL** est défini sur la valeur appropriée.  
3.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Plan comptable des types de coûts**, puis choisissez le lien associé.  
4.  Sur la page **Fiche type de coût**, vérifiez que le champ **Plage compte du grand livre** est lié correctement de sorte que chaque type de coût récupère les écritures du grand livre.  
5.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Plan comptable**, puis choisissez le lien associé.  
6.  Pour chaque compte GL approprié, sur la page **Fiche compte du grand livre**, vérifiez que le champ **N° type coût** est lié correctement à un type de coût. Pour plus d'informations, voir [Configuration du contrôle de gestion](finance-set-up-cost-accounting.md).  
7.  Vérifiez que toutes les écritures GL comprennent des valeurs de dimension correspondant à un centre de coûts et à un objet de coûts.  

### <a name="to-transfer-general-ledger-entries-to-cost-entries" />Pour transférer les écritures vers les écritures de coûts

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Transférer les écritures comptables vers CA**, puis sélectionnez le lien associé.  
2.  Cliquez sur le bouton **Oui** pour démarrer le transfert. Le processus transfère toutes les écritures qui n'ont pas encore été transférées.  

Lors du transfert, le processus crée des connexions dans les écritures des tables **Écriture de coûts** et **Registre de coûts**. Cela permet d'identifier l'origine des écritures de coûts.

## <a name="automatic-transfer-and-combined-entries" />Transfert automatique et écritures combinées

En comptabilité analytique, vous pouvez transférer les écritures vers un type de coût à l'aide d'un report combiné. Vous pouvez spécifier si un type de coût reçoit des écritures combinées dans le champ **Combiner écritures** dans la définition du type de coût. Le tableau suivant décrit les différentes options.  

|Combiner écritures|Description|  
|---------------------|-----------------|  
|Aucun|Chaque écriture est transférée individuellement vers le type de coût correspondant.|  
|Jour|Les écritures, dont la date de report est identique, sont transférées en une seule écriture vers le type de coût correspondant.|  
|Mois|Toutes les écritures du même mois calendaire sont transférées en une seul écriture vers le type de coût correspondant.|  

> [!IMPORTANT]  
>  Si vous avez coché la case **Transférer automatiquement à partir du GL** sur la page **Configuration de la comptabilité analytique**, [!INCLUDE[prod_short](includes/prod_short.md)] met à jour la comptabilité analytique après chaque report dans le grand livre. Les écritures combinées ne sont pas possibles.

## <a name="results-of-transferring-general-ledger-entries-to-cost-entries" />Résultats du transfert des écritures GL vers les écritures de coûts

Lors du transfert des écritures GL vers les écritures de coûts, [!INCLUDE[prod_short](includes/prod_short.md)] crée des connexions dans les écritures des tables **Écriture**, **Écriture de coûts** et **Registre de coûts** pour assurer le suivi des connexions entre les écritures de coûts et les écritures GL.  

### <a name="general-ledger-entries" />Écritures journal général

Pour chaque écriture GL transférée vers la comptabilité analytique, [!INCLUDE[prod_short](includes/prod_short.md)] renseigne le champ **N° écriture**.  

### <a name="cost-entries" />Écritures de coûts

Pour chaque écriture de coûts, [!INCLUDE[prod_short](includes/prod_short.md)] garde le numéro d'écriture de l'écriture GL correspondante dans le champ **N° Écriture** de la table **Écriture de coûts**.  

Pour les écritures de coûts combinées, [!INCLUDE[prod_short](includes/prod_short.md)] garde le numéro de la dernière écriture comptable, à savoir l'écriture avec le numéro le plus élevé.  

Le champ **Compte du grand livre** de la table **Écriture de coûts** contient le numéro du compte GL, d'où provient l'écriture de coûts.  

Pour les écritures de coûts uniques, [!INCLUDE[prod_short](includes/prod_short.md)] transfère le texte de validation depuis l'écriture comptable vers le champ de texte **Description**. Pour les écritures combinées, le champ de texte indique que ces écritures sont transférées en tant qu'écritures combinées. Par exemple, pour une écriture combinée pour octobre 2013, le texte peut être **Écritures combinées, octobre 2013**.  

### <a name="cost-register" />Registre de coûts

Dans la table **Registre de coûts**, [!INCLUDE[prod_short](includes/prod_short.md)] crée une écriture à l'aide du transfert source depuis la comptabilité. L'écriture enregistre le premier et le dernier numéros des écritures transférées, en plus des premier et dernier numéros des écritures de coûts créées.

## <a name="see-related-microsoft-trainingtrainingmodulestransfer-gl-entries-dynamics-365-business-central" />Voir la [formation Microsoft](/training/modules/transfer-gl-entries-dynamics-365-business-central/) associée

## <a name="see-also" />Voir aussi .

 [À propos de la comptabilité analytique](finance-about-cost-accounting.md)  
 [Paramétrage du contrôle de gestion](finance-set-up-cost-accounting.md)  
 [Définition et répartition des coûts](finance-define-and-allocate-costs.md)  
 [Comptabilité pour les coûts](finance-manage-cost-accounting.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
