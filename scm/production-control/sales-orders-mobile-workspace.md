---
title: "Mobiler Arbeitsbereich für Aufträge für die Microsoft Dynamics 365 for Operations-App"
description: "Mit dem mobilen Arbeitsbereich für Aufträge können Sie in den Aufträgen jederzeit und überall Stand bleiben."
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

# <a name="sales-orders-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Mobiler Arbeitsbereich für Aufträge für die Microsoft Dynamics 365 for Operations-App

Mit dem mobilen Arbeitsbereich für Aufträge können Sie in den Aufträgen jederzeit und überall Stand bleiben. 

<a name="prerequisites"></a>Voraussetzungen
-------------

| Voraussetzung                                                         | Beschreibung                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lesen Sie mehr über die Microsoft Dynamics 365 für operations mobile Plattform | [Mobile Plattform für Dynamics 365 for Operations](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 for Operations                                          | Stellen Sie sicher, dass Sie eine Umgebung verwenden, die Microsoft Dynamics 365 for Operations Version 1611 und Microsoft Dynamics for Operations Platform Update 3 (November 2016) nutzen. |
| Hotfix KB 3215650                                                    | Installieren Sie den Hotfix, um die Arbeitsbereiche zu aktivieren, die in Microsoft Dynamics 365 for Operations bereitgestellt werden.                                                                       |
| Mobiles Gerät, auf dem die Dynamics 365 for Operations-App installiert ist | Laden Sie die Dynamics 365 for Operations-App aus dem mobilen App Store herunter.                                                                                                      |

## <a name="overview"></a>Überblick
Dieser mobile Arbeitsbereich greift auf die Dynamics 365 for Operations-App zu und zeigt detaillierte Informationen zu den einzelnen Aufträgen, z.B. den Auftragsstatus, Debitorenkontaktinformationen und Auftragsannahmekontaktinformationen anzeigen. Der mobile Arbeitsbereich enthält eine einzige Ansicht der Aufträge. Sie können Aufträge nach Debitor anzeigen, oder zeigen Sie alle Aufträge oder Informationen über einen bestimmten Auftrag angezeigt. Der mobile Arbeitsbereich enthält zwei Ansichten, um Ihnen dabei zu unterstützten, die detaillierten Verkaufsaufträge analysieren.

### <a name="view-all-sales-orders"></a>Alle Aufträge anzeigen

Bei dieser Ansicht werden alle Aufträge auf.

-   Wählen Sie einen der folgenden Filter aus, um den anzuzeigenden Auftrag auszuwählen.
    -   Suche von Aufträgen
    -   Nach Debitorenkonto suchen
    -   Debitorname suchen
    -   Nach Status suchen
    -   Nach Veröffentlichung suchen
    -   Nach Datum und Uhrzeit suchen

<!-- -->

-   Nach der Auswahl der Aufträge können Sie auf der Seite Auftrag anzeigen angezeigt werden. Sie können Folgendes anzeigen:
    -   Debitorenname und Adressinformationen
    -   Verschiedene Auftragsdatumsangaben, z.B. angefordertes und bestätigtes Versanddatum
    -   Kontaktinformationen des Auftragsnehmers
    -   Kontaktinformationen für den Debitor
    -   Auftragspositionen
    -   Lieferungen, die zeigen, wie und wann ein Auftrag geliefert wurde

### <a name="view-orders-for-a-customer-"></a>Aufträge für einen Kunden anzeigen** **

Zeigt Listen mit Aufträgen nach Debitor an.

-   Verwendung einer der nachfolgenden Filter, Aufträge für einen Debitor anzeigen.
    -   Suche nach Name
    -   Suche nach Konto

<!-- -->

-   Nachdem Sie einen Debitor auswählen, können Sie Folgendes anzeigen:
    -   Debitorname und Gruppe
    -   Kontaktinformationen für Debitor
    -   Kundenaufträge und andere Details zu Aufträgen:
        -   Debitorenname und Adressinformationen
        -   Verschiedene Auftragsdatumsangaben
        -   Kontaktinformationen des Auftragsnehmers
        -   Kontaktinformationen für Debitor
        -   Auftragspositionen
        -   Lieferungen, die zeigen, wie und wann ein Auftrag geliefert wurde

## <a name="get-started"></a>Erste Schritte
Gehen Sie folgendermaßen vor, um den mobilen Arbeitsbereich für Autrage auf Ihrem mobilen Gerät zu nutzen.

1.  Laden Sie die App im App Store herunter und installieren Sie die Microsoft Dynamics 365 for Operations-App.
2.  Starten Sie die App auf Ihrem Gerät.
3.  Geben Sie die URL Dynamics 365 ein.
4.  Geben Sie das Unternehmen ein. Geben Sie beispielsweise **USMF** ein.
5.  Wenn Sie sich zum ersten Mal anwenden, werden Sie nach einem Benutzernamen und einem Kennwort für Ihr Microsoft Dynamics 365 for Operations Konto gefragt. Geben Sie Ihre Anmeldeinformationen ein. Nachdem Sie sich angemeldet haben, sehen Sie verfügbaren Arbeitsbereiche für Ihr Unternehmen.

Um die Arbeitsbereiche auf der mobilen App zu sehen, müssen Sie zuerst die gewünschten Arbeitsbereiche in Dynamics 365 for Operations-App veröffentlichen.

1.  Starten Sie Dynamics 365 for Operations.
2.  Gehen Sie zu **ystemadministration**&gt; **Einrichten** &gt; **Systemparameter**.
3.  Wählen Sie **Mobile App verwalten**.
4.  Wählen Sie den Arbeitsbereich, um auf der mobilen Plattform zu veröffentlichen.
5.  Wählen Sie **Arbeitsbereich veröffentlichen**.
6.  Aktualisieren Sie das Gerät, um die veröffentlichten Arbeitsbereiche anzuzeigen.

## <a name="view-information-about-sales-orders-for-a-customer"></a>Zeigt Informationen zu Aufträgen für einen Debitor an.
1.  Wählen Sie auf Ihrem mobilen Gerät den Arbeitsbereich **Auträge**.
2.  Wählen Sie **Aufträge für einen Kunden anzeigen**.
3.  Verwenden Sie **Konto** oder **Debitorenname** Informationen, um den gewünschten Debitor zu suchen.
4.  Auswählen des Debitors
5.  Wählen Sie **Kontaktinformationen** oder **Aufträge** aus.
6.  Wenn **Aufträge** aktiviert ist, wird eine Liste der Aufträge für den Debitor angezeigt.
7.  **Auftrag** auswählen.
8.  Hier werden Informationen zu Auftragspositionen, Lieferungen, Debitorenkontaktinformationen und Auftragsannahmekontaktinformationen anzeigen.




