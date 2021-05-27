---
title: Der Lagerort in der Kommissionierlistenerfassung wird in einer Stücklistenposition nicht aktualisiert.
description: Der Lagerort in der Kommissionierlistenerfassung wird in einer Stücklistenposition nicht aktualisiert.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5d24c0b8538f3894fd1d2a3edb3a6ed8633c9609
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026532"
---
# <a name="the-warehouse-in-the-picking-list-journal-isnt-updated-on-a-bom-line"></a>Der Lagerort in der Kommissionierlistenerfassung wird in einer Stücklistenposition nicht aktualisiert

KB-Nummer: 4614848

## <a name="symptoms"></a>Symptome

Der Lagerort in der Kommissionierlistenerfassung wird in einer Stücklistenposition nicht aktualisiert.

## <a name="resolution"></a>Lösung

Das System verhält sich wie vorgesehen. Wenn eine Kommissionierlisten-Erfassungsposition erstellt wird, die einen Verweis (über die Loskennung) auf eine Produktionsstücklistenposition enthält, wird der Lagerort in der Produktionsstücklistenposition nicht aktualisiert, wenn die Lagerortdimension in der Produktions-Kommissionierlisten-Erfassungsposition später geändert wird.
