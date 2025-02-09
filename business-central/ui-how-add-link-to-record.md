---
title: 'Ajouter des pièces jointes, des liens et des notes sur des enregistrements'
description: 'Joignez un lien hypertexte pointant vers un document ou un site Web à un enregistrement spécifique, tel qu’une fiche client ou un document.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: how-to
ms.date: 02/24/2023
ms.custom: bap-template
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents" />Gérer les pièces jointes, les liens et les notes sur les fiches et les documents

Sur la plupart des pages de liste, fiches et documents, vous pouvez joindre des fichiers, ajouter des liens et rédiger des notes dans l’onglet **Pièces jointes** du volet **Récapitulatif**. Le nombre situé dans le titre de l’onglet indique le nombre de fichiers, liens ou notes attachés existants pour la fiche ou le document.

Dans le raccourci **Lignes**, vous pouvez également utiliser l’action **Pièces jointes** pour joindre des documents à une ligne spécifique. Par exemple, vous souhaiterez peut-être joindre des spécifications de conception à un article sur une facture achat.

Les pièces jointes, les liens et les notes restent attachés à la fiche ou au document pendant son passage à d’autres provinces. Par exemple, d’un document de vente en cours à une facture client reportée. Cependant, aucun type de pièce jointe n'est sorti du système, par exemple lors de l'impression ou de l'enregistrement dans un fichier.

Vous pouvez également ajouter des pièces jointes aux courriels que vous envoyez depuis [!INCLUDE [prod_short](includes/prod_short.md)]. Lorsque vous envoyez un courriel directement à partir d’un document, tel qu’un devis, l’action **Ajouter un fichier à partir du document source** vous permet de choisir les fichiers qui y sont joints. Vous ne pouvez choisir que les fichiers joints au document. Vous ne pouvez pas choisir des fichiers joints à des lignes.

> [!NOTE]
> Lorsque vous livrez et facturez partiellement un document de vente ou un bon de commande, la pièce jointe ne sera annexée qu'à la facture finale de cette commande. De même, lorsque vous facturez à l’aide de la fonction Reports, la pièce jointe est annexé aux écritures GL pour le document, mais pas pour les écritures report.
>
> Si vous supprimez une commande avant qu'elle ne soit facturée, la pièce jointe est également supprimée. Lorsque vous facturez des bons de commande à l'aide de l'action Obtenir des lignes de réception à partir d'une facture achat, la pièce jointe sur les bons de commande n'est pas ajoutée à la facture achat.

## <a name="to-attach-a-file-to-a-purchase-invoice" />Pour joindre un fichier à une facture achat

Vous pouvez joindre n’importe quel type de fichier, tel que des fichiers texte, image ou vidéo, à une fiche, un document ou une ligne sur un document. Ceci est utile, par exemple, lorsque vous souhaitez stocker la facture d’un fournisseur sous forme de fichier PDF sur la facture achat correspondante dans [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Les fichiers joints à la fonction Documents entrants ne sont pas inclus dans l’onglet **Pièces jointes**. Pour plus d’informations, voir [Documents entrants](across-income-documents.md). Il en va de même pour les fichiers joints à des lignes sur des documents.

La procédure suivante se base sur une facture achat. Les étapes sont similaires pour tous les autres documents et fiches pris en charge.

> [!TIP]
> Si votre pièce jointe est spécifique à une ligne d’un document, vous pouvez la joindre à la ligne. Choisissez la ligne, puis choisissez l’action **Pièces jointes**.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Factures achat**, puis sélectionnez le lien associé.
2. Ouvrez la facture achat à laquelle vous souhaitez joindre un fichier.
3. Dans le volet **Récapitulatif**, sélectionnez l’onglet **Pièces jointes**.
4. Choisissez la valeur associée au champ **Documents**, telle que « 0 ».
5. Sur la page **Documents joints**, dans le champ **Pièce jointe**, choisissez l'action **Sélectionner un fichier**.
6. Sélectionnez un fichier à n'importe quel emplacement, puis choisissez le bouton **Ouvrir**.

Le fichier est désormais joint à la facture achat.

## <a name="to-view-an-attached-file" />Pour afficher un fichier joint

1. Dans le volet **Récapitulatif**, ouvrez l’onglet **Pièces jointes**.
2. Choisissez la valeur associée au champ **Documents**, telle que « 1 ».
3. Sur la page **Documents joints**, sélectionnez l'action **Aperçu**.
4. Ouvrez le fichier téléchargé.

## <a name="to-save-a-document-as-a-pdf-attachment" />Pour enregistrer un document en tant que pièce jointe PDF

Chaque fois que vous devez enregistrer un document en tant que fichier, vous pouvez utiliser l'action **Joindre en tant que PDF** pour capturer le contenu actuel du document sous forme de fichier PDF joint au récapitulatif du document. Cela est utile, par exemple, lorsque des documents suivent plusieurs étapes d'un processus, comme un processus de vente ou un flux de travail approbation, et que vous souhaitez vous référer à une impression de l'étape précédente.

La procédure suivante se base sur un document de vente. Les étapes sont similaires pour tous les autres documents pris en charge.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Documents de vente**, puis sélectionnez le lien associé.
2. Sélectionnez un document de vente, puis l'action **Joindre en tant que PDF**.

Un fichier PDF avec le contenu actuel du document de vente est ajouté à l'onglet **Pièces jointes** du récapitulatif.

## <a name="to-add-a-link-from-an-item-card" />Pour ajouter un lien à partir d'une fiche article

Vous pouvez ajouter un lien à partir d’une fiche ou d’un document à n’importe quelle URL. Ceci est utile, par exemple, lorsque vous souhaitez lier une fiche article au catalogue d'articles du fournisseur.

La procédure suivante se base sur une fiche article. Les étapes sont similaires pour toutes les autres fiches et tous les documents pris en charge.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Articles**, puis choisissez le lien associé.
2. Sélectionnez l'article à partir duquel vous souhaitez ajouter un lien, puis choisissez l'onglet **Pièces jointes** dans le Récapitulatif.
3. Dans la section **Liens**, choisissez l'icône **+**.
4. Entrez le lien dans le champ **Adresse du lien**.

    Le lien doit être une URL Internet ou intranet valide.

5. Dans le champ **Description**, entrez les informations sur le lien.  
6. Choisissez le bouton **OK**.

Le lien est maintenant attaché à la fiche article.  

## <a name="to-write-a-note-on-a-sales-order" />Pour écrire une note sur un document de vente

Vous pouvez écrire une note sur un document ou une ficher, par exemple pour communiquer des instructions spéciales aux autres utilisateurs du document ou de la fiche. Vous pouvez inclure des liens et des URL de fichier dans les notes.

> [!NOTE]
> Les notes sur l'onglet **Pièces jointes** ne sont pas liées à la fonctionnalité de notes internes, qui est principalement utilisée pour communiquer entre les utilisateurs de workflows. Pour plus d'informations, reportez-vous à [Configuration de notifications de flux de travail](across-setting-up-workflow-notifications.md).

La procédure suivante se base sur un document de vente. Les étapes sont similaires pour tous les autres documents et fiches pris en charge.

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Documents de vente**, puis sélectionnez le lien associé.
2. Sélectionnez le document de vente pour lequel vous souhaitez écrire une note, puis choisissez l'onglet **Pièces jointes** dans le Récapitulatif.
3. Dans la section **Notes**, choisissez l'icône **+**.
4. Dans le champ **Note**, écrivez n’importe quel texte, par exemple « Ceci est une commande urgente ».
5. Choisissez le bouton **OK**.

La note est maintenant jointe au document de vente.

## <a name="see-also" />Voir aussi
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Documents entrants](across-income-documents.md)  
[Configuration de notifications de workflow](across-setting-up-workflow-notifications.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
