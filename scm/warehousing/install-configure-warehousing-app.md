---
title: "Installieren und Konfigurieren von Microsoft Dynamics 365 für Arbeitsgänge &#8211; Einlagerung"
description: "In diesem Thema wird beschrieben, wie Microsoft Dynamics 365 für Warehousing - Arbeitsgänge eingerichtet und konfiguriert."
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

# <a name="install-and-configure-microsoft-dynamics-365-for-operations-8211-warehousing"></a>Installieren und Konfigurieren von Microsoft Dynamics 365 für Arbeitsgänge &#8211; Einlagerung

In diesem Thema wird beschrieben, wie Microsoft Dynamics 365 für Warehousing - Arbeitsgänge eingerichtet und konfiguriert.

Dynamics 365 für Arbeitsgänge Warehousing - handelt es sich um eine Anwendung, die auf Play Google Store und Windows Store verfügbar ist. Für die aktuelle Version von Microsoft Dynamics 365 für Arbeitsgänge, wird diese Anwendungskonfigurationstool als eigenständige Komponente bereitgestellt, die auf den SelbstBereitstellung Geräten bedeutet, die für Lagerortaufgaben verwendet werden. Um der Zeit-App in Ihrem Dynamics 365 für Arbeitsgänge Umgebung zu verwenden, müssen Sie auf jedem der Zeit-App Gerät herunterladen und konfiguriert werden um für Ihr Dynamics 365 für Arbeitsgangsumgebung herzustellen. In diesem Thema wird beschrieben, wie der Zeit-App auf Ihren Geräten eingerichtet. Es werden auch, wie der Zeit-App konfiguriert, um für Ihr Dynamics 365 für Arbeitsgangsumgebung herzustellen.

## <a name="prerequisites"></a>Voraussetzungen
Die auf Android- Zeit-App ist und Windows-Betriebssystemen verfügbar. Um diese Anwendungskonfigurationstool zu verwenden, müssen Sie eines der folgenden unterstützten Betriebssysteme haben, die auf Ihren Geräten eingerichtet werden. Sie müssen eine der unterstützten folgenden Versionen von Microsoft Dynamics 365 für Arbeitsgänge verfügen. Verwenden Sie die Informationen in der folgenden Tabelle aus, die überprüft werden soll, wenn die Hardware und Software-Umgebung bereit ist die Installation, zu unterstützen.

| Plattform                    | Version                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| Windows UWP ()               | Windows alle Versionen (10)                                                                                                                                                   |
| Dynamics 365 für Arbeitsgänge | Microsoft Dynamics 365 für Arbeitsgangsversion 1611 - 7.0/7.0.1 oder Version Microsoft Dynamics Public-Vorlage Dynamics AX und Microsoft Dynamics AX-Plattformaktualisierung 2 mit 3210014 KB Hotfix |

## <a name="get-the-app"></a>Erwerben der Zeit-App ab
-   Windows UWP (-) [Dynamics 365 für Arbeitsgänge - Warehousing auf Windows Store (https://www.microsoft.com/store/apps/9p1bffd5tstm)]
-   - Android [Dynamics 365 für Arbeitsgänge Warehousing - auf dem Play Google Store (https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)]

## <a name="create-a-web-service-application-in-active-directory"></a>Erstellen Sie eine Webdienstbewerbung in Active Directory
Um der Zeit-App Möglichkeit erhalten mit bestimmten Dynamics 365 für Arbeitsgänge Server zu interagieren, müssen Sie eine Webdienstbewerbung in Azure Active Directory für die Dynamics 365 für Arbeitsgangsmandanten erfassen. Aus Sicherheitsgründen wird empfohlen, dass Sie eine Webdienstbewerbung für jedes Gerät erstellt werden, das Sie verwenden. Um eine Webdienstbewerbung in Azure Active Directory " Azure ANZEIGE) erstellen, führen Sie die folgenden Schritte aus:

1.  In einem Webbrowser fahren Sie https://manage.windowsazure.com>.
2.  Geben Sie den Namen und das Kennwort des Benutzers ein, der Zugriff auf Azure Dauerauftrag hat.
3.  Im Azure Portal im linken Navigationsbereich, klicken Sie ** Active Directory **. [] (. /media/wh-01-active-directory-example.png) [] (wh-01-active-directory-example ![. /media/wh-01-active-directory-example.png)]". /media/wh-01-active-directory-example.png)
4.  Im Raster wählen die Active Directory-Instanz aus, die von Dynamics 365 für Arbeitsgänge verwendet wird.
5.  Klicken Sie auf der Leiste Symbolleiste auf Anwendungen ** **. ![wh-02-active-directory-applications ([]. /media/wh-02-active-directory-applications-1024x197.png)]". /media/wh-02-active-directory-applications.png)
6.  Klicken Sie im unteren Fenster auf ** Hinzufügen **. ** Die Bewerbung fügen Sie Assistentenanfänge ** hinzu.
7.  Geben Sie einen Namen für die Anwendung ein und wählen Sie aus ** Webanwendung und/oder Internet API **. ![wh-03-active-directory-add-application ([]. /media/wh-03-active-directory-add-application.png)]". /media/wh-03-active-directory-add-application.png)
8.  Geben Sie die Bereitschafts-URL, der die Anwendungs-URL in Ihrem Mandanten Stamm Arbeitsgänge, ist die URL ein. Die Bereitschafts-URL ist derzeit nicht aktiv, sofern der Zeit-App verwendet, authentifiziert, jedoch, ist ein Pflichtfeld. Geben Sie die URL auf dem gleichen ID-URI-Gebiet Zeit-App ein. ![wh-04-ad-add-properties ([]. /media/wh-04-ad-add-properties.png)]". /media/wh-04-ad-add-properties.png)
9.  Zur ** konfigurieren Sie ** Registerkarte. ![wh-05-ad-configure-app ([]. /media/wh-05-ad-configure-app.png)]". /media/wh-05-ad-configure-app.png)
10. Navigieren Sie nach unten, bis der ** Berechtigungen anderen Bewerbungen ** Abschnitt finden. ** Sie auf Hinzufügen Anwendung ** hinzu. ![wh-06-ad-app-add-permissions ([]. /media/wh-06-ad-app-add-permissions.png)]". /media/wh-06-ad-app-add-permissions.png)
11. ** Wählen Sie Microsoft Dynamics ERP ** in der Liste aus. Klicken Sie auf die Sie schließen ** Scheck ab ** Schaltfläche in der rechten Ecke der Seite. ![wh-07-ad-select-permissions ([]. /media/wh-07-ad-select-permissions.png)]". /media/wh-07-ad-select-permissions.png)
12. ** Delegaten-Berechtigungen ** In der Liste wählen Sie alle Kontrollkästchen. Click **Save**. ![wh-08-ad-delegate-permissions ([]. /media/wh-08-ad-delegate-permissions.png)]". /media/wh-08-ad-delegate-permissions.png)
13. Notieren Sie die folgenden Informationen:
    -   ** Client-ID ** - seit dem Rollup der Seite durch, finden Sie Client-ID ** ** angezeigt.
    -   ** Schlüssel ** - im ** Schlüssel ** Abschnitt, erstellen einen Schlüssel, indem er Dauer aus, und kopieren den Schlüssel. Dieser Schlüssel später als Unternehmen Kundengeheimnis ** **.

## <a name="create-and-configure-a-user-account-in-dynamics-365-for-operations"></a>Erstellen und Konfigurieren Sie ein Benutzerkonto in Dynamics 365 für Arbeitsgänge
Wählen Sie Dynamics 365 für Arbeitsgänge zu aktivieren Azure um die ANZEIGENbewerbung zu verwenden, müssen folgende Konfigurationsschritte abgeschlossen werden:

1.  Erstellen eines neuen Benutzerkontos in Azure Active Directory für die Dynamics 365 für Arbeitsgangsmandanten. Der Zweck dieses Benutzerkontos ist, bestimmte die Steuerbehörde gesendet der Warehousing-App zuzugreifen, auf das Dynamics 365 für Arbeitsgangsserver verfügbar macht. Nachdem Sie diesen Schritt abgeschlossen wurde, besitzen Sie WMDP-Benutzeranmeldeinformationen, die einer WMDP-E-Mail-Adresse und einem WMDP-Kennwort bestehen. Um die grundlegenden Schritte zum Hinzufügen von Benutzern zur Azure ANZEIGE und von Microsoft Dynamics 365 für Arbeitsgänge zu ermitteln, verweisen Sie dieses Lernprogramm an: [Anmelden Microsoft Dynamics 365 für Arbeitsgangsdauerauftrag] angezeigt( /dynamics365/operations/dev-itpro/sign-up-preview-subscription).
2.  Erstellen Sie Dynamics 365 für Arbeitsgangsbenutzer, der zu den Warehousing-App-Benutzeranmeldeinformationen entspricht.
    1.  In Dynamics 365 für Arbeitsgänge, fahren ** Systemverwaltung ** &gt; ** Common ** &gt; ** ** Benutzer.
    2.  Erstellen eines neuen Benutzers erstellen.
    3.  Weisen Sie den Benutzer der Lagerort geräts mobilen, wie im folgenden Screenshot angezeigt werden. ![wh-09-add-user-security-role ([]. /media/wh-09-add-user-security-role.png)]". /media/wh-09-add-user-security-role.png)

3.  Ordnen Sie die Azure Active Directory-Bewerbung mit dem Warehousing-App-Benutzer zu.
    1.  In Dynamics 365 für Arbeitsgänge, fahren ** Systemverwaltung ** &gt; ** Einstellungen ** &gt; ** Azure Active Directory-Bewerbungen **.
    2.  Erstellen Sie eine neue Position.
    3.  Geben Sie ein Client-ID ** ** (wird im letzten Abschnitt), geben Sie dieser Kennung einen Namen, und wählen Sie den zuvor erstellten Benutzer aus. Es wird empfohlen, dass Sie alle Geräte markiert, sodass Sie den Zugriff zu Dynamics 365 für Arbeitsgänge von dieser Seite können leicht entfernen, sofern sie verloren gehen. ![wh-10-ad-applications-form ([]. /media/wh-10-ad-applications-form.png)]". /media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Konfigurieren der Anwendung
Sie müssen der Zeit-App im Gerät konfigurieren, um an das Dynamics 365 für Arbeitsgangsserver durch die Azure ANZEIGENbewerbung herzustellen. Um dies zu bewerkstelligen, führen Sie die folgenden Schritte aus.

1.  In der Zeit-App wechseln ** Verbindungseinstellungen **.
2.  Deaktivieren Sie das ** Demomodus ** Feld. ![wh-11-app-connection-settings-demo-mode ([]. /media/wh-11-app-connection-settings-demo-mode-169x300.png)]". /media/wh-11-app-connection-settings-demo-mode.png)
3.  Geben Sie die folgenden Informationen ein: ** - Azure Active Directory-Client-ID ** - Die Client-ID wird in Schritt 13 in "Erstellen einer Webdienstbewerbung in Active Directory " erhalten. - ** Azure Active Directory-Kundengeheimnis ** - Das Kundengeheimnis wird in Schritt 13 in "Erstellen einer Webdienstbewerbung in Active Directory " erhalten. - ** Azure Active Directory-Ressource ** - Die Azure ANZEIGENverzeichnisressource enthält das Dynamics 365 für Arbeitsgangsstamm URL dar. ** Hinweis **: Beenden Sie dieses Feld nicht mit einem Schrägstrichzeichen (/). - ** Azure Active Directory-Mandant ** - Der Azure verwendet ANZEIGENverzeichnismandant dem Dynamics 365 für Arbeitsgangsserver: https://login.windows.net/your-AD-tenant-ID &lt;&gt;. Beispiel: https://login.windows.net/contosooperations.onmicrosoft.com. 
** Hinweis **: Beenden Sie dieses Feld nicht mit einem Schrägstrichzeichen (/). - ** Unternehmen ** - Geben Sie die juristische Person in Dynamics 365 für Arbeitsgänge ein, auf die die Anwendung herstellen soll. ![wh-12-app-connection-settings ([]. /media/wh-12-app-connection-settings-169x300.png)]". /media/wh-12-app-connection-settings.png)
4.  Wählen Sie die Rückseite ** ** Schaltfläche in der linken oberen Ecke der Bewerbung aus. Die Anwendung umfasst jetzt an Ihr Dynamics 365 für Arbeitsgangsserver anzeigen und der Bildschirm Anmeldung Lagerarbeiter für den Bogen wird angezeigt. ![wh-13-log-in-screen ([]. /media/wh-13-log-in-screen-180x300.png)]". /media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>Aufheben des Zugriffs für ein Gerät
Im Fall von verlorenen oder beeinträchtigten Geräts müssen Sie den Zugriff zu Dynamics 365 für Arbeitsgänge für das Gerät entfernen. In den folgenden Schritten wird den empfohlenen Verarbeiten, um den Zugriff zu entfernen.

1.  In Dynamics 365 für Arbeitsgänge, fahren ** Systemverwaltung ** &gt; ** Einstellungen ** &gt; ** Azure Active Directory-Bewerbungen **.
2.  Löscht die Position, die wieder dem Gerät entspricht, dem Sie Zugriff entfernen möchten. Hinweis hinunter ** Client-ID ** verwendet für das Gerät erfasst.
3.  Melden Sie sich das Azure klassische Portal unter <> https://manage.windowsazure.com.
4.  Klicken Sie auf das Symbol ** ** Active Directory im linken Menü, und klicken Sie anschließend auf das gewünschte Verzeichnis.
5.  Klicken Sie im Hauptmenü klicken auf Anwendungen ** ** und anschließend auf die Anwendung, die Sie konfigurieren möchten. ** Die Schnellstart ** Seite wird mit einmaligen Anmelden und weitere Konfigurationsinformationen.
6.  Klicken Sie auf die Registerkarte ** konfigurieren Sie **, zurücksetzen Sie unten und stellen Sie sicher, dass Client-ID ** ** der Anwendung das gleiche wie in Schritt 2 dieses Abschnitts ist.
7.  Klicken Sie auf die Schaltfläche Löschen ** ** in der Befehlsleiste.
8.  ** Auf Ja ** Bestätigungsmeldung in der.



