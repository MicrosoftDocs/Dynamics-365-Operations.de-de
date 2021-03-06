---
title: Verweise auf Originalrechnungen in Gutschriften
description: In diesem Thema wird erläutert, wie Sie die ursprünglichen Rechnungsnummern in zugehörigen Gutschriften einrichten und ausdrucken.
author: ilkond
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8d7f32c5d3d29be8d1d2742c4017c1719cbd47a8
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897331"
---
# <a name="references-to-original-invoices-in-credit-notes"></a>Verweise auf Originalrechnungen in Gutschriften

[!include [banner](../includes/banner.md)]


In einigen Ländern und Regionen ist es gesetzlich vorgeschrieben, dass gedruckte Gutschriften Verweise auf die Originalrechnungen enthalten. In diesem Thema wird erläutert, wie Sie die ursprünglichen Rechnungsnummern in zugehörigen Gutschriften einrichten und ausdrucken.

## <a name="prerequisites"></a>Voraussetzungen

- Aktivieren Sie im **Funktionsverwaltung**-Arbeitsbereich die Funktion **Layout für die Fakturierung von Gutschriften auf Verkaufs- und Projektrechnungsberichte**. Weitere Informationen finden Sie unter [Funktionsverwaltung – Übersicht](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Die druckbaren Formate der erforderlichen Dokumente müssen in der Druckverwaltung konfiguriert werden.

Die in diesem Thema beschriebene Funktionalität gilt für die folgenden Dokumente:

**Debitorenkonten**

- Freitext-Gutschrift
- Debitorengutschrift

**Projektverwaltung und Buchhaltung**

- Projektgutschrift

## <a name="configure-accounts-receivable-parameters"></a>Debitorenparameter konfigurieren

Befolgen Sie diese Schritte, um den Parameter festzulegen, der steuert, ob Verweise auf die Originalrechnungen in zugehörigen Gutschriften gedruckt werden.

1. Gehen Sie zu **Debitoren** \> **Einrichtung** \> **Debitorenparameter**.
2. Auf der **Updates**-Registerkarte auf im Inforegister **Rechnung** stellen Sie die Option **Das Layout für die Fakturierung von Gutschriften auf Verkaufs- und Projektrechnungsberichte anwenden** auf **Ja**.

![Konfigurieren von Debitorenparametern](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a>Verweise auf Originalrechnungen definieren

Verwenden Sie die folgenden Verfahren, um Verweise auf Originalrechnungen basierend auf dem Dokumenttyp zu definieren.

### <a name="free-text-credit-note"></a>Freitext-Gutschrift

1. Wechseln Sie zu **Debitoren** \> **Rechnungen** \> **Alle Freitextrechnungen**.
2. Erstellen Sie eine neue Gutschrift oder wählen Sie eine vorhandene Gutschrift aus.
3. Öffnen Sie die Rechnung.
4. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Rechnung** in der Gruppe **Funktionen** **Fakturierung von Gutschriften** aus.
5. Geben Sie den Verweis auf die Originalrechnung ein und wählen Sie den Grund für die Korrektur aus.

![Definieren des Verweises für eine Freitextrechnung](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a>Debitorengutschrift

1. Wechseln Sie zu **Debitoren** \> **Aufträge** \> **Alle Aufträge**.
2. Wählen Sie den in Rechnung gestellten zu korrigierenden Auftrag aus und öffnen Sie ihn.
3. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Verkaufen** in der Gruppe **Gutschrift** die Option **Gutschrift**.
4. Geben Sie hier die Ursache für die Korrektur ein. Der Verweis auf die Originalrechnung wird automatisch hergestellt.

![Definieren des Verweises für einen Auftrag](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a>Projektgutschrift

1. Wechseln Sie zu **Projektverwaltung und -verrechnung** \> **Projektrechnungen** \> **Projektrechnung**.
2. Wählen Sie die zu korrigierende Projektrechnung aus und öffnen Sie sie.
3. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Projektrechnung** in der Gruppe **Funktionen** **Für Gutschrift auswählen** aus.
4. Wählen Sie **Gutschriftenfakturierung** aus.
5. Geben Sie hier die Ursache für die Korrektur ein. Der Verweis auf die Originalrechnung wird automatisch hergestellt.

![Definieren des Verweises für eine Projektrechnung](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a>Drucken von Gutschriften

Wenn Sie Freitext-, Kunden- und Projektgutschriften drucken, enthalten diese den Verweis auf die Originalrechnung und den Korrekturgrund.

![Gedruckte Gutschrift](media/credit-note-FTI.jpg)

> [!NOTE]
> Stellen Sie, davon ausgehend, dass Verweise auf Originalrechnungen gedruckt werden, sicher, dass die druckbaren Formate der Dokumente korrekt konfiguriert sind.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]