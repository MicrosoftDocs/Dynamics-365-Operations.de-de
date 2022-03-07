---
title: Geplanter Produktionsauftrag muss eingeplant werden, bevor er fixiert werden kann
description: Wenn Sie versuchen, einen geplanten Auftrag zu fixieren, erhalten Sie eine Fehlermeldung, die besagt, dass der Auftrag eingeplant werden muss, bevor er fixiert werden kann.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a360cb3cbd26e1bc1ebb1baf1a6a4d8282c28c5c
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294087"
---
# <a name="planned-production-order-must-be-scheduled-before-it-can-be-firmed"></a>Geplanter Produktionsauftrag muss eingeplant werden, bevor er fixiert werden kann

Fehlercode: SYS309802

## <a name="symptoms"></a>Symptome

Wenn Sie versuchen, einen geplanten Auftrag zu fixieren, erhalten Sie die folgende Fehlermeldung:

> Der geplante Produktionsauftrag muss geplant werden, bevor er umgewandelt werden kann.

## <a name="cause"></a>Ursache

Die geplanten Start- und Endtermine können nicht leer sein.

## <a name="resolution"></a>Lösung

Gehen Sie folgendermaßen vor, um Start- und Endtermine für den geplanten Auftrag festzulegen.

1. Gehen Sie zu **Produktprogrammplanung \> Gesamtplanung \> Geplante Aufträge**.
1. Öffnen Sie den betreffenden geplanten Auftrag.
1. Geben Sie auf dem Inforegister **Allgemein** im Abschnitt **Terminiert** die Daten in den Feldern **Startdatum** und **Enddatum** an.
