---
title: "POS Offlinefunktionalität"
description: "Dieser Artikel enthält Informationen zum Offlinemodus für moderne Einzelhandels-POS fest, in dem POS-Geräte automatisch von der Kanaldatenbank zur Offlinen Datenbank wechseln, wenn der Einzelhandelsserver nicht verfügbar ist. Dieser Artikel umfasst auch Informationen zu den allgemeinen Einstellungen für den Offline-Modus und erklärt die Datensynchronisierung, die zwischen der Offline-Datenbank und der Kanaldatenbank erfolgt."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 27041
ms.assetid: 20b51874-8912-40cf-9296-864df707315a
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ef4d20b3302e4a420c7013b77a57ebdfa99fe6a3
ms.lasthandoff: 03/31/2017


---

# <a name="pos-offline-functionality"></a>POS Offlinefunktionalität

[!include[banner](includes/banner.md)]


Dieser Artikel enthält Informationen zum Offlinemodus für moderne Einzelhandels-POS fest, in dem POS-Geräte automatisch von der Kanaldatenbank zur Offlinen Datenbank wechseln, wenn der Einzelhandelsserver nicht verfügbar ist. Dieser Artikel umfasst auch Informationen zu den allgemeinen Einstellungen für den Offline-Modus und erklärt die Datensynchronisierung, die zwischen der Offline-Datenbank und der Kanaldatenbank erfolgt.

<a name="overview"></a>Überblick
--------

In Retail Modern POS ein Verkaufsstelle (POS)-Gerät in Ausführen eines indirekten, sobald der Retail Server nicht verfügbar ist. Daher, wenn die Verbindung mit dem Retail-Server verloren geht, wird Retail Modern POS automatisch zur Offlinedatenbank gewechselt. Wenn eine Datenanforderung während einer Verkaufsbuchung nicht innerhalb des Timeoutintervalls, das im Offline-Profil konfiguriert wurde, erfolgreich ist, schaltet der Retail Modern POS automatisch auf die Offlinen Datenbank um und setztdie Verkaufsbuchung fort. Während das POS-Gerät im Offline-Modus ist, versucht der Retail Modern POS die Verbindung zum Einzelhandel-Server gemäß der im Offline-Profil konfigurierten Intervalle für Wiederverbindungsversuche wieder herzustellen. Dieser Wiederverbindungsversuch tritt nur am Anfang einer Transaktion auf.

### <a name="determining-the-connection-mode-of-retail-modern-pos"></a>Den Anschlussmodus von Retail Modern POS bestimmen

Die Statuskopfzeile im Retail Modern POS gibt den aktuellen Verbindungsstatus an und die das Fenster **Verbindungsstatus** zeigt den Status des letzten Versuchs der Synchronisation mit der Offline-Datenbank an. [![Verbindungsstatus](./media/status.png)](./media/status.png)

### <a name="creating-a-button-to-manually-switch-between-online-and-offline-modes"></a>Erstellen einer Schaltfläche, um manuell zwischen Online- und Offline-Modus zu wechseln

Sie können eine Schaltfläche zum Retail Modern POS hinzufügen, um manuell zwischen Online- und Offline-Modus zu wechseln. Erstellen Sie eine Schaltfläche für den POS-Vorgang **917 - Datenbankverbindungsstatus**. Der Name dieser Schaltfläche ist, **Trennen** wenn der Retail Modern POS mit einem Einzelhandel-Server verbunden ist und **Verbinden** er getrennt wurde. Sie können diese Schaltfläche verwenden, um die Verbindung anzuzeigen und sie vom Einzelhandel-Server zu trennen oder sie herzustellen. [![Schaltfläche "Trennen" im Retail Modern POS](./media/details-1024x537.png)](./media/details.png)

## <a name="setup"></a>Einrichten
Um Unterstützung offline für ein POS-Gerät (Register ) zu aktivieren, wählen Sie die **Offlineunterstützung** Option auf **Ja** auf der **Register** Seite aus. Eine neue Kanaldatenbankentität wird der Kanaldatengruppe der Filiale erstellt und hinzugefügt. Führen Sie dann alle erforderlichen Verteilungszeitpläne aus, um die Datenpakete für die Offline-Datenbank zu generieren. Richten Sie die modernen offline Version von Retail Modern POS. Der Installationsprozess erstellt offline die Datenbank. Darüber hinaus müssen Sie Microsoft SQL Server 2014 Express, sofern dies erforderlich ist. Die Offline-Datensynchronisierung beginnt nach der ersten Anmeldung im Retail Modern POS.

## <a name="data-synchronization"></a>Datensynchronisierung
Das Einzelhandel-Steuerprogramm wird verwendet, um Masterdaten an die Offline-Datenbank zu senden. Wenn ein Vertriebsplan ausgeführt wird, werden Datenänderungen standardmäßig sowohl an die Kanaldatenbank als auch die Offline-Datenbank gesendet. Retail Modern POS enthält die Async-Synchronisierungsbibliothek, die alle verfügbaren Datenpakete herunterlädt und sie in die Offline-Datenbank einfügt. Wenn Transaktionen offline erstellt werden, lädt Retail Modern POS sie auf den Einzelhandel-Server, damit sie in die Kanaldatenbank eingefügt werden können. Offline-Datensynchronisierung ist nur möglich, wenn Retail Modern POS ausgeführt wird. [![Offlinesynchronisierung](./media/offline-sync-1024x521.png)](./media/offline-sync.png)




