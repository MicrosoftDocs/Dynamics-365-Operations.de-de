---
title: Sicherheitsbestandserfassung verwenden, um die Mindestdeckung für Artikel zu aktualisieren
description: In diesem Thema wird beschrieben, wie Sie die Sicherheitsbestandserfassung verwenden, um die Sicherheitsbestandsmenge für Artikel zu aktualisieren, indem Vorschläge zur Mindestdeckung basierend auf historischen Transaktionen berechnet werden.
author: ChristianRytt
ms.date: 10/28/2021
ms.topic: article
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, ReqItemTableSetup, ReqItemTable, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-10-28
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 59e4959898cd961582e1ac1d2285c0c0867ee7af
ms.sourcegitcommit: bc9e75c38e192664cde226ed3a94df5a0b304369
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/10/2021
ms.locfileid: "7790973"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage-for-items"></a>Sicherheitsbestandserfassung verwenden, um die Mindestdeckung für Artikel zu aktualisieren

[!include [banner](../../includes/banner.md)]

Durch Sicherheitslagerbestand wird eine zusätzliche Menge eines Artikels angegeben, der im Bestand gehalten wird, um das Risiko zu verringern, dass der Artikel nicht mehr vorrätig ist. Sicherheitslagerbestand wird als Ausgleichsbestand verwendet, für den Fall das Aufträge eintreffen, der Lieferant aber nicht in der Lage ist, das angeforderte Lieferdatum des Debitors einzuhalten.

Dieses Thema beschreibt, wie man die Sicherheitsbestanderfassung verwendet, um basierend auf früheren Transaktionen Vorschläge zur Mindestdeckung zu berechnen, und dann die Artikeldeckung mit dem Vorschlag aktualisiert.

## <a name="overview-of-minimum-coverage-usage"></a>Übersicht über die Mindestdeckungsnutzung

Sicherheitsbestand wird auf der Seite **Artikeldeckung** für jeden Artikel eingerichtet. Verschiedene Arten von Wiederbeschaffung werden durch verschiedene Dispositionsverfahren dargestellt. (Weitere Informationen finden Sie unter [Sicherheitslagerbestandserfüllung für Artikel](safety-stock-replenishment.md) .) Alle Dispositionsverfahren verwenden jedoch den Wert, der im Feld **Minimum** auf der Seite **Artikeldeckung** für jeden Artikel festgelegt ist. Es gibt zwei Hauptansätze für die Verwendung des Felds **Minimum**:

- **Mindestmenge für Min./Max.-Zwecke** – Dieser Ansatz verwendet die Mindestmenge zusammen mit der Min/Max-Logik. Es gilt, wenn das Feld **Dispositionsverfahren** auf *Min./Max.* für die entsprechende Position oder Dispositionssteuerungsgruppe festgelegt ist. Die **Minimum**-Menge stellt den durchschnittlichen täglichen Verbrauch multipliziert mit der Vorlaufzeit des Artikels dar.
- **Mindestmenge für Bestandsplanzwecke** – Dieser Ansatz verwendet die Mindestmenge, um einen Bestandsplan in Kombination mit Bedarfsprognosen darzustellen. Es gilt, wenn das Feld **Dispositionsverfahren** auf *Periode* oder *Bedarf* für die entsprechende Position oder Dispositionssteuerungsgruppe festgelegt ist. Die **Minimum**-Menge stellt einen Bestandsplan dar, der das gewünschte Kundenserviceniveau widerspiegelt, um Fehlbestände, Teillieferungen und Lieferzeiten zu reduzieren. Die Mindestmenge spiegelt einen Prozentsatz der Prognosegenauigkeit für einen bestimmten Artikel wider. Es stellt keine gewünschte Inventarposition dar.

Der **Minimum**-Wert kann auf drei Arten eingestellt werden:

- Manuell auf der Seite **Artikeldeckung**
- Durch das Datenverwaltungsframework (*Artikeldeckung*-Datenentitäten)
- Durch die Sicherheitsbestandsberechnung, die von Sicherheitsbestandserfassungen durchgeführt wird

## <a name="calculate-minimum-coverage-based-on-historical-usage"></a>Mindestabdeckung basierend auf der historischen Nutzung berechnen

Sicherheitsbestandserfassungen werden verwendet, um eine vorgeschlagene Mindestmenge basierend auf der historischen Verwendung eines Artikels zu berechnen, entweder für Min./Max.-Zwecke oder für Bestandsplanzwecke. Die historische Nutzung stellt alle Verbrauchstransaktionen während eines bestimmten Zeitraums dar. Diese Verbrauchstransaktionen umfassen Auftragstransaktionen und Bestandsanpassungen. Die Berechnungen identifizieren auch die Auswirkungen der vorgeschlagenen Mindestmenge auf den Bestandswert und die Veränderung des Bestandswerts im Vergleich zu den aktuellen Mindestmengen.

Jede Sicherheitsbestandserfassungsposition repräsentiert einen Artikel und seine Deckungsdimensionen. Diese Erfassungspositionen werden auf der Seite **Positionen zur Erfassung des Sicherheitsbestands** erstellt und gezeigt (**Produktprogrammplanung \> Produktprogrammplanung \> Ausführen \> Sicherheitslagerbestands-Berechnung**). Der Geschäftsprozess zur Verwendung der Sicherheitsbestandserfassung zur Berechnung der vorgeschlagenen Mindestmengen wird weiter unten in diesem Thema beschrieben.

Der Planer verwendet eine Sicherheitsbestandserfassung, um vorgeschlagene Mindestmengen für ausgewählte Artikel basierend auf dem historischen Verbrauch während ausgewählter Zeiträume zu berechnen. Die vorgeschlagenen Mindestwerte können bei Bedarf manuell überschrieben werden, und Sie können die möglichen Auswirkungen der vorgeschlagenen Mindestwerte auf den Bestandswert überprüfen. Beim Buchen der Erfassung werden die zugehörigen Mindestmengen in der Artikeldeckung automatisch aktualisiert.

### <a name="create-a-new-safety-stock-journal-name"></a>Einen neuen Sicherheitsbestands-Erfassungsname erstellen

Sie müssen mindestens einen Sicherheitsbestandserfassungsnamen erstellen, bevor Sie diesen Erfassungstyp generieren können. In der Regel verwenden Sie mehrere Erfassungsnamen, um Ihre Sicherheitsbestandsberechnungen zu trennen.

1. Gehen Sie zu **Produktprogrammplanung \> Einrichten \> Namen zur Erfassung für Sicherheitslagerbestand**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Stellen Sie die folgenden Felder für die neue Position ein:

    - **Name** – Geben Sie hier einen Kurznamen für die Erfassung ein.
    - **Beschreibung** – Geben Sie eine Beschreibung der Erfassung ein.
    - **Privat für Benutzergruppe** – Um die Zielgruppe für den aktuellen Erfassungsnamen einzuschränken, wählen Sie eine Benutzergruppe aus.
    - **Positionen nach der Buchung löschen** – Aktivieren Sie dieses Kontrollkästchen, um Erfassungspositionen beim Buchen standardmäßig zu bereinigen. Deaktivieren Sie es, um alle gebuchten Positionen beizubehalten.

    Das Feld **Erfassungstyp** ist schreibgeschützt und voreingestellt auf *Sicherheitslagerbestand*.

1. Schließen Sie die Seite.

### <a name="create-a-safety-stock-journal-and-lines"></a>Erfassung und Positionen für einen Sicherheitslagerbestand erstellen

Dieser Schritt erstellt eine Erfassung und fügt ihr automatisch Positionen hinzu. Jede Zeile identifiziert einen Artikel, seine Deckungsdimensionen und mehrere berechnete Mengen aus der Verbrauchshistorie. Die berechneten Mengen umfassen die durchschnittlichen Abgänge pro Artikeldurchlaufzeit, durchschnittliche Abgänge pro Monat und die monatliche Standardabweichung.

#### <a name="automatically-generate-journal-lines"></a>Erfassungspositionen automatisch generieren

Erfassungspositionen können nur dann automatisch generiert werden, wenn für die aktuell angezeigte Erfassung keine Positionen vorhanden sind.

Führen Sie diese Schritte aus, um automatisch Erfassungspositionen zu generieren.

1. Gehen Sie zu **Produktprogrammplanung \> Produktprogrammplanung \> Ausführen \> Sicherheitslagerbestands-Berechnung**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus. Eine neue Sicherheitsbestandserfassung wird erstellt.
1. Auf dem Inforegister **Details in der Erfassungskopfzeile** setzen Sie die folgenden Felder fest:

    - **Name** – Wählen Sie den Namen der Sicherheitsbestandserfassung aus, der die Zeile hinzugefügt werden soll.
    - **Beschreibung** – Der Standardwert ist die Beschreibung des ausgewählten Erfassungsnamens. Allerdings können Sie den Wert in diesem Feld bearbeiten.
    - **Positionen nach der Buchung löschen** – Aktivieren Sie dieses Kontrollkästchen, um Erfassungspositionen beim Buchen zu bereinigen. Deaktivieren Sie es, um alle gebuchten Positionen beizubehalten. Die Einstellung wird vom ausgewählten Erfassungsnamen geerbt.

    Das Feld **Erfassung** ist schreibgeschützt und zeigt die ID-Nummer der Erfassung an, die Sie erstellen und der Sie Zeilen hinzufügen.

1. Wählen Sie auf dem Inforegister **Erfassungspositionen** in der Werkzeugleiste **Positionen erstellen**.
1. Legen Sie im Dialogfeld **Erfassungspositionen für vorgeschlagene Mindestlagerbestände erstellen** die folgenden Felder fest:

    - **Von Datum** – Wählen Sie das Startdatum des Zeitraums, für den die Abgänge in die Berechnung einfließen sollen.
    - **Bis Datum** – Wählen Sie das Enddatum des Zeitraums, für den die Abgänge in diese Berechnung einfließen sollen. Zwischen Start- und Enddatum müssen mindestens zwei Monate liegen.
    - **Standardabweichung berechnen** – Setzen Sie diese Option auf *Ja*, um die Standardabweichung zu berechnen. Sie müssen diese Option auf *Ja* setzen, um die Option **Verwendung der Leistungsebene** zu benutzen, wenn Sie den Vorschlag berechnen (wie weiter unten in diesem Thema beschrieben).

1. Im Inforegister **Einzubeziehende Datensätze** können Sie Filter und Einschränkungen einrichten, um zu definieren, welche Artikel aufgenommen werden sollen. (Sie können beispielsweise filtern nach dem **Dispositionssteuerungsgruppe**-Wert.) Wählen Sie **Filter**, um ein standardmäßiges Dialogfeld des Abfrageeditors zu öffnen, in dem Sie Auswahlkriterien, Sortierkriterien und Verknüpfungen definieren können. Die Felder funktionieren genauso wie bei anderen Arten von Abfragen in Microsoft Dynamics 365 Supply Chain Management.
1. Im Inforegister **Im Hintergrund ausführen** wählen Sie aus, ob der Auftrag im Batch-Modus ausgeführt werden soll, und/oder richten einen wiederkehrenden Zeitplan ein. Die Felder funktionieren genauso wie bei anderen Arten von [Hintergrund-Jobs](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) im Supply Chain Management.
1. Wählen Sie **OK** aus. Positionen werden für Dimensionen erstellt, die Bestandstransaktionen haben.

#### <a name="manually-add-or-remove-journal-lines"></a>Erfassungspositionen manuell hinzufügen oder entfernen

Sie können Erfassungspositionen jederzeit manuell hinzufügen und/oder entfernen (entweder nach oder anstelle der automatischen Positionsgenerierung). Verwenden Sie die folgenden Schaltflächen in der Symbolleiste des Inforegisters **Erfassungspositionen**:

- **Neu** – Fügen Sie eine neue Position hinzu. Geben Sie dann in jede Spalte einen Wert ein, um das zu berechnende Produkt zu definieren und neue Mindestwerte anzuwenden. Da vorgeschlagene Mindestberechnungen für manuell hinzugefügte Zeilen nicht verfügbar sind, werden keine neuen **Berechnete Mindestmenge**-Werte für sie angezeigt. Daher müssen Sie die **Neue Mindestmenge**-Werte manuell eingeben. Sie können jedoch immer noch die potenziellen Auswirkungen des Werts **Neue Mindestmenge** auf den Bestandswert und die potenzielle Bestandsveränderung gegenüber dem aktuell festgelegten Mindestwert anzeigen.
- **Löschen** – Löschen Sie die ausgewählte Position.
- **Erfassungspositionen löschen** – Löschen Sie alle Positionen in der Erfassung.

### <a name="calculate-a-proposal"></a>Einen Vorschlag ermitteln

In diesem Schritt werden ein vorgeschlagener Mindestwert für jede Erfassungsposition und die potenzielle Auswirkung der Position auf den Bestandswert berechnet. (Das vorgeschlagene Minimum wird als **Berechnete Mindestmenge**-Wert gezeigt.) Sie können die Berechnung nach Bedarf mehrmals durchführen. Die Berechnung aktualisiert den **Berechnete Mindestmenge**-Wert, der für alle Erfassungspositionen angezeigt wird.

Die angezeigten Berechnungen wirken sich nicht auf die tatsächlichen Mindestmengenwerte für jedes Produkt aus, bis Sie **Buchen** im Aktivitätsbereich auswählen. Zu diesem Zeitpunkt werden die **Neue Mindestmenge**-Werte auf jedes Produkt angewendet.

1. Gehen Sie zu **Produktprogrammplanung \> Produktprogrammplanung \> Ausführen \> Sicherheitslagerbestands-Berechnung**.
1. Öffnen Sie die Erfassung, um einen Vorschlag zu berechnen. Alternativ können Sie eine neue Erfassung erstellen, wie weiter oben in diesem Thema beschrieben.
1. Wählen Sie auf dem Inforegister **Erfassungspositionen** in der Werkzeugleiste **Vorschlag ermitteln**. (Sie müssen keine Positionen auswählen.)
1. Legen Sie im Dialogfeld **Vorschlag für Mindestlagerbestand ermitteln** die folgenden Felder fest:

    - **Durchschnittliche Abgänge während Lieferzeit verwenden** – Wählen Sie diese Option zum Generieren der Werte **Berechnete Mindestmenge** basierend auf der durchschnittlichen Abgänge während des angegebenen Zeitraums. Geben Sie dann im Feld **Multiplikationsfaktor** einen Wert ein, um das Ergebnis nach Bedarf anzupassen. Geben Sie beispielsweise *1,0* ein, um den genau berechneten Durchschnitt zu verwenden, oder *1,1*, um einen zusätzlichen Puffer von 10 Prozent hinzuzufügen.
    - **Verwendung der Leistungsebene** – Wählen Sie diese Option, um ein vorgeschlagenes Minimum basierend auf der gewünschten Leistungsebene zu berechnen. Wählen Sie dann im Feld **Leistungsebene** Ihre bevorzugte Leistungsebene aus.
    - **Lieferzeitspanne** – Geben Sie einen Wert ein, um die normale Lieferzeit zu verlängern (z. B. um die Verwaltung zu ermöglichen).
    - **Berechnete Mindestmenge als neue Mindestmenge verwenden** – Setzen Sie diese Option auf *Ja* zum automatischen Kopieren von Werten aus der **Berechnete Mindestmenge**-Spalte in die **Neue Mindestmenge**-Spalte für alle Positionen nach Abschluss der Berechnung. Wenn Sie diese Option auf *Nein* setzen, wird der **Aktuelle Mindestmenge**-Wert in die **Neue Mindestmenge**-Spalte für alle Positionen kopiert. Sie müssen dann die **Neue Mindestmenge**-Werte nach Bedarf manuell bearbeiten.

1. Im Inforegister **Im Hintergrund ausführen** wählen Sie aus, ob der Auftrag im Batch-Modus ausgeführt werden soll, und/oder richten einen wiederkehrenden Zeitplan ein. Die Felder funktionieren genauso wie bei anderen Arten von [Hintergrund-Jobs](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) im Supply Chain Management.
1. Wählen Sie **OK** aus. Die Ergebnisse der Berechnung werden in der **Berechnete Mindestmenge**-Spalte im Inforegister **Erfassungspositionen** angezeigt. Im Moment sind die Werte nur vorgeschlagene Werte, die noch nicht auf Ihre Produkte angewendet wurden.

### <a name="update-minimum-quantity"></a>Mindestmenge aktualisieren

Sie können eine beliebige Position in einer Sicherheitsbestandserfassung auswählen und den Wert ihres Felds **Neue Mindestmenge** manuell überschreiben.

1. Gehen Sie zu **Produktprogrammplanung \> Produktprogrammplanung \> Ausführen \> Sicherheitslagerbestands-Berechnung**.
1. Öffnen Sie die Erfassung zur Bearbeitung. Alternativ können Sie eine neue Erfassung erstellen, wie weiter oben beschrieben.
1. Suchen Sie im **Erfassungspositionen**-Inforegister die anzupassende Position und bearbeiten Sie dann den Wert in der Spalte **Neue Mindestmenge**. Sie können beispielsweise den **Neue Mindestmenge**-Wert so festlegen, dass er mit dem **Berechnete Mindestmenge**-Wert übereinstimmt. Wenn der **Berechnete Mindestmenge**-Wert *0* (null) ist, können Sie den gewünschten zukünftigen Wert eingeben.

### <a name="post-the-new-minimum-quantity-and-validate-the-result"></a>Buchen Sie die neue Mindestmenge und überprüfen Sie das Ergebnis

Führen Sie die folgenden Schritte aus, um die neue Mindestmenge zu buchen und das Ergebnis zu überprüfen.

1. Gehen Sie zu **Produktprogrammplanung \> Produktprogrammplanung \> Ausführen \> Sicherheitslagerbestands-Berechnung**.
1. Öffnen Sie die Erfassung, um dafür neue Mindestmengen zu buchen. Alternativ können Sie eine neue Erfassung erstellen, wie weiter oben beschrieben.
1. Wählen Sie im Aktionsbereich **Buchen** aus.
1. Legen Sie im Dialogfeld **Erfassung buchen** das Feld **Alle Buchungsfehler in eine neue Erfassung übertragen** nach Bedarf fest. Wählen Sie dann **OK**, um die Erfassung zu buchen.
1. Wenn Sie den Wert **Neue Mindestmenge** für eine Position im Inforegister **Erfassungspositionen** geändert haben, können Sie die Änderung bestätigen, indem Sie die folgenden Schritte ausführen:

    1. Wählen Sie für die von Ihnen bearbeitete Position den Link in der Spalte **Artikelnummer**.
    1. Wählen Sie im Dialogfeld **Produktinformationen** den Link im Feld **Artikelnummer**, um den zugehörigen freigegebenen Produktdatensatz zu öffnen.
    1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Plan** in der Gruppe **Planungshorizont** die Option **Artikeldeckung** aus.
    1. Beachten Sie, dass der **Minimum**-Wert für den Standort und Lagerort, den Sie mithilfe der gebuchten Sicherheitsbestandserfassung angepasst haben, jetzt aktualisiert wurde, damit er mit Ihrer Bearbeitung übereinstimmt.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Sicherheitslagerbestandserfüllung für Artikel](safety-stock-replenishment.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
