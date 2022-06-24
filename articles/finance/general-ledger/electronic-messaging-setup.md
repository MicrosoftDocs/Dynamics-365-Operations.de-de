---
title: Elektronische Nachrichten einrichten
description: In diesem Artikel erfahren Sie, wie Sie die Funktionalität für elektronische Nachrichten (EN) einrichten.
author: liza-golub
ms.date: 11/18/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2021-06-23
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 6ac6e4fbc37165a3126de3b1f937a43c980410b4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874550"
---
# <a name="set-up-electronic-messages"></a>Elektronische Nachrichten einrichten

[!include [banner](../includes/banner.md)]

Mithilfe der Funktion **elektronische Nachrichten** (EN) können Sie verschiedene elektronische Berichterstellungsprozesse für verschiedene Dokumenttypen verwalten. In einigen komplexen Szenarien, die [Funktionen zur länderspezifischen Berichterstellung](electronic-messaging.md#country-specific-regulatory-features-supported-by-the-em-functionality) unterstützen, wird die EN-Funktionalität so eingerichtet, dass sie eine Kombination vieler Nachrichtenstatus, Nachrichtenelementstatus, Aktivitäten, zusätzlicher Felder und ausführbarer Klassen ist. Für diese Szenarien sind Pakete von Datenentitäten für den Import verfügbar. Wenn Sie diese Datenentitätspakete verwenden, sollten Sie sie in eine juristische Person importieren, indem Sie das Datenverwaltungstool verwenden. Weitere Informationen dazu, wie das Datenverwaltungstool verwendet wird, finden Sie unter [Datenverwaltung](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).

Wenn Sie kein Datenentitätspaket importieren, kann die EN-Funktionalität manuell eingerichtet werden. In diesem Fall müssen Sie die folgenden Elemente einrichten:

- [Nummernkreise](#sequences)
- [Nachrichtenelementtypen](#types)
- [Nachrichtenelementstatus](#item)
- [Nachrichtenstatus](#statuses)
- [Zusätzliche Felder](#additional)
- [Ausführbare Klasseneinstellungen](#executable)
- [Datensatzauffüllungsaktivitäten](#populate)
- [Datensätze von mehreren Unternehmen ausfüllen](#multiple-companies-populate)
- [Webanwendungen](#applications)
- [Webdiensteinstellungen](#settings)
- [Verarbeitungsaktivitäten für Nachrichten](#actions)
- [Verarbeitung der elektronischen Nachricht](#processing)

Die folgenden Abschnitte enthalten mehr Informationen zu jedes dieser Elemente.

## <a name="number-sequences"></a><a id="sequences"></a>Nummernkreise

Richten Sie Nummernkreise sowohl für Nachrichten als auch Nachrichtenelemente ein. Die Nummernkreise werden dann verwendet, um die Nachrichten und die Nachrichtenelemente automatisch zu nummerieren. Die zugeordneten Nummern werden als eindeutige Bezeichner für die Nachrichten und die Nachrichtenelemente im System verwendet. Sie können Nummernkreise für elektronisches Messaging über **Hauptbuch** \> **Sachkonto einrichten** \> **Hauptbuchparameter** einrichten.

## <a name="message-item-types"></a><a id="types"></a>Nachrichtenelementtypen

Nachrichtenelementtypen identifizieren die Datensatztypen, die in den elektronischen Nachrichten verwendet werden. Sie können Nachrichtenelementtypen über **Steuer** \> **Einrichten** \> **Elektronische Nachrichten** \> **Nachrichtenelementtypen** einrichten.

## <a name="message-item-statuses"></a><a id="item"></a>Nachrichtenelementstatus

Nachrichtenelementstatus identifizieren die Status, die für Nachrichtenelemente in der Verarbeitung gelten, die Sie gerade einrichten. Sie können Nachrichtenelementstatus über **Steuer** \> **Einrichten** \> **Elektronische Nachrichten** \> **Nachrichtenelementstatus** einrichten.

Der Parameter **Löschen zulassen** eines Nachrichtenelementstatus definiert, ob Sie Nachrichtenelemente löschen können, die diesen Status auf der Seite **Elektronische Nachrichten** oder der Seite **Elektronische Nachrichtenelemente** haben.

## <a name="message-statuses"></a><a id="statuses"></a>Nachrichtenstatus

Richten Sie die Nachrichtenstatus ein, die bei der Nachrichtenverarbeitung verfügbar sein sollen. Sie können Nachrichtenstatus über **Steuer** \> **Einrichten** \> **Elektronische Nachrichten** \> **Nachrichtenstatus** einrichten.

In der folgenden Tabelle werden die Felder auf der Seite **Nachrichtenstatus** beschrieben.

| Feldname          | Beschreibung |
|---------------------|-------------|
| Nachrichtenstatus      | Geben Sie einen eindeutigen Namen für den Nachrichtenstatus ein. Nachrichtenstatus werden verwendet, um den Status einer elektronischen Nachricht in jedem Moment zu kennzeichnen. Der Name, den Sie eingeben, wird auf der Seite **Elektronische Nachrichten** und in einem Protokoll angezeigt, das elektronischen Nachrichten zugeordnet ist. |
| Beschreibung         | Geben Sie eine Beschreibung des Nachrichtenstatus ein. |
| Antworttyp       | Wählen Sie den Antworttyp für den Nachrichtenstatus aus. Einige Aktivitäten in einer Verarbeitung können mehr als einen Antworttyp erzeugen. Eine Aktion des Typs **Webdienst** kann beispielsweise Antworten des Typs **Erfolgreich ausgeführt** oder des Typs **Technischer Fehler** erzeugen, je nach dem Ergebnis der Ausführung. Definieren Sie in diesem Fall Nachrichtenstatus für beide Antworttypen. Weitere Informationen zu Aktivitätstypen und deren Antworttypen, die sich auf sie beziehen, finden Sie weiter unten in diesem Artikel unter [Aktivitätstypen bei der Nachrichtenverarbeitung](#action-types). |
| Nachrichtenelementstatus | Manchmal muss sich der Status einer elektronischen Nachricht auf den Status zugehöriger Nachrichtenelemente auswirken. Wählen Sie einen Nachrichtenelementstatus in diesem Feld aus, um ihn dem Nachrichtenstatus zuzuordnen. |
| Löschen zulassen        | Aktivieren Sie dieses Kontrollkästchen, wenn Benutzer elektronische Nachrichten löschen können sollen, die diesen Status auf der Seite **Elektronische Nachrichten** haben. |

## <a name="additional-fields"></a><a id="additional"></a>Zusätzliche Felder

Mit der EN-Funktionalität können Sie Datensätze aus Transaktionstabellen in Microsoft Dynamics 365 Finance als Nachrichtenelemente sammeln. Auf diese Weise können Sie die Datensätze für die Berichterstellung vorbereiten und diese anschließend melden. Transaktionstabellen enthalten manchmal jedoch nicht genügend Informationen, um die Datensätze in eine Weise auszufüllen, die die Berichtsanforderungen erfüllt. Um alle Informationen einzugeben, die für einen Datensatz gemeldet werden müssen, können Sie zusätzliche Felder einrichten. Zusätzliche Felder können Nachrichten sowie Nachrichtenelementen zugeordnet werden. Sie können zusätzliche Felder über **Steuer** \> **Einrichten** \> **Elektronische Nachrichten** \> **zusätzliche Felder** einrichten.

In der folgenden Tabelle werden die allgemeinen Felder auf der Seite **Zusätzliche Felder** beschrieben.

| Feld       | Beschreibung |
|-------------|-------------|
| Feldname  | Geben Sie den Namen eines zusätzlichen Felds für elektronische Nachrichten oder Nachrichtenelementen ein, die dem Prozess zugeordnet sind. Dieser Name wird auf der Benutzeroberfläche (UI) angezeigt, wenn sie mit dem Prozess arbeiten. Der Name kann auch in EB-Konfigurationen (elektronische Berichterstellung) verwendet werden, die dem Prozess zugeordnet sind. |
| Beschreibung | Geben Sie eine Beschreibung für das zusätzliche Feld ein. |
| Benutzerbearbeitung   | Legen Sie diese Option auf **Ja** fest, wenn Benutzer den Wert des zusätzlichen Felds in der Benutzeroberfläche ändern können sollen. |
| Zähler     | Legen Sie diese Option auf **Ja** fest, wenn das zusätzliche Feld einen Nummernkreis in einer elektronischen Nachricht enthalten soll. Der Wert des zusätzlichen Felds wird automatisch ausgefüllt, wenn eine Aktivität vom Typ **Elektronischer Berichtexport** ausgeführt wird. |
| Ausgeblendet      | Setzen Sie diese Option auf **Ja**, wenn das zusätzliche Feld in der Benutzeroberfläche auf der Seite **Elektronische Nachrichten** oder **Elektronische Nachrichtenelemente** ausgeblendet werden soll. |

Auf dem Inforegister **Werte** können Sie Werte voreinstellen, die ein zusätzliches Feld haben kann. Diese Werte stehen dann den Benutzern zur Auswahl zur Verfügung. Daher müssen sie während der Verarbeitung nicht manuell ausgefüllt werden. In der folgenden Tabelle werden die Felder näher erläutert.

| Feld                | Beschreibung |
|----------------------|-------------|
| Feldwert          | Geben Sie den Feldwert zur Verwendung für eine Nachricht oder ein Nachrichtenelement während der Berichterstellung ein. |
| Beschreibung          | Geben Sie eine Beschreibung des Feldwerts ein. |
| Kontenart         | Einige Feldwerte sind möglicherweise auf bestimmte Kontotypen beschränkt. Wählen Sie einen der folgenden Wert aus: **Alle**, **Kunde** oder **Lieferant**. |
| Kontocode         | Wenn Sie **Kunde** oder **Lieferant** im Feld **Kontotyp** ausgewählt haben, können Sie die Benutzung des Feldwerts weiter auf eine bestimmte Gruppe oder Tabelle einschränken. |
| Konto-/Gruppennummer | Wenn Sie **Kunde** oder **Lieferant** im Feld **Kontotyp** ausgewählt haben und wenn Sie eine Gruppe oder Tabelle im Feld **Kontocode** eingegeben haben, können Sie eine bestimmte Gruppe oder einen Counteragent in diesem Feld eingeben. |
| Gültig            | Geben Sie das Datum an, an dem die Berücksichtigung des Werts beginnen soll. |
| Ablauf           | Geben Sie das Datum an, an dem die Berücksichtigung des Werts beendet werden soll. |

Standardmäßig wirken sich Kombinationen von Kriterien, die von den Feldern **Konto-/Gruppennummer**, **Kontocode**, **Gültig** und **Ablauf** definiert werden, nicht auf die Auswahl von Werten für zusätzliche Felder aus. Allerdings können diese Kombinationen in einer ausführbaren Klasse verwendet werden, um eine bestimmte Logik zu implementieren, die Werte für zusätzliche Felder berechnet.

## <a name="executable-class-settings"></a><a id="executable"></a>Ausführbare Klasseneinstellungen

Eine ausführbare Klasse ist eine X++-Methode oder -Klasse, die die elektronische Nachrichtenverarbeitung in Bezug auf eine Aktivität aufrufen kann, wenn irgendeine Auswertung für den Prozess erforderlich ist.

Sie können manuell eine ausführbare Klasse einrichten, die während der Verarbeitung aufgerufen werden muss, indem Sie auf **Steuer** \> **Einrichten** \> **Elektronische Nachrichten** \> **Ausführbare Klasseneinstellungen** gehen. Erstellen Sie auf der Seite **Ausführbare Klasseneinstellungen** eine Zeile und legen Sie die folgenden Felder fest.

| Feld                 | Beschreibung |
|-----------------------|-------------|
| Ausführbare Klasse      | Geben Sie den Namen ein, der bei der Einrichtung einer Nachrichtenverarbeitungsaktivität verwendet wird, in Bezug auf den diese Klasse aufgerufen wird. |
| Beschreibung           | Geben Sie eine Beschreibung der ausführbaren Klasse ein. |
| Ausführbarer Klassenname | Wählen Sie eine ausführbare X++-Klasse aus. |
| Ausführungsebene       | Dieses Feld wird automatisch festgelegt, da der Wert für die ausgewählte ausführbare Klasse vordefiniert ist. Dieses Feld begrenzt die Ebene, auf der die dazugehörige Auswertung ausgeführt wird. |
| Klassenbeschreibung     | Dieses Feld wird automatisch festgelegt, da der Wert für die ausgewählte ausführbare Klasse vordefiniert ist. |
| Vorgangstyp           | Dieses Feld ist verfügbar, wenn die Funktion **\[EN\] Typ ausführbare Klassenaktivität** im Arbeitsbereich **Funktionsverwaltung** eingestellt ist. Verwenden Sie dieses Feld, um den Aktivitätstyp für die ausführbare Klasse anzugeben. Dieses Feld ermöglicht eine genauere Kontrolle über die nächsten Aktivitäten, die für die elektronische Nachricht auf der Seite **Elektronische Nachrichten** zur Verfügung stehen. |

Einige ausführbare Klassen besitzen möglicherweise obligatorische Parameter, die definiert werden müssen, bevor die ausführbare Klasse zum ersten Mal ausgeführt wird. Um diese Parameter festzulegen, wählen Sie im Aktivitätsbereich **Parameter** aus. Richten Sie im angezeigten Dialogfeld die Felder ein und wählen Sie dann **OK**. Es ist wichtig, dass Sie **OK** auswählen. Andernfalls werden die Parameter nicht in der Datenbank gespeichert, und die ausführbare Klasse wird nicht ordnungsgemäß aufgerufen.

## <a name="populate-records-actions"></a><a id="populate"></a>Datensatzauffüllungsaktivitäten

Sie verwenden Aktivitäten zum Auffüllen von Datensätzen, um Aktivitäten einzurichten, durch die Datensätze zur Tabelle „Nachrichtenelemente“ hinzugefügt werden, sodass sie einer elektronischen Nachricht hinzugefügt werden können. Wenn beispielsweise Ihre elektronische Nachricht Debitorenrechnungen melden muss, müssen Sie eine Aktivität zum Auffüllen von Datensätzen einrichten, die mit dem Feld **Datenquelle** in der Tabelle „Debitorenrechnungserfassung” verknüpft ist.

Sie können Aktivitäten zum Auffüllen von Datensätzen über **Steuer** \> **Einrichten** \> **Elektronische Nachrichten** \> **Datensatzaktivitäten auffüllen** einrichten. Erstellen Sie einen neuen Datensatz für jede Aktivität, durch die Datensätze der Tabelle hinzugefügt werden sollen, und legen Sie die folgenden Felder fest.

| Feld       | Beschreibung |
|-------------|-------------|
| Name        | Geben Sie einen Namen für die Aktivität ein, durch die Datensätze in Ihrem Prozess ausgefüllt werden. |
| Beschreibung | Geben Sie eine Beschreibung der Aktivität zum Auffüllen von Datensätzen ein. |

Fügen Sie im Inforegister **Datenquelleneinrichtung** eine Position für jede Datenquelle hinzu, die für den Prozess verwendet wird, und legen Sie die folgenden Felder fest.

| Feld                  | Beschreibung |
|------------------------|-------------|
| Name                   | Geben Sie einen Namen für die Datenquelle ein. |
| Nachrichtenelementtyp      | Wählen Sie den Typ des Nachrichtenelements aus, der verwendet werden soll, wenn Datensätze für die Datenquelle erstellt werden. |
| Kontenart           | Wählen Sie den Kontotyp aus, der den Datensätzen aus der Datenquelle zugeordnet werden soll. |
| Mastertabellenname      | Wählen Sie die Tabelle aus, die eine Datenquelle sein soll. |
| Feld „Dokumentnummer”  | Wählen Sie das Feld aus, aus dem die Belegnummer in der ausgewählten Mastertabelle entnommen werden soll. Der Wert dieses Felds wird als Wert des Felds **Dokumentnummer** für das Nachrichtenelement genutzt. |
| Feld „Dokumentdatum”    | Wählen Sie das Feld aus, aus dem das Dokumentdatum in der ausgewählten Mastertabelle entnommen werden soll. Der Wert dieses Felds wird als Wert des Felds **Nachrichtenelementdatum** für das Nachrichtenelement genutzt. |
| Feld „Dokumentenkonto” | Wählen Sie das Feld aus, aus dem das Dokumentkonto in der ausgewählten Mastertabelle entnommen werden soll. Der Wert dieses Felds wird als Wert des Felds **Kontonummer** für das Nachrichtenelement genutzt. |
| Firma                | Dieses Feld ist verfügbar, wenn die Funktion **Unternehmensübergreifende Abfragen für Aktivitäten zum Auffüllen von Datensätzen** im Arbeitsbereich **Funktionsverwaltung** aktiviert ist. Verwenden Sie diese Funktion, um unternehmensübergreifende Datenquellen für die Aktivitäten zum Auffüllen von Datensätzen einzurichten. Daten können aus mehreren Unternehmen abgerufen werden. |
| Benutzerabfrage             | <p>Wenn Sie eine Abfrage einrichten, indem Sie über dem Raster **Abfrage bearbeiten** auswählen, und Sie geben die Kriterien an, die auf die ausgewählte Mastertabelle, aus der Daten entnommen werden, angewendet werden müssen, wird dieses Kontrollkästchen automatisch aktiviert. Andernfalls werden alle Datensätze aus der ausgewählten Mastertabelle ausgefüllt.</p><p>Wenn die Funktion **Unternehmensübergreifende Abfragen für Aktivitäten zum Auffüllen von Datensätzen** im Arbeitsbereich **Funktionsverwaltung** aktiviert ist und Datensätze von mehreren Unternehmen eingeholt werden müssen, fügen Sie eine Zeile für jede zusätzliche juristische Person hinzu, die in die Berichterstellung einbezogen werden muss. Wählen Sie für jede neue Zeile **Abfrage bearbeiten** aus und geben Sie ein zugehöriges Kriterium an, das für die im Feld **Unternehmen** der Zeile angegebene juristische Person spezifisch ist. Wenn Sie fertig sind, enthält das Raster **Datenquelleneinrichtung** Zeilen für alle juristischen Personen, die in die Berichterstellung einbezogen werden müssen.</p> |

## <a name="populate-records-from-multiple-companies"></a><a id="multiple-companies-populate"></a>Datensätze von mehreren Unternehmen ausfüllen

Wenn Ihr Unternehmen von mehreren juristischen Personen in derselben Finanzdatenbank berichten muss, richten Sie die [Aktionen zum Auffüllen von Datensätzen](#populate) für alle juristischen Personen ein, deren Daten in die Berichterstattung einbezogen werden müssen.

Befolgen Sie diese Schritte, um diese Funktionen in Ihrer Finanzumgebung zu aktivieren. 

1. Wechseln Sie zu **Arbeitsbereiche** \> **Verwaltung von Funktionen**.
2. Suchen und wählen Sie die **Unternehmensübergreifende Abfragen für Aktivitäten zum Auffüllen von Datensätzen**-Funktion in der Liste aus.
3. Wählen Sie **Jetzt aktivieren**. 

Um [Aktionen zum Auffüllen von Datensätzen](#populate) für mehrere Unternehmen einzurichten, von denen Daten in die Berichterstattung einbezogen werden müssen, gehen Sie wie folgt vor.

1. Gehen Sie zu **Steuer** \> **Einrichten** \> **Elektronische Nachrichten** \> **Datensatzauffüllungsaktivitäten**.

    Wenn die **Unternehmensübergreifende Abfragen für die Aktionen zum Auffüllen von Datensätzen**-Funktion aktiviert ist, enthält das **Einrichtung von Datenquellen**-Raster auf der **Datensatzauffüllungsaktivität**-Seite ein Feld **Unternehmen**. Für bestehende Datensätze, die bei der allgemeinen Einrichtung des [Datensatzauffüllungsaktivität](#populate) erstellt wurden, zeigt dieses Feld die Kennung der aktuellen juristischen Person an.

2. Im Raster **Einrichtung von Datenquellen** fügen Sie für jede untergeordnete juristische Person, die in die Berichterstellung einbezogen werden muss, und legen Sie die folgenden Felder fest.

    | Feldname             | Wert |
    |------------------------|-------|
    | Name                   | Geben Sie einen Textwert ein, der Ihnen hilft zu verstehen, woher dieser Datensatz stammt. Geben Sie z. B. **Datenquellenname – Tochtergesellschaft 1** ein. |
    | Nachrichtenelementtyp      | Wählen Sie den Nachrichtenpositionstyp aus, der für Ihre EM-Verarbeitung erforderlich ist. |
    | Kontenart           | Legen Sie den Kontotyp fest, der für Ihre EM-Verarbeitung erforderlich ist. Wenn Ihre EM-Verarbeitung keine bestimmten Kontotypen hat, wählen Sie **Alle** aus. |
    | Mastertabellenname      | Geben Sie den Namen der Mastertabelle an, die für Ihre EM-Verarbeitung erforderlich ist. |
    | Feld „Dokumentnummer”  | Geben Sie das Feld an, das die Belegnummer in Datensätzen Ihrer EM-Verarbeitung enthält. |
    | Feld „Dokumentdatum”    | Geben Sie das Feld an, das das Belegdatum in Datensätzen Ihrer EM-Verarbeitung enthält. |
    | Feld „Dokumentenkonto” | Geben Sie das Feld an, das das Belegkonto in Datensätzen Ihrer EM-Verarbeitung enthält. |
    | Unternehmen                | Wählen Sie die ID der untergeordneten juristischen Person aus. |
    | Benutzerabfrage             | Dieses Kontrollkästchen wird automatisch aktiviert, wenn Sie Kriterien definieren, indem Sie **Abfrage bearbeiten** auswählen. |

3. Wählen Sie für jede neue Zeile **Abfrage bearbeiten** aus und geben Sie zugehörige Kriterien an, das für die im Feld **Unternehmen** der Zeile angegebene juristische Person spezifisch ist.

## <a name="web-applications"></a><a id="applications"></a>Webanwendungen

Verwenden Sie Webanwendungseinstellungen, um eine Webanwendung einzurichten, damit sie Open Authorization (OAuth) 2.0 unterstützt. OAuth ist ein offener Standard, mit dem Benutzer „sicheren delegierten Zugriff” auf die Anwendung in ihrem Auftrag gewähren können, ohne ihre Anmeldeinformationen für den Zugriff zu teilen. Sie können auch den Autorisierungsprozess durchführen, indem Sie einen Autorisierungscode und ein Zugriffstoken abrufen. Sie können Webanwendungseinsteinstellungen über **Steuer** \> **Einrichten** \> **Elektronische Nachrichten** \> **Webanwendungen** einrichten.

In der folgenden Tabelle werden die Felder auf der Seite **Webanwendungen** beschrieben.

| Feld                        | Beschreibung |
|------------------------------|-------------|
| Anwendungsname             | Geben Sie einen Namen für den Webanwendung ein. |
| Beschreibung                  | Geben Sie eine Beschreibung des Webanwendung ein. |
| Basis-URL                     | Geben Sie die Basis-Internetadresse der Webanwendung ein. |
| Autorisierungs-URL-Pfad       | Geben Sie den Pfad ein, der verwendet wird, um die URL für die Autorisierung zu erstellen. |
| Token-URL-Pfad               | Geben Sie den Pfad an, der verwendet wird, um die URL für den Token zu erstellen. |
| Umleitungs-URL                 | Umleitungs-URL eingeben. |
| Clientkennung                    | Geben Sie die Client-ID der Webanwendung ein. |
| Geheimer Clientschlüssel                | Geben Sie den geheimen Clientschlüssel der Webanwendung ein. |
| Servertoken                 | Geben Sie das Server-Token der Webanwendung ein. |
| Autorisierungsformatzuordnung | Wählen Sie das EB-Format aus, das verwendet wird, um die Anforderung zur Autorisierung zu generieren. |
| Importtoken-Modellzuordnung   | Wählen Sie die EB-Importmodellzuordnung aus, mit der der Zugriffstoken gespeichert wird. |
| Gewährter Bereich                | Der Bereich, der für Anforderungen zur Bewerbung gewährt wird. Dieses Feld wird automatisch aktualisiert. |
| Zugriffstoken läuft ab in  | Die verbleibende Zeit, bevor der Zugriffstoken abläuft. Dieses Feld wird automatisch aktualisiert. | 
| Übernehmen                       | Geben Sie die Eigenschaft **Annehmen** der Webanforderung an. Geben Sie beispielsweise **application/vnd.hmrc.1.0+json** ein. |
| Inhaltstyp                 | Geben Sie den Inhaltstyp an. Geben Sie beispielsweise **application/json** ein. |

Darüber hinaus sind die folgenden Schaltflächen verfügbar im Aktivitätsbereich der Seite **Webanwendungen**, um den Autorisierungsprozess zu unterstützen:

- **Autorisierungscode abrufen** – Autorisierung der Webanwendung initialisieren. Diese Funktion verwendet das EB-Format, das im Feld **Autorisierungsformatzuordnung**, um eine Autorisierungsanfrage zu generieren.
- **Zugriffstoken abrufen** – Den Prozess des Abrufens eines Zugriffstokens initialisieren.
- **Zugriffstoken aktualisieren** – Einen Zugriffstoken aktualisieren. Diese Funktion verwendet das EB-Format, das im Feld **Importtoken-Modellzuordnung**, um Informationen über das empfangene Zugriffstoken zu importieren.

Wenn ein Zugriffstoken für eine Webanwendung, die in der Datenbank des Systems in verschlüsseltem Format gespeichert ist, kann es für Anforderungen an einen Webdienst verwendet werden. Aus Sicherheitsgründen ist der Zugriff auf das Zugriffstoken auf die Sicherheitsrollen begrenzt, die derartige Anforderungen ausfüllen dürfen. Wenn jemand außerhalb der Sicherheitsgruppe versucht, eine Anforderung zu erteilen, erhält er eine Fehlermeldung, die aussagt, dass er nicht über die ausgewählte Webanwendung interagieren darf. Um die Sicherheitsrollen einzurichten, die Zugriff auf das Zugriffstoken haben, verwenden Sie das Inforegister **Sicherheitsrollen** auf der Seite **Webanwendungen**. Wenn Sicherheitsrollen für eine Webanwendung nicht definiert sind, kann nur ein Systemadministrator mithilfe der Webanwendung interagieren.

Für jede Aktivität mit der ausgewählten Webanwendung speichert das Inforegister **Aktivitätsprotokoll** Informationen über den Benutzer sowie Datum und Uhrzeit.

Bei einigen Webdiensten müssen möglicherweise unterschiedliche Kopfzeilen in die Anforderungen aufgenommen werden. Der Systemadministrator kann zusätzliche Kopfzeilen und deren Werte im Inforegister **Ergänzende Kopfzeilen** einrichten und diese dann während der Anforderungsgenerierung verwenden.

## <a name="web-service-settings"></a><a id="settings"></a>Webdiensteinstellungen

Verwenden Sie Webdiensteinstellungen, um direkte Datenübermittlung zu einem Webdienst einzurichten. Sie können Webdiensteinsteinstellungen über **Steuer** \> **Einrichten** \> **Elektronische Nachrichten** \> **Webdiensteinstellungen** einrichten.

In der folgenden Tabelle werden die Felder auf der Seite **Webdiensteinstellungen** beschrieben.

| Feld                          | Beschreibung |
|--------------------------------|-------------|
| Webdienst                    | Geben Sie einen Namen für den Webdienst ein. |
| Beschreibung                    | Geben Sie eine Beschreibung des Webdiensts ein. |
| Internetadresse               | <p>Geben Sie die Internetadresse des Webdiensts ein. Wenn eine Webanwendung für den Webdienst angegeben ist und wenn die Internetadresse des Webdiensts mit der Internetadresse identisch sein soll, die für diese Webanwendung definiert ist, wählen Sie **Basis-URL kopieren** aus. In dieses Feld wird dann die Basis-URL der Webanwendung kopiert.</p><p>**Warnung:** Drittanbieterdienste oder andere Dienste, die Sie hier konfigurieren, benötigen keine Zertifizierung und erfüllen möglicherweise nicht die Datenschutzstandards von Microsoft. Sie sollten die Datenschutzdokumentation jedes Diensts überprüfen und mit jedem Dienstanbieter zusammenarbeiten, um mehr über die Konformitätsstufe zu erfahren, die dieser Dienst bietet. Sie sind dafür verantwortlich, sicherzustellen, dass diese Dienste Ihre Sicherheits-, Datenschutz- und gesetzlichen Standards erfüllen. Sie tragen das Risiko, das sich aus der Verwendung der Dienste ergibt. Microsoft gewährt keine ausdrücklichen Gewährleistungen, Garantien oder Bedingungen. Es wird dringend empfohlen, dass Sie nur Diensten verwenden, die sichere und autorisierte Verbindungen wie HTTPS verwenden.</p> |
| Zertifikat                    | Wählen Sie ein Azure Key Vault-Zertifikat aus, das zuvor eingerichtet wurde. |
| Webanwendung                | Wählen Sie eine Webanwendung aus, die zuvor eingerichtet wurde. |
| Der Antworttyp – XML        | Legen Sie diese Option auf **Ja** fest, wenn der Antworttyp XML ist. |
| Anforderungsmethode                 | Geben Sie die Methode der Anforderung an. HTTP definiert eine Gruppe von Anforderungsmethoden, die die Aktivität angeben, die für eine bestimmte Ressource ausgeführt werden soll. Die Anforderungsmethode kann **GET**, **POST** oder eine andere HTTP-Methode sein. |
| Anforderungskopfzeile                | Geben Sie Anforderungskopfzeilen an. Eine Anforderungskopfzeile ist eine HTTP-Kopfzeile, die in einer HTTP-Anforderung verwendet werden kann. Sie hat nichts mit dem Inhalt der Nachricht zu tun. |
| Übernehmen                         | Geben Sie die Eigenschaft „Übernehmen“ der Webanforderung an. |
| Codierung akzeptieren                | Geben Sie den Wert „Accept-Encoding“ an. Die HTTP-Kopfzeile der Accept-Codierungsanforderung kündigt die Inhaltscodierung an, die der Client verstehen kann. Diese Inhaltscodierung ist normalerweise ein Komprimierungsalgorithmus. |
| Inhaltstyp                   | Geben Sie den Inhaltstyp an. Die HTTP-Kopfzeile der Entität „Inhaltstyp” gibt den Medientyp der Ressource an. |
| Code für erfolgreiche Antwort       | Geben Sie den HTTP-Statuscode an, der angibt, dass die Anforderung erfolgreich war. |
| Anforderungskopfzeilen-Formatzuordnung | Wählen Sie das EB-Format aus, das verwendet wird, um Webanforderungskopfzeilen zu generieren. |

## <a name="message-processing-actions"></a><a id="actions"></a>Verarbeitungsaktivitäten für Nachrichten

Mithilfe von Nachrichtenverarbeitungsaktivitäten erstellen Sie Aktivitäten für Ihre Prozesse und richten deren Parameter ein. Sie können Nachrichtenverarbeitungsaktivitäten über **Steuer** \> **Einrichten** \> **Elektronische Nachrichten** \> **Nachrichtenverarbeitungsaktivitäten** einrichten.

In den folgenden Tabellen werden die Felder auf der Seite **Nachrichtenverarbeitungsaktivitäten** beschrieben.

### <a name="general-fasttab"></a>Allgemeines Inforegister

| Feld                                     | Beschreibung |
|-------------------------------------------|-------------|
| Vorgangstyp                               | Wählen Sie den Typ der Aktivität aus. Informationen zu den verfügbaren Optionen finden Sie weiter unten in diesem Artikel im Abschnitt [Nachrichtenverarbeitungsaktivitäts-Typen](#action-types). |
| Formularzuordnung                            | Wählen Sie das EB-Format aus, das für die Aktivität aufgerufen werden soll. Dieses Feld ist nur für Aktivitäten der Typen **Elektronischer Berichterstellungsexport**, **Elektronischer Berichterstellungsimport** und **Elektronische Berichterstellungsexportnachricht** verfügbar. |
| Formatzuordnung für URL-Pfad               | Wählen Sie das EB-Format aus, das für die Aktivität aufgerufen werden soll. Dieses Format wird verwendet, um den Pfad der URL-Adresse zu erstellen, der der Basisinternetadresse hinzugefügt wird, die für den ausgewählten Webserver angegeben wird. Dieses Feld ist nur für Aktivitäten vom Typ **Webdienst** verfügbar. |
| Nachrichtenelementtyp                         | Wählen Sie den Typ von Datensätzen aus, für den die Aktivität ausgewertet werden soll. Dieses Feld ist für Aktivitäten der Typen **Nachrichtenelement-Ausführungsebene**, **Elektronischer Berichterstellungsexport**, **Elektronischer Berichterstellungsimport** und **Webdienst** und andere Typen verfügbar. Wenn Sie dieses Feld leer lassen, werden alle Nachrichtenelementtypen, die für die Nachrichtenverarbeitung definiert sind, ausgewertet. |
| Ausführbare Klasse                          | Wählen Sie eine vorhandene ausführbare Klasseneinstellung aus. Dieses Feld ist nur für Aktivitäten der Typen **Nachrichtenelement-Ausführungsebene** und **Nachrichtenelementausführungsebene** verfügbar. |
| Datensatzauffüllungsaktivität                   | Wählen Sie eine vorhandene Aktivität zum Auffüllen von Datensätzen aus. Dieses Feld ist nur für Aktivitäten vom Typ **Datensätze auffüllen** verfügbar. |
| Webdienst                               | Wählen Sie einen vorhandenen Webdienst aus. Dieses Feld ist nur für Aktivitäten vom Typ **Webdienst** verfügbar. |
| Name der zu versendenden Datei                         | Geben Sie den Namen des Anhangs einer elektronischen Nachricht ein, die bei dieser Aktion gesendet werden muss. Wenn mehrere Anhänge denselben ursprünglichen Dateinamen haben, wird der neueste gesendet. Wird kein Anhang mit dem angegebenen Originaldateinamen gefunden, wird die Anfrage ohne Inhalt gesendet. Dieses Feld ist nur für Aktivitäten vom Typ **Webdienst** verfügbar. |
| Dateiname                                 | Geben Sie den Namen der Datei an, die das Ergebnis der Aktivität sein wird. Diese Datei kann die Antwort vom Webserver oder vom Bericht sein, der erzeugt wird. Dieses Feld ist nur für Aktivitäten der Typen **Webdienst** und **Elektronische Berichterstellungsexportnachricht** verfügbar. |
| Dateien an Quelldokumente anhängen          | Aktivieren Sie dieses Kontrollkästchen, um generierte Dateien an Datensätze in einer referenzierten Mastertabelle für EN-Artikel anzuhängen. Dieses Feld ist nur für Aktivitäten der Typen **Elektronischer Berichtexport** und **Webdienst** verfügbar. |
| Dateien aus dem Ausgabenarchiv den Elementen anfügen | Aktivieren Sie dieses Kontrollkästchen, um separate XML-Dateien aus der Ausgabenarchivdatei zu extrahieren und an die entsprechenden elektronischen Nachrichtenelemente anzuhängen. Dieses Feld ist nur für Aktivitäten vom Typ **Elektronischer Berichterstellungsexport** verfügbar. |
| Anzahl der Nachrichtenelemente pro Export        | Geben Sie den Grenzwert für die Anzahl der Nachrichtenelemente an, die in einer Datei (Nachricht) enthalten sein müssen. Dieses Feld ist nur für Aktivitäten vom Typ **Elektronischer Berichterstellungsexport** verfügbar. |
| EB-Quelle verwenden                             | Aktivieren Sie dieses Kontrollkästchen, um EB-Quellparameter für den Import zu verwenden. Andernfalls wird der Anhang der elektronischen Nachricht verwendet. Dieses Feld ist nur für Aktivitäten vom Typ **Elektronischer Berichterstellungsimport** verfügbar. |
| Dialog anzeigen                               | Legen Sie diese Option auf **Ja** fest, wenn ein Dialogfeld Benutzern angezeigt werden muss, bevor der Bericht generiert wird. Dieses Feld ist nur für Aktivitäten vom Typ **Elektronische Berichterstellungsexportnachricht** verfügbar. |

#### <a name="message-processing-action-types"></a><a id="action-types"></a>Nachrichtenverarbeitungsaktivitäts-Typen

Die folgenden Optionen sind im Feld **Aktivitätstypen** verfügbar:

- **Nachricht erstellen** – Verwenden Sie diesen Aktivitätstyp, damit Benutzer Nachrichten auf der Seite **Elektronische Nachricht** manuell erstellen können. Ein Anfangsstatus für eine Aktivität dieses Typs kann nicht eingerichtet werden.
- **Datensätze ausfüllen** – Dieser Aktionstyp muss bereits eingerichtet sein. Ordnen Sie ihm eine Aktivität zum Auffüllen von Datensätze zu, damit er in die Verarbeitung eingezogen werden kann. Es wird angenommen, dass dieser Aktivitätstyp für die erste Aktivität in der Nachrichtenverarbeitung verwendet wird (wenn keine elektronische Nachricht im Voraus erstellt wurde) oder für eine Aktivität, die Nachrichtenelemente einer Nachricht hinzufügt, die zuvor mithilfe des Aktivitätstyps **Nachricht erstellen** erstellt wurde. Daher kann für Aktivitäten dieses Typs ein Ergebnisstatus nur für Nachrichtenelements eingerichtet werden. Ein Anfangsstatus kann nur für Nachrichten eingerichtet werden.
- **Nachrichtenausführungsebene** – Dieser Aktivitätstyp wird verwendet, um eine ausführbare Klasse einzurichten, die auf der Nachrichtenebene ausgewertet werden soll.
- **Nachrichtenelement-Ausführungsebene** – Dieser Aktivitätstyp wird verwendet, um eine ausführbare Klasse einzurichten, die auf der Nachrichtenelementebene ausgewertet werden soll.
- **Elektronischer Berichterstellungsexport** – Verwenden Sie diesen Aktivitätstyp für Aktivitäten, die einen Bericht generieren sollen, der auf einer Export-EB-Konfiguration auf der Nachrichtenelementebene basiert.
- **Elektronische Berichterstellungsexport-Nachricht** – Verwenden Sie diesen Aktivitätstyp für Aktivitäten, die einen Bericht generieren sollen, der auf einer Export-EB-Konfiguration auf der Nachrichtenebene basiert (wenn beispielsweise eine Nachricht keine Nachrichtenelemente hat).
- **Elektronischer Berichterstellungsimport** – Verwenden Sie diesen Aktivitätstyp für Aktivitäten, die einen Bericht basierend auf einer Import-EB-Konfiguration generieren sollen.
- **Benutzerverarbeitung auf Nachrichtenebene** – Verwenden Sie diesen Aktivitätstyp für Aktivitäten, bei denen von einigen manuellen Aktivitäten durch den Benutzer auf der Nachrichtenebene ausgegangen wird. Beispielsweise aktualisiert der Benutzer unter Umständen den Status von Nachrichten.
- **Benutzerverarbeitung** – Verwenden Sie diesen Aktivitätstyp für Aktivitäten, bei denen von einigen manuellen Aktivitäten durch den Benutzer auf der Nachrichtenelementebene ausgegangen wird. Beispielsweise aktualisiert der Benutzer unter Umständen den Status von Nachrichtenelementen.
- **Webdienst** – Verwenden Sie diesen Aktivitätstyp für Aktivitäten, durch die ein generierter Bericht zu einem Webdienst übertragen werden sollen. Dieser Aktivitätstyp wird nicht für die Berichterstellung für „Italienischer Einkauf” und „Verkaufsrechnungskommunikation” verwendet. Bei diesem Aktivitätstyp umfasst die Seite **Nachrichtenverarbeitungsaktivitäten** ein Inforegister **Sonstige Details**, wo Sie einen Bestätigungstext angeben können. Dieser Bestätigungstext wird Benutzer angezeigt, bevor Anforderungen an den ausgewählten Webdienst gesendet werden.
- **Überprüfung anfordern** – Dieser Aktivitätstyp wird verwendet, um die Überprüfung von einem Server anzufordern.

### <a name="initial-statuses-fasttab"></a>Anfangsstatus-Inforegister

> [!NOTE]
> Das Inforegister **Anfangsstatus** ist nicht für Aktivitäten mit dem Anfangsaktivitätstyp **Nachricht erstellen** verfügbar.

| Feld               | Beschreibung |
|---------------------|-------------|
| Nachrichtenelementstatus | Wählen Sie den Nachrichtenelementstatus aus, für den die ausgewählte Nachrichtenverarbeitungsaktivität ausgewertet werden soll. |
| Beschreibung         | Eine Beschreibung des ausgewählten Nachrichtenelementstatus. |

### <a name="result-statuses-fasttab"></a>Ergebnisstatus-Inforegister

| Feld               | Beschreibung |
|---------------------|-------------|
| Nachrichtenstatus      | Wählen Sie die Nachrichtenstatus aus, für den die ausgewählte Nachrichtenverarbeitungsaktivität ausgewertet werden soll. Dieses Feld ist nur für Nachrichtenverarbeitungsaktivitäten verfügbar, die auf Nachrichtenebene ausgewertet werden. Beispielsweise ist es für Aktivitäten der Typen **Elektronischer Berichterstellungsexport** und **Elektronischer Berichterstellungsimport** verfügbar. Es ist jedoch nicht für Aktivitäten der Typen **Benutzerverarbeitung** und **Nachrichtenelementausführungsebene** verfügbar. |
| Beschreibung         | Eine Beschreibung des ausgewählten Nachrichtenstatus. |
| Antworttyp       | Der Antworttyp des ausgewählten Nachrichtenstatus. |
| Nachrichtenelementstatus | Wählen Sie die resultierenden Status aus, die verfügbar sein sollten, nachdem die ausgewählte Nachrichtenverarbeitungsaktivität ausgewertet ist. Dieses Feld ist nur für Nachrichtenverarbeitungsaktivitäten verfügbar, die auf Nachrichtenelementebene ausgewertet werden. Beispielsweise ist es für Aktivitäten der Typen **Benutzerverarbeitung** und **Nachrichtenelement-Ausführungsebene** verfügbar. Für Nachrichtenverarbeitungsaktivitäten, die auf Nachrichtenebene ausgewertet werden, zeigt dieses Feld den Nachrichtenelementstatus an, der für den ausgewählten Nachrichtenstatus eingerichtet wurde. |

In der folgenden Tabelle werden die Ergebnisstatus angezeigt, die für verschiedene Aktivitätstypen und Antworttypen eingerichtet werden müssen.

| Aktivitätstyp/Antworttyp der elektronischen Nachricht | Erfolgreich ausgeführt | Geschäftsfehler | Technischer Fehler | Von Benutzer definiert | Stornieren |
|----------------------------------------------|-----------------------|----------------|-----------------|--------------|--------|
| Nachricht erstellen                               | X                     |                |                 |              |        |
| Elektronischer Berichtexport                  | X                     |                |                 |              |        |
| Elektronischer Berichtimport                  |                       |                |                 |              |        |
| Webdienst                                  | X                     |                | X               |              |        |
| Benutzerverarbeitung                              |                       |                |                 |              |        |
| Nachrichtenausführungsebene                      |                       |                |                 |              |        |
| Datensätze auffüllen                             |                       |                |                 |              |        |
| Nachrichtenelement-Ausführungsebene                 |                       |                |                 |              |        |
| Überprüfung anfordern                         | X                     | X              | X               |              |        |
| Nachricht zum elektronischen Berichtexport          | X                     |                |                 |              |        |
| Benutzerverarbeitung auf Nachrichtenebene                |                       |                |                 |              |        |

## <a name="electronic-message-processing"></a><a id="processing"></a>Verarbeitung der elektronischen Nachricht

Die elektronische Nachrichtenverarbeitung ist ein Grundprinzip der EN-Funktion. Dadurch werden Aktivitäten aggregiert, die für die elektronische Nachricht ausgewertet sollen. Die Aktivitäten können mithilfe eines Anfangsstatus und eines Ergebnisstatus verknüpft werden. Alternativ können Aktivitäten des Typs **Benutzerverarbeitung** unabhängig gestartet werden. Um die Verarbeitung elektronischer Nachrichten einzurichten, gehen Sie zu **Steuer** \> **Einrichten** \> **Elektronische Nachrichten** \> **Elektronische Nachrichtenverarbeitung**.

Mithilfe des Inforegisters **Aktivität** können Sie der Verarbeitung vordefinierte Aktivitäten hinzufügen. Sie können angeben, ob eine Aktivität gesondert ausgeführt werden muss oder ob sie durch die Verarbeitung gestartet werden kann. Um anzugeben, dass eine Aktivität bei der Verarbeitung nur von einem Benutzer initialisiert werden kann, legen Sie das Feld **Getrennt ausführen** für diese Aktivität auf **Ja** fest. Wenn eine Aktivität durch die Verarbeitung für Nachrichten oder Nachrichtenelemente gestartet werden sollte, die sich im Status befinden, der als Anfangsstatus für die Aktivität definiert ist, legen Sie das Feld **Getrennt ausführen** auf **Nein** fest. Aktivitäten des Typs **Benutzeraktivität** müssen immer separat ausgeführt werden.

Manchmal müssen mehrere Aktivitäten in einen Nummernkreis zusammengefasst werden, obwohl die erste Aktivität so eingerichtet ist, dass sie gesondert ausgeführt wird. Zum Beispiel muss ein Benutzer die Berichtsgenerierung initialisieren. Unmittelbar nachdem der Bericht erstellt ist, muss er aber an einen Webdienst gesendet werden, und die Antwort vom Webdienst muss im System berücksichtigt werden. In diesem Fall können Sie eine untrennbare Sequenz für die Aktivitäten erstellen, die immer zusammen ausgeführt werden müssen. Wählen Sie im Inforegister **Aktivität** die Option **Untrennbare Sequenzen** über dem Raster aus, und erstellen Sie eine Sequenz. Wählen Sie dann für alle Aktivitäten, die zusammen in einer Sequenz ausgeführt werden müssen, die Sequenz im Feld **Untrennbare Sequenz** aus. In diesem Beispiel kann das Feld **Getrennt ausführen** für die erste Aktivität in der Sequenz auf **Ja** festgelegt werden und für alle anderen Aktivitäten auf **Nein**.

Aktivitäten vom Typ **Elektronischer Berichtsexport** und **Nachricht zum elektronischen Berichtexport** führen ein EB-Format mit Eingabeparametern aus. Wenn zu Ihrer elektronischen Nachrichtenverarbeitung solche Aktivitäten gehören, müssen Sie die Werte für die Eingabeparameter vor der Berichtsgenerierung angeben. So kann das System den Bericht über ein Chargenregime generieren. Sie können über dem Raster **Parameter** auswählen, um die Parameter für den ausgewählten Aktivitätstyp einzurichten (**Elektronischer Berichtexport** oder **Nachricht zum elektronischen Berichtexport**). Wählen Sie das Kontrollkästchen **Parameter verwenden** für die Aktivität, die mit den angegebenen Parametern in einem Chargenregime ausgeführt werden muss.

Verwenden Sie das Inforegister **Zusätzliche Felder des Nachrichtenelements**, um vordefinierte zusätzliche Felder hinzufügen, die Nachrichtenelementen zugeordnet sind. Sie müssen zusätzliche Felder für jeden Typ von Nachrichtenelement hinzufügen, dem die Felder zugeordnet sind. Sie können einen Standardwert angeben, der dem zusätzlichen Feld während der Verarbeitung zugewiesen wird.

Verwenden Sie das Inforegister **Zusätzliche Felder des Nachrichtenelements**, um vordefinierte zusätzliche Felder hinzufügen, die Nachrichten zugeordnet sind. Sie können einen Standardwert angeben, der dem zusätzlichen Feld während der Verarbeitung zugewiesen wird.

Verwenden Sie das Inforegister **Sicherheitsrollen**, um Sicherheitsrollen einzurichten, die im System zur speziellen Verarbeitung vordefiniert sind. Benutzer, die eine bestimmte Rolle besitzen, sehen nur die Verarbeitung, die für diese Rolle definiert ist.

Verwenden Sie das Inforegister **Charge**, um festzulegen, dass die Verarbeitung in einem Chargensystem funktioniert. Wir empfehlen Ihnen, ein Chargensystem für Ihre Verarbeitung direkt auf der Seite **Elektronische Nachrichten** oder **Elektronische Nachrichtenelemente** einzurichten, wenn Sie im Aktivitätsbereich **Verarbeitung ausführen** zum Starten der Verarbeitung auswählen.
