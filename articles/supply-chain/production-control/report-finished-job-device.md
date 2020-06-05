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
ms.openlocfilehash: 74e1e30f5afe51cd0ecec2530ffcb9a59eec5fee
ms.sourcegitcommit: 89022f39502b19c24c0997ae3a01a64b93280f42
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2020
ms.locfileid: "3367244"
---
# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>Melden Sie einen nicht kennzeichengesteuerte Lagerplatz über das Einzelvorgangslistengerät als beendet

[!include [banner](../includes/banner.md)]

Der Prozess, der Fertigmeldung genannt wird, schließt Produkte auf einem Produktionsauftrag im Lagerbestand ab. Wenn das fertige Produkt für die erweiterten Lagerortprozesse aktiviert ist, wird das Produkt, das als fertig gemeldet wurde, in einem Lagerort als fertig gemeldet, der auch als Produktionsausgabelagerplatz bezeichnet wird. Informationen zum Einrichten des Produktionsausgabelagerplatzes finden Sie unter [Lagerplatz für Produktions-Warenabgang](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).

Wenn der Produktionsausgabestandort kennzeichengesteuert ist, muss ein Kennzeichen angegeben werden, wenn die Meldung als abgeschlossen gilt. Das Feld **Kennzeichen** wird in der Aufforderung **Berichtsfortschritt** auf der Seite **Einzelvorgangslistengerät** angezeigt. Das Feld ist nur in der Aufforderung **Fortschritt melden** sichtbar, wenn die Berichtsstellung beim letzten Vorgang des Produktsionauftrags und des Artikels für den Produktionsauftrag für Lagerortverwaltungsprozesse aktiviert ist.

Es gibt zwei Möglichkeiten, das Kennzeichen bereitzustellen:

- Der Benutzer wählt im Kennzeichenfeld ein vorhandenes Kennzeichen aus.
- Das Kennzeichen wird automatisch aus einer Nummernfolge generiert und standardmäßig in das Kennzeichenfeld übernommen.

Die Option, den Ladungsträger automatisch generieren zu lassen, wird durch die Auswahl der Option **Ladungsträger generieren** auf der Seite **Einzelvorgangsliste für Geräte konfigurieren** generiert.
