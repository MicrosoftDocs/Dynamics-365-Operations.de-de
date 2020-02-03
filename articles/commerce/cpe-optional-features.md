---
title: Konfigurieren optionaler Funktionen für eine Commerce-Vorschauumgebung
description: In diesem Thema wird erläutert, wie optionale Funktionen für eine Microsoft Dynamics 365 Commerce-Vorschauumgebung konfiguriert wird.
author: psimolin
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2c4872cdebc414eaa865af025237bd9e1d14bfd2
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906115"
---
# <a name="configure-optional-features-for-a-commerce-preview-environment"></a><span data-ttu-id="7afc4-103">Konfigurieren optionaler Funktionen für eine Commerce-Vorschauumgebung</span><span class="sxs-lookup"><span data-stu-id="7afc4-103">Configure optional features for a Commerce preview environment</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="7afc4-104">In diesem Thema wird erläutert, wie optionale Funktionen für eine Microsoft Dynamics 365 Commerce-Vorschauumgebung konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="7afc4-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7afc4-105">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="7afc4-105">Prerequisites</span></span>

<span data-ttu-id="7afc4-106">Wenn Sie die Transaktions-E-Mail-Funktionen bewerten möchten, müssen die folgenden Voraussetzungen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="7afc4-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="7afc4-107">Ihnen steht ein E-Mail-Server (Simple Mail Transfer Protocol \[SMTP\]-Server) zur Verfügung, der über das Microsoft Azure-Abonnement verwendet werden kann, auf dem Sie die Vorschauumgebung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7afc4-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the preview environment.</span></span>
- <span data-ttu-id="7afc4-108">Sie verfügen über den vollqualifizierten Domänennamen (FQDN)/die vollqualifizierte IP-Adresse, die SMTP-Portnummer und die Authentifizierungsdetails des Servers.</span><span class="sxs-lookup"><span data-stu-id="7afc4-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

<span data-ttu-id="7afc4-109">Wenn Sie die Funktionen der digitalen Anlagenverwaltung durch die Aufnahme neuer Mehrkanal-Images bewerten möchten, muss Ihnen der Name Ihres CMS-Mandanten (Content Management System) zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="7afc4-109">If you want to evaluate Digital Asset Management features by ingesting new omni-channel images, you must have the name of your content management system (CMS) tenant available.</span></span> <span data-ttu-id="7afc4-110">Anweisungen zum Auffinden dieses Namens finden Sie weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="7afc4-110">Instructions for finding this name are provided later in this topic.</span></span> <span data-ttu-id="7afc4-111">>>> (F: Wo sind die Anweisungen?)</span><span class="sxs-lookup"><span data-stu-id="7afc4-111">>>>(Q: where are the instructions?)</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="7afc4-112">Konfigurieren Sie das Image-Backend</span><span class="sxs-lookup"><span data-stu-id="7afc4-112">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="7afc4-113">Auffinden Ihrer medienbasierten URL</span><span class="sxs-lookup"><span data-stu-id="7afc4-113">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="7afc4-114">Bevor Sie diesen Vorgang abschließen können, müssen Sie die Schritte in [Richten Sie Ihre Site in Commerce ein](cpe-post-provisioning.md#set-up-your-site-in-commerce) abschließen.</span><span class="sxs-lookup"><span data-stu-id="7afc4-114">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="7afc4-115">Melden Sie sich beim Commerce-Site-Management-Tool mit der URL an, die Sie bei der Initialisierung von E-Commerce während der Bereitstellung notiert haben (siehe [E-Commerce initialisieren](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="7afc4-115">Sign in to the Commerce site management tool by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="7afc4-116">Öffnen Sie die Site **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="7afc4-116">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="7afc4-117">Wählen Sie im linken Menü **Assets** aus.</span><span class="sxs-lookup"><span data-stu-id="7afc4-117">On the menu on the left, select **Assets**.</span></span>
1. <span data-ttu-id="7afc4-118">Wählen Sie ein einzelnes Image-Medienobjekt aus.</span><span class="sxs-lookup"><span data-stu-id="7afc4-118">Select any single image asset.</span></span>
1. <span data-ttu-id="7afc4-119">Suchen Sie im Eigenschafteninspektor rechts die Eigenschaft **Öffentliche URL**.</span><span class="sxs-lookup"><span data-stu-id="7afc4-119">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="7afc4-120">Der Wert ist eine URL.</span><span class="sxs-lookup"><span data-stu-id="7afc4-120">The value is a URL.</span></span> <span data-ttu-id="7afc4-121">Hier ist ein Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7afc4-121">Here is an example:</span></span>

    <span data-ttu-id="7afc4-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span><span class="sxs-lookup"><span data-stu-id="7afc4-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="7afc4-123">Ersetzen Sie den letzten Bezeichner in der URL (**MA1nQC** im vorherigen Beispiel) durch die Zeichenfolge **search?fileName=**.</span><span class="sxs-lookup"><span data-stu-id="7afc4-123">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="7afc4-124">So sieht die Beispiel-URL nach dieser Änderung aus:</span><span class="sxs-lookup"><span data-stu-id="7afc4-124">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="7afc4-125">Diese URL ist Ihre Mediendatenbank-URL.</span><span class="sxs-lookup"><span data-stu-id="7afc4-125">This URL is your media base URL.</span></span> <span data-ttu-id="7afc4-126">Machen Sie sich eine Notiz davon.</span><span class="sxs-lookup"><span data-stu-id="7afc4-126">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="7afc4-127">Aktualisieren der medienbasierten URL</span><span class="sxs-lookup"><span data-stu-id="7afc4-127">Update the media base URL</span></span>

1. <span data-ttu-id="7afc4-128">Melden Sie sich bei Dynamics 365 Retail an.</span><span class="sxs-lookup"><span data-stu-id="7afc4-128">Sign in to Dynamics 365 Retail.</span></span>
1. <span data-ttu-id="7afc4-129">Navigieren Sie über das Menü links zu **Modulee \> Retail \> Kanaleinstellungen \> Kanalprofile**.</span><span class="sxs-lookup"><span data-stu-id="7afc4-129">Use the menu on the left to go to **Modules \> Retail \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="7afc4-130">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="7afc4-130">Select **Edit**.</span></span>
1. <span data-ttu-id="7afc4-131">Ersetzen Sie unter **Profileigenschaften** den Wert für die Eigenschaft **Media Server-Basis-URL** durch die medienbasierte URL, die Sie zuvor erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="7afc4-131">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="7afc4-132">Wählen Sie in der Liste links unter dem Kanal **Standard** den anderen Kanal aus.</span><span class="sxs-lookup"><span data-stu-id="7afc4-132">In the list on the left, under the **Default** channel, select the other channel.</span></span>
1. <span data-ttu-id="7afc4-133">Wählen Sie unter **Profileigenschaften** die Option **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="7afc4-133">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="7afc4-134">Wählen Sie für die hinzugefügte Eigenschaft **Media Server-Basis-URL** als Eigenschaftsschlüssel aus.</span><span class="sxs-lookup"><span data-stu-id="7afc4-134">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="7afc4-135">Geben Sie als Eigenschaftswert die zuvor erstellte Media Base-URL ein.</span><span class="sxs-lookup"><span data-stu-id="7afc4-135">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="7afc4-136">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="7afc4-136">Select **Save**.</span></span>

## <a name="configure-the-email-server"></a><span data-ttu-id="7afc4-137">Konfigurieren des E-Mail-Servers</span><span class="sxs-lookup"><span data-stu-id="7afc4-137">Configure the email server</span></span>

> [!NOTE]
> <span data-ttu-id="7afc4-138">Der SMTP-Server oder E-Mail-Dienst, den Sie hier eingeben, muss über das Azure-Abonnement zugänglich sein muss, das Sie für die Umgebung verwenden.</span><span class="sxs-lookup"><span data-stu-id="7afc4-138">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="7afc4-139">Melden Sie sich bei Retail an.</span><span class="sxs-lookup"><span data-stu-id="7afc4-139">Sign in to Retail.</span></span>
1. <span data-ttu-id="7afc4-140">Navigieren Sie über das Menü links zu **Module \> Systemverwaltung \> Einstellungen \> E-Mail \> E-Mail-Parameter**.</span><span class="sxs-lookup"><span data-stu-id="7afc4-140">Use the menu on the left to go to **Modules \> System administration \> Setup \> Email \> Email parameters**.</span></span>
1. <span data-ttu-id="7afc4-141">Geben Sie auf der Registerkarte **SMTP-Einstellungen** im Feld **Name des SMTP-Servers** den vollständig qualifizierten Namen (FQDN) oder die IP-Adresse Ihres SMTP-Servers oder E-Mail-Dienstes an.</span><span class="sxs-lookup"><span data-stu-id="7afc4-141">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="7afc4-142">Geben Sie im Feld **SMTP-Portnummer** die Portnummer ein.</span><span class="sxs-lookup"><span data-stu-id="7afc4-142">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="7afc4-143">(Wenn Sie Secure Sockets Layer \[SSL\] nicht verwenden, lautet die Standardportnummer **25**.)</span><span class="sxs-lookup"><span data-stu-id="7afc4-143">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="7afc4-144">Wenn eine Authentifizierung erforderlich ist, geben Sie Werte in das Feld **Benutzername** und **Kennwort** ein.</span><span class="sxs-lookup"><span data-stu-id="7afc4-144">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="7afc4-145">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="7afc4-145">Select **Save**.</span></span>
1. <span data-ttu-id="7afc4-146">Wählen Sie **Aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="7afc4-146">Select **Refresh**.</span></span>
1. <span data-ttu-id="7afc4-147">Wählen Sie auf der Registerkarte **Test-E-mail** im Feld **E-Mail-Anbieter** die Option **SMTP** aus.</span><span class="sxs-lookup"><span data-stu-id="7afc4-147">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="7afc4-148">Geben Sie im Feld **Senden an** die E-Mail-Adresse ein, an die die Test-E-Mail gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7afc4-148">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="7afc4-149">Wählen Sie **Test-E-Mail senden** aus.</span><span class="sxs-lookup"><span data-stu-id="7afc4-149">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="7afc4-150">Konfigurieren der E-Mail-Vorlagen</span><span class="sxs-lookup"><span data-stu-id="7afc4-150">Configure email templates</span></span>

<span data-ttu-id="7afc4-151">Für jedes Transaktionsereignis, für das Sie E-Mails senden möchten, müssen Sie die E-Mail-Vorlage mit einer gültigen Absender-E-Mail-Adresse aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="7afc4-151">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="7afc4-152">Melden Sie sich bei Retail an.</span><span class="sxs-lookup"><span data-stu-id="7afc4-152">Sign in to Retail.</span></span>
1. <span data-ttu-id="7afc4-153">Navigieren Sie über das Menü links zu **Module \> Organizationsverwaltung \> Einstellungen \> Organisations-E-Mail-Vorlagen**.</span><span class="sxs-lookup"><span data-stu-id="7afc4-153">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="7afc4-154">Wählen Sie **Liste anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="7afc4-154">Select **Show list**.</span></span>
1. <span data-ttu-id="7afc4-155">Führen Sie für jede Vorlage in der Liste die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="7afc4-155">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="7afc4-156">Geben Sie im Feld **E-Mail des Absenders** die E-Mail-Adresse des Absenders ein.</span><span class="sxs-lookup"><span data-stu-id="7afc4-156">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="7afc4-157">Optional: Geben Sie im Feld **Absendername** den Namen ein, der als Absendername verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7afc4-157">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="7afc4-158">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="7afc4-158">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="7afc4-159">E-Mail-Vorlagen anpassen</span><span class="sxs-lookup"><span data-stu-id="7afc4-159">Customize email templates</span></span>

<span data-ttu-id="7afc4-160">Möglicherweise möchten Sie die E-Mail-Vorlagen so anpassen, dass sie unterschiedliche Bilder verwenden.</span><span class="sxs-lookup"><span data-stu-id="7afc4-160">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="7afc4-161">Oder Sie möchten die Links in den Vorlagen aktualisieren, damit sie in Ihre Vorschauumgebung gelangen.</span><span class="sxs-lookup"><span data-stu-id="7afc4-161">Or you might want to update the links in the templates so that they go to your preview environment.</span></span> <span data-ttu-id="7afc4-162">In dieser Prozedur wird erläutert, wie Sie die Standardvorlagen herunterladen, anpassen und die Vorlagen im System aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="7afc4-162">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="7afc4-163">Laden Sie über einen Webbrowser [die Datei Microsoft Dynamics 365 Commerce-Vorschau-Standard-E-Mail-Vorlagen.zip](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) auf Ihren lokalen Computer herunter.</span><span class="sxs-lookup"><span data-stu-id="7afc4-163">In a web browser, download the [Microsoft Dynamics 365 Commerce Preview default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="7afc4-164">Diese Datei enthält die folgenden HTML-Dokumente:</span><span class="sxs-lookup"><span data-stu-id="7afc4-164">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="7afc4-165">Auftragsbestätigungsvorlage</span><span class="sxs-lookup"><span data-stu-id="7afc4-165">Order confirmation template</span></span>
    - <span data-ttu-id="7afc4-166">Geschenkkartenvorlage ausstellen</span><span class="sxs-lookup"><span data-stu-id="7afc4-166">Issue gift card template</span></span>
    - <span data-ttu-id="7afc4-167">Neue Auftragsvorlage</span><span class="sxs-lookup"><span data-stu-id="7afc4-167">New order template</span></span>
    - <span data-ttu-id="7afc4-168">Verpackungsvorlage</span><span class="sxs-lookup"><span data-stu-id="7afc4-168">Pack order template</span></span>
    - <span data-ttu-id="7afc4-169">Entnahmevorlage</span><span class="sxs-lookup"><span data-stu-id="7afc4-169">Pick order template</span></span>

1. <span data-ttu-id="7afc4-170">Passen Sie die Vorlagen mit einem Text- oder HTML-Editor an.</span><span class="sxs-lookup"><span data-stu-id="7afc4-170">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="7afc4-171">Schauen Sie sich die Lister der [unterstützten Token](#supported-tokens-in-the-email-template) später in diesem Thema an.</span><span class="sxs-lookup"><span data-stu-id="7afc4-171">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="7afc4-172">Melden Sie sich bei Retail an.</span><span class="sxs-lookup"><span data-stu-id="7afc4-172">Sign in to Retail.</span></span>
1. <span data-ttu-id="7afc4-173">Navigieren Sie über das Menü links zu **Module \> Organizationsverwaltung \> Einstellungen \> Organisations-E-Mail-Vorlagen**.</span><span class="sxs-lookup"><span data-stu-id="7afc4-173">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="7afc4-174">Erweitern Sie die Liste auf der linken Seite, um alle Vorlagen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7afc4-174">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="7afc4-175">Gehen Sie für jede Vorlage, die Sie anpassen möchten, folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="7afc4-175">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="7afc4-176">Wählen Sie die Vorlage in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="7afc4-176">Select the template in the list.</span></span>
    1. <span data-ttu-id="7afc4-177">Wählen Sie unter **Inhalt der E-Mail-Nachricht** die entsprechende Sprachversion in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="7afc4-177">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="7afc4-178">(Die Standardsprache lautet **en-us**.)</span><span class="sxs-lookup"><span data-stu-id="7afc4-178">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="7afc4-179">Wählen Sie uner **Inhalt der E-Mail-Nachricht** die Option **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="7afc4-179">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="7afc4-180">Der Bereich **E-Mail-Vorlage hochladen** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7afc4-180">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="7afc4-181">Wählen Sie **Durchsuchen** aus, und finden Sie die HTML-Datei mit dem angepassten Inhalt.</span><span class="sxs-lookup"><span data-stu-id="7afc4-181">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="7afc4-182">Wählen Sie **Hochladen** aus.</span><span class="sxs-lookup"><span data-stu-id="7afc4-182">Select **Upload**.</span></span> <span data-ttu-id="7afc4-183">Die Vorlage wird in das System hochgeladen und eine Vorschau wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7afc4-183">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="7afc4-184">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="7afc4-184">Select **OK**.</span></span>
    1. <span data-ttu-id="7afc4-185">Optional: Passen Sie die Eigenschaft **Betreff** der Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="7afc4-185">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="7afc4-186">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="7afc4-186">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="7afc4-187">Unterstützte Token in der E-Mail-Vorlage</span><span class="sxs-lookup"><span data-stu-id="7afc4-187">Supported tokens in the email template</span></span>

<span data-ttu-id="7afc4-188">Diese Token werden beim Rendern per E-Mail durch die tatsächlichen Werte ersetzt, die für den Debitor und die Debitorenbestellung gelten.</span><span class="sxs-lookup"><span data-stu-id="7afc4-188">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="7afc4-189">Auftrag</span><span class="sxs-lookup"><span data-stu-id="7afc4-189">Sales order</span></span>

<span data-ttu-id="7afc4-190">Die folgenden Token gelten für den gesamten Auftrag.</span><span class="sxs-lookup"><span data-stu-id="7afc4-190">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="7afc4-191">Name des Token</span><span class="sxs-lookup"><span data-stu-id="7afc4-191">Name of the token</span></span> | <span data-ttu-id="7afc4-192">Token </span><span class="sxs-lookup"><span data-stu-id="7afc4-192">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="7afc4-193">Auftragsnummer</span><span class="sxs-lookup"><span data-stu-id="7afc4-193">Order number</span></span>      | <span data-ttu-id="7afc4-194">%salesid%</span><span class="sxs-lookup"><span data-stu-id="7afc4-194">%salesid%</span></span> |
| <span data-ttu-id="7afc4-195">Debitorenname</span><span class="sxs-lookup"><span data-stu-id="7afc4-195">Customer's name</span></span>   | <span data-ttu-id="7afc4-196">%customername%</span><span class="sxs-lookup"><span data-stu-id="7afc4-196">%customername%</span></span> |
| <span data-ttu-id="7afc4-197">Lieferadresse</span><span class="sxs-lookup"><span data-stu-id="7afc4-197">Delivery address</span></span>  | <span data-ttu-id="7afc4-198">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="7afc4-198">%deliveryaddress%</span></span> |
| <span data-ttu-id="7afc4-199">Rechnungsadresse</span><span class="sxs-lookup"><span data-stu-id="7afc4-199">Billing address</span></span>   | <span data-ttu-id="7afc4-200">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="7afc4-200">%customeraddress%</span></span> |
| <span data-ttu-id="7afc4-201">Spätestens</span><span class="sxs-lookup"><span data-stu-id="7afc4-201">Order date</span></span>        | <span data-ttu-id="7afc4-202">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="7afc4-202">%shipdate%</span></span> |
| <span data-ttu-id="7afc4-203">Liefermodus</span><span class="sxs-lookup"><span data-stu-id="7afc4-203">Delivery mode</span></span>     | <span data-ttu-id="7afc4-204">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="7afc4-204">%modeofdelivery%</span></span> |
| <span data-ttu-id="7afc4-205">Skonto</span><span class="sxs-lookup"><span data-stu-id="7afc4-205">Discount</span></span>          | <span data-ttu-id="7afc4-206">%discount%</span><span class="sxs-lookup"><span data-stu-id="7afc4-206">%discount%</span></span> |
| <span data-ttu-id="7afc4-207">Mehrwertsteuer</span><span class="sxs-lookup"><span data-stu-id="7afc4-207">Sales tax</span></span>         | <span data-ttu-id="7afc4-208">%tax%</span><span class="sxs-lookup"><span data-stu-id="7afc4-208">%tax%</span></span> |
| <span data-ttu-id="7afc4-209">Bestellung gesamt</span><span class="sxs-lookup"><span data-stu-id="7afc4-209">Order total</span></span>       | <span data-ttu-id="7afc4-210">%total%</span><span class="sxs-lookup"><span data-stu-id="7afc4-210">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="7afc4-211">Verkaufsposition</span><span class="sxs-lookup"><span data-stu-id="7afc4-211">Sales line</span></span>

<span data-ttu-id="7afc4-212">Die folgenden Token werden durch Werte für jedes Produkt im Auftrag ersetzt.</span><span class="sxs-lookup"><span data-stu-id="7afc4-212">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="7afc4-213">Setzen Sie den Token **Produktliste – Start** an den Anfang des HTML-Blocks, der für jedes Produkt wiederholt wird, und den Token **Produktliste – Ende** an das Ende des Blocks.</span><span class="sxs-lookup"><span data-stu-id="7afc4-213">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="7afc4-214">Name des Token</span><span class="sxs-lookup"><span data-stu-id="7afc4-214">Name of the token</span></span>      | <span data-ttu-id="7afc4-215">Token </span><span class="sxs-lookup"><span data-stu-id="7afc4-215">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="7afc4-216">Produktliste - Start</span><span class="sxs-lookup"><span data-stu-id="7afc4-216">Product list - start</span></span>   | <span data-ttu-id="7afc4-217">\<!--%tablebegin.salesline% --\></span><span class="sxs-lookup"><span data-stu-id="7afc4-217">\<!--%tablebegin.salesline% --\></span></span> |
| <span data-ttu-id="7afc4-218">Produktliste - Ende</span><span class="sxs-lookup"><span data-stu-id="7afc4-218">Product list - end</span></span>     | <span data-ttu-id="7afc4-219">\<!--%tableend.salesline%--\></span><span class="sxs-lookup"><span data-stu-id="7afc4-219">\<!--%tableend.salesline%--\></span></span> |
| <span data-ttu-id="7afc4-220">Produktname</span><span class="sxs-lookup"><span data-stu-id="7afc4-220">Product name</span></span>           | <span data-ttu-id="7afc4-221">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="7afc4-221">%lineproductname%</span></span> |
| <span data-ttu-id="7afc4-222">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7afc4-222">Description</span></span>            | <span data-ttu-id="7afc4-223">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="7afc4-223">%lineproductdescription%</span></span> |
| <span data-ttu-id="7afc4-224">Leistung</span><span class="sxs-lookup"><span data-stu-id="7afc4-224">Quantity</span></span>               | <span data-ttu-id="7afc4-225">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="7afc4-225">%linequantity%</span></span> |
| <span data-ttu-id="7afc4-226">Preiseinheit der Position</span><span class="sxs-lookup"><span data-stu-id="7afc4-226">Line unit price</span></span>        | <span data-ttu-id="7afc4-227">%lineprice% (prüfen)</span><span class="sxs-lookup"><span data-stu-id="7afc4-227">%lineprice% (verify)</span></span> |
| <span data-ttu-id="7afc4-228">Positionsartikel gesamt</span><span class="sxs-lookup"><span data-stu-id="7afc4-228">line item total</span></span>        | <span data-ttu-id="7afc4-229">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="7afc4-229">%linenetamount%</span></span> |
| <span data-ttu-id="7afc4-230">Positionsrabatt</span><span class="sxs-lookup"><span data-stu-id="7afc4-230">line discount</span></span>          | <span data-ttu-id="7afc4-231">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="7afc4-231">%linediscount%</span></span> |
| <span data-ttu-id="7afc4-232">Versanddatum</span><span class="sxs-lookup"><span data-stu-id="7afc4-232">Ship date</span></span>              | <span data-ttu-id="7afc4-233">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="7afc4-233">%lineshipdate%</span></span> |
| <span data-ttu-id="7afc4-234">Beschaffungsmethode</span><span class="sxs-lookup"><span data-stu-id="7afc4-234">Procurement method</span></span>     | <span data-ttu-id="7afc4-235">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="7afc4-235">%linedeliverymode%</span></span> |
| <span data-ttu-id="7afc4-236">Lieferadresse</span><span class="sxs-lookup"><span data-stu-id="7afc4-236">delivery address</span></span>       | <span data-ttu-id="7afc4-237">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="7afc4-237">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="7afc4-238">Verkaufseinheit der Position</span><span class="sxs-lookup"><span data-stu-id="7afc4-238">Sales unit of the line</span></span> | <span data-ttu-id="7afc4-239">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="7afc4-239">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="7afc4-240">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7afc4-240">Additional resources</span></span>

[<span data-ttu-id="7afc4-241">Commerce-Vorschauumgebung – Übersicht</span><span class="sxs-lookup"><span data-stu-id="7afc4-241">Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="7afc4-242">Bereitstellen einer Commerce-Vorschauumgebung</span><span class="sxs-lookup"><span data-stu-id="7afc4-242">Provision a Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="7afc4-243">Konfigurieren einer Commerce-Vorschauumgebung</span><span class="sxs-lookup"><span data-stu-id="7afc4-243">Configure a Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="7afc4-244">Commerce-Vorschauumgebung – FAQ</span><span class="sxs-lookup"><span data-stu-id="7afc4-244">Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="7afc4-245">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="7afc4-245">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="7afc4-246">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="7afc4-246">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="7afc4-247">Microsoft Azure-Portal</span><span class="sxs-lookup"><span data-stu-id="7afc4-247">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="7afc4-248">Dynamics 365 Commerce-Website</span><span class="sxs-lookup"><span data-stu-id="7afc4-248">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="7afc4-249">Hilferessourcen für Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="7afc4-249">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)