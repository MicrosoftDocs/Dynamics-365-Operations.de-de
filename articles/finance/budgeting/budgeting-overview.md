---
title: Startseite der Budgetierung
description: Dieses Thema enthält eine Übersicht über die Budgetierungsfunktionskomponenten, die Budgetierungstools und die Berichtsfunktionen in Microsoft Dynamics 365 Finance.
author: panolte
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetPlanningWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "106043"
- intro-internal
ms.assetid: 702f692e-ad1c-4798-8d3e-c3cf8591d3fa
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9ced76e20a54d61fe96b5d2a5118adb0c5eb7ccf
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355699"
---
# <a name="budgeting-home-page"></a>Startseite der Budgetierung

[!include [banner](../includes/banner.md)]

Dieses Thema enthält eine Übersicht über die Budgetierungsfunktionskomponenten, die Budgetierungstools und die Berichtsfunktionen. 

## <a name="components-of-budgeting-functionality"></a>Budgetfunktionskomponenten

Der Ressourcenplanungszyklus für ein Unternehmen besteht normalerweise aus folgenden Aktivitäten: Planung, Budgetierung und Prognose.

[![Budgetfunktionskomponenten.](./media/budgeting-functionality-components.jpg)](./media/budgeting-functionality-components.jpg)

Der Prozess sowohl für die langfristige strategische Planung als auch für die Jahresbudgetplanung werden von einem Budgetplandokument unterstützt. Budgetplandokumente sind eng in Microsoft Excel integriert. Benutzer können unbegrenzt monetäre und quantitative Szenarien konfigurieren sowie eine Budgetplanungs-Organisationshierarchie anlegen, um die Budgetplanungsmethoden Top-Down und Bottom-Up zu unterstützen. Nach dem Einrichten und Genehmigen eines Budgets in der Anwendung konvertieren Sie den Budgetplan in einen Budgetregistereintrag. Budgetregistereinträge enthalten Tools zur Verwaltung des Budgets und für die Nachverfolgung von Beträgen über Budgetcodes. Mit Budgetregistereinträgen können Sie ursprüngliche Budgets überarbeiten, Umbuchungen tätigen und Budgetbeträge vom Vorjahr übertragen. Auf Grundlage eines eingerichteten Budgets kann ein Unternehmen Budgetsteuerung aktivieren. Das Maß an Kontrolle hängt von der Kultur einer Organisation und vom Maturitätsgrad der Organisation ab. Organisationen mit einem niedrigen Reifegrad möchten das Budget möglicherweise nicht verändern und sind eher reaktiv als proaktiv, falls ein Budget nicht den Erwartungen entspricht. Andere Organisationen aktivieren möglicherweise Budgetsteuerungsrichtlinien, die Benutzer am Einkauf hindern, wenn keine Budgetmittel verfügbar sind.

Schließlich etablieren sehr erfahrene Organisationen möglicherweise eine Organisationskultur, in der die Mitarbeiter über organisatorische Ziele informiert sind und versuchen, diese Ziele mittels Richtlinien wie z. B. „Ziehen Sie eine Online-Besprechung einer Dienstreise vor“ zu erreichen. Die Anwendung beinhaltet ein Budgetsteuerungsframework, mit dem das Unternehmensmanagement entweder strikte Kontrolle (wodurch Buchungen verhindert werden, die über das Budget hinausgehen) oder weniger strikte Kontrolle (der Benutzer wird gewarnt, wenn die verfügbaren Budgetmittel überschritten werden, kann jedoch selbst entscheiden, ob er fortfahren möchte) wählen kann. Schließlich können Sie rollende Planungen verwenden. Eine rollende Planung ist ein regelmäßiger Vergleich des Budgets mit Istwerten und wird verwendet, um zu ermitteln, inwieweit das Unternehmen im Rahmen des Budgets agiert. Eine rollende Planung wird auch verwendet, um Trends zu erkennen. In Finance and Operations werden rollende Planungen durch ein Budgetplandokument als Erstplanungsaktivitäten unterstützt. Rollende Planungen können parallel zur Planung des bevorstehenden Budgetzyklus ausgeführt werden.

-   [Budgetierungsüberblick](basic-budgeting-overview-configuration.md)
-   [Budgetsteuerung – Übersicht](budget-control-overview-configuration.md)
-   [Budgetplanung – Übersicht](budget-planning-overview-configuration.md)
-   [Positionsplanung](position-forecasting.md)
-   [Begründungsdokumente für die Budgetplanung](budget-planning-justification-docs.md)
-   [Budgetplanungsvorlagen für Excel](budget-planning-excel-templates.md)

## <a name="budgeting-tools"></a>Budgetierungstools
[![Budgetierungstools.](./media/budgeting-tools.jpg)](./media/budgeting-tools.jpg) 

Es sind zusätzliche Planungs- und Budgetierungsfunktionalitäten verfügbar und in Sachkontenbudgets integriert.

-   **Belegschaftsbudgets** – Die Belegschaftsbudgetplanung umfasst die detaillierte Planung von Budgetkostenkomponenten für Positionen, Lohngruppen usw.
-   **Anlagenbudgets** – Auf Grundlage von Anlagendaten können Sie geplante Abschreibung berechnen und andere anlagebezogenen Transaktionen erfassen.
-   **Projektbudgets** – Im Projektmodus können Sie detaillierte Projektplanungen erstellen. Die Projektprognosen enthalten Details zu geplanten Stunden und Ausgaben sowie die Gebühren und die Artikel.
-   **Bedarfsplanung** – Basierend auf früheren Buchungsdaten können Sie den zukünftigen Bestandsbedarf schätzen und Bedarfsplanungen erstellen.

Informationen zur Integration von Planungsdaten aus anderen Modulen in Budgetpläne finden Sie unter [Budgetplanungsintegration in andere Module](budget-planning-integration-other-modules.md).

## <a name="user-interface-and-reporting-capabilities"></a>Benutzeroberfläche und Berichtsfunktionen
Benutzer können Budgetpläne entweder direkt im Client (mithilfe einer konfigurierbaren Budgetplan-Dokumentenseite) oder in Excel erstellen. Excel bietet mehrere zusätzliche Funktionen. So können Sie beispielsweise externe Daten als Quelle für einen Budgetplan nutzen, benutzerdefinierte Berechnungen ausführen und Microsoft Excel-PivotTable-Tabellen und -Diagramme verwenden. Die meisten Variablen im Budgetplanungsprozess können konfiguriert werden. 

Sie können beispielsweise definieren, wer die Budgetierung vornimmt, was budgetiert wird und wie der Prozess verläuft. Obwohl Sie Excel für die Budgetplanung verwenden können, ist die Anwendung die vertrauenswürdigere Quelle, mit der Sie Budgetsteuerungsprobleme vermeiden können. Periodische Prozesse können verwendet werden, um ursprüngliche Daten für die Budgetierung in den Budgetplan einzufügen. Die Anwendung bietet zu Berichtszwecken eine Zusammenstellung an Standardabfrageseiten an, in denen Sie Budgetplanungsdaten anzeigen und analysieren können. Über [Financial Reporting](../general-ledger/financial-reporting-getting-started.md) können Sie auf Budgetplandaten zugreifen. Separate Budgetplanszenarien können Sie sich als Spalten im Finanzbericht anzeigen lassen.








[!INCLUDE[footer-include](../../includes/footer-banner.md)]
