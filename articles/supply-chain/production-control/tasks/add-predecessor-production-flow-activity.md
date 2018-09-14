--- 
title: "Eine vorherige Aktivität zu einer Produktionsflussaktivität hinzufügen"
description: "In einer Produktionsflussversion müssen alle Aktivitäten geordnet werden."
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: d19fb20e8cc941daeaa506e4bf1cb0c7031cf2ee
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a>Eine vorherige Aktivität zu einer Produktionsflussaktivität hinzufügen

[!include [task guide banner](../../includes/task-guide-banner.md)]

In einer Produktionsflussversion müssen alle Aktivitäten geordnet werden. Eine Aktivität kann ein oder mehrere vorherige Aktivitäten oder Folgeaktivitäten haben. 

Dieses Verfahren zeigt, wie eine vorherige Aktivität zu einer Aktivität zugeordnet werden. 

Um diese Aufgabe durchzuführen, benötigen Sie einen Produktionsfluss das die Entwurfsversion mit mindestens zwei Aktivitäten hat, die zugeordnet werden können. 

Weitere Informationen finden Sie im Whitepaper "Produktionsflüsse und Aktivitäten beim Lean Manufacturing".


## <a name="find-the-production-flow-and-version"></a>Suchen der Produktionsfluss und -version
1. Wechseln Sie zu "Produktionssteuerung" > "Einrichten" > "Lean-Produktionsfluss" > "Produktionsflüsse".
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
5. Klicken Sie auf "Aktivitäten".

## <a name="select-an-activity-and-add-a-predecessor"></a>Aktivität auswählen und eine vorherige Aktivität hinzufügen
1. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
2. Klicken Sie auf "Vorherige Aktivität hinzufügen".
3. Geben Sie im Feld 'Aktivität' einen Wert ein, oder wählen Sie einen Wert aus.
4. Geben Sie im Feld "Zykluszeitanteil" eine Zahl ein.
    * Der Standardzykluszeitanteil einer Aktivitätsrelation ist 1. Diese nimmt an, dass die beiden Aktivitäten mit dem gleichen Tempo oder zur gleichen Taktzeit ausgeführt werden. Wenn die vorherige Aktivität an einem höheren Tempo (niedrigere Taktzeit) ausgeführt wird, sollte das Verhältnis niedriger als 1 sein. Wenn die vorherige Aktivität in einem langsameren Tempo (höhere Taktzeit) ausgeführt wird, ist der Zykluszeitanteil größer als 1.  
5. Klicken Sie auf "OK".


