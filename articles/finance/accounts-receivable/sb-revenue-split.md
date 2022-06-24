---
title: Umsatzerlösverteilungsvorlagen in Abonnementabrechnung
description: In diesem Artikel wird erläutert, wie Sie Umsatzerlösaufteilungsvorlagen für Artikel einrichten, die als Bündel verkauft werden.
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
ms.openlocfilehash: 145ca6e6f0673a5a09fe9a23cf5e163421617fd9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904758"
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

## <a name="additional-revenue-split-information"></a>Zusätzliche Informationen zur Umsatzaufteilung

Wenn Sie einen Artikel hinzufügen, der Teil eines Umsatz-Splits ist, beachten Sie die folgenden Informationen: 

- Der übergeordnete Betrag kann nicht verschoben werden.
- Die Werte für Startdatum, Enddatum, Menge, Einheit, Standort und Lager der untergeordneten Artikel basieren auf dem übergeordneten Artikel. Diese Werte können nicht für die untergeordneten Artikel geändert werden. Alle Änderungen müssen an dem übergeordneten Artikel vorgenommen werden. 
- Die Preismethode ist **Flat** und kann nicht geändert werden.
- Untergeordnete Artikel können hinzugefügt oder entfernt werden.
- Übergeordnete und untergeordnete Artikel müssen die gleiche Artikelgruppe verwenden. 
- Untergeordnete Artikel können eine der folgenden Einrichtungen haben:

    - Die Felder **Abrechnungshäufigkeit** und **Abrechnungsintervalle** werden auf denselben Wert wie der übergeordnete Artikel festgelegt. 
    - Das Feld **Rechnungshäufigkeit** wird auf **Einmalig** festgelegt. In diesem Fall wird das Feld **Abrechnungsintervalle** automatisch auf **1** festgelegt. 

- Die Summe der Nettobeträge der untergeordneten Artikel entspricht dem übergeordneten Betrag. Wenn die Zuordnungsmethode **Nullbeträge** lautet, ist sowohl die Summe der Beträge der untergeordneten Artikel als auch der übergeordnete Betrag 0 (Null). 

    > [!NOTE]
    > Wenn die Zuweisungsmethode **Null übergeordneter Betrag** lautet, ist die (von Null abweichende) Summe der untergeordneten Artikel nicht gleich dem übergeordneten Betrag, der 0 (Null) ist. Diese Zuordnungsmethode wird für interne Zwecke verwendet, damit die Mitarbeiter die untergeordneten Artikel sehen können. Die Debitoren können jedoch nur den übergeordneten Artikel sehen.

- Wenn der MEA-Typ (Multiple Element Arrangement) des Verkaufsauftrags **Einzel** ist, wird beim Hinzufügen der übergeordneten und untergeordneten Artikel die entsprechende Transaktionszeile für die Aufteilung des Umsatzes erstellt. 
- Wenn die Zuordnungsmethode für einen Umsatzsplit **Gleiche Beträge** lautet und der übergeordnete Betrag geändert wird, werden die Beträge für alle untergeordneten Zeilen neu berechnet. 
- Bei einem Umsatzsplit mit der Zuteilungsmethode **Variabler Betrag** verhält sich das System wie folgt:

    - Der Nettobetrag des übergeordneten Artikels erscheint in der Spalte **Übergeordneter Betrag**. Dieser Wert kann bearbeitet werden. Der Einheitspreis, der Nettobetrag und der Rabatt sind jedoch 0 (Null) und können nicht bearbeitet werden.
    - Der Einheitspreis der untergeordneten Artikel ist 0 (Null). Sie können den Einheitspreis oder den Nettobetrag bearbeiten. Wenn Sie einen Wert bearbeiten, wird der andere Wert automatisch aktualisiert.

- Bei einem Umsatzsplit mit der Verrechnungsmethode **Prozentsatz** verhält sich der Artikel wie folgt:

    - Der Nettobetrag des übergeordneten Artikels erscheint in der Spalte **Übergeordneter Betrag**. Dieser Wert kann bearbeitet werden. Der Einheitspreis, der Nettobetrag und der Rabatt sind jedoch 0 (Null) und können nicht bearbeitet werden. 
    - Der Nettobetrag der untergeordneten Artikel wird berechnet als *Prozentsatz* &times; *Übergeordneter Betrag*.

- Bei einem Umsatzsplit mit der Verrechnungsmethode **Gleicher Betrag** verhält sich das System wie folgt:

    - Der Nettobetrag des übergeordneten Artikels erscheint in der Spalte **Übergeordneter Betrag**. Dieser Wert kann bearbeitet werden. Der Einheitspreis, der Nettobetrag und der Rabatt sind jedoch 0 (Null) und können nicht bearbeitet werden. 
    - Der Nettobetrag der untergeordneten Artikel wird berechnet, indem der übergeordnete Betrag gleichmäßig auf alle untergeordneten Artikel aufgeteilt wird. 
    - Wenn untergeordnete Artikel entfernt oder hinzugefügt werden, werden der Nettobetrag und die Einheitspreise neu berechnet, so dass alle untergeordneten Zeilen die gleichen Beträge aufweisen. 
    - Wenn der übergeordnete Betrag nicht gleichmäßig aufgeteilt werden kann, können der Nettobetrag und der Preis pro Einheit des letzten untergeordneten Artikels etwas höher oder niedriger sein als der Nettobetrag und der Preis pro Einheit der anderen untergeordneten Artikel. 

- Bei einem Umsatzsplit, bei dem die Allokationsmethode **Nullbetrag** ist, tritt das folgende Verhalten auf:

    - Der Einheitspreis, der Nettobetrag und der Rabatt können bearbeitet werden. Der übergeordnete Betrag ist 0 (Null) und kann nicht bearbeitet werden. 
    - Die Werte für Menge, Einheit, Standort und Lager der untergeordneten Artikel basieren auf dem übergeordneten Artikel. Sie können diese Werte nicht für die untergeordneten Artikel ändern. Alle Änderungen müssen an dem übergeordneten Artikel vorgenommen werden. 
    - Der Einheitspreis und der Nettopreis der untergeordneten Artikel ist 0 (Null) und kann nicht bearbeitet werden. 

- Bei einem Umsatzsplit mit der Zuordnungsmethode **Null übergeordneter Betrag** kommt es zu folgendem Verhalten:

    - Stückpreis, übergeordneter Betrag und Nettobetrag des übergeordneten Artikels sind 0 (Null).
    - In einem Fakturierungsplan erscheinen die untergeordneten Zeilen so, als ob sie manuell hinzugefügt worden wären, und alle Werte werden auf der Grundlage der ausgewählten Fakturierungsplangruppe aktualisiert. Diese Werte können bearbeitet werden. Bei untergeordneten Artikeln können Sie über die Felder **Erfasste Menge**, **Einheitspreis**, **Rabatt** und **Nettobetrag** in **Abrechnungsdetails anzeigen** auf die Optionen **Skalierung und Rabatt** und **Erweiterte Preisgestaltung** zugreifen. 
    - Auf einem Verkaufsauftrag haben die untergeordneten Zeilen einen Rabatt und einen Rabattprozentsatz von 0 (Null). 
    - Der Fakturierungsrhythmus der übergeordneten und der untergeordneten Artikel kann geändert werden, und jede Zeile kann einen anderen Rhythmus haben. Der übergeordnete Artikel wird jedoch automatisch aktualisiert, so dass er die kürzeste Frequenz aus seinen untergeordneten Zeilen verwendet. Ein Beispiel: Ein Umsatzsplit hat zwei untergeordnete Artikel, von denen einer den Abrechnungsrhythmus **Monatlich** und der andere den Abrechnungsrhythmus **Jährlich** verwendet. In diesem Fall wird die Abrechnungshäufigkeit des übergeordneten Artikels auf **Monatlich** aktualisiert.
