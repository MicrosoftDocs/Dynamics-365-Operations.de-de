---
title: Onlineauftrag und asynchrone Debitorenauftragstransaktionen bearbeiten und prüfen
description: In diesem Artikel wird beschrieben, wie Onlineauftrags- und asynchrone Debitorenauftragstransaktionen in Microsoft Dynamics 365 Commerce bearbeitet und überwacht werden.
author: josaw1
ms.date: 10/21/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.industry: Retail
ms.openlocfilehash: dbeeff47446c1617da44f34ae56f333717f577a1
ms.sourcegitcommit: 18b7a02c497709e8d9c7b943d82f1fcc3dafa4cd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2022
ms.locfileid: "9712107"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a>Onlineauftrag und asynchrone Debitorenauftragstransaktionen bearbeiten und prüfen

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie Onlineauftrags- und asynchrone Debitorenauftragstransaktionen in Microsoft Dynamics 365 Commerce bearbeitet und überwacht werden.

## <a name="overview"></a>Übersicht

Zwischen den Commerce-Versionen 10.0.5 und 10.0.6 wurde die Unterstützung für die Bearbeitung von Abholungstransaktion (z. B. Verkäufe und Rückgaben) und Zahlungsmanagementtransaktionen (z. B. Bareinlage und Entfernung von Zahlungsmitteln) hinzugefügt. In Commerce Version 10.0.7 wurde Unterstützung für das Bearbeiten von Onlineauftragstransaktionen und asynchronen Debitorenauftragstransaktionen hinzugefügt.

## <a name="edit-and-audit-order-transactions"></a>Auftragstransaktionen bearbeiten und prüfen

Führen Sie die folgenden Schritte aus, um Auftragstransaktionen im Commerce headquarters zu bearbeiten und zu prüfen.

1. Installieren Sie das [Microsoft Dynamics Office Add-In](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).
1. Legen Sie auf der Seite **Commerce-Parameter**, der Registerkarte **Debitorenaufträge**, im Inforegister **Auftrag** einen Sperrcode für **Code bei Auftragssynchronisierungsfehler sperren** fest.
2. Halten Sie andere Auftragssynchronisierungsaufträge an, die mit dem Timing Ihrer Bearbeitung und Prüfung im Konflikt stehen.
3. Öffnen Sie den Arbeitsbereich **Finanzdaten für Shop**. Die Kacheln **Onlineauftragssynchronisierungsfehler** und **Debitorenauftragssynchronisierungsfehler** bieten eine vorgefilterte Ansicht der Einzelhandelstransaktionsseite. Es werden die Transaktionsdatensätze angezeigt, bei denen die Synchronisierung des entsprechenden Auftragstyps fehlgeschlagen ist.
4. Öffnen Sie entweder die Seite **Onlineauftragssynchronisierungsfehler** oder die Seite **Debitorenauftragssynchronisierungsfehler**. Wählen Sie einen Datensatz aus, um die Details des Synchronisationsfehlers anzuzeigen. Das Inforegister **Synchronisierungsstatus** bietet folgende Fehlerdetails:

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
    > [!NOTE]
    > Wenn Sie das Feld, das Sie bearbeiten müssen, nicht finden, gehen Sie wie folgt vor, um das fehlende Feld im Arbeitsblatt hinzuzufügen.
    >   1. Wählen Sie im Data Connector **Entwurf** aus.
    >   1. Wählen Sie das Stiftsymbol neben der Tabelle aus, in der Sie ein Feld hinzufügen möchten.
    >   1. Wählen Sie im Abschnitt **Verfügbare Felder** das Feld aus, und klicken Sie dann auf **Hinzufügen**.
    >   1. Fügen Sie so viele Felder hinzu, wie Sie benötigen, und wählen Sie dann **Aktualisieren** aus.
    >   1. Wenn die Aktualisierung abgeschlossen ist, müssen Sie möglicherweise **Aktualisierung** auswählen, um die Werte zu aktualisieren.

3. Sie können sich ein vollständiges Protokoll der Änderungen anzeigen lassen, indem Sie **Audit-Trail anzeigen** in der **Einzelhandelstransaktion**-Kopfzeile (Änderungen auf Kopfzeilenebene) oder in den entsprechenden Abschnitt und Datensatz auswählen. Beispielsweise werden alle Änderungen, die sich auf Verkaufspositionen beziehen, auf der Seite **Verkaufstransaktionen** angezeigt, und alle Änderungen, die sich auf Zahlungen beziehen, werden auf der Seite **Zahlungstransaktionen** angezeigt. Die folgenden Prüfungsdetails werden für die Änderungen beibehalten:

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
