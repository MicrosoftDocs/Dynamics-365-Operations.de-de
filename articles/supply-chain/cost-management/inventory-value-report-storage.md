---
title: Lagerwertberichte
description: Dieses Thema beschreibt, wie man Lagerwertberichte einrichtet, generiert und verwendet. Diese Berichte enthalten Details zu den physischen und finanziellen Mengen und Beträgen Ihrer Bestände.
author: banluo-ms
ms.date: 10/19/2021
ms.topic: article
ms.search.form: InventValueProcess, InventValueReportSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: banluo
ms.search.validFrom: 2021-10-19
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 3da92c384d3074335067433120eccc97d11b6b81
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103939"
---
# <a name="inventory-value-reports"></a>Lagerwertberichte

[!include [banner](../includes/banner.md)]

Lagerwertberichte enthalten Details zu den physischen und finanziellen Mengen und Beträgen Ihrer Bestände. Sie können die Berichte auf viele verschiedene Arten anzeigen lassen. Sie können beispielsweise Summen oder Buchungen anzeigen lassen oder nach Artikeln oder einen Zeitbereich filtern. Sie können die Werte des Wareneinsatzes (COGS) oder die Werte der Ressourcen in Fertigung (RIF) anzeigen lassen und andere Optionen festlegen.

Mit Lagerwertberichten können Sie die folgenden Aufgaben ausführen:

- Hauptbuch und Bestand abstimmen.
- Den verfügbaren Lagerbestand und die Werte für einen bestimmten Zeitraum konsultieren.
- Berichtskonfigurationen erstellen, die auf einen bestimmten Zweck zugeschnitten sind.
- Berichtskonfigurationen abspeichern, damit sie mehrfach verwendet werden können.
- Bereiche hinzufügen, um beim Ausführen eines Berichts Daten zu filtern.

## <a name="types-of-inventory-value-report"></a>Typen von Lagerwertberichten

Es gibt zwei Typen von Lagerwertberichten: **Lagerwert** (der Standardbericht) und **Lagerwert-Berichtsspeicher**.

### <a name="standard-inventory-value-report"></a>Standardlagerwertbericht

Der Standardbericht **Lagerwert** ist ein einfacher Bericht, mit dem Sie die enthaltenen Informationen auswählen und diese dann auf dem Bildschirm anzeigen lassen können. Die Ergebnisse werden nicht gespeichert. Es bietet auch keine interaktiven Funktionen zum Filtern, Aufschlüsseln, Browsen oder Exportieren. Aus diesen Gründen sollten Sie in den meisten Fällen den Bericht **Lagerwert-Berichtsspeicher** verwenden.

### <a name="inventory-value-report-storage-report"></a>Bericht „Lagerwert-Berichtsspeicher“

Der Bericht **Lagerwert-Berichtsspeicher** gibt entweder eine interaktive Seite in Microsoft Dynamics 365 Supply Chain Management oder ein exportiertes Dokument in einem von mehreren Formaten heraus.

Wenn Sie den Bericht in Ihrem Browser anzeigen, werden die Spalten und Summenbilanzen je nach Ihrem konfigurierten Layout dynamisch angepasst. Sie können die Ergebnisse sortieren, filtern, die Daten aufschlüsseln und vieles mehr.

Berichtsergebnisse werden in der **Inventarwert**-Datenentität gespeichert. Daher können Sie die Ergebnisse filtern und in ein Format wie CSV (Comma Separated Values) oder ein Microsoft Excel-Format exportieren.

Der **Lagerwert-Berichtsspeicher** ist hilfreich, wenn die Ausgabe viele Zeilen enthält. Sie haben beispielsweise 50.000 Artikel und 300 Geschäfte wurden als Lager eingerichtet. In diesem Fall enthält die Ausgabe viele Positionen, wenn Sie Bestandsendguthaben nach Artikel, Standort und Lager anfordern.

> [!NOTE]
> Der Bericht **Lagerwert-Berichtsspeicher** enthält keine Zwischensummen, die im Berichtslayout definiert sind. Er enthält auch keine Hauptbuchsalden, wenn diese Salden im Berichtslayout definiert sind. Die Abstimmung mit dem Hauptbuch muss unter Verwendung von Probesalden erfolgen. Der Standard-**Lagerwert** bericht dagegen enthält diese Zwischensummen und Salden.

## <a name="turn-the-inventory-value-report-storage-feature-on-or-off"></a>Funktion „Lagerwert-Berichtsspeicher“ ein- oder ausschalten

Ab Supply Chain Management Version 10.0.25 ist diese Funktion standardmäßig aktiviert. Administratoren können diese Funktionalität an- oder ausschalten, indem Sie nach der Funktion *Lagerwert-Berichtsspeicher* im Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) suchen.

## <a name="define-inventory-value-report-configurations"></a><a name="report-configuration"></a>Konfigurationen von Lagerwertberichten definieren

Verwenden Sie die Seite **Lagerwertberichte**, um den Inhalt einzurichten, der in den verschiedenen Arten von Lagerwertberichten enthalten ist. Sie können eine beliebige Anzahl von Berichttypen festlegen.. Jedes Mal, wenn Sie einen Lagerwertbericht erstellen, wählen Sie einen Berichtstyp aus.

1. Wechseln Sie zu **Kostenverwaltung \> Einrichtung der Bestandsbuchhaltungsrichtlinien \> Lagerwertberichte**.
1. Führen Sie einen dieser Schritte aus:

    - Um einen vorhandenen Bericht zu bearbeiten, wählen Sie sie im Listenbereich aus und wählen Sie dann **Bereich** im Aktivitätsbereich.
    - So erstellen Sie einen neuen Bericht: Wählen Sie im Aktivitätsbereich **Neu**.

1. Legen Sie in der Kopfzeile des neuen oder ausgewählten Berichts die folgenden Felder fest:

    - **ID**: Geben Sie einen kurzen Bezeichner für den Bericht ein. Dieser Wert muss in allen Lagerwertberichtskonfigurationen eindeutig sein. Er kann nicht bearbeitet werden, nachdem Sie eine neue Konfiguration gespeichert haben.
    - **Name**: Geben Sie einen beschreibenden Namen für den Bericht ein.

1. Wenn Sie eine neue Berichtskonfiguration erstellen, wählen Sie im Aktivitätsbereich **Speichern**, um die verbleibenden Felder verfügbar zu machen.
1. Legen Sie im Inforegister **Allgemein** die folgenden Felder fest:

    - **Datumsintervall**: Wählen Sie ein vordefiniertes Datumsintervall. Sie können dieses Datumsintervall beim Ausführen des Berichts überschreiben.
    - **Bereich**: Wählen Sie entweder *Buchungsdatum* oder *Transaktionsuhrzeit*, abhängig von Datum und Uhrzeit, die beim Abrufen von Datensätzen für den Bericht verwendet werden sollen.
    - **Dimensionssatz**: Wählen Sie den Dimensionssatz aus, für den die Daten ausgeführt werden sollen. (Die Dimensionen sind im Hauptbuch definiert.) Sie können beispielsweise die Daten für *Hauptkonto* oder für *Hauptkonto + Unternehmenseinheit* ausführen. Der von Ihnen ausgewählte Dimensionssatz darf nicht mehr als zwei Dimensionen aufweisen. Weitere Informationen finden Sie unter [Finanzdimensionssätze](../../finance/general-ledger/financial-dimension-sets.md).

1. Legen Sie im Inforegister **Spalten** die folgenden Felder fest. Diese Felder steuern die Spalten, die Ihr Bericht enthält, und die Datentypen, die diese Spalten enthalten.

    - **Bestand**: Setzen Sie diese Option auf *Ja*, um die Lagerwerte anzuzeigen. Anschließend können Sie diese Werte mit den Salden des Hauptbuchkontos abstimmen.
    - **RIF**: Setzen Sie diese Option auf *Ja*, um die RIF-Werte anzuzeigen. Anschließend können Sie diese Werte mit den Salden des RIF-Kontos im Hauptbuch abstimmen. Wenn Sie diese Option auf *Ja* setzen, zeigt der Bericht nur die physischen Mengen und Bestandsmengen mit RIF-Status an. Produktionsaufträge mit dem RIF-Status wurden entnommen oder als fertig gemeldet, aber noch nicht beendet.
    - **Verzögerter Wareneinsatz**: Setzen Sie diese Option auf *Ja*, um eine Spalte anzuzeigen, die die physischen Mengen und Bestandsmengen für einen verzögerten Wareneinsatz anzeigt. Verzögerte Wareneinsätze werden unter Verwendung physischer Mengen und Beträge angezeigt, da sie Lieferscheinmengen und -beträge ausgleichen.
    - **COGS**: Setzen Sie diese Option auf *Ja*, um eine Spalte anzuzeigen, die die finanziellen Mengen und Bestandsmengen für COGS anzeigt. COGS werden unter Verwendung finanzieller Mengen und Beträge angezeigt, da sie Rechnungsmengen und -beträge ausgleichen.
    - **Gewinn und Verlust**: Setzen Sie diese Option auf *Ja*, um eine Spalte anzuzeigen, die den wertmäßigen Betrag anzeigt, der auf die Gewinn- und Verlustkonten für den Bestand gebucht wurde.
    - **Kumulierte Kontowerte zum Vergleich drucken**: Setzen Sie diese Option auf *Ja*, um eine Spalte anzuzeigen, die das Saldo des Hauptbuchkontos anzeigt. Auf diese Weise müssen Sie die Probebilanz nicht überprüfen. Diese Option funktioniert nur mit dem Standard-**Lagerwert** bericht, nicht mit dem Bericht **Lagerwert-Berichtsspeicher**. Nachdem Sie diese Option auf *Ja* gesetzt haben, müssen Sie die folgenden Felder verwenden, um jedes Hauptbuchkonto anzugeben, das Sie auflisten möchten, abhängig von den Optionen für **Finanzpositionen**, die Sie aktiviert haben.

        > [!NOTE]
        > Wenn Sie für eines dieser Felder ein *Summen* konto ausgewählt haben, wird sowohl der Betrag jedes Lagerkontos, der im Summenkonto enthalten ist, als auch der Betrag des Summenkontos angezeigt.

        - **Lagerkonto**: Geben Sie das Hauptbuchkonto an, für das Bestandsinformationen angezeigt werden sollen. (Sowohl die Option **Bestand** als auch die Option **Kumulierte Kontowerte zum Vergleich drucken** muss auf *Ja* gesetzt sein.)
        - **RIF-Konto**: Geben Sie das Hauptbuchkonto an, für das RIF-Informationen angezeigt werden sollen. (Sowohl die Option **RIF** als auch die Option **Kumulierte Kontowerte zum Vergleich drucken** müssen auf *Ja* gesetzt sein.)
        - **Verzögertes Wareneinsatzkonto**: Geben Sie das Hauptbuchkonto an, für das verzögerte Wareneinsatzinformationen angezeigt werden sollen. (Sowohl die Option **Verzögerter Wareneinsatz** als auch die Option **Kumulierte Kontowerte zum Vergleich drucken** müssen auf *Ja* gesetzt sein.)
        - **Wareneinsatzkonto**: Geben Sie das Hauptbuchkonto an, für das COGS-Informationen angezeigt werden sollen. (Sowohl die Option **COGS** als auch die Option **Kumulierte Kontowerte zum Vergleich drucken** müssen auf *Ja* gesetzt sein.)

    - **Physische Werte und Finanzwerte zusammenfassen**: Setzen Sie diese Option auf *Ja*, um eine Spalte anzuzeigen, die die Gesamtbestandsmenge und den Bestandsbetrag anzeigt (eine Zusammenfassung sowohl der physischen als auch der finanziellen Bestandswerte). Wenn diese Option auf *Nein* gestellt ist, zeigt der Bericht sowohl physische als auch finanzielle Bestandswerte an.
    - **Nicht auf das Sachkonto gebuchte Werte einbeziehen**: Setzen Sie diese Option auf *Ja*, um eine Spalte anzuzeigen, die die Buchungen anzeigt, die nie in das Hauptbuch gebucht wurden. Buchungen für die folgenden Arten von Artikeln werden möglicherweise nicht in das Hauptbuch gebucht:

        - Erhaltene und noch nicht fakturierte Artikel, wenn die Option **Physischen Bestand buchen** für die entsprechende Artikelmodellgruppe deaktiviert ist.
        - Erhaltene und noch nicht fakturierte Artikel, wenn die Option **Produktzugang auf Sachkonto buchen** im Inforegister **Produktzugang** auf der Registerkarte **Allgemein** der Seite **Kreditorenkontenparameter** deaktiviert ist (**Kreditorenkonten \> Setup \> Kreditorenkontenparameter**).

    - **Durchschnittliche Einheitenkosten berechnen**: Setzen Sie diese Option auf *Ja*, um eine Spalte anzuzeigen, die die durchschnittlichen Einheitenkosten anzeigt. Die durchschnittlichen Einheitenkosten sind die Gesamtmenge geteilt durch den Gesamtbetrag.
    - **Gesamtmenge und -wert**: Setzen Sie diese Option auf *Ja*, um Spalten anzuzeigen, die die Gesamtmenge des physischen Bestands (sowie die finanziellen Mengen) und den Gesamtbetrag des physischen Bestand (sowie die finanziellen Beträge) anzeigt. Sie können diese Option nur dann auf *Ja* festlegen, wenn die Option **Physische Werte und Finanzwerte zusammenfassen** auf *Nein* festgelegt ist.
    - **Lagerungsdimensionen**: Wählen Sie in diesem Raster das Kästchen **Ansicht** für jede Dimension aus, die Sie im Bericht anzeigen möchten. Nur Dimensionen, bei denen die Option **Wertmäßiger Bestand** aktiviert ist, zeigen Werte im Bericht an. Andere Dimensionen zeigen nur leere Spalten. Für die Dimensionen, die Sie zum Anzeigen auswählen, können Sie das Kontrollkästchen **Gesamt** auswählen, um auch Summen einzuschließen.
    - **Ressourcen-ID**: Stellen Sie die Option **Ansicht** auf *Ja*, um eine Spalte anzuzeigen, die den Artikel für jede Zeile identifiziert. Setzen Sie die Option **Gesamt** auf *Ja*, um auch Summen einzubeziehen. Je nach Art des Artikels, der in jeder Zeile aufgeführt ist, zeigt die Spalte eine der folgenden Arten von Informationen an:

        - **Material**: Die Spalte zeigt den `ItemID`-Feldwert für den entsprechenden Materialdatensatz an.
        - **Arbeit**: Die Spalte zeigt den `WorkCenterID`-Feldwert für den entsprechenden Arbeitsdatensatz an.
        - **Indirekte Kosten**: Die Spalte zeigt den `CodeID`-Feldwert für den entsprechenden Kostendatensatz an.

        Wenn die Option **Ansicht** auf *Nein* sowohl für das Feld **Ressourcen-ID** als auch das Feld **Ressourcengruppe** gesetzt ist, wird nur ein Gesamtbestandswert angezeigt, der auf den von Ihnen ausgewählten Bestandsdimensionen basiert.

    - **Ressourcengruppe**: Stellen Sie die Option **Ansicht** auf *Ja*, um eine Spalte anzuzeigen, die die Ressourcengruppe für jede Zeile identifiziert. Setzen Sie die Option **Gesamt** auf *Ja*, um auch Summen einzubeziehen. Je nach Art des Artikels, der in jeder Zeile aufgeführt ist, zeigt die Spalte eine der folgenden Arten von Informationen an:

        - **Material**: Die Spalte zeigt den `ItemGroup`-Feldwert für den entsprechenden Materialdatensatz an.
        - **Arbeit**: Die Spalte zeigt den `WorkcenterGroup`-Feldwert für den entsprechenden Arbeitsdatensatz an.
        - **Indirekte Kosten**: Die Spalte zeigt den `CostGroup`-Feldwert für den entsprechenden Kostendatensatz an. (Der `CostGroupType`-Wert muss *Indirekt* sein.)

        Wenn die Option **Ansicht** auf *Nein* sowohl für das Feld **Ressourcen-ID** als auch das Feld **Ressourcengruppe** gesetzt ist, wird nur ein Gesamtbestandswert angezeigt, der auf den von Ihnen ausgewählten Bestandsdimensionen basiert.

1. Legen Sie auf dem Inforegister **Zeilen** die folgenden Felder fest: Mit diesen Feldern können Sie dem Bericht entsprechende RIF-bezogene Unterabschnitte hinzufügen oder entfernen.

    - **Material**: Setzen Sie diese Option auf *Ja*, um Informationen über Materialien anzuzeigen. *Material* ist ein Standardressourcentyp, da Materialien in allen Berichtskonfigurationen enthalten sein müssen, um eine zuverlässige Ausgabe zu erstellen.
    - **Arbeit**: Setzen Sie diese Option auf *Ja*, um Arbeitskosten von RIF zu zeigen.
    - **Indirekte Kosten**: Setzen Sie diese Option auf *Ja*, um indirekte Kosten von RIF zu zeigen.
    - **Direktes Outsourcing**: Setzen Sie diese Option auf *Ja*, um direktes Outsourcing von RIF zu zeigen. Diese Informationen sind für Fremdarbeit hilfreich.
    - **Detailebene**: Wählen Sie eine Ansichtsoption für den Bericht:

        - *Buchungen*: Zeigen Sie alle relevanten Buchungen im Bericht an. Beachten Sie, dass beim Anzeigen von Berichten mit einem großen Buchungsvolumen möglicherweise Leistungsprobleme auftreten können. Wenn Sie diese Ansichtsoption nutzen möchten, empfehlen wir Ihnen daher, den Bericht **Lagerwert-Berichtsspeicher** zu verwenden.
        - *Summen*: Ansicht des Gesamtergebnisses.

    - **Anfangssaldo einbeziehen**: Setzen Sie diese Option auf *Ja*, um den Anfangssaldo anzuzeigen. Diese Option ist nur verfügbar, wenn das Feld **Detailebene** auf *Buchungen* gesetzt wird.

## <a name="generate-an-inventory-value-report-storage-report"></a>Einen Lagerwert-Berichtsspeicher-Bericht generieren

Befolgen Sie diese Schritte, um einen **Lagerwert-Berichtsspeicher**-Bericht zu erstellen und zu speichern.

1. Gehen Sie zu **Kostenmanagement \> Anfragen und Berichte \> Lagerbericht zum Bestandswert**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie im Dialogfeld **Lagerwert** auf dem Inforegister **Parameter** die folgenden Felder fest:

    - **Name**: Geben Sie einen eindeutigen Namen für den Bericht ein.
    - **ID**: Wählen Sie für den Bericht [Lagerwertberichtskonfigurationen](#report-configuration) aus. Die Konfiguration legt Optionen für die Spalten und Zeilen fest, die in Ihren Bericht aufgenommen werden.
    - **Datumsintervall**: Verwenden Sie die Felder in diesem Abschnitt, um zu definieren, welche Datensätze in den Bericht aufgenommen werden. Um das Datumsintervall zu definieren, können Sie entweder einen voreingestellten Bereich (relativ zum Berichtserstellungsdatum) im Feld **Datumsintervallcode** auswählen, oder Sie wählen bestimmte Daten in den Feldern **Startdatum** und **Enddatum**.

1. Richten Sie in den Abschnitten **Einzubeziehende Datensätze** Filter und Einschränkungen ein, um festzulegen, welche Daten in den Bericht aufgenommen werden sollen. Wählen Sie **Filter**, um einen Standard-Abfrage-Editor-Dialog anzuzeigen, in dem Sie Auswahlkriterien, Sortierkriterien und Verknüpfungen definieren können. Die Felder funktionieren genauso wie bei anderen Arten von Abfragen im Supply Chain Management. Alle diese Filter werden auf die Lagerbuchungen angewendet, aber nicht auf den Hauptbuchsaldo. Berücksichtigen Sie dieses Verhalten, wenn Sie Ihre Filter einrichten. Andernfalls stellen Sie vielleicht eine Diskrepanz zwischen dem Lagerbestand und dem Hauptbuch fest.
1. Im Inforegister **Im Hintergrund ausführen** geben Sie an, wie, wann und wie oft der Bericht erstellt wird. Die Felder funktionieren genauso wie bei anderen Arten von [Hintergrund-Jobs](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) im Supply Chain Management.

    > [!NOTE]
    > Dieser Bericht wird immer als Teil eines Batchauftrags ausgeführt.

1. Wählen Sie **OK**, um Ihre Einstellungen zu übernehmen und das Dialogfeld zu schließen.

Nach Abschluss des Batchauftrags wird der Bericht auf der Seite **Lagerbericht zum Bestandswert** angezeigt. Sie müssen die Seite möglicherweise aktualisieren, um den Bericht anzuzeigen.

> [!IMPORTANT]
> In der ausgewählten Lagerwertberichtskonfiguration erhalten Sie möglicherweise einen falschen Anfangssaldo, wenn Sie das gleiche Datum sowohl im Feld **Startdatum** als auch im Feld **Enddatum** und wenn Sie außerdem die Option **Anfangssaldo einbeziehen** auf *Ja* gesetzt haben.

## <a name="explore-an-inventory-value-report-storage-report"></a>Einen Lagerwert-Berichtsspeicher-Bericht kennenlernen

Nachdem Sie einen Bericht erstellt haben, können Sie ihn jederzeit mit den folgenden Schritten einsehen und untersuchen.

1. Gehen Sie zu **Kostenmanagement \> Anfragen und Berichte \> Lagerbericht zum Bestandswert**.
1. Wählen Sie in der Liste einen Bericht aus. Die Seite zeigt die Details der [Lagerwertberichtskonfiguration](#report-configuration) an, die zum Generieren des ausgewählten Berichts verwendet wurde.
1. Wählen Sie im Aktivitätsbereich **Details anzeigen** aus, um den Berichtsinhalt anzuzeigen.
1. Durchsuchen Sie den Bericht, indem Sie einen der folgenden Schritte ausführen:

    - Wie für die meisten Standardseiten in Supply Chain Management können Sie fast eine beliebige Spaltenüberschrift auswählen, um das Raster nach den Werten in dieser Spalte zu sortieren oder zu filtern.
    - Verwenden Sie das Feld **Filter**, um den Bericht nach einem beliebigen Wert in einer der mehreren verfügbaren Spalten zu filtern.
    - Verwenden Sie das Ansichtsmenü (über dem Feld **Filter**), um Ihre bevorzugten Kombinationen von Sortier- und Filteroptionen zu speichern und zu laden.

## <a name="export-an-inventory-value-report-storage-report"></a>Einen Lagerwert-Berichtsspeicher-Bericht exportieren

Jeder Bericht, den Sie generieren, wird in der Datenentität **Lagerwert**. Sie können die Standarddatenverwaltungsfunktionen des Supply Chain Management verwenden, um Daten aus dieser Entität in jedes unterstützte Datenformat, einschließlich CSV oder Excel, zu exportieren.

Das folgende Beispiel zeigt, wie Sie einen **Lagerwertbericht-Berichtsspeicher**-Bericht exportieren.

1. Wechseln Sie zu **Systemverwaltung \> Arbeitsbereiche \> Datenverwaltung**.
1. Im Abschnitt **Import/Export** wählen Sie die Kachel **Export** aus.
1. Auf der angezeigten Seite **Export** richten Sie den Exportauftrag ein. Geben Sie zunächst einen Gruppennamen für den Auftrag ein.
1. Im Abschnitt **Ausgewählte Entitäten** wählen Sie **Entität hinzufügen**.
1. Im angezeigten Dialogfeld legen Sie die folgenden Felder fest:

    - **Entitätsname** – Wählen Sie *Lagerwert* aus.
    - **Zieldatenformat** – Wählen Sie das Format aus, in das Daten exportiert werden sollen.

1. Wählen Sie **Hinzufügen**, um die neue Zeile hinzuzufügen, und wählen Sie dann **Schließen**, um das Dialogfenster zu schließen.
1. Normalerweise exportieren Sie jeweils nur einen Bericht. Richten Sie zum Exportieren eines einzelnen Berichts einen Filter für die Zeile ein, die Sie gerade zum Dialogfeld **Anfrage** hinzugefügt haben. Auf diese Weise können Sie definieren, welcher Bericht aus der **Lagerwert**-Entität in Ihrem Export enthalten ist. Folgen Sie diesen Schritten, um die folgenden Filteroptionen so festzulegen, dass ein einzelner Bericht exportiert wird:

    1. Wählen Sie auf der Registerkarte **Bereich** die Option **Hinzufügen**, um eine Zeile hinzuzufügen.
    2. Legen Sie das Feld **Tabelle** auf *Lagerwert* fest.
    3. Legen Sie das Feld **Abgeleitete Tabelle** auf *Lagerwert* fest.
    4. Setzen Sie das Feld **Feld** auf das Feld, nach dem Sie filtern möchten. Normalerweise verwenden Sie das Feld **Ausführungsname** und/oder **Ausführungszeit**.
    5. Stellen Sie das Feld **Kriterien** auf den Wert, nach dem Sie im ausgewählten Feld suchen möchten. (Wenn Sie das Feld **Ausführungsname** im vorherigen Schritt ausgewählt haben, ist dieser Wert der Name des Berichts. Wenn Sie das Feld **Ausführungszeit** ausgewählt haben, ist es die Zeit, zu der der Bericht erstellt wurde.)
    6. Fügen Sie nach bedarf weitere Zeilen zur Registerkarte **Bereich** hinzu, bis Sie den gesuchten Bericht eindeutig identifiziert haben.

1. Wählen Sie **OK**, um Ihre Einstellungen zu speichern und das Dialogfeld zu schließen.
1. Wählen Sie **Speichern**, um Ihre Export-Einstellungen zu speichern.
1. Wählen Sie auf der Registerkarte **Exportoptionen** die Option **Jetzt exportieren**, um die Exportdatei zu erzeugen.
1. Die Seite **Ausführungszusammenfassung** wird geöffnet, auf der Sie den Status Ihres Exportauftrags und eine Liste der exportierten Entitäten sehen können. Wählen Sie im Abschnitt **Verarbeitungsstatus der Entität** die Entität **Lagerwert** aus der Liste, und wählen Sie dann **Datei herunterladen**, um die von dieser Entität exportierten Daten herunterzuladen.

Weitere Informationen über die Verwendung der Datenverwaltung für den Datenexport finden Sie unter [Übersicht über Datenimport- und -exportjobs](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).

## <a name="generate-a-standard-inventory-value-report"></a>Einen Standardlagerwertbericht generieren

Verwenden Sie das folgende Verfahren, um einen **Standardlagerwertbericht** zu erstellen.

1. Gehen Sie zu **Kostenverwaltung \> Anfragen und Berichte \> Bestandsbuchhaltung – Statusberichte \> Lagerwert**.
1. Legen Sie im Dialogfeld **Lagerwertbericht** auf dem Inforegister **Parameter** die folgenden Felder fest:

    - **Name**: Geben Sie einen eindeutigen Namen für den Bericht ein.
    - **ID**: Wählen Sie für den Bericht [Lagerwertberichtskonfigurationen](#report-configuration) aus. Die Konfiguration legt Optionen für die Spalten und Zeilen fest, die in Ihren Bericht aufgenommen werden.
    - **Datumsintervall**: Verwenden Sie die Felder in diesem Abschnitt, um zu definieren, welche Datensätze in den Bericht aufgenommen werden. Um das Datumsintervall zu definieren, können Sie entweder einen voreingestellten Bereich (relativ zum Berichtserstellungsdatum) im Feld **Datumsintervallcode** auswählen, oder Sie wählen bestimmte Daten in den Feldern **Startdatum** und **Enddatum**.

1. Richten Sie in den Abschnitten **Einzubeziehende Datensätze** Filter und Einschränkungen ein, um festzulegen, welche Daten in den Bericht aufgenommen werden sollen. Wählen Sie **Filter**, um einen Standard-Abfrage-Editor-Dialog anzuzeigen, in dem Sie Auswahlkriterien, Sortierkriterien und Verknüpfungen definieren können. Die Felder funktionieren genauso wie bei anderen Arten von Abfragen im Supply Chain Management.
1. Im Inforegister **Im Hintergrund ausführen** geben Sie an, wie, wann und wie oft der Bericht erstellt wird. Die Felder funktionieren genauso wie bei anderen Arten von [Hintergrund-Jobs](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) im Supply Chain Management.
1. Wählen Sie **OK**, um Ihre Einstellungen zu übernehmen und das Dialogfeld zu schließen. Der Bericht erscheint.

## <a name="reading-inventory-value-reports"></a>Lagerwertberichte lesen

Dieser Abschnitt enthält einige Anleitungen zum Lesen und Verstehen eines Lagerwertberichts.

Supply Chain Management unterstützt die folgenden zwei wichtigen Konzepte, die mit dem Bestandsstatus zusammenhängen:

- **Finanzielle Werte aktualisiert**: Dieses Konzept gibt an, dass die Bestandsbuchungen bereits fakturiert sind. Bei Produktionsaufträgen kennzeichnet es das Ende eines Produktionsauftrags.
- **Physische Werte aktualisiert**: Dieses Konzept zeigt an, dass die Bestandsbuchungen noch nicht in Rechnung gestellt, aber eingegangen oder versendet wurden. Bei Produktionsaufträgen zeigt es an, dass Material entnommen oder der Produktionsauftrag als fertig gemeldet wurde.

Wenn Sie diese beiden Konzepte verstehen, sollten Sie auch die folgenden Spalten in der Berichtsausgabe leicht verstehen:

- **Bestand: wertmäßige Menge**: Die Menge, die wertmäßig aktualisiert wurde.
- **Bestand: wertmäßiger Betrag**: Der Betrag des Bestands, der wertmäßig aktualisiert wurde.
- **Bestand: gebuchte physische Menge**: Die Menge, die physisch aktualisiert wurde.
- **Bestand: gebuchter physischer Betrag**: Der Betrag des Bestands, der physisch aktualisiert wurde.
- **Bestand: nicht gebuchte physische Menge**: Die Menge, die Bestandsbuchungen enthält, aber noch nicht in das Hauptbuch gebucht wurde. Sie haben beispielsweise eine Artikelmodellgruppe, in der die Optionen **Physischen Bestand buchen** und **Finanziellen Bestand buchen** deaktiviert sind, und Sie haben einen Artikel, der mit dieser Gruppe verknüpft ist. Anschließend legen Sie eine Bestellung an, empfangen sie und fakturieren sie. Wenn Sie zu diesem Zeitpunkt den Lagerwertbericht für den Artikel überprüfen, werden Sie feststellen, dass die Menge und der Wert der Bestellung in den Spalten **Bestand: nicht gebuchte physische Menge** und **Bestand: nicht gebuchter physischer Betrag** angezeigt werden.
- **Bestand: nicht gebuchter physischer Betrag**: Sie können Ihre Berichte so einrichten, dass sie nicht gebuchte Beträge anzeigen. Wenn Sie den Bericht jedoch für die Abstimmung des Lagerbestands verwenden, verwenden Sie diesen Wert nicht. Andernfalls wird der Betrag nicht in das Hauptbuch gebucht.
- **Bestand: Menge**: Die Gesamtmenge aller Mengenspalten im Bericht.
- **Bestand: Betrag**: Die Gesamtmenge aller Betragsspalten im Bericht. Verwenden Sie diese Spalte bei der Abstimmung des Lagerbestands nicht, wenn Ihr Bericht die Spalte **Bestand: nicht gebuchter physischer Betrag** enthält. In diesem Fall müssen Sie den Betrag **Bestand: nicht gebuchter physischer Betrag** vom Gesamtbetrag ausschließen.
- **Durchschnittliche Einheitenkosten**: Der Gesamtbetrag geteilt durch die Gesamtmenge.

In der Regel verwenden Sie einen Lagerwertbericht, um den Lagerwert und die Menge anzuzeigen. Manchmal zeigt der Bericht jedoch nicht alle relevanten Lagerungsdimensionen an. Wenn die erwarteten Dimensionen nicht angezeigt werden, überprüfen Sie die folgenden Einstellungen:

- Überprüfen Sie die Artikelspeicher- und Rückverfolgungsangabengruppen. Nur Dimensionen, bei denen die Option **Wertmäßiger Bestand** aktiviert ist, können im Bericht angezeigt werden.
- Gehen Sie zu **Kostenverwaltung \> Einrichtung der Bestandsbuchhaltungsrichtlinien \> Lagerwertberichte**, wählen Sie die Berichtskonfiguration aus, die Sie zum Generieren des Berichts verwendet haben, und vergewissern Sie sich, dass die erforderlichen Lagerungsdimensionen in der Spalte **Ansicht** ausgewählt sind.

Sie haben beispielsweise einen Artikel mit der Artikelnummer *A0001*. In der Lagerdimensionsgruppe ist nur die Standort für den wertmäßigen Bestand aktiviert. Sowohl der Standort als auch der Lagerort sind für den physischen Bestand aktiviert. In der Nachverfolgungsangabengruppe ist die Chargennummer für den physischen Bestand aktiviert, jedoch nicht für den wertmäßigen Bestand. Anschließend verwenden Sie eine Berichtskonfiguration, in der Standort, Lagerort und Chargennummer ausgewählt sind. Wenn Sie den Bericht anzeigen, sehen Sie nur einen Wert für den Standort. Die Spalten für Lagerort und Chargennummer sind leer. Wie dieses Beispiel zeigt, können Lagerwertberichte nur Lagerungsdimensionen anzeigen, die für wertmäßige Bestände aktiviert sind.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
