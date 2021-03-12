---
title: URL in POS öffnen
description: Dieses Thema bietet einen Überblick über die Verbesserungen der Produkt- und Debitorensuchfunktion in Dynamics 365 Commerce.
author: AamirAllaq
manager: AnnBe
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: e4ccb8e03d63a7bd1ab2d118d86633a8c6324d43
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965451"
---
# <a name="open-url-in-pos"></a><span data-ttu-id="cfc32-103">Öffnen der URL in POS</span><span class="sxs-lookup"><span data-stu-id="cfc32-103">Open URL in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cfc32-104">In diesem Thema wird beschrieben, wie Sie eine Schaltfläche in der Retail-Verkaufsstelle (POS) konfigurieren, um eine URL zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="cfc32-104">This topic describes how you can configure a button in Retail point of sale (POS) to open a URL.</span></span> <span data-ttu-id="cfc32-105">Diese Funktion erfordert keine Codeanpassung und kann von jemandem in einer Nicht-Entwickler-Rolle konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="cfc32-105">This feature does not require a code customization, and can be configured by someone in a non-developer role.</span></span> 

<span data-ttu-id="cfc32-106">Diese Funktion ermöglicht die Konfiguration einer Schaltfläche in POS mithilfe des Raster-Designers, um eine URL zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="cfc32-106">This feature allows configuration of a button in POS, using the button grid designer to open a URL.</span></span> <span data-ttu-id="cfc32-107">Aktuell wird diese in den folgenden Konfigurationen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="cfc32-107">Currently, this is supported in the following configurations:</span></span>

- <span data-ttu-id="cfc32-108">In neuem Fenster öffnen.</span><span class="sxs-lookup"><span data-stu-id="cfc32-108">Open in new window.</span></span>
- <span data-ttu-id="cfc32-109">Innerhalb von POS öffnen.</span><span class="sxs-lookup"><span data-stu-id="cfc32-109">Open within POS.</span></span>
- <span data-ttu-id="cfc32-110">Eine native App öffnen.</span><span class="sxs-lookup"><span data-stu-id="cfc32-110">Open a native app.</span></span>

## <a name="open-in-new-window"></a><span data-ttu-id="cfc32-111">In neuem Fenster öffnen</span><span class="sxs-lookup"><span data-stu-id="cfc32-111">Open in new window</span></span>

<span data-ttu-id="cfc32-112">Diese Konfiguration definiert, ob die URL in einem neuen Fenster oder innerhalb der App geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cfc32-112">This configuration defines whether to open the URL in a new window or within the app.</span></span> <span data-ttu-id="cfc32-113">Wenn so konfiguriert wird, dass eine Web-URL innerhalb der App geöffnet wird, sind der Seitennavigationsbereich und der obere Balken der POS sichtbar und stehen zur Benutzerinteraktion zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="cfc32-113">When configured to open a web URL within the app, the side navigation panel and top bar of POS are visible and available for user interaction.</span></span> <span data-ttu-id="cfc32-114">Wenn so konfiguriert wird, dass in einem neuen Fenster geöffnet wird, wird die URL in einem neuen App-Fenster in Modern POS für Windows geöffnet und in einer neuen Browserregisterkarte in allen anderen POS-Clients.</span><span class="sxs-lookup"><span data-stu-id="cfc32-114">When configured to open in a new window, the URL will open in a new app window on Modern POS for Windows, and in a new browser tab in all other POS clients.</span></span> <span data-ttu-id="cfc32-115">Um dies zu ermöglichen, müssen Sie die URL unter Auswahl der Option **In neuem Fenster öffnen** konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="cfc32-115">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

## <a name="open-within-pos"></a><span data-ttu-id="cfc32-116">Innerhalb von POS öffnen</span><span class="sxs-lookup"><span data-stu-id="cfc32-116">Open within POS</span></span>

<span data-ttu-id="cfc32-117">Das Öffnen einer Web-URL innerhalb von POS wird aktuell nur für Modern POS in Windows unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cfc32-117">Opening a web URL within POS is currently only supported for Modern POS on Windows.</span></span> <span data-ttu-id="cfc32-118">In anderen Clients ist diese Fähigkeit in Entwicklung und für zukünftige Updates geplant.</span><span class="sxs-lookup"><span data-stu-id="cfc32-118">On other clients, this capability is under development and planned for release in future updates.</span></span> <span data-ttu-id="cfc32-119">Um dies zu ermöglichen, müssen Sie die URL ohne Auswahl der Option **In neuem Fenster öffnen** konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="cfc32-119">To enable this, you must configure the URL with the **Open in new window** option not selected.</span></span>

## <a name="open-a-native-app"></a><span data-ttu-id="cfc32-120">Eine native App öffnen</span><span class="sxs-lookup"><span data-stu-id="cfc32-120">Open a native app</span></span>

<span data-ttu-id="cfc32-121">Diese Funktion ermöglicht zudem, Nicht-Web-URLs anzugeben, um eine native App zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="cfc32-121">This feature also allows you to specify non-web URLs to open a native app.</span></span> <span data-ttu-id="cfc32-122">Beispielsweise können Sie URL-Protokolle wie beispielsweise MailTo, SIP, Sofortnachricht oder MSTEAMS angeben, die dann von jeweiligen nativen Apps im Hostgerät gehandhabt werden können.</span><span class="sxs-lookup"><span data-stu-id="cfc32-122">For example, you can specify URL protocols such as MailTo, SIP, IM, or MSTEAMS, which can then be handled by respective native apps on the host device.</span></span> <span data-ttu-id="cfc32-123">Um dies zu ermöglichen, müssen Sie die URL unter Auswahl der Option **In neuem Fenster öffnen** konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="cfc32-123">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

- <span data-ttu-id="cfc32-124">Zu Windows-Computern sehen Sie [Standardanwendungszuordnungen exportieren oder importieren](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations), um die Standardprotokollzuordnungen festzulegen, wenn Sie Ihren Computer mithilfe von Abbildverwaltung für die Bereitstellung (DISM) einrichten.</span><span class="sxs-lookup"><span data-stu-id="cfc32-124">For Windows computers, see [Export or Import Default Application Associations](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) to set the default protocol associations if you are setting up your computer using Deployment Image Servicing and Management (DISM).</span></span>
- <span data-ttu-id="cfc32-125">Wenn Sie MDM verwenden, wie Intune, um Ihre Windows-Computer zu verwalten, finden Sie Informationen unter [Richtlinien-CSP – ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span><span class="sxs-lookup"><span data-stu-id="cfc32-125">If you are using MDM, such as Intune to manage your Windows computers, see [Policy CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span></span>
- <span data-ttu-id="cfc32-126">Wenn Sie ein Entwickler sind, der eine benutzerdefinierte Website erstellt, finden Sie Informationen unter [Die Standard-App für eine URI starten](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span><span class="sxs-lookup"><span data-stu-id="cfc32-126">If you are a developer building a custom website, see [Launch the default app for a URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span></span>

## <a name="open-a-native-app-seamlessly"></a><span data-ttu-id="cfc32-127">Eine native App problemlos öffnen</span><span class="sxs-lookup"><span data-stu-id="cfc32-127">Open a native app seamlessly</span></span>

<span data-ttu-id="cfc32-128">Windows, iOS und Android ermöglichen auch das problemlosere Öffnen von Apps, basierend auf der App-Protokollzuordnung.</span><span class="sxs-lookup"><span data-stu-id="cfc32-128">Windows, iOS, and Android also allow opening of apps more seamlessly, based on app protocol association.</span></span> <span data-ttu-id="cfc32-129">Wenn Ihre App nicht bereits dazu konfiguriert ist, das Öffnen von einem Webbrowser aus zu handhaben, benötigen Sie möglicherweise einen Entwickler, um dies zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="cfc32-129">If your app is not already configured to handle opening from a web browser, you may need a developer to configure this.</span></span>

- <span data-ttu-id="cfc32-130">Für Windows sehen Sie Informationen unter [Aktivieren von Apps für Websites mithilfe von App-URI-Handlern](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span><span class="sxs-lookup"><span data-stu-id="cfc32-130">For Windows, see [Enable apps for websites using app URI handlers](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span></span>
- <span data-ttu-id="cfc32-131">Für IOS finden Sie Informationen unter [Universelle Links für Entwickler](https://developer.apple.com/ios/universal-links/).</span><span class="sxs-lookup"><span data-stu-id="cfc32-131">For iOS, see [Universal Links for Developers](https://developer.apple.com/ios/universal-links/).</span></span>
- <span data-ttu-id="cfc32-132">Für Android finden Sie Informationen unter [Handhabung von Android-App-Links](https://developer.android.com/training/app-links/).</span><span class="sxs-lookup"><span data-stu-id="cfc32-132">For Android, see [Handling Android App Links](https://developer.android.com/training/app-links/).</span></span>

| <span data-ttu-id="cfc32-133">Kunde</span><span class="sxs-lookup"><span data-stu-id="cfc32-133">Client</span></span>                | <span data-ttu-id="cfc32-134">In neuem Fenster öffnen</span><span class="sxs-lookup"><span data-stu-id="cfc32-134">Open in new window</span></span> | <span data-ttu-id="cfc32-135">Native App öffnen</span><span class="sxs-lookup"><span data-stu-id="cfc32-135">Open native app</span></span> | <span data-ttu-id="cfc32-136">Innerhalb von POS öffnen</span><span class="sxs-lookup"><span data-stu-id="cfc32-136">Open within POS</span></span> | <span data-ttu-id="cfc32-137">Detaildaten</span><span class="sxs-lookup"><span data-stu-id="cfc32-137">Details</span></span>                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| <span data-ttu-id="cfc32-138">Modern POS auf Windows</span><span class="sxs-lookup"><span data-stu-id="cfc32-138">Modern POS on Windows</span></span> | <span data-ttu-id="cfc32-139">✓\*</span><span class="sxs-lookup"><span data-stu-id="cfc32-139">✓\*</span></span>                | <span data-ttu-id="cfc32-140">✓</span><span class="sxs-lookup"><span data-stu-id="cfc32-140">✓</span></span>               | <span data-ttu-id="cfc32-141">✓</span><span class="sxs-lookup"><span data-stu-id="cfc32-141">✓</span></span>              | <span data-ttu-id="cfc32-142">\* Wird in neuem „Modern POS”-Fenster geöffnet</span><span class="sxs-lookup"><span data-stu-id="cfc32-142">\* Opens in new Modern POS window</span></span> |
| <span data-ttu-id="cfc32-143">Cloud POS</span><span class="sxs-lookup"><span data-stu-id="cfc32-143">Cloud POS</span></span>             | <span data-ttu-id="cfc32-144">✓\*</span><span class="sxs-lookup"><span data-stu-id="cfc32-144">✓\*</span></span>                | <span data-ttu-id="cfc32-145">✓</span><span class="sxs-lookup"><span data-stu-id="cfc32-145">✓</span></span>               | <span data-ttu-id="cfc32-146">X</span><span class="sxs-lookup"><span data-stu-id="cfc32-146">X</span></span>              | <span data-ttu-id="cfc32-147">\* Wird in neuer Browserregisterkarte geöffnet</span><span class="sxs-lookup"><span data-stu-id="cfc32-147">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="cfc32-148">Modern POS auf iOS</span><span class="sxs-lookup"><span data-stu-id="cfc32-148">Modern POS on iOS</span></span>     | <span data-ttu-id="cfc32-149">✓\*</span><span class="sxs-lookup"><span data-stu-id="cfc32-149">✓\*</span></span>                | <span data-ttu-id="cfc32-150">✓</span><span class="sxs-lookup"><span data-stu-id="cfc32-150">✓</span></span>               | <span data-ttu-id="cfc32-151">X</span><span class="sxs-lookup"><span data-stu-id="cfc32-151">X</span></span>              | <span data-ttu-id="cfc32-152">\* Wird in neuer Browserregisterkarte geöffnet</span><span class="sxs-lookup"><span data-stu-id="cfc32-152">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="cfc32-153">Modern POS auf Android</span><span class="sxs-lookup"><span data-stu-id="cfc32-153">Modern POS on Android</span></span> | <span data-ttu-id="cfc32-154">✓\*</span><span class="sxs-lookup"><span data-stu-id="cfc32-154">✓\*</span></span>                | <span data-ttu-id="cfc32-155">✓</span><span class="sxs-lookup"><span data-stu-id="cfc32-155">✓</span></span>               | <span data-ttu-id="cfc32-156">X</span><span class="sxs-lookup"><span data-stu-id="cfc32-156">X</span></span>              | <span data-ttu-id="cfc32-157">\* Wird in neuer Browserregisterkarte geöffnet</span><span class="sxs-lookup"><span data-stu-id="cfc32-157">\* Opens in new browser tab</span></span>        |

## <a name="before-you-begin"></a><span data-ttu-id="cfc32-158">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="cfc32-158">Before you begin</span></span>

<span data-ttu-id="cfc32-159">Bevor Sie beginnen, überprüfen Sie, wie [Bildschirmlayouts für die Verkaufsstelle (POS)](pos-screen-layouts.md) konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="cfc32-159">Before you begin, review how to configure [Screen layouts for the point of sale (POS)](pos-screen-layouts.md).</span></span>

## <a name="open-url-in-pos"></a><span data-ttu-id="cfc32-160">URL in POS öffnen</span><span class="sxs-lookup"><span data-stu-id="cfc32-160">Open URL in POS</span></span>

<span data-ttu-id="cfc32-161">Um eine URL zu konfigurieren, die in POS geöffnet werden soll, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="cfc32-161">To configure a URL to be opened in POS, perform the following steps.</span></span>

1. <span data-ttu-id="cfc32-162">Wechseln Sie in der Zentrale zu **Einzelhandel und Handel \> Kanaleinstellungen \> POS-Einstellungen \> POS \> Bildschirmlayouts**.</span><span class="sxs-lookup"><span data-stu-id="cfc32-162">In head office, go to **Retail and Commerce \> Channel Setup \> POS Setup \> POS \> Screen Layouts**.</span></span>
2. <span data-ttu-id="cfc32-163">Wählen Sie **Schaltflächenraster \> Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="cfc32-163">Select **Button Grids \> Designer**.</span></span>
3. <span data-ttu-id="cfc32-164">Erstellen Sie eine neue Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="cfc32-164">Create a new button.</span></span>
4. <span data-ttu-id="cfc32-165">Wählen Sie die Eigenschaften **Schaltfläche** aus.</span><span class="sxs-lookup"><span data-stu-id="cfc32-165">Select **Button** properties.</span></span>
5. <span data-ttu-id="cfc32-166">Wählen Sie **URL öffnen** als die Aktivität aus.</span><span class="sxs-lookup"><span data-stu-id="cfc32-166">Select **Open URL** as the action.</span></span>
6. <span data-ttu-id="cfc32-167">Geben Sie die URL ein, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="cfc32-167">Enter the URL that you want to use.</span></span>
7. <span data-ttu-id="cfc32-168">Konfigurieren Sie, ob die URL in einem neuen Fenster geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cfc32-168">Configure whether to open the URL in a new window.</span></span>
