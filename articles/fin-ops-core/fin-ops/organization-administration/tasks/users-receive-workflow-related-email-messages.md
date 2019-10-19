---
title: Ermöglichen Sie es Benutzern, workflowbezogene E-Mail-Nachrichten zu erhalten.
description: Sie können das System konfigurieren, um E-Mail-Nachrichten an Benutzer zu senden, wenn workflowbezogene Ereignisse auftreten.
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5e08f95ef6d263ee0f8c0a94b258c8a2795786bc
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189843"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="61708-103">Ermöglichen Sie es Benutzern, workflowbezogene E-Mail-Nachrichten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="61708-103">Enable users to receive workflow-related email messages</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="61708-104">Sie können das System konfigurieren, um E-Mail-Nachrichten an Benutzer zu senden, wenn workflowbezogene Ereignisse auftreten.</span><span class="sxs-lookup"><span data-stu-id="61708-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="61708-105">So können E-Mail-Nachrichten an Benutzer gesendet werden, wenn ihnen Dokumente zur Genehmigung zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="61708-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="61708-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="61708-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="61708-107">Wechseln Sie zu **Navigationsbereich > Module > Systemverwaltung > Benutzer > Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="61708-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="61708-108">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="61708-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="61708-109">Klicken Sie im **Aktionsbereich** auf **Benutzeroptionen**.</span><span class="sxs-lookup"><span data-stu-id="61708-109">On the **Action pane**, click **User options**.</span></span>
4. <span data-ttu-id="61708-110">Klicken Sie auf die Registerkarte **Workflow**. Stellen Sie sicher, dass der Abschnitt **Benachrichtigungen** erweitert ist.</span><span class="sxs-lookup"><span data-stu-id="61708-110">Click the **Workflow** tab. Make sure that the **Notifications** section is expanded.</span></span> <span data-ttu-id="61708-111">Im Abschnitt **Benachrichtigungen** können Sie festlegen, wie der Benutzer über workflowbezogene Ereignisse informiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="61708-111">In the **Notifications** section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="61708-112">Wählen Sie im Feld **Positionsartikelworkflow-Benachrichtigungstyp** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="61708-112">In the **Line-item workflow notification type** field, select an option.</span></span>
    - <span data-ttu-id="61708-113">Gruppiert – Benachrichtigungen für Positionsartikel werden in eine einzige E-Mail-Nachricht gruppiert.</span><span class="sxs-lookup"><span data-stu-id="61708-113">Grouped – Notifications for line items are grouped into a single email message.</span></span>
    - <span data-ttu-id="61708-114">Einzeln - eine E-Mail wird für jeden Positionsartikel übermittelt.</span><span class="sxs-lookup"><span data-stu-id="61708-114">Individual – An email message is sent for each line item.</span></span>  
    - <span data-ttu-id="61708-115">Wenn der Benutzer im Client Benachrichtigungen erhalten soll, aktivieren Sie das Kontrollkästchen **Benachrichtigungen in E-Mail senden**.</span><span class="sxs-lookup"><span data-stu-id="61708-115">If you want the user to receive notifications in the client, select the **Send notifications in email** check box.</span></span>  
6. <span data-ttu-id="61708-116">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="61708-116">Click **Save**.</span></span>
7. <span data-ttu-id="61708-117">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="61708-117">Close the page.</span></span>

