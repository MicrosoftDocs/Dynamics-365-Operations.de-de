---
title: Authentifizierung
description: Dieser Artikel enthält eine Übersicht über die Authentifizierung bei der Daten-Anwendungsprogrammierschnittstelle (API) von Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4e73438170294863b7aa092cf1fc027787f57c70
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054379"
---
# <a name="authentication"></a>Authentifizierung

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dieser Artikel enthält eine Übersicht über die Authentifizierung bei der Daten-Anwendungsprogrammierschnittstelle (API) von Microsoft Dynamics 365 Human Resources.

## <a name="overview"></a>Übersicht

Die Daten-API für Human Resources ist eine OData-Implementierung. Weitere Informationen finden Sie unter [Open Data Protocol (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).

Ihre Anwendung muss sich als autorisierter Aufrufer authentifizieren, bevor die API Anforderungen von Ihrer Anwendung bearbeiten kann.

## <a name="fundamentals"></a>Grundlagen

Zum Aufrufen der Daten-API muss Ihre Anwendung ein Zugriffstoken von der Microsoft Identity Platform erwerben. Das Zugriffstoken enthält Informationen zu Ihrer Anwendung und die Berechtigung, Ressourcen in Human Resources aufzurufen.

### <a name="access-token"></a>Zugriffstoken

Von der Microsoft Identity Platform ausgegebene Zugriffstoken sind Base64-codierte JSON-Web-Token (JWTs) (JavaScript Object Notation). Sie enthalten Informationen (Ansprüche), die die Daten-API (und andere von der Microsoft Identity Platform gesicherte Web-APIs) verwenden, um den Aufrufer zu validieren und sicherzustellen, dass der Aufrufer über die entsprechenden Berechtigungen zum Ausführen des von ihm angeforderten Vorgangs verfügt. Während eines Anrufs können Sie Zugriffstoken als undurchsichtig behandeln. Sie sollten Zugriffstoken immer über einen sicheren Kanal übertragen, z. B. über TLS (Transport Layer Security) und HTTPS (Hypertext Transfer Protocol Secure).

Hier ist ein Beispiel für ein Zugriffstoken, das von der Microsoft Identity Platform ausgegeben wird.

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

Um die Daten-API aufzurufen, hängen Sie das Zugriffstoken als Bearer-Token an den Autorisierungsheader in Ihrer HTTP-Anforderung an. Hier ist ein Beispiel.

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a>Eine neue Anwendung im Azure-Portal registrieren

1. Melden Sie sich mit einem Geschäfts- oder Schulkonto oder mit einem persönlichen Microsoft-Konto beim [Microsoft Azure-Portal](https://portal.azure.com) an.

2. Wenn Sie mit Ihrem Konto auf mehrere Mandanten zugreifen können, wählen Sie Ihr Konto in der oberen rechten Ecke aus und stellen Sie Ihre Portalsitzung auf den gewünschten Mandanten im Azure Active Directory (Azure AD) ein.

3. Wählen Sie zuerst im linken Bereich den **Azure Active Directory**-Dienst aus und wählen Sie dann **App-Registrierungen \> Neue Registrierung** aus.

4. Wenn die Seite **Registrieren einer Anwendung** angezeigt wird, geben Sie die Registrierungsinformationen Ihrer Anwendung ein:

    - **Name**: Geben Sie einen aussagekräftigen Anwendungsnamen ein, der den Benutzern der App angezeigt wird.
    - **Unterstützte Kontotypen**: Wählen Sie die Kontotypen aus, die Ihre App unterstützen soll.

        | Unterstützte Kontenarten | Beschreibung |
        |-------------------------|-------------|
        | Konten nur in diesem Organisationsverzeichnis | Wählen Sie diese Option aus, wenn Sie eine Branchen-App erstellen. Diese Option ist nur verfügbar, wenn Sie die App in einem Verzeichnis registrieren.<p>Diese Option ist **Azure AD nur Einzelmandant** zugeordnet.</p><p>Diese Option ist die Standardoption, sofern Sie die App nicht außerhalb eines Verzeichnisses registrieren. In diesem Fall ist die Standardoption **Azure AD mehrinstanzenfähige und persönliche Microsoft-Konten**.</p> |
        | Konten nur jedem Organisationsverzeichnis | Wählen Sie diese Option aus, um alle Geschäfts- und Ausbildungskunden anzusprechen.<p>Diese Option ist **Azure AD nur mehrinstanzenfähig** zugeordnet.</p><p>Wenn Sie die App als **Azure AD nur Einzelmandant** registriert haben, können Sie das Blade **Authentifizierung** verwenden, um ein Update auf **Azure AD nur mehrinstanzenfähig** durchzuführen und dann wieder zurück zu **Azure AD nur Einzelmandant** zu wechseln.</p> |
        | Konten in einem beliebigen Organisationsverzeichnis und persönliche Microsoft-Konten | Wählen Sie diese Option aus, um die meisten Kunden anzusprechen.<p>Diese Option ist **Azure AD mehrinstanzenfähige und persönliche Microsoft-Konten** zugeordnet.</p><p>Wenn Sie die App als **Azure AD mehrinstanzenfähige und persönliche Microsoft-Konten** registriert haben, können Sie diese Einstellung über die Benutzeroberfläche nicht ändern. Stattdessen müssen Sie den Anwendungsmanifest-Editor verwenden, um die unterstützten Kontotypen zu ändern.</p> |

    - **Umleitungs-URI (optional)**  – Wählen Sie den App-Typ aus, den Sie erstellen: **Internet** oder **Öffentlicher Client (Mobil und Desktop)**. Geben Sie dann den Umleitungs-URI (oder die Antwort-URL) für die App ein.

        - Geben Sie für Internetanwendungen die Basis-URL der App an. Beispielsweise könnte `http://localhost:31544` die URL für eine Internetanwendung sein, die auf Ihrem lokalen Computer ausgeführt wird. Benutzer verwenden diese URL, um sich bei einer Webclient-App anzumelden.
        - Geben Sie für öffentliche Client-Apps den URI an, den Azure AD verwendet, um Tokenantworten zurückzugeben. Geben Sie einen für Ihre App spezifischen Wert ein, z. B. `myapp://auth`.

        Spezielle Beispiele für Internetanwendungen oder native Apps finden Sie in den Schnellstarts unter [Microsoft Identity Platform (früher Azure Active Directory für Entwickler)](/azure/active-directory/develop/#quickstarts).

5. Wählen Sie unter **API-Berechtigungen** die Option **Ein Berechtigung hinzufügen** aus. Suchen Sie dann auf der Registerkarte **Von meiner Organisation verwendete APIs** nach **Dynamics 365 Human Resources** und fügen Sie Ihrer App die Berechtigung **benutzer\_identitätswechsel** hinzu. Die Anwendungs-ID für die Personalverteilung lautet f9be0c49-aa22-4ec6-911a-c5da515226ff. Verwenden Sie diese ID, um sicherzustellen, dass Sie die richtige Anwendung ausgewählt haben.

6. Wählen Sie **Registrieren** aus.

   [![Registrieren einer neuen App im Azure-Portal](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)

Azure AD weist Ihrer App eine eindeutige Anwendungs-ID (Client-ID) zu und führt Sie zur Seite **Übersicht** für Ihre App. Um Ihrer App weitere Funktionen hinzuzufügen, können Sie andere Konfigurationsoptionen auswählen, z. B. Optionen für das Branding sowie für Zertifikate und Geheimnisse.

## <a name="retrieving-an-access-token"></a>Ein Zugriffstoken abrufen

Wie Sie ein Zugriffstoken zum Aufrufen der Daten-API für Human Resources abrufen, hängt von den Technologien ab, die Sie zum Entwickeln Ihrer Clientanwendung verwenden. Mögliche Beispiele sind die [Durchführung von Tests mit einem Drittanbieter-Hilfsprogramm](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (z. B. Postman), die Entwicklung von C#-Konsolenanwendungen oder -Webdiensten oder die Erstellung eines JavaScript/TypeScript-Clients.

Beispiel für eine C#-Clientanwendung:
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

Nachdem Sie ein Zugriffstoken abgerufen haben, übergeben Sie das Token im Autorisierungsheader wie oben beschrieben bei jeder an die Daten-API gesendeten Anforderung als Bearer-Token.


[!INCLUDE[footer-include](../includes/footer-banner.md)]