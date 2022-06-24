---
title: Lagerbuchungsdetails
description: Dieser Artikel bietet einen Überblick über die Buchungsdetails-Seite, auf der Details einer ausgewählten Lagerbuchung angezeigt werden.
author: rachel-profitt
ms.date: 04/25/2022
ms.topic: article
ms.search.form: InventTrans, InventTransDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-04-25
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 55e29d5804f57cd86fb5ddac5d6c5576b7ea5f61
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859386"
---
# <a name="inventory-transaction-details"></a>Lagerbuchungsdetails

Verwenden Sie die **Buchungsdetails**-Seite, um Details zu ausgewählten Lagerbuchungen anzuzeigen.

## <a name="open-the-transaction-details-page"></a>Buchungsdetails-Seite öffnen

Führen Sie die folgenden Schritte aus, um die Seite **Buchungsdetails** zu öffnen.

1. Wechseln Sie zu **Lagerverwaltung \> Abfragen und Berichte \> Buchungen**.
1. Wählen Sie die Buchung aus, die Sie überprüfen möchten.
1. Wählen Sie im Aktivitätsbereich **Buchungsdetails** aus.

## <a name="fasttabs-overview"></a>Inforegisterübersicht

Die Seite **Buchungsdetails** ist in mehrere Inforegister aufgeteilt. Die folgende Tabelle beschreibt den Zweck der einzelnen Inforegister.

| Inforegister | Description |
|---|---|
| Allgemeines | Dieses Inforegister zeigt grundlegende Informationen über die ausgewählte Lagerbuchung. Zusätzlich zu den Feldern, die auf der Seite **Lagerbuchungen** angezeigt werden, enthält sie die zusätzlichen Felder, die weiter unten in diesem Artikel beschrieben werden. |
| Aktualisierungen | Dieses Inforegister zeigt Informationen an, die sich auf die physischen, finanziellen und Abrechnungsaspekte der ausgewählten Lagerbuchung beziehen. Je nach aktuellem Status der Buchung können einige Felder leer sein. Diese Felder werden jedoch automatisch festgelegt, wenn Transaktionen gebucht werden. Zusätzlich zu den Feldern, die auf der Seite **Lagerbuchungen** angezeigt werden, enthält dieses Inforegister die zusätzlichen Felder, die weiter unten in diesem Artikel beschrieben werden. |
| Sachkontobuchungen | Dieses Inforegister zeigt den Buchungstyp und das Sachkonto, die für die physische Aktualisierung, Finanzaktualisierung, für physische Umsatzerlöse, physische Belastungen, Finanzerträge und Finanzbelastungen verwendet werden, die sich auf die ausgewählte Lagerbuchung beziehen. |
| Referenzen | Dieses Inforegister zeigt zusätzliche Informationen über die Quellbuchung, die die ausgewählte Lagerbuchung erstellt hat. Diese Informationen können beispielsweise Details aus der Bestellung oder dem Auftrag enthalten. |
| Zugehörige Informationen | Dieses Inforegister zeigt zusätzliche Informationen über die ausgewählte Lagerbuchung. Diese Felder werden möglicherweise nicht festgelegt, wenn Sie einige Funktionen nicht verwenden, z. B. Beschaffungskategorien oder Projekte. |
| Finanzdimensionen – Physisch | Dieses Inforegister zeigt die Finanzdimensionswerte an, die verwendet wurden, als die physische Aktualisierung gebucht wurde. Wenn die physische Aktualisierung nicht gepostet wurde, sind die Felder leer. |
| Finanzdimensionen – Finanzen | Dieses Inforegister zeigt die Finanzdimensionswerte an, die verwendet wurden, als die Finanzaktualisierung gebucht wurde. Wenn die Finanzaktualisierung nicht gepostet wurde, sind die Felder leer. |
| Lagerungsdimensionen | Dieses Inforegister zeigt die Lagerungsdimensionswerte an, die der ausgewählten Lagerbuchung zugewiesen sind. Zu den Werten zählen Site, Lagerhaus, Größe, Farbe, Konfiguration, Standort, Chargennummer, Seriennummer, Bestandsstatus, Ladungsträger und Besitzer. |

## <a name="fields-on-the-general-fasttab"></a>Felder auf dem Inforegister „Allgemein“

Die folgende Tabelle beschreibt die Felder auf dem Inforegister **Allgemein**, die nicht auch auf der **Lagerbuchungen**-Seite angezeigt werden.

| Feld | Description |
|---|---|
| Partei | Der Name der relevanten Partei für die ausgewählte Lagerbuchung. Beispielsweise zeigt eine Bestellbuchung den Namen des Lieferanten auf der Bestellung und eine Auftragsbuchung den Namen des Kunden. Dieses Feld ist nicht für alle Typen von Lagerbuchungen verfügbar. |
| Lagerreferenz | Wenn eine andere Lagerbuchung mit der ausgewählten Lagerbuchung verknüpft ist, der Typ dieser anderen Buchung. Wenn z. B. eine Bestellung für einen Auftrag markiert ist, wird das Feld **Lagerreferenz** der Bestellbuchung auf *Auftrag* festgelegt. Die Kennzeichnung erfolgt automatisch für Direktlieferaufträge und Intercompany-Aufträge. Wenn Sie die Markierung mit anderen Nachkalkulationsmethoden als *Standardkosten* und *gleitender Durchschnitt* verwenden, erstellt das System Abrechnungen und Anpassungen für genau die markierten Buchungen. Auf diese Weise erreichen Sie eine „Ist“-Kalkulation, die die Logik für FIFO (First In, First Out), LIFO (Last In, First Out) oder gewichteten Durchschnitt außer Kraft setzt. |
| Lagernummer | Die spezifische Buchung, die sich auf die ausgewählte Lagerbuchung bezieht. Wenn z. B. eine Bestellung für einen Auftrag markiert ist, wird das Feld **Lagernummer** der Bestellbuchung auf die Auftragsnummer festgelegt. |
| Projektkennung | Wenn sich die ausgewählte Lagerbuchung auf ein Projekt bezieht, wird dieses Feld auf die Projektnummer gesetzt. |
| Loskennung | Die eindeutige Los-ID, die das System der ausgewählten Lagerbuchung zugewiesen hat. |
| Los-Referenz | Wenn eine andere Lagerbuchung mit der ausgewählten Lagerbuchung verknüpft ist, die Los-ID dieser anderen Buchung. Wenn z. B. eine Bestellung für einen Auftrag markiert ist, wird das Feld **Los-Referenz** der Bestellbuchung der **Los-ID**-Wert der Lagerbuchung der Auftragsposition. |
| Dimensionsnummer | Eine eindeutige ID, die die Kombination aller Lagerungsdimensionswerte darstellt, die der ausgewählten Lagerbuchung zugewiesen sind. |
| Offener Wert | Ein Wert, der angibt, ob die ausgewählte Lagerbuchung durch den Lagerabschlussprozess ausgeglichen wurde. Ist dieses Feld auf *Ja* festgelegt, wurde die Buchung nicht ausgeglichen. |
| Erwartetes Datum | Bei Zugangsbuchungen das Datum, an dem der Lagerzugang erwartet wird. Dieses Feld kann beispielsweise das erwartete Eingangsdatum auf einem Bestandssperrauftrag oder das Lieferdatum auf einer Bestellposition anzeigen. |
| Inventurdatum | Dieses Feld wird gesetzt, wenn eine Registrierungsbuchung für den Eingangsauftrag durchgeführt wurde, bevor ein physischer Zugang gebucht wurde. |
| Nicht wertmäßige Umlagerung | Ein Wert, der angibt, ob die ausgewählte Lagerbuchung eine nicht wertmäßige Umlagerung ist. Eine nicht wertmäßige Umlagerung erfolgt, wenn eine Änderung der Lagerungsdimensionen auf der Seite **Lagersteuerungsgruppe** nicht wertmäßig nachverfolgt wird. |
| Umlagerungsloskennung | Wenn es sich bei der ausgewählten Lagerbuchung um eine nicht wertmäßige Umlagerung handelt, wird dieses Feld auf den **Los-ID**-Wert der anderen Lagerbuchung festgelegt, mit der die ausgewählte Buchung abgerechnet wird. |

## <a name="fields-on-the-updates-fasttab"></a>Felder auf dem Inforegister „Aktualisierungen“

Die folgende Tabelle beschreibt die Felder auf dem Inforegister **Aktualisierungen**, die nicht auch auf der **Lagerbuchungen**-Seite angezeigt werden.

| Feld | Description |
|---|---|
| Physischer Beleg | Die Belegnummer aus dem Hauptbuch, in dem die physische Buchung für die ausgewählte Lagerbuchung generiert wurde. |
| Route | Der Arbeitsplan, der sich auf die ausgewählte Lagerbuchung bezieht. Dieses Feld wird nur für Produktionskommissionierlisten-Buchungen festgelegt, bei denen die Kommissionierliste (Bill of Materials, BOM) oder die Formelposition mit einem bestimmten Artikel verknüpft ist. |
| Lieferschein | Die Lieferscheinnummer, die für eine Bestellungs-Produktzugangsbuchung eingegeben wurde. |
| Phys. Einstandsbetrag | Der Betrag, der in das Hauptbuch für die physische Aktualisierung gebucht wurde. Bei einem Produkt mit Standardkosten stellt dieser Betrag die Standardkosten dar. Bei anderen Nachkalkulationsmethoden stellt es den gewichteten Durchschnitt für das Produkt zum Zeitpunkt der Buchung dar. |
| Physischer Umsatzerlös | Der Betrag des verzögerten Umsatzerlöses, der in das Hauptbuch für die physische Aktualisierung gebucht wurde. |
| Ladungskennung | Wenn sich die aktuelle Buchung auf eine Ladung in der Transportverwaltung bezieht, zeigt dieses Feld die eindeutige Nummer der Ladung, die den Artikel enthielt. |
| Physisch gebucht | Ein Wert, der angibt, ob die ausgewählte Lagerbuchung physisch gebucht wurde. Wenn die aktuelle Transaktion in das Hauptbuch gebucht wird, gibt es auch einen physischen Beleg. |
| Wertmäßig gebucht | Ein Wert, der angibt, ob die ausgewählte Lagerbuchung wertmäßig gebucht wurde. Wenn die aktuelle Transaktion in das Hauptbuch gebucht wird, gibt es auch einen Finanzbeleg. |
| Physische Belastung gebucht | Ein Wert, der angibt, ob die physischen Belastungen, die sich auf die ausgewählte Lagerbuchung beziehen, gebucht wurden. |
| Finanzielle Belastung gebucht | Ein Wert, der angibt, ob die Finanzbelastungen, die sich auf die ausgewählte Lagerbuchung beziehen, gebucht wurden. |
| Finanzbeleg | Die Belegnummer im Hauptbuch, wo die Finanzbuchung generiert wurde. |
| Rechnung | Die Rechnungsnummer, die beispielsweise für eine Bestellung oder einen Auftrag generiert wurde. |
| Regulierung | Der Betrag, der bei der ausgewählten Lagerbuchung aus dem Lagerabschluss- und Anpassungsprozess angepasst wurde. |
| Gewinn und Verlust, gebuchter Betrag | Der Betrag der ausgewählten Lagerbuchung, der in der Gewinn- und Verlustrechnung gebucht wurde. |
| Ungebuchte Rechnung | Die Rechnungsnummer einer zugehörigen Bestellung, die auf der Seite **Ausstehende Kreditorenrechnung** angezeigt wird. |
| Wertmäßig abgeschlossen | Das Datum, an dem die Buchung vollständig ausgeglichen wurde. |
| Abgedeckte CW-Menge | Die Artikelgewichtsmenge, die von dem Ausgleich abgedeckt wird. |
| Ausgeglichene Menge | Die Menge, die für die ausgewählte Lagerbuchung ausgeglichen wurde. |
| Ausgleichsbetrag | Der Wert, der für die ausgewählte Lagerbuchung ausgeglichen wurde. |
