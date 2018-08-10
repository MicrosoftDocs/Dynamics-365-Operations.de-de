---
title: Installieren und Konfigurieren von Microsoft Dynamics 365 for Finance and Operations &#8211; Lagerung
description: In diesem Thema wird beschrieben, wie Microsoft Dynamics 365 for Finance and Operations - Lagerung eingerichtet und konfiguriert wird.
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 608543c9cfd93c4772e93089e1d174312d8b23a6
ms.openlocfilehash: 411bb28668f5aa9d07774211814da4e9757ac43c
ms.contentlocale: de-de
ms.lasthandoff: 03/06/2018

---

# <a name="install-and-configure-microsoft-dynamics-365-for-finance-and-operations-8211-warehousing"></a>Installieren und Konfigurieren von Microsoft Dynamics 365 for Finance and Operations &#8211; Lagerung

[!include [banner](../includes/banner.md)]

> [!NOTE]
> 
> In diesem Thema wird beschrieben, wie Lagerhaltung für Cloudbereitstellungen konfiguriert wird. Wenn Sie erfahren möchten, wie die Lagerhaltung für lokale Bereitstellungen konfiguriert wird, finden Sie Informationen unter [Lagerhaltung für lokale Bereitstellungen](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md).


In diesem Thema wird beschrieben, wie Microsoft Dynamics 365 for Finance and Operations - Lagerung eingerichtet und konfiguriert wird.

Finance and Operations – Lagerung ist eine Anwendung, die im Google Play Store und Windows Store verfügbar ist. Für die aktuelle Version von Finance and Operations wird die App als eigenständige Komponente bereitgestellt, die auf den Geräten für Lagerortarbeiten selbst bereitgestellt wird. Um die App in Ihrer Finance and Operations-Umgebung zu verwenden, müssen Sie sie auf jedes Gerät herunterladen und konfigurieren und mit Ihrer Finance and Operations-Umgebung verbinden. In diesem Thema wird beschrieben, wie App auf Ihren Geräten eingerichtet wird. Es wird auch gezeigt, wie der App konfiguriert wird, um sie mit Ihrer Finance and Operations-Umgebung zu verbinden.

## <a name="prerequisites"></a>Voraussetzungen
Die App ist auf Android und Windows-Betriebssystemen verfügbar. Um diese App zu verwenden, müssen Sie eines der folgenden unterstützten Betriebssysteme haben, die auf Ihren Geräten eingerichtet werden. Sie müssen eine der unterstützten folgenden Versionen von Finance and Operations haben. Verwenden Sie die Informationen in der folgenden Tabelle, um zu prüfen, ob die Hardware und Software-Umgebung bereit ist die Installation zu unterstützen.

| Plattform                    | Version                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0, 7.0, 8.0                                                                                                                                                     |
| Windows (UWP)               | Windows 10 (alle Vesionen)                                                                                                                                                   |
| Finance and Operations | Microsoft Dynamics 365 for Operations, Version 1611 <br>– oder – <br>Microsoft Dynamics AX Version 7.0/7.0.1 und Microsoft Dynamics AX-Plattform Update 2 mit Hotfix KB 3210014 |

## <a name="get-the-app"></a>Abrufen der App
-   Windows (UWP)
     - [Finance and Operations – Lagerhaltung im Windows Store](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android
    - [Finance and Operations - Lagerung im Google Play Store](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)
    - [Finance and Operations - Lagerung in der Zebra AppGallery](https://appgallery.zebra.com/showcase/apps/146?type=showcase)

## <a name="create-a-web-service-application-in-azure-active-directory"></a>Erstellen einer Webdienstanwendung in Azure Active Directory
Um der App die Möglichkeit mit bestimmten Finance and Operations-Server zu interagieren zu ermöglichen, müssen Sie eine Webdienstanwendung in einem Azure Active Directory für den Finance and Operations-Mandanten erfassen. Aus Sicherheitsgründen wird empfohlen, dass Sie eine Webdienstanwendung für jedes Gerät erstellt werden, das Sie verwenden. Um eine Webdienstanwendung in Azure Active Directory (Azure AD) zu erstellen, führen Sie die folgenden Schritte aus:

1.  In einem Webbrowser gehen Sie zu <https://portal.azure.com>.
2.  Geben Sie den Namen und das Kennwort des Benutzers ein, der Zugriff auf Azure Abonnement hat.
3.  Im Azure Portal im linken Navigationsbereich, klicken Sie auf **Azure Active Directory**.[](./media/WMA-01-active-directory-example.png)[![WMA-01-active-directory-example](./media/WMA-01-active-directory-example.png )](./media/WMA-01-active-directory-example.png)
4.  Stellen Sie sicher, dass die Active Directory-Instanz diejenige ist, die von Finance and Operations verwendet wird.
5.  Klicken Sie in der Liste auf **App-Registrierungen**. [![WMA-02-active-directory-app-registrations](./media/WMA-02-active-directory-app-registrations.png)](./media/WMA-02-active-directory-app-registrations.png)
6.  Klicken Sie im oberen Bereich auf **Registrierung von neuer Anwendung**. Der **Anwendung hinzufügen**-Assistent startet.
7.  Geben Sie einen Namen für die Anwendung ein und wählen Sie **Webanwendung/Web-API** aus. Geben Sie die Anmelde-URL ein, die Ihre Web-App-URL ist. Diese URL ist die gleiche wie die Bereitstellungs-URL, außer dass oauth hinzugefügt ist. Klicken Sie auf **Erstellen**. [![WMA-03-active-directory-add-application](./media/WMA-03-active-directory-add-application.png)](./media/WMA-03-active-directory-add-application.png)
8.  Wählen Sie die neue App in der Liste aus. [![WMA-04-active-directory-configure-app](./media/WMA-04-active-directory-configure-app.png)](./media/WMA-04-active-directory-configure-app.png)
9.  Merken Sie sich die **Anwendungskennung**, Sie werden sie später benötigen. Die **Anwendungskennung** wird später als die **Client-ID** bezeichnet.
10. Klicken Sie auf **Schlüssel** im **Einstellungsbereich**. Erstellen Sie einen Schlüssel, indem Sie eine Schlüsselbeschreibung sowie eine Dauer im Abschnitt **Kennwörter** eingeben. 
11. Klicken Sie **Speichern** und kopieren Sie den Schlüssel. Dieser Schlüssel dient später als **Clientgeheimnis**. [![WMA-05-active-directory-create-key](./media/WMA-05-active-directory-create-key.png)](./media/WMA-05-active-directory-create-key.png)

## <a name="create-and-configure-a-user-account-in-finance-and-operations"></a>Erstellen und Konfigurieren eines Benutzerkontos in Finance and Operations
Um Finance and Operations zu aktivieren für Ihre Azure AD-Anwendung, müssen folgende Konfigurationsschritte abgeschlossen werden:

1.  Erstellen Sie ein neues Benutzerkonto in Azure Active Directory für den Finance and Operations-Mandanten. Der Zweck dieses Benutzerkontos ist, auf bestimmte benutzerdefinierte Dienste der Warehousing-App zuzugreifen, die der Finance and Operations-Server verfügbar macht. Nachdem Sie diesen Schritt abgeschlossen wurde, besitzen Sie WMDP-Benutzeranmeldeinformationen, die einer WMDP-E-Mail-Adresse und einem WMDP-Kennwort bestehen. Um die grundlegenden Schritte zum Hinzufügen von Benutzern zu Azure AD und Finance and Operations zu ermitteln, sehen Sie sich dieses Lernprogramm an [Anmelden für ein Finance and Operations-Abonnement](../../dev-itpro/dev-tools/sign-up-preview-subscription.md).
2.  Erstellen Sie einen Finance and Operations-Benutzer der den Warehousing-App-Benutzeranmeldeinformationen entspricht.
    1.  In Finance and Operations wechseln Sie zu **Systemverwaltung** &gt; **Allgemein** &gt; **Benutzer**.
    2.  Erstellen Sie einen neuen Benutzer
    3.  Weisen Sie den Warhouse-Mobilbenutzer zu, wie im folgenden Screenshot angezeigt werden. [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  Ordnen Sie die Azure Active Directory-Anwendung mit dem Warehousing-App-Benutzer zu.
    1.  In Finance and Operations wechseln sie zu **Systemverwaltung** &gt; **Einstellungen** &gt; **Azure Active Directory-Anwendung**.
    2.  Erstellen Sie eine neue Position.
    3.  Geben Sie die **Client-ID** ein (wird im vorherigen Abschnitt erhalten), geben Sie dieser Kennung einen Namen, und wählen Sie den zuvor erstellten Benutzer aus. Es wird empfohlen, dass Sie alle Geräte markieren, sodass Sie den Zugriff auf Finance and Operations von dieser Seite leicht entfernen können, sofern sie verloren gehen. [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Anwendung konfigurieren
Sie müssen die App auf dem Gerät konfigurieren, um mit dem Finance and Operations-Server über die Azure AD-Anwendung zu verbinden. Führen Sie dazu die folgenden Schritte aus.

1.  In der App wechseln Sie zu **Verbindungseinstellungen**.
2.  Deaktivieren Sie das **Demomodus** Feld. <br>[![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Geben Sie die folgenden Informationen ein: 
    + **Azure Active Directory-Client-IDs** – Die Client-ID können Sie über Schritt 9 „Erstellen einer Webdienstbewerbung in Active Directory " erhalten. 
    + **Azure Active Directory-Client-Schlüssel** – Den Clientschlüssel erhalten Sie in Schritt 11 „Erstellen einer Webdienstbewerbung in Active Directory“. 
    + **Azure Active Directory-Ressource** – Die Azure AD-Ressource bildet die Finance and Operations-Stamm-URL ab. **Hinweis**: Beenden Sie dieses Feld nicht mit einem Schrägstrichzeichen (/). 
    + **Azure Active Directory-Mandant** – Der Azure Active Directory-Mandant, der mit dem Finance and Operations-Server verwendet wird:`https://login.windows.net/your-AD-tenant-ID`. Beispiel: `https://login.windows.net/contosooperations.onmicrosoft.com.` 
    <br>**Hinweis**: Beenden Sie dieses Feld nicht mit einem Schrägstrichzeichen (/). 
    + **Unternehmen** – Geben Sie die juristische Person in Finance and Operations ein, mit der Sie die Anwendung verbinden möchten. <br>[![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Wählen Sie die **Zurück** Schaltfläche in der linken oberen Ecke der Anwendung aus. Die Anwendung stellt jetzt eine Verbindung mit Ihrem Finance and Operations-Server her, und der Anmeldebildschirm für die Lagerortarbeitskraft wird angezeigt. <br>[![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

Informationen darüber, wie Sie Dynamics 365 for Finance and Operations – Warehousing einrichten, um  Strichcodes mithilfe einer Kamera auf einem mobilen Gerät zu scannen, finden Sie unter [Scannen Sie Strichcodes mithilfe einer Kamera in Dynamics 365 for Finance and Operations – Warehousing](scan-bar-codes-using-a-camera.md)

## <a name="remove-access-for-a-device"></a>Aufheben des Zugriffs für ein Gerät
Im Fall von verlorenen oder beeinträchtigten Geräten müssen Sie den Zugriff des Geräts auf Finance and Operations entfernen. In den folgenden Schritten wird den empfohlenen Verarbeiten, um den Zugriff zu entfernen.

1.  In Finance and Operations wechseln sie zu **Systemverwaltung** &gt; **Einstellungen** &gt; **Azure Active Directory-Anwendung**.
2.  Löscht die Position, die dem Gerät entspricht, dem Sie Zugriff entfernen möchten. Merken Sie sich die **Client-ID**, die für das entfernte Gerät verwendet wird, Sie werden sie später benötigen.
3.  Melden Sie sich beim Azure-Portal an unter <https://portal.azure.com>.
4.  Klicken Sie auf das Symbol **Active Directory** im linken Menü, und stellen Sie sicher, dass Sie im richtigen Verzeichnis sind.
5.  Klicken Sie in der Liste auf **App-Registrierungen** und anschließend auf die Anwendung, die Sie konfigurieren möchten. Die Seite **Einstellungen** wird mit Konfigurationsinformationen angezeigt.
6.  Stellen Sie sicher, dass die **Client-ID** der Anwendung dieselbe wie in Schritt 2 in diesem Abschnitt ist.
7.  Klicken Sie auf die Schaltfläche **Löschen** im oberen Bereich.
8.  Klicken Sie in der daraufhin angezeigten Meldung auf **Ja**.

