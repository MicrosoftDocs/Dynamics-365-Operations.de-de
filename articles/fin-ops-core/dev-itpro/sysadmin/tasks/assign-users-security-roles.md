---
title: Benutzern Sicherheitsrollen zuweisen
description: Für den Zugriff auf Finanz- und Betriebs-Apps müssen Benutzern Sicherheitsrollen zugewiesen werden.
author: Peakerbl
ms.date: 02/09/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b5e69a79f123daff3f85d0100647615ad818288e
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103867"
---
# <a name="manage-users-and-security-roles"></a>Benutzer und Sicherheitsrollen verwalten

[!include [banner](../../includes/banner.md)]

Um andere als die allgemeinen Funktionalitäten in den Finanz- und Betriebs-Apps zu verwenden, müssen den Benutzern Sicherheitsrollen zugewiesen werden. Sie können Benutzer Rollen basierend auf Regeln und Geschäftsdaten automatisch zuweisen, Benutzer von der automatischen Rollenzuweisung ausschließen oder Benutzer manuell zu Rollen hinzufügen.

## <a name="automatically-assign-users-to-roles"></a>Weisen Sie Benutzer automatisch Rollen zu
Diese Prozedur zeigt, wie Systemadministratoren Benutzer automatisch zu Rollen zuweisen können, basierend auf Geschäftsdaten. 
1. Wechseln Sie zu **Navigationsbereich > Module > Systemverwaltung > Sicherheit > Benutzer zu Rollen zuweisen**.
2. In der Struktur wählen Sie "Supervisor Buchhaltung" aus. Wählen Sie die Rolle aus, für die Sie die Regel konfigurieren möchten. In diesem Beispiel wählen Sie "Supervisor Buchhaltung" aus. 
3. Wählen Sie **Regel hinzufügen** aus, um das Dialogmenü zu öffnen.
4. In der Liste **Eine Abfrage auswählen** suchen Sie den gewünschten Datensatz und wählen Sie ihn aus. Wählen Sie die Abfrage aus, die für diese Regel zu verwenden ist.  
5. Klicken Sie in der Liste **Mitgliederregelname** auf den Link in der ausgewählten Zeile.
6. Wählen Sie **Abfrage bearbeiten**. Bearbeiten Sie die Abfrage nach Bedarf.  
7. Wählen Sie **OK**.
8. Wählen Sie **Automatische Rollenzuweisung ausführen** aus.
9. Wechseln Sie zu **Navigationsbereich > Module > Systemverwaltung > Benutzer > Benutzer** (idealerweise in einer separaten Browserregisterkarte).
10. Überprüfen Sie die Rollen, die unterschiedlichen Benutzern zugewiesen sind, um zu bestätigen, dass die Rollenzuweisungsabfrage korrekt war. Passen Sie bei Bedarf die Werte an, und führen Sie den Vorgang erneut aus.

## <a name="exclude-users-from-automatic-role-assignment"></a>Schließen Sie Benutzer von der automatischen Rollenzuweisung aus
In diesem Verfahren wird erläutert, wie Sie Benutzer von der automatischen Rollenzuweisung ausschließen.

1. Schließen Sie die Seite.
2. Wechseln Sie zu **Navigationsbereich > Module > Systemverwaltung > Sicherheit > Benutzer zu Rollen zuweisen**.
3. In der Struktur wählen Sie "Supervisor Buchhaltung" aus. Wählen Sie hier eine Rolle aus. Wählen Sie für dieses Beispiel "Supervisor Buchhaltung" aus.  
4. Im Menü **Der Rolle zugewiesene Benutzer** wählen Sie **Benutzer manuell zuweisen/ausschließen** aus.
5. Markieren Sie in der Liste **Benutzer der Rolle zuweisen oder davon ausschließen** die ausgewählte Zeile. Wählen Sie einen Benutzer aus.  
6. Wählen Sie im **Aktivitätsbereich** die Option **Von Rolle ausschließen** aus.
7. Wählen Sie **Von Rolle ausschließen** aus, um die ausgewählten Benutzer von der Rolle auszuschließen. Um Ausschlüsse zu entfernen, wählen Sie die Benutzer aus, für die Sie Ausschlüsse entfernen möchten, und klicken Sie dann auf **Status zurücksetzen**. Wenn Sie einen Ausschluss entfernen, indem Sie den Status des Benutzers zurücksetzen, wird die Rolle des Benutzers automatisch zugewiesen. Allerdings wird der Benutzer nicht sofort der Rolle zugewiesen oder von der Rolle ausgeschlossen, wenn Sie den Status zurücksetzen. Stattdessen wird der Benutzer entweder der Rolle zugewiesen oder von der Rolle entfernt, und zwar das nächste Mal, wenn die Regeln für automatische Rollenzuweisung ausgeführt werden.  

## <a name="manually-assign-users-to-roles"></a>Benutzer manuell Rollen zuweisen
Benutzer, die manuell Sicherheitsrollen zugewiesen werden, müssen auch manuell vom Administrator entfernt werden. Diese Benutzer werden nicht durch Regeln für automatische Rollenzuweisung von Rollen entfernt.

1. Wechseln Sie zu **Navigationsbereich > Module > Systemverwaltung > Sicherheit > Benutzer zu Rollen zuweisen**.
2. In der Struktur wählen Sie eine Rolle aus, und im Menü **Der Rolle zugewiesene Benutzer** wählen Sie **Benutzer manuell zuweisen/ausschließen** aus.
4. Im **Benutzer der Rolle zuweisen oder von der Rolle ausschließen** werden Benutzer, denen die Rolle nicht zugewiesen ist, mit dem **Zuweisungsmodus** auf **Keiner** festgelegt aufgelistet. Wählen Sie einen oder mehrere Benutzer aus, denen die Rolle zugewiesen werden soll.
5. Wählen Sie im **Aktionsbereich** die Option **Der Rolle zuweisen** aus. Der **Zuweisungsmodus** wird aktualisiert auf **Manuell** und den Benutzern wurde jetzt eine neue Rolle zugewiesen.

## <a name="manually-remove-users-from-roles"></a>Benutzer manuell aus Rollen entfernen
Benutzer, die manuell Sicherheitsrollen zugewiesen werden, müssen auch manuell vom Administrator entfernt werden. Diese Benutzer werden nicht durch Regeln für automatische Rollenzuweisung von Rollen entfernt.

1. Wechseln Sie zu **Navigationsbereich > Module > Systemverwaltung > Sicherheit > Benutzer zu Rollen zuweisen**.
2. Gehen Sie folgendermaßen vor, um einen Benutzer zu entfernen:
   1. Wählen Sie in der Struktur eine Rolle aus. 
   2. Wählen Sie im Bereich **Der Rolle zugewiesene Benutzer** den Benutzer aus, der entfernt werden soll.
   3. Wählen Sie **Entfernen** und der Benutzer wird aus der Rolle entfernt.
3. Gehen Sie folgendermaßen vor, um mehrere Benutzer zu entfernen:
   1. Wählen Sie in der Struktur eine Rolle aus. 
   2. Wählen Sie im Bereich **Der Rolle zugewiesene Benutzer** **Benutzer manuell zuweisen/ausschließen** aus.
   3. Auf der Seite **Benutzer der Rolle zuweisen oder von der Rolle ausschließen** wird bei Benutzern, denen die Rolle nicht zugewiesen wurde, **Keine** in der Spalte **Zuweisungsmodus** angezeigt. Wählen Sie die Benutzer aus, die von der Rolle ausgeschlossen werden sollen.
   4. Wählen Sie im **Aktivitätsbereich** die Option **Von Rolle ausschließen** aus. Die Spalte **Zuweisungsmodus** ist jetzt auf **Manuell** aktualisiert und die Benutzern sind jetzt von der Rolle ausgeschlossen.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

