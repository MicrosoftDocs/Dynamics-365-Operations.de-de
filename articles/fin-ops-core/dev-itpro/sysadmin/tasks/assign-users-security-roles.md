---
title: Zuweisen von Benutzern zu Sicherheitsrollen
description: Für den Zugriff auf Finance and Operations müssen Benutzer Sicherheitsrollen zugewiesen werden.
author: Peakerbl
ms.date: 05/06/2020
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
ms.openlocfilehash: bb4b143400a1f092c8f7a15bbb047eda52a4a4d8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745884"
---
# <a name="assign-users-to-security-roles"></a>Zuweisen von Benutzern zu Sicherheitsrollen

[!include [banner](../../includes/banner.md)]

Um etwas außerhalb der allgemeinen Funktionen in Finance and Operations-Apps verwenden zu können, müssen Benutzern Sicherheitsrollen zugewiesen werden. Sie können Benutzer Rollen basierend auf Regeln und Geschäftsdaten automatisch zuweisen, Benutzer von der automatischen Rollenzuweisung ausschließen oder Benutzer manuell zu Rollen hinzufügen.

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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]