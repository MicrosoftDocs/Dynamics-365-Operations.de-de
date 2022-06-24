---
title: Geplante Ausführung
description: In diesem Artikel wird die planmäßige Ausführung im Anlagenverwaltung erläutert.
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
ms.openlocfilehash: 5e9d6af5c224f683481378da57708fda3c1b7207
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848048"
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
6. Wählen Sie **Speichern** aus.

![Geplante Ausführung.](media/20-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]