---
title: Beispiele und Logik für Lagerwertberichte
description: Dieses Thema enthält einige Beispiele für Ergebnisse, die in den einzelnen Typen von Lagerwertberichten dargestellt werden. Lagerwertberichte enthalten Details zu den physischen und finanziellen Mengen und Beträgen Ihrer Bestände.
author: banluo-ms
ms.date: 10/19/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: banluo
ms.search.validFrom: 2021-10-19
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 4ad85058c8743895185d3da2e8975711f1e3bc2c
ms.sourcegitcommit: ba10ba2cd4fb4267afb5aacae4f6a52aa2456e7e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/11/2021
ms.locfileid: "7798392"
---
# <a name="inventory-value-report-examples-and-logic"></a>Beispiele und Logik für Lagerwertberichte

[!include [banner](../includes/banner.md)]

Lagerwertberichte enthalten Details zu den physischen und finanziellen Mengen und Beträgen Ihrer Bestände. Dieses Thema enthält einige Beispiele für Ergebnisse, die in den einzelnen Typen von Lagerwertberichten dargestellt werden.

Weitere Informationen zum Generieren und Verwenden der einzelnen Typen von Lagerwertberichten finden Sie unter [Lagerwertberichte](inventory-value-report-storage.md).

## <a name="sample-data-that-is-used-in-these-examples"></a>Beispieldaten, die in diesen Beispielen verwendet werden

Die Beispiele in diesem Thema basieren auf den in diesem Abschnitt beschriebenen Beispieltransaktionsdaten für das Inventar.

### <a name="storage-dimension-setup"></a>Lagerdimensionsgruppe einrichten

Das Beispielsystem enthält die folgenden Einstellungen für die Speicherabmessungen.

| Name | Aktiv | Physischer Bestand | Wertmäßiger Bestand |
|---|---|---|---|
| Site | Ja | Ja | Ja |
| Lagerort | Ja | Ja | Nein |

### <a name="inventory-model"></a>Lagermodell

Für das Beispielsystem lautet das Lagermodell für die freigegebenen Produkte *FIFO*, und das Feld **Selbstkostenpreis** für das Lagermodell ist auf *Physischen Wert einbeziehen* eingestellt.

### <a name="inventory-transactions"></a>Lagerbuchungen

Das Beispielsystem enthält die folgenden Lagerbuchungen für ein freigegebenes Produkt mit der Artikelnummer *B0001*.

| Referenz | Standort | Lagerhaus | Zugang | Problem | Physisches Datum | Finanzdatum | Menge | Betrag KORE | Phys. Einstandsbetrag |
|---|---|---|---|---|---|---|---|---|---|
| Bestellung | 1 | 11 | Eingekauft | | 15. März | 15. März | 10 | 1.000 | 1.000 |
| Bestellung | 2 | 21 | Eingekauft | | 15. März | 15. März | 10 | 2,000 | 2,000 |
| Bestellung | 1 | 11 | Eingegangen | | April 15 | | 5 | | 375 |
| Umlagerungsauftrag | 1 | 11 | | Verkauft | Mai 2 | Mai 2 | -5 | -458.33 | -458.33 |
| Umlagerungsauftrag | 1 | 12 | Eingekauft | | Mai 2 | Mai 2 | 5 | 458.33 | 458.33 |
| Auftrag | 1 | 12 | | Verkauft | Mai 3 | Mai 3 | -1 | -91.67 | -91.67 |

### <a name="inventory-value-report-configuration"></a>Lagerwertberichtskonfiguration

Das Beispielsystem enthält eine Lagerwertberichtskonfiguration mit den folgenden Einstellungen:

- **Bereich:** *Buchungsdatum*
- **Bestand:** *Ja*
- **Durchschnittliche Einheitenkosten berechnen:** *Ja*
- **Gesamtmenge und -wert:** *Ja*
- **Standort, Ansicht:** *Ausgewählt*
- **Ressourcen-ID, Ansicht:** *Ja*
- **Ebene:** *Summen*

## <a name="inventory-value-report-example-1"></a>Lagerwertberichtbeispiel 1

Die folgende Tabelle und Abbildungen zeigen die Ergebnisse, wenn Sie die zuvor in diesem Thema beschriebene Beispieldaten- und -berichtskonfiguration verwenden.

| Ressourcentyp | Ressource | Standort | Referenz | Lager: Wertmäßige Menge | Lager: Wertmäßiger Betrag | Lager: Gebuchte physische Menge | Lager: Gebuchter physischer Betrag | Lager: Menge | Lager: Betrag | Durchschnittliche Einheitskosten |
|---|---|---|---|---|---|---|---|---|---|---|
| Material | B0001 | 1 | Endsaldo | 9.00 | 908.33 | 5.00 | 375.00 | 14,00 | 1,283.33 | 91.67 |
| Material | B0001 | 2 | Endsaldo | 10.00 | 2,000.00 | 0,00 | 0,00 | 10.00 | 2,000.00 | 200.00 |

### <a name="standard-inventory-value-report-for-example-1"></a>Standardlagerwertbericht für Beispiel 1

Die folgende Abbildung zeigt den Standard **lagerwert** bericht für Beispiel 1. (Wählen Sie die Abbildung aus, um eine größere Version zu öffnen.)

[![Standardlagerwertbericht für Beispiel 1.](media/inventory-value-report-ex1-small.png "Standardlagerwertbericht für Beispiel 1")](media/inventory-value-report-ex1.png)

### <a name="inventory-value-report-storage-report-for-example-1"></a>Lagerwert-Berichtsspeicher-Bericht für Beispiel 1

Die folgende Abbildung zeigt den **Lagerwert-Berichtspeicher**-Bericht für Beispiel 1. (Wählen Sie die Abbildung aus, um eine größere Version zu öffnen.)

[![Lagerwert-Berichtsspeicher-Bericht für Beispiel 1.](media/inventory-value-report-storage-ex1-small.png "Lagerwert-Berichtsspeicher-Bericht für Beispiel 1")](media/inventory-value-report-storage-ex1.png)

## <a name="inventory-value-report-example-2"></a>Lagerwertberichtbeispiel 2

Die folgende Tabelle und die folgenden Abbildungen zeigen die Ergebnisse, wenn Sie die weiter oben in diesem Thema beschriebenen Beispieldaten verwenden, aber den Wert im Feld **Ebene** in der Berichtskonfiguration auf *Buchungen* ändern das Feld **Startdatum** auf den *15. März* ändern, wenn Sie den Bericht ausführen.

| Ressourcentyp | Ressource | Standort | Datum | Anzahl | Referenz | Lager: Wertmäßige Menge | Lager: Wertmäßiger Betrag | Lager: Gebuchte physische Menge | Lager: Gebuchter physischer Betrag | Lager: Menge | Lager: Betrag |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Material | B0001 | 1 | 15.03.2021 | 00000126 | Bestellung | 0,00 | 0,00 | 10.00 | 1,000.00 | **10.00** | **1,000.00** |
| Material | B0001 | 1 | 15.03.2021 | 00000126 | Bestellung | 10.00 | 1,000.00 | -10,00 | -1.000,00 | **0.00** | **0.00** |
| Material | B0001 | 1 | 15.04.2021 | 00000128 | Bestellung | 0,00 | 0,00 | 5.00 | 375.00 | **5.00** | **375.00** |
| Material | B0001 | 1 | 02.05.2021 | 000003 | Umlagerungsauftragslieferung | -5,00 | -458.33 | 0,00 | 0,00 | **-5.00** | **-458.33** |
| Material | B0001 | 1 | 02.05.2021 | 000003 | Umlagerungsauftragsempfang | 5.00 | 458.33 | 0,00 | 0,00 | **5.00** | **458.33** |
| Material | B0001 | 1 | 03.05.2021 | 000835 | Auftrag | 0,00 | 0,00 | -1,00 | -91.67 | **-1.00** | **-91.67** |
| Material | B0001 | 1 | 03.05.2021 | 000835 | Auftrag | -1,00 | -91.67 | 1.00 | 91.67 | **0.00** | **0.00** |
| Material | B0001 | 2 | 15.03.2021 | 00000127 | Bestellung | 0,00 | 0,00 | 10.00 | 2,000.00 | **10.00** | **2,000.00** |
| Material | B0001 | 2 | 15.03.2021 | 00000127 | Bestellung | 10.00 | 2,000.00 | -10,00 | -2,000,00 | **0.00** | **0.00** |
| Material | B0001 | 2 | 02.05.2021 | 000003 | Umlagerungsauftragslieferung | 5.00 | 458.33 | 0,00 | 0,00 | **5.00** | **458.33** |
| Material | B0001 | 2 | 02.05.2021 | 000003 | Umlagerungsauftragsempfang | -5,00 | -458.33 | 0,00 | 0,00 | **-5.00** | **-458.33** |

### <a name="standard-inventory-value-report-for-example-2"></a>Standardlagerwertbericht für Beispiel 2

Die folgende Abbildung zeigt den Standard **lagerwert** bericht für Beispiel 2. (Wählen Sie die Abbildung aus, um eine größere Version zu öffnen.)

[![Standardlagerwertbericht für Beispiel 2.](media/inventory-value-report-ex2-small.png "Standardlagerwertbericht für Beispiel 2")](media/inventory-value-report-ex2.png)

### <a name="inventory-value-report-storage-report-for-example-2"></a>Lagerwert-Berichtsspeicher-Bericht für Beispiel 2

Die folgende Abbildung zeigt den **Lagerwert-Berichtspeicher**-Bericht für Beispiel 2. (Wählen Sie die Abbildung aus, um eine größere Version zu öffnen.)

[![Lagerwert-Berichtsspeicher-Bericht für Beispiel 2.](media/inventory-value-report-storage-ex2-small.png "Lagerwert-Berichtsspeicher-Bericht für Beispiel 2")](media/inventory-value-report-storage-ex2.png)

## <a name="inventory-value-report-example-3"></a>Lagerwertberichtbeispiel 3

Sie sollten Lagerwertberichte nach der Neuberechnung oder dem Lagerabschluss auszuführen, damit Sie die Buchungen und Beträge haben, die von der Neuberechnung oder dem Lagerabschluss betroffen sind.

Die folgenden Unterabschnitte zeigen die Lagerwertberichte, die nach dem Lagerabschluss bis zum 30. Mai generiert werden.

### <a name="example-3-when-the-totals-level-is-used"></a>Beispiel 3 bei Verwendung der Summenebene

Die folgende Tabelle zeigt die Ergebnisse, wenn Sie die zuvor in diesem Thema beschriebene Beispieldaten- und -berichtskonfiguration verwenden. (In dieser Berichtskonfiguration ist das Feld **Ebene** auf *Summen* gesetzt.)

| Ressourcentyp | Ressource | Standort | Referenz | Lager: Wertmäßige Menge | Lager: Wertmäßiger Betrag | Lager: Gebuchte physische Menge | Lager: Gebuchter physischer Betrag | Lager: Menge | Lager: Betrag | Durchschnittliche Einheitskosten |
|---|---|---|---|---|---|---|---|---|---|---|
| Material | B0001 | 1 | Endsaldo | 9.00 | 900.00 | 5.00 | 375.00 | 14,00 | 1,275.00 | 91.07 |
| Material | B0001 | 2 | Endsaldo | 10.00 | 2,000.00 | 0,00 | 0,00 | 10.00 | 2,000.00 | 200.00 |

### <a name="example-3-when-the-transactions-level-is-used"></a>Beispiel 3 bei Verwendung der Buchungsebene

Die folgende Tabelle zeigt die Ergebnisse, wenn Sie die weiter oben in diesem Thema beschriebenen Beispieldaten verwenden, aber den Wert des Felds **Ebene** in der Berichtskonfiguration auf *Buchungen* ändern.

| Ressourcentyp | Ressource | Standort | Datum | Anzahl | Referenz | Lager: Wertmäßige Menge | Lager: Wertmäßiger Betrag | Lager: Gebuchte physische Menge | Lager: Gebuchter physischer Betrag | Lager: Menge | Lager: Betrag |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Material | B0001 | 1 | 15.03.2021 | 00000126 | Bestellung | 0,00 | 0,00 | 10.00 | 1,000.00 | 10.00 | 1,000.00 |
| Material | B0001 | 1 | 15.03.2021 | 00000126 | Bestellung | 10.00 | 1,000.00 | -10,00 | -1.000,00 | 0,00 | 0,00 |
| Material | B0001 | 1 | 15.04.2021 | 00000128 | Bestellung | 0,00 | 0,00 | 5.00 | 375.00 | 5.00 | 375.00 |
| Material | B0001 | 1 | 02.05.2021 | 000003 | Umlagerungsauftragslieferung | -5,00 | -458.33 | 0,00 | 0,00 | -5,00 | -458.33 |
| Material | B0001 | 1 | 02.05.2021 | 000003 | Umlagerungsauftragsempfang | 5.00 | 458.33 | 0,00 | 0,00 | 5.00 | 458.33 |
| Material | B0001 | 1 | 03.05.2021 | 000835 | Auftrag | 0,00 | 0,00 | -1,00 | -91.67 | -1,00 | -91.67 |
| Material | B0001 | 1 | 03.05.2021 | 000835 | Auftrag | -1,00 | -91.67 | 1.00 | 91.67 | 0,00 | 0,00 |
| Material | B0001 | 1 | 31.05.2021 | 000835 | Auftrag | 0,00 | -8,33 | 0,00 | 0,00 | 0,00 | -8,33 |
| Material | B0001 | 1 | 31.05.2021 | 000003 | Umlagerungsauftragslieferung | 0,00 | -41,67 | 0,00 | 0,00 | 0,00 | -41,67 |
| Material | B0001 | 1 | 31.05.2021 | 000003 | Umlagerungsauftragsempfang | 0,00 | 41.67 | 0,00 | 0,00 | 0,00 | 41.67 |
| Material | B0001 | 2 | 15.03.2021 | 00000127 | Bestellung | 0,00 | 0,00 | 10.00 | 2,000.00 | 10.00 | 2,000.00 |
| Material | B0001 | 2 | 15.03.2021 | 00000127 | Bestellung | 10.00 | 2,000.00 | -10,00 | -2,000,00 | 0,00 | 0,00 |
| Material | B0001 | 2 | 02.05.2021 | 000003 | Umlagerungsauftragslieferung | 5.00 | 458.33 | 0,00 | 0,00 | 5.00 | 458.33 |
| Material | B0001 | 2 | 02.05.2021 | 000003 | Umlagerungsauftragsempfang | -5,00 | -458.33 | 0,00 | 0,00 | -5,00 | -458.33 |
| Material | B0001 | 2 | 31.05.2021 | 000003 | Umlagerungsauftragslieferung | 0,00 | 41.67 | 0,00 | 0,00 | 0,00 | 41.67 |
| Material | B0001 | 2 | 31.05.2021 | 000003 | Umlagerungsauftragsempfang | 0,00 | -41,67 | 0,00 | 0,00 | 0,00 | -41,67 |
