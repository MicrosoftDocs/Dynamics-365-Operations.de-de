---
title: Sie können einen Artikel nicht mithilfe der Entität „Freigegebene Produkte V2“ importieren
description: Sie können einen Artikel nicht mithilfe der Entität „Freigegebene Produkte V2“ importieren.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended, DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: efd773313f89784d8fca6b37d867e204cb2d06ab29694a19cbec7eed107a8019
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764691"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a>Sie können einen Artikel nicht mithilfe der Entität „Freigegebene Produkte V2“ importieren

KB-Nummer: 4611825

## <a name="symptoms"></a>Symptome

Wenn Sie versuchen, einen Artikel mithilfe der Entität *Freigegebene Produkte V2* zu importieren, erhalten Sie eine Fehlermeldung, die dem folgenden Beispiel ähnelt:

> In „Artikel – Rückverfolgungsangabengruppen“ kann kein Datensatz erstellt werden (EcoResTrackingDimensionGroupItem). Artikelnummer: 2040663, Charge. Der Datensatz ist bereits vorhanden.

## <a name="resolution"></a>Lösung

Um neu freigegebene Produkte zu importieren, müssen Sie die Entität *Erstellung eines freigegebenen Produkts V2* anstelle der Entität *Freigegebene Produkte V2* verwenden.
