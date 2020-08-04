---
title: Azure-Ressourcen für IoT-Intelligenz einrichten
description: In diesem Thema wird erläutert, wie Sie Microsoft Azure-Ressourcen erstellen und konfigurieren, die Sie für IoT-Intelligenz benötigen.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 431ad6766f1e7f2035d6d5ed87bed4856e58e098
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597263"
---
# <a name="set-up-azure-resources-for-iot-intelligence"></a>Azure-Ressourcen für IoT-Intelligenz einrichten

[!include [banner](../../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie Microsoft Azure-Ressourcen erstellen und konfigurieren, die Sie für IoT-Intelligenz benötigen.

## <a name="create-azure-resources"></a>Azure-Ressourcen erstellen

Führen Sie die folgenden Schritte aus, um einen IoT-Hub, einen Redis-Cache und einen Schlüsseltresor erstellen, auf den Microsoft Dynamics 365 Supply Chain Management zugreifen kann.

### <a name="verify-that-the-microsoft-dynamics-erp-microservices-first-party-app-id-is-in-your-tenant"></a>Sicherstellen, dass die Microsoft Dynamics ERP-Microservices sich in Ihrem Mandanten befinden

Führen Sie die folgenden Schritte aus, um zu überprüfen, ob die App-ID für Microsoft Dynamics ERP-Microservices sich in Ihrem Mandanten befindet.

1. Melden Sie sich beim Azure-Portal an unter <https://portal.azure.com>.
2. Gehe zu **Azure Active Directory**.
3. Wechseln Sie zu **Unternehmensanwendungen**.
4. Wählen Sie im Feld **Anwendungstyp** die Option **Microsoft-Anwendungen** aus.
5. Geben Sie **Microsoft Dynamics ERP-Microservices** in das Suchfeld ein.
6. Überprüfen Sie, ob **Microsoft Dynamics ERP-Microservices** in der Liste enthalten ist. Andere Anwendungen haben ähnliche Namen. Achten Sie deshalb darauf, dass Sie die richtige Anwendung finden. Die App-ID lautet **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.

    Wenn die Anwendung nicht in der Liste enthalten ist, müssen Sie sie Ihrem Mandanten hinzufügen:

    1. Wählen Sie im Azure-Portal auf der Symbolleiste die Schaltfläche zum Öffnen von Azure Cloud Shell aus.
    2. Führen Sie den Befehl **Install-Module AzureAD** aus. Geben Sie **Y** ein, um das Modul zu installieren.
    3. Führen Sie den Befehl **Get-InstalledModule -Name "AzureAD"** aus, um zu überprüfen, ob das Modul installiert ist.
    4. Führen Sie den Befehl **Connect-AzureAD -Confirm** aus, um die Authentifizierung auszuführen.
    5. Führen Sie den Befehl **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2** aus.

    Sie können jetzt die Schritte 1 bis 6 wiederholen, um zu überprüfen, ob sich die App-ID in Ihrem Mandanten befindet.

### <a name="create-a-key-vault-resource"></a>Schlüsseltresor-Ressource erstellen

Führen Sie die folgenden Schritte aus, um eine Schlüsseltresor-Ressource zu erstellen.

1. Erstellen Sie im Azure-Portal eine Ressourcengruppe, oder wechseln Sie zu einer.
2. Wählen Sie **Hinzufügen** aus.
3. Geben Sie auf der Seite **Neu** **Schlüsseltresor** in das Suchfeld ein. Wählen Sie dann **Erstellen** aus.
4. Geben Sie auf der Seite **Schlüsseltresor erstellen** im Feld **Schlüsseltresor-Name** einen Namen ein.
5. Überprüfen Sie die Standardwerte, und wählen Sie dann **Überprüfen + Erstellen** aus.
6. Wählen Sie **Erstellen** aus.

Der Schlüsseltresor wird im Hintergrund erstellt.

### <a name="create-an-iot-hub-resource"></a>IoT-Hub-Ressource erstellen

Führen Sie die folgenden Schritte aus, um eine IoT-Hub-Ressource zu erstellen.

1. Erstellen Sie eine Ressourcengruppe, oder wechseln Sie zu einer.
2. Wählen Sie **Hinzufügen** aus.
3. Geben Sie auf der Seite **Neu** **IoT-Hub** in das Suchfeld ein. Wählen Sie dann **Erstellen** aus.
4. Geben Sie im Feld **IoT-Hub-Name** einen Namen ein.
5. Überprüfen Sie die Standardwerte, und wählen Sie dann **Überprüfen + Erstellen** aus.
6. Wählen Sie **Erstellen** aus.

Der IoT-Hub wird im Hintergrund erstellt.

> [!NOTE]
> Es wird empfohlen, nur eine IoT-Hub-Ressource pro Umgebung zu erstellen.

### <a name="create-a-redis-cache-resource"></a>Redis-Cache-Ressource erstellen

Führen Sie die folgenden Schritte aus, um eine Redis-Cache-Ressource zu erstellen.

1. Erstellen Sie eine Ressourcengruppe, oder wechseln Sie zu einer.
2. Wählen Sie **Hinzufügen** aus.
3. Geben Sie auf der Seite **Neu** **Azure Cache für Redis** in das Suchfeld ein. Wählen Sie dann **Erstellen** aus.
4. Geben Sie im Feld **DNS-Name** einen Namen ein.
5. Überprüfen Sie die Standardwerte, und wählen Sie dann **Erstellen** aus.

Der Redis-Cache wird im Hintergrund erstellt.

> [!NOTE]
> Es wird empfohlen, nur einen Redis-Cache pro Umgebung zu erstellen.

Alle Ressourcen wurden jetzt erstellt.

## <a name="configure-the-azure-resources"></a>Azure-Ressourcen konfigurieren

### <a name="configure-the-iot-hub"></a>IoT-Hub konfigurieren

Führen Sie die folgenden Schritte aus, um den IoT-Hub zu konfigurieren.

1. Wählen Sie die IoT-Hub-Ressource aus Ihren Ressourcen aus.
2. Wählen Sie im linken Navigationsbereich **Integrierte Endpunkte** aus.
3. Fügen Sie die folgenden Consumergruppen unter **Consumergruppen** ein. Diese Consumergruppen entsprechen den vordefinierten Szenarien.

    + microsoft.dynamics.iotintelligence-1
    + microsoft.dynamics.iotintelligence-2
    + microsoft.dynamics.iotintelligence-3

### <a name="configure-the-key-vault"></a>Vault Key konfigurieren

Führen Sie die folgenden Schritte aus, um den Vault Key zu konfigurieren.

1. Wählen Sie die Vault Key-Ressource aus Ihren Ressourcen aus.
2. Wählen Sie im linken Navigationsbereich **Zugriffsrichtlinien** aus.
3. Wählen Sie **Zugriffsrichtlinie hinzufügen**.
4. Wählen Sie auf der Seite **Zugriffsrichtlinie hinzufügen** im Feld **Berechtigungen für Geheimnis** die Optionen **Abrufen** und **Liste** aus.
5. Klicken Sie auf **Prinzipal auswählen**.
6. Suchen Sie im Dialogfeld **Prinzipal** nach **Microsoft Dynamics ERP-Microservices**, und wählen Sie sie aus. Klicken Sie dann auf **Auswählen**.
7. Wählen Sie **Hinzufügen** aus.
8. Wählen Sie **Speichern**.

Die App hat jetzt Zugriff auf die geheimen Schlüssel im Schlüsseltresor.

### <a name="save-the-iot-hub-connection-string-secret"></a>Geheimen Schlüssel der IoT-Hub-Verbindungszeichenfolge speichern

Führen Sie die folgenden Schritte aus, um den geheimen Schlüssel der IoT-Hub-Verbindungszeichenfolge zu speichern.

1. Wählen Sie die IoT-Hub-Ressource aus Ihren Ressourcen aus.
2. Wählen Sie im linken Navigationsbereich **Integrierte Endpunkte** aus.
3. Kopieren Sie den Wert im Feld **Event Hub-kompatibler Endpunkt**.
4. Wechseln Sie zur Vault Key-Ressource.
5. Wählen Sie im linken Navigationsbereich die Option **Geheime Schlüssel** aus.
6. Wählen Sie **Generieren/Importieren** aus.
7. Geben Sie im Feld **Name** einen Namen ein.
8. Fügen Sie den zuvor kopierten Endpunktwert in das Feld **Wert** ein.
9. Wählen Sie **Erstellen** aus.

### <a name="save-the-redis-cache-connection-string-secret"></a>Geheimen Schlüssel der Redis-Cache-Verbindungszeichenfolge speichern

Führen Sie die folgenden Schritte aus, um den geheimen Schlüssel der Redis-Cache-Verbindungszeichenfolge zu speichern.

1. Wählen Sie die Redis-Cache-Ressource aus Ihren Ressourcen aus.
2. Wählen Sie **Zugangsschlüssel** aus.
3. Kopieren Sie den Wert in das Feld **Primäre Verbindungszeichenfolge**.
4. Wechseln Sie zur Vault Key-Ressource.
5. Wählen Sie im linken Navigationsbereich die Option **Geheime Schlüssel** aus.
6. Wählen Sie **Generieren/Importieren** aus.
7. Geben Sie im Feld **Name** einen Namen ein.
8. Fügen Sie die zuvor kopierte Verbindungszeichenfolge in das Feld **Wert** ein.
9. Wählen Sie **Erstellen** aus.

> [!NOTE]
> Wenn Sie eine der Verbindungszeichenfolgen aktualisieren, müssen Sie auch die Werte der geheimen Schlüssel aktualisieren.

Sie haben nun die Bereitstellung der erforderlichen Azure-Ressourcen abgeschlossen. Als Nächstes muss der Schritt [IoT-Intelligenz-Add-In in Microsoft Dynamics Lifecycle Services (LCS) installieren](iot-lcs-setup.md) ausgeführt werden.
