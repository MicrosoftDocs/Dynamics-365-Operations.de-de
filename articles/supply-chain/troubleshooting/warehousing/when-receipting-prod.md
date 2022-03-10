---
title: Auf einem Beleg wird nur eine Beschriftung für mehrere Arbeitsköpfe gedruckt
description: Auf einem Beleg wird nur eine Beschriftung für mehrere Arbeitsköpfe gedruckt.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: cf307964a07c2b69eb5e4ef2cf9dc094482736d0970e333e84f674c9be6331c7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740526"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a>Auf einem Beleg wird nur eine Beschriftung für mehrere Arbeitsköpfe gedruckt

KB-Nummer: 4614667

## <a name="symptoms"></a>Symptome

Im Rahmen eines einzelnen Empfangsereignisses in der Lagerort-App werden mehrere Arbeitsköpfe für den gleichen Zielladungsträger erstellt. Bei Erhalt des Produkts wird jedoch nur eine Ladungsträgerbeschriftung gedruckt.

## <a name="resolution"></a>Lösung

Das System verhält sich wie vorgesehen.

Im aktuellen Design wird unabhängig von der Anzahl der vorhandenen Kombinationen aus Arbeitskopf und Arbeitsposition immer nur eine Ladungsträgerbeschriftung generiert. Die generierte Beschriftung enthält die Informationen für nur eine Kombination.

Stellen Sie zur Umgehung dieses Problems sicher, dass die Erstellung des Arbeitskopfs immer nur einem Zielladungsträger zugeordnet ist.
