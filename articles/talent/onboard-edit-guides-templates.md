---
title: Bearbeiten von Onboarding-Anleitungen und Vorlagen in Dynamics 365 Talent - Onboard
description: In diesem Thema wird erläutert, wie die Aktivitäten und anderen Informationen Onboarding Anleitungen und Vorlagen in Microsoft Dynamics 365 Talent - Onboard hinzugefügt werden.
author: andreabichsel
manager: ''
ms.date: 06/19/2019
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
ms.search.validFrom: 2019-06-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 291f7aefac61c26dfab81cfff28c1c6580d46de5
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897119"
---
# <a name="edit-onboarding-guides-and-templates"></a>Bearbeiten von Onboarding Anleitungen und Vorlagen

[!include [banner](includes/banner.md)]

Nachdem Sie ein Onboarding Anleitung oder eine Vorlage erstellt haben in Microsoft Dynamics 365 Talent: Onboard, müssen Sie eine Einleitung, Aktivitäten, Kontakte und Ressourcen hinzufügen. Mit Onboard können Sie umfangreiche Inhalte der Onboarding-Anleitung hinzufügen, inklusive:

- YouTube Videos
- Microsoft Sway Präsentationen
- Microsoft PowerApps Apps
- Microsoft Stream Videos
- Microsoft Forms Formulare
- Iframes, das den Webinhalt enthält

## <a name="edit-introductions-or-activities-imported-from-a-template"></a>Bearbeiten Sie die Einführungen oder Aktivitäten, die anhand einer Vorlage importiert werden

Wenn Sie ein Onboarding Handbuch aus einer Vorlage erstellen oder wenn Sie Aktivitäten aus einer Vorlage in andere importieren, sehen Sie eine Schaltfläche **Sperren** für die importierten Aktivitäten. Diese werden *verwaltete Aktivitäten* genannt.

[![Verwaltete Aktivitäten](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)

Wenn Sie eine verwaltete Aktivität auswählen, können Sie die Quellvorlage oben an der Aktivität anzeigen.

[![Verwaltete Aktivitätsquelle](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)

Wenn Sie eine Aktivität in einer Vorlage bearbeiten, überträgt Onboard die Änderungen per Push auf alle Anleitungen, Vorlagen und ungesendeten Anleitungen, die auf dieser Vorlage basieren. Wenn Sie ein ungesendetes Handbuch auf Basis einer Vorlage auswählen, die Sie bearbeitet haben und dann die Registerkarte  **Aktivitäten** im Handbuch auswählen, lesen Sie einen Hinweis, dass die Anleitung geändert hat. Wenn Sie die Benachrichtigung ablehnen, wählen Sie **OK** aus. 

[![Benachrichtigung ändern](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)

Sie finden einen schwarzen Fleck neben den aktualisierten Aktivitäten.

[![Aktivität geändert](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)

Sie können Aktivitäten nicht außerhalb der ursprünglichen Vorlage verwalten mit Ausnahme der nicht bearbeiten, um eine zugewiesener Person, Fälligkeitsdatum oder andere Informationen im rechten Bereich der Aktivität hinzuzufügen.

Wenn Sie eine verwaltete Aktivität bearbeiten möchten oder wenn Sie keine Aktivität von Aktualisierungen der Vorlage erhalten möchten, wählen Sie die Schaltfläche **Sperren** für diese Aktivität. Die Schaltfläche **Sperren** wird nicht mehr angezeigt. Die Aktivität wird nicht mehr von der ursprüngliche Vorlage verwaltet und erhält keine weiteren Aktualisierungen aus der Vorlage. Aktualisierungen, die für eine Aktivität vornehmen, haben keinen Einfluss auf die ursprüngliche Vorlage.

Wenn Sie eine Aktivität von einer Anleitung löschen und Änderungen aus der Vorlage dieser Anleitung puschen, bleibt die Aktivität gelöscht in der Anleitung.

> [!NOTE]
> Kontakte und Ressourcen werden nicht von Vorlagen verwaltet. Darüber hinaus werden Abschnitte nicht verwaltet, wenn Sie einen Abschnitt in einer Vorlage hinzufügen oder bearbeiten, werden die Änderungen nicht auf Anleitungen oder Vorlagen gepusht,  die auf dieser Vorlage basieren.
> 
> Wenn Sie neue Aktivitäten einer Vorlage hinzufügen, werden die neuen Aktivitäten auf die Anleitungen und Vorlagen basierende auf dieser Vorlage gepusht und neue Aktivitäten werden oben angezeigt.

## <a name="import-activities-from-another-template"></a>Importieren von Aktivitäten aus einer anderen Vorlage

Sie können Aktivitäten aus einer oder mehrerer Vorlagen in eine Anleitung oder Vorlage importieren.

1. Wählen Sie die Anleitung oder Vorlage, die Sie bearbeiten möchten.

2. Wählen Sie die Registerkarte **Aktivitäten** aus.

3. Wählen Sie die Registerkarte **Importieren** im Abschnitt auf der rechten Seite.

   [![Importieren Sie Aktivitäten](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)

4. Um die Aufgaben im Vergleich zur Registerkarte in Ihrem Browser in der Vorschau anzuzeigen, wählen Sie die Schaltfläche **Öffnen in neuer Registerkarte** auf einer beliebigen Vorlage aus.

   [![Importieren Sie Aktivitäten](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)

5. Drag & Drop der gewünschten Vorlage an den Ort in der Anleitungsvorlage, in dem die Aktivitäten angezeigt werden sollen. Setzt das Bearbeiten der Anleitung oder der Vorlage fort.

Die importierten Aktivitäten beinhalten eine Schaltfläche **Sperren**, die anzeigt, dass diese Aktivitäten verwaltet werden von der Vorlage, aus er Sie importiert haben. Wenn Sie Änderungen vornehmen an der Vorlage, die Sie importiert haben, werden diese Aktivitäten in der Vorlage aktualisiert, in die Sie importiert haben. Allerdings werden die Änderungen nicht automatisch zu einer beliebigen Anleitung gepusht aus der Vorlage erstellt haben, in die Sie importiert haben.

## <a name="push-changes-from-a-template-to-other-templates-or-guides"></a>Push ändert sich von einer Vorlage in eine andere Vorlage oder eine Anleitung

Wenn sie eine Vorlage bearbeiten, die Aktivitäten enthält, die in anderen Vorlagen oder in Anleitungen verwendet werden, müssen die Änderungen gepusht werden. wenn diese in anderen Vorlagen oder in den Anleitungen angezeigt werden sollen.

Wenn Sie nicht sicher sind, ob die Aktivitäten der Vorlage in anderen Vorlagen oder in Anleitungen verwendet werden, wählen Sie die Registerkarte **Verwendet in** aus, um anzuzeigen, wo diese Aktivitäten angezeigt werden.

   [![Hier finden Sie Anleitungen und  Vorlagenaktivitäten, die verwendet werden in](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)

Um Ihre Änderungen zu pushen:

1. Speichert die Änderungen, **Speichern** indem Sie die Schaltfläche auswählen. Wenn Sie keine Auswahl treffen, werden Sie aufgefordert, im nächsten Schritt die Änderungen zu speichern.

2. Wählen Sie **Diese Änderungen pushen**.

   
## <a name="add-or-edit-an-introduction"></a>Hinzufügen oder bearbeiten Sie eine Einleitung

1. Auf der Registerkarte **Einführung** geben Sie einen Titel für Anleitung und eine Öffnungsnachricht ein. Um den Beispieltext zu verwenden, wählen Sie **Verwenden Sie diese Meldung**.

    [![Einführungsregisterkarte in einer Onboard Vorlage](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)

2. Verwenden Sie die Formatierungsschaltflächen, um Text auszurufen, wie Sie ihn benötigen, oder um Links oder Bilder hinzufügen.
3. Wählen Sie **Speichern** aus, um die Arbeit zu speichern.

## <a name="add-or-edit-activities"></a>Hinzufügen oder Bearbeiten auswählen

1. Auf der Registerkarte **Aktivitäten** ziehen Sie Artikel von Rechts in den Bearbeitungsbereich.
2. Um Ihre Anleitung in Abschnitte zu organisieren, ziehen Sie das Element **Neuer Abschnitt** in den zu bearbeitenden Bereich und geben einen Namen und eine optionale Beschreibung für den Bereich ein.

    ![[Hinzufügen eines neuen Abschnitts zu einem Onboarding-Leitfaden oder einer Onboarding-Vorlage](./media/onboard-edit-add-section.png)](./media/onboard-edit-add-section.png)

3. Um die Aktivitäten hinzuzufügen, um die Einstellung abzuschließen, ziehen Sie das Element **Neue Aktivität** in den zu bearbeitenden Bereich und geben Sie einen Namen und eine Beschreibung für die Aktivität ein.

    ![[Hinzufügen einer neuen Aktivität zu einem Onboarding-Leitfaden oder einer Onboarding-Vorlage](./media/onboard-edit-add-activity.png)](./media/onboard-edit-add-activity.png)

4. Fügen Sie umfangreichen Inhalt Ihrer Onboarding Anleitung hinzu:

    - Um ein YouTube Videodatei hinzuzufügen, ziehen Sie den Artikel des zu bearbeitenden Bereichs **YouTube**, geben Sie einen Namen und eine Beschreibung für die Aktivität ein, und geben Sie die URL für die YouTube Videodatei ein.
    - Um eine Sway Präsentation oder einen Newsletter hinzufügen, ziehen Sie das Element **Sway** in den zu bearbeitenden Bereich und geben einen Namen und eine Beschreibung für die Aktivität oder die eingebettete URL für die Sway Präsentation oder den Newsletter ein.
    - Um eine Microsoft Power Apps-App hinzuzufügen, ziehen Sie den Artikel in den zu bearbeitenden Bereich **Power Apps**, geben Sie einen Namen und eine Beschreibung für die Aktivität ein, und wählen Sie entweder die Power Apps-App oder die Power Apps-App Kennung ein
    - Um ein Microsoft Stream Videodatei hinzuzufügen, ziehen Sie den Artikel des zu bearbeitenden Bereichs **Microsoft Stream**, geben Sie einen Namen und eine Beschreibung für die Aktivität ein, und geben Sie die URL für die Microsoft Stream Videodatei ein.
    - Um ein Microsoft Forms-Formular hinzuzufügen, ziehen Sie den Artikel in den zu bearbeitenden Bereich **Microsoft Forms**, geben Sie einen Namen und eine Beschreibung für die Aktivität, die URL für das Microsoft Forms-Formular ein, und geben Sie die Größe des Bildschirmbereichs an.
    - Um einen iFrame hinzuzufügen, der Internetinhalt enthält, ziehen Sie das Element **Web Inhalt (iFrame)** in den zu bearbeitenden Bereich, geben einen Namen und eine Beschreibung ein, geben die URL für den Internetinhalt ein und definieren die Größe des Bildschirmbereichs.

    ![[Hinzufügen eines umfangreichen Inhalts zu einem Onboarding-Leitfaden oder einer Onboarding-Vorlage](./media/onboard-edit-add-rich-content.png)](./media/onboard-edit-add-rich-content.png)

2. Optional: Im Bereich auf der rechten Seite weisen Sie jeder Aktivität eine bestimmte Person oder einer Rolle die Aktivität zu, fügen Sie ein Fälligkeitsdatum und eine Kontaktperson ein, und weisen Sie eine Kategoriefarbe zu. Wenn Sie eine Person oder einer Rolle einer Aktivität zuweisen, wird eine Aufgabe für jede Person erstellt. Diese Aufgabe wird im Onboard Menü unter **Aufgaben** angezeigt.

    [![Zuweisen einer Aktivität in eine Onboarding Anleitung oder Vorlage](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)

3. Wählen Sie **Speichern** aus, um die Arbeit zu speichern.

Wenn Sie eine Aktivität oder einen Abschnitt löschen, tun Sie dies, indem Sie die Schaltfläche **Löschen** (das Abfalleimersymbol) in der oberen rechten Ecke der Aktivität oder des Abschnitts auswählen.

Um die Aktivitäten und Abschnitte neu anzuordnen, ziehen Sie sie an einen neuen Speicherort.

## <a name="add-or-edit-contacts"></a>Kontakte hinzufügen oder bearbeiten

Sie können Kontaktpersonen hinzufügen, die Ihre neuen Mitarbeiter von Beginn weg unterstützen. Diese Kontakte können Personalverantwortliche, Teamkollegen, Onboarding-Kollegen, Mentoren, Administratoren und IT-Supportmitarbeiter sein.

1. Auf der Registerkarte **Kontakte** wählen Sie **Neuen Kontakt** aus.
2. Im Dialogfeld **Fügen Sie Teammitglied hinzu** geben Sie den Namen oder die E-Mail-Adresse der Kontaktperson ein, eine kurze Beschreibung, die erläutert, wie die Kontaktperson den neuen Mitarbeiter unterstützen kann und wählen Sie dann **Hinzufügen** aus. 

    ![[Hinzufügen eines Kontakts zu einem Onboarding-Leitfaden oder einer Onboarding-Vorlage](./media/onboard-edit-add-contact.png)](./media/onboard-edit-add-contact.png)

    Alternativ können Sie einen oder mehrere Kontakte unter **Vorschlägen** auswählen.

3. Wählen Sie **Speichern** aus, um die Arbeit zu speichern.

Um einen Kontakt zu löschen, wählen Sie die Schaltfläche **Löschen** (Abfalleimersymbol), das rechts neben dem Kontakt ist.

Um einen Kontakt zu bearbeiten, wählen Sie die Schaltfläche **Bearbeiten** (Stiftsymbol), das rechts neben dem Kontakt ist.

## <a name="add-or-edit-resources"></a>Ressourcen hinzufügen oder bearbeiten

Sie können nützliche Dateien, Zuordnungen und Links im Abschnitt **Ressourcen** Ihrer Onboarding-Anleitung hinzufügen.

1. Auf der Registerkarte **Ressourcen** wählen Sie **Neue Ressource** aus.
2. Führen Sie einen dieser Schritte aus:

    - Um eine Datei hinzufügen, wählen Sie die Registerkarte **Datei**, und ziehen Sie die Datei in den ausgewählten Bereich. (Alternativ klicken Sie auf eine beliebige Stelle in diesem Bereich, um die Datei auf dem Computer zu suchen, oder wählen Sie **Durchsuchen OneDrive** aus.) Geben Sie einen Namen für die Datei ein, und wählen Sie dann **Hinzufügen** aus.
    - Um eine Verknüpfung hinzuzufügen, wählen Sie die Registerkarte **Verknüpfung** aus, geben Sie einen Namen und die Adresse für die Verknüpfung ein, und wählen Sie dann **Hinzufügen** aus.
    - Um eine Zuordnung hinzuzufügen, wählen Sie die Registerkarte **Zuordnen** aus, geben Sie einen Namen und die Adresse für die Zuordnung ein, und wählen Sie dann **Hinzufügen** aus. Onboard eine Zuordnung der Adresse, die Sie angeben.

    ![[Hinzufügen einer Ressource zu einem Onboarding-Leitfaden oder einer Onboarding-Vorlage](./media/onboard-edit-add-resource.png)](./media/onboard-edit-add-resource.png)

3. Wählen Sie **Speichern** aus, um die Arbeit zu speichern.

Um eine Ressource zu löschen, wählen Sie die Schaltfläche **Löschen** Abfalleimersymbol), das rechts neben der Ressource ist.

Um einen Kontakt zu bearbeiten, wählen Sie die Schaltfläche **Bearbeiten** (Stiftsymbol), das rechts neben der Ressource ist.

## <a name="next-steps"></a>Nächste Schritte

- [Hier können Sie Inhalte mit anderen Personen teilen](./onboard-share-template.md)
- [Anzeigen des Status von Aufgaben und dem Onboarding von Mitarbeitern](./onboard-view-status.md)
- [Erstellen von Einstellungsteams in Onboard](./onboard-create-team.md)

### <a name="see-also"></a>Siehe auch

- [Testen oder kaufen Sie die Onbaord-App](https://dynamics.microsoft.com/talent/onboard/)
- [Was ist neu oder geändert in Dynamics 365 Talent](./whats-new.md)
- [Release-Pläne](https://docs.microsoft.com/business-applications-release-notes/index)
- [Sie erhalten Unterstützung für Microsoft Dynamics 365 Talent](./talent-support.md)
