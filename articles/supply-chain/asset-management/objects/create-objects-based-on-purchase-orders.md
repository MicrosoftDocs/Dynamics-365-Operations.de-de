---
title: BestellungErstellen von Anlagen basierend auf den Bestellungen
description: In diesem Thema wird erläutert, wie Sie eine Liste von Anlageposten erstellen können, die als Grundlage für die Erstellung von Anlagen für Wartungsaufträge im Asset-Management verwendet werden können.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectItem, EntAssetPendingAssets
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 97b40528db4acc2627b087e8ee90bfd1fd79efa7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253277"
---
# <a name="create-assets-based-on-purchase-orders"></a><span data-ttu-id="9e2ba-103">BestellungErstellen von Anlagen basierend auf den Bestellungen</span><span class="sxs-lookup"><span data-stu-id="9e2ba-103">Create assets based on purchase orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="9e2ba-104">In diesem Thema wird erläutert, wie Sie eine Liste von Anlageposten erstellen können, die als Grundlage für die Erstellung von Anlagen für Wartungsaufträge im Asset-Management verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-104">This topic explains how you can create a list of asset items that can be used as a basis for creating assets for maintenance jobs in Asset Management.</span></span> <span data-ttu-id="9e2ba-105">Basierend auf Anlageartikeln können Sie eine Liste der Bestellungen anzeigen, die für diesen Artikel erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-105">Based on the asset items, you are able to view a list of the purchase order lines that have been created on those items.</span></span> <span data-ttu-id="9e2ba-106">Der Zweck dieser Funktion ist es, einfach eine Anlage im Asset-Management basierend auf einer Bestellung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-106">The purpose of this functionality is to easily create an asset in Asset Management based on a purchase order.</span></span>

<span data-ttu-id="9e2ba-107">Zuerst richten Sie Artikel ein, die für das Erstellen von Anlagen für eine Bestellung in **Anlageartikel** verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-107">First, you set up the items to be used for creating assets from a purchase order in **Asset items**.</span></span> <span data-ttu-id="9e2ba-108">Nachdem Sie einer Bestellposition erstellt haben, erstellen Sie die Anlage unter **Pendente Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-108">After creating a purchase order line, you create the assets in **Pending assets**.</span></span> <span data-ttu-id="9e2ba-109">Es ist möglihc zu entscheid, in welcher Phase der Bestellung die Anlage erstellt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-109">It is possible to decide at which stage of the purchase order the asset should be created.</span></span>


## <a name="select-asset-items"></a><span data-ttu-id="9e2ba-110">Anlageartikel auswählen</span><span class="sxs-lookup"><span data-stu-id="9e2ba-110">Select asset items</span></span>

1. <span data-ttu-id="9e2ba-111">Klicken Sie auf **Anlagt-Management** > **Einstellungen** > **Anlagen** > **Artikel**.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-111">Click **Asset management** > **Setup** > **Assets** > **Items**.</span></span>
2. <span data-ttu-id="9e2ba-112">Klicken Sie auf **Neu**, um einen neuen Anlageartikel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-112">Click **New** to create a new asset item.</span></span>
3. <span data-ttu-id="9e2ba-113">Wählen Sie im Feld **Artikelnummer** einen Artikel aus.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-113">Select the item in the **Item number** field.</span></span> <span data-ttu-id="9e2ba-114">Wenn Sie dieses Feld leer lassen, wird der Name automatisch im Feld **Produktname** eingefügt.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-114">When you leave that field, the item name is automatically inserted in the **Product name** field.</span></span>
4. <span data-ttu-id="9e2ba-115">Auf dem Inforegister **Allgemeines** wählen Sie einen Anlagentyp für den Artikel aus.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-115">On the **General** FastTab, select an asset type for the item.</span></span>
5. <span data-ttu-id="9e2ba-116">Wählen Sie Anlagenhersteller und -Modell für den Artikel aus.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-116">Select asset manufacturer and model for the item.</span></span>
6. <span data-ttu-id="9e2ba-117">Speichert den Artikel.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-117">Save the item.</span></span>


## <a name="create-assets-from-pending-assets"></a><span data-ttu-id="9e2ba-118">Anlagen erstellen aus den ausstehenden Anlagen</span><span class="sxs-lookup"><span data-stu-id="9e2ba-118">Create assets from pending assets</span></span>

1. <span data-ttu-id="9e2ba-119">Klicken Sie auf **Anlage-Management** > **Gemeinsam** > **Anlagen** > **Ausstehende Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-119">Click **Asset management** > **Common** > **Assets** > **Pending Assets**.</span></span>
2. <span data-ttu-id="9e2ba-120">Sie finden eine aktualisierte Liste der Bestellungen auf der Grundlage der Artikel, die unter **Anlageartikel** ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-120">You will see an updated list of the purchase orders based on the items selected in **Asset items**.</span></span>
3. <span data-ttu-id="9e2ba-121">Sie können den Status von Bestellungen filtern, um auszuwählen, in welchem Lebenszyklusstatus die Anlage erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-121">You can filter the status of purchase orders to select at which lifecycle state the asset should be created.</span></span> <span data-ttu-id="9e2ba-122">Beispielsweise sollten Sie nur Anlagen erstellen, wenn ein Produktzugang für eine Bestellung gebucht wurde.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-122">For example, you may only want to create assets when a product receipt has been posted on a purchase order.</span></span>
4. <span data-ttu-id="9e2ba-123">Wählen Sie den Link **Referenznummer** auf einer Bestellposition aus, um die detaillierte Informationen zum Artikel anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-123">Select the **Reference number** link on a purchase order line to view detailed information about the item.</span></span>
5. <span data-ttu-id="9e2ba-124">Wenn Sie bearbeiten möchten, welche Dimensionen auf dem Inforegister **Bestanddimensionen** angezeigt werden, klicken Sie auf die Schaltfläche **Anzeigen-Dimensionen**, und treffen Sie Ihre Auswahl.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-124">If you want to edit which dimensions are displayed on the **Inventory dimensions** FastTab, click the **Display Dimensions** button, and make your selections.</span></span>
6. <span data-ttu-id="9e2ba-125">Wenn Sie eine Anlage basierend  auf einer Bestellposition erstellen möchten, aktivieren Sie das Kontrollkästchen in der Spalte **Markieren** für diese Position auf der Listenseite aus, und klicken Sie **Anlagen erstellen**.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-125">If you want to create an asset based on a purchase order line, select the check box in the **Mark** column for that line on the list page, and click **Create assets**.</span></span> <span data-ttu-id="9e2ba-126">Eine Meldung wird angezeigt, die Sie über die Anlage-Kennung informiert.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-126">A message will be displayed informing you of the asset ID.</span></span>
7. <span data-ttu-id="9e2ba-127">Wählen Sie die Anlage in der Liste **Alle Anlagen** aus und klicken **Bearbeiten**, um weitere Informationen zur Anlage hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-127">Select the asset in the **All assets** list and click **Edit** to add more information to the asset.</span></span>
8. <span data-ttu-id="9e2ba-128">Unter **Ausstehende Anlagen** wenn Sie eine Position löschen möchten, da Sie keine Anlage erstellen möchten, wählen Sie das Kontrollkästchen in der Spalte **Markieren** für diese Position und klicken Sie **Ausstehende Anlage ignorieren**.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-128">In **Pending assets**, if you want to delete a line because you don't want to create an asset, select the check box in the **Mark** column for that line, and click **Discard pending assets**.</span></span> <span data-ttu-id="9e2ba-129">Eine Meldung wird angezeigt, die Sie über die Anlage-Kennung informiert.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-129">A message will be displayed informing you of the asset ID.</span></span> <span data-ttu-id="9e2ba-130">Löschen Sie nicht die Bestellung bzw. den Auftrag, nur den Datensatz, von dem Sie die Anlage in **Anlage-Management** erstellt haben könnten.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-130">You are not deleting the purchase order or sales order, just the record from which you could have created an asset in **Asset Management**.</span></span>

>[!NOTE]
><span data-ttu-id="9e2ba-131">Alle Produktdimensionen (Größe, Farbe, Konfigurationsusw.) werden automatisch in die Anlagenattribute übertragen.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-131">All product dimensions (size, color, configuration etc.) are automatically transferred to the asset attributes.</span></span> <span data-ttu-id="9e2ba-132">Rückverfolgungsdimensionen (Seriennummer) werden direkt für die Anlage aufbewahrt, wenn die Anlage erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-132">Tracking dimensions (serial number) are stored directly on the asset when the asset is created.</span></span>


## <a name="find-pending-assets"></a><span data-ttu-id="9e2ba-133">Suchen Sie ausstehende Anlagen</span><span class="sxs-lookup"><span data-stu-id="9e2ba-133">Find pending assets</span></span>

<span data-ttu-id="9e2ba-134">Sie können **Ausstehende Anlagenanzahl** ausführen, um ausstehende Anlagen zu prüfen.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-134">You can run a **Pending asset count** to check for pending assets.</span></span> <span data-ttu-id="9e2ba-135">Beispielsweise kann diese Funktion zum Empfangen einer Benachrichtigung verwendet werden, wenn eine der Anlage fertig ist, als Anlage erstellt zu werden.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-135">For example, this function can be used for receiving a notification each time a pending asset is ready to be created as an asset.</span></span>

1. <span data-ttu-id="9e2ba-136">Klicken Sie auf **Anlage-Management** > **Gemeinsam** > **Anlagen** > **Ausstehende Anlagenzählung**.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-136">Click **Asset management** > **Periodic** > **Assets** > **Pending asset count**.</span></span>
2. <span data-ttu-id="9e2ba-137">Klicken Sie **OK**, um den Einzelvorgang zu aktivieren und die Liste in **Ausstehende Anlagen** zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-137">Click **OK** to run the job and update the list in **Pending assets**.</span></span>
3. <span data-ttu-id="9e2ba-138">Sie können diesen Einzelvorgang als Batchauftrag einrichten, so dass er beispielsweise einmal pro Tag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-138">You can set up this job to run as a batch job, for example, once each day.</span></span>

<span data-ttu-id="9e2ba-139">**Vorsicht:**, Wenn Daten in einer Bestellung geändert werden, *nachdem* Sie eine Anlage auf Basis des dazu gehörenden Artikels erstellt haben, werden diese Änderungen nicht in der Anlage angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9e2ba-139">**Caution:** If data is changed on a purchase order *after* you have created an asset based on the appertaining item, those changes will not be reflected on the asset.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]