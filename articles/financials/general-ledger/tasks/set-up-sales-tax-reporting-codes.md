---
title: Mehrwertsteuer-Erklärungscodes einrichten
description: Die "Mehrwertsteuer-Erklärungscodes" verweisen auf eine Feldnummer in einem Mehrwertsteuerbericht.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 830a3465944b32cc17feee60e3cbc5ad0a4dc9d7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834773"
---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="8ec8a-103">Mehrwertsteuer-Erklärungscodes einrichten</span><span class="sxs-lookup"><span data-stu-id="8ec8a-103">Set up sales tax reporting codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8ec8a-104">Die "Mehrwertsteuer-Erklärungscodes" verweisen auf eine Feldnummer in einem Mehrwertsteuerbericht.</span><span class="sxs-lookup"><span data-stu-id="8ec8a-104">The Sales tax reporting codes refer to a field number on a sales tax report.</span></span> <span data-ttu-id="8ec8a-105">Sie werden bei länderspezifischen Berichtslayouts und dem "Bericht zu Mehrwertsteuerzahlung nach Code" verwendet, um Mehrwertsteuerbeträge für einen Abrechnungszeitraum drucken, die pro Berichtscode zusammengefasst werden.</span><span class="sxs-lookup"><span data-stu-id="8ec8a-105">They are used on country specific report layouts and the Sales tax payment by code report to print sales tax amounts for a settlement period summarized per reporting code.</span></span> <span data-ttu-id="8ec8a-106">Nachdem Sie die Mehrwertsteuer-Erklärungscodes erstellt haben, können Sie auf dem Inforegister "Berichtseinstellungen" auf der Seite "Mehrwertsteuercode" auf sie verweisen.</span><span class="sxs-lookup"><span data-stu-id="8ec8a-106">After you create Sales tax reporting codes, you can refer to them on the Report setup FastTabs in the Sales tax code page.</span></span> 

<span data-ttu-id="8ec8a-107">Für diese Erfassung wird das Demo-Unternehmen DEMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="8ec8a-107">This recording uses the DEMF demo company.</span></span>



1. <span data-ttu-id="8ec8a-108">Wechseln Sie zu "Steuer" > Mehrwertsteiuer > ;Mehrwertsteuerberichterstattungscodes.</span><span class="sxs-lookup"><span data-stu-id="8ec8a-108">Go to Tax > Setup > Sales tax > Sales tax reporting codes.</span></span>
2. <span data-ttu-id="8ec8a-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="8ec8a-109">Click New.</span></span>
3. <span data-ttu-id="8ec8a-110">Wählen Sie das Berichtslayout aus, zu dem der Berichtscode gehört.</span><span class="sxs-lookup"><span data-stu-id="8ec8a-110">Select the report layout that the reporting code belongs to.</span></span>
    * <span data-ttu-id="8ec8a-111">Dieses Layout wird verwendet, um die verfügbaren Erklärungscodes für einen Mehrwertsteuercode zu filtern.</span><span class="sxs-lookup"><span data-stu-id="8ec8a-111">This layout is used to filter the available reporting codes for a Sales tax code.</span></span> <span data-ttu-id="8ec8a-112">Jeder Mehrwertsteuercode gehört zu einem Abrechnungszeitraum, der zu einer Mehrwertsteuerbehörde gehört, die ein Berichtslayout verwendet.</span><span class="sxs-lookup"><span data-stu-id="8ec8a-112">Each Sales tax code belongs to a settlement period which belongs to a Sales tax authority which uses a Report layout.</span></span>  
4. <span data-ttu-id="8ec8a-113">Geben Sie hier eine Nummer ein, die auf ein Feld im Mehrwertsteuerbericht verweist.</span><span class="sxs-lookup"><span data-stu-id="8ec8a-113">Enter a number that refers to a field on a sales tax report.</span></span>
5. <span data-ttu-id="8ec8a-114">Geben Sie im Berichtstextfeld eine Beschreibung ein, die bei Berichten angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8ec8a-114">In the Report text field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="8ec8a-115">Geben Sie im Feld "Kurze Beschreibung" eine Beschreibung für interne Zwecke ein.</span><span class="sxs-lookup"><span data-stu-id="8ec8a-115">In the Brief description field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="8ec8a-116">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="8ec8a-116">Click Save.</span></span>

