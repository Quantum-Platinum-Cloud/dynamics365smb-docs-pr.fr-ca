---
title: Configurer les cartes en ligne
description: Découvrez comment configurer Business Central pour proposer des itinéraires et des informations de localisation avec un service de carte en ligne.
author: rubenseishima
ms.service: dynamics365-business-central
ms.topic: article
ms.search.form: '800, 804'
ms.date: 07/15/2022
ms.author: a-reishima
---
# <a name="set-up-online-maps" />Configurer les cartes en ligne

Si vous prévoyez de rendre visite, par exemple, à un client, en suivant une adresse indiquée sur une fiche, vous pouvez vous procurer auprès d’un service de cartes en ligne une carte avec des instructions d’itinéraire fournies dans la langue que vous sélectionnez. Pour s’assurer que ce service de cartes en ligne trouvera la carte et l’itinéraire appropriés, vous devez le configurer dans [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="set-up-the-online-map-feature" />Configurer la fonctionnalité de carte en ligne par défaut

1. Sélectionnez l’icône en forme ![d’ampoule qui ouvre la fonction Tell Me 1.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") saisissez **Configuration Online Map**, puis choisissez le lien associé.
2. Sur la page **Configuration Online Map**, renseignez les champs. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
3. Activez le bouton bascule **Activé**.

### <a name="customize-the-online-map-provider-features" />Personnaliser les fonctionnalités du fournisseur de cartes en ligne

Pour personnaliser la fonction de carte en ligne au-delà des options répertoriées sur la page **Configuration Online Map** ou pour utiliser un autre fournisseur de cartes, procédez comme suit :

1. Sur la page **Configuration Online Map**, choisissez l’action **Définition paramètre**.
2. Sur la page **Définition paramètre Online Map**, choisissez l’action **Nouveau**.
3. Remplissez les champs pour personnaliser la façon dont [!INCLUDE[prod_short](includes/prod_short.md)] générera les URL des services disponibles. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
   * Consultez la liste **Paramètre de substitution Online Map** sur le volet **Récapitulatif** des données disponibles pour générer des URL.

## <a name="see-also" />Voir aussi .

[Utilisez des cartes en ligne pour trouver des emplacements et des directions](across-online-maps.md)  
[Préparation aux activités commerciales](ui-get-ready-business.md)  
[Administration](admin-setup-and-administration.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
