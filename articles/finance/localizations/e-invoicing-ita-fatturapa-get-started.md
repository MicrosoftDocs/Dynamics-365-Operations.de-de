---
title: Direkte Integration des italienischen FatturaPA mit SDI einrichten
description: Dieses Thema bietet Informationen, die Ihnen den Einstieg in die elektronische Rechnungsstellung für Italien und die Einrichtung der direkten Integration des italienischen FatturaPA mit dem Exchange-System (SDI) erleichtern.
author: abaryshnikov
ms.date: 01/15/2022
ms.topic: article
audience: Application User, Developer
ms.reviewer: kfend
ms.search.region: Global
ms.author: abaryshnikov
ms.search.validFrom: 2021-10-18
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 73cb08c880d7b3459201acfc7aeaa8d0dee1674f
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2022
ms.locfileid: "7984802"
---
# <a name="set-up-direct-integration-of-italian-fatturapa-with-sdi"></a>Direkte Integration des italienischen FatturaPA mit SDI einrichten

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Die elektronische Rechnungsstellung für Italien unterstützt derzeit möglicherweise nicht alle Funktionen, die für elektronische Rechnungen in Microsoft Dynamics 365 Finance und Dynamics 365 Supply Chain Management verfügbar sind.

Dieses Thema enthält Informationen, die Ihnen den Einstieg in die elektronische Rechnungsstellung für Italien in Finance und Supply Chain Management erleichtern. Es führt Sie durch die Konfigurationsschritte, die in Regulatory Configuration Services (RCS) sowie in Finance länder-/regionenabhängig sind. Diese Schritte ergänzen die Schritte, die in [Los geht's  mit der elektronischen Rechnungsstellung](e-invoicing-get-started.md) beschrieben sind.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie die Schritte in diesem Thema abschließen können, müssen die folgenden Voraussetzungen erfülltl sein.

- Ergänzen Sie die Schritte unter [Erste Schritte mit der Dienstverwaltung für die elektronische Rechnungsstellung](e-invoicing-get-started.md).
- Importieren Sie die **Italienisch FatturaPA (IT)** elektronische Rechnungsfunktion in RCS aus dem globalen Repository. Weitere Informationen finden Sie unter [Importieren Sie eine Funktion für die elektronische Rechnungsstellung vom Microsoft-Konfigurationsanbieter](e-invoicing-get-started.md#import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider) Abschnitt des zuvor erwähnten Themas Erste Schritte mit der elektronischen Rechnungsstellung.
- Fügen Sie Links von den erforderlichen Zertifikaten zur Serviceumgebung hinzu. Zu den erforderlichen Zertifikaten gehören das Zertifikat für die digitale Signatur, das Zertifikat der Zertifizierungsstelle (CA) und das Client-Zertifikat. Weitere Informationen unter [Erstellen Sie ein digitales Zertifikatgeheimnis](e-invoicing-get-started-service-administration.md#create-a-digital-certificate-secret), wie im Abschnitt Erste Schritte für die elektronische Rechnungsstellung beschrieben ist.

## <a name="country-specific-configuration-for-the-italian-fatturapa-it-electronic-invoicing-feature"></a>Länderspezifische Konfiguration für die elektronische Rechnungsstellungsfunktion der italienischen FatturaPA (IT)

Führen Sie die folgende Prozedur aus, bevor Sie die Anwendungseinrichtung in Ihrer verbundenen Finance oder Supply Chain Management Anwendung bereitstellen.

Dieser Abschnitt ergänzt den Abschnitt [Länderspezifische Konfiguration der Anwendungseinrichtung](e-invoicing-get-started.md#country-specific-configuration-of-application-setup) im Thema Erste Schritte mit der elektronischen Rechnungsstellung.

### <a name="create-a-new-feature"></a>Neue Feature erstellen

1. Melden Sie sich bei RCS an.
2. Im **Elektronische Berichterstattung** Arbeitsbereich, im Abschnitt **Konfigurationsanbieter** markieren Sie den Konfigurationsanbieter Ihres Unternehmens als aktiv.
3. Wählen Sie im Abschnitt **Funktionen** des Arbeitsbereichs **Globalisierungsfunktion** die Kachel **Elektronische Rechnungsstellung** aus.
4. Auf der **Elektronische Rechnungsfunktionen** Seite, wählen Sie **Hinzufügen** \> **Vasierend auf vorhandener Funktion**.
5. Unter **Microsoft-Konfigurationsanbieter**, wählen Sie **Italienisch FatturaPA (IT)** als Basisfunktion einen Namen ein und wählen Sie dann **Funktion erstellen**.

### <a name="set-up-application-specific-parameters"></a>Anwendungsspezifische Parameter einrichten

1. Auf der **Elektronische Rechnungsfunktionen** Seite, wählen Sie die Feature zum Bearbeiten aus.
2. Überprüfen Sie auf der Registerkarte **Versionen**, ob die **Entwurf**-Version ausgewählt ist.
3. Wählen Sie auf der Registerkarte **Konfigurationen** **Anwendungsspezifische Parametereinstellung** aus.
4. Im **Lookup** Abschnitt, stellen Sie sicher, dass die -Suche **Liste der Natura-Reverse-Charge-Unterkategorien** ausgewählt ist.
5. Wählen Sie im **Bedingungen**-Abschnitt **Hinzufügen** aus.
6. Fügen Sie für jede im System definierte Unterkategorie spezifische Bedingungen hinzu und speichern Sie dann Ihre Änderungen.

    > [!NOTE]
    > In der Spalte **Name** können Sie die **\*Leer\*** oder **\*Nicht leer\*** Platzhalterwerte anstelle eines bestimmten Werts auswählen.

### <a name="configure-a-processing-pipeline-for-export"></a>Konfigurieren Sie eine Verarbeitungspipeline für den Export

1. Auf der **Elektronische Rechnungsfunktionen** Seite, wählen Sie die Feature zum Bearbeiten aus.
2. Wählen Sie auf der Registerkarte **Einstellungen** **Verkaufsrechnungen** und dann **Bearbeiten** aus.
3. Im **Verarbeitungspipeline** Abschnitt, gehen Sie die Aktionen durch und legen Sie alle erforderlichen Felder fest:

    - Für die **Dokument unterschreiben** Aktion, im Feld **Zertifikatname** geben Sie das Zertifikat für die digitale Signatur an.
    - Für die **Übermitteln** Aktion, legen Sie die **URL-Adresse** und **Zertifikate** Felder fest. Der Wert des Felds **Zertifikate** ist eine Kette von Zertifikaten, von denen das erste das Root-CA-Zertifikat (caentrate.cer) und das zweite das Client-Zertifikat ist.

4. Wählen Sie **Bestätigen**, um sicherzustellen, dass alle erforderlichen Felder festgelegt wurden.
5. Speichern Sie Ihre Änderungen und schließen Sie die Seite.
6. Wählen Sie auf der Registerkarte **Einrichten** **Projektrechnungen** und dann **Bearbeiten** aus.
7. Wiederholen Sie die Schritte 3 bis 5 für Projektrechnungen.

### <a name="configure-the-processing-pipeline-for-import"></a>Konfigurieren Sie eine Verarbeitungspipeline für den Import

1. Auf der **Elektronische Rechnungsfunktionen** Seite, wählen Sie die Feature zum Bearbeiten aus.
2. Wählen Sie auf der Registerkarte **Einrichten** **Rechnungen importieren** und dann **Bearbeiten** aus.
3. Geben Sie im Abschnitt **Datenkanal** in der Registerkarte **Parameter** im Feld **Datenkanal** eine Zeichenfolge für den Wert ein.
4. Auf der **Anwendbarkeitsregeln** Registerkarte, legen Sie die Felder für die Einrichtung fest. Sie können die Standardeinstellung **Kanal**-Klausel verwenden, indem Sie den Wert übergeben, den Sie für das **Datenkanal** Feld im vorherigen Schritt zum **Wert** Bereich festgelegt haben.

    ![Einrichten von Anwendbarkeitsregeln.](media/e-invoicing-ita-fatturapa-get-started-apprules-setup.png)

5. Wählen Sie **Bestätigen**, um sicherzustellen, dass alle erforderlichen Felder festgelegt wurden.

### <a name="deploy-the-feature"></a>Die Feature bereitstellen

1. Die Featre für die Service-Umgebung beenden, veröffentlichen und bereitstellen. Weitere Informationen finden Sie im Abschnitt [Bereitstellen der Funktion Elektronische Rechnungsstellung für die Service-Umgebung](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment) des zuvor erwähnten Themas Erste Schritte mit der elektronischen Rechnungsstellung.
2. Stellen Sie die Funktion für die verbundene Anwendung bereit. Weitere Informationen finden Sie im Abschnitt [Bereitstellen der Feature Elektronische Rechnungsstellung für die verbundene Anwendung](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-connected-application) des zuvor erwähnten Themas Erste Schritte mit der elektronischen Rechnungsstellung.

### <a name="set-up-finance"></a>Finanzen einrichten

1. Melden Sie sich in Ihrer Finance-Umgebung an.
2. Wählen Sie im Arbeitsbereich **Elektronische Berichterstellung** im Abschnitt **Konfigurationsanbieter** die Kachel **Microsoft** aus.
3. Wählen Sie **Repositories** \> **Global** \> **Öffnen**.
4. Wählen und importieren Sie die **Kontextmodell für Kundenrechnungen** und **Lieferantenrechnungsimport (IT)** Konfigurationen.
5. Navigieren Sie zu **Organisationsverwaltung** \> **Einrichtung** \> **Parameter elektronischer Dokumente**.
6. Auf der **Merkmale** Registerkarte, suchen und wählen Sie die Funktion **Italienische elektronische Rechnung** und wählen Sie dann das Kontrollkästchen **Aktivieren** aus.
7. Auf der Registerkarte **Elektronisches Dokument** stellen Sie sicher, dass die Felder für **Kundenrechnungsjournal** und **Projektrechnung** gemäß den Angaben unter [Konfigurieren Sie die Anwendungseinrichtung](e-invoicing-get-started.md#configure-the-application-setup) festgelegt sind.

### <a name="set-up-vendor-invoice-import"></a>Das Importieren von Kreditorenrechnungen einrichten 

1. In Finance im Arbeitsbereich **Elektronische Berichterstattung** im Abschnitt **Konfigurationsanbieter** markieren Sie den Konfigurationsanbieter Ihres Unternehmens als aktiv.
2. Wählen Sie **Berichterstellungskonfigurationen** aus.
3. Wählen **Kontextmodell Debitorenrechnung** und wählen dann **Konfiguration erstellen** aus.
4. Wählen Sie **Vom Namen ableiten: Kontextmodell Debitorenrechnung, Microsoft** aus, um eine abgeleitete Konfiguration zu erstellen.
5. Wählen Sie in der Version **Entwurf** **Designer** aus.
6. Wählen Sie im Baum **Datenmodell** **Zuordnungsmodell an Datenquelle**.
7. Wählen Sie im Baum **Definition** die Option **DataChannel** und wählen Sie dann **Designer** aus.
8. Erweitern Sie im Baum **Datenquellen** den **\$Kontext\_Kanal** Container.
9. Wählen Sie im Feld **Wert** **Bearbeiten** aus. 
10. Geben Sie den Namen des Datenkanals ein. Der Name sollte maximal 10 Zeichen lang sein. Es sollte dem Wert vom **Datenkanal** Parameter des Datenkanals für die Funktion Elektronische Rechnungsstellung in RCS entsprechen.
11. Speichern Sie Ihre Änderungen und gehen Sie dann zu **Berichtskonfigurationen** \> **Vollständige Konfigurationsversion**.
12. Wählen Sie auf der Registerkarte **Externe Kanäle** in Abschnitt **Kanäle** udn wählen **Hinzufügen** aus.
13. Im **Kanal** Feld, geben Sie einen **\$Kontextkanal** Wert ein.
14. Geben Sie in den Feldern **Beschreibung** und **Unternehmen** Werte ein.
15. Wählen Sie im Feld **Dokumentkontext** die neu abgeleitete Konfiguration, die Sie von **Kontextmodell Kundenrechnung** erhalten haben aus. Die Zuordnungsbeschreibung sollte **Datenkanalkontext** lauten.
16. Wählen Sie auf der Registerkarte **Quellen importieren** die Option **Hinzufügen** aus, und legen Sie dann die folgenden Werte fest:

    - **Name:** OutputFile
    - **Name der Datenentität:** Kopf der Kreditorenrechnung (**Datenentität:** VendorInvoiceHeaderEntity)
    - **Modellzuordnung:** Lieferantenrechnungsimport (IT)

> [!NOTE]
> Wenn Sie Kreditorenrechnungen aus verschiedenen Quellen importiert haben, können Sie mehrere externe Kanäle und mehrere abgeleitete Konfigurationen mit unterschiedlichen **\$Kontextkanal** Werten erstellen. Sie möchten beispielsweise Kreditorenrechnungen für verschiedene juristische Personen importieren.

## <a name="proxy-server-setup"></a>Einrichtung des Proxy-Servers

Dieser Abschnitt enthält Informationen, die Ihnen beim Einrichten und Konfigurieren des Proxy-Dienstes für die Kommunikation zwischen dem Exchange-System (SDI) und dem Dienst für die elektronische Rechnungsstellung helfen.

### <a name="create-an-app-registration"></a>Erstellen einer App-Registrierung

1. Verwenden Sie das folgende Windows PowerShell-Skript, um ein selbstsigniertes Zertifikat für die Dienst-zu-Dienst-Authentifizierung (S2S) zu erstellen.

    ```powershell
    $certOutputLocation = "C:\certs\proxytest"
    $certName = "sdiProxyClientS2SCert"
    $certPassword = "123"

    $certCerFile = Join-Path $certOutputLocation "$certName.cer"
    $certPfxFile = Join-Path $certOutputLocation "$certName.pfx"

    $securePassword = ConvertTo-SecureString $certPassword -AsPlainText -Force

    $cert = New-SelfSignedCertificate -KeyLength 2048 -KeyExportPolicy Exportable -FriendlyName "CN=$certName" -CertStoreLocation Cert:\CurrentUser\My -Subject $certName -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider"

    Export-Certificate -Cert $cert -FilePath $certCerFile -type CERT | Out-Null
    Export-PfxCertificate -Cert $cert -FilePath $certPfxFile -Password $securePassword | Out-Null
    ```

2. Speichern Sie die .pfx-Zertifikatsdatei im Schlüsseltresor, und löschen Sie dann die lokale Kopie.
3. Melden Sie sich im [Azure-Portal](https://portal.azure.com) als Administrator an.
4. Erstellen Sie eine App-Registrierung für den SDI-Proxy-Dienst.

    1. Gehen Sie zu **App-Registrierungen**, erstellen Sie eine Registrierung und legen Sie dann die folgenden Werte dafür fest:

        - **Name:** SDI-Proxy-Client
        - **Unterstützte Kontotypen:** Nur Konten in diesem Organisationsverzeichnis (Einzelner Mandant)

    2. Wählen Sie **Registrieren**, und wählen Sie dann die soeben erstellte App-Registrierung aus.
    3. Gehen Sie zu **API-Berechtigungen**, und wählen Sie **Administratoreinwilligung gewähren**.
    4. Gehen Sie zu **Zertifikate & Geheimnisse**, wählen **Zertifikat hochladen**, und laden Sie die .cer-Zertifikatsdatei für die S2S-Authentifizierung hoch.
    5. Gehen Sie zu **Geschäftliche Anwendungen**, und wählen Sie die erstellte App aus.
    6. Speichern Sie die **Anwendungs-ID** (Client-ID) und **Objekt Identifikation** Werte für die App.
    7. Das Team des Rechnungsservice muss der App Zugriff auf den Service gewähren. Senden Sie die Werte der folgenden Parameter an <D365EInvoiceSupport@microsoft.com>:

        - AAD-Mandantenkennung
        - LCS-Umgebungs-ID
        - Anwendungs-ID
        - Objektkennung

5. IN RCS fügen Sie die App der Liste der Anwendung für Ihre Service-Umgebung hinzu.

    1. Gehen Sie zu **Globalisierungsfunktionen** \> **Umgebungen** \> **Elektronische Rechnungsstellung** \> **Serviceumgebungen**, und wählen Sie Ihre Umgebung aus.
    2. Im **Anwendungen** Abschnitt, fügen Sie dem Raster eine Zeile hinzu und geben Sie den Namen und die Objekt-ID der App ein.

        ![Hinzufügen der Anwendung zur Serviceumgebung.](media/e-invoicing-ita-fatturapa-get-started-add-app-to-env.png)

    3. Wählen Sie **Speichern** und dann **Veröffentlichen** aus.

### <a name="create-an-azure-virtual-machine"></a>Erstellen Sie einen virtuellen Azure-Computer

1. Gehen Sie im [Azure-Portal](https://portal.azure.com) zu **Virtuelle Maschinen** und wählen Sie dann **Jetzt erstellen** aus.
2. Auf der Registerkarte **Grundlagen** wählen Sie Ihr Abonnement und Ihre Ressourcengruppe aus. Die Werte sollten das Abonnement und die Ressourcengruppe sein, in der sich Ihr Schlüsseltresor und Ihr Blobspeicher befinden.
3. Wählen Sie die Region aus. Dieser Wert sollte die Region sein, in der Ihre Finanzumgebung bereitgestellt wird.
4. Fügen Sie den Benutzernamen und das Kennwort des Administrators hinzu und speichern Sie sie im Schlüsseltresor.
5. Im Feld **Wählen Sie eingehende Ports aus** wählen Sie **HTTPS (443)** und **RPD (3389)**.

    > [!NOTE]
    > Wir empfehlen Ihnen, den **EPLR (3389)** Port zu deaktivieren, wenn das System in Produktion geht. Sie können es wieder aktivieren, wenn Sie zu Fehlerbehebungszwecken eine Verbindung mit der virtuellen Maschine (VM) herstellen müssen.

    ![Festlegen der Felder auf der Registerkarte Grundlagen zum Erstellen einer Azure-VM.](media/e-invoicing-ita-fatturapa-get-started-create-vm-1.png)

6. Auf der **Datenträger** Registerkarte, auf dem Inforegister **Erweitert** wählen Sie im Inforegister das **Verwaltete Datenträger verwenden** Kontrollkästchen. Lassen Sie das **Kurzlelbiger Betriebssystemdatenträger** Kontrollkästchen deaktiviert.

    ![Festlegen der Felder auf der Registerkarte Datenträger zum Erstellen einer Azure-VM.](media/e-invoicing-ita-fatturapa-get-started-create-vm-2.png)

7. Auf der **Netzwerk** Registerkarte im Feld **Öffentliche IP-Adresse** wählen Sie **Neu erstellen**.

    ![Festlegen der Felder auf der Netzwerk-Registerkarte zum Erstellen einer Azure-VM.](media/e-invoicing-ita-fatturapa-get-started-create-vm-3.png)

8. Im Dialogfeld **öffentliche IP-Adresse erstellen** in der Feldgruppe **SKU** wählen Sie die Option **Standard** aus. In der Feldgruppe **Zuweisung** wählen Sie die Option **statisch** aus.

    ![Erstellen einer öffentlichen IP-Adresse.](media/e-invoicing-ita-fatturapa-get-started-create-vm-4.png)

9. Auf der **Verwaltung** Registerkarte, löschen Sie das Kontrollkästchen **Automatische Abschaltung**, um das automatische Herunterfahren zu deaktivieren.
10. Stellen Sie das Feld **Gast-BS-Updates** auf **Manuell**, und legen Sie dann alle anderen Richtlinien fest.
11. Wählen Sie Überprüfen und VM erstellen.
12. Gehen Sie in der neuen VM zu **Identität** \> **System zugewiesen**, und legen Sie die **Status** Option auf **Ein** fest.
13. Gewähren Sie der VM Zugriff auf den Schlüsseltresor.

    1. Gehen Sie im Schlüsseltresor zu **Zugangskontrolle (IAM)** \> **Rollenzuweisungen**.
    2. Wählen Sie **Rollenzuweisung hinzufügen** und dann legen Sie die folgenden Felder fest:

        1. Im Feld **Rolle** spezifizieren Sie **Schlüsseltresor-Benutzer**.
        2. Im Feld **Zugriff zuweisen zu** spezifizieren Sie **Virtueller Computer**.
        3. Im **Abonnement** Feld geben Sie Ihr Abonnement ein.
        4. Im **Auswahl** Feld geben Sie Ihre VM ein.

    3. Wechseln Sie zu **Zugriffsrichtlinien**.
    4. Wählen Sie **Zugriffsrichtlinie hinzufügen** und legen Sie dann die folgenden Felder fest:

        1. In dem **Prinzipal auswählen** Feld wählen Sie Ihren VM aus.
        2. Legen Sie im Abschnitt **Zertifikat** die Berechtigungen **Liste** und **Abrufen** fest.

14. Im [Azure-Portal](https://portal.azure.com) gehen Sie zu **Öffentliche IP-Adressen** und wählen Sie die IP-Adresse aus, die in der VM erstellt wurde.
15. Gehen Sie zu **Konfiguration** und legen Sie den Domänennamensystem (DNS) fest.

### <a name="prepare-the-proxy-service-environment"></a>Bereiten Sie die Proxy-Dienstumgebung vor

Führen Sie diese Schritte auf dem Computer aus, auf dem der Proxy-Dienst gehostet wird.

1. Stellen Sie über die Remotedesktopverbindung eine Verbindung mit der VM her.
2. Öffnen Sie das Snap-In Zertifikat des lokalen Computers. Weitere Informationen finden Sie unter [Gewusst wie: Anzeigen von Zertifikaten mit dem MMC-Snap-In](/dotnet/framework/wcf/feature-details/how-to-view-certificates-with-the-mmc-snap-in).
3. Importieren Sie das **caentrate.cer** Zertifikat für die Produktion und **CAEntratetest.cer** zum Testen im [Vertrauenswürdige Stammzertifizierungsstellen-Store](/dotnet/framework/wcf/feature-details/working-with-certificates#certificate-stores). (**CAEntratetest.cer** ist das Root-CA-Zertifikat, das von der Behörde bereitgestellt wurde.)
4. Öffnen Sie in der Systemsteuerung **Schalten Sie die Windows Funktionen ein oder aus** oder gehen Sie zu **Server Administrator** \> **Rollen und Funktionen hinzufügen** für das Serverbetriebssystem (OS) und aktivieren Sie die Funktionen der Internetinformationsdienste (IIS):

    - Web-Management-Tools
        - IIS-Verwaltungskonsole
    - World Wide Web-Dienste
        - Anwendungsentwicklungsfunktionen
            - .NET-Erweiterbarkeit 4.7 (oder 4.8)
            - ASP
            - ASP.NET 4.7 (oder 4.8)
            - CGI
            - ISAPI-Erweiterungen
            - ISAPI-Filter
        - Allgemeine HTTP-Funktionen
            - Standarddokument
            - Verzeichnis durchsuchen
            - HTTP-Fehler
            - Statischer Inhalt
        - Integrität und Diagnose
            - HTTP-Protokollierung
            - Verfolgung
        - Leistungs-Funktionen
            - Komprimierung statischer Inhalte
        - Sicherheit
            - Anfragefilterung

    ![Aktivieren der IIS-Funktionen.](media/e-invoicing-ita-fatturapa-get-started-turnon-features.png)

### <a name="set-up-the-sdi-proxy-service-in-iis"></a>Einrichten des SDI-Proxy-Dienstes in IIS

1. In Microsoft Dynamics Lifecycle Services (LCS) gehen Sie zu den freigegebenen Anlage und wählen Sie **Datenpakete** als Anlagentyp aus.
2. Suchen sie **Elektronischer Rechnungsservice Sdi Proxy**, und laden Sie es auf die VM herunter.
3. Konfigurieren des Service.

    1. Entpacken Sie den **Elektronischer Rechnungsservice Sdi Proxy** Archivordner, den Sie heruntergeladen haben.
    2. Im **src\\FattureService** Ordner, öffnen Sie die **appsettings.json** Datei und legen Sie die folgenden Parameter fest:

        - **KeyVaultUri** – Geben Sie die Adresse des Schlüsseltresors an, in dem das Clientzertifikat für den Rechnungsservice gespeichert ist.
        - **TenantId** – Geben Sie den Global Unique Identifier (GUID) des Mandanten des Kunden an.
        - **EnvironmentId** – Geben Sie die ID der LCS-Umgebung an.
        - **ClientID** – Geben Sie die App-ID der App-Registrierung für Zwischendienste im Mandanten des Kunden an.
        - **ClientCertificateName** – Geben Sie den Namen des S2S-Zertifikats im Schlüsseltresor an.
        - **SecurityServiceClientOptions.Endpoint** – Geben Sie die URL des Sicherheitsdienstes an.
        - **SecurityServiceClientOptions.Resource** – Geben Sie den Bereich an, für den das Token abgerufen werden soll.
        - **InvoicingServiceClientOptions.Endpoint** – Geben Sie den Endpunkt des Rechnungsservices an. Dieser Wert sollte derselbe Endpunkt sein, der für RCS und Finance verwendet wird.
        - **InvoicingServiceClientOptions.ServiceEnvironmentId** – Geben Sie den Namen der Serviceumgebung an. Dieser Wert sollte der Name Ihrer Finanzumgebung sein.
        - **NotificationsFolder** – Geben Sie den Ordner an, in dem eingehende Benachrichtigungsdateien gespeichert werden sollen.

    3. In der **Web.config** Datei, suchen Sie die folgende Zeile und fügen Sie den Fingerabdruck des Proxyserverzertifikats hinzu.

        `<serviceCertificate findValue="[certificate thumbprint]" storeLocation="LocalMachine" storeName="My" x509FindType="FindByThumbprint">`

        > [!TIP]
        > Wenn das System in Produktion geht, können Sie einige Werte in der Datei Web.config ändern, um die Menge der gesammelten Protokollinformationen zu reduzieren und Speicherplatz zu sparen. Im **\<system.diagnostics\>\<source\>** Knoten, ändern Sie den Wert von **switchValue** zu **Kritischer Fehler**. Weitere Informationen finden Sie unter [MS Serviceüberwachungsviewer](/dotnet/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe).

4. Öffnen Sie den IIS-Manager. Bleiben Sie im Baum links im Stammknoten. Wählen Sie rechts **Serverzertifikate**.

    ![Auswählen von Dienstzertifikaten im IIS-Manager.](media/e-invoicing-ita-fatturapa-get-started-proxy-cert-1.png)

5. Öffnen Sie das Menü und wählen Sie **Importieren**.
6. Im **Zertifikat importieren** Dialogfeld, im Feld **Zertifikatsdatei (.pfx)** geben Sie den Pfad der .pfx-Datei für das Proxyserverzertifikat an.

    ![Angeben der Zertifikatsdatei des Proxy-Dienstes.](media/e-invoicing-ita-fatturapa-get-started-proxy-cert-2.png)

7. Wählen und halten Sie die Datei (oder klicken Sie mit der rechten Maustaste) **Site** und wählen Sie dann **Website hinzufügen** aus.
8. Geben Sie im Dialogfeld **Website erstellen** im Feld **Site-Name** einen Namen für die Site ein.
9. Im Feld **Physischer Pfad** Feld, zeigen Sie auf den Ordner **src\\FattureService**.
10. Wählen Sie im Feld **Bindungstyp** den Eintrag **https** aus.
11. Geben Sie im Feld **Hostnae** den Hostnamen ein.
12. Lassen Sie die Felder **IP Adresse** und **Port** auf den Standardwerten.
13. Stellen Sie sicher, dass das Kontrollkästchen **Servernamenangabe erforderlich** deaktiviert ist, da SDI diese Technologie nicht unterstützt.
14. Im Feld **SSL-Zertifikat** wählen Sie das importierte Proxyserverzertifikat aus.
15. Im **Anwendungspool** Feld, geben Sie einen Pool für die Site an und notieren Sie sich den Namen (z.B. **SdiAppPool**).

    ![Hinzufügen einer Website.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-1.png)

16. Nachdem Sie die Website erstellt haben, öffnen Sie das Menü für **SSL-Einstellungen**.

    ![Öffnen des Menüs für SSL-Einstellungen.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-2.png)

17. Wählen Sie das **SSL erforderlich** Kontrollkästchen und dann **Client-Zertifikate** in der Feldgruppe und wählen Sie die Option **Erforderlich**.

    ![SSL-Einstellungen konfigurieren.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-3.png)

18. Öffnen Sie **Verzeichnis durchsuchen**, und wählen Sie **Aktivieren**.
19. Gehen Sie in einem beliebigen Webbrowser zu **serverDNS/TrasmissioneFatture.svc**. Es muss eine Standardseite über den Dienst erscheinen.

    ![Überprüfen des Dienstes in einem Browser.](media/e-invoicing-ita-fatturapa-get-started-proxy-open-browser.png)

20. Erstellen Sie die folgenden Ordner zum Speichern von Protokollen und Dateien:

    - **C:\\Protokolle\\** – Protokolldateien hier speichern. Diese Dateien können vom [MS Service Trace Viewer](/dotnet/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe) eingesehen werden.
    - **C:\\Dateien\\** – Speichern Sie hier alle Antwortdateien.

21. Gewähren Sie im Datei-Explorer **NETZWERKDIENST** und **IIS AppPool\\SdiAppPool** (oder **IIS AppPool\\DefaultAppPool** wenn Sie den Standardpool verwenden) Zugriff auf die Ordner **Protokolle** und **Dateien**.

    1. Wählen und halten Sie den Ordner (oder klicken Sie mit der rechten Maustaste) und wählen Sie dann **Eigenschaften**.
    2. Im **Eigenschaften** Dialogfeld, auf der Registerkarte **Sicherheit** wählen Sie **Bearbeiten** aus.
    3. Fügen Sie die Benutzer hinzu, wenn sie nicht aufgeführt sind.
    4. Wiederholen Sie die Schritte 1 bis 3 für alle anderen Ordner.

    ![Hinzufügen von Berechtigungen zum Dienstbenutzer.](media/e-invoicing-ita-fatturapa-get-started-proxy-add-user.png)

## <a name="privacy-notice"></a>Datenschutzhinweis 

Das Aktivieren der **Italienische elektronische Rechnung** Funktion erfordert möglicherweise, dass begrenzte Daten gesendet werden. Zu diesen Daten gehört die Steueridentifikationsnummer der Organisation. Ein Administrator kann die italienische elektronische Rechnungsfunktion aktivieren und deaktivieren. Um eine Funktion zu deaktivieren, führen Sie folgende Schritte aus.

1. Navigieren Sie zu **Organisationsverwaltung** \> **Einrichtung** \> **Parameter elektronischer Dokumente**.
2. Auf der **Funktionen** Registerkarte, wählen Sie die Zeilen aus, die die Funktion **Italienische elektronische Rechnung** enthalten und wählen Sie dann das Kontrollkästchen **Jetzt deaktivieren** aus.

Daten, die aus diesen externen Systemen in diesen Dynamics 365-Onlinedienst importiert werden, unterliegen unseren [Datenschutzbestimmungen](https://go.microsoft.com/fwlink/?LinkId=512132). Weitere Informationen finden Sie in den Abschnitten zum Datenschutz in der landes-und regionenspezifischen Funktionsdokumentation.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Informationen zur elektronischen Rechnungsstellung](e-invoicing-service-overview.md)
- [Erste Schritte mit der Dienstverwaltung für die elektronische Rechnungsstellung](e-invoicing-get-started-service-administration.md)
- [Erste Schritte mit der elektronischen Rechnungsstellung](e-invoicing-get-started.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
