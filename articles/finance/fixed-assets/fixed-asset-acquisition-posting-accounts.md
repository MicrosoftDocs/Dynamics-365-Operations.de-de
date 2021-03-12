---
title: Buchungskonten für die Anlagenanschaffung
description: Dieser Artikel beschreibt, wie Kontoeinträge im Hauptbuch eingerichtet werden, um Anlagen zu erwerben.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa0d73790a20f3fe5bb76b87e635b1f16e034479
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976115"
---
# <a name="fixed-asset-acquisition-posting-accounts"></a><span data-ttu-id="86bcd-103">Buchungskonten für die Anlagenanschaffung</span><span class="sxs-lookup"><span data-stu-id="86bcd-103">Fixed asset acquisition posting accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="86bcd-104">Dieser Artikel beschreibt, wie Kontoeinträge im Hauptbuch eingerichtet werden, um Anlagen zu erwerben.</span><span class="sxs-lookup"><span data-stu-id="86bcd-104">This article explains how to set up general ledger posting accounts for acquiring assets.</span></span>

<span data-ttu-id="86bcd-105">Konten, die zum Buchen von Anlagenanschaffungen verwendet werden, können je nach verwendeter Methode zur Anschaffung von Anlage abweichen.</span><span class="sxs-lookup"><span data-stu-id="86bcd-105">Accounts used for posting fixed asset acquisitions may vary depending upon the method used to acquire the asset.</span></span> <span data-ttu-id="86bcd-106">Wählen Sie auf der Anlagenbuchungsprofilseite auf der Sachkontoregisterkarte die ausgewählten Anschaffung und der Anschaffungsänderung aus, um Anlagekonten für das Buchen auf das Sachkonto einzurichten.</span><span class="sxs-lookup"><span data-stu-id="86bcd-106">On the Fixed asset posting profiles page, on the Ledger accounts tab, select Acquisition and Acquisition adjustment to set up fixed asset accounts to post to the ledger.</span></span> 

<span data-ttu-id="86bcd-107">In Erfassungen und Bestellungen ist das Sachkonto normalerweise das Bilanzkonto (Kontenart), dem der Anschaffungswert für die neue Anlage belastet wird.</span><span class="sxs-lookup"><span data-stu-id="86bcd-107">In journals and on purchase orders, Ledger account is typically the balance sheet account, where the acquisition value of the new fixed asset is debited.</span></span> <span data-ttu-id="86bcd-108">Dieses Konto ist in der Erfassung nicht zu sehen und kann in Buchungen nicht ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="86bcd-108">This account is not displayed in the journal and cannot be replaced in transactions.</span></span> 

<span data-ttu-id="86bcd-109">Das Gegenkonto ist ebenfalls ein Bilanzkonto (Kontenart).</span><span class="sxs-lookup"><span data-stu-id="86bcd-109">Offset account is also a balance sheet account.</span></span> <span data-ttu-id="86bcd-110">In der allgemeinen Erfassung und der Anlagenerfassung ist dieses Konto oft das Bankkonto, über das die Anschaffung der Anlage bezahlt wird.</span><span class="sxs-lookup"><span data-stu-id="86bcd-110">In the general journal and in the fixed assets journal, this account often will be the bank account that is used to pay for the acquisition of the asset.</span></span> <span data-ttu-id="86bcd-111">Das Gegenkonto wird in den Erfassungen als Standardkonto vorgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="86bcd-111">The offset account is a default account, which is suggested in the journals.</span></span> <span data-ttu-id="86bcd-112">Es kann in der Erfassung in ein beliebiges anderes Konto aus dem Kontenplan oder aber in ein Kreditorenkonto geändert werden, wenn die Anlage von einem Kreditor erworben wurde.</span><span class="sxs-lookup"><span data-stu-id="86bcd-112">It can be changed in the journal to any other account from the chart of accounts or to a vendor account, if the fixed asset was purchase from a vendor.</span></span> 

<span data-ttu-id="86bcd-113">Wenn im Kreditorenkonto die Funktion Rechnungserfassung oder Aufträge für Anlagenanschaffungen verwendet wird, wird das Gegenkonto für die Anlagenbuchung durch das Kreditorenkonto ersetzt, das für die Buchung ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="86bcd-113">When Invoice journal or Purchase orders in Accounts payable are used for fixed asset acquisitions, the offset account for the fixed asset transaction is replaced by the vendor account that is selected for the transaction.</span></span>

<span data-ttu-id="86bcd-114">Bei Anschaffungen, die über die Erfassung für Anlagenbestand im Hauptbuch gebucht wurden, wird die Anlage nicht von externen Quellen gekauft, sondern aus dem Lager des Unternehmens umgebucht.</span><span class="sxs-lookup"><span data-stu-id="86bcd-114">For acquisitions posted using the Inventory to fixed assets journal in General ledger, the fixed asset is not bought from external sources, but transferred from the company's own inventory.</span></span> <span data-ttu-id="86bcd-115">Aus diesem Grund handelt es sich bei dem Gegenkonto um ein Lagerabgangskonto für den Lagerartikel in der Lagerverwaltung.</span><span class="sxs-lookup"><span data-stu-id="86bcd-115">Therefore, the offset account is an inventory issue account for the inventory item in Inventory management.</span></span>

<span data-ttu-id="86bcd-116">Weitere Informationen finden Sie unter[Anlagen über Beschaffung erhalten](acquire-assets-procurement.md).</span><span class="sxs-lookup"><span data-stu-id="86bcd-116">For more information, see [Acquire assets through procurement](acquire-assets-procurement.md).</span></span>



