---
title: Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung
description: Dieses Thema enthält Informationen, die Ihnen den Einstieg in das Add-On für die elektronische Rechnungsstellung in Microsoft Dynamics 365 Finance und Dynamics 365 Supply Chain Management erleichtern.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 61933bb846383932d7dd73e9c4d3c2db7a515a98
ms.sourcegitcommit: 025561f6a21fe8705493daa290f3f6bfb9f1b962
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2020
ms.locfileid: "3835962"
---
# <a name="get-started-with-the-electronic-invoicing-add-on"></a>Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Dieses Thema enthält Informationen, die Ihnen den Einstieg in das Add-On für die elektronische Rechnungsstellung erleichtern. Zunächst werden Sie durch die Konfigurationsschritte in Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Services (RCS) und Dynamics 365 Finance geführt. Als Nächstes wird der Prozess zum Übermitteln von Dokumenten über den Service mithilfe von Dynamics 365 Finance oder Dynamics 365 Supply Chain Management beschrieben. Sie erfahren außerdem, wie Sie die Übermittlungsprotokolle interpretieren.

## <a name="availability"></a>Verfügbarkeit

Das Add-On für die elektronische Rechnungsstellung ist zunächst für mehrere Länder verfügbar. Das Add-In unterstützt das Erstellen elektronischer Rechnungen und das Übermitteln der folgenden Geschäftsdokumente:

| Land/Region  | Geschäftsdokument                          |
|-----------------|--------------------------------------------|
| Österreich         | Verkaufs- und Projektrechnungen                 |
| Belgien         | Verkaufs- und Projektrechnungen                 |
| Brasilien          | Elektronische Steuerdokumentmodell 55 (NF-e) |
| Dänemark         | Verkaufs- und Projektrechnungen                 |
| Estland         | Verkaufs- und Projektrechnungen                 |
| Finnland         | Verkaufs- und Projektrechnungen                 |
| Frankreich          | Verkaufs- und Projektrechnungen                 |
| Deutschland         | Verkaufs- und Projektrechnungen                 |
| Italien           | Verkaufs- und Projektrechnungen                 |
| Mexiko          | CFDI-Rechnung                               |
| Niederlande     | Verkaufs- und Projektrechnungen                 |
| Norwegen          | Verkaufs- und Projektrechnungen                 |
| Spanien           | Verkaufs- und Projektrechnungen                 |
| Europa          | Verkaufs- und Projektrechnungen im PEPPOL-Format          |
    
## <a name="licensing"></a>Lizenzierung

Sie können das Add-On für die elektronische Rechnungsstellung mit Ihrer aktuellen Lizenz verwenden. Für die Nutzung des Service sind keine zusätzlichen Lizenzen erforderlich.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie die Schritte in diesem Thema abschließen, müssen die folgenden Voraussetzungen erfüllt sein:

- Zugriff auf Ihr LCS-Konto.
- Ein LCS-Bereitstellungsprojekt, das Finance oder Supply Chain Management Version 10.0.12 oder höher enthält.
- Zugriff auf Ihr RCS-Konto.
- Aktivieren Sie die Globalisierungsfunktion für Ihr RCS-Konto über das Modul **Funktionsverwaltung**. Weitere Informationen finden Sie unter [Regulatory Configuration Services (RCS) – Globalisierungsfunktionen](rcs-globalization-feature.md)
- Erstellen Sie einen Schlüsseltresor und ein Speicherkonto in Azure. Weitere Informationen finden Sie unter [Erstellen eines Azure-Speicherkontos und eines Schlüsseltresors](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="overview"></a>Übersicht

Die folgende Abbildung zeigt die fünf Hauptschritte, die Sie in diesem Thema ausführen werden.

![Übersicht über die fünf Schritte in diesem Thema](media/e-invoicing-services-get-started-overview-5-steps.png)

1. **Einrichtung der Azure-Ressourcen:** Konfigurieren Sie den Azure-Speicher und das Hochladen digitaler Zertifikate in Azure Key Vault.
2. **LCS-Einrichtung:** Installieren Sie das Add-In für Microservices.
3. **RCS-Einrichtung:** Richten Sie die Funktionen für Umgebung, Benutzerzugriff und elektronische Rechnungsstellung ein.
4. **Clienteinrichtung:** Richten Sie die Verbindung zwischen dem Client und dem Add-On für die elektronische Rechnungsstellung ein und deaktivieren Sie die alten Funktionen zum Übermitteln und Empfangen von Antworten für elektronische Dokumente.
5. **Rechnungen übermitteln:** Übermitteln Sie elektronische Dokumente über das Add-On für die elektronische Rechnungsstellung und empfangen Sie Antworten.

> [!NOTE]
> Einige Konfigurationsschritte in diesem Thema werden häufig ausgeführt und sind landes-/regionsunabhängig. Die landesspezifischen Schritte und Einrichtungsprozeduren werden in landesspezifischen Themen beschrieben.

## <a name="lcs-setup"></a>LCS-Einstellungen

1. Melden Sie sich bei Ihrem LCS-Konto an.
2. Wählen Sie das LCS-Bereitstellungsprojekt aus. Bevor Sie das Projekt auswählen können, muss es betriebsbereit sein.
3. Wählen Sie auf dem Inforegister **Umgebungs-Add-Ins** die Option **Neues Add-In installieren** aus.
4. Wählen Sie **Übermittlung von Geschäftsdokumenten** aus.
5. Geben Sie im Dialogfeld **Add-In einrichten** in das Feld **AAD-Anwendungs-ID** die ID **091c98b0-a1c9-4b02-b62c-7753395ccabe** ein. Dieser Wert ist ein fester Wert.
6. Geben Sie in das Feld **AAD-Mandanten-ID** die ID Ihres Azure-Abonnementkontos ein.

    ![Einrichten des Add-In-Dialogfelds in LCS](media/e-invoicing-services-get-started-lcs-addin-setup.png)

7. Aktivieren Sie das Kontrollkästchen, um die allgemeinen Geschäftsbedingungen zu akzeptieren.
8. Wählen Sie **Installieren**.

## <a name="rcs-setup"></a>RCS-Einstellungen

Während der RCS-Einrichtung führen Sie folgende Aufgaben aus:

1. Richten Sie den Schlüsseltresor in RCS ein.
2. Richten Sie die RCS-Integration auf dem Add-On-Server für die elektronische Rechnungsstellung ein.
3. Erstellen Sie eine Add-On-Umgebung für die elektronische Rechnungsstellung für Ihre Organisation.

### <a name="set-up-the-key-vault-in-rcs"></a>Einrichten des Schlüsseltresors in RCS

1. Melden Sie sich bei Ihrem RCS-Konto an.
2. Wählen Sie im Arbeitsbereich **Globalisierungsfunktionen** im Abschnitt **Umgebungen** die Kachel **Elektronische Rechnungsstellung** aus.
3. Wählen Sie **Serviceumgebungen** aus.

    ![Auswählen der Serviceumgebungen](media/e-invoicing-services-get-started-select-service-environments.png)

> [!NOTE]
> Die Option **Verbundene Anwendungen** gewährt Zugriff auf die automatische Konfiguration des Add-Ons für die elektronische Rechnungsstellung in Finance oder Supply Management über das RCS. Derzeit befindet sich diese Funktion jedoch noch in der Entwicklung.

4. Wählen Sie im Aktivitätsbereich **Key Vault-Parameter** aus.

    ![Auswählen der Key Vault-Parameter](media/e-invoicing-services-get-started-select-key-vault-parameters.png)

5. Wählen Sie im Aktivitätsbereich **Neu** aus, um einen Schlüsseltresor hinzuzufügen.
6. Geben Sie im Feld **Key Vault URI** den Wert des **DNS-Name**-Attributs der Schlüsseltresorressource ein, die Sie in Azure konfiguriert haben. Informationen dazu, wo Sie den Wert **DNS-Name** finden, sind unter [Erstellen eines Azure-Speicherkontos und eines Schlüsseltresors](e-invoicing-create-azure-storage-account-key-vault.md) zu finden.

    ![Feld „Key Vault URI“](media/e-invoicing-services-get-started-enter-key-vault-uri.png)

7. Wählen Sie auf dem Inforegister **Zertifikate** die Option **Hinzufügen** aus und geben Sie die Namen der digitalen Zertifikate und die wichtigsten Schlüsseltresorgeheimnisse ein. Beide Wertegruppen werden in Azure für die Schlüsseltresorressource konfiguriert.

    ![Hinzufügen von Zertifikaten](media/e-invoicing-services-get-started-add-digital-certificates.png)

8. Wenn für Ihre landes-/regionsspezifische Rechnung eine Zertifikatskette erforderlich ist, um eine digitale Signatur anzuwenden, wählen Sie im Aktivitätsbereich die Option **Zertifikatskette** aus und geben Sie die Reihenfolge der Zertifikate oder Schlüsseltresorgeheimnisse ein, aus denen die Kette besteht.

### <a name="set-up-the-rcs-integration-with-the-electronic-invoicing-add-on-server"></a>Einrichten der RCS-Integration auf dem Add-On-Server für die elektronische Rechnungsstellung

1. Wählen Sie im Arbeitsbereich **Globalisierungsfunktionen** im Abschnitt **Zugehörige Links** den Link **Elektronische Berichterstellungsparameter** aus.
2. Wählen Sie **Hier klicken, um eine Verbindung zu Lifecycle Service herzustellen** aus. Wenn Sie keine Verbindung zu LCS herstellen möchten, wählen Sie **Abbrechen** aus.
3. Geben Sie auf der Registerkarte **Add-On für die elektronische Rechnungsstellung** in das Feld **Dienstendpunkt-URI** `https://businessdocumentsubmission.us.operations365.dynamics.com/` ein.
4. Überprüfen Sie, ob im Feld **Anwendungs-ID** die ID **0cdb527f-a8d1-4bf8-9436-b352c68682b2** angezeigt wird. Dieser Wert ist ein fester Wert.
5. Geben Sie in das Feld **LCS-Umgebungs-ID** die ID Ihres LCS-Abonnementkontos ein.

![Eingeben der Add-On-Parameter für die elektronische Rechnungsstellung](media/e-invoicing-services-get-started-enter-e-invoicing-parameters.png)

### <a name="add-an-electronic-invoicing-add-on-environment"></a>Hinzufügen einer Add-On-Umgebung für die elektronische Rechnungsstellung

Sie können verschiedene Umgebungen für das Add-On für die elektronische Rechnungsstellung erstellen, z. B. Entwicklungs-, Test- oder Produktionsumgebungen.

1. Wählen Sie im Arbeitsbereich **Globalisierungsfunktionen** im Abschnitt **Umgebungen** die Kachel **Elektronische Rechnungsstellung** aus.
2. Wählen Sie **Neu** aus, um eine Umgebung zu erstellen.
3. Geben Sie im **Speicher SAS-Tokenkonto** den Wert des Schlüsseltresorgeheimnisses ein, das Sie im Schlüsseltresor in RCS konfiguriert haben.

    ![Feld „Speicher SAS-Tokenkonto“](media/e-invoicing-services-get-started-enter-sas-token-secret.png)

4. Wählen Sie auf dem Inforegister **Benutzer** die Option **Neu** aus, um Benutzern Zugriff auf diese Umgebung zu gewähren.

    ![Hinzufügen von Servicebenutzern](media/e-invoicing-services-get-started-enter-service-users.png)

5. Wählen Sie im Aktivitätsbereich die Option **Veröffentlichen** aus, um die Umgebung auf dem Add-On-Server für die elektronische Rechnungsstellung zu veröffentlichen.

    ![Schaltfläche „Veröffentlichen“](media/e-invoicing-services-get-started-publish-service-environment.png)

### <a name="e-invoicing-feature-setup"></a>Einrichtung für die Funktion für die elektronische Rechnungsstellung

„Die Funktion für die elektronische Rechnungsstellung“ ist der generische Name für die Ressource, die so konfiguriert und veröffentlicht ist, dass sie den Add-On-Server für die elektronische Rechnungsstellung verwendet. Das Einrichten der Funktion für die elektronische Rechnungsstellung umfasst unter anderem die Verwendung von Konfigurationsformaten der elektronischen Berichterstellung (EB) zum Erstellen konfigurierbarer Export- und Importdateien sowie die Verwendung von Aktivitäten und Aktivitätsabläufen, um die Erstellung konfigurierbarer Regeln zum Senden von Anforderungen, zum Importieren von Antworten und zum Analysieren des Inhalts der Antworten zu ermöglichen.

Aufgrund unterschiedlicher Rechnungsformate und Aktivitätsabläufe ist die Einrichtung der Funktion für die elektronische Rechnungserstellung landes-/regionsabhängig.

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a>Einrichten der Add-On-Integration für die elektronische Rechnungsstellung in Finance oder Supply Chain Management 

Während dieser Einrichtung führen Sie die folgenden Aufgaben aus:

1. Öffnen der Flight-Funktion
2. Aktivieren Sie die Integrationsfunktion für das Add-On für die elektronische Rechnungsstellung, um die Integration in Finance zu ermöglichen.
3. Richten Sie die URL des Endpunkts des Add-Ons für die elektronische Rechnungsstellung ein.
4. Importieren Sie die EB-Konfigurationen, die sich auf die landes-/regionsspezifische Funktion für die elektronische Rechnungsstellung beziehen.
5. Aktivieren Sie die entsprechende landes-/regionsspezifische Funktion für die elektronische Rechnungsstellung.
6. Importieren Sie die BR-Konfigurationen und richten Sie die Antworttypen ein, die erforderlich sind, um Ihr landes-/regionsspezifisches Rechnungsdokument als Ergebnis des Übermittlungsprozesses zu aktualisieren.

### <a name="open-flighted-feature"></a>Öffnen einer per Flighting aktivierten Funktion
Die Funktion zur Integration elektronischer Rechnungen wird per Flighting aktiviert. Flighting ist ein Konzept, bei dem eine Funktion standardmäßig ein- oder ausgeschaltet sein kann. Die folgenden Schritte ermöglichen die Erstellung eines Flight in einer Nicht-Produktionsumgebung. 

1. Führen Sie den folgenden SQL-Befehl aus:

    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)
    
    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)
    
2. Führen Sie nach der obigen Änderung einen IISReset für alle Microsoft Dynamics AX Application Object Server (AOS) durch

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a>Aktivieren Sie die Integrationsfunktion für das Add-On für die elektronische Rechnungsstellung.

1. Melden Sie sich bei Finance oder Supply Chain Management an.
2. Suchen Sie im Arbeitsbereich **Funktionsverwaltung** nach der neuen Funktion **Integration des konfigurierbaren Add-Ons für die elektronische Rechnungsstellung**. Wenn die Funktion auf der Seite „Funktionsverwaltung“ weiterhin nicht angezeigt wird, führen Sie die Funktion **Nach Updates suchen** aus.
3. Wählen Sie die Funktion aus und wählen Sie dann **Jetzt aktivieren** aus.

### <a name="set-up-the-service-endpoint-url"></a>Einrichten der Service-Endpunkt-URL

1. Navigieren Sie zu **Organisationsverwaltung \> Einrichtung \> Parameter elektronischer Dokumente**.
2. Geben Sie auf der Registerkarte **Abonnementservice** in das Feld **Dienstendpunkt-URL** `https://businessdocumentsubmission.us.operations365.dynamics.com/` ein.
3. Geben Sie in das Feld **Umgebung** den Namen der Add-On-Umgebung für die elektronische Rechnungsstellung ein, die Sie während der RCS-Einrichtung erstellt haben.

![Eingeben von Serviceparametern](media/e-invoicing-services-get-started-enter-service-endpoint.png)

### <a name="import-the-er-configurations"></a>Importieren der EB-Konfigurationen

Damit Geschäftsdaten erfasst und an das Add-On für die elektronische Rechnungsstellung gesendet werden können, müssen Sie das EB-Datenmodell und die EB-Datenmodellkonfiguration importieren, die sich auf die landes-/regionsspezifische Funktion für die elektronische Rechnungsstellung beziehen, die Sie verwenden möchten.

1. Wählen Sie im Arbeitsbereich **Elektronische Berichterstellung** im Abschnitt **Konfigurationsanbieter** die Kachel **Microsoft** aus. Stellen Sie sicher, dass dieser Konfigurationsanbieter auf **Aktiv** festgelegt ist. Weitere Informationen zum Festlegen eines Anbieters auf **Aktiv** finden Sie unter [Erstellen von Konfigurationsanbietern und Markieren als aktiv](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. Wählen Sie **Repositorys** aus.
4. Wählen Sie **Globale Ressource** und dann **Öffnen** aus.
5. Wählen Sie im Dialogfeld **Mit Lifecycle Services verbinden** die Option **Hier klicken, um eine Verbindung zu Lifecycle Service herzustellen** aus.
6. Abhängig von dem Land oder der Region, in der Sie die Funktion für die elektronische Rechnungsstellung verwenden möchten, müssen Sie das entsprechende Datenmodell, die Datenmodellzuordnung und die Formate importieren. Informationen zu den EB-Konfigurationen, die Sie importieren sollten, finden Sie im landes-/regionsspezifischen Thema „Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung“.
7. Importieren Sie **Kontextmodell Debitorenrechnung**. Dieses Modell enthält zusätzliche Parameter, die unter anderem die Umgebung in Finance beschreiben, die für das Add-On für die elektronische Rechnungsstellung während der Übermittlung von Geschäftsdaten verwendet wird.

### <a name="turn-on-countryregion-specific-e-invoicing-features"></a><a name="region-specific"></a>Aktivieren landes-/regionsspezifischer Funktion für die elektronische Rechnungsstellung

Um landes-/regionsspezifische Funktionen für die elektronische Rechnungsstellung zu aktivieren, damit sie mit dem Add-On für die elektronische Rechnungsstellung funktionieren, müssen Sie die Funktion in jeder juristischen Person aktivieren, in der Sie sie verwenden möchten. Anschließend kann die alte Integration der elektronischen Rechnungsstellung nicht mehr verwendet werden und die Integration mit dem neuen Add-On für die elektronische Rechnungsstellung wird aktiviert.

1. Navigieren Sie zu **Organisationsverwaltung \> Einrichtung \> Parameter elektronischer Dokumente**.
2. Aktivieren Sie auf der Registerkarte **Funktionen** in der Zeile für die Funktion, die sich auf Ihre landes-/regionsspezifische Funktion für die elektronische Rechnungsstellung bezieht, das Kontrollkästchen in der Spalte **Aktiviert**. Informationen zu den Funktionen, die Sie aktivieren sollten, finden Sie im landes-/regionsspezifischen Thema „Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung“.

![Aktivieren der Funktion für die elektronische Rechnungsstellung](media/e-invoicing-services-get-started-enable-invoicing-feature.png)

> [!NOTE]
> Bei mehreren juristischen Personen, die für verschiedene Länder oder Regionen konfiguriert sind, können Sie die landes-/regionsspezifische Funktion für jede juristische Person einzeln aktivieren.

### <a name="import-er-configurations-and-set-up-the-response-types-to-update-your-countryregion-specific-invoice-document"></a>Importieren Sie EB-Konfigurationen und richten Sie die Antworttypen ein, um Ihr landes-/regionsspezifisches Rechnungsdokument zu aktualisieren

Wenn für das übermittelte Rechnungsdokument nach der Antwort auf die Übermittlung an die staatlichen Autorisierungsdienste eine Aktualisierung erforderlich ist, müssen Sie ein spezielles EB-Datenmodell und Konfigurationen importieren, damit der Status des Rechnungsdokuments oder eines anderen zusätzlichen Felds aktualisiert werden kann.

1. Wählen Sie im Arbeitsbereich **Elektronische Berichterstellung** im Abschnitt **Konfigurationsanbieter** die Kachel **Microsoft** aus.
2. Wählen Sie **Repositorys** aus.
3. Wählen Sie **Globale Ressource** und dann **Öffnen** aus.
4. Importieren Sie **Antwortnachrichtenmodell**, **Importformat für Antwortnachrichten**, **Zuordnung des Antwortnachrichtenmodells zu Ziel** und **Importformat für Dateiinhalte**.
5. Navigieren Sie zu **Organisationsverwaltung \> Einrichtung \> Parameter elektronischer Dokumente**.
6. Wählen Sie auf der Registerkarte **Elektronisches Dokument** die Option **Hinzufügen** aus, um den Namen der Tabelle einzugeben, die sich auf Ihr landes-/regionsspezifisches Rechnungsdokument bezieht. Informationen zu den Tabellennamen, die Sie auswählen sollten, finden Sie im landes-/regionsspezifischen Thema „Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung“.
7. Wählen Sie **Antworttypen** aus, um die Antworttypen zu konfigurieren. Informationen zu den Tabellennamen, die Sie auswählen sollten, finden Sie im landes-/regionsspezifischen Thema „Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung“.

![Einrichten von Antworttypen](media/e-invoicing-services-get-started-set-up-response-types.png)

## <a name="e-invoicing-feature-names-by-country"></a>Namen der Funktionen für die elektronische Rechnungsstellung nach Land 
In der folgenden Tabelle werden andere Funktionen für die elektronische Rechnungsstellung beschrieben, die aus dem globalen Repository für elektronische Berichte heruntergeladen werden können, um elektronische Rechnungen zu generieren.
In RCS können Sie die in dieser Tabelle aufgeführten Funktionen für die elektronische Rechnungsstellung, die EB-Konfigurationen und die verfügbaren Funktionseinrichtungen zur elektronische Rechnungsstellung herunterladen.
In Finance können Sie die zugehörigen Funktionsreferenzen auf der Seite **Parameter elektronischer Dokumente** aktivieren, um elektronische Rechnungen für diese Länder auszustellen. Weitere Informationen finden Sie im Abschnitt [Aktivieren landes-/regionsspezifischer Funktion für die elektronische Rechnungsstellung](#region-specific) weiter oben in diesem Thema.

| Funktionsname                      | Beschreibung                                 | ER-Konfigurationen                                                                                                  | Einrichtungen                                                                                                                                                         | Land/Region  | Funktionsreferenz      |
|-----------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------|------------------------|
| Elektronische Rechnungen für Österreich (AT) | Verkaufs- und Projektrechnungen für Österreich      | - OIOUBL Verkaufsrechnung <br>- OIOUBL Projektrechnung <br>- OIOUBL Verkaufsgutschrift <br>- OIOUBL Projektgutschrift | - Generierung von Verkaufsrechnungen (AT) <br>- Generierung von Projektrechnungen (AT) <br>- Generierung von Verkaufsgutschriften (AT) <br>- Generierung von Projektgutschriften (AT)         | Österreich         | EUR-00023              |
| Elektronische Rechnungen für Belgien (BE)   | Verkaufs- und Projektrechnungen für Belgien      | - UBL Verkaufsrechnung BE <br>- UBL Projektrechnung BE <br>- UBL Projektgutschrift BE <br>- UBL Verkaufsgutschrift BE | - Generierung von Verkaufsrechnungen (BE)<br>- Generierung von Projektrechnungen (BE) <br>- Generierung von Verkaufsgutschriften (BE) <br>- Generierung von Projektgutschriften (BE)         | Belgien         | EUR-00023              |
| Elektronische Rechnungen für Dänemark (DK)    | Verkaufs- und Projektrechnungen für Dänemark      | - OIOUBL Verkaufsrechnung <br>- OIOUBL Projektrechnung <br>- OIOUBL Verkaufsgutschrift <br>- OIOUBL Projektgutschrift | - Generierung von Verkaufsrechnungen (DK) <br>- Generierung von Projektrechnungen (DK) <br>- Generierung von Verkaufsgutschriften (DK)<br>- Generierung von Projektgutschriften (DK)         | Dänemark         | EUR-00023<br> DK-00001 |
| Elektronische Rechnungen für die Niederlande (NL)     | Verkaufs- und Projektrechnungen für die Niederlande  | - UBL Verkaufsrechnung NL <br>- UBL Projektrechnung NL <br>- UBL Verkaufsgutschrift NL <br>- UBL Projektgutschrift NL | - Generierung von Verkaufsrechnungen (NL) <br> - Generierung von Projektrechnungen (NL) <br> - Generierung von Verkaufsgutschriften (NL) <br>- Generierung von Projektgutschriften (NL)          | Die Niederlande | EUR-00023              |
| Elektronische Rechnungen für Estland (EE)  | Verkaufs- und Projektrechnungen für Estland      | - Verkaufsrechnung (EE) <br> - Projektrechnung (EE)                                                                     | - Generierung von Verkaufsrechnungen (EE) <br>- Generierung von Projektrechnungen (EE)                                                                                           | Estland         | EUR-00023              |
| Elektronische Rechnungen für Finnland (FI)   | Verkaufs- und Projektrechnungen für Finnland      | - Verkaufsrechnung (FI) <br>- Generierung von Projektrechnungen (FI)                                                          | - Generierung von Verkaufsrechnungen (FI) <br>- Generierung von Projektrechnungen (FI)                                                                                           | Finnland         | EUR-00023              |
| Elektronische Rechnungen für Frankreich (FR)    | Verkaufs- und Projektrechnungen für Frankreich    | - UBL Verkaufsrechnung FR <br> - UBL Projektrechnung FR <br> - UBL Verkaufsgutschrift FR <br>- UBL Projektgutschrift FR | - Generierung von Verkaufsrechnungen (FR) <br> - Generierung von Projektrechnungen (FR) <br>- Generierung von Verkaufsgutschriften (FR) <br>- Generierung von Projektgutschriften (FR)         | Frankreich          | EUR-00023              |
| Elektronische Rechnungen für Deutschland (DE)    | Verkaufs- und Projektrechnungen für Deutschland      |- Verkaufsrechnung (DE) <br> - Projektrechnung <DE>                                                                     | - Generierung von Verkaufsrechnungen (DE) <br>- Generierung von Projektrechnungen (DE)                                                                                           | Deutschland         | EUR-00023              |
| Elektronische Rechnungen für Norwegen (NO) | Verkaufs- und Projektrechnungen für Norwegen       | - OIOUBL Verkaufsrechnung <br>- OIOUBL Projektrechnung <br>- OIOUBL Verkaufsgutschrift <br>- OIOUBL Projektgutschrift | - Generierung von Verkaufsrechnungen (NO) <br>- Generierung von Projektrechnungen (NO) <br>- Generierung von Verkaufsgutschriften (NO) <br>- Generierung von Projektgutschriften (NO)          | Norwegen          | EUR-00023<br> NO-00010 |
| Elektronische Rechnungen für Spanien (ES)   | Verkaufs- und Projektrechnungen für Spanien        | - Verkaufsrechnung (ES) <br>- Projektrechnung (ES)                                                                     | - Generierung von Verkaufsrechnungen (ES) <br>- Generierung von Projektrechnungen (ES)                                                                                           | Spanien           | EUR-00023 <br>ES-00025 |
| Elektronische Rechnungen für Italien (IT)   | Verkaufs- und Projektrechnungen für Italien        | - (Vorschau) Verkaufsrechnung (IT) <br> - Projektrechnung (IT)                                                           | - Verkaufsrechnung <br> - Projektrechnung                                                                                                                           | Italien           | EUR-00023 <br>IT-00036 |
| Elektronische Rechnungen im PEPPOL-Format         | Generierung von Verkaufs- und Projektrechnungen im PEPPOL-Format | - Verkaufsrechnung im PEPPOL-Format <br>- Projektrechnung im PEPPOL-Format <br>- Verkaufsgutschrift im PEPPOL-Format <br> - Projektgutschrift im PEPPOL-Format | - Generierung von Verkaufsrechnungen im PEPPOL-Format <br>- Generierung von Projektrechnungen im PEPPOL-Format <br>- Generierung von Verkaufsgutschriften im PEPPOL-Format <br>- Generierung von Projektgutschriften im PEPPOL-Format |                 | EUR-00023              |


## <a name="electronic-invoice-processing-in-finance-and-supply-chain-management"></a>Elektronische Rechnungsverarbeitung in Finance und Supply Chain Management

Während der Verarbeitung führen Sie folgende Aufgaben aus:

1. Übermitteln Sie ein Geschäftsdokument (Rechnung) über das Add-On für die elektronische Rechnungsstellung.
2. Zeigen Sie die Ausführungsprotokolle für die Übermittlung an.

### <a name="submit-business-documents"></a>Übermitteln von Geschäftsdokumenten

Während des regulären Übermittlungsprozesses erfolgt die Kommunikation zwischen dem Kunden und dem Add-On für die elektronische Rechnungsstellung bidirektional. Der Zweck besteht darin, zwei Hauptaufgaben bei der Übermittlung elektronischer Dokumente zu erledigen:

1. Senden Sie alle elektronischen Dokumente, deren Übermittlung von Finance aussteht und die den korrekten Status für die Übermittlung haben und die Auswahlkriterien erfüllen.
2. Importieren Sie in Finance die Antwort, die das Add-On für die elektronische Rechnungsstellung für zuvor übermittelte elektronische Dokumente zurückgibt. Nach dem Import werden die Antworten analysiert und der Status der Geschäftsdokumente entsprechend aktualisiert.

Sie können Geschäftsdokumente entweder manuell oder basierend auf Ihren Zeitplananforderungen übermitteln.

1. Navigieren Sie zu **Organisationsverwaltung \> Periodisch \> Elektronische Dokumente \> Elektronische Dokumente übermitteln**.
2. Legen Sie für die erste Übermittlung irgendeines Dokuments immer die Option **Dokumente erneut übermitteln** auf **Nein** fest. Wenn Sie ein Dokument erneut über den Service übermitteln müssen, legen Sie diese Option auf **Ja** fest.
3. Wählen Sie auf dem Inforegister **Einzuschließende Datensätze** die Option **Filtern** aus, um das Dialogfeld **Anfrage** zu öffnen, in dem Sie eine Abfrage erstellen können, um Dokumente für die Übermittlung auszuwählen.

![Dialogfeld „Elektronische Dokumente übermitteln“](media/e-invoicing-services-get-started-submission-form.png)

### <a name="filter-query"></a>Filterabfrage

1. Geben Sie im Dialogfeld **Anfrage** auf der Registerkarte **Bereich** Filterkriterien an, indem Sie die Felder **Tabelle**, **Abgeleitete Tabelle**, **Feld** und **Kriterien** verwenden.
2. Wählen Sie **Hinzufügen** aus, um so viele zusätzliche Kriterien hinzuzufügen, wie Sie zur Auswahl der Geschäftsdokumente benötigen.

    ![Einrichten von Filterkriterien für Übermittlungen](media/e-invoicing-services-get-started-set-up-submission-filter-criteria.png)

3. Wählen Sie **OK** aus, um das Dialogfeld **Anfrage** zu schließen.
4. Wählen Sie **OK** aus, um die ausgewählten Geschäftsdokumente an das Add-On für die elektronische Rechnungsstellung zu übermitteln.

    > [!NOTE]
    > Bei Ihrem ersten Versuch, ein Dokument über den Service zu übermitteln, werden Sie aufgefordert, die Verbindung mit dem Add-On für die elektronische Rechnungsstellung zu bestätigen. Wählen Sie **Hier klicken, um eine Verbindung mit dem Electronic Document Submission Service herzustellen** aus.
    >
    > ![Herstellen einer Verbindung zum Meldungsfeld Electronic Document Submission Service](media/e-invoicing-services-get-started-dialog-form-connect-e-Invoicing-services.png)
    >
    > Wenn die Verbindung erfolgreich hergestellt wurde, erhalten Sie eine Bestätigungsnachricht.
    >
    > ![Bestätigung der Verbindung zum Add-On für die elektronische Rechnungsstellung](media/e-invoicing-services-get-started-confirmation-connection-e-invoicing-services.png)

5. Schließen Sie das Dialogfeld.

> [!NOTE]
> Nach jeder Übermittlung zeigt das Aktionszentrum die Anzahl der übermittelten Dokumente an.
>
> ![Aktionszentrumsmeldungen](media/e-invoicing-services-get-started-view-action-center-messages.png)

### <a name="submission-by-batch"></a>Batchübermittlung

Anstatt Dokumente manuell zu übermitteln, können Sie den Übermittlungsprozess automatisieren und im Hintergrund ausführen, basierend auf einer konfigurierten Häufigkeit der Batchausführung.

1. Legen Sie im Dialogfeld **Elektronische Dokumente übermitteln** auf dem Inforegister **Im Hintergrund ausführen** die Option **Batchverarbeitung** auf **Ja** fest.
2. Konfigurieren Sie auf der Registerkarte **Wiederholung** die Häufigkeit der Batchverarbeitung.

![Einrichten der Batchübermittlung](media/e-invoicing-services-get-started-set-up-submission-batch.png)

### <a name="view-all-submission-logs"></a>Anzeigen aller Übermittlungsprotokolle

1. Navigieren Sie zu **Organisationsverwaltung \> Periodisch \> Elektronische Dokumente \> Übermittlungsprotokoll für elektronische Dokumente**.
2. Wählen Sie im Feld **Dokumenttyp** den Dokumenttyp aus, nach dem gefiltert werden soll.

    ![Auswählen des Dokumenttyps, für den Übermittlungsprotokolle angezeigt werden sollen](media/e-invoicing-services-get-started-select-document-type-for-viewing-submission-log.png)

    > [!IMPORTANT]
    > Der Wert, der in der Spalte **Übermittlungsstatus** angezeigt wird, gibt den Status an, der sich auf den Abschluss des Übermittlungsprozesses selbst bezieht. Er zeigt an, ob der in RCS konfigurierte Ablauf von Aktivitäten bis zum Ende ausgeführt wurde, unabhängig davon, ob das elektronische Dokument genehmigt oder abgelehnt wurde. Der Wert in der Spalte **Übermittlungsstatus** gibt nicht den Status des übermittelten Dokuments an. Sie können den Status des übermittelten Dokuments (d. h., ob das Dokument genehmigt oder abgelehnt wurde) auf dem Inforegister **Aktivitätsprotokoll verarbeiten** in den Details des Übermittlungsprotokolls anzeigen, wie im Folgenden beschrieben.

3. Wählen Sie im Aktivitätsbereich **Anfragen \> Übermittlungsdetails** aus.
4. Zeigen Sie die Details des Übermittlungsprotokolls an.

    ![Details des Übermittlungsprotokolls](media/e-invoicing-services-get-started-view-submission-log-form.png)

Die im Übermittlungsprotokoll angezeigten Ergebnisse hängen davon ab, wie die Funktion für die elektronische Rechnungserstellung in RCS eingerichtet wurde. Unabhängig von der Einrichtung enthält das Übermittlungsprotokoll jedoch immer drei Inforegister:

- **Verarbeitungsaktivitäten** – Dieses Inforegister zeigt das Ausführungsprotokoll für die Aktionen an, die in der in RCS eingerichteten Funktionsversion konfiguriert sind. Die Spalte **Status** zeigt an, ob die Aktion erfolgreich ausgeführt wurde.
- **Aktionsdateien** – Dieses Inforegister zeigt die Zwischendateien an, die während der Ausführung der Aktionen generiert wurden. Sie können **Anzeigen** auswählen, um die Datei herunterzuladen und ihren Inhalt anzuzeigen.
- **Aktivitätsprotokoll verarbeiten** – Dieses Inforegister zeigt die Ergebnisse der Kommunikation zwischen dem Add-On für die elektronische Rechnungsstellung und dem Ziel-Webdienst an. Außerdem wird angezeigt, was von der Verarbeitung durch den Webdienst zurückgegeben wurde.

## <a name="related-topics"></a>Verwandte Themen

- [Übersicht über das Add-On für die elektronische Rechnungsstellung](e-invoicing-service-overview.md)
- [Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung für Brasilien](e-invoicing-bra-get-started.md)
- [Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung für Mexiko](e-invoicing-mex-get-started.md)
- [Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung für Italien](e-invoicing-ita-get-started.md)
- [Einrichten des Add-Ons für die elektronische Rechnungsstellung](e-invoicing-setup.md)
