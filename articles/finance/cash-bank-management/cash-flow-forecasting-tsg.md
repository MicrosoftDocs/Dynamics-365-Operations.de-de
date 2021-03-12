---
title: Problembehandlung bei Einrichtung der Cashflow-Planung
description: Dieses Thema enthält Antworten auf Fragen, die Sie möglicherweise haben, wenn Sie die Cashflow-Planung konfigurieren. Behandelt werden häufig gestellte Fragen (FAQ) zur Einrichtung des Cashflows sowie zu Aktualisierungen des Cashflows und des Power BI-Cashflows.
author: panolte
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 89eb2f1bcfc73a6a7171a275532b2356e858e87c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985286"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a>Problembehandlung bei Einrichtung der Cashflow-Planung

[!include [banner](../includes/banner.md)]

Dieses Thema enthält Antworten auf Fragen, die Sie möglicherweise haben, wenn Sie die Cashflow-Planung konfigurieren. Behandelt werden häufig gestellte Fragen (FAQ) zur Einrichtung des Cashflows sowie zu Aktualisierungen des Cashflows und des Power BI-Cashflows.

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a>Warum wird der Cashflow nur für eine juristische Person angezeigt?

Die Cashflow-Planung wird pro juristischer Person konfiguriert und berechnet. Power BI-Berichte und die Funktion zur Cashflow-Planung in Finance Insights zeigen die Ergebnisse an.

Die Cashflow-Planung muss für jede juristische Person eingerichtet werden, für die Sie sich eine Planung anzeigen lassen möchten. Überprüfen Sie die Konfiguration der Cashflow-Planung in allen Ihren juristischen Personen. Überprüfen Sie alternativ die Konfiguration aller juristischen Personen für die Cashflow-Planung, und stellen Sie sicher, dass sie wie beabsichtigt festgelegt sind.

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a>Warum zeigt Power BI nicht alle Cashflow-Daten an?

Es müssen mehrere Schritte ausgeführt werden, bevor Cashflow-Planungen in Power BI-Ansichten angezeigt werden können. Überprüfen Sie die folgende Checkliste, und stellen Sie sicher, dass jeder Schritt abgeschlossen wurde:

- Richten Sie den Cashflow für jede juristische Person ein.
- Legen Sie in den Hauptbuchparametern die Systemwährung und den -wechselkurstyp fest.
- Legen Sie die Buchhaltungswährung für Sachkonto sowie den Wechselkurstyp fest.
- Geben Sie die Wechselkurse zwischen der Buchungswährung und der Buchhaltungswährung ein.
- Geben Sie die Wechselkurse zwischen der Buchhaltungswährung und der Systemwährung ein.
- Geben Sie die Wechselkurse zwischen der Buchhaltungswährung und jeder Bankwährung ein.

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a>Warum funktionierte der Cashflow-Power BI in früheren Versionen, ist jetzt aber leer?

Stellen Sie sicher, dass die Messungen „Cashflow Measure V2“ und „LedgerCovLiquidityMeasurement“ aus dem Entitätsspeicher konfiguriert wurden. Weitere Informationen zum Arbeiten mit Daten im Entitätsspeicher finden Sie unter [Power BI-Integration mit Entitätsspeicher](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md). Stellen Sie sicher, dass alle Schritte zum Anzeigen von Power BI-Inhalten abgeschlossen sind. Weitere Informationen finden Sie unter [Bargelübersicht Power BI Inhalt](Cash-Overview-Power-BI-content.md).

## <a name="have-the-entity-store-entities-been-refreshed"></a>Wurden die Entitätsspeicher-Entitäten aktualisiert?

Sie müssen Ihre Entitäten regelmäßig aktualisieren, um sicherzustellen, dass die Daten aktuell und korrekt sind. Rufen Sie **Systemverwaltung \> Einrichtung \> Entitätsspeicher** auf. Wählen Sie die Entität und anschließend **Aktualisieren** aus, um eine bestimmte Entität manuell zu aktualisieren. Die Daten können auch automatisch aktualisiert werden. Setzen Sie auf der Seite **Entitätsspeicher** die Option **Automatische Aktualisierung aktiviert** auf **Ja**.
