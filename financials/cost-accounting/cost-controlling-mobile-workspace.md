---
title: "Mobiler Arbeitsbereich für die Kostensteuerung für die Microsoft Dynamics 365 for Operations-App"
description: "Mit dem Arbeitsbereich Kostensteuerung können Kostenstellenmanager die Kostenstellenleistung jederzeit und überall finden."
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

# <a name="cost-controlling-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Mobiler Arbeitsbereich für die Kostensteuerung für die Microsoft Dynamics 365 for Operations-App

Mit dem Arbeitsbereich Kostensteuerung können Kostenstellenmanager die Kostenstellenleistung jederzeit und überall finden. 

<a name="prerequisites"></a>Voraussetzungen
-------------

| Voraussetzung                                                         | Beschreibung                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lesen Sie mehr über die Microsoft Dynamics 365 für operations mobile Plattform | [Mobile Plattform für Dynamics 365 for Operations](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 for Operations                                          | Stellen Sie sicher, dass Sie eine Umgebung verwenden, die Microsoft Dynamics 365 for Operations Version 1611 und Microsoft Dynamics for Operations Platform Update 3 (November 2016) nutzen. |
| Hotfix KB 3215650                                                    | Installieren Sie den Hotfix, um die Arbeitsbereiche zu aktivieren, die in Microsoft Dynamics 365 for Operations bereitgestellt werden.                                                                       |
| Mobiles Gerät, auf dem die Dynamics 365 for Operations-App installiert ist | Laden Sie die Dynamics 365 for Operations-App aus dem mobilen App Store herunter.                                                                                                      |

## <a name="introduction"></a>Einführung
Der Arbeitsbereicht Kostensteuerung enthält eine einzige Ansicht der Leistung der aktuellen Kostenstellen aus dem Vergleich von Istkosten im Vergleich zu den geplanten Kosten. Sie können den Status einzelner Kostenfaktoren mit Detailinformationen anzeigen.

### <a name="example"></a>Beispiel

Ein Mitarbeiter erhält eine Einladung zu einer internationalen Konferenz. Die Organisation muss alle Reisespesen abdecken. Der Mitarbeiter fragt den Vorgesetzten, ob er an der Konferenz teilnehmen darf. Der Vorgesetzte öffnet schnell den Arbeitsbereich Kostenkontrolle auf seinem Mobiltelefon, um festzustellen, ob er das Budget hat, und der Mitarbeiter die Konferenz besuchen kann.

### <a name="data-security"></a>Datensicherheit

Die Daten im Arbeitsbereich Kostensteuerung werden mit Anmeldeinformationen geschützt. Ein Kostenstellenmanager kann nur Daten für seine eigene Kostenstelle sehen. Die Zugriffsebenensicherheit wird im Modul "Kostenrechnung" verwaltet. Buchhalter definieren den Arbeitsbereicht Kostensteuerung im Modul Buchhaltungskosten. Nachdem der Arbeitsbereich auf Microsoft Dynamics 365 FOR Operations auf der App veröffentlicht ist, ist er in der mobilen App für Dynamics 365 for Operations verfügbar. Dadurch wird sichergestellt, dass alle Kostenstellenmanager in der gleichen Organisation Daten im selben Format sehen.

### <a name="actions-views-and-links"></a>Aktivitäten, Ansichten und Links

Der mobile Arbeitsbereich Kostensteuerunge in Dynamics 365 for Operations-App bietet folgende Aktivitäten, Ansichten und Links:

-   Aktionen 
    -   Wählen Sie  **Konfiguration**, un ein Layout auszuwählen.
    -   Wählen Sie **Kostenträger**, um die Kostenstellen zu wählen, von denen Sie Daten filtern möchten. **Hinweis:** Die Liste wird gemäß dem Zugriff angezeigt, der im Modul "Kostenrechnung" gewährt wird.

<!-- -->

-   Auf Grundlage der ausgewählten **Aktivitäten** und der Konfiguration im Modul "Kostenrechnung" können Sie folgende Informationen in den Karten anzeigen. Beachten Sie, dass der Betrag im gleichen Format angezeigt wird: Ist-, Budget, Abweichung und Abweichung %. 
    -   Ist-Wert verglichen mit Budget (aktuelle Periode)
    -   Aktuelle Periode vs Budget (aktuelle Periode)
    -   Ist-Wert verglichen mit Budget (vorherige Periode)
    -   Aktuelle Periode vergliechen mit überarbeitetem Budget (vorherige Periode)
    -   Istwert und Budget (seit Jahresbeginn)
    -   Istwert und überarbeitets Budget (Seit Jahresbeginn)

<!-- -->

-   Verknüpfungen
    -   Details für aktuelle Periode.
    -   Details für vorherige Periode.
    -   Details für Jahr bis jetzt.

Wenn Sie einen der Links auswählen, wird pro Ausgaben eine Karte angezeigt. Der Betrag in den Karten wird im folgenden Format angezeigt: Ist, Budget, Planabweichung, Planabweichung %, überarbeitetes Budget, überarbeitetes Budget Abweichung und überarbeitete Budget Abweichung %.  [![Kostensteuerung](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="get-started"></a>Erste Schritte
Gehen Sie folgendermaßen vor, um die mobilen Kosten-App auf Ihrem mobilen Gerät zu nutzen.

1.  Laden Sie die App im App Store herunter und installieren Sie die Microsoft Dynamics 365 for Operations-App.
2.  Starten Sie die App auf Ihrem Gerät.
3.  Geben Sie die URL Dynamics 365 ein.
4.  Geben Sie das Unternehmen ein. Geben Sie beispielsweise **USMF** ein.
5.  Wenn Sie sich zum ersten Mal anwenden, werden Sie nach einem Benutzernamen und einem Kennwort für Ihr Microsoft Dynamics 365 for Operations Konto gefragt. Geben Sie Ihre Anmeldeinformationen ein. Nachdem Sie sich angemeldet haben, sehen Sie verfügbaren Arbeitsbereiche für Ihr Unternehmen.

Um die Arbeitsbereiche auf der mobilen App zu sehen, müssen Sie zuerst die gewünschten Arbeitsbereiche in Dynamics 365 for Operations-App veröffentlichen.

1.  Starten Sie Dynamics 365 for Operations.
2.  Gehen Sie zu **ystemadministration**&gt; **Einrichten** &gt; **Systemparameter**.
3.  Wählen Sie **Mobile App verwalten**.
4.  Wählen Sie den Arbeitsbereich **Kostensteuerung, um auf der mobilen Plattform zu veröffentlichen.
5.  Wählen Sie **Arbeitsbereich veröffentlichen**.
6.  Aktualisieren Sie das Gerät, um die veröffentlichten Arbeitsbereiche anzuzeigen.

## <a name="view-the-performance-of-your-cost-center"></a>Hier können Sie die Leistung der Kostenstelle anzeigen
1.  Wählen Sie auf Ihrem mobilen Gerät den Arbeitsbereich **Kostensteuerung**.
2.  Wählen Sie **Kostenträgersteuerung **.
3.  Klicken Sie auf **Aktiviäten**.
4.  Klicken Sie auf **Konfiguration auswählen**, um das Layout der Kostensteuerung zu wählen.
5.  Klicken Sie auf **Fertig.**
6.  Klicken Sie auf **Aktivitäten**.
7.  Klicken Sie auf **Kostenträger auswählen **, um die Kostenstelle auszuwähen, auf die Sie Zugriff haben.
8.  Klicken Sie auf **Fertig.**
9.  Hier können Sie die Leistung der Kostenstelle anzeigen.
10. Klicken Sie auf **Details für die aktuelle Periode**.
11. Hier können Sie die Leistung der einzelnen Kostenelemente anzeigen
12. Sie können auch nach bestimmten Kostenfaktoren suchen.



