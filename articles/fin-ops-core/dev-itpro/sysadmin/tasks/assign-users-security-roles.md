---
title: Zuweisen von Benutzern zu Sicherheitsrollen
description: Um auf Finance and Operations-Apps zuzugreifen, müssen Benutzer Sicherheitsrollen zugewiesen werden.
author: ChrisGarty
manager: AnnBe
ms.date: 09/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4daecc1acd589cd1656402244e5325382a407e7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180966"
---
# <a name="assign-users-to-security-roles"></a>Zuweisen von Benutzern zu Sicherheitsrollen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Um etwas außerhalb der allgemeinen Funktionen verwenden zu können, müssen Benutzern Sicherheitsrollen zugewiesen werden. Diese Prozedur zeigt, wie Systemadministratoren Benutzer automatisch zu Rollen zuweisen können, basierend auf Geschäftsdaten. 

## <a name="automatically-assign-users-to-roles"></a>Weisen Sie Benutzer automatisch Rollen zu
1. Wechseln Sie zu **Navigationsbereich > Module > Systemverwaltung > Sicherheit > Benutzer zu Rollen zuweisen**.
2. In der Struktur wählen Sie "Supervisor Buchhaltung" aus. Wählen Sie die Rolle aus, für die Sie die Regel konfigurieren möchten. In diesem Beispiel wählen Sie "Supervisor Buchhaltung" aus. 
3. Klicken Sie auf **Regel hinzufügen**, um das Ablagedialogfeld zu öffnen.
4. In der Liste **Eine Abfrage auswählen** den gewünschten Datensatz suchen und auswählen. Wählen Sie die Abfrage aus, die für diese Regel zu verwenden ist.  
5. Klicken Sie in der Liste **Mitgliederregelname** auf den Link in der ausgewählten Zeile.
6. Klicken Sie auf **Abtrage bearbeiten**. Bearbeiten Sie die Abfrage nach Bedarf.  
7. Klicken Sie auf **OK**.

## <a name="exclude-users-from-automatic-role-assignment"></a>Schließen Sie Benutzer von der automatischen Rollenzuweisung aus
1. Schließen Sie die Seite.
2. Wechseln Sie zu **Navigationsbereich > Module > Systemverwaltung > Sicherheit > Benutzer zu Rollen zuweisen**.
3. In der Struktur wählen Sie "Supervisor Buchhaltung" aus. Wählen Sie hier eine Rolle aus. Wählen Sie für dieses Beispiel "Supervisor Buchhaltung" aus.  
4. Im Menü **Der Rolle zugewiesene Benutzer** wählen Sie **Benutzer manuell zuweisen/ausschließen** aus.
5. Markieren Sie in der Liste **Benutzer der Rolle zuweisen oder davon ausschließen** die ausgewählte Zeile. Wählen Sie einen Benutzer aus.  
6. Wählen Sie im **Aktivitätsbereich** die Option **Von Rolle ausschließen** aus.
    
    Klicken Sie auf **Von Rolle ausschließen**, um die ausgewählten Benutzer von der Rolle auszuschließen. Um Ausschlüsse zu entfernen, wählen Sie die Benutzer aus, für die Sie Ausschlüsse entfernen möchten, und klicken Sie dann auf **Status zurücksetzen**. Wenn Sie einen Ausschluss entfernen, indem Sie den Status des Benutzers zurücksetzen, wird die Rolle des Benutzers erneut automatisch zugewiesen. Allerdings wird der Benutzer nicht sofort der Rolle zugewiesen oder von der Rolle ausgeschlossen, wenn Sie den Status zurücksetzen. Stattdessen wird der Benutzer entweder der Rolle zugewiesen oder von der Rolle entfernt, und zwar das nächste Mal, wenn die Regeln für automatische Rollenzuweisung ausgeführt werden.  