---
title: Clientwarnbenachrichtigungen per E-Mail
description: Dieses Thema enthält Informationen zur Einrichtung von Regeln, die bei vordefinierten Ereignisse E-Mail-Benachrichtigungen senden.
author: tjvass
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: bf485b407d56b21621617682bab3492925f7f9a4
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693821"
---
# <a name="client-alert-notifications-by-email"></a><span data-ttu-id="64411-103">Client-Warnungsbenachrichtigungen per E-Mail</span><span class="sxs-lookup"><span data-stu-id="64411-103">Client alert notifications by email</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="64411-104">Sie können benutzerdefinierte Warnregeln definieren, die gefilterte Datenansichten überwachen und automatisch E-Mail-Benachrichtigungen senden, wenn vordefinierte Ereignisse auftreten.</span><span class="sxs-lookup"><span data-stu-id="64411-104">You can define custom alert rules that monitor filtered views of data and automatically send email notifications when predefined events occur.</span></span> <span data-ttu-id="64411-105">Die Option zum Senden von Benachrichtigungen steht für alle unterstützten Warntypen zur Verfügung und kann auch für vorhandene Warnregeln aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="64411-105">The option to send email notifications is available for all supported alert types and can also be turned on for existing alert rules.</span></span>

<span data-ttu-id="64411-106">Sie können integrierte Kontrollen verwenden, um Warnregeln zu erstellen, die die gefilterten Ansichten von Systembatchaufträgen überwachen.</span><span class="sxs-lookup"><span data-stu-id="64411-106">You can use built-in controls to create alert rules that monitor the filtered views of system batch jobs.</span></span> <span data-ttu-id="64411-107">Durch die Überwachung des Werts des Felds **Status** können Sie auch Warnregeln konfigurieren, die E-Mails senden, wenn ein Batchauftrag fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="64411-107">By monitoring the value of the **Status** field, you can also configure alert rules that send email when a batch job fails.</span></span> <span data-ttu-id="64411-108">Nachdem diese Warnregeln erstellt wurden, müssen Sie die Berichte nicht mehr auf Änderungen an Geschäftsdaten überprüfen.</span><span class="sxs-lookup"><span data-stu-id="64411-108">After these alert rules are created, you no longer have to check reports for changes to business data.</span></span> <span data-ttu-id="64411-109">Stattdessen kann der intelligente Änderungserkennungsdienst die Überwachung für Sie übernehmen.</span><span class="sxs-lookup"><span data-stu-id="64411-109">Instead, you can let the intelligent change detection service do the monitoring for you.</span></span>

<span data-ttu-id="64411-110">Clientwarnungen hängen vom E-Mail-Subsystem ab, das durch die Integration in Microsoft Office bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="64411-110">Client alerts depend on the email subsystem that is provided through integration with Microsoft Office.</span></span> <span data-ttu-id="64411-111">Es wird empfohlen, den Simple Mail Transfer Protocol (SMTP)-Anbieter zu verwenden, sodass die E-Mail-Verteilung nicht von einem lokalen Mailclient abhängt.</span><span class="sxs-lookup"><span data-stu-id="64411-111">We recommend that you use the Simple Mail Transfer Protocol (SMTP) provider, so that email distribution doesn't have to rely on a local mail client.</span></span>

<span data-ttu-id="64411-112">Um Benachrichtigungen per E-Mail zu senden, müssen Kunden integrierte E-Mail-Services konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="64411-112">To send notifications by email, customers must configure integrated email services.</span></span> <span data-ttu-id="64411-113">E-Mail-Benachrichtigungen werden an Empfänger im Auftrag der Warnungseigentümer gesendet.</span><span class="sxs-lookup"><span data-stu-id="64411-113">Email notifications are sent to recipients on behalf of alert owners.</span></span>

<span data-ttu-id="64411-114">Weitere Informationen über die Konfiguration von E-Mails finden Sie unter [E-Mail konfigurieren und senden](../organization-administration/configure-email.md).</span><span class="sxs-lookup"><span data-stu-id="64411-114">For more information about how to configure email, see [Configure and send email](../organization-administration/configure-email.md).</span></span>

<span data-ttu-id="64411-115">Das folgende Bild zeigt das Dialogfeld **Warnregel erstellen**, das jetzt die Option **E-Mail senden** enthält.</span><span class="sxs-lookup"><span data-stu-id="64411-115">The following image shows the **Create alert rule** dialog box, which now includes a **Send email** option.</span></span>

<span data-ttu-id="64411-116">[![Erstellen Sie ein Warnregeldialogfeld, bei dem die Option "E-Mail senden" auf "Ja" festgelegt ist](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span><span class="sxs-lookup"><span data-stu-id="64411-116">[![Create alert rule dialog box, where the Send email option is set to Yes](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span></span>

> [!NOTE]
> <span data-ttu-id="64411-117">Wenn die Option **E-Mail senden** auf **Ja** festgelegt wurde, werden weiter Warnbenachrichtigungen vom Aktivitätszentrum übermittelt.</span><span class="sxs-lookup"><span data-stu-id="64411-117">When the **Send email** option is set to **Yes**, alert notifications will continue to be delivered from the Action Center.</span></span>

## <a name="alert-notification-email-templates"></a><span data-ttu-id="64411-118">E-Mail-Vorlagen für Warnbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="64411-118">Alert notification email templates</span></span>

<span data-ttu-id="64411-119">Der Dienst sendet E-Mail-Benachrichtigungen, indem er vordefinierte E-Mail-Vorlagen verwendet, die die grundlegenden Details der Warnbenachrichtigung enthalten.</span><span class="sxs-lookup"><span data-stu-id="64411-119">The service sends email notifications by using predefined email templates that deliver the basic details of the alert notification.</span></span>

<span data-ttu-id="64411-120">Das folgende Bild zeigt die Warnbenachrichtigungen, wenn sie per E-Mail eingehen.</span><span class="sxs-lookup"><span data-stu-id="64411-120">The following image show the structure of the alert notifications when they are received by email.</span></span>

<span data-ttu-id="64411-121">[![Auf Vorlagen basierende Warnbenachrichtigungen für Datensatzerstellungen, Feldänderungen und Vorlagenlöschvorgänge](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span><span class="sxs-lookup"><span data-stu-id="64411-121">[![Template-based alert notifications for record creation, field changes, and template deletion](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span></span>
