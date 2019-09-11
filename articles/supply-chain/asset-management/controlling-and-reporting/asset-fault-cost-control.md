---
title: Kostensteuerung für Anlagenfehler
description: In diesem Thema wird die Kostensteuerung für Anlagenfehler in der Anlagenverwaltung erläutert.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2fe75c327cdc2bdd76173430ed551895f5941c7b
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918302"
---
# <a name="asset-fault-cost-control"></a><span data-ttu-id="0975e-103">Kostensteuerung für Anlagenfehler</span><span class="sxs-lookup"><span data-stu-id="0975e-103">Asset fault cost control</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="0975e-104">In der Anlagenverwaltung können Sie Kosten für Anlagenfehlererfassungen berechnen, um sich so einen Überblick über die Istkosten im Vergleich zu den Budgetkosten für Fehler zu verschaffen.</span><span class="sxs-lookup"><span data-stu-id="0975e-104">In Asset Management, you can calculate costs on asset fault registrations to get an overview of actual costs compared to budget costs on faults.</span></span> <span data-ttu-id="0975e-105">Istkosten basieren auf gebuchten Transaktionen.</span><span class="sxs-lookup"><span data-stu-id="0975e-105">Actual costs are based on posted transactions.</span></span> <span data-ttu-id="0975e-106">Das Datum ist das Fehlerdatum, an dem das Symptom erfasst wurde.</span><span class="sxs-lookup"><span data-stu-id="0975e-106">The date is the fault date on which the symptom was recorded.</span></span>

1. <span data-ttu-id="0975e-107">Klicken Sie auf **Anlagenverwaltung** > **Abfragen** > **Anlagenfehler** > **Kostensteuerung für Anlagenfehler**.</span><span class="sxs-lookup"><span data-stu-id="0975e-107">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault cost control**.</span></span>

2. <span data-ttu-id="0975e-108">Im Dialogfeld **Kostensteuerung für Anlagenfehler** wählen Sie eine Finanzdimension aus, die in die Berechnung einbezogen werden soll, falls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0975e-108">In the **Asset fault cost control** dialog, select a financial dimension set to be included in the calculation, if required.</span></span>

4. <span data-ttu-id="0975e-109">Wählen Sie „Ja“ auf der Umschaltfläche **Null überspringen** aus, wenn keine Ergebnisse mit Kosten von Null angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0975e-109">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="0975e-110">Sie können das Feld **Ebene** verwenden, um anzugeben, wie detailliert die Kostensteuerungspositionen bezüglich funktionaler Standorte sein sollen.</span><span class="sxs-lookup"><span data-stu-id="0975e-110">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> <span data-ttu-id="0975e-111">Wenn Sie beispielsweise die Zahl „1“ im Feld einfügen und eine funktionale Standortstruktur auf mehreren Ebenen haben, werden alle Kostensteuerungspositionen für einen funktionalen Standort auf der höchsten Ebene angezeigt, und daher werden die Stunden in einer Position von den funktionalen Standorten auf einer niedrigeren Ebene hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0975e-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="0975e-112">Wenn Sie die Zahl „0“ im Feld **Ebene** eingeben, wird ein detailliertes Ergebnis mit allen Kostensteuerungspositionen von Anlagenfehlern für alle funktionalen Standortebenen angezeigt, denen sie zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0975e-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault cost control lines on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="0975e-113">Wenn Sie die Suche begrenzen möchten, können Sie bestimmte Anlagen, Fehlerdaten und Fehlerursachen auf dem Inforegister **Einzuschließende Datensätze** auswählen.</span><span class="sxs-lookup"><span data-stu-id="0975e-113">If you want to limit the search, you can select specific assets, fault dates, and fault causes on the **Records to include** FastTab.</span></span>

7. <span data-ttu-id="0975e-114">Klicken Sie auf **OK**, um die Berechnung zu starten.</span><span class="sxs-lookup"><span data-stu-id="0975e-114">Click **OK** to start the calculation.</span></span>

8. <span data-ttu-id="0975e-115">In den Aktivitätsbereichsgruppen **Gruppieren nach…** klicken Sie auf die entsprechenden Schaltflächen, um die erforderliche Detailebene der Berechnung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0975e-115">In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="0975e-116">Die ausgewählten Aktionsbereichschaltflächen werden hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="0975e-116">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="0975e-117">Klicken Sie auf eine Schaltfläche, um sie zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="0975e-117">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="0975e-118">In der folgenden Abbildung wird ein Beispiel der Berechnung der Kostensteuerung für Anlagenfehler angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0975e-118">The figure below shows an example of an asset fault cost control calculation.</span></span>

![Abbildung 1](media/05-controlling-and-reporting.png)

<span data-ttu-id="0975e-120">Informationen zum Einrichten von Fehlern finden Sie unter [Fehlermanagement](../setup-for-work-orders/fault-management.md).</span><span class="sxs-lookup"><span data-stu-id="0975e-120">Refer to the [Fault management](../setup-for-work-orders/fault-management.md) section for information on how to set up faults.</span></span>

>[!NOTE]
><span data-ttu-id="0975e-121">Das Feld **Ursprüngliches Budget** zeigt Budgetkosten aus der Arbeitsauftragsplanung.</span><span class="sxs-lookup"><span data-stu-id="0975e-121">The **Original budget** field shows budget costs from the work order forecast.</span></span> <span data-ttu-id="0975e-122">Das Feld **Istkosten** zeigt gebuchte Kosten auf Arbeitsaufträgen.</span><span class="sxs-lookup"><span data-stu-id="0975e-122">The **Actual cost** field shows posted costs on work orders.</span></span> <span data-ttu-id="0975e-123">Das Feld **Zugesagte Kosten** zeigt die Gesamtkosten, zu denen Ihr Unternehmen in Bezug auf Arbeitsaufträge verpflichtet ist.</span><span class="sxs-lookup"><span data-stu-id="0975e-123">The **Committed cost** field shows total costs that your company is committed to in relation to work orders.</span></span>

