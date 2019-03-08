---
title: Kostenkategorien, die in der Produktionssteuerung und in der Projektverwaltungsbuchhaltung verwendet werden
description: Bestimmte Arten von Produktionsarbeiten beziehen sich auch auf Vorkalkulationen und Berichte in Bezug auf den Projektzeitaufwand. Dieser Artikel bietet Informationen zu den Kostenkategorien, die Sie für diese Arten von Produktionsarbeiten für Produktion und Projektzwecke definieren müssen.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCategory
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 78253
ms.assetid: cfdd58a0-8afa-4a6f-a208-a76e2c162429
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cab4629740e92f9075b7afc7a5d228b2e01c4664
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "326031"
---
# <a name="cost-categories-used-in-production-control-and-project-management-accounting"></a><span data-ttu-id="dff2f-104">Kostenkategorien in der Produktionssteuerung und in der Projektverwaltung und -buchhaltung</span><span class="sxs-lookup"><span data-stu-id="dff2f-104">Cost categories used in Production control and Project management accounting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dff2f-105">Bestimmte Arten von Produktionsarbeiten beziehen sich auch auf Vorkalkulationen und Berichte in Bezug auf den Projektzeitaufwand.</span><span class="sxs-lookup"><span data-stu-id="dff2f-105">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="dff2f-106">Dieser Artikel bietet Informationen zu den Kostenkategorien, die Sie für diese Arten von Produktionsarbeiten für Produktion und Projektzwecke definieren müssen.</span><span class="sxs-lookup"><span data-stu-id="dff2f-106">This article provides information about the cost categories that you must define for these types of production work for production and project purposes.</span></span>

<span data-ttu-id="dff2f-107">Bestimmte Arten von Produktionsarbeiten beziehen sich auch auf Vorkalkulationen und Berichte in Bezug auf den Projektzeitaufwand.</span><span class="sxs-lookup"><span data-stu-id="dff2f-107">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="dff2f-108">In diesem Fall ist eine Kostenkategorie für die Produktion und die Projektzwecke erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dff2f-108">In this case, a cost category is required for production and project purposes.</span></span> <span data-ttu-id="dff2f-109">Wenn eine Kostenkategorie in der Produktion und in Projekten verwendet werdeb, müssen zusätzliche, projektbezogene Informationen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="dff2f-109">When a cost category is used in production and projects, additional project-related information must be defined.</span></span> <span data-ttu-id="dff2f-110">So können sich beispielsweise die Stundenkosten, die Projekten zugeordnet sind, von den Stundenkosten für die Produktion unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="dff2f-110">For example, the hourly costs that are associated with projects can differ from the hourly costs that are associated with production.</span></span> <span data-ttu-id="dff2f-111">Verwenden Sie die Seite **Kostenkategorien**, um eine Kostenkategorie zu definieren, die in der Produktionssteuerung und in der Projektverwaltung und -buchhaltung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dff2f-111">You can use the **Cost categories** page to define a cost category that is used in Production control and Project management accounting.</span></span> 

<span data-ttu-id="dff2f-112">**Hinweis:** Die Kostenrechnung enthält zwar die Seite **Projektkategorien**, diese steht jedoch in keinerlei Zusammenhang mit den in diesem Thema beschriebenen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="dff2f-112">**Note:** Cost accounting has a **Project categories** page, but this page has no relationship to the functionality that is described in this topic.</span></span> <span data-ttu-id="dff2f-113">Wenn Sie eine Kostenkategorie in Projekten verwenden, hat die Seite **Kostenkategorien** zusätzliche Registerkarten, die zusätzliche projektbezogene Informationen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="dff2f-113">When you use a cost category in projects, the **Cost categories** page has additional tabs that show additional project-related information.</span></span> <span data-ttu-id="dff2f-114">Zu diesen Informationen gehören die Kategoriegruppe, ein Abrechnungscode und Sachkonten, die der Kostenkategorie zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="dff2f-114">This information includes the category group, a line property, and ledger accounts that are assigned to the cost category.</span></span>

-   <span data-ttu-id="dff2f-115">Die Kostenkategorie muss einer Kategoriegruppe zugewiesen werden, in der der Buchungstyp **Stunden** unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="dff2f-115">The cost category must be assigned to a category group that supports a transaction type of **Hours**.</span></span>
-   <span data-ttu-id="dff2f-116">Die Abrechnungscodes geben Standardinformationen an, auf welche Weise gemeldete Zeiten für ein Projekt in Rechnung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="dff2f-116">The line property indicates default information about how reported time can be charged to a project.</span></span>
-   <span data-ttu-id="dff2f-117">Üblicherweise werden die kosten- und verkaufsbezogenen Sachkonten für die Kategoriegruppe definiert, die der Kostenkategorie zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="dff2f-117">Typically, the ledger accounts that are related to costs and sales are defined for the category group that is assigned to the cost category.</span></span> <span data-ttu-id="dff2f-118">Für eine einzelne Kostenkategorie können jedoch auch individuelle Konten definiert werden.</span><span class="sxs-lookup"><span data-stu-id="dff2f-118">However, specific accounts can be defined for an individual cost category.</span></span>

<span data-ttu-id="dff2f-119">Zusätzliche Schaltflächen auf der Seite **Kostenkategorien** ermöglichen Ihnen den Zugriff auf projektbezogene Informationen zu einer ausgewählten Kostenkategorie.</span><span class="sxs-lookup"><span data-stu-id="dff2f-119">Additional buttons on the **Cost categories** page let you access project-related information about a selected cost category.</span></span> <span data-ttu-id="dff2f-120">Durch Klicken auf die Schaltflächen lassen sich beispielsweise projektbezogene Buchungen anzeigen sowie Mitarbeiter oder Projekte, Kosten pro Stunde und Verkaufspreise definieren und Berichte anzeigen.</span><span class="sxs-lookup"><span data-stu-id="dff2f-120">For example, you can view project-related transactions, define employees or projects, define hourly costs and sales prices, and view reports.</span></span>



