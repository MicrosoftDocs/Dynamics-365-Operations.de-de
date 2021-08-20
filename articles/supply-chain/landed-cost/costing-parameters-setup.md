---
title: Kalkulation Parameterwerte einrichten
description: Beim Einrichten des Moduls Gesamttransportkosten können Sie mehrere Sätze allgemeiner Werte festlegen, die zur Verfügung stehen, wenn Sie bestimmte Arten von Kalkulationsparameterwerten in anderen Teilen der App auswählen. In diesem Thema wird erklärt, wie Sie diese Wertesätze festlegen.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMCostTypeTable, ITMCostTypeGroup, ITMCostTransferGroup, ITMCostTemplateTable, ITMVolumetricDivisorTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: dada2f9a3ae13f41b7f63d1f0907002860d0717ff9d8c2453fc6f3ad123cbf78
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736742"
---
# <a name="costing-parameter-values-setup"></a>Kalkulation Parameterwerte einrichten

[!include [banner](../../includes/banner.md)]

Wenn Sie das Modul **Gesamttransportkosten** festlegen, können Sie mehrere Sätze von allgemeinen Werten und zugehörigen Einstellungen pro Wert definieren. Diese Werte stehen dann zur Verfügung, wenn Sie bestimmte Typen von Kalkulationsparameterwerten in anderen Teilen der App auswählen. In diesem Thema wird erklärt, wie Sie diese Wertesätze festlegen.

## <a name="set-up-cost-type-codes"></a>Festlegen von Codes für die Kalkulation

Kostenartencodes bestimmen die Art der Kosten, die bei der Anlandung der Waren im Lagerort anfallen, oder die Anlandungskosten der Fahrt. Obwohl sie in der Regel den Wert der Waren erhöhen, können sie auch verwendet werden, um Beträge in das Hauptbuch einzutragen. Ledger-Anpassungen werden verwendet, wenn Kosten im Laufe der Zeit oder während einer Reihe von Fahrten anfallen und in einer einzigen Transaktion verrechnet werden.

> [!NOTE]
> Wenn die Tabelle der Kostenarten für juristische Entitäten gemeinsam genutzt wird, muss auch der Kontenplan für juristische Entitäten gemeinsam genutzt werden. Andernfalls funktionieren die Buchungstransaktionen nicht korrekt.

Um Ihre Kostenartencodes festzulegen, gehen Sie zu **Gesamttransportkosten \> Kalkulation einrichten \> Kostenartencodes**. Mit den Schaltflächen im Aktivitätsbereich können Sie neue Kostenartencodes erstellen, vorhandene Codes bearbeiten oder eine ausgewählte Kostenart löschen.

Die folgende Tabelle beschreibt die Felder, die für jeden Kostenartencode zur Verfügung stehen.

| Feld | Beschreibung |
|---|---|
| Kostentypcode | Geben Sie einen Namen für den Kostenartencode ein. |
| Beschreibung | Geben Sie eine Beschreibung für den Kostenartencode ein. |
| Versandrate verwenden | Legen Sie diese Option auf *Ja* fest, wenn der Exchange-Satz der Fahrt (manchmal auch als Management-Satz bezeichnet) für die Kalkulation dieser Kosten verwendet werden muss. In diesem Fall wird der Fahrtkurs anstelle des Standard-Standard- oder Spot-Wechselkurses zum Umrechnen von Fremdwährungsrechnungen verwendet. |
| Berichtskategorie | Dieses Feld legt eine Berichtskategorie für die Kostenart fest. Berichte können entweder nach Berichtskategorien oder nach Kostenart gedruckt werden. |
| Solltyp | Wählen Sie aus, ob die Kostenart den Artikel, das Ledger-Konto oder den Lieferanten belasten soll. |
| Sollbuchung | Wenn das Feld **Belastungstyp** auf *Ledger-Konto* festgelegt ist, wählen Sie die Buchungsbeschreibung. |
| Sollkonto | Wenn das Feld **Belastungstyp** auf *Ledger-Konto* festgelegt ist, wählen Sie das zu verwendende Ledger-Konto. |
| Gutschrifttyp | Wählen Sie aus, ob dieser Kalkulationstyp den Artikel, das Ledger-Konto oder den Lieferanten entlasten soll. |
| Habenbuchung | Wenn das Feld **Gutschriftstyp** auf *Ledger-Konto* festgelegt ist, wählen Sie die Buchungsbeschreibung. |
| Habenkonto | Wenn das Feld **Kreditart** auf *Ledger-Konto* festgelegt ist, wählen Sie das zu verwendende Ledger-Konto. |
| Clearingkonto | Wählen Sie das Verrechnungskonto für die Kalkulationsart. Wir empfehlen, für jede Kostenart ein eigenes Verrechnungskonto anzugeben, um die Abstimmung zu erleichtern. |
| Standard-Kostenbuchungsart | Wenn Sie eine Standardkalkulation verwenden, wählen Sie die Buchungsbeschreibung. |
| Standardkostenabweichungs-Konto | <p>Wenn Sie die Standardkalkulation verwenden, wird das hier angegebene Konto für die Buchung einer Abweichung verwendet. Dieses Konto verwendet die Aufschlüsselung der Gesamttransportkosten auf der Seite **Artikelpreise**. Diese Aufschlüsselung wird mit Hilfe der periodischen Routine zur Aktualisierung der Preise erstellt.</p><p>Beispiel: Die Standardkosten eines Artikels sind $15,00, die FOB ist $13,00 und die Fracht ist $2,00. Wenn die Rechnung für den Bestand eingeht, wird der Artikel zu $15,00 empfangen, aber es gibt eine Standardpreisabweichung von $2,00 für den Artikel, weil die tatsächliche FOB $13,00 ist. Diese Abweichung wird auf das Standardpreisabweichungskonto gebucht, das im Artikelbuchungsprofil festgelegt ist. Da die geschätzte Fracht $2,00 beträgt, gibt es keine Abweichung, wenn die Lagerrechnung gebucht wird. Wenn jedoch die Rechnung für die Fracht eingeht, beträgt die Fracht 2,50 $ pro Einheit. Daher wird eine Abweichung von $0,50 auf die angegebenen Kosten gebucht. |
| Gleitender Durchschnitt für Abweichungskonto | <p>Wenn Sie mit gleitender Durchschnittskalkulation arbeiten, wird das hier angegebene Konto für die Buchung der Abweichung verwendet.</p><p>Zum Beispiel beträgt die geschätzte Fracht $2,00. Wenn jedoch die Rechnung für die Fracht eingeht, beträgt die Fracht 2,50 $ pro Einheit. Daher muss eine Abweichung von $0,50 gebucht werden.</p><p>Wenn die Option **Anpassungen als Abweichung buchen** auf der Seite **Gesamttransportkosten-Parameter** auf *Ja* festgelegt ist, werden alle Abweichungen zwischen geschätzten und tatsächlichen Transportkosten auf das hier angegebene Konto für gleitende Durchschnittsabweichungen gebucht. Wenn die Option **Anpassungen als Abweichung buchen** auf *Nein* festgelegt ist, wird die Standardfunktionalität verwendet, und die Abweichung wird je nach Lagerbestand entweder auf den Bestand oder auf das hier festgelegte Konto für gleitende Durchschnittsabweichungen angewendet.</p> |
| Abgrenzungskonto für Belastungen | Wählen Sie das Konto aus, das für Kalkulationen bei der Buchung der Kaufrechnung verwendet wird. Dieses Feld wird nur verwendet, wenn die Option **Kostenart Belastungsabgrenzungskonto verwenden** auf *Ja* im Inforegister **Kalkulation** auf der Registerkarte **Allgemein** der Seite **Gesamttransportkostenparameter** festgelegt ist. |
| Belastungskonto | Wählen Sie das Konto aus, das zur Erfassung der eingehenden Transportkosten verwendet wird, die von einem Lieferanten in Rechnung gestellt wurden. Der Betrag wird als Lastschrift gebucht. Das Gegenkonto ist das Bestandsabweichungskonto. Diese Buchung wird nur verwendet, wenn auf der Seite **Kreditorenparameter** die Option **Buchen auf Belastungskonto im Hauptbuch** auf *Ja* festgelegt ist. |
| Abweichungskonto | Das Konto, das bei der Buchung der Kauf-Rechnung zur Verrechnung der Gebührenabgrenzungen verwendet wird. Dieses Feld wird nur verwendet, wenn die Option **Kostenart Belastungsabgrenzungskonto verwenden** auf *Ja* im Inforegister **Kalkulation** auf der Registerkarte **Allgemein** der Seite **Gesamttransportkostenparameter** festgelegt ist. |

## <a name="vendor-cost-type-groups"></a>Kostentypgruppen für Kreditor

Die Kostenartengruppen der Lieferanten bestimmen, wie die *Autokalkulation* gefunden und auf eine Fahrt angewendet wird. Lieferanten, die ähnliche Kalkulationen haben, werden miteinander verknüpft. Zum Beispiel zahlen alle Lieferanten aus Schwellenländern den gleichen Prozentsatz an Zöllen für die gleiche Art von Produkt, das von einem etablierten Markt gekauft wird.

Sie können Lieferanten-Kostenartengruppen pflegen, indem Sie zu **Gesamttransportkosten \> Kalkulation einrichten \> Lieferanten-Kostenartengruppen** gehen. Die Seite **Lieferanten-Kostenartengruppen** bietet ein Raster, das alle vorhandenen Lieferanten-Kostenartengruppen auflistet. Sie können die Schaltflächen im Aktivitätsbereich verwenden, um Zeilen im Raster hinzuzufügen, zu entfernen und zu bearbeiten.

Die folgende Tabelle beschreibt die Felder, die in jeder Zeile des Rasters verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Kostentypgruppen für Kreditor | Geben Sie einen eindeutigen Namen für die Kostenartengruppe des Lieferanten ein (z. B. *Aufstrebende Märkte*). |
| Beschreibung | Geben Sie eine Beschreibung der Kostenartengruppe des Lieferanten ein. Diese Beschreibung kann Details über die Höhe oder Art der Gebühr liefern, die mit der Lieferantengruppe verbunden ist. |

## <a name="item-cost-type-groups"></a>Kostentypgruppen für Artikel

Artikel-Kostentypgruppen helfen zu bestimmen, wie *Autokalkulation* Gebühren gefunden und auf eine Fahrt angewendet werden. Ähnliche Artikel werden miteinander verknüpft. Zum Beispiel könnten alle Artikel, die einen Zollsatz von 5 Prozent haben, zu einer bestimmten Kostenartengruppe gehören.

Sie können Artikel-Kostenartengruppen pflegen, indem Sie zu **Gesamttransportkosten \> Kalkulation einrichten \> Artikel-Kostenartengruppen** gehen. Die Seite **Artikel-Kostenartengruppen** bietet ein Raster, das alle vorhandenen Artikel-Kostenartengruppen auflistet. Sie können die Schaltflächen im Aktivitätsbereich verwenden, um Zeilen im Raster hinzuzufügen, zu entfernen und zu bearbeiten.

Die folgende Tabelle beschreibt die Felder, die in jeder Zeile des Rasters verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Kostentypgruppen für Artikel | Geben Sie einen eindeutigen Namen für die Artikel-Kostenartengruppe ein (z.B. *Zoll 5%*). |
| Beschreibung | Geben Sie eine Beschreibung der Kostenartengruppe für Artikel ein. Diese Beschreibung kann Details über die Höhe oder Art der Gebühr liefern, die mit der Artikelgruppe verbunden ist. |

> [!NOTE]
> Die Artikelkostenart ist mit dem Artikel über das Feld **Kostenartengruppe** auf dem Inforegister **Kauf** der Seite **Freigegebenes Produkt** des Artikels verknüpft.

## <a name="transfer-order-cost-type-groups"></a>Umlagerungsauftrag Kostenartengruppen

Umlagerungsauftrag-Kostentypgruppen helfen zu bestimmen, wie *Autokalkulation* Kosten gefunden werden. Ähnliche Artikel werden miteinander verknüpft. Zum Beispiel könnten alle Artikel, die einen Zollsatz von 7 Prozent haben, zu einer bestimmten Kostenartengruppe gehören.

Sie können Transportauftrags-Kostenartengruppen pflegen, indem Sie zu **Gesamttransportkosten \> Kalkulation einrichten \> Umlagerungsauftrag-Kostenartengruppen** gehen. Die Seite **Umlagerungsauftrag Kostenartengruppen** bietet ein Raster, in dem alle vorhandenen Umlagerungsauftrag Kostenartengruppen aufgelistet sind. Sie können die Schaltflächen im Aktivitätsbereich verwenden, um Zeilen im Raster hinzuzufügen, zu entfernen und zu bearbeiten.

Die folgende Tabelle beschreibt die Einstellungen, die in jeder Zeile des Rasters verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Umlagerungsauftrag Kostenartengruppen | Geben Sie einen eindeutigen Namen für die Kostenartengruppe des Umlagerungsauftrags ein (z. B. *Zoll 7%*). |
| Beschreibung | Geben Sie eine Beschreibung der Kostenartengruppe für den Umlagerungsauftrag ein. Diese Beschreibung kann Details über die Höhe oder Art der Kalkulation liefern, die mit der Kostenartengruppe des Umlagerungsauftrags verbunden ist. |

> [!NOTE]
> Die Kostenart des Umlagerungsauftrags ist mit dem Artikel über das Feld **Kostengruppe des Umlagerungsauftrags** auf dem Inforegister **Einkauf** der Seite **Freigegebenes Produkt** des Artikels verknüpft.

## <a name="cost-templates"></a>Kostenvorlagen

Sie verwenden Kostenvorlagen, um Standardwerte für Einstellungen festzulegen, die Benutzer, die die Kalkulation erhalten, möglicherweise nicht kennen. Kostenvorlagen können dazu beitragen, die Komplexität im Kalkulationsprozess zu reduzieren, indem sie die Auswahlen minimieren, die Benutzer treffen müssen, um eine genaue Kalkulation zu erhalten.

Um mit Kostenvorlagen zu arbeiten, gehen Sie zu **Gesamttransportkosten \> Kalkulation einrichten \> Kostenvorlagen**. Auf der Seite **Kostenvorlagen** zeigt der Listenbereich auf der linken Seite alle aktuellen Kalkulationsvorlagen an. Sie können die Schaltflächen im Aktivitätsbereich verwenden, um Vorlagen hinzuzufügen, zu entfernen und zu bearbeiten.

Die folgende Tabelle beschreibt die Einstellungen, die für jede Vorlage verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Kostenvorlage | Geben Sie einen eindeutigen Namen für die Kalkulationsvorlage ein. Der Name beschreibt typischerweise den Faktor oder Kostenmultiplikator für die Vorlage. |
| Beschreibung | Geben Sie eine Beschreibung für die Kalkulationsvorlage ein. |
| Versandunternehmen | Wählen Sie das Lieferantenkonto der Firma, die mit der Kalkulation-Vorlage verknüpft werden soll. |
| Lieferart | Wählen Sie die Versandart, die die Kostenvorlage bei der Berechnung der geschätzten Kosten eines Artikels verwenden soll. Dieses Feld hilft bei der Bestimmung der Autokalkulationen, die mit den Waren auf der Kalkulation verbunden sind. |
| Versandcontainertyp | Wählen Sie den Typ des Transportcontainers, der mit der Kostenvorlage verknüpft werden soll. Dieses Feld hilft bei der Bestimmung der Autokalkulationen, die mit den Waren auf der Kalkulation verbunden sind. |
| Zollbroker | Wählen Sie den Zoll Broker (Lieferant), der mit der Kalkulationsvorlage verknüpft werden soll. Dieses Feld hilft bei der Bestimmung der Autokalkulationen, die mit der Kalkulation verknüpft werden. |
| Faktor | Geben Sie einen Faktor ein, der auf die endgültige Kalkulation der Waren angewendet werden soll. Um z.B. 10 Prozent auf die kalkulierte Kalkulation zu addieren, geben Sie *1,10* ein. |

## <a name="volumetric-divisors"></a>Volumetrische Divisoren

Volumendivisoren werden verwendet, um das Volumengewicht zu berechnen. Jede Firma formuliert ihre eigenen volumetrischen Divisoren. Darüber hinaus variieren die Divisoren einer Firma typischerweise je nach Lieferart. Zum Beispiel haben Luft- und Seefracht oft sehr unterschiedliche Divisoren. Eine Firma kann ihre Regeln auch komplexer gestalten, je nachdem, von wo aus sie versendet.

Zum Beispiel hat ein Paket, das per Luftfracht verschickt wird, ein Volumen von 3 Kubikmetern (m³). Die Firma berechnet nach Volumengewicht und wendet einen Volumendivisor von 6 an. Dieser Divisor wird mit dem Volumen multipliziert, um das Volumengewicht zu ermitteln. Daher beträgt das Volumengewicht für dieses Beispiel 3 × 6 = 18 Kilogramm (kg).

Um volumetrische Divisoren festzulegen, gehen Sie zu **Gesamttransportkosten \> Kalkulation einrichten \> Volumetrische Divisoren**. Die Seite **Volumetrische Teiler** bietet ein Raster, das alle vorhandenen volumetrischen Teiler auflistet. Sie können die Schaltflächen im Aktivitätsbereich verwenden, um Zeilen im Raster hinzuzufügen, zu entfernen und zu bearbeiten.

Die folgende Tabelle beschreibt die Felder, die in jeder Zeile des Rasters verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Versandunternehmen | Wählen Sie das Kreditorenkonto der Firma, die mit dem volumetrischen Teiler verbunden ist. |
| Kostentypcode | Wählen Sie den Code der Kalkulation, die mit dem volumetrischen Divisor verbunden ist. Verwenden Sie dieses Feld, um die Kalkulationen in die Berichtsbereiche einzulagern. Berichte können entweder nach Berichtskategorien oder nach Kostenart gedruckt werden. |
| Von-Port | Wählen Sie den „Von Hafen“, für den der Volumendivisor gilt. |
| Volumetrischer Divisor | Geben Sie den Wert des volumetrischen Divisors ein, der für die Zeile gilt. Der von Ihnen eingegebene Wert wird *mit dem Volumen jedes Pakets multipliziert*, um das Volumengewicht dieses Pakets zu bestimmen. |
