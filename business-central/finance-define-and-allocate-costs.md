---
title: Définition et répartition des coûts
description: 'Les affectations de coûts déplacent les coûts et les revenus entre les types de coûts, les centres de coûts et les coûts associés. Vous pouvez définir autant d''affectations que nécessaire.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '1102, 1105, 1106, 1107, 1109, 1114'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="defining-and-allocating-costs" />Définition et répartition des coûts

Les affectations de coûts déplacent les coûts et les revenus entre les types de coûts, les centres de coûts et les coûts associés. Vous pouvez définir autant d'affectations que nécessaire. Chaque affectation comporte les éléments suivants :  

- Une source affectation.  
- Une ou plusieurs cibles d'affectation.  

La source d'affectation détermine les coûts à affecter, tandis que les cibles d'affectation déterminent à quels emplacement affecter ces coûts. Par exemple, les coûts pour le type de coût Fournitures non stockables représentent une source d'affectation. Vous affectez tous les coûts de fournitures non stockables à trois centres de coûts : Atelier, Production, et Vente. Ces centres de coûts sont les cibles d'affectation.  

Pour chaque source d'affectation, vous définissez un niveau d'affectation, une période de validité et une variante comme identificateur de regroupement. Vous pouvez utiliser un traitement en lot pour définir des filtres afin de sélectionner les définitions d'affectation, puis exécuter les affectations des coûts automatiquement.  

Pour chaque cible d'affectation, vous définissez une base d'affectation. La base d'affectation peut être statique ou dynamique.  

- Les bases d'affectation statique dépendent d'une valeur définie, par exemple, la superficie ou un ratio d'affectation prédéfini, comme 5:2:4.  
- Les bases d'affectation dynamique dépendent de valeurs variables, telles que le nombre d'employés dans un centre de coût ou les revenus de vente d'un objet de coûts associé pour une période donnée.  

Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.

## <a name="setting-up-allocation-source-and-targets" />Configuration de la source et des cibles d'affectation

Chaque affectation comporte une source et au moins une cible. La source d'affectation définit les coûts à affecter. Les cibles d'affectation déterminent où affecter ces coûts.  

### <a name="to-set-up-cost-allocations" />Pour configurer les affectations de coûts

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Affectation des coûts**, puis choisissez le lien associé.  
2. Sur la page **Affectation des coûts**, sélectionnez l'action **Modifier**.  
3. Dans le champ **ID**, entrez un ID pour la source d’affectation.  
4. Définissez un niveau compris entre les chiffres 1 et 99 dans le champ **Niveau**. Le report de l’affectation suit l’ordre des niveaux.  
5. Entrez un type de coût pour définir les types de coût à affecter dans le champ **Plage type de coûts**. Si tous les coûts pour un type donné sont affectés, aucune plage n'est définie.  
6. Entrez un centre de coûts avec des coûts à affecter dans le champ **Code centre de coûts**.  
7. Entrez un coût associé avec des coûts à affecter dans le champ **Code coûts associés**. Ce champ reste vide la plupart du temps car les coûts associés sont rarement affectés à d'autres coûts associés.  
8. Entrez un type de coût dans le champ **Type de crédit\\\/coût**. Les coûts affectés sont crédités dans le type de coût d’origine. Le report des crédits est reporté sur le type de coût spécifié ici.  
9. Sur le raccourci **Lignes**, définissez les cibles d’affectation. Sur la première ligne, entrez un type de coût dans le champ **Type coût cible**. Il définit le type de coût à partir duquel l'affectation est débitée.  
10. Sur la première ligne, saisissez la première cible d'affectation dans le champ **Centre de coûts cible** ou **Objet de coûts cible**. Ces deux champs définissent le centre de coûts ou l'objet de coûts à partir desquels l'affectation est débitée. Vous pouvez renseigner uniquement l'un de ces champs, mais pas les deux.  
11. Répétez les mêmes étapes sur la deuxième ligne pour configurer les cibles d'affectation supplémentaires.  
12. Après avoir paramétré la cible et les sources d’affectation, sélectionnez **Calculer la clé d'affectation** pour calculer le total des valeurs d'action.  

> [!NOTE]  
> Cochez la case **Bloqué** pour désactiver la configuration de l'affectation.

## <a name="setting-filters-for-dynamic-allocation-bases" />Définition de filtres pour les bases d'affectation dynamique

Le mode d'affectation dynamique dépend des valeurs modifiables. Par exemple, le nombre d'employés dans un centre de coûts ou le nombre d'articles vendus d'un objet de coûts pour une période donnée. Il existe neuf bases d'affectation prédéfinies et douze plages de dates dynamiques. Vous définissez plusieurs filtres en fonction de la base d'affectation.  

### <a name="setting-filters" />Définition des filtres

Le tableau suivant affiche les filtres applicables aux diverses bases de ventilation et les valeurs valides dans les champs **Filtre n°** et **Filtre groupe**. Sélectionnez <kbd>F1</kbd> dans le champ **Code filtre date** pour lire les descriptions détaillées.  

|**Base**|**Filtre n°**|**Code filtre date**|**Filtre centre de coûts**|**Filtre objet de coûts**|**Filtre groupe**|  
|--------------|----------------------------------------|----------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------|  
|Écritures|Compte général|Oui|Oui|Oui|N/A|  
|Écritures budget|Compte général|Oui|Oui|Oui|Nom de budget du grand livre|  
|Écritures du type de coût|Type coût|Oui|Oui|Oui|N/A|  
|Écritures budget des coûts|Type coût|Oui|Oui|Oui|Nom du budget|  
|Nombre de salariés|N/A|Oui|Oui|Oui|N/A|  
|Articles vendus (qté)|N° d'article|Oui|Oui|Oui|Groupe de report inventaire|  
|Articles achetés (qté)|N° d'article|Oui|Oui|Oui|Groupe de report inventaire|  
|Articles vendus (montant)|N° d'article|Oui|Oui|Oui|Groupe de report inventaire|  
|Articles achetés (montant)|Nombre d'articles|Oui|Oui|Oui|Groupe de report inventaire|

## <a name="scenario-1-defining-static-allocations-based-on-allocation-ratio" />Scénario 1 : Définition des affectations statiques en fonction du ratio d'affectation

Le mode d'affectation statique dépend d'une valeur définie, par exemple, les mètres carrés utilisés ou un ratio d'affectation prédéfini, comme 5:2:4.  

Cette rubrique décrit comment définir trois nouveaux objet de coûts pour la cible d'affectation pour le centre de coûts PROD de la source d'affectation à l'aide d'un ratio d'affectation prédéfini, comme 5:2:4. Les trois coûts associés cibles sont ACCESSO, PEINTURE et ACCESSOIRES.  

> [!NOTE]  
> L'exemple utilise les données de démonstration dans [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab" />Pour définir le centre de coûts PROD de la source d'affectation sur le raccourci Général

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Affectation des coûts**, puis choisissez le lien associé.  
2. Sur la page **Affectation des coûts**, sélectionnez l'action **Nouveau**.  
3. Dans le champ **Code**, sélectionnez <kbd>Entrée</kbd> ou entrez un code.  
4. Dans le champ **Niveau**, saisissez **1**.  
5. Dans les champs **Valide à partir de** et **Valide jusque**, entrez les dates appropriées.  
6. Dans le champ **Code centre de coûts**, entrez **PROD**.  
7. Dans le champ **Type de crédit\\\/coût**, entrez le type de coût **9903**.  

### <a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab" />Pour définir les coûts associés de la cible d'affectation sur le raccourci Lignes

1. Sur la première ligne facture, dans le champ **Type coût cible**, saisissez **9903**.  
2. Sur la première ligne facture, dans le champ **Coûts associés cibles**, saisissez **ACCESSO**.  
3. Sur la première ligne, dans le champ **Type cible affectation**, sélectionnez **Tous les coûts** pour définir le mode d'affectation de tous les coûts cumulés.  
4. Sur la première ligne, dans le champ **Base**, sélectionnez **Statique** pour utiliser le mode de ventilation statique.  
5. Sur la première ligne, dans le champ **Part**, saisissez le ratio d'affectation **5**.  
6. Sur la deuxième ligne, dans le champ **Type coût cible**, saisissez **9903**.  
7. Sur la deuxième ligne, dans le champ **Coûts associés cibles**, saisissez **PEINTURE**.  
8. Sur la deuxième ligne, dans le champ **Type cible affectation**, sélectionnez **Tous les coûts** pour définir le mode d'affectation de tous les coûts cumulés.  
9. Sur la deuxième ligne, dans le champ **Base**, sélectionnez **Statique** pour utiliser le mode de ventilation statique.  
10. Sur la deuxième ligne, dans le champ **Part**, saisissez le ratio d'affectation **2**.  
11. Sur la troisième ligne, dans le champ **Type coût cible**, saisissez **9903**.  
12. Sur la troisième ligne facture, dans le champ **Coûts associés cibles**, saisissez **ACCESSOIRES**.  
13. Sur la troisième ligne, dans le champ **Type cible affectation**, sélectionnez **Tous les coûts** pour définir le mode d'affectation de tous les coûts cumulés.  
14. Sur la troisième ligne, dans le champ **Base**, sélectionnez **Statique** pour utiliser le mode de ventilation statique.  
15. Sur la troisième ligne, dans le champ **Part**, saisissez le ratio d'affectation **4**.  

> [!IMPORTANT]  
> [!INCLUDE[prod_short](includes/prod_short.md)] calcule automatiquement le champ **Pour cent** à l'aide d'un pourcentage qui dépend de ces trois ratios d'affectation saisis dans le champ **Part** pour chacune des trois lignes.

## <a name="scenario-2-defining-dynamic-allocations-based-on-items-sold" />Scénario 2 : Définition des affectations dynamique sur la base des articles vendus

Cette rubrique explique comment définir les affectations à l'aide du mode d'affectation dynamique. Dans l'exemple, vous modifiez l'affectation dynamique des coûts pour que le centre de coûts VENTES prenne en charge le nouveau ÉQUIPEMENT IT de l'objet de coûts. Les packages ÉQUIPEMENT IT ont des numéros d'articles dont la plage s'échelonne entre 8904-W et 8924-W. Vous pouvez utiliser les chiffres de ventes de l'exercice précédent pour en calculer le partage. L'affectation est reportée en fonction du type de coût d'aide 9903.  

> [!NOTE]  
> L'exemple utilise les données de démonstration dans [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year" />Pour définir les ventilations dynamique en fonction des articles vendus de l'exercice précédent

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Affectations des coûts**, puis choisissez le lien associé.  
2. Sur la page **Affectation des coûts**, sélectionnez l'action **Nouveau**.  
3. Dans le champ **Code**, sélectionnez <kbd>Entrée</kbd> ou entrez un code.  
4. Dans le champ **Niveau**, saisissez **1**.  
5. Dans les champs **Valide à partir de** et **Valide jusque**, entrez les dates appropriées.  
6. Dans le champ **Code centre de coûts**, entrez **VENTES**.  
7. Dans le champ **Type de crédit\\\/coût**, entrez le type de coût **9903**.  
8. Dans le champ **Type coût cible**, entrez le type de coût **9903**.  
9. Dans le champ **Objet de coûts cible**, sélectionnez **Nouveau** pour créer un nouvel objet de coût ÉQUIPEMENT IT et renseigner les champs, le cas échéant. Sélectionnez **ÉQUIPEMENT IT**. Laissez le champ **Centre de coûts cible** vide.  
10. Dans le champ **Type cible affectation**, sélectionnez **Tous les coûts** pour définir le mode d'affectation de tous les coûts cumulés.  
11. Dans le champ **Base**, sélectionnez la base d'affectation **Articles vendus (Montant)**.  
12. Dans le champ **Filtre n°**, entrez **8904-W..8924-W**.  
13. Dans le champ **Code filtre date**, entrez **Année précédente**.  
14. Choisissez l'action **Calculer la clé d'affectation** pour calculer l'action.  

> [!IMPORTANT]  
> [!INCLUDE[prod_short](includes/prod_short.md)] utilise les chiffres de ventes des exercices précédents pour calculer une part de 1596,50 DS avec 100 % alloués pour les packages ÉQUIPEMENT IT. Cela signifie que tous les articles vendus au cours de l'exercice précédent seront affectés à l'ÉQUIPEMENT IT des objets de coûts.

## <a name="see-related-microsoft-trainingtrainingmodulesallocate-costs-dynamics-365-business-central" />Voir la [formation Microsoft](/training/modules/allocate-costs-dynamics-365-business-central/) associée

## <a name="see-also" />Voir aussi .

 [Paramétrage du contrôle de gestion](finance-set-up-cost-accounting.md)  
 [Transfert et report des écritures de coûts](finance-transfer-and-post-cost-entries.md)  
 [Comptabilité pour les coûts](finance-manage-cost-accounting.md)  
 [Terminologie en comptabilité analytique](finance-terminology-in-cost-accounting.md)  
 [À propos de la comptabilité analytique](finance-about-cost-accounting.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
