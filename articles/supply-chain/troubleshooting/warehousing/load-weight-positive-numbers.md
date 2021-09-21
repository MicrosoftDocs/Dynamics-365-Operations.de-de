---
title: Ladegewicht darf nur positive Zahlen enthalten
description: Bei der Verarbeitung von Arbeiten zwischen Lagerplätzen kann es sein, dass Sie eine Fehlermeldung bezüglich des Ladegewichts erhalten und Ihre Aktualisierung abgebrochen wird. Führen Sie die folgenden Schritte aus, um das Problem zu beheben.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8ea1f6679a521e3e8683b8e5f18f509e98044414
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476432"
---
# <a name="load-weight-error-and-update-canceled-when-processing-work-between-locations"></a>Aufgrund eines Ladegewichtsfehlers wurde die Aktualisierung während der Verarbeitung zwischen Lagerplätzen abgebrochen.

## <a name="symptoms"></a>Symptome

Wenn bei der Verarbeitung von Arbeit von Packplätzen zu Lagerplätzen oder von Lagerplätzen zu Andockplätzen offene Arbeit vorhanden ist, erhalten Sie möglicherweise folgenden Fehler:

> Das Feld „Ladegewicht“ (= –%1) darf nur positive Zahlen enthalten. Aktualisierung wurde storniert.

## <a name="resolution"></a>Lösung

Um dieses Problem zu beheben, gehen Sie zu **Systemadministration \> Periodische Aufgaben \> Datenbank \> Konsistenzprüfung**, und führen Sie den Prozess für **Konsistenzprüfung für Lagerort-Lastgewicht** aus.
