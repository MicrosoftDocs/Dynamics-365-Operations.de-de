---
title: Verbindlichkeiten, Anlagen und Ausgabentransaktionen anzeigen
description: In diesem Thema wird erläutert, wie Sie Transaktionen für einen Leasingobjekt anzeigen. Diese Transaktionen umfassen Leasingverbindlichkeitstransaktionen und Transaktionen mit Ausführungskosten, die gebucht wurden.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 58a57b2a1237b41c99e44cf40c57d80257fc9b5b77188586aab6735a8a3f4984
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765739"
---
# <a name="view-liability-asset-and-expense-transactions"></a>Verbindlichkeiten, Anlagen und Ausgabentransaktionen anzeigen

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie Transaktionen für einen Leasingobjekt anzeigen. Diese Transaktionen umfassen Leasingverbindlichkeitstransaktionen und Transaktionen mit Ausführungskosten, die gebucht wurden. Die Buchwerte der Verbindlichkeit und des Nutzungsrechts am Leasingobjekt werden in mehreren Berichten verwendet. Sie werden auch zur Berechnung von Regulierungswerten verwendet.

## <a name="liability-transactions"></a>Verbindlichkeitstransaktionen

Um die Leasingverbindlichkeitstransaktionen anzuzeigen, wählen Sie einen Mietvertrag auf der **Mietvertragsübersicht**-Seite und dann **Bücher** aus, um die Bücher zu öffnen, die dem Mietvertragsdatensatz zugewiesen sind. Nachdem eine erstmalige Erfassung, eine Rechnung oder eine Zinserfassung gebucht wurde, wählen Sie **Verbindlichkeitstransaktionen** aus.

Die **Verbindlichkeitstransaktionen**-Seite zeigt die Transaktionen, die die Leasingverbindlichkeit erhöhen oder verringern. Negative Beträge auf dieser Seite repräsentieren Habentransaktionen in der Standardanwendung. Zinsabgrenzungen werden als negative Werte ausgewiesen und erhöhen die gesamte Leasingverbindlichkeit. Alle Mietvertragsregulierungen werden je nach Art und Auswirkung des Leasingbuchs als positive oder negative Werte angezeigt. Der aktuelle Nettosaldo der Leasingverbindlichkeit für den ausgewählten Mietvertrag wird unten links auf der Seite angezeigt.

## <a name="asset-transactions"></a>Anlagenbuchungen

Um die Mietanlagentransaktionen anzuzeigen, wählen Sie einen Mietvertrag auf der **Mietvertragsübersicht**-Seite und dann **Bücher** aus, um die Leasingbücher zu öffnen, die dem Mietvertragsdatensatz zugewiesen sind. Wählen Sie dann **Anlagentransaktionen** aus.

Die **Anlagentransaktion**-Seite zeigt die Transaktionen, die die Mietanlage und die kumulierten Abschreibungskonten entweder erhöhen oder verringern. Belastungen werden wie auf der **Verbindlichkeitstransaktionen**-Seite als positive Werte und Gutschriften als negative Werte angezeigt. Die gebuchte erstmalige Erfassung und die nächste kumulierte Abschreibung werden unten links auf der Seite als Anlagensaldo angezeigt. 

## <a name="expenses-transactions"></a>Ausgabentransaktionen

Um die Mietausgabentransaktionen anzuzeigen, wählen Sie einen Mietvertrag auf der **Mietvertragsübersicht**-Seite und dann **Bücher** aus, um die Leasingbücher zu öffnen, die dem Mietvertragsdatensatz zugewiesen sind. Wählen Sie dann **Ausgabentransaktionen** aus.

Die **Ausgabentransaktionen**-Seite werden alle Ausgaben angezeigt, die auf den Mietvertrag gebucht wurden, z. B. Zinsaufwendungen, Abschreibungsaufwendungen und etwaige Nebenkosten beim Leasing.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
