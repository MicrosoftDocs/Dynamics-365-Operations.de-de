---
title: Finanzdimensionen definieren
description: Dieser Aufgabenleitfaden veranschaulicht das Hinzufügen einer Finanzdimension und einer benutzerdefinierten Finanzdimension auf Basis einer Entität.
author: aprilolson
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6fbe739eec0cfa1e7b0276872640bd4f82be3ef7
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138335"
---
# <a name="define-financial-dimensions"></a><span data-ttu-id="1e9aa-103">Finanzdimensionen definieren</span><span class="sxs-lookup"><span data-stu-id="1e9aa-103">Define financial dimensions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1e9aa-104">Dieser Aufgabenleitfaden veranschaulicht das Hinzufügen einer Finanzdimension und einer benutzerdefinierten Finanzdimension auf Basis einer Entität.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-104">This task guide demonstrates adding an entity backed financial dimension and a custom financial dimension.</span></span>  <span data-ttu-id="1e9aa-105">Der Leitfaden verwendet das Demounternehmen USMF.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-105">The guide uses the USMF demo company.</span></span>


## <a name="create-an-entity-backed-financial-dimension"></a><span data-ttu-id="1e9aa-106">Erstellen einer Finanzdimension auf Basis einer Entität</span><span class="sxs-lookup"><span data-stu-id="1e9aa-106">Create an entity backed financial dimension</span></span>
1. <span data-ttu-id="1e9aa-107">Gehen Sie zu **Navigationsbereich > Module > Hauptbuch > Kontenplan > Dimensionen > Finanzdimensionen**.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Dimensions > Financial dimensions**.</span></span>
2. <span data-ttu-id="1e9aa-108">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-108">Click **New**.</span></span>
3. <span data-ttu-id="1e9aa-109">Wählen Sie im Formularfeld **Benutzerwerte** eine vom System definierte Entität aus, auf der die Finanzdimension basieren soll.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-109">In the **User values form** field, select a system-defined entity to base the financial dimension on.</span></span> 
4. <span data-ttu-id="1e9aa-110">Geben Sie im Feld **Dimensionsname** einen Wert ein, um die Finanzdimension zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-110">In the **Dimension name** field, type a value to describe the financial dimension.</span></span> <span data-ttu-id="1e9aa-111">Der Name kann vom der im System definierte Entität abweichen. Er kann jedoch keine Leerzeichen und Sonderzeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-111">The name can be different than the system-defined entity but cannot contain spaces or special characters.</span></span>
5. <span data-ttu-id="1e9aa-112">Klicken Sie auf **Aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-112">Click **Activate**.</span></span> <span data-ttu-id="1e9aa-113">"Aktivieren der Finanzdimension" aktualisiert die Tabelle mit dem Finanzdimensionsnamen und entfernt gelöschte Dimensionen.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-113">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="1e9aa-114">Sie können Dimensionswerte eingegeben, bevor Sie eine Finanzdimension aktivieren, Finanzdimension kölnnen jedoch nicht verwendet werden, bis sie aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-114">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="1e9aa-115">Klicken Sie auf **Schließen** auf der Aktivierungsnachricht.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-115">Click **Close** on the activation message.</span></span>
7. <span data-ttu-id="1e9aa-116">Klicken Sie auf **Aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-116">Click **Activate**.</span></span> <span data-ttu-id="1e9aa-117">Die Dimensionsaktivierung kann geplant werden, um als Stapelverarbeitung zu einem bestimmten Datum und zu einer Zeit erledigt zu werden.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-117">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
8. <span data-ttu-id="1e9aa-118">Klicken Sie im **Aktivitätsbereich** auf **Dimensionswerte**.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-118">On **Action pane**, click **Dimension values**.</span></span> <span data-ttu-id="1e9aa-119">Einige Dimensionswerte sind unternehmensspezifisch.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-119">Some dimension values are company specific.</span></span> <span data-ttu-id="1e9aa-120">Sie können prüfen, ob sie unternehmensspezifisch sind, wenn der Unternehmensname in der Dimensionswertliste anzeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-120">You can verify if they are company specific by if the company name is showing in the dimension values list.</span></span>  

## <a name="create-a-custom-financial-dimension"></a><span data-ttu-id="1e9aa-121">Erstellen einer benutzerdefinierten Finanzdimension</span><span class="sxs-lookup"><span data-stu-id="1e9aa-121">Create a custom financial dimension</span></span>
1. <span data-ttu-id="1e9aa-122">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-122">Close the page.</span></span>
2. <span data-ttu-id="1e9aa-123">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-123">Click **New**.</span></span>
3. <span data-ttu-id="1e9aa-124">Wählen Sie im Feld **Werte verwenden aus** die Option **Benutzerdefinierte Dimension**.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-124">In the **Use values from** field, select **Custom dimension**.</span></span>
4. <span data-ttu-id="1e9aa-125">Geben Sie im Feld **Dimensionsname** einen Wert ein, um die Finanzdimension zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-125">In the **Dimension name** field, type a value to describe the financial dimension.</span></span>
    - <span data-ttu-id="1e9aa-126">Der Name darf keine Leerzeichen oder Sonderzeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-126">The name cannot contain spaces or special characters.</span></span>  
    - <span data-ttu-id="1e9aa-127">Sie können auch eine Kontenmaske angeben. Sie beschränkt die Menge und die Art von Informationen, die für Dimensionswerte eingegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-127">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span>   
    - <span data-ttu-id="1e9aa-128">Sie können Zeichen eingeben, die dieselben bleiben für jeden Dimensionswert, wie Buchstaben oder einen Bindestrich.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-128">You can enter characters that remain the same for each dimension value, such as letters or a hyphen.</span></span> <span data-ttu-id="1e9aa-129">Sie können auch Nummernzeichen (#) und kaufmännische Und-Zeichen (&) als Platzhalter für Buchstaben und Zahlen eingeben, die sich jedes Mal ändern werden, wenn ein Dimensionswert erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-129">You can also enter number signs (#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="1e9aa-130">Verwenden Sie ein Nummernzeichen (#) als Platzhalter für eine Zahl und ein kaufmännisches Und-Zeichen (&) als Platzhalter für einen Buchstaben.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-130">Use a number sign (#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span>  <span data-ttu-id="1e9aa-131">Beispiel: Um den Dimensionswert auf die Buchstaben CC und drei Zahlen einzuschränken, geben Sie CC-### als Formatmaske ein.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-131">Example: To limit the dimension value to the letters CC and three numbers, you enter CC-### as the format mask.</span></span>  
5. <span data-ttu-id="1e9aa-132">Klicken Sie auf **Aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-132">Click **Activate**.</span></span> <span data-ttu-id="1e9aa-133">"Aktivieren der Finanzdimension" aktualisiert die Tabelle mit dem Finanzdimensionsnamen und entfernt gelöschte Dimensionen.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-133">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="1e9aa-134">Sie können Dimensionswerte eingegeben, bevor Sie eine Finanzdimension aktivieren, Finanzdimension kölnnen jedoch nicht verwendet werden, bis sie aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-134">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>     
6. <span data-ttu-id="1e9aa-135">Klicken Sie auf **Aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-135">Click **Activate**.</span></span> <span data-ttu-id="1e9aa-136">Die Dimensionsaktivierung kann geplant werden, um als Stapelverarbeitung zu einem bestimmten Datum und zu einer Zeit erledigt zu werden.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-136">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>      
7. <span data-ttu-id="1e9aa-137">Klicken Sie im **Aktivitätsbereich** auf **Dimensionswerte**.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-137">On **Action pane**, click **Dimension values**.</span></span>
8. <span data-ttu-id="1e9aa-138">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-138">Click **New**.</span></span>
9. <span data-ttu-id="1e9aa-139">Geben Sie im Feld **Dimensionswert** einen Namen ein, um den Finanzdimensionswert zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-139">In the **Dimension value** field, type a name to describe your financial dimension value.</span></span>
10. <span data-ttu-id="1e9aa-140">Geben Sie im Textfeld eine **Beschreibung** ein, die den Finanzdimensionswert beschreibt.</span><span class="sxs-lookup"><span data-stu-id="1e9aa-140">In the **Description** field, type a description that describes your financial dimension value.</span></span>

