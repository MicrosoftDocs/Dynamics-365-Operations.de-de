--- 
title: "Ermöglichen Sie es Benutzern, workflowbezogene E-Mail-Nachrichten zu erhalten."
description: "Sie können das System konfigurieren, um E-Mail-Nachrichten an Benutzer zu senden, wenn workflowbezogene Ereignisse auftreten."
author: jasongre
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: abd59b96a2e5dceb2492c2db2c617485b332fbd3
ms.openlocfilehash: 6800d02878123388611d35760123d0215e9d539f
ms.contentlocale: de-de
ms.lasthandoff: 09/13/2018

---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="91188-103">Ermöglichen Sie es Benutzern, workflowbezogene E-Mail-Nachrichten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="91188-103">Enable users to receive workflow-related email messages</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="91188-104">Sie können das System konfigurieren, um E-Mail-Nachrichten an Benutzer zu senden, wenn workflowbezogene Ereignisse auftreten.</span><span class="sxs-lookup"><span data-stu-id="91188-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="91188-105">So können E-Mail-Nachrichten an Benutzer gesendet werden, wenn ihnen Dokumente zur Genehmigung zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="91188-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="91188-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="91188-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="91188-107">Wechseln Sie zu "Systemverwaltung" > "Benutzer" > "Benutzer".</span><span class="sxs-lookup"><span data-stu-id="91188-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="91188-108">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="91188-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="91188-109">Klicken Sie auf "Benutzeroptionen".</span><span class="sxs-lookup"><span data-stu-id="91188-109">Click User options.</span></span>
4. <span data-ttu-id="91188-110">Klicken Sie auf die Registerkarte „Workflow”.</span><span class="sxs-lookup"><span data-stu-id="91188-110">Click the Workflow tab.</span></span>
    * <span data-ttu-id="91188-111">Überprüfen Sie, ob der Bereich „Benachrichtigungen” erweitert ist.</span><span class="sxs-lookup"><span data-stu-id="91188-111">Make sure that the Notifications section is expanded.</span></span>     <span data-ttu-id="91188-112">Im Abschnitt „Benachrichtigungen” geben Sie an, wie der Benutzer über workflowbezogene Ereignisse informiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="91188-112">In the Notifications section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="91188-113">Wählen Sie im Feld Positionsartikelworkflow-Benachrichtigungstyp eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="91188-113">In the Line-item workflow notification type field, select an option.</span></span>
    * <span data-ttu-id="91188-114">Gruppiert – Benachrichtigungen für Positionsartikel werden in eine einzige E-Mail-Nachricht gruppiert.</span><span class="sxs-lookup"><span data-stu-id="91188-114">Grouped – Notifications for line items are grouped into a single email message.</span></span>    <span data-ttu-id="91188-115">Einzeln - eine E-Mail wird für jeden Positionsartikel übermittelt.</span><span class="sxs-lookup"><span data-stu-id="91188-115">Individual – An email message is sent for each line item.</span></span>  
    * <span data-ttu-id="91188-116">Wenn der Benutzer Benachrichtigungen im Microsoft -Client erhalten soll, aktivieren Sie das Kontrollkästchen „Benachrichtigungen per E-Mail senden”.</span><span class="sxs-lookup"><span data-stu-id="91188-116">If you want the user to receive notifications in the client, select the Send notifications in email check box.</span></span>  
6. <span data-ttu-id="91188-117">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="91188-117">Click Save.</span></span>
7. <span data-ttu-id="91188-118">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="91188-118">Close the page.</span></span>


