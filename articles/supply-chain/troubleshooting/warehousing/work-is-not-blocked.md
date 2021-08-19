---
title: Arbeit ist nicht blockiert
description: Arbeit ist nicht blockiert
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 6b4361682246397732e8326b98b1b86ff878664e54c8c352296b0d7eaff6bbbd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719550"
---
# <a name="work-isnt-blocked"></a>Arbeit ist nicht blockiert

Fehlercode: WHSUnblockNotBlockedWorkErrorMessage

## <a name="symptoms"></a>Symptome

Das System zeigt die folgende Fehlermeldung an:

> Arbeit mit Id %1 ist nicht blockiert.

## <a name="cause"></a>Ursache

Die Option **Blockierte Welle** auf der Welle wird auf *Nein* festgelegt. Die Arbeit kann nicht entsperrt werden, da sie derzeit nicht gesperrt ist.

## <a name="resolution"></a>Lösung

 Nur Arbeiten, bei denen die Option **Blockierte Welle** auf *Ja* festgelegt ist, können entsperrt werden.
