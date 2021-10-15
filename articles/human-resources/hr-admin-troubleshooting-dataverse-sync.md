---
title: Dataverse-Synchronisierung zurücksetzen
description: In diesem Thema wird die Problembehebung bei Datensätzen beschrieben, die zwischen Microsoft Dynamics 365 Human Resources und der Human Capital Management (HCM) Common-Lösung in Microsoft Dataverse nicht synchronisiert werden können.
author: jaredha
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-09-27
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: d88f538fbf22313feaca6771b7cb1757a3c3fbad
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559649"
---
# <a name="reset-dataverse-synchronization"></a>Dataverse-Synchronisierung zurücksetzen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a>Problem

Datensätze werden zwischen Microsoft Dynamics 365 Human Resources und den Entitäten in der Human Capital Management (HCM) Common-Lösung in Microsoft Dataverse nicht synchronisiert. Weitere Informationen zur Synchronisierung finden Sie unter [Dataverse-Integration konfigurieren](hr-admin-integration-common-data-service.md). Eine fehlerhafte Synchronisierung kann auftreten, wenn die Batchaufträge **Dataverse-Integrationswiederholung** oder **Fehlende Anforderungssynchronisierung bei der Dataverse-Integration** im Status **Ausführung** verbleiben.

## <a name="resolution"></a>Lösung

Wenn die Batchaufträge **Dataverse-Integrationswiederholung** oder **Fehlende Anforderungssynchronisierung bei der Dataverse-Integration** im Status **Ausführen** oder **Abbrechen** verbleiben, können Sie den Status zurücksetzen. Dies kann durch Abbrechen des Batchauftrags erfolgen, indem Sie die Anleitung unter [Steckengebliebene Batchaufträge zurücksetzen](hr-admin-troubleshooting-batch-execution.md) befolgen. Nachdem Sie den Batchauftrag abgebrochen haben, können Sie den Batchauftrag zurücksetzen, indem Sie ihn in den Status **Warten** versetzen. Der Batchauftrag wird dann während der nächsten geplanten Laufzeit ausgeführt.

1. Falls noch nicht geschehen, aktivieren Sie die Funktion **Erweiterter Batchabbruch** in der **Funktionsverwaltung**.
   1. Wechseln Sie zur Seite **Funktionsverwaltung** (**Systemadministration** > **Zusammenfassung** > **Funktionsverwaltung**).
   2. Wählen Sie die Registerkarte **Alle** aus.
   3. Wählen Sie die Spalte **Funktionsname** aus, und filten Sie nach **Erweiterte Batchabbruch**.
   4. Wählen Sie die Aktion **Aktivieren** aus, wenn sie nicht bereits aktiviert ist.

2. Deaktivieren Sie die Dataverse-Integration.
   1. Wechseln Sie zur Seite **Microsoft Dataverse-Integration** (**Systemadministration**, navigieren Sie zu **Links** > **Integrationen** > **Dataverse-Konfiguration**).
   2. Legen Sie die Option **Dataverse-Integration aktivieren** auf **Nein** fest.

3. Brechen Sie den Batchauftrag **Dataverse Integrationswiederholung** ab.
   1. Wechseln Sie zur Seite **Batchaufträge** (**Systemadministration**, navigieren Sie zu **Links** > **Batchaufträge** > **Batchaufträge**).
   2. Filtern Sie die Spalte **Einzelvorgangsbeschreibung** nach **Integration**.
   3. Wählen Sie den Batchauftrag **Dataverse-Integrationswiederholung** aus.
   4. Wählen Sie im Aktionsband die **Batchauftrag**, **Abbrechen erzwingen** und dann **Ja** aus, um den Vorgang zu bestätigen.

   > [!NOTE]
   > Je nachdem, wann die Integration zum ersten Mal aktiviert wurde, kann die Beschreibung des Batchauftrags **Common Data Service-Integrationswiederholung** lauten. Wählen Sie anstelle des Batchauftrags **Dataverse-Integrationswiederholung** diesen Batchauftrag aus, wenn er aufgeführt ist.

4. Löschen Sie alle Batch-Aufträge der Dataverse-Integration.
   1. Wählen Sie auf der Seite **Batch-Aufträge** die Batch-Aufträge **Fehlende Anforderungssynchronisierung bei der Dataverse-Integration**, **Dataverse- Integrationswiederholung** und **Erstsynchronisierung bei der Dataverse-Integration** aus.
   2. Wählen Sie im Aktionsband die Aktion **Status ändern** aus. 
   3. Wählen Sie **Zurückhalten** und dann **OK** aus.
   4. Wählen Sie im Aktionsmenüband die Aktion **Löschen** und anschließend **Ja** aus, um die Aktion zu bestätigen.

5. Aktivieren Sie die Batch-Aufträge der Dataverse-Integration.
   1. Wechseln Sie zur Seite **Microsoft Dataverse-Integration** (**Systemadministration** > **Links** > **Integration** > **Dataverse-Konfiguration**).
   2. Legen Sie die Option **Dataverse-Integration aktivieren** auf **Ja** fest.

6. Wechseln Sie zur Seite **Batch-Aufträge**, und bestätigen Sie, dass die Batch-Aufträge **Dataverse-Integrationswiederholung** und **Fehlende Anforderungssynchronisierung bei der Dataverse-Integration** erstellt wurden.

Nachdem die Batch-Aufträge neu erstellt wurden, können Sie nun den Batchauftrag **Dataverse Integrationswiederholung** überwachen, um zu ermitteln, wie lange die Ausführung des Auftrags dauert. Sie können dann überprüfen, ob die Datensätze korrekt mit der HCM Common-Lösung in Microsoft Dataverse synchronisiert werden.

## <a name="see-also"></a>Siehe auch

[Dataverse-Integration konfigurieren](hr-admin-integration-common-data-service.md)<br>
[Steckengebliebene Batchaufträge zurücksetzen](hr-admin-troubleshooting-batch-execution.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
