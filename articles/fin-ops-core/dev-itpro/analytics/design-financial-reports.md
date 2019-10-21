---
title: Finanzberichte entwerfen und verwalten
description: Dieser Artikel enthält Übungen, die Sie durch das Anzeigen und Erstellen von Finanzberichten für Microsoft Dynamics 365 Finance führen.
author: jcart1106
manager: AnnBe
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReportingSetup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 10814
ms.assetid: cd5f6483-c09b-4c2d-9336-d22eb6ab6e4f
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dc68289514dc3b201b423091c92fa128d3065707
ms.sourcegitcommit: 7bec89b33a56447072d01066af4da473b8092ca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/02/2019
ms.locfileid: "2536800"
---
# <a name="view-and-design-financial-reports"></a>Finanzberichte entwerfen und verwalten

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Übungen, die Sie durch das Anzeigen und Erstellen von Finanzberichten für Microsoft Dynamics 365 Finance führen. Die Finanzberichterstellung besteht aus einer Betrachtungserfahrung innerhalb der Anwendung und einem Ein-Klick-Berichts-Designer, mit dem Sie Finanzberichte erstellen und bearbeiten können.

## <a name="exercise-1-generate-and-explore-a-default-financial-report"></a>Übung 1: Generieren und untersuchen Sie einen Standardfinanzbericht

In dieser Übung generieren und untersuchen Sie einen vorhandenen Standardbericht. Dieser Bericht umfasst alle Konten und enthält auch Kontoeeigenschaften (Attribute) für die Konten. Sie werden Transaktionsdetails anzeigen, Dimensionsfilter anwenden und Währung im Bericht ändern. Zuerst aktualisieren wir die Anzeigereihenfolge der Dimensionen für die Finanzberichterstellung. Dadurch wird es Ihnen ermöglicht, auszuwählen, wie die Dimensionen nicht nur beim Entwerfen und Anzeigen von Finanzberichten angezeigt werden.

1. Wechseln Sie zu **Finanzdimensionskonfiguration für Integrationsanwendungen** unter **Dimensionen des Kontenplans** im Hauptbuch.
2. Verschieben Sie die Dimensionen in die folgende Reihenfolge:

    1. Hauptkonto
    2. Unternehmenseinheit
    3. Kostenstelle
    4. Abteilung

    > [!NOTE]
    > Die anderen Dimensionen können in der aktuellen Reihenfolge bleiben.

3. Speichern Sie die Dimensionskonfiguration. Danach generieren wir einen Bericht und untersuchen die Daten im Bericht.
4. Wechseln Sie zu **Finanzberichte** unter **Abfragen und Berichte** im Hauptbuch.
5. Wählen Sie die Zeile für den Bericht namens **Hauptbuchdetail - Standard** aus.
6. Wählen Sie **Bearbeiten** aus.

    > [!NOTE]
    > Sie werden aufgefordert, den Ein-Klick-Berichts-Designer herunterzuladen und sich anzumelden. Verwenden Sie die Anmeldeinformationen, um sich anzumelden. Melden Sie sich mit Ihren Anmeldeinformationen an.

7. Ändern Sie das Basisjahr auf 2012, und wählen Sie **Generieren** aus. Wenn ein Bericht im Berichts-Designer generiert wird, wird er in einer neuen Browserregisterkarte geöffnet. Sie können den Bericht in der neuen Browserregisterkarte oder in Ihrer ursprünglichen Browserregisterkarte anzeigen und den Bericht dort öffnen, indem Sie ihn aus der Liste  **Finanzberichte** auswählen.
8. Wählen Sie im geöffneten Bericht einen der Beträge zur Anzeige der Kontodetails für den Bericht aus.
9. Sobald die Kontodetails angezeigt werden, wählen Sie ein Konto mit Daten aus und rufen Sie die **Berichtbuchungs-Drillstufe** auf. Auf der Berichtsbuchungsstufe können Sie die Eigenschaften (Attribute) anzeigen, die im Entwurf dieses Berichts enthalten sind. Je nach Transaktion und Konto werden möglicherweise einige oder alle Attribute angezeigt.
10. Schließen Sie die Berichtbuchungsstufe.
11. Wählen Sie das gleiche oder ein anderes Konto aus, und **öffnen Sie Belegbuchungen**. Belegbuchungen werden nach Perioden-, Jahres- und Konto- + Dimensionskombination des ausgewählten Kontos gefiltert. Aus den Belegbuchungen können Sie auswählen, andere Informationen zur Transaktion zu untersuchen.
12. Schließen Sie die Belegbuchungen. Innerhalb eines Finanzberichts können Sie angeben, die Daten entweder für eine andere Periode und Jahr oder mit verschiedenen übernommenen Attributen und Dimensionen anzuzeigen. Dies erfolgt, indem **Berichtsoptionen** verwendet werden.
13. Wählen Sie **Berichtsoptionen** aus.
14. Wählen Sie **Dimensionsfilter hinzufügen** und **Unternehmenseinheit** aus.
15. Geben Sie "001" in das Feld ein, und wählen Sie **OK** aus. Der Bericht zeigt nun nur die Daten für die 001 Unternehmenseinheit an. Dies ist eine personalisierte Ansicht des Berichts und nicht für Andere verfügbar.
16. Schließen Sie den gefilterten Bericht. Finanzberichte können in jeder Währung angezeigt werden, die der Anwendung hinzugefügt wurden.
17. Wählen Sie **Währung** dann **EUR** aus. Der Berichts wird nun in Euro angezeigt. Alle Währungscodes oder Währungssymbole, die im Berichtsdesign enthalten sind, werden nun in der übernommenen Währung angezeigt. Wenn kein Währungssymbol für eine Währung definiert wird, wird das Währungssymbol nicht angezeigt.
18. Schließen Sie den Bericht **Hauptbuchdetail**.
19. Schließen Sie den **Berichts-Designer**.

## <a name="exercise-2-add-additional-account-properties-to-a-report-design"></a>Übung 2: Hinzufügen weiterer Kontoeeigenschaften zu einem Berichtsdesign
In dieser Übung ändern Sie einen vorhandenen Standardbericht. Sie werden Zeilendefinition aktualisieren, um alle Konten einzubeziehen und die Spaltendefinition aktualisieren, um Kontoattribute einzubeziehen. Sobald die Aktualisierungen abgeschlossen sind, generieren Sie den neu erstellten Bericht und untersuchen ihn. Wir beginnen mit der Finanzberichtsliste.

1. Wechseln Sie zu **Finanzberichte** unter "Abfragen und Berichte" im Hauptbuch.
2. Wählen Sie die Zeile für den Bericht namens **Zusammenfassende Zwischenbilanz - Standard Spaltentypen** aus.
3. Wählen Sie **Bearbeiten** aus. **Zusammenfassende Zwischenbilanz - Standard** wird im Berichts-Designer geöffnet.
4. Wählen Sie **Datei** anschließend **Speichern unter** aus, und nennen Sie den Bericht "Ausführliche Zwischenbilanz mit Attributen".

    > [!NOTE]
    > Wenn ein neuer Bericht im Berichts-Designer erstellt wird, wird die Finanzberichtsliste aktualisiert.

5. Wählen Sie aus der Berichtsdefinition heraus das Zeilendefinitionssymbol aus, um zu die **Zwischenbilanz - Standardzeilendefinition** zu öffnen.
6. Speichern Sie die Zeilendefinition als **Ausführliche Zwischenbilanz mit Attributen**.
7. Klicken Sie mit dem Cursor in Zeile 50, wählen Sie **Bearbeiten** anschließend **Zeilen aus Dimensionen einfügen** aus. Mit "Zeilen aus Dimensionen einfügen" können Sie die Dimensionen in Ihrer Zeilendefinition auswählen. In dieser Übung werden wir die Zeilendefinition mithilfe des Hauptkontos aufbauen.
8. Stellen Sie sicher, dass das **Hauptkonto** alle kaufmännischen Und-Zeichen enthält, und wählen Sie **OK** aus. Die Zeilendefinition enthält nun alle Hauptkonten für juristische USMF-Person.
9. Führen Sie einen Bildlauf nach unten zur Zeile 11110 durch, und löschen Sie Zeile 11110.
10. Wählen Sie in Zeile 11080 **--- (Unterstrichbeträge)** aus.
11. Geben Sie in Zeile 11140 die **Summe aller Konten** in Spalte B ein.
12. Wählen Sie in der Spalte C in der Dropdownliste **TOT** aus.
13. Geben Sie **50:11080** in Spalte D ein.
14. **Speichern** Sie die Zeilendefinition. Die Zeilendefinition enthält nun alle Konten und eine Gesamt-Zeile, um alle Konten zu addieren. Danach aktualisieren wir die Spaltendefinition, um zusätzliche Kontoattribute einzubeziehen.
15. Wählen Sie in der Berichtsdefinition **Ausführliche Zwischenbilanz mit Attributen** das Spaltendefinitionssymbol aus, um die Spaltendefinition **Zusammenfassende Zwischenbilanz - Standard** zu öffnen.
16. Speichern Sie die Spaltendefinition als **Ausführliche Zwischenbilanz mit Attributen**. Die Spaltendefinition enthält Finanzdatenspalten, eine Beschreibungsspalte und Berechnungsspalten. Wir werden der Spaltendefinition Attributspalten hinzufügen, um den Konten zusätzliche Details bereitzustellen.
17. Die folgenden Attribute werden der Spaltendefinition hinzugefügt:

    - Erfassungsnummer
    - Erfassungsbeschreibung
    - Buchungsdatum
    - Erstellt von
    - Zuletzt geändert von

18. Wählen Sie in Spalte I **ATTR** als Spaltentyp aus. Anschließend wählen Sie die **Erfassungsnummer** als die Attributkategorie aus.
19. Fügen Sie weiterhin Spalten für die übrigen Attribute hinzu.
20. Fügen Sie in der Zeile **Überschrift 2** Beschreibungen für jede der neuen Spalten hinzu, die hinzugefügt wurden.
21. Speichern Sie die Berichtsdefinition. Jetzt, da die Zeilendefinition und die Spaltendefinition aktualisiert wurden, müssen wir sie der Berichtsdefinition hinzufügen.
22. Wählen Sie in der Berichtsdefinition **Ausführliche Zwischenbilanz mit Attributen** für die Zeilen- und Spaltendefinition " Ausführliche Zwischenbilanz mit Attributen" aus.
23. Ändern Sie das Basisjahr zu **2012**.
24. **Speichern** Sie die Berichtsdefinition und **generieren** Sie. Sobald der Bericht fertig generiert wurde und geöffnet wird, können Sie in den Bericht untersuchen, wie Sie schon in der ersten Übung. Führen Sie auf verschiedenen Konten einen Drilldown durch, um zu sehen, wie die zusätzlichen Attribute angezeigt werden.
25. Schließen Sie den Bericht **Ausführliche Zwischenbilanz mit Attributen**.
26. Schließen Sie den **Berichts-Designer**.

## <a name="exercise-3-create-a-multidimensional-report-using-a-reporting-tree"></a>Übung 3: Einen mehrdimensionalen Bericht mithilfe einer Berichtsbaumstruktur erstellen
In dieser Übung ändern Sie einen vorhandenen Standardbericht. Sie werden eine Berichtsbaumstruktur erstellen und zu einer Berichtsdefinition hinzufügen, um eine Kostenstelle/Divisionseinkommensaufstellung zu erzeugen. «»Sobald die Aktualisierungen abgeschlossen sind, generieren Sie die Kostenstelle/Divisionseinkommensaufstellung und untersuchen den Bericht unter Verwendung der Berichtsbaumstruktur. Wir beginnen mit der Finanzberichtsliste.

1. Wechseln Sie zu **Finanzberichte** unter "Abfragen und Berichte" im Hauptbuch.
2. Wählen Sie die Zeile für den Bericht namens **Einkommensaufstellung - Standard** aus.
3. Wählen Sie **Bearbeiten** aus. **Einkommensaufstellung - Standard** wird im Berichts-Designer geöffnet.
4. Zeigen Sie im Menü **Datei** auf **Neu**, und klicken Sie dann auf **Berichtsbaumstruktur-Definition**.
5. Klicken Sie im Menü **Bearbeiten** auf **Berichtseinheiten aus Dimensionen einfügen**.
6. Deaktivieren Sie die Kontrollkästchen für alle Dimensionen außer **Kostenstelle**.
7. Klicken Sie auf das Feld **Ausgangsdimension** für die Kostenstellendimension, geben Sie **007** ein, und drücken Sie dann die TAB-Taste. Geben Sie im Feld **Zieldimension** **018** ein.
8. **Speichern** Sie die resultierende Struktur mit dem Namen **Kostenstellen nach Division.** Nachdem die Berichtsbaumstruktur erstellt wurde, ändern Sie die Berichtsbaumstruktur, um drei neue Rollupeinheiten einzubeziehen: Marketing, Arbeitsgänge und Einzelhandel.
9. Klicken Sie im Menü **Fenster** auf **Kostenstellen nach Division**. (Wenn die Berichtsbaumstruktur geschlossen wurde, wählen Sie sie in den Berichtsbaumstruktur-Definitionen im Navigationsbereich aus.)
10. Klicken Sie auf Einheit Nummer zwei **Messen**, und klicken Sie auf das Symbol **Berichtseinheit einfügen**.
11. Doppelklicken Sie auf die Entitätsspalte auf der leeren Zeile, und wählen Sie **USMF** aus.
12. Geben Sie in den Spalten B und C **Marketing** ein.
13. Klicken Sie auf Einheit Nummer fünf **Servicearbeitsgänge**, und führen Sie einen Rechtsklick aus. Wählen Sie **Berichtserstelluungseinheit einfügen** aus.
14. Wiederholen Sie Schritt 11.
15. Geben Sie in den Spalten B und C **Arbeitsgänge** ein.
16. Klicken Sie auf Einheit Nummer zwölf, **Ausgang**, und führen Sie einen Rechtsklick durch. Wählen Sie **Berichtseinheit einfügen** aus.
17. Wiederholen Sie Schritt 11.
18. Geben Sie in den Spalten B und C **Einzelhandel** ein. Beachten Sie, dass die Einheiten "Marketing", "Arbeitsgänge" und "Einzelhandel" auf der gleichen Ebene wie die aktuellen Rollupeinheiten angezeigt werden. Die neuen Einheiten werden danach sortiert. Berichtserstellungseinheiten werden durch die Rechtsklickoptionen, herauf- bzw. heraubstufen oder durch Drag & Drop organisiert.
19. Überprüfen Sie, dass Einheit drei **Messen**, aktiv ist und führen Sie einen Rechtsklick durch.
20. Wählen Sie **Berichtseinheit tieferstufen** aus. Beachten Sie, dass die Einheit nun als untergeordnete Einheit von **Marketing** anzeigt wird.
21. Klicken Sie auf Einheit vier, **Marketing-Kampagne**, und führen Sie einen Rechtsklick durch.
22. Wählen Sie **Berichtseinheit tieferstufen** aus.
23. Klicken Sie auf **Servicearbeitsgänge** in der grafischen Anzeige. Drücken und halten Sie die linke Maustaste, wenn Sie die Einheit zu **Arbeitsgänge** ziehen. Lassen Sie die linke Maus los, um die Einheit im Rollup "Arbeitsgänge" abzulegen. Wiederholen Sie diesen Vorgang für **Produktion, Qualitätskontrolle, Logistik, Beschaffung und Verwaltung**.
24. Machen Sie aus **Outlet**, **Super**, **Kaufhaus** und **Online** untergeordnete Elemente von **Einzelhandel**, indem Sie sie entweder tieferstufen oder per Drag & Drop verschieben.
25. Speichern Sie die sich ergebende Neuorganisation. Nachdem die Berichterstellungsstruktur erstellt und organisiert wurde, kann sie der Berichtsdefinition hinzugefügt werden.
26. Wählen im Menü **Fenster** die Option **Einkommensaufstellung - Standard** aus, um die Berichtsdefinition zu öffnen.
27. Klicken Sie auf den **Strukturtyp**-Dropdownpfeil, und wählen Sie **Berichtserstellungstruktur** aus.
28. Klicken Sie auf den Struktur-Dropdownpfeil, und wählen Sie **Kostenstellen nach Division** aus.
29. Ändern Sie das Basisjahr zu **2012**. **Speichern** Sie die Änderungen, und **Generieren** Sie den Bericht. Nachdem der Bericht fertig generiert und geöffnet wurde, können Sie den Bericht untersuchen.
30. Wählen Sie das Dropdownmenü **Berichtserstellungsstruktur** aus, um die Berichtseinheiten anzuzeigen. Sie können in einer Zeile des Berichts auch einen Drilldown ausführen, um alle Salden für alle Einheiten der Berichtserstellungsstruktur anzuzeigen.
31. Schließen Sie **Einkommensaufstellung - Standard**.
32. Schließen Sie den **Berichts-Designer**.

## <a name="exercise-4-create-a-consolidated-report-using-an-organization-hierarchy"></a>Übung 4: Einen konsolidierten Bericht mithilfe einer Organisationshierarchie erstellen
In dieser Übung ändern Sie einen vorhandenen Standardbericht. Sie werden eine Organisationshierarchie in der Berichtsdefinition hinzufügen, um eine konsolidierte Einkommensaufstellung und eine Bilanz zu erzeugen. Sobald die Aktualisierungen abgeschlossen sind, generieren Sie die konsolidierten Bericht und untersuchen den Bericht unter Verwendung der Berichtsbaumstruktur. Wir beginnen mit der Finanzberichtsliste.

1. Wechseln Sie zu **Finanzberichte** unter "Abfragen und Berichte" im Hauptbuch.
2. Wählen Sie die Zeile für den Bericht namens **Bilanz und Einkommensaufstellung parallel - Standard** aus.
3. Wählen Sie **Bearbeiten** aus. **Bilanz und Einkommensaufstellung parallel - Standard** wird im Bericht-Designer geöffnet.
4. Wählen Sie **Datei** &gt; **Speichern unter**  aus und benennen Sie den Bericht **Konsolidierte Bilanz und Einkommensaufstellung paralle**.
5. Ändern Sie das Basisjahr zu 2012.
6. Klicken Sie auf den Strukturtyp-Dropdownpfeil, und wählen Sie **Organisationshierarchien** aus.
7. Klicken Sie auf den Strukturtyp-Dropdownpfeil, und wählen Sie **Contoso Holdings** aus.
8. Speichern Sie die Änderungen und generieren Sie den Bericht. Wenn Sie dazu aufgefordert werden, wählen Sie alle Berichtseinheiten aus. Nachdem der Bericht fertig generiert und geöffnet wurde, können Sie den Bericht untersuchen.
9. Wählen Sie **Berichtsoptionen** aus.
10. Wählen Sie **Dimensionsfilter hinzufügen** und **Abteilung** aus.
11. Geben Sie **022** in das Feld ein, und wählen Sie **OK** aus.
12. Schließen Sie den gefilterten Bericht.
13. Wählen Sie das Dropdownmenü **Berichtserstellungsstruktur** aus, um die Berichtseinheiten anzuzeigen. Sie können in einer Zeile des Berichts auch einen Drilldown ausführen, um alle Salden für alle Einheiten der Berichtserstellungsstruktur anzuzeigen.
14. Schließen Sie **Konsolidierte Bilanz und Einkommensaufstellung parallel**.
15. Schließen Sie den **Berichts-Designer**.

## <a name="exercise-5-create-a-sidebyside-departmental-report"></a>Übung 5: Einen parallelen Abteilungsbericht erstellen
In dieser Übung erstellen Sie einen neuen Bericht. Der Bericht ist eine parallele Einkommensaufstellung der Abteilungen. Sie verwenden eine vorhandene Zeilendefinition, erstellen aber eine neue Berichtsdefinition und eine neue Spaltendefinition, die Dimensionsfilter verwenden. Wir beginnen mit der Finanzberichtsliste.

1. Wechseln Sie zu **Finanzberichte** unter "Abfragen und Berichte" im Hauptbuch.
2. Wählen Sie **Neu** aus. Der Berichts-Designer wird mit einer leeren offenen Berichtsdefinition geöffnet. Ihre erste Aufgabe ist das Erstellen der Spaltendefinition.
3. Erstellen Sie eine neue Spaltendefinition, indem Sie auf **Datei** anschließend auf **Neu** und dann auf **Spaltendefinition** klicken.
4. Wählen Sie in **Spalte A** **DESC** als Spaltentyp aus.
5. Wählen Sie in **Spalte B** **FD** als Spaltentyp aus.
6. Doppelklick Sie im Feld **Dimensionsfilter**.
7. Doppelklicken Sie im Fenster **Dimension** auf die Spalte **Abteilung**.
8. Klicken Sie im Bereich "Einzel" oder "Bereich" des Dialogfelds, auf die Schaltfläche mit **...**, damit das Feld **Von** eine Liste der Abteilungen anzeigt.
9. Wählen Sie Abteilung **022**, **Vertrieb und Marketing** aus, und klicken Sie dann auf **OK**.
10. Wiederholen Sie die Schritte 5 bis 8 für die Abteilungen 23-25.
11. Geben Sie auf der Zeile **Überschrift 2** für jede FD-Spalte die folgenden Abteilungsbeschreibungen ein:

    - Spalte B: Vertriebs- und Marketing
    - Spalte C: Arbeitsgänge
    - Spalte D: Finanzen
    - Spalte E – IT

12. Speichern Sie die Spaltendefinition als parallele Abteilungen. Da wir eine vorhandene Zeilendefinition verwenden, kann die Berichtsdefinition nun geändert werden, sodass die neu erstellte Spaltendefinition und die vorhandene Zeilendefinition verwendet werden.
13. Wählen im Menü **Fenster** die Option **Neue Berichtsdefinition** aus, um die Berichtsdefinition zu öffnen.
14. Wählen Sie **Einkommensaufstellung - Standard** als die Zeilendefinition und **Parallele Abteilungen** als die Spaltendefinition aus.
15. Speichern Sie die Berichtsdefinition als **Parallele Einkommensaufstellung der Abteilungen**.
16. Ändern Sie das Basisjahr zu **2012**.
17. Ändern Sie die Detailebene auf **Finanz, Konto und Transaktion**.
18. **Speichern** Sie Ihre Änderungen und **generieren** Sie. Nachdem der Bericht fertig generiert und geöffnet wurde, können Sie den Bericht untersuchen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen
[Finanzberichterstellung](../../../finance/general-ledger/financial-reporting-getting-started.md)

[Finanzberichte anzeigen](../../../finance/general-ledger/view-financial-reports.md)

[Dynamics Financial Reporting-Blog](http://blogs.msdn.com/b/dynamics_financial_reporting/)
