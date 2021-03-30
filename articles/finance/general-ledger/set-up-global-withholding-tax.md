---
title: Globale Quellensteuer einrichten
description: In diesem Thema werden die Schritte zum Einrichten der globalen Quellensteuer für Verkäufe und Käufe aufgeführt.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
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
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 00c472e90f4926c52ffe9b19661e68cbfa6bd493
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204832"
---
# <a name="set-up-global-withholding-tax"></a><span data-ttu-id="21f71-103">Globale Quellensteuer einrichten</span><span class="sxs-lookup"><span data-stu-id="21f71-103">Set up global withholding tax</span></span>

<span data-ttu-id="21f71-104">In diesem Thema werden die Schritte zum Einrichten der globalen Quellensteuer für Verkäufe und Käufe aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="21f71-104">This topic lists the steps for setting up global withholding tax for sales and purchases.</span></span> 

1. <span data-ttu-id="21f71-105">Richten Sie Quellensteuerbehörden auf der Seite **Quellensteuerbehörden** ein.</span><span class="sxs-lookup"><span data-stu-id="21f71-105">Set up withholding tax authorities on the **Withholding tax authorities** page.</span></span>

2. <span data-ttu-id="21f71-106">Richten Sie Einrichten von Quellensteuerausgleichsperioden auf der Seite **Quellensteuerausgleichsperioden** ein.</span><span class="sxs-lookup"><span data-stu-id="21f71-106">Set up withholding settlement periods on the **Withholding tax settlement periods** page.</span></span>

3. <span data-ttu-id="21f71-107">Richten Sie eine Quellensteuer-Sachkontobuchungsgruppe auf der Seite **Quellensteuer > Sachkontobuchungsgruppe** ein.</span><span class="sxs-lookup"><span data-stu-id="21f71-107">Set up withholding ledger posting group on the **Withholding tax > ledger posting group** page.</span></span>

   > [!Note] 
   >
   > <span data-ttu-id="21f71-108">Das **Quellensteuer**-Konto wird einem Hauptkonto mit **Buchungstyp** „Quellensteuer“ zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="21f71-108">**Withholding tax** account will be assigned with a main account with **Posting type** of Withholding tax.</span></span> <span data-ttu-id="21f71-109">Das **Quellensteuer-Gegenkonto** wird ebenfalls einem Hauptkonto mit dem **Buchungstyp** „Quellensteuer-Gegenkonto“ zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="21f71-109">**Withholding tax offset** account will also be assigned with a main account with **Posting type** "Withholding tax offset".</span></span> <span data-ttu-id="21f71-110">Rufen Sie **Hauptbuch > Kontenplan> Konten > Hauptkonten** auf, und richten Sie den **Buchungstyp** im Unterformular **Buchungsprüfung** für die Hauptkonten ein.</span><span class="sxs-lookup"><span data-stu-id="21f71-110">Go to **General ledger > Chart of accounts > Accounts > Main accounts**, set up the **Posting type** in the **Posting validation** sub-form for the main accounts.</span></span>

4. <span data-ttu-id="21f71-111">Richten Sie Quellensteuercodes auf der Seite **Quellensteuercodes** ein.</span><span class="sxs-lookup"><span data-stu-id="21f71-111">Set up withholding tax codes on the **Withholding tax codes** page.</span></span>

5. <span data-ttu-id="21f71-112">Richten Sie Quellensteuergruppen auf der Seite **Quellensteuergruppen** ein.</span><span class="sxs-lookup"><span data-stu-id="21f71-112">Set up withholding tax groups on the **Withholding tax groups** page.</span></span>

6. <span data-ttu-id="21f71-113">Richten Sie Quellensteuer-Umsatzerlöstypen auf der Seite **Quellensteuerumsatz** **Typen** ein.</span><span class="sxs-lookup"><span data-stu-id="21f71-113">Set up withholding tax revenue types on the **Withholding tax revenue** **types** page.</span></span>

7. <span data-ttu-id="21f71-114">Richten Sie Quellensteuergruppen auf der Seite **Artikel-Quellensteuergruppen** für einen Artikel oder eine Dienstleistung ein.</span><span class="sxs-lookup"><span data-stu-id="21f71-114">Set up withholding tax groups on the **Item withholding tax groups** page for an item or service.</span></span>

8. <span data-ttu-id="21f71-115">Richten Sie **Mindestrechnungsbetrag** auf der Seite **Hauptbuchparameter > Quellensteuer** ein.</span><span class="sxs-lookup"><span data-stu-id="21f71-115">Set up **Minimum invoice amount** on the **General ledger parameters > Withholding tax** page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]