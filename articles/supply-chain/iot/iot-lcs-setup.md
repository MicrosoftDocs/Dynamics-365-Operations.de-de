---
title: IoT-Intelligenz-Add-In in LCS installieren
description: In diesem Thema wird erläutert, wie Sie das IoT-Intelligenz-Add-In in Microsoft Dynamics Lifecycle Services (LCS) installieren.
author: robinarh
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c4727f4341104b77838c103fcf378a5971f8ba176f18c2d32d619ecd6614b1ae
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736818"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a>IoT-Intelligenz-Add-In in LCS installieren

[!include [banner](../../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie das IoT-Intelligenz-Add-In in Microsoft Dynamics Lifecycle Services (LCS) installieren. Beachten Sie, dass Add-Ins nicht in einer Demo-/Testversionsumgebung installiert werden können. Bevor Sie das Add-In installieren können, müssen Sie die [Azure-Ressourcen erstellen](iot-azure-setup.md).

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