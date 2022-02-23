---
title: Erstellen von Arbeitsaufträgen
description: In diesem Thema wird erläutert, wie Sie Arbeitsaufträge in der Anlagenverwaltung erstellen.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f94f8bc20753e38ce1cb6eccdfbc85c2e491ffad
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428743"
---
# <a name="creating-work-orders"></a>Erstellen von Arbeitsaufträgen

[!include [banner](../../includes/banner.md)]

 

Wenn Sie vorbeugende Wartungsaufträge geplant haben, ist der nächste Schritt, Arbeitsaufträge für die Einzelvorgänge zu erstellen. Dies erfolgt in einem der Wartungszeitpläne. Die geplanten Einzelvorgänge in einem Wartungszeitplan können verschiedene Referenztypen haben:

| Referenztyp | Beschreibung                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| Wartungspläne     | Vorbeugende Wartungsaufträge auf Grundlage der Wartungsplantypen „Zeit“ oder „Zähler“.                       |
| Wartungsdurchgänge    | Vorbeugende Wartungsaufträge, die mehrere Anlagen enthalten, die einen ähnlichen Wartungstyp erfordern.           |
| Wartungsanfrage   | Manuell erstellte Anforderung für die Wartung oder Reparatur einer Anlage, die in einen Arbeitsauftrag konvertiert werden kann. |


1. Klicken Sie auf **Anlagenverwaltung** > **Allgemein** > **Alle Wartungspläne** oder **Wartungszeitplanpositionen öffnen** oder **Wartungszeitplanpools öffnen**.

2. Wählen Sie die geplanten Wartungsaufträge aus, für die Sie einen Arbeitsauftrag erstellen möchten, und klicken Sie auf **Arbeitsauftrag**. Im Dialog **Arbeitsaufträge erstellen** wird die Gesamtanzahl von Planungsstunden für die ausgewählten Positionen im Feld **Wartungsprognosestunden** angezeigt.

3. Im Abschnitt **Parameter** wählen Sie aus, wie viele Arbeitsaufträge erstellt werden sollen. Sie können einen Arbeitsauftrag pro Wartungszeitplanposition oder mehrere Arbeitsaufträge basierend auf Ihrer Auswahl im Abschnitt **Ein Arbeitsauftrag pro** erstellen.

4. Wählen Sie einen **Arbeitsauftragstyp** aus, der für alle Arbeitsaufträge verwendet wird, die Sie erstellen. In der folgenden Abbildung wird ein Beispiel des Dialogfelds **Arbeitsaufträge erstellen** angezeigt.

![Abbildung 1](media/18-preventive-maintenance.png)

5. Klicken Sie auf **OK**. Einer oder mehrere Arbeitsaufträge werden erstellt.

