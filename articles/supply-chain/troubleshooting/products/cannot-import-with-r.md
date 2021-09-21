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
ms.openlocfilehash: bf6eb0eb755de3f2842c235946bfd7ccad04ccf7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474723"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a>Sie können einen Artikel nicht mithilfe der Entität „Freigegebene Produkte V2“ importieren

KB-Nummer: 4611825

## <a name="symptoms"></a>Symptome

Wenn Sie versuchen, einen Artikel mithilfe der Entität *Freigegebene Produkte V2* zu importieren, erhalten Sie eine Fehlermeldung, die dem folgenden Beispiel ähnelt:

> In „Artikel – Rückverfolgungsangabengruppen“ kann kein Datensatz erstellt werden (EcoResTrackingDimensionGroupItem). Artikelnummer: 2040663, Charge. Der Datensatz ist bereits vorhanden.

## <a name="resolution"></a>Lösung

Um neu freigegebene Produkte zu importieren, müssen Sie die Entität *Erstellung eines freigegebenen Produkts V2* anstelle der Entität *Freigegebene Produkte V2* verwenden.
