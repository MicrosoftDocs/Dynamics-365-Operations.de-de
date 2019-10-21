---
title: Benutzer in Personenauswahl in Attract oder Onboard nicht gefunden
description: In diesem Thema wird erläutert, was zu tun ist, wenn Benutzer im Unternehmensmandanten nicht in der Personenauswahl in Dynamics 365 Talent - Attract oder Onboard erscheinen.
author: andreabichsel
manager: AnnBe
ms.date: 01/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2a3c83fcc3f48aa235ffb2db2dc492b34a306c4c
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024188"
---
# <a name="azure-active-directory-users-not-found-in-people-picker"></a>Azure Active Directory-Benutzer wurden nicht in der Personenauswahl gefunden

[!include [banner](includes/banner.md)]

## <a name="issue"></a>Abgang

Bestimmte gültige Benutzer in Microsoft Azure Active Directory (Azure AD) für den Mandanten erscheinen nicht, wenn Sie nach dem Namen in der Personenauswahl in Dynamics 365 Talent: Attract oder Dynamics 365 Talent: Onboard suchen.

## <a name="cause"></a>Ursache

Bestimmte Benutzertypen werden derzeit in Attract und Onboard nicht unterstützt. Stellen Sie sicher, dass der Benutzer kein Azure AD Business to Business (B2B) Gastbenutzer ist. Die Informationen zum "Benutzertyp" finden Sie im Azure Active Directory-Blade auf dem Azure-Portal.

Weitere Informationen zu Azure B2B, finden Sie unter [Was ist der Gastbenutzerzugriff in Azure Active Directory B2B](https://docs.microsoft.com/azure/active-directory/b2b/what-is-b2b).

Für Nicht-B2B-Benutzer gibt es bestimmte Benutzer, die möglicherweise eine unvollständige "Benutzertyp"-Eigenschaft auf dem **Benutzer**-Objekt haben. Dies kann mithilfe des Azure AD PowerShell-Moduls überprüft und korrigiert werden. Weitere Informationen finden Sie unter [Azure AD](https://docs.microsoft.com/powershell/module/azuread/?view=azureadps-2.0).

## <a name="resolution"></a>Lösung

Um die folgenden Schritte zur Behebung des Problems durchzuführen, benötigen Sie die Berechtigungen "Global Administrator" für den Mandanten von Azure Active Directory oder die Berechtigungen für **User.ReadWrite.All**.

So überprüfen Sie den "Benutzertyp" für den betroffenen Benutzer.

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
Der Befehl gibt die folgenden Informationen zurück.
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
Beachten Sie die Eigenschaft **Benutzertyp** für den Benutzer. Wenn **Benutzertyp** leer ist,beispielsweise nicht "Mitglied "oder "Gast", aktualisieren Sie den **Benutzertyp** mit folgenden Befehl.

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```
