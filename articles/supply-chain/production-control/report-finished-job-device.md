---
title: Melden Sie einen nicht kennzeichengesteuerte Lagerplatz über das Einzelvorgangslistengerät als beendet
description: In diesem Thema wird der Prozess zum Abschließen von Produkten auf einem Produktionsauftrag im Bestand beschrieben, wenn ein Lagerplatz kennzeichengesteuert ist.
author: johanhoffmann
manager: tfehr
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: f5863202facc83afb91b380ba5666334783ccbcf
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211168"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a><span data-ttu-id="0a1de-103">Melden Sie einen nicht kennzeichengesteuerte Lagerplatz über das Einzelvorgangslistengerät als beendet</span><span class="sxs-lookup"><span data-stu-id="0a1de-103">Report as finished to a license plate controlled location from the Job card device</span></span> 

<span data-ttu-id="0a1de-104">Der Prozess, der Fertigmeldung genannt wird, schließt Produkte auf einem Produktionsauftrag im Lagerbestand ab.</span><span class="sxs-lookup"><span data-stu-id="0a1de-104">The process called Reporting as finished completes finished products on a production order to the inventory.</span></span> <span data-ttu-id="0a1de-105">Wenn das fertige Produkt für die erweiterten Lagerortprozesse aktiviert ist, wird das Produkt, das als fertig gemeldet wurde, in einem Lagerort als fertig gemeldet, der auch als Produktionsausgabelagerplatz bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="0a1de-105">If the finished product is enabled for the advanced warehouse processes, the product is reported as finished to a location called the production output location.</span></span> <span data-ttu-id="0a1de-106">Informationen zum Einrichten des Produktionsausgabelagerplatzes finden Sie unter [Lagerplatz für Produktions-Warenabgang](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span><span class="sxs-lookup"><span data-stu-id="0a1de-106">For information about setting up the production output location, see [Production output location](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span></span>

<span data-ttu-id="0a1de-107">Wenn der Produktionsausgabestandort kennzeichengesteuert ist, muss ein Kennzeichen angegeben werden, wenn die Meldung als abgeschlossen gilt.</span><span class="sxs-lookup"><span data-stu-id="0a1de-107">If the production output location is license plate controlled, then a license plate must be provided when reporting as finished.</span></span> <span data-ttu-id="0a1de-108">Das Feld **Kennzeichen** wird in der Aufforderung **Berichtsfortschritt** auf der Seite **Einzelvorgangslistengerät** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0a1de-108">The **License plate** field is visible on the **Report progress** prompt on the **Job card device** page.</span></span> <span data-ttu-id="0a1de-109">Das Feld ist nur in der Aufforderung **Fortschritt melden** sichtbar, wenn die Berichtsstellung beim letzten Vorgang des Produktsionauftrags und des Artikels für den Produktionsauftrag für Lagerortverwaltungsprozesse aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0a1de-109">The field is only visible on the **Report progress** prompt when reporting on the last operation of the production order and the item for the production order is enabled for the warehouse management processes.</span></span> 

<span data-ttu-id="0a1de-110">Es gibt zwei Möglichkeiten, das Kennzeichen bereitzustellen</span><span class="sxs-lookup"><span data-stu-id="0a1de-110">There are two options for providing the license plate</span></span>
- <span data-ttu-id="0a1de-111">Der Benutzer wählt im Kennzeichenfeld ein vorhandenes Kennzeichen aus.</span><span class="sxs-lookup"><span data-stu-id="0a1de-111">The user is selecting an existing license plate in the license plate field.</span></span>
- <span data-ttu-id="0a1de-112">Das Kennzeichen wird automatisch aus einer Nummernfolge generiert und standardmäßig in das Kennzeichenfeld übernommen.</span><span class="sxs-lookup"><span data-stu-id="0a1de-112">The license plate is automatically generated from a number sequence and defaulted to the license plate field.</span></span>

<span data-ttu-id="0a1de-113">Die Option, den Ladungsträger automatisch generieren zu lassen, wird durch die Auswahl der Option **Ladungsträger generieren** auf der Seite **Einzelvorgangsliste für Geräte konfigurieren** generiert.</span><span class="sxs-lookup"><span data-stu-id="0a1de-113">The option to have the license plate generated automatically is configured by selecting the option **Generate license plate** on the **Configure job card for devices** page.</span></span>
