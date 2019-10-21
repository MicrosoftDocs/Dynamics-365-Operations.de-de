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
ms.openlocfilehash: 35ad27a6b8a52bfd086fbe4fc57b1681ff88fd5b
ms.sourcegitcommit: 58db26b7edf02e7c33aaaf1c934e3263aa74b01f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/11/2019
ms.locfileid: "1995141"
---
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>Melden Sie einen nicht kennzeichengesteuerte Lagerplatz über das Einzelvorgangslistengerät als beendet 

Der Prozess, der Fertigmeldung genannt wird, schließt Produkte auf einem Produktionsauftrag im Lagerbestand ab. Wenn das fertige Produkt für die erweiterten Lagerortprozesse aktiviert ist, wird das Produkt, das als fertig gemeldet wurde, in einem Lagerort als fertig gemeldet, der auch als Produktionsausgabelagerplatz bezeichnet wird. Informationen zum Einrichten des Produktionsausgabelagerplatzes finden Sie unter [Lagerplatz für Produktions-Warenabgang](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).

Sie müssen eine vorhandene Kennzeichennummer auswählen, um diese Aufgabe abzuschließen. Wenn der Produktionsausgabelagerplatz zur Verfolgung nach Kennzeichennummer eingerichtet wird, muss eine Kennzeichennummer beim Melden der Produktion als fertig enthalten sein. Das Feld **Kennzeichen** wird in der Aufforderung **Berichtsfortschritt** auf der Seite **Einzelvorgangslistengerät** angezeigt. Das Feld ist nur auf Berichten im Zuge des letzten Arbeitsgangs eines Produktionsauftrags unter **Berichtsfortschritt** sichtbar. Das Feld wird nur angezeigt, wenn der Artikel für den Produktionsauftrag für die Lagerortverwaltungsprozesse aktiviert ist. 