---
title: Dynamics 365 Human Resources Infrastruktur zusammenführen FAQ
description: Dieser Artikel beantwortet häufig gestellte Fragen zum Infrastruktur-Merge für Microsoft Dynamics 365 Human Resources und die Apps für Finance und Operations.
author: twheeloc
ms.date: 08/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fd71d728f9c97dc9e2c44a7e7a0e773be891b818
ms.sourcegitcommit: 6d9fcb52d723ac5022a3002e0ced8e7b56e9bc2a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/27/2022
ms.locfileid: "9203198"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>Dynamics 365 Human Resources Infrastruktur zusammenführen FAQ

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="what-is-dynamics-365-human-resources"></a>Was ist Dynamics 365 Human Resources?

Microsoft Dynamics 365 Human Resources bietet Tools, die HR-Teams dabei helfen, die organisatorische Agilität zu erhöhen, die Mitarbeitererfahrung zu verändern und HR-Programme zu optimieren, um einen Workplace zu erstellen, in dem Mitarbeiter und Unternehmen erfolgreich sind. Um mehr über Dynamics 365 Human Resources zu erfahren, siehe [Dynamics 365 Human Resources](https://dynamics.microsoft.com/human-resources/overview/).

- **Transformieren Sie die Erfahrungen Ihrer Mitarbeiter**. Binden Sie Spitzenkräfte an Ihr Unternehmen, indem Sie Managern und Mitarbeitern durch vernetzte Self-Service-Erlebnisse die Möglichkeit geben, sich zu engagieren und zu wachsen.
- **HR-Programme optimieren**. Senken Sie die Betriebskosten, und erstellen Sie personalbezogene Programme für Urlaub und Abwesenheit, Zeit, Leistungen und Vergütung.
- **Steigern Sie die organisatorische Agilität**. Ermöglichen Sie der Personalabteilung, mit der vom Unternehmen geforderten Geschicklichkeit zu arbeiten, indem Sie Dataverse und Microsoft Power Platform verwenden, um Personaldaten zu zentralisieren und Dynamics 365 Human Resources einfach zu erweitern.
- **Einblicke in die Belegschaft entdecken**. Treffen Sie datengestützte Entscheidungen, indem Sie Personendaten auf umfangreichen Dashboards analysieren und visualisieren, die auf jedem Gerät verfügbar sind.

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>Wert und Nutzen der Infrastruktur zusammenführen

### <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>Was ist Dynamics 365 Human Resources Infrastruktur zusammenführen?

Derzeit gibt es in Dynamics 365 zwei getrennte Funktionalitäten für das Personalwesen auf zwei verschiedenen Infrastrukturen:

- **Dynamics 365 Human Resources** – Eine eigenständige App, die auf einer unabhängigen Infrastruktur ausgeführt wird. Bei der Einführung dieser App wurde die Infrastruktur von anderen Dynamics 365 Vorgängen Apps getrennt. Unsere Debitor nutzen diese App, um die organisatorische Agilität zu erhöhen, HR-Programme zu optimieren, die Erfahrungen der Mitarbeiter zu verändern und Einblicke in die Belegschaft zu gewinnen.
- **HR-Modul** – Ein veralteter Satz von Funktionalitäten, der früher Teil der Unified Operations-Lizenzierung Stock Keeping Unit (SKU) war. Das HR-Modul wird auf der Finanzen und Betrieb-Infrastruktur ausgeführt, die für alle Apps des Vorgangs gleich ist. Zu diesen Apps gehören Dynamics 365 Finance, Dynamics 365 Project Operations und Dynamics 365 Supply Chain Management. Kunden haben die Funktionalitäten für das Personalwesen als Teil von Dynamics 365 Finance oder Dynamics 365 Supply Chain Management erhalten.

In den letzten drei Jahren hat Microsoft keine neuen Funktionalitäten oder Erweiterungen für das HR-Modul hinzugefügt. Stattdessen haben sich unsere Investitionen in der Roadmap auf die Dynamics 365 Human Resources App konzentriert.

Indem wir diese beiden Funktionalitäten in dieselbe Infrastruktur einbringen, können wir unseren Debitor die folgenden Vorteile bieten:

- Erweiterungen, die in den letzten drei Jahren zu Dynamics 365 Human Resources hinzugefügt wurden, einschließlich verbesserter Funktionen für Urlaub und Abwesenheit, Leistungsmanagement und Reporting.
- Verbesserte Erweiterbarkeit durch Microsoft Power Platform und die Möglichkeit, die Geschäftslogik zu erweitern, um Seiten zu personalisieren.
- Verbesserte Bereitstellung, Updates und Wartung, die in Bezug auf Application Lifecycle Management (ALM), Lifecycle Services, geografische Verfügbarkeit und mehr konsistent sind.
- Mehr technologische Innovation, da unser technisches Team gemeinsame Dienste, Tools und geringere Plattformkosten nutzt.

Von dieser Umstellung sind Debitor betroffen, die derzeit entweder Dynamics 365 Human Resources oder das veraltete HR-Modul verwenden.

## <a name="glossary-of-terms-used-in-this-faq"></a>Glossar der in dieser FAQ verwendeten Begriffe

- **Dynamics 365 Human Resources** – Unser aktuelles und zukünftiges Produkt, das dem Markt HR Funktionalitäten bietet.
- **HR-Modul** – Ein veraltetes Set von Funktionalitäten, das zuvor mit dem Unified Operations Angebot lizenziert wurde. Die Funktionalitäten sind aktiviert, wenn ein Debitor Dynamics 365 Finance oder Dynamics 365 Supply Chain Management besitzt.
- **Finanz- und Operations-Infrastruktur** – Die Entwicklungsarchitektur, die vom Operations-Portfolio verwendet wird, einschließlich Dynamics 365 Finance, Dynamics 365 Supply Chain Management und Dynamics 365 Project Operations. Diese Infrastruktur ist diejenige, die in Zukunft verwendet werden soll. In dieser FAQ bezieht sich der Begriff *gemischte Infrastruktur* auf die Finanz- und Betriebs-Umgebung.
- **Human Resources Infrastruktur** – Die Entwicklungsarchitektur, die in der Vergangenheit für die App Dynamics 365 Human Resources verwendet wurde. Das Projekt zur Zusammenlegung der Infrastruktur bringt Dynamics 365 Human Resources in die Finanzen und Betrieb Infrastruktur. Die eigenständige Infrastruktur wird nicht mehr weitergeführt.

## <a name="general-questions-about-the-infrastructure-merge"></a>Allgemeine Fragen zur Zusammenführung der Infrastruktur

### <a name="will-customers-lose-any-features-or-capabilities"></a>Verlieren Debitor irgendwelche Funktionen oder Funktionalitäten?

Unser Ziel ist es, die Auswirkungen dieser Umstellung auf den Debitor zu minimieren. Wir werden keine Funktionen oder Funktionalitäten entfernen. Es wird eine funktionale Parität zwischen Dynamics 365 Human Resources und dem HR-Modul bestehen. In Fällen, in denen eine Funktion in beiden Infrastrukturen vorhanden ist, wird die Dynamics 365 Human Resources Erfahrung verwendet.

### <a name="will-the-user-experience-change"></a>Wird sich die Benutzererfahrung ändern?

Die Benutzererfahrung wird mit der Standardplattform von Dynamics 365 übereinstimmen. Obwohl die allgemeine Bedienung des Dashboards und der Menüs ähnlich bleibt, wird sie an die Standardbedienung der Dynamics 365 Finance App angepasst. Die Navigation wird sowohl Module als auch Arbeitsbereiche umfassen, Favoriten zulassen und vieles mehr. Die Dynamics 365 Human Resources-Arbeitsbereiche, wie **Personalverwaltung** und **Personen**, werden in die Finanzen und Betrieb-Infrastruktur integriert. In Zukunft werden neue Funktionalitäten über die Funktionsverwaltung bereitgestellt, mit der Debitor neue Funktionen einsehen und entscheiden kann, welche er nutzen möchte. Weitere Informationen finden Sie unter [Übersicht über die Funktionsverwaltung](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) und [Dokumentation der Benutzeroberfläche](../fin-ops-core/fin-ops/get-started/user-interface-elements.md?toc=/dynamics365/human-resources/toc.json).

### <a name="when-will-the-dynamics-365-human-resources-infrastructure-merge-be-completed"></a>Wann wird die Zusammenführung der Dynamics 365 Human Resources-Infrastruktur abgeschlossen sein?

Die Zusammenführung der Infrastruktur wird schrittweise erfolgen, um den Debitor Zeit zu geben, die notwendigen Schritte zu planen und durchzuführen. Wir haben damit begonnen, Funktionalitäten im Dynamics 2021 Veröffentlichungszyklus 2 einzuführen. Wir planen, die gesamte Produktentwicklung für dieses Projekt bis zum Ende des Veröffentlichungszyklus 2 im Jahr 2022 abzuschließen. Beachten Sie, dass sich die Zeitpläne noch ändern können. Die aktuellsten Informationen finden Sie auf der Seite [Releasepläne](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance).

### <a name="what-training-and-resources-will-be-available-to-help-with-the-infrastructure-merge"></a>Welche Schulungen und Ressourcen werden für die Zusammenführung der Infrastruktur zur Verfügung stehen?

Wir werden Belege zur Verfügung stellen, die jeden Schritt des Prozesses der Zusammenführung von Infrastrukturen im Detail beschreiben. Wir werden bei Bedarf zusätzliche Schulungsressourcen wie Videos und Workshops bereitstellen, um Debitor und Partner bei einem reibungslosen Übergang zu unterstützen.

### <a name="will-there-be-changes-in-development-capabilities-after-the-infrastructure-merge-is-completed"></a>Werden sich die Funktionalitäten für die Entwicklung ändern, nachdem die Zusammenführung der Infrastruktur abgeschlossen ist?

Um mehr über die Funktionalitäten der Entwicklung zu erfahren, siehe [Homepage entwickeln und anpassen](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md).

## <a name="feature-availability-questions"></a>Fragen zur Verfügbarkeit von Funktionen

### <a name="will-the-linkedin-talent-hub-integration-work-on-the-finance-and-operations-infrastructure"></a>Wird die LinkedIn Talent Hub-Integration mit der Finanzen und Betrieb-Infrastruktur funktionieren?

Nein, die LinkedIn Talent Hub-Integration wird nicht Teil der fusionierten Infrastruktur sein. Öffentliche Anwendungsprogrammierschnittstellen (APIs) stehen zur Verfügung, um Integrationen mit Recruiting- und Bewerberverfolgungslösungen zu erstellen. Debitoren, die LinkedIn Talent Hub nutzen möchten, sollten mit ihrem Microsoft-Partner zusammenarbeiten, um die Integration über die bereitgestellten APIs durchzuführen. Weitere Informationen über Applicant Tracking System (ATS) Integrations-APIs finden Sie unter [Einführung in die Applicant Tracking System Integration API](./hr-admin-integration-ats-api-introduction.md).

### <a name="will-the-capabilities-that-are-currently-available-only-in-dynamics-365-human-resources-for-example-leave-management-and-benefits-management-be-available-after-the-merge-is-completed"></a>Werden die Funktionalitäten, die derzeit nur in Dynamics 365 Human Resources verfügbar sind (z.B. Urlaubsverwaltung und Leistungsmanagement), auch nach Abschluss der Zusammenführung verfügbar sein?

Ja. Alle Funktionalitäten der Anwendung Dynamics 365 Human Resources werden in die Infrastruktur von Finanzen und Betrieb übernommen. Die Funktionen werden schrittweise zur Verfügung gestellt. Für aktuelle Informationen über die Verfügbarkeit von Funktionen für die zusammengeführte Infrastruktur überprüfen Sie regelmäßig die [Releasepläne](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance).

### <a name="will-ceridian-integrations-with-dynamics-365-human-resources-be-available-after-the-infrastructure-merge-is-completed"></a>Werden Ceridian-Integrationen mit Dynamics 365 Human Resources nach Abschluss der Zusammenführung der Infrastruktur verfügbar sein?

Ceridian ist dabei, eine V2-Integration mit Dynamics 365 Human Resources zu erstellen, die die Vorteile der Payroll APIs nutzt. Die dateibasierte Integration, die derzeit in Dynamics 365 Human Resources existiert, wird nicht in die Finanzen und Betrieb-Infrastruktur migriert. Weitere Informationen finden Sie unter [Einführung der Gehaltsabrechnungs-API](./hr-admin-integration-payroll-api-introduction.md).

### <a name="will-applicant-tracking-or-onboardingoffboarding-of-employees-functionality-be-included"></a>Werden Funktionen zur Bewerberverfolgung oder zum Onboarding/Offboarding von Mitarbeitern enthalten sein?

In früheren Versionen haben wir die ATS-Integrations-API erstellt, um es Partnern und Kunden zu ermöglichen, ATS-Integrationen mit Human Resources zu erstellen. Zusätzliche ATS-bezogene Funktionen wurden in 2022 Welle 1 verfügbar. Wir werden diese APIs in zukünftigen Versionen weiter verbessern.

Die HR-Funktionalität, die derzeit in der Infrastruktur von Finanzen und Betrieb vorhanden ist, umfasst einige Funktionen für das Einstellungsmanagement, die in Dynamics 365 Human Resources nicht vorhanden sind. Wenn die Zusammenführung der Infrastruktur abgeschlossen ist, wird diese Funktionalität allen Debitor der Human Resources zur Verfügung stehen. Diese Funktion bietet eine einfache ATS-Funktionalität. Wir haben jedoch nicht vor, diese Funktionalität in Zukunft zu erweitern. Debitor-Kunden, die erweiterte Funktionen benötigen, können die Vorteile der ATS-Integrationen von Partnern nutzen. Weitere Informationen über ATS-Integrations-APIs finden Sie unter [Bewerber-Tracking-System-Integrations-API-Einführung](./hr-admin-integration-ats-api-introduction.md).

### <a name="will-the-dynamics-ax-2012-upgrade-tools-be-used-to-upgrade-the-hr-module-in-ax-2012-to-the-dynamics-365-human-resources-app"></a>Können die Dynamics AX 2012 Upgrade-Tools verwendet werden, um das HR-Modul in AX 2012 auf die Dynamics 365 Human Resources App zu aktualisieren?

Ja. Das Upgrade von Dynamics AX 2012 auf Dynamics 365 Human Resources erfolgt über denselben Upgrade-Pfad und dieselben Tools, die auch für das Upgrade auf die neueste Version anderer Apps für den Betrieb von Dynamics 365 verwendet werden, z. B. Dynamics 365 Finance oder Dynamics 365 Supply Chain Management.

Weitere Informationen über die Migration zur Finanzen und Betrieb-Infrastruktur finden Sie unter [Migration von Human Resources Debitor FAQ](./customer-migration.md).
