---
title: Überblick über die erweiterte Bankabstimmung
description: In diesem Artikel wird der Fluss für den erweiterten Bankabstimmungsprozess beschrieben. Mit der erweiterten Bankabstimmungsfunktion können Sie Bankauszüge importieren, die aus Bankbuchungen automatisch abgestimmt werden können.
author: panolte
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: roschlom
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 09128f33d4208bc5c987683bb881aa1129b0dc8e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985435"
---
# <a name="advanced-bank-reconciliation-overview"></a><span data-ttu-id="0b864-104">Überblick über die erweiterte Bankabstimmung</span><span class="sxs-lookup"><span data-stu-id="0b864-104">Advanced bank reconciliation overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0b864-105">In diesem Artikel wird der Fluss für den erweiterten Bankabstimmungsprozess beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0b864-105">This article describes the flow for the advanced bank reconciliation process.</span></span> <span data-ttu-id="0b864-106">Mit der erweiterten Bankabstimmungsfunktion können Sie Bankauszüge importieren, die aus Bankbuchungen automatisch abgestimmt werden können.</span><span class="sxs-lookup"><span data-stu-id="0b864-106">The advanced bank reconciliation feature lets you import bank statements that can be automatically reconciled from within bank transactions.</span></span>

<span data-ttu-id="0b864-107">Mit der erweiterten Bankabstimmungsfunktion können Sie Bankauszüge importieren.</span><span class="sxs-lookup"><span data-stu-id="0b864-107">The advanced bank reconciliation feature lets you import bank statements.</span></span> <span data-ttu-id="0b864-108">Der importierte Bankauszug kann aus Banktransaktionen heraus automatisch abgestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="0b864-108">The imported bank statement can then be automatically reconciled from within bank transactions.</span></span> <span data-ttu-id="0b864-109">Hierbei gelten die Schritte des erweiterten Bankabstimmungsflusses.</span><span class="sxs-lookup"><span data-stu-id="0b864-109">Here are the steps in the advanced bank reconciliation flow.</span></span>

1.  <span data-ttu-id="0b864-110">Richten Sie einen Bankauszugsimport ein.</span><span class="sxs-lookup"><span data-stu-id="0b864-110">Set up a bank statement import.</span></span>
    -   <span data-ttu-id="0b864-111">Importieren Sie Bankauszüge durch das Datenentitätsframework.</span><span class="sxs-lookup"><span data-stu-id="0b864-111">Import bank statements through the data entity framework.</span></span>
    -   <span data-ttu-id="0b864-112">Drei typische Bankauszugsformate sind integriert: ISO20022, BAI2 und MT940.</span><span class="sxs-lookup"><span data-stu-id="0b864-112">Three typical bank statement formats are built in: ISO20022, BAI2, and MT940.</span></span>
    -   <span data-ttu-id="0b864-113">Die Funktionen können in jedes beliebige Format erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="0b864-113">The functionality can be extended to any format.</span></span>

2.  <span data-ttu-id="0b864-114">Richten Sie einen Nummernkreis ein, der für erweiterte Bankabstimmung verwendet wird, und definieren Sie die Abgleichsregeln für Bankabstimmung.</span><span class="sxs-lookup"><span data-stu-id="0b864-114">Set up a number sequence to use for advanced bank reconciliation, and define the bank reconciliation matching rules.</span></span>
    -   <span data-ttu-id="0b864-115">Eine Abstimmungsübereinstimmungsregel ist eine Gruppe von Kriterien, die verwendet werden, um Bankauszugspositionen und Microsoft Dynamics 365 Finance-Bankdokumentpositionen während des Abstimmungsvorgangs zu filtern.</span><span class="sxs-lookup"><span data-stu-id="0b864-115">A reconciliation matching rule is a set of criteria that are used to filter bank statement lines and Microsoft Dynamics 365 Finance bank transaction lines during the reconciliation process.</span></span> <span data-ttu-id="0b864-116">Abhängig von Ihrer Geschäftspraktik können Sie mehrere Übereinstimmungsregel einrichten, die Ihren Abstimmungsprozess automatisieren und optimieren.</span><span class="sxs-lookup"><span data-stu-id="0b864-116">Depending on your business practice, you can set up more than one matching rule to automate and optimize your reconciliation process.</span></span>

3.  <span data-ttu-id="0b864-117">Stimmen Sie Bankauszüge mit Finance-Banktransaktionen ab.</span><span class="sxs-lookup"><span data-stu-id="0b864-117">Reconcile bank statements with Finance bank transactions.</span></span>
    -   <span data-ttu-id="0b864-118">Führen Sie den automatischen Abgleich und die Erstellung von Abstimmungserfassungen aus.</span><span class="sxs-lookup"><span data-stu-id="0b864-118">Perform automatic matching and creation of reconciliation journals.</span></span>
    -   <span data-ttu-id="0b864-119">Zeigen Sie Bankauszüge und Finance-Banktransaktionen parallel an.</span><span class="sxs-lookup"><span data-stu-id="0b864-119">View bank statements and Finance bank transactions side by side.</span></span>
    -   <span data-ttu-id="0b864-120">Buchen Sie Finance-Banktransaktionen automatisch, wenn sie auf einem Bankauszug aber nicht in der Finance-App angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="0b864-120">Automatically post Finance bank transactions if they appear on a bank statement but don't appear in the Finance app.</span></span>
    -   <span data-ttu-id="0b864-121">Generieren eines Abstimmungsauszugs</span><span class="sxs-lookup"><span data-stu-id="0b864-121">Generate a reconciliation statement.</span></span>





