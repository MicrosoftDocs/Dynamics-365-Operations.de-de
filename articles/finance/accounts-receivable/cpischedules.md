---
title: Zeitplan für Verbraucherpreisindex
description: In diesem Thema wird erläutert, wie Sie die Liste der Verbraucherpreisindex-Pläne erstellen, die Sie aus dem Internet erhalten, um die Eskalationsgebühr bei der Abonnementabrechnung zu ermitteln.
author: JodiChristiansen
ms.date: 11/04/2021
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
ms.openlocfilehash: 2a69e58095844286878e27a100fa49a44a4a71f4
ms.sourcegitcommit: 4d7bc52e6cdf6afce3793893ba2aa07176302314
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/11/2022
ms.locfileid: "8560491"
---
# <a name="consumer-price-index-schedule"></a>Zeitplan für Verbraucherpreisindex

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Pläne für Verbraucherpreisindizes (VPI) erstellt, gelöscht, überprüft und verarbeitet werden. Ein VPI-Plan kann verwendet werden, um die Preise für Verbrauchsgüter und Dienstleistungen zu ermitteln, die Sie als Abrechnungszeitplanpositionen hinzufügen. Der Verbraucherpreisindex kann dann mit Eskalations- und Rabattpreisen in einem Abrechnungszeitplan verwendet werden oder auch manuell verarbeitet werden, um die Abrechnungsbeträge in Abrechnungszeitplänen zu aktualisieren. Sie können VPI-Pläne manuell eingeben oder sie importieren, indem Sie die zusammengesetzte Entität für VPI-Pläne verwenden.

Um einen VPI-Plan hinzuzufügen, führen Sie die folgenden Schritte aus.

1. Wählen Sie auf der Seite **Verbraucherpreisindex-Plan** die Option **Neu** aus.
2. Geben Sie im Feld **Verbraucherpreisindex-Plan** einen eindeutigen Namen ein.
3. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
4. Wählen Sie auf der Registerkarte **Verbraucherpreisindex-Plan** die Option **Hinzufügen** aus.
5. Geben Sie im Feld **Datum des Verbraucherpreisindex** das Datum ein, an dem der neue VPI-Plan aktiv wird.
6. Geben Sie im Feld **Verbraucherpreisindex-Plan** den Namen ein, den Sie in Schritt 2 eingegeben haben.
7. Wählen Sie **Speichern** aus.

Um das Datum für einen VPI-Plan zu löschen, gehen Sie wie folgt vor.

1. Wählen Sie auf der Seite **Verbraucherpreisindex-Plan** eine oder mehrere Zeilen aus, die Sie löschen möchten, und wählen Sie dann **Entfernen** aus.
2. Um den gesamten VPI-Plan zu löschen, wählen Sie im Aktivitätsbereich **Löschen** aus. Sie können den ausgewählten VPI-Plan nicht löschen, wenn er mit einem Abrechnungszeitplan verknüpft ist.
3. Wählen Sie im Aktivitätsbereich **Verarbeiten** aus, um die Abrechnungszeitpläne zu aktualisieren, die den ausgewählten VPI-Plan verwenden. Es werden die neuesten VPI-Daten und -Planbeträge verwendet, um die Preise des Abrechnungszeitplans zu aktualisieren.
4. Überprüfen Sie auf dem Inforegister **Verbraucherpreisindex-Prozess** die aktualisierten Felder **Abrechnungszeitplannummer**, **Artikelnummer**, **Startdatum der Abrechnung**, **Enddatum der Abrechnung**, **Eskalationsdatum** und **Eskalationshäufigkeit**.

Nachdem die VPI-Pläne eingerichtet wurden, können sie für Eskalations- und Rabattpreisänderungen in Abrechnungszeitplänen verwendet werden.

## <a name="cpi-calculation"></a>Berechnung des Verbraucherpreisindex

Für diese Beispiele reicht der Zeitraum vom 1. Januar 2020 bis zum 31. Dezember 2022. Der VPI-Basissatz (der VPI-Wert bei Vertragsbeginn) beträgt 105,65. Am 1. Januar 2021 beträgt der aktuelle Verbraucherpreisindex 110,5. Am 1. Januar 2022 beträgt der aktuelle Verbraucherpreisindex 114,25. Der anfängliche Betrag ist 1.000 $.

**Beispiel 1**

Legen Sie auf der Seite **Wiederkehrende Vertragsabrechnungsparameter** das Feld **Berechnung des Verbraucherpreisindex** auf **Basis-Verbraucherpreisindex** fest.

Für den Zeitraum vom 1. Januar 2021 wird der erste Eskalationsbetrag auf der Grundlage des Ausgangsbetrags wie folgt berechnet:

1.000 + (110,5 – 105,65) &divide; 105,65 &times; 1.000 = 1.045,91

Für den Zeitraum vom 1. Januar 2022 wird der Eskalationsbetrag wie folgt berechnet:

1.000 + (114,25 – 105,65) &divide; 105,65 &times; 1.000 = 1.081,40

**Beispiel 2**

Legen Sie auf der Seite **Wiederkehrende Vertragsabrechnungsparameter** das Feld **Berechnung des Verbraucherpreisindex** auf **Vorheriger Verbraucherpreisindex** fest.

Für den Zeitraum vom 1. Januar 2021 wird der erste Eskalationsbetrag auf der Grundlage des Ausgangsbetrags wie folgt berechnet:

1.000 + (110,5 – 105,65) &divide; 105,65 &times; 1.000 = 1.045,91

Für den Zeitraum vom 1. Januar 2022 wird der Eskalationsbetrag auf der Grundlage des ersten Eskalationsbetrags wie folgt berechnet:

1.045,91 + (114,25 – 110,5) &divide; 110,5 &times; 1.045,91 = 1.081,40

> [!NOTE]
> Der Eskalationsprozess verwendet immer den neuesten VPI-Wert, unabhängig vom Indexdatum. Wenn beispielsweise die Eskalation im September liegt, der letzte Verbraucherpreisindexwert jedoch für Juli gilt, wird der Juli-Index verwendet. Nach Eingabe des September-Index werden keine Anpassungen vorgenommen.

## <a name="prorated-escalation"></a>Anteilige Eskalation

Wenn die Eskalation mitten in einem Abrechnungszeitraum erfolgt, wird der Betrag anteilig berechnet. Beispielsweise geht der Abrechnungszeitraum vom 1. August 2020 bis zum 31. Juli 2021. Am VPI-Datum 1. September 2019 beträgt der VPI-Wert 244. Am VPI-Datum 1. September 2020 beträgt dieser VPI-Wert 250. Wenn der vorherige Satz 1.000 beträgt, werden die folgenden Formeln verwendet, um den Abrechnungsbetrag für den Zeitraum zu berechnen:

* *VPI-Änderungen* = (250 – 244) &divide; 244 = 2,459 %
* *Aktueller Satz* = 1.000 &times; 2,459 % = 1.024,59
* *Anzahl der Tage zum aktuellen Satz* = 31. Juli 2021 – 1. September 2020 = 334
* *Vorheriger Satz* = 1.000
* *Anzahl der Tage zum vorherigen Satz* = 31. August 2020 – 1. August 2020 = 31
* *Gesamtzahl der Tage im Abrechnungszeitraum* = 31. Juli 2021 – 1. August 2020 + 1 = 365
* *Rechnungsbetrag für diesen Zeitraum* = (1.000 &times; 31 &divide; 365) + (1.024,59 &times; 334 &divide; 365) = 1.022,50

## <a name="escalation-that-uses-the-cpi-and-percentage"></a>Eskalation, die den VPI und den Prozentsatz verwendet

Eskalationen können mithilfe des VPI durchgeführt werden. Der VPI zuzüglich einer dreiprozentigen Eskalation beginnt am 1. Januar 2020 und hat eine jährliche Frequenz.

- Der Betrag, der für den 1. Januar 2019 bis zum 31. Dezember 2020 abgerechnet wird, beträgt 4.000.
- Der Abrechnungszeitraum, der eskaliert wird, geht vom 1. Januar 2020 bis zum 31. Dezember 2020.
- Am VPI-Datum 1. Dezember 2018 beträgt der VPI-Wert 205,3. Am VPI-Datum 1. Dezember 2019 beträgt der VPI-Wert 219,6.

Wenn der vorherige Satz 4.000 beträgt, wird der Abrechnungsbetrag für diesen Zeitraum wie folgt berechnet:

- *VPI-Änderungen* = (219,6 – 205,3) &divide; 205,3 = 6,965 %
- *Aktueller Satz* = (4.000 &times; 6,965 %) – 4.000 = 278,60
- *Prozentuale Änderungen* = (4.000 &times; 1,03) – 4.000 = 120
- *Abrechnungsbetrag* = 4.000 + 278,6 + 120 = 4.398,6
