---
title: Einen Einzelhandelskanal einrichten
description: In diesem Thema wird beschrieben, wie Sie einen neuen Retail Channel in Microsoft Dynamics 365 Commerce erstellen.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 713cbe68c151b6893519843611089941cabf0e70
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800590"
---
# <a name="set-up-a-retail-channel"></a>Einen Retail Channel einrichten

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie einen neuen Retail Channel in Microsoft Dynamics 365 Commerce erstellen.

Dynamics 365 Commerce unterstützt mehrere Retail Channels. Diese Vertriebskanäle umfassen Onlineshops, Callcenter und Einzelhandelsgeschäfte (auch physische Läden genannt). Jeder Einzelhandelskanal kann seine eigenen Zahlungsmethoden, Preisgruppen, POS-Register, Ein- und Ausgabenkonten und Mitarbeiter einrichten. Sie müssen alle Elemente einrichten, bevor Sie ein Ladengeschäftskanal erstellen können. 

Stellen Sie vor dem Erstellen eines Retail Channel sicher, dass Sie die folgenden [Kanalvoraussetzungen](channels-prerequisites.md) befolgen.

## <a name="create-and-configure-a-new-retail-channel"></a>Einen neuen Retail Channel erstellen und konfigurieren

1. Gehen Sie im Navigationsbereich zu **Module \> Kanäle \> Geschäfte \>Alle Geschäfte**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Geben Sie im Feld **Name** einen Namen für den neuen Kanal ein.
1. Wählen Sie im Feld **Shopnummer** eine einmalige Shopnummer aus. Die Nummer kann alphanumerisch mit maximal 10 Zeichen sein.
1. Geben Sie in der Dropdown-Liste **Juristische Person** die entsprechende juristische Person ein.
1. Geben Sie in der Dropdown-Liste **Lagerort** den entsprechenden Lagerort ein.
1. Wählen Sie im Feld **Zeitzone des Shops** die entsprechende Zeitzone aus.
1. Wählen Sie in der Dropdown-Liste **Umsatzsteuergruppe** eine entsprechende Umsatzsteuergruppe für das Geschäft aus.
1. Wählen Sie im Feld **Währung** die entsprechende Währung aus.
1. Geben Sie im Feld **Kundenadressbuch** ein gültiges Adressbuch an.
1. Geben Sie im Feld **Standardkunde** einen gültigen Standardkunden an.
1. Wählen Sie im Feld **Funktionsprofil** gegebenenfalls ein Funktionsprofil aus.
1. Geben Sie in das Feld **E-Mail-Benachrichtigungsprofil** ein gültiges E-Mail-Benachrichtigungsprofil ein.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

Das folgende Bild zeigt die Erstellung eines neuen Retail Channel.

![Neuer Retail Channel](media/channel-setup-retail-1.png)

Das folgende Bild zeigt ein Beispiel für einen Retail Channel.

![Beispiel für einen Retail Channel](media/channel-setup-retail-2.png)

## <a name="other-settings"></a>Andere Einstellungen

Es gibt zahlreiche andere optionale Einstellungen, die in den Abschnitten **Auszug/Abschluss** und **Sonstiges** basierend auf den Bedürfnissen des Einzelhandelsgeschäfts eingestellt werden können.

Darüber hinaus siehe [Bildschirmlayouts für den Point of Sale (POS)](pos-screen-layouts.md)für Informationen zum Einrichten des Standard-Bildschirmlayouts im Abschnitt **Bildschirmlayout** und [konfigurieren und installieren Sie die Retail Hardware station](retail-hardware-station-configuration-installation.md) für Informationen zum Einrichten über den Abschnitt **Hardwarestationen**.

Das folgende Bild zeigt ein Beispiel für einen Retail Channel-Einrichtungskonfiguration.

![Retail Channel-Beispielkonfiguration](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a>Einrichtung eines zusätzlichen Kanals

Für einen Kanal, der im **Aktionsbereich** im Abschnitt **Einrichtung** zu finden ist, müssen zusätzliche Elemente eingerichtet werden.

Zusätzliche Aufgaben, die für das Einrichten des Onlinekanals erforderlich sind, umfassen das Einrichten von Zahlungsmethoden, Bargelddeklaration, Lieferarten, Einnahmen-/Aufwandskonto, Abteilungen, Erfüllungsgruppenzuweisungen und Safes.

Das folgende Bild zeigt verschiedene zusätzliche Optionen zum Einrichten von Retail Channels auf der Registerkarte **Einrichten**.

![Kanal einrichten](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a>Einrichten von Zahlungsmethoden

Führen Sie die folgenden Schritte aus, um die Zahlungsmethoden für jede auf diesem Kanal unterstützte Zahlungsart einzurichten.

1. Wählen Sie im Aktionsbereich die Registerkarte **Einrichten** und dann **Zahlungsmethoden**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Wählen Sie im Navigationsbereich eine gewünschte Zahlungsmethode aus.
1. Geben Sie im Abschnitt **Allgemeines** einen **Operationsname** an und konfigurieren Sie alle anderen gewünschten Einstellungen.
1. Konfigurieren Sie ggf. zusätzliche Einstellungen für die Zahlungsart.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

Das folgende Bild zeigt ein Beispiel für eine Bargeldzahlungsmethode.

![Beispielzahlungsmethoden](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a>Bargelddeklaration einrichten

1. Wählen Sie im Aktionsbereich die Registerkarte **Einrichten** und dann **Bargelddeklaration**.
1. Wählen Sie im Aktionsbereich **Neu** aus und erstellen Sie dann alle zutreffenden Denominationen **Münze** und **Hinweis**.

Das folgende Bild zeigt ein Beispiel für eine Bargelddeklaration.

![Bargelddeklarationen einrichten](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a>Lieferarten einrichten

Sie können die konfigurierten Zustellmodi anzeigen, indem Sie **Lieferarten** aus der Registerkarte **Einrichten** im **Aktionsbereich** auswählen.  

Gehen Sie folgendermaßen vor, um eine Lieferart zu ändern oder hinzuzufügen.

1. Gehen Sie im Navigationsbereich zu **Module \> Bestandsverwaltung \> Lieferarten**.
1. Wählen Sie im Aktionsbereich **Neu** aus, um eine neue Lieferart zu erstellen oder wählen Sie einen vorhandenen Modus aus.
1. Im Abschnitt **Retail Channels** wählen Sie **Zeile hinzufügen** aus, um den Kanal hinzuzufügen. Durch das Hinzufügen von Kanälen mithilfe von Organisationsknoten, anstatt jeden Kanal einzeln hinzuzufügen, kann das Hinzufügen von Kanälen rationalisiert werden.

Das folgende Bild zeigt ein Beispiel für eine Lieferart.

![Lieferarten einrichten](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a>Einnahmen-/Aufwandskonto einrichten

Gehen Sie zum Einrichten eines Einnahmen-/Aufwandskontos folgendermaßen vor:

1. Wählen Sie im Aktionsbereich die Registerkarte **Einrichten** und dann **Einnahmen-/Aufwandskonto**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Geben Sie unter **Name** einen Namen ein.
1. Geben Sie unter **Suchbegriff** einen Suchbegriff ein.
1. Geben Sie unter **Kontenart** die Kontenart ein.
1. Geben Sie den Text für die **Meldungszeile 1**, **Meldungszeile 2**, **Belegtext 1** und **Belegtext 2** ein.
1. Geben Sie unter **Posten** die Buchungsinformationen ein.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

Die folgende Abbildung zeigt ein Beispiel für ein Einnahmen-/Ausgabenkonto.

![Einnahmen-/Aufwandskonten einrichten](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a>Abschnitte einrichten

Gehen Sie zum Einrichten von Abschnitten folgendermaßen vor:

1. Wählen Sie im Aktionsbereich die Registerkarte **Einrichten** aus und klicken Sie dann auf **Abschnitte**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Geben Sie unter **Abschnittsnummer** eine Abschnittsnummer ein.
1. Geben Sie unter **Beschreibung** eine Beschreibung ein.
1. Geben Sie unter **Abschnittsgröße** eine Abschnittsgröße ein.
1. Konfigurieren Sie zusätzliche Einstellungen für **Allgemeines** und **Verkaufsstatistik**.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

### <a name="set-up-a-fulfillment-group-assignment"></a>Eine Erfüllungsgruppenzuweisung einrichten

Gehen Sie zum Einrichten einer Erfüllungsgruppe folgendermaßen vor:

1. Wählen Sie im Aktionsbereich die Registerkarte **Einrichten** und dann **Erfüllungsgruppenzuweisung** aus.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Wählen Sie in der Dropdown-Liste **Erfüllungsgruppe** eine Erfüllungsgruppe aus.
1. Geben Sie in der Dropdown-Liste **Beschreibung** eine Beschreibung ein.
1. Wählen Sie im Aktionsbereich **Speichern** aus

Die folgende Abbildung zeigt ein Beispiel für die Einrichtung einer Erfüllungsgruppenzuweisung.

![Erfüllungsgruppenzuweisung einrichten](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a>Safes einrichten

Gehen Sie zum Einrichten von Safes folgendermaßen vor:

1. Wählen Sie im Aktionsbereich die Registerkarte **Einrichten** aus und klicken Sie dann auf **Safes**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Geben Sie einen Namen für den Safe ein.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Kanalübersicht](channels-overview.md)

[Voraussetzungen der Kanaleinrichtung](channels-prerequisites.md)

[Einen Onlinekanal einrichten](channel-setup-online.md)

[Einen Callcenterkanal einrichten](channel-setup-callcenter.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
