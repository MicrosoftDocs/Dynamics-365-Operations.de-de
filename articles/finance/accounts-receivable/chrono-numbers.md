---
title: Chronologisches Nummerieren von Dokumenten und Belegen
description: In diesem Thema wird erläutert, wie Sie chronologische Nummern für geeignete Dokumente und zugehörige Belege einrichten und verwenden.
author: ikond
manager: AnnBe
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceGroup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 401195
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-15
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 31745632de7339d167ac9f18f02e6611e1a78b28
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104387"
---
# <a name="numbering-documents-and-vouchers-chronologically"></a>Chronologisches Nummerieren von Dokumenten und Belegen

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

In einigen Ländern ist es gesetzlich vorgeschrieben, Dokumente und zugehörige Belege in chronologischer Reihenfolge zu nummerieren. Die Chronologie muss durch Perioden unterstützt werden. Alle Nummern, die zu früheren Perioden gehören, müssen kleiner sein als die Zahlen, die zu späteren Perioden gehören. Um diese Anforderung zu erfüllen, wurde eine chronologische Nummerierungsfunktion implementiert. In diesem Thema wird erläutert, wie Sie chronologische Nummern für geeignete Dokumente und zugehörige Belege konfigurieren und verwenden.

## <a name="prerequisites"></a>Voraussetzungen

Aktivieren Sie im Arbeitsbereich „Funktionsverwaltung“ die Funktion **Chronologische Nummerierung**: Weitere Informationen finden Sie unter [Funktionsverwaltung – Übersicht](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="configure-chronological-numbering"></a>Die chronologische Nummerierung konfigurieren

Die chronologische Nummerierung betrifft die folgenden Dokumente.

**Debitorenkonten**
- Debitorenrechnung
- Debitorenrechnungsbeleg
- Verkaufsgutschrift
- Verkaufsgutschriftbeleg
- Freitextrechnung
- Freitext-Rechnungsbeleg
- Freitext-Gutschrift
- Freitext-Gutschriftbeleg
- Lieferschein
- Lieferscheinbeleg
- Lieferschein-Korrekturbeleg
- Zinsrechnungsbeleg
- Mahnschreibenbeleg

**Kreditorenkonten**
- Rechnungsbeleg
- Gutschriftbeleg
- Produktzugangsbeleg

**Projektverwaltung**
- Rechnung
- Rechnungsbeleg
- Gutschrift
- Gutschriftbeleg 

### <a name="define-number-sequences"></a>Nummernkreise definieren

Rufen Sie zur Definition von Nummernkreisen **Organisationsverwaltung** > **Nummernkreise** > **Nummernkreise** auf. Sie können beliebig viele Nummernkreise definieren, um die betroffenen Perioden für die erforderlichen Dokumente abzudecken. 

Geben Sie für jeden Nummernkreis ein Unternehmen an. Die Segmente der Nummernkreise müssen so definiert werden, dass sie eine chronologische Reihenfolge für Perioden liefern. Beispielsweise können die Segmentnamen ein spezielles Präfix enthalten, das eine bestimmte Periode identifiziert.

![Nummernkreiseinrichtung](media/chrono-num-sequence.jpg)

### <a name="configure-number-sequence-groups"></a>Nummernkreisgruppen konfigurieren

Rufen Sie **Debitorenkonten** > **Einrichtung** > **Debitorenkontenparameter** auf, um Nummernkreisgruppen zu definieren. Definieren Sie auf der Registerkarte **Nummernkreise** so viele Nummernkreisgruppen, wie erforderlich sind, um die betroffenen Perioden abzudecken. 

Wählen Sie für jede Gruppe im Abschnitt **Referenz** eine der unterstützten Dokumentreferenzen aus, und beziehen Sie sich im Feld **Nummernkreiscode** auf einen Nummernkreis, der zuvor für die zugehörige Periode erstellt wurde.

![Nummernkreisgruppeneinrichtung](media/chrono-num-sequence-group.jpg)

Konfigurieren Sie in ähnlicher Weise Nummernkreisgruppen in **Kreditorenkonten**- und **Projektverwaltung und -buchhaltung**-Modulen.

### <a name="configure-number-sequence-groups-chronology"></a>Nummernkreisgruppen chronologisch konfigurieren

Rufen Sie **Organisationsverwaltung** > **Nummernkreise** > **Chronologische Nummernkreisgruppen** auf, um die Chronologie der Nummernkreisgruppen zu konfigurieren. Definieren Sie die Anwendbarkeitsbedingungen für Nummernkreisgruppen.

![Chronologische Nummerneinrichtung](media/chrono-num-sequence-group-period.jpg)

| Feld            | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| In Kraft  | Das Startdatum der Anwendbarkeit der Nummernkreisgruppe. |
| Ablaufdatum      | Das Enddatum der Anwendbarkeit der Nummernkreisgruppe. Wenn kein Enddatum eingesetzt wird, wählen Sie **Niemals** aus. |
| Nummernkreisgruppe | Nummernkreisgruppe, mit der während der Periode Dokumentnummern generiert werden. |
| Ursprüngliche Nummernkreisgruppe | Dieser Nummernkreisgruppencode wird zum zusätzlichen Filtern für Fälle verwendet, in denen Dokumenten bereits eine bestimmte *permanente* Nummernkreisgruppe zugewiesen ist. Ein leerer Wert wird als bestimmter Wert betrachtet. Wenn Sie eine vorläufig zugewiesene Gruppe ignorieren müssen, verwenden Sie für dieses Setup die Option **Standard**. |
| Standard | Wenn diese Option aktiviert ist, ignoriert das System die vorläufig zugewiesene Dokumentnummernkreisgruppe und verwendet nur die Start- und Enddaten der Perioden für die Anwendbarkeitsanalyse. Bei Deaktivierung verwendet das System die vollständige Kombination **Gültig** + **Ablaufdatum** + **Ursprüngliche Nummernkreisgruppe** als Auswahl. |

## <a name="document-posting"></a>Dokumentbuchung
Wenn Sie ein Dokument buchen, wird dem Dokument die entsprechende Nummernkreisgruppe basierend auf dem Buchungsdatum des Dokuments zugewiesen und anschließend zum Generieren einer Dokumentnummer basierend auf dem erkannten Nummernkreis verwendet. Das System gibt eine Meldung zur Zuweisung der Nummernkreisgruppen aus.

![Dokumentnummer](media/chrono-num-sequence-fti.jpg)

> [!NOTE]
> Für einige Länder gibt es bereits eine spezifische Logik für die Nummerierung von Dokumenten. In diesem Fall überschreibt die länderspezifische Logik die Funktion **Chronologische Nummerierung**.
