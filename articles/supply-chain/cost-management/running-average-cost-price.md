---
title: Laufender Durchschnittseinstandspreis
description: "Durch den Lagerabschluss werden Abgangsbuchungen mit Zugangsbuchungen ausgeglichen. Grundlage hierfür bildet die Lagerbewertungsmethode, die in der Artikelmodellgruppe des Artikels ausgewählt ist. Vor Ausführung des Lagerabschlusses wird vom System jedoch ein laufender Durchschnittseinstandspreis berechnet, der in der Regel zum Ausführen von Abgangsbuchungen verwendet wird."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, Retail
ms.custom: 79003
ms.assetid: adc3f245-dc9d-4327-88fb-6a579194a5fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 875325bca949c0f3dfc0eab55f64db5659a2faef
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="running-average-cost-price"></a>Laufender Durchschnittseinstandspreis

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


Durch den Lagerabschluss werden Abgangsbuchungen mit Zugangsbuchungen ausgeglichen. Grundlage hierfür bildet die Lagerbewertungsmethode, die in der Artikelmodellgruppe des Artikels ausgewählt ist. Vor Ausführung des Lagerabschlusses wird vom System jedoch ein laufender Durchschnittseinstandspreis berechnet, der in der Regel zum Ausführen von Abgangsbuchungen verwendet wird.

Das System schätzt die laufenden Durchschnittseinstandspreises für einen Artikel mithilfe folgender Formel: 

Vorkalkulierter Preis = (physischer Betrag + wertmäßiger Betrag) / (physische Menge + wertmäßige Menge)

## <a name="using-the-running-average-cost-price"></a>Verwendung des laufenden Durchschnittseinstandspreises
Die folgende Tabelle gibt an, wann Lagerbuchungen vom System unter Verwendung des laufenden Durchschnittseinstandspreises ausgeführt werden und wann stattdessen der im Artikelmasterdatensatz definierte Einstandspreis verwendet wird:

| Bedingung                                               | Das System verwendet den vorkalkulierten laufenden Durchschnittseinstandspreis | Das System verwendet den Einstandspreis, der im Artikelmaster definiert ist |
|---------------------------------------------------------|----------------------------------------------------------|-------------------------------------------------------------------|
| Sowohl Zähler\* als auch Nenner\*\* sind positiv.  | Ja                                                      | Nr.                                                                |
| Zähler\* und/oder Nenner\*\* sind negativ. | Nr.                                                       | Ja                                                               |
| Der Nenner\*\* ist 0 (Null).                        | Nr.                                                       | Ja                                                               |

\* Zähler = (physischer Betrag + wertmäßiger Betrag) \*\* Nenner = (physischer Menge + wertmäßige Menge) 

**Hinweis** Ist die Option **Physischen Wert einschließen** für einen Artikel nicht aktiviert, wird vom System sowohl für den physischen Betrag als auch für die physische Menge der Wert 0 (Null) verwendet. Informationen zu dieser Option, finden Sie unter [Physischen Wert einbeziehen](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Preisverstärkung vermeiden
In seltenen Fällen versieht das System mehrere Abgänge mit einem Preis, bevor eine genügende Menge von Zugängen vorhanden ist, auf die der Preis gestützt werden kann. Dieses Szenario kann dazu führen, dass Vorkalkulationen des laufenden Durchschnittseinstandspreises , zu hoch werden. Diese Preisverstärkung lässt sich jedoch durch bestimmte Maßnahmen vermeiden oder zumindest abschwächen. **Szenario** Die folgenden Buchungen treten bei einem Artikel auf, für den Sie die Option **Physischen Wert einbeziehen** ausgewählt haben:

1.  Sie erhalten wertmäßig die Menge von 100 zu jeweils EUR 100,00.
2.  Sie geben wertmäßig eine Menge von 200 ab.
3.  Sie erhalten physikalisch eine Menge von 101 zu jeweils EUR 202,00.

Beim Betrachten des vorkalkulierten laufenden Durchschnittseinstandspreises für den Artikel haben Sie einen Einstandspreis von EUR 1,51 erwartet. Allerdings ergibt sich aus der folgenden Formel ein vorkalkulierter laufender Durchschnitt von EUR 102,00: Vorkalkulierter Preis = \[202 + (- 100)\] ÷ \[101 + (- 100)\] = 102 ÷ 1 = 102 Diese Preiskalkulationsverstärkung tritt auf, da das System beim wertmäßigen Abgang der 200 Artikel (Schritt 2) 100 Artikel mit einem Preis versehen muss, bevor die entsprechenden Zugänge zur Verfügung stehen. Diese Situation verursacht negativen Bestand. Wie zu erwarten war, wird von dem System daraufhin ein Preis pro Einheit von EUR 1,00 vorkalkuliert. Wenn der entsprechende Zugang von 100 Stück erfolgt, besitzen diese einen Einheitenpreis von EUR 2.00. 

**Hinweis:** Obwohl sich durch die Abgänge ein negativer Bestand ergibt, ist der Bestand zum Zeitpunkt der Abgangspreisberechnung positiv. Aus diesem Grund wird anstelle des Preises aus dem Artikelmaster der laufende Durchschnittseinstandspreis verwendet. An diesem Punkt liegt das System ein Lagerwertversatz von EUR 100.00 vor. Obwohl sich dieser Versatz für 100 Stück mit einem Versatz pro Einheit von EUR 1,00 kumuliert, enthält der Bestand jedoch nur noch ein Stück. Daher wird der Versatz von EUR 100,00 diesem einzelnen Stück zugeordnet. Daraus ergibt sich eine zu hohe Vorkalkulation des Einstandspreises. 

**Hinweis:** Wären die Schritte 2 und 3 des Szenarios vertauscht, würden 200 Artikel zu einem Einheitenpreis von EUR 1,51 ausgegeben, und ein Stück bliebe mit einem Einheitenpreis von EUR 1,51 übrig. Da diese Preisverstärkung auftreten kann, wenn negativer Bestand vorhanden ist, ist sie in den folgenden Fällen nur schwer vermeidbar:

-   Abgangspreise für Wert und Menge des verfügbaren Bestands müssen vorkalkuliert werden.
-   Sie müssen den Wert und die Menge der Ab- und Zugänge des verfügbaren Bestands regulieren.
-   Ihr Geschäftsmodell ermöglicht den Versand oder die Preisbildung für mehr Stücke als vorhanden sind.
-   Sie müssen alle an Sie übermittelten Zugangswerte und -mengen annehmen.

Sollten die folgenden Methoden im Rahmen des Geschäftsmodells zulässig sein, können sie dazu beitragen, negative Mengen zu vermeiden, die ansonsten eine Preisverstärkung begünstigen:

-   Wenn Sie die Option **Physischen Wert einbeziehen** für einen Artikel auswählen, müssen Sie das Kontrollkästchen **Physischer negativer Bestand** auf der Seite **Artikelmodellgruppen** deaktivieren.
-   Wenn Sie *nicht* die Option **Physischen Wert einbeziehen** für einen Artikel auswählen, müssen Sie das Kontrollkästchen **Wertmäßig negativer Bestand** auf der Seite **Artikelmodellgruppen** deaktivieren.

Bedenken Sie ausserdem, dass der maximale Versatz des physischen Lagerwerts durch die Anzahl der physischen Buchungen, sowie durch die Differenz zwischen physischen und wertmäßigen Preisen begrenzt wird. Vorausgesetzt, dass alle physischen Buchungen letzten Endes wertmäßig aktualisiert werden, kann der physische Wert keinen extrem hohen Wert erreichen. Beachten Sie, dass der Verstärkungseffekt sich deutlich abschwächt , wenn sich der kumulierte Versatz nicht auf einen verfügbaren Artikel beschränkt, sondern sich auf mehrere Artikel verteilt.




