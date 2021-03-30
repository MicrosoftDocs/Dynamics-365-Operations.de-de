---
title: Einrichten von Mehrwertsteuerbehörden
description: Mehrwertsteuerbehörden sind Entitäten, an welche die eingezogene Mehrwertsteuer gemeldet und abgeführt werden muss.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eff67bc32eafea86d0ff582c56059c28706ed2a1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222237"
---
# <a name="set-up-sales-tax-authorities"></a><span data-ttu-id="e72e9-103">Einrichten von Mehrwertsteuerbehörden</span><span class="sxs-lookup"><span data-stu-id="e72e9-103">Set up sales tax authorities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e72e9-104">Mehrwertsteuerbehörden sind Entitäten, an welche die eingezogene Mehrwertsteuer gemeldet und abgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="e72e9-104">Sales tax authorities are entities to which collected sales tax needs to be reported and paid.</span></span> <span data-ttu-id="e72e9-105">Sie können die Mehrwertsteuer direkt an die Behörde abführen oder mittels eines für die Mehrwertsteuerbehörde erstellten Kreditorenkontos.</span><span class="sxs-lookup"><span data-stu-id="e72e9-105">You can pay sales taxes to the authority directly or through a vendor account that you create for the sales tax authority.</span></span> <span data-ttu-id="e72e9-106">Dies ermöglicht dem Unternehmen die Verwendung der normalen Zahlungsroutinen zum Abführen der Mehrwertsteuer an die Mehrwertsteuerbehörde und gewährleistet eine pünktliche Zahlung.</span><span class="sxs-lookup"><span data-stu-id="e72e9-106">If you do this, the company can use its usual payment routines to pay the sales tax authority on time.</span></span> <span data-ttu-id="e72e9-107">Wird die Steuerbehörde nicht als Kreditor eingerichtet, muss am korrekten Fälligkeitsdatum eine manuelle Zahlung an die Steuerbehörde vorbereitet werden.</span><span class="sxs-lookup"><span data-stu-id="e72e9-107">If you do not set up the tax authority as a vendor, someone must prepare a manual payment to the tax authority on the appropriate due date.</span></span> <span data-ttu-id="e72e9-108">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="e72e9-108">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="e72e9-109">Wechseln Sie zu "Steuer" > "Indirekte Steuern" > "Mehrwertsteuer" > "Mehrwertsteuerbehörden".</span><span class="sxs-lookup"><span data-stu-id="e72e9-109">Go to Tax > Indirect taxes > Sales tax > Sales tax authorities.</span></span>
2. <span data-ttu-id="e72e9-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="e72e9-110">Click New.</span></span>
3. <span data-ttu-id="e72e9-111">Geben Sie im Feld "Behörde" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e72e9-111">In the Authority field, type a value.</span></span>
4. <span data-ttu-id="e72e9-112">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e72e9-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="e72e9-113">Klicken Sie im Feld "Kreditorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e72e9-113">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e72e9-114">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="e72e9-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="e72e9-115">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="e72e9-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="e72e9-116">Wählen das Berichtslayout für das Land/die Region aus (sofern verfügbar).</span><span class="sxs-lookup"><span data-stu-id="e72e9-116">Select the report layout for your country/region, if one is available.</span></span> <span data-ttu-id="e72e9-117">Wenn die Berichtslayouts nicht den Anforderungen der Mehrwertsteuerbehörde entsprechen, verwenden Sie das Standardlayout.</span><span class="sxs-lookup"><span data-stu-id="e72e9-117">If the report layouts do not correspond to the requirements of the sales tax authority, use default layout.</span></span>
9. <span data-ttu-id="e72e9-118">Geben Sie Werte im Formular "Rundung" und in den Feldern "Rundung" ein, um anzugeben, wie der zu zahlende Gesamtsteuerbetrag gerundet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e72e9-118">Enter values in the Rounding form and the Round-off fields to specify how the tax total amount to be paid should be rounded.</span></span> <span data-ttu-id="e72e9-119">Alle Rundungsdifferenzen werden zu "Konten für automatische Buchungen" gebucht, die im "Hauptbuch" eingerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="e72e9-119">Any rounding differences will be posted to Accounts for automatic transactions set up in General ledger.</span></span>
10. <span data-ttu-id="e72e9-120">Geben Sie im Feld "Rundung" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="e72e9-120">In the Round-off field, enter a number.</span></span>
11. <span data-ttu-id="e72e9-121">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="e72e9-121">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]