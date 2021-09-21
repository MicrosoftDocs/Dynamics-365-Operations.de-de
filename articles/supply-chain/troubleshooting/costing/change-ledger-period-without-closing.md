---
title: Warnungen oder Fehler beim Ändern des Sachkontoperiodenstatus ohne Bestandsabschluss
description: Warnungen oder Fehler beim Ändern des Sachkontoperiodenstatus ohne Bestandsabschluss
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 05851753e29da75f014d2cc77e2b8df259620eee
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476430"
---
# <a name="warnings-or-errors-on-changing-ledger-period-status-without-closing-inventory"></a>Warnungen oder Fehler beim Ändern des Sachkontoperiodenstatus ohne Bestandsabschluss

Microsoft hat die folgenden Überprüfungen eingeführt, um Probleme zu vermeiden, die durch einen fehlerhaften Periodenabschlussprozess rund um die Kalkulation verursacht werden. Wenn eine der folgenden Fehlermeldungen auftritt, finden Sie in [KB 4561987](https://fix.lcs.dynamics.com/Issue/Details?kb=4561987&bugId=445351&dbType=3&qc=f514f2adcddcddceec43af58c26ae8a9020effdc7cdfe085d9d0deeb8cc7b6a3) weitere Informationen zur Behebung dieser Probleme.

- Sie sind im Begriff, eine Neukalkulation mit dem Datum %1 (10.02.2019) auszuführen. Die letzte registrierte Neuberechnung wurde in einer früheren Periode mit einem Datum %2 (20.01.2019) ausgeführt. Es wurde keine Ausführung eines Bestandsabschlusses mit dem Datum %3 (31.01.2019) passend zum Periodenende registriert. Bitte denken Sie daran, einen Bestandsabschluss zum Datum %3 (31.01.2019) passend zum Periodenende auszuführen. Die Bewertung der Bestände, des Wareneinsatzes und der Abweichungen sind im Neben- oder Hauptbuch möglicherweise nicht korrekt, bis dies ausgeführt wurde.

- Sie sind dabei, den Status der Sachkontoperiode %1 auf %2 zu ändern. Es wurde keine Ausführung eines Bestandsabschlusses mit einem Datum %3, das mit dem Periodenende übereinstimmt, registriert. Bitte führen Sie einen Bestandsabschluss ab %3 passend zum Periodenende aus, bevor Sie den Status ändern. Die Bewertung der Bestände, des Wareneinsatzes und der Abweichungen sind im Neben- oder Hauptbuch möglicherweise nicht korrekt, bis dies ausgeführt wurde. Gemeldet von der juristischen Entität %4. Derzeit dient dies nur zu Informationszwecken, aber diese Aktivität wird in Zukunft erforderlich sein.

- Die Kontenstruktur %1 wurde geändert. Ein oder mehrere Hauptkonten %2 sind nicht mehr vorhanden. Diese Hauptkonten werden von der %3 mit einem Datum %4 benötigt. Bitte fügen Sie diese Hauptkonten zur Kontenstruktur %1 hinzu, bevor Sie den Auftrag %3 fortsetzen können. Derzeit dient dies nur zu Informationszwecken, aber diese Aktivität wird in Zukunft erforderlich sein.

- Sie sind dabei, einen Bestandsabschluss mit einem Datum %1 (31.01.2019) auszuführen. Es wurde keine Ausführung einer retrograden Kalkulation mit einem Datum %2 (31.01.2019) registriert, das dem Periodenende entspricht. Bitte denken Sie daran, eine Nachkalkulation mit einem Datum %3 (31.01.2019) passend zum Periodenende auszuführen. Die Bewertung der Bestände, des Wareneinsatzes und der Abweichungen sind im Neben- oder Hauptbuch möglicherweise nicht korrekt, bis dies ausgeführt wurde.

- Sie sind im Begriff, eine Nachkalkulation mit dem Datum %1 (28.02.2019) auszuführen. Die letzte registrierte Nachkalkulation wurde in einer vorherigen Periode mit einem Datum %2 (31-01-2019) ausgeführt. Es wurde keine Ausführung eines Bestandsabschlusses mit dem Datum %3 (31.01.2019) registriert, der mit einem Periodenende übereinstimmt.

Bitte denken Sie daran, einen Bestandsabschluss zum Datum %3 (31.01.2019) passend zu einem Periodenende auszuführen. Die Bewertung der Bestände, die Selbstkosten und die Abweichungen sind in der Nebenbuchhaltung oder im Hauptbuch möglicherweise nicht korrekt, bis der Bestandsabschluss ausgeführt wurde.