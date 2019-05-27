---
title: Vereinbarungen zum Servicelevel
description: In einer SLA stimmt der Debitor einer Mindestantwortzeit zu, basierend auf der Zeit zwischen der Aufzeichnung des Problems durch das Serviceunternehmen bis zum Beheben des Problems.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cffe3a7766502dd5d888a7a99a32150967911301
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562625"
---
# <a name="service-level-agreements"></a>Vereinbarungen zum Servicelevel        

[!include [banner](../includes/banner.md)]


Eine Vereinbarung zum Servicelevel (Service Level Agreement, SLA) ist eine Vereinbarung zwischen einem Serviceunternehmen und einem Debitor. In einer SLA stimmt der Debitor einer Mindestantwortzeit zu, basierend auf der Zeit zwischen der Aufzeichnung des Problems durch das Serviceunternehmen bis zum Beheben des Problems.

Eine SLA setzt einen Standard-Servicelevel durch, der Debitoren angeboten wird, und zeigt außerdem einem Serviceunternehmen an, wann ein Servicevorgang ausgeführt werden soll.

Es kann eine beliebige Zahl von SLAs erstellt werden, um Debitoren verschiedene Servicelevels zu bieten.

## <a name="create-a-service-level-agreement"></a>Erstellen einer Vereinbarung zum Servicelevel

1.  Klicken Sie auf **Serviceverwaltung** \> **Einstellungen** \> **Servicevereinbarungen** \> **Vereinbarungen zum Servicelevel**.

2.  Geben Sie einen Namen für eine Vereinbarung zum Servicelevel im Feld **Vereinbarung zum Servicelevel** ein.

3.  Geben Sie die Zeit ein, die Sie für die Ausführung von Serviceeinsätzen einräumen möchten, die der Vereinbarung zum Servicelevel zugeordnet sind. Wählen Sie dann einen Kalender aus, wenn die Vereinbarung zum Servicelevel auf einem bestimmten Kalender beruhen soll.

## <a name="apply-a-service-level-agreement"></a>Anwenden einer Vereinbarung zum Servicelevel

Die SLA wird direkt auf eine Servicevereinbarung angewendet.

Serviceaufträge, die Sie manuell erstellen und einer Servicevereinbarung zuordnen, die eine SLA hat, werden anhand dieser SLA gemessen.

Automatisch erstellte Serviceaufträge werden keiner Vereinbarung zum Servicelevel zugeordnet.

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a>Anwenden der Vereinbarung zum Servicelevel auf die Servicevereinbarung

1.  Klicken Sie auf den Bereichsseitenknoten: **Serviceverwaltung** \> **Gemeinsam** \> **Servicevereinbarungen** \> **Servicevereinbarungen**. Wählen Sie die Servicevereinbarung aus, auf die Sie die SLA anwenden möchten, und klicken Sie anschließend im **Aktivitätsbereich** auf **Bearbeiten**.

2.  Wählen Sie im **Vereinbarung zum Servicelevel** Feld die Vereinbarung zum Servicelevel, die Sie zuordnen möchten.

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a>Anwenden der Vereinbarung zum Servicelevel auf die Servicevereinbarungsgruppe

1.  Klicken Sie auf **Serviceverwaltung** \> **Einstellungen** \> **Servicevereinbarungen** \> **Serviceverinbarungsgruppen**.

2.  Wählen Sie im **Vereinbarung zum Servicelevel** Feld die Vereinbarung zum Servicelevel, die Sie zuordnen möchten.

## <a name="track-time-on-a-service-order-against-an-sla"></a>Zeiterfassung für einen Serviceauftrag anhand der Vereinbarung zum Servicelevel

Wenn Sie einen neuen Serviceauftrag für eine Servicevereinbarung erstellen, der eine SLA zugewiesen ist, wird das Zeitintervall für die Lieferung des Services gestartet, und das System beginnt mit der Erfassung der Lieferzeit. Darüber hinaus können Sie die folgenden Optionen festlegen:

  - Sie können die Zeitaufzeichnung für den Serviceauftrag starten und anhalten, um die Gesamtzeit für Serviceaufträge zu erfassen.

  - Sie können die Einhaltung des in der Vereinbarung zum Servicelevel festgelegten Zeitrahmens überwachen.

  - Sie können Ursachencodes definieren, die festgelegt sein müssen, wenn der Zeitrahmen der Vereinbarung zum Servicelevel überschritten wird.

## <a name="see-also"></a>Siehe auch

[Anzeigen der Konformität mit Vereinbarungen zum Servicelevel](view-compliance-with-service-level-agreements.md)

  


