---
title: Finanzdimensionen und Hauptkonten in einer Rechts-nach-links-Sprache
description: "In diesem Thema werden einige der Implementierungsentscheidungen beschrieben, die Sie berücksichtigen sollten, wenn Sie eine Rechts-nach-links-Sprache verwenden, und Sie müssen Finanzdimensionen und Hauptkonten einrichten."
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b8ceee7486cae9ec0ff7dfedc35909e2f01d0616
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="financial-dimensions-and-main-accounts-in-a-right-to-left-language"></a>Finanzdimensionen und Hauptkonten in einer Rechts-nach-links-Sprache

[!include[banner](../includes/banner.md)]


In diesem Thema werden einige der Implementierungsentscheidungen beschrieben, die Sie berücksichtigen sollten, wenn Sie eine Rechts-nach-links-Sprache verwenden, und Sie müssen Finanzdimensionen und Hauptkonten einrichten.

Finanzdimensionen und Hauptkonten sind Schlüsselkomponenten der Planungsphase für eine Implementierung. Nachdem Finanzdimensionen und Hauptkonten im System erstellt wurden, werden sie auf den Seiten **Kontostrukturen konfigurieren**, **Erweiterte Regelstrukturen** und **Finanzdimensionskonfiguration zum Integrieren von Anwendungen** verwendet. Die Reihenfolge, die auf diesen Seiten definiert wird, wird im System für die Dateneingabe und -nutzung verwendet. An verschiedenen Stellen im System werden die Finanzdimensionen und Hauptkonten in separaten Feldern angezeigt. Allerdings an anderen Stellen, wie Erfassungen, werden die Finanzdimensionen und Hauptkonten als einzelne Zeichenfolge angezeigt.

### <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a>Optimale Verfahren zum Einrichten von Finanzdimensionen und Hauptkonten in einem Rechts-nach-links-System

-   Wenn Sie das Trennzeichen für Kontenpläne auswählen, wählen Sie eine der Optionen für doppelte Trennzeichen aus: doppelter Bindestrich (--), doppelter Balken (||), doppelter Punkt (..) oder doppelter Unterstrich  (\_\_).
-   Wenn Sie Finanzdimensions- und Hauptkontowerte erstellen, verwenden Sie nur Nummern sowie Zeichen von Rechts-nach-Links-Sprachen.
-   Vermeiden Sie es, die ausgewählte Trennzeichen für Kontenpläne in den Finanzdimensions- und Hauptkontowerten zu verwenden.

Indem Sie diese bewährten Methoden verwenden, tragen Sie zu einer konsistenten Darstellung der benutzerdefinierten Reihenfolge im gesamten System bei.




