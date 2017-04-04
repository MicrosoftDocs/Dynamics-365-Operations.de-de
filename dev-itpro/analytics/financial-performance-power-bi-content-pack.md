---
title: Finanzleistungs-Energie BIinhalt
description: "In diesem Thema wird das Microsoft Dynamics 365 für zufriedenes Pack der Arbeitsgangs- leistung für Microsoft-Energie BI. Es wird das Dashboard und Berichte, die im Paket enthalten inhaltliche sind, und enthält Informationen zum Datenmodell und die Entitäten, die verwendet wurde, um das Inhaltstext Pack zu erstellen."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 227285720e7f28beeb135eea081940578531d458
ms.lasthandoff: 03/31/2017


---

# <a name="financial-performance-power-bi-content"></a>Finanzleistungs-Energie BIinhalt

In diesem Thema wird das Microsoft Dynamics 365 für zufriedenes Pack der Arbeitsgangs- leistung für Microsoft-Energie BI. Es wird das Dashboard und Berichte, die im Paket enthalten inhaltliche sind, und enthält Informationen zum Datenmodell und die Entitäten, die verwendet wurde, um das Inhaltstext Pack zu erstellen.

<a name="accessing-the-content-pack"></a>Zugreifen des das Content Packs
--------------------------

Zwei Versionen des das Content Packs der finanziellen sind verfügbar. Eine Version ist von den Microsoft Dynamics Lifecycle Services (LCS) verfügbar, während die andere von verfügbar ist PowerBI.com.

-   ** Version, die von Kreditbriefen verfügbar ist: ** Der Inhaltstext Pack der finanziellen, das der Kreditbriefe verfügbar ist, unterstützt Microsoft Dynamics 365 für Arbeitsgangsversion 1611. Sie können das Inhaltstext Pack in der Bibliothek der freigegebenen Anlage in Kreditbriefen suchen. Weitere Informationen dazu, wie das herunterlädt Inhaltstext Pack und es für Ihr Microsoft Dynamics 365 für Arbeitsgänge, Daten finden Sie in BIinhalt herstellt [Energie Kreditbriefen von Microsoft und von den Partnern]( power-bi-content-microsoft-partners.md).
-   ** Version, die von PowerBI.com verfügbar ist: ** Der Inhaltstext Pack der finanziellen von PowerBI.com, das verfügbar ist, AX-Versionen unterstützt Microsoft Dynamics 7,0 und 7.0.1. Weitere Informationen dazu, wie das Dynamics 365 für Arbeitsgänge Daten, finden Sie Zugriffs-Energie Verbindung hergestellt und lädt [BIinhalt von PowerBI.com ]( power-bi-home-page.md).

## <a name="main-account-setup"></a>Hauptkontoeinstellung
Da Organisationen Verbindlichkeiten und Umsatzerlöse als positive Beträge auf Berichten angezeigt werden sollen, sind die Einstellungen der Hauptkonten in Dynamics 365 für Arbeitsgänge wichtig. Damit diese Hauptkonten als positive Beträge, das Hauptkonto den Typ muss auf festgelegt werden werden ** Verbindlichkeiten ** oder ** Umsatzerlös **. Wenn die Kontenart verwendet werden, Microsoft-Energie Melden von BI storniert die Vorzeichen umkehren und zeigt die Beträge als - an.

## <a name="dashboard-and-reports-that-are-included-in-the-content-pack"></a>Dashboard und Berichte, die im Paket enthalten inhaltliche sind
Nachdem Sie das Inhaltspaket mit Ihren Dynamics 365 for Operations Daten verbunden haben, zeigen das Dashboard und die Berichte Ihre Finanzdaten an. Wenn von Nie Leistungsfähigkeit BI zuvor verwendet haben, können Sie dieser auf mehr zu erfahren [geführt, Seite für Leistung BI] (https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData) erfahrend. Das Dashboard enthält zusammengefasste Kacheln von Daten, die auf grundlegenden Berichten basieren. Jede Kachel enthält zusammengefasste Informationen für das aktuelle Jahr aller Unternehmen in einer Organisation. Nachfolgend sind einige der Kacheln:

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

Jede Kachel wird durch Schwierigkeiten unterstützenden Bericht unterstützt. Diese Berichte enthalten Diagramme und Tabellen, die weitere Informationen bieten. Die Berichte werden in der folgenden Tabelle näher erläutert.

| Bericht                      | Der Bericht enthält die folgenden Informationen:                                                                                                                                                                                                                                                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bargeld-Analyse               | Bargeld- nach juristischer Person, Bargeld Quartal, Bargeld und Summe für Bargeld- nach Konto ** Hinweis: ** Der ** Bargeld Quartal ** Bericht umfasst Anfangssalden nicht ganz für das erste Quartal. Er zeigt die Summe von neuen Buchungen an, die für jedes Quartal gebucht werden.                                                                                |
| Analyse des derzeitigen Gewinnanteils      | Gewinnanteil nach juristischer Person, Gewinnanteil nach Quartal und Salden für aktuelle Anlagen und Verbindlichkeiten                                                                                                                                                                                                                              |
| Analyse des Liquiditätsgrads        | Liquidität ersten Grades nach juristischer Person, Liquidität ersten Grades Quartal und Salden für Bargeld, Debitor und aktuelle Verbindlichkeiten                                                                                                                                                                                                                      |
| Analyse des Wareneinsatzes | Wareneinsatz (COGS) nach juristischer Person, COGS dieses Jahr und letztes Jahr nach Quartal, COGS verkaufsbezogenen nach juristischer Person, COGS Summe und COGS im Umsatzprozentsatz                                                                                                                                                                                   |
| Analyse des Betriebskapitals    | Betriebskapital nach juristischer Person, Betriebskapital nach Quartal, aktuellen Anlagen, Verbindlichkeiten und Gesamtbetriebskapital                                                                                                                                                                                                                   |
| Analyse von Anlagen und Verbindlichkeiten     | Rendite auf gesamtes Anlagevermögen und Verbindlichkeiten für gesamtes Anlagevermögen nach juristischer Person, Verbindlichkeiten für gesamtes Anlagevermögen und Rendite auf gesamtes Anlagevermögen nach Quartal bis heute, Anlagen und Verbindlichkeiten                                                                                                                                                                                     |
| Analyse der Gewinnspanne      | Tatsächliche und Budgetgewinnspanne nach juristischer Person, Gewinnmarkierung Quartal, Gewinnspanne in Prozent und Gewinnspanne                                                                                                                                                                                                                       |
| Analyse des Nettoeinkommen         | Tatsächliches und Budgetnettoeinkommen nach juristischer Person, Nettoeinkommen dieses und letztes Jahr und Ausgaben auf Nettoeinkommen in Prozent                                                                                                                                                                                                                       |
| Einnahme-Analyse           | Tatsächliche und Budgeteinnahmen vor Zinsen und Steuern (EBIT) nach juristischer Person, EBIT dieses und letztes Jahr, Ausgaben zum Umsatzerlös in Prozent und tatsächliche und Budgetausgaben zum Umsatzerlös                                                                                                                                                          |
| Analyse des Umsatzerlöses            | Gesamtumsatzerlös, tatsächlicher und Budgetgesamtumsatzerlös nach juristischer Person, Gesamtumsatzerlös dieses und letztes Jahr , Abweichung beim Umsatzerlösbudget nach juristischer Person und Gesamtumsatzerlös in dieser und in der letzten Periode.                                                                                                                                                 |
| Analyse der Ausgaben            | Die Gesamtausgaben, tatsächliche und Budgetgesamtausgaben nach juristischer Person, tatsächliche und Budgetgesamtausgaben nach Quartal, Gesamtausgaben nach Kontokategorie und Betriebskosten-Verhältnis                                                                                                                                                                 |
| Analyse des berechneten Umsatzerlöses     | Summenkonto, Summenkonten Ausstehender nach juristischer Person, Summenkonten Ausstehender Quartal und Salden für Debitorkonten ** Hinweis: ** Die Berichte enthalten Folgendes nicht Anfangssalden für die Debitorsachkonten. Sie zeigen die Summe von neuen Buchungen an, die für den Debitor gebucht werden. |

Die Diagramme und die Kacheln auf allen diesen Berichten können gefiltert und an das Dashboard geheftet werden. Weitere Informationen dazu, wie Sie in Power BI filtern und anheften, finden Sie unter [Erstellen und Konfigurieren eines Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Das Datenmodells und die Entitäten verstehen
Die Daten, die das Dashboard und Berichten im das Content Pack der finanziellen aufgefüllt werden, Dynamics 365 für Arbeitsgangsdaten. Die folgenden Entitäten wurden als Grundlage des das Content Packs verwendet: ** Die Datenentitäten **

-   ** GeneralLedgerActivities ** – diese Einheit zusammenfasst Hauptbuchsalden nach Kontokategorie.
-   ** BudgetActivities ** – diese Einheit zusammenfasst Budgetsalden nach Kontokategorie.

**Data entities**

-   FiscalCalendars
-   MainAccounts
-   LegalEntities
-   Sachkonten
-   ChartofAccounts

Diese wurden Entitäten verwendet, um berechnete Kennzahlen im - Datenmodell zu erstellen. Die berechnete Kennzahlen, werden die Leistungskennzahlen (KPIs) und Berichten zu verwendet, die in das Content Pack verwendet werden. Standardmäßig enthält das Inhaltspaket Daten für die letzten drei Jahre und ein zukünftiges Jahr. Um zusätzliche Berechnungen in Ihre Berichten und Dashboards einzubeziehen, können Sie das [Microsoft Excel Arbeitsbuch](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi) ändern. Diese Arbeitsmappe ist das Standarddatenmodell, das verwendet wurde, um das Inhaltspaket zu erstellen. Nachdem Sie die Änderungen vorgenommen haben, können Sie ein Organisations-Inhaltspaket und ein Dashboard erstellen, die die von Ihnen hinzugefügten Informationen enthalten.

## <a name="additional-resources"></a>Zusätzliche Ressourcen
Nachfolgend finden Sie einige hilfreiche Links zum Thema Entitäten und Erstellen von Power BI-Inhalten:

-   [Datenentitäten](..\data-entities\data-entities.md)
-   [Erstellen von Organisations-Inhaltspaketen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datenmodellierung mithilfe von Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Hinzufügen von Power BI-Kacheln zu Arbeitsbereichen](configure-power-bi-integration.md)



