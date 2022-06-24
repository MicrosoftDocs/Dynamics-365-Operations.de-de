---
title: Ausrichtungsdatumsszenarien
description: Dieser Artikel enthält Beispiele, die zeigen, wie Ausrichtungsdaten in der Abonnementabrechnung funktionieren.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 102e3a104be5be287f914172160e95aff65d0b18
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872614"
---
# <a name="alignment-date-scenarios"></a>Ausrichtungsdatumsszenarien

Dieser Artikel enthält Beispiele, die zeigen, wie Ausrichtungsdaten in der Abonnementabrechnung funktionieren.

Für diese Beispiele hat ein Abrechnungsdetail für einen Abrechnungszeitplan das Ausrichtungsdatum 31. Oktober 2019. Das erste Abrechnungsdetail für die Position endet am 31. Oktober 2019 und wird entsprechend anteilig berechnet. Die Position wird automatisch verlängert, indem als Verlängerungsstartdatum der 11. November verwendet wird.

> [!NOTE]
> Das Jahr ist relevant, da es dazu führen kann, dass das Ausrichtungsdatum mehr oder weniger als ein Jahr beträgt. Für diese Beispiele ist die Methode der anteiligen Verrechnung auf der Seite **Parameter für wiederkehrende Vertragsabrechnungen** auf **Monatlich** festgelegt. Wenn sie auf **Täglich** eingestellt ist, werden einige Teilbeträge abweichen.

## <a name="scenario-1-no-alignment"></a>Szenario 1: Keine Ausrichtung

Der Abrechnungszeitplan wird mit folgenden Daten erstellt:

- **Startdatum:** 1. Mai 2019
- **Enddatum:** 31. Dezember 2024
- **Betrag:** 1.000 $

| Startdatum der Abrechnung | Enddatum der Abrechnung | Vorherige Ablesung | Aktuelle Ablesung | Eingegebene Menge | Freimenge | Fakturierbare Menge | Preis je Einheit |
|---|---|---|---|---|---|---|---|
| 01.05.2019 | 30.04.2020 | | | 1.00 | | 1.00 | 1,000.00 |
| 01.05.2020 | 30.04.2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 01.05.2021 | 30.04.2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 01.05.2022 | 30.04.2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 01.05.2023 | 30.04.2024 | | | 1.00 | | 1.00 | 1,000.00 |
| 01.05.2024 | 31.12.2024 | | | 1.00 | | 1.00 | 666.67 |

## <a name="scenario-2-shortened-alignment"></a>Szenario 2: Verkürzte Ausrichtung

Der Abrechnungszeitplan wird mit folgenden Daten erstellt:

- **Startdatum:** 1. Mai 2019
- **Enddatum:** 31. Dezember 2024
- **Betrag:** 1.000 $
- **Ausrichtungsdatum:** 31. Dezember 2019

Der erste Verlängerungsbetrag ist für weniger als ein Jahr.

| Startdatum der Abrechnung | Enddatum der Abrechnung | Vorherige Ablesung | Aktuelle Ablesung | Eingegebene Menge | Freimenge | Fakturierbare Menge | Preis je Einheit |
|---|---|---|---|---|---|---|---|
| 01.05.2019 | 31.12.2019 | | | 1.00 | | 1.00 | 666.67 |
| 1/1/2020 | 31/12/2020 | | | 1.00 | | 1.00 | 1,000.00 |
| 01.01.2021 | 31.12.2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 01.01.2022 | 31.12.2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 01.01.2023 | 31.12.2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 01.01.2024 | 31.12.2024 | | | 1.00 | | 1.00 | 1,000.00 |

## <a name="scenario-3-extended-alignment"></a>Szenario 3: Verlängerte Ausrichtung

Der Abrechnungszeitplan wird mit folgenden Daten erstellt:

- **Startdatum:** 1. Mai 2019
- **Enddatum:** 31. Dezember 2024
- **Betrag:** 1.000 $
- **Ausrichtungsdatum:** 31. Dezember 2020

Der erste Verlängerungsbetrag ist für mehr als ein Jahr.

| Startdatum der Abrechnung | Enddatum der Abrechnung | Vorherige Ablesung | Aktuelle Ablesung | Eingegebene Menge | Freimenge | Fakturierbare Menge | Preis je Einheit |
|---|---|---|---|---|---|---|---|
| 01.05.2019 | 31/12/2020 | | | 1.00 | | 1.00 | 1,666.67 |
| 01.01.2021 | 31.12.2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 01.01.2022 | 31.12.2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 01.01.2023 | 31.12.2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 01.01.2024 | 31.12.2024 | | | 1.00 | | 1.00 | 1,000.00 |

## <a name="scenario-4-alignment-with-a-different-end-month"></a>Szenario 4: Ausrichtung mit einem anderen Endmonat

Der Abrechnungszeitplan wird mit folgenden Daten erstellt:

- **Startdatum:** 1. Mai 2019
- **Enddatum:** 31. Oktober 2024
- **Betrag:** 1.000 $
- **Ausrichtungsdatum:** 31. Dezember 2019

> [!NOTE]
> Dieses Szenario ist nicht üblich.

| Startdatum der Abrechnung | Enddatum der Abrechnung | Vorherige Ablesung | Aktuelle Ablesung | Eingegebene Menge | Freimenge | Fakturierbare Menge | Preis je Einheit |
|---|---|---|---|---|---|---|---|
| 01.05.2019 | 31.12.2019 | | | 1.00 | | 1.00 | 666.67 |
| 1/1/2020 | 31/12/2020 | | | 1.00 | | 1.00 | 1,000.00 |
| 01.01.2021 | 31.12.2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 01.01.2022 | 31.12.2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 01.01.2023 | 31.12.2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 01.01.2024 | 31.10.2024 | | | 1.00 | | 1.00 | 833.33 |

## <a name="scenario-5-single-partial-year"></a>Szenario 5: Einzelnes Teiljahr

Der Abrechnungszeitplan wird mit folgenden Daten erstellt:

- **Startdatum:** 1. Mai 2019
- **Enddatum:** 31. Dezember 2019
- **Betrag:** 1.000 $
- **Ausrichtungsdatum:** 31. Dezember 2019

In diesem Szenario wird das Ausrichtungsdatum nicht benötigt. Dieses Szenario ist bei automatischen Verlängerungen üblich.

| Startdatum der Abrechnung | Enddatum der Abrechnung | Vorherige Ablesung | Aktuelle Ablesung | Eingegebene Menge | Freimenge | Fakturierbare Menge | Preis je Einheit |
|---|---|---|---|---|---|---|---|
| 01.05.2019 | 31.12.2019 | | | 1.00 | | 1.00 | 666.67 |

## <a name="scenario-6-calculated-dates"></a>Szenario 6: Berechnete Daten

Support und Verlängerung werden mit folgenden Daten erstellt:

- **Startdatum überschreiben:** Nein
- **Startdatum für Support und Verlängerung:** Beginn des nächsten Monats
- **Rechnungsbuchungsdatum:** 22. Juni 2019
- **Ausrichtungsdatum:** 31. Dezember 2020

| Startdatum der Abrechnung | Enddatum der Abrechnung | Vorherige Ablesung | Aktuelle Ablesung | Eingegebene Menge | Freimenge | Fakturierbare Menge | Preis je Einheit |
|---|---|---|---|---|---|---|---|
| 01.07.2019 | 31.07.2019 | | | 1.00 | | 1.00 | 297.60 |
| 01.08.2019 | 31/12/2020 | | | 1.00 | | 1.00 | 6,936.00 |

## <a name="scenario-7-calculated-dates-and-future-posting"></a>Szenario 7: Berechnete Daten und zukünftige Buchung

Support und Verlängerung werden mit folgenden Daten erstellt:

- **Startdatum überschreiben:** Nein
- **Startdatum für Support und Verlängerung:** Beginn des nächsten Monats
- **Rechnungsbuchungsdatum:** 22. Juni 2019
- **Ausrichtungsdatum:** 31. Dezember 2020

Für dieses Szenario wird das Ausrichtungsdatum auf den 31. Dezember 2021 geändert.

| Startdatum der Abrechnung | Enddatum der Abrechnung | Vorherige Ablesung | Aktuelle Ablesung | Eingegebene Menge | Freimenge | Fakturierbare Menge | Preis je Einheit |
|---|---|---|---|---|---|---|---|
| 22.06.2019 | 22.06.2019 | | | 1.00 | | 1.00 | 0,00 |
| 01.08.2019 | 31/12/2020 | | | 1.00 | | 1.00 | 4,250.00 |

## <a name="scenario-8-manual-dates-and-multiple-years"></a>Szenario 8: Manuelle Daten und mehrere Jahre

Support und Verlängerung werden mit folgenden Daten erstellt:

- **Startdatum überschreiben:** Ja
- **Verlängerungsstartdatum:** 1. Juli 2020
- **Verlängerungsenddatum:** 31. Dezember 2024
- **Ausrichtungsdatum:** 31. Dezember 2021

| Startdatum der Abrechnung | Enddatum der Abrechnung | Vorherige Ablesung | Aktuelle Ablesung | Eingegebene Menge | Freimenge | Fakturierbare Menge | Preis je Einheit |
|---|---|---|---|---|---|---|---|
| 22.06.2019 | 22.06.2019 | | | 1.00 | | 1.00 | 0,00 |
| 01.07.2020 | 31.12.2021 | | | 1.00 | | 1.00 | 375.00 |
| 01.01.2022 | 31.12.2022 | | | 1.00 | | 1.00 | 250,00 |
| 01.01.2023 | 31.12.2023 | | | 1.00 | | 1.00 | 250,00 |
| 01.01.2024 | 31.12.2024 | | | 1.00 | | 1.00 | 250,00 |

## <a name="scenario-9-manual-dates-multiple-years-and-a-different-end-month"></a>Szenario 9: Manuelle Daten, mehrere Jahre und ein anderer Endmonat

Support und Verlängerung werden mit folgenden Daten erstellt:

- **Startdatum überschreiben:** Ja
- **Verlängerungsstartdatum:** 1. Juli 2020
- **Verlängerungsenddatum:** 31. Oktober 2024
- **Ausrichtungsdatum:** 31. Dezember 2021

| Startdatum der Abrechnung | Enddatum der Abrechnung | Vorherige Ablesung | Aktuelle Ablesung | Eingegebene Menge | Freimenge | Fakturierbare Menge | Preis je Einheit |
|---|---|---|---|---|---|---|---|
| 22.06.2019 | 22.06.2019 | | | 1.00 | | 1.00 | 0,00 |
| 01.07.2020 | 31.12.2021 | | | 1.00 | | 1.00 | 375.00 |
| 01.01.2022 | 31.12.2022 | | | 1.00 | | 1.00 | 250,00 |
| 01.01.2023 | 31.12.2023 | | | 1.00 | | 1.00 | 250,00 |
| 01.01.2024 | 31.10.2024 | | | 1.00 | | 1.00 | 208.33 |

## <a name="scenario-10-alignment-without-proration"></a>Szenario 10: Ausrichtung ohne anteilige Verrechnung

Support und Verlängerung werden mit folgenden Daten erstellt:

- **Startdatum überschreiben:** Nein
- **Rechnungsbuchungsdatum:** 22. Juni 2019
- **Ausrichtungsdatum:** 31. Dezember 2019

Das Verlängerungsstartdatum und die Ausrichtungsdaten werden so angepasst, dass beide Startdaten nach dem Buchungsdatum liegen.

- **Verlängerungsstartdatum:** 1. Januar 2020
- **Verlängerungsenddatum:** 31. Dezember 2020
