---
title: Erstellen von Blankoschecks
description: In diesem Thema wird erläutert, wie Sie auf der Seite „Schecks“ Blankoschecks für ein Bankkonto erstellen.
author: abruer
manager: AnnBe
ms.date: 10/26/2017
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: af79dd4831f2e7fc71c296922d73a9e42f7955b3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175941"
---
# <a name="create-checks-that-have-blank-status"></a><span data-ttu-id="310ca-103">Erstellen von Blankoschecks</span><span class="sxs-lookup"><span data-stu-id="310ca-103">Create checks that have Blank status</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="310ca-104">In diesem Thema wird erläutert, wie Sie Blankoschecks erstellen.</span><span class="sxs-lookup"><span data-stu-id="310ca-104">This topic explains how to create blank checks.</span></span> <span data-ttu-id="310ca-105">Sie müssen möglicherweise einen Blankoscheck erstellen, um einen Scheck zu erfassen, der beschädigt wurde und nicht zur Zahlung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="310ca-105">For example, you might create a blank check to record a check that has been damaged and can't be used for payment.</span></span>

<span data-ttu-id="310ca-106">Auf der Seite **Schecks** führen Sie Verwaltungsaufgaben für Schecks aus.</span><span class="sxs-lookup"><span data-stu-id="310ca-106">On the **Checks** page, you perform maintenance tasks for checks.</span></span> <span data-ttu-id="310ca-107">Sie können beispielsweise neue Schecknummern erstellen und Schecks löschen.</span><span class="sxs-lookup"><span data-stu-id="310ca-107">For example, you can create new check numbers and delete checks.</span></span> <span data-ttu-id="310ca-108">Sie können auch Schecks erstellen, die den Status **Leer** haben.</span><span class="sxs-lookup"><span data-stu-id="310ca-108">You can also create checks that have a status of **Blank**.</span></span> <span data-ttu-id="310ca-109">Nach der Erstellung eines Blankoschecks können sie diesen nicht im System löschen oder erneut verwenden.</span><span class="sxs-lookup"><span data-stu-id="310ca-109">After blank checks are created, they can't be deleted or reused in the system.</span></span>

> [!NOTE]
> <span data-ttu-id="310ca-110">Diese Funktion ist nur auf der Seite **Schecks** verfügbar, wenn Sie die Funktion **Blankoschecks auf der Seite „Schecks“ erstellen** auf der Seite **Funktionsverwaltung** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="310ca-110">This feature is available on the **Checks** page only if you turn on the **Create checks with a blank status on the Checks page** feature on the **Feature management** page.</span></span> <span data-ttu-id="310ca-111">Wenn die Funktion nicht aktiviert ist, können Sie Schecks mit dem Status **Leer** nur über das Dialogfeld **Zahlung per Scheck** während des Zahlungsgenerierungsprozesses in Kreditorenkonten erstellen.</span><span class="sxs-lookup"><span data-stu-id="310ca-111">If the feature isn't turned on, checks that have **Blank** status can be created only from the **Payment by check** dialog box during the payment generation process in Accounts payable.</span></span>

<span data-ttu-id="310ca-112">Um die Seite **Schecks** zu öffnen, navigieren Sie zu **Bargeld- und Bankverwaltung \> Bankkonten \> Bankkonten** und wählen dann im Aktivitätsbereich auf der Registerkarte **Zahlungen verwalten** in der Gruppe **Zugehörige Informationen** die Option **Schecks** aus.</span><span class="sxs-lookup"><span data-stu-id="310ca-112">To open the **Checks** page, go to **Cash and bank management \> Bank accounts \> Bank accounts**, and then, on the Action Pane, on the **Manage payments** tab, in the **Related information** group, select **Checks**.</span></span> <span data-ttu-id="310ca-113">Alternativ können Sie auch **Bargeld- und Bankverwaltung \> Abfragen und Berichte \> Schecks** verwenden.</span><span class="sxs-lookup"><span data-stu-id="310ca-113">Alternatively, go to **Cash and bank management \> Inquiries and reports \> Checks**.</span></span>

<span data-ttu-id="310ca-114">Um anschließend Schecks mit dem Status **Leer** zu erstellen, wählen Sie im Aktivitätsbereich **Blankoschecks erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="310ca-114">Then, to create checks that have **Blank** status, on the Action Pane, select **Create blank checks**.</span></span> <span data-ttu-id="310ca-115">Während das System Blankoschecks erstellt, wird das zugehörige Bankkonto vorübergehend deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="310ca-115">While the system is creating blank checks, the associated bank account is temporarily inactivated.</span></span> <span data-ttu-id="310ca-116">Dieses Verhalten verringert das Risiko, dass gleichzeitig Zahlungen und Blankoschecks erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="310ca-116">This behavior reduces the risk that payments will be generated at the same time that blank checks are created.</span></span> <span data-ttu-id="310ca-117">Wenn die Verarbeitung abgeschlossen ist, wird das zugehörige Bankkonto wieder aktiviert.</span><span class="sxs-lookup"><span data-stu-id="310ca-117">When the processing is completed, the associated bank account is reactivated.</span></span>
