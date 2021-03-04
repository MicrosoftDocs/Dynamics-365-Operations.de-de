---
title: Leasingbuchungsarten
description: In diesem Thema werden die Buchungsarten beschrieben, die für Anlagenleasing-Transaktionen verwendet werden.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ceb4fbeb4dbf2f535e05a9d46c84169435d2803b
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4443784"
---
# <a name="lease-posting-types"></a>Leasingbuchungsarten

[!include [banner](../includes/banner.md)]

In diesem Thema werden die Buchungsarten beschrieben, die für Anlagenleasing-Transaktionen verwendet werden.

## <a name="lease-asset"></a>Leasingobjekt

Das Konto ist mit dem Nutzungsrecht am Leasingobjekt verknüpft. Dieses Konto wird belastet, wenn ein Mietvertrag zum ersten Mal gemäß den neuen Mietbilanzierungsstandards, dem Kodifizierungsthema 842 (ASC 842) und dem International Financial Reporting Standard 16 (IFRS 16) erfasst wird. Bei einem geänderten Mietvertrag kann dieses Konto entweder belastet oder gutgeschrieben werden, je nachdem, ob die Änderung die Mietverbindlichkeit erhöht oder verringert.

**Beispieljournaleinträge:** Erstmalige Erfassung<br>
**Soll:** Mietanlage XXX<br>
**Haben:** Leasingverbindlichkeit XXX

## <a name="lease-liability"></a>Leasingverbindlichkeit

Das Konto ist mit der Leasingverbindlichkeit verbunden, die entsteht, wenn Zahlungen nach den neuen Standards IFRS 16 und ASC 842 abgezinst werden. Dieses Konto wird gutgeschrieben, wenn ein Mietvertrag nach den neuen Standards erstmals anerkannt wird. Es wird für Mietzahlungen belastet und für Zinsabgrenzungen gutgeschrieben.

**Beispieljournaleinträge:** Erstmalige Erfassung<br>
**Soll:** Mietanlage XXX<br>
**Haben:** Leasingverbindlichkeit XXX

**Beispieljournaleinträge:** Zinsabgrenzung<br>
**Soll:** Zinsausgaben XXX<br>
**Haben:** Leasingverbindlichkeit XXX

**Beispieljournaleinträge:** Mietzahlung<br>
**Soll:** Leasingverbindlichkeit XXX<br>
**Haben:** Kreditorenzahlung/Leasingzahlung XXX

## <a name="short-term-lease-liability"></a>Kurzfristige Leasingverbindlichkeiten

Das Konto ist mit der kurzfristigen Leasingverbindlichkeit verbunden, wenn der Journaleintrag für die kurzfristige Leasingverbindlichkeit neu gebucht wird. Diesem Konto wird die kurzfristige Verbindlichkeit aus dem Tilgungsplan am letzten Tag des Monats gutgeschrieben. Der gleiche Betrag wird jedoch am ersten Tag des nächsten Monats abgebucht.

**Beispieljournaleinträge:** Umgliederung der kurzfristigen Leasingverbindlichkeit<br>
**Soll:** Leasingverbindlichkeit XXX<br>
**Haben:** Kurzfristige Leasingverbindlichkeit XXX<br>
**Soll:** Kurzfristige Leasingverbindlichkeit XXX<br>
**Haben:** Leasingverbindlichkeit XXX

## <a name="depreciation-expense"></a>Abschreibungsausgaben

Das Konto ist mit dem Aufwand verbunden, der im Zusammenhang mit der Abschreibung des Nutzungsrecht am Leasingobjekt nach IFRS 16, ASC 842 und Finanzierungsleasing nach IAS 17 und ASC 840 steht. Dieses Konto wird belastet, wenn ein Nutzungsrecht am Leasingobjekt jeden Monat abgeschrieben wird.

**Beispieljournaleinträge:** Abschreibungsabgrenzung<br>
**Soll:** Abschreibungsausgaben XXX<br>
**Haben:** Kumulierte Abschreibung XXX

## <a name="gainloss-on-lease-modification"></a>Gewinn/Verlust bei Änderung des Mietvertrags

Das Konto ist mit Gewinnen oder Verlusten verbunden, die sich aus Mietvertragsänderungen ergeben. Ein Gewinn kann während einer Mietvertragsänderung entstehen, wenn die Änderung die Leasingverbindlichkeit um einen Betrag verringert, der den Buchwert des Nutzungsrecht am Leasingobjekts übersteigt.

Beispielsweise hat ein Mietvertrag einen aktuellen Buchwert der Leasingverbindlichkeit von 150.000 USD und einen Buchwert des Nutzungsrecht am Leasingobjekts von 100.000 USD. Der mietvertrag wird geändert, und diese Änderung ergibt einen neuen Barwert der zukünftigen Mindestleasingzahlungen (PVFMLP) von 40.000 USD. Daher wird die Leasingverbindlichkeit von 110.000 USD (150.000 USD – 40.000 USD) belastet. Da das Nutzungsrecht am Leasingobjekt nur 100.000 USD ist, verringert die Verringerung von 110.000 USD der Anlage nach 0 (Null). In den Bilanzierungsrichtlinien heißt es daher, dass der Rest auf ein Gewinnkonto gebucht werden sollte. In diesem Fall ist der endgültige Journaleintrag eine Belastung der Leasingverbindlichkeit für 110.000 USD, eine Gutschrift für das Mietobjekt für 100.000 USD und eine Gutschrift für das Gewinnkonto für 10.000 USD.

**Beispieljournaleinträge:** Mietvertragsänderungen<br>
**Soll:** Leasingverbindlichkeit XXX<br>
**Haben:** Mietanlage XXX<br>
**Haben:** Gewinn XXX

## <a name="accumulated-depreciation"></a>Kumulierte Abschreibung

Das Konto ist dem Gegen-Anlagenkonto des Nutzungsrecht am Leasingobjekt zugeordnet. Auf diesem Konto erfolgt beim Buchen einer Abschreibungsausgabe eine Habenbuchung.

**Beispieljournaleinträge:** Abschreibungsabgrenzung<br>
**Soll:** Abschreibungsausgaben XXX<br>
**Haben:** Kumulierte Abschreibung XXX

## <a name="retained-earnings"></a>Nicht ausgeschüttete Gewinne

Das den Anfangssalden zugeordnete Konto. Dieses Konto kann entweder in einem Journaleintrag für die Übergangsregulierung unter Verwendung der vollständigen retrospektiven Methode oder der Methode der kumulativen Nachholoption A belastet oder gutgeschrieben werden. Die Differenz zwischen dem anfänglichen Nutzungsrecht am Leasingobjekt und der Leasingverbindlichkeit wird in den Gewinnrücklagen verbucht. In seltenen Fällen können die Gewinnrücklagen auch während der Änderung des Mieterhältnisses beeinflusst werden, wenn die Klassifizierung eines Mietvertrags von „Finanzierung“ in„Betrieb“ geändert wird, um den ROU-Vermögenswert so hoch oder runter zu schreiben, dass er der Leasingverbindlichkeit entspricht.

**Beispieljournaleinträge:** Übergangsregulierung (vollständige retrospektive oder kumulative Nachholoption A-Methode)<br>
**Soll:** Leasingverbindlichkeit XXX<br>
**Haben:** Mietanlage XXX<br>
**Haben:** Nicht ausgeschüttete Gewinne XXX

## <a name="variable-payment"></a>Variable Zahlung

Das Konto ist mit variablen Mietzahlungen verbunden, die durch eine Indexneubewertung gemäß Mietverträgen nach ASC 842, ASC 840 und IAS 17 erzielt werden. Im Mietzahlungsplan sind variable Zahlungen in der Spalte **Variable Zahlung** enthalten. Dieses Konto wird belastet, wenn eine Rechnung für eine Zahlungsplanzeile erstellt wird, die eine variable Zahlung enthält.

**Beispieljournaleinträge:** Mietzahlung<br>
**Soll:** Leasingverbindlichkeit XXX<br>
**Soll:** Variable Zahlung XXX<br>
**Haben:** Kreditorenzahlung/Leasingzahlung XXX

## <a name="deferred-rent-asset-liability"></a>Zurückgestellter Mietaufwand für Anlage (Verbindlichkeit)

Das Konto ist mit der Forderung des zurückgestellten Mietaufwands oder der Verbindlichkeit aus einem Mietvertrag mit Behandlung von zurückgestelltem Mietaufwand verbunden. Dieses Konto wird belastet, wenn eine Rechnung gegen ein Mietvertrag mit Behandlung von zurückgestelltem Mietaufwand gebucht wird, wenn der Mietzahlungsbetrag den linearen Mietaufwand des Zeitraums übersteigt. Es wird gutgeschrieben, wenn die Mietzahlung unter dem linearen Mietaufwand des Zeitraums liegt.

**Beispieljournaleinträge:** Mietzahlung (Mietvertrag mit Behandlung von zurückgestelltem Mietaufwand)<br>
**Soll:** Mietkosten XXX<br>
**Haben:** Zurückgestellter Mietaufwand für Verbindlichkeit XXX<br>
**Haben:** Kreditorenzahlung/Leasingzahlung XXX

## <a name="lease-expense"></a>Mietvertragsausgaben

Das Konto ist mit dem Mietaufwand verbunden, wenn der Mietvertrag als Mietvertrag mit Behandlung von zurückgestellem Mietaufwand eingestuft wird. Dieses Konto wird belastet, wenn eine Rechnung gegen ein Mietvertrag mit Behandlung von zurückgestelltem Mietaufwand gebucht wird.

**Beispieljournaleinträge:** Mietzahlung (Mietvertrag mit Behandlung von zurückgestelltem Mietaufwand)<br>
**Soll:** Mietkosten XXX<br>
**Haben:** Zurückgestellter Mietaufwand für Verbindlichkeit XXX<br>
**Haben:** Kreditorenzahlung/Leasingzahlung XXX

## <a name="impairment-expense"></a>Aufwand der dauerhaften Wertminderung

Das Konto wird gebucht, wenn ein Mietvertrag wertgemindert ist. Dieses Konto wird belastet, während das Konto für das Nutzungsrecht am Leasingobjekt direkt gutgeschrieben wird.

**Beispieljournaleinträge:** Mietzahlung<br>
**Soll:** Aufwand der dauerhaften Wertminderung XXX<br>
**Haben:** Nutzungsrecht am Leasingobjekt XXX

## <a name="lease-payment"></a>Mietzahlung

Das Konto wird gegen gebucht, wenn der **An Kreditor bezahlen**-Parameter ausgeschaltet ist. Dieses Konto wird anstelle des Kreditors gutgeschrieben, wenn der Parameter deaktiviert ist.

**Beispieljournaleinträge:** Mietzahlung<br>
**Soll:** Leasingverbindlichkeit XXX<br>
**Haben:** Mietzahlung XXX

## <a name="expense-type-postings"></a>Buchungen des Ausgabentyps

Das für jede Ausgabenart ausgewählte Konto wird belastet, wenn eine Zahlung für diese Ausgabenart generiert wird. Zum Beispiel wird das Konto, das für die Kostenart **Versicherung** angegeben ist, immer dann belastet, wenn eine Rechnung oder ein Zahlungsjournaleintrag aus dem Plan für Nebenkosten beim Leasing bei Versicherungskosten erstellt wird.

**Beispieljournaleinträge:** Versicherungszahlung<br>
**Soll:** Versicherungskostenartkonto XXX<br>
**Haben:** Gegenkonto XXX

> [!NOTE]
> Das Gegenkonto wird auf Mietvertragsebene in den Zeilen für den Zahlungsplan für die Nebenkosten beim Leasing ausgewählt. Dieses Gegenkonto kann dem Kreditor oder einem Sachkonto zugeordnet werden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]