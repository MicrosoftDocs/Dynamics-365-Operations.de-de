---
title: Bei der Erfassung der Fertigmeldung wird ein Fehler gebucht
description: Wenn Sie den die Erfassung der Fertigmeldung buchen, erhalten Sie eine Fehlermeldung, dass die bestellte Menge nicht reduziert werden kann.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage, ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 55db7d0033dd66c1b973abf96671a20ab05d61d8
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026530"
---
# <a name="error-when-the-report-as-finished-journal-is-posted"></a>Bei der Erfassung der Fertigmeldung wird ein Fehler gebucht

KB-Nummer: 4612891

## <a name="symptoms"></a>Symptome

Wenn Sie die Erfassung **Fertigmeldung** buchen, tritt ein Fehler auf und Sie erhalten die folgende Fehlermeldung:

> Die bestellte Menge kann nicht reduziert werden, da nicht genügend offene Lagerposten mit dem Status 'Bestellt' vorhanden sind. Die Artikel sind als „Eingekauft“, „Eingegangen“ und „Registriert“ angegeben.

Dieser Fehler tritt nur auf, wenn das Feld **Fehlermenge** auf die erste Position der Erfassung **Fertigmeldung** und das Feld **Gutmenge** auf die letzte Position gesetzt ist. Wenn das Feld **Fehlermenge** auf die letzte Position gesetzt ist, tritt kein Fehler auf.

## <a name="resolution"></a>Lösung

Um diesen Fehler zu vermeiden, öffnen Sie die Seite **Produktionssteuerungsparameter** und dann die Registerkarte **Allgemein**, stellen Sie die Option **Verbleibende Menge um Fehlermenge erhöhen** auf *Ja*.
