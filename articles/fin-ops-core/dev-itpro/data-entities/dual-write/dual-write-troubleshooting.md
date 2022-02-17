---
title: Allgemeine Problembehandlung
description: Dieses Thema enthält allgemeine Informationen zur Problembehandlung für die duales Schreiben-Integration zwischen Apps für Finanzen und Betrieb und Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f6f5b9f26990e2f4db9bf69040a6c4be31400b40
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062337"
---
# <a name="general-troubleshooting"></a>Allgemeine Problembehandlung

[!include [banner](../../includes/banner.md)]



Dieses Thema enthält allgemeine Informationen zur Problembehandlung für die duales Schreiben-Integration zwischen Apps für Finanzen und Betrieb und Dataverse.

> [!IMPORTANT]
> Einige der in diesem Thema behandelten Probleme erfordern möglicherweise entweder die Systemadministratorrolle oder Microsoft Azure Active Directory (Azure AD) Anmeldeinformationen des Mandantenadministrators. Im Abschnitt zu jedem Problem wird erläutert, ob eine bestimmte Rolle oder Anmeldeinformationen erforderlich sind.

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Aktivieren und Anzeigen des Plug-In-Überwachungsprotokolls in Dataverse, um Fehlerdetails anzuzeigen

**Erforderliche Rolle zum Aktivieren des Ablaufverfolgungsprotokolls und zum Anzeigen von Fehlern:** System Administrator

Um die Nachverfolgung einzuschalten, führen Sie diese Schritte aus.

1. Melden Sie sich bei der Kundenbindungs-App an, öffnen Sie die Seite **Einstellungen** und dann unter **System**, wählen Sie **Verwaltung**.
2. Wählen Sie auf der Seite **Verwaltung** die Option **Systemeinstellungen** aus.
3. Auf der Registerkarte **Anpassung** wählen Sie in der Spalte **Plug-In und benutzerdefinierte Workflow-Aktivitätsverfolgung** **Alle** aus, um das Plug-Trace-Protokoll zu aktivieren. Wenn Sie Ablaufverfolgungsprotokolle nur protokollieren möchten, wenn Ausnahmen auftreten, können Sie stattdessen **Ausnahme** auswählen.


Um die Nachverfolgung anzuzeigen, führen Sie diese Schritte aus.

1. Melden Sie sich bei der Kundenbindungs-App an, öffnen Sie die Seite **Einstellungen** und dann unter **Anpassung**, wählen Sie **Plug-In-Ablaufverfolgungsprotokoll**.
2. Suchen Sie die Ablaufverfolgungsprotokolle, in denen die Spalte **Typname** auf **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin** festgelegt ist.
3. Doppelklicken Sie auf ein Element, um das vollständige Protokoll anzuzeigen, und klicken Sie dann auf das Inforegister **Ausführung** und üerrprüfen Sie den Text **Nachrichtenblock**.

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

### <a name="chrome"></a>Chrome

1. Drücken Sie in der geöffneten Registerkarte **F12** oder wählen Sie **Entwickler-Tools**, um die Entwickler-Tools zu öffnen.
2. Öffnen Sie die Registerkarte **Netzwerk** und geben Sie **integ** in das Filtertextfeld ein.
3. Führen Sie Ihr Szenario aus und beobachten Sie, wie die Anfragen protokolliert werden.
4. Klicken Sie mit der rechten Maustaste auf die Einträge und wählen Sie **Alle als HAR mit Inhalt speichern**.

### <a name="microsoft-edge"></a>Microsoft Edge

1. Drücken Sie in der geöffneten Registerkarte **F12** oder wählen Sie **Entwickler-Tools**, um die Entwickler-Tools zu öffnen.
2. Öffnen Sie die Registerkarte **Netzwerk**.
3. Führen Sie Ihr Szenario aus.
4. Wählen Sie **Speichern**, um die Ergebnisse als HAR zu exportieren.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
