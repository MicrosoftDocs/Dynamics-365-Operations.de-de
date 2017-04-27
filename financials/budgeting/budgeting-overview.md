---
title: "Startseite für die Budgetierung"
description: "Dieses Thema enthält eine Übersicht über die Budgetierungsfunktionskomponenten, die Budgetierungstools und die Berichtsfunktionen in Microsoft Dynamics 365 for Operations."
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

[!include[banner](../includes/banner.md)]


Dieses Thema enthält eine Übersicht über die Budgetierungsfunktionskomponenten, die Budgetierungstools und die Berichtsfunktionen in Microsoft Dynamics 365 for Operations. 

<a name="components-of-budgeting-functionality"></a>Budgetfunktionskomponenten
-------------------------------------

Der Ressourcenplanungszyklus für ein Unternehmen besteht normalerweise aus den Aktivitäten Planen, Budgetieren und Prognose.
[![Budget-Funktionenkomponenten](./media/budgeting-functionality-components.jpg)](./media/budgeting-functionality-components.jpg)Der Prozess sowohl für die langfristige strategische Planung wie auch für die Jahresbudgetplanung werden von einem Budgetplandokument unterstützt. Budgetplandokumente werden eng in Microsoft Excel integriert. Benutzer können unbegrenzt monetäre und quantitative Szenarien konfigurieren und eine Budgetplanungs-Organisationshierarchie anlegen, um Top-Down- und Bottom-Up-Budgetplanungsmethoden zu unterstützen. Nachdem ein Budget in Microsoft Dynamics 365 for Operations eingerichtet und genehmigt wurde, konvertieren Sie den Budgetplan in einem Budgetregistereintrag. Budgetregistereinträge enthalten Tools für die Verwaltung des Budgets und für die Nachverfolgung von Beträgen über Budgetcodes. Budgetregistereinträge lassen Sie ursprüngliche Budgets überarbeiten, Umbuchungen tätigen und Budgetbeträge vom Jahr zuvor übertragen. Auf Grundlage eines eingerichteten Budgets kann ein Unternehmen Budgetsteuerung aktivieren. Das Maß an Kontrolle hängt von der Kultur einer Organisation und vom Maturitätsgrad der Organisation ab. Organisationen mit einem niedrigen Reifegrad wollen möglicherweise das Budget nicht verändern und sind eher reaktiv als proaktiv, falls ein Budget nicht den Erwartungen entspricht. Andere Organisationen aktivieren möglicherweise Budgetsteuerungsrichtlinien, die Benutzer am Einkauf hindern, wenn keine Budgetmittel verfügbar sind. Schließlich haben sehr reife Organisationen möglicherweise einer Organisationskultur, in der die Mitarbeiter über organisatorische Ziele informiert sind und diese Ziele über Richtlinien folge Leisten wie "Berücksichtigen von Online-Meetings anstelle einer Reise". Dynamics 365 for Operations beinhaltet ein Budgetsteuerungsframework, mit der das Unternehmens entweder uneingeschränkte Steuerelement auswählen kann (die Buchungen verhindern, die über das Budget hinausgehen) oder "weiche" Steuerung (der Benutzer wird gewarnt, wenn die verfügbaren Budgetmittel überschritten werden, aber er kann selber entscheid, ob er fortfahren möchte). Schließlich können Sie Rollenplanungen verwenden. Eine Rollenplanung ist ein normaler Vergleich des Budgets mit Istwerten und wird verwendet, um zu definieren, inwieweit das Unternehmen in Rahmen des Budgets tätig ist. Eine Rollenplanung wird auch verwendet, um Trends zu erkennen. In Microsoft Dynamics 365 for Operations werden Rollenplanungen durch ein Budgetplandokument als Erstplanungsaktivitäten unterstützt. Rollierende Prognosen können parallel zur Planung für den bevorstehenden Budgetzyklus ausgeführt werden.

-   [Allgemeine Budgetplanung: Überblick und Konfiguration](basic-budgeting-overview-configuration.md)
-   [Budgetsteuerung: Überblick und Konfiguration](budget-control-overview-configuration.md)
-   [Budgetplanung: Überblick und Konfiguration](budget-planning-overview-configuration.md)
-   [Positionsplanung](position-forecasting.md)
-   [Budgetplanungs-Begründungsdokumente](budget-planning-justification-docs.md)
-   [Budgetplanungsvorlage für Microsoft Excel](budget-planning-excel-templates.md)

## <a name="budgeting-tools-in-dynamics-365-for-operations"></a>Budgetierungstools in Dynamics 365 for Operations
[![Budgetierungstools](./media/budgeting-tools.jpg)](./media/budgeting-tools.jpg) 

Zusätzliche Planungs- und Budgetierungsfunktionalitäten sind in Dynamics 365 for Operations verfügbar und in Sachkontobudgets integriert.

-   **Belegschaftsbudgets** - Die Belegschaftsbudgetplanung umfasst die detaillierte Planung von Komponenten der Budgetkosten für Positionen, Lohngruppen, usw.
-   **Anlagenbudgets** - Auf Grundlage von Anlagendaten können Sie geplante Abschreibung berechnen und andere anlagebezogenen Transaktionen erfassen.
-   **Projektbudgets** - Im Projektmodus können Sie detaillierte Projektplanungen erstellen. Die Projektprognosen enthalten Details zu geplanten Stunden, Ausgaben, die Gebühren und die Artikel.
-   **Bedarfsplanung** Verschiedene Tools bieten die Möglichkeit an, den zukünftigen Bestandsbedarf zu schätzen und Bedarfsplanungen basierend auf früheren Buchungsdaten zu erstellen.

Informationen zur Integration von Planungsdatumsangaben aus anderen Modulen in Haushaltspläne finden Sie unter [Budgetplanungsintegration in andere Module](budget-planning-integration-other-modules.md).

## <a name="user-interface-and-reporting-capabilities"></a>Benutzeroberfläche und Berichtsfunktionen
In Microsoft Dynamics 365 for Operations können Benutzer Budgetpläne entweder direkt im Microsoft Dynamics 365 for Operations-Client (mithilfe einer konfigurierbaren Budgetplan-Dokumentenseite) oder in Excel erstellen. Excel beinhaltet mehrere zusätzliche Funktionen. So können beispielsweise externe Daten als Quelle für einen Budgetplan genutzt werden, benutzerdefinierte Berechnungen ausgeführt werden und Microsoft Pivottabellen und - Diagramme verwendet werden. Die meisten Variablen im Budgetplanungsprozess können konfiguriert werden. Sie können beispielsweise Folgendes definieren, wer budgetiert, was budgetiert wird und wie der Prozess aussieht. Obwohl Sie Excel für die Budgetplanung verwenden können, ist Microsoft Dynamics 365 for Operations die einzige vertrauenswürdige Quelle und hilft Budgetsteuerungsprobleme zu vermeiden. Periodische Prozesse können verwendet werden, um ursprünglichen Daten für die Budgetierung in den Budgetplan einzufügen. Microsoft Dynamics 365 for Operations bietet zu Berichtszwecken eine Zusammenstellung an Standardabfrageseiten an, in denen Sie Budgetplanungsdaten anzeigen und analysieren können. Über den Managementreporter können Sie auf Budgetplandaten zugreifen und separate Budgetplanszenarien können als Spalten im Managementreporter-Bericht angezeigt werden.







