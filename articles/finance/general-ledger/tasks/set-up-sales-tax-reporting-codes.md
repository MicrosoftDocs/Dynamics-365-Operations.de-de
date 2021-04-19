---
title: Mehrwertsteuer-Erklärungscodes einrichten
description: Die Mehrwertsteuer-Erklärungscodes verweisen auf eine Feldnummer, die in einem Mehrwertsteuerbericht aufgeführt wird.
author: twheeloc
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e040bac6ef9e950e8d7f97e3c136636acf1fe43
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813530"
---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="f57df-103">Mehrwertsteuer-Erklärungscodes einrichten</span><span class="sxs-lookup"><span data-stu-id="f57df-103">Set up sales tax reporting codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f57df-104">Die Mehrwertsteuer-Erklärungscodes verweisen auf eine Feldnummer, die in einem Mehrwertsteuerbericht aufgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f57df-104">The Sales tax reporting codes refer to a field number that's listed on a sales tax report.</span></span> <span data-ttu-id="f57df-105">Sie werden in länderspezifischen Berichtslayouts verwendet.</span><span class="sxs-lookup"><span data-stu-id="f57df-105">They are used on country-specific report layouts.</span></span> <span data-ttu-id="f57df-106">Sie werden auch im Bericht zu Mehrwertsteuerzahlung nach Code verwendet.</span><span class="sxs-lookup"><span data-stu-id="f57df-106">They're also used on the Sales tax payment by code report.</span></span> <span data-ttu-id="f57df-107">Dieser Bericht enthält Mehrwertsteuerbeträge für einen Abrechnungszeitraum, die für jeden Berichtscode zusammengefasst sind.</span><span class="sxs-lookup"><span data-stu-id="f57df-107">That report shows sales tax amounts for a settlement period summarized for each reporting code.</span></span> <span data-ttu-id="f57df-108">Nachdem Sie die Mehrwertsteuer-Erklärungscodes erstellt haben, können Sie diese auf dem Inforegister Berichtseinstellungen darauf verweisen, auf das Sie von der Seite **Mehrwertsteuercode** zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="f57df-108">After you create Sales tax reporting codes, you can refer to those codes on the Report setup FastTabs, which you can access from the **Sales tax code** page.</span></span> 

<span data-ttu-id="f57df-109">Für diese Erfassung wird das Demo-Unternehmen DEMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="f57df-109">This recording uses the DEMF demo company.</span></span>

1. <span data-ttu-id="f57df-110">Gehen Sie im Navigationsbereich **Navigationsbereich** zu **Steuern > Einrichten > Umsatzsteuer > Umsatzsteuer-Meldekennzeichen**.</span><span class="sxs-lookup"><span data-stu-id="f57df-110">In the **Navigation pane**, go to **Tax > Setup > Sales tax > Sales tax reporting codes**.</span></span>
2. <span data-ttu-id="f57df-111">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="f57df-111">Click **New**.</span></span>
3. <span data-ttu-id="f57df-112">Wählen Sie das Berichtslayout aus, zu dem der Berichtscode gehört.</span><span class="sxs-lookup"><span data-stu-id="f57df-112">Select the report layout that the reporting code belongs to.</span></span> <span data-ttu-id="f57df-113">Dieses Layout wird verwendet, um die verfügbaren Erklärungscodes für einen Mehrwertsteuercode zu filtern.</span><span class="sxs-lookup"><span data-stu-id="f57df-113">This layout is used to filter the available reporting codes for a sales tax code.</span></span> <span data-ttu-id="f57df-114">Jeder Mehrwertsteuercode gehört zu einem Abrechnungszeitraum, der zu einer Mehrwertsteuerbehörde gehört, die ein Berichtslayout verwendet.</span><span class="sxs-lookup"><span data-stu-id="f57df-114">Each sales tax code belongs to a settlement period, which belongs to a Sales tax authority, which uses a report layout.</span></span>  
4. <span data-ttu-id="f57df-115">Geben Sie im Feld **Reporting code** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="f57df-115">In the **Reporting code** field, enter a number.</span></span>
5. <span data-ttu-id="f57df-116">Geben Sie im Feld **Berichtstext** eine Beschreibung ein, die in Berichten angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f57df-116">In the **Report text** field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="f57df-117">Geben Sie im Feld **Kurzbeschreibung** eine Beschreibung für interne Zwecke ein.</span><span class="sxs-lookup"><span data-stu-id="f57df-117">In the **Brief description** field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="f57df-118">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="f57df-118">Click **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]