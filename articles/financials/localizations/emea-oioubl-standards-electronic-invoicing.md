---
title: Unterstützte Standards für die elektronische Rechnungsstellung in Europa
description: Dieses Thema beschreibt die Abdeckung für eine elektronische Rechnungsstellung in Microsoft Dynamics 365 for Finance and Operations in der europäischen Region.
author: mrolecki
manager: AnnBe
ms.date: 07/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 10274
ms.search.region: Austria, Denmark, Italy, Norway, Spain, France, Belgium, Netherlands
ms.search.industry: ''
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 869deceb825ce6a823d5a39052e64e5b7ab61447
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/02/2019
ms.locfileid: "1852455"
---
# <a name="supported-standards-for-electronic-invoicing-in-europe"></a>Unterstützte Standards für die elektronische Rechnungsstellung in Europa

[!include [banner](../includes/banner.md)]

Dieses Thema beschreibt die Abdeckung für eine elektronische Rechnungsstellung für Europa. 

Die Implementierung und Übernahme der EU-weiten elektronischen Rechnungsstellung ist in der [Ratsrichtlinie 2010/45/EU](https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF) geregelt, die für alle EU-Mitgliedstaaten gilt. Unternehmen, die von der elektronischen Rechnungsstellung profitieren wollen, müssen Vertriebsrechnungen, Freitextrechnungen, Projektrechnungen, Vertriebsgutschriften und Projektrechnungsgutschriften als .xml-Dateien an die Regierung oder andere Handelspartner schicken, die die Verwendung der elektronischen Rechnungsstellung unterstützen. Diese .xml-Dateien müssen bestimmten Standards entsprechen. Die länderspezifischen Anforderungen und ihre Implementierung kann sich zwischen EU-Mitgliedstaaten unterscheiden, aber in der Regel verwenden Sie [UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl) (Universal Business Language) in unterschiedlichen Versionen mit Anpassungen, ebenso wie [PEPPOL](https://www.peppol.eu)-Spezifikationen und -Zugriffspunkte für die Überprüfung und den Transport. Der Hauptvorteil von UBL ist, dass Geschäftsunterlagen für unterschiedliche Zwecke standardisiert werden können. UBL ist ein flexibler, internationaler Standard, der viele Geschäftsanforderungen unterstützt, deshalb können diese Geschäftsunterlagen über Landesgrenzen hinweg ausgetauscht werden.

## <a name="what-electronic-invoice-formats-are-currently-available-in-finance-and-operations"></a>Welche elektronischen Rechnungsformate stehen derzeit in Finance and Operations zur Verfügung?

Die folgenden länderspezifischen Formate elektronischer Rechnungen stehen zur Verfügung:

-   OIOUBL v.2.02 für Dänemark
-   EHF v.2.0.8 für Norwegen
-   PEPPOL BIS v.2 für Österreich, Frankreich und Belgien
-   UBL-OHNL 1.9 für die Niederlande
-   FacturaE v.3.2.1 für Spanien
-   FatturaPA v.1.2 für Italien

Die elektronische Rechnungsstellung basiert auf der [elektronischen Berichtserstellung](../../dev-itpro/analytics/general-electronic-reporting.md). Es gibt ein **Kundenrechnungsmodell**-Datenmodell sowie mehrere länderspezifische elektronische Berichtsformatkonfigurationen für Österreich (AT), Dänemark (DK), Italien (IT), Norwegen (NO), Spanien (ES), Frankreich (FR), Belgien (BE) und die Niederlande (NL).

-   OIOUBL Vertriebsrechnung – für AT, DK und NO
-   OIOUBL Vertriebsgutschrift – für AT, DK und NO
-   OIOUBL Projektrechnung – für AT, DK und NO
-   OIOUBL Projektgutschrift – für AT, DK und NO
-   UBL Vertriebsrechnung FR
-   UBL Vertriebsgutschrift FR
-   UBL Projektrechnung FR
-   UBL Projektgutschrift FR
-   UBL Vertriebsrechnung BE
-   UBL Vertriebsgutschrift BE
-   UBL Projektrechnung BE
-   UBL Projektgutschrift BE
-   UBL Vertriebsrechnung NL
-   UBL Vertriebsgutschrift NL
-   UBL Projektrechnung NL
-   UBL Projektgutschrift NL 
-   Vertriebsrechnung (ES)
-   Vertriebsrechnung (IT)
-   Projektrechnung (ES)
-   Projektrechnung (IT)

Die von Ihnen erstellten elektronischen Rechnungen und Gutschriften enthalten die erforderlichen Informationen, wie beispielsweise die EAN-Nummer (European Article Numbering), den Ansprechpartner, die Kontonummer sowie Adressinformationen für den Kunden. Bei der Erstellung von Rechnungen werden Auswertungsregeln angewendet, Sie können also überprüfen, ob die richtigen Informationen eingetragen wurden. Welche Informationen gefordert werden, unterscheidet sich für die einzelnen Länder. Die Anforderungen und die unterstützten Länder und Formate verändern sich in unregelmäßigen Abständen, Sie sollten also immer die Bibliothek der freigegebenen Anlagen in Microsoft Dynamics Lifecycle Services (LCS) besuchen und die aktuellste Liste der verfügbaren Dateien mit dem Anlagentyp der **GER-Konfiguration** abfragen.

## <a name="additional-information"></a>Weitere Informationen
Weitere Informationen über die Einrichtung elektronischer Rechnungen finden Sie in den folgenden [Aufgabenleitfäden](../../fin-and-ops/get-started/help-overview.md#task-guides) im Feld Hilfe:

 - Einrichten der elektronischen OIOUBL-Rechnungsstellung
 - Konfigurationen der elektronischen Fakturierung des Imports OIOUBL
 - Einrichten von Debitorenkonten für die elektronische Fakturierung per OIOXML

> [!NOTE] 
> Diese Aufgabenleitfäden wurden für das für Dänemark spezifische Format elektronischer Rechnungen erstellt, *OIOUBL*, sie gelten jedoch mit geringen Abweichungen auch für andere unterstütze Länder.
