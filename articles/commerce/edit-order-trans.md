---
title: Onlineauftrag und asynchrone Debitorenauftragstransaktionen bearbeiten und prüfen
description: In diesem Thema wird beschrieben, wie Sie Onlineaufträge und asynchrone Debitorenauftragstransaktionen in Microsoft Dynamics 365 Commerce bearbeiten und prüfen.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: b9f2db25c8897662baa177752d0c5fc4ac6178a4
ms.sourcegitcommit: ce51ff2b6099c75dceb99de6dea9d53baf99772d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "4459121"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a>Onlineauftrag und asynchrone Debitorenauftragstransaktionen bearbeiten und prüfen

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie Onlineaufträge und asynchrone Debitorenauftragstransaktionen in Microsoft Dynamics 365 Commerce bearbeiten und prüfen.

## <a name="overview"></a>Übersicht

Von Commerce-Version 10.0.5 auf 10.0.6 wurde Unterstützung für die Bearbeitung von Abholungstransaktionen (z. B. Verkäufe und Retouren) sowie Bargeldverwaltungstransaktionen (z. B. Entfernen von Mittelzugängen und Zahlungsmitteln) hinzugefügt. In Commerce Version 10.0.7 wurde Unterstützung für das Bearbeiten von Onlineauftragstransaktionen und asynchronen Debitorenauftragstransaktionen hinzugefügt.

## <a name="edit-and-audit-order-transactions"></a>Auftragstransaktionen bearbeiten und prüfen

Führen Sie die folgenden Schritte aus, um Auftragstransaktionen in der Commerce-Zentralverwaltung zu bearbeiten und zu prüfen.

1. Installieren Sie das [Microsoft Dynamics Office-Add-In](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).
1. Legen Sie auf der Seite **Einzelhandelsparameter**, der Registerkarte **Debitorenaufträge**, im Inforegister **Auftrag** einen Sperrcode für **Code bei Auftragssynchronisierungsfehler sperren** fest.
1. Öffnen Sie den Arbeitsbereich **Finanzdaten für Shop**. Die Kacheln **Onlineauftragssynchronisierungsfehler** und **Debitorenauftragssynchronisierungsfehler** bieten eine vorgefilterte Ansicht der Einzelhandelstransaktionsseite. Es werden die Transaktionsdatensätze angezeigt, bei denen die Synchronisierung des entsprechenden Auftragstyps fehlgeschlagen ist.
1. Öffnen Sie entweder die Seite **Onlineauftragssynchronisierungsfehler** oder die Seite **Debitorenauftragssynchronisierungsfehler**. Wählen Sie einen Datensatz aus, um die Details des Synchronisationsfehlers anzuzeigen. Das Inforegister **Synchronisierungsstatus** bietet folgende Fehlerdetails:

    - Status des ausstehenden Auftrags
    - Auftragsfehlerdetails
    - Änderungsdatum und -uhrzeit
    - Anzahl von Wiederholungen

1. Wenn der Datensatz laut Fehlerdetails repariert werden muss, wählen Sie **Office-Add-In** und anschließend **Ausgewählte Transaktion bearbeiten** aus. Es öffnet sich eine Excel-Datei mit den Details der ausgewählten Transaktion.

    - Wenn es sich bei der zu bearbeitenden Transaktion um eine Onlineauftragstransaktion handelt, enthält die Excel-Datei folgende Arbeitsblätter:

        - **Transaktion** – Dieses Arbeitsblatt enthält die Kopfzeilendetails der Transaktion.
        - **Verkaufstransaktion** – Dieses Arbeitsblatt enthält die Positionsdetails der Transaktion.
        - **Zahlungstransaktionen** – Dieses Arbeitsblatt enthält die Details der Zahlungspositionen der Transaktion.
        - **Rabatttransaktionen** – Dieses Arbeitsblatt enthält die rabattbezogenen Details der Transaktion.
        - **Steuertransaktionen** – Dieses Arbeitsblatt enthält die steuerlichen Details der Transaktion.
        - **Belastungsbuchungen** – Dieses Arbeitsblatt enthält die belastungsbezogenen Daten der Transaktion.

    - Wenn es sich bei der zu bearbeitenden Transaktion um eine asynchrone Debitorenauftragstransaktion handelt, enthält die Excel-Datei folgende Arbeitsblätter:

        - **Positionen** – Dieses Arbeitsblatt enthält die Kopfzeilen- und Positionsdetails der Transaktion.
        - **Zahlungen** – Dieses Arbeitsblatt enthält die Details der Zahlungspositionen der Transaktion.
        - **Rabatte** – Dieses Arbeitsblatt enthält die rabattbezogenen Details der Transaktion.
        - **Steuern** – Dieses Arbeitsblatt enthält die steuerlichen Details für die Transaktion.
        - **Gebühren** – Dieses Arbeitsblatt enthält die belastungsbezogenen Daten der Transaktion.

1. Geben Sie **Bearbeitung** in der Excel-Datei im Feld **Status des ausstehenden Auftrags** ein, und veröffentlichen Sie dann die Änderung. Auf diese Weise verhindern Sie, dass der Einzelvorgang **Auftrag synchronisieren**, der im Batchmodus ausgeführt wird, diesen Datensatz bei der Bearbeitung überspringt.
1. Ändern Sie die entsprechenden Felder in der Excel-Datei, und laden Sie die Daten dann mit Hilfe der Veröffentlichungsfunktion des Dynamics Excel-Add-Ins wieder in die Commerce-Zentralverwaltung hoch. Sobald die Daten veröffentlich sind, werden die Änderungen im System berücksichtigt. Während der Veröffentlichung wird keine Überprüfung der von den Benutzern vorgenommenen Änderungen durchgeführt.
1. Sie können sich ein vollständiges Protokoll der Änderungen anzeigen lassen, indem Sie **Audit-Trail anzeigen** in der **Einzelhandelstransaktion**-Kopfzeile (Änderungen auf Kopfzeilenebene) oder in den entsprechenden Abschnitt und Datensatz auswählen. Beispielsweise werden alle Änderungen, die sich auf Verkaufspositionen beziehen, auf der Seite **Verkaufstransaktionen** angezeigt, und alle Änderungen, die sich auf Zahlungen beziehen, werden auf der Seite **Zahlungstransaktionen** angezeigt. Die folgenden Prüfungsdetails werden für die Änderungen beibehalten:

    - Änderungsdatum und -uhrzeit
    - Feld
    - Alter Wert
    - Neuer Wert
    - Geändert von

1. Sobald Sie Ihre Änderungen vorgenommen und veröffentlicht haben, wählen Sie **Auftrag synchronisieren** aus, um den Synchronisierungsprozess sofort zu starten. Alternativ können Sie auf den Synchronisierungsprozess warten, der im Batchmodus ausgeführt wird, um die Transaktion zu verarbeiten.

Sobald die Aufträge erfolgreich synchronisiert wurden, werden sie standardmäßig in einen Wartestatus versetzt, basierend auf dem in den Commerce-Parametern definierten Sperrcode. Das Zurückhalten der Aufträge muss aufgehoben werden, bevor die Aufträge zur Erfüllung oder für andere Vorgänge weiter verarbeitet werden können.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Abholungs- und Bargeldverwaltungstransaktionen bearbeiten und prüfen](edit-cash-trans.md)

[Finanzdimensionen für Einzelhandelstransaktionen bearbeiten](edit-financial-dim.md)

[Excel-Arbeitsmappe zum Bearbeiten von Einzelhandelstransaktionen erstellen](create-excel-edit.md)

[Einer Excel-Arbeitsmappe zum Bearbeiten von Einzelhandelstransaktionen Felder hinzufügen](add-fields-excel.md)
