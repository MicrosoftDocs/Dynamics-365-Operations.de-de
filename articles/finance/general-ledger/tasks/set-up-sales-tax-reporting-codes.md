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
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 460e41d69a78cda664e0d3af828fdc482169ac52
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145074"
---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="82ab9-103">Mehrwertsteuer-Erklärungscodes einrichten</span><span class="sxs-lookup"><span data-stu-id="82ab9-103">Set up sales tax reporting codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="82ab9-104">Die "Mehrwertsteuer-Erklärungscodes" verweisen auf eine Feldnummer in einem Mehrwertsteuerbericht.</span><span class="sxs-lookup"><span data-stu-id="82ab9-104">The Sales tax reporting codes refer to a field number on a sales tax report.</span></span> <span data-ttu-id="82ab9-105">Sie werden bei länderspezifischen Berichtslayouts und dem "Bericht zu Mehrwertsteuerzahlung nach Code" verwendet, um Mehrwertsteuerbeträge für einen Abrechnungszeitraum drucken, die pro Berichtscode zusammengefasst werden.</span><span class="sxs-lookup"><span data-stu-id="82ab9-105">They are used on country specific report layouts and the Sales tax payment by code report to print sales tax amounts for a settlement period summarized per reporting code.</span></span> <span data-ttu-id="82ab9-106">Nachdem Sie die Mehrwertsteuer-Erklärungscodes erstellt haben, können Sie auf dem Inforegister "Berichtseinstellungen" auf der Seite "Mehrwertsteuercode" auf sie verweisen.</span><span class="sxs-lookup"><span data-stu-id="82ab9-106">After you create Sales tax reporting codes, you can refer to them on the Report setup FastTabs in the Sales tax code page.</span></span> 

<span data-ttu-id="82ab9-107">Für diese Erfassung wird das Demo-Unternehmen DEMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="82ab9-107">This recording uses the DEMF demo company.</span></span>

1. <span data-ttu-id="82ab9-108">Gehen Sie im Navigationsbereich **Navigationsbereich** zu **Steuern > Einrichten > Umsatzsteuer > Umsatzsteuer-Meldekennzeichen**.</span><span class="sxs-lookup"><span data-stu-id="82ab9-108">In the **Navigation pane**, go to **Tax > Setup > Sales tax > Sales tax reporting codes**.</span></span>
2. <span data-ttu-id="82ab9-109">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="82ab9-109">Click **New**.</span></span>
3. <span data-ttu-id="82ab9-110">Wählen Sie das Berichtslayout aus, zu dem der Berichtscode gehört.</span><span class="sxs-lookup"><span data-stu-id="82ab9-110">Select the report layout that the reporting code belongs to.</span></span> <span data-ttu-id="82ab9-111">Dieses Layout wird verwendet, um die verfügbaren Erklärungscodes für einen Mehrwertsteuercode zu filtern.</span><span class="sxs-lookup"><span data-stu-id="82ab9-111">This layout is used to filter the available reporting codes for a Sales tax code.</span></span> <span data-ttu-id="82ab9-112">Jeder Mehrwertsteuercode gehört zu einem Abrechnungszeitraum, der zu einer Mehrwertsteuerbehörde gehört, die ein Berichtslayout verwendet.</span><span class="sxs-lookup"><span data-stu-id="82ab9-112">Each Sales tax code belongs to a settlement period which belongs to a Sales tax authority which uses a Report layout.</span></span>  
4. <span data-ttu-id="82ab9-113">Geben Sie im Feld **Reporting code** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="82ab9-113">In the **Reporting code** field, enter a number.</span></span>
5. <span data-ttu-id="82ab9-114">Geben Sie im Feld **Berichtstext** eine Beschreibung ein, die in Berichten angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="82ab9-114">In the **Report text** field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="82ab9-115">Geben Sie im Feld **Kurzbeschreibung** eine Beschreibung für interne Zwecke ein.</span><span class="sxs-lookup"><span data-stu-id="82ab9-115">In the **Brief description** field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="82ab9-116">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="82ab9-116">Click **Save**.</span></span>

