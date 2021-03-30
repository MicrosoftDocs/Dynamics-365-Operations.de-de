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
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3d4cd276283483340f1dc0bc995cc9073a8aa9c0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232688"
---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a> Auffüllungsregeln für Crossdocking und Käuferübertragung einrichten

[!include [banner](../includes/banner.md)]

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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]