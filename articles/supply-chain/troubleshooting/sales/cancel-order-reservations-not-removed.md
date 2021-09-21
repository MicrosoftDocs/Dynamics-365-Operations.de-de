---
title: Reservierungen können nicht entfernt werden, wenn ein Auftrag storniert wird
description: Sie können einen Auftrag erst stornieren, wenn die diesem Auftrag zugeordnete Arbeit storniert oder rückgängig gemacht wurde. Befolgen Sie hierzu die folgenden drei Schritte.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a8d947e64568246dba5eff3c21fd3920b6494b73
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476455"
---
# <a name="reservations-cannot-be-removed-when-canceling-an-order"></a>Reservierungen können nicht entfernt werden, wenn ein Auftrag storniert wird

## <a name="symptoms"></a>Symptome

Wenn einem Auftrag Arbeit zugeordnet ist und Sie versuchen, diesen Auftrag zu stornieren, wird die folgende Fehlermeldung angezeigt:

> Reservierungen können nicht entfernt werden, da von diesen Reservierungen abhängige Arbeit erstellt wird.

Sie können den Auftrag erst stornieren, wenn die diesem Auftrag zugeordnete Arbeit storniert oder rückgängig gemacht wurde. Diese Anforderung gilt auch dann, wenn die mit dem Auftrag verbundene Arbeit abgeschlossen ist.

## <a name="resolution"></a>Lösung

Um dieses Problem zu beheben, führen Sie die folgenden Schritte aus:

1. Stornieren Sie die Arbeit und legen Sie den Bestand wieder an den gewünschten Lagerplatz. Gehen Sie zur entsprechenden Auslastung des Auftrags und wählen Sie entweder **Entnommene Menge reduzieren** auf der Ladungsposition oder **Arbeit stornieren** im Aktionsbereich.

    Die Arbeit hat jetzt den Status *Storniert* und neue Bestandsbewegungsarbeiten werden automatisch erstellt und verarbeitet, um den Bestand wieder an den Lagerplatz zu bringen, der zum Zeitpunkt der Stornierung beschrieben wurde.

2. Löschen Sie die Auslastung. Die Lieferung wird ebenfalls gelöscht.

3. Sie sollten nun in der Lage sein, zum Auftrag zu gehen und ihn zu stornieren.
