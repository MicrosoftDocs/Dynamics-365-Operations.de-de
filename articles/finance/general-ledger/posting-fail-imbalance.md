---
title: Fehler bei der Erfassung von Erfassungen aufgrund eines Ungleichgewichts
description: Dieses Thema erklärt, warum Soll- und Habenbeträge in Belegtransaktionen möglicherweise nicht ausgeglichen sind, so dass die Transaktionen nicht gebucht werden können. Das Thema enthält auch Schritte zur Behebung des Problems.
author: kweekley
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-8-03
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: fc413f8230849653aef8c2951f1749823edded6e
ms.sourcegitcommit: 25b3dd639e41d040c2714f56deadaa0906e4b493
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/06/2021
ms.locfileid: "7605428"
---
# <a name="journal-posting-failure-because-of-imbalance"></a>Fehler bei der Erfassung von Erfassungen aufgrund eines Ungleichgewichts

[!include [banner](../includes/banner.md)]

Dieses Thema erklärt, warum Soll- und Habenbeträge in Belegtransaktionen möglicherweise nicht ausgeglichen sind, so dass die Transaktionen nicht gebucht werden können. Das Thema enthält auch Schritte zur Behebung des Problems.

## <a name="symptom"></a>Symptom

In manchen Fällen kann eine Erfassung nicht gebucht werden, und es wird die folgende Nachricht angezeigt: "Die Transaktionen auf einem bestimmten Beleg sind ab einem bestimmten Datum nicht ausgeglichen (Buchhaltungswährung: 0,01 - Berichtswährung: 0,06)." Warum kann die Erfassung nicht gebucht werden?

## <a name="resolution"></a>Lösung

Beim Buchen im Hauptbuch muss jeder Beleg in der Transaktionswährung, der Buchhaltungswährung und der Berichtswährung ausgeglichen werden, wenn diese Währungen auf der Seite **Einrichtung des Hauptbuchs** definiert sind. (Belege sind ausgeglichen, wenn die Summe der Belastungen gleich der Summe der Gutschriften ist).

Unten auf der Seite mit den Buchungsblattzeilen werden die Summen in der Buchungswährung und der Berichtswährung angezeigt. Sie werden **nicht** in der Transaktionswährung für Fremdwährungstransaktionen angezeigt. Außerdem zeigt die Fehlermeldung, die Benutzer während der Simulation oder Buchung erhalten, die Differenzen nur in der Buchhaltungswährung und der Berichtswährung an. Sie werden nicht in der Transaktionswährung angezeigt, da ein einzelner Beleg mehr als eine Transaktionswährung haben kann und das Journal Belege in verschiedenen Transaktionswährungen enthalten kann. Daher ist es wichtig, dass Sie manuell überprüfen, ob die Transaktionswährungsbeträge für jeden Beleg mit nur einer Transaktionswährung ausgeglichen sind.

### <a name="transaction-currency"></a>Buchungswährung

Während der Simulation und Buchung prüft das System, dass jeder Beleg mit nur einer Transaktionswährung in der Transaktionswährung ausgeglichen ist. Für jeden eingegebenen Beleg kann es eine oder mehrere Währungen als Transaktionswährung geben. Ein Beleg, der im Allgemeinen Erfassungen eingegeben wird, kann z.B. zwei Transaktionswährungen haben, wenn Bargeld von einem Bankkonto, das Euro (EUR) verwendet, auf ein Bankkonto, das kanadische Dollar (CAD) verwendet, übertragen wird.

Wenn ein Beleg nur eine Transaktionswährung hat, muss die Summe der Belastungen der Summe der Gutschriften für diesen Beleg in der Transaktionswährung entsprechen. Kunden sind auf die folgenden Szenarien gestoßen, in denen die Buchung korrekt fehlgeschlagen ist, weil die Beträge der Transaktionswährungen nicht ausgeglichen waren:

- Die Gesamtbelastungen und Gesamtgutschriften waren **nicht** in der Transaktionswährung ausgeglichen, aber sie waren für die Buchhaltungswährung und die Berichtswährung ausgeglichen. Ein Debitor nahm an, dass der Beleg trotzdem gebucht werden würde. Diese Annahme war jedoch falsch. **Die Beträge in Transaktionswährung auf einem Beleg müssen immer ausgeglichen sein, wenn alle Zeilen des Belegs die gleiche Transaktionswährung haben.**
- Der Beleg wurde mit einer Datenentität über das Data Management Framework (DMF) importiert, und der Benutzer dachte, dass die Beträge in der Transaktionswährung ausgeglichen waren. In der Importdatei hatten einige Beträge mehr als zwei Dezimalstellen, und beim Importieren der Beträge wurden mehr als zwei Dezimalstellen einbezogen. Daher stimmten die Belastungen nicht mit den Gutschriften überein, da sie um den Bruchteil eines Pennys abwichen. Die Erfassung spiegelte diese Differenz in den Zeilen des Belegs nicht wider, da die angezeigten Beträge nur zwei Dezimalstellen haben.
- Der Beleg wurde mit einer Datenentität über DMF importiert, und der Benutzer dachte, dass die Beträge der Transaktionswährung ausgeglichen seien. Obwohl der **Beleg** ausgeglichen war, hatten einige Zeilen des Belegs unterschiedliche Transaktionsdaten. Wenn Sie die Gesamtsoll- und Gesamthabenbeträge in der Transaktionswährung pro **Beleg und Transaktionsdatum** addierten, waren sie nicht ausgeglichen. Diese Anforderung wird erzwungen, wenn Sie einen Beleg über das Allgemeine Buch.-Blatt im System erfassen. Es wird jedoch nicht erzwungen, wenn ein Beleg mit einer Datenentität über DMF importiert wird.

In einem unterstützten Szenario kann ein Beleg mehr als eine Transaktionswährung haben. In diesem Fall prüft das System **nicht**, ob die Belastungen gleich den Gutschriften in der Transaktionswährung sind, da die Währungen nicht übereinstimmen. Stattdessen prüft das System, dass die Beträge in der Buchungswährung und Berichtswährung ausgeglichen sind.

### <a name="accounting-currency"></a>Buchhaltungswährung

Wenn alle Zeilen eines Belegs die gleiche Transaktionswährung haben und die Beträge in der Transaktionswährung ausgeglichen sind, prüft das System, dass die Beträge in der Buchhaltungswährung ausgeglichen sind. Wenn der Beleg in einer Fremdwährung eingegeben wurde, wird der Wechselkurs in den Belegzeilen verwendet, um die Beträge in Transaktionswährung in die Buchhaltungswährung umzurechnen. Zunächst wird jede Zeile des Belegs umgerechnet und auf zwei Dezimalstellen gerundet. Dann werden die Zeilen summiert, um die Gesamtsoll- und Gesamtsollbeträge zu ermitteln. Da jede Zeile umgerechnet wird, kann es sein, dass die Gesamtsoll- und Gesamtsollbeträge nicht ausgeglichen sind. Wenn der absolute Wert der Differenz jedoch innerhalb des Wertes **Maximale Centdifferenz** liegt, der auf der Seite **Hauptbuchparameter** definiert ist, wird der Beleg gebucht, und die Differenz wird automatisch auf das Centdifferenz-Konto gebucht.

Wenn der Beleg mehr als eine Transaktionswährung hat, wird jede Zeile des Belegs in die Buchhaltungswährung umgerechnet und auf zwei Dezimalstellen gerundet, und dann werden die Zeilen summiert, um die Gesamtsoll- und Gesamthabenbeträge zu ermitteln. Um als ausgeglichen zu gelten, müssen die Belastungen und Gutschriften ausgeglichen sein, entweder in der Umrechnung oder unter Einbeziehung der Cent-Rundungsdifferenz der Buchhaltungswährung.

### <a name="reporting-currency"></a>Berichtswährung

Wenn alle Zeilen eines Beleges die gleiche Transaktionswährung haben und die Beträge in der Transaktionswährung ausgeglichen sind, prüft das System, ob die Beträge in der Berichtswährung ausgeglichen sind. Wenn der Beleg in einer Fremdwährung eingegeben wurde, wird der Exchange-Satz in den Belegzeilen verwendet, um die Beträge in Transaktionswährung in die Berichtswährung umzurechnen. Zunächst wird jede Zeile des Belegs umgerechnet und auf zwei Dezimalstellen gerundet. Dann werden die Zeilen summiert, um die Gesamtsoll- und Gesamtsollbeträge zu ermitteln. Da jede Zeile umgerechnet wird, kann es sein, dass die Gesamtsoll- und Gesamtsollbeträge nicht ausgeglichen sind. Wenn die Differenz jedoch innerhalb des Wertes **Maximale Pfennigrundung in der Berichtswährung** liegt, der auf der Seite **Hauptbuch-Parameter** definiert ist, wird der Beleg gebucht und die Differenz wird automatisch auf das Pfennig-Differenzkonto gebucht.

Wenn der Beleg mehr als eine Transaktionswährung hat, wird jede Zeile des Belegs in die Berichtswährung umgerechnet und auf zwei Dezimalstellen gerundet, und dann werden die Zeilen summiert, um die Gesamtsoll- und Gesamthabenbeträge zu ermitteln. Um als ausgeglichen zu gelten, müssen die Belastungen und Gutschriften ausgeglichen sein, entweder in der Umrechnung oder unter Einbeziehung der Cent-Rundungsdifferenz der Berichtswährung.

### <a name="example-for-an-accounting-currency-imbalance"></a>Beispiel für ein Ungleichgewicht in der Buchhaltungswährung

> [!NOTE]
> Der Berichtswährungsbetrag wird aus dem Transaktionswährungsbetrag auf die gleiche Weise wie der Buchhaltungswährungsbetrag berechnet.

Wechselkurs: 1,5

| Position | Beleg | Konto | Währung | Soll (Transaktion) | Haben (Transaktion) | Soll (Buchhaltung) | Haben (Buchhaltung) |
|---|---|---|---|---|---|---|---|
| 1 | 001 | 1101-01 | EUR | 3.33 | | 5,00 (4,995) | |
| 2 | 001 | 1101-02 | EUR | 3.33 | | 5,00 (4,995) | |
| 3 | 001 | 1101-03 | EUR | 3.34 | | 5.01 | |
| 4 | 001 | 4101- | EUR | | 10.00 | | 15.00 |
| **Summe** | | | | **10.00** | **10.00** | **15.01** | **15.00** |

Die Rechnungswährung ist um 0,01 aus dem Gleichgewicht. Solange die maximale Cent-Rundung in der Buchhaltungswährung jedoch mindestens 0,01 beträgt, wird die Differenz automatisch auf das Cent-Differenzkonto gebucht und der Beleg erfolgreich gebucht.
