---
title: Auftrag konnte mit ausgehenden Lagervorgängen nicht freigegeben werden
description: Es gibt mehrere Gründe, warum Sie möglicherweise eine Fehlermeldung erhalten, dass ein Kundenauftrag nicht freigegeben werden konnte. Auf dieser Seite wird erklärt, warum und wie das Problem gelöst werden kann.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fca5ee1bc97545ea4de56d940fdedd320a6cfe84
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476459"
---
# <a name="sales-order-could-not-be-released-with-outbound-warehouse-operations"></a>Debitorenauftrag konnte mit ausgehenden Lagervorgängen nicht freigegeben werden

## <a name="symptoms"></a>Symptome

Bei der Arbeit mit ausgehenden Lagerortvorgängen erhalten Sie allenfalls die folgende Fehlermeldung:

> Auftrag konnte nicht freigegeben werden.

## <a name="cause"></a>Ursache

Dieses Problem kann aus mehreren Gründen auftreten. Zum Beispiel befindet sich der Auftrag in der Kreditverwaltung und es können keine Sendungen erstellt werden, bis eine gültige Postadresse für alle Verkaufszeilen, die mit einem Auftrag verbunden sind, eingegeben wurde. Oder es gibt eine Auftragssperre, die behoben werden muss, bevor der Auftrag für das Lagerort freigegeben werden kann. Dieser Halt kann auftragsspezifisch sein oder sich auf das Kundenkonto beziehen.

## <a name="resolution"></a>Lösung

Fügen Sie die Adresse auf dem Auftrag und den Auftragszeilen hinzu oder aktualisieren Sie sie, und geben Sie den Auftrag dann für das Lager frei. Aufträge können nur dann für das Lagerort freigegeben werden, wenn sie eine gültige Lieferadresse haben (gemäß dem Adressformat, das im Modul **Organisationsverwaltung** eingerichtet wurde).

Untersuchen Sie den Auftragsstopp und beheben Sie dann die Probleme. Entfernen Sie dann die Sperrung des Auftrags oder des Kunden und geben Sie den Auftrag für das Lagerort frei.
