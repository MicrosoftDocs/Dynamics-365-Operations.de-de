---
title: Nummernkreisübersicht
description: Nummernkreise dienen zum Generieren von lesbaren, eindeutigen Bezeichnern für Masterdatensätze und Buchungsdatensätze, die Bezeichner benötigen.
author: MargoC
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceConfiguration
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom:
- "15461"
- intro-internal
ms.assetid: 6e19bd1d-192b-4da2-8573-84f6e1ce98ef
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1a6c7b7ee36ae1ea37842aea744fc8601f972d89
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/03/2021
ms.locfileid: "6338903"
---
# <a name="number-sequences-overview"></a>Nummernkreisübersicht

[!include [banner](../includes/banner.md)]

Nummernkreise dienen zum Generieren von lesbaren, eindeutigen Bezeichnern für Masterdatensätze und Buchungsdatensätze, die Bezeichner benötigen. Ein Masterdatensatz oder Buchungsdatensatz, der eine Kennung erfordert, wird als *Referenz* bezeichnet.

Bevor neue Datensätze für eine Referenz erstellt werden können, muss ein Nummernkreis eingerichtet und der Referenz zugeordnet werden. Es wird empfohlen, die Seiten in **Organisationsverwaltung** zum Einrichten von Nummernkreisen zu verwenden. Wenn modulspezifische Einstellungen erforderlich sind, können Sie die Seite Parameter in einem Modul verwenden, um Nummernkreise für die Referenzen in diesem Modul anzugeben. Sie können beispielsweise in **Debitoren** und **Kreditoren** Nummernkreisgruppen einrichten, um bestimmten Debitoren oder Kreditoren bestimmte Nummernkreise zuzuordnen.

Wenn Sie einen Nummernkreis einrichten, müssen Sie einen Bereich angeben, der definiert, welche Organisation den Nummernkreis verwendet. Der Bereich kann **Gemeinsam genutzt**, **Unternehmen**, **Juristische Person** oder **Organisationseinheit** sein. Die Bereiche **Juristische Person** und **Unternehmen** können auch mit **Steuerkalenderperiode** kombiniert werden, um noch spezifischere Nummernkreise zu erstellen.

Nummernkreisformate werden aus Segmenten gebildet. Nummernkreise, die einen anderen Bereich als **Gemeinsam genutzt** besitzen, können Segmente enthalten, die dem Bereich entsprechen. Ein Nummernkreis mit dem Bereich **Juristische Person** kann beispielsweise ein Segment für juristische Personen enthalten. Durch Einfügen eines Bereichssegments in das Nummernkreisformat können Sie den Bereich eines bestimmten Datensatzes anhand seiner Nummer feststellen.

Neben den Segmenten, die Bereichen entsprechen, können Nummernkreisformate die Segmente **Konstante** und **Alphanumerische Segmente** enthalten. Ein Segment vom Typ **Konstante** enthält eine Gruppe von Buchstaben, Zahlen oder Symbolen, die unverändert bleiben. Ein Segment vom Typ **Alphanumerisch** enthält eine Gruppe von Buchstaben oder Zahlen, die jedes Mal schrittweise erhöht werden, wenn eine Nummer aus dem Nummernkreis verwendet wird. Verwenden Sie ein Nummernzeichen (\#) zur Angabe inkrementeller Nummern und ein kaufmännisches Und-Zeichen zur Angabe inkrementeller Buchstaben. Mit dem Format \#\#\#\#\#\_2017 wird beispielsweise der Nummernkreis 00001\_2017, 00002\_2017 usw. erstellt.

## <a name="number-sequence-examples"></a>Nummernkreisbeispiele

Die folgenden Beispiele zeigen, wie Segmente verwendet werden, um Nummernkreisformate zu erstellen. Insbesondere verdeutlichen die Beispiele, welche Auswirkungen das Verwenden von Bereichssegmenten hat.

### <a name="expense-report-numbers"></a>Spesenabrechnungsnummern

Im folgenden Beispiel werden Spesenabrechnungsnummern für die juristische Person mit dem Titel **CS** eingerichtet.

- **Bereich:** Reisekosten und Ausgaben
- **Referenz:** Ausgaben-Berichtsnummer
- **Umfang:** Juristische Person
- **Juristische Person:** CS

| Segmente  | Segmenttyp | Wert     |
|-----------|--------------|-----------|
| Segment 1 | Juristische Person | CS        |
| Segment 2 | Konstante     | -SPESEN- |
| Segment 3 | Alphanumerisch | \#\#\#\#  |

**Beispiel für formatierte Nummer**: CS-SPESEN-0039

Sie können ein ähnliches Nummernkreisformat für andere juristische Personen einrichten. Beispiel: Wenn Sie für eine juristische Person namens **RW** nur den Wert des Segments für die juristische Person ändern, lautet die formatierte Nummer RW-SPESEN-0039. Sie können auch das gesamte Nummernkreisformat für andere juristische Personen ändern. Sie können beispielsweise das Bereichssegment für die juristische Person auslassen, um eine formatierte Nummer zu erstellen, beispielsweise SPESEN-0001.

### <a name="sales-order-numbers"></a>Auftragsnummern

Im folgenden Beispiel werden Auftragsnummern für die Unternehmenskennung **CEU** eingerichtet.

- **Bereich:** Verkäufe
- **Referenz:** Verkaufsauftrag
- **Umfang:** Unternehmen
- **Unternehmen:** CEU

| Segmente  | Segmenttyp | Wert    |
|-----------|--------------|----------|
| Segment 1 | Konstante     | AU-      |
| Segment 2 | Alphanumerisch | \#\#\#\# |

**Beispiel für formatierte Nummer**: SO-0029

Auch wenn das Format kein Bereichssegment enthält, beginnt die Nummerierung für jede Unternehmenskennung erneut. Wenn Sie dasselbe Format für alle Unternehmenskennungen verwenden, werden in allen Unternehmen dieselben Zahlen verwendet. Beispielsweise wird in jedem Unternehmen die Auftragsnummer AU-0029 verwendet. Sie können auch das gesamte Nummernkreisformat für andere Unternehmenskennungen ändern.

### <a name="purchase-requisition-numbers"></a>Bestellanforderungsnummern

Im folgenden Beispiel werden Bestellanforderungsnummern organisationsweit verwendet.

- **Bereich:** Einkauf
- **Referenz:** Einkaufspreis
- **Umfang:** Geteilt

| Segmente  | Segmenttyp | Wert    |
|-----------|--------------|----------|
| Segment 1 | Konstante     | BestAnf      |
| Segment 2 | Alphanumerisch | \#\#\#\# |

**Beispiel für formatierte Nummer**: Req0052

Da der Umfang **Geteilt** ist, wird das Nummernsequenzformat in der gesamten Organisation verwendet. Sie können für verschiedene Bereiche der Organisation nicht verschiedene Nummernkreisformate verwenden.

## <a name="performance-considerations-for-number-sequences"></a>Leistungsüberlegungen für Nummernkreise

Berücksichtigen Sie vor dem Einrichten von Nummernkreisen die folgenden Informationen, die Aufschluss darüber eben, wie sich die Konfiguration von Nummernkreisen auf die Systemleistung auswirken kann.

### <a name="continuous-and-non-continuous-number-sequences"></a>Fortlaufende bzw. nicht fortlaufende Nummernkreise

Nummernkreise können fortlaufend bzw. nicht fortlaufend sein. Bei einem fortlaufenden Nummernkreis werden keine Zahlen übersprungen, aber Zahlen werden ggf. nicht sequentiell verwendet. Zahlen aus einem nicht fortlaufenden Nummernkreis werden sequenziell verwendet, aber der Nummernkreis kann Zahlen überspringen. Beispiel: Ein Benutzer storniert eine Buchung. In diesem Fall wird eine Nummer generiert, aber nicht verwendet. In einem fortlaufenden Nummernkreis wird diese Nummer später recycelt. In einem nicht fortlaufenden Nummernkreis wird diese Nummer nicht verwendet.

Fortlaufende Nummernkreise sind normalerweise für externe Dokumente erforderlich, beispielsweise für Bestellungen, Aufträge und Rechnungen. Fortlaufende Nummernkreise können sich jedoch negativ auf die Antwortzeiten des Systems auswirken, da das System jedes Mal, wenn ein Dokument oder ein Datensatz angelegt wird, eine Nummer aus der Datenbank anfordern muss.

Wenn Sie einen nicht fortlaufenden Nummernkreis verwenden, können Sie auf der Seite **Nummernkreise** auf dem Inforegister **Leistung** die Option **Vorabzuordnung** aktivieren. Wenn Sie eine Menge von vorab zugeordneten Nummern angegeben, wählt das System diese Nummern aus und speichert sie im Arbeitsspeicher. Neue Nummern werden nur aus der Datenbank angefordert, nachdem die vorab zugewiesenen Nummern verbraucht wurden.

Sofern nicht vorgeschrieben ist, fortlaufende Nummernkreise zu verwenden, wird empfohlen, aus Leistungsgründen nicht fortlaufende Nummernkreise zu verwenden.

### <a name="automatic-cleanup-of-number-sequences"></a>Automatische Bereinigung von Nummernkreisen

Bei einem Stromausfall, Anwendungsfehler oder einem anderen unerwarteten Problem kann das System die Nummern für fortlaufende Nummernkreise nicht automatisch recyceln. Sie können den Bereinigungsprozess manuell oder automatisch ausführen, um die verloren gegangenen Nummern wiederherzustellen.

Berücksichtigen Sie aber die Serverauslastung, wenn Sie den Bereinigungsprozess planen. Es wird empfohlen, die Bereinigung außerhalb der Spitzenzeiten als Stapelverarbeitungslauf auszuführen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]