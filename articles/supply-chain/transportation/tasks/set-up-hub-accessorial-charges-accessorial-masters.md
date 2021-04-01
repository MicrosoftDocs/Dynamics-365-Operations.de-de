---
title: Hub-Zusatzgebühren und Zusatzleistungsmaster einrichten
description: Im folgenden Verfahren wird dargestellt, wie ein Zusatzleistungsmaster für einen Hub erstellt und dieser Master verwendet wird, um eine Hub-Zusatzgebühr zu erstellen.
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSCarrierAccessorial,TMSAccessorialMaster, TMSHubAccessorial
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb2e9125c7a38d1dc5e6866a056fb71f25e40928
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233678"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a><span data-ttu-id="dd635-103">Hub-Zusatzgebühren und Zusatzleistungsmaster einrichten</span><span class="sxs-lookup"><span data-stu-id="dd635-103">Set up hub accessorial charges and accessorial masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dd635-104">Im folgenden Verfahren wird dargestellt, wie ein Zusatzleistungsmaster für einen Hub erstellt und dieser Master verwendet wird, um eine Hub-Zusatzgebühr zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="dd635-104">This procedure shows how to create an accessorial master for a hub and use that master to create a hub accessorial charge.</span></span> <span data-ttu-id="dd635-105">Das Verfahren verwendet das USMF-Dataset.</span><span class="sxs-lookup"><span data-stu-id="dd635-105">The procedure uses the USMF dataset.</span></span> <span data-ttu-id="dd635-106">Diese Einstellung wird normalerweise von einem Transportkoordinator vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="dd635-106">This set up will typically be done by a transportation coordinator.</span></span>


## <a name="set-up-a-hub-master"></a><span data-ttu-id="dd635-107">Einen Hubmaster einrichten</span><span class="sxs-lookup"><span data-stu-id="dd635-107">Set up a hub master</span></span>
1. <span data-ttu-id="dd635-108">Wechseln Sie zu "Transportverwaltung" > "Einrichten" > "Bewertung" > "Zusatzleistungsmaster".</span><span class="sxs-lookup"><span data-stu-id="dd635-108">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="dd635-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="dd635-109">Click New.</span></span>
3. <span data-ttu-id="dd635-110">Geben Sie einen Wert in das Feld "Zusatzleistungsmaster" ein.</span><span class="sxs-lookup"><span data-stu-id="dd635-110">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="dd635-111">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="dd635-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="dd635-112">Wählen Sie im Feld "Zusatzleistungstyp" "Hub" aus.</span><span class="sxs-lookup"><span data-stu-id="dd635-112">In the Accessorial type field, select 'Hub'.</span></span>
6. <span data-ttu-id="dd635-113">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="dd635-113">Click Save.</span></span>
7. <span data-ttu-id="dd635-114">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="dd635-114">Close the page.</span></span>

## <a name="set-up-a-hub-accessorial-charge"></a><span data-ttu-id="dd635-115">Hubzusatzgebühr einrichten</span><span class="sxs-lookup"><span data-stu-id="dd635-115">Set up a hub accessorial charge</span></span>
1. <span data-ttu-id="dd635-116">Wechseln Sie zu "Transportverwaltung" > "Einrichten" > "Bewertung" > "Hubzusatzgebühren".</span><span class="sxs-lookup"><span data-stu-id="dd635-116">Go to Transportation management > Setup > Rating > Hub accessorial charges.</span></span>
2. <span data-ttu-id="dd635-117">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="dd635-117">Click New.</span></span>
3. <span data-ttu-id="dd635-118">Geben Sie einen Wert in das Feld "Kennung für Hubzusatzgebühren" ein.</span><span class="sxs-lookup"><span data-stu-id="dd635-118">In the Hub accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="dd635-119">Klicken Sie im Feld "Hub" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="dd635-119">In the Hub field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="dd635-120">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="dd635-120">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="dd635-121">Wählen Sie im Feld "Hubposition" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="dd635-121">In the Hub position field, select an option.</span></span>
    * <span data-ttu-id="dd635-122">Sie können den Zuschlag entweder als Abholung oder Lieferung erstellen.</span><span class="sxs-lookup"><span data-stu-id="dd635-122">You can either create the charge as a pickup or drop-off.</span></span> <span data-ttu-id="dd635-123">Je nach getroffener Auswahl wird der Zuschlag dem entsprechenden Transportsegment auf den Arbeitsplan angewendet.</span><span class="sxs-lookup"><span data-stu-id="dd635-123">Depending on your selection the charge will be applied to the corresponding transportation segment on your route.</span></span>  
7. <span data-ttu-id="dd635-124">Klicken Sie im Feld "Zusatzleistungsmaster" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="dd635-124">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="dd635-125">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="dd635-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="dd635-126">Wählen Sie den Master aus, den Sie soeben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="dd635-126">Select the master you just created.</span></span>  
9. <span data-ttu-id="dd635-127">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="dd635-127">Click Save.</span></span>
10. <span data-ttu-id="dd635-128">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="dd635-128">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]