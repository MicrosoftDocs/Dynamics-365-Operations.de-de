---
title: Kaufverträge eingeben
description: Diese Prozedur zeigt wie Sie einen Kaufvertrag erstellen, der einen Debitor verpflichtet, ein Produkt in einer bestimmten Menge über einen vorgegebenen Zeitraum zu erwerben, wobei ihm im Gegenzug Rabatte zustehen.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 025c9fe2f769f37b63bd79c6c3afedc31a955310
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "346869"
---
# <a name="enter-sales-agreements"></a><span data-ttu-id="c3ae8-103">Kaufverträge eingeben</span><span class="sxs-lookup"><span data-stu-id="c3ae8-103">Enter sales agreements</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c3ae8-104">Diese Prozedur zeigt wie Sie einen Kaufvertrag erstellen, der einen Debitor verpflichtet, ein Produkt in einer bestimmten Menge über einen vorgegebenen Zeitraum zu erwerben, wobei ihm im Gegenzug Rabatte zustehen.</span><span class="sxs-lookup"><span data-stu-id="c3ae8-104">This procedure shows you how to create a sales agreement that commits one of your customers to buy a product for an agreed amount over time in exchange for special discounts.</span></span> <span data-ttu-id="c3ae8-105">Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3ae8-105">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-sales-agreement-header"></a><span data-ttu-id="c3ae8-106">Kaufvertragskopfzeile einrichten</span><span class="sxs-lookup"><span data-stu-id="c3ae8-106">Set up sales agreement header</span></span>
1. <span data-ttu-id="c3ae8-107">Wechseln Sie zu "Vertrieb und Marketing" > "Kaufverträge" > "Kaufverträge".</span><span class="sxs-lookup"><span data-stu-id="c3ae8-107">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="c3ae8-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="c3ae8-108">Click New.</span></span>
3. <span data-ttu-id="c3ae8-109">Klicken Sie im Feld "Debitorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c3ae8-109">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="c3ae8-110">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="c3ae8-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="c3ae8-111">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c3ae8-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c3ae8-112">Klicken Sie im Feld "Kaufvertragsklassifizierung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c3ae8-112">In the Sales agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="c3ae8-113">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c3ae8-113">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="c3ae8-114">Erweitern Sie den Abschnitt "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="c3ae8-114">Expand the General section.</span></span>
9. <span data-ttu-id="c3ae8-115">Wählen Sie im Feld "Standardzusage" "Produktwertszusage" aus.</span><span class="sxs-lookup"><span data-stu-id="c3ae8-115">In the Default commitment field, select 'Product value commitment'.</span></span>
    * <span data-ttu-id="c3ae8-116">Ein Zusagetyp ist ein erforderliches Kriterium, das Sie Verträgen zuweisen müssen, um zu definieren, wie Vertrag erfüllt wird.</span><span class="sxs-lookup"><span data-stu-id="c3ae8-116">A commitment type is a mandatory criterion that you must assign to the agreement to define how the agreement contract will be fulfilled.</span></span> <span data-ttu-id="c3ae8-117">Mit den vier vordefinierten Typen können Sie das Zusageziel des Debitors einrichten (als Menge bzw. Wert).</span><span class="sxs-lookup"><span data-stu-id="c3ae8-117">The four predefined types let you set up the customer's commitment target, expressed as a quantity or a value.</span></span> <span data-ttu-id="c3ae8-118">Der Mengenzusagetyp kann nur auf ein bestimmtes Produkt angewendet werden. Die wertbasierten Typen sind auf den Verkauf bestimmter und unspezifischer Produkte anwendbar.</span><span class="sxs-lookup"><span data-stu-id="c3ae8-118">The quantity commitment type can only be applied to a specific product, but the value-based types are applicable to sales of both specific and non-specific products.</span></span>  
10. <span data-ttu-id="c3ae8-119">Wählen Sie im Feld "Ablaufdatum" Datum auf das Datum fest, ab dem Sie die Vereinbarung abzulaufen soll.</span><span class="sxs-lookup"><span data-stu-id="c3ae8-119">In the Expiration date field, set the date to a future date when you want the agreement to expire.</span></span>
11. <span data-ttu-id="c3ae8-120">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c3ae8-120">Click OK.</span></span>

## <a name="set-up-product-value-commitment-lines"></a><span data-ttu-id="c3ae8-121">Produktwertzusagepositionen einrichten</span><span class="sxs-lookup"><span data-stu-id="c3ae8-121">Set up product value commitment lines</span></span>
1. <span data-ttu-id="c3ae8-122">Klicken Sie auf "Position hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="c3ae8-122">Click Add line.</span></span>
2. <span data-ttu-id="c3ae8-123">Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c3ae8-123">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="c3ae8-124">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="c3ae8-124">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="c3ae8-125">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c3ae8-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c3ae8-126">Der Typ der Zusage, den Sie für die Vereinbarung ausgewählt haben, betrifft die Art der Informationen, die Sie für die Vereinbarungspositionen eingeben können.</span><span class="sxs-lookup"><span data-stu-id="c3ae8-126">The type of commitment that you have chosen for the agreement affects the kind of information you can enter for the agreement lines.</span></span> <span data-ttu-id="c3ae8-127">Für eine wertbasierte Vereinbarung müssen Sie zum Beispiel den Gesamtnettobetrag (in der vereinbarten Währung) für den der Debitor den Kauf von Waren von Ihnen zusagt angeben.</span><span class="sxs-lookup"><span data-stu-id="c3ae8-127">For example, for a value-based agreement you must specify the total net amount (in the agreed currency) for which the customer commits to buys goods from you.</span></span> <span data-ttu-id="c3ae8-128">In diesem Beispiel sind die Felder "Menge" und "Einheit" in der Position nicht verfügbar, da Sie eine Vereinbarung für den Kunden zum Kauf eines bestimmten Wertes eines Produkts erstellten.</span><span class="sxs-lookup"><span data-stu-id="c3ae8-128">In this example the Quantity and Unit fields on the line are unavailable because you’re creating an agreement for the customer to buy a specific value of a product.</span></span>   
5. <span data-ttu-id="c3ae8-129">Im Feld "Nettobetrag" geben Sie den Geldbetrag ein, den der Debitor für den Einkauf zugesagt hat.</span><span class="sxs-lookup"><span data-stu-id="c3ae8-129">In the Net amount field, enter the monetary amount that the customer has committed to buying.</span></span>
6. <span data-ttu-id="c3ae8-130">Geben Sie im Feld "Rabattprozent" einen Prozentwert ein, der für die Auftragspositionen des Debitors gilt, der dieser Vereinbarung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c3ae8-130">In the Discount percent field, enter a percentage value that will apply to the customer's sales order lines that are linked to this agreement.</span></span>
7. <span data-ttu-id="c3ae8-131">Erweitern Sie den Abschnitt "Positionsdetails".</span><span class="sxs-lookup"><span data-stu-id="c3ae8-131">Expand the Line details section.</span></span>
8. <span data-ttu-id="c3ae8-132">Wählen Sie "Ja" im Feld "Maximum wird erzwungen".</span><span class="sxs-lookup"><span data-stu-id="c3ae8-132">Select Yes in the Max is enforced field.</span></span>
    * <span data-ttu-id="c3ae8-133">Die Auswahl von "Maximum wird erzwungen" bedeutet, dass der Gesamtbetrag aller Auftragspositionen, die die Sonderpreise der Zusage verwenden und/oder der Zahlungsbedingungen den auf der Zusage angegeben Betrag nicht überschreiten darf.</span><span class="sxs-lookup"><span data-stu-id="c3ae8-133">Selecting Max is enforced means that the total amount of all the sales order lines that use the commitment's special prices, discounts and/or payment terms must not exceed the amount specified on the commitment.</span></span>  
    * <span data-ttu-id="c3ae8-134">Die minimalen und maximalen Freigabemengen geben einen Wertebereich an, für bei jedem Auftrag verkauft werden muss, der die ausgewählte Vereinbarung verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3ae8-134">The minimum and maximum release amounts specify a range of values that must be sold on each sales order that uses the selected agreement.</span></span>   
9. <span data-ttu-id="c3ae8-135">Erweitern Sie den Kopfbereich "Kaufvertrag".</span><span class="sxs-lookup"><span data-stu-id="c3ae8-135">Expand the Sales agreement header section.</span></span>
    * <span data-ttu-id="c3ae8-136">Solange der Status der Vereinbarung nicht auf "Effektiv" festgelegt ist, können Aufträge nicht dem Vertrag zugeordneten werden. Sie können daher nicht zur Erfüllung dieser Vereinbarung beitragen.</span><span class="sxs-lookup"><span data-stu-id="c3ae8-136">Unless the status of the agreement is set to Effective, sales orders cannot be associated with the agreement and can therefore not contribute to the fulfilment of that agreement.</span></span> <span data-ttu-id="c3ae8-137">Der können den Status zu diesem Zeitpunkt manuell ändern.</span><span class="sxs-lookup"><span data-stu-id="c3ae8-137">You can change the status manually at this stage.</span></span> <span data-ttu-id="c3ae8-138">Allerdings wird der Status normalerweise geändert, wenn die Vereinbarung für den Debitor bestätigt wird.</span><span class="sxs-lookup"><span data-stu-id="c3ae8-138">However, the status would normally be changed when you confirm the agreement for the customer.</span></span>  
10. <span data-ttu-id="c3ae8-139">Klicken Sie im Aktivitätsbereich auf "Kaufvertrag".</span><span class="sxs-lookup"><span data-stu-id="c3ae8-139">On the Action Pane, click Sales agreement.</span></span>
11. <span data-ttu-id="c3ae8-140">Klicken Sie auf Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="c3ae8-140">Click Confirmation.</span></span>
    * <span data-ttu-id="c3ae8-141">Stellen Sie sicher, dass die Option "Vertrag als 'Effektiv' kennzeichnen" auf "Ja" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c3ae8-141">Make sure that the Mark agreement as effective option is set to Yes.</span></span>  
12. <span data-ttu-id="c3ae8-142">Wählen Sie "Ja" im Feld "Bericht drucken" aus.</span><span class="sxs-lookup"><span data-stu-id="c3ae8-142">Select Yes in the Print report field.</span></span>
13. <span data-ttu-id="c3ae8-143">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c3ae8-143">Click OK.</span></span>
14. <span data-ttu-id="c3ae8-144">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c3ae8-144">Close the page.</span></span>
    * <span data-ttu-id="c3ae8-145">Die Vereinbarung ist nun effektiv und Sie können Kundenaufträge mit der Vereinbarung verknüpfen, um diese dem Zusageziel zuzurechnen.</span><span class="sxs-lookup"><span data-stu-id="c3ae8-145">The agreement is now effective and you can start linking the customer's orders to the agreement, to offset against the committed target.</span></span>  

