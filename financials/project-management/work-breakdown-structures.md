---
title: "Projektstrukturpläne"
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23861
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 1666691ec122e65128b74056817a0c40551f49b5
ms.lasthandoff: 03/31/2017


---

# <a name="work-breakdown-structures"></a>Projektstrukturpläne

[!include[banner](../includes/banner.md)]




Projektstrukturpläne: Ein Projektstrukturplan (PSP) ist eine Beschreibung der Arbeit, die für ein Projekt ausgeführt wird. Sie ist eine Hierarchie von Aufgaben, die das Verständnis des Projektteams zur Zusammenstellung der Arbeit und die Größe, Kosten und Dauer der einzelnen Komponenten oder Aufgaben darstellt. Ein PSP hat drei wichtige Funktionen:

-   Beschreiben der Aufschlüsselung oder die Zusammenstellung der Arbeit in Aufgaben.
-   Planen der Projektarbeit
-   Vorkalkulieren der Kosten jeder Aufgabe.

Der erforderliche Genauigkeit in einem PSP hängt vom Ebene der Genauigkeit ab, die für die Vorkalkulationen erforderlich ist und von der Nachverfolgung, die für diese Vorkalkulationen erforderlich ist. Projekte, die eine niedrige Toleranz für Planungs- oder Kostenverschiebungen haben, erfordern normalerweise einen ausführlicheren PSP und eine sorgfältigere Nachverfolgung des Arbeitsstatus und der Kosten gegen den PSP. Diese Art von Projekten treten häufig in der Bau- und Konstruktionsbranche auf. 

Projekte in Branchen wie Medien und Werbung, Software und IT-Infrastruktur sind recht ähnlich. Die Produktivität hängt von der Erfahrung und der Kompetenz der Person ab, die die Aufgabe ausführen wird. Daher verwenden diese Branchen einen PSP, um eine Näherung der Größe eines Projekts abzurufen statt den Status des Projekts detailliert zu verfolgen. 

Das Einrichten eines PSP ist ein intensiver Prozess, der normalerweise über eine lange Zeitspanne geleistet wird und der die Zusammenarbeit und Informationen einer breiten Palette von Personen erfordert. In diesem Thema wird beschrieben, wie Sie PSP-Erweiterungen in Microsoft Dynamics 365 for Operations verwenden können, um die Bedingungen für die Vorkalkulationen und Nachverfolgung zu erfüllen.

## <a name="prerequisites-for-creating-a-wbs"></a>Voraussetzungen für die Erstellung eines PSP
Um einen PSP zu erstellen, müssen Sie in der Lage sein, einen Arbeitsplan zu erstellen und die Kosten der Arbeit zu bewerten.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Voraussetzungen für das Erstellen eines Arbeitsplans

Damit Sie die vollständigen Planungsfunktionen der PSP-Funktionen nutzen können, führen Sie die folgenden Einrichtungen aus:

1.  Richten Sie einen Standardkalender und einen Projektkalender ein:
    1.  Klicken Sie auf **Projektverwaltung und -buchhaltung** &gt; **Einstellungen** &gt; **Planung**. Wählen Sie im Feld **Standardmäßiger Arbeitskalender** einen Standardkalender aus. Dies ist der standardmäßige Arbeitskalender für jedes neue Projekt, das erstellt wird.
    2.  Sie können den Standardkalender für ein bestimmtes Projekt ändern. Klicken Sie auf die Detailseite des Projekts und dann auf das **Projektteam und Planung**-Inforegister, aktualisieren Sie das **Planungskalender**-Feld, indem Sie einen anderen Kalender auswählen.

2.  Richten Sie Standardwerktage und Arbeitsstunden ein. Der Kalender, den Sie als Arbeitskalender für Ihr Projekt im PSP einrichten, wird verwendet werden, um die folgenden Informationen festzulegen:

-   Arbeitstage und Urlaubszeiten
-   Die Anzahl von Arbeitsstunden in einem Tag

Um die Arbeitstage und die Arbeitsstunden für einen Kalender einzurichten, oder einen neuen Kalender zu erstellen, klicken Sie auf **Organisationsverwaltung** &gt; **Allgemein** &gt; **Kalender**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Voraussetzungen zur Vorkalkulation der Kosten der Arbeit

Damit die vollständigen Vorkalkulationsfunktionen des PSP verwendet werden können, richten Sie Kosten und Verkaufspreise für Arbeitskräfte, Arbeitskategorien, Ausgaben, Gebühren und Artikel ein.

-   Um die Kosten und den Verkaufspreis der Arbeit, die Ausgaben und die Gebührenkategorien einzurichten, klicken Sie auf **Projektverwaltung und -buchhaltung** &gt; **Einstellungen** &gt; **Preise**.
-   Um die Kosten und den Verkaufspreis von Artikeln einzurichten, verwenden Sie die **Handelsvereinbarungen **-Seite für jeden Artikel auf der **Freigegebene Produkte**-Listenseite im Produkt-Informationsmanagement.

## <a name="creating-a-wbs"></a>Erstellen eines PSP
Die Erstellung eines PSP umfasst drei Aktivitäten:

1.  **Arbeitsaufschlüsselung** - Erstellen einer Aufschlüsselung der Arbeit in überschaubare Ausschnitte oder in Aufgaben.
2.  **Arbeitsplanung** - Vorkalkulieren der Zeit, die benötigt wird, um eine Aufgabe auszuführen, Festlegen von Aufgabenabhängigkeiten und Auswählen des Start- und Enddatums für die Aufgaben.
3.  **Kostenvorkalkulation** - Vorkalkulationskosten für jede Aufgabe.

In den folgenden Abschnitten wird erläutert, wie die PSP-Funktionen Sie bei diesen Aktivitäten unterstützen können.

### <a name="work-decomposition"></a>Arbeitsaufschlüsselung

Eine Aufschlüsselung der Arbeit ist normalerweise der erste Schritt beim Erstellen eines PSP. Die PSP-Funktionen unterstützen die folgenden grundlegenden Projektstrukturen und Aufschlüsselungen. 

**Projektstammaufgabe** Die Projektstammaufgabe ist die zusammenfassende Aufgabe der obersten Ebene für ein Projekt. Alle anderen Projektaufgaben werden ihr untergeordnet erstellt. Der Name der Stammaufgabe wird immer auf den Projektnamen festgelegt. Der Aufwand, die Datumsangaben und die Dauer des Stammknotens fassen die Werte für die Aufgaben unter der Stammaufgabe zusammen. Sie können die Eigenschaften des Stammknotens nicht ändern oder löschen.

**Zusammenfassung- oder Containeraufgaben** Eine zusammenfassende Aufgabe ist eine Aufgabe, die untergeordnete Aufgaben hat oder der einzelne Aufgaben zugeordnet sind. Eine zusammenfassende Aufgabe hat selbst keine Arbeitseinsatz oder Kosten. Stattdessen betragen der Arbeitseinsatz und die Kosten einer Zusammenfassungsaufgabe die Summe des Arbeitseinsatzes und Kosten ihrer konstituierend Aufgaben. Das früheste Startdatum der konstituierend Aufgaben wird als Startdatum der Zusammenfassungsaufgabe verwendet, und das Enddatum der konstituierend Aufgaben wird als Enddatum verwendet. Sie können den Namen einer Zusammenfassungsaufgabe ändern, aber Sie können die Planungseigenschaften für den Aufwand, die Datumsangaben und die Dauer nicht ändern. Wenn Sie eine zusammenfassende Aufgabe löschen, werden auch alle zugehörigen konstituierend Aufgaben gelöscht. 

**Blattknotenaufgaben** Eine Blattknotenaufgab stellt das präziseste Arbeitspaket im Projekt dar. Ein Blattknoten hat einen vorkalkulierten Aufwand, eine geplante Anzahl an Ressourcen, ein geplantes Start- und Enddatum und eine Dauer. 

Sie können die folgenden Hierarchiearbeitsgänge abschließen, um die Erstellung einer Arbeitshierarchie oder Aufschlüsselung für ein Projekt zu ermöglichen. 

**Neue Aufgabe** Jede neue Aufgabe, die Sie erstellen, wird automatisch unter dem Stammknoten erstellt und es wird automatisch eine PSP-Nummer zugewiesen. Die PSP-Nummer stellt die Bearbeitungsebene in der Hierarchie dar. Für Aufgaben in der ersten Ebene unter der Projektstammaufgabe, wird ein Nummerierungsschema von 1, 2, 3, usw. verwendet. Für Aufgaben unter der ersten Ebene wird ein Nummerierungsschema von 1.1, 1.2, 1.3, usw. verwendet. Für jede Ebene, die unter einer vorherigen Ebene hinzugefügt wird, werden neuen Unternummern hinzugefügt. 

So können Sie die PSP-Nummerierung zurzeit nicht anpassen. 

**Herunterstufen von Aufgaben** Wenn Sie eine Aufgabe herunterstufen, wird diese zum untergeordneten Element der Aufgabe, die ihr vorangeht. Die PSP-Nummer der neuen untergeordneten Aufgabe wird automatisch anhand der PSP-Nummer ihres neuen übergeordneten Artikels neu berechnet. Die übergeordnete Aufgabe ist jetzt ein Zusammenfassung- oder Containeraufgabe und wird daher zu einer konstituierenden Aufgabe. 

> [!NOTE] 
> Wenn Sie Aufgaben unterhalb einer Aufgabe verschieben möchten, die vorher ein Blattknoten war, verliert die neu erstellte zusammenfassende Aufgabe eigene Datumsangaben, den Aufwand und Anzahl der Ressourcen. Sie verwendet nun eine Zusammenfassung der Werte ihrer neuen konstituierenden Aufgaben. 

**Hochstufen von Aufgaben** Wenn Sie Aufgabe hochstufen, ist diese nicht mehr eine konstituierende Aufgabe ihre übergeordneten Elementes. Die PSP-Nummer dieser Aufgabe wird automatisch neu berechnet, um die neuen Ebene der Aufgabe in der Hierarchie widerzuspiegeln. Der Aufwand, die Kosten und die Datumsangaben der vorherigen übergeordneten Aufgabe der Aufgabe werden neu berechnet, um diese Aufgabe auszuschließen. 

**Nach oben/unten verschieben** Wenn Sie auf **Nach oben** und **Nach unten** klicken, ändern Sie die Position einer Aufgabe innerhalb der Hierarchie des übergeordneten Artikels. Die Position einer Aufgabe wirkt sich nicht auf den Aufwand, die Kosten, die Datumsangaben oder Dauer der Aufgabe aus. Die PSP-Nummer dieser Aufgabe wird automatisch neu berechnet, um die neuen Ebene der Aufgabe in der Hierarchie widerzuspiegeln.

### <a name="schedule-estimation"></a>Zeitplankalkulation

Die Zeitplankalkulation ist normalerweise der zweiten Schritt, wenn Sie den PSP erstellen. Als optimale Methode sollten Sie die Zeitplankalkulation abschließen, nachdem Sie die Aufgaben erstellt haben. Die **Projektstrukturplan**-Seite in Microsoft Dynamics 365 for Operation hat zwei Abschnitte. Der obere Bereich ist für die Zeitplankalkulation bewirken und der untere Bereich enthält eine Registerkarte **Vorkalkulierte Kosten und Umsatzerlöse**, die für die Kostenschätzung verwendet wird. 
**Aufgabenabhängigkeiten** In einem PSP können Sie eine Vorgängerbeziehung zwischen Aufgaben erstellen. Wenn Sie Aufgaben eine Vorgängeraufgabe zuweisen, kann sie nur dann starten, wenn alle Vorgängeraufgaben ausgeführt wurden. Das geplante Startdatum der Aufgabe wird automatisch zum spätestmöglichen Datum aller ihrer Vorgänger festgelegt. 

**Aufgabenplanung in Microsoft Dynamics 365 for Operations** Die folgenden Faktoren bestimmen die Planung von Blattknotenaufgaben:

-   Vorherige Aktivitäten
-   Aufwand
-   Die Anzahl der Ressourcen
-   Start- und Enddatum

Das Startdatum einer Blattknotenaufgabe ohne Vorgänger wird automatisch auf das Planungsstartdatum des Projekts festgelegt. Die Dauer einer Blattknotenaufgabe wird immer als die Anzahl von Arbeitstagen zwischen den Start- und Enddatum berechnet. 

****Planungsregeln**** Wenn die automatische Planungshilfe aktiviert ist, gelten folgende Regeln für die Aufgabenplanung für Blattknotenaufgaben:

-   Die Start- und Enddatumsangaben einer Aufgabe müssen Arbeitstage gemäß dem Planungskalender des Projekts sein.
-   Das Startdatum einer Aufgabe mit Vorgänger wird automatisch zum spätestmöglichen Datum aller ihrer Vorgänger festgelegt.
-   Der Aufwand für eine Aufgabe wird automatisch wie folgt berechnet:

Anzahl der Personen × Dauer × Anzahl der Stunden an einem Standardarbeitstag im Projektkalender. 

In einigen Fällen möchten Sie von diesen Regeln abweichen. Sie können die automatische Planung deaktivieren, um zu verhindern, dass Microsoft Dynamics 365 for Operations automatisch alle Eigenschaften von Blattknotenaufgaben festlegt oder korrigiert. Wenn Sie Informationen für eine Aufgabe eingeben, die eine Verletzung einer Planungsregel darstellen, wird ein Planungsfehlersymbol für die Aufgabe angezeigt. Wenn die Planungsfehler nicht angezeigt werden sollen, klicken Sie auf **Planungsfehlern werden angezeigt**, um die Funktion zu deaktivieren. 

> [!NOTE] 
> Die Werte für eine Zusammenfassungs- oder Containeraufgabe werden auch weiterhin aus Summe der Werte der konstituierenden Aufgaben berechnet. Dies geschieht unabhängig davon, ob die automatische Planungshilfe aktiviert ist. 

**Beheben von Planungsfehlern** Wenn die automatische Planungshilfe aktiviert ist, sind Planungsfehlern nicht wahrscheinlich. Wenn Sie jedoch die automatische Planungshilfe deaktivieren und diese später aktivieren, werden möglicherweise Planungsfehlersymbole im PSP angezeigt. 

**Beheben von Planungsfehlern nach Aufgaben** Wenn Sie auf das Zeitplanfehlersymbol für eine bestimmte Aufgabe doppelklicken, wird ein Dialogfeld mit allen Planungsfehlern für diese Aufgabe angezeigt. Sie können entscheiden, welche Fehler Sie korrigieren möchten. 

**Korrigieren aller Planungsfehler** Wenn Sie möchten, dass Microsoft Dynamics 365 for Operations alle Planungsfehler im PSP korrigiert, klicken Sie im Aktivitätsbereich auf **Reparieren von alle Planungsabweichungen**. 

> [!NOTE] 
> Diese Funktion kann zu erheblichen Änderungen am PSP führen. Fehler werden in der folgenden Reihenfolge korrigiert:

1.  Der vorkalkulierte Aufwand für alle Aufgaben wird geändert, sodass er gleich die Kapazität im Projektkalender ist.
2.  Das Startdatum jeder Aufgabe wird geändert, sodass die Aufgabe nach Abschluss ihrer Vorgänger startet.
3.  Das Startdatum jeder Aufgabe wird geändert, um Lücken in den Startdaten der vorherigen Aktivitäten aufzuheben.

### <a name="cost-estimation"></a>Kostenvorkalkulation

Wie oben in diesem Dokument angegeben wurde, geben Sie die Vorkalkulation für jede Endknotenaufgabe ein, indem Sie die Registerkarte **Vorkalkulierte Kosten und Umsatzerlöse** im unteren Bereich der Seite **Projektstrukturplan** verwenden. 

> [!NOTE] 
> Sie können die Vorkalkulation für eine Zusammenfassungs- oder Containeraufgabe nicht ändern. Die Vorkalkulation für eine zusammenfassende Aufgabe entspricht der Summe der Vorkalkulation ihrer Endknotenaufgaben. Die vorkalkulierten Gesamtkosten für jede Aufgabe werden als die Summe der Beträge der vorkalkulierten Kosten für die folgenden Buchungstypen berechnet:

-   Arbeit
-   Artikel oder Material
-   Ausgaben

Eine **Gebühr** Buchungsart wird verwendet, um den gebührenbasierten Umsatzerlös zu kalkulieren. Diese Buchungsart hat keine Kostenkomponente und wird daher nicht berücksichtigt wenn Kosten vorkalkuliert werden. 

Eine **Akonto**-Buchungsart wird zum Erfassen des vereinbarten Verkaufswerts in einem Projekt vom Typ "Fester Wert" verwendet. Diese Buchungsart auch wird nicht berücksichtigt, wenn Kosten vorkalkuliert werden. 

Wenn Sie Kosten für Arbeit, Material und Ausgaben für jede Aufgabe kalkulieren, müssen Sie eine Projektkategorie zu den vorkalkulierten Kosten zuweisen. 

**Vorkalkulation von Arbeitskosten** Für jede Endknotenaufgabe weisen Sie einen Arbeitseinsatz in Stunden und eine Standardkategorie zu. Wenn Sie einen Zeitplan für eine Aufgabe einrichten, werden daher die vorkalkuierten Arbeitskosten für diese Aufgabe automatisch in der Standardkategorie für Arbeit hinzugefügt. Diese Vorkalkulation wird auf der Registerkarte **Vorkalkulierte Kosten und Umsatzerlöse** im Raster **Positionsdetails** für diese Aufgabe angezeigt. Wenn Sie mehr vorkalkulierte Arbeitskosten benötigen, können Sie sie auf dieser Registerkarte hinzufügen. Wenn Sie die Stunden für die vorkalkulierten Arbeitskosten erhöhen oder verringern, wird der Zeitplan für die Aufgabe automatisch neu berechnet. 

**Vorkalkulation Ausgaben und Materialkosten** Auf der **Vorkalkulierte Kosten und Umsatzerlöse** Registerkarte können Sie wenn nötig auch Ausgaben und Materialkosten für eine Aufgabe kalkulieren. 

Die Kosten und der Verkaufspreis für Arbeit- oder Ausgabenenvorkalkulationspositionen basieren auf den Einstellungen, die für jede Kategorie in den Preiskalkulationstabellen unter **Projektverwaltung und -buchhaltung** &gt; **Einstellungen** &gt; **Preise** definiert sind. Bei Artikeln werden die Kosten und der Verkaufspreis standardmäßig aus dem Artikel oder der Handelsvereinbarungen auf der Listenseite **Freigegebene Produkte** im Produkt-Informationsmanagement hinzugefügt.

## <a name="tracking-progress-on-the-wbs"></a>Verfolgen des Status im PSP
In einigen Branchen wird der Fortschritt eines Projekts über ein PSP sehr präzise verfolgt. Andere verfolgen den Status auf einer höheren Ebene des PSP. In diesem Abschnitt wird beschrieben, wie Sie die PSP-Nachverfolgung für Ihre Projektanforderungen verwenden können. 

Microsoft Dynamics 365 for Operations verfügt über drei Ansichten für den PSP eines Projekts: Projektplanungsansich, Aufwandsverfolgungsansicht und Kostenverfolgungsansicht.

### <a name="planning-view"></a>Projektplanungsansicht

Die Projektplanungsansicht zeigt die geplante Vorkalkulation oder die Basisvorkalkulation des Plans und die Kosteninformationen an. Obwohl keine Funktionen für die Verfolgung der Version und der Basis für einen Projekt-PSP vorhanden sind, dienen die Werte in dieser zur Darstellung der Basisversion. Die Abschnitte Zeitplankalkulation und Kostenkalkulation dieses Themas beschreiben dieser Ansicht und deren Verwendung, um einen PSP zu erstellen.

### <a name="effort-tracking-view"></a>Aufwandsverfolgungsansicht

Die Aufwandsverfolgungsansicht zeigt die Nachverfolgung des Status für Aufgaben im PSP. Sie vergleicht die kumulierten tatsächlichen Aufwandsstunden für eine Aufgabe mit den geplanten Aufwandsstunden. Die folgenden Formeln gelten für die Werte in der Aufwandsnachverfolgungsansicht:

-   Status (in Prozent) = tatsächlicher Aufwand bis dato ÷ geplanter Aufwand für die Aufgabe
-   Verbleibender Aufwand (auch "Geschätzte Dauer bis zum Abschluss \[ETC\]) = geplanter Aufwand - tatsächlicher Aufwand bis dato
-   Geschätzte Gesamtkosten = verbleibender Aufwand + Aufwand bis dato
-   Voraussichtliche Aufwandsabweichung = geplanter Aufwand - Geschätzte Gesamtkosten (EAC)

Die Aufwandsnachverfolgungsansicht zeigt eine Projektion der Aufwandsabweichung für die Aufgabe basierend auf dem EAC an (größer oder kleiner als der geplante Aufwand).

-   Wenn der EAC größer als der geplante Aufwand ist, wird die Aufgabe mehr Zeit als ursprünglich geplant benötigen und ist verspätet.
-   Wenn der EAC kleiner als der geplante Aufwand ist, wird die Aufgabe weniger Zeit als ursprünglich geplant benötigen und ist dem Plan voraus.

**Neuprojektion des Aufwands durch den Projektmanagers** Gelegentlich müssen der Projektmanager oder eine andere Person, die den Status eines Projekts verfolgt, die ursprünglichen Vorkalkulationen für eine Aufgabe überarbeiten. Die Aufgabe wird möglicherweise aus unterschiedlichen Gründen schneller oder langsamer als ursprünglich durchgeführt. Beispielsweise kann sich der Umfang verringert haben, oder Arbeitskräfte haben weniger Erfahrung als ursprünglich geplant. Projektionen stellen die Vorstellung eines Projektmanagers zur Vorkalkulationen dar. Sie basieren auf dem aktuellen Status in einem Projekt. Im Allgemeinen sollte Sie die Basiswerte nicht ändern, da eine Basis des Projekts ein veröffentlichtes Dokument für den Zeitplan des Projekts und die Vorkalkulation darstellt, de alle Projektbeteiligten im Projekt zugestimmt haben. 

Es gibt zwei Arten, wie Projektmanager den Aufwand für Aufgaben ändern können:

-   Ändern Sie den verbleibenden Aufwand, der automatisch festgelegt wird, um den tatsächlichen verbleibenden Aufwand für die Aufgabe zu aktualisieren.
-   Ändern Sie den Arbeitsstatus (in Prozent), der automatisch festgelegt wird, um den tatsächlichen Status für die Aufgabe zu aktualisieren.

Beide Arten führen eine Neuberechnung des ETC, des EAC und des Status in Prozent der Aufgabe sowie der geplanten Aufwandsabweichung für die Aufgabe durch. Der EAC, ETC und der Status in Prozent bei Zusammenfassungsaufgaben werden ebenfalls neu berechnet und die voraussichtliche Aufwandsabweichung wird aktualisiert. 

**Geänderter Aufwand bei Zusammenfassungsaufgaben** Sie können den Aufwand für Zusammenfassungs- oder Containeraufgaben ändern. Unabhängig davon, ob Sie diese Werte ändern, indem Sie den verbleibenden Aufwand oder den Statusprozentsatz für Zusammenfassungsaufgaben ändern, treten die Berechnungen automatisch in der folgenden Reihenfolge auf:

1.  Der EAC, ETC und der Status in Prozent für die Aufgabe werden berechnet.
2.  Der neue EAC wird den untergeordneten Aufgaben im gleichen Verhältnis zugeordnet wie der ursprüngliche EAC-Betrag.
3.  Der neue EAC in jeder Endknotenaufgabe wird berechnet.
4.  Der verbleibende Aufwand und der Status in Prozent werden für alle betroffenen untergeordneten Aufgaben basierend auf dem neuen EAC-Wert berechnet. Die Aufwandsabweichung der Aufgaben wird auch neu berechnet.
5.  Der EAC der Zusammenfassungsaufgaben wird aus den Endknoten neu berechnet.

Klicken Sie auf **Erweitern auf Ebene** in der Aufwandsverfolgungsansicht, um die Ebene festzulegen, auf der Sie Ihren PSP verfolgen und warten. Der PSP wird automatisch auf die Ebene in der Aufwandsnachverfolgungsansicht erweitert, wenn Sie sie öffnen.

### <a name="cost-tracking-view"></a>Kostenverfolgungsansicht

Die Kostenverfolgungsansicht zeigt die Nachverfolgung des Kostenverbrauchs für eine Aufgabe an. In dieser Ansicht werden die Istkosten, die für eine Aufgabe bis jetzt ausgegeben wurden, mit den geplanten Kosten für die Aufgabe verglichen. Die folgenden Formeln gelten für die Werte in der Kostenverfolgungsansicht:

-   Prozentsatz der verbrauchten Kosten = Istkosten bis dato ÷ geplante Kosten für die Aufgabe
-   Fertigstellungskosten (CTC) = geplante Kosten – tatsächliche Kosten bis dato
-   Geschätzte Gesamtkosten (EAC) = CTC + tatsächliche Kosten bis dato
-   Voraussichtliche Kostenabweichung = geplante Kosten - EAC

Die Kostennachverfolgungsansicht zeigt eine Projektion der Kostenabweichung für die Aufgabe basierend auf dem EAC an (größer oder kleiner als die geplanten Kosten).

-   Wenn der EAC größer als die geplanten Kosten ist, wird die Aufgabe mehr Finanzmittel als ursprünglich geplant benötigen und liegt über dem Budget.
-   Wenn der EAC kleiner als die geplanten Kosten ist, wird die Aufgabe weniger Finanzmittel als ursprünglich geplant benötigen und liegt unter dem Budget.

**Neuprojektion der Kosten durch den Projektmanagers** Projektmanager müssen über den CTC die ursprüngliche Kostenvorkalkulation für eine Aufgabe überarbeiten. Der Projektmanager kann den CTC-Wert auf die Kosten ändern, die benötigt werden, um die Aufgabe abzuschließen. Wenn Sie den CTC-Wert ändern, werden der CTC der Aufgabe, der EAC, der Prozentsatz der verbrauchten Kosten und die voraussichtliche Kostenabweichung für eine Aufgabe neu berechnet. Der EAC, ETC und die Kosten in Prozent bei Zusammenfassungsaufgaben werden ebenfalls neu berechnet und die voraussichtliche Kostenabweichung wird aktualisiert. 

> [!NOTE] 
> Wenn Sie Aufwand für eine PSP-Aufgabe in der Aufwandsnachverfolgungsansicht überarbeiten, werden der CTC der Aufgabe, der EAC, der Prozentsatz der verbrauchten Kosten und die voraussichtliche Kostenabweichung alle in der Kostennachverfolgungsansicht neu berechnet. Kostenüberarbeitungen wirken sich jedoch nicht auf die Werte in der Aufwandsnachverfolgungsansicht aus, da die Kosten nach Buchungsart (Arbeit, Material oder Ausgaben) oder Projektkategorie nicht überarbeitet werden. 

**Projektionsüberarbeitung für Kosten zu Zusammenfassungsaufgaben** Sie können die Kosten für Zusammenfassungsaufgaben überarbeiten. Die Berechnungen treten automatisch in der folgenden Reihenfolge auf:

1.  Der EAC, der CTC und der Prozentsatz der verbrauchten Kosten für die Aufgabe werden neu berechnet.
2.  Der neue EAC wird den untergeordneten Aufgaben im gleichen Verhältnis zugeordnet wie der ursprüngliche EAC der Aufgaben.
3.  Der neue EAC für jede Aufgabe wird berechnet.
4.  Der CTS und der Prozentsatz der verbrauchten Kosten werden für die betroffenen untergeordneten Aufgaben basierend auf dem EAC-Wert neu berechnet. Die Kostenabweichung der Aufgaben wird neu berechnet.
5.  Der EAC für alle Zusammenfassungsaufgaben wird auf Grundlage dieser Änderung neu berechnet.

Klicken Sie auf **Erweitern auf Ebene** in der Kostenverfolgungsansicht, um die Ebene festzulegen, auf der Sie Ihren PSP verfolgen und warten. Der PSP wird automatisch auf die Ebene in der Kostennachverfolgungsansicht erweitert, wenn Sie sie öffnen.

### <a name="earned-value-management"></a>Verwaltung des Ertragswerts

Sie können die Ertragswertmethode (EVM) verwenden, um den Status des Projekts zu verfolgen. Sie können Ertragswertmetrik im Rollencenter des Projektmanagers anzeigen. Die Ertragswertdiagrammkomponente zeigt die phasenweisen Werte des geplanten Werts sowie der Istkosten an. Ertragswerte ab dem aktuellen Datum werden als Punkt angezeigt. Phasenweise Daten für Ertragswert sind im Moment nicht verfügbar. 

Die Zeitphase im Ertragswertdiagramm wird pro Woche oder Monat angezeigt. In diesem Abschnitt werden die drei Säulen des EVM beschrieben: geplanter Wert, Ertragswert und Istkosten. 

**Geplanter Wert** Die EVM-Theorie besagt, das der Graph mit dem geplanten Wert den Satz darstellt, mit dem das Team des Projekts für eine Rentabilität geplant hat. 

Microsoft Dynamics 365 for Operations verwendet die 0:100-Einnahmeregel für die Darstellung des geplanten Werts. Bei dieser Regel wird der Wert der Aufgabe am Enddatum für die Aufgabe gebucht. Kein Wert wird gebucht, bis die Aufgabe zu 100 Prozent abgeschlossen ist. 

Im Projektverwaltungs- und Buchhaltungsmodul geben Sie das Enddatum der Endknoten und die geplanten Kosten ein. Wenn das Diagramm für den geplanten Wert nach Woche angezeigt wird, wird der geplanter Wert wochenweise für alle Endknotenaufgaben für die Dauer des Projekts zusammengefasst. 

**Ertragswert** Die EVM-Theorie besagt, das der Graph mit dem Ertragswert den Satz darstellt, mit dem das Team des Projekts rentabel ist. 

Microsoft Dynamics 365 for Operations verwendet die 0:100-Einnahmeregel für die Darstellung des Ertragswerts. Bei dieser Regel wird der Wert der Aufgabe am Enddatum für die Aufgabe gebucht. Kein Wert wird gebucht, bis die Aufgabe zu 100 Prozent abgeschlossen ist. 

Wenn der Ertragswert berechnet wird, wird der Statusprozentsatz jeder Aufgabe berücksichtigt. Bei der 0:100-Regel werden nur Aufgaben, die während einer bestimmten Periode abgeschlossen werden, für die Berechnung des Ertragswerts am Ende der Periode berücksichtigt. Der Ertragswert für das Projekt wird für alle Aufgaben berechnet, die abgeschlossen wurden, wenn das Diagramm erstellt wird. 

> [!NOTE] 
> Im Moment verfügt das System für die PSP-Nachverfolgung nicht über Datenstrukturen, um historische Statusprozentsätze für jede Aufgabe zu speichern. Daher kann der Ertragswert nur ab der Zeit gemeldet werden zu der der Cube verarbeitet wird. Verarbeiten Sie den Cube regelmäßig, um die Ertragswertdaten zu aktualisieren, die im Rollencenter angezeigt werden. 

**Istkosten** Die EVM-Theorie besagt, dass Istkosten den Satz darstellen, zu dem Geld für das Projekt ausgegeben wird. 

Buchungen, die für ein Projekt gebucht werden, werden für die Darstellung der Istkosten verwendet. Die Kosten werden nach Datum zusammengefasst. Diese Daten werden dann verwendet, um die Istkosten grafisch darzustellen (nach Woche oder nach Monat).

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>So nutzen Sie die Konzepte zum geplanten Wert, Ertragswerts und zu den Istkosten

**Abweichung planen** Während der Planung erstellen Sie auf einer Zeitachse eine Planung für Arbeit. Daher ist der geplante Wert der Satz, zu dem die Projektplaner die Arbeit im Projekt als abgeschlossen angenommen haben. Nachdem sich ein Projekt in Bearbeitung befindet, wird die Arbeit abgeschlossen, und das Projekt bringt Ertrag. Wenn Sie den geplanten Wert mit dem Ertragswert vergleichen, können Sie sehen, wie die Arbeit im Projekt fortschreitet. Das Ergebnis dieses Vergleichs wird als "Zeitplanabweichung" bezeichnet. 

Wenn der geplante Wert für eine Periode über dem Ertragswert liegt, wurde weniger Arbeit für ein Projekt durchgeführt als geplant. Daher ist das Projekt verspätet. Da der geplante Wert und Ertragswert Geldbeträge sind, wird auch der Verzögerungszeit im Projekt ein monetärer Wert zugewiesen. 

Wenn der geplante Wert für eine Periode unter dem Ertragswert liegt, wurde mehr Arbeit für ein Projekt durchgeführt als geplant. Daher ist das Projekt dem Plan voraus. Dieser Durchlaufzeit wird auch ein monetären Wert gegeben.

**Kostenabweichung** Da der Ertragswert den Einstandspreis als Multiplikator verwendet, gibt der Ertragswert die Kosten der Arbeit an, die an einem Projekt ausgeführt wurde. Im Laufe eines Projektes stellt das Transaktionslog einen Datensatz zu den Geldmitteln bereit, die tatsächlich für dieses Projekt ausgegeben wurden. Wenn Sie den Ertragswert mit den Istkosten vergleichen, können Sie den Geldbetrag der aufgewendet wurde und den Ertrag sehen. Das Ergebnis dieses Vergleichs wird als "Kostenabweichung" bezeichnet. 

Wenn die Istkosten, die für eine Periode aufgewendet wurden, über dem Ertragswert liegen, wurde mehr eingenommenen als ausgegeben. Daher ist das Projekt über dem Budget. 

Wenn die Istkosten, die für eine Periode aufgewendet wurden, unter dem Ertragswert liegen, wurde mehr ausgegeben als eingenommenen. Daher ist das Projekt unter dem Budget.

## <a name="wbs-templates"></a>WBS-Vorlagen
Sie können die PSP-Vorlagenfunktionen verwenden, um Standardvorlagen für Projekte zu erstellen. Wenn die Projekte viel wiederholbare Arbeit umfassen, sollten Sie eine PSP-Vorlage erstellen. 

Sie können eine PSP-Vorlage vom PSP eines vorhandenen Projekts erstellen. So werden die Erkenntnisse und bewährten Methoden, die Sie bei der Planung dieses Projekts erworben haben, auf ähnlichen Projekte in der Zukunft wiederverwendet. Manchmal ist es jedoch nicht sinnvoll, den gesamten PSP als Vorlage zu speichern. Daher können Sie Vorlagen aus den Teilen des PSP für ein Projekt erstellen.

### <a name="saving-a-projects-wbs-as-a-template"></a>Speichern des PSP eines Projekts als Vorlage

Nachdem Sie eine Vorlage erstellt haben, können Sie sie in PSP eines neuen Projekts unter den Stammknoten oder unter jede Aufgabe im PSP des Projekts importieren.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>Importieren einer PSP-Vorlage in den PSP eines Projekts

Wenn Sie Aufgaben importieren, werden die Aufgaben in der Vorlage auf Grundlage des Startdatums der Aufgabe organisiert, unter der Sie importieren. Während des Imports werden Vorgängerbeziehungen der Vorlagenaufgaben verwendet, um die Startdaten für die importierten Aufgaben zu berechnen. Der Standardarbeitskalender des Zielprojekts wird angewendet, um die Enddaten der importierten Aufgaben zu berechnen, damit die im aktuellen Arbeitskalender des Projekts definierten Arbeitstage und Standardarbeitsstunden erhalten bleiben. 

Die Kostenbeträge und Verkaufspreise für die Vorkalkulationspositionen werden angewendet, um sicherzustellen, dass Preise für das Projekt oder dem Projektvertrag ein gültiges Datum haben.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Unterschiede zwischen dem PSP eines Projekts und einer PSP-Vorlage

-   Die Aufgaben in PSP-Vorlagen haben keine Start- und Enddaten.

Die Arbeitstage und die arbeitsfreien Tage werden nicht für PSP-Vorlagen festgelegt.

-   PSP-Vorlagen verwenden immer den Planungskalender, der als Standardkalender für alle Projekte eingerichtet wurde.

Der standardmäßige Planungskalender wird verwendet, um die Stunden in einem Standardarbeitstag abzufragen.

-   Vorgängerbeziehungen werden nicht mit einer PSP-Vorlage kopiert.

Da PSP-Vorlagen kein Datum haben, ist die Startdatumlogik, die auf dem Enddatum dem Vorgänger-Enddatum basiert, nicht erforderlich.

-   Eine Lohnkostenvorkalkulationsposition wird automatisch erstellt, wenn eine Aufgabe in einer PSP-Vorlage erstellt wird. Der Verkaufspreis und der Kostenbetrag werden aus der ausgewählten Arbeitskraft kopiert.

Ausgaben und Artikelkosten können manuell erstellt werden, genauso wie bei dem PSP eines Projekts.

-   Planungsfehlern werden angezeigt, wenn es Abweichungen von der folgenden Formel gibt:

Aufwand = Anzahl von Ressourcen × Dauer × Anzahl der Stunden im Standardarbeitstag 

Sie können alle Planungsfehlern gleichzeitig beheben, indem Sie auf **Alle Planungsfehlern korrigieren** klicken. 

Alternativ können Sie Planungsfehler einzeln korrigieren, indem Sie auf das Warnsymbol für jede Aufgabe klicken.




