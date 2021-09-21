---
title: Kennzeichen kann nicht verschoben werden, wenn leere Ausgabe und leere Quittung erlaubt
description: Sie können ein Kennzeichen nicht verschieben, wenn die Seriennummer eine leere Ausgabe und eine leere Quittung erlaubt. Dies wird behoben, indem das Seriennummernfeld optional gemacht wird.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0047f79aa417c8fc910447505f07963d014f54e7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476436"
---
# <a name="cant-move-license-plate-if-serial-number-has-blank-issue-and-blank-receipt-allowed"></a>Kennzeichen kann nicht verschoben werden, wenn die Seriennummer eine leere Ausgabe und eine leere Quittung erlaubt.

## <a name="symptoms"></a>Symptome

Sie können ein Kennzeichen nicht mit dem Menüelement **Verschieben** verschieben, wenn die Seriennummer die Einstellungen *Leere Ausgabe erlaubt* und *Leere Quittung erlaubt* in der Rückverfolgungsangabengruppe hat und wenn sich mehrere Kennzeichen an demselben Lagerplatz befinden, von denen einige Seriennummern haben und einige nicht.

## <a name="resolution"></a>Lösung

Dieses Problem wird durch Änderungen behoben, die in [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687) bereitgestellt werden. Diese Änderungen machen das Feld **Seriennummer** optional, wenn leere Quittungen und leere Ausgaben erlaubt sind.
