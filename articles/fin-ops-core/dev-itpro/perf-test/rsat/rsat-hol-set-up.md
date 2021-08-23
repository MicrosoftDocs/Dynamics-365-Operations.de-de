---
title: Regression Suite Automation Tool-Tutorial einrichten und installieren
description: Dieses Thema enthält ein Lernprogramm, das zeigt, wie das Regression Suite Automation Tool (RSAT) eingerichtet wird.
author: robinarh
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761, NotInToc
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2019-05-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 9cab5d9c9daf80fe5d2a510d189e71993265aa278342d5a99666615303158f61
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742275"
---
# <a name="set-up-and-install-regression-suite-automation-tool-tutorial"></a>Regression Suite Automation Tool-Tutorial einrichten und installieren

Dieses Thema ist ein Tutorial, mit dem Sie RSAT sowie die Tools einrichten und verwenden können, die der Verwendung von RSAT zugeordnet werden.

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> Verwenden Sie das Internet-Browsertool, um die Seite in PDF-Format herunterzuladen und zu speichern.

## <a name="key-concepts"></a>Schlüsselkonzepte

- Verstehen Sie die Installation und die vorausgesetzte Einrichtung, die für die verschiedenen Anwendungen erforderlich sind, die das Regression Suite Automation Tool (RSAT) unterstützen.
- Verstehen Sie, wie die Aufgabenaufzeichnungsfunktion in Verbindung mit Microsoft Dynamics Lifecycle Services (LCS) und Microsoft Azure DevOps Sie Testfälle erstellen, konfigurieren, ausführen, untersuchen und melden lässt.
- Ermöglichen Sie es funktionalen Benutzern, mit der Aufgabenaufzeichnung Geschäftsaufgaben aufzuzeichnen, und die Aufgabenaufzeichnung in eine Suite automatisierter Tests zu konvertieren, ohne Quellcode zu schreiben.

## <a name="before-you-begin"></a>Bevor Sie beginnen

### <a name="prerequisites"></a>Voraussetzungen

- Eine Umgebung, die Microsoft Dynamics 365 for Finance and Operations Version 10.0 (April 2019 ) oder höher ausführt ist für dieses Lernprogramm erforderlich. Für Kunden, die Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3 verwenden, wird auch Plattform-Update 20 (PU20) oder später unterstützt.
- Der Benutzer muss über Administratorrechte für die Umgebung verfügen.
- Sie müssen Zugriff auf den Debitorenmandant LCS und Azure DevOps (zuvor Microsoft Visual Studio Team- Services\[VSTS\]) haben.
- Der Benutzer, der Testsuites erstellt und verwaltet muss über eine Azure DevOps Test Plans oder Test Manager-Lizenz verfügen. Die folgenden Lizenzen geben ebenfalls Zugriff auf Test Plans:
    - Visual Studio Enterprise Lizenz
    - Visual Studio Test Professional-Lizenz
    - MSDN Platforms-Abonnentenlizenz
- RSAT muss Zugriff auf die Testumgebung über einen Webbrowser haben.
- Um Testparameter zu generieren und zu bearbeiten muss Microsoft Excel installiert sein.

## <a name="configure-azure-devops"></a>Azure DevOps konfigurieren

### <a name="user-eligibility"></a>Benutzerberechtigung

Überprüfen Sie, ob der Benutzer in Azure DevOps erstellt ist und über eine Abonnementstufe verfügt, die Zugriff auf Azure Test Plans bietet. Eine Azure DevOps Test Plan Lizenz ist nur erforderlich, wenn der Benutzer Testfälle erstellt und verwaltet (das heißt, nicht alle RSAT-Benutzer benötigen eine Lizenz). Informationen zur Lizenzanforderungen finden Sie unter [Lizenzanforderungen](/azure/devops/test/manual-test-permissions#license-requirements).

### <a name="create-a-new-azure-devops-project"></a>Erstellen eines neuen Azure DevOps-Projekts

RSAT verwendet Azure Devops für Testfall- und Testsuiteverwaltungs, -berichterstellung und die Untersuchung von Testlaufergebnissen.

> [!NOTE]
> Sie können ein vorhandenes Azure DevOps-Projekt verwenden. Wenn Ihr vorhandenes Azure DevOps-Projekt allerdings so eingerichtet ist, dass es über eine benutzerdefinierte Vorlage verfügt, erhalten Sie einen „VSTS-Synchronisierungsfehler“-Fehler, wenn Sie Testfälle vom Geschäftsprozessmodellierer (BPM) zu Azure DevOps synchronisieren (Informationen dazu finden Sie im Abschnitt [Testen der Synchronisierung von BPM zu Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops).) Wenn die folgenden bewährten Methoden für die benutzerdefinierte Vorlage befolgt wurden, können Sie die Testfälle zu Azure DevOps synchronisieren. (Diese bewährten Methoden werden in der Fehlermeldung aufgeführt).

- Löschen Sie keine Arbeitsaufgabentypen oder integrierten Felder.
- Löschen Sie keinen Status eines Arbeitsaufgabentyps.
- Fügen Sie keine erforderlichen Arbeitsaufgabentypen hinzu.

![Fehlermeldung mit einer Liste der bewährten Methoden.](./media/setup_rsa_tool_02.png)

Andernfalls wird für dieses Lernprogramm empfohlen, dass Sie ein neues Azure DevOps-Projekt erstellen. Weitere Informationen finden Sie unter [Probleme bei der Synchronisierung zu BPM mithilfe einer benutzerdefinierten Azure DevOps (VSTS) Prozessvorlage](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).

1. Öffnen Sie die Azure DevOps-URL (`https://dev.azure.com/<Azure DevOps Name>`).
2. Wählen Sie in der rechten oberen Ecke der Azure DevOps-Seite **Projekt erstellen** aus.

    ![Schaltfläche „Projekt erstellen“.](./media/setup_rsa_tool_03.png)

3. Füllen Sie die folgenden Felder aus, und wählen Sie dann **Erstellen** aus:

    - **Projektbezeichnung**
    - **Versionskontrolle** – Wählen Sie **Team Foundation-Versionskontrolle** aus. Beachten Sie, dass die Standardoption **Git** nicht unterstützt wird.
    - **Arbeitsaufgabenprozess**

    ![Erstellen eines neuen Projektdialogfelds.](./media/setup_rsa_tool_04.png)

### <a name="create-a-personal-access-token"></a>Erstellen eines persönlichen Zugangstokens

In diesem Lernprogramm verwenden Sie den LCS-Geschäftsprozessmodellierer (BPM), um eine Testfallbibliothek zu erstellen und Ihre Testfälle mit Azure DevOps zu synchronisieren. Sie benötigen einen persönlichen Zugriffstoken, um BPM mit Azure DevOps zu synchronisieren.

1. Wählen Sie das Profilsymbol in der rechten oberen Ecke der Seite für Ihr Azure DevOps-Projekt aus, und wählen Sie dann **Sicherheit** aus.

    ![Sicherheitsbefehl.](./media/setup_rsa_tool_05.png)

2. Im linken Bereich unter **Sicherheit** wählen Sie **Persönliches Zugriffstoken** aus. Wählen Sie dann **Neues Token** aus.

    ![Schaltfläche „Neues Token“ auf der Registerkarte „Persönliches Zugriffstoken“ in den Benutzereinstellungen.](./media/setup_rsa_tool_06.png)

3. Füllen Sie die folgenden Felder aus, und wählen Sie dann **Erstellen** aus:

    - **Name**
    - **Ablauf (UTC)** – Wählen Sie **Benutzerdefiniert** aus und verwenden Sie dann die Datumsauswahl, um das letzte verfügbare Datum auszuwählen.
    - **Bereiche** – Wählen Sie die Option **Vollzugriff** aus.

    ![Dialogfeld „Neues persönliches Zugriffstoken erstellen“.](./media/setup_rsa_tool_07.png)

    > [!NOTE]
    > Notieren Sie das persönliche Zugriffstoken, das erstellt wird. Sie benötigen es später, wenn Sie die RSAT-Konfiguration einrichten.

    ![Persönliches Zugriffstoken.](./media/setup_rsa_tool_08.png)

## <a name="configure-the-lcs-project"></a>Konfigurieren des LCS-Projekts

Sie benötigen ein Lifecycle Services (LCS)-Projekt für Ihre Mastertestbibliothek. Der LCS-Geschäftsprozessmodellierer (BPM) wird als Master-Bibliothek für Ihre Testfälle verwendet. BPM wird verwendet, um Testbibliotheken in LCS-Projekten zu verwalten und zu verteilen. Beispielsweise veröffentlicht ein Microsoft-Partner oder ein unabhängiger Softwareanbieter (ISV), der Testbibliotheken erstellt, Testfälle in Form von BPM-Bibliotheken. In BPM werden Testfälle nach Geschäftsprozess sortiert. BPM definiert die Ausführungsreihenfolge der die Häufigkeit des Testerfolgs nicht. Diese Details werden in Azure DevOps verwaltet, wie später in diesem Thema beschrieben.  

Für das LCS-Projekt können Sie eine vorhandene Benutzerimplementierung oder ein Partnerprojekt verwenden.

### <a name="update-the-lcs-language"></a>Aktualisieren der LCS-Sprache

> [!NOTE]
> Damit die Benutzeroberfläche (UI) die Geschäftsprozesse korrekt anzeigt, muss die bevorzugte Sprache von LCS auf **Englisch (USA)** festgelegt werden.

1. Gehen Sie zum LCS-Implementierungsprojekt.
2. Wählen Sie die Schaltfläche **Einstellungen** (das Rad-Symbol) in der rechten oberen Ecke der Seite aus, und wählen Sie dann **Spracheinstellungen**.

    ![Aktualisieren der Spracheinstellung.](./media/setup_rsa_tool_09.png)

3. Im Feld **Bevorzugte Sprache** wählen Sie **Englisch (USA)** und **Speichern** aus.

    ![Registerkarte „Spracheneinstellung“ in den Benutzereinstellungen.](./media/setup_rsa_tool_10.png)

### <a name="configure-lcs-to-connect-to-the-azure-devops-project"></a>Konfigurieren von LCS, um eine Verbindung mit dem Azure DevOps-Projekt herzustellen

Wenn Sie zuvor ein neues Azure DevOps-Projekt erstellt haben, konfigurieren Sie das LCS-Projekt, um eine Verbindung damit herzustellen. Andernfalls wenn Ihr LCS-Projekt bereits mit Ihrem Azure DevOps-Projekt verbunden ist, können Sie mit dem nächsten Abschnitt fortfahren.

1. Gehen Sie zum LCS-Implementierungsprojekt.
2. Aktivieren Sie die Schaltfläche **Menü**, und wählen Sie dann **Projekteinstellungen** aus.

    ![Befehl „Projekteinstellungen“.](./media/setup_rsa_tool_11.png)

3. Wählen Sie im linken Bereich **Visual Studio Team Services** aus und wählen Sie dann **Einstellungen Visual Studio Team Services** aus.

    ![Registerkarte „Visual Studio Team Services“ in den Projekteinstellungen.](./media/setup_rsa_tool_12.png)

4. Geben Sie im Feld **Azure DevOps-Website-URL** die URL der Azure DevOps-Website ein. Wählen Sie im Feld **Persönliches Zugriffstoken** das persönliche Zugriffstoken aus, das zuvor erstellt wurde.

    > [!NOTE]
    > Obwohl VSTS nun als Azure DevOps bezeichnet wird, verwenden Sie die alte URL, um LCS mit Ihrem Azure DevOps-Projekt zu verbinden. Beispielsweise lautet die Azure DevOps-URL, die in diesem Lernprogramm verwendet wird `https://dev.azure.com/D365FOFastTrack/`. In der folgenden Abbildung wird sie allerdings als `https://D365FOFastTrack.visualstudio.com/` eingegeben.

    ![Schritt 1 in „Einrichten von Visual Studio Team Services“.](./media/setup_rsa_tool_13.png)

5. Wählen Sie **Fortsetzen** aus.
6. Wählen Sie im Feld **Visual Studio Team Services-Projekt** das VSTS-Projekt auf der ausgewählten Website aus, die mit dem LCS-Projekt verknüpft werden soll. Das Feld **Vorlage verarbeiten** wird standardmäßig auf **Agile** festgelegt. Für eine benutzerdefinierte Vorlage überprüfen Sie den Leitfaden zu bewährten Methoden im Abschnitt [Neues Azure DevOps-Projekt erstellen](#create-a-new-azure-devops-project). Wählen Sie dann **Fortsetzen** aus.

    ![Schritt 2 in „Einrichten von Visual Studio Team Services“.](./media/setup_rsa_tool_14.png)

7. Überprüfen Sie die Einstellungen, und wählen Sie dann **Speichern** aus.

    ![Schritt 3 in „Einrichten von Visual Studio Team Services“.](./media/setup_rsa_tool_15.png)

8. Wählen Sie **Autorisieren** aus, um LCS zu autorisieren, um auf die konfigurierten Azure DevOps-Website in Ihrem Auftrag zuzugreifen und Funktionen zu aktivieren, die mit VSTS integrieren.

    ![Schaltfläche „Autorisieren“.](./media/setup_rsa_tool_16.png)

9. Ein Nachrichtenfeld mit folgender Meldung wird angezeigt: „Sie werden auf eine externe Website weitergeleitet, um LCS zu autorisieren, und in Ihrem Namen eine Verbindung mit Visual Studio-Team Services herzustellen. Fortfahren?“ Wählen Sie **Ja** aus.

    ![Meldungsfeld.](./media/setup_rsa_tool_17.png)

10. Wählen Sie **Akzeptieren** aus.

    ![Autorisieren des Zugriffs.](./media/setup_rsa_tool_18.png)

11. Wenn Sie als Benutzer berechtigt sind, sollte Sie die Benutzeroberfläche zur LCS-Projekteinstellungsseite zurückbringen.

    ![Autorisierter Benutzer.](./media/setup_rsa_tool_19.png)

### <a name="create-a-new-bpm-library"></a>Eine neue BPM-Bibliothek erstellen

1. Gehen Sie zum LCS-Implementierungsprojekt.
2. Aktivieren Sie die Schaltfläche **Menü**, und wählen Sie dann **Geschäftsprozessmodellierer** aus.

    ![Befehl „Geschäftsprozessmodellierer“.](./media/setup_rsa_tool_20.png)

3. Wählen Sie **Neue Bibliothek** aus.

    ![Schaltfläche „Neue Bibliothek“.](./media/setup_rsa_tool_21.png)

4. Geben Sie im Feld **Bibliotheksname** einen Namen ein, und wählen Sie dann **Erstellen** aus. Nennen Sie die BPM-Bibliothek in diesem Lernprogramm **RSAT**.

    ![Dialogfeld „Neue Bibliothek erstellen“.](./media/setup_rsa_tool_22.png)

5. Öffnen Sie die neue BPM-Bibliothek **RSAT**.
6. Wählen Sie den Prozess **Beispielkerngeschäftsprozess** und dann auf der rechten Seite die Option **Bearbeitungsmodus** aus.

    ![Schaltfläche „Bearbeitungsmodus“.](./media/setup_rsa_tool_23.png)

7. Ändern Sie den Wert der beiden Felder **Name** und **Beschreibung** zu **Ein Produkt erstellen**. Wählen Sie dann **Speichern** aus.

    ![Die Felder „Name“ und „Beschreibung“.](./media/setup_rsa_tool_24.png)

## <a name="environment"></a>Umgebung

### <a name="version-requirement"></a>Versionsanforderung

Eine Test- oder Sandboxumgebung, die Version 10 ausführt, ist erforderlich. Für Kunden, die Version 7.3 verwenden, wird auch Plattform-Update 20 oder später unterstützt.

> [!NOTE]
> RSAT muss Zugriff auf Ihre Testumgebung über einen Webbrowser haben.

### <a name="user-criteria"></a>Benutzerkriterien

Der Benutzer muss über Administratorrechte für diese Umgebung verfügen.

### <a name="set-up-help-settings-to-connect-with-lcs"></a>Richten Sie Hilfeeinstellungen ein, um eine Verbindung mit LCS herzustellen

Dieser Schritt ist erforderlich, um eine Verbindung mit LCS herzustellen, damit die Aufgabenaufzeichnungen über den Client in der entsprechenden BPM-Bibliothek in LCS gespeichert werden können.

1. Öffnen Sie den Client.
2. Gehen Sie zu **Systemadministration \> Einrichten \> Systemparameter**.
3. Wählen Sie auf der Registerkarte **Hilfe** im Feld **Lifecycle Services-Hilfekonfiguration** das betreffende LCS-Projekt (**RSAT** für dieses Lernprogramm) aus.

    ![Feld „Lifecycle Services-Hilfekonfiguration“ auf der Registerkarte „Hilfe“.](./media/setup_rsa_tool_25.png)

    BPM-Bibliotheken werden im entsprechenden LCS-Projekt ausgefüllt.

4. Wählen Sie **Speichern**.
5. Möglicherweise müssen Sie den Browser aktualisieren, um den aktualisierten Hilfeinhalt anzuzeigen.

    ![Benachrichtigung zum Aktualisieren des Browsers.](./media/setup_rsa_tool_26.png)

## <a name="task-recordings"></a>Aufgabenaufzeichnung

> [!NOTE]
> Stellen Sie sicher dass alle Aufgabenaufzeichnungen im Hauptdashboard starten. Halten Sie Einzelaufzeichnungen kurz und konzentrieren Sie sich auf eine Geschäftsaufgabe, wie die Erstellung eines Auftrags.

### <a name="create-a-task-recording-and-save-it-to-the-bpm-library"></a>Eine Aufgabenaufzeichnung erstellen und in der BPM-Bibliothek speichern

Erstellen Sie eine entsprechende Aufgabenaufzeichnung, die Sie dem einfachen Geschäftsprozess anfügen können, der in der neuen BPM-Bibliothek erstellt wurde.

1. Öffnen Sie den Client.
2. Wählen Sie im Hauptdashboard die Schaltfläche **Einstellungen** (das Zahnradsymbol) aus, und wählen Sie dann **Aufgabenaufzeichnung** aus.

    ![Wählen Sie im Menü „Einstellungen“ die Option „Aufgabenaufzeichnung“ aus.](./media/setup_rsa_tool_27.png)

3. Wählen Sie **Aufzeichnung erstellen** aus.

    ![Schaltfläche „Aufzeichnung erstellen“.](./media/setup_rsa_tool_28.png)

4. Füllen Sie die Felder **Aufzeichnungsname** und **Aufzeichnungsbeschreibung** aus, und wählen Sie dann **Starten** aus.

    ![Felder „Aufzeichnungsname“ und „Aufzeichnungsbeschreibung“.](./media/setup_rsa_tool_29.png)

5. Erfassen Sie die Schritte zum Erstellen eines Produkts. Wenn Sie fertig sind, wählen Sie **Beenden** aus, um die Erfassung zu beenden.

    ![Schritte zum Erstellen eines Produkts.](./media/setup_rsa_tool_30.png)

6. Wählen Sie **In Lifecycle Services speichern** aus.

    ![Speichern Sie die Aufgabenaufzeichnung in Lifecycle Services.](./media/setup_rsa_tool_31.png)

    Bibliotheksinformationen werden aus LCS geladen.

    ![Laden von Bibliotheksinformationen.](./media/setup_rsa_tool_32.png)

7. Wählen Sie die BPM-Bibliothek aus, die der Aufgabenaufzeichnung zugeordnet werden soll. In diesem Lernprogramm wählen Sie die **RSAT**-BPM-Bibliothek aus, die zuvor erstellt wurde, und den Geschäftsprozess **Ein Produkt erstellen** darunter. Wählen Sie dann **OK** aus.

    ![Die Aufgabenaufzeichnung einer BPM-Bibliothek und einem Geschäftsprozess zuordnen.](./media/setup_rsa_tool_33.png)

    Die Meldung „Das Speichern in Lifecycle Services war erfolgreich“ erscheint.

    ![Meldung einer erfolgreichen Speicherung in LCS.](./media/setup_rsa_tool_34.png)

8. Wenn Sie die Aufgabenaufzeichnung lokal speichern und dann durch LCS zu BPM hochladen möchten, führen Sie die folgenden Schritte aus:

    1. Nachdem die Aufzeichnung abgeschlossen ist, wählen Sie **Auf diesem PC speichern** aus.

        ![Auf diesem PC speichern.](./media/setup_rsa_tool_35.png)

    2. In der Benachrichtigungsleiste des Browsers wählen Sie **Speichern** oder **Speichern unter** aus, um die Datei auf dem lokalen Computer zu speichern.

        ![Benachrichtigungsleiste.](./media/setup_rsa_tool_36.png)

    3. Wechseln Sie zur BPM-Bibliothek **RSAT**, und wählen Sie den Geschäftsprozess aus, für den die Aufgabenaufzeichnung gespeichert wird.
    4. Auf der Registerkarte **Überblick** wählen Sie **Hochladen** aus.

        ![Schaltfläche „Hochladen“.](./media/setup_rsa_tool_37.png)

    5. Wählen Sie **Durchsuchen** und dann die .axtr-Datei aus, die Sie zuvor gespeichert haben. Wählen Sie dann **Hochladen** aus.

        ![Auswählen der .axtr-Datei zum Hochladen.](./media/setup_rsa_tool_38.png)

### <a name="test-the-synchronization-from-bpm-to-azure-devops"></a>Testen der Synchronisierung von BPM zu Azure DevOps

Da jetzt eine Aufgabenaufzeichnung dem Geschäftsprozess zugeordnet ist, müssen Sie überprüfen, dass der Geschäftsprozess und die zugehörige Aufgabenaufzeichnung mithilfe der in VSTS-Synchronisierungsfunktion in LCS (je) mit Azure DevOps als eine Funktion und ein Testfall synchronisiert werden kann.

> [!NOTE]
> Der entsprechende Arbeitsaufgabentyp, der in Azure DevOps erstellt wird, variiert abhängig von der Prozessvorlage, die Sie ausgewählt haben, als Sie das LCS-Projekt mit Azure DevOps konfiguriert haben, wie im Abschnitt [Erstellen eines neuen Azure DevOps-Projekt](#create-a-new-azure-devops-project) beschrieben.

1. Wechseln Sie zur BPM-Bibliothek und öffnen Sie die **RSAT**-Bibliothek, die Sie zuvor erstellt haben.
2. Aktivieren Sie die Ellipsen-Schaltfläche (**…**), und wählen Sie **VSTS-Synchronisierung** aus.

    ![Befehl „VSTS-Synchronisierung“ im Ellipsen-Menü.](./media/setup_rsa_tool_39.png)

    Nachdem die VSTS-Synchronisierung abgeschlossen ist, wird auf der linken Seite die Registerkarte **Anforderungen** angezeigt, die die entsprechende Azure DevOps-Arbeitsaufgabe enthält.

    > [!NOTE]
    > Die Arbeitsaufgabe, die in Azure DevOps erstellt wird, weist den BPM-Bibliotheksnamen als Titelpräfix vor.

    ![Registerkarte „Anforderungen“.](./media/setup_rsa_tool_40.png)

3. Aktualisieren Sie die Seite.
4. Wählen Sie die Elipsen-Schaltfläche (**...**) aus. Es wird die Zusatzfunktion **Testfälle synchronisieren** angezeigt. Wählen Sie diese Option aus.

    ![Befehl „Testfälle synchronisieren“ im Ellipsen-Menü.](./media/setup_rsa_tool_41.png)

    > [!NOTE]
    > Wenn die Option **Testfälle synchronisieren** nicht verfügbar ist, nachdem Sie die Seite aktualisieren, wechseln zur Hauptseite für BPM, und wählen Sie **Testfälle synchronisieren** für die gesamte Bibliothek aus. Hierdurch erzwingen Sie eine Synchronisierung für die gesamte Bibliothek.
    >
    > ![Auswählen der Synchronisierung von Testfällen für die gesamte Bibliothek.](./media/setup_rsa_tool_42.png)

    Nachdem die Synchronisierung der Testfälle abgeschlossen ist, wird auf der Registerkarte **Anforderungen** ein neuer Testfall erstellt.

    ![Neuer Testfall auf der Registerkarte „Anforderungen“.](./media/setup_rsa_tool_43.png)

5. Wechseln Sie zu Ihrem Azure DevOps-Projekt, und wählen Sie **Übersichten \> Arbeitsaufgaben** aus.

    ![Befehl „Arbeitsaufgaben“ unter „Übersichten“.](./media/setup_rsa_tool_44.png)

6. Überprüfen Sie, ob die Arbeitsaufgabe und der Testfall, die Sie durch BPM-Synchronisierung erstellt haben, vorhanden sind.

    ![Arbeitsaufgabe und Testfall.](./media/setup_rsa_tool_45.png)

## <a name="install-and-configure-rsat"></a>RSAT installieren und konfigurieren

RSAT kann auf einem beliebigen Computer installiert werden, der Windows 10 ausführt und der eine Verbindung mit der Umgebung über einen Webbrowser herstellen kann (Internet Explorer oder Google Chrome).

> [!NOTE]
> Bevor Sie eine neue Version des Tools installieren, wird empfohlen, dass Sie die vorherige Version deinstallieren.

### <a name="install-an-authentication-certificate"></a>Installieren eines Authentifizierungszertifikats

Um die Authentifizierung zu aktivieren, müssen Sie ein Zertifikat auf dem gleichen Computer generieren und installieren, auf dem RSAT ausgeführt wird.

#### <a name="generate-a-certificate"></a>Generieren eines Zertifikats

1. Um eine Zertifikatsdatei zu generieren, öffnen Sie ein Microsoft Windows PowerShell-Fenster als Administrator, und führen Sie den folgenden Befehl aus.

    ```powershell
    $certificate = New-SelfSignedCertificate -dnsname 127.0.0.1 -CertStoreLocation cert:\LocalMachine\My -FriendlyName "D365 Automated testing certificate" -Provider "Microsoft Strong Cryptographic Provider"
    ```

2. Öffnen Sie den Zertifikatsmanager, indem Sie **certlm.msc** in das Dialogfeld **Ausführen** eingeben und bestätigen, dass das **D365 Automated-Testzertifikats** unter **Persönlich \> Zertifikate** erstellt wird.

    > [!NOTE]
    > Stellen Sie sicher, dass Sie **certlm.msc** und nicht **certmgr.msc** eingeben, da die Zertifikate auf dem lokalen Computer gespeichert werden.

    ![Zertifikat „Automatisiertes D365-Testzertifikat“.](./media/setup_rsa_tool_46.png)

3. Klicken Sie mit der rechten Maustaste auf das Zertifikat, und wählen Sie dann **Kopieren** aus.
4. Wechseln Sie zu **Vertrauenswürdige Stammzertifizierungsstellen \> Zertifikate**.

    ![Zertifikatsordner unter dem Ordner „Vertrauenswürdige Stammzertifizierungsstellen“.](./media/setup_rsa_tool_47.png)

5. Wählen Sie im Menü **Aktivität** **Einfügen** aus, um das Zertifikat in den Speicherort der **Vertrauenswürdigen Stammzertifizierungsstellen** zu kopieren.

    ![Befehl „Einfügen“ im Menü „Aktivität“.](./media/setup_rsa_tool_48.png)

6. Um die Fingerabdruck des installierten Zertifikats zu erhalten, aber ohne Leerzeichen und Sonderzeichen, öffnen Sie ein Windows PowerShell-Fenster als Administrator und führen die folgenden Befehle aus.

    ```powershell
    cd Cert:\LocalMachine\My

    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    > [!NOTE]
    > Speichern Sie den Fingerabdruck, da Sie ihn später benötigen, wenn Sie die .wif-Dateien für Application Object Server (AOS) aktualisieren und die RSAT-Konfiguration einrichten.

#### <a name="configure-the-aos-computer-to-trust-the-connection"></a>Konfigurieren des AOS-Computers, um der Verbindung zu vertrauen

> [!NOTE]
> Wenn die Umgebung eine Umgebung der Ebene 2+ ist, muss der Zertifikatsfingerabdruck in der wif.config-Datei für **alle** dAOS-Computer der Umgebung aktualisiert werden.

1. Stellen Sie eine Remote Desktop Protocol (RDP)-Verbindung mit dem AOS-Computer her. Anmeldungsdetails sind auf der Umgebungsdetailseite in LCS verfügbar.
2. Öffnen Sie Microsoft-Internetinformationsdienste (IIS) und navigieren Sie zu **AOSService** in der Website-Liste.

    ![AOSService in der Website-Liste.](./media/setup_rsa_tool_49.png)

3. Klicken Sie mit der rechten Maustaste auf **Erkunden**, um den Ordner **\<Drive\>: \\AosService\\Webroot** zu öffnen. Suchen Sie die Datei **wif.config**.

    ![Wif.config-Datei im Webroot-Ordner.](./media/setup_rsa_tool_50.png)

4. Aktualisieren Sie die Datei **wif.config**, indem Sie einen neuen Zertifikatseintrag für Ihr Zertifikat und den Behördennamen hinzufügen, wie im folgenden Beispiel dargestellt.

    ```Xml
    <issuerNameRegistry type="Microsoft.Dynamics.AX.Security.SharedUtility.AxIssuerNameRegistry,Microsoft.Dynamics.AX.Security.SharedUtility">
        <authority name="CN=127.0.0.1">
            <keys>
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
            </keys>
            <validIssuers>
                <add name="CN=127.0.0.1" />
            </validIssuers>
        </authority>
    ```

    > [!NOTE]
    > Wenn mehrere Benutzer dieselbe Anwendung verwenden, muss jeder Benutzer separate Fingerabdrücke generieren und jeder dieser Fingerabdrücke muss dem Abschnitt **\<keys\>** hinzugefügt werden.

5. Sind es mehrere AOS-Computer gibt, wiederholen Sie die Schritte 3 bis 4 für jeden weiteren Computer.

    > [!NOTE]
    > Im Gegensatz zu älteren Umgebung der Ebene 2 werden neue Umgebung der Ebene 2 mit zwei AOS-Instanzen bereitgestellt.

6. Führen Sie **iisreset** für alle AOS-Computer aus.

    > [!NOTE]
    > Wenn Sie nicht über Administratorrechte verfügen, um **iisreset** auf einem Computer der Ebene 1 auszuführen, wählen Sie auf der Umgebungsdetailseite in LCS „Verwalten > Dienste neustarten“ aus.

#### <a name="tier-2-environment"></a>Ebene 2+-Umgebung

Wenn eine Umgebung der Ebene 2+ (Standard-Akzeptanztestsandbox oder höher) verwendet wird, prüfen Sie die folgende Registrierungseinstellung auf dem Computer, auf dem RSAT eingerichtet ist, oder legen Sie die Einstellung dort fest. Dieser Schritt ist erforderlich, da er Sie dabei unterstützt, Authentifizierungs- oder RSAT-Verbindungsfehler zu vermeiden.

```PowerShell
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
}
```

### <a name="install-rsat"></a>Installieren von RSAT

1. Wechseln Sie zu <https://www.microsoft.com/download/details.aspx?id=57357> und wählen Sie **Download** aus.
2. Wählen Sie alle Dateien aus, und wählen Sie dann **Weiter** aus.

    ![Auswählen aller Dateien.](./media/setup_rsa_tool_51.png)

3. Doppelklicken Sie auf das .msi-Paket, um das Installationsprogramm auszuführen. Wenn die Installation abgeschlossen ist, wählen Sie **Fertig stellen** aus.

    ![RSAT-Installationsprogrammdatei.](./media/setup_rsa_tool_52.png)

### <a name="install-selenium-and-browser-drivers"></a>Einrichten von Selenium- und Browsertreibern

In den Vorgängerversionen von RSAT mussten Sie Selenium- und Browsertreiber einrichten. Sie müssen dieses Treiber nicht mehr installieren, da sie automatisch installiert werden.

1. Beim erstmaligen Öffnen von RSAT werden Sie aufgefordert, Selenium automatisch herunterzuladen und zu installieren. Weitere Informationen finden Sie im Abshnitt [RSAT konfigurieren](#configure-rsat).
2. Bevor Sie einen Testfall ausführen können, werden Sie aufgefordert, den Browsertreiber automatisch herunterzuladen und zu installieren, der dem Standardbrowser entspricht, der in der RSAT-Konfiguration aktiviert ist. Weitere Informationen finden Sie im Abschnitt [Testfälle laden und ausführen](#load-and-run-test-cases).

## <a name="get-started-with-rsat"></a>Erste Schritte mit RSAT

### <a name="create-a-test-plan-and-test-suites"></a>Einen Testplan und Testsuiten erstellen

1. Wechseln Sie zum Azure DevOps-Projekt, und wählen Sie **Testpläne** aus.

    ![Befehl „Testpläne“.](./media/setup_rsa_tool_53.png)

2. Wählen Sie **Neuer Testplan** aus.

    ![Schaltfläche „Neuer Testplan“.](./media/setup_rsa_tool_54.png)

3. Füllen Sie das Feld **Name** aus, und wählen Sie dann **Erstellen** aus. In diesem Lernprogramm geben Sie dem Testplan den Namen **RSAT-Testplan**.

    ![Dialogfeld „Neuer Testplan“.](./media/setup_rsa_tool_55.png)

4. Wählen Sie das Pluszeichen (**+**) aus, und wählen Sie dann **Statische Suite** aus, um eine statische Suite unterhalb des neuen Testplans zu erstellen. Nennen Sie die neue Testsuite **T01 – Fertigung auf Lager**

    > [!NOTE]
    > Sie können auch eine abfragebasierte Suite erstellen, wenn die neuen Testfälle von BPM automatisch in die RSAT-Testsuite gezogen werden sollen.

    ![Erstellen einer statischen Suite.](./media/setup_rsa_tool_56.png)

### <a name="attach-test-cases-to-test-suites"></a>Anfügen von Testfällen an Testsuiten

1. Wählen Sie rechts **Vorhandenes Element hinzufügen** aus, um vorhandene Testfälle der Testsuite hinzuzufügen.

    ![Schaltfläche „Vorhandenes Element hinzufügen“.](./media/setup_rsa_tool_57.png)

2. Auf der Seite **Testfälle der Suite hinzufügen** wählen Sie **Abfrage ausführen** aus, und dann wählen Sie den Testfall aus, der der Testsuite hinzugefügt werden soll. In diesem Lernprogramm wählen Sie den Testfall **Neues Produkt erstellen** aus. Wählen Sie dann in der unteren rechten Ecke der Seite **Testfälle hinzufügen** aus (diese Schaltfläche wird in der folgenden Abbildung nicht dargestellt).

    ![Schaltfläche „Abfrage ausführen“.](./media/setup_rsa_tool_58.png)

    Der Testfall wird der Testsuite **T01-Fertigung auf Lager** hinzugefügt.

    ![Testfall der Testsuite hinzugefügt.](./media/setup_rsa_tool_59.png)

### <a name="configure-rsat"></a>RSAT konfigurieren

1. RSAT öffnen

    ![RSAT-Symbol.](./media/setup_rsa_tool_60.png)

2. Andernfalls wird folgende Warnung angezeigt: „Regression Suite Automation Tool benötigt Selenium. Soll es jetzt automatisch heruntergeladen und installiert werden?“ Wählen Sie **Ja** aus.

    ![Warnmeldung, dass Regression Suite Automation Tool Selenium benötigt.](./media/setup_rsa_tool_61.png)

3. Wählen Sie die Schaltfläche **Einstellungen** (das Zahnradsymbol) in der oberen rechten Ecke aus, und füllen Sie dann im angezeigten Dialogfeld die folgenden Felder aus:

    - **Azure DevOps URL** – Geben Sie die URL Ihres Azure DevOps Projekts ein, wie `https://yourAzureDevOpsUrlHere.visualStudio.com`.
    - **Zugriffstoken** – Geben Sie das Zugriffstoken ein, mit dem das Tool eine Verbindung mit Azure DevOps herstellen kann. Verwenden Sie das persönliche Zugriffstoken, Sie zuvor in diesem Lernprogramm erstellt haben. Weitere Informationen finden Sie unter [Authentifizieren des Zugriffs mit persönlichen Zugriffstoken](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).
    - **Projektname** – Wählen Sie den Namen Ihres Azure DevOps-Projekts aus.
    - **Testplan** – Wählen Sie den Azure DevOps-Testplan aus, der die Testfälle enthält. Weitere Informationen finden Sie unter [Erstellen von Testplänen und Testsuiten](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan). Nachdem Sie einen Testplan ausgewählt haben, wählen Sie **Verbindung testen** aus, um die Verbindung mit Azure DevOps zu testen.
    - **Hostname** – Geben Sie den Hostnamen der Testumgebung ein, z. B. **\<myaos\>.cloudax.dynamics.com**. Schließen Sie kein **https://** oder **http://** Präfix ein.
    - **SOAP Hostname** – Geben Sie den SOAP-Hostnamen der Testumgebung ein. Normalerweise entspricht der SOAP-Hostname dem Hostnamen, hat aber ein **soap**-Suffix. Es folgt ein Beispiel: **\<myaos\>soap.cloudax.dynamics.com**. Schließen Sie kein **https://** oder **http://** Präfix ein.

        > [!NOTE]
        > Um den Hostnamen und den SOAP-Hostnamen zu finden, öffnen Sie den IIS-Manager, klicken Sie mit der rechten Maustaste auf **Websites \> AOSService**, und wählen Sie dann **Bindungen bearbeiten** aus. Die Werte in der Spalte **Hostname** geben Ihnen den Hostnamen und den SOAP-Hostnamen (der SOAP-Hostname hat das Suffix **soap** in der URL).

        ![Hostname und SOAP-Hostname in der Spalte „Hostname“.](./media/setup_rsa_tool_63.png)

    - **Benutzername des Administrators** – Geben Sie die E-Mail-Adresse des Administratorbenutzers in der Testumgebung ein.
    - **Fingerabdruck** – Geben Sie den Fingerabdruck für das Authentifizierungszertifikat ein, wie zuvor in diesem Lernprogramm beschrieben.
    - **Arbeitsverzeichnis** – Geben Sie den Speicherort des Ordners zum Speichern von Testautomatisierungsdateien wie Excel-Testdatendateien ein. Geben Sie beispielsweise **C:\\Temp\\RegressionTool** ein oder wählen Sie den Pfad aus.

        > [!NOTE]
        > Wenn der Name des Ordners Leerzeichen hat, schlägt die Ausführung fehl, da der Ordner nicht gefunden werden kann. Dieses Problem ist bekannt und sollte in der neuesten Version des Tools korrigiert werden.

    - **Standardbrowser** – Wählen Sie entweder **Internet Explorer** oder **Google Chrome** aus. Stellen Sie sicher, dass die entsprechenden Browsertreiber eingerichtet wurden.
    - **Testlauf-Timeout** – Geben Sie den Timeout-Zeitraum für Testläufe in Minuten an. Wenn der Timeout-Zeitraum vergeht, werden alle aktiven Fenster geschlossen und ausstehende Testfälle schlagen fehl.
    - **Testaktion-Timeout** – Dieses Feld steuert den Timeout-Zeitraum für Serveranforderungen der Finance and Operation-Umgebung in Minuten. Normalerweise sollte der Standardwert (2 Minuten) ausreichen. Bei langsameren Umgebungen können Sie den Wert ggf. erhöhen wollen, falls Fehler in Zusammenhang mit Timeouts auftreten.
    - **Unternehmensname** – Geben Sie den Unternehmensnamen zur Verwendung als Standardunternehmen ein, wenn Excel-Parameterdateien erstellt werden. Sie können das Unternehmen später ändern, indem Sie die Excel-Parameterdatei bearbeiten.

    ![Dialogfeld „Einstellungen“.](./media/setup_rsa_tool_62.png)

4. Wählen Sie **Übernehmen** aus, um die Einstellungen anzuwenden und zu speichern.

    Um Ihre aktuellen Einstellungen in einer Konfigurationsdatei auf dem Computer zu speichern, wählen Sie **Speichern unter** aus. Um Ihre aktuellen Einstellungen aus einer Konfigurationsdatei auf dem Computer wiederherzustellen, wählen Sie **Öffnen** aus.

5. Klicken Sie auf **Schließen**, um die Dialogfelder zu schließen.

### <a name="load-and-run-test-cases"></a>Laden und Ausführen von Testfällen

1. Wählen Sie **Laden** aus, um den Testplan **RSAT-Testplan** aus dem Azure DevOps-Projekt zu laden.

    ![Schaltfläche „Laden“.](./media/setup_rsa_tool_64.png)

2. Wählen Sie den Testfall **Neues Produkt erstellen** aus der Testsuite aus, und wählen Sie dann **Neu \> Testausführung und Parameterdateien generieren** aus.

    ![Befehl „Testausführung und Parameterdateien generieren“ im Menü „Neu“.](./media/setup_rsa_tool_65.png)

    Die Excel-Parameterdatei wird im lokalen Ordner erstellt, den Sie in der RSAT-Konfiguration angegeben haben (z. B. **C:\\Temp\\RegressionTool**).

    ![Excel-Parameterdatei erstellt.](./media/setup_rsa_tool_66.png)

3. Wenn Sie die Parameterdateien speichern möchten, wählen Sie **Hochladen** aus. Testautomatisierungsdateien aller ausgewählten Testfälle werden für künftige Verwendung in Azure DevOps hochgeladen. (Diese Dateien enthalten Excel-Testparameterdateien.)

    Auf diese Weise können Sie **Laden** auswählen, um die Parameterdateien (und die Automatisierungsdateien) aus dem Testfall direkt aus Azure DevOps zu laden. Sie müssen die Parameterdateien nicht erneut generieren. Dieser Ansatz wird später wichtig, wenn Sie die Änderungen in der Parameterdatei beibehalten möchten und diese nicht überschrieben werden sollen.

4. Um sicherzustellen, dass die Automatisierungsdateien und die Parameterdateien in Azure DevOps gespeichert werden, wechseln Sie zum Azure DevOps- Projekt, wählen Sie **Üersichten \> Arbeitsaufgaben** aus und wählen Sie den Testfall **Neues Produkt erstellen** aus. Auf der Registerkarte **Anhänge** können Sie vier Dateien sehen:

    - **.cs** – C-\#-Automatisierungsdatei
    - **.dll** – als Assembly kompilierte Automatisierungsdatei
    - **.xlsx** – Excel-Parameterdatei
    - **.xml** – Aufzeichnungsdatei

    ![Dateien auf der Registerkarte „Anhänge“.](./media/setup_rsa_tool_67.png)

5. Wählen Sie den Testfall aus, der ausgeführt werden soll, und wählen Sie dann **Ausführen** aus.

    > [!NOTE]
    > Bevor Sie Testfälle ausführen, wenn Sie Internet Explorer als Browser verwenden, stellen Sie sicher, dass die Desktop-Auflösung unter **Windows-Anzeigeeinstellungen \> Maßstab und Layout** auf **100 %** festgelegt ist. Wenn Sie diese Einstellungen auf einem virtuellen Computer (VM) nicht ändern können, ändern Sie ihn auf dem Client (Laptop), von dem Sie auf die WM zuzugreifen versuchen. Die Auflösungseinstellungen werden dann von den VM-Anzeigeeinstellungen geerbt.

    ![Desktopauflösung auf 100 % eingestellt.](./media/setup_rsa_tool_68.png)

6. Wenn die Browsertreiber nicht im System installiert sind, erhalten Sie folgende Warnmeldung: „Dieser Vorgang erfordert den Treiber für \<browser name\>. Möchten Sie ihn jetzt automatisch herunterladen und installieren?“ Wählen Sie **Ja** aus.

    ![Warnmeldung für Internet Explorer.](./media/setup_rsa_tool_69.png)

    ![Warnmeldung für Chrome.](./media/setup_rsa_tool_70.png)

    > [!NOTE]
    > Wenn Sie Chrome als Browser verwenden und eine Fehlermeldung erhalten, die angibt, dass die Sitzung nicht erstellt wurde, da die Chrome-Version falsch ist, laden Sie den letzten Chrome-Treiber von <http://chromedriver.chromium.org/downloads> in den Ordner **C:\\Programme (x86)\\Regression Suite Automation Tool\\Allgemein\\Extern\\Selenium** herunter.

    ![Fehlermeldung für Chrome.](./media/setup_rsa_tool_71.png)

    Der Testfall wird ausgeführt und das Feld **Ergebnis** wird aktualisiert.

    ![Feld „Ergebnis“ wurde aktualisiert.](./media/setup_rsa_tool_72.png)

    Wenn Sie diesem Lernprogramm folgen, schlägt der **Neues Produkt erstellen**-Testfall fehlt, da die Aufgabenaufzeichnung für das Erstellen eines Produkts den Produktname als hartcodierten Wert gespeichert hat. Wenn Sie den gleichen Testfall wiederholen, sollten Sie eine Fehlermeldung erhalten, da das Produkt bereits vorhanden ist.

    ![Auf „Fehlgeschlagen“ festgelegtes Ergebnisfeld.](./media/setup_rsa_tool_72.png)

### <a name="view-the-test-results"></a>Anzeigen des Testergebnisses

1. Doppelklicken Sie auf den fehlgeschlagenen Testfall.

    Es wird eine Fehlermeldung angezeigt.

    ![Fehlermeldung.](./media/setup_rsa_tool_73.png)

2. Wählen Sie **Detail**, um die gesamten Fehlermeldung anzuzeigen.

    ![Die ganze Fehlermeldung.](./media/setup_rsa_tool_74.png)

3. Um eine ausführliche Version eine Fehlermeldung in Azure DevOps anzuzeigen, wählen Sie **In Azure DevOps öffnen** aus. In Azure DevOps können Sie den Status des Testfalls und die detaillierte Fehlermeldung anzeigen.

    ![Detaillierte Fehlermeldung in Azure DevOps.](./media/setup_rsa_tool_75.png)

4. Um die Testergebnisse direkt im Azure DevOps-Projekt anzuzeigen, navigieren Sie zu **Testpläne \> Testpläne \> Ausführungen**. Doppelklicken Sie auf den Test, für den weitere Details angezeigt werden sollen.

    ![Liste der Testläufe in Azure DevOps.](./media/setup_rsa_tool_76.png)

5. Die Registerkarte **Ausführungszusammenfassung** gibt an, dass der Testfall fehlgeschlagen ist, aber die tatsächliche Fehlermeldung wird nicht bereitgestellt. Um die detaillierten Fehlermeldung anzuzeigen, wählen Sie die Registerkarte **Testergebnisse** aus.

    ![Registerkarte „Ausführungszusammenfassung“.](./media/setup_rsa_tool_77.png)

    Die Registerkarte **Testergebnisse** enthält die Testfallinformationen, zusammen mit dem Ergebnis und die Fehlermeldung.

    ![Registerkarte „Testergebnis“.](./media/setup_rsa_tool_78.png)

6. Doppelklicken Sie auf den entsprechenden Datensatz, um die detaillierte Fehlermeldung anzuzeigen.

    ![Detaillierte Fehlermeldung.](./media/setup_rsa_tool_79.png)

    > [!NOTE]
    > Alle Fehlermeldungen sind auch lokal in **C:\\Benutzer\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt** verfügbar.

7. Sie können die Testlaufergebnisse auch von der Testplanebene exportieren, indem Sie **Exportieren** auswählen.

    ![Exportieren eines Testplans.](./media/setup_rsa_tool_80.png)

### <a name="modify-the-excel-parameter-file"></a>Ändern Sie die Excel-Parameterdatei.

1. RSAT öffnen
2. Wählen Sie den Testfall aus, und wählen Sie dann **Bearbeiten** aus, um die Excel-Parameterdatei zu öffnen.

    Beachten Sie auf dem **EcoResProductCreate**-Arbeitsblatt, dass der Wert des Feldes **Produktnummer** fest hartcodiert ist. Sie müssen dieses Feld auf eine neue Produktnummer aktualisieren, bevor Sie den Testfall erneut ausführen.

3. Um eine eindeutige Produktnummer für jeden Lauf zu generieren, ohne die Excel-Parameterdatei jedes Mal erneut zu öffnen und die Produktnummer manuell zu aktualisieren, verwenden Sie die folgende Excel-Formel.

    ```vba
    ="RSAT_"&TEXT(NOW(),"yyymmddhhmm")
    ```

    > [!NOTE]
    > Zusätzlich zur Registerkarte **Allgemein** enthält die Excel-Parameterdatei eine Datenregisterkarte für jede Formularseite, die der Testfall besucht.

    ![Produktnummernfeld.](./media/setup_rsa_tool_81.png)

4. Wählen Sie **Speichern** aus und schließen die Excel-Arbeitsmappe.
5. Wählen Sie **Hochladen** aus, um die Excel-Parameterdatei in Azure DevOps zu speichern.

    ![Meldung für erfolgreichen Upload.](./media/setup_rsa_tool_82.png)

    > [!NOTE]
    > Um Testfälle in einem bestimmten Benutzerkontext auszuführen, geben Sie die E-Mail-Kennung des Benutzers im Feld **Testbenutzer** auf der Registerkarte **Allgemein** der Excel-Parameterdatei ein. In der neuesten Version von RSAT wurde das Layout der Felder in der Excel-Parameterdatei aktualisiert, das Konzept bleibt jedoch gleich.
    >
    > ![Feld „Testbenutzer“.](./media/setup_rsa_tool_83.png)

### <a name="validate-the-results"></a>Das Ergebnis validieren

- Wählen Sie **Ausführen** aus, um den Testfall erneut auszuführen, und überprüfen Sie, ob der Testfall erfolgreich war. Sie können die Testergebnisse wie im Abschnitt [Anzeigen der Testergebnisse](#view-the-test-results) beschrieben anzeigen.

    ![Auf „Erfolgreich“ festgelegtes Ergebnisfeld.](./media/setup_rsa_tool_84.png)

### <a name="chaining-of-test-cases"></a>Verketten von Testfällen

Eine wichtige Funktion von RSAT ist das Verketten von Testfällen (das heißt, die Fähigkeit eines Tests, Werte an andere Tests zu übergeben). Testfälle werden entsprechend ihrer im Azure DevOps Testplan definierten Reihenfolge ausgeführt. (Diese Reihenfolge kann im Testtool auch aktualisiert werden.) Wenn Sie also Variablen von einem Testfall an den anderen übergeben möchten, ist es sehr wichtig, dass die Tests in der richtigen Reihenfolge sind.

In diesem Abschnitt erstellen Sie eine gespeicherte Variable im ersten Testfall. Sie erstellen einen zweiten Testfall und übergeben die gespeicherte Variable vom ersten Testfall an den zweiten Testfall. Sie führen die Testfälle dann als verketteten Testfall in RSAT aus.

#### <a name="modify-an-existing-task-recording-to-create-a-saved-variable"></a>Ändern einer vorhandenen Aufgabenaufzeichnung, um eine gespeicherte Variablen zu erstellen

1. Öffnen Sie den Client.
2. Wählen Sie die Schaltfläche **Einstellungen** (das Zahnradsymbol) aus, und wählen Sie dann **Aufgabenaufzeichnung** aus.
3. Wählen Sie **Aufzeichnung bearbeiten** aus.

    ![Schaltfläche „Aufzeichnung bearbeiten“.](./media/setup_rsa_tool_85.png)

4. Wählen Sie **In Lifecycle Services öffnen** aus.

    ![Schaltfläche „In Lifecycle Services öffnen“.](./media/setup_rsa_tool_86.png)

5. Wählen Sie **Lifecycle Services-Bibliothek auswählen** aus.

    ![Schaltfläche „Lifecycle Services-Bibliothek auswählen“.](./media/setup_rsa_tool_87.png)

    BPM-Bibliotheken werden aus LCS geladen.

    ![Laden von BPM-Bibliotheken.](./media/setup_rsa_tool_88.png)

6. Nachdem die BPM-Bibliotheken aus LCS geladen wurden, wählen Sie die BPM-Bibliothek **RSAT** und den Geschäftsprozess **Neues Produkt erstellen** aus, dem die Aufgabenaufzeichnung zugeordnet wurde. Wählen Sie dann **OK** aus.

    ![Auswählen einer BPM-Bibliothek und eines Geschäftsprozesses.](./media/setup_rsa_tool_89.png)

7. Der Name der entsprechenden Aufgabenaufzeichnung wird im Feld **Aufzeichnungsname** eingegeben. Wählen Sie **Starten** aus.

    ![Name der Aufgabenaufzeichnung im Feld „Aufzeichnungsname“.](./media/setup_rsa_tool_90.png)

8. Navigieren Sie zu **Produktinformationsverwaltung \> Produkte**, und wählen Sie **Neu** aus, um die Seite zu öffnen, in der die ursprüngliche Aufgabenaufzeichnung **Ein Produkt erstellen** aufgezeichnet wurde.
9. Wählen Sie **Schritt einfügen** aus.

    > [!NOTE]
    > Der neue Schritt wird **nach** dem Schritt eingefügtes, den Sie im Bereich ausgewählt haben.

    ![Schaltfläche „Schritt einfügen“.](./media/setup_rsa_tool_91.png)

10. Klicken Sie mit der rechten Maustaste auf das Feld **Produktnummer**, und wählen Sie dann **Aufgabenaufzeichnung \> Kopieren** aus.

    ![Kopieren-Befehl.](./media/setup_rsa_tool_92.png)

11. Ein neuer Schritt wird dem Bereich hinzugefügt. Notieren Sie sich den Wert im Feld **Produktnummer**, da Sie ihn zu einem späteren Zeitpunkt benötigen.

    ![Neuer Schritt hinzugefügt.](./media/setup_rsa_tool_93.png)

12. Wählen Sie **Bearbeitung beendet** aus.
13. Wählen Sie **In Lifecycle Services speichern** aus, und ordnen Sie die neue Aufgabenaufzeichnung der gleichen BPM-Bibliothek und demselben Geschäftsprozess zu, der die ursprüngliche Aufgabenaufzeichnung zugeordnet war. Weitere Informationen finden Sie im Abschnitt [Erstellen einer Aufgabenaufzeichnung und Speichern in der BPM-Bibliothek](#create-a-task-recording-and-save-it-to-the-bpm-library).
14. Navigieren Sie zur BPM-Bibliothek, und wählen Sie **Testfälle synchronisieren** aus, um die Aufgabenaufzeichnung zu überschreiben, die dem Testfall in Azure DevOps zugeordnet ist, wie im Abschnitt [Testen der Synchronisierung von BPM zu Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) beschrieben.
15. Öffnen Sie RSAT und wählen Sie **Laden** aus, um alle Testfälle in der Testsuite erneut zu laden. Sie müssen die Automatisierung und die Parameterdateien für den entsprechenden Testfall erneut generieren, indem Sie den Testfall auswählen und dann **Neu \> Test-Ausführung und Parameterdateien generieren** auswählen, wie im Abschnitt [Laden und Ausführen von Testfällen](#load-and-run-test-cases) beschrieben.

    > [!NOTE]
    > Wenn die Excel-Parameterdatei offen gelassen wurde, schlägt die Regeneration fehl. Daher sollten Sie sicherstellen, dass die Excel-Parameterdatei für den Testfall geschlossen ist, bevor Sie die neue Excel-Parameterdatei generieren.

16. Wählen Sie **Bearbeiten** aus, um die neue Excel-Parameterdatei zu öffnen. Sie finden einen neuen **Gespeicherte Variable**-Eintrag in Zeile 9. Diese Variable, **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** wird in der XML-Datei der Aufgabenaufzeichnung gespeichert und kann in folgenden Tests verwendet werden.

    ![Eintrag der gespeicherten Variable.](./media/setup_rsa_tool_94.png)

#### <a name="create-a-new-test-case"></a>Neuen Testfall erstellen

1. Navigieren Sie zur **RSAT**-BPM-Bibliothek
2. Wählen Sie den Prozess **Beispiel-Support-Geschäftsprozess** und dann auf der rechten Seite die Option **Bearbeitungsmodus** aus.
3. Ändern Sie den Wert der beiden Felder **Name** und **Beschreibung** zu **Ein Produkt veröffentlichen**. Wählen Sie dann **Speichern** aus.

    ![Name und Beschreibung geändert, um ein Produkt zu veröffentlichen.](./media/setup_rsa_tool_95.png)

#### <a name="create-a-new-task-recording-that-has-a-validate-function"></a>Erstellen einer neuen Aufgabenaufzeichnung, die eine Validierungsfunktion hat

- Erstellen Sie einer Aufgabenaufzeichnung, um das Produkt zu veröffentlichen, das zuvor in der juristische USRT-Person erstellt wurde. Weitere Informationen finden Sie im Abschnitt [Erstellen einer Aufgabenaufzeichnung und Speichern in der BPM-Bibliothek](#create-a-task-recording-and-save-it-to-the-bpm-library).

    > [!NOTE]
    > Für verkettete Testfälle wird immer empfohlen, dass Sie den erforderlichen Datensatz suchen oder danach filtern, indem Sie *den Wert des Felds manuell eingeben*. Auf diese Weise kann das Tool den Datensatz bestimmen, für den die Aktion im folgenden Testfall ausgeführt werden muss.

    ![Neue Aufgabenaufzeichnung, die eine Validierungsfunktion hat.](./media/setup_rsa_tool_96.png)

    Für die vorherige Darstellung zeigt, validieren Sie den Wert des Felds **Produktnummer** nachdem das Produkt mit dem Schnellfilter gefunden wurde, aber bevor Sie **Produkte veröffentlichen** auswählen, um sicherzustellen, dass es sich bei der Produktkennung um die von zuvor handelt. Um den Wert zu überprüfen, klicken Sie mit der rechten Maustaste auf das Feld **Produktnummer**, und wählen Sie dann **Aufgabenaufzeichnung \> Überprüfen \> Aktueller Wert** aus.

    ![Validieren des aktuellen Werts.](./media/setup_rsa_tool_97.png)

#### <a name="save-the-task-recording-to-bpm"></a>Aufgabenaufzeichnung in BPM speichern

1. Nachdem die Aufgabenaufzeichnung abgeschlossen ist, wählen Sie **Lifecycle Services** aus.

    ![Speichern Sie die abgeschlossene Aufgabenaufzeichnung in Lifecycle Services.](./media/setup_rsa_tool_98.png)

2. Bibliotheksinformationen werden aus LCS geladen.

    ![Laden von Bibliotheksinformationen aus LCS.](./media/setup_rsa_tool_99.png)

3. Wählen Sie die BPM-Bibliothek aus, die der Aufgabenaufzeichnung zugeordnet werden soll. In diesem Lernprogramm wählen Sie die **RSAT**-BPM-Bibliothek aus, die zuvor erstellt wurde, und den Geschäftsprozess **Ein Produkt veröffentlichen** darunter. Wählen Sie dann **OK** aus.

#### <a name="sync-bpm-to-azure-devops"></a>BPM mit Azure DevOps synchronisieren

1. Navigieren Sie zur BPM-Bibliothek, und öffnen Sie die Bibliothek **RSAT**.
2. Wählen Sie **VSTS-Synchronisierung** und anschließend **Testfälle synchronisieren** aus. Weitere Informationen finden Sie im Abschnitt [Testen der Synchronisierung von BPM mit Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops).

    Nach Abschluss der Synchronisierung wird die neue Arbeitsaufgabe und der entsprechende Testfall für den Geschäftsprozess **Ein Produkt veröffentlichen** in Azure DevOps unter **Karten \> Arbeitsaufgaben** angezeigt.

#### <a name="add-the-new-test-case-to-the-existing-test-suite"></a>Den neuen Testfall der vorhandenen Testsuite hinzufügen

1. Navigieren Sie zu **Testpläne \> Testpläne** und wählen Sie den Plan **RSAT-Testplan** aus.
2. Wählen Sie **Vorhandene Elemente auswählen** aus.
3. Wählen Sie auf der Seite **Testfällen der Suite hinzufügen** **Abfrage ausführen** aus.
4. Wählen Sie den neuen Testfall aus, der für **Produkt veröffentlichen** erstellt wurde, und wählen Sie dann **Testfälle hinzufügen** in der unteren rechten Ecke der Seite aus (diese Schaltfläche wird in der folgenden Abbildung nicht dargestellt).

    ![Seite „Testfällen der Suite hinzufügen“.](./media/setup_rsa_tool_100.png)

    Die Testsuite besitzt nun zwei Testfälle.

    ![Zwei Testfälle in der Testsuite.](./media/setup_rsa_tool_101.png)

#### <a name="load-test-cases-into-rsat"></a>Testfälle in RSAT laden

1. Öffnen Sie RSAT und wählen Sie **Laden** aus.
2. Die Testfälle werden geladen und Sie erhalten folgende Warnung „Diese Aktivität überschreibt Excel-Testdatendateien, lokale Änderungen gehen verloren. Möchten Sie den Vorgang fortsetzen?“ Wählen Sie **Ja**, um die Excel-Parameterdateien im lokalen System zu aktualisieren, ohne die Excel-Parameterdateien zu aktualisieren, die zu Azure DevOps hochgeladen wurden.

    ![Diese Aktion überschreibt Excel-Testdatendateien.](./media/setup_rsa_tool_102.png)

    Beide Testfälle werden geladen, zusammen mit der Excel-Parameterdatei für den ersten Testfall. Da Sie bei der letzten Ausführung **Hochladen** ausgewählt haben, werden die Parameterdateien von Azure DevOps gezogen.

    ![Testfälle geladen.](./media/setup_rsa_tool_103.png)

3. Wählen Sie nur den zweiten Testfall, und wählen Sie dann **Neu \> Testausführungs- und Parameterdateien generieren** aus.

#### <a name="edit-the-excel-parameter-file"></a>Excel-Parameterdatei bearbeiten

1. Wählen Sie nur den zweiten Testfall aus, und wählen Sie dann **Bearbeiten** aus, um die entsprechenden Excel-Parameterdatei zu öffnen.
2. Kopieren Sie die gespeicherte Variable **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** (weitere Informationen im Abschnitt [Ändern einer vorhandenen Aufgabenaufzeichnung, um einer gespeicherte Variablen zu erstellen](#modify-an-existing-task-recording-to-create-a-saved-variable)) aus dem ersten Testfall in alle Felder, in denen die Produktnummer verwendet wird. In diesem Fall kopieren Sie die Variable in die Felder **Produktnummer** und **Produktnummer prüfen** im Arbeitsblatt **EcoResProductListPage**.

    ![Felder „Produktnummer“ und „Produktnummer prüfen“.](./media/setup_rsa_tool_104.png)

    > [!NOTE]
    > Variablen können nur zwischen Tests für den gleichen Testlauf übergeben werden. Die Namen der Variablen müssen genau übereinstimmen.

3. Wählen Sie **Speichern** aus und schließen die Excel-Arbeitsmappe.
4. Wählen Sie **Hochladen** aus, um die Änderungen zu speichern, die Sie an der Excel-Parameterdatei vorgenommen haben.

#### <a name="run-the-chained-test-cases"></a>Verkettete Testfälle ausführen

1. Wählen Sie beide Testfälle aus, die ausgeführt werden sollen, und wählen Sie dann **Ausführen** aus.
2. Überprüfen Sie, dass beide Testfälle erfolgreich waren.

    ![Auf „Erfolgreich“ festgelegtes Ergebnisfeld für beide Testfälle.](./media/setup_rsa_tool_105.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]