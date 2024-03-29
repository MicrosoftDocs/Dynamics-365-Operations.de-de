---
title: Einen Onlinechannel einrichten
description: In diesem Artikel wird beschrieben, wie Sie einen neuen Onlinechannel in Microsoft Dynamics 365 Commerce erstellen.
author: samjarawan
ms.date: 02/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: be9fafe8ece771ad6577db1cdb70af6f48e054cc
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272879"
---
# <a name="set-up-an-online-channel"></a>Einen Onlinechannel einrichten

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie einen neuen Onlinechannel in Microsoft Dynamics 365 Commerce erstellen.

Dynamics 365 Commerce unterstützt mehrere Retail Channels. Diese Vertriebskanäle umfassen Onlineshops, Callcenter und Einzelhandelsgeschäfte (auch physische Läden genannt). Onlineshops geben Kunden die Gelegenheit, Produkte über die Onlinepräsenz des Einzelhändlers sowie aus dessen Einzelhandelsgeschäften zu erwerben.

Um einen Onlineshop in Commerce zu erstellen, müssen Sie zunächst einen Onlinechannel erstellen. Vergewissern Sie sich vor dem Erstellen eines neuen Onlinechannels, dass Sie die [Voraussetzungen für die Kanaleinrichtung](channels-prerequisites.md) erfüllen.

Bevor Sie eine neue Site erstellen können, muss mindestens ein Onlineshop in Commerce erstellt werden. Weitere Informationen finden Sie unter [Erstellen einer E-Commerce-Webseite](create-ecommerce-site.md).

## <a name="create-and-configure-a-new-online-channel"></a>Einen neuen Onlinechannel erstellen und konfigurieren

Um einen Onlinechannel zu erstellen und zu konfigurieren, führen Sie die folgenden Schritte aus.

1. Gehen Sie im Navigationsbereich zu **Module \> Kanäle \> Onlineshops**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Geben Sie im Feld **Name** einen Namen für den neuen Kanal ein.
1. Geben Sie im Dropdown **Juristische Person** die entsprechende juristische Person ein.
1. Geben Sie im Dropdown **Lagerort** den entsprechenden Lagerort ein.
1. Wählen Sie im Feld **Zeitzone des Shops** die entsprechende Zeitzone aus.
1. Wählen Sie im Feld **Währung** die entsprechende Währung aus.
1. Geben Sie im Feld **Standardkunde** einen gültigen Standardkunden an.
1. Geben Sie im Feld **Kundenadressbuch** ein gültiges Adressbuch an.
1. Wählen Sie im Feld **Funktionsprofil** gegebenenfalls ein Funktionsprofil aus.
1. Geben Sie in das Feld **E-Mail-Benachrichtigungsprofil** ein gültiges E-Mail-Benachrichtigungsprofil ein.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

Das folgende Bild zeigt die Erstellung eines neuen Onlinechannel.

![Neuer Onlinechannel.](media/channel-setup-online-1.png)

Das folgende Bild zeigt ein Beispiel für einen Onlinechannel.

![Beispiel-Onlinechannel.](media/channel-setup-online-2.png)

## <a name="assign-the-channel-to-a-commerce-scale-unit"></a>Weisen Sie den Kanal einer Commerce Scale Unit zu

Ihr neuer Channel muss einer Commerce Scale Unit zugewiesen werden. Anweisungen finden Sie unter [Kanäle für die Verwendung von Commerce Scale Unit konfigurieren](../fin-ops-core/dev-itpro/deployment/initialize-retail-channels.md#configure-channels-to-use-commerce-scale-unit).

## <a name="set-up-languages"></a>Sprachen einrichten

Wenn Ihre E-Commerce Website mehrere Sprachen unterstützt, erweitern Sie den Abschnitt **Sprachen** und fügen Sie bei Bedarf weitere Sprachen hinzu.

## <a name="set-up-payment-account"></a>Zahlungskonto einrichten

Aus dem Abschnitt **Zahlungskonto** können Sie einen Drittanbieter für Zahlungen hinzufügen. Mehr Informationen zum Einrichten eines Adyen-Zahlungskonnektors finden Sie unter [Dynamics 365 Adyen-Zahlungskonnektor](./dev-itpro/adyen-connector.md).

## <a name="additional-channel-setup"></a>Einrichtung eines zusätzlichen Kanals

Zusätzliche Aufgaben, die für das Einrichten des Onlinechannel erforderlich sind, umfassen das Einrichten von Zahlungsmethoden, die Lieferarten und die Erfüllungsgruppenzuweisungen.

Das folgende Bild zeigt die Einrichtungsoptionen **Lieferarten**, **Zahlungsmethoden** und **Zuordnung der Erfüllungsgruppen** auf der Registerkarte **Installieren**.

![Zusätzliche Aktionen zum Einrichten von Onlinechannels.](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a>Einrichten von Zahlungsmethoden

Führen Sie die folgenden Schritte aus, um die Zahlungsmethoden für jede auf diesem Kanal unterstützte Zahlungsart einzurichten.

1. Wählen Sie im Aktionsbereich die Registerkarte **Einrichten** und dann **Zahlungsmethoden**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Wählen Sie im Navigationsbereich eine gewünschte Zahlungsmethode aus.
1. Geben Sie im Abschnitt **Allgemeines** einen **Operationsname** an und konfigurieren Sie alle anderen gewünschten Einstellungen.
1. Konfigurieren Sie ggf. zusätzliche Einstellungen für die Zahlungsart.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

Das folgende Bild zeigt ein Beispiel für eine Bargeldzahlungsmethode.

![Beispielzahlungsmethoden.](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a>Lieferarten einrichten

Sie können die konfigurierten Zustellmodi anzeigen, indem Sie **Lieferarten** aus der Registerkarte **Einrichten** im **Aktionsbereich** auswählen.  

Gehen Sie folgendermaßen vor, um eine Lieferart zu ändern oder hinzuzufügen.

1. Gehen Sie im Navigationsbereich zu **Module \> Lagerverwaltung \> Lieferarten**.
1. Wählen Sie im Aktionsbereich **Neu** aus, um eine neue Lieferart zu erstellen oder wählen Sie einen vorhandenen Modus aus.
1. Im Abschnitt **Retail Channels** wählen Sie **Zeile hinzufügen** aus, um den Kanal hinzuzufügen. Durch das Hinzufügen von Kanälen mithilfe von Organisationsknoten, anstatt jeden Kanal einzeln hinzuzufügen, kann das Hinzufügen von Kanälen rationalisiert werden.

Das folgende Bild zeigt ein Beispiel für eine Lieferart.

![Lieferarten einrichten.](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a>Eine Erfüllungsgruppenzuweisung einrichten

Gehen Sie zum Einrichten einer Erfüllungsgruppe folgendermaßen vor:

1. Wählen Sie im Aktionsbereich die Registerkarte **Einrichten** und dann **Erfüllungsgruppenzuweisung** aus.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Wählen Sie in der Dropdown-Liste **Erfüllungsgruppe** eine Erfüllungsgruppe aus.
1. Geben Sie in der Dropdown-Liste **Beschreibung** eine Beschreibung ein.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

Die folgende Abbildung zeigt ein Beispiel für die Einrichtung einer Erfüllungsgruppenzuweisung.

![Erfüllungsgruppenzuweisung einrichten.](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über Kanäle](channels-overview.md)

[Kanaleinstellungen – Voraussetzungen](channels-prerequisites.md)

[Einen Retail Channel einrichten](channel-setup-retail.md)

[Einen Callcenterkanal einrichten](channel-setup-callcenter.md)

[Connector für Adyen-Zahlungen für Dynamics 365](./dev-itpro/adyen-connector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
