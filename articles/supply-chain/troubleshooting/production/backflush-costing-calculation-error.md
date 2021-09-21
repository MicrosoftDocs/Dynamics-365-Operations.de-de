---
title: Fehler bei der Nachkalkulation für Produktionskosten beim Bestandsabschluss
description: In früheren Versionen haben Sie beim Bestandsabschluss möglicherweise einen Fehler bei der Nachkalkulation für Produktionskosten erhalten. Dieses Problem wurde behoben.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ae92b7121998d6b1ba2f08ea5736c55637867fbf
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476429"
---
# <a name="backflush-costing-calculation-error-during-inventory-closing"></a>Fehler bei der Nachkalkulation für Produktionskosten beim Bestandsabschluss

## <a name="symptoms"></a>Symptome

In Versionen vor 10.0.13 erhalten Sie beim Bestandsabschluss die folgende fehlerhafte Warnmeldung, wenn Sie nicht den Lean Production Costing Flow verwenden:

> Sie sind dabei, einen Bestandsabschluss mit einem Datum %1 auszuführen. Es wurde keine Ausführung einer Nachkalkulation mit einem Datum %1 registriert, das dem Periodenende entspricht. Bitte denken Sie daran, eine Nachkalkulation mit einem Datum %1 auszuführen, das dem Periodenende entspricht. Die Bewertung der Bestände, des Wareneinsatzes und der Abweichungen sind im Neben- oder Hauptbuch möglicherweise nicht korrekt, bis dies ausgeführt wurde.

## <a name="resolution"></a>Lösung

Dieses Problem wurde in Version 10.0.13 und später behoben. Weitere Informationen finden Sie in [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).
