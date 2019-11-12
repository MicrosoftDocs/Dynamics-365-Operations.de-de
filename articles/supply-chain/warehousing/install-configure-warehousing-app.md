---
title: 'Einrichten und Konfigurieren der Warehousing-App: Übersicht'
description: In diesem Thema wird erläutert, wie die Dynamics 365 for Finance and Operations Warehousing-App eingerichtet und konfiguriert wird.
author: MarkusFogelberg
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
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
ms.openlocfilehash: f629fffc5c424c244a25bb8faef0435814398ee1
ms.sourcegitcommit: 4aac45c84b87f463b22b318f5f6f729f8d737090
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/03/2019
ms.locfileid: "2548967"
---
# <a name="install-and-configure-the-warehousing-app-overview"></a>Einrichten und Konfigurieren der Warehousing-App: Übersicht

[!include [banner](../includes/banner.md)]

> [!NOTE]
> 
> In diesem Thema wird beschrieben, wie Lagerhaltung für Cloudbereitstellungen konfiguriert wird. Wenn Sie erfahren möchten, wie die Lagerhaltung für lokale Bereitstellungen konfiguriert wird, finden Sie Informationen unter [Lagerhaltung für lokale Bereitstellungen](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md).


In diesem Thema wird erläutert, wie die Dynamics 365 for Finance and Operations Warehousing-App eingerichtet und konfiguriert wird.

Die Lagerungs-App ist auf Google Play Store und Windows Store verfügbar. Für die aktuelle Version von Dynamics 365 Supply Chain Management wird die App als eigenständige Komponente bereitgestellt, die auf den Geräten für Lagerortarbeiten selbst bereitgestellt wird. Um die App zu verwenden, müssen Sie sie auf jedes Gerät herunterladen und konfigurieren und mit Ihrer Supply Chain Management-Umgebung verbinden. In diesem Thema wird beschrieben, wie App auf Ihren Geräten eingerichtet wird. Es wird auch gezeigt, wie der App konfiguriert wird, um sie mit Ihrer Supply Chain Management Umgebung zu verbinden.

## <a name="prerequisites"></a>Voraussetzungen
Die App ist auf Android- und Windows-Betriebssystemen verfügbar. Um diese App zu verwenden, müssen Sie eines der folgenden unterstützten Betriebssysteme haben, die auf Ihren Geräten eingerichtet werden. Sie müssen auch eine der folgenden unterstützten Versionen haben. Verwenden Sie die Informationen in der folgenden Tabelle, um zu prüfen, ob die Hardware und Software-Umgebung bereit ist die Installation zu unterstützen.

| Plattform                    | Version                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0, 7.0, 8.0, 9.0                                                                                                                                                     |
| Windows (UWP)               | Windows 10 (alle Vesionen)                                                                                                                                                   |
| Finance and Operations | Microsoft Dynamics 365 for Operations, Version 1611 <br>– oder – <br>Microsoft Dynamics AX Version 7.0/7.0.1 und Microsoft Dynamics AX-Plattform Update 2 mit Hotfix KB 3210014 |

## <a name="get-the-app"></a>Abrufen der App
-   Windows (UWP)
     - [Finance and Operations – Lagerhaltung im Windows Store](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android
    - [Finance and Operations - Lagerung im Google Play Store](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

> [!NOTE]
> Die Zebra AppGallery wurde zurückgezogen, was bedeutet, dass die Lagerorte-App an diesem Speicherort nicht mehr zum Download verfügbar ist.

## <a name="create-a-web-service-application-in-azure-active-directory"></a>Erstellen einer Webdienstanwendung in Azure Active Directory
Um der App die Interaktion mit einem bestimmten Supply Chain Management-Server zu ermöglichen, müssen Sie eine Webdienstanwendung in einem Azure Active Directory für den Supply Chain Management-Mandanten erfassen. Aus Sicherheitsgründen wird empfohlen, dass Sie eine Webdienstanwendung für jedes Gerät erstellt werden, das Sie verwenden. Um eine Webdienstbewerbung in Azure Active Directory (Azure AD) zu erstellen, führen Sie die folgenden Schritte aus:

1.  In einem Webbrowser gehen Sie zu <https://portal.azure.com>.
2.  Geben Sie den Namen und das Kennwort des Benutzers ein, der Zugriff auf Azure Abonnement hat.
3.  Klicken Sie im Azure-Portal im linken Navigationsbereich auf **Azure Active Directory**.[](./media/WMA-01-active-directory-example.png)[![WMA-01-active-directory-example](./media/WMA-01-active-directory-example.png )](./media/WMA-01-active-directory-example.png)
4.  Stellen Sie sicher, dass die Active Directory-Instanz diejenige ist, die von Supply Chain Management verwendet wird.
5.  Klicken Sie in der Liste auf **App-Registrierungen**. [![WMA-02-active-directory-app-registrations](./media/WMA-02-active-directory-app-registrations.png)](./media/WMA-02-active-directory-app-registrations.png)
6.  Klicken Sie im oberen Bereich auf **Neue Erfassung**. Der **Einen Anwendungsassistent erfassen**-Assistent startet.
7.  Geben Sie einen Namen für die Anwendung ein und wählen Sie **Nur Konten in diesem organisatorischen Verzeichnis** aus. Kicken Sie auf **Erfassen**.  [![WMA-03-active-directory-add-application](./media/WMA-03-active-directory-add-application.png)](./media/WMA-03-active-directory-add-application.png)
8.  Die neue App-Erfassung wird geöffnet. [![WMA-04-active-directory-configure-app](./media/WMA-04-active-directory-configure-app.png)](./media/WMA-04-active-directory-configure-app.png)
9.  Merken Sie sich die **Anwendungskennung**, Sie werden sie später benötigen. Die **Anwendungskennung** wird später als die **Client-ID** bezeichnet.
10. Klicken Sie auf **Zertifikate und Geheimnisse** im Bereich **Verwalten**. Klicken Sie auf **Neues Kundengeheimnis**. [![WMA-05-active-directory-create-key](./media/WMA-05-active-directory-create-key.png)](./media/WMA-05-active-directory-create-key.png)
11. Erstellen Sie einen Schlüssel, indem Sie eine Schlüsselbeschreibung sowie eine Dauer im Abschnitt **Kennwörter** eingeben. Klicken Sie **Hinzufügen** und kopieren Sie den Schlüssel. Dieser Schlüssel dient später als **Clientgeheimnis**. [![WMA-06-active-directory-save-key](./media/WMA-06-active-directory-save-key.png)](./media/WMA-06-active-directory-save-key.png)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a>Erstellen und Konfigurieren eines Benutzerkontos in Supply Chain Management
Um Supply Chain Management für Ihre Azure AD-Anwendung zu aktivieren, müssen folgende Konfigurationsschritte abgeschlossen werden:

1.  Erstellen Sie einen Supply Chain Management-Benutzer der den Warehousing-App-Benutzeranmeldeinformationen entspricht.
    1.  Wechseln Sie zu **Systemverwaltung** &gt; **Benutzer** &gt; **Benutzer**.
    2.  Erstellen Sie einen neuen Benutzer
    3.  Weisen Sie den Warhouse-Mobilbenutzer zu, wie im folgenden Screenshot angezeigt werden. [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

2.  Ordnen Sie die Azure Active Directory-Anwendung dem Lagerorte-App-Benutzer zu.
    1.  In Supply Chain Management wechseln Sie zu **Systemverwaltung** &gt; **Einstellungen** &gt; **Azure Active Directory-Anwendungen**.
    2.  Erstellen Sie eine neue Position.
    3.  Geben Sie die **Client-ID** ein (wird im vorherigen Abschnitt erhalten), geben Sie dieser Kennung einen Namen, und wählen Sie den zuvor erstellten Benutzer aus. Es wird empfohlen, dass Sie alle Geräte markieren, sodass Sie den Zugriff auf Supply Chain Management von dieser Seite leicht entfernen können, sofern sie verloren gehen. [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Anwendung konfigurieren
Sie müssen die App auf dem Gerät so konfigurieren, dass eine Verbindung zum Supply Chain Management-Server über die Azure AD-Anwendung hergestellt wird. Führen Sie dazu die folgenden Schritte aus.

1.  In der App wechseln Sie zu **Verbindungseinstellungen**.
2.  Deaktivieren Sie das **Demomodus** Feld. <br>[![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Geben Sie die folgenden Informationen ein: 
    + **Azure Active Directory-Client-IDs** – Die Client-ID können Sie über Schritt 9 „Erstellen einer Webdienstbewerbung in Active Directory " erhalten. 
    + **Azure Active Directory-Client-Schlüssel** – Den Clientschlüssel erhalten Sie in Schritt 11 „Erstellen einer Webdienstbewerbung in Active Directory“. 
    + **Azure Active Directory-Ressource** – Die Azure AD-Ressource bildet die Supply Chain Management-Stamm-URL ab. **Hinweis**: Beenden Sie dieses Feld nicht mit einem Schrägstrichzeichen (/). 
    + **Azure Active Directory-Mandant** – Der Azure AD-Mandant, der mit dem Supply Chain Management-Server verwendet wird: `https://login.windows.net/your-AD-tenant-ID`. Beispiel: `https://login.windows.net/contosooperations.onmicrosoft.com.` 
    <br>**Hinweis**: Beenden Sie dieses Feld nicht mit einem Schrägstrichzeichen (/). 
    + **Unternehmen** – Geben Sie die juristische Person in Supply Chain Management ein, mit der Sie die Anwendung verbinden möchten. <br>[![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Wählen Sie die **Zurück** Schaltfläche in der linken oberen Ecke der Anwendung aus. Die Anwendung stellt jetzt eine Verbindung mit Ihrem Supply Chain Management-Server her, und der Anmeldebildschirm für die Lagerortarbeitskraft wird angezeigt. <br>[![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

Informationen zum Einrichten der Lagerungs-App zum Scannen von Strichcodes mithilfe einer Kamera auf einem mobilen Gerät finden Sie unter [Strichcodes mithilfe einer Kamera in Dynamics 365 for Finance and Operations – Lagerung](scan-bar-codes-using-a-camera.md) scannen.

## <a name="remove-access-for-a-device"></a>Aufheben des Zugriffs für ein Gerät
Im Fall von verlorenen oder beeinträchtigten Geräten müssen Sie den Zugriff des Geräts auf Supply Chain Management entfernen. In den folgenden Schritten wird den empfohlenen Verarbeiten, um den Zugriff zu entfernen.

1.  Gehen Sie zu **Systemadministration** &gt; **Einstellungen** &gt; **Azure Active Directory-Anwendungen**.
2.  Löscht die Position, die dem Gerät entspricht, dem Sie Zugriff entfernen möchten. Merken Sie sich die **Client-ID**, die für das entfernte Gerät verwendet wird, Sie werden sie später benötigen.
3.  Melden Sie sich beim Azure-Portal an unter <https://portal.azure.com>.
4.  Klicken Sie auf das Symbol **Active Directory** im linken Menü, und stellen Sie sicher, dass Sie im richtigen Verzeichnis sind.
5.  Klicken Sie in der Liste auf **App-Registrierungen** und anschließend auf die Anwendung, die Sie konfigurieren möchten. Die Seite **Einstellungen** wird mit Konfigurationsinformationen angezeigt.
6.  Stellen Sie sicher, dass die **Client-ID** der Anwendung dieselbe wie in Schritt 2 in diesem Abschnitt ist.
7.  Klicken Sie auf die Schaltfläche **Löschen** im oberen Bereich.
8.  Klicken Sie in der daraufhin angezeigten Meldung auf **Ja**.
