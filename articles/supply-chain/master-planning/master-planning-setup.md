---
title: Produktprogrammpläne einrichten
description: Dieses Thema beschreibt die verschiedenen wichtigen Strategien und Parameter, die zum Einrichten der Produktprogrammpläne verwendet werden.
author: t-benebo
ms.date: 07/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: c06e8cc3ba37baae803bfe8d79b8e111f9e53ac3576ed8004f592cff70a358ff
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758567"
---
# <a name="set-up-master-planning"></a>Produktprogrammpläne einrichten

[!include [banner](../includes/banner.md)]

Dieses Thema beschreibt die verschiedenen wichtigen Strategien und Parameter, die zum Einrichten der Produktprogrammpläne verwendet werden. Es gibt einen Überblick über die verschiedenen Plantypen, die von der Produktprogrammplanung verwendet werden und erläutert, welche Strategie Sie verwenden sollen, abhängig von Ihren Geschäftsanforderungen. Darüber hinaus werden die Hauptparameter beschrieben, die den Plan betreffen und erläutert, wie diese Parameter die Bestellvorschläge beeinflussen.

## <a name="types-of-master-plans"></a>Typen von Produktprogrammplänen

Produktprogrammplanung enthält zwei Arten von Plänen: dynamische und statische. Jeder Typ ist für eine andere Verwendung vorgesehen. Für die optimale Leistung wird empfohlen, dass Sie den relevanten Plan für Ihr Szenario verwenden.

### <a name="static-plan"></a>Statischer Plan

Der statischen Plan bleibt unverändert, unabhängig von Änderungen im Angebot und Nachfrage, bis das nächste Mal diese Produktprogrammplanung ausgeführt wird.

Der statischen Plan wird verwendet, um die Aufträge zu genehmigen und halten, die vorgeschlagen werden. Es handelt sich um einen Betriebsablaufplan, den verschiedene Mitarbeiter wie (Einkäufer oder Produktionsplaner) verwenden können, um informierte Entscheidungen zu treffen und um ihre täglichen Aufgaben und Aktivitäten auszuführen.

Der statische Plan unterstützt auch die Regeneration. Ein total neuer optimierter Plan wird jedes Mal berechnet, wenn die Produktprogrammplanung ausgeführt wird, und vorhandene Aufträge, die nicht genehmigt wurden, werden gelöscht.

### <a name="dynamic-plan"></a>Dynamischer Plan

Der dynamischen Plan beginnt normalerweise als Kopie des statischen Plans, allerdings kann er jedes Mal aktualisiert werden, wenn Stammdaten ändern. Wenn beispielsweise die Daten ändern, wird ein neuer Auftrag erstellt.

Der dynamische Plan wird für auch für Ad-Hoc-Planung verwendet. Damit kann das Unternehmen das sich ändernde Auftragsnetzwerk und die Artikelverfügbarkeit überwachen, ohne den statischen Plan zu stören, den andere Personen für ihre Arbeitsprozesse benötigen. Er wird für besondere Verfügbarkeitszusagen (CTP) verwendet. Der dynamische Plan ist der Standardplan, wenn die Nettoanforderungen über die Auftragsseiten geöffnet sind (wie Bestellung, Auftrag oder Produktionsauftragsseiten).

Der dynamische Plan verwendet Nettoveränderung. Dies hilft, eine schnellere Ausführungszeit sicherzustellen.

## <a name="strategies-for-using-master-plans"></a>Strategien zum Verwenden von Produktprogrammplänen

Sie können einen der Pläne oder zwei Pläne in der Produktprogrammplanung verwenden. Die Strategie, die Sie verwenden, hängt von Ihren Geschäftsanforderungen ab.

### <a name="one-plan-strategy"></a>Ein-Plan-Strategie

Für die Ein-Planstrategie verwenden Sie den gleichen Produktprogrammplan für den statischen Plan und den dynamischen Plan. Diese Strategie wird für Szenarien verwendet, die auf Auftrag gefertigt werden, wenn Sie in der Regel keinen Plan zum Simulieren eines Auftrages haben.

Die Ein-Planstrategie wird üblicherweise bei den Einzelhandel- und Verteilungsbranchen verwendet, oder wo Vertriebslieferdaten bestätigt werden, die auf Service Level-Vereinbarungen (SLAs) oder Lieferzeiten basieren. Für den Plan kann die Lieferdatumskontrolle ohne CTP verwendet werden.

Wenn Sie eine Simulation ausführen müssen, kann der Plan für die Artikel erneut durchgeführt werden, die eine Simulation erfordern. Die geplanten Aufträge, die Simulationserzeugnisse bestellen, werden üblicherweise umgewandelt.

### <a name="two-plan-strategy"></a>Zwei-Plan-Strategie

Für die Zwei-Plan-Strategie verwenden Sie einen statischen Plan und einen anderen und dynamischen Plan. Die Zwei-Plan-Strategie wird in der Regel für Konfigurieren-auf-Auftrag- und Fertigen-auf-Auftrag-Szenarios verwendet, in denen Sie Auftragssimulationen und exakte Lieferdaten für Aufträge berechnen müssen, bei denen die Berechnungen aber die täglichen Arbeitsgänge nicht beeinflussen dürfen. Diese Simulationen werden immer im dynamischen Plan ausgeführt. Die Zwei-Plan-Strategie ist in den Automobil- und Originalcomputerhersteller (OEM)-Branchen beispielsweise nützlich.

Für die Zwei-Plan-Strategie kann für die Lieferdatumskontrolle CTP verwendet werden. Wenn CTP verwendet wird, wird die Ausführung automatisch im dynamischen Plan ausgelöst.

### <a name="setting-up-the-plans"></a>Die Pläne einrichten

Sie können Pläne auf der Seite **Produktprogrammpläne** (**Produktprogrammplanung \> Einstellungen \> Pläne \> Produktprogrammpläne**) erstellen.

Sie können angeben, welche Pläne für den statischen Plan und den dynamischen Plan verwendet werden sollen, indem Sie die Felder **Aktueller statischer Produktprogrammplan** und **Aktueller dynamischer Produktprogrammplan** auf der Seite **Parameter für Produktprogrammplanung** (**Produktprogrammplanung \> Einstellungen \>-Parameter für Produktprogrammplanung**) übernehmen. Um eine Ein-Plan-Strategie zu verwenden, wählen Sie den gleichen Plan in den Feldern **Aktueller statischer Produktprogrammplan** und **Aktueller dynamischer Produktprogrammplan**.

## <a name="types-of-planning-methods"></a>Typen von Planungsmethoden

Drei Berechnungsmethoden können verwendet werden, um die Produktprogrammplanung ausführen: Regenerierung und Nettoveränderung. Jede Methode erstellt einen anderen Plan, wenn sie ausgeführt wird.

Sie geben die Planungsmethode im Dialogfeld **Produktprogrammplanungsausführung** an. Zum Öffnen dieses Dialogfelds, wechseln Sie zu **Produktprogrammplanung \> Produktprogrammplanung \> Ausführen \> Produktprogrammplanung** oder wählen Sie **Ausführen** im Arbeitsbereich **Produktprogrammplanung** aus.

### <a name="regeneration"></a>Neu erzeugen

Die Regenerierungsplanungsmethode löscht vorhandene Bestellvorschläge, es sei denn, sie werden umgewandelt. Sie erstellt neue geplante Aufträge, die auf sämtlichen Anforderungen basieren Die Regeneration ist die einzige Planungsmethode, die für statische Pläne verfügbar ist.

- Änderungen in Lieferungen werden berücksichtigt. Diese Änderungen schließen die Planung mit ein.
- Diese Methode berücksichtigt den **Perioden** Abdeckungscode.
- Diese Methode unterstützt Produktsubstitutionsfunktionen (PI).

### <a name="net-change"></a>Nettoveränderung

Die Nettoveränderungsplanungsmethode generiert Bestellvorschläge, um den Bedarf zu decken, der seit der letzten Produktprogrammplanungsausführung erstellt oder geändert wurde. Angebotsänderungen werden nicht berücksichtigt, wenn diese Methode ausgeführt wird. Das System berücksichtigt keine neuen Lieferungen und zuvor erstellte Bestellvorschläge werden nicht gelöscht, wenn sie nicht mehr benötigt werden. Die Nettoveränderungsplanungsmethode wird schneller ausgeführt als die Regenerierungsmethode. Sie ist nur für dynamische Pläne verfügbar.

- Aktivitätsdaten und zukünftige Daten werden jedoch für alle Anforderungen aktualisiert.
- Diese Methode berücksichtigt den **Perioden** Abdeckungscode aber nicht.
- Diese Methode erfüllt die Planung nicht, selbst wenn sie im Plan aktiviert ist.
- Diese Methode unterstützt die Produktsubstitutionsfunktionen (PI) nicht.

### <a name="net-change-minimized"></a>Nettoveränderung minimiert

Die minimierte Nettoveränderungsplanungsmethode generiert Bestellvorschläge, die nur den Bedarf decken, der seit der letzten Produktprogrammplanungsausführung erstellt oder geändert wurde. Für diese Methode werden, im Gegensatz zu der Nettoveränderungsmethode, die Aktivitätsdaten und zukünftige Daten nur für neuen oder geänderten Bedarf aktualisiert. Diese Planungsmethode ist nur für dynamische Pläne verfügbar.

## <a name="types-of-scheduling-methods"></a>Typen von Planungsmethoden

Für jeden Plan auf dem Inforegister **Allgemeines** der Seite **Produktprogrammpläne** (**Produktprogrammplanung \> Einstellungen \> Pläne \> Produktprogrammpläne**), müssen Sie die Planungsmethode auswählen, die für Produktionsaufträge verwendet wird. Sie können die Produktion auf der Arbeitsgangsebene und auf der Einzelvorgangebene planen.

### <a name="operations-scheduling"></a>Grobterminierung

Diese Grobplanung wird häufig verwendet, wenn eine allgemeine Schätzung der Dauer des Produktionsprozesses benötigt wird. Mit der Grobterminierung werden die Arbeitsgänge im Produktionsarbeitsplan nicht in Einzelvorgänge aufgelöst. Weitere Informationen zur Grobterminierung finden Sie unter [Grobterminierung](/dynamics365/unified-operations/supply-chain/production-control/operations-scheduling).

### <a name="job-scheduling"></a>Feinterminierung

Die Feinterminierung ist eine detailliertere Planungsmethode, in der jeder Arbeitsgang in einzelne Aufgaben oder Einzelvorgänge unterteilt wird. Die Feinterminierung enthält Informationen wie Kapazität. Die Feinterminierung wird normalerweise verwendet, um Einzelvorgänge im Fertigungsbereich für einen sofortigen oder kurzfristigen Zeitrahmen zu planen. Weitere Informationen zur Feinterminierung finden Sie unter [Feinterminierung](/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).

## <a name="time-fences-in-days"></a>Planungszeitraum in Tagen

Für jeden Plan können Sie auswählen, wie weit die verschiedenen zukünftigen Anforderungen und die anderen Aspekte von der Produktprogrammplanung berechnet werden müssen. Die Periode wird als *Planungszeitraum* bezeichnet. Für die optimale Leistung in der Produktprogrammplanung wird empfohlen, dass Sie die verschiedenen Planungszeiträume anpassen, um Ihre geschäftlichen Anforderungen zu erfüllen. Für jeden Plan können Sie die Planungszeiträume auf dem Inforegister **Planungszeiträume in Tagen** auf der Seite **Produktprogrammpläne** finden (**Produktprogrammplanung \> Einstellungen \> Pläne \> Produktprogrammpläne**).

> [!NOTE]
> Die Planungszeiträume geben an, wie weit die verschiedenen Anforderungen und die anderen Aspekte in der Zukunft liegen müssen, um von der Produktprogrammplanung berechnet zu werden. Die Planungszeiträume, die auf dieser Seite ausgewählte sind, setzen die Planungszeiträume, die in der Dispositionssteuerungsgruppe definiert werden. Das bedeutet, dass eine Planungszeitraumoption, die auf Ja festgelegt ist und die Tage definiert, den Planungszeitraum überschreibt, der in der Dispositionssteuerungsgruppe definiert wird. Ist sie auf Nein festgelegt, wird der Planungszeitraum in der Dispositionssteuerungsgruppe definiert. Wenn Sie eine Option nicht verwenden möchten oder nicht verwenden müssen (beispielsweise, wenn Sie keine Aktivitätenmeldungen nutzen möchten) legen Sie diese auf **Ja** fest, und wählen Sie dann im Planungszeitraum (null) Tage **0**.

### <a name="coverage"></a>Disposition

Der Planungszeitraum zeigt die Planungsperiode oder wie weit hinaus der Bedarf mit einbezogen werden soll. In anderen Worten, dies zeigt Ihren Planungshorizont an.

Wenn Sie die Option **Disposition** auf **Ja** festlegen, können Sie den Planungszeitraum überschreiben, der für den Artikel während des Produktprogrammplanungslaufs definiert wird. In diesem Fall geben Sie die Anzahl der Tage ein, für die der Bedarf durch die Berechnung der Produktprogrammplanung gedeckt sein soll. Der Planungszeitraum wird ab dem aktuellen Datum vorwärts berechnet. Bedarf vor dem aktuellen Datum wird immer bearbeitet.

> [!NOTE]
> Für die optimale Leistung in der Produktprogrammplanung wird empfohlen, dass Sie die verschiedenen Planungszeiträume an Ihren Planungshorizont anpassen.

### <a name="freeze"></a>Nichtplanungszeitraum

Der Nichtplanungszeitraum stellt die Periode dar, in der vorhandene Bestellvorschläge nicht geändert werden, wenn eine neue Produktprogrammplanung ausgeführt wird. Die geplanten Aufträge werden gesperrt und es werden keine neuen geplanten Aufträge vorgeschlagen.

Wenn Sie die Option **Sperren** auf **Ja** festlegen, können Sie den gesperrten Planungszeitraum überschreiben, der für den Artikel während des Produktprogrammplanungslaufs definiert wird. In diesem Fall geben Sie die Anzahl Tage ein, für die die Aktivität gesperrt werden soll. Denken Sie daran, dass in dieser Zeit keine neuen Bestellvorschläge generiert werden und vorhandene Bestellvorschläge können nicht geändert werden.

### <a name="firming"></a>Umwandeln

Der Planungszeitraum gibt den Zeithorizont an, in dem Bestellvorschläge automatisch in Produktion und Bestellungen konvertiert werden. Dieser Vorgang ist auch als *automatisches Umwandeln von Bestellvorschlägen* bekannt.

Wenn Sie die Option **Umwandeln** auf **Ja** festlegen, können Sie den umgewandelten Planungszeitraum überschreiben, der für den Artikel während des Produktprogrammplanungslaufs definiert wird. Geben Sie in diesem Fall die Anzahl der Tage ein, für die Bestellvorschläge und geplante Produktionsaufträge automatisch umgewandelt werden sollen. Der umgewandelte Zeitraum wird ab dem Datum des Produktprogrammplanungslaufs vorwärts berechnet. Die automatische Umwandlung einer geplanten Einkaufsbestellung kann vorgenommen werden, wenn Sie einem Kreditor zugewiesen wird.

### <a name="forecast-plan"></a>Absatzplanung

Der Zeitraum für die Absatzplanung gibt an, wie weit die zukünftige Produktprogrammplanung Bestellvorschläge für Artikel erstellt, die geplanten Bedarf haben.

Wenn Sie die Option **Absatzplanung** auf **Ja** festlegen, können Sie den Planungszeitraum überschreiben, der für den Artikel während des Produktprogrammplanungslaufs definiert wird. Geben Sie in diesem Fall die Anzahl der Tage ein, für die die Umsatzplanung aus dem Absatzplan in den Produktprogrammplanungslauf einbezogen werden soll.

### <a name="capacity"></a>Kapazität

Der Kapazitätsplanungszeitraum gibt an, wie weit in der Zukunft das System die maximale Kapazität Ihrer Ressourcen berücksichtigt, wenn es Aufträge plant. Mit anderen Worten bedeutet das, dass der Plan die Produktionsaufträge festlegt, indem er den Produktionsarbeitsplan für die Artikel verwendet, und er die Ressourcen und die maximale Kapazität des Produktionsarbeitsplans jeder Ressource berücksichtigt.

Wenn Sie die Option **Kapazität** auf **Ja** festlegen, können Sie den Kapazitätszeitraum überschreiben, der für den Artikel während des Produktprogrammplanungslaufs definiert wird. In diesem Fall geben Sie die Anzahl der Tage ein, für die die Kapazität für geplante Produktionsaufträge geplant werden soll. Die Produktprogrammplanung verwendet den aktiven Produktionsarbeitsplan für den Artikel und plant ab dem Bedarfsdatum rückwärts. Wenn das Bedarfsdatum für einen geplanten Produktionsauftrag außerhalb des Kapazitätsplanungszeitraums liegt, wird die Durchlaufzeit anhand der Lieferzeit des Artikels bestimmt. Der Kapazitätszeitraum wird ab dem aktuellen Datum vorwärts berechnet.

### <a name="action-message"></a>Aktivitätsmeldung

Aktivitätsmeldungen schlagen Änderungen vor, damit Änderungen am vorhandenen Lieferungsauftrag vorgenommen werden können, um den Lieferungsplan zu optimieren. Zum Beispiel empfiehlt er möglicherweise, dass Sie Aufträge im Voraus wechseln oder verschieben oder dass Sie die Auftragsmengen erhöhen oder verringern.

Wenn Sie die Option **Aktivitätsmeldung** auf **Ja** festlegen, können Sie den Aktivitätsmeldungszeitraum überschreiben, der für den Artikel während des Produktprogrammplanungslaufs definiert wird. In diesem Fall geben Sie die Anzahl der Tage ein, für die Aktivitätsmeldungen für den Bedarf im Produktprogrammplanungslauf generiert werden sollen. Der Aktivitätenmeldungszeitraum wird ab dem aktuellen Datum vorwärts berechnet.

Weitere Informationen zu den Aktivitätenmeldungen finden Sie unter [Aktivitätenmeldungen](/dynamics365/unified-operations/supply-chain/master-planning/action-messages).

> [!NOTE]
> Die Berechnung der Aktivitätsmeldungen bewirkt eine längere Laufzeit der Produktprogrammplanung. Wenn Aktivitätsmeldungen nicht regelmäßig analysiert und angewendet werden (täglich, wöchentlich, usw.), sollten Sie die Berechnung beim Produktprogrammplanungslauf deaktivieren. Um die Berechnung auszuschalten, legen Sie auf der Seite **Produktprogrammpläne** den Planungszeitraum für die **Aktivitätsmeldungen** auf **0** (null) fest für die Produktprogrammplanung, die Sie ausführen. Überprüfen Sie außerdem, dass die Einstellung **Aktivitätsmeldung** für alle Dispositionssteuerungsgruppen deaktiviert ist.

### <a name="calculated-delays"></a>Berechnete Verzögerungen

Sie können angeben, wie weit in der Zukunft mögliche Verzögerungen in den Bestellvorschlägen erkannt und gemeldet werden. Auf diese Weise können Sie alle möglichen (verzögerten) Lieferdaten planen.

Wenn ein Bestellvorschlag nicht für das Anforderungsdatum erfüllt werden kann, ist er für das erste mögliche Erfüllungsdatum für eine Transaktion geplant, basierend auf den Durchlaufzeiten und der Material- und Kapazitätsverfügbarkeit.

### <a name="approved-requisitions-time-fence"></a>Genehmigter Anforderungsplanungszeitraum

Sie können die Produktprogrammplanung einrichten, um Bestellvorschläge für Materialanforderungsbedarf zu erstellen. Hier können Sie die Option **Anforderungen einbeziehen** im Inforegister **Allgemein** auf **Ja** festlegen auf der Seite **Produktprogrammpläne**. Wenn der Zweck einer genehmigten Bestellanforderung Wiederauffüllung lautet, erstellt die Produktprogrammplanung automatisch einen entsprechenden Bestellvorschlag, um ihn zu erfüllen. Die Methode Wiederbeschaffung wird durch die Versorgungsrichtlinien bestimmt, die für die Artikel in der Organisation eingerichtet sind und mit dem Produktprogrammplanungslauf geplant wurden. Nachdem die Wiederbeschaffungsanforderung erstellt und genehmigt wurde, ist keine zusätzliche Benutzeraktivität erforderlich.

Wenn Sie die Option **Genehmigter Materialanforderungsplanungszeitraum** auf dem Inforegister auf **Ja** festgelegt haben unter **Planungszeiträume in Tagen**, können Sie den genehmigten Materialanforderungsplanungszeitraum überschreiben, der für den Artikel während des Produktprogrammplanungslaufs definiert wird. Geben Sie in diesem Fall im Feld die Anzahl der Tage in der Vergangenheit, während derer der Bedarf aus genehmigten Anforderungen bestand, die einen Wiederbeschaffungszweck haben, der im Produktprogrammplanungslauf einbezogen ist. Beispielsweise können Sie angeben, dass nur nicht erfüllter, überfälliger Bedarf aus genehmigten Anforderungen, die in den letzten 10 Tagen erstellt wurden, berücksichtigt und geplant werden soll.

### <a name="sequencing"></a>Abfolge

Abfolge aktivierter Bestellvorschläge werden auf Grundlage der Abfolgeattribute angeordnet, die dem fertigen Produkt zugeordnet werden. Dies wird oft verwendet, um Produktionsaufträge für das Verpacken vorzubereiten. Sie kann zum Beispiel verwendet werden, um Felder in einer bestimmten Reihenfolge, basierend auf Farbe und Größe erneut zu verpacken.

Wenn Sie die Option **Abfolge** auf **Ja** festlegen, können Sie angeben, wie weit die Arbeitsgänge oder Einzelvorgänge geordnet werden sollen. Denken Sie daran, je größer der Planungszeitraum ist, desto länger dauert die Ausführung der Produktprogrammplanung.

### <a name="calculated-delays"></a>Berechnete Verzögerungen

Verzögerungsoptionen helfen sicherzustellen, dass Aufträge durchführbare geplante Daten haben. Die folgenden Optionen sind auf dem Inforegister **Berechnete Verzögerungen** der Seite **Produktprogrammpläne** verfügbar:

- **Stellen Sie sicher, dass die Bestellvorschläge nicht vor Produktprogrammplanungsausführungsproduktionsdatum erstellt werden** – Legen Sie diese Option auf **Jaf** fest, um sicherzustellen, dass Aufträge nicht für Daten in der Vergangenheit geplant werden können.
- **Hinzufügen der berechneten Verzögerung zum Bedarfsdatum** (unter **Geplante Einkaufsbestellungen**) – Legen Sie diese Option auf **Ja** fest, um die berechnete Verzögerung den Bedürfnissen hinzuzufügen.
- **Hinzufügen der berechneten Verzögerung zum Bedarfsdatum** (unter **Geplanter Produktionsauftrag**) – Legen Sie diese Option auf **Ja** fest, um die berechnete Verzögerung den Bedürfnissen hinzuzufügen.
- **Hinzufügen der berechneten Verzögerung zum Bedarfsdatum** (unter **Geplanter Übertrag**) – Legen Sie diese Option auf **Ja** fest, um die berechnete Verzögerung den Bedürfnissen hinzuzufügen.
- **Hinzufügen der berechneten Verzögerung zum Bedarfsdatum** (unter **Geplanter Kanban**) – Legen Sie diese Option auf **Ja** fest, um die berechnete Verzögerung den Bedürfnissen hinzuzufügen.

Wenn Sie die Optionen **Hinzufügen der berechneten Verzögerung zum Bedarfsdatum** auf **Ja** festlegen, werden die Verzögerungen den Bedürfnissen hinzugefügt und das System berücksichtigt die Kapazität von Ressourcen und erstellt durchführbare Bestellvorschläge. Neuberechnen der Bestellvorschlagsdatumsangaben, um die Ausführungszeit für die Produktprogrammplanung zu erhöhen. Wenn Sie die Verzögerungen nicht verwenden müssen, legen Sie Optionen auf **Nein** fest.

## <a name="positive-and-negative-days"></a>Positive und negative Tage

Positive und negative Tage beeinflussen, wie die Produktprogrammplanung Bestellvorschläge und Aktivitäten vorschlägt. Positive und negative Tage werden auf der Artikeldeckungsgruppe des Artikels festgelegt. Sie können unterschiedliche Dispositionssteuerungsgruppen definieren und die Parameter auf der Seite **Dispositionssteuerungsgruppen** festlegen (**Produktprogrammplanung \> Einstellungen \> Disposition \> Dispositionssteuerungsgruppen**).

### <a name="positive-days"></a>Positive Tage

Positive Tage geben an, wie weit zukünftig Produktprogrammplanung den aktuellen Lagerbestand bzw. die Zugänge berücksichtigt, einen zukünftigen Bedarf zu decken. Wenn beispielsweise die positiven Tage auf **100** festgelegt werden, kann der aktuelle Lagerbestand verwendet werden, um Bedarf in die nächsten 100 Tagen zu erfüllen. Wenn ein Auftrag 150 Tage ab dem aktuellen Datum angezeigt wird, erstellt die Produktprogrammplanung einen Bestellvorschlag, der den Bedarf erfüllt, wenn der verfügbare Lagerbestand für den Artikel des Auftrags geeignet ist. Für sich schnell bewegende Artikel, die eine kurze Lieferzeit haben, sollten Sie nicht verfügbaren Lagerbestand für einen Auftrag verwenden, der weit in der Zukunft liegt. In diesem sich schnell bewegenden Fall wird der aktuelle verfügbare Lagerbestand schnell weg sein und weitere Aufträge können in der Zukunft hinzugefügt werden, um einen künftigen Bedarf zu decken, der aufgrund einer kurzen Lieferzeit des Artikels möglich ist.

Die positiven Tage betreffen auch die Aktivitätsmeldungen. Beispielsweise kann das System empfehlen, dass Sie eine geplante Bestellung erhöhen, sodass sie einen Bedarf enthält, der innerhalb der Anzahl von positive Tage in der Zukunft ist. Wenn die positiven Tage auf **100** gesetzt sein und wenn es Bedarf für einen Artikel in 30 Tagen ab dem aktuellen Datum hat, erstellt das System einen Bestellvorschlag, der diese Anforderungen erfüllt. Wenn Bedarf für den gleichen Artikel in 90 Tagen ab dem aktuellen Datum besteht, empfiehlt das System, dass Sie die Menge des Auftrags in 30 Tagen ab dem aktuellen Datum,erhöhen , damit der Auftrag auch den Bedarf in Tage 90 enthält. Wenn Bedarf für den Artikel in 150 Tagen ab dem aktuellen Datum besteht, wird das System nicht empfehlen, dass Sie die Menge der Bestellung erhöhen, der bereits geplant wurde. Stattdessen wird ein neuer Bestellvorschlag erstellt.

In der Regel werden Positive Tage auf einen Wert festgelegt, der zwischen der längsten Lieferzeit der Artikel und dem Planungszeitraum liegt. Es wird empfohlen, dass Sie Artikel zuordnen, die regelmäßig für eine Dispositionssteuerungsgruppe beschafft oder produziert werden, in der die positiven Tage der Lieferzeit des Artikels ergeben.

### <a name="negative-days"></a>Negative Tage

Negative Tage gebem an, wie verspätete Artikelzugänge zulässig sind. Sie zeigen die Anzahl der Tage an, die Sie bereit sind zu warten, bevor Sie eine neue Wiederbeschaffung tätigen, wenn Sie einen negativen Bestand oder nicht genug Bestand haben. Bei negativen Tage wird die Frage gestellt, soll eine neue Bestellung für den Artikel erzeugt werden oder soll ein vorhandener Einkauf verwendet werden, obwohl Sie wissen, dass der Artikel überfällig ist?

Beispielsweise haben Sie einen Auftrag für einen Artikel 15 Tage ab dem aktuellen Datum. Sie haben außerdem eine Bestellung für denselben Artikel. Diese Bestellung wird in 20 Tagen ab dem aktuellen Datum eingehen. Möchten Sie, dass das System eine Bestellung für diesen Auftrag erstellt oder möchten Sie den vorhandenen Auftrag verwenden, auch wenn Sie den Auftrag nicht fristgerecht erfüllen können? Wenn die Anzahl der negativen Tage auf unter **5** festgelegt ist, bedeutet das, dass die Lieferverzögerung für den Artikel maximal fünf Tage sein darf. Das System erstellt dann eine neue geplante Einkaufsbestellung, um den Auftrag zu erfüllen. Wenn die Anzahl der negativen Tage auf über **5** festgelegt ist, verwendet das System den vorhandenen Auftrag für den Artikel.

Die negativen Tage betreffen auch die Leistung der Produktprogrammplanung. Wenn die Anzahl der negativen Tage sehr hoch ist, werden viele Aktivitätsmeldungen generiert.

Es wird empfohlen, dass Sie die negativen Tage auf einen Wert festlegen, der kleiner ist als die Lieferzeit des Artikels.

### <a name="dynamic-negative-days"></a>Dynamische negative Tage

Dynamische negative Tage berücksichtigen die Lieferzeit des Artikels und die negativen Tage, die Sie definiert haben. Das System erstellt eine neue geplante Einkaufsbestellung basierend dem Planungszeitraum der negativen Tage, die mithilfe der folgenden Formel berechnet werden:

Lieferzeit + Negative Tage + Aktuelles Datum - Fälligkeitsdatum des Bedarfs

Das System verwendet nur die geplanten Lieferaufträge, die innerhalb dieses Planungszeitraums sind, und er erstellt einen neuen Bestellvorschlag außerhalb. dieser Zeit. Der Vorteil von dynamischen negativen Tagen ist, dass sie die Einzelproduktlieferzeit enthalten, vorhandene Aufträge wieder verwenden, und das Erstellen neuer Bestellvorschläge vermeiden, die zusammen an einem späteren Datum aufgrund von Verzögerungen in der Lieferzeit enden. 

Weitere Informationen finden Sie unter [Negative Tage und dynamische negative Tagen](/dynamics365/unified-operations/supply-chain/master-planning/more-about-dynamic-negative-days).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]