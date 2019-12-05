---
title: Erstellen und versenden eines Onboarding-Leitfadens mithilfe von Dynamics 365 Talent - Onboard
description: In diesem Thema wird erläutert, wie die Microsoft Dynamics 365 Talent - Onboard-App eine Vorlage für ein Onboarding-Handbuch für Ihre Neueinstellungen erstellt. Diese Aufgabe ist ein erster Schritt in einer Human Capital Management (HCM)-Einstellungsstrategie.
author: andreabichsel
manager: ''
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a095fe97b05898403b501763204a462ee8dcc12a
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814627"
---
# <a name="create-and-send-an-onboarding-guide-by-using-dynamics-365-talent---onboard"></a>Erstellen und versenden eines Onboarding-Leitfadens mithilfe von Dynamics 365 Talent - Onboard

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Talent: Onboard lässt Sie Onboarding Anleitungen von Vorlagen erstellen, die Sie selbst erstellt haben, von Vorlagen, die in einem Katalog verfügbar ist, oder von Grund auf neu.

Nachdem Sie ein Onboarding Handbuch erstellt haben, können Sie diese an einen neuen Mitarbeiter senden. Alternativ können Sie es an mehrere neue Mitarbeiter senden, die Sie in einer Microsoft Excel Datei angeben, die Sie von der Onboard-App herunterladen.

## <a name="create-an-onboarding-guide-from-a-template-and-send-it-to-a-single-new-hire"></a>Erstellen Sie ein Onboarding Handbuch aus einer Vorlage und senden Sie dieses an einen einzelnen neuen Mitarbeiter

1. Wählen Sie im linken Menü **Vorlagen** aus.
2. Wählen Sie unter **Meine Vorlagen** die Vorlage aus, die Sie als Onboarding Handbuch für die neuen Mitarbeiter einrichten möchten.
3. Bearbeiten Sie die Vorlage, wie Sie es wünschen. Denken Sie daran, Ihre Arbeit regelmäßig zu speichern.
4. Klicken Sie abschließend auf die Vorlage und wählen Sie **Anleitung erstellen**.

    [![Erstellen des Onboarding-Leitfadens anhand der Vorlage](./media/onboard-create-guide.png)](./media/onboard-create-guide.png)

5. Im Fenster **Erstellen Sie Anleitungen** unter **für wen ist das Onboarding**, geben Sie den Namen oder die neue E-Mail-Adresse des neuen Mitarbeiters ein. Wenn der neue Mitarbeiter noch nicht im System ist, wählen Sie **Jetzt hinzufügen**, und geben Sie die Informationen des Mitarbeiters ein.

    ![[Informationen für das Onboarding-Handbuch](./media/onboard-create-a-guide-window.png)](./media/onboard-create-a-guide-window.png)

6. Wählen Sie unter **Wann beginnen sie** ein Startdatum aus.
7. Wenn das Onboarding Handbuch automatisch an einen neuen Mitarbeiter zu einem bestimmten Zeitpunkt gesendet wird, stellen Sie sicher, dass die Option **Planen Sie ein automatisches Sendedatum** aktiviert ist, und wählen Sie dann das automatische Sendedatum aus. Um die Anleitung sofort zu senden, deaktivieren Sie die Option **Ein automatisches Sendedatum planen** aus.
8. Wählen Sie **Fertig**.
9. Wenn Sie fertig sind, das Onboarding Handbuch zu bearbeiten, wählen Sie in der rechten Ecke **Senden**. Folgen Sie dann diesen Schritten:

    - Um dem neuen Mitarbeiter einen Link zum Onboarding Handbuch zu senden, und wählen Sie **kopieren Sie einen Link** und dann **Kopieren** aus.
    - Um die E-Mail für das Onboarding Handbuch anzupassen bevor Sie es senden, wählen Sie **Passen Sie die E-Mail an, bevor Sie übermitteln**, wählen Sie **Weiter**, um die E-Mail, die Sie anpassen möchten und wählen Sie **Senden** aus.
    - Um die E-Mail ohne Anpassung zu senden, wählen Sie **Weiter** und dann **Senden** aus.

## <a name="create-an-onboarding-guide-from-a-template-and-send-it-to-multiple-new-hires"></a>Erstellen Sie ein Onboarding Handbuch aus einer Vorlage und senden Sie dieses an mehrere neue Mitarbeiter

Mit Onboard können Sie ein Onboarding Handbuch zu mehreren Neueinstellungen gleichzeitig senden.

1. Wählen Sie im linken Menü **Vorlagen** aus.
2. Wählen Sie unter **Meine Vorlagen** die Vorlage aus, die Sie als Onboarding Handbuch für die neuen Mitarbeiter einrichten möchten.
3. Bearbeiten Sie die Vorlage, wie Sie es wünschen. Denken Sie daran, Ihre Arbeit regelmäßig zu speichern.
4. Klicken Sie abschließend auf die Vorlage und wählen Sie **Anleitung erstellen**.
5. Im Fenster **Erstellen einer Anleitung** wählen Sie **Mehre Personen auf einmal onboarden**.

    [![Erstellen eines Onboarding Handbuchs für mehre neue Mitarbeiter](./media/onboard-send-guide-multiple-people.png)](./media/onboard-send-guide-multiple-people.png)

6. Wählen Sie **neue Einstellungsvorlage** aus.
7. Nachdem die .XLSX-Datei heruntergeladen wurde, wählen Sie **Öffnen** aus, geben Sie die Informationen zu den Mitarbeiter in der Excel-Arbeitsmappe ein, und speichern Sie die Arbeitsmappe.

    [![Die Excel-Vorlage zum Senden der Onboarding-Anleitung an mehrere Neueinstellungen herunterladen](./media/onboard-send-guide-download-spreadsheet.png)](./media/onboard-send-guide-download-spreadsheet.png)

    > [!NOTE]
    > Damit Sie die Arbeitsmappe bearbeiten können, müssen Sie **Aktivieren der Bearbeitung** in Excel auswählen.
    > 
    > [![Bearbeitung aktivieren](./media/onboard-send-guide-enable-editing.png)](./media/onboard-send-guide-enable-editing.png)

8. Ziehen Sie die Excel-Arbeitsmappe in den ausgewählten Bereich im Fenster **Erstellen Sie mehrere Anleitungen**, oder klicken Sie an beliebiger Stelle in diesem Bereich, um die Datei auf dem Computer zu suchen.

    [![Ziehen der bearbeiteten Arbeitsmappe](./media/onboard-send-guide-drag-spreadsheet.png)](./media/onboard-send-guide-drag-spreadsheet.png)

9. Wenn Sie fertig sind, das Onboarding Handbuch zu bearbeiten, wählen Sie in der rechten Ecke **Senden**. Folgen Sie dann diesen Schritten:

    - Um den neuen Mitarbeiter einen Link zum Onboarding Handbuch zu senden, wählen Sie **kopieren Sie einen Link** und dann **Kopieren** aus.
    - Um die E-Mail für das Onboarding Handbuch anzupassen bevor Sie es senden, wählen Sie **Passen Sie die E-Mail an, bevor Sie übermitteln**, wählen Sie **Weiter**, um die E-Mail, die Sie anpassen möchten und wählen Sie **Senden** aus.
    - Um die E-Mail ohne Anpassung zu senden, wählen Sie **Weiter** und dann **Senden** aus.

## <a name="create-a-guide-without-using-a-template"></a>Anleitung ohne Vorlage erstellen

Sie müssen nicht immer Anleitungen aus einer Vorlage erstellen. Wenn Sie es bevorzugen, können Sie Anleitungen von Grund auf neu erstellen.

1. Wählen Sie im linken Menü **Anleitungen** und dann **Hinzufügen** aus der Schaltfläche (das Pluszeichen \[**+**\]).
2. Im Fenster **Erstellen Sie Anleitungen** unter **für wen ist das Onboarding**, geben Sie den Namen oder die neue E-Mail-Adresse des neuen Mitarbeiters ein. Wenn der neue Mitarbeiter noch nicht im System ist, wählen Sie **Jetzt hinzufügen**, und geben Sie die Informationen des Mitarbeiters ein.

    ![[Informationen für das Onboarding-Handbuch](./media/onboard-create-a-guide-window.png)](./media/onboard-create-a-guide-window.png)

3. Wählen Sie unter **Wann beginnen sie** ein Startdatum aus.
4. Wenn das Onboarding Handbuch automatisch an einen neuen Mitarbeiter zu einem bestimmten Zeitpunkt gesendet wird, stellen Sie sicher, dass die Option **Planen Sie ein automatisches Sendedatum** aktiviert ist, und wählen Sie dann das automatische Sendedatum aus. Um die Anleitung sofort zu senden, deaktivieren Sie die Option **Ein automatisches Sendedatum planen** aus.
5. Wählen Sie **Fertig**.

## <a name="save-a-guide-as-a-template"></a>Speichert Anleitungen als Vorlage.

Sie können eine Onboarding Anleitung als Vorlage speichern. Dadurch können Sie Zeit sparen, wenn Sie weitere Onboarding Anleitungen später erstellen müssen.

1. Wählen Sie im linken Menü **Anleitungen** aus.
2. Wählen Sie die Schaltfläche**Weiter** aus (die Auslassungspunkte \[**...**\]) für die Anleitung, von er Sie die Vorlage erstellen möchten und wählen Sie dann die aktuelle Vorlage **Als Vorlage speichern** aus.

    ![[Ein Onboarding Handbuch wird als Vorlage gespeichert](./media/onboard-save-guide-as-template.png)](./media/onboard-save-guide-as-template.png)

3. Im Fenster **Speichern als neue Vorlage** geben Sie einen Namen für die neue Vorlage ein, und wählen Sie dann **Speichern** aus.

## <a name="next-steps"></a>Nächste Schritte

- [Bearbeiten von Onboarding Anleitungen und Vorlagen](./onboard-edit-guides-templates.md)
- [Hier können Sie Inhalte mit anderen Personen teilen](./onboard-share-template.md)
- [Anzeigen des Status von Aufgaben und dem Onboarding von Mitarbeitern](./onboard-view-status.md)
- [Erstellen von Einstellungsteams in Onboard](./onboard-create-team.md)

### <a name="see-also"></a>Siehe auch

- [Testen oder kaufen Sie die Onbaord-App](https://dynamics.microsoft.com/talent/onboard/)
- [Was ist neu oder geändert in Dynamics 365 Talent](./whats-new.md)
- [Release-Pläne](https://docs.microsoft.com/business-applications-release-notes/index)
- [Sie erhalten Unterstützung für Microsoft Dynamics 365 Talent](./talent-support.md)
