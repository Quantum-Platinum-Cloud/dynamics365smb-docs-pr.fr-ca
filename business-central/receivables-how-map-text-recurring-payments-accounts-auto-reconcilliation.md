---
title: Paramétrage de la mise en correspondance du texte avec le compte pour les paiements récurrents
description: 'Lier le texte sur les paiements à des comptes spécifiques, afin que les paiements soient reportés dans les comptes lorsque vous reportez le journal rapprochement bancaire.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'account linking, direct payment posting, automatic payment processing, reconcile payment, recurring expense, recurring cash receipt'
ms.search.form: '1290, 1294, 1287'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation" />Mapper du texte sur les paiements récurrents aux comptes pour un rapprochement automatique

Sur la page **Correspondance texte et compte** à laquelle vous accédez à partir de la page **Journal rapprochement paiement**, vous pouvez configurer des mappages entre le texte des paiements et des comptes de débit, de crédit et de contrepartie spécifiques afin que ces paiements soient reportés dans les comptes spécifiés lorsque vous reportez le journal rapprochement de paiement.

Une fonctionnalité similaire existe pour rapprocher les montants excédentaires sur les lignes journal rapprochement paiement de façon ponctuelle. Pour plus d'informations, voir [Rapprocher les paiements qui ne peuvent pas être affectés automatiquement](receivables-how-reconcile-payments-cannot-apply-auto.md).

Les paiements reportés basés sur le mappage de texte à compte ne sont pas affectés aux écritures ouvertes, mais sont simplement reportés dans les comptes spécifiés en plus de créer des écritures de compte bancaire. Par conséquent, le mappage de texte à compte est approprié pour les recettes ou dépenses récurrentes en liquide, notamment les achats fréquents de carburant pour les voitures ou les frais et intérêts bancaires, qui apparaissent régulièrement sur le relevé bancaire et n'ont pas besoin d'un document d'entreprise lié. Pour en savoir plus, voir « Exemple – Mappage de texte à compte pour les frais de carburant » dans cette rubrique.

> [!NOTE]  
>   Les paiements sur les lignes de feuille de rapprochement ne sont définies sur validation en fonction du mappage de texte à compte que si la fonction d'application automatique peut fournir une confiance une correspondance **Faible** ou **Moyenne**. Si la fonction d'affectation automatique fournit un taux de fiabilité correspondance Élevé, alors le paiement est automatiquement affecté à une ou plusieurs écritures ouvertes, et le paiement n'est pas reporté sur les comptes spécifiés sur la page **Correspondance texte et compte**. En d'autres termes, une confiance de correspondance **Élevée** outrepasse un mappage de texte à compte.

Sur une ligne journal rapprochement paiement dont le paiement a été défini sur report en fonction du mappage de texte à compte, le champ **Fiabilité correspondance** contient la valeur **Élevé – Mappage de texte à compte**, et les champs **Type compte** et **N° compte** contiennent les comptes mappés.

## <a name="to-map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation" />Pour associer le texte sur les paiements récurrents aux comptes pour un rapprochement automatique

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Journaux rapprochement bancaire**, puis sélectionnez le lien associé.
2. Ouvrez un journal rapprochement paiement. Pour plus d'informations, reportez-vous à [Rapprocher les paiements à l'aide du lettrage automatique](receivables-how-reconcile-payments-auto-application.md).
3. Sélectionnez l'action **Mapper le texte avec le compte**. La page **Correspondance texte et compte** s'affiche.
4. Dans le champ **Correspondance texte**, saisissez n'importe quel texte se produisant sur les paiements que vous souhaitez valider dans les comptes spécifiés sans les appliquer à une écriture ouverte. Vous pouvez entrer jusqu'à 50 caractères.

    > [!NOTE]  
    >   Si aucun autre paiement n'existe avec le texte de mappage en question, le mappage du texte avec le compte surviendra uniquement lorsqu'une seule partie du texte de paiement existe en tant que texte de mappage.
5. Dans le champ **N° fournisseur**, entrez le fournisseur pour lequel les paiements seront reportés.
6. Dans le champ **Type origine solde**, indiquez si le paiement est validé dans un compte général ou dans un compte client ou fournisseur.
7. Dans le champ **N° origine solde**, indiquez le compte dans lequel le paiement est reporté, en fonction de votre sélection dans le champ **Type origine solde**.

    > [!NOTE]
    > N'utilisez pas les champs **N° cpte débit** et **N° cpte crédit** en relation avec le rapprochement bancaire. Ils sont utilisés pour les documents entrants uniquement. Pour en savoir plus, voir [Utiliser un service OCR pour convertir des fichiers PDF et image en documents électroniques](across-how-use-ocr-pdf-images-files.md).

8. Répétez les étapes 3 à 7 pour tout le texte sur les paiements que vous souhaitez mapper à des comptes pour un report direct sans affectation.

La prochaine fois que vous importez un fichier de relevé bancaire ou sélectionnez l'action **Affecter automatiquement** sur la page **Journal rapprochement paiement**, les lignes journal pour les paiements qui contiennent le texte de mappage spécifié contiendront les comptes mappés dans les champs **Type compte** et **N° compte**. Le champ **Fiabilité correspondance** contient **Élevée - Correspondance texte et compte**. Ce, à condition que la fonction de lettrage automatique ne puisse fournir qu'une fiabilité de correspondance **Basse** ou **Moyenne**.

## <a name="example-text-to-account-mapping-for-bank-fees" />Exemple : Mappage de texte à compte pour les frais bancaires

Pour toujours reporter les dépenses liées aux frais d’une banque spécifique, MyBank, sur le compte GL pour les frais et frais bancaires (compte 60400), remplissez une ligne sur la page **Mappage de texte à compte** comme suit.

| Correspondance texte | N° cpte débit | N° cpte crédit | Type origine solde | N° origine solde |
| --- | --- | --- | --- | --- |
| MyBank |VIDE |60400|Compte général |VIDE |

## <a name="see-related-microsoft-trainingtrainingmodulesuse-journals-dynamics-365-business-central" />Voir la [formation Microsoft](/training/modules/use-journals-dynamics-365-business-central/) associée

## <a name="see-also" />Voir aussi .

[Gestion des comptes client](receivables-manage-receivables.md)  
[Ventes](sales-manage-sales.md)  
[Configurer le service Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Personnalisation de [!INCLUDE[prod_short](includes/prod_short.md)] à l'aide des extensions](ui-extensions.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
