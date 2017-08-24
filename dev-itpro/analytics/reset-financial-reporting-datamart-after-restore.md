---
title: "Finanzberichts-Data Mart noch Wiederherstellung der Datenbank Zurücksetzen"
description: "In diesem Thema wird beschrieben, wie Finanzberichts-Data Mart zurückgesetzt wird, nachdem die Microsoft Dynamics 365 for Finance and Operations-Datenbank wiederhergestellt wurde."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 9953d2f29a67b35f4bb43f577df1c4d910e379a1
ms.openlocfilehash: 08a420a776f47119a5dc47f9119545aa448ffdbd
ms.contentlocale: de-de
ms.lasthandoff: 08/03/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>Finanzberichts-Data Mart noch Wiederherstellung der Datenbank Zurücksetzen

[!include[banner](../includes/banner.md)]


In diesem Thema wird beschrieben, wie Finanzberichts-Data Mart zurückgesetzt wird, nachdem die Microsoft Dynamics 365 for Finance and Operations-Datenbank wiederhergestellt wurde.

Wenn Sie ggf. die Finanz- und Arbeitsgangsdatenbank aus einer Sicherung wiederherstellen oder die Datenbank aus einer anderen Umgebung kopieren, müssen Sie die Schritte in diesem Thema ausführen, um sicherzustellen, dass der Rechnungslegungs-datamart ordnungsgemäß die zu stornierenden Finanz- und Arbeitsgangsdatenbank verwendet. 
<!--If you have questions about resetting the financial reporting data mart for a reason outside of restoring a Finance and Operations database, refer to the [Resetting the Management Reporter data mart](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) for more information. -->
> [!Note] 
> Beachten Sie, dass die Schritte dieses Prozesses für Dynamics 365 for Operations Mai 2016 (App-Build 7.0.1265.23014 und Financial Reporting Build 7.0.10000.4) und später Versionen unterstützt werden. Wenn Sie eine frühere Version von Finance and Operations nutzen, wenden Sie sich bitte an unser Support-Team.

## <a name="export-report-definitions"></a>Exportieren von Berichtsdefinitionen
Zuerst exportieren Sie die Berichtsdesigns im Berichts-Designer, und zwar mithilfe der folgenden Schritte aus:

1.  Wechseln Sie im Berichts-Designer zu **Unternehmen** &gt; **Bausteingruppen**.
2.  Wählen Sie die Bausteingruppe aus, die exportiert werden soll, und klicken Sie **Export**. 
    > [!Note] 
    > Für Finance and Operations wird nur eine Bausteingruppe, unterstützt **Standard**.
3.  Wählen Sie die Berichtsdefinition für den Export aus:
    -   Um alle Ihre Berichtsdefinitionen und die zugeordneten Bausteine zu exportieren, klicken Sie auf **Alles auswählen**.
    -   Um bestimmte Berichte, Zeilen, Spalten, Strukturen oder Dimensionssätze zu exportieren, klicken Sie auf die entsprechende Registerkarte und wählen die Artikel aus, die exportiert werden sollen. Drücken und halten Sie die STRG-Taste gedrückt, um mehrere Elemente in einer Registerkarte auszuwählen. Wenn Sie Berichte zum Exportieren auswählen, werden die zugeordneten Zeilen, Spalten, Baumstrukturen und Dimensionssätze ausgewählt.

4.  Klicken Sie auf "**Export**".
5.  Geben Sie einen Dateinamen eingeben und einen sicheren Ort aus, an dem Sie die exportierten Berichtsdefinitionen speichern möchten.
6.  Klicken Sie auf **Speichern**.

Die Datei kann an einem sicheren Speicherort kopiert oder hochgeladen werden und in einer anderen Umgebung, in einer anderen der Zeitpunkt importiert werden können. Informationen zur Verwendung eines Microsoft Azure Storage-Kontos können gefunden werden in [Daten mit dem AzCopy-Kommandozeilenutility übertragen](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy). 
> [!NOTE]
> Microsoft stellt kein Speicherkonto im Rahmen der Finance and Operations Vereinbarung bereit. Sie müssen entweder ein Speicherkonto kaufen oder ein Speicherkonto von einem separaten Azure-Abonnement verwenden. 
> [!WARNING]
> Wichtig: Berücksichtigen Sie das Verhalten des D-Laufwerks von Azure Virtual Machines. Speichern Sie nicht die exportierten Bausteingruppen dort dauerhaft. Weitere Informationen zu temporären, finden Sie unter [Informationen zum temporären Laufwerk in Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

## <a name="stop-services"></a>Services anhalten
Verwenden den Remotedesktop, um sich mit allen Computern in der Umgebung zu verbinden und die folgenden Windows-Dienste zu beenden, indem Sie services.msc verwenden:

-   Per Internet WWW-Publishing-Dienst (für alle AOS-Computer)
-   Microsoft Dynamics 365 for Finance and Operations Batch Management Service (nur nicht-private AOS-Computern)
-   Management Reporter 2012 Process Service (nur BI-Computer)

Diese Dienste haben offene Verbindungen zur Finance and Operations-Datenbank.

## <a name="reset"></a>Zurücksetzen
#### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a>Suchen und laden Sie das letzte MinorVersionDataUpgrade.zip-Paket herunter

Suchen Sie das letzte MinorVersionDataUpgrade.zip-Paket mithilfe der Anweisungen in [Skript DataUpgrade.zip herunterladen](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package) herunter. Die Anweisungen zeigen, wie Sie die korrekte Version des Datenaktualisierungspakets für Ihre Umgebung lokalisieren und herunterladen. Eine Aktualisierung ist nicht erforderlich, um das MinorVersionDataUpgrade.zip-Paket herunterzuladen. Sie müssen nur die Schritte des "Herunterladen zur Bereitstellung geeigneter Paket der letzten Aktualisierung abschließen" Bereich, ohne einen der Schritte im anderen Artikel, um eine Kopie des MinorVersionDataUpgrade.zip-Pakets abzurufen.

#### <a name="execute-scripts-against-finance-and-operations-database"></a>Ausführen von Skripts für die Finance and Operations-Datenbank

Führen Sie die folgenden Skripts für die Finance and Operations-Datenbank aus (nicht für die Financial-Reporting-Datenbank).

-   DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Diese Skripts sicherstellen, dass die Benutzer, die Rollen und die Änderungsnachverfolgungseinstellungen korrekt sind.

#### <a name="execute-powershell-command-to-reset-database"></a>PowerShell-Befehle zum zurückzusetzen der Datenbank

Führen Sie den folgenden Befehl direkt auf dem AOS-Computer aus, um die Integration zwischen Finance and Operations und Financial Reporting zurückzusetzen:

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
-   Microsoft Dynamics 365 for Finance and Operations Batch Management Service (nur nicht-private AOS-Computern)
-   Management Reporter 2012 Process Service (nur BI-Computer)

## <a name="import-report-definitions"></a>Imporiteren von Berichtsdefinitionen
Importieren Sie die Berichtsdesigns im Berichts-Designer, und zwar mithilfe der Datei, die während des Exports erstellt wird:

1.  Wechseln Sie im Berichts-Designer zu **Unternehmen** &gt; **Bausteingruppen**.
2.  Wählen Sie die Bausteingruppe aus, die exportiert werden soll, und klicken Sie **Export**. 

    > [!NOTE]
    > Für Finance and Operations wird nur eine Bausteingruppe, unterstützt **Standard**.
    
3.  Wählen Sie den **Standard**-Baustein und klicken Sie auf **Importieren**.
4.  Wählen Sie die Datei aus, welche die exportierten Berichtsdefinitionen enthält und klicken Sie auf **Öffnen**.
5.  Wählen Sie im Dialogfeld Importieren die Berichtsdefinitionen aus, die importiert werden soll:
    -   Um alle Berichtsdefinitionen und die unterstützenden Bausteine zu importieren, klicken Sie auf **Alles auswählen**.
    -   Um bestimmte Berichte, Zeilen, Spalten, Baumstrukturen oder Dimensionssätze zu importieren, wählen Sie die Berichte, Zeilen, Spalten, Baumstrukturen oder Dimensionssätze aus, die importiert werden sollen.

6.  Klicken Sie auf **Importieren**.





