---
title: Überblick über die Finanzberichterstellung
description: In diesem Thema wird beschrieben, wo Sie in Microsoft Dynamics 365 Finance auf Finanzberichte zugreifen und wie Sie Finanzberichtfunktionen verwenden.
author: aprilolson
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "10444"
- intro-internal
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8a209390a8424e2ec3d6654b54b36e36fcd349b3
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/06/2022
ms.locfileid: "8721898"
---
# <a name="get-started-with-financial-reporting"></a>Erste Schritte mit der Finanzberichterstellung 

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wo Sie auf Finanzberichte zugreifen und wie Sie Finanzberichtsfunktionen verwenden. Es umfasst auch eine Beschreibung der Standardfinanzberichte, die zur Verfügung stehen.

## <a name="accessing-financial-reporting"></a>Finanzberichterstellung nutzen

Sie können das Menü **Finanzberichterstattung** an den folgenden Orten finden:

- **Hauptbuch** &gt; **Abfragen und Berichte**
- **Planung** &gt; **Anfragen und Berichte** &gt; **Grundlegende Planung**
- **Planung** &gt; **Anfragen und Berichte** &gt; **Grundlegende Planung**
- **Planung** &gt; **Anfragen und Berichte** &gt; **Grundlegende Steuerung**
- Konsolidierungen

Um Finanzberichte für eine juristische Person zu erstellen und zu generieren, müssen Sie die folgenden Informationen für diese juristische Person einrichten:

- Steuerkalender
- Unternehmen
- Kontenplan
- Währung
- Eine Buchung auf mindestens ein Konto buchen
- „MainAccount“ ist in der Spalte **Ausgewählt** auf der Seite **Finanzberichterstellungseinrichtung** (**Hauptbuch > Sachkontoeinrichtung > Finanzberichterstellung**) aufgeführt

## <a name="granting-security-access-to-financial-reporting"></a>Gewähren des Sicherheitszugriffs auf die Finanzberichterstellung

Die Finanzberichtsfunktionen stehen Benutzern zur Verfügung, denen die entsprechenden Rechte und die Aufgaben über ihre Sicherheitsrollen zugewiesen werden. Die folgenden Abschnitten führen diese Rechte und Aufgaben und die zugeordneten Rollen auf.

### <a name="duties"></a>Aufgaben

| Aufgabenbezeichnung                            | Beschreibung                                                             | AOT-Name                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Finanzberichtssicherheit verwalten | Finanzberichtssicherheit verwalten und Verwaltungsaufgaben ausführen | FinancialReportsSecurityMaintain |
| Finanzberichte verwalten            | Finanzberichte entwerfen und verwalten.                                  | FinancialReportsMaintain         |
| Finanzberichte generieren            | Finanzberichte generieren und aktualisieren.                                 | FinancialReportsGenerate         |
| Die Finanzen des Unternehmens überprüfen          | Die Finanzen des Unternehmens überprüfen und analysieren.                               | FinancialReportsPerfReview       |

### <a name="privileges"></a>Berechtigungen

| Rechtebezeichnung                       | Beschreibung                                                             | AOT-Name                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Finanzberichtssicherheit verwalten | Finanzberichtssicherheit verwalten und Verwaltungsaufgaben ausführen | FinancialReportsSecuritySystemMaintain |
| Finanzberichte verwalten            | Finanzberichte entwerfen und verwalten.                                  | FinancialReportsMaintainReports  |
| Finanzberichte generieren            | Finanzberichte generieren und aktualisieren.                                 | FinancialReportsGenerateReports  |
| Finanzberichte anzeigen                | Finanzberichte anzeigen.                                                 | FinancialReportsView             |

### <a name="roles"></a>Rollen

| Rechtebezeichnung                       | Abgabe                                  | Rollen                                                                           |
|---------------------------------------|---------------------------------------|---------------------------------------------------------------------------------|
| Finanzberichtssicherheit verwalten | Finanzberichtssicherheit verwalten | Sicherheitsadministrator                                                          |
| Finanzberichte verwalten            | Finanzberichte verwalten            | Buchhaltungsmanager, Buchhaltungsvorgesetzter, Finanzcontroller, Planungsmanager |
| Finanzberichte generieren            | Finanzberichte generieren            | CEO, CFO, Buchhalter                                                            |
| Finanzberichte anzeigen                | Die Finanzen des Unternehmens überprüfen          | Nicht zugewiesen                                                                   |

Nachdem Sie ein Benutzer hinzugefügt haben, oder eine Rolle geändert wurde, sollte der Benutzer innerhalb weniger Minuten auf die Finanzberichterstellung zugreifen können. 

> [!NOTE]
> Die Rolle SysAdmin wird allen Rollen in der Finanzberichterstattung hinzugefügt.

## <a name="report-deletions-and-expirations"></a>Löschungen und Verfallsdaten melden

Benutzer, die einen Bericht erstellen, können ihre eigenen Berichte löschen. Benutzer mit der Pflicht **Finanzberichtssicherheit verwalten** können die Berichte anderer Benutzer löschen. 

In Release 10.0.8 wurde das Konzept der Ablaufdaten eingeführt. Eine neue erforderliche Funktion ist auf der Seite **Alle** im Arbeitsbereich der Funktionsverwaltung aktiviert. Die Funktion **Richtlinien zur Aufbewahrung von Finanzberichten** enthält die folgenden Änderungen:
* Neu generierte Berichte werden automatisch mit einem Ablaufdatum von 90 Tagen ab dem Zeitpunkt ihrer Generierung gekennzeichnet.
* Alle vorhandenen Berichte, die vor der Installation der Funktion erstellt wurden, haben eine Gültigkeitsdauer von 90 Tagen. Das Datum wird möglicherweise für einen kurzen Zeitraum leer angezeigt, bis der Finanzberichtsdienst ausgeführt wird, ein Bericht generiert wird und der Dienst die Aktualisierung vorhandener Berichte mit einem leeren Ablaufdatum durchführt. 
* Benutzer mit **Finanzberichtssicherheit verwalten** haben Zugriff auf diese Funktion. Jeder Benutzer mit der Pflicht **Finanzberichte verwalten**, der die Berechtigung **Ablaufdatum des Finanzberichts beibehalten** erhalten hat, kann den Ablaufzeitraum ändern. Derzeit sind zwei Optionen zur Vermerkdauer verfügbar: 

    * Ablauf von 90 Tagen.
    * Eine Option zum Festlegen, dass der Bericht niemals abläuft.

Wenn ein Ablaufdatum ausgewählt wird, zum Beispiel 90 Tage, werden die 90 Tage ab heute gezählt. Dies ist anders als bei den 90 Tagen ab dem ursprünglichen Generierungsdatum, das bei der Erstellung des Berichts festgelegt wurde. 

Zusätzliche Optionen werden in zukünftigen Funktionen berücksichtigt. Ablauf von 90 Tagen ist die Standardeinstellung und Benutzer mit entsprechenden Berechtigungen können die Standardeinstellung für die **Finanzberichte**-Listenseite überschreiben.

## <a name="default-reports"></a>Standardberichte

Die Finanzberichterstellung enthält 22 standardmäßige Finanzberichte. Jeder Bericht verwendet die standardmäßige Hauptkontokategorien. Sie können diese Berichte verwenden oder sie als Ausgangspunkt für Ihre Finanzberichte nutzen. Zusätzlich zu herkömmlichen Finanzaufstellungen (z. B. Einkommensaufstellung und Bilanz) enthalten diese Standardberichte Berichte, die die unterschiedlichen Arten von Finanzberichten aufzeigen, die Sie erstellen können. 

<!--Each report in the following table links to an Office Mix presentation about the report.-->

| Standardbericht                                                                                         | Beschreibung                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 12 Monatiges Rollen-Einspalteneinkommensaufstellung - Standard | Hier wird die Rentabilität einer Organisation für den letzten 12 Monate in einer Spalte angezeigt.                                                                                                                                                                                                                                      |
| 12 Monatige Einnahmentrendaufstellung - Standard                 | Hier wird die Rentabilität einer Organisation für jeden der letzten 12 Monate angezeigt. Die 12 Monate können mehr als ein Geschäftsjahr umfassen.                                                                                                                                                                                             |
| Projekt vs. Budget – Standard                                | Anzeigen ausführlicher Saldoinformationen für alle Konten für das ursprüngliche Budget und Vergleich des überarbeiteten Budgets mit den tatsächlichen Zahlen mit einer Abweichung.                                                                                                                                                                          |
| Überwachungsdetails – Standard                                  | Detaillierte Ansicht der Saldoinformationen für alle Konten. In diesem Bericht werden Soll- und Guthabensalden in der Berichtswährung und in der lokalen Währung angezeigt, zusammen mit zusätzlichen Buchungsinformationen, wie der Benutzerkennung, dem Benutzer, der zuletzt die Daten bearbeitet hat, dem Datum der letzten Änderung und der Erfassungskennung. |
| Saldenliste – Standard                                   | Detaillierte Ansicht der Saldoinformationen für alle Konten. In diesem Bericht werden Anfangs- und Abschlusssalden sowie Soll- und Guthaben für die aktuelle Periode bis zum aktuellen Jahr zusammen mit zusätzlichen Buchungsinformationen, wie dem Beleg angezeigt.                                                                    |
| Bilanz – Standard                                   | Enthält eine Ansicht der Finanzposition der Organisation für das Jahr.                                                                                                                                                                                                                                                             |
| Konsolidierte Bilanz und Einkommensaufstellung parallel – Standard | Hier werden der finanzielle Stand und die Rentabilität der Organisation für das Jahr nebeneinander angezeigt.                                                                                                                                                                                                                              |
| Cashflow – Standard                                       | Informationen zum Bargeld, das ein- und ausgeht.                                                                                                                                                                                                                                   |
| Detaillierter JE- und TB-Review - Standard                      | Hier werden Anfangssaldo und Aktivitätsinformationen für alle Konten angezeigt.                                                                                                                                                                                                                                                      |
| [Ausführliche Zwischenbilanz – Standard](trial-balance-financial-reports.md)| Enthält Saldoinformationen für alle Konten und schließt Soll- und Habensalden und deren Nettowert zusammen mit dem Transaktionsdatum, dem Beleg und der Erfassungsbeschreibung ein.                                                                                                                                  |
| Vierteljährlicher Ausgabentrend über drei Jahre – Standard             | Information zu Ausgaben während der letzten 12 Quartale in den vorherigen drei Jahren.                                                                                                                                                                                                                                   |
| Finanztitel JE- und TB-Review – Standard            | Ein Überblicks der Salden und der Aktivität für die Anlage, die Fälligkeit, das Eigenkapitalkonto, Umsatzerlöse, Ausgaben, Gewinn oder Verlust Finanztitel.                                                                                                                                                                           |
| [Einkommensaufstellung – Standard](income-statement-financial-report.md)| Enthält eine Ansicht der Rentabilität der Organisation für die aktuelle Periode und seit Jahresbeginn.                                                                                                                                                                                                                                   |
| Sachkontobuchungsliste – Standard                        | Detaillierte Ansicht der Saldoinformationen für alle Konten. Dieser Bericht zeigt die Soll- und Habensaldos, zusammen mit zusätzlichen Buchungsinformationen, wie Buchungsdatum, der Erfassungsnummer, dem Beleg, dem Buchungstyp und der Tracenummer an.                                                                            |
| Kennzahlen – Standard                                          | Hier werden die Solvenz, die Rentabilität und die Effizienzrate für die Organisation für das Jahr angezeigt.                                                                                                                                                                                                                           |
| Umlaufende Ausgaben über 12 Monate – Standard                       | Informationen zu Ausgaben für die letzten 12 Monate. Die 12 Monate können mehr als ein Geschäftsjahr umfassen.                                                                                                                                                                                                       |
| Umlaufende vierteljährliche Einkommensaufstellung – Standard               | Hier wird die Rentabilität der Organisation vierteljährlich für das letzte Jahr und für das laufende Jahr angezeigt.                                                                                                                                                                                                                   |
| Parallele Bilanz – Standard                      | Enthält eine Ansicht der Finanzposition der Organisation für das Jahr. Dieser Bericht zeigt die Aktiva und die Verbindlichkeiten und das Eigenkapital der Anteilseigner parallel an.                                                                                                                                                                                |
| [Zusammengefasste Zwischenbilanz – Standard](trial-balance-financial-reports.md)| Enthält Saldoinformationen für alle Konten und schließt Eröffnungs- und Abschlusssalden sowie Soll- und Habensalden, zusammen mit ihrem Nettounterschied ein.                                                                                                                                                                  |
| [Jährlich zusammengefasste Zwischenbilanz – Standard](trial-balance-financial-reports.md)| Enthält Saldoinformationen für alle Konten und schließt Eröffnungs- und Abschlusssalden sowie Soll- und Habensalden, zusammen mit ihrem Nettounterschied für das aktuelle Jahr und das vergangene Jahr ein.                                                                                                                           |
| Wochenumsatz und Rabatte – Standard                     | Informationen zum in Verkauf und zu Rabatten für jeder Woche in einem Monat. Dieser Bericht umfasst eine Summe für vier Wochen.                                                                                                                                                                                                              |
| Die verfügbaren Budgetmittel - Standard                         | Hier wird ein detaillierter Vergleich des überarbeiteten Budgets, die tatsächliche Aufwendungen, Budgetreservierungen und der Budgetmittel, die für alle Konten verfügbar sind, angezeigt                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Öffnen von Finanzberichten

Wenn Sie das Menü **Finanzberichterstattung** auswählen, wird die Liste der standardmäßigen Finanzberichte für das Unternehmen angezeigt. Sie können einen Bericht öffnen oder ändern. Um einen der Standardberichte zu öffnen, wählen Sie den Berichtsname aus. Wenn ein Bericht zum ersten Mal geöffnet wird, wird er automatisch für den vorherigen Monat generiert. Wenn Sie beispielsweise einen Bericht zum ersten Mal im August 2019 öffnen, wird der Bericht zum 31. Juli 2019 generiert. Nach dem Öffnen eines Berichts können Sie ihn durchsuchen, indem Sie Detailinformationen bestimmter Daten anzeigen und Berichtsoptionen ändern.

## <a name="creating-and-modifying-financial-reports"></a>Finanzberichte erstellen und ändern

Über die Finanzberichte Liste können Sie einen neuen Bericht erstellen oder einen vorhandenen Bericht ändern. Wenn Sie die erforderlichen Berechtigungen besitzen, können Sie einen neuen Finanzbericht erstellen, indem Sie **Neu** im Aktionsbereich auswählen. Ein Berichts-Designer-Programm wird auf Ihr Gerät heruntergeladen. Nachdem der Berichts-Designer startete, können Sie den neuen Bericht erstellen. Nachdem Sie den neuen Bericht gespeichert haben, erscheint er in der Finanzberichtsliste. Die Liste enthält nur Berichte, die für das Unternehmen erstellt wurden, das Sie in Dynamics 365 Finance verwenden. 

## <a name="reporting-tree-definitions"></a>Berichtsbaumstruktur-Definitionen

Eine der Komponenten, die zum Erstellen von Finanzberichten verwendet werden, ist eine Berichtsbaumdefinition. Die Berichtsstruktur-Definition hilft, die Struktur und die Hierarchie Ihrer Organisation zu definieren. Es ist eine dimensionsübergreifende hierarchische Struktur, die auf den dimensionalen Beziehungen in den Finanzdaten basieren. Sie stellt Informationen für alle Einheiten in der Struktur auf der Berichtseinheitenebene und auf einer Zusammenfassungsebene bereit.

Sie können eine unbegrenzte Anzahl von Berichtsbaumstrukturen erstellen, um die Daten der Organisation auf verschiedene Weise anzuzeigen. Jeder Berichtsbaum kann eine beliebige Kombination von Abteilungen und Zusammenfassungseinheiten enthalten. Eine Berichtsdefinition kann jedoch jeweils nur mit einem Berichtsbaum verknüpft werden. 

## <a name="update-the-financial-reporting-version-through-slipstreaming"></a>Die Version der Finanzberichterstattung durch Slipstreaming aktualisieren

Apps für Finanzen und Betrieb werden jeden Monat aktualisiert. Die Finanzberichterstattung wird jedoch nicht unbedingt in diesem Rhythmus aktualisiert. Darüber hinaus haben Kunden mehr Möglichkeiten, wann sie Updates für Apps für Finanzen und Betrieb implementieren. Updates für die Finanzberichterstattung werden automatisch installiert. Die Finanzberichterstattung hat eine bestimmte Version, die in einer Kundenumgebung verwendet wird, wenn ein Serviceupdate implementiert wird, wenn eine Ausfallzeit eingeleitet wird oder wenn sich die Kundenumgebung im Wartungsmodus befindet. Dieser Prozess ist als *Slipstreaming* oder *True-up* bekannt, da alle Kundenimplementierungen auf dieselbe Version der Finanzberichterstattung festgelegt sind.

Änderungen, die in jeder Version veröffentlicht werden, finden Sie in [Was ist neu oder wurde in Dynamics 365 Finance geändert](../../finance/get-started/whats-new-home-page.md). Plattform-Updates und Problembehandlungen finden Sie im Abschnitt „Zusätzliche Ressourcen“ am Ende der Seite für jede Version.

Die ausgewählte Slipstream-Version ist eine überprüfte und validierte Version der Finanzberichterstattung, die zur Produktion bereit ist. Sie ist mit jeder früheren oder zukünftigen Version von Dynamics 365 Finance kompatibel. Beispielsweise kann die Finanzberichterstattung über das neueste 10.0.19-Build verfügen, während der Kunde noch die Anwendungsversion 10.0.16 verwendet.

> [!NOTE]
> Der einzige Umstand, in dem Kunden zu einer früheren Version wechseln können (ein Downgrade-Szenario), tritt ein, wenn Microsoft einen True-Up-Rollout aufgrund eines Problems stoppt. Sobald ein Fix verfügbar ist, wird dieser automatisch angewendet.

Der Slipstream-Prozess ist vollständig automatisiert und erfordert keine Kundenaktion. Drei Topologien nutzen Slipstream, jede auf etwas andere Weise:

- **Lokal** – Lokale Bereitstellungen unterstützen kein Slipstream und True-Up.
- **Infrastructure as a service (IaaS)** – Die Slipstream-Logik wird bei jedem Vorgang angewendet, der versucht, die Finanzberichterstattung zu aktualisieren. Sie enthält binäre Updates oder Broadcasts, die binäre Updates enthalten.
- **Self-Service** – Jeder Vorgang, der eine Ausfallzeit der Finanzberichterstattung erfordert, wendet die Slipstream-Logik an:

    - Binäre Updates oder Broadcasts, die binäre Updates enthalten
    - S-Patching oder andere Ausfallzeiten der Infrastruktur
    - AOT-Paketbereitstellungen

## <a name="troubleshooting-issues-opening-report-designer"></a>Behandlung von Problemen beim Öffnen des Berichts-Designers

Es gibt einige häufige Probleme, die beim Öffnen des Berichts-Designers zu Problemen führen können. Diese Probleme und die Schritte zu ihrer Behebung lauten wie folgt.

Problem 1: Der Berichts-Designer wird nicht gestartet, wenn Sie **Neu** oder **Bearbeiten** auswählen.

* Im Internet Explorer wählen Sie **Einstellungen** aus, dann wählen Sie **Internetoptionen** aus. Wähle Sie die Registerkarte **Sicherheit** aus. Wählen Sie „Vertrauenswürdige Sites“ und dann **Sites** aus. Unter **Diese Website zur Zone hinzufügen** geben Sie „\*\.dynamics.com“ (ohne Anführungszeichen) ein und wählen dann **Hinzufügen** aus. 
* Im Internet Explorer wählen Sie **Einstellungen** aus, dann wählen Sie **Internetoptionen** aus. Wählen Sie die Registerkarte **Sicherheit** aus. Wählen Sie „Vertrauenswürdige Sites“ aus. Im Bereich mit der Bezeichnung „Sicherheitsstufe für diese Zone“ ändern Sie die Option zu **Mittel bis niedrig**.
* Deaktivieren Sie den Popupblocker in Ihrem Browser.
* Auf Arbeitsstationen muss Microsoft .NET-Framework 4.7.2 oder höher installiert sein. Diese Version von Microsoft .NET Framework kann heruntergeladen und eingerichtet werden vom [Microsoft Download Center](https://dotnet.microsoft.com/download/dotnet-framework/net472).
* Wenn Sie einen Chrome-Browser verwenden, müssen Sie eine ClickOnce-Erweiterung installieren, um den Berichts-Designer-Client herunterzuladen. Wenn Sie Chrome im Incognito-Modus verwenden, sollten Sie sicherstellen, dass die ClickOnce-Erweiterung auch für den privaten Modus aktiviert ist. Weitere Informationen zu der ClickOnce-Erweiterung von Chrome finden Sie unter [Systemanforderungen für Cloud-Bereitstellung](../../fin-ops-core/fin-ops/get-started/system-requirements.md).
* Wenn Sie Microsoft Edge mit einem Chrome-Browser verwenden, müssen Sie keine ClickOnce-Erweiterung für Edge Chromium installieren. Sie müssen jedoch die ClickOnce-Option aktivieren, um den Report Designer-Client herunterladen zu können. Wenn Sie den Inkognitomodus ausführen, sollten Sie sicherstellen, dass die ClickOnce-Erweiterung auch für den Inkognitomodus aktiviert ist.

    1. Öffnen Sie einen neuen Browser in Microsoft Edge.
    2. Geben Sie **edge://flags** ein und wählen **Eingeben**.
    3. Suchen Sie nach der Option **ClickOnce-Support** oder verwenden Sie diesen direkten Link: **edge://flags/#edge-click-once**.
    4. Stellen Sie die Dropdown-Menüoption auf **Aktiviert** ein.
    5. Wählen Sie **Browser neu starten** aus.

Problem 2: Dem Benutzer wurden nicht die erforderlichen Berechtigungen zur Verwendung von Financial Reporting zugewiesen. 

* Um zu überprüfen, ob der Benutzer keine Berechtigung hat, wählen Sie **Ja** beim Fehler „Verbindung zum Financial Reporting-Server kann nicht hergestellt werden“ aus. Wählen Sie „Ja“ aus, wenn Sie fortfahren und eine andere Serveradresse angeben möchten." Wählen Sie dann **Verbindung testen** aus. Wenn Sie keine Berechtigung haben, wird folgende Meldung angezeigt:„Verbindungsversuch fehlgeschlagen. Der Benutzer verfügt nicht über die entsprechenden Berechtigungen zum Herstellen einer Verbindung zum Server. Wenden Sie sich an einen Systemadministrator.“
* Erforderliche Berechtigungen sind oben aufgeführt in [Gewähren des Sicherheitszugriffs auf die Finanzberichterstellung](#granting-security-access-to-financial-reporting). Die Sicherheit in der Finanzberichterstellung basiert auf diesen Rechten. Sie haben keinen Zugriff, wenn Ihnen diese Rechte (oder eine andere Sicherheitsrolle, die diese Rechte enthält) nicht zugewiesen wurden. 
* Die Integrationsaufgabe **Unternehmensbenutzeranbieter für Unternehmen** (welche auch für die Benutzerintegration verantwortlich und als diese bekannt ist) wird in einem 5-minütigen Intervall ausgeführt. Es kann bis zu 10 Minuten dauern, bis irgendwelche Berechtigungsänderungen in Financial Reporting wirksam werden. 

    Wenn ein anderer Benutzer den Berichts-Designer öffnen kann, wählen Sie **Werkzeuge** aus, und dann wählen Sie **Integrationsstatus** aus. Überprüfen Sie, dass die Integrationszuordnung „Unternehmensbenutzeranbieter für Unternehmen“ erfolgreich ausgeführt wurde, da Ihnen die Berechtigung zur Verwendung von Financial Reporting zugewiesen wurde. 

* Möglicherweise hat ein anderer Fehler verhindert, dass die **Integration von Dynamics-Benutzer in Financial Reporting-Benutzer** fertig gestellt wurde. Oder es ist möglich, dass eine Data Mart-Zurücksetzung initiiert und noch nicht abgeschlossen wurde oder dass ein anderer Systemfehler aufgetreten ist. Versuchen Sie den Prozess später erneut auszuführen. Wenn das Problem weiterhin besteht, wenden Sie sich an Ihren Systemadministrator.

Problem 3: Sie können über die Anmeldeseite von **ClickOnce Report Designer** fortfahren, die Anmeldung im Report Designer jedoch nicht abschließen. 

* Die auf Ihrem lokalen Computer festgelegte Zeit für die Eingabe Ihrer Anmeldeinformationen muss innerhalb von fünf Minuten nach der Zeit auf dem Financial Reporting-Server liegen. Bei einem Unterschied von mehr als fünf Minuten lässt das System keine Anmeldung zu. 
* Wenn die Uhrzeit auf Ihrem Computer von der Uhrzeit auf dem Finanzberichterstellungsserver abweicht, empfehlen wir, die Windows Option zu aktivieren, die die Uhrzeit Ihres Computers automatisch einstellt. 

## <a name="troubleshoot-report-designer-issues-with-event-viewer"></a>Beheben von Problemen mit dem Report Designer mit der Ereignisanzeige

Sie können die Ereignisanzeige verwenden, um einige der Probleme zu analysieren, die bei der Verwendung der Finanzberichterstellung auftreten. 

### <a name="what-happens-when-you-have-connections-issues-with-financial-reporting"></a>Was passiert, wenn Sie Verbindungsprobleme mit der Finanzberichterstellung haben? 

Hier sind einige Schritte, die Sie unternehmen können, um Ihr Gespräch mit dem Microsoft-Support effektiver zu gestalten und Sie schneller zu einer Lösung zu bringen. 
 
Die folgenden Schritte führen durch den Prozess zum Aktivieren von Ereignisanzeigenachrichten für die Finanzberichterstellung. Die von der Ereignisanzeige generierten Protokolle helfen Supportmitarbeitern dabei, die Ursache des Verbindungsproblems schnell zu identifizieren. Senden Sie Kopien dieser Protokolle zusammen mit Ihrem Ticket, wenn Sie den Support kontaktieren.


1. Kopieren Sie die Datei RegisterETW.zip auf die Client-Arbeitsstation (vorzugsweise den Desktop) und entpacken Sie [RegisterETW.zip](https://mbs2.microsoft.com/fileexchange/?fileID=60b1106b-d5f8-4e0f-8041-039102505122).
2. Stellen Sie sicher, dass die Windows-Ereignisanzeige geschlossen ist.
3. Öffnen Sie eine Administrator PowerShell-Eingabeaufforderung und wechseln Sie in das Verzeichnis, in dem sich RegisterETW.ps1 befindet.
4. Führen Sie den folgenden Befehl aus: .\RegisterETW.ps1

    Eine erfolgreiche Ausgabe in PowerShell wird mit der Meldung **Abgeschlossenes RegisterETW-Skript** bestätigt.

    Öffnen Sie erneut die Ereignisanzeige, und Sie sehen diese Protokolle nun unter **Microsoft > Dynamics**:

    * MR-Client
    * MR-DVT
    * MR-Integration
    * MR-Logger
    * MR-Reporting
    * MR_SchedulerTasks
    * MR-Sql
    * MR-TraceManager

5. Reproduzieren Sie das Problem im Report Designer.
6. Exportieren Sie die MR-Logger-Ereignisse mit der Ereignisanzeige.

## <a name="troubleshoot-issues-connecting-to-financial-reporting"></a>Beheben von Problemen bei der Verbindung mit der Finanzberichterstellung

Problem: Sie erhalten die Fehlermeldung „Verbindung zum Finanzberichterstellungsserver kann nicht hergestellt werden“.

* Stellen Sie fest, ob das Problem in Chrome- und Edge-Internetbrowsern auftritt.
* Wenn das Problem nur in einem Browser auftritt, könnte es sich um ein ClickOnce-Problem handeln. 
* Wenn Sie die Verbindungsfehlermeldung erhalten, wählen Sie **Testen**, um die Verbindung zu testen, um zu sehen, welche Meldung angezeigt wird. 
* Das Problem könnte darauf zurückzuführen sein, dass ein anderer Benutzer keinen Zugriff auf die Finanzberichterstellung hat. Wenn ein Benutzer keinen Zugriff hat, erhält er eine Nachricht, dass er keine Berechtigung hat.
* Wenn das Problem in mehreren Browsern auftritt, stellen Sie sicher, dass die Zeitschaltuhr auf Ihrer Arbeitsstation auf „Automatisch“ eingestellt ist.
* Arbeiten Sie mit einer Person mit Sicherheitsadministrationsrechten in Dynamics 365 Finance und Administrationsrechte für die Netzwerkdomäne, um sich bei Ihrer Arbeitsstation anzumelden, um zu überprüfen, ob eine Verbindung hergestellt werden kann. Wenn sie eine Verbindung herstellen können, hängt das Problem möglicherweise mit den Netzwerkberechtigungen zusammen.
* Deaktivieren Sie auf der Arbeitsstation vorübergehend die Firewall. Wenn Sie sich dann mit Report Designer verbinden können, liegt das Problem an Ihrer Firewall. Arbeiten Sie mit der IT-Abteilung Ihrer Organisation zusammen, um das Problem zu beheben.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Finanzberichte anzeigen](view-financial-reports.md)
- [Definitionen für Berichtsbaumstrukturen in Finanzberichten](../../fin-ops-core/dev-itpro/analytics/financial-reporting-tree-definitions.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
