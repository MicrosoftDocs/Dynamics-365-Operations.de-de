---
title: Urlaubs- und Abwesenheitskonzepte
description: In diesem Thema wird beschrieben Urlaub- und Abwesenheitskonzepte und wie Freizeitsalden bestimmt werden.
author: andreabichsel
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application user
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: ''
ms.openlocfilehash: 96e3aa74e513a2421b04bac049400cf71042e2c8
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518070"
---
# <a name="leave-and-absence-concepts"></a>Urlaubs- und Abwesenheitskonzepte

[!include[banner](../includes/banner.md)]

Die Konzepte und Bedingungen, die in diesem Thema beschriebenen, erleichtern, zu ermitteln, wie einem Mitarbeiter zuerkannten Freizeit wird und wie Zeitsalden dieses Mitarbeiter berechnet werden. Weitere Informationen zu Urlaub- und Abwesenheitsverwaltung, finden Sie unter [Urlaub- und Abwesenheitsverwaltung](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).

## <a name="leave-plan-details"></a>Urlaubsplandetails

### <a name="start-date"></a>Startdatum

Das Startdatum ist das Datum, wenn der Abgrenzungsprozess beginnt. Das Startdatum dient zudem als das Jahrestagsdatum, das verwendet wird, um Übertragbeträge zu berechnen.

## <a name="accruals"></a>Abgrenzungen

Abgrenzungen bestimmen, wann und wieoft ein Mitarbeiter Freizeit erhält. Richtlinien, wenn Abgrenzungen bewilligt werden sollen und Richtlinien zur Beschränkung der Erzeugungskapazität werden im Bereich **Abgrenzungen** festgelegt, sofern der Urlaub- und Abwesenheitsplan eingerichtet wurde.

### <a name="accrual-frequency"></a>Abgrenzungshäufigkeit

Die Antizipierungshäufigkeit definiert, wieoft der Urlaub antizipiert oder ausgesprochen wird. Die folgenden Optionen sind verfügbar:

- Täglich
- Wöchentlich
- Zweiwöchentlich
- Halbmonatlich
- Monatlich
- Quartalsweise
- Halbjährlich
- Jährlich
- Keines

### <a name="accrual-period-basis"></a>Abgrenzungsbasis

Die Abgrenzungsperiodenbasis bestimmt das DAtum, das für die Berechnung der Abgrenzungsperioden verwendet wird. Die folgenden Optionen sind verfügbar:

- **Plan-Startdatum**
- **Mitarbeiterspezifisches Datum** – Wenn diese Option ausgewählt wird, bestimmt der Wert des ersten Datumswerts die Quelle, dier verwendet wird, um Abgrenzungsperioden zu berechnen. Die folgenden Optionen sind verfügbar:

    - Benutzerdefiniert
    - Jahrestag
    - Ursprüngliches Einstellungsdatum
    - Dienstalterdatum
    - Angepasstes Startdatum der Arbeitskraft
    - Startdatum der Arbeitskraft

### <a name="accrual-award-date"></a>Zuerkennungsdatum für Anhäufungen

Die Abgrenzungen bestimmen, wann und wieoft ein Mitarbeiter Freizeit erhält. Die folgenden Optionen sind verfügbar:

- **Abgrenzungsperiodeenddatum** – Dem Mitarbeiter wird Freizeit am letzten Datum der Prämienperiode bewilligt.

    Um den richtigen Betrag abzugrenzen, muss der Abgrenzungsprozess die gesamte Periode enthalten. Beispielsweise ist die Abgrenzungsperiode vom 1. Januar 2018 bis zum 31. Januar 2018. In diesem Fall wir der Januar einbezogen, die Abgrenzung muss ausgeführt werden für den 1. Februar 2018.

- **Abgrenzungsperiodenstartdat um** – Dem Mitarbeiter wird Freizeit am ersten Tagder Prämienperiode bewilligt.

### <a name="accrual-policy-on-enrollment"></a>Abgrenzungsrichtlinie bei Registrierung

Die Abgrenzungsrichtlinie bei Registrierung definiert, wie die Abgrenzung berechnet wird, wenn ein Mitarbeiter mitten in einer Abgrenzungsperiode registriert wird. Die folgenden Optionen sind verfügbar:

- **Aufgeteilt** – Der Datumsbereich zwischen dem Registrierungsdatum und dem Startdatum wird verwendet, um die Differenz in Tagen zu bestimmen. Diese Differenz wird angewendet, wenn Abgrenzungen verarbeitet werden.
- **Vollständige Abgrenzung** – Der vollständige Abgrenzungsbetrag auf der Ebene ist während des ersten Abgrenzungsverarbeitens bewilligt.
- **Keine Abgrenzung** – Keine Abgrenzung wird auf die nächste Abgrenzungsperiode bewilligt.

### <a name="accrual-policy-on-unenrollment"></a>Abgrenzungsrichtlinie bei Nicht-Registrierung

Die Abgrenzungsrichtlinie bei Abmeldung definiert, wie die Abgrenzung berechnet wird, wenn ein Mitarbeiter mitten in einer Abgrenzungsperiode abgemeldet wird. Die folgenden Optionen sind verfügbar:

- **Aufgeteilt** – Der Datumsbereich zwischen dem Registrierungsdatum und dem Startdatum wird verwendet, um die Differenz in Tagen zu bestimmen. Diese Differenz wird angewendet, wenn Abgrenzungen verarbeitet werden.
- **Vollständige Abgrenzung** – Der vollständige Abgrenzungsbetrag auf der Ebene ist während des ersten Abgrenzungsverarbeitens bewilligt.
- **Keine Abgrenzung** – Keine Abgrenzung wird auf die nächste Abgrenzungsperiode bewilligt.

## <a name="accrual-schedule"></a>Abgrenzungszeitplan

Der Abgrenzungszeitplan bestimmt, wie ein Mitarbeiter Freizeit erhält und welche Beträge für den Mitarbeiter abgegrenzt und vorgetragen werden. Ebenen können erstellt werden, sodass Freizeit auf der Grundlage verschiedener Ebenen vergeben wird.

### <a name="months-of-service"></a>Dienstmonate

Der **Monate des Service**-Wert definiert die Mindestanzahl von Monaten, die Mitarbeiter arbeiten müssen, damit Abgrenzungen möglich werden. Wenn kein Minimum für Mitarbeiter erforderlich ist, legen Sie den Wert auf **0** fest.

### <a name="hours-worked"></a>Gearbeitete Stunden

Der **Gearbeitete Stunden**-Wert definiert die Mindestanzahl von Stunden, die Mitarbeiter arbeiten müssen, damit Abgrenzungen möglich werden. Wenn kein Minimum für Mitarbeiter erforderlich ist, legen Sie den Wert auf **0** fest.

### <a name="accrual-amount"></a>Antizipierungssumme

Der Abgrenzungsbetrag ist die Anzahl von Stunden oder die Tage, die Mitarbeiter pro Periode antizipieren. Der Zeitraum basiert auf der Antizipierungshäufigkeit.

### <a name="minimum-balance"></a>Mindestsaldo

Ein negativer Wert kann für den Mindestsaldo verwendet werden, wenn Mitarbeiter mehr Urlaub anfordern, als sie verfügen.

### <a name="maximum-carry-forward"></a>Maximaler Vortrag

Der Abgrenzungsprozess reguliert Urlaubsalden, die den maximalen Übertragsaldo für den Jahrestag des Startdatums im Feld überschreiten.

### <a name="grant-amount"></a>Zuschussbetrag

Der Zuschussbetrag ist die Anzahl von Stunden oder die Tage, die Mitarbeitern gewährt werden, wenn sie zuerst im Urlaubplan registriert werden. Der Betrag wird nicht für jede Abgrenzungsperiode antipiziert.

## <a name="enrollments-and-balances"></a>Registrierung und Salden

### <a name="enrollment-date"></a>Registrierungsdatum

Das Registrierungsdatum bestimmt, wenn ein Mitarbeiter beginnen kann, Freizeit zu antipizieren. Wenn ein Mitarbeiter zum Beispiel in einem Ferienplan am 15. Juni 2018 registriert wird, kann dieser keine Freizeit vor dem 15. Juni 2018 antipizieren.

### <a name="current-balance"></a>Aktueller Saldo

Der aktuelle Saldo ist der Betrag von Sonderurlaub, der für Freizeitanforderungen verfügbar ist. Dieser Betrag umfasst Abgrenzungen, genehmigte Anforderungen und Anpassungen durch das aktuelle Datum.

### <a name="current-balance-examples"></a>Aktueller Saldo, Beispiele

#### <a name="annual-plan"></a>Jährlicher Plan

**Planeinrichtung**

| Plan-Startdatum | Registrierungsdatum | Abgrenzungshäufigkeit | Abgrenzungsbasis | Zuerkennungsdatum für Anhäufungen    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/1/2018        | Jährlich            | Plan-Startdatum      | Enddatum des Anhäufungszeitraums |

Abgrenzungen werden am 1. Januar 2019 (1/1/2019) verarbeitet, damit die gesamte Periode enthalten ist.

**Ergebnisse**

| Antizipierungssumme | Mindestsaldo | Maximaler Vortrag | Angeforderter Betrag | Aktueller Saldo (per 1/1/2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 200            | 0               | 120                   | 40             | 160                              |

Aktueller Saldo (160) = Abgrenzungsbetrag (200 )– Dient zum Anfordern eines Betrag (40 )

#### <a name="semimonthly-plan"></a>Halbmonatlicher Plan

**Planeinrichtung**

| Plan-Startdatum | Registrierungsdatum | Abgrenzungshäufigkeit | Abgrenzungsbasis | Zuerkennungsdatum für Anhäufungen    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Halbmonatlich       | Plan-Startdatum      | Enddatum des Anhäufungszeitraums |

Abgrenzungen werden am 1. Mai 2018 (5/1/2018) verarbeitet, damit die gesamte Periode enthalten ist.

**Ergebnisse**

| Antizipierungssumme | Mindestsaldo | Maximaler Vortrag | Angeforderter Betrag | Aktueller Saldo (per 1/1/2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 22                               |

Aktueller Saldo (22) = Abgrenzungsbetrag (5 × 6 )– Dient zum Anfordern eines Betrags (8)

#### <a name="monthly-plan"></a>Monatlicher Plan

**Planeinrichtung**

| Plan-Startdatum | Registrierungsdatum | Abgrenzungshäufigkeit | Abgrenzungsbasis | Zuerkennungsdatum für Anhäufungen    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Halbmonatlich       | Plan-Startdatum      | Enddatum des Anhäufungszeitraums |

Abgrenzungen werden am 1. Mai 2018 (5/1/2018) verarbeitet, damit die gesamte Periode enthalten ist.

**Ergebnisse**

| Antizipierungssumme | Mindestsaldo | Maximaler Vortrag | Angeforderter Betrag | Aktueller Saldo (per 1/1/2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 7                                |

Aktueller Saldo (7) = Abgrenzungsbetrag (5 × 3 )– Dient zum Anfordern eines Betrag (8)

### <a name="forecasted-balance"></a>Geplanter Saldo

Der *Geplante Saldo* ist der Betrag für den Urlaub, der zu einem künftigen Zeitpunkt verfügbar ist. Abgrenzungen und Übertragregulierungen werden bis zu diesem Datum geplant.

Verwendete Formel:

Montag geplante Saldo = aktueller Saldo – Abgrenzungen + Anforderungen – Übertragregulierung

### <a name="forecasted-balance-examples"></a>Prognostizierte Saldobeispiele

#### <a name="annual-plan"></a>Jährlicher Plan

**Planeinrichtung**

| Plan-Startdatum | Registrierungsdatum | Abgrenzungshäufigkeit | Abgrenzungsbasis | Zuerkennungsdatum für Anhäufungen    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/1/2018        | Jährlich            | Plan-Startdatum      | Enddatum des Anhäufungszeitraums |

Abgrenzungen werden am 15. Februar 2019 (2/15/2019) verarbeitet, damit die gesamte Periode enthalten ist.

**Ergebnisse**

| Antizipierungssumme | Mindestsaldo | Maximaler Vortrag | Aktueller Saldo | Geplanter Saldo (per 2/15/2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 20             | 0               | 20                    | 40              | 40                                   |

Geplanter Saldo (40) = Antizipierter Betrag (20) + Aktueller Saldo (40) – Übertragregulierung (20)

#### <a name="semimonthly-plan"></a>Halbmonatlicher Plan

**Planeinrichtung**

| Plan-Startdatum | Registrierungsdatum | Abgrenzungshäufigkeit | Abgrenzungsbasis | Zuerkennungsdatum für Anhäufungen    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Halbmonatlich       | Plan-Startdatum      | Enddatum des Anhäufungszeitraums |

Abgrenzungen werden am 15. Februar 2019 (2/15/2019) verarbeitet, damit die gesamte Periode enthalten ist.

**Ergebnisse**

| Antizipierungssumme | Mindestsaldo | Maximaler Vortrag | Aktueller Saldo | Geplanter Saldo (per 2/15/2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 5              | 0               | 20                    | 40              | 35                                   |

Geplanter Saldo (35) = Antizipierter Betrag (5 × 3) + Aktueller Saldo (40) – Übertragregulierung (20)

#### <a name="monthly-plan"></a>Monatlicher Plan

**Planeinrichtung**

| Plan-Startdatum | Registrierungsdatum | Abgrenzungshäufigkeit | Abgrenzungsbasis | Zuerkennungsdatum für Anhäufungen    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Halbmonatlich       | Plan-Startdatum      | Enddatum des Anhäufungszeitraums |

Abgrenzungen werden am 15. Februar 2019 (2/15/2019) verarbeitet, damit die gesamte Periode enthalten ist.

**Ergebnisse**

| Antizipierungssumme | Mindestsaldo | Maximaler Vortrag | Aktueller Saldo | Geplanter Saldo (per 2/15/2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 10             | 0               | 20                    | 40              | 30                                   |

Geplanter Saldo (30) = Antizipierter Betrag (10 × 1) + Aktueller Saldo (40) – Übertragregulierung (20)

### <a name="proration-balance-examples"></a>Erzeugungskapazitätsaldo

#### <a name="prorated-monthly-plan"></a>Aufgeteilter Monatsplan

**Planeinrichtung**

| Plan-Startdatum | Abgrenzungshäufigkeit | Abgrenzungsbasis |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Monatlich           | Plan-Startdatum      |

**Ergebnisse**

| Mitarbeiter            | Dienstmonate | Registrierungsdatum | Startdatum | Antizipierungssumme | Antipizierungsprozess | Bilanz |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3,00    |
| Jay-Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1,00           | 9/1/2018        | 2.53    |

#### <a name="full-accrual-monthly-plan"></a>Monatsplan der vollständigen Abgrenzung

**Planeinrichtung**

| Plan-Startdatum | Abgrenzungshäufigkeit | Abgrenzungsbasis |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Monatlich           | Plan-Startdatum      |

**Ergebnisse**

| Mitarbeiter            | Dienstmonate | Registrierungsdatum | Startdatum | Antizipierungssumme | Antipizierungsprozess | Bilanz |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3,00    |
| Jay-Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1,00           | 9/1/2018        | 3,00    |

#### <a name="no-accrual-monthly-plan"></a>Kein monatlicher Antipizerungsplan

**Planeinrichtung**

| Plan-Startdatum | Abgrenzungshäufigkeit | Abgrenzungsbasis |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Monatlich           | Plan-Startdatum      |

**Ergebnisse**

| Mitarbeiter            | Dienstmonate | Registrierungsdatum | Startdatum | Antizipierungssumme | Antipizierungsprozess | Bilanz |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3,00    |
| Jay-Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1,00           | 9/1/2018        | 2.00    |
