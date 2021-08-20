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
ms.openlocfilehash: 970930bbdd30b57a8374de7810bb3ece8cb19a7010b5ef19d90bfc39d09f172b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740550"
---
# <a name="the-warehouse-in-the-picking-list-journal-isnt-updated-on-a-bom-line"></a>Der Lagerort in der Kommissionierlistenerfassung wird in einer Stücklistenposition nicht aktualisiert

KB-Nummer: 4614848

## <a name="symptoms"></a>Symptome

Der Lagerort in der Kommissionierlistenerfassung wird in einer Stücklistenposition nicht aktualisiert.

## <a name="resolution"></a>Lösung

Das System verhält sich wie vorgesehen. Wenn eine Kommissionierlisten-Erfassungsposition erstellt wird, die einen Verweis (über die Loskennung) auf eine Produktionsstücklistenposition enthält, wird der Lagerort in der Produktionsstücklistenposition nicht aktualisiert, wenn die Lagerortdimension in der Produktions-Kommissionierlisten-Erfassungsposition später geändert wird.
