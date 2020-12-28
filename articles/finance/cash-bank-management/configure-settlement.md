---
title: Konfigurieren eines Ausgleichs
description: Wie und wann Transaktionen ausgeglichen werden, können komplexe Themen sein; daher ist es wichtig, dass Sie den Vorgang verstehen und die Parameter für Ihre geschäftlichen Anforderungen korrekt definieren. Dieses Thema beschreibt die Parameter, die für den Ausgleich sowohl der Kreditorenkonten als auch der Debitoren verwendet werden.
author: kweekley
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, CustParameters, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14601
ms.assetid: 6b61e08c-aa8b-40c0-b904-9bca4e8096e7
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 094b8876b3b10b6dcbc0ce399a1a9915271459ed
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443714"
---
# <a name="configure-settlement"></a>Konfigurieren eines Ausgleichs

[!include [banner](../includes/banner.md)]

Wie und wann Transaktionen ausgeglichen werden, können komplexe Themen sein; daher ist es wichtig, dass Sie den Vorgang verstehen und die Parameter für Ihre geschäftlichen Anforderungen korrekt definieren. Dieses Thema beschreibt die Parameter, die für den Ausgleich sowohl der Kreditorenkonten als auch der Debitoren verwendet werden. 

Die folgenden Parameter haben Auswirkungen darauf, wie Ausgleiche in Microsoft Dynamics 365 Finance verarbeitet werden. Ausgleich ist der Prozess für das Begleichen einer Rechnung durch eine Zahlung oder eine Gutschrift. Diese Parameter werden befinden sich im **Ausgleich**-Bereich der **Debitorenparameter** **Kreditorenkontenparameter**-Seiten.

- **Automatischer Ausgleich** – Legen Sie diese Option auf **Ja** fest, wenn eine Transaktion bei der Buchung automatisch mit anderen offenen Posten ausgeglichen werden soll. Ist die Option auf **Nein** festgelegt, können Benutzer Transaktionen manuell ausgleichen, wenn sie Zahlungen eingeben, oder später, indem die Seite **Buchungen ausgleichen** verwenden.
- **Skontoverwaltung** – Geben Sie an wie ein [Skonto ausgeführt wird, wenn für eine Rechnung zu viel bezahlt wird](cash-discount-handling-overpayments.md) Bei einer Überzahlung kann das Skonto verringert werden, sie kann als Differenz behandelt werden oder sie kann beim Kreditoren oder Debitoren bleiben.
  -   **Lax**– Der Skontobetrag wird um den Betrag der Überzahlung verringert. Dieses Verhalten wird immer verwendet, unabhängig davon, ob der Überzahlungsbetrag möglicherweise größer oder kleiner ist als der Betrag, der im Feld **Maximale Über- bzw. Unterzahlung** eingegeben wird.
  -   **Genau** – Der Überzahlungsbetrag wird entweder zu einem Sachkonto für den Skontounterschied gebucht oder verbleibt als Kontensaldo auf dem Debitorenkonto. Das geneue Verhalten hängt davon ab, ob der Überzahlungsbetrag zwischen 0,00 und dem Betrag liegt, der im Feld **Maximale Über- bzw. Unterzahlung** eingegeben wurde, oder ob der Überzahlungsbetrag größer als der Betrag in **Maximale Über- bzw. Unterzahlung** ist.
- **Maximale Centdifferenz** – Geben Sie die maximal zulässige Centdifferenz für die ausgeglichenen Transaktionen ein. Wenn die Differenz kleiner oder gleich der in diesem Feld festgelegten Differenz ist, wird sie auf das Sachkonto für die Centdifferenz gebucht, das auf der Seite **Konten für automatische Buchungen** angegeben ist.
- **Maximale Über- bzw. Unterzahlung** – Geben Sie den Betrag ein, der für Über- und Unterzahlungen akzeptiert wird. Um die Steuer für Über- oder Unterzahlungen zu berechnen, klicken Sie auf der Seite **Hauptbuchparameter** auf **Mehrwertsteuer**, und wählen Sie dann die Option **Mehrwertsteuer auf Über- bzw. Unterzahlung** aus.
  -   Führt die Über- oder Unterzahlung zu einer Differenz, die kleiner ist als die im Feld **Maximale Centdifferenz** definierte Differenz, wird der Centdifferenzbetrag auf das Centdifferenzkonto gebucht.
  -   Wenn die Über- oder Unterzahlung eine Differenz führt, die größer ist als die im Feld **Maximale Centdifferenz** definierte Differenz, wird der Differenzbetrag auf das Differenzkonto gebucht, das für den Buchungstyp **Debitorenskonto** oder **Kreditorenskonto** auf der Seite **Konten für automatische Buchungen** ausgewählt ist.
- **Skonti für Teilzahlungen berechnen** – Legen Sie diese Option auf **Ja** fest, um die automatische Berechnung von Skonti für Teilzahlungen zu aktivieren.
  -   Die Auswirkungen auf diese Option hängen vom Wert des Felds **Skonto verwenden** auf der Seite **Buchungen ausgleichen** ab. Ist die Option auf **Ja** festgelegt, wird der Rabatt verwendet, wenn das Feld **Skonto verwenden** auf **Normal** festgelegt ist. Wenn das Feld **Skonto verwenden** auf **Immer** festgelegt ist, wird das Skonto immer verwendet, unabhängig von der Einstellung in diesem Feld. Wenn das Feld **Skonto verwenden** auf **Niemals** festgelegt ist, wird das Skonto nie verwendet, unabhängig von der Einstellung in diesem Feld.
  -   Wenn diese Option auf **Ja** festgelegt ist, und im Feld **Auszugleichender Betrag** auf der Seite **Buchungen ausgleichen** der Wert von einem Benutzer geändert wird, wird der Rabatt automatisch berechnet und als Standardeintrag im Feld **In Anspruch zu nehmender Skonto** angezeigt.
  -   Wenn diese Option auf **Nein** festgelegt und auf der Seite **Offene Buchungen ausgleichen** ein Benutzer den Wert im Feld **Auszugleichender Betrag** ändert, ist der Standardeintrag im Feld **In Anspruch zu nehmender Skonto** **0** (null).
- **Skonti für Gutschriften berechnen** – Legen Sie diese Option auf **Ja** fest, um ein Skonto für Gutschriften automatisch zu berechnen. Bei Debitoren ist eine Gutschriftbuchung eine negative Transaktion, die im Feld **Rechnung** der Seite **Freitextrechnung** einen Wert besitzt, oder eine Rückgabe auf der Seite **Auftrag**.
  - Die Auswirkungen auf diese Option hängen vom Wert des Felds <strong>Skonto verwenden</strong> auf der Seite <strong>Buchungen ausgleichen</strong> ab. Ist die Option auf <strong>Ja</strong> festgelegt, wird der Rabatt verwendet, wenn das Feld *<strong><em>Skonto verwenden</em></strong>* auf <strong>Normal</strong> festgelegt ist. Wenn das Feld *<strong><em>Skonto verwenden</em></strong>* auf <strong>Immer</strong> festgelegt ist, wird das Skonto immer verwendet, unabhängig von der Einstellung in diesem Feld. Wenn das Feld *<strong><em>Skonto verwenden</em></strong>* auf <strong>Niemals</strong> festgelegt ist, wird das Skonto nie verwendet, unabhängig von der Einstellung in diesem Feld.
  - Wenn diese Option auf **Ja** festgelegt ist, und auf der Seite **Offene Buchungen ausgleichen** eine Gutschrift markiert ist, wird der Rabatt automatisch berechnet und als Standardeintrag im Feld **In Anspruch zu nehmender Skonto** angezeigt.
  - Wenn diese Option auf **Nein** festgelegt ist und auf der Seite **Offene Buchungen ausgleichen** eine Gutschrift markiert wird, ist der Standardeintrag im Feld **In Anspruch zu nehmender Skonto** **0** (null).

- **Rabattgegenkontos (nur Kreditor)** – Definieren Sie das standardmäßige Skontosachkonto, das für den Buchhaltungseintrag für Skonti verwendet werden soll.
  -   **Hauptkonto für Kreditorenrabatte verwenden** – Der Skonto wird auf das Hauptkonto gebucht, das auf der Seite **Skontoeinstellung** definiert ist.
  -   **Konten in den Rechnungspositionen** – Das Skonto wird auf die Sachkonten auf der ursprünglichen Rechnung gebucht.
- **Positionen auf Freitextrechnungen und Zinsrechnungen markieren (nur Debitor)** – Legen Sie diese Option auf **Ja** fest, um die Schaltfläche **Rechnungspositionen markieren** auf den Seiten **Debitorenzahlungen eingeben**, **Zahlungserfassungsbeleg** und **Buchungen ausgleichen** zu aktivieren. Mit dieser Schaltfläche können Benutzer nun einzelne Positionen für den Ausgleich markieren.
- **Ausgleich priorisieren (nur Debitor)** – Legen Sie diese Option auf **Ja** fest, um die Schaltfläche **Nach Priorität markieren** auf den Seiten **Debitorenzahlungen eingeben** und **Buchungen ausgleichen** zu aktivieren. Diese Schaltfläche können Benutzer den zuvor festgelegten Ausgleichsauftrag für die Buchungen zuweisen.  Nach Anwendung des Standardausgleichsauftrags auf eine Buchung mithilfe der Schaltfläche können die Auftrags- und Zahlungszuteilung vor der Buchung geändert werden.
- **Verwendungspriorität für automatische Ausgleiche**– Legen Sie diese Option auf **Ja**, um die festgelegte Prioritätsreihenfolge zu verwenden, wenn Buchungen automatisch ausgeglichen werden. Dieses Feld ist nur verfügbar, wenn Sie den **Ausgleich priorisieren** und **Automatischer Ausgleich** auf **Ja** festlegen.

## <a name="fixed-dimensions-on-accounts-receivableaccounts-payable-main-accounts"></a>Feste Dimensionen auf Debitoren-/Kreditorenhauptkonten

Wenn auf dem Debitoren-/Kreditorenhauptkonto feste Dimensionen verwendet werden, werden durch den Ausgleichsprozess zusätzliche Buchhaltungseinträge und zwei zusätzliche Kreditorenbuchungen gebucht. Der Ausgleich vergleicht das Debitoren-/Kreditorensachkonto der Rechnung und Zahlung.  Wenn die Zahlung und der Ausgleich gemeinsam abgeschlossen werden, was das typische Szenario ist, wird der Buchhaltungseintrag der Zahlung erst nach Abschluss des Ausgleichsprozesses in das Hauptbuch gebucht. Aufgrund der Reihenfolge der Verarbeitungsereignisse kann die Abrechnung das tatsächliche Debitoren-/Kreditorensachkonto nicht aus dem Buchhaltungseintrag der Zahlung ermitteln. Der Ausgleich rekonstruiert das Sachkonto für die Zahlung. Dies wird zum Problem, wenn eine feste Dimension für das Debitoren-/Kreditorenhauptkonto verwendet wird.

Zur Rekonstruktion des Sachkontos wird das Debitoren-/Kreditorenhauptkonto aus dem Buchungsprofil und die Finanzdimensionen aus dem Kreditorenbuchungsssatz für die Zahlung, wie in der Zahlungserfassung definiert, abgerufen. Feste Dimensionen werden nicht auf Zahlungserfassungen übernommen, sondern als letzter Schritt des Buchungsprozesses auf das Hauptkonto angewendet. Daher ist der feste Dimensionswert nicht in der Kreditorenbuchung enthalten, es sei denn, er wurde von einer anderen Quelle, z.B. dem Kreditor, bestimmt. Das rekonstruierte Konto enthält nicht die feste Dimension. Beim der Ausgleichsprozess wird festgestellt, daß eine Regulierungseingabe erstellt werden muß, da die Rechnung mit dem festen Dimensionswert aber nicht dem rekonstruierten Zahlungskonto gebucht wurde.  Da der Ausgleich mit der Buchung der Regulierungseingabe fortgeführt wird, ist der letzte Schritt der Buchung die Anwendung der festen Dimension. Durch Hinzufügen der festen Dimension zur Regulierungseingabe wird diese mit Soll und Haben auf das gleiche Sachkonto gebucht. Der Ausgleich kann den Buchhaltungseintrag nicht zurücknehmen.

Um zusätzliche Buchhaltungseinträge, Soll und Haben in dem selben Sachkonto zu vermeiden, sollten je nach Ihren Unternehmensanforderungen die folgenden Problemumgehungen berücksichtigt werden. 

-   Organisationen verwenden oft feste Dimensionen, um eine Finanzdimension, die nicht benötigt wird, mit Null zu füllen. Dies ist in der Regel der Fall bei Bilanzkonten, wie z.B. Debitoren/Kreditorenkonten. Kontostrukturen können verwendet werden, um Finanzdimension nicht zu verfolgen, die typischerweise mit Null gefüllt sind.  Sie können die Finanzdimensionen für die Bilanzkonten entfernen, so dass Sie keine festen Dimensionen verwenden müssen.
-   Wenn Ihr Unternehmen auf dem Debitoren-/Kreditorenhauptkonto feste Dimensionen benötigt, finden Sie eine Möglichkeit, die feste Dimension auf die Zahlung vorzuschlagen, so dass der Wert der festen Dimension auf der Kreditorenbuchung für die Zahlung gespeichert wird. Dadurch kann das System das Debitoren-/Kreditorenhauptkonto unter Berücksichtigung der festen Dimensionswerte rekonstruieren. Der Wert der festen Dimension kann entweder als Standard für den Kreditor oder den Erfassungsnamen für die Zahlungserfassung definiert werden.
