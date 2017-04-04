---
title: "Mobiler Arbeitsbereich der Aufträge für Microsoft Dynamics 365 für Arbeitsgangs-App"
description: "Bei Aufträgen mobiler Arbeitsbereich, können Sie in den Aufträgen jederzeit und überall Stand bleiben."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267134
ms.assetid: dbc6dc39-b535-42d3-9fbd-4724597388ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 851c53e1c53fb37488ed86e25e3ede83ca0541db
ms.lasthandoff: 03/31/2017


---

# <a name="sales-orders-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Mobiler Arbeitsbereich der Aufträge für Microsoft Dynamics 365 für Arbeitsgangs-App

Bei Aufträgen mobiler Arbeitsbereich, können Sie in den Aufträgen jederzeit und überall Stand bleiben. 

<a name="prerequisites"></a>Voraussetzungen
-------------

| Voraussetzung                                                         | Beschreibung                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lesen Sie zum Microsoft Dynamics 365 für Arbeitsgangsmobileplattform | [Dynamics 365 für mobile Plattform der Arbeitsgänge (/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)]                                                              |
| Dynamics 365 für Arbeitsgänge                                          | Stellen Sie sicher, dass Sie eine Umgebung verwenden, die Microsoft Dynamics 365 für Arbeitsgangsversion 1611 und Microsoft Dynamics for Arbeitsgangsplattformaktualisierung 3 (November 2016). |
| Hotfix KB 3215650                                                    | Installieren des Hotfix, um die Arbeitsbereiche zu ermöglichen, die in Microsoft Dynamics 365 für Arbeitsgänge bereitgestellt werden.                                                                       |
| Mobiles Gerät, das das Dynamics 365 für die Einstellungen Arbeitsgangs-App hat | Lädt die Dynamics 365 für Arbeitsgangs-App von Ihrem App-Shop mobilen herunter.                                                                                                      |

## <a name="overview"></a>Überblick
Dieser mobile Arbeitsbereich greift das Dynamics 365 für Arbeitsgangsbewerbung zu und können Sie detaillierte Informationen zu den einzelnen Aufträgen, z, Auftragsstatus, Debitorenkontaktinformationen und Auftragsannahmekontaktinformationen anzeigen. Der Arbeitsbereich mobile enthält eine einzige Ansicht der Aufträge. Sie können Aufträge nach Debitor anzeigen, oder zeigen Sie alle Aufträge oder Informationen über einen bestimmten Auftrag angezeigt. Der Arbeitsbereich mobile enthält zwei Ansichten, um Ihnen dabei zu unterstützten, die detaillierten Verkaufsaufträge analysieren.

### <a name="view-all-sales-orders"></a>Hier können Sie alle Aufträge anzeigen

Bei dieser Ansicht werden alle Aufträge auf.

-   Verwendung einer der nachfolgenden Filter, die Aufträge auszuwählen, der angezeigt werden soll.
    -   Suche von Aufträgen
    -   Suche nach Debitorenkonto
    -   Suche nach Debitorenname
    -   Suche nach Status
    -   Suche nach Freigabenstatus
    -   Suche nach Erstellungsdatum an und Zeit

<!-- -->

-   Nachdem Sie die Aufträge auswählen, können Sie die Details bestimmter Aufträge anzeigen. Wir können Sie Folgendes anzeigen:
    -   Debitorenname und Adressinformationen
    -   Verschiedene Auftragsdatumsangaben, z Angefordertes und bestätigtes Versanddatum
    -   Auftragsannahmekontaktinformationen
    -   Debitorenkontaktinformationen
    -   Auftragspositionen
    -   Lieferungen, die zeigen, wie und wann ein Auftrag geliefert wurde

### <a name="view-orders-for-a-customer-"></a>Ansichtsaufträge ** ** für einen Debitor

Bei dieser Ansicht werden Aufträge pro Debitor auf.

-   Verwendung einer der nachfolgenden Filter, Aufträge für einen Debitor anzeigen.
    -   Suche nach Name
    -   Suche nach Konto

<!-- -->

-   Nachdem Sie einen Debitor auswählen, können Sie Folgendes anzeigen:
    -   Debitorenname und Gruppe
    -   Debitorenkontaktinformationen
    -   Kundenaufträge und andere Details zu den für:
        -   Debitorenname und Adressinformationen
        -   Verschiedene Auftragsdatumsangaben
        -   Auftragsannahmekontaktinformationen
        -   Debitorenkontaktinformationen
        -   Auftragspositionen
        -   Lieferungen, die zeigen, wie und wann Aufträge versendet wurde

## <a name="get-started"></a>Erste Schritte
Gehen Sie folgendermaßen vor, um mithilfe des - Arbeitsbereichs mobilen der Aufträge auf Ihrem mobilen Gerät anzufangen.

1.  Auf dem App-Shop mobilen Hochladen der Dateien herunter und Einrichten des Microsoft Dynamics 365 für Arbeitsgangs-App.
2.  Starten der Zeit-App auf Ihrem Gerät.
3.  Geben Sie die URL Dynamics 365 ein.
4.  Geben Sie das Unternehmen, um in zu signieren. Geben Sie beispielsweise ein USMF ** **.
5.  Das zum ersten Mal, in dem Sie gerade signieren, werden für Sie den Benutzernamen und das Kennwort für Ihr Microsoft Dynamics 365 für Arbeitsgangskonto aufgefordert. Geben Sie Ihre Anmeldeinformationen ein. Nachdem Sie in signieren, wird im verfügbaren Arbeitsbereiche für Ihr Unternehmen.

Um auf Arbeitsbereiche der Zeit-App mobilen anzuzeigen, müssen Sie die gewünschten Arbeitsbereiche dem Dynamics 365 für Arbeitsgangs-App zuerst veröffentlichen.

1.  Start Dynamics 365 für Arbeitsgänge.
2.  Wechseln ** Systemverwaltung ** &gt; ** Einstellungen ** &gt; ** Systemparameter **.
3.  Wählen Sie aus ** Verwalten mobile Zeit-App **.
4.  Wählen Sie den aus, die der Verknüpfung mobilen Plattform zu veröffentlichen.
5.  Wählen Sie aus ** Veröffentlichen Arbeitsbereich **.
6.  Aktualisieren Sie das Gerät, um die veröffentlichten Arbeitsbereiche anzuzeigen.

## <a name="view-information-about-sales-orders-for-a-customer"></a>Hier werden Informationen zu Aufträgen für einen Debitor anzeigen
1.  Auf einem mobilen Gerät Auswählen des Arbeitsbereichs ** ** Aufträge aus.
2.  Wählen Sie aus ** Anzeigen von Aufträgen für einen Debitor anzeigen **.
3.  Verwendung ** Konto ** oder ** Debitorenname ** Informationen, den gewünschten Debitor zu suchen.
4.  Wählen Sie den Debitor aus.
5.  Wählen Sie aus oder Kontaktinformationen ** ** ** ** Aufträge.
6.  ** ** Wenn Aufträge aktiviert ist, wird eine Liste der Aufträge für den Debitor angezeigt.
7.  Wählen Sie aus ** ** Auftrag.
8.  Hier werden Informationen zu Auftragspositionen, Lieferungen, Debitorenkontaktinformationen und Auftragsannahmekontaktinformationen anzeigen.




