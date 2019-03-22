---
title: Elektronisches Messaging
description: Dieses Thema enthält eine Übersicht und Einrichtungsinformationen für elektronisches Messaging in Microsoft Dynamics 365 for Finance and Operations.
author: ShylaThompson
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 5326642553c7efcebc6c6af953e2dafe9e62e9ec
ms.sourcegitcommit: f6fc90585632918d9357a384b27028f2aebe9b5a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/11/2019
ms.locfileid: "832194"
---
# <a name="electronic-messaging"></a>Elektronische Nachrichten

[!include [banner](../includes/banner.md)]

Dieses Thema enthält eine Übersicht und Einrichtungsinformationen für elektronisches Messaging in Microsoft Dynamics 365 for Finance and Operations.

Vor kurzem haben die Behörden und die gesetzgebenden Instanzen aus verschiedenen Ländern und Regionen der Welt Meldeanforderungen für Unternehmen implementiert, die in diesen Ländern oder Regionen registriert sind. Anhand dieser Anforderungen sollen Daten von diesen Unternehmen in elektronischem Format bezogen werden, direkt aus den Systemen, in denen sie kalkuliert, gespeichert und verarbeitet werden.

Die Funktionalität zum elektronischen Messaging in Finance and Operations unterstützt verschiedene Prozesse zum elektronischen dialogfähigen Betrieb zwischen Finance and Operations und den Systemen, die Regierungen und gesetzgebende Instanzen zur Berichterstellung, Übermittlung und dem Empfang von amtlichen Informationen anbieten.

Die Funktion zum elektronischen Messaging ist im Modul **Elektronische Berichterstellung** (EB) integriert. Daher können Sie EB-Formate für elektronische Nachrichten einrichten. Weitere Informationen finden Sie unter [Elektronische Berichterstellung (EB)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting).

Elektronisches Messaging basiert auf folgenden Entitäten:

- **Elektronische Nachricht** – Ein Bericht oder eine Meldung, die intern gemeldet und/oder gesendet werden sollte Ein Beispiel ist ein Bericht, der an eine Steuerbehörde gesendet wird.
- **Elektronische Nachrichtenelemente** – Datensätze, die in die Nachricht eingeschlossen werden sollen, die gemeldet wird.
- **Verarbeiten der elektronischen Nachricht** – Eine Kette von Aktivitäten, entweder verknüpft oder nicht verknüpft, die ausgeführt werden sollte, um die erforderlichen Daten zu sammeln, Berichte zu generieren, Daten in Microsoft Azure Blob Storage zu speichern, Berichte außerhalb des Systems zu übermitteln, Antworten von außerhalb des Systems abzurufen und die Datenbank anhand empfangener Informationen zu aktualisieren.

Die folgende Abbildung zeigt den Datenfluss für elektronisches Messaging an.

![Datenfluss des elektronischen Messaging](media/electronic-messaging-data-flow.png)

Die Funktion der elektronischen Messaging unterstützt die folgenden Szenarien:

- Manuelles Erstellen von Nachrichten und Generieren von Berichten, die auf zugeordneten EB-Formaten verschiedener Typen für das Exportieren basieren: Microsoft Excel, XML, JavaScript Object Notation (JSON), PDF, Text und Microsoft Word.
- Automatisches Erstellen und Verarbeiten von Nachrichten, die auf Informationen basieren, die von einer Behörde über ein zugeordnetes EB-Format für den Import angefordert und abgerufen wurden.
- Sammeln und Verarbeiten von Informationen aus Datenquellen (Finance and Operations-Tabelle) als Nachrichtenelemente.
- Zusätzliche Informationen speichern und verschiedene Werte auswerten, indem speziell definierte ausführbare Klassen in Relation zu Nachrichten und Nachrichtenelementen aufgerufen werden.
- Aggregieren von Informationen, die in Nachrichtenelementen gesammelt werden, Aufteilung dieser Informationen nach Nachricht und Generieren von Berichten, die in zugeordneten Export-EB-Formaten sind.
- Übermitteln von Berichten, die für einen Webdienst mithilfe von Sicherheitsinformationen generiert werden, die in Azure Key Vault gespeichert sind.
- Abrufen einer Antwort über einen Webdienst, Interpretieren der Antwort und Aktualisieren der Daten in Finance and Operations je nach Bedarf.
- Speichern und Überprüfen aller Berichte, die generiert werden.
- Speichern und Überprüfen aller Protokollinformationen, die Aktivitäten zugeordnet sind, die für die eine Nachricht oder ein Nachrichtenelement ausgeführt werden.
- Steuern der Verarbeitung durch verschiedene Nachrichtenstatus und Nachrichtenelementstatus.

## <a name="set-up-electronic-messaging"></a>Einrichten des elektronischen Messaging

Mithilfe des elektronischen Messaging können Sie verschiedene elektronische Berichterstellungsprozesse für verschiedene Dokumenttypen verwalten. In einigen komplexen Szenarien wird elektronisches Messaging eingerichtet, um eine Kombination vieler Nachrichtenstatus, Nachrichtenelementstatus, Aktivitäten, zusätzlicher Felder und ausführbarer Klassen zu haben. Für diese Szenarien sind Pakete von Datenentitäten für den Import verfügbar. Wenn Sie diese Datenentitätspakete verwenden, sollten Sie sie zu einer juristischen Person importieren, indem Sie das Datenverwaltungstool verwenden. Weitere Informationen dazu, wie das Datenverwaltungstool verwendet wird, finden Sie unter [Datenverwaltung](../../dev-itpro/data-entities/data-entities-data-packages.md).

Wenn Sie kein Datenentitätspaket importieren, kann die Funktionalität für elektronische Nachrichten manuell eingerichtet werden. In diesem Fall müssen Sie die folgenden Elemente einrichten: 

- [Nummernkreise](#number-sequences)
- [Nachrichtenelementtypen und -status](#message-item-types-and-statuses)
- [Nachrichtenstatus](#message-statuses)
- [Zusätzliche Felder](#additional-fields)
- [Ausführbare Klasseneinstellungen](#executable-class-settings)
- [Datensatzauffüllungsaktivitäten](#populate-records-actions)
- [Webanwendungen](#web-applications)
- [Webdiensteinstellungen](#web-service-settings)
- [Verarbeitungsaktivitäten für Nachrichten](#message-processing-actions)
- [Verarbeitung der elektronischen Nachricht](#electronic-message-processing)

Die folgenden Abschnitte enthalten mehr Informationen zu jedes dieser Elemente.

### <a name="number-sequences"></a>Nummernkreise

Richten Sie Nummernkreise sowohl für Nachrichten als auch Nachrichtenelemente ein. Mithilfe der Nummernkreise werden automatisch die Nachrichten und die Nachrichtenelemente nummeriert, und die Nummern, die zugewiesen werden, werden als eindeutige Bezeichner für die Nachrichten und Nachrichtenelemente im System verwendet. Sie können Nummernkreise für elektronisches Messaging auf der Seite **Hauptbuchparameter** (**Hauptbuch** \> **Sachkonto-Einrichtung** \> **Hauptbuchparameter**) einrichten.

### <a name="message-item-types-and-statuses"></a>Nachrichtenelementtypen und -status

Nachrichtenelementtypen identifizieren die Datensatztypen, die in den elektronischen Nachrichten verwendet werden. Sie können auf der Seite **Nachrichtenelementtypen** (**Steuer** \> **Einrichtung** \> **Elektronische Nachrichten** \> **Nachrichtenelementtypen**) Nachrichtenelementtypen einrichten.

Nachrichtenelementstatus identifizieren die Status, die für Nachrichtenelemente in der Verarbeitung gelten, die Sie gerade einrichten. Sie können auf der Seite **Nachrichtenelementstatus** (**Steuer** \> **Einrichtung** \> **Elektronische Nachrichten** \> **Nachrichtenelementstatus**) Nachrichtenelementtypen einrichten.

Der **Löschen zulassen**-Paramter eines Nachrichtenelementstatus definiert, ob der Benutzer ein Nachrichtenelement in diesem Status über ein Formular **Elektronische Nachrichten** oder ein Formular **Elektronische Nachrichtenelemente** löschen darf. 

### <a name="message-statuses"></a>Nachrichtenstatus

Richten Sie die Nachrichtenstatus ein, die bei der Nachrichtenverarbeitung verfügbar sein sollen. Sie können auf der Seite **Nachrichtenstatus** (**Steuer** \> **Einrichtung** \> **Elektronische Nachrichten** \> **Nachrichtenstatus**) Nachrichtenelementstatus einrichten.

Feldbeschreibungen:

| Feldname           | Beschreibung |
|----------------------|-------------|
|Nachrichtenstatus        | Eindeutiger Name eines Status der elektronischen Nachricht, der den Zustand einer Nachricht an jedem Zeitpunkt kennzeichnet. Dieser Name wird im Formular "Elektronische Nachrichten" und in einem Protokoll bezüglich elektronischer Nachrichten angezeigt. |
|Beschreibung           | Beschreibung zum Status der elektronischen Nachricht      |
|Antworttyp         | Einige Aktivitäten in einer Verarbeitung ergeben möglicherweise mehrere Antworttypen. Eine Aktion von Typ **Webdienst** ergibt möglicherweise entweder den Antworttyp **Erfolgreich ausgeführt** oder **Technischer Fehler**, je nach dem Ergebnis der Ausführung. In diesem Fall muss der Nachrichtenstatus für beide Antworttypen definiert werden. Weitere Informationen zu Aktivitätstypen und deren zugehörige Antworttypen finden Sie unter [Aktivitätstypen bei der Nachrichtenverarbeitung](#message-processing-action-types). |
|Nachrichtenelementstatus   |Es gibt Fälle, bei denen sich der Status der elektronischen Nachricht auf die Status der jeweiligen zugehörigen Nachrichtenelemente auswirken muss. Ordnen Sie solch einen Nachrichtenelementstatus in diesem Feld zu, indem Sie in der Auswahlliste auswählen. |
|Löschen zulassen          | Der **Löschen zulassen**-Paramter eines elektronischen Nachrichtenelementstatus definiert, ob der Benutzer ein elektronisches Nachrichtenelement in diesem Status über das Formular **Elektronische Nachrichten** löschen darf.            |

### <a name="additional-fields"></a>Zusätzliche Felder

Die Funktion für elektronische Nachrichten ermöglicht es Ihnen, Datensätze aus einer Transaktionstabelle aufzufüllen. Auf diese Weise können Sie die Datensätze für die Berichterstellung vorbereiten und diese anschließend melden. Manchmal gibt es nicht genügend Informationen in der Transaktionstabelle, um einen Datensatz gemäß den Berichtsanforderungen zu melden. Sie können alle Informationen eingeben, die für einen Datensatz gemeldet werden müssen, indem Sie zusätzliche Felder einrichten. Zusätzliche Felder können sowohl Nachrichten als auch Nachrichtenelementen zugeordnet werden. Sie können zusätzliche Felder auf der Seite **Zusätzliche Felder** "**Steuer** \> **Einrichtung** \> **Elektronische Nachrichten** \> **Zusätzliche Felder**) einrichten.

In der folgenden Tabelle werden die allgemeinen Felder auf der Seite **Zusätzliche Felder** beschrieben:

| Feld                | Beschreibung |
|----------------------|-------------|
| Feldname           | Geben Sie den Namen eines zusätzlichen Attributs von Nachrichtenelementen ein, die dem Prozess zugeordnet sind. Dieser Name wird auf der Benutzeroberfläche angezeigt, wenn sie mit dem Prozess arbeiten. Er kann auch in EB-Konfigurationen verwendet werden, die dem Prozess zugeordnet sind. |
| Beschreibung          | Geben Sie eine Beschreibung des zusätzlichen Attributs von Nachrichtenelementen ein, die dem Prozess zugeordnet sind. |
| Benutzerbearbeitung            | In einem Fall, wenn ein Benutzer in der Lage sein muss, den Wert des zusätzlichen Felds der Benutzeroberfläche zu ändern, legen Sie dieses Kontrollkästchen auf **Ja** fest, anderfalls auf **Nein**. |
| Zähler              | Wenn das zusätzliche Feld eine laufende Nummer innerhalb einer elektronischen Nachricht enthalten muss, aktivieren Sie dieses Kontrollkästchen. Werte des zusätzlichen Felds werden automatisch während der Ausführung einer Aktivität vom Typ "Elektronischer Berichtexport" ausgefüllt.  |
| Ausgeblendet               | Wenn das zusätzliche Feld aus der Benutzeroberfläche ausgeblendet werden muss, aktivieren Sie dieses Kontrollkästchen.  |

Jedes zusätzliche Feld verfügt über verschiedene Werte zur Bearbeitung. Sie können diese Werte im Inforregister "Werte" definieren:

| Feld                | Beschreibung |
|----------------------|-------------|
| Feldwert          | Geben Sie den Feldwert zur Verwendung in Bezug auf eine Nachricht oder ein Nachrichtenelement während der Berichterstellung ein. |
| Feldbeschreibung    | Geben Sie eine Beschreibung des Feldwerts zur Verwendung in Bezug auf eine Nachricht oder ein Nachrichtenelement während der Berichterstellung ein. |
| Kontenart         | Einige zusätzliche Feldwerte sind möglicherweise auf bestimmte Kontotypen beschränkt. Wählen Sie einen der folgenden Wert aus: **Alle**, **Kunde** oder **Lieferant**. |
| Kontocode         | Wenn Sie **Kunde** oder **Lieferant** im Feld **Kontotyp** ausgewählt haben, können Sie die Benutzung von Feldwertung weiter auf eine bestimmte Gruppe oder Tabelle einschränken. |
| Konto-/Gruppennummer | Wenn Sie **Kunde** oder **Lieferant** im Feld **Kontotyp** ausgewählt haben und wenn Sie eine Gruppe oder Tabelle im Feld **Kontocode** eingegeben haben, können Sie eine bestimmte Gruppe oder einen Counteragent in diesem Feld eingeben. |
| Gültig            | Geben Sie das Datum an, an dem die Berücksichtigung des Werts beginnen soll. |
| Ablauf           | Geben Sie das Datum an, an dem die Berücksichtigung des Werts beendet werden soll. |

Kombinationen aus den Kriterien, die in **Konto-/Gruppennummer**, **Kontocode**, **Gültig**, **Ablauf** definiert sind, wirken sich standardmäßig nicht auf die Auswahl des Werts für daszusätzliche Feld aus, können jedoch in der ausführbaren Klasse verwendet werden, um bei der Berechnung eines zusätzlichen Feldwerts eine gewisse Menge an bestimmter Logik zu implementieren.

### <a name="executable-class-settings"></a>Ausführbare Klasseneinstellungen

Eine ausführbare Klasse ist eine X++-Methode oder -Klasse, die die elektronische Nachrichtenverarbeitung in Bezug auf eine Aktivität aufrufen kann, wenn irgendeine Auswertung für den Prozess erforderlich ist.

Sie können eine ausführbare Klasse manuell auf der Seite **Ausführbare Klasseneinstellungen** (**Steuer** \> **Einrichtung** \> **Elektronische Nachrichten** \> **Ausführbare Klasseneinstellungen**) einrichten. Erstellen Sie eine Position und legen Sie die folgenden Felder fest.

| Feld                 | Beschreibung |
|-----------------------|-------------|
| Ausführbare Klasse      | Geben Sie den Namen ein, der bei der Einrichtung einer Nachrichtenverarbeitungsaktivität verwendet wird, in Bezug auf den diese Klasse aufgerufen wird. |
| Beschreibung           | Geben Sie eine Beschreibung der ausführbaren Klasse ein. |
| Ausführbarer Klassenname | Wählen Sie eine ausführbare X++-Klasse aus. |
| Ausführungsebene       | Dieses Feld wird automatisch festgelegt, da der Wert für die ausgewählte ausführbare Klasse vordefiniert werden sollte. Dieses Feld begrenzt die Ebene, auf der die Auswertung ausgeführt wird. |
| Klassenbeschreibung     | Dieses Feld wird automatisch festgelegt, da der Wert für die ausgewählte ausführbare Klasse vordefiniert werden sollte. |

Einige ausführbare Klassen besitzen möglicherweise obligatorische Parameter, die definiert werden müssen, bevor die ausführbare Klasse zum ersten Mal ausgeführt wird. Um derartige Parameter zu definieren, klicken Sie im Aktivitätsbereich auf die Schaltfläche **Parameter**, richten Sie die entsprechenden Werte und Felder im Dialogfenster ein und klicken Sie auf die Schaltfläche **OK**. Es ist wichtig, hier auf die Schaltfläche **OK** zu klicken, da die Parameter andernfalls nicht in der Basis gespeichert werden und die ausführbare Klasse nicht ordnungsgemäß aufgerufen wird.

### <a name="populate-records-actions"></a>Datensatzauffüllungsaktivitäten

Sie verwenden Aktivitäten zum Auffüllen von Datensätzen, um Aktivitäten einzurichten, durch die Datensätze zur Tabelle „Nachrichtenelemente” hinzugefügt werden, sodass sie einer elektronischen Nachricht hinzugefügt werden können. Wenn beispielsweise Ihre elektronische Nachricht Debitorenrechnungen melden muss, müssen Sie eine Aktivität **Datensätze auffüllen** einrichten, die mit der Tabelle **Debitorenrechnungserfassung** verknüpft ist (im Feld **Datenquelle** ). Sie können Aktivitäten zum Auffüllen von Datensätzen auf der Seite **Aktivität zum Auffüllen von Datensätzen** einrichten (**Steuer** \> **Einrichtung** \> **Elektronische Nachrichten** \> **Datensatzaktivitäten auffüllen**) einrichten. Erstellen Sie einen neuen Datensatz für jede Aktivität, durch die Datensätze der Tabelle hinzugefügt werden sollen, und legen Sie die folgenden Felder fest.

| Feld       | Beschreibung                                                               |
|-------------|---------------------------------------------------------------------------|
| Name        | Geben Sie einen Namen für die Aktivität ein, durch die Datensätze in Ihrem Prozess aufgefüllt werden.       |
| Beschreibung | Geben Sie eine Beschreibung der Aktivität ein, durch die Datensätze in Ihrem Prozess aufgefüllt werden. |

Fügen Sie im Inforegister **Datenquelleneinrichtung** eine Position für jede Datenquelle hinzu, die für den Prozess verwendet wird, und legen Sie die folgenden Felder fest.

| Feld                  | Beschreibung |
|------------------------|-------------|
| Name                   | Geben Sie einen Namen für die Datenquelle ein. |
| Nachrichtenelementtyp      | Wählen Sie den Typ des Nachrichtenelements aus, der verwendet werden soll, wenn Datensätze für die Datenquelle erstellt werden. |
| Kontenart           | Wählen Sie den Kontotyp aus, der den Datensätzen aus der Datenquelle zugeordnet werden soll. |
| Mastertabellenname      | Wählen Sie die Tabelle in Finance and Operations aus, die eine Datenquelle sein sollen. |
| Feld „Dokumentnummer”  | Wählen Sie das Feld aus, aus dem die Belegnummer in der ausgewählten Tabelle entnommen werden soll. |
| Feld „Dokumentdatum”    | Wählen Sie das Feld aus, aus dem das Belegdatum in der ausgewählten Tabelle entnommen werden soll. |
| Feld „Dokumentenkonto” | Wählen Sie das Feld aus, aus dem das Belegkonto in der ausgewählten Tabelle entnommen werden soll. |
| Benutzerabfrage             | Wenn dieses Kontrollkästchen aktiviert ist, können Sie eine Abfrage einrichten, indem Sie **Abfrage bearbeiten** über dem Raster auswählen. Andernfalls werden alle Datensätze aus der Datenquelle aufgefüllt. |

### <a name="web-applications"></a>Webanwendungen

Sie verwenden die Webanwendungsseite, um Parameter einer Webanwendung einzurichten, um den offenen OAuth 2.0-Standard zu unterstützen, mit dem Benutzer in ihrem Namen "Sicheren delegierten Zugriff" auf die Anwendung gewähren könen, ohne ihre Zugriffsanmeldeinformationen freizugeben zu müssen. Von dieser Seite aus können Sie auch den Autorisierungsprozess durchführen, indem Sie einen Autorisierungscode und ein Zugriffstoken abrufen. Sie können Webanwendungseinsteinstellungen auf der Seite **Webanwendungen** (**Steuer** \> **Einrichtung** \> **Elektronische Nachrichten** \> **Webanwendungen**) einrichten.

In der folgenden Tabelle werden die Felder auf der Seite **Webanwendungen** beschrieben.

| Feld                         | Beschreibung |
|-------------------------------|-------------|
| Anwendungsname              | Geben Sie einen Namen für den Webanwendung ein. |
| Beschreibung                   | Geben Sie eine Beschreibung des Webanwendung ein. |
| Basis-URL                      | Geben Sie die Basis-Internetadresse der Webanwendung ein. |
| Autorisierungs-URL-Pfad        | Geben Sie den Pfad ein, um die URL für die Autorisierung zu verfassen.  |
| Token-URL-Pfad                | Geben Sie den Pfad ein, um die URL für das Token zu verfassen.  |
| Umleitungs-URL                  | Umleitungs-URL eingeben.  |
| Clientkennung                     | Geben Sie die Client-ID der Webanwendung ein.  |
| Geheimer Clientschlüssel                 | Geben Sie den geheimen Clientschlüssel der Webanwendung ein.  |
| Servertoken                  | Geben Sie das Server-Token der Webanwendung ein.  |
| Autorisierungsformatzuordnung  | Wählen Sie ein elektronisches Berichtsformat aus, das verwendet wird, um Authorisierungsanforderung zu generieren.   |
| Importtoken-Modellzuordnung    | Wählen Sie eine ER-Importmodellzuordnung aus, mit der Zugriffstoken gespeichert werden.  |
| Bewilligter Bereich      Zugriffstoken läuft ab in  | Dieses Feld wird automatisch aktualisiert. Sein Wert zeigt den bewilligten Bereich der Anforderungen an die Webanwendung.  |
| Übernehmen                        | Geben Sie die Annahmeeigenschaft der Webanforderung an. Beispielsweise "application/vnd.hmrc.1.0+json".  |
| Inhaltstyp           | Inhaltstyp angeben. Beispielsweise "application/json".  |

Die folgenden Funktionen sind von der **Webanwendungen**-Seite verfügbar, um den Autorisierungsprozess zu unterstützen:
-   **Autorisierungscode abrufen** -, um die Autorisierung Webanwendung zu initialisieren.
-   **Zugriffstoken abrufen** -, um den Abruf von Zugriffstoken zu initialisieren.
-   **Zugriffstoken aktualisieren** -, um einen Zugriffstoken zu aktualisieren.

Wenn ein Zugriffstoken einer Webanwendung, die in der Datenbank des Systems in verschlüsseltem Format gespeichert ist, kann es für Anforderungen an einen Webdienst verwendet werden. Aus Sicherheitsgründen muss der Zugriff auf das Zugriffstoken nur auf die Sicherheitsrollen begrenzt werden, die derartige Anforderungen stellen können müssen. Wenn ein Benutzer außerhalb der Sicherheitsgruppe eine eine Anforderung zu erteilen versucht, wird der Benutzer über eine Ausnahme darüber informiert, dass er (sie) nicht über die ausgewählte Webanwendung. zusammenarbeiten darf.
Verwenden Sie die Tabelle **Sicherheitsrollen** der Seite "Steuer > Einrichtung > Elektronische Nachrichrten > Webanwendungen", um von Rollen einzurichten, die über Zugriff auf Zugriffstoken verfügen müssen. Wenn keine Sicherheitsrollen für eine Webanwendung definiert sind, steht ein Systemadministrator nur über die Webanwendung zusammenzuwirken.

### <a name="web-service-settings"></a>Webdiensteinstellungen

Sie verwenden Webdiensteinstellungen, um direkte Datenübermittlung zu einem Webdienst einzurichten. Sie können Webdiensteinstellungen auf der Seite **Webdiensteinstellungen** (**Steuer** \> **Einrichtung** \> **Elektronische Nachrichten** \> **Webdiensteinstellungen**) einrichten.

In der folgenden Tabelle werden die Felder auf der Seite **Webdiensteinstellungen** beschrieben.

| Feld                   | Beschreibung |
|-------------------------|-------------|
| Webdienst             | Geben Sie einen Namen für den Webdienst ein. |
| Beschreibung             | Geben Sie eine Beschreibung des Webdiensts ein. |
| Internetadresse        | Geben Sie die Internetadresse des Webdiensts ein. Wenn eine Webanwendung für einen Webdienst angegeben ist, sollte die Internetadresse mit der für die ausgewählte Webanwendung übereinstimmen. Klicken Sie die Schaltfläche **Basis-URL kopieren**, um die **Basis-URL** aus der Webanwendung in das Feld **Internetadresse**des Webdiensts zu kopieren.  |
| Bescheinigung             | Wählen Sie ein Key Vault-Zertifikat aus, das zuvor eingerichtet wurde. |
| Webanwendung         | Wählen Sie ein Key Vault-Zertifikat aus, das zuvor eingerichtet wurde. |
| Der Antworttyp – XML | Legen Sie diese Option auf **Ja** fest, wenn der Antworttyp XML ist. |
| Anforderungsmethode          | Geben Sie die Methode der Anforderung an. HTTP definiert eine Gruppe von Anforderungsmethoden, die die Aktivität angeben, die für eine bestimmte Ressource ausgeführt werden soll. Die Methode kann **GET**, **POST** oder eine andere HTTP-Methode sein. |
| Anforderungskopfzeile         | Geben Sie Anforderungskopfzeilen an. Eine Anforderungskopfzeile ist eine HTTP-Kopfzeile, die in einer HTTP-Anforderung verwendet werden kann und die nicht dem Inhalt der Nachricht zugeordnet ist. |
| Übernehmen                  | Geben Sie die Annahmeeigenschaft der Webanforderung an. |
| Codierung akzeptieren         | Geben Sie die Accept-Codierung an. Die HTTP-Kopfzeile der Accept-Codierungsanforderung kündigt die Inhaltscodierung an, die der Client verstehen kann. Diese Inhaltscodierung ist normalerweise ein Komprimierungsalgorithmus. |
| Inhaltstyp            | Geben Sie den Inhaltstyp an. Die Entitätskopfzeile „Inhaltstyp” gibt den Medientyp der Ressource an. |
| Code für erfolgreiche Antwort   | Geben Sie den HTTP-Statuscode an, der angibt, dass die Anforderung erfolgreich war. |
| Anforderungskopfzeilen-Formatzuordnung  | Wählen Sie das ER-Format zur Generierung von Webanforderungsheadern aus. |

### <a name="message-processing-actions"></a>Verarbeitungsaktivitäten für Nachrichten

Mithilfe von Nachrichtenverarbeitungsaktivitäten erstellen Sie Aktivitäten für Ihre Prozesse und richten deren Parameter ein. Sie können Nachrichtenverarbeitungsaktivitäten auf der Seite **Nachrichtenverarbeitungsaktivitäten** (**Steuer** \> **Einrichtung** \> **Elektronische Nachrichten** \> **Nachrichtenverarbeitungsaktivitäten**) einrichten.

In den folgenden Tabellen werden die Felder auf der Seite **Nachrichtenverarbeitungsaktivitäten** beschrieben.

#### <a name="general-fasttab"></a>Allgemeines Inforegister

| Feld                   | Beschreibung |
|-------------------------|-------------|
| Vorgangstyp             | Wählen Sie den Typ der Aktivität aus. Informationen zu den verfügbaren Optionen finden Sie im Abschnitt [Nachrichtenverarbeitungsaktivitäts-Typen](#message-processing-action-types). |
| Formularzuordnung          | Wählen Sie das EB-Format aus, das für die Aktivität aufgerufen werden soll. Dieses Feld ist nur für Aktivitäten der Typen **Elektronischer Berichterstellungsexport**, **Elektronischer Berichterstellungsimport** und **Elektronische Berichterstellungsexportnachricht** verfügbar. |
| Formatzuordnung für URL-Pfad | Wählen Sie das EB-Format aus, das für die Aktivität aufgerufen werden soll. Dieses Feld ist nur für die Aktivitäten des Typs **Webdienst** verfügbar und wird verwendet, um den Pfad der URL-Adresse zu verfassen, die der Basisinternetadresse hinzugefügt wird, die für den ausgewählten Webserver angegeben wird. |
| Nachrichtenelementtyp       | Wählen Sie den Typ von Datensätzen aus, für den die Aktivität ausgewertet werden soll. Dieses Feld ist für Aktivitäten der Typen **Nachrichtenelement-Ausführungsebene**, **Elektronischer Berichterstellungsexport**, **Elektronischer Berichterstellungsimport** und **Webanwendung** verfügbar sowie für einige andere Typen. Wenn Sie dieses Feld leer lassen, werden alle Nachrichtenelementtypen, die für die Nachrichtenverarbeitung definiert sind, ausgewertet. |
| Ausführbare Klasse        | Wählen Sie die Einstellungen ausführbarer Klassen aus, die zuvor erstellt wurden. Dieses Feld ist nur für Aktivitäten der Typen **Nachrichtenelement-Ausführungsebene** und **Nachrichtenelementausführungsebene** verfügbar. |
| Datensatzauffüllungsaktivität | Wählen Sie eine Aktivität zum Auffüllen von Datensätzen aus, die zuvor eingerichtet wurde. Dieses Feld ist nur für Aktivitäten vom Typ **Datensätze auffüllen** verfügbar. |
| Webdienst  | Wählen Sie einen Webdienst aus, der zuvor eingerichtet wurde. Dieses Feld ist nur für Aktivitäten vom Typ **Webdienst** verfügbar.  |
| Dateiname  | Geben Sie den Namen der Datei an, die die Aktivität als Antwort vom Webserver oder der Generierung eines Berichts ergibt. Dieses Feld ist nur für Aktivitäten vom Typ **Webdienst** und **Elektronische Berichterstellungsexportnachricht** verfügbar.   |
| Dialog anzeigen  | Aktivieren Sie dieses Kontrollkästchen, wenn einen Benutzer vor der Berichtserstellung ein Dialogfeld angezeigt werden muss. Dieses Feld ist nur für Aktivitäten vom Typ **Elektronische Berichterstellungsexportnachricht** verfügbar.   |

##### <a name="message-processing-action-types"></a>Nachrichtenverarbeitungsaktivitäts-Typen

Die folgenden Optionen sind im Feld **Aktivitätstypen** verfügbar:

- **Nachricht erstellen** – Dieser Typ wird verwendet, damit Benutzer Nachrichten auf der Seite **Elektronische Nachricht** manuell erstellen können. Ein Anfangsstatus für eine Aktivität dieses Typs kann nicht eingerichtet werden.
- **Datensätze auffüllen** – Eine Aktivität **Datensätze auffüllen** muss zuvor eingerichtet werden. Ordnen Sie sie einer Aktivität des Typs **Datensätze auffüllen** zu, um sie dafür zu aktivieren, in die Verarbeitung einbezogen zu werden. Es wird angenommen, dass dieser Aktivitätstyp entweder für die erste Aktivität in der Nachrichtenverarbeitung verwendet wird (wenn keine elektronische Nachricht im Voraus erstellt wird) oder als eine Aktivität, die Nachrichtenelemente einer zuvor erstellten Nachricht hinzufügt (durch eine Aktivität von Typ **Nachricht erstellen** ). Daher kann der Ergebnisstatus nur eines Nachrichtenelements für eine Aktivität dieses Typs eingerichtet werden. Ein Anfangsstatus kann nur für Nachrichten eingerichtet werden.
- **Nachrichtenausführungsebene** – Dieser Typ wird verwendet, um eine ausführbare Klasse einzurichten, die auf der Nachrichtenebene ausgewertet werden soll.
- **Nachrichtenelement-Ausführungsebene** – Dieser Typ wird verwendet, um eine ausführbare Klasse einzurichten, die auf der Nachrichtenelementebene ausgewertet werden soll.
- **Elektronischer Berichterstellungsexport** – Verwenden Sie diesen Typ für Aktivitäten, die einen Bericht generieren sollen, der auf einer Export-EB-Konfiguration auf der Nachrichtenelementebene basiert.
- **Elektronischer Berichterstellungsexport-Nachricht** – Verwenden Sie diesen Typ für Aktivitäten, die einen Bericht generieren sollen, der auf einer Export-EB-Konfiguration auf der Nachrichtenebene basiert (beispielsweise wenn eine Nachricht keine Nachrichtenelemente hat).
- **Elektronischer Berichterstellungsimport** – Verwenden Sie diesen Typ für Aktivitäten, die einen Bericht generieren sollen, der auf einer Import-EB-Konfiguration basiert.
- **Benutzerverarbeitung auf Nachrichtenebene** – Verwenden Sie diesen Typ für Aktivitäten, bei denen von einigen manuellen Aktivitäten durch den Benutzer ausgegangen wird. Beispielsweise aktualisiert der Benutzer unter Umständen den Status von Nachrichten.
- **Benutzerverarbeitung** – Verwenden Sie diesen Typ für Aktivitäten, bei denen von irgendeiner manuellen Aktivität durch den Benutzer ausgegangen wird. Beispielsweise aktualisiert der Benutzer unter Umständen den Status von Nachrichtenelementen.
- **Webdienst** – Verwenden Sie diesen Typ für Aktivitäten, durch die ein generierter Bericht zu einem Webdienst übertragen werden sollen. Dieser Aktivitätstyp wird nicht für die Berichterstellung für „Italienischer Einkauf” und „Verkaufsrechnungskommunikation” verwendet. Bei Aktivitäten vom Typ **Webdienst** können Sie einen **Bestätigungstext** im Inforregister **Sonstige Details** der **Verarbeitungsaktivitäten für Nachrichten** angeben. Dieser Bestätigungstext wird dem Benutzer angezeigt, bevor die Anforderung zum ausgewählten Webdienst behandelt wird.
- **Überprüfung anfordern** – Dieser Typ wird verwendet, um die Überprüfung von einem Server anzufordern.

#### <a name="initial-statuses-fasttab"></a>Anfangsstatus-Inforegister

> [!NOTE]
> Das Inforegister **Anfangsstatus** ist nicht für Aktivitäten mit dem Anfangstyp **Datensätze erstellen** verfügbar.

| Feld               | Beschreibung                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------|
| Nachrichtenelementstatus | Wählen Sie den Nachrichtenelementstatus aus, für den die ausgewählte Nachrichtenverarbeitungsaktivität ausgewertet werden soll. |
| Beschreibung         | Eine Beschreibung des ausgewählten Nachrichtenelementstatus.                                                  |

#### <a name="result-statuses-fasttab"></a>Ergebnisstatus-Inforegister

| Feld               | Beschreibung |
|---------------------|-------------|
| Nachrichtenstatus      | Wählen Sie die Nachrichtenstatus aus, für den die ausgewählte Nachrichtenverarbeitungsaktivität ausgewertet werden soll. Dieses Feld ist nur für Nachrichtenverarbeitungsaktivitäten verfügbar, die auf Nachrichtenebene ausgewertet werden. Beispielsweise ist es für Aktivitäten der Typen **Elektronischer Berichterstellungsexport** und **Elektronischer Berichterstellungsimport** verfügbar. Es ist nicht für Aktivitäten der Typen **Benutzerverarbeitung** und **Nachrichtenelement-Ausführungsebene** verfügbar. |
| Beschreibung         | Eine Beschreibung des ausgewählten Nachrichtenstatus. |
| Antworttyp       | Der Antworttyp des ausgewählten Nachrichtenstatus. |
| Nachrichtenelementstatus | Wählen Sie die resultierenden Status aus, die verfügbar sein sollten, nachdem die ausgewählte Nachrichtenverarbeitungsaktivität ausgewertet ist. Dieses Feld ist nur für Nachrichtenverarbeitungsaktivitäten verfügbar, die auf Nachrichtenelementebene ausgewertet werden. Beispielsweise ist es für Aktivitäten der Typen **Benutzerverarbeitung** und **Nachrichtenelement-Ausführungsebene** verfügbar. Für Nachrichtenverarbeitungsaktivitäten, die auf Nachrichtenebene ausgewertet werden, zeigt dieses Feld den Nachrichtenelementstatus an, der für den ausgewählten Nachrichtenstatus eingerichtet wurde. |

Die folgende Tabelle veranschaulicht, welche Ergebnisstatus hinsichtlich der Aktivitätstypen eingerichtet werden müssen:

| Aktionstyp/Antworttyp der elektronischen Nachricht  | Erfolgreich ausgeführt  | Geschäftsfehler  | Technischer Fehler  | Von Benutzer definiert  | Stornieren  |
|-------------------------------------------------|--------------|---------|-------|-----|-----------------|
| Nachricht erstellen                                  | X            |         |       |     |                 |
| Elektronischer Berichtexport                     | X            |         |       |     |                 |
| Elektronischer Berichtimport                     |              |         |       |     |                 |
| Webdienst                                     | X            |         | X     |     |                 |
| Benutzerverarbeitung                                 |              |         |       |     |                 |
| Nachrichtenausführungsebene                         |              |         |       |     |                 |
| Datensätze auffüllen                                |              |         |       |     |                 |
| Nachrichtenelement-Ausführungsebene                    |              |         |       |     |                 |
| Überprüfung anfordern                            | X            |  X      | X     |     |                 |
| Nachricht zum elektronischen Berichtexport             | X            |         |       |     |                 |
| Benutzerverarbeitung auf Nachrichtenebene                   |              |         |       |     |                 |

### <a name="electronic-message-processing"></a>Verarbeitung der elektronischen Nachricht

Elektronische Nachrichtenverarbeitung ist ein Grundprinzip der elektronischen Nachrichtenfunktion. Dadurch werden Aktivitäten aggregiert, die für die elektronische Nachricht ausgewertet sollen. Die Aktivitäten können über einen Anfangsstatus und einen Ergebnisstatus verknüpft werden. Alternativ können Aktivitäten des Typs **Benutzerverarbeitung** unabhängig gestartet werden. Auf der Seite **Elektronische Nachrichtenverarbeitung** (**Steuer** \> **Einrichtung** \> **Elektronische Nachrichten** \> **Elektronische Nachrichtenverarbeitung**) können Sie auch zusätzliche Felder auswählen, die für die Verarbeitung auf Nachrichtenebene oder Nachrichtenelementebene unterstützt werden sollen.

Mithilfe des Inforegisters **Aktivität** können Sie der Verarbeitung vordefinierte Aktivitäten hinzufügen. Sie können angeben, ob eine Aktivität gesondert ausgeführt werden muss oder ob sie durch die Verarbeitung initiiert werden kann. Um zu definieren, ob die Aktivität nur von einem Benutzer initialisiert werden kann, aktivieren Sie bei der Verarbeitung das Kontrollkästchen **Separat ausführen** für die Aktivität. Haben Sie die Markierung des **Separat ausführen**-Parameters auf, wenn die Aktivität von der Verarbeitung gestartet werden soll, wenn sich Nachrichten oder Nachrichtenelemente im als Anfängsstatus für diese Aktivität definierten Status befinden. Eine Aktivität des Typs **Benutzeraktivität** darf nur separat ausgeführt werden. 

Manchmal kann sie benötigt werden, um mehrere Aktivitäten in einen Nummernkreis zu aggregieren, wenn das erste Element so definiert wurde, dass es separat ausgeführt werden soll. Beispiel: wenn die Berichtserstellung von einem Benutzer initialisiert werden muss, aber ein generierten Bericht sofort an einem Webdienst gesendet und die Antwort vom Webdienst im System hinterlegt werden muss. In solchen Fällen können Sie **Untrennbarer Nummernkreis** verwenden. Klicken Sie dazu im Aktivitätsbereich des Inforregisters **Aktivität** auf der Seite **Verarbeitung der elektronischen Nachricht** auf die Schaltfläche **Untrennbarer Nummernkreis**. Erstellen Sie einen Nummernkreis und wählen Sie ihn in der Spalte für **Untrennbarer Nummernkreis** für die Aktivitäten aus, die immer zusammen ausgeführt werden müssen. Die erste Aktivität kann in diesem Fall als **Separat ausführen** eingerichtet werden, alle anderen jedoch nicht.

Mithilfe des Inforegisters **Zusätzliche Felder des Nachrichtenelements** können Sie vordefinierte zusätzliche Felder hinzufügen, die Nachrichtenelementen zugeordnet sind. Sie müssen zusätzliche Felder für jeden Typ von Nachrichtenelement hinzufügen, dem die Felder zugeordnet sind.

Mithilfe des Inforegisters **Zusätzliche Felder des Nachrichtenelements** können Sie vordefinierte zusätzliche Felder hinzufügen, die Nachrichten zugeordnet sind.

Mithile des Inforegisters **Sicherheitsrollen** können Sie Sicherheitsrollen einrichten, die im System zur speziellen Verarbeitung vordefiniert sind. Benutzer, die eine bestimmte Rolle besitzen, sehen nur Verarbeitung, die für diese Rolle definiert ist.

Mithilfe des Inforegisters **Charge** können Sie festlegen, dass Verarbeitung in einem Chargensystem funktioniert.

## <a name="work-with-electronic-messages-functionality"></a>Arbeit mit Funktionen der elektronischen Nachrichten

Wenn Sie auf der Nachrichtenebene arbeiten, ist die Seite **Elektronische Nachrichten** (**Steuer** \> **Abfragen und Berichte** \> **Elektronische Nachrichten** \> **Elektronische Nachrichten**) nützlicher. Wenn Sie auf der Datensammlungs-(Nachrichtenelement)-Ebene arbeiten, ist die Seite **Elektronische Nachrichtenelemente** (**Steuer** \> **Abfragen und Berichte** \> **Elektronische Nachrichten** \> **Elektronische Nachrichtenelemente**) nützlicher.

### <a name="electronic-messages"></a>Elektronische Nachrichten

Die Seite **Elektronische Nachrichten** zeigt die Verarbeitung an, die für Sie verfügbar ist, basierend auf Ihrer Rolle. Sicherheitsrollen werden mit der Verarbeitung in den Einstellungen dieser Verarbeitung zugeordnet. Für jede Verarbeitung, die für Sie verfügbar ist, zeigt die Seite elektronische Nachrichten sowie Informationen an, die ihnen zugeordnet ist.

Das Inforegister **Nachrichten** zeigt elektronische Nachrichten für die ausgewählte Verarbeitung an. Abhängig vom Status der ausgewählten Nachricht und der vordefinierten Verarbeitung, können Sie einige Aktivitäten ausführen, indem Sie die Schaltflächen über dem Raster auswählen:

- **Neu** – Diese Schaltfläche ist Aktivitäten vom Typ **Nachricht erstellen** zugeordnet.
- **Löschen** – Diese Schaltfläche ist verfügbar, wenn das Kontrollkästchen **Löschen ermöglichen** für den aktuellen Status der ausgewählten Nachricht aktiviert ist.
- **Daten erfassen** - Diese Schaltfläche wird Aktivitäten des Typs **Datensätze auffüllen** zugeordnet.
- **Bericht generieren** – Diese Schaltfläche ist Aktivitäten vom Typ **Elektronische Berichterstellungsexportnachricht** zugeordnet.
- **Bericht senden** – Diese Schaltfläche ist Aktivitäten vom Typ **Webdienst** zugeordnet.
- **Antwort generieren** – Diese Schaltfläche ist Aktivitäten vom Typ **Elektronischer Berichtimport** zugeordnet.
- **Status aktualisieren** – Diese Schaltfläche ist Aktivitäten vom Typ **Nachrichtenebenen-Benutzerverarbeitung** zugeordnet.
- **Nachrichtenelemente** – Öffnet die Seite **Elektronische Nachrichtenelemente**.

Das Inforegister **Aktivitätsprotokoll** zeigt Informationen zu allen Aktivitäten an, die für die ausgewählte Nachricht ausgeführt wurden. Wenn eine Aktivität zu einem Fehler geführt hat, werden Informationen zu dem Fehler an der entsprechenden Aktivitätsprotokollposition angefügt. Wählen Sie die Position aus, und klicken auf die Schaltfläche **Anfügen** in der oberen rechten Ecke der Seite, um die Informationen zu dem Fehler zu überprüfen.

Das Inforegister **Zusätzliche Felder der Nachricht** zeigt alle zusätzlichen Felder an, die für Nachrichten in den Verarbeitungseinstellungen definiert sind. Außerdem zeigt es die Werte dieser zusätzlichen Felder an.

Das Inforegister **Nachrichtenelemente** zeigt alle Nachrichtenelemente an, die der ausgewählten Nachricht zugeordnet sind. Für jedes der folgenden Nachrichtenelemente kann "fynction" abhängig vom Status dieses Nachrichtenelements verwendet werden:

- **Löschen** – Diese Schaltfläche ist verfügbar, wenn das Kontrollkästchen **Löschen ermöglichen** für den aktuellen Status des ausgewählten Nachrichtelements aktiviert ist.
- **Status aktualisieren** – Diese Schaltfläche ist Aktivitäten vom Typ **Benutzerverarbeitung** zugeordnet.
- **Originaldokument** - Diese Schaltfläche ermöglicht es einem Benutzer, eine Seite mit dem Originaldokument der ausgewählten Nachricht zu öffnen.

Sie können alle Anhänge für die ausgewählte Nachricht prüfen. Diese Anhänge sind Berichte, die bereits generiert und empfangen wurden. Wählen Sie die Nachricht aus, für die Anhänge überprüft werden sollen, und wählen Sie dann die Schaltfläche **Anhang** im Aktionsbereich aus.

![Schaltfläche „Anhang”](media/attachment-icon.png)

Die Seite **Anhänge** zeigt alle Anhänge an, die dieser Nachricht zugeordnet sind. Um eine Datei anzuzeigen, wählen Sie diese in der Liste auf der linken Seite aus, und wählen Sie anschließend **Öffnen** im Aktionsbereich aus.

![Schaltfläche „Öffnen”](media/open-button.png)

Wenn Sie einen Anhang überprüfen möchten, der einer bestimmten Aktivität zugeordnet ist, die zuvor für eine Nachricht ausgeführt wurde, wählen Sie die Nachricht auf der Seite **Elektronische Nachrichten** aus, und wählen Sie dann auf der Registerkarte **Aktivitätsprotokoll** die Aktivität aus. Wählen Sie dann die Schaltfläche **Anhang** im Aktionsbereich aus.

Sie können auch entweder die gesamte Verarbeitung oder nur eine bestimmte Aktivität ausführen, indem Sie **Verarbeitung ausführen** auswählen.

### <a name="electronic-message-items"></a>Elektronische Nachrichtenelemente

Die Seite **Elektronische Nachrichtenelemente** zeigt alle Nachrichtenelemente und ein Protokoll der Aktivitäten an, die für jedes Nachrichtenelement ausgeführt wurden. Sie zeigt auch die zusätzlichen Felder, die für die Nachrichtenelemente definiert sind sowie die Werte dieser zusätzlichen Felder.

In der folgenden Tabelle werden die Felder auf der Registerkarte **Nachrichtenelemente** beschrieben.

<table>
<thead>
<tr>
<th>Feld</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr>
<td>Bearbeitung</td>
<td>Der Name der Verarbeitung, die zum Erstellen des Nachrichtenelements verwendet wurde.</td>
</tr>
<tr>
<td>Nachrichtenelement</td>
<td>Die Kennung des Nachrichtenelements. Diese Kennung wird automatisch zugewiesen, basierend auf dem Nummernkreis <strong>Nachrichtenelement</strong>, der auf der Seite <strong>Hauptbuchparameter</strong> definiert ist.</td>
</tr>
<tr>
<td>Nachrichtenelementdatum</td>
<td>Das Datum, an dem das Nachrichtenelement erstellt wurde.</td>
</tr>
<tr>
<td>Nachrichtenelementtyp</td>
<td>Der Typ des Nachrichtenelements. Mehrere Typen von Nachrichtenelementen können für dieselbe Verarbeitung eingerichtet werden (beispielsweise <strong>Eingehende Rechnungen</strong> und <strong>Ausgehende Rechnungen</strong>). Dieses Feld kann nur automatisch ausgefüllt werden, wenn eine Rechnung der Tabelle „Nachrichtenelemente” hinzugefügt wurde.</td>
</tr>
<tr>
<td>Nachrichtenelementstatus</td>
<td>Der tatsächliche Status des Nachrichtenelements. Die verfügbaren Status variieren, abhängig vom Typ des Nachrichtenelements. Nachfolgend finden Sie einige Beispiele:
<ul>
<li><strong>Aufgefüllt</strong> – Ein Datensatz wurde der Tabelle „Nachrichtenelemente” hinzugefügt.</li>
<li><strong>Ausgewertet</strong> – Zusätzliche Attribute wurden für das Nachrichtenelement berechnet.</li>
<li><strong>Berichtet</strong> – Das Nachrichtenelement wurde erfolgreich zu einem Bericht hinzugefügt.</li>
<li><strong>Ausgeschlossen</strong> – Dieser Status kann nützlich sein, wenn Sie einige Nachrichtenelemente aus einem Bericht ausschließen müssen, bevor er exportiert wird.</li>
</ul>
</td>
</tr>
<tr>
<td>Übermittlungsdatum</td>
<td>Zur Verarbeitung, die automatisch einen generierten Bericht außerhalb des Systems übermittelt, das Datum, an dem das Nachrichtenelement übermittelt wurde.</td>
</tr>
<tr>
<td>Dokumentnummer</td>
<td>Dieses Feld wird basierend auf den Einstellungen der Aktivität zum Auffüllen von Datensätzen automatisch ausgefüllt. Dieses Feld kann nur automatisch ausgefüllt werden, wenn eine Rechnung der Tabelle „Nachrichtenelemente” hinzugefügt wurde.</td>
</tr>
<tr>
<td>Kontonummer</td>
<td>Die Kontonummer eines Kunden oder Lieferanten (oder ein anderer Feldwert, abhängig vom Feld, das bei der Aktivität <strong>Datensätze auffüllen</strong> definiert ist). Dieses Feld kann nur automatisch ausgefüllt werden, wenn eine Rechnung der Tabelle „Nachrichtenelemente” hinzugefügt wurde.</td>
</tr>
<tr>
<td>Nachricht</td>
<td>Die Nummer der Nachricht. Diese Zahl wird automatisch zugewiesen, basierend auf dem Nummernkreis <strong>Nachricht</strong>, der auf der Seite <strong>Hauptbuchparameter</strong> definiert ist.</td>
</tr>
<tr>
<td>Nachrichtenstatus</td>
<td>Der tatsächliche Status der elektronischen Nachricht.</td>
</tr>
<tr>
<td>Nächste Aktivität</td>
<td>Die nächsten Aktivitäten, die für den aktuellen Status des Nachrichtenelements initiiert werden können.</td>
</tr>
</tbody>
</table>

Die Registerkarte **Zusätzliche Felder** zeigt die zusätzlichen Felder für das ausgewählte Nachrichtenelement und deren Werte an.

#### <a name="run-processing"></a>Verarbeitung ausführen

Wählen Sie im Aktionsbereich **Verarbeitung ausführen** aus, um die Verarbeitung für Nachrichtenelemente auszuführen. Um eine bestimmte Aktivität im Dialogfeld **Verarbeitung ausführen** auszuführen, legen Sie die Option **Aktivität auswählen** auf **Ja** fest, und wählen Sie dann eine Aktivität aus. Um die gesamte Verarbeitung auszuführen, belassen Sie die Option **Aktivität auswählen** auf **Nein** festgelegt.

#### <a name="generate-report"></a>Bericht generieren

Wählen Sie im Aktionsbereich **Bericht generieren** aus, um einen Bericht zu generieren. Diese Schaltfläche ist Aktivitäten vom Typ **Elektronischer Berichterstellungsexport** zugeordnet.

#### <a name="update-status"></a>Status aktualisieren

Wählen Sie im Aktivitätsbereich **Status aktualisieren** aus, um den Status einer oder mehrerer Nachrichtenelemente zu aktualisieren. Im Dialogfeld **Status aktualisieren** verwenden Sie das Inforegister **Einzuschließende Datensätze**, um Nachrichtenelemente für die Aktualisierung auszuwählen. Stellen Sie sicher, dass Sie die Auswahlkriterien richtig definieren, da Nachrichtenelementstatus gemäß dieser Kriterien, dem Anfangsstatus der ausgewählten Aktivität und dem Wert **Neuer Status**, den Sie festlegen, aktualisiert werden. Nachdem eine Statusaktualisierung abgeschlossen ist, wird es schwierig zu bestimmen, welche Elemente soeben aktualisiert wurden. Daher wird es schwierig sein, ein Rollback für Statusupdates auszuführen.

#### <a name="electronic-messages"></a>Elektronische Nachrichten

Wählen Sie im Aktionsbereich **Elektronische Nachricht** aus, um eine elektronische Nachricht zu prüfen, die dem ausgewählten Nachrichtenelement zugeordnet ist.

Sie können auch alle Dateien prüfen, die dem Nachrichtenelement entsprechen. Wählen Sie das Feld **Nachricht** des Nachrichtenelements aus, oder wählen Sie **Elektronische Nachricht** im Aktionsbereich aus. Wählen Sie auf der Seite **Elektronische Nachricht** die Nachricht aus, für die ein Bericht geprüft werden soll, und wählen Sie dann die Schaltfläche **Anhang** im Aktionsbereich aus.

![Schaltfläche „Anhang”](media/attachment-icon.png)

Die Seite **Anhänge** zeigt alle Anhänge an, die dieser Nachricht zugeordnet sind. Um eine Datei anzuzeigen, wählen Sie diese in der Liste auf der linken Seite aus, und wählen Sie anschließend **Öffnen** im Aktionsbereich aus.

![Schaltfläche „Öffnen”](media/open-button.png)

#### <a name="original-document"></a>Originaldokument

Wählen Sie im Aktionsbereich **Originaldokument** aus, um das Originaldokument für das ausgewählte Nachrichtenelement zu öffnen.

## <a name="example"></a>Beispiel

Nachdem Sie Ihr EB-Format erstellt haben, es Datenquellen zugeordnet haben und ihn abgeschlossen haben, können Sie es mithilfe des Arbeitsbereichs **Elektronische Berichterstellung** ausführen. Ein Bericht wird generiert, den Sie lokal speichern können.

Um die folgenden Aspekte des Berichterstellungsprozesses zu steuern, müssen Sie die elektronische Messagingverarbeitung einrichten.

- Protokollieren Sie Informationen darüber, wer den Bericht generiert hat.
- Protokollieren Sie, wann der Bericht generiert wurde.
- Speichern Sie Berichte, die für frühere Perioden generiert wurden.

Dieser Abschnitt enthält ein Beispiel, das anzeigt, wie Sie möglicherweise die elektronischen Nachrichtenfunktionen einrichten, um einen Berichterstellungsprozess zu erstellen.

### <a name="set-up-and-run-processing-to-call-a-simple-er-exporting-format-to-generate-an-excel-report"></a>Einrichten und Ausführen der Verarbeitung, um ein einfaches EB-Exportformat aufzurufen, um einen Excel-Bericht zu generieren

Dieser Abschnitt enthält ein Beispiel, das anzeigt, wie Sie elektronisches Messaging einrichten können, um einen Bericht zu generieren, der auf einem Export-EB-Format für Excel basiert. Um diesem Beispiel zu folgen, muss das EB-Excel-Exportformat bereits erstellt, zugeordnet zu Datenquellen und abgeschlossen sein. Ein Nummernkreis muss für elektronische Nachrichten bereitss eingerichtet sein.

Wenn Sie die Verarbeitung erstellen, ist es hilfreich, wenn Sie zuerst die Verarbeitungsaktivitätsstatus definieren, die eingerichtet werden. Die folgende Abbildung zeigt, wie die Verarbeitung für dieses Beispiel aussieht.

![Verarbeitungsschema](media/processing-scheme.png)

#### <a name="create-message-statuses"></a>Nachrichtenstatus erstellen

1. Wechseln Sie zu **Steuer \> Einrichtung \> Elektronische Nachrichten \> Nachrichtenstatus**.
2. Erstellen Sie die folgenden Nachrichtenstatus:

    - Neue
    - Vorbereitet
    - Generiert

    ![Nachrichtenstatus](media/message-statuses.png)

3. Auf der Position für den Status **Neu**, aktivieren Sie das Kontrollkästchen **Löschen ermöglichen**, um Benutzern das Löschen von Meldungen zu ermöglichen, die diesen Status besitzen.

#### <a name="create-additional-fields"></a>Zusätzliche Felder erstellen

1. Wechseln Sie zu **Steuer \> Einrichtung \> Elektronische Nachrichten \> Zusätzliche Felder**.
2. Fügen Sie ein zusätzliches Feld und seine Werte hinzu. Hier ist ein Beispiel.

    ![Zusätzliche Felder](media/additional-fields.png)

3. Legen Sie die Option **Benutzerbearbeitung** auf **Ja** fest, damit Benutzer das Feld bearbeiten können.

#### <a name="create-message-processing-actions"></a>Nachrichtenverarbeitungsaktivitäten erstellen

Für dieses Beispiel werden Sie die folgenden Aktivitäten erstellen:

- **Nachricht erstellen**
- **Aktualisieren auf „Vorbereitet”**
- **Bericht generieren**
- **Aktualisieren auf Anfangsstatus** (optional)

1. Wechseln Sie zu **Steuer \> Einrichtung \> Elektronische Nachrichten \> Nachrichtenverarbeitungsaktivitäten**.
2. Erstellen Sie eine Aktivität mit der Bezeichnung **Nachricht erstellen**. Wählen Sie im Inforegister **Allgemein** im Feld **Aktivitätstyp** die Option **Nachricht erstellen** aus.
3. Erstellen Sie eine Aktivität mit der Bezeichnung **Aktualisieren auf „Vorbereitet”**, und legen Sie die folgenden Felder fest:

    - Wählen Sie im Inforegister **Allgemein** im Feld **Aktivitätstyp** die Option **Nachrichtenebenenbenutzer-Verarbeitung** aus.
    - Wählen Sie im Inforegister **Anfangsstatus** im Feld **Nachrichtenstatus** die Option **Neu** aus.
    - Wählen Sie im Inforegister **Ergebnisstatus** im Feld **Nachrichtenstatus** die Option **Vorbereitet** aus. Geben Sie im Feld **Antworttyp** den Text **Erfolgreich ausgeführt** ein.

4. Erstellen Sie eine Aktivität mit der Bezeichnung **Bericht generieren**, und legen Sie die folgenden Felder fest:

    - Wählen Sie im Inforegister **Allgemein** im Feld **Aktivitätstyp** die Option **Elektronischer Berichterstellungsexport** aus. Wählen Sie im Feld **Formatzuordnung** das Export-EB-Format aus. Die Optionen sind **Excel**, **XML**, **JSON**, **Text** und **Andere**.
    - Wählen Sie im Inforegister **Anfangsstatus** im Feld **Nachrichtenstatus** die Option **Vorbereitet** aus.
    - Wählen Sie im Inforegister **Ergebnisstatus** im Feld **Nachrichtenstatus** die Option **Generiert** aus. Geben Sie im Feld **Antworttyp** den Text **Erfolgreich ausgeführt** ein.

    ![Berichtsaktivität generieren](media/generate-report-action.png)

5. Optional: Um es Benutzern zu ermöglichen, einen Bericht mehrere Male neu zu generieren, können Sie eine Aktivität **Auf Anfangsstatus aktualisieren** erstellen und die folgenden Felder festlegen:

    - Wählen Sie im Inforegister **Allgemein** im Feld **Aktivitätstyp** die Option **Nachrichtenebenenbenutzer-Verarbeitung** aus.
    - Wählen Sie im Inforegister **Anfangsstatus** im Feld **Nachrichtenstatus** die Option **Generiert** aus.
    - Wählen Sie im Inforegister **Ergebnisstatus** im Feld **Nachrichtenstatus** die Option **Vorbereitet** oder (und) **Neu** aus. Geben Sie im Feld **Antworttyp** den Text **Erfolgreich ausgeführt** ein.

#### <a name="electronic-message-processing"></a>Verarbeitung der elektronischen Nachricht

In diesem Beispiel sollten alle Aktivitäten eingerichtet werden, sodass sie getrennt ausgeführt werden. Es wird davon ausgegangen, dass jede Aktivität vom Benutzer initiiert wird.

1. Wechseln Sie zu **Steuer \> Einrichtung \> Elektronische Nachrichten \> Elektonische Nachrichtenverarbeitung**.
2. Fügen Sie einen Datensatz für Ihre Verarbeitung hinzu, und fügen Sie alle zuvor definierten Aktivitäten sowie ein zusätzliches Feld hinzu.
3. Optional: Definieren Sie im Inforegister **Sicherheitsrollen** Sicherheitsrollen für Ihre Verarbeitung, um den Zugriff auf bestimmte Berichterstellung zu beschränken.
4. Wechseln Sie zu **Steuer \> Abfragen und Berichte \> Elektronische Nachrichten \> Elektronische Nachrichten**.
5. Wählen Sie **Neu** aus, um eine Nachricht zu erstellen. An diesem Punkt können Sie Datumsangaben und eine Beschreibung hinzufügen. Sie können auch den Wert des zusätzlichem Felds auch Bedarf aktualisieren.

    ![Eine elektronische Nachricht erstellen](media/create-electronic-message.png)

Das Raster im Inforegister **Aktivitätsprotokoll** wird automatisch mit einem Protokoll aller Aktivitäten ausgefüllt, die zu dieser Nachricht ausgeführt werden.

Sie können jetzt den Nachrichtenstatus entweder löschen oder aktualisieren. Um den Nachrichtenstatus zu aktualisieren, wählen Sie **Status aktualisieren** aus, und dann im Feld **Neuer Status** wählen Sie **Vorbereitet** aus. Wählen Sie dann **OK** aus.

![Den Nachrichtenstatus aktualisieren](media/update-status.png)

Der Nachrichtenstatus wird auf **Vorbereitet** aktualisiert, und Sie können jetzt den Bericht generieren, indem Sie **Bericht generieren** auswählen. Der Bericht wird generiert, und der Nachrichtenstatus sowie das Aktivitätsprotokoll werden aktualisiert. Um den generierten Bericht anzuzeigen, wählen Sie die im Aktivitätsbereich die Schaltfläche **Anhang** aus.
