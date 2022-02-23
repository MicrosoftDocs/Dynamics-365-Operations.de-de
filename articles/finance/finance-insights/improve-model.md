---
title: Vorhersagemodell verbessern (Vorschau)
description: In diesem Thema werden Funktionen beschrieben, mit denen Sie die Leistung von Vorhersagemodellen verbessern können.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 23c9062dcc13951792306c955b54cae6f656fec5
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646078"
---
# <a name="improve-the-prediction-model-preview"></a>Vorhersagemodell verbessern (Vorschau)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In diesem Thema werden Funktionen beschrieben, mit denen Sie die Leistung von Vorhersagemodellen verbessern können. Sie beginnen Ihr Modell im **Zahlungsvorhersagen für Debitoren**-Arbeitsbereich in Microsoft Dynamics 365 Finance zu verbessern. Die Verbesserungsschritte werden dann in AI Builder abgeschlossen.

## <a name="select-historical-outcomes"></a>Historische Ergebnisse auswählen

Sie wählen zunächst eines oder mehrere der drei möglichen Ergebnisse für Rechnungen aus: **Pünktlich**, **Verspätet** und **Sehr spät**. Alle drei Ergebnisse sollten ausgewählt werden. Wenn Sie die Auswahl eines der Ergebnisse deaktivieren, werden Rechnungen aus dem Trainingsprozess herausgefiltert und die Genauigkeit der Vorhersage wird verringert.

[![Ergebnisse bestätigen](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)

Wenn Ihre Organisation nur zwei Ergebnisse benötigt, ändern Sie die **Verspätet**- und **Sehr spät**-Schwellenwerte auf 0 (Null) Tage. Auf diese Weise reduzieren Sie die Vorhersage effektiv auf einen binären Zustand von **Pünktlich** oder **Verspätet**.

## <a name="select-fields"></a>Felder auswählen

Beachten Sie bei der Auswahl von Feldern, die in das Modell aufgenommen werden sollen, dass die Liste alle verfügbaren Felder in der Common Data Service-Entität enthält, die den Daten im Azure-Data Lake zugeordnet ist. Einige dieser Felder sollten **nicht** ausgewählt werden. Die Felder, die nicht ausgewählt werden sollten, fallen in eine von drei Kategorien:

- Das Feld wird für die Common Data Service-Entität benötigt, aber es gibt keine Sicherungsdaten dafür im Data Lake.
- Das Feld ist eine ID und daher für eine Machine-Learning-Funktion nicht sinnvoll.
- Das Feld stellt Informationen dar, die während der Vorhersage nicht verfügbar sind.

In den folgenden Abschnitten werden die Felder angezeigt, die für die Rechnungs- und Kundenentitäten verfügbar sind, und es werden die Felder aufgelistet, die werden **nicht** für das Training ausgewählt werden sollen. Die Kategorie, die für jedes dieser Felder angegeben ist, bezieht sich auf die Kategorien in der vorhergehenden Liste.
 
### <a name="invoice-common-data-model-entity"></a>Common Data Model-Rechnungsentität

Die folgende Abbildung zeigt die Felder an, die für die Rechnungsentität verfügbar sind.

[![Verfügbare Felder für die Rechnungsentität](./media/available-fields.png)](./media/available-fields.png)

Die folgenden Felder sollten nicht für das Training ausgewählt werden:

- **Rechnungskonto** (Kategorie 2)
- **Ist geschlossen** (Kategorie 3) – In diesem Feld werden Rechnungen für Training (geschlossen) und Vorhersage (nicht geschlossen) gefiltert.
- **Name** (Kategorie 1)
- **Quell-ID** (Kategorie 2)
- **Quelldatensatz** (Kategorie 2)
- **Quelltabelle** (Kategorie 2)

### <a name="customer-common-data-model-entity"></a>Common Data Model-Debitorenentität

Die folgende Abbildung zeigt die Felder an, die für die Debitorenentität verfügbar sind.

[![Verfügbare Felder für die Debitorenentität](./media/related-entities.png)](./media/related-entities.png)

Das folgende Feld sollte nicht für das Training ausgewählt werden:

- **Eindeutiger Zeilenschlüssel** (Kategorie 2)

## <a name="filters"></a>Filter

Die Filter unterstützen derzeit das Szenario des Debitorenzahlungsprädiktors nicht. Wählen Sie daher **Diesen Schritt überspringen** aus und fahren Sie mit der Übersichtsseite fort.

[![Fokusmodell mit Filtern](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)

#### <a name="privacy-notice"></a>Datenschutzhinweis
Vorschauen (1) wenden möglicherweise weniger Datenschutz- und Sicherheitsmaßnahmen an als der Dynamics 365 Finance and Operations-Dienst, (2) sind nicht in der Service Level Agreement (SLA) für diesen Dienst enthalten, (3) sollten nicht zur Verarbeitung personenbezogener Daten oder anderer Daten verwendet werden, die gesetzlichen oder behördlichen Compliance-Anforderungen unterliegen, und (4) hat begrenzten Support.
