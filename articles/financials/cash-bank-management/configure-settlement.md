---
title: Konfigurieren eines Ausgleichs
description: "Wie und wann Transaktionen ausgeglichen werden, können komplexe Themen sein; daher ist es wichtig, dass Sie den Vorgang verstehen und die Parameter für Ihre geschäftlichen Anforderungen korrekt definieren. Dieser Artikel beschreibt die Parameter, die für den Ausgleich für Kreditoren und Debitoren verwendet werden."
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, CustParameters, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14601
ms.assetid: 6b61e08c-aa8b-40c0-b904-9bca4e8096e7
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 059513de66827aa3a839b9eb06973ec4c1549f73
ms.contentlocale: de-de
ms.lasthandoff: 06/13/2017

---

# <a name="configure-settlement"></a>Konfigurieren eines Ausgleichs

[!include[banner](../includes/banner.md)]


Wie und wann Transaktionen ausgeglichen werden, können komplexe Themen sein; daher ist es wichtig, dass Sie den Vorgang verstehen und die Parameter für Ihre geschäftlichen Anforderungen korrekt definieren. Dieser Artikel beschreibt die Parameter, die für den Ausgleich für Kreditoren und Debitoren verwendet werden. 

Die folgenden Parameter haben Auswirkungen darauf, wie Ausgleiche in der Enterprise-Edition von Microsoft Dynamics 365 for Finance and Operations verarbeitet werden. Ausgleich ist der Prozess für das Begleichen einer Rechnung durch eine Zahlung oder eine Gutschrift. Diese Parameter werden befinden sich im **Ausgleich**-Bereich der **Debitorenparameter** **Kreditorenkontenparameter**-Seiten.

-   **Automatischer Ausgleich** – Legen Sie diese Option auf **Ja** fest, wenn eine Transaktion bei der Buchung automatisch mit anderen offenen Posten ausgeglichen werden soll. Ist die Option auf **Nein** festgelegt, können Benutzer Transaktionen manuell ausgleichen, wenn sie Zahlungen eingeben, oder später, indem die Seite **Buchungen ausgleichen** verwenden.
-   **Skontoverwaltung** – Geben Sie an wie ein [Skonto ausgeführt wird, wenn für eine Rechnung zu viel bezahlt wird](cash-discount-handling-overpayments.md) Bei einer Überzahlung kann das Skonto verringert werden, sie kann als Differenz behandelt werden oder sie kann beim Kreditoren oder Debitoren bleiben.
    -   **Lax**– Der Skontobetrag wird um den Betrag der Überzahlung verringert. Dieses Verhalten wird immer verwendet, unabhängig davon, ob der Überzahlungsbetrag möglicherweise größer oder kleiner ist als der Betrag, der im Feld **Maximale Über- bzw. Unterzahlung** eingegeben wird.
    -   **Genau** – Der Überzahlungsbetrag wird entweder zu einem Sachkonto für den Skontounterschied gebucht oder verbleibt als Kontensaldo auf dem Debitorenkonto. Das geneue Verhalten hängt davon ab, ob der Überzahlungsbetrag zwischen 0,00 und dem Betrag liegt, der im Feld **Maximale Über- bzw. Unterzahlung** eingegeben wurde, oder ob der Überzahlungsbetrag größer als der Betrag in **Maximale Über- bzw. Unterzahlung** ist.
-   **Maximale Centdifferenz** – Geben Sie die maximal zulässige Centdifferenz für die ausgeglichenen Transaktionen ein. Wenn die Differenz kleiner oder gleich der in diesem Feld festgelegten Differenz ist, wird sie auf das Sachkonto für die Centdifferenz gebucht, das auf der Seite **Konten für automatische Buchungen** angegeben ist.
-   **Maximale Über- bzw. Unterzahlung** – Geben Sie den Betrag ein, der für Über- und Unterzahlungen akzeptiert wird. Um die Steuer für Über- oder Unterzahlungen zu berechnen, klicken Sie auf der Seite **Hauptbuchparameter** auf **Mehrwertsteuer**, und wählen Sie dann die Option **Mehrwertsteuer auf Über- bzw. Unterzahlung** aus.
    -   Führt die Über- oder Unterzahlung zu einer Differenz, die kleiner ist als die im Feld **Maximale Centdifferenz** definierte Differenz, wird der Centdifferenzbetrag auf das Centdifferenzkonto gebucht.
    -   Wenn die Über- oder Unterzahlung eine Differenz führt, die größer ist als die im Feld **Maximale Centdifferenz** definierte Differenz, wird der Differenzbetrag auf das Differenzkonto gebucht, das für den Buchungstyp **Debitorenskonto** oder **Kreditorenskonto** auf der Seite **Konten für automatische Buchungen** ausgewählt ist.
-   **Skonti für Teilzahlungen berechnen** – Legen Sie diese Option auf **Ja** fest, um die automatische Berechnung von Skonti für Teilzahlungen zu aktivieren.
    -   Diese Auswirkungen auf diese Option hängen vom Wert des Felds **Skonto verwenden** auf der Seite **Buchungen ausgleichen** ab. Ist die Option auf **Ja** festgelegt, wird der Rabatt verwendet, wenn das Feld **Skonto verwenden** auf **Normal** festgelegt ist. Wenn das Feld **Skonto verwenden** auf **Immer** festgelegt ist, wird das Skonto immer verwendet, unabhängig von der Einstellung in diesem Feld. Wenn das Feld **Skonto verwenden** auf **Niemals** festgelegt ist, wird das Skonto nie verwendet, unabhängig von der Einstellung in diesem Feld.
    -   Wenn diese Option auf **Ja** festgelegt ist, und im Feld **Auszugleichender Betrag** auf der Seite **Buchungen ausgleichen** der Wert von einem Benutzer geändert wird, wird der Rabatt automatisch berechnet und als Standardeintrag im Feld **In Anspruch zu nehmender Skonto** angezeigt.
    -   Wenn diese Option auf **Nein** festgelegt und auf der Seite **Offene Buchungen ausgleichen** ein Benutzer den Wert im Feld **Auszugleichender Betrag** ändert, ist der Standardeintrag im Feld **In Anspruch zu nehmender Skonto** **0** (null).
-   **Skonti für Gutschriften berechnen** – Legen Sie diese Option auf **Ja** fest, um ein Skonto für Gutschriften automatisch zu berechnen. Bei Debitoren ist eine Gutschriftbuchung eine negative Transaktion, die im Feld **Rechnung** der Seite **Freitextrechnung** einen Wert besitzt, oder eine Rückgabe auf der Seite **Auftrag**.
    -   Die Auswirkungen auf diese Option hängen vom Wert des Felds **Skonto verwenden** auf der Seite **Buchungen ausgleichen** ab. Ist die Option auf **Ja** festgelegt, wird der Rabatt verwendet, wenn das Feld ****Skonto verwenden**** auf **Normal** festgelegt ist. Wenn das Feld ****Skonto verwenden**** auf **Immer** festgelegt ist, wird das Skonto immer verwendet, unabhängig von der Einstellung in diesem Feld. Wenn das Feld ****Skonto verwenden**** auf **Niemals** festgelegt ist, wird das Skonto nie verwendet, unabhängig von der Einstellung in diesem Feld.
    -   Wenn diese Option auf **Ja** festgelegt ist, und auf der Seite **Offene Buchungen ausgleichen** eine Gutschrift markiert ist, wird der Rabatt automatisch berechnet und als Standardeintrag im Feld **In Anspruch zu nehmender Skonto** angezeigt.
    -   Wenn diese Option auf **Nein** festgelegt ist und auf der Seite **Offene Buchungen ausgleichen** eine Gutschrift markiert wird, ist der Standardeintrag im Feld **In Anspruch zu nehmender Skonto** **0** (null).
-   **Rabattgegenkontos (nur Kreditor)** – Definieren Sie das standardmäßige Skontosachkonto, das für den Buchhaltungseintrag für Skonti verwendet werden soll.
    -   **Hauptkonto für Kreditorenrabatte verwenden** – Der Skonto wird auf das Hauptkonto gebucht, das auf der Seite **Skontoeinstellung** definiert ist.
    -   **Konten in den Rechnungspositionen** – Das Skonto wird auf die Sachkonten auf der ursprünglichen Rechnung gebucht.
-   **Positionen auf Freitextrechnungen und Zinsrechnungen markieren (nur Debitor)** – Legen Sie diese Option auf **Ja** fest, um die Schaltfläche **Rechnungspositionen markieren** auf den Seiten **Debitorenzahlungen eingeben**, **Zahlungserfassungsbeleg** und **Buchungen ausgleichen** zu aktivieren. Mit dieser Schaltfläche können Benutzer nun einzelne Positionen für den Ausgleich markieren.
-   **Ausgleich priorisieren (nur Debitor)** – Legen Sie diese Option auf **Ja** fest, um die Schaltfläche **Nach Priorität markieren** auf den Seiten **Debitorenzahlungen eingeben** und **Buchungen ausgleichen** zu aktivieren. Diese Schaltfläche können Benutzer den zuvor festgelegten Ausgleichsauftrag für die Buchungen zuweisen.  Nach Anwendung des Standardausgleichsauftrags auf eine Buchung mithilfe der Schaltfläche können die Auftrags- und Zahlungszuteilung vor der Buchung geändert werden.
-   **Verwendungspriorität für automatische Ausgleiche**– Legen Sie diese Option auf **Ja**, um die festgelegte Prioritätsreihenfolge zu verwenden, wenn Buchungen automatisch ausgeglichen werden. Dieses Feld ist nur verfügbar, wenn Sie den **Ausgleich priorisieren** und **Automatischer Ausgleich** auf **Ja** festlegen.




