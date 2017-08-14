---
title: "Power BI-Inhalt – Bargeldüberblick"
description: "In diesem Thema wird der Inhalt des Power BI-Bargeldüberblicks beschrieben. Es wird beschrieben, wie auf die Berichte, die im Inhalt enthalten sind, zugegriffen wird und es werden Informationen zum Datenmodell und den Entitäten bereitgestellt, die zum Erstellen des Inhalts verwendet wurden."
author: saraschi2
manager: AnnBe
ms.date: 06/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30T00:00:00.000Z
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 367fe61492648ee3ee629a8121e664dfaa0c6c99
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---

# <a name="cash-overview-power-bi-content"></a>Power BI-Inhalt – Bargeldüberblick

[!include[banner](../includes/banner.md)]

In diesem Thema wird der Inhalt des Microsoft Power BI-**Bargeldüberblicks** beschrieben. Es wird beschrieben, wie auf die Berichte, die im Inhalt enthalten sind, zugegriffen wird und es werden Informationen zum Datenmodell und den Entitäten bereitgestellt, die zum Erstellen des Inhalts verwendet wurden.

## <a name="overview"></a>Überblick

Der Power BI-**Bargeldüberblick** wurde für Personen erstellt, die in ihrer Organisation für das Bargeld zuständig sind. Die Power BI-**Bargeldüberblick** ermöglicht Sichtbarkeit des Cashflows. Es enthält auch Planungen, die Sie beim Treffen besserer Entscheidungen unterstützen, und daher den Status Ihres Cashflows verbessern. Sie können die Bargeld nach juristischer Person, Währung und Bankkonto analysieren, um ein besseres Verständnis für Überschüsse und Defizite zu erhalten.

## <a name="accessing-the-power-bi-content"></a>Zugreifen au Power BI Inhalt

Wenn Sie das Update von Juli 2017 für Dynamics 365 for Finance and Operations, Enterprise-Edition, verwenden, werden Berichte vom **Bargeldüberblick**-Inhalt von Power BI in den Arbeitsbereichen **Bargeldüberblick** und **Bankverwaltung** angezeigt.

Um die Bargeld-Planungsberichte mit Daten anzuzeigen, müssen Sie zuerst die Planungsberechnung unter Verwendung der Funktion **Bargeld-Planungen berechnen** aus dem Bereich Bargeld- und Bankverwaltung durchführen.  Dies muss für jedes in die Planung aufgenommene Unternehmen stattfinden.  Anschließend müssen Sie die LedgerCovLiquidityMeasurement-Aggregatmessung auf der Seite **Entitätsspeicher** aktualisieren.  

Für Demonstrationszwecke können Sie Demodaten für die Bargeld-Planung unter Verwendung der Seite **Daten generieren** im Demodatenmodul hinzufügen.  Dieses Skript fügt Daten in die Bargeld-Planungstabellen ein, um schnell die für Berichte benötigten Informationen bereitzustellen.  Dieses Modul steht nur zur Verfügung, wenn Sie das Demo-Datenpaket-Modell in der Umgebung bereitgestellt haben. 

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Berichte, die im Power BI Inhalt enthalten sind
Die folgende Tabelle enthält Details zur Metrik, die sich auf jeder Berichtsseite im BI-Inhalt **Bargeldüberblick** befinden.

| Bericht                                | Inhalt |
|---------------------------------------|----------|
| Bargeldüberblick – alle Unternehmen         | <ul><li>Zu- und Abflüsse in Systemwährung</li><li>Prognostizierte Währungssalden</li><li>Gesamter Banksaldo in der Systemwährung</li><li>Saldo nach juristischer Person</li><li>Vergleich des heutigen Ist-Saldos gegenüber des geplanten Saldos in Bankkontowährung</li></ul> |
| Bargeldüberblick – aktuelles Unternehmen       | <ul><li>Zu- und Abflüsse in Buchführungswährung</li><li>Prognostizierte Währungssalden</li><li>Gesamter Banksaldo in Buchhaltungswährung</li><li>Vergleich des heutigen Ist-Saldos gegenüber des geplanten Saldos in Bankkontowährung</li></ul> |
| Cashflowplanung – alle Unternehmen    | <ul><li>Zu- und Abflüsse in Systemwährung</li><li>Tägliche Planungsüberblick</li><li>Planungsdetails</li></ul> |
| Cashflow-Planung – Währungsunternehmen | <ul><li>Zu- und Abflüsse in Buchführungswährung</li><li>Tägliche Planungsüberblick</li><li>Planungsdetails</li></ul> |
| Währungsplanung                     | <ul><li>Prognostizierte Währungssalden</li><li>Tägliche Währungsüberblick</li><li>Planungsdetails</li></ul> |
| Banksalden                         | <ul><li>Gesamter Banksaldo in der Systemwährung</li><li>Saldo nach juristischer Person</li><li>Vergleich des heutigen Ist-Saldos gegenüber des geplanten Saldos in Bankkontowährung</li><li>Saldo nach Bankkonto</li><li>Saldo in Währung</li></ul> |

## <a name="extending-the-power-bi-content"></a>Erweitern des Power BI-Inhalts
Sie können Personen, die sich nicht bei Dynamics 365 anmelden, großartige Analysen bereitstellen, indem Sie die Inhaltspakete verwenden, die in den Lifecycle Services (LCS) verfügbar sind. Diese Inhaltspakete können angepasst werden, damit Sie weitere Berichte oder grafische Elemente umfassen, und dann zur Analyse auf Ihrem Power BI.com-Mandanten veröffentlicht werden. 

Sie können die **Bargeldüberblick**-Power BI-Inhalt in der freigebenen Anlagenbibliothek in LCS finden. Weitere Informationen dazu, wie Sie Power BI-Inhalte herunterladen und in Ihrer Organisation implementieren, finden Sie unter [Power BI-Inhalt in LCS von Microsoft und Ihren Partnern](/dynamics365/unified-operations/dev-itpro/analytics/power-bi-content-microsoft-partners). Um eine Vorführung anzusehen, die zeigt, wie der Power BI-Inhalt impementiert wird, zeigen Sie den Office Mix [Power BI-Inhalt von Microsoft und Ihren Partnern in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) an.

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen

Die folgende Tabelle zeigt die Entitäten, auf denen das der **Bargeldüberblick**-Inhalt von Power BI basiert.

| Entität                                                                          | Inhalt |
|---------------------------------------------------------------------------------|----------|
| LedgerCovLiquidityMeasurement\_Company                                          | Unternehmen, nach denen Berichte gefiltert werden können |
| LedgerCovLiquidityMeasurement\_Date                                             | Daten, nach denen Berichte gefiltert werden können |
| LedgerCovLiquidityMeasurement\_LedgerCovForecastActual                          | Tatsächlicher Banksaldo gegenüber letztem prognostiziertem Banksaldo |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidity                               | Progonstizierte Buchungsdetails |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceCompany    | Zusammengefasste Bargeldzu- und -abflüsse und -saldo mithilfe der Buchhaltungswährung jedes Unternehmens |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceEnterprise | Zusammengefasste Bargeldzu- und -abflüsse und -saldo mithilfe der Systemwährung für alle Unternehmen |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityTransactionCurrency            | Zusammengefasster und Nettobuchungsbetrag und -saldo von Währungen anhand der Buchungswährung |

Diese Entitäten wurden verwendet, um berechnete Messungen im Datenmodell zu erstellen. Diese berechneten Messungen werden verwendet, um die Diagramme und Berichte zu erstellen, die im **Bargeldüberblick**-Inhalt verwendet werden. Um zusätzliche Berechnungen in Ihren Berichten und Dashboard einzubeziehen, können Sie die Power BI-Datei von LCS herunterladen und bearbeiten. Diese Datei ist das Standarddatenmodell, das verwendet wurde, um den Inhalt zu erstellen. Nachdem Sie die Änderungen vorgenommen haben, können Sie Organisations-Inhalte und Dashboards erstellen, die die von Ihnen hinzugefügten Informationen enthalten.


