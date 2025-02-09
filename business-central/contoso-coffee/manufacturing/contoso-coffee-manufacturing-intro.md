---
title: Introduction à la fabrication Contoso Coffee
description: Vue d’ensemble des scénarios relatifs à la façon dont les données de démonstration Contoso Coffee peuvent vous aider à apprendre à utiliser les capacités de fabrication dans Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4760
author: edupont04
ms.author: andreipa
---

# <a name="introduction-to-contoso-coffee-manufacturing" />Introduction à la fabrication Contoso Coffee

Contoso Coffee est une compagnie fictive qui produit des cafetières grand public et commerciales. Les applications **Contoso Coffee** pour Business Central ajoutent des données de démonstration que vous pouvez utiliser pour apprendre à utiliser les capacités de fabrication dans Business Central.  

L’application propose quatre produits optimisés pour différents scénarios :

- **SP-SCM1009 Airpot**  

  Ce produit est une nomenclature (BOM) avec un sous-ensemble, **Itinéraire**. Utilisez-le pour faire la démonstration du flux de production standard. Il est configuré avec des itinéraires alternatifs que vous pouvez utiliser pour illustrer différents scénarios impliquant des sous-traitants. Le mode d’évaluation stock est *Standard*.  

- **SP-SCM1011 Airpot Duo**  

  Ce produit requiert une traçabilité et possède une composante qui requiert également une traçabilité. Le mode d’évaluation stock est *Spécifique*.  

- **SP-SCM1004 Autodrip**  

  Ce produit est une nomenclature avec un sous-ensemble, **Itinéraire**. Nous le recommandons pour faire la démonstration des différentes méthodes de consommation à la fois pour les composantes et les opérations. Le mode d’évaluation stock est *Standard*.

- **SP-SCM1006 AutoDripLite**

  Ce produit comporte trois variantes et trois nomenclatures pouvant être affectées à des unités de stock. Le produit utilise le concept de nomenclature fantôme. Le mode d’évaluation stock est *Standard*.

Les activités de fabrication pour tous les scénarios utilisent l’emplacement *NORD*.  

> [!IMPORTANT]
> Avant d’exécuter l’un des scénarios pour Contoso Coffee, reportez toutes les lignes journal article avec soldes d’ouverture. Pour connaître plus d’exigences, voir la section [Configurer les données de Contoso Coffee](#set-up-contoso-coffee-manufacturing-data).

## <a name="set-up-contoso-coffee-manufacturing-data" />Configurer les données de fabrication Contoso Coffee

Pour utiliser les données de démonstration de fabrication Contoso Coffee, vous devez installer deux applications dans la compagnie concernée dans [!INCLUDE [prod_short](../../includes/prod_short.md)] :  

- **Jeu de données de démonstration Contoso Coffee**  

    Cette application fournit des données de démonstration pour l’application de base.  
- **Jeu de données de démonstration Contoso Coffee (Code pays)**  

    Cette application ajoute du contenu spécifique au pays en plus de l’application de base.

Ajoutez les applications à une compagnie vide dans un abonnement payant ou dans le cadre d’un essai. Par exemple, créez une compagnie sans exemples de données à partir du guide de configuration assistée **Créer une nouvelle compagnie** que vous pouvez ouvrir dans la liste **Compagnies**. Ajoutez ensuite les applications depuis le [marché](../../ui-extensions-install-uninstall.md#install) si elles ne sont pas déjà répertoriées sur la page **Gestion des extensions**.  

Une fois que les applications appropriées sont installées, accédez à la page [Données de démonstration Contoso Coffee](https://businesscentral.dynamics.com/?page=4760) dans [!INCLUDE [prod_short](../../includes/prod_short.md)] et modifiez les paramètres par défaut en fonction de vos besoins. La table suivante décrit les paramètres :  

|Champ  |Désignation  |
|---------|---------|
|**Année de début** |Spécifie la première année que vous souhaitez utiliser pour les données de démonstration Contoso Coffee. Selon la configuration de la compagnie, l’année est soit une année civile, soit une année fiscale.|
|**Lieu de production** |Spécifie l’entrepôt que vous souhaitez utiliser pour les opérations de production. La valeur par défaut est *NORD*, mais vous pouvez la modifier selon vos besoins.|
|**Type de compagnie**    |Spécifie si la compagnie actuelle doit déclarer la TVA ou la taxe de vente. |
|**National : groupe de report de marché**|Spécifie un code entreprise pour les clients et fournisseurs nationaux. Les codes entreprise sont utilisés lors du report des transactions. |
|**Capacité : groupe de report de produit**    |Spécifie un code pour les articles ou les ressources qui doivent être utilisés pour reporter la capacité.|
|**Détail : groupe de report de produit**    |Spécifie un code pour les articles ou les ressources qui doivent être utilisés pour reporter la vente détail.|
|**Mat. prem. : groupe de report de produit**    |Spécifie un code pour les articles ou les ressources qui doivent être utilisés pour reporter les matières premières. |
|**Code TVA base**    |Spécifie un groupe produits TVA existant qui sera utilisé pour les articles.|
|**Code fini**    |Spécifie un groupe produits existant qui sera utilisé pour les articles finis.|
|**Facteur prix**     |Spécifie un facteur pour convertir un prix USD/EUR en devise locale. *1* signifie que le prix est le même dans n’importe quelle devise. Un nombre plus élevé sera utilisé pour obtenir le prix dans la devise locale. |
|**Précision arrondissement**  |Définit comment les quantités consommées calculées sont arrondies une fois saisies sur les lignes journal consommation. Les quantités inférieures à 0,5 sont arrondies au chiffre inférieur. Les quantités égales ou supérieures à 0,5 sont arrondies au chiffre supérieur.|

Une fois que vous êtes prêt, choisissez l’action **Créer des données de démonstration**. L’ajout des données à la base de données sous-jacente prend quelques minutes, mais vous êtes ensuite prêt à exécuter les différents scénarios.  

## <a name="scenarios" />Cas de figure

Les données de démonstration de facturation Contoso Coffee prennent actuellement en charge les scénarios suivants pour les tests et la formation :

1. [Créer une nomenclature de production et une version de nomenclature](create-new-production-bom-version.md)  
2. [Créer un itinéraire](create-new-routing.md)  
3. [Créer un bon de production planifié ferme et le modifier](create-firm-planned-production-order-change.md)  
4. [Combiner la consommation automatique et la consommation manuelle](combine-automatic-manual-flushing.md)  
5. [Utiliser la planification des commandes pour créer et réserver un approvisionnement](order-planning-create-reserve-supply.md)  
6. [Configurer et traiter une opération de sous-traitance](set-up-process-subcontracting-operation.md)  
7. [Configurer une nouvelle capacité](set-up-new-capacity.md)  
8. [Prévoir la demande pour des variantes articles avec différentes nomenclatures affectées](variants.md)  

Lisez les étapes de chaque scénario dans l’article correspondant.  

> [!IMPORTANT]
> Ces procédures pas à pas nécessitent que l’expérience utilisateur soit définie sur *Premium* dans la page **Informations compagnie**.

## <a name="see-also" />Voir aussi

[Production](../../production-manage-manufacturing.md)  
[Rapports de production et analyses dans Business Central](../../production-reports.md)  
