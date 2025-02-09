---
title: "Procédure pas à pas\_: calcul des travaux en cours pour un projet"
description: 'Les projets impliquent la consommation d''heures employé, d''heures machines, d''articles en inventaire et d''autres types d''utilisation devant être suivis au fur et à mesure de l''avancée du projet.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="walkthrough-calculating-work-in-process-for-a-job" />Procédure pas à pas : calcul des travaux en cours pour un projet

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Avec les projets, vous pouvez programmer l'utilisation des ressources de votre compagnie et suivre les différents coûts pour un projet spécifique. Les projets impliquent la consommation d'heures employé, d'heures machines, d'articles en inventaire et d'autres types d'utilisation devant être suivis au fur et à mesure de l'avancée du projet. Si celui-ci couvre une longue période, il se peut que vous souhaitiez transférer les coûts correspondants vers un compte Travaux en cours (TEC) dans le bilan au cours de projet. Vous pouvez ensuite reconnaître les coûts et ventes dans vos comptes état des résultats, le cas échéant.  

## <a name="about-this-walkthrough" />À propos de cette procédure pas à pas

 Cette procédure pas à pas présente les tâches suivantes :  

-   calcul des TEC ;  
-   sélection d'une méthode de calcul TEC ;  
-   Exclusion d'une section du projet des TEC.  
-   Report des TEC dans le grand livre.  
-   Inversion d'un report TEC.  

 Chaque étape du processus calcule la valeur et déplace les transactions du projet dans le grand livre. Les phases de calcul et de report sont distinctes, ce qui vous permet de consulter vos données et d'y apporter des modifications avant de les reporter dans le grand livre. Vous devez donc vous assurer que toutes les informations sont correctes après avoir exécuté les traitements en lot de calcul et avant de lancer les traitements en lot de report.  

## <a name="roles" />Rôles

 Cette procédure pas à pas décrit les activités de Tricia, membre de l'équipe Projet.  

## <a name="prerequisites" />Conditions préalables

 Avant de pouvoir exécuter les tâches de cette procédure pas à pas, [!INCLUDE[prod_short](includes/prod_short.md)] doit être installé sur votre ordinateur.  

## <a name="story" />Scénario

 Ce procédure pas à pas se concentre sur la société CRONUS International Ltd., entreprise de conception et de conseil, qui conçoit et équipe de nouvelles infrastructures (telles que des salles de conférence et des bureaux) avec du mobilier, des accessoires et des unités de stockage. La majeure partie du travail à CRONUS est orientée projets et Tricia, membre de l'équipe Projet, utilise les projets pour obtenir un aperçu des projets en cours acceptés par CRONUS, ainsi que des projets terminés. Certains des projets peuvent être très longs et durer plusieurs mois. Tricia peut utiliser un compte TEC pour enregistrer les travaux en cours et suivre les coûts tout au long du projet.  

## <a name="calculating-wip" />Calcul TEC

 CRONUS a accepté un projet à long terme qui s'est étendu sur plusieurs périodes de reporting. Tricia, membre de l'équipe projet, calcule les travaux en cours (TEC) pour vérifier que l'état financier de la compagnie sera exact.  

 Au cours de cette procédure, Tricia sélectionne un groupe de tâches spécifique qui sera inclus dans le calcul TEC. Sur la page **Lignes tâche projet**, Tricia peut spécifier ces lignes dans la colonne **Total TEC**.  

 Le tableau suivant décrit trois options.  

|Champ|Description|  
|-------------------------------------|---------------------------------------|  
|**\<blank\>**|Laissez le champ vierge si la tâche projet fait partie d'un groupe de tâches.|  
|**Total**|Définit la plage ou le groupe de tâches incluses dans le calcul des TEC et de la réception. Au sein du groupe, n'importe quelle tâche projet dont le **Type tâche projet** est défini sur **Report** est incluse dans le total TEC, à moins que le champ **TEC-Total** soit paramétré sur **Exclu**.|  
|**Exclu**|S'applique uniquement à une tâche dont le **Type tâche projet** est défini sur **Validation**. La tâche n'est pas incluse lors du calcul des TEC et de la réception.|  

 Dans la procédure pas-à-pas suivante, Tricia applique la méthode Valeur de coût, la norme de leur compagnie, pour calculer les TEC. Tricia indique la partie du projet qui est incluse dans le calcul des TEC en affectant des valeurs Total TEC à différentes lignes tâche projet.  

### <a name="to-calculate-wip" />Pour calculer les TEC :

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Projets**, puis choisissez le lien associé.  
2.  Dans la liste **Projets**, sélectionnez le projet **Deerfield**, puis choisissez l'action **Modifier**. La fiche projet s'ouvre en mode édition.  

     Les TEC peuvent être calculés en fonction de la méthode sélectionnée dans ce champ : Valeur de coût, Valeur des ventes, Coût des ventes, Pourcentage avancement ou Fin de contrat. Dans cet exemple, CRONUS utilise la méthode Valeur de coût.  

3.  Sur le raccourci **Report**, choisissez le champ **Méthode TEC**, puis sélectionnez **Valeur de coût**.  
4.  Choisissez l'action **Lignes tâche projet** et définissez les valeurs suivantes dans le champ **Total TEC**.  

     Le tableau suivant décrit les valeurs.  

    |N° tâche projet|Champ Total TEC|  
    |------------------|----------------------|  
    |1130|Exclu|  
    |1190|Total|  
    |1210|Exclu|  
    |1310|Exclu|  

5.  Choisissez l'action **TEC**, puis l'action **Calculer TEC**.  
6.  Dans la page **Projet Calculer TEC**, vous pouvez sélectionner un projet pour lequel vous souhaitez effectuer le calcul TEC. Dans le raccourci **Projet**, sélectionnez **Deerfield** dans le champ **N°** .  
7.  Dans le champ **Date de report**, entrez une date postérieure à la date de travail.
8.  Dans le champ **N° document** , saisissez **1**. Cela crée un document auquel vous pourrez vous référer ultérieurement à des fins de traçabilité.  
9. Pour lancer le traitement par lots, cliquez sur le bouton **OK**. Un message s'affiche. Cliquez sur le bouton **OK** pour continuer. Fermez la page **Lignes tâche projet**.  

    > [!NOTE]  
    >  Le message déclare qu'il y a des avertissements associés au calcul TEC. Vous les examinerez dans la procédure suivante.  

10. Dans la fiche **Projet**, affichez le raccourci **TEC et Réception** afin de visualiser les valeurs calculées. Vous pouvez également visualiser **Date validation TEC** et les valeurs qui ont été validées dans la comptabilité, le cas échéant.  

 Notez que la valeur de **Montant coûts récep.** est 215,60 dans la colonne **À valider**. Cela reflète les coûts totaux de deux des éléments du groupe de tâches projet 1110 à 1130. Le troisième élément a été défini sur **Exclu**, et n'est donc pas inclus dans le calcul TEC.  

### <a name="to-review-wip-warnings" />Pour étudier les avertissements TEC

1.  Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Cockpit TEC**, puis choisissez le lien associé.  
2.  Sélectionnez le projet **Deerfield**, puis l'action **Afficher des avertissements**.  
3.  Sur la page **Avertissements TEC projet**, examinez l'avertissement associé au projet.  

 Après la fin de la période comptable, Tricia doit recalculer les TEC afin d'inclure le travail accompli jusqu'à cette date.  

### <a name="to-recalculate-wip" />Pour recalculer les TEC :

1.  Sur la fiche **Projet**, choisissez l'action **Écritures TEC** pour afficher le calcul TEC.  

     La page **Écritures TEC projet** affiche les dernières écritures TEC calculées pour un projet, même si les TEC n'ont pas encore été reportés dans le grand livre.  

2.  Vous pouvez suivre les étapes de la procédure qui explique comment calculer les TEC dans le but de recalculer les TEC. Lors de chaque calcul TEC, une écriture est créée sur la page **Écritures TEC projet**.  
3.  Fermez la page.  

> [!NOTE]  
>  Seuls les travaux en cours et les réceptions sont calculés. Il n'est pas reporté dans le grand livre. Pour ce faire, exécutez le traitement en lot **Reporter TEC au GL** à l'issue du calcul.

## <a name="posting-wip-to-general-ledger" />Report des TEC dans le grand livre

 Après avoir calculé les TEC pour ce projet, ils peuvent les reporter dans le grand livre.  

### <a name="to-post-wip-to-general-ledger" />Pour reporter les TEC dans le grand livre

1.  Dans la liste **Projets**, sélectionnez le projet **Deerfield**.  
2.  Choisissez l'action **TEC**, puis l'action **Reporter TEC au GL**.  
3.  Sur la page **Projet - Reporter TEC au GL**, sur le raccourci **Projet**, sélectionnez **Deerfield** dans le champ **N°**. .  
4.  Sur le raccourci **Options**, dans le champ **N° document contrepassation**, entrez **1**.  
5.  Cliquez sur le bouton **OK** pour valider les TEC en comptabilité.  
6.  Cliquez sur le bouton **OK** pour fermez la page de confirmation.  

     Après avoir terminé le report, vous pouvez visualiser les informations le concernant sur la page **Écritures GL TEC**.  

7.  Dans la liste **Projets**, sélectionnez le projet **Deerfield**, puis choisissez l'action **Écritures compta. TEC**.  

     Sur la page **Écritures GL TEC projet**, vérifiez que les TEC ont été reportés dans le grand livre.  

8.  Fermez la page.  
9. Ouvrez la fiche **Projet** pour le projet **Deerfield**.  
10. Sur le raccourci **TEC et Réception**, vous remarquez que dans la colonne **Reporté**, le champ **Montant GL coûts récep.** est à présent rempli, ce qui indique que les TEC ont bien été reportés dans le grand livre.  
11. Cliquez sur le bouton **OK** pour fermer la fiche.  

## <a name="reversing-a-wip-posting" />Inversion d'un report TEC

 Tricia conclut que les tâches projet qui ont été exclues du calcul des TEC auraient dues être incluses dans ce calcul. Tricia peut inverser les reports incorrects sans devoir rereporter les TEC.  

### <a name="to-reverse-a-wip-posting" />Pour inverser un report TEC

1.  Dans la liste **Projets**, sélectionnez le projet **Deerfield**.  
2.  Choisissez l'action **TEC**, puis l'action **Reporter TEC au GL**.  
3.  Sur la page **Projet - Reporter TEC au GL**, sur le raccourci **Projet**, sélectionnez **Deerfield** dans le champ **N°**. .  
4.  Sur le raccourci **Options**, dans le champ **N° document contrepassation**, entrez **1**.  
5.  Dans le champ **Date validation contrepassation**, saisissez la date validation originale. La date doit correspondre à celle utilisée initialement pour calculer les TEC.  
6.  Sélectionnez le champ **Contrepasser uniquement** . Cela permettra d'inverser les TEC précédemment reportés, sans reporter de nouveaux TEC dans le grand livre.  
7.  Cliquez sur le bouton **OK** pour exécuter le traitement en lot, puis sur le bouton **OK** pour fermer la page de confirmation.  
8.  Ouvrez la fiche **Projet** correspondant à **Deerfield**.  
9. Sur le raccourci **TEC et Réception** , vérifiez qu'il n'y a pas d'écritures TEC validées.  
10. Fermez cette page.  
11. Dans la liste **Projets**, sélectionnez le projet **Deerfield**, choisissez l'action **TEC**, puis l'action **Écritures compta. TEC**. La case du champ **Contre-passé** des écritures TEC est sélectionnée.  
12. Fermez cette page.  
13. Ouvrez les **Lignes tâche projet** pour le projet, incluez les sections du projet qui auraient dû faire partie du calcul des TEC, puis recalculez et validez le nouveau résultat en comptabilité.  

    > [!NOTE]  
    >  Supposons que Tricia a calculé et reporté les TEC d'un projet avec des dates incorrectes. En suivant la méthode vue précédemment, Tricia peut inverser les reports incorrects, corriger les dates et revalider les TEC dans le grand livre.  

## <a name="next-steps" />Étapes suivantes

 Cette procédure pas-à-pas vous a montré comment calculer les TEC dans [!INCLUDE[prod_short](includes/prod_short.md)]. Avec des projets plus vastes, il peut être utile de transférer les coûts vers un compte TEC de manière périodique tandis que le projet est en cours d’achèvement. Cette procédure pas-à-pas vous a montré comment exclure des lignes tâche d'un calcul. Elle vous montre également à quel moment vous devriez avoir à recalculer. Enfin, cette procédure pas-à-pas montre comment reporter les TEC dans le grand livre. Un exemple de la manière d'inverser un report des TEC dans le grand livre est également inclus.  

## <a name="see-related-microsoft-trainingtrainingpathscalculate-post-job-wip" />Voir la [formation Microsoft](/training/paths/calculate-post-job-wip/) associée

## <a name="see-also" />Voir aussi

 [Procédures pas à pas liées au processus entreprise](walkthrough-business-process-walkthroughs.md)  
 [Procédure pas à pas : gestion des projets](walkthrough-managing-projects-with-jobs.md)  
 [Comprendre les méthodes TEC](projects-understanding-wip.md)  
 [Surveillance de la progression et des performances](projects-how-monitor-progress-performance.md)  
 [Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
