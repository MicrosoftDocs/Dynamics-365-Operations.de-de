---
title: Projektressourcen
description: "Dieses Thema enthält Informationen zu Projektbeschaffung."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: cmercado
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: c29c95fc6abd13e668c44d3ccf437bb0e879e46b
ms.lasthandoff: 03/31/2017


---

# <a name="project-resourcing"></a>Projektressourcen

Dieses Thema enthält Informationen zu Projektbeschaffung.

Eine für Herausforderung Projektmanager und Ressourcen-Manager für die Projektplanungsphase ist Ressourcenzuordnung, in der diese Ressource die korrekte bestimmen und reservieren müssen, um für die Arbeit an einem Projekt feststellen. In Microsoft Dynamics 365 für Arbeitsgänge, lassen Beschaffungsfunktionen Sie Rollen für Projekte definieren, die als vorübergehende Ressourcen, die für ein bestimmtes Engagement reserviert werden können oder Teil eines Engagements behandelt werden. Mit diesem Ressourcentyp können Projektmanager und Ressourcen-Manager die folgenden Aufgaben abschließen:

-   Definieren einer Rolle, die die erforderlichen Kompetenzen hat, um den Ressourcen zu entsprechen.
-   Verwendungsrollen, um einen Engagementzeitplans ersten zu definieren, der auf Cubes Ressourcen reserviert ist.
-   Vorkalkulieren von Kosten und bestimmen Sie ein erstes Budget auf Grundlage der zugewiesenen Rollen und Ressourcen eines Projekts.
-   Mithilfe Sie Rollen, um die Anzahl von Ressourcenreservierungen dar, die für jedes Engagement erforderlich sind.
-   Vorkalkulieren der Anzahl der Ressourcen, die für den gesamten Lebenszyklus eines Projekts erforderlich sind.
-   Entwerfen eines Projektstrukturplans (WBS) mit den ersten Ressourcenzuweisungen.

[] ."![Projektlebenszyklus/media/projectresourcing02-1024x812.jpg)]". /media/projectresourcing02.jpg) 

Während Projektplanung fortfährt, können geplante Ressourcen nach Personal gebesetzte Ressourcen ersetzt werden. Der Projektmanager kann auch wechseln Sie zurück und die während der Beschaffungsreservierungen aller Projektphasen aktualisieren.

## <a name="set-up-project-resources"></a>Einrichten von Projektressourcen
Sie müssen einen Kalender einrichten und diesen einem Mitarbeiter oder einer Arbeitskraft zuordnen. Der Kalender wird verwendet, um das Projekt und die Arbeitszeit der Ressourcen geplant werden kann, die für das Projekt reserviert werden. Während der Kalendereinstellung können Projektmanager einen Ressourcenausgleich als Teil der Ressourcenoptimierung ausführen. Basierend auf dem Kalenderzeitplan können Einschränkungen für Ressourcen platziert werden. Sie können einen Kalender auf der Seite ** ** Kalender einrichten. 

Wenn Sie eine Arbeitskraft als Projektressource einrichten, können Sie von Arbeitskräften auswählen, die im Unternehmen, für das Sie Ressourcen einrichten, oder Sie können Arbeitskräfte von anderen Unternehmen in Ihrer Organisation ausgewählt arbeiten. Diese sind Intergesellschaftsressourcen. Nachfolgend wird erläutert, wie eine Arbeitskraft als Projektressource im Unternehmen eingerichtet und wie eine Intergesellschaftsprojektressource eingerichtet.

### <a name="set-up-a-worker-as-a-project-resource"></a>Arbeitskräfte als Projektressourcen einrichten

1.  Auf der ** Arbeitskräfte ** Seite der ** Arbeitskräfte ** Liste, wählen Sie die Arbeitskraft, die Sie als Projektressource hinzufügen aus, und öffnen Sie dem Arbeitskraftdatensatz.
2.  Klicken Sie im Aktivitätsbereich ** Projekt ** &gt; ** auf Einstellungen ** &gt; ** Projekteinstellungen **.
3.  Wählen Sie einen Kalender aus, und schließen Sie die Seite.

Sie können außerdem standardmäßige Projekte für eine Ressource als Typ einer Vorabzuweisung angeben. Vorabzuweisungen können verwendet werden, wenn der Ressourcen-Manager oder der Projektmanager weiß, welche Projekte für die Ressource gelten oder im Voraus. Vorabzuweisungen können außerdem auf der Anforderung eines Projektträgers oder des Debitors basieren. Damit ein Projekt auf der Seite **Projekte zuweisen** vorab zugewiesen werden kann, wählen Sie auf der Registerkarte **Projekte** in der Liste **Verbleibende Projekte** das gewünschte Projekt aus.

### <a name="set-up-an-intercompany-resource"></a>Einrichten einer Intergesellschaftsressource

Wenn Sie eine Arbeitskraft als Intergesellschaftsressource einrichten, müssen Sie die Einstellungen im Ausleiheunternehmen und im borgenden Unternehmen ausführen. 

** Im Ausleiheunternehmen: **

1.  In Dynamics 365 für Arbeitsgänge, überprüfen Sie, dass das Ausleiheunternehmen aktiviert ist, und schließen Sie dann wie vorstehend, "können eine Arbeitskraft als Projektressource " ab.
2.  Wechseln ** Hauptbuch **&gt; ** Buchungseinstellungen **&gt; ** Verrechnung **. Click **New**.
3.  ** Im Feld Kennung der juristischen Person ** Feld das Ausleiheunternehmen aus. Füllen Sie die restlichen Felder entsprechend aus, und klicken Sie dann speichern ** **.
4.  ** Wechseln die Projektverwaltung und - verrechnung **&gt; ** Einstellungen **&gt; ** Preise ** &gt; ** interner Verrechnungspreis **. _ **entity_PLACEHOLDER **
5.  Wählen Sie im ** interner Verrechnungspreis ** Formular klicken Sie erneut ** ** ** und im Feld ausleihende juristische Person ** Feld auswählen, das entsprechende Unternehmen.
6.  Wenn Sie den borgenden Unternehmen die Ressource nur ausleihen möchten, die Sie am Anfang dieses Abschnitts, im Feld Ressource ** ** Feld erstellt haben, wählen Sie den Namen der Ressource aus, die Sie erstellt haben. Wenn alle Ressourcen im Unternehmen erstellen möchten, das dem borgenden Unternehmen verfügbar ist, lassen Sie das Feld leer. ** ** Ressource
7.  Wechseln ** Projektverwaltung und Buchhaltung **&gt; ** Einstellungen **&gt; ** Projektverwaltungs- und Buchhaltungsparameter ** und Intercompany ** ** auf der Registerkarte, legen als ** aktivieren Sie Intergesellschaftseinsatzplanung und Arbeitszeitnachweise ** Feld fest ** Ja **.

** Im borgenden Unternehmen: **

1.  Wechseln ** Projektverwaltung und Buchhaltung ** &gt; ** ** ** &gt; einer Ressourcenliste **.
2.  Im Suchenfilter geben Sie den Namen der Ressource ein, die Sie im vorherigen Verfahren erstellt haben, für das Ausleiheunternehmen überprüft, ob der Name in der Ressourcenliste für das borgende Unternehmen enthalten ist.

## <a name="manage-resource-competencies"></a>Verwalten von Ressourcenkompetenzen
Ressourcenkompetenzen sind ein wichtiger Bestandteil das Ressourcenmanagement. Kompetenzen können als Basis verwendet werden, um Ressourcen zu bestimmen, die die korrekte Kompetenzbilanz, Ausbildungen, Bescheinigungen und Projekterfahrungen haben. Sie sollten diese Informationen für jede Ressource einrichten und diese regelmäßig aktualisieren. Auf diese Weise können Sie Funktionen maximieren, wenn bestimmte Ressourcenkompetenzen während der Projektressourcen-Zuweisung abgeglichen werden. [![Beispiele von Fähigkeiten, Bescheinigungen und der Ausbildung, Projekterfahrung von] ". /media/projectresourcing06-1024x383.jpg)]". /media/projectresourcing06.jpg) 

Nachfolgend wird erläutert, wie einige der Kompetenzen für eine Ressource eingerichtet werden. 

Um Kompetenzen für eine Arbeitskraft einzurichten, können Sie entweder die Listenseite **Arbeitskräfte** in der Personalverwaltung oder die Listenseite **Ressourcen** im Projektverwaltungs- und Buchhaltungsmodul verwenden. Für die folgenden Prozeduren wird die ** Arbeitskräfte ** Listenseite in der Personalverwaltung verwendet.

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
1.  ** Auf Projektverwaltung und Buchhaltung ** &gt; ** Arbeitsbereiche ** &gt; ** Projektverwaltung **.
2.  Klicken Sie auf **Neues Projekt**, und geben Sie dann die folgenden Werte ein.
    -   ** Projekttyp ** - Aufwand
    -   ** Projektname ** - XYZ-Aktualisierungs-Phase 2
    -   ** ** Projektgruppe - TM \_RIF
    -   ** Projektvertragskennung ** - 00000002
3.  Klicken Sie auf **Projekt erstellen**.

### <a name="assign-a-resource-to-a-project"></a>Ressource zum Projekt zuweisen

1.  ** Auf Personalverwaltung ** &gt; ** Arbeitskräfte ** &gt; ** Arbeitskräfte **.
2.  Wählen Sie in der Liste **Arbeitskräfte** den Datensatz für die Arbeitskraft, für die Sie zuvor Kompetenzen eingerichtet haben aus, und öffnen Sie den Arbeitskraftdatensatz.
3.  Klicken Sie im Aktivitätsbereich auf der **Projekt**-Registerkarte auf die **Einrichten**-Gruppe und auf **Projekte zuweisen**.
4.  Klicken Sie auf der Seite **Projektzuweisungen für Ressourcenüberprüfung** auf die Registerkarte **Projekte**.
5.  In ** fügen Sie dem ausgewählten Projekt, Projekte hinzu ** Filter für das Projekt, XYZ-Aktualisierungs-Phase 2
6.  Wählen Sie im Bereich **Verbleibende Projekte** ein Projekt aus, und klicken Sie anschließend auf den Pfeil, um sie dem Bereich **Ausgewählte Projekte** hinzuzufügen.
7.  Schließen Sie die Seite.

Bei Bedarf können Sie auch Kategorien für eine Ressource zuweisen. Der Kategorietyp ist "Kosten" oder "Umsatzerlös". Dies wird durch Ihre Organisation bestimmt. Wenn keine zugeordneten Kategorien für die Ressource entstehen, sucht Dynamics 365 oben die Standardkategorie für Arbeitsgänge auf Stunden-Preisen nach Kosten und Umsatzerlöse.

### <a name="set-up-project-resource-and-role-characteristics"></a>Einrichten von Projektressourcen und Rollenmerkmalen

Ein Projektmanager kann die Projektressourcenfunktionen verwenden, um die Rollen erstellen, die für das Projekt erforderlich sind. Rollen können verwendet werden, wenn Ressourcen bestätigte wenn noch unbekannt sind, Ressourcen reservierend. Vorübergehendes reservierte können Rollen z Ressourcen erfolgt sein, damit die Projektplanungsphasen fortsetzen können. 

![[] (beispielsweise einer Rolle. /media/projectresourcing05.jpg)]". /media/projectresourcing05.jpg) 

**Szenario: **Contoso wurde für ein Aufwandsprojekt gebucht, das eine genehmigte Projektcharter hat. Der Juniorprojektmanager arbeitet noch am Umfang des Projekts. Ressourcen-Manager Der derzeit zugewiesene Ressourcen identifiziert, die reserviert werden, an der dem neuen Projekt zu arbeiten. Eine der Rollen, die der Projektträger, aufgrund der wichtigen Art des Projekts angefordert hat, der zugewiesen ist Projektmanager. Der Ressourcen-Manager muss die neue Ressource abgerufen sowie die Rolle im System definiert werden, falls der Juniorprojektmanager die Ressourceninformationen für die Projektplanung benötigt. 

Die nachfolgenden Schritte veranschaulichen, die Leiterin des Ressourcenmanagements die ältere "Projektmanager" einrichten und Ressourcenmerkmale ihr zugeordnet werden kann. Später kann die Rolle verwendet werden, um für verfügbare Ressourcen zu finden, die die erforderlichen Ressourcenkompetenzen aufweisen.

1.  ** Auf Projektverwaltung und Buchhaltung ** &gt; ** Einstellungen ** &gt; ** Ressourcen ** &gt; ** Einstellungsrollen **.
2.  Klicken Sie auf **Neu**, und geben Sie dann die folgenden Werte ein.
    -   ** Rolle Kennung ** - älterer Projektmanager
    -   ** Beschreibung ** - älterer Projektmanager
3.  Klicken Sie auf **Erstellen**.
4.  Wählen Sie die Rolle **Senior Project Manager** aus, und klicken Sie anschließend **Merkmale konfigurieren**.
5.  Wählen Sie im Feld **Merkmalstyp** die Option **Qualifikation**.
6.  Geben Sie im **Verfügbare Merkmale**-Feld die Qualifikation ein, die Sie suchen.
7.  Wählen Sie im Feld **Merkmalstyp** die Option **Bescheinigung** aus.
8.  Geben Sie im **Verfügbare Merkmale**-Feld die Bescheinigung ein, die Sie suchen.
9.  Klicken Sie auf **OK**, und schließen Sie die Seite.

### <a name="assign-a-project-resource-to-a-project"></a>Projektressource zum Projekt zuweisen

1.  ** Auf Projektverwaltung und Buchhaltung ** &gt; ** Common ** &gt; ** Projekte ** &gt; ** alle Projekte ** und öffnen Sie das XYZ-Aktualisierungs-Phase ** 2 ** Projekt.
2.  Klicken Sie auf der **Projektteam und Planung**-Registerkarte auf **Hinzufügen**.
3.  Wählen Sie im Feld **Rolle** **Teammitglied** aus.
4.  Klicken Sie auf **Aus Kalender buchen**.
5.  Klicken Sie auf der Seite **Ressourcenverfügbarkeit** auf **Einstellungen anzeigen**.
6.  Geben Sie auf der **Ansichtseinstellungen anpassen**-Seite die folgenden Werte ein:
    -   ** Format für Datumsbereichsansicht ** - Tag
    -   ** Beschreibung - Anzeigenverfügbarkeit ** Ja
    -   ** Anzeigenrestkapazität ** - Ja
7.  Wählen Sie in der Liste der Ressourcen eine Ressource aus.
8.  ** Auf uneingeschränkte Buch ** &gt; ** vollständige Kapazität **.
9.  Schließen Sie die Seite.

### <a name="assign-a-resource-to-a-default-role"></a>Zuweisen einer Ressource zu einer Standardrolle

Um Projekt oder Ressourcen-Managern zu unterstützen, können Sie weiter an Ressourcen von Detailinformationen die für ein Projekt reserviert werden können. Sie können eine standardmäßige Rolle zu einer vorhandenen Ressource oder zu einer neu abgerufenen Ressource zuordnen. Wenn Sie beispielsweise als Daniel eingestellt wurde, weist er Erfahrung und Fähigkeiten, um die der Business Analysten-Rolle ein. Ressourcen-Manager Der zugewiesene Rolle diese als Daniels Standardrolle zu. Daher ist Leiterin des Ressourcenmanagements Daniel einem Pool der Business Analysten hinzu, hinzufügen, die verfügbar sind, für Projekte zu arbeiten. 

Während der Ressourcen reservierung Projektmanager können die Rolle Ressourcen filtern, die verfügbar sind, für Projekte zu arbeiten. Sie können diese Informationen als als Kriterium verwenden, wenn sie Multikriterienentscheidungsanalysen für die Ressourcenerfüllung ausführen. Sie können andere Ressourcenmerkmale dem Filter für die Suche nach Ressourcen hinzufügen, die eine bestimmte Ausbildung, Qualifikationen und Erfahrungen für ein bestimmtes Projekt besitzen. 

** Szenario: ** Ein Projekt genehmigt wurde gestartet, und die ältere "Projektmanager" wurde als geplante Ressource für die Projektplanungsphase reserviert. Der Ressourcen-Manager hat nun eine Ressource abgerufen, um die Rolle Senio-Projektmanager zu erfüllen.

1.  ** Auf Projektverwaltung und Buchhaltung ** &gt; ** ** ** &gt; einer Ressourcenliste **.
2.  Wählen Sie in der Liste der **Ressourcen** eine **Daniel Goldschmidt** aus.
3.  ** Auf Projektressource ** ** &gt; Verwalten ** ** &gt; Ressourcenrolle **.
4.  Klicken Sie auf **Neu**, und geben Sie dann die folgenden Werte ein.
    -   ** Effektiv ** - (das aktuelle Datum)
    -   ** Ablauf ** - nie
    -   ** Rolle ** - älterer Projektmanager
5.  Klicken Sie auf **Speichern** und schließen Sie die Seite.
6.  Fügen Sie auf der **Kompetenzen**-Registerkarte die **ProjectMgmt**-Qualifikation und die **PMP**-Bescheinigung hinzu.

## <a name="set-up-role-based-pricing"></a>Einrichten der rollenbasierten Preisgestaltung
Alle Kosten, Verkaufs- und Verrechnungspreise können für Rollen eingerichtet werden.

1.  ** Auf Projektverwaltung und Buchhaltung ** &gt; ** Einstellungen ** &gt; ** Preise ** &gt; ** Verkaufspreis (Stunde) **.
2.  Click **New**.
3.  Geben Sie ein Gültigkeitsdatum ein.
4.  Wählen Sie in der Spalte **Rolle** eine Rolle aus.
5.  Geben Sie in der Spalte **Preisgestaltung** einen Preis für die ausgewählte Ressourcenrolle ein.

## <a name="form-a-project-team"></a>Formular Projektteam ein
Um die Rollen zu verwenden die zuvor in einem Projekt angelegt wurden, muss Projektmanager die Rollen mit dem Projekt zugeordnet. Mehrere Rollen können für ein Projekt, damit für Dynamics 365 Beschriftungen der Arbeitsgänge automatisch zugewiesen sind diese Rollen für die Reservierung, spätere Unklarheiten zu verhindern. Wenn beispielsweise der Projektmanager drei Software Engineers benötigt, drei Rollen, Software Engineer die Software Engineer 1, 2 Engineer Software und Software Engineer 3 haben, während die Beschriftungen automatisch generiert werden. Wenn zuvor Rollenmerkmal für die Rolle festgelegt wurden, werden sie als Filter für die Suche nach einer Ressource angewendet. Zusätzliche Merkmale können nach Bedarf hinzugefügt werden, um die Suche noch weiter zu verfeinern. 

Die Ansichtseinstellungen können ebenfalls angepasst werden, um eine bessere Ansicht der Ressourcenverfügbarkeit zu ermöglichen. Es gibt Optionen für eine stündliche, tägliche, wöchentliche, monatliche, quartalsweise und jährliche Verfügbarkeit. Es gibt auch eine Option, um verfügbarer und Restkapazitäten für Ressourcen anzuzeigen. Diese Option ist für Zeitverwaltung hilfreich, wenn Sie die verfügbare Zeit für Aktivitäten oder die Ressourcenverfügbarkeit bewerten. 

Der Projektmanager kann eine Rolle auf der Seite auswählen und dann, wenn es einen verfügbaren Mitteln gibt, die die Anforderung passt, wählt aus, um eine Ressource zu reservieren, um die Rolle ein. Beachten Sie, dass nicht die Ressourcen für die Planungsphase nun reserviert werden müssen. Wenn Sie einen PSP erstellen, können Sie Rollen nach Personal gebesetzte Ressourcen für das Projekt. Wenn Rollen nach Personal gebesetzte Ressourcen im PSP ersetzt wurden, aktualisiert der Ressource, die automatisch festgelegt wurde, die Projektteamlisten und Feinterminierung. 

[Projektteamlisten ![, die Rollen und tatsächliche]( Ressourcen einbezogen werden sollen . /media/projectresourcing03-1024x368.jpg)]". /media/projectresourcing03.jpg) 

Der Projektmanager hat verschiedene Optionen für die Buchung einer Ressource für ein Projekt wie **Restkapazität****Restkapazität** **Volle Kapazität** und **spezifische Stunden**. Diese Buchungsoptionen können jederzeit storniert werden, wenn sich Ressourcenzuweisung ändern. Es werden gibt zwei Typen von Buchungen unterstützt:

-   ** Hartes Buch ** – Die Ressourcenreservierung wurde genehmigt und bestätigt, um an dem Engagement für die bestimmten Zeitrahmens zu arbeiten.
-   ** Weiches Buch ** – Die Ressourcenreservierungen wurde vorbehaltliche festgelegt, an dem Engagement für die bestimmten Zeitrahmens zu arbeiten.

Das folgende Verfahren zeigt, wie ein Projektteam erstellt wird.

### <a name="create-a-project-team"></a>Projektteam erstellen

1.  Wählen Sie auf der Listenseite **Alle Projekte** ein Projekt aus, und klicken Sie anschließend auf **Bearbeiten**.
2.  Auf der Projektteam ** und Planung ** Registerkarte im Feld Zeitplanenddatum ** ** Feld, geben Sie das Zeitplanstartdatum plus einem Monat. Wenn beispielsweise das Zeitplanstartdatum am 24. Juni 2017 (24/06/2017), geben Sie ein 24/07/2017 ** **.
3.  Click **Add**.
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

**Synchronize resource capacity roll-ups**

Der Synchronisierungsprozess wurde entworfen, um alle Ressourcenkalenderinformationen zu synchronisieren. Dazu gehören Basiskalenderinformationen zu Änderungen an der Ressourcenkalenderkapazitätstabelle des Projekts. Wenn neue Ressourcen im Projekt hinzugefügt werden, muss Synchronisierungshilfen, dass die aktualisierten Kalenderinformationen verfügbar sind. Es Synchronisierung kann jederzeit durchgeführt werden. 

Es wird empfohlen, eine Stapelverarbeitung zu verwenden. Die Optionen sind nur verfügbar, wenn Sie Kapazitätsreservierungen synchronisieren.

-   ** Auf Projektverwaltung und Buchhaltung ** &gt; ** Periodisch ** &gt; ** Kapazitätssynchronisierung ** ** &gt; zum Synchronisieren der Ressourcenkapazität RolleUPS **.

| Mit der folgenden Option... | Beschreibung                                                                                                                                                                                          |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ja    | Synchronisieren Sie alle Ressourcendaten mit Kalender- und Basiskalenderinformationen, und ersetzen Sie alle Informationen im Ressourcen-Kapazitätskalender des Projekts.                                                  |
| Nein     | Synchronisieren Sie Ressourcendaten, basierend auf dem Datumsintervallcode und dem angegebenen Start- und Enddatum. Diese Option entfernt nicht vorhandene Daten und aktualisiert nur Informationen für neu hinzugefügte Ressourcen. |

[] (![Synchronisierung. /media/projectresourcing09.jpg)]". /media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Einrichten von Rollen für PSP-Vorlagen
Projektmanager können PSP-Vorlagen einrichten, die sie übernehmen können, wenn sie einen PSP für neue Projekte erstellen. Projektmanager können Rollen hinzugefügt werden, wenn er eine Vorlage erstellen. Gehen Sie folgendermaßen vor, um eine Rolle in einer PSP-Vorlage zuzuweisen. ** **

1.  ** Auf Projektverwaltung und Buchhaltung ** &gt; ** Einstellungen ** &gt; ** Projekte ** &gt; ** Projektstrukturplanvorlagen **.
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
<td>Fügen Sie automatisch geplante Ressourcen hinzu, indem Sie Rollen verwenden, die einer Aufgabe zugeordnet sind. Dynamics 365 für Arbeitsgänge geplanten Ressourcen schlägt automatisch vor, indem Sie Multikriterienentscheidungsanalyse verwendet, die anhand Rollen ist. Nachdem Rollen und Aufwand (Stunden) sind für die Aufgaben eines PSP einrichtet sind, und die Struktur freigegeben wurde, klicken Sie auf <strong>Team autom. generieren</strong>. Die erforderliche Anzahl der geplanten Ressourcen wird dem PSP und zur Registerkarte <strong>Projekt und Teamplanung</strong> hinzugefügt.</td>
</tr>
<tr class="odd">
<td>Ressource (Dropdownliste)</td>
<td>Auf der <strong>Startressourcenzuweisung </strong>-Seite können Sie Ressourcen verbindlich oder nicht verbindlich buchen (je nach angegebener Dauer). Sie können die Ansichtseinstellungen anpassen anpassen, um die Dauer von Ressourcenaktivitäten anzuzeigen und festzulegen. Sie können Ressourcen am Arbeitspaket auswählen und zuweisen, indem Sie die folgenden Optionen des Stücklistenartikels nutzen:
<ul>
<li><strong>Übernehmen</strong> - Bestätigen von Änderungen an der Ressource, die einer Aufgabe zugewiesen ist.</li>
<li><strong>Stornieren</strong> - Stornieren von Änderungen an der Ressource, die einer Aufgabe zugewiesen ist.</li>
<li><strong>Automatisch zuweisen</strong> – Diese Option wird gebesetzten Personal verfügbaren Ressourcen mit einer entsprechenden Rolle der ausgewählten Aufgabe aus.</li>
</ul></td>
</tr>
</tbody>
</table>

1.  ** Auf Projektverwaltung und Buchhaltung ** &gt; ** Projekte ** &gt; ** ** alle Projekte.
2.  Wählen Sie in der Liste das **XYZ-Upgrade-Phase 2**-Projekt aus.
3.  ** Plan auf ** &gt; ** Aktivitäten ** &gt; ** Projektstrukturplan **.
4.  Klicken Sie auf **Neu**, um die folgenden Ebenenaktivitäten dem PSP hinzuzufügen:
    -   Initiieren
    -   Planung
    -   Ausführung
    -   Überwachen und Steuern
    -   Schließen

5.  Hier können Sie die Datumsangaben und Aufwand (Stunden), wie im folgenden Screenshot) fest. [![die Daten und Aufwand festlegt] ". /media/projectresourcing10.jpg)]". /media/projectresourcing10.jpg)
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
16. Klicken Sie auf Weicher ** Ablehnen zu ** &gt; ** vollständige Kapazität **.
17. Klicken Sie auf **Speichern** und schließen Sie die Seite. 

> [!NOTE] 
> Sie wird keine Warnung angezeigt, dass die angegebene Ressource nun 2 ist, dass die Anzahl der Ressourcen an 1. muss.
18. Prüfen Sie auf der Seite **Projektstrukturplan ** Seite die Ressourcenzuweisung im PSP, und klicken Sie anschließend auf **Speichern**.

## <a name="resource-fulfillment-for-planned-resources"></a>Ressourcenerfüllung für geplante Ressourcen
Ein Projektmanager kann erforderliche Ressourcenrollen für ein Projekt planen. Der Ressourcen-Manager sieht diese geplanten Ressourcen als Anforderungen auf der **Ressourcenerfüllung**-Seite und kann die tatsächliche Ressourcen zuweisen.

1.  ** Auf Projektverwaltung und Buchhaltung ** &gt; ** Projekte ** &gt; ** ** alle Projekte.
2.  Wählen Sie in der Liste das **XYZ-Upgrade-Phase 2**-Projekt aus.
3.  Klicken Sie auf **Projekt**.
4.  Klicken Sie auf **Bearbeiten**.
5.  Auf der Projektteam ** und Planung ** Registerkarte ** ** auf ** Hinzufügen **.
6.  Wählen Sie im **Rollen hinzufügen**-Dialogfeld die **Softwareentwickler**-Rolle aus.
7.  Klicken Sie auf **Erstellen**.
8.  Schließen Sie die Proektseite.
9.  ** Auf Projektverwaltung und Buchhaltung ** &gt; ** ** ** &gt; einer Ressourcenerfüllung **.
10. Wählen Sie **Softwareentwickler 1** das Projekt **XYZ Upgrade project Phase 2** aus.
11. Wählen Sie eine Arbeitskraft aus, und klicken Sie dann auf **Zuweisen**.
12. Überprüfen Sie, ob die Position für **Softwareentwickler 1** für das Projekt **XYZ Upgrade project Phase 2** entfernt wurde.
13. Prüfen Sie auf der Registerkarte **Projektteam und Planung** für das **XYZ-Upgrade-Phase 2**-Projekt, ob die Arbeitskraft aus Schritt 11 als **Softwareentwickler** hinzugefügt wurde.

## <a name="requests-for-project-resources"></a>Einer Angebotsanforderung
Die Projekteinsatzplanungsfunktionen unterstützen nur Ressourcen-Manager, um gebesetzte Personal Ressourcen auf Engagement oder Projekten zu verteilen. Um diese Funktion zu aktivieren, führen Sie die folgenden Aufgaben aus, oder überprüfen Sie sie abgeschlossen wurden.

-   Hier können Sie Nummernkreise einrichten.
-   Einrichten von Projektverwaltungs- und Buchhaltungsworkflows.
-   Aktivieren Sie Ressourcenanforderungsworkflow.

Nachdem Sie entweder den Aufgaben wird überprüft oder abgeschlossen haben, können Sie die folgenden Aufgaben bei Bedarf ausführen.

-   Erstellen Sie eine Ressourcenanforderung von weich-gebuchten Personal gebesetzten Ressourcen.
-   Überwachen von Ressourcenanforderungen.
-   Erfüllen von Ressourcenanforderungen.
-   Dient zum Anfordern von Personal gebesetzten Ressourcen aus PSP.
-   Buchbetriebsmittel einem Projekt ohne eine Anforderung für Personal gebesetzten Ressourcen.

## <a name="monitor-project-teams"></a>Bildschirmprojektteams
1.  ** Auf Projektverwaltung und Buchhaltung ** &gt; ** Projekte ** &gt; ** ** alle Projekte.
2.  Klicken Sie in der Liste der Projekte auf den **Projektkennung**-Link für das **XYZ-Upgrade-Phase 2**-Projekt.
3.  Überprüfen Sie auf dem **Projektteam und Planung**-Inforegister, dass die Projektressourcen korrekt aufgelistet werden.



