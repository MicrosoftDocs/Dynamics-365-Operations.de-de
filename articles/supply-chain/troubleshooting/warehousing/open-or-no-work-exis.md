---
title: Sie können eine Sendung nicht bestätigen, weil Arbeiten unvollständig sind oder fehlen
description: Sie können eine Sendung nicht bestätigen, weil Arbeiten unvollständig sind oder fehlen
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm, WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: beef0909d41e69f3e7bcc1021527be35b7e6fd44
ms.sourcegitcommit: c2c6d687a89bc1534c029109315c23e92865b63b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2021
ms.locfileid: "6123842"
---
# <a name="you-cant-confirm-a-shipment-because-of-incomplete-or-missing-work"></a>Sie können eine Sendung nicht bestätigen, weil Arbeiten unvollständig sind oder fehlen

Fehlercode: WAX515

## <a name="symptoms"></a>Symptome

Wenn Sie versuchen, eine Sendung zu bestätigen, zeigt das System die folgende Fehlermeldung an:

> Die Lieferung für die Ladung %1 konnte nicht überprüft werden, da sämtliche Arbeiten für die Ladung abgeschlossen sein müssen.

Daher können Sie die Sendung für die Ladung nicht bestätigen.

## <a name="cause"></a>Ursache

Die Ladung oder Sendung befindet sich derzeit in einem Status, in dem die Versandbestätigung fehlschlägt. Bevor Sie die Ladung bestätigen können, müssen zumindest einige Arbeiten für die Ladung vorhanden sein, und alle diese Arbeiten müssen einen Status von *Geschlossen* oder *Storniert* haben.

## <a name="resolution"></a>Lösung

Prüfen Sie die zugehörigen Verkaufsaufträge oder Umlagerungsaufträge für die Ladung oder den Transport, und stellen Sie sicher, dass alle zugehörigen Arbeiten abgeschlossen oder storniert wurden.

Sie können mit Sendungen und Ladungen auf mehreren Seiten arbeiten. In den folgenden Unterabschnitten finden Sie einige Beispiele.

### <a name="all-loads-page"></a>Alle Ladungen Seite

1. Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.
1. Wählen Sie die Ladung, für die die Sendung nicht bestätigt werden kann.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Ladungen** in der Gruppe **Zugehörige Informationen** die Option **Arbeit**.
1. Untersuchen Sie den Status jeder Arbeits-ID. Verfolgen Sie jede Arbeits-ID nach, die nicht den Status *Geschlossen* oder *Storniert* hat.
1. Wenn jede Arbeits-ID den Status *Geschlossen* oder *Abgebrochen* hat, versuchen Sie erneut, die Sendung zu bestätigen.

### <a name="all-shipments-page"></a>Alle Sendungen Seite

1. Gehen Sie zu **Lagerortverwaltung \> Lieferungen \> Alle Lieferungen**.
1. Wählen Sie die Sendung aus, die nicht bestätigt werden kann.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Sendungen** in der Gruppe **Arbeit** die Option **Arbeitsdetails**.
1. Untersuchen Sie den Status jeder Arbeits-ID. Verfolgen Sie jede Arbeits-ID nach, die nicht den Status *Geschlossen* oder *Storniert* hat.
1. Wenn jede Arbeits-ID den Status *Geschlossen* oder *Abgebrochen* hat, versuchen Sie erneut, die Sendung zu bestätigen.

### <a name="all-work-page"></a>Seite „Alle Arbeiten

1. Gehen Sie zu **Lagerortverwaltung \> Arbeit \> Alle Arbeiten**.
1. Wählen Sie die Arbeit für die Auftragsnummer, für die die Sendung nicht bestätigt werden kann.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Sendung** in der Gruppe **Sendung** die Option **Sendung bestätigen**.
1. Untersuchen Sie den Status jeder Arbeits-ID. Verfolgen Sie jede Arbeits-ID nach, die nicht den Status *Geschlossen* oder *Storniert* hat.
1. Wenn jede Arbeits-ID den Status *Geschlossen* oder *Abgebrochen* hat, versuchen Sie erneut, die Sendung zu bestätigen.
