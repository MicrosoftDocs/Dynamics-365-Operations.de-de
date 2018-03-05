---
title: Einkaufsaufgaben
description: "Bei der Einkaufssteuer handelt es sich um eine Steuer auf die eingehende Mehrwertsteuer. Sie wird als prozentualer Anteil der gezahlten Mehrwertsteuer berechnet. Dieses Thema bezieht sich auf eine bestimmte Funktionserweiterung, die für juristische Personen in Österreich gilt."
author: neserovleo
manager: AnnBe
ms.date: 05/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxPurchaseTaxTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria
ms.author: v-lenest
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 92a52646063c145d733b9d2960253004e8eab80a
ms.openlocfilehash: 9c1d54606618cee47d0ecab0c86c569e16687be4
ms.contentlocale: de-de
ms.lasthandoff: 03/05/2018

---

# <a name="purchase-duties-for-austria"></a><span data-ttu-id="d0eb7-104">Einkaufssteuern für Österreich</span><span class="sxs-lookup"><span data-stu-id="d0eb7-104">Purchase duties for Austria</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d0eb7-105">Bei der Einkaufssteuer handelt es sich um eine Steuer auf die eingehende Mehrwertsteuer. Sie wird als prozentualer Anteil der gezahlten Mehrwertsteuer berechnet.</span><span class="sxs-lookup"><span data-stu-id="d0eb7-105">A purchase duty is a tax on incoming sales tax and is calculated as a percentage of the paid sales tax.</span></span> <span data-ttu-id="d0eb7-106">Dieses Thema umfasst Informationen zu Einkaufssteuern für juristische Personen mit primärer Adresse in Österreich.</span><span class="sxs-lookup"><span data-stu-id="d0eb7-106">This topic includes information about purchase duties for legal entities that have their primary address in Austria.</span></span> <span data-ttu-id="d0eb7-107">Weitere Informationen über die globale Mehrwertsteuerfunktionen finden Sie im [Mehrwertsteuerüberblick](../general-ledger/indirect-taxes-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d0eb7-107">For more information about the global sales tax functionality, see [Sales tax overview](../general-ledger/indirect-taxes-overview.md).</span></span>

<span data-ttu-id="d0eb7-108">Die Berechnung der Einkaufssteuern basiert auf Mehrwertsteuercodes.</span><span class="sxs-lookup"><span data-stu-id="d0eb7-108">The calculation of purchase duties is based on sales tax codes.</span></span> <span data-ttu-id="d0eb7-109">Um einen Mehrwertsteuercode in die Einkaufssteuerberechnung einzubeziehen, aktivieren Sie das Kontrollkästchen **Einkaufssteuer** auf der Seite **Mehrwertsteuercodes**.</span><span class="sxs-lookup"><span data-stu-id="d0eb7-109">To include a sales tax code in the purchase duty calculation, select the **Purchase duty** check box on the **Saxes tax codes** page.</span></span> 

<span data-ttu-id="d0eb7-110">Sie können Einkaufssteuereinstellungen im Menü **Steuereinstellungen** auf der Seite **Einkaufssteuer** angeben.</span><span class="sxs-lookup"><span data-stu-id="d0eb7-110">You can specify purchase duty settings on the **Tax setup** menu on the **Purchase duty** page.</span></span> <span data-ttu-id="d0eb7-111">Sie können den Bezeichner für Berechtigungen (beispielsweise **KU**), Beschreibung, Steuerbehörde und Konten, die für die Buchung verwendet werden, festlegen</span><span class="sxs-lookup"><span data-stu-id="d0eb7-111">You can set the duty identifier (for example, **KU**), description, tax authority, and accounts that will be used for posting.</span></span> <span data-ttu-id="d0eb7-112">Das Steuerkonto ist ein Bilanzkonto, in dem die Verbindlichkeiten für die Einkaufssteuer erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="d0eb7-112">Duty account is a balance account where the liability for the purchase duty is registered.</span></span> <span data-ttu-id="d0eb7-113">Das Kostenkonto ist ein Gewinn- und Verlustkonto, auf dem die Kosten gebucht werden, und ein Ausgleichskonto, wo Ausgleichstransaktionen generiert werden.</span><span class="sxs-lookup"><span data-stu-id="d0eb7-113">Cost account is a profit and loss account that the costs are posted to and a Settle account where settlement transactions will be generated.</span></span>

<span data-ttu-id="d0eb7-114">Um den Wert der Einkaufssteuer anzugeben, klicken Sie auf **Einkaufssteuerwert**, um die Seite **Einkaufssteuerwert** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d0eb7-114">To specify the value of the purchase duty, click **Purchase duty value** to open the **Purchase duty value** page.</span></span> <span data-ttu-id="d0eb7-115">Sie können den Einkaufssteuersatz in Prozent ( z. B. **0.30**) für den erforderlichen Zeitraum angeben.</span><span class="sxs-lookup"><span data-stu-id="d0eb7-115">You can specify the purchase duty percentage (for example **0,30**) for the required period.</span></span>

<span data-ttu-id="d0eb7-116">Einkaufssteuern werden generiert, wenn Sie die Mehrwertsteuer ausgleichen und buchen.</span><span class="sxs-lookup"><span data-stu-id="d0eb7-116">Purchase duties are generated when you settle and post sales taxes.</span></span> <span data-ttu-id="d0eb7-117">Sie können den Bericht **Einkaufssteuer** im Menü **Einkaufssteuererklärung** generieren.</span><span class="sxs-lookup"><span data-stu-id="d0eb7-117">You can generate the **Purchase duty** report from the **Purchase duty reporting** menu.</span></span>

