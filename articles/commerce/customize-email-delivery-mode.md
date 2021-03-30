---
title: Transaktions-E-Mails nach Lieferart anpassen
description: In diesem Thema wird beschrieben, wie Sie benutzerdefinierte E-Mail-Vorlagen für bestimmte Benachrichtigungstypen und Lieferarten in Microsoft Dynamics 365 Commerce einrichten.
author: stuharg
manager: annbe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: d0d96ddb20b2b09751d8c0c0bf8af713de35279a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222632"
---
# <a name="customize-transactional-emails-by-mode-of-delivery"></a><span data-ttu-id="49b57-103">Transaktions-E-Mails nach Lieferart anpassen</span><span class="sxs-lookup"><span data-stu-id="49b57-103">Customize transactional emails by mode of delivery</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="49b57-104">In diesem Thema wird beschrieben, wie Sie benutzerdefinierte E-Mail-Vorlagen für bestimmte Benachrichtigungstypen und Lieferarten in Microsoft Dynamics 365 Commerce einrichten.</span><span class="sxs-lookup"><span data-stu-id="49b57-104">This topic describes how to set up custom email templates for specific notification types and modes of delivery in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="49b57-105">Transaktions-E-Mails können jetzt für eine Kombination eines Benachrichtigungstyps angepasst werden (z. B. **Auftrag erstellt**, **Bestellung verpackt** oder **Bestellung in Rechnung gestellt**) sowie für eine Lieferart (z. B. über Nacht, Abholung im Laden oder Abholung am Straßenrand).</span><span class="sxs-lookup"><span data-stu-id="49b57-105">Transactional emails can now be customized for a combination of a notification type (for example, **Order created**, **Order packed**, or **Order invoiced**) and a mode of delivery (for example, overnight, in-store pickup, or curbside pickup).</span></span> <span data-ttu-id="49b57-106">Mit benutzerdefinierten Transaktions-E-Mails können Einzelhändler ihre Kundenbestellung mit Erfüllungserlebnissen anbieten, die auf die Lieferart der Bestellung zugeschnitten sind.</span><span class="sxs-lookup"><span data-stu-id="49b57-106">Custom transactional emails let retailers provide their customers order with fulfillment experiences that are tailored to the order's mode of delivery.</span></span> <span data-ttu-id="49b57-107">Beispielsweise kann das Ereignis „Bestellung gepackt“ so angepasst werden, dass es Anweisungen zur Abholung am Straßenrand für Kunden enthält, die sich für die Abholung am Straßenrand entscheiden.</span><span class="sxs-lookup"><span data-stu-id="49b57-107">For example, the "order packed" event can be customized so that it provides curbside pickup instructions for customers who choose curbside pickup.</span></span> <span data-ttu-id="49b57-108">Alternativ kann es Informationen zu Spediteur und Lieferinformationen für Kunden bereitstellen, die ihren Auftrag liefern lassen möchten.</span><span class="sxs-lookup"><span data-stu-id="49b57-108">Alternatively, it can provide shipping carrier and delivery information for customers who choose to have their order shipped.</span></span>

> [!NOTE]
> <span data-ttu-id="49b57-109">Um die Funktionalität für benutzerdefinierte Transaktions-E-Mails nutzen zu können, müssen Sie zuerst die Funktion **Transaktions-E-Mail-Vorlagen nach Zustellungsart anpassen** aktivieren, indem Sie in der Commerce-Zentralverwaltung zu **Arbeitsbereiche \> Funktionsverwaltung** wechseln.</span><span class="sxs-lookup"><span data-stu-id="49b57-109">To use the functionality for customized transactional emails, you first must turn on the **Customize transactional email templates by mode of delivery** feature by going to **Workspaces \> Feature management** in Commerce headquarters.</span></span>

<span data-ttu-id="49b57-110">E-Mails können je nach Lieferart für die folgenden Benachrichtungstypen angepasst werden:</span><span class="sxs-lookup"><span data-stu-id="49b57-110">Emails can be customized by mode of delivery for the following notification types:</span></span>

- <span data-ttu-id="49b57-111">**Auftragsstornierung** – Dieser E-Mail-Benachrichtigungstyp ist neu.</span><span class="sxs-lookup"><span data-stu-id="49b57-111">**Order cancellation** – This email notification type is new.</span></span>
- <span data-ttu-id="49b57-112">**Auftrag erstellt**</span><span class="sxs-lookup"><span data-stu-id="49b57-112">**Order created**</span></span>
- <span data-ttu-id="49b57-113">**Auftrag bestätigt**</span><span class="sxs-lookup"><span data-stu-id="49b57-113">**Order confirmed**</span></span>
- <span data-ttu-id="49b57-114">**Auftrag fakturiert** – Dieser E-Mail-Benachrichtigungstyp ist neu.</span><span class="sxs-lookup"><span data-stu-id="49b57-114">**Order invoiced** – This email notification type is new.</span></span> <span data-ttu-id="49b57-115">Er kann anstelle des Benachrichtigungstyps **Auftrag gesendet** verwendet werden, wodurch eine Benachrichtigung für jedes Rechnungsereignis gesendet wird, das die Lieferart Gesendet (nicht Abholung, Mitnehmen oder elektronische Lieferart) hat.</span><span class="sxs-lookup"><span data-stu-id="49b57-115">It can be used instead of the **Order shipped** notification type that will send a notification for any invoice event that has a shipped mode of delivery (not a pickup, carry out, or electronic mode of delivery).</span></span>
- <span data-ttu-id="49b57-116">**Auftrag entnommen**</span><span class="sxs-lookup"><span data-stu-id="49b57-116">**Order picked**</span></span>
- <span data-ttu-id="49b57-117">**Auftrag verpackt**</span><span class="sxs-lookup"><span data-stu-id="49b57-117">**Order packed**</span></span>
- <span data-ttu-id="49b57-118">**Auftrag zur Abholung bereit** – Dieser Benachrichtigungstyp kann nur dann nach Lieferart angepasst werden, wenn die Funktion **Unterstützung für mehrere Lieferarten** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="49b57-118">**Order ready for pickup** – This notification type can be customized by mode of delivery only if the **Support for multiple pickup delivery modes** feature is turned on.</span></span> <span data-ttu-id="49b57-119">In diesem Fall entspricht dieser Benachrichtigungstyp funktional dem Benachrichtigugnstyp **Auftrag verpackt**.</span><span class="sxs-lookup"><span data-stu-id="49b57-119">In that case, this notification type is functionally equivalent to the **Order packed** notification type.</span></span>
- <span data-ttu-id="49b57-120">**Zahlung fehlgeschlagen**</span><span class="sxs-lookup"><span data-stu-id="49b57-120">**Payment failed**</span></span>
- <span data-ttu-id="49b57-121">**Ersatzauftrag erstellt**</span><span class="sxs-lookup"><span data-stu-id="49b57-121">**Replacement order created**</span></span>

## <a name="configure-email-templates-for-specific-modes-of-delivery"></a><span data-ttu-id="49b57-122">E-Mail-Vorlagen für bestimmte Lieferarten konfigurieren</span><span class="sxs-lookup"><span data-stu-id="49b57-122">Configure email templates for specific modes of delivery</span></span>

<span data-ttu-id="49b57-123">Bei diese Prozedur wird davon ausgegangen, dass Sie bereits Ihre neuen, benutzerdefinierten E-Mail-Vorlagen erstellt und sie der Seite **E-Mail-Vorlagen der Organisation** hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="49b57-123">For this procedure, the assumption is that you've already created your new, custom email templates and added them to the **Organization email templates** page.</span></span> <span data-ttu-id="49b57-124">Informationen zum Erstellen und Hochladen von E-Mail-Vorlagen finden Sie unter [E-Mail-Vorlagen für Transaktionsereignisse erstellen](email-templates-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="49b57-124">For information about how to create and upload email templates, see [Create email templates for transactional events](email-templates-transactions.md).</span></span>

<span data-ttu-id="49b57-125">Führen Sie die folgenden Schritte aus, um E-Mail-Vorlagen für bestimmte Lieferarten in der Commerce-Zentralverwaltung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="49b57-125">To configure email templates for specific modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="49b57-126">Wechseln Sie zum **Commerce-E-Mail-Benachrichtigungsprofil**.</span><span class="sxs-lookup"><span data-stu-id="49b57-126">Go to **Commerce email notification profile**.</span></span>
1. <span data-ttu-id="49b57-127">Unter **Einstellungen für Retail-Ereignisbenachrichtigungen** wählen Sie einen vorhandenen Benachrichtigungstyp aus.</span><span class="sxs-lookup"><span data-stu-id="49b57-127">Under **Retail event notification settings**, select an existing notification type.</span></span>
1. <span data-ttu-id="49b57-128">Während der Benachrichtigungstyp noch ausgewählt ist, wählen Sie **Lieferarten konfigurieren** aus.</span><span class="sxs-lookup"><span data-stu-id="49b57-128">While the notification type is still selected, select **Configure modes of delivery**.</span></span>
1. <span data-ttu-id="49b57-129">Wählen Sie im Dialogfeld **Lieferarten** die Option **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="49b57-129">In the **Modes of delivery** dialog box, select **New**.</span></span>
1. <span data-ttu-id="49b57-130">Wählen Sie in der neuen Zeile im Feld **Lieferart** eine Lieferart aus.</span><span class="sxs-lookup"><span data-stu-id="49b57-130">In the new row, in the **Mode of delivery** field, select a mode of delivery.</span></span>
1. <span data-ttu-id="49b57-131">Im Feld **E-Mail-ID** wählen Sie die E-Mail-Vorlage aus, die der Lieferart zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="49b57-131">In the **Email ID** field, select the email template to map to the mode of delivery.</span></span>
1. <span data-ttu-id="49b57-132">Aktivieren Sie das Kontrollkästchen **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="49b57-132">Select the **Active** check box.</span></span>
1. <span data-ttu-id="49b57-133">Wiederholen Sie die Schritte 4 bis 7, um weitere Lieferarten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="49b57-133">Repeat steps 4 through 7 to add more modes of delivery.</span></span>
1. <span data-ttu-id="49b57-134">Wählen Sie abschließend **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="49b57-134">When you've finished, select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="49b57-135">Wenn in verschiedenen Positionen in einem Auftrag mehr als eine Lieferart vorhanden sind, wird die Standardvorlage verwendet.</span><span class="sxs-lookup"><span data-stu-id="49b57-135">When more than one mode of delivery is present across lines in a sales order, the default template will be used.</span></span> <span data-ttu-id="49b57-136">Die Standardvorlage ist die Vorlage, die dem Benachrichtigungstyp auf der Seite **Commerce-E-Mail-Benachrichtigungsprofil** zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="49b57-136">The default template is the template that is mapped to the notification type on the **Commerce email notification profile** page.</span></span>
> - <span data-ttu-id="49b57-137">Wenn ein Auftrag eine Lieferart hat, die nicht für eine benutzerdefinerte E-Mail-Vorlage konfiguriert wurde, wird die standardmäßige E-Mail-Vorlage verwendet.</span><span class="sxs-lookup"><span data-stu-id="49b57-137">If a sales order has a mode of delivery that hasn't been configured for a custom email template, the default email template will be used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="49b57-138">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="49b57-138">Additional resources</span></span>

[<span data-ttu-id="49b57-139">Callcenteraufträge erstellen</span><span class="sxs-lookup"><span data-stu-id="49b57-139">Create call center orders</span></span>](tasks/create-call-center-orders.md)

[<span data-ttu-id="49b57-140">Lieferart in POS ändern</span><span class="sxs-lookup"><span data-stu-id="49b57-140">Change mode of delivery in POS</span></span>](pos-change-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]