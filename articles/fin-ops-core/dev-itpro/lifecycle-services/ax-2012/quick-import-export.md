---
title: Direktimport/-export
description: Zweck des Direktimports/-exports ist der Import und Export über weniger Schritte.
author: margoc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: AX 2012
ms.custom: 89041
ms.assetid: 990d64e6-d436-4c79-9bb5-bf8c5c5a048f
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 2012 R3 CU8
ms.openlocfilehash: 7655de1399c49328bae1736c796325e546796bd5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181150"
---
# <a name="quick-import-export"></a>Direktimport/-export

[!include [banner](../../includes/banner.md)]

Zweck des Direktimports/-exports ist der Import und Export über weniger Schritte.

Wir haben eine Funktion für den Direktimport/-export hinzugefügt, um den Benutzer den schnellen Import oder Export von einfachen Einzelaufträgen zu ermöglichen. Die Funktion wird im Idealfall in Szenarien genutzt, in denen eine Datei automatisch zum System zugeordnet wird und der Benutzer keine erweiterte Zuordnung durchführen oder wiederholt Import- oder Exportvorgänge erstellen muss.

- Diese Funktion unterstützt die Arbeit mit standardmäßigen und angepassten Entitäten.
- Sie können aus Dateien importieren. Wenn Sie eine ODBC-Datenquelle verwenden, können Sie eine Abfrage zum Definieren des Imports auswählen.
- Sie müssen zuvor Quelldatenformate für AX oder Datei definiert haben und deren Speicherort kennen.
- Sie müssen keine Verarbeitungsgruppe für den Direktimport/-export erstellen. Das System erstellt bei der Ausführung automatisch eine Verarbeitungsgruppe. Sie können außerdem den Verlauf der importieren/exportieren Daten speichern.

  Beachten Sie, dass der Direktimport/-export davon ausgeht, dass Sie mit den DIXF-Konzepten vertraut sind.



