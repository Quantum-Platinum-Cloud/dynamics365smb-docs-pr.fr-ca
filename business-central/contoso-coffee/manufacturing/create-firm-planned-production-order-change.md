---
title: Créer un bon de production planifié ferme et le modifier
description: 'Procédure pas à pas pour un gestionnaire de production chez Contoso Coffee qui souhaite créer un bon de production planifié ferme, puis le modifier.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# <a name="walkthrough-create-a-firm-planned-production-order-and-change-it" />Procédure pas à pas : Créer un bon de production planifié ferme et le modifier

Dans cet article, nous vous expliquons comment utiliser les données de démonstration Contoso Coffee pour les bons de production.  

## <a name="scenario" />Scénario

Eduardo, le gestionnaire de production chez Contoso Coffee, doit créer un bon de production pour 10 unités de l’article **SP-SCM1009, Airpot** dont l’échéance est le 28 avril. Eduardo effectue une planification en arrière et confirme qu’ils peuvent commencer l’ordre le 27 avril.  

Peu de temps après avoir terminé cette tâche, Eduardo doit augmenter l’ordre à 50 unités. Ce faisant, la date de début de l’ordre annoncée par la fonctionnalité de planification en arrière est trop tôt. Eduardo planifie donc l’ordre à partir du 23 avril afin de déterminer une date de fin plus réaliste.  

## <a name="steps" />Étapes

1. Créez le bon de production initial pour 10 unités de l’article **SP-SCM1009, Airpot**.

    1. Choisissez l'icône d'![ampoule qui ouvre la fonction Tell Me.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **bons de production planifiés fermes**, puis sélectionnez le lien associé.  

    2. Cliquez sur l’action **Nouveau**, puis renseignez les champs comme indiqué dans le tableau suivant.  

        |Champ  |Valeur  |
        |---------|---------|
        |**Type origine** |Article ;|
        |**N° origine** |SP-SCM1009|
        |**Quantité** |10|
        |**Date d’échéance**|Avril 28  |

    3. Choisissez l’action **Actualiser Bon de production**.  

    4. Sur la page **Actualiser Bon de production**, acceptez toutes les valeurs par défaut, puis choisissez le bouton **OK** pour démarrer le processus.  

        Dans la configuration actuelle, ce processus utilise la planification en arrière. Dans la nouvelle ligne du bon de production, la date début est le 26 avril.  

2. Modifiez la quantité du bon de production à 50 unités et programmez l’ordre.  

    1. Sur le raccourci **Lignes** de la **Nomenclature de production**, sélectionnez la ligne récemment ajoutée, puis, dans le champ **Quantité**, entrez *50*.  

3. Choisissez l’action **Actualiser Bon de production**.  

    La date de début est désormais repoussée au 20 avril. Cette date n’est pas acceptable pour Eduardo.

4. Déclenchez une planification en aval du bon de production.

    1. Sur le raccourci **Programmer**, définissez le champ **Date début** sur *23 avril*.

    La date de début de l’ordre est maintenant le 25 avril et la date de fin est le 2 mai. La date d’échéance de l’ordre est fixée un jour plus tard, le 3 mai. Eduardo sait maintenant que la livraison de l’ordre pour lequel la quantité a été augmentée aura lieu le 3 mai.

> [!NOTE]
> Planifier un ordre en modifiant sa date de début ou de fin ne nécessite pas d’effectuer le traitement en lot **Actualiser Bon de production**, car toutes les dates sont recalculées automatiquement.

Le nouveau bon de production est maintenant configuré et les exigences d’Eduardo sont satisfaites.  

## <a name="see-also" />Voir aussi

[Introduction aux données de démonstration Contoso Coffee](../contoso-coffee-intro.md)  
