---
title: Ein Fehler tritt auf, wenn der Lagerplatz während der Kommissionierlistenregistrierung ausgewählt wird
description: Ein Fehler tritt auf, wenn der Lagerplatz während der Kommissionierlistenregistrierung ausgewählt wird.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b7fc579821f9a80d94aea949fcc0301b9d8f6935
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026525"
---
# <a name="an-error-occurs-when-the-location-is-selected-during-picking-list-registration"></a>Ein Fehler tritt auf, wenn der Lagerplatz während der Kommissionierlistenregistrierung ausgewählt wird

KB-Nummer: 4613106

## <a name="symptoms"></a>Symptome

Dieses Problem tritt auf, wenn Ihr System so konfiguriert ist, dass Aufträge automatisch reserviert werden. Wenn Sie versuchen, den Lagerplatz für eine Kommissionierlistenregistrierungsposition auszuwählen, wird bei Verwendung des Reservierungsprozesses im Lagerortmanagement (WMS) die folgende Fehlermeldung angezeigt:

> Menge kann nicht mit neuen Dimensionen aktualisiert werden

Dieses Problem kann auftreten, weil Sie an einem bestimmten Lagerplatz nicht über genügend Bestände verfügen.

## <a name="resolution"></a>Lösung

Das System verhält sich wie vorgesehen.

In Szenarien, in denen Sie den Reservierungsprozess auf Lagerortebene verwenden, sollten Sie den manuellen Reservierungsprozess von der Entnahmeposition aus verwenden, wenn der vorhandene Bestand nicht auf allen Bestandsdimensionsebenen reserviert wird und Sie nicht über ausreichend verfügbare Bestände an einem bestimmten Lagerplatz verfügen. Sie können dann die Funktion *Los reservieren* zum Verteilen der unteren Reservierungen verwenden, z. B. des Lagerplatzes, für alle verfügbaren Mengen.
