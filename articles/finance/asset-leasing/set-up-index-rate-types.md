---
title: Indexraten einrichten
description: In diesem Thema wird erläutert, wie Sie Indexraten einrichten. Indexsätze sind erforderlich, wenn Ihre Organisation Mietzahlungsbeträge mit einer Reihe von Indexraten verknüpft.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 6424248e8d01d04720ad65e80aaa543b42abccc6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823022"
---
# <a name="set-up-index-rates"></a>Indexraten einrichten

[!include [banner](../includes/banner.md)]

Wenn Mietzahlungen von einem Index abhängen, können die Indexzinsarten hinzugefügt und im System verwaltet werden. Um die Mietzahlungen von der **Indexratentyp**-Seite neu zu bewerten, verwendet der Indexsatz-Neubewertungsprozess den neuesten Indexsatz ab dem Datum der Neubewertung.

Führen Sie die folgenden Schritte aus, um Indexratentypen und Indexraten hinzuzufügen.

1. Wechseln Sie zu **Anlagenleasing \> Einrichtung \> Indexratentypen**.
2. Wählen Sie **Neu** aus.
3. Geben Sie in die entsprechenden Felder den Ratentyp und den Namen der Indexrate ein.
4. Um einen neuen Indexratenwert hinzuzufügen, wählen Sie den Indexratentyp aus dann **Hinzufügen**.
5. Wählen Sie das effektive Startdatum der Rate und den Ratenwert.

Sie müssen entweder **Indexratenwertdifferenz** oder **Indexratenwert** als Indexratenmethode auswählen.

- Wählen Sie die **Indexratenwertdifferenz**-Methode zur Berechnung einer neuen Mietzahlung basierend auf der Differenz zwischen der Indexrate am Startdatum und der letzten Indexrate aus. Die Indexrate wird im **Indexrate (%)**-Feld definiert.
- Wählen Sie die **Indexratenwert**-Methode zur Berechnung der Mietzahlung unter Verwendung des im Feld **Indexrate (%)** Prozentsatzes aus.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]