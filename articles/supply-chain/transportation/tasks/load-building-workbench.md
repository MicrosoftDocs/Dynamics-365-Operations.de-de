---
title: Ladungserstellungsworkbench
description: In diesem Thema wird beschrieben, wie Sie mit der Ladungserstellungsworkbench arbeiten.
author: Henrikan
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSLoadBuildWorkbench,TMSLoadBuildTemplateCreate,TMSLoadBuildStrategy,TMSLoadBuildTemplateApply
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7b8633adbab43c95366d42cf409f5e508771c906
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809037"
---
# <a name="load-building-workbench"></a><span data-ttu-id="0dc57-103">Ladungserstellungsworkbench</span><span class="sxs-lookup"><span data-stu-id="0dc57-103">Load building workbench</span></span>

<span data-ttu-id="0dc57-104">Mit der Ladungserstellungsworkbench können Sie Ladungserstellungstrategien anwenden, wenn Sie Ladungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="0dc57-104">The load building workbench lets you apply load building strategies when you create loads.</span></span>

## <a name="create-a-load-building-strategy"></a><span data-ttu-id="0dc57-105">Erzeugen einer Ladungserstellungstrategie</span><span class="sxs-lookup"><span data-stu-id="0dc57-105">Create a load building strategy</span></span>

<span data-ttu-id="0dc57-106">Sie verwenden Ladungserstellungstrategien, um Ladungen automatisch zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0dc57-106">You use load building strategies to automatically build loads.</span></span> <span data-ttu-id="0dc57-107">Diese Funktionalität kann in den folgenden Situationen von Vorteil sein:</span><span class="sxs-lookup"><span data-stu-id="0dc57-107">This capability can be beneficial in the following situations:</span></span>

- <span data-ttu-id="0dc57-108">Wenn Sie regelmäßig eine bestimmte Anzahl von Produkten versenden, helfen Ladungserstellungstrategien, Zeit zu sparen, weil Sie nicht jedes Mal die gleiche Ladung aufbauen müssen.</span><span class="sxs-lookup"><span data-stu-id="0dc57-108">If you regularly ship a specific set of products, load strategies help save time, because you don't have to build the same load every time.</span></span>
- <span data-ttu-id="0dc57-109">Wenn Sie halbvolle Ladungen vermeiden wollen, um die Effizienz zu maximieren, können Ladestrategien helfen, jede Ladung so weit wie möglich zu füllen.</span><span class="sxs-lookup"><span data-stu-id="0dc57-109">If you want to avoid half-full loads to maximize efficiency, load strategies can help fill each load as much as possible.</span></span>

<span data-ttu-id="0dc57-110">Eine Ladungserstellungstrategieklasse mit dem Namen `TMSLoadBuildingVolumeStrategy` bietet eine Ladungserstellungstrategie mit dem Namen *Volumenbasierte Ladungserstellungstrategie*.</span><span class="sxs-lookup"><span data-stu-id="0dc57-110">A load building strategy class that is named `TMSLoadBuildingVolumeStrategy` provides a load building strategy that is named *Volume-based load building strategy*.</span></span> <span data-ttu-id="0dc57-111">Mit dieser Strategie können Sie die Höchstwerte verwenden, die für Höhe und Gewicht in der Ladungsvorlage angegeben sind, oder die Einstellungen überschreiben, indem sie neuen Werte eingeben.</span><span class="sxs-lookup"><span data-stu-id="0dc57-111">This strategy lets you use the maximum values that are specified for height and weight in the load template, or you can override the settings by entering new values.</span></span> <span data-ttu-id="0dc57-112">Diese Strategie ist die einzige Strategie, die von Haus aus enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="0dc57-112">This strategy is the only strategy that is included out of the box.</span></span> <span data-ttu-id="0dc57-113">(Möglicherweise haben Sie jedoch einige benutzerdefinierte Strategien.)</span><span class="sxs-lookup"><span data-stu-id="0dc57-113">(However, you might have some custom strategies.)</span></span>

<span data-ttu-id="0dc57-114">Um die Out-of-Box-Strategie *Volumenbasierte Ladungserstellung-Strategie* zu verwenden, wählen Sie sie im Feld **Ladungserstellung-Strategie** auf der Seite **Ladungserstellungsworkbench** (**Transportverwaltung &gt; Planung &gt; Ladungserstellungsworkbench**).</span><span class="sxs-lookup"><span data-stu-id="0dc57-114">To use the out-of-box *Volume-based load building strategy* strategy, select it in the **Load building strategy** field on the **Load building workbench** page (**Transportation management &gt; Planning &gt; Load building workbench**).</span></span>

<span data-ttu-id="0dc57-115">Gehen Sie folgendermaßen vor, um eine Strategie für die Ladungsaufnahme zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0dc57-115">To create a load building strategy, follow these steps.</span></span>

1. <span data-ttu-id="0dc57-116">Gehen Sie zu **Transportverwaltung &gt; Einrichten &gt; Ladungserstellung &gt; Ladungserstellung-Strategien**.</span><span class="sxs-lookup"><span data-stu-id="0dc57-116">Go to **Transportation management &gt; Setup &gt; Load building &gt; Load building strategies**.</span></span>
1. <span data-ttu-id="0dc57-117">Wählen Sie im Aktivitätsbereich **Klassenliste generieren**, um sicherzustellen, dass Sie die neuesten Versionen aller verfügbaren Klassen haben.</span><span class="sxs-lookup"><span data-stu-id="0dc57-117">On the Action Pane, select **Generate class list** to make sure that you have the latest versions of all available classes.</span></span>
1. <span data-ttu-id="0dc57-118">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="0dc57-118">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="0dc57-119">Geben Sie einen eindeutigen Namen für die Strategie ein, wählen Sie die Ladungserstellungstrategieklasse dafür aus und geben Sie eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="0dc57-119">Enter a unique name for the strategy, select the load building strategy class for it, and enter a description.</span></span>
1. <span data-ttu-id="0dc57-120">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="0dc57-120">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="0dc57-121">Wählen Sie im Aktivitätsbereich **Parameter** aus.</span><span class="sxs-lookup"><span data-stu-id="0dc57-121">On the Action Pane, select **Parameters**.</span></span>
1. <span data-ttu-id="0dc57-122">Wählen Sie auf der Seite **Ladungserstellungstrategie-Parameter** in der Liste **Volumenkapazität** und geben Sie dann in das Feld **Wert** den Prozentsatz der gesamten Volumenkapazität der Ladung ein, der für die neue Ladungserstellungstrategie angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0dc57-122">On the **Load building strategy parameters** page, select **Volume capacity** in the list, and then, in the **Value** field, enter the percentage of the load's total volume capacity that should be applied for the new load building strategy.</span></span>
1. <span data-ttu-id="0dc57-123">Wählen Sie **Gewichtskapazität** in der Liste und geben Sie dann in das Feld **Wert** den Prozentsatz der Gesamtgewichtskapazität der Ladung ein, der für die neue Ladungserstellungstrategie angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0dc57-123">Select **Weight capacity** in the list, and then, in the **Value** field, enter the percentage of the load's total weight capacity that should be applied for the new load building strategy.</span></span>
1. <span data-ttu-id="0dc57-124">Schließen Sie die Seite **Ladungserstellungstrategie-Parameter**.</span><span class="sxs-lookup"><span data-stu-id="0dc57-124">Close the **Load building strategy parameters** page.</span></span>
1. <span data-ttu-id="0dc57-125">Schließen Sie die Seite **Ladungserstellungstrategien**.</span><span class="sxs-lookup"><span data-stu-id="0dc57-125">Close the **Load building strategies** page.</span></span>

<span data-ttu-id="0dc57-126">Sie können die Ladungserstellungsstrategie nun einer Ladungserstellungsvorlage zuweisen.</span><span class="sxs-lookup"><span data-stu-id="0dc57-126">You can now assign the load building strategy to a load building template.</span></span> <span data-ttu-id="0dc57-127">Alternativ können Sie sie auch direkt in der Ladungserstellungsworkbench verwenden.</span><span class="sxs-lookup"><span data-stu-id="0dc57-127">Alternatively, you can use it directly in the load planning workbench.</span></span>

## <a name="use-a-load-building-strategy-in-the-load-building-workbench"></a><span data-ttu-id="0dc57-128">Verwenden einer Ladungserstellungstrategie in der Ladungserstellungsworkbench</span><span class="sxs-lookup"><span data-stu-id="0dc57-128">Use a load building strategy in the load building workbench</span></span>

1. <span data-ttu-id="0dc57-129">Gehen Sie zu **Transportverwaltung &gt; Planung &gt; Ladungserstellungsworkbench**.</span><span class="sxs-lookup"><span data-stu-id="0dc57-129">Go to **Transportation management &gt; Planning &gt; Load building workbench**.</span></span>
1. <span data-ttu-id="0dc57-130">Führen Sie einen dieser Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="0dc57-130">Follow one of these steps:</span></span>

    - <span data-ttu-id="0dc57-131">Wählen Sie eine Strategie im Feld **Ladungserstellungsstrategie**.</span><span class="sxs-lookup"><span data-stu-id="0dc57-131">Select a strategy in the **Load building strategy** field.</span></span>
    - <span data-ttu-id="0dc57-132">Wenn Sie eine Ladungserstellungvorlage definiert und ihr die Ladungserstellungstrategie zugewiesen haben, wählen Sie im Aktivitätsbereich auf der Registerkarte **Vorlagen verwalten** die Option **Vorlage anwenden**.</span><span class="sxs-lookup"><span data-stu-id="0dc57-132">If you've defined a load building template and assigned the load building strategy to it, on the Action Pane, on the **Manage templates** tab, select **Apply template**.</span></span> <span data-ttu-id="0dc57-133">Wählen Sie dann in der Dropdown-Dialogbox **Ladungserstellungsvorlage anwenden** eine Vorlage im Feld **Ladungserstellungsvorlagenname**.</span><span class="sxs-lookup"><span data-stu-id="0dc57-133">Then, in the **Apply load building template** drop-down dialog box, select a template in the **Load building template name** field.</span></span>

1. <span data-ttu-id="0dc57-134">Wählen Sie auf dem Inforegister **Vorlagen Sequenz laden** eine oder mehrere [Ladevorlagen](load-template.md).</span><span class="sxs-lookup"><span data-stu-id="0dc57-134">On the **Load templates sequence** FastTab, select one or more [load templates](load-template.md).</span></span> <span data-ttu-id="0dc57-135">Die Workbench wird versuchen, die Ladung in diese Arten von Containern einzupassen, und zwar in der hier angegebenen Sequenz.</span><span class="sxs-lookup"><span data-stu-id="0dc57-135">The workbench will try to fit the load into these types of containers, in the sequence that is specified here.</span></span> <span data-ttu-id="0dc57-136">Normalerweise sollten Sie die kleinsten Container an den Anfang der Liste einlagern, um sicherzustellen, dass der kleinstmögliche Container zuerst ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="0dc57-136">Typically, you should put the smallest containers at the top of the list to ensure that the smallest possible container is selected first.</span></span>
1. <span data-ttu-id="0dc57-137">Wählen Sie im Aktivitätsbereich **Ladungen vorschlagen**.</span><span class="sxs-lookup"><span data-stu-id="0dc57-137">On the Action Pane, select **Propose loads**.</span></span>
1. <span data-ttu-id="0dc57-138">Überprüfen Sie die vorgeschlagenen Ladungen und die vorgeschlagenen Zeilen.</span><span class="sxs-lookup"><span data-stu-id="0dc57-138">Review the proposed loads and proposed load lines.</span></span>
1. <span data-ttu-id="0dc57-139">Wählen Sie im Aktivitätsbereich **Ladungen erstellen**, um Ladungen zu erstellen, die auf den Zeilen des Quelldokuments im Inforegister **Vorgeschlagene Ladungszeilen** basieren.</span><span class="sxs-lookup"><span data-stu-id="0dc57-139">On the Action Pane, select **Create loads** to create loads that are based on the source document lines on the **Proposed load lines** FastTab.</span></span>
1. <span data-ttu-id="0dc57-140">Schließen Sie die Seite **Ladungserstellungsworkbench**.</span><span class="sxs-lookup"><span data-stu-id="0dc57-140">Close the **Load building workbench** page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]