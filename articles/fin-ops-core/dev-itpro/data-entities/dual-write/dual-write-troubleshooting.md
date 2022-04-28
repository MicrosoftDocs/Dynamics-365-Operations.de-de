---
title: Allgemeine Problembehandlung
description: Dieses Thema enthält allgemeine Informationen zur Problembehandlung für die duales Schreiben-Integration zwischen Apps für Finanzen und Betrieb und Dataverse.
author: RamaKrishnamoorthy
ms.date: 04/07/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 8b5951f9f40179ca0bf31f5cccf1f05a0f968213
ms.sourcegitcommit: 1843235766b6f8cf950a13a310e9f4f2f53c59a4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/07/2022
ms.locfileid: "8554598"
---
# <a name="general-troubleshooting"></a>Allgemeine Problembehandlung

[!include [banner](../../includes/banner.md)]



Dieses Thema enthält allgemeine Informationen zur Problembehandlung für die duales Schreiben-Integration zwischen Apps für Finanzen und Betrieb und Dataverse.

> [!IMPORTANT]
> Einige der in diesem Thema behandelten Probleme erfordern möglicherweise entweder die Systemadministratorrolle oder Microsoft Azure Active Directory (Azure AD) Anmeldeinformationen des Mandantenadministrators. Im Abschnitt zu jedem Problem wird erläutert, ob eine bestimmte Rolle oder Anmeldeinformationen erforderlich sind.

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Aktivieren und Anzeigen des Plug-In-Überwachungsprotokolls in Dataverse, um Fehlerdetails anzuzeigen

Ablaufverfolgungsprotokolle können bei der Behebung von Problemen mit der Dual-Write-Live-Synchronisierung zwischen Finance & Operations und Dataverse nützlich sein. Diese Protokolle können den Teams, die technischen und entwicklungsbezogenen Support für Dynamics 365 bereitstellen, spezifische Details liefern. In diesem Artikel wird beschrieben, wie Ablaufverfolgungsprotokolle aktiviert und angezeigt werden. Ablaufverfolgungsprotokolle werden auf der Seite „Dynamics 365-Einstellungen“ verwaltet und erfordern zum Ändern und Anzeigen Administrationsrechte. 

**Erforderliche Rolle zum Aktivieren des Ablaufverfolgungsprotokolls und zum Anzeigen von Fehlern:** System Administrator

### <a name="turn-on-the-trace-log"></a>Ablaufverfolgungsprotokoll aktivieren
Um die Nachverfolgung einzuschalten, führen Sie diese Schritte aus.

1.  Melden Sie sich bei Dynamics 365 an, und wählen Sie in der oberen Navigationsleiste **Einstellungen** aus. Klicken Sie auf der Seite „Systeme“ auf **Verwaltung**.
2.  Wählen Sie auf der Seite „Verwaltung“ die Option **Systemeinstellungen** aus.
3.  Wählen Sie die Registerkarte **Anpassung** und „Plug-In“, und ändern Sie dann im Abschnitt für die angepasste Workflow-Aktivitätsverfolgung die Dropdown-Auswahl in **Alle**. So werden alle Aktivitäten nachverfolgt und umfassende Daten für die Teams bereitgestellt, die potenzielle Probleme überprüfen müssen.

> [!NOTE]
> Wenn Sie im Dropdown-Menü **Ausnahme** auswählen, erhalten Sie nur Ablaufverfolgungsinformationen, wenn Ausnahmen (Fehler) auftreten.

Nach der Aktivierung werden die Plug-In-Ablaufverfolgungsprotokolle weiterhin erfasst, bis sie manuell deaktiviert werden. Kehren Sie dazu zu dieser Stelle zurück, und wählen Sie **Aus**.

### <a name="view-the-trace-log"></a>Ablaufverfolgungsprotokoll anzeigen
Um die Nachverfolgung anzuzeigen, führen Sie diese Schritte aus.

1. Wählen Sie auf der Seite mit den Dynamics 365-Einstellungen in der oberen Navigationsleiste **Einstellungen** aus. 
2. Wählen Sie im Abschnitt **Anpassungen** auf der Seite die Option **Plug-In-Ablaufverfolgungsprotokoll** aus.
3. Sie können Einträge in der Liste der Ablaufverfolgungsprotokolle basierend auf Typname und/oder Meldungsname finden.
4. Öffnen Sie den gewünschten Eintrag, um das vollständige Protokoll anzuzeigen. Der Nachrichtenblock im Abschnitt „Ausführung“ stellt verfügbare Informationen für das Plug-In bereit. Falls verfügbar, werden auch Ausnahmedetails bereitgestellt. 

Sie können den Inhalt der Ablaufverfolgungsprotokolle kopieren und in eine andere Anwendung wie Notepad oder andere Tools einfügen, um Protokolle oder Textdateien anzuzeigen und den gesamten Inhalt einfacher darstellen zu können. 

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>Debug-Modus aktivieren, um Probleme mit der Live-Synchronisation in Apps für Finanzen und Betrieb zu beheben

**Erforderliche Rolle zum Anzeigen der Fehler:** System Administrator

Duales Schreiben-Fehler, die ihren Ursprung in Dataverse haben, können in der Finance und Operations App auftreten. Um die ausführliche Protokollierung für die Fehler zu aktivieren, gehen Sie wie folgt vor:

1. Für alle Projektkonfigurationen in der Finance und Operations App gibt es ein Flag **IsDebugMode** in der Tabelle **DualWriteProjectConfiguration**.
2. Öffnen Sie die **DualWriteProjectConfiguration** mit dem Excel-Addin. Um das Add-In zu verwenden, aktivieren Sie den Entwurfsmodus im Excel-Add-In Finance und Operations und fügen die **DualWriteProjectConfiguration** zum Blatt hinzu. Weitere Informationen finden Sie unter [Entitätsdaten mit Excel anzeigen und aktualisieren](../../office-integration/use-excel-add-in.md).
3. Legen Sie **IsDebugMode** auf dem Projekt auf **Ja** fest.
4. Führen Sie das Szenario aus, das Fehler generiert.
5. Die ausführlichen Protokolle werden in der Tabelle **DualWriteErrorLog** gespeichert.
6. Um die Daten im Tabellenbrowser nachzuschlagen, verwenden Sie den folgenden Link: `https://999aos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`, ersetzen Sie `999` nach Bedarf.
7. Aktualisieren Sie erneut nach [KB 4595434](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=98e5dc124ac125c57ad633d885ac612aea3ddb8f4abf9d71ab3aa354f2e06cbe), das für Plattform-Updates 37 und später verfügbar ist. Wenn Sie diesen Fix installiert haben, werden im Debug-Modus mehr Protokolle erfasst.  

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Überprüfen Sie Synchronisierungsfehler auf der virtuellen Maschine für die Finance und Operations App

**Erforderliche Rolle zum Anzeigen der Fehler:** Systemadministrator

1. Melden Sie sich bei Microsoft Dynamics Lifecycle Services (LCS) an.
2. Öffnet das LCS-Projekt, das Sie ausgewählt haben, um das Testing für das duale Schreiben durchzuführen.
3. Wählen Sie die Kachel **Cloud gehostete Umgebungen** aus.
4. Verwenden Sie Remote Desktop, um sich bei der virtuellen Maschine (VM) für die Finance und Operations App anzumelden. Verwenden Sie das lokale Konte, das in LCS angezeigt wird.
5. Öffnen Sie nun die Ereignisanzeige.
6. Wählen Sie **Anwendungs- und Dienstprotokolle \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operativ**.
7. Überprüfen Sie die Liste der letzten Fehler.

## <a name="dual-write-ui-landing-page-showing-blank"></a>Dual-Write-UI-Zielseite wird leer angezeigt
Beim Öffnen der Dual-Write-Seite im Browser Microsoft Edge oder Google Chrome, wird die Startseite nicht geladen und Sie sehen eine leere Seite oder einen Fehler wie „Ein Fehler ist aufgetreten“.
In den Entwicklungstools sehen Sie einen Fehler in den Konsolenprotokollen:

>bundle.eed39124e62c58ef34d2.js:37 DOMException: Eigenschaft 'sessionStorage' von 'Window' konnte nicht gelesen werden: Zugriff für dieses Dokument verweigert. at t.storeInSessionStorage (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:16:136860 ) at new t (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:69:20103 ) at ci (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:44115 ) at Eo (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:58728 ) at jo (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:65191 ) at Nr (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:84692 ) at Or (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:85076 ) at Ss (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:91750 ) at vs (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:91130 ) at hs (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:90151 )

Die Bedienoberfläche verwendet den „Sitzungsspeicher“ des Browsers, um einige Eigenschaftswerte zum Laden der Startseite zu speichern. Damit dies funktioniert, müssen Cookies von Drittanbietern im Browser für die Website zugelassen werden. Der Fehler weist darauf hin, dass die Bedienoberfläche nicht auf den Sitzungsspeicher zugreifen kann. Dieses Problem kann in zwei Szenarien auftreten:

1.  Sie öffnen die Bedienoberfläche im Inkognito-Modus von Edge/Chrome, und Drittanbieter-Cookies im Inkognito-Modus werden blockiert.
2.  Sie haben Drittanbieter-Cookies in Edge/Chrome vollständig blockiert.

### <a name="mitigation"></a>Mitigation
Cookies von Drittanbietern müssen in den Browsereinstellungen zugelassen werden.

### <a name="google-chrome-browser"></a>Google Chrome-Browser
1. Möglichkeit:
1.  Gehen Sie zu den Einstellungen, indem Sie „chrome://settings/“ in die Adressleiste eingeben, und navigieren Sie dann zu „Datenschutz und Sicherheit -> Cookies und andere Websitedaten“.
2.  Wählen Sie „Alle Cookies zulassen“ aus. Wenn Sie dies nicht möchten, entscheiden Sie sich für die zweite Option.

2. Möglichkeit:
1.  Gehen Sie zu den Einstellungen, indem Sie „chrome://settings/“ in die Adressleiste eingeben, und navigieren Sie dann zu „Datenschutz und Sicherheit -> Cookies und andere Websitedaten“.
2.  Wenn „Cookies von Drittanbietern im Inkognitomodus blockieren“ oder „Drittanbieter-Cookies blockieren“ ausgewählt ist, gehen Sie zu „Websites, die Cookies immer verwenden dürfen“, und klicken Sie auf **Hinzufügen**. 
3.  Fügen Sie den Namen der Website Ihrer Finanz- und Betriebs-Apps hinzu: https://<Ihre_FinOp_Instanz>.cloudax.dynamics.com. Stellen Sie sicher, dass Sie das Kontrollkästchen für „Alle Cookies, nur auf dieser Website“ aktivieren. 

### <a name="microsoft-edge-browser"></a>Microsoft Edge-Browser
1.  Navigieren Sie zu „Einstellungen -> Websiteberechtigungen -> Cookies und Websitedaten“.
2.  Deaktivieren Sie „Cookies von Drittanbietern blockieren“.  

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a>Lösen Sie die Verknüpfung und verknüpfen Sie eine andere Dataverse-Umgebung aus einer Finance und Operations App

**Benötigte Rolle zum Aufheben der Verknüpfung der Umgebung:** Systemadministrator für eine der Apps Finance und Operations und Dataverse.

1. Melden Sie sich bei der Finance und Operations App an.
2. Gehe zu **Arbeitsbereiche \> Datenmanagement** und wählen Sie die Kachel **Duales Schreiben**.
3. Wählen Sie alle ausgeführten Zuordnungen aus, und wählen Sie **Beenden**.
4. Wählen Sie **Verknüpfung für Umgebung aufheben** aus.
5. Wählen Sie **Ja** aus, um den Vorgang zu bestätigen.

Sie können jetzt eine neue Umgebung verknüpfen.

## <a name="unable-to-view-the-sales-order-line-information-form"></a>Das Formular für die Auftragspositionsinformationen können nicht angezeigt werden. 

Wenn Sie in Dynamics 365 Sales einen Autrag erstellen, können Sie durch das Klicken auf **+ Produkte hinzufügen** möglicherweise zum Bestellformular für Dynamics 365 Project Operations weitergeleitet werden. Von diesem Formular aus gibt es keine Möglichkeit, das Formular **Information** der Kundenauftragsposition anzuzeigen. Die Option für **Information** wird in der Dropdownliste unter **Neue Auftragsposition** nicht angezeigt. Dies liegt daran, dass Project Operations in Ihrer Umgebung installiert wurde.

Um die Formularoption **Information** wieder zu aktivieren, führen Sie die folgenden Schritte aus:

1. Navigieren Sie zur Tabelle **Auftragsposition**.
2. Suchen Sie das **Information**-Formular unter dem Formularknoten.
3. Wählen Sie das Formular **Information** und klicken Sie auf **Sicherheitsrollen aktivieren**.
4. Ändern Sie die Sicherheitseinstellung in **Anzeige für alle**.

## <a name="how-to-enable-and-save-network-trace-so-that-traces-can-be-attached-to-support-tickets"></a>So aktivieren und speichern Sie die Netzwerkaufzeichnung, damit die Aufzeichnungen an Support-Tickets angehängt werden können

Das Support-Team muss möglicherweise Netzwerkspuren überprüfen, um einige Probleme zu beheben. Um eine Netzwerkspur zu erstellen, gehen Sie folgendermaßen vor:

### <a name="google-chrome-browser"></a>Google Chrome-Browser

1. Drücken Sie in der geöffneten Registerkarte **F12** oder wählen Sie **Entwickler-Tools**, um die Entwickler-Tools zu öffnen.
2. Öffnen Sie die Registerkarte **Netzwerk** und geben Sie **integ** in das Filtertextfeld ein.
3. Führen Sie Ihr Szenario aus und beobachten Sie, wie die Anfragen protokolliert werden.
4. Klicken Sie mit der rechten Maustaste auf die Einträge und wählen Sie **Alle als HAR mit Inhalt speichern**.

### <a name="microsoft-edge-browser"></a>Microsoft Edge-Browser

1. Drücken Sie in der geöffneten Registerkarte **F12** oder wählen Sie **Entwickler-Tools**, um die Entwickler-Tools zu öffnen.
2. Öffnen Sie die Registerkarte **Netzwerk**.
3. Führen Sie Ihr Szenario aus.
4. Wählen Sie **Speichern**, um die Ergebnisse als HAR zu exportieren.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
