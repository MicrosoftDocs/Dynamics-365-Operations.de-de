---
title: Qualitätszuordnungen
description: Dieses Thema beschreibt, wie Sie Qualitätsprüfungsaufträge in Microsoft Dynamics 365 Supply Chain Management verwenden können, um automatisch Qualitätsprüfungsaufträge zu generieren, die mit Ihren Verkaufs-, Einkaufs- und Produktionsprozessen zusammenhängen.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2020-06-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f46f09dc9b67cfb04d0320a071c2c739266af58
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956666"
---
# <a name="quality-associations"></a>Qualitätszuordnungen

[!include [banner](../includes/banner.md)]

Dieses Thema beschreibt, wie Sie Qualitätsprüfungsaufträge in Microsoft Dynamics 365 Supply Chain Management verwenden können, um automatisch Qualitätsprüfungsaufträge zu generieren, die mit Ihren Verkaufs-, Einkaufs- und Produktionsprozessen zusammenhängen.

Eine Qualitätszuordnung definiert alle folgenden Informationen für einen erzeugten Qualitätsprüfungsauftrag:

- Das Buchungsereignis
- Die Tests, die für die Artikel ausgeführt werden müssen.
- Die akzeptable Qualitätsstufe (AQL)
- Den Musteraufnahmeplan

Sie müssen eine Qualitätszuordnung für jede Variante in einem Geschäftsprozess definieren, die eine automatische Generierung eines Qualitätsprüfungsauftrags erfordert. So kann ein Qualitätsprüfungsauftrag beispielsweise in Geschäftsprozessen für Bestellungen, Quarantäneaufträge, Aufträge und Produktionsaufträge generiert werden.

## <a name="working-with-quality-associations"></a>Arbeiten mit Qualitätszuordnungen

Der Geschäftsprozess, der eine Qualitätszuordnung verwendet, kann sich auf verschiedene Quelldokumente beziehen (z. B. Bestellungen, Aufträge oder Produktionsaufträge).

Jeder Qualitätszuordnungsdatensatz definiert den Testsatz, das akzeptable Qualitätsniveau (AQL) und den Musteraufnahmeplan, der für die Qualitätsprüfungsaufträge gilt, die generiert werden. Sie müssen einen Qualitätszuordnungsdatensatz für jede Variante in einem Geschäftsprozess definieren. So können Sie beispielsweise eine Qualitätszuordnung einrichten, die einen Qualitätsprüfungsauftrag generiert, wenn ein Produktzugang für Bestellungen aktualisiert wird. Je nach Einrichten des Ausführungsplans kann der auslösende Prozess selbst blockiert werden, während ein offener Qualitätsprüfungsauftrag vorliegt. Alternativ können nachfolgende Prozesse, wie z.B. die Rechnungsstellung für den Kauf, blockiert werden.

> [!NOTE]
> Solange es offene Qualitätsprüfungsaufträge gibt, werden Bestandsmengen automatisch für die Ausgabe gesperrt. Abhängig von der Einstellung des Felds **Vollsperrung** auf der Seite **Artikelmusteraufnahme** ist die Menge entweder die Menge auf dem Qualitätsprüfungsauftrag oder die Menge auf der Quelldokumentzeile. Weitere Informationen finden Sie unter [Qualitätsmanagement Artikelmusteraufnahme](quality-item-sampling.md).

Für einen bestimmten Geschäftsprozess identifiziert der Datensatz für die Qualitätszuordnung das Ereignis und die Bedingungen, für die ein Qualitätsprüfungsauftrag erzeugt wird. Die Bedingungen können entweder für einen Standort oder für eine juristische Person spezifisch sein. Ein Qualitätsprüfungsauftrag mit Zerstörungstests kann nur ausgeführt werden, wenn am Lager Artikel für das Ereignis vorhanden sind.

Um mit Qualitätsverbänden zu arbeiten, gehen Sie zu **Bestandsmanagement \> Einrichten \> Qualitätskontrolle \> Qualitätsverbände**. Die folgenden Beispiele zeigen, wie ein Datensatz für die Qualitätszuordnung für die Variationen in jedem Geschäftsprozess definiert wird. Für jedes Beispiel sind zudem in der folgenden Tabelle die Ereignisse und Bedingungen zusammengefasst, die durch einen Qualitätszuordnungsdatensatz definiert werden.

<table>
<thead>
<tr>
<th>Referenztyp</th>
<th>Ereignistyp</th>
<th>Ausführung</th>
<th>Ereignissperrung</th>
<th>Dokumentreferenz</th>
</tr>
</thead>
<tbody>
<tr>
<td>Bestand</td>
<td>Nicht zutreffend</td>
<td>Nicht zutreffend</td>
<td>Keine</td>
<td>Alle</td>
</tr>
<tr>
<td rowspan="7">Verk.</td>
<td rowspan="4">Entnahmeprozess wurde geplant</td>
<td rowspan="4">Vor</td>
<td>Keine</td>
<td rowspan="22">Spezifische Kennung, Gruppe oder Alle.</td>
</tr>
<tr>
<td>Entnahmeprozess</td>
</tr>
<tr>
<td>Lieferschein</td>
</tr>
<tr>
<td>Rechnung</td>
</tr>
<tr>
<td rowspan="3">Lieferschein</td>
<td rowspan="3">Vor</td>
<td>Keine</td>
</tr>
<tr>
<td>Lieferschein</td>
</tr>
<tr>
<td>Rechnung</td>
</tr>
<tr>
<td rowspan="15">Einkauf</td>
<td rowspan="7">Zugangsliste</td>
<td rowspan="4">Vor</td>
<td>Keine</td>
</tr>
<tr>
<td>Zugangsliste</td>
</tr>
<tr>
<td>Produktzugang</td>
</tr>
<tr>
<td>Rechnung</td>
</tr>
<tr>
<td rowspan="3">Nach</td>
<td>Keine</td>
</tr>
<tr>
<td>Produktzugang</td>
</tr>
<tr>
<td>Rechnung</td>
</tr>
<tr>
<td rowspan="3">Umsatzsteuernummer</td>
<td rowspan="3">Nicht zutreffend</td>
<td>Keine</td>
</tr>
<tr>
<td>Produktzugang</td>
</tr>
<tr>
<td>Rechnung</td>
</tr>
<tr>
<td rowspan="5">Produktzugang</td>
<td rowspan="3">Vor</td>
<td>Keine</td>
</tr>
<tr>
<td>Produktzugang</td>
</tr>
<tr>
<td>Rechnung</td>
</tr>
<tr>
<td rowspan="2">Nach</td>
<td>Keine</td>
</tr>
<tr>
<td>Rechnung</td>
</tr>
<tr>
<td rowspan="8">Produktion</td>
<td rowspan="3">Umsatzsteuernummer</td>
<td rowspan="3">Nicht zutreffend</td>
<td>Keine</td>
<td rowspan="12">Alle</td>
</tr>
<tr>
<td>Fertigmeldung</td>
</tr>
<tr>
<td>Beenden</td>
</tr>
<tr>
<td rowspan="5">Fertigmeldung</td>
<td rowspan="3">Vor</td>
<td>Keine</td>
</tr>
<tr>
<td>Fertigmeldung</td>
</tr>
<tr>
<td>Beenden</td>
</tr>
<tr>
<td rowspan="2">Nach</td>
<td>Keine</td>
</tr>
<tr>
<td>Beenden</td>
</tr>
<tr>
<td rowspan="4">Quarantäne</td>
<td rowspan="3">Fertigmeldung</td>
<td rowspan="2">Vor</td>
<td>Fertigmeldung</td>
</tr>
<tr>
<td>Beenden</td>
</tr>
<tr>
<td>Nach</td>
<td>Beenden</td>
</tr>
<tr>
<td>Beenden</td>
<td>Vor</td>
<td>Beenden</td>
</tr>
<tr>
<td rowspan="3">Arbeitsplan-Arbeitsgang</td>
<td rowspan="3">Fertigmeldung</td>
<td rowspan="2">Vorher</td>
<td>Keines</td>
<td rowspan="3">Spezifische ID, Gruppe oder Alle und spezifische Ressource, Gruppe oder Alle</td>
</tr>
<tr>
<td>Fertigmeldung</td>
</tr>
<tr>
<td>Später</td>
<td>Keines</td>
</tr>
<tr>
<td rowspan="3">Kuppelprodukt - Produktion</td>
<td>Umsatzsteuernummer</td>
<td>Nicht zutreffend</td>
<td rowspan="3">Keines</td>
<td rowspan="3">Alle</td>
</tr>
<tr>
<td rowspan="2">Fertigmeldung</td>
<td>Vorher</td>
</tr>
<tr>
<td>Später</td>
</tr>
</tbody>
</table>

> [!NOTE]
> Die Funktion *Qualitätsmanagement für Lagerorte* fügt Funktionalitäten für die Verarbeitung von Qualitätsprüfungsaufträgen für die Produktion hinzu, bei denen das Feld **Ereignistyp** auf *Bericht als fertig* und das Feld **Ausführung** auf *Nach* festgelegt ist, und für den Kauf, bei dem das Feld **Ereignistyp** auf *Registrierung* festgelegt ist. Weitere Informationen finden Sie unter [Qualitätsmanagement für Lagerortprozesse](quality-management-for-warehouses-processes.md).

Die folgende Tabelle enthält weitere Informationen darüber, wie Qualitätsprüfungsaufträge für bestimmte Arten von Prozessen generiert werden können.

<div class="tableSection">
<table>
<thead>
<tr>
<th>Prozesstypen</th>
<th>Wenn Qualitätsprüfungsaufträge automatisch generiert werden können</th>
<th>Wenn Qualitätsprüfungsaufträge generiert werden können, wenn Zerstörungstest erforderlich ist</th>
<th>Bedingungsinformationen</th>
<th>Manuelle Generierungsinformationen</th>
</tr>
</thead>
<tbody>
<tr>
<td>Bestellung</td>
<td>Bevor oder nachdem eine Zugangsliste oder ein Produktzugang für das erhaltene Material gebucht wird</td>
<td>Nachdem der Produktzugang für das Material, das erhalten wurde, gebucht wurde, da das Material für Zerstörungstest verfügbar sein muss</td>
<td>Der Bedarf für einen Qualitätsprüfungsauftrag kann einen bestimmten Betrieb, ein Element oder einen Kreditor oder eine Kombination dieser Bedingungen widerspiegeln.</td>
<td>Ein manuell generierter Qualitätsprüfungsauftrag, der sich auf eine Bestellung bezieht, kann Informationen in einem Qualitätszuordnungsdatensatz, wie dem Testmusteraufnahmeplan, verwenden.</td>
</tr>
<tr>
<td>Quarantäneauftrag</td>
<td>Bevor oder nachdem der Quarantäneauftrag als fertig oder abgeschlossen gemeldet wird</td>
<td>Qualitätsprüfungsaufträge, die zerstörende Tests erfordern, können nicht erstellt werden. Es wird davon ausgegangen, dass die Funktionalität des Quarantäneauftrags die Disposition des zerstörten Materials übernimmt.</td>
<td>Der Bedarf für einen Qualitätsprüfungsauftrag kann einen bestimmten Betrieb, ein Element oder einen Kreditor oder eine Kombination dieser Bedingungen widerspiegeln.</td>
<td>Ein manuell generierter Qualitätsprüfungsauftrag, der sich auf eine Quarantänebestellung bezieht, kann Informationen in einem Qualitätszuordnungsdatensatz, wie dem Testmusteraufnahmeplan, verwenden.</td>
</tr>
<tr>
<td>Auftrag</td>
<td>Vor eine geplanter Entnahmevorgang oder eine Lieferscheinaktualisierung für die zu liefernden Artikel</td>
<td>Bei einem beliebigen Schritt</td>
<td>Die Anforderung für einen Qualitätsprüfungsauftrag kann einen bestimmten Standort, ein Element oder einen Debitor oder eine Kombination dieser Bedingungen widerspiegeln.</td>
<td>Ein manuell generierter Qualitätsprüfungsauftrag, der sich auf einen Auftrag bezieht, kann Informationen in einem Qualitätszuordnungsdatensatz, wie dem Testmusteraufnahmeplan, verwenden.</td>
</tr>
<tr>
<td>Produktionsauftrag</td>
<td>Bevor oder nachdem die fertig gestellte Menge für den Produktionsauftrag gemeldet wird</td>
<td>Nachdem die fertig gestellte Menge für den Produktionsauftrag gemeldet wird</td>
<td>Die Anforderung für einen Qualitätsprüfungsauftrag kann einen bestimmten Betrieb oder ein Element oder eine Kombination dieser Bedingungen widerspiegeln.</td>
<td>Ein manuell generierter Qualitätsprüfungsauftrag, der sich auf einen Produktionsauftrag bezieht, kann Informationen in einem Qualitätszuordnungsdatensatz, wie dem Testmusteraufnahmeplan, verwenden.</td>
</tr>
<tr>
<td>Produktionsauftrag, der über einen Arbeitsplan-Arbeitsgang verfügt</td>
<td>Bevor oder nachdem der für einen Arbeitsgang abgeschlossen ist</td>
<td>Nachdem die Meldung für den letzten Arbeitsgang abgeschlossen ist</td>
<td>Die Anforderung für einen Qualitätsprüfungsauftrag kann einen bestimmten Standort, ein Element oder eine Vorgangsressource oder eine Kombination dieser Bedingungen widerspiegeln.</td>
<td>Ein manuell generierter Qualitätsprüfungsauftrag, der sich auf einen Arbeitsplan-Arbeitsgang bezieht, kann Informationen in einem Qualitätszuordnungsdatensatz, wie dem Testmusteraufnahmeplan, verwenden.</td>
</tr>
<tr>
<td>Bestand</td>
<td>Ein Qualitätsprüfungsauftrag kann nicht automatisch für eine Transaktion in einer Bestandserfassung oder für Umlagerungserfassungstransaktionen generiert werden.</td>
<td></td>
<td></td>
<td>Ein Qualitätsprüfungsauftrag muss manuell für die Bestandsmenge eines Elements erstellt werden. Physischer Lagerbestand ist erforderlich.</td>
</tr>
</tbody>
</table>
</div>

## <a name="examples-of-automatic-generation-of-quality-orders"></a>Beispiele zur automatischen Generierung von Qualitätsprüfungsaufträgen

### <a name="purchasing"></a>Einkaufen

Im Einkauf, wenn Sie das Feld **Ereignistyp** auf *Produktzugang* und das **Ausführung**-Feld auf *Später* auf der Seite **Qualitätszuordnungen** festgelegt haben, erhalten Sie die folgenden Ergebnisse:

- Wenn die Option **Pro aktualisierter Menge** auf *Ja* festgelegt wird, wird ein Qualitätsprüfungsauftrag für jeden Zugang für den Auftrag anhand der Eingangsmenge und Einstellungen in der Artikelmusteraufnahme generiert. Wenn eine Menge für den Auftrag eingeht, werden neue Qualitätsprüfungsaufträge auf Grundlage der neuen Eingangsmenge generiert.
- Wenn die Option **Pro aktualisierter Menge** auf *Nein* festgelegt wird, wird ein Qualitätsprüfungsauftrag für den ersten Zugang für den Auftrag anhand der Eingangsmenge generiert. Außerdem werden eine oder mehrere Qualitätsprüfungsaufträge auf Basis der Restmenge je nach den Überwachungsdimensionen erstellt. Qualitätsprüfungsaufträge werden nicht für nachfolgende Zugänge für den Auftrag generiert.

### <a name="production"></a>Produktion

In der Produktion, wenn Sie das Feld **Ereignistyp** auf *Fertigmeldung* und das **Ausführung**-Feld auf *Später* auf der Seite **Qualitätszuordnungen** festgelegt haben, erhalten Sie die folgenden Ergebnisse:

- Wenn die Option **Pro aktualisierter Menge** auf *Ja* festgelegt wird, wird ein Qualitätsprüfungsauftrag auf der Basis einer jeden fertiggestellten Menge und der Einstellungen in der Artikelmusteraufnahme generiert. Jedes Mal, wenn eine Menge als fertiggestellt gegen den Produktionsauftrag gemeldet wird, werden neue Qualitätsprüfungsaufträge basierend auf der neu fertiggestellten Menge erzeugt. Diese Generierungslogik ist mit dem Einkauf konsistent.
- Wenn die Option **Pro aktualisierter Menge** auf *Nein* festgelegt wird, wird ein Qualitätsprüfungsauftrag das erste Mal, wenn eine Menge als fertig gemeldet wird, anhand der fertiggestellten Menge generiert. Außerdem werden eine oder mehrere Qualitätsprüfungsaufträge auf Basis der Restmenge je nach den Überwachungsdimensionen der Artikelmusteraufnahme erstellt. Qualitätsprüfungsaufträge werden nicht für nachfolgende fertiggestellte Mengen generiert.

<table>
<thead>
<tr>
<th>Qualitätsspezifikation</th>
<th>Pro aktualisierter Menge</th>
<th>Pro Rückverfolgungsangabe</th>
<th>Ergebnis</th>
</tr>
</thead>
<tbody>
<tr>
<td>Prozentsatz: 10 %</td>
<td>Ja</td>
<td>
<p>Chargennummer: Nein</p>
<p>Seriennummer: Nein</p>
</td>
<td>
<p>Auftragsmenge: 100</p>
<ol>
<li>Fertigmeldung für 30
<ul>
<li>Qualitätsprüfungsauftrag 1 zu 3 (10% von 30)</li>
</ul>
</li>
<li>Fertigmeldung für 70
<ul>
<li>Qualitätsprüfungsauftrag 2 zu 7 (10% der verbleibenden Auftragsmenge, die in diesem Fall 70 beträgt)</li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td>Feste Menge: 1</td>
<td>Nr.</td>
<td>
<p>Chargennummer: Nein</p>
<p>Seriennummer: Nein</p>
</td>
<td>Auftragsmenge: 100
<ol>
<li>Fertigmeldung für 30
<ul>
<li>Qualitätsprüfungsauftrag 1 zu 1 (für die erste als fertig gemeldete Menge, die einen festen Wert von 1 hat)</li>
<li>Qualitätsprüfungsauftrag 2 für 1 (für die Restmenge, die immer noch den festen Wert 1 hat)</li>
</ul>
</li>
<li>Fertigmeldung für 10
<ul>
<li>Es werden keine Qualitätsprüfungsaufträge erstellt.</li>
</ul>
</li>
<li>Fertigmeldung für 60
<ul>
<li>Es werden keine Qualitätsprüfungsaufträge erstellt.</li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td>Feste Menge: 1</td>
<td>Ja</td>
<td>
<p>Chargennummer: Ja</p>
<p>Seriennummer: Ja</p>
</td>
<td>
<p>Auftragsmenge: 10</p>
<ol>
<li>Fertigmeldung für 3: 1 für Batch-Nummer b1, Seriennummer s1; 1 für Batch-Nummer b2, Seriennummer s2; und 1 für Batch-Nummer b3, Seriennummer s3
<ul>
<li>Qualitätsprüfungsauftrag 1 zu 1 von Batch-Nummer b1, Seriennummer s1</li>
<li>Qualitätsprüfungsauftrag 2 für 1 von Batch-Nummer b2, Seriennummer s2</li>
<li>Qualitätsprüfungsauftrag 3 für 1 der Batchnummer b3, Seriennummer s3</li>
</ul>
</li>
<li>Bericht als fertig für 2: 1 für Batch-Nummer b4, Seriennummer s4; und 1 für Batch-Nummer b5, Seriennummer s5
<ul>
<li>Qualitätsprüfungsauftrag 4 für 1 der Batchnummer b4, Seriennummer s4</li>
<li>Qualitätsprüfungsauftrag 5 für 1 der Batchnummer b5, Seriennummer s5</li>
</ul>
</li>
</ol>
<p><strong>Hinweis:</strong> Die Charge kann wiederverwendet werden.</p>
</td>
</tr>
<tr>
<td>Feste Menge: 2</td>
<td>Nr.</td>
<td>
<p>Chargennummer: Ja</p>
<p>Seriennummer: Ja</p>
</td>
<td>
<p>Auftragsmenge: 10</p>
<ol>
<li>Fertigmeldung für 4: 1 für Batchnummer b1, Seriennummer s1; 1 für Batchnummer b2, Seriennummer s2; 1 für Batchnummer b3, Seriennummer s3; und 1 für Batchnummer b4, Seriennummer s4
<ul>
<li>Qualitätsprüfungsauftrag 1 zu 1 von Batch-Nummer b1, Seriennummer s1</li>
<li>Qualitätsprüfungsauftrag 2 für 1 von Batch-Nummer b2, Seriennummer s2</li>
<li>Qualitätsprüfungsauftrag 3 für 1 der Batchnummer b3, Seriennummer s3</li>
<li>Qualitätsprüfungsauftrag 4 für 1 der Batchnummer b4, Seriennummer s4</li>
</ul>
<ul>
<li>Qualitätsprüfungsauftrag 5 zu 2, ohne Bezug auf eine Batch-Nummer und eine Seriennummer</li>
</ul>
</li>
<li>Bericht als beendet für 6: 1 für Batch-Nummer b5, Seriennummer s5; 1 für Batch-Nummer b6, Seriennummer s6; 1 für Batch-Nummer b7, Seriennummer s7; 1 für Batch-Nummer b8, Seriennummer s8; 1 für Batch-Nummer b9, Seriennummer s9; und 1 für Batch-Nummer b10, Seriennummer s10
<ul>
<li>Es werden keine Qualitätsprüfungsaufträge erstellt.</li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Qualitätsmanagementprozesse](quality-management-processes.md)
- [Qualitäts- und Qualitätsmangel-Management aktivieren](enable-quality-management.md)
- [Qualitätsmanagement für Lagerortprozesse](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
