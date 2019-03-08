---
title: Power BI-Inhalt zur Kredit- und Inkassoverwaltung
description: In diesem Thema wird beschrieben, was im Power BI-Inhalt zur Kredit und Inkassoverwaltung enthalten ist. Es erläutert, wie Sie auf die Power BI-Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a80a180623d1cca77c633f12bcd92a088e089ee5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "325180"
---
# <a name="credit-and-collections-management-power-bi-content"></a>Power BI-Inhalt zur Kredit- und Inkassoverwaltung

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, was im Microsoft Power BI-Inhalt zur **Kredit und Inkassoverwaltung** enthalten ist. Es erläutert, wie Sie auf die Power BI-Berichte zugreifen, und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet wurden, um den Inhalt zu erstellen.

## <a name="overview"></a>Übersicht

Der Power BI-Inhalt zur **Kredit- und Inkassoverwaltung** wurde für Kredit- und Inkassoverwalter und Inkassobearbeiter erstellt. Er bietet wichtige Kredit- und Inkasso-Metriken, wie ausstehende Verkäufe in Tagen, überfälliger Saldo, Kreditrisken und Debitoren, die das Kreditlimit überschritten haben. Es verwendet Transaktionsdaten und bietet Aggregatansichten von Kredit- und Inkassovorgängen für alle Unternehmen. Er bietet auch eine Aufschlüsselung pro Unternehmen, Debitorengruppe und Debitor.

Dieser Power BI-Inhalt besteht aus 10 Berichtsseiten:

- Zwei Überblicksseiten (eine Seite für einen Kreditüberblick und eine Seite für einen Inkassoüberblick)
- Acht Detailseiten, die Details der Kredit- und Inkassometriken liefern, die in verschiedene Dimensionen und aufgeteilt sind

Alle Beträge werden in der Systemwährung angezeigt. Sie können die Systemwährung auf der Seite **Systemparameter** festlegen.

Standardmäßig wird die Kredit- und Inkassodaten für das aktuelle Unternehmen angezeigt. Um die Daten für alle Unternehmen anzuzeigen, weisen Sie der Rolle die Berechtigung **CustCollectionsBICrossCompany** zu.

## <a name="accessing-the-power-bi-content"></a>Zugreifen auf den Power BI-Inhalt
Der Power BI-Inhalt zur **Kredit- und Inkassoverwaltung** wird im Arbeitsbereich **Debitorenkredit und Inkasso** angezeigt.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Berichte, die im Power BI-Inhalt enthalten sind

Der Power BI-Inhalt zu **CustCollectionsBICrossCompany** umfasst einen Bericht, der aus einem Satz von Metriken besteht. Diese Metrik werden als Diagramme, Kacheln und Tabellen visuell dargestellt. Die folgende Tabelle enthält eine Übersicht der Visualisierungen im Power BI-Inhalt zu **CustCollectionsBICrossCompany**.

| Berichtsseiten                 | Darstellung |
|-----------------------------|---------------|
| Inkassoüberblick        | <ul><li>Überfällige Debitoren</li><li>Debitoren über Kreditlimit</li><li>DSO 30 Tage</li><li>Offene Anfragen</li><li>Durchschnittliche Anzahl der Tage bis zum Schließen eines Falls</li><li>Offene Aktivitäten</li><li>Durchschnittliche Anzahl der Tage bis zum Schließen von Aktivitäten</li><li>Offene Zinsrechnungen</li><li>Offene Mahnschreiben</li><li>Debitorensperre</li><li>Umsatzsperre</li><li>Saldenrückblick</li><li>Inkassostatusbeträge</li><li>Inkassocodebeträge</li><li>Abschreibung nach Grund</li><li>Fällige Salden nach Region</li><li>Erwartete Zahlungen</li></ul> |
| Kreditüberblick             | <ul><li>Überfällige Debitoren</li><li>Kreditlimit gegenüber fälligem Saldo</li><li>Debitoren über Kreditlimitraster</li><li>Debitoren über Kreditlimit pro Unternehmen</li><li>Verwendete Gutschrift im Vgl. zu Kreditlimit</li><li>Kreditlimit im Vgl. zu verwendeter Gutschrift nach Region</li><li>Debitoren pro Kreditwürdigkeit</li></ul> |
| Kreditlimit                | <ul><li>Kreditlimit</li><li>Kreditlimitdetails</li><li>Kreditlimit pro Debitor</li><li>Kreditlimit pro Debitorengruppe</li><li>Kreditlimit pro Kreditwürdigkeit pro Unternehmen</li><li>Kreditlimit im Vgl. zu verwendete Gutschrift nach Region</li></ul> |
| Debitoren über Kreditlimit | <ul><li>Debitoren über Kreditlimit</li><li>Details zu Debitoren über Kreditlimit</li><li>Debitoren über Kreditlimit pro Unternehmen</li><li>Debitor über Kreditlimit pro Debitorengruppe</li><li>Debitoren über Kreditlimit nach Region</li></ul> |
| Überfällige Debitoren          | <ul><li>Überfällige Debitoren</li><li>Details zu überfälligen Debitoren</li><li>Überfälliger Debitor pro Unternehmen</li><li>Überfälliger Debitor pro Debitorengruppe</li><li>Überfälliger Debitor nach Region</li></ul> |
| Saldenrückblick               | <ul><li>Saldenrückblick</li><li>Details zu Saldenrückblicken</li><li>Saldenrückblicke pro Unternehmen</li><li>Saldenrückblicke pro Debitorengruppe</li></ul> |
| Erwartete Zahlungen           | <ul><li>Erwartete Zahlungen</li><li>Details zu erwarteten Zahlungen</li><li>Erwartete Zahlungen pro Unternehmen</li><li>Erwartete Zahlungen pro Debitorengruppe</li><li>Erwartete Zahlungen nach Region</li></ul> |
| Abschreibungen                  | <ul><li>Abschreibungen nach Regionen</li><li>Details zu Abschreibungen</li><li>Abschreibungen nach Hauptkonto</li><li>Abschreibungen pro Unternehmen</li><li>Abschreibungen pro Debitorgruppe</li><li>Abschreibungen nach Regionen</li></ul> |
| Inkassostatus          | <ul><li>Strittig</li><li>Zahlungszusage nicht eingehalten</li><li>Zahlungszusage</li><li>Inkassostatussetails</li><li>Inkassostatusbeträge</li><li>Offene Anfragen</li><li>Offene Aktivitäten</li></ul> |
| Mahnschreiben         | <ul><li>Sammlungscodebeträge</li><li>Details zu Sammlungscodebeträgen</li><li>Mahnschreibenbetrag pro Unternehmen</li><li>Mahnschreibenbetrag pro Debitorengruppe</li><li>Mahnschreibenbetrag nach Region</li></ul> |

Die Diagramme und die Kacheln auf allen diesen Berichten können gefiltert und an das Dashboard geheftet werden. Weitere Informationen dazu, wie Sie in Power BI filtern und anheften, finden Sie unter [Erstellen und Konfigurieren eines Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Sie können auch die Funktionen zum Export zugrunde liegender Daten verwenden, um die zugrunde liegenden Daten zu exportieren, die in einer Visualisierung zusammengefasst sind.

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen

Die folgenden Daten werden verwendet, um den Bericht im Power BI-Inhalt zur **Kredit- und Inkassoverwaltung** auszufüllen. Diese Daten werden als gesamte Messungen dargestellt, die im Entitätsshop bereitgestellt werden. Der Entitätsshop ist eine Microsoft SQL Server-Datenbank, die für die Analyse optimiert ist. Weitere Informationen finden Sie in der [Übersicht Power BI-Integration mit Entitätsspeicher](../../dev-itpro/analytics/power-bi-integration-entity-store.md).


|                   Entität                    |      Zentrale aggregierte Messungen      |             Datenquelle              |                           Feld                            |                                    Beschreibung                                     |
|---------------------------------------------|--------------------------------------|--------------------------------------|------------------------------------------------------------|------------------------------------------------------------------------------------|
| CustCollectionsBIActivitiesAverageCloseTime | NumOfActivities, AveragecClosedTime  |            smmActivities             | AverageOfChildren (AverageClosedTime) Count(ActivityNumber) |     Die Anzahl der abgeschlossenen Aktivitäten und die Durchschnittszeit zum Schließen der Aktivitäten.     |
|       CustCollectionsBIActivitiesOpen       |            ActivityNumber            |            smmActivities             |                   Count(ActivityNumber)                    |                           Die Anzahl der offenen Aktivitäten.                            |
|        CustCollectionsBIAgedBalances        |             AgedBalances             |  CustCollectionsBIAgedBalancesView   |                 Sum(SystemCurrencyBalance)                 |                             Die Summe der Saldenrückblicke.                              |
|        CustCollectionsBIBalancesDue         |         SystemCurrencyAmount         |   CustCollectionsBIBalanceDueView    |                 Sum(SystemCurrencyAmount)                  |                           Die Beträge, die überfällig sind.                            |
|    CustCollectionsBICaseAverageCloseTIme    |  NumOfCases, CaseAverageClosedTime   |      CustCollectionsCaseDetail       | AverageOfChildren(CaseAverageClosedTime) Count(NumOfCases) |        Die Anzahl der abgeschlossenen Fälle und die Durchschnittszeit zum Schließen dieser Fälle.        |
|         CustCollectionsBICasesOpen          |                CaseId                |      CustCollectionsCaseDetail       |                       Count(CaseId)                        |                              Die Anzahl der offenen Fälle.                              |
|      CustCollectionsBICollectionLetter      |         CollectionLetterNum          |       CustCollectionLetterJour       |                 Count(CollectionLetterNum)                 |                       Die Anzahl der offenen Mahnschreiben.                        |
|   CustCollectionsBICollectionLetterAmount   |       CollectionLetterAmounts        | CustCollectionsBIAccountsReceivables |                 Sum(SystemCurrencyAmount)                  |                     Der Saldo der gebuchten Mahnschreiben.                      |
|      CustCollectionsBICollectionStatus      |       CollectionStatusAmounts        | CustCollectionsBIAccountsReceivables |                 Sum(SystemCurrencyAmount)                  |                Der Saldo der Buchungen mit Inkassostatus.                 |
|           CustCollectionsBICredit           | CreditExposed, AmountOverCreditLimit |     CustCollectionsBICreditView      |       Sum(CreditExposed), Sum(AmountOverCreditLimit)       | Die Summe der Kreditrisiken und Beträge, die Debitoren über dem Kreditlimit sind. |
|         CustCollectionsBICustOnHold         |               Gesperrt                |      CustCollectionsBICustTable      |                       Count(Blocked)                       |                     Die Anzahl der Debitoren, die gesperrt sind.                      |
|            CustCollectionsBIDSO             |                DSO30                 |       CustCollectionsBIDSOView       |                  AverageOfChildren(DSO30)                  |                        Tage ausstehender Verkäufe für 30 Tage.                         |
|      CustCollectionsBIExpectedPayment       |           ExpectedPayment            | CustCollectionsBIExpectedPaymentView |                 Sum(SystemCurrencyAmounts)                 |                 Die Summe der erwarteten Zahlungen innerhalb des nächsten Jahrs.                 |
|        CustCollectionsBIInterestNote        |             InterestNote             |           CustInterestJour           |                    Count(InterestNote)                     |                Die Anzahl der erstellten Zinsrechnungen.                |
|        CustCollectionsBISalesOnHold         |               SalesId                |              SalesTable              |                       Count(SalesId)                       |                 Die Anzahl der gesamten Aufträge, die gesperrt sind.                 |
|          CustCollectionsBIWriteOff          |            WriteOffAmount            |    CustCollectionsBIWriteOffView     |                 Sum(SystemCurrencyAmount)                  |                Die Gesamtanzahl der Buchungen, die abgeschrieben wurden.                 |

