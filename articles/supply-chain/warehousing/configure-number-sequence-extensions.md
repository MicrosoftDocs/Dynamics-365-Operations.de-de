---
title: Nummernkreise für Lagerflows konfigurieren
description: Dieses Thema bietet einen Überblick über die Funktionen, die Nummernkreiserweiterungen für Kennzeichen-IDs, Wellenetikett-IDs, Container-IDs und Frachtbrief-IDs.
author: Mirzaab
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSNumberSequenceExt
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: 20438ed3e34775a6312508595bcd32b16a37a81d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669554"
---
# <a name="configure-number-sequences-for-warehouse-flows"></a>Nummernkreise für Lagerflows konfigurieren

[!include [banner](../includes/banner.md)]

Die Funktion *Nummernkreiserweiterungen* fügt eine neue Konfigurationsseite zum Einrichten von Nummernkreisen hinzu. Sie ermöglicht die flexible Konfiguration von GS1-regulierten IDs, einschließlich GS1-Präfixen und Prüfziffern (Modulo 10), und erzwingt eine Längenbeschränkung für vorhandene Nummernkreise.

Standard-Nummernkreissegmente sind für die GS1-Implementierung nicht geeignet, da keine Prüfziffer berechnet wird und das GS1-Präfix des Unternehmens manuell aktualisiert werden muss.

Diese Funktion fügt die folgenden Funktionen hinzu:

- Frachtbrief-IDs (BOL) können im Voraus generiert werden.
- Ein eindeutiger Nummernkreis kann für Nummern der Versandeinheit (SSCC) generiert werden.
- GS1-konforme Nummernkreise können für Frachtbrief- und SSCC-Zahlen erstellt werden. Die Funktion fügt sofort einsatzbereite Unterstützung für Kennzeichen-IDs, Container-IDs, Wellenetikett-IDs und Frachtbrief-IDs hinzu.
- Die Konfiguration der Kennzeichen-ID-Nummern ist flexibel. Beispielsweise können Sie Anwendungskennungen (AI) ein- oder ausschließen, z. B. vorstehende Nullen (00).

Diese Funktionalität macht es effizienter, die Etiketten von Kartons zu unterstützen und neue Zahlen anzupassen, die vom System generiert werden.

## <a name="turn-on-the-number-sequence-extensions-feature"></a>Aktivieren Sie die Nummernkreiserweiterungs-Funktion

Bevor Sie die Funktion nutzen können, muss sie auf Ihrem System aktiviert werden. Administratoren können mit der Einstellung [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und ggf. aktivieren. Dort wird die Funktion folgendermaßen aufgelistet:

- **Module:** *Lagerortverwaltung*
- **Funktionsname:** *Nummernkreiserweiterungen*

## <a name="set-up-the-feature"></a>Die Funktion einrichten

Führen Sie die folgenden Schritte aus, um Nummernfolgenerweiterungen in Ihrem System einzurichten.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerortverwaltungsparameter**.
1. Auf der Registerkarte **Allgemein** im Feld **GS1-Unternehmenspräfix** geben Sie das GS1-Präfix Ihres Unternehmens ein. Dieser Wert wirkt sich auf alle Nummernkreise aus, in denen das GS1-Präfix als Segment enthalten ist.
1. Wenn Sie Frachtbriefnummern für Wellenetiketten generieren möchten, aktivieren Sie auf der Registerkarte **Berichte** das Kontrollkästchen **Frachtbriefnummern beim Drucken von Wellenetiketten generieren**.

    > [!NOTE]
    > Dieses Kontrollkästchen ist nur verfügbar, wenn die Funktionalität für [Wellenetikettendruck](configure-wave-label-printing.md) aktiviert ist.

1. Gehen Sie zu **Lagerortverwaltung** \> **Setup** \> **Nummernkreiserweiterungen**
1. Wählen Sie im Aktionsbereich **Standardsetup erstellen** aus. Ein GS1-kompatibler Frachtbrief-Nummernkreis und drei Typen von SSCC-Nummernkreisen werden erstellt. Alle diese Nummernkreise berücksichtigen die Länge des GS1-Präfixes Ihres Unternehmens.

    Weitere Informationen zum Anpassen dieser Standardnummernkreise und/oder zum Hinzufügen neuer Nummernkreise finden Sie im nächsten Abschnitt. Sie können jede dieser Sequenzen auch entfernen, wenn Sie sie nicht benötigen.

1. Kehren Sie zurück zu **Lagerortverwaltung \> Setup \> Lagerort-Verwaltungsparameter**.
1. Auf der Registerkarte **Nummernkreise** wählen Sie eine relevante Nummernkreiserweiterung aus, um damit Nummern für Ihre Kennzeichen-IDs, Wellenetikett-IDs, Container-IDs (in diesem Fall wählen Sie den entsprechenden **SSCC-18-Nummern**-Kreis aus) und/oder Frachtbrief-IDs (in diesem Fall wählen Sie den **Frachtbrief**-Nummernkreis aus) zu generieren. Standardmäßig werden Nummernkreisweiterungen nur für diese vier ID-Typen unterstützt.

Wenn das nächste Mal eine neue Nummer für eine dieser Nummernkreise generiert wird, wird die neue Logik verwendet.

> [!NOTE]
> Wenn Sie keine Nummernkreiserweiterung für Kennzeichen-IDs auswählen, werden die aktuellen Regeln zum Generieren von Kennzeichen-IDs verwendet. Andernfalls wird Ihr ausgewählter Nummernkreis verwendet. Die anderen IDs verwenden einen einfachen Nummernkreis, bis Sie eine Nummernkreiserweiterung für sie anwenden.

## <a name="create-and-edit-number-sequences"></a>Nummernkreise erstellen und bearbeiten

Im vorherigen Abschnitt haben Sie einen Standardsatz von Nummernkreisen generiert. In diesem Abschnitt wird erläutert, wie jeder Nummernkreis definiert wird. Außerdem wird erläutert, wie Sie benutzerdefinierte Reihenfolgen erstellen und die Standardsequenzen oder benutzerdefinierten Sequenzen bearbeiten.

Führen Sie die folgenden Schritte aus, um Nummernkreise zu erstellen und zu bearbeiten.

1. Gehen Sie zu **Lagerortverwaltung** \> **Setup** \> **Nummernkreiserweiterungen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Im Feld **Nummernkreiserweiterung** geben einen Namen für den neuen Nummernkreis ein. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
1. Im Inforegister **Segmente** verwenden Sie die Schaltflächen in der Symbolleiste, um Ihr Nummerierungsformat durch Hinzufügen, Löschen und Anordnen von Segmenten zusammenzustellen. Im Feld **Segment** für jede Zeile weisen Sie einen Segmenttyp zu, um den Zweck und Inhalt dieses Segments zu definieren. In der folgenden Tabelle werden die verfügbaren Segmenttypen beschrieben.

    | Segmenttyp | Beschreibung |
    |---|---|
    | Konstante | Dieser Segmenttyp fügt für jede generierte Zahl im Nummernkreis denselben konstanten Text hinzu. Geben Sie den Text im Feld **Wert** den erforderlichen Text ein. Das Feld **Länge** wird automatisch auf die Länge des Textes aktualisiert, den Sie in das Feld **Wert** eingegeben haben. |
    | Nummernkreis | Geben Sie im Feld **Wert** ein Nummernzeichen (*\#*) für jedes Zeichen ein, das im generierten Nummernkreis angezeigt werden soll. Der Nummernkreis selbst generiert möglicherweise längere Zahlen, es werden jedoch nur die Zeichen ganz rechts angezeigt. Das Feld **Länge** wird automatisch auf die Zahl der Nummernzeichen aktualisiert, die Sie in das Feld **Wert** eingegeben haben.<p>Stellen Sie sicher, dass die Länge dieses Segments 16 minus der Länge Ihres GS1-Präfixes beträgt, um die GS1-Anforderungen für SSCC-18-Nummern zu erfüllen.</p> |
    | GS1-Präfix | Dieser Segmenttyp fügt den Wert hinzu, der im Feld **GS1-Unternehmenspräfix** auf der Seite **Lagerort-Verwaltungsparameter** festgelegt ist. Das Feld **Wert** zeigt den Wert an, der auf der Seite **Lagerort-Verwaltungsparameter** festgelegt ist und das Feld **Länge** zeigt die Anzahl der Zeichen im Wert an. Sowohl das Feld **Wert** als auch das Feld **Länge** sind schreibgeschützt. |
    | Anwendungskennung | Im Feld **Wert** geben Sie einen Anwendungsbezeichner ein, der durch die relevante GS1-Richtlinie für diesen Typ von Nummernkreis angegeben ist. Geben Sie zum Beispiel *00* für SSCC oder *420* für Frachtbrief ein. Das Feld **Länge** wird automatisch auf die Länge des Bezeichners aktualisiert, den Sie in das Feld **Wert** eingegeben haben. |
    | Verpackungstyp | Für Elemente, die eindeutig identifiziert werden können, fügt dieser Segmenttyp einen Feldwert aus der entsprechenden Einheitsnummernkreisgruppe (von der Seite **Einheitsnummernkreisgruppen**) hinzu. (Dieses Verhalten entspricht der vorhandenen Logik für Kennzeichen-IDs.) Bei Kennzeichen, die mehrere Lagermengeneinheiten (SKUs) enthalten, fügt dieser Segmenttyp *0* (Null) standardmäßig hinzu. Für diesen Segmenttyp wird das Feld **Wert** immer auf *P* festgelegt, und das Feld **Länge** wird immer auf *1* festgelegt.|
    | Prüfziffer | Dieser Segmenttyp fügt eine Prüfziffer hinzu, bei der es sich um eine Modulo 10-Berechnung handelt. (Dieses Verhalten entspricht der vorhandenen Logik für Kennzeichen-IDs.) Für diesen Segmenttyp wird das Feld **Wert** immer auf ein Caretzeichen festgelegt (*^*), und das Feld **Länge** wird immer auf *1* festgelegt. |

1. Um ein Beispiel für Ihr endgültiges Zahlenformat anzuzeigen, überprüfen Sie das Feld **Format** am unteren Rand des Inforegisters **Segmente**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]