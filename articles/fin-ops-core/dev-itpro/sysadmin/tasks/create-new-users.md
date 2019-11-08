---
title: Erstellen neuer Benutzer
description: Benutzer sind interne Mitarbeiter der Organisation oder externe Debitoren und Kreditoren, die Zugriff auf Microsoft Dynamics AX anfordern, ihre Einzelvorgänge auszuführen.
author: maertenm
manager: AnnBe
ms.date: 10/08/2019
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
ms.openlocfilehash: 3c347a34a389c32d005cc8086c4a1349ecb8a698
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570520"
---
# <a name="create-new-users"></a>Erstellen neuer Benutzer

[!include [task guide banner](../../includes/task-guide-banner.md)]

Benutzer sind interne Mitarbeiter der Organisation oder externe Debitoren und Kreditoren, die Zugriff auf das System anfordern, um ihre Einzelvorgänge auszuführen.

## <a name="associate-a-user-with-a-license-new-license-types-only"></a>Zuordnen eines Benutzers zu einer Lizenz (nur neue Lizenztypen)
Für Debitoren mit einem der neuen Lizenztypen, die im Oktober 2019 hinzugefügt wurden, müssen Benutzern eine Lizenz zugeordnet werden. Benutzer, die einer Lizenz zugeordnet sind, werden automatisch als Systembenutzer hinzugefügt, die bei der ersten Anmeldung keine Rollen haben. Benutzer, denen keine Lizenz zugeordnet ist, erhalten eine Warnmeldung.

Systemadministratoren können [Benutzern Lizenzen zuordnen](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) – im [Microsoft 365 Admin Center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).

## <a name="add-a-new-user"></a>Hinzufügen eines neuen Benutzers
1. Wechseln Sie zu **Systemverwaltung \> Benutzer \> Benutzer**.
2. Wählen Sie im Aktivitätsbereich **Neu** aus.
3. Geben Sie im Feld **Benutzerkennung** eine eindeutige Kennung für den Benutzer ein. Geben Sie ein Kennwort ein.  
4. Geben Sie im Feld **Benutzername** den Namen des Benutzers ein.  
5. Geben Sie im Feld **Domain** die Domäne des Benutzers ein.  
6. Geben Sie im Feld **Alias** den Alias des Benutzers ein.  
7. Wählen Sie im Feld **Unternehmen** das gewünschte Unternehmen aus. 
8. Setzen Sie im Inforegister **Benutzerrollen** die Option **Rollen zuweisen** auf [Zuweisen von Benutzern zu Sicherheitsrollen](assign-users-security-roles.md)
9. Wählen Sie **OK**.
10. Wählen Sie **Speichern**.

## <a name="import-users"></a>Benutzer importieren
1. Wählen Sie im Aktivitätsbereich **Benutzer importieren** aus.
2. Markieren Sie in der Liste die ausgewählte Zeile.
3. Wählen Sie **Benutzer importieren** aus.
4. Wählen Sie **Schließen** aus.

