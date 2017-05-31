---
title: Financial Performance Power BI Inhalt
description: "Dieser Artikel beschreibt das Microsoft Dynamics 365 for Operations Financial Performance-Inhaltspaket für Microsoft Power BI. Es wird zudem beschrieben, wie das Dashboard und die Berichte, die im Inhaltspaket enthalten sind, verwendet werden und enthält Informationen zum Datenmodell und den Entitäten, die verwendet werden, um das Inhaltspaket zu erstellen."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 9cd1d7e5b7b1fd892034dcca0a0c141363104a45
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="financial-performance-power-bi-content"></a>Financial Performance Power BI Inhalt

[!include[banner](../includes/banner.md)]


Dieser Artikel beschreibt das Microsoft Dynamics 365 for Operations Financial Performance-Inhaltspaket für Microsoft Power BI. Es wird zudem beschrieben, wie das Dashboard und die Berichte, die im Inhaltspaket enthalten sind, verwendet werden und enthält Informationen zum Datenmodell und den Entitäten, die verwendet werden, um das Inhaltspaket zu erstellen.

<a name="accessing-the-content-pack"></a>Zugreifen auf das Inhaltspaket
--------------------------

Zwei Versionen des Financial Performance Inhaltspaket sind verfügbar. Eine Version ist vom Microsoft Dynamics Lifecycle Services (LCS) verfügbar, während die andere von  PowerBI.com verfügbar ist.

-   **Version, die von LCS verfügbar ist**: Das Financial Performance Inhaltspaket, das von LCS verfügbar ist, unterstützt Microsoft Dynamics 365 for Operations, Version 1611. Sie können das Inhaltspaket in der Bibliothek der freigegebenen Anlage in LCS suchen. Weitere Informationen dazu, wie Sie Inhalte herunterladen und mit Ihrem Microsoft Dynamics 365 for Operations verbinden, finden Sie unter [Power Bi Inhalt in LCS von Microsoft und Ihren Partnern](power-bi-content-microsoft-partners.md).
-   **Version, die von PowerBI.com verfügbar ist**: Das Financial Performance Inhaltspaket, das von PowerBI.com verfügbar ist, unterstützt Microsoft Dynamics AX Version 7.0 und Version 7.0.1. Weitere Informationen dazu, wie Sie Dynamics 365 for Operations Daten verbinden und laden finden Sie unter [Zugriff auf Power Bi Inhalt von PowerBI.com](power-bi-home-page.md).

## <a name="main-account-setup"></a>Hauptkonto einrichten
Da Organisationen möchten, dass Verbindlichkeiten und Umsatzerlöse als positive Beträge auf Berichten angezeigt werden, sind die Einstellungen der Hauptkonten in Dynamics 365 for Operations wichtig. Damit diese Hauptkonten als positive Beträge angezeigt werden, muss das Hauptkonto den Typ auf **Verbindlichkeiten** **Umsatzerlös** festlegen. Wenn diese Kontenarten verwendet werden, wird die Berichterstattung über Microsoft Power BI die Vorzeichen umkehren und die Werte als "positiv" anzeigen.

## <a name="dashboard-and-reports-that-are-included-in-the-content-pack"></a>Dashboard und Berichte sind im Paket enthalten
Nachdem Sie das Inhaltspaket mit Ihren Dynamics 365 for Operations Daten verbunden haben, zeigen das Dashboard und die Berichte Ihre Finanzdaten an. Wenn Sie bisher noch nie Microsoft Power BI verwendet haben, finden Sie weitere Informationen unter [Erste Schritte in Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Das Dashboard enthält zusammengefasste Kacheln von Daten, die auf grundlegenden Berichten basieren. Jede Kachel enthält zusammengefasste Informationen für das aktuelle Jahr aller Unternehmen in einer Organisation. Beispiele für solche Kacheln:

-   Bargeld
-   Diesjähriger Gesamtumsatz
-   Diesjährige Gesamtausgaben
-   Diesjähriges Nettoeinkommen
-   Liquiditätsgrad
-   Diesjährige Gesamtausgaben nach Kontokategorie
-   Derzeitiger Gewinnanteil
-   Verbindlichkeiten für gesamtes Anlagevermögen
-   Tatsächlicher und geplanter Umsatz im Vergleich
-   Diesjähriger berechneter Gesamtumsatz
-   Diesjähriges Bertriebskosten-Verhältnis
-   Diesjährige Gewinnspanne
-   Tatsächliche und Budgetausgaben im Vergleich – Alle Unternehmen

Jede dieser Kacheln wird durch einen unterstützenden Bericht gesichert. Diese Berichte enthalten Diagramme und Tabellen, die weitere Informationen bieten. Die Berichte werden in der folgenden Tabelle näher erläutert.

| Bericht                      | Der Bericht enthält die folgenden Informationen:                                                                                                                                                                                                                                                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bargeld-Analyse               | Bargeld nach juristischer Person, Bargeld nach Quartal, Total Bargeld und Bargeld nach Konto **Hinweis:** Der **Bargeld nach Quartal** ** Bericht umfasst die Anfangssalden im Total für das erste Quartal nicht. Er zeigt die Summe von neuen Buchungen an, die für jedes Quartal gebucht werden.                                                                                |
| Analyse des derzeitigen Gewinnanteils      | Gewinnanteil nach juristischer Person, Gewinnanteil nach Quartal und Salden für aktuelle Anlagen und Verbindlichkeiten                                                                                                                                                                                                                              |
| Analyse des Liquiditätsgrads        | Liquiditätsgrad nach juristischer Person, Liquiditätsgrad nach Quartal und Salden für Bargeld, Debitorenkonten und aktuelle Verbindlichkeiten                                                                                                                                                                                                                      |
| Analyse des Wareneinsatzes | Wareneinsatz (COGS) nach juristischer Person, COGS dieses Jahr und letztes Jahr nach Quartal, COGS verkaufsbezogenen nach juristischer Person, COGS Summe und COGS im Umsatzprozentsatz                                                                                                                                                                                   |
| Analyse des Betriebskapitals    | Betriebskapital nach juristischer Person, Betriebskapital nach Quartal, aktuellen Anlagen, Verbindlichkeiten und Gesamtbetriebskapital                                                                                                                                                                                                                   |
| Analyse von Anlagen und Verbindlichkeiten     | Rendite auf gesamtes Anlagevermögen und Verbindlichkeiten für gesamtes Anlagevermögen nach juristischer Person, Verbindlichkeiten für gesamtes Anlagevermögen und Rendite auf gesamtes Anlagevermögen nach Quartal bis heute, Anlagen und Verbindlichkeiten                                                                                                                                                                                     |
| Analyse der Gewinnspanne      | Tatsächliche und Budgetgewinnspanne nach juristischer Person, Gewinnmarkierung Quartal, Gewinnspanne in Prozent und Gewinnspanne                                                                                                                                                                                                                       |
| Analyse des Nettoeinkommen         | Tatsächliches und Budgetnettoeinkommen nach juristischer Person, Nettoeinkommen dieses und letztes Jahr und Ausgaben auf Nettoeinkommen in Prozent                                                                                                                                                                                                                       |
| Einnahme-Analyse           | Tatsächliche und Budgeteinnahmen vor Zinsen und Steuern (EBIT) nach juristischer Person, EBIT dieses und letztes Jahr, Ausgaben zum Umsatzerlös in Prozent und tatsächliche und Budgetausgaben zum Umsatzerlös                                                                                                                                                          |
| Analyse des Umsatzerlöses            | Gesamtumsatzerlös, tatsächlicher und Budgetgesamtumsatzerlös nach juristischer Person, Gesamtumsatzerlös dieses und letztes Jahr , Abweichung beim Umsatzerlösbudget nach juristischer Person und Gesamtumsatzerlös in dieser und in der letzten Periode.                                                                                                                                                 |
| Analyse der Ausgaben            | Die Gesamtausgaben, tatsächliche und Budgetgesamtausgaben nach juristischer Person, tatsächliche und Budgetgesamtausgaben nach Quartal, Gesamtausgaben nach Kontokategorie und Betriebskosten-Verhältnis                                                                                                                                                                 |
| Analyse des berechneten Umsatzerlöses     | Total Debitoren, Total Debitoren nach juristischer Person, Total Debitoren nach Quartal und Salden für Debitorkonten **Hinweis:** Die Berichte enthalten keine Anfangssalden für die Debitorsachkonten. Sie zeigen die Summe von neuen Buchungen an, die für den Debitor gebucht werden. |

Die Diagramme und die Kacheln auf allen diesen Berichten können gefiltert und an das Dashboard geheftet werden. Weitere Informationen dazu, wie Sie in Power BI filtern und anheften, finden Sie unter [Erstellen und Konfigurieren eines Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen
Die Daten, die verwendet werden, um Dashboard und Berichte im Financial Performance-Inhaltspaket aufzufüllen, sind Dynamics 365 for Operations Daten. Die folgenden Entitäten wurden als Grundlage des Inhaltspakets verwendet: **Aggregierte Datenentitäten**

-   **GeneralLedgerActivities** – Diese Einheit fasst Hauptbuchsalden nach Kontokategorie zusammen.
-   **BudgetActivities** – Diese Einheit fasst Hauptbuchsalden nach Kontokategorie zusammen.

**Datenentitäten**

-   FiscalCalendars
-   MainAccounts
-   LegalEntities
-   Sachkonten
-   ChartofAccounts

Diese Entitäten wurden verwendet, um berechnete Messungen im Datenmodell zu erstellen. Diese berechneten Messungen werden verwendet, um die Messdaten (KPIs) und Berichte zu erstellen, die im Inhaltspaket verwendet werden. Standardmäßig enthält das Inhaltspaket Daten für die letzten drei Jahre und ein zukünftiges Jahr. Um zusätzliche Berechnungen in Ihre Berichten und Dashboards einzubeziehen, können Sie das [Microsoft Excel Arbeitsbuch](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi) ändern. Diese Arbeitsmappe ist das Standarddatenmodell, das verwendet wurde, um das Inhaltspaket zu erstellen. Nachdem Sie die Änderungen vorgenommen haben, können Sie ein Organisations-Inhaltspaket und ein Dashboard erstellen, die die von Ihnen hinzugefügten Informationen enthalten.

## <a name="additional-resources"></a>Zusätzliche Ressourcen
Nachfolgend finden Sie einige hilfreiche Links zum Thema Entitäten und Erstellen von Power BI-Inhalten:

-   [Datenentitäten](..\data-entities\data-entities.md)
-   [Erstellen von Organisations-Inhaltspaketen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datenmodellierung mithilfe von Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Hinzufügen von Power BI-Kacheln zu Arbeitsbereichen](configure-power-bi-integration.md)





