---
title: Autokalkulation einrichten
description: Dieses Thema beschreibt, wie Sie Kalkulationsregeln für verschiedene eingehende Fahrten festlegen können. Basierend auf diesen Regeln kalkuliert das System die Kosten und fügt sie automatisch hinzu. Daher müssen die Benutzer die Kalkulationen nicht manuell hinzufügen.
author: sherry-zheng
ms.date: 01/21/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMCostAutoSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-21
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 2e9135019323db74a4dca9343d315cbbf9683e32
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841958"
---
# <a name="auto-costs-setup"></a>Autokalkulation einrichten

[!include [banner](../../includes/banner.md)]

Sie können die Seite **Autokalkulation** verwenden, um Kostenregeln für verschiedene Kostenbereiche (wie Fahrten, Transportcontainer, Paletten, Kaufsbestellungen, Artikel oder Umlagerungsaufträge) festzulegen. Basierend auf den Regeln und den Feldern, die Benutzer auswählen, wenn sie Datensätze für einen der Kostenbereiche erstellen, berechnet das System die Kosten und fügt sie automatisch hinzu. Daher müssen die Benutzer die Kalkulationen nicht manuell hinzufügen.

Um mit Autokalkulationen zu arbeiten, gehen Sie zu **Gesamttransportkosten \> Kalkulation einrichten \> Autokalkulation**. Legen Sie dann die Regeln für die Autokalkulation fest, wie im weiteren Verlauf dieses Themas beschrieben.

## <a name="work-with-cost-areas"></a>Arbeiten mit Kalkulationen

Autokalkulationen funktionieren wie Handelsvereinbarungen oder Auto-Sonstige Kosten. Jeder Autokalkulationssatz gehört zu einer bestimmten Kalkulationsebene. Verwenden Sie das Feld **Kostenbereich** im Listenbereich der Seite **Autokalkulation**, um den Kostenbereich auszuwählen, mit dem Sie arbeiten möchten. Im Listenbereich werden nur Autokalkulationen angezeigt, die zu dem aktuell ausgewählten Kostenbereich gehören. Alle Autokalkulationen, die Sie erstellen, gehören zu dem aktuell ausgewählten Kostenbereich.

Kostenbereiche ermöglichen es dem System, die Kosten auf die Zeilen der Einkaufsbestellung in einem Kostenbereich aufzuteilen. Zum Beispiel wird eine Kalkulation für einen Transportcontainer den Wert auf alle Produkte in diesem Transportcontainer umlegen. Wenn es zwei oder mehr Transportcontainer gibt, kann für jeden Transportcontainer die gleiche Kalkulation angegeben werden. Daher kann der Containertyp verwendet werden, um die richtige Autokalkulation zu finden.

## <a name="buttons-on-the-action-pane"></a>Schaltflächen im Aktivitätsbereich

Die folgende Tabelle beschreibt die Schaltflächen, die im Aktivitätsbereich der Seite **Autokalkulation** verfügbar sind.

| Schaltfläche | Beschreibung |
|---|---|
| Bearbeiten | Eine bestehende Autokalkulation bearbeiten. |
| Neue | Eine Autokalkulation erstellen. |
| Löschen | Eine Autokalkulation löschen. |
| Kopieren von | Einen neuen Datensatz für eine Autokalkulation erstellen, der auf einem bestehenden Datensatz basiert. Sie können den neuen Datensatz dann frei bearbeiten. Mit dieser Schaltfläche können Sie schnell neue Autokalkulationen erstellen. |
| Dimensionen anzeigen | Öffnet ein Dialogfeld, in dem Sie die Bestandsdimensionen auswählen können, die für die von Ihnen angezeigten Transaktionen der Kalkulationen angezeigt werden. Wenn Sie Kontrollkästchen deaktivieren, werden weniger Bestandsdimensionen für die Transaktionen der Kalkulation angezeigt. Daher werden auch weniger Details für die Transaktion angezeigt. Wenn eine Bestandsdimension für eine Autokalkulation angegeben ist, wird die Autokalkulation nur angewendet, wenn die angegebene Bestandsdimension für den Artikel auf einer Fahrt verwendet wird. |

## <a name="settings-on-the-header"></a>Einstellungen in der Kopfzeile

Die Kombination der Einstellungen im Kopfbereich bestimmt, wann und wie eine bestimmte Autokalkulation zu einer Fahrt hinzugefügt wird. Eine Autokalkulation wird nur dann auf eine Fahrt, einen Transportcontainer oder eine Palette angewandt, wenn die Details der Autokalkulation mit den Details in der Kopfzeile des jeweiligen Kostenbereichs übereinstimmen. Die Summe aller übereinstimmenden Autokalkulationen bestimmt die geschätzten Gesamttransportkosten für eine Fahrt. Diese Kosten werden auf alle Artikel auf dem Schiff oder der Fahrt umgelegt.

Die folgende Tabelle beschreibt alle Felder, die im Kopfbereich erscheinen können. Die spezifischen Felder, die zur Verfügung stehen, variieren jedoch, je nachdem, welcher Kostenbereich und welche Dimensionen der Anzeige gerade ausgewählt sind.

| Feld | Beschreibung |
|---|---|
| **Kontocode** | <p>Wählen Sie einen der folgenden Werte aus:</p><ul><li>**Tabelle** - Die Kalkulation gilt nur für einen bestimmten Anbieter.</li><li>**Gruppe** - Die Kalkulationsregel gilt für eine bestimmte Lieferantengruppe. Das System sucht nach der [Lieferanten-Kostentypgruppe](costing-parameters-setup.md), die mit dem Lieferantendatensatz verknüpft ist.</li><li>**Alle** - Die Kalkulationsregel gilt für alle Lieferanten. |
| **Versandunternehmen** | Wählen Sie den Lieferanten oder die Lieferantengruppe aus, für die die Kalkulationsregel gilt. Dieses Feld ist nur verfügbar, wenn Sie *Tabelle* oder *Gruppe* im Feld **Kontocode** wählen. |
| **Zollbroker** | Wählen Sie den Lieferanten oder die Lieferantengruppe aus, für die die Kalkulationsregel gilt. Dieses Feld ist nur verfügbar, wenn Sie *Tabelle* oder *Gruppe* im Feld **Kontocode** wählen. |
| **Artikelcode** | <p>Wählen Sie einen der folgenden Werte aus:</p><ul><li>**Tabelle** - Die Kalkulationsregel gilt nur für einen bestimmten Artikel.</li><li>**Gruppe** - Die Kalkulationsregel gilt für eine bestimmte Artikelgruppe. Das System sucht nach der [Artikel-Kostentyp-Gruppe](costing-parameters-setup.md), die mit dem Artikel-Datensatz verknüpft ist.</li><li>**Alle** - Die Kalkulationsregel gilt für alle Artikel.|
| **Artikelrelation** | Wählen Sie den Artikel oder die Artikelgruppe, für die die Kalkulation gilt. Dieses Feld ist nur verfügbar, wenn Sie *Tabelle* oder *Gruppe* im Feld **Artikelcode** wählen. |
| **Lieferart** | Wählen Sie die Versandart (z. B. Luft- oder Seefracht), für die die Kalkulationsregel gilt. |
| **Containertyp** | Der Typ des Transportcontainers, in dem die Waren verschickt werden. Eine Autokalkulation kann nur auf eine Fahrt angewendet werden, wenn der Containertyp in der Autokalkulation-Einrichtung mit dem Containertyp der Fahrt übereinstimmt. |
| **Vom Hafen** und **An Hafen** | Der Quellhafen („Von“) und der Zielhafen („An“) der Fahrt. (Einige Transportcontainer können verschiedene „Nach“-Häfen haben, weil die Fahrt in mehreren Häfen Halt machen kann.) Eine Autokalkulation kann nur dann auf eine Fahrt angewendet werden, wenn die „Von“- und „Nach“-Häfen in der Autokalkulation-Einrichtung mit den „Von“- und „Nach“-Häfen der Fahrt übereinstimmen. |
| **Automatische Kostennummer** | Der eindeutige Bezeichner der Autokalkulations-Regel. Der Wert dieses Feldes wird automatisch generiert, basierend auf der Sequenz der Nummern, die auf der Seite **Gesamttransportkosten-Parameter** festgelegt wurde. |
| **Lagerungsdimensionen** | In einigen Kalkulationsbereichen können Sie eine oder mehrere Dimensionen des Artikels in die Kopfzeile aufnehmen (z.B. Größe, Farbe, Lagerort und Chargennummer). Wählen Sie **Dimensionen anzeigen** im Aktivitätsbereich, um die Dimensionen auszuwählen, die einbezogen werden sollen. |

## <a name="settings-on-the-lines-fasttab"></a>Einstellungen auf dem Inforegister Linien

Fügen Sie auf dem Inforegister **Zeilen** eine Zeile für jede Währung hinzu, die verwendet werden kann, wenn eine Kalkulation auf eine Zeile einer Einkaufsbestellung auf einer Fahrt angewendet wird. 

Bei Artikeln und Bestellungen gleicht das System die Währung jeder Einkaufsbestellung mit den Währungen ab, die auf der Registerkarte **Zeilen** angegeben sind. Es wendet nur den Wert der Kalkulation an, der für die passende Zeile oder den passenden Artikel festgelegt ist. Wenn keine Zeile für die Währung der Zeile oder des Artikels festgelegt ist, wird die Autokalkulation nicht auf diese Zeile oder diesen Artikel angewandt.

Für andere Arten von Kostenbereichen werden alle Zeilen auf dem Inforegister **Zeilen** auf jede Fahrt, jeden Transportcontainer, jede Palette oder jeden Umlagerungsauftrag angewendet, die mit den Werten übereinstimmen, die in der Kopfzeile festgelegt wurden.

Die folgende Tabelle beschreibt alle Felder, die in jeder Zeile erscheinen können. Die spezifischen Felder, die zur Verfügung stehen, variieren jedoch je nach dem aktuell ausgewählten Kostenbereich.

| Feld | Beschreibung |
|---|---|
| **Währung** | Wählen Sie die Währung, für die die Zeile gilt. Diese Währung bezieht sich auf die Einkaufsbestellung. Wenn das System versucht, die Autokalkulationen zu finden, die auf eine Fahrt und ihre Zeilen angewendet werden sollen, wählt es die Zeile aus, die die gleiche Währung wie die Einkaufsbestellung hat. Dieses Feld ist nur verfügbar, wenn das Feld **Kostenbereich** auf *Bestellung* oder *Artikel* festgelegt ist. |
| **Kostentypcode** | Die Art der Kalkulation. |
| **Umlagemethode** | <p>Die Methode, mit der die Kosten auf die Zeilen verteilt werden. Die folgenden Optionen stehen zur Verfügung:</p><ul><li><p>**Prozentsatz** - Der Wert des Feldes **Kostenwert** ist ein Prozentsatz, der für den Gesamtwert der Waren gilt.</p><p>Wenn zum Beispiel das Feld **Kostenwert** auf *10* festgelegt ist und der Gesamtwert der Waren 800 $ beträgt, ist der Kostenwert 80 $ (= 800 $ × 10 Prozent).</p></li><li>**Menge** - Die Kosten werden auf Basis der Menge der Waren umgelegt.</li><li>**Betrag** - Die Kosten werden auf Basis des Wertes der Waren umgelegt.</li><li>**Volumen** - Die Kosten werden auf der Basis des Volumens der Waren umgelegt. Das Volumen wird im Artikelstamm angegeben.</li><li>**Gewicht** - Die Kosten werden auf der Basis des Gewichts der Waren umgelegt. Das Gewicht wird im Artikelstamm angegeben.</li><li>**Volumetrisch** - Die Kosten werden auf der Grundlage der volumetrischen Messung der Waren umgelegt.</li><li><p>**Messung** - Mit dieser Option kann eine Messung im Modul **Gesamttransportkosten** angegeben werden. Sie wird oft von Unternehmen verwendet, die das individuelle Volumen oder Gewicht der Waren nicht kennen, aber eine genauere Aufteilung benötigen, als es die Optionen **Betrag** und **Menge** ermöglichen. Der Spediteur oder Agent stellt dem Unternehmen die Gewichts- oder Volumenmessung zur Verfügung, entweder auf der Ebene des Artikels oder auf der Ebene der Einkaufsbestellung.</p><p>Beispiel: Seefracht beträgt $900. Artikel A hat ein Gewicht von 800 Kilogramm (kg) und ein Volumen von 2 Kubikmetern (m³). Artikel B hat ein Gewicht von 100 kg und ein Volumen von 1 m³. Hier sind die Ergebnisse, wenn die Kosten nach Gewicht aufgeteilt werden:</p><ul><li>Artikel A = $800</li><li>Artikel B = $100</li></ul><p>Hier sind die Ergebnisse, wenn die Kosten nach Volumen aufgeteilt werden:</p><ul><li>Artikel A = $600</li><li>Artikel B = $300</li></ul><p>**Hinweis:** Wenn das Feld **Aufteilungsmethode** auf *Messung* festgelegt ist, verwendet das System die Messungen, die sowohl für den Kostenbereich (den Transportcontainer) als auch für die Zeilen eingegeben werden. Diese Messungen müssen sich nicht unbedingt zur erwarteten Gesamtsumme addieren. Wenn Sie jedoch verlangen, dass sie sich zur erwarteten Summe addieren, können Sie eine Überprüfung durchführen, indem Sie die Statistik verwenden, um die Gesamtmessung zu überprüfen. Die Einstellung für die Abfrage der Messung und die automatische Aktualisierung der Messung auf Transport- oder Containerebene werden im Kopf der Fahrt festgelegt.</p></li></ul> |
| **Anfangsdatum** | Geben Sie den Beginn des Datumsbereichs für die Kalkulation an, wenn es einen Datumsbereich gibt. Dieses Datum ist das erste Datum, an dem die Autokalkulation angewendet wird. |
| **Enddatum** | Legen Sie das Ende des Datumsbereichs für die Kalkulation fest, wenn es einen Datumsbereich gibt. Dieses Datum ist das letzte Datum, an dem die Autokalkulation gelten soll. |
| **Kategorie** | <p>Wählen Sie die Methode, die für die Kalkulation verwendet werden soll. Die folgenden Optionen stehen zur Verfügung:</p><ul><li>**Fest** - Die Kalkulation wird auf der Grundlage der Umlagemethode durchgeführt.</li><li>**Stück** - Die Kosten werden pro Stück umgelegt. Daher wird die Umlagemethode nicht verwendet.</li><li>**Prozent** - Es wird ein Prozentsatz des Wertes der Waren zugerechnet. Daher wird die Umlagemethode nicht verwendet.</li><li>**Satz** - Wählen Sie diese Option, wenn es Mengenaufteilungen gibt. Das Feld **Aufteilungsmethode** für die Zeile muss auf *Messung* festgelegt sein.</li><ul> |
| **Aufgeschlüsselt nach Menge** | <p>Aktivieren Sie dieses Kontrollkästchen, um die Schaltfläche **Mengenbrüche** auf dem Inforegister **Zeilen** verfügbar zu machen. Mengenbrüche ermöglichen es, die Kosten aufzuschlüsseln und die verschiedenen Kalkulationen in Abhängigkeit von der Menge in der Zeile der Einkaufsbestellung der Fahrt zu variieren. Diese Funktionalität wird oft verwendet, wenn die Lieferart Luft ist. Das Feld **Kategorie** für die Zeile muss auf *Satz* festgelegt werden.</p><p>Die Menge bezieht sich auf die Option, die im Feld **Aufteilungsmethode** ausgewählt ist. Der Kalkulationswert entspricht der Menge, die im Feld **Kalkulationswert** eingegeben wird.<p>Zum Beispiel erzeugen Mengen von 45-100 kg eine Gebühr von $6,00 pro Messung (wie kg/m³). Mengen, die 100 kg überschreiten, erzeugen eine Gebühr von $5,50 pro Messung (z.B. kg/m³).</p> |
| **Einstandswert** | Geben Sie den Wert der Kalkulation ein. |
| **Kostenwährungscode** | Wählen Sie die Währung für die Kalkulation. |
| **Artikel-Mehrwertsteuergruppe** | Wählen Sie das Steuerkennzeichen für die Kalkulation. |
| **Mindestkosten** | <p>Dieses Feld gilt nur, wenn das Kontrollkästchen **Aufgeschlüsselt nach Menge** aktiviert ist. Wenn die Messung diesen Wert nicht erreicht, wird der Mindestwert gewählt, unabhängig von den Kosten, die auf der Seite **Mengenbrüche** angegeben sind.<p>Mengen von 0-45 kg erzeugen z.B. eine Gebühr von $6 pro Messung (kg/m³). Mengen von 46-100 kg ergeben eine Gebühr von $5,50 pro Messung (kg/m³). Wenn 2 kg versendet werden, erstellt der Mengenbruch einen Kostenwert von $12. Wenn jedoch das Feld **Mindestkosten** auf *$100* festgelegt ist, beträgt die endgültige Kalkulation $100.</p> |
| **Aggregieren** | Aktivieren Sie dieses Kontrollkästchen, damit der Benutzer diese Kalkulation von der Ebene des Transportcontainers auf die Ebene der Fahrt verschieben kann. In diesem Fall können die Kosten automatisch auf der Ebene des Transportcontainers kalkuliert werden. Sie können aber auch kombiniert und auf alle Artikel in allen Transportcontainern auf einer Fahrt umgelegt werden, anstatt auf alle Artikel in den einzelnen Transportcontainern. |
| **Verknüpfter Kostentyp** | <p>Verknüpfen Sie die aktuelle Zeile mit einer anderen Zeile im gleichen Autokalkulations-Datensatz, indem Sie den **Kostenartencode** der Zeile angeben, mit der Sie verknüpft werden sollen. Diese Funktionalität ist nur verfügbar, wenn das Feld **Kategorie** für die aktuelle Zeile auf *Prozent* festgelegt ist. Wenn die aktuelle Zeile mit einer anderen Zeile verknüpft ist, basieren die Kosten der aktuellen Zeile auf den Kalkulationen der anderen Zeile.</p><p>Beispiel: Die Fracht beträgt $1.000, und Sie möchten, dass der Treibstoffzuschlag 10 Prozent der Frachtkosten beträgt. In diesem Fall muss die Zeile einen **Kategorie**-Wert von *Prozent*, einen **Kostenwert**-Wert von *10%* und einen **verknüpften Kostentyp**-Wert von *Fracht* haben.</p> |
| **Wertanpassung** und **Anpassungsbetrag** | <p>Verwenden Sie diese Felder, um den Wert und den Betrag für verschiedene Prozentwerte anzupassen. Sie sind nur verfügbar, wenn das Feld **Kostenbereich** auf *Artikel* festgelegt ist.</p><p>Für verschiedene Komponenten eines Artikels kann eine unterschiedliche Kalkulation festgelegt werden. Eine Komponente eines Artikels kann eine andere prozentuale Kalkulation haben als die anderen Komponenten dieses Artikels. Dieser Ansatz ist manchmal erforderlich, um einen bestimmten Teil der Waren mit unterschiedlichen Sätzen zu bewerten.</p><p>Zum Beispiel wird der Zoll für eine Uhr mit zwei Sätzen berechnet: eine Komponente der Uhr hat einen 10-prozentigen Zollsatz und eine zweite Komponente hat einen 2-prozentigen Zollsatz. In diesem Fall wird die Kalkulation auf die beiden Komponenten aufgeteilt.</p><p>Die Kalkulation wird für den Artikel berechnet, aber der Kalkulationswert wird um den Wert der Komponenten angepasst, die die unterschiedliche Kostenkategorie haben. Die Kosten der verbleibenden Komponenten können dann unter Verwendung des Betrags berechnet werden, um den die vorherige Kalkulation angepasst wurde.</p><p>Beispiel: Komponente A der Uhr hat Kosten von $9,50 und eine Kalkulation von 10 Prozent, und Komponente B hat Kosten von $0,50 und eine Kalkulation von 2 Prozent. Daher betragen die Gesamtkosten $10,00. Der erste Eintrag ist für die 10-Prozent-Zeile. Er verwendet die folgenden Werte:</p><ul><li>**Kategorie:** *Prozentsatz*</li><li>**Kalkulationswert:** *10*</li><li>**Wert angepasst:** *Anpassen um*</li><li>**Angepasster Wert:** *-0,50*</li></ul><p>Diese Einrichtung legt fest, dass die Kosten des Artikels ($10) um $0,50 (den Preis der Komponente B) reduziert werden müssen, bevor eine 10-prozentige Zollgebühr berechnet wird. Daher werden 10 Prozent auf $9,50 angewendet.</p><p>Die zweite Eingabe ist für die 2-Prozent-Zeile (die $0,50, um die die vorherige Eingabe angepasst wurde). Er verwendet die folgenden Werte:</p><ul><li>**Kategorie:** *Prozentsatz*</li><li>**Kalkulationswert:** *2*</li><li>**Wert angepasst:** *Verwendung*</li><li>**Anpassung:** *0,50*</li></ul><p>Dieses Setup berechnet den verbleibenden Zoll, der auf Komponente B zu zahlen ist.</p> |
