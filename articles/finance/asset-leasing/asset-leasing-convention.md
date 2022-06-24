---
title: Konventionen beim Anlagenleasing
description: Dieser Artikel beschreibt die Konventionen für Leasingobjekte.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: f2f0e21b20a969c0847ce3a6eb167287c1d7ee3e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898268"
---
# <a name="asset-leasing-conventions"></a>Konventionen beim Anlagenleasing

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dieser Artikel beschreibt die Konventionen für Leasingobjekte. Leasingkonventionen werden verwendet, um das Anfangsdatum eines Leasingbuchs zu bestimmen. Wenn die Leasingkonvention auf **Keine** festgelegt ist, entspricht das Anfangsdatum dem Startdatum des Mietvertrags (also dem Wert des **Mietbeginn**-Feldes). Wenn die Leasingkonvention auf **Voller Monat** festgelegt ist, ist das Anfangsdatum der erste Tag des Monats, in den das Startdatum des Mietvertrags fällt.

Das Anfangsdatum bestimmt das Startdatum des Zeitraums für die Zeitpläne zur Amortisierung von Leasingverbindlichkeiten und zur Abschreibung von Leasingobjekten. Zinsaufwände und Abschreibungskosten werden am Periodenenddatum der entsprechenden Zeitpläne gebucht. Die anfängliche Erfassung und der Regulierungsjournaleintrag erfolgen am Anfangsdatum.

> [!NOTE]
> Die Funktion für Leasingkonventionen muss über die Funktionsverwaltung aktiviert werden. Suchen und wählen Sie im Arbeitsbereich **Funktionsverwaltung** die Funktion namens **Leasingkonvention für das Anlagenleasing** aus. Wählen Sie anschließend **Jetzt aktivieren** aus.

Leasingkonventionen werden der Einrichtung eines Mietobjektbuchs zugewiesen.

Führen Sie die folgenden Schritte aus, um die Leasingkonvention anzuzeigen oder zuzuweisen.

1. Wechseln Sie zu **Anlagenleasing \> Einrichtung \> Leasingbücher**.
2. Wählen Sie im Feld **Leasingkonvention** einen der folgenden Werte aus.

    | Leasingkonvention | Beschreibung |
    |--------------------|-------------|
    | Keines               | Die Zeitpläne für die Amortisierung von Verbindlichkeiten und die Abschreibung von Leasingobjekten beginnen am Startdatum des Mietvertrags, da das Anfangsdatum dem Startdatum des Mietvertrags entspricht. Das Enddatum ist einen Monat später. Diese Leasingkonvention garantiert nicht, dass die Zinsen am letzten Tag eines jeden Monats verbucht werden. |
    | Ganzer Monat         | Bei Mietverträgen mit einem Startdatum, das auf einem beliebigen Zeitpunkt während des Monats liegt, beginnen die Zeitpläne für die Amortisierung von Verbindlichkeiten sowie die Abschreibung von Leasingobjekten am ersten Tag des Monats mit der Aufwandsabgrenzung. Diese Leasingkonvention gewährleistet, dass am letzten Tag eines jeden Monats für den gesamten Monat Zinsen abgegrenzt werden. |

3. Wählen Sie **Speichern** aus.

Wenn ein Mietvertrag erstellt wird, wird das Anfangsdatum jedes Buches automatisch basierend auf dem für den Mietvertrag eingegebenen Startdatum und der für das Buch angegebenen Leasingkonvention eingegeben.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
