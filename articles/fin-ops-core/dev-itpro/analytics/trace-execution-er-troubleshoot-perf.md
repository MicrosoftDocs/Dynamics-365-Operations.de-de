---
title: Überwachen der Ausführung von ER-Formaten zur Behebung von Leistungsproblemen
description: Dieses Thema bietet Informationen darüber, wie die Leistungsnachverfolgungsfunktion in der Elektronischen Berichterstellung (EB) verwendet werden kann, um Leistungsprobleme zu behandeln.
author: NickSelin
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 10eddf2f60db914e6451840d4d7aedb9dce7108874ea3ff45f375b85a55a694f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724392"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a>Ausführung von EB-Formaten nachverfolgen, um Leistungsprobleme zu behandeln

[!include[banner](../includes/banner.md)]

Im Rahmen des Prozesses, Elektronische Berichterstellungs-(EB)-Konfigurationen zu entwerfen, um elektronische Dokumente zu generieren, definieren Sie die Methode, mit der Daten aus der Anwendung abgerufen werden und in der Ausgabe, die generiert wird, eingegeben werden. Die EB-Leistungsablaufverfolgungfunktion hilft dabei, die Zeit und Kosten zu verringern, die durch das Sammeln der Details der EB-Formatausführung und bei deren Verwendung zur Behandlung von Leistungsproblemen. Dieses Tutorial bietet Richtlinien dazu, wie Leistungsnachverfolgungen für ausgeführte EB-Formate gewonnen werden und wie die Informationen aus diesen Nachverfolgungen zur Verbesserung der Leistung verwendet werden.

## <a name="prerequisites"></a>Voraussetzungen

Um die Beispiele in diesem Tutorial abzuschließen, müssen Sie den folgenden Zugriff haben:

- Zugriff auf eine der folgenden Rollen:

    - Entwickler für elektronische Berichterstellung
    - Funktionaler Berater für elektronische Berichterstellung
    - Systemadministrator

- Zugriff auf die Instanz des Regulatory Configuration Service (RCS), der für denselben Mandanten wie die Anwendung bereitgestellt wurde, für eine der folgenden Rollen:

    - Entwickler für elektronische Berichterstellung
    - Funktionaler Berater für elektronische Berichterstellung
    - Systemadministrator

Sie müssen auch die folgenden Dateien herunterladen und lokal speichern.

| Datei                                  | Inhalt                               |
|---------------------------------------|---------------------------------------|
| Leistungsnachverfolgung model.version.1     | [Beispiel-EB-Datenmodell-Konfiguration](https://download.microsoft.com/download/0/a/a/0aa84e48-8040-4c46-b542-e3bf15c9b2ad/Performancetracemodelversion.1.xml)    |
| Leistungsnachverfolgung metadata.version.1  | [Beispiel-EB-Metadatenkonfiguration](https://download.microsoft.com/download/a/9/3/a937e8c4-1f8a-43e4-83ee-7d599cf7d983/Performancetracemetadataversion.1.xml)      |
| Leistungsnachverfolgung mapping.version.1.1 | [Beispiel-EB-Modellzuordnungskonfiguration](https://download.microsoft.com/download/7/7/3/77379bdc-7b22-4cfc-9b64-a9147599f931/Performancetracemappingversion1.1.xml) |
| Leistungsnachverfolgung format.version.1.1  | [Beispiel-EB-Formatkonfiguration](https://download.microsoft.com/download/8/6/8/868ba581-5a06-459e-b173-fb00f038b37f/Performancetraceformatversion1.1.xml)       |

### <a name="configure-er-parameters"></a>Parameter der elektronischen Berichterstellung konfigurieren

Jede EB-Leistungsablaufverfolgung, die in der Anwendung generiert wird, wird als Anhang des Ausführungsprotokoll-Datensatzes gespeichert. Das Dokumentenverwaltungs-(DM)-Framework wird verwendet, um diese Anhänge zu verwalten. Sie müssen EB-Parameter im Voraus konfigurieren, um den DM-Dokumenttyp anzugeben, der verwendet werden soll, um Leistungsnachverfolgungen anzufügen. Klicken Sie im Arbeitsbereich **Elektronische Berichterstellung** auf den Link **Parameter der elektronischen Berichterstellung**. Wählen Sie anschließend auf der Seite **Elektronische Berichterstellungsparameter** unter der Registerkarte **Anhänge** im Feld **Andere** den DM-Dokumenttyp aus, der für Leistungsnachverfolgungen zu verwenden ist.

![Parameterseite der elektronischen Berichterstellung.](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

Um im Suchfeld **Andere** verfügbar zu sein, muss ein DM-Dokumenttyp in folgender Weise auf der Seite **Dokumenttypen** konfiguriert sein (**Organisationsverwaltung \> Dokumentenverwaltung \> Dokumenttypen**):

- **Klasse:** Datei anfügen
- **Gruppe:** Datei

![Seite „Dokumenttypen“.](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> Der ausgewählte Dokumenttyp muss in jedem Unternehmen der aktuellen Instanz verfügbar sein, da DM-Anhänge unternehmensspezifisch sind.

### <a name="configure-rcs-parameters"></a>RCS-Parameter konfigurieren

EB-Leistungsnachverfolgungen, die generiert werden, werden in RCS zur Analyse importiert, indem der EB-Format-Designer und der EB-Zuordnungs-Designer verwendet wird. Da EB-Leistungsnachverfolgungen als Anlagen des Ausführungsprotokoll-Datensatzes gespeichert werden, der dem EB-Format zugeordnet ist, müssen Sie RCS-Parameter im Voraus konfigurieren, um den DM-Dokumenttyp anzugeben, der verwendet werden soll, um Leistungsablaufverfolgungen anzufügen. In der Instanz von RCS, der für Ihr Unternehmen im Arbeitsbereich **Elektronische Berichterstellung** bereitgestellt wurde, wählen Sie **Elektronische Berichterstellungsparameter** aus. Wählen Sie anschließend auf der Seite **Elektronische Berichterstellungsparameter** unter der Registerkarte **Anhänge** im Feld **Andere** den DM-Dokumenttyp aus, der für Leistungsnachverfolgungen zu verwenden ist.

![Seite der elektronischen Berichterstellungsparameter in RCS.](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

Um im Suchfeld **Andere** verfügbar zu sein, muss ein DM-Dokumenttyp in folgender Weise auf der Seite **Dokumenttypen** konfiguriert sein (**Organisationsverwaltung \> Dokumentenverwaltung \> Dokumenttypen**):

- **Klasse:** Datei anfügen
- **Gruppe:** Datei

## <a name="design-an-er-solution"></a>Eine EB-Lösung entwerfen

Nehmen Sie an, Sie haben mit dem Entwurf einer neuen EB-Lösung begonnen, um einen neuen Bericht zu generieren, der Kreditorentransaktionen darstellt. Aktuell können Sie die Transaktionen für einen ausgewählten Kreditor auf der Seite **Kreditorenbuchungen** suchen (wechseln Sie zu **Kreditor \> Kreditoren \> Alle Kreditoren**, wählen Sie einen Kreditor aus, und dann, im Aktivitätsbereich unter der Registerkarte **Kreditor** in der Gruppe **Transaktionen** wählen Sie **Transaktionen**). Sie möchten jedoch alle Kreditorenbuchungen gleichzeitig in einem elektronischen Dokument im XML-Format haben. Diese Lösung besteht aus mehreren EB-Konfigurationen, die das erforderliche Datenmodell, die Metadaten, die Modellzuordnung und Formatkomponenten enthalten.

1. Melden Sie sich bei der Instanz von RCS an, die für Ihr Unternehmen bereitgestellt wurde.
2. In diesem Tutorial erstellen und modifizieren Sie Konfigurationen für das Beispielunternehmen **Litware, Inc.**. Stellen Sie daher sicher, dass dieser Konfigurationsanbieter RCS hinzugefügt wurde und als aktiv ausgewählt wurde. Anweisungen finden Sie unter der Prozedur [Konfigurationsanbieter erstellen und als aktiv markieren](tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Im Arbeitsbereich **Elektronische Berichterstellung** wählen Sie die Kachel **Berichterstellungskonfigurationen** aus.
4. Auf der Seite **Konfigurationen** importieren Sie die EB-Konfigurationen, die Sie als Voraussetzung nach RCS heruntergeladen haben, in der folgenden Reihenfolge: Datenmodell, Metadaten, Modellzuordnung, Format. Führen Sie für jede Konfiguration die folgenden Schritte aus:

    1. Wählen Sie im Aktivitätsbereich **Austausch \> Aus XML-Datei laden** aus.
    2. Wählen Sie **Durchsuchen** aus, um die entsprechende Datei für die erforderliche EB-Konfiguration im XML-Format auszuwählen.
    3. Wählen Sie **OK** aus.

    ![Konfigurationsseite in RCS.](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a>Ausführen der EB-Lösung, um Ausführung nachzuverfolgen

Gehen Sie davon aus, dass Sie das Entwerfen der ersten Version der EB-Lösung beendet haben. Jetzt möchten Sie sie in Ihrer Instanz testen und die Ausführungsleistung analysieren.

### <a name="import-an-er-configuration-from-rcs-into-finance-and-operations"></a><a id='import-configuration'></a>Importieren einer EB-Konfiguration aus RCS in Finance and Operations

1. Anmelden bei Ihrer Anwendungsinstanz.
2. Für dieses Tutorial importieren Sie Konfigurationen aus Ihrer RCS-Instanz (wo Sie Ihre EB-Komponenten entwerfen) in Ihre Instanz (wo Sie sie testen und schließlich benutzen). Daher müssen Sie sicherstellen, dass alle erforderlichen Artefakte vorbereitet wurden. Anweisungen finden Sie unter der Prozedur [Importieren von elektronischen Berichtstellungskonfigurationen (EB) aus Regulatory Configuration Services (RCS)](rcs-download-configurations.md).
3. Gehen Sie folgendermaßen vor, um die Konfigurationen von RCS in die Anwendung zu importieren:

    1. Im Arbeitsbereich **Elektronische Berichterstellung** in der Kachel für den Konfigurationsanbieter **Litware, Inc.** wählen Sie **Repositorys** aus.
    2. Wählen Sie auf de Seite **Konfigurationsrepository** das Repository des Typs **RCS** aus und wählen Sie dann **Öffnen** aus.
    3. Im Inforegister **Konfigurationen** wählen Sie die Konfiguration **Leistungsnachverfolgungsformat** aus.
    4. Wählen Sie im Inforegister **Versionen** die Version **1.1** der ausgewählten Konfiguration aus, und wählen Sie dann **Importieren** aus.

    ![Konfigurationsrepository-Seite.](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

Die entsprechenden Versionen der Datenmodell- und Modellzuordnungskonfigurationen werden automatisch als Voraussetzungen für die importierte EB-Formatkonfiguration importiert.

### <a name="turn-on-the-er-performance-trace"></a>Aktivieren der EB-Leistungsnachverfolgung

1. Wechseln Sie zu **Organisationsverwaltung \> Elektronische Berichterstellung \> Konfigurationen**.
2. Auf der Seite **Konfigurationen** im Aktivitätsbereich, auf der Registerkarte **Konfigurationen** in der Gruppe **Erweiterte Einstellungen** wählen Sie **Benutzerparameter** aus.
3. Im Dialogfeld **Benutzerparameter** im Abschnitt **Ausführungsnachverfolgung** führen Sie die folgenden Schritte aus:

    1. Geben Sie im Feld **Ausführungs-Trace-Format** das Format des generierten Performance-Trace an, in dem die Ausführungsdetails für ER-Format- und Zuordnungselemente gespeichert werden sollen:

        - **Debug-Trace-Format** – Wählen Sie diesen Wert, wenn Sie planen, ein ER-Format, das eine kurze Ausführungszeit hat, interaktiv auszuführen. Die Sammlung von Details zur ER-Format-Ausführung wird dann gestartet. Wenn dieser Wert ausgewählt ist, sammelt der Performance-Trace Informationen über die Zeit, die für die folgenden Aktionen aufgewendet wird:

            - Ausführen jeder Datenquelle in der Modellzuordnung, die aufgerufen wird, um Daten abzurufen
            - Verarbeitung jedes Formatelements, um Daten in der Ausgabe einzugeben, die generiert wird

            Wenn Sie den Wert **Debug-Trace-Format** wählen, können Sie den Inhalt des Trace im ER-Vorgangsdesigner analysieren. Dort können Sie sich die ER-Format- oder Zuordnungselemente ansehen, die im Trace erwähnt werden.

        - **Aggregiertes Trace-Format** – Wählen Sie diesen Wert, wenn Sie planen, ein ER-Format, das eine lange Ausführungszeit hat, im Batch-Modus auszuführen. Die Sammlung der aggregierten Details zur ER-Format-Ausführung wird dann gestartet. Wenn dieser Wert ausgewählt ist, sammelt der Performance-Trace Informationen über die Zeit, die für die folgenden Aktionen aufgewendet wird:

            - Ausführen jeder Datenquelle in der Modellzuordnung, die aufgerufen wird, um Daten abzurufen
            - Ausführen jeder Datenquelle in der Zuordnung des Formats, die aufgerufen wird, um Daten zu erhalten
            - Verarbeitung jedes Formatelements, um Daten in der Ausgabe einzugeben, die generiert wird

            Der Wert **Aggregiertes Trace-Format** ist in Microsoft Dynamics 365 Finance Version 10.0.20 und später verfügbar.

            Im ER-Formatdesigner und ER-Model-Zuordnungsdesigner können Sie die Gesamtausführungszeit für eine einzelne Komponente anzeigen. Zusätzlich enthält die Ablaufverfolgung Details über die Ausführung, wie z. B. die Anzahl der Ausführungen sowie die minimale und maximale Zeit einer einzelnen Ausführung.

            > [!NOTE]
            > Diese Ablaufverfolgung wird auf der Grundlage des Pfads der verfolgten Komponenten gesammelt. Daher kann die Statistik falsch sein, wenn eine einzelne übergeordnete Komponente mehrere unbenannte untergeordnete Komponenten enthält oder wenn mehrere untergeordnete Komponenten denselben Namen haben.

    2. Legen Sie die folgenden Optionen auf **Ja** fest, um bestimmte Details der Ausführung der EB-Modellzuordnung und EB-Formatkomponenten zu sammeln:

        - **Abfragestatistiken sammeln** – Wenn diese Option aktiviert ist, wird die Leistungsnachverfolgung die folgenden Informationen sammeln:

            - Die Anzahl von Datenbankaufrufen, die nach Datenquellen vorgenommen wurden
            - Anzahl der Doppeltaufrufe der Datenbank
            - Details der SQL-Anweisungen, die verwendet wurden, um Datenbankaufrufe vorzunehmen

        - **Zugriff der Zwischenspeicherung nachverfolgen** – Wenn diese Option aktiviert ist, sammelt die Leistungsnachverfolgung Informationen über die Cacheverwendung durch die EB-Modellzuordnung.
        - **Datenzugriff nachverfolgen** – Wenn diese Option aktiviert ist, sammelt die Leistungsnachverfolgung Informationen zur Anzahl der Aufrufe der Datenbank für ausgeführte Datenquellen des Datensatz-Listentyps.
        - **Listenenumeration nachverfolgen** – Wenn diese Option aktiviert ist, sammelt die Leistungsnachverfolgung Informationen zur Anzahl der Datensätze, die von Datenquellen des Datensatz-Listentyps angefordert werden.

    > [!NOTE]
    > Die Parameter im Dialogfeld **Benutzerparameter** sind für den Benutzer und das aktuelle Unternehmen spezifisch.

    ![Benutzerparameter-Dialogfeld.](./media/GER-PerfTrace-GER-UserParameters.png)

### <a name="run-the-er-format"></a><a id='run-format'></a>Das EB-Format ausführen

1. Wählen Sie das Unternehmen **DEMF** aus.
2. Wechseln Sie zu **Organisationsverwaltung \> Elektronische Berichterstellung \> Konfigurationen**.
3. Auf der Seite **Konfigurationen** in der Konfigurationsstruktur wählen Sie das Element **Leistungsnachverfolgungsformat** aus.
4. Wählen Sie im Aktivitätsbereich auf **Ausführen**.

Beachten Sie, dass die Datei, die generiert wird, Informationen über 265 Transaktionen für sechs Kreditoren präsentiert.

## <a name="review-the-execution-trace"></a>Überprüfen der Ausführungsnachverfolgung

### <a name="export-the-generated-trace-from-the-application"></a><a id='export-trace'></a>Exportieren Sie die generierte Ablaufverfolgung der Anwendung

Leistungsnachverfolgungen werden vom Quell-EB-Format entkoppelt und können in eine externe ZIP-Datei serialisiert werden.

1. Wechseln Sie zu **Organisationsverwaltung \> Elektronische Berichterstellung \> Konfigurations-Debug-Protokolle**.
2. Auf der Seite **Elektronische Berichterstellungs-Ausführungsprotokolle** im linken Bereich im Feld **Konfigurationsname** wählen Sie **Leistungsnachverfolgungsformat** aus, um die Protokolldatensätze zu suchen, die durch die Ausführung der Konfiguration **Leistungsnachverfolgungsformat** generiert wurden.
3. Wählen Sie die Schaltfläche **Anhänge** aus (das Büroklammersymbol) in der oberen rechten Ecke der Seite, oder drücken Sie **Strg+Umschalt+A**.

    ![Anhangschaltfläche auf der Seite für Elektronische Berichterstellungsausführungsprotokolle.](./media/GER-PerfTrace-GER-DebugLog.png)

4. Auf der Seite **Anhänge für elektronische Berichterstellungsausführungsprotokolle** im Aktivitätsbereich wählen Sie **Öffnen** aus, um die Leistungsnachverfolgung als ZIP-Datei abzurufen und sie lokal zu speichern.

    ![Anhänge für elektronische Berichterstellungsausführungsprotokolle.](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> Die Nachverfolgung, die generiert wird, hat eine Referenz auf den Quell-EB-Bericht über einen eindeutigen Berichtsbezeichner ausschließlich im **GUID**-Format. Die Versionsnummerierung des Formats wird nicht berücksichtigt.

Beachten Sie, dass die Zuordnung zwischen der Leistungsnachverfolgung, die für das ausgeführte EB-Format generiert wurde, und der EB-Modellzuordnung auf dem Stammdeskriptor basiert, der verwendet wurde, sowie dem allgemeinen Datenmodell. Die Versionsnummerierung des Formats und der Modellzuordnung wird nicht berücksichtigt. Die Einstellung der Markierung **Standard für Modellzuordnung** für die Modellzuordnung wird ebenfalls nicht berücksichtigt.

### <a name="import-the-generated-trace-into-rcs"></a><a id='import-trace'></a>Generierte Nachverfolgung nach RCS importieren

1. Im RCS, im Arbeitsbereich **Elektronische Berichterstellung** wählen Sie die Kachel **Berichterstellungskonfigurationen** aus.
2. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur das Element **Leistungsnachverfolgungsmodell**, und wählen Sie das Element **Leistungsnachverfolgungsformat** aus.
3. Wählen Sie im Aktivitätsbereich **Designer** aus.
4. Auf der Seite **Format-Designer** im Aktivitätsbereich wählen Sie **Leistungsnachverfolgung** aus.
5. Im Dialogfeld **Leistungsnachverfolgungs-Ergebniseinstellungen** wählen Sie **Leistungsnachverfolgung importieren** aus.
6. Wählen Sie **Durchsuchen**, um die ZIP-Datei auszuwählen, die Sie zuvor exportiert haben.
7. Wählen Sie **OK** aus.

    ![Leistungsnachverfolgungsergebnis-Einstellungen-Dialogfeld in RCS.](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a>Verwenden Sie die Leistungsnachverfolgung zur Analyse in RCS – Formatausführung

1. In RCS auf der Seite **Format-Designer** wählen Sie **Erweitern/Reduzieren** aus, um den Inhalt aller Formatelemente zu erweitern.

    Beachten Sie, dass zusätzliche Informationen für einige Artikel des aktuellen Formats angezeigt werden:

    - Tatsächlicher Zeitaufwand für die Eingabe von Daten in der generierten Ausgabe mithilfe des Formatelements
    - Die gleiche Zeit, ausgedrückt als Prozentsatz der gesamten Zeit, die für das Generieren der gesamten Ausgabe aufgewendet wurde

    ![Format-Designer-Seite in RCS.](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. Seite **Format-Designer** schließen.

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><a id='use-trace'></a>Verwenden Sie die Leistungsnachverfolgung zur Analyse in RCS – Modellzuordnung

1. In RCS, auf der Seite **Konfigurationen** in der Konfigurationsstruktur wählen Sie das Element **Leistungsnachverfolgungszuordnung** aus.
2. Wählen Sie im Aktivitätsbereich **Designer** aus.
3. Wählen Sie **Designer** aus.
4. Auf der Seite **Modellzuordnungsdesigner** im Aktivitätsbereich wählen Sie **Leistungsnachverfolgung** aus.
5. Wählen Sie die Nachverfolgung aus, die Sie zuvor importierten.
6. Wählen Sie **OK**.

Beachten Sie, dass neue Informationen für einige Datenquellelemente der aktuellen Modellzuordnung verfügbar werden:

- Tatsächlicher Zeitaufwand für das Abrufen von Daten mithilfe der Datenquelle
- Die gleiche Zeit, ausgedrückt als Prozentsatz der gesamten Zeit, die für das Ausführen der gesamten Modellzuordnung aufgewendet wurde

Beachten Sie, dass EB Sie informiert, dass die aktuelle Modellzuordnung Datenbankanforderungen dupliziert, während die Datenquelle VendTable/\<Relations/VendTrans.VendTable\_AccountNum ausgeführt wird. Diese Duplizierung findet statt, weil die Liste von Kreditorentransaktionen zweimal für jeden iterierten Kreditorendatensatz aufgerufen wird:

- Ein Aufruf wird vorgenommen, um Details jeder Transaktion in das Datenmodell einzugeben, basierend auf konfigurierten Bindungen.
- Ein Aufruf wird vorgenommen, um die berechnete Anzahl von Transaktionen pro Kreditor im Datenmodell einzugeben.

![Meldung zu doppelten Datenbankanforderungen auf der Seite Modellzuordnungsdesigner in RCS.](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

Der Wert **\[Q:530\]** gibt an, dass die Tabelle VendTrans 530 Mal aufgerufen wurde, um einen Datensatz von dieser Tabelle an die Datenquelle VendTable/\<Relations/VendTrans.VendTable\_AccountNum zurückzugeben. Der Wert **\[530\]** gibt an, dass die Datenquelle VendTable/\<Relations/VendTrans.VendTable\_AccountNum 530 Mal aufgerufen wurde, um einen Datensatz aus dieser Datenquelle zurückzugeben und die Details daraus in das Datenmodell einzugeben.

Es wird empfohlen, dass Sie das Zwischenspeichern für die Datenquelle VendTable/\<Relations/VendTrans.VendTable\_AccountNum verwenden, um die Anzahl von Aufrufen zu verringern, die vorgenommen werden, um die Details für 265 Transaktionen abzurufen und die Leistung der Modellzuordnung zu verbessern.

Es kann außerdem hilfreich sein, die Anzahl von Aufrufen zu reduzieren, die an die Datenquelle LedgerTransTypeList vorgenommen werden. Diese Datenquelle wird verwendet, um jeden Wert der Enumeration **LedgerTransType** seiner Beschriftung zuzuordnen. Indem Sie diese Datenquelle verwenden, können Sie eine entsprechende Beschriftung finden und sie in das Datenmodell für jede Kreditorentransaktion eingeben. Die aktuelle Anzahl von Aufrufen an diese Datenquelle (9.027) ist ziemlich hoch für 265 Buchungen.

![Modellzuordnungsdesigner-Seite in RCS, die 9.027 Aufrufe an die Datenquelle zeigt.](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a>Verbessern der Modellzuordnung auf der Grundlage von Informationen aus der Ausführungsnachverfolgung

### <a name="modify-the-logic-of-the-model-mapping"></a>Die Logik der Modellzuordnung ändern

1. Gehen Sie folgendermaßen vor, um Zwischenspeicherung zu verwenden, um doppelte Aufrufe an die Datenbank zu verhindern:

    1. In RCS auf der Seite **Modellzuordnungsdesigner** im Bereich **Datenquellen** wählen Sie das Element **VendTable** aus.
    2. Wählen Sie **Cache** aus.
    3. Erweitern Sie das Element **VendTable**, erweitern Sie die Liste der 1:n-Beziehungen für die Datenquelle VendTable (das Element **\<Relations**), und wählen Sie das Element **VendTrans.VendTable\_AccountNum** aus.
    4. Wählen Sie **Cache** aus.

    ![Zwischenspeicherungseinstellung, um doppelte Aufrufe zu verhindern.](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. Gehen Sie folgendermaßen vor, um die Datenquelle LedgerTransTypeList in den Bereich der Datenquelle VendTable zu bringen.

    1. Erweitern Sie im Bereich **Datenquellentypen** das Element **Funktionen**, und wählen Sie das Element **Berechnetes Feld** aus.
    2. Wählen Sie im Bereich **Datenquellen** das Element **VendTable** aus.
    3. Wählen Sie **Hinzufügen** aus.
    4. Geben Sie im Feld **Name** die Bezeichnung **\$TransType** ein.
    5. Wählen Sie **Formel bearbeiten** aus.
    6. Geben Sie im Feld **Formel** die Bezeichnung **LedgerTransTypeList** ein.
    7. Wählen Sie **Speichern**.
    8. Schließen Sie die Seite **Formel-Editor**.
    9. Klicken Sie auf **OK**.

3. Gehen Sie folgendermaßen vor, um die Zwischenspeicherung des Felds **\$TransType** auszuführen:

    1. Wählen Sie das Element **LedgerTransTypeList** aus.
    2. Wählen Sie **Cache** aus.
    3. Wählen Sie das Element **VendTable.\$TransType** aus.
    4. Wählen Sie **Cache** aus.

    ![Zwischenspeicherungseinstellung für das Feld $TransType.](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. Gehen Sie folgendermaßen vor, um das Feld **\$TransTypeRecord** zu ändern, sodass es damit beginnt, das zwischengespeicherte Feld **\$TransType** zu verwenden:

    1. Erweitern Sie im Bereich **Datenquellen** das Element **VendTable**, erweitern Sie das Element **\<Relations**, erweitern Sie das Element **VendTrans.VendTable\_AccountNum**, und wählen Sie das Element **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** aus.
    2. Wählen Sie **Bearbeiten** aus.
    3. Wählen Sie **Formel bearbeiten** aus.
    4. Suchen Sie im Feld **Formel** den folgenden Ausdruck:

        FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))

    5. Geben Sie im Feld **Formel** den folgenden Ausdruck ein:

        FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).

    6. Wählen Sie **Speichern**.
    7. Schließen Sie die Seite **Formel-Editor**.
    8. Wählen Sie **OK**.

5. Wählen Sie **Speichern**.
6. Schließen Sie die Seite **Modellzuordnungsdesigner**.
7. Schließen Sie die Seite **Modellzuordnungen**.

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a>Die geänderte Version der EB-Modellzuordnung abschließen

1. In RCS auf der Seite **Konfigurationen** im Inforegister **Versionen** wählen Sie die Version **1.2** der Konfiguration **Leistungsnachverfolgungszuordnung** aus.
2. Wählen Sie **Status ändern** aus.
3. Wählen Sie **Abgeschlossen** aus.

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-the-application"></a>Importieren der geänderten EB-Modellzuordnungskonfiguration von RCS in die Anwendung

Wiederholen Sie die Schritte im Abschnitt [Importieren einer EB-Konfiguration von RCS nach Finance and Operations](#import-configuration) weiter oben in diesem Thema, um Version 1.2 der Konfiguration **Leistungsnachverfolgungszuordnung** zu importieren.

## <a name="run-the-modified-er-solution-to-trace-execution"></a>Ausführen der geänderten EB-Lösung, um Ausführung nachzuverfolgen

### <a name="run-the-er-format"></a>Das EB-Format ausführen

Wiederholen Sie die Schritte im Abschnitt [Das EB-Format ausführen](#run-format) weiter oben in diesem Thema, um eine neue Leistungsnachverfolgung zu generieren.

## <a name="work-with-the-execution-trace"></a>Arbeiten Sie mit der Ausführungsnachverfolgung

### <a name="export-the-generated-trace-from-the-application"></a>Exportieren Sie die generierte Ablaufverfolgung der Anwendung

Wiederholen Sie die Schritte im Abschnitt [Die generierte Nachverfolgung aus der Anwendung exportieren](#export-trace) weiter oben in diesem Thema, um eine neue Leistungsnachverfolgung lokal zu speichern.

### <a name="import-the-generated-trace-into-rcs"></a>Generierte Nachverfolgung nach RCS importieren

Wiederholen Sie die Schritte im Abschnitt [Importieren der generierten Nachverfolgung nach RCS](#import-trace) weiter oben in diesem Thema, um die neue Leistungsnachverfolgung nach RCS zu importieren.

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a>Verwenden Sie die Leistungsnachverfolgung zur Analyse in RCS – Modellzuordnung

Wiederholen Sie die Schritte im Abschnitt [Verwenden der Leistungsnachverfolgung zur Analyse in RCS – Modellzuordnung](#use-trace) weiter oben in diesem Thema, um die aktuellste Leistungsnachverfolgung analysieren.

Beachten Sie, dass die Regulierungen, die Sie an der Modellzuordnung vorgenommen haben, doppelte Abfragen an eine Datenbank beseitigt haben. Die Anzahl der Aufrufe an Datenbanktabellen und Datenquellen für diese Modellzuordnung ist auch reduziert worden. Daher wurde die Leistung der gesamten EB-Lösung verbessert.

![Nachverfolgungsinformationen für die VendTable-Datenquelle auf der Seite Modellzuordnungsdesigner in RCS.](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

In den Nachverfolgungsinformationen gibt der Wert **\[12\]** für die Datenquelle VendTable an, dass diese Datenquelle 12 Mal aufgerufen wurde. Der Wert **\[Q:6\]** gibt an, dass sechs Aufrufe in Datenbankaufrufe an die Tabelle VendTable übersetzt wurden. Der Wert **\[C:6\]** gibt an, dass die Datensätze, die aus der Datenbank abgerufen wurden, zwischengespeichert wurden, und sechs weitere Aufrufe wurden mithilfe des Cache verarbeitet.

Beachten Sie, dass die Anzahl der Aufrufe an die LedgerTransTypeList-Datenquelle von 9.027 auf 240 verringert wurde.

![Nachverfolgungsinformationen für die LedgerTransTypeList-Datenquelle auf der Seite Modellzuordnungsdesigner in RCS.](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-the-application"></a>Wiederholen Sie die Ausführungsablaufverfolgung in der Anwendung

Neben RCS bieten manche Versionen möglicherweise Funktionen für die Funktionalität eines EB-Framework-Designers. Diese Versionen von haben eine Option **Entwurfsmodus aktivieren**, die aktiviert werden kann. Sie können diese Option unter der Registerkarte **Allgemein** der Seite **Elektronische Berichterstellungsparameter** finden, die Sie vom Arbeitsbereich **Elektronische Berichterstellung** aus öffnen können.

![Aktivieren Sie die Entwurfsmodusoption auf der elektronischen Berichterstellungsparameterseite.](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

Wenn Sie eine dieser Versionen verwenden, können Sie die Details von generierten Leistungsnachverfolgungen direkt in der Anwendung analysieren. Sie müssen sie nicht aus der Anwendung exportieren und nach RCS importieren.

## <a name="review-the-execution-trace-by-using-external-tools"></a>Überprüfung der Ausführungsnachverfolgung mithilfe externer Tools

### <a name="configure-user-parameters"></a>Benutzerparameter konfigurieren

1. Wechseln Sie zu **Organisationsverwaltung \> Elektronische Berichterstellung \> Konfigurationen**.
2. Auf der Seite **Konfigurationen** im Aktivitätsbereich, auf der Registerkarte **Konfigurationen** in der Gruppe **Erweiterte Einstellungen** wählen Sie **Benutzerparameter** aus.
3. Im Dialogfeld **Benutzerparameter** im Abschnitt **Ausführungsnachverfolgung** im Feld **Ausführungsnachverfolgungsformat** wählen Sie **PerfView XML** aus.

### <a name="run-the-er-format"></a>Das EB-Format ausführen

Wiederholen Sie die Schritte im Abschnitt [Das EB-Format ausführen](#run-format) weiter oben in diesem Thema, um eine neue Leistungsnachverfolgung zu generieren.

Beachten Sie, dass der Webbrowser eine ZIP-Datei zum Herunterladen anbietet. Diese Datei beinhaltet die Leistungsnachverfolgung im PerfView-Format. Sie können dann das PerfView-Leistungsanalysetool verwenden, um die Details der EB-Formatausführung zu analysieren.

![Informationen zur Leistungsnachverfolgung im PerfView-Format.](./media/GER-PerfTrace2-PerfViewTrace1.PNG)

## <a name="use-external-tools-to-review-an-execution-trace-that-includes-database-queries"></a>Nutzen Sie externe Tools, um eine Ausführungsablaufverfolgung zu prüfen, die Datenbankabfragen enthält

Aufgrund der Verbesserungen, die vorgenommen wurden, zeigt die Leistungsablaufverfolgung, die in PerfView-Format nun generiert wird, weitere Informationen zur ER-Formatausführung an. In Microsoft Dynamics 365 for Finance and Operations Version 10.0.4 (Juli 2019), kann diese Ablaufverfolgung Details der durchgeführten SQL-Abfragen der Anwendungsdatenbank enthalten.

### <a name="configure-user-parameters"></a>Benutzerparameter konfigurieren

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Auf der Seite **Konfigurationen** im Aktivitätsbereich, auf der Registerkarte **Konfigurationen** in der Gruppe **Erweiterte Einstellungen** wählen Sie **Benutzerparameter** aus.
3. Im Dialogfeld **Benutzerparameter** im Abschnitt **Ausführungsnachverfolgung** führen Sie die folgenden Parameter aus:

    - Wählen Sie im Feld **Ausführungsablaufverfolgungsformat** **PerfView XML** aus.
    - Legen Sie die Option **Sammeln Sie Abfragestatistik** auf **Ja** fest.
    - Legen Sie die Option **Abfrage nachverfolgen** auf **Ja** fest.

    ![Abschnitt zur Ablaufverfolgung der Ausführung, Benutzerparameter-Dialogfeld.](./media/GER-PerfTrace2-GER-UserParameters.PNG)

### <a name="run-the-er-format"></a>Das EB-Format ausführen

Wiederholen Sie die Schritte im Abschnitt [Das EB-Format ausführen](#run-format) weiter oben in diesem Thema, um eine neue Leistungsnachverfolgung zu generieren.

Beachten Sie, dass der Webbrowser eine ZIP-Datei zum Herunterladen anbietet. Diese Datei beinhaltet die Leistungsnachverfolgung im PerfView-Format. Sie können dann das PerfView-Leistungsanalysetool verwenden, um die Details der EB-Formatausführung zu analysieren. Diese Ablaufverfolgung umfasst jetzt die Details von SQL-Datenbankzugriff bei der Ausführung des ER-Formats.

![Verfolgt die Informationen für das ausgeführte ER-Format in PerfView nach.](./media/GER-PerfTrace2-PerfViewTrace2.PNG)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)
- [Verbessern Sie die Leistung von EB-Lösungen, indem Sie parametrisierte CALCULATED FIELD-Datenquellen hinzufügen](er-calculated-field-ds-performance.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
