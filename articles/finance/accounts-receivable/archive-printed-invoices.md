---
title: Gedruckte Debitorenrechnungen mit Hashnummern archivieren
description: In diesem Artikel wird erläutert, wie Sie die Archivierung aktivieren, um gedruckte Debitorenrechnungen mit Hashnummern zu speichern.
author: mrolecki
ms.date: 09/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.custom: 539093
ms.search.form: ''
ms.openlocfilehash: 4c9bd7ead1615a4e6b0e8e672e858312ba518b56
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291668"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a>Gedruckte Debitorenrechnungen mit Hashnummern archivieren

[!include [banner](../includes/banner.md)]

In einigen Ländern ist es gesetzlich vorgeschrieben, berechnete Hashnummern zusammen mit Ausdrucken einiger Dokumente im System zu speichern. Hashnummern können für die Berichterstattung an Behörden und während Audits verwendet werden.

In diesem Artikel wird erläutert, wie Sie die Archivierung konfigurieren, um gedruckte Debitorenrechnungen mit Hashnummern zu speichern.

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

![Anhangs-Hashnummer.](media/attach-hash-num.jpg)

