---
title: Skonti
description: "Skonti werden für Kreditoren und Debitoren eingerichtet und freigegeben.  Das verfügbare Skonto kann auf der Debitorenrechnung oder der Kreditorenrechnung definiert werden und wird übernommen, wenn die Rechnung innerhalb des Skontodatums bezahlt wird."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: c105abdcd851b33a67ef2814c92c9839adb35b0a
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="cash-discounts"></a>Skonti

[!include[banner](../includes/banner.md)]


Skonti werden für Kreditoren und Debitoren eingerichtet und freigegeben.  Das verfügbare Skonto kann auf der Debitorenrechnung oder der Kreditorenrechnung definiert werden und wird übernommen, wenn die Rechnung innerhalb des Skontodatums bezahlt wird. 

<a name="cash-discounts"></a>Skonti
--------------

Skonti für Debitoren oder Kreditoren können auf der Skontoseite erstellt werden. Mithilfe des Felds "Nächster Skontocode" können Sie zudem eine Reihe von aufeinander folgenden Skonti definieren, die aufeinander folgen. Weitere Informationen finden Sie weiter unten in diesem Thema unter "Beispiel: Reihe von aufeinander folgenden Skonti". Wenn die Rechnung, die Habenbuchung (entweder Zahlung oder Gutschrift) oder beide nicht in einer Buchungswährung der juristischen Person eingegeben werden, wird das Skonto basierend auf dem Wechselkurs für Skonti für das Datum der Zahlung oder der Gutschrift berechnet. Wenn die Rechnung und das Habendokument in verschiedenen juristischen Personen erfasst werden und die Buchhaltungswährungen der juristischen Personen unterschiedlich sind, wird der Wechselkurs der juristischen Person der Rechnung verwendet, der am Datum des Habendokuments gültig ist. Weitere Informationen finden Sie weiter unten in diesem Thema unter "Beispiel: Wechselkurse für Skonti".
Standardreihenfolge des Skonto-Hauptkontos
----------------------------------------------

Wird eine Rechnung so frühzeitig beglichen, dass ein Skonto gewährt wird, so wird das Skonto automatisch auf ein Hauptkonto gebucht. Hierbei gilt folgende Standardpriorität:
1.  Das Hauptkonto, das im alternativen Feld "Alternatives Skontokonto" auf der Seite "Offene Buchungen ausgleichen" oder auf der Seite "Offene Buchungen ausgleichen" des Kreditors angegeben ist.
2.  Das Hauptkonto, das im Feld "Debitorenskonto" oder im Feld "Kreditorenskonto" der Sachkontobuchungsgruppe angegeben ist, die dem Mehrwertsteuercode der Rechnung zugeordnet ist. Richten Sie Sachkontobuchungsgruppen auf der Sachkontobuchungsgruppenseite ein und weisen Sie sie zu Mehrwertsteuercodes in der Mehrwertsteuercodeseite zu.
3.  Das Hauptbuchungskonto, das auf der Seite "Skonti" entweder im Feld "Hauptkonto für Debitorenrabatte" oder im Feld "Hauptkonto für Kreditorenrabatte" für den Skontocode auf der ausgeglichenen Rechnung angegeben ist.
4.  Das Hauptkonto für Skonti, wie in auf der Seite "Konten für automatische Buchungen" angegeben.

## <a name="example-series-of-cash-discounts"></a> Beispiel: Reihe von aufeinander folgenden Skonti
Richten Sie wie nachstehend gezeigt drei Skontocodes ein:
-   Code 5D10% – Skonto von 10 %, wenn der Betrag innerhalb von 5 Tagen beglichen wird.
-   Code 10D5% – Skonto von 5 %, wenn der Betrag innerhalb von 10 Tagen beglichen wird.
-   Code 14D2% – Skonto von 2 %, wenn der Betrag innerhalb von 14 Tagen beglichen wird.

Wählen Sie im Feld "Nächster Skontocode":
-   Wählen Sie 10D5% für den Code 5D10%.
-   Wählen Sie 14D2% für den Code 10D5%.
-   Lassen Sie für den Code "14D2%" das Feld "Nächster Skontocode" leer.

Diese drei Skonti folgen aufeinander da das Zahlungsdatum nach dem vorherigen Skontodatum der Rechnung liegt. Nur ein Skonto wird gewährt, wenn die Rechnung bezahlt wird. Dies basiert darauf, welches Skontodatum in der Folge von Skontos gilt.

## <a name="example-exchange-rates-for-cash-discounts"></a> Beispiel: Wechselkurse für Skonti
Die Buchhaltungswährung der juristischen Person ist EUR, und für US-Dollar sind folgende Wechselkurse angegeben:
-   1. Februar = 110
-   1. März = 80

Eine Rechnung in Höhe von 1.000 US-Dollar mit den Skontobedingungen von 20D2% wird am 15. Februar gebucht. Der Rechnungsbetrag in der Buchhaltungswährung beträgt 1.100 EUR. Eine Zahlung in Höhe von 980 US-Dollar wird mit der Rechnung vom 1. März ausgeglichen. Der Skontobetrag ist 20 US-Dollar. Der Zahlungsbetrag in der Buchhaltungswährung ist 784 EUR. Der Buchhaltungswährungsbetrag des Skontos wird mit dem Wechselkurs am 1. März berechnet: 20 \* 80 / 100 = 16 EUR.
| **Hinweis**                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Wenn die Option "Skonti für Teilzahlungen berechnen" auf der Debitorenparameter- oder Kreditorenparameterseite aktiviert ist, wird der Wechselkurs, der am Tag der jeweiligen Teilzahlung gültig ist, verwendet. |

 
=

 




