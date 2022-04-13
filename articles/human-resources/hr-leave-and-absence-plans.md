---
title: Erstellen Sie einen Urlaubs- und Abwesenheitsplan
description: In diesem Thema wird beschrieben, wie Sie Urlaubspläne in Dynamics 365 Human Resources für verschiedene Urlaubsarten erstellen.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 47a0db91a1c27e1c0b1117da79d9f8d2abc665cb
ms.sourcegitcommit: 67c4ed957e43d4d60bb609d93921a0be9619e675
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8509583"
---
# <a name="create-a-leave-and-absence-plan"></a>Erstellen Sie einen Urlaubs- und Abwesenheitsplan

> [!Important]
> Die in diesem Thema beschriebene Funktionalität ist derzeit für Kunden der eigenständigen Version von Dynamics 365 Human Resources verfügbar. Einige oder die gesamten Funktionen werden in einem zukünftigen Release der Finance-Infrastruktur nach Finance-Version 10.0.26 verfügbar sein.


[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Urlaubs – und Abwesenheitspläne definieren in Dynamics 365 Human Resources für jede Art von Urlaub, den Sie anbieten. Urlaubs- und Abwesenheitspläne können mit unterschiedlichen Häufigkeiten anfallen, z. B. jährlich, monatlich oder halbmonatlich. Sie können Pläne auch als genehmigt definieren, wenn eine einzelne Abgrenzung an einem bestimmten Datum anfällt. Sie können beispielsweise einen Plan erstellen, der jährlich wechselnde Feiertage gewährt.

Mit gestuften Urlaubsplänen können Mitarbeiter Leistungen erhalten, die von der Zeit abhängen, die sie mit einer Organisation verbracht haben. Stufenpläne ermöglichen die automatische Registrierung für zusätzliche Leistungsstunden.

Sie können maximale Übertragungs- oder Mindestsalden festlegen, um sicherzustellen, dass die Mitarbeiter nur die von ihnen angesammelten Leistungsstunden verwenden.

Mit einem gestuften Plan können Sie beispielsweise neuen Mitarbeitern entlohnte Zeit von 80 Stunden (PTO) gewähren. Dann können Sie 120 Stunden von 60 Monaten Dienstzeit gewähren.

Sie können auch arbeitsplatzbezogene Urlaubsleistungen, z. B. nur für Führungskräfte erstellen.

## <a name="create-a-leave-plan"></a>Absenzplan erstellen

1. Auf der Seite **Urlaub- und Abwesenheit** klicken Sie auf **Neuen Plan erstellen**.

2. Unter **Einzelheiten**, geben Sie den **Namen**, **Anfangsdatum**, **Beschreibung**, und **Abwesenheitstyp** für Ihren Plan ein.

Wenn die Funktion **Konfigurieren Sie mehrere Urlaubstypen für einen einzelnen Urlaubs- und Abwesenheitsplan** aktiviert ist, werden Urlaubstypen im **Abgrenzungsplan** statt unter **Einzelheiten** konfiguriert. Für jeden Datensatz in der Abgrenzungstabelle können Sie eine Urlaubsart definieren. Wenn diese Funktion aktiviert ist, müssen Sie neue Datenentitäten für Integrationen oder andere Szenarien verwenden, in denen Sie Entitäten verwenden müssen. 

Die neuen Entitäten sind:

- Buchung für Urlaubs- und Abwesenheitszeitkonto V2
- Urlaubs- und Abwesenheitsregistrierung V2
- Stufe des Urlaubs- und Abwesenheitsplans V2
- Urlaubs- und Abwesenheitsplan V2
- Antrag auf arbeitsfreie Zeit V2

 > [!IMPORTANT]
   > Nachdem Sie dies Funktion aktiviert haben, können Sie diese nicht mehr deaktivieren.

3. Rückstellungen definieren in der Registerkarte **Rückstellungen**: Rückstellungen bestimmen, wann und wie oft ein Mitarbeiter freie Zeit erhält. In diesem Schritt definieren Sie Richtlinien über den Zeitpunkt von Abgrenzungen und Richtlinien zur Aufteilung von Urlaubsleistungen.

   1. Wählen Sie einen Wert aus dem Dropdown-Feld **Abgrenzungshäufigkeit**:

      - Täglich
      - Wöchentlich
      - Zweiwöchentlich
      - Halbmonatlich
      - Monatlich
      - Quartalsweise
      - Halbjährlich
      - Jährlich
      - Nichts

   2. Wählen Sie eine Option aus dem Dropdownfeld **Periodenabgrenzungsbasis**, um das Startdatum für die Berechnung der Abgrenzungsperioden zu bestimmen:

      | Abgrenzungsbasis | Beschreibung |
      | --- | --- |
      | **Plan-Startdatum** | Das Startdatum der Abgrenzungsperiode ist das Datum, an dem der Plan verfügbar ist. |
      | **Mitarbeiter spezifische Daten** | Das Startdatum der Abgrenzungsperiode hängt von einem Mitarbeiterereignis ab:</br><ul><li>Benutzerdefiniert (Sie müssen für jede einzelne Anmeldung ein Abgrenzungsdatum festlegen)</li><li>Jahrestag</li><li>Ursprüngliches Einstellungsdatum</li><li>Dienstalterdatum</li><li>Angepasstes Startdatum der Arbeitskraft</li><li>Startdatum der Arbeitskraft</li></ul> |

   3. Wählen Sie eine Option aus dem Dropdown-Feld **Stichtag der Abgrenzung**:

      - **Abgrenzungsperiodendatum** – Dem Mitarbeiter wird Freizeit am letzten Datum der Prämienperiode bewilligt. Um den richtigen Betrag abzugrenzen, muss der Abgrenzungsprozess die gesamte Periode enthalten. Wenn der Abgrenzungszeitraum beispielsweise vom 1. Januar 2020 bis zum 31. Januar 2020 ist, müssen Sie die Abgrenzung für den 1. Februar 2020 ausführen, um den Januar einzuschließen.

      - **Abgrenzungsperiodenstartdat um** – Dem Mitarbeiter wird Freizeit am ersten Tag der Prämienperiode bewilligt.

   4. Wählen Sie eine Option aus dem Dropdown-Feld **Abgrenzungsrichtlinie bei Registrierung**. Dieser Wert definiert, wie die Abgrenzung berechnet wird, wenn sich ein Mitarbeiter mitten in einer Abgrenzungsperiode anmeldet.

      - **Aufgeteilt** – Der Datumsbereich zwischen dem Registrierungsdatum und dem Startdatum wird verwendet, um die Differenz in Tagen zu bestimmen. Diese Differenz wird angewendet, wenn Abgrenzungen verarbeitet werden.

      - **Vollständige Abgrenzung** - Der vollständige Abgrenzungsbetrag auf der Ebene ist während des ersten Abgrenzungsverarbeitens bewilligt.

      - **Keine Abgrenzung** - Keine Abgrenzung wird auf die nächste Abgrenzungsperiode bewilligt.

   5. Wählen Sie eine Option aus dem Dropdown-Feld **Abgrenzungsrichtlinie bei der Abmeldung**. Dieser Wert definiert, wie die Abgrenzung berechnet wird, wenn sich ein Mitarbeiter mitten in einer Abgrenzungsperiode abmeldet.

      - **Aufgeteilt** – Der Datumsbereich zwischen dem Registrierungsdatum und dem Startdatum wird verwendet, um die Differenz in Tagen zu bestimmen. Diese Differenz wird angewendet, wenn Abgrenzungen verarbeitet werden.

      - **Vollständige Abgrenzung** – Der vollständige Abgrenzungsbetrag auf der Ebene ist während des ersten Abgrenzungsverarbeitens bewilligt.

      - **Keine Abgrenzung** – Keine Abgrenzung wird auf die nächste Abgrenzungsperiode bewilligt.

4. Definieren Sie den Abgrenzungsplan in der Registerkarte **Abgrenzungsplan**. Der Abgrenzungsplan bestimmt:

   - Wie ein Mitarbeiter Freizeit abgrenzt
   - Welche Beträge der Mitarbeiter anhäufen wird
   - Welche Beträge vorgetragen werden

   Sie können Ebenen erstellen, um Freizeit auf der Grundlage verschiedener Ebenen zu vergeben.

   Wenn sie Mitarbeiter im Stundensatz haben, können Sie Freizeit auf Grundlage der Stunden vergeben, anstelle der Anstellung bei der Organisation. Die Daten für die gearbeiteten Stunden werden in der Regel in einem Zeit- und in einem Anwesenheitssystem gespeichert. Sie können reguläre Arbeitsstunden und Überstunden aus dem Zeiterfassungssystem importieren und als Grundlage für die Auszeichnung eines Mitarbeiters verwenden.
   
    1. Wählen Sie eine Option aus dem Dropdown-Feld **Abgrenzungstyp**:

      - **Dienstmonate** – Den Abgrenzungsplan auf die Dienstmonate stützen.

      - **Arbeitsstunden** – Den Abgrenzungsplan auf die geleisteten Arbeitsstunden stützen. Weitere Informationen zu Rückstellungen für geleistete Arbeitsstunden finden Sie unter [Freizeit basierend auf geleisteten Arbeitsstunden](hr-leave-and-absence-plans.md?accrue-time-off-based-on-hours-worked).

      Weitere Informationen zu Rückstellungssaldi finden Sie unter [Freizeit basierend auf geleisteten Arbeitsstunden](hr-leave-and-absence-plans.md?enrollments-and-balances).

    2. Geben Sie Werte in den Abgrenzungszeitplan ein:

      - **Dienstmonate**- Wert definiert die Mindestanzahl von Monaten, die Mitarbeiter arbeiten müssen, damit Abgrenzungen möglich werden. Wenn Sie kein Minimum benötigen, setzen Sie den Wert auf 0.

      - **Gearbeitete Stunden**- Wert definiert die Mindestanzahl von Stunden, die Mitarbeiter arbeiten müssen, damit Abgrenzungen möglich werden. Wenn Sie kein Minimum benötigen, setzen Sie den Wert auf 0.

      - **Abgrenzungsbetrag** - Die Anzahl von Stunden oder die Tage, die Mitarbeiter pro Periode antizipieren. Der Zeitraum basiert auf der Antizipierungshäufigkeit.

      - **Mindestsaldo** -Ein negativer Wert kann für den Mindestsaldo verwendet werden, wenn Mitarbeiter mehr Urlaub anfordern, als sie verfügen.

      - **Maximaler Übertragssaldo** - Der Abgrenzungsprozess reguliert Urlaubsaldi, die den maximalen Übertragsaldo für den Jahrestag des Startdatums im Feld überschreiten.

      - **Zuschussbetrag** - Dies is die Anzahl von Stunden oder die Tage, die Mitarbeitern gewährt werden, wenn sie zuerst im Urlaubplan registriert werden. Der Betrag wird nicht für jede Abgrenzungsperiode antipiziert.
      
Wenn die Funktion **Konfigurieren Sie mehrere Urlaubstypen für einen einzelnen Urlaubs- und Abwesenheitsplan** aktiviert ist, wählen Sie eine Option **Typ verlassen** aus. 

   > [!IMPORTANT]
   > Nachdem Sie dies Funktion aktiviert haben, können Sie diese nicht mehr deaktivieren.

Wenn die Funktion **Festgelegte Vollzeitäquivalen nutzen** aktiviert ist, nutzt die Personalabteilung die für die Position festgelegte Vollzeitäquivalenz (FTE), um die Rückstellung eines Mitarbeiters aufzuteilen. Wenn zum Beispiel der VZÄ 0,5 beträgt und der Abgrenzungsbetrag 10 beträgt, wird der Mitarbeiter 5 abgrenzen. Sie können diese Funktion nur verwenden, wenn Sie mehrere Urlaubsarten aktivieren.  

5. Wählen Sie **Speichern**.

## <a name="accrue-time-off-based-on-hours-worked"></a>Abgrenzen der arbeitsfreien Zeit auf Grundlage der gearbeiteten Stunden

Wenn sie Mitarbeiter im Stundensatz haben, können Sie Freizeit auf Grundlage der Stunden vergeben, anstelle der Anstellung bei der Organisation. Die Daten für die gearbeiteten Stunden werden in der Regel in einem Zeit- und in einem Anwesenheitssystem gespeichert. Sie können reguläre Arbeitsstunden und Überstunden aus Ihrem Zeiterfassungssystem importieren und als Grundlage für die Auszeichnung eines Mitarbeiters verwenden.

Wenn gearbeitete Stunden als Abgrenzungstyp ausgewählt haben, gibt es zwei Typen von Stunden, die zur Abgrenzung verwendet werden können: reguläre Stunden und Überstunden. Der Abgrenzungsprozess für gearbeitet Stunden nutzt die Antizipierungshäufigkeit, zusammen mit der Abgrenzungsperiodengrundalge, die die abzugrenzenden Stunden bestimmt.

### <a name="annual-accrual-frequency"></a>Jährliche Antizipierungshäufigkeit

| Bewilligungsdatum der Abgrenzung    | Gearbeitete Stundenbasis    | Antizipierungssumme        | Arbeitsstunden-Daten   | Aktuell gearbeitete Stunden| Prämie               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 12/31/2018            | 2080                 | 144                   | 1/1/2018-12/31/2018  | 2085                | 144                 |        
| 12/31/2018            | 2080                 | 144                   | 1/1/2018-12/31/2018  | 2000                | 0                 |


### <a name="monthly-accrual-frequency"></a>Monatliche Antizipierungshäufigkeit

| Bewilligungsdatum der Abgrenzung    | Gearbeitete Stundenbasis    | Antizipierungssumme        | Arbeitsstunden-Daten   | Aktuell gearbeitete Stunden| Prämie               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 160                  | 12                    | 8/1/2018-8/31/2018   | 184                 | 12                  |        
| 8/31/2018             | 160                  | 3                     | 8/1/2018-8/31/2018   | 184                 | 3                   |

### <a name="semi-monthly-accrual-frequency"></a>Halb-monatliche Antizipierungshäufigkeit

| Bewilligungsdatum der Abgrenzung    | Gearbeitete Stundenbasis    | Antizipierungssumme        | Arbeitsstunden-Daten   | Aktuell gearbeitete Stunden| Prämie               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 80                   | 6                     | 8/16/2018-8/31/2018  | 8.1                  | 6                  |        
| 8/31/2018             | 80                   | 6                     | 8/16/2018-8/31/2018  | 75                  | 0                   |

### <a name="weekly-accrual-frequency"></a>Wöchentliche Antizipierungshäufigkeit

| Bewilligungsdatum der Abgrenzung    | Gearbeitete Stundenbasis    | Antizipierungssumme        | Arbeitsstunden-Daten   | Aktuell gearbeitete Stunden| Prämie               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 40                   | 3                     | 8/27/2018-8/31/2018  | 42                  | 3                  |        
| 8/31/2018             | 40                   | 3                     | 8/27/2018-8/31/2018  | 35                  | 0                   |

### <a name="employee-assigned-leave-plans"></a>Mitarbeitern zugewiesene Urlaubspläne

In den den Mitarbeitern zugewiesenen Urlaubpläne wird die Basisebene und die Art der Stunden für die Pläne angezeigt. Die tatsächlichen Arbeitsstunden für die Abgrenzungsperioden ab dem aktuellen Datum werden ebenfalls als Referenz angezeigt.

### <a name="loading-data"></a>Daten werden geladen

Tatsächliche Stunden können mithilfe von **Urlaubs- und Abwesenheitsstunden** der Entität in der Datenverwaltung verwendet werden. Wenn Sie Arbeitszeitkalender verwenden, überprüft der Import, dass die regulären gearbeiteten Stunden die geplanten Stunden in einem Tag nicht überschreitet, die anhand des Kalenders definiert wurden. Der Import prüft auch, dass die Stunden, die für einen bestimmten Tag gearbeitet werden, 24 Stunden nicht übersteigt. 

Die folgenden Informationen werden benötigt, um die tatsächlichen Arbeitsstunden, die im Urlaubabgrenzungsprozess verwendet werden, zu importieren:

- Personalnummer 
- Datum Arbeitstag
- Typ
- Stunden

Ein einzelnes Datum kann nur je einen zugeordneten Typ haben.

| Personalnummer       | Datum Arbeitstag           | Typ                  | Stunden                |
| --------------------- | -------------------- | --------------------- | -------------------- |
| 000337                | 8/6/2018             | Regelmäßig               | 8                    |       
| 000337                | 8/7/2018             | Regelmäßig               | 8                    |
| 000337                | 8/7/2018             | Überstunden              | 3                    |
| 000337                | 8/8/2018             | Regelmäßig               | 8                    |
| 000337                | 8/7/2018             | Regelmäßig               | 8                    |
| 000337                | 8/9/2018             | Regelmäßig               | 8                    |

## <a name="enrollments-and-balances"></a>Registrierung und Salden

### <a name="enrollment-date"></a>Registrierungsdatum

Das Registrierungsdatum bestimmt, wenn ein Mitarbeiter beginnen kann, Freizeit zu antipizieren. Wenn ein Mitarbeiter zum Beispiel in einem Ferienplan am 15. Juni 2018 registriert wird, kann dieser keine Freizeit vor dem 15. Juni 2018 antipizieren.

### <a name="current-balance"></a>Aktueller Saldo

Der aktuelle Saldo ist der Betrag von Sonderurlaub, der für die Freizeitanforderungen verfügbar ist. Dieser Betrag umfasst Abgrenzungen, genehmigte Anforderungen und Anpassungen durch das aktuelle Datum.

### <a name="current-balance-examples"></a>Aktueller Saldo, Beispiele

#### <a name="annual-plan"></a>Jährlicher Plan

**Planeinrichtung**

| Plan-Startdatum | Registrierungsdatum | Abgrenzungshäufigkeit | Abgrenzungsbasis | Zuerkennungsdatum für Anhäufungen    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/1/2018        | Jährlich            | Plan-Startdatum      | Enddatum des Anhäufungszeitraums |

Abgrenzungen werden am 1. Januar 2019 (1/1/2019) verarbeitet, damit die gesamte Periode darin enthalten ist.

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

Abgrenzungen werden am 1. Mai 2018 (5/1/2018) verarbeitet, damit die gesamte Periode darin enthalten ist.

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

Abgrenzungen werden am 1. Mai 2018 (5/1/2018) verarbeitet, damit die gesamte Periode darin enthalten ist.

**Ergebnisse**

| Antizipierungssumme | Mindestsaldo | Maximaler Vortrag | Angeforderter Betrag | Aktueller Saldo (per 1/1/2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 7                                |

Aktueller Saldo (7) = Abgrenzungsbetrag (5 × 3 )– Dient zum Anfordern eines Betrag (8)

### <a name="forecasted-balance"></a>Planungssaldo

Der *geplante Saldo* ist der Betrag für den Urlaub, der zu einem künftigen Zeitpunkt verfügbar ist. Abgrenzungen und Übertragregulierungen werden bis zu diesem Datum geplant.

Die Personalabteilung verwendet die folgende Formel:

Montag geplante Saldo = aktueller Saldo – Abgrenzungen + Anforderungen – Übertragregulierung

### <a name="forecasted-balance-examples"></a>Prognostizierte Saldobeispiele

#### <a name="annual-plan"></a>Jährlicher Plan

**Planeinrichtung**

| Plan-Startdatum | Registrierungsdatum | Abgrenzungshäufigkeit | Abgrenzungsbasis | Zuerkennungsdatum für Anhäufungen    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/1/2018        | Jährlich            | Plan-Startdatum      | Enddatum des Anhäufungszeitraums |

Abgrenzungen werden am 15. Februar 2019 (2/15/2019) verarbeitet, damit die gesamte Periode darin enthalten ist.

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

Abgrenzungen werden am 15. Februar 2019 (2/15/2019) verarbeitet, damit die gesamte Periode darin enthalten ist.

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

Abgrenzungen werden am 15. Februar 2019 (2/15/2019) verarbeitet, damit die gesamte Periode darin enthalten ist.

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
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3.00    |
| Jay-Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1.00           | 9/1/2018        | 2.00    |

## <a name="see-also"></a>Siehe auch

- [Urlaubs- und Abwesenheitsübersicht](hr-leave-and-absence-overview.md)
- [Urlaubs- und Abwesenheitstypen konfigurieren](hr-leave-and-absence-types.md)
- [Urlaubs- und Abwesenheitspläne antizipieren](hr-leave-and-absence-accrue.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
