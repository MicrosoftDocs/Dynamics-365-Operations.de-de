---
title: Invoice Capture-Lösungsdashboard
description: Dieser Artikel beschreibt das Dashboard der Invoice Capture-Lösung.
author: sunfzam
ms.date: 10/15/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4c9000039488c1290f4ab992d7fe79b8ccac7b19
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690121"
---
# <a name="invoice-capture-solution-dashboard"></a>Invoice Capture-Lösungsdashboard

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In Invoice Capture enthält das Dashboard Diagramme, die einen Überblick über importierte Rechnungen bieten. Diese Diagramme können dem Leiter der Kreditorenbuchhaltung (AP) helfen, die Leistung des Rechnungserstellungsprozesses zu analysieren. Der AP-Manager kann den Status des Rechnungserstellungsprozesses und durch Anwenden verschiedener Filter auch Details anzeigen.

## <a name="available-charts"></a>Verfügbare Diagramme

Die folgenden Diagramme sind im Dashboard verfügbar:

- **Alle erfassten Rechnungen nach Status** – Dieses Diagramm zeigt die folgenden Status für eine erfasste Rechnung. Durch die Auswahl eines Status können Benutzer die erfassten Rechnungen in der detaillierten Liste filtern.

    - Erfasst
    - Vollständig
    - Wird überprüft
    - Veraltet

- **Gesamtes erfasstes Rechnungsvolumen** – Dieses Diagramm zeigt die Anzahl der erfassten Rechnungen nach Zeitraum. Benutzer können den Zeitraum mithilfe der Dropdown-Liste ändern.
- **Erfasste Rechnungen von den wichtigsten Kreditoren** – Dieses Diagramm zeigt die Gesamtanzahl der erfassten Rechnungen pro Kreditor an. Die Lieferanten mit den meisten Rechnungen erscheinen ganz oben.
- **Tage, die pro Rechnung abgeschlossen werden müssen, mit Ausnahmen** – Dieses Diagramm zeigt die durchschnittliche Anzahl von Tagen, die zum Erfassen einer Rechnung erforderlich sind. Diese Informationen können dem AP-Manager helfen, die Zeit für die Verarbeitung einer Rechnung zu analysieren, wenn ein manueller Eingriff erforderlich ist. Wenn es einen Aufwärtstrend gibt, können Benutzer die Prozessdetails überprüfen und Einstellungen anpassen, um die Anzahl der erforderlichen Tage zu reduzieren.
- **Unvollständige Rechnungen nach ausstehender Zeit** – Dieses Diagramm zeigt die Anzahl der Tage, an denen eine erfasste Rechnung nicht im ERP-System (Enterprise Resource Planning) generiert wurde. Je größer die Anzahl der ausstehenden Tage, desto länger dauert der Rechnungserstellungsprozess. Der AP-Manager kann die detailliert erfassten Rechnungen aufschlüsseln und Rechnungen im ERP-System generieren.
