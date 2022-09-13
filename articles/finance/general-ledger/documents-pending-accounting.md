---
title: Belege in der offenen Buchhaltung
description: Dieser Artikel beschreibt, wie Sie die Funktionen auf der Seite „Belege in der offenen Buchhaltung” können.
author: ryanCCarlson2
ms.date: 09/02/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: e915c248abd1c842f8f01490a49db9b824644a29
ms.sourcegitcommit: 07ed6f04dcf92a2154777333651fefe3206a817a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2022
ms.locfileid: "9424365"
---
# <a name="documents-pending-accounting"></a>Belege in der offenen Buchhaltung

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Dieser Artikel beschreibt, wie Sie die Funktionen auf der Seite **Belege in der offenen Buchhaltung** können.

In Microsoft Dynamics 365 Finance 10.0.30 ist die Funktion **Verbesserte Leistung des Quelldokument-Buchhaltungsframeworks** verfügbar. Diese Funktion verbessert die Buchungsprozesse für Quelldokument-fähige Dokumentbuchungen, beginnend mit dem Buchungsprozess für Freitext-Rechnungen.

Wenn diese Funktion aktiviert ist, erfolgt die Buchung des untergeordneten Sachkontos getrennt von der Buchungserstellung oder *Journalisierung*, die die vollständigen Buchungsdetails erstellt, die in das Hauptbuch übertragen werden. Bei der Buchung von Freitext-Rechnungen wird zum Beispiel die Debitorenrechnung im Modul **Debitoren** erfasst, bevor die vollständige Buchung erstellt wird. Durch diese leistungssteigernde Funktion können Debitorenrechnungen schneller erfasst werden, während sich die Erstellung der Buchhaltung verzögert.

Die folgenden Schaltflächen sind auf der Seite **Belege in der offenen Buchhaltung** verfügbar.

- **Buchhaltung generieren** – Senden Sie einen Beleg, der derzeit zur Erfassung ansteht, zur Journalisierung.
- **Verteilungen ansehen** – Zeigen Sie die Buchhaltungsverteilungen für einen ausgewählten Beleg in der Liste an.
- **Fehlerprotokoll anzeigen** – Zeigen Sie alle Details zu Fehlermeldungen an, die für einen Beleg existieren, bei dem der Status der Buchhaltung „Fehler” anzeigt. Sie können dieselben Details zu Fehlermeldungen anzeigen, indem Sie den Link **Fehlerprotokoll** in der Belegzeile auswählen.

Die Erstellung der Buchhaltung erfolgt über einen Hintergrundprozess der Prozessautomatisierung, der **Accounting Framework Processor** genannt wird. Weitere Informationen über die Einrichtung und Konfiguration aller Prozessautomatisierungen finden Sie unter [Prozessautomatisierung](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
