---
title: Ein E-Mail-Benachrichtigungsprofil einrichten
description: In diesem Thema wird beschrieben, wie Sie ein E-Mail-Benachrichtigungsprofil in Microsoft Dynamics 365 Commerce erstellen.
author: samjarawan
manager: annbe
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: c0ab56c15a37313d0a88b1174d5bcf51d391dcec
ms.sourcegitcommit: 17ffdcbf4b1801bd6ee9c9ddc18622d5d04b8a98
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3180194"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="61eb6-103">Ein E-Mail-Benachrichtigungsprofil einrichten</span><span class="sxs-lookup"><span data-stu-id="61eb6-103">Set up an email notification profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="61eb6-104">In diesem Thema wird beschrieben, wie Sie ein E-Mail-Benachrichtigungsprofil in Microsoft Dynamics 365 Commerce erstellen.</span><span class="sxs-lookup"><span data-stu-id="61eb6-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="61eb6-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="61eb6-105">Overview</span></span>

<span data-ttu-id="61eb6-106">Bevor Sie Kanäle erstellen, sollten Sie ein Profil einrichten, um sicherzustellen, dass E-Mail-Benachrichtigungen für verschiedene Ereignisse gesendet werden können, z. B. Auftragserstellung, Auftragsversandstatus und Zahlungsfehler.</span><span class="sxs-lookup"><span data-stu-id="61eb6-106">Before creating channels, you'll want to set up a profile to ensure that email notifications can be sent out for various events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="61eb6-107">Weitere Informationen über die Konfiguration von E-Mails finden Sie unter [E-Mail konfigurieren und senden](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="61eb6-107">For additional email configuration information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="61eb6-108">Ein E-Mail-Benachrichtigungsprofil erstellen</span><span class="sxs-lookup"><span data-stu-id="61eb6-108">Create an email notification profile</span></span>

<span data-ttu-id="61eb6-109">Gehen Sie folgendermaßen vor, um ein E-Mail-Benachrichtigungsprofil zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="61eb6-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="61eb6-110">Gehen Sie im Navigationsbereich zu **Module \> Retail and Commerce \> Headquarters-Einrichtung \> Commerce-E-Mail-Benachrichtigungsprofil**.</span><span class="sxs-lookup"><span data-stu-id="61eb6-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="61eb6-111">Klicken Sie im Aktivitätsbereich auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="61eb6-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="61eb6-112">Geben Sie im Feld **E-Mail-Benachrichtigungsprofil** einen Namen ein, um das Profil zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="61eb6-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="61eb6-113">Geben Sie im Feld **Beschreibung** eine entsprechende Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="61eb6-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="61eb6-114">Stellen Sie den Hebel **Aktiv** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="61eb6-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="61eb6-115">E-Mail-Vorlage erstellen</span><span class="sxs-lookup"><span data-stu-id="61eb6-115">Create an email template</span></span>

<span data-ttu-id="61eb6-116">Bevor eine E-Mail-Benachrichtigung erstellt werden kann, müssen Sie eine Organisations-E-Mail-Vorlage erstellen, die die E-Mail-Informationen des Absenders und die E-Mail-Vorlage enthält.</span><span class="sxs-lookup"><span data-stu-id="61eb6-116">Before an email notification can be created, you must create an organization email template which contains the senders email information and the email template.</span></span>

<span data-ttu-id="61eb6-117">Führen Sie folgende Schritte aus, um eine E-Mail-Vorlage zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="61eb6-117">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="61eb6-118">Gehen Sie im Navigationsbereich zu **Module \> Retail und Commerce \> Zentralverwaltungseinrichtung \> Parameter \> Organisations-E-Mail-Vorlagen**.</span><span class="sxs-lookup"><span data-stu-id="61eb6-118">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="61eb6-119">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="61eb6-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="61eb6-120">Geben Sie im Feld **E-Mail-Kennung** eine Kennung ein, um diese Vorlage zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="61eb6-120">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="61eb6-121">Geben Sie im Feld **Absendername** den Namen des Absenders ein.</span><span class="sxs-lookup"><span data-stu-id="61eb6-121">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="61eb6-122">Geben Sie im Feld **E-Mail-Beschreibung** eine aussagekräftige Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="61eb6-122">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="61eb6-123">Geben Sie im Feld **E-Mail des Absenders** die E-Mail-Adresse des Absenders ein.</span><span class="sxs-lookup"><span data-stu-id="61eb6-123">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="61eb6-124">Füllen Sie im Abschnitt **Allgemeines** die optionalen Informationen aus, die Sie benötigen (z. B. die E-Mail-Priorität).</span><span class="sxs-lookup"><span data-stu-id="61eb6-124">In the **General** section, fill out any optional information needed (such as the email priority).</span></span>
1. <span data-ttu-id="61eb6-125">Erweitern Sie die Abschnitt **Inhalt der E-Mail-Nachricht** und wählen Sie **Neu**, um den Vorlageninhalt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="61eb6-125">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="61eb6-126">Wählen Sie für jedes Inhaltselement die Sprache aus und geben Sie den Betreff der E-Mail an.</span><span class="sxs-lookup"><span data-stu-id="61eb6-126">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="61eb6-127">Wenn die E-Mail einen Textkörper haben soll, stellen Sie sicher, dass das Kästchen **Hat Text** markiert ist.</span><span class="sxs-lookup"><span data-stu-id="61eb6-127">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="61eb6-128">Wählen Sie im Aktionsbereich **E-Mail-Nachricht**, um eine E-Mail-Textvorlage bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="61eb6-128">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="61eb6-129">Das folgende Bild zeigt einige Beispieleinstellungen für E-Mail-Vorlagen.</span><span class="sxs-lookup"><span data-stu-id="61eb6-129">The following image shows some example email template settings.</span></span>

![E-Mail-Vorlageneinstellungen](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="61eb6-131">E-Mail-Ereignis erstellen</span><span class="sxs-lookup"><span data-stu-id="61eb6-131">Create an email event</span></span>

<span data-ttu-id="61eb6-132">Führen Sie folgende Schritte aus, um eine E-Mail-Ereignis zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="61eb6-132">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="61eb6-133">Gehen Sie im Navigationsbereich zu **Module \> Retail and Commerce \> Headquarters-Einrichtung \> Commerce-E-Mail-Benachrichtigungsprofil**.</span><span class="sxs-lookup"><span data-stu-id="61eb6-133">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="61eb6-134">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="61eb6-134">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="61eb6-135">Wählen Sie die E-Mail-Vorlage aus der Dropdownliste **E-Mail-Kennung**.</span><span class="sxs-lookup"><span data-stu-id="61eb6-135">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="61eb6-136">Wählen Sie aus der Dropdownliste den entsprechenden **E-Mail-Kennungstyp**.</span><span class="sxs-lookup"><span data-stu-id="61eb6-136">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="61eb6-137">Aktivieren Sie das Kontrollkästchen **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="61eb6-137">Select the **Active** check box.</span></span>
1. <span data-ttu-id="61eb6-138">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="61eb6-138">On the action pane, select **Save**.</span></span>

<span data-ttu-id="61eb6-139">Das folgende Bild zeigt einige Beispiele für die Einstellungen der Ereignisbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="61eb6-139">The following image shows some example event notification settings.</span></span>

![Einstellungen für die Ereignisbenachrichtigung](media/email-notification-profile.png)

### <a name="next-steps"></a><span data-ttu-id="61eb6-141">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="61eb6-141">Next steps</span></span>

<span data-ttu-id="61eb6-142">Bevor Sie E-Mails senden können, müssen Sie Ihren Postausgangsdienst konfigurieren und einen Batchauftrag einrichten.</span><span class="sxs-lookup"><span data-stu-id="61eb6-142">Before you can send mails, you must configure your outgoing mail service and set up a batch job.</span></span> <span data-ttu-id="61eb6-143">Weitere Informationen finden Sie unter [E-Mail konfigurieren und senden](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="61eb6-143">For more information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="61eb6-144">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="61eb6-144">Additional resources</span></span>

[<span data-ttu-id="61eb6-145">E-Mails konfigurieren und senden</span><span class="sxs-lookup"><span data-stu-id="61eb6-145">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="61eb6-146">Kanäle – Übersicht</span><span class="sxs-lookup"><span data-stu-id="61eb6-146">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="61eb6-147">Kanaleinstellungen – Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="61eb6-147">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="61eb6-148">Organisationen und Organisationshierarchien – Übersicht</span><span class="sxs-lookup"><span data-stu-id="61eb6-148">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
