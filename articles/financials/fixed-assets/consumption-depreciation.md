---
title: Verbrauchsabschreibung
description: Dieser Artikel enthält eine Übersicht der Verbrauchsabschreibungsmethode.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13751
ms.assetid: d25a681f-49a5-4bfc-aa76-1c6373e35dd8
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2c9d95a7a45ed99c63516749285126c786685c87
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840696"
---
# <a name="consumption-depreciation"></a>Verbrauchsabschreibung

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält eine Übersicht der Verbrauchsabschreibungsmethode.

Wenn Sie beim Einrichten eines Anlagenabschreibungsprofils **Verbrauch** im Feld **Methode** auf der Seite **Abschreibungsprofile** auswählen, basiert die Abschreibung von Anlagen, die diesem Abschreibungsprofil zugeordnet sind, auf der Nutzung der jeweiligen Anlage. Sie müssen Prozentsätze und Intervalle nicht auf der Seite **Abschreibungsprofile** einrichten. Nach der Erstellung des Profils für die Methode "Verbrauch" kann die Methode auf vielfältige Weise eingerichtet werden.

## <a name="set-up-and-use-consumption-depreciation"></a>Einrichten und Nutzen der Verbrauchsabschreibung
1.  Erstellen Sie auf der Seite **Abschreibungsprofile** das Abschreibungsprofil. Für Verbrauchsberechnungen muss das Abschreibungsprofil eine Kennung und einen Namen besitzen, und **Verbrauch** muss im Feld **Methode** ausgewählt werden.
2.  Auf der **Verbrauchsfaktoren**-Seite richten Sie Verbrauchsfaktoren ein. Jeder Verbrauchsfaktor muss eine Kennung und einen Namen und einen Verbrauchsfaktor besitzen, der entweder als Menge oder Prozentsatz angegeben ist.
3.  Auf der **Verbrauchseinheiten**-Seite richten Sie Verbrauchseinheiten ein. Jede Verbrauchseinheit muss eine Kennung und einen Namen besitzen. Abschreibungseinheiten werden verwendet, um Verbrauchsabschreibung auf der Seite **Verbrauchsabschreibung** zu berechnen. Beispiele für Einheiten sind Kilometer (km), Kilogramm (kg) oder Stunde.
4.  Auf der **Anlagevermögen**-Seite richtet Sie einzelne Anlagen ein. Wählen Sie für jede Anlage Wertmodelle oder Abschreibungsbücher aus, die über Abschreibungsprofile verfügen. Sie müssen Wertmodelle oder Abschreibungsbücher für die Verbrauchsabschreibung einrichten, wenn Sie Anlagen haben, die Abschreibungsprofile verwenden, die auf der Methode "Verbrauch" basieren. Diese Einrichtung wird entweder auf der Registerkarte **Abschreibung** der Seite **Wertmodelle** oder auf dem Inforegister **Allgemeines** der Seite **Abschreibungsprofil** ausgeführt. Das gleiche Wertmodell kann für mehrere Anlagen verwendet werden. Abschreibungsprofile sind Teil des Wertmodells oder des Abschreibungsbuchs, das für jede Anlage ausgewählt wurde. Auf der Seite **Anlagen** können Abschreibungsprofile nicht direkt hinzufügen oder geändert werden. Sie können Abschreibungsprofile nur auf der Seite **Abschreibungsbücher** ändern.
5.  Geben Sie auf der Seite **Wertmodelle** oder **Abschreibungsbücher** in der Feldgruppe **Verbrauchsabschreibung** in den folgenden Feldern Daten ein:
    -   Verbrauchsfaktor
    -   Einheit
    -   Abschreibung pro Einheit
    -   Vorkalkulierter Verbrauch

    Das Feld**Gebuchter Verbrauch** enthält die Verbrauchsabschreibung (in Einheiten), die bereits für die Kombination aus Anlage und Wertmodell oder für das Abschreibungsbuch gebucht wurde. Sie können diesen Feldwert nicht manuell aktualisieren.

## <a name="examples"></a>Beispiele
### <a name="example-1"></a>Beispiel 1

Für den 31. Januar wird der folgende Verbrauchsfaktor eingerichtet:

-   Die Menge beträgt 1.000.
-   Die für die Anlage angegebene Abschreibung pro Einheit beträgt 1,5.

Der Abschreibungsvorschlag am 31. Januar lautet wie folgt: Menge × Abschreibung pro Einheit 1.000 × 1,5 = 1,500. Wenn der Faktor, der für die Anlage angegeben wird, ein Prozentsatz ist, wir die Menge im Feld **Vorkalkulierter Verbrauch** für das Wertmodell der Anlage mit dem Prozentsatz multipliziert, der für das ausgewählte Enddatum eingerichtet ist. Die resultierende Menge wird als Abschreibungsmenge für die Periode vorgeschlagen.

### <a name="example-2"></a>Beispiel 2

Für den 31. Januar wird der folgende Faktor für die Verbrauchsabschreibung eingerichtet:

-   Der Prozentsatz beträgt 10 Prozent.
-   Die für die Anlage angegebene Abschreibung pro Einheit beträgt 1,5.
-   Die vorkalkulierte Menge der Anlage ist 2.000.

Der Abschreibungsvorschlag am 31. Januar lautet wie folgt: Abschreibung pro Einheit × Prozentsatz × Abschreibung pro Einheit 2.000 × 0,10 × 1,5 = 300



