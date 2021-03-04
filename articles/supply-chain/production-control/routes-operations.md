---
title: Arbeitsplan und Arbeitsgänge
description: Dieses Thema enthält allgemeine Informationen zu Arbeitsplan und Arbeitsgänge.
author: sorenva
manager: tfehr
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMDesigner, BOMDesignerRouteVersion, Route, RouteInventProd, RouteOpr, RouteOprTable, ProdRouteJob, ProdRouteTrans, ProdRouteOverview, ProdRouteJobOverview, ProdRouteJobListPagePreviewPane, RouteTable, RouteVersionFeasibility, ProdRouteJobCurrent, RouteGroup, RouteProductionOrder, EngChgCaseRouteTablePart, EcoResProductProdTypeFormulaNoActiveRouteFormPart,
ms.author: sorenand
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 268124
ms.assetid: f78d5836-3e71-42b7-a5d1-41f19228d9d2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: adf890f5305f4e6a62c2d7527ff3b593ed61eff3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428514"
---
# <a name="routes-and-operations"></a>Arbeitspläne und Arbeitsgänge

[!include [banner](../includes/banner.md)]

Dieses Thema enthält allgemeine Informationen zu Arbeitsplan und Arbeitsgänge. Ein Arbeitsplan definiert den Prozess für die Produktion eines Produkts oder die Produktvariante. Er beschreibt jeden Schritt (Arbeitsgang) im Produktionsprozess und den Auftrag für den diese Schritte ausgeführt werden müssen. Für jeden Schritt definiert der Arbeitsplan erforderliche betrieblichen Ressourcen, die Zeit der erforderlichen Einstellungen und die Bearbeitungszeit sowie wie die Kosten berechnet werden sollen.

<a name="overview"></a>Überblick
--------

Ein Arbeitsplan beschreibt die Reihenfolge der Arbeitsgänge, der erforderlich ist, um ein Produkt oder eine ausgewählte Produktvariante zu erzeugen. Für jeden Arbeitsgang definiert der Arbeitsplan auch die betrieblichen Ressourcen, die erforderlich sind, die Zeit, die benötigt wird, um den Arbeitsgang einrichten und ausführen, und wie Kosten berechnet werden sollen. Sie können dieselben Arbeitsplan verwenden, um mehrere Produkte anzuzeigen, oder Sie können einen eindeutigen Arbeitsplan für jedes Produkt oder Produktvariante definieren. Sie können sogar mehrere Arbeitspläne für das gleiche Produkt haben. In diesem Fall hängt der Arbeitsplan, der verwendet wird, von Faktoren wie der Menge, die produziert werden muss ab. Die Definition eines Arbeitsplans in Supply Chain Management besteht aus vier verschiedenen Elemente, die zusammen den Produktionsprozess beschreiben:

- **Arbeitsplan** – Ein Arbeitsplan definiert die Struktur des Produktionsprozesses. Das bedeutet, er definiert die Reihenfolge der Arbeitsgänge.
- **Arbeitsgang** – Ein Arbeitsgang gibt einen Schritt in einem benannten Arbeitsplan an (z. B. **Zusammenbau**). Der gleiche Vorgang kann in mehreren Arbeitsplänen auftreten und unterschiedliche Arbeitsgangnummern haben.
- **Arbeitsgangzuordnung** – Eine Arbeitsgangzuordnung definiert die betrieblichen Eigenschaften eines Arbeitsgangs, wie Rüstzeit und die Bearbeitungszeit, Kostenkategorien, Verbrauchsparameter und Ressourcenanforderungen. Die betrieblichen Arbeitsgangzuordnung ermöglicht unterschiedliche Eigenschaften eines Arbeitsgangs, je nach spezifischem Arbeitsplan und Arbeitsgang für die Produkte die produziert werden.
- **Arbeitsplanversion** – Eine Arbeitsplanversion definiert den Arbeitsplan, der verwendet wird, um ein Produkt oder eine ausgewählte Produktvariante zu erzeugen. Arbeitsplanversionen ermöglichen das Wiederverwendet von Arbeitsplänen für Produkte oder Änderungen. Sie ermöglichen auch unterschiedliche Arbeitpläne, um die gleichen Produkte zu erzeugen. In diesem Fall hängt der Arbeitsplan, der verwendet wird, von Faktoren wie dem Standort oder der Menge, die produziert werden muss ab.

## <a name="routes"></a>Arbeitspläne
Ein Arbeitsplan beschreibt die Reihenfolge der Arbeitsgänge, der verwendet wird, um ein Produkt oder eine ausgewählte Produktvariante zu erzeugen. Jeder Arbeitsgang wird eine Arbeitsgangnummer und einen Folgeaktivitätsarbeitsgang zugewiesen. Die Reihenfolge der Arbeitsgangsformularen eines Arbeitsplan-Netzwerks kann als Diagramm dargestellt werden, das ein oder mehrere Startpunkte und einen bestimmten Endpunkt hat. In Supply Chain Management werden Arbeitspläne basierend auf dem Typ der Struktur unterschieden. Die zwei Typen der Arbeitspläne sind einfache Arbeitspläne und Arbeitsplan-Netzwerke. In den Produktionssteuerungsparametern können Sie angeben, ob nur einfache Arbeitspläne verwendet werden können oder ob die komplexeren Arbeitsplan-Netzwerke verwendet werden können.

### <a name="simple-routes"></a>Einfache Arbeitspläne

Ein einfacher Arbeitsplan ist fortlaufend, und es ist nur einen Startpunkt für den Arbeitsplan definiert.  

[![Einfache Arbeitspläne](./media/routes-and-operations-1-simple-route.png)](./media/routes-and-operations-1-simple-route.png)  

Wenn Sie nur einfache Arbeitspläne in den Produktionssteuerungsparametern aktivieren, generiert Supply Chain Management automatisch die Arbeitsgangnummern (10, 20, 30 usw.), wenn Sie den Arbeitsplan definieren.

### <a name="route-networks"></a>Arbeitsplan-Netzwerke

Wenn Sie die komplexeren Arbeitsplan-Netzwerke in den Produktionssteuerungsparametern aktivieren, können Sie Arbeitspläne definieren, die mehrere Startpunkte haben und Arbeitsgängen, die gleichzeitig ausgeführt werden können.  

[![Arbeitsplan-Netzwerk](./media/routes-and-operations-2-route-network.png)](./media/routes-and-operations-2-route-network.png)  

> [!NOTE]
> - Jeder Arbeitsgang kann nur einen Folgeaktivitätsarbeitsgang haben, und der gesamte Arbeitsplan muss in einem einzigen Arbeitsgang beendet werden.
> - Dies gibt keine Garantie, dass mehrere Arbeitsgänge, die den gleichen Folgeaktivitätsarbeitsgang haben (z. B. Arbeitsgänge 30 und 40 in der vorhergehenden Abbildung)tatsächlich parallel ausgeführt werden. Die Verfügbarkeit und die Kapazität von Ressourcen kann Einschränkungen auf den Weg der Planung von Arbeitsgängen verursachen.
> - Sie können 0 (null) nicht als Arbeitsgangnummer verwenden. Die Nummer und reserviert und wird verwendet, um anzugeben, dass der letzte Arbeitsgang im Arbeitsplan keine Folgeaktivitätsarbeitsgang hat.

### <a name="parallel-operations"></a>Parallele Arbeitsgänge

Manchmal ist eine Kombination aus mehreren betrieblichen Ressourcen, die bestimmte Merkmale aufweisen, erforderlich, um einen Arbeitsgang auszuführen. Beispielsweise könnte ein Zusammenbauvorgang eine Maschine und ein Werkzeug erfordern, und eine Arbeitskraft, die zwei Maschinen beaufsichtigt für den Arbeitsgang. Dies kann z.B. modelliert werden, indem parallele Arbeitsgänge verwendet werden, bei denen ein Arbeitsgang ausgewählt ist, der der primäre Arbeitsgang ist und der andere der sekundäre ist.  

[![Arbeitsplan mit primären und sekundären Arbeitsgängen](./media/routes-and-operations-3-parallel-operations.png)](./media/routes-and-operations-3-parallel-operations.png)  

In der Regel stellt der primäre Arbeitsgang die Engpassressource dar, die die Bearbeitungszeit für die sekundären Arbeitsgänge definiert. Bei der Planung mit begrenzter Kapazität, muss die Ressourcen, für die geplant werden soll, für den primären Arbeitsgang und die sekundären Arbeitsgänge gleichzeitig verfügbar sein und die freie Kapazität haben.  

Der primäre Arbeitsgang und die sekundären Arbeitsgänge müssen die gleiche Arbeitsgangnummer (30 in der vorherigen Abbildung) verwenden.  

Im vorherigen Beispiel ist die Ressourcenanforderung für den primären Arbeitsgang (30) die Maschine, während die Ressourcenanforderungen für die sekundären Arbeitsgänge (30' und 30") Werkzeug und Arbeitskraft sind. Die Unterstützt einer fünfzigprozentigen Auslastung stellt sicher, dass die geplante die Arbeitskraft zwei Maschinen gleichzeitig überwachen kann.

### <a name="approval-of-routes"></a>Genehmigung der Arbeitspläne

Ein Arbeitsplan muss genehmigt werden, bevor er im Produktionsprozess verwendet werden kann. Die Genehmigung gibt an, dass das Arbeitsplandesign abgeschlossen wurde. Dasselbe freigegebene Produkt oder die freigegebene Variante des Produkts können mehrere genehmigter Arbeitspläne haben. In der Regel erfolgt die Genehmigung eines Arbeitsplans, wenn der erste entsprechende Arbeitsplan genehmigt wurde. In einigen Geschäftsszenarien ist die Genehmigung des Arbeitsplans und der Arbeitsplanversion jedoch separate Aktivitäten, die möglicherweise verschiedene Prozessbesitzer einbeziehen.  

Jeder Arbeitsplan kann separat genehmigt oder widerrufen werden. Beachten Sie, dass, wenn ein Arbeitsplan widerrufen ist, alle zugehörigen Arbeitsplanversionen auch widerrufen sind. In den Produktionssteuerungsparametern können Sie angeben, ob die Arbeitsplangenehmigung widerrufen werden kann und ob genehmigte Arbeitspläne geändert werden können.  

Wenn Sie ein Protokoll beibehalten müssen, das festhält, wer jeden Arbeitsplan genehmigt, können Sie elektronische Signaturen für Genehmigung des Arbeitsplans anfordern. Benutzer müssen anschließend ihre Identität bestätigen, indem sie [elektronische Signaturen](../../fin-and-ops/organization-administration/electronic-signature-overview.md) verwenden.

## <a name="operations"></a>Operations
Ein Arbeitsgang ist ein Schritt im Produktionsprozess. Jeder Arbeitsgang besitzt eine Kennung und eine einfache Beschreibung. Die folgenden Tabellen zeigt typische Beispiele für Arbeitsgänge einer Maschinenwerkstatt.

| Arbeitsgang  | Beschreibung        |
|------------|--------------------|
| PipeCut    | Rohrschnitt       |
| TIGweld    | TIG-Schweißen        |
| JigAssy    | Jig-Montage       |
| Prüfung | Qualitätsprüfung |

Die betrieblichen Eigenschaften eines Arbeitsgangs, wie Rüstzeit und die Bearbeitungszeit, Ressourcenanforderungen, Kalkulationsinformationen und Verbrauchsparameter werden über Arbeitsgangzuordnung angegeben. Weitere Informationen zu Arbeitsgangzuordnungen finden Sie im nächsten Abschnitt.

## <a name="operation-relations"></a>Arbeitsgangzuordnungen
Die betrieblichen folgenden Eigenschaften eines Arbeitsgangs werden auf der Arbeitsgangzuordnung verwaltet:

- Kostenarten
- Verbrauchsparameter
- Bearbeitungszeiten
- Verarbeitung von Mengen
- Ressourcenanforderungen
- Hinweise und Anweisungen

Sie können mehrere Arbeitsgangzuordnungen für denselben Arbeitsgang definieren. Allerdings ist jede Arbeitsgangzuordnung für einen Arbeitsgang bestimmt und speichert Eigenschaften, die einen Arbeitsplan, ein freigegebenes Produkt oder einer Gruppe von gemeinsamen Produkten gehören, die einer Artikelgruppe zugeordnet werden. Daher kann der gleiche Vorgang in mehreren Arbeitsplänen mit verschiedene betriebliche Eigenschaften verwendet werden. Darüber hinaus können Sie problemlos die Masterdaten beibehalten, wenn Sie normale Arbeitsgänge mit gleichen Eigenschaften nutzen, unabhängig von dem Arbeitsplan und dem Produkt. Der Umfang der Arbeitsgangzuordnung wird durch die Eigenschaften **Artikelcode**, **Artikelrelation**, **Arbeitsplancode** und **Arbeitsplanzuordnung** wie in der folgenden Tabelle dargestellt definiert.

| Artikelcode | Artikelrelation         | Arbeitsplancode | Arbeitsplanrelationscode   | Umfang der Arbeitsgangzuordnung                                                                                                                                                                                                                                                                              |
|-----------|-----------------------|------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tabelle     | &lt;Artikelkennung&gt;       | Arbeitsplan      | &lt;Routenkennung&gt; | Die betrieblichen Eigenschaften eines Arbeitsgangs, wenn er im Arbeitsplan verwendet wird (**Arbeitsplannummer**=&lt;Arbeitsplankennung&gt;) zur Produktion des Produkts im Feld **Artikelnummer**=&lt;Artikelkennung&gt;.                                                                                                                        |
| Tabelle     | &lt;Artikelkennung&gt;       | Alle        |                  | Die standardmäßige betrieblichen Eigenschaften eines Arbeitsgangs, zur Produktion des Produkts im Feld **Artikelnummer**=&lt;Artikelkennung&gt;. Das bedeutet, die betrieblichen Eigenschaften gelten, wenn es keine arbeitsplanspezifische Arbeitsgangzuordnung für das freigegebene Produkt gibt.                                     |
| Gruppieren     | &lt;Artikelgruppenkennung&gt; | Arbeitsplan      | &lt;Routenkennung&gt; | Die betrieblichen Eigenschaften eines Arbeitsgangs, wenn sie im Arbeitsplan mit der **Arbeitsplannummer**=&lt;Arbeitsplankennung&gt; zur Produktion von freigegebenen Produkten verwendet mit der Artikelgruppen &lt;Artikelgruppe&gt; verwendet werden, es sei denn, dass es eine arbeitsplanspezifische Arbeitsgangzuordnung für das freigegebene Produkt gibt.                         |
| Gruppieren     | &lt;Artikelgruppenkennung&gt; | Alle        |                  | Die betrieblichen Eigenschaften eines Arbeitsgangs, wenn er zur Produktion von freigegebenen Produkten verwendet wird, die einer Artikelgruppe mit &lt;Artikelgruppenkennung&gt; zugeordnet sind, es sei denn eine genauere Arbeitsgangzuordnung ist vorhanden.                                                                                                  |
| Alle       |                       | Arbeitsplan      | &lt;Routenkennung&gt; | Die standardmäßigen betrieblichen Eigenschaften des Arbeitsgangs, wenn dieser im Arbeitsplan mit **Arbeitsplannummer**=&lt;Arbeitsgangkennung&gt; verwendet wird. Das bedeutet, die betrieblichen Eigenschaften gelten, wenn es keine arbeitsplanspezifische für diesen Arbeitsgang für das freigegebene Produkt oder seine zugeordnete Artikelgruppe gibt. |
| Alle       |                       | Alle        |                  | Die standardmäßigen betrieblichen Eigenschaften eines Arbeitsgangs. Diese betrieblichen Eigenschaften gelten, wenn eine spezifischere Arbeitsplan nicht vorhanden ist.                                                                                                                                                                |

Sie können auch angeben, dass in einer Arbeitsgangzuordnung ein Standort besteht. Auf diese Weise können die betrieblichen Eigenschaften eines Arbeitsgangs abhängig vom Standort variieren wo der Arbeitsgang ausgeführt wird. Für konfigurierte Produkte können verschiedene Eigenschaften für jede betriebliche Produktkonfiguration angegeben werden.  

Arbeitsgangzuordnungen bietet viel Flexibilität, wenn Sie die Arbeitspläne definieren. Darüber senkt die Möglichkeit Standardeigenschaften zu definieren die Menge der zu verwaltenden Masterdaten. Allerdings bedeutet diese Flexibilität auch, dass Sie den Kontext berücksichtigen müssen, über den Sie eine Arbeitsgangzuordnung ändern.  

> [!NOTE]
> Da die betrieblichen Eigenschaften in Arbeitsgangzuordnungen für jeden Arbeitsgang und Arbeitsplan gespeichert werden, haben alle Instanzen desselben Arbeitsgangs (beispielsweise Montage) dieselbe Rüstzeit, Bearbeitungszeit undRessourcenanforderungen. Wenn zwei Begebenheiten eines Arbeitsgangs im gleichen Arbeitsplan auftreten, aber unterschiedliche Bearbeitungszeiten haben, müssen Sie zwei eindeutige Arbeitsgänge, wie Assembly1 und Assembly2 erstellen.

### <a name="modifying-product-specific-routes"></a>Ändern der produktspezifischen Arbeitspläne

Wenn Sie die **Arbeitsplan** Seite über die **Freigegebene Produkte** Seite öffnen, werden die Arbeitsplanversionen angezeigt, die dem ausgewählten freigegebenen Produkt zugeordnet sind. In diesem Zusammenhang zeigt Supply Chain Management für jeden Arbeitsgang die betrieblichen Eigenschaften aus der Arbeitsgangrelation, die am besten zu der Arbeitsplanversion passen. Beachten Sie, dass die Liste der Arbeitsgänge die **Artikelcode** und **Arbeitsplancode** Eigenschaften aus der Arbeitsgangzuordnung enthält. Daher kann bestimmt werden, welche Arbeitsgangzuordnung angezeigt wird.  

Auf der Seite **Arbeitsplan** können Sie die betrieblichen Eigenschaften des Arbeitsgangs, wie die Bearbeitungszeit oder die Kostenkategorien, ändern. Die Änderungen werden für die Arbeitsgangzuordnung gespeichert, die über den Arbeitsplan und das freigegebene Produkt festgelegt sind, auf die in die aktuelle Arbeitsplanversion verwiesen wird. Wenn die Arbeitsgangzuordnung, die angezeigt wird, nicht für den Arbeitsplan und das freigegebene Produkt festgelegt ist, erstellt das System eine Kopie der Arbeitsgangzuordnung. Die Kopie *ist* für den Arbeitsplan und das freigegebene Produkt spezifisch. Änderungen betreffen daher keine anderen Arbeitspläne oder freigegebene Produkte. Um zu prüfen, welche der Arbeitsgangzuordnung auf der **Arbeitsplan** Seite geändert wird, beachten Sie die **Artikelcode** und **Arbeitsplancode** Felder.  

Sie können einen Arbeitsgang auch manuell erstellen, die für einen Arbeitsplan und ein freigegebenes Produkt bestimmt ist, indem die **Kopieren und Bearbeiten** Beziehung Funktion verwenden.  

> [!NOTE]
> Wenn Sie einen neuen Arbeitsgang für einen Arbeitsplan auf der Seite **Arbeitsplan** hinzufügen, wird einer Arbeitsgangzuordnung nur für das aktuelle freigegebene Produkt erstellt. Wenn der Arbeitsplan verwendet wird, um andere freigegebene Produkte zu produzieren, besteht keine entsprechende Arbeitsgangzuordnung für freigegebene Produkte und der Arbeitsplan kann für diese freigegebene Produkte nicht mehr verwendet werden.

### <a name="maintaining-operation-relations-per-route"></a>Verwalten von Arbeitsgangzuordnungen pro Arbeitsplan

Wenn Sie die **Arbeitsplandetails** Seite aus der **Arbeitspläne** Listenseite öffnen, wird eine Liste aller Arbeitsgangzuordnungen, die auf den ausgewählten Arbeitsplan angewendet werden, angezeigt. Daher können Sie sich vergewissern, welche die betrieblichen Eigenschaften für Produkte verwendet werden. Sie können Standardeigenschaftswerte und produktspezifische Eigenschaftswerte ändern.  

Wenn Sie eine neue Arbeitsgangzuordnung auf der Seite **Arbeitsplandetails** hinzufügen, wird das **Arbeitsplancode** Feld automatisch auf **Arbeitsplan** festgelegt, und das **Arbeitsplanzuordnung** Feld wird mit der Arbeitsplannummer des aktuellen Arbeitsplans festgelegt.

### <a name="maintaining-operation-relations-per-operation"></a>Verwalten von Arbeitsgangzuordnungen pro Arbeitsgang

Von der **Arbeitsgänge** Seite können Sie die Seite **Arbeitsgangzuordnungen** öffnen. Auf dieser Seite können Sie alle Arbeitsgangzuordnungen für einen bestimmten Arbeitsgang ändern. Sie können Arbeitsgangzuordnungen auch ändern, der Standardwerte enthalten.  

Wenn Ihr Unternehmen Standardarbeitsgänge verwendet und die Arbeitsgangparameter identisch für allen Produkten und Prozessen sind, beinhaltet die **Arbeitsgangzuordnungen** Seite eine bequeme Möglichkeit, um die Eigenschaften von betrieblichen Arbeitsgänge zu verwaltet.

### <a name="applying-operation-relations"></a>Arbeitsgangzuordnungen anwenden

In einigen Fällen muss Supply Chain Management die betrieblichen Eigenschaften für einen Arbeitsgang finden. Wenn beispielsweise eine Bestellung erstellt wird, müssen die betrieblichen Eigenschaften einzelner Arbeitsgänge von Arbeitsgangzuordnungen dem Produktionsarbeitsplan kopiert werden. In solchen Fällen sucht Supply Chain Management die relevanten Arbeitsgangzuordnungen von der bestimmtesten Kombination bis zu unbestimmtesten Kombination.  

Wenn Supply Chain Management nach der für ein freigegebenes Produkt relevantesten Arbeitsgangrelation sucht, wird eine Arbeitsgangrelation, die der Artikelkennung des freigegebenen Produkts entspricht gegenüber einer Arbeitsgangrelation bevorzugt, die mit der Artikelgruppenkennung übereinstimmt. Eine Arbeitsgangzuordnung, die der Artikelgruppenkennung entspricht, wird gegenüber der Standardarbeitsgangzuordnung bevorzugt. Die Suchreihenfolge wird in der folgenden Tabelle veranschaulicht:

1.  **Artikelcode**=**Tabelle** und **Artikelrelation**=&lt;Artikelkennung&gt;
2.  **Artikelcode**=**Gruppe** und **Artikelrelation**=&lt;Artikelgruppenkennung&gt;
3.  **Artikelcode**=**Alle**
4.  **Arbeitsplancode**=**Arbeitsplan** und **Arbeitsplanzuordnung**=&lt;Arbeitsplankennung&gt;
5.  **Arbeitsplancode**=**Alle**
6.  **Konfiguration**=&lt;Konfigurationskennung&gt;
7.  **Konfiguration**=
8.  **Standort**=&lt;Standortkennung&gt;
9.  **Standort**=

Daher sollte ein Arbeitsgang nur einmal für jeden Arbeitsplan verwendet werden. Wenn der Arbeitsgang mehrmals im gleichen Arbeitsplan auftritt, haben alle Auftreten dieses Arbeitsgangs dieselbe Arbeitsgangzuordnung, und Sie können nicht verschiedene Eigenschaften (beispielsweise Bearbeitungszeiten) haben.

## <a name="route-versions"></a>Arbeitsplanversionen

Arbeitsplanversionen werden verwendet, um Abweichungen bei der Herstellung von Produkten gerecht zu werden, oder um eine stärkere Kontrolle über den Produktionsprozess zu ermöglichen. Sie definieren, welcher Arbeitsplan verwendet werden soll, wenn ein bestimmtes freigegebenes Produkt oder eine Variante des freigegebenen Produkts produziert wird. Sie können die folgenden Einschränkungen verwenden, um festzulegen, welche Arbeitsplanung für ein freigegebenes Produkt verwendet wird:

- Produktdimensionen (Größe, Farbe, Stil, Konfiguration)
- Produktionsmengen
- Produktionsstandort
- Produktionsdatum

Wenn Sie das Produkt an einen bestimmten Standort, in einer bestimmten Menge oder in einer bestimmten Periode erstellen, können Sie eine bestimmte Arbeitsplanversion als die Standardarbeitsplanversion auswählen. Beachten Sie, dass nur ein aktiver Arbeitsplan für ein gegebenes freigegebenes Produkt und einen vorgegebenen Reihe von Beschränkungen zulässig ist.  

In den Produktionssteuerungsparametern können Sie festlegen, dass die Gültigkeitsperiode einer Arbeitsplanversion immer angegeben wird.

### <a name="approval-of-route-versions"></a>Genehmigung des Arbeitsplanversionen

Ein Arbeitsplan muss genehmigt werden, bevor er im Produktionsprozess verwendet werden kann. Wenn Sie eine Arbeitsplanversion genehmigen, wird der Arbeitsplan automatisch genehmigt. Beachten Sie, dass, wenn ein Arbeitsplan nur genehmigt werden kann, wenn die zugehörigen Arbeitsplanversionen genehmigt ist.

### <a name="activating-the-default-route-version"></a>Aktivieren der Standardarbeitsplanversion

Wenn Sie eine Arbeitsplanversion aktivieren, legen Sie diese als die Standardarbeitsplanversion fest, die Masterplan verwendet oder der verwendet wird, um Produktionsaufträge zu generieren. Sie können nur eine aktive Arbeitsplanversion für einen vorgegebenen Reihe von Beschränkungen haben (z.B. Periode, Standort oder Menge). Sie erhalten eine Fehlermeldung, wenn die Version, die Sie aktivieren möchten, einen Konflikt mit einer Version ergibt, die bereits aktiv ist. Sie müssen dann entweder die Konflikt verursachende Version deaktivieren oder die Versionseinschränkungen für die Arbeitsplanversion (meist die Periode) ändern, um eine mehrdeutige Aktivierung zu verhindern.

### <a name="electronic-signatures"></a>Elektronische Signaturen

Wenn Sie ein Protokoll beibehalten müssen, das festhält, wer jeden Arbeitsplan genehmigt und aktiviert, können Sie elektronische Signaturen für Genehmigung des Arbeitsplans anfordern. Benutzer, die Arbeitsplanversionen genehmigen und aktivieren, müssen dann ihre Identität bestätigen, indem sie eine [elektronische Signatur](../../fin-and-ops/organization-administration/electronic-signature-overview.md) verwenden.

### <a name="product-change-that-uses-case-management"></a>Produktänderung mit Anfrageverwaltung

Der Produktänderungsfall zur Genehmigung und Aktivierung von neuen oder geänderten Arbeitspläne und Arbeitsplanversionen enthält eine einfache Möglichkeit, einen Überblick über die Arbeitsplanversionseinschränkungen anzuzeigen. Sie können auch alle Arbeitspläne genehmigen und aktivieren, die mit einer spezifischen Änderung in einem Arbeitsgang im Dokument und die Ergebnisse im Produkt zugeordnet werden.

## <a name="maintaining-routes"></a>Arbeitspläne verwalten

Abhängig von Ihren Geschäftsanforderungen könnten Sie den Aufwand reduzieren, der erforderlich ist, um die Prozeßdefinitionen verwalten.

### <a name="making-routes-independent-of-resources"></a>Arbeitsplan unabhängiger von Ressourcen gestalten

In vielen Systemen müssen die betriebliche Ressource oder Ressourcengruppen, die einen Arbeitsgang ausführen sollen, in einem im Arbeitsplan angegeben werden. In Supply Chain Management können Sie Bedingungen definieren, die eine betriebliche Ressource erfüllen muss, um für den Arbeitsgang in Frage zu kommen. Daher muss die betriebliche Ressource oder Ressourcengruppe, die verwendet werden soll, nicht festgelegt werden, bis der Vorgang tatsächlich geplant ist. Diese Funktion ist besonders nützlich, wenn Sie zahlreiche Arbeitskräfte oder Maschinen zu einer Gruppe zusammenfassen, die denselben Arbeitsgang ausführen können.  

Geben Sie beispielsweise an, dass ein Arbeitsgang eine betriebliche Ressource vom Typ **Maschine** erfordert, die eine **Stanzkraft** von 20 Tonnen hat. Das Planungsmodul löst diese Anforderungen in eine betriebliche Ressource oder Ressourcengruppe auf, wenn der Arbeitsgang geplant wird. Da Sie nur Anforderungen angeben können, anstatt den Vorgang mit einer bestimmten Maschine zu binden, sind Sie hiermit viel mehr Flexibel. Darüber hinaus ist die Verwaltung einfacher, wenn Ressourcen verschoben werden, oder neue Ressourcen hinzugefügt werden.  

Weitere Informationen zu den unterschiedlichen Arten von Ressourcenanforderungen und deren Nutzung finden Sie in "Anforderungen für betrieblichen Ressourcen" und [Ressourcenfunktionen](resource-capabilities.md).

### <a name="sharing-routes-across-sites"></a>Standortübergreifende Freigabe von Arbeitsplänen

Wenn Sie dasselbe Produkt an mehr als einen Produktionsstandort erzeugen und die Schritte für die Erstellung des Produkts identisch an allen Standorten sind, können Sie einen freigegebenen Arbeitsplan entwerfen, der allen Produktionsstandorten verwendet wird. Um einem freigegebenen Arbeitsplan zu erstellen, geben Sie kein Standort im Arbeitsplan selbst an. Sie müssen jedoch noch eine Arbeitsplanversion erstellen, die den freigegebenen Arbeitsplan dem Produkt an jedem Standort zuordnet.  

Stellen Sie außerdem sicher, ob die Ressourcenanforderungen für jeden Arbeitsgang im Arbeitsplan nicht betriebliche Ressourcen oder Ressourcengruppen benötigen, sondern stattdessen die Merkmale der erforderlichen Ressourcen angeben. Das Planungsmodul ist dann in der Lage, die entsprechenden betrieblichen Ressourcen dem Standort zuweisen, für dass die Produktion geplant wird. Wenn es beispielsweise geringfügige Unterschiede in der Laufzeit gibt, oder wenn die Rüstzeit für einen bestimmten Arbeitsgang standortspezifisch ist, können Sie diese Informationen angeben, indem Sie eine zusätzliche Arbeitsgangzuordnung für diesen Standort hinzufügen.  

Um den vollständigen Nutzen aus freigegebenen Arbeitsplänen zu ziehen, sollten Sie den Ressourcenverbrauch auf der jeweiligen Stückliste (BOM) verwenden. Ist der Option für den Ressourcenverbrauch auf der Stücklistenposition gesetzt, werden Lagerort und Lagerplatz von dem Rohmaterialien verbraucht werden aus der betrieblichen Ressource für die der Arbeitsgang geplant ist abgeleitet. Daher müssen der Lagerort und der Lagerplatz nicht ermittelt werden, solange die Produktion tatsächlich geplant ist. Auf diese Weise können Sie die Stückliste und den Arbeitsplan unabhängigen vom physischen Standort erstellen, in dem das Produkt hergestellt wird.

### <a name="standard-operation-relations"></a>Standard-Arbeitsgangzuordnungen

Wenn Ihr Unternehmen standardisierte Arbeitsgänge für die Produktion verwendet und wenn es wenig oder keine Änderung der Rüstzeit, Bearbeitungszeit, Verbrauchsberechnung, Kostenberechnung usw. gibt, kann es nützlich sein Standardarbeitsgangzuordnungen für alle Arbeitsgänge zu erstellen. In diesem Fall vermeiden Sie Arbeitsgangzuordnungen zu erstellen, die für einen beliebigen Arbeitsplan oder ein freigegebenes Produkt sind.  

Wenn Sie außerdem Ressourcenanforderungen hinsichtlich Qualifikation und Funktionen ausdrücken, und Ihre Arbeitspläne Standort-unabhängig erstellen, können Sie die Verwaltung der Geschäftsprozesse auf ein Mindestmaß beschränken.  

Wenn Sie diesen Ansatz verwenden, wird die Seite **Arbeitsgangzuordnungen** Ihr primäres Ziel für Verwaltungsaufgaben zur Laufzeit und anderer allgemeiner Eigenschaften.

### <a name="resource-specific-process-times"></a>Ressourcenspezifische Bearbeitungszeiten

Wenn Sie keine betriebliche Ressourcen oder eine Ressourcengruppe als Teil der Ressourcenanforderungen für einen Arbeitsgang angegeben, arbeiten möglicherweise die entsprechenden Ressourcen mit unterschiedlichen Geschwindigkeiten. Daher kann die Dauer, die erforderlich ist, um einen Arbeitsgang zum Verarbeiten, abweichen. Zur Behebung dieses Problems, können Sie das Feld **Formel** in der Arbeitsgangzuordnung verwenden, um die Berechnung von Zeitintervall festzulegen. Die folgenden Optionen sind verfügbar:

- **Standard** – (Standardeinstellung) Die Berechnung verwendet nur die Felder aus der Arbeitsgangzuordnung und multipliziert die angegebene Bearbeitungszeit und die Auftragsmenge.
- **Kapazität** – Die Berechnung umfasst das **Kapazität** Feld aus der betrieblichen Ressource. Daher ist die Zeit ressourceabhängig. Der Wert, der in dieser betrieblichen Ressource angegeben wird, ist Kapazität pro Stunde. Die **Prozesszeit** wird berechnet als **Bestellmenge** geteilt durch **Kapazität**.
- **Charge** – Eine Chargenkapazität wird berechnet, indem die Informationen aus der Arbeitsgangzuordnung verwendet werden. Die Anzahl von Chargen und daher die Bearbeitungszeit können auf Basis der Auftragsmenge dann berechnet werden.
- **Ressourcencharge** – Diese Option ist grundlegend die gleiche wie die **Charge** Option. Allerdings umfasst die Berechnung das **Chargenkapazität** Feld aus der betrieblichen Ressource. Daher ist die Zeit ressourceabhängig.

### <a name="set-up-route-groups"></a>Arbeitsplangruppen einrichten

Sie können die Arbeitsplangruppen und die Einstellungen für den Stellentyp unter **Produktionssteuerung > Einrichten > Arbeitspläne > Arbeitsplangruppen** definieren. Für jeden Plan/Stellentyp in der Arbeitsplangruppe können Sie die folgenden Optionen aktivieren oder deaktivieren:

- **Aktivierung** - Wählen Sie diese Option, um die Berechnungen und die Planung für den ausgewählten Stellentyp zu aktivieren und Stellenfeedback zu erhalten, wenn Sie die Stellenplanung ausführen. Sie müssen diese Option aktivieren, um den Stellentyp zu aktivieren, und anschließend wählen Sie die verbleibenden Optionen für diesen Stellentyp aus. Wenn die Aktivierung nicht ausgewählt ist, wird dieser Stellentyp nicht aktiviert, unabhängig von der Auswahl der anderen Optionen. 
- **Stellenverwaltung** - Wählen Sie diese Option, um den Stellentyp in der Stellenverwaltung einzubeziehen, wenn Sie die Stellenplanung ausführen. 
- **Arbeitszeit** - Wählen Sie diese Option, um den Stellentyp gemäß dem Arbeitszeitkalender zu planen, der für die betriebliche Ressource definiert ist, sonst verwenden Sie den gregorianischen Kalender. Arbeitszeit kann entweder über den gregorianischen Kalender oder über die festgelegte Arbeitszeit geplant werden. Wenn Sie diese Option auswählen, ist die Planung auf Grundlage des definierten Arbeitszeitkalender. Außerdem wird der Einzelvorgang des Einzelvorgangstyps vom Einzahlungen auf das Datum geplant, das als Startdatum des Einzelvorgangs definiert ist.
- **Kapazität** - Wählen Sie diese Option, um Kapazität für den Stellentyp zu reservieren, wenn Sie die Stellenplanung ausführen. Wenn Sie diese Option auswählen wird die Kapazität für den ausgewählten Jobtyp reserviert. Dadurch erhalten Sie einen Überblick darüber, welche Joptypen in jeder Arbeitsganggruppenverwendung die betrieblichen Ressourcen verwendet. Beispielsweise In einer Situation, in der Trockenarbeitsgänge Engpassressourcen sind, müssen diese Ressourcen ls Engpässe angegeben werden. Trocknende Arbeitsgänge, die den Wartezeit-Einzelvorgangstypen zugewiesen werden, reservieren Trockenarbeitsgänge. 

Für jeden der Stellentypen müssen Sie zunächst aktivieren oder deaktivieren. Wenn deaktiviert, wird keine der anderen Einrichtungen (Stellenverwaltung, Arbeitszeit und Kapazität) berücksichtigt, da der Stellentyp nicht aktiv ist. 

Unter den Stellentypen finden Sie Überschneidungen. Überschneidungen lassen verschiedene Einzelvorgänge zu, die gleichzeitig ausgeführt werden. Wenn Einzelvorgänge überlappend sind, können die Ressourcen verwendet werden, können aber nicht für bestimmte Einzelvorgänge reserviert werden.
Wenn für Aktivierung für das Überschneiden ausgewählt wird, hat der Rest Einstellungen (Stellenverwaltung, Arbeitszeit und Kapazität) keine Auswirkungen in der Arbeitsplangruppe. 

> [!NOTE]
> Wenn Sie Versionen aktualisieren, werden möglicherweise folgende Fehler angezeigt: **"CRL Fehler aufgetreten, während das Planungsmodul aufgerufen wird"**. Wenn Sie diesen Fehler erhalten, gehen Sie zur Seite **Arbeitsplangruppen**. Löschen Sie für alle Arbeitspläne, in denen Sie **Überlappen** aktiviert haben, die Option **Stellenverwaltung** **Arbeitszeit** und **Kapazität**. 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Stücklisten und Formeln](bill-of-material-bom.md)

- [Kostenkategorien in Produktionsrouting](../cost-management/cost-categories-used-production-routings.md)

- [Ressourcenfähigkeiten](resource-capabilities.md)

- [Elektronische Signatur – Überblick](../../fin-and-ops/organization-administration/electronic-signature-overview.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]