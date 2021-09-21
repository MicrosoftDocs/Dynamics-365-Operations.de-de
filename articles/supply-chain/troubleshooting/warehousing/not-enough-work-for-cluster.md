---
title: Nach der Profilkonfiguration wurde nicht genügend Arbeit für den Cluster gefunden
description: Wenn Sie ein Clusterprofil konfigurieren, erhalten Sie möglicherweise eine Fehlermeldung, die besagt, dass nicht genügend Arbeit gefunden wurde. Bearbeiten Sie das Profil und setzen Sie Positionen aktivieren auf „Nein“.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 139fd72e571c8ef83af2fd0e497cf334b6ef0ea4
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476410"
---
# <a name="not-enough-work-found-for-cluster-when-using-system-directed-cluster-picking"></a>Es wurde nicht genügend Arbeit für Cluster gefunden, während die systemgesteuerte Clusterauswahl verwendet wird

## <a name="symptoms"></a>Symptome

Bei Verwendung des Prozesses *Systemgesteuerte Cluster-Kommissionierung*, und wenn Sie ein Cluster-Profil konfigurieren, bei dem z.B. 10 Positionen entnommen werden können, funktioniert der Prozess wie geplant, wenn genügend Arbeit vorhanden ist, um 10 Positionen zu entnehmen. Wenn jedoch nur acht Positionen auszuwählen sind, erhalten Sie die folgende Fehlermeldung:

> Nicht genügend Arbeit für Cluster gefunden.

## <a name="resolution"></a>Lösung

Um dieses Problem zu beheben, bearbeiten Sie das Clusterprofil und legen Sie die Option **Positionen aktivieren** auf *Nein* fest.
