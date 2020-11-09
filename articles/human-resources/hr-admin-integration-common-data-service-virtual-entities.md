---
title: Konfigurieren von Common Data Service virtuellen Entitäten
description: In diesem Thema wird gezeigt, wie virtuelle Entitäten für Dynamics 365 Human Resources konfiguriert werden. Generieren und aktualisieren Sie vorhandene virtuelle Entitäten und analysieren Sie generierte und verfügbare Entitäten.
author: andreabichsel
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0d6f79ea569a7a9b0d25e73e8666bf9ba19095d0
ms.sourcegitcommit: a8665c47696028d371cdc4671db1fd8fcf9e1088
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2020
ms.locfileid: "4058153"
---
# <a name="configure-common-data-service-virtual-entities"></a>Konfigurieren von Common Data Service virtuellen Entitäten

[!include [banner](includes/preview-feature.md)]

Dynamics 365 Human Resources ist eine virtuelle Datenquelle in Common Data Service. Es bietet vollständige CRUD-Vorgänge zum Erstellen, Lesen, Aktualisieren und Löschen von Common Data Service und Microsoft Power Platform. Die Daten für virtuelle Entitäten werden nicht in Common Data Service gespeichert, aber in der Anwendungsdatenbank. 

Um CRUD-Vorgänge für Personalabteilungen von Common Data Service zu aktivieren, müssen Sie die Entitäten als virtuelle Entitäten in Common Data Service verfügbar machen. Auf diese Weise können Sie CRUD-Vorgänge von Common Data Service und Microsoft Power Platform auf Daten ausführen, die sich in der Personalabteilung befinden. Die Vorgänge unterstützen auch die vollständige Überprüfung der Geschäftslogik der Personalabteilung, um die Datenintegrität beim Schreiben von Daten in die Entitäten sicherzustellen.

## <a name="available-virtual-entities-for-human-resources"></a>Verfügbare virtuelle Einheiten für die Personalabteilung

Alle Open Data Protocol (OData)-Entitäten in der Personalabteilung sind als virtuelle Entitäten in Common Data Service verfügbar. Sie sind auch in Power Platform verfügbar. Sie können jetzt Apps und Erfahrungen mit Daten direkt aus der Personalabteilung mit voller CRUD-Fähigkeit erstellen, ohne Daten nach Common Data Service kopieren oder synchronisieren zu müssen. Sie können Power Apps-Portale zum Erstellen von nach außen gerichteten Websites, die Kollaborationsszenarien für Geschäftsprozesse in der Personalabteilung ermöglichen, verwenden.

Sie können die Liste der in der Umgebung aktivierten virtuellen Entitäten anzeigen und mit den Entitäten in [Power Apps](https://make.powerapps.com) in der Lösung **Virtuelle Entitäten von Dynamics 365 HR** arbeiten.

![Dynamics 365 HR virtuelle Entitäten in Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a>Virtuelle Entitäten versus natürliche Entitäten

Virtuelle Einheiten für die Personalabteilung sind nicht die gleichen wie die natürlichen Common Data Service-Entitäten, die für die Personalabteilung erstellt wurden. Die natürlichen Entitäten für die Personalabteilung werden separat generiert und in der HCM Common-Lösung in Common Data Service verwaltet. Bei natürlichen Entitäten werden die Daten in Common Data Service gespeichert und erfordern eine Synchronisation mit der Anwendungsdatenbank der Personalabteilung.

> [!NOTE]
> Eine Liste der natürlichen Common Data Service-Entitäten für die Personalabteilung ist verfügbar unter [Common Data Service Entitäten](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).

## <a name="setup"></a>Einrichtung

Befolgen Sie diese Einrichtungsschritte, um virtuelle Entitäten in Ihrer Umgebung zu aktivieren. 

### <a name="register-the-app-in-microsoft-azure"></a>Registrieren Sie die App in Microsoft Azure

Zunächst müssen Sie die App im Azure-Portal registrieren, damit die Microsoft-Identitätsplattform Authentifizierungs- und Autorisierungsdienste für die App und die Benutzer bereitstellen kann. Weitere Informationen zum Registrieren von Apps in Azure finden Sie unter [Schnellstart: Registrieren Sie eine Anwendung bei der Microsoft-Identitätsplattform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).

1. Öffnen Sie das [Microsoft Azure-Portal](https://portal.azure.com).

2. Wählen Sie in der Liste der Azure-Dienstleistungen die Option **App-Registrierungen** aus.

3. Wählen Sie **Neue Registrierung** aus.

4. Geben Sie im Feld **Name** einen aussagekräftigen Namen für die App ein. Beispielsweise, **Dynamics 365 Human Resources Virtuelle Entitäten**.

5. Geben Sie im Feld **URI umleiten** die Namespace-URL Ihrer Instanz der Personalabteilung ein.

6. Wählen Sie **Registrieren** aus.

7. Nach Abschluss der Registrierung zeigt das Azure-Portal den Bereich **Überblick** der App-Registrierung an, der dessen **Anwendungs-ID (Client-ID)** enthält. Beachten Sie die **Anwendungs-ID (Client-ID)** zu diesem Zeitpunkt. Sie geben diese Informationen ein, wenn Sie [Konfigurieren der Datenquelle der virtuellen Entität](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).

8. Wählen Sie im linken Navigationsbereich **Zertifikate und Geheimnisse** aus.

9. In dem Abschnitt **Kundengeheimnisse** der Seite wählen Sie **Neues Kundengeheimnis** aus.

10. Geben Sie eine Beschreibung ein, wählen Sie eine Dauer aus und wählen Sie **Hinzufügen**.

11. Erfassen Sie den Wert des Geheimnisses. Sie geben diese Informationen ein, wenn Sie [Konfigurieren der Datenquelle der virtuellen Entität](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).

    > [!IMPORTANT]
    > Beachten Sie zu diesem Zeitpunkt unbedingt den Wert des Geheimnisses. Das Geheimnis wird nie wieder angezeigt, nachdem Sie diese Seite verlassen haben.

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a>Installieren Sie die Dynamics 365 HR Virtual Entity-App

Installieren Sie die Dynamics 365 HR Virtual Entity-App in Ihrer Power Apps-Umgebung, um das Lösungspaket für virtuelle Entitäten für Common Data Service bereitzustellen.

1. Öffnen Sie das [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).

2. In der Liste **Umgebungen** wählen Sie die Power Apps-Umgebung, die Ihrer Personalabteilungsinstanz zugeordnet ist.

3. In dem Abschnitt **Ressourcen** der Seite wählen Sie **Dynamics 365-Apps**.

4. Wählen Sie die Aktion **App installieren** aus.

5. Wählen Sie **Dynamics 365 HR Virtuelle Entität** und dann **Weiter**.

6. Überprüfen und markieren Sie, um den Vertragsbedingungen zuzustimmen.

7. Wählen Sie **Installieren**.

Die Installation dauert einige Minuten. Fahren Sie nach Abschluss mit den nächsten Schritten fort.

![Installieren Sie die Dynamics 365 HR Virtual Entity-App vom Power Platform-Admin Center](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a>Konfigurieren Sie die Datenquelle der virtuellen Entität 

Der nächste Schritt besteht darin, die Datenquelle der virtuellen Entität in der Power Apps-Umgebung zu konfigurieren. 

1. Öffnen Sie das [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).

2. In der Liste **Umgebungen** wählen Sie die Power Apps-Umgebung, die Ihrer Personalabteilungsinstanz zugeordnet ist.

3. Wählen Sie die **Umgebungs-URL** im Abschnitt **Details** der Seite aus.

4. Im **Lösungsintegrität-Hub** wählen Sie das Symbol **Erweiterte Suche** oben rechts auf der Anwendungsseite aus.

5. Wählen Sie auf der Seite **Erweiterte Suche** in der Dropdown-Liste **Suchen** **Finance and Operations Konfigurationen virtueller Datenquellen** aus.

6. Wählen Sie **Ergebnisse** aus.

7. Wählen Sie den Datensatz **Microsoft HR-Datenquelle**.

8. Geben Sie die erforderlichen Informationen für die Datenquellenkonfiguration ein.

   - **Ziel-URL** : Die URL Ihres Personalabteilungs-Namespace.
   - **Mandanten-ID** : Die Azure Active Directory (Azure AD)-Mandanten-ID.
   - **AAD-Anwendungs-ID** : Die Anwendungs-ID (Client-ID), die für die im Microsoft Azure-Portal registrierte Anwendung erstellt wurde. Sie haben diese Informationen früher während des Schritts [Registrieren Sie die App in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure) erhalten.
   - **AAD-Anwendungs-Geheimnis** : Das Kundengeheimnis, das für die im Microsoft Azure-Portal registrierte Anwendung erstellt wurde. Sie haben diese Informationen früher während des Schritts [Registrieren Sie die App in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure) erhalten.

9. Wählen Sie **Speichern & Schließen** aus.

   ![Microsoft HR-Datenquelle](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

### <a name="grant-app-permissions-in-human-resources"></a>Erteilen Sie App-Berechtigungen in der Personalabteilung

Erteilen Sie Berechtigungen für die beiden Azure AD-Anwendungen in der Personalabteilung:

- Die für Ihren Mandanten im Microsoft Azure-Portal erstellte App
- Die Dynamics 365 HR Virtual Entity-App installiert in der Power Apps-Umgebung 

1. Öffnen Sie in der Personalabteilung die Seite **Azure Active Directory-Anwendungen**.

2. Wählen Sie **Neu** aus, um einen neuen Anwendungsdatensatz zu erstellen:

    - Geben Sie im Feld **Client-ID** die Client-ID der App ein, die Sie im Microsoft Azure-Portal registriert haben.
    - Geben Sie im Feld **Name** den Namen der App ein, die Sie im Microsoft Azure-Portal registriert haben.
    - Wählen Sie im Feld **Benutzer-ID** die Benutzer-ID eines Benutzers mit Administratorrechten in der Personalabteilung und der Power Apps-Umgebung aus.

3. Wählen Sie **Neu** aus, um einen zweiten Anwendungsdatensatz zu erstellen:

    - **Client-ID** : f9be0c49-aa22-4ec6-911a-c5da515226ff
    - **Name** : Dynamics 365 HR Virtual Entity
    - Wählen Sie im Feld **Benutzer-ID** die Benutzer-ID eines Benutzers mit Administratorrechten in der Personalabteilung und der Power Apps-Umgebung aus.

## <a name="generate-virtual-entities"></a>Erstellen virtueller Entitäten

Nach Abschluss des Setups können Sie die virtuellen Entitäten auswählen, die Sie generieren und in Ihrer Common Data Service-Instanz aktivieren möchten.

1. Öffnen Sie in der Personalabteilung die Seite **Common Data Service (CDS) Integartion**.

2. Wählen Sie die Registerkarte **Virtuelle Entitäten**.

> [!NOTE]
> Die Umschaltung **Aktivieren Sie die virtuelle Entität** wird automatisch auf **Ja** gesetzt, wenn alle erforderlichen Einstellungen abgeschlossen sind. Wenn der Schalter auf **Nein** eingestellt ist, überprüfen Sie die Schritte in den vorherigen Abschnitten dieses Dokuments, um sicherzustellen, dass alle erforderlichen Einstellungen abgeschlossen sind.

3. Wählen Sie die Entität oder Entitäten aus, die Sie in Common Data Service generieren möchten.

4. Wählen Sie **Generieren/Aktualisieren**.

![Common Data Service Integration](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-entity-generation-status"></a>Überprüfen Sie den Status der Entitätsgenerierung

Virtuelle Entitäten werden in Common Data Service durch einen asynchronen Hintergrundprozess generiert. Aktualisierungen der Prozessanzeige im Action Center. Details zum Prozess, einschließlich Fehlerprotokollen, werden in der Seite **Prozessautomatisierung** angezeigt.

1. Öffnen Sie in Human Resources die Listenseite **Prozessautomatisierung**.

2. Wählen Sie die Registerkarte **Hintergrundprozesse**.

3. Wählen Sie **Hintergrundprozess für asynchrone Operationen einer virtuellen Entität**.

4. Wählen Sie **Aktuelle Ergebnisse anzeigen**.

Im Slideout-Bereich werden die neuesten Ausführungsergebnisse für den Prozess angezeigt. Sie können das Protokoll für den Prozess anzeigen, einschließlich aller von Common Data Service zurückgegebener Fehler.

## <a name="see-also"></a>Siehe auch

[Was ist Common Data Service?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[Entitätsübersicht](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[Übersicht über Entitätsbeziehungen](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[Erstellen und bearbeiten Sie virtuelle Entitäten, die Daten aus einer externen Datenquelle enthalten](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[Was sind Power Apps-Portale?](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[Übersicht über das Erstellen von Apps in Power Apps](https://docs.microsoft.com/powerapps/maker/)
