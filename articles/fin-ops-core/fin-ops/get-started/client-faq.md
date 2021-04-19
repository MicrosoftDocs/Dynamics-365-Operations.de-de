---
title: Kunden-FAQs
description: Dieser Artikel enthält Antworten auf häufig gestellte Fragen zum Finance and Operations-Client.
author: jasongre
ms.date: 09/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 12334
ms.assetid: a9a57f0e-a67c-46b1-83c9-5d6350fb3b86
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f4311e93505f1d59f6beeae01a2a2e796ad47cd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749220"
---
# <a name="client-faq"></a><span data-ttu-id="57393-103">Kunden-FAQ</span><span class="sxs-lookup"><span data-stu-id="57393-103">Client FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="57393-104">Dieser Artikel enthält Antworten auf häufig gestellte Fragen zum Finance and Operations-Client.</span><span class="sxs-lookup"><span data-stu-id="57393-104">This article provides answers to frequently asked questions about the Finance and Operations client.</span></span>

## <a name="why-arent-symbols-loaded"></a><span data-ttu-id="57393-105">Warum werden keine Symbole geladen?</span><span class="sxs-lookup"><span data-stu-id="57393-105">Why aren't symbols loaded?</span></span>

<span data-ttu-id="57393-106">Die Sicherheitseinstellungen in Ihrem Browser verhinderten möglicherweise, das die Symbole ordnungsgemäß geladen werden.</span><span class="sxs-lookup"><span data-stu-id="57393-106">The security settings on your browser might prevent the symbols from being loaded correctly.</span></span> <span data-ttu-id="57393-107">Zur Behebung dieses Problems wird Folgendes empfohlen:</span><span class="sxs-lookup"><span data-stu-id="57393-107">To resolve this issue, try the following steps:</span></span>

- <span data-ttu-id="57393-108">Falls dieses Problem in Internet Explorer auftritt, klicken Sie auf **Tools**, und klicken Sie dann auf **Internetoptionen**.</span><span class="sxs-lookup"><span data-stu-id="57393-108">If you're experiencing this issue in Internet Explorer, click **Tools**, and then click **Internet Options**.</span></span> <span data-ttu-id="57393-109">Im Internetoptionsdialogfeld **Datenschutz** auf der Registerkarte, klicken Sie **Benutzerdefinierte  Ebene** an, und vergewissern Sie sich, dass die **Schriftartdownload** Option ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="57393-109">In the Internet Options dialog box, on the **Privacy** tab, click **Custom level**, and make sure the **Font download** option is selected.</span></span>
- <span data-ttu-id="57393-110">Andernfalls müssen Sie möglicherweise die App-Website der Liste der vertrauenswürdigen Standorte hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="57393-110">Otherwise, you might have to add the app site to the list of trusted sites.</span></span>

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a><span data-ttu-id="57393-111">Ich vermisse das Menüband von Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="57393-111">I miss the ribbon from Dynamics AX 2012.</span></span> <span data-ttu-id="57393-112">Kann ich Registerkarten ständig offen anhalten?</span><span class="sxs-lookup"><span data-stu-id="57393-112">Can I keep Action Pane tabs open all the time?</span></span>

<span data-ttu-id="57393-113">Wir planen, diese Funktion bald zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="57393-113">We are planning to implement this feature soon.</span></span> <span data-ttu-id="57393-114">Die Benutzer können dann angeben, ob die Registerkarten im Aktivitätsbereichen ständig offen sein soll.</span><span class="sxs-lookup"><span data-stu-id="57393-114">Users will then be able to choose to keep the tabs on Action Panes open all the time.</span></span> <span data-ttu-id="57393-115">Andernfalls werden die Registerkarten reduziert wenn sie nicht verwendet werden, um mehr Platz für die Seite zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="57393-115">Otherwise, the tabs will be collapsed when they aren't being used, to gain more screen space for the page.</span></span>

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-right-click"></a><span data-ttu-id="57393-116">Warum sehe ich manchmal andere Kontextmenüs, wenn mit rechts klicke?</span><span class="sxs-lookup"><span data-stu-id="57393-116">Why do I sometimes see different shortcut menus when I right click?</span></span>

<span data-ttu-id="57393-117">Wenn Sie mit rechts auf ein bearbeitbares Feld klicken, oder wenn Text markiert ist, wird das Kontextmenü des Browsers angezeigt.</span><span class="sxs-lookup"><span data-stu-id="57393-117">If you right-click in an editable field (or if text is selected), the browser's shortcut menu is displayed.</span></span> <span data-ttu-id="57393-118">Dieses Menü ermöglicht das **Ausschneiden**, **Kopieren** und **Einfügen**.</span><span class="sxs-lookup"><span data-stu-id="57393-118">This menu gives you access to the **Cut**, **Copy**, and **Paste** commands.</span></span> <span data-ttu-id="57393-119">Wir können diese Befehle aus Sicherheitsgründen nicht in die Kontextmenüs einbetten, da die Browser den programmgesteuerten Zugriff auf die Systemzwischenablage nicht gestatten.</span><span class="sxs-lookup"><span data-stu-id="57393-119">We can't embed these commands into the shortcut menus because, for security reasons, browsers don't allow us to programmatically access the system clipboard.</span></span>

<span data-ttu-id="57393-120">Wenn Sie mit der rechten Maustaste auf eine Feldbezeichnung oder auf den Wert eines schreibgeschützten Steuerelements klicken, erhalten Sie das Kontextmenü.</span><span class="sxs-lookup"><span data-stu-id="57393-120">If you right-click a field label or the value of a read-only control, you'll see the shortcut menu.</span></span>

<span data-ttu-id="57393-121">Um den Tastaturzugriff zu vereinfachen, planen wir, eine Tastenkombination zu implementieren, die das Kontextmenü öffnet.</span><span class="sxs-lookup"><span data-stu-id="57393-121">To make keyboard access easier, we plan to implement a keyboard shortcut in the future that will open the shortcut menu.</span></span>

## <a name="where-is-the-view-details-functionality"></a><span data-ttu-id="57393-122">Wo ist die Funktion „Details anzeigen”?</span><span class="sxs-lookup"><span data-stu-id="57393-122">Where is the View details functionality?</span></span>

<span data-ttu-id="57393-123">Die **Details anzeigen**-Option ist auf mehrere Arten verfügbar:</span><span class="sxs-lookup"><span data-stu-id="57393-123">The **View details** option is available in a couple of ways:</span></span>

- <span data-ttu-id="57393-124">Wenn ein Steuerelemente die Funktionen **Details anzeigen** hat, und wenn das Steuerelement einen Wert enthält, dann wird der Wert als Link angezeigt.</span><span class="sxs-lookup"><span data-stu-id="57393-124">If a control has **View details** capabilities, and if the control has a value, that value is displayed as a hyperlink.</span></span> <span data-ttu-id="57393-125">Sie können auf die Verknüpfung klicken, um die Seite zu öffnen, die zusätzliche Details enthält.</span><span class="sxs-lookup"><span data-stu-id="57393-125">You can click the hyperlink to open a page that contains additional details.</span></span>
- <span data-ttu-id="57393-126">**Details anzeigen** ist außerdem eine Option in den Kontextmenüs.</span><span class="sxs-lookup"><span data-stu-id="57393-126">**View details** is also an option on shortcut menus.</span></span> <span data-ttu-id="57393-127">Weitere Informationen zur Anzeige von Kontextmenüs, die beim Rechtsklick angezeigt werden, finden Sie im vorherigen Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="57393-127">For more information about when shortcut menus are displayed when you right-click, see the previous section.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]