---
title: Auftrag aus einem anderen Shop versenden
description: In diesem Thema wird beschrieben die Funktion Belastung senden.
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 797058bdbbdb63a08eb35034ffe3c913307f38df
ms.openlocfilehash: 41434614b01f9a00f2b8a56765ecb90ee07e3d90
ms.contentlocale: de-de
ms.lasthandoff: 03/05/2018

---

# <a name="ship-an-order-from-a-different-store"></a><span data-ttu-id="05ffd-103">Auftrag aus einem anderen Shop versenden</span><span class="sxs-lookup"><span data-stu-id="05ffd-103">Ship an order from a different store</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="05ffd-104">Bei der Belastung übermitteln Funktion in Dynamics 365 for Retail, können Debitorenaufträge in einen Shops platziert und aus einem anderen Shop versendet werden.</span><span class="sxs-lookup"><span data-stu-id="05ffd-104">With the Charge send feature in Dynamics 365 for Retail, customer orders can be placed in one store and shipped from another store.</span></span> <span data-ttu-id="05ffd-105">Debitorenaufträge im Verkaufsstellen (POS)-Client unterstützen mehrere Erfüllungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="05ffd-105">Customer orders in the point of sale (POS) client support multiple fulfillment options.</span></span> <span data-ttu-id="05ffd-106">Einige Beispiele von Erfüllungsoptionen enthalten:</span><span class="sxs-lookup"><span data-stu-id="05ffd-106">Some examples of fulfillment options include:</span></span>
-   <span data-ttu-id="05ffd-107">Entnahme vom gleichen Shop an einem anderen Datum.</span><span class="sxs-lookup"><span data-stu-id="05ffd-107">Pick up from the same store on a different date.</span></span>
-   <span data-ttu-id="05ffd-108">Entnahme von einem anderen Shop an demselben oder an einem anderen Datum.</span><span class="sxs-lookup"><span data-stu-id="05ffd-108">Pick up from a different store on the same date or a different date.</span></span>
-   <span data-ttu-id="05ffd-109">Versand vom Standardversandlagerort, der dem Shop zugeordnet ist und Lieferung an einem bestimmtes Datum.</span><span class="sxs-lookup"><span data-stu-id="05ffd-109">Ship from the default shipping warehouse that is assigned to the store, and deliver on a specific date.</span></span>

<span data-ttu-id="05ffd-110">Die Belastung senden Funktion verwendet die folgenden POS-Vorgänge: Versand aller Produkte und die Lieferung bestimmter Produkte.</span><span class="sxs-lookup"><span data-stu-id="05ffd-110">The Charge send feature uses the following POS operations: Ship all products and Ship selected products.</span></span> <span data-ttu-id="05ffd-111">Dies ermöglicht dem Ladenangestellten, den "Versand von"-Speicherort auszuwählen, von dem der Auftrag oder die Auftragsposition erfüllt werden können.</span><span class="sxs-lookup"><span data-stu-id="05ffd-111">This allows the store clerk to select the “ship from” location that the order or order line can be fulfilled from.</span></span> <span data-ttu-id="05ffd-112">Standardmäßig ist der "Versand von"-Lagerplatz der Versandlagerort, der dem Shop zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="05ffd-112">By default, the “ship from” location is the shipping warehouse that is associated with the store.</span></span> <span data-ttu-id="05ffd-113">Allerdings kann der Ladenangestellte diesen Ort ggf. ändern und einen beliebigen Shop wählen, der in der Filialsuchegruppe definiert wird, die dem Shop zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="05ffd-113">However, the store clerk can change this location and select any store that is defined in the store locator group that is assigned to the store.</span></span> 

<span data-ttu-id="05ffd-114">Die Möglichkeit, Versand zu"-Adressen auszuwählen bleibt unverändert.</span><span class="sxs-lookup"><span data-stu-id="05ffd-114">The ability to select “ship to” addresses remains unchanged.</span></span> 

<span data-ttu-id="05ffd-115">Die Versandmethoden, die verwendet werden können, um die Auftragsposition zu decken, basieren auf der Konfiguration mit gültigen Lieferarten für Produkte und Adressen.</span><span class="sxs-lookup"><span data-stu-id="05ffd-115">The shipping methods that can be used to fulfill the order line are based on the configuration of valid modes of delivery for products and addresses.</span></span> <span data-ttu-id="05ffd-116">Da die Regeln, die von Lieferarten gültig sind, nur im Retail Zentralverwaltung (HQ) hat, der POS-Kunde ermöglicht einem Echtzeitanruf die gültigen Lieferarten für eine Schiffsposition abrufen verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="05ffd-116">Because the rules about valid of modes of delivery are maintained only in the Retail headquarters (HQ), the POS client makes a real-time call to fetch the valid modes of delivery for a ship line.</span></span> 


