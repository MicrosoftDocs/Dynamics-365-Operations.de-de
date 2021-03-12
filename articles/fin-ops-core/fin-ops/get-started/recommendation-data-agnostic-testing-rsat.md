---
title: Agnostische Datentests mit dem Regression Suite Automation Tool
description: In diesem Thema werden die Empfehlungen für agnostische Datentests mit Regression Suite Automation Tool beschrieben.
author: kfend
manager: AnnBe
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2019-09-11
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 2398bcbf0d148932e62ebe90aa8016acf0c79c28
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798200"
---
# <a name="data-agnostic-testing-using-the-regression-suite-automation-tool"></a>Agnostische Datentests mit dem Regression Suite Automation Tool

[!include [banner](../includes/banner.md)]

Während die funktionale Prüfung einer ERP-Anwendung nicht vollständig datenagnostisch sein kann, gibt es mehrere Phasen und Ansätze für Testzwecke. Diese Testphasen enthalten:  

- SysTest-Framework
- ATL-Framework
- Regression Suite Automation Tool (RSAT)

[![Testklassifizierungspyramide](./media/rsat-data-agnostic-testing-01.PNG)](./media/rsat-data-agnostic-testing-01.PNG)

## <a name="overview"></a>Übersicht
-   **SysTest-Framework** – Das SysTest-Framework dient zum zuverlässigen Schreiben von Einheitentests. Da Einheitentests allgemein eine Methode oder eine Funktion testen, sollten sie immer datenagnostisch und nur von den Daten abhängig sein, die im Rahmen des Tests bereitgestellt werden.
-   **ATL-Framework** – Microsoft hat ein ATL-Framework, eine Abstraktion im Feld SysTest-Framework, die eine Funktionsprüfung und Testschreibvorgänge einfacher und zuverlässiger macht. Dieses Framework sollte zum Schreiben von Komponententests oder von einfachen Integrationstests verwendet werden.
-   **RSAT** – Das RSAT wird für Integrationstest- und Geschäftszyklustests verwendet. Die Geschäftszyklustests, auch als Regressionsprüfungstests bekannt, sind von vorhandenen Daten abhängig. Allerdings können diese Tests datenagnostisch werden, wenn zusätzliche Faktoren berücksichtigt werden. 

    - o Wenn Einheitentests und Teiltests auf niedriger Ebene ausgeführt werden und vollständig datenagnostisch sein können (nicht abhängig von vorhandenen Dataset), sind die Geschäftszyklus- oder Regressionsprüfungstests von vorhandenen Daten abhängig. Zu diesen Daten zählen Einstellungen, Konfigurationseinstellungen (Parameter) und Masterdaten (Debitoren, Kreditoren, Artikel usw.), jedoch niemals Buchungsdaten. Stellen Sie sicher, dass wenn während des Tests irgendetwas geändert wird, dies zum letzten Test zurückgesetzt wird.
    - Wählen Sie Masterdaten anhand bestimmter Kriterien aus anstatt einen bestimmten Datensatz. Wenn Sie beispielsweise einen Artikel basierend auf den Stücklisten-Dimensionswerten und der Verfügbarkeit des Lagers auswählen möchten, filtern Sie die Produkte mit diesen Werten, wählen Sie den ersten Artikel aus, und kopieren Sie die bei künftigen Tests zu verwendende Zahl. Wenn es eine einfache Masterdatenposition ist, wie beispielsweise Debitor, Kreditor oder Artikel, kann diese als Teil der Automatisierung erstellt und in künftigen Tests durch Verkettung verwendet werden. 
    - o Geben Sie die eindeutigen Bezeichner, wie die Rechnungsnummern durch einen Nummernkreis ein oder indem Microsoft Excel-Funktionen verwenden, wie =TEXT(NOW(),"yyyymmddhhmm"). Diese Funktion stellt jede Minute eine eindeutige Zahl bereit, die es Ihnen ermöglicht, die Aktivität zu verfolgen. Dies kann für Variablen wie Produktzugangsnummern und Kreditorenrechnungsnummern verwendet werden. Diese Tests funktionieren immer wieder mit derselben Datenbank, ohne dass eine Wiederherstellung nötig ist.
    - Legen Sie den **Bearbeitungsmodus** der Umgebung immer auf **Lesen** oder **Bearbeiten** als ersten Testfall fest, da die Standardoption **Automatisch** ist. Die Optionen **Automatisch** verwenden immer die vorherige Einstellung und können zu unzuverlässigen Tests führen. 
 
    [![Seite „Optionen“, Registerkarte „Leistung“](./media/rsat-data-agnostic-testing-02.PNG)](./media/rsat-data-agnostic-testing-02.PNG)
 
    - Überprüfen Sie nur, wenn Sie eine bestimmte Buchung anstelle der generischen Prüfung filtern. Filtern Sie z. B. für die Anzahl von Datensätzen die Buchungsnummer oder das Buchungsdatum, damit die Überprüfung alle weiteren Buchungen ausschließt. 
    - Wenn Sie ein Debitorensaldo oder eine Budgetprüfung prüfen, speichern Sie den Wert zuerst und fügen Sie dann Ihren Buchungswert hinzu, um das erwartete Ergebnis anstelle eines erwarteten festen Werts zu prüfen. 
 
