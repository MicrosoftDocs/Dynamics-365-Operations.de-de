---
title: Abholinformationsmodul
description: Dieses Thema behandelt das Abholinformationsmodul und beschreibt, wie es zu Auftragsabschlussseiten in Microsoft Dynamics 365 Commerce hinzugefügt wird.
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-09021
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 61b97d72b6a397737c10476cd6c02764e60f10b1
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665347"
---
# <a name="pickup-information-module"></a><span data-ttu-id="e3fa0-103">Abholinformationsmodul</span><span class="sxs-lookup"><span data-stu-id="e3fa0-103">Pickup information module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e3fa0-104">Dieses Thema behandelt das Abholinformationsmodul und beschreibt, wie es zu Auftragsabschlussseiten in Microsoft Dynamics 365 Commerce hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="e3fa0-104">This topic covers the pickup information module and describes how to add it to checkout pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e3fa0-105">Das Abholinformationsmodul kann in einem Auftragsabschlussmodul verwendet werden, um Auftragsabholinformationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e3fa0-105">The pickup information module can be used in a checkout module to show order pickup information.</span></span> <span data-ttu-id="e3fa0-106">Kunden können verfügbare Abholtermine und Zeitfenster anzeigen und dann einen geeigneten Zeitpunkt für die Abholung ihres Auftrags auswählen.</span><span class="sxs-lookup"><span data-stu-id="e3fa0-106">Customers can view available pickup dates and time slots, and then select a suitable time to pick up their order.</span></span> <span data-ttu-id="e3fa0-107">Beispielsweise kann ein Kunde auswählen, einen Auftrag um 15:00 Uhr am 21. März vom Geschäft in San Francisco abzuholen.</span><span class="sxs-lookup"><span data-stu-id="e3fa0-107">For example, a customer can choose to pick up an order at 3 PM on March 21 from the San Francisco store.</span></span>

<span data-ttu-id="e3fa0-108">Die Abholzeitfenster für die entsprechenden Geschäfte müssen in der Commerce-Zentralverwaltung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="e3fa0-108">Pickup time slots for the appropriate stores must be configured in Commerce headquarters.</span></span> <span data-ttu-id="e3fa0-109">Weitere Informationen finden Sie unter [Zeitfenster für die Kundenabholung erstellen und aktualisieren](dev-itpro/pickup-timeslots.md).</span><span class="sxs-lookup"><span data-stu-id="e3fa0-109">For more information, see [Create and update time slots for customer pickup](dev-itpro/pickup-timeslots.md).</span></span>

<span data-ttu-id="e3fa0-110">Wenn ein Abholinformationsmodul auf einer Auftragsabschlussseite erstellt wird, aber keine Zeitfenster für das Geschäft definiert sind, das für die Abholung ausgewählt wird, zeigt das Modul Informationen an, aber der Benutzer kann keine Zeitfenster auswählen.</span><span class="sxs-lookup"><span data-stu-id="e3fa0-110">If a pickup information module is created on a checkout page, but no time slots are defined for the store that is selected for pickup, the module will show information, but the user won't be able to select any time slots.</span></span> <span data-ttu-id="e3fa0-111">Zeitfenster sind optional und nicht erforderlich, um einen Auftrag zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="e3fa0-111">Time slots are optional and aren't required to place an order.</span></span>

<span data-ttu-id="e3fa0-112">Wenn mehrere Artikel für die Abholung in mehreren Filialen ausgewählt werden, ermöglicht das Abholinformationsmodul es dem Benutzer, ein Zeitfenster für jede Filiale auszuwählen, vorausgesetzt diese Zeitfenster sind für diese verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e3fa0-112">If multiple items are selected for pickup across multiple stores, the pickup information module will let the user select a time slot for each store, provided that time slots are available for it.</span></span>

> [!NOTE]
> <span data-ttu-id="e3fa0-113">Unterstützung für Zeitfenster und das Auftragsabschluss-Abholinformationsmodul ist in Dynamics 365 Commerce Version 10.0.15 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e3fa0-113">Support for time slots and the checkout pickup information module is available in Dynamics 365 Commerce version 10.0.15 and later.</span></span>

<span data-ttu-id="e3fa0-114">Die folgende Abbildung zeigt ein Beispiel für die Auswahl eines Zeitfensters über das Abholinformationsmodul auf einer Auftragsabschlussseite.</span><span class="sxs-lookup"><span data-stu-id="e3fa0-114">The following illustration shows an example of time slot selection through the pickup information module on a checkout page.</span></span>

![Beispiel eines Abholinformationsmoduls auf einer Auftragsabschlussseite](./dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="module-properties"></a><span data-ttu-id="e3fa0-116">Moduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="e3fa0-116">Module properties</span></span>

- <span data-ttu-id="e3fa0-117">**Überschrift** – Geben Sie eine Überschrift für das Modul ein.</span><span class="sxs-lookup"><span data-stu-id="e3fa0-117">**Heading** – Enter a heading for the module.</span></span>

## <a name="show-time-slot-information-after-an-order-is-placed"></a><span data-ttu-id="e3fa0-118">Zeigen Sie Zeitfensterinformationen an, nachdem ein Auftrag erteilt wurde</span><span class="sxs-lookup"><span data-stu-id="e3fa0-118">Show time slot information after an order is placed</span></span>

<span data-ttu-id="e3fa0-119">Nachdem ein Auftrag erstellt wurde, können Informationen zum ausgewählten Zeitfenster im [Auftragsbestätigungsmodul](order-confirmation-module.md) und im [Auftragsdetailmodul](account-management.md#order-details-page) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e3fa0-119">After an order is placed, information about the selected time slot can be viewed in the [order confirmation module](order-confirmation-module.md) and the [order details module](account-management.md#order-details-page).</span></span> <span data-ttu-id="e3fa0-120">Diese beiden Module haben die Eigenschaft **Zeitfensterinformationen anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="e3fa0-120">Both these modules have a **Show timeslot information** property.</span></span> <span data-ttu-id="e3fa0-121">Bevor sie das ausgewählte Zeitfenster während des Auftragsprozesses anzeigen können, muss diese Eigenschaft auf **True** festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="e3fa0-121">Before they can show the selected time slot during the order process, this property must be set to **True**.</span></span>

## <a name="add-a-checkout-pickup-information-module-to-a-page"></a><span data-ttu-id="e3fa0-122">Ein Auftragsabholinformationsmodul zu einer Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="e3fa0-122">Add a checkout pickup information module to a page</span></span>

<span data-ttu-id="e3fa0-123">Anweisungen zum Hinzufügen eines Abholinformationsmoduls zu einer Auftragsabschlussseite und zum Festlegen der erforderlichen Eigenschaften finden Sie unter [Auftragsabschlussmodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="e3fa0-123">For instructions about how to add a pickup information module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="e3fa0-124">Die folgende Abbildung zeigt ein Beispiel für eine E-Commerce-Auftragsabschlussseite, die Zeitfenster für Abholpositionsartikel enthält.</span><span class="sxs-lookup"><span data-stu-id="e3fa0-124">The following illustration shows an example of an e-Commerce checkout page that includes time slots for pickup line items.</span></span>

![Beispiel für eine E-Commerce-Auftragsabschlussseite, die Zeitfenster für Abholpositionen enthält](./dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a><span data-ttu-id="e3fa0-126">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e3fa0-126">Additional resources</span></span>

[<span data-ttu-id="e3fa0-127">Zeitfenster für die Kundenabholung erstellen und aktualisieren</span><span class="sxs-lookup"><span data-stu-id="e3fa0-127">Create and update time slots for customer pickup</span></span>](dev-itpro/pickup-timeslots.md)

[<span data-ttu-id="e3fa0-128">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="e3fa0-128">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="e3fa0-129">Auftragsbestätigungsmodul</span><span class="sxs-lookup"><span data-stu-id="e3fa0-129">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="e3fa0-130">Auftragsdetailmodul</span><span class="sxs-lookup"><span data-stu-id="e3fa0-130">Order details module</span></span>](account-management.md)
