---
title: Szenarien für die Rechnungszahlung einrichten
description: In diesem Thema wird beschrieben, wie Sie Dynamics 365 for Retail so konfigurieren, dass verschiedene Szenarien in Bezug auf Rechnungszahlungen unterstützt werden.
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: b7132dc9b3c78fa04fcfc38ea72b5678ad08deb2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564969"
---
# <a name="set-up-pay-invoice-scenarios"></a><span data-ttu-id="c3923-103">Szenarien für die Rechnungszahlung einrichten</span><span class="sxs-lookup"><span data-stu-id="c3923-103">Set up pay invoice scenarios</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c3923-104">Die Funktion für die Rechnungszahlung in Dynamics 365 for Retail wurde erweitert und unterstützt nun Folgendes:</span><span class="sxs-lookup"><span data-stu-id="c3923-104">The Pay invoice functionality in Dynamics 365 for Retail has been expanded to support:</span></span>

- <span data-ttu-id="c3923-105">Gewinn aus mehreren Auftragsrechnungen in einer einzigen POS-Transaktion.</span><span class="sxs-lookup"><span data-stu-id="c3923-105">Payoff of multiple sales order invoices in a single POS transaction.</span></span>
- <span data-ttu-id="c3923-106">Zahlung der verschiedenen Kundenrechnungsarten wie Freitextrechnungen, projektbasierte Rechnungen und Gutschriften.</span><span class="sxs-lookup"><span data-stu-id="c3923-106">Payment of various customer invoice types including free text invoices, project-based invoices, and credit notes.</span></span>

<span data-ttu-id="c3923-107">Um diese Szenarien zu aktivieren, muss das Funktionsprofil für Geschäfte wie unten skizziert konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="c3923-107">To enable these scenarios, the functionality profile for stores must be configured as outlined in below.</span></span>

1. <span data-ttu-id="c3923-108">Gehen Sie zu **Einzelhandel \> Kanaleinrichtung \> POS-Einrichtung \> POS-Profile \> Funktionsprofile**, und wählen Sie ein Profil aus das mit den Geschäften verknüpft ist, für die Sie Änderungen vornehmen möchten.</span><span class="sxs-lookup"><span data-stu-id="c3923-108">Go to **Retail \> Channel setup \> POS setup \> POS profiles \> Functionality profiles** and select a profile that's linked to the stores that you want to make the changes for.</span></span>
2. <span data-ttu-id="c3923-109">Konfigurieren Sie auf der Registerkarte **Funktionen** die folgenden Parameter nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="c3923-109">On the **Functions** tab, configure the following parameters as needed.</span></span>

    - <span data-ttu-id="c3923-110">**Auftragsrechnung** – Wählen Sie **Ja** aus, damit Benutzer eine oder mehrere auftragsbasierte Rechnungen in einer einzigen POS-Transaktion bezahlen können.</span><span class="sxs-lookup"><span data-stu-id="c3923-110">**Sales order invoice** – Select **Yes** to allow users to pay one or more sales order-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="c3923-111">**Freitextrechnung** – Wählen Sie **Ja** aus, damit Benutzer eine oder mehrere freitextbasierte Rechnungen in einer einzigen POS-Transaktion bezahlen können.</span><span class="sxs-lookup"><span data-stu-id="c3923-111">**Free text invoice** – Select **Yes** to allow users to pay one or more free text-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="c3923-112">**Projektrechnung** – Wählen Sie **Ja** aus, damit Benutzer eine oder mehrere projektbasierte Rechnungen in einer einzigen POS-Transaktion bezahlen können.</span><span class="sxs-lookup"><span data-stu-id="c3923-112">**Project invoice** – Select **Yes** to allow users to pay one or more project-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="c3923-113">**Auftragsgutschrift** – Wählen Sie **Ja** aus, damit Benutzer mehrere auftragsbasierte Gutschriften auf offene Rechnungen anrechnen können oder eine Rückerstattung an den Debitoren für eine offene Gutschrift verarbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c3923-113">**Sales order credit note** – Select **Yes** to allow users to settle multiple sales order-based credit notes against open invoices or process a refund to the customer for an open credit note.</span></span>

> [!NOTE]
> <span data-ttu-id="c3923-114">Zahlung oder Ausgleich in Teilbeträgen wird noch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c3923-114">Payment or settlement of partial amounts is not yet supported.</span></span>
