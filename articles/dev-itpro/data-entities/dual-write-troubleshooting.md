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
ms.openlocfilehash: 5e71729dafd2ad85a01b055363d1c7056b5558b2
ms.sourcegitcommit: 3f05ede8b8acdf0550240a83a013e093b4ad043d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2019
ms.locfileid: "1873104"
---
# <a name="troubleshooting-guide-for-data-integration"></a>Leitfaden zur Problembehandlung für die Datenintegration

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a>Aktivieren der Plug-In-Ablaufverfolgungsprotokolle in Common Data Service und Überprüfen der Plug-In-Fehlerdetails für duales Schreiben

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Sollte ein Problem oder Fehler bei der Synchronisierung des dualen Schreibens auftreten, führen Sie die folgenden Schritte aus, um die Fehler im Ablaufverfolgungsprotokoll zu überprüfen.

1. Bevor Sie die Fehler überprüfen können, müssen Sie Plug-In-Ablaufverfolgungsprotokolle aktivieren. Anweisungen finden Sie im Abschnitt „Ablaufverfolgungsprotokolle anzeigen“ im [Tutorial: Schreiben und Registrieren eines Plug-Ins](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).

    Jetzt können Sie die Fehler überprüfen.

2. Melden Sie sich bei Microsoft Dynamics 365 for Sales an.
3. Wählen Sie die Schaltfläche **Einstellungen** (das Zahnradsymbol) aus, und wählen Sie dann **Erweiterte Einstellungen** aus.
4. Wählen Sie im Menü **Einstellungen** die Option **Anpassung \> Plug-In-Ablaufverfolgungsprotokoll**.
5. Wählen Sie **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** als Typnamen aus, um die Fehlerdetails anzuzeigen.

## <a name="inspect-dual-write-synchronization-errors-in-finance-and-operations"></a>Überprüfen von Synchronisierungsfehlern beim dualen Schreiben in Finance and Operations

Gehen Sie folgendermaßen vor, um während des Testens Fehler zu überprüfen.

1. Melden Sie sich bei Microsoft Dynamics Lifecycle Services (LCS) an.
2. Öffnen Sie das LCS-Projekt, wofür der Test für das duale Schreiben durchgeführt werden soll.
3. Wählen Sie **In der Cloud gehostete Umgebungen** aus.
4. Stellen Sie eine Remote Desktop-Verbindung mit dem virtuellen Dynamics 365 for Finance and Operations-Computer her, indem Sie lokales Konto verwenden, das in LCS angezeigt wird.
5. Öffnen Sie die Ereignisanzeige. 
6. Gehen Sie zu **Anwendungs- und Dienstprotokolle \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operativ**. Die Fehler und Details werden angezeigt.

## <a name="unlink-one-common-data-service-environment-from-finance-and-operations-and-link-another-environment"></a>Aufheben einer Common Data Service-Umgebungs-Verknüpfung von Finance and Operations und Verknüpfung einer anderen Umgebung

Um Verknüpfungen zu aktualisieren, führen Sie die folgenden Schritte aus:

1. Gehen Sie zur Finance and Operations-Umgebung.
2. Öffnen Sie die Datenverwaltung.
3. Wählen Sie **Verknüpfung zu CDS für Apps** aus.
4. Wählen Sie alle Zuordnungen aus, die ausgeführt werden, und wählen Sie dann **Beenden** aus.
5. Wählen Sie alle Zuordnungen und dann **Löschen** aus.

    > [!NOTE]
    > Die Option **Löschen** ist nicht verfügbar, wenn die Vorlage **CustomerV3-Account** ausgewählt wird. Heben Sie die Auswahl dieser Vorlage nach Bedarf auf. **CustomerV3-Account** ist eine ältere bereitgestellte Vorlage und funktioniert mit der Prospect to Cash-Lösung. Da es global veröffentlicht wird, wird es unter allen Vorlagen angezeigt.

6. Wählen Sie **Verknüpfung für Umgebung aufheben** aus.
7. Wählen Sie **Ja** aus, um den Vorgang zu bestätigen.
8. Um die neue Umgebung zu verknüpfen, führen Sie die Schritte unter [Installationsleitfaden](https://aka.ms/dualwrite-docs) aus.
