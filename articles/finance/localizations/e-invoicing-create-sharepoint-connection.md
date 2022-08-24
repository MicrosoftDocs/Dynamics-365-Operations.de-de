---
title: Konfigurieren Sie eine SharePoint-Verbindung
description: In diesem Artikel wird erklärt, wie Sie eine Verbindung konfigurieren, damit die Elektronische Rechnungsstellung auf eine Microsoft SharePoint-Seite zugreifen kann.
author: gionoder
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: a2762178686d1f29c457b6de2a9b052fd048484b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283986"
---
# <a name="configure-a-sharepoint-connection"></a>Konfigurieren Sie eine SharePoint-Verbindung

[!include [banner](../includes/banner.md)]

Der Dienst für die elektronische Rechnungsstellung kann Dateien aus Microsoft SharePoint-Ordnern lesen und Dateien in SharePoint hochladen. Um sicherzustellen, dass die Elektronische Rechnungsstellung auf eine bestimmte SharePoint-Seite zugreifen kann, müssen Sie dem Dienst für die elektronische Rechnungsstellung die Anmeldeinformationen für die Seite zur Verfügung stellen. Um außerdem sicherzustellen, dass die Anmeldeinformationen sicher gespeichert werden, geben Sie sie nicht direkt weiter. Speichern Sie sie stattdessen in einem Azure Key Vault, und geben Sie ein Azure Key Vault Geheimnis an.

## <a name="grant-access-to-a-sharepoint-folder"></a>Zugriff auf einen SharePoint-Ordner gewähren

1. Erstellen Sie eine App-Registrierung in dem Mandant, in dem Regulatory Configuration Service (RCS) installiert ist.

    1. Melden Sie sich beim [Azure-Portal](https://portal.azure.com/) an.
    2. Gehen Sie zu **App-Registrierungen**.
    3. Wählen Sie **Neue Registrierung** aus.
    4. Geben Sie einen Namen ein, z.B. **SharePoint App für Elektronische Rechnungsstellung**, und schließen Sie die Registrierung ab
    5. Wählen Sie die neue App-Registrierung.
    6. Aktivieren Sie auf der Registerkarte **Authentifizierung** die Option **Öffentliche Client Flows zulassen**.
    4. Wählen Sie auf der Registerkarte **Zertifikate & Geheimnisse** die Option **Neues Client Geheimnis**, um ein Client Geheimnis zu erstellen.
    5. Kopieren Sie den Wert des erstellten Geheimnisses.

    Befolgen Sie diese Richtlinien:

    - Verwenden Sie nicht die gleiche App-Registrierung für verschiedene Dienste.
    - Befolgen Sie die [Empfehlungen zur Kennwort-Richtlinie](/microsoft-365/admin/misc/password-policy-recommendations?view=o365-worldwide).
    - Festlegen der Rotation von Kennwörtern. Erstellen Sie während der Rotation ein neues Client-Geheimnis für die App-Registrierung, aktualisieren Sie den Key Vault und löschen Sie dann das alte Geheimnis.

2. Speichern Sie die Werte **Geheimnis der App-Registrierung** und **Anwendungs-(Client-)ID** als zwei neue Geheimnisse im Key Vault bei der Einrichtung Ihrer Umgebung für die Elektronische Rechnungsstellung.
3. Fügen Sie die Geheimnisse, die Sie erstellt haben, zu den Key Vault-Parametern bei der Einrichtung Ihrer Umgebung für Elektronische Rechnungsstellung in RCS hinzu.
4. Gewähren Sie im Azure-Portal den Zugriff auf SharePoint. Dieser Schritt sollte vom Mandant-Administrator ausgeführt werden.

    1. Wählen Sie die App-Registrierung, die Sie erstellt haben.
    2. Auf der Registerkarte **API Berechtigungen** wählen Sie **Eine Berechtigung hinzufügen**.
    3. Wählen Sie **Microsoft Graph (Anwendungsberechtigungen)** \> **Sites.Selected**.
    4. Wählen Sie **Admin-Zustimmung für \<user&nbsp;name\> erteilen**.
    5. Überprüfen Sie das Feld **Status**, um sicherzustellen, dass die Berechtigungen erteilt wurden.

        ![Berechtigungen, die auf der Registerkarte API-Berechtigungen erteilt werden.](media/configured-permissions.jpg)

    6. Öffnen Sie [Graph-Explorer - Microsoft Graph](https://developer.microsoft.com/graph/graph-explorer), und melden Sie sich an.
    7. Wählen Sie im linken Fensterbereich auf der Registerkarte **Beispielabfragen** unter **SharePoint Sites** die Option **SharePoint-Site auf Basis des relativen Pfads der Site abrufen**.
    8. Füllen Sie die Parameter **\{host-name\}** und **\{server-relative-path\}** aus. Geben Sie zum Beispiel `<domain>.sharepoint.com` für **\{host-name\}** und `sites/<siteName>` für **\{server-relative-path\}** ein.

        > [!NOTE]
        > Für die Standard-Website lassen Sie den Parameter **\{server-relative-path\}** leer.

    9. Wählen Sie **Abfrage ausführen**, und speichern Sie das Ergebnis.
    10. Konfigurieren Sie die folgende Abfrage.

        `POST https://graph.microsoft.com/v1.0/sites/{site-id}/permissions`

        In dieser Abfrage ist **\{site-id\}** der Wert des Knotens **id** aus der vorherigen Abfrageantwort.

        Hier ist der Körper der Anfrage.

        ```json
        {
            "roles": [
                "read",
                "write"
            ],
            "grantedToIdentities": [
                {
                    "application": {
                        "id": "{app-id}",
                        "displayName": "{app-name}"
                    }
                }
            ]
        }
        ```

        In diesem Abfragetext ist **\{app-id\}** der Wert **Anwendung (Client) ID** und **\{app-name\}** der Wert **Anwendungsname**.

        ![POST-Abfrage.](media/app-id-query.jpg)

    11. Wählen Sie auf der Registerkarte **Berechtigungen ändern** die Option **Das Berechtigungsfeld öffnen** und wählen Sie dann **Sites** \> **Sites.FullControl.All** \> **Consent**.
    12. Wählen Sie **Abfrage ausführen**.

Der Dienst für die elektronische Rechnungsstellung hat jetzt Zugriff auf Ihren Standort SharePoint.
