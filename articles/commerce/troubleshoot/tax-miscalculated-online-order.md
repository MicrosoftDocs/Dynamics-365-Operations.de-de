---
title: Falsch berechnete Steuern auf Onlinebestellungen
description: Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn Steuern auf Onlinebestellungen falsch berechnet werden oder die Steuergruppe in der Verkaufsposition nicht richtig festgelegt ist.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7f71add679e1d24f80db8ce3990058b591128ec1
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801410"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a><span data-ttu-id="455a1-103">Falsch berechnete Steuern auf Onlinebestellungen</span><span class="sxs-lookup"><span data-stu-id="455a1-103">Taxes on online orders are incorrectly calculated</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="455a1-104">Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn Steuern auf Onlinebestellungen falsch berechnet werden oder die Steuergruppe in der Verkaufsposition nicht richtig festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="455a1-104">This topic provides troubleshooting guidance that can help when taxes on online orders are incorrectly calculated, or when the tax group on the sales line isn't correctly set.</span></span>

## <a name="description"></a><span data-ttu-id="455a1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="455a1-105">Description</span></span>

<span data-ttu-id="455a1-106">Wenn ein E-Commerce-Auftrag aufgegeben wird, werden die Steuern falsch berechnet oder die Steuergruppe in der Verkaufsposition ist falsch festgelegt.</span><span class="sxs-lookup"><span data-stu-id="455a1-106">When an e-commerce order is placed, the taxes are incorrectly calculated, or the tax group on the sales line is incorrectly set.</span></span>

## <a name="resolution"></a><span data-ttu-id="455a1-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="455a1-107">Resolution</span></span>

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a><span data-ttu-id="455a1-108">Die Mehrwertsteuer für ein Einzelhandelsgeschäft in der Commerce-Zentralverwaltung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="455a1-108">Configure the sales tax for a retail store in Commerce headquarters</span></span>

<span data-ttu-id="455a1-109">Befolgen Sie diese Schritte, um die Mehrwertsteuer für ein Einzelhandelsgeschäft in der Commerce-Zentralverwaltung zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="455a1-109">To configure the sales tax for a retail store in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="455a1-110">Rufen Sie **Retail und Commerce \> Kanäle \> Alle Shops** auf.</span><span class="sxs-lookup"><span data-stu-id="455a1-110">Go to **Retail and Commerce \> Channels \> All stores**.</span></span>
1. <span data-ttu-id="455a1-111">Wählen Sie das Geschäft aus, für das die Mehrwertsteuer konfiguriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="455a1-111">Select the store to configure sales tax for.</span></span>
1. <span data-ttu-id="455a1-112">Konfigurieren Sie im Inforegister **Allgemein** des Abschnitts **Mehrwertsteuer** die Mehrwertsteuerinformationen für den Shop.</span><span class="sxs-lookup"><span data-stu-id="455a1-112">On the **General** FastTab, in the **Sales tax** section, configure the sales tax information for the store.</span></span>

> [!NOTE]
> <span data-ttu-id="455a1-113">Bei der Produktabholung aus einem Shop stammt die Steuergruppe von dem Shop, der für die Abholung ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="455a1-113">For product pickup from a store, the tax group comes from the store that is selected for pickup.</span></span> <span data-ttu-id="455a1-114">Weitere Informationen finden Sie unter [Festlegen anderer Steueroptionen für Shops](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span><span class="sxs-lookup"><span data-stu-id="455a1-114">For more information, see [Set other tax options for stores](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a><span data-ttu-id="455a1-115">Die Mehrwertsteuer für eine Debitorenadresse in der Commerce-Zentralverwaltung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="455a1-115">Configure the sales tax for a customer's address in Commerce headquarters</span></span>

<span data-ttu-id="455a1-116">Befolgen Sie diese Schritte, um die Mehrwertsteuer für eine Debitorenadresse in der Commerce-Zentralverwaltung zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="455a1-116">To configure the sales tax for a customer's address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="455a1-117">Gehen Sie zu **Debitorenkonten \> Debitoren \> Alle Debitoren**.</span><span class="sxs-lookup"><span data-stu-id="455a1-117">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="455a1-118">Wählen Sie den Debitor aus, für den die Mehrwertsteuer konfiguriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="455a1-118">Select the customer to configure sales taxes for.</span></span>
1. <span data-ttu-id="455a1-119">Wählen Sie im Inforegister **Adressen** die Adresse aus, für die die Mehrwertsteuer konfiguriert werden soll. Wählen Sie **Weitere Optionen** und anschließend **Erweitert** aus.</span><span class="sxs-lookup"><span data-stu-id="455a1-119">On the **Addresses** FastTab, select the address to configure sales taxes for, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="455a1-120">Wählen Sie auf der Registerkarte **Allgemein** die Option **Steuergruppe** aus.</span><span class="sxs-lookup"><span data-stu-id="455a1-120">On the **General** FastTab, select the **Tax group**.</span></span>
1. <span data-ttu-id="455a1-121">Wählen Sie im Feld **Mehrwertsteuer** den entsprechenden Wert aus.</span><span class="sxs-lookup"><span data-stu-id="455a1-121">In the **Sales tax** field, select the appropriate value.</span></span>

> [!NOTE]
> <span data-ttu-id="455a1-122">Bei mehrwertsteuerpflichtigem Versand der Debitorenadresse bestimmt die Lieferadresse der Position die Steuergruppe für die Position.</span><span class="sxs-lookup"><span data-stu-id="455a1-122">For shipping that involves sales tax on the customer's address, the delivery address of the line determines the tax group for the line.</span></span> <span data-ttu-id="455a1-123">Wenn der Debitor an eine vorhandene Adresse versendet, für die bereits eine Steuergruppe konfiguriert ist, wird die vorhandene Steuergruppe verwendet.</span><span class="sxs-lookup"><span data-stu-id="455a1-123">If the customer is shipping to an existing address that has a tax group that is already configured, the existing tax group will be used.</span></span> <span data-ttu-id="455a1-124">Standardmäßig haben Adressen beim Erstellen keine Steuergruppe.</span><span class="sxs-lookup"><span data-stu-id="455a1-124">By default, addresses don't have a tax group when they are created.</span></span>

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a><span data-ttu-id="455a1-125">Allgemeine Mehrwertsteuergruppen in der Commerce-Zentralverwaltung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="455a1-125">Configure general sales tax groups in Commerce headquarters</span></span>

<span data-ttu-id="455a1-126">Befolgen Sie diese Schritte, um allgemeine Mehrwertsteuergruppen in der Commerce-Zentralverwaltung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="455a1-126">To configure general sales tax groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="455a1-127">Rufen Sie **Steuer \> Indirekte Steuern \> Mehrwertsteuer \> Mehrwertsteuergruppen** auf.</span><span class="sxs-lookup"><span data-stu-id="455a1-127">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax group**.</span></span>
1. <span data-ttu-id="455a1-128">Wählen Sie in der linken Navigation die zu konfigurierende Steuergruppe aus.</span><span class="sxs-lookup"><span data-stu-id="455a1-128">In the left navigation, select the tax group to configure.</span></span>
1. <span data-ttu-id="455a1-129">Konfigurieren Sie im Inforegister **Auf Adresse des Einzelhandels bezogene Steuer** die Steuern für die Mehrwertsteuergruppe.</span><span class="sxs-lookup"><span data-stu-id="455a1-129">On the **Retail destination based tax** FastTab, configure the taxes for the sales tax group.</span></span>

> [!NOTE]
> <span data-ttu-id="455a1-130">Bei Versand ohne Mehrwertsteuer der Debitorenadresse bestimmen die Lieferadresse der Position sowie die adressbezogenen Steuern, die für die Steuergruppe konfiguriert sind, die Steuergruppe.</span><span class="sxs-lookup"><span data-stu-id="455a1-130">For shipping that doesn't involve sales tax on the customer's address, the delivery address of the line and the destination-based taxes that are configured for the tax group determine the tax group.</span></span> <span data-ttu-id="455a1-131">Weitere Informationen finden Sie unter [Steuern für Online-Shops auf der Grundlage des Ziels einrichten](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span><span class="sxs-lookup"><span data-stu-id="455a1-131">For more information, see [Set up taxes for online stores based on destination](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="455a1-132">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="455a1-132">Additional resources</span></span>

[<span data-ttu-id="455a1-133">Mehrwertsteuer für Onlinebestellungen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="455a1-133">Configure sales tax for online orders</span></span>](../sales-tax-config.md)
