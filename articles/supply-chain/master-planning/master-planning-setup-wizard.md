---
title: Produktprogrammplanungs-Setup-Assistent
description: Dieses Thema beschreibt die verschiedenen wichtigen Strategien und Parameter, die zum Einrichten der Produktprogrammpläne verwendet werden.
author: t-benebo
ms.date: 10/21/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 26dea90a208eddc39b9a92d534fbc3a5242da29f4839a7f0e427b0efb03701b9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767459"
---
# <a name="master-planning-setup-wizard"></a>Produktprogrammplanungs-Setup-Assistent

[!include [banner](../includes/banner.md)]

Dieses Thema enthält eine Anleitung für den **Produktprogrammplanungssetupassistent**. Es wird erläutert, wie Parametervorschläge berechnet werden und sie enthalten auch Beispiele, wie verschiedene Unternehmen Produktprogrammplanung einrichten, basierend auf den Geschäftsanforderungen.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3YnSB]

Der Einrichtungs-Assistent für [Hauptpläne in Dynamics 365 Supply Chain Management](https://youtu.be/c-e6n-8rZb4) Video (oben angezeigt) ist in der [Finance and Operations Wiedergabeliste](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) in YouTube verfügbar.


## <a name="specific-requirements-of-your-company"></a>Bestimmte Unternehmensanforderungen

Die erste Seite des Assistenten fragt nach bestimmten Anforderungen Ihres Unternehmens. Ihre Antworten auf diese Fragen müssen nicht genau sein, aber Sie sollten in der Lage sein, eine grobe Form der voraussichtlichen Anzahl von Artikeln und der Bestellvorschläge bereitzustellen, die für die juristische Person sind. Ihre Antworten werden verwendet, um Parameter, die für Ihre juristische Personen gelten, nicht nur in den Produktprogrammplan zu konfigurieren, den Sie ausgewählt haben. In den folgenden Abschnitten werden die Parameter beschrieben, die berechnet werden und die Formeln, die verwendet werden.

### <a name="number-of-threads"></a>Anzahl der Threads

- **Bei der Produktion eines dieser Elemente:** Anzahl der Threads = Anzahl der geplanten Bestellungen ÷ 1.000
- **Bei der Produktion eines dieser Elemente:** Anzahl der Threads = Anzahl der Elemente ÷ 1.000

Wenn die Anzahl der Threads, die berechnet wird, 75 Prozent der verfügbaren Anzahl von Threads übersteigt, wird sie bei 75 Prozent der Anzahl von Threads gekürzt, die für jeden Kunden verfügbar sind. (Die Anzahl der verfügbaren Threads wird für jeden Debitor bestimmt).

Weitere Informationen finden Sie unter [Anzahl Threads](/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-threads).

### <a name="bundle-size"></a>Paketgröße

Die Bündelgröße wird auf **1** festgelegt. Dieser Wert ist oft der beste Werte, weil er hilft, die Leistung der Produktprogrammplanung zu verbessern.

Weitere Informationen finden Sie unter [Anzahl der Aufgaben im Hilfsaufgabenbündel](/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-tasks-in-helper-task-bundle).

### <a name="firming-bundle-size"></a>Feste Bündelgröße

- **WEnn Sie einen der Artikel herstellen:** Die feste Bündelgröße wird auf den größeren der beiden Werte festgelegt: **10** und die Bündelberechnung
- **Wenn Sie keinen der Artikel herstellen:** Die feste Bündelgröße wird auf den größeren der beiden Werte festgelegt: **50** und die Bündelberechnung

Bündelberechnung = (Anzahl der Bestellvorschläge × (Sofortanlagezeitraum ÷ Planungszeitraum) ÷ Anzahl Threads) ÷ 10

### <a name="cache-size"></a>Cachegröße

Die Cachegröße wird auf **Maximum** festgelegt. Dieser Wert ist oft der beste Werte, weil er hilft, die Leistung der Produktprogrammplanung zu verbessern.

Weitere Informationen finden Sie unter [Weisen Sie Zeit den Einzelvorgängen im einen zu Einzelvorgangsbündel zu](/dynamics365/unified-operations/supply-chain/production-control/allocate-time-jobs-job-bundle).

### <a name="manufacturing-setup"></a>Produktion einrichten

Wenn Sie Artikel erstellen, wird eine Seite **Fertigungseinstellung** später im Assistenten angezeigt.

## <a name="scope-of-the-current-plan"></a>Umfang des aktuellen Plans

Auf der Seite **Bereich des aktuellen Plans** den Assistenten beantworten Sie Fragen, die sich darauf beziehen, wie weit zukünftig verschiedene Anforderungen in der Produktprogrammplanung berücksichtigt und berechnet werden. Jede Frage erkundigt sich, ob Sie eine Funktion verwenden und wie Sie diese konfigurieren möchten.

Für die Absatzplanfunktion fragt der Assistent „Möchten Sie einen Absatzplan in der Produktprogrammplanung verwenden, damit Bestellvorschläge verwendet werden, um den geplanten Bedarf zu decken?“

Die folgenden Optionen sind verfügbar:

- **Nein** – Bestellvorschläge schlägt Produktprogrammplanung nicht vor, eine Planung zu erfüllen. Auf der Registerkarte **Planungszeiträume** auf der Seite **Produktprogrammpläne** (**Produktprogrammplanung \> Einstellungen \> Pläne \> Produktprogrammpläne**), legt der Assistent die Option **Absatzplan Planungszeitraum ()** auf **Ja** fest und setzt die Anzahl von Tagen auf **0** (null). Diese Einstellung setzt den Planungszeitraum außer Kraft, der in der Dispositionssteuerungsgruppe angegeben wurde. Da die Anzahl der Tage auf **0** (Null) festgelegt ist, wird die Funktion nicht verwendet.
- **Ja, wie in diesem definierten Produktprogrammplan definiert** – Ein Feld ist verfügbar, wo Sie die Anzahl von Tagen eingeben können, die die Produktprogrammplanung vorschlägt, um den geplanten Bedarf zu decken. Der Assistent legt die Option **Produktprogrammpläne (Produktprogrammplanung)** auf **Ja** fest und definiert die Anzahl Tage für die Anzahl der Tage, die im Feld **Absatzplanung** auf der Registerkarte **Planungszeitraum** auf der Seite **Produktprogrammpläne** eingegeben werden. Diese Einstellungen werden die Werte angegeben, die in Dispositionssteuerungsgruppen festgelegt werden.
- **Ja, wie in der Disposition festgelegt** – Der Assistent legt die Option **Absatzplan (Planungszeitraum)** auf **Nein** fest. Die Planungszeiträume, die in der Dispositionssteuerungsgruppe angegeben werden, werden verwendet, um anzugeben, wie lange Sie für die Planung brauchen.

Die verbleibenden Fragen zu dieser Seite und ihre Antworten folgen dem gleichen Schema:

- **Nein** – Die Option **Absatzplan (Planungszeitraum)** wird auf **Ja** festgelegt, und die Anzahl von Tagen wird auf **0** (null) festgelegt.
- **Ja, wie in diesem Produktprogrammplan festgelegt** – Der Assistent legt die Option **Absatzplan (Planungszeitraum)** auf **Nein** fest. Die Anzahl von Tagen, die Sie eingeben, wird verwendet und setzt die Werte außer Kraft, die in der Dispositionssteuerungsgruppen festgelegt werden.
- **Ja, wie in der Dispositionssteuergruppe festgelegt** – Der Assistent legt die Option **Absatzplan (Planungszeitraum)** auf **Nein** fest.

Weitere Informationen finden Sie unter [Feinterminierung](/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).

## <a name="scheduling-options"></a>Terminierungsoptionen

Die Seite **Planungsoptionen** wird nur angezeigt, wenn Sie **Ja** beantworteten auf die Frage „Sie erstellen einen der geplanten Artikel?“ auf der ersten Seite des Assistenten.

Ihre Antwort zur ersten Frage auf dieser Seite (Müssen Sie Arbeitsgänge planen, die in individuelle Einzelvorgänge aufgeteilt werden?) ist ausschlaggebend für die Planungsmethode auf der Registerkarte **Allgemeines** der Seite **Produktprogrammpläne**.

- **Ja** – Feinterminierung wird verwendet.
- **Nein** – Grobterminierung wird verwendet.

Weitere Informationen finden sie unter [Grobterminierung](/dynamics365/unified-operations/supply-chain/production-control/operations-scheduling) und [Feinterminierung](/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).

## <a name="updates-of-demand-and-supply"></a>Aktualisierungen von Nachfrage und Angebot

Die Fragen zur Seite **Aktualisierungen der Nachfrage und des Angebotes** werden dem Umwandeln, den Aktivitätsmeldungen und den Verzögerungen zugeordnet.

Die Produktprogrammplanungseinstellung wird auf Grundlage Ihrer Antworten gemäß dem gleichen Schema aktualisiert, das im vorherigen Abschnitt beschrieben wird:

- **Nein** – Die Option **Absatzplan** auf der Seite **Planungszeitraum** wird auf **Ja** festgelegt, und die Anzahl von Tagen wird auf **0** (null) festgelegt.
- **Ja, wie in diesem Produktprogrammplan festgelegt** – Der Assistent legt die Option **Absatzplan** auf **Ja** fest. Die Anzahl von Tagen, die Sie eingeben, wird verwendet und setzt die Werte außer Kraft, die in der Dispositionssteuerungsgruppen festgelegt werden.
- **Ja, wie in der Dispositionssteuergruppe festgelegt** – Der Assistent legt die Option **Absatzplan** auf **Nein** fest.

Bei berechneten Verzögerungen werden Ihre Antworten auf Fragen im Assistenten die entsprechenden Parameter auf der Registerkarte **Berechnete Verzögerungen** der Seite **Produktprogrammpläne** aktualisieren.

## <a name="summary-of-your-changes"></a>Zusammenfassung Ihrer Änderungen

Die letzte Seite des Assistenten zeigt die Änderungen an, die auf Grundlage Ihrer Antworten empfohlen werden. Sie gibt den Wert in vorgenommenen Einstellungen (**Aktuelle Einstellungen**) sowie den Wert an, für den der Assistent empfiehlt (**Neue Konfiguration**).

Sie können die Parameter im Formular neue Konfiguration auch ändern. Die Parameter werden in Parameter getrennt, die Ihre juristischen Personen und Parameter betreffen, die nur für den Produktprogrammplan gelten, den Sie ausgewählt haben. Um alle Einstellungsparameter anzuzeigen die geändert werden können unter Verwendung des Assistenten wählen Sie **Alle Parameter anzeigen** im unteren Bereich der Seite aus. Sie können die Parameter anschließend ändern.

Wenn Sie **Fertig stellen** auswählen, wird die neue Konfiguration angewendet. Wenn Sie **Abbrechen** auswählen, werden keine der Änderungen übernommen.

## <a name="examples"></a>Beispiele

In diesem Abschnitt wird die Einrichtung der zwei fiktiven Unternehmen beschrieben, um anzuzeigen, wie die Einstellungen gemäß den Anforderungen jedes Unternehmens geändert werden kann.

### <a name="example-1-contoso-manufacturer"></a>Beispiel 1: Contoso-Hersteller

Der Contoso-Hersteller ist ein Unternehmen, das Lautsprecher erzeugt. Es kauft die verschiedenen Rohmaterialien und Komponenten, die für verschiedene Lieferanten für die endgültigen Lautsprecher verwendet werden. Nachfolgend sind einige der Merkmale der Lieferung und Fertigung:

- Die letzten Artikel, die das Unternehmen erstellt hat, hat eine Stückliste (BOM)- Struktur.
- Alle Artikel und endgültigen Komponenten werden von der Produktprogrammplanung geplant. Manuelle Planung wird nicht ausgeführt.
- Ein Arbeitsplan von Arbeitsgängen wird für die Endproduktion eines Artikels definiert.
- Die Produktionseinrichtung produkziert die letzten Artikel. Es wurde eine definierte Nummer von Mahl- und Bohrmaschinen bestimmt, die verwendet wird, um die Komponenten zu verarbeiten. Die verschiedenen Komponenten müssen von diesen Maschinen verarbeitet werden.
- Es gibt viele Lieferanten. Die durchschnittliche Durchlaufzeit für Artikel ist eine Woche. Eine Gruppe Artikel vom gleichen Lieferanten hat eine Lieferzeit von sieben Wochen.

Im Assistenten werden die folgenden Werte für den Contoso-Hersteller eingegeben:

- **Disposition:**

    - „**Frage:** Möchten Sie die Anzahl der Tage des Planungshorizontes angeben?“
    - **Antwort:** „Ja, wie in den Dispositionssteuerungsgruppen definiert“.

    Da die Lieferzeit für Artikel sehr unterschiedlich ist, muss Contoso noch nicht alle Artikel für die gleiche Periode in der Zukunft planen. Dispositionssteuerungsgruppen für die Artikel, die erstellt werden. Artikel, die ähnliche Lieferzeiten haben, werden der gleichen Dispositionssteuerungsgruppe zugeordnet. Der Planungshorizont für jede Dispositionssteuerungsgruppe (das heißt, der Planungszeitraum) stellt die ungefähre Lieferzeit plus eine Marge von einer Woche dar. Produktprogrammplanung stellt dann sicher, dass die Artikel im Voraus geplant sind, auf Grundlage der Lieferzeit.

    Daher werden zwei Dispositionssteuerungsgruppen für dieses Beispiel erstellt. Eine Dispositionssteuerungsgruppe hat den Planungszeitraum von zwei Wochen, und die andere den Planungszeitraum von acht Wochen.

    Wenn **Ja, wie in diesem definierten Produktprogrammplan** als Antwort aktiviert ist, soll die Anzahl der Tage, die erreicht wird, die längste Lieferzeit aller Artikel überschreiten. Da allerdings zahlreiche Artikel nicht bis jetzt im Voraus eingeplant werden müssen, werden viele Bestellvorschläge berechnet aber nie verwendet. Daher steigt die Ausführungszeit der Produktprogrammplanung.

- **Terminplanung:**

    - **Frage:** „Müssen Tätigkeiten in einzelne Aufgaben aufgeteilt geplant werden?“
    - **Antwort:** „Ja.“

    Der Contoso-Hersteller muss für einzelne Aufgabengebiete planen und geplant werden, die im Fertigungsbereich ausgeführt werden. Daher wird die Feinterminierung verwendet.

- **Kapazität:**

    - **Frage:** „Sie möchten den Zeitplan mithilfe der Kapazität von Ressourcen planen“?
    - **Antwort:** „Ja, wie in diesem Produktprogrammplan definiert.“ **10 Tage** wird eingegeben.

    Die Anzahl von Mahl- und Bohrmaschinen ist beschränkt. Produktionsplanung muss diese Einschränkung berücksichtigen und Einzelvorgänge in der Zeit entsprechend der Kapazität der Ressourcen anordnen. Das bedeutet, dass die geplanten Einzelvorgänge basierend auf den Einschränkungen für die Ressourcen neu geplant werden. Planung verwendet die Lieferzeit zusätzlich zur Periode, die definiert wird. (Geplante Produktionsaufträge können sich überschneiden.) Da die Vorlaufzeit der Produktion für die Artikel mit sieben Tage angegeben ist, ist die Kapazität der Ressourcen für die Produktprogrammplanung für 10 Tage berücksichtigt.

- **Abfolge:**

    - **Frage:** „Wollen Sie die Bestellvorschläge mithilfe der Nummernkreiswerte des Produkts anordnen?“
    - **Antwort:** „Ja, wie in den Dispositionssteuerungsgruppen definiert“.

    Ein Arbeitsplan wird für die Endproduktion eines Artikels definiert. Daher wird die Produktprogrammplanung Aufträge in zeitlicher Abfolge gemäß den festgelegten Arbeitsplänen planen.

- **Simultanplanungszeitraum:**

    - **Frage:** „Möchten Sie Aufträge für alle Elemente in einer Stückliste (Plan für das übergeordnete Element und alle untergeordneten Elemente) planen?“
    - **Antwort:** „Ja, wie in den Dispositionssteuerungsgruppen definiert“.

    Alle Artikel, die für die Produktion verwendet werden, müssen geplant werden. Da die Artikel verschiedene Lieferzeiten haben, hat die Produktprogrammplanung eine bessere Leistung, wenn sie die Dispositionssteuerungsgruppen verwendet. Wieder kann eine Marge für eine Woche eingegeben werden, und die Auflösung kann gleichzeitig wie die Disposition ausgeführt werden.

### <a name="example-2-contoso-retailer"></a>Beispiel 2: Contoso-Einzelhändler

Der Contoso-Einzelhändler ist ein Vertriebsunternehmen in der Modeindustrie. Es verwendet Produktprogrammplanung, wenn Bestellungen hinzugefügt werden sollen, basierend auf den geplanten Verkäufen. Nachfolgend sind einige der Merkmale:

- Der Contoso-Einzelhändler verwendet eine Bedarfsplanung, um Verkäufe vorherzusagen. Bestellungen werden entsprechend der Planung geplant.
- Geschäfte verwenden Anforderungen für die Wiederbeschaffung.
- Die Lieferzeit vom Hauptlagerort in jedes Geschäft dauert ungefähr zwei Wochen für alle Artikel.

Im Assistenten werden die folgenden Werte für den Contoso-Einzelhändler eingegeben:

- **Geplanter Bedarf:**

    - **Frage:** „Möchten Sie einen Absatzplan in der Produktprogrammplanung verwenden, damit Bestellvorschläge vorgeschlagen werden, um den geplanten Bedarf zu decken?“
    - **Antwort:** „Ja, wie in diesem Produktprogrammplan definiert.“

    Contoso hat eine Bedarfsplanung einbezogen, um den Verkauf zu ermöglichen. Daher muss die Produktprogrammplanung Bestellvorschläge empfehlen, um die Planung zu erfüllen.

- **Umwandeln:**

    - **Frage:** „Soll die Produktprogrammplanung automatisch die geplanten Aufträgen fest einplanen, z.B. in die Produktion oder in Bestellungen?“
    - **Antwort:** „Ja, wie in diesem Produktprogrammplan definiert.“ **1 Tag** wird eingegeben.

    Da der Contoso-Einzelhändler Bestellungen direkt aus der geplanten Einkaufsbestellungen erstellt wird, ist es von Vorteil, wenn die geplanten Einkaufsbestellungen automatisch umgewandelt werden. Da das Unternehmen die Produktprogrammplanung jeden Tag ausführt, wird ein Sofortanlagezeitraum von einem Tag automatisch alle Aufträge umwandeln, die für den nächsten Tag benötigt werden.

- **Genehmigte Anforderungen:**

    - **Frage:** „Möchten Sie auf der Grundlage genehmigter Anforderungen Nachfrage einschließen, um die Geschäfte zu beliefern?“
    - **Antwort:** „Ja, wie in diesem Produktprogrammplan definiert.“ **1 Tag** wird eingegeben.

    Contoso verwendet die genehmigten Anforderungen von den enthaltenen Ladengeschäften, um geplante Einkaufsbestellungen zu erstellen, um diese Geschäfte zu beliefern. Da die Produktprogrammplanung jeden Tag ausgeführt wird, sind die Anforderungen vom letzten Tag in der Planung enthalten.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]