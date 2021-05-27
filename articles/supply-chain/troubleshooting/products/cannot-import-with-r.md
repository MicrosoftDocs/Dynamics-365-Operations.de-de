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
ms.openlocfilehash: 8182f2f83f6a3e4cf54fe6fa64b25a2f461ff541
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026533"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a>Sie können einen Artikel nicht mithilfe der Entität „Freigegebene Produkte V2“ importieren

KB-Nummer: 4611825

## <a name="symptoms"></a>Symptome

Wenn Sie versuchen, einen Artikel mithilfe der Entität *Freigegebene Produkte V2* zu importieren, erhalten Sie eine Fehlermeldung, die dem folgenden Beispiel ähnelt:

> In „Artikel – Rückverfolgungsangabengruppen“ kann kein Datensatz erstellt werden (EcoResTrackingDimensionGroupItem). Artikelnummer: 2040663, Charge. Der Datensatz ist bereits vorhanden.

## <a name="resolution"></a>Lösung

Um neu freigegebene Produkte zu importieren, müssen Sie die Entität *Erstellung eines freigegebenen Produkts V2* anstelle der Entität *Freigegebene Produkte V2* verwenden.
