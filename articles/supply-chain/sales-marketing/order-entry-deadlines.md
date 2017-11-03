---
title: "Fristen für Auftrag"
description: "Dieser Artikel enthält Informationen zu Auftragserfassungsfristen. Eine Auftragserfassungsfrist ist eine Sperrzeit, die bestimmt, ob ein Kundenauftrag als am aktuellen Tag oder dem nächsten Tag empfangen behandelt (und erfüllt) werden soll."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventOrderEntryDeadlineGroup, InventOrderEntryDeadlineParameters, InventOrderEntryDeadlineTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 7151
ms.assetid: bbc4f9a2-df4b-4d92-9f18-25282a85541f
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9e9d1912abf9a356542ce2c317fa717bc991dbf9
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="order-entry-deadlines"></a>Fristen für Auftrag

[!include[banner](../includes/banner.md)]


Dieser Artikel enthält Informationen zu Auftragserfassungsfristen. Eine Auftragserfassungsfrist ist eine Sperrzeit, die bestimmt, ob ein Kundenauftrag als am aktuellen Tag oder dem nächsten Tag empfangen behandelt (und erfüllt) werden soll.

In vielen Unternehmen werden Aufträge, die bis zu einer bestimmten Uhrzeit eingegangen sind, so behandelt, als er wären sie am gleichen Tag erfasst worden. Alle Aufträge, die nach diesem Zeitpunkt eingehen, werden so behandelt, als ob sie am nächsten Werktag eingehen. Diese Sperrzeit für Aufträge wird Frist für die Auftragserfassung genannt.  

Fristen für die Auftragserfassung werden als Eingabe die Lieferterminzusage verwendet. Dadurch helfen sie beim Verwalten der Debitorenerwartungen bezüglich der Auftragslieferungen. So können Debitoren sehen, dass Sie beim Bestellen eines Auftrags vor einem bestimmten Zeitpunkt die Waren am selben Tag versenden. Wenn sie diese Frist fehlen, können sie die Lieferung nur am folgenden Arbeitstag ein. Sie setzen Auftragsfristen auf Grundlage Ihrer Lagerortfunktionen und Spediteurzeitpläne.  

Auf der Seite **Fristen für Auftrag** richten Sie die Fristen für die Auftragserfassung für alle Wochentage ein. Wenn Aufträge nach den angegebenen Zeitpunkten eingehen, werden sie so behandelt, als ob sie am nächsten Werktag eingehen. Standardmäßig ist diese Frist auf 23:59 Uhr (also auf eine Minute vor Mitternacht am Ende des jeweiligen Tages) festgelegt. Diese Standardzeiten können so geändert werden, dass sie mit den tatsächlichen Versand- oder Auftragsfristen übereinstimmen.  

Auftragsfristen können für eine bestimmte Debitorengruppe festgelegt werden. Dies kann beispielsweise hilfreich sein, wenn einer bestimmten Debitorengruppe eine spätere Auftragsfrist als anderen Debitoren gewährt werden soll. In diesem Fall definieren Sie zunächst Gruppen für Fristen für Aufträge auf der Seite **Fristengruppen für Auftrag**. Anschließend weisen Sie Gruppen zu Debitoren auf der Seite **Debitoren** zu.  

Verfügt das Unternehmen über mehrere Standorte, lassen sich Auftragsfristen für die einzelnen Standorte einrichten. Befinden sich die Standorte in unterschiedlichen Zeitzonen, erfolgt die Einrichtung der Auftragsfristen gemäß der Zeitzone des Standorts. Beim Arbeiten mit Aufträgen und Verkaufsangeboten wird die Auftragsfrist jedoch auf der Seite **Verfügbare Versand- und Eingangsdaten** in die eigene Zeitzone konvertiert.  

Auf der Seite **Fristenkombinationen für Aufträge aktivieren** definieren Sie die Kombinationen von Standorten und Fristengruppen für Aufträge, die zulässig sind.

## <a name="example-order-entry-deadline"></a>Beispiel: Auftragsfrist
Die Frist für den Auftrag an Dienstagen wurde auf 16:00 festgelegt. An einem bestimmten Dienstag versuchen Sie um 17:00 Uhr, das aktuelle Datum als Versanddatum festzulegen. (Beachten Sie, dass es keine Lieferzeit für dieses Beispiel gibt). Wenn das Kontrollkästchen **Lieferdatumskontrolle** aktiviert ist, erhalten Sie eine Warnung, dass das Datum nicht gültig ist. Diese Warnung wird auf der Seite **Verfügbare Versand- und Eingangsdaten** angezeigt, auf der Sie dann auch alternative Daten auswählen können.

## <a name="example-different-order-entry-deadlines-per-site"></a>Beispiel: Unterschiedliche Auftragsfristen pro Standort
Ihr Unternehmen verfügt über zwei Standorte. Die Standorte befinden sich in verschiedenen Zeitzonen, wie in der folgenden Tabelle gezeigt.

| Standort A                      | Standort B                      |
|-----------------------------|-----------------------------|
| Kalifornien                  | Florida                     |
| PST (Pacific Normalzeit) | EST (Eastern Normalzeit) |

Für Standort A und B sind die folgenden Auftragsfristen definiert.

| Tag der Woche             | A: Fristen für Auftrag (PST) | B: Fristen für Auftrag (EST) |
|-----------------------------|--------------------------------|--------------------------------|
| Montag                      | 13:00                          | 14:00                          |
| Dienstag                     | 13:00                          | 14:00                          |
| Mittwoch                   | 13:00                          | 14:00                          |
| Donnerstag                    | 13:00                          | 14:00                          |
| Freitag                      | 13:00                          | 14:00                          |

Sie sind Auftragsbearbeiter und befinden sich in Utah, also in der Zeitzone MST (Mountain Normalzeit). Das bedeutet Folgendes: Sofern Aufträge für Standort A bis spätestens 14:00 Uhr (MST) und Aufträge für Standort B bis spätestens 12:00 Uhr (MST) erteilt werden, werden die Auftragsfristen beider Standorte eingehalten.  

In der folgenden Tabelle sind die in MST umgerechneten Auftragsfristen für Standort A und B dargestellt.

| Standort A (PST)         | Standort A (MST)        | Standort B (EST)           | Standort B (MST)        |
|---------------------|--------------------|-----------------------|--------------------|
| 13:00               | 14:00              | 14:00                 | 12:00              |

**Hinweis:** Falls die Anpassung auf Sommerzeit aktiviert ist, werden die Auftragsfristen entsprechend angeglichen.

## <a name="example-same-order-entry-deadline-per-site"></a>Beispiel: Gleiche Auftragsfrist pro Standort
Ihr Unternehmen verfügt über zwei Standorte. Die Standorte befinden sich in verschiedenen Zeitzonen, wie in der folgenden Tabelle gezeigt.

| Standort A                      | Standort B                      |
|-----------------------------|-----------------------------|
| Kalifornien                  | Florida                     |
| PST (Pacific Normalzeit) | EST (Eastern Normalzeit) |

Für Standort A und B sind die folgenden Auftragsfristen definiert.

| Tag der Woche | PST und EST |
|-----------------|-------------|
| Montag          | 13:00       |
| Dienstag         | 13:00       |
| Mittwoch       | 13:00       |
| Donnerstag        | 13:00       |
| Freitag          | 13:00       |

Sie sind Auftragsbearbeiter und befinden sich in Utah, also in der Zeitzone MST (Mountain Normalzeit). Das bedeutet Folgendes: Sofern Aufträge für Standort A bis spätestens 14:00 Uhr (MST) und Aufträge für Standort B bis spätestens 11:00 Uhr (MST) erteilt werden, werden die Auftragsfristen beider Standorte eingehalten. 

In der folgenden Tabelle sind die in MST umgerechneten Auftragsfristen für Standort A und B dargestellt.

| Standort A (PST)         | Standort A (MST)        | Standort B (EST)           | Standort B (MST)        |
|---------------------|--------------------|-----------------------|--------------------|
| 13:00               | 14:00              | 13:00                 | 11:00              |

**Hinweis:** Falls die Anpassung auf Sommerzeit aktiviert ist, werden die Auftragsfristen entsprechend angeglichen.

<a name="see-also"></a>Siehe auch
--------

[Lieferzeitpläne](delivery-schedules.md)




