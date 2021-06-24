---
title: Vorhersagemodell verbessern (Vorschau)
description: In diesem Thema werden Funktionen beschrieben, mit denen Sie die Leistung von Vorhersagemodellen verbessern können.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 184a1cb5d3851e26b41340b711c51ef38e06eb53
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186641"
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

Beachten Sie bei der Auswahl von Feldern, die in das Modell aufgenommen werden sollen, dass die Liste alle verfügbaren Felder in der Microsoft Dataverse-Tabelle enthält, die den Daten im Azure-Data Lake zugeordnet ist. Einige dieser Felder sollten **nicht** ausgewählt werden. Die Felder, die nicht ausgewählt werden sollten, fallen in eine von drei Kategorien:

- Das Feld wird für die Dataverse-Tabelle benötigt, aber es gibt keine Sicherungsdaten dafür im Data Lake.
- Das Feld ist eine ID und daher für eine Machine-Learning-Funktion nicht sinnvoll.
- Das Feld stellt Informationen dar, die während der Vorhersage nicht verfügbar sind.

In den folgenden Abschnitten werden die Felder angezeigt, die für die Rechnungs- und Kundenentitäten verfügbar sind, und es werden die Felder aufgelistet, die werden **nicht** für das Training ausgewählt werden sollen. Die Kategorie, die für jedes dieser Felder angegeben ist, bezieht sich auf die Kategorien in der vorhergehenden Liste.
 
### <a name="invoice-dataverse-table"></a>Rechnungs-Dataverse-Tabelle

Die folgende Abbildung zeigt die Felder an, die für die Rechnungstabelle verfügbar sind.

[![Verfügbare Felder für die Rechnungstabelle](./media/available-fields.png)](./media/available-fields.png)

Die folgenden Felder sollten nicht für das Training ausgewählt werden:

- **Rechnungskonto** (Kategorie 2)
- **Ist geschlossen** (Kategorie 3) – In diesem Feld werden Rechnungen für Training (geschlossen) und Vorhersage (nicht geschlossen) gefiltert.
- **Name** (Kategorie 1)
- **Quell-ID** (Kategorie 2)
- **Quelldatensatz** (Kategorie 2)
- **Quelltabelle** (Kategorie 2)

### <a name="customer-dataverse-table"></a>Debitoren-Dataverse-Tabelle

Die folgende Abbildung zeigt die Felder an, die für die Debitorentabelle verfügbar sind.

[![Verfügbare Felder für die Debitorentabelle](./media/related-entities.png)](./media/related-entities.png)

Das folgende Feld sollte nicht für das Training ausgewählt werden:

- **Eindeutiger Zeilenschlüssel** (Kategorie 2)

## <a name="filters"></a>Filter

Die Filter unterstützen derzeit das Szenario des Debitorenzahlungsprädiktors nicht. Wählen Sie daher **Diesen Schritt überspringen** aus und fahren Sie mit der Übersichtsseite fort.

[![Fokusmodell mit Filtern](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
