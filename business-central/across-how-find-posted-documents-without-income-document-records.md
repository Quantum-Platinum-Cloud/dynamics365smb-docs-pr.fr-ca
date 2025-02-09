---
title: Rechercher des documents reportés sans document entrant
description: 'Vous pouvez rechercher des écritures pour des documents achat et vente reportés qui n’ont pas de documents électroniques entrants, tels que les factures importées.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: edupont
---
# <a name="find-posted-documents-without-incoming-document-records" />Rechercher des enregistrements reportés sans enregistrements document entrant

Depuis les pages **Plan comptable** et **Écritures**, vous pouvez utiliser la fonction de recherche pour rechercher les écritures pour des documents achat et vente reportés qui n’ont pas d’enregistrements document entrant, puis les lier de façon centralisée à des enregistrements existants ou en créer de nouveaux avec des fichiers joints.

## <a name="to-find-posted-documents-without-incoming-document-records" />Rechercher des enregistrements reportés sans enregistrements document entrant

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Plan comptable**, puis choisissez le lien associé.
2. Sélectionnez une ligne pour un compte général pour les écritures comptables duquel vous souhaitez voir les documents ventes et achats validés sans enregistrement document entrant, puis sélectionnez l'action **Documents validés sans document entrant**.
3. Sinon, sélectionnez l'action **Écritures comptables**.
4. Sur la page **Écritures**, sélectionnez l'action **Documents reportés sans documents entrants**.

La page **Documents reportés sans document entrant** s'ouvre et affiche des documents achat et vente reportés sans enregistrement document entrant représentés par des écritures sur le compte GL pour lequel vous avez ouvert la page. Au maximum, la page affiche 1 000 lignes. Par défaut, le champ **Filtre date** contient donc un filtre qui limite l'affichage des lignes à celles dont les écritures ont une date comptabilisation comprise entre le début de la période comptable et la date de travail.

## <a name="to-connect-found-documents-to-existing-incoming-document-records" />Lier des documents recherchés à des enregistrements document entrant existants

1. Sur la page **Documents reportés sans document entrant**, sélectionnez la ligne d'un document reporté que vous souhaitez lier à un enregistrement document entrant existant, puis sélectionnez l'action **Sélectionner le document entrant**.
2. Sur la page **Documents entrants**, sélectionnez l'enregistrement document entrant que vous souhaitez lier au document reporté trouvé, puis sélectionnez le bouton **OK**.
3. Sur la page **Documents reportés sans document entrant**, l'enregistrement document entrant sélectionné est désormais lié au document reporté, comme vous pouvez le constater dans le récapitulatif **Fichiers du document entrant**.

Si un enregistrement document entrant approprié n’existe pas sur la page **Documents entrants**, vous pouvez le créer. Pour plus d'informations, voir [Créer des enregistrements document entrant](across-how-create-income-document-records.md).

## <a name="see-related-microsoft-trainingtrainingmodulesincoming-documents-dynamics-365-business-central" />Voir la [formation Microsoft](/training/modules/incoming-documents-dynamics-365-business-central/) associée

## <a name="see-also" />Voir aussi .

[Créer des enregistrements document entrant](across-how-create-income-document-records.md)
[Utiliser un service OCR pour convertir des fichiers PDF et image en documents électroniques](across-how-use-ocr-pdf-images-files.md)
[Créer des enregistrements document entrant directement à partir de documents et d’écritures](across-how-connect-disconnect-income-document-records.md)
[Documents entrants](across-income-documents.md)  
[Procédure d'achat](purchasing-manage-purchasing.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
