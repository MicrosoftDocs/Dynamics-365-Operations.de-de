---
title: Financial Performance Power BI Inhalt
description: "In diesem Thema wird der Microsoft Power BI-Inhalt Finanzleistung beschrieben. Es werden das Dashboard und die Berichte beschrieben, die enthalten sind, zugegriffen wird und es werden Informationen zum Datenmodell und den Entitäten bereitgestellt, die zum Erstellen des Inhalts verwendet wurden."
author: kweekley
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: b20f526d20d357750777d0f9bda26e4d9d55b335
ms.contentlocale: de-de
ms.lasthandoff: 06/13/2017

---

# <a name="financial-performance-power-bi-content"></a>Financial Performance Power BI Inhalt

[!include[banner](../includes/banner.md)]

In diesem Thema wird der Microsoft Power BI-Inhalt **Finanzleistung** beschrieben. Es werden das Dashboard und die Berichte beschrieben, die enthalten sind, zugegriffen wird und es werden Informationen zum Datenmodell und den Entitäten bereitgestellt, die zum Erstellen des Inhalts verwendet wurden.

## <a name="accessing-the-power-bi-content"></a>Zugreifen au Power BI Inhalt

Sie können auf das **Finanzleistung** Power BI von Microsoft Dynamics Lifecycle Services (LCS) und von PowerBI.com aus zugreifen.

### <a name="available-from-lcs"></a>Verfügbar von LCS
Der Power BI-Inhalt **Finanzleistung**, der von LCS verfügbar ist, unterstützt die folgenden Versionen:

- Microsoft Dynamics 365 for Finance and Operations, Enterprise-Edition, Update vom Juli 2017
- Microsoft Dynamics 365 for Operations, Version 1611 

Sie können den Power BI-Inhalt in der freigegebenen Anlagenbibliothek in LCS finden. Weitere Informationen dazu, wie Sie das Inhaltspaket herunterladen und in Ihrer Organisation implementieren, finden Sie unter [Power BI-Inhalt in LCS von Microsoft und Ihren Partnern](power-bi-content-microsoft-partners.md). Um eine Vorführung anzusehen, die zeigt, wie der Power BI-Inhalt impementiert wird, zeigen Sie den Office Mix [Power BI-Inhalt von Microsoft und Ihren Partnern in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) an.

### <a name="available-from-powerbicom"></a>Verfügbar von PowerBI.com
Der Power BI-Inhalt **Finanzleistung**, der von PowerBI.com verfügbar ist, unterstützt Microsoft Dynamics AX Version 7.0 und Version 7.0.1. Weitere Informationen dazu, wie Sie Dynamics 365 AX-Daten verbinden und laden finden Sie unter [Zugriff auf Power Bi Inhalt von PowerBI.com](power-bi-home-page.md).

## <a name="main-account-setup"></a>Hauptkonto einrichten
Da Organisationen möchten, dass Verbindlichkeiten und Umsatzerlöse als positive Beträge auf Berichten angezeigt werden, sind die Einstellungen der Hauptkonten wichtig. Damit diese Hauptkonten als positive Beträge angezeigt werden, muss das Hauptkonto den Typ auf **Verbindlichkeiten** **Umsatzerlös** festlegen. Wenn diese Kontenarten verwendet werden, wird die Berichterstattung über Power BI die Vorzeichen umkehren und die Werte als "positiv" anzeigen.

## <a name="dashboard-and-reports-that-are-included-in-the-power-bi-content"></a>Dashboard und Berichte sind im Power BI-Inhalt enthalten
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
| Bargeld-Analyse               | Bargeld nach juristischer Person, Bargeld nach Quartal, Gesamtbargeld und Bargeld nach Konto<blockquote>[!NOTE]<br>Die Bargeld-pro-Quartal-Informationen umfassen die Anfangssalden im Total für das erste Quartal nicht. Er zeigt die Summe von neuen Buchungen an, die für jedes Quartal gebucht werden.</blockquote> |
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
| Analyse des berechneten Umsatzerlöses     | Gesamte Debitorenkonten, gesamte Debitorenkonten nach juristischer Person, gesamte Debitorenkonten nach Quartal und Salden für Debitorenkonten<blockquote>[!NOTE]<br>Die Informationen enthalten keine Anfangssalden für die Debitorensachkonten. Es zeigt die Summe der neuen Buchungen, die für Debitoren gebucht werden.</blockquote> |

Die Diagramme und die Kacheln auf allen diesen Berichten können gefiltert und an das Dashboard geheftet werden. Weitere Informationen dazu, wie Sie in Power BI filtern und anheften, finden Sie unter [Erstellen und Konfigurieren eines Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen
Die folgenden Entitäten wurden als Grundlage des Power BI-Inhaltspakets **Finanzleistung** verwendet:

**Zusammenführen von Datenentitäten**

- **GeneralLedgerActivities** – Diese Einheit fasst Hauptbuchsalden nach Kontokategorie zusammen.
- **BudgetActivities** – Diese Einheit fasst Hauptbuchsalden nach Kontokategorie zusammen.

**Datenentitäten**

- FiscalCalendars
- MainAccounts
- LegalEntities
- Sachkonten
- ChartofAccounts

Diese Entitäten wurden verwendet, um berechnete Messungen im Datenmodell zu erstellen. Diese berechneten Messungen werden verwendet, um die Messdaten (KPIs) und Berichte zu erstellen, die im Inhalt verwendet werden. Standardmäßig enthält der Inhalt Daten für die letzten drei Jahre und ein zukünftiges Jahr. Um zusätzliche Berechnungen in Ihre Berichten und Dashboards einzubeziehen, können Sie das [Microsoft Excel Arbeitsbuch](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi) ändern. Diese Arbeitsmappe ist das Standarddatenmodell, das verwendet wurde, um den Inhalt zu erstellen. Nachdem Sie die Änderungen vorgenommen haben, können Sie ein Organisations-Inhaltspaket und ein Dashboard erstellen, die die von Ihnen hinzugefügten Informationen enthalten.

