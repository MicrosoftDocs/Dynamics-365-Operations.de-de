---
title: "Steuernder mobiler Arbeitsbereich Kostenanteile für Microsoft Dynamics 365 für Arbeitsgangs-App"
description: "Mit dem steuernden mobilen Arbeitsbereich Kosten können Kostenstellenmanager die Kostenstellenleistung jederzeit und überall finden."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16 - 53 - 04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267114
ms.assetid: 84740472-494f-444c-9b74-f83b7342fd25
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 8136efb1d2669c39fcc0f80b60e80ecae983d5d8
ms.lasthandoff: 03/31/2017


---

# <a name="cost-controlling-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Steuernder mobiler Arbeitsbereich Kostenanteile für Microsoft Dynamics 365 für Arbeitsgangs-App

Mit dem steuernden mobilen Arbeitsbereich Kosten können Kostenstellenmanager die Kostenstellenleistung jederzeit und überall finden. 

<a name="prerequisites"></a>Voraussetzungen
-------------

| Voraussetzung                                                         | Beschreibung                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lesen Sie zum Microsoft Dynamics 365 für Arbeitsgangsmobileplattform | [Dynamics 365 für mobile Plattform der Arbeitsgänge (/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)]                                                              |
| Dynamics 365 für Arbeitsgänge                                          | Stellen Sie sicher, dass Sie eine Umgebung verwenden, die Microsoft Dynamics 365 für Arbeitsgangsversion 1611 und Microsoft Dynamics for Arbeitsgangsplattformaktualisierung 3 (November 2016). |
| Hotfix KB 3215650                                                    | Installieren des Hotfix, um die Arbeitsbereiche zu ermöglichen, die in Microsoft Dynamics 365 für Arbeitsgänge bereitgestellt werden.                                                                       |
| Mobiles Gerät, das das Dynamics 365 für die Einstellungen Arbeitsgangs-App hat | Lädt die Dynamics 365 für Arbeitsgangs-App von Ihrem App-Shop mobilen herunter.                                                                                                      |

## <a name="introduction"></a>Einführung
Der steuernde mobile Arbeitsbereich Kosten enthält eine einzige Ansicht der Leistung der aktuellen Kostenstellen aus dem Vergleich von Istkosten im Vergleich die geplanten Kosten angeben. Sie können den Status einzelner Kostenfaktoren Detailinformationen anzeigen.

### <a name="example"></a>Beispiel

Ein Mitarbeiter erhält eine Einladung zu einer Konferenz Internationalen. Die Organisation muss alle Reisespesen enthalten. Der Mitarbeiter fordert um seine Sicht auf, ob er den Konferenz anwesend sein kann. Der Vorgesetzte öffnet schnell den steuernden mobilen Arbeitsbereich Kosten nach freiem Mobiltelefon, um festzustellen, ob er das Budget aus, damit der Mitarbeiter die Konferenz bedient.

### <a name="data-security"></a>Datensicherheit

Die Daten im steuernden Arbeitsbereich Kosten werden nach Benutzeranmeldeinformationen geschützt. Einem Kostenstellenmanager ist nur zulässig, um Daten für eigene Kostenstelle zu finden. Die Zugriffsebenensicherheit wird im Modul "Kostenrechnung" verwaltet. Danach Kosten definieren die steuernde mobile Arbeitsbereichkonfiguration Kosten im Modul "Kostenrechnung". Nachdem der Arbeitsbereich auf Microsoft Dynamics 365 für Arbeitsgangs-App veröffentlicht ist, wurde er im Dynamics 365 für Arbeitsgangsmobile-App verfügbar. Dadurch wird sichergestellt, dass alle Kostenstellenmanager in der gleichen Organisation Daten im Format berücksichtigen.

### <a name="actions-views-and-links"></a>Aktivitäten, Sicht- und Links

Der steuernde mobile Arbeitsbereich Kostenanteile für Dynamics 365 für Arbeitsgangs-App bietet folgende Aktivitäten Ansichten, die und die Links:

-   Aktionen 
    -   Wählen Sie aus ** Konfigurationen ** um ein Layout zu entnehmen.
    -   Wählen Sie ** Kostenträger aus ** um Kostenstellen die zu entnehmen, für die Sie Daten soll. ** Hinweis: ** Die Liste wird gemäß dem der Zugriff angezeigt, der im Modul "Kostenrechnung" gewährt wird.

<!-- -->

-   Auf Grundlage, der unter ausgewählt wird ** ** Aktivitäten und Aufgaben im Modul "Kostenrechnung" konfiguriert wird, können Sie die folgenden Informationen im den Karten anzeigen können. Beachten Sie, dass der Betrag im gleichen Format angezeigt wird: Ist-, Budget-, Abweichung und Abweichung %. 
    -   Istwert verglichen mit Budget (aktuelle Periode)
    -   Istwert verglichen mit Budget " überarbeitetes aktuelle Periode)
    -   Istwert verglichen mit Budget " vorherige Periode)
    -   Istwert verglichen mit Budget " überarbeitetes vorherige Periode)
    -   Istwert verglichen mit Budget (Seit Jahresbeginn)
    -   Istwert verglichen mit Budget überarbeitetes (Seit Jahresbeginn)

<!-- -->

-   Verknüpfungen
    -   Details für aktuelle Periode.
    -   Details für vorherige Periode.
    -   Details für Jahr bis jetzt.

Wenn Sie einen der Links auswählen, wird pro Ausgaben eine Karte angezeigt. Der Betrag in die Karten wird im folgenden Format angezeigt: Ist-, Budget-, Planabweichung, Planabweichung %, überarbeitete Budget überarbeitete, und Planabweichung überarbeitete Planabweichung %.  [] (Kosten-steuerndes ![. /media/cost-controlling.png)]". /media/cost-controlling.png)

## <a name="get-started"></a>Erste Schritte
Gehen Sie folgendermaßen vor, um mithilfe der Zeit-App mobilen der Kostensteuerung auf Ihrem mobilen Gerät anzufangen.

1.  Auf dem App-Shop mobilen Hochladen der Dateien herunter und Einrichten des Microsoft Dynamics 365 für Arbeitsgangs-App.
2.  Starten der Zeit-App auf Ihrem Gerät.
3.  Geben Sie die URL Dynamics 365 ein.
4.  Geben Sie das Unternehmen, um in zu signieren. Geben Sie beispielsweise ein USMF ** **.
5.  Das zum ersten Mal, in dem Sie gerade signieren, werden für Sie den Benutzernamen und das Kennwort für Ihr Microsoft Dynamics 365 für Arbeitsgangskonto aufgefordert. Geben Sie Ihre Anmeldeinformationen ein. Nachdem Sie in signieren, wird im verfügbaren Arbeitsbereiche für Ihr Unternehmen.

Um auf Arbeitsbereiche der Zeit-App mobilen anzuzeigen, müssen Sie die gewünschten Arbeitsbereiche dem Dynamics 365 für Arbeitsgangs-App zuerst veröffentlichen.

1.  Start Dynamics 365 für Arbeitsgänge.
2.  Wechseln ** Systemverwaltung ** &gt; ** Einstellungen ** &gt; ** Systemparameter **.
3.  Wählen Sie aus ** Verwalten mobile Zeit-App **.
4.  Wählen Sie des Arbeitsbereichs ** Steuern Kosten auswählen ** die der mobilen Plattform zu veröffentlichen.
5.  Wählen Sie aus ** Veröffentlichen Arbeitsbereich **.
6.  Aktualisieren Sie das Gerät, um die veröffentlichten Arbeitsbereiche anzuzeigen.

## <a name="view-the-performance-of-your-cost-center"></a>Hier können Sie die Leistungsfähigkeit der Kostenstelle an
1.  Auf einem mobilen Gerät Auswählen des ** Sie Kosten das Steuern ** Arbeitsbereich aus.
2.  Wählen Sie aus Kostenträgersteuern ** **.
3.  ** ** Auf Aktivitäten.
4.  ** Wählen auf der Konfiguration aus ** um einen steuernden Layouts auszuwählen Kosten.
5.  Click **Done**.
6.  ** ** Auf Aktivitäten.
7.  ** Auf wählen Sie z ** Kostenträger aus der Kostenstellen aus, denen Sie Zugriff gewährt wurde.
8.  Click **Done**.
9.  Zeigt die Gesamtleistung der Kostenstelle an.
10. ** Auf Details für aktuelle Periode **.
11. Hier können Sie die Leistungsfähigkeit einzelner Kostenfaktoren angezeigt.
12. Sie können für bestimmte Kostenfaktoren auch finden.



