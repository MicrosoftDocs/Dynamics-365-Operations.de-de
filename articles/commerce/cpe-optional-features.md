---
title: Optionale Funktionen für eine Dynamics 365 Commerce-Auswertungsumgebung konfigurieren
description: In diesem Thema wird erläutert, wie optionale Funktionen für eine Microsoft Dynamics 365 Commerce-Auswertungsumgebung konfiguriert werden.
author: psimolin
manager: annbe
ms.date: 07/16/2020
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
ms.openlocfilehash: 6f7ba7e6de3791720458b509059f008423c73a82
ms.sourcegitcommit: 5175e3fae432016246244cf70fe05465f43de88c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/17/2020
ms.locfileid: "3599819"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="a458e-103">Optionale Funktionen für eine Dynamics 365 Commerce-Auswertungsumgebung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="a458e-103">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a458e-104">In diesem Thema wird erläutert, wie optionale Funktionen für eine Microsoft Dynamics 365 Commerce-Auswertungsumgebung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="a458e-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a458e-105">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="a458e-105">Prerequisites</span></span>

<span data-ttu-id="a458e-106">Wenn Sie die Transaktions-E-Mail-Funktionen bewerten möchten, müssen die folgenden Voraussetzungen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="a458e-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="a458e-107">Ihnen steht ein E-Mail-Server (Simple Mail Transfer Protocol \[SMTP\]-Server) zur Verfügung, der über das Microsoft Azure-Abonnement verwendet werden kann, auf dem Sie die Auswertungsumgebung bereitgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="a458e-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the evaluation environment.</span></span>
- <span data-ttu-id="a458e-108">Sie verfügen über den vollqualifizierten Domänennamen (FQDN)/die vollqualifizierte IP-Adresse, die SMTP-Portnummer und die Authentifizierungsdetails des Servers.</span><span class="sxs-lookup"><span data-stu-id="a458e-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="a458e-109">Konfigurieren Sie das Image-Backend</span><span class="sxs-lookup"><span data-stu-id="a458e-109">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="a458e-110">Auffinden Ihrer medienbasierten URL</span><span class="sxs-lookup"><span data-stu-id="a458e-110">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="a458e-111">Bevor Sie diesen Vorgang abschließen können, müssen Sie die Schritte in [Richten Sie Ihre Site in Commerce ein](cpe-post-provisioning.md#set-up-your-site-in-commerce) abschließen.</span><span class="sxs-lookup"><span data-stu-id="a458e-111">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="a458e-112">Melden Sie sich beim Commerce-Website-Generator mit der URL an, die Sie bei der Initialisierung von E-Commerce während der Bereitstellung notiert haben (siehe [E-Commerce initialisieren](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="a458e-112">Sign in to the Commerce site builder by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="a458e-113">Öffnen Sie die Site **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="a458e-113">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="a458e-114">Wählen Sie im linken Menü **Medienbibliothek** aus.</span><span class="sxs-lookup"><span data-stu-id="a458e-114">On the menu on the left, select **Media Library**.</span></span>
1. <span data-ttu-id="a458e-115">Wählen Sie ein einzelnes Image-Medienobjekt aus.</span><span class="sxs-lookup"><span data-stu-id="a458e-115">Select any single image asset.</span></span>
1. <span data-ttu-id="a458e-116">Suchen Sie im Eigenschafteninspektor rechts die Eigenschaft **Öffentliche URL**.</span><span class="sxs-lookup"><span data-stu-id="a458e-116">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="a458e-117">Der Wert ist eine URL.</span><span class="sxs-lookup"><span data-stu-id="a458e-117">The value is a URL.</span></span> <span data-ttu-id="a458e-118">Hier ist ein Beispiel:</span><span class="sxs-lookup"><span data-stu-id="a458e-118">Here is an example:</span></span>

    <span data-ttu-id="a458e-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span><span class="sxs-lookup"><span data-stu-id="a458e-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="a458e-120">Ersetzen Sie den letzten Bezeichner in der URL (**MA1nQC** im vorherigen Beispiel) durch die Zeichenfolge **search?fileName=**.</span><span class="sxs-lookup"><span data-stu-id="a458e-120">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="a458e-121">So sieht die Beispiel-URL nach dieser Änderung aus:</span><span class="sxs-lookup"><span data-stu-id="a458e-121">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="a458e-122">Diese URL ist Ihre Mediendatenbank-URL.</span><span class="sxs-lookup"><span data-stu-id="a458e-122">This URL is your media base URL.</span></span> <span data-ttu-id="a458e-123">Machen Sie sich eine Notiz davon.</span><span class="sxs-lookup"><span data-stu-id="a458e-123">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="a458e-124">Aktualisieren der medienbasierten URL</span><span class="sxs-lookup"><span data-stu-id="a458e-124">Update the media base URL</span></span>

1. <span data-ttu-id="a458e-125">Melden Sie sich bei der Commerce-Zentralverwaltung an.</span><span class="sxs-lookup"><span data-stu-id="a458e-125">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="a458e-126">Verwenden Sie das Menü auf der linken Seite, um zu **Module \> Retail and Commerce \> Kanaleinrichtung \> Kanalprofile** zu gehen.</span><span class="sxs-lookup"><span data-stu-id="a458e-126">Use the menu on the left to go to **Modules \> Retail and commerce \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="a458e-127">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="a458e-127">Select **Edit**.</span></span>
1. <span data-ttu-id="a458e-128">Ersetzen Sie unter **Profileigenschaften** den Wert für die Eigenschaft **Media Server-Basis-URL** durch die medienbasierte URL, die Sie zuvor erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="a458e-128">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="a458e-129">Wählen Sie den Kanal mit der Bezeichnung **scXXXXXXXXX** aus.</span><span class="sxs-lookup"><span data-stu-id="a458e-129">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="a458e-130">Wählen Sie unter **Profileigenschaften** die Option **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="a458e-130">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="a458e-131">Wählen Sie für die hinzugefügte Eigenschaft **Media Server-Basis-URL** als Eigenschaftsschlüssel aus.</span><span class="sxs-lookup"><span data-stu-id="a458e-131">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="a458e-132">Geben Sie als Eigenschaftswert die zuvor erstellte Media Base-URL ein.</span><span class="sxs-lookup"><span data-stu-id="a458e-132">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="a458e-133">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="a458e-133">Select **Save**.</span></span>

## <a name="configure-and-test-the-email-server"></a><span data-ttu-id="a458e-134">Den E-Mail-Server konfigurieren und testen</span><span class="sxs-lookup"><span data-stu-id="a458e-134">Configure and test the email server</span></span>

> [!NOTE]
> <span data-ttu-id="a458e-135">Der SMTP-Server oder E-Mail-Dienst, den Sie hier eingeben, muss über das Azure-Abonnement zugänglich sein muss, das Sie für die Umgebung verwenden.</span><span class="sxs-lookup"><span data-stu-id="a458e-135">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="a458e-136">Melden Sie sich bei der Commerce-Zentralverwaltung an.</span><span class="sxs-lookup"><span data-stu-id="a458e-136">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="a458e-137">Verwenden Sie das Menü links, um zu **Module \> Retail und Commerce \> Zentralverwaltungs-Setup \> Parameter \> E-Mail-Parameter** zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="a458e-137">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Email parameters**.</span></span>
1. <span data-ttu-id="a458e-138">Geben Sie auf der Registerkarte **SMTP-Einstellungen** im Feld **Name des SMTP-Servers** den vollständig qualifizierten Namen (FQDN) oder die IP-Adresse Ihres SMTP-Servers oder E-Mail-Dienstes an.</span><span class="sxs-lookup"><span data-stu-id="a458e-138">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="a458e-139">Geben Sie im Feld **SMTP-Portnummer** die Portnummer ein.</span><span class="sxs-lookup"><span data-stu-id="a458e-139">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="a458e-140">(Wenn Sie Secure Sockets Layer \[SSL\] nicht verwenden, lautet die Standardportnummer **25**.)</span><span class="sxs-lookup"><span data-stu-id="a458e-140">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="a458e-141">Wenn eine Authentifizierung erforderlich ist, geben Sie Werte in das Feld **Benutzername** und **Kennwort** ein.</span><span class="sxs-lookup"><span data-stu-id="a458e-141">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="a458e-142">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="a458e-142">Select **Save**.</span></span>
1. <span data-ttu-id="a458e-143">Wählen Sie **Aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="a458e-143">Select **Refresh**.</span></span>
1. <span data-ttu-id="a458e-144">Wählen Sie auf der Registerkarte **Test-E-mail** im Feld **E-Mail-Anbieter** die Option **SMTP** aus.</span><span class="sxs-lookup"><span data-stu-id="a458e-144">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="a458e-145">Geben Sie im Feld **Senden an** die E-Mail-Adresse ein, an die die Test-E-Mail gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a458e-145">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="a458e-146">Wählen Sie **Test-E-Mail senden** aus.</span><span class="sxs-lookup"><span data-stu-id="a458e-146">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="a458e-147">Konfigurieren der E-Mail-Vorlagen</span><span class="sxs-lookup"><span data-stu-id="a458e-147">Configure email templates</span></span>

<span data-ttu-id="a458e-148">Für jedes Transaktionsereignis, für das Sie E-Mails senden möchten, müssen Sie die E-Mail-Vorlage mit einer gültigen Absender-E-Mail-Adresse aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a458e-148">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="a458e-149">Melden Sie sich bei der Commerce-Zentralverwaltung an.</span><span class="sxs-lookup"><span data-stu-id="a458e-149">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="a458e-150">Verwenden Sie das Menü links, um zu **Module \> Retail und Commerce \> Zentralverwaltungs-Setup \> Parameter \> Organisations-E-Mail-Vorlagen** zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="a458e-150">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="a458e-151">Wählen Sie **Liste anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="a458e-151">Select **Show list**.</span></span>
1. <span data-ttu-id="a458e-152">Führen Sie für jede Vorlage in der Liste die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="a458e-152">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="a458e-153">Geben Sie im Feld **E-Mail des Absenders** die E-Mail-Adresse des Absenders ein.</span><span class="sxs-lookup"><span data-stu-id="a458e-153">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="a458e-154">Optional: Geben Sie im Feld **Absendername** den Namen ein, der als Absendername verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a458e-154">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="a458e-155">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="a458e-155">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="a458e-156">E-Mail-Vorlagen anpassen</span><span class="sxs-lookup"><span data-stu-id="a458e-156">Customize email templates</span></span>

<span data-ttu-id="a458e-157">Möglicherweise möchten Sie die E-Mail-Vorlagen so anpassen, dass sie unterschiedliche Bilder verwenden.</span><span class="sxs-lookup"><span data-stu-id="a458e-157">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="a458e-158">Oder Sie möchten die Links in den Vorlagen aktualisieren, damit sie in Ihre Auswertungsumgebung gelangen.</span><span class="sxs-lookup"><span data-stu-id="a458e-158">Or you might want to update the links in the templates so that they go to your evaluation environment.</span></span> <span data-ttu-id="a458e-159">In dieser Prozedur wird erläutert, wie Sie die Standardvorlagen herunterladen, anpassen und die Vorlagen im System aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a458e-159">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="a458e-160">Laden Sie über einen Webbrowser die [Microsoft Dynamics 365 Commerce--Auswertungsstandard-E-Mail-Vorlagen-ZIP-Datei](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) auf Ihren lokalen Computer herunter.</span><span class="sxs-lookup"><span data-stu-id="a458e-160">In a web browser, download the [Microsoft Dynamics 365 Commerce Evaluation default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="a458e-161">Diese Datei enthält die folgenden HTML-Dokumente:</span><span class="sxs-lookup"><span data-stu-id="a458e-161">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="a458e-162">Auftragsbestätigungsvorlage</span><span class="sxs-lookup"><span data-stu-id="a458e-162">Order confirmation template</span></span>
    - <span data-ttu-id="a458e-163">Geschenkkartenvorlage ausstellen</span><span class="sxs-lookup"><span data-stu-id="a458e-163">Issue gift card template</span></span>
    - <span data-ttu-id="a458e-164">Neue Auftragsvorlage</span><span class="sxs-lookup"><span data-stu-id="a458e-164">New order template</span></span>
    - <span data-ttu-id="a458e-165">Verpackungsvorlage</span><span class="sxs-lookup"><span data-stu-id="a458e-165">Pack order template</span></span>
    - <span data-ttu-id="a458e-166">Entnahmevorlage</span><span class="sxs-lookup"><span data-stu-id="a458e-166">Pick order template</span></span>

1. <span data-ttu-id="a458e-167">Passen Sie die Vorlagen mit einem Text- oder HTML-Editor an.</span><span class="sxs-lookup"><span data-stu-id="a458e-167">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="a458e-168">Schauen Sie sich die Lister der [unterstützten Token](#supported-tokens-in-the-email-template) später in diesem Thema an.</span><span class="sxs-lookup"><span data-stu-id="a458e-168">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="a458e-169">Melden Sie sich bei Commerce an.</span><span class="sxs-lookup"><span data-stu-id="a458e-169">Sign in to Commerce.</span></span>
1. <span data-ttu-id="a458e-170">Navigieren Sie über das Menü links zu **Module \> Organizationsverwaltung \> Einstellungen \> Organisations-E-Mail-Vorlagen**.</span><span class="sxs-lookup"><span data-stu-id="a458e-170">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="a458e-171">Erweitern Sie die Liste auf der linken Seite, um alle Vorlagen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a458e-171">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="a458e-172">Gehen Sie für jede Vorlage, die Sie anpassen möchten, folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="a458e-172">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="a458e-173">Wählen Sie die Vorlage in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="a458e-173">Select the template in the list.</span></span>
    1. <span data-ttu-id="a458e-174">Wählen Sie unter **Inhalt der E-Mail-Nachricht** die entsprechende Sprachversion in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="a458e-174">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="a458e-175">(Die Standardsprache lautet **en-us**.)</span><span class="sxs-lookup"><span data-stu-id="a458e-175">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="a458e-176">Wählen Sie uner **Inhalt der E-Mail-Nachricht** die Option **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="a458e-176">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="a458e-177">Der Bereich **E-Mail-Vorlage hochladen** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a458e-177">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="a458e-178">Wählen Sie **Durchsuchen** aus, und finden Sie die HTML-Datei mit dem angepassten Inhalt.</span><span class="sxs-lookup"><span data-stu-id="a458e-178">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="a458e-179">Wählen Sie **Hochladen** aus.</span><span class="sxs-lookup"><span data-stu-id="a458e-179">Select **Upload**.</span></span> <span data-ttu-id="a458e-180">Die Vorlage wird in das System hochgeladen und eine Vorschau wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a458e-180">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="a458e-181">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="a458e-181">Select **OK**.</span></span>
    1. <span data-ttu-id="a458e-182">Optional: Passen Sie die Eigenschaft **Betreff** der Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="a458e-182">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="a458e-183">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="a458e-183">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="a458e-184">Unterstützte Token in der E-Mail-Vorlage</span><span class="sxs-lookup"><span data-stu-id="a458e-184">Supported tokens in the email template</span></span>

<span data-ttu-id="a458e-185">Diese Token werden beim Rendern per E-Mail durch die tatsächlichen Werte ersetzt, die für den Debitor und die Debitorenbestellung gelten.</span><span class="sxs-lookup"><span data-stu-id="a458e-185">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="a458e-186">Auftrag</span><span class="sxs-lookup"><span data-stu-id="a458e-186">Sales order</span></span>

<span data-ttu-id="a458e-187">Die folgenden Token gelten für den gesamten Auftrag.</span><span class="sxs-lookup"><span data-stu-id="a458e-187">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="a458e-188">Name des Token</span><span class="sxs-lookup"><span data-stu-id="a458e-188">Name of the token</span></span> | <span data-ttu-id="a458e-189">Token </span><span class="sxs-lookup"><span data-stu-id="a458e-189">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="a458e-190">Auftragsnummer</span><span class="sxs-lookup"><span data-stu-id="a458e-190">Order number</span></span>      | <span data-ttu-id="a458e-191">%salesid%</span><span class="sxs-lookup"><span data-stu-id="a458e-191">%salesid%</span></span> |
| <span data-ttu-id="a458e-192">Debitorenname</span><span class="sxs-lookup"><span data-stu-id="a458e-192">Customer's name</span></span>   | <span data-ttu-id="a458e-193">%customername%</span><span class="sxs-lookup"><span data-stu-id="a458e-193">%customername%</span></span> |
| <span data-ttu-id="a458e-194">Lieferadresse</span><span class="sxs-lookup"><span data-stu-id="a458e-194">Delivery address</span></span>  | <span data-ttu-id="a458e-195">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="a458e-195">%deliveryaddress%</span></span> |
| <span data-ttu-id="a458e-196">Rechnungsadresse</span><span class="sxs-lookup"><span data-stu-id="a458e-196">Billing address</span></span>   | <span data-ttu-id="a458e-197">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="a458e-197">%customeraddress%</span></span> |
| <span data-ttu-id="a458e-198">Spätestens</span><span class="sxs-lookup"><span data-stu-id="a458e-198">Order date</span></span>        | <span data-ttu-id="a458e-199">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="a458e-199">%shipdate%</span></span> |
| <span data-ttu-id="a458e-200">Liefermodus</span><span class="sxs-lookup"><span data-stu-id="a458e-200">Delivery mode</span></span>     | <span data-ttu-id="a458e-201">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="a458e-201">%modeofdelivery%</span></span> |
| <span data-ttu-id="a458e-202">Skonto</span><span class="sxs-lookup"><span data-stu-id="a458e-202">Discount</span></span>          | <span data-ttu-id="a458e-203">%discount%</span><span class="sxs-lookup"><span data-stu-id="a458e-203">%discount%</span></span> |
| <span data-ttu-id="a458e-204">Mehrwertsteuer</span><span class="sxs-lookup"><span data-stu-id="a458e-204">Sales tax</span></span>         | <span data-ttu-id="a458e-205">%tax%</span><span class="sxs-lookup"><span data-stu-id="a458e-205">%tax%</span></span> |
| <span data-ttu-id="a458e-206">Bestellung gesamt</span><span class="sxs-lookup"><span data-stu-id="a458e-206">Order total</span></span>       | <span data-ttu-id="a458e-207">%total%</span><span class="sxs-lookup"><span data-stu-id="a458e-207">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="a458e-208">Verkaufsposition</span><span class="sxs-lookup"><span data-stu-id="a458e-208">Sales line</span></span>

<span data-ttu-id="a458e-209">Die folgenden Token werden durch Werte für jedes Produkt im Auftrag ersetzt.</span><span class="sxs-lookup"><span data-stu-id="a458e-209">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="a458e-210">Setzen Sie den Token **Produktliste – Start** an den Anfang des HTML-Blocks, der für jedes Produkt wiederholt wird, und den Token **Produktliste – Ende** an das Ende des Blocks.</span><span class="sxs-lookup"><span data-stu-id="a458e-210">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="a458e-211">Name des Token</span><span class="sxs-lookup"><span data-stu-id="a458e-211">Name of the token</span></span>      | <span data-ttu-id="a458e-212">Token</span><span class="sxs-lookup"><span data-stu-id="a458e-212">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="a458e-213">Produktliste - Start</span><span class="sxs-lookup"><span data-stu-id="a458e-213">Product list - start</span></span>   | \<!--%tablebegin.salesline% --\> |
| <span data-ttu-id="a458e-214">Produktliste - Ende</span><span class="sxs-lookup"><span data-stu-id="a458e-214">Product list - end</span></span>     | \<!--%tableend.salesline%--\> |
| <span data-ttu-id="a458e-215">Produktname</span><span class="sxs-lookup"><span data-stu-id="a458e-215">Product name</span></span>           | <span data-ttu-id="a458e-216">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="a458e-216">%lineproductname%</span></span> |
| <span data-ttu-id="a458e-217">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a458e-217">Description</span></span>            | <span data-ttu-id="a458e-218">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="a458e-218">%lineproductdescription%</span></span> |
| <span data-ttu-id="a458e-219">Leistung</span><span class="sxs-lookup"><span data-stu-id="a458e-219">Quantity</span></span>               | <span data-ttu-id="a458e-220">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="a458e-220">%linequantity%</span></span> |
| <span data-ttu-id="a458e-221">Preiseinheit der Position</span><span class="sxs-lookup"><span data-stu-id="a458e-221">Line unit price</span></span>        | <span data-ttu-id="a458e-222">%lineprice% (prüfen)</span><span class="sxs-lookup"><span data-stu-id="a458e-222">%lineprice% (verify)</span></span> |
| <span data-ttu-id="a458e-223">Positionsartikel gesamt</span><span class="sxs-lookup"><span data-stu-id="a458e-223">line item total</span></span>        | <span data-ttu-id="a458e-224">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="a458e-224">%linenetamount%</span></span> |
| <span data-ttu-id="a458e-225">Positionsrabatt</span><span class="sxs-lookup"><span data-stu-id="a458e-225">line discount</span></span>          | <span data-ttu-id="a458e-226">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="a458e-226">%linediscount%</span></span> |
| <span data-ttu-id="a458e-227">Versanddatum</span><span class="sxs-lookup"><span data-stu-id="a458e-227">Ship date</span></span>              | <span data-ttu-id="a458e-228">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="a458e-228">%lineshipdate%</span></span> |
| <span data-ttu-id="a458e-229">Beschaffungsmethode</span><span class="sxs-lookup"><span data-stu-id="a458e-229">Procurement method</span></span>     | <span data-ttu-id="a458e-230">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="a458e-230">%linedeliverymode%</span></span> |
| <span data-ttu-id="a458e-231">Lieferadresse</span><span class="sxs-lookup"><span data-stu-id="a458e-231">delivery address</span></span>       | <span data-ttu-id="a458e-232">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="a458e-232">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="a458e-233">Verkaufseinheit der Position</span><span class="sxs-lookup"><span data-stu-id="a458e-233">Sales unit of the line</span></span> | <span data-ttu-id="a458e-234">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="a458e-234">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="a458e-235">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a458e-235">Additional resources</span></span>

[<span data-ttu-id="a458e-236">Dynamics 365 Commerce-Auswertungsumgebung – Übersicht</span><span class="sxs-lookup"><span data-stu-id="a458e-236">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="a458e-237">Bereitstellen einer Dynamics 365 Commerce-Auswertungsumgebung</span><span class="sxs-lookup"><span data-stu-id="a458e-237">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="a458e-238">Konfigurieren einer Dynamics 365 Commerce-Auswertungsumgebung</span><span class="sxs-lookup"><span data-stu-id="a458e-238">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="a458e-239">BOPIS in einer Dynamics 365 Commerce-Auswertungsumgebung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="a458e-239">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="a458e-240">Dynamics 365 Commerce-Auswertungsumgebung – FAQ</span><span class="sxs-lookup"><span data-stu-id="a458e-240">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="a458e-241">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="a458e-241">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="a458e-242">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="a458e-242">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="a458e-243">Microsoft Azure-Portal</span><span class="sxs-lookup"><span data-stu-id="a458e-243">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="a458e-244">Dynamics 365 Commerce-Website</span><span class="sxs-lookup"><span data-stu-id="a458e-244">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
