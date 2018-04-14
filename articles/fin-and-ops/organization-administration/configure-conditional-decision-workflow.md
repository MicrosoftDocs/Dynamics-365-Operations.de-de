---
title: Konfigurieren einer bedingten Entscheidung in einem Workflow
description: Verwenden Sie die folgenden Verfahren, um die Eigenschaften der bedingten Entscheidung zu konfigurieren.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: af000e04af6a2a2821ee37f3dd0e91b3e0d0d42a
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---

# <a name="configure-a-conditional-decision-in-a-workflow"></a><span data-ttu-id="f259e-103">Konfigurieren einer bedingten Entscheidung in einem Workflow</span><span class="sxs-lookup"><span data-stu-id="f259e-103">Configure a conditional decision in a workflow</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="f259e-104">Verwenden Sie die folgenden Verfahren, um die Eigenschaften der bedingten Entscheidung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="f259e-104">Use the following procedure to configure the properties of a conditional decision.</span></span>

<span data-ttu-id="f259e-105">Eine bedingte Entscheidung ist ein Punkt, an dem ein Workflow sich in zwei Verzweigungen gabelt.</span><span class="sxs-lookup"><span data-stu-id="f259e-105">A conditional decision is a point at which a workflow divides into two branches.</span></span> <span data-ttu-id="f259e-106">Klicken Sie zum Konfigurieren einer bedingten Entscheidung im Workflow-Editor mit der rechten Maustaste auf die bedingte Entscheidung, und klicken Sie dann auf **Eigenschaften**, um das Formular **Eigenschaften** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f259e-106">To configure a conditional decision, in the workflow editor, right-click the conditional decision, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-a-decision"></a><span data-ttu-id="f259e-107">Name einer Entscheidung</span><span class="sxs-lookup"><span data-stu-id="f259e-107">Name a decision</span></span>
<span data-ttu-id="f259e-108">Gehen Sie folgendermaßen vor, um einen Namen für die bedingte Entscheidung einzugeben.</span><span class="sxs-lookup"><span data-stu-id="f259e-108">Follow these steps to enter a name for a conditional decision.</span></span>
1.  <span data-ttu-id="f259e-109">Klicken Sie im linken Bereich auf **Grundeinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="f259e-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="f259e-110">Geben Sie im Feld **Name** einen eindeutigen Namen für die bedingte Entscheidung ein.</span><span class="sxs-lookup"><span data-stu-id="f259e-110">In the **Name** field, enter a unique name for the conditional decision.</span></span>

## <a name="set-conditions"></a><span data-ttu-id="f259e-111"> Festlegen von Bedingungen</span><span class="sxs-lookup"><span data-stu-id="f259e-111">Set conditions</span></span>
<span data-ttu-id="f259e-112">Das System bestimmt durch Überprüfen, ob das übermittelte Dokument bestimmten Bedingungen entspricht, welche Verzweigung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f259e-112">The system determines which branch is used by evaluating the submitted document to determine whether it meets specific conditions.</span></span>
1.  <span data-ttu-id="f259e-113">Klicken Sie im linken Bereich auf **Grundeinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="f259e-113">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="f259e-114">Klicken Sie auf **Bedingung hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="f259e-114">Click **Add condition**.</span></span>
3.  <span data-ttu-id="f259e-115">Geben Sie eine Bedingung ein.</span><span class="sxs-lookup"><span data-stu-id="f259e-115">Enter a condition.</span></span>
4.  <span data-ttu-id="f259e-116">Geben Sie ggf. zusätzliche Bedingungen ein.</span><span class="sxs-lookup"><span data-stu-id="f259e-116">Enter additional conditions, if they are required.</span></span>
5.  <span data-ttu-id="f259e-117">Führen Sie folgende Schritte aus, um die korrekte Konfiguration der eingegebenen Bedingungen zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="f259e-117">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>
    1.  <span data-ttu-id="f259e-118">Klicken Sie auf **Test**, um das Formular **Workflow-Bedingungen testen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f259e-118">Click **Test** to open the **Test workflow condition** form.</span></span>
    2.  <span data-ttu-id="f259e-119">Wählen Sie im Bereich **Bedingung überprüfen** des Formulars einen Datensatz aus.</span><span class="sxs-lookup"><span data-stu-id="f259e-119">Select a record in the **Validate condition** area of the form.</span></span>
    3.  <span data-ttu-id="f259e-120">Klicken Sie auf **Test**.</span><span class="sxs-lookup"><span data-stu-id="f259e-120">Click **Test**.</span></span> <span data-ttu-id="f259e-121">Der Datensatz wird ausgewertet, um zu bestimmen, ob er den festgelegten Bedingungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="f259e-121">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4.  <span data-ttu-id="f259e-122">Klicken Sie auf **OK** oder **Abbrechen**, um zum Formular **Eigenschaften** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="f259e-122">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>






