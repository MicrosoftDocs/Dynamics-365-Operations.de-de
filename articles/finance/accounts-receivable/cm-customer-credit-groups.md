---
title: Debitorenkreditgruppen
description: Dieser Artikel enthält Informationen zu Debitorenkreditgruppen.
author: JodiChristiansen
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 032e92431946f0a41bf2e52c155e422d4ea0b3b7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886515"
---
# <a name="customer-credit-groups"></a>Debitorenkreditgruppen

[!include [banner](../includes/banner.md)]

Sie können Debitorengruppen mit geteilten Kreditlimit definieren. Das auf dem Debitorenrechnungskonto festgelegte individuelle Kreditlimit wird ebenfalls berücksichtigt.

Mitglieder einer Debitorenkreditgruppe können aus verschiedenen juristischen Personen ausgewählt werden. Wenn Sie der Liste der Debitoren in der Debitorenkreditgruppe einen Debitor hinzufügen, wird das Ablaufdatum des Kreditlimits für jeden Debitor in das Ablaufdatum geändert, das der Gruppe zugewiesen ist.

Sie können Debitorengruppen auf der Seite **Debitorenkreditgruppen** einrichten (**Kreditmanagement \> Debitorenkreditgruppen \> Debitorenkreditgruppen**).

1. Geben Sie in den Feldern **Gruppennummer** und **Beschreibung** einen Bezeichner und eine Beschreibung für die Gruppe ein.
2. Geben Sie in die Felder **Kreditlimit** und **Währung** das Kreditlimit und die Währung ein, die verwendet werden sollen, wenn das System das Kreditlimit für ein Mitglied der Gruppe überprüft.
3. Geben Sie im Feld **Kreditlimit bis Datum** das Datum ein, an dem das Kreditlimit abläuft. Die Kreditorenkreditgruppen müssen ein Ablaufdatum haben.

Nachdem Sie eine Kreditorenkreditgruppe eingerichtet haben, können Sie Kreditoren hinzufügen, indem Sie deren juristische Person und Kreditorenkonto-ID angeben. Wenn Sie einer Kreditorenkreditgruppe einen neuen Kreditor hinzufügen, sucht das System unter allen juristischen Personen nach demselben Kreditorenkonto und fordert Sie auf, es der Kreditorenkreditgruppe hinzuzufügen.

Verwenden Sie das Menü **Saldenrückblick**, um die Details des Saldenrückblicks für alle Rechnungskreditoren in einer Kreditorenkreditgruppe anzuzeigen. Die Seite **Saldenrückblick** zeigt eine Zusammenfassung der Saldenrückblicke für die Rechnungskreditorenkonten.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
