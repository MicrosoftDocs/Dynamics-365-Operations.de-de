---
title: Arbeiten Sie mit Einrichtungen für Funktionen
description: In diesem Artikel wird erklärt, wie Sie die Funktionen für die Elektronische Rechnungsstellung festlegen.
author: dkalyuzh
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 23466a53bb8ba597503aaa12d41395fc82b9f14e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904324"
---
# <a name="work-with-feature-setups"></a>Arbeiten Sie mit Einrichtungen für Funktionen

[!include [banner](../includes/banner.md)]

Um die Erzeugung elektronischer Dateien und andere Verarbeitungsschritte einzurichten (z.B. das digitale Signieren von Dateien, das Senden an den Webdienst der Regierung und das Empfangen einer Antwort oder das Speichern der Dateien), legen Sie die Pipeline für die Verarbeitung, die Regeln für die Anwendbarkeit und die Variablen für die Funktionen der Elektronischen Rechnungsstellung fest.

Die Einrichtungsinformationen werden im *Funktionseinrichtungskonzept* zusammengefasst und können erstellt, gelöscht und angepasst werden. Für die abgeschlossenen Versionen der Funktionen der Elektronischen Rechnungsstellung können die Informationen ebenfalls eingesehen werden.

Sie können so viele Elemente für die Einrichtung von Funktionen erstellen, wie Sie benötigen, um verschiedene Szenarien für die Erstellung, die Verarbeitung und den Empfang elektronischer Dateien zu definieren. Obwohl diese Elemente für die Einrichtung der Funktion über unabhängige Verarbeitungsaktionen und Ausführungsbedingungen verfügen, werden sie als Teil einer einzigen Funktion für die Elektronische Rechnungsstellung erstellt und erben deren Lebenszyklus und Bereitstellungsprozess.

## <a name="add-a-feature-setup"></a>Hinzufügen einer Einrichtung für eine Funktion

1. Melden Sie sich bei Ihrem RCS-Konto (Regulatory Configuration Service) an.
2. Wählen Sie im Abschnitt **Funktionen** des Arbeitsbereichs **Globalisierungsfunktion** die Kachel **Elektronische Rechnungsstellung** aus.
3. Wählen Sie auf der Seite **Elektronische Rechnungsstellung** eine Funktion für die elektronische Rechnungsstellung aus, die den Status **Entwurf** hat.
4. Auf der Registerkarte **Einrichtungen** wählen Sie **Hinzufügen**.
5. Wählen Sie im Dropdown-Dialog **Einrichtung einer Funktion erstellen** in der Feldgruppe **Neu** eine der folgenden Optionen:
 
    - **Benutzerdefinierte Einrichtung** - Erstellen Sie eine neue Einrichtung für eine Funktion mit leeren Kanälen, einer leeren Pipeline-Liste für die Verarbeitung, einem leeren Abschnitt für Anwendbarkeitsregeln und einem Standardsatz von Variablen, abhängig vom Einrichtungstyp.
    - **Von der Einrichtung einer Funktion** - Erstellt eine Kopie einer anderen Einrichtung einer Funktion im Rahmen der aktuellen Funktion Elektronische Rechnungsstellung.

6. Wenn Sie im letzten Schritt die Option **Benutzerdefinierte Einrichtung** gewählt haben, geben Sie einen Namen und eine Beschreibung für das Element zur Einrichtung der Funktion ein und wählen dann in der Feldgruppe **Einrichtungstyp** eine der folgenden Optionen aus:

    - **Pipeline verarbeiten** - Wählen Sie diese Option, um ausgehende elektronische Belege zu erzeugen und zu verarbeiten. Für diesen Einrichtungstyp erstellt das System eine leere Pipeline-Liste für die Verarbeitung, einen leeren Abschnitt für Anwendbarkeitsregeln und einen Standardsatz von Variablen. Sie werden nicht mit den Kanälen für eingehende elektronische Belege arbeiten können.
    - **Datenkanal** – Wählen Sie diese Option, um den Prozess des Empfangs eingehender elektronischer Belege von einem der definierten Kanäle festzulegen und sie direkt an Microsoft Microsoft Dynamics 365 Finance oder Dynamics 365 Supply Chain Management ohne zusätzliche Aktionen zu übergeben. Für diesen Einrichtungstyp erstellt das System eine vordefinierte Liste von Parametern für die Datenkanäle, einen leeren Abschnitt für Anwendbarkeitsregeln und einen Satz von Standardvariablen. Sie werden keine Aktionen in der Pipeline für die Verarbeitung hinzufügen können.
    - **Datenkanal und Verarbeitungspipeline** - Dieser Einrichtungstyp ähnelt dem Einrichtungstyp **Datenkanal**. Bevor ein eingehender elektronischer Beleg an Finance oder Supply Chain Management weitergeleitet wird, können Sie jedoch zusätzliche Aktionen in der Pipeline für die Verarbeitung festlegen.

7. Wenn Sie im letzten Schritt die Option **Datenkanal** oder **Datenkanal und Verarbeitungspipeline** gewählt haben, müssen Sie im Feld **Datenkanal auswählen** den Kanal auswählen, in den integriert werden soll.
8. Wählen Sie **Erstellen** aus.

Nachdem eine Einrichtung erstellt wurde, können Sie **Bearbeiten** wählen, um die Funktion zu konfigurieren.

## <a name="edit-a-feature-setup"></a>Bearbeiten Sie eine Einrichtung für eine Funktion

Je nach Art der Einrichtung der Funktion können Sie den Prozess der Generierung ausgehender elektronischer Belege und deren Senden an externe Kanäle oder den Empfang eingehender Belege und deren Weiterleitung an Ihre Finance- oder Supply Chain Management-Anwendung konfigurieren.

### <a name="data-channel"></a>Datenkanal

Ein *Datenkanal* nimmt die elektronische Datei auf und verarbeitet sie entweder oder leitet sie direkt an Finance oder Supply Chain Management weiter. Diese Option ist nicht verfügbar für Funktionen des Typs **Pipeline verarbeiten**.

Um einen Datenkanal festzulegen, geben Sie den Namen des Kanals ein. Definieren Sie dann die Parameter, basierend auf dem gewählten Channel-Typ. Die Kennung des Datenkanals muss sich auf die Variable beziehen, die speziell zur Identifizierung des Datenkanals erstellt wird. Es wird als Referenz in Finance oder Supply Chain Management verwendet.

Auf der Registerkarte **Anhangsfilter** sollten Sie eine Reihe von Filtern festlegen, um bestimmte Dateien aus dem Channel zu erhalten. Sie können mehrere Zeilen erstellen, wenn Sie davon ausgehen, dass Dateien unterschiedliche Dateinamenserweiterungen haben werden oder wenn Dateien je nach Dateiname unterschiedlich verarbeitet werden müssen. Hier sind die wichtigsten Parameter:

- **Name** - Geben Sie den Namen der Datei ein, auf die sich das System bei der Verarbeitung bezieht. In den Anwendungen Finance und Supply Chain Management werden Sie die Dateien im Einreichungsprotokoll sehen können.
- **Filter** - Definieren Sie den Filter zur Auswahl der Dateien.
- **Optional** - Wenn dieses Kontrollkästchen deaktiviert ist, ist die Datei erforderlich. In diesem Fall zeigt das System eine Fehlermeldung an, wenn die Kanäle keine Dateien enthalten, die dem Filter entsprechen. Dieser Parameter ist auf E-Mails anwendbar.

Wenn es sich bei dem Channel um ein Postfach handelt und eine eingehende E-Mail mehrere Anhänge enthält, können Sie Regeln konfigurieren, um festzulegen, wie der Dienst Anhänge behandeln soll. Der Dienst kann jeden Anhang als separate elektronische Rechnung betrachten, oder er kann einen Anhang als Hauptrechnung und alle anderen Anhänge als Ergänzungen behandeln.

### <a name="processing-pipeline"></a>Verarbeitungspipeline

Eine *Verarbeitungs Pipeline* ist eine Reihe von *Aktionen*, die nacheinander ausgeführt werden, bis sie erfolgreich abgeschlossen sind. Sie können eine Pipeline für die Verarbeitung verwenden, um den Prozess für die Erzeugung elektronischer Belege und die Durchführung anderer Schritte festzulegen (z.B. das digitale Signieren von Dateien, das Senden an externe Webdienste und das Parsen der Antwort sowie den Empfang und die Verarbeitung eingehender Dokumente).

Die Liste der Aktionen ist vordefiniert. Mit den Schaltflächen **Neu** und **Löschen** können Sie die Kombination von Aktionen festlegen, die den gewünschten Prozess zum Senden oder Empfangen von Dokumenten logisch definiert.

Die Reihenfolge der Aktionen ist wichtig. Sie können die Reihenfolge mit den Schaltflächen **Auf** und **Ab** anpassen.

Für jede Aktion gibt es eine Reihe von Parametern, die Sie konfigurieren oder anpassen können. Welche Parameter genau festgelegt werden, hängt von der Art der Aktion ab.

- **Aktion** - Wählen Sie die Art der Aktion aus.
- **Aktionsname** - Geben Sie den Namen der Aktion ein. Dieser Name erscheint in Übermittlungsprotokollen und in Nachrichten in den Anwendungen Finance und Supply Chain Management.
- **Beschreibung** - Geben Sie weitere Details über den Zweck der Aktion im Prozess an.
- **Wiederholung aktivieren** - Wenn Sie dieses Kontrollkästchen aktivieren, können Sie eine Aktion im Feld **Wiederholungsaktion** auswählen und zusätzliche Parameter auf der Registerkarte **Wiederholungsparameter** konfigurieren.

    Mit der Wiederholungsfunktion können Sie das Verhalten des Dienstes konfigurieren, wenn eine bestimmte Aktion nicht ausgeführt werden kann. Wenn der externe Webdienst, zu dem Sie eine Verbindung herstellen möchten, beispielsweise nicht antwortet, können Sie angeben, wie oft das System die Verbindung erneut versuchen soll, in welchem Intervall und ab welcher Aktion in der Pipeline der Verarbeitung.

- **Ergebnisse exportieren** - Sie können dieses Kontrollkästchen für *eine* Aktion in der Pipeline der Verarbeitung aktivieren. Die elektronische Datei, die die Aktion in der Anwendung Finance oder Supply Chain Management erzeugt, kann dann von der Seite **Protokoll der Einreichung elektronischer Belege** exportiert werden.

### <a name="applicability-rules"></a>Regeln für die Anwendbarkeit

*Anwendbarkeitsregeln* sind konfigurierbare Klauseln, die den Kontext für das Ausführen von Funktionen der Elektronischen Rechnungsstellung über die auf der Elektronischen Rechnungsstellung festgelegten Funktionalitäten liefern.
Geschäftsdokumente, die von Finance oder Supply Chain Management an die Elektronische Rechnungsstellung gesendet werden, enthalten keinen expliziten Verweis, der festlegt, dass die Funktionalitäten der Elektronischen Rechnungsstellung eine bestimmte Version der Funktion Elektronische Rechnungsstellung und ein bestimmtes Element zur Einrichtung der Funktion aufrufen, um die Übermittlung zu verarbeiten. Wenn ein elektronischer Beleg jedoch korrekt konfiguriert ist, enthält er die erforderlichen Elemente, die es der Elektronischen Rechnungsstellung ermöglichen, zu bestimmen, welche Version der Funktion Elektronische Rechnungsstellung und der Pipeline für die Verarbeitung ausgewählt und ausgeführt werden muss.

Anwendbarkeitsregeln ermöglichen es dem Dienst für die elektronische Rechnungsstellung, die genauen Funktionen für die elektronische Rechnungsstellung zu finden, die für die Verarbeitung einer Einreichung verwendet werden müssen. Um die richtigen Funktionen zu finden, werden die **Kontext**-Felder aus dem gesendeten Geschäftsdokument mit Klauseln aus den Anwendbarkeitsregeln abgeglichen.

Sie können mit Anwendbarkeitsregeln auf folgende Weise arbeiten:

- Wählen Sie **Neu**, um eine neue Klausel auf einem festgelegten Regelwerk für die Anwendbarkeit hinzuzufügen.
- Wählen Sie **Löschen**, um eine Klausel zu löschen.
- Wählen Sie mehrere Datensätze aus und erstellen Sie über die Schaltflächen **Gruppieren** oder **Ungruppieren** eine Kombination von Elementen oder logischen Aussagen. Markieren Sie zum Beispiel die Zeilen, die Sie gruppieren möchten, und wählen Sie dann **Gruppierungsklausel**. Wenn Klauseln gruppiert werden, wird dem Raster eine neue Spalte hinzugefügt. Diese Spalte gibt den logischen Operator für die Gruppenklausel an. Die folgenden Arten von Vorgängen werden unterstützt:

    - Equal
    - Not equal
    - Größer als, kleiner als
    - Größer als oder gleich, kleiner als oder gleich
    - Enthält
    - Beginnen mit

    > [!NOTE]
    > Wenn Sie die Gruppierung für eine Klausel aufheben, beginnen Sie immer mit der innersten Gruppierungsebene.

### <a name="variables"></a>Variable

*Variablen* geben Ihnen mehr Flexibilität, wenn Sie eine Pipeline für die Verarbeitung und den Flow der Daten zwischen den Aktionen festlegen. Sie können in einigen Aktionsparametern auf eine Variable verweisen, um Daten oder elektronische Dateien vorübergehend zu speichern. Einige Variablen werden verwendet, um Daten zwischen Finance- oder Supply Chain Management-Anwendungen und dem Dienst für die elektronische Rechnungsstellung zu übermitteln.

Das System erstellt standardmäßig einige Variablen. Die Variable **BusinessDocumentDataModel** enthält z.B. Geschäftsdaten in einer JavaScript Object Notation (JSON)-Struktur, die beim Aufruf von der angeschlossenen Anwendung während des Einreichungsprozesses kommt.

Die folgenden Arten von Variablen sind verfügbar:

- **Konstant** - Ein Container zum Speichern temporärer Daten, die bei der Verarbeitung von Pipeline-Aktionen verwendet werden.
- **Vom Client** - Der Inhalt der Variable wird vom Dynamics 365 Client bezogen, wenn der Einreichungsprozess ausgeführt wird.
- **An Client** - Der Inhalt der Variablen wird für den Import durch den Dynamics 365 Client zur Verfügung gestellt, wenn der Übermittlungsprozess ausgeführt wird.
- **Datentyp** - Wählen Sie den Datentyp der Informationen, die in der Variable gespeichert werden.

### <a name="parameters"></a>Parameter

Die Option **Reduzierung der Geschäftsdaten deaktivieren** dient zur Optimierung der Struktur des Payloads der Geschäftsdaten, die bei der Einreichung elektronischer Belege aus der Anwendung Finance oder Supply Chain Management kommen. Die Optimierung trägt dazu bei, die Daten zu reduzieren, die in den Dienst für die elektronische Rechnungsstellung zur weiteren Umwandlung in die gewünschte elektronische Datei eingehen. Standardwert ist **Keiner**.

- **Ja** - Finance oder Supply Chain Management senden eine JSON-Datei der Struktur **Rechnungsmodell** oder **Steuermodell** (für Brasilien), die im Modul **Elektronisches Reporting** definiert ist. Alle Elemente des Modells werden auf der Anwendungsseite mit Geschäftsdaten befüllt, unabhängig von der endgültigen Struktur der elektronischen Datei. Modelle enthalten in der Regel mehr Geschäftsdaten, als die Zieldateistruktur erfordert, und es kann mehr Zeit in Anspruch nehmen, diese Daten in der Anwendung zu generieren. Ein Wert von **Ja** für diese Option ist für das seltene Ereignis erforderlich, dass Sie in einer Funktion und Einrichtung der elektronischen Rechnungsstellung verschiedene Ausgabedateien erzeugen möchten. Ein Wert von **Ja** ist nützlich, wenn Sie Probleme mit Ihren Szenarien, der Struktur der elektronischen Dateien und der Vollständigkeit der Geschäftsdaten beheben möchten.
- **Nein** - Die Finanzabteilung oder das Supply Chain Management ruft den Dienst erstmals ohne Geschäftsdaten auf. Der Zweck dieses Aufrufs ist es, Informationen über die Konfiguration des elektronischen Berichtswesens (ER) zu erhalten, das für die Umwandlung elektronischer Dateien in der Pipeline verwendet wird. Diese Informationen werden an die Anwendung zurückgegeben, die damit die Teilmenge der Geschäftsdaten bestimmt, die in die JSON-Datei der Struktur **Rechnungsmodell** oder **Finanzmodell** (für Brasilien) aufgenommen werden soll. Ein Wert von **Nein** für diese Option trägt dazu bei, die Menge der Geschäftsdaten, die die Anwendung an den Dienst sendet, zu reduzieren, da die Anwendung nur die Geschäftsdaten senden kann, die für die erfolgreiche Erstellung einer elektronischen Datei erforderlich sind.

### <a name="validate-a-feature-setup"></a>Einrichtung einer Funktion validieren

Sie können eine Validierung ausführen, um die Konsistenz der gesamten Konfiguration zu überprüfen. Wenn z.B. ein obligatorischer Parameter für eine Aktion leer gelassen wurde, erkennt die Validierung diese Inkonsistenz und Sie erhalten eine Warnmeldung.

- Wählen Sie auf der Seite **Einrichtung der Versionsverwaltung** im Aktionsbereich **Validieren**.

## <a name="delete-a-feature-setup"></a>Löschen einer Einrichtung für eine Funktion

1. Wählen Sie auf der Seite **Elektronische Rechnungsstellung** eine Funktion für die elektronische Rechnungsstellung aus, die den Status **Entwurf** hat.
2. Auf der Registerkarte **Einrichtungen** wählen Sie **Löschen**.
3. Wählen Sie in der angezeigten Nachrichtenbox **Ja**, um zu bestätigen, dass Sie die Einrichtung der Funktion löschen möchten.
