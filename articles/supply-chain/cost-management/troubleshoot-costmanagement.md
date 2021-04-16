---
title: Behebung von Problemen bei der Kostenverwaltung
description: Dieses Thema beschreibt, wie Sie Probleme beheben, die bei der Arbeit mit dem Kostenmanagement auftreten können.
author: AndersGirke
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: fc6a48a44a529c82c2a9ee818af95569d9bcb249
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834288"
---
# <a name="troubleshoot-cost-management"></a>Behebung von Problemen bei der Kostenverwaltung

Dieses Thema beschreibt, wie Sie Probleme beheben, die bei der Arbeit mit dem Kostenmanagement auftreten können.

## <a name="functional-gaps-between-the-inventory-valueaging-reports-and-their-storage-versions"></a>Funktionelle Lücken zwischen den Berichten über Bestandswert/Alterung und ihren Speicherversionen

Die Funktionen [Speicherung von Bestandsalterungsberichten](inventory-aging-report-storage.md) und [Speicherung von Bestandswerten](inventory-value-report-storage.md) ermöglichen es dem Supply Chain Management, große Mengen von Bestandstransaktionen anzuzeigen. In jedem Fall werden die Berichtsergebnisse zum Durchsuchen und Exportieren gespeichert, anders als bei den nicht-speicherbaren Versionen dieser Berichte. Einige Funktionen, die in den Nicht-Speicher-Versionen dieser Berichte vorhanden sind, gibt es jedoch in den Speicher-Versionen nicht. Die folgenden Unterabschnitte fassen die Unterschiede zusammen und bieten Umgehungsmöglichkeiten.

### <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>Speicherberichte enthalten keine Zwischensummen, auch wenn sie im Berichtslayout aktiviert sind

Zwischensummen können beim Exportieren des Ergebnisses zu Problemen führen, insbesondere wenn Benutzer die Sequenz der Datensätze ändern.

Um die Zwischensummen zu prüfen, können Sie das Ergebnis in Microsoft Excel exportieren. Wenn Sie die Zwischensummen innerhalb des Supply Chain Managements prüfen wollen, verwenden Sie alternativ die [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), um die Funktionen *Neue Rastersteuerung* und *Gruppierung in Rastern* zu aktivieren, die eine viel flexiblere Möglichkeit bieten, die Zwischensumme für jede Gruppe nach Spalten zu sehen. Weitere Informationen finden Sie unter [Rasterfunktionen](../../fin-ops-core/fin-ops/get-started/grid-capabilities.md).

### <a name="inventory-value-storage-report-doesnt-support-ledger-account-information"></a>Bestandswert-Speicherbericht unterstützt keine Ledger-Kontoinformationen

Sie können den Test-Saldo ausführen, um den Saldo der Bestandskonten zu erhalten und diesen mit dem **Bestandswert-Speicherung**-Bericht zu vergleichen.

## <a name="warnings-or-errors-are-shown-when-changing-a-ledger-period-status-without-closing-inventory"></a>Beim Ändern eines Ledger-Periodenstatus ohne Abschluss des Bestands werden Warnungen oder Fehler angezeigt

Microsoft hat die folgenden Überprüfungen eingeführt, um Probleme zu vermeiden, die durch einen fehlerhaften Periodenabschlussprozess rund um die Kalkulation verursacht werden. Wenn eine der folgenden Fehlermeldungen auftritt, finden Sie in [KB 4561987](https://fix.lcs.dynamics.com/Issue/Details?kb=4561987&bugId=445351&dbType=3&qc=f514f2adcddcddceec43af58c26ae8a9020effdc7cdfe085d9d0deeb8cc7b6a3) weitere Informationen zur Behebung dieser Probleme.

- Sie sind im Begriff, eine Neukalkulation mit dem Datum %1 (10.02.2019) auszuführen. Die letzte registrierte Neuberechnung wurde in einer früheren Periode mit einem Datum %2 (20.01.2019) ausgeführt. Es wurde keine Ausführung eines Bestandsabschlusses mit dem Datum %3 (31.01.2019) passend zum Periodenende registriert. Bitte denken Sie daran, einen Bestandsabschluss zum Datum %3 (31.01.2019) passend zum Periodenende auszuführen. Die Bewertung der Bestände, des Wareneinsatzes und der Abweichungen sind im Neben- oder Hauptbuch möglicherweise nicht korrekt, bis dies ausgeführt wurde.

- Sie sind dabei, den Status der Sachkontoperiode %1 auf %2 zu ändern. Es wurde keine Ausführung eines Bestandsabschlusses mit einem Datum %3, das mit dem Periodenende übereinstimmt, registriert. Bitte führen Sie einen Bestandsabschluss ab %3 passend zum Periodenende aus, bevor Sie den Status ändern. Die Bewertung der Bestände, des Wareneinsatzes und der Abweichungen sind im Neben- oder Hauptbuch möglicherweise nicht korrekt, bis dies ausgeführt wurde. Gemeldet von der juristischen Entität %4. Derzeit dient dies nur zu Informationszwecken, aber diese Aktivität wird in Zukunft erforderlich sein.

- Die Kontenstruktur %1 wurde geändert. Ein oder mehrere Hauptkonten %2 sind nicht mehr vorhanden. Diese Hauptkonten werden von der %3 mit einem Datum %4 benötigt. Bitte fügen Sie diese Hauptkonten zur Kontenstruktur %1 hinzu, bevor Sie den Auftrag %3 fortsetzen können. Derzeit dient dies nur zu Informationszwecken, aber diese Aktivität wird in Zukunft erforderlich sein.

- Sie sind dabei, einen Bestandsabschluss mit einem Datum %1 (31.01.2019) auszuführen. Es wurde keine Ausführung einer retrograden Kalkulation mit einem Datum %2 (31.01.2019) registriert, das dem Periodenende entspricht. Bitte denken Sie daran, eine Nachkalkulation mit einem Datum %3 (31.01.2019) passend zum Periodenende auszuführen. Die Bewertung der Bestände, des Wareneinsatzes und der Abweichungen sind im Neben- oder Hauptbuch möglicherweise nicht korrekt, bis dies ausgeführt wurde.

- Sie sind im Begriff, eine Nachkalkulation mit dem Datum %1 (28.02.2019) auszuführen. Die letzte registrierte Nachkalkulation wurde in einer vorherigen Periode mit einem Datum %2 (31-01-2019) ausgeführt. Es wurde keine Ausführung eines Bestandsabschlusses mit dem Datum %3 (31.01.2019) registriert, der mit einem Periodenende übereinstimmt.
Bitte denken Sie daran, einen Bestandsabschluss zum Datum %3 (31.01.2019) passend zu einem Periodenende auszuführen. Die Bewertung der Bestände, die Selbstkosten und die Abweichungen sind in der Nebenbuchhaltung oder im Hauptbuch möglicherweise nicht korrekt, bis der Bestandsabschluss ausgeführt wurde.

## <a name="inventory-aging-report-discrepancies"></a>Diskrepanzen im Bestandsalterungsbericht

Der **Bestandsalterungsbericht** zeigt unterschiedliche Werte an, wenn er in verschiedenen Dimensionen der Lagerung (z.B. Standort oder Lagerort) betrachtet wird. Weitere Informationen über die Berichtslogik finden Sie unter [Beispiele und Logik des Berichts zur Bestandsalterung](inventory-aging-report.md).

## <a name="an-update-conflict-occurs-when-the-inventory-valuation-method-is-either-standard-cost-or-moving-average"></a>Ein Aktualisierungskonflikt tritt auf, wenn als Bestandsbewertungsmethode entweder „Standardkosten“ oder „Gleitender Durchschnitt“ verwendet wird.

Wenn Sie Dokumente wie Bestandserfassungen, Einkaufsrechnungen oder Auftragsrechnungen aus Gründen der Skalierbarkeit und Leistung parallel buchen, wird möglicherweise eine Fehlermeldung zu einem Aktualisierungskonflikt angezeigt und einige der Dokumente werden möglicherweise nicht gebucht. Dieses Problem kann auftreten, wenn als Bestandsbewertungsmethode entweder *Standardkosten* oder *Gleitender Durchschnitt* verwendet wird. Beide Methoden sind kontinuierliche Nachkalkulationsmethoden. Anders ausgedrückt: Die endgültigen Kosten werden zum Zeitpunkt der Buchung festgelegt.

Wenn Sie die Methode *Gleitender Durchschnitt* verwenden, ähnelt die Fehlermeldung diesem Beispiel:

> Bestandswert xx.xx wird nach Berechnung der anteiligen Ausgaben nicht erwartet

Wenn Sie die Methode *Standardkosten* verwenden, ähnelt die Fehlermeldung diesem Beispiel:

> Die Standardkosten stimmen nicht mit dem Wert des finanziellen Bestands nach der Aktualisierung überein. Wert = xx.xx, Menge = yy.yy, Standardkosten = zz.zz

Verwenden Sie die folgenden Problemumgehungen, bis Microsoft eine Lösung zur Behebung des Problems veröffentlicht, um diese Fehler zu vermeiden oder zu reduzieren:

- Buchen Sie die fehlgeschlagenen Dokumente erneut.
- Erstellen Sie Dokumente mit weniger Positionen.
- Vermeiden Sie Dezimalwerte in den Standardkosten. Versuchen Sie, die Standardkosten so zu definieren, dass das Feld **Preismenge** auf *1* festgelegt ist. Wenn Sie einen Wert für **Preismenge** angeben müssen, der größer als *1* ist, versuchen Sie, die Anzahl der Dezimalstellen in den Standardkosten der Einheit zu minimieren. (Idealerweise sollten weniger als zwei Dezimalstellen vorhanden sein.) Vermeiden Sie beispielsweise die Definition von Standardkosteneinstellungen wie **Preis** = *10* und **Preismenge** = *3*, weil sie Standardkosten pro Einheit von 3,333333 erzeugen (wobei sich der Dezimalwert wiederholt).
- Vermeiden Sie in den meisten Dokumenten mehrere Positionen mit derselben Kombination aus Produkt- und Finanzbestandsdimensionen.
- Reduzieren Sie den Parallelisierungsgrad. (In diesem Fall wird Ihr System möglicherweise schneller, da weniger Aktualisierungskonflikte und Wiederholungsversuche auftreten.)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]