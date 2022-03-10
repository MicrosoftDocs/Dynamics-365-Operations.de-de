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
ms.openlocfilehash: a89f5f98895be5b934dbdc1194fa58b9af34f9cbc7f5e2092f6f47791dd52400
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777742"
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
