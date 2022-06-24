---
title: Verweise auf Originalrechnungen in Gutschriften
description: In diesem Artikel wird erläutert, wie Sie die ursprünglichen Rechnungsnummern in zugehörigen Gutschriften einrichten und ausdrucken.
author: ilkond
ms.date: 10/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ebfeb43aaf137ef336b460f340fbda50f5918d08
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861530"
---
# <a name="references-to-original-invoices-in-credit-notes"></a>Verweise auf Originalrechnungen in Gutschriften

[!include [banner](../includes/banner.md)]


In einigen Ländern und Regionen ist es gesetzlich vorgeschrieben, dass gedruckte Gutschriften Verweise auf die Originalrechnungen enthalten. In diesem Artikel wird erläutert, wie Sie die ursprünglichen Rechnungsnummern in zugehörigen Gutschriften einrichten und ausdrucken.

## <a name="prerequisites"></a>Voraussetzungen

- Aktivieren Sie im **Funktionsverwaltung**-Arbeitsbereich die Funktion **Layout für die Fakturierung von Gutschriften auf Verkaufs- und Projektrechnungsberichte**. Weitere Informationen finden Sie unter [Funktionsverwaltung – Übersicht](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Die druckbaren Formate der erforderlichen Dokumente müssen in der Druckverwaltung konfiguriert werden.

Die in diesem Artikel beschriebene Funktionalität gilt für die folgenden Dokumente:

**Debitorenkonten**

- Freitext-Gutschrift
- Debitorengutschrift

**Projektverwaltung und Buchhaltung**

- Projektgutschrift

## <a name="configure-accounts-receivable-parameters"></a>Debitorenparameter konfigurieren

Befolgen Sie diese Schritte, um den Parameter festzulegen, der steuert, ob Verweise auf die Originalrechnungen in zugehörigen Gutschriften gedruckt werden.

1. Gehen Sie zu **Debitoren** \> **Einrichtung** \> **Debitorenparameter**.
2. Auf der **Updates**-Registerkarte auf im Inforegister **Rechnung** stellen Sie die Option **Das Layout für die Fakturierung von Gutschriften auf Verkaufs- und Projektrechnungsberichte anwenden** auf **Ja**.

![Konfigurieren von Debitorenparametern.](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a>Verweise auf Originalrechnungen definieren

Verwenden Sie die folgenden Verfahren, um Verweise auf Originalrechnungen basierend auf dem Dokumenttyp zu definieren.

### <a name="free-text-credit-note"></a>Freitext-Gutschrift

1. Wechseln Sie zu **Debitoren** \> **Rechnungen** \> **Alle Freitextrechnungen**.
2. Erstellen Sie eine neue Gutschrift oder wählen Sie eine vorhandene Gutschrift aus.
3. Öffnen Sie die Rechnung.
4. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Rechnung** in der Gruppe **Funktionen** **Fakturierung von Gutschriften** aus.
5. Geben Sie den Verweis auf die Originalrechnung ein und wählen Sie den Grund für die Korrektur aus.

![Definieren des Verweises für eine Freitextrechnung.](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a>Debitorengutschrift

1. Wechseln Sie zu **Debitoren** \> **Aufträge** \> **Alle Aufträge**.
2. Wählen Sie den in Rechnung gestellten zu korrigierenden Auftrag aus und öffnen Sie ihn.
3. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Verkaufen** in der Gruppe **Gutschrift** die Option **Gutschrift**.
4. Geben Sie hier die Ursache für die Korrektur ein. Der Verweis auf die Originalrechnung wird automatisch hergestellt.

![Definieren des Verweises für einen Auftrag.](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a>Projektgutschrift

1. Wechseln Sie zu **Projektverwaltung und -verrechnung** \> **Projektrechnungen** \> **Projektrechnung**.
2. Wählen Sie die zu korrigierende Projektrechnung aus und öffnen Sie sie.
3. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Projektrechnung** in der Gruppe **Funktionen** **Für Gutschrift auswählen** aus.
4. Wählen Sie **Gutschriftenfakturierung** aus.
5. Geben Sie hier die Ursache für die Korrektur ein. Der Verweis auf die Originalrechnung wird automatisch hergestellt.

![Definieren des Verweises für eine Projektrechnung.](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a>Drucken von Gutschriften

Wenn Sie Freitext-, Kunden- und Projektgutschriften drucken, enthalten diese den Verweis auf die Originalrechnung und den Korrekturgrund.

![Gedruckte Gutschrift.](media/credit-note-FTI.jpg)

> [!NOTE]
> Stellen Sie, davon ausgehend, dass Verweise auf Originalrechnungen gedruckt werden, sicher, dass die druckbaren Formate der Dokumente korrekt konfiguriert sind.

## <a name="references-to-original-invoices-in-debit-notes"></a>Verweise auf Originalrechnungen in Lastschriften

Für Gutschriften können standardmäßig Verweise auf Originalrechnungen erfasst werden. Sie können beispielsweise Referenzen eingeben, wenn Sie negative (abnehmende) Korrekturen von Originalrechnungen vornehmen.

Um Referenzen bei positiven (erhöhten) Korrekturen von Originalrechnungen erfassen zu können, müssen Sie die **Verweise auf Originalrechnungen in Belastungsanzeigen**-Funktion im Arbeitsberiech **Funktionsverwaltung** aktivieren.  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
