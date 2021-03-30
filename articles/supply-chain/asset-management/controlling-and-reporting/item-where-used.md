---
title: Artikelverwendungsort
description: In diesem Thema erfahren Sie, wie Sie sich einen Überblick darüber verschaffen können, wo ein Artikel im Asset Management verwendet wird.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetItemWhereUsed, EntAssetItemWhereUsedCalculate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ef020c6a917f0a2c358f775991182e1e494d45d6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253757"
---
# <a name="item-where-used"></a><span data-ttu-id="c9ac8-103">Artikelverwendungsort</span><span class="sxs-lookup"><span data-stu-id="c9ac8-103">Item where used</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c9ac8-104">Sie können eine Kalkulation für einen bestimmten Artikel durchführen, um sich einen Überblick zu verschaffen, wo in Asset Management der Artikel verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c9ac8-104">You can make a calculation for a specific item to get an overview of where in Asset Management the item has been used.</span></span> <span data-ttu-id="c9ac8-105">Die Ergebnisse zeigen den Kontext, in dem der Artikel während seiner Lebensdauer verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c9ac8-105">The results show the context in which the item has been used during its lifetime.</span></span> <span data-ttu-id="c9ac8-106">Die Seite **Artikelverwendungsort** kann vom Anlagenmanagement-Hauptmenü geöffnet werden, ist auch über die folgenden Seiten zugänglich:</span><span class="sxs-lookup"><span data-stu-id="c9ac8-106">The **Item where used** page can be opened from the main Asset Management menu, and it can also be accessed from the following pages:</span></span>

- [<span data-ttu-id="c9ac8-107">Anlagenstücklisten</span><span class="sxs-lookup"><span data-stu-id="c9ac8-107">Asset BOMs</span></span>](../objects/object-BOM.md)

- [<span data-ttu-id="c9ac8-108">Ersatzteile in Anlagentypstandardeinstellungen</span><span class="sxs-lookup"><span data-stu-id="c9ac8-108">Spare parts on asset type defaults</span></span>](../setup-for-objects/object-types.md#spare-parts-on-the-asset-type-setup)

- [<span data-ttu-id="c9ac8-109">Kategorien von Wartungsaufträgen und Arten von Wartungsaufträgen, Variationen von Wartungsaufträgen, Handel von Wartungsaufträgen und Wartungsprüflisten</span><span class="sxs-lookup"><span data-stu-id="c9ac8-109">Maintenance job type categories and maintenance job types, maintenance job type variants, maintenance job trades, and maintenance checklists</span></span>](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

- [<span data-ttu-id="c9ac8-110">Wartungsprognose</span><span class="sxs-lookup"><span data-stu-id="c9ac8-110">Maintenance forecast</span></span>](../work-orders/maintenance-forecasts.md)

- [<span data-ttu-id="c9ac8-111">Beschaffung</span><span class="sxs-lookup"><span data-stu-id="c9ac8-111">Procurement</span></span>](../work-orders/procurement.md)

- [<span data-ttu-id="c9ac8-112">Arbeitsauftrag – Einkauf</span><span class="sxs-lookup"><span data-stu-id="c9ac8-112">Work order purchase</span></span>](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a><span data-ttu-id="c9ac8-113">Erstellen Sie eine Artikelverwendungsort-Berechnung</span><span class="sxs-lookup"><span data-stu-id="c9ac8-113">Make an item-where-used calculation</span></span>

1. <span data-ttu-id="c9ac8-114">Klicken Sie **Anlagenverwaltungsparameter** > **Abfragen** > **Artikelverwendungsort**, oder wählen Sie die Schaltfläche **Artikelverwendungsort** auf einer der Seiten aus, die oben genannten werden.</span><span class="sxs-lookup"><span data-stu-id="c9ac8-114">Click **Asset management** > **Inquiries** > **Item where used**, or select the **Item where used** button on one of the pages mentioned above.</span></span>

2. <span data-ttu-id="c9ac8-115">Im Dialogfeld **Artikelverwendungsort** wählen Sie den Artikel aus, für den Sie die Berechnung im Feld **Artikelnummer** vornehmen wollen.</span><span class="sxs-lookup"><span data-stu-id="c9ac8-115">In the **Item where used** dialog, select the item for which you want to make the calculation in the **Item number** field.</span></span>

3. <span data-ttu-id="c9ac8-116">Sie können das Feld **Ebene** verwenden, um anzugeben, wie detailliert die Artikelpositionen bezüglich funktionaler Standorte sein sollen.</span><span class="sxs-lookup"><span data-stu-id="c9ac8-116">You can use the **Level** field to indicate how detailed you want the item lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="c9ac8-117">Wenn Sie z.B. die Nummer „1“ in das Feld einfügen und eine funktionale Standortstruktur auf mehreren Ebenen haben, werden auf der obersten Ebene alle Artikelpositionen zu einem funktionalen Standort angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c9ac8-117">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all item lines for a functional location will be shown on the top level.</span></span> <span data-ttu-id="c9ac8-118">Daher kann die Relation/Menge auf einer Position von funktionalen Standorten auf einer niedrigeren Ebene summiert werden.</span><span class="sxs-lookup"><span data-stu-id="c9ac8-118">Therefore, relation/quantity on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="c9ac8-119">Wenn Sie die Zahl „0“ im Feld **Ebene** eingeben, wird ein detailliertes Ergebnis mit allen Artikelpositionen für alle funktionalen Standortebenen angezeigt, denen sie zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c9ac8-119">If you insert the number "0" in the **Level** field, you will see a detailed result showing all item lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="c9ac8-120">Wählen Sie im Abschnitt **Einbeziehen** „Ja“ auf den Umschaltflächen aus, die Sie in die Berechnung einbeziehen möchten.</span><span class="sxs-lookup"><span data-stu-id="c9ac8-120">In the **Include** section, select "Yes" on the toggle buttons that you want to include in the calculation.</span></span>

5. <span data-ttu-id="c9ac8-121">Klicken Sie auf **OK**, um die Berechnung zu starten.</span><span class="sxs-lookup"><span data-stu-id="c9ac8-121">Click **OK** to start the calculation.</span></span>

6. <span data-ttu-id="c9ac8-122">Wählen Sie auf der Registerkarte **Artikelverwendungsort** die **Gruppieren nach…**-Schaltflächen aus, um die erforderliche Detailebene der Berechnung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c9ac8-122">On the **Item where used** tab, select the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="c9ac8-123">Die ausgewählten **Gruppieren nach…**-Schaltflächen werden hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="c9ac8-123">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="c9ac8-124">Klicken Sie auf eine Schaltfläche, um sie zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="c9ac8-124">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="c9ac8-125">Wenn Sie die Dimensionen anzeigen möchten, die dem Artikel zugeordnet werden, klicken Sie auf **Dimensionen anzeigen** und wählen die Dimensionen aus, die angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c9ac8-125">If you want to show dimensions related to the item, click **Display dimensions**, and select the dimensions to be shown.</span></span>

## <a name="example"></a><span data-ttu-id="c9ac8-126">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c9ac8-126">Example</span></span>

<span data-ttu-id="c9ac8-127">Im nachfolgenden Screenshot finden Sie ein Beispiel für eine Artikelverwendungsort-Berechnung für Artikelnummer „1000“.</span><span class="sxs-lookup"><span data-stu-id="c9ac8-127">In the screenshot below, you see an example of an item-where-used calculation for item number "1000".</span></span>

![Beispiel einer Artikelverwendungsort-Berechnung](media/12-controlling-and-reporting.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]