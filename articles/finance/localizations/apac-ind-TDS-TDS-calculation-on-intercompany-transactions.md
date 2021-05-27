---
title: TDS für Intercompany-Buchungen berechnen
description: In diesem Thema wird der Prozess beschrieben, mit dem die Quellenbesteuerung (TDS) bei Intercompany-Buchungen in Phasen berechnet wird.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 0e304747cc93bfe0a39beababc3182ca14664b11
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023271"
---
# <a name="tds-calculation-on-intercompany-transactions"></a><span data-ttu-id="ef02f-103">TDS für Intercompany-Buchungen berechnen</span><span class="sxs-lookup"><span data-stu-id="ef02f-103">TDS calculation on intercompany transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef02f-104">In diesem Thema wird der Prozess beschrieben, mit dem die Quellenbesteuerung (TDS) bei Intercompany-Buchungen in Phasen berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="ef02f-104">This topic describes the process that is used to calculate Tax Deducted at Source (TDS) on intercompany transactions in phases.</span></span>

<span data-ttu-id="ef02f-105">Wenn eine Intercompany-Bestellung oder ein Intercompany-Auftrag erstellt wird, wird die für den Debitor oder Kreditor festgelegte Standard-TDS-Gruppe zur Berechnung des TDS-Betrags verwendet.</span><span class="sxs-lookup"><span data-stu-id="ef02f-105">When an intercompany purchase order or sales order is created, the default TDS group that is defined for the customer or vendor is used to calculate the TDS amount.</span></span> <span data-ttu-id="ef02f-106">Der TDS-Betrag wird nach Buchung der Rechnung auf das Rückerstattungs- oder Kreditorenkonto gebucht.</span><span class="sxs-lookup"><span data-stu-id="ef02f-106">The TDS amount is posted to the recoverable or payable accounts after the invoice is posted.</span></span>

<span data-ttu-id="ef02f-107">Ein Intercompany-Auftrag oder eine Intercompany-Bestellung wird automatisch für die ursprüngliche Bestellung oder den ursprünglichen Auftrag erstellt.</span><span class="sxs-lookup"><span data-stu-id="ef02f-107">An intercompany sales order or purchase order is automatically created for the original purchase order or sales order.</span></span> <span data-ttu-id="ef02f-108">Die Standard-TDS-Gruppe wird in der Intercompany-Bestellung angezeigt, damit die TDS berechnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ef02f-108">The default TDS group is shown on the intercompany order, so that TDS can be calculated.</span></span> <span data-ttu-id="ef02f-109">Die TDS-Gruppe kann geändert werden.</span><span class="sxs-lookup"><span data-stu-id="ef02f-109">You can change the TDS group.</span></span> <span data-ttu-id="ef02f-110">Die Rechnung kann nur gebucht werden, wenn der Nettorechnungsbetrag in der automatisch erstellten Intercompany-Bestellung mit dem Nettorechnungsbetrag in der ursprünglichen Bestellung übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="ef02f-110">The invoice can be posted only if the net invoice amount on the intercompany order that is automatically created matches the net invoice amount on the original order.</span></span> <span data-ttu-id="ef02f-111">(Der Nettobetrag ist der Rechnungsbetrag nach Abzug der TDS.)</span><span class="sxs-lookup"><span data-stu-id="ef02f-111">(The net amount is the invoice amount after TDS is deducted.)</span></span>

<span data-ttu-id="ef02f-112">Beispielsweise wird eine Verkaufsrechnung für 50.000 erstellt, und die TDS-Gruppe **10 %** wird damit verbunden.</span><span class="sxs-lookup"><span data-stu-id="ef02f-112">For example, a sales invoice is created for 50,000, and the **10%** TDS group is attached to it.</span></span> <span data-ttu-id="ef02f-113">Der gebuchte Rechnungsbetrag beträgt 45.000 und der gebuchte TDS-Betrag für die Verkaufsrechnung beträgt 5.000.</span><span class="sxs-lookup"><span data-stu-id="ef02f-113">The posted invoice amount is 45,000, and the posted TDS amount for the sales invoice is 5,000.</span></span> <span data-ttu-id="ef02f-114">Für den Intercompany-Auftrag wird automatisch eine Bestellung erstellt und die TDS-Gruppe **10 %** wird damit verbunden.</span><span class="sxs-lookup"><span data-stu-id="ef02f-114">A purchase order is automatically created for the intercompany sales order, and the  **10%** TDS group is attached to it.</span></span> <span data-ttu-id="ef02f-115">Wenn Sie die TDS-Gruppe auf **15 %** ändern, können Sie die Rechnung nicht buchen, da der Nettorechnungsbetrag des automatisch erstellten Intercompany-Auftrags nicht mit dem Nettorechnungsbetrag des ursprünglichen Auftrags übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="ef02f-115">If you change the TDS group to **15%**, you can't post the invoice, because the net invoice amount of the intercompany sales order that was automatically created doesn't match the net invoice amount of the original sales order.</span></span>

<span data-ttu-id="ef02f-116">Eine Zahlungserfassung, die für eine Intercompany-Rechnung erstellt wird, wird automatisch gebucht.</span><span class="sxs-lookup"><span data-stu-id="ef02f-116">A payment journal that is created for an intercompany invoice is automatically posted.</span></span> <span data-ttu-id="ef02f-117">Diese Zahlungserfassung kann nur gebucht werden, wenn ihr Nettozahlungsbetrag mit dem Nettozahlungsbetrag in der ursprünglichen Zahlungserfassung übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="ef02f-117">That payment journal can be posted only if the net payment amount on it matches the net payment amount on the original payment journal.</span></span>
