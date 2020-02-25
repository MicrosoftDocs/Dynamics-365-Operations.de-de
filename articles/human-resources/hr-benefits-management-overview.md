---
title: Vorteilsverwaltung – Übersicht
description: Übersicht über die Vorschaufunktion für die Vorteilsverwaltung in Dynamics 365 Human Resources. Bieten Sie Ihren Mitarbeitern erweiterte Vorteilsoptionen mit einer benutzerfreundlichen Online-Erfahrung.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63db1b55bae9150dd87d9981136b96d72ffd0c59
ms.sourcegitcommit: 523049c363a999050c58d20695f1c7d151b3fd3e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029462"
---
# <a name="benefits-management-overview"></a>Vorteilsverwaltung – Übersicht

[!include [banner](includes/preview-feature.md)]

Um wettbewerbsfähig zu bleiben, müssen Sie zahlreiche Vorteile bieten, um die besten Mitarbeiter anzuwerben und zu halten. Zusätzlich zu den Standardleistungen wie Kranken‑ und Zahnzusatzversicherung möchten Sie möglicherweise auch erweiterte Dienstleistungen wie Adoptionsunterstützung, Freizeitprogramme und Aufwandsentschädigungen anbieten. Die Vorschaufunktion für die Vorteilsverwaltung in Microsoft Dynamics 365 Human Resources bietet Ihnen eine flexible Lösung, die eine Vielzahl von Vorteilsoptionen unterstützt. Human Resources umfasst auch eine benutzerfreundliche Mitarbeitererfahrung, die Ihre Angebote vorstellt.

- Mit erweiterten Vorteilsplänen können Sie einzigartige Vorteilspläne erstellen und verwalten sowie komplexe Vorteilssatztabellen und verschachtelte Stufen unterstützen. Sie können auf einfache Weise Vorteilsprogramme, Bündel und Regeln für die automatische Registrierung erstellen, um die Mitarbeitererfahrung zu vereinfachen.

- Mit Flexguthabenprogrammen können Sie die Altersvorsorge und andere Lebensereignisse anteilig unterstützen.

- Umfangreiche Berechtigungsregeln stellen sicher, dass Sie den richtigen Mitarbeitern die richtigen Vorteile zur Verfügung stellen.

- Die Online-Vorteilsregistrierung bietet Ihren Mitarbeitern eine einfache Erfahrung.

- Qualifizierte Verarbeitung von Lebensereignissen ist im Mitarbeiter-Self-Service integriert und unterstützt auch zukünftige Lebensereignisse.

Wenn Sie auf die Demodaten zugreifen möchten, müssen Sie Ihre Sandkastenumgebung erneut bereitstellen.

Sie können direktes Feedback geben oder Probleme melden an: D365BenefitsPreview@microsoft.com.

## <a name="benefits-management-known-issues"></a>Bekannte Probleme bei der Vorteilsverwaltung

### <a name="eligibility-processing"></a>Verarbeitung von Berechtigungen

Wenn Sie die Berechtigung für Vorteile ausführen, die ein 1,5-faches Gehalt, einen Prozentsatz des Gehalts und ein Pauschalbetrag als Abdeckungsbetrag verwenden, müssen Sie das Datum der **Vorteilsdetails** auf das **Mitarbeiterstartdatum** in **Beschäftigungshistorie** festlegen. Sie müssen auch **Arbeitsstunden**, **Zahlungshäufigkeit** und **Jährliches Vorteilsgehalt** einschließen. Wenn die Arbeitskraft eine feste Vergütung hat, geben Sie **Arbeitsstunden** und **Zahlungshäufigkeit** ein. Der jährliche Gehaltsbetrag wird berechnet. Wenn der Mitarbeiter fest angestellt ist, müssen Sie keine **Arbeitsstunden** eintragen. Wir empfehlen, bei der Erstellung neuer Mitarbeiter zunächst eine feste Vergütung einzugeben. So aktualisieren Sie den Datensatz mit Vorteilsdetails: Navigieren Sie zu **Arbeitskraft > Beschäftigungshistorie > Beschäftigungsdetails**. Passen Sie das Datum an das Startdatum der Arbeitskraft an.

### <a name="employee-self-service"></a>Mitarbeiter-Self-Service

Der Mitarbeiterbetrag wird bei der Aktualisierung des Abdeckungsbetrags für die Lebensversicherung nicht berechnet. Wenn einem Mitarbeiter beispielsweise eine Lebensversicherung angeboten wird, kann er bis zu 50.000 Euro Versicherungsschutz zu einem Preis von 0,36 Euro pro 1.000 Euro Versicherungsschutz auswählen.  Wenn der Mitarbeiter den Abdeckungsbetrag aktualisiert, bleiben die damit verbundenen Kosten des Mitarbeiters bei Null.

Bei einem Vorteilsplan, der nur eine einzige Auswahl dieses Plantyps zulässt, wird dem Benutzer eine Fehlermeldung angezeigt, wenn er versucht, nach Auswahl eines Plans auf einen Plan zu verzichten. Beispielsweise wählt ein Benutzer einen Krankenversicherungsplan aus und legt ihn in seinen Warenkorb. Der Benutzer wählt dann **Aufheben** für einen anderen Krankenversicherungsplan aus. Der Benutzer erhält eine Fehlermeldung.

## <a name="enable-benefits-management"></a>Vorteilsverwaltung aktivieren

Die Vorteilsverwaltung ist eine Vorschaufunktion und nur in **Sandkasten**umgebungen verfügbar. In diesen Artikeln wird beschrieben, wie Sie die Vorschaufunktionen in Human Resources aktivieren. Sie geben auch an, welche vorhandenen Funktionen in Human Resources die Vorteilsverwaltung ersetzt oder deaktiviert, sobald Sie die Vorteilsverwaltung aktivieren.

- [Funktionen verwalten](hr-admin-manage-features.md)
- [Vorschaufunktion: Vorteilsverwaltung](hr-admin-manage-features.md?preview-feature-benefits-management)

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
- [Warteperioden konfigurieren](hr-benefits-setup-waiting-periods.md)
- [Rundungsregeln einrichten](hr-benefits-setup-rounding-rules.md)
- [Mitarbeiterkategorien erstellen](hr-benefits-setup-employment-categories.md)
- [Beschäftigungstypen einrichten](hr-benefits-setup-employment-types.md)
- [Mitarbeiter-Self-Service konfigurieren](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a>Vergütungspläne erstellen

In diesen Artikeln wird gezeigt, wie Sie Vorteilspläne erstellen, einschließlich Bündeln und Flexguthabenprogrammen.

- [Vergütungspläne einrichten](hr-benefits-plans-setup.md)
- [Vergütungspläne für Arbeitskräfte erstellen](hr-benefits-plans-worker.md)
- [Flexguthabenprogramme einrichten](hr-benefits-plans-flex-credit-programs.md)
- [Zukünftige Lebensereignisse konfigurieren](hr-benefits-plans-future-life-events.md)

## <a name="process-benefit-plans"></a>Vergütungspläne verarbeiten

Sie müssen einige Ihrer Änderungen verarbeiten, um sie zu aktivieren.

- [Vergütungsberechtigung verarbeiten](hr-benefits-process-enrollment-eligibility.md)
- [Lebensereignisse verarbeiten](hr-benefits-process-life-events.md)
- [Änderungen von Lebensereignissen verarbeiten](hr-benefits-process-life-event-changes.md)
- [Lebensereignisberechtigung verarbeiten](hr-benefits-process-life-event-eligibility.md)
- [Satzänderungen verarbeiten](hr-benefits-process-rate-changes.md)

