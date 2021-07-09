---
title: Kunden-Check-in-Benachrichtigungen im Point of Sale (POS) aktivieren
description: Dieses Thema beschreibt, wie Sie in Point of Sale (POS) Microsoft Dynamics 365 Commerce Check-In-Benachrichtigungen für Debitor aktivieren können.
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b42dc7766f8a69a7409c28d21b49cc96eca18dd4
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271424"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a><span data-ttu-id="2c213-103">Kunden-Check-in-Benachrichtigungen im Point of Sale (POS) aktivieren</span><span class="sxs-lookup"><span data-stu-id="2c213-103">Enable customer check-in notifications in point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2c213-104">Dieses Thema beschreibt, wie Sie in Point of Sale (POS) Microsoft Dynamics 365 Commerce Check-In-Benachrichtigungen für Debitor aktivieren können.</span><span class="sxs-lookup"><span data-stu-id="2c213-104">This topic describes how to enable customer check-in notifications in Microsoft Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="2c213-105">Unternehmen können in ihren „Bestellung bereit zur Abholung“-E-Mails einen Link oder eine Schaltfläche bereitstellen, mit dem/der der Debitor dem Geschäft mitteilen kann, dass er auf dem Gelände ist und darauf wartet, dass sein Paket zu ihm gebracht wird.</span><span class="sxs-lookup"><span data-stu-id="2c213-105">In their "order ready for pickup" emails, organizations can provide a link or button that lets customers notify the store that they are on the premises and waiting for their package to be brought out to them.</span></span> <span data-ttu-id="2c213-106">Der Debitor erhält dann eine Check-in-Bestätigung, und die Filiale erhält eine Benachrichtigung als Aufgabe in ihrer POS-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="2c213-106">Customers then receive a check-in confirmation, and the store receives a notification as a task in its POS application.</span></span> <span data-ttu-id="2c213-107">Diese Aufgabe dient als Aufforderung an einen Vertriebsmitarbeiter, den Auftrag an das Fahrzeug des Debitors zu liefern.</span><span class="sxs-lookup"><span data-stu-id="2c213-107">This task serves as a prompt for a sales associate to deliver the order to the customer's vehicle.</span></span> <span data-ttu-id="2c213-108">Daher muss der Debitor den Laden nicht betreten.</span><span class="sxs-lookup"><span data-stu-id="2c213-108">Therefore, the customer doesn't have to enter the store.</span></span>

<span data-ttu-id="2c213-109">Der Workflow für das Einchecken des Debitors kann auch so konfiguriert werden, dass zusätzliche Informationen vom Debitor erfasst werden, z. B. die Parkplatznummer, Marke, Modell und Farbe des Fahrzeugs sowie Lieferanweisungen.</span><span class="sxs-lookup"><span data-stu-id="2c213-109">The customer check-in workflow can also be configured to collect additional information from customers, such as their parking spot number, the make, model, and color of their vehicle, and delivery instructions.</span></span> <span data-ttu-id="2c213-110">Der Verkäufer kann diese Informationen verwenden, um die Auftragserfüllung zu erleichtern.</span><span class="sxs-lookup"><span data-stu-id="2c213-110">The retail store attendant can use this information to facilitate order fulfillment.</span></span>

## <a name="enable-customer-check-in"></a><span data-ttu-id="2c213-111">Aktivieren Sie den Kunden-Check-in</span><span class="sxs-lookup"><span data-stu-id="2c213-111">Enable customer check-in</span></span>

<span data-ttu-id="2c213-112">Wenn die Funktion zum Einchecken des Debitors eingeschaltet ist, generiert Commerce eine Auftragsbestätigungs-ID (auch bekannt als Kanalreferenz-ID).</span><span class="sxs-lookup"><span data-stu-id="2c213-112">When the customer check-in feature is turned on, Commerce generates an order confirmation ID (also known as the channel reference ID).</span></span> <span data-ttu-id="2c213-113">Es generiert auch Auftragsbestätigungs-IDs für Aufträge, die über Point of Sale (POS) oder Call-Center-Kanäle erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2c213-113">It also generates order confirmation IDs for orders that are created through point of sale (POS) or call center channels.</span></span> 

<span data-ttu-id="2c213-114">Um die Funktion zum Einchecken von Debitor in der Commerce-Zentrale zu aktivieren, führen Sie diese Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="2c213-114">To turn on the customer check-in feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="2c213-115">Wechseln Sie zu **Arbeitsbereiche \> Verwaltung von Funktionen**.</span><span class="sxs-lookup"><span data-stu-id="2c213-115">Go to **Workspaces \> Feature management**.</span></span>
2. <span data-ttu-id="2c213-116">Suchen Sie nach der Funktion **Kanalübergreifend ein konsistentes Kanalreferenz-ID-Format generieren**.</span><span class="sxs-lookup"><span data-stu-id="2c213-116">Search for the **Generate a consistent channel reference ID format across channels** feature.</span></span> 
3. <span data-ttu-id="2c213-117">Wählen Sie die Funktion aus und wählen Sie dann **Jetzt aktivieren** im Eigenschaftenfenster.</span><span class="sxs-lookup"><span data-stu-id="2c213-117">Select the feature, and then select **Enable now** in the properties pane.</span></span> 

## <a name="create-a-check-in-confirmation-page"></a><span data-ttu-id="2c213-118">Erstellen Sie eine Check-in-Bestätigungsseite</span><span class="sxs-lookup"><span data-stu-id="2c213-118">Create a check-in confirmation page</span></span>

<span data-ttu-id="2c213-119">Auf Ihrer E-Commerce-Site müssen Sie eine neue Seite erstellen, die als Check-in-Bestätigung dienen soll.</span><span class="sxs-lookup"><span data-stu-id="2c213-119">On your e-commerce site, you must create a new page that will serve as the check-in confirmation experience.</span></span> <span data-ttu-id="2c213-120">Durch zusätzliche Konfiguration kann die Seite auch ein Formular enthalten, das zusätzliche Informationen vom Debitor sammelt, um die Auftragsabwicklung zu erleichtern.</span><span class="sxs-lookup"><span data-stu-id="2c213-120">Through additional configuration, the page can also include a form that collects additional information from customers to facilitate order fulfillment.</span></span> <span data-ttu-id="2c213-121">Informationen zum Festlegen der Seite und des Moduls finden Sie unter [Modul zum Einchecken von Kunden](check-in-pickup-module.md).</span><span class="sxs-lookup"><span data-stu-id="2c213-121">For information about how to set up the page and module, see [Customer check-in module](check-in-pickup-module.md).</span></span>

## <a name="configure-the-transactional-email-template"></a><span data-ttu-id="2c213-122">Konfigurieren Sie die E-Mail-Vorlage für die Transaktion</span><span class="sxs-lookup"><span data-stu-id="2c213-122">Configure the transactional email template</span></span>

<span data-ttu-id="2c213-123">Sie müssen einen **Ich bin hier**-Link oder eine Schaltfläche in die Vorlage für die Transaktions-E-Mail einfügen, die Debitor erhält, wenn seine Bestellung zur Abholung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="2c213-123">You must add an **I am here** link or button to the template for the transactional email that customers receive when their order is ready for pickup.</span></span> <span data-ttu-id="2c213-124">Über diesen Link oder diese Schaltfläche benachrichtigt der Debitor die Filiale, dass er angekommen ist, um seine Bestellung zu entnehmen.</span><span class="sxs-lookup"><span data-stu-id="2c213-124">Customers will use this link or button to notify the store that they have arrived to pick up their order.</span></span> 

<span data-ttu-id="2c213-125">Fügen Sie der Vorlage den Link oder die Schaltfläche hinzu, der/die dem Meldungstyp **Verpackung abgeschlossen** und der Lieferart zugeordnet ist, die Sie für die Auftragsabwicklung an der Bordsteinkante verwenden.</span><span class="sxs-lookup"><span data-stu-id="2c213-125">Add the link or button to the template that is mapped to the **Packing completed** notification type and the mode of delivery that you're using for curbside order fulfillment.</span></span> <span data-ttu-id="2c213-126">Erstellen Sie in der Vorlage einen HTML-Link oder eine Schaltfläche, die auf die URL der von Ihnen erstellten Check-in-Bestätigungsseite verweist.</span><span class="sxs-lookup"><span data-stu-id="2c213-126">In the template, create an HTML link or button that points to the URL of the check-in confirmation page that you created.</span></span> <span data-ttu-id="2c213-127">Hier ist ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="2c213-127">Here is an example.</span></span>

```
<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%channelreferenceid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>
```
<span data-ttu-id="2c213-128">Weitere Informationen zur Konfiguration von E-Mail-Vorlagen finden Sie unter [Anpassen von Transaktions-E-Mails nach Versandart](customize-email-delivery-mode.md).</span><span class="sxs-lookup"><span data-stu-id="2c213-128">For more information about how to configure email templates, see [Customize transactional emails by mode of delivery](customize-email-delivery-mode.md).</span></span> 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a><span data-ttu-id="2c213-129">Eine Check-in-Bestätigungsaufgabe wird in POS erstellt</span><span class="sxs-lookup"><span data-stu-id="2c213-129">A check-in confirmation task is created in POS</span></span>

<span data-ttu-id="2c213-130">Nachdem ein Kunde die Filiale benachrichtigt hat, dass er zur Abholung anwesend ist, erhält er eine Eincheck-Bestätigung und es wird eine Aufgabe in der Aufgabenliste in POS für die Filiale erstellt, in der der Kunde die Bestellung abholt.</span><span class="sxs-lookup"><span data-stu-id="2c213-130">After a customer notifies the store that they are present for pickup, they receive a check-in confirmation notification, and a task is created in the tasks list in POS for the store where the customer is picking up the order.</span></span> <span data-ttu-id="2c213-131">Die Aufgabe enthält alle Debitor- und Auftragsinformationen, die zur Erfüllung des Auftrags erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="2c213-131">The task contains all the customer and order information that is required to fulfill the order.</span></span> <span data-ttu-id="2c213-132">In der Aufgabe zeigt das Anleitungsfeld alle Informationen an, die vom Debitor über das Formular für zusätzliche Informationen erfasst wurden.</span><span class="sxs-lookup"><span data-stu-id="2c213-132">In the task, the instructions field shows any information that was collected from the customer through the additional information form.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="2c213-133">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2c213-133">Additional resources</span></span>

[<span data-ttu-id="2c213-134">Scheck für Abholmodul</span><span class="sxs-lookup"><span data-stu-id="2c213-134">Check-in for pickup module</span></span>](check-in-pickup-module.md)
