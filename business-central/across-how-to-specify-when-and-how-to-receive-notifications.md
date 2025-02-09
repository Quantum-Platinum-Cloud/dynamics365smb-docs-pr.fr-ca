---
title: Spécifier quand et comment recevoir des notifications de workflow
description: 'Lorsque vous configurez des utilisateurs dans des flux de travails d’approbation, vous pouvez spécifier comment et quand chaque utilisateur d’approbation reçoit des notifications.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '663, 1500, 1512, 1513,'
ms.date: 09/09/2022
ms.author: bholtorf
---
# <a name="specify-when-and-how-to-receive-workflow-notifications" />Spécifier quand et comment recevoir des notifications de workflow

Lorsque vous configurez des utilisateurs d’approbation dans des flux de travail où vous souhaitez que quelqu’un approuve les modifications, par exemple lorsque des enregistrements sont créés ou lorsque quelqu’un demande une approbation, vous devez spécifier comment et quand avertir l’utilisateur d’approbation. Par exemple, vous pouvez spécifier qu’un utilisateur d’approbation recevra immédiatement un courriel lorsque quelqu’un créera un client. Sinon, vous pouvez programmer les notifications à envoyer, par exemple, sur une base hebdomadaire ou mensuelle.

Les personnes peuvent également modifier leur configuration de notification en choisissant **Changer les paramètres de notification** sur toute notification.  

> [!NOTE]
> Les notifications sont envoyées en fonction des paramètres de notification pour le destinataire, et non l’expéditeur. Cette distinction est importante, car cela signifie que lorsqu’un utilisateur demande une approbation dans le cadre d’un flux de travail, sa demande n’est pas nécessairement envoyée immédiatement. Au lieu de cela, elle sera remise selon le calendrier de notification spécifié dans les paramètres de notification de l’approbateur.

Avant de pouvoir paramétrer des préférences de notification d’un utilisateur approbation, vous devez configurer l’utilisateur en tant qu’utilisateur d'approbation. En savoir plus sur [Configurer des utilisateurs d’approbation](across-how-to-set-up-approval-users.md).  

> [!NOTE]
> Si vous souhaitez utiliser le courriel comme méthode de notification, vous devez configurer l’adresse de courriel de l’expéditeur et du destinataire dans [!INCLUDE [prod_short](includes/prod_short.md)]. Pour en savoir plus, voir [Configurer les courriels](admin-how-setup-email.md).

## <a name="steps-in-workflows" />Étapes de flux de travail

Pour un grand nombre d’étapes d’approbation du flux de travail, il s’agit de notifier des utilisateurs qu’un événement s’est produit et qu’ils peuvent agir dessus. Par exemple, sur une étape de workflow, l'événement peut être que l'Utilisateur 1 demande l'approbation d'un nouvel enregistrement. La réponse associée est qu'une notification est envoyée à l'Utilisateur 2, l'approbateur. Sur la prochaine étape de workflow, l'événement peut être que l'Utilisateur 2 approuve l'enregistrement. La réponse associée est qu'une notification est envoyée à l'Utilisateur 3 afin de commencer un processus avec l'enregistrement approuvé. Pour les étapes de flux de travail concernant des approbations, chaque notification est liée à une écriture d’approbation. En savoir plus sur [Flux de travail](across-workflow.md).  

## <a name="specify-when-and-how-approval-users-receive-notifications" />Spécifier quand et comment les utilisateurs d’approbation reçoivent des notifications

1. Sélectionnez l’icône ![Ampoule qui ouvre la fonction Tell Me.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Configuration d'utilisateur d'approbation**, puis choisissez le lien associé.  
2. Sélectionnez la ligne de l’utilisateur pour lequel vous souhaitez paramétrer des préférences de notification, puis choisissez l’action **Configuration de la notification**.  
3. Sur la page **Configuration des notifications de workflow**, renseignez les champs comme indiqué dans le tableau suivant.  

   > [!NOTE]
   > Si vous ouvrez la page **Configuration des notifications de workflow** à partir de la page **Configuration de l'utilisateur d’approbation**, la configuration des notifications est liée à l’utilisateur d’approbation. L’utilisateur d’approbation recevra toujours des notifications de workflow en fonction de cette configuration de notification. Si vous utilisez la fonctionnalité *Tell Me* pour ouvrir la page **Configuration des notifications de workflow**, la configuration des notifications s’appliquera à tous les utilisateurs.

   |Champ|Désignation|
   |-----|-----------|
   |**Type de notification**|Spécifiez le type d’événement dont il s’agit dans la notification.<br /><br /> Sélectionnez l'une des options suivantes :<br /><br /> -   **Nouvel enregistrement** spécifie que la notification concerne un nouvel enregistrement, par exemple un document sur lequel l'utilisateur doit agir.<br />-   **Approbation** spécifie que la notification concerne une ou plusieurs demandes d'approbation.<br />-   **Échu** spécifie que l’objet de la notification est de rappeler aux utilisateurs qu’ils sont en retard pour agir sur un événement.|
   |**Mode de notification**|Spécifiez si la notification est un courriel ou une note interne.|

   Vous pouvez définir la présentation des courriels de notification en personnalisant le rapport 1320, notification par courriel. En savoir plus sur [Créer et modifier des présentations de rapport personnalisées](ui-how-create-custom-report-layout.md).

   À présent, vous avez spécifié la manière dont l’utilisateur reçoit des notifications. Continuez à spécifier lorsque l'utilisateur reçoit des notifications.  
4. Choisissez l'action **Calendrier de notification**.  
5. Sur la page **Calendrier de notification**, renseignez les champs comme indiqué dans le tableau suivant.  

   |Champ|Désignation|
   |-----|-----------|
   |**Répétition**|Spécifiez la périodicité à laquelle les notifications sont envoyées à l'utilisateur.|
   |**Heure**|Spécifiez à quelle heure du jour l’utilisateur reçoit les notifications lorsque la valeur du champ **Répétition** est différente de la valeur **Instantané**.|
   |**Fréquence quotidienne**|Spécifiez quel type de jours l'utilisateur reçoit des notifications lorsque la valeur dans le champ **Répétition** est **Tous les jours**.<br /><br /> Sélectionnez **Jour de la semaine** pour recevoir des notifications chaque jour ouvré de la semaine. Sélectionnez **Tous les jours** pour recevoir des notifications tous les jours, y compris le week-end.|
   |**Lundi** à **Dimanche**|Spécifiez quel type de jours l'utilisateur reçoit des notifications lorsque la valeur dans le champ **Répétition** est **Chaque semaine**.|
   |**Date du mois**|Spécifiez si l'utilisateur reçoit des notifications le premier ou le dernier jour du mois, ou à une date spécifique du mois.|
   |**Date de notification mensuelle**|Spécifiez à quelle date du mois l'utilisateur reçoit des notifications lorsque la valeur dans le champ **Date du mois** est **Personnalisé**.|

## <a name="change-when-and-how-you-receive-notifications" />Modifier le moment et le mode de réception des notifications

1. Sur l’une des notifications que vous avez reçue, par courriel ou comme note, sélectionnez le bouton **Modifier les paramètres de notification**.  
2. Sur la page **Configuration des notifications de workflow**, modifiez vos préférences de notification comme décrit dans les étapes 3 à 5 ci-dessus.
   1. Confirmez que la bonne notification est sélectionnée sous le champ **Type de notification**.
   2. Choisissez si vous souhaitez recevoir un courriel ou une note de notification sous le champ **Méthode de notification**.
   3. Sélectionnez le **Calendrier des notifications** pour modifier la fréquence et la récurrence d’envoi des notifications.

## <a name="see-also" />Voir aussi .

[Configurer des utilisateurs d'approbation](across-how-to-set-up-approval-users.md)  
[Créer et modifier des présentations de rapport personnalisées](ui-how-create-custom-report-layout.md)  
[Configuration de notifications de flux de travail approbation](across-setting-up-workflow-notifications.md)  
[Configurer les flux de travail approbation](across-set-up-workflows.md)  
[Utilisation des flux d’approbation](across-use-workflows.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
