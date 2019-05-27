---
title: Qualitätsmanagement-Übersicht
description: In diesem Thema wird beschrieben, wie Sie das Qualitätsmanagement in Microsoft Dynamics 365 for Finance and Operations verwenden können, um die Produktqualität innerhalb der Lieferkette zu verbessern.
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1630d13437d7e930fdf32ed5fdc61fc62bc33817
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557499"
---
# <a name="quality-management-overview"></a>Qualitätsmanagement-Übersicht

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie das Qualitätsmanagement in Microsoft Dynamics 365 for Finance and Operations verwenden können, um die Produktqualität innerhalb der Lieferkette zu verbessern.

Das Qualitätsmanagement kann Ihnen dabei helfen, Abfertigungszeiten zu fehlerhaften Produkten zu verwalten (unabhängig vom Ursprung). Da Diagnosetypen mit der Korrekturberichterstellung verknüpft sind, kann Microsoft Dynamics 365 for Finance and Operations Aufgaben planen, um Probleme zu korrigieren und das erneute Auftreten zu verhindern.

Zusätzlich zu den Funktionen für die Verwaltung des Qualitätsmangels, umfasst das Qualitätsmanagement Funktionen für die Nachverfolgung von Problemen nach Problemtyp (auch interne Probleme) und zur Kennzeichnung von Lösungen als kurzzeitig oder langfristig. Die Statistiken zu Key Performance Indicators (KPIs) geben Einblick in den Verlauf von vorherigen Qualitätsmangelprobleme sowie zu Lösungen zu deren Korrektur. Sie können Verlaufsdaten verwenden, um die Effizienz vorheriger Qualitätsmaßnahmen zu prüfen und geeignete Maßnahmen für die Zukunft zu bestimmen.

Wenn Sie eine Qualitätszuordnung festlegen, kann Finance and Operations Qualitätsprüfungsaufträge für verschiedene Geschäftsprozesse, Ereignisse und Bedingungen generieren. Die Qualitätszuordnung kann einen bestimmten Artikel, eine bestimmte Artikelgruppe oder alle Artikel enthalten.

## <a name="examples-of-the-use-of-quality-management"></a>Beispiele für die Nutzung des Qualitätsmanagements
Das Qualitätsmanagement ist flexibel und kann auf unterschiedliche Weise implementiert werden um die Bedingungen bestimmter Lieferkettenarbeitsgangstufen zu erfüllen. Die folgenden Beispiele zeigen die mögliche Verwendung dieser Funktionen:

-   Starten Sie automatisch einen Qualitätskontrollenprozess, basierend auf vordefinierten Kriterien (nach Lagerortregistrierung einer Bestellung von einem bestimmten Kreditor).
-   Sperren Sie einen Bestand während der Prüfung, um die Verwendung eines genehmigten Bestands zu unterbinden (vollständige Sperrung von Bestellungsmengen).
-   Verwenden Sie die Artikelmusteraufnahme als Teil einer Qualitätszuordnung, um die Menge des aktuellen physischen Bestands zu definieren, der geprüft werden müssen. Die Musteraufnahme kann auf festen Mengen oder einem Prozentsatz basieren.
-   Erstellen Sie Qualitätsaufträge für Teilbelege. Um einen Qualitätsauftrag zu erstellen, der auf der für einen Auftrag physisch erhaltenen Menge basiert, müssen Sie das Kontrollkästchen **Pro aktualisierter Menge** auf dem Formular **Artikelmusteraufnahme** markieren.
-   Erstellen Sie Testtypen, die Minimum-, Maximum- und Zielprüfwerte enthalten, und führen Sie Qualitativ-gegen-quantitative-Tests mit vordefinierten Prüfergebnissen aus.
-   Legen Sie ein akzeptables Qualitätsniveau (AQL) fest, um die Qualitätsmessungstoleranz zu steuern.
-   Geben Sie die Ressourcen an, die ein Inspektionsarbeitsgang erfordert (z. B. ein Testbereich und Testinstrumente).

## <a name="working-with-quality-associations"></a>Arbeiten mit Qualitätszuordnungen
Der Geschäftsprozess, der eine Qualitätszuordnung verwendet, kann sich auf verschiedene Quelldokumente beziehen (z. B. Bestellungen, Aufträge oder Produktionsaufträge).

Jeder Qualitätszuordnungsdatensatz definiert den Testsatz, das akzeptable Qualitätsniveau (AQL) und den Musteraufnahmeplan, der für die Qualitätsprüfungsaufträge gilt, die generiert werden. Sie müssen einen Qualitätszuordnungsdatensatz für jede Variante in einem Geschäftsprozess definieren. So können Sie beispielsweise eine Qualitätszuordnung einrichten, die einen Qualitätsprüfungsauftrag generiert, wenn ein Produktzugang für Bestellungen aktualisiert wird. Je nach Einrichtung des Ausführungsplans, kann der auslösende Prozess auch gesperrt werden während es einen offenen Qualitätsprüfungsauftrag gibt. Oder die folgenden Prozesse (z. B. das Fakturieren von Bestellungen) können gesperrt werden.

**Hinweis:** Solange es offene Qualitätsprüfungsaufträge gibt, werden Bestandsmengen automatisch für die Ausgabe gesperrt. Je nach den **Vollständige Sperrung**-Einstellungen auf der **Artikelmusteraufnahmen**-Seite, ist die Menge entweder die Menge im Qualitätsprüfungsauftrag oder die Menge in der Quelldokumentposition.

Für einen angegebenen Geschäftsprozess identifiziert Datensatz für Qualitätszuordnungen das Ereignis und Bedingungen, für die ein Qualitätsprüfungsauftrag generiert wird. Die Bedingungen können entweder für einen Standort oder für eine juristische Person spezifisch sein. Ein Qualitätsprüfungsauftrag mit Zerstörungstests kann nur ausgeführt werden, wenn am Lager Artikel für das Ereignis vorhanden sind.

In den folgenden Beispielen wird die Konfiguration eines Qualitätszuordnungsdatensatzes für die Varianten der einzelnen Geschäftsprozesse erläutert. Für jedes Beispiel sind zudem in der folgenden Tabelle die Ereignisse und Bedingungen zusammengefasst, die durch einen Qualitätszuordnungsdatensatz definiert werden.

<table>
<tbody>
<tr>
<th>Referenztyp</th>
<th>Ereignistyp</th>
<th>Ausführung</th>
<th>Ereignissperrung</th>
<th>Dokumentreferenz</th>
</tr>
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
<td rowspan="2">Vor</td>
<td>Keine</td>
<td rowspan="3">Bestimmte Kennung, Gruppe oder Alle und Ressourcenspezifisch, Gruppe oder Alle</td>
</tr>
<tr>
<td>Fertigmeldung</td>
</tr>
<tr>
<td>Nach</td>
<td>Keine</td>
</tr>
<tr>
<td rowspan="3">Kuppelprodukt - Produktion</td>
<td>Umsatzsteuernummer</td>
<td>Nicht zutreffend</td>
<td rowspan="3">Keine</td>
<td rowspan="3">Alle</td>
</tr>
<tr>
<td rowspan="2">Fertigmeldung</td>
<td>Vor</td>
</tr>
<tr>
<td>Nach</td>
</tr>
</tbody>
</table>

Die folgende Tabelle enthält weitere Informationen darüber, wie Qualitätsprüfungsaufträge für bestimmte Arten von Prozessen generiert werden können.
<div class="tableSection">

<table>
<tbody>
<tr>
<th>Prozesstypen</th>
<th>Wenn Qualitätsprüfungsaufträge automatisch generiert werden können</th>
<th>Wenn Qualitätsprüfungsaufträge generiert werden können, wenn Zerstörungstest erforderlich ist</th>
<th>Bedingungsinformationen</th>
<th>Manuelle Generierungsinformationen</th>
</tr>
<tr>
<td>Bestellung</td>
<td>Bevor oder nachdem eine Zugangsliste oder ein Produktzugang für das erhaltene Material gebucht wird</td>
<td>Nachdem der Produktzugang für das Material, das erhalten wurde, gebucht wurde, da das Material für Zerstörungstest verfügbar sein muss</td>
<td>Die Anforderung für einen Qualitätsprüfungsauftrag kann sich auf einen bestimmten Standort, einen Artikel, einen Kreditor oder auf eine Kombination aus diesen Bedingungen beziehen.</td>
<td>Ein manuell generierter Qualitätsprüfungsauftrag, der sich auf eine Bestellung bezieht, kann Informationen in einem Qualitätszuordnungsdatensatz, wie dem Testmusteraufnahmeplan, verwenden.</td>
</tr>
<tr>
<td>Quarantäneauftrag</td>
<td>Bevor oder nachdem der Quarantäneauftrag als fertig oder abgeschlossen gemeldet wird</td>
<td>Qualitätsprüfungsaufträge, die Zerstörungstests erfordern, können nicht generiert werden. Es wird angenommen, dass die Quarantäneaufträge-Funktionen die Disposition des Materials verarbeiten, das zerstört wird.</td>
<td>Die Anforderung für einen Qualitätsprüfungsauftrag kann sich auf einen bestimmten Standort, einen Artikel, einen Kreditor oder auf eine Kombination aus diesen Bedingungen beziehen.</td>
<td>Ein manuell generierter Qualitätsprüfungsauftrag, der sich auf eine Quarantänebestellung bezieht, kann Informationen in einem Qualitätszuordnungsdatensatz, wie dem Testmusteraufnahmeplan, verwenden.</td>
</tr>
<tr>
<td>Auftrag</td>
<td>Vor eine geplanter Entnahmevorgang oder eine Lieferscheinaktualisierung für die zu liefernden Artikel</td>
<td>Bei einem beliebigen Schritt</td>
<td>Der Bedarf für einen Qualitätsprüfungsauftrag kann sich auf einen bestimmten Standort, einen Artikel, einen Debitor oder auf eine Kombination aus diesen Bedingungen beziehen.</td>
<td>Ein manuell generierter Qualitätsprüfungsauftrag, der sich auf einen Auftrag bezieht, kann Informationen in einem Qualitätszuordnungsdatensatz, wie dem Testmusteraufnahmeplan, verwenden.</td>
</tr>
<tr>
<td>Produktionsauftrag</td>
<td>Bevor oder nachdem die fertig gestellte Menge für den Produktionsauftrag gemeldet wird</td>
<td>Nachdem die fertig gestellte Menge für den Produktionsauftrag gemeldet wird</td>
<td>Der Bedarf für einen Qualitätsprüfungsauftrag kann sich auf einen bestimmten Standort, Debitor oder auf eine Kombination aus diesen Bedingungen beziehen.</td>
<td>Ein manuell generierter Qualitätsprüfungsauftrag, der sich auf einen Produktionsauftrag bezieht, kann Informationen in einem Qualitätszuordnungsdatensatz, wie dem Testmusteraufnahmeplan, verwenden.</td>
</tr>
<tr>
<td>Produktionsauftrag, der über einen Arbeitsplan-Arbeitsgang verfügt</td>
<td>Bevor oder nachdem der für einen Arbeitsgang abgeschlossen ist</td>
<td>Nachdem die Meldung für den letzten Arbeitsgang abgeschlossen ist</td>
<td>Der Bedarf für einen Qualitätsprüfungsauftrag kann sich auf einen bestimmten Standort, einen Artikel, eine betriebliche Ressource oder auf eine Kombination aus diesen Bedingungen beziehen.</td>
<td>Ein manuell generierter Qualitätsprüfungsauftrag, der sich auf einen Arbeitsplan-Arbeitsgang bezieht, kann Informationen in einem Qualitätszuordnungsdatensatz, wie dem Testmusteraufnahmeplan, verwenden.</td>
</tr>
<tr>
<td>Bestand</td>
<td>Ein Qualitätsprüfungsauftrag kann nicht für eine Buchung in einer Lagererfassung oder für Umlagerungsauftragsbuchungen automatisch generiert werden.</td>
<td></td>
<td></td>
<td>Ein Qualitätsprüfungsauftrag muss für die Lagermenge eines Artikels manuell erstellt werden. Physischer Lagerbestand ist erforderlich.</td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a>Qualitätsmanagementseiten
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Seite</th>
<th>Beschreibung</th>
<th>Beispiel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Qualitätszuordnungen</td>
<td>Siehe vorherige Abschnitte dieses Artikels.</td>
<td>Eine Qualitätszuordnung definiert alle folgenden Informationen für einen erzeugten Qualitätsprüfungsauftrag:
<ul>
<li>Das Buchungsereignis</li>
<li>Die Tests, die für die Artikel ausgeführt werden müssen.</li>
<li>Das akzeptable Qualitätsniveau</li>
<li>Den Musteraufnahmeplan</li>
</ul>
Sie müssen eine Qualitätszuordnung für jede Variante in einem Geschäftsprozess definieren, die eine automatische Generierung eines Qualitätsprüfungsauftrags erfordert. So kann ein Qualitätsprüfungsauftrag beispielsweise in Geschäftsprozessen für Bestellungen, Quarantäneaufträge, Aufträge und Produktionsaufträge generiert werden.</td>
</tr>
<tr class="even">
<td>Tests</td>
<td>Mithilfe dieser Seite können Sie die einzelnen Tests definieren und anzeigen, mit denen ermittelt wird, ob Ihre Produkte den Qualitätsangaben entsprechen. Einzelne Tests können einer Testgruppe zugewiesen werden. In diesem Fall werden auch testspezifische Informationen (beispielsweise die zulässigen Messwerte) angegeben. Messwerte kommen bei Mengentests, Testvariablen bei Qualitätstests zum Einsatz.
<ul>
<li>Ein Mengentest besitzt den Testtyp <strong>Ganzzahl</strong> oder <strong>Bruchteil</strong> sowie eine Angabe für die Maßeinheit. Qualitätsangaben und Testergebnisse werden in Zahlen ausgedrückt.</li>
<li>Für einen Qualitätstest wird der Testtyp <strong>Option</strong> verwendet. Qualitative Tests erfordern zusätzliche Informationen über die zu messende Variable und die zugehörigen Optionen. Qualitätsangaben und Testergebnisse werden gemäß einem Ergebnis ausgedrückt.</li>
</ul></td>
<td>Ein Produktionsunternehmen führt zwei Tests für eingekauftes Material durch: einen Mengentest für die Materialqualität und einen Qualitätstest für Verpackungsschäden. Für den Qualitätstest werden weitere Informationen definiert, um die Testvariable (beschädigte Verpackung) und die Ergebnisse zu bestimmen. Auf der Seite <strong>Testgruppen</strong> werden die beiden Tests einer Testgruppe zugeordnet und die testspezifischen Informationen angegeben. Die Testgruppe wird einem Qualitätsprüfungsauftrag zugeordnet, sodass das Unternehmen einen Bericht über die Testergebnisse für die beiden Tests erhält.</td>
</tr>
<tr class="odd">
<td>Testgruppen</td>
<td>Mithilfe dieser Seite können Sie Testgruppen und die einzelnen Tests einrichten, bearbeiten und anzeigen, die einer Testgruppe zugeordnet sind. Im oberen Bereich werden Testgruppen, im unteren Bereich die Tests angezeigt, die einer ausgewählten Testgruppe zugeordnet sind. Sie ordnen einer Testgruppe mehrere Richtlinien zu, z. B. einen Musteraufnahmeplan, eine akzeptables Qualitätsniveau und die Anforderungen für Zerstörungstests. Wenn Sie einer Testgruppe einen einzelnen Test zuweisen, können Sie zusätzliche Informationen definieren (z. B. die Sequenz, Dokumente und Prüfdaten). Bei einem Mengentest zählen zu den zu definierenden Informationen auch die akzeptablen Messwerte. Bei einem Qualitätstest zählen hierzu auch die Testvariable und das Standardergebnis. Die einem Qualitätsprüfungsauftrag zugeordnete Testgruppe definiert die Tests, die für den angegebenen Artikel ausgeführt werden müssen. Tests für die Qualitätsprüfung können jedoch hinzugefügt, geändert oder gelöscht werden. Testergebnisse werden für jeden Test im Qualitätsprüfungsauftrag gemeldet.</td>
<td>Ein Produktionsunternehmen definiert eine Testgruppe für jede Abweichung von den Qualitätsrichtlinien. In den verschiedenen Testgruppen sind Unterschiede in den Musteraufnahmeplänen, die zusammen auszuführenden Tests, das akzeptable Qualitätsniveau und andere Faktoren enthalten. Bei Mengentests sind zudem Unterschiede hinsichtlich der akzeptablen Messwerte enthalten. Um die Qualitätsrichtlinien durchzusetzen weißt das Unternehmen jeder Regel eine Testgruppe zum automatischen Erstellen von Qualitätsprüfungsaufträgen zu (im Formular <strong>Qualitätszuordnungen</strong>) und weißt eine Testgruppe zu den manuell erstellten Qualitätsprüfungsaufträgen zu.</td>
</tr>
<tr class="even">
<td>Artikelqualitätsgruppen</td>
<td>Mithilfe dieser Seite können Sie die Artikel, die einer Qualitätsgruppe zugewiesen sind, oder die Qualitätsgruppen, die einem Artikel zugewiesen sind, einrichten, bearbeiten und anzeigen. Eine Qualitätsgruppe gibt Aufschluss über allgemeine Testanforderungen für Artikel. Nachdem Sie die Testanforderungen auf der Seite <strong>Testgruppen</strong> definiert haben, können die Regeln für die automatische Generierung von Qualitätsprüfungsaufträgen definieren. Um den Vorgang zu vereinfachen, definieren Sie keine Regeln für einzelne Artikel. Stattdessen definieren Sie Regeln für eine Qualitätsgruppe, indem Sie die Seite <strong>Qualitätszuordnungen</strong> verwenden. Sie können auch die Seite <strong>Artikelqualitätsgruppen</strong> für eine ausgewählte Qualitätsgruppe verwenden, um dieser Gruppe geeignete Artikel zuzuweisen. Sie können auch die Seite <strong>Artikelqualitätsgruppen</strong> für eine ausgewählte Qualitätsgruppe verwenden, um dieser dem Artikel passende Qualitätsgruppen zuzuweisen.</td>
<td>Ein Produktionsunternehmen erwirbt verschiedene Rohstoffe, bei denen die gleichen Testanforderungen zur Prüfung eingehender Waren gelten. Das Unternehmen definiert eine Qualitätsgruppe und weist die zugehörigen Artikelnummern der Rohstoffe der Gruppe zu. Später erwirbt das Unternehmen einen neuen Rohstofftyp, für den die gleichen Testanforderungen gelten. Anstatt neue Testanforderungen für den neuen Rohstoff einzurichten, fügt das Unternehmen die Artikelnummer neuen Materials der vorhandenen Qualitätsgruppe hinzu. Das gleiche Produktionsunternehmen produziert auch Artikel, für die die gleichen Produktionstestanforderungen gelten, und liefert Artikel mit den gleichen Anforderungen für die Durchführung von Tests vor der Lieferung. Das Unternehmen definiert zwei zusätzliche Qualitätsgruppen und weist dann jeder Qualitätsgruppe die entsprechenden Artikelnummern zu.</td>
</tr>
<tr class="odd">
<td>Testvariablen</td>
<td>Mit dieser Seite können Sie das die Variablen definieren und anzeigen, die Qualitätstests zugeordnet sind. Für jede Variable definieren Sie Ergebnisaufzählungen, die die möglichen Optionen darstellen. Sie definieren Tests auf der <strong>Tests</strong>-Seite. Bei Mengentests müssen Sie den Testtyp auf <strong>Option</strong> festlegen. Verwenden Sie die Seite <strong>Testgruppen</strong>, um einem einzelnen Test eine Testvariable zuzuweisen.</td>
<td>Ein Unternehmen, das Kekse herstellt, führt einen Prüftest bezüglich des fertigen Produkts aus. Diese Abnahmeprüfung besitzt mehrere Variablen. Eine Variable ist der Geschmack, wobei die möglichen Ergebnisse "gut" oder "schlecht" lauten. Eine zweite Variable ist die Farbe, bei der die möglichen Ergebnisse "zu dunkel", "zu hell" und "in Ordnung" sind.</td>
</tr>
<tr class="even">
<td>Ergebnisse für Testvariable</td>
<td>Mithilfe dieser Seite werden die möglichen Testergebnisse für eine Testvariable geändert, die einem Qualitätstest zugeordnet ist. Für jedes Ergebnis weisen Sie entweder den Status <strong>Erfolgreich</strong> oder <strong>Fehlgeschlagen</strong> zu. Definieren Sie eine Variable und die Ergebnisse für jeden Qualitätstest, der auf der Seite <strong>Tests</strong> definiert ist. (Für Qualitätstests, wird der Testtyp auf der Seite <strong>Option</strong> auf <strong>Tests</strong>) gesetzt. Verwenden Sie die Seite <strong>Testgruppen</strong>, um eine Testvariable und ein Standardergebnis einzelnem Qualitätstest zuzuweisen.</td>
<td>Ein Unternehmen, das Kekse herstellt, führt einen Prüftest bezüglich des fertigen Produkts aus. Diese Abnahmeprüfung besitzt mehrere Variablen. Eine Variable ist der Geschmack, wobei die möglichen Ergebnisse "gut" oder "schlecht" lauten. Eine zweite Variable ist die Farbe, bei der die möglichen Ergebnisse "zu dunkel", "zu hell" und "in Ordnung" sind. Für jedes Ergebnis wird der Status <strong>Erfolgreich</strong> oder <strong>Fehlgeschlagen</strong> festgelegt. Während der Abnahmeprüfung für jede Variable meldet der Inspektor das Testergebnis, indem er eines der Ergebnisse auswählt.</td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Qualitätsmanagementprozesse](quality-management-processes.md)

[Verwaltung von Qualitätsmängeln aktivieren](enable-nonconformance-management.md)
