---
title: Benutzer in Personenauswahl in Attract oder Onboard nicht gefunden
description: In diesem Thema wird erläutert, was zu tun ist, wenn Benutzer im Unternehmensmandanten nicht in der Personenauswahl in Dynamics 365 for Talent Attract oder Onboard-Anwendungen erscheinen.
author: ChrisChua
manager: AnnBe
ms.date: 01/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: chrichua
ms.search.validFrom: 2019-01-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2d4a74ee2cc65153c1f9fdc1b42c2fc440d188d6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "304586"
---
# <a name="azure-active-directory-users-not-found-in-people-picker"></a><span data-ttu-id="2e0f6-103">Azure Active Directory-Benutzer wurden nicht in der Personenauswahl gefunden</span><span class="sxs-lookup"><span data-stu-id="2e0f6-103">Azure Active Directory users not found in People Picker</span></span>

[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="2e0f6-104">Abgang</span><span class="sxs-lookup"><span data-stu-id="2e0f6-104">Issue</span></span>

<span data-ttu-id="2e0f6-105">Bestimmte gültige Benutzer in Microsoft Azure Active Directory (Azure AD) für den Mandanten erscheinen nicht, wenn Sie nach dem Namen in der Personenauswahl in Dynamics 365 for Talent Attract oder Onboard-Anwendungen suchen.</span><span class="sxs-lookup"><span data-stu-id="2e0f6-105">Certain valid users in Microsoft Azure Active Directory (Azure AD) for the tenant do not appear when searching for the name in the People Picker in the Dynamics 365 for Talent Attract or Onboard applications.</span></span>

## <a name="cause"></a><span data-ttu-id="2e0f6-106">Ursache</span><span class="sxs-lookup"><span data-stu-id="2e0f6-106">Cause</span></span>

<span data-ttu-id="2e0f6-107">Bestimmte Benutzertypen werden derzeit in den Anwendungen Attract und Onboard nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2e0f6-107">Certain user types are not currently supported in the Attract and Onboard applications.</span></span> <span data-ttu-id="2e0f6-108">Stellen Sie sicher, dass der Benutzer kein Azure AD Business to Business (B2B) Gastbenutzer ist.</span><span class="sxs-lookup"><span data-stu-id="2e0f6-108">Verify that the user is not an Azure AD Business to Business (B2B) guest user.</span></span> <span data-ttu-id="2e0f6-109">Die Informationen zum "Benutzertyp" finden Sie im Azure Active Directory-Blade auf dem Azure-Portal.</span><span class="sxs-lookup"><span data-stu-id="2e0f6-109">"User Type" information can be found in the Azure Active Directory blade on the Azure portal.</span></span>

<span data-ttu-id="2e0f6-110">Weitere Informationen zu Azure B2B, finden Sie unter [Was ist der Gastbenutzerzugriff in Azure Active Directory B2B](https://docs.microsoft.com/en-us/azure/active-directory/b2b/what-is-b2b).</span><span class="sxs-lookup"><span data-stu-id="2e0f6-110">For more information about Azure B2B, see [What is guest user access in Azure Active Directory B2B](https://docs.microsoft.com/en-us/azure/active-directory/b2b/what-is-b2b).</span></span>

<span data-ttu-id="2e0f6-111">Für Nicht-B2B-Benutzer gibt es bestimmte Benutzer, die möglicherweise eine unvollständige "Benutzertyp"-Eigenschaft auf dem **Benutzer**-Objekt haben.</span><span class="sxs-lookup"><span data-stu-id="2e0f6-111">For non-B2B users, there are certain users who may have an incomplete "User Type" property on the **User** object.</span></span> <span data-ttu-id="2e0f6-112">Dies kann mithilfe des Azure AD PowerShell-Moduls überprüft und korrigiert werden.</span><span class="sxs-lookup"><span data-stu-id="2e0f6-112">This can be verified and fixed using the Azure AD Powershell module.</span></span> <span data-ttu-id="2e0f6-113">Weitere Informationen finden Sie unter [Azure AD](https://docs.microsoft.com/en-us/powershell/module/azuread/?view=azureadps-2.0).</span><span class="sxs-lookup"><span data-stu-id="2e0f6-113">For more information, see [Azure AD](https://docs.microsoft.com/en-us/powershell/module/azuread/?view=azureadps-2.0).</span></span>

## <a name="resolution"></a><span data-ttu-id="2e0f6-114">Lösung</span><span class="sxs-lookup"><span data-stu-id="2e0f6-114">Resolution</span></span>

<span data-ttu-id="2e0f6-115">Um die folgenden Schritte zur Behebung des Problems durchzuführen, benötigen Sie die Berechtigungen "Global Administrator" für den Mandanten von Azure Active Directory oder die Berechtigungen für **User.ReadWrite.All**.</span><span class="sxs-lookup"><span data-stu-id="2e0f6-115">To complete the following steps to resolve the issue, you will need to have "Global Administrator" permissions on the Azure Active Directory tenant or permissions for **User.ReadWrite.All**.</span></span>

<span data-ttu-id="2e0f6-116">So überprüfen Sie den "Benutzertyp" für den betroffenen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="2e0f6-116">To verify the "User Type" for the affected user.</span></span>

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
<span data-ttu-id="2e0f6-117">Der Befehl gibt die folgenden Informationen zurück.</span><span class="sxs-lookup"><span data-stu-id="2e0f6-117">The command returns the following information.</span></span>
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
<span data-ttu-id="2e0f6-118">Beachten Sie die Eigenschaft **Benutzertyp** für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="2e0f6-118">Note the **UserType** property on the user.</span></span> <span data-ttu-id="2e0f6-119">Wenn **Benutzertyp** leer ist,beispielsweise nicht "Mitglied "oder "Gast", aktualisieren Sie den **Benutzertyp** mit folgenden Befehl.</span><span class="sxs-lookup"><span data-stu-id="2e0f6-119">If the **UserType** is blank, for example not "Member" or "Guest", update the **UserType** using the following command.</span></span>

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```