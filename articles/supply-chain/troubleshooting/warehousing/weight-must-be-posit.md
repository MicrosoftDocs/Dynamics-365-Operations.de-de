---
title: Gewicht muss positiv sein
description: Gewicht muss positiv sein
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSContainerCloseDiag_canClose
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dcbcde3143cb509b68b277cb7c709263e2659b5b
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924302"
---
# <a name="weight-must-be-positive"></a>Gewicht muss positiv sein

Fehlercode: WeightMustBePositive

## <a name="symptoms"></a>Symptome

Das System zeigt die folgende Fehlermeldung an:

> Das Gewicht muss positiv sein.

## <a name="cause"></a>Ursache

Das Feld **Bruttogewicht** wird auf *0* (Null) oder einen negativen Wert festgelegt.

## <a name="resolution"></a>Lösung

Um eine Gewichtung festzulegen, führen Sie einen der folgenden Schritte aus.

- Legen Sie im Feld **Bruttogewicht** einen Wert fest. Wählen Sie dann eine Einheit in der Dropdown-Liste.
- Wählen Sie **Systemgewicht abrufen**, um den Wert **Bruttogewicht** zu berechnen.
