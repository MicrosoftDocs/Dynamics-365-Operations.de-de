---
title: Erstellen von Arbeitsaufträgen
description: In diesem Thema wird erläutert, wie Sie Arbeitsaufträge in der Anlagenverwaltung erstellen.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b23ed3251b2f6cf4f34b423ce2f85301d6ab31a1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875667"
---
# <a name="creating-work-orders"></a>Erstellen von Arbeitsaufträgen


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Wenn Sie vorbeugende Wartungsaufträge geplant haben, ist der nächste Schritt, Arbeitsaufträge für die Einzelvorgänge zu erstellen. Dies erfolgt in einem der Wartungszeitpläne. Die geplanten Einzelvorgänge in einem Wartungszeitplan können verschiedene Referenztypen haben:

| Referenztyp | Beschreibung                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| Wartungspläne     | Vorbeugende Wartungsaufträge auf Grundlage der Wartungsplantypen „Zeit“ oder „Zähler“.                       |
| Wartungsdurchgänge    | Vorbeugende Wartungsaufträge, die mehrere Anlagen enthalten, die einen ähnlichen Wartungstyp erfordern.           |
| Wartungsanfrage   | Manuell erstellte Anforderung für die Wartung oder Reparatur einer Anlage, die in einen Arbeitsauftrag konvertiert werden kann. |


1. Klicken Sie auf **Anlagenverwaltung** > **Allgemein** > **Alle Wartungspläne** oder **Wartungszeitplanpositionen öffnen** oder **Wartungszeitplanpools öffnen**.

2. Wählen Sie die geplanten Wartungsaufträge aus, für die Sie einen Arbeitsauftrag erstellen möchten, und klicken Sie auf **Arbeitsauftrag**. Die Gesamtanzahl von Planungsstunden für die ausgewählten Positionen wird im Feld **Wartungsprognosestunden** angezeigt.

3. Im Abschnitt **Parameter** wählen Sie aus, wie viele Arbeitsaufträge erstellt werden sollen. Sie können einen Arbeitsauftrag pro Wartungszeitplanposition oder mehrere Arbeitsaufträge basierend auf Ihrer Auswahl im Abschnitt **Ein Arbeitsauftrag pro** erstellen.

4. Wählen Sie einen **Arbeitsauftragstyp** aus, der für alle Arbeitsaufträge verwendet wird, die Sie erstellen.

5. Klicken Sie auf **OK**. Einer oder mehrere Arbeitsaufträge werden erstellt.

![Abbildung 1](media/18-preventive-maintenance.png)

