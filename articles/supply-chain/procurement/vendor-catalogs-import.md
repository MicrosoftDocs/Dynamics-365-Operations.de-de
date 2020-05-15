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
ms.openlocfilehash: 608d2b57bb4d5ab80d75b22ed5c8a4df5263e5f3
ms.sourcegitcommit: 86052c58e3c365c443bd6f37ad1054bea395e21b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/06/2020
ms.locfileid: "3338307"
---
# <a name="import-vendor-catalogs"></a><span data-ttu-id="1ab3c-103">Lieferantenkataloge importieren</span><span class="sxs-lookup"><span data-stu-id="1ab3c-103">Import vendor catalogs</span></span>

[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a><span data-ttu-id="1ab3c-104">Lieferantenkatalogimport</span><span class="sxs-lookup"><span data-stu-id="1ab3c-104">Vendor catalogs import</span></span>

<span data-ttu-id="1ab3c-105">In Dynamics 365 Supply Chain Management können Einkäufer Kataloge erstellen und verwalten, die Unternehmensmitarbeiter beim Bestellen von Artikeln und Dienstleistungen für den internen Gebrauch verwenden können.</span><span class="sxs-lookup"><span data-stu-id="1ab3c-105">In Dynamics 365 Supply Chain Management, purchasing professionals can create and maintain catalogs for company employees to use when they order items and services for internal use.</span></span> <span data-ttu-id="1ab3c-106">Beim Erstellen eines Beschaffungskatalogs können Sie die Artikel und Dienstleistungen hinzufügen, die für Mitarbeiter verfügbar sein sollen, indem Sie entweder die Lieferantenkatalogdaten importieren oder die Lieferantenkatalogdaten manuell dem Produktmaster hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1ab3c-106">To create a procurement catalog, you can add the items and services that you want to make available to employees, either by importing the product catalog data or by manually adding the product catalog data to the product master.</span></span> 

<span data-ttu-id="1ab3c-107">Sie können Katalogdaten hochladen, die von einem Kreditor vom Kunden Microsoft Dynamics 365 übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="1ab3c-107">You can upload catalog data submitted by a vendor from the Microsoft Dynamics 365 client.</span></span>

<span data-ttu-id="1ab3c-108">Die Produktdaten, die der Lieferant in Form einer Anforderungsdatei für die Katalogverwaltung (CMR-Datei) übermittelt, müssen im XML-Dateiformat vorliegen.</span><span class="sxs-lookup"><span data-stu-id="1ab3c-108">The product data that a vendor submits to you, in the form of a catalog maintenance request (CMR) file, must be in XML file format.</span></span> <span data-ttu-id="1ab3c-109">Die CMR-Datei sollte alle Details der Produkte enthalten, die der Lieferant für Ihr Unternehmen liefern kann.</span><span class="sxs-lookup"><span data-stu-id="1ab3c-109">The CMR file should contain the details for the products that the vendor supplies to your company.</span></span>

## <a name="import-vendor-catalog-data"></a><span data-ttu-id="1ab3c-110">Importieren von Lieferantenkatalogdaten</span><span class="sxs-lookup"><span data-stu-id="1ab3c-110">Import vendor catalog data</span></span>

<span data-ttu-id="1ab3c-111">Führen Sie zum Importieren der Lieferantenkatalogdaten die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="1ab3c-111">To import vendor catalog data, you must complete the following tasks:</span></span>

1. <span data-ttu-id="1ab3c-112">Richten Sie ein Projekt im Datenverwaltungsarbeitsbereich ein, in dem Sie die Datenenzuordnungsregeln definiert haben.</span><span class="sxs-lookup"><span data-stu-id="1ab3c-112">Set up a project in the Data management workspace where you have defined your data mapping rules.</span></span> <span data-ttu-id="1ab3c-113">Wählen Sie **Datenverwaltung** und **Einstellungsrollen für Datenprojekte** aus.</span><span class="sxs-lookup"><span data-stu-id="1ab3c-113">Select **Data management** and then select **Set up roles for data projects**.</span></span>

2. <span data-ttu-id="1ab3c-114">Richten Sie eine Beschaffungskategoriehierarchie ein, und weisen Sie den Beschaffungskategorien Lieferanten zu.</span><span class="sxs-lookup"><span data-stu-id="1ab3c-114">Set up a procurement category hierarchy, and assign your vendors to procurement categories.</span></span> <span data-ttu-id="1ab3c-115">Wenn Sie Warencodes verwenden, fügen Sie die Warencodes den Beschaffungskategorien hinzu.</span><span class="sxs-lookup"><span data-stu-id="1ab3c-115">If you use commodity codes, add the commodity codes to the procurement categories.</span></span> <span data-ttu-id="1ab3c-116">Informationen zum Einrichten einer Beschaffungskategoriehierarchie finden Sie unter [Einrichten einer Beschaffungskategoriehierarchie](../procurement/tasks/set-up-procurement-category-hierarchy.md)</span><span class="sxs-lookup"><span data-stu-id="1ab3c-116">For information about setting up a procurement category hierarchy, see [Set up a procurement category hierarchy](../procurement/tasks/set-up-procurement-category-hierarchy.md).</span></span>

3. <span data-ttu-id="1ab3c-117">Konfigurieren Sie den Lieferanten für den Katalogimport.</span><span class="sxs-lookup"><span data-stu-id="1ab3c-117">Configure the vendor for catalog import.</span></span> <span data-ttu-id="1ab3c-118">Wählen Sie einen Kreditor aus, und wählen Sie anschließend **Beschaffung** > **Einstellungen** > **Kreditor für Katalogimport konfigurieren** aus.</span><span class="sxs-lookup"><span data-stu-id="1ab3c-118">Select a vendor, and then select **Procurement** > **Set up** > **Configure vendor for catalog import**.</span></span>

4. <span data-ttu-id="1ab3c-119">Konfigurieren Sie den Workflow für den Katalogimport.</span><span class="sxs-lookup"><span data-stu-id="1ab3c-119">Configure workflow for catalog import.</span></span> <span data-ttu-id="1ab3c-120">Erstellen Sie eine CMR-Dateivorlage und geben Sie diese mit dem Kreditor frei.</span><span class="sxs-lookup"><span data-stu-id="1ab3c-120">Create a CMR file template and share this with your vendor.</span></span>

5. <span data-ttu-id="1ab3c-121">Wählen Sie **Beschaffung** \> **Gemeinsam** \> **Kataloge** \> **Lieferantenkataloge**, um einen Lieferantenkatalog zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1ab3c-121">Select **Procurement and sourcing** \> **Common** \> **Catalogs** \> **Vendor catalogs** to create a vendor catalog.</span></span> <span data-ttu-id="1ab3c-122">In diesem Katalog werden die Anforderungsdateien für die Katalogverwaltung (CMR-Dateien) gruppiert, die Sie von Ihrem Lieferanten erhalten.</span><span class="sxs-lookup"><span data-stu-id="1ab3c-122">The catalog maintenance request (CMR) files that you receive from your vendor are grouped in this catalog.</span></span> 

6. <span data-ttu-id="1ab3c-123">Laden Sie die CMR-Datei hoch.</span><span class="sxs-lookup"><span data-stu-id="1ab3c-123">Upload the CMR file.</span></span>

7. <span data-ttu-id="1ab3c-124">Prüfen Sie die Produkte im Lieferantenkatalog, um sie entweder zu genehmigen oder abzulehnen.</span><span class="sxs-lookup"><span data-stu-id="1ab3c-124">Review, approve, or reject the products in the vendor catalog.</span></span> <span data-ttu-id="1ab3c-125">Die Produkte werden automatisch den Beschaffungskategorien zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="1ab3c-125">The products are automatically mapped to the procurement categories.</span></span> 

<span data-ttu-id="1ab3c-126">Genehmigte Produkte werden dem Produktmaster hinzugefügt und für die ausgewählten juristischen Personen freigegeben.</span><span class="sxs-lookup"><span data-stu-id="1ab3c-126">Approved products are added to the product master and are released to the selected legal entities.</span></span> <span data-ttu-id="1ab3c-127">Nur genehmigte Produkte können dem Beschaffungskatalog hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="1ab3c-127">Only approved products can be added to the procurement catalog.</span></span>

## <a name="generate-a-catalog-import-file-template"></a><span data-ttu-id="1ab3c-128">Generieren einer Katalogimport-Dateivorlage</span><span class="sxs-lookup"><span data-stu-id="1ab3c-128">Generate a catalog import file template</span></span>

<span data-ttu-id="1ab3c-129">Bei der Katalogimport-Dateivorlage handelt es sich um eine XSD-Datei, mit der eine CMR-Datei für die Lieferantenprodukte erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1ab3c-129">The catalog import file template is an XSD file that you use to create a CMR file for a vendor's products.</span></span> <span data-ttu-id="1ab3c-130">Mithilfe der erstellten CMR-Datei können Sie einen neuen Katalog erstellen, einen vorhandenen Katalog ersetzen oder einen vorhandenen Katalog ändern.</span><span class="sxs-lookup"><span data-stu-id="1ab3c-130">You can use the CMR file to create a new catalog, replace an existing catalog, or modify an existing catalog.</span></span>

1. <span data-ttu-id="1ab3c-131">Wählen Sie **Beschaffung** \> **Kataloge** \> **Lieferantenkataloge** aus, und doppelklicken Sie auf den Katalog, den Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="1ab3c-131">Select **Procurement and sourcing** \> **Catalogs** \> **Vendor  catalogs** and double-click the catalog that you want  to work with.</span></span>

2. <span data-ttu-id="1ab3c-132">Laden Sie eine aktuelle Katalogimportvorlage herunter (XSD-Datei).</span><span class="sxs-lookup"><span data-stu-id="1ab3c-132">Download a current catalog import template (XSD file).</span></span> <span data-ttu-id="1ab3c-133">Auf der Seite **Katalog aktualisieren** auf **Aktivitätsbereich**, auf der Registerkarte **Kataloge** in der Gruppe **Zugehörige Informationen**, **Katalogvorlage generieren**, und wählen Sie **Beschaffungskategorie** aus.</span><span class="sxs-lookup"><span data-stu-id="1ab3c-133">On the **Update catalog** page, on the **Action Pane**, on the **Catalogs** tab, in the **Related information** group, click **Generate catalog template** and select **Procurement category**.</span></span>

    - <span data-ttu-id="1ab3c-134">Mit der **Beschaffungskatalog**-Option können Sie eine Katalogvorlage mit den Beschaffungskategorien, in denen der Lieferant zum Liefern von Produkten autorisiert ist erstellen.</span><span class="sxs-lookup"><span data-stu-id="1ab3c-134">With the **Procurement category** option you can generate a catalog template that includes the procurement categories in which the vendor is authorized to provide products.</span></span>

3. <span data-ttu-id="1ab3c-135">Wählen Sie im Dialogfeld **Speichern unter** den Ort aus, an dem die Katalogdateivorlage gespeichert werden soll, und speichern Sie sie.</span><span class="sxs-lookup"><span data-stu-id="1ab3c-135">In the **Save as** dialog box, select the location where you want to store the catalog file template and save the file.</span></span>

<span data-ttu-id="1ab3c-136">Weitere Informationen und Beispiele finden Sie in diesem Blogbeitrag: [Kreditorenkataloge in Dynamics AX.](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/)</span><span class="sxs-lookup"><span data-stu-id="1ab3c-136">For more information and for examples, refer to this blog post: [Vendor catalogs in Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).</span></span>
