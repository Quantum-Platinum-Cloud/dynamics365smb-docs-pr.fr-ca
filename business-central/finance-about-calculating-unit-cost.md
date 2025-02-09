---
title: À propos du calcul du coût unitaire
description: Découvrez comment la méthode d’évaluation stock et d’autres facteurs influencent le champ Coût unitaire de la fiche Article.
author: rubenseishima
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 03/06/2022
ms.author: a-reishima
---
# <a name="about-unit-cost-calculation" />À propos du calcul du coût unitaire

Chaque article a un coût unitaire qui est calculé en fonction de la méthode d’évaluation stock de la compagnie et d’autres facteurs. En règle générale, avec le mode évaluation stock *standard*, la valeur du champ **Coût unitaire** repose sur le coût standard de l’article. Pour toutes les autres méthodes d’évaluation stock (*FIFO*, *LIFO*, *Spécifique* et *Moyen*), le coût unitaire est calculé sur la base du coût unitaire moyen sur une période.  

Pour plus d’informations, reportez-vous à [Gestion des coûts de l'inventaire](finance-manage-inventory-costs.md).  

## <a name="when-is-the-unit-cost-field-updated" />À quel moment le champ Coût unitaire est-il mis à jour

Le mode évaluation stock a une incidence sur le moment où le champ **Coût unitaire** est mis à jour.

Lorsque le mode évaluation stock est défini sur *Standard*, le champ **Coût unitaire** est mis à jour chaque fois que le coût standard est modifié, et les utilisateurs ne peuvent pas modifier le champ **Coût unitaire**. Pour plus d’informations, voir [Mise à jour des coûts standard](finance-how-to-update-standard-costs.md).

Si le mode d’évaluation du stock est *FIFO*, *LIFO*, *Spécifique* ou *Moyen*, le champ **Coût unitaire** est mis à jour dans les cas suivants :

* Lorsque l’article fait l’objet d’un ajustement des coûts, automatiquement ou par une tâche [Ajuster coûts](inventory-how-adjust-item-costs.md#to-adjust-item-costs-manually).
* Lors du report de factures achat, de production ou d’ajustement positif si l’une des conditions suivantes est remplie :
  * Le solde quantités facturées de l'article, négatif ou égal à zéro, est changé en valeur positive.
  * Le coût unitaire actuel est nul.

Si l’une de ces conditions est remplie, le champ **Coût unitaire** est mis à jour avec la valeur du champ **Dernier coût direct** de la fiche article.

> [!NOTE]
> Le champ **Coût unitaire** n’est pas mis à jour si le coût unitaire actuel est supérieur à zéro et que le nouveau coût unitaire est égal à zéro. Un coût unitaire de zéro est considéré comme une exception aux activités régulières. Par conséquent, le coût unitaire actuel est retenu pour fournir la dernière valeur pertinente connue. Cette exception s’applique même si l’inventaire existant a été réévalué à zéro.

Dans le champ **Coût unitaire** de la fiche article, vous pouvez explorer pour afficher l’historique des transactions à partir duquel est calculé le coût moyen des unités disponibles sur la fenêtre **Aperçu calc. coût moyen**.

## <a name="unit-cost-calculation-for-purchases" />Calcul du coût unitaire pour les achats

Lorsque vous achetez des articles, le programme copie toujours la valeur du champ **Dernier coût direct** de la fiche article vers le champ **Coût unitaire direct** d’une ligne achat ou vers la ligne **Montant unitaire** sur une ligne journal article.

L'élément sélectionné dans le champ **Mode d'évaluation du stock** détermine la façon dont [!INCLUDE[prod_short](includes/prod_short.md)] calcule le contenu du champ **Coût unitaire** sur les lignes.

### <a name="costing-method-fifo-lifo-specific-or-average" />Modes d’évaluation du stock FIFO, LIFO, spécifique ou moyen

[!INCLUDE[prod_short](includes/prod_short.md)] calcule la valeur du champ **Coût unitaire $** sur la ligne achat, ou la valeur du champ **Coût unitaire** sur la ligne journal article sur la base de la formule suivante :

*Coût unitaire $ = (Coût unitaire direct - (Montant de l'escompte/Quantité)) x (1 + % du coût indirect/100) + Frais généraux*

### <a name="costing-method-standard" />Mode évaluation stock Standard

Le champ **Coût unitaire $** sur la ligne achat, ou le champ **Coût unitaire** est renseigné sur la ligne journal article en copiant la valeur du champ **Coût unitaire** de la fiche article. En utilisant le mode évaluation stock *Standard*, cette valeur repose toujours sur le coût standard.

Lorsque vous reportez l’achat, [!INCLUDE[prod_short](includes/prod_short.md)] utilise le coût unitaire de la ligne achat ou de la ligne journal article vers l’écriture facture article d’achat. Vous pouvez le voir sur la liste des entrées pour l’élément.

### <a name="all-costing-methods" />Tous les modes évaluation stock

Le programme utilise toujours le coût unitaire de la ligne document source pour calculer la valeur du champ **Coût indiqué (réel)**, ou éventuellement du champ **Coût indiqué (prévu)** concernant cette écriture article, quel que soit la méthode évaluation coût de l'article.

## <a name="unit-cost-calculation-for-sales" />Calcul du coût unitaire pour les ventes

Lorsque vous vendez des articles, le coût unitaire est copié du champ **Coût unitaire** de la fiche article vers la ligne vente ou la ligne journal article.

Lorsque vous reportez, le programme copie le coût unitaire vers l'écriture article facture vente, et il peut être vu dans la liste d'écritures de l'article. [!INCLUDE[prod_short](includes/prod_short.md)] utilise le coût unitaire de la ligne document source pour calculer la valeur du champ **Coût indiqué (réel)**, ou éventuellement du champ **Coût indiqué (prévu)** dans l'écriture valeur concernant cette écriture article.

## <a name="see-also" />Voir aussi .

[Gestion des coûts ajustés](finance-manage-inventory-costs.md)  
[Enregistrement de nouveaux articles](inventory-how-register-new-items.md)  
[À propos de l'évaluation des coûts de stock](finance-learn-about-costing.md)  
[Stock](inventory-manage-inventory.md)  
[Ventes](sales-manage-sales.md)  
[Procédure d'achat](purchasing-manage-purchasing.md)  
[Pratiques de configuration recommandées : mode évaluation stock](setup-best-practices-costing-method.md)  
[Détails de conception : modes évaluation stock](design-details-costing-methods.md)  
[Détails de conception : ajustement des coûts](design-details-cost-adjustment.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
