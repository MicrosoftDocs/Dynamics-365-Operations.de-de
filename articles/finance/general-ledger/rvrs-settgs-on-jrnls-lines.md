---
title: Einstellungen für Erfassungen und Positionen stornieren
description: In diesem Thema wird erläutert, warum ein Stornoeintrag, der in einer allgemeinen Erfassung eingegeben wurde, möglicherweise nicht in der gebuchten Transaktion enthalten ist.
author: kweekley
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 74020f6fc9b0fa8e05a1e2a09fd13dcd60490dc0
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028564"
---
# <a name="reverse-settings-on-journals-and-lines"></a>Einstellungen für Erfassungen und Positionen stornieren

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, warum ein Stornoeintrag, der in einer allgemeinen Erfassung eingegeben wurde, möglicherweise nicht in der gebuchten Transaktion enthalten ist.  

## <a name="symptom"></a>Symptom

Eine allgemeine Erfassung enthält eine Stornierungsbuchung und ein Stornierungsdatum für die Erfassung. Wenn Sie die Erfassung buchen, wird keiner der Belege storniert. Was sind die Gründe dafür?

## <a name="resolution"></a>Lösung

Wenn die Erfassung gebucht wird, werden beim Stornierungsvorgang nur die Einstellungen **Stornierungseintrag** und **Stornierungsdatum** im Abschnitt **Positionen** des Belegs berücksichtigt. Dieser Ansatz ermöglicht es, in einer Erfassung einige zur Stornierung markierte sowie andere Belege einzubeziehen.

Die Werte aus der Erfassung werden nur beim Hinzufügen von *neuen* Positionen als Standardwerte verwendet. Änderungen an den Werten der Erfassung wirken sich nicht auf vorhandene Positionen aus. In diesem Beispiel wurden zuerst die Belegzeilen eingegeben. Wenn Sie die Positionsdetails eingeben, bevor Sie die Erfassung als Stornobuchung festlegen, wird die Bezeichnung für Stornierungseintrag und -datum nicht auf vorhandene Positionen angewendet.

Durch eine Änderung des Stornierungseintrags oder des Stornierungsdatums in einer vorhandenen Position werden diese Änderungen an andere Positionen im selben Beleg weitergegeben. Um die Leistung zu optimieren, wird das Raster nicht aktualisiert, nachdem Änderungen an andere Positionen weitergegeben wurden. Sie können die aktualisierten Werte anzeigen, indem Sie das Raster aktualisieren.


