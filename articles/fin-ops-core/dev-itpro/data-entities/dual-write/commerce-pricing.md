---
title: Dynamics 365 Commerce-Preisgestaltungsmodul mit Dynamics 365 Sales verwenden
description: In diesem Thema wird die Verwendung des Microsoft Dynamics 365 Commerce-Preisgestaltungsmoduls zur Erstellung von Verkaufsangeboten in Dynamics 365 Sales beschrieben.
author: ShalabhjainMSFT
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: shajain
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-11-03
ms.openlocfilehash: 364cc5adf0358ffa952750149ad31d62cbd35e87
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751433"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a><span data-ttu-id="c2ff6-103">Dynamics 365 Commerce-Preisgestaltungsmodul mit Dynamics 365 Sales verwenden</span><span class="sxs-lookup"><span data-stu-id="c2ff6-103">Use the Dynamics 365 Commerce pricing engine with Dynamics 365 Sales</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c2ff6-104">In diesem Thema wird die Verwendung des Microsoft Dynamics 365 Commerce-Preisgestaltungsmoduls zur Erstellung von Verkaufsangeboten in Dynamics 365 Sales beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c2ff6-104">This topic describes how to use the Microsoft Dynamics 365 Commerce pricing engine to create sales quotations in Dynamics 365 Sales.</span></span>

<span data-ttu-id="c2ff6-105">Das Dynamics 365 Commerce-Preisgestaltungsmodul unterstützt die meisten B2C-Preisszenarien (Business-to-Consumer), z. B. Preisgestaltung auf Filialebene, zugehörigkeits- und treuebasierte Preisgestaltung, Rabatte für Angebots-Sortimente, Mengenrabatte und Schwellenrabatte.</span><span class="sxs-lookup"><span data-stu-id="c2ff6-105">The Dynamics 365 Commerce pricing engine supports most business-to-consumer (B2C) pricing scenarios, such as store-level pricing, affiliation-based and loyalty-based pricing, mix-and-match discounts, quantity discounts, and threshold discounts.</span></span> <span data-ttu-id="c2ff6-106">Das Preisgestaltungsmodul verwendet komplexe Regeln, um den besten Preis für ein bestimmtes Angebot oder eine bestimmte Bestellung zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="c2ff6-106">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span>

<span data-ttu-id="c2ff6-107">Wenn Sie [duales Schreiben](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview) verwenden, haben Sie drei Möglichkeiten für Ihre Preisgestaltungsanforderungen.</span><span class="sxs-lookup"><span data-stu-id="c2ff6-107">When you use [dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), you have three options for your pricing needs.</span></span> <span data-ttu-id="c2ff6-108">Sie können mit der statischen Preisgestaltung arbeiten, die die Preisliste aus Dynamics 365 Sales verwendet, mit dem Preisgestaltungsmodul von Dynamics 365 Supply Chain Management oder mit dem Preisgestaltungsmodul von Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c2ff6-108">You can use the static pricing that comes from the price list in Dynamics 365 Sales, the pricing engine in Dynamics 365 Supply Chain Management, or the pricing engine in Dynamics 365 Commerce.</span></span> <span data-ttu-id="c2ff6-109">Unter diesen Optionen eignet sich das Preisgestaltungsmodul von Commerce am besten für B2C-Szenarien.</span><span class="sxs-lookup"><span data-stu-id="c2ff6-109">Among these options, the Commerce pricing engine is best suited to B2C scenarios.</span></span>

## <a name="use-the-commerce-pricing-engine-in-sales"></a><span data-ttu-id="c2ff6-110">Preisgestaltungsmodul von Commerce in Sales verwenden</span><span class="sxs-lookup"><span data-stu-id="c2ff6-110">Use the Commerce pricing engine in Sales</span></span>

> [!NOTE]
> <span data-ttu-id="c2ff6-111">Derzeit kann das Preisgestaltungsmodul von Commerce nur für die Angebotserstellung in Sales verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2ff6-111">Currently, the Commerce pricing engine can be used only for quotation creation in the Sales.</span></span> <span data-ttu-id="c2ff6-112">Die Integration von Aufträgen in das Preisgestaltungsmodul von Commerce ist noch nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c2ff6-112">Sales order integration with the Commerce pricing engine isn't yet available.</span></span>

<span data-ttu-id="c2ff6-113">Wenn Benutzer ein Angebot in Sales initiieren, kopiert das Framework für duales Schreiben die Angebotsdetails nach Commerce.</span><span class="sxs-lookup"><span data-stu-id="c2ff6-113">When users initiate a quotation in Sales, the dual-write framework copies the quotation details to Commerce.</span></span> <span data-ttu-id="c2ff6-114">Alle Änderungen an vorhandenen oder neu hinzugefügten Angebotspositionen in Sales werden nach Commerce kopiert.</span><span class="sxs-lookup"><span data-stu-id="c2ff6-114">Any changes to existing quotation lines or any newly added quotation lines in Sales are copied to Commerce.</span></span> <span data-ttu-id="c2ff6-115">Wenn Benutzer das Preisgestaltungsmodul von Commerce verwenden möchten, um das Angebot zu bepreisen, können sie **Angebot bepreisen** auswählen, um die Preise des Angebots basierend auf dem Preisgestaltungsmodul von Commerce zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c2ff6-115">When users want to use the Commerce pricing engine to price the quotation, they can select **Price quote** to update the prices of the quotation, based on the Commerce pricing engine.</span></span> <span data-ttu-id="c2ff6-116">Die Preise werden dann automatisch sowohl in Sales als auch in Commerce aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c2ff6-116">Prices are then automatically updated in both Sales and Commerce.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c2ff6-117">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="c2ff6-117">Prerequisites</span></span>

- <span data-ttu-id="c2ff6-118">Bevor Sie das Preisgestaltungsmodul von Commerce in Sales verwenden können, müssen Sie die Schritte in [Prospect-to-Cash in Dual-Write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/) ausführen.</span><span class="sxs-lookup"><span data-stu-id="c2ff6-118">Before you can use the Commerce pricing engine in Sales, you must follow the steps in [Prospect-to-cash in dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/).</span></span>
- <span data-ttu-id="c2ff6-119">Sie müssen die Bewertung von Handelsvereinbarungen für die manuelle Eingabe deaktivieren, indem Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="c2ff6-119">You must turn off trade agreement evaluation for manual entry by following these steps:</span></span>

    1. <span data-ttu-id="c2ff6-120">Rufen Sie in Ihrer Commerce-Umgebung **Debitoren \> Einrichtung \> Debitorenparameter** auf.</span><span class="sxs-lookup"><span data-stu-id="c2ff6-120">In your Commerce environment, go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    1. <span data-ttu-id="c2ff6-121">Deaktivieren Sie auf der Registerkarte **Preise** im Inforegister **Handelsvereinbarungsauswertung** das Kontrollkästchen **Manuelle Eingabe**.</span><span class="sxs-lookup"><span data-stu-id="c2ff6-121">On the **Prices** tab, on the **Trade agreement evaluation** FastTab, clear the **Manual entry** check box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c2ff6-122">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c2ff6-122">Additional resources</span></span>

[<span data-ttu-id="c2ff6-123">Prospect-to-cash in Dual-Write</span><span class="sxs-lookup"><span data-stu-id="c2ff6-123">Prospect-to-cash in dual-write</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]