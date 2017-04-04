---
title: "Mobiler Arbeitsbereich des Lagerbestandes für Microsoft Dynamics 365 für Arbeitsgangs-App"
description: "Die Arbeitsbereichhilfen mobilen des Lagerbestandes Sie erhalten Einblicke mobile in zur reservierten und zur verfügbaren Bestand jederzeit und überall."
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

# <a name="inventory-on-hand-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Mobiler Arbeitsbereich des Lagerbestandes für Microsoft Dynamics 365 für Arbeitsgangs-App

Die Arbeitsbereichhilfen mobilen des Lagerbestandes Sie erhalten Einblicke mobile in zur reservierten und zur verfügbaren Bestand jederzeit und überall. 

<a name="prerequisites"></a>Voraussetzungen
-------------

| Voraussetzung                                                         | Beschreibung                                                                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Lesen Sie zum Microsoft Dynamics 365 für Arbeitsgangsmobileplattform | [Dynamics 365 für mobile Plattform der Arbeitsgänge (/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)]                                   |
| Dynamics 365 für Arbeitsgänge                                          | Eine Umgebung, zur Microsoft Dynamics 365 für Arbeitsgangsversion 1611 und Microsoft Dynamics for Arbeitsgangsplattformaktualisierung 3 (November 2016) |
| Hotfix KB 3215650                                                    | Installieren des Hotfix Arbeitsbereiche, um die zu aktivieren, die im Microsoft Dynamics 365 für Arbeitsgänge bereitgestellt werden.                                       |
| Mobiles Gerät, das das Dynamics 365 für die Einstellungen Arbeitsgangs-App hat | Lädt die Dynamics 365 für Arbeitsgangs-App von Ihrem App-Shop mobilen herunter.                                                                           |

## <a name="introduction"></a>Einführung
Normalerweise haben Unternehmen mehrere Lieferungen und mehrere Anzeigen des Lagers jeden Tag. Diese Bewegungen ändern ständig den Status des verfügbaren Lagerbestands. Der Arbeitsbereich mobile des Lagerbestandes können Sie den Status des unternehmensübergreifenden verfügbaren Lagerbestand finden, um die neuesten Einblicke in Bestandsdaten im mobilen Gerät Auswahl erhalten können. Unabhängig davon, ob Sie am Lagerort, Einkaufs-, in Verkaufs-, bei der Herstellung oder bei der Verwaltung arbeiten oder haben Sie andere Rollen, können Sie die Daten des verfügbaren Lagerbestands jederzeit und überall zugreifen. Der Arbeitsbereich mobile enthält eine einzige Ansicht des Lagerstatus zur Einrichtung und schließt der verfügbare Lagerbestand oberhalb Einrichtungen, aktuellen Formulars und Reservierungen vorbehaltlosem verfügbarem Lagerbestand angezeigt. Sie können Artikelnummern auch eingeben, um verfügbaren Lagebestand abzufragen und führen eine gefilterte Dient zur Suche nach verfügbaren Produkte oder Varianten aus. Speziell enthält der Arbeitsbereich mobile diese Funktionen:

-   Sie können Nebenproduktnummer oder -Produktnamen suchen, um Produkte anzuzeigen, um den Status des verfügbaren Lagerbestands für angezeigt.
-   Für die ausgewählten Produkte können die folgenden Informationen angezeigt werden:
    -   Verfügbarer Lagerbestand pro Standort
    -   Verfügbarer Lagerbestand pro Lagerort
    -   Verfügbarer Lagerbestand pro Standort
    -   Verfügbarer Lagerbestand pro Charge (Produkte für chargengesteuerte)
    -   Verfügbarer Lagerbestand pro Bestandsstatus

<!-- -->

-   Produktverfügbarer Lagerbestand wird folgendermaßen angezeigt:
    -   Durch physischen Bestand (In dieser Ansicht bietet den Gesamtbetrag) dar.
    -   Durch den physisch reserviert "dieser Ansicht bietet den reservierten Betrag) dar.
    -   Durch verfügbare physische Menge "dieser Ansicht bietet verfügbare Betrag dar, der keine Reservierungen hat).

## <a name="get-started"></a>Erste Schritte
Klicken Sie auf dem mobiles Gerät anfangen:

1.  In Ihrem App-Shop mobilen Hochladen der Dateien herunter und Einrichten des Microsoft Dynamics 365 für Arbeitsgangs-App.
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

## <a name="view-the-onhand-inventory-for-a-product"></a>Zeigt den verfügbaren Bestand für ein Produkt an
1.  Auf einem mobilen Gerät wählen Sie den Lagerbestand ** ** Arbeitsbereich aus.
2.  Wählen Sie aus ** überprüfen Sie Bestand für einen Artikel **. Sie wird eine Liste der Produkte, die sich in der Zeit-App für offline Verwendung geladen werden. Standardmäßig sind 50 Artikel geladen, aber Sie können diese Nummer ändern. Weitere Informationen finden Sie im Doppellesehandbuch.
3.  Wenn der Artikel nicht in der Liste, wählen Sie ** suchen Sie mehr aus ** um eine Suche in Dynamics Online 365 für Vorgänge auszuführen. Suchen Sie Nebenproduktnummer oder wechseln Sie zu einem Suchennebenproduktnamen.
4.  Wählen Sie ein Produkt aus. Wenn der Artikel ein Bild hat das Bild, wird angezeigt.
5.  Wählen Sie eine der folgenden Optionen aus, um den Status für verfügbaren Lagerbestand anzeigen aus:
    -   Dient zum Anzeigen verfügbarer Bestand pro Standort an
    -   Dient zum Anzeigen verfügbarer Bestand pro Lagerort angezeigt
    -   Dient zum Anzeigen verfügbarer Bestand pro Standort anzeigen
    -   Dient zum Anzeigen verfügbarer Bestand pro Charge an (Produkte für chargengesteuerte)
    -   Dient zum Anzeigen verfügbarer Bestand pro Bestandsstatus an

    Produktverfügbarer Lagerbestand wird folgendermaßen angezeigt:
    -   Durch physischen Bestand (In dieser Ansicht bietet den Gesamtbetrag) dar.
    -   Durch den physisch reserviert "dieser Ansicht bietet den reservierten Betrag) dar.
    -   Durch verfügbare physische Menge (In dieser Ansicht werden der verfügbare Betrag dar, der keine Reservierungen hat).




