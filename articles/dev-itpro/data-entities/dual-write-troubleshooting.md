---
title: Leitfaden zur Problembehandlung für die Datenintegration
description: Dieses Thema enthält Problembehandlungsinformationen zur Datenintegration zwischen Microsoft Dynamics 365 for Finance and Operations und Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: ca62a6b3aa64ec2383ee3ded3b7bbf4650a41166
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797274"
---
# <a name="troubleshooting-guide-for-data-integration"></a>Leitfaden zur Problembehandlung für die Datenintegration

## <a name="enable-plugin-trace-in-common-data-service-and-check-the-dual-write-plugin-error-details"></a>Aktivieren der Plug-In-Ablaufverfolgung in Common Data Service und Überprüfen der Plug-In-Fehlerdetails für duales Schreiben

Wenn Sie bei der Synchronisierung des dualen Schreibens ein Problem haben oder ein Fehler auftritt, können Sie die Fehler im Ablaufverfolgungsprotokoll überprüfen:

1. Bevor Sie die Fehler überprüfen können, müssen Sie die Plug-In-Ablaufverfolgung mithilfe der Anweisungen unter [Plug-In registrieren](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) aktivieren. Jetzt können Sie die Fehler überprüfen.
2. Melden Sie sich bei Dynamics 365 for Sales an.
3. Klicken Sie auf das Einstellungssymbol (ein Zahnrad), und wählen Sie **Erweiterte Einstellungen** aus.
4. Wählen Sie im Menü **Einstellungen** die Option **Anpassung > Plug-In-Ablaufverfolgungsprotokoll** aus.
5. Klicken Sie auf den Typnamen **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**, um die Fehlerdetails anzuzeigen.

## <a name="check-dual-write-synchronization-errors-in-finance-and-operations"></a>Überprüfen von Synchronisierungsfehlern beim dualen Schreiben in Finance and Operations

Sie können die Fehler während des Testens überprüfen, indem Sie die folgenden Schritte ausführen:

+ Melden Sie sich bei LifeCycle Services (LCS) an.
+ Öffnet das LCS-Projekt, das Sie ausgewählt haben, um das Testing für das duale Schreiben durchzuführen.
+ Gehen Sie zu den in der Cloud gehosteten Umgebungen.
+ Stellen Sie über Remotedesktop eine Verbindung zum Finance and Operations-VM mithilfe des lokalen Kontos her, das in LCS angezeigt wird.
+ Öffnen Sie die Ereignisanzeige. 
+ Navigieren Sie zu **Anwendungs- und Dienstprotokolle > Microsoft > Dynamics > AX-DualWriteSync > Operativ**. Die Fehler und Details werden angezeigt.

## <a name="how-to-unlink-and-link-another-common-data-service-environment-from-finance-and-operations"></a>Vorgehensweise zum Herstellen und Aufhaben einer Verknüpfung zu einer anderen Common Data Service-Umgebung von Finance and Operations aus

Sie können Links aktualisieren, indem Sie die folgenden Schritte ausführen:

+ Navigieren Sie zur Finance and Operations-Umgebung.
+ Öffnen Sie die Datenverwaltung.
+ Klicken Sie auf **Verknüpfung zu CDS für Apps**.
+ Wählen Sie alle ausgeführten Zuordnungen aus, und klicken Sie auf **Beenden**. 
+ Wählen Sie alle Zuordnungen aus, und klicken Sie auf **Löschen**.

    > [!NOTE]
    > Die Option **Löschen** wird nicht angezeigt, wenn die Vorlage **CustomerV3-Account** ausgewählt wird. Heben Sie die Auswahl bei Bedarf auf. **CustomerV3-Account** ist eine ältere bereitgestellte Vorlage und funktioniert mit der Prospect to Cash-Lösung. Da es global veröffentlicht wird, wird es unter allen Vorlagen angezeigt.

+ Klicken Sie auf **Verknüpfung für Umgebung aufheben**.
+ Klicken Sie zur Bestätigung auf **Ja**.
+ Um die neue Umgebung zu verknüpfen, führen Sie die Schritte unter [Installationsleitfaden](https://aka.ms/dualwrite-docs) aus.

