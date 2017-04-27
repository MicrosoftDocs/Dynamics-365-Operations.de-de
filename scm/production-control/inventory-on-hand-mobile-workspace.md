---
title: "Mobilen Arbeitsbereich für die Lagerbestand für die Microsoft Dynamics 365 for Operations-App"
description: "Die mobile Arbeitbereich für Lagerbestand bietet mobile Einblicke in reservierte und zur verfügbaren Bestand jederzeit und überall."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267094
ms.assetid: 85058f55-e566-40e2-9234-42d3e4fe5ff6
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 2ad48765528e1d1c6e7c90417b54a248ec79f546
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-on-hand-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Mobilen Arbeitsbereich für die Lagerbestand für die Microsoft Dynamics 365 for Operations-App

Die mobile Arbeitbereich für Lagerbestand bietet mobile Einblicke in reservierte und zur verfügbaren Bestand jederzeit und überall. 

<a name="prerequisites"></a>Voraussetzungen
-------------

| Voraussetzung                                                         | Beschreibung                                                                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Lesen Sie mehr über die Microsoft Dynamics 365 für operations mobile Plattform | [Mobile Plattform für Dynamics 365 for Operations](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                   |
| Dynamics 365 for Operations                                          | Eine Umgebung, die Microsoft Dynamics 365 for Operations Version 1611 und Microsoft Dynamics for Operations Platform Update 3 (November 2016) nutzen. |
| Hotfix KB 3215650                                                    | Installieren Sie den Hotfix, um die Arbeitsbereiche zu aktivieren, die in Microsoft Dynamics 365 for Operations bereitgestellt werden.                                       |
| Mobiles Gerät, auf dem die Dynamics 365 for Operations-App installiert ist | Laden Sie die Dynamics 365 for Operations-App aus dem mobilen App Store herunter.                                                                           |

## <a name="introduction"></a>Einführung
Normalerweise haben Unternehmen mehrere Lieferungen und mehrere Anzeigen des Lagers jeden Tag. Diese Bewegungen ändern ständig den Status des verfügbaren Lagerbestands. Der Arbeitsbereich mobile des Lagerbestandes können Sie den Status des unternehmensübergreifenden verfügbaren Lagerbestand finden, um die neuesten Einblicke in Bestandsdaten im mobilen Gerät Auswahl erhalten können. Unabhängig davon, ob Sie am Lagerort, Einkaufs-, in Verkaufs-, bei der Herstellung oder bei der Verwaltung arbeiten oder haben Sie andere Rollen, können Sie die Daten des verfügbaren Lagerbestands jederzeit und überall zugreifen. Der Arbeitsbereich mobile enthält eine einzige Ansicht des Lagerstatus zur Einrichtung und schließt der verfügbare Lagerbestand oberhalb Einrichtungen, aktuellen Formulars und Reservierungen vorbehaltlosem verfügbarem Lagerbestand angezeigt. Sie können Artikelnummern auch eingeben, um verfügbaren Lagebestand abzufragen und führen eine gefilterte Dient zur Suche nach verfügbaren Produkte oder Varianten aus. Speziell enthält der mobile Arbeitsbereich diese Funktionen:

-   Sie können Nebenproduktnummer oder -Produktnamen suchen, um Produkte anzuzeigen, um den Status des verfügbaren Lagerbestands für angezeigt.
-   Für die ausgewählten Produkte können die folgenden Informationen angezeigt werden:
    -   Verfügbarer Lagerbestand nach Standort
    -   Verfügbaren Bestand nach Lagerort
    -   Verfügbarer Lagerbestand nach Standort
    -   Verfügbarer Lagerbestand nach Charge (für chargengesteuerte Produkte)
    -   Verfügbaren Bestand nach Bestandsstatus

<!-- -->

-   Verfügbarer Lagerbestand wird folgendermaßen angezeigt:
    -   Durch physischen Bestand (Ansicht stellt den Gesamtbetrag dar).
    -   Durch physischen Reservierungen (Ansicht stellt den reservierten Betrag dar).
    -   Durch verfügbare physische Menge (Ansicht stellt den verfügbare Betrag dar, der keine Reservierungen hat).

## <a name="get-started"></a>Erste Schritte
Erste Schritte auf dem mobiles Gerät:

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

## <a name="view-the-onhand-inventory-for-a-product"></a>Verfügbarer Lagerbestand für das ausgewählte Produkt anzeigen
1.  Wählen Sie auf Ihrem mobilen Gerät den Arbeitsbereich **Verfügbarer Bestand**.
2.  Wählen Sie aus **Überprüfen des verfügbaren Bestand für einen Artikel**. Sie wird eine Liste der Produkte, die sich in der Zeit-App für offline Verwendung geladen werden. Standardmäßig sind 50 Artikel geladen, aber Sie können diese Nummer ändern. Weitere Informationen finden Sie im Handbuch in den Voraussetzungen.
3.  Wenn der Artikel nicht in der Liste, wählen Sie **Weitere suchen** aus, um eine Suche in Dynamics Online 365 for Operations auszuführen. Suchen Sie Nebenproduktnummer oder wechseln Sie zu einem Suchennebenproduktnamen.
4.  Wählen Sie ein Produkt aus. Wenn der Artikel ein Bild hat das Bild, wird angezeigt.
5.  Wählen Sie eine der folgenden Optionen aus, um den Status für verfügbaren Lagerbestand anzeigen aus:
    -   Verfügbaren Lagerbestand pro Site anzeigen
    -   Verfügbaren Lagerbestand pro Lagerort anzeigen
    -   Verfügbaren Lagerbestand pro Standort anzeigen
    -   Verfügbarer Lagerbestand nach Charge (für chargengesteuerte Produkte) anzeigen
    -   Verfügbaren Lagerbestand pro Bestandsstatus anzeigen

    Verfügbarer Lagerbestand wird folgendermaßen angezeigt:
    -   Durch physischen Bestand (Ansicht stellt den Gesamtbetrag dar).
    -   Durch physischen Reservierungen (Ansicht stellt den reservierten Betrag dar).
    -   Durch verfügbare physische Menge (Ansicht stellt den verfügbare Betrag dar, der keine Reservierungen hat).




