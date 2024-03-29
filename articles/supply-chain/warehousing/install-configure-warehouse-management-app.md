---
title: Mobile Warehouse Management-App installieren und verbinden
description: In diesem Artikel wird erläutert, wie Sie die mobile Lagerortverwaltungs-App auf jedem Ihrer mobilen Geräte installieren und für die Verbindung mit Ihrer Microsoft Dynamics 365 Supply Chain Management-Umgebung konfigurieren.
author: Mirzaab
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2021-02-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 1333881f80c735794784831d4042bfe7d070b796
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838471"
---
# <a name="install-and-connect-the-warehouse-management-mobile-app"></a>Mobile Warehouse Management-App installieren und verbinden

[!include [banner](../includes/banner.md)]

In diesem Artikel wird erklärt, wie Sie die Warehouse Management mobile App herunterladen und auf jedem Ihrer mobilen Geräte installieren und wie Sie die App für die Verbindung mit Ihrer Supply Chain Management Umgebung konfigurieren. Sie können jedes Gerät manuell konfigurieren oder Verbindungseinstellungen über eine Datei oder durch Scannen eines QR-Codes importieren.

## <a name="system-requirements"></a>Systemanforderungen

Die Lagerortverwaltungs-App ist für Windows- und Google Android-Betriebssysteme verfügbar. Um diese App zu verwenden, muss eines der folgenden Betriebssysteme auf Ihren mobilen Geräten installiert sein:

- Windows 10 (Universal Windows Platform \[UWP\]) Oktober 2018 Update 1809 (Build 10.0.17763) oder höher
- Android 4.4 oder höher

## <a name="turn-warehouse-management-mobile-app-features-on-or-off-in-supply-chain-management"></a>Schalten Sie die Funktionen der Warehouse Management Mobile App in Supply Chain Management ein oder aus

Um die mobile Warehouse Management App zu verwenden, muss die Funktion *Benutzereinstellungen, Symbole und Schritttitel für die neue Lagerort-App* für Ihr System aktiviert sein. Ab Supply Chain Management 10.0.25 ist diese Funktion obligatorisch und kann nicht deaktiviert werden. Wenn Sie eine ältere Version als 10.0.25 ausführen, können Administratoren diese Funktionalität ein- oder ausschalten, indem sie nach der Funktion *Benutzereinstellungen, Symbole und Schritttitel für die neue Lagerort-App* im Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) suchen.

## <a name="get-the-warehouse-management-mobile-app"></a>Die mobile Lagerortverwaltungs-App erhalten

Bei kleineren Bereitstellungen können Sie die App typischerweise auf jedem Gerät aus dem entsprechenden Store installieren und dann die Verbindung zu den von Ihnen verwendeten Umgebungen manuell konfigurieren.

Bei größeren Bereitstellungen können Sie das Bereitstellen und/oder die Konfiguration von Apps automatisieren, was bequemer sein kann, wenn Sie viele Geräte verwalten. Sie könnten z.B. eine Lösung für die Verwaltung von mobilen Geräten und mobilen Anwendungen wie [Microsoft Intune](/mem/intune/fundamentals/what-is-intune) verwenden. Weitere Informationen dazu, wie Sie Intune zum Hinzufügen von Anwendungen verwenden, finden Sie unter [Microsoft Intune Apps hinzufügen](/mem/intune/apps/apps-add).

### <a name="install-the-app-from-an-app-store"></a>Installieren Sie die App aus einem App-Store

Der einfachste Weg, die App auf einem einzelnen Gerät zu installieren, ist die Installation aus einem App-Store, der immer die neueste allgemein verfügbare Version bereitstellt. Microsoft Intune kann auch Apps aus den App-Stores holen. Verwenden Sie einen der folgenden Links, um die App aus einem App-Store zu installieren:

- **Windows (UWP):** [Lagerortverwaltung im Microsoft Store](https://www.microsoft.com/store/apps/9pd35cdqcmg3)

- **Android:** [Lagerortverwaltung im Google Play Store](https://play.google.com/store/apps/details?id=com.Microsoft.WarehouseManagement)

### <a name="download-the-app-from-microsoft-app-center"></a>Laden Sie die App aus dem Microsoft App Center herunter

Als Alternative zur Installation aus einem App-Store können Sie die App stattdessen auch aus dem Microsoft App Center herunterladen. Das App Center stellt installierbare Pakete zur Verfügung, die Sie per Sideload laden können. Zusätzlich zur aktuellen Version können Sie im App Center auch frühere Versionen herunterladen und eventuell Vorschauversionen mit neuen Funktionen, die Sie ausprobieren können. Um aktuelle, frühere oder Vorschau-Versionen der mobilen App „Lagerortverwaltung“ aus dem Microsoft App Center herunterzuladen, verwenden Sie einen der folgenden Links:

- **Windows (UWP):** [Warehouse Management (Windows)](https://aka.ms/wma-windows-official-release)  
    Anweisungen zur Installation eines heruntergeladenen Pakets auf einem Windows-Gerät und zum anschließenden Festlegen der erforderlichen Zertifikate finden Sie unter [Installieren eines Builds aus dem App Center](/appcenter/distribution/installation).

- **Android:** [Lagerortverwaltung (Android)](https://aka.ms/wma-android-official-release)  
    Wenn Sie eine Vorschau-Version herunterladen, sind ein paar zusätzliche Schritte erforderlich, um sie zu installieren. Einzelheiten finden Sie unter [Testen von Android-Apps](/appcenter/distribution/testers/testing-android).

Informationen über die Installation eines aus dem App Center heruntergeladenen Builds finden Sie unter [Installieren eines Builds](/appcenter/distribution/installation).

## <a name="create-a-web-service-application-in-azure-active-directory"></a><a name="create-service"></a>Webdienstanwendung in Azure Active Directory erstellen

Sie müssen eine Webdienstanwendung für den Supply Chain Management-Mandanten in Azure Active Directory (Azure AD) registrieren, damit die mobile Lagerortverwaltungs-App mit einem bestimmten Supply Chain Management-Server interagieren kann. Das folgende Verfahren veranschaulicht eine Möglichkeit, diese Aufgabe auszuführen. Detaillierte Informationen und Alternativen finden Sie unter den Links nach dem Verfahren.

1. Navigieren Sie in einem Webbrowser zu [https://portal.azure.com](https://portal.azure.com/).
1. Geben Sie den Namen und das Kennwort des Benutzers ein, der Zugriff auf das Azure-Abonnement hat.
1. Wählen Sie im linken Navigationsbereich des Azure-Portals **Azure Active Directory** aus.

    ![Azure Active Directory.](media/app-connect-azure-aad.png "Azure Active Directory")

1. Stellen Sie sicher, dass Sie mit der Azure AD-Instanz arbeiten, die von Supply Chain Management verwendet wird.
1. Wählen Sie in der Liste **Verwalten** die Option **App-Registrierungen** aus.

    ![App-Registrierungen.](media/app-connect-azure-register.png "App-Registrierungen")

1. Wählen Sie auf der Symbolleiste **Neue Registrierung** aus, um den Assistenten **Anwendung registrieren** zu öffnen.
1. Geben Sie einen Namen für die Anwendung ein, wählen Sie die Option **Nur Konten in diesem organisatorischen Verzeichnis** und dann **Registrieren** aus.

    ![Anwendungsassistenten registrieren.](media/app-connect-azure-register-wizard.png "Anwendungsassistenten registrieren")

1. Die neue App-Registrierung wird geöffnet. Notieren Sie sich den Wert der **Anwendungs(Client)-ID**, da Sie ihn zu einem späteren Zeitpunkt benötigen. Dies ID wird später in diesem Artikel als *Client-ID* bezeichnet.

    ![Anwendungs-ID (Client).](media/app-connect-azure-app-id.png "Anwendungs-ID (Client)")

1. Wählen Sie in der Liste **Verwalten** **Zertifikat und geheime Schlüssel** aus. Wählen Sie dann eine der folgenden Schaltflächen aus, je nachdem, wie Sie die App für die Authentifizierung konfigurieren möchten. (Weitere Informationen finden Sie im Abschnitt [Mit einem Zertifikat oder geheimen Clientschlüssel authentifizieren](#authenticate) weiter unten in diesem Artikel.)

    - **Zertifikat hochladen** – Laden Sie ein Zertifikat hoch, um es als geheimen Schlüssel zu verwenden. Wir empfehlen diese Methode, da sie sicherer ist und außerdem vollständig automatisiert werden kann. Wenn Sie die mobile Lagerortverwaltungs-App auf Windows-Geräten ausführen, notieren Sie sich den **Fingerabdruck**-Wert, der nach dem Hochladen des Zertifikats angezeigt wird. Sie benötigen diesen Wert, wenn Sie das Zertifikat auf Windows-Geräten konfigurieren.
    - **Neuer geheimer Clientschlüssel** – Erstellen Sie einen Schlüssel, indem Sie eine Schlüsselbeschreibung und eine Dauer im Abschnitt **Passwörter** eingeben, und wählen Sie dann **Hinzufügen** aus. Erstellen Sie eine Kopie des Schlüssels, und bewahren Sie ihn sicher auf.

    ![Zertifikat und geheime Schlüssel.](media/app-connect-azure-authentication.png "Zertifikat und geheime Schlüssel")

Weitere Informationen zum Einrichten von Webdienstanwendungen in Azure AD finden Sie in den folgenden Ressourcen:

- Anweisungen zum Einrichten von Webdienstanwendungen mit Windows PowerShell in Azure AD finden Sie unter [Vorgehensweise: Azure PowerShell zum Erstellen eines Dienstprinzipals mit einem Zertifikat verwenden](/azure/active-directory/develop/howto-authenticate-service-principal-powershell).
- Ausführliche Informationen zum manuellen Erstellen einer Webdienstanwendung in Azure AD finden Sie in den folgenden Artikeln:

    - [Schnellstart: Eine Anwendung bei der Microsoft Identity Platform registrieren](/azure/active-directory/develop/quickstart-register-app)
    - [Vorgehensweise: Das Portal verwenden, um eine Azure AD-Anwendung- und einen -Dienstprinzipal zu erstellen, die auf Ressourcen zugreifen können](/azure/active-directory/develop/howto-create-service-principal-portal)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a><a name="user-azure-ad"></a>Erstellen und Konfigurieren eines Benutzerkontos in Supply Chain Management

Führen Sie die folgenden Schritte aus, um Supply Chain Management die Verwendung Ihrer Azure AD-Anwendung zu ermöglichen.

1. Erstellen Sie einen Benutzer, der den Benutzeranmeldeinformationen für die mobile Lagerortverwaltungs-App entspricht:

    1. Wechseln Sie in Supply Chain Management zu **Systemverwaltung \> Benutzer \> Benutzer**.
    1. Erstellen Sie einen Benutzer.
    1. Weisen Sie den Benutzer die Benutzerrolle *Mobiles Geräts für Lagerhaltung zu*.

    ![Weisen Sie den Benutzer des mobilen Geräts für Lagerhaltung zu.](media/app-connect-app-users.png "Den Benutzer des mobilen Geräts für Lagerhaltung zuweisen")

1. Ordnen Sie Ihre Azure AD-Anwendung dem Benutzer der mobilen Lagerortverwaltungs-App zu:

    1. Gehen Sie zu **Systemadministration \> Einrichtung \> Azure Active Directory-Anwendungen**.
    1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zu erstellen.
    1. Geben Sie im Feld **Client-ID** die Client-ID ein, den Sie sich im vorherigen Abschnitt notiert haben.
    1. Geben Sie im Feld **Name** einen Namen ein.
    1. Wählen Sie im Feld **Benutzer-ID** die Benutzer-ID aus, dass Sie gerade erstellt haben.

    ![Azure Active Directory-Anwendungen.](media/app-connect-aad-apps.png "Azure Active Directory-Anwendungen")

> [!TIP]
> Eine Möglichkeit, diese Einstellungen zu verwenden, besteht darin, für jedes Ihrer physischen Geräte eine Client-ID in Azure zu erstellen und dann jede Client-ID zur **Azure Active Directory-Anwendungen**-Seite hinzuzufügen. Wenn ein Gerät dann verloren gehen, können Sie seinen Zugriff auf Supply Chain Management einfach eentfernen, indem Sie dessen Client-ID von dieser Seite entfernen. (Dieser Ansatz funktioniert, weil die auf jedem Gerät gespeicherten Verbindungsanmeldeinformationen auch eine Client-ID angeben, wie weiter unten in diesem Artikel beschrieben.)
>
> Darüber hinaus werden die Standardeinstellungen für Sprache, Zahlenformat und Zeitzone für jede Client-ID durch die Einstellungen festgelegt, die für den **Benutzer-ID**-Wert, der hier zugeordnet ist, festgelegt wird. Daher können Sie diese Einstellungen verwenden, um basierend auf der Client-ID Standardeinstellungen für jedes Gerät oder jede Gerätesammlung festzulegen. Diese Standardeinstellungen werden jedoch überschrieben, wenn sie auch für das *Benutzerkonto der Lager-App*, die ein Mitarbeiter verwendet, um sich auf dem Gerät anzumelden, definiert sind. (Weitere Informationen finden Sie unter [Benutzerkonten für mobile Geräte](mobile-device-work-users.md).)

## <a name="authenticate-by-using-a-certificate-or-client-secret"></a><a name="authenticate"></a>Sich mit einem Zertifikat oder einem geheimen Clientschlüssel authentifizieren

Die Authentifizierung mit Azure AD bietet eine sichere Möglichkeit, ein mobiles Gerät mit Supply Chain Management zu verbinden. Sie können sich mit einem Zertifikat oder einem geheimen Clientschlüssel authentifizieren. Wenn Sie Verbindungseinstellungen importieren, empfiehlt es sich, anstelle eines geheimen Clientschlüssels ein Zertifikat zu verwenden. Da der geheime Clientschlüssel immer sicher gespeichert werden muss, können Sie ihn nicht aus einer Verbindungseinstellungsdatei oder einem QR-Code importieren, wie später in diesem Artikel beschrieben.

Zertifikate können als geheime Schlüssel verwendet werden, um die Identität der Anwendung zu belegen, wenn ein Token angefordert wird. Der öffentliche Teil des Zertifikats wird in die App-Registrierung im Azure-Portal hochgeladen, während das vollständige Zertifikat auf jedem Gerät bereitgestellt werden muss, auf dem die mobile Lagerortverwaltungs-App installiert ist. Ihre Organisation ist für die Verwaltung des Zertifikats in Bezug auf Rotation usw. verantwortlich. Sie können selbstsignierte Zertifikate verwenden, Sie sollten jedoch stets nicht exportierbare Zertifikate verwenden.

Sie müssen das Zertifikat lokal auf jedem Gerät verfügbar machen, auf dem Sie die mobile Lagerortverwaltungs-App ausführen. Weitere Informationen dazu, wie Sie bei Verwendung von Intune, Intune-gesteuerte Geräte verwalten, finden Sie unter [Zertifikate zur Authentifizierung in Microsoft Intune verwenden](/mem/intune/protect/certificates-configure).

## <a name="configure-the-warehouse-management-mobile-app-for-cloud-and-edge-scale-units"></a>Konfigurieren Sie die Warehouse Management Mobile-App für Scale-Units in der Cloud und am Rand

Es sind einige zusätzliche Schritte erforderlich, wenn Sie die Warehouse Management Mobile-App gegen eine Scale-Unit in der Cloud oder am Edge ausführen möchten. Anweisungen finden Sie unter [Konfigurieren Sie die Warehouse Management Mobile-App für Scale-Units in der Cloud und im Edge](../cloud-edge/cloud-edge-workload-setup-warehouse-app.md).

## <a name="configure-the-application-by-importing-connection-settings"></a>Die Anwendung durch Importieren der Verbindungseinstellungen konfigurieren

Sie können die Verbindungseinstellungen importieren, anstatt sie manuell auf jedem Gerät einzugeben, um die Wartung und Bereitstellung der Anwendung auf vielen mobilen Geräten zu vereinfachen. In diesem Abschnitt wird erläutert, wie Sie die Einstellungen erstellen und importieren.

### <a name="create-a-connection-settings-file-or-qr-code"></a>Eine Verbindungseinstellungsdatei oder einen QR-Code erstellen

Sie können Verbindungseinstellungen aus einer Datei oder einem QR-Code importieren. Für beide Methoden müssen Sie zuerst eine Einstellungsdatei erstellen, die das JSON-Format (JavaScript Object Notation) und die -Syntax verwendet. Die Datei muss eine Verbindungsliste mit den einzelnen Verbindungen enthalten, die hinzugefügt werden müssen. In der folgenden Tabelle sind die Parameter zusammengefasst, die Sie in der Verbindungseinstellungsdatei angeben müssen.

| Parameter | Beschreibung |
|---|---|
| ConnectionName | Geben Sie den Namen der Verbindungseinstellung an. Der Text kann maximal 20 Zeichen umfassen. Da dieser Wert die eindeutige Kennung für eine Verbindungseinstellung ist, müssen Sie sicherstellen, dass er in der Liste eindeutig ist. Wenn auf dem Gerät bereits eine Verbindung mit demselben Namen vorhanden ist, wird diese durch die Einstellungen aus der importierten Datei überschrieben. |
| ActiveDirectoryClientAppId | Geben Sie die Client-ID an, die Sie sich beim Einrichten von Azure AD im Abschnitt [Webdienstanwendung in Azure Active Directory erstellen](#create-service) notiert haben. |
| ActiveDirectoryResource | Geben Sie die Stamm-URL von Supply Chain Management an. |
| ActiveDirectoryTenant | Geben Sie den Azure AD-Domänennamen an, den Sie mit dem Supply Chain Management-Server verwenden. Dieser Wert hat die Form `https://login.windows.net/<your-Azure-AD-domain-name>`. Hier ist ein Beispiel: `https://login.windows.net/contosooperations.onmicrosoft.com`. Weitere Informationen darüber, wie Sie Ihren Azure AD-Domänennamen finden, finden Sie unter [Wichtige IDs für einen Benutzer lokalisieren](/partner-center/find-ids-and-domain-names). |
| Firma | Geben Sie die juristische Person in Supply Chain Management an, mit der die Anwendung eine Verbindung herstellen soll. |
| ConnectionType | (Optional) Geben Sie an, ob für die Verbindungseinstellung ein Zertifikat oder ein geheimer Clientschlüssel verwendet werden soll, um eine Verbindung mit einer Umgebung herzustellen. Gültige Werte sind *"certificate"* und *"clientsecret"*. Der Standardwert ist *"certificate"*.<p>**Hinweis:** Geheime Clientschlüssel können nicht importiert werden.</p> |
| IsEditable | (Optional) Geben Sie an, ob die Bearbeitung der Verbindungseinstellung für den Benutzer möglich sein soll. Gültige Werte sind *"Wahr"* und *"Falsch"*. Der Standardwert ist *"Wahr"*. |
| IsDefault | (Optional) Geben Sie an, ob es sich bei der Verbindung um die Standardverbindung handelt. Eine Verbindung, die als Standardverbindung festgelegt ist, wird beim Öffnen der App automatisch vorausgewählt. Es kann nur eine Verbindung als Standardverbindung festgelegt werden. Gültige Werte sind *"Wahr"* und *"Falsch"*. Der Standardwert ist *"Falsch"*. |
| CertificateThumbprint | (Optional) Bei Windows-Geräten können Sie den Zertifikatfingerabdruck für die Verbindung angeben. Bei Android-Geräten muss der App-Benutzer das Zertifikat auswählen, wenn eine Verbindung zum ersten Mal verwendet wird. |

Das folgende Beispiel zeigt eine gültige Verbindungseinstellungsdatei, die zwei Verbindungen enthält. Wie Sie sehen, ist die Verbindungsliste (mit dem Namen *"ConnectionList"* in der Datei) ein Objekt mit einem Array, in dem jede Verbindung als Objekt gespeichert ist. Jedes Objekt muss in geschweifte Klammern ({}) eingeschlossen und durch Kommas getrennt und das Array muss in Klammern (\[\]) eingeschlossen werden.

```json
{
    "ConnectionList": [
        {
            "ActiveDirectoryClientAppId":"aaaaaaaa-bbbb-ccccc-dddd-eeeeeeeeeeee",
            "ConnectionName": "Connection1",
            "ActiveDirectoryResource": "https://yourenvironment.cloudax.dynamics.com",
            "ActiveDirectoryTenant": "https://login.windows.net/contosooperations.onmicrosoft.com",
            "Company": "USMF",
            "IsEditable": false,
            "IsDefaultConnection": true,
            "CertificateThumbprint": "aaaabbbbcccccdddddeeeeefffffggggghhhhiiiii",
            "ConnectionType": "certificate"
        },
        {
            "ActiveDirectoryClientAppId":"aaaaaaaa-bbbb-ccccc-dddd-eeeeeeeeeeee",
            "ConnectionName": "Connection2",
            "ActiveDirectoryResource": "https://yourenvironment2.cloudax.dynamics.com",
            "ActiveDirectoryTenant": "https://login.windows.net/contosooperations.onmicrosoft.com",
            "Company": "USMF",
            "IsEditable": true,
            "IsDefaultConnection": false,
            "ConnectionType": "clientsecret"
        }
    ]
}
```

Sie können die Informationen entweder als JSON-Datei speichern oder einen QR-Code mit demselben Inhalt generieren. Wenn Sie die Informationen als Datei speichern, empfehlen wir, sie unter dem Standardnamen zu speichern. *connections.json*. Dies gilt insbesondere dann, wenn Sie es auf jedem mobilen Gerät am Standardspeicherort speichern.

### <a name="save-the-connection-settings-file-on-each-device"></a>Verbindungseinstellungsdatei auf jedem Gerät speichern

In der Regel verwenden Sie ein Geräteverwaltungstool oder -skript, um die Verbindungseinstellungsdateien auf jedes von Ihnen verwaltete Gerät zu verteilen. Wenn Sie beim Speichern der Verbindungseinstellungsdatei auf jedem Gerät den Standardnamen und den Standardspeicherort verwenden, wird diese von der mobilen Lagerortverwaltungs-App automatisch importiert, auch während der ersten Ausführung nach der Installation der App. Wenn Sie einen benutzerdefinierten Namen oder Speicherort für die Datei verwenden, muss der App-Benutzer die Werte bei der ersten Ausführung angeben. Die App verwendet jedoch auch danach weiterhin den angegebenen Namen und Speicherort.

Bei jedem Start der App werden die Verbindungseinstellungen aus ihrem vorherigen Speicherort erneut importiert, um zu ermitteln, ob Änderungen vorgenommen wurden. Die App aktualisiert nur Verbindungen, deren Namen mit denen der Verbindungen in der Verbindungseinstellungsdatei identisch sind. Vom Benutzer erstellte Verbindungen, die andere Namen verwenden, werden nicht aktualisiert.

Sie können eine Verbindung nicht mithilfe der Verbindungseinstellungsdatei entfernen.

Wie bereits erwähnt, lautet der Standarddateiname *connections.json*. Der Standardspeicherort für Dateien hängt davon ab, ob Sie ein Windows- oder ein Android-Gerät verwenden:

- **Windows:** `C:\Users\<User>\AppData\Local\Packages\Microsoft.WarehouseManagement_8wekyb3d8bbwe\LocalState`
- **Android:** `Android\data\com.Microsoft.WarehouseManagement\files`

Normalerweise werden die Pfade nach dem ersten Ausführen der App automatisch erstellt. Sie können sie jedoch manuell erstellen, wenn Sie die Verbindungseinstellungsdatei vor der Installation auf das Gerät übertragen müssen.

> [!NOTE]
> Wenn die App deinstalliert wird, werden der Standardpfad und sein Inhalt entfernt.

### <a name="import-the-connection-settings"></a>Verbindungseinstellungen importieren

Führen Sie die folgenden Schritte aus, um die Verbindungseinstellungen aus einer Datei oder einem QR-Code zu importieren.

1. Starten Sie die mobile Lagerortverwaltungs-App auf Ihrem mobilen Gerät. Beim ersten Start der App wird eine Willkommensnachricht angezeigt. Wählen Sie **Eine Verbindung auswählen**.

    ![Begrüßungsnachricht.](media/app-configure-welcome-screen.png "Begrüßungsnachricht")

1. Wenn Sie die Verbindungseinstellungen aus einer Datei importieren und beim Speichern der Datei der Standardname und der Standardspeicherort verwendet wurden, hat die App die Datei möglicherweise bereits gefunden. Fahren Sie in diesem Fall mit Schritt 4 fort. Andernfalls wählen Sie **Verbindung einrichten** aus, und fahren Sie dann mit Schritt 3 fort.

    ![Verbindung einrichten.](media/app-configure-set-up-connection.png "Verbindung einrichten")

1. In dem Dialogfeld **Verbindungsaufbau** wählen Sie **Aus Datei hinzufügen** oder **Aus QR-Code hinzufügen** aus, je nachdem, wie Sie die Einstellungen importieren möchten:

    - Wenn Sie die Verbindungseinstellungen aus einer Datei importieren, wählen Sie **Aus Datei hinzufügen**, navigieren Sie zu der Datei auf Ihrem lokalen Gerät, und wählen Sie sie aus. Wenn Sie einen benutzerdefinierten Speicherort auswählen, speichert die App diesen und verwendet ihn beim nächsten Mal automatisch.
    - Wenn Sie die Verbindungseinstellungen durch Scannen eines QR-Codes importieren, wählen Sie **Aus QR-Code hinzufügen** aus. Die App fordert Sie auf, die Verwendung der Kamera des Geräts zu erlauben. Nachdem Sie die Erlaubnis erteilt haben, wird die Kamera gestartet, damit Sie sie zum Scannen verwenden können. Je nach Qualität der Kamera des Geräts und Komplexität des QR-Codes kann es schwierig sein, einen korrekten Scan zu erhalten. Versuchen Sie in diesem Fall, die Komplexität des QR-Codes zu verringern, indem Sie nur eine Verbindung pro QR-Code generieren. (Derzeit können Sie nur die Kamera des Geräts zum Scannen des QR-Codes verwenden.)

    ![Verbindungsaufbau-Menü.](media/app-configure-connection-setup-flyout.png "Verbindungsaufbau-Menü")

1. Wenn die Verbindungseinstellungen erfolgreich geladen wurden, wird die ausgewählte Verbindung angezeigt.

    ![Verbindungseinstellungen wurden geladen.](media/app-configure-select-connection.png "Verbindungseinstellungen wurden geladen")

1. Wenn Sie ein Android-Gerät und ein Zertifikat zur Authentifizierung verwenden, fordert das Gerät Sie auf, das Zertifikat auszuwählen.

    ![Eingabeaufforderung zum Auswählen eines Zertifikats auf einem Android-Gerät.](media/app-configure-select-certificate.png "Eingabeaufforderung zum Auswählen eines Zertifikats auf einem Android-Gerät")

1. Die App stellt eine Verbindung zu Ihrem Supply Chain Management-Server her und zeigt die Anmeldeseite an.

    ![Anmeldeseite.](media/app-configure-sign-in-page.png "Anmeldeseite")

## <a name="manually-configure-the-application"></a><a name="config-manually"></a>Anwendung manuell konfigurieren

Wenn Sie keine Datei oder keinen QR-Code haben, können Sie die App manuell auf dem Gerät konfigurieren, sodass sie eine Verbindung mit dem Supply Chain Management-Server über die Azure AD-Anwendung herstellt.

1. Starten Sie die mobile Lagerortverwaltungs-App auf Ihrem mobilen Gerät.
1. Wenn die App im **Demomodus** gestartet wird, wählen Sie **Verbindungseinstellungen** aus. Wenn die Seite **Anmelden** angezeigt wird, wenn die App gestartet wird, wählen Sie **Verbindung ändern**.
1. Wählen Sie **Verbindung einrichten**.

    ![Verbindung einrichten.](media/app-configure-set-up-connection.png "Verbindung einrichten")

1. Wählen Sie **Manuell eingeben**.

    ![Verbindungsaufbau-Menü.](media/app-configure-connection-setup-flyout.png "Verbindungsaufbau-Menü")

    Die Seite **Neue Verbindung** wird angezeigt und zeigt die Einstellungen, die zur manuellen Eingabe der Verbindungsdetails erforderlich sind.

    ![Manuelle Verbindungsfelder.](media/app-configure-input-manually.png "Manuelle Verbindungsfelder")

1. Geben Sie die folgenden Informationen ein:

    - **Geheimen Clientschlüssel verwenden** – Legen Sie die Option auf _Ja_ fest, um einen geheimen Clientschlüssel für die Authentifizierung mit Supply Chain Management zu verwenden. Legen Sie sie auf _Nein_ fest, um ein Zertifikat für die Authentifizierung zu verwenden. (Weitere Informationen finden Sie im Abschnitt [Erstellen einer Webdienstanwendung in Azure Active Directory](#create-service) weiter oben in diesem Artikel.)
    - **Verbindungsname** – Geben Sie einen Namen für die neue Verbindung ein. Dieser Name wird beim nächsten Öffnen der Verbindungseinstellungen im Feld **Verbindung auswählen** angezeigt. Der eingegebene Name muss eindeutig sein. (Das bedeutet, dass er sich von allen anderen auf Ihrem Gerät gespeicherten Verbindungsnamen unterscheiden muss, wenn dort andere Verbindungsnamen gespeichert sind.)
    - **Active Directory-Client-ID** – Geben Sie die Client-ID ein, die Sie sich beim Einrichten von Azure AD im Abschnitt [Webdienstanwendung in Azure Active Directory erstellen](#create-service) notiert haben.
    - **Geheimer Active Directory-Clientschlüssel** – Dieses Feld ist nur verfügbar, wenn die Option **Geheimen Clientschlüssel verwenden** auf _Ja_ gesetzt ist. Geben Sie den geheimen Clientschlüssel ein, den Sie sich beim Einrichten von Azure AD im Abschnitt [Webdienstanwendung in Azure Active Directory erstellen](#create-service) notiert haben.
    - **Active Directory-Zertifikatfingerabdruck** – Dieses Feld ist nur dann für Windows-Geräte verfügbar, wenn die Option **Geheimen Clientschlüssel verwenden** auf _Nein_ gesetzt ist. Geben Sie den Zertifikatfingerabdruck ein, den Sie sich beim Einrichten von Azure AD im Abschnitt [Webdienstanwendung in Azure Active Directory erstellen](#create-service) notiert haben.
    - **Active Directory-Ressource** – Geben Sie die Stamm-URL von Supply Chain Management an.

        > [!IMPORTANT]
        > Beenden Sie diesen Wert nicht mit einem Schrägstrich (/).
        > Stellen Sie sicher, dass das HTTPS (SSL)-Zertifikat gültig ist.

    - **Mandant des aktiven Verzeichnisses** - Geben Sie den Azure AD-Domänennamen ein, den Sie mit dem Supply Chain Management-Server verwenden. Dieser Wert hat die Form `https://login.windows.net/<your-Azure-AD-domain-name>`. Hier ist ein Beispiel: `https://login.windows.net/contosooperations.onmicrosoft.com`. Weitere Informationen darüber, wie Sie Ihren Azure AD-Domänennamen finden, finden Sie unter [Wichtige IDs für einen Benutzer lokalisieren](/partner-center/find-ids-and-domain-names).

        > [!IMPORTANT]
        > Beenden Sie diesen Wert nicht mit einem Schrägstrich (/).

    - **Unternehmen** – Geben Sie die juristische Person (Unternehmen) in Supply Chain Management ein, mit der Sie die Anwendung verbinden möchten.

1. Wählen Sie in der rechten oberen Ecke der Seite die Schltfläche **Speichern** aus.
1. Wenn Sie ein Android-Gerät und ein Zertifikat zur Authentifizierung verwenden, fordert das Gerät Sie auf, das Zertifikat auszuwählen.
1. Die App stellt eine Verbindung zu Ihrem Supply Chain Management-Server her und zeigt die Anmeldeseite an.

## <a name="remove-access-for-a-device"></a>Aufheben des Zugriffs für ein Gerät

Im Fall von verlorenen oder beeinträchtigten Geräten müssen Sie den Zugriff des Geräts auf Supply Chain Management entfernen. Anhand der folgenden Schritten wird beschrieben, wie der Zugriff entfernt wird.

1. Gehen Sie zu **Systemadministration \> Einrichtung \> Azure Active Directory-Anwendungen**.
1. Löschen Sie die Position, die dem Gerät entspricht, dessen Zugriff Sie entfernen möchten. Notieren Sie sich die Client-ID, die für das Gerät verwendet wird, da Sie diese später benötigen.

    Wenn Sie nur eine Client-ID registriert haben und mehrere Geräte dieselbe Client-ID verwenden, müssen Sie neue Verbindungseinstellungen für diese Geräte vornehmen. Andernfalls verlieren Sie den Zugriff.

1. Melden Sie sich beim Azure-Portal unter [https://portal.azure.com](https://portal.azure.com/) an.
1. Wählen Sie im linken Navigationsbereich **Active Directory**, und stellen Sie sicher, dass Sie sich im richtigen Verzeichnis befinden.
1. Wählen Sie in der Liste **Verwalten** die Option **App-Registrierungen** und anschließend die Anwendung aus, die Sie konfigurieren möchten. Die Seite **Einstellungen** wird mit den entsprechenden Konfigurationsinformationen angezeigt.
1. Stellen Sie sicher, dass die Client-ID der Anwendung mit der Client-ID übereinstimmt, die Sie sich in Schritt 2 notiert haben.
1. Wählen Sie auf der Symbolleiste **Löschen** aus.
1. Wählen Sie in der angezeigten Bestätigungsmeldung **Ja** aus.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Benutzereinstellungen für mobile Geräte](mobile-device-user-settings.md)
- [Weisen Sie der mobilen Warehouse Management-App Schrittsymbole und -titel zu](step-icons-titles.md)
- [Konfigurieren Sie die Warehouse Management Mobile-App für Scale-Units in der Cloud und im Edge-Bereich](../cloud-edge/cloud-edge-workload-setup-warehouse-app.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
