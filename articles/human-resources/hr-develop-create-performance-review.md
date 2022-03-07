---
title: Leistungsbeurteilungen erstellen
description: Dieses Thema erklärt, wie eine Leistungsüberprüfung erstellt wird, und es beschreibt den Zweck der Abschnitte der Prüfung.
author: twheeloc
ms.date: 08/26/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EssWorkspace, HcmDiscussionNewDialog, HcmDiscussion, HcmDiscussionChangeSettings, HcmDiscussionAddGoalDialog, HcmTopicCreate, HcmMeasurementDetailDialog, HcmPerfJournalAdd, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9c3ab4e769008bd8b401967e454aa6402f013773
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066949"
---
# <a name="create-performance-reviews"></a>Leistungsbeurteilungen erstellen


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]


Dieses Thema erklärt, wie eine Leistungsüberprüfung erstellt wird, und es beschreibt den Zweck der Abschnitte der Prüfung. Diese Prozedur wurde mit dem Demodatenunternehmen USMF erstellt.

1. Wählen Sie auf der Startseite den Arbeitsbereich **Mitarbeiter-Self-Service** aus.
2. Wählen Sie **Neue Überprüfung** aus, um eine neue Überprüfung zu erstellen.
3. Geben Sie im Feld **Überprüfungstyp** einen Wert ein, oder wählen Sie einen Wert aus.
4. Geben Sie im Feld **Leistungszeitraum** einen Wert ein, oder wählen Sie einen Wert aus.
5. Geben Sie im Feld **Enddatum** ein Datum ein.
6. Wählen Sie **OK**. Sie haben außerdem die Möglichkeit, eine Überprüfung auf der Grundlage einer Vorlage zu erstellen. Dies ist die beste Methode eine Überprüfung zu erstellen, da jeder Abschnitt die Informationen enthält, die Sie für den Start einer Überprüfung benötigen.  
7. Sie können Registerkarten wie die Anhangregisterkarte anzeigen oder ausblenden:

    1. Im Aktionsbereich wählen Sie **Abschnitte anzeigen** aus, um das Dialogmenü zu öffnen.
    1. Wählen Sie **Ja** oder **Nein** im Feld **Anhänge anzeigen** aus, um die Anhangregisterkarte ein- oder auszublenden.
    1. Wählen Sie **Speichern**.

8. Wählen Sie **Ziel zur Überprüfung hinzufügen** aus, um ein Ziel hinzuzufügen. Wählen Sie abschließend **OK** aus.
9. Wählen Sie **Kompetenz hinzufügen** aus, um das Dropdown-Dialogfeld zu öffnen.
10. Geben Sie im Feld **Titel** einen Wert ein.
11. Geben Sie im Feld **Beschreibung** `Increase customer skills by working with the support team` ein.
12. Wählen Sie **OK**.
13. Wählen Sie **Alle reduzieren** aus.
14. Wählen Sie **Alle erweitern** aus.
15. Wählen Sie **Kommentar hinzufügen** aus.
16. Wählen Sie **Buchen** aus.
17. Wählen Sie die Registerkarte **Messungen** aus.
18. Wählen Sie **Messung hinzufügen** aus, um das Dialogmenü zu öffnen.
19. Geben Sie im Feld **Messung** einen Wert ein, oder wählen Sie einen Wert aus.
26. Geben Sie im Feld **Zielbetrag** eine Zahl ein.
20. Wählen Sie **OK**.
21. Wählen Sie die Registerkarte **Aktivitäten** aus.
22. Wählen Sie **Hinzufügen** aus.
23. Geben Sie im Feld **Titel** einen Wert ein.
24. Geben Sie im Feld **Beschreibung** einen Wert ein.
25. Geben Sie im Feld **Startdatum** ein Datum ein.
26. Geben Sie im Feld **Abschlussdatum** ein Datum ein.
27. Wählen Sie im Feld **Entwicklungsplan** **Ja** aus.
28. Geben Sie im Feld **Schlüsselwörter** einen Wert ein.
29. Wählen Sie **Speichern**.
30. Wählen Sie die Registerkarte **Bewertungen** aus.  

    - Über das Inforegister **Bewertungsdetails** können Mitarbeiter sich selbst und der Manager den Mitarbeiter bewerten. Wenn Gewichtungen verwendet werden, wird der Gewichtungswert der Bewertungen automatisch berechnet.  
    - Um diesen Abschnitt anzuzeigen, aktivieren Sie die Parametereinstellungen für die Anzeige von Mitarbeiterbewertungen auf der Seite **Freigegebene Human-Resources-Parameter**.  

31. Wählen Sie die Registerkarte **Abzeichnungen** aus. Wenn die Überprüfung einen Workflow verwendet, werden die Abzeichnungen erst angezeigt, nachdem der Workflow abgeschlossen ist. Wird kein Workflow verwendet wird, dann werden die Arbeitskraft und der Manager hier aufgeführt. Das Kontrollkästchen **Erforderlich** für **Abzeichnungen** wird auf der Grundlage der Einstellungen im Überprüfungstyp aktiviert.  
32. Wählen Sie die Registerkarte **Allgemein**.

    - Die Leistungsperiode definiert das standardmäßige Start- und Enddatum. Diese Daten können geändert werden.  
    - Der Status steuert den Zugriff zur Prüfung. Der Status **Nicht gestartet** ermöglicht jedem die Bearbeitung der Prüfung. Der Status **In Bearbeitung** gestattet nur dem Mitarbeiter die Bearbeitung und Anzeige der Überprüfung. **Bereit zur Überprüfung** gestattet nur dem Manager das Anzeigen und Bearbeiten der Überprüfung. Der Status **Abschließende Überprüfung** ermöglicht sowohl dem Mitarbeiter als auch dem Vorgesetzten das Anzeigen und Bearbeiten der Überprüfung, falls die Option **Bearbeitung in abschließender Überprüfung zulassen** im Überprüfungstyp ausgewählt ist. Die Status **Abgeschlossen**, **Abgebrochen** markieren die Überprüfung als schreibgeschützt. Wenn eine Bewertung **Abgelehnt** ist und an den Mitarbeiter zurückgesendet wird, können sowohl der Mitarbeiter als auch der Manager die erforderlichen Änderungen vornehmen, damit der Mitarbeiter sie erneut einreichen kann.

33. Geben Sie im Feld **Überblick** einen Wert ein.
34. Wählen Sie die Registerkarte **Überprüfung** aus. Während die Überprüfung die Statuswerte durchläuft, können der Mitarbeiter und Manager Kommentare für jedes Ziel oder jede Kompetenz hinzufügen.  
35. Wählen Sie die Registerkarte **Abzeichnungen** aus. Die Arbeitskraft und der Manager können die Prüfung abzeichnen. Wenn alle erforderlichen Abzeichnungen abgeschlossen sind, wird der Status zu **Abgeschlossen** und es können keine weiteren Änderungen vorgenommen werden.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
