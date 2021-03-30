---
title: Buchungsdefinitionsbeispiele
description: Dieser Artikel enthält Beispiele, die zeigen, wie Bestellbelastungen für Budgetzuteilungen und Buchungsdefinitionen verwendet werden.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8dbbc727120f5292a3ad94711cf79138b35593bf
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235136"
---
# <a name="posting-definition-examples"></a>Buchungsdefinitionsbeispiele

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Beispiele, die zeigen, wie Bestellbelastungen für Budgetzuteilungen und Buchungsdefinitionen verwendet werden.

Bevor Sie dieses Thema lesen, sollten Sie sich mit Buchungsdefinitionen und Transaktionsbuchungsdefinitionen vertraut gemacht haben. Informationen zu den Buchungsebenen finden Sie unter [Buchungsdefinitionen](posting-definitions.md). Die folgenden Beispiele können im Formular **Buchungsdefinitionen** eingerichtet werden. Jedes Beispiel umfasst folgende Abschnitte:

-   Buchungsdefinition – Übereinstimmungskriterien
-   Buchungsdefinition – Generierte Einträge
-   Buchungen mit Konten, Dimensionswerten und Beträgen
-   Aus der Buchungsdefinition generierte Sachkontoeinträge

Wenn die Konten und Dimensionswerte im Bereich **Übereinstimmungskriterien** für die Buchungsdefinition mit den Konten und Dimensionswerten der Buchung übereinstimmen, werden Sachkontoeinträge basierend auf dem Bereich **Generierte Einträge** für die Buchungsdefinition generiert. 
> [!NOTE]
> Verwenden Sie die Seite **Transaktions-Buchungsdefinitionen**, um eine Buchungsdefinition einer bestimmten Buchungsart zuzuordnen. Nachdem Sie einer Buchungsart eine Buchungsdefinition zugeordnet und auf der Seite **Hauptbuch-Parameter** **Buchungsdefinitionen verwenden** ausgewählt haben, müssen für alle Buchungen der ausgewählten Buchungsart Buchungsdefinitionen verwendet werden.

## <a name="example-purchase-order-encumbrances"></a>Beispiel: Bestellbelastungen
Wenn Sie die Belastungsverarbeitung aktivieren, indem Sie **Belastungsprozess aktivieren** auf der Seite **Hauptbuchparameter** auswählen, müssen Buchungsdefinitionen verwendet werden, um im Hauptbuch Belastungen für beliebige Konten zu erfassen, die reserviert werden sollen. In den meisten Fällen werden alle Spesenkonten in der Bilanz reserviert. 

Buchungsdefinitionen für Belastungen werden für das Modul **Einkauf** auf der Seite **Buchungsdefinitionen** eingerichtet. Im Bereich **Einkauf** der Seite **Transaktionsbuchungsdefinitionen** können Sie dann die Buchungsart **Bestellung** auswählen, um die Buchungsdefinition Bestellungen zuzuordnen. 

Alle Belegbuchungen für Bestellbelastungen müssen in jeder eindeutigen Dimension auf einem Beleg ausgeglichen sein (Soll muss gleich Haben sein).

### <a name="posting-definition--match-criteria"></a>Buchungsdefinition – Übereinstimmungskriterien

| Kontostruktur       | Kontonummer abgleichen | Priorität |
|-------------------------|----------------------|----------|
| Kontostruktur - GuV | \*                   | 1        |

<em>Ein leerer Wert im Feld **Kontonummer abgleichen</em>* bedeutet, dass alle übereinstimmenden Konten in der definierten Kontostruktur Teil der Abgleichsregel sind.

### <a name="posting-definition--generated-entries"></a>Buchungsdefinition – Generierte Einträge

| Kontostruktur | Generierte Kontonummer                    | Generierter Soll-/Habenbetrag |
|-------------------|---------------------------------------------|------------------------|
| Gesamtbetrag           | 300143 - -(Belastungskonto)             | Gleich                   |
| Gesamtbetrag           | 300144 - -(Reserve für Belastungskonto) | Ausbalancieren              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a>Buchungen mit Konten, Dimensionswerten und Beträgen

Die Konten und Dimensionswerte stammen entweder aus den Buchhaltungsverteilungen, die Sie für eine Bestellposition eingeben, oder aus den Konten und Dimensionen, die automatisch basierend auf den Standardeinstellungen für Kreditoren, Artikel, Kategorien und Dimensionsvorlagen generiert werden.

| Konto + Dimensionen           | Soll  | Entlastung | Kommentar |
|--------------------------------|--------|--------|---------|
| 606400-OU\_1-OU\_3566-Schulung | 250,00 |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a>Aus der Buchungsdefinition generierte Sachkontoeinträge

Generierte Sachkontoeinträge werden erstellt, um die Belastungen zu erfassen.

| Konto + Dimensionen           | Soll  | Entlastung | Kommentar |
|--------------------------------|--------|--------|---------|
| 300143-OU\_1-OU\_3566-Schulung | 250,00 |        |         |
| 300144-OU\_1-OU\_3566-Schulung |        | 250,00 |         |

In diesem Beispiel stimmt jedes Konto, das Teil der Kontostruktur - GuV ist, mit den Buchungsdefinitionskriterien überein. Wenn daher 606500-OU\_1-OU\_3566-Schulung ausgewertet wird, werden für Konten, die im Bereich **Generierte Einträge** für die Buchungsdefinition definiert sind, Einträge generiert.

## <a name="example-budget-appropriations"></a>Beispiel: Budgetzuteilungen
Wenn Sie die Budgetzuteilung aktivieren, indem Sie **Budgetzuteilung aktivieren** auf der Seite **Hauptbuchparameter** auswählen, müssen Buchungsdefinitionen verwendet werden, um Budgetregistereinträge im Hauptbuch zu erfassen. Wenn eine Budgetsteuerungskonfiguration aktiv und aktiviert ist, können Buchungsdefinitionen und Transaktionsbuchungsdefinitionen verwendet werden, um die Erfassung von Einträgen in Bezug auf Verteilung, Überarbeitung, Übertragung, Projekte, Anlagen und die Angebots- sowie Bedarfsplanung im Hauptbuch zu unterstützen. 

Eine Buchungsdefinition für Budgetregistereinträge mit dem Budgettyp **Ursprüngliches Budget**, für die Verteilungen aktiviert sind, kann mit dem Modul **Budget** auf der Seite **Buchungsdefinitionen** eingerichtet werden. Sie können dann im Bereich **Budget** auf der Seite **Transaktionsbuchungsdefinitionen** Budgetcodes verwenden, um die Buchungsdefinition den Budgetregistereinträgen mit dem Budgettyp **Ursprüngliches Budget** zuzuordnen. 

Wenn Budgetzuteilungen und Buchungsdefinitionen aktiviert sind, werden die Budgetregistereinträge für die Budgetsteuerung und im Hauptbuch erfasst.

### <a name="posting-definition--match-criteria"></a>Buchungsdefinition – Übereinstimmungskriterien

| Kontostruktur       | Kontonummer abgleichen | Priorität |
|-------------------------|----------------------|----------|
| Kontostruktur - GuV | \*                   | 1        |

<em>Ein leerer Wert im Feld **Kontonummer abgleichen</em>* bedeutet, dass alle übereinstimmenden Konten in der definierten Kontostruktur Teil der Abgleichsregel sind.

### <a name="posting-definition--generated-entries"></a>Buchungsdefinition – Generierte Einträge

| Kontostruktur | Generierte Kontonummer              | Generierter Soll-/Habenbetrag |
|-------------------|---------------------------------------|------------------------|
| Kontostruktur | 300145 - -(Konto für vorkalkulierten Umsatzerlös) | Gleich                   |
| Kontostruktur | 300146 - -(Zuteilungskonto)     | Ausbalancieren              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a>Buchungen mit Konten, Dimensionswerten und Beträgen

Sie geben Konten, Dimensionswerte und Beträge für den Budgetkontoeintrag auf der Seite **Budgetregistereintrag** ein.

| Konto + Dimensionen           | Soll | Entlastung | Kommentar |
|--------------------------------|-------|--------|---------|
| 606400-OU\_1-OU\_3566-Schulung |       | 250,00 |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a>Aus der Buchungsdefinition generierte Sachkontoeinträge

Generierte Sachkontoeinträge werden erstellt, um das ursprüngliche Budget in jeder Dimension zu erfassen.

| Konto + Dimensionen           | Soll  | Entlastung | Kommentar |
|--------------------------------|--------|--------|---------|
| 300145-OU\_1-OU\_3566-Schulung |        | 250,00 |         |
| 300146-OU\_1-OU\_3566-Schulung | 250,00 |        |         |

In diesem Beispiel stimmt jedes Konto, das Teil der Kontostruktur - GuV ist, mit den Buchungsdefinitionskriterien überein. Daher werden die generierten Sachkontoeinträge beim Auswerten von 606400-OU\_1-OU\_3566-Schulung erstellt.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]