---
title: Angepasste Seiten für die Benutzeranmeldung einrichten
description: In diesem Thema wird beschrieben, wie Sie benutzerdefinierte Seiten in Microsoft Dynamics 365 Commerce erstellen, die benutzerdefinierte Anmeldungen für Benutzer von Business-to-Consumer (B2C)-Mandanten von Azure Active Directory (Azure AD) verarbeiten.
author: brianshook
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3328fad5328ae1954a6749f9a5eebcb71c723698
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477947"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a><span data-ttu-id="3c916-103">Angepasste Seiten für die Benutzeranmeldung einrichten</span><span class="sxs-lookup"><span data-stu-id="3c916-103">Set up custom pages for user sign-ins</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3c916-104">In diesem Thema wird beschrieben, wie Sie benutzerdefinierte Seiten in Microsoft Dynamics 365 Commerce erstellen, die benutzerdefinierte Anmeldungen für Benutzer von Business-to-Consumer (B2C)-Mandanten von Azure Active Directory (Azure AD) verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="3c916-104">This topic describes how to build custom pages in Microsoft Dynamics 365 Commerce that handle customized sign-ins for users of Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants.</span></span>

<span data-ttu-id="3c916-105">Um benutzerdefinierte Seiten zu verwenden, die in Dynamics 365 Commerce erstellt werden können, um Benutzeranmeldungsflüsse zu verarbeiten, müssen Sie die Azure AD Richtlinien festlegen, auf die in der Geschäftsumgebung verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="3c916-105">To use custom pages that are authored in Dynamics 365 Commerce to handle user sign-in flows, you must set up the Azure AD policies that will be referenced in the Commerce environment.</span></span> <span data-ttu-id="3c916-106">Sie können die Azure AD B2C Richtlinien „An- und Abmeldung“, „Profilverwaltung“ und „Kennwortzurücksetzung“ mithilfe der Azure AD B2C Anwendung konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="3c916-106">You can configure the "Sign up and sign in," "Profile editing," and "Password reset" Azure AD B2C policies by using the Azure AD B2C application.</span></span> <span data-ttu-id="3c916-107">Die Azure AD B2C Mandanten- und Richtliniennamen können dann während des Bereitstellungsprozesses referenziert werden, der für die Handelsumgebung mithilfe von Microsoft Dynamics Lifecycle Services (LCS) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3c916-107">The Azure AD B2C tenant and policy names can then be referenced during the provisioning process that is done for the Commerce environment by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="3c916-108">Die benutzerdefinierten Handelsseiten können erstellt werden, indem Anmeldung, Abmeldung, Kontoprofile bearbeiten oder Kennwortrücksetzungsmodul verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3c916-108">The custom Commerce pages can be built by using the sign in, sign up, account profile edit, or password reset module.</span></span> <span data-ttu-id="3c916-109">Die Seite URLs, die für die benutzerdefinierten Seiten veröffentlicht werden, sollten dann in Azure AD B2C Richtlinienkonfigurationen im Azureportal referenziert werden.</span><span class="sxs-lookup"><span data-stu-id="3c916-109">The page URLs that are published for these custom pages should then be referenced in Azure AD B2C policy configurations in the Azure portal.</span></span>

## <a name="set-up-b2c-policies"></a><span data-ttu-id="3c916-110">B2C Richtlinien einrichten</span><span class="sxs-lookup"><span data-stu-id="3c916-110">Set up B2C policies</span></span>

<span data-ttu-id="3c916-111">Nachdem Sie den Mandanten Azure AD B2C eingerichtet haben und diesen der Handelsumgebung zugeordnet haen, wechseln Sie zu **Azure AD B2C** im Azure Portal und anschließend wählen Sie **Richtlinien**, **Benutzerfluss (Richtlinien)**.</span><span class="sxs-lookup"><span data-stu-id="3c916-111">After you set up your Azure AD B2C tenant and associate it with your Commerce environment, go to the **Azure AD B2C** page in the Azure portal, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

![Benutzerfluss (Richtlinien) Befehl im Menü](./media/B2C_CustomPage_PoliciesMenu.png)

<span data-ttu-id="3c916-113">Sie können jetzt Registrieren und Anmelden, Profilbearbeitung und Kennwortrücksetzung im Fluss konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="3c916-113">You can now configure the "Sign up and sign in," "Profile editing," and "Password reset" user sign-in flows.</span></span>

### <a name="configure-the-sign-up-and-sign-in-policy"></a><span data-ttu-id="3c916-114">Konfigurieren von Registrieren und Anmelden in der Richtlinie</span><span class="sxs-lookup"><span data-stu-id="3c916-114">Configure the "Sign up and sign in" policy</span></span>

<span data-ttu-id="3c916-115">Um die Richtlinie Registrieren und Anmelden zu konfigurieren führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="3c916-115">To configure the "Sign up and sign in" policy, follow these steps.</span></span>

1. <span data-ttu-id="3c916-116">Wählen Sie **Neuer Benutzerfluss**, und dann, auf der Registerkarte **Empfohlen** wählen Sie die Richtlinie **Registrieren und Anmelden**.</span><span class="sxs-lookup"><span data-stu-id="3c916-116">Select **New user flow**, and then, on the **Recommended** tab, select the **Sign up and sign in** policy.</span></span>
1. <span data-ttu-id="3c916-117">Geben Sie einen Namen für die Richtlinie ein (z.B. **B2C \_1\_SignInSignUp**).</span><span class="sxs-lookup"><span data-stu-id="3c916-117">Enter a name for the policy (for example, **B2C\_1\_SignInSignUp**).</span></span>
1. <span data-ttu-id="3c916-118">Im Abschnitt **Identitätsanbieter** wählen Sie den Identitätsanbieter aus, den Sie für die Richtlinie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="3c916-118">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="3c916-119">Es muss mindestens **E-Mail-Registrierung** ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="3c916-119">At a minimum, **Email signup** must be selected.</span></span>
1. <span data-ttu-id="3c916-120">In der Spalte **Attribut sammeln** aktivieren Sie die Kontrollkästchen für **E-Mail-Adresse**, **Vorname** und **Nachname** aus.</span><span class="sxs-lookup"><span data-stu-id="3c916-120">In the **Collect attribute** column, select the check boxes for **Email Address**, **Given Name**, and **Surname**.</span></span>
1. <span data-ttu-id="3c916-121">In der Spalte **Rücknahme anfordern** aktivieren Sie die Kontrollkästchen für **E-Mail-Adressen**, **Vorname**, **Identitätsanbieter**, **Nachname** und **Objekt-ID des Benutzers**.</span><span class="sxs-lookup"><span data-stu-id="3c916-121">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>

    ![Attribute und Ansprüche ausgewählt](./media/B2C_SignInSignUp_Attributes.png)

1. <span data-ttu-id="3c916-123">**OK** wählen, um die Richtlinie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3c916-123">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="3c916-124">Doppelklicken Sie auf den neuen Richtliniennamen, und wählen dann im Navigationsbereich **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="3c916-124">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="3c916-125">Legen Sie **Aktivieren Sie JavaScript erzwingt Seitenlayout (Vorschau)** auf **Aktiviert** fest.</span><span class="sxs-lookup"><span data-stu-id="3c916-125">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

    ![Eigenschaftenseite für die neue Richtlinie](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> <span data-ttu-id="3c916-127">Der Richtlinienname verweist ganz auf die Handelsumgebung.</span><span class="sxs-lookup"><span data-stu-id="3c916-127">The policy name will be fully referenced in the Commerce environment.</span></span> <span data-ttu-id="3c916-128">(Das Präfix **B2C\_1\_** ist in der Referenz enthalten.) Richtlinien können nicht umbenannt werden, nachdem sie erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="3c916-128">(The **B2C\_1\_** prefix will be included in the reference.) Policies can't be renamed after they are created.</span></span> <span data-ttu-id="3c916-129">Wenn Sie eine vorhandene Richtlinie für die Handelsumgebung ersetzen, können Sie die ursprüngliche Richtlinie löschen und eine neue Richtlinie erstellen, die denselben Namen hat.</span><span class="sxs-lookup"><span data-stu-id="3c916-129">If you're replacing an existing policy for your Commerce environment, you can delete the original policy and build a new policy that has the same name.</span></span> <span data-ttu-id="3c916-130">Falls die Umgebung bereits bereitgestellt wurde, können Sie den neuen Richtliniennamen durch eine Serviceanforderung senden.</span><span class="sxs-lookup"><span data-stu-id="3c916-130">Alternatively, if the environment has already been provisioned, you can submit the new policy name through a service request.</span></span>

<span data-ttu-id="3c916-131">Sie kehren zu dieser Richtlinie zurück, um die Einrichtung zu beenden, nachdem Sie die benutzerdefinierten Seiten erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="3c916-131">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="3c916-132">Jetzt schließen Sie die Richtlinie, um zur Seite **Benutzerfluss (Richtlinien)** im Azure-Portal zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="3c916-132">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-profile-editing-policy"></a><span data-ttu-id="3c916-133">Konfigurieren Sie die Profilbearbeitungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3c916-133">Configure the "Profile editing" policy</span></span>

<span data-ttu-id="3c916-134">Um die Profilbearbeitungsrichtlinie zu konfigurieren, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="3c916-134">To configure the "Profile editing" policy, follow these steps.</span></span>

1. <span data-ttu-id="3c916-135">Wählen Sie **Neuer Benutzerfluss**, und dann auf der Registerkarte **Empfohlen** wählen Sie die Richtlinie **Profil bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="3c916-135">Select **New user flow**, and then, on the **Recommended** tab, select the **Profile editing** policy.</span></span>
1. <span data-ttu-id="3c916-136">Geben Sie einen Namen für die Richtlinie ein (z.B. **B2C\_1\_EditProfile**).</span><span class="sxs-lookup"><span data-stu-id="3c916-136">Enter a name for the policy (for example, **B2C\_1\_EditProfile**).</span></span>
1. <span data-ttu-id="3c916-137">Im Abschnitt **Identitätsanbieter** wählen Sie den Identitätsanbieter aus, den Sie für die Richtlinie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="3c916-137">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="3c916-138">Es muss mindestens **Lokale Kontoen-Anmeldung** ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="3c916-138">At a minimum, **Local Account SignIn** must be selected.</span></span>
1. <span data-ttu-id="3c916-139">In der Spalte **Attribut sammeln** aktivieren Sie die Kontrollkästchen für **E-Mail-Adresse** **Nachname** aus.</span><span class="sxs-lookup"><span data-stu-id="3c916-139">In the **Collect attribute** column, select the check boxes for **Email Addresses** and **Surname**.</span></span>
1. <span data-ttu-id="3c916-140">In der Spalte **Rücknahme anfordern** aktivieren Sie die Kontrollkästchen für **E-Mail-Adressen**, **Vorname**, **Identitätsanbieter**, **Nachname** und **Objekt-ID des Benutzers**.</span><span class="sxs-lookup"><span data-stu-id="3c916-140">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>
1. <span data-ttu-id="3c916-141">**OK** wählen, um die Richtlinie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3c916-141">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="3c916-142">Doppelklicken Sie auf den neuen Richtliniennamen, und wählen dann im Navigationsbereich **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="3c916-142">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="3c916-143">Legen Sie **Aktivieren Sie JavaScript erzwingt Seitenlayout (Vorschau)** auf **Aktiviert** fest.</span><span class="sxs-lookup"><span data-stu-id="3c916-143">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="3c916-144">Sie kehren zu dieser Richtlinie zurück, um die Einrichtung zu beenden, nachdem Sie die benutzerdefinierten Seiten erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="3c916-144">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="3c916-145">Jetzt schließen Sie die Richtlinie, um zur Seite **Benutzerfluss (Richtlinien)** im Azure-Portal zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="3c916-145">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-password-reset-policy"></a><span data-ttu-id="3c916-146">Konfigurieren Sie die Kennwortrücksetzungs „Richtlinie“</span><span class="sxs-lookup"><span data-stu-id="3c916-146">Configure the "Password reset" policy</span></span>

<span data-ttu-id="3c916-147">Um die Kennwortzurücksetzungsrichtlinie zu konfigurieren, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="3c916-147">To configure the "Password reset" policy, follow these steps.</span></span>

1. <span data-ttu-id="3c916-148">Wählen Sie **Neuer Benutzerfluss**, und dann auf der Registerkarte **Vorschau** wählen Sie die Richtlinie **Kennwor zurücksetzen v1.1**.</span><span class="sxs-lookup"><span data-stu-id="3c916-148">Select **New user flow**, and then, on the **Preview** tab, select the **Password reset v1.1** policy.</span></span>

    ![Richtlinie der Kennwortrücksetzung v1.1 ausgewählt auf der Vorschauregisterkarte](./media/B2C_ForgetPassword_Menu.png)

1. <span data-ttu-id="3c916-150">Geben Sie einen Namen für die Richtlinie ein (z.B. **B2C\_1\_ForgetPassword**).</span><span class="sxs-lookup"><span data-stu-id="3c916-150">Enter a name for the policy (for example, **B2C\_1\_ForgetPassword**).</span></span>
1. <span data-ttu-id="3c916-151">Im Abschnitt **Identitätsanbieter** wählen Sie **Rücksetzungskennwort mithilfe der E-Mail-Adresse** aus.</span><span class="sxs-lookup"><span data-stu-id="3c916-151">In the **Identity Providers** section, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="3c916-152">In der Spalte **Anforderung zurückgeben** aktivieren Sie die Kontrollkästchen für **E-Mail-Adressen**, **Vorname**, **Nachname** und **Objekt-ID des Benutzers**.</span><span class="sxs-lookup"><span data-stu-id="3c916-152">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Surname**, and **User's Object ID**.</span></span>

    ![Anforderung ausgewählt](./media/B2C_ForgetPassword_Attributes.png)

1. <span data-ttu-id="3c916-154">**OK** wählen, um die Richtlinie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3c916-154">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="3c916-155">Doppelklicken Sie auf den neuen Richtliniennamen, und wählen dann im Navigationsbereich **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="3c916-155">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="3c916-156">Legen Sie **Aktivieren Sie JavaScript erzwingt Seitenlayout (Vorschau)** auf **Aktiviert** fest.</span><span class="sxs-lookup"><span data-stu-id="3c916-156">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="3c916-157">Sie kehren zu dieser Richtlinie zurück, um die Einrichtung zu beenden, nachdem Sie die benutzerdefinierten Seiten erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="3c916-157">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="3c916-158">Jetzt schließen Sie die Richtlinie, um zur Seite **Benutzerfluss (Richtlinien)** im Azure-Portal zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="3c916-158">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

## <a name="build-the-custom-pages"></a><span data-ttu-id="3c916-159">Benutzerdefinierte Seiten erstellen</span><span class="sxs-lookup"><span data-stu-id="3c916-159">Build the custom pages</span></span>

<span data-ttu-id="3c916-160">Um benutzerdefinierte die Seiten zu erstellen, um Benutzer-Registrierungen zu behandeln, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="3c916-160">To build the custom pages to handle user sign-ins, follow these steps.</span></span>

1. <span data-ttu-id="3c916-161">Im Handels-Erstellungstool gehen Sie zu Ihrer Site.</span><span class="sxs-lookup"><span data-stu-id="3c916-161">In the Commerce authoring tools, go to your site.</span></span>
1. <span data-ttu-id="3c916-162">Erstellen Sie die folgenden fünf Vorlagen und fünf Seiten:</span><span class="sxs-lookup"><span data-stu-id="3c916-162">Build the following five templates and five pages:</span></span>

    - <span data-ttu-id="3c916-163">Eine Vorlage **Anmelden** und eine Seite die das Anmeldungsmodul verwendet.</span><span class="sxs-lookup"><span data-stu-id="3c916-163">A **Sign In** template and page that use the sign in module.</span></span>
    - <span data-ttu-id="3c916-164">Eine Vorlage **Abmelden** und eine Seite die das Abmeldungsmodul verwendet.</span><span class="sxs-lookup"><span data-stu-id="3c916-164">A **Sign Up** template and page that use the sign up module.</span></span>
    - <span data-ttu-id="3c916-165">Eine Vorlage **Kennwort zurücksetzen** und Seite, die das Kennwortrücksetzungsmodul verwenden.</span><span class="sxs-lookup"><span data-stu-id="3c916-165">A **Password Reset** template and page that use the password reset module.</span></span>
    - <span data-ttu-id="3c916-166">Eine Vorlage **Kennwort zurücksetzen prüfen** und Seite, die das Kennwortrücksetzungsmodul überprüft.</span><span class="sxs-lookup"><span data-stu-id="3c916-166">A **Password Reset verification** template and page that use the password reset verification module.</span></span>
    - <span data-ttu-id="3c916-167">Eine Vorlage **Profil bearbeiten** und Seite, die das Kundenprofil verwenden Modul bearbeiten</span><span class="sxs-lookup"><span data-stu-id="3c916-167">A **Profile Edit** template and page that use the account profile edit module</span></span>

<span data-ttu-id="3c916-168">Wenn Sie die Seiten erstellen, folgen Sie diesen Richtlinien:</span><span class="sxs-lookup"><span data-stu-id="3c916-168">When you build the pages, follow these guidelines:</span></span>

- <span data-ttu-id="3c916-169">Für jede Seite oder Modul verwenden Sie das Layout und den Stil, die am besten Ihren Geschäftsanforderungen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3c916-169">For each page or module, use the layout and style that best suit your business requirements.</span></span>
- <span data-ttu-id="3c916-170">Veröffentlichen Sie alle Seiten und URLs, die in der Azure AD B2C Einstellung verwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="3c916-170">Publish all pages and URLs that must be used in the Azure AD B2C setup.</span></span>
- <span data-ttu-id="3c916-171">Nachdem die Seiten und URLs veröffentlicht wurden, sammeln Sie die URLs, die für die Azure AD B2C Richtlinienkonfiguration verwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="3c916-171">After the pages and URLs are published, collect the URLs that must be used for the Azure AD B2C policy configurations.</span></span> <span data-ttu-id="3c916-172">Ein **?preloadscripts=true** Suffix wird jeder URL hinzugefügt, wenn sie verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3c916-172">A **?preloadscripts=true** suffix will be added to every URL when it's used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3c916-173">Verwenden Sie die allgemeine Kopf- und Fußzeilen nicht erneut, die relative Verknüpfungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="3c916-173">Don't reuse universal headers and footers that have relative links.</span></span> <span data-ttu-id="3c916-174">Da diese Seiten in der Azure AD B2C Domäne gehostet werden, wenn sie nicht verwendet werden, sollten nur absolute URLs für alle Links verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3c916-174">Because these pages will be hosted in the Azure AD B2C domain when they are used, only absolute URLs should be used for all links.</span></span>

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a><span data-ttu-id="3c916-175">Konfigurieren von Azure AD B2C Richtlinien mit benutzerdefinierten Seiteninformationen</span><span class="sxs-lookup"><span data-stu-id="3c916-175">Configure Azure AD B2C policies with custom page information</span></span> 

<span data-ttu-id="3c916-176">Im Azure Portal kehren Sie zur Seite **Azure AD B2C** zurück und anschließend auf dem Menü unter **Richtlinien** wählen Sie **Benutzerfluss (Richtlinien)**.</span><span class="sxs-lookup"><span data-stu-id="3c916-176">In the Azure portal, return to the **Azure AD B2C** page, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a><span data-ttu-id="3c916-177">Aktualisieren Sie die Richtlinie „registrieren und anmelden“ mit benutzerdefinierten Seiteninformationen</span><span class="sxs-lookup"><span data-stu-id="3c916-177">Update the "Sign up and sign in" policy with custom page information</span></span>

<span data-ttu-id="3c916-178">Um die Richtlinie „registrieren und anmelden“ mit benutzerdefinierten Seiteninformationen zu aktualisieren, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="3c916-178">To update the "Sign up and sign in" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="3c916-179">In der Richtlinie **Anmelden und abmelden** die Sie eben im Navigationsbereich konfiguriert haben, wählen Sie **Seitenlayouts** aus.</span><span class="sxs-lookup"><span data-stu-id="3c916-179">In the **Sign in and sign up** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="3c916-180">Wählen Sie das Layout **Einheitliche An- und Abmeldung auf der Seite** aus.</span><span class="sxs-lookup"><span data-stu-id="3c916-180">Select the **Unified sign up or sign in page** layout.</span></span>
1. <span data-ttu-id="3c916-181">Hier können Sie die Option **Benutzerdefinierten Seiteninhalt verwwenden** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="3c916-181">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="3c916-182">Im Feld **Benutzerdefinierte Seiten-URLe** geben Sie die vollständige Anmeldungs-URL ein.</span><span class="sxs-lookup"><span data-stu-id="3c916-182">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="3c916-183">Schließt das Suffix **? preloadscripts=true** ein.</span><span class="sxs-lookup"><span data-stu-id="3c916-183">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="3c916-184">Geben Sie beispielsweise ``www.<my domain>.com/sign-in?preloadscripts=true`` ein.</span><span class="sxs-lookup"><span data-stu-id="3c916-184">For example, enter ``www.<my domain>.com/sign-in?preloadscripts=true``.</span></span>
1. <span data-ttu-id="3c916-185">Im Feld **Seitenlayoutversion (Vorschau)** wählen Sie **1.2.0** aus.</span><span class="sxs-lookup"><span data-stu-id="3c916-185">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="3c916-186">Wählen Sie das Layout **Lokale Kontoanmeldeseite** aus.</span><span class="sxs-lookup"><span data-stu-id="3c916-186">Select the **Local account sign up page** layout.</span></span>
1. <span data-ttu-id="3c916-187">Hier können Sie die Option **Benutzerdefinierten Seiteninhalt verwwenden** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="3c916-187">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="3c916-188">Im Feld **Benutzerdefinierte Seiten-URI** geben Sie die vollständige Anmeldungs-URL ein.</span><span class="sxs-lookup"><span data-stu-id="3c916-188">In the **Custom page URI** field, enter the full sign-up URL.</span></span> <span data-ttu-id="3c916-189">Schließt das Suffix **? preloadscripts=true** ein.</span><span class="sxs-lookup"><span data-stu-id="3c916-189">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="3c916-190">Geben Sie beispielsweise ``www.<my domain>.com/sign-up?preloadscripts=true`` ein.</span><span class="sxs-lookup"><span data-stu-id="3c916-190">For example, enter ``www.<my domain>.com/sign-up?preloadscripts=true``.</span></span>
1. <span data-ttu-id="3c916-191">Im Feld **Seitenlayoutversion (Vorschau)** wählen Sie **1.2.0** aus.</span><span class="sxs-lookup"><span data-stu-id="3c916-191">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="3c916-192">Im Abschnitt **Benutzerattribute** folgen Sie diesen Schritten:</span><span class="sxs-lookup"><span data-stu-id="3c916-192">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="3c916-193">Für die Attribute **E-Mail-Adresse** **Vorname** und **Nachname** wählen Sie  **Nein** im Feld **Erfordert Prüfung** aus.</span><span class="sxs-lookup"><span data-stu-id="3c916-193">For the **Email Address**, **Given Name**, and **Surname** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="3c916-194">Für die Attribute **Vorname** und **Nachname** wählen Sie **Nein** im Feld **Optional** aus.</span><span class="sxs-lookup"><span data-stu-id="3c916-194">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

    ![Konfiguration des lokalen Kontos sich als Neukunde Seitenrichtlinie an](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a><span data-ttu-id="3c916-196">Aktualisieren Sie die Richtlinie „Profil bearbeiten“ mit den benutzerdefinierten Seiteninformationen</span><span class="sxs-lookup"><span data-stu-id="3c916-196">Update the "Profile editing" policy with custom page information</span></span>

<span data-ttu-id="3c916-197">Um die Richtlinie „Profil bearbeiten“ mit benutzerdefinierten Seiteninformationen zu aktualisieren, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="3c916-197">To update the "Profile editing" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="3c916-198">In der Richtlinie **Profil bearbeiten** die Sie eben im Navigationsbereich konfiguriert haben, wählen Sie **Seitenlayouts** aus.</span><span class="sxs-lookup"><span data-stu-id="3c916-198">In the **Profile Editing** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="3c916-199">Wählen Sie das Layout **Profilbearbeitungsseite** aus.</span><span class="sxs-lookup"><span data-stu-id="3c916-199">Select the **Profile edit page** layout.</span></span>
1. <span data-ttu-id="3c916-200">Hier können Sie die Option **Benutzerdefinierten Seiteninhalt verwwenden** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="3c916-200">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="3c916-201">Im Feld **Benutzerdefinierte Seiten-URI** geben Sie die vollständige Profilbearbeitungs-URL ein.</span><span class="sxs-lookup"><span data-stu-id="3c916-201">In the **Custom page URI** field, enter the full profile edit URL.</span></span> <span data-ttu-id="3c916-202">Schließt das Suffix **? preloadscripts=true** ein.</span><span class="sxs-lookup"><span data-stu-id="3c916-202">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="3c916-203">Geben Sie beispielsweise ``www.<my domain>.com/profile-edit?preloadscripts=true`` ein.</span><span class="sxs-lookup"><span data-stu-id="3c916-203">For example, enter ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span></span>
1. <span data-ttu-id="3c916-204">Im Feld **Seitenlayoutversion (Vorschau)** wählen Sie **1.2.0** aus.</span><span class="sxs-lookup"><span data-stu-id="3c916-204">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="3c916-205">Im Abschnitt **Benutzerattribute** folgen Sie diesen Schritten:</span><span class="sxs-lookup"><span data-stu-id="3c916-205">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="3c916-206">Für die Attribute **E-Mail-Adresse**, **Vorname** wählen Sie **Nein** aus im Feld **Erfordert Prüfung**.</span><span class="sxs-lookup"><span data-stu-id="3c916-206">For the **Email Address**, **Given Name** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="3c916-207">Für die Attribute **Vorname** und **Nachname** wählen Sie **Nein** im Feld **Optional** aus.</span><span class="sxs-lookup"><span data-stu-id="3c916-207">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

### <a name="update-the-password-reset-policy-with-custom-page-information"></a><span data-ttu-id="3c916-208">Aktualisieren Sie die Richtlinie „Kennwort zurücksetzen“ mit den benutzerdefinierten Informationen</span><span class="sxs-lookup"><span data-stu-id="3c916-208">Update the "Password reset" policy with custom page information</span></span>

<span data-ttu-id="3c916-209">Um die Richtlinie „Kennwort zurücksetzen“ mit benutzerdefinierten Seiteninformationen zu aktualisieren, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="3c916-209">To update the "Password reset" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="3c916-210">In der Richtlinie **Kennwort zurücksetzen** die Sie eben im Navigationsbereich konfiguriert haben, wählen Sie **Seitenlayouts** aus.</span><span class="sxs-lookup"><span data-stu-id="3c916-210">In the **Password Reset** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="3c916-211">Wählen Sie das Layout **Neue Kennwortseite** aus.</span><span class="sxs-lookup"><span data-stu-id="3c916-211">Select the **New password page** layout.</span></span>
1. <span data-ttu-id="3c916-212">Hier können Sie die Option **Benutzerdefinierten Seiteninhalt verwwenden** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="3c916-212">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="3c916-213">Im Feld **Benutzerdefinierte Seiten-URI** geben Sie die vollständige URL zum Zurücksetzen von Passwörtern ein.</span><span class="sxs-lookup"><span data-stu-id="3c916-213">In the **Custom page URI** field, enter the full password reset URL.</span></span> <span data-ttu-id="3c916-214">Schließt das Suffix **? preloadscripts=true** ein.</span><span class="sxs-lookup"><span data-stu-id="3c916-214">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="3c916-215">Geben Sie beispielsweise ``www.<my domain>.com/passwordreset?preloadscripts=true`` ein.</span><span class="sxs-lookup"><span data-stu-id="3c916-215">For example, enter ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span></span>
1. <span data-ttu-id="3c916-216">Im Feld **Seitenlayoutversion (Vorschau)** wählen Sie **1.2.0** aus.</span><span class="sxs-lookup"><span data-stu-id="3c916-216">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="3c916-217">Wählen Sie das Layout **Kontoenprüfungsseite** aus.</span><span class="sxs-lookup"><span data-stu-id="3c916-217">Select the **Account verification page** layout.</span></span>
1. <span data-ttu-id="3c916-218">Hier können Sie die Option **Benutzerdefinierten Seiteninhalt verwwenden** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="3c916-218">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="3c916-219">Im Feld **Benutzerdefinierte Seiten-URI** geben Sie die vollständige Überprüfungs-URL ein.</span><span class="sxs-lookup"><span data-stu-id="3c916-219">In the **Custom page URI** field, enter the full password reset verification URL.</span></span> <span data-ttu-id="3c916-220">Schließt das Suffix **? preloadscripts=true** ein.</span><span class="sxs-lookup"><span data-stu-id="3c916-220">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="3c916-221">Geben Sie beispielsweise ``www.<my domain>.com/passwordreset-verification?preloadscripts=true`` ein.</span><span class="sxs-lookup"><span data-stu-id="3c916-221">For example, enter ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span></span>
1. <span data-ttu-id="3c916-222">Im Feld **Seitenlayoutversion (Vorschau)** wählen Sie **1.2.0** aus.</span><span class="sxs-lookup"><span data-stu-id="3c916-222">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a><span data-ttu-id="3c916-223">Passen Sie Standardtextzeichenfolgen für Beschriftungen und Beschreibungen an</span><span class="sxs-lookup"><span data-stu-id="3c916-223">Customize default text strings for labels and descriptions</span></span>

<span data-ttu-id="3c916-224">In der Modulbibliothek sind die Anmeldungsmodule mit Standardtextzeichenfolgen für Beschriftungen und Beschreibungen vorausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="3c916-224">In the module library, sign-in modules are prefilled with default text strings for the labels and descriptions.</span></span> <span data-ttu-id="3c916-225">Sie können diese Zeichenfolgen in Software Development Kit (SDK) anpassen, indem Sie die Werte in der global.json-Datei für das Zeichen im Modul aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3c916-225">You can customize these strings in the software development kit (SDK) by updating the values in the global.json file for the sign in module.</span></span>

<span data-ttu-id="3c916-226">Beispielsweise ist der Standardtext für den Link Kennwort vergessenen **Vergessenes Kennwort?**.</span><span class="sxs-lookup"><span data-stu-id="3c916-226">For example, the default text for the forgotten password link is **Forgotten password?**.</span></span> <span data-ttu-id="3c916-227">Nachfolgend wird der Standardtext auf der Anmeldeseite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3c916-227">The following shows this default text on the sign-in page.</span></span>

![Der Standardtext für den Link Kennwort vergessenen auf der Anmeldeseite](./media/B2C_SignUp_ModuleFace.png)

<span data-ttu-id="3c916-229">Sie könnnen jedoch in der Datei global.json für das Anmeldungsmodul in der Modulbibliothek den Text zu **Kennwort vergessen?** ändern, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3c916-229">However, in the global.json file for the module library sign-in module, you can edit the text to **Forgot Password?**, as shown in the following illustration.</span></span>

![Aktualisierter Hyperlinktext im Anmeldungsmodul global.json-Datei](./media/B2C_CustomizingStringsForModule.png)

<span data-ttu-id="3c916-231">Nachdem Sie die Datei global.json aktualisiert und die Änderungen veröffentlicht haben, wird der neue Hyperlinktext im Anmeldungsmodul in Commerce und auf der Liveanmeldeseite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3c916-231">After you update the global.json file and publish your changes, the new link text appears in the sign-in module in both Commerce and on the live sign-in page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3c916-232">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3c916-232">Additional resources</span></span>

[<span data-ttu-id="3c916-233">Domänennamen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="3c916-233">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="3c916-234">Neuen E-Commerce-Mandanten bereitstellen</span><span class="sxs-lookup"><span data-stu-id="3c916-234">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="3c916-235">E-Commerce-Website erstellen</span><span class="sxs-lookup"><span data-stu-id="3c916-235">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="3c916-236">Zuordnen einer Dynamics 365 Commerce-Website zu einem Onlinekanal</span><span class="sxs-lookup"><span data-stu-id="3c916-236">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="3c916-237">Robots.txt-Dateien verwalten</span><span class="sxs-lookup"><span data-stu-id="3c916-237">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="3c916-238">URL-Umleitungen in Massen hochladen</span><span class="sxs-lookup"><span data-stu-id="3c916-238">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="3c916-239">Einrichten eines B2C-Mandanten in Commerce</span><span class="sxs-lookup"><span data-stu-id="3c916-239">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="3c916-240">Konfigurieren Sie mehrere B2C-Mandanten in einer Commerce-Umgebung</span><span class="sxs-lookup"><span data-stu-id="3c916-240">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="3c916-241">Hinzufügen von Unterstützung für ein Content Delivery Network (CDN)</span><span class="sxs-lookup"><span data-stu-id="3c916-241">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="3c916-242">Standortbasierte Shop-Erkennung aktivieren</span><span class="sxs-lookup"><span data-stu-id="3c916-242">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
