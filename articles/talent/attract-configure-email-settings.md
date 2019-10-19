---
title: 'Konfigurieren von E-Mail-Einstellungen in Microsoft Dynamics 365 Talent: Attract'
description: 'In diesem Thema wird erläutert, wie Einstellungen für E-Mail konfiguriert werden, die von Microsoft Dynamcis 365 Talent: Attract gesendet werden.'
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c891a36f01d36774bd921475fa5995d207cd2d51
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008661"
---
# <a name="configure-email-settings"></a><span data-ttu-id="96dc9-103">E-Mail-Einstellungen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="96dc9-103">Configure email settings</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="96dc9-104">Ihre Marke etabliert die Vertrauen und hilft Ihnen eine Beziehung mit Kandidaten aufzubauen, bevor sie sich auf Ihre Positionen bewerben.</span><span class="sxs-lookup"><span data-stu-id="96dc9-104">Your brand establishes trust and helps you build a relationship with candidates before they even apply for your positions.</span></span> <span data-ttu-id="96dc9-105">Positives Markenbewusstsein zieht beste Talente an und erhöht die Loyalität bestehender Mitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="96dc9-105">Positive brand perception attracts top talent and increases the loyalty of existing employees.</span></span> <span data-ttu-id="96dc9-106">Mit Microsoft Dynamics 365 Talent: Attract können Sie E-Mails so konfigurieren, dass sie der Marke Ihres Unternehmens entsprechen.</span><span class="sxs-lookup"><span data-stu-id="96dc9-106">Microsoft Dynamics 365 Talent: Attract lets you configure emails so that they reflect your company's brand.</span></span> <span data-ttu-id="96dc9-107">Daher können Sie Bewerbern eine konsistente Erfahrung bei deren Fortschritt durch den Bewerbungsprozess bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="96dc9-107">Therefore, you can provide a consistent experience to job candidates as they progress through the application process.</span></span>

<span data-ttu-id="96dc9-108">Mit Attract können Sie diese Aktivitäten ausführen:</span><span class="sxs-lookup"><span data-stu-id="96dc9-108">Attract lets you perform these actions:</span></span>

- <span data-ttu-id="96dc9-109">Konfigurieren Sie E-Mail-Einstellungen, so dass das Microsoft Exchange-E-Mail-Service-Konto Ihres Unternehmens verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="96dc9-109">Configure email settings so that your company's Microsoft Exchange email service account is used.</span></span> <span data-ttu-id="96dc9-110">Hierdurch wissen Kandidaten, dass die E-Mails aus Ihrem Unternehmen stammen.</span><span class="sxs-lookup"><span data-stu-id="96dc9-110">In this way, candidates know that the emails are coming from your company.</span></span> <span data-ttu-id="96dc9-111">So können Sie die Einstellungen beispielsweise so konfigurieren, dass Kandidaten E-Mails von `recruiting@contoso.com` statt von `contoso@microsoft.com`erhalten.</span><span class="sxs-lookup"><span data-stu-id="96dc9-111">For example, you can configure your settings so that candidates receive emails from `recruiting@contoso.com` instead of `contoso@microsoft.com`.</span></span>
- <span data-ttu-id="96dc9-112">Erstellen Sie ein konsistentes Branding für Ihre gesamte E-Mail-Kommunikation indem Sie erst eine globale Kopf- und Fußzeile für alle E-Mail-Vorlagen festlegen.</span><span class="sxs-lookup"><span data-stu-id="96dc9-112">Create consistent branding for all your email communications by setting a global header and footer for email templates.</span></span> 

> [!NOTE]
> <span data-ttu-id="96dc9-113">Um Attract so zu konfigurieren, dass es das E-Mail-Service-Konto Ihres Unternehmens verwendet, um E-Mails zu senden, benötigen Sie das Einstellungs-Add-on „Comprehensive“.</span><span class="sxs-lookup"><span data-stu-id="96dc9-113">To configure Attract so that it uses your company's email service account to send email, you need the Comprehensive hiring add-on.</span></span>

## <a name="connect-an-email-service-account"></a><span data-ttu-id="96dc9-114">Anschließen eines E-Mail-Service-Kontos</span><span class="sxs-lookup"><span data-stu-id="96dc9-114">Connect an email service account</span></span>

<span data-ttu-id="96dc9-115">Indem Sie das E-Mail-Service-Konto Ihres Unternehmens verbinden, können Sie eine Branding-E-Mail-Erfahrung für die Job-Kandidaten erstellen.</span><span class="sxs-lookup"><span data-stu-id="96dc9-115">By connecting your company's email service account, you can create a branded email experience for your job candidates.</span></span> <span data-ttu-id="96dc9-116">Wenn Sie Ihr Unternehmenskonto nicht verbinden, verwendet Attract das Standard-Branding-E-Mail-Service-Konto von Microsoft.</span><span class="sxs-lookup"><span data-stu-id="96dc9-116">If you don't connect your company account, Attract uses the default Microsoft-branded email service account.</span></span>

1. <span data-ttu-id="96dc9-117">Wählen Sie **Einstellungen** (das Zahnrad-Symbol in der rechten oberen Ecke) aus, und wählen Sie dann **Administratorcenter**.</span><span class="sxs-lookup"><span data-stu-id="96dc9-117">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="96dc9-118">Wählen Sie auf der Registerkarte **E-Mail-Einstellungen** unter **E-Mail-Service-Konten** **Ein Unternehmenskonto verbinden** aus.</span><span class="sxs-lookup"><span data-stu-id="96dc9-118">On the **Email settings** tab, under **Email service accounts**, select **Connect a company account**.</span></span>

    ![Verbinden des E-Mail-Service-Kontos Ihres Unternehmens in Attract](./media/attract-admin-email-service-accounts.png)

    <span data-ttu-id="96dc9-120">Weitere Informationen dazu, wie Sie ein gemeinsames E-Mail-Konto erstellen, finden Sie unter [Gemeinsame Postfächer in Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).</span><span class="sxs-lookup"><span data-stu-id="96dc9-120">For more information about how to create a shared email account, see [Shared mailboxes in Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).</span></span>

3. <span data-ttu-id="96dc9-121">Melden Sie sich im Microsoft-Anmeldungsfenster mit Ihren Unternehmensanmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="96dc9-121">In the Microsoft sign-in window, sign in by using your corporate credentials.</span></span>
4. <span data-ttu-id="96dc9-122">Wenn Sie noch kein E-Mail-Service-Konto eingerichtet haben oder wenn Sie ein neues hinzufügen möchten, wählen Sie **Neues Dienstkonto hinzufügen** aus, und geben Sie dann Ihre E-Mail-Informationen ein.</span><span class="sxs-lookup"><span data-stu-id="96dc9-122">If you haven't yet set up an email service account, or if you want to add a new one, select **Add new service account**, and then enter your email information.</span></span> <span data-ttu-id="96dc9-123">Wenn Sie bereits ein E-Mail-Service-Konto eingerichtet haben, das Sie verwenden möchten, wählen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="96dc9-123">If you've already set up the email service account that you want to use, select it.</span></span>

<span data-ttu-id="96dc9-124">Wenn Ihr E-Mail-Service-Konto erfolgreiche konfiguriert ist, wird es unter **E-Mail-Service-Konten** aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="96dc9-124">When your email service account is successfully configured, you will see it listed under **Email service accounts**.</span></span>

## <a name="disconnect-an-email-service-account"></a><span data-ttu-id="96dc9-125">Trennen eines E-Mail-Service-Kontos</span><span class="sxs-lookup"><span data-stu-id="96dc9-125">Disconnect an email service account</span></span>

<span data-ttu-id="96dc9-126">Wenn Sie die Domäne Ihres Unternehmens nicht mehr in der E-Mail-Kommunikation durch Attract verwenden möchten, können Sie ein E-Mail-Service-Konto trennen.</span><span class="sxs-lookup"><span data-stu-id="96dc9-126">If you want to stop using your company's domain in email communications through Attract, you can disconnect an email service account.</span></span>

1. <span data-ttu-id="96dc9-127">Wählen Sie **Einstellungen** (das Zahnrad-Symbol in der rechten oberen Ecke) aus, und wählen Sie dann **Administratorcenter**.</span><span class="sxs-lookup"><span data-stu-id="96dc9-127">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="96dc9-128">Wählen Sie auf der Registerkarte **E-Mail-Einstellungen** unter **E-Mail-Service-Konten** die Schaltfläche **Weiter** (drei vertikale Punkte) neben dem E-Mail-Service-Konto aus, das Sie trennen möchten.</span><span class="sxs-lookup"><span data-stu-id="96dc9-128">On the **Email settings** tab, under **Email service accounts**, select the **More** button (three vertical dots) next to the email service account that you want to disconnect.</span></span>
3. <span data-ttu-id="96dc9-129">Wählen Sie **E-Mail-Konto trennen** aus.</span><span class="sxs-lookup"><span data-stu-id="96dc9-129">Select **Disconnect email account**.</span></span>

    ![Trennen des E-Mail-Service-Kontos Ihres Unternehmens](./media/attract-admin-disconnect-email-account.png)

4. <span data-ttu-id="96dc9-131">Wenn Sie aufgefordert werden, den Vorgang zu bestätigen, wählen Sie **Trennen** aus.</span><span class="sxs-lookup"><span data-stu-id="96dc9-131">When you're prompted to confirm the operation, select **Disconnect**.</span></span>

    ![Bestätigen der Trennung des E-Mail-Service-Kontos Ihres Unternehmens](./media/attract-admin-email-confirm-disconnect.png)

<span data-ttu-id="96dc9-133">Wenn Sie kein anderes E-Mail-Service-Konto verbinden, verwenden E-Mails, die von Attract gesendet werden, das Standard-Branding-E-Mail-Service-Konto von Microsoft.</span><span class="sxs-lookup"><span data-stu-id="96dc9-133">If you don't connect a different email service account, emails that are sent from Attract will use the default Microsoft-branded email service account.</span></span>

## <a name="configure-email-template-settings"></a><span data-ttu-id="96dc9-134">Konfigurieren von E-Mail-Vorlageeinstellungen</span><span class="sxs-lookup"><span data-stu-id="96dc9-134">Configure email template settings</span></span>

<span data-ttu-id="96dc9-135">Sie können ein Bild des Logos Ihres Unternehmens und andere Informationen als Branding-Kopfzeile für Ihre E-Mails hochladen.</span><span class="sxs-lookup"><span data-stu-id="96dc9-135">You can upload an image of your company's logo and other information as a branded header for your emails.</span></span> <span data-ttu-id="96dc9-136">Sie können auch Links zu Ihrer Datenschutzrichtlinie und den Nutzungsbedingungen in den E-Mail-Fußzeilen angeben.</span><span class="sxs-lookup"><span data-stu-id="96dc9-136">You can also provide links to your privacy policy and terms of use in email footers.</span></span>

> [!NOTE]
> <span data-ttu-id="96dc9-137">Sie müssen alle in Ihrem Land oder Ihrer Region geltenden Gesetze sowie die im Land des E-Mail-Empfängers geltenden erfüllen.</span><span class="sxs-lookup"><span data-stu-id="96dc9-137">You must comply with all applicable laws of your country or region, and also the country or region that governs the email recipient.</span></span> <span data-ttu-id="96dc9-138">Diese Gesetze beinhalten Antispambestimmungen.</span><span class="sxs-lookup"><span data-stu-id="96dc9-138">These laws include anti-spam regulations.</span></span>

1. <span data-ttu-id="96dc9-139">Wählen Sie **Einstellungen** (das Zahnrad-Symbol in der rechten oberen Ecke) aus, und wählen Sie dann **Administratorcenter**.</span><span class="sxs-lookup"><span data-stu-id="96dc9-139">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="96dc9-140">Auf der Registerkarte **E-Mail-Einstellungen** unter **Email-Vorlageneinstellungen** ziehen Sie das Bild, das Sie als Ihre E-Mail-Kopfzeile verwenden möchten in das Bildfeld, oder klicken Sie in das Bildfeld, um nach der Datei zu suchen.</span><span class="sxs-lookup"><span data-stu-id="96dc9-140">On the **Email settings** tab, under **Email template settings**, drag the image that you want to use as your email header into the image box, or click in the image box to browse for the file.</span></span> <span data-ttu-id="96dc9-141">Um ein vorhandenes Bild zu ersetzen, müssen Sie zunächst **Entfernen** daneben auswählen.</span><span class="sxs-lookup"><span data-stu-id="96dc9-141">To replace an existing image, you must first select **Remove** next to it.</span></span> <span data-ttu-id="96dc9-142">Das Bild muss eine JPEG-, JPG-, PNG- oder SVG-Datei sein.</span><span class="sxs-lookup"><span data-stu-id="96dc9-142">The image must be a JPEG, JPG, PNG, or SVG file.</span></span> <span data-ttu-id="96dc9-143">Die empfohlene Größe für Bilder liegt zwischen 25 und 800 Pixeln Breite und zwischen 25 und 150 Pixeln Höhe.</span><span class="sxs-lookup"><span data-stu-id="96dc9-143">The recommended size for images is between 25 and 800 pixels wide, and between 25 and 150 pixels high.</span></span> <span data-ttu-id="96dc9-144">Die maximale Dateigröße für die Kopfzeile ist 1 Megabyte (MB).</span><span class="sxs-lookup"><span data-stu-id="96dc9-144">The maximum file size for the header is 1 megabyte (MB).</span></span>

    ![Hinzufügen eines Bilds für die Kopfzeile der Unternehmens-E-Mail](./media/attract-admin-email-header.png)

3. <span data-ttu-id="96dc9-146">Geben Sie unter **Ihre Datenschutzrichtlinie für Kommunikation** einen Link zur Datenschutzrichtlinie des Unternehmens an.</span><span class="sxs-lookup"><span data-stu-id="96dc9-146">Under **Your Privacy policy for communications**, provide a link to your company's privacy policy.</span></span> <span data-ttu-id="96dc9-147">Geben Sie unter **Ihre Bedingungen für Kommunikation** einen Link zu den Nutzungsbedingungen Ihres Unternehmens an.</span><span class="sxs-lookup"><span data-stu-id="96dc9-147">Under **Your Terms and conditions for communication**, provide a link to your company's terms of use.</span></span>

    ![Hinzufügen von Links zur Datenschutzrichtlinie und den Nutzungsbedingungen des Unternehmens für die E-Mail-Fußzeile](./media/attract-admin-email-footer.png)

4. <span data-ttu-id="96dc9-149">Wählen Sie **Speichern** aus, um Ihre E-Mail-Vorlageneinstellungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="96dc9-149">Select **Save** to save your email template settings.</span></span>
