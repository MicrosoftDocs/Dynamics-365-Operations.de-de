---
title: Periodische Aufgaben in der wiederkehrenden Vertragsabrechnung
description: Dieses Thema beschreibt die periodischen Aufgaben, die in der wiederkehrenden Vertragsabrechnung verfügbar sind.
author: JodiChristiansen
ms.date: 04/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 80f65d82881bb000f626c4225b3eac7dd1a2a44a
ms.sourcegitcommit: 1877696fa05d66b6f51996412cf19e3a6b2e18c6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/20/2022
ms.locfileid: "8786969"
---
# <a name="periodic-tasks-in-recurring-contract-billing"></a>Periodische Aufgaben in der wiederkehrenden Vertragsabrechnung

Dieses Thema beschreibt die periodischen Aufgaben, die in der wiederkehrenden Vertragsabrechnung verfügbar sind.

## <a name="generate-invoice"></a>Rechnung generieren

Verwenden Sie die Seite **Rechnung erstellen**, um monatlich wiederkehrende Massenrechnungen aus den Informationen zu erstellen, die Sie auf den Seiten **Alle Abrechnungspläne** und **Ansicht Abrechnungsdetails** festgelegt haben. Wenn eine Rechnung erstellt wird, wird die Artikelbeschreibung für die Zeile der Verkaufsauftragsbearbeitung mit der Artikelbeschreibung und dem Start- und Enddatum der Rechnungsstellung für die Einteilung, die in Rechnung gestellt wird, aktualisiert.

## <a name="generate-invoice-batch-processing"></a>Batchverarbeitung für Rechnung generieren

Verwenden Sie die Seite **Rechnungen im Batch-Verfahren erstellen**, um wiederkehrende Rechnungen über einen wiederkehrenden Batch-Prozess zu erstellen. Die verfügbaren Parameter sind die gleichen wie die Parameter auf der Seite **Rechnung erstellen**, aber sie können in einem Batch-Prozess gespeichert werden, der mehrfach ausgeführt werden kann.

## <a name="price-update"></a>Preis aktualisieren

Verwenden Sie das Dienstprogramm Preisaktualisierung, um die Preise mehrerer Artikel auf mehreren Abrechnungsplänen in einer einzigen Aktion zu aktualisieren. Die Preise können entweder auf der Grundlage eines bestimmten Prozentsatzes oder eines bestimmten Betrags aktualisiert werden. Die Liste der Zeilen zeigt nur die aktuellen Einheitspreise der Artikel an. Es zeigt die Preise nach der Preisaktualisierung nicht an.

Beachten Sie die folgenden Punkte zum Dienstprogramm Preisaktualisierung:

- Wenn der Verkaufsauftrag für ein bestimmtes Jahr bereits erstellt wurde (d.h. die Artikel wurden bereits fakturiert), ist der Preis der Positionen davon nicht betroffen.
- Das Dienstprogramm Preisaktualisierung kann für Zeilen verwendet werden, die den Status **Aktiv** oder **Zurückgestellt** haben. Bei Artikeln, die sich in der Warteschleife befinden, muss die Option **Plan anpassen** auf **Nein** festgelegt worden sein, als die Warteschleife angelegt wurde.
- Das Dienstprogramm Preisaktualisierung kann nicht für Zeilen verwendet werden, die Nutzungspositionen sind, die Eskalation, Meilensteinabrechnung oder Umsatzsplitting verwenden.

### <a name="price-update-example"></a>Beispiel für Preisaktualisierung

Ein Abrechnungsplan wird erstellt und ein Artikel zur Verlängerung wird hinzugefügt. Der Preis pro Einheit beträgt $750. Das erste Jahr des Artikels wird am 15. Dezember 2021 bezahlt. Der Fakturierungsplan wird für den Zeitraum vom 1. Januar bis zum 31. Dezember 2022 erstellt.

Zum Zeitpunkt der Erneuerung erstellt der Prozess **Rechnung generieren** den Verkaufsauftrag für das Jahr 2022. Nachdem das Dienstprogramm Preisaktualisierung ausgeführt wurde, wird der Preis von $750 auf $800 aktualisiert.

Der Verkaufsauftrag und der Fakturierungsplan für 2022 sind davon nicht betroffen, und der Preis pro Einheit bleibt bei $750, da der Fakturierungsplan für 2022 bereits fakturiert wurde. Die Fakturierungseinteilung und das Zeilendetail für 2023 werden auf 800 $ aktualisiert, da die Fakturierungseinteilung für 2023 noch nicht fakturiert worden ist.

### <a name="update-prices--flat-pricing-method"></a>Preise aktualisieren - Pauschalpreismethode

Wenn Sie Preise für Artikel aktualisieren, die die Pauschalpreismethode verwenden, können Sie einen Prozentsatz oder einen Betrag angeben, um den Preis zu erhöhen.

Führen Sie diese Schritte aus, um das Dienstprogramm Preisaktualisierung für Artikel auszuführen, die die Pauschalpreismethode verwenden.

1. Wählen Sie auf der Seite **Preisaktualisierung** die Methode **Pauschalpreis**.
2. Wählen Sie im Feld **Erhöhungsmethode** die Erhöhungsmethode, mit der der Preis der Artikel aktualisiert werden soll.
3. Je nach der von Ihnen gewählten Erhöhungsmethode geben Sie den Prozentsatz im Feld **Prozent** oder den Betrag im Feld **Betrag** an.
4. Auf der Registerkarte **Einzubeziehende Datensätze** verwenden Sie die Schaltfläche **Filter**, um Datenfilter hinzuzufügen.
5. Wählen Sie **Vorschau anzeigen**, um den Bereich der Datensätze anzuzeigen.
6. Wenn Sie einige der Zeilen nicht verarbeiten möchten, markieren Sie diese und wählen Sie dann **Entfernen**.
7. Wählen Sie **OK** aus.

### <a name="update-prices--standard-pricing-method"></a>Preise aktualisieren - Standard-Preismethode

Wenn der Preis eines Artikels im Datensatz des Artikels geändert wurde, kann er für alle Fakturierungseinteilungen aktualisiert werden, wenn der Artikel die Standardpreismethode verwendet.

1. Wählen Sie auf der Seite **Preisaktualisierung** die Preismethode **Standard**.
2. Auf der Registerkarte **Einzubeziehende Datensätze** verwenden Sie die Schaltfläche **Filter**, um Datenfilter hinzuzufügen.
3. Wählen Sie **Vorschau anzeigen**, um den Bereich der Datensätze anzuzeigen.
4. Wenn Sie einige der Zeilen nicht verarbeiten möchten, markieren Sie diese und wählen Sie dann **Entfernen**.
5. Wählen Sie **OK** aus.

## <a name="mass-hold-processing"></a>Massensperrverarbeitung

Verwenden Sie die Seite **Massensperre**, um Sperroptionen auf mehrere Abrechnungspläne gleichzeitig anzuwenden.

Um nur einen Fakturierungsplan oder eine Fakturierungsplanzeile auf Halten zu setzen, öffnen Sie die Seite **Alle Fakturierungspläne** und wählen Sie **Halten setzen**. Um eine Sperrung aufzuheben, verwenden Sie die Seite **Sperrung aufheben**.

### <a name="put-billing-schedules-on-hold"></a>Rechnungspläne zurückstellen

Um mehrere Abrechnungspläne zu sperren, gehen Sie wie folgt vor.

1. Auf der Seite **Massenspeicher** legen Sie im Feld **Verarbeitungsoption** fest: **Speicherplatz zuweisen**.
2. Wählen Sie im Feld **Grundcode** einen Grundcode aus.
3. Legen Sie die Option **Zeitplan anpassen** fest:

    - **Ja** - Wenn Sie die Option auf **Ja** festlegen, geben Sie ein Haltedatum im Feld **Haltedatum** an. Alle Fakturierungseinteilungen nach dem Haltedatum werden entfernt.
    - **Nein** - Die Rechnungseinteilungen werden nicht geändert. Es wird nur der Status geändert. Sie wird auf **Auf Vorrat** aktualisiert.

4. Auf der Registerkarte **Einzubeziehende Datensätze** verwenden Sie die Schaltfläche **Filter**, um Datenfilter hinzuzufügen.
5. Wählen Sie **Vorschau anzeigen**, um den Bereich der Datensätze anzuzeigen.
6. Wenn Sie einige der Zeilen nicht verarbeiten möchten, markieren Sie diese und wählen Sie dann **Entfernen**.
7. Wählen Sie **OK** aus.

Wenn Sie zur Liste der Fakturierungspläne zurückkehren, sollten Sie sehen, dass der Status der Fakturierungspläne auf **In der Warteschleife** geändert worden ist.

### <a name="remove-a-hold-from-several-billing-schedules"></a>Halten Sie mehrere Abrechnungspläne zurück

1. Legen Sie auf der Seite **Massenhalten** das Feld **Verarbeitungsoption** auf **Halten entfernen** fest.
2. Geben Sie in das Feld **Grundcode** einen Grundcode ein.
3. Wählen Sie im Feld **Entfernungsdatum** das Datum aus, an dem der Sperrvermerk entfernt werden soll.
4. Legen Sie die Felder **Wiederaufnahmedatum** und **Abgrenzungsdatum** wie gewünscht fest. Das Datum der Abgrenzung wird zu allen Zeilen hinzugefügt, die aufgeschoben werden können.
5. Auf der Registerkarte **Einzubeziehende Datensätze** verwenden Sie die Schaltfläche **Filter**, um Datenfilter hinzuzufügen.
6. Wählen Sie **Vorschau anzeigen**, um den Bereich der Datensätze anzuzeigen.
7. Wenn Sie einige der Zeilen nicht verarbeiten möchten, markieren Sie diese und wählen Sie dann **Entfernen**.
8. Wählen Sie **OK** aus.

> [!NOTE]
> Um eine Sperrung zu entfernen, müssen Sie auf der Seite **Parameter für die Abrechnung wiederkehrender Verträge** den Wert **Benutzergruppenüberschreibung der Sperrung entfernen** festlegen.

Eine Rechnungszeile hat zum Beispiel ein Startdatum vom 1. Februar 2022 und ein Enddatum vom 28. Februar 2022. Der Rechnungsbetrag beträgt $200. Das Feld **Haltedatum** ist auf den 10. Februar 2022 festgelegt. Daher wird der Zeitraum im Februar angepasst, um jedes Datum nach dem 10. Februar auszuschließen. Der neue Zeitraum reicht vom 1. bis zum 9. Februar, und der Betrag beträgt 64,29 $ (durch tägliche Abgrenzung). Alle Rechnungseinteilungen am oder nach dem 10. Februar werden entfernt.

Wenn der Prozess **Haltestelle entfernen** abgeschlossen ist und das Feld **Entfernungsdatum** auf den 10. Februar 2022 festgelegt ist, gibt es zwei Abrechnungszeiträume. Der erste Abrechnungszeitraum ist vom 1. bis 9. Februar und der Betrag beträgt 64,29 $. Der zweite Abrechnungszeitraum ist vom 10. bis 28. Februar und der Betrag beträgt 135,71 $.

## <a name="mass-termination-processing"></a>Massenkündigungsverarbeitung

Verwenden Sie die Seite **Massenterminierung**, um aktuell angezeigte Rechnungseinteilungen zu beenden, indem Sie ein Beendigungsdatum angeben.

Wenn Sie die Abgrenzung von Umsatz und Ausgaben verwenden, können Sie auf der Seite **Alle Abrechnungspläne** Abrechnungspläne, bei denen das Feld **Abschlussdatum** auf **Zeitplan anpassen** festgelegt ist, eine Rückerstattung vornehmen.

Rechnungseinteilungen, die die MEA-Funktionalität (Multiple Element Allocation) verwenden, erscheinen nicht auf der Seite **Massenterminierung**. Sie können einen einzelnen Fakturierungsplan noch beenden, indem Sie die Beendigungsfunktion des Fakturierungsplans verwenden.

> [!NOTE]
> Rechnungseinteilungen, die derzeit in einem **Rechnung generieren** Batch enthalten sind, stehen für diesen Prozess nicht zur Verfügung.

Informationen zu den einzelnen Feldern und dem Prozess finden Sie unter [Abrechnungspläne beenden](terminate-billing-schedule.md).

## <a name="mass-archive-process"></a>Massenarchivierungsprozess

Verwenden Sie die Seite **Massenarchivierung**, um mehrere Abrechnungspläne zu archivieren. Es können nur beendete Fakturierungspläne archiviert werden.

Nachdem ein Fakturierungsplan archiviert wurde, treten die folgenden Ereignisse ein:

- Der Status wird auf **Archiviert** geändert.
- Die Fakturierungseinteilungen sind dauerhaft gesperrt.
- Die Zeilen des Fakturierungsplans sind auf den Abfrageseiten nicht mehr verfügbar.

> [!NOTE]
> Die Archivierung eines Fakturierungsplans ist eine permanente Aktion und kann nicht rückgängig gemacht werden.

Um Rechnungspläne zu archivieren, führen Sie die folgenden Schritte aus.

1. Geben Sie auf der Seite **Massenarchiv** im Feld **Rechnungsenddatum** ein Rechnungsenddatum an. Um alle beendeten Abrechnungszeitpläne anzuzeigen, lassen Sie dieses Feld leer.
2. Auf der Registerkarte **Einzuschließende Datensätze** des Inforegisters verwenden Sie die Schaltfläche **Filter**, um die angezeigten Datensätze einzuschränken.
3. Wählen Sie **Vorschau anzeigen**.
4. Wenn Sie einige Datensätze nicht archivieren möchten, markieren Sie diese und wählen Sie dann **Entfernen**.
5. Wählen Sie **OK**, um die Datensätze auf der Seite zu archivieren.

## <a name="mass-stubbing-process"></a>Masseninitialisierungsprozess

Verwenden Sie die Seite **Massenstub**, um alle ausgewählten Rechnungseinteilungen als fakturiert (Stub) oder nicht fakturiert (Reverse Stub) zu kennzeichnen. Stubs oder umgekehrte Stubs werden meist bei importierten Fakturierungseinteilungen durchgeführt, die zuvor in einem anderen System fakturiert wurden. Gestrichene Fakturierungseinteilungen erscheinen als gestrichen und erstellen keine Rechnung für den Debitor.

### <a name="stub-records"></a>Stub-Datensätze

1. Auf der Seite **Massenstub**, im Feld **Verarbeitungsoptionen**, wählen Sie **Stub**.
2. Legen Sie im Feld **Abschaltdatum** ein Abschaltdatum fest, um die Zeilen zu bestimmen, auf die Sie den Prozess anwenden möchten. Es werden nur Datensätze angezeigt, bei denen das Startdatum der Fakturierung am oder vor dem angegebenen Stichtag liegt.
3. Wählen Sie **Vorschau anzeigen**, um die Zeilen anzuzeigen, die Sie stubben möchten.
4. Um eine Zeile von der Verarbeitung auszuschließen, markieren Sie sie und wählen Sie dann **Entfernen**.
5. Wählen Sie **Verarbeiten**, um die Zeilen zu stubben.

### <a name="reverse-stub-records"></a>Stub-Datensätze stornieren

1. Wählen Sie auf der Seite **Massenstub** im Feld **Verarbeitungsoptionen** die Option **Stub umkehren**.
2. Legen Sie im Feld **Abschaltdatum** ein Abschaltdatum fest, um die Zeilen zu bestimmen, auf die Sie den Prozess anwenden möchten. Es werden nur Datensätze angezeigt, bei denen das Startdatum der Fakturierung am oder vor dem angegebenen Stichtag liegt.
3. Wählen Sie **Vorschau anzeigen**, um die Zeilen anzuzeigen, die Sie stornieren möchten.
4. Um eine Zeile von der Verarbeitung auszuschließen, markieren Sie sie und wählen Sie dann **Entfernen**.
5. Wählen Sie **Verarbeiten**, um die Zeilen zu stubben.

## <a name="update-completion-date-process"></a>Abschlussdatumsprozess aktualisieren

Verwenden Sie die Seite **Aktualisierung des Fertigstellungsdatums**, um das Fertigstellungsdatum für bestimmte Meilensteine für mehrere Abrechnungspläne oder Benutzer zu aktualisieren. Sie können auch den Fertigstellungsprozentsatz für Artikel auf Meilensteinvorlagen aktualisieren, die die Methode **Prozent abgeschlossen** verwenden.

1. Gehen Sie auf der Seite **Erledigungsdatum aktualisieren** zu **Meilensteine verarbeiten** und wählen Sie **Prozentuale Erledigung aktualisieren**.
2. Geben Sie in das Feld **Prozentsatz** den Gesamtprozentsatz ein, der abgeschlossen wurde.
3. Wählen Sie die Artikelnummer, die sich auf die Meilenstein-Vorlage bezieht.
4. Wählen Sie auf der Registerkarte **Einzubeziehende Datensätze** Inforegister die Option **Filter**, um einen bestimmten **Benutzerkonto**-, **Abrechnungsplannummer**- oder **Artikelnummern**-Wert als Filterkriterium auszuwählen.
5. Wählen Sie **OK**, um die Änderung zu verarbeiten. Wenn die Verarbeitung abgeschlossen ist, wird der Meilensteinzuordnung eine neue Zeile hinzugefügt. Diese Zeile stellt den Prozentsatz dar, der für die Meilenstein-Vorlage abgeschlossen wurde.

## <a name="unbilled-revenue-mass-processing"></a>Massenverarbeitung nicht abgerechneter Umsatzerlöse

Verwenden Sie die Seite **Massenverarbeitung von nicht fakturierten Umsätzen**, um den Journaleintrag für nicht fakturierte Umsätze zu erstellen oder den Journaleintrag für eine oder mehrere ausgewählte Buchungsblattzeilen oder Rechnungsdetails zu stubben.

- **Journaleintrag erstellen** - Erzeugt Journaleinträge für nicht fakturierte Umsätze für mehrere Buchungsblattzeilen. Verwenden Sie die Schaltfläche **Filter** auf dem Inforegister **Einzuschließende Datensätze**, um den Bereich der Datensätze auszuwählen, die in der Liste erscheinen. Die Liste zeigt nur Fakturierungseinteilungen, für die noch keine Journaleinträge für nicht fakturierte Umsätze erstellt wurden. Die ersten Journaleinträge werden erstellt. Für Abgrenzungsartikel werden auch die Abgrenzungspläne erstellt.
- **Stub Journaleintrag** - Markieren Sie die Fakturierungseinteilungen, für die bereits die nicht fakturierten Journaleinträge erstellt wurden. Diese Option wird verwendet, wenn die Erfassung des nicht fakturierten Journaleintrags bereits in einem anderen System gebucht wurde. Es kennzeichnet das Journal mit den nicht fakturierten Umsätzen als Stub und bucht keine Transaktion im Hauptbuch.
- **Stub-Journaleintrag stornieren** - Stornieren Sie bereits verarbeitete Stub-Journaleinträge. Wenn bei der Verarbeitung von **Journaleintrag stubben** ein Fehler unterlaufen ist, wird mit dieser Option das Kontrollkästchen **Stubben** für die Rechnungseinteilung deaktiviert.
- **Stub Rechnungsdetailzeile** - Verwenden Sie diesen Prozess, wenn nicht fakturierte Umsätze in einem externen System verarbeitet wurden und einige der Rechnungsdetailzeilen bereits fakturiert wurden. Dieser Prozess stellt sicher, dass der richtige Betrag auf den Konten für nicht fakturierte Umsätze erscheint.
- **Reverse Stub billing detail line** - Stornieren Sie alle **Stub billing detail line** Aktionen.

Das Feld **Journalname** wird verwendet, um **Journaleintrag erstellen** im Hauptbuch zu buchen.

> [!NOTE]
> Der Stub-Prozess bucht keine Beträge in das Allgemeine Hauptbuch. Das Feld **Journalname** ist nicht für alle Stub und Reverse Stub Prozesse verfügbar.

### <a name="unbilled-revenue-stub-example"></a>Beispiel für einen Stub für nicht fakturierte Umsätze

Ein Abrechnungsplan wird für ein Jahr festgelegt, von Oktober 2021 bis September 2022. Der nicht fakturierte Umsatz wurde bereits in einem externen System verarbeitet. Neun Monate des Abrechnungsplans sind bereits abgerechnet worden. Der Betrag für jeden Abrechnungszeitraum beträgt $250. Zu Beginn des Jahres beträgt der Gesamtbetrag, der in den nicht fakturierten Umsatz gebucht wurde, 3.000 $. Nach neun Monaten sind bereits $2.250 in Rechnung gestellt worden, und es verbleiben $750 an nicht fakturiertem Umsatz.

Um den Abrechnungsplan festzulegen, bei dem nur noch drei Monate an nicht abgerechneten Umsätzen verbleiben, gehen Sie wie folgt vor.

1. Erstellen Sie auf der Seite **Abrechnungsdetails anzeigen** einen Abrechnungsplan für den Zeitraum von Oktober 2021 bis September 2022, die Artikelnummer S0001 und einen Betrag von 250 $ pro Monat.
2. Wählen Sie **Journaleintrag erstellen** für den Rechnungsplan. Der Betrag von 3.000 $ wird auf den nicht fakturierten Umsatz gebucht.
3. Wählen Sie **Abrechnungsdetailzeile streichen** und geben Sie ein Transaktionsdatum von Juni 2022 (neun Monate) an. Die Fakturierungseinteilungen werden nicht in der Vorschau angezeigt. Welche Zeilen betroffen sind, hängt vom Datum der Transaktion ab.
4. Wählen Sie **OK** aus.

Die ersten neun Monate, die abgerechnet wurden, werden gestubbt.

[![Rechnungsdetails anzeigen Stub.](./media/01_View-billing-detail-stub.png)](./media/01_View-billing-detail-stub.png)

Die 3.000 $ werden aus den nicht fakturierten Umsätzen storniert, und die verbleibenden 750 $ an nicht fakturierten Umsätzen werden gebucht. Um die Buchungen der nicht fakturierten Umsätze anzuzeigen, wählen Sie **Prüfung des Journaleintrags für nicht fakturierte Umsätze** auf der Registerkarte **Erneuerungen** der Seite Zeilendetails.

[![Prüfung des Journaleintrags für nicht fakturierte Umsätze](./media/02_Unbilled-rev-journal-audit.png)](./media/02_Unbilled-rev-journal-audit.png)

> [!NOTE]
> Der Journaleintrag für nicht fakturierte Umsätze kann für jede Verlängerungsperiode erstellt werden, vorausgesetzt, dass alle Buchungsblattzeilen der vorherigen Periode fakturiert wurden. Zum Beispiel hat eine Rechnungseinteilung einen monatlichen Abrechnungsrhythmus für einen 12-monatigen Zeitraum, von Januar bis Dezember 2021. Die Zeile hat drei Laufzeiten: die erste Laufzeit, eine zweite Laufzeit (Januar bis Dezember 2022) und eine dritte Laufzeit (Januar bis Dezember 2023). Nachdem die Rechnung für alle Rechnungsdetailzeilen aus den ersten 12 Monaten im Jahr 2021 erstellt wurde, kann der Journaleintrag für nicht fakturierte Umsätze für die zweite Laufzeit erstellt werden.
>
> Bei Abgrenzungsartikeln, die die Funktion des nicht fakturierten Umsatzes verwenden, werden die Rechnungszeile und die Rabattzeilen verarbeitet. Für diese Artikel werden der Journaleintrag für nicht fakturierte Umsätze und der Abgrenzungsplan für die Buchungsblattzeile und die Skontolinie erstellt.
>
> Die Journaleinträge, die für nicht abgrenzbare Artikel und abgrenzbare Artikel erstellt werden, buchen eine Gutschrift auf verschiedene Umsatzkonten.
