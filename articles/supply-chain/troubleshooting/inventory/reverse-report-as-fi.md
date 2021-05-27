---
title: Die Stornierung der Fertigmeldung führt zu einer unerwarteten offenen Buchung
description: Durch die Stornierung der Fertigmeldung mit Kennzeichnung wird eine offene Buchung erstellt, bei der die stornierte Menge die gleichen Bestandsdimensionen wie die stornierte Buchung aufweist.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ea9044a9008e766c7fc92f98e27cfb91076f5b44
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026553"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a>Die Stornierung der Fertigmeldung führt zu einer unerwarteten offenen Buchung

KB-Nummer: 4612469

## <a name="symptoms"></a>Symptome

Wenn Sie die Fertigmeldung mit Kennzeichnung stornieren, erstellt das System eine offene Buchung, bei der die stornierte Menge die gleichen Bestandsdimensionen wie die stornierte Buchung aufweist.

## <a name="resolution"></a>Lösung

Wenn Sie einen als fertig gemeldeten Vorgang stornieren , wird die Bestandsdimension aus der Produktionserfassung initialisiert. Daher erhält es die Chargennummer. Aufgrund der Kennzeichnung erben die Auftragsbuchungen die Chargennummer.

Die Dimension kann zurückgesetzt werden, wenn die Fertigmeldung gebucht wird.
