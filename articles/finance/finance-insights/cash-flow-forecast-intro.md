---
title: Cashflow-Planung (Vorschau)
description: In diesem Thema wird die Funktion zur Cashflow-Planung beschrieben.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 64935db3b50e7598f2076ecbec72aba020d4f908
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186539"
---
# <a name="cash-flow-forecast-preview"></a>Cashflow-Planung (Vorschau)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Der Cashflow ist für jedes Unternehmen von entscheidender Bedeutung. Selbst profitable Unternehmen können insolvent werden, wenn sie den Cashflow nicht aufrechterhalten, um den unmittelbaren Bedarf zu decken. Die Funktion zur Cashflow-Planung in Finance Insights kann Unternehmen dabei helfen, ihre Bargeldbilanz effektiv zu überwachen und zu verwalten. Diese Funktion verwendet Machine Learning, um Unternehmen dabei zu helfen, Cashflows genauer als bisher vorherzusagen. Es kann Managern auch dabei helfen, Entscheidungen zu treffen, die die Chancen im Kontext ihrer aktuellen Bargeldposition optimieren. 

Für die meisten Unternehmen ist die Verwaltung des Cashflows und die Durchführung von Cashflow-Planungen ein langwieriger, sich wiederholender und manueller Prozess. Die meisten Unternehmen verlassen sich auf Microsoft Excel-Lösungen mit unterschiedlicher Komplexität. Zu den Herausforderungen bei der genauen Prognose des Cashflows gehören:

- Daten stehen Entscheidungsträgern nicht zur Verfügung, da sie an mehreren Stellen verteilt sind, darunter: 
  - Das Buchhaltungs- oder Unternehmensressourcenplanungssystem
  - Finanzplanungssoftware
  - Excel
  - Zusätzliche Softwareanwendungen 
- Die Prognose basiert auf internem Wissen, das sich in „Silos“ innerhalb jeder Domäne oder Abteilung befindet.
- Die Messung der Genauigkeit der Cashflow-Planung nach Realisierung der Finanzdaten ist ungewiss und schwierig.
    
## <a name="details-of-the-cash-flow-forecasts-capability"></a>Details zur Fähigkeit zur Cashflow-Planung
Die Cashflow-Planungsfunktion umfasst die folgenden Funktionen. 

- Erleichtert die Integration von Cashflow-Daten von externen Systemen in Dynamics 365 Finance. Cashflow-Planungen können auch das Framework für Datenimport-Export verwenden. Dieses Framework erleichtert die Integration in Excel OData. Sie können auch Daten aus mehreren Quellen kombinieren, um eine umfassende Cashflow-Lösung zu erstellen. 

- Führt eine intelligente Bargeldposition ein. Die Bargeldposition wird basierend auf dem Zahlungsverhalten des Debitors erstellt, um vorherzusagen, wann ein Unternehmen mit Bargeld auf seinen Konten rechnen kann. Außerdem werden die historischen Muster zahlender Kreditoren analysiert, um vorherzusagen, wann zukünftige Rechnungen und Bestellungen voraussichtlich bezahlt werden. 

- Einführung einer intelligenten Cashflow-Planung für Langzeitprognosen unter Verwendung von Zeitreihenprognosen durch automatisierte Integration in AI Builder.

- Bietet die Möglichkeit, bestimmte Cashflow-Positionen oder Prognosen zu speichern, zu bearbeiten und dann die Prognoseleistung einfach mit den tatsächlichen Finanzdaten zu vergleichen und zu messen.

- Aktiviert die Was-wäre-wenn-Analyse durch den Vergleich von Momentaufnahmen. Sie können beispielsweise mehrere Momentaufnahmen erstellen, die optimistische, pessimistische und realistischste Ansichten Ihres Cashflows darstellen, und dann die Unterschiede vergleichen und anzeigen.

- Bietet die Möglichkeit, die Cashflow-Planung in mehreren Währungen über juristische Personen hinweg anzuzeigen und den Cashflow in Bezug auf ein Bankkonto zu filtern und anzuzeigen. 

- Hiermit können Sie Bankkonten filtern und anzeigen, die sich auf Finanzdimensionen beziehen.

Die Funktion zur Cashflow-Planung in Dynamics 365 Finance ermöglicht Ihrem Unternehmen, langwierige, komplexe und sich wiederholende Cashflow-Planungen in einen einfachen, automatisierten Prozess umzuwandeln. Durch die Automatisierung der langwierigsten Aspekte der Cashflow-Planung können Sie sich auf kritische Entscheidungen konzentrieren, um die gewünschten Geschäftsergebnisse zu erzielen.

## <a name="setting-up-dimensions-for-cash-flow-forecasting"></a>Einrichten von Dimensionen für die Cashflow-Planung
Auf der neuen Registerkarte auf der **Einrichtung der Cashflow-Planung** Seite können Sie steuern, welche Finanzdimensionen für die Filterung im **Cashflow-Planung**-Arbeitsbereich verwendet werden sollen. Diese Registerkarte wird nur angezeigt, wenn die Cashflow-Planungsfunktion aktiviert ist. 

Wählen Sie auf der Registerkarte **Dimensionen** aus der Liste der zur Filterung verwendeten Dimensionen aus und verschieben Sie sie mit den Pfeiltasten in die rechte Spalte. Zum Filtern von Cashflow-Planungsdaten können nur zwei Dimensionen ausgewählt werden. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
