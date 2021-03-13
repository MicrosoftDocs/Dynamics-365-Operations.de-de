---
title: Erste Schritte in der Add-On-Dienstverwaltung für die elektronische Rechnungsstellung
description: Dieses Thema erläutert die ersten Schritte mit dem Add-On für die elektronische Rechnungsstellung.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 111ec65aa826795125d4a9ce835f72e1a0f41b7b
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104383"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a>Erste Schritte in der Add-On-Dienstverwaltung für die elektronische Rechnungsstellung

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie die Vorgehensweisen in diesem Thema abschließen, müssen die folgenden Voraussetzungen erfüllt sein:

- Sie müssen Zugriff auf Ihr Microsoft Dynamics Lifecycle Services (LCS)-Konto haben.
- Sie müssen über ein LCS-Projekt verfügen, das Version 10.0.13 oder höher von Microsoft Dynamics 365 Finance und Dynamics 365 Supply Chain Management umfasst. Darüber hinaus müssen diese Apps in einer der folgenden Azure-Regionen bereitgestellt werden:

    - USA, Osten
    - USA, Westen
    - Norden, Europa
    - Westen, Europa

- Sie müssen Zugriff auf Ihr RCS-Konto (Dynamics 365 Regulatory Configuration Services) haben.
- Die Globalisierungsfunktion für Ihr RCS-Konto muss in der Funktionsverwaltung aktiviert sein. Weitere Informationen finden Sie unter [Regulatory Configuration Services (RCS) – Globalisierungsfunktionen](rcs-globalization-feature.md).
- Sie müssen einen Schlüsseltresor und ein Speicherkonto in Azure erstellen. Weitere Informationen finden Sie unter [Ein Azure-Speicherkonto und einen Schlüsseltresor erstellen](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a>Das Add-On für Microservices in Lifecycle Services installieren

1. Melden Sie sich bei Ihrem LCS-Konto an.
2. Wählen Sie die Kachel **Verwaltung von Vorschaufunktionen** aus.
3. Wählen Sie im Abschnitt **Verwaltung von Vorschaufunktionen** **E-Invoicing-Dienst** aus.
4. Stellen Sie sicher, dass die Option **Vorschaufunktion aktiviert** auf **Ja** festgelegt ist.

## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a>Richten Sie die Parameter für die RCS-Integration im Add-On für die elektronische Rechnungsstellung ein.

1. Melden Sie sich bei Ihrem RCS-Konto an.
2. Wählen Sie im Arbeitsbereich **Elektronische Berichterstellung** im Abschnitt **Zugehörige Links** **Elektronische Berichterstellungsparameter** aus.
3. Geben Sie im Feld **Dienstendpunkt-URI** auf der Registerkarte **E-Invoicing-Dienst** den entsprechenden Dienstendpunkt für Ihre Azure-Region ein, wie in folgender Tabelle dargestellt.

    | Azure-Rechenzentrumgeografie | Dienst-Endpunkt-URI                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | USA, Osten                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | USA, Westen                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | Norden, Europa                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | Westen, Europa                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. Vergewissern Sie sich, dass das Feld **Anwendungs-ID** auf **0cdb527f-a8d1-4bf8-9436-b352c68682b2** gesetzt ist. Dieser Wert ist ein fester Wert.
5. Geben Sie in das Feld **LCS-Umgebungs-ID** die ID Ihres LCS-Abonnementkontos ein.
6. Klicken Sie auf **Speichern** und schließen Sie die Seite.

## <a name="create-key-vault-secret"></a>Ein Key Vault-Geheimnis erstellen

1. Melden Sie sich bei Ihrem RCS-Konto an.
2. Wählen Sie im Arbeitsbereich **Globalisierungsfunktion** im Abschnitt **Umgebung** die Kachel **Elektronische Rechnungsstellung** aus.
3. Wählen Sie im Aktivitätsbereich auf der Seite **Umgebungseinrichtungen** **Service-Umgebung** und anschließend **Key Vault-Parameter** aus.
4. Wählen Sie **Neu** aus, um ein Schlüsseltresorgeheimnis zu erstellen.
5. Geben Sie im Feld **Name** den Namen des Schlüsseltresorgeheimnisses ein. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
6. Fügen Sie im Feld **Key Vault URI** das Geheimnis aus Azure Key Vault ein.
7. Wählen Sie **Speichern** aus.

## <a name="create-storage-account-secret"></a>Ein Speicherkontogeheimnis erstellen

1. Wählen Sie auf der Seite **Key Vault-Parameter** im Abschnitt **Zertifikate** **Hinzufügen** aus.
2. Geben Sie im Feld **Name** den Namen des Speicherkontogeheimnisses ein. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
3. Wählen Sie im Feld **Typ** die Option **Zertifikat** aus.
4. Klicken Sie auf **Speichern** und schließen Sie die Seite.

## <a name="create-an-electronic-invoicing-add-on-environment"></a>Eine Add-On-Umgebung für die elektronische Rechnungsstellung erstellen

1. Melden Sie sich bei Ihrem RCS-Konto an.
2. Wählen Sie im Arbeitsbereich **Globalisierungsfunktion** im Abschnitt **Umgebung** die Kachel **Elektronische Rechnungsstellung** aus.

## <a name="create-a-service-environment"></a>Eine Service-Umgebung erstellen

1. Wählen Sie im Aktivitätsbereich auf der Seite **Umgebungseinrichtungen** **Service-Umgebung** aus.
2. Wählen Sie **Neu** aus, um eine neue Service-Umgebung zu erstellen.
3. Geben Sie im Feld **Name** den Namen der Umgebung für die elektronische Rechnungsstellung ein. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
4. Wählen Sie im Feld **Speicher SAS-Tokengeheimnis** den Namen des Zertifikats aus, das zur Authentifizierung des Zugriffs auf das Speicherkonto verwendet werden muss.
5. Wählen Sie im Abschnitt **Benutzer** die Option **Hinzufügen** aus, um einen Benutzerhinzuzufügen, der elektronische Rechnungen über die Umgebung senden und eine Verbindung zum Speicherkonto herstellen darf.
6. Geben Sie im Feld **Benutzer-ID** den Alias des Benutzers ein. Geben Sie im Feld **E-Mail** die E-Mail-Adresse des Benutzers ein.
7. Wählen Sie **Speichern** aus.
8. Wenn Ihre landes-/regionsspezifischen Rechnungen zur Anwendung digitaler Signaturen eine Zertifikatskette erfordern, wählen Sie im Aktivitätsbereich die Option **Key Vault-Parameter** und anschließend **Zertifikatskette** aus. Befolgen Sie dann diese Schritte:

    1. Wählen Sie **Neu** aus, um eine Zertifikatskette zu erstellen.
    2. Geben Sie im Feld **Name** den Namen der Zertifikatskette ein. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
    3. Wählen Sie im Abschnitt **Zertifikate** die Option **Hinzufügen** aus, um der Kette ein Zertifikat hinzuzufügen.
    4. Verwenden Sie die Schaltflächen **Oben**- oder **Unten**-Schaltfläche, um die Position des Zertifikats in der Kette zu ändern.
    5. Klicken Sie auf **Speichern** und schließen Sie die Seite.
    6. Schließen Sie die Seite.
9. Wählen Sie im Aktivitätsbereich auf der Seite **Service-Umgebung** die Option **Veröffentlichen** aus, um die Umgebung in der Cloud zu veröffentlichen. Der Wert des Felds **Status** wird in **Veröffentlicht** geändert.

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

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a>Die Add-On-Integration für die elektronische Rechnungsstellung in Finance oder Supply Chain Management einrichten

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a>Aktivieren Sie die Integrationsfunktion für das Add-On für die elektronische Rechnungsstellung.

1. Melden Sie sich bei Ihrer Finance- oder Supply Chain Management-Instanz an.
2. Suchen Sie im Arbeitsbereich **Funktionsverwaltung** nach der Funktion **Integration des Add-Ons für die elektronische Rechnungsstellung**. Wenn diese Funktion nicht auf der Seite angezeigt wird, wählen Sie **Nach Updates suchen** aus.
3. Wählen Sie die Funktion aus und wählen Sie dann **Jetzt aktivieren** aus.

### <a name="set-up-the-service-endpoint-url"></a>Einrichten der Service-Endpunkt-URL

1. Navigieren Sie zu **Organisationsverwaltung \> Einrichtung \> Parameter elektronischer Dokumente**.
2. Geben Sie im Feld **Dienstendpunkt-URL** auf der Registerkarte **Übermittlungsdienst** den entsprechenden Dienstendpunkt für Ihre Azure-Region ein, wie in folgender Tabelle dargestellt.

    | Azure-Rechenzentrumgeografie | Dienstendpunkt-URL                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | USA, Osten                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | USA, Westen                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | Norden, Europa                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | Westen, Europa                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. Geben Sie im Feld **Umgebung** den Namen der Add-On-Umgebung für die elektronische Rechnungsstellung ein.
4. Klicken Sie auf **Speichern** und schließen Sie die Seite.
