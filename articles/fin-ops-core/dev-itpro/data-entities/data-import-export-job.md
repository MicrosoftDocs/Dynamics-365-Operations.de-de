---
title: Einzelvorgänge für Datenimport und ‑export – Übersicht
description: Verwenden Sie den Datenverwaltungsarbeitsbereich, um Datenimport- und Exporteinzelvorgänge zu erstellen und zu verwalten.
author: peakerbl
ms.date: 10/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.custom: intro-internal
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 51c7d678017bdd9388767500735e21e5374c9f29
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/23/2021
ms.locfileid: "7675368"
---
# <a name="data-import-and-export-jobs-overview"></a>Einzelvorgänge für Datenimport und ‑export – Übersicht

[!include [banner](../includes/banner.md)]

Um Datenimport- und Datenexporteinzelvorgänge zu erstellen und zu verwalten, verwenden Sie den Arbeitsbereich **Datenverwaltung**. Standardmäßig der Datenimport und der Exportvorgang eine für jede Stagingtabelle Entität in der Zieldatenbank erstellt. Mit Stagingtabellen können Sie Daten prüfen, bereinigen oder konvertieren, bevor Sie diese verschieben.

> [!NOTE]
> Für dieses Thema wird vorausgesetzt, dass Sie sich mit dem Thema [Datenentitäten](data-entities.md) vertraut gemacht haben.

## <a name="data-importexport-process"></a>Prozess für Datenimport und -export
Nachfolgend sind die Schritte dargestellt, um Daten zu importieren oder zu exportieren.

1. Erstellen eines Import- oder Exportvorgangs, wo Sie die folgenden Aufgaben durchführen können:

    - Projektkategorie definieren.
    - Geben Sie die Entitäten an, um Daten zu importieren oder exportieren.
    - Legen Sie das Datenformat für den Stapelverarbeitungsauftrag fest.
    - Entitäten nummerieren, damit sie in logischen Gruppen sowie in einen Auftrag verarbeitet werden, der logisch ist.
    - Hier legen Sie fest, ob Tabellen verwendet werden.

2. Überprüfen Sie, ob die Daten und die Zieldaten korrekt zugeordnet werden.
3. Überprüfen Sie die Sicherheit für den Export- oder Importvorgang.
4. Führt den Import- oder Exportvorgang aus.
5. Überprüfen Sie, ob der Einzelvorgang z erwartet ausgeführt wurde, da die Einzelvorgangshistorie hat.
6. Bereinigen der Tabellen.

Die verbleibenden Themen enthalten zusätzliche Details für jeden Schritt des Prozesses.

> [!NOTE]
> Um das Exportformular Datenimport/export zu aktualisieren um den aktuellen Status anzuzeigen, verwenden Sie das Formularaktualisierungssymbol. Die Aktualisierung des Browsers wird nicht empfohlen, da alle Import-/Exporteinzelvorgänge unterbrochen werden, die nicht in Stapelverarbeitung ausgeführt werden.

## <a name="create-an-import-or-export-job"></a>Erstellen eines Import- oder Exportvorgangs
Ein Datenimport- oder Exportvorgang kann einmal oder mehrmals ausgeführt werden.

### <a name="define-the-project-category"></a>Projektkategorie definieren
Es wird empfohlen, Zeit zu nehmen, um eine entsprechende Projektkategorie für den Import- oder Exportvorgang zu wählen. Projektkategorien können helfen, zugehörige Einzelvorgänge zu verwalten.

### <a name="identify-the-entities-to-import-or-export"></a>Geben Sie die Entitäten an, um Daten zu importieren oder zu exportieren.
Sie können bestimmte Entitäten einem Import- oder Exportvorgang hinzufügen oder eine Vorlage auswählen, die übernommen werden soll. Vorlagen füllen einen Einzelvorgang mit einer Liste von Entitäten aus. Die Option **Vorlage anwenden** ist verfügbar, wenn Sie dem Einzelvorgang einen Namen geben und den Einzelvorgang speichern.

### <a name="set-the-data-format-for-the-job"></a>Legen Sie das Datenformat für den Stapelverarbeitungsauftrag fest.
Wenn Sie eine Einheit auswählen, müssen Sie die Verpackungseinheiten das Format der Daten auswählen, die exportiert oder importiert werden. Sie legen Formate fest, indem Sie die Kachel **Datenquelleneinstellung** verwenden. Ein Quelldatenformat ist eine Kombination aus **Typ**, **Dateiformat**, **Zeilentrennzeichen** und **Spaltentrennzeichen**. Es gibt auch andere Attribute, aber diese sind die Wesentlichen, die man verstehen sollte. In der folgenden Tabelle werden die gültigen Kombinationen aufgeführt.

| Dateiformat            | Zeilen-/Spaltentrennzeichen                       | XML-Stil                 |
|------------------------|--------------------------------------------|---------------------------|
| Excel                  | Excel                                      | \-k. A.-                     |
| XML                    | \-k. A.-                                      | XML-Element XML-Attribut |
| Mit Trennzeichen, fest mit | Komma, Semikolon, Registerkarte, senkrechter Strich, Doppelpunkt | \-k. A.-                     |

> [!NOTE]
> Es ist wichtig, den richtigen Wert für **Zeilentrennzeichen**, **Spaltentrennzeichen** und **Textqualifizierer** auszuwählen, wenn die **Datei Format**-Option auf **Getrennt** eingestellt ist. Stellen Sie sicher, dass Ihre Daten nicht das als Trennzeichen oder Qualifizierer verwendete Zeichen enthalten, da dies beim Import und Export zu Fehlern führen kann.

### <a name="sequence-the-entities"></a>Sequenz der Entitäten
Entitäten können in einer Datenvorlage in den Serverkonfigurationsdateien oder im Import- und Exporteinzelvorgang sequenziert werden. Wenn Sie einen Einzelvorgang ausführen, der mehr als eine Datenentität enthält, müssen Sie prüfen, ob die Datenentitäten ordnungsgemäß geordnet werden. Sie ordnen die Entitäten hauptsächlich so, dass Sie beliebige funktionalen Abhängigkeiten unter den Entitäten adressieren können. Wenn Entitäten keine funktionalen Abhängigkeiten haben, können Sie diese für Parallelimport oder Export planen.

#### <a name="execution-units-levels-and-sequences"></a>Ausführungseinheiten, Ebenen und Nummernkreise
Die Ausführungseinheit, die Ebene in der Ausführungseinheit und die Sequenz der Entität helfen, die Reihenfolge der Daten zu steuern, die importiert oder exportiert werden.

- Entitäten in verschiedenen Ausführungseinheiten werden parallel verarbeitet.
- In jeder Ausführungseinheit werde Entitäten parallel verarbeitet, wenn sie dieselbe Ebene haben.
- Auf ejder Stufe werden Entitäten entsprechend der Sequenznummer in dieser Ebene verarbeitet.
- Nachdem eine Ebene verarbeitet wurde, wird die nächste Ebene verarbeitet.

#### <a name="resequencing"></a>Neue Reihenfolge
Möglicherweise empfiehlt es sich, die Entitäten in den folgenden Situationen neu zu ordnen:

- Wenn nur ein Datenenvorgang für alle Änderungen verwendet wird, können Sie die Optionen neu verwenden, um die Ausführungszeit des vollständigen Einzelvorgang zu optimieren. In diesen Fällen kann die Ausführungseinheit verwendet werden, um das Modul darzustellen, die Schichten im Funktionsbereich im Modul anzugeben und den Nummernkreis der zu zeigen. Wenn Sie diesen Ansatz verwenden, können Sie in allen Modulen parallel arbeiten, aber trotzdem in der Sequenz in einem Modul arbeiten. Zur Sicherstellung einer korrekten Erfassung , dass parallele Arbeitsgänge erfolgreich sind, müssen Sie alle Abhängigkeiten berücksichtigt.
- Wenn mehrere Dateneneinzelvorgänge, (beispielsweise ein Einzelvorgang für jedes Modul) verwendet werden, können Sie Abfolgen verenden, um die Ebene und den Nummernkreis von Entitäten für optimale Ausführung zu gewährleisten.
- Wenn es keine vorhanden Abhängigkeiten gibt, können Sie Nummernkreisentitäten an verschiedenen Ausführungseinheiten für maximale Optimierungsaufgaben definieren.

Das Menü **Neu Sequenzen** ist nur verfügbar, wenn mehrere Entitäten ausgewählt werden. Sie können neue Sequenzen basierend auf Grundlage der Ausführungseinheit, der Ebene oder der Nummernkreisoptionen definieren. Sie können eine Erhöhung zur neuen Sequenzierung der Entität festlegen, die ausgewählt wurden. Die Einheit, die Ebene und/oder eine laufende Nummer, die für jede Entität ausgewählt ist, wird durch die angegebene Erhöhung aktualisiert.

#### <a name="sorting"></a>Sortieren
Sie können die Option **Sortieren nach** verwenden, um die Entitätsliste in sequenzieller Reihenfolge anzuzeigen.

### <a name="truncating"></a>Kürzen
Bei Importprojekten können Sie Datensätze in den Entitäten vor dem Import kürzen. Dies ist nützlich, wenn Ihre Datensätze in einen leeren Satz Tabellen importiert werden müssen. Diese Einstellung ist standardmäßig ausgeschaltet.

## <a name="validate-that-the-source-data-and-target-data-are-mapped-correctly"></a>Überprüfen Sie, ob die Daten und die Zieldaten korrekt zugeordnet werden.
Zuordnung ist eine Funktion, die Importe und Exporteinzelvorgänge gilt.

- Im Kontext eines Importeinzelvorgangs beschreibt die Zuordnung, welche Spalten in der Quelldatei zu den Spalten in der Stagingtabelle werden. Daher kann das System bestimmen, welche Spaltendaten in der Quelldatei in welche Spalte Stagingtabelle kopiert werden müssen.
- Im Kontext eines Importeinzelvorgangs beschreibt die Zuordnung, welche Spalten in der Quelldatei zu den Spalten in der Stagingtabelle werden.

Wenn die Spaltennamen in der Stagingtabelle und die Datei übereinstimmen, erstellt das System automatisch die Zuordnung basierend auf den Namen. Wenn die Namen unterschiedlich sind, werden die Spalten nicht automatisch zugeordnet. In diesem Fall müssen Sie die Verknüpfung abschließen, indem Sie die Option **Ansichtszuordnung** für die Entität im Dateneneinzelvorgang auswählen.

Es gibt zwei zuzuordnende Ansichten: **Zuordnungsvisualisierung**, das die Standardansicht ist, und **Zuordnungsdetails**. Ein rotes Sternchen (\*) kennzeichnet alle Pflichtfelder in der Entität. Diese Felder müssen zugeordnet werden, damit die Entität arbeiten können. Sie können andere Felder nach Bedarf trennen, wenn Sie mit Entitäten arbeiten. Wenn Sie Felder trennen, wählen Sie entweder die Spalte **Entität** oder die Spalte **Quelle** aus und anschließend **Auswahl löschen**. Klicken Sie auf **Speichern** um die Änderungen zu speichern und zur Listenseite Projekte zurückzukehren. Sie können den gleichen Prozess verwenden, um Feldzuordnung von der Quelle zum Bereitstellen bearbeiten, nachdem Sie den Import ausgeführt haben.

Sie können auf der Seite eine Zuordnung generieren, indem Sie **Generieren Sie Quellzuordnung** auswählen. Eine generierte Zuordnung verhält sich wie eine automatische Zuordnung. Daher müssen Sie alle nicht zugeordneten Felder manuell zuordnen.

![Datenzuordnung.](./media/dixf-map.png)

## <a name="verify-the-security-for-your-import-or-export-job"></a>Überprüfen Sie die Sicherheit für den Export- oder Importvorgang.
Der Zugriff auf den Arbeitsbereich **Datenverwaltung** kann eingeschränkt werden, damit Benutzer nur auf bestimmte Dateneneinzelvorgänge zugreifen können. Der Zugriff auf einen Dateneneinzelvorgang bedeutet Zugriff auf die Ausführungshistorie dieses Einzelvorgangs und Zugriff auf die Tabellen. Daher müssen Sie prüfen, ob übereinstimmende Zugriffssteuerungen vorhanden sind, wenn Sie einen Dateneneinzelvorgang erstellen.

### <a name="secure-a-job-by-roles-and-users"></a>Sichern Sie einen Einzelvorgang nach Rollen und Benutzer
Verwenden Sie das Menü **Anwendbare Rollen**, um den Einzelvorgang für mindestens eine Sicherheitsrolle einzuschränken. Nur Benutzer mit diesen Rollen haben Zugriff auf den Einzelvorgang.

Darüber hinaus können Sie einen Auftrag für bestimmte Benutzer einschränken. Wenn Sie einen Einzelvorgang nach Benutzer und nicht nach Rollen speichern, gibt es weitere Steuerelemente, falls mehrere Benutzer einer Rolle zugewiesen sind.

### <a name="secure-a-job-by-legal-entity"></a>Einen Einzelvorgang nach juristischer Person schützen
Dateneneinzelvorgänge sind global. Wenn ein Dateneneinzelvorgang erstellt wurde und in einer juristischen Person ist, wird der Einzelvorgang in anderen juristischen Personen im System angezeigt. Dieses Standardverhalten kann in einigen Anwendungsszenarien bevorzugt werden. So kann eine Organisation, die Rechnungen importiert, indem Sie Datenentitäten verwendet, ein zentralisiertes Fakturierungsteam bereitstellen, das zur Verwaltung von Rechnungsfehlern für alle Geschäftsbereiche in der Organisation verantwortlich ist. In diesem Szenario ist es hilfreich für das zentralisierte Fakturierungsteam, den Zugriff auf die Rechnungsimporteinzelvorgängen von allen juristischen Personen verwendet werden. Daher entspricht das Standardverhalten der Bedingung aus einer Perspektive der juristischen Person.

Allerdings sollte eine Organisation Fakturierungsteams pro juristische Personen enthalten. In diesem Fall sollte ein Team in einer juristischen Personen nur Zugriff auf Rechnungsimporteinzelvorgang in der eigenen juristischen Personen enthalten. Um dieser Bedingung zu entsprechen, können Sie Entität-basierte gültige Zugriffssteuerung auf den Dateneneinzelvorgängen konfigurieren indem Sie **Anwendbare juristische Personen** im Dateneneinzelvorgangs verwenden. Nachdem die Konfiguration erfolgt ist, können Benutzer nur Stellen anzeigen, die für die juristische Person verfügbar sind, bei dem sie derzeit angemeldet sind. Um Einzelvorgänge einer anderen juristischen Person zu finden, müssen Benutzer diese juristische Person verwendet.

Einer Stelle kann durch Rollen, Benutzer und juristischen Person gleichzeitig geschützt werden.

## <a name="run-the-import-or-export-job"></a>Führt den Import- oder Exportvorgang aus
Sie können einen Einzelvorgang gleichzeitig aktivieren, indem Sie **Importieren** **Exportieren** auswählen, nachdem Sie den Einzelvorgang definiert haben. Um einen sich wiederholenden Auftrag einzurichten, wählen Sie **Erstellen eines sich wiederholenden Dateneneinzelvorgangs** aus.

> [!NOTE]
> Ein Import- oder Exportvorgang kann ausgeführt werden, indem Sie die Schalfläche **Importieren** bzw. **Exportieren** auswählen. Dadurch wird ein Batchauftrag so geplant, dass er nur einmal ausgeführt wird. Der Einzelvorgang wird möglicherweise nicht sofort ausgeführt, wenn der Batchservice aufgrund der Belastung des Batchservice gedrosselt wird. Die Einzelvorgänge können durch Auswahl von **Jetzt importieren** oder **Jetzt exportieren** synchron ausgeführt werden. Dadurch wird der Einzelvorgang sofort gestartet. Das ist hilfreich, wenn der Batchauftrag aufgrund einer Drosselung nicht startet. Die Einzelvorgänge können auch so geplant werden, dass sie zu einem späteren Zeitpunkt ausgeführt werden. Dies kann durch Auswahl der Option **Im Batch ausführen** erfolgen. Stapelressoucen sind von Drosselung betroffen. Der Einzelvorgang zur Stapelverarbeitung startet also möglicherweise nicht sofort. Die Verwendung einer Stapelverarbeitung wird empfohlen, da dies auch bei großen Datenmengen hilfreich ist, die importiert oder exportiert werden müssen. Chargensaufträge können geplant wurden, sodass sie in einer bestimmte Chargengruppe ausgeführt werden. Dies bietet von einer Lastenausgleichsperspektive aus betrachtet eine bessere Steuerung.

## <a name="validate-that-the-job-ran-as-expected"></a>Überprüfen Sie, ob der Einzelvorgang wie erwartet ausgeführt wurde
Die Einzelvorgangshistorie ist zur Problembehebung und Untersuchung auf Import- und Exporteinzelvorgängen verfügbar. Historische Einzelvorgangsausführungen werden nach Perioden sortiert.

![Historie des Stapelverarbeitungsauftrags.](./media/dixf-job-history.md.png)

Jede Einzelvorgangsausführung enthält die folgenden Details:

- Ausführungsdetails
- Ausführungsprotokoll

Ausführungsdetails zeigt den Status der einzelnen Datenentitäten an, die den Einzelvorgang verarbeitet. Daher können Sie die folgenden Informationen schnell suchen:

- Welche Entitäten verarbeitet wurden
- Für eine Entität, wie viele Datensätze erfolgreich verarbeitet wurden und wie viele nicht erfolgreich waren
- Die Stagingdatensätze für jede Entität

Sie können die Stagingdaten in Einzelvorgängen einer Datei für den Export herunterladen, oder Sie können sie als Paket für Import- und Exporteinzelvorgänge herunterladen.

Aus den Ausführungsdetails können Sie auch das Ausführungsprotokoll öffnen.

## <a name="parallel-imports"></a>Parallelimporte
Um den Import von Daten zu beschleunigen, kann die parallele Verarbeitung des Imports einer Datei aktiviert werden, wenn die Entität parallele Importe unterstützt. Um den Parallelimport für eine Entität zu konfigurieren, müssen die folgenden Schritte ausgeführt werden.

1. Wechseln Sie zu **Systemverwaltung \> Arbeitsbereiche \> Datenverwaltung**.
2. Im Abschnitt **Import/Export** wählen Sie die Kachel **Frameworkparameter** zum Öffnen der Seite **Rahmenparameter für Datenimport/-export**.
3. Auf der Registerkarte **Entitätseinstellungen** wählen Sie **Entitätsausführungsparameter konfigurieren**, um die Seite **Ausführungsparameter für den Entitätsimport** zu öffnen.
4. Legen Sie die folgenden Felder fest, um den Parallelimport für eine Entität zu konfigurieren:

    - Wählen Sie im Feld **Entität** aus, die Entität aus.
    - Geben Sie im Feld **Importschwellenwert für Datensatzanzahl** die Anzahl der Schwellenwerte für den Import ein. Dies bestimmt die Anzahl der Datensätze, die von einem Thread verarbeitet werden sollen. Wenn eine Datei 10 KB an Datensätzen enthält, bedeutet eine Datensatzanzahl von 2500 mit einer Aufgabenanzahl von 4, dass jeder Thread 2500 Datensätze verarbeitet.
    - Im Feld **Aufgabenanzahl importieren** geben Sie die Anzahl der Importaufgaben ein. Dies darf die maximale Anzahl von Batch-Threads nicht überschreiten, die für die Stapelverarbeitung in **Systemadministration \>Serverkonfiguration** zugewiesen sind.

## <a name="job-history-clean-up"></a>Auftragshistorie bereinigen 
Die Funktion zur Bereinigung des Auftragsverlaufs in der Datenverwaltung muss verwendet werden, um eine regelmäßige Bereinigung des Ausführungsverlaufs einzuplanen. Diese Funktion ersetzt die vorherige Bereinigungsfunktion für Stagingtabellen, die ab sofort nicht mehr bereitgestellt wird. Die folgenden Tabellen werden durch den Bereinigungsprozess bereinigt.

-   Alle Stagingtabellen

-   DMFSTAGINGVALIDATIONLOG

-   DMFSTAGINGEXECUTIONERRORS

-   DMFSTAGINGLOGDETAIL

-   DMFSTAGINGLOG

-   DMFDEFINITIONGROUPEXECUTIONHISTORY

-   DMFEXECUTION

-   DMFDEFINITIONGROUPEXECUTION

Die Funktionen **Bereinigung des Ausführungsverlaufs** müssen in der Funktionsverwaltung aktiviert werden und sind über **Datenverwaltung \> Bereinigung des Einzelvorgangsverlaufs** verfügbar.

### <a name="scheduling-parameters"></a>Planungsparameter

Wenn Sie den Bereinigungsprozess planen, müssen die folgenden Parameter angegeben werden, um die Bereinigungskriterien zu definieren.

-   **Anzahl der Tage zur Beibehaltung des Verlaufs** – Diese Einstellung wird verwendet, um den Umfang des beizubehaltenden Ausführungsverlaufs zu steuern. Wird in Anzahl Tagen angegeben. Wenn der Bereinigungsauftrag als wiederkehrender Batchauftrag geplant wird, funktioniert diese Einstellung wie ein sich fortlaufend bewegendes Fenster, das heißt, der Verlauf wird für die angegebene Anzahl von Tagen unverändert gelassen, während der Rest gelöscht wird. Der Standardwert ist 7 Tage.

-   **Anzahl der Stunden für die Ausführung des Auftrags** – Je nach Umfang des zu bereinigenden Verlaufs kann die gesamte Ausführungszeit für den Bereinigungsauftrag von wenigen Minuten bis zu ein paar Stunden variieren. Dieser Parameter muss auf die Anzahl der Stunden eingestellt werden, die der Job ausgeführt wird. Nachdem der Bereinigungsjob für die angegebene Anzahl von Stunden ausgeführt wurde, wird der Job beendet und bei der nächsten Ausführung auf der Grundlage des Wiederholungszeitplans wieder aufgenommen.

    Eine maximale Ausführungszeit kann durch Festlegen eines Höchstlimits für die Anzahl der Stunden angegeben werden, die der Auftrag unter Verwendung dieser Einstellung ausgeführt werden muss. Die Bereinigungslogik geht chronologisch eine Auftragsausführungskennung nach der anderen durch. Dabei wird die älteste bei der Bereinigung des entsprechenden Ausführungsverlaufs zuerst berücksichtigt. Sie endet mit der Verarbeitung neuer Ausführungskennungen für die Bereinigung, wenn die verbleibende Ausführungsdauer innerhalb der letzten 10 % des angegebenen Zeitraums liegt. In einigen Fällen wird der Bereinigungsauftrag erwartungsgemäß über die angegebene Höchstzeit fortgesetzt. Dies hängt weitestgehend von der Anzahl der Datensätze ab, die für die aktuelle Ausführungskennung zu löschen sind, die gestartet wurde, bevor der Schwellenwert von 10 % erreicht wurde. Die Bereinigung, die gestartet wurde, muss abgeschlossen werden, um die Datenintegrität sicherzustellen. Dies bedeutet, dass die Bereinigung auch dann fortgesetzt wird, denn das angegebene Limit überschritten wurde. Wenn der Vorgang abgeschlossen ist, werden keine neuen Ausführungskennungen verarbeitet und der Bereinigungsauftrag wird abgeschlossen. Der verbleibende Ausführungsverlauf, der aufgrund unzureichender Ausführungszeit nicht bereinigt wurde, wird das nächste Mal verarbeitet, wenn der Bereinigungsauftrag eingeplant wird. Der Standard- und Mindestwert für diese Einstellung ist 2 Stunden.

-   **Wiederkehrender Stapel** – Der Bereinigungsauftrag kann als einmalige, manuelle Ausführung ausgeführt oder für eine wiederkehrende Ausführung in Stapeln eingeplant werden. Der Stapel kann mithilfe der Einstellungen **Im Hintergrund ausführen** geplant werden. Dies ist die Standardstapeleinstellung.

> [!NOTE]
> Wenn Sätze in den Staging-Tabellen nicht vollständig bereinigt werden, stellen Sie sicher, dass der Bereinigungsjob für die Ausführung in Wiederholung eingeplant wird. Wie oben erläutert, wird der Job bei jeder Bereinigungsausführung nur so viele Ausführungs-IDs bereinigen, wie innerhalb der vorgegebenen maximalen Stunden möglich sind. Um mit der Bereinigung der verbleibenden Staging-Datensätze fortzufahren, muss der Job für eine periodische Ausführung eingeplant werden.

## <a name="job-history-clean-up-and-archival"></a>Bereinigung und Archivierung des Einzelvorgangsverlaufs 
Die Funktionen zum Bereinigen und Archivieren des Einzelvorgangsverlaufs ersetzen die vorherigen Versionen der Bereinigungsfunktion. In diesem Abschnitt werden diese neuen Funktionen erläutert.

Eine der wichtigsten Änderungen an der Bereinigungsfunktion ist die Verwendung des System-Batchauftrags zum Bereinigen des Verlaufs. Die Verwendung des System-Batchauftrags ermöglicht Finance and Operations-Apps die automatische Planung und Ausführung des Batchauftrags zur Bereinigung, sobald das System bereit ist. Es ist nicht mehr erforderlich, den Batchauftrag manuell zu planen. In diesem Standardausführungsmodus wird der Batchauftrag ab Mitternacht jede Stunde ausgeführt und der Ausführungsverlauf für die letzten 7 Tage beibehalten. Der gelöschte Verlauf wird für den zukünftigen Abruf archiviert. Ab Version 10.0.20 ist diese Funktion immer aktiviert.

Die zweite Änderung am Bereinigungsprozess ist die Archivierung des gelöschten Ausführungsverlaufs. Der Bereinigungsauftrag archiviert die gelöschten Datensätze im Blob Storage, den DIXF für regelmäßige Integrationen verwendet. Die archivierte Datei liegt im DIXF-Paketformat vor und ist 7 Tage lang im Blob verfügbar. Während dieser Zeit kann sie heruntergeladen werden. Die Standardlebensdauer von 7 Tagen für die archivierte Datei kann in den Parametern auf maximal 90 Tage geändert werden.

### <a name="changing-the-default-settings"></a>Standardeinstellungen ändern
Diese Funktion ist derzeit in der Vorschau verfügbar und muss explizit aktiviert werden, indem der Flight DMFEnableExecutionHistoryCleanupSystemJob aktiviert wird. Die Funktion zur Stagingbereinigung muss auch in der Funktionsverwaltung aktiviert sein.

Um die Standardeinstellung für die Langlebigkeit der archivierten Datei zu ändern, wechseln Sie zum Datenverwaltungsarbeitsbereich und wählen Sie **Bereinigung des Auftragsverlaufs** aus. Legen Sie **Tage zur Beibehaltung des Pakets im Blob** auf einen Wert zwischen 7 und 90 (inklusive) fest. Dies tritt für die Archive in Kraft, die nach dieser Änderung erstellt werden.

### <a name="downloading-the-archived-package"></a>Archiviertes Paket herunterladen
Diese Funktion ist derzeit in der Vorschau verfügbar und muss explizit aktiviert werden, indem der Flight DMFEnableExecutionHistoryCleanupSystemJob aktiviert wird. Die Funktion zur Stagingbereinigung muss auch in der Funktionsverwaltung aktiviert sein.

Um den archivierten Ausführungsverlauf herunterzuladen, wechseln Sie zum Datenverwaltungsarbeitsbereich und wählen Sie **Bereinigung des Auftragsverlaufs** aus. Wählen Sie **Verlauf Paketsicherung** aus, um das Verlaufsformular zu öffnen. Dieses Formular zeigt die Liste aller archivierten Pakete an. Ein Archiv kann durch Auswahl von **Paket herunterladen** ausgewählt und heruntergeladen werden. Das heruntergeladene Paket liegt im DIXF-Paketformat vor und enthält die folgenden Dateien:

-   Die Stagingtabellendatei der Entität
-   DMFDEFINITIONGROUPEXECUTION
-   DMFDEFINITIONGROUPEXECUTIONHISTORY
-   DMFEXECUTION
-   DMFSTAGINGEXECUTIONERRORS
-   DMFSTAGINGLOG
-   DMFSTAGINGLOGDETAILS
-   DMFSTAGINGVALIDATIONLOG



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
