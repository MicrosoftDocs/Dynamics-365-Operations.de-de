---
title: Aktivieren der verzögerten Steuerberechnung in der Erfassung
description: In diesem Thema wird erläutert, wie Sie die Funktion **Verzögerte Steuerberechnung in der Erfassung aktivieren** verwenden, um die Leistung der Steuerberechnung zu verbessern, wenn die Anzahl der Erfassungspositionen groß ist.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 5a8ae30a007d3e2b8b7a9bc9eb7786f6e58246d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177871"
---
# <a name="enable-delayed-tax-calculation-on-journal"></a><span data-ttu-id="db09a-103">Aktivieren der verzögerten Steuerberechnung in der Erfassung</span><span class="sxs-lookup"><span data-stu-id="db09a-103">Enable delayed tax calculation on journal</span></span>
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="db09a-104">In diesem Thema wird erläutert, wie Sie die Funktion **Verzögerte Steuerberechnung in der Erfassung aktivieren** verwenden, um die Leistung der Steuerberechnung zu verbessern, wenn die Anzahl der Erfassungspositionen groß ist.</span><span class="sxs-lookup"><span data-stu-id="db09a-104">This topic explains how to use the **Enable delayed tax calculation on journal** feature to improve tax calculation performance when the volume of journal lines is huge.</span></span>

<span data-ttu-id="db09a-105">Das aktuelle Mehrwertsteuerberechnungsverhalten in der Erfassung wird in Echtzeit ausgelöst, wenn der Benutzer steuerbezogene Felder wie Mehrwertsteuergruppe/Artikel-Mehrwertsteuergruppe aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="db09a-105">Current sales tax calculation behavior on journal is real-time triggered when user updates tax related fields, e.g. sales tax group/item sales tax group.</span></span> <span data-ttu-id="db09a-106">Jede Aktualisierung auf Erfassungspositionsebene berechnet den Steuerbetrag für alle Erfassungspositionen neu.</span><span class="sxs-lookup"><span data-stu-id="db09a-106">Any update at journal line level will re-calculate tax amount on all journal lines.</span></span> <span data-ttu-id="db09a-107">Dies ermöglicht ermöglicht dem Benutzer die Anzeige des in Echtzeit berechneten Steuerbetrags, kann jedoch auch zu Performanceproblemen führen, wenn die Anzahl der Erfassungspositionen groß ist.</span><span class="sxs-lookup"><span data-stu-id="db09a-107">It helps user to see real-time calculated tax amount but it could also bring performance issue if  the volume of journal lines is huge.</span></span>

<span data-ttu-id="db09a-108">Diese Funktion ermöglicht das Verzögern der Steuerberechnung, um Performanceproblem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="db09a-108">This feature provides an option to delay tax calculation to solve performance issue.</span></span> <span data-ttu-id="db09a-109">Wenn diese Funktion aktiviert ist, wird der Steuerbetrag nur dann berechnet, wenn Benutzer auf den Befehl „Mehrwertsteuer“ klickt oder die Erfassung bucht.</span><span class="sxs-lookup"><span data-stu-id="db09a-109">If this feature is turned on, tax amount will only be calculated when user clicks "Sales Tax" command or posts the journal.</span></span>

<span data-ttu-id="db09a-110">Der Benutzer kann den Parameter auf drei Ebenen aktivieren/deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="db09a-110">User can turn on/off the parameter at three levels:</span></span>
- <span data-ttu-id="db09a-111">Nach juristischer Person</span><span class="sxs-lookup"><span data-stu-id="db09a-111">By legal entity</span></span>
- <span data-ttu-id="db09a-112">Nach Erfassungsname</span><span class="sxs-lookup"><span data-stu-id="db09a-112">By journal name</span></span>
- <span data-ttu-id="db09a-113">Nach Erfassungskopf</span><span class="sxs-lookup"><span data-stu-id="db09a-113">By journal header</span></span>

<span data-ttu-id="db09a-114">Das System betrachtet den Parameterwert im Erfassungskopf als endgültig.</span><span class="sxs-lookup"><span data-stu-id="db09a-114">System will take the parameter value on journal header as final.</span></span> <span data-ttu-id="db09a-115">Der Parameterwert im Erfassungskopf wird standardmäßig aus dem Erfassungsnamen entnommen.</span><span class="sxs-lookup"><span data-stu-id="db09a-115">Parameter value on journal header will be defaulted from journal name.</span></span> <span data-ttu-id="db09a-116">Der Parameterwert im Erfassungsnamen wird standardmäßig aus dem Hauptbuchparameter entnommen, wenn der Erfassungsname erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="db09a-116">Parameter value on journal name will be defaulted from general ledger parameter when the journal name is created.</span></span>

<span data-ttu-id="db09a-117">Die Felder „Tatsächlicher Mehrwertsteuerbetrag“ und „Berechneter Mehrwertsteuerbetrag“ in der Erfassung werden ausgeblendet, wenn dieser Parameter aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="db09a-117">"Actual sales tax amount" and "Calculated sales tax amount" fields on journal will be hided if this parameter is turned on.</span></span> <span data-ttu-id="db09a-118">Auf diese Weise soll eine Verwirrung des Benutzers verhindert werden, da der Wert dieser beiden Felder immer 0 ist, bevor der Benutzer die Steuerberechnung auslöst.</span><span class="sxs-lookup"><span data-stu-id="db09a-118">The purpose is not to confuse user because the value of these two fields will always show 0 before user trigger the tax calculation.</span></span>

## <a name="enable-delayed-tax-calculation-by-legal-entity"></a><span data-ttu-id="db09a-119">Aktivieren der verzögerten Steuerberechnung nach juristischer Person</span><span class="sxs-lookup"><span data-stu-id="db09a-119">Enable delayed tax calculation by legal entity</span></span>

1. <span data-ttu-id="db09a-120">Wechseln Sie zu **Hauptbuch > Hauptbucheinstellungen > Hauptbuchparameter**.</span><span class="sxs-lookup"><span data-stu-id="db09a-120">Go to **General ledger > Ledger setup > General ledger parameters**</span></span>
2. <span data-ttu-id="db09a-121">Klicken Sie auf die Registerkarte **Mehrwertsteuer**.</span><span class="sxs-lookup"><span data-stu-id="db09a-121">Click **Sales tax** tab</span></span>
3. <span data-ttu-id="db09a-122">Suchen Sie unter **Allgemeines** den Parameter **Verzögerte Steuerberechnung**, und aktivieren/deaktivieren Sie ihn.</span><span class="sxs-lookup"><span data-stu-id="db09a-122">Under **General** fast tab, find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-gl.png)



## <a name="enable-delayed-tax-calculation-by-journal-name"></a><span data-ttu-id="db09a-123">Aktivieren der verzögerten Steuerberechnung nach Erfassungsname</span><span class="sxs-lookup"><span data-stu-id="db09a-123">Enable delayed tax calculation by journal name</span></span>

1. <span data-ttu-id="db09a-124">Wechseln Sie zu **Hauptbuch > Erfassung einrichten >Erfassungsnamen**.</span><span class="sxs-lookup"><span data-stu-id="db09a-124">Go to **General ledger > Journal setup > Journal names**</span></span>
2. <span data-ttu-id="db09a-125">Suchen Sie unter **Allgemeines** den Parameter **Verzögerte Steuerberechnung**, und aktivieren/deaktivieren Sie ihn.</span><span class="sxs-lookup"><span data-stu-id="db09a-125">Under **General** fast tab, find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-journal-name.png)

## <a name="enable-delayed-tax-calculation-by-journal"></a><span data-ttu-id="db09a-126">Aktivieren der verzögerten Steuerberechnung nach Erfassung</span><span class="sxs-lookup"><span data-stu-id="db09a-126">Enable delayed tax calculation by journal</span></span>

1. <span data-ttu-id="db09a-127">Wechseln Sie zu **Hauptbuch > Erfassungseinträge > Allgemeine Erfassungen**.</span><span class="sxs-lookup"><span data-stu-id="db09a-127">Go to **General ledger > Journal entries > General journals**</span></span>
2. <span data-ttu-id="db09a-128">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="db09a-128">Click **New**</span></span>
3. <span data-ttu-id="db09a-129">Auswählen eines Erfassungsnamens</span><span class="sxs-lookup"><span data-stu-id="db09a-129">Select a journal name</span></span>
4. <span data-ttu-id="db09a-130">Klicken Sie auf **Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="db09a-130">Click **Setup**</span></span>
5. <span data-ttu-id="db09a-131">Suchen Sie den Paramater **Verzögerte Steuerberechnung**, und aktivieren/deaktivieren Sie ihn.</span><span class="sxs-lookup"><span data-stu-id="db09a-131">Find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-journal-header.png)
