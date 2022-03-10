---
title: Bestätigen und übertragen
description: In diesem Thema wird die Verwendung der Bestätigungs- und Übertragungsfunktion erläutert, mit der Benutzer Ladungen vom Lagerort aus versenden können, bevor sie alle mit diesen Ladungen verbundenen Arbeiten abgeschlossen haben.
author: mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadTemplate,WHSWorkTemplateTable,WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 7b487684980f60112d9af6bea02672f7e919c834
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103588"
---
# <a name="confirm-and-transfer"></a>Bestätigen und übertragen

[!include [banner](../includes/banner.md)]

Mit der Funktion *Bestätigen und übertragen* können Benutzer Ladungen vom Lagerort aus versenden, bevor sie alle mit diesen Ladungen verbundenen Arbeiten abgeschlossen haben. Wenn eine Lieferung eingeht, die nicht vollständig kommissionierte Ladungspositionen enthält, wird der bestätigende Benutzer aufgefordert, entweder die verbleibenden Mengen auf eine neue Ladung aufzuteilen oder die unvollständigen Mengen zu stornieren.

Systeme, die so eingerichtet sind, dass sie Szenarien zur Ladungsaufteilung unterstützen, in denen geplante und teilweise geladene Ladungen aufgrund neuer oder sich ändernder Umstände angepasst werden müssen.

Der Client verfügt über eine Logik, mit der eine teilweise geladene Ladung geschlossen und als versendet bestätigt werden kann. Alle verbleibenden Lieferungen und Ladungspositionen (einschließlich vollständiger oder teilweiser Positionsmengen) werden dann auf eine neu erstellte Ladung und Lieferung übertragen, wenn diese Übertragung erforderlich ist und die Einrichtung dies zulässt. Neue Lieferungen und Ladungen werden automatisch basierend auf den anfänglichen Kriterien für die Erstellung von Lieferungen und Ladungen erstellt und ihre Hauptattribute bleiben unverändert. Verbleibende Mengen können auch automatisch storniert werden, wenn noch kein Arbeitsauftrag erstellt wurde und der Benutzer diese Stornierung für erforderlich hält.

Diese Funktion unterstützt Szenarien, in denen die volle Ladung nicht auf einen einzelnen LKW passt oder in denen ein Teil der Ladung den Lagerort verlassen sollte, bevor der Rest der Ladung versandbereit ist. In diesen Szenarien können die verbleibenden Produkte auf eine neue Ladung und damit auf einen neuen LKW übertragen werden. Da diese Funktion für Ladungen verwendet werden kann, für die ansonsten eine Lieferung mit voller Ladung erforderlich ist, bietet sie zusätzliche Flexibilität, sodass Transportmanager nicht standardisierte oder unvorhergesehene Szenarien lösen können.

Wenn eine Ladung aufgeteilt wird, führt die Funktion *Bestätigen und übertragen* die folgenden Aktivitäten aus:

- Neue Ladungen und Lieferungen werden nach Bedarf erstellt. Jede Ladung oder Lieferung verfügt über fast alle Attribute der ursprünglichen Ladung oder Lieferung. Die Ausnahme ist der Ladungsstatus, der basierend auf dem Arbeitsstatus neu berechnet wird.
- Der Benutzer wird informiert, dass eine neue Ladung erstellt wurde. Dem Benutzer wird auch die ID der neuen Ladung mitgeteilt.
- Die aufgeteilten Ladungspositionen, Arbeitskopfzeilen und Arbeitspositionen werden mit den neuen Ladungs- und Lieferungsinformationen aktualisiert.
- Wenn eine ganze Lieferung aufgeteilt wird, wird die Lieferung beibehalten und nur die Ladungsreferenzen werden aktualisiert. Wenn die Lieferung aufgeteilt werden muss, wird eine neue Lieferung erstellt.

Wenn verbleibende Mengen storniert werden, werden alle Ladungspositionsmengen, die nicht entnommen wurden und denen keine nicht stornierten Arbeiten zugeordnet sind, aus der Ladung entfernt. Wenn eine Arbeit in Bearbeitung ist, kann der Benutzer nur die Ladung aufteilen. Verbleibende Mengen können nicht storniert werden.

Sie können nur Ladungen aufteilen, die alle der folgenden Kriterien erfüllen:

- Einer oder mehrerer Ladungspositionen wurden Mengen entnommen.
- Der Ladungsstatus ist geringer als geladen.
- Es gibt keine Ladungspositionsdaten. (Diese Daten werden durch Ladungsträger-Konsolidierung am Bereitstellungslagerplatz erstellt und die Funktion Bestätigen und übertragen unterstützt keine Ladungsträger-Konsolidierung.)
- Derzeit wartet kein Bestand auf das Verpacken an einem Verpackungslagerplatz. (Die Funktion *Bestätigen und übertragen* unterstützt keinen für die Packstation entnommenen Bestand, der noch nicht verpackt wurde, es sei denn, verpackte Container werden an Staginglagerplätze mit erstellter Ladearbeit platziert.)

> [!NOTE]
> Diese Funktion unterscheidet sich von der Transportladungsfunktion, die an Lagerorten verwendet werden sollte, die vor der Entnahme niemals Ladungen planen und erstellen können, sondern die stattdessen den verfügbaren Transportraum nach Abschluss der Entnahme laden.
>
> Verwenden Sie die Funktion *Bestätigen und übertragen* in Situationen, in denen Ladungen normalerweise im Voraus geplant und erstellt werden, in denen jedoch gelegentlich Ausnahmen auftreten, in denen die Ladung nicht zum verfügbaren Transport passt (z. B. einem LKW).

## <a name="turn-the-confirm-and-transfer-feature-on-or-off"></a>Schalten Sie die Bestätigungs- und Übertragungsfunktion ein oder aus

Um die Funktionalität zu verwenden, die in diesem Thema beschrieben wird, die Funktion *Bestätigung und Übertragung* für Ihr System eingeschaltet werden. Ab Supply Chain Management 10.0.25 ist diese Funktion obligatorisch und kann nicht deaktiviert werden. Wenn Sie eine ältere Version als 10.0.25 ausführen, können Administratoren diese Funktionalität ein- oder ausschalten, indem sie nach der Funktion *Bestätigung und Übertragung* im Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) suchen.

## <a name="set-up-confirm-and-transfer"></a>Einrichten der Bestätigung und Übetragung

Um die Funktion *Bestätigen und übertragen* verwenden zu können, müssen Sie sie in jeder relevanten Ladungsvorlage aktivieren. Darüber hinaus möchten Sie möglicherweise abhängig von den Anforderungen Ihre Arbeitsvorlagen vorbereiten, um die Funktion zu unterstützen. Wenn Sie das weiter unten in diesem Thema enthaltene Beispielszenario durcharbeiten möchten, richten Sie Ihr System wie in diesem Abschnitt beschrieben ein. (Dieses Szenario basiert auf **USMF**-Demodaten.)

### <a name="prepare-your-load-templates"></a>Vorbereiten Ihrer Ladungsvorlagen

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Ladung \> Ladungsvorlagen**.
1. Klicken Sie im Aktivitätsbereich auf **Bearbeiten**, um die Seite in den Bearbeitungsmodus zu versetzen.
1. Aktivieren Sie das Kontrollkästchen **Ladungsaufteilung während Lieferungsbestätigung zulassen** für jede vorhandene Vorlage, in der Sie die Funktion aktivieren möchten. Alternativ wählen Sie **Neu** aus, um eine neue Vorlage zu erstellen und sie nach Bedarf zu konfigurieren. Jede Ladung, die Sie mit dieser Vorlage erstellen, erbt diese Funktion. (Wenn Sie mit den **USMF**-Demodaten arbeiten, aktivieren Sie die Funktion für die Ladungsvorlage **20 'Container**.)

### <a name="prepare-your-work-templates"></a>Vorbereiten Ihrer Arbeitsvorlagen

Diese Einrichtung ist nicht in allen Situationen erforderlich. Das hier gezeigte Beispiel stellt sicher, dass die Arbeit durch die Lieferung unterbrochen werden kann, um das weiter unten in diesem Thema behandelte Beispielszenario zu unterstützen. Es gibt auch andere Möglichkeiten, um dieses Ergebnis zu erreichen.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Arbeit \> Arbeitsvorlagen**.
1. Wählen Sie im Raster im oberen Teil der Seite eine vorhandene Arbeitsvorlage aus, in der Sie die Funktion *Bestätigen und übertragen* einrichten möchten. (Wenn Sie mit den **USMF**-Demodaten arbeiten, wählen Sie die Arbeitsvorlage **51 Entnahme zu Plattform** aus.) Alternativ können Sie eine neue Arbeitsvorlage erstellen.
1. Wählen Sie im Aktivitätsbereich **Abfrage bearbeiten** aus, um das Dialogfeld **Vertrieb** zu öffnen.
1. Wählen Sie im Dialogfeld **Vertrieb** auf der Registerkarte **Sortierung** die Option **Hinzufügen** aus, um dem Raster eine Zeile hinzuzufügen.
1. Legen Sie in der neuen Zeile die folgenden Werte fest:

    - **Tabelle:** *Temporäre Arbeitstransaktionen*
    - **Abgeleitete Tabelle:** *Temporäre Arbeitstransaktionen*
    - **Feld:** *Lieferungs-ID*
    - **Suchrichtigung:** *Aufsteigend*

1. Wählen Sie **OK** aus, um Ihre Einstellungen zu speichern und das Dialogfeld **Vertrieb** zu schließen.
1. Wenn Sie eine Nachricht erhalten, die besagt, dass die Gruppierung zurückgesetzt wird, wählen Sie **Ja** aus, um fortzufahren.
1. Wählen Sie im Raster im oberen Teil der Seite **Arbeitsvorlagen** die soeben bearbeitete Vorlage aus und wählen Sie dann im Aktivitätsbereich **Arbeitskopfzeilenumbrüche** aus.
1. Klicken Sie im Aktivitätsbereich auf **Bearbeiten**, um die Seite in den Bearbeitungsmodus zu versetzen.
1. Legen Sie im Raster die folgenden Werte fest:

    - **Tabellenname:** *Temporäre Arbeitstransaktionen*
    - **Feldname:** *Lieferungs-ID*
    - **Nach diesem Feld gruppieren:** Aktivieren Sie dieses Kontrollkästchen.

1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Schließen Sie die Seite.

## <a name="scenario"></a>Szenario

Dieses Szenario zeigt ein Beispiel, in dem der Entnahmeprozess noch nicht abgeschlossen ist, die bisher entnommenen Artikel jedoch auf einen LKW geladen und trotzdem versendet werden müssen. Daher kann der Benutzer die Ladungspositionen, deren Entnahme rückgängig gemacht wurde, auf eine neue Ladung aufteilen. Alle Datenbeziehungen werden daraufhin automatisch aktualisiert.

> [!NOTE]
> Die Werte, die in diesem Szenario beschrieben werden, basieren auf den **USMF**-Demodaten. Wir empfehlen, dass Sie diese Demodaten verwenden, während Sie die Verwendung der Funktion demonstrieren oder erlernen. Wenn Sie die **USMF**-Demodaten nicht verwenden, ersetzen Sie Ihre eigenen Werte nach Bedarf.

### <a name="step-1-create-a-load-that-has-multiple-load-lines"></a>Schritt 1: Erstellen einer Last mit mehreren Ladungspositionen

Bevor Sie diese Funktion verwenden können, benötigen Sie eine Ladung mit mehreren Ladungspositionen. Außerdem müssen Sie sicherstellen, dass die Entnahmeorte über genügend Bestand für alle Artikel in den Aufträgen verfügen, die Sie erstellen werden. Überprüfen Sie die Einrichtung der Lagerplatzrichtlinie (**Lagerortverwaltung \> Einstellungen \> Lagerplatzrichtlinien**) und notieren Sie sich die Entnahmeorte, die für die Entnahme von Aufträgen verwendet werden. Wenn Sie den Bestand anpassen müssen, können Sie je nach Bedarf manuelle Bewegungen erstellen, Wiederbeschaffung verwenden oder einen anderen Flow verwenden.

Um eine qualifizierende Ladung zu erstellen, müssen Sie zunächst drei Aufträge erstellen, indem Sie folgendermaßen vorgehen.

1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um das Dialogfeld **Auftrag erstellen** zu öffnen.
1. Legen Sie im Dialogfeld **Auftrag erstellen** (mindestens) die folgenden Werte fest:

    - Legen Sie im Inforegister **Kunde** das Feld **Kundenkonto** auf *US-004* (*Cave Wholesales*) fest.
    - Legen Sie im Inforegister **Allgemein** das Feld **Lagerort** auf *51* fest.

1. Wählen Sie **OK** aus, um den Auftrag zu erstellen, und schließen Sie das Dialogfeld **Auftrag erstellen**.
1. Ihr neuer Auftrag wird geöffnet. Fügen Sie im Raster **Auftragspositionen** eine Position mit den folgenden Werten hinzu:

    - **Artikelnummer:** *M9200*
    - **Menge** *40*
    - **Einheit:** *ea*

1. Wählen Sie im Menü **Lagerbestand** über dem Raster die Option **Reservierung** aus.
1. Wählen Sie im Aktivitätsbereich **Los reservieren** aus, um die Seite **Reservierung** zu öffnen.
1. Reservieren Sie den Bestand in der Verkaufsposition und schließen Sie die Seite **Reservierung**.
1. Wiederholen Sie die Schritte 1 bis 4, um einen zweiten Auftrag für denselben Kunden und denselben Lagerort hinzuzufügen.
1. Fügen Sie zwei Verkaufspositionen mit den folgenden Werten hinzu. Reservieren Sie nach dem Hinzufügen jeder einzelnen Position Bestand für sie, wie in den Schritten 6 bis 8 beschrieben.

    - **Position 1:** Legen Sie das Feld **Artikelnummer** auf *M9200*, das Feld **Menge** auf *30* und das Feld **Einheit** auf *EA* fest.
    - **Position 2:** Legen Sie das Feld **Artikelnummer** auf *M9201*, das Feld **Menge** auf *20* und das Feld **Einheit** auf *EA* fest.

1. Wiederholen Sie die Schritte 1 bis 4, um einen dritten Auftrag für denselben Kunden und denselben Lagerort hinzuzufügen.
1. Fügen Sie zwei Verkaufspositionen mit den folgenden Werten hinzu. Reservieren Sie nach dem Hinzufügen jeder einzelnen Position Bestand für sie, wie in den Schritten 6 bis 8 beschrieben.

    - **Position 1:** Legen Sie das Feld **Artikelnummer** auf *M9201*, das Feld **Menge** auf *20* und das Feld **Einheit** auf *EA* fest.
    - **Position 2:** Legen Sie das Feld **Artikelnummer** auf *M9202*, das Feld **Menge** auf *60* und das Feld **Einheit** auf *EA* fest.

#### <a name="load-planning-workbench"></a>Ladungsplanungsworkbench

Die Ladungsplanungs-Workbench verwendet die Ladungsvorlagen-ID, um die Lieferungen zu erstellen und die Auftragspositionen an den Lagerort freizugeben.

1. Wechseln Sie zu **Transportverwaltung \> Planung \> Ladungsplanungsworkbench**.
1. Im Feld **Lagerort** wählen Sie *51* aus.

    Nun erstellen Sie die Ladung für die Aufträge, die Sie soeben erstellt haben.

1. Wählen Sie auf der Registerkarte **Auftragspositionen** im Raster die Auftragspositionen für die neuen Aufträge aus.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Angebot und Nachfrage** in der Gruppe **Hinzufügen** die Option **Zu neuer Ladung** aus.
1. Wählen Sie im Dialogfeld **Ladungsvorlagenzuordnung** im Feld **Ladungsvorlagen-ID** die Option *20' Container* aus.
1. Wählen Sie **OK**.
1. Suchen Sie im Bereich **Ladungen** auf der Seite **Ladungsplanungs-Workbench** im Raster nach der neue erstellten Ladungs-ID für den Lagerort *51*. Scrollen Sie nach rechts, bis Sie die Spalte **Ladungsaufteilung während Lieferungsbestätigung zulassen** sehen. Das Kontrollkästchen sollte für Ihre Ladung aktiviert sein.
1. Wählen Sie die Ladung aus.
1. Wählen Sie im Menü **Freigabe** oberhalb des Rasters **An Lagerort freigeben** aus, um Arbeit zu erstellen.
1. Überprüfen Sie im Dialogfeld **Ladung an Lagerort freigeben**, ob auf dem Inforegister **Einzuschließende Datensätze** Ihre Ladungs-ID angezeigt wird.
1. Wählen Sie **OK**.

    Möglicherweise wird die Meldung „Vorgang wird bearbeitet“ angezeigt, während das System die Lieferungen und die Arbeit erstellt.

1. Ihre Ladung sollte jetzt im Bereich **Ladungen** auf der Seite **Ladungsplanungs-Workbench** mit dem Ladungsstatus *In Wellen* angezeigt werden. Wählen Sie die Ladung aus und wählen Sie dann im Menü **Zugehörige Informationen** oberhalb des Rasters **Wellendetails** aus, um die erstellten Lieferungs-IDs anzuzeigen. Wenn Sie fertig sind, schließen Sie die Seite **Wellen**.
1. Wählen Sie im Bereich **Ladungen** auf der Seite **Ladungsplanungs-Workbench** die Ladung aus. Wählen Sie anschließend im Menü **Zugehörige Informationen** oberhalb des Rasters **Arbeitsdetails** aus, um die Arbeit anzuzeigen, die für die Aufträge erstellt wurde.
1. Notieren Sie sich die angezeigten Arbeits-IDs, die erstellt wurden. Möglicherweise müssen Sie nach rechts scrollen, um die Auftragsnummer und die Lieferungs-ID sehen zu können, die der Arbeits-ID zugeordnet sind.

### <a name="step-2-set-up-the-execution-flow-for-mobile-devices"></a>Schritt 2: Einrichten des Ausführungsflusses für mobile Geräte

Für Aufgaben auf mobilen Geräten müssen Benutzer Informationen wie die Arbeits-ID oder die Kennzeichen-ID eingeben. In den Feldern werden diese Informationen für Lagerortbenutzer in der Regel als Strichcodes bereitgestellt, die in der Dokumentation, auf der Verpackung oder am Regal zu finden sind. Stellen Sie zum Ausführen der Schritte für mobile Geräte für Szenarien sicher, dass Sie die Arbeits-IDs für die Transaktionen und die Kennzeichen-IDs für den Artikel und den Lagerplatz in den Transaktionen angegeben haben.

1. Melden Sie sich mit einer Benutzer-ID und einem Kennwort für den Lagerort *51* am mobilen Gerät an.
1. Wählen Sie **Ausgehend** aus.
1. Wählen Sie **Verkaufsauswahl** aus.
1. Sie können entweder die Arbeits-ID oder die Kennzeichen-ID eingeben. Geben Sie die Arbeits-ID für den ersten Auftrag ein und wählen Sie dann **Eingeben** aus.
1. Geben Sie in das Feld **LOC** den angezeigten Lagerplatz ein, um den Entnahmeort zu bestätigen. Wählen Sie dann **Eingeben** aus.
1. Geben Sie in das Feld **LP** die Kennzeichen-ID ein. Die Kennzeichen-ID muss mit dem Artikel, dem Lagerort und dem Lagerplatz des Artikels übereinstimmen, der vom ausgewählten Lagerplatz entnommen wird. Wählen Sie **Eingeben** aus, wenn Sie fertig sind.
1. Geben Sie in das Feld **Artikel** die Artikelnummer ein, um den entnommenen Artikel zu bestätigen, und wählen Sie dann **Eingeben** aus.
1. Geben Sie in das Feld **Menge** die Menge für den entnommenen Artikel ein, und wählen Sie dann **Eingeben** aus.
1. Geben Sie in das Feld **Ziel-LP** eine Zielkennzeichen-ID ein. Zielkennzeichen werden vom Benutzer definiert. Geben Sie unbedingt eine Kennzeichen-ID ein, an die Sie sich erinnern können. Wir empfehlen, dass Sie als Format das aktuelle Datum plus zwei Ziffern (JJMMTT\#\#) verwenden, beispielsweise *19112301*. Wählen Sie **Eingeben** aus, wenn Sie fertig sind.
1. Überprüfen Sie die angezeigten Informationen. Hierbei handelt es sich um die *Entnahmeinformationen*, die jetzt zu den *Einlieferungsdaten* für die Einlieferungstransaktion werden. Wählen Sie **Eingeben** aus, wenn Sie fertig sind.

    - Sie erhalten die Nachricht **Arbeit abgeschlossen**.

1. Wiederholen Sie die Schritte 4 bis 10 für die Arbeits-ID des zweiten Auftrags.

Der nächste Schritt besteht darin, die zwei entnommenen Kennzeichen auf den LKW zu laden.

1. Melden Sie sich mit einer Benutzer-ID und einem Kennwort für den Lagerort *51* am mobilen Gerät an.
1. Wählen Sie **Ausgehend** aus.
1. Wählen Sie **Verkaufsverladung** aus.
1. Geben Sie die benutzerdefinierte Zielkennzeichen-ID ein, die Sie in der vorherigen Prozedur für die erste Arbeits-ID erstellt haben. Wählen Sie dann **Eingeben** aus, um das Zielkennzeichen am Lagerplatz **PLATTFORM** einzuliefern.
1. Geben Sie die Zielkennzeichen-ID erneut ein und wählen Sie dann **Eingeben** aus, um das Kennzeichen am Lagerplatz **LADEBUCHT** einzuliefern.
1. Wiederholen Sie die Schritte 4 bis 5 für die Zielkennzeichen-ID, die Sie für die zweite Arbeits-ID erstellt haben.

Die beiden Arbeits-IDs werden nun geschlossen (geladen).

### <a name="step-3-confirm-the-outbound-shipment"></a>Schritt 3: Bestätigen der ausgehenden Lieferung

In diesem Schritt bestätigen Sie die beiden Aufträge und Arbeiten, die für die Ladung abgeschlossen wurden, um die entnommenen Artikel der Ladung zu versenden und eine neue Ladung für diejenigen Artikel zu erstellen, deren Entnahme rückgängig gemacht wurde. Die Bestätigung für die ausgehende Lieferung muss auf der Seite **Ladungsdetails** erfolgen.

1. Wechseln Sie zu **Transportverwaltung \> Planung \> Ladungsplanungsworkbench**.
1. Wählen Sie im Bereich **Ladungen** im Raster die Zeile für die von Ihnen erstellte Ladungs-ID aus.
1. Wählen Sie den Link der Ladungskennung aus, um die Seite **Ladungsdetails** zu öffnen.
1. Wählen Sie auf der Seite **Ladungsdetails** im Aktivitätsbereich auf der Registerkarte **Liefern und empfangen** in der Gruppe **Bestätigen** die Option **Ausgehende Lieferung** aus, um die Bestätigung einzuleiten.
1. Wählen Sie im Dialogfeld **Lieferungsbestätigung** im Feld **Ladungsaufteilungsmethode während Lieferungsbestätigung** die Option *Menge auf neue Ladung aufteilen* aus.
1. Wählen Sie **OK**.

    Möglicherweise erhalten Sie die Meldung „Vorgang wird bearbeitet“.

    Sie erhalten Informationsmeldungen, die darauf hinweisen, dass die Lieferung für Ihre Ladung bestätigt wurde und aus der aufgeteilten Menge eine neue Ladung erstellt wurde.

Aktualisieren Sie die Seite **Ladungsplanungs-Workbench**, um die neu erstellte Ladung anzuzeigen.

Sie können auch bestätigen, dass die Transaktionsbeziehungen wie folgt aktualisiert wurden:

- Die verbleibenden (unverarbeiteten) Lieferungen und Lieferpositionen wurden mit der neuen Ladungskennung aktualisiert.
- Der Auftrag ist mit der neuen Ladungskennung verknüpft.
- Die ursprüngliche Ladung enthält nicht die verbleibenden Ladungspositionen.
- Die verbleibende Arbeit wurde mit der neuen Ladungskennung aktualisiert.
- Die Welle bleibt gleich.
- Der Status der neuen Ladung wurde korrekt aktualisiert. (Wenn für den Arbeitsstatus _In Bearbeitung_ angezeigt wird, sollte auch für den Ladungsstatus _In Bearbeitung_ angezeigt werden.)

## <a name="notes-and-tips"></a>Hinweise und Tipps

- Sie können den Parameter **Ladungsaufteilung während Lieferungsbestätigung zulassen** auch nach dem Erstellen der Ladung mit deaktiviertem Parameter **Ladungsvorlage** aktivieren, wenn mit dem Ladeprozess noch nicht begonnen wurde. Wechseln Sie zu der gewünschten Ladung und aktivieren Sie in der Kopfzeile den Parameter.
- Die Option **Menge auf neue Ladung aufteilen** funktioniert auch, wenn einige der verbleibenden Arbeitskopfzeilen den Status *In Bearbeitung* aufweisen. Daher können Sie die Funktion selbst dann verwenden, wenn die Arbeitskräfte bereits die Entnahmeaufträge ausführen.
- Wenn Sie **Unerfüllte Menge stornieren** auswählen, während es noch verbleibende Arbeit mit dem Status *Offen* oder *In Bearbeitung* gibt, wird die folgende Fehlermeldung angezeigt: „Verbleibende Menge für Ladung kann nicht storniert werden. Für die Ladung ist Arbeit vorhanden.“
- Wenn Sie **Unerfüllte Menge stornieren** auswählen, wenn keine verbleibende Arbeit vorhanden ist, sich jedoch nicht freigegebene Ladungspositionen auf der Ladung befinden, wird die folgende Fehlermeldung angezeigt: „Die Lieferung für die Ladung konnte nicht bestätigt werden, da die Menge für den Artikel den Prozentsatz überschreitet, der für eine zu kleine Lieferung definiert ist.“ Um den Fehler zu vermeiden, können Sie den Prozentsatz für **Zu kleine Lieferung** für die nicht freigegebene Ladungsposition auf 100 Prozent festlegen. Nicht freigegebene Positionen werden nicht auf eine neue Ladung verschoben, aber die aktuelle Ladung wird mit einer zu kleinen Lieferung bestätigt. In diesem Fall können Sie den ursprünglichen Auftrag nicht erneut freigeben. Daher müssen Sie hierfür eine andere Lösung finden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]