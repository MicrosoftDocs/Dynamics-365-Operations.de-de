---
title: Problembehandlung beim Einrichten von Finance Insights
description: In diesem Thema werden Probleme aufgelistet, die auftreten können, wenn Sie die Funktionen von Finance Insights verwenden. Außerdem wird erläutert, wie Sie diese Probleme beheben können.
author: panolte
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-20
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: fc616e5fce6bbfeaa3b36ccc35f1b1cf407af4a6
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109859"
---
# <a name="troubleshoot-finance-insights-setup-issues"></a>Problembehandlung beim Einrichten von Finance Insights

[!include [banner](../includes/banner.md)]

In diesem Thema werden Probleme aufgelistet, die auftreten können, wenn Sie die Funktionen von Finance Insights verwenden. Außerdem wird erläutert, wie Sie diese Probleme beheben können.

## <a name="symptom-why-cant-i-map-the-customer-payment-insights-data-integration-template-destination-column"></a>Symptom: Warum kann ich die Zielspalte der Debitorenzahlungseinblicke für Customer Payment Insights nicht zuordnen?

### <a name="resolution"></a>Lösung

Möglicherweise verwenden Sie eine Vorlage für eine frühere Version. Vor der Veröffentlichung von Version 10.0.17 haben Kunden der Vorschauversion die Vorlage **Ergebnisse der Debitorenzahlungserkenntnisse (CDS an Finance and Operations)** für die Datenintegration (DI) mithilfe der Entität **Ergebnis der Zahlungsvorhersage (Vorschauversion)** konfiguriert. Nach einem Upgrade auf 10.0.17 und höher sollten Sie die DI-Vorlage **Ergebnisse der Customer Payment Insights (CDS für Fin and Ops 10.0.17 und höher)** verwenden, um die Zuordnung abzuschließen. Möglicherweise können Sie die Zielspalte der DI-Vorlage erst zuordnen, wenn die Liste der Datenverwaltungsentitäten aktualisiert wurde und die Entität **Ergebnis der Zahlungsvorhersage** darin angezeigt wird. Führen Sie die Schritte in Microsoft Dynamics 365 Finance und Dataverse (bisher als Common Data Service \[CDS\] Administratorportal bezeichnet) aus, um die Entitätsliste zu aktualisieren und das Ergebnis der Zahlungsvorhersage anzuzeigen.

### <a name="in-finance"></a>In Finance

Führen Sie nach dem Upgrade diese Schritte in Finance aus.

1. Wechseln Sie zu **Systemverwaltung \> Arbeitsbereiche \> Datenverwaltung**.
2. Wählen Sie im Arbeitsbereich **Datenmanagement** die Kachel **Framework-Parameter** aus.
3. Wählen Sie auf der Seite **Rahmenparameter für den Datenimport/-Export** die Option **Entitätseinstellungen** und dann **Entitätsliste aktualisieren** aus.
4. Schließen Sie die Seite **Rahmenparameter für den Datenimport/-Export**.
5. Im Arbeitsbereich **Datenmanagement** wählen Sie die Kachel **Datenentitäten**.
6. Suchen Sie nach „Ergebnis der Zahlungsvorhersage“. Stellen Sie sicher, dass es sich bei der Entität **Ergebnis der Zahlungsvorhersage** nicht um die Vorschauversion handelt. Der Name der Vorschauversion endet auf „(Vorschauversion)“. Wenn nur die Vorschauversion der Entität angezeigt wird, wenden Sie sich an den Microsoft-Support.

### <a name="in-dataverse"></a>In Dataverse

Führen Sie diese Schritte im [Power Platform Admin-Center](https://admin.powerplatform.microsoft.com/environments) aus, um Ihre Datenintegrationsprojekte zu aktualisieren.

1. Wenn Sie eine Vorschauversion von Finance Insights verwenden, entfernen Sie das DI-Projekt, das der Vorlage **Ergebnisse der Kundenzahlungserkenntnisse (CDS zu Fin und Ops)** zugeordnet ist.
2. Führen Sie die Schritte unter [Datenintegratorprojekt erstellen](create-data-integrate-project.md) aus. Verwenden Sie die Vorlage **Ergebnisse der Customer Payment Insights (CDS für Fin and Ops 10.0.17 und höher)** verwenden.

## <a name="symptom-when-i-try-to-open-ai-builder-by-using-the-links-on-the-customer-payment-predictions-setup-page-why-do-i-receive-the-following-error-message-sorry-theres-been-a-disconnect"></a>Symptom: Warum erhalte ich die folgende Fehlermeldung, wenn ich versuche, AI Builder über die Links auf der Einstellungsseite für Vorhersagen für Kundenzahlungen zu öffnen: „Entschuldigung, die Verbindung wurde unterbrochen“?

### <a name="resolution"></a>Lösung

Dynamics 365 Finance Benutzer müssen ein Microsoft Power Apps Benutzerkonto für die Umgebung haben, und dieses Benutzerkonto muss die Rolle Systemanpasser haben. Der Microsoft Power Apps Systemadministrator kann das Benutzerkonto erstellen und die Rolle zuweisen. Dann können Sie zu <https://make.preview.powerapps.com/> gehen, sich mit diesem Benutzerkonto anmelden und es erneut mit den Links versuchen.

## <a name="symptom-why-doesnt-the-cash-forecast-tab-in-the-cash-flow-forecast-workspace-show-any-data"></a>Symptom: Warum zeigt die Registerkarte „Bargeldplanung“ im Arbeitsbereich „Cashflow-Planungen“ keine Daten an?

### <a name="resolution"></a>Lösung

Die Cashflow-Prognose-Funktion in der Bargeld- und Bankverwaltung und die Cashflow-Prognose-Funktion in Finance Insights müssen korrekt eingerichtet und aktiviert sein, damit die Daten im Arbeitsbereich **Cashflow-Planungen** angezeigt werden.

Richten Sie zunächst die Cashflow-Vorhersage und die Liquiditätskonten ein, und aktivieren Sie sie. Weitere Informationen unter [Cashflowprognosen](../cash-bank-management/cash-flow-forecasting.md). Wenn diese Einrichtung abgeschlossen ist, die erwarteten Ergebnisse jedoch nicht angezeigt werden, finden Sie weitere Informationen unter [Problembehandlung beim Einrichten der Cashflow-Planung](../cash-bank-management/cash-flow-forecasting-tsg.md).

Bestätigen Sie als Nächstes, dass die Funktion „Cashflow-Planungen“ in Finance Insights (**Bargeld- und Bankverwaltung \> Einrichtung \> Finance Insights \> Cashflow-Planungen**) aktiviert wurde und das Training des KI-Modells abgeschlossen ist. Wenn die Schulung nicht abgeschlossen ist, wählen Sie **Jetzt planen** aus, um den Modelltrainingsprozess zu starten.

## <a name="symptom-why-isnt-the-install-a-new-add-in-button-visible-in-microsoft-dynamics-lifecycle-services"></a>Symptom: Warum ist die Schaltfläche „Neues Add-In installieren“ in Microsoft Dynamics Lifecycle Services nicht sichtbar?

### <a name="resolution"></a>Lösung

Stellen Sie zunächst sicher, dass entweder die **Umgebungsmanager** oder **Projektbesitzer**-Rolle dem Benutzer im **Projektsicherheitsrolle**-Feld in Microsoft Dynamics Lifecycle Services (LCS) zugewiesen werden. Für die Installation der neuen Add-Ins ist eine dieser Projektsicherheitsrollen erforderlich.

Wenn Ihnen die richtige Projektsicherheitsrolle zugewiesen ist, müssen Sie möglicherweise Ihr Browserfenster aktualisieren, um die **Neues Add-In installieren**-Schaltfläche anzuzeigen.

## <a name="symptom-the-finance-insights-add-in-doesnt-seem-to-be-installing-why-is-that"></a>Symptom: Das Finance Insights-Add-In scheint nicht installiert zu werden. Warum ist das so?

### <a name="resolution"></a>Lösung

Die folgenden Schritte sollten abgeschlossen sein.

- Stellen Sie sicher, dass Sie **Systemadministrator** und **Systemanpasser**-Zugriff im Power Portal Admin Center haben.
- Stellen Sie sicher, dass eine Dynamics 365 Finance- oder eine gleichwertige Lizenz auf den Benutzer angewendet wird, der das Add-In installiert.
- Stellen Sie sicher, dass folgende Azure AD-App in Azure AD registriert ist: 

  | Bewerbung                  | App-Kennung           |
  | ---------------------------- | ---------------- |
  | Microsoft Dynamics ERP-Microservices-CDS | 703e2651-d3fc-48f5-942c-74274233dba8 | 
  
## <a name="symptom-error-we-didnt-find-any-data-for-the-selected-filter-range-please-select-a-different-filter-range-and-try-again"></a>Symptom: Fehler, „Wir haben keine Daten für den ausgewählten Filterbereich gefunden. Bitte wählen Sie einen anderen Filterbereich und versuchen Sie es erneut.“ 

### <a name="resolution"></a>Lösung

Überprüfen Sie die Einrichtung des Datenintegrators, um sicherzustellen, dass er wie erwartet funktioniert und die Daten von AI Builder wieder in Finance einfügt.  
Weitere Informationen finden Sie unter [Erstellen Sie ein Datenintegrationsprojekt](../finance-insights/create-data-integrate-project.md).

## <a name="symptom-customer-payment-prediction-training-failed-and-the-ai-builder-error-states-prediction-should-have-only-2-distinct-outcome-values-to-train-the-model-map-to-two-outcomes-and-retrain-training-report-issue-isnotminrequireddistinctnonnullvalues"></a>Symptom: Das Training der Vorhersage von Debitorenzahlungen ist fehlgeschlagen und der Status AI Builder besagt: „Die Vorhersage sollte nur 2 verschiedene Ergebniswerte haben, um das Modell zu trainieren. Zuordnung zu zwei Ergebnissen und erneute Schulung“, „Problem mit dem Schulungsbericht: IsNotMinRequiredDistinctNonNullValues“.

### <a name="resolution"></a>Lösung

Dieser Fehler deutet darauf hin, dass es im letzten Jahr nicht genügend historische Transaktionen gibt, die jede der in den Kategorien **Pünktlich**, **Spät** und **Sehr spät** beschriebenen Kategorien repräsentieren. Um diesen Fehler zu beheben, passen Sie den Zeitraum für **Sehr spät** Transaktionen an. Wenn die Anpassung des **Sehr spät** Transaktionszeitraums den Fehler nicht behebt, ist **Zahlungsvorhersagen für Kunden** nicht die beste Lösung, da es für Trainingszwecke Daten in jeder Kategorie benötigt.

Weitere Informationen über die Anpassung der Kategorien **Pünktlich**, **Verspätet** und **Sehr verspätet** finden Sie unter [Zahlungsvorhersagen für Debitor aktivieren](../finance-insights/enable-cust-paymnt-prediction.md).

## <a name="symptom-model-training-failed"></a>Symptom: Modelltraining fehlgeschlagen

### <a name="resolution"></a>Lösung

Für das Training des Modells **Cashflow Planung** werden Daten benötigt, die mehr als 100 Transaktionen enthalten und sich über mehr als ein Jahr erstrecken. Wir empfehlen Ihnen mindestens zwei Jahre Daten mit mehr als 1.000 Transaktionen.

Die Funktion **Vorhersagen für Kundenzahlungen** erfordert mehr als 100 Transaktionen in den letzten sechs bis neun Monaten. Bei den Transaktionen kann es sich um Freitextrechnungen, Verkaufsaufträge und Kundenzahlungen handeln. Diese Daten müssen über die Einstellungen **Pünktlich**, **Spät** und **Sehr spät** verteilt sein, die auf der Seite **Konfiguration** sind.    

Die Funktion **Budgetvorschlag** erfordert Budget- oder Istdaten aus mindestens drei Jahren. Diese Lösung verwendet drei bis zehn Jahre Daten in den Projektionen. Mehr als drei Jahre liefern bessere Ergebnisse. Die Daten selbst funktionieren am besten, wenn die Werte variieren. Wenn die Daten nur konstante Daten enthalten, wie z. B. Leasingkosten, kann das Training fehlschlagen, da die KI aufgrund der fehlenden Abwechslung keine Prognosen der Beträge erstellen muss.

## <a name="symptom-error-message-states-that-the-table-with-name-msdyn_paypredpredictionresultentities-does-not-exist-the-remote-server-returned-an-error-404-not-found"></a>Symptom: Die Fehlermeldung besagt, dass die „Tabelle mit dem Namen ‚msdyn_paypredpredictionresultentities‘ nicht existiert. Der Remoteserver hat einen Fehler zurückgegeben: (404) nicht gefunden ...“

### <a name="resolution"></a>Lösung

Die Umgebung hat den maximalen Tabellengrenzwert der Data-Lake-Services erreicht. Weitere Informationen zum Limit finden Sie im Abschnitt **Datenänderungen in Quasi-Echtzeit aktivieren** des Themas [Übersicht über den Export in Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/Azure-Data-Lake-GA-version-overview.md).
