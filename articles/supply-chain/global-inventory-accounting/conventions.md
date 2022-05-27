---
title: Konventionen
description: Dieses Thema beschreibt, wie Sie Konventionen festlegen, um zu bestimmen, wie die Kalkulation in der Globalen Bestandsbuchhaltung erfolgen soll.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4919d8fcab76741175bad6ea090eea61d4146fa8
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673157"
---
# <a name="conventions"></a>Konventionen

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 4/30/2022 -->

Eine Konvention ist ein Container für eine Reihe von Richtlinien, die das Systemverhalten beeinflussen. Basierend auf Ihren geschäftlichen Anforderungen müssen Sie Konventionen definieren, indem Sie eine Kombination der verschiedenen Richtlinien verwenden, die festlegen, wie Kosten in der Globalen Bestandsbuchhaltung kalkuliert werden sollen. Sie können jede Konvention mit einem oder mehreren Sachkonten verknüpfen, um die Konsistenz der Richtlinien zu gewährleisten, die in allen Sachkonten angewendet werden.

Um Ihre Konventionen einzurichten, gehen Sie auf **Globale Bestandsbuchhaltung \> Einrichten \> Konventionen**. Legen Sie für jede Konvention die folgenden Felder fest:

- **Name** – Geben Sie den Namen der Konvention ein.
- **Beschreibung** – Geben Sie eine Beschreibung der Konvention ein.
- **Kostenobjekt-Richtlinie** – Wählen Sie eine Richtlinie für das Kostenobjekt. Diese Richtlinien bestimmen die Granularität, die das System zur Berechnung und Pflege des Bestandswertes anwendet. Die folgenden vordefinierten Optionen sind verfügbar:

    - Produkt
    - Produkt – Standort
    - Produkt – Standort – Lagerort

    Wenn Sie z.B. *Produkt – Standort* wählen, berechnet und pflegt das System bei jeder Bestandsbewegung (Zu- oder Abgang) die Produktkosten jedes Bestands auf Standortebene. Daher haben Bestandsbewegungen auf niedrigeren Ebenen, wie z.B. der Ebene des Lagerorts, keinen Einfluss auf den Bestandswert. (Ein Beispiel für eine Umlagerung auf Lagerebene ist eine Artikelumlagerung zwischen zwei Lagerorten in einem Betrieb). Ebenso können Sie die Kalkulation des Bestands auf einer niedrigeren Ebene, wie z. B. der Ebene des Lagerorts, nicht anzeigen.

- **Richtlinie für die Basis der Messungen** – Wählen Sie eine Richtlinie für die Basis der Messungen. Diese Richtlinien bestimmen die Kosten, die in das Bestandskonto fließen sollen, und die Kosten, die berechnet werden sollen. Die folgenden Optionen sind für Firmen im Handel relevant:

    - **Normal historisch** – Alle Kostenelemente fließen in das Bestandskonto.
    - **Standard** – Standardkosten fließen in die Bestandskonten, und die Differenz zwischen den angesetzten Kosten und den tatsächlichen Kosten wird auf Abweichungskonten belastet. Wenn Sie eine Richtlinie für die *Standard*-Eingangsmessung erstellen möchten, müssen Sie zunächst eine Preisliste erstellen, in der die Richtlinie die Standardkosten des Elements nachschlagen kann.
    - **Preislisten** – Die Globale Bestandsbuchhaltung unterstützt das Abrufen von Artikelpreisen von mehreren juristischen Entitäten. Sie können eine Preisliste definieren, die von der Richtlinie für die Eingabe der Messungen verwendet wird. Auf diese Weise weiß das System, wo es den Artikelpreis nachschlagen muss. Gehen Sie wie folgt vor, um Preislisten festzulegen:

        1. Geben Sie im Feld **Name** einen Namen ein.
        1. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
        1. Wählen Sie im Feld **Kalkulationsart** eine Kalkulationsart (*Standardkosten* oder *Plan-Kosten*).
        1. Wählen Sie im Feld **Preistyp** eine Preisart aus (*Kosten*, *Kauf* oder *Verkaufspreis*).
        1. Fügen Sie eine Version der Kalkulation hinzu.
        1. Wählen Sie im Aktionsbereich **Preis**, um die Artikelpreise in der Preisliste zu validieren.

- **Richtlinie zur Übernahme von Kostenflüssen** – Wählen Sie eine Richtlinie zur Übernahme von Kostenflüssen. Diese Richtlinien bestimmen, wie die Kosten aus dem Bestand entfernt und als Kosten der verkauften Waren ausgewiesen werden. Die folgenden vordefinierten Optionen sind verfügbar:

    - Durchschnitt
    - Spezifisch – Batch

    > [!NOTE]
    > Die Globale Bestandsbuchhaltung ist ein System der permanenten Inventur. Daher verfolgt das System den Wert des Bestands auf der Basis einzelner Transaktionen.

- **Kostenartenrichtlinie** – Sie können Richtlinien für Kostenarten definieren und mit diesem Feld verknüpfen. Ein *Kostenelement* ist die Kalkulation einer Ressource, die durch ein Ereignis verbraucht wird. Sie können Kostenelemente verwenden, um Kosten zu verfolgen und zu kategorisieren. Um Richtlinien für Kostenelemente zu erstellen, geben Sie Informationen an den folgenden Stellen ein:

    - **Feld Name**
    - **Beschreibung** Feld
    - **Kostenelement** Liste
    - **Regeln** Raster

    Wenn Sie den Wert des Bestandes nicht weiter aufschlüsseln wollen, müssen Sie trotzdem eine Kostenartenliste erstellen, die eine einzelne Kostenart enthält. Anschließend müssen Sie eine Richtlinie für die Kostenarten erstellen, um alle relevanten Messungen (Kostenelemente) dieser Kostenart zuzuordnen.
