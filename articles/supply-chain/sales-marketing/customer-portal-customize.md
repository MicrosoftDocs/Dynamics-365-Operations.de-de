---
title: Das Debitorenportal anpassen und verwenden
description: In diesem Thema wird erläutert, wie Sie das Kundenportal anpassen, nachdem es Ihrem System hinzugefügt wurde.
author: dasani-madipalli
manager: tfehr
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e3ab79bc9203309c0cfa1ff18f75580297ae1001
ms.sourcegitcommit: 713b5dfc76a6875d0ba6d86c5cbd585ea502cf9d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2020
ms.locfileid: "3413968"
---
# <a name="customize-and-use-the-customer-portal"></a><span data-ttu-id="7cf50-103">Das Debitorenportal anpassen und verwenden</span><span class="sxs-lookup"><span data-stu-id="7cf50-103">Customize and use the Customer portal</span></span>

<span data-ttu-id="7cf50-104">In diesem Thema werden die verschiedenen Seiten beschrieben, die im Kundenportal sofort verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="7cf50-104">This topic describes the different pages that available in the Customer portal out of the box.</span></span> <span data-ttu-id="7cf50-105">Es wird erklärt, was die Seiten tun und wie Sie sie anpassen können.</span><span class="sxs-lookup"><span data-stu-id="7cf50-105">It explains what the pages do and how you can customize them.</span></span>

<span data-ttu-id="7cf50-106">Das Kundenportal bietet einige vordefinierte Websiten und Aktionen.</span><span class="sxs-lookup"><span data-stu-id="7cf50-106">The Customer portal offers a few webpages and actions out of the box.</span></span> <span data-ttu-id="7cf50-107">Die folgende Sitemap bietet einen Überblick über diese Webseiten und Aktionen sowie die Rollen, die die Aktionen ausführen können.</span><span class="sxs-lookup"><span data-stu-id="7cf50-107">The following site map provides an overview of those webpages and actions, and the roles that can perform the actions.</span></span>

![![Kundenportal-Sitemap](media/customer-portal-site-map.png "Kundenportal-Sitemap")](media/customer-portal-site-map.png "Customer portal site map")

## <a name="typical-customizations"></a><span data-ttu-id="7cf50-109">Typische Anpassungen</span><span class="sxs-lookup"><span data-stu-id="7cf50-109">Typical customizations</span></span>

<span data-ttu-id="7cf50-110">Die folgenden Themen helfen Ihnen beim Erlernen der Grundlagen von Power Apps Portal und wie Sie Portale anpassen können:</span><span class="sxs-lookup"><span data-stu-id="7cf50-110">The following topics will help you learn the basics about Power Apps portals and how you can customize portals:</span></span>

- <span data-ttu-id="7cf50-111">[Arbeiten Sie mit Vorlagen](https://docs.microsoft.com/powerapps/maker/portals/work-with-templates) – Dieses Thema bietet einen allgemeinen Überblick darüber, wie Power Apps Portale funktionieren und wie Sie einfache Anpassungen von Portalen vornehmen können.</span><span class="sxs-lookup"><span data-stu-id="7cf50-111">[Work with templates](https://docs.microsoft.com/powerapps/maker/portals/work-with-templates) – This topic provides a general overview of how Power Apps portals works and how you can do simple customizations of portals.</span></span>
- <span data-ttu-id="7cf50-112">[Portalinhalte verwalten](https://docs.microsoft.com/dynamics365/portals/manage-portal-content) – In diesem Thema wird erläutert, wie Sie den Inhalt verwalten und anpassen können, den Sie in Ihrem Portal anzeigen.</span><span class="sxs-lookup"><span data-stu-id="7cf50-112">[Manage portal content](https://docs.microsoft.com/dynamics365/portals/manage-portal-content) – This topic explains how you can manage and customize the content that you surface in your portal.</span></span>
- <span data-ttu-id="7cf50-113">[Bearbeiten von CSS](https://docs.microsoft.com/powerapps/maker/portals/edit-css) – Mit diesem Thema können Sie komplexere Anpassungen an der Benutzeroberfläche Ihres Portals vornehmen.</span><span class="sxs-lookup"><span data-stu-id="7cf50-113">[Edit CSS](https://docs.microsoft.com/powerapps/maker/portals/edit-css) – This topic helps you make more complex customizations to the user interface (UI) of your portal.</span></span>
- <span data-ttu-id="7cf50-114">[Erstellen Sie ein Thema für Ihr Portal](https://docs.microsoft.com/dynamics365/portals/create-theme) – Mit diesem Thema können Sie ein UI-Thema für Ihr Portal erstellen.</span><span class="sxs-lookup"><span data-stu-id="7cf50-114">[Create a theme for your portal](https://docs.microsoft.com/dynamics365/portals/create-theme) – This topic helps you create a UI theme for your portal.</span></span>
- <span data-ttu-id="7cf50-115">[Erstellen und Anzeigen von Portalinhalten auf einfache Weise](https://docs.microsoft.com/dynamics365/portals/create-expose-portal-content) – In diesem Thema können Sie die zugrunde liegenden Daten und Entitäten verwalten, die Sie für Ihr Portal verwenden.</span><span class="sxs-lookup"><span data-stu-id="7cf50-115">[Create and expose portal content easily](https://docs.microsoft.com/dynamics365/portals/create-expose-portal-content) – This topic helps you manage the underlying data and entities that you use for your portal.</span></span>
- <span data-ttu-id="7cf50-116">[Konfigurieren Sie einen Kontakt für die Verwendung in einem Portal](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) – In diesem Thema wird erläutert, wie Benutzerrollen erstellt und angepasst werden und wie Sicherheit und Authentifizierung in Power Apps Portalen funktionieren.</span><span class="sxs-lookup"><span data-stu-id="7cf50-116">[Configure a contact for use on a portal](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) – This topic explains how to create and customize user roles, and how security and authentication work in Power Apps portals.</span></span>
- <span data-ttu-id="7cf50-117">[Konfigurieren Sie Notizen für Entitätsformulare und Webformulare auf Portalen](https://docs.microsoft.com/powerapps/maker/portals/configure-notes) – In diesem Thema wird erläutert, wie Sie Ihrem Portal Dokumente und zusätzlichen Speicher hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7cf50-117">[Configure notes for entity forms and web forms on portals](https://docs.microsoft.com/powerapps/maker/portals/configure-notes) – This topic explains how to add documents and additional storage to your portal.</span></span>
- <span data-ttu-id="7cf50-118">[Fehlerbehandlung für Portal-Website](https://docs.microsoft.com/powerapps/maker/portals/admin/view-portal-error-log) – In diesem Thema wird erläutert, wie Sie Portalfehlerprotokolle anzeigen und in I Microsoft Azure Blob-Speicherkonto speichern.</span><span class="sxs-lookup"><span data-stu-id="7cf50-118">[Error handling for portal website](https://docs.microsoft.com/powerapps/maker/portals/admin/view-portal-error-log) – This topic explains how to view portal error logs and store them in your Microsoft Azure Blob storage account.</span></span>

## <a name="customize-the-order-creation-process"></a><span data-ttu-id="7cf50-119">Passen Sie den Prozess der Auftragserstellung an</span><span class="sxs-lookup"><span data-stu-id="7cf50-119">Customize the order creation process</span></span>

<span data-ttu-id="7cf50-120">Wenn ein Benutzer eine Bestellung über das Kundenportal abgibt, wird die Bestellung automatisch mit der entsprechenden Dynamics 365 Supply Chain Management Umgebung synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="7cf50-120">When a user submits an order by using the Customer portal, the order is automatically synced to the corresponding Dynamics 365 Supply Chain Management environment.</span></span> <span data-ttu-id="7cf50-121">Da der Benutzer ein externer Kunde ist, werden einige erforderliche Informationen absichtlich vor ihm verborgen.</span><span class="sxs-lookup"><span data-stu-id="7cf50-121">Because the user is an external customer, some required information is intentionally hidden from him or her.</span></span> <span data-ttu-id="7cf50-122">Diese Informationen werden automatisch ausgefüllt, wenn das Formular gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="7cf50-122">This information will automatically be filled in when the form is submitted.</span></span>

<span data-ttu-id="7cf50-123">Dieser Abschnitt zeigt, wie Sie Kontakte einrichten sollten, um Fehler zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="7cf50-123">This section shows how you should set up contacts to avoid errors.</span></span> <span data-ttu-id="7cf50-124">Es werden Felder erläutert, die automatisch festgelegt werden, und wie Sie den Wert dieser Felder bei Bedarf ändern können.</span><span class="sxs-lookup"><span data-stu-id="7cf50-124">It explains fields that are automatically set and how you can modify the value of those fields if you must.</span></span>

### <a name="the-out-of-box-order-creation-process"></a><span data-ttu-id="7cf50-125">Definierten Prozess der Auftragserstellung anpassen</span><span class="sxs-lookup"><span data-stu-id="7cf50-125">The out-of-box order creation process</span></span>

<span data-ttu-id="7cf50-126">Hier sind die Standardschritte zum Absenden eines Auftrags über das Kundenportal.</span><span class="sxs-lookup"><span data-stu-id="7cf50-126">Here are the standard steps for submitting an order from the Customer portal.</span></span>

1. <span data-ttu-id="7cf50-127">Wählen Sie auf der Startseite die Kachel **Auftrag erstellen** zum Öffnen des Assistenten **Auftrag erstellen**.</span><span class="sxs-lookup"><span data-stu-id="7cf50-127">On the home page, select the **Create order** tile to open the **Create Order** wizard.</span></span>
1. <span data-ttu-id="7cf50-128">Auf der Seite **Bestellinformationen** setzen Sie die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="7cf50-128">On the **Order Information** page, set the following fields:</span></span>

    - <span data-ttu-id="7cf50-129">**Angefordertes Empfangsdatum** – Geben Sie das Lieferdatum an.</span><span class="sxs-lookup"><span data-stu-id="7cf50-129">**Requested receipt date** – Specify the date of delivery.</span></span>
    - <span data-ttu-id="7cf50-130">**Lieferadresse** – Geben Sie die Adresse ein, an die die Bestellung geliefert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7cf50-130">**Delivery address** – Enter the address that the order should be delivered to.</span></span>
    - <span data-ttu-id="7cf50-131">**Unternehmen** – Wählen Sie den Namen des Kundenunternehmens.</span><span class="sxs-lookup"><span data-stu-id="7cf50-131">**Company** – Select the name of the customer company.</span></span> <span data-ttu-id="7cf50-132">Dieses Feld wird automatisch für Benutzer ohne Administratorrechte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7cf50-132">This field is automatically set for non-admin users.</span></span>
    - <span data-ttu-id="7cf50-133">**Anforderungsnummer** – Geben Sie die Bestellnummer der Bestellung ein.</span><span class="sxs-lookup"><span data-stu-id="7cf50-133">**Requisition number** – Enter the requisition number of the order.</span></span> <span data-ttu-id="7cf50-134">Dieses Feld ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7cf50-134">This field isn't required.</span></span>
    - <span data-ttu-id="7cf50-135">**Versand nach Land/Region** – Geben Sie das Land oder die Region ein, in die die Artikel geliefert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7cf50-135">**Ship to country/region** – Enter the country or region that the items will be delivered to.</span></span> <span data-ttu-id="7cf50-136">Dieses Feld wird automatisch für Benutzer ohne Administratorrechte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7cf50-136">This field is automatically set for non-admin users.</span></span>

    ![![Auftragsinformationsseite](media/customer-portal-order-information.png "Auftragsinformationsseite")](media/customer-portal-order-information.png "Order Information page")

1. <span data-ttu-id="7cf50-138">Wählen Sie **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="7cf50-138">Select **Next**.</span></span>
1. <span data-ttu-id="7cf50-139">Wählen Sie auf der Seite **Artiekl** **Artikel hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="7cf50-139">On the **Items** page, select **Add Item**.</span></span>

    ![![Artikelseite](media/customer-portal-items.png "Artikelseite")](media/customer-portal-items.png "Items page")

1. <span data-ttu-id="7cf50-141">Im angezeigten Dialogfeld **Artikelinformation** legen Sie die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="7cf50-141">In the **Item Information** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="7cf50-142">**Produktname** – Suchen Sie ein Produkt und wählen Sie es aus, um es der Bestellung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="7cf50-142">**Product Name** – Find and select a product to add to the order.</span></span>
    - <span data-ttu-id="7cf50-143">**Menge** – Geben Sie die Menge des ausgewählten Produkts an.</span><span class="sxs-lookup"><span data-stu-id="7cf50-143">**Quantity** – Enter the quantity of the selected product.</span></span>
    - <span data-ttu-id="7cf50-144">**Einheit** – Geben Sie die Maßeinheit an (z. B. **ea.**, **kg**, oder **Schachtel**).</span><span class="sxs-lookup"><span data-stu-id="7cf50-144">**Unit** – Specify the unit of measure (for example, **ea.**, **kgs**, or **box**).</span></span>
    - <span data-ttu-id="7cf50-145">**Geschätzter Nettobetrag** – Der Wert wird berechnet als der geschätzte Preis des Artikels × die Menge für die ausgewählte Einheit.</span><span class="sxs-lookup"><span data-stu-id="7cf50-145">**Estimated net amount** – The value is calculated as the estimated price of the item × the quantity for the selected unit.</span></span>

    ![![Dialogfeld Artikelinformation](media/customer-portal-item-information.png "Dialogfeld Artikelinformation")](media/customer-portal-item-information.png "Item Information dialog box")

1. <span data-ttu-id="7cf50-147">Wählen Sie **Übermitteln**, um dem Auftrag den Artikel hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="7cf50-147">Select **Submit** to add the item to the order.</span></span>
1. <span data-ttu-id="7cf50-148">Wiederholen Sie die Schritte 4 bis 6, bis Sie alle Artikel hinzugefügt haben, die Sie bestellen möchten.</span><span class="sxs-lookup"><span data-stu-id="7cf50-148">Repeat steps 4 through 6 until you've added all the items that you want to order.</span></span>
1. <span data-ttu-id="7cf50-149">Wenn Sie alle Elemente hinzugefügt haben, wählen Sie **Weiter** auf der Seite **Artikel**.</span><span class="sxs-lookup"><span data-stu-id="7cf50-149">When you've finished adding items, select **Next** on the **Items** page.</span></span>
1. <span data-ttu-id="7cf50-150">Die Seite **Bestellinformationen** zeigt eine Zusammenfassung der Bestellung.</span><span class="sxs-lookup"><span data-stu-id="7cf50-150">The **Order Information** page provides a summary of the order.</span></span> <span data-ttu-id="7cf50-151">Überprüfen Sie den Bestellinhalt und die Lieferdetails.</span><span class="sxs-lookup"><span data-stu-id="7cf50-151">Review the order contents and delivery details.</span></span> <span data-ttu-id="7cf50-152">Wenn alles richtig aussieht, wählen Sie **übermitteln**, um die Bestellung abzuschicken.</span><span class="sxs-lookup"><span data-stu-id="7cf50-152">If everything looks correct, select **Submit** to submit the order.</span></span>

    ![![Auftragsinformationsseite](media/customer-portal-order-submit.png "Auftragsinformationsseite")](media/customer-portal-order-submit.png "Order Information page")

### <a name="standard-data-setup"></a><span data-ttu-id="7cf50-154">Standarddaten einrichten</span><span class="sxs-lookup"><span data-stu-id="7cf50-154">Standard data setup</span></span>

<span data-ttu-id="7cf50-155">Um eine reibungslose Benutzererfahrung zu gewährleisten, füllt das Kundenportal automatisch Werte für mehrere erforderliche Felder aus.</span><span class="sxs-lookup"><span data-stu-id="7cf50-155">To help ensure a smooth user experience, the Customer portal automatically fills in values for several required fields.</span></span> <span data-ttu-id="7cf50-156">Diese Werte basieren auf Informationen im Kontaktdatensatz des Kunden, der die Bestellung abgibt.</span><span class="sxs-lookup"><span data-stu-id="7cf50-156">These values are based on information in the contact record of the customer who is submitting the order.</span></span>

<span data-ttu-id="7cf50-157">Für jeden [Kontaktdatensatz](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts), der zu einem Kunden gehört, der das Kundenportal zum Absenden von Bestellungen verwendet, muss für die folgenden erforderlichen Felder Werte angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7cf50-157">For each [contact record](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) that belongs to a customer who will use the Customer portal to submit orders, values must be specified for the following required fields.</span></span> <span data-ttu-id="7cf50-158">Andernfalls treten Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="7cf50-158">Otherwise, errors will occur.</span></span>

- <span data-ttu-id="7cf50-159">**Unternehmen** – Die juristische Person, zu der der Auftrag gehört</span><span class="sxs-lookup"><span data-stu-id="7cf50-159">**Company** – The legal entity that the order belongs to</span></span>
- <span data-ttu-id="7cf50-160">**Möglicher Kunde** – Das dem ausgewählten Auftrag zugeordnete Debitorenkonto</span><span class="sxs-lookup"><span data-stu-id="7cf50-160">**Potential customer** – The customer account that is associated with the order</span></span>
- <span data-ttu-id="7cf50-161">**Preisliste** – Die benutzerdefinierte Preisliste für den Kunden</span><span class="sxs-lookup"><span data-stu-id="7cf50-161">**Price list** – The custom price list for the customer</span></span>
- <span data-ttu-id="7cf50-162">**Währung** – Die Währung des Preises</span><span class="sxs-lookup"><span data-stu-id="7cf50-162">**Currency** – The currency of the price</span></span>
- <span data-ttu-id="7cf50-163">**Versand nach Land/Region** – Das Land oder die Region eingeben, in die die Artikel geliefert werden sollen</span><span class="sxs-lookup"><span data-stu-id="7cf50-163">**Ship to country/region** – The country or region that the items will be delivered to</span></span>

<span data-ttu-id="7cf50-164">Die folgenden Felder werden automatisch für die Kundenauftragseinheit festgelegt:</span><span class="sxs-lookup"><span data-stu-id="7cf50-164">The following fields are automatically set for the sales order entity:</span></span>

- <span data-ttu-id="7cf50-165">**Sprache** – Die Sprache der Bestellung (standardmäßig wird der Wert aus dem Kontaktdatensatz übernommen.)</span><span class="sxs-lookup"><span data-stu-id="7cf50-165">**Language** – The language of the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="7cf50-166">**Versand nach Land/Region** – Das Land oder die Region, in die die Artikel geliefert werden (standardmäßig wird der Wert aus dem Kontaktdatensatz übernommen.)</span><span class="sxs-lookup"><span data-stu-id="7cf50-166">**Ship to country/region** – The country or region that the items will be delivered to (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="7cf50-167">**Kontaktperson** – Der Benutzer, der kontaktiert werden kann, um Informationen zur Bestellung zu erhalten (standardmäßig wird der Wert aus dem Kontaktdatensatz übernommen.)</span><span class="sxs-lookup"><span data-stu-id="7cf50-167">**Contact person** – The user who can be contacted for information about the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="7cf50-168">**Unternehmen** – Die juristische Person, zu der die Bestellung gehört (standardmäßig wird der Wert aus dem Kontaktdatensatz übernommen.)</span><span class="sxs-lookup"><span data-stu-id="7cf50-168">**Company** – The legal entity that the order belongs to (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="7cf50-169">**Potenzieller Kunde** – Das Kundenkonto, das der Bestellung zugeordnet ist (standardmäßig wird der Wert aus dem Kontaktdatensatz übernommen.)</span><span class="sxs-lookup"><span data-stu-id="7cf50-169">**Potential customer** – The customer account that is associated with the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="7cf50-170">**Kundenrechnung** – Das Kundenkonto, das der Bestellung zugeordnet ist (standardmäßig wird der Wert aus dem Kontaktdatensatz übernommen.)</span><span class="sxs-lookup"><span data-stu-id="7cf50-170">**Invoice customer** – The billing account of the order (The default value is the potential customer from the contact record.)</span></span>
- <span data-ttu-id="7cf50-171">**Kundenauftragsname** – Der Name des Kundenauftrags (Der Standardwert ist **Kundenauftrag** .)</span><span class="sxs-lookup"><span data-stu-id="7cf50-171">**Sales order name** – The name of the sales order (The default value is **sales order**.)</span></span>
- <span data-ttu-id="7cf50-172">**Währung** – Die Währung des Preises (standardmäßig wird der Wert aus dem Kontaktdatensatz übernommen.)</span><span class="sxs-lookup"><span data-stu-id="7cf50-172">**Currency** – The currency of the price (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="7cf50-173">**Preisliste** – Die benutzerdefinierte Preisliste für den Kunden (standardmäßig wird der Wert aus dem Kontaktdatensatz übernommen.)</span><span class="sxs-lookup"><span data-stu-id="7cf50-173">**Price list** – The custom price list for the customer (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="7cf50-174">**Beschreibung der Lieferadresse** – Die Lieferadresse des Kundenauftrags (Der Standardwert ist **Beschreibung der Lieferadresse** .)</span><span class="sxs-lookup"><span data-stu-id="7cf50-174">**Delivery address description** – The delivery address of the sales order (The default value is **delivery address description**.)</span></span>

### <a name="modify-the-order-creation-process"></a><span data-ttu-id="7cf50-175">Den Prozess der Auftragserstellung anpassen</span><span class="sxs-lookup"><span data-stu-id="7cf50-175">Modify the order creation process</span></span>

<span data-ttu-id="7cf50-176">Sie können das Erscheinungsbild und die Benutzeroberfläche des Kundenportals frei ändern, wenn Sie den grundlegenden Prozess zur Auftragserstellung nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="7cf50-176">You can freely modify the appearance and UI of the Customer portal if you don't change the basic order creation process.</span></span> <span data-ttu-id="7cf50-177">Wenn Sie den Prozess der Auftragserstellung ändern möchten, müssen Sie einige Punkte beachten.</span><span class="sxs-lookup"><span data-stu-id="7cf50-177">If you want to change the order creation process, there are a few points that you must keep in mind.</span></span>

<span data-ttu-id="7cf50-178">Entfernen Sie die folgenden Felder nicht aus der Kundenauftragsentität in Common Data Service, weil sie einen Kundenauftrag in dualem Schreiben erstellen müssen:</span><span class="sxs-lookup"><span data-stu-id="7cf50-178">Don't remove the following fields from the sales order entity in Common Data Service, because they are required to create a sales order in dual-write:</span></span>

- <span data-ttu-id="7cf50-179">**Unternehmen** – Die juristische Person, zu der der Auftrag gehört</span><span class="sxs-lookup"><span data-stu-id="7cf50-179">**Company** – The legal entity that the order belongs to</span></span>
- <span data-ttu-id="7cf50-180">**Name** –Der Name des konsolidierten Verkaufsauftrags</span><span class="sxs-lookup"><span data-stu-id="7cf50-180">**Name** – The name of the sales order</span></span>
- <span data-ttu-id="7cf50-181">**Währung** – Die Währung des Preises</span><span class="sxs-lookup"><span data-stu-id="7cf50-181">**Currency** – The currency of the price</span></span>
- <span data-ttu-id="7cf50-182">**Preisliste** – Die benutzerdefinierte Preisliste für den Kunden</span><span class="sxs-lookup"><span data-stu-id="7cf50-182">**Price list** – The custom price list for the customer</span></span>
- <span data-ttu-id="7cf50-183">**Versand nach Land/Region** – Das Land oder die Region eingeben, in die die Artikel geliefert werden sollen</span><span class="sxs-lookup"><span data-stu-id="7cf50-183">**Ship to country/region** – The country or region that the items will be delivered to</span></span>
- <span data-ttu-id="7cf50-184">**Möglicher Kunde** – Das dem ausgewählten Auftrag zugeordnete Debitorenkonto</span><span class="sxs-lookup"><span data-stu-id="7cf50-184">**Potential customer** – The customer account that is associated with the order</span></span>
- <span data-ttu-id="7cf50-185">**Sprache** – Die Sprache der Bestellung (In der Regel ist diese Sprache die Sprache des potenziellen Kunden.)</span><span class="sxs-lookup"><span data-stu-id="7cf50-185">**Language** – The language of the order (Typically, this language is the language of the potential customer.)</span></span>
- <span data-ttu-id="7cf50-186">**Beschreibung der Lieferadresse** – Die Lieferadresse des Kundenauftrags</span><span class="sxs-lookup"><span data-stu-id="7cf50-186">**Delivery address description** – The delivery address of the sales order</span></span>

<span data-ttu-id="7cf50-187">Für Artikel sind folgende Felder erforderlich:</span><span class="sxs-lookup"><span data-stu-id="7cf50-187">For items, the following fields are required:</span></span>

- <span data-ttu-id="7cf50-188">**Produkt** – Das zu bestellende Produkt</span><span class="sxs-lookup"><span data-stu-id="7cf50-188">**Product** – The product to order</span></span>
- <span data-ttu-id="7cf50-189">**Menge** – Die Menge des ausgewählten Produkts</span><span class="sxs-lookup"><span data-stu-id="7cf50-189">**Quantity** – The quantity of the selected product</span></span>
- <span data-ttu-id="7cf50-190">**Einheit** – Die Maßeinheit (z. B. **ea.**, **kg**, oder **Schachtel**)</span><span class="sxs-lookup"><span data-stu-id="7cf50-190">**Unit** – The unit of measure (for example, **ea.**, **kgs**, or **box**)</span></span>
- <span data-ttu-id="7cf50-191">**Versand nach Land/Region** – Das Land oder die Region der Lieferung</span><span class="sxs-lookup"><span data-stu-id="7cf50-191">**Ship to country/region** – The country or region of delivery</span></span>
- <span data-ttu-id="7cf50-192">**Beschreibung der Lieferadresse** – Die Lieferadresse des Kundenauftrags</span><span class="sxs-lookup"><span data-stu-id="7cf50-192">**Delivery address description** – The delivery address of the order</span></span>

<span data-ttu-id="7cf50-193">Sie müssen sicherstellen, dass Ihr Kundenportal irgendwie Werte für alle diese Felder übermittelt.</span><span class="sxs-lookup"><span data-stu-id="7cf50-193">You must make sure that your Customer portal somehow submits values for all these fields.</span></span>

<span data-ttu-id="7cf50-194">Wenn Sie der Seite Felder hinzufügen oder Felder entfernen möchten, lesen Sie [Erstellen oder bearbeiten Sie schnell erstellte Formulare für eine optimierte Dateneingabe](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms).</span><span class="sxs-lookup"><span data-stu-id="7cf50-194">If you want to add fields to the page, or remove fields, see [Create or edit quick create forms for a streamlined data entry experience](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms).</span></span>

<span data-ttu-id="7cf50-195">Wenn Sie ändern möchten, wie Felder voreingestellt sind und wie Werte beim Speichern der Seite festgelegt werden, lesen Sie die folgenden Informationen in der Dokumentation Power Apps Portal:</span><span class="sxs-lookup"><span data-stu-id="7cf50-195">If you want to change how fields are preset and how values are set when the page is saved, see the following information in the Power Apps portals documentation:</span></span>

- [<span data-ttu-id="7cf50-196">Feld vorausfüllen</span><span class="sxs-lookup"><span data-stu-id="7cf50-196">Prepopulate field</span></span>](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-web-form-metadata#prepopulate-field)
- [<span data-ttu-id="7cf50-197">Wert beim Speichern festlegen</span><span class="sxs-lookup"><span data-stu-id="7cf50-197">Set Value On Save</span></span>](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-web-form-metadata#set-value-on-save)

## <a name="customize-the-home-page"></a><span data-ttu-id="7cf50-198">Passen Sie die Startseite an</span><span class="sxs-lookup"><span data-stu-id="7cf50-198">Customize the home page</span></span>

<span data-ttu-id="7cf50-199">Alle Steuerelemente im Kundenportal sind integrierte Power Apps Portal Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="7cf50-199">All the controls in the Customer portal are built-in Power Apps portals controls.</span></span> <span data-ttu-id="7cf50-200">Sie können sie anpassen, indem Sie die folgenden Schritte ausführen [Verfassen Sie eine Seite](https://docs.microsoft.com/powerapps/maker/portals/compose-page) in der Dokumentation Power Apps Portal.</span><span class="sxs-lookup"><span data-stu-id="7cf50-200">You can customize them by following the steps in [Compose a page](https://docs.microsoft.com/powerapps/maker/portals/compose-page) in the Power Apps portals documentation.</span></span>

<span data-ttu-id="7cf50-201">Das einzige benutzerdefinierte Steuerelement, das in der Kundenportalvorlage enthalten ist, wird zum Erstellen der Kacheln auf der Startseite verwendet.</span><span class="sxs-lookup"><span data-stu-id="7cf50-201">The only custom control that is included in the Customer portal template is used to create the tiles on the home page.</span></span>

![![Kacheln auf der Startseite](media/customer-portal-home-page-tiles.png "Kacheln auf der Startseite")](media/customer-portal-home-page-tiles.png "Tiles on the home page")

<span data-ttu-id="7cf50-203">Um die Kacheln auszuführen, führen Sie folgende Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="7cf50-203">To modify the tiles, follow these steps.</span></span>

1. <span data-ttu-id="7cf50-204">Öffnen Sie die [Portal Management App](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-portal).</span><span class="sxs-lookup"><span data-stu-id="7cf50-204">Open the [Portal Management app](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-portal).</span></span>
1. <span data-ttu-id="7cf50-205">Wählen Sie im linken Navigationsbereich **Seitenvorlage** aus.</span><span class="sxs-lookup"><span data-stu-id="7cf50-205">In the navigation pane on the left, select **Page Templates**.</span></span>

    ![![Navigationsbereich der Portalverwaltung](media/customer-portal-nav.png "Navigationsbereich der Portalverwaltung")](media/customer-portal-nav.png "Portal Management navigation pane")

1. <span data-ttu-id="7cf50-207">Wählen Sie die benannte Seitenvorlage aus **Startseite**.</span><span class="sxs-lookup"><span data-stu-id="7cf50-207">Select the page template that is named **Home**.</span></span>
1. <span data-ttu-id="7cf50-208">Im Feld **Webvorlage** wählen Sie den Link **Startseite** aus, um den Quellcode für diese Seite zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7cf50-208">In the **Web Template** field, select the **Home** link to open the source code for that page.</span></span>

    ![![Webvorlagenfeld](media/customer-portal-web-template.png "Webvorlagenfeld")](media/customer-portal-web-template.png "Web Template field")

1. <span data-ttu-id="7cf50-210">Sie sollten jetzt den gesamten Quellcode für die Homepage sehen und können ihn nach Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="7cf50-210">You should now see all the source code for the home page and can modify it as you require.</span></span>

## <a name="resources"></a><span data-ttu-id="7cf50-211">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7cf50-211">Resources</span></span>

<span data-ttu-id="7cf50-212">Weitere Informationen zum Einrichten und Anpassen des Kundenportals finden Sie in den folgenden Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="7cf50-212">To learn more about how you can set up and customize the Customer portal, see the following resources:</span></span>

- [<span data-ttu-id="7cf50-213">Power Apps Portaldokumentation</span><span class="sxs-lookup"><span data-stu-id="7cf50-213">Power Apps portals documentation</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [<span data-ttu-id="7cf50-214">Dokumentation Duales Schreiben</span><span class="sxs-lookup"><span data-stu-id="7cf50-214">Dual-write documentation</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)
- [<span data-ttu-id="7cf50-215">Informationen zum Portallebenszyklus</span><span class="sxs-lookup"><span data-stu-id="7cf50-215">About portal lifecycle</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [<span data-ttu-id="7cf50-216">Aktualisieren Sie ein Portal</span><span class="sxs-lookup"><span data-stu-id="7cf50-216">Upgrade a portal</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [<span data-ttu-id="7cf50-217">Portalkonfiguration migrieren</span><span class="sxs-lookup"><span data-stu-id="7cf50-217">Migrate portal configuration</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [<span data-ttu-id="7cf50-218">Solution Lifecycle Management: Dynamics 365 for Customer Engagement Apps</span><span class="sxs-lookup"><span data-stu-id="7cf50-218">Solution Lifecycle Management: Dynamics 365 for Customer Engagement apps</span></span>](https://www.microsoft.com/download/details.aspx?id=57777)