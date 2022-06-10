---
title: Signieren Sie die MPOS .appx-Datei mit einem Code Signing Zertifikat
description: In diesem Thema wird erläutert, wie MPOS mit einem Codesignaturzertifikat signiert wird.
author: mugunthanm
ms.date: 05/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: 28021
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-09-2019
ms.openlocfilehash: 38c094de6f94381a809fdb68d2e76d410e406934
ms.sourcegitcommit: 336a0ad772fb55d52b4dcf2fafaa853632373820
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2022
ms.locfileid: "8811084"
---
# <a name="sign-the-mpos-appx-file-with-a-code-signing-certificate"></a>Signieren Sie die MPOS .appx-Datei mit einem Code Signing Zertifikat

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Um Modern POS (MPOS) zu installieren, müssen Sie die MPOS-App mit einem Codesignaturzertifikat eines vertrauenswürdigen Anbieters signieren und dasselbe Zertifikat auf allen Computern installieren, auf denen MPOS im vertrauenswürdigen Stammordner für den aktuellen Benutzer installiert ist.

Um die MPOS-App mit einem Zertifikat zu signieren, verwenden Sie eine dieser Optionen in der Datei **Retail SDK\\Build tool\\Customization.settings**:

- Fügen Sie den Aufgabenteil „Sichere Datei“ der Azure DevOps-Build-Schritte hinzu und laden Sie das Zertifikat hoch, um die Dateiaufgabe zu sichern. Verwenden Sie die Ausgabenpfadvariable für Aufgabe „Sichere Datei“ als Parameter in der Customization.settings-Datei.

    > [!NOTE]
    > Die Aufgabe „Sichere Datei“ unterstützt kein kennwortgeschütztes Zertifikat. Sie müssen das Kennwort entfernen, bevor Sie diese Aufgabe hochladen. Da das Zertifikat in Azure in die Aufgabe für sichere Dateisysteme hochgeladen wird, können Sie das Kennwort nur für diesen Schritt entfernen. Sie sollten das Entfernen des Kennworts jedoch mit Ihren Sicherheitsexperten besprechen, um festzustellen, ob dies die richtige Maßnahme für Ihr Projekt ist. Entfernen Sie das Zertifikatkennwort nicht für andere Szenarien.
- Verwenden Sie ein Zertifikat, das sich im Dateisystem befindet. Laden Sie dazu ein Zertifikat herunter oder generieren Sie es und platzieren Sie es im Dateisystem, in dem der Build ausgeführt wird. Der von Microsoft gehostete Agent oder Build-Benutzer sollte Zugriff auf diesen Pfad und diese Datei haben.
- Verwenden Sie den Fingerabdruck, um im Zertifikat im Store nachzuschlagen und sich mit diesem Zertifikat anzumelden.

## <a name="use-a-secure-file-task-for-universal-windows-platform-app-signing"></a>Verwenden einer Aufgabe „Sichere Datei“ für die Universal Windows Platform-App-Signatur

> [!NOTE]
> Sie können auch Azure Key Vault verwenden, um das Zertifikat zu speichern, und das Azure-Signaturtool verwenden, um die Modern POS-APPX-Datei und Self-Service-Installationsprogramme zu signieren. Beispiele für Pipelineskripte und zusätzliche Informationen finden Sie unter [Build-Pipeline in Azure DevOps einrichten, um Self-Service-Pakete für den Einzelhandel zu generieren](build-pipeline.md#set-up-a-build-pipeline-in-azure-devops-to-generate-retail-self-service-packages).

Die Verwendung einer Aufgabe „Sichere Datei“ ist der empfohlene Ansatz für das Signieren von Universal Windows Platform(UWP)-Apps. Weitere Informationen zum Signieren von Paketen finden Sie unter [Paketsignierung konfigurieren](/windows/uwp/packaging/auto-build-package-uwp-apps#configure-package-signing). Dieser Prozess wird im folgenden Bild dargestellt.

![MPOS-App-Signatur-Flow.](media/POSSigningFlow.png)

> [!NOTE]
> Derzeit unterstützt das OOB-Packaging nur das Signieren der .appx-Datei, die verschiedenen Self-Service-Installer wie MPOIS, RSSU und HWS werden von diesem Prozess nicht signiert. Sie müssen es manuell mit SignTool oder anderen Signiertools signieren. Das zum Signieren der .appx-Datei verwendete Zertifikat muss auf dem Rechner installiert sein, auf dem Modern POS installiert ist.

## <a name="steps-to-configure-the-certificate-for-signing-in-azure-pipelines"></a>Schritte zum Konfigurieren des Zertifikats für die Anmeldung in Azure Pipelines

### <a name="certificate-in-the-file-systemsecure-location"></a>Zertifikat im Dateisystem/sicherer Speicherort

Laden Sie die [DownloadFile-Aufgabe](/visualstudio/msbuild/downloadfile-task) herunter und fügen Sie sie als ersten Schritt im Build-Prozess hinzu. Der Vorteil der Verwendung der Aufgabe „Sichere Datei“ besteht darin, dass die Datei verschlüsselt und während des Builds auf dem Datenträger platziert wird, unabhängig davon, ob die Buildpipeline erfolgreich ist, fehlschlägt oder abgebrochen wird. Die Datei wird nach Abschluss des Build-Vorgangs aus dem Download-Speicherort gelöscht.

1. Laden Sie die Aufgabe „Sichere Datei“ herunter und fügen Sie sie als ersten Schritt in der Azure-Buildpipeline hinzu. Sie können die Aufgabe „Sichere Datei“ aus [DownloadFile](https://marketplace.visualstudio.com/items?itemName=automagically.DownloadFile) herunterladen.
1. Laden Sie das Zertifikat in die Aufgabe „Sichere Datei“ hoch und legen Sie den Referenznamen unter „Ausgabevariablen“ fest, wie auf dem folgenden Bild gezeigt.
    > [!div class="mx-imgBorder"]
    > ![Aufgabe „Sichere Datei“](media/SecureFile.png)
1. Erstellen Sie eine neue Variable in Azure Pipelines, indem Sie **Neue Variable** auf der Registerkarte **Variablen** auswählen.
1. Geben Sie im Wertefeld einen Namen für die Variable an, z. B. **MySigningCert**.
1. Speichern Sie die Variable.
1. Öffnen Sie die Datei **Customization.settings** aus **RetailSDK\\BuildTools** und aktualisieren Sie **ModernPOSPackageCertificateKeyFile** mit dem in der Pipeline erstellten Variablennamen (Schritt 3). Beispiel:

    ```Xml
    <ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(MySigningCert)</ModernPOSPackageCertificateKeyFile>
    ```
    Dieser Schritt ist erforderlich, wenn das Zertifikat nicht kennwortgeschützt ist. Wenn das Zertifikat kennwortgeschützt ist, fahren Sie mit den folgenden Schritten fort.
    
1. Wenn Sie die MPOS .appx-Datei beim Signieren mit einem Zertifikat mit einem Zeitstempel versehen möchten, öffnen Sie die Datei **Retail SDK \\Build Tool \\Customization.settings** und aktualisieren Sie die Variable **ModernPOSPackageCertificateTimestamp** mit dem Zeitstempelanbieter (z.B. `http://timestamp.digicert.com`).
1. Fügen Sie auf der Registerkarte **Variablen** der Pipeline eine neue Variable für sicheren Text hinzu. Stellen Sie den Namen auf **MySigningCert.secret** ein und legen Sie den Wert des Kennworts für das Zertifikat fest. Wählen Sie das Schlosssymbol aus, um die Variable zu sichern.
1. Fügen Sie der Pipeline eine **Powershell-Skript**-Aufgabe Task hinzu (nach dem Herunterladen der sicheren Datei und vor dem Build-Schritt). Stellen Sie den **Anzeige**-Namen bereit und legen Sie den Typ als **Inline** fest. Kopieren Sie Folgendes und fügen Sie es in den Skriptabschnitt ein.

    ```powershell
    Write-Host "Start adding the PFX file to the certificate store."
    $pfxpath = '$(MySigningCert.secureFilePath)'
    $secureString = ConvertTo-SecureString "$(MySigningCert.secret)" -AsPlainText -Force
    Import-PfxCertificate -FilePath $pfxpath -CertStoreLocation Cert:\CurrentUser\My -Password $secureString
    ```

1. Öffnen Sie die Datei **Customization.settings** aus **RetailSDK\\BuildTools** und aktualisieren Sie **ModernPOSPackageCertificateThumbprint** mit dem Wert des Zertifikatfingerabdrucks.

    ```Xml
       <ModernPOSPackageCertificateThumbprint Condition="'$(ModernPOSPackageCertificateThumbprint)' == ''"></ModernPOSPackageCertificateThumbprint>
    ```
 
Einzelheiten zum Abrufen des Fingerabdrucks für ein Zertifikat finden Sie unter [Zertifikatfingerabdruck abrufen](/dotnet/framework/wcf/feature-details/how-to-retrieve-the-thumbprint-of-a-certificate#to-retrieve-a-certificates-thumbprint). 

## <a name="download-or-generate-a-certificate-to-sign-the-mpos-app-manually-using-msbuild-in-sdk"></a>Zertifikat herunterladen oder generieren, um die MPOS-App manuell mit msbuild im SDK zu signieren

Wenn ein heruntergeladenes oder generiertes Zertifikat verwendet wird, um die MPOS-App zu signieren, dann führt das Aktualisieren des Knotens **ModernPOSPackageCertificateKeyFile** in der Datei **BuildTools\\Customization.settings** dazu, das auf den Speicherort der PFX-Datei (**$(SdkReferencesPath)\\appxsignkey.pfx**) verwiesen wird. Beispiel:

```xml
<ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(SdkReferencesPath)\appxsignkey.pfx</ModernPOSPackageCertificateKeyFile>
```

In diesem Fall lautet der Dateiname des Zertifikats **appxsignkey.pfx**, und dieses liegt im Ordner **Retail SDK\\Referenz**.

## <a name="use-thumbprint-to-sign-the-mpos-app"></a>Fingerabdruck für das Signieren der MPOS-App verwenden

Wenn Sie den Fingerabdruck zum Signieren der MPOS-App verwenden, installieren Sie das Zertifikat lokal. Aktualisieren Sie den Fingerabdruckwert im Knoten **ModernPOSPackageCertificateThumbprint** in der Datei **BuildTools\\Customization.settings**.

Diese Option funktioniert, wenn der Build-Benutzer ein lokaler Benutzer ist. Wenn Sie jedoch die Azure DevOps-Agenten verwenden, um den Build zu generieren, dann hat der Agent möglicherweise keine Berechtigung, auf den Zertifikatspeicher zuzugreifen, um das Zertifikat zum Signieren zu verwenden, oder auf dem Build-Computer ist das Zertifikat nicht installiert. In diesem Fall kann das Problem umgangen werden, indem der Build-Benutzer in einen lokalen Benutzer geändert und das Zertifikat im Feld installiert wird. Diese Option funktioniert jedoch nicht, wenn Sie keinen Administratorzugriff auf das Feld haben.

> [!NOTE]
> Wenn die .pfx-Datei oder die Aufgabenoption „Sichere Datei“ zum Signieren der App verwendet wird, lassen Sie den Knoten **ModernPOSPackageCertificateThumbprint** in **Customization.settings** leer. Wenn die Fingerabdruckoption verwendet wird, lassen Sie **ModernPOSPackageCertificateKeyFile** leer. Wenn beide Werte aktualisiert werden, schlägt der Build fehl.

### <a name="certification-renewal"></a>Erneuerung der Zertifizierung

### <a name="renew-a-certificate-from-trusted-ca"></a>Zertifikat von einer vertrauenswürdigen Zertifizierungsstelle erneuern

Wenden Sie sich für den Zertifikatserneuerungsprozess an Ihre Zertifizierungsstelle. Für ein vertrauenswürdiges Zertifikat ist auf der MPOS-Seite keine Aktion erforderlich.

### <a name="renew-a-self-signed-certificate"></a>Selbstsigniertes Zertifikat erneuern

Verwenden Sie das im Retail SDK verfügbare Beispielzertifikat nicht für die Produktion. Es kann nur zu Entwicklungszwecken verwendet werden. Das Contoso-Beispielzertifikat kann nicht erneuert werden und das in der Retail SDK-Version 10.0.16 oder früher enthaltene Beispielzertifikat ist am 31. Dezember 2020 abgelaufen. Wenn dieses Zertifikat oder ein selbst signiertes Zertifikat zum Signieren eines benutzerdefinierten Modern POS verwendet wurde, besteht eine hohe Wahrscheinlichkeit, dass Modern POS nach diesem Datum nicht mehr ordnungsgemäß funktioniert.
 
### <a name="impact"></a>Auswirkung
 
Wenn das oben Gesagte auf Sie zutrifft, werden Sie auf das Problem stoßen, dass das Installationsprogramm nach dem 31. Dezember 2020 nicht mehr ausgeführt werden kann. Je nach verwendeten IT-Unternehmensrichtlinien kann Modern POS möglicherweise nicht funktionieren. Es ist wichtig, dass Sie dies testen, indem Sie das Datum vorübergehend auf ein zukünftiges Datum ändern, um die Auswirkungen auf Ihre Organisation zu ermitteln.
 
### <a name="steps-to-determine-the-issue"></a>Schritte zur Bestimmung des Problems
 
1.  Verwenden Sie die Windows-Einstellungen, um die Computeruhr auf ein Datum und eine Uhrzeit im Jahr 2021 umzustellen.
2.  Stellen Sie sicher, dass Modern POS geöffnet werden kann, Sie sich anmelden können und eine Transaktion abgeschlossen werden kann.
3.  Stellen Sie sicher, dass das Modern POS-Self-Service-Installationsprogramm ausgeführt werden kann. Wenn dies der Fall ist, wird die Installation erfolgreich abgeschlossen.
4.  Setzen Sie die Windows-Uhreinstellungen auf das richtige Datum und die richtige Uhrzeit zurück.
 
Wenn Sie alle diese Schritte ohne Probleme abschließen können, können Sie mit dem aktuellen Zertifikat nach dem 31. Dezember 2020 arbeiten.  
 
### <a name="steps-going-forward"></a>Weitere Schritte 

Es wird dringend empfohlen, das zuvor verwendete Zertifikat zu erneuern. Wir empfehlen Ihnen dringend, sich ein neues Zertifikat zu besorgen. Dazu können Sie auf dieser Seite eine der folgenden Aktivitäten durchführen:
 
- **Bevorzugt** – Fordern Sie ein Codesignaturzertifikat von einer vertrauenswürdigen Zertifizierungsstelle an.

- **Nicht bevorzugt** – Generieren Sie ein selbstsigniertes Codesignaturzertifikat, das Sie verwenden können. Dies wird normalerweise nur für Entwicklungszwecke innerhalb einer Domäne verwendet und wird nicht für die Produktion empfohlen. 

- **Als temporäre Lösung erhältlich** – Verwenden Sie das erneuerte Codesignaturzertifikat von Contoso. Dies wird normalerweise zu Testzwecken verwendet, daher wird es nicht empfohlen, es in der Produktion bereitzustellen.
 
Generieren Sie als Nächstes ein neues benutzerdefiniertes Modern POS-Paket, das mit diesem Zertifikat signiert ist, und das Sie aus einer der oben genannten Aktionen erhalten haben. Je nach Zertifikat muss eine der folgenden Aktionen ausgeführt werden:
 
- Wenn Sie ein neues, vertrauenswürdiges Zertifikat (oder ein neues, selbstsigniertes Zertifikat) verwenden, müssen Sie auf jedem Gerät ein neues Zertifikat installieren. Danach müssen Sie das neu erstellte Modern POS-Paket (Installationsprogramm) verwenden, die vorhandene Anwendung deinstallieren und dann das neue Modern POS-Paket neu installieren. Sie müssen auf jedem Gerät eine Geräteaktivierung von Modern POS durchführen.

- Wenn Sie das erneuerte Contoso-Zertifikat verwenden, müssen Sie das neue Zertifikat auf jedem Gerät installieren und das Modern POS-Paket (Installationsprogramm) installieren. Eine Deinstallation ist nicht erforderlich, Sie müssen jedoch eine Neuinstallation auf dem Gerät durchführen. Beachten Sie, dass eine Geräteaktivierung von Modern POS nicht erforderlich ist. Diese Option ist eine vorübergehende Lösung. Verwenden Sie diese Option nur, um eine erneute Aktivierung zu vermeiden und das Problem zu beheben, bevor Sie ein neues vertrauenswürdiges Zertifikat erhalten.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
