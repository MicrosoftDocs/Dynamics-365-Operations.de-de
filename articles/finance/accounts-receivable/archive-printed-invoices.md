---
title: Gedruckte Debitorenrechnungen mit Hashnummern archivieren
description: In diesem Thema wird erläutert, wie Sie die Archivierung aktivieren, um gedruckte Debitorenrechnungen mit Hashnummern zu speichern.
author: ilyako
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 841e6059f5b0d70dbd1fe12a1f8910bbb31ddc86
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018977"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a>Gedruckte Debitorenrechnungen mit Hashnummern archivieren

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

In einigen Ländern ist es gesetzlich vorgeschrieben, berechnete Hashnummern zusammen mit Ausdrucken einiger Dokumente im System zu speichern. Hashnummern können für die Berichterstattung an Behörden und während Audits verwendet werden.

In diesem Thema wird erläutert, wie Sie die Archivierung konfigurieren, um gedruckte Debitorenrechnungen mit Hashnummern zu speichern.

## <a name="prerequisites"></a>Voraussetzungen

- In dem Arbeitsbereich **Funktionsverwaltung** aktivieren Sie die Funktion **Gedruckte Debitorenrechnungen mit Hashnummern archivieren**. Weitere Informationen finden Sie unter [Funktionsverwaltung – Übersicht](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Konfigurieren Sie die druckbaren Formate der erforderlichen Dokumente in der **Druckverwaltung**.

Diese Funktionalität gilt für die folgenden Dokumente.

**Debitorenkonten**
- Debitorenrechnung
- Debitorengutschrift
- Freitextrechnung
- Freitext-Gutschrift

**Projektverwaltung und Buchhaltung**
- Projektrechnung
- Projektgutschrift

## <a name="configure-customer-master-data"></a>Debitorenmasterdaten konfigurieren
Führen Sie die folgenden Schritte aus, um Kundendaten zu konfigurieren und die Möglichkeit zu aktivieren, gedruckte Rechnungen automatisch als Anhänge zu speichern.

1. Wechseln Sie zu **Debitorenkonten** > **Alle Debitoren**. 
2. Wählen Sie einen Kunden aus und wählen Sie im Inforegister **Rechnung und Lieferung** im Abschnitt **E-RECHNUNG** im Feld **eInvoice-Anhang** die Option **Ja** aus.

## <a name="print-invoices"></a>Rechnungen drucken
Sie können jede Freitext-, Debitoren- und Projektrechnung oder -gutschrift für den Kunden, die im vorherigen Verfahren konfiguriert wurde, buchen und ausdrucken.

Öffnen Sie die Seite **Anhänge** für die gedruckte Rechnung. Im Inforegister **Anhang** in der Feldgruppe **Weitere Details** im Feld **Dokument-Hashnummer** finden Sie die gespeicherte Hashnummer, die für die gedruckte Rechnung berechnet wurde.

![Anhangs-Hashnummer](media/attach-hash-num.jpg)

