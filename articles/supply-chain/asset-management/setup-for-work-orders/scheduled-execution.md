---
title: Geplante Ausführung
description: In diesem Abschnitt wird die planmäßige Ausführung im Asset Management erläutert.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fae899bcfa8bb2566d1a9aee3f0dbe22bc219edf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825637"
---
# <a name="scheduled-execution"></a>Geplante Ausführung

[!include [banner](../../includes/banner.md)]

 

Sie können die Service Levels für Arbeitsaufträge verwenden, um die geplante Ausführung einzurichten. (Weitere Informationen zu den Service Levels der Arbeitsaufträge finden Sie unter [Service Level und Beschreibung](service-level-and-description.md).) Die planmäßige Ausführung bietet Flexibilität bei der Arbeitsplanung für Instandhalter, da Sie für das Intervall, in dem ein Arbeitsauftrag abgeschlossen werden soll, detailliertere oder weniger detaillierte Anforderungen einrichten können. So kann beispielsweise ein Wartungsmitarbeiter, der einen Auftrag in einer Produktionsstätte schneller als erwartet erledigt, zu einem anderen nahegelegenen Auftrag wechseln, der für die aktuelle Woche geplant war, aber nicht unbedingt für den aktuellen Tag. Dieser Ansatz ermöglicht die Optimierung der Arbeitsvorbereitung und der Auftragsabwicklung.

Die Einrichtung der geplanten Ausführung, die sich auf Arbeitsaufträge bezieht, kann generisch oder spezifisch sein. Sie können generische Zeilen einrichten, die nicht auf bestimmte Arbeitsauftragsarten, Anlagentypen usw. beschränkt sind. Alternativ können Sie auch geplante Ausführungspositionen erstellen, die sich auf eine bestimmte Arbeitsauftragsart, Anlagenart, Wartungsauftragsart usw. beziehen.

1. Wählen Sie **Anlagenmanagement** \> **Einrichtung** \> **Arbeitsaufträge** \> **Planausführung**.
2. Wählen Sie **Neu**, um eine geplante Ausführungsposition zu erstellen.
3. Wählen Sie in den Feldern **Technischer Standort**, **Auftragsart**, **Assettyp**, **Hersteller**, **Modell**, **Wartungsauftragstyp Kategorie**, **Wartungsauftragstyp**, **Wartungsauftragstyp Variante** und **Wechseln** die gewünschten Werte aus.
4. Wählen Sie im Feld **Service Level** ein Service Level für Arbeitsaufträge aus. Wenn Sie dieses Feld leer lassen, machen Sie den generischsten Typ der geplanten Ausführungslinie. Ein Beispiel für eine generische Zeile finden Sie im ersten Satz in der folgenden Abbildung. Diese Position ermöglicht es, alle Arbeitsaufträge, die keinen Servicegrad für Arbeitsaufträge haben, für ein bestimmtes Datum und eine bestimmte Uhrzeit zu planen.
5. Wählen Sie im Feld **Geplante Ausführung** das Zeitintervall aus.
6. Wählen Sie **Speichern**.

![Geplante Ausführung](media/20-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]