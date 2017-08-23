--- 
title: "Berechnung zu einem Produktkonfigurationsmodell hinzufügen"
description: "Im folgenden Verfahren sehen Sie, wie Sie einen neuen Berechnung zu einem Produktkonfigurationsmodell hinzufügen können."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 9ac2d9bcc316a57941136c248a0c5ff030a1fe49
ms.contentlocale: de-de
ms.lasthandoff: 07/28/2017

---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>Berechnung zu einem Produktkonfigurationsmodell hinzufügen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Im folgenden Verfahren sehen Sie, wie Sie einen neuen Berechnung zu einem Produktkonfigurationsmodell hinzufügen können. Darin wird angezeigt, wie Sie einen logischen Ausdruck unter Verwendung des "If"-Operators erstellen können, um eine Lautsprecherhöhe bis 10 für weiße Lautsprecher und 15 für alle anderen Gehäusefarben festzulegen. Das Verfahren verwendet die Komponente "High end speaker" im Vorführungsunternehmen USMF.


## <a name="add-a-calculation"></a>Eine Berechnung hinzufügen

## <a name="create-calculation-expression"></a>Berechnungsausdruck erstellen
1. Klicken Sie auf "Ausdruck bearbeiten".
2. Geben Sie im Feld "ConstraintBody" "If[CabinetFinish== "White", 10, 15]" ein.
3. Klicken Sie auf "Überprüfen".
4. Klicken Sie auf "Schließen".
5. Klicken Sie auf "OK".


