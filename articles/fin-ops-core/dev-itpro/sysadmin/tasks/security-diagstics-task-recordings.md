---
title: Sicherheitsdiagnose für Aufgabenaufzeichnungen
description: Dieses Thema enthält Informationen zum Analysieren und Verwalten von Sicherheitsberechtigungsanforderungen basierend auf einer Aufgabenaufzeichnung.
author: Peakerbl
manager: AnnBe
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.openlocfilehash: 88eb90b35f1a9754cc4daa01d8f40cdf712db4f8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679789"
---
# <a name="security-diagnostics-for-task-recordings"></a><span data-ttu-id="87364-103">Sicherheitsdiagnose für Aufgabenaufzeichnungen</span><span class="sxs-lookup"><span data-stu-id="87364-103">Security diagnostics for task recordings</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a><span data-ttu-id="87364-104">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="87364-104">Before you begin</span></span>

<span data-ttu-id="87364-105">Dieses Thema enthält Informationen zum Analysieren und Verwalten von Sicherheitsberechtigungsanforderungen basierend auf einer Aufgabenaufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="87364-105">This topic provides information about how to analyze and manage security permission requirements based on a task recording.</span></span> <span data-ttu-id="87364-106">Bevor Sie die Schritte in diesem Thema ausführen, müssen Sie über eine Aufgabenaufzeichnung des Geschäftsprozesses verfügen, den Sie analysieren möchten.</span><span class="sxs-lookup"><span data-stu-id="87364-106">Before you complete the steps in this topic, you must have a task recording of the business process that you want to analyze.</span></span> <span data-ttu-id="87364-107">Informationen zum Aufzeichnen eines Geschäftsprozesses finden Sie unter [Aufgabenaufzeichnungsressourcen](../../user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="87364-107">To record a business process, see [Task recorder resources](../../user-interface/task-recorder.md).</span></span> 

## <a name="manage-security-for-a-task-recording"></a><span data-ttu-id="87364-108">Sicherheit für eine Aufgabenaufzeichnung verwalten</span><span class="sxs-lookup"><span data-stu-id="87364-108">Manage security for a task recording</span></span>

1. <span data-ttu-id="87364-109">Wechseln Sie zu **Systemadministration** > **Sicherheit** > **Sicherheitsdiagnose für die Aufgabenaufzeichnung**.</span><span class="sxs-lookup"><span data-stu-id="87364-109">Go to **System administration** > **Security** > **Security diagnostic for task recording**.</span></span>
2. <span data-ttu-id="87364-110">Öffnen Sie die Aufgabenaufzeichnung von ihrem Standort aus.</span><span class="sxs-lookup"><span data-stu-id="87364-110">Open the task recording from its location.</span></span> <span data-ttu-id="87364-111">Wählen Sie **Von diesem PC aus öffnen** oder **Von Lifecycle Services aus öffnen** aus, und wählen Sie dann **Schließen** aus.</span><span class="sxs-lookup"><span data-stu-id="87364-111">Select **Open from this PC** or **Open from Lifecycle Services**, and then select **Close**.</span></span>
3. <span data-ttu-id="87364-112">Dies öffnet die Seite **Sicherheitsmenüelement-Details**, auf der die für den Prozess erforderlichen Sicherheitsobjekte aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="87364-112">This will open the **Security menu item details** page that lists the security objects required for the process.</span></span>

 > [!NOTE]
 > <span data-ttu-id="87364-113">Die Menüelemente **Aktivität** und **Ausgabe** sind nicht in der Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="87364-113">The **Action** and **Output** menu items are not included in the list.</span></span>

4. <span data-ttu-id="87364-114">Im Feld **Benutzer-ID** wählen Sie einen Benutzer aus.</span><span class="sxs-lookup"><span data-stu-id="87364-114">In the **User ID** field, select a user.</span></span> <span data-ttu-id="87364-115">Wenn der Benutzer für einige Menüelemente keine Berechtigungen hat, wird das Feld **Fehlende Berechtigungen** auf **Ja** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="87364-115">If the user does not have permissions for some menu items, the **Missing permissions** field will update to **Yes**.</span></span>
  
  ![Seite „Sicherheitsmenüelement-Details“](../media/Security-Menu-Item-Details.png)

5. <span data-ttu-id="87364-117">Wählen Sie **Referenz hinzufügen**, um eine Liste der Sicherheitsobjekte anzuzeigen, einschließlich Rollen, Aufgaben und Berechtigungen, die die fehlende Berechtigung erteilen.</span><span class="sxs-lookup"><span data-stu-id="87364-117">Select **Add Reference** to see a list of the security objects, including roles, duties, and privileges that grant the missing permission.</span></span>
6. <span data-ttu-id="87364-118">Wählen Sie ein Sicherheitsobjekt aus der Liste aus:</span><span class="sxs-lookup"><span data-stu-id="87364-118">Select a security object from the list:</span></span>

    - <span data-ttu-id="87364-119">Wenn **Rolle** ausgewählt ist, wählen Sie **Dem Benutzer Rolle hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="87364-119">If **Role** is selected, select **Add role to user**.</span></span> <span data-ttu-id="87364-120">Dies öffnet die Seite **Benutzer zu Rollen zuweisen**.</span><span class="sxs-lookup"><span data-stu-id="87364-120">This will open the **Assign users to roles** page.</span></span> <span data-ttu-id="87364-121">Ausführlichere Informationen finden Sie auf der Seite [Zuweisen von Benutzern zu Sicherheitsrollen](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="87364-121">For more information, see [Assign users to security roles](assign-users-security-roles.md) page.</span></span>
    - <span data-ttu-id="87364-122">Wenn **Aufgabe** ausgewählt ist, wählen Sie **Aufgabe zu Rolle hinzufügen** aus, wählen Sie die Rollen aus, zu denen die Aufgabe hinzugefügt werden soll, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="87364-122">If **Duty** is selected, select **Add duty to role**, select the roles that the duty should be added to, and then select **OK**.</span></span>
    - <span data-ttu-id="87364-123">Wenn **Recht** ausgewählt ist, wählen Sie **Recht zu Aufgaben hinzufügen** aus, wählen Sie die Rollen aus, zu denen die Aufgabe hinzugefügt werden soll, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="87364-123">If **Privilege** is selected, select **Add privilege to duties**, select the roles that the duty should be added to, and then select **OK**.</span></span>
