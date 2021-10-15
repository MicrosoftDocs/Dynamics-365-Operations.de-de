---
title: Engineering-Versionen und Engineering-Produktkategorien
description: Dieses Thema informiert Sie über das Konzept der Engineering-Versionen. Engineering-Versionen sorgen dafür, dass unterschiedliche Zustände eines Produkts und seiner Daten aktuell und übersichtlich gehalten und im System visualisiert werden können.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgLookupDynastring, EngChgProductVersionNumberRule, EngChgEcmProductRoute, EngChgEcmRequestProducts, EngChgEcmProductRoute, EngChgEcmProductPreview,EngChgEcmProductBOMItemIdLookup, EngChgEcmProductBOMConsistOf, EngChgEcmProductCreate, EngChgEcmProductLookup, EngChgProductVersionPrCompany, ngChgProductTypeLookup, EngChgProductType, EngChgProductItemPart, EngChgProductItem, EngChgEcmCategory, EngChgEcmBomDesignerEditBom, EngChgEcmBomDesigner, EngChgEcmBOMCopyDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 42faa9e5f073d718c18422e37212c2ae8a28b28d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572888"
---
# <a name="engineering-versions-and-engineering-product-categories"></a>Engineering-Versionen und Engineering-Produktkategorien

[!include [banner](../includes/banner.md)]

Engineering-Produkte entwickeln sich im Laufe ihres Produktlebenszyklus aus vielen Gründen weiter. Beispielsweise können Änderungen eingeführt werden, um die Gebrauchstauglichkeit des Produkts zu verbessern, eine Komponente zu ändern, weil der Lieferant sie nicht mehr anbietet, auf neue Insights zu reagieren oder Fehler im ursprünglichen Design zu beheben. Es gibt auch viele Gründe, warum diese Änderungen als Teil eines laufenden Produkts gespeichert werden sollten, und zwar so, dass frühere Daten nicht überschrieben werden. Hier sind einige dieser Gründe:

- Sie möchten den Überblick über das Produkt behalten, wie es in früheren Lebenszyklusstatus hergestellt und an Ihre Kunden geliefert wurde.
- Sie benötigen eine Vorlaufzeit, bevor Sie die Änderungen genehmigen und anwenden.
- Sie möchten einen Zeitstempel für jede Änderung haben, und Sie möchten in der Lage sein, zuvor hergestellte Produkte getrennt voneinander auszuliefern.

*Engineering-Versionen* sorgen dafür, dass die verschiedenen Zustände eines Produkts und seiner Daten aktuell und übersichtlich gehalten werden und im System visualisiert werden können. Dieses Konzept hilft Ihnen, die Konsistenz zu wahren, die Stückliste für die Produktion zu sperren, Variabilität zu eliminieren und Änderungen leicht zu erkennen.

Im Allgemeinen wird die *Form-fit-function*-Regel angewendet, um zu bestimmen, ob eine Änderung ein neues Produkt, eine neue Version oder eine Aktualisierung einer bestehenden Version erfordert. Jeder der drei Begriffe im Namen dieser Regel bezieht sich auf einen bestimmten Aspekt eines Teils, was den Ingenieuren hilft, die Teile den Anforderungen anzupassen. Die Form-Fit-Function-Regel erhöht die Flexibilität bei Konstruktionsänderungen, da nur ein minimaler Dokumentations- und Konstruktionsaufwand erforderlich ist, um ein Teil zu ändern, vorausgesetzt, die Passform, Form und Funktion des Produkts bleiben erhalten.

- **Passform** bezieht sich auf die Fähigkeit des Teils oder der Funktion, sich mit einem anderen Teil oder einer anderen Funktion in einer Assembly zu verbinden, zu paaren oder zu fügen. Die Passung ermöglicht es dem Teil, die erforderlichen Assembly-Toleranzen einzuhalten, sodass es nützlich sein kann.
- **Form** bezieht sich auf Eigenschaften eines Teils oder einer Assembly, wie z. B. die äußeren Dimensionen, das Gewicht, die Größe und das optische Erscheinungsbild. Die Form ist der Aspekt, der am meisten von den ästhetischen Entscheidungen eines Ingenieurs beeinflusst wird. Sie umfasst das Gehäuse, das Chassis und das Bedienfeld, die das äußere „Gesicht“ des Produkts bilden.
- **Funktion** ist ein Kriterium, das erfüllt ist, wenn das Teil seinen angegebenen Zweck effektiv und zuverlässig erfüllt. Bei einem Elektronikprodukt kann die Funktion zum Beispiel von den verwendeten Halbleiterkomponenten und der Software oder Firmware abhängen. Oft hängt sie auch von den Funktionen des gewählten Gehäuses ab. Zwei der häufigsten Gründe, warum ein Gehäuse das Funktionskriterium nicht erfüllt, sind schlecht platzierte oder schlecht bemessene Anschlüsse sowie irreführende oder fehlende Beschriftungen. 

## <a name="engineering-versions"></a>Entwicklungsversionen

Wenn Sie Engineering-Produkte verwenden, hat jedes Produkt mindestens eine Engineering-Version. Die erste Engineering-Version wird automatisch erstellt, wenn Sie ein Engineering-Produkt erstellen. Jede Engineering-Version speichert die Engineering-relevanten Daten, die spezifisch für diese Version sind. Hier sind einige Beispiele für diese Daten:

- Die Versionsnummer und die vorherige Versionsnummer (falls zutreffend)
- Das Gültig-ab- und Gültig-bis-Datum
- Der Aktiv-Status der Produktversion, der angibt, ob die Version freigegeben ist und in Transaktionen verwendet werden kann (Weitere Informationen finden Sie unter [Produktbereitschaft](product-readiness.md)).
- Das Ingenieurbüro, das das Produkt erstellt hat und Eigentümer des Produkts ist (weitere Informationen finden Sie unter [Ingenieurbüros und Dateneigentumsregeln](engineering-org-data-ownership-rules.md)).
- Zugehörige technische Dokumente, wie z. B. eine Assembly-Anleitung, Benutzeranweisungen, Bilder und Links
- Die Engineering-Attribute (Weitere Informationen finden Sie unter [Engineering-Attribute und die Suche nach Engineering-Attributen](engineering-attributes-and-search.md).)
- Stückliste (BOM) für technische Produkte
- Formeln für die Prozessfertigung von Produkten
- Die Arbeitspläne für das Engineering

Sie können diese Daten in einer bestehenden Version aktualisieren oder eine neue Version erstellen, indem Sie einen *Engineering-Änderungsauftrag* verwenden. (Weitere Informationen finden Sie unter [Änderungen an Engineering-Produkten verwalten](engineering-change-management.md).) Wenn Sie eine neue Version eines Produkts erstellen, kopiert das System alle Engineering-relevanten Daten in diese neue Version. Sie können dann die Daten für diese neue Version ändern. Auf diese Weise können Sie bestimmte Daten für jede aufeinanderfolgende Version verfolgen. Um die Unterschiede zwischen aufeinanderfolgenden Engineering-Versionen zu vergleichen, sehen Sie sich den Engineering-Änderungsauftrag an, der Änderungsarten enthält, die alle Änderungen anzeigen.

Wie bereits erwähnt, wird die erste Engineering-Version automatisch erstellt, wenn Sie ein Engineering-Produkt erstellen. Die Versionsnummer für diese Version folgt der Versionsnummernregel, die in der Engineering-Kategorie für das Produkt definiert ist. Um zu einer Folgeversion überzugehen, müssen Sie das Produkt als Zeile zu einem Änderungsauftrag hinzufügen und das Feld **Auswirkung** auf *Neue Version* festlegen. Der Änderungsauftrag wird die Details der Änderung von der aktuellen Version zur nächsten Version enthalten.

Beachten Sie, dass ein technisches Produkt immer nur in einem Änderungsauftrag sein kann. Diese Einschränkung gewährleistet die Datengenauigkeit und hilft, sich überschneidende oder widersprüchliche Änderungen am Produkt zu vermeiden. Beachten Sie auch, dass das Feld **Ingenieur** in der Ansicht **Kopf** des Änderungsauftrags den Ingenieur anzeigt, der für den Änderungsauftrag verantwortlich ist. Wenn der Ingenieur zu einem Team gehört, das im System definiert ist, zeigt das Feld **Verantwortlicher** den Leiter dieses Teams an.

## <a name="track-versions-in-transactions"></a>Versionen in Transaktionen verfolgen

Wenn Sie die Verwaltung für technische Änderung verwenden, enthalten Ihre Produktstammdaten immer eine oder mehrere Entwicklungsversionen. In Ihrem Einrichten von Engineering-Produkten können Sie wählen, ob die Engineering-Version auch Teil von *logistischen Transaktionen* ist. (Weitere Informationen finden Sie im Abschnitt [Einrichten von Engineering-Produktkategorien](#product-category) weiter unten in diesem Thema). Wenn die logistische Auswirkung relevant ist, unterscheidet sie sich pro Produkt und pro Firma. Manchmal wird nur die neueste Version eines Produkts verwendet. Wenn Sie also eine neue Version einführen, kann die Vorgängerversion nicht mehr verwendet werden. In anderen Fällen wird die vorherige Version bei logistischen Transaktionen benötigt, um folgende Herausforderungen zu bewältigen:

- Die Logistikabteilung muss zwei Stück eines Produkts an einen Kunden liefern. In diesem Fall muss entschieden werden, ob zwei verschiedene Versionen verschickt werden sollen oder dürfen.
- Später wird festgestellt, dass ein Problem auftritt, das mit einer bestimmten Änderung zusammenhängt. In diesem Fall kann es von Vorteil sein, genau zu bestimmen, welche Version in jedem Auftrag ausgeliefert wurde.
- Unternehmen wollen in der Regel alte Versionen zuerst ausliefern, um sie aus dem Bestand zu nehmen. Vor allem bei Produkten mit geringem Volumen kann dieser Ansatz oft durch die Bestimmung der Gültigkeitsdaten der neuen Version in Relation zu den Vorhersagen, wann der Bestand der alten Version aufgebraucht sein wird, gesteuert werden. Manchmal ist dieser Vergleich jedoch nicht möglich, oder die Unsicherheit der Vorhersagen über den Lagerbestand ist zu groß.

Die Entscheidung, ob Versionen im Bestand sichtbar gemacht werden sollen, hängt von Faktoren wie den zuvor genannten ab, sowie von der Unternehmenspraxis und anderen Überlegungen, die für jedes Unternehmen spezifisch sind. Sie können das Verhalten für die *Produktkategorie Technik* festlegen. Es gilt dann für alle Produkte, die aus dieser Kategorie erstellt werden, für alle Firmen, für die das Produkt freigegeben wird.

Für Produkte, die so festgelegt sind, dass sie logistische Auswirkungen haben, muss die Engineering-Version bei jeder Transaktion angegeben werden. Obwohl das System die *letzte aktive Version* vorschlägt, können Sie unter allen aktiven Versionen wählen, die für die Firma verfügbar sind. Für Produkte, die so festgelegt sind, dass sie keine logistischen Auswirkungen haben, wird die Engineering-Version nicht auf Transaktionen angegeben. Das System verwendet jedoch die letzte aktive Version. Wenn Sie z. B. ein Produkt zu einer Produktionsstückliste hinzufügen, wird die neueste Version verwendet, und wenn Sie die Masterplanung ausführen, wird die neueste Version angenommen.

## <a name="set-up-engineering-product-categories"></a><a name="product-category"></a>Einrichten von Engineering-Produktkategorien

Eine Engineering-Produktkategorie bietet eine Grundlage für das Erstellen eines bestimmten Engineering-Produkts. Jede Kategorie legt eine Reihe von Standardwerten und Richtlinien fest. Wenn Sie ein Engineering-Produkt erstellen, wählen Sie daher zunächst die Kategorie aus, in der es erstellt werden soll.

Beachten Sie, dass ein neuer Kategorie-Hierarchietyp (*Engineering-Produkt-Hierarchie*) automatisch für Sie festgelegt wird. Sie können die Kategorien manuell erstellen, indem Sie zu **Verwaltung für technische Änderung \> Einrichten \> Engineering-Produktkategoriedetails** gehen.

Jede Engineering-Produktkategorie legt das Standardverhalten der Engineering-Produkte fest, die auf der Basis dieser Kategorie erstellt werden. Nachdem Sie ein Engineering-Produkt erstellt haben, können Sie seine Engineering-Produktkategorie nicht mehr ändern. Wenn Sie jedoch die falsche Kategorie ausgewählt haben, können Sie das Produkt löschen und anschließend neu erstellen.

Wenn eine technische Produktkategorie erstellt wird, können Sie die folgenden Einstellungen nicht mehr ändern:

- Ingenieurbüro
- Produkttyp
- Produktuntertyp
- Produktdimensionsgruppe
- Konfigurationstechnologie
- Versionsnummernregel

Andere Einstellungen können die Standardwerte erben, die für die Engineering-Produktkategorie festgelegt wurden. Gemäß den Systemregeln können diese Werte jedoch geändert werden.

Um mit Verwaltung für technische Änderung zu arbeiten, gehen Sie zu **Verwaltung für technische Änderung \> Einrichten \> Details der Entwicklungsproduktkategorie**. Führen Sie dann einen der folgenden Schritte aus.

- Um eine neue Kategorie zu erstellen, wählen Sie **Neu** im Aktivitätsbereich und legen Sie dann die Felder wie in den folgenden Unterabschnitten beschrieben fest.
- Um eine bestehende Kategorie zu bearbeiten, wählen Sie sie im Listenbereich aus, wählen Sie **Bearbeiten** im Aktivitätsbereich und legen Sie dann die Felder fest, wie in den folgenden Unterabschnitten beschrieben.
- Um eine vorhandene Kategorie zu löschen, wählen Sie sie im Listenbereich aus und wählen Sie dann **Löschen** im Aktivitätsbereich.

### <a name="header"></a>Übergeordnet

Legen Sie die folgenden Felder in der Kopfzeile einer Engineering-Produktkategorie fest.

| Feld | Beschreibung |
|---|---|
| Name | Geben Sie einen Namen für die Engineering-Produktkategorie ein. |
| Engineering-Firma | Wählen Sie das Ingenieurbüro aus, in dem Produkte in dieser Engineering-Produktkategorie erstellt werden können und in dem sie gepflegt werden sollen. |

### <a name="details-fasttab"></a>Details Inforegister

Legen Sie die folgenden Felder auf dem **Details** Inforegister einer Engineering-Produktkategorie fest.

| Feld | Beschreibung |
|---|---|
| Produkttyp | Wählen Sie aus, ob die Kategorie für Produkte oder Dienstleistungen gilt. |
| Produktionstyp | Dieses Feld wird nur angezeigt, wenn Sie [Formeländerungsmanagement](manage-formula-changes.md) in Ihrem System aktiviert haben. Dient zum Auswählen des Produktionstyps, für den diese Produktkategorie gültig ist:<ul><li>**Planungsgegenstand** – Verwenden Sie diese Engineering-Kategorie, um das Formeländerungsmanagement für Planungselemente durchzuführen. Planungselemente verwenden Formeln. Sie ähneln Formeln, werden jedoch nur zur Herstellung von Co-Produkten und Nebenprodukten verwendet, nicht von Fertigprodukten. Formeln werden bei der Prozessherstellung verwendet.</li><li>**Stückliste** – Verwenden Sie diese Engineering-Kategorie, um Engineering-Produkte zu verwalten, die keine Formeln verwenden und normalerweise (aber nicht unbedingt) Stücklisten enthalten.</li><li>**Formel** – Verwenden Sie diese Engineering-Kategorie, um das Formeländerungsmanagement für fertiggestellte Produkte durchzuführen. Diese Artikel haben eine Formel, aber keine Stückliste. Formeln werden bei der Prozessherstellung verwendet.</li></ul> |
| Artikelgewicht | Diese Option wird nur angezeigt, wenn Sie [Formeländerungsmanagement](manage-formula-changes.md) in Ihrem System aktiviert haben. Es ist nur verfügbar, wenn das Feld **Produktionsart** auf *Planungsgegenstand* oder *Formel* festgelegt ist. Setzen Sie diese Option auf *Ja*, wenn Sie diese Engineering-Kategorie verwenden, um Elemente zu verwalten, für die eine Unterstützung des Fanggewichts erforderlich ist. |
| Versionen in Transaktionen verfolgen | Wählen Sie, ob die Version des Produkts auf allen Transaktionen gestempelt werden soll (logistische Auswirkungen). Wenn Sie beispielsweise die Version in Transaktionen verfolgen, wird in jedem Verkaufsauftrag angezeigt, welche spezifische Version des Produkts in diesem Verkaufsauftrag verkauft wurde. Wenn Sie die Version in Transaktionen nicht nachverfolgen, zeigen Verkaufsaufträge nicht an, welche spezifische Version verkauft wurde. Stattdessen zeigen sie immer die neueste Version an.<ul><li>Wenn diese Option auf *Ja* festgelegt ist, wird ein Produktstamm für das Produkt erstellt, und jede Version des Produkts wird eine Variante sein, die die Produktdimension *Version* verwendet. Das Feld **Produktuntertyp** wird automatisch auf *Produktstamm* festgelegt, und im Feld **Produktdimensionsgruppe** müssen Sie eine Produktdimensionsgruppe auswählen, in der die Dimension *Version* aktiv ist. Es werden nur Produktdimensionsgruppen angezeigt, bei denen *Version* eine aktive Dimension ist. Sie können neue Produktdimensionsgruppen erstellen, indem Sie die Schaltfläche **Bearbeiten** (Bleistiftsymbol) wählen.</li><li>Wenn diese Option auf *Nein* festgelegt ist, wird die Produktdimension *Version* nicht verwendet. Sie können dann wählen, ob ein Produkt oder ein Produktstamm erstellt werden soll, der die anderen Dimensionen verwendet.</li></ul><p>Diese Option wird oft für Produkte verwendet, die einen Kostenunterschied zwischen den Versionen haben, oder für Produkte, bei denen unterschiedliche Bedingungen in Bezug auf den Kunden gelten. Daher ist es wichtig, anzugeben, welche Version in jeder Transaktion verwendet wurde.</p> |
| Produktuntertyp | Wählen Sie, ob die Kategorie Produkte oder Produktstämme enthalten soll. Für Produktstämme werden Produktdimensionen verwendet.
| Produktdimensionsgruppe | Die Einstellung **Versionen in Transaktionen verfolgen** hilft Ihnen, die Gruppe der Produktdimensionen auszuwählen. Wenn Sie angegeben haben, dass Sie die Version in Transaktionen verfolgen wollen, werden die Produktdimensionsgruppen angezeigt, in denen die Dimension *Version* verwendet wird. Andernfalls werden nur Produktdimensionsgruppen angezeigt, in denen die Dimension *Version* nicht verwendet wird. |
| Status des Produktlebenszyklus bei der Erstellung | Legen Sie den Standardstatus für den Produktlebenszyklus fest, den ein Engineering-Produkt haben soll, wenn es zum ersten Mal erstellt wird. Weitere Informationen finden Sie unter [Produktlebenszyklusstatus und Transaktionen](product-lifecycle-state-transactions.md). |
| Versionsnummernregel | Wählen Sie die Versionsnummernregel, die für die Kategorie gilt:<ul><li>**Manuell** - Sie wählen die Versionsnummer für jede neue Version.</li><li>**Automatisch** - Das System legt die Versionsnummer fest, basierend auf einem Format, das Sie definieren. Wenn Sie das Format festlegen, verwenden Sie ein Zahlenzeichen (\#), um eine Ziffer darzustellen, und jedes andere Zeichen, um einen konstanten Wert darzustellen. Wenn Sie das Format z. B. als *V-\#\#* definieren, ist die erste Version „V-01“, die zweite Version „V-02“ und so weiter.</li><li>**Liste** - Das System nimmt die nächste Nummer aus einer vordefinierten Liste von benutzerdefinierten Werten, die Sie definieren.</li></ul> |
| Gültigkeit erzwingen | Wählen Sie, ob die Gültigkeitsdaten von Engineering-Versionen zusammenhängend sein müssen oder ob es Lücken und Überschneidungen geben kann. Diese Einstellung wirkt sich auf die Art und Weise aus, wie Sie die Felder **Gültig von** und **Gültig bis** für jede Engineering-Version verwenden können, für die die Kategorie gilt.<ul><li>Wenn diese Option auf *Ja* festgelegt ist, muss für jede Version ein **Wirksam von**-Wert angegeben werden, und es sind weder Überschneidungen noch Lücken zwischen den Versionen erlaubt. Der Datumsbereich für jede Engineering-Version ist direkt mit der vorherigen und der nächsten Engineering-Version verbunden, falls diese existieren. In diesem Szenario wird immer die neueste Version verwendet, und ältere Versionen werden nicht mehr verwendet.</li><li>Wenn diese Option auf **Nein** festgelegt ist, gibt es keine Einschränkungen bei den Gültigkeitsdatumsfeldern für Engineering-Versionen, und sowohl Überschneidungen als auch Lücken sind erlaubt. In diesem Szenario können mehrere Versionen gleichzeitig aktiv sein, und Sie können mit jeder aktiven Version arbeiten.</li></ul><p>Diese Option wirkt sich auch auf Stücklisten und Arbeitspläne aus, die mit einer Produktversion verbunden sind. Weitere Informationen finden Sie im Abschnitt [Stücklisten und Arbeitspläne mit Engineering-Versionen verbinden](#boms-routes) weiter unten in diesem Thema.</p> |
| Nummernregelbezeichnungen verwenden | Legen Sie diese Option auf *Ja* fest, um Regeln für die Definition einer Produktnummer durch Verwendung von Sequenzen, Namen und Werten von Engineering-Attributen und Textkonstanten als Segmente zu aktivieren. Um Regeln zu erstellen oder zu ändern, wählen Sie die Schaltfläche **Bearbeiten**. |
| Namensregelbezeichnungen verwenden | Legen Sie diese Option auf *Ja* fest, um Regeln für die Definition eines Namens durch die Verwendung von Engineering-Attributnamen, Engineering-Attributwerten und Textkonstanten als Segmente zu aktivieren. Um Regeln zu erstellen oder zu ändern, wählen Sie die Schaltfläche **Bearbeiten**. |
| Beschreibungsregelbezeichnung verwenden | Legen Sie diese Option auf *Ja* fest, um Regeln für die Definition der Beschreibung zu aktivieren, indem Sie die Engineering-Attribut-Namen, Engineering-Attribut-Werte und Textkonstanten als Segmente verwenden. Um Regeln zu erstellen oder zu ändern, wählen Sie die Schaltfläche **Bearbeiten**. |

### <a name="attributes-fasttab"></a>Attribute Inforegister

Verwenden Sie das Raster auf dem Inforegister **Attribute**, um die technischen Attribute festzulegen, die für Produkte gelten, die zu dieser Kategorie gehören. Informationen über das Erstellen von Engineering-Attributen finden Sie unter [Engineering-Attribute und Engineering-Attribut-Suche](engineering-attributes-and-search.md).

Verwenden Sie die Schaltflächen auf dem Inforegister **Attribute**, um Attribute im Raster hinzuzufügen, zu entfernen und anzuordnen.

Wenn Sie die Auswahl der Attribute für eine Engineering-Kategorie ändern und bereits Produkte existieren, die auf dieser Kategorie basieren, müssen Sie entscheiden, ob Sie Ihre Änderungen auf diese Produkte anwenden wollen. Wenn Sie möchten, dass vorhandene Produkte die Änderungen widerspiegeln, wählen Sie **Vorhandene Produkte aktualisieren** auf der Inforegisterkarte **Attribute**.

Legen Sie für jede Zeile, die Sie dem Raster hinzufügen, die folgenden Felder fest.

| Feld | Beschreibung |
|---|---|
| Name | Wählen Sie das Attribut, das Sie hinzufügen möchten. |
| Wert | Wählen Sie den Standardwert für das Attribut. |
| Obligatorisch | Bei Attributen vom Typ *Boolean* muss der Benutzer, wenn diese Option auf *Ja* festgelegt ist, das Attribut auf *Ja* setzen. Wenn diese Option auf *Nein* festgelegt ist, können Benutzer das Attribut entweder auf *Ja* oder *Nein* festlegen. Für andere Datentypen hat die Einstellung dieser Option nur informativen Charakter. |
| Chargenattribut | Wählen Sie, ob das Attribut über die Batch-Funktionalität propagiert werden soll. |

### <a name="readiness-policy-fasttab"></a>Richtlinie für Bereitschaft Inforegister

Verwenden Sie das Feld **Produkt-Bereitschaftsrichtlinie**, um die Bereitschaftsrichtlinie auszuwählen, die für Produkte gilt, die zu dieser Engineering-Kategorie gehören. Weitere Informationen finden Sie unter [Produktbereitschaft](product-readiness.md).

> [!NOTE]
> Das Feld **Produktbereitschaftsrichtlinie** funktioniert etwas anders, wenn Sie die Funktion *Produktbereitschaftsprüfungen* in Ihrem System aktiviert haben. (Mit dieser Funktion können Sie Bereitschaftsrichtlinien auf Standard \[Nicht-Engineering\] Produkte anwenden). Weitere Informationen finden Sie unter [Weisen Sie Standard- und Engineering-Produkten Bereitschaftsrichtlinien zu](product-readiness.md#assign-policy).

### <a name="release-policy-fasttab"></a>Inforegister-Richtlinie

Verwenden Sie das Feld **Produktfreigabe-Richtlinie**, um die Freigabe-Richtlinie auszuwählen, die für die Produkte gilt, die zu dieser Kategorie gehören. Weitere Informationen finden Sie unter [Produktstrukturen freigeben](release-product-structure.md).

## <a name="connect-boms-and-routes-to-engineering-versions"></a><a name="boms-routes"></a>Stücklisten und Arbeitspläne mit Engineering-Versionen verknüpfen

Die Einstellung der Option **Gültigkeit erzwingen** ist wichtig für die Verbindung von Stücklisten und Arbeitsplänen mit jeder Engineering-Version. Sie können mehrere Stücklisten oder Arbeitspläne pro Produkt nur dann aktivieren, wenn es einen Unterschied in einer der folgenden Einstellungen gibt:

- Produktdimension
- Leistung
- Standort
- Gültigkeitsdaten

Stücklisten und Arbeitspläne werden von der jeweiligen Arbeitsplanversion aus erstellt, für die sie gelten. Sie sind an dem Häkchen im Kontrollkästchen **Engineering gesteuert** zu erkennen. Wenn Sie mit Engineering-Stücklisten und Arbeitsplänen arbeiten, werden Sie diese in der Regel nicht mit unterschiedlichen Mengen konstruieren. Sie werden auch nicht typischerweise verschiedene Stücklisten pro Standort entwerfen. Außerdem werden die Gültigkeitsdaten für technische Stücklisten und Arbeitspläne immer aus der technischen Version übernommen. Daher haben eine technische Version, ihre Stückliste und ihr Arbeitsplan alle die gleichen Gültigkeitsdaten.

Für Produkte, bei denen Sie die Produktdimension *Version* verwenden (zusammen mit logistischen Auswirkungen auf die Transaktionen), wird die Version auch zu den Stücklisten und Arbeitsplänen hinzugefügt. Dieses Verhalten hilft bei der Unterscheidung der Stücklisten und Arbeitspläne von aufeinanderfolgenden Versionen, unabhängig von der Einstellung **Wirkung erzwingen**.

Für Produkte, bei denen Sie die Produktdimension *Version* nicht verwenden (ohne logistische Auswirkungen auf die Transaktionen), wird die Version nicht zu den Stücklisten oder Arbeitsplänen hinzugefügt. Daher gibt es keinen Unterschied zwischen den Stücklisten und Arbeitsplänen von aufeinanderfolgenden Versionen. In diesem Fall empfehlen wir dringend, die Option **Wirkung erzwingen** auf *Ja* festzulegen. Auf diese Weise verhindern Sie zum einen, dass sich Engineering-Versionen überschneiden, zum anderen können Sie die Stückliste und den Arbeitsplan einer neueren Version aktivieren, ohne vorher die Stückliste und den Arbeitsplan der Vorgängerversion inaktivieren zu müssen. Wenn Sie in diesem Fall die Option **Wirksamkeit erzwingen** auf *Ja* festlegen, müssen Sie die Stücklisten und Arbeitspläne älterer Versionen manuell inaktivieren, bevor Sie die neuere Version aktivieren können.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
