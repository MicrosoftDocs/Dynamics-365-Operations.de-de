---
title: Problembehandlung beim Einrichten von Finance Insights
description: In diesem Thema werden Probleme aufgelistet, die auftreten können, wenn Sie die Funktionen von Finance Insights verwenden. Außerdem wird erläutert, wie Sie diese Probleme beheben können.
author: panolte
ms.date: 11/03/2021
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
ms.openlocfilehash: c1bbdbec2bc0273a73ffc13a4cce024543af5a13
ms.sourcegitcommit: 133aa728b8a795eaeaef22544f76478da2bd1df9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968835"
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
  
