---
title: Power BI-Inhalt – Bargeldübersicht
description: In diesem Thema wird der Inhalt des Power BI-Bargeldüberblicks beschrieben. Es wird beschrieben, wie auf die Berichte, die im Inhalt enthalten sind, zugegriffen wird und es werden Informationen zum Datenmodell und den Entitäten bereitgestellt, die zum Erstellen des Inhalts verwendet wurden.
author: saraschi2
manager: AnnBe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 0f10022ae4906972d08e08e3e5476630213468d6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985460"
---
# <a name="cash-overview-power-bi-content"></a>Power BI-Inhalt – Bargeldübersicht

[!include [banner](../includes/banner.md)]

In diesem Thema wird der Inhalt vom Microsoft Power BI-**Bargeldüberblick** beschrieben. Es wird beschrieben, wie auf die Berichte, die im Inhalt enthalten sind, zugegriffen wird und es werden Informationen zum Datenmodell und den Entitäten bereitgestellt, die zum Erstellen des Inhalts verwendet wurden.

## <a name="overview"></a>Übersicht

Der Power BI-**Bargeldüberblick** wurde für Personen erstellt, die in ihrer Organisation für das Bargeld zuständig sind. Der Power BI-**Bargeldüberblick** ermöglicht die Sichtbarkeit des Cashflows. Es enthält auch Planungen, die Sie beim Treffen besserer Entscheidungen unterstützen, und daher den Status Ihres Cashflows verbessern. Sie können die Bargeld nach juristischer Person, Währung und Bankkonto analysieren, um ein besseres Verständnis für Überschüsse und Defizite zu erhalten.

## <a name="setup-needed-to-view-power-bi-content"></a>Einrichtung erforderlich, um Power BI-Inhalt anzuzeigen

Die folgende Einrichtung muss abgeschlossen werden, damit Daten in den Grafiken **Bargeldüberblick** und **Bankwesen** Power BI angezeigt werden.

1. Wechseln Sie zu **Systemverwaltung > Einrichtung > Systemparameter**, um **Systemwährung** und **Systemwechselkurs** festzulegen.
2. Wechseln Sie zu **Hauptbuch > Kalender > Steuerkalender**, um Steuerkalenderdaten zu überprüfen, die der aktiven Zeitperiode zugewiesen sind.
3. Wechseln Sie zu **Hauptbuch > Einrichtung> Sachkonto**, um **Buchhaltungswährung** und **Wechselkurstyp** festzulegen.
4. Definieren Sie Wechselkurse zwischen Buchungswährungen und der Buchhaltungswährung, Buchhaltungswährung und Systemwährung sowie der Buchhaltungswährung und den Bankwährungen. Wechseln Sie dazu zu **Hauptbuch > Währungen > Währungswechselkurse**.
5. Konfigurieren Sie die Cashflow-Planung und führen Sie sie aus. Weitere Informationen dazu, wie Cashflow-Planung eingerichtet wird, finden Sie unter [Cashflow-Planung](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting). 
6. Wechseln Sie zu **Systemverwaltung > Einrichtung > Entitätsspeicher**, um die **LedgerCovLiquidityMeasurement**-Aggregatmessung zu aktualisieren.

## <a name="accessing-the-power-bi-content"></a>Zugreifen auf den Power BI-Inhalt

Berichte vom Inhalt vom Power BI-**Bargeldüberblick** werden in den Arbeitsbereichen **Bargeldüberblick** und **Bankverwaltung** angezeigt.

Um die Bargeld-Planungsberichte mit Daten anzuzeigen, müssen Sie zuerst die Planungsberechnung unter Verwendung der Funktion **Bargeld-Planungen berechnen** aus dem Bereich Bargeld- und Bankverwaltung durchführen. Dies muss für jedes in die Planung aufgenommene Unternehmen stattfinden.  Anschließend müssen Sie die LedgerCovLiquidityMeasurement-Aggregatmessung auf der Seite **Entitätsspeicher** aktualisieren.  

Für Demonstrationszwecke können Sie Demodaten für die Bargeld-Planung unter Verwendung der Seite **Daten generieren** im Demodatenmodul hinzufügen.  Dieses Skript fügt Daten in die Bargeld-Planungstabellen ein, um schnell die für Berichte benötigten Informationen bereitzustellen.  Dieses Modul steht nur zur Verfügung, wenn Sie das Demo-Datenpaket-Modell in der Umgebung bereitgestellt haben. 

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Berichte, die im Power BI-Inhalt enthalten sind

Die folgende Tabelle enthält Details zur Metrik, die sich auf jeder Berichtsseite im Inhalt vom Power BI-**Bargeldüberblick** befinden.

| Bericht                                | Inhalt |
|---------------------------------------|----------|
| Bargeldüberblick – alle Unternehmen         | <ul><li>Zu- und Abflüsse in Systemwährung</li><li>Prognostizierte Währungssalden</li><li>Gesamter Banksaldo in der Systemwährung</li><li>Saldo nach juristischer Person</li><li>Vergleich des heutigen Ist-Saldos gegenüber des geplanten Saldos in Bankkontowährung</li></ul> |
| Bargeldüberblick – aktuelles Unternehmen       | <ul><li>Zu- und Abflüsse in Buchführungswährung</li><li>Prognostizierte Währungssalden</li><li>Gesamter Banksaldo in Buchhaltungswährung</li><li>Vergleich des heutigen Ist-Saldos gegenüber des geplanten Saldos in Bankkontowährung</li></ul> |
| Cashflowplanung – alle Unternehmen    | <ul><li>Zu- und Abflüsse in Systemwährung</li><li>Tägliche Planungsüberblick</li><li>Planungsdetails</li></ul> |
| Cashflow-Planung – Währungsunternehmen | <ul><li>Zu- und Abflüsse in Buchführungswährung</li><li>Tägliche Planungsüberblick</li><li>Planungsdetails</li></ul> |
| Währungsplanung                     | <ul><li>Prognostizierte Währungssalden</li><li>Tägliche Währungsüberblick</li><li>Planungsdetails</li></ul> |
| Banksalden                         | <ul><li>Gesamter Banksaldo in der Systemwährung</li><li>Saldo nach juristischer Person</li><li>Vergleich des heutigen Ist-Saldos gegenüber des geplanten Saldos in Bankkontowährung</li><li>Saldo nach Bankkonto</li><li>Saldo in Währung</li></ul> |


## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen

Die folgende Tabelle zeigt die Entitäten, auf denen der Inhalt vom Power BI-**Bargeldüberblick** basiert.

| Entität                                                                          | Inhalt |
|---------------------------------------------------------------------------------|----------|
| LedgerCovLiquidityMeasurement\_Company                                          | Unternehmen, nach denen Berichte gefiltert werden können |
| LedgerCovLiquidityMeasurement\_Date                                             | Daten, nach denen Berichte gefiltert werden können |
| LedgerCovLiquidityMeasurement\_LedgerCovForecastActual                          | Tatsächlicher Banksaldo gegenüber letztem prognostiziertem Banksaldo |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidity                               | Progonstizierte Buchungsdetails |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceCompany    | Zusammengefasste Bargeldzu- und -abflüsse und -saldo mithilfe der Buchhaltungswährung jedes Unternehmens |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceEnterprise | Zusammengefasste Bargeldzu- und -abflüsse und -saldo mithilfe der Systemwährung für alle Unternehmen |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityTransactionCurrency            | Zusammengefasster und Nettobuchungsbetrag und -saldo von Währungen anhand der Buchungswährung |
