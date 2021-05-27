---
title: Ein Fehler tritt auf, wenn der Lagerplatz während der Kommissionierlistenregistrierung ausgewählt wird
description: Ein Fehler tritt auf, wenn der Lagerplatz während der Kommissionierlistenregistrierung ausgewählt wird.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b7fc579821f9a80d94aea949fcc0301b9d8f6935
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026525"
---
# <a name="an-error-occurs-when-the-location-is-selected-during-picking-list-registration"></a><span data-ttu-id="5e52b-103">Ein Fehler tritt auf, wenn der Lagerplatz während der Kommissionierlistenregistrierung ausgewählt wird</span><span class="sxs-lookup"><span data-stu-id="5e52b-103">An error occurs when the location is selected during picking list registration</span></span>

<span data-ttu-id="5e52b-104">KB-Nummer: 4613106</span><span class="sxs-lookup"><span data-stu-id="5e52b-104">KB number: 4613106</span></span>

## <a name="symptoms"></a><span data-ttu-id="5e52b-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="5e52b-105">Symptoms</span></span>

<span data-ttu-id="5e52b-106">Dieses Problem tritt auf, wenn Ihr System so konfiguriert ist, dass Aufträge automatisch reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="5e52b-106">This issue occurs when your system is configured to automatically reserve sales orders.</span></span> <span data-ttu-id="5e52b-107">Wenn Sie versuchen, den Lagerplatz für eine Kommissionierlistenregistrierungsposition auszuwählen, wird bei Verwendung des Reservierungsprozesses im Lagerortmanagement (WMS) die folgende Fehlermeldung angezeigt:</span><span class="sxs-lookup"><span data-stu-id="5e52b-107">If you try to select the location for a picking list registration line, you receive the following error message when you use warehouse management (WMS) reservation processes:</span></span>

> <span data-ttu-id="5e52b-108">Menge kann nicht mit neuen Dimensionen aktualisiert werden</span><span class="sxs-lookup"><span data-stu-id="5e52b-108">Can't update quantity with new dimensions</span></span>

<span data-ttu-id="5e52b-109">Dieses Problem kann auftreten, weil Sie an einem bestimmten Lagerplatz nicht über genügend Bestände verfügen.</span><span class="sxs-lookup"><span data-stu-id="5e52b-109">This issue can occur because you don't have enough on-hand inventory at a specified location.</span></span>

## <a name="resolution"></a><span data-ttu-id="5e52b-110">Lösung</span><span class="sxs-lookup"><span data-stu-id="5e52b-110">Resolution</span></span>

<span data-ttu-id="5e52b-111">Das System verhält sich wie vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="5e52b-111">The system is behaving as designed.</span></span>

<span data-ttu-id="5e52b-112">In Szenarien, in denen Sie den Reservierungsprozess auf Lagerortebene verwenden, sollten Sie den manuellen Reservierungsprozess von der Entnahmeposition aus verwenden, wenn der vorhandene Bestand nicht auf allen Bestandsdimensionsebenen reserviert wird und Sie nicht über ausreichend verfügbare Bestände an einem bestimmten Lagerplatz verfügen.</span><span class="sxs-lookup"><span data-stu-id="5e52b-112">In scenarios where you use the warehouse-level reservation process, if the on-hand inventory won't be reserved on all inventory dimension levels, and you don't have enough on-hand inventory at a specified location, we recommend that you use the manual reservation process from the picking line.</span></span> <span data-ttu-id="5e52b-113">Sie können dann die Funktion *Los reservieren* zum Verteilen der unteren Reservierungen verwenden, z. B. des Lagerplatzes, für alle verfügbaren Mengen.</span><span class="sxs-lookup"><span data-stu-id="5e52b-113">You can then use the *Reserve lot* function to distribute the lower reservations, such as location, for all the available on-hand quantities.</span></span>
