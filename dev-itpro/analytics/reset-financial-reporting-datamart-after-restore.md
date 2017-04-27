---
title: "Finanzberichts-Data Mart noch Wiederherstellung der Datenbank Zurücksetzen"
description: "In diesem Thema wird beschrieben, wie Finanzberichts-Data Mart zurückgesetzt wird, nachdem die Microsoft Dynamics 365 for Operations-Datenbank wiederhergestellt wurde."
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

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>Finanzberichts-Data Mart noch Wiederherstellung der Datenbank Zurücksetzen

In diesem Thema wird beschrieben, wie Finanzberichts-Data Mart zurückgesetzt wird, nachdem die Microsoft Dynamics 365 for Operations-Datenbank wiederhergestellt wurde. 

Es gibt mehrere Szenarios, in denen möglicherweise die Dynamics 365 for Operations-Datenbank aus einer Sicherung wiederherstellen oder die Datenbank aus einer anderen Umgebung kopieren müssen. Wenn dies der Fall ist, müssen Sie auch die entsprechenden Aktivitäten ausgeführt werden, um sicherzustellen, dass der Finanzberichts-Data Mart ordnungsgemäß die wiederhergestellte Dynamics 365 for Operations-Datenbank verwendet. Wenn Sie Fragen zum Zurücksetzen des Finanzberichts-Data Mart außerhalb der Wiederherstellung der Dynamics 365 for Operations-Datenbank haben, finden Sie unter [Management Reporter-Data-Mart zurücksetzen](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) weitere Informationen. Beachten Sie, dass die Schritte dieses Prozesses für Dynamics 365 for Operations Mai 2016 (App-Build 7.0.1265.23014 und Financial Reporting Build 7.0.10000.4) und später Versionen unterstützt werden. Wenn Sie einer früheren Version von Microsoft Dynamics 365 for Operations nutzen, wenden Sie sich bitte unserem Support-Team.

## <a name="export-report-definitions"></a>Exportieren von Berichtsdefinitionen
Zuerst exportieren Sie die Berichtsdesigns im Berichts-Designer, und zwar mithilfe der folgenden Schritte aus:

1.  Wechseln Sie im Berichts-Designer zu **Unternehmen** &gt; **Bausteingruppen**.
2.  Wählen Sie die Bausteingruppe aus, die exportiert werden soll, und klicken Sie **Export**. **Hinweis:** Für Dynamics 365 for Operations wird nur eine Bausteingruppe, unterstützt (**Standard**).
3.  Wählen Sie die Berichtsdefinition für den Export aus:
    -   Um alle Ihre Berichtsdefinitionen und die zugeordneten Bausteine zu exportieren, klicken Sie auf **Alles auswählen**.
    -   Um bestimmte Berichte, Zeilen, Spalten, Strukturen oder Dimensionssätze zu exportieren, klicken Sie auf die entsprechende Registerkarte und wählen die Artikel aus, die exportiert werden sollen. Drücken und halten Sie die STRG-Taste gedrückt, um mehrere Elemente in einer Registerkarte auszuwählen. Wenn Sie Berichte zum Exportieren auswählen, werden die zugeordneten Zeilen, Spalten, Baumstrukturen und Dimensionssätze ausgewählt.

4.  Klicken Sie auf "**Export**".
5.  Geben Sie einen Dateinamen eingeben und einen sicheren Ort aus, an dem Sie die exportierten Berichtsdefinitionen speichern möchten.
6.  Klicken Sie auf **Speichern**.

Die Datei kann an einem sicheren Speicherort kopiert oder hochgeladen werden und in einer anderen Umgebung, in einer anderen der Zeitpunkt importiert werden können. Informationen zur Verwendung eines Microsoft Azure Storage-Kontos können gefunden werden in [Daten mit dem AzCopy-Kommandozeilenutility übertragen](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy). **Hinweis:** Microsoft stellt ein Speicherkonto nicht im Rahmen Ihrer Dynamics 365 for Operations Vereinbarung bereit. Sie müssen entweder ein Speicherkonto kaufen oder ein Speicherkonto von einem separaten Azure-Abonnement verwenden. **Wichtig:** Berücksichtigen Sie das Verhalten des D-Laufwerks von Azure Virtual Machines. Speichern Sie nicht die exportierten Bausteingruppen dort dauerhaft. Weitere Informationen zu temporären, finden Sie unter [Informationen zum temporären Laufwerk in Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

## <a name="stop-services"></a>Services anhalten
Verwenden den Remotedesktop, um sich mit allen Computern in der Umgebung zu verbinden und die folgenden Windows-Dienste zu beenden, indem Sie services.msc verwenden:

-   Per Internet WWW-Publishing-Dienst (für alle AOS-Computer)
-   Microsoft Dynamics 365 for Operations Batch Management Service (nur nicht-private AOS-Computern)
-   Management Reporter 2012 Process Service (nur BI-Computer)

Diese Dienste haben offene Verbindungen zur Dynamics 365 for Operations-Datenbank.

## <a name="reset"></a>Zurücksetzen
#### <a name="locate-the-latest-dataupgradezip-package"></a>Suchen Sie das letzte DataUpgrade.zip-Paket

Suchen Sie das letzte DataUpgrade.zip-Paket mithilfe Anweisungen aus [Download the DataUpgrade.zip script](..\migration-upgrade\upgrade-data-to-latest-update.md). Die Anweisungen zeigen, wie Sie die korrekte Version des Datenaktualisierungspakets für Ihre Umgebung lokalisieren.

#### <a name="execute-scripts-against-dynamics-365-for-operations-database"></a>Ausführen von Skripts für die Dynamics 365 for Operations-Datenbank

Führen Sie die folgenden Skripts für die Dynamics 365 for Operations-Datenbank aus (nicht für die Financial-Reporting-Datenbank).

-   DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Diese Skripts sicherstellen, dass die Benutzer, die Rollen und die Änderungsnachverfolgungseinstellungen korrekt sind.

#### <a name="execute-powershell-command-to-reset-database"></a>PowerShell-Befehle zum zurückzusetzen der Datenbank

Führen Sie den folgenden Befehl direkt auf dem AOS-Computer aus, um die Integration zwischen Dynamics 365 for Operations und Financial Reporting zurückzusetzen:

1.  Windows PowerShell als Administrator öffnen.
2.  Ausführen: F:
3.  Ausführen: cd F:\\MRApplicationService\\MRInstallDirectory
4.  Ausführen: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1
5.  Ausführen: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;my reason for resetting&gt;”
    -   Sie werden gegebenenfalls aufgefordert, "Y" einzugeben, um zu bestätigen.

Erläuterung der Parameter:

-   Die gültigen Werte für -Reason sind: SERVICING, BADDATA, OTHER.
-   Der -ReasonDetail-Parameter ist Freitext.
-   Der Grund und reasonDetail werden in der Telemetrie-/Umgebungsüberwachung erfasst.

## <a name="start-services"></a>Dienste starten
Verwenden Sie services.msc, um die Services neu zu starten, die Sie eben beendeten:

-   Per Internet WWW-Publishing-Dienst (für alle AOS-Computer)
-   Microsoft Dynamics 365 for Operations Batch Management Service (nur nicht-private AOS-Computern)
-   Management Reporter 2012 Process Service (nur BI-Computer)

## <a name="import-report-definitions"></a>Imporiteren von Berichtsdefinitionen
Importieren Sie die Berichtsdesigns im Berichts-Designer, und zwar mithilfe der Datei, die während des Exports erstellt wird:

1.  Wechseln Sie im Berichts-Designer zu **Unternehmen** &gt; **Bausteingruppen**.
2.  Wählen Sie die Bausteingruppe aus, die exportiert werden soll, und klicken Sie **Export**. **Hinweis:** Für Dynamics 365 for Operations wird nur eine Bausteingruppe, unterstützt (**Standard**).
3.  Wählen Sie den **Standard**-Baustein und klicken Sie auf **Importieren**.
4.  Wählen Sie die Datei aus, welche die exportierten Berichtsdefinitionen enthält und klicken Sie auf **Öffnen**.
5.  Wählen Sie im Dialogfeld Importieren die Berichtsdefinitionen aus, die importiert werden soll:
    -   Um alle Berichtsdefinitionen und die unterstützenden Bausteine zu importieren, klicken Sie auf **Alles auswählen**.
    -   Um bestimmte Berichte, Zeilen, Spalten, Baumstrukturen oder Dimensionssätze zu importieren, wählen Sie die Berichte, Zeilen, Spalten, Baumstrukturen oder Dimensionssätze aus, die importiert werden sollen.

6.  Klicken Sie auf **Importieren**.



