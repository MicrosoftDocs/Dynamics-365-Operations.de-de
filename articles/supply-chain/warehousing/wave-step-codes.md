---
title: Wellenschrittcodes
description: Dieses Thema bietet einen Überblick über Wellenschrittcodes und wie diese verwendet werden.
author: josaw1
manager: tfehr
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 251e9982451c888424589e0f0d6fce48aab42df1
ms.sourcegitcommit: 68092ed283bfbb7b6f611cce1b62c791f9b6a208
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2020
ms.locfileid: "3323576"
---
# <a name="wave-step-codes"></a><span data-ttu-id="8f728-103">Wellenschrittcodes</span><span class="sxs-lookup"><span data-stu-id="8f728-103">Wave step codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8f728-104">Wellenschrittcodes sind Codes, die Benutzer einrichten und verwenden können, um bestimmte Instanzen von Wellenmethoden mit einer entsprechenden Vorlage zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="8f728-104">Wave step codes are codes that users can set up and use to link specific instances of wave methods to a corresponding template.</span></span> <span data-ttu-id="8f728-105">Die Vorlagen enthalten Vorlagen für die Auffüllung, Containerisierung, Etikettendruck, Auslastungsgebäude und Sortieren.</span><span class="sxs-lookup"><span data-stu-id="8f728-105">The templates include templates for replenishment, containerization, label printing, load building, and sorting.</span></span>

<span data-ttu-id="8f728-106">Wenn keine Wellenschrittcodes verwendet werden, müssen Benutzer Freitext eingeben, um auf eine bestimmte Vorlage aus der Wellenmethodeninstanz zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="8f728-106">When wave step codes aren't used, users must enter free text to reference a specific template from the wave method instance.</span></span> <span data-ttu-id="8f728-107">Freier Text ist fehleranfällig, da Benutzer sicherstellen müssen, dass der Wellenschritttext, den sie für eine bestimmte Wellenschrittmethode in einer Wellenvorlage hinzufügen, genau mit dem Wellenschritttext in der Zielvorlage übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="8f728-107">Free text is prone to errors because users must make sure that the wave step text that they add for a specific wave step method in a wave template exactly matches the wave step text in the target template.</span></span>

<span data-ttu-id="8f728-108">Wellenschrittcodes für einen bestimmten Wellenschritttyp werden auf einer separaten Seite eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="8f728-108">Wave step codes for a specific wave step type are set up on a separate page.</span></span> <span data-ttu-id="8f728-109">Für jede Wellenschritt-Methodeninstanz in einer Wellenvorlage, die einen Wellenschrittcode erfordert, muss der Wellenschrittcode in einer Dropdownliste ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="8f728-109">For every wave step method instance in a wave template that requires a wave step code, the wave step code must be selected in a drop-down list.</span></span> <span data-ttu-id="8f728-110">Die Auswahl in einer Dropdownliste ersetzt den freien Texteintrag und hilft, das Risiko und die Auswirkungen des menschlichen Versagens zu verringern.</span><span class="sxs-lookup"><span data-stu-id="8f728-110">Selection in a drop-down list replaces free text entry and helps reduce the risk and impact of human error.</span></span> <span data-ttu-id="8f728-111">Einstellungscodes werden verwendet, um eine Wellenschrittmethode in einer Wellenvorlage zu einer Zielvorlage für die Methode zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="8f728-111">Setup codes are used to link a wave step method in a wave template to a target template for the method.</span></span>

> [!NOTE]
> <span data-ttu-id="8f728-112">Die Verwendung der Wellenschrittcode-Funktion ist optional.</span><span class="sxs-lookup"><span data-stu-id="8f728-112">Use of the wave step codes feature is optional.</span></span> <span data-ttu-id="8f728-113">Sie ist organisationsweit für alle juristischen Personen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8f728-113">It is enabled organization-wide for all legal entities.</span></span>

## <a name="setup-demo"></a><span data-ttu-id="8f728-114">Demo einrichten</span><span class="sxs-lookup"><span data-stu-id="8f728-114">Setup demo</span></span> 

<span data-ttu-id="8f728-115">Für diese Vorführung müssen Demodaten eingerichtet werden, und Sie müssen das **USMF**-Demodatunternehmen verwenden.</span><span class="sxs-lookup"><span data-stu-id="8f728-115">For this demo, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="enable-wave-step-codes"></a><span data-ttu-id="8f728-116">Wellenschrittcodes aktivieren</span><span class="sxs-lookup"><span data-stu-id="8f728-116">Enable wave step codes</span></span>

<span data-ttu-id="8f728-117">Gehen Sie folgendermaßen vor, um die Wellenschritt-Codefunktion zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="8f728-117">Follow these steps to turn on the wave step codes feature.</span></span>

1. <span data-ttu-id="8f728-118">Navigieren Sie zu **Funktionsverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="8f728-118">Go to **Feature Management**.</span></span>
2. <span data-ttu-id="8f728-119">Wählen Sie diese Option aus, um die Funktion mit der Bezeichnung **Organisationsweiter Wellenschrittcode** zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="8f728-119">Select to enable the feature called **Organization-wide Wave Step Code**.</span></span>

<span data-ttu-id="8f728-120">Alle Freitexte des vorhandenen Wellenschritts in allen juristischen Personen werden in der neuen Struktur aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="8f728-120">All existing wave step free texts in all legal entities are upgraded to the new structure.</span></span> <span data-ttu-id="8f728-121">Nachdem dieses Upgrade für alle juristischen Personen abgeschlossen ist, wird die Funktion aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8f728-121">After this upgrade is completed for all legal entities, then the feature is enabled.</span></span> <span data-ttu-id="8f728-122">Wenn die Funktion für eine oder mehrere juristische Personen nicht aktiviert werden kann, ist die Funktion für keine juristische Person aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8f728-122">If the feature cannot be enabled for one or more legal entities, then the feature is not enabled for any legal entities.</span></span>

<span data-ttu-id="8f728-123">Während der Aktivierung werden Überprüfungen während der Datenaktualisierung durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="8f728-123">During the enablement, validations are done during the data upgrade.</span></span> <span data-ttu-id="8f728-124">Wenn das Upgrade fehlschlägt, erhalten Sie eine Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="8f728-124">If the upgrade fails, you receive an error message.</span></span> <span data-ttu-id="8f728-125">Eine Aktualisierung kann aufgrund der folgenden Konflikte fehlschlagen:</span><span class="sxs-lookup"><span data-stu-id="8f728-125">An upgrade might fail because of the following conflicts:</span></span>

- <span data-ttu-id="8f728-126">Es sind doppelte Freitexte des Wellenschritts vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8f728-126">Duplicate wave step free texts exist.</span></span>
- <span data-ttu-id="8f728-127">Es sind Anpassungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8f728-127">Customizations exist.</span></span>
- <span data-ttu-id="8f728-128">Ein Wellenschrittfreitext, der einer Wellenschritt-Methodeninstanz zugeordnet ist, entspricht nicht dem erwarteten Vorlagentyp.</span><span class="sxs-lookup"><span data-stu-id="8f728-128">A wave step free text that is associated with a wave step method instance doesn't match the expected template type.</span></span>

<span data-ttu-id="8f728-129">Nachdem Sie alle Konflikte behoben haben, die während der Überprüfung aufgetreten sind, können Sie erneut versuchen, die Funktion zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="8f728-129">After you've resolved any conflicts that are identified during the validations, you can retry to enable the feature.</span></span>

<span data-ttu-id="8f728-130">Wenn die Funktion aktiviert wurde, wird die Seite **Wellenschrittcodes** (**Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenschrittcodes**) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8f728-130">When the feature has been enabled, the **Wave step codes** page (**Warehouse management \> Setup \> Waves \> Wave step codes**) becomes available.</span></span> <span data-ttu-id="8f728-131">Auf dieser Seite werden die Wellenschrittcodes aufgelistet, die aktualisiert wurden, als die Funktion „Organisationsweiter Wellenschrittcode“ aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="8f728-131">This page lists the wave step codes that were upgraded when the Organization-wide Wave Step Code feature was enabled.</span></span>

### <a name="create-new-wave-step-codes"></a><span data-ttu-id="8f728-132">Erstellen neuer Wellenschrittcodes</span><span class="sxs-lookup"><span data-stu-id="8f728-132">Create new wave step codes</span></span>

<span data-ttu-id="8f728-133">Sie können die Seite **Wellenschrittcodes** verwenden, um Wellenschrittcodes zu erstellen und zu löschen.</span><span class="sxs-lookup"><span data-stu-id="8f728-133">You can use the **Wave step codes** page to create and delete wave step codes.</span></span>

<span data-ttu-id="8f728-134">Jeder neue Wellenschrittcode und die zugeordnete Kennung müssen für alle Wellenschritttypen eindeutig sein, und sie müssen für einen bestimmten Wellenschritttyp definiert werden.</span><span class="sxs-lookup"><span data-stu-id="8f728-134">Every new wave step code and its associated ID must be unique across all wave step types, and they must be defined for a specific wave step type.</span></span>

### <a name="apply-wave-step-codes"></a><span data-ttu-id="8f728-135">Wellenschrittcodes anwenden</span><span class="sxs-lookup"><span data-stu-id="8f728-135">Apply wave step codes</span></span>

<span data-ttu-id="8f728-136">Nachdem Sie die gewünschten Wellenschrittcodes definiert haben, können sie auf die Wellenprozessmethoden angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="8f728-136">After you've defined the appropriate wave step codes, they can be applied to the wave process methods.</span></span>

<span data-ttu-id="8f728-137">Um Wellenschrittcodes anzuwenden, wechseln zur entsprechenden Zielvorlage.</span><span class="sxs-lookup"><span data-stu-id="8f728-137">To apply wave step codes, go to the appropriate target template.</span></span> <span data-ttu-id="8f728-138">Hierbei gelten die Zielvorlagen, auf die die Wellenschrittcodes verweisen:</span><span class="sxs-lookup"><span data-stu-id="8f728-138">Here are the target templates that the wave step codes are designated to point to:</span></span>

- <span data-ttu-id="8f728-139">**Wiederbeschaffungsvorlagen:** Lagerortverwaltung \> Einstellungen \> Wiederbeschaffung \> Wiederbeschaffungsvorlagen</span><span class="sxs-lookup"><span data-stu-id="8f728-139">**Replenishment templates:** Warehouse management \> Setup \> Replenishment \> Replenishment templates</span></span>
- <span data-ttu-id="8f728-140">**Ladungserstellungsvorlagen:** Lagerortverwaltung \> Einstellungen \> Laden \> Ladungserstellungsvorlagen</span><span class="sxs-lookup"><span data-stu-id="8f728-140">**Load build templates:** Warehouse management \> Setup \> Load \> Load build templates</span></span>
- <span data-ttu-id="8f728-141">**Vorlagen sortieren:** Lagerortverwaltung \> Einstellungen \> Verpackung \> Ausgehende Sortierenvorlagen</span><span class="sxs-lookup"><span data-stu-id="8f728-141">**Sort templates:** Warehouse management \> Setup \> Packing \> Outbound sorting templates</span></span>
- <span data-ttu-id="8f728-142">**Containerisierungsvorlagen:** Lagerortverwaltung \> Einstellungen \> Container \> Containererstellungsvorlagen</span><span class="sxs-lookup"><span data-stu-id="8f728-142">**Containerization templates:** Warehouse management \> Setup \> Containers \> Container build templates</span></span>
- <span data-ttu-id="8f728-143">**Etikettendruckvorlagen:** Lagerortverwaltung \> Einstellungen \> Dokumentweiterleitung \> Wellenbeschriftungsvorlagen</span><span class="sxs-lookup"><span data-stu-id="8f728-143">**Label printing templates:** Warehouse management \> Setup \> Document routing \> Wave label templates</span></span>

<span data-ttu-id="8f728-144">Die Vorlagen in dieser Liste werden angewendet, wenn auf sie aus einer Wellenprozessmethode verwiesen wird, die in einer Wellenvorlage aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="8f728-144">The templates in this list are applied when they are referenced from a wave process method that is selected in a wave template.</span></span> <span data-ttu-id="8f728-145">Wenn der Wellenschrittcode auf einer Wellenprozessmethode in einer Wellenvorlage den Wellenschrittcode in einem der Vorlagentypen entspricht, wird die Vorlage angewendet.</span><span class="sxs-lookup"><span data-stu-id="8f728-145">When the wave step code on a wave process method in a wave template matches the wave step code in one of the templates types, the template is applied.</span></span>

### <a name="sample-scenario"></a><span data-ttu-id="8f728-146">Beispielszenario</span><span class="sxs-lookup"><span data-stu-id="8f728-146">Sample scenario</span></span>

<span data-ttu-id="8f728-147">Die folgenden Prozedurhilfen stellen sicher, dass die Wiederbeschaffungsvorlage, die Sie erstellt haben, auf die Wellenvorlage angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8f728-147">The following procedure helps guarantee that the replenishment template that you created will be applied for the wave template.</span></span>

1. <span data-ttu-id="8f728-148">Navigieren Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenschrittcodes**, und erstellen Sie einen Wellenschrittcode für den Typ **Wiederbeschaffung**.</span><span class="sxs-lookup"><span data-stu-id="8f728-148">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**, and create a wave step code for the **Replenishment** type.</span></span>
2. <span data-ttu-id="8f728-149">Navigieren Sie zu **Lagerortverwaltung \> Einstellungen \> Wiederbeschaffung \> Wiederbeschaffungsvorlagen**, und erstellen Sie eine Wiederbeschaffungsvorlage.</span><span class="sxs-lookup"><span data-stu-id="8f728-149">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**, and create a replenishment template.</span></span>
3. <span data-ttu-id="8f728-150">In der Wiederbeschaffungsvorlage wählen Sie den Wellenschrittcode aus, den Sie für die Art haben **Wiederbeschaffung**</span><span class="sxs-lookup"><span data-stu-id="8f728-150">In the replenishment template, select the wave step code that you created for the **Replenishment** type.</span></span>
4. <span data-ttu-id="8f728-151">Navigieren Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenvorlagen**, und wählen Sie die Wellenvorlage aus, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="8f728-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**, and select the wave template that you intend to use.</span></span>
5. <span data-ttu-id="8f728-152">In der Vorlage auf dem Inforegister **Methoden** wählen Sie die Methode **Wiederbeschaffung**.</span><span class="sxs-lookup"><span data-stu-id="8f728-152">In the template, on the **Methods** FastTab, select the **Replenishment** method.</span></span>
6. <span data-ttu-id="8f728-153">Im Feld **Wellenschrittcode** wählen Sie den Wellenschrittcode aus, den Sie für die Wiederbeschaffungsvorlage ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="8f728-153">In the **Wave step code** field, select the wave step code that you selected in the replenishment template.</span></span>

<span data-ttu-id="8f728-154">Sie führen diese Schritte für jede juristische Person aus.</span><span class="sxs-lookup"><span data-stu-id="8f728-154">You perform these steps for each legal entity.</span></span>
