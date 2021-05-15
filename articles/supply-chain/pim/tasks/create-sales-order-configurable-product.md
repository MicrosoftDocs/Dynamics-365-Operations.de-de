---
title: Auftrag für ein konfigurierbares Produkt erstellen
description: Dieses Verfahren zeigt, wie die Konfigurationsvorlage für das Produkt auf einem Auftrag angewendet wird.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8607de5705354aa58c985fb536f3e1d52acd1f37
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921288"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="2009a-103">Auftrag für ein konfigurierbares Produkt erstellen</span><span class="sxs-lookup"><span data-stu-id="2009a-103">Create a sales order for a configurable product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2009a-104">Dieses Verfahren zeigt, wie die Konfigurationsvorlage für das Produkt auf einem Auftrag angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="2009a-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="2009a-105">Dieses Beispiel verwendet das Lausprechermodell D0006 im Demodatenunternehmen USMF.</span><span class="sxs-lookup"><span data-stu-id="2009a-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="2009a-106">Diese Aufgaben werden normalerweise von einem Auftragsbearbeiter ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2009a-106">Typically, a sales order processor uses this procedure.</span></span>

## <a name="create-a-sales-order"></a><span data-ttu-id="2009a-107">Auftrag erstellen</span><span class="sxs-lookup"><span data-stu-id="2009a-107">Create a sales order</span></span>

1. <span data-ttu-id="2009a-108">Gehen Sie zu **Vertrieb und Marketing \> Arbeitsbereiche \> Verkaufsauftragsverarbeitung und Abfrage**.</span><span class="sxs-lookup"><span data-stu-id="2009a-108">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="2009a-109">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="2009a-109">Select **New**.</span></span>
1. <span data-ttu-id="2009a-110">**Auftrag** auswählen.</span><span class="sxs-lookup"><span data-stu-id="2009a-110">Select **Sales order**.</span></span>
1. <span data-ttu-id="2009a-111">Wählen Sie im Feld **Kundenkonto** die Option *US-001* aus.</span><span class="sxs-lookup"><span data-stu-id="2009a-111">In the **Customer account** field, select *US-001*.</span></span> 
1. <span data-ttu-id="2009a-112">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="2009a-112">Select **OK**.</span></span>
1. <span data-ttu-id="2009a-113">Wählen Sie im Feld *Artikelnummer* die Option **D0006** aus.</span><span class="sxs-lookup"><span data-stu-id="2009a-113">In the **Item number** field, select *D0006*.</span></span>
    * <span data-ttu-id="2009a-114">Für diese Aufgabe müssen Sie ein konfigurierbares Produkt auswählen.</span><span class="sxs-lookup"><span data-stu-id="2009a-114">For this task, you must select a configurable product.</span></span>  
1. <span data-ttu-id="2009a-115">Wählen Sie **Produkt und Lieferung**.</span><span class="sxs-lookup"><span data-stu-id="2009a-115">Select **Product and supply**.</span></span>
1. <span data-ttu-id="2009a-116">Wählen Sie **Zeile konfigurieren**.</span><span class="sxs-lookup"><span data-stu-id="2009a-116">Select **Configure line**.</span></span>
    * <span data-ttu-id="2009a-117">Beachten Sie, dass sich der Preis basierend auf der gewählten Konfiguration geändert hat und dass das Feld **Website bearbeiten** jetzt auf *Wahr* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2009a-117">Note that the price has changed, based on the configuration that was selected, and that the **Include cable** field is now set to *True*.</span></span>  
    * <span data-ttu-id="2009a-118">Beachten Sie den Standardpreis und die Einstellungen, die für das Kabel ausgewählt sind.</span><span class="sxs-lookup"><span data-stu-id="2009a-118">Note the default price and the settings that are selected for the cable.</span></span>  
1. <span data-ttu-id="2009a-119">Wählen Sie **Vorlage laden**.</span><span class="sxs-lookup"><span data-stu-id="2009a-119">Select **Load template**.</span></span>
    * <span data-ttu-id="2009a-120">Dieses Beispiel verdeutlicht, wie Sie eine Vorlage verwenden können, um eine vordefinierte Konfiguration auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="2009a-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="2009a-121">Wenn Sie diese Vorgehensweise als Anleitung verwenden und die anderen verfügbaren Attributwerte sehen wollen, müssen Sie die Schaltfläche **Entsperren** wählen.</span><span class="sxs-lookup"><span data-stu-id="2009a-121">If you're using this procedure as a task guide and want to see the other attribute values that are available, you must select the **Unlock** button.</span></span>  
1. <span data-ttu-id="2009a-122">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="2009a-122">Select **OK**.</span></span>
1. <span data-ttu-id="2009a-123">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="2009a-123">Select **OK**.</span></span>
1. <span data-ttu-id="2009a-124">Erweitern Sie den Abschnitt **Positionsdetails**.</span><span class="sxs-lookup"><span data-stu-id="2009a-124">Expand the **Line details** section.</span></span>
1. <span data-ttu-id="2009a-125">Wählen Sie die Registerkarte **Produkt**.</span><span class="sxs-lookup"><span data-stu-id="2009a-125">Select the **Product** tab.</span></span>
    * <span data-ttu-id="2009a-126">Die Konfiguration des Artikels wird jetzt unter Produktdimensionen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2009a-126">The configuration of the item is now listed under the product dimensions.</span></span>  
1. <span data-ttu-id="2009a-127">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="2009a-127">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]