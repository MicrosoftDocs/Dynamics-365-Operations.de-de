---
title: "Vorlagenstücklisten"
description: "Mit einer Vorlagenstückliste verfügen Sie über eine standardisierte Liste von Komponenten für Serviceobjekte, die regelmäßig verwaltet werden."
author: ShylaThompson
manager: AnnBe
ms.date: 09/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1aae5797e37b846a38f957b02870e213da528a2d
ms.openlocfilehash: f9c61ecd79f38301f46e3c21a33ec2801f33d19f
ms.contentlocale: de-de
ms.lasthandoff: 09/21/2018

---

# <a name="template-boms"></a><span data-ttu-id="bd9f1-103">Vorlagenstücklisten</span><span class="sxs-lookup"><span data-stu-id="bd9f1-103">Template BOMs</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="bd9f1-104">Mit einer Vorlagenstückliste verfügen Sie über eine standardisierte Liste von Komponenten für Serviceobjekte, die regelmäßig verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-104">A template bill of materials (BOM) provides you with a standardized list of components for service objects that are serviced regularly.</span></span> <span data-ttu-id="bd9f1-105">Die in der Vorlagenstückliste aufgeführten Komponenten stellen die einzelnen Unterkomponenten des Serviceobjekts dar.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-105">The components that are listed in the template BOM represent the individual subcomponents of the service object.</span></span> <span data-ttu-id="bd9f1-106">Indem Sie eine Vorlagenstückliste auf ein Serviceobjekt anwenden, können Sie die verfolgen, welche Unterkomponenten im Serviceobjekt ersetzt wurden.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-106">By applying a template BOM to a service object, you can keep a record of the subcomponents that have been replaced on the service object.</span></span>

<span data-ttu-id="bd9f1-107">Um eine Vorlagenstückliste auf eine Servicevereinbarung oder einen Serviceauftrag anzuwenden, ordnen Sie sie einer Serviceobjektbeziehung zu.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-107">To apply a template BOM to a service agreement or a service order, you attach it to a service object relation.</span></span>


> [!NOTE]
> <P><span data-ttu-id="bd9f1-108">Einem Serviceobjekt kann nur eine Vorlagenstückliste zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-108">You can apply only one template BOM to a service object.</span></span></P>

## <a name="create-a-template-bom"></a><span data-ttu-id="bd9f1-109">Erstellen einer Vorlagenstückliste</span><span class="sxs-lookup"><span data-stu-id="bd9f1-109">Create a template BOM</span></span>

<span data-ttu-id="bd9f1-110">Die folgende Tabelle enthält Informationen zu den verschiedenen Methoden, die Sie zum Erstellen einer Vorlagenstückliste verwenden können.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-110">The following table contains information about the various methods that you can use to create a template BOM.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bd9f1-111">Methode</span><span class="sxs-lookup"><span data-stu-id="bd9f1-111">Method</span></span></p></th>
<th><p><span data-ttu-id="bd9f1-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bd9f1-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd9f1-113">Produktion</span><span class="sxs-lookup"><span data-stu-id="bd9f1-113">Production</span></span></p></td>
<td><p><span data-ttu-id="bd9f1-114">Die Vorlagenstückliste basiert auf einem Produktionsauftrag.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-114">The template BOM is based on a production order.</span></span> <span data-ttu-id="bd9f1-115">Diese Option kann nur angewendet werden, wenn Sie innerhalb einer Produktionsumgebung agieren.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-115">This option is applicable only if you operate in a production environment.</span></span> <span data-ttu-id="bd9f1-116">Der Vorteil besteht darin, dass Sie über eine aktuelle und umfassende Auflistung der Komponenten eines Artikels verfügen.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-116">The benefit is that you have a current, detailed listing of the components that make up an item.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd9f1-117">Artikel BOM</span><span class="sxs-lookup"><span data-stu-id="bd9f1-117">Item BOM</span></span></p></td>
<td><p><span data-ttu-id="bd9f1-118">Die Vorlagenstückliste basiert auf einer Artikelstückliste.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-118">The template BOM is based on an item BOM.</span></span> <span data-ttu-id="bd9f1-119">Die Artikelstückliste ist im Gegensatz zur Produktionsstückliste eine statische Liste der Komponenten, die einen Artikel bilden.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-119">The item BOM, unlike the production BOM, is a static list of the components that make up an item.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd9f1-120">Vorhandene Vorlage</span><span class="sxs-lookup"><span data-stu-id="bd9f1-120">Existing template</span></span></p></td>
<td><p><span data-ttu-id="bd9f1-121">Die Vorlage basiert auf einer vorhandenen Vorlagenstückliste.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-121">The template is based on an existing template BOM.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd9f1-122">Manuell</span><span class="sxs-lookup"><span data-stu-id="bd9f1-122">Manual</span></span></p></td>
<td><p><span data-ttu-id="bd9f1-123">Wenn Sie genau wissen, welche Ersatzteile in der Regel in einem Serviceobjekt ersetzt werden, können Sie die Vorlagenstückliste manuell erstellen.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-123">If you know what spare parts are typically replaced on a service object, you can create your template BOM manually.</span></span> <span data-ttu-id="bd9f1-124">Mit dieser Methode können leichter Sie sicherstellen, dass die in der Vorlage enthaltenen Komponenten die tatsächlichen Anforderungen des Arbeitsplatzes widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-124">This method helps make sure that the components that are included in the template reflect the actual requirements of your workplace.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="apply-the-template-bom-to-a-service-agreement-or-service-order"></a><span data-ttu-id="bd9f1-125">Wenden Sie die Vorlagenstückliste auf eine Servicevereinbarung oder einen Serviceauftrag an</span><span class="sxs-lookup"><span data-stu-id="bd9f1-125">Apply the template BOM to a service agreement or service order</span></span>

<span data-ttu-id="bd9f1-126">Die Vorlagenstückliste kann auf eine Servicevereinbarung, einen Serviceauftrag oder beides angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-126">You can apply a template BOM to a service agreement, a service order, or both.</span></span> <span data-ttu-id="bd9f1-127">Die Servicevereinbarung deckt in der Regel eine langfristige Beziehung zu einem Debitor ab.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-127">The service agreement usually covers a long-term relationship with a customer.</span></span> <span data-ttu-id="bd9f1-128">Bei dem in der Vorlagenstückliste aufgezeichnete Verlauf von Ersetzungen handelt es sich um nützliche Daten für die Servicevereinbarung.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-128">The history of replacements that is recorded in the service BOM is useful data to have for the service agreement.</span></span>

<span data-ttu-id="bd9f1-129">Vorlagenstücklisten können auch auf einen Serviceauftrag angewendet werden, um den Verlauf der Dienstleistung erfassen, die an einem Serviceobjekt erbracht wurde.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-129">You can also apply a template BOM to a service order to record the history of the service that has been performed on a service object.</span></span>

## <a name="copy-the-history-of-a-service-bom"></a><span data-ttu-id="bd9f1-130">Kopieren des Verlaufs einer Servicestückliste</span><span class="sxs-lookup"><span data-stu-id="bd9f1-130">Copy the history of a service BOM</span></span>

<span data-ttu-id="bd9f1-131">Der Verlauf einer Servicestücklistenposition kann zwischen Servicevereinbarungen kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-131">You can copy the history of a service BOM line from one service agreement to another service agreement.</span></span> <span data-ttu-id="bd9f1-132">Durch das Kopieren des Serviceverlaufs zwischen Servicevereinbarungen kann der Datensatz zu Ersetzungen für einen Artikel erhalten werden.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-132">By copying the service history between service agreements, you can preserve the record of replacements for an item.</span></span>

<span data-ttu-id="bd9f1-133">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="bd9f1-133">**Example**</span></span>

<span data-ttu-id="bd9f1-134">Sie haben eine Servicevereinbarung über drei Jahre für das Auto eines Kunden eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-134">You have set up a three-year service agreement for a customer's car.</span></span> <span data-ttu-id="bd9f1-135">Während dieser Periode gewöhnt sich der Debitor an den guten Service, die das Unternehmen anbietet.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-135">During that period, the customer becomes accustomed to the good service that the company provides.</span></span> <span data-ttu-id="bd9f1-136">Nach dem Ablauf der Vereinbarung möchte der Debitor daher eine neue Vereinbarung treffen.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-136">Therefore, after the agreement expires, the customer wants to set up a new one.</span></span> <span data-ttu-id="bd9f1-137">Sie können nun eine günstigere Vereinbarung für das Unternehmen aushandeln.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-137">You are now able to negotiate a more favorable agreement for the company.</span></span> <span data-ttu-id="bd9f1-138">Da der Datensatz ersetzter Komponenten in der Zukunft nützlich sein kann, kopieren Sie den Verlauf der Servicestückliste in die neue Vereinbarung.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-138">Because the record of replaced components might be useful in the future, you copy the history of the service BOM to the new agreement.</span></span>

## <a name="modify-the-template-bom"></a><span data-ttu-id="bd9f1-139">Ändern der Vorlagenstückliste</span><span class="sxs-lookup"><span data-stu-id="bd9f1-139">Modify the template BOM</span></span>

<span data-ttu-id="bd9f1-140">Wenn eine Vorlagenstückliste keinem Serviceobjekt zugeordnet wurde, können Sie sie ändern oder Positionen daraus löschen.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-140">If a template BOM has not been attached to a service object, you can modify or delete lines in it.</span></span> <span data-ttu-id="bd9f1-141">Nach der Zuordnung der Vorlagenstückliste zu einem Serviceobjekt kann nur die lokale Version der Stückliste geändert werden.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-141">After the template BOM is attached to a service object, you can modify only the local version of the BOM.</span></span> <span data-ttu-id="bd9f1-142">Zum Duplizieren der Einstellungen der lokalen Version einer Vorlagenstückliste kann eine neue Vorlagenstückliste auf Grundlage der der lokalen Version erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-142">If you want to duplicate the setup of a local version of a template BOM, you can create a new template BOM based on the local version.</span></span> <span data-ttu-id="bd9f1-143">Weitere Informationen zu Serviceintervallen finden Sie unter [Ändern einer Servicestückliste](modify-service-bom.md).</span><span class="sxs-lookup"><span data-stu-id="bd9f1-143">For more information, see [Modify a Service BOM](modify-service-bom.md).</span></span>

<span data-ttu-id="bd9f1-144">Wenn Sie einen Artikel in der Stückliste ersetzen, können Sie die Ersetzung in der Stücklistenposition im Stücklisten-Designer erfassen.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-144">If you replace an item in the BOM, you can register the replacement on the BOM line in the BOM designer.</span></span> <span data-ttu-id="bd9f1-145">Optional können Sie eine Serviceauftragsposition für das Ersetzungsobjekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-145">Optionally, you can create a service order line for the replacement object.</span></span> <span data-ttu-id="bd9f1-146">Wenn Sie eine Serviceauftragsposition erstellen, können Sie den Ersetzungsartikel fakturieren.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-146">If you create a service order line, you can invoice the replacement item.</span></span> <span data-ttu-id="bd9f1-147">Wenn keine Serviceauftragsposition für eine Ersetzung erstellt wird, wird die Ersetzungserfassung zum Nachverfolgen des Verlaufs des Serviceobjekts in den Datensätzen beibehalten.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-147">If you do not create a service order line for a replacement, the replacement registration is kept to track the history of the service object.</span></span>

## <a name="change-how-information-on-the-bom-line-is-displayed"></a><span data-ttu-id="bd9f1-148">Ändern, wie Informationen zu Stücklistenposition angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="bd9f1-148">Change how information on the BOM line is displayed</span></span>

<span data-ttu-id="bd9f1-149">Die Anzeige der Stücklistenpositionsdaten kann für alle Vorlagen- und Servicestücklisten geändert werden.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-149">You can change the way that information on the BOM line is displayed for all template and service BOMs.</span></span> <span data-ttu-id="bd9f1-150">Die Änderungen werden auf alle Vorlagen- und Servicestücklisten angewendet.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-150">The changes are applied to all template BOMs and service BOMs.</span></span> <span data-ttu-id="bd9f1-151">Hierzu gehören auch diejenigen, die Serviceobjekten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-151">This includes those that are attached to service objects.</span></span>

## <a name="set-up-number-sequences-for-template-boms"></a><span data-ttu-id="bd9f1-152">Einrichten von Nummernkreisen für die Vorlagenstückliste</span><span class="sxs-lookup"><span data-stu-id="bd9f1-152">Set up number sequences for template BOMs</span></span>

<span data-ttu-id="bd9f1-153">Um Vorlagenstücklisten verwenden möchten, müssen Sie zwei Nummernkreise einrichten.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-153">To use template BOMs, you must set up two number sequences.</span></span> <span data-ttu-id="bd9f1-154">Richten Sie einen Nummernkreis für die Vorlagenstückliste und einen die für die Positionsnummer des Stücklistenverlaufs ein.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-154">Set up one number sequence for the template BOM and one for the BOM history line number.</span></span>


> [!NOTE]
> <P><span data-ttu-id="bd9f1-155">Nummernkreise werden in Sequenzen verwendet, um Datensätzen, die dies erfordern, Kennungen zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-155">Number sequences are used to allocate identifiers to records that require them.</span></span> <span data-ttu-id="bd9f1-156">Bevor Sie einen Nummernkreis einer Vorlagenstückliste oder Positionsnummer des Stücklistenverlaufs zuweisen können, müssen Sie Nummernkreiscodes einrichten.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-156">Before you can assign a number sequence to a template BOM or a BOM history line number, you must set up number sequences codes.</span></span></P>


## <a name="set-up-number-sequences"></a><span data-ttu-id="bd9f1-157">Nummernkreise einrichten</span><span class="sxs-lookup"><span data-stu-id="bd9f1-157">Set up number sequences</span></span>

1.  <span data-ttu-id="bd9f1-158">Erstellen Sie auf der Listenseite **Nummernkreise** Nummernkreise für Vorlagenstücklisten und die Positionsnummer des Stücklistenverlaufs.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-158">On the **Number sequences** list page, create number sequences for template BOMs and the BOM history line number.</span></span> 

2.  <span data-ttu-id="bd9f1-159">Klicken Sie auf **Serviceverwaltung** \> **Einrichtung** \> **Serviceverwaltungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-159">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

3.  <span data-ttu-id="bd9f1-160">Klicken Sie auf **Nummernkreise**, und wählen Sie dann einen Nummernkreiscode für Nummernkreisreferenzen aus, die Sie im Formular **Nummernkreise** erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-160">Click **Number sequences**, and then select a number sequence code for the number sequence references that you created in the **Number sequences** form.</span></span>

4.  <span data-ttu-id="bd9f1-161">Schließen Sie das Formular, um Ihre Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-161">Close the form to save your changes.</span></span>


> [!NOTE]
> <P><span data-ttu-id="bd9f1-162">Die Positionsnummer des Stücklistenverlaufs wird verwendet, um die Buchungen im Stücklistenverlauf einem Servicevertrag oder Serviceauftrag zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-162">The BOM history line number is used by the system to associate the transactions in the BOM history with a service agreement or service order.</span></span> <span data-ttu-id="bd9f1-163">Die Nummer wird nicht in der Benutzeroberfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bd9f1-163">The number is not displayed in the user interface.</span></span></P>



## <a name="see-also"></a><span data-ttu-id="bd9f1-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd9f1-164">See also</span></span>

[<span data-ttu-id="bd9f1-165">Erstellen einer Vorlagenstückliste</span><span class="sxs-lookup"><span data-stu-id="bd9f1-165">Create a template BOM</span></span>](create-template-bom.md)

[<span data-ttu-id="bd9f1-166">Verwalten von Vorlagenstücklisten für Objektbeziehungen</span><span class="sxs-lookup"><span data-stu-id="bd9f1-166">Manage template BOMs on object relations</span></span>](manage-template-boms-on-object-relations.md)

[<span data-ttu-id="bd9f1-167">Ändern einer Servicestückliste</span><span class="sxs-lookup"><span data-stu-id="bd9f1-167">Modify a Service BOM</span></span>](modify-service-bom.md)

 



