---
title: Szenarien für die Rechnungszahlung einrichten
description: In diesem Thema wird beschrieben, wie Sie Dynamics 365 Commerce so konfigurieren, dass verschiedene Szenarien in Bezug auf Rechnungszahlungen unterstützt werden.
author: josaw1
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 08d3cf48c0bea6f0e13dda49e53b314a6037860d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804552"
---
# <a name="set-up-pay-invoice-scenarios"></a><span data-ttu-id="6a28f-103">Szenarien für die Rechnungszahlung einrichten</span><span class="sxs-lookup"><span data-stu-id="6a28f-103">Set up pay invoice scenarios</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6a28f-104">Die Funktion für die Rechnungszahlung in Dynamics 365 Commerce wurde erweitert und unterstützt nun Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6a28f-104">The Pay invoice functionality in Dynamics 365 Commerce has been expanded to support:</span></span>

- <span data-ttu-id="6a28f-105">Gewinn aus mehreren Auftragsrechnungen in einer einzigen POS-Transaktion.</span><span class="sxs-lookup"><span data-stu-id="6a28f-105">Payoff of multiple sales order invoices in a single POS transaction.</span></span>
- <span data-ttu-id="6a28f-106">Zahlung der verschiedenen Kundenrechnungsarten wie Freitextrechnungen, projektbasierte Rechnungen und Gutschriften.</span><span class="sxs-lookup"><span data-stu-id="6a28f-106">Payment of various customer invoice types including free text invoices, project-based invoices, and credit notes.</span></span>

<span data-ttu-id="6a28f-107">Um diese Szenarien zu aktivieren, muss das Funktionsprofil für Geschäfte wie unten skizziert konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="6a28f-107">To enable these scenarios, the functionality profile for stores must be configured as outlined in below.</span></span>

1. <span data-ttu-id="6a28f-108">Gehen Sie zu **Retail und Commerce \> Kanaleinstellungen \> POS-Einstellungen \> POS-Profile \> Funktionsprofile**, und wählen Sie ein Profil aus, das mit den Stores verknüpft ist, für die Sie Änderungen vornehmen möchten.</span><span class="sxs-lookup"><span data-stu-id="6a28f-108">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Functionality profiles** and select a profile that's linked to the stores that you want to make the changes for.</span></span>
2. <span data-ttu-id="6a28f-109">Konfigurieren Sie auf der Registerkarte **Funktionen** die folgenden Parameter nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="6a28f-109">On the **Functions** tab, configure the following parameters as needed.</span></span>

    - <span data-ttu-id="6a28f-110">**Auftragsrechnung** – Wählen Sie **Ja** aus, damit Benutzer eine oder mehrere auftragsbasierte Rechnungen in einer einzigen POS-Transaktion bezahlen können.</span><span class="sxs-lookup"><span data-stu-id="6a28f-110">**Sales order invoice** – Select **Yes** to allow users to pay one or more sales order-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="6a28f-111">**Freitextrechnung** – Wählen Sie **Ja** aus, damit Benutzer eine oder mehrere freitextbasierte Rechnungen in einer einzigen POS-Transaktion bezahlen können.</span><span class="sxs-lookup"><span data-stu-id="6a28f-111">**Free text invoice** – Select **Yes** to allow users to pay one or more free text-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="6a28f-112">**Projektrechnung** – Wählen Sie **Ja** aus, damit Benutzer eine oder mehrere projektbasierte Rechnungen in einer einzigen POS-Transaktion bezahlen können.</span><span class="sxs-lookup"><span data-stu-id="6a28f-112">**Project invoice** – Select **Yes** to allow users to pay one or more project-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="6a28f-113">**Auftragsgutschrift** – Wählen Sie **Ja** aus, damit Benutzer mehrere auftragsbasierte Gutschriften auf offene Rechnungen anrechnen können oder eine Rückerstattung an den Debitoren für eine offene Gutschrift verarbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6a28f-113">**Sales order credit note** – Select **Yes** to allow users to settle multiple sales order-based credit notes against open invoices or process a refund to the customer for an open credit note.</span></span>

> [!NOTE]
> <span data-ttu-id="6a28f-114">Zahlung oder Ausgleich in Teilbeträgen wird noch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6a28f-114">Payment or settlement of partial amounts is not yet supported.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]