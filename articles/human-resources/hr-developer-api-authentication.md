---
title: Authentifizierung
description: Dieser Artikel enthält eine Übersicht über die Authentifizierung bei der Daten-Anwendungsprogrammierschnittstelle (API) von Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a0509ce99205d49d516e180203ffb65a1dc09a7c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418608"
---
# <a name="authentication"></a><span data-ttu-id="c6763-103">Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="c6763-103">Authentication</span></span>

<span data-ttu-id="c6763-104">Dieser Artikel enthält eine Übersicht über die Authentifizierung bei der Daten-Anwendungsprogrammierschnittstelle (API) von Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c6763-104">This article provides overview information about how to authenticate with the Microsoft Dynamics 365 Human Resources data application programming interface (API).</span></span>

## <a name="overview"></a><span data-ttu-id="c6763-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="c6763-105">Overview</span></span>

<span data-ttu-id="c6763-106">Die Daten-API für Human Resources ist eine OData-Implementierung.</span><span class="sxs-lookup"><span data-stu-id="c6763-106">The data API for Human Resources is an OData implementation.</span></span> <span data-ttu-id="c6763-107">Weitere Informationen finden Sie unter [Open Data Protocol (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).</span><span class="sxs-lookup"><span data-stu-id="c6763-107">For more information, see [Open Data Protocol (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).</span></span>

<span data-ttu-id="c6763-108">Ihre Anwendung muss sich als autorisierter Aufrufer authentifizieren, bevor die API Anforderungen von Ihrer Anwendung bearbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="c6763-108">Your application must authenticate as an authorized caller before the API will service requests from your application.</span></span>

## <a name="fundamentals"></a><span data-ttu-id="c6763-109">Grundlagen</span><span class="sxs-lookup"><span data-stu-id="c6763-109">Fundamentals</span></span>

<span data-ttu-id="c6763-110">Zum Aufrufen der Daten-API muss Ihre Anwendung ein Zugriffstoken von der Microsoft Identity Platform erwerben.</span><span class="sxs-lookup"><span data-stu-id="c6763-110">To call the data API, your application must acquire an access token from the Microsoft identity platform.</span></span> <span data-ttu-id="c6763-111">Das Zugriffstoken enthält Informationen zu Ihrer Anwendung und die Berechtigung, Ressourcen in Human Resources aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c6763-111">The access token contains information about your application and the permission that it has to call resources in Human Resources.</span></span>

### <a name="access-token"></a><span data-ttu-id="c6763-112">Zugriffstoken</span><span class="sxs-lookup"><span data-stu-id="c6763-112">Access token</span></span>

<span data-ttu-id="c6763-113">Von der Microsoft Identity Platform ausgegebene Zugriffstoken sind Base64-codierte JSON-Web-Token (JWTs) (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="c6763-113">Access tokens issued by the Microsoft identity platform are base64–encoded JavaScript Object Notation (JSON) Web Tokens (JWTs).</span></span> <span data-ttu-id="c6763-114">Sie enthalten Informationen (Ansprüche), die die Daten-API (und andere von der Microsoft Identity Platform gesicherte Web-APIs) verwenden, um den Aufrufer zu validieren und sicherzustellen, dass der Aufrufer über die entsprechenden Berechtigungen zum Ausführen des von ihm angeforderten Vorgangs verfügt.</span><span class="sxs-lookup"><span data-stu-id="c6763-114">They contain information (claims) that the data API (and other web APIs that are secured by the Microsoft identity platform) use to validate the caller and make sure that the caller has the correct permissions to perform the operation they're requesting.</span></span> <span data-ttu-id="c6763-115">Während eines Anrufs können Sie Zugriffstoken als undurchsichtig behandeln.</span><span class="sxs-lookup"><span data-stu-id="c6763-115">During calls, you can treat access tokens as opaque.</span></span> <span data-ttu-id="c6763-116">Sie sollten Zugriffstoken immer über einen sicheren Kanal übertragen, z. B. über TLS (Transport Layer Security) und HTTPS (Hypertext Transfer Protocol Secure).</span><span class="sxs-lookup"><span data-stu-id="c6763-116">You should always transmit access tokens over a secure channel, such as Transport Layer Security (TLS) and Hypertext Transfer Protocol Secure (HTTPS).</span></span>

<span data-ttu-id="c6763-117">Hier ist ein Beispiel für ein Zugriffstoken, das von der Microsoft Identity Platform ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c6763-117">Here is an example of an access token that is issued by the Microsoft identity platform.</span></span>

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

<span data-ttu-id="c6763-118">Um die Daten-API aufzurufen, hängen Sie das Zugriffstoken als Bearer-Token an den Autorisierungsheader in Ihrer HTTP-Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="c6763-118">To call the data API, you attach the access token as a bearer token to the authorization header in your HTTP request.</span></span> <span data-ttu-id="c6763-119">Hier ist ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="c6763-119">Here is an example.</span></span>

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a><span data-ttu-id="c6763-120">Eine neue Anwendung im Azure-Portal registrieren</span><span class="sxs-lookup"><span data-stu-id="c6763-120">Register a new application by using the Azure portal</span></span>

1. <span data-ttu-id="c6763-121">Melden Sie sich mit einem Geschäfts- oder Schulkonto oder mit einem persönlichen Microsoft-Konto beim [Microsoft Azure-Portal](https://portal.azure.com) an.</span><span class="sxs-lookup"><span data-stu-id="c6763-121">Sign in to the [Microsoft Azure portal](https://portal.azure.com) with a work or school account, or a personal Microsoft account.</span></span>

2. <span data-ttu-id="c6763-122">Wenn Sie mit Ihrem Konto auf mehrere Mandanten zugreifen können, wählen Sie Ihr Konto in der oberen rechten Ecke aus und stellen Sie Ihre Portalsitzung auf den gewünschten Mandanten im Azure Active Directory (Azure AD) ein.</span><span class="sxs-lookup"><span data-stu-id="c6763-122">If your account gives you access to more than one tenant, select your account in the upper-right corner, and set your portal session to the Azure Active Directory (Azure AD) tenant that you want.</span></span>

3. <span data-ttu-id="c6763-123">Wählen Sie zuerst im linken Bereich den **Azure Active Directory**-Dienst aus und wählen Sie dann **App-Registrierungen \> Neue Registrierung** aus.</span><span class="sxs-lookup"><span data-stu-id="c6763-123">In the left pane, select the **Azure Active Directory** service, and then select **App registrations \> New registration**.</span></span>

4. <span data-ttu-id="c6763-124">Wenn die Seite **Registrieren einer Anwendung** angezeigt wird, geben Sie die Registrierungsinformationen Ihrer Anwendung ein:</span><span class="sxs-lookup"><span data-stu-id="c6763-124">When the **Register an application** page appears, enter your application's registration information:</span></span>

    - <span data-ttu-id="c6763-125">**Name**: Geben Sie einen aussagekräftigen Anwendungsnamen ein, der den Benutzern der App angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c6763-125">**Name**: Enter a meaningful application name that will be shown to users of the app.</span></span>
    - <span data-ttu-id="c6763-126">**Unterstützte Kontotypen**: Wählen Sie die Kontotypen aus, die Ihre App unterstützen soll.</span><span class="sxs-lookup"><span data-stu-id="c6763-126">**Supported account types**: Select the types of accounts that your app should support.</span></span>

        | <span data-ttu-id="c6763-127">Unterstützte Kontenarten</span><span class="sxs-lookup"><span data-stu-id="c6763-127">Supported account types</span></span> | <span data-ttu-id="c6763-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6763-128">Description</span></span> |
        |-------------------------|-------------|
        | <span data-ttu-id="c6763-129">Konten nur in diesem Organisationsverzeichnis</span><span class="sxs-lookup"><span data-stu-id="c6763-129">Accounts in this organizational directory only</span></span> | <span data-ttu-id="c6763-130">Wählen Sie diese Option aus, wenn Sie eine Branchen-App erstellen.</span><span class="sxs-lookup"><span data-stu-id="c6763-130">Select this option if you're building a line-of-business app.</span></span> <span data-ttu-id="c6763-131">Diese Option ist nur verfügbar, wenn Sie die App in einem Verzeichnis registrieren.</span><span class="sxs-lookup"><span data-stu-id="c6763-131">This option isn't available unless you're registering the app in a directory.</span></span><p><span data-ttu-id="c6763-132">Diese Option ist **Azure AD nur Einzelmandant** zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c6763-132">This option is mapped to **Azure AD only single-tenant**.</span></span></p><p><span data-ttu-id="c6763-133">Diese Option ist die Standardoption, sofern Sie die App nicht außerhalb eines Verzeichnisses registrieren.</span><span class="sxs-lookup"><span data-stu-id="c6763-133">This option is the default option unless you're registering the app outside a directory.</span></span> <span data-ttu-id="c6763-134">In diesem Fall ist die Standardoption **Azure AD mehrinstanzenfähige und persönliche Microsoft-Konten**.</span><span class="sxs-lookup"><span data-stu-id="c6763-134">In that case, the default option is **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p> |
        | <span data-ttu-id="c6763-135">Konten nur jedem Organisationsverzeichnis</span><span class="sxs-lookup"><span data-stu-id="c6763-135">Accounts in any organizational directory</span></span> | <span data-ttu-id="c6763-136">Wählen Sie diese Option aus, um alle Geschäfts- und Ausbildungskunden anzusprechen.</span><span class="sxs-lookup"><span data-stu-id="c6763-136">Select this option to target all business and educational customers.</span></span><p><span data-ttu-id="c6763-137">Diese Option ist **Azure AD nur mehrinstanzenfähig** zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c6763-137">This option is mapped to **Azure AD only multi-tenant**.</span></span></p><p><span data-ttu-id="c6763-138">Wenn Sie die App als **Azure AD nur Einzelmandant** registriert haben, können Sie das Blade **Authentifizierung** verwenden, um ein Update auf **Azure AD nur mehrinstanzenfähig** durchzuführen und dann wieder zurück zu **Azure AD nur Einzelmandant** zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="c6763-138">If you registered the app as **Azure AD only single-tenant**, you can use the **Authentication** blade to update it to **Azure AD only multi-tenant** and then back to **Azure AD only single-tenant**.</span></span></p> |
        | <span data-ttu-id="c6763-139">Konten in einem beliebigen Organisationsverzeichnis und persönliche Microsoft-Konten</span><span class="sxs-lookup"><span data-stu-id="c6763-139">Accounts in any organizational directory and personal Microsoft accounts</span></span> | <span data-ttu-id="c6763-140">Wählen Sie diese Option aus, um die meisten Kunden anzusprechen.</span><span class="sxs-lookup"><span data-stu-id="c6763-140">Select this option to target the widest set of customers.</span></span><p><span data-ttu-id="c6763-141">Diese Option ist **Azure AD mehrinstanzenfähige und persönliche Microsoft-Konten** zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c6763-141">This option is mapped to **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p><p><span data-ttu-id="c6763-142">Wenn Sie die App als **Azure AD mehrinstanzenfähige und persönliche Microsoft-Konten** registriert haben, können Sie diese Einstellung über die Benutzeroberfläche nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="c6763-142">If you registered the app as **Azure AD multi-tenant and personal Microsoft accounts**, you can't change this setting in the user interface (UI).</span></span> <span data-ttu-id="c6763-143">Stattdessen müssen Sie den Anwendungsmanifest-Editor verwenden, um die unterstützten Kontotypen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c6763-143">Instead, you must use the application manifest editor to change the supported account types.</span></span></p> |

    - <span data-ttu-id="c6763-144">**Umleitungs-URI (optional)**  – Wählen Sie den App-Typ aus, den Sie erstellen: **Internet** oder **Öffentlicher Client (Mobil und Desktop)**.</span><span class="sxs-lookup"><span data-stu-id="c6763-144">**Redirect URI (optional)** – Select the type of app that you're building: **Web** or **Public client (mobile & desktop)**.</span></span> <span data-ttu-id="c6763-145">Geben Sie dann den Umleitungs-URI (oder die Antwort-URL) für die App ein.</span><span class="sxs-lookup"><span data-stu-id="c6763-145">Then enter the redirect URI (or reply URL) for the app.</span></span>

        - <span data-ttu-id="c6763-146">Geben Sie für Internetanwendungen die Basis-URL der App an.</span><span class="sxs-lookup"><span data-stu-id="c6763-146">For web apps, provide the base URL of the app.</span></span> <span data-ttu-id="c6763-147">Beispielsweise könnte `http://localhost:31544` die URL für eine Internetanwendung sein, die auf Ihrem lokalen Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c6763-147">For example, `http://localhost:31544` might be the URL for a web app that runs on your local machine.</span></span> <span data-ttu-id="c6763-148">Benutzer verwenden diese URL, um sich bei einer Webclient-App anzumelden.</span><span class="sxs-lookup"><span data-stu-id="c6763-148">Users then use this URL to sign in to a web client app.</span></span>
        - <span data-ttu-id="c6763-149">Geben Sie für öffentliche Client-Apps den URI an, den Azure AD verwendet, um Tokenantworten zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="c6763-149">For public client apps, provide the URI that Azure AD uses to return token responses.</span></span> <span data-ttu-id="c6763-150">Geben Sie einen für Ihre App spezifischen Wert ein, z. B. `myapp://auth`.</span><span class="sxs-lookup"><span data-stu-id="c6763-150">Enter a value that is specific to your app, such as `myapp://auth`.</span></span>

        <span data-ttu-id="c6763-151">Spezielle Beispiele für Internetanwendungen oder native Apps finden Sie in den Schnellstarts unter [Microsoft Identity Platform (früher Azure Active Directory für Entwickler)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).</span><span class="sxs-lookup"><span data-stu-id="c6763-151">To see specific examples for web apps or native apps, see the quickstarts in [Microsoft identity platform (formerly Azure Active Directory for developers)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).</span></span>

5. <span data-ttu-id="c6763-152">Wählen Sie unter **API-Berechtigungen** die Option **Ein Berechtigung hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="c6763-152">Under **API permissions**, select **Add a permission**.</span></span> <span data-ttu-id="c6763-153">Suchen Sie dann auf der Registerkarte **Von meiner Organisation verwendete APIs** nach **Dynamics 365 Human Resources** und fügen Sie Ihrer App die Berechtigung **benutzer\_identitätswechsel** hinzu.</span><span class="sxs-lookup"><span data-stu-id="c6763-153">Then, on the **APIs my organization uses** tab, search for **Dynamics 365 Human Resources**, and add the **user\_impersonation** permission to your app.</span></span> <span data-ttu-id="c6763-154">Die Anwendungs-ID für die Personalverteilung lautet f9be0c49-aa22-4ec6-911a-c5da515226ff.</span><span class="sxs-lookup"><span data-stu-id="c6763-154">The Application ID for Human Resources is f9be0c49-aa22-4ec6-911a-c5da515226ff.</span></span> <span data-ttu-id="c6763-155">Verwenden Sie diese ID, um sicherzustellen, dass Sie die richtige Anwendung ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="c6763-155">Use this ID to ensure you have chosen the correct application.</span></span>

6. <span data-ttu-id="c6763-156">Wählen Sie **Registrieren** aus.</span><span class="sxs-lookup"><span data-stu-id="c6763-156">Select **Register**.</span></span>

   <span data-ttu-id="c6763-157">[![Registrieren einer neuen App im Azure-Portal](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="c6763-157">[![Registering a new app in the Azure portal](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span></span>

<span data-ttu-id="c6763-158">Azure AD weist Ihrer App eine eindeutige Anwendungs-ID (Client-ID) zu und führt Sie zur Seite **Übersicht** für Ihre App.</span><span class="sxs-lookup"><span data-stu-id="c6763-158">Azure AD assigns a unique application ID (client ID) to your app, and takes you to the **Overview** page for your app.</span></span> <span data-ttu-id="c6763-159">Um Ihrer App weitere Funktionen hinzuzufügen, können Sie andere Konfigurationsoptionen auswählen, z. B. Optionen für das Branding sowie für Zertifikate und Geheimnisse.</span><span class="sxs-lookup"><span data-stu-id="c6763-159">To add more capabilities to your app, you can select other configuration options, such as options for branding and for certificates and secrets.</span></span>

## <a name="retrieving-an-access-token"></a><span data-ttu-id="c6763-160">Ein Zugriffstoken abrufen</span><span class="sxs-lookup"><span data-stu-id="c6763-160">Retrieving an access token</span></span>

<span data-ttu-id="c6763-161">Wie Sie ein Zugriffstoken zum Aufrufen der Daten-API für Human Resources abrufen, hängt von den Technologien ab, die Sie zum Entwickeln Ihrer Clientanwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="c6763-161">The specifics of how you retrieve an access token for calling the Human Resources data API will depend on what technologies you're using to develop your client application.</span></span> <span data-ttu-id="c6763-162">Mögliche Beispiele sind die [Durchführung von Tests mit einem Drittanbieter-Hilfsprogramm](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (z. B. Postman), die Entwicklung von C#-Konsolenanwendungen oder -Webdiensten oder die Erstellung eines JavaScript/TypeScript-Clients.</span><span class="sxs-lookup"><span data-stu-id="c6763-162">For example, you might be [testing with a third party utility](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (such as Postman), developing a C# console application or web service, or building a javascript/TypeScript client.</span></span>

<span data-ttu-id="c6763-163">Beispiel für eine C#-Clientanwendung:</span><span class="sxs-lookup"><span data-stu-id="c6763-163">Example C# client application:</span></span>
```C#
using System;
using System.Net.Http;
using System.Threading.Tasks;

// requires appropriate NuGet package references in the project
using Microsoft.IdentityModel.Clients.ActiveDirectory;

namespace TalentODataPoC
{
    class Program
    {
        // prereq: This client app must be registered in Azure Active Directory. The app must be
        // registered as requiring permission to the Dynamics 365 for Talent API (with the Dynamics
        // HCM Workload delegated permission).
        static string clientId = "4fc703ef-672c-4e2c-813f-2f9d29d726db"; // This value should be obtained from AAD and must match your registered app
        static string talentNamespaceUri = "";

        public static async Task CallTalentODataService()
        {
            // authority URI
            UriBuilder uri = new UriBuilder("https://login.microsoftonline.com/common");
            AuthenticationContext authenticationContext = new AuthenticationContext(uri.ToString());

            // request token for the resource we want to access (Human Resources). This will authenticate
            // the user and return an access token containing claims for the authenticated user.
            var authResult = await authenticationContext.AcquireTokenAsync(
                "http://hr.talent.dynamics.com", /*Talent app id or resource URI*/
                clientId, /*registered client app id*/
                new Uri("https://localhost"), /*redirect URI, as registered in your AAD app*/
                new PlatformParameters(PromptBehavior.SelectAccount));

            // create the authorization header, which needs to be passed in the Header of the HTTP Requests to Talent
            string authHeader = authResult.CreateAuthorizationHeader();

            // HINT: paste the JWT into https://jwt.ms to decode and view it
            Console.Write("authHeader: ");
            Console.WriteLine(authHeader);
            Console.WriteLine();

            HttpClient client = new HttpClient();
            client.DefaultRequestHeaders.Add("Authorization", authHeader);

            string s;

            Console.Write("Talent Namespace URI: ");
            Console.WriteLine(talentNamespaceUri);
            Console.WriteLine();

            // call the OData service to get JobType data from Talent
            var resultOdata = await client.GetAsync(talentNamespaceUri + "data/JobTypes");
            s = await resultOdata.Content.ReadAsStringAsync();
            Console.WriteLine(s);
            Console.WriteLine();
        }

        static void Main(string[] args)
        {
            Console.WriteLine();

            // if the user passes in a single parameter, assume it is the namespaceUri for Talent
            if (args.Length == 1)
            {
                talentNamespaceUri = args[0];
            } else if (args.Length == 0)
            {
                Console.WriteLine("Enter Talent URL including namespace.");
                Console.WriteLine("Example: https://aos-rts-sf-21454f9d830-prod-westus2.hr.talent.dynamics.com/namespaces/2328af1a-2d45-4c6a-99e3-12a4c3867dcf/");
                Console.Write("> ");
                talentNamespaceUri = Console.ReadLine();
                if (!talentNamespaceUri.EndsWith("/"))
                {
                    talentNamespaceUri = talentNamespaceUri + "/";
                }
            } else
            {
                Console.WriteLine("Unexpected Arguments");
                System.Environment.Exit(1);
            }

            Task t = Program.CallTalentODataService();
            t.Wait();
        }
    }
}
```

<span data-ttu-id="c6763-164">Nachdem Sie ein Zugriffstoken abgerufen haben, übergeben Sie das Token im Autorisierungsheader wie oben beschrieben bei jeder an die Daten-API gesendeten Anforderung als Bearer-Token.</span><span class="sxs-lookup"><span data-stu-id="c6763-164">Once you've retrieved an access token, you'll pass the token in the Authorization header as a bearer token with each request you send to the data API, as described above.</span></span>
