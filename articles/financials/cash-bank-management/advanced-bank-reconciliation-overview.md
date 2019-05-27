---
title: Überblick über die erweiterte Bankabstimmung
description: In diesem Artikel wird der Fluss für den erweiterten Bankabstimmungsprozess beschrieben. Mit der erweiterten Bankabstimmungsfunktion können Sie Bankauszüge importieren, die aus Bankbuchungen automatisch abgestimmt werden können.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c6cec76ebc8328f221ecb6c30ae93716bd9bfe9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546500"
---
# <a name="advanced-bank-reconciliation-overview"></a><span data-ttu-id="b9753-104">Überblick über die erweiterte Bankabstimmung</span><span class="sxs-lookup"><span data-stu-id="b9753-104">Advanced bank reconciliation overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9753-105">In diesem Artikel wird der Fluss für den erweiterten Bankabstimmungsprozess beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b9753-105">This article describes the flow for the advanced bank reconciliation process.</span></span> <span data-ttu-id="b9753-106">Mit der erweiterten Bankabstimmungsfunktion können Sie Bankauszüge importieren, die aus Bankbuchungen automatisch abgestimmt werden können.</span><span class="sxs-lookup"><span data-stu-id="b9753-106">The advanced bank reconciliation feature lets you import bank statements that can be automatically reconciled from within bank transactions.</span></span>

<span data-ttu-id="b9753-107">Mit der erweiterten Bankabstimmungsfunktion können Sie Bankauszüge importieren.</span><span class="sxs-lookup"><span data-stu-id="b9753-107">The advanced bank reconciliation feature lets you import bank statements.</span></span> <span data-ttu-id="b9753-108">Der importierte Bankauszug kann aus Banktransaktionen heraus automatisch abgestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="b9753-108">The imported bank statement can then be automatically reconciled from within bank transactions.</span></span> <span data-ttu-id="b9753-109">Hierbei gelten die Schritte des erweiterten Bankabstimmungsflusses.</span><span class="sxs-lookup"><span data-stu-id="b9753-109">Here are the steps in the advanced bank reconciliation flow.</span></span>

1.  <span data-ttu-id="b9753-110">Richten Sie einen Bankauszugsimport ein.</span><span class="sxs-lookup"><span data-stu-id="b9753-110">Set up a bank statement import.</span></span>
    -   <span data-ttu-id="b9753-111">Importieren Sie Bankauszüge durch das Datenentitätsframework.</span><span class="sxs-lookup"><span data-stu-id="b9753-111">Import bank statements through the data entity framework.</span></span>
    -   <span data-ttu-id="b9753-112">Drei typische Bankauszugsformate sind integriert: ISO20022, BAI2 und MT940.</span><span class="sxs-lookup"><span data-stu-id="b9753-112">Three typical bank statement formats are built in: ISO20022, BAI2, and MT940.</span></span>
    -   <span data-ttu-id="b9753-113">Die Funktionen können in jedes beliebige Format erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="b9753-113">The functionality can be extended to any format.</span></span>

2.  <span data-ttu-id="b9753-114">Richten Sie einen Nummernkreis ein, der für erweiterte Bankabstimmung verwendet wird, und definieren Sie die Abgleichsregeln für Bankabstimmung.</span><span class="sxs-lookup"><span data-stu-id="b9753-114">Set up a number sequence to use for advanced bank reconciliation, and define the bank reconciliation matching rules.</span></span>
    -   <span data-ttu-id="b9753-115">Eine Abstimmungsübereinstimmungsregel ist eine Gruppe von Kriterien, die verwendet werden, um Bankauszugspositionen und Microsoft Dynamics 365 for Finance and Operations-Bankdokumentpositionen während des Abstimmungsvorgangs zu filtern.</span><span class="sxs-lookup"><span data-stu-id="b9753-115">A reconciliation matching rule is a set of criteria that are used to filter bank statement lines and Microsoft Dynamics 365 for Finance and Operations bank transaction lines during the reconciliation process.</span></span> <span data-ttu-id="b9753-116">Abhängig von Ihrer Geschäftspraktik können Sie mehrere Übereinstimmungsregel einrichten, die Ihren Abstimmungsprozess automatisieren und optimieren.</span><span class="sxs-lookup"><span data-stu-id="b9753-116">Depending on your business practice, you can set up more than one matching rule to automate and optimize your reconciliation process.</span></span>

3.  <span data-ttu-id="b9753-117">Stimmen Sie Bankauszüge mit Finance and Operations Banktransaktionen ab.</span><span class="sxs-lookup"><span data-stu-id="b9753-117">Reconcile bank statements with Finance and Operations bank transactions.</span></span>
    -   <span data-ttu-id="b9753-118">Führen Sie den automatischen Abgleich und die Erstellung von Abstimmungserfassungen aus.</span><span class="sxs-lookup"><span data-stu-id="b9753-118">Perform automatic matching and creation of reconciliation journals.</span></span>
    -   <span data-ttu-id="b9753-119">Zeigen Sie Bankauszüge und Finance and Operations-Banktransaktionen parallel an.</span><span class="sxs-lookup"><span data-stu-id="b9753-119">View bank statements and Finance and Operations bank transactions side by side.</span></span>
    -   <span data-ttu-id="b9753-120">Buchen Sie Finance and Operations-Banktransaktionen automatisch, wenn sie auf einem Bankauszug aber nicht in Finance and Operations angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b9753-120">Automatically post Finance and Operations bank transactions if they appear on a bank statement but don't appear in Finance and Operations.</span></span>
    -   <span data-ttu-id="b9753-121">Generieren eines Abstimmungsauszugs</span><span class="sxs-lookup"><span data-stu-id="b9753-121">Generate a reconciliation statement.</span></span>





