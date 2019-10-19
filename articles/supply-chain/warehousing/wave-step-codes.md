---
title: Wellenschrittcodes
description: Dieses Thema bietet einen Überblick über Wellenschrittcodes und wie diese verwendet werden.
author: josaw1
manager: AnnBe
ms.date: 09/06/2019
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
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f89c6098db9e2e3a9aa4ee3666e4b9ae608f054
ms.sourcegitcommit: d8f1135cdbc2deca70bc4b2805a0519253c9a31f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/06/2019
ms.locfileid: "1992356"
---
# <a name="wave-step-codes"></a><span data-ttu-id="31af2-103">Wellenschrittcodes</span><span class="sxs-lookup"><span data-stu-id="31af2-103">Wave step codes</span></span>

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

## <a name="about-wave-step-codes"></a><span data-ttu-id="31af2-104">Info über Wellenschrittcodes</span><span class="sxs-lookup"><span data-stu-id="31af2-104">About wave step codes</span></span>

<span data-ttu-id="31af2-105">Wellenschrittcodes sind Codes, die Benutzer einrichten und verwenden können, um bestimmte Instanzen von Wellenmethoden mit einer entsprechenden Vorlage zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="31af2-105">Wave step codes are codes that users can set up and use to link specific instances of wave methods to a corresponding template.</span></span> <span data-ttu-id="31af2-106">Die Vorlagen enthalten Vorlagen für die Auffüllung, Containerisierung, Etikettendruck, Auslastungsgebäude und Sortieren.</span><span class="sxs-lookup"><span data-stu-id="31af2-106">The templates include templates for replenishment, containerization, label printing, load building, and sorting.</span></span>

<span data-ttu-id="31af2-107">Wenn keine Wellenschrittcodes verwendet werden, müssen Benutzer Freitext eingeben, um auf eine bestimmte Vorlage aus der Wellenmethodeninstanz zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="31af2-107">When wave step codes aren't used, users must enter free text to reference a specific template from the wave method instance.</span></span> <span data-ttu-id="31af2-108">Freier Text ist fehleranfällig, da Benutzer sicherstellen müssen, dass der Wellenschritttext, den sie für eine bestimmte Wellenschrittmethode in einer Wellenvorlage hinzufügen, genau mit dem Wellenschritttext in der Zielvorlage übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="31af2-108">Free text is prone to error, because users must make sure that the wave step text that they add for a specific wave step method in a wave template exactly matches the wave step text in the target template.</span></span>

<span data-ttu-id="31af2-109">Wellenschrittcodes für einen bestimmten Wellenschritttyp werden auf einer separaten Seite eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="31af2-109">Wave step codes for a specific wave step type are set up on a separate page.</span></span> <span data-ttu-id="31af2-110">Für jede Wellenschritt-Methodeninstanz in einer Wellenvorlage, die einen Wellenschrittcode erfordert, muss der Wellenschrittcode in einer Dropdownliste ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="31af2-110">For every wave step method instance in a wave template that requires a wave step code, the wave step code must be selected in a drop-down list.</span></span> <span data-ttu-id="31af2-111">Die Auswahl in einer Dropdownliste ersetzt den freien Texteintrag und hilft, das Risiko und die Auswirkungen des menschlichen Versagens zu verringern.</span><span class="sxs-lookup"><span data-stu-id="31af2-111">Selection in a drop-down list replaces free text entry and helps reduce the risk and impact of human error.</span></span> <span data-ttu-id="31af2-112">Einstellungscodes werden verwendet, um eine Wellenschrittmethode in einer Wellenvorlage zu einer Zielvorlage für die Methode zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="31af2-112">Setup codes are used to link a wave step method in a wave template to a target template for the method.</span></span>

> [!NOTE]
> <span data-ttu-id="31af2-113">Die Verwendung der Wellenschritt-Codefunktion ist optional und erfolgt pro juristischer Person.</span><span class="sxs-lookup"><span data-stu-id="31af2-113">Use of the wave step codes feature is optional, and uptake is per legal entity.</span></span> <span data-ttu-id="31af2-114">Wenn eine bestimmte juristische Person die Funktion verwendet, werden alle vorhandenen Wellenschrittcodes dieser juristischen Person in der neuen Struktur aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="31af2-114">Therefore, if a specific legal entity uses the feature, all existing wave step codes in that legal entity are upgraded to the new structure.</span></span>

## <a name="setup-demo"></a><span data-ttu-id="31af2-115">Demo einrichten</span><span class="sxs-lookup"><span data-stu-id="31af2-115">Setup demo</span></span> 

<span data-ttu-id="31af2-116">Für diese Vorführung müssen Demodaten eingerichtet werden, und Sie müssen das **USMF**-Demodatunternehmen verwenden.</span><span class="sxs-lookup"><span data-stu-id="31af2-116">For this demo, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="enable-wave-step-codes"></a><span data-ttu-id="31af2-117">Wellenschrittcodes aktivieren</span><span class="sxs-lookup"><span data-stu-id="31af2-117">Enable wave step codes</span></span>

<span data-ttu-id="31af2-118">Gehen Sie folgendermaßen vor, um die Wellenschritt-Codefunktion zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="31af2-118">Follow these steps to turn on the wave step codes feature.</span></span>

1. <span data-ttu-id="31af2-119">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerortverwaltungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="31af2-119">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
2. <span data-ttu-id="31af2-120">Legen Sie auf der Registerkarte **Allgemein** im Inforegister **Wellenverarbeitung** die Option **Wellenschrittcodes aktivieren** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="31af2-120">On the **General** tab, on the **Wave processing** FastTab, set the **Enable wave step codes** option to **Yes**.</span></span>

<span data-ttu-id="31af2-121">Alle Freitextrechnungen des vorhandenen Wellenschritts werden in der neuen Struktur aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="31af2-121">All existing wave step free texts are upgraded to the new structure.</span></span> <span data-ttu-id="31af2-122">Nachdem diese Aktualisierung für eine juristische Person abgeschlossen ist, ist die Option **Wellenschrittcodes aktivieren** nicht mehr auf der Seite **Lagerverwaltungsparameter** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="31af2-122">After this upgrade is completed for a legal entity, the **Enable wave step codes** option is no longer available on the **Warehouse management parameters** page.</span></span>

<span data-ttu-id="31af2-123">Überprüfungen werden während der Aktualisierung ausgeführt, und wenn die Aktualisierung nicht erfolgreich ist, wird eine Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="31af2-123">Validations are done during the upgrade, and if the upgrade fails, you receive an error message.</span></span> <span data-ttu-id="31af2-124">Eine Aktualisierung kann aufgrund der folgenden Konflikte fehlschlagen:</span><span class="sxs-lookup"><span data-stu-id="31af2-124">An upgrade might fail because of the following conflicts:</span></span>

- <span data-ttu-id="31af2-125">Es sind doppelte Freitexte des Wellenschritts vorhanden.</span><span class="sxs-lookup"><span data-stu-id="31af2-125">Duplicate wave step free texts exist.</span></span>
- <span data-ttu-id="31af2-126">Es sind Anpassungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="31af2-126">Customizations exist.</span></span>
- <span data-ttu-id="31af2-127">Ein Wellenschrittfreitext, der einer Wellenschritt-Methodeninstanz zugeordnet ist, entspricht nicht dem erwarteten Vorlagentyp.</span><span class="sxs-lookup"><span data-stu-id="31af2-127">A wave step free text that is associated with a wave step method instance doesn't match the expected template type.</span></span>

<span data-ttu-id="31af2-128">Nachdem Sie alle Konflikte behoben haben, die während der Überprüfung auftraten, können Sie den Aktualisierungsprozess wiederholen.</span><span class="sxs-lookup"><span data-stu-id="31af2-128">After you've resolved any conflicts that are identified during the validations, you can rerun the upgrade process.</span></span>

<span data-ttu-id="31af2-129">Wenn die Aktualisierung erfolgreich war, steht die Seite **Wellenschrittcodes** (**Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenschrittcodes**) zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="31af2-129">When the upgrade succeeds, the **Wave step codes** page (**Warehouse management \> Setup \> Waves \> Wave step codes**) becomes available.</span></span> <span data-ttu-id="31af2-130">Auf dieser Seite werden die Wellenschrittcodes aufgelistet, die aktualisiert wurden, als die Wellenschritt-Codefunktion aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="31af2-130">This page lists the wave step codes that were upgraded when the wave step codes feature was turned on.</span></span>

### <a name="create-new-wave-step-codes"></a><span data-ttu-id="31af2-131">Erstellen neuer Wellenschrittcodes</span><span class="sxs-lookup"><span data-stu-id="31af2-131">Create new wave step codes</span></span>

<span data-ttu-id="31af2-132">Sie können die Seite **Wellenschrittcodes** verwenden, um Wellenschrittcodes zu erstellen und zu löschen.</span><span class="sxs-lookup"><span data-stu-id="31af2-132">You can use the **Wave step codes** page to create and delete wave step codes.</span></span>

<span data-ttu-id="31af2-133">Jeder neue Wellenschrittcode und die zugeordnete Kennung müssen für alle Wellenschritttypen eindeutig sein, und sie müssen für einen bestimmten Wellenschritttyp definiert werden.</span><span class="sxs-lookup"><span data-stu-id="31af2-133">Every new wave step code and its associated ID must be unique across all wave step types, and they must be defined for a specific wave step type.</span></span>

### <a name="apply-wave-step-codes"></a><span data-ttu-id="31af2-134">Wellenschrittcodes anwenden</span><span class="sxs-lookup"><span data-stu-id="31af2-134">Apply wave step codes</span></span>

<span data-ttu-id="31af2-135">Nachdem Sie die gewünschten Wellenschrittcodes definiert haben, können sie auf die Wellenprozessmethoden angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="31af2-135">After you've defined the appropriate wave step codes, they can be applied to the wave process methods.</span></span>

<span data-ttu-id="31af2-136">Um Wellenschrittcodes anzuwenden, wechseln zur entsprechenden Zielvorlage.</span><span class="sxs-lookup"><span data-stu-id="31af2-136">To apply wave step codes, go to the appropriate target template.</span></span> <span data-ttu-id="31af2-137">Hierbei gelten die Zielvorlagen, auf die die Wellenschrittcodes verweisen:</span><span class="sxs-lookup"><span data-stu-id="31af2-137">Here are the target templates that the wave step codes are designated to point to:</span></span>

- <span data-ttu-id="31af2-138">**Wiederbeschaffungsvorlagen:** Lagerortverwaltung \> Einstellungen \> Wiederbeschaffung \> Wiederbeschaffungsvorlagen</span><span class="sxs-lookup"><span data-stu-id="31af2-138">**Replenishment templates:** Warehouse management \> Setup \> Replenishment \> Replenishment templates</span></span>
- <span data-ttu-id="31af2-139">**Ladungserstellungsvorlagen:** Lagerortverwaltung \> Einstellungen \> Laden \> Ladungserstellungsvorlagen</span><span class="sxs-lookup"><span data-stu-id="31af2-139">**Load build templates:** Warehouse management \> Setup \> Load \> Load build templates</span></span>
- <span data-ttu-id="31af2-140">**Vorlagen sortieren:** Lagerortverwaltung \> Einstellungen \> Verpackung \> Ausgehende Sortierenvorlagen</span><span class="sxs-lookup"><span data-stu-id="31af2-140">**Sort templates:** Warehouse management \> Setup \> Packing \> Outbound sorting templates</span></span>
- <span data-ttu-id="31af2-141">**Containerisierungsvorlagen:** Lagerortverwaltung \> Einstellungen \> Container \> Containererstellungsvorlagen</span><span class="sxs-lookup"><span data-stu-id="31af2-141">**Containerization templates:** Warehouse management \> Setup \> Containers \> Container build templates</span></span>
- <span data-ttu-id="31af2-142">**Etikettendruckvorlagen:** Lagerortverwaltung \> Einstellungen \> Dokumentweiterleitung \> Wellenbeschriftungsvorlagen</span><span class="sxs-lookup"><span data-stu-id="31af2-142">**Label printing templates:** Warehouse management \> Setup \> Document routing \> Wave label templates</span></span>

<span data-ttu-id="31af2-143">Die Vorlagen in dieser Liste werden angewendet, wenn auf sie aus einer Wellenprozessmethode verwiesen wird, die in einer Wellenvorlage aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="31af2-143">The templates in this list are applied when they are referenced from a wave process method that is selected in a wave template.</span></span> <span data-ttu-id="31af2-144">Wenn der Wellenschrittcode auf einer Wellenprozessmethode in einer Wellenvorlage den Wellenschrittcode in einem der Vorlagentypen entspricht, wird die Vorlage angewendet.</span><span class="sxs-lookup"><span data-stu-id="31af2-144">When the wave step code on a wave process method in a wave template matches the wave step code in one of the templates types, the template is applied.</span></span>

### <a name="sample-scenario"></a><span data-ttu-id="31af2-145">Beispielszenario</span><span class="sxs-lookup"><span data-stu-id="31af2-145">Sample scenario</span></span>

<span data-ttu-id="31af2-146">Die folgenden Prozedurhilfen stellen sicher, dass die Wiederbeschaffungsvorlage, die Sie erstellt haben, auf die Wellenvorlage angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="31af2-146">The following procedure helps guarantee that the replenishment template that you created will be applied for the wave template.</span></span>

1. <span data-ttu-id="31af2-147">Navigieren Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenschrittcodes**, und erstellen Sie einen Wellenschrittcode für den Typ **Wiederbeschaffung**.</span><span class="sxs-lookup"><span data-stu-id="31af2-147">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**, and create a wave step code for the **Replenishment** type.</span></span>
2. <span data-ttu-id="31af2-148">Navigieren Sie zu **Lagerortverwaltung \> Einstellungen \> Wiederbeschaffung \> Wiederbeschaffungsvorlagen**, und erstellen Sie eine Wiederbeschaffungsvorlage.</span><span class="sxs-lookup"><span data-stu-id="31af2-148">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**, and create a replenishment template.</span></span>
3. <span data-ttu-id="31af2-149">In der Wiederbeschaffungsvorlage wählen Sie den Wellenschrittcode aus, den Sie für die Art haben **Wiederbeschaffung**</span><span class="sxs-lookup"><span data-stu-id="31af2-149">In the replenishment template, select the wave step code that you created for the **Replenishment** type.</span></span>
4. <span data-ttu-id="31af2-150">Navigieren Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenvorlagen**, und wählen Sie die Wellenvorlage aus, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="31af2-150">Go to **Warehouse management \> Setup \> Waves \> Wave templates**, and select the wave template that you intend to use.</span></span>
5. <span data-ttu-id="31af2-151">In der Vorlage auf dem Inforegister **Methoden** wählen Sie die Methode **Wiederbeschaffung**.</span><span class="sxs-lookup"><span data-stu-id="31af2-151">In the template, on the **Methods** FastTab, select the **Replenishment** method.</span></span>
6. <span data-ttu-id="31af2-152">Im Feld **Wellenschrittcode** wählen Sie den Wellenschrittcode aus, den Sie für die Wiederbeschaffungsvorlage ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="31af2-152">In the **Wave step code** field, select the wave step code that you selected in the replenishment template.</span></span>
