---
title: Festlegen verschiedener Dimensionen für Verpackung und Lagerung
description: In diesem Thema wird gezeigt, wie Sie angeben, für welchen Prozess (Verpackung, Lagerung oder verschachtelte Verpackung) jede angegebene Dimension verwendet wird.
author: mirzaab
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResPhysicalProductDimensions, WHSPhysDimUOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: e997f8bccde7856303d8b3c6407143598ccc6030
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818919"
---
# <a name="set-different-dimensions-for-packing-and-storage"></a><span data-ttu-id="12fad-103">Festlegen verschiedener Dimensionen für Verpackung und Lagerung</span><span class="sxs-lookup"><span data-stu-id="12fad-103">Set different dimensions for packing and storage</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="12fad-104">Einige Artikel werden so verpackt oder gelagert, dass Sie möglicherweise die physischen Dimensionen für jeden von mehreren verschiedenen Prozessen unterschiedlich nachverfolgen müssen.</span><span class="sxs-lookup"><span data-stu-id="12fad-104">Some items are packed or stored in such a way that you may need to track physical dimensions differently for each of several different processes.</span></span> <span data-ttu-id="12fad-105">Die Funktion *Produktdimensionen für Verpackung* ermöglicht für jedes Produkt das Einrichten einer oder mehrerer Arten von Dimensionen.</span><span class="sxs-lookup"><span data-stu-id="12fad-105">The *Packaging product dimensions* feature lets you set up one or several types of dimensions for each product.</span></span> <span data-ttu-id="12fad-106">Jede Dimensionsart bietet eine Reihe physikalischer Messwerte (Gewicht, Breite, Tiefe und Höhe) und legt den Prozess fest, bei dem diese physikalischen Messwerte gelten.</span><span class="sxs-lookup"><span data-stu-id="12fad-106">Each dimension type provides a set of physical measurements (weight, width, depth, and height), and establishes the process where those physical measurement values apply.</span></span> <span data-ttu-id="12fad-107">Wenn diese Funktion aktiviert ist, unterstützt Ihr System die folgenden Arten von Dimensionen:</span><span class="sxs-lookup"><span data-stu-id="12fad-107">When this feature is enabled, your system will support the following types of dimensions:</span></span>

- <span data-ttu-id="12fad-108">*Lagerung* – Die Lagerdimensionen werden zusammen mit Volumenmetriken für den Lagerplatz verwendet, um zu bestimmen, wie viele Artikel an verschiedenen Lagerort-Lagerplätzen gelagert werden können.</span><span class="sxs-lookup"><span data-stu-id="12fad-108">*Storage* - Storage dimensions are used along with location volumetrics to determine how many of each item can be stored in various warehouse locations.</span></span>
- <span data-ttu-id="12fad-109">*Verpackung* – Die Verpackungsdimensionen werden während der Containerisierung und des manuellen Verpackungsprozesses verwendet, um zu bestimmen, welche Stückzahl eines jeden Artikels in verschiedene Containertypen passt.</span><span class="sxs-lookup"><span data-stu-id="12fad-109">*Packing* - Packing dimensions are used during containerization and the manual packing process to determine how many of each item will fit in various container types.</span></span>
- <span data-ttu-id="12fad-110">*Verschachtelte Verpackung* – Dimensionen für die verschachtelte Verpackung werden verwendet, wenn der Verpackungsprozess mehrere Ebenen umfasst.</span><span class="sxs-lookup"><span data-stu-id="12fad-110">*Nested packing* - Nested packing dimensions are used when the packing process contains multiple levels.</span></span>

<span data-ttu-id="12fad-111">*Lagerdimensionen* werden auch dann unterstützt, wenn die Funktion *Produktdimensionen für Verpackung* nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="12fad-111">*Storage* dimensions are supported even when the *Packaging product dimensions* feature isn't enabled.</span></span> <span data-ttu-id="12fad-112">Sie richten sie über die Seite **Physische Dimensionen** in Supply Chain Management ein.</span><span class="sxs-lookup"><span data-stu-id="12fad-112">You set these up using the **Physical dimension** page in Supply Chain Management.</span></span> <span data-ttu-id="12fad-113">Diese Dimensionen werden von allen Prozessen verwendet, bei denen die Dimensionen Verpackung und verschachtelte Verpackung nicht angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="12fad-113">These dimensions are used by all processes where the packing and nested packing dimensions aren't specified.</span></span>

<span data-ttu-id="12fad-114">Die Dimensionen *Verpackung* und *Verschachtelte Verpackung* werden über die Seite **Physische Produktdimensionen** eingerichtet, die hinzugefügt wird, wenn Sie die Funktion *Produktdimensionen für Verpackung* aktivieren.</span><span class="sxs-lookup"><span data-stu-id="12fad-114">*Packing* and *nested packing* dimensions are set up using the **Physical product dimensions** page, which is added when you enable the *Packaging product dimensions* feature.</span></span>
<span data-ttu-id="12fad-115">Dieses Thema enthält ein Szenario, das die Verwendung dieser Funktion veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="12fad-115">This topic provides a scenario that illustrates how to use this feature.</span></span>

## <a name="turn-on-the-packaging-product-dimensions-feature"></a><span data-ttu-id="12fad-116">Aktivieren der Funktion für Produktdimensionen für die Verpackung</span><span class="sxs-lookup"><span data-stu-id="12fad-116">Turn on the packaging product dimensions feature</span></span>

<span data-ttu-id="12fad-117">Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="12fad-117">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="12fad-118">Administratoren können mit der Einstellung [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und ggf. aktivieren.</span><span class="sxs-lookup"><span data-stu-id="12fad-118">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="12fad-119">Dort wird die Funktion folgendermaßen aufgelistet:</span><span class="sxs-lookup"><span data-stu-id="12fad-119">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="12fad-120">**Module:** *Lagerortverwaltung*</span><span class="sxs-lookup"><span data-stu-id="12fad-120">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="12fad-121">**Funktionsname:** *Produktdimensionen für Verpackung*</span><span class="sxs-lookup"><span data-stu-id="12fad-121">**Feature name:** *Packaging product dimensions*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="12fad-122">Beispielszenario</span><span class="sxs-lookup"><span data-stu-id="12fad-122">Example scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="12fad-123">Szenario einrichten</span><span class="sxs-lookup"><span data-stu-id="12fad-123">Set up the scenario</span></span>

<span data-ttu-id="12fad-124">Bevor Sie das Beispielszenario ausführen können, müssen Sie Ihr System wie in diesem Abschnitt beschrieben vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="12fad-124">Before you can run the example scenario, you must prepare your system as described in this section.</span></span>

#### <a name="enable-demo-data"></a><span data-ttu-id="12fad-125">Aktivieren der Demodaten</span><span class="sxs-lookup"><span data-stu-id="12fad-125">Enable demo data</span></span>

<span data-ttu-id="12fad-126">Um dieses Szenario mit den hier angegebenen Demodatensätzen und -werten durchzuarbeiten, müssen Sie ein System verwenden, auf dem die standardmäßigen [Demodaten](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) installiert sind.</span><span class="sxs-lookup"><span data-stu-id="12fad-126">To work through this scenario using the demo records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="12fad-127">Außerdem müssen Sie die *USMF* juristische Person auswählen, bevor Sie beginnen.</span><span class="sxs-lookup"><span data-stu-id="12fad-127">Additionally, you must select the *USMF* legal entity before you begin.</span></span>

#### <a name="add-a-new-physical-dimension-to-a-product"></a><span data-ttu-id="12fad-128">Hinzufügen einer neuen physischen Dimension zu einem Produkt</span><span class="sxs-lookup"><span data-stu-id="12fad-128">Add a new physical dimension to a product</span></span>

<span data-ttu-id="12fad-129">Fügen Sie eine neue physische Dimension für ein Produkt hinzu, indem Sie folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="12fad-129">Add a new physical dimension for a product by doing the following:</span></span>

1. <span data-ttu-id="12fad-130">Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="12fad-130">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="12fad-131">Wählen Sie das Produkt mit der **Artikelnummer** *A0001* aus.</span><span class="sxs-lookup"><span data-stu-id="12fad-131">Select the product with **Item number** *A0001*.</span></span>
1. <span data-ttu-id="12fad-132">Öffnen Sie im Aktionsbereich die Registerkarte **Bestand verwalten** und wählen Sie in der Gruppe **Lagerort** die Option **Physische Produktdimensionen** aus.</span><span class="sxs-lookup"><span data-stu-id="12fad-132">On the Action Pane, open the **Manage inventory** tab and, from the **Warehouse** group, select **Physical product dimensions**.</span></span>
1. <span data-ttu-id="12fad-133">Die Seite **Physische Produktdimensionen** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="12fad-133">The **Physical product dimensions** page opens.</span></span> <span data-ttu-id="12fad-134">Wählen Sie im Aktionsbereich **Neu** aus, um dem Raster eine neue Dimension mit folgenden Einstellungen hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="12fad-134">On the Action Pane, select **New** to add a new dimension to the grid with the following settings:</span></span>
    - <span data-ttu-id="12fad-135">**Art der physischen Dimension** - *Verpackung*</span><span class="sxs-lookup"><span data-stu-id="12fad-135">**Physical dimension type** - *Packing*</span></span>
    - <span data-ttu-id="12fad-136">**Physische Einheit** - *Stk.*</span><span class="sxs-lookup"><span data-stu-id="12fad-136">**Physical unit** - *pcs*</span></span>
    - <span data-ttu-id="12fad-137">**Gewicht** - *4*</span><span class="sxs-lookup"><span data-stu-id="12fad-137">**Weight** - *4*</span></span>
    - <span data-ttu-id="12fad-138">**Gewichtseinheit** - *kg*</span><span class="sxs-lookup"><span data-stu-id="12fad-138">**Weight unit** - *kg*</span></span>
    - <span data-ttu-id="12fad-139">**Tiefe** - *3*</span><span class="sxs-lookup"><span data-stu-id="12fad-139">**Depth** - *3*</span></span>
    - <span data-ttu-id="12fad-140">**Höhe** - *4*</span><span class="sxs-lookup"><span data-stu-id="12fad-140">**Height** - *4*</span></span>
    - <span data-ttu-id="12fad-141">**Breite** - *3*</span><span class="sxs-lookup"><span data-stu-id="12fad-141">**Width** - *3*</span></span>
    - <span data-ttu-id="12fad-142">**Länge** - *cm*</span><span class="sxs-lookup"><span data-stu-id="12fad-142">**Length** - *cm*</span></span>
    - <span data-ttu-id="12fad-143">**Volumeneinheit** - *cm3*</span><span class="sxs-lookup"><span data-stu-id="12fad-143">**Volume unit** - *cm3*</span></span>

<span data-ttu-id="12fad-144">Der Wert im Feld **Volumen** wird automatisch basierend auf Ihren Einstellungen für **Tiefe**, **Höhe** und **Breite** berechnet.</span><span class="sxs-lookup"><span data-stu-id="12fad-144">The **Volume** field is automatically calculated based on your **Depth**, **Height**, and **Width** settings.</span></span>

#### <a name="create-a-new-container-type"></a><span data-ttu-id="12fad-145">Einen neuen Containertyp erstellen</span><span class="sxs-lookup"><span data-stu-id="12fad-145">Create a new container type</span></span>

<span data-ttu-id="12fad-146">Wechseln Sie zu **Lagerortverwaltung \> Einrichten \> Container \> Containertypen** und erstellen Sie einen neuen Datensatz mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="12fad-146">Go to **Warehouse management \> Setup \> Containers \> Container types** and create a new record with the following settings:</span></span>

- <span data-ttu-id="12fad-147">**Containertypcode** - *Kurzer Karton*</span><span class="sxs-lookup"><span data-stu-id="12fad-147">**Container type code** - *Short Box*</span></span>
- <span data-ttu-id="12fad-148">**Beschreibung** - *Kurzer Karton*</span><span class="sxs-lookup"><span data-stu-id="12fad-148">**Description** - *Short Box*</span></span>
- <span data-ttu-id="12fad-149">**Maximales Nettogewicht** - *50*</span><span class="sxs-lookup"><span data-stu-id="12fad-149">**Maximum net weight** - *50*</span></span>
- <span data-ttu-id="12fad-150">**Volumen** - *144*</span><span class="sxs-lookup"><span data-stu-id="12fad-150">**Volume** - *144*</span></span>
- <span data-ttu-id="12fad-151">**Länge** - *6*</span><span class="sxs-lookup"><span data-stu-id="12fad-151">**Length** - *6*</span></span>
- <span data-ttu-id="12fad-152">**Breite** - *6*</span><span class="sxs-lookup"><span data-stu-id="12fad-152">**Width** - *6*</span></span>
- <span data-ttu-id="12fad-153">**Höhe** - *4*</span><span class="sxs-lookup"><span data-stu-id="12fad-153">**Height** - *4*</span></span>

#### <a name="create-a-container-group"></a><span data-ttu-id="12fad-154">Erstellen einer Containergruppe</span><span class="sxs-lookup"><span data-stu-id="12fad-154">Create a container group</span></span>

<span data-ttu-id="12fad-155">Wechseln Sie zu **Lagerortverwaltung \> Einrichten \> Container \> Containergruppen** und erstellen Sie einen neuen Datensatz mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="12fad-155">Go to **Warehouse management \> Setup \> Containers \> Container groups** and create a new record with the following settings:</span></span>

- <span data-ttu-id="12fad-156">**Containergruppenkennung** - *Kurzer Karton*</span><span class="sxs-lookup"><span data-stu-id="12fad-156">**Container group ID** - *Short Box*</span></span>
- <span data-ttu-id="12fad-157">**Beschreibung** - *Kurzer Karton*</span><span class="sxs-lookup"><span data-stu-id="12fad-157">**Description** - *Short Box*</span></span>

<span data-ttu-id="12fad-158">Fügen Sie eine neue Position zum Abschnitt **Details** hinzu.</span><span class="sxs-lookup"><span data-stu-id="12fad-158">Add a new line to the **Details** section.</span></span> <span data-ttu-id="12fad-159">Legen Sie den **Containertyp** auf *Kurzer Karton* fest.</span><span class="sxs-lookup"><span data-stu-id="12fad-159">Set the **Container type** to *Short Box*.</span></span>

#### <a name="set-up-a-container-build-template"></a><span data-ttu-id="12fad-160">Eine Containererstellungsvorlage einrichten</span><span class="sxs-lookup"><span data-stu-id="12fad-160">Set up a container build template</span></span>

<span data-ttu-id="12fad-161">Wechseln Sie zu **Lagerortverwaltung \> Einrichten \> Container \> Containererstellungsvorlagen** und wählen Sie **Kartons** aus.</span><span class="sxs-lookup"><span data-stu-id="12fad-161">Go to **Warehouse management \> Setup \> Containers \> Container build templates** and select **Boxes**.</span></span> <span data-ttu-id="12fad-162">Ändern Sie den Wert von **Containergruppenkennung** zu *Kurzer Karton*.</span><span class="sxs-lookup"><span data-stu-id="12fad-162">Change the **Container group ID** to *Short Box*.</span></span>

### <a name="run-the-scenario"></a><span data-ttu-id="12fad-163">Ausführen des Szenarios</span><span class="sxs-lookup"><span data-stu-id="12fad-163">Run the scenario</span></span>

<span data-ttu-id="12fad-164">Nachdem Sie Ihr System wie im vorherigen Abschnitt beschrieben vorbereitet haben, können Sie das Szenario wie im nächsten Abschnitt beschrieben ausführen.</span><span class="sxs-lookup"><span data-stu-id="12fad-164">After you have prepared your system as described in the previous section, you are ready to run the scenario as described in the next section.</span></span>

#### <a name="create-a-sales-order-and-create-a-shipment"></a><span data-ttu-id="12fad-165">Erstellen eines Auftrags und einer Lieferung</span><span class="sxs-lookup"><span data-stu-id="12fad-165">Create a sales order and create a shipment</span></span>

<span data-ttu-id="12fad-166">In diesem Prozess erstellen Sie eine Lieferung basierend auf der Artikeldimension *Verpackung*, für die die Höhe weniger als 3 beträgt.</span><span class="sxs-lookup"><span data-stu-id="12fad-166">In this process you will create a shipment based on the item *packing* dimensions, for which the height is less than 3.</span></span>

1. <span data-ttu-id="12fad-167">Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="12fad-167">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="12fad-168">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="12fad-168">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="12fad-169">Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="12fad-169">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="12fad-170">**Debitorenkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="12fad-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="12fad-171">**Lagerort:** *63*</span><span class="sxs-lookup"><span data-stu-id="12fad-171">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="12fad-172">Wählen Sie **OK** aus, um den Auftrag zu erstellen und das Dialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="12fad-172">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="12fad-173">Der neue Auftrag wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="12fad-173">The new sales order is opened.</span></span> <span data-ttu-id="12fad-174">Es sollte eine neue, leere Position im Raster auf dem Inforegister **Auftragspositionen** enthalten.</span><span class="sxs-lookup"><span data-stu-id="12fad-174">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="12fad-175">Legen Sie die folgenden Werte für diese Position fest:</span><span class="sxs-lookup"><span data-stu-id="12fad-175">On this line, set the following values:</span></span>

    - <span data-ttu-id="12fad-176">**Artikelnummer** *A001*</span><span class="sxs-lookup"><span data-stu-id="12fad-176">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="12fad-177">**Menge** *5*</span><span class="sxs-lookup"><span data-stu-id="12fad-177">**Quantity:** *5*</span></span>

1. <span data-ttu-id="12fad-178">Wählen Sie im Inforegister **Auftragspositionen** die Option **Bestand \> Reservierung** aus.</span><span class="sxs-lookup"><span data-stu-id="12fad-178">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="12fad-179">Wählen Sie auf der Seite **Reservierung** im Aktionsbereich die Option **Los reservieren** aus, um den Lagerbestand zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="12fad-179">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="12fad-180">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="12fad-180">Close the page.</span></span>
1. <span data-ttu-id="12fad-181">Öffnen Sie im Aktionsbereich die Registerkarte **Lagerort** und wählen Sie **Lagerortfreigabe** aus, um Arbeit für den Lagerort zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="12fad-181">On the Action Pane, open the **Warehouse** tab and select **Release to warehouse** to create work for the warehouse.</span></span>
1. <span data-ttu-id="12fad-182">Wechseln Sie auf dem Inforegister **Auftragspositionen** zu **Lagerort \> Lieferdetails**.</span><span class="sxs-lookup"><span data-stu-id="12fad-182">On the **Sales order lines** FastTab, select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="12fad-183">Öffnen Sie im Aktionsbereich die Registerkarte **Transport** und wählen Sie **Container anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="12fad-183">On the Action Pane, open the **Transportation** tab and select **View containers**.</span></span> <span data-ttu-id="12fad-184">Bestätigen Sie, dass der Artikel in den zwei Containern *Kurzer Karton* verpackt wurde.</span><span class="sxs-lookup"><span data-stu-id="12fad-184">Confirm that the item was containerized into the two *Short Box* containers.</span></span>

#### <a name="place-an-item-into-storage"></a><span data-ttu-id="12fad-185">Platzieren eines Artikel im Lager</span><span class="sxs-lookup"><span data-stu-id="12fad-185">Place an item into storage</span></span>

1. <span data-ttu-id="12fad-186">Öffnen Sie das Mobilgerät, melden Sie sich bei Warehouse 63 an und wechseln Sie zu **Bestand \> Anpassen in**.</span><span class="sxs-lookup"><span data-stu-id="12fad-186">Open the mobile device, sign in to warehouse 63 and go to **Inventory \> Adjust In**.</span></span>
1. <span data-ttu-id="12fad-187">Geben Sie **Loc** = *SHORT-01*.</span><span class="sxs-lookup"><span data-stu-id="12fad-187">Enter **Loc** = *SHORT-01*.</span></span> <span data-ttu-id="12fad-188">Erstellen Sie ein neues Kennzeichen mit **Artikel** = *A0001* und **Menge** = *1 Stk.*.</span><span class="sxs-lookup"><span data-stu-id="12fad-188">Make a new license plate with **Item** = *A0001* and **Quantity** = *1 pcs*.</span></span>
1. <span data-ttu-id="12fad-189">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="12fad-189">Select **OK**.</span></span> <span data-ttu-id="12fad-190">Die Fehlermeldung „Lagerplatz SHORT-01 ist fehlgeschlagen, da Artikel A0001 nicht zu den für den Lagerplatz angegebenen Dimensionen passt.“ wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="12fad-190">You will receive the error "Location SHORT-01 failed because item A0001 does not fit in location's specified dimensions."</span></span> <span data-ttu-id="12fad-191">Das liegt daran, dass die Dimensionen der Art *Lagerung* des Produkts größer sind als die im Lagerplatzprofil angegebenen Dimensionen.</span><span class="sxs-lookup"><span data-stu-id="12fad-191">This is because the *Storage* type dimensions of the product are larger than the dimensions specified on the location profile.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]