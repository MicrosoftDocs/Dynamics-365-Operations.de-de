---
title: Startseite von Finance Insights
description: Finance Insights bietet konfigurierbare und erweiterbare Modelle, mit denen Sie den Cashflow Ihres Unternehmens genau und intelligent vorhersagen können und auch, wann Sie Zahlungen für ausstehende Forderungen erhalten, und einen Budgetvorschlag erstellen können, der Ihren Budgetierungsprozess beschleunigen kann. Alle diese Funktionen basieren auf intelligenten Machine Learning-Modellen.
author: ShivamPandey-msft
ms.date: 01/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 42ea8884c357bcb26ac96df8dca75e7ff449d4f4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881961"
---
# <a name="finance-insights-home-page"></a>Startseite von Finance Insights

[!include [banner](../includes/banner.md)]

Finance Insights bietet konfigurierbare und erweiterbare Lösungen, mit denen Sie den Cashflow Ihres Unternehmens intelligent vorhersagen können und auch, wann Sie Zahlungen für ausstehende Forderungen erhalten, und einen Budgetvorschlag erstellen können, der Ihren Budgetierungsprozess beschleunigen kann. Diese Funktionen verwenden intelligente Vorlagen für maschinelles Lernen, um Modelle mit den von Ihnen bereitgestellten Daten zu erstellen (einschließlich Daten von Drittanbietern wie Verbraucherberichtsinformationen von einer Behörde). Diese intelligenten Funktionen unterstützen die Entscheidungsfindung und helfen Ihnen, Maßnahmen zu ergreifen, um effektiv auf aktuelle und erwartete geschäftliche Herausforderungen zu reagieren. Sie sind für alle Daten verantwortlich, die mit Finance Insights verwendet oder daraus ausgegeben werden.

> [!NOTE]
> Finance Insights ist in den Vereinigten Staaten von Amerika, Kanada, dem Vereinigten Königreich, Europa, dem asiatisch-pazifischen Raum, Japan, Australien und Neuseeland zur Bereitstellung verfügbar. Microsoft fügt schrittweise Unterstützung für weitere Regionen hinzu.

## <a name="prerequisites"></a>Voraussetzungen

In diesem Abschnitt werden die Anforderungen für die Verwendung von Finannzinformationen aufgeführt. Nach Möglichkeit werden Links zu Quellen zusätzlicher Informationen bereitgestellt.

### <a name="system-requirements"></a>Systemanforderungen

Für die Finance Insights-Vorschau ist eine Umgebung der Stufe 2 (Multi-Box) erforderlich. Weitere Hintergrundinformationen über Umgebungen finden Sie unter [Umgebungsplanung](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

### <a name="version-requirements"></a>Versionsanforderungen

Dieser Artikel gilt für Microsoft Dynamics 365 Finance ab Version 10.0.21.

### <a name="license-requirements"></a>Lizenz-Anforderungen

Finance Insights erstellt mit AI Builder Credits finanzielle Vorhersagen. Alle dafür notwendigen Lizenzen sind in der Mandantenlizenz enthalten. Jedem Dynamics 365 Finance-Mandanten werden monatlich 20.000 AI Builder-Gutschriften zur Verfügung gestellt. Wenn für den geschäftlichen Bedarf zusätzliche Kredite benötigt werden, können diese direkt über AI Builder gekauft werden.

### <a name="historical-data-requirements"></a>Anforderungen an historische Daten

Kundenrechnungen im Wert von mindestens einem Jahr sind erforderlich, um das Machine Learning-Modell, das für die Funktion zur Vorhersage von Kundenzahlungen verwendet wird, korrekt zu trainieren. Für Cashflow-Planungen werden drei Jahre historische Daten empfohlen. Für intelligente Budgetvorschläge werden drei Jahre historischer Budget- und/oder Ist-Werte empfohlen.

## <a name="configure-finance-insights"></a>Finance Insights konfigurieren

Sie müssen Konfigurationsschritte ausführen, bevor Sie Finance Insights verwenden können. Weitere Informationen zum Konfigurieren von Finance Insights finden Sie unter [Konfiguration für Finance Insights](configure-for-fin-insites.md).

## <a name="create-a-data-integrator-project"></a>Erstellen Sie ein Datenintegratorprojekt

Sie müssen ein Datenintegratorprojekt erstellen, damit Daten, die vom Machine Learning-Modell generiert werden, in Dynamics 365 Finance einfließen können. Die Schritte zum Erstellen dieses Projekts finden Sie unter [Erstellen eines Datenintegratorprojekts](create-data-integrate-project.md).

## <a name="enable-finance-insights-capabilities"></a>Aktivieren Sie die Funktionen für Finance Insights

Wenn Sie die Konfigurationsschritte abgeschlossen und Demodaten eingerichtet haben, müssen Sie alle Funktionen aktivieren und einrichten, die Sie verwenden möchten: Zahlungsvorhersagen für Kunden, Cashflow-Planungen und Budgetvorschläge.

### <a name="enable-customer-payment-predictions"></a>Aktivieren der Zahlungsvorhersagen für Debitoren
Wenn Sie Demodaten zum Testen von Debitorenzahlungsvorhersagen verwenden, müssen Sie möglicherweise zusätzliche Demodaten importieren, um Ihr KI-Modell erfolgreich zu erstellen. 

Um Zahlungsvorhersagen für Debitoren zu aktivieren, müssen Sie eine Reihe von Schritten ausführen, um ein Machine Learning-Modell zu erstellen, das die Daten Ihres Unternehmens verwendet, um Vorhersagen darüber zu erstellen, wann Debitoren voraussichtlich ausstehende Rechnungen bezahlen und wann bestimmte Rechnungen wahrscheinlich bezahlt werden. Weitere Informationen und die spezifischen Schritte finden Sie unter [Aktivieren der Zahlungsvorhersagen für Debitoren](enable-cust-paymnt-prediction.md). 

### <a name="enable-cash-flow-forecasting"></a>Cashflow-Planung aktivieren
Um die Cashflow-Planung zu aktivieren, müssen Sie eine Reihe von Schritten ausführen, um ein Machine Learning-Modell zu erstellen, um eine Cashflow-Planung zu erstellen. Weitere Informationen und die spezifischen Schritte finden Sie unter [Aktivieren der Cashflow-Planung](enable-cash-flow-forecasting.md).

### <a name="enable-budget-proposals"></a>Budgetvorschläge aktivieren

Die Funktion „Budgetvorschläge “ verwendet ein Machine Learning-Modell zusammen mit den historischen Daten Ihres Unternehmens, um einen Budgetvorschlag zu erstellen. Der generierte Vorschlag kann Ihnen dabei helfen, einen Budgetierungsprozess zu starten, der effektiver und effizienter als ein manueller Prozess ist. Informationen zu den spezifischen Schritten zum Aktivieren dieser Funktion finden Sie unter [Budgetvorschläge aktivieren](enable-budget-proposal.md). 

## <a name="using-finance-insights-features"></a>Verwenden von Finance Insights-Funktionen

### <a name="using-customer-payment-predictions"></a>Verwenden der Zahlungsvorhersagen für Debitoren

- Informationen dazu, wie Kundenzahlungsvorhersagen die Informationen liefern können, die dafür notwendig sind, mit einer proaktiven Erfassung zu beginnen, finden Sie unter [Verwenden der Zahlungsvorhersagen für Debitoren](use-customer-payment-predictions.md).
- Informationen, mit denen Sie die Wirksamkeit des Vorhersagemodells nach dem Start der Funktion bewerten können, finden Sie unter [Bewerten des anfänglichen Modell zur Vorhersage der Debitorenzahlung](evaluate-payment-prediction.md).
- Informationen, mit denen Sie die Daten anpassen können, die zum Erstellen der Vorhersage und damit zur Verbesserung ihrer Effektivität verwendet werden, finden Sie unter [Verbessern des Vorhersagemodells](improve-model.md).
- Weitere Informationen zu den Ergebnissen von KI-Vorhersagemodellen finden Sie unter [Ergebnisse von Machine Learning-Modellen](confusion-matrix.md).

### <a name="using-cash-flow-forecasts"></a>Verwenden von Cashflow-Planungen

Mit der Funktion zur Cashflow-Planung können Sie Ihre Cash-Position genauer einschätzen. Die intelligente Cashflow-Planung baut auf der vorhandenen Funktionalität zur Cashflow-Planung in Dynamics 365 Finance auf. Informationen zum Überprüfen der vorhandenen Funktionen finden Sie unter [Cashflow-Planung](../cash-bank-management/cash-flow-forecasting.md).

- Informationen zu den neuen Funktionen in Cashflow-Planungen finden Sie unter [Cahflow-Planung](cash-flow-forecast-intro.md).
- Informationen zum Importieren externer Daten, die hier in Ihre Cashflow-Prognose aufgenommen werden sollen, finden Sie unter [Verwenden externer Daten in Cashflow-Planungen](external-data-in-cash-flow.md). 
- Informationen zur Verwendung eines KI-Modells zur Planung des kurzfristigen Cashflows finden Sie unter [Bargeldposition](cash-position.md).
- Informationen zum Speichern von Cashflow-Positionen und Cashflow-Planungen als Momentaufnahmen sowie zum Vergleichen einer Momentaufnahme mit tatsächlichen Werten finden Sie unter [Übersicht über Momentaufnahmen](payment-snapshots.md).

### <a name="using-budget-proposal"></a>Budgetvorschlag verwenden

Informationen zur Beschleunigung der Erstellung eines Budgets finden Sie unter [Budgetvorschläge](budget-proposals.md). 

## <a name="feedback-and-support"></a>Feedback und Support

Wenn Sie an Feedback interessiert sind oder Support brauchen, senden Sie eine E-Mail an [Finance insights](mailto:fiap@microsoft.com).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
