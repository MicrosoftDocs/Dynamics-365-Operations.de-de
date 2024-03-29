---
title: Mitarbeiter- und Manager-Self-Service-Übersicht
description: Dieser Artikel bietet einen Überblick über den Self-Service-Arbeitsbereich für Mitarbeiter und Manager.
author: twheeloc
ms.date: 09/12/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.custom:
- "51941"
- intro-internal
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0ecc3f5ae03dda6932dfa111bd4d8b7e6e7b5c7f
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2022
ms.locfileid: "9702155"
---
# <a name="employee-and-manager-self-service-overview"></a>Mitarbeiter- und Manager-Self-Service-Übersicht


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dieser Artikel bietet einen Überblick über den Self-Service-Arbeitsbereich für Mitarbeiter und Manager.

## <a name="edit-personal-details"></a>Personendaten bearbeiten

Wenn Sie persönliche Informationen hinzufügen oder ändern müssen, lesen Sie [Persönliche Daten bearbeiten](hr-employee-manager-self-service-edit-personal-information.md).

## <a name="user-not-assigned-to-a-worker-record"></a>Benutzer, der keinem Arbeitskraftdatensatz zuwiesen ist

Wenn Sie Ihren Benutzer nicht mit einem **Arbeitskraft**-Datensatz auf der Seite **Benutzer** verknüpft haben, wird die folgende Meldung angezeigt:

**Die Benutzerkennung ist dem Mitarbeiterdatensatz im System nicht zugeordnet. Sie können die Informationen erst anzeigen oder aktualisieren, wenn die entsprechende Zuordnung erfolgt ist. Wenden Sie sich hierzu an Ihren Vorgesetzten oder Ihr Support-Team.**

Um einen Benutzer mit einem **Arbeitskraft**-Datensatz zu verknüpfen, navigieren Sie zu **Benutzer**, und wählen Sie den Benutzer aus. Wählen Sie **Bearbeiten** aus, fügen Sie die entsprechende Arbeitskraft im Feld **Person** auf der Seite hinzu, und wählen Sie **Speichern** aus. Sie sollten jetzt Zugriff auf **Mitarbeiter-Self-Service** haben.

## <a name="security-requirements-for-employee-and-manager-self-service"></a>Sicherheitsanforderungen Employee und Manager Self-Service

Employee und Manager Self-Service benötigen zwei Sicherheitsrollen:

- Mitarbeiter benötigen die Mitarbeiter-Rolle.
- Manager benötigen sowohl die Mitarbeiter- als auch die Manager-Rolle.

>[!NOTE]
>Sie können auch benutzerdefinierte Rollen verwenden, um auf den Employee und Manager Self-Service zuzugreifen, sofern ihnen der Zugriff auf die Arbeitsbereiche für Mitarbeiter und Manager gewährt wurde.<br>
>Der Zugriff des Managers auf Mitarbeiterinformationen basiert auf der aktuellen Positionshierarchie, die in Human Resources definiert ist.

## <a name="employee-self-service"></a>Mitarbeiter-Self-Service

Auf der Registerkarte **Meine Information** werden die folgenden Informationen für den **Mitarbeiter-Self-Service** angezeigt.  

### <a name="summary"></a>Summe

**Mir zugewiesene Arbeitsaufgaben** zeigt alle Genehmigungen und Workflowelemente an, die dem Mitarbeiter zugewiesen sind. Sie können Workflowelemente so konfigurieren, dass E-Mails an den Benutzer gesendet werden.

**Mir zugewiesene Fragebögen** zeigt alle geplanten Fragebögen an, die direkt dem Mitarbeiter oder der Gruppe zugewiesen sind.

**Firmenverzeichnis** lässt Mitarbeiter Informationen zu Personen in der Organisation nachschlagen. Öffentliche Kontaktinformationen stehen allen Mitarbeitern zur Verfügung. Das Firmenverzeichnis ist auf die Firma beschränkt, bei der sich der Mitarbeiter angemeldet hat.

**Teamkalender** zeigt die Kalenderinformationen Ihres Teams an. Weitere Informationen finden Sie unter [Team- und Unternehmenskalender anzeigen](hr-employee-self-service-calendar.md).

### <a name="my-career-information"></a>Meine Laufbahninformationen

Der Abschnitt **Meine Karriereinformationen** von **Mitarbeiter-Self-Service** zeigt Kacheln zu Urlaub und Abwesenheit, Leistungsmanagement, Kompetenzen, Vorteilen, Aufgaben und Anhängen an.

Die Kachel **Freizeitguthaben** zeigt die Guthaben für alle registrierten Pläne an. Diese Kachel prognostiziert Ihr Guthaben basierend auf Ihrer Abgrenzungsmethode. Sie können Freistellungsanfragen eingeben und senden, die dann einen Genehmigungsworkflow durchlaufen. Weitere Informationen zu Urlaub und Abwesenheit finden Sie unter [Urlaubs- und Abwesenheitsübersicht](hr-leave-and-absence-overview.md).

Die Kachel **Aufgaben** zeigt Aufgaben an, die Ihnen zugewiesen sind, und ermöglicht Ihnen das Anzeigen und Verwalten dieser Aufgaben.

Die Kachel **Nächster registrierter Kurs** zeigt den nächsten Kurs an, für den Sie registriert sind. Sie können alle offene Kurse anzeigen und sich dafür registrieren. Alle Kurse, die zur Anmeldung geöffnet sind, haben den Status **Gestartet** und Mitarbeiter können sich selbst registrieren. Abhängig von den Einstellungen Ihrer Organisation wird Ihre Kursregistrierung möglicherweise einem Genehmigungsprozess unterzogen.

Die Kachel **Zertifikate** zeigt das Zertifikat und das Ablaufdatum des Zertifikats an, das dem aktuellen Datum am nächsten kommt. Sie können Zertifikate aktualisieren, hinzufügen oder entfernen. Abhängig von den Einstellungen Ihrer Organisation werden Kursaktualisierungen möglicherweise einem Genehmigungsprozess unterzogen.

Die Kachel **Nächste geplante Überprüfung** zeigt Ihre nächste Leistungsbeurteilung an. Über diese Kachel können Sie eine neue Überprüfung starten. Ihr Manager oder Personalvertreter kann auch Überprüfungen einleiten. Abhängig von den Einstellungen Ihres Unternehmens können Sie möglicherweise auch Exit-Bewertungen anzeigen, aktualisieren und senden.

Sie können Ihre Ziele über **Leistungsziele** verwalten. Diese Kachel zeigt die Anzahl der Ziele an, die Sie in jedem Status haben (**Nicht angefangen**, **Auf dem richtigen Weg**, und **Muss verbessert werden**). Sie können Ziele erstellen, aktualisieren und entfernen, abhängig von Ihrer zugewiesenen rollenbasierten Sicherheit. Wenn Sie möchten, können Sie neue Ziele aus Gruppen oder Vorlagen hinzufügen. Manager und HR können auch im Namen der Mitarbeiter Ziele erstellen und bestimmen, wie detailliert jedes Ziel sein wird. Manager und Mitarbeiter können gemeinsam an Zielen arbeiten und Aktivitäten, Messungen und Status aktualisieren. Sie können auch Anhänge einfügen.

Sie können Ihre vorhandenen Fähigkeiten auf der Kachel **Kompetenzen** anzeigen. Sie können Fähigkeiten aktualisieren, neue hinzufügen oder nicht mehr relevante entfernen. Abhängig von den Einstellungen Ihrer Organisation werden Änderungen an Ihren Kompetenzen möglicherweise einem Genehmigungsprozess unterzogen.

Sie können Ihre aktuelle Vergütung auf **Vergütung** anzeigen. Wählen **Anzeigen** aus, um Ihren Jahreslohn und den letzten Erhöhungsbetrag anzuzeigen. Wenn Sie in mehr als einem Unternehmen beschäftigt sind, wird jeder Jahresbetrag angezeigt. Um Ihre detaillierte Vergütungshistorie anzuzeigen, wählen Sie den Betrag **Jährliches Gehalt** aus, um die Seite **Feste und variable Vergütungshistorie** zu öffnen. Zukünftige Vergütungen werden auf dieser Seite nicht angezeigt. Wenn Sie mehr als eine Beschäftigung haben, können Sie auf dieser Seite zwischen Unternehmen wechseln, um Ihren Vergütungsverlauf anzuzeigen, ohne sich bei jedem Unternehmen anzumelden.

Mit der Kachel **Anhänge** können Sie Dokumente anzeigen und verwalten. Sie können alle **Externen** Anhänge verwalten. Sowohl die Personalabteilung als auch die Mitarbeiter können Anhänge über den **Mitarbeiter-Self-Service** oder über die Seite **Arbeitskraft** hinzufügen. Anhänge werden standardmäßig auf **Extern** gesetzt.

### <a name="additional-information"></a>Zusätzliche Informationen

Dieser Abschnitt enthält Links zu anderen Bereichen des **Mitarbeiter-Self-Service**, ähnlich dem Abschnitt **Meine Karriereinformationen**.

Melden Sie sich über den Link **Vorteile** für Vorteile an. Weitere Informationen zur Vorteilsverwaltung finden Sie unter [Vorteilsübersicht](hr-benefits-management-overview.md).

Unter **Leistung** können Sie **Leistungserfassungen** auswählen, um Leistungsjournaleinträgen zu erstellen, die sowohl für Leistungsziele als auch für Überprüfungen verwendet werden können. Sie können **Feedback abschicken** auswählen, um Feedback für andere Mitarbeiter in Ihrer Organisation zu geben. Abhängig von den Einstellungen Ihres Unternehmens werden möglicherweise E-Mails an den Empfänger, den Absender und die Manager gesendet. Sie können Feedback an alle Mitarbeiter innerhalb der Organisation senden. Das Senden von Feedback wird nicht vom Unternehmen eingeschränkt.

Unter **Kompetenzen** können Sie Änderungen an **Kursen**, **Bildung**, **Vertrauenspositionen**, und **Berufserfahrung** vornehmen. Abhängig von den Einstellungen Ihrer Organisation werden Aktualisierungen dieser Kompetenzen möglicherweise einem Genehmigungsprozess unterzogen.

Sie können Jobdetails unter **Organisation** anzeigen. Zu den Jobdetails gehören Fähigkeiten, Zertifikate und Verantwortungsbereiche für Ihre primäre Position. Sie können auch alle ausgeliehenen Geräte sehen, die bei Ihnen ausgecheckt wurden. Abhängig von den Einstellungen Ihrer Organisation werden Änderungen an verliehener Ausrüstung möglicherweise einem Genehmigungsprozess unterzogen.

Unter **Fragebogen** können Sie ausgefüllte Fragebögen sehen. Sie können auch unternehmensweite Fragebögen anzeigen, die noch nicht ausgefüllt wurden. Sie können jederzeit einen Fragebogen ausfüllen. Der Autor des Fragebogens kann den Zeitrahmen bestimmen und für wen der Fragebogen gilt.

Sie können benutzerdefinierte Links in **Human-Resources-Parameter** verwalten. Sie können beispielsweise Links zu Gehaltsabrechnungen, Jahresenddokumentation oder externen Lösungen definieren. Diese Links werden am Ende dieses Abschnitts angezeigt. Sie können sie jedoch mithilfe der Personalisierung verschieben.

Sie können durch Einbetten von Power Apps auch zusätzliche Registerkarten innerhalb des Arbeitsbereichs **Mitarbeiter-Self-Service** erstellen. Verwenden Sie das Menü **Einstellungen**, um die Seite mit einer beliebigen Power Apps zu personalisieren. Im Menü **Einstellungen** können Sie eine Power App hinzufügen, die Details vervollständigen und die App einfügen. Standardmäßig wird Power Apps als erste Registerkarte in der Sequenz angezeigt. Sie können die Reihenfolge über die standardmäßige Personalisierung ändern.

## <a name="my-team"></a>Mein Team

Auf der Registerkarte **Mein Team** werden die folgenden Informationen für den **Manager-Self-Service** angezeigt. Nur Manager können auf die Registerkarte **Mein Team** zugreifen.

### <a name="personnel-actions"></a>Personalaktivitäten

Personalaktionen werden basierend auf den Konfigurationsoptionen in **Gemeinsame Parameter der Personalabteilung** und **Personalverwaltungsparameter** angezeigt. Wenn sie für **Arbeitskräfte** aktiviert sind, ermöglichen Personalaktionen neue Menüoptionen, darunter:

- **Neuen Mitarbeiter anfordern**
- **Neuen Auftragnehmer anfordern**
- **Arbeitskraft-Neuzuweisung anfordern**
- **Kündigung anfordern**
- **Vergütungsänderung beantragen**

Sie können diese Optionen so konfigurieren, dass sie einen optionalen Überprüfungs- und Genehmigungsworkflow durchlaufen.

Durch das Aktivieren von **Positionsaktivitäten** werden die folgenden Optionen aktiviert:

- **Neue Position anfordern**
- **Änderung der Positionsdetails anfordern**

Sie können diese Optionen auch so konfigurieren, dass sie einen optionalen Überprüfungs- und Genehmigungsworkflow durchlaufen.

### <a name="summary"></a>Summe

Informationen im Abschnitt **Zusammenfassung** hängen von den Optionen ab, die HR in **Human-Resources-Parameter** ausgewählt hat. Auf der Registerkarte **Manager-Self-Service** der Seite **Human Resources-Parameter** können Sie Optionen für die Anzeige ablaufender Datensätze und offener Positionen konfigurieren. Durch Aktivieren dieser Optionen wird festgelegt, was Manager im Abschnitt **Zusammenfassung** sehen können.

Sie können die folgenden Kacheln für Manager konfigurieren:

- **Ablaufende Zertifikate für mein Team**
- **Für mein Team ablaufende Kennnummern**
- **Für mein Team ablaufende Proben**
- **Für mein Team ablaufende Prüfungen**
- **Für mein Team ablaufende Tests**
- **Offene Positionen für direkte und/oder erweiterte Berichte**
- **Ausstehende Anfragen für mein Team**
- **Bewertung der Teamqualifikationen**
- **Analyse der Qualifikationslücken**
- **Teamleistungserfassungen**
- **Leistungsziele des Teams**
- **Team-Leistungsüberprüfungen**
- **Ausscheidende Arbeitskräfte**

Sie können die folgenden Optionen für Manager konfigurieren, um Änderungen vorzunehmen oder Urlaubsanträge für ihre direkten Berichte hinzuzufügen:

- Bescheinigungen
- Kurse
- Ausleihartikel
- Qualifikationen
- Urlaubs- und Abwesenheitsanträge

### <a name="my-team-information"></a>Meine Teaminformationen

Über **Mein Team** können Manager direkte und erweiterte Berichte anzeigen und aktualisieren. Um auf erweiterte Berichte zuzugreifen, wählen Sie zunächst den Mitarbeiter mit den Anweisungen und anschließend **Team anzeigen** auf der Kachel aus. Alle gleichen Optionen gelten für erweiterte Berichte als direkte Berichte. 

#### <a name="summary-tab"></a>Registerkarte „Zusammenfassung“

Die Registerkarte **Zusammenfassung** bietet eine schnelle Ansicht Ihrer direkten Berichte. Wenn in einem direkten Bericht auch Mitarbeiter Bericht erstatten, wird auf der Karte die Anzahl der direkten Berichte im oberen Bereich zusammen mit einer Schaltfläche **Team anzeigen** angezeigt. Optionen über jeder Kachel gelten für den ausgewählten Mitarbeiter. Wenn Sie beispielsweise im Namen eines Mitarbeiters einen Urlaubsantrag stellen möchten, wählen Sie den Mitarbeiter aus und wählen Sie dann **Arbeitsfreie Zeit anfordern** aus. 

Wenn Sie die Schaltfläche **Details** nach Auswahl eines Mitarbeiters auswählen, werden die folgenden Optionen angezeigt:

- **Bescheinigungen**
- **Kompensation**
- **Kurse**
- **Überprüfungen**
- **Arbeitsfreie Zeit**
- **Ausgeliehene Artikel**
- **Leistungsziele**
- **Registrierte Kurse**
- **Qualifikationen**
- **Feedback senden**

Abhängig von den Einstellungen Ihrer Organisation können Sie entweder Änderungen vornehmen oder nur anzeigen.

#### <a name="position-tab"></a>Registerkarte „Position“

Die Registerkarte **Position** bietet eine zusammenfassende Ansicht der Mitarbeiter in ihrer primären Position. Name, Kachel und Abteilung werden im Überschriftenbereich jeder Kachel angezeigt. Diese Kachel umfasst Folgendes:

- **Dienstalter** – Wird im Abschnitt „Arbeitskraftzusammenfassung“ der Seite **Arbeitskraft** angezeigt.
- **Dienstjahre** – Wird auf der Grundlage des Beschäftigungsbeginns des Mitarbeiters berechnet.
- **Anzahl der vorherigen Positionen** – Durch Auswahl dieser Nummer wird basierend auf dem Positionsverlauf die Detailansicht aller zuvor gehaltenen Positionen geöffnet.
- **Geburtsdatum** – Monat und Tag des Geburtsdatums des Mitarbeiters.

Sie können Positionsdaten sowohl für direkte als auch für erweiterte Berichte anzeigen.

#### <a name="compensation-tab"></a>Registerkarte „Vergütung“

Auf der Registerkarte **Vergütung** wird das Jahresgehalt des Mitarbeiters angezeigt. Unter dem Gehaltsbetrag wird eine Firmenkennung angezeigt. Wenn ein Mitarbeiter mehr als eine Beschäftigung hat und von mehreren juristischen Personen bezahlt wird, verfügt der Mitarbeiter über mehrere Vergütungspläne. Um alle Vergütungspläne für juristische Personen ohne Unternehmenswechsel anzuzeigen, müssen Sie die Kreuzvergütung aktivieren unter **Human Resources > Gemeinsame Parameter > Erweiterter Zugriff > Unternehmensübergreifende Vergütung aktivieren**.

Um den Vergütungsverlauf anzuzeigen, wählen Sie den **Gehaltsbetrag** aus, um die Seite **Details** zu öffnen. Auf der Seite **Vergütung** werden nur aktuelle und historische feste und variable Vergütungsdatensätze angezeigt. Wenn ein Mitarbeiter mehr als eine Beschäftigung hat, können Sie zwischen Unternehmen wechseln, um den Vergütungsverlauf in jedem Unternehmen anzuzeigen, oder die unternehmensübergreifende Vergütung unter **Freigegebene Human-Resources-Parameter** aktivieren, um alle Vergütungspläne anzuzeigen.

Sie können Vergütungen sowohl für direkte als auch für erweiterte Berichte anzeigen.

#### <a name="leave-and-absence-tab"></a>Registerkarte „Urlaub und Abwesenheit“

Auf der Registerkarte **Urlaub und Abwesenheit** werden die Top-Salden für Mitarbeiter mit Aktivität angezeigt. Wählen Sie **Details** und dann **Arbeitsfreie Zeit** aus, um Maßnahmen zu ergreifen oder eine vollständige Liste der Aktivitäten anzuzeigen. Auf der Seite **Arbeitsfreie Zeit** können Sie Salden, Anfragen, genehmigte arbeitsfreie Zeit und prognostizierte Salden anzeigen, um den Mitarbeitern zu helfen, die Zeit besser zu verwalten. Abhängig von den Einstellungen Ihres Unternehmens können Sie auch eine Freistellung für Ihre Direktiven und erweiterten Berichte beantragen.

#### <a name="performance-goals-tab"></a>Registerkarte „Leistungsziele“

Die Registerkarte **Leistungsziele** fasst die Leistungsziele nach Status zusammen. Wählen Sie eine Nummer für einen Status oder wählen Sie Leistungsziele aus der Registerkarte **Details** aus, um alle Ziele für einen Mitarbeiter zu sehen. Manager und Mitarbeiter können Ziele über die Dauer des Ziels nach Bedarf aktualisieren.

Manager können alle Ziele für ihr Team über die Kachel **Teamleistungsziele** im Abschnitt **Zusammenfassung** von **Mein Team** sehen.

#### <a name="reviews-tab"></a>Registerkarte „Bewertungen“

Die Registerkarte **Bewertungen** fasst die Bewertungen des Mitarbeiters in den einzelnen Bundesstaaten zusammen: **In Bearbeitung**, **Bereit zur Überprüfung**, und **Abschließende Prüfung**. Um auf die Bewertung eines Mitarbeiters zuzugreifen, wählen Sie die Schaltfläche **Details** und wählen Sie dann die Bewertungen aus, an denen Sie zusammenarbeiten möchten. Anhand der Position einer Überprüfung im Workflow-Prozess können Sie feststellen, ob die Überprüfung zur Aktualisierung verfügbar ist. 

Sie können alle Bewertungen für ihr Team über die Kachel **Teamleistungsüberprüfung** im Abschnitt **Zusammenfassung** von **Mein Team** sehen.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
