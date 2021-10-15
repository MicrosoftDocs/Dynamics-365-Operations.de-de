---
title: Problembehandlung beim Einrichten von Finance Insights
description: In diesem Thema werden Probleme aufgelistet, die auftreten können, wenn Sie die Funktionen von Finance Insights verwenden. Außerdem wird erläutert, wie Sie diese Probleme beheben können.
author: panolte
ms.date: 08/20/2021
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
ms.openlocfilehash: 7ff42ffc334147c1a4c6b6349c86580df7f1955b
ms.sourcegitcommit: 47a3ad71210c7ac84d0c25e913c440b5ba205282
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2021
ms.locfileid: "7512889"
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

## <a name="symptom-why-doesnt-the-cash-forecast-tab-in-the-cash-flow-forecast-workspace-show-any-data"></a>Symptom: Warum zeigt die Registerkarte „Bargeldplanung“ im Arbeitsbereich „Cashflow-Planungen“ keine Daten an?

### <a name="resolution"></a>Lösung

Die Cashflow-Prognose-Funktion in der Bargeld- und Bankverwaltung und die Cashflow-Prognose-Funktion in Finance Insights müssen korrekt eingerichtet und aktiviert sein, damit die Daten im Arbeitsbereich **Cashflow-Planungen** angezeigt werden.

Richten Sie zunächst die Cashflow-Vorhersage und die Liquiditätskonten ein, und aktivieren Sie sie. Weitere Informationen unter [Cashflowprognosen](../cash-bank-management/cash-flow-forecasting.md). Wenn diese Einrichtung abgeschlossen ist, die erwarteten Ergebnisse jedoch nicht angezeigt werden, finden Sie weitere Informationen unter [Problembehandlung beim Einrichten der Cashflow-Planung](../cash-bank-management/cash-flow-forecasting-tsg.md).

Bestätigen Sie als Nächstes, dass die Funktion „Cashflow-Planungen“ in Finance Insights (**Bargeld- und Bankverwaltung \> Einrichtung \> Finance Insights \> Cashflow-Planungen**) aktiviert wurde und das Training des KI-Modells abgeschlossen ist. Wenn die Schulung nicht abgeschlossen ist, wählen Sie **Jetzt planen** aus, um den Modelltrainingsprozess zu starten.
