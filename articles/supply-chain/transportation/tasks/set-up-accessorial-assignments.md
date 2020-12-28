---
title: Zusatzleistungszuweisungen einrichten
description: Dieses Verfahren zeigt Ihnen an, wie eine Zusatzleistungszuweisung eingerichtet wird.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSAccessorialAssignment
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8d7f48da374a0434130f2cf95bf77a126635cd63
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4429075"
---
# <a name="set-up-accessorial-assignments"></a><span data-ttu-id="79c30-103">Zusatzleistungszuweisungen einrichten</span><span class="sxs-lookup"><span data-stu-id="79c30-103">Set up accessorial assignments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="79c30-104">Dieses Verfahren zeigt Ihnen an, wie eine Zusatzleistungszuweisung eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="79c30-104">This procedure shows how to set up an accessorial assignment.</span></span> <span data-ttu-id="79c30-105">Diese Einstellung wird normalerweise von einem Transportkoordinator vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="79c30-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="79c30-106">Bevor Sie diese Anleitung verwenden, müssen Sie die Anweisungen unter "Hubzusatzgebühren und Zusatzleistungsmaster einrichten" ausführen.</span><span class="sxs-lookup"><span data-stu-id="79c30-106">Before you use this guide you need to run the "Set up hub accessorial charges and accessorial masters" guide.</span></span>


## <a name="set-up-accessorial-assignment"></a><span data-ttu-id="79c30-107">Einrichten von Zusatzleistungszuweisung</span><span class="sxs-lookup"><span data-stu-id="79c30-107">Set up Accessorial assignment</span></span>
1. <span data-ttu-id="79c30-108">Wechseln Sie zu "Transportverwaltung" > "Einrichten" > "Bewertung" > "Zusatzleistungszuweisungen".</span><span class="sxs-lookup"><span data-stu-id="79c30-108">Go to Transportation management > Setup > Rating > Accessorial assignments.</span></span>
2. <span data-ttu-id="79c30-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="79c30-109">Click New.</span></span>
3. <span data-ttu-id="79c30-110">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="79c30-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="79c30-111">Schalten Sie die Erweiterung des Abschnitts "Details" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="79c30-111">Toggle the expansion of the Details section.</span></span>
5. <span data-ttu-id="79c30-112">Klicken Sie im Feld "Hub" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="79c30-112">In the Hub field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="79c30-113">Wählen Sie in der Liste den Hub aus, für den Sie einen Zusatzleistungsmaster erstellt haben, als Sie das Handbuch "Hubzusatzgebühren und Zusatzleistungsmaster einrichten" ausgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="79c30-113">In the list, select the Hub that you created an accessorial master for when you ran the "Set up hub accessorial charges and accessorial masters" guide.</span></span> 
7. <span data-ttu-id="79c30-114">Klicken Sie im Feld "Kennung für Hubzusatzgebühren" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="79c30-114">In the Hub accessorial ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="79c30-115">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="79c30-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="79c30-116">Schalten Sie die Erweiterung des Abschnitts "Kriterien" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="79c30-116">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="79c30-117">Im Abschnitt "Kriterien" können Sie basierend auf den verschiedenen angebotenen Werten die genauen Kriterien dafür auswählen, wann die Belastung angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="79c30-117">In the Criteria section you can choose the exact criteria for when the charge should apply, based on the different values offered here.</span></span>  
10. <span data-ttu-id="79c30-118">Legen Sie die Option "Immer anwenden" auf "Ja" fest.</span><span class="sxs-lookup"><span data-stu-id="79c30-118">Set the Always apply option to Yes.</span></span>
11. <span data-ttu-id="79c30-119">Wählen Sie im Feld "Zusatzleistungs-Zuweisungsebene" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="79c30-119">In the Accessorial assignment level field, select an option.</span></span>
12. <span data-ttu-id="79c30-120">Schalten Sie die Erweiterung des Abschnitts "Berechnung" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="79c30-120">Toggle the expansion of the Calculation section.</span></span>
13. <span data-ttu-id="79c30-121">Wählen Sie im Feld "Gebühr Zusatzleistung" "Pauschal" aus.</span><span class="sxs-lookup"><span data-stu-id="79c30-121">In the Accessorial fee type field, select 'Flat'.</span></span>
    * <span data-ttu-id="79c30-122">Der "Gebührentyp Zusatzleistung" bestimmt, wie die tatsächlichen Zuschläge berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="79c30-122">The Accessorial fee type determines how to calculate the actual charge.</span></span> <span data-ttu-id="79c30-123">In diesem Beispiel ist es eine pauschale Belastung.</span><span class="sxs-lookup"><span data-stu-id="79c30-123">In this example it's a flat charge.</span></span>  
14. <span data-ttu-id="79c30-124">Geben Sie im Feld "Gebühr Zusatzleistung" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="79c30-124">In the Accessorial fee field, enter a number.</span></span>
15. <span data-ttu-id="79c30-125">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="79c30-125">Click Save.</span></span>

