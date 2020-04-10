---
title: Erstellen neuer Benutzer
description: Benutzer sind interne Mitarbeiter der Organisation oder externe Debitoren und Kreditoren, die Zugriff auf Microsoft Dynamics AX anfordern, ihre Einzelvorgänge auszuführen.
author: maertenm
manager: AnnBe
ms.date: 02/06/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9db4b6d355d6499bce6c550b2fbe76b82cf69fd4
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143576"
---
# <a name="create-new-users"></a>Erstellen neuer Benutzer

[!include [banner](../../includes/banner.md)]

Benutzer sind interne Mitarbeiter der Organisation oder externe Debitoren und Kreditoren, die Zugriff auf das System anfordern, um ihre Einzelvorgänge auszuführen.

## <a name="associate-a-user-with-a-license-new-license-types-only"></a>Zuordnen eines Benutzers zu einer Lizenz (nur neue Lizenztypen)
Für Debitoren mit einem der neuen Lizenztypen, die im Oktober 2019 hinzugefügt wurden, müssen Benutzern eine Lizenz zugeordnet werden. Benutzer, die einer Lizenz zugeordnet sind, werden automatisch als Systembenutzer hinzugefügt, die bei der ersten Anmeldung keine Rollen haben.

Systemadministratoren können [Benutzern Lizenzen zuordnen](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) – im [Microsoft 365 Admin Center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).

## <a name="associate-an-external-user-with-a-license-new-license-types-only"></a>Zuordnen eines externen Benutzers zu einer Lizenz (nur neue Lizenztypen)
Benutzer außerhalb des Mandanten, in dem die Umgebung bereitgestellt wurde, müssen im Host-Mandantenverzeichnis vertreten sein ( Azure Active Directory ( Azure AD)), damit ihnen Lizenzen zugewiesen werden können. Diese externen Benutzer sollten dem Mandanten in Azure AD als Gastbenutzer hinzugefügt werden und dann sollten ihnen die entsprechenden Lizenzen zugewiesen werden. Weitere Informationen finden Sie unter [Azure Active Directory Benutzer der B2B-Zusammenarbeit im Azure-Portal hinzufügen](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).

## <a name="add-a-new-user"></a>Hinzufügen eines neuen Benutzers
1. Wechseln Sie zu **Systemverwaltung \> Benutzer \> Benutzer**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus.
3. Geben Sie im Feld **Benutzerkennung** eine eindeutige Kennung für den Benutzer ein. Geben Sie ein Kennwort ein.  
4. Geben Sie im Feld **Benutzername** den Namen des Benutzers ein.  
5. Geben Sie im Feld **Domain** die Domäne des Benutzers ein.  
6. Geben Sie im Feld **Alias** den Alias des Benutzers ein.  
7. Wählen Sie im Feld **Unternehmen** das gewünschte Unternehmen aus. 
8. Wählen Sie im Inforegister **Benutzerrollen** die Option **Rollen zuweisen** aus, um Sicherheitsrollen zuzuweisen. Ausführlichere Informationen finden Sie unter [Zuweisen von Benutzern zu Sicherheitsrollen](assign-users-security-roles.md).
9. Wählen Sie **OK**.
10. Wählen Sie **Speichern**.

## <a name="import-users"></a>Benutzer importieren
1. Wählen Sie im Aktivitätsbereich **Benutzer importieren** aus.
2. Markieren Sie in der Liste die ausgewählte Zeile.
3. Wählen Sie **Benutzer importieren** aus.
4. Wählen Sie **Schließen** aus.

