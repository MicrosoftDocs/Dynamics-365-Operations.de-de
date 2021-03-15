---
title: Überblick zur Budgetsteuerung
description: Dieser Artikel stellt Budgetsteuerung vor und bietet Informationen, mit denen Sie die Budgetsteuerung in Microsoft Dynamics 365 Finance so konfigurieren können, dass Sie Finanzquellen verwalten können.
author: ShylaThompson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetControlConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom: 60493
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b371e6c87c65e707bf1468eb8df4be892f7750d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990942"
---
# <a name="budget-control-overview"></a>Budgetsteuerung – Übersicht

[!include [banner](../includes/banner.md)]

Dieser Artikel stellt Budgetsteuerung vor und bietet Informationen, mit denen Sie die Budgetsteuerung so konfigurieren können, dass Sie Finanzquellen verwalten können.

<a name="overview"></a>Übersicht
--------

Die Budgetsteuerung unterstützt die Verwaltung der Finanzquellen einer Organisation über den Kontenplan, Workflows, Benutzergruppen, Quelldokumente und Erfassungen, konfigurierbare Berechnungen der verfügbaren Budgetmittel, Budgetzyklen und Schwellenwerte. Mit Steuerelementen kann eine Organisation während des Geschäftsjahrs seine Finanzquellen planen, messen und verwalten. 

Nachdem Budgets in Microsoft Dynamics 365 Finance genehmigt wurden, können Sie Budgetpläne verwenden, um Budgetregistereinträge zu generieren, um das Aufwendungensbudget für eine Organisation zu erfassen. Alternativ können Sie Budgetregistereinträge von einem Programm von einem Drittanbieter erstellen oder importieren, anstatt Budgetplanungsfunktionen zu verwenden. 

Ausgaben können erfasst werden, indem Hauptkonten und Finanzdimensionen verwendet werden. Sie können Steuerelement der gesamten Aufwendungen so konfigurieren, dass sie die Richtlinien und Bedingungen der Organisation erfüllen, indem Sie Kombinationen von Finanzdimensionen und von Hauptkonten gruppieren. 

Das folgende Diagramm zeigt die Funktion der Budgetsteuerung in den Phasen für einen typischen Budgetzyklus.

[![Typischer Budgetzyklus](./media/budgetingcycle-300x198.png)](./media/budgetingcycle.png) 

Sie können die Budgetsteuerung gemäß verschiedenen Faktoren konfigurieren:

-   **Finanzdimensionen**– Welche Finanzdimensionen müssen verwendet werden, um einen Bericht des Budgets und der Istwerte zu erstellen und welche Finanzdimensionen sind erforderlich, um das Budget zu steuern? Gibt es bestimmte Dimensionskombinationen oder Hauptkonten, die besondere Aufmerksamkeit erfordern? Gibt es beispielsweise eine Anforderung, das Budget zu den Istwerten nach Kostenstelle und Programm zu verfolgen? Erfordern Reisekosten bestimmte Aufmerksamkeit?
-   **Zeit** – Welcher Zeitrahmen (Finanzzeitraum, Finanzzeitraum seit Jahresbeginn usw.) wird verwendet, um verfügbare Budgets auszuwerten?
-   **Quelldokumente** – welche Quelldokumente müssen für Budgetsteuerung ausgewertet werden? Müssen die Dokumente pro Position oder pro Dokument ausgewertet werden?
-   **Berechnung der verfügbaren Budgetmittel** – Sollten Dokumente wie Bestellanforderungen (Vorabbelastung) sowie Bestellungen (Belastungen) in die Berechnung der Budgetmittel berücksichtigt werden? Müssen Dokumente in einem Entwurfsstatus in die Berechnung der Budgetmittel berücksichtigt werden?
-   **Berechtigung für Außerkraftsetzung**– Wer ist berechtigt, das verfügbare Budget zu überschreiten?

Die Budgetsteuerung ist vollständig in die Anwendung integriert: Daher können Sie das verfügbare Budget für geplante Einkäufe und tatsächliche Einkäufe überprüfen. Budgetanfragen und Berichte sind verfügbar. Benutzer können das Budget über Budgetzyklen evaluieren und die erforderlichen Anpassungen in Form einer Budgetüberarbeitung oder einer Übertrag vornehmen. Ein Budget-Manager kann auch das Budget und die Istwerte nach Microsoft Excel exportieren, um besser nach Bedarf zu analysieren und zu planen.

## <a name="configuring-budget-control"></a>Konfigurieren der Budgetsteuerung
### <a name="budget-cycle-time-span"></a>Zeitspanne für Budgetzyklus

Nachdem die grundlegende Budgetierung konfiguriert ist, definieren Sie die Zeit oder die Start- und Endperioden für die Budgetierung und Budgetsteuerung auf der Seite **Zeitspanne für Budgetzyklus**. Budgetzyklen entsprechen häufig dem Steuerkalender, können aber Geschäftsjahre umfassen.

Die nächsten Schritte in der Konfiguration werden auf den verschiedenen Registerkarten auf der Seite **Budgetsteuerungskonfiguration** abgeschlossen.

### <a name="define-parameters"></a>Parameter definieren

Auf Grundlage der Finanzdimensionen, die für das Budget aktiviert sind, können Sie alle oder eine Teilmenge der Finanzdimensionen für die Budgetsteuerung verwenden. 

Darüber hinaus können Sie das standardmäßige Zeitintervall angeben (beispielsweise **Geschäftsjahr** **Geschäftsjahr bis heute** **Finanzzeitraum** oder **Quartalsweise**), die für diese Budgetsteuerung für in die zugehörige Zeitspanne für den Budgetzyklus ausgeführt wird. Sie können auch einen standardmäßigen Budget-Manager und den Schwellenwert angeben, der verwendet wird, um Benutzer zu informiern, wenn der Schwellenwert erreicht wurde. Die Werte in diesen Feldern werden als Standardwerte in jeder neuen Budgetsteuerungsregel oder Budgetgruppe verwendet, die erstellt wird. Allerdings können die Standardwerte für einzelne Gruppen oder Regeln geändert werden. 

Die Art und Weise, auf die die Budgets im Budgetregister erstellt und erfasst werden, spielt eine Rolle bei der Bestimmung der auszuwählenden Zeitspanne, wenn verfügbare Budgetmittel ausgewertet werden. Wenn ein auf das Jahr bezogener Betrag für eine Dimensionswertkombination entwickelt und verwendet wird, ist möglicherweise ein Geschäftsjahres- oder Geschäftsjahr seit Jahresbeginn-Ansatz sinnvoll. Wenn eine Organisation aber ein Budget nach Finanzzeitraum erstellt oder den Steuerperioden zuordnet und ausführlichere Kontrolle wünscht, sollten Sie Zeitspannen wie Geschäftsjahr seit Jahresbeginn oder vierteljährlich in Betracht ziehen. 

Darüber hinaus spielt die Kultur einer Organisation hinsichtlich der Budgetierung und Budgetsteuerung bei der Definition der Konfiguration eine Rolle .

### <a name="over-budget-permissions"></a>Berechtigungen für Budgetüberschreitung

Dann können Sie auf der Registerkarte **Berechtigungen für Budgetüberschreitung** die Benutzergruppen angeben. Sie können auch angeben, ob Benutzer, die Mitglieder einer Benutzergruppe sind, berechtigt sind, das Budget zu überschreiten. Sie können Benutzer am Überschreiten des Budgets nach dem Budgetschwellenwert verhindern, der auf der Seite **Budgetparameter** festgelegt wurde oder Sie können diese am Überschreiten des Budgets um einen beliebigen Betrag, unabhängig vom Schwellenwert, hindern. Je nachdem, wie proaktiv eine Organisation die Ausgaben verwaltet, können diese Berechtigungen bei der Verwaltung der Finanzquellen helfen. 

### <a name="budget-funds-available"></a>Verfügbare Budgetmittel

Dann können Sie auf der Registerkarte **Verfügbare Budgetmittel** die Formel definieren, die verwendet wird, um die verfügbaren Budgetmittel zu berechnen. Je nachdem wie konservativ eine Organisation ihre Finanzquellen verwaltet oder unter Berücksichtigung der Bestimmungen oder der Industrieanforderungen, kann die Berechnung einen Entwurf oder ungebuchte Dokumenten enthalten. 

> [!NOTE] 
> Wenn diese Berechnung während eines Budgetzyklus geändert wird, beachten Sie, dass Dokumente, die möglicherweise zuvor Budgetsteuerungsüberprüfungen bestanden haben und gebucht oder abgeschlossen wurden, diesen Status beibehalten.

### <a name="documents-and-journals"></a>Dokumente und Erfassungen

Auf der Registerkarte **Dokumente und Erfassung** können Sie auswählen, welche Quelldokumente und Erfassungen von Budgetsteuerungsüberprüfungen abhängig sind und ob die Prüfung am Positionseintrag oder für das gesamte Dokument durchgeführt wird. 

Wählen Sie die Quelldokumente, die in den Kontrollkästchen aktiviert sind, damit die Summen in der Berechnung der verfügbaren Budgetmittel eingeschlossen sind. Wenn Sie beispielsweise **Budgetreservierungen für Belastungen** ausgewählt haben, sollten Sie die Option **Bestellungen** auswählen. Wenn die Budgetprüfung für die Beträge und Konten in einer Bestellposition ausgeführt wird, ist **Belastung** die Budgetsteuerungskategorie, die der Reservierung zugewiesen wird. Wenn die Budgetprüfung für die Beträge und Konten in einer Bestellanforderung ausgeführt wird, ist die Budgetsteuerungskategorie, die der Reservierung zugewiesen wird **vorbelastet**. 

Wenn die **Budgetreservierungen für die Belastung** und/oder die **Budgetreservierungen für die Vorabbelastung** in der Berechnung der verfügbaren Budgetmittel einbezogen sind und durch Buchungen im Hauptbuch dargestellt werden müssen, sollte die Finanzbudgetüberwachung auf der Seite **Hauptbuchparameter** aktiviert werden.  

### <a name="assign-budget-models"></a>Budgetmodelle zuweisen

Dann sollten Sie auf der Registerkarte **Budgetmodelle zuweisen** der Zeitspanne für den Budgetzyklus Budgetmodelle zuweisen, die in der Budgetsteuerung enthalten sein sollten.

### <a name="define-budget-control-rules"></a>Budgetsteuerungsregeln definieren

Auf der Registerkarte **Budgetsteuerungsregeln definieren** müssen Sie spezifische Regeln basierend auf den Finanzdimensionen erstellen, die für die Budgetsteuerung aktiviert sind. Wenn es beispielsweise einen Fokus basierend auf den Aufwendungen oder dem Ausgabenbereich für eine Abteilung gibt, dann kann das mit den Einstellungen hier definiert und ausgewertet werden. Verschiedene Schwellenwerte können für jede Budgetsteuerungsregel definiert werden. 

> [!Important]
> Die Budgetsteuerung wird für ein Hauptkonto **Gewinn und Verlust**, **Ausgaben**, **Einnahmen, Bilanz, Verbindlichkeiten, Eigenkapital** oder **Anlage**-Typen. Wenn dieser Registerkarte eine Regel enthält, die leere Kriterien hat, wird die Budgetsteuerung für **alle** Finanzdimensionskombinationen aktiviert, die Hauptkonten dieses Typs umfassen. Daher ist es wichtig, Budgetsteuerungsregeln zu erstellen, die nur die Bereiche der Finanzdimensionskombinationen definieren, in denen eine aktivierte Budgetsteuerung von Bedeutung ist.  

### <a name="select-main-accounts"></a>Hauptkonten auswählen

Wenn das **Hauptkonto** nicht als Budgetsteuerungsdimension auf der Seite markiert **Parameter definieren** ausgewählt ist, aber bestimmten Ausgaben verwaltet werden, können Sie diese Aufwendungen auf der Registerkarte **Hauptkonten** auswählen auswählen. Wenn **Hauptkonto** als Budgetsteuerungsdimension ausgewählt ist, sind keine Einträge erforderlich.  

### <a name="define-budget-groups"></a>Budgetgruppen definieren

Auf der Registerkarte **Budgetgruppen definieren** können Sie optional eindeutige Kombinationen von Finanzdimensionen definieren, in denen Budgetressourcen für sekundäre Budgetprüfung zusammengelegt werden. Sie können einen einzelnen Datensatz erstellen, der die gesamte Organisation umfasst oder Sie definieren mehrere Gruppen, um einzelne Abteilungen oder Kostenstellen darzustellen.  

### <a name="define-message-levels"></a>Meldungsebenen definieren

Wenn Warnmeldungen zur Budgetsteuerung für alle Benutzergruppen unterdrückt werden sollen, können Sie diese Gruppen auf der Seite **Meldungsebenen definieren** angeben. Mitglieder der Benutzergruppe erhalten weiterhin Fehlermeldungen, wenn die verfügbaren Budgetmittel basierend auf ihren Berechtigungen für Budgetüberschreitung überschritten werden.

### <a name="activate-budget-control"></a>Budgetsteuerung aktivieren

Nachdem die Budgetsteuerung konfiguriert wurde, können Sie diese Nutzung auf der Registerkarte **Budgetsteuerung aktivieren** aktivieren. Die Entwurfversion wird dann aktiv.
> [!Important]
> Wenn die Budgetsteuerung aktiviert wird und Transaktionen gebucht werden, sollte sie während des Jahres nicht abgeschaltet werden. Wenn die Budgetsteuerung deaktiviert ist, werden Budgettransaktionen nicht in der Budgetquellennachverfolgung erfasst, und es werden keine Budgetprüfungen mehr ausgeführt. Daher beinhalteten möglicherweise Dokumente, die bereits gebucht wurden, ordnungsgemäß keine Entlastungsbeträge oder Salden in Abfragen und Berichten, die zur Budgetsteuerung zugeordnet sind. Dazu zählen die Budgetsteuerungsstatistiken für alle Downstream-Aktivitäten oder das Anpassen von Dokumenten und Erfassungen. 

Beachten Sie zudem, dass Transaktionen, die gebucht wurden, bevor die Budgetsteuerung aktiviert wurde, nicht für die Budgetsteuerung berücksichtigt werden. Daher empfiehlt es sich, die Budgetsteuerung nur zu Beginn eines neuen Budgetzyklus zu aktivieren. Stellen Sie sicher, dass für die Budgetregistereinträge, die Anfangsbudgetsalden für die Budgetsteuerung enthalten, nur aktualisierte Budgetsalden verwendet werden, nachdem die Budgetsteuerung aktiviert ist. Jedes offene Dokument (beispielsweise eine Bestellung) wird auf verfügbare Budgetmittel überprüft und erhält eine Budgetreservierung für die Budgetsteuerung, wenn Benutzer die Budgetsteuerungsüberprüfung im Dokument manuell auslösen.

## <a name="using-budget-control"></a>Verwenden der Budgetsteuerung
Sobald die Budgetsteuerung aktiviert wird, erhalten Benutzer Budgetsteuerungswarnungen und -fehlermeldungen in Dokumenten und Erfassungen, die für die Budgetsteuerung konfiguriert werden. Denken Sie daran, Sie können die Budgetsteuerung konfigurieren, sodass Benutzer, wenn sie die Budgetmittel überschreiten, gewarnt werden, aber trotzdem weiterhin die Buchung bestätigen oder buchen können. Benutzer können die Details von fehlgeschlagenen Budgetprüfungen auf der Seite **Budgetsteuerungsfehler und Warnungen** anzeigen.   

Von dieser Seite aus können Benutzer auf der Seite **Budgetsteuerungsstatistiken** Budgetverfügbarkeiten nach Perioden anzeigen und Reservierungen für eine ausgewählte Budgetsteuerungsdimensionskombination anzeigen. Benutzer können auf der Seite **Budgetsteuerungsstatistik** auch die Budgetverfügbarkeit für alle Finanzdimensionskombinationen anzeigen, die in der Budgetsteuerung verwendet werden. 

Wenn die Budgetsteuerung für Bestellungen aktiviert ist, kann der Budget-Manager den Arbeitsbereich **Sachkontobudgets und Planungen** verwenden, um die Warteschlange aller nicht bestätigter Bestellungen mit Budgetprüfungswarnungen und -fehlern überprüfen. Wenn der Budget-Manager Berechtigungen für Budgetüberschreitung konfiguriert hat, kann die Bestellung direkt im Arbeitsbereich bestätigt werdeen.    


[!INCLUDE[footer-include](../../includes/footer-banner.md)]