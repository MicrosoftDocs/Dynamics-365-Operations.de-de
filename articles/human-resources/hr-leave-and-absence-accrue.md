---
title: Urlaubs- und Abwesenheitspläne antizipieren
description: Sie können Urlaub und Abwesenheit in Dynamics 365 Human Resources für mehrere Mitarbeiter oder für eine Einzelperson abgrenzen.
author: twheeloc
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 886cfa2a901150e720e60709104afaf3863486a9
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686002"
---
# <a name="accrue-leave-and-absence-plans"></a>Urlaubs- und Abwesenheitspläne antizipieren

>[!Important]
>Die in diesem Thema beschriebene Funktionalität ist derzeit für Kunden der eigenständigen Version von Dynamics 365 Human Resources verfügbar. Einige oder die gesamten Funktionen werden in einem zukünftigen Release der Finance-Infrastruktur nach Finance-Version 10.0.26 verfügbar sein.


[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Sie können Urlaub und Abwesenheit in Dynamics 365 Human Resources für mehrere Mitarbeiter oder für eine Einzelperson abgrenzen.

## <a name="accrue-leave-and-absence-for-multiple-employees"></a>Abwesenheit und Urlaub für mehrere Mitarbeiter erfassen

1. Auf der Seite **Urlaub- und Abwesenheit** klicken Sie auf die Registerkarte **Links**.

2. Unter **Urlaub verwalten**, wählen Sie **Urlaubs- und Abwesenheitspläne aufbauen**.

3. Das Dialogfeld **Urlaubs- und Abwesenheitspläne** wird angezeigt. Unter **Aufgelaufen ab** wählen Sie entweder **Heutiges Datum** oder wählen Sie **Benutzerdefiniertes Datum** und geben Sie ein benutzerdefiniertes Datum ein.

4. Wenn Sie Rückstellungen für alle Unternehmen erstellen möchten, wählen Sie **Alle Unternehmen** aus. Wenn Sie Rückstellungen für einen einzelnen Urlaubsplan bearbeiten möchten, wählen Sie **Nein** für **Alle Pläne** aus, und dann wählen Sie **Urlaubsplan** aus. Wenn Sie alle Unternehmen auswählen, können Sie keinen einzelnen Urlaubsplan auswählen.

5. Wenn Sie den Erfassungsprozess im Hintergrund ausführen möchten, wählen Sie **Im Hintergrund ausführen** und führen Sie die folgenden Aufgaben aus:

    1. Geben Sie Informationen für den Erfassungsprozess ein.
    2. Um eine wiederkehrende Stelle einzurichten, wählen Sie **Wiederholung**, geben Sie dann die Wiederholungsinformationen ein und wählen Sie **OK**.
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

## <a name="leave-accrual-rounding"></a>Rundung für Urlaubsabgrenzungen
Wenn ein Mitarbeiter an- oder abgemeldet ist, wird die Rundung für Urlaubsabgrenzungen anteilig berechnet. Bisher war das Runden nur zulässig, wenn ein Urlaubsplan auf anteilig eingestellt war und ein Mitarbeiter in der Mitte des Zeitraums an-/abgemeldet wurde. Urlaubsabgrenzungen werden jetzt unabhängig von der Anmeldung/Abmeldung in der Mitte des Zeitraums oder zu Beginn eines Zeitraums gerundet.

## <a name="leave-accrual-transaction-auditing"></a>Überwachung von Urlaubsabgrenzungstransaktionen

Diese Funktion hilft den Managern von Urlaub und Abwesenheit, die Transaktionen zur Abgrenzung von Urlaub und Abwesenheit zu verstehen, die mit den Zeitsalden eines Mitarbeiters für eine bestimmte Urlaubsart zusammenhängen.

Zum Anzeigen von Transaktionsdetails:

1. Wählen Sie im Datensatz des Mitarbeiters **Abweseneheit** aus.

2. Wählen Sie **Freizeit anzeigen** und wählen Sie dann die Registerkarte **Saldo**.

Wählen Sie den numerischen Wert im Feld aus, um die Abgrenzungstransaktionen anzuzeigen, die sich auf einen bestimmten Urlaubstyp beziehen in der Spalte **Aktueller Saldo**.

Um die Transaktionsdetails für einen bestimmten Abgrenzungsbetrag anzuzeigen, wählen Sie eine Abgrenzungszeile aus und öffnen Sie den Bereich **Verwandte Informationen** auf der rechten Seite, und öffnen Sie dann den Bereich **Transaktionsdetails**. Der Abschnitt Transaktionsdetails wird angezeigt:

- Änderungen des Urlaubstypsaldos des Mitarbeiters
- Beschäftigungsdetails für den angegebenen Abgrenzungszeitraum
- Details zum Abgrenzungszeitraum und zu den Sätzen
- Alle Änderungen, die vorgenommen wurden, um die Plan-Konfigurationen zu verlassen

![Zeigt die Überwachung von Urlaubsabgrenzungstransaktionen an.](media/hr-leave-and-absence-accrue-audit.png)

## <a name="see-also"></a>Siehe auch

[Urlaubs- und Abwesenheitsübersicht](hr-leave-and-absence-overview.md)</br>
[Einen Urlaubs- und Abwesenheitsplan erstellen](hr-leave-and-absence-plans.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
