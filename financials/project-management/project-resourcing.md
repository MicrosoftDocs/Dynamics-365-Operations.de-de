---
title: Projektressourcen
description: "Dieser Artikel enthält Informationen zu Projektressourcen."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: cmercado
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: a7275e9ad8d655d0d2ee5ba90a792775dec0cf05
ms.contentlocale: de-de
ms.lasthandoff: 06/13/2017


---

# <a name="project-resourcing"></a>Projektressourcen

[!include[banner](../includes/banner.md)]


Dieser Artikel enthält Informationen zu Projektressourcen.

Eine Herausforderung für Projektmanager und Ressourcen-Manager während der Projektplanungsphase ist die Ressourcenzuordnung bei der sie die richtige Ressource für die Arbeit an einem Projekt festlegen und reservieren müssen. In Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, können Sie mit Ressourcenfunktionalitäten für Projekte Rollen definieren, die als temporäre Ressourcen behandelt werden, die einem bestimmten Arbeitspaket oder Teil des Projekts reservieren werden können. Mit diesem Ressourcentyp können Projektmanager und Ressourcen-Manager die folgenden Aufgaben abschließen:

-   Definieren einer Rolle, die die erforderlichen Kompetenzen hat, um den Ressourcen zu entsprechen.
-   Verwenden von Rollen, um einen ersten Auftragsplan zu definieren, der auf den reservierten Ressourcen basiert.
-   Vorkalkulieren von Kosten und bestimmen Sie ein erstes Budget auf Grundlage der zugewiesenen Rollen und Ressourcen eines Projekts.
-   Verwenden von Rollen, um die Anzahl von Ressourcenreservierungen bewerten, die für jedes Auftrag erforderlich sind.
-   Vorkalkulieren der Anzahl der Ressourcen, die für den gesamten Lebenszyklus eines Projekts erforderlich sind.
-   Entwerfen eines Projektstrukturplans (WBS) mit den ersten Ressourcenzuweisungen.

[![Projektlebenszyklus](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg) 

Projektlebenszyklus im weiteren Verlauf der Projektplanung können durch geplante Ressourcen ersetzt werden. Der Projektmanager kann außerdem zurückgehen und die Ressourcenreservierungen während jeder Projektphase aktualisieren.

## <a name="set-up-project-resources"></a>Einrichten von Projektressourcen
Sie müssen einen Kalender einrichten und diesen einem Mitarbeiter oder einer Arbeitskraft zuordnen. Der Kalender wird verwendet, um das Projekt und die Arbeitszeit der Ressourcen planen, die dem Projekt reserviert werden. Während der Kalendereinstellung können Projektmanager einen Ressourcenausgleich als Teil der Ressourcenoptimierung ausführen. Basierend auf dem Kalenderzeitplan können Einschränkungen für Ressourcen platziert werden. Sie können einen Kalender auf der **Seite** Kalender einrichten. 

Wenn Sie eine Arbeitskraft als Projektressource einrichten, können Sie von Arbeitskräften auswählen, die im Unternehmen, für das Sie Ressourcen einrichten, oder Sie können Arbeitskräfte von anderen Unternehmen in Ihrer Organisation ausgewählt arbeiten. Diese sind Intercompany-Ressourcen. Nachfolgend wird erläutert, wie eine Arbeitskraft als Projektressource im Unternehmen eingerichtet und wie eine Intercompany-Ressourcen eingerichtet.

### <a name="set-up-a-worker-as-a-project-resource"></a>Arbeitskräfte als Projektressourcen einrichten

1.  Wählen Sie auf der Seite **Arbeitskräfte** in der Liste **Arbeitskräfte** die Arbeitskraft, die Sie als Projektressource hinzufügen und öffnen Sie den Arbeitskraftdatensatz.
2.  Klicken Sie im Aktivitätsbereich auf **Projekt** &gt; **Einstellungen** &gt; **Projekteinstellungen**.
3.  Wählen Sie einen Kalender aus, und schließen Sie die Seite.

Sie können außerdem standardmäßige Projekte für eine Ressource als Typ einer Vorabzuweisung angeben. Vorabzuweisungen können verwendet werden, wenn der Ressourcen-Manager oder der Projektmanager weiß, welche Projekte für die Ressource gelten oder im Voraus. Vorabzuweisungen können außerdem auf der Anforderung eines Projektträgers oder des Debitors basieren. Damit ein Projekt auf der Seite **Projekte zuweisen** vorab zugewiesen werden kann, wählen Sie auf der Registerkarte **Projekte** in der Liste **Verbleibende Projekte** das gewünschte Projekt aus.

### <a name="set-up-an-intercompany-resource"></a>Einrichten einer Intercompany-Ressource

Wenn Sie eine Arbeitskraft als Intercompany-Ressource einrichten, müssen Sie die Einstellungen im Ausleiheunternehmen und im leihenden Unternehmen ausführen. 

**Im Ausleiheunternehmen:**

1.  In Finance and Operations überprüfen Sie, dass das Ausleiheunternehmen aktiviert ist, und schließen Sie dann wie vorstehend die Aufgabe "Arbeitkraft als Projektressource einrichten" ab.
2.  Wechseln ** Hauptbuch **&gt; ** Buchungseinstellungen **&gt; **Intercompany-Verrechnung**. Klicken Sie auf **Neu**.
3.  Im Feld **Kennung der juristischen Person** wählen Sie das Ausleiheunternehmen aus. Füllen Sie die restlichen Felder entsprechend aus, und klicken Sie dann **Speichern**.
4.  Wechseln Sie zu **Projektverwaltung und -buchhaltung**&gt; **Einrichtung ** &gt; **Preise** ** &gt;  **Verrechnungspreis**. **
5.  Wählen Sie im **Interner Verrechnungspreis** Formular **Neu** aus und klicken Sie erneut im Feld **Ausleihende juristische Person** Feld auf das entsprechende Unternehmen.
6.  Wenn Sie den borgenden Unternehmen die Ressource nur ausleihen möchten, die Sie am Anfang dieses Abschnitts, im Feld **Ressource** erstellt haben, wählen Sie den Namen der Ressource aus, die Sie erstellt haben. Wenn alle Ressourcen im Unternehmen erstellen möchten, das dem borgenden Unternehmen verfügbar ist, lassen Sie das Feld **Ressource** leer.
7.  Wechseln Sie zu ** Projektverwaltung und Buchhaltung **&gt; ** Einstellungen **&gt; **Projektverwaltungs- und Buchhaltungsparameter** und auf der **Intercompany** Registerkarte legen Sie **Intercompany-Ressourcenplanung und -Arbeitszeitnachweise** Feld auf **Ja** fest.

**Im leihenden Unternehmen:**

1.  Wechseln Sie zu **Projektverwaltung und -buchhaltung** &gt; **Projektressourcen** &gt; **Ressourcenliste**.
2.  Im Suchenfilter geben Sie den Namen der Ressource ein, die Sie im vorherigen Verfahren erstellt haben, für das Ausleiheunternehmen überprüft, ob der Name in der Ressourcenliste für das borgende Unternehmen enthalten ist.

## <a name="manage-resource-competencies"></a>Verwalten von Ressourcenkompetenzen
Ressourcenkompetenzen ist ein wichtiger Bestandteil der Ressourcenverwaltung. Kompetenzen können als Basis verwendet werden, um Ressourcen zu bestimmen, die die korrekte Kompetenzbilanz, Ausbildungen, Bescheinigungen und Projekterfahrungen haben. Sie sollten diese Informationen für jede Ressource einrichten und diese regelmäßig aktualisieren. Auf diese Weise können Sie Funktionen maximieren, wenn bestimmte Ressourcenkompetenzen während der Projektressourcen-Zuweisung abgeglichen werden. [![Beispiele von Fähigkeiten, Zertifikaten, Ausbildung und Projekterfahrung](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg) 

Nachfolgend wird erläutert, wie einige der Kompetenzen für eine Ressource eingerichtet werden. 

Um Kompetenzen für eine Arbeitskraft einzurichten, können Sie entweder die Listenseite **Arbeitskräfte** in der Personalverwaltung oder die Listenseite **Ressourcen** im Projektverwaltungs- und Buchhaltungsmodul verwenden. Für die folgenden Verfahren verwenden wir die **Arbeitskräfte**-Listenseite in der Personalverwaltung.

### <a name="set-up-competencies-certificates"></a>Kompetenzen einrichten: Bescheinigungen

1.  Wählen Sie auf der **Arbeitskräfte**-Listenseite die Position der Arbeitskraft aus, für die Sie Bescheinigungsinformationen hinzufügen.
2.  Klicken Sie im Aktivitätsbereich auf der Registerkarte **Arbeitskräfte** in der Gruppe **Kompetenzen** auf **Bescheinigungen**.
3.  Klicken Sie auf **Neu**.
4.  Wählen Sie im Feld **Bescheinigungstyp** die Option **PMP** aus.
5.  Wählen Sie im Feld **Startdatum** das Datum **10.1.2015** aus.
6.  Klicken Sie auf **Speichern** und schließen Sie die Seite.

### <a name="set-up-competencies-skills"></a>Kompetenzen einrichten: Qualifikationen

1.  Stellen Sie auf der Listenseite **Arbeitskräfte** sicher, dass die Arbeitskraft, die Sie im vorherigen Verfahren verwendet haben, weiterhin ausgewählt ist. Klicken Sie dann im Aktivitätsbereich auf der Registerkarte **Arbeitskräfte** in der Gruppe **Kompetenzen** auf **Qualifikationen**.
2.  Klicken Sie auf **Neu**.
3.  Wählen Sie im Feld **Qualifikation** die Option **Projektmanagement**.
4.  Wählen Sie im Feld **Stufe** **5 Experte** aus.
5.  Wählen Sie im Feld **Stufendatum** das Datum **14.1.2015** aus.
6.  Geben Sie in **Jahren Erfahrung** **10** ein.
7.  Klicken Sie auf **Speichern** und schließen Sie die Seite.

## <a name="create-a-new-project"></a>Neues Projekt erstellen
1.  Klicken auf **Projektverwaltung und -buchhaltung** &gt; **Arbeitsbereiche** &gt; **Projektmanagement**.
2.  Klicken Sie auf **Neues Projekt**, und geben Sie dann die folgenden Werte ein.
    -   **Projekttype** - Nach Aufwand
    -   **Projektname** - XYZ Upgrade-Phase 2
    -   **Projektgruppe** - TM\_WIP
    -   **Projektvertragskennung** - 00000002
3.  Klicken Sie auf **Projekt erstellen**.

### <a name="assign-a-resource-to-a-project"></a>Ressource zum Projekt zuweisen

1.  Klicken Sie auf **Personalverwaltung** &gt; **Arbeitskräfte** &gt; **Arbeitskräfte**.
2.  Wählen Sie in der Liste **Arbeitskräfte** den Datensatz für die Arbeitskraft, für die Sie zuvor Kompetenzen eingerichtet haben aus, und öffnen Sie den Arbeitskraftdatensatz.
3.  Klicken Sie im Aktivitätsbereich auf der **Projekt**-Registerkarte auf die **Einrichten**-Gruppe und auf **Projekte zuweisen**.
4.  Klicken Sie auf der Seite **Projektzuweisungen für Ressourcenüberprüfung** auf die Registerkarte **Projekte**.
5.  **Fügen Sie das Projekt zu den ausgewählten Projekten hinzu**, und filtern Sie das Projekt XYZ-Upgrade Phase 2.
6.  Wählen Sie im Bereich **Verbleibende Projekte** ein Projekt aus, und klicken Sie anschließend auf den Pfeil, um sie dem Bereich **Ausgewählte Projekte** hinzuzufügen.
7.  Schließen Sie die Seite.

Bei Bedarf können Sie auch Kategorien für eine Ressource zuweisen. Der Kategorietyp ist "Kosten" oder "Umsatzerlös". Dies wird durch Ihre Organisation bestimmt. Wenn keine zugewiesenen Kategorien für die Ressource vorhanden sind, sucht Finance and Operations nach den Standardkategorie zu Stundenpreisen für die Kosten und den Umsatzerlös.

### <a name="set-up-project-resource-and-role-characteristics"></a>Einrichten von Projektressourcen und Rollenmerkmalen

Ein Projektmanager kann die Projektressourcenfunktionen verwenden, um die Rollen erstellen, die für das Projekt erforderlich sind. Rollen können verwendet werden, wenn bestätigte Ressourcen während der Ressourcenreservierungen noch unbekannt sind. Rollen können verwendet werden, um Ressourcen vorübergehend als geplante Ressourcen zu reservieren, um die Projektplanungsphasen fortsetzen zu können. 

[![Beispiel einer Rolle](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Szenario:** Contoso wurde für ein Aufwandsprojekt gebucht, das eine genehmigte Projektcharter hat. Der Juniorprojektmanager arbeitet noch am Umfang des Projekts. Der Ressourcen-Manager identifiziert derzeit zugewiesene Ressourcen, die reserviert für die Arbeit an dem neuen Projekt zugewiesen werden. Eine der Rollen, die der Projektträger aufgrund der Wichtigkeit des Projekts angefordert hat, ist ein Senior-Projektmanager. Der Ressourcen-Manager muss die neue Ressource abgerufen und beschließt, die Rolle im System zu definieren, falls der Juniorprojektmanager die Ressourceninformationen während der Projektplanung benötigt. 

Die folgenden Schritte zeigen, wie der Ressourcen-Manager den Senior-Projektmanager einrichten und Ressourcenmerkmale zuordnen kann. Später kann die Rolle verwendet werden, um für verfügbare Ressourcen zu finden, die die erforderlichen Ressourcenkompetenzen aufweisen.

1.  Klicken Sie auf **Projektverwaltung und -buchhaltung** &gt; **Einrichten** &gt; **Ressourcen** &gt; **Einstellungsrollen**.
2.  Klicken Sie auf **Neu**, und geben Sie dann die folgenden Werte ein.
    -   **Rollenkennung:** Senior Project Manager
    -   **Beschreibung:** Senior Project Manager
3.  Klicken Sie auf **Erstellen**.
4.  Wählen Sie die Rolle **Senior Project Manager** aus, und klicken Sie anschließend **Merkmale konfigurieren**.
5.  Wählen Sie im Feld **Merkmalstyp** die Option **Qualifikation**.
6.  Geben Sie im **Verfügbare Merkmale**-Feld die Qualifikation ein, die Sie suchen.
7.  Wählen Sie im Feld **Merkmalstyp** die Option **Bescheinigung** aus.
8.  Geben Sie im **Verfügbare Merkmale**-Feld die Bescheinigung ein, die Sie suchen.
9.  Klicken Sie auf **OK**, und schließen Sie die Seite.

### <a name="assign-a-project-resource-to-a-project"></a>Projektressource zum Projekt zuweisen

1.  Klicken Sie auf **Projektverwaltung und -buchhaltung** &gt; **Allgemein** &gt; **Projekte** &gt; **Alle Projekte** und öffnet Sie das Projekt **XYZ-Upgrade Phase 2**.
2.  Klicken Sie auf der **Projektteam und Planung**-Registerkarte auf **Hinzufügen**.
3.  Wählen Sie im Feld **Rolle** **Teammitglied** aus.
4.  Klicken Sie auf **Aus Kalender buchen**.
5.  Klicken Sie auf der Seite **Ressourcenverfügbarkeit** auf **Einstellungen anzeigen**.
6.  Geben Sie auf der **Ansichtseinstellungen anpassen**-Seite die folgenden Werte ein:
    -   **Format für Datumsbereichsansicht:** Tag
    -   **Verfügbarkeitsbeschreibungen anzeigen**: Ja
    -   **Verbleibende Kapazität anzeigen**: Ja
7.  Wählen Sie in der Liste der Ressourcen eine Ressource aus.
8.  Klicken Sie auf **Verbindlich buchen** &gt; **Vollständige Kapazität**.
9.  Schließen Sie die Seite.

### <a name="assign-a-resource-to-a-default-role"></a>Zuweisen einer Ressource zu einer Standardrolle

Um Projekt- und Ressourcen-Manager zu unterstützen, können Sie die zu einem Projekt reservierbare Ressourcen detaillierter darstellen. Sie können eine standardmäßige Rolle zu einer vorhandenen Ressource oder zu einer neu abgerufenen Ressource zuordnen. Wenn Sie beispielsweise als Daniel eingestellt wurde, weist er Erfahrung und Fähigkeiten, um die der Business Analysten-Rolle ein. Ressourcen-Manager Der zugewiesene Rolle diese als Daniels Standardrolle zu. Daher ist Leiterin des Ressourcenmanagements Daniel einem Pool der Business Analysten hinzu, hinzufügen, die verfügbar sind, für Projekte zu arbeiten. 

Während der Ressourcenreservierung können Projektmanager die Rollenressourcen filtern, die verfügbar sind, um an Projekten zu arbeiten. Sie können diese Informationen als als Kriterium verwenden, wenn sie Multikriterienentscheidungsanalysen für die Ressourcenerfüllung ausführen. Sie können andere Ressourcenmerkmale dem Filter für die Suche nach Ressourcen hinzufügen, die eine bestimmte Ausbildung, Qualifikationen und Erfahrungen für ein bestimmtes Projekt besitzen. 

**Szenario:** Ein genehmigtes Projekt wurde gestartet, und die Senior-Projektmanager wurde während der Projektplanungsphase als geplante Ressource reserviert. Der Ressourcen-Manager hat nun eine Ressource abgerufen, um die Rolle Senio-Projektmanager zu erfüllen.

1.  Klicken Sie auf **Projektverwaltung und -buchhaltung** &gt; **Projektressourcen** &gt; **Ressourcenliste**.
2.  Wählen Sie in der Liste der **Ressourcen** eine **Daniel Goldschmidt** aus.
3.  Klicken Sie auf **Projektressource** &gt; **Verwalten** &gt; **Ressourcenrolle**.
4.  Klicken Sie auf **Neu**, und geben Sie dann die folgenden Werte ein.
    -   **Gültigkeit:** (das aktuelle Datum)
    -   **Gültig bis:** Nie
    -   **Rolle:** Senior Project Manager
5.  Klicken Sie auf **Speichern** und schließen Sie die Seite.
6.  Fügen Sie auf der **Kompetenzen**-Registerkarte die **ProjectMgmt**-Qualifikation und die **PMP**-Bescheinigung hinzu.

## <a name="set-up-role-based-pricing"></a>Einrichten der rollenbasierten Preisgestaltung
Alle Kosten, Verkaufs- und Verrechnungspreise können für Rollen eingerichtet werden.

1.  Klicken Sie auf **Projektverwaltung und -buchhaltung** &gt; **Einrichten** &gt; **Preise** &gt; **Verkaufspreis (Stunde)**.
2.  Klicken Sie auf **Neu**.
3.  Geben Sie ein Gültigkeitsdatum ein.
4.  Wählen Sie in der Spalte **Rolle** eine Rolle aus.
5.  Geben Sie in der Spalte **Preisgestaltung** einen Preis für die ausgewählte Ressourcenrolle ein.

## <a name="form-a-project-team"></a>Ein Projektteam bilden
Um die Rollen zu verwenden, muss ein Projektmanager die Rollen dem Projekt zuordnen. Mehrere Rollen können für ein Projekt zugewiesen werden und Finance and Operations beschriftet diese Rollen automatisch während der Reservierung, um spätere Unklarheiten zu verhindern. Wenn beispielsweise der Projektmanager drei Softwareingenieure benötigt, werden automatisch drei Softwareingenieur-Rollen mit der Beschriftung "Software Engineer 1", "Software Engineer 2" und "Software Engineer 3" generiert. Wenn zuvor Rollenmerkmal für die Rolle festgelegt wurden, werden sie als Filter für die Suche nach einer Ressource angewendet. Zusätzliche Merkmale können nach Bedarf hinzugefügt werden, um die Suche noch weiter zu verfeinern. 

Die Ansichtseinstellungen können ebenfalls angepasst werden, um eine bessere Ansicht der Ressourcenverfügbarkeit zu ermöglichen. Es gibt Optionen für eine stündliche, tägliche, wöchentliche, monatliche, quartalsweise und jährliche Verfügbarkeit. Es gibt auch eine Option, um verfügbarer und Restkapazitäten für Ressourcen anzuzeigen. Diese Option ist für Zeitverwaltung hilfreich, wenn Sie die verfügbare Zeit für Aktivitäten oder die Ressourcenverfügbarkeit bewerten. 

Der Projektmanager kann eine Rolle auf der Seite auswählen. Wenn es eine verfügbares Ressourcen gibt, die zu den Anforderung passt, kann er die Ressource einer Rolle reservieren. Beachten Sie, dass die Ressourcen zu diesem Zeitpunkt der Planungsphase noch nicht in reserviert werden müssen. Wenn Sie einen PSP erstellen, können Sie Rollen durch geplanten Ressourcen für das Projekt ersetzen. Wenn die Rollen durch mit Personal versehene Ressourcen im PSP ersetzt werden, aktualisiert die Ressourceneinrichtung automatisch die Projektteamliste und den Zeitplan. 

[![Projektteamliste mit Rollen und aktuellen Ressourcen](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Der Projektmanager hat verschiedene Optionen für die Buchung einer Ressource für ein Projekt wie **Restkapazität****Restkapazität** **Volle Kapazität** und **spezifische Stunden**. Diese Buchungsoptionen können jederzeit storniert werden, wenn sich Ressourcenzuweisung ändern. Es werden gibt zwei Typen von Buchungen unterstützt:

-   **Verbindlich buchen** - Die Ressourcenreservierung wurde genehmigt und bestätigt, um an dem Auftrag in dem festgelegten Zeitraum zu arbeiten.
-   **Nicht verbindlich buchen** - Die Ressourcenreservierung wurde eingeplant, um an dem Auftrag in dem festgelegten Zeitraum zu arbeiten.

Das folgende Verfahren zeigt, wie ein Projektteam erstellt wird.

### <a name="create-a-project-team"></a>Projektteam erstellen

1.  Wählen Sie auf der Listenseite **Alle Projekte** ein Projekt aus, und klicken Sie anschließend auf **Bearbeiten**.
2.  Geben Sie auf der Registerkarte **Projektteam und Planung** im Feld **Enddatum planen** das Zeitplanstartdatum plus einen Monat ein. Wenn das Zeitplanstartdatum beispielsweise am 24. Juni 2017 ist, geben Sie **24.07.2017** ein.
3.  Klicken Sie auf **Hinzufügen**.
4.  Wählen Sie im Bereich **Rollen zum Projekt hinzufügen** im **Rolle**-Feld **Senior-Projektmanager** aus.
5.  Klicken Sie auf **Erforderliche Kompetenzen**.
6.  Auf der Seite **Merkmale auswählen** wählen Sie die Merkmale, dass Sie zuvor für die Senior-Projektmanager festgelegt haben. Klicken Sie auf **OK**.
7.  Auf der Seite **Rollen zum Projekt hinzufügen** geben Sie im Feld **Anzahl der Ressourcen** den Wert **1** ein.
8.  Im Feld **Ressource** zeigt die Suche alle Ressourcen an, die die erforderlichen Kompetenzen haben. Wählen Sie **Daniel Goldschmidt** aus, und klicken Sie dann auf **Erstellen**.
9.  Klicken Sie auf der Seite **Projekt** auf **Hinzufügen**.
10. Wählen Sie im Bereich **Rollen zum Projekt hinzufügen** im **Rolle**-Feld **Teammitglied** aus. Geben Sie **5** in das Feld **Anzahl der Ressourcen** ein.
11. Klicken Sie auf **Erstellen**.
12. Klicken Sie auf **Ressource auffüllen** auf der **Projekte**-Seite.

## <a name="resource-capacity-synchronization"></a>Ressourcenkapazitätssynchronisierung
Die Prozesse für die Ressourcensynchronisierung stellen sicher, dass die Kalender- und Basiskalenderinformationen zur Projekteinsatzplanung passen. Wenn der Kalender geändert wird, nehmen die Prozesse die erforderlichen Aktualisierungen der Planung von Projektbetriebsmitteln vor. Die Prozesse verbesser außerdem die Leistung, da die Ressourceninformationen des Kalenders im Voraus synchronisiert werden, damit Aktualisierungen der Einsatzplanungsinformationen schneller auftreten. Es wird empfohlen, die Prozesse als Stapelverarbeitung und nicht einzeln zu planen. Andernfalls besteht das Risiko, das jemand die inklusiven Datumsangaben bei der letzten Synchronisierung der Information vergisst. Wenn keine inklusiven Datumsangaben verwendet werden, können Lücken während der Datumssynchronisierung auftreten.

### <a name="calendar-synchronizationmediaprojectresourcing04-1024x471jpg"></a>![Kalendersynchronisierung](./media/projectresourcing04-1024x471.jpg)

**Ressourcenkapazitätszusammenfassungen synchronisieren**

Der Synchronisierungsprozess wurde entworfen, um alle Ressourcenkalenderinformationen zu synchronisieren. Dazu gehören Basiskalenderinformationen zu Änderungen an der Ressourcenkalenderkapazitätstabelle des Projekts. Wenn neue Ressourcen zum Projekt hinzugefügt werden, stellen die Synchronisierungshilfen sicher, dass die aktualisierten Kalenderdaten verfügbar sind. Es Synchronisierung kann jederzeit durchgeführt werden. 

Es wird empfohlen, eine Stapelverarbeitung zu verwenden. Die Optionen sind nur verfügbar, wenn Sie Kapazitätsreservierungen synchronisieren.

-   Klicken Sie auf **Projektverwaltung und -buchhaltung** &gt; **Periodisch** &gt; **Kapazitätssynchronisierung** &gt; **Ressourcenkapazitätszusammenfassungen synchronisieren**.

| Mit der folgenden Option... | Beschreibung                                                                                                                                                                                          |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ja    | Synchronisieren Sie alle Ressourcendaten mit Kalender- und Basiskalenderinformationen, und ersetzen Sie alle Informationen im Ressourcen-Kapazitätskalender des Projekts.                                                  |
| Nein     | Synchronisieren Sie Ressourcendaten, basierend auf dem Datumsintervallcode und dem angegebenen Start- und Enddatum. Diese Option entfernt nicht vorhandene Daten und aktualisiert nur Informationen für neu hinzugefügte Ressourcen. |

[![Synchronisierungsprozess](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Einrichten von Rollen für PSP-Vorlagen
Projektmanager können PSP-Vorlagen einrichten, die sie übernehmen können, wenn sie einen PSP für neue Projekte erstellen. Projektmanager können Rollen hinzufügen, wenn sie eine Vorlage erstellen. Gehen Sie folgendermaßen vor, um eine Rolle in einer PSP-Vorlage zuzuweisen.** **

1.  Klicken Sie auf **Projektverwaltung und -buchhaltung** &gt; **Einstellungen** &gt; **Projekte** &gt; **Vorlagen für Projektstrukturpläne.**
2.  Klicken Sie auf **Details** für eine ausgewählte PSP-Vorlage.
3.  Wählen Sie eine Aufgabe in der Liste, und dann im **Rolle**-Feld eine Rolle aus, die der Aufgabe zugewiesen werden soll.

### <a name="work-with-a-wbs"></a>Arbeiten mit einem PSP

Sie können einen neuen PSP erstellen, oder Sie können einen PSP aus einer vorhandenen PSP-Vorlage kopieren. Ein Projektmanager kann die Ressourcen problemlos verwaltet werden, indem er Rollen in die neuen Aufgaben im PSP zuweist. Rollen können ersetzt werden, nachdem eine Ressource abgerufen ist oder nachdem eine bestätigte Ressource für die Arbeit an der Aufgabe identifiziert wurde. Diese Flexibilität bietet Projektmanager die Möglichkeit die folgenden Aufgaben ausführen:

-   Ermitteln der Anzahl der Ressourcen, die für PSP-Arbeitsplanpakete erforderlich sind.
-   Vorkalkulation von Projektkosten.
-   Festlegen eines vorläufigen Budgets.
-   Vorkalkulation der Aktivitätsdauer auf Grundlage von Rollen und Ressourcen.
-   Entwickeln Sie mehrere Projektmanagementpläne auf Grundlage der verfügbaren Projektinformationen.

Es wurden zusätzliche Optionen im PSP zur besseren Verwendung der Ressourcenfunktionalität hinzugefügt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Mit der folgenden Option...</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ressourcenzuweisungen</td>
<td>Zeigen Sie die zugewiesenen Ressourcen, Datumsangaben, Anzahl Stunden und Buchungstypen für Aufgaben im PSP an.</td>
</tr>
<tr class="even">
<td>Team autom. generieren</td>
<td>Fügen Sie automatisch geplante Ressourcen hinzu, indem Sie Rollen verwenden, die einer Aufgabe zugeordnet sind. Finance and Operations schlägt automatisch geplante Ressourcen vor, indem es Multikriterienentscheidungsanalysen verwendet, die auf Rollen basieren. Nachdem Rollen und Aufwand (Stunden) sind für die Aufgaben eines PSP einrichtet sind, und die Struktur freigegeben wurde, klicken Sie auf <strong>Team autom. generieren</strong>. Die erforderliche Anzahl der geplanten Ressourcen wird dem PSP und zur Registerkarte <strong>Projekt und Teamplanung</strong> hinzugefügt.</td>
</tr>
<tr class="odd">
<td>Ressource (Dropdownliste)</td>
<td>Auf der <strong>Startressourcenzuweisung </strong>-Seite können Sie Ressourcen verbindlich oder nicht verbindlich buchen (je nach angegebener Dauer). Sie können die Ansichtseinstellungen anpassen anpassen, um die Dauer von Ressourcenaktivitäten anzuzeigen und festzulegen. Sie können Ressourcen am Arbeitspaket auswählen und zuweisen, indem Sie die folgenden Optionen des Stücklistenartikels nutzen:
<ul>
<li><strong>Übernehmen</strong> - Bestätigen von Änderungen an der Ressource, die einer Aufgabe zugewiesen ist.</li>
<li><strong>Stornieren</strong> - Stornieren von Änderungen an der Ressource, die einer Aufgabe zugewiesen ist.</li>
<li><strong>Automatisch zuweisen</strong> – Diese Option wählt Personal verfügbaren Ressourcen mit einer entsprechenden Rolle der ausgewählten Aufgabe aus.</li>
</ul></td>
</tr>
</tbody>
</table>

1.  Klicken Sie auf **Projektverwaltung und -buchhaltung** &gt; **Projekte** &gt; **Alle Projekte.**
2.  Wählen Sie in der Liste das **XYZ-Upgrade-Phase 2**-Projekt aus.
3.  Klicken Sie auf **Plan** &gt; **Aktivitäten** &gt; **Projektstrukturplan.**
4.  Klicken Sie auf **Neu**, um die folgenden Ebenenaktivitäten dem PSP hinzuzufügen:
    -   Initiieren
    -   Planung
    -   Ausführung
    -   Überwachen und Steuern
    -   Schließen

5.  Legen Sie die Datumsangaben und den Aufwand (Stunden) wie im folgenden Bild angezeigt. [![Einrichten der Datumsangaben und des Aufwands](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)
6.  Wählen Sie die **Initiieren**-Aufgabenposition, und wählen Sie dann im **Rolle**-Feld **Senior-Projektmanager**.
7.  Klicken Sie auf **Veröffentlichen**.
8.  Wählen Sie in der gleichen Position im **Ressource**-Feld **Daniel Goldschmidt** aus.
9.  Klicken Sie auf **Annehmen**.
10. Wählen Sie die **Planung**-Aufgabenposition, und wählen Sie dann im **Rolle**-Feld **Business Analyst**.
11. Klicken Sie auf **Veröffentlichen** und **Team autom. generieren**.
12. Klicken Sie im Bestätigungsdialogfeld auf **Ja**.
13. Prüfen Sie im **Ressource**-Feld, ob der Wert **Business Analyst 1** ist.
14. Für die **Business Analyst 1**-Ressource öffnen Sie die Suche und klicken Sie auf **Ressourcenzuweisungsformular starten**.
15. Wählen Sie eine Arbeitskraft für die Aufgabe.
16. Klicken Sie auf **Nicht verbindlich zuweisen** &gt; **Vollständige Kapazität.**
17. Klicken Sie auf **Speichern** und schließen Sie die Seite. 

> [!NOTE] 
> Es wird keine Warnung angezeigt, dass die angegebene Ressource jetzt 2 ist, da die Anzahl der Ressourcen bei 1 bleibt.
18. Prüfen Sie auf der Seite **Projektstrukturplan** Seite die Ressourcenzuweisung im PSP, und klicken Sie anschließend auf **Speichern**.

## <a name="resource-fulfillment-for-planned-resources"></a>Ressourcenerfüllung für geplante Ressourcen
Ein Projektmanager kann erforderliche Ressourcenrollen für ein Projekt planen. Der Ressourcen-Manager sieht diese geplanten Ressourcen als Anforderungen auf der **Ressourcenerfüllung**-Seite und kann die tatsächliche Ressourcen zuweisen.

1.  Klicken Sie auf **Projektverwaltung und -buchhaltung** &gt; **Projekte** &gt; **Alle Projekte.**
2.  Wählen Sie in der Liste das **XYZ-Upgrade-Phase 2**-Projekt aus.
3.  Klicken Sie auf **Projekt**.
4.  Klicken Sie auf **Bearbeiten**.
5.  Klicken Sie auf der **Projektteam und Planung**-Registerkarte auf **Hinzufügen**.
6.  Wählen Sie im **Rollen hinzufügen**-Dialogfeld die **Softwareentwickler**-Rolle aus.
7.  Klicken Sie auf **Erstellen**.
8.  Schließen Sie die Proektseite.
9.  Klicken Sie auf **Projektverwaltung und -buchhaltung** &gt; **Projektressourcen** &gt; **Ressourcenerfüllung.**
10. Wählen Sie **Softwareentwickler 1** das Projekt **XYZ Upgrade project Phase 2** aus.
11. Wählen Sie eine Arbeitskraft aus, und klicken Sie dann auf **Zuweisen**.
12. Überprüfen Sie, ob die Position für **Softwareentwickler 1** für das Projekt **XYZ Upgrade project Phase 2** entfernt wurde.
13. Prüfen Sie auf der Registerkarte **Projektteam und Planung** für das **XYZ-Upgrade-Phase 2**-Projekt, ob die Arbeitskraft aus Schritt 11 als **Softwareentwickler** hinzugefügt wurde.

## <a name="requests-for-project-resources"></a>Anforderungen für Projektressourcen
Die Projekteinsatzplanungsfunktionen unterstützen nur Ressourcen-Manager, um zur Verteilung Personal Ressourcen auf Engagement oder Projekten. Um diese Funktion zu aktivieren, führen Sie die folgenden Aufgaben aus, oder überprüfen Sie sie abgeschlossen wurden.

-   Hier können Sie Nummernkreise einrichten.
-   Einrichten von Projektverwaltungs- und Buchhaltungsworkflows
-   Ressourcenanforderungsworkflow aktivieren

Nachdem Sie entweder den Aufgaben wird überprüft oder abgeschlossen haben, können Sie die folgenden Aufgaben bei Bedarf ausführen.

-   Erstellen Sie eine Ressourcenanforderung von nicht fest gebuchten Personal Ressourcen.
-   Ressourcenanforderungen überwachen
-   Ressourcenanforderungen erfüllen
-   Anfordern von Personal Ressourcen aus PSP.
-   Resssourcen aus einem Projekt ohne eine Anforderung für Personal Ressourcen buchen

## <a name="monitor-project-teams"></a>Überwachung von Projektteams
1.  Klicken Sie auf **Projektverwaltung und -buchhaltung** &gt; **Projekte** &gt; **Alle Projekte.**
2.  Klicken Sie in der Liste der Projekte auf den **Projektkennung**-Link für das **XYZ-Upgrade-Phase 2**-Projekt.
3.  Überprüfen Sie auf dem **Projektteam und Planung**-Inforegister, dass die Projektressourcen korrekt aufgelistet werden.





