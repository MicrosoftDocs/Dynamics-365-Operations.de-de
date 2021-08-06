---
title: Vorteilsverwaltung – Übersicht
description: Übersicht über die Vorschaufunktion für die Vorteilsverwaltung in Dynamics 365 Human Resources. Bieten Sie Ihren Mitarbeitern erweiterte Vorteilsoptionen mit einer benutzerfreundlichen Online-Erfahrung.
author: andreabichsel
ms.date: 07/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fd3ffa08b7714d1c6019ea5987dc18ad717720a7
ms.sourcegitcommit: 08797bc43e93ea05711c5a70dd7cdb82cada667a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/13/2021
ms.locfileid: "6558320"
---
# <a name="benefits-management-overview"></a>Vorteilsverwaltung – Übersicht

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Um wettbewerbsfähig zu bleiben, müssen Sie zahlreiche Vorteile bieten, um die besten Mitarbeiter anzuwerben und zu halten. Zusätzlich zu den Standardleistungen wie Kranken‑ und Zahnzusatzversicherung möchten Sie möglicherweise auch erweiterte Dienstleistungen wie Adoptionsunterstützung, Freizeitprogramme und Aufwandsentschädigungen anbieten. Die Leistungsverwaltung in Microsoft Dynamics 365 Human Resources bietet Ihnen eine flexible Lösung, die eine Vielzahl von Vorteilsoptionen unterstützt. Human Resources umfasst auch eine benutzerfreundliche Mitarbeitererfahrung, die Ihre Angebote vorstellt.

- Mit erweiterten Vorteilsplänen können Sie einzigartige Vorteilspläne erstellen und verwalten sowie komplexe Vorteilssatztabellen und verschachtelte Stufen unterstützen. Sie können auf einfache Weise Vorteilsprogramme, Bündel und Regeln für die automatische Registrierung erstellen, um die Mitarbeitererfahrung zu vereinfachen.
- Mit Flexguthabenprogrammen können Sie die Altersvorsorge und andere Lebensereignisse anteilig unterstützen.
- Umfangreiche Berechtigungsregeln stellen sicher, dass Sie den richtigen Mitarbeitern die richtigen Vorteile zur Verfügung stellen.
- Die Online-Vorteilsregistrierung bietet Ihren Mitarbeitern eine einfache Erfahrung.
- Qualifizierte Lebensereignisverarbeitung unterstützt zukünftige Lebensereignisse.

Wenn Sie auf die Demodaten zugreifen möchten, müssen Sie Ihre Sandkastenumgebung erneut bereitstellen.

> [!NOTE]
> Sie können jetzt Formulare für die Verwaltung von Leistungen anpassen. Sie können dem Formular **Deckungsoption** für Leistungspläne jetzt angepasste Felder in Bezug auf die Sätze hinzufügen. Weitere Informationen zum Arbeiten mit angepassten Feldern finden Sie unter [Benutzerdefinierte Felder](hr-developer-custom-fields.md).
>
> ![Angepasste Felder für die Verwaltung von Leistungen ](media/hr-benefits-management-custom-fields.png)

## <a name="enable-benefits-management"></a>Vorteilsverwaltung aktivieren

Dieses Thema beschreibt, wie Sie die Vorschaufunktionen in Human Resources aktivieren. Er zeigt auch, welche vorhandenen Funktionen in Human Resources die Vorteilsverwaltung ersetzt oder welche deaktiviert werden, sobald Sie die Vorteilsverwaltung aktivieren.

> [!IMPORTANT]
> Nachdem Sie die Leistungsverwaltung in einer **Produktions** Umgebung aktiviert haben, können Sie diese nicht mehr deaktivieren. Wir empfehlen, das Leistungsmanagement in einer **Sandkasten** Umgebung zu aktivieren und zu testen, bevor Sie es in einer aktivieren **Produktion** Umgebung aktivieren. Es gibt erhebliche Unterschiede zwischen der alten Leistungs-Funktionalität und der neuen Leistungsverwaltungs-Funktionalität, die zusätzliche Einstellungen erfordern und vor der Inbetriebnahme getestet werden sollten.

Weitere Informationen finden Sie unter [Funktionsverwaltung](hr-admin-manage-features.md).

## <a name="process-overview"></a>Prozessüberblick

Der Prozess der Konfiguration von Leistungen umfasst die folgenden Aufgaben:

1.  Richten Sie die erforderlichen Leistungsinformationen ein.
2.  Richten Sie die optionalen Leistungsinformationen ein.
3.  Leistungspläne einrichten.
4.  Programme für flexible Kredite einrichten (optional).
5.  Konfigurieren Sie die erforderlichen Mitarbeiterinformationen.
6.  Konfigurieren Sie die optionalen Mitarbeiterinformationen.
7.  Verarbeiten Sie Mitarbeiter, um die Berechtigung zu bestimmen.
8.  Mitarbeiter wählen Pläne über den Mitarbeiter-Self-Service aus (optional).
9.  Bestätigen Sie die Auswahl der Mitarbeiterpläne.
10. Lebensereignisverarbeitung (optional).
11. Preisaktualisierungen (optional).

## <a name="set-up-required-benefit-information"></a>Richten Sie die erforderlichen Leistungsinformationen ein

Bevor Mitarbeiter in die Pläne aufgenommen werden können, müssen mehrere Komponenten eingerichtet werden:

- **Parameter für das Leistungsmanagement** – Diese Einstellungen werden unternehmensübergreifend geteilt. Sie können Standard-Ursachencodes festlegen, die **Leistungen Jahresgehalt** Option aktivieren, eine  Standardzahlungshäufigkeit für Neueinstellungen festlegen und Lebensereignisse aktivieren. Weitere Informationen finden Sie unter [Leistungsverwaltungsparameter festlegen](hr-benefits-setup-parameters.md).
- **Möglichkeiten zur persönlichen Kontaktaufnahme** – persönliche Ansprechpartner sind die Personen, die von den erstellten Plänen entweder abhängig oder begünstigt werden. Typischerweise sind es Kinder, Ehepartner oder Treuhandorganisationen. Weitere Informationen finden Sie unter [Berechtigungsoptionen für persönliche Kontakte konfigurieren](hr-benefits-setup-contact-eligibility-options.md).
- **Deckungsoptionen** – Legen Sie die Deckungsarten fest, die für einen Plan verfügbar sein werden. Definieren Sie insbesondere, wer abgedeckt werden soll oder wie viel Abdeckung verfügbar ist. Weitere Informationen finden Sie unter [Deckungsoptionen erstellen](hr-benefits-setup-coverage-options.md).
- **Planarten** – Richten Sie die Typen von Plänen ein, die verfügbar sind, wenn Sie einen Leistungsplan erstellen. Beispiele für Plantypen sind **Zahnbehandlung**, **Augenbehandlung**, und **Sparen**. Einige wichtige Einstellungen zum Plantyp bestimmen die Einstellungen, die im Leistungsplan verfügbar sind. Weitere Informationen finden Sie unter [Plantypen erstellen](hr-benefits-setup-plan-types.md).
- **Teilnahmebedingungen** – Berechtigungsregeln werden verwendet, um zu bestimmen, ob ein Mitarbeiter für einen Plan in Frage kommt. Jedem Leistungsplan muss mindestens eine Anspruchsberechtigungsregel zugeordnet sein. Weitere Informationen finden Sie unter [Berechtigungsregeln für persönliche Kontakte konfigurieren](hr-benefits-setup-eligibility-rules.md).
- **Zahlungsfrequenzen** – Zahlungsfrequenzen sind bei der Konfiguration von Leistungssätzen erforderlich. Die für einen Tarif verwendete Zahlungshäufigkeit hilft bei der Identifizierung des Betrags, den der Arbeitnehmer und/oder Arbeitgeber auf wöchentlicher, monatlicher oder jährlicher Basis schuldet. Weitere Informationen finden Sie unter [Zahlungshäufigkeit festlegen](hr-benefits-setup-payment-frequencies.md).
- **Preise** – Die Tarife legen fest, wie viel eine Leistung entweder dem Arbeitnehmer oder dem Arbeitgeber kostet. Soll einem Mitarbeiter Geld zurückgezahlt werden (z. B. eine Gutschrift für eine Fitnessstudio-Mitgliedschaft), wird ein negativer Satz eingetragen. Weitere Informationen finden Sie unter [Sätze kKnfigurieren](hr-benefits-setup-rates.md).
- **Stufentarife** – Tarifsätze werden verwendet, wenn sich ein Satz aufgrund bestimmter Kriterien ändern muss. Der gebräuchlichste Tarifsatz ist eine einzelne Stufe, die auf dem Alter basiert. Es können jedoch auch doppelstufige Tarife eingerichtet werden, bei denen sich der Tarif je nach Geschlecht, Alter oder anderen Kriterien ändern kann.
- **Abzüge** – Die Abzüge sind im Wesentlichen die Kopfzeileninformationen/Codes, die an das Abrechnungssystem weitergegeben werden, um den Abzug für die Leistung zu identifizieren. Sie müssen diese Abzüge einrichten, da sie im Leistungsplan erforderlich sind. Weitere Informationen finden Sie unter [Konfigurieren von Abzügen](hr-benefits-setup-deductions.md).
- **Leistungszeiträume** – Ein Leistungszeitraum ist der Zeitraum, in dem Arbeitnehmer Leistungsschutz haben. Es wird auch als Planjahr bezeichnet. Hier werden auch die offenen Beitrittsfristen eingerichtet.

## <a name="set-up-optional-benefit-information"></a>Richten Sie die optionalen Leistungsinformationen ein

Die folgenden Komponenten müssen nicht eingerichtet werden, um einen Leistungsplan zu erstellen:

- **Programme** – Ein Programm ist eine Reihe von Leistungen, die denselben Anspruchsvoraussetzungen unterliegen. Zum Beispiel könnte jeder in der Verkaufsabteilung ein Handy bekommen.
- **Bündel** – Ein Paket ist eine Gruppe von Vorteilen, bei der ein Plan ausgewählt werden muss, bevor die Option zur Auswahl zusätzlicher Pläne verfügbar ist. Beispielsweise kann ein Krankenversicherungsplan mit hohem Selbstbehalt mit einem Gesundheitssparplan (HSA) gebündelt werden.
- **Arten von Lebensereignissen** – Lebensereignisse sind Ereignisse, die eine Änderung des Versicherungsschutzes eines Mitarbeiters ermöglichen. Lebensereignistypen sind mit einem Plantyp verknüpft. Eine Krankenversicherungsart kann beispielsweise Planänderungen aufgrund einer Geburt oder Adoption oder aufgrund einer Änderung des Familienstands zulassen. Ein Versicherungsplantyp lässt jedoch möglicherweise keine Änderungen aufgrund von Lebensereignissen zu. Weitere Informationen finden Sie unter [Konfigurieren der Lebensereignistypen](hr-benefits-setup-life-event-types.md).
- **Wartezeiten und Wartezeiten** – In einem Leistungsplan kann eine Deckungswartezeit festgelegt werden. Beispielsweise kann sich ein neu eingestellter Mitarbeiter möglicherweise erst nach drei Monaten Beschäftigung in ein 401 (k) einschreiben. In diesem Fall beträgt die Wartezeit drei Monate. Wartetage werden in der Wartefrist verwendet, wenn Neuanmeldungen nur an einem bestimmten Tag des Monats bearbeitet und beim Anbieter eingereicht werden können. Wenn beispielsweise 401(k)-Anmeldungen nur am 15. des Monats bearbeitet werden können, beträgt die festgelegte Wartezeit nach drei Monaten Beschäftigung drei Monate und der Wartetag ist der fünfzehnte. Weitere Informationen finden Sie unter [Wartetage konfigurieren](hr-benefits-setup-waiting-days.md) und [Wartezeiten konfigurieren](hr-benefits-setup-waiting-periods.md).
- **Ursachencodes** – Ursachencodes werden verwendet, um zu erklären, warum sich eine Leistung für einen Mitarbeiter ändern könnte. Weitere Informationen finden Sie unter [Einrichten von Ursachencodes](hr-benefits-setup-reason-codes.md).

## <a name="set-up-benefit-plans"></a>Vergütungspläne einrichten

Wenn Sie einen Leistungsplan einrichten, müssen Sie die folgenden Schritte ausführen, bevor Mitarbeiter aufgenommen werden können:

- Zuweisen einer Vergütungsperiode.
- Abdeckungsoptionen anhängen.
- Legen Sie ein Gültig-von- und Gültig-bis-Datum auf der Reigisterkarte **Allgemein** fest.
- Weisen Sie mindestens eine Berechtigungsregel zu.
- Legen Sie die Registerkarte **Registrierung zulassen/fortsetzen** im Feld **Installieren** fest.

Weitere Informationen zum Einrichten von Leistungsplänen finden Sie unter [Leistungspläne einrichten](hr-benefits-plans-setup.md).

## <a name="set-up-flex-credit-programs-optional"></a>Programme für flexible Kredite einrichten (optional)

Sie können Flexguthabenprogramme verwenden, um Mitarbeiter für Vorteile gemäß einer festgelegten Höhe von Flexguthaben zu registrieren. Mitarbeiter können wählen, wie ihr Flexguthaben zugeordnet wird. Wenn Mitarbeiter beispielsweise bereits in der Krankenversicherung ihres Ehepartners versichert sind, müssen sie ihre Guthaben nicht für die Krankenversicherung verwenden. Daher möchten sie sie möglicherweise stattdessen für andere Vorteile verwenden. Weitere Informationen zu flexiblen Gutschriftenprogrammen finden Sie unter [Flexible Gutschriftenprogramme einrichten](hr-benefits-plans-flex-credit-programs.md).

## <a name="configure-required-employee-information"></a>Konfigurieren Sie die erforderlichen Mitarbeiterinformationen

Bevor Sie Mitarbeiter für Leistungen anmelden können, müssen Sie dafür die erforderlichen Informationen angeben. Jeder Mitarbeiter muss eine Stelle haben. Sie müssen Mitarbeiter zu ihrem Eintrittsdatum in einen festen Vergütungsplan aufnehmen oder sie müssen einen jährlichen Gehaltsbetrag für Sozialleistungen haben. Außerdem müssen Sie im Abschnitt **Beschäftigung-Details** auf der Seite **Arbeitskraft** einen Wert im Feld **Häufigkeit der Leistungszahlung** eingeben.

Wenn Sie einen Mitarbeiter haben, der eine zusätzliche Vergütung wie Provisionen erhält, können Sie einen Betrag **Jahresgehalt für Vorteile** aus dem Mitarbeiterdatensatz hinzufügen. Die Personalverwaltung wird den Betrag **Jahresgehalt für Vorteile** verwenden, wenn Deckungssummen festgelegt werden, anstatt eines festen jährlichen Vergütungsbetrags. Das **Jahresgehalt für Vorteile** muss ab dem Startdatum des Mitarbeiters oder dem Beginn des Vorteilszeitraums gültig sein, je nachdem, welcher Zeitpunkt der letzte ist. Wenn für einen Mitarbeiter sowohl eine feste Vergütung als auch einen Betrag des Jahresgehalts für Vorteile erfasst ist, wird das Jahresgehalt für Vorteile verwendet, um die Deckungssummen zu bestimmen.

## <a name="configure-optional-employee-information"></a>Konfigurieren Sie die optionalen Mitarbeiterinformationen

Wenn Sie einen Leistungsplan erstellen, der Sätze verwendet, die auf Geschlecht oder Alter basieren, müssen Sie ein Geburtsdatum und ein Geschlecht eingeben, damit der Mitarbeiter die Leistungskosten berechnen kann.

## <a name="process-employees-to-determine-eligibility"></a>Verarbeiten Sie Mitarbeiter, um die Berechtigung zu bestimmen

Bevor Mitarbeiter in Pläne aufgenommen werden können, wird eine Berechtigungsverarbeitung durchgeführt, um zu bestimmen, für welche Pläne sie berechtigt sind. Sie können die Ergebnisse des Berechtigungsprozesses in der Prozessergebnisanzeige anzeigen. Weitere Informationen finden Sie unter [Beitrittsprozessberechtigung](hr-benefits-process-enrollment-eligibility.md).

## <a name="employees-select-plans-via-employee-self-service-optional"></a>Mitarbeiter wählen Pläne über den Mitarbeiter-Self-Service aus (optional)

Wenn eine offene Registrierung erfolgt, Mitarbeiter neu eingestellt werden oder ein Lebensereignis eintritt, können Mitarbeiter ihre Leistungen über den Mitarbeiter-Self-Service auswählen oder aktualisieren. Weitere Informationen finden Sie unter [Mitarbeiter Self-Service konfigurieren](hr-benefits-setup-employee-self-service.md).

## <a name="confirm-employee-plan-selections"></a>Bestätigen Sie die Auswahl der Mitarbeiterpläne

Die von den Arbeitnehmern ausgewählten Leistungen müssen bestätigt werden, bevor die Arbeitnehmer als eingeschrieben gelten. Leistungen können auch im Namen eines Mitarbeiters ausgewählt werden. Um Leistungen auszuwählen oder zu bestätigen, wählen Sie auf der Seite **Mitarbeiter** auf der Registerkarte **Leistungen** **Leistungspläne für Arbeitnehmer** aus. Um Leistungen für mehrere Mitarbeiter auszuwählen oder zu bestätigen, verwenden Sie die Seite **Massenaktualisierung für Arbeitnehmerleistungspläne**.

## <a name="life-event-processing-optional"></a>Lebensereignisverarbeitung (optional)

Während des Mitarbeiterlebenszyklus kann jeder Mitarbeiter verschiedene Lebensereignisse erleben, wie z. B. Heirat, Beschäftigungswechsel oder Änderungen von Angehörigen oder Anspruchsberechtigten. Um Lebensereignisse zu verwenden, müssen Sie sie auf der Seite **Gemeinsame Parameter der Personalabteilung** aktivieren. Richten Sie Lebensereignistypen und Lebensereignisoptionen für Plantypen ein.

Bevor Sie Lebensereignisse verarbeiten können, müssen Sie mindestens einmal während einer Einstellungsperiode eine offene Registrierung durchgeführt haben. In den USA erfolgt die offene Registrierung in der Regel einmal pro Jahr. Außerhalb der USA kann eine offene Registrierung zum Zeitpunkt der Einstellung durchgeführt werden. Die Verarbeitung von Lebensereignissen erfordert nicht, dass Arbeitnehmer einen Leistungsplan auswählen. Die Arbeitnehmer müssen jedoch in die offene Einschreibungsbearbeitung einbezogen worden sein. Weitere Informationen finden Sie in folgenden Themen:

- [Lebensereignisse verarbeiten](hr-benefits-process-life-events.md)
- [Änderungen von Lebensereignissen verarbeiten](hr-benefits-process-life-event-changes.md)
- [Lebensereignisberechtigung verarbeiten](hr-benefits-process-life-event-eligibility.md)

## <a name="rate-updates-optional"></a>Preisaktualisierungen (optional)

Manchmal ändert sich der Satz einer Leistung während des Planzeitraums. Um die Tarife für bereits im Plan angemeldete Mitarbeiter zu aktualisieren, müssen Sie die Tarifänderungen bearbeiten. Weitere Informationen finden Sie unter [Prozesstarifänderungen](hr-benefits-process-rate-changes.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
