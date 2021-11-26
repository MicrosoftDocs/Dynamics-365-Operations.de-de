---
title: Metriken für IoT-Intelligenz einrichten
description: In diesem Thema wird erläutert, wie Sie Metriken für IoT-Intelligenz einrichten.
author: tonyafehr
ms.date: 04/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85db0211c32ad4e27c3a9a65d2c74c5a39687f9c
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783097"
---
# <a name="set-up-metrics-for-iot-intelligence"></a>Metriken für IoT-Intelligenz einrichten

[!include [banner](../../includes/banner.md)]

## <a name="configure-metrics"></a>Konfigurieren von Metriken

Wenn Sie die Zeitreihendiagramme Ihrer Nachrichten in Microsoft Dynamics 365 Supply Chain Management anzeigen möchten, müssen Sie die Metriken wie folgt einrichten.

1. Kopieren Sie die Verbindungszeichenfolge für den Redis Cache:

    1. Navigieren Sie im Azure-Portal zum Redis Cache.
    2. Gehen Sie zu **Einstellungen** \> **Zugriffsschlüssel**.
    3. Kopieren Sie den Wert in das Feld **Primäre Verbindungszeichenfolge**.

2. Wechseln Sie in Supply Chain Management zu **Produktionskontrolle \> Einrichtung \> IoT-Intelligenz \> Szenarioparameter**.
3. Auf der Seite **Szenarioparameter** in der Registerkarte **Zeitreihen**  in der **Redis-Metrikspeicher-Verbindungszeichenfolge** fügen Sie die zuvor kopierte Verbindungszeichenfolge ein. Dieser Schritt ermöglicht die Visualisierung der Metriken von Azure IoT Hub in Supply Chain Management. Wenn Sie den Wert in das Feld einfügen, wird er als **\*\*\*\*\*\*** angezeigt.

    > [!NOTE]
    > Wenn Sie eine die Redis-Cache-Verbindungszeichenfolge aktualisieren, müssen Sie auch dieses Feld aktualisieren.

4. Gehen Sie zu **Produktionskontrolle \> Anfragen und Berichte \> IoT-Intelligenz \> Metrikschlüssel**.
5. Wählen Sie auf der Seite **Metrikschlüssel** **Aktualisieren**.
6. Beachten Sie im Dialogfeld **Metrikschlüssel aktualisieren**, dass **Im Hintergrund ausführen** im Feld ausgewählt ist. Wählen Sie **OK** aus.

Alle Metrikschlüssel im Redis Cache werden abgerufen und der **Metrikschlüssel**-Liste hinzugefügt. Metrikwerte werden erst angezeigt, wenn Sie [die Szenarien aktivieren](iot-scenario-setup.md).

## <a name="configure-the-resource-status-time-series"></a>Konfigurieren der Ressourcenstatuszteitreihe

Folgen Sie diesen Schritten, um die **Ressourcenstatus**-Zeitreihe zu konfigurieren.

1. Gehen Sie im Supply Chain Management zu **Produktionskontrolle \>Fertigungsausführung \>Ressourcenstatus**.
2. Wählen Sie auf der Seite **Ressourcenstatus** **Konfigurieren** aus.
2. wählen Sie im **Konfigurieren**-Dialogfeld, in der **Ressource**-Liste ein zu überwachendes Element aus.
3. Wählen Sie die Schaltfläche **Bearbeiten** für **Zeitreihe 1**.
4. Wählen Sie im Dialogfeld **Zeitreihe auswählen** eine Metrik im Raster aus. (Sie können auch den **Metrikschlüssel aktualisieren**-Link zum Aktualisieren der Metrikschlüssel in diesem Dialogfeld verwenden.)
5. Wählen Sie **OK** aus, um zum Dialogfeld **Konfigurieren** zurückzukehren.
6. Geben Sie einen Anzeigename ein.
7. Wählen Sie im Feld **Daten anzeigen von** einen Zeitrahmen aus.
8. Wählen Sie **OK** aus.

Das Diagramm wird angezeigt.

## <a name="delete-a-metric-key"></a>Einen Metrikschlüssel löschen

1. Gehen Sie in Supply Chain Management zu **Produktionskontrolle \> Anfragen und Berichte \> IoT-Intelligenz \> Metrikschlüssel**.
2. Wählen Sie auf der Seite **Metrikschlüssel** den zu löschenden Metrikschlüssel aus.
3. Wählen Sei **Löschen**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]