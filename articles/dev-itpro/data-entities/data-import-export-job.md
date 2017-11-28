---
title: "Einzelvorgänge für Datenimport und -export"
description: "Verwenden Sie den Datenverwaltungsarbeitsbereich, um Datenimport- und Exporteinzelvorgänge zu erstellen und zu verwalten."
author: Sunil-Garg
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e79fcaa634c4b4eb601241d75da2f36f2455db4e
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="data-import-and-export-jobs"></a>Einzelvorgänge für Datenimport und -export

[!include[banner](../includes/banner.md)]

Um Datenimport- und Datenexportaufträge in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, zu erstellen und zu verwalten verwenden Sie den Arbeitsbereich**Datenverwaltung**. Standardmäßig der Datenimport und der Exportvorgang eine für jede Stagingtabelle Entität in der Zieldatenbank erstellt. Mit Stagingtabellen können Sie Daten prüfen, bereinigen oder konvertieren, bevor Sie diese verschieben.

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

## <a name="create-an-import-or-export-job"></a>Erstellen eines Import- oder Exportvorgangs
Ein  Datenimport- oder Exportvorgang kann einmal oder mehrmals ausgeführt werden.

### <a name="define-the-project-category"></a>Projektkategorie definieren
Es wird empfohlen, Zeit zu nehmen, um eine entsprechende Projektkategorie für den Import- oder Exportvorgang zu wählen. Projektkategorien können helfen, zugehörige Einzelvorgänge zu verwalten.

### <a name="identify-the-entities-to-import-or-export"></a>Geben Sie die Entitäten an, um Daten zu importieren oder zu exportieren.
Sie können bestimmte Entitäten einem Import- oder Exportvorgang hinzufügen oder eine Vorlage auswählen, die übernommen werden soll. Vorlagen füllen einen Einzelvorgang mit einer Liste von Entitäten aus. Die Option **Vorlage anwenden** ist verfügbar, wenn Sie dem Einzelvorgang einen Namen geben und den Einzelvorgang speichern.

### <a name="set-the-data-format-for-the-job"></a>Legen Sie das Datenformat für den Stapelverarbeitungsauftrag fest.
Wenn Sie eine Einheit auswählen, müssen Sie die Verpackungseinheiten das Format der Daten auswählen, die exportiert oder importiert werden. Sie legen Formate fest, indem Sie die Kachel **Datenquelleneinstellung** verwenden. Viele Organisationen beginnen  mit den Formaten, die standardmäßig im Demodatsatz enthalten sind. Das hier eine Liste mit einigen dieser Formate:

- AX (für Daten, die im gleichen Format importiert oder exportiert werden müssen, die für Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition) verwendet werden.
- ColonSeparated
- CSV
- Excel
- Paket

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

## <a name="validate-that-the-source-data-and-target-data-are-mapped-correctly"></a>Überprüfen Sie, ob die Daten und die Zieldaten korrekt zugeordnet werden.
Zuordnung ist eine Funktion, die Importe und Exporteinzelvorgänge gilt.

- Im Kontext eines Importeinzelvorgangs beschreibt die Zuordnung, welche Spalten in der Quelldatei zu den Spalten in der Stagingtabelle werden. Daher kann das System bestimmen, welche Spaltendaten in der Quelldatei in welche Spalte Stagingtabelle kopiert werden müssen.
- Im Kontext eines Importeinzelvorgangs beschreibt die Zuordnung, welche Spalten in der Quelldatei zu den Spalten in der Stagingtabelle werden.

Wenn die Spaltennamen in der Stagingtabelle und die Datei übereinstimmen, erstellt das System automatisch die Zuordnung basierend auf den Namen. Wenn die Namen unterschiedlich sind, werden die Spalten nicht automatisch zugeordnet. In diesem Fall müssen Sie die Verknüpfung abschließen, indem Sie die Option **Ansichtszuordnung** für die Entität im Dateneneinzelvorgang auswählen.

Es gibt zwei zuzuordnende Ansichten: **Zuordnungsvisualisierung**, das die Standardansicht ist, und **Zuordnungsdetails**. Ein rotes Sternchen (\*) kennzeichnet alle Pflichtfelder in der Entität. Diese Felder müssen zugeordnet werden, damit die Entität arbeiten können. Sie können andere Felder nach Bedarf trennen, wenn Sie mit Entitäten arbeiten. Wenn Sie Felder trennen, wählen Sie entweder die Spalte **Entität** oder die Spalte **Quelle** aus und anschließend **Auswahl löschen**. Klicken Sie auf **Speichern** um die Änderungen zu speichern und zur Listenseite Projekte zurückzukehren. Sie können den gleichen Prozess verwenden, um Feldzuordnung von der Quelle zum Bereitstellen bearbeiten, nachdem Sie den Import ausgeführt haben.

Sie können auf der Seite eine Zuordnung generieren, indem Sie **Generieren Sie Quellzuordnung** auswählen. Eine generierte Zuordnung verhält sich wie eine automatische Zuordnung. Daher müssen Sie alle nicht zugeordneten Felder manuell zuordnen.

![Datenzuordnung](./media/dixf-map.png)

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

## <a name="validate-that-the-job-ran-as-expected"></a>Überprüfen Sie, ob der Einzelvorgang wie erwartet ausgeführt wurde
Die Einzelvorgangshistorie ist zur Problembehebung und Untersuchung auf Import- und Exporteinzelvorgängen verfügbar. Historische Einzelvorgangsausführungen werden nach Perioden sortiert.

![Historie des Stapelverarbeitungsauftrags](./media/dixf-job-history.md.png)

Jede Einzelvorgangsausführung enthält die folgenden Details:

- Ausführungsdetails
- Ausführungsprotokoll

Ausführungsdetails zeigt den Status der einzelnen Datenentitäten an, die den Einzelvorgang verarbeitet. Daher können Sie die folgenden Informationen schnell suchen:

- Welche Entitäten verarbeitet wurden
- Für eine Entität, wie viele Datensätze erfolgreich verarbeitet wurden und wie viele Prüfung nicht erfolgreich waren
- Die Stagingdatensätze für jede Entität

Sie können die Stagingdaten in Einzelvorgängen einer Datei für den Export herunterladen, oder Sie können sie als Paket für Import- und Exporteinzelvorgänge herunterladen.

Aus den Ausführungsdetails können Sie auch das Ausführungsprotokoll öffnen.

## <a name="clean-up-the-staging-tables"></a>Bereinigen der Tabellen
Sie können Tabellen bereinigen, indem Sie die Funktion **Bereinigen der Tabellen** im **Datenverwaltung** Arbeitsbereich verwenden. Sie können folgende Optionen verwenden, um auszuwählen, welche Datensätze gelöscht werden sollen, aus den Stagingtabellen:

- **Entität** – Wenn nur eine Entität angegeben wurde, werden alle Datensätze ab dieser Stagingtabellen Entität gelöscht. Wählen Sie diese Option aus, um alle Daten für die Entität zu allen Datenprojekten und allen Einzelvorgängen zu bereinigen.
- **Auftrags-ID** – Wenn nur eine Einzelvorgangskennung angegeben wurde, werden alle Datensätze für allen Entitäten im ausgewählten Einzelvorgang aus den entsprechenden Tabellen gelöscht.
- **Datenprojekte** – Wenn nur ein Datenprojekt aktiviert ist, werden alle Datensätze für alle Entitäten und zu allen Einzelvorgängen für das ausgewählte Datenprojekt gelöscht.

Sie können auch die Optionen kombinieren, um den Datensatz einzuschränken, der gelöscht werden soll.

