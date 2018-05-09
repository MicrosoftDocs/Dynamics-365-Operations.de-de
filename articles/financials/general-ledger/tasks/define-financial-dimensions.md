--- 
title: Finanzdimensionen definieren
description: "Dieser Aufgabenleitfaden veranschaulicht das Hinzufügen einer Finanzdimension und einer benutzerdefinierten Finanzdimension auf Basis einer Entität."
author: aprilolson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 192af4e8a9f77e4728954375d9d9699187137803
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---
# <a name="define-financial-dimensions"></a><span data-ttu-id="c7761-103">Finanzdimensionen definieren</span><span class="sxs-lookup"><span data-stu-id="c7761-103">Define financial dimensions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c7761-104">Dieser Aufgabenleitfaden veranschaulicht das Hinzufügen einer Finanzdimension und einer benutzerdefinierten Finanzdimension auf Basis einer Entität.</span><span class="sxs-lookup"><span data-stu-id="c7761-104">This task guide demonstrates adding an entity backed financial dimension and a custom financial dimension.</span></span>  <span data-ttu-id="c7761-105">Der Leitfaden verwendet das Demounternehmen USMF.</span><span class="sxs-lookup"><span data-stu-id="c7761-105">The guide uses the USMF demo company.</span></span>


## <a name="create-an-entity-backed-financial-dimension"></a><span data-ttu-id="c7761-106">Erstellen einer Finanzdimension auf Basis einer Entität</span><span class="sxs-lookup"><span data-stu-id="c7761-106">Create an entity backed financial dimension</span></span>
1. <span data-ttu-id="c7761-107">Wechseln Sie zu Hauptbuch >; Kontenplan > Dimensionen > Finanzdimensionen.</span><span class="sxs-lookup"><span data-stu-id="c7761-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="c7761-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="c7761-108">Click New.</span></span>
3. <span data-ttu-id="c7761-109">Wählen Sie im Feld "Benutzerwerte von" eine vom System definierte Entität aus, auf der die Finanzdimension basieren soll.</span><span class="sxs-lookup"><span data-stu-id="c7761-109">In the User values from field, select a system-defined entity to base the financial dimension on.</span></span> 
4. <span data-ttu-id="c7761-110">Geben Sie im Feld "Dimensionsname" einen Wert ein, um die Finanzdimension zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="c7761-110">In the Dimension name field, type a value to describe the financial dimension.</span></span>
    * <span data-ttu-id="c7761-111">Der Name kann vom der im System definierte Entität abweichen. Er kann jedoch keine Leerzeichen und Sonderzeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="c7761-111">The name can be different than the system-defined entity but cannot contain spaces or special characters.</span></span>  
5. <span data-ttu-id="c7761-112">Klicken Sie auf Aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c7761-112">Click Activate.</span></span>
    * <span data-ttu-id="c7761-113">"Aktivieren der Finanzdimension" aktualisiert die Tabelle mit dem Finanzdimensionsnamen und entfernt gelöschte Dimensionen.</span><span class="sxs-lookup"><span data-stu-id="c7761-113">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="c7761-114">Sie können Dimensionswerte eingegeben, bevor Sie eine Finanzdimension aktivieren, Finanzdimension kölnnen jedoch nicht verwendet werden, bis sie aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="c7761-114">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="c7761-115">Klicken Sie auf "Schließen" auf der Aktivierungsnachricht.</span><span class="sxs-lookup"><span data-stu-id="c7761-115">Click Close on the activation message.</span></span>
7. <span data-ttu-id="c7761-116">Klicken Sie auf Aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c7761-116">Click Activate.</span></span>
    * <span data-ttu-id="c7761-117">Die Dimensionsaktivierung kann geplant werden, um als Stapelverarbeitung zu einem bestimmten Datum und zu einer Zeit erledigt zu werden.</span><span class="sxs-lookup"><span data-stu-id="c7761-117">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
8. <span data-ttu-id="c7761-118">Klicken Sie auf "Dimensionswerte".</span><span class="sxs-lookup"><span data-stu-id="c7761-118">Click Dimension values.</span></span>
    * <span data-ttu-id="c7761-119">Einige Dimensionswerte sind unternehmensspezifisch.</span><span class="sxs-lookup"><span data-stu-id="c7761-119">Some dimension values are company specific.</span></span> <span data-ttu-id="c7761-120">Sie können prüfen, ob sie unternehmensspezifisch sind, wenn der Unternehmensname in der Dimensionswertliste anzeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c7761-120">You can verify if they are company specific by if the company name is showing in the dimension values list.</span></span>  

## <a name="create-a-custom-financial-dimension"></a><span data-ttu-id="c7761-121">Erstellen einer benutzerdefinierten Finanzdimension</span><span class="sxs-lookup"><span data-stu-id="c7761-121">Create a custom financial dimension</span></span>
1. <span data-ttu-id="c7761-122">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c7761-122">Close the page.</span></span>
2. <span data-ttu-id="c7761-123">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="c7761-123">Click New.</span></span>
3. <span data-ttu-id="c7761-124">Wählen Sie eine Option im Feld <Custom dimension> aus.</span><span class="sxs-lookup"><span data-stu-id="c7761-124">In the Use values from field, select <Custom dimension>.</span></span>
4. <span data-ttu-id="c7761-125">Geben Sie im Feld "Dimensionsname" einen Wert ein, um die Finanzdimension zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="c7761-125">In the Dimension name field, type a value to describe the financial dimension.</span></span>
    * <span data-ttu-id="c7761-126">Der Name darf keine Leerzeichen oder Sonderzeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="c7761-126">The name cannot contain spaces or special characters.</span></span>  
    * <span data-ttu-id="c7761-127">Sie können auch eine Kontenmaske angeben. Sie beschränkt die Menge und die Art von Informationen, die für Dimensionswerte eingegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="c7761-127">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span>   
    * <span data-ttu-id="c7761-128">Sie können Zeichen eingeben, die dieselben bleiben für jeden Dimensionswert, wie Buchstaben oder einen Bindestrich.</span><span class="sxs-lookup"><span data-stu-id="c7761-128">You can enter characters that remain the same for each dimension value, such as letters or a hyphen.</span></span> <span data-ttu-id="c7761-129">Sie können auch Nummernzeichen (#) und kaufmännische Und-Zeichen (&) als Platzhalter für Buchstaben und Zahlen eingeben, die sich jedes Mal ändern werden, wenn ein Dimensionswert erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c7761-129">You can also enter number signs (#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="c7761-130">Verwenden Sie ein Nummernzeichen (#) als Platzhalter für eine Zahl und ein kaufmännisches Und-Zeichen (&) als Platzhalter für einen Buchstaben.</span><span class="sxs-lookup"><span data-stu-id="c7761-130">Use a number sign (#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span>  <span data-ttu-id="c7761-131">Beispiel: Um den Dimensionswert auf die Buchstaben CC und drei Zahlen einzuschränken, geben Sie CC-### als Formatmaske ein.</span><span class="sxs-lookup"><span data-stu-id="c7761-131">Example: To limit the dimension value to the letters CC and three numbers, you enter CC-### as the format mask.</span></span>  
5. <span data-ttu-id="c7761-132">Klicken Sie auf Aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c7761-132">Click Activate.</span></span>
    * <span data-ttu-id="c7761-133">"Aktivieren der Finanzdimension" aktualisiert die Tabelle mit dem Finanzdimensionsnamen und entfernt gelöschte Dimensionen.</span><span class="sxs-lookup"><span data-stu-id="c7761-133">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="c7761-134">Sie können Dimensionswerte eingegeben, bevor Sie eine Finanzdimension aktivieren, Finanzdimension kölnnen jedoch nicht verwendet werden, bis sie aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="c7761-134">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="c7761-135">Klicken Sie auf Aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c7761-135">Click Activate.</span></span>
    * <span data-ttu-id="c7761-136">Die Dimensionsaktivierung kann geplant werden, um als Stapelverarbeitung zu einem bestimmten Datum und zu einer Zeit erledigt zu werden.</span><span class="sxs-lookup"><span data-stu-id="c7761-136">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
7. <span data-ttu-id="c7761-137">Klicken Sie auf "Dimensionswerte".</span><span class="sxs-lookup"><span data-stu-id="c7761-137">Click Dimension values.</span></span>
8. <span data-ttu-id="c7761-138">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="c7761-138">Click New.</span></span>
9. <span data-ttu-id="c7761-139">Geben Sie im Feld "Dimensionswert" einen Namen ein, um den Finanzdimensionswert zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="c7761-139">In the Dimension value field, type a name to describe your financial dimension value.</span></span>
10. <span data-ttu-id="c7761-140">Geben Sie im Textfeld eine Beschreibung ein, die den Finanzdimensionswert beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c7761-140">In the Description field, type a description that describes your financial dimension value.</span></span>


