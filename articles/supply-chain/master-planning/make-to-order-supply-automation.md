---
title: Automatisierung der Lieferungen zur Auftragsfertigung
description: In diesem Artikel wird beschrieben, wie Sie die verschiedenen Erweiterungen einrichten und verwenden, die durch die Automatisierungsfunktion für auftragsbezogene Lieferungen hinzugefügt werden.
author: t-benebo
ms.date: 07/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-07-27
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: d376c2f4d8514a4e6122e2e94455d57a39d2babf
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740193"
---
# <a name="make-to-order-supply-automation"></a>Automatisierung der Lieferungen zur Auftragsfertigung

[!include [banner](../includes/banner.md)]

Die Funktion *Auftragsautomatisierung der Lieferung* fügt Microsoft Dynamics 365 Supply Chain Management mehrere Verbesserungen hinzu. Mit diesen Erweiterungen können Sie die folgenden Aufgaben ausführen:

- Sehen Sie sich die Kapazitätsauslastung der Ressource für einen benutzerdefinierten Zeitraum an und ermöglichen Sie so eine langfristige Auswertung der Kapazitätsauslastung.
- Verbessern Sie die Flexibilität, indem Sie die Verzögerungstoleranz (negative Tage) für jeden Masterplan steuern.
- Halten Sie Produkte für Last-Minute-Bestellungen verfügbar und optimieren Sie die Nutzung des vorhandenen Angebots, indem Sie das spätestmögliche Angebot an eine Nachfrage koppeln, anstatt das erstmögliche Angebot zu verwenden.
- Halten Sie die Komponentenzuweisung für Produktionsaufträge nach der Fixierung flexibel, damit das System Bedarfsänderungen in letzter Minute optimieren kann. Mit anderen Worten: Beschränken Sie die Markierung auf eine Ebene.
- Kontrollieren Sie die Erfüllungsrichtlinie für jeden Verkaufsauftrag. Voreinstellungen werden aus dem Kundensetup übernommen.
- Erweitern Sie den Intercompany-Informationenfluss. Bestellungen werden aktualisiert, sodass sie Felder für Lieferart, Lieferbedingungen und externe Artikelnummer enthalten. Diese Änderung stellt sicher, dass detaillierte Bedarfsinformationen an das liefernde Unternehmen fließen können.

In diesem Artikel wird beschrieben, wie die einzelnen Erweiterungen eingerichtet und verwendet werden.

## <a name="turn-on-the-make-to-order-supply-automation-feature"></a>Aktivieren Sie die Funktion zur Auftragsautomatisierung

Bevor Sie die in diesem Artikel beschriebenen Funktion verwenden können, müssen Sie sie in Ihrem System aktivieren. Im Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) können Administratoren die Funktion wie folgt verwenden:

- **Modul:** *Produktprogrammplanung*
- **Funktionsname:** *Automatisierung der Lieferungen zur Auftragsfertigung*

## <a name="set-the-number-of-days-to-show-on-capacity-load-page"></a>Legen Sie die Anzahl der Tage fest, die auf der Seite Kapazitätsauslastung angezeigt werden sollen

Auf der Seite **Kapazitätsauslastung** können Sie die verfügbare Kapazität einer Ressource überprüfen. Die Funktion *Automatisierung der Lieferungen zur Auftragsfertigung* verbessert die **Kapazitätsauslastung** Seite durch Hinzufügen des Felds **Anzahl der Tage**. Sie können dieses Feld verwenden, um die Anzahl der Tage zu begrenzen, die das Gitter **Überblick** zeigt. Der eingestellte Wert wird gespeichert. Wenn Sie also die Seite verlassen und später zurückkehren, zeigt das Raster **Überblick** weiterhin die Anzahl der Tage an, die Sie zuletzt angegeben haben.

Zum Öffnen Seite **Kapazitätsauslastung** gehen Sie wie folgt vor, um die verfügbare Kapazität für eine einzelne Ressource anzuzeigen.

1. Wechseln Sie zu **Organisationsverwaltung \> Ressourcen \> Ressourcen**.
1. Zu untersuchende Ressource auswählen
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Ressource** in der Gruppe **Ansicht** den Eintrag **Kapazitätsauslastung**.
1. Verwenden Sie **Anzahl der Tage**, um die Anzahl der Tage zu begrenzen, die das Raster **Überblick** zeigt.

Zum Öffnen Seite **Kapazitätsauslastung** gehen Sie wie folgt vor, um die verfügbare Kapazität für eine einzelne Ressourcengruppe anzuzeigen.

1. Wechseln Sie zu **Organisationsverwaltung \> Ressourcen \> Ressourcengruppen**.
1. Zu untersuchende Ressourcengruppe auswählen.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Ressourcengruppe** in der Gruppe **Ansicht** den Eintrag **Kapazitätsauslastung**.
1. Verwenden Sie **Anzahl der Tage**, um die Anzahl der Tage zu begrenzen, die das Raster **Überblick** zeigt.

## <a name="apply-a-single-level-of-marking-when-you-firm-planned-orders"></a>Wenden Sie eine einzelne Markierungsebene an, wenn Sie Planaufträge fixieren

*Markierung* wird verwendet, um Angebot und Nachfrage zu verknüpfen. Sie ähnelt dem *Bedarfsverursacher*, der angibt, wie die Produktprogrammplanung die Nachfrage zu decken gedenkt. Die Markierung ist jedoch dauerhafter als Bedarfsverursacher. Die Funktion *Automatisierung der Lieferungen zur Auftragsfertigung* fügt die Möglichkeit hinzu, die Bestandskennzeichnung auf eine einzige Ebene zu beschränken, wenn Planaufträge bestätigt werden. Es fügt die folgenden neuen Optionen dem Feld **Kennzeichnung aktualisieren** im **Umwandeln** Dialogfeld, wenn Sie einen Auftragsvorschlag umwandeln:

- *Einstufiger Standard* – Es wird eine einstufige Markierung verwendet. Die Markierung auf einer Ebene markiert nur den Hauptartikel, nicht seine Komponenten der Stückliste (BOM). Daher können Sie die Komponentenzuordnung für Fertigungsaufträge nach der Fixierung flexibel halten. Die einstufige Markierung ermöglicht es dem System, Last-Minute-Bedarfsänderungen zu optimieren. Bei der einstufigen *Standard*-Markierung werden Bedarfsaufträge mit ihren Auftragserfüllung-Aufträgen markiert, aber Auftragserfüllungs-Aufträge werden nicht markiert, wenn sie eine Restmenge haben.
- *Einzelne Ebene erweitert* – Es wird eine einstufige Markierung verwendet. Bei der erweiterten *Einzelebenen*-Markierung werden Bedarfsaufträge mit ihren Auftragserfüllung-Aufträgen markiert, und Auftragserfüllungs-Aufträge werden immer markiert, egal ob sie eine Restmenge haben oder nicht.

Diese Optionen sind auch im Feld **Kennzeichnung aktualisieren** auf der **Standard-Update** Registerkarte der Seite **Masterplanungsparameter** verfügbar, auf der Sie die Standardauswahl für das Dialogfeld **Umwandeln** definieren.

Weitere Informationen finden Sie unter [Bestandsmarkierung](planning-optimization/marking.md).

## <a name="set-delay-tolerance-negative-days-at-the-master-plan-level"></a>Legen Sie die Verzögerungstoleranz (negative Tage) auf Hauptplanebene fest

Die Funktion *Automatisierung der Lieferungen zur Auftragsfertigung* fügt die Möglichkeit hinzu, die Verzögerungstoleranz (negative Tage) auf Masterplanebene zu konfigurieren. Die Einstellung ist auch auf Artikeldeckungs- und Deckungsgruppenebene verfügbar. Wenn negative Tage auf mehr als einer Ebene zugewiesen werden, wendet das System die folgende Hierarchie an, um zu entscheiden, welche Einstellung verwendet werden soll:

- Wenn negative Tage auf der Seite **Masterpläne** konfiguriert sind, überschreibt diese Einstellung alle anderen Einstellungen für negative Tage, wenn der Plan ausgeführt wird.
- Wenn negative Tage auf der Seite **Artikelabdeckung** konfiguriert sind, überschreibt diese Einstellung die Einstellung der Abdeckungsgruppe.
- Negative Tage, die auf der Seite **Deckungsgruppen** konfiguriert sind, gelten nur, wenn negative Tage nicht für einen relevanten Artikel oder Hauptplan konfiguriert wurden.

Gehen Sie folgendermaßen vor, um negative Tage für einen Masterplan festzulegen.

1. Wechseln Sie zu **Produktprogrammplanung \> Einrichtung \> Pläne \> Produktprogrammpläne**.
1. Wählen Sie einen Produktprogrammplan im Listenbereich aus, oder erstellen Sie einen neuen Produktprogrammplan.
1. Setzen Sie auf dem Inforegister **Planungszeitraum in Tagen** die Option **Negative Tage** auf *Ja*.
1. Geben Sie die Anzahl der negativen Tage im Feld daneben ein.

Weitere Informationen zur Verwendung negativer Tage finden Sie unter [Verzögerungstoleranz (negative Tage)](planning-optimization/delay-tolerance.md).

## <a name="control-the-pegging-sequence-used-during-master-planning"></a>Kontrolle der Bedarfsverursachersequenz, die während der Hauptplanung verwendet wird

Die Masterplanung verwendet eine *Bedarfsverursachersequenz*, um zu bestimmen, welches Angebot welche Nachfrage deckt. Die Funktion *Automatisierung der Lieferungen zur Auftragsfertigung* fügt eine neue Option **Spätestmöglichen Vorrat verwenden** hinzu, die Ihnen mehr Kontrolle über die Bedarfsverursachersequenz gibt. Mit der neuen Option halten Sie Produkte für Last-Minute-Bestellungen verfügbar und optimieren Sie die Nutzung des vorhandenen Angebots, indem Sie das spätestmögliche Angebot an eine Nachfrage koppeln, anstatt das erstmögliche Angebot zu verwenden.

Sie können die Bedarfsverursachersequenz auf Hauptplan-, Artikeldeckungs- oder Deckungsgruppenebene festlegen. Wenn eine Bedarfsverursachersequenz auf mehr als einer Ebene eingerichtet wird, wendet das System die folgende Hierarchie an, um zu entscheiden, welche Einstellung verwendet werden soll:

- Wenn eine Bedarfsverursachersequenz auf der Seite **Masterpläne** eingerichtet ist, überschreibt diese Einstellung alle anderen Bedarfsverursacher-Sequenzeinstellungen.
- Wenn eine Bedarfsverursachersequenz auf der Seite **Artikelabdeckung** konfiguriert ist, überschreibt diese Einstellung die Einstellung der Abdeckungsgruppe.
- Die auf der Seite **Deckungsgruppen** eingerichtete Bedarfsverursachersequenz gilt nur, wenn für einen relevanten Artikel oder Hauptplan keine Bedarfsverursacher-Sequenzeinstellungen konfiguriert wurden.

Führen Sie die folgenden Schritte aus, um Bedarfsverursacher auf der Ebene der Deckungsgruppe einzurichten.

1. Gehen Sie zu **Produktprogrammplanung \> Einstellungen \> Planungshorizont \> Dispositionssteuerungsgruppen**
1. Wählen Sie eine Gruppe im Listenbereich aus, oder erstellen Sie eine neue.
1. Auf dem Inforegister **Allgemein** im Abschnitt **Bedarfsverursachersequenz** verwenden Sie die Felder **Verfügbaren Lagerbestand verbrauchen** und **Spätestmöglichen Vorrat verwenden**, um Ihre Bedarfsverursachersequenz zu konfigurieren. Die Tabelle weiter unten in diesem Abschnitt zeigt, wie diese Einstellungen kombiniert werden, um Ihre Bedarfsverursachersequenz zu definieren.

Führen Sie die folgenden Schritte aus, um Bedarfsverursacher auf der Ebene der Artikeldeckungsgruppe einzurichten.

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Wählen Sie ein Produkt im Raster aus, oder erstellen Sie ein neues.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Plan** die Option **Artikelabdeckung**.
1. Die Seite **Artikelabdeckung** enthält Zeilen, mit denen Sie Deckungsregeln definieren können, die für den Artikel in jedem Lager gelten. Wählen Sie eine vorhandene Zeile im Raster aus oder erstellen Sie eine neue.
1. Auf der Registerkarte **Allgemein** wählen Sie **Bedarfsverursachersequenz überschreiben**.
1. Verwenden Sie die Felder **Verfügbaren Lagerbestand verbrauchen** und **Spätestmöglichen Vorrat verwenden**, um Ihre Bedarfsverursachersequenz zu konfigurieren. Die Tabelle weiter unten in diesem Abschnitt zeigt, wie diese Einstellungen kombiniert werden, um Ihre Bedarfsverursachersequenz zu definieren.

Führen Sie die folgenden Schritte aus, um Bedarfsverursacher auf der Masterplanebene einzurichten.

1. Wechseln Sie zu **Produktprogrammplanung \> Einrichtung \> Pläne \> Produktprogrammpläne**.
1. Wählen Sie einen Produktprogrammplan im Listenbereich aus, oder erstellen Sie einen neuen Produktprogrammplan.
1. Legen Sie im Inforegister **Allgemein** die Option **Bedarfsverursacher-Sequenz außer Kraft setzen** auf *Ja* fest.
1. Verwenden Sie die Felder **Verfügbaren Lagerbestand verbrauchen** und **Spätestmöglichen Vorrat verwenden**, um Ihre Bedarfsverursachersequenz zu konfigurieren. Die Tabelle weiter unten in diesem Abschnitt zeigt, wie diese Einstellungen kombiniert werden, um Ihre Bedarfsverursachersequenz zu definieren.

Die folgende Tabelle zeigt, wie **Verfügbaren Lagerbestand verbrauchen** und **Spätestmöglichen Vorrat verwenden** Einstellungen kombiniert werden, um Ihre Bedarfsverursacher-Sequenz festzulegen.

| | Spätestmöglichen Vorrat verwenden = Ja | Spätestmöglichen Vorrat verwenden = Nein |
|---|---|---|
| **Vorhandenes Inventar verbrauchen** = *Vor allem anderen Bestand* | <ol><li>Bestand</li><li>Vorhandenes Angebot, das das Nachfragedatum erfüllen kann</li><li>Vorhandenes Angebot, das das Bedarfsdatum nicht erfüllen kann, sich aber noch in negativen Tagen befindet</li><li>Erstellen Sie ein neues Angebot (geplanter Auftrag)</li></ol> | <ol><li>Bestand</li><li>Vorhandenes Angebot, das das Nachfragedatum erfüllen kann</li><li>Vorhandenes Angebot, das das Bedarfsdatum nicht erfüllen kann, sich aber noch in negativen Tagen befindet</li><li>Erstellen Sie ein neues Angebot (geplanter Auftrag)</li></ol> |
| **Vorhandenes Inventar verbrauchen** = *Nach allem anderen Bestand* | <ol><li>Vorhandenes Angebot, das das Nachfragedatum erfüllen kann</li><li>Bestand</li><li>Vorhandenes Angebot, das das Bedarfsdatum nicht erfüllen kann, sich aber noch in negativen Tagen befindet</li><li>Erstellen Sie ein neues Angebot (geplanter Auftrag)</li></ol> | <ol><li>Vorhandenes Angebot, das das Nachfragedatum erfüllen kann</li><li>Vorhandenes Angebot, das das Bedarfsdatum nicht erfüllen kann, sich aber noch in negativen Tagen befindet</li><li>Bestand</li><li>Erstellen Sie ein neues Angebot (geplanter Auftrag)</li></ol> |

## <a name="review-and-set-the-fulfillment-policy-that-applies-to-each-sales-order"></a>Überprüfen und legen Sie die Erfüllungsrichtlinie fest, die für jeden Verkaufsauftrag gilt

Die Auftragserfüllungsrichtlinien steuern den Prozentsatz des Gesamtpreises oder der Menge eines Auftrags, der physisch reserviert sein muss, bevor ein Auftrag für den Lagerort freigegeben werden kann. Sie können eine globale Standard-Auftragserfüllung-Richtlinie festlegen und diese dann nach Bedarf für bestimmte Kunden überschreiben. Die Funktion *Automatisierung der Lieferungen zur Auftragsfertigung* fügt die Möglichkeit hinzu, anzuzeigen, welche Standardrichtlinie tatsächlich für eine Bestellung gilt, und bei Bedarf eine auftragsspezifische Überschreibung anzuwenden.

- Um die Standardeinstellung der globalen Erfüllungsrichtlinie für Verkaufsaufträge festzulegen, gehen Sie zu **Debitorenkonten \> Konfiguration \> Debitorenkontenparameter**. Legen Sie dann auf der Registerkarte **Warehouse Management** das Feld **Auftragserfüllungsrichtlinie** auf den Namen der Richtlinie, die Sie verwenden möchten. 
- Um eine kundenspezifische Erfüllungsrichtlinie für Verkaufsaufträge festzulegen, gehen Sie zu **Debitorenkonten \> Kunden \> Alle Kunden**. Legen Sie dann auf der Registerkarte **Warehouse** das Feld **Auftragserfüllungsrichtlinie** auf den Namen der Richtlinie, die Sie verwenden möchten.

Führen Sie die folgenden Schritte aus, um die Standardrichtlinie anzuzeigen, die für jede Bestellung gilt, und eine auftragsspezifische Überschreibung anzuwenden.

1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Öffnen Sie den Auftrag, den Sie untersuchen oder bearbeiten möchten.
1. Wählen Sie die Ansicht **Kopfzeile** aus.
1. Auf der Inforegister **Lagerort** überprüfen und bearbeiten Sie die folgenden Felder nach Bedarf:

    - **Auftragserfüllungsrichtlinie** – Wählen Sie die Auftragserfüllungsrichtlinie aus, die für die ausgewählte Bestellung verwendet werden soll. Die Standardrichtlinie wird überschrieben. Zu Verwenden der standardmäßigen Auftragserfüllungsrichtlinie, die in **Standardausführungsrichtlinie**, lassen Sie dieses Feld leer.
    - **Standardausführungsrichtlinie** – Dieses Feld zeigt die standardmäßige Erfüllungsrichtlinie an, die gilt, wenn das Feld **Auftragserfüllungsrichtlinie** ist leer. Dieses Feld ist schreibgeschützt. Wenn es leer ist, ist keine kundenspezifische oder globale Standard-Auftragserfüllungsrichtlinie definiert.

    Wenn die Felder **Standardausführungsrichtlinie** und **Auftragserfüllungsrichtlinie** leer sind, gilt keine Auftragserfüllungsrichtlinie. Es können jedoch andere Einschränkungen bestehen, die erfordern, dass Reservierungen oder andere Bedingungen erfüllt werden, bevor der Verkaufsauftrag freigegeben werden kann.

## <a name="set-the-delivery-mode-and-terms-on-individual-purchase-order-lines"></a>Legen Sie den Liefermodus und die Bedingungen für einzelne Bestellpositionen fest

Alle Bestellungen beinhalten **Lieferbedingungen** und **Art der Lieferung** Einstellungen im Auftragskopf. Die Funktion *Automatisierung der Lieferungen zur Auftragsfertigung* fügt diese Einstellungen jeder Bestellposition hinzu. Daher können Sie Überschreibungen von **Lieferbedingungen** und/oder **Art der Lieferung** für eine oder alle Auftragspositionen nach Bedarf überschreiben. Für Zeilen, in denen keine Überschreibung definiert ist, wird der Wert aus der Kopfzeile verwendet. Sie können angeben, ob eine Änderung des Werts eines oder beider dieser Felder im Auftragskopf auch alle Zeilen aktualisieren soll.

Um festzulegen, was mit den Leitungseinstellungen passieren soll, wenn ein Benutzer die Werte für **Lieferbedingungen** und/oder **Art der Lieferung** in einem Auftragskopf ändert, folgen Sie diesen Schritten.

1. Gehen Sie zu **Beschaffung und Ursproung\> Einstellungen \> Beschaffungs- und Ursprungsparameter**.
1. Auf der Registerkarte **Allgemein** im Inforegister **Standardwerte und Parameter** wählen Sie den Link **Bestellpositionen aktualisieren**.
1. In dem **Bestellpositionen aktualisieren** Dialogfeld in den Feldern **Aktualisierung der Lieferbedingungen** und **Lieferart aktualisieren** wählen Sie einen der folgenden Werte aus:

    - *Niemals* – Aktualisieren Sie niemals die Auftragspositionen, nachdem die Einstellungen im Auftragskopf geändert wurden.
    - *Immer* – Aktualisieren Sie immer alle Auftragspositionen, nachdem die Einstellungen im Auftragskopf geändert wurden.
    - *Eingabeaufforderung* – Wenn ein Benutzer eine oder beide Einstellungen im Auftragskopf ändert, öffnen Sie einen Dialogbot, der fragt, ob der Benutzer alle Zeilen aktualisieren möchte, damit sie der Änderung an einer oder beiden Einstellungen entsprechen.

Gehen Sie folgendermaßen vor, um Lieferinformationen in einem Bestellkopf festzulegen.

1. Wechseln Sie zu **Beschaffung \> Bestellungen \> Alle Bestellungen**.
1. Öffnen Sie die Bestellung, die Sie untersuchen oder bearbeiten möchten.
1. Wählen Sie die Ansicht **Kopfzeile** aus.
1. Auf dem Inforegister **Lieferung** legen Sie **Art der Lieferung** und **Lieferbedingungen** nach Bedarf fest.
1. Abhängig von den Einstellungen auf der Seite **Beschaffungs- und Beschaffungsparameter** werden Sie möglicherweise gefragt, ob Sie Ihre Änderungen auf alle Auftragspositionen anwenden möchten.

Gehen Sie folgendermaßen vor, um Überschreibungen der Lieferinformationen in einem Bestellkopf festzulegen.

1. Wechseln Sie zu **Beschaffung \> Bestellungen \> Alle Bestellungen**.
1. Öffnen Sie die Bestellung, die Sie untersuchen oder bearbeiten möchten.
1. Wählen Sie die Ansicht **Positionen** aus.
1. Im Inforegister **Bestellpositionen** wählen Sie die zu bearbeitende Position aus.
1. Auf dem Inforegister **Positionsdetails** auf der Registerkarte **Lieferung** legen Sie **Art der Lieferung** und **Lieferbedingungen** nach Bedarf fest. Löschen Sie eines oder beide Felder, um die übereinstimmenden Einstellungen in der Kopfzeile zu verwenden.

Bei Intercompany-Aufträgen werden die Werte für die **Art der Lieferung** und **Lieferbedingungen** Felder in jeder Bestellposition werden zwischen der Bestellung und dem zugehörigen Verkaufsauftrag synchronisiert.

## <a name="sync-external-item-ids-and-descriptions-for-intercompany-orders"></a>Synchronisieren Sie externe Artikel-IDs und Beschreibungen für Intercompany-Bestellungen

Bei Intercompany-Aufträgen ist die Funktion *Automatisierung der Lieferungen zur Auftragsfertigung* ermöglicht die Synchronisierung externer Artikel-IDs und Textbeschreibungen in Bestellpositionen mit den zugehörigen Intercompany-Auftragspositionen, unabhängig davon, ob die Bestellung für die Direktlieferung bestimmt ist. Die Funktion fügt auch die Möglichkeit hinzu, das endgültige externe Kundenkonto auf einer Intercompany-Bestellung anzugeben. Das System übernimmt dann automatisch externe Artikel-IDs und Textbeschreibungen aus dem externen Kundendatensatz anstelle des (internen) Intercompany-Lieferantendatensatzes.

Führen Sie die folgenden Schritte aus, um einen Intercompany-Lieferanten einzurichten, um externe Artikel-IDs und Artikelnamen zwischen Intercompany-Bestellungen und den zugehörigen Intercompany-Aufträgen zu synchronisieren.

1. Gehen Sie zu **Beschaffung \> Kreditoren \> Alle Kreditoren**.
1. Wählen Sie den Intercompany-Kreditor zum Einrichten aus.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Allgemein** und in der Gruppe **Einrichtung** auf **Intercompany**.
1. Auf der Seite **Intercompany**, auf der Registerkarte **Bestellrichtlinien** im Abschnitt **Intercompany-Bestellung -\> Intercompany-Auftrag**, wählen Sie **Externe Element-ID und Elementname**.

Zum Angeben des endgültigen externen Kundenkontos auf einer Intercompany-Bestellung befolgen Sie diese Schritte. Das Feld **Kundenkonto** gilt nur für Intercompany-Bestellungen. Verwenden Sie es, um die Kontonummer des Kunden anzugeben, der die Ware letztendlich erhalten wird. Wenn dieses Feld festgelegt ist, übernehmen Bestellpositionen externe Artikelbeschreibungen und -nummern aus dem angegebenen Kundenkonto anstelle des in der Bestellung angegebenen Intercompany-Lieferanten. Wenn Sie das Kundenkonto später ändern, werden externe Artikelbeschreibungen und IDs aktualisiert, damit sie mit den Werten für das neue Konto übereinstimmen. Externe Artikelbeschreibungen und IDs für jede Position werden ebenfalls mit dem entsprechenden Intercompany-Auftrag synchronisiert.

1. Wechseln Sie zu **Beschaffung \> Bestellungen \> Alle Bestellungen**.
1. Öffnen Sie die Bestellung, die Sie einrichten möchten, oder erstellen Sie eine neue.
1. Wählen Sie die Ansicht **Kopfzeile** aus.
1. Im Abschnitt **Referenz** setzen Sie das Feld **Kundenkonto** auf das entsprechende externe Kundenkonto.

Führen Sie die folgenden Schritte aus, um externe Artikel-IDs und Textbeschreibungen für eine Bestellposition für eine Intercompany-Bestellung anzugeben. Die von Ihnen festgelegten Werte werden mit den zugehörigen Intercompany-Auftragspositionen synchronisiert, unabhängig davon, ob es sich bei der Bestellung um eine Direktlieferung handelt.

1. Wechseln Sie zu **Beschaffung \> Bestellungen \> Alle Bestellungen**.
1. Öffnen Sie die Bestellung, die Sie einrichten möchten, oder erstellen Sie eine neue.
1. Wählen Sie die Ansicht **Positionen** aus.
1. Im Inforegister **Bestellpositionen** wählen Sie die zu bearbeitende Position aus.
1. Auf dem Inforegister **Liniendetails** auf der **Allgemein** Registerkarte, im Abschnitt **Bestellzeile** im **Text** geben Sie eine externe Beschreibung des Artikels an, der in der ausgewählten Auftragsposition angegeben ist. Dieser Wert wird mit der zugehörigen Intercompany-Auftragsposition synchronisiert.
1. Geben Sie im Abschnitt **Referenz** im Feld **Extern** eine externe Artikel-ID für den Artikel an, der in der ausgewählten Auftragsposition angegeben ist. Dieser Wert wird mit der zugehörigen Intercompany-Auftragsposition synchronisiert.

Weitere Informationen, siehe [Einen Intercompany-Auftrag für einen externen Debitor erstellen und abrechnen](../sales-marketing/intercompany-sales-order-for-external-customer.md)
