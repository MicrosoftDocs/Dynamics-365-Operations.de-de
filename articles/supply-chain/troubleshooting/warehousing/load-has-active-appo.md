---
title: Sie können eine Sendung nicht bestätigen, weil es ein Problem mit dem Kalender gibt
description: Sie können eine Sendung nicht bestätigen, weil es ein Problem mit dem Kalender gibt
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f1fccd10d8867252f32b37c77f9a3bad54157bdd
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938478"
---
# <a name="you-cant-confirm-a-shipment-because-of-an-issue-with-the-calendar"></a>Sie können eine Sendung nicht bestätigen, weil es ein Problem mit dem Kalender gibt

Fehlercode: TRX2716

## <a name="symptoms"></a>Symptome

Wenn Sie versuchen, eine Sendung zu bestätigen, zeigt das System die folgende Fehlermeldung an:

> Der Kalendertyp %1 erfordert, dass der Termin %2 ein- und ausgecheckt wird.

Daher können Sie die Sendung für die Ladung nicht bestätigen.

## <a name="cause"></a>Ursache

Aktive Termine für die Ladung sind vorhanden. Zum Beispiel gibt es eine Regel, die das Einchecken von Fahrern erfordert. Daher befindet sich die Ladung derzeit in einem Status, in dem die Versandbestätigung fehlschlägt.

## <a name="resolution"></a>Lösung

Sie müssen alle Probleme mit den aktiven Terminen, die mit der Ladung verbunden sind, untersuchen und beheben.

1. Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.
1. Wählen Sie die Ladung, für die die Sendung nicht bestätigt werden kann.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Transporte** in der Gruppe **Termine** den Eintrag **Terminplanung**.
1. Führen Sie einen dieser Schritte aus:

    - Stellen Sie sicher, dass das Ein- und Auschecken des Fahrers für den Termin abgeschlossen ist.
    - Vervollständigen oder stornieren Sie den Termin.
    - Deaktivieren Sie die Option **Fahrer Check-In erforderlich** für die zugehörige Terminregel.
