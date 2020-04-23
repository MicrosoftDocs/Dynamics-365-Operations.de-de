---
title: Lieferantenkataloge importieren
description: In diesem Thema wird beschrieben, wie Lieferantenkatalogdaten importiert werden.
author: mkirknel
manager: tfehr
ms.date: 03/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: mkirknel
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 35b8e2a87708c88b12c5c7605a7977712a35a0f4
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207371"
---
# <a name="import-vendor-catalogs"></a><span data-ttu-id="44520-103">Lieferantenkataloge importieren</span><span class="sxs-lookup"><span data-stu-id="44520-103">Import vendor catalogs</span></span>
[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a><span data-ttu-id="44520-104">Lieferantenkatalogimport</span><span class="sxs-lookup"><span data-stu-id="44520-104">Vendor catalogs import</span></span>

<span data-ttu-id="44520-105">In Dynamics 365 Supply Chain Management können Einkäufer Kataloge erstellen und verwalten, die Unternehmensmitarbeiter beim Bestellen von Artikeln und Dienstleistungen für den internen Gebrauch verwenden können.</span><span class="sxs-lookup"><span data-stu-id="44520-105">In Dynamics 365 Supply Chain Management, purchasing professionals can create and maintain catalogs for company employees to use when they order items and services for internal use.</span></span> <span data-ttu-id="44520-106">Beim Erstellen eines Beschaffungskatalogs können Sie die Artikel und Dienstleistungen hinzufügen, die für Mitarbeiter verfügbar sein sollen, indem Sie entweder die Lieferantenkatalogdaten importieren oder die Lieferantenkatalogdaten manuell dem Produktmaster hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="44520-106">To create a procurement catalog, you can add the items and services that you want to make available to employees, either by importing the product catalog data or by manually adding the product catalog data to the product master.</span></span> 

<span data-ttu-id="44520-107">Sie können Katalogdaten hochladen, die von einem Kreditor vom Kunden Microsoft Dynamics 365 übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="44520-107">You can upload catalog data submitted by a vendor from the Microsoft Dynamics 365 client.</span></span>

<span data-ttu-id="44520-108">Die Produktdaten, die der Lieferant in Form einer Anforderungsdatei für die Katalogverwaltung (CMR-Datei) übermittelt, müssen im XML-Dateiformat vorliegen.</span><span class="sxs-lookup"><span data-stu-id="44520-108">The product data that a vendor submits to you, in the form of a catalog maintenance request (CMR) file, must be in XML file format.</span></span> <span data-ttu-id="44520-109">Die CMR-Datei sollte alle Details der Produkte enthalten, die der Lieferant für Ihr Unternehmen liefern kann.</span><span class="sxs-lookup"><span data-stu-id="44520-109">The CMR file should contain the details for the products that the vendor supplies to your company.</span></span>
<span data-ttu-id="44520-110">''''</span><span class="sxs-lookup"><span data-stu-id="44520-110">''''</span></span>
## <a name="import-vendor-catalog-data"></a><span data-ttu-id="44520-111">Importieren von Lieferantenkatalogdaten</span><span class="sxs-lookup"><span data-stu-id="44520-111">Import vendor catalog data</span></span>
<span data-ttu-id="44520-112">Führen Sie zum Importieren der Lieferantenkatalogdaten die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="44520-112">'' To import vendor catalog data, you must complete the following tasks:</span></span>

1.  <span data-ttu-id="44520-113">Richten Sie ein Projekt im Datenverwaltungsarbeitsbereich ein, in dem Sie die Datenenzuordnungsregeln definiert haben.</span><span class="sxs-lookup"><span data-stu-id="44520-113">Set up a project in the Data management workspace where you have defined your data mapping rules.</span></span> <span data-ttu-id="44520-114">Wählen Sie **Datenverwaltung** und **Einstellungsrollen für Datenprojekte** aus.</span><span class="sxs-lookup"><span data-stu-id="44520-114">Select **Data management** and then select **Set up roles for data projects**.</span></span> 
    <span data-ttu-id="44520-115">''</span><span class="sxs-lookup"><span data-stu-id="44520-115">''</span></span>
2.  <span data-ttu-id="44520-116">Richten Sie eine Beschaffungskategoriehierarchie ein, und weisen Sie den Beschaffungskategorien Lieferanten zu.</span><span class="sxs-lookup"><span data-stu-id="44520-116">Set up a procurement category hierarchy, and assign your vendors to procurement categories.</span></span> <span data-ttu-id="44520-117">Wenn Sie Warencodes verwenden, fügen Sie die Warencodes den Beschaffungskategorien hinzu.</span><span class="sxs-lookup"><span data-stu-id="44520-117">If you use commodity codes, add the commodity codes to the procurement categories.</span></span> <span data-ttu-id="44520-118">Informationen zum Einrichten einer Beschaffungskategoriehierarchie finden Sie unter [Einrichten einer Beschaffungskategoriehierarchie](../procurement/tasks/set-up-procurement-category-hierarchy.md)</span><span class="sxs-lookup"><span data-stu-id="44520-118">For information about setting up a procurement category hierarchy, see [Set up a procurement category hierarchy](../procurement/tasks/set-up-procurement-category-hierarchy.md).</span></span>
    <span data-ttu-id="44520-119">''</span><span class="sxs-lookup"><span data-stu-id="44520-119">''</span></span>
3.  <span data-ttu-id="44520-120">Konfigurieren Sie den Lieferanten für den Katalogimport.</span><span class="sxs-lookup"><span data-stu-id="44520-120">Configure the vendor for catalog import.</span></span> <span data-ttu-id="44520-121">Wählen Sie einen Kreditor aus, und wählen Sie anschließend **Beschaffung** > **Einstellungen** > **Kreditor für Katalogimport konfigurieren** aus.</span><span class="sxs-lookup"><span data-stu-id="44520-121">Select a vendor, and then select **Procurement** > **Set up** > **Configure vendor for catalog import**.</span></span>
<span data-ttu-id="44520-122">''''</span><span class="sxs-lookup"><span data-stu-id="44520-122">''''</span></span>
4.  <span data-ttu-id="44520-123">Konfigurieren Sie den Workflow für den Katalogimport.</span><span class="sxs-lookup"><span data-stu-id="44520-123">Configure workflow for catalog import.</span></span> <span data-ttu-id="44520-124">Erstellen Sie eine CMR-Dateivorlage und geben Sie diese mit dem Kreditor frei.</span><span class="sxs-lookup"><span data-stu-id="44520-124">Create a CMR file template and share this with your vendor.</span></span>

5.  <span data-ttu-id="44520-125">Wählen Sie **Beschaffung** \> **Gemeinsam** \> **Kataloge** \> **Lieferantenkataloge**, um einen Lieferantenkatalog zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="44520-125">Select **Procurement and sourcing** \> **Common** \> **Catalogs** \> **Vendor catalogs** to create a vendor catalog.</span></span> <span data-ttu-id="44520-126">In diesem Katalog werden die Anforderungsdateien für die Katalogverwaltung (CMR-Dateien) gruppiert, die Sie von Ihrem Lieferanten erhalten.</span><span class="sxs-lookup"><span data-stu-id="44520-126">The catalog maintenance request (CMR) files that you receive from your vendor are grouped in this catalog.</span></span> 

6.  <span data-ttu-id="44520-127">Laden Sie die CMR-Datei hoch.</span><span class="sxs-lookup"><span data-stu-id="44520-127">Upload the CMR file.</span></span>

7.  <span data-ttu-id="44520-128">Prüfen Sie die Produkte im Lieferantenkatalog, um sie entweder zu genehmigen oder abzulehnen.</span><span class="sxs-lookup"><span data-stu-id="44520-128">Review, approve, or reject the products in the vendor catalog.</span></span> <span data-ttu-id="44520-129">Die Produkte werden automatisch den Beschaffungskategorien zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="44520-129">The products are automatically mapped to the procurement categories.</span></span> 
    
<span data-ttu-id="44520-130">Genehmigte Produkte werden dem Produktmaster hinzugefügt und für die ausgewählten juristischen Personen freigegeben.</span><span class="sxs-lookup"><span data-stu-id="44520-130">Approved products are added to the product master and are released to the selected legal entities.</span></span> <span data-ttu-id="44520-131">Nur genehmigte Produkte können dem Beschaffungskatalog hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="44520-131">Only approved products can be added to the procurement catalog.</span></span>

## <a name="generate-a-catalog-import-file-template"></a><span data-ttu-id="44520-132">Generieren einer Katalogimport-Dateivorlage</span><span class="sxs-lookup"><span data-stu-id="44520-132">Generate a catalog import file template</span></span>

<span data-ttu-id="44520-133">Bei der Katalogimport-Dateivorlage handelt es sich um eine XSD-Datei, mit der eine CMR-Datei für die Lieferantenprodukte erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="44520-133">The catalog import file template is an XSD file that you use to create a CMR file for a vendor's products.</span></span> <span data-ttu-id="44520-134">Mithilfe der erstellten CMR-Datei können Sie einen neuen Katalog erstellen, einen vorhandenen Katalog ersetzen oder einen vorhandenen Katalog ändern.</span><span class="sxs-lookup"><span data-stu-id="44520-134">You can use the CMR file to create a new catalog, replace an existing catalog, or modify an existing catalog.</span></span>

1.  <span data-ttu-id="44520-135">Wählen Sie **Beschaffung** \> **Kataloge** \> **Lieferantenkataloge** aus und doppelklicken Sie auf den Katalog, den Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="44520-135">Select **Procurement and sourcing** \> **Catalogs** \> **Vendor catalogs** and double-click the catalog that you want to work with.</span></span>

2.  <span data-ttu-id="44520-136">Laden Sie eine aktuelle Katalogimportvorlage herunter (XSD-Datei).</span><span class="sxs-lookup"><span data-stu-id="44520-136">Download a current catalog import template (XSD file).</span></span> <span data-ttu-id="44520-137">Auf der Seite **Katalog aktualisieren** auf **Aktivitätsbereich**, auf der Registerkarte **Kataloge** in der Gruppe **Zugehörige Informationen**, **Katalogvorlage generieren**, und wählen Sie **Beschaffungskategorie** aus.</span><span class="sxs-lookup"><span data-stu-id="44520-137">On the **Update catalog** page, on the **Action Pane**, on the **Catalogs** tab, in the **Related information** group, click **Generate catalog template** and select **Procurement category**.</span></span>

    -   <span data-ttu-id="44520-138">Mit der **Beschaffungskatalog**-Option können Sie eine Katalogvorlage mit den Beschaffungskategorien, in denen der Lieferant zum Liefern von Produkten autorisiert ist erstellen.</span><span class="sxs-lookup"><span data-stu-id="44520-138">With the **Procurement category** option you can generate a catalog template that includes the procurement categories in which the vendor is authorized to provide products.</span></span>

3. <span data-ttu-id="44520-139">Wählen Sie im Dialogfeld **Speichern unter** den Ort aus, an dem die Katalogdateivorlage gespeichert werden soll, und speichern Sie sie.</span><span class="sxs-lookup"><span data-stu-id="44520-139">In the **Save as** dialog box, select the location where you want to store the catalog file template and save the file.</span></span>

<span data-ttu-id="44520-140">Weitere Informationen und Beispiele finden Sie in diesem Blogbeitrag: [Kreditorenkataloge in Dynamics AX.](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/)</span><span class="sxs-lookup"><span data-stu-id="44520-140">For more information and for examples, refer to this blog post: [Vendor catalogs in Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).</span></span>
