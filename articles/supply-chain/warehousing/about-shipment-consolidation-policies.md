---
title: Lieferungskonsolidierungsrichtlinien
description: Dieses Thema bietet einen Überblick über die Funktionen, die eine flexible Konfiguration der Lieferungskonsolidierungsrichtlinien ermöglichen.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 4afa037ce9e446402128e4908a61ed32a30ebd59
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986949"
---
# <a name="shipment-consolidation-policies"></a>Lieferungskonsolidierungsrichtlinien

Der Lieferungskonsolidierungsprozess, der Richtlinien zur Lieferungskonsolidierung verwendet, ermöglicht eine automatisierte Lieferungskonsolidierung während der automatisierten und manuellen Freigabe an das Lager. Die automatisierte Konsolidierung, die vor Einführung dieser Funktion verfügbar war, hatte fest codierte Felder und basierte auf dem Feld **Lieferung bei Freigabe an Lagerort konsolidieren**-Feld, das für ein Lager festgelegt wurde.

Lieferungskonsolidierungsrichtlinien werden für die folgenden Funktionen verwendet:

- Der automatisierte Batchauftrag für die Freigabe an das Lager
- Der **Für Lagerort freigeben**-Befehl in einem Auftrag oder Transportauftrag
- Die dedizierte **Für Lagerort freigeben**-Seite
- Der **Für Lagerort freigeben**-Befehl auf der **Ladungsplanungsworkbench**-Seite
- Die manuelle Konsolidierung von Lieferungen auf den Seiten **Lieferungen konsolidieren** und **Lieferungskonsolidierungs-Workbench**

Vor der Einführung von Lieferungskonsolidierungsrichtlinien bestand die Konsolidierungsfunktion als Einstellung auf Lagerebene. Alle Bestellungen für alle Kunden aus einem einzigen Lager wurden so behandelt, als hätten sie die gleichen Konsolidierungsanforderungen. Richtlinien zur Lieferungskonsolidierung bieten Unterstützung für Szenarien, in denen verschiedene Organisationen unterschiedliche Anforderungen an die Lieferungskonsolidierung haben.

Abfragen werden verwendet, um die geltende Lieferungskonsolidierungsrichtlinie zu identifizieren. Anschließend kann anhand einer bearbeitbaren Reihe von Feldern festgelegt werden, wie die Ladezeilen auf Lieferungsebene gruppiert werden. (Dieses Muster ähnelt dem Muster, dem Wellenvorlagen folgen.) Außerdem wurde jeder Richtlinie eine **Mit bestehenden Lieferungen konsolidieren**-Option hinzugefügt. Wenn diese Option aktiviert ist, sucht das *Für Lagerort freigeben*-Verfahren Lieferungen zur Konsolidierung, indem es nach vorhandenen Lieferungen sucht, die auf der Grundlage derselben Konsolidierungsrichtlinie erstellt wurden. In diesem Fall wählt das System eine vorhandene Lieferung oder Ladung aus, anstatt eine neue zu erstellen. Das System wird jedoch nur mit vorhandenen Lieferungen konsolidiert, die den Status *Offen* haben; Lieferungen, die zu einer Wellenfreigabe mit dem Status *Veröffentlicht* oder höher gehören, werden nicht als Konsolidierungsziele angesehen.

Wenn Richtlinien zur Lieferungskonsolidierung verfügbar gemacht werden, wird die **Lieferung bei Freigabe an Lagerort konsolidieren**-Einstellung, die zuvor auf der **Lagerorte**-Einstellungsseite verfügbar war, ausgeblendet. Um Ihnen den Übergang zur neuen Versandkonsolidierungsfunktion zu erleichtern, erstellt eine Funktion auf der **Richtlinien zur Lieferungskonsolidierung**-Seite eine Standardrichtlinie, die automatisch die alte Einstellung für vorhandene Lager enthält. Nachdem diese Standardrichtlinie erstellt wurde, wird die **Lieferung bei Freigabe an Lagerort konsolidieren**-Einstellung auf der **Lagerorte**-Einstellungsseite nicht mehr berücksichtigt.

Sie können die Seite **Für Lagerort freigeben** verwenden, um die geltende Konsolidierungsrichtlinie manuell auf dieselbe Weise zu überschreiben, wie Sie Erfüllungsrichtlinien überschreiben können.

Sie können den Befehl **Freigeben \> Für Lagerort freigeben** auf der **Ladeplanungs-Workbench**-Seite zum Erstellen ausgehender Ladungen verwenden, die auf Kundenauftrags- und Überweisungsauftragspositionen basieren, bevor Sie die Freigabe an das Lager vornehmen. Diese Ladungen verwenden dieselbe Konsolidierungslogik, die zusammen mit der Konsolidierung der Versandrichtlinien eingeführt wurde.

Sie können die **Lieferungskonsolidierungs-Workbench**-Seite zum Konsolidieren vorhandener Lieferungen verwenden, die noch nicht bestätigt, aber bereits im Lager freigegeben wurden. Diese Funktion unterstützt Szenarien, in denen der automatisierte Freigabeprozess mit eigener Lieferungskonsolidierung mehrmals täglich ausgeführt wird. Potenzielle zusätzliche Konsolidierungen werden jedoch manuell identifiziert, bevor die Lieferung an Spediteure während des Bestätigungsprozesses abgeschlossen wird. Mit dieser Funktion können Sie ausgehende Lieferungen, die aus Kundenauftrags- oder Überweisungsauftragspositionen erstellt wurden, jederzeit konsolidieren, nachdem die Lieferungen an das Lager freigegeben wurden, aber bevor sie bestätigt wurden.

Das **Lieferungskonsolidierungs-Workbench**-Seite funktioniert wie die Ladungserstellungsworkbench, in der Sie mehrere Lieferungen gleichzeitig bewerten und einer bestimmten Lieferung einen nicht konsolidierten Auftrag zuweisen können. Sie können Lieferungskonsolidierungsvorlagen anwenden, um vorgeschlagene Konsolidierungen mehrmals zu bewerten und zu bestätigen. Einige Regeln werden implementiert, um eine unbefugte Konsolidierung zu verhindern und Sie vor möglichen Fehlern zu warnen.

## <a name="overview-of-new-functionality"></a>Übersicht über neue Funktionen

In diesem Abschnitt werden die Seiten, Befehle und Funktionen beschrieben, die beim Einschalten und Verwenden der Funktion *Richtlinien zur Lieferungskonsolidierung* geändert oder hinzugefügt werden.

### <a name="shipment-consolidation-policies-page"></a>Seite „Richtlinien zur Lieferungskonsolidierung“

Richtlinien werden nach Arbeitsauftragstyp unterschieden. Der **Aufträge**-Typ steht für _Auftrag_-Lieferungen und der **Umlagerungsaufträge**-Typ steht für _Übergangsabgang_-Lieferungen.

Jede Lieferungskonsolidierungsrichtlinie verfügt über eine Abfrage, die definiert, wann sie angewendet wird, und eine Sequenznummer, die die Ausführungsreihenfolge bestimmt. Die Konsolidierung wird für jede eindeutige Kombination der ausgewählten Felder angewendet. Ein zusätzlicher Parameter, der bereitgestellt wird, wird für die Konsolidierung mit vorhandenen (offenen) Lieferungen verwendet. Die Richtlinien werden jedes Mal ausgewertet und angewendet, wenn eine neue Lieferung erstellt wird (vor der Wellenverarbeitung).

Wenn in einer Richtlinie Pflichtfelder fehlen oder verbotene Felder enthalten sind, wird die Richtlinie in der Richtlinie im Abschnitt **Ausgewählt** als ungültig markiert. Die Listen der Pflichtfelder und der verbotenen Felder sind fest codiert und können erweitert werden.

Die folgende Liste zeigt die Pflichtfelder. Da Lieferungen immer basierend auf diesen Feldern aufgeteilt werden, können Sie nicht mehrere Lieferungen mit unterschiedlichen Werten für diese Felder gruppieren.

- Für Aufträge:

    - **Kontonummer:** _WHSShipmentTable.AccountNum_
    - **Lieferempfänger:** _WHSShipmentTable.DeliveryName_
    - **Postanschrift (RecId):** _WHSShipmentTable.DeliveryPostalAddress_
    - **Lagerort:** _WHSShipmentTable.InventLocationId_

- Für Umlagerungsaufträge:

    - **Von Lagerort:** _InventTransferTable.InventLocationIdFrom_
    - **Nach Lagerort:** _InventTransferTable.InventLocationIdTo_

Die folgenden Felder sind nicht für alle Dokumenttypen verfügbar. Diese Felder sind in der Benutzeroberfläche nicht sichtbar und können nicht für die Konsolidierung verwendet werden.

- **Lieferungs-ID:** _WHSShipmentTable.ShipmentId_
- **Status:** _WHSShipmentTable.ShipmentStatus_
- **Richtlinie für Lieferungskonsolidierung:** _WHSShipmentTable.ShipConsolidationPolicyName_
- **Arbeitstransaktionstyp:** _WHSShipmentTable.WorkTransType_
- **Wellenkennung:** _WHSShipmentTable.WaveId_
- **Ladungskennung:** _WHSShipmentTable.LoadId_
- **Lieferungs-ID:** _WHSLoadLine.ShipmentId_
- **Ladungskennung:** _WHSLoadLine.LoadId_

Wenn Sie eine Richtlinie erstellen, werden standardmäßig die obligatorischen Felder als Konsolidierungsfelder verwendet. Sie können die Liste jedoch mithilfe der Links- und Rechtspfeiltasten ändern. (Der Prozess ähnelt dem Prozess zum Auswählen von Methoden in Wellenvorlagen.)

Die Werte, die Benutzer für diese Felder auswählen, werden für alle neu erstellten Lieferungen verwendet oder während der Konsolidierung mit diesen Lieferungen zu vorhandenen Lieferungen hinzugefügt. Wenn zwei Lieferungen für ein Feld, das für die Konsolidierung dieser Lieferungen ausgewählt wurde, denselben Wert haben, werden die Lieferungen konsolidiert. Das gleiche Prinzip gilt für alle nachfolgenden Konsolidierungsfelder, die ausgewählt werden. Wenn sich die Werte unterscheiden, wird die zweite Lieferung verworfen und für eine neue Lieferung ausgewählt. Der automatisierte Konsolidierungsprozess besteht darin, alle eindeutigen Wertekombinationen für die Lieferungskonsolidierungsfelder zu erstellen und dann der entsprechenden Kombination eine Lieferung zuzuweisen.

Nicht ausgewählte Felder werden während des Konsolidierungsprozesses ignoriert. Wenn zwei Lieferungen unterschiedliche Werte für ein nicht ausgewähltes Feld haben, wird das Feld gelöscht (d. h., es ist leer). Wenn beide Lieferungen für ein nicht ausgewähltes Feld den gleichen Wert haben, wird das Feld ausgefüllt.

Die Liste der Konsolidierungsfelder (d. h. der Felder, die gelöscht werden, wenn sie unterschiedliche Werte haben) ist fest codiert. Die Liste enthält alle Felder, die aus einem Kundenauftrag oder einer Transportauftragsposition initialisiert werden, wenn eine neue Lieferung erstellt wird. Mit anderen Worten, wenn ein Feld nicht aus einem Kundenauftrag oder einer Transportauftragsposition initialisiert wird, wird es ignoriert, wenn einer vorhandenen Lieferung neue Daten hinzugefügt werden.

### <a name="release-to-warehouse-page"></a>Auf Lagerseite freigeben

- Ein neues Feld im unteren Raster zeigt die angewandte Konsolidierungsrichtlinie.
- Mit einer neuen Schaltfläche können Sie die Konsolidierungsrichtlinie manuell auswählen und/oder überschreiben.

### <a name="release-to-warehouse-command-on-the-load-planning-workbench-page"></a>Für Lagerort freigeben-Befehl auf der Ladungsplanungsworkbench-Seite

- Die Logik wurde so angepasst, dass angewandte Konsolidierungsrichtlinien verwendet werden.
- Lieferungen werden jetzt nur noch innerhalb einer einzigen Ladung konsolidiert.

### <a name="consolidate-shipments-page"></a>Lieferungen konsolidieren-Seite

- Die Suche nach ähnlichen Lieferungen (d. h. nach Kandidaten für die Konsolidierung) wurde geändert, sodass Felder verwendet werden, die in der Versandkonsolidierungsrichtlinie ausgewählt sind.
- Felder mit unterschiedlichen Werten in unterschiedlichen Lieferungen sind jetzt leer. (Bisher wurden die Werte aus der ausgewählten „Basis“-Lieferung verwendet.)

### <a name="shipment-consolidation-workbench-page"></a>Seite „Lieferungskonsolidierungs-Workbench“

- Neue Funktionen replizieren den Prozess der manuellen Konsolidierung in größerem Maßstab.
- Sie können diese Seite jetzt über das Menü **An Lager freigeben** im Modul **Lagerverwaltung** öffnen.
- Der Algorithmus analysiert vorhandene Lieferungen, die noch nicht versendet wurden. Anschließend wird eine Konsolidierung vorgeschlagen, die auf Feldern basiert, die in den Konsolidierungsrichtlinien ausgewählt sind.

## <a name="comparison-of-functionality"></a>Funktionsvergleich

In der folgenden Tabelle wird zusammengefasst, wie die Lieferungskonsolidierung funktioniert, wenn Sie keine Richtlinien zur Lieferungskonsolidierung verwenden und wenn Sie diese verwenden.

| Ohne Richtlinien zur Lieferungskonsolidierung | Mit Richtlinien zur Lieferungskonsolidierung |
|---|----|
| Nicht zutreffend | Verkaufs- oder Transferlieferungen, die für die Konsolidierung ausgewählt wurden, müssen dieselbe Konsolidierungsrichtlinie haben wie die Lieferung, die erstellt wird, oder sie müssen einer offenen Lieferung zugeordnet sein (wenn die **Mit bestehenden Lieferungen konsolidieren**-Option aktiviert ist). |
| Das *An Lager freigeben*-Verfahren sucht nicht zwischen vorhandenen Lieferungen, um eine Lieferung zur Konsolidierung zu finden. Nur Lieferungen, die von einer aktuellen Instanz des *An Lager freigeben*-Verfahrens erstellt wurden, werden verwendet, um eine Lieferung für die Konsolidierung zu finden. | Wenn die **Mit bestehenden Lieferungen konsolidieren**-Option ist für eine Konsolidierungsrichtlinie aktiviert ist, die derzeit verwendet wird, sucht das *An Lager freigeben*-Verfahren unter vorhandenen Lieferungen, die auf der Grundlage derselben Konsolidierungsrichtlinie erstellt wurden, um eine Lieferung zur Konsolidierung zu finden. Wenn Sie also zwei Richtlinien haben, wird eine Lieferung, die auf der Grundlage von Richtlinie 2 erstellt wird, niemals mit einer Lieferung konsolidiert, die auf der Grundlage von Richtlinie 1 erstellt wurde. |
| Nicht zutreffend | Wenn eine Liste der Konsolidierungsrichtlinienfelder leer ist oder eine Richtlinie nicht gefunden werden kann, wird für jeden Kundenauftrag oder jede Überweisungsauftragsposition eine neue Lieferung erstellt. |
| Das folgende Konsolidierungsfeld definiert die eindeutige Wertekombination, die zum Konsolidieren von Lieferungen für eine *Umlagerungsposition* verwendet wird. (Alle anderen Felder werden ignoriert.)<ul><li>Auftragsnummer (OrderNum)</li></ul> | Die folgenden Konsolidierungsfelder definieren die eindeutige Wertekombination, die zum Konsolidieren von Lieferungen für eine *Umlagerungsposition* verwendet wird. (Alle anderen Felder werden ignoriert.)<ul><li>Auftragsnummer (OrderNum)</li><li>Lieferempfänger (DeliveryName)</li><li>Postanschrift (DeliveryPostalAddress)</li><li>ISO-Ländercode (CountryRegionISOCode)</li><li>Adresse (Address)</li><li>Website (InventSiteId)</li><li>Lagerort (InventLocationId)</li><li>Spediteur (CarrierCode)</li><li>Spediteurdienstleistung (CarrierServiceCode)</li><li>Lieferart (ModeCode)</li><li>Spediteurgruppe (CarrierGroupCode)</li><li>Lieferbedingungen (DlvTermId)</li></ul>Diese Felder sind die einzigen Felder, die verfügbar und initialisiert sind, wenn eine neue Lieferung erstellt wird. |
| Die folgenden Konsolidierungsfelder definieren die eindeutige Wertekombination, die zum Konsolidieren von Lieferungen für eine *Verkaufsposition* verwendet wird. (Alle anderen Felder werden ignoriert.)<ul><li>Auftragsnummer (OrderNum)</li><li>Debitorenreferenz (CustomerRef)</li><li>Debitorenanforderung (CustomerReq)</li><li>Lieferbedingungen (DlvTermId)</li></ul> | Die folgenden Konsolidierungsfelder definieren die eindeutige Wertekombination, die zum Konsolidieren von Lieferungen für eine *Verkaufsposition* verwendet wird. (Alle anderen Felder werden ignoriert.)<ul><li>Auftragsnummer (OrderNum)</li><li>Kontonummer (AccountNum)</li><li>Lieferempfänger (DeliveryName)</li><li>Postanschrift (DeliveryPostalAddress)</li><li>ISO-Ländercode (CountryRegionISOCode)</li><li>Adresse (Address)</li><li>Website (InventSiteId)</li><li>Lagerort (InventLocationId)</li><li>Spediteur (CarrierCode)</li><li>Spediteurdienstleistung (CarrierServiceCode)</li><li>Lieferart (ModeCode)</li><li>Spediteurgruppe (CarrierGroupCode)</li><li>Brokerkennung (BrokerCode)</li><li>Richtung (LoadDirection)</li><li>Lieferbedingungen (DlvTermId)</li><li>Debitorenreferenz (CustomerRef)</li><li>Debitorenanforderung (CustomerReq)</li></ul>Diese Felder sind die einzigen Felder, die verfügbar und initialisiert sind, wenn eine neue Lieferung erstellt wird. |
| Nicht zutreffend | Die folgenden Konsolidierungsfelder sind für eine *Verkaufsposition* obligatorisch und können nicht entfernt werden:<ul><li>Kontonummer (AccountNum)</li><li>Lieferempfänger (DeliveryName)</li><li>Postanschrift (DeliveryPostalAddress)</li><li>Lagerort (InventLocationId)</li></ul>Standardmäßig werden diese Felder zugewiesen, wenn eine neue Richtlinie erstellt wird. Sie können nicht entfernt werden. |
| Das *Ladungen für Lagerort freigeben*-Verfahren auf der **Ladungsplanungs-Workbench**-Seite verwendet einen eigenen Code, um Lieferungen und Wellen zu erstellen. | Lieferungskonsolidierungsrichtlinien werden angewendet, um zu bestimmen, welche Felder für die Konsolidierung ausgewertet werden sollen. Lieferungen werden jetzt nur noch innerhalb einer einzigen Ladung konsolidiert. |
| Sie wählen **Lieferungen konsolidieren** auf der **Alle Lieferungen**-Seite manuell aus und wählen dann eine Ziel-„Basis“-Lieferung. Der Filter schlägt alle vorhandenen Lieferungen vor, deren Werte für mehrere Schlüsselfelder übereinstimmen. | Sie wählen **Lieferungen konsolidieren** auf der **Alle Lieferungen**-Seite manuell aus und wählen dann eine Ziel-„Basis“-Lieferung. Das System schlägt andere vorhandene Lieferungen vor, indem es die Werte mehrerer Schlüsselfelder abgleichen, die für die entsprechenden Richtlinien zur Lieferungskonsolidierung konfiguriert sind. |
| Sie können **Lieferungen konsolidieren**-Befehl auf der **Alle Lieferungen**-Seite für nur eine Lieferung verwenden. | Auf der **Lieferungskonsolidierungs-Workbench**-Seite finden Sie eine Reihe von Lieferungen, die sich noch nicht im Versandzustand befinden. Diese Lieferungen werden anhand mehrerer Schlüsselfelder analysiert, die in Ihren Lieferungskonsolidierungsrichtlinien konfiguriert sind. Alle Lieferungen, bei denen die Werte dieser Felder übereinstimmen, werden zur Konsolidierung vorgeschlagen.<p>Sie können die Konsolidierung manuell verwalten, indem Sie Lieferungen aus vorgeschlagenen Konsolidierungen entfernen und/oder ihnen Lieferungen hinzufügen. Es können verschiedene Arten von Fehlern auftreten, von denen Sie jedoch einige überschreiben können.</p> |
| **Entwurfshinweis:** Das *Automatische Freigabe von Aufträgen an das Lager*-Verfahren teilt Verkaufspositionen in Gruppen auf. Jede Gruppe hat ihren eigenen **ReleaseToWarehouseId**-Wert und wird separat vom *An Lager freigeben*-Verfahren verarbeitet. Diese Prozedur erstellt neue Arbeit unabhängig von der Einrichtung der Arbeitspause. | **Entwurfshinweis:** Das *Automatische Freigabe von Aufträgen an das Lager*-Verfahren weist den gleichen **ReleaseToWarehouseId**-Wert für alle Verkaufspositionen zu, die verarbeitet werden. Alle Verkaufspositionen werden vom *An Lager freigeben*-Verfahren zur gleichen Zeit verarbeitet. Um das frühere Verhalten sicherzustellen, müssen Sie die Arbeitspause pro Lieferungs-ID konfigurieren. |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Richtlinien zur Lieferungskonsolidierung konfigurieren](configure-shipment-consolidation-policies.md)