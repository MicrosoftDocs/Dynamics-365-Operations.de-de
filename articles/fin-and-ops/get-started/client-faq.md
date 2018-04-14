---
title: "Finance and Operations-Client – FAQ"
description: "Dieser Artikel enthält Antworten auf häufig gestellte Fragen zum Microsoft Dynamics 365 for Finance and Operations-Client."
author: jasongre
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 12334
ms.assetid: a9a57f0e-a67c-46b1-83c9-5d6350fb3b86
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6f65b0ea66b4ce876e4a7d1cbf7125b5241c1e20
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---

# <a name="finance-and-operations-client-faq"></a><span data-ttu-id="68d99-103">Finance and Operations-Client – FAQ</span><span class="sxs-lookup"><span data-stu-id="68d99-103">Finance and Operations client FAQ</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="68d99-104">Dieser Artikel enthält Antworten auf häufig gestellte Fragen zum Microsoft Dynamics 365 for Finance and Operations-Client.</span><span class="sxs-lookup"><span data-stu-id="68d99-104">This article provides answers to frequently asked questions about the Microsoft Dynamics 365 for Finance and Operations client.</span></span>

<a name="why-arent-symbols-loaded-when-i-use-finance-and-operations"></a><span data-ttu-id="68d99-105">Warum werden Symbole nicht geladen, wenn ich Dynamics 365 for Finance and Operations verwende?</span><span class="sxs-lookup"><span data-stu-id="68d99-105">Why aren't symbols loaded when I use Finance and Operations?</span></span>
-----------------------------------------------------------------

<span data-ttu-id="68d99-106">Die Sicherheitseinstellungen in Ihrem Browser verhinderten möglicherweise, das die Symbole ordnungsgemäß geladen werden.</span><span class="sxs-lookup"><span data-stu-id="68d99-106">The security settings on your browser might prevent the symbols from being loaded correctly.</span></span> <span data-ttu-id="68d99-107">Zur Behebung dieses Problems wird Folgendes empfohlen:</span><span class="sxs-lookup"><span data-stu-id="68d99-107">To resolve this issue, try the following steps:</span></span>

-   <span data-ttu-id="68d99-108">Falls dieses Problem in Internet Explorer ermitteln, klicken Sie **Tools**, und klicken Sie dann **Internetoptione**.</span><span class="sxs-lookup"><span data-stu-id="68d99-108">If you're experiencing this issue in Internet Explorer, click **Tools**, and then click **Internet Options**.</span></span>  <span data-ttu-id="68d99-109">Im Internetoptionsdialogfeld **Datenschutz** auf der Registerkarte, klicken Sie **Benutzerdefinierte  Ebene** an, und vergewissern Sie sich, dass die **Schriftartdownload** Option ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="68d99-109">In the Internet Options dialog box, on the **Privacy** tab, click **Custom level**, and make sure the **Font download** option is selected.</span></span>
-   <span data-ttu-id="68d99-110">Andernfalls müssen Sie möglicherweise die Finance and Operations-Website der Liste der vertrauenswürdigen Standorte hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="68d99-110">Otherwise, you might have to add the Finance and Operations site to the list of trusted sites.</span></span>

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a><span data-ttu-id="68d99-111">Ich vermisse das Menüband von Microsoft Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="68d99-111">I miss the ribbon from Dynamics AX 2012.</span></span> <span data-ttu-id="68d99-112">Kann ich Registerkarten ständig offen anhalten?</span><span class="sxs-lookup"><span data-stu-id="68d99-112">Can I keep Action Pane tabs open all the time?</span></span>
<span data-ttu-id="68d99-113">Wir planen, diese Funktion bald zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="68d99-113">We are planning to implement this feature soon.</span></span> <span data-ttu-id="68d99-114">Die Benutzer können dann angeben, ob die Registerkarten im Aktivitätsbereichen ständig offen sein soll.</span><span class="sxs-lookup"><span data-stu-id="68d99-114">Users will then be able to choose to keep the tabs on Action Panes open all the time.</span></span> <span data-ttu-id="68d99-115">Andernfalls werden die Registerkarten reduziert wenn sie nicht verwendet werden, um mehr Platz für die Seite zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="68d99-115">Otherwise, the tabs will be collapsed when they aren't being used, to gain more screen space for the page.</span></span>

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-right-click"></a><span data-ttu-id="68d99-116">Warum sehe ich manchmal andere Kontextmenüs, wenn mit rechts klicke?</span><span class="sxs-lookup"><span data-stu-id="68d99-116">Why do I sometimes see different shortcut menus when I right click?</span></span>
<span data-ttu-id="68d99-117">Wenn Sie mit rechts auf ein bearbeitbares Feld klicken, oder wenn Text markiert ist, wird das Kontextmenü des Browsers angezeigt.</span><span class="sxs-lookup"><span data-stu-id="68d99-117">If you right-click in an editable field (or if text is selected), the browser's shortcut menu is displayed.</span></span> <span data-ttu-id="68d99-118">Dieses Menü ermöglicht das **Ausschneiden**, **Kopieren** und **Einfügen**.</span><span class="sxs-lookup"><span data-stu-id="68d99-118">This menu gives you access to the **Cut**, **Copy**, and **Paste** commands.</span></span> <span data-ttu-id="68d99-119">Wir können diese Befehle nicht in die Kontextmenüs von Finance and Operations einbetten, da Browser aus Sicherheitsgründen den programmgesteuerten Zugriff auf die Systemzwischenablage nicht gestatten.</span><span class="sxs-lookup"><span data-stu-id="68d99-119">We can't embed these commands into the Finance and Operations shortcut menus because, for security reasons, browsers don’t allow us to programmatically access the system clipboard.</span></span>

<span data-ttu-id="68d99-120">Wenn Sie mit rechts auf eine Feldbezeichnung oder auf den Wert eines schreibgeschützten Steuerelements klicken, erhalten Sie das Finance and Operations-Kontextmenü.</span><span class="sxs-lookup"><span data-stu-id="68d99-120">If you right-click a field label or the value of a read-only control, you'll see the Finance and Operations shortcut menu.</span></span>

<span data-ttu-id="68d99-121">Um den Tastaturzugriff zu vereinfachen, planen wir eine Tastenkombination zu implementieren, die das Kontextmenü von Finance and Operations öffnet.</span><span class="sxs-lookup"><span data-stu-id="68d99-121">To make keyboard access easier, we plan to implement a keyboard shortcut in the future that will open the Finance and Operations shortcut menu.</span></span>

## <a name="where-is-the-view-details-functionality-in-finance-and-operations"></a><span data-ttu-id="68d99-122">Wo ist in Finance and Operations die "Details anzeigen"-Funktion?</span><span class="sxs-lookup"><span data-stu-id="68d99-122">Where is the View details functionality in Finance and Operations?</span></span>
<span data-ttu-id="68d99-123">Die **Details anzeigen**-Option ist auf mehrere Arten verfügbar:</span><span class="sxs-lookup"><span data-stu-id="68d99-123">The **View details** option is available in a couple of ways:</span></span>

-   <span data-ttu-id="68d99-124">Wenn ein Steuerelemente die Funktionen **Details anzeigen** hat, und wenn das Steuerelement einen Wert enthält, dann wird der Wert als Link angezeigt.</span><span class="sxs-lookup"><span data-stu-id="68d99-124">If a control has **View details** capabilities, and if the control has a value, that value is displayed as a hyperlink.</span></span> <span data-ttu-id="68d99-125">Sie können auf die Verknüpfung klicken, um die Seite zu öffnen, die zusätzliche Details enthält.</span><span class="sxs-lookup"><span data-stu-id="68d99-125">You can click the hyperlink to open a page that contains additional details.</span></span>
-   <span data-ttu-id="68d99-126">**Details anzeigen** ist außerdem eine Option in den Kontextmenüs von Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="68d99-126">**View details** is also an option on Finance and Operations shortcut menus.</span></span> <span data-ttu-id="68d99-127">Weitere Informationen zur Anzeige von Finance and Operations-Kontextmenü beim Rechtsklick finden Sie im vorherigen Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="68d99-127">For more information about when Finance and Operations shortcut menus are displayed when you right-click, see the previous section.</span></span>





