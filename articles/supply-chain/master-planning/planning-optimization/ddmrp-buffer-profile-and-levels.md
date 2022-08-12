---
title: Pufferprofil und Ebenen
description: Dieser Artikel enthält Informationen zu Pufferprofilen und -niveaus, die die Mindest- und Höchstbestände festlegen, die für jeden Entkopplungspunkt gehalten werden sollten.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ReqItemDecoupledLeadTime
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: dd72332abefd31fd391ff66931a5abae0efb08de
ms.sourcegitcommit: 529fc10074b06f4c4dc52f2b4dc1f159c36e8dbc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/22/2022
ms.locfileid: "9186664"
---
# <a name="buffer-profile-and-levels"></a>Pufferprofil und Ebenen

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Nachdem Sie Ihre Entkopplungspunkte identifiziert haben (wichtige Artikel, die Sie strategisch auf Lager halten werden), müssen Sie entscheiden, wie viel Bestand (Puffer) Sie an jedem dieser Punkte halten werden. Diese Aufgabe ist der zweite Schritt der bedarfsgesteuerten Materialressourcenplanung (DDMRP).

## <a name="buffer-levels-and-zones"></a>Pufferebenen und Zonen

In DDMRP wird jeder Bestandspuffer durch drei Werte definiert: die Mindestmenge, die Höchstmenge und den Neubestellungspunkt. Diese Werte bilden drei Differenzzonen, die durch die folgenden Farbcodes gekennzeichnet sind:

- **Rote Zone** – Der Bereich unterhalb der Mindestmenge. Die Mindestmenge wird auch als „top of red“ bezeichnet, und Ihre Planungsstrategie sollte so angelegt sein, dass die Bestände immer über diesem Punkt liegen.
- **Gelbe Zone** – Der Bereich zwischen der Mindestmenge und dem Neubestellungspunkt. Der Neubestellungspunkt wird auch als „top of yellow“ bezeichnet. Wenn dieser Punkt erreicht ist, sollte das System eine Neuordnung vornehmen.
- **Grüne Zone** – Der Bereich zwischen dem Neubestellungspunkt und der Höchstmenge. Die maximale Menge wird auch als „Top of Green“ bezeichnet. Dieser Punkt ist der Höchststand, bis zu dem der Bestand wiederbeschafft werden kann.

Die folgende Abbildung zeigt die drei farbigen Zonen und wie sie sich auf die Mindestmenge, die Höchstmenge und den Neubestellungspunkt beziehen.

![DDMRP Pufferzonen und -ebenen.](media/ddmrp-buffer-levels.png "DDMRP Pufferzonen und -ebenen")

## <a name="calculating-the-buffer-zones"></a>Berechnen Sie die Pufferzonen

Dieser Abschnitt erklärt, wie die Höhe der einzelnen Pufferzonen berechnet wird.

Die gelbe Zone wird normalerweise zuerst berechnet. Diese Zone steht für die Menge, die Sie vom Zeitpunkt der Bestellung bis zum Eintreffen der Bestellung verbrauchen. Mit anderen Worten, es handelt sich um den erwarteten Verbrauch während der Vorlaufzeit der Wiederbeschaffung. Er wird mit Hilfe der folgenden Gleichung berechnet:

- **Gelbe Zone** = *Der durchschnittliche tägliche Verbrauch (ADU)* × *Entkoppelte Vorlaufzeit*

Die *Entkoppelte Vorlaufzeit* stellt die Zeit dar, die benötigt wird, um einen Artikel zu produzieren oder zu erhalten, wenn die Entkopplungspunkte immer auf Lager sind. Sie ist normalerweise viel kürzer als die *kumulierte Vorlaufzeit*, die traditionell in der Produktprogrammplanung verwendet wird. Korrekte Puffereinstellungen sind der Schlüssel, um sicherzustellen, dass die Entkopplungspunkte immer tatsächlich auf Lager sind, aber nicht überbestückt werden.

Die rote Zone wird mit Hilfe der folgenden Gleichungen berechnet:

- **Rote Basis** = *ADU* × *Entkoppelte Vorlaufzeit* × *Vorlaufzeitfaktor*
- **Rote Sicherheit** = *Rote Basis* × *Variabilitätsfaktor*
- **Rote Zone** = *Rote Basis* + *Rote Sicherheit*

Die grüne Zone wird als das maximale Ergebnis der folgenden drei Gleichungen berechnet:

- *Minimale Auftragsmenge*
- *ADU* × *Auftragszyklus*
- *ADU* × *Entkoppelte Vorlaufzeit* × *Vorlaufzeitfaktor*

## <a name="calculating-average-daily-usage"></a>Berechnung des durchschnittlichen täglichen Verbrauchs

Das System verwendet einen der drei Ansätze, um die Menge zu berechnen, die Sie pro Tag verbrauchen:

- **Durchschnittlicher täglicher Verbrauch (rückwärts)** – Dieser Ansatz basiert auf dem tatsächlichen Verbrauch in der Vergangenheit.
- **Durchschnittlicher täglicher Verbrauch (vorwärts)** – Dieser Ansatz basiert auf dem geplanten zukünftigen Verbrauch.
- **Durchschnittlicher täglicher Verbrauch (gemischt)** – Dieser Ansatz basiert auf einer gewichteten Mischung aus vergangenem und geplantem Verbrauch.

### <a name="average-daily-usage-past"></a>Durchschnittlicher täglicher Verbrauch (rückwärts)

Die ADU der Vergangenheit wird als Durchschnitt berechnet, indem die Mengen, die jeden Tag für eine bestimmte Anzahl vergangener Tage verbraucht wurden, addiert und dann durch die Anzahl der Tage geteilt werden. Die folgende Abbildung zeigt, wie dieser Ansatz funktioniert, wenn die Berechnung drei Tage in die Vergangenheit blickt.

![Durchschnittlicher täglicher Verbrauch (rückwärts) Diagramm.](media/ddmrp-adu-past.png "Diagramm durchschnittlicher täglicher Verbrauch (rückwärts)")

Wenn heute der Morgen des 11. Juni ist, beträgt die ADU für die vorangegangenen drei Tage (8., 9. und 10. Juni) 21.

- **ADU (Vergangenheit)** = (29 + 11 + 23) ÷ 3 = 21

### <a name="average-daily-usage-forward"></a>Durchschnittlicher täglicher Verbrauch (vorwärts)

Bei einem neuen Produkt haben Sie möglicherweise keine Daten zur Nutzung in der Vergangenheit. Verwenden Sie daher stattdessen die voraussichtliche ADU für die Zukunft (z.B. auf der Grundlage des geplanten Bedarfs). Die folgende Abbildung zeigt, wie dieser Ansatz funktioniert, wenn die Berechnung drei Tage in die Zukunft reicht (einschließlich heute).

![Durchschnittlicher täglicher Verbrauch (vorwärts) Diagramm.](media/ddmrp-adu-forward.png "Diagramm durchschnittlicher täglicher Verbrauch (vorwärts)")

Wenn in der vorherigen Abbildung heute der Morgen des 11. Juni ist, beträgt die ADU für die nächsten drei Tage (11., 12. und 13. Juni) 21,66.

- **ADU (vorwärts)** = (18 + 18 + 29) ÷ 3 = 21,66

### <a name="average-daily-usage-blended"></a>Durchschnittlicher täglicher Verbrauch (gemischt)

Der gemischte ADU kombiniert den durchschnittlichen Verbrauch in der Vergangenheit und den durchschnittlichen Verbrauch in der Zukunft, wie in der folgenden Abbildung dargestellt.

![Der durchschnittliche tägliche Verbrauch (gemischt)](media/ddmrp-adu-blended.png "Diagramm durchschnittlicher täglicher Verbrauch (gemischt)").

Wenn heute der Morgen des 11. Juni ist, beträgt die gemischte ADU für die vorangegangenen und die folgenden drei Tage (8. bis 13. Juni) 21,33, wie in der vorherigen Abbildung gezeigt.

- **ADU gemischt** = (*ADU Vergangenheit* + *ADU vorwärts*) ÷ 2<br>= (21 + 21,66) / 2<br>= 21,33

## <a name="buffer-calculation-factors"></a>Faktoren für die Pufferberechnung

Für jeden Artikel können Sie zwei Faktoren festlegen, um die Größe der roten und grünen Zonen anzupassen. Auf diese Weise können Sie die erwartete Vorlaufzeit und die Schwankungen des Bedarfs ausgleichen.

![Vorlaufzeit und Variabilitätsfaktoren.](media/ddmrp-zone-factors.png "Vorlaufzeit und Variabilitätsfaktoren")

Der erste Faktor ist der *Faktor Vorlaufzeit*. Der Wert ist ein Dezimalwert von 0 bis 1. Je länger die Vorlaufzeit ist, desto niedriger sollte der Wert sein. Das Demand Driven Institute empfiehlt die folgenden Bereiche:

- **Lange Vorlaufzeit:** 0,20-0,40
- **Mittlere Vorlaufzeit:** 0,41-0,60
- **Kurze Vorlaufzeit:** 0,61-1,00

Der zweite Faktor ist der *Variabilitätsfaktor*. Der Wert ist ein Dezimalwert von 0 bis 1. Je höher die Variabilität des Bedarfs ist, desto niedriger sollte der Wert sein. Das Demand Driven Institute empfiehlt die folgenden Bereiche:

- **Geringe Variabilität:** 0,20-0,40
- **Mittlere Variabilität:** 0,41-0,60
- **Hohe Variabilität:** 0,61-1,00

## <a name="buffer-calculation-examples"></a>Beispiele für Pufferberechnungen

Dieses Beispiel setzt das Beispiel für die Kissenproduktion fort, das in [Bestandspositionierung](ddmrp-inventory-positioning.md) enthalten ist. In diesem Beispiel haben Sie Entkopplungspunkte ausgewählt, die die Vorlaufzeit von 21 Tagen auf fünf Tage reduziert haben, wie in der folgenden Abbildung dargestellt.

![Beispiel für eine entkoppelte Vorlaufzeit.](media/ddmrp-bom-decoupled-lead-time-example.png "Beispiel für eine entkoppelte Vorlaufzeit")

Nehmen Sie für dieses Beispiel an, dass der ADU mit 23 Stück berechnet wurde und die entkoppelte Vorlaufzeit, wie in der vorherigen Abbildung gezeigt, fünf Tage beträgt. Anhand dieser Werte können Sie die gelbe Zone mit Hilfe der folgenden Gleichung berechnen:

- **Gelbe Zone** = *ADU* × *Entkoppelte Vorlaufzeit* = 115

![Beispiel für die Berechnung der gelben Zone.](media/ddmrp-example-calc-yellow.png "Beispiel für die Berechnung der gelben Zone")

Die Berechnung der roten Zone ähnelt der Berechnung der gelben Zone, aber sie ist um die Variabilität und die Vorlaufzeit ergänzt. Nehmen Sie für dieses Beispiel an, dass Sie eine mittlere Vorlaufzeit (Faktor = 0,50) und eine hohe Variabilität des Bedarfs (Faktor = 0,8) beobachtet haben. Wenn Sie diese Werte zusammen mit den Komponenten aus der Gleichung für die gelbe Zone verwenden, können Sie die rote Zone mit Hilfe der folgenden Gleichungen berechnen:

- **Rote Basis** = *ADU* × *Entkoppelte Vorlaufzeit* × *Vorlaufzeitfaktor* = 57,5
- **Rote Sicherheit** = *Rote Basis* × *Variabilitätsfaktor* = 46
- **Rote Zone** = *Rote Basis* + *Rote Sicherheit* = 103,5

Das System rundet die rote Zone auf 104 Stück (ea), da die Stücke in ganzen Zahlen gezählt werden.

![Beispiel für die Berechnung der roten Zone.](media/ddmrp-example-calc-red.png "Beispiel für die Berechnung der roten Zone")

Die Berechnung der grünen Zone umfasst ebenfalls die Komponenten aus der Gleichung für die gelbe Zone, lässt aber eine Mindestbestellmenge, einen Auftragszyklus und einen Faktor für die Vorlaufzeit zu. Nehmen Sie für dieses Beispiel an, dass es keinen Bestellzyklus gibt (Sie haben also keine zeitlichen Beschränkungen hinsichtlich der Bestellhäufigkeit) und die Mindestbestellmenge 10 Stück beträgt. Die grüne Zone wird dann als maximales Ergebnis der folgenden drei Gleichungen berechnet:

- *Mindestbestellmenge* = 10
- *ADU* × *Auftragszyklus* = 0
- *ADU* × *Entkoppelte Vorlaufzeit* × *Vorlaufzeitfaktor* = 57,5

Das System rundet die grüne Zone auf 58 Stück (ea), da die Stücke in ganzen Zahlen gezählt werden.

![Beispiel für eine rot-grüne Berechnung.](media/ddmrp-example-calc-green.png "Beispiel für die Berechnung der grünen Zone")

Die folgende Abbildung fasst die Ergebnisse der Zonenberechnung mit Hilfe der Trichtergrafik zusammen, die häufig in DDMRP verwendet wird.

![Zusammenfassung der Zonenberechnungsergebnisse](media/ddmrp-example-calc-summary.png "Zusammenfassung der Ergebnisse der Zonenberechnung").

## <a name="dynamic-adjustments"></a><a name="dynamic-adjustments"></a>Dynamische Anpassungen

Dynamische Anpassungen ermöglichen Ihnen die Anwendung eines *Bedarfsanpassungsfaktors* in Zeiten mit hohem oder niedrigem Bedarf. Dieser Faktor multipliziert die ADU in allen Berechnungen für den ausgewählten Zeitraum. Die Pufferzonen werden dann der Reihe nach geändert. In der Regel wenden Sie diesen Faktor an, nachdem Sie Ihre anfänglichen Pufferwerte generiert haben, sodass Sie diese im Laufe der Zeit und als Reaktion auf veränderte Bedingungen feinabstimmen können. Diese Aufgabe ist der dritte Schritt der DDMRP.

Im August könnte es beispielsweise mehr Bedarf an einem Kissenprodukt geben, da die Menschen dann in den Urlaub fahren. Daher werden die Umsätze voraussichtlich höher ausfallen. In diesem Fall können Sie den Wert **Bedarfsanpassungsfaktor** für das Produkt auf *1,5* für alle Wochen im August ändern.

Auf diese Weise können Sie Pufferwerte im Laufe der Zeit berechnen und sie dann auf der Grundlage von mehr als nur den Informationen, die das System hat, anpassen. In einer vollständigen Implementierung von DDMRP werden Sie jeden Tag neue Pufferwerte über einen Batchauftrag berechnen und die Werte automatisch übernehmen. Sie werden dann die Planung als Batchauftrag ausführen und die geplanten Aufträge täglich überprüfen, um die Puffer wieder aufzufüllen.

## <a name="implement-buffers-in-supply-chain-management"></a>Implementierung von Puffern im Supply Chain Management

Dieser Abschnitt beschreibt, wie Sie Ihre Pufferzonenstrategie in Microsoft Dynamics 365 Supply Chain Management implementieren. Es wird davon ausgegangen, dass Sie die Analysen und Berechnungen, die in der ersten Hälfte dieses Artikels beschrieben werden, bereits durchgeführt haben.

### <a name="set-up-buffers-for-a-decoupling-point-item"></a><a name="set-up-buffers"></a>Puffer für einen Artikel des Entkopplungspunkts festlegen

Führen Sie diese Schritte aus, um Pufferwerte für einen Entkopplungspunkt festzulegen.

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Wählen Sie einen zugelassenen Artikel, der als Entkopplungspunkt festgelegt ist. (Weitere Informationen finden Sie unter [Positionierung von Beständen](ddmrp-inventory-positioning.md)).
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Plan** die Option **Artikelabdeckung**.
1. Wählen Sie auf der Seite **Artikelabdeckung** einen Datensatz zur Artikelabdeckung aus, der einen Entkopplungspunkt erstellt. (In diesem Datensatz wird der Name einer Abdeckungsgruppe angezeigt, die zum Erstellen von Entkopplungspunkten festgelegt ist.)
1. Wählen Sie die Registerkarte **Allgemein**.
1. Wenn Sie möchten, dass das System die Pufferwerte täglich oder wöchentlich neu berechnet, basierend auf Ihrer Verkaufshistorie, Ihren Planungen und den Einstellungen für die Deckungsgruppen, führen Sie die folgenden Schritte aus:

    1. Legen Sie die Option **Pufferwerte im Laufe der Zeit** auf *Ja* fest.
    1. Eine Nachricht weist Sie darauf hin, dass Ihre manuellen Puffereinstellungen (**Minimum**, **Neubestellungspunkt** und **Maximum**) zurückgesetzt werden, wenn Sie fortfahren. Wählen Sie **Ja**, um die neue Einstellung zu übernehmen.

    Wenn Sie es vorziehen, Ihre Puffereinstellungen nur einmal zu berechnen oder einzugeben, gehen Sie alternativ wie folgt vor:

    1. Legen Sie die Option **Pufferwerte im Laufe der Zeit** auf *Nein* fest.
    1. Legen Sie die Felder **Minimum**, **Neubestellungspunkt** und **Maximum** auf die Pufferwerte fest, die Sie für den Artikel berechnet haben, wie weiter oben in diesem Artikel beschrieben.

1. Legen Sie die folgenden Felder fest, um die DDMRP-Berechnungen für den Artikel abzuschließen:

    - **Bestellzyklus** – Geben Sie die Anzahl der Tage an, die zwischen den Bestellungen für den Artikel vergehen müssen. Legen Sie den Wert auf *0* (Null) fest, wenn keine Einschränkungen für die Reihenfolge bestehen. Dieses Feld wirkt sich auf den maximalen Mengenpuffer aus, wie bereits in diesem Artikel beschrieben.
    - **Durchschnittlicher täglicher Verbrauch** – Sie können optional einen geschätzten ADU für den Artikel eingeben. Dieses Feld dient nur zu Informationszwecken. Normalerweise wird der Wert automatisch als Teil der Pufferberechnungen berechnet.
    - **Schwellenwert für Bestellungsspitzen** – Geben Sie die Mindestanzahl der täglichen Verkäufe des Artikels an, die als Verkaufsspitze gelten (ungewöhnlich hoher Bedarf). Das System verwendet dieses Feld, um die Nachbestellmenge geplanter Aufträge in Perioden mit hohem Bedarf zu erhöhen. Weitere Informationen finden Sie unter [Bedarfsgesteuerte Planung](ddmrp-planning.md).

### <a name="calculate-or-enter-decoupled-lead-times"></a><a name="calc-lead-time"></a>Berechnen Sie entkoppelte Vorlaufzeiten oder geben Sie sie ein

Für Artikel, bei denen Sie dem System erlauben, [Ihre Pufferzonen automatisch zu berechnen](#set-up-buffers), führen Sie diese Schritte aus, um entkoppelte Vorlaufzeiten für einen Entkopplungspunktartikel zu berechnen oder einzugeben.

1. Öffnen Sie die Seite **Artikelabdeckung** für Ihren Entkopplungspunkt-Artikel. (Weitere Informationen finden Sie unter [Puffer für einen Artikel mit Entkopplungspunkt festlegen](#set-up-buffers).)
1. Wählen Sie einen Datensatz zur Positionserfassung, der einen Entkopplungspunkt erstellt.
1. Wählen Sie die Registerkarte **Pufferwerte**.
1. Wenn im Raster keine Zeiträume angezeigt werden, wählen Sie im Aktionsbereich auf der Registerkarte **Pufferwerte** die Option **Zeiträume hinzufügen**. Das System füllt das Raster mit Zeilen für jeden täglichen oder wöchentlichen Zeitraum, je nachdem, ob das Feld **Min, Max und Wiederbestellpunkt Zeitraum** für die [Abdeckungsgruppe](ddmrp-inventory-positioning.md) auf *Täglich* oder *Wöchentlich* festgelegt ist. Das System fügt genügend Zeilen hinzu, um den Zeitraum zu erreichen, der für die dem Artikel zugewiesene Deckungsgruppe angegeben ist.
1. Wählen Sie den Zeitraum, in dem Sie die entkoppelte Vorlaufzeit berechnen möchten. (Normalerweise ist dieser Zeitraum der Zeitraum, der das heutige Datum einschließt.)
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Pufferwerte** die Option **Berechnen Sie die entkoppelte Vorlaufzeit**.
1. Legen Sie in der Dialogbox **Entkoppelte Vorlaufzeit berechnen** die folgenden Felder fest:

    - **Stückliste** – Wählen Sie die Stückliste aus, für die Sie die Berechnung ausführen möchten.
    - **Datum** – Wählen Sie das Datum, an dem Sie die Berechnung ausführen möchten. Die Stücklisten werden so gefiltert, dass nur die Stücklisten angezeigt werden, die für das ausgewählte Datum aktiv sind.
    - **Menge** – Geben Sie die Menge ein, für die Sie die Berechnung ausführen möchten. Die festgelegte Stückliste wird so gefiltert, dass nur Stücklisten angezeigt werden, die auf die angegebene Menge zutreffen.

1. Wählen Sie **OK**, um die Berechnung auszuführen und das Dialogfeld **Berechnen der entkoppelten Vorlaufzeit** zu schließen. Die Spalte **Entkoppelte Vorlaufzeit** für den von Ihnen gewählten Zeitraum zeigt jetzt den berechneten Wert an.

### <a name="calculate-or-enter-average-daily-usage"></a><a name="calc-adu"></a>Berechnen Sie den durchschnittlichen täglichen Verbrauch oder geben Sie ihn ein.

Für Artikel, bei denen Sie zulassen, dass das System [Ihre Pufferzonen automatisch berechnet](#set-up-buffers), führen Sie diese Schritte aus, um die ADU für einen Artikel mit Entkopplungspunkt zu berechnen oder einzugeben.

1. Öffnen Sie die Seite **Artikelabdeckung** für Ihren Entkopplungspunkt-Artikel. (Weitere Informationen finden Sie unter [Puffer für einen Artikel mit Entkopplungspunkt festlegen](#set-up-buffers).)
1. Wählen Sie einen Datensatz zur Positionserfassung, der einen Entkopplungspunkt erstellt.
1. Wählen Sie die Registerkarte **Pufferwerte**.
1. Wenn im Raster keine Zeiträume angezeigt werden, wählen Sie im Aktionsbereich auf der Registerkarte **Pufferwerte** die Option **Zeiträume hinzufügen**. Das System füllt das Raster mit Zeilen für jeden täglichen oder wöchentlichen Zeitraum, je nachdem, ob das Feld **Min, Max und Wiederbestellpunkt Zeitraum** für die [Abdeckungsgruppe](ddmrp-inventory-positioning.md) auf *Täglich* oder *Wöchentlich* festgelegt ist. Darüber hinaus werden die Standardwerte für die Felder **Faktor Vorlaufzeit** und **Faktor Variabilität** aus der Deckungsgruppe übernommen. Sie können diese Werte für jede Zeile nach Bedarf bearbeiten.
1. Wählen Sie einen Zeitraum, für den Sie ADU berechnen möchten.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Pufferwerte** die Option **Berechne durchschnittlichen täglichen Verbrauch**. Das System versucht, die Daten zu sammeln, die für die ADU-Berechnung erforderlich sind, wie für die [Erfassungsgruppe](ddmrp-inventory-positioning.md) definiert.
1. Führen Sie einen dieser Schritte aus:

    - Wenn die erforderlichen Daten verfügbar sind, werden die Berechnungsergebnisse in der Spalte **Durchschnittlicher täglicher Verbrauch** hinzugefügt. In diesem Fall ist keine Aktion erforderlich.
    - Wenn die erforderlichen Daten nicht verfügbar sind, werden automatisch keine Werte hinzugefügt. In diesem Fall geben Sie manuell geschätzte Werte für jede Zeile ein, für die Sie Pufferwerte berechnen möchten.

### <a name="calculate-and-apply-buffer-values"></a>Berechnen Sie die Pufferwerte und wenden Sie sie an

Für Artikel, bei denen Sie die automatische [Berechnung Ihrer Pufferzonen](#set-up-buffers) zulassen, können Sie die Berechnung der Pufferwerte manuell auslösen, indem Sie diese Schritte ausführen.

1. Für den entsprechenden Artikel des Entkopplungspunktes [konfigurieren Sie die Pufferberechnung](#set-up-buffers), [berechnen oder geben Sie entkoppelte Vorlaufzeiten](#calc-lead-time) und [berechnen oder geben Sie den durchschnittlichen täglichen Verbrauch](#calc-adu) für alle relevanten Zeiträume ein, wie zuvor in diesem Artikel beschrieben.
1. Öffnen Sie die Seite **Artikelabdeckung** für Ihren Entkopplungspunkt-Artikel.
1. Wählen Sie die Registerkarte **Pufferwerte**, die bereits eine Liste von Zeiträumen zeigen sollte.
1. Wählen Sie den Zeitraum, für den Sie die Pufferwerte berechnen möchten. (In der Regel ist dieser Zeitraum der Zeitraum, der das heutige Datum einschließt.) Die Zeile, die Sie auswählen, muss bereits Werte ungleich Null in den Spalten **Durchschnittlicher täglicher Verbrauch** und **Entkoppelte Vorlaufzeit** aufweisen.
1. Bearbeiten Sie das Feld **Bedarfsanpassungsfaktor** für eine oder mehrere Zeilen nach Bedarf. Das System wendet diesen Faktor auf den Wert **Durchschnittlicher täglicher Verbrauch** in allen Pufferberechnungen an, in denen dieser Wert verwendet wird. Mit diesem Faktor können Sie die Schwankungen des Bedarfs nach Datum ausgleichen (z.B. bei Feiertagen oder saisonalen Artikeln).
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Pufferwerte** die Option **Min-, Max- und Neubestellungspunktmengen berechnen**. Das System berechnet und füllt die Spalten **Berechneter Min**, **Berechneter Neubestellungspunkt** und **Berechneter Max** im Raster auf der Seite **Artikelabdeckung**.
1. Wenn Sie die Überprüfung der berechneten Werte abgeschlossen haben, müssen Sie sie anwenden. Andernfalls haben sie keine Auswirkung. Wenn Sie eine Berechnung für eine oder mehrere Zeilen anwenden, werden Werte aus den Feldern **Berechnetes Minimum**, **Berechnetes Neubestellungspunkt** und **Berechnetes Maximum** in die Spalten **Minimum**, **Neubestellungspunkt** und **Max** kopiert. Wählen Sie im Aktionsbereich auf der Registerkarte **Pufferwerte** in der Gruppe **Aktion ausführen** eine der folgenden Schaltflächen:

    - **Alle Berechnungen akzeptieren** – Wendet alle berechneten Werte im Raster an.
    - **Berechnungen für ausgewählte Zeilen akzeptieren** – Wenden Sie berechnete Werte nur für die ausgewählten Zeilen an.
    - **Alle Berechnungen verwerfen** – Verwerfen Sie alle berechneten Werte für Mindestmengen, Höchstmengen und Neubestellungspunkte im Raster.
    - **Berechnungen für ausgewählte Zeilen verwerfen** – Verwerfen Sie alle berechneten Werte für Mindestmengen, Maximalmengen und Neubestellungspunkte für die ausgewählten Zeilen.

### <a name="schedule-automatic-buffer-value-calculations"></a>Planen Sie automatische Pufferwertberechnungen

Nachdem Sie Ihre DDMRP-Einstellungen vollständig festgelegt und bestätigt haben, dass sie wie erwartet funktionieren, werden Sie wahrscheinlich einen Batchauftrag einrichten wollen, um die ADU und die zugehörigen Pufferwerte nach Bedarf auf der Grundlage der tatsächlichen Verbrauchsdaten und/oder aktualisierter Planungen neu zu berechnen. Dieses Verfahren gilt nur für Artikel, bei denen Sie dem System erlauben, [automatisch Ihre Pufferzonen zu berechnen](#set-up-buffers).

Führen Sie diese Schritte aus, um automatische Pufferwertberechnungen zu planen.

1. Gehen Sie zu **Masterprogrammplanung \> Masterplanung \> DDMRP \> Pufferwerte berechnen**.
1. Legen Sie in der Dialogbox **Pufferwerte berechnen** die folgenden Felder fest:

    - **Durchschnittlichen täglichen Verbrauch berechnen** – Legen Sie diese Option auf *Ja* fest, um den durchschnittlichen täglichen Verbrauch (ADU) der Artikel des Entkopplungspunkts jedes Mal neu zu berechnen, wenn der Auftrag ausgeführt wird. Legen Sie es auf *Nein* fest, um diese Berechnung zu überspringen. Normalerweise sollten Sie diese Option auf *Ja* festlegen.
    - **Entkoppelte Vorlaufzeit berechnen** – Legen Sie diese Option auf *Ja* fest, um die entkoppelten Vorlaufzeiten jedes Mal neu zu berechnen, wenn der Auftrag ausgeführt wird. Legen Sie es auf *Nein* fest, um diese Berechnung zu überspringen. Normalerweise sollten Sie diese Option auf *Ja* festlegen.
    - **Pufferwerte berechnen** – Legen Sie diese Option auf *Ja* fest, um die Pufferwerte jedes Mal, wenn der Auftrag ausgeführt wird, neu zu berechnen. Legen Sie es auf *Nein* fest, um diese Berechnung zu überspringen. Normalerweise sollten Sie diese Option auf *Ja* festlegen.
    - **Berechnung für Min, Max und Neubestellungspunkt akzeptieren** – Legen Sie diese Option auf *Ja* fest, um die neu berechneten Pufferwerte jedes Mal, wenn der Auftrag ausgeführt wird, automatisch zu genehmigen und anzuwenden. Legen Sie die Option auf *Nein* fest, damit die neu berechneten Werte nicht angewendet werden. In diesem Fall werden die neu berechneten Werte nicht wirksam, es sei denn, jemand wendet sie später manuell auf der Seite **Artikelabdeckung** des jeweiligen Produkts an. Normalerweise sollten Sie diese Option auf *Ja* festlegen.
    - **Masterplan** – Wählen Sie einen Masterplan aus, der die Artikel enthält, die von der Berechnung betroffen sein werden. Die Berechnung wird auf alle Artikel im Planfilter angewendet, der durch die **Filter**-Einstellungen in diesem Dialogfeld weiter eingeschränkt wird.

1. Um die Datensätze einzuschränken, für die dieser Batchauftrag ausgeführt werden soll, wählen Sie auf der Registerkarte **Einzuschließende Datensätze** Inforegister die Option **Filter**, um das Dialogfeld **Abfrage** zu öffnen. Dieses Dialogfeld funktioniert genauso wie bei anderen Arten von [Hintergrundaufträgen](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) im Supply Chain Management.
1. Auf der Registerkarte **Im Hintergrund ausführen** Inforegister legen Sie fest, wie, wann und wie oft die ausgewählten Berechnungen für die ausgewählten Artikel durchgeführt werden sollen. Die Felder funktionieren genauso wie bei anderen Arten von [Hintergrund-Jobs](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) im Supply Chain Management.
1. Wählen Sie **OK**, um den neuen Auftrag zur Ausführung in eine Batch-Warteschlange aufzunehmen.

### <a name="review-and-recalculate-decoupled-lead-times-for-all-items"></a>Überprüfen und berechnen Sie die entkoppelten Vorlaufzeiten für alle Artikel neu

Führen Sie diese Schritte aus, um alle entkoppelten Vorlaufzeiten, die in Ihrer juristischen Entität (Firma) verfügbar sind, zu überprüfen und neu zu berechnen.

1. Gehen Sie zu **Masterplanung \> Masterplanung \> DDMRP \> Entkoppelte Vorlaufzeit**.
1. Auf der Seite **Entkoppelte Vorlaufzeit** können Sie die Liste nach Bedarf durchsuchen und filtern, um die gewünschten Informationen zu finden. Um noch mehr Informationen zu einem Artikel anzuzeigen, wählen Sie den entsprechenden Link in der Spalte **Artikelnummer**.
1. Wenn Sie die entkoppelte Vorlaufzeit für einen beliebigen Artikel neu berechnen möchten, markieren Sie den Artikel und wählen Sie dann **Entkoppelte Vorlaufzeit berechnen** im Aktionsbereich. Das Dialogfenster **Entkoppelte Vorlaufzeit berechnen** erscheint. Dieses Dialogfeld funktioniert genauso wie bei der [Berechnung der entkoppelten Vorlaufzeiten](#calc-lead-time) für denselben Artikel auf der Seite **Artikelabdeckung**.
