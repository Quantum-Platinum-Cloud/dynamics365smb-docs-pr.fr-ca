---
title: 'Paramétrer les coûts, prix, et capacité des projets'
description: 'Pour utiliser des ressources et faciliter la gestion de projets, vous spécifiez les coûts et les prix des différents ressources ou groupes de ressources, et définissez la capacité ressource.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'project management, capacity, staff'
ms.search.form: '72, 76, 77, 203, 204'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="set-up-resources-for-projects" />Configurer des ressources pour les projets

Pour gérer correctement les activités liées aux ressources, vous devez configurer ces dernières, ainsi que les coûts et prix associés. Les prix, remises et règles de facteur coût associés au projet, sont définis dans la fiche projet. Vous pouvez spécifier les coûts et prix pour des ressources individuelles, des groupes de ressources, ou toutes les ressources disponibles de la compagnie.

Lorsque des ressources sont utilisées ou vendues dans le cadre d'un projet, les prix et les coûts qui leur sont associés sont récupérés à l'aide des informations de configuration.

Vous spécifiez le montant horaire par défaut lors de la création de la ressource. Par exemple, si vous utilisez une machine spécifique pour un projet de cinq heures, le projet sera calculé sur la base du montant horaire.

> [!NOTE]
> Vous pouvez acheter des ressources externes non liées à un projet, par exemple pour facturer un fournisseur pour le travail fourni. Pour plus d'informations, voir [Enregistrer des achats](purchasing-how-record-purchases.md).<br /><br />
> Il est recommandé de nommer ou de regrouper les ressources externes afin de ne pas les confondre avec vos ressources internes.
>  
> Si vous reportez des transactions intercompagnies, même si vous pouvez affecter une ressource à une ligne d’un document de vente, si vous convertissez le document de vente en bon de commande côté réception, la ressource ne sera pas incluse. Pour utiliser des ressources dans des transactions intercompagnies, utilisez le champ **N° cpte G/L partenaire ach. IC** sur la fiche ressource pour spécifier le compte sur lequel reporter les dépenses.

## <a name="to-set-up-a-resource" />Pour paramétrer une ressource

Créez une fiche pour chaque ressource à utiliser dans les projets.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Ressources**, puis choisissez le lien associé.
2. Sélectionnez l'action **Nouveau**.
3. Renseignez les champs selon vos besoins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-a-resource-group" />Pour configurer un groupe de ressources

Vous pouvez combiner plusieurs ressources dans un groupe ressources. Toutes les capacités et tous les budgets du groupe ressources sont additionnés à partir des ressources. Il est également possible de saisir des capacités pour les groupes ressource, indépendamment des valeurs cumulées ou en plus de ces valeurs.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Groupes de ressources**, puis choisissez le lien associé.
2. Sélectionnez l'action **Nouveau**.
3. Renseignez les champs selon vos besoins.

## <a name="to-set-capacity-for-a-resource" />Pour définir la capacité d'une ressource

Pour calculer le temps qu'une ressource peut passer sur des projets, leur capacité doit d'abord être configurée comme temps disponible par période sur le calendrier de travail. Cette configuration est utilisée lorsque vous renseignez les lignes planification projet qui contiennent la ressource. Pour plus d'informations, voir [Créer des projets](projects-how-create-jobs.md).

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Ressources**, puis choisissez le lien associé.
2. Ouvrez la fiche ressource appropriée, puis cliquez sur **Capacité ressource**.
3. Sur la page **Capacité ressource**, dans le champ **Afficher par**, précisez la durée de la période (par exemple **Jour**) qui est indiquée dans le raccourci **Matrice Capacité ressource**.
4. Pour chaque ressource sur une ligne, spécifiez pour chaque période sur les colonnes le nombre d'heures pendant lesquelles la ressource est disponible.
5. Sinon, pour détailler la capacité hebdomadaire de la ressource dans un certain intervalle de temps, cliquez sur **Paramétrage capacité ressource**.
6. Sur la page **Paramétrage capacité ressource**, renseignez les champs sur une ligne selon vos besoins.
7. Cliquez sur **Mettre à jour la capacité**. La page **Capacité ressource** est mise à jour avec la capacité saisie.
8. Fermez la page.

## <a name="to-set-up-alternate-resource-costs" />Pour configurer des coûts ressource secondaires

Outre le coût spécifié sur la fiche ressource, vous pouvez configurer des coûts secondaires pour chaque ressource. Par exemple, si le taux horaire d'un employé augmente en raison d'heures supplémentaires, vous pouvez configurer un coût ressource pour le taux lié aux heures supplémentaires. Le coût secondaire que vous avez configuré pour la ressource remplace le coût de la fiche ressource lorsque vous utilisez la ressource dans le journal ressource.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Ressources**, puis choisissez le lien associé.  
2. Sélectionnez la ressource pour laquelle vous souhaitez configurer un ou plusieurs coûts secondaires, puis cliquez sur **Coûts**.  
3. Sur la page **Coûts ressource**, renseignez les champs sur une ligne selon vos besoins.  
4. Répétez l'étape 3 pour chaque autre coût ressource à configurer.

**Remarque**. Pour configurer des coûts ressource s'appliquant à toutes les ressources et à tous les groupes ressources, ouvrez la page **Coûts ressource** et renseignez les champs.

## <a name="to-set-up-alternate-resource-prices" />Pour configurer le prix des ressources secondaires

Outre le prix spécifié sur la fiche ressource, vous pouvez configurer des prix secondaires pour chaque ressource. Ces prix secondaires peuvent être conditionnels. Ils peuvent être liés à l'utilisation de la ressource avec un projet ou un type travail donné.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Ressources**, puis choisissez le lien associé.
2. Sélectionnez la ressource pour laquelle vous souhaitez configurer un ou plusieurs prix secondaires, puis sélectionnez l'action **Prix**.
3. Sur la page **Prix ressource**, renseignez les champs sur une ligne selon vos besoins.
4. Répétez l'étape 3 pour chaque autre prix ressource à configurer.

## <a name="see-related-microsoft-trainingtrainingpathsset-up-jobs-resources" />Voir la [formation Microsoft](/training/paths/set-up-jobs-resources/) associée

## <a name="see-also" />Voir aussi .

[Configuration de la gestion de projet](projects-setup-projects.md)  
[Gestion de projets](projects-manage-projects.md)  
[Finance](finance.md)  
[Procédure d'achat](purchasing-manage-purchasing.md)  
[Vente](sales-manage-sales.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
