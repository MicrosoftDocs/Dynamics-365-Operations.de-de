---
title: " Auffüllungsregeln für Crossdocking und Käuferübertragung einrichten"
description: Diese Prozedur zeigt die Schritte, um Auffüllungsregeln zu erstellen.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailReplenishmentRuleTable, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ecc3e1ce842e8d3b693b5e81ed665e9f3c00bfb5
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022628"
---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a> Auffüllungsregeln für Crossdocking und Käuferübertragung einrichten

[!include[task guide banner](../includes/task-guide-banner.md)]

Diese Prozedur zeigt die Schritte, um Auffüllungsregeln zu erstellen. Auffüllungsregeln können verwendet werden, um zu steuern, wie Produkte an Shops verteilt werden, wenn Crossdocking und Käuferübertragung verwendet werden. Auffüllungsregeln können für Shops oder Shopgruppen eingerichtet werden. Das Gewicht, das für jede Position in einer Regel definiert wurde, steuert, wie die Mengen von Produkten zwischen den Shops verteilt werden, wenn die Auffüllungsregeln als die Verteilungsmethode im Crossdocking oder in der Käuferübertragung verwendet werden. Für diese Prozedur wird das Demo-Unternehmen USRT verwendet.

1. Gehen Sie zu "Auffüllungsregeln".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Auffüllungsregel" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Klicken Sie auf "Speichern".
6. Klicken Sie auf Hinzufügen.
7. Markieren Sie in der Liste die ausgewählte Zeile.
    * Sie können "Auffüllungshierarchie" oder "Kanal" für den Typ auswählen. Der Wert überprüft, ob die Auswahl in "Name" eine Hierarchie von Kanälen oder ein bestimmter Kanal ist.  Im vorliegenden Beispiel lassen Sie es festgelegt als "Auffüllungshierarchie".  
8. Wählen Sie im Feld "Name" einen Wert aus.
    * Der standardmäßige Gewichtswert wird aus dem Gewicht ausgefüllt, das für den Lagerort definiert ist.  Dieses Gewicht kann für die Auffüllungsregel verwendet werden, oder Sie können ein neues Gewicht im Feld "Gewicht" eingeben.  
9. Geben Sie im Feld "Gewicht" eine Zahl ein.
10. Klicken Sie auf Hinzufügen.
11. Markieren Sie in der Liste die ausgewählte Zeile.
12. Wählen Sie im Feld "Typ" die Option "Kanal" aus.
13. Geben Sie im Feld "Name" einen Wert ein, oder wählen Sie einen Wert aus.
14. Geben Sie im Feld "Gewicht" eine Zahl ein.
15. Klicken Sie auf "Speichern".

