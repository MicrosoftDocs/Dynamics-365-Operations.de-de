---
title: Setzt den Rechnungslegungs-datamart wieder, nachdem Sie eine Datenbank wiederhergestellt wurde
description: "In diesem Thema wird beschrieben, wie der Rechnungslegungs-datamart zurückgesetzt wird, nachdem er Microsoft Dynamics 365 für Arbeitsgangsdatenbank storniert hat."
author: twheeloc
manager: AnnBe
ms.date: 2016-12-08 16 - 20 - 13
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 3967cbb869fbb23d5d7716f619e4c22b4a273921
ms.lasthandoff: 03/29/2017


---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>Setzt den Rechnungslegungs-datamart wieder, nachdem Sie eine Datenbank wiederhergestellt wurde

In diesem Thema wird beschrieben, wie der Rechnungslegungs-datamart zurückgesetzt wird, nachdem er Microsoft Dynamics 365 für Arbeitsgangsdatenbank storniert hat. 

Es gibt mehrere Szenarios, in denen möglicherweise das Dynamics 365 für Arbeitsgangsdatenbank aus einer Sicherung wiederherstellen oder die Datenbank aus einer anderen Umgebung kopieren müssen. Wenn dies der Fall ist, müssen Sie auch die entsprechenden Aktivitäten ausgeführt werden, um sicherzustellen, dass der Rechnungslegungs-datamart ordnungsgemäß das zu stornierenden Dynamics 365 für Arbeitsgangsdatenbank verwendet. Wenn Sie Fragen zum Zurücksetzen des Rechnungslegungs-datamarts für eine Ursache außerhalb der Beitreibung von Dynamics 365 für Arbeitsgangsdatenbank haben, finden Sie unter den Reporter-datamart Management [] (https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) zurücksetzend unter. Beachten Sie, dass die Schritte dieses Prozesses für Dynamics 365 zur Freigabe des Arbeitsgangs im Mai 2016 (App-Build 7.0.1265.23014 und Rechnungslegungsbuild 7.0.10000.4) und später Versionen unterstützt werden. Wenn Sie einer früheren Version von Microsoft Dynamics 365 für Arbeitsgänge wurde, wenden Sie sich bitte unserem mit Unterstützung für Team - Hilfe.

## <a name="export-report-definitions"></a>Exportieren von Berichtsdefinitionen
Zuerst exportieren Sie die Berichtsdesigne im Berichts-Designer, und zwar mithilfe der folgenden Schritte aus:

1.  Im Berichts-Designer fahren ** Unternehmen ** &gt; ** Bausteingruppen **.
2.  Wählen Sie die Bausteingruppe aus, die exportiert werden soll, und klicken Sie ** Export **. ** Hinweis: ** Für Dynamics 365 für Arbeitsgänge, wird nur eine Bausteingruppe, unterstützt ** Standard **.
3.  Wählen Sie die Berichtsdefinitionen aus, die exportiert werden soll:
    -   Um alle Ihre Berichtsdefinitionen und die zugeordneten Bausteine zu exportieren, klicken Sie auf **Alles auswählen**.
    -   Um bestimmte Berichte, Zeilen, Spalten, Strukturen oder Dimensionssätze zu exportieren, klicken Sie auf die entsprechende Registerkarte und wählen die Artikel aus, die exportiert werden sollen. Drücken und halten Sie die STRG-Taste gedrückt, um mehrere Elemente in einer Registerkarte auszuwählen. Wenn Sie Berichte für den Export auswählen, werden in, werden die zugeordneten Zeilen, Spalten, Strukturen und Dimensionssätze ausgewählt.

4.  ** Export ** auf.
5.  Geben Sie einen Dateinamen eingeben und einen sicheren Ort aus, an dem Sie die exportierten Berichtsdefinitionen speichern möchten.
6.  Click **Save**.

Die Datei kann an einem sicheren Speicherort zu kopierenden oder hochgeladen werden und in einer anderen Umgebung, in einer anderen der Zeitpunkt importiert werden können. Informationen zur Verwendung eines Microsoft Azure-Speicherkontos können in gefunden werden Daten mit dem AzCopy-Befehlszeilenprogramm []( https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy). ** Hinweis: ** Microsoft stellt ein Speicherkonto nicht im Rahmen Ihres Dynamics 365 für Arbeitsgangsvereinbarung bereit. Sie müssen entweder ein Speicherkonto kaufen oder ein Speicherkonto von einem separaten Azure Dauerauftrag verwenden. ** Wichtig: ** Berücksichtigen Sie das Verhalten des D-Laufwerks auf Azure virtuellen Computer. Führen Sie nicht die exportierten Bausteingruppen hier dauerhaft. Weitere Informationen zu temporären, finden Sie Laufwerke [das temporäre Laufwerk auf Windows Azure-virtuellenComputern]( https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/) verstehen.

## <a name="stop-services"></a>Beenden von Services
Verwenden Sie die, um an Desktop aller Computer in der Umgebung herstellen und die folgenden Windows-Dienste zu beenden, indem Sie services.msc verwenden:

-   Per Internet Web-Veröffentlichungsdienst (für alle AOS-Computern)
-   Microsoft Dynamics 365 für Arbeitsgangs-Chargen-Verwaltungsservice (nur nicht-privaten AOS-Computern)
-   Management Reporter-Prozessdienst 2012 (nur BIcomputern)

Diese Dienstleistungen haben offene Beziehungen zum Dynamics 365 für Arbeitsgangsdatenbank.

## <a name="reset"></a>Zurücksetzen
#### <a name="locate-the-latest-dataupgradezip-package"></a>Suchen Sie das letzte DataUpgrade.zip-Paket

Suchen Sie das letzte DataUpgrade.zip-Paket mithilfe der Positionen, die in enthalten sind [laden Sie das DataUpgrade.zip-Skript herunter.] ". \ \ MigrationAktualisierung upgrade-data-to-latest-update.md). Die Positionen, für wie die korrekte Version des Datenaktualisierungspakets für Ihre Umgebung lokalisiert.

#### <a name="execute-scripts-against-dynamics-365-for-operations-database"></a>Führen Sie Skripts für Dynamics 365 für Arbeitsgangsdatenbank aus

Führen Sie die folgenden Skripts für das Dynamics 365 für Arbeitsgangsdatenbank aus (nicht für die Rechnungslegungsdatenbank).

-   Skripts ConfigureAxReportingIntegration.sql \\DataUpgrade.zip\\AosService\\
-   Skripts GrantAzViewChangeTracking.sql \\DataUpgrade.zip\\AosService\\

Diese Skripts sicherstellen, dass die Benutzer, die Rollen und die Änderungsnachverfolgungs einstellungen korrekt sind.

#### <a name="execute-powershell-command-to-reset-database"></a>Führen Sie PowerShell-Befehls zurückzusetzen Datenbank aus,

Führen Sie den folgenden Befehl, direkt auf dem Computer aus, die Integration zwischen Dynamics 365 für Arbeitsgänge und Finanzberichte zurückzusetzen:

1.  Öffnet Sie Windows PowerShell als Administrator.
2.  Ausführen: F:
3.  Ausführen: CD F:\\MRApplicationService\\MRInstallDirectory
4.  Ausführen: Import-Modul.\\MRDeploy Server\\\\MRDeploy.psd1
5.  Ausführen: Zurückgesetztes-DatamartIntegration - Grund ANDERER - Grund "&lt;ReasonDetail Kontrollkästchen für das Zurücksetzen&gt;"
    -   Sie werden gegebenenfalls aufgefordert, "Y" eingeben, um zu bestätigen.

Erläuterung der Parameter:

-   Die gesetzmäßigen Werte für - Grund sind: WARTUNG, BADDATA, ANDERES.
-   - Der Text ReasonDetail-Parameter ist.
-   Der Grund und das reasonDetail werden in der Telemetrie-/Umgebungsüberwachung erfasst.

## <a name="start-services"></a>Anfangsdienstleistungen
Verwenden Sie services.msc, um die Services neu zu starten, die Sie eben beendeten:

-   Per Internet Web-Veröffentlichungsdienst (für alle AOS-Computern)
-   Microsoft Dynamics 365 für Arbeitsgangs-Chargen-Verwaltungsservice (nur nicht-privaten AOS-Computern)
-   Management Reporter-Prozessdienst 2012 (nur BIcomputern)

## <a name="import-report-definitions"></a>Importieren von Berichtsdefinitionen
Importieren Sie die Berichtsdesigne im Berichts-Designer, und zwar mithilfe der Datei, die während des Exports erstellt wird:

1.  Im Berichts-Designer fahren ** Unternehmen ** &gt; ** Bausteingruppen **.
2.  Wählen Sie die Bausteingruppe aus, die exportiert werden soll, und klicken Sie ** Export **. ** Hinweis: ** Für Dynamics 365 für Arbeitsgänge, wird nur eine Bausteingruppe, unterstützt ** Standard **.
3.  Wählen Sie den Standardwert ** ** Baustein aus und klicken Sie ** Import **.
4.  Wählen Sie die Datei aus, welche die exportierten Berichtsdefinitionen enthält und klicken Sie ** geöffnet **.
5.  Wählen Sie im Dialogfeld Importieren die Berichtsdefinitionen aus, die importiert werden soll:
    -   Um alle Berichtsdefinitionen und die unterstützenden Bausteine zu importieren, klicken Sie auf **Alles auswählen**.
    -   Um bestimmte Berichte, Zeilen, Spalten, Baumstrukturen oder Dimensionssätze zu importieren, wählen Sie die Berichte, Zeilen, Spalten, Baumstrukturen oder Dimensionssätze aus, die importiert werden sollen.

6.  Click **Import**.



