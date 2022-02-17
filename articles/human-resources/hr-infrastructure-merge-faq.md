---
title: Dynamics 365 Human Resources Infrastruktur zusammenführen FAQ
description: Dieses Thema beantwortet häufig gestellte Fragen zur Infrastruktur-Zusammenführung für Microsoft Dynamics 365 Human Resources und Apps für Finanzen und Betrieb.
author: twheeloc
ms.date: 08/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c022bb15975a1411230d28067a2225c95c0573bf
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062724"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>Dynamics 365 Human Resources Infrastruktur zusammenführen FAQ

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Dieses Thema beantwortet häufig gestellte Fragen zur Infrastruktur-Zusammenführung für Microsoft Dynamics 365 Human Resources und Apps für Finanzen und Betrieb.

## <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>Was ist Dynamics 365 Human Resources Infrastruktur zusammenführen?

Dynamics 365 Human Resources ist eine eigenständige Anwendung, die eine andere Infrastruktur nutzt als andere Apps für Finanzen und Betrieb, wie z.B. Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, und Dynamics 365 Project Operations. Durch die Zusammenführung der Infrastruktur wird Dynamics 365 Human Resources in dieselbe Infrastruktur wie andere Apps für Finanzen und Betrieb gebracht.

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>Wert und Nutzen der Infrastruktur zusammenführen

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-what-benefits-will-we-see-from-these-changes"></a>Meine Organisation verwendet Dynamics 365 Human Resources um seine HR-Aktivitäten zu verwalten. Welche Vorteile werden wir von diesen Veränderungen sehen?

- Diese Änderungen beseitigen die Verwirrung, die durch mehrere festgelegte Funktionalitäten für Human Resources (HR) in Dynamics 365 entsteht.
- Sie bieten sowohl Microsoft Power Platform Erweiterbarkeit und eine Möglichkeit, die Geschäftslogik und die Funktionsoptionen zu erweitern.
- Sie sorgen für Konsistenz zwischen Dynamics 365 Human Resources und anderen Apps für Finanzen und Betrieb in Bezug auf Application Lifecycle Management (ALM), Microsoft Dynamics Lifecycle Services (LCS), geografische Verfügbarkeit, Erweiterbarkeit und mehr.
- Sie ermöglichen Ihnen die Nutzung von Shared Services und Tools und helfen Ihnen, Kosten zu senken.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-benefits-will-we-see-from-these-changes"></a>Meine Organisation verwendet das Human Resources Modul in Dynamics 365 Finance, Supply Chain Management, Commerce oder Project Operations. Welche Vorteile werden wir von diesen Veränderungen sehen?

Die Fähigkeiten und Investitionen, die in Dynamics 365 Human Resources gemacht wurden, stehen nun Kunden zur Verfügung, die das HR-Modul in Dynamics 365 Finance verwenden. Einige dieser Funktionen umfassen Urlaubs- und Abwesenheitsmanagement, Leistungsmanagement und Aufgabenmanagement.

### <a name="will-i-lose-any-features-or-capabilities-that-i-currently-use"></a>Verliere ich alle Funktionen oder Fähigkeiten, die ich derzeit verwende?

Es wird eine funktionale Parität zwischen Dynamics 365 Human Resources und dem HR-Modul in Apps für Finanzen und Betrieb geben. Dynamics 365 Human Resources hat Vorrang für ähnliche Funktionen. Weitere Informationen finden Sie unter [Funktionsverwaltung – Übersicht](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="will-the-experience-change-for-my-users"></a>Wird sich die Erfahrung für meine Benutzer ändern?

Die neuen HR-Funktionen werden über die Funktions-Verwaltung verwaltet. Die Kunden entscheiden, ob sie sie aufnehmen möchten. In einigen Fällen können die Funktionen geändert werden. In diesen Fällen werden Unterlagen zur Verfügung gestellt.

### <a name="how-does-this-change-affect-me-if-i-am-an-existing-customer-and-i-use-both-the-hr-module-on-the-finance-and-operations-infrastructure-and-dynamics-365-human-resources-through-custom-integrations"></a>Wie wirkt sich diese Änderung auf mich aus, wenn ich ein bestehender Debitor bin und sowohl das HR-Modul auf der Finance und Operations-Infrastruktur als auch Dynamics 365 Human Resources über angepasste Integrationen verwende?

Benutzerdefinierte Integrationen zwischen Dynamics 365 Human Resources und dem HR-Modul in Dynamics 365 Finance wird nicht mehr benötigt. Alle HR-Daten werden in der gleichen Datenbank gespeichert wie die anderen Apps für Finanzen und Betrieb.

## <a name="migration-from-dynamics-365-human-resources-to-finance-and-operations-apps"></a>Migration von Dynamics 365 Human Resources zu Apps für Finanzen und Betrieb

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-hr-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>Meine Organisation verwendet Dynamics 365 Human Resources um seine HR-Aktivitäten zu verwalten. Was müssen wir planen, um auf die neue Erfahrung zu migrieren?

Wenn Ihr Unternehmen Dynamics 365 Human Resources verwendet, aber keine anderen Apps für Finanzen und Betrieb einsetzt, wird Ihre Umgebung für Human Resources auf die neue Infrastruktur migriert. Ein Großteil dieses Migrationsprozesses wird automatisiert. Es werden Prozesse eingerichtet, um Ihre Datenbank zu migrieren und mit der neuen Infrastruktur zu synchronisieren.

Darüber hinaus werden Tools bereitgestellt, mit denen Sie den Migrationsprozess testen und Ihre Daten und Erfahrungen validieren können, bevor Sie Ihre Produktionsumgebung migrieren.

Wenn Ihr Unternehmen sowohl Dynamics 365 Human Resources als auch andere Apps für Finanzen und Betrieb verwendet, sollten Sie mehr Zeit für die Validierung einplanen, um sicherzustellen, dass Ihre Daten korrekt in die neue Umgebung migriert werden. Bei der Migration auf die neue Infrastruktur werden die Daten aus Ihrer Human Resources Umgebung mit Ihrer Finance und Operations Umgebung zusammengeführt. Widersprüchliche Daten erfordern eine Benutzereingabe, um zu bestimmen, wie der Konflikt aufgelöst werden soll. Benutzer und Administratoren müssen die Datenzuordnungen bei Konflikten verwalten und die Migration in Sandbox-Umgebungen vor der Migration von Produktionsumgebungen testen.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>Meine Organisation verwendet das Human Resources Modul in Dynamics 365 Finance, Supply Chain Management, Commerce oder Project Operations. Was müssen wir planen, um auf die neue Erfahrung zu migrieren?

Für Organisationen, die das HR-Modul in Apps für Finanzen und Betrieb verwenden, werden die neuen Funktionen von Dynamics 365 Human Resources über den Standardprozess für One Version Updates auf Ihre Umgebung angewendet. Sie können davon ausgehen, dass die neuen Funktionen in Ihrer Umgebung in jedem Update verfügbar sind. Sie können die Funktionsverwaltung verwenden, um neue Funktionen einzuschalten, sollten aber eine Validierung dieser Funktionen einplanen. Befolgen Sie die Prozesse, die Sie zum Überprüfen anderer Updates für Ihre Umgebung eingerichtet haben. Weitere Informationen darüber, wie Updates auf Apps für Finanzen und Betrieb angewendet werden, finden Sie unter [One Version Übersicht](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="when-will-my-organization-be-migrated"></a>Wann wird meine Organisation migriert?

Die Migration für jede Organisation hängt von ihrer aktuellen Konfiguration und ihrer Bereitschaft zur Migration auf die neue Infrastruktur ab. Diese Termine können sich ändern.

- Organisationen, die das HR-Modul in Apps für Finanzen und Betrieb verwenden, erhalten die HR-Funktionalität für Dynamics 365 Human Resources im Rahmen des regulären Aktualisierungsprozesses von One Version. Es ist geplant, dass die neuen Funktionen ab Januar 2022 allgemein verfügbar sein werden.
- Organisationen, die nur Dynamics 365 Human Resources verwenden, werden Zugriff auf Migrationstools haben, so dass sie ab Mitte 2022 mit den Tests beginnen und die Migration starten können. Das Datum, bis zu dem die Migration auf die neue Infrastruktur abgeschlossen sein muss, steht noch nicht fest. Es dauert jedoch mindestens ein Jahr nach dem Datum, an dem die Migrationstools verfügbar sind.
- Organisationen, die sowohl Dynamics 365 Human Resources als auch andere Apps für Finanzen und Betrieb verwenden, werden Zugriff auf Migrationstools haben, sodass sie ab Ende 2022 mit den Tests und der Migration beginnen können. Das Datum, bis zu dem die Migration auf die neue Infrastruktur abgeschlossen sein muss, steht noch nicht fest. Es dauert jedoch mindestens ein Jahr nach dem Datum, an dem die Migrationstools verfügbar sind.

Weitere Informationen zu den neuen Funktionen für Dynamics 365 Human Resources finden Sie unter [Was ist in Human Resources neu oder hat geändert](./hr-admin-whats-new.md).

### <a name="my-organization-has-not-yet-gone-live-on-dynamics-365-human-resources-should-we-go-live-with-the-human-resources-module-in-the-finance-and-operations-apps-or-with-the-dynamics-365-human-resources-app-on-the-legacy-infrastructure"></a>Meine Organisation ist noch nicht mit Dynamics 365 Human Resources live gegangen. Sollen wir mit dem Human Resources Modul in den Apps für Finanzen und Betrieb oder mit der Dynamics 365 Human Resources App auf der veralteten Infrastruktur live gehen?

Wichtige zu berücksichtigende Artikel sind, welche HR-Funktionalität benötigt wird und wann diese Funktionalität in der neuen Infrastruktur verfügbar sein wird. Wenn die Organisation die Kernfunktionalität für die Personalverwaltung benötigt, ist diese derzeit im HR-Modul der Apps für Finanzen und Betrieb in der neuen Infrastruktur verfügbar. Die Parität der Funktionen zwischen dem HR-Modul der Apps für Finanzen und Betrieb und der App Dynamics 365 Human Resources wird für die Version 10.0.25 erwartet, die voraussichtlich im März 2022 allgemein verfügbar sein wird. Funktionen wie die Integration der Teams App und der Dataverse-Entitäten werden in späteren Versionen verfügbar sein.

Wenn die von der Organisation benötigten HR-Funktionen in der neuen Infrastruktur innerhalb des Zeitrahmens, in dem die Organisation in Betrieb geht, verfügbar sein werden, ist es möglicherweise einfacher, mit dem Human Resources-Modul in den Apps für Finanzen und Betrieb in Betrieb zu gehen. Dies wird zu einer einfacheren Migration führen, da es sich um ein Standard-Anwendungs-Upgrade auf die Dynamics 365 Human Resources-Anwendung handelt und der Debitor bereits auf der neuen Infrastruktur ist. Wenn sich das Unternehmen entscheidet, mit der Dynamics 365 Human Resources-Anwendung auf der veralteten Infrastruktur live zu gehen, ist eine Migration der Umgebung auf die neue Infrastruktur erforderlich. Dies kann vermieden werden, indem man auf der neuen Infrastruktur live geht.

### <a name="i-am-using-new-capabilities-that-are-available-only-in-dynamics-365-human-resources-such-as-leave-and-absence-and-benefits-management-will-these-capabilities-now-be-available-in-the-human-resources-module-on-the-finance-and-operations-infrastructure-too"></a>Ich verwende neue Funktionen, die nur in Dynamics 365 Human Resources verfügbar sind (wie zum Beispiel **Urlaub und Abwesenheit** und **Leistungsmanagement**). Werden diese Funktionalitäten nun auch im Modul Human Resources in der Infrastruktur von Finance und Operations verfügbar sein?

Ja, alle Module von Dynamics 365 Human Resources werden wie bisher in den Apps Finance und Operations funktionieren, und es wird eine 100-prozentige Parität der Funktionen geben. Als Teil der allgemeinen Migrationsstrategie für Kunden, die diese Funktionalitäten derzeit in HR nutzen, werden die Debitorendaten so migriert, dass sie weiterhin in der Finance und Operations-Infrastruktur funktionieren.

### <a name="i-use-the-new-dynamics-365-human-resources-benefits-management-capabilities-ive-built-custom-integrations-with-the-hr-module-on-the-finance-and-operations-infrastructure-so-that-i-can-take-advantage-of-the-payroll-capabilities-by-using-benefits-data-will-these-custom-integrations-be-required-going-forward"></a>Ich benutze die neue Funktionalitäten Dynamics 365 Human Resources Leistungsmanagements. Ich habe angepasste Integrationen mit dem HR-Modul auf der Infrastruktur von Finance und Operations erstellt, sodass ich die Funktionalitäten der Gehaltsabrechnung durch die Verwendung von Leistungsdaten nutzen kann. Werden diese benutzerdefinierten Integrationen in Zukunft erforderlich sein?

Im Rahmen der Zusammenführung der Infrastruktur werden die Personaldaten in dieselbe Datenbank wie andere Apps für Finanzen und Betrieb gebracht. Die Integration zwischen Modulen in Apps für Finanzen und Betrieb wird nicht mehr erforderlich sein.

### <a name="my-organization-uses-one-or-more-isv-solutions-with-dynamics-365-human-resources-will-our-isv-solutions-be-migrated-automatically"></a>Meine Organisation verwendet eine oder mehrere ISV-Lösungen mit Dynamics 365 Human Resources. Werden unsere ISV-Lösungen automatisch migriert?

Die Migrationserfahrung für jede Lösung eines unabhängigen Softwareanbieters (ISV) variiert je nach Integrationsmethode der Lösung. Microsoft wird eng mit ISVs zusammenarbeiten, um einen reibungslosen Übergang zur neuen Infrastruktur zu gewährleisten.

### <a name="my-organization-uses-linkedin-talent-hub-integration-with-dynamics-365-human-resources-will-this-integration-continue-to-work-after-the-infrastructure-change-is-completed"></a>Meine Organisation verwendet die LinkedIn Talent Hub-Integration mit Dynamics 365 Human Resources. Funktioniert diese Integration auch nach Abschluss der Infrastrukturänderung?

Nein, die LinkedIn Talent Hub-Integration wird nach der Migration auf die neue Infrastruktur nicht mehr funktionieren. Der Dienst für die LinkedIn Talent Hub-Integration wird mit der veralteten Dynamics 365 Human Resources-Infrastruktur außer Betrieb genommen.

### <a name="my-organization-uses-the-human-resources-app-for-teams-will-the-app-continue-to-work-after-the-infrastructure-change-is-completed"></a>Meine Organisation verwendet die Human Resources App für Teams. Funktioniert die App auch nach Abschluss der Infrastrukturänderung?

Ja, die Human Resources App für Teams funktioniert auch nach der Migration auf die neue Infrastruktur.

### <a name="my-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-our-custom-security-still-be-applied-after-the-infrastructure-change-is-completed"></a>Meine Organisation hat benutzerdefinierte Sicherheit in Dynamics 365 Human Resources konfiguriert. Wird unsere benutzerdefinierte Sicherheit nach Abschluss der Infrastrukturänderung weiterhin angewendet?

Ja, benutzerdefinierte Sicherheitskonfigurationen werden in die Datenmigration in die neue Infrastruktur einbezogen.

### <a name="we-are-using-data-integrator-to-move-data-between-dynamics-365-human-resources-and-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected"></a>Wir verwenden Data Integrator, um Daten zwischen den Apps Dynamics 365 Human Resources und Finance und Operations zu verschieben. Wie werden die Daten beeinflusst, die derzeit integriert werden?

HR-Daten, die sich derzeit in Dynamics 365 Human Resources befinden, werden mit Dataverse synchronisiert. Data Integrator kann dann für eine einseitige Synchronisierung mit Apps für Finanzen und Betrieb verwendet werden. Nach der Migration auf die neue Infrastruktur werden die HR-Daten in den Apps Finance und Operations nativ sein. Data Integrator wird nicht mehr benötigt, um die Daten zwischen Apps für Finanzen und Betrieb und Human Resources zu synchronisieren.

Die jetzige Dataverse native Datentabellen für Human Resources werden weiterhin die Daten aus der Umgebung auf der neuen Infrastruktur synchronisieren. Die Entitäten werden konvertiert, um Duales Schreiben zu unterstützen. Alle anderen Datenintegrationen, die über Data Integrator für diese Tabellen für andere Dynamics 365-Apps konfiguriert wurden, funktionieren weiterhin so, wie sie derzeit konfiguriert sind.

### <a name="we-are-using-dual-write-to-move-hr-data-between-dataverse-and-other-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected-by-the-migration-to-the-new-infrastructure"></a>Wir verwenden duales Schreiben, um HR-Daten zwischen Dataverse und anderen Apps für Finanzen und Betrieb zu verschieben. Wie werden die Daten, die derzeit integriert werden, von der Migration auf die neue Infrastruktur beeinflusst?

Die HR-Daten werden den Apps Finance und Operations in der Umgebung auf der neuen Infrastruktur zugewiesen. Dual-Write wird verwendet, um HR-Daten zwischen der neuen Umgebung und der Dataverse-Umgebung zu verschieben.

### <a name="we-have-built-custom-integrations-from-dynamics-365-human-resources-to-one-or-more-external-systems-will-we-have-to-develop-new-integrations-after-the-infrastructure-change-is-completed"></a>Wir haben benutzerdefinierte Integrationen erstellt von Dynamics 365 Human Resources an ein oder mehrere externe Systeme. Müssen wir neue Integrationen entwickeln, nachdem der Infrastrukturwechsel vollzogen ist?

Dies hängt vom Integrationsendpunkt ab. Weitere Informationen zu den Integrationstechnologien, die in Apps für Finanzen und Betrieb verfügbar sind, und zur Auswahl der besten Integrationstechnologie finden Sie unter [Integrationsübersicht](../fin-ops-core/dev-itpro/data-entities/integration-overview.md).

### <a name="we-have-extended-dataverse-for-dynamics-365-human-resources-will-these-extensions-be-migrated-automatically"></a>Wir haben Dataverse für Dynamics 365 Human Resources verlängert. Werden diese Erweiterungen automatisch migriert?

Wenn die Umgebungen Dynamics 365 Human Resources und Finance und Operations, die in der Umgebung auf der neuen Infrastruktur zusammengeführt werden, mit derselben Dataverse-Umgebung verbunden sind, werden die beiden Apps nach der Migration weiterhin mit derselben Dataverse-Umgebung verbunden sein. Für alle Dataverse-Erweiterungen wird keine Migration erforderlich sein.

Wenn jedoch die Umgebungen Dynamics 365 Human Resources und Finance und Operations derzeit mit separaten Dataverse-Umgebungen verbunden sind, müssen die beiden Dataverse-Umgebungen zusammengeführt werden, sodass sie mit einer einzigen Umgebung auf der neuen Infrastruktur verbunden sind. Für diese Dataverse Migration können die Dataverse Tabellen, die in den Human Resources-Lösungen standardmäßig enthalten sind, mit der neuen Dataverse Umgebung verbunden und .erneut synchronisiert werden. Alle Erweiterungen der Dataverse-Umgebung werden nicht automatisch migriert, sondern müssen in der neuen Umgebung neu bereitgestellt werden. Wir empfehlen Ihnen, verwaltete Lösungen zu verwenden, um Ihre Dataverse Erweiterungen zu verwalten. Weitere Informationen finden Sie unter [Einführung in Lösungen](/powerapps/developer/data-platform/introduction-solutions).

### <a name="we-have-configured-microsoft-power-automate-flows-andor-microsoft-power-apps-to-work-with-dynamics-365-human-resources-will-these-microsoft-power-platform-components-be-migrated-and-work-automatically-after-the-infrastructure-change-is-completed"></a>Wir haben Microsoft Power Automate Flows und/oder Microsoft Power Apps für das Arbeiten mit Dynamics 365 Human Resources konfiguriert. Werden diese Microsoft Power Platform Komponenten migriert werden und nach Abschluss der Infrastrukturänderung automatisch funktionieren?

Power Apps, Power Automate Flows und andere Microsoft Power Platform Anpassungen sind ähnlich wie Dataverse Erweiterungen. Ob sie nach der Migration auf die neue Infrastruktur automatisch funktionieren, hängt davon ab, ob die Human Resources App und die Apps für Finanzen und Betrieb vor der Migration mit der gleichen Power Apps-Umgebung verbunden sind.

Wenn die Apps derzeit mit derselben Power Apps Umgebung verbunden sind, werden sie auch weiterhin mit der Power Apps Umgebung nach der Migration auf die neue Infrastruktur verbunden sein. In diesem Fall funktionieren Power Apps, Power Automate Flows und andere Microsoft Power Platform Anpassungen weiterhin ohne zusätzliche Konfiguration. Wir empfehlen Ihnen, verwaltete Lösungen zu verwenden, um Ihre Anwendungserweiterungen in Dataverse zu verwalten. Weitere Informationen finden Sie unter [Einführung in Lösungen](/powerapps/developer/data-platform/introduction-solutions).

Wenn jedoch die Human Resources App und die Apps für Finanzen und Betrieb mit separaten Power Apps-Umgebungen verbunden sind, müssen sie im Rahmen der Migration zusammengeführt werden. Diese Aufgabe erfordert, dass alle Power Apps und andere Anpassungen in der neuen Umgebung neu bereitgestellt werden.

### <a name="we-have-enabled-dataverse-virtual-tables-for-dynamics-365-human-resources-what-will-happen-to-these-tables-during-the-migration"></a>Wir haben Dataverse virtuelle Tabellen für Dynamics 365 Human Resources aktiviert. Was passiert mit diesen Tabellen während der Migration?

Wenn die Umgebung der neuen Infrastruktur nach der Migration weiterhin mit der Dataverse Umgebung verbunden bleibt, mit der sie aktuell mit Dynamics 365 Human Resources verbunden ist, funktionieren die Dataverse virtuellen Tabellen, die in dieser Umgebung generiert wurden, weiterhin ohne zusätzliche Konfiguration.

Wenn die Umgebung der neuen Infrastruktur jedoch mit nach der Migration mit einer anderen Dataverse Umgebung verbunden ist, müssen die virtuellen Tabellen in der neuen Dataverse Umgebung erneut generiert werden.

### <a name="we-have-developed-an-integration-by-using-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-will-these-integrations-continue-to-work-after-the-infrastructure-change-is-completed"></a>Wir haben eine Integration entwickelt, indem wir das Bewerber-Verfolgungs-System (ATS) API, Gehaltsabrechnungs-API und Dataverse virtuelle Tabellen für Dynamics 365 Human Resources oder andere Entitäten in der Dataverse Web-API verwenden. Funktionieren diese Integrationen auch nach Abschluss der Infrastrukturänderung?

Wenn die Umgebung der neuen Infrastruktur nach der Migration weiterhin mit der Dataverse Umgebung verbunden bleibt, mit der sie aktuell mit Dynamics 365 Human Resources verbunden ist, funktionieren die Dataverse virtuellen Tabellen, die in dieser Umgebung generiert wurden, weiterhin ohne zusätzliche Konfiguration.

Wenn die Umgebung der neuen Infrastruktur nach der Migration mit einer anderen Dataverse Umgebung verbunden wird, müssen alle Integrationen, die mit der Dataverse Web API entwickelt wurden, neu konfiguriert werden, damit sie mit der neuen Dataverse Ungebung verbunden werden können.

### <a name="is-there-an-impact-on-the-azure-region-when-my-environment-is-migrated"></a>Hat die Migration meiner Umgebung Auswirkungen auf die Azure-Region?

Es wird erwartet, dass Ihre Personalumgebung während der Migration normalerweise in derselben Azure-Region verbleibt. Die einzige Ausnahme ist, wenn die Human Resources Umgebung mit einer Finance und Operations Umgebung zusammengeführt wird, die sich in einer anderen Region befindet. In diesem Fall wird die Human Resources Umgebung in die Azure Region der Finance und Operations Umgebung migriert.

### <a name="my-organization-depends-on-workflows-in-dynamics-365-human-resources-for-one-or-more-business-processes-will-the-workflows-be-migrated-automatically"></a>Meine Organisation ist abhängig von Workflows in Dynamics 365 Human Resources für einen oder mehrere Geschäftsprozesse. Werden diese Workflows automatisch migriert?

Ja, Workflow-Konfigurationen, Workflow-Historie und aktuelle In-Process-Workflows werden migriert.

### <a name="what-training-and-resources-will-be-available-to-help-with-the-migration-process"></a>Welche Schulungen und Ressourcen stehen zur Verfügung, um den Migrationsprozess zu unterstützen?

Eine vollständige Dokumentation wird bereitgestellt, um jeden Schritt des Migrationsprozesses im Detail zu beschreiben. Je nach Bedarf können auch zusätzliche Schulungsressourcen wie Videos und Workshops verfügbar sein.

### <a name="my-organization-has-created-saved-views-in-dynamics-365-human-resources-to-improve-the-usability-of-the-interface-will-the-saved-views-be-migrated-automatically"></a>Meine Organisation hat gespeicherte Ansichten erstellt in Dynamics 365 Human Resources um die Benutzerfreundlichkeit der Schnittstelle zu verbessern. Werden diese gespeicherten Ansichten automatisch migriert?

Ja, gespeicherte Ansichten werden in die neue Infrastruktur migriert.

### <a name="we-are-using-ceridian-with-dynamics-365-human-resources-will-the-ceridian-integration-be-available-after-the-infrastructure-change-is-completed"></a>Wir verwenden Ceridian mit Dynamics 365 Human Resources. Wir die Ceridian Integariont nach der Abschluss der Infrastrukturänderung zur Verfügung stehen? 

Die Integration mit Ceridian wird auf die Gehaltsabrechnung-API-basierte Integration migriert. Die dateibasierte Integration, die derzeit in Dynamics 365 Human Resources existiert, wird nicht in die Finance und Operations-Infrastruktur migriert. Weitere Informationen finden Sie unter [Einführung der Gehaltsabrechnungs-API](./hr-admin-integration-payroll-api-introduction.md).

### <a name="how-will-the-migration-affect-the-service-update-process"></a>Wie wirkt sich die Migration auf den Service-Update-Prozess aus?

Nach der Migration haben Kunden viel mehr Flexibilität in Bezug auf ALM und Service-Updates. Service-Updates werden nicht mehr automatisch auf Human Resources-Umgebungen angewendet. Stattdessen folgt der Dienst den Aktualisierungsprozessen und der Funktionalität des One Version-Dienstes. Daher werden Konfigurationsoptionen für Updates über LCS verfügbar sein. Weitere Informationen finden Sie unter [One Version– Übersicht](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="how-will-the-migration-affect-my-lcs-project-for-dynamics-365-human-resources"></a>Wie wirkt sich die Migration auf mein LCS-Projekt aus für Dynamics 365 Human Resources?

Durch die Migration auf die neue Infrastruktur wird die Verwaltung Ihrer Dynamics 365 Human Resources-Umgebungen in ein Finance und Operations-Implementierungsprojekt in LCS verlagert. Wenn die Migration eine Zusammenführung Dynamics 365 Human Resources mit einer bestehenden Finance und Operations Umgebung ist, wird Ihr Human Resources LCS Projekt mit dem LCS Implementierungsprojekt für die Finance und Operations App zusammengeführt. Wenn Sie derzeit nur Dynamics 365 Human Resources verwenden, wird ein neues LCS-Implementierungsprojekt erstellt und Ihr vorhandenes Human Resources LCS-Projekt wird in das neue Projekt migriert.

Das neue Projekt ist der gleiche Projekttyp, den auch die Apps Finance und Operations verwenden. Es wird die gleichen Funktionen und Funktionen für die Umgebungsverwaltung haben. Weitere Informationen finden Sie unter [Lifecycle Services Ressourcen](../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

### <a name="we-have-linked-our-task-recordings-to-the-business-process-modeler-in-human-resources-how-will-the-business-process-modeler-be-migrated-and-merged-into-lcs"></a>Wir haben unsere Aufgabenaufzeichnungen mit dem Geschäftsprozessmodellierer in Human Resources verknüpft. Wie wird der Geschäftsprozessmodellierer migriert und in LCS zusammengeführt?

Geschäftsprozessbibliotheken für das LCS-Projekt werden in das neue LCS-Projekt für Human Resources migriert.

### <a name="my-organization-currently-uses-only-dynamics-365-human-resources-what-resources-are-available-so-that-we-can-learn-more-about-the-development-capabilities-after-the-infrastructure-change-is-completed"></a>Meine Organisation verwendet derzeit nur Dynamics 365 Human Resources. Welche Ressourcen stehen zur Verfügung, damit wir nach Abschluss der Infrastrukturänderung mehr über die Entwicklungsmöglichkeiten erfahren können?

Sowohl die Microsoft Power Platform-Erweiterungsoptionen als auch die Finance und Operations-Erweiterungsoptionen sind verfügbar und können für die Entwicklung verwendet werden. Weitere Informationen finden Sie unter [Homepage entwickeln und anpassen](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md).

### <a name="we-have-enabled-features-in-dynamics-365-human-resources-will-these-features-be-enabled-automatically-during-the-migration"></a>Wir haben Funktionen in Dynamics 365 Human Resources aktiviert. Werden diese Funktionen während der Migration automatisch aktiviert?

Ob eine Funktion automatisch in der neuen Infrastruktur aktiviert wird, wird für jede Funktion individuell festgelegt. Diese Informationen werden in die Funktionsdokumentation aufgenommen.

### <a name="what-happens-to-my-byod-database-during-the-migration"></a>Was passiert mit meiner BYOD-Datenbank während der Migration?

Import- und Exportkonfigurationen für Bring Your Own Database (BYOD) werden auf die neue Infrastruktur migriert.

### <a name="what-happens-to-my-azure-data-lake-during-the-migration"></a>Was passiert mit meinem Azure Data Lake während der Migration?

Alle Exporte, die in den Apps Finance und Operations derzeit für Azure Data Lake Storage konfiguriert sind, behalten diese Konfiguration auch nach der Migration bei.

### <a name="we-are-currently-using-dynamics-ax-2012-will-the-upgrade-tools-that-are-currently-available-be-used-to-upgrade-the-hr-module-in-ax-2012-to-dynamics-365-human-resources"></a>Wir verwenden derzeit Dynamics AX 2012. Werden die derzeit verfügbaren Upgrade-Tools verwendet, um das HR-Modul in AX 2012 auf Dynamics 365 Human Resources zu aktualisieren?

Ja. Dynamics 365 Human Resources wird in der zusammengeführten Codebasis und Infrastruktur für Apps für Finanzen und Betrieb enthalten sein. Ein Upgrade von Dynamics AX 2012 auf Dynamics 365 Human Resources erfolgt über denselben Upgrade-Pfad und dasselbe Tool, das auch für das Upgrade auf die neueste Version der Apps für Finanzen und Betrieb verwendet wird.

### <a name="we-use-document-handling-with-dynamics-365-human-resources-what-will-happen-to-the-documents-during-the-migration"></a>Wir verwenden das Dokumentenhandling mit Dynamics 365 Human Resources. Was passiert mit diesen Dokumenten während der Migration?

Die Dokumente verbleiben in der bestehenden Dokumentenablage. Sie werden der Umgebung in der neuen Infrastruktur neu zugeordnet.

### <a name="what-happens-to-the-batch-jobs-that-we-have-configured-in-dynamics-365-human-resources-after-the-migration"></a>Was passiert mit den Batch-Jobs nach der Migration, die wir in Dynamics 365 Human Resources konfiguriert haben?

Anwendbare Batch-Jobs werden automatisch in die neue Infrastruktur migriert.

## <a name="licensing-impact"></a>Auswirkungen auf die Lizenzierung

Diese Dokumentation ersetzt oder ersetzt keine der rechtlichen Dokumentationen, die Nutzungsrechte abdecken.

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-does-our-licensing-or-cost-change"></a>Meine Organisation verwendet Dynamics 365 Human Resources um seine HR-Aktivitäten zu verwalten. Ändert sich unsere Lizenzierung oder unsere Kosten?

Kunden, die Dynamics 365 Human Resources Lizenzen gekauft haben, sind davon nicht betroffen. Für diese Kunden gibt es keine Lizenzmigration. Die zusätzliche Sandbox Lagermengeneinheit (SKU), die für die Personalabteilung spezifisch war, ist nicht mehr anwendbar. Stattdessen können Debitor eine Apps für Finanzen und Betrieb Tier 2 Sandbox zu etwas geringeren Kosten erwerben. Bestehende Debitor, die eine Sandbox für Human Resources gekauft haben, werden ohne zusätzliche Kosten auf eine Sandbox für Apps für Finanzen und Betrieb Tier 2 migriert.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-does-my-licensing-or-cost-change"></a>Meine Organisation verwendet das Human Resources Modul in Dynamics 365 Finance, Supply Chain Management, Commerce oder Project Operations. Ändern sich meine Lizenzierung oder meine Kosten?

Bestehende Benutzer von Dynamics 365-Apps und Benutzer von eigenständigen Dynamics 365 Finance, Supply Chain Management, Commerce und Project Operations können im Rahmen dieser Lizenzen bis Februar 2025 oder bis zum Ablauf der aktuellen Lizenzvereinbarung auf Human Resources zugreifen, je nachdem, was früher eintritt. Sie können sich für einen früheren Wechsel zu Human Resources-Lizenzen entscheiden, wenn Sie dadurch bessere Kosteneinsparungen erzielen. Ab Februar 2025 müssen alle bestehenden CSP- und EA-Kunden das HR-Modul ablösen und Human Resources-Lizenzen erwerben, um die neuen Funktionalitäten zu nutzen, die in die Apps Finance und Operations aufgenommen werden.

### <a name="my-organization-is-live-with-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-will-we-be-required-to-purchase-an-additional-environment-to-support-the-infrastructure-merge"></a>Meine Organisation ist mit Dynamics 365 Finance, Supply Chain Management, Commerce oder Project Operations live. Müssen wir eine zusätzliche Umgebung erwerben, um die Zusammenführung der Infrastruktur zu unterstützen?

Zusätzliche Umgebungen sind nicht erforderlich, um die Infrastrukturänderung zu unterstützen.

### <a name="where-should-i-go-if-i-have-additional-questions-about-product-licensing"></a>Wohin soll ich mich wenden, wenn ich weitere Fragen zur Produktlizenzierung habe?

Wenn Sie Fragen zur Lizenzierung haben, finden Sie weitere Informationen auf [Biz Apps Hub – D365-Preise und -Lizenzierung](https://businessapplications.transform.microsoft.com/resources/pricing-and-licensing?tab=grandfathering). Wenn diese Informationen bei Ihrem Problem nicht helfen, öffnen Sie eine Anfrage bei LicenseQ.
