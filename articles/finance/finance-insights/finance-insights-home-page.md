---
title: Homepage zu Finance Insights (Vorschau)
description: Finance Insights bietet konfigurierbare und erweiterbare Modelle, mit denen Sie den Cashflow Ihres Unternehmens genau und intelligent vorhersagen können und auch, wann Sie Zahlungen für ausstehende Forderungen erhalten, und einen Budgetvorschlag erstellen können, der Ihren Budgetierungsprozess beschleunigen kann. Alle diese Funktionen basieren auf intelligenten Machine Learning-Modellen.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 9920d24ea92196331ea318cab2f67501801937bd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995089"
---
# <a name="finance-insights-home-page-preview"></a>Homepage zu Finance Insights (Vorschau)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Finance Insights bietet konfigurierbare und erweiterbare Modelle, mit denen Sie den Cashflow Ihres Unternehmens genau und intelligent vorhersagen können und auch, wann Sie Zahlungen für ausstehende Forderungen erhalten, und einen Budgetvorschlag erstellen können, der Ihren Budgetierungsprozess beschleunigen kann. Alle diese Funktionen basieren auf intelligenten Machine Learning-Modellen. Wenn diese neuen Funktionen mit der Automatisierung von Kreditorenzahlungen und Inkasso kombiniert werden, bieten sie ein umfassendes und intelligentes Finanzsystem, das die Entscheidungsfindung vorantreibt und Ihnen hilft, Maßnahmen zu ergreifen, um effektiv auf aktuelle und erwartete geschäftliche Herausforderungen zu reagieren.

Die Finance Insights-Vorschau ist für Testbereitstellungen in den Vereinigten Staaten von Amerika, Europa und Großbritannien verfügbar. Microsoft fügt schrittweise Unterstützung für weitere Regionen hinzu.

Vorschaufunktionen können und sollten nur in Sandbox-Umgebungen der Stufe 2 aktiviert werden. Einrichtungs- und künstliche Intelligenz(KI)-Mopelle, die in einer Sandbox-Umgebung erstellt werden, können nicht in eine Produktionsumgebung migriert werden. Weitere Informationen finden Sie unter [Ergänzende Nutzungsbedingungen für Microsoft Dynamics 365 Vorschauen](https://docs.microsoft.com/dynamics365/legal/supp-dynamics365-preview#:~:text=Supplemental%20Terms%20of%20Use%20for%20Microsoft%20Dynamics%20365,%28governing%20your%20use%20of%20Microsoft%20Dynamics%20365%20Online%29.).

## <a name="prerequisites"></a>Voraussetzungen

In diesem Abschnitt werden die Anforderungen für die Verwendung von Finannzinformationen aufgeführt. Nach Möglichkeit werden Links zu Quellen zusätzlicher Informationen bereitgestellt.

### <a name="legal-requirements"></a>Rechtliche Anforderungen

Um sich für das Vorschauprogramm zu bewerben, füllen Sie das Feld aus [Finance Insights-Vorschau für Dynamics 365 Finance-Vereinbarung](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUM1c0Uzc1RFpaU1RVTEwxVTNWUERPRThUSy4u).

### <a name="system-requirements"></a>Systemanforderungen

Für die Finance Insights-Vorschau ist eine Sandbox-Umgebung der Stufe 2 (Multi-Box) erforderlich. Weitere Hintergrundinformationen über Umgebungen finden Sie unter [Umgebungsplanung](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/imp-lifecycle/environment-planning).

### <a name="version-requirements"></a>Versionsanforderungen

Dieses Dokument gilt für Version 10.0.11 von Finance and Operations-Apps (Platform Update 35) und spätere Versionen.

### <a name="historical-data-requirements"></a>Anforderungen an historische Daten

Kundenrechnungen im Wert von mindestens einem Jahr sind erforderlich, um das Machine Learning-Modell, das für die Funktion zur Vorhersage von Kundenzahlungen verwendet wird, korrekt zu trainieren.

Beispieldaten sind für Demosysteme verfügbar, die über den Contoso-Demo-Datensatz verfügen.

### <a name="role-and-permission-requirements"></a>Rollen- und Berechtigungsanforderungen

Änderungen werden an Microsoft Dynamics 365 Finance, Microsoft Dynamics Lifecycle Services (LCS), Power Apps und Azure vorgenommen. In diesen Umgebungen sind korrekte Berechtigungen erforderlich. Nachfolgend sind einige Beispiele der Änderungen aufgeführt, die vorgenommen werden:

- Eine neue Umgebung wird in Microsoft Power Platform erstellt.
- In Azure werden ein Speicherkonto, ein Key Vault und eine Anwendung erstellt.
- Der Active Directory-Mandantenadministrator muss die AI Builder-Anwendung für den Zugriff auf den Data Lake autorisieren.
- Die Funktion wird in Dynamics 365 aktiviert.

Vertrautheit mit dem Erstellen und Verwalten von Ressourcen in Azure, Microsoft Dataverse und LCS sind hilfreich, wenn Sie diesen Vorgang abschließen.

## <a name="configure-finance-insights"></a>Konfigurieren von Finance Insights

Sie müssen einige Konfigurationsschritte ausführen, bevor Sie Finance Insights verwenden können. Weitere Informationen zum Konfigurieren von Finance Insights finden Sie unter [Konfiguration für Finance Insights](configure-for-fin-insites.md).

## <a name="create-a-data-integrator-project"></a>Erstellen Sie ein Datenintegratorprojekt

Sie müssen ein Datenintegratorprojekt erstellen, damit Daten, die vom Machine Learning-Modell generiert werden, in Dynamics 365 Finance einfließen können. Die Schritte zum Erstellen dieses Projekts finden Sie unter [Erstellen eines Datenintegratorprojekts](create-data-integrate-project.md).

## <a name="enable-finance-insights-capabilities"></a>Aktivieren Sie die Funktionen für Finance Insights

Wenn Sie die Konfigurationsschritte abgeschlossen und Demodaten eingerichtet haben, müssen Sie alle Funktionen aktivieren und einrichten, die Sie verwenden möchten: Zahlungsvorhersagen für Kunden, Cashflow-Planungen und Budgetvorschläge.

### <a name="enable-customer-payment-predictions"></a>Aktivieren der Zahlungsvorhersagen für Debitoren
Wenn Sie Demodaten zum Testen von Debitorenzahlungsvorhersagen verwenden, müssen Sie möglicherweise zusätzliche Demodaten importieren, um Ihr KI-Modell erfolgreich zu erstellen. Informationen zu den spezifischen Schritten zum Importieren von Demodaten finden Sie unter [Einrichten der Demodaten für Zahlungsvorhersagen](set-up-demo-data.md).

Um Zahlungsvorhersagen für Debitoren zu aktivieren, müssen Sie eine Reihe von Schritten ausführen, um ein Machine Learning-Modell zu erstellen, das die Daten Ihres Unternehmens verwendet, um anhand der Daten Ihres Unternehmens Vorhersagen darüber zu erstellen, wann Debitoren voraussichtlich ausstehende Rechnungen bezahlen und wann bestimmte Rechnungen wahrscheinlich bezahlt werden. Weitere Informationen und die spezifischen Schritte finden Sie unter [Aktivieren der Zahlungsvorhersagen für Debitoren](enable-cust-paymnt-prediction.md). 

### <a name="enable-cash-flow-forecasting"></a>Cashflow-Planung aktivieren
Um die Cashflow-Planung zu aktivieren, müssen Sie eine Reihe von Schritten ausführen, um ein Machine Learning-Modell zu erstellen, das die Daten Ihrer Organisation verwendet, um eine Cashflow-Planung zu erstellen. Weitere Informationen und die spezifischen Schritte finden Sie unter [Aktivieren der Cashflow-Planung](enable-cash-flow-forecasting.md) 

### <a name="set-up-and-use-cash-flow-forecasting"></a>Einrichten und Verwenden der Cashflow-Planung
Weitere Informationen dazu, wie die Cashflow-Planung eingerichtet und verwendet wird, finden Sie unter [Cashflow-Planung aktivieren](enable-cash-flow-forecasting.md). Weitere Informationen dazu, wie diese Fähigkeit verwendet wird, finden Sie unter [Cachflow-Planung](cash-flow-forecast-intro.md).

### <a name="enable-budget-proposals"></a>Budgetvorschläge aktivieren

Die Funktion „Budgetvorschläge “ verwendet ein Machine Learning-Modell zusammen mit den historischen Daten Ihres Unternehmens, um einen Budgetvorschlag zu erstellen. Der generierte Vorschlag kann Ihnen dabei helfen, einen Budgetierungsprozess zu starten, der effektiver und effizienter als ein manueller Prozess ist. Informationen zu den spezifischen Schritten zum Aktivieren dieser Funktion finden Sie unter [Budgetvorschläge aktivieren](enable-budget-proposal.md). 

## <a name="using-finance-insights-features"></a>Verwenden von Finance Insights-Funktionen

### <a name="using-customer-payment-predictions"></a>Verwenden der Zahlungsvorhersagen für Debitoren

Die intelligente Cashflow-Planung baut auf der vorhandenen Funktionalität zur Cashflow-Planung in Dynamics 365 Finance auf. Informationen zum Überprüfen der vorhandenen Funktionen finden Sie unter [Cashflow-Planung](../cash-bank-management/cash-flow-forecasting.md).

- Informationen dazu, wie Kundenzahlungsvorhersagen die Informationen liefern können, die für eine proaktive Erfassung erforderlich sind, finden Sie unter [Verwenden der Zahlungsvorhersagen für Debitoren](use-customer-payment-predictions.md).
- Informationen, mit denen Sie die Wirksamkeit des Vorhersagemodells nach dem Start der Funktion bewerten können, finden Sie unter [Bewerten des anfänglichen Modell zur Vorhersage der Debitorenzahlung](evaluate-payment-prediction.md).
- Informationen, mit denen Sie die Daten anpassen können, die zum Erstellen der Vorhersage und damit zur Verbesserung ihrer Effektivität verwendet werden, finden Sie unter [Verbessern des Vorhersagemodells](improve-model.md).

Weitere Informationen zu den Ergebnissen von KI-Vorhersagemodellen finden Sie unter [Ergebnisse von Machine Learning-Modellen](confusion-matrix.md).

### <a name="using-cash-flow-forecasts"></a>Verwenden von Cashflow-Planungen

Mit der Funktion zur Cashflow-Planung können Sie Ihre Cash-Position genauer einschätzen. 

- Informationen zu den neuen Funktionen in Cashflow-Planungen finden Sie unter [Cahflow-Planung](cash-flow-forecast-intro.md).
- Informationen zum Importieren externer Daten, die hier in Ihre Cashflow-Prognose aufgenommen werden sollen, finden Sie unter [Verwenden externer Daten in Cashflow-Planungen](external-data-in-cash-flow.md). 
- Informationen zur Verwendung eines KI-Modells zur Planung des langfristigen Cashflows finden Sie unter [Übersicht über die Cashflow-Planungen](cash-position.md).
- Informationen zum Speichern von Cashflow-Positionen und Cashflow-Planungen als Momentaufnahmen sowie zum Vergleichen einer Momentaufnahme mit tatsächlichen Werten finden Sie unter [Übersicht über Momentaufnahmen](payment-snapshots.md).

### <a name="using-budget-proposal"></a>Budgetvorschlag verwenden

Informationen zur Beschleunigung der Erstellung eines Budgets finden Sie unter [Budgetvorschläge](budget-proposals.md). 

Demo-Daten für Budgetvorschlag:

## <a name="feedback-and-support"></a>Feedback und Support

Bitte senden Sie eine E-Mail an [Debitorenzahlungseinblicke (Vorschau)](mailto:fiap@microsoft.com), wenn Sie an Feedback interessiert sind oder Support benötigen.

## <a name="privacy-notice"></a>Datenschutzhinweis

Vorschauen (1) wenden möglicherweise weniger Datenschutz- und Sicherheitsmaßnahmen an als der Dynamics 365 Finance and Operations-Dienst, (2) sind nicht in der Service Level Agreement (SLA) für diesen Dienst enthalten, (3) sollten nicht zur Verarbeitung personenbezogener Daten oder anderer Daten verwendet werden, die gesetzlichen oder behördlichen Compliance-Anforderungen unterliegen, und (4) hat begrenzten Support.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]