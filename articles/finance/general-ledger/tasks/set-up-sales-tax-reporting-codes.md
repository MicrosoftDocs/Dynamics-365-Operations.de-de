---
title: Mehrwertsteuer-Erklärungscodes einrichten
description: Die "Mehrwertsteuer-Erklärungscodes" verweisen auf eine Feldnummer in einem Mehrwertsteuerbericht.
author: twheeloc
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6c18f4fb0db31a959647bb10d2b99d940646676e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976792"
---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="24e6f-103">Mehrwertsteuer-Erklärungscodes einrichten</span><span class="sxs-lookup"><span data-stu-id="24e6f-103">Set up sales tax reporting codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="24e6f-104">Die "Mehrwertsteuer-Erklärungscodes" verweisen auf eine Feldnummer in einem Mehrwertsteuerbericht.</span><span class="sxs-lookup"><span data-stu-id="24e6f-104">The Sales tax reporting codes refer to a field number on a sales tax report.</span></span> <span data-ttu-id="24e6f-105">Sie werden bei länderspezifischen Berichtslayouts und dem "Bericht zu Mehrwertsteuerzahlung nach Code" verwendet, um Mehrwertsteuerbeträge für einen Abrechnungszeitraum drucken, die pro Berichtscode zusammengefasst werden.</span><span class="sxs-lookup"><span data-stu-id="24e6f-105">They are used on country specific report layouts and the Sales tax payment by code report to print sales tax amounts for a settlement period summarized per reporting code.</span></span> <span data-ttu-id="24e6f-106">Nachdem Sie die Mehrwertsteuer-Erklärungscodes erstellt haben, können Sie auf dem Inforegister "Berichtseinstellungen" auf der Seite "Mehrwertsteuercode" auf sie verweisen.</span><span class="sxs-lookup"><span data-stu-id="24e6f-106">After you create Sales tax reporting codes, you can refer to them on the Report setup FastTabs in the Sales tax code page.</span></span> 

<span data-ttu-id="24e6f-107">Für diese Erfassung wird das Demo-Unternehmen DEMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="24e6f-107">This recording uses the DEMF demo company.</span></span>

1. <span data-ttu-id="24e6f-108">Gehen Sie im Navigationsbereich **Navigationsbereich** zu **Steuern > Einrichten > Umsatzsteuer > Umsatzsteuer-Meldekennzeichen**.</span><span class="sxs-lookup"><span data-stu-id="24e6f-108">In the **Navigation pane**, go to **Tax > Setup > Sales tax > Sales tax reporting codes**.</span></span>
2. <span data-ttu-id="24e6f-109">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="24e6f-109">Click **New**.</span></span>
3. <span data-ttu-id="24e6f-110">Wählen Sie das Berichtslayout aus, zu dem der Berichtscode gehört.</span><span class="sxs-lookup"><span data-stu-id="24e6f-110">Select the report layout that the reporting code belongs to.</span></span> <span data-ttu-id="24e6f-111">Dieses Layout wird verwendet, um die verfügbaren Erklärungscodes für einen Mehrwertsteuercode zu filtern.</span><span class="sxs-lookup"><span data-stu-id="24e6f-111">This layout is used to filter the available reporting codes for a Sales tax code.</span></span> <span data-ttu-id="24e6f-112">Jeder Mehrwertsteuercode gehört zu einem Abrechnungszeitraum, der zu einer Mehrwertsteuerbehörde gehört, die ein Berichtslayout verwendet.</span><span class="sxs-lookup"><span data-stu-id="24e6f-112">Each Sales tax code belongs to a settlement period which belongs to a Sales tax authority which uses a Report layout.</span></span>  
4. <span data-ttu-id="24e6f-113">Geben Sie im Feld **Reporting code** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="24e6f-113">In the **Reporting code** field, enter a number.</span></span>
5. <span data-ttu-id="24e6f-114">Geben Sie im Feld **Berichtstext** eine Beschreibung ein, die in Berichten angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="24e6f-114">In the **Report text** field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="24e6f-115">Geben Sie im Feld **Kurzbeschreibung** eine Beschreibung für interne Zwecke ein.</span><span class="sxs-lookup"><span data-stu-id="24e6f-115">In the **Brief description** field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="24e6f-116">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="24e6f-116">Click **Save**.</span></span>

