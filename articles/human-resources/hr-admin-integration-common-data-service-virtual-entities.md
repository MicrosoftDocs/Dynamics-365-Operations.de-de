---
title: Virtuelle Dataverse-Tabellen konfigurieren
description: Dieser Artikel zeigt, wie Sie virtuelle Tabellen konfigurieren, generieren, aktualisieren und generierte und verfügbare Tabellen für Dynamics 365 Human Resources analysieren.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0154faec8a9f3e968ea1b665e2a815cc9ec02379
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899729"
---
# <a name="configure-dataverse-virtual-tables"></a>Virtuelle Dataverse-Tabellen konfigurieren


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Dynamics 365 Human Resources ist eine virtuelle Datenquelle in Microsoft Dataverse. Es bietet vollständige CRUD-Vorgänge zum Erstellen, Lesen, Aktualisieren und Löschen von Dataverse und Microsoft Power Platform. Die Daten für virtuelle Tabellen werden nicht in Dataverse gespeichert, aber in der Anwendungsdatenbank.

Um CRUD-Vorgänge für Human Resources-Entitäten von Dataverse zu aktivieren, müssen Sie die Entitäten als virtuelle Tabellen in Dataverse verfügbar machen. Auf diese Weise können Sie CRUD-Vorgänge von Dataverse und Microsoft Power Platform auf Daten ausführen, die sich in Human Resources befinden. Die Vorgänge unterstützen auch die vollständige Überprüfung der Geschäftslogik von Human Resources, um die Datenintegrität beim Schreiben von Daten in die Entitäten sicherzustellen.

> [!NOTE]
> Human Resources-Entitäten entsprechen Dataverse-Tabellen. Weitere Informationen zu Dataverse (früher Common Data Service) und Terminologie-Updates finden Sie unter [Was ist Microsoft Dataverse ?](/powerapps/maker/data-platform/data-platform-intro)

## <a name="available-virtual-tables-for-human-resources"></a>Verfügbare virtuelle Tabellen für Human Resources

Alle Open Data Protocol (OData)-Entitäten in Human Resources sind als virtuelle Tabellen in Dataverse verfügbar. Sie sind auch in Power Platform verfügbar. Sie können jetzt Apps und Erfahrungen mit Daten direkt aus Human Resources mit voller CRUD-Fähigkeit erstellen, ohne Daten nach Dataverse kopieren oder synchronisieren zu müssen. Sie können Power Apps-Portale zum Erstellen von nach außen gerichteten Websites, die Kollaborationsszenarien für Geschäftsprozesse in Human Resources ermöglichen, verwenden.

Sie können die Liste der in der Umgebung aktivierten virtuellen Tabellen anzeigen und mit den Tabellen in [Power Apps](https://make.powerapps.com) in der Lösung **Virtuelle Tabellen von Dynamics 365 HR** arbeiten.

![Dynamics 365 HR virtuelle Tabellen in Power Apps.](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a>Virtuelle Tabellen gegenüber nativen Tabellen

Virtuelle Tabellen für Human Resources sind nicht die gleichen wie die nativen Dataverse-Tabellen, die für Human Resources erstellt wurden. 

Die nativen Tabellen für Human Resources werden separat generiert und in der HCM Common-Lösung in Dataverse verwaltet. Bei nativen Tabellen werden die Daten in Dataverse gespeichert und erfordern eine Synchronisation mit der Anwendungsdatenbank von Human Resources.

> [!NOTE]
> Eine Liste der nativen Dataverse-Tabellen für Human Resources ist verfügbar unter [Dataverse Tabellen](./hr-developer-entities.md).

## <a name="setup"></a>Einstellung

Befolgen Sie diese Einrichtungsschritte, um virtuelle Tabellen in Ihrer Umgebung zu aktivieren.

### <a name="enable-virtual-tables-in-human-resources"></a>Virtuelle Tabellen in Human Resources aktivieren

Zunächst müssen Sie virtuelle Tabellen im Arbeitsplatz **Funktionsverwaltung** aktivieren.

1. Wählen Sie in Human Resources **Systemverwaltung** aus.

2. Wählen Sie die Kachel **Funktionsverwaltung**.

3. Wählen Sie **Support für virtuelle Tabellen für HR in Dataverse** und dann **Aktivieren**.

Weitere Informationen zum Aktivieren und Deaktivieren von Funktionen finden Sie unter [Funktionen verwalten](hr-admin-manage-features.md).

### <a name="register-the-app-in-microsoft-azure"></a>Registrieren Sie die App in Microsoft Azure

Zunächst müssen Sie Ihre Human Resources-Instanz im Azure-Portal registrieren, damit die Microsoft-Identitätsplattform Authentifizierungs- und Autorisierungsdienste für die App und die Benutzer bereitstellen kann. Weitere Informationen zum Registrieren von Apps in Azure finden Sie unter [Schnellstart: Registrieren Sie eine Anwendung bei der Microsoft-Identitätsplattform](/azure/active-directory/develop/quickstart-register-app).

1. Öffnen Sie das [Microsoft Azure-Portal](https://portal.azure.com).

2. Wählen Sie in der Liste der Azure-Dienstleistungen die Option **App-Registrierungen** aus.

3. Wählen Sie **Neue Registrierung** aus.

4. Geben Sie im Feld **Name** einen aussagekräftigen Namen für die App ein. Beispielsweise, **Dynamics 365 Human Resources Virtuelle Tabellen**.

5. Geben Sie im Feld **URI umleiten** die Namespace-URL Ihrer Instanz in Human Resources ein.

6. Wählen Sie **Registrieren** aus.

7. Nach Abschluss der Registrierung zeigt das Azure-Portal den Bereich **Überblick** der App-Registrierung an, der dessen **Anwendungs-ID (Client-ID)** enthält. Beachten Sie die **Anwendungs-ID (Client-ID)** zu diesem Zeitpunkt. Sie geben diese Informationen ein, wenn Sie [Konfigurieren der Datenquelle der virtuellen Tabelle](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).

8. Wählen Sie im linken Navigationsbereich **Zertifikate und Geheimnisse** aus.

9. In dem Abschnitt **Kundengeheimnisse** der Seite wählen Sie **Neues Kundengeheimnis** aus.

10. Geben Sie eine Beschreibung ein, wählen Sie eine Dauer aus und wählen Sie **Hinzufügen**.

11. Erfassen Sie den Wert des Geheimnisses aus dem der Eigenschaft **Wert** der Tabelle. Sie geben diese Informationen ein, wenn Sie [Konfigurieren der Datenquelle der virtuellen Tabelle](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).

    > [!IMPORTANT]
    > Beachten Sie zu diesem Zeitpunkt unbedingt den Wert des Geheimnisses. Das Geheimnis wird nie wieder angezeigt, nachdem Sie diese Seite verlassen haben.

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a>Installieren Sie die Dynamics 365 HR Virtual Table-App

Installieren Sie die Dynamics 365 HR Virtual Table-App in Ihrer Power Apps-Umgebung, um das Lösungspaket für virtuelle Tabellen für Dataverse bereitzustellen.

1. Öffnen Sie in Human Resources die Seite **Microsoft Dataverse-Integartion**.

2. Wählen Sie die Registerkarte **Virtuelle Tabellen**.

3. Wählen Sie **Installieren Sie die App für virtuelle Tische**.

### <a name="configure-the-virtual-table-data-source"></a>Konfigurieren Sie die Datenquelle der virtuellen Tabelle

Der nächste Schritt besteht darin, die Datenquelle der virtuellen Tabelle in der Power Apps-Umgebung zu konfigurieren.

1. Öffnen Sie das [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).

2. In der Liste **Umgebungen** wählen Sie die Power Apps-Umgebung, die Ihrer Human Resources-Instanz zugeordnet ist.

3. Wählen Sie die **Umgebungs-URL** im Abschnitt **Details** der Seite aus.

4. Im **Lösungsintegrität-Hub** wählen Sie das Symbol **Erweiterte Suche** oben rechts auf der Anwendungsseite aus.

5. Wählen Sie auf der Seite **Erweiterte Suche** in der Dropdown-Liste **Suchen nach** die Option **Finance und Operations Virtual Data Source Configurations**.

   > [!NOTE]
   > Die Installation der virtuellen Tabellen-App aus dem vorherigen Einrichtungsschritt kann einige Minuten dauern. Wenn **Finance und Operations Virtual Data Source Configurations** nicht in der Liste vorhanden ist, warten Sie eine Minute und aktualisieren Sie die Liste.

6. Wählen Sie **Ergebnisse** aus.

7. Wählen Sie den Datensatz **Microsoft HR-Datenquelle**.

8. Geben Sie die erforderlichen Informationen für die Datenquellenkonfiguration ein:

   - **Ziel-URL**: Die URL Ihres Human Resources-Namespace. Das Format der Ziel-URL sieht wie folgt aus:
     
     https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/

     Beispiel:
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     >Vergessen Sie das „**/**“-Zeichen am Ende der URL nicht, um einen Fehler zu vermeiden.

     >[!NOTE]
     >Die Ziel-URL bestimmt die Human Resources Umgebung, auf die virtuelle Tabellen für Daten verweisen werden. Wenn Sie eine Sandbox-Umgebung erstellen, indem Sie eine Kopie Ihrer Produktionsumgebung erstellen, aktualisieren Sie diesen Wert auf die Namespace-URL Ihrer neuen Sandbox-Umgebung. Dadurch wird sichergestellt, dass die virtuellen Tabellen mit den Daten der Sandbox-Umgebung verbunden sind und nicht weiterhin auf die Produktionsumgebung zeigen.

   - **Mandanten-ID**: Die Azure Active Directory (Azure AD)-Mandanten-ID.

   - **AAD-Anwendungs-ID**: Die Anwendungs-ID (Client-ID), die für die im Microsoft Azure-Portal registrierte Anwendung erstellt wurde. Sie haben diese Informationen früher während des Schritts [Registrieren Sie die App in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure) erhalten.

   - **AAD-Anwendungs-Geheimnis**: Das Kundengeheimnis, das für die im Microsoft Azure-Portal registrierte Anwendung erstellt wurde. Sie haben diese Informationen früher während des Schritts [Registrieren Sie die App in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure) erhalten.

   ![Microsoft HR-Datenquelle.](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. Wählen Sie **Speichern & Schließen** aus.

### <a name="grant-app-permissions-in-human-resources"></a>App-Berechtigungen in Human Resources erteilen

Erteilen Sie Berechtigungen für die beiden Azure AD-Anwendungen in Human Resources:

- Die für Ihren Mandanten im Microsoft Azure-Portal erstellte App
- Die Dynamics 365 HR Virtual Table-App installiert in der Power Apps-Umgebung 

1. Öffnen Sie in Human Resources die Seite **Azure Active Directory-Anwendungen**.

2. Wählen Sie **Neu** aus, um einen neuen Anwendungsdatensatz zu erstellen:

    - Geben Sie im Feld **Client-ID** die Client-ID der App ein, die Sie im Microsoft Azure-Portal registriert haben.
    - Geben Sie im Feld **Name** den Namen der App ein, die Sie im Microsoft Azure-Portal registriert haben.
    - Wählen Sie im Feld **Benutzer-ID** die Benutzer-ID eines Benutzers mit Administratorrechten in Human Resources und der Power Apps-Umgebung aus.

3. Wählen Sie **Neu** aus, um einen zweiten Anwendungsdatensatz zu erstellen:

    - **Client-ID**: f9be0c49-aa22-4ec6-911a-c5da515226ff
    - **Name**: Dynamics 365 HR Virtual Table
    - Wählen Sie im Feld **Benutzer-ID** die Benutzer-ID eines Benutzers mit Administratorrechten in Human Resources und der Power Apps-Umgebung aus.

## <a name="generate-virtual-tables"></a>Erstellen virtueller Tabellen

Nach Abschluss des Setups können Sie die virtuellen Tabellen auswählen, die Sie generieren und in Ihrer Dataverse-Instanz aktivieren möchten.

1. Öffnen Sie in Human Resources die Seite **Microsoft Dataverse-Integartion**.

2. Wählen Sie die Registerkarte **Virtuelle Tabellen**.

> [!NOTE]
> Die Umschaltung **Aktivieren Sie die virtuelle Tabelle** wird automatisch auf **Ja** gesetzt, wenn alle erforderlichen Einstellungen abgeschlossen sind. Wenn der Schalter auf **Nein** eingestellt ist, überprüfen Sie die Schritte in den vorherigen Abschnitten dieses Dokuments, um sicherzustellen, dass alle erforderlichen Einstellungen abgeschlossen sind.

3. Wählen Sie die Tabelle oder Tabellen aus, die Sie in Dataverse generieren möchten.

4. Wählen Sie **Generieren/Aktualisieren**.

![Dataverse-Integration.](./media/hr-admin-integration-dataverse-integration.png)

## <a name="check-table-generation-status"></a>Überprüfen Sie den Status der Tabellengenerierung

Virtuelle Tabellen werden in Dataverse durch einen asynchronen Hintergrundprozess generiert. Aktualisierungen der Prozessanzeige im Action Center. Details zum Prozess, einschließlich Fehlerprotokollen, werden in der Seite **Prozessautomatisierung** angezeigt.

1. Öffnen Sie in Human Resources die Listenseite **Prozessautomatisierung**.

2. Wählen Sie die Registerkarte **Hintergrundprozesse**.

3. Wählen Sie **Hintergrundprozess für asynchrone Operationen einer virtuellen Tabelle**.

4. Wählen Sie **Aktuelle Ergebnisse anzeigen**.

Im Slideout-Bereich werden die neuesten Ausführungsergebnisse für den Prozess angezeigt. Sie können das Protokoll für den Prozess anzeigen, einschließlich aller von Dataverse zurückgegebener Fehler.

## <a name="see-also"></a>Siehe auch

[Was ist Dataverse?](/powerapps/maker/common-data-service/data-platform-intro)<br>
[Tabellen in Dataverse](/powerapps/maker/common-data-service/entity-overview)<br>
[Übersicht über Tabellenbeziehungen](/powerapps/maker/common-data-service/relationships-overview)<br>
[Erstellen und bearbeiten Sie virtuelle Tabellen, die Daten aus einer externen Datenquelle enthalten](/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[Was sind Power Apps-Portale?](/powerapps/maker/portals/overview)<br>
[Übersicht über das Erstellen von Apps in Power Apps](/powerapps/maker/)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
