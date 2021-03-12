---
title: EUR-00015 Suche nach Partei per MwSt.-Kennung
description: Dieses Verfahren zeigt, wie Sie eine Parteiensuche mithilfe einer Erfassungskennung durchführen.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyTable, DirPartTaxRegistrationSearch
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c586de249575def120a6ae04fdc409aadfa1083d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4984839"
---
# <a name="eur-00015-party-search-using-vat-id"></a><span data-ttu-id="31f17-103">EUR-00015 Suche nach Partei per MwSt.-Kennung</span><span class="sxs-lookup"><span data-stu-id="31f17-103">EUR-00015 Party search using VAT ID</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="31f17-104">Dieses Verfahren zeigt, wie Sie eine Parteiensuche mithilfe einer Erfassungskennung durchführen.</span><span class="sxs-lookup"><span data-stu-id="31f17-104">This procedure shows how to complete a party search using a registration ID.</span></span> <span data-ttu-id="31f17-105">Bevor Sie dieses Verfahren ausführen können, müssen Sie MwSt.-IDs einrichten und sämtliche MwSt.-IDs für Debitoren, Kreditoren oder juristischen Personen eingeben.</span><span class="sxs-lookup"><span data-stu-id="31f17-105">Before you can complete this procedure, you must set up VAT IDs and enter any VAT IDs for vendors, customers, or legal entities.</span></span>

<span data-ttu-id="31f17-106">Diese Prozedur gilt für alle europäischen Länder/Regionen.</span><span class="sxs-lookup"><span data-stu-id="31f17-106">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="31f17-107">Diese Prozedur wurde mithilfe des Demodatenunternehmens DEMF mit der primären Adresse einer juristischen Person in Deutschland erstellt.</span><span class="sxs-lookup"><span data-stu-id="31f17-107">The procedure was created using the demo data company DEMF with a primary address in Germany.</span></span> <span data-ttu-id="31f17-108">Diese Vorgehensweise ist für einen Kreditor-Manager oder einen Debitor-Manager vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="31f17-108">This procedure is intended for an accounts payable manager or accounts receivable manager.</span></span> <span data-ttu-id="31f17-109">Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="31f17-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="31f17-110">Wechseln Sie zu Organisationsverwaltung > Globales Adressbuch > Globales Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="31f17-110">Go to Organization administration > Global address book > Global address book.</span></span>
2. <span data-ttu-id="31f17-111">Klicken Sie auf "Registrierungskennungssuche".</span><span class="sxs-lookup"><span data-stu-id="31f17-111">Click Registration ID search.</span></span>
3. <span data-ttu-id="31f17-112">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="31f17-112">Click Add.</span></span>
4. <span data-ttu-id="31f17-113">Geben Sie im Feld "Registrierungstyp" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="31f17-113">In the Registration type field, enter or select a value.</span></span>
    * <span data-ttu-id="31f17-114">Wenn Sie z. B. Parteien mit einer Erfassungskennung vom Typ MwSt.-Kennung suchen, wählen Sie "MwSt.-Kennung" aus</span><span class="sxs-lookup"><span data-stu-id="31f17-114">For example, if you wanted to find parties with a registration ID of type VAT ID, select VAT ID.</span></span>  
5. <span data-ttu-id="31f17-115">Wählen Sie im Feld Name/Region einen Wert aus oder geben Sie ihn ein«».</span><span class="sxs-lookup"><span data-stu-id="31f17-115">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="31f17-116">Geben Sie beispielsweise "DEU" ein.</span><span class="sxs-lookup"><span data-stu-id="31f17-116">For example, enter DEU.</span></span>  
6. <span data-ttu-id="31f17-117">Geben Sie im Feld "Registrierungsnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="31f17-117">In the Registration number field, type a value.</span></span>
7. <span data-ttu-id="31f17-118">Klicken Sie auf "Suchen".</span><span class="sxs-lookup"><span data-stu-id="31f17-118">Click Find.</span></span>
    * <span data-ttu-id="31f17-119">Alle Parteien mit dieser Erfassungskennung werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="31f17-119">All parties with that registration ID will be displayed.</span></span>  

