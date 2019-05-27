---
title: Financial Performance PowerBI.com-Lösung
description: Dieses Thema beschreibt die Financial Performance PowerBI.com-Lösung.
author: kweekley
manager: AnnBe
ms.date: 05/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 78512e39e82e24f94dae93bbac116e6f07d25438
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553951"
---
# <a name="financial-performance-powerbicom-solution"></a>Financial Performance PowerBI.com-Lösung

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Diese PowerBI.com-Lösung ist veraltet, wie in [Power BI-Inhaltspakete auf AppSource](../migration-upgrade/deprecated-features.md#power-bi-content-packs-available-on-appsource) dokumentiert.

Dieses Thema beschreibt die **Financial Performance** PowerBI.com-Lösung. Es beschreibt das Dashboard und die enthaltenen Berichte und liefert Informationen über das Datenmodell und die Entitäten, mit denen die Lösung erstellt wurde.

## <a name="main-account-setup"></a>Hauptkonto einrichten
Da Organisationen möchten, dass Verbindlichkeiten und Umsatzerlöse als positive Beträge auf Berichten angezeigt werden, sind die Einstellungen der Hauptkonten wichtig. Damit diese Hauptkonten als positive Beträge angezeigt werden, muss das Hauptkonto den Typ auf **Verbindlichkeiten** **Umsatzerlös** festlegen. Wenn diese Kontenarten verwendet werden, wird die Berichterstattung über Power BI die Vorzeichen umkehren und die Werte als "positiv" anzeigen.

## <a name="dashboard-and-reports-that-are-included-in-the-powerbicom-solution"></a>Dashboard und Berichte, die in der PowerBI.com-Lösung enthalten sind.
Das Dashboard enthält zusammengefasste Kacheln von Daten, die auf grundlegenden Berichten basieren. Jede Kachel enthält zusammengefasste Informationen für das aktuelle Jahr aller Unternehmen in einer Organisation. Beispiele für solche Kacheln:

- Bargeld
- Diesjähriger Gesamtumsatz
- Diesjährige Gesamtausgaben
- Diesjähriges Nettoeinkommen
- Liquiditätsgrad
- Diesjährige Gesamtausgaben nach Kontokategorie
- Derzeitiger Gewinnanteil
- Verbindlichkeiten für gesamtes Anlagevermögen
- Tatsächlicher und geplanter Umsatz im Vergleich
- Diesjähriger berechneter Gesamtumsatz
- Diesjähriges Bertriebskosten-Verhältnis
- Diesjährige Gewinnspanne
- Tatsächliche und Budgetausgaben im Vergleich – Alle Unternehmen

Jede dieser Kacheln wird durch einen unterstützenden Bericht gesichert. Diese Berichte enthalten Diagramme und Tabellen, die weitere Informationen bieten. Die Berichte werden in der folgenden Tabelle näher erläutert.

| Bericht                      | Der Bericht enthält die folgenden Informationen: |
|-----------------------------|--------------------------------------|
| Bargeld-Analyse               | Bargeld nach juristischer Person, Bargeld nach Quartal, Gesamtbargeld und Bargeld nach Konto<blockquote>[!NOTE] Die Bargeld-pro-Quartal-Informationen umfassen die Anfangssalden im Total für das erste Quartal nicht. Er zeigt die Summe von neuen Buchungen an, die für jedes Quartal gebucht werden.</blockquote> |
| Analyse des derzeitigen Gewinnanteils      | Gewinnanteil nach juristischer Person, Gewinnanteil nach Quartal und Salden für aktuelle Anlagen und Verbindlichkeiten |
| Analyse des Liquiditätsgrads        | Liquiditätsgrad nach juristischer Person, Liquiditätsgrad nach Quartal und Salden für Bargeld, Debitorenkonten und aktuelle Verbindlichkeiten |
| Analyse des Wareneinsatzes | Wareneinsatz (COGS) nach juristischer Person, COGS dieses Jahr und letztes Jahr nach Quartal, COGS verkaufsbezogenen nach juristischer Person, COGS Summe und COGS im Umsatzprozentsatz |
| Analyse des Betriebskapitals    | Betriebskapital nach juristischer Person, Betriebskapital nach Quartal, aktuellen Anlagen, Verbindlichkeiten und Gesamtbetriebskapital |
| Analyse von Anlagen und Verbindlichkeiten     | Rendite auf gesamtes Anlagevermögen und Verbindlichkeiten für gesamtes Anlagevermögen nach juristischer Person, Verbindlichkeiten für gesamtes Anlagevermögen und Rendite auf gesamtes Anlagevermögen nach Quartal bis heute, Anlagen und Verbindlichkeiten |
| Analyse der Gewinnspanne      | Tatsächliche und Budgetgewinnspanne nach juristischer Person, Gewinnmarkierung Quartal, Gewinnspanne in Prozent und Gewinnspanne |
| Analyse des Nettoeinkommen         | Tatsächliches und Budgetnettoeinkommen nach juristischer Person, Nettoeinkommen dieses und letztes Jahr und Ausgaben auf Nettoeinkommen in Prozent |
| Einnahme-Analyse           | Tatsächliche und Budgeteinnahmen vor Zinsen und Steuern (EBIT) nach juristischer Person, EBIT dieses und letztes Jahr, Ausgaben zum Umsatzerlös in Prozent und tatsächliche und Budgetausgaben zum Umsatzerlös |
| Analyse des Umsatzerlöses            | Gesamtumsatzerlös, tatsächlicher und Budgetgesamtumsatzerlös nach juristischer Person, Gesamtumsatzerlös dieses und letztes Jahr , Abweichung beim Umsatzerlösbudget nach juristischer Person und Gesamtumsatzerlös in dieser und in der letzten Periode. |
| Analyse der Ausgaben            | Die Gesamtausgaben, tatsächliche und Budgetgesamtausgaben nach juristischer Person, tatsächliche und Budgetgesamtausgaben nach Quartal, Gesamtausgaben nach Kontokategorie und Betriebskosten-Verhältnis |
| Analyse des berechneten Umsatzerlöses     | Gesamte Debitorenkonten, gesamte Debitorenkonten nach juristischer Person, gesamte Debitorenkonten nach Quartal und Salden für Debitorenkonten<blockquote>[!NOTE] Die Informationen enthalten keine Anfangssalden für die Debitorensachkonten. Es zeigt die Summe der neuen Buchungen, die für Debitoren gebucht werden.</blockquote> |

Die Diagramme und die Kacheln auf allen diesen Berichten können gefiltert und an das Dashboard geheftet werden. Weitere Informationen dazu, wie Sie in Power BI filtern und anheften, finden Sie unter [Erstellen und Konfigurieren eines Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen
Die folgenden Entitäten wurden als Basis für die **Financial Performance** PowerBI.com Lösung verwendet:

**Zusammenführen von Datenentitäten**

- **GeneralLedgerActivities** – Diese Einheit fasst Hauptbuchsalden nach Kontokategorie zusammen.
- **BudgetActivities** – Diese Einheit fasst Hauptbuchsalden nach Kontokategorie zusammen.

**Datenentitäten**

- FiscalCalendars
- MainAccounts
- LegalEntities
- Sachkonten
- ChartofAccounts

Diese Entitäten wurden verwendet, um berechnete Messungen im Datenmodell zu erstellen. Diese berechneten Messungen werden verwendet, um die Messdaten (KPIs) und Berichte zu erstellen, die im Inhalt verwendet werden. Standardmäßig enthält der Inhalt Daten für die letzten drei Jahre und ein zukünftiges Jahr. Um zusätzliche Berechnungen in Ihren Berichten und Dashboards einzubeziehen, können Sie die [Microsoft Excel-Arbeitsmappe](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi) ändern. Diese Arbeitsmappe ist das Standarddatenmodell, das verwendet wurde, um den Inhalt zu erstellen.
