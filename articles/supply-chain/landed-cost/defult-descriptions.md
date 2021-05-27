---
title: Standardbeschreibungen für das Hauptbuch
description: Standardbeschreibungen können verwendet werden, um das Feld Beschreibung in Belegbuchungen im Hauptbuch zu aktualisieren.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 25dd72c86b22b50eccef22a5d2cbcfcf04280684
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021611"
---
# <a name="default-descriptions-for-the-general-ledger"></a><span data-ttu-id="80212-103">Standardbeschreibungen für das Hauptbuch</span><span class="sxs-lookup"><span data-stu-id="80212-103">Default descriptions for the general ledger</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="80212-104">Standardbeschreibungen können verwendet werden, um das Feld **Beschreibung** in Belegbuchungen in das Hauptbuch zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="80212-104">Default descriptions can be used to update the **Description** field in voucher postings to the general ledger.</span></span> <span data-ttu-id="80212-105">Diese Funktionalität wurde für die Arbeit mit kalkulierten Gesamttransportkosten erweitert.</span><span class="sxs-lookup"><span data-stu-id="80212-105">This functionality has been enhanced to work with Landed cost.</span></span>

<span data-ttu-id="80212-106">Um Standardbeschreibungen für Hauptbuchbuchungen festzulegen, gehen Sie zu **Organisationsverwaltung \> Einrichtung \> Standardbeschreibungen**.</span><span class="sxs-lookup"><span data-stu-id="80212-106">To set up default descriptions for ledger postings, go to **Organizational administration \> Setup \> Default descriptions**.</span></span>

<span data-ttu-id="80212-107">Die folgende Tabelle zeigt die neuen Werte, die für das Feld **Beschreibung** auf der Seite **Standardbeschreibungen** hinzugefügt wurden, um die Gesamttransportkosten zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="80212-107">The following table lists the new values that have been added for the **Description** field on the **Default descriptions** page to support Landed cost.</span></span>

| <span data-ttu-id="80212-108">Typ der Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80212-108">Description type</span></span> | <span data-ttu-id="80212-109">Notizen</span><span class="sxs-lookup"><span data-stu-id="80212-109">Notes</span></span> |
|---|---|
| <span data-ttu-id="80212-110">Kalkulation importieren - Kostenabgrenzung</span><span class="sxs-lookup"><span data-stu-id="80212-110">Import costing – Cost accrual</span></span> | <span data-ttu-id="80212-111">Wenn eine Rechnung für eine Einkaufsbestellung gebucht wird, wird eine Kostenabgrenzung für die geschätzten Kosten der Fahrt verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="80212-111">When a purchase order invoice is posted, a cost accrual is processed for estimate voyage costs.</span></span> <span data-ttu-id="80212-112">Es können Standardbeschreibungen angegeben werden, um die Fahrtnummer zur Beschreibung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="80212-112">Default descriptions can be specified to add the voyage number to the description.</span></span> <span data-ttu-id="80212-113">Verwenden Sie *%4* für die Sendungsnummer.</span><span class="sxs-lookup"><span data-stu-id="80212-113">Use *%4* for the shipment number.</span></span> |
| <span data-ttu-id="80212-114">Importkalkulation - Waren in Zustellung</span><span class="sxs-lookup"><span data-stu-id="80212-114">Import costing – Goods in transit order</span></span> | <span data-ttu-id="80212-115">Wenn Sie die In-Transit-Verarbeitung verwenden, wird die Rechnung der Einkaufsbestellung gebucht und die Waren werden auf ein Konto für Waren in Zustellung gebucht.</span><span class="sxs-lookup"><span data-stu-id="80212-115">If you're using in-transit processing, the purchase order invoice is posted, and the goods are posted to a goods in transit account.</span></span> <span data-ttu-id="80212-116">Es können Standardbeschreibungen angegeben werden, um die Nummer des Auftrags in Zustellung zur Beschreibung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="80212-116">Default descriptions can be specified to add the in-transit order number to the description.</span></span> <span data-ttu-id="80212-117">Verwenden Sie *%4* für die In-Transit-Auftragsnummer.</span><span class="sxs-lookup"><span data-stu-id="80212-117">Use *%4* for the in-transit order number.</span></span> |
| <span data-ttu-id="80212-118">Bestand - Abschluss - Anpassung</span><span class="sxs-lookup"><span data-stu-id="80212-118">Inventory – close – adjustment</span></span> | <span data-ttu-id="80212-119">Wenn die Kreditorenrechnung (AP) für eine Fahrt verarbeitet wird, wird eine Bestandsanpassung verarbeitet, um die Kosten für die Fahrt zu schätzen.</span><span class="sxs-lookup"><span data-stu-id="80212-119">When the accounts payable (AP) invoice is processed for a voyage cost, an inventory adjustment is processed to estimate voyage costs.</span></span> <span data-ttu-id="80212-120">Es können Standardbeschreibungen angegeben werden, um die Fahrtnummer zur Beschreibung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="80212-120">Default descriptions can be specified to add the voyage number to the description.</span></span> <span data-ttu-id="80212-121">Verwenden Sie *%4* für die Sendungsnummer.</span><span class="sxs-lookup"><span data-stu-id="80212-121">Use *%4* for the shipment number.</span></span> |

<span data-ttu-id="80212-122">Weitere Informationen zum Arbeiten mit der Seite **Standardbeschreibungen** finden Sie unter [Standardbeschreibungen für automatische Buchungen festlegen](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).</span><span class="sxs-lookup"><span data-stu-id="80212-122">For more information about how to work with the **Default descriptions** page, see [Set up default descriptions for automatic posting](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).</span></span>
