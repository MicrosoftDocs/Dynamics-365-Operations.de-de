---
title: IoT-Intelligenz-Add-In in LCS installieren
description: In diesem Thema wird erläutert, wie Sie das IoT-Intelligenz-Add-In in Microsoft Dynamics Lifecycle Services (LCS) installieren.
author: johanhoffmann
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 12ffa71dc1c2badaffdc2e419a47d855635016f2
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8679022"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a>IoT-Intelligenz-Add-In in LCS installieren

[!include [banner](../../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie das IoT-Intelligenz-Add-In in Microsoft Dynamics Lifecycle Services (LCS) installieren. Beachten Sie, dass Add-Ins nicht in einer Demo-/Testversionsumgebung installiert werden können. Bevor Sie das Add-In installieren können, müssen Sie die [Azure-Ressourcen erstellen](iot-azure-setup.md).

Sie können IoT-Intelligenz einrichten und konfigurieren, ohne Code schreiben zu müssen. Hier sind die grundlegenden Schritte:

1. [Einrichten von Azure-Ressourcen](iot-azure-setup.md) – Erstellen Sie einen IoT-Hub, einen Redis Cache und einen Schlüsseltresor, auf den über Supply Chain Management zugegriffen werden kann.
2. [Nachrichtenschemaformate für IoT Hub](iot-schema-format.md) – Konfigurieren Sie Ihre Geräte zum Senden von Nachrichten an IoT Hub und definieren Sie das Nachrichtenformat JavaScript Object Notation (JSON).
3. Aktivieren Sie in der Funktionsverwaltung das IoT-Intelligenz-Funktions-Flag.
4. Das IoT-Intelligenz-Add-In in Microsoft Dynamics Lifecycle Services (LCS) installieren – Installieren Sie das Add-In in LCS und konfigurieren Sie die Azure-Geheimnisse (wie in diesem Thema beschrieben).
5. [Metriken einrichten](iot-metrics-setup.md) – Richten Sie Metriken im Supply Chain Management ein.
6. [Szenario-Einrichtung](iot-scenario-setup.md) – Richten Sie die Szenarien im Supply Chain Management ein.

## <a name="set-up-the-lcs-environment"></a>LCS-Umgebung einrichten

1. Öffnen Sie LCS, und wechseln Sie zu Ihrer Microsoft Dynamics 365 Supply Chain Management-Umgebung.
2. Scrollen Sie zum Abschnitt **Umgebungs-Add-Ins**.
3. Wählen Sie **Neues Add-In installieren** aus, um die Liste der Add-Ins anzuzeigen, die für die Umgebung aktiviert wurden.
4. Wählen Sie im Dialogfeld **Zu installierendes Add-In auswählen** die Option **IoT-Intelligenz** aus.
5. Geben Sie im Dialogfeld **Add-In einrichten** die Details Ihres IoT-Hubs und Redis-Caches an. Sie finden die erforderlichen Werte im Schlüsseltresor, den Sie unter [Azure-Ressourcen erstellen](iot-azure-setup.md) erstellt haben.

    + **Mandanten-ID** – Wechseln Sie im Azure-Portal zum Schlüsseltresor, wählen Sie dann im linken Navigationsbereich **Übersicht** aus, und kopieren Sie den Wert **Verzeichnis-ID**. Fügen Sie diesen Wert in das Dialogfeld **Add-In einrichten** ein.
    + **Schlüsseltresor-URI des IoT-Event Hub-kompatiblen Endpunkts** – Wechseln Sie zum Schlüsseltresor, wählen Sie dann im linken Navigationsbereich **Übersicht** aus, und kopieren Sie den Wert für **DNS-Name**. Fügen Sie diesen Wert in das Dialogfeld **Add-In einrichten** ein.
    + **Geheimer Schlüssel des IoT-Event-Hub-kompatiblen Endpunkts** – Wechseln Sie zum Schlüsseltresor, wählen Sie dann im linken Navigationsbereich **Geheime Schlüssel** aus, und kopieren Sie den Namen des geheimen Schlüssels, in dem die Event-Hub-Verbindungszeichenfolge für den IoT-Hub gespeichert ist. Fügen Sie diesen Wert in das Dialogfeld **Add-In einrichten** ein.
    + **Schlüsseltresor-URI des Redis-Caches** – Wechseln Sie zum Schlüsseltresor, wählen Sie dann im linken Navigationsbereich **Übersicht** aus, und kopieren Sie den Wert für **DNS-Name**. Fügen Sie diesen Wert in das Dialogfeld **Add-In einrichten** ein.
    + **Name des geheimen Schlüssels des Redis-Cache-Endpunkts** – Wechseln Sie zum Schlüsseltresor, wählen Sie dann im linken Navigationsbereich **Geheime Schlüssel** aus, und kopieren Sie den Namen des geheimen Schlüssels, in dem die Event-Hub-Verbindungszeichenfolge für den Redis-Cache gespeichert ist. Fügen Sie diesen Wert in das Dialogfeld **Add-In einrichten** ein.

6. Aktivieren Sie das Kontrollkästchen, um die allgemeinen Geschäftsbedingungen zu akzeptieren.
7. Wählen Sie **Installieren**.
8. Es wird ein Meldungsfeld mit dem Inhalt „Add-In wurde erfolgreich für die Installation ausgelöst“ angezeigt. Wählen Sie **OK**.

Die LCS-Einrichtung ist nun abgeschlossen. Als Nächstes muss der Schritt [Szenarien einrichten](iot-scenario-setup.md) ausgeführt werden.

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a>Add-In deinstallieren

1. Führen Sie in Supply Chain Management den Schritt [Szenarien deaktivieren](iot-scenario-setup.md#disable-a-scenario) aus.
2. Wechseln Sie in LCS zu den Details Ihrer Supply Chain Management-Umgebung.
3. Scrollen Sie zum Abschnitt **Umgebungs-Add-Ins**.
4. Wählen Sie für das IoT-Intelligenz-Add-In **Deinstallieren** aus.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]