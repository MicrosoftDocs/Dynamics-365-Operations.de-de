---
title: Laufender Durchschnittseinstandspreis
description: Durch den Lagerabschluss werden Abgangsbuchungen mit Zugangsbuchungen ausgeglichen. Grundlage hierfür bildet die Lagerbewertungsmethode, die in der Artikelmodellgruppe des Artikels ausgewählt ist. Vor Ausführung des Lagerabschlusses wird vom System jedoch ein laufender Durchschnittseinstandspreis berechnet, der in der Regel zum Ausführen von Abgangsbuchungen verwendet wird.
author: JennySong-SH
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79003
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d324324312ce9e47b07de8e3de952b8d7c53647
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672177"
---
# <a name="running-average-cost-price"></a>Laufender Durchschnittseinstandspreis

[!include [banner](../includes/banner.md)]

Durch den Lagerabschluss werden Abgangsbuchungen mit Zugangsbuchungen ausgeglichen. Grundlage hierfür bildet die Lagerbewertungsmethode, die in der Artikelmodellgruppe des Artikels ausgewählt ist. Vor Ausführung des Lagerabschlusses wird vom System jedoch ein laufender Durchschnittseinstandspreis berechnet, der in der Regel zum Ausführen von Abgangsbuchungen verwendet wird.

Das System schätzt die laufenden Durchschnittseinstandspreises für einen Artikel mithilfe folgender Formel:

Vorkalkulierter Preis = (physischer Betrag + wertmäßiger Betrag) / (physische Menge + wertmäßige Menge)

## <a name="default-item-cost"></a>Standard-Artikel Kalkulation

Die standardmäßigen Produktkosten für einen zugelassenen Artikel können auf eine von zwei Arten auf der Seite **Details zum zugelassenen Artikel** konfiguriert werden:

- Erstellen Sie eine Standardkalkulation, indem Sie **Preis des Artikels** in der Gruppe **Einrichten** auf der Registerkarte **Kosten verwalten** des Aktionsbereichs auswählen. Wenn Sie diese Methode verwenden, müssen Sie eine Standardkalkulationsversion verwenden und die Kosten müssen aktiviert sein.
- Definieren Sie einen Standardeinkaufspreis für einen zugelassenen Artikel, indem Sie einen Wert in das Feld **Preis** auf der Registerkarte **Kosten verwalten** eingeben.

Zusätzlich zur Eingabe oder Erstellung eines Preises können Sie das Kontrollkästchen **Neuesten Einstandspreis verwenden** auf dem Inforegister **Kosten verwalten** der Seite **Freigegebene Produktdetails** aktivieren. In diesem Fall aktualisiert das System automatisch das Feld **Preis**, wenn Sie eine Finanzaktualisierung buchen. Wenn Sie zum Beispiel eine Einkaufsrechnung buchen, wird das Feld auf den Kaufpreis dieser Rechnung festgelegt.

Wenn Sie einen Selbstkostenpreis in einer aktiven Kalkulationsversion haben und einen Preis auf dem Inforegister **Kosten verwalten** eingeben, verwendet das System den Preis aus der aktiven Kalkulationsversion, bevor es den Preis verwendet, der auf dem Inforegister **Kosten verwalten** definiert ist.

## <a name="using-the-running-average-cost-price"></a>Verwendung des laufenden Durchschnittseinstandspreises

Die folgende Tabelle gibt an, wann Lagerbuchungen vom System unter Verwendung des laufenden Durchschnittseinstandspreises ausgeführt werden und wann stattdessen der im Artikelmasterdatensatz definierte Einstandspreis verwendet wird:

| Bedingung | Das System verwendet den vorkalkulierten laufenden Durchschnittseinstandspreis | Das System verwendet den Standardeinkaufspreis für Artikel |
| --- | --- | --- |
| Sowohl Zähler\* als auch Nenner\*\* sind positiv. | Ja | Nein |
| Zähler\* und/oder Nenner\*\* sind negativ. | Nein | Ja |
| Der Nenner\*\* ist 0 (Null). | Nein | Ja |

\* Zähler = (physischer Betrag + finanzieller Betrag)  
\*\* Nenner = (Physische Menge + Finanzielle Menge)

> [!NOTE]
> Wenn die Option **Physikalischen Wert einbeziehen** für einen Artikel nicht markiert ist, verwendet das System 0 (Null) sowohl für den physischen Betrag als auch für die physische Menge. Informationen zu dieser Option, finden Sie unter [Physischen Wert einbeziehen](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Preisverstärkung vermeiden

In seltenen Fällen versieht das System mehrere Abgänge mit einem Preis, bevor eine genügende Menge von Zugängen vorhanden ist, auf die der Preis gestützt werden kann. Dieses Szenario kann dazu führen, dass Vorkalkulationen des laufenden Durchschnittseinstandspreises , zu hoch werden. Diese Preisverstärkung lässt sich jedoch durch bestimmte Maßnahmen vermeiden oder zumindest abschwächen.

**Szenario:** Die folgenden Transaktionen treten für einen Artikel auf, für den Sie die Option **Physikalischen Wert einbeziehen** gewählt haben:

1. Sie erhalten wertmäßig die Menge von 100 zu jeweils EUR 100,00.
2. Sie geben wertmäßig eine Menge von 200 ab.
3. Sie erhalten physikalisch eine Menge von 101 zu jeweils EUR 202,00.

Beim Betrachten des vorkalkulierten laufenden Durchschnittseinstandspreises für den Artikel haben Sie einen Einstandspreis von EUR 1,51 erwartet. Stattdessen finden Sie einen geschätzten laufenden Durchschnitt von USD 102,00, der auf der folgenden Formel basiert:

Geschätzter Preis = \[202 + (-100) \] ÷ \[101 + (-100) \] = 102 ÷ 1 = 102

Diese Preiserhöhung tritt auf, weil das System bei 200 Artikeln, die in Schritt 2 finanziell ausgegeben werden, 100 der Artikel bepreisen muss, bevor es entsprechende Eingänge hat. Diese Situation verursacht negativen Bestand. Das System schätzt dann einen Preis pro Einheit von USD 1,00, wie Sie es erwarten können. Wenn der entsprechende Zugang von 100 Stück erfolgt, besitzen diese einen Einheitenpreis von EUR 2.00.

> [!NOTE]
> Obwohl die Ausgaben einen negativen Bestand erstellen, ist der Bestand positiv, wenn der Ausgabepreis berechnet wird. Aus diesem Grund wird anstelle des Preises aus dem Artikelmaster der laufende Durchschnittseinstandspreis verwendet. An diesem Punkt liegt das System ein Lagerwertversatz von EUR 100.00 vor. Obwohl dieser Ausgleich über 100 Stück aufgebaut wurde, bei denen eine Einheit von 1,00 USD pro Stück vorhanden war, haben Sie jetzt nur noch ein Stück im Bestand. Daher wird der Versatz von EUR 100,00 diesem einzelnen Stück zugeordnet. Daraus ergibt sich eine zu hohe Vorkalkulation des Einstandspreises.
>
> Beachten Sie zum Vergleich, dass, wenn die Schritte 2 und 3 im Szenario umgekehrt werden, 200 Artikel zu einem Einheitspreis von USD 1,51 ausgegeben werden und ein Artikel bei einem Einheitspreis von USD 1,51 bleibt. Da diese Preisverstärkung auftreten kann, wenn negativer Bestand vorhanden ist, ist sie in den folgenden Fällen nur schwer vermeidbar:
>
> - Abgangspreise für Wert und Menge des verfügbaren Bestands müssen vorkalkuliert werden.
> - Sie müssen den Wert und die Menge der Ab- und Zugänge des verfügbaren Bestands regulieren.
> - Ihr Geschäftsmodell ermöglicht den Versand oder die Preisbildung für mehr Stücke als vorhanden sind.
> - Sie müssen alle an Sie übermittelten Zugangswerte und -mengen annehmen.

Sollten die folgenden Methoden im Rahmen des Geschäftsmodells zulässig sein, können sie dazu beitragen, negative Mengen zu vermeiden, die ansonsten eine Preisverstärkung begünstigen:

- Wenn Sie die Option **Physikalischen Wert einbeziehen** für einen Artikel wählen, deaktivieren Sie das Kontrollkästchen **Physikalischer negativer Bestand** auf der Seite **Artikelmodellgruppen**.
- Wenn Sie **nicht** die Option **Physischen Wert einbeziehen** für einen Artikel auswählen, müssen Sie das Kontrollkästchen **Wertmäßig negativer Bestand** auf der Seite **Artikelmodellgruppen** deaktivieren.

Bedenken Sie ausserdem, dass der maximale Versatz des physischen Lagerwerts durch die Anzahl der physischen Buchungen, sowie durch die Differenz zwischen physischen und wertmäßigen Preisen begrenzt wird. Vorausgesetzt, dass alle physischen Buchungen letzten Endes wertmäßig aktualisiert werden, kann der physische Wert keinen extrem hohen Wert erreichen. Beachten Sie, dass der Verstärkungseffekt sich deutlich abschwächt , wenn sich der kumulierte Versatz nicht auf einen verfügbaren Artikel beschränkt, sondern sich auf mehrere Artikel verteilt.

## <a name="avoid-a-zero-cost-price-on-issues"></a>Vermeiden Sie eine Kalkulation zum Nulltarif bei Ausgaben

Wenn die Option **Physikalischen Wert einbeziehen** auf der Seite **Artikelmodellgruppe** nicht aktiviert ist, kann eine Ausgabe aus dem Bestand einen Selbstkostenpreis von Null haben, wenn keine finanziell aktualisierten Eingänge im Bestand vorhanden sind. Um dieses Szenario zu vermeiden, sollten Sie die folgenden Optionen in Betracht ziehen:

- Wählen Sie die Option **Physikalischen Wert einbeziehen** auf der Seite **Artikelmodellgruppe**. Diese Option verhindert eine Kalkulation zum Nulltarif für eine Ausgabe, vorausgesetzt, der Bon wird physisch aktualisiert. Wenn Sie keinen negativen physischen Bestand zulassen, berechnet Issues den laufenden Durchschnitt aus den physisch aktualisierten Transaktionen.
- Erstellen Sie einen Standardeinkaufspreis für einen Artikel, indem Sie eine Kalkulationsversion mit Standardkosten aktivieren, oder geben Sie den Preis auf dem Inforegister **Kosten verwalten** der Seite **Zugelassene Artikel** ein. Diese Option ist am besten geeignet, wenn die Option **Physikalischen Wert einbeziehen** auf der Seite **Artikelmodellgruppe** nicht ausgewählt ist, da das System dann immer einen Ausweichpreis verwenden kann.
- Markieren Sie die Option **Neuesten Einstandspreis verwenden** auf dem Inforegister **Kosten verwalten** der Seite **Details zu freigegebenen Produkten**. Diese Option hält das Feld **Preis** jedes Mal auf dem neuesten Stand, wenn Sie einen Bon finanziell aktualisieren. Wenn Sie diese Option wählen, aber keinen Standardpreis eingeben oder eine Kalkulation in einer Standardkalkulationsversion aktivieren, können Sie trotzdem einen Nullwert für eine Ausgabe haben.

Wenn Sie Ausgabetransaktionen haben, deren Kosten gleich Null sind, korrigiert der Prozess *Bestandsabschluss und -anpassung* den Selbstkostenpreis, indem er eine Anpassung erstellt, nachdem die Bestände finanziell aktualisiert wurden. Denken Sie daran, dass der Finanzzeitraum, in dem diese Aktualisierung stattfindet, von dem Finanzzeitraum abweichen kann, in dem die Artikel physisch eingegangen oder ausgegeben wurden.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
