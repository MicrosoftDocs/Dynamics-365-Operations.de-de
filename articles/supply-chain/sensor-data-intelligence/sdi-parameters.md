---
title: Sensor Data Intelligence-Parameter
description: Dieser Artikel enthält Informationen zu Konfigurationseinstellungen, die auf der Parameterseite von Sensor Data Intelligence verfügbar sind.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreServiceParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 4a6665cc078e54da4ebb7920ec8826352ab7a816
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428364"
---
# <a name="sensor-data-intelligence-parameters"></a>Sensor Data Intelligence-Parameter

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Die **Sensor Data Intelligence-Parameter**-Seite bietet einige Einstellungen, mit denen Sie die Funktion konfigurieren können. Diese Einstellungen umfassen Azure-Verbindungsparameter und einen Parameter für die Lebensdauer von Warnmeldungen, die als Reaktion auf Sensormessungen an Benutzer gesendet werden.

## <a name="read-and-change-connection-details-for-your-azure-iot-solution"></a>Lesen und ändern Sie Verbindungsdetails für Ihre Azure IoT-Lösung

Normalerweise richten Sie Ihre Azure IoT-Lösung ein und verbinden sie mit Microsoft Dynamics 365 Supply Chain Management über die **Azure-Ressourcen bereitstellen und verbinden**-Seite, die Sie durch beide Verfahren führt. (Weitere Informationen finden Sie unter [Bereitstellen einer IoT-Lösung auf Azure](sdi-deploy-iot-solution-on-azure.md) .) Sie können die Verbindungsdetails auch jederzeit im Supply Chain Management anzeigen und bearbeiten, indem Sie diesen Schritten folgen.

1. Gehen Sie zu **Systemadministration \> Einrichten \> Sensor Data Intelligence \> Sensor Data Intelligence-Parameter**.
1. Auf der **Zeitserien**-Registerkarte geben Sie im Feld **Verbindungszeichenfolge für Redis Metric Store** den Wert **Primäre Verbindungszeichenfolge (StackExchange.Redis)** für die Azure IoT-Lösung ein, mit der Sie eine Verbindung herstellen möchten. Weitere Informationen zum Ermitteln dieses Werts finden Sie unter [Bereitstellen einer IoT-Lösung auf Azure](sdi-deploy-iot-solution-on-azure.md).
1. Auf der **Integrationen**-Registerkarte geben Sie im Feld **Client-ID für Azure AD-Anwendung** den Wert **Kunden-ID** für die Azure IoT-Lösung ein, mit der Sie eine Verbindung herstellen möchten. Weitere Informationen zum Ermitteln dieses Werts finden Sie unter [Bereitstellen einer IoT-Lösung auf Azure](sdi-deploy-iot-solution-on-azure.md).

## <a name="set-the-lifetime-of-alert-messages"></a>Legen Sie die Lebensdauer von Warnmeldungen fest

Jedes Mal, wenn Sensor Data Intelligence eine Situation erkennt, die die Aufmerksamkeit des Benutzers erfordert, sendet es eine Benachrichtigung an den entsprechenden Benutzer. Um zu verhindern, dass sich diese Benachrichtigungen im System häufen, sollten Sie sie so einstellen, dass sie nach einigen Tagen ablaufen.

1. Gehen Sie zu **Systemadministration \> Einrichten \> Sensor Data Intelligence \> Sensor Data Intelligence-Parameter**.
1. Geben Sie auf der **Benachrichtigungen**-Registerkarte im Feld **Benachrichtigungstage bis Liveschaltung** die Anzahl der Tage ein, die eine Benachrichtigung aufbewahrt werden soll. Nach Ablauf der angegebenen Zeitspanne wird die Benachrichtigung gelöscht.
