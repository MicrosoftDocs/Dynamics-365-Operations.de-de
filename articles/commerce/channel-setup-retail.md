---
title: Einen Einzelhandelskanal einrichten
description: In diesem Thema wird beschrieben, wie Sie einen neuen Retail Channel in Microsoft Dynamics 365 Commerce erstellen.
author: samjarawan
ms.date: 04/23/2021
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
ms.openlocfilehash: 3f1f5dc2c8402d9b6b68a049f804932812eb74c0
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937533"
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

Es gibt zusätzliche Elemente, die für einen Kanal festgelegt werden müssen, die Sie im Aktivitätsbereich unter dem Abschnitt **Einrichten** finden.

Zusätzliche Aufgaben, die für das Einrichten des Onlinekanals erforderlich sind, umfassen das Einrichten von Zahlungsmethoden, Bargelddeklaration, Lieferarten, Einnahmen-/Aufwandskonto, Abteilungen, Erfüllungsgruppenzuweisungen und Safes.

Das folgende Bild zeigt verschiedene zusätzliche Optionen zum Einrichten von Retail Channels auf der Registerkarte **Einrichten**.

![Kanal einrichten](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a>Einrichten von Zahlungsmethoden

Führen Sie die folgenden Schritte aus, um die Zahlungsmethoden für jede auf diesem Kanal unterstützte Zahlungsart einzurichten.

1. Wählen Sie im Aktivitätsbereich die Registerkarte **Einrichten** und wählen Sie dann **Zahlungsmethoden**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Wählen Sie im Navigationsbereich eine gewünschte Zahlungsmethode aus.
1. Geben Sie im Abschnitt **Allgemeines** einen **Operationsname** an und konfigurieren Sie alle anderen gewünschten Einstellungen.
1. Konfigurieren Sie ggf. zusätzliche Einstellungen für die Zahlungsart.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

Das folgende Bild zeigt ein Beispiel für eine Bargeldzahlungsmethode.

![Beispielzahlungsmethoden](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a>Bargelddeklaration einrichten

1. Wählen Sie im Aktivitätsbereich die Registerkarte **Einrichten** und klicken Sie dann auf **Kassenerklärung**.
1. Wählen Sie im Aktivitätsbereich **Neu**, und erstellen Sie dann alle **Münzen** und **Noten**, die in Frage kommen.

Das folgende Bild zeigt ein Beispiel für eine Bargelddeklaration.

![Bargelddeklarationen einrichten](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a>Lieferarten einrichten

Sie können die konfigurierten Lieferarten sehen, indem Sie **Lieferarten** auf der Registerkarte **Einrichten** im Aktivitätsbereich auswählen.  

Gehen Sie folgendermaßen vor, um eine Lieferart zu ändern oder hinzuzufügen.

1. Gehen Sie im Navigationsbereich zu **Module \> Bestandsverwaltung \> Lieferarten**.
1. Wählen Sie im Aktivitätsbereich **Neu**, um eine neue Art der Zustellung zu erstellen, oder wählen Sie eine vorhandene Art aus.
1. Im Abschnitt **Retail Channels** wählen Sie **Zeile hinzufügen** aus, um den Kanal hinzuzufügen. Durch das Hinzufügen von Kanälen mithilfe von Organisationsknoten, anstatt jeden Kanal einzeln hinzuzufügen, kann das Hinzufügen von Kanälen rationalisiert werden.

Das folgende Bild zeigt ein Beispiel für eine Lieferart.

![Lieferarten einrichten](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a>Einnahmen-/Aufwandskonto einrichten

Gehen Sie zum Einrichten eines Einnahmen-/Aufwandskontos folgendermaßen vor:

1. Wählen Sie im Aktivitätsbereich die Registerkarte **Einrichten** und wählen Sie dann **Einnahme-/Ausgabekonto**.
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

1. Wählen Sie im Aktionsbereich die Registerkarte **Einrichten** und klicken Sie auf **Abschnitte**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Geben Sie unter **Abschnittsnummer** eine Abschnittsnummer ein.
1. Geben Sie unter **Beschreibung** eine Beschreibung ein.
1. Geben Sie unter **Abschnittsgröße** eine Abschnittsgröße ein.
1. Konfigurieren Sie zusätzliche Einstellungen für **Allgemeines** und **Verkaufsstatistik**.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

### <a name="set-up-a-fulfillment-group-assignment"></a>Eine Erfüllungsgruppenzuweisung einrichten

Gehen Sie zum Einrichten einer Erfüllungsgruppe folgendermaßen vor:

1. Wählen Sie im Aktivitätsbereich die Registerkarte **Einrichten** und wählen Sie dann **Erfüllungsgruppenzuordnung**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Wählen Sie in der Dropdown-Liste **Erfüllungsgruppe** eine Erfüllungsgruppe aus.
1. Geben Sie in der Dropdown-Liste **Beschreibung** eine Beschreibung ein.
1. Wählen Sie im Aktivitätsbereich **Speichern**.

Die folgende Abbildung zeigt ein Beispiel für die Einrichtung einer Erfüllungsgruppenzuweisung.

![Erfüllungsgruppenzuweisung einrichten](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a>Safes einrichten

Gehen Sie zum Einrichten von Safes folgendermaßen vor:

1. Wählen Sie im Aktionsbereich die Registerkarte **Einrichten** und klicken Sie auf **Sicherheiten**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Geben Sie einen Namen für den Safe ein.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

### <a name="ensure-unique-transaction-ids"></a>Stellen Sie eindeutige Transaktions-IDs sicher

Ab der Commerce-Version 10.0.18 sind die für den Point of Sale (POS) generierten Transaktions-IDs sequenziell und umfassen die folgenden Teile:

- Ein fester Teil, der eine Verkettung von Filial-ID und Terminal-ID ist. 
- Ein sequenzieller Teil, bei dem es sich um eine Sequenz von Zahlen handelt. 

Konkret lautet das Format *{store}-{terminal}-{numbersequence}*. 

Da Transaktions-IDs im Offline- und Online-Modus erzeugt werden können, gab es Fälle, in denen doppelte Transaktions-IDs erzeugt wurden. Das Eliminieren von doppelten Transaktions-IDs erfordert eine Menge manueller Datenkorrekturen. 

Mit Commerce Version 10.0.19 wurde das Format der Transaktions-ID aktualisiert, um den sequenziellen Teil zu entfernen und stattdessen eine 13-stellige Nummer zu verwenden, die durch Berechnung der Zeit in Millisekunden seit 1970 erzeugt wird. Mit dieser Änderung lautet das neue Format der Transaktions-ID *{store}-{terminal}-{millisecondsSince1970}*. Diese Aktualisierung macht die Transaktions-ID nicht-sequentiell und stellt sicher, dass die Transaktions-IDs immer eindeutig sind. 

> [!NOTE]
> Transaktions-IDs sind nur für den internen Systemgebrauch gedacht, sie müssen also nicht fortlaufend sein. In vielen Ländern müssen die Beleg-IDs jedoch sequentiell sein.

Die neue Funktion für das Format der Transaktions-ID kann im Arbeitsbereich **Funktionsverwaltung** aktiviert werden. 

Um die Verwendung neuer Transaktions-IDs zu aktivieren, führen Sie diese Schritte aus:

1. Gehen Sie in der Commerce-Zentrale zu **Systemadministration \> Arbeitsbereiche \> Funktionen verwalten**.
1. Filter für das Modul „Retail und Commerce“.
1. Suchen Sie nach der Funktion **Neue Transaktions-ID aktivieren, um doppelte Transaktions-IDs zu vermeiden**.
1. Wählen Sie die Funktion aus und wählen Sie dann **Jetzt aktivieren** im rechten Fensterbereich.  
1. Gehen Sie zu **Einzelhandel und Handel \> Einzelhandel und Handel IT \> Vertriebsplan**.
1. Führen Sie die Jobs **1070 Kanalkonfiguration** und **1170 POS-Datensatz** aus, um die aktivierte Funktion mit den Filialen zu synchronisieren.
1. Nachdem die Änderungen an die Filialen gesendet wurden, müssen die POS-Terminals geschlossen und erneut geöffnet werden, um das neue Transaktions-ID-Format zu verwenden. 

> [!NOTE]
> Nachdem die Funktion für das neue Transaktions-ID-Format aktiviert ist, können Sie diese Funktion nicht mehr deaktivieren. Wenn es deaktiviert werden muss, wenden Sie sich bitte an den Commerce Support.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über Kanäle](channels-overview.md)

[Kanaleinstellungen – Voraussetzungen](channels-prerequisites.md)

[Einen Onlinekanal einrichten](channel-setup-online.md)

[Einen Callcenterkanal einrichten](channel-setup-callcenter.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
