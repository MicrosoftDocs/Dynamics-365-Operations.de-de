---
title: Melden Sie einen nicht kennzeichengesteuerte Lagerplatz über das Einzelvorgangslistengerät als beendet
description: In diesem Thema wird der Prozess zum Abschließen von Produkten auf einem Produktionsauftrag im Bestand beschrieben, wenn ein Lagerplatz kennzeichengesteuert ist.
author: johanhoffmann
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: cb809e596fd6bf3030bcee460838798435512b95
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572128"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a><span data-ttu-id="5363a-103">Melden Sie einen nicht kennzeichengesteuerte Lagerplatz über das Einzelvorgangslistengerät als beendet</span><span class="sxs-lookup"><span data-stu-id="5363a-103">Report as finished to a license plate controlled location from the Job card device</span></span> 

<span data-ttu-id="5363a-104">Der Prozess, der Fertigmeldung genannt wird, schließt Produkte auf einem Produktionsauftrag im Lagerbestand ab.</span><span class="sxs-lookup"><span data-stu-id="5363a-104">The process called Reporting as finished completes finished products on a production order to the inventory.</span></span> <span data-ttu-id="5363a-105">Wenn das fertige Produkt für die erweiterten Lagerortprozesse aktiviert ist, wird das Produkt, das als fertig gemeldet wurde, in einem Lagerort als fertig gemeldet, der auch als Produktionsausgabelagerplatz bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="5363a-105">If the finished product is enabled for the advanced warehouse processes, the product is reported as finished to a location called the production output location.</span></span> <span data-ttu-id="5363a-106">Informationen zum Einrichten des Produktionsausgabelagerplatzes finden Sie unter [Lagerplatz für Produktions-Warenabgang](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span><span class="sxs-lookup"><span data-stu-id="5363a-106">For information about setting up the production output location, see [Production output location](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span></span>

<span data-ttu-id="5363a-107">Sie müssen eine vorhandene Kennzeichennummer auswählen, um diese Aufgabe abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="5363a-107">You must select an existing license plate number to complete this task.</span></span> <span data-ttu-id="5363a-108">Wenn der Produktionsausgabelagerplatz zur Verfolgung nach Kennzeichennummer eingerichtet wird, muss eine Kennzeichennummer beim Melden der Produktion als fertig enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="5363a-108">If the production output location is set up to be tracked by license plate, then a license plate number must be included when reporting the production output location as finished.</span></span> <span data-ttu-id="5363a-109">Das Feld **Kennzeichen** wird in der Aufforderung **Berichtsfortschritt** auf der Seite **Einzelvorgangslistengerät** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5363a-109">The **License plate** field is visible on the **Report progress** prompt on the **Job card device** page.</span></span> <span data-ttu-id="5363a-110">Das Feld ist nur auf Berichten im Zuge des letzten Arbeitsgangs eines Produktionsauftrags unter **Berichtsfortschritt** sichtbar.</span><span class="sxs-lookup"><span data-stu-id="5363a-110">The field is only visible on the **Report progress** prompt when reporting on the last operation of the production order.</span></span> <span data-ttu-id="5363a-111">Das Feld wird nur angezeigt, wenn der Artikel für den Produktionsauftrag für die Lagerortverwaltungsprozesse aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5363a-111">The field is only shown if the item for the production order is enabled for the warehouse management processes.</span></span> 
