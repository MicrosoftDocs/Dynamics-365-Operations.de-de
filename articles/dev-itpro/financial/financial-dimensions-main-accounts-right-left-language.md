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
ms.search.scope: Core, Operations
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9859023853b235aa2695ee5c595627571a4d746c
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="financial-dimensions-and-main-accounts-in-a-right-to-left-language"></a><span data-ttu-id="b9a55-103">Finanzdimensionen und Hauptkonten in einer Rechts-nach-links-Sprache</span><span class="sxs-lookup"><span data-stu-id="b9a55-103">Financial dimensions and main accounts in a right-to-left language</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b9a55-104">In diesem Thema werden einige der Implementierungsentscheidungen beschrieben, die Sie berücksichtigen sollten, wenn Sie eine Rechts-nach-links-Sprache verwenden, und Sie müssen Finanzdimensionen und Hauptkonten einrichten.</span><span class="sxs-lookup"><span data-stu-id="b9a55-104">This topic describes some of the implementation decisions that you should consider when you use a right-to-left language, and you must set up financial dimensions and main accounts.</span></span>

<span data-ttu-id="b9a55-105">Finanzdimensionen und Hauptkonten sind Schlüsselkomponenten der Planungsphase für eine Implementierung.</span><span class="sxs-lookup"><span data-stu-id="b9a55-105">Financial dimensions and main accounts are key components of the planning phase for an implementation.</span></span> <span data-ttu-id="b9a55-106">Nachdem Finanzdimensionen und Hauptkonten im System erstellt wurden, werden sie auf den Seiten **Kontostrukturen konfigurieren**, **Erweiterte Regelstrukturen** und **Finanzdimensionskonfiguration zum Integrieren von Anwendungen** verwendet.</span><span class="sxs-lookup"><span data-stu-id="b9a55-106">After financial dimensions and main accounts are created in the system, they are used on the **Configure account structures**, **Advanced rule structures**, and **Financial dimension configuration for integrating applications** pages.</span></span> <span data-ttu-id="b9a55-107">Die Reihenfolge, die auf diesen Seiten definiert wird, wird im System für die Dateneingabe und -nutzung verwendet.</span><span class="sxs-lookup"><span data-stu-id="b9a55-107">The order that is defined on those pages is used in the system for data entry and consumption.</span></span> <span data-ttu-id="b9a55-108">An verschiedenen Stellen im System werden die Finanzdimensionen und Hauptkonten in separaten Feldern angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b9a55-108">In some places in the system, the financial dimensions and main accounts appear in separate fields.</span></span> <span data-ttu-id="b9a55-109">Allerdings an anderen Stellen, wie Erfassungen, werden die Finanzdimensionen und Hauptkonten als einzelne Zeichenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b9a55-109">However, in other places, such as journals, the financial dimensions and main accounts appear as a single string.</span></span>

### <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a><span data-ttu-id="b9a55-110">Optimale Verfahren zum Einrichten von Finanzdimensionen und Hauptkonten in einem Rechts-nach-links-System</span><span class="sxs-lookup"><span data-stu-id="b9a55-110">Best practices for setting up financial dimensions and main accounts in a right-to-left system</span></span>

-   <span data-ttu-id="b9a55-111">Wenn Sie das Trennzeichen für Kontenpläne auswählen, wählen Sie eine der Optionen für doppelte Trennzeichen aus: doppelter Bindestrich (--), doppelter Balken (||), doppelter Punkt (..) oder doppelter Unterstrich  (\_\_).</span><span class="sxs-lookup"><span data-stu-id="b9a55-111">When you select the delimiter for charts of accounts, select one of the double delimiter options: double hyphen (--), double bar (||) or double period (..), or double underscore (\_\_).</span></span>
-   <span data-ttu-id="b9a55-112">Wenn Sie Finanzdimensions- und Hauptkontowerte erstellen, verwenden Sie nur Nummern sowie Zeichen von Rechts-nach-Links-Sprachen.</span><span class="sxs-lookup"><span data-stu-id="b9a55-112">When you create financial dimension and main account values, use only numbers and right-to-left language characters.</span></span>
-   <span data-ttu-id="b9a55-113">Vermeiden Sie es, die ausgewählte Trennzeichen für Kontenpläne in den Finanzdimensions- und Hauptkontowerten zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b9a55-113">Avoid using the selected chart of accounts delimiter in financial dimension and main account values.</span></span>

<span data-ttu-id="b9a55-114">Indem Sie diese bewährten Methoden verwenden, tragen Sie zu einer konsistenten Darstellung der benutzerdefinierten Reihenfolge im gesamten System bei.</span><span class="sxs-lookup"><span data-stu-id="b9a55-114">By following these best practices, you help guarantee consistent representation of the user defined-order throughout the system.</span></span>




