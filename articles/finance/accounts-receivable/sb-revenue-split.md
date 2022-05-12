---
title: Umsatzerlösverteilungsvorlagen in Abonnementabrechnung
description: In diesem Thema wird erläutert, wie Sie Umsatzerlösaufteilungsvorlagen für Artikel einrichten, die als Bündel verkauft werden.
author: JodiChristiansen
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 5c2eb6c8e18770eb149c445f662ab7a90aad81a7
ms.sourcegitcommit: 367e323bfcfe41976e5d8aa5f5e24a279909d8ac
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2022
ms.locfileid: "8660454"
---
# <a name="revenue-split-templates-in-subscription-billing"></a>Umsatzerlösverteilungsvorlagen in Abonnementabrechnung

Verwenden Sie die Seite **Umsatzerlösverteilungsvorlage** zum Einrichten von Vorlagen für die Umsatzerlösverteilung. Die Umsatzerlösverteilung besteht aus einem übergeordneten Artikel mit untergeordneten Artikeln. Diese Art von Artikel wird häufig als Einzelartikel oder Bündel an Kunden verkauft.

Ein Computerelement kann beispielsweise folgendermaßen erstellt werden:

- **Übergeordneter Artikel:** Abonnement Silber
- **(Untergeordnete) Positionen:**

    - Support
    - Wartung
    - Lizenz

Beachten Sie beim Erstellen eines übergeordneten Artikels die folgenden Einschränkungen:

- Ein Artikel kann nur einmal als übergeordneter Artikel angegeben werden.
- Der übergeordnete Artikel kann in derselben Vorlage als untergeordneter Artikel ausgewählt werden.
- Eine gültige Vorlage erfordert mindestens einen untergeordneten Artikel.
- Ein Artikel kann als untergeordneter Artikel für mehr als einen Bündelartikel angegeben werden.
- Jede Übergeordnet-Untergeordnet-Beziehung muss eindeutig sein.

## <a name="create-a-parent-item-that-has-child-items"></a>Übergeordneten Artikel mit untergeordneten Artikeln erstellen

Gehen Sie folgendermaßen vor, um einen übergeordneten Artikel mit untergeordneten Artikeln zu erstellen.

1. Wählen Sie auf der Seite **Umsatzerlösverteilungsvorlage** die Option **Neu** aus.
1. Wählen Sie im Feld **Übergeordneter Artikel** einen übergeordneten Artikel aus. Das Feld **Variantennummer** wird automatisch aktualisiert. Sie den Wert in diesem Feld nach Bedarf ändern.
1. Wählen Sie im Feld **Zuordnungsmethode** eine Zuordnungsmethode aus.
1. Wählen Sie in der Liste **Komponentenartikel** die Option **Hinzufügen** aus, um untergeordnete Artikel hinzuzufügen.
1. Wenn Sie **Prozentsatz** im Feld **Zuordnungsmethode** gewählt haben, geben Sie im Feld **Prozentsatz** einen Prozentsatz an.

    - Wenn Sie **Gleicher Betrag** im Feld **Zuordnungsmethode** ausgewählt haben, wird das Feld **Prozentsatz** automatisch aktualisiert, sodass jeder Artikel den gleichen Prozentsatz hat.
    - Wenn Sie **Variabler Betrag**, **Null übergeordneter Betrag** oder **Nullbetrag** im Feld **Zuordnungsmethode** ausgewählt haben, bleibt der Wert im Feld **Prozentsatz** bei **0** (Null) und kann nicht geändert werden.

1. Wählen Sie **Speichern** aus.

## <a name="fields"></a>Felder

Die Seite **Umsatzerlösverteilungsvorlage** enthält die folgenden Felder.

| Feld | Description |
|-------|-------------|
| Übergeordneter Artikel | Wählen Sie eine Artikelnummer aus. Dieser Artikel wird zum übergeordneten Artikel für den von Ihnen erstellten Bündelartikel. |
| Produktname | Der Produktname. |
| Zuordnungsmethode | <p>Wählen Sie die Zuordnungsmethode:</p><ul><li>**Gleicher Betrag** – Die Zuweisungsprozentsätze werden automatisch berechnet und gleichmäßig auf alle Elemente in der Vorlage aufgeteilt.</li><li>**Prozentsatz** – Es kann ein prozentualer Betrag für die Zuordnung angegeben werden. Die Summe aller Prozentsätze muss gleich 100 sein.</li><li>**Variabler Betrag** – Untergeordnete Artikel, die hinzugefügt werden, haben einen Nettobetrag von 0 (Null). Der Preis der untergeordneten Artikel muss auf Transaktionsebene angegeben werden.</li><li>**Nullbetrag** – Der übergeordnete Artikel behält seinen Einzelpreis und seinen Nettobetrag. Alle untergeordneten Artikel haben einen Nettobetrag von 0 (Null).</li><li>**Null übergeordneter Betrag** – Der übergeordnete Artikel hat einen festen Nettobetrag von 0 (Null). Alle untergeordneten Artikel werden wie Standardartikel behandelt. Es wird keine Validierung durchgeführt, um sicherzustellen, dass die Summe der untergeordneten Artikelbeträge gleich dem Betrag des übergeordneten Artikels ist.</li></ul> |
| **Komponentenartikel** | |
| Komponentenartikel | Wählen Sie eine Artikelnummer aus. Dieser Artikel ist ein untergeordneter Artikel. |
| Variantennummer | Wählen Sie die Variantennummer für den Artikel. |
| Produktname | Der Produktname. |
| Prozentsatz | <p>Der Zuweisungsprozentsatz für den Meilenstein:</p><ul><li>Wenn das Feld **Zuordnungsmethode** auf **Prozentsatz** festgelegt ist, können Sie den Prozentsatz angeben.</li><li>Wenn das Feld **Zuweisungsmethode** auf **Gleicher Betrag** festgelegt ist, wird der Prozentsatz berechnet, sodass jeder Artikel in der Vorlage den gleichen Prozentsatz hat.</li><li>Wenn das Feld **Zuordnungsmethode** auf **Variabler Betrag**, **Null übergeordneter Betrag** oder **Nullbetrag** festgelegt ist, ist der Prozentsatz 0 (Null) und kann nicht bearbeitet werden.</li></ul><p>Der Wert dieses Felds kann eine beliebige positive Zahl zwischen 0 (Null) und 100 sein. Die Summe aller Prozentsätze muss gleich 100 sein.</p> |
| Gesamter Prozentsatz | <p>Die Summe der Werte in der Spalte **Prozentsatz**.</p><ul><li>Wenn das Feld **Zuordnungsmethode** auf **Gleicher Betrag** oder **Prozentsatz** festgelegt ist, muss die Summer aller Prozentsätze insgesamt 100 ergeben.</li><li>Wenn das Feld **Zuordnungsmethode** auf **Variabler Betrag**, **Null übergeordneter Betrag** oder **Nullbetrag** festgelegt ist, ist der gesamte Prozentsatz 0 (Null).</li></ul> |

## <a name="revenue-split-on-a-sales-order"></a>Umsatzerlösverteilung für einen Auftrag

Führen Sie die folgenden Schritte aus, um einen Auftrag zu erstellen, der einen Artikel enthält, der für die Umsatzerlösverteilung eingerichtet ist.

1. Erstellen Sie auf der Seite **Auftrag** einen Auftrag.
2. Aktivieren Sie in der Position für jeden Artikel, der für die Umsatzerlösverteilung eingerichtet ist, das Kontrollkästchen **Umsatzerlösverteilung**. Dieser Artikel wird zum übergeordneten Artikel. Wenn die Vorlage bereits eingerichtet ist, werden die untergeordneten Artikel automatisch in der Liste angezeigt.
3. Um weitere untergeordnete Artikel hinzuzufügen, wählen Sie **Untergeordnete Umsatzerlösaufteilung hinzufügen** und wählen Sie den untergeordneten Artikel aus, den Sie hinzufügen möchten.
4. Speichern Sie den Auftrag.

## <a name="revenue-split-with-billing-schedules"></a>Umsatzerlösverteilung mit Abrechnungszeitplänen

Führen Sie die folgenden Schritte aus, um einen Abrechnungszeitplan zu erstellen, der einen Artikel enthält, der für die Umsatzerlösverteilung eingerichtet ist.

1. Erstellen Sie auf der Seite **Alle/Aktive Abrechnungszeitpläne** einen Abrechnungszeitplan.
2. Aktivieren Sie in der Position für jeden Artikel, der für die Umsatzerlösverteilung eingerichtet ist, das Kontrollkästchen **Umsatzerlösverteilung**. Dieser Artikel wird zum übergeordneten Artikel. Wenn die Vorlage bereits eingerichtet ist, werden die untergeordneten Artikel automatisch in der Liste angezeigt.
3. Um weitere untergeordnete Artikel hinzuzufügen, wählen Sie **Untergeordnete Umsatzerlösaufteilung hinzufügen** und wählen Sie den untergeordneten Artikel aus, den Sie hinzufügen möchten.
4. Fahren Sie mit den Schritten zum Arbeiten mit dem Abrechnungszeitplan fort.

> [!NOTE]
> Wenn die Option **Umsatzerlösverteilung automatisch erstellen** auf **Ja** eingestellt ist (Seite **Wiederkehrende Abrechnungsparameter für Vertrag**), werden die folgenden Aktionen ausgeführt:
>
> - Wenn der Positionsartikel als übergeordneter Artikel in der Umsatzerlösverteilungsvorlage eingerichtet ist, ist das Kontrollkästchen **Umsatzerlösverteilung** automatisch aktiviert.
> - Die untergeordneten Artikel werden automatisch in die Auftrags- oder Abrechnungszeitplanposition eingegeben.
>
> Wenn die Option **Umsatzerlösverteilung automatisch erstellen** auf **Nein** eingestellt ist, ist das Verhalten wie zuvor erläutert.
