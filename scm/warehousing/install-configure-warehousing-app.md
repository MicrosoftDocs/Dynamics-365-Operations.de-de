---
title: Installieren und Konfigurieren von Microsoft Dynamics 365 for Operations &#8211; Warehousing
description: In diesem Thema wird beschrieben, wie Microsoft Dynamics 365 for Operations - Warehousing eingerichtet und konfiguriert wird.
author: YuyuScheller
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 231c087ddc976aa552fc9cd6c89188f82a0247d1
ms.lasthandoff: 03/31/2017


---

# <a name="install-and-configure-microsoft-dynamics-365-for-operations-8211-warehousing"></a>Installieren und Konfigurieren von Microsoft Dynamics 365 for Operations &#8211; Warehousing

In diesem Thema wird beschrieben, wie Microsoft Dynamics 365 for Operations - Warehousing eingerichtet und konfiguriert wird.

Dynamics 365 for Operations - Warehousing ist eine Anwendung, die auf Play Google Store und Windows Store verfügbar ist. Für die aktuelle Version von Microsoft Dynamics 365 for Operations wird die App als eigenständige Komponente bereitgestellt, die auf den Geräten selbst bereitgestellt wird. Um die App in Ihrem Dynamics 365 for Operations Umgebung zu verwenden, müssen Sie auf jedem die App auf jedes Gerät herunterladen und konfiguriert und mit Dynamics 365 for Operations verbinden. In diesem Thema wird beschrieben, wie App auf Ihren Geräten eingerichtet wird. Es werden auch gezeigt, wie der App konfiguriert wird, um sie mit Dynamics 365 for Operations zu verbinden.

## <a name="prerequisites"></a>Voraussetzungen
Die App ist auf Android und Windows-Betriebssystemen verfügbar. Um diese App zu verwenden, müssen Sie eines der folgenden unterstützten Betriebssysteme haben, die auf Ihren Geräten eingerichtet werden. Sie müssen eine der unterstützten folgenden Versionen von Microsoft Dynamics 365 for Operations verfügen. Verwenden Sie die Informationen in der folgenden Tabelle, um zu prüfen, ob die Hardware und Software-Umgebung bereit ist die Installation zu unterstützen.

| Plattform                    | Version                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| Windows (UWP)               | Windows 10 (alle Vesionen)                                                                                                                                                   |
| Dynamics 365 for Operations | Microsoft Dynamics 365 for Operations 1611 oder Microsoft Dynamics Dynamics AX Version 7.0/7.1 und Microsoft Dynamics AX-Plattformaktualisierung 2 mit 3210014 KB Hotfix. |

## <a name="get-the-app"></a>Abrufen der App
-   Windows (UWP) - [Dynamics 365 for Operations - Warehousing über den Windows Store](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android - [Dynamics 365 for Operations - Warehousing über den Google Play Store](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

## <a name="create-a-web-service-application-in-active-directory"></a>Erstellen einer Webdienstanwendung in Active Directory
Um der App die Möglichkeit mit bestimmten Dynamics 365 for Operations-Servern zu interagieren zu ermöglichen, müssen Sie eine Webdienstanwendung in Azure Active Directory für den Dynamics 365 for Operations-Mandanten erfassen. Aus Sicherheitsgründen wird empfohlen, dass Sie eine Webdienstanwendung für jedes Gerät erstellt werden, das Sie verwenden. Um eine Webdienstanwendung in Azure Active Directory (Azure AD) zu erstellen, führen Sie die folgenden Schritte aus:

1.  In einem Webbrowser wechseln Sie zu <https://manage.windowsazure.com>.
2.  Geben Sie den Namen und das Kennwort des Benutzers ein, der Zugriff auf Azure Abonnement hat.
3.  Im Azure Portal im linken Navigationsbereich, klicken Sie **Active Directory**[](./media/wh-01-active-directory-example.png)[![wh-01-active-directory-example](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)
4.  Im Raster wählen die Active Directory-Instanz aus, die von Dynamics 365 for Operations verwendet wird.
5.  Klicken Sie im oben Aktivitätsbereich auf **Anwendungen**. [![wh-02-active-directory-applications](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)
6.  Klicken Sie im unteren Bereich auf **Hinzufügen**. Der **Anwendung hinzufügen**-Assistent startet.
7.  Geben Sie einen Namen für die Anwendung ein und wählen Sie aus **Webanwendung und/oder Internet API**. [![wh-03-active-directory-add-application](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)
8.  Geben Sie die Anmelde-URL ein, die die Anwendungs-URL in Ihrem Mandanten Stamm Arbeitsgänge ist die (Stamm-URL). Die Anmelde-URL ist derzeit nicht aktiv genutzt in der App authentifiziert, ist jedoch ein Pflichtfeld. Geben die URL im Feld "App ID URI" ein. [![wh-04-ad-add-properties](./media/wh-04-ad-add-properties.png)](./media/wh-04-ad-add-properties.png)
9.  Wechseln Sie zur Registerkarte **Konfigureren**. [![wh-05-ad-configure-app](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)
10. Navigieren Sie nach unten, bis der **Berechtigungen anderen Bewerbungen** Abschnitt finden. Klicken Sie auf **Anwendung hinzufügen**. [![wh-06-ad-app-add-permissions](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)
11. Wählen Sie **Microsoft Dynamics ERP** in der Liste aus. Klicken Sie auf **Check abschließen** in der rechten unter Seitenecke auf diese Seite. [![wh-07-ad-select-permissions](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)
12. Wählen Sie in der Liste **Delegaten-Berechtigungen** Sie alle Kontrollkästchen. Klicken Sie auf **Speichern**. [![wh-08-ad-delegate-permissions](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)
13. Notieren Sie die folgenden Informationen:
    -   **Client-ID** - Beim Hochscrollen finden Sie die **Client-ID** angezeigt.
    -   **Schlüssel** - Im **Schlüssel** Abschnitt, erstellen einen Schlüssel, indem sie die Dauer auswählen, und kopieren den Schlüssel. Dieser Schlüssel dient später als **Clientgeheimnis**.

## <a name="create-and-configure-a-user-account-in-dynamics-365-for-operations"></a>Erstellen und Konfigurieren Sie ein Benutzerkonto in Dynamics 365 for Operations
Um Dynamics 365 for Operations zu aktivieren für Ihre Azure AD-Anwendung, müssen folgende Konfigurationsschritte abgeschlossen werden:

1.  Erstellen eines neuen Benutzerkontos in Azure Active Directory für die Dynamics 365 for Operations-Mandant. Der Zweck dieses Benutzerkontos ist, auf bestimmte benutzerdefinierte Dienste der Warehousing-App zuzugreifen, die Dynamics 365 for Operations verfügbar macht. Nachdem Sie diesen Schritt abgeschlossen wurde, besitzen Sie WMDP-Benutzeranmeldeinformationen, die einer WMDP-E-Mail-Adresse und einem WMDP-Kennwort bestehen. Um die grundlegenden Schritte zum Hinzufügen von Benutzern zur Azure AD und von Microsoft Dynamics 365 for Operations zu ermitteln, lesen Sie dieses Lernprogramm [Anmelden für ein Microsoft Dynamics 365 for Operations Abonnement](/dynamics365/operations/dev-itpro/sign-up-preview-subscription).
2.  Erstellen Sie Dynamics 365 for Operations-Benutzer der den Warehousing-App-Benutzeranmeldeinformationen entspricht.
    1.  In Dynamics 365 for Operations wechseln Sie zu **Systemverwaltung** &gt; **Allgemein** &gt; **Benutzer**.
    2.  Erstellen Sie einen neuen Benutzer
    3.  Weisen Sie den Warhouse-Mobilbenutzer zu, wie im folgenden Screenshot angezeigt werden. [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  Ordnen Sie die Azure Active Directory-Anwendung mit dem Warehousing-App-Benutzer zu.
    1.  In Dynamics 365 for Operations wechseln sie zu **Systemverwaltung** &gt; **Einstellungen** &gt; **Azure Active Directory-Anwendung**.
    2.  Erstellen Sie eine neue Position.
    3.  Geben Sie die **Client-ID** ein (wird im vorherigen Abschnitt erhalten), geben Sie dieser Kennung einen Namen, und wählen Sie den zuvor erstellten Benutzer aus. Es wird empfohlen, dass Sie alle Geräte markiert, sodass Sie den Zugriff zu Dynamics 365 for Operations von dieser Seite können leicht entfernen, sofern sie verloren gehen. [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Anwendung konfigurieren
Sie müssen die App im Gerät konfigurieren, um mit dem Dynamics 365 for Operations-Server über die Azure AD-Anwendung zu verbinden. Führen Sie dazu die folgenden Schritte aus.

1.  In der App wechseln Sie zu **Verbindungseinstellungen**.
2.  Deaktivieren Sie das **Demomodus** Feld. [![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Geben Sie die folgenden Informationen ein: **Azure Active Directory-Client-ID** - Die Client-ID wird in Schritt 13 in "Erstellen einer Webdienstbewerbung in Active Directory " erhalten. - **Azure Active Directory-Client-Geheminis** - Das Geheminis wird in Schritt 13 in "Erstellen einer Webdienstbewerbung in Active Directory " erhalten. - **Azure Active Directory-Ressource** - Die Ressource enthält die Dynamics 365 for Operations Stamm-URL. **Hinweis**: Beenden Sie dieses Feld nicht mit einem Schrägstrichzeichen (/). - **Azure Active Directory-Mandant** - Der Azure Active Directory-Mandant wird mit dem Dynamics 365 for Operations Server genutzt https://login.windows.net/&lt;ihre-AD-mandant-ID&gt;. Beispiel: https://login.windows.net/contosooperations.onmicrosoft.com. 
**Hinweis**: Beenden Sie dieses Feld nicht mit einem Schrägstrichzeichen (/). - **Unternehmen** - Geben Sie die juristische Person in Dynamics 365 for Operations ein, auf die die Anwendung herstellen soll. [![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Wählen Sie die **Zurück** Schaltfläche in der linken oberen Ecke der Anwendung aus. Die Anwendung verbindet jetzt an Ihr Dynamics 365 for Operations-Server und anzeigen den Bildschirm Anmeldung. [![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>Aufheben des Zugriffs für ein Gerät
Im Fall von verlorenen oder beeinträchtigten Geräts müssen Sie den Zugriff zu Dynamics 365 for Operations für das Gerät entfernen. In den folgenden Schritten wird den empfohlenen Verarbeiten, um den Zugriff zu entfernen.

1.  In Dynamics 365 for Operations wechseln sie zu **Systemverwaltung** &gt; **Einstellungen** &gt; **Azure Active Directory-Anwendung**.
2.  Löscht die Position, die dem Gerät entspricht, dem Sie Zugriff entfernen möchten. Beachten Sie die **Client-ID** für das entfernte Gerät.
3.  Melden Sie sich das Azure Portal unter <https://manage.windowsazure.com> an.
4.  Klicken Sie auf das Symbol **Active Directory** im linken Menü, und klicken Sie anschließend auf das gewünschte Verzeichnis.
5.  Klicken Sie im Hauptmenü auf **Anwendungen** und anschließend auf die Anwendung, die Sie konfigurieren möchten. Die **Schnellstart** Seite wird angezeigt mit einmaligen Anmelden und weitere Konfigurationsinformationen.
6.  Klicken Sie auf die Registerkarte **konfigurieren**, scrollen sie nach unten und stellen Sie sicher, dass die **Client-ID** der Anwendung das gleiche wie in Schritt 2 dieses Abschnitts ist.
7.  Klicken Sie in der Befehlsleiste auf die Schaltfläche '**Löschen**'.
8.  Klicken Sie in der daraufhin angezeigten Meldung auf **Ja**.



