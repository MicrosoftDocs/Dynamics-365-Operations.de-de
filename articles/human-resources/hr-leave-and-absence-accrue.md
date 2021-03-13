---
title: Urlaubs- und Abwesenheitspläne antizipieren
description: Sie können Urlaub und Abwesenheit in Dynamics 365 Human Resources für mehrere Mitarbeiter oder für eine Einzelperson abgrenzen.
author: andreabichsel
manager: tfehr
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: aed36a38c5d50767b5ac14ae82ca424f0c835ae0
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "5116091"
---
# <a name="accrue-leave-and-absence-plans"></a>Urlaubs- und Abwesenheitspläne antizipieren

Sie können Urlaub und Abwesenheit in Dynamics 365 Human Resources für mehrere Mitarbeiter oder für eine Einzelperson abgrenzen.

## <a name="accrue-leave-and-absence-for-multiple-employees"></a>Abwesenheit und Urlaub für mehrere Mitarbeiter erfassen

1. Auf der Seite **Urlaub- und Abwesenheit** klicken Sie auf die Registerkarte **Links**.

2. Unter **Urlaub verwalten**, wählen Sie **Urlaubs- und Abwesenheitspläne aufbauen**.

3. Das Dialogfeld **Urlaubs- und Abwesenheitspläne** wird angezeigt. Unter **Aufgelaufen ab** wählen Sie entweder **Heutiges Datum** oder wählen Sie **Benutzerdefiniertes Datum** und geben Sie ein benutzerdefiniertes Datum ein.

4. Wenn Sie Rückstellungen für alle Unternehmen erstellen möchten, wählen Sie **Alle Unternehmen** aus. Wenn Sie Rückstellungen für einen einzelnen Urlaubsplan bearbeiten möchten, wählen Sie **Nein** für **Alle Pläne** aus, und dann wählen Sie **Urlaubsplan** aus. Wenn Sie alle Unternehmen auswählen, können Sie keinen einzelnen Urlaubsplan auswählen. 

5. Wenn Sie den Erfassungsprozess im Hintergrund ausführen möchten, wählen Sie **Im Hintergrund ausführen** und führen Sie die folgenden Aufgaben aus:

   1. Geben Sie Informationen für den Erfassungsprozess ein.

   2. Um eine wiederkehrende Stelle einzurichten, wählen Sie **Wiederholung**, geben Sie die Wiederholungsinformationen ein und wählen Sie **OK**.

   3. Um eine Stellenbenachrichtigung einzurichten, wählen Sie **Benachrichtigungen**, wählen Sie die zu empfangenden Benachrichtigungen und wählen Sie dann **OK**.

   4. Wählen Sie **OK**. Der Erfassungsprozess wird mit den von Ihnen festgelegten Parametern ausgeführt.

## <a name="accrue-leave-and-absence-for-an-employee"></a>Abwesenheit und Urlaub für einen Mitarbeiter antizipieren

1. Wählen Sie im Datensatz des Mitarbeiters **Abweseneheit** aus.

2. **Urlaubs- und Abwesenheitspläne antizipieren** auswählen.

3. Das Dialogfeld **Urlaubs- und Abwesenheitspläne** wird angezeigt. Unter **Aufgelaufen ab** wählen Sie entweder **Heutiges Datum** oder wählen Sie **Benutzerdefiniertes Datum** und geben Sie ein benutzerdefiniertes Datum ein.

4. Wenn Sie Rückstellungen für alle Unternehmen erstellen möchten, wählen Sie **Alle Unternehmen** aus. Wenn Sie Rückstellungen für einen einzelnen Urlaubsplan bearbeiten möchten, wählen Sie **Nein** für **Alle Pläne** aus, und dann wählen Sie **Urlaubsplan** aus. Wenn Sie alle Unternehmen auswählen, können Sie keinen einzelnen Urlaubsplan auswählen. 

5. Wenn Sie den Erfassungsprozess im Hintergrund ausführen möchten, wählen Sie **Im Hintergrund ausführen** und führen Sie die folgenden Aufgaben aus:

   1. Geben Sie Informationen für den Erfassungsprozess ein.

   2. Um eine wiederkehrende Stelle einzurichten, wählen Sie **Wiederholung**, geben Sie die Wiederholungsinformationen ein und wählen Sie **OK**.

   3. Um eine Stellenbenachrichtigung einzurichten, wählen Sie **Benachrichtigungen**, wählen Sie die zu empfangenden Benachrichtigungen und wählen Sie dann **OK**.

   4. Wählen Sie **OK**. Der Erfassungsprozess wird mit den von Ihnen festgelegten Parametern ausgeführt.

## <a name="delete-leave-and-absence-accruals-for-multiple-employees"></a>Aufgelaufene Abwesenheit und Urlaub für mehrere Mitarbeiter löschen

Löschen Sie Abgrenzungssätze für einen bestimmten Plan und Zeitraum. Abgrenzungsdaten müssen heute oder in der Zukunft datiert werden.

1. Auf der Seite **Urlaub- und Abwesenheit** klicken Sie auf die Registerkarte **Links**.

2. Unter **Urlaub verwalten**, wählen Sie **Aufgelaufene Urlaubs- und Abwesenheitspläne löschen**.

3. Im Dialogfeld **Aufgelaufene Urlaubs- und Abwesenheitspläne löschen** wählen Sie **Plan verlassen**. 

4. Falls zutreffend, wählen Sie **Saldo-Anpassungen löschen**.

5. Geben Sie ein oder wählen Sie **Datum Urlaub aussetzen**. Dieses Datum muss entweder heute oder in der Zukunft liegen. 

6. Wählen Sie **OK**. Der Erfassungsprozess löscht Abgrenzungen mit den von Ihnen festgelegten Parametern. 

## <a name="delete-leave-and-absence-accruals-for-a-single-employee"></a>Aufgelaufene Abwesenheit und Urlaub für einzelne Mitarbeiter löschen

1. Wählen Sie im Datensatz des Mitarbeiters **Abweseneheit** aus.

2. **Aufgelaufene Urlaubs- und Abwesenheitspläne löschen** auswählen.

3. Im Dialogfeld **Aufgelaufene Urlaubs- und Abwesenheitspläne löschen** wählen Sie **Plan verlassen**. 

4. Falls zutreffend, wählen Sie **Saldo-Anpassungen löschen**.

5. Geben Sie ein oder wählen Sie **Datum Urlaub aussetzen**. Das Datum muss entweder heute oder in der Zukunft liegen. 

6. Wählen Sie **OK**. Der Erfassungsprozess löscht Abgrenzungen mit den von Ihnen festgelegten Parametern. 

## <a name="review-leave-accrual-and-deletion-processes"></a>Überprüfen Sie die Abgrenzungs- und Löschprozesse

**Rückstellungsprüfung verlassen** zeigt jedes Mal an, wenn Sie eine Rückstellung für einen oder alle Mitarbeiter ausführen oder löschen. Das Datum und die Person, die die Aktion ausgeführt hat, werden ebenfalls angezeigt.

1. Auf der Seite **Urlaub- und Abwesenheit** klicken Sie auf die Registerkarte **Links**.

2. Unter **Urlaub verwalten**, wählen Sie **Aufgelaufene Urlaubs- und Abwesenheitsprüfung löschen**.

## <a name="see-also"></a>Siehe auch

[Urlaubs- und Abwesenheitsübersicht](hr-leave-and-absence-overview.md)</br>
[Einen Urlaubs- und Abwesenheitsplan erstellen](hr-leave-and-absence-plans.md)
