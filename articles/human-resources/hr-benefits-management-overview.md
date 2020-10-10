---
title: Vorteilsverwaltung – Übersicht
description: Übersicht über die Vorschaufunktion für die Vorteilsverwaltung in Dynamics 365 Human Resources. Bieten Sie Ihren Mitarbeitern erweiterte Vorteilsoptionen mit einer benutzerfreundlichen Online-Erfahrung.
author: andreabichsel
manager: AnnBe
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e2e8fcdd0b6124b459c4dc073e2929418d18bcc5
ms.sourcegitcommit: 084eda1d5503be83e97e2e428e67ef5393535fab
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/17/2020
ms.locfileid: "3819764"
---
# <a name="benefits-management-overview"></a>Vorteilsverwaltung – Übersicht

Um wettbewerbsfähig zu bleiben, müssen Sie zahlreiche Vorteile bieten, um die besten Mitarbeiter anzuwerben und zu halten. Zusätzlich zu den Standardleistungen wie Kranken‑ und Zahnzusatzversicherung möchten Sie möglicherweise auch erweiterte Dienstleistungen wie Adoptionsunterstützung, Freizeitprogramme und Aufwandsentschädigungen anbieten. Die Leistungsverwaltung in Microsoft Dynamics 365 Human Resources bietet Ihnen eine flexible Lösung, die eine Vielzahl von Vorteilsoptionen unterstützt. Human Resources umfasst auch eine benutzerfreundliche Mitarbeitererfahrung, die Ihre Angebote vorstellt.

- Mit erweiterten Vorteilsplänen können Sie einzigartige Vorteilspläne erstellen und verwalten sowie komplexe Vorteilssatztabellen und verschachtelte Stufen unterstützen. Sie können auf einfache Weise Vorteilsprogramme, Bündel und Regeln für die automatische Registrierung erstellen, um die Mitarbeitererfahrung zu vereinfachen.

- Mit Flexguthabenprogrammen können Sie die Altersvorsorge und andere Lebensereignisse anteilig unterstützen.

- Umfangreiche Berechtigungsregeln stellen sicher, dass Sie den richtigen Mitarbeitern die richtigen Vorteile zur Verfügung stellen.

- Die Online-Vorteilsregistrierung bietet Ihren Mitarbeitern eine einfache Erfahrung.

- Qualifizierte Lebensereignisverarbeitung unterstützt zukünftige Lebensereignisse.

Wenn Sie auf die Demodaten zugreifen möchten, müssen Sie Ihre Sandkastenumgebung erneut bereitstellen.

## <a name="enable-benefits-management"></a>Vorteilsverwaltung aktivieren

Dieses Thema beschreibt, wie Sie die Vorschaufunktionen in Human Resources aktivieren. Er zeigt auch, welche vorhandenen Funktionen in Human Resources die Vorteilsverwaltung ersetzt oder deaktiviert, sobald Sie die Vorteilsverwaltung aktivieren.

> [!IMPORTANT]
> Nachdem Sie die Leistungsverwaltung in einer **Produktions** Umgebung aktiviert haben, können Sie diese nicht mehr deaktivieren. Wir empfehlen, das Leistungsmanagement in einer **Sandkasten** Umgebung zu aktivieren und zu testen, bevor Sie es in einer aktivieren **Produktion** Umgebung aktivieren. Es gibt erhebliche Unterschiede zwischen der alten Leistungs-Funktionalität und der neuen Leistungsverwaltungs-Funktionalität, die zusätzliche Einstellungen erfordern und vor der Inbetriebnahme getestet werden sollten.

- [Funktionen verwalten](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a>Mitarbeiterdaten konfigurieren

Bevor Sie Mitarbeiter für Leistungen anmelden können, müssen Sie die erforderlichen Informationen angeben. Sie müssen einen Mitarbeiter bei seinem Eintrittsdatum in einem **Festen Vergütungsplan** erfassen und Sie müssen die **Häufigkeit der Leistungsbezüge** unter **Beschäftigungs-Details** im Formular **Arbeitskraft** auswählen.

Wenn Sie einen Mitarbeiter haben, der eine zusätzliche Vergütung wie Provisionen erhält, können Sie einen Betrag **Jahresgehalt für Vorteile** aus dem Mitarbeiterdatensatz hinzufügen. Die Personalverwaltung wird den Betrag **Jahresgehalt für Vorteile** verwenden, wenn Deckungssummen festgelegt werden, anstatt eines festen jährlichen Vergütungsbetrags. Die **Jahresgehalt für Vorteile** müssen ab dem Startdatum des Mitarbeiters oder dem Beginn des Vorteilszeitraums gültig sein, je nachdem, welcher Zeitpunkt der letzte ist. Wenn für einen Mitarbeiter sowohl eine feste Vergütung als auch einen Betrag des Jahresgehalts für Vorteile erfasst ist, wird das Jahresgehalt für Vorteile verwendet, um die Deckungssummen zu bestimmen.

Wenn Sie einen Leistungsplan erstellen, der Sätze verwendet, die auf Geschlecht oder Alter basieren, müssen Sie ein Geburtsdatum und ein Geschlecht eingeben, damit der Mitarbeiter die Leistungskosten berechnen kann.

## <a name="configure-benefits-management"></a>Vorteilsverwaltung konfigurieren

Bevor Sie Vorteilspläne für Ihre Mitarbeiter erstellen können, müssen Sie Optionen für die Pläne konfigurieren.

- [Vorteilsverwaltungsparameter festlegen](hr-benefits-setup-parameters.md)
- [Berechtigungsregeln und -optionen konfigurieren](hr-benefits-setup-eligibility-rules.md)
- [Berechtigungsoptionen für persönliche Kontakte konfigurieren](hr-benefits-setup-contact-eligibility-options.md)
- [Abdeckungsoptionen erstellen](hr-benefits-setup-coverage-options.md)
- [Zahlungshäufigkeiten einrichten](hr-benefits-setup-payment-frequencies.md)
- [Lebensereignistypen konfigurieren](hr-benefits-setup-life-event-types.md)
- [Plantypen erstellen](hr-benefits-setup-plan-types.md)
- [Ursachencodes einrichten](hr-benefits-setup-reason-codes.md)
- [Schichtcodes einrichten](hr-benefits-setup-tier-codes.md)
- [Sätze konfigurieren](hr-benefits-setup-rates.md)
- [Abzüge konfigurieren](hr-benefits-setup-deductions.md)
- [Wartezeiten konfigurieren](hr-benefits-setup-waiting-days.md)
- [Wartezeiträume konfigurieren](hr-benefits-setup-waiting-periods.md)
- [Rundungsregeln einrichten](hr-benefits-setup-rounding-rules.md)
- [Mitarbeiterkategorien erstellen](hr-benefits-setup-employment-categories.md)
- [Beschäftigungstypen einrichten](hr-benefits-setup-employment-types.md)
- [Mitarbeiter-Self-Service konfigurieren](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a>Vergütungspläne erstellen

In diesen Artikeln wird gezeigt, wie Sie Vorteilspläne erstellen, einschließlich Bündeln und Flexguthabenprogrammen.

- [Vergütungspläne einrichten](hr-benefits-plans-setup.md)
- [Programme für flexible Kredite einrichten](hr-benefits-plans-flex-credit-programs.md)

## <a name="process-benefit-plans"></a>Vergütungspläne verarbeiten

Sie müssen einige Ihrer Änderungen verarbeiten, um sie zu aktivieren.

- [Vergütungsberechtigung verarbeiten](hr-benefits-process-enrollment-eligibility.md)
- [Lebensereignisse verarbeiten](hr-benefits-process-life-events.md)
- [Änderungen von Lebensereignissen verarbeiten](hr-benefits-process-life-event-changes.md)
- [Lebensereignisberechtigung verarbeiten](hr-benefits-process-life-event-eligibility.md)
- [Satzänderungen verarbeiten](hr-benefits-process-rate-changes.md)

