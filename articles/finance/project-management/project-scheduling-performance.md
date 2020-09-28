---
title: Leistung der Projektressourcenplanung
description: Dieses Thema enthält Informationen zur Verbesserung der Leistung der Ressourcenplanung für eine große Anzahl von Projekten.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 988fc83230f08a6534caa7c37784757d73c1cc12
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760559"
---
# <a name="project-resource-scheduling-performance"></a>Leistung der Projektressourcenplanung

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Leistungsprobleme im Zusammenhang mit der Ressourcenplanung können auftreten, wenn die Anzahl der Projekte Tausende beträgt. Um die Leistung der Ressourcenplanung zu verbessern, steht eine Funktion zur Verfügung, mit der Benutzer die Zeit reduzieren können, die zum Starten des Ressourcenverfügbarkeitsformulars erforderlich ist. Dies entfernt insbesondere den Rollup-Synchronisierungsprozess für die Ressourcenkapazität und verwendet die **ResProjectResource**-Tabelle, um die Ressourcensuche zu beschleunigen. Beachten Sie, dass die **ResRollup**-Tabelle nicht mehr verwendet wird.

> [!IMPORTANT]
> Bei einer Abhängigkeit vom Rollup-Synchronisierungsprozess der Ressourcenkapazität oder von der **ResProjectResource**-Tabelle verwenden Sie diese Funktion nicht.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Aktivieren der Leistungsverbesserung bei der Ressourcenplanung
Führen Sie die folgenden Schritte aus, um die Leistungsverbesserung bei der Ressourcenplanung zu aktivieren.

1. Wechseln Sie zu **Funktionsverwaltung** > **Alle** und suchen Sie in der Funktionsliste nach **Funktion zum Aktivieren der Leistungsverbesserung bei der Ressourcenplanung**.
2. Wählen Sie **Jetzt aktivieren**.

> [!NOTE]
> Wenn Sie die Funktion in der Liste nicht finden können, wählen Sie **Auf Updates prüfen**, um die Liste zu aktualisieren.

3. Aktualisieren Sie Ihren Browser und wechseln Sie dann zu **Projektverwaltung und Buchhaltung** > **Periodisch** > **Projektressourcen** > **Kapazität für Kalender und Ressourcen in allen Unternehmen synchronisieren** .
4. Legen Sie **Vorhandene Kapazitätsdatensätze entfernen** auf **Ja** fest, um vorherige Daten zu entfernen. Wenn Sie inkrementelle Daten generieren möchten, legen Sie diese Option auf **Nein** fest.
5. wählen Sie im Feld **Periodencode** den Zeitraum aus, in dem Daten generiert werden sollen. Wenn Sie einen Periodencode auswählen, müssen kein Start- und Enddatum definiert werden.
6. Wenn Sie das Feld **Periodencode** leer lassen, wählen Sie bestimmte Start- und Enddaten aus, um Daten zu generieren.
7. Wählen Sie **OK**.

 > [!NOTE]
 > Dadurch werden allgemeine Daten in allen Unternehmen in Ihrer Umgebung an die **ResCalendarCapacity**-Tabelle verteilt sodass der Batch-Auftrag nur in einer juristischen Person ausgeführt werden muss. Die Daten in diesem Batch-Auftrag werden benötigt, um die Ressourcenkapazität für den zugehörigen Kalender zu berechnen.

8. Wechseln Sie zu **Projektverwaltung und Buchhaltung** > **Periodisch** > **Projektressourcen** > **Projektressourcen in allen Unternehmen füllen** und wählen Sie dann **OK**. Dies ist das Datenaktualisierungsskript für allgemeine Daten in den Tabellen **ResProjectResource**, **ResCalendarDateTimeRange** und **ResEffectiveDateTimeRange**. Werte für das **PSAPRojSchedRole.RootActivity**-Feld werden ebenfalls aktualisiert. Wenn dies nicht ausgeführt wird, erhalten Sie eine Warnung, wenn Sie versuchen, Ressourcenplanungsvorgänge auszuführen.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Ausschalten der Leistungsverbesserung bei der Ressourcenplanung

1. Wechseln Sie zu **Funktionsverwaltung** > **Alle** und suchen Sie nach **Funktion zum Aktivieren der Leistungsverbesserung bei der Ressourcenplanung**.
2. Wählen Sie die Funktion aus und wählen Sie dann die **Deaktivieren**-Schaltfläche aus.
3. Aktualisieren Sie Ihren Browser.
4. Wechseln Sie zu **Projektverwaltung und Buchhaltung** > **Periodisch** > **Kapazitätssynchronisierung** > **Ressourcenkapazitätszusammenfassungen synchronisieren**.
5. Auf der **Synchronisation der Kapazitätszusammenfassung**-Seite, setzen Sie **Vorhandene Kapazitätsdatensätze entfernen** auf **Ja**, um vorherige Daten zu entfernen. Wenn Sie inkrementelle Daten generieren möchten, legen Sie diese Option auf **Nein** fest.
6. wählen Sie im Feld **Periodencode** den Zeitraum aus, in dem Daten generiert werden sollen. Wenn Sie einen Periodencode auswählen, müssen kein Start- und Enddatum definiert werden.
7. Wenn Sie das Feld **Periodencode** leer lassen, wählen Sie bestimmte Start- und Enddaten aus, um Daten zu generieren.
8. Wählen Sie **OK**.

> [!NOTE]
> Dadurch werden allgemeine Daten in allen Unternehmen in Ihrer Umgebung an die **ResRollup**-Tabelle verteilt sodass der Batch-Auftrag nur in einer juristischen Person ausgeführt werden muss. Dieser Batch-Auftrag wird für alle **Ressourcenverfügbarkeit**-Ansichten benötigt. Wenn dieser Batch-Auftrag nicht ausgeführt wird, werden die **ResRollup**-Daten im laufenden Betrieb generiert, was einige Zeit dauern kann.
