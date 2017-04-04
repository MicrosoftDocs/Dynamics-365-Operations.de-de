---
title: "Startseite für die Budgetierung"
description: "Dieses Thema enthält einen Überblick der Haushaltsplanungsfunktionenskomponenten, der der Haushaltsplanungstools und Berichtsfunktionen in Microsoft Dynamics 365 für Arbeitsgänge bereit."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: index-page
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 106043
ms.assetid: 702f692e-ad1c-4798-8d3e-c3cf8591d3fa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: f7b4efc06b8e64c05da026850b41cb5b68c33ec3
ms.lasthandoff: 03/31/2017


---

# <a name="budgeting-home-page"></a>Startseite für die Budgetierung

Dieses Thema enthält einen Überblick der Haushaltsplanungsfunktionenskomponenten, der der Haushaltsplanungstools und Berichtsfunktionen in Microsoft Dynamics 365 für Arbeitsgänge bereit.

<a name="components-of-budgeting-functionality"></a>Budgetfunktionskomponenten
-------------------------------------

Der Ressourcenplanungszyklus für ein Unternehmen besteht normalerweise aus den Aktivitäten Planen, Budgetieren und Prognose.
[]![Haushaltsplanungsfunktionenskomponenten![. /media/budgeting-functionality-components.jpg)]". /media/budgeting-functionality-components.jpg) Die Prozesse für strategische Planung der Zeitraum und Jahresbudgetplanung sind durch ein Budgetplandokument unterstützt. Budgetplandokumente werden eng in Microsoft Excel integriert. Benutzer können unbegrenzt monetäre und quantitative Szenarien konfigurieren und eine Budgetplanungs-Organisationshierarchie anlegen, um Top-Down- und Bottom-Up-Budgetplanungsmethoden zu unterstützen. Nachdem ein Budget in Microsoft Dynamics 365 for Operations eingerichtet und genehmigt wurde, konvertieren Sie den Budgetplan in einem Budgetregistereintrag. Budgetregistereinträge enthalten Tools für die Verwaltung des Budgets und für die Nachverfolgung von Beträgen über Budgetcodes. Budgetregistereinträge lassen Sie ursprüngliche Budgets überarbeiten, Umbuchungen tätigen und Budgetbeträge vom Jahr zuvor übertragen. Auf Grundlage eines eingerichteten Budgets kann ein Unternehmen Budgetsteuerung aktivieren. Das Maß an Kontrolle hängt von der Kultur einer Organisation und vom Maturitätsgrad der Organisation ab. Organisationen mit einem niedrigen Reifegrad wollen möglicherweise das Budget nicht verändern und sind eher reaktiv als proaktiv, falls ein Budget nicht den Erwartungen entspricht. Andere Organisationen aktivieren möglicherweise Budgetsteuerungsrichtlinien, die Benutzer am Einkauf hindern, wenn keine Budgetmittel verfügbar sind. Schließlich richteten sehr reife Organisationen möglicherweise einer Organisationsbank Kultur, in der die Mitarbeiter zu erzogen organisatorische Ziele sind und diesen Ziele von Richtlinien Vorgehensweise folgen "berücksichtigt Online anstelle einer Besprechung Reise" ein. Dynamics 365 für Arbeitsgänge beinhaltet ein Budgetsteuerungsframework ein, der für die Verwaltung des Unternehmens entweder uneingeschränkte Steuerelement (das ausgewählt ist, die Buchungen verhindert zum Budget hinausgehen werden) oder "Weich" Steuerung (wobei Benutzer gewarnt werden, denen sie, die verfügbaren Budgetmittel zu überschreiten, jedoch selbst entscheiden können, z wohl überlegt sein). Schließlich können Sie Rollenplanungen verwenden. Eine Rollenplanung ist ein regelmäßiger Vergleich des Budgets auf die Wirklichkeiten und wird verwendet, um festzulegen, inwieweit das Unternehmen tätig anhand des Budgets. Eine Rollenplanung wird auch verwendet, um Trends zu erkennen. In Microsoft Dynamics 365 for Operations werden Rollenplanungen durch ein Budgetplandokument als Erstplanungsaktivitäten unterstützt. Rollierende Prognosen können parallel zur Planung für den bevorstehenden Budgetzyklus ausgeführt werden.

-   [Allgemeine Budgetplanung: Überblick und Konfiguration](basic-budgeting-overview-configuration.md)
-   [Budgetsteuerung: Überblick und Konfiguration](budget-control-overview-configuration.md)
-   [Budgetplanung: Überblick und Konfiguration](budget-planning-overview-configuration.md)
-   [Positionsplanung](position-forecasting.md)
-   Budgetplanungs-Begründungsdokumente [] (budget-planning-justification-docs.md )
-   [Microsoft Excel-Vorlagen für Budgetplanung] (budget-planning-excel-templates.md)

## <a name="budgeting-tools-in-dynamics-365-for-operations"></a>Budgetierungstools in Dynamics 365 for Operations
[![( Haushaltsplanungstools![. /media/budgeting-tools.jpg)]". /media/budgeting-tools.jpg) 

Zusätzliche Planungs- und Budgetierungsfunktionalitäten sind in Dynamics 365 for Operations verfügbar und in Sachkontobudgets integriert.

-   **Belegschaftsbudgets** - Die Belegschaftsbudgetplanung umfasst die detaillierte Planung von Komponenten der Budgetkosten für Positionen, Lohngruppen, usw.
-   **Anlagenbudgets** - Auf Grundlage von Anlagendaten können Sie geplante Abschreibung berechnen und andere anlagebezogenen Transaktionen erfassen.
-   **Projektbudgets** - Im Projektmodus können Sie detaillierte Projektplanungen erstellen. Die Projektprognosen enthalten Details zu geplanten Stunden, Ausgaben, die Gebühren und die Artikel.
-   ** Bedarfsplanung ** – auf früheren Buchungsdaten, können Sie zukünftige Bestandsbedarf bewerten und Auffüllung erstellen.

Informationen zur Integration von Planungsdatumsangaben aus anderen Modulen in Haushaltspläne finden Sie unter [Budgetplanungsintegration in andere Module](budget-planning-integration-other-modules.md).

## <a name="user-interface-and-reporting-capabilities"></a>Benutzeroberfläche und Berichtsfunktionen
In Microsoft Dynamics 365 for Operations können Benutzer Budgetpläne entweder direkt im Microsoft Dynamics 365 for Operations-Client (mithilfe einer konfigurierbaren Budgetplan-Dokumentenseite) oder in Excel erstellen. Excel beinhaltet mehrere zusätzliche Funktionen. So können beispielsweise externe Daten als Quelle für einen Budgetplan genutzt werden, benutzerdefinierte Berechnungen ausgeführt werden und Microsoft Pivottabellen und - Diagramme verwendet werden. Die meisten Variablen im Budgetplanungsprozess können konfiguriert werden. Sie können beispielsweise Folgendes definieren, wer budgetiert, was budgetiert wird und wie der Prozess aussieht. Obwohl Sie Excel für die Budgetplanung verwenden können, ist Microsoft Dynamics 365 for Operations die einzige vertrauenswürdige Quelle und hilft Budgetsteuerungsprobleme zu vermeiden. Periodische Prozesse können verwendet werden, um ursprünglichen Daten für die Budgetierung in den Budgetplan einzufügen. Microsoft Dynamics 365 for Operations bietet zu Berichtszwecken eine Zusammenstellung an Standardabfrageseiten an, in denen Sie Budgetplanungsdaten anzeigen und analysieren können. Über den Managementreporter können Sie auf Budgetplandaten zugreifen und separate Budgetplanszenarien können als Spalten im Managementreporter-Bericht angezeigt werden.





