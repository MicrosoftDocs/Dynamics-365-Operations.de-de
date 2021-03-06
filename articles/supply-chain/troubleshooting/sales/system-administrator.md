---
title: Systemadministratoren können Auftragssperren nicht löschen, da sie nicht dazu autorisiert sind
description: Systemadministratoren können Auftragssperren nicht löschen, da sie nicht dazu autorisiert sind.
author: SmithaNataraj
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: acabd6409d9b2860535335bc648bcc34304e0cb0
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026558"
---
# <a name="system-administrators-cant-clear-order-holds-because-they-arent-authorized"></a>Systemadministratoren können Auftragssperren nicht löschen, da sie nicht dazu autorisiert sind

KB-Nummer: 4614642

## <a name="symptoms"></a>Symptome

Systemadministratoren können Auftragssperren nur löschen, wenn sie die spezifische Rolle haben, die im Auftragssperrcode zugewiesen ist.

## <a name="resolution"></a>Lösung

Der Zugriff auf manche Vorgänge, z. B. das Löschen von Auftragssperren, wird durch die Einrichtung einer Geschäftsrichtlinie gesteuert. Systemadministratoren dürfen normalerweise keine Vorgänge dieses Typs ausführen. 

Häufiger wird der Zugriff zur Ausführung einer bestimmten Aufgabe durch Geschäftsrichtlinien geregelt, und nur bestimmte Personen in einer Organisation sind zur Ausführung dieser Aufgabe berechtigt. Beispiele hierfür sind Genehmigungen, die aus Workflow-Genehmigungen stammen, und bestimmte Aufgaben, die aus einer Workflow-Konfiguration stammen.

Obwohl mit Auftragssperren kein Workflow verbunden ist, ist das Prinzip ähnlich. Eine relevante Rolle bezeichnet die spezifische Gruppe von Personen in einer Organisation, die das Recht haben, Auftragssperren zu löschen. Dieses Recht sollte nicht unbedingt allen Administratoren gewährt werden, da dieser Ansatz gegen die festgelegte Geschäftsrichtlinie verstößt.
