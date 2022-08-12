---
title: Apps von Drittanbietern einbetten
description: Dieser Artikel erklärt, wie Sie Apps von Drittanbietern einbinden können, um die Funktionalität des Produkts zu erweitern.
author: jasongre
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, UserWorkspaceAdd, UserWorkspaceConfigureWebsite
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2021-04-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ef5ed6c3c99d62010643940f3e2f158963ff0dc2
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2022
ms.locfileid: "9123717"
---
# <a name="embed-third-party-apps"></a>Apps von Drittanbietern einbetten

[!include [banner](../includes/banner.md)]

Viele Debitor verwenden eine Reihe von Anwendungen, um ihr Geschäft auszuführen. Bei einigen dieser Anwendungen handelt es sich um Web Apps von Drittanbietern, die mit den Finanz- und Betriebs-Apps zusammenarbeiten. Um eine nahtlosere Benutzererfahrung zu bieten, können Sie die Funktion **Full Page Apps** verwenden, um diese Apps von Drittanbietern direkt in Ihre Finanz- und Betriebs-Apps einzubetten (vorausgesetzt, die Apps von Drittanbietern lassen die Einbindung zu). Auf diese Weise können Benutzer auf die von ihnen benötigten Websites und Apps zugreifen, ohne die Registerkarten oder Fenster wechseln zu müssen.

Bevor Sie Apps von Drittanbietern in das Produkt einbetten können, müssen Sie die Funktion **Vollständige Seite Apps** in der Funktionsverwaltung einschalten. Sie können dann eine der folgenden Methoden verwenden, um eine App oder Website eines Drittanbieters einzubinden. Diese Methoden sind analog zu den Methoden, mit denen Canvas Apps von Microsoft Power Apps in Finanz- und Betriebs-Apps eingebettet werden.

- Einbetten der App oder Website auf einer bestehenden Seite als neue Registerkarte (Pivot-Tab, Inforegister, Blade oder Arbeitsbereich).
- Erstellen Sie eine neue ganzseitige Erfahrung für die App oder Website vom Dashboard aus.

## <a name="embed-a-website-on-an-existing-page"></a>Einbetten einer Website auf einer bestehenden Seite

Verwenden Sie dieses Verfahren, wenn Sie eine bestehende Seite im System mit einer eingebetteten App ergänzen wollen.

1. Öffnen Sie die Seite, auf der Sie die App einbetten möchten.
2. Öffnen Sie den Bereich **Hinzufügen einer App**:

    1. Wählen Sie **Einstellungen** und dann **Personalisierung**, um die Symbolleiste **Personalisierung** zu öffnen.
    2. Wählen Sie **Mehr \> Eine App hinzufügen**.

3. Wählen Sie den Bereich der Seite, in dem Sie die App hinzufügen wollen. Dieser Bereich muss ein *Registerkarten-Container* für eine Pivot-Registerkarte, eine Inforegisterkarte, eine Klinge oder einen Arbeitsbereich sein.
4. Wählen Sie **Website**.
5. Die eingebettete App konfigurieren:

    - **Name** – Geben Sie den Text ein, der für die Registerkarte angezeigt werden soll, die die eingebettete App enthält. Oft werden Sie wollen, dass dieser Text der Name der App ist.
    - **URL** – Geben Sie den Lagerplatz der App an.

    > [!IMPORTANT]
    > - Aus Sicherheitsgründen muss die URL das Hypertext Transfer Protocol Secure (HTTPS) verwenden.
    > - Die App oder Website muss so konfiguriert sein, dass sie das Einbetten zulässt.

6. Wählen Sie **Speichern**, um die App auf der Seite einzubetten. Die App wird als letzte Registerkarte oder Abschnitt in der Gruppe hinzugefügt.
7. Bestätigen Sie, dass die App wie erwartet erscheint. Wenn die App nicht gerendert wird, lesen Sie den Abschnitt [Fehlerbehebung](#troubleshooting) weiter unten in diesem Artikel.
8. Öffnen Sie die Ansichtsauswahl und wählen Sie entweder **Speichern** (wenn die App mit der aktuellen Ansicht verbunden werden soll) oder **Speichern unter** (um die App in einer anderen Ansicht zu speichern).

    Wenn die Seite keinen Ansichtsselektor hat (z. B. wenn die Seite ein Dialogfeld oder ein Arbeitsbereich ist), können Sie diesen Schritt überspringen.

## <a name="embed-a-website-as-a-full-page-experience-from-the-dashboard"></a>Einbetten einer Website als Ganzseitenerlebnis vom Dashboard aus

Verwenden Sie dieses Verfahren, wenn die App, die Sie einbetten möchten, nicht mit einer bestehenden Seite verknüpft ist, oder wenn Sie nur eine ganzseitige Darstellung der App innerhalb der Finanz- und Betriebs-App wünschen.

1. Öffnen Sie das Dashboard.
2. Wählen und halten Sie (oder klicken Sie mit der rechten Maustaste) auf dem Dashboard, wählen Sie **Personalisieren**, und wählen Sie dann **Seite hinzufügen**.
3. Wählen Sie im Bereich **Seite hinzufügen** die Option **Website**.
4. Die eingebettete App konfigurieren:

    - **Name** – Geben Sie den Text ein, der auf der Kachel angezeigt werden soll, die für die eingebettete App auf dem Dashboard hinzugefügt wird. Oft werden Sie wollen, dass dieser Text der Name der App ist.
    - **URL** – Geben Sie den Lagerplatz der App an.

    > [!IMPORTANT]
    > - Aus Sicherheitsgründen muss die URL HTTPS verwenden.
    > - Die App oder Website muss so konfiguriert sein, dass sie das Einbetten zulässt.

5. Wählen Sie **Speichern**, um die App dem Dashboard als neue Kachel hinzuzufügen.
6. Wählen Sie die neue Kachel auf dem Dashboard und bestätigen Sie, dass die App wie erwartet angezeigt wird. Wenn die App nicht gerendert wird, lesen Sie den Abschnitt [Problembehandlung](#troubleshooting) weiter unten in diesem Artikel.

## <a name="sharing-embedded-apps"></a>Gemeinsame Nutzung eingebetteter Apps

Nachdem Sie eine App mit Hilfe einer der in den vorherigen Abschnitten beschriebenen Methoden eingebettet haben, möchten Sie die Ansicht vielleicht für andere Benutzer im System freigeben. Um eine eingebettete App freizugeben, verwenden Sie eine der folgenden Methoden:

- **Veröffentlichen Sie die Ansicht (empfohlen):** Wenn die eingebettete App in einer Ansicht gespeichert wurde, ist der empfohlene und bevorzugte Weg, sie zu teilen, die Ansicht für Benutzer zu veröffentlichen, die die entsprechenden Sicherheitsrollen in den angestrebten juristischen Entitäten haben. In diesem Fall werden nur die gewünschten Benutzer die eingebettete App auf dieser Seite sehen. Weitere Informationen über das Veröffentlichen einer Ansicht finden Sie unter [Veröffentlichen von Ansichten](saved-views.md#publishing-views).

    Sie können auch eine App veröffentlichen, die als ganzseitige Erfahrung vom Dashboard aus eingebettet wurde. Wählen und halten Sie auf dem Dashboard die Kachel, die mit der App verknüpft ist (oder klicken Sie mit der rechten Maustaste), wählen Sie **Personalisieren** und dann **Seite veröffentlichen**. Es wird ein Erlebnis angezeigt, das dem *Veröffentlichen von Ansichten* ähnelt, und Sie können die Sicherheitsrollen auswählen, an die veröffentlicht werden soll. Wenn in Update 10.0.21 oder später die Funktion **Verbesserte Unterstützung juristischer Entitäten für gespeicherte Ansichten** aktiviert ist, können Sie die App auch für die gewünschten juristischen Entitäten veröffentlichen.

- **Kopieren Sie die Personalisierung:** Für Seiten, die keine Ansichten unterstützen (z. B. Dialogfelder oder Arbeitsbereiche), oder für das ganzseitige App-Erlebnis können Sie die Personalisierung auf die entsprechenden Benutzer kopieren. Weitere Informationen finden Sie unter [Freigeben von Personalisierungen](personalize-user-experience.md#sharing-personalizations).

## <a name="viewing-embedded-apps"></a>Anzeigen von eingebetteten Apps

Um eine eingebettete App auf einer Seite in Finanz- und Betriebs-Apps zu sehen, öffnen Sie die Seite, auf der die App eingebettet ist. Denken Sie daran, dass auf einigen Seiten auf eingebettete Apps über die Schaltfläche **Power Apps** im Standard-Aktivitätsbereich zugegriffen werden kann. Alternativ können sie direkt auf der Seite als neues Inforegister, Inforegister oder Blade oder als neuer Abschnitt in einem Arbeitsbereich erscheinen.

## <a name="editing-or-removing-embedded-apps"></a>Bearbeiten oder Entfernen von eingebetteten Apps

Nachdem eine App auf einer Seite eingebettet wurde, müssen Sie eventuell ihre Konfiguration bearbeiten (z. B. durch Ändern des Abschnitts-Labels oder der URL). Alternativ können Sie sie auch aus der Seite entfernen. Verwenden Sie eines der folgenden Verfahren, um die Konfiguration einer eingebetteten App zu bearbeiten oder sie vollständig zu entfernen.

### <a name="apps-that-are-embedded-on-existing-pages"></a>Apps, die auf bestehenden Seiten eingebettet sind

1. Öffnen Sie die Seite, auf der die App eingebettet ist.
2. Wählen Sie **Einstellungen** und dann **Personalisierung**, um die Symbolleiste **Personalisierung** zu öffnen.
3. Wählen Sie das Tool **Auswählen** und wählen Sie dann die eingebettete App.
4. Um die App zu bearbeiten, nehmen Sie die gewünschten Änderungen an ihrer Konfiguration vor und wählen Sie dann **Speichern**.

    Um die App zu entfernen, wählen Sie alternativ **Löschen**.

5. Speichern Sie die Ansicht erneut oder veröffentlichen Sie sie erneut. Beachten Sie, dass, wenn Sie die Seite verlassen, ohne die Ansicht explizit zu speichern, keine der Aktionen, die Sie im Bereich **Website bearbeiten** durchgeführt haben, beibehalten wird.

### <a name="apps-that-are-embedded-from-the-dashboard"></a>Apps, die vom Dashboard aus eingebettet werden

1. Öffnen Sie das Dashboard.
2. Wählen und halten Sie (oder klicken Sie mit der rechten Maustaste) die Kachel, die mit der eingebetteten App verbunden ist, und wählen Sie dann **Personalisieren**.
3. Um die App zu bearbeiten, wählen Sie **Seite bearbeiten**. Nehmen Sie im Bereich **Website bearbeiten** die gewünschten Änderungen an der App-Konfiguration vor und wählen Sie dann **Speichern**.

    Um die App zu entfernen, wählen Sie alternativ **Seite entfernen**.

## <a name="appendix"></a>Anhang

### <a name="troubleshooting"></a>Problembehandlung

Wenn eine Website nicht korrekt gerendert wird, nachdem sie in eine App für Finanzen und Vorgänge eingebettet wurde, oder wenn Sie eine Fehlermeldung erhalten, die besagt, dass der URL eine Verbindung verweigert wurde, ist die Website wahrscheinlich so konfiguriert, dass sie nicht in einen Iframe eingebettet werden kann. Führen Sie diese Schritte aus, um festzustellen, ob die Website eingebettet werden kann.

1. Öffnen Sie die Entwickler-Tools für den von Ihnen verwendeten Browser.
2. Suchen Sie auf der Registerkarte **Netzwerk** die Antwort von der eingebetteten Seite und wählen Sie sie aus.
3. Suchen Sie auf der Registerkarte **Kopfzeilen** unter **Antwortkopfzeilen** nach **x-frame-options**. Wenn **x-frame-options** in den Antwort-Headern vorhanden ist und einen Wert von **DENY** oder **SAMEORIGIN** hat, kann die Website derzeit nicht eingebettet werden. Sie müssen mit dem Besitzer der App zusammenarbeiten, damit diese sicher eingebettet werden kann.

### <a name="developer-modeling-a-website-on-a-form"></a>[Entwickler] Modellieren einer Website auf einem Formular

Obwohl sich dieser Artikel auf das Einbetten von Apps oder Websites von Drittanbietern durch Personalisierung konzentriert, können Entwickler diese auch in ein Formular einbetten, indem sie die Visual Studio-Entwicklungsumgebung nutzen. Fügen Sie einfach ein **WebsiteHostControl** Steuerelement in das Formular ein. Die für das Steuerelement verfügbaren Metadaten-Eigenschaften bieten die gleichen Funktionalitäten wie das Personalisierungserlebnis.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

