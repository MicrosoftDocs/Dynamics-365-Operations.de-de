---
title: Leistungsverbesserung der Kontostrukturaktivierung
description: In diesem Artikel wird die neue Leistungsverbesserung für den Aktivierungsprozess der Kontostruktur erläutert.
author: RyanCCarlson2
ms.date: 10/31/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2022-10-08
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: 42f8fcebba6465261489f74a9bb1dd46c2d5fa16
ms.sourcegitcommit: c6c2486be2359bd30106f7f52bda788239147d8c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/22/2022
ms.locfileid: "9713998"
---
# <a name="account-structure-activation-performance-enhancement"></a>Leistungsverbesserung der Kontostrukturaktivierung

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Dank dieser Leistungsverbesserung können Sie Kontostrukturen schneller aktivieren, indem Sie mehrere Transaktionsaktualisierungen gleichzeitig ausführen. Darüber hinaus wird die Struktur nach ihrer Überprüfung als aktiv markiert, und die Transaktionsverarbeitung kann fortgesetzt werden, während vorhandene ungebuchte Transaktionen auf die neue Struktur aktualisiert werden. Da Transaktionsaktualisierungen einige Zeit in Anspruch nehmen können, können Sie den Status Ihrer Aktivierung verfolgen, indem Sie auf der Seite **Kontostrukturen** über dem Raster **Aktivierungsstatus anzeigen** auswählen. Außerdem können Sie den Aktivierungsstauts auch einsehen, indem Sie im Aktivitätsbereich **Anzeigen** und dann aus dem Dropdownmenü **Aktivierungsstatus** auswählen.

[![Seite Kontostrukturen](./media/AccountStructure1.png)](./media/AccountStructure1.png)

Nachdem Sie **Aktivierungsstatus anzeigen** ausgewählt haben, wird ein Dialogfeld mit den einzelnen Aufgaben angezeigt, die im Rahmen des Aktivierungsprozesses ausgeführt werden. Sie können für jede Aufgabe den Status sowie nach Abschluss der Aufgabe Datum und Uhrzeit des Abschlusses anzeigen.

[![Zeitskala für die Aktivierung der Kontostruktur.](./media/AccountStructureTimeline.png)](./media/AccountStructureTimeline.png)

## <a name="account-structure-activation-tips"></a>Tipps für die Kontostrukturaktivierung

Im Dialogfeld zur Aktivierung der Kontostruktur, das erscheint, wenn Sie für eine Entwurfskontostruktur **Aktivieren** auswählen, gibt es den Registerkartenabschnitt **Nicht gebuchte Transaktionen aktualisieren**. Dieser Abschnitt enthält die Option **Aktualisierung erzwingen**. Wählen Sie diese Option aus, um alle ungebuchten Transaktionen auf die aktuelle Struktur zu aktualisieren. Sie sollten diese Option jedoch nur verwenden, wenn ein Fehler aufgetreten ist oder der Microsoft-Support Sie dazu auffordert.

Einige Faktoren, die die Leistung des Aktivierungsprozesses beeinflussen können:

- Eine große Zahl ungebuchter Journaldatensätze
- Eine große Zahl an Open-Source-Dokumentdatensätzen wie Freitextrechnungen, Kreditorenrechnungen und zugehörige Dokumente, die das Framework des Quelldokuments verwenden und offene Buchhaltungsverteilungen haben
- Die Datenmenge in TaxUncommitted
- Die Menge an offenen Budgetdaten
- Import von Journaldaten während laufender Aktivierungsaufgaben

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
