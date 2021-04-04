---
title: Ein E-Mail-Benachrichtigungsprofil einrichten
description: In diesem Thema wird beschrieben, wie Sie ein E-Mail-Benachrichtigungsprofil in Microsoft Dynamics 365 Commerce erstellen.
author: bicyclingfool
manager: annbe
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: d82a1abe68ff6e162acb75c6fdc1e207af11c279
ms.sourcegitcommit: 88babb2fffe97e93bbde543633fc492120f2a4fc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "5555306"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="619c2-103">E-Mail-Benachrichtigungsprofil einrichten</span><span class="sxs-lookup"><span data-stu-id="619c2-103">Set up an email notification profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="619c2-104">In diesem Thema wird beschrieben, wie Sie ein E-Mail-Benachrichtigungsprofil in Microsoft Dynamics 365 Commerce erstellen.</span><span class="sxs-lookup"><span data-stu-id="619c2-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="619c2-105">Wenn Sie Kanäle erstellen, können Sie ein E-Mail-Benachrichtigungsprofil einrichten.</span><span class="sxs-lookup"><span data-stu-id="619c2-105">When you create channels, you can set up an email notification profile.</span></span> <span data-ttu-id="619c2-106">Auf diese Weise können E-Mails an Kunden für verschiedene Transaktionsereignisse gesendet werden, z. B. für die Auftragserstellung, den Versandstatus der Bestellung und Zahlungsfehler.</span><span class="sxs-lookup"><span data-stu-id="619c2-106">In that way, emails can be sent to customers for various transactional events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="619c2-107">Weitere Informationen über die Konfiguration von E-Mails finden Sie unter [E-Mail konfigurieren und senden](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="619c2-107">For additional email configuration information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="619c2-108">Ein E-Mail-Benachrichtigungsprofil erstellen</span><span class="sxs-lookup"><span data-stu-id="619c2-108">Create an email notification profile</span></span>

<span data-ttu-id="619c2-109">Gehen Sie folgendermaßen vor, um ein E-Mail-Benachrichtigungsprofil zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="619c2-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="619c2-110">Gehen Sie im Navigationsbereich zu **Module \> Retail and Commerce \> Headquarters-Einrichtung \> Commerce-E-Mail-Benachrichtigungsprofil**.</span><span class="sxs-lookup"><span data-stu-id="619c2-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="619c2-111">Klicken Sie im Aktivitätsbereich auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="619c2-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="619c2-112">Geben Sie im Feld **E-Mail-Benachrichtigungsprofil** einen Namen ein, um das Profil zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="619c2-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="619c2-113">Geben Sie im Feld **Beschreibung** eine entsprechende Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="619c2-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="619c2-114">Stellen Sie den Hebel **Aktiv** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="619c2-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="619c2-115">E-Mail-Vorlage erstellen</span><span class="sxs-lookup"><span data-stu-id="619c2-115">Create an email template</span></span>

<span data-ttu-id="619c2-116">Bevor ein E-Mail-Benachrichtigungstyp aktiviert werden kann, müssen Sie eine E-Mail-Vorlage für die Organisation in der Commerce-Zentrale erstellen.</span><span class="sxs-lookup"><span data-stu-id="619c2-116">Before an email notification type can be enabled, you must create an organization email template in Commerce headquarters.</span></span> <span data-ttu-id="619c2-117">Diese Vorlage definiert den E-Mail-Betreff, den Absender, die Standardsprache und den E-Mail-Text für jede Sprache, die Sie unterstützen möchten.</span><span class="sxs-lookup"><span data-stu-id="619c2-117">This template defines the email subject, sender, default language, and email body for each language that you want to support.</span></span>

<span data-ttu-id="619c2-118">Führen Sie folgende Schritte aus, um eine E-Mail-Vorlage zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="619c2-118">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="619c2-119">Gehen Sie im Navigationsbereich zu **Module \> Einzelhandel und Handel \> Zentralverwaltungseinrichtung \> Parameter \> Organisations-E-Mail-Vorlagen**.</span><span class="sxs-lookup"><span data-stu-id="619c2-119">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="619c2-120">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="619c2-120">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="619c2-121">Geben Sie im Feld **E-Mail-Kennung** eine Kennung ein, um diese Vorlage zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="619c2-121">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="619c2-122">Geben Sie im Feld **Absendername** den Namen des Absenders ein.</span><span class="sxs-lookup"><span data-stu-id="619c2-122">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="619c2-123">Geben Sie im Feld **E-Mail-Beschreibung** eine aussagekräftige Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="619c2-123">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="619c2-124">Geben Sie im Feld **E-Mail des Absenders** die E-Mail-Adresse des Absenders ein.</span><span class="sxs-lookup"><span data-stu-id="619c2-124">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="619c2-125">Wählen Sie im Abschnitt **Allgemein** eine Standardsprache für die E-Mail-Vorlage aus.</span><span class="sxs-lookup"><span data-stu-id="619c2-125">In the **General** section, select a default language for the email template.</span></span> <span data-ttu-id="619c2-126">Die Standardsprache wird verwendet, wenn für die angegebene Sprache keine lokalisierte Vorlage vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="619c2-126">The default language will be used when no localized template exists for the specified language.</span></span>
1. <span data-ttu-id="619c2-127">Erweitern Sie die Abschnitt **Inhalt der E-Mail-Nachricht** und wählen Sie **Neu**, um den Vorlageninhalt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="619c2-127">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="619c2-128">Wählen Sie für jedes Inhaltselement die Sprache aus und geben Sie den Betreff der E-Mail an.</span><span class="sxs-lookup"><span data-stu-id="619c2-128">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="619c2-129">Wenn die E-Mail einen Textkörper haben soll, stellen Sie sicher, dass das Kästchen **Hat Text** markiert ist.</span><span class="sxs-lookup"><span data-stu-id="619c2-129">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="619c2-130">Wählen Sie im Aktionsbereich **E-Mail-Nachricht**, um eine E-Mail-Textvorlage bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="619c2-130">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="619c2-131">Das folgende Bild zeigt einige Beispieleinstellungen für E-Mail-Vorlagen.</span><span class="sxs-lookup"><span data-stu-id="619c2-131">The following image shows some example email template settings.</span></span>

![E-Mail-Vorlageneinstellungen](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="619c2-133">E-Mail-Ereignis erstellen</span><span class="sxs-lookup"><span data-stu-id="619c2-133">Create an email event</span></span>

<span data-ttu-id="619c2-134">Führen Sie folgende Schritte aus, um eine E-Mail-Ereignis zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="619c2-134">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="619c2-135">Gehen Sie im Navigationsbereich zu **Module \> Retail and Commerce \> Headquarters-Einrichtung \> Commerce-E-Mail-Benachrichtigungsprofil**.</span><span class="sxs-lookup"><span data-stu-id="619c2-135">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="619c2-136">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="619c2-136">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="619c2-137">Wählen Sie die E-Mail-Vorlage aus der Dropdownliste **E-Mail-Kennung**.</span><span class="sxs-lookup"><span data-stu-id="619c2-137">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="619c2-138">Wählen Sie aus der Dropdownliste den entsprechenden **E-Mail-Kennungstyp**.</span><span class="sxs-lookup"><span data-stu-id="619c2-138">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="619c2-139">Aktivieren Sie das Kontrollkästchen **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="619c2-139">Select the **Active** check box.</span></span>
1. <span data-ttu-id="619c2-140">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="619c2-140">On the action pane, select **Save**.</span></span>

<span data-ttu-id="619c2-141">Das folgende Bild zeigt einige Beispiele für die Einstellungen der Ereignisbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="619c2-141">The following image shows some example event notification settings.</span></span>

![Einstellungen für die Ereignisbenachrichtigung](media/email-notification-profile.png)

### <a name="next-steps"></a><span data-ttu-id="619c2-143">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="619c2-143">Next steps</span></span>

<span data-ttu-id="619c2-144">Bevor Sie E-Mails senden können, müssen Sie Ihren Postausgangsdienst konfigurieren und einen Batchauftrag einrichten.</span><span class="sxs-lookup"><span data-stu-id="619c2-144">Before you can send mails, you must configure your outgoing mail service and set up a batch job.</span></span> <span data-ttu-id="619c2-145">Weitere Informationen finden Sie unter [E-Mail konfigurieren und senden](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="619c2-145">For more information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="619c2-146">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="619c2-146">Additional resources</span></span>

[<span data-ttu-id="619c2-147">E-Mails konfigurieren und senden</span><span class="sxs-lookup"><span data-stu-id="619c2-147">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="619c2-148">Kanäle – Übersicht</span><span class="sxs-lookup"><span data-stu-id="619c2-148">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="619c2-149">Kanaleinstellungen – Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="619c2-149">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="619c2-150">Organisationen und Organisationshierarchien – Übersicht</span><span class="sxs-lookup"><span data-stu-id="619c2-150">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
