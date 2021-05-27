---
title: Erste Schritte mit der Dienstverwaltung für die elektronische Rechnungsstellung
description: Dieses Thema erläutert die ersten Schritte mit der elektronischen Rechnungsstellung.
author: gionoder
ms.date: 05/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f389e111006327fe8d82581d01140b4cff2e200d
ms.sourcegitcommit: 35fdcc6501e099c54a58583b1e3aba16f02a5ccc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2021
ms.locfileid: "5980974"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a>Erste Schritte mit der Dienstverwaltung für die elektronische Rechnungsstellung

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie die Vorgehensweisen in diesem Thema abschließen, müssen die folgenden Voraussetzungen erfüllt sein:

- Sie müssen Zugriff auf Ihr Microsoft Dynamics Lifecycle Services (LCS)-Konto haben.
- Sie müssen über ein LCS-Projekt verfügen, das Version 10.0.17 oder höher von Microsoft Dynamics 365 Finance und Dynamics 365 Supply Chain Management umfasst. Darüber hinaus müssen diese Apps in einer der folgenden Azure-Regionen bereitgestellt werden:

    - Vereinigte Staaten
    - Europa
    - Vereinigtes Königreich
    - Asien

- Sie müssen Zugriff auf Ihr RCS-Konto (Dynamics 365 Regulatory Configuration Services) haben.
- Die Globalisierungsfunktion für Ihr RCS-Konto muss in der Funktionsverwaltung aktiviert sein. Weitere Informationen finden Sie unter [Regulatory Configuration Services (RCS) – Globalisierungsfunktionen](rcs-globalization-feature.md).
- Sie müssen einen Schlüsseltresor und ein Speicherkonto in Azure erstellen. Weitere Informationen finden Sie unter [Ein Azure-Speicherkonto und einen Schlüsseltresor erstellen](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>Das Add-In für Microservices in Lifecycle Services installieren

1. Melden Sie sich bei Ihrem LCS-Konto an.
2. Wählen Sie die Kachel **Verwaltung von Vorschaufunktionen** aus.
3. Wählen Sie im Abschnitt **Öffentliche Vorschaufunktionen** **Elektronische Rechnungsstellung** aus.
4. Stellen Sie sicher, dass die Option **Vorschaufunktion aktiviert** auf **Ja** festgelegt ist.
5. Wählen Sie in Ihrem LCS-Projektdashboard ein LCS-Projekt aus.
6. Wählen Sie im LCS-Projekt im LCS-Umgebungs-Dashboard Ihr LCS-Bereitstellungsprojekt aus. Das LCS-Bereitstellungsprojekt muss ausgeführt werden.
7. Wählen Sie in der Registerkarte **Power Platform-Integration** in der Feldgruppe **Umgebungs-Add-Ins** **Neues Add-In installieren**.
8. Wählen Sie **Elektronische Rechnungsstellung** aus.
9. Geben Sie im **AAD-Anwendungs-ID**-Feld **091c98b0-a1c9-4b02-b62c-7753395ccabe** ein. Dies ist ein fester Wert.
10. Geben Sie in das Feld **AAD-Mandanten-ID** die Mandanten-ID Ihres Azure-Abonnementkontos ein.
11. Lesen Sie die allgemeinen Geschäftsbedingungen, und aktivieren Sie dann das Kontrollkästchen.
12. Wählen Sie **Installieren**.


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>Parameter für die RCS-Integration in die elektronische Rechnungsstellung einrichten

1. Melden Sie sich bei Ihrem RCS-Konto an.
2. Wählen Sie im Arbeitsbereich **Elektronische Berichterstellung** im Abschnitt **Zugehörige Links** **Elektronische Berichterstellungsparameter** aus.
3. Geben Sie im Feld **Dienstendpunkt-URI** auf der Registerkarte **E-Invoicing-Dienst** den entsprechenden Dienstendpunkt für Ihre Azure-Region ein, wie in folgender Tabelle dargestellt.

    | Azure-Rechenzentrumgeografie | Dienst-Endpunkt-URI                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | Vereinigte Staaten              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Europa                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Vereinigtes Königreich             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Asien                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

4. Vergewissern Sie sich, dass das Feld **Anwendungs-ID** auf **0cdb527f-a8d1-4bf8-9436-b352c68682b2** gesetzt ist. Dieser Wert ist ein fester Wert.
5. Geben Sie in das Feld **LCS-Umgebungs-ID** die ID Ihrer LCS-Umgebung ein.
6. Klicken Sie auf **Speichern** und schließen Sie die Seite.

## <a name="create-key-vault-references"></a>Schlüsseltresorreferenzen erstellen

1. Melden Sie sich bei Ihrem RCS-Konto an.
2. Wählen Sie im Arbeitsbereich **Globalisierungsfunktion** im Abschnitt **Umgebung** die Kachel **Elektronische Rechnungsstellung** aus.
3. Wählen Sie im Aktivitätsbereich auf der Seite **Umgebungseinrichtungen** **Service-Umgebung** und anschließend **Key Vault-Parameter** aus.
4. Wählen Sie **Neu** aus, um eine Schlüsseltresorreferenz zu erstellen.
5. Geben Sie im Feld **Name** den Namen des Schlüsseltresorreferenz ein. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
6. Fügen Sie im Feld **Key Vault-URI** das Schlüsseltresorgeheimnis aus Azure Key Vault ein. Weitere Informationen finden Sie unter [Ein Azure-Speicherkonto und einen Schlüsseltresor erstellen](e-invoicing-create-azure-storage-account-key-vault.md).
7. Wählen Sie **Speichern** aus.

## <a name="create-storage-account-secret"></a>Ein Speicherkontogeheimnis erstellen

1. Wählen Sie im Aktivitätsbereich auf der Seite **Umgebungseinrichtungen** **Service-Umgebung** > **Key Vault-Parameter** aus.
2. Wählen Sie eine **Key Vault-Referenz** und im Abschnitt **Zertifikate** **Hinzufügen** aus.
3. Geben Sie im Feld **Name** den Namen des Speicherkontogeheimnisses ein. Weitere Informationen finden Sie unter [Ein Azure-Speicherkonto und einen Schlüsseltresor erstellen](e-invoicing-create-azure-storage-account-key-vault.md).
4. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
5. Wählen Sie im Feld **Typ** **Geheimnis** aus.
6. Klicken Sie auf **Speichern** und schließen Sie die Seite.

## <a name="create-a-digital-certificate-secret"></a>Ein digitales Zertifikatgeheimnis erstellen

1. Wählen Sie im Aktivitätsbereich auf der Seite **Umgebungseinrichtungen** **Service-Umgebung** und anschließend **Key Vault-Parameter** aus.
2. Wählen Sie eine **Key Vault-Referenz** und dann im Abschnitt **Zertifikate** **Hinzufügen** aus.
3. Geben Sie im Feld **Name** den Namen des digitalen Zertifikatsgeheimnisses ein. Weitere Informationen finden Sie unter [Ein Azure-Speicherkonto und einen Schlüsseltresor erstellen](e-invoicing-create-azure-storage-account-key-vault.md).
4. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
5. Wählen Sie im Feld **Typ** die Option **Zertifikat** aus.
6. Klicken Sie auf **Speichern** und schließen Sie die Seite.

## <a name="create-a-service-environment"></a>Eine Service-Umgebung erstellen

1. Melden Sie sich bei Ihrem RCS-Konto an.
2. Wählen Sie im Arbeitsbereich **Globalisierungsfunktion** im Abschnitt **Umgebung** die Kachel **Elektronische Rechnungsstellung** aus.
3. Wählen Sie im Aktivitätsbereich auf der Seite **Umgebungseinrichtungen** **Service-Umgebung** aus.
4. Wählen Sie **Neu** aus, um eine neue Service-Umgebung zu erstellen.
5. Geben Sie im Feld **Name** den Namen der Umgebung für die elektronische Rechnungsstellung ein. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
6. Wählen Sie im Feld **Storage SAS-Tokengeheimnis** den Namen des Speicherkontogeheimnisses aus, das zur Authentifizierung des Zugriffs auf das Speicherkonto verwendet werden muss.
7. Wählen Sie im Abschnitt **Benutzer** die Option **Hinzufügen** aus, um einen Benutzerhinzuzufügen, der elektronische Rechnungen über die Umgebung senden und eine Verbindung zum Speicherkonto herstellen darf.
8. Geben Sie im Feld **Benutzer-ID** den Alias des Benutzers ein. Geben Sie im Feld **E-Mail** die E-Mail-Adresse des Benutzers ein.
9. Wählen Sie **Speichern** aus.
10. Wenn Ihre landes-/regionsspezifischen Rechnungen zur Anwendung digitaler Signaturen eine Zertifikatskette erfordern, wählen Sie im Aktivitätsbereich die Option **Key Vault-Parameter** und anschließend **Zertifikatskette** aus. Befolgen Sie dann diese Schritte:
    1. Wählen Sie **Neu** aus, um eine Zertifikatskette zu erstellen.
    2. Geben Sie im Feld **Name** den Namen der Zertifikatskette ein. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
    3. Wählen Sie im Abschnitt **Zertifikate** die Option **Hinzufügen** aus, um der Kette ein Zertifikat hinzuzufügen.
    4. Verwenden Sie die Schaltflächen **Oben**- oder **Unten**-Schaltfläche, um die Position des Zertifikats in der Kette zu ändern.
    5. Klicken Sie auf **Speichern** und schließen Sie die Seite.
    6. Schließen Sie die Seite.
11. Wählen Sie im Aktivitätsbereich auf der Seite **Service-Umgebung** die Option **Veröffentlichen** aus, um die Umgebung in der Cloud zu veröffentlichen. Der Wert des Felds **Status** wird in **Veröffentlicht** geändert.

## <a name="create-a-connected-application"></a>Eine verbundene Anwendung erstellen

1. Wählen Sie im Aktivitätsbereich auf der Seite **Umgebungseinrichtungen** **Verbundene Anwendungen** aus.
2. Wählen Sie **Neu** aus, um eine verbundene Anwendung zu erstellen.
3. Geben Sie im Feld **Name** den Namen der zu verbindenden Anwendung ein.
4. Geben Sie im Feld **Anwendung** die URL der Finance- und Supply Chain Management-Umgebung ein, um eine Verbindung herzustellen.
4. Geben Sie im Feld **Mandant** den Mandanten der Finance- und Supply Chain Management-Umgebung ein.
5. Wählen Sie **Speichern** aus.
6. Wählen Sie im Aktivitätsbereich die Option **Verbindung prüfen** aus, um die Verbindung mit der Umgebung zu testen. Schließen Sie nun die Seite.

## <a name="link-connected-applications-to-environments"></a>Verbundene Anwendungen mit Umgebungen verknüpfen

1. Wählen Sie auf der Seite **Umgebungseinrichtungen** die Option **Neu** aus, um einer Umgebung eine verbundene Anwendung zuzuweisen.
2. Wählen Sie im Feld **Verbundene Anwendung** eine verbundene Anwendung aus.
3. Wählen Sie im Feld **Service-Umgebung** eine Service-Umgebung aus.
4. Klicken Sie auf **Speichern** und schließen Sie die Seite.

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a>Einrichten der Integration für die elektronische Rechnungsstellung in Finance und Supply Chain Management

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a>Aktivieren der Integrationsfunktion für die elektronische Rechnungsstellung

1. Melden Sie sich bei Ihrer Finance- oder Supply Chain Management-Instanz an.
2. Suchen Sie im Arbeitsbereich **Funktionsverwaltung** nach der Funktion **Integration für die elektronische Rechnungsstellung**. Wenn diese Funktion nicht auf der Seite angezeigt wird, wählen Sie **Nach Updates suchen** aus.
3. Wählen Sie die Funktion aus und wählen Sie dann **Jetzt aktivieren** aus.

### <a name="set-up-the-service-endpoint-url"></a>Einrichten der Service-Endpunkt-URL

1. Navigieren Sie zu **Organisationsverwaltung \> Einrichtung \> Parameter elektronischer Dokumente**.
2. Geben Sie im Feld **Dienstendpunkt-URL** auf der Registerkarte **Übermittlungsdienst** den entsprechenden Dienstendpunkt für Ihre Azure-Region ein, wie in folgender Tabelle dargestellt.

    | Azure-Rechenzentrumgeografie | Dienst-Endpunkt-URI                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | Vereinigte Staaten              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Europa                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Vereinigtes Königreich             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Asien                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. Geben Sie im Feld **Umgebung** den Namen der Service-Umgebung ein, die in der elektronischen Rechnungsstellung veröffentlicht wurde.
4. Klicken Sie auf **Speichern** und schließen Sie die Seite.

### <a name="enable-flighting-keys"></a>Flighting-Schlüssel aktivieren

Aktivieren Sie Flighting-Schlüssel für Microsoft Dynamics 365 Finance- oder Microsoft Dynamics 365 Supply Chain Management-Versionen 10.0.17 oder früher. 
1. Führen Sie den folgenden SQL-Befehl aus:

    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)
    
    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)

2. Führen Sie einen IISreset-Befehl für alle AOS aus.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
