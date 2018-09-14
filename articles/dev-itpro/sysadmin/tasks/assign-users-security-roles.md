--- 
title: Weisen Sie Benutzer zu Sicherheitsrollen zu
description: Wenn Sie auf Microsoft Dynamics 365 for Finance and Operations, Enterprise edition zugreifen, muss der Benutzer einer Sicherheitsrollen zugewiesen werden.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 551048af26f46d334c562d1968963aed262a5e03
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="assign-users-to-security-roles"></a>Weisen Sie Benutzer zu Sicherheitsrollen zu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Wenn Sie auf Microsoft Dynamics 365 for Finance and Operations, Enterprise edition zugreifen, muss der Benutzer einer Sicherheitsrollen zugewiesen werden. Diese Prozedur zeigt, wie Systemadministratoren Benutzer automatisch zu Rollen zuweisen können, basierend auf Geschäftsdaten. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.


## <a name="automatically-assign-users-to-roles"></a>Weisen Sie Benutzer automatisch Rollen zu
1. Wechseln Sie zu "Systemverwaltung"  "Sicherheit"  "Benutzer zu Rollen zuweisen".
2. In der Struktur wählen Sie "Supervisor Buchhaltung" aus.
    * Wählen Sie die Rolle aus, für die Sie die Regel konfigurieren möchten. In diesem Beispiel wählen Sie "Supervisor Buchhaltung" aus.  
3. Klicken Sie auf "Regel hinzufügen", um das Ablagedialogfeld zu öffnen.
4. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wählen Sie die Abfrage aus, die für diese Regel zu verwenden ist.  
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
6. (Zum Bearbeiten klicken)
    * Bearbeiten Sie die Abfrage nach Bedarf.  
7. Klicken Sie auf "OK".

## <a name="exclude-users-from-automatic-role-assignment"></a>Schließen Sie Benutzer von der automatischen Rollenzuweisung aus
1. Schließen Sie die Seite.
2. Wechseln Sie zu "Systemverwaltung"  "Sicherheit"  "Benutzer zu Rollen zuweisen".
3. In der Struktur wählen Sie "Supervisor Buchhaltung" aus.
    * Wählen Sie hier eine Rolle aus. Wählen Sie für dieses Beispiel "Supervisor Buchhaltung" aus.  
4. Klicken Sie auf "Benutzer manuell zuweisen/ausschließen".
5. Markieren Sie in der Liste die ausgewählte Zeile.
    * Wählen Sie einen Benutzer aus.  
6. Klicken Sie auf "Von Rolle ausschließen".
    * Klicken Sie auf "Von Rolle ausschließen", um die ausgewählten Benutzer von der Rolle auszuschließen. Um Ausschlüsse zu entfernen, wählen Sie die Benutzer aus, für die Sie Ausschlüsse entfernen möchten, und klicken Sie dann auf "Status zurücksetzen". Wenn Sie einen Ausschluss entfernen, indem Sie den Status des Benutzers zurücksetzen, wird die Rolle des Benutzers erneut automatisch zugewiesen. Allerdings wird der Benutzer nicht sofort der Rolle zugewiesen oder von der Rolle ausgeschlossen, wenn Sie den Status zurücksetzen. Stattdessen wird der Benutzer entweder der Rolle zugewiesen oder von der Rolle entfernt, und zwar das nächste Mal, wenn die Regeln für automatische Rollenzuweisung ausgeführt werden.  


