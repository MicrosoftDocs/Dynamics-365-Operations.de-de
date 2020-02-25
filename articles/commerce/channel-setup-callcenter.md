---
title: Einen Callcenterkanal einrichten
description: In diesem Thema wird beschrieben, wie ein Callcenterkanal in Microsoft Dynamics 365 Commerce erstellt wird.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6ec42ab920868f541eeac54556f4f24cb1efaa3a
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002449"
---
# <a name="set-up-a-call-center-channel"></a>Einen Callcenterkanal einrichten


[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie ein Callcenterkanal in Microsoft Dynamics 365 Commerce erstellt wird.

## <a name="overview"></a>Übersicht

In Dynamics 365 Commerce ist ein Callcenter ein Retail Channel-Typ, der in der Anwendung definiert werden kann. Durch das Definieren eines Kanals für Ihre Callcenter-Entitäten kann das System bestimmte Daten und Auftragsverarbeitungsstandards mit Aufträgen verknüpfen. Ein Unternehmen kann Callcenterkanäle in Commerce definieren. 

Vergewissern Sie sich vor dem Erstellen eines neuen Callcenterkanals, dass Sie die [Voraussetzungen für die Kanaleinrichtung](channels-prerequisites.md) erfüllen.

## <a name="create-and-configure-a-new-call-center-channel"></a>Einen neuen Callcenterkanal erstellen und konfigurieren

Um einen Callcenterkanal zu erstellen und zu konfigurieren, führen Sie die folgenden Schritte aus.

1. Gehen Sie im Navigationsbereich zu **Module \> Kanäle \> Callcenter \>Alle Callcenter**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Geben Sie im Feld **Name** einen Namen für den neuen Kanal ein.
1. Wählen Sie die entsprechende **Juristische Person** aus dem Dropdown aus.
1. Wählen Sie den entsprechenden Standort des **Lagerorts** aus dem Dropdown aus.
1. Geben Sie im Feld **Standardkunde** einen gültigen Standardkunden an.
1. Geben Sie in das Feld **E-Mail-Benachrichtigungsprofil** ein gültiges E-Mail-Benachrichtigungsprofil ein.
1. Geben Sie einen Infocode **Preisüberschreibung** an. Beachten Sie, dass Sie möglicherweise zuerst einen Infocode dafür erstellen müssen.
1. Geben Sie einen Infocode **Code halten** ein. Beachten Sie, dass Sie möglicherweise zuerst einen Infocode dafür erstellen müssen.
1. Geben Sie einen Infocode **Haben** ein. Beachten Sie, dass Sie möglicherweise zuerst einen Infocode dafür erstellen müssen.
1. Wählen Sie **Speichern**.

Das folgende Bild zeigt die Erstellung eines neuen Callcenterkanals.

![Neuer Callcenterkanal](media/channel-setup-callcenter-1.png)

Das folgende Bild zeigt ein Beispiel für einen Callcenterkanal.

![Beispiel eines Callcenterkanals](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a>Einrichtung eines zusätzlichen Kanals

Zusätzliche Aufgaben, die für das Einrichten des Callcenterkanals erforderlich sind, umfassen das Einrichten von Zahlungsmethoden und Lieferarten.

Das folgende Bild zeigt die Einrichtungsoptionen **Lieferarten** und **Zahlungsmethoden** auf der Registerkarte **Einrichten**.

![Zusätzliche Aktionen zum Einrichten von Callcenterkanälen](media/channel-setup-callcenter-3.png)

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

### <a name="set-up-modes-of-delivery"></a>Lieferarten einrichten

Sie können die konfigurierten Zustellmodi anzeigen, indem Sie **Lieferarten** aus der Registerkarte **Einrichten** im **Aktionsbereich** auswählen.  

Gehen Sie folgendermaßen vor, um eine Lieferart zu ändern oder hinzuzufügen.

1. Gehen Sie im Navigationsbereich zu **Module \> Bestandsverwaltung \> Lieferarten**.
1. Wählen Sie im Aktionsbereich **Neu** aus, um eine neue Lieferart zu erstellen oder wählen Sie einen vorhandenen Modus aus.
1. Im Abschnitt **Retail Channels** wählen Sie **Zeile hinzufügen** aus, um den Kanal hinzuzufügen. Durch das Hinzufügen von Kanälen mithilfe von Organisationsknoten, anstatt jeden Kanal einzeln hinzuzufügen, kann das Hinzufügen von Kanälen rationalisiert werden.

Das folgende Bild zeigt ein Beispiel für eine Lieferart.

![Lieferarten einrichten](media/channel-setup-retail-7.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Voraussetzungen der Kanaleinrichtung](channels-prerequisites.md)

[Callcenter-Vertriebsfunktionen](call-center-functionality.md)

[Callcenter-Auftragsabwicklungsoptionen einrichten](set-up-order-processing-options.md)

[Callcenterkataloge](call-center-catalogs.md)

[Einrichten und Verwenden von Betrugswarnungen](set-up-fraud-alerts.md)

[Einrichten von Anschlussprogrammen für Callcenter](set-up-continuity-program.md)
