---
title: "Arbeitspläne und Arbeitsgänge"
description: "Dieses Thema enthält Informationen zu Arbeitsplänen und Arbeitsgängen. Ein Arbeitsplan definiert den Prozess für die Produktion eines Produkts oder die Produktvariante. Er wird beschrieben jeden Arbeitsgang) (Schritt im Produktionsprozess und im Auftrag, dass diese Schritte ausgeführt werden müssen. Für jeden Schritt definiert der Arbeitsplan auch erforderliche betrieblichen Ressourcen, die Zeit der erforderlichen Einstellungen und die Bearbeitungszeit sowie wie die Kosten berechnet werden sollen."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMDesigner, BOMDesignerRouteVersion, Route, RouteInventProd, RouteOpr, RouteOprTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 268124
ms.assetid: f78d5836-3e71-42b7-a5d1-41f19228d9d2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 556b9859d0b162b11f0bcbfc6552f6fd9a900596
ms.lasthandoff: 03/31/2017


---

# <a name="routes-and-operations"></a>Arbeitspläne und Arbeitsgänge

Dieses Thema enthält Informationen zu Arbeitsplänen und Arbeitsgängen. Ein Arbeitsplan definiert den Prozess für die Produktion eines Produkts oder die Produktvariante. Er wird beschrieben jeden Arbeitsgang) (Schritt im Produktionsprozess und im Auftrag, dass diese Schritte ausgeführt werden müssen. Für jeden Schritt definiert der Arbeitsplan auch erforderliche betrieblichen Ressourcen, die Zeit der erforderlichen Einstellungen und die Bearbeitungszeit sowie wie die Kosten berechnet werden sollen.

<a name="overview"></a>Überblick
--------

Ein Arbeitsplan beschreibt die Reihenfolge der Arbeitsgänge, der erforderlich ist, um ein Produkt oder eine ausgewählte Produktvariante zu erzeugen. Für jeden Arbeitsgang definiert auch der Arbeitsplan die betrieblichen Ressourcen vertraut, die erforderlich sind, die Zeit, die benötigt wird, um den Arbeitsgang einrichten und ausführen, und wie Kosten berechnet werden sollen. Sie können dieselben Arbeitsplan verwenden, um mehrere Produkte anzuzeigen, oder Sie können einen eindeutigen Arbeitsplan für jedes Produkt oder Produktvariante definieren. Sie können mehrere Arbeitspläne für das gleiche Produktdimensionsgruppe sogar haben. In diesem Fall ist der Arbeitsplan, der verwendet wird, hängt von Faktoren wie der Menge, die produziert werden muss. Die Definition eines Arbeitsplans in Microsoft Dynamics 365 für Arbeitsgänge besteht aus vier verschiedenen Elemente, die zusammen den Produktionsprozess beschrieben wird:

-   ** Arbeitsplan ** – ein Arbeitsplan definiert die Struktur des Produktionsprozesses. Das bedeutet, er definiert die Reihenfolge der Arbeitsgänge.
-   ** Arbeitsgang ** – ein Arbeitsgang gibt einen Schritt in einem benannten Arbeitsplan, z ** Assembly **. Der gleiche Vorgang kann in mehreren Arbeitsplänen auftreten und unterschiedliche Arbeitsgangnummern haben.
-   ** Arbeitsgangzuordnung ** – einer Arbeitsgangzuordnung definiert die betrieblichen Eigenschaften eines Arbeitsgangs, die wie Rüstzeit und die Bearbeitungszeit, Kostenkategorien, Verbrauchsparameter und Ressourcenanforderungen. Die betrieblichen Arbeitsgangzuordnung aktiviert die Eigenschaften eines Arbeitsgangs, um, je nach spezifischem Arbeitsplan zu variieren, dass der Arbeitsgang unter oder die Produkte verwendet wird, die produziert werden.
-   ** ** Arbeitsplanversion – Eine Arbeitsplanversion definiert den Arbeitsplan, der verwendet wird, um ein Produkt oder eine ausgewählte Produktvariante zu erzeugen. Arbeitsplanversionen aktivieren zu Produkten wiederverwendet werden die Arbeitsplan-Einzelvorgänge, oder, im Zeitverlauf geändert wurden. Sie ermöglichen auch die unterschiedlichen, um dem gleichen Produkt zu erzeugen, Arbeitspläne verwendet werden. In diesem Fall ist der Arbeitsplan, der verwendet, ist von Faktoren wie den Speicherort ab bzw. die Menge, die produziert werden müssen.

## <a name="routes"></a>Arbeitspläne
Ein Arbeitsplan beschreibt die Reihenfolge der Arbeitsgänge, der verwendet wird, um ein Produkt oder eine ausgewählte Produktvariante zu erzeugen. Jeder Arbeitsgang wird eine Arbeitsgangnummer und einen Folgeaktivitätsarbeitsgang zugewiesen. Die Reihenfolge der Arbeitsgangsformularen Arbeitsplan-Netzwerk ein, das nach einem verwiesenes Diagramm dargestellt werden kann, das ein oder mehrere Startpunkte und für einen bestimmten Endpunkt hat. In Dynamics 365 für Arbeitsgänge werden, Arbeitspläne Basierend auf dem Typ der Struktur unterschieden. Die zwei Typen der Arbeitspläne sind einfache Arbeitspläne und Arbeitsplan-Netzwerken. In den Produktionssteuerungsparametern können Sie angeben, ob nur einfache Arbeitspläne verwendet werden können oder ob die komplexeren Arbeitsplan-Netzwerken verwendet werden können.

### <a name="simple-routes"></a>Einfache Arbeitspläne

Ein einfacher Arbeitsplan fortlaufend ist, und es ist nur einen Startpunkt für den Arbeitsplan.  

einfacher Arbeitsplan ([] (![. /media/routes-and-operations-1-simple-route.png)]". /media/routes-and-operations-1-simple-route.png)  

Wenn Sie nur einfache Arbeitspläne in den Produktionssteuerungsparametern aktivieren, generiert Dynamics 365 für Arbeitsgänge automatisch die Arbeitsgangnummern (10,20,30 usw.), wenn Sie den Arbeitsplan.

### <a name="route-networks"></a>Arbeitsplan-Netzwerken

Wenn Sie die Produktionssteuerungsparametern komplexeren Arbeitsplan-Netzwerken in den aktivieren, können Sie Arbeitspläne definieren, die mehrere Startpunkte haben und Arbeitsgängen, die gleichzeitig ausgeführt werden können.  

[![Route network](./media/routes-and-operations-2-route-network.png)](./media/routes-and-operations-2-route-network.png)  

**Hinweise:**

-   Jeder Arbeitsgang kann nur einen Folgeaktivitätsarbeitsgang haben, und der Ganzarbeitsplan muss in einem einzigen Arbeitsgang beendet.
-   Es gibt keine Garantie, dass mehrere Arbeitsgänge, die den gleichen Folgeaktivitätsarbeitsgang haben (z Arbeitsgänge, 30 und 40 in der Abbildung) vorhergehenden tatsächlich parallel ausgeführt werden. Die Verfügbarkeit und die Kapazität von Ressourcen können kann Einschränkungen auf den Weg, dass Arbeitsgänge geplant werden.
-   Sie können 0 (null) nicht als Arbeitsgangnummer verwenden. Die Nummer und reserviert ist, wird verwendet, um anzugeben, dass der letzte Arbeitsgang im Arbeitsplan keine Folgeaktivitätsarbeitsgang hat.

### <a name="parallel-operations"></a>Gleichzeitig ausgeführte Arbeitsgänge

Manchmal ist eine Kombination aus mehreren betrieblichen Ressourcen, die bestimmte Merkmale aufweisen, erforderlich, um einen Arbeitsgang auszuführen. Beispielsweise könnte es eine Assemblierung eine Maschine und ein Werkzeug, eine Arbeitskraft, damit jede zwei Maschinen beaufsichtigen den Arbeitsgang. Dies kann z modelliert werden, indem parallele Arbeitsgänge verwendet, in dem ein Arbeitsgang ausgewählt ist, da der primäre Arbeitsgang und die anderen sekundär sind.  

[![Arbeitsplan, die primäre und sekundäre Arbeitsgänge hat] ". /media/routes-and-operations-3-parallel-operations.png)]". /media/routes-and-operations-3-parallel-operations.png)  

In der Regel stellt der primäre Arbeitsgang die Engpassressource dar und in die geschrieben wird die Bearbeitungszeit für die sekundären Arbeitsgänge vor. Allerdings bei der Planung die, betrifft, muss von begrenzten Kapazität, die Ressourcen, die für geplant werden, der primäre Arbeitsgang und die sekundären Arbeitsgänge gleichzeitig verfügbar sein und die Kapazität nicht zugesicherten haben.  

Müssen der primäre Arbeitsgang und die sekundären Arbeitsgänge die gleiche Arbeitsgangnummer (30 in der vorherigen Abbildung) verwenden.  

Im vorherigen Beispiel ist die Ressourcenanforderung für den primären Arbeitsgang (30) der Maschine, während die Ressourcenanforderungen für die sekundären Arbeitsgänge ('30 und 30 ") als Tool und die Arbeitskraft sind. Unterstützt einer FünfzigProzent-Auslastung sicherzustellen, dass geplante die Arbeitskraft zwei Maschinen gleichzeitig haben kann.

### <a name="approval-of-routes"></a>Genehmigung der Arbeitspläne

Ein Arbeitsplan muss genehmigt werden, bevor sie in der Planung oder im Produktionsprozess verwendet werden kann. Genehmigung gibt an, dass das Arbeitsplandesign abgeschlossen wurde. Dasselbe freigegebene Produkt oder freigegebene Variante des Produkts können mehrere genehmigter Arbeitspläne haben. In der Regel erfolgt Genehmigung eines Arbeitsplans auf, wenn die erste entsprechende Arbeitsplanversion genehmigt wurde. Geschäftsszenarien, jedoch in manchen sind die Genehmigung des Arbeitsplans und der Arbeitsplanversion separate Aktivitäten, die möglicherweise über verschiedene miteinbezögen Prozessbesitzer.  

Jeder Arbeitsplan getrennt kann genehmigt oder widerrufen werden. Beachten Sie jedoch, dass, wenn ein Arbeitsplan widerrufen ist, auf alle diesbezüglichen Arbeitsplanversionen auch widerrufen werden. In den Produktionssteuerungsparametern können Sie angeben, ob Arbeitspläne Genehmigung widerrufen werden kann und ob genehmigte Arbeitspläne geändert werden können.  

Wenn Sie ein Protokoll beibehalten müssen das Datensätze, die jeden Arbeitsplan genehmigt, können Sie elektronische Signaturen anfordern für Genehmigung des Arbeitsplans. Benutzer müssen anschließend ihre Identität bestätigen, indem sie verwenden elektronische Signatur [] (/dynamics365/operations/organization-administration/electronic-signature-overview).

## <a name="operations"></a>Handelsrechtl. Buchung
Ein Arbeitsgang handelt es sich um einen Schritt im Produktionsprozess. In Dynamics 365 für Arbeitsgänge, besitzt jeder Arbeitsgang eine Kennung und eine einfache Beschreibung. Die folgenden Tabellen sind typische Beispiele für Arbeitsgänge von einer Maschinenwerkstatt angezeigt.

| Arbeitsgang  | Beschreibung        |
|------------|--------------------|
| PipeCut    | Pipeausschnitt       |
| TIGweld    | Tig-Schweißen        |
| JigAssy    | Spannvorrichtungsassembly       |
| Prüfung | Qualitätsprüfung |

Die betrieblichen Eigenschaften des Arbeitsgangs, die wie Rüstzeit und die Bearbeitungszeit, Ressourcenanforderungen, Verbrauchsberechnung und Nachkalkulationsinformationen, werden für die Arbeitsgangzuordnung angegeben. (Weitere Informationen zu Arbeitsgangzuordnungen, finden Sie im nächsten Abschnitt.)

## <a name="operation-relations"></a>Arbeitsgangzuordnungen
Die betrieblichen folgenden Eigenschaften eines Arbeitsgangs auf der Arbeitsgangzuordnung verwaltet werden:

-   Kostenarten
-   Verbrauchsparameter
-   Bearbeitungszeiten
-   Verarbeitung von Mengen
-   Ressourcenanforderungen
-   Hinweise und Anweisungen

Sie können mehrere Arbeitsgangzuordnungen für denselben Arbeitsgang definieren. Allerdings ist jede Arbeitsgangzuordnung einem Arbeitsgang bestimmt und speichert Eigenschaften, die einem Arbeitsplan, in ein freigegebenes Produkt oder zu einer Gruppe von gemeinsamen Produkten handelt, die einer Artikelgruppe zugeordnet werden. Daher kann der gleiche Vorgang in mehreren Arbeitsplänen verwendet werden, mit denen verschiedene betriebliche Eigenschaften. Darüber hinaus können Sie problemlos die Masterdaten beibehalten, wenn Sie Normalbetriebe, die betrieblichen besitzen die gleichen Eigenschaften, unabhängig von den Arbeitsplan, der verwendet wird und Produkt verwenden, die produziert wird. Der Umfang der Arbeitsgangzuordnung wird durch ** Artikelcode **, ** Artikelrelation **, ** Arbeitsplancode ** und ** Arbeitsplanzuordnung ** Eigenschaften, wie in der folgenden Tabelle dargestellt definiert.

| Artikelcode | Artikelrelation         | Arbeitsplancode | Arbeitsplanrelationscode   | Umfang der Arbeitsgangzuordnung                                                                                                                                                                                                                                                                              |
|-----------|-----------------------|------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tabelle     | &lt;Artikelkennung&gt;       | Arbeitsplan      | &lt;Routenkennung&gt; | Die betrieblichen Eigenschaften eines Arbeitsgangs, wenn sie in der Arbeitsplanverwendet hat, wo ** Arbeitsplannummer **=&lt;Arbeitsplankennung das freigegebene&gt; Produkt im Feld Artikelnummer ** **=erzeugt&lt;.&gt;                                                                                                                        |
| Tabelle     | &lt;Artikelkennung&gt;       | Alle        |                  | Die Eigenschaften von betrieblichen eines Arbeitsgangs, wenn sie verwendet wird, um das freigegebene Produkt zu erzeugen im Feld Artikelnummer ** **=&lt;Artikelkennung&gt;. Das bedeutet, gelten die betrieblichen Eigenschaften zu, wenn keine Arbeitsplanbesonderearbeitsgangzuordnung für das freigegebene Produkt gibt.                                     |
| Gruppieren     | &lt;Artikels-bit für Dauerauftragsgruppen&gt; | Arbeitsplan      | &lt;Routenkennung&gt; | Die betrieblichen Eigenschaften eines Arbeitsgangs, wenn sie in der Arbeitsplanverwendet hat, wo ** Arbeitsplannummer **=&lt;Arbeitsplankennung freigegebene Produkte&gt; verwendet wird, die mit Artikelgruppenartikels-bit der Einzelhandelsgruppe zugeordnet &lt;werden, es&gt;sei denn, dass eine Arbeitsplanbesonderearbeitsgangzuordnung für das freigegebene Produkt gibt.                         |
| Gruppieren     | &lt;Artikels-bit für Dauerauftragsgruppen&gt; | Alle        |                  | Die Eigenschaften von betrieblichen eines Arbeitsgangs, wenn diese Anlagenbuchungsart verwendet hat, um anrechenbare Produkte anzuzeigen, die mit Artikelgruppenartikels-bit der &lt;Einzelhandelsgruppe zugeordnet werden, es sei denn, für&gt;eine Einzelgeschäftrelation mehr vorhanden ist.                                                                                                  |
| Alle       |                       | Arbeitsplan      | &lt;Routenkennung&gt; | Die betrieblichen Eigenschaften des Standards des Arbeitsgangs, wenn diese im Arbeitsplan in Feld Arbeitsplannummer ** **=Kennung&lt;Arbeitsplan verfügt&gt; Das bedeutet, gelten die betrieblichen Eigenschaften zu, wenn keine Arbeitsgangzuordnung für diesen Arbeitsplan vorhanden, der entweder auf den freigegebenen Produkt oder dessen zugeordnete Artikelgruppe besteht. |
| Alle       |                       | Alle        |                  | Die Eigenschaften von betrieblichen eines Arbeitsgangs. Diese Eigenschaften betrieblichen gelten, wenn eine Einzelgeschäftrelation nicht mehr vorhanden ist.                                                                                                                                                                |

Sie können auch angeben, dass einer Arbeitsgangzuordnung einem Standort besteht. Auf diese Weise können die betrieblichen Eigenschaften eines Arbeitsgangs, abhängig vom Standort (das heißt, der Standort) variieren wo der Arbeitsgang ausgeführt wird. Für konfigurierte Produkte können verschiedene Eigenschaften für jede betriebliche Produktkonfiguration auch angeben.  

Arbeitsgangzuordnungen geben Sie viele Flexibilität, wenn die Arbeitspläne definieren. Darüber hinaus reduzieren die Möglichkeit, Standardeigenschaftenhilfen definieren den Betrag von Masterdaten, die Sie verwalten. Allerdings bedeutet dies Flexibilität auch, dass Sie den Kontext müssen Sie berücksichtigen, dass einer Arbeitsgangzuordnung in ändern.  

** Hinweis: ** Da die betrieblichen Eigenschaften gespeicherte Beziehungen wirksam pro Arbeitsgang pro Arbeitsplan basieren, besitzt alle Auftreten desselben Arbeitsgangs (beispielsweise), Montage dieselbe Rüstzeit, Bearbeitungszeit, Ressourcenanforderungen, usw. Wenn zwei Auftreten eines Arbeitsgangs im gleichen Arbeitsplan auftreten aber unterschiedliche Bearbeitungszeiten haben muss, müssen Sie zwei Assembly1 eindeutige Arbeitsgänge, wie und Assembly2 erstellen.

### <a name="modifying-product-specific-routes"></a>Ändern der produktspezifischen Arbeitsplänen

Wenn Sie die ** Arbeitsplan ** Seite aus der ** freigegebene Produkte ** Seite öffnen, Arbeitsplanversionen werden, die dem ausgewählten zugeordnet sind, gemeinsam verwendete Produktdimensionsgruppe angezeigt. In diesem Zusammenhang für jeden Arbeitsgang werden, Dynamics 365 für Arbeitsgänge den Eigenschaften von betrieblichen der Arbeitsgangzuordnung besten zu die Arbeitsplanversion angezeigt. Beachten Sie, dass die Liste der Arbeitsgänge ** Artikelcode ** und ** Arbeitsplancode ** Eigenschaften aus der Arbeitsgangzuordnung enthält. Daher kann bestimmt werden, welche Arbeitsgangzuordnung angezeigt wird.  

** Arbeitsplan ** Auf der Seite können Sie die betrieblichen Eigenschaften des Arbeitsgangs, wie die Bearbeitungszeit die Kostenkategorien oder ändern. Die Änderungen werden für die Arbeitsgangzuordnung gespeichert, die dem Arbeitsplan und den gemeinsam verwendete Produktdimensionsgruppe bestimmt ist, die in die aktuelle Arbeitsplanversion verwiesen wird. Wenn die Arbeitsgangzuordnung, die angezeigt wird, nicht an den Arbeitsplan und den gemeinsam verwendete Produktdimensionsgruppe bestimmt ist, müssen die Änderungen gespeichert ist, erstellt das System eine Kopie der Arbeitsgangzuordnung. Dieses *is* Kopie enthält den Arbeitsplan und den gemeinsam verwendete Produktdimensionsgruppe. Daher Änderungen betreffen die keinen anderen Arbeitsplan oder freigegebene Produkte. Um sicherzustellen welche der Arbeitsgangzuordnung auf geändert wird ** Arbeitsplan ** Seite, beachten Sie ** Artikelcode ** und ** Arbeitsplancode ** Felder.  

Sie können einen Arbeitsgang auch manuell erstellt werden, die einem Arbeitsplan und in ein freigegebenes Produkt bestimmt ist, indem die ** Kopieren und Bearbeiten Beziehung ** Funktion verwendet.  

** Hinweis: ** Wenn Sie einen neuen Arbeitsgang einen Arbeitsplan auf der Seite ** Arbeitsplan ** hinzufügen, wird einer Arbeitsgangzuordnung nur für das aktuelle freigegebene Produkt erstellt. Wenn auch der Arbeitsplan verwendet wird, um andere freigegebene Produkte zu produzieren, besteht keine entsprechende für die Arbeitsgangzuordnung Freigegebene Produkte ", und der Arbeitsplan kann für diese freigegebene Produkte nicht mehr verwendet werden.

### <a name="maintaining-operation-relations-per-route"></a>Wartungsarbeitsgangzuordnungen pro Arbeitsplan

Wenn Sie die ** Arbeitsplandetails ** Seite aus der Arbeitspläne ** ** Listenseite öffnen, wird eine Liste aller Arbeitsgangzuordnungen, die auf den ausgewählten Arbeitsplan angewendet werden, angezeigt. Daher können Sie sich vergewissern, die betrieblichen Eigenschaften, bei denen Produkte. Sie können Standardeigenschaftswerte und Eigenschaftswerte produktspezifische ändern.  

Wenn Sie eine neue Arbeitsgangzuordnung auf der Seite ** Arbeitsplandetails ** hinzufügen, wird das ** Arbeitsplancode ** Feld automatisch auf festgelegt ** Arbeitsplan **, und das ** Arbeitsplanzuordnung ** Feld wird mit der Arbeitsplannummer des aktuellen Arbeitsplans festgelegt.

### <a name="maintaining-operation-relations-per-operation"></a>Wartungsarbeitsgangzuordnungen pro Arbeitsgang

Von der Arbeitsgänge ** ** Seite können Sie die Seite öffnen ** ** Arbeitsgangzuordnungen. Auf dieser Seite können Sie alle Arbeitsgangzuordnungen für einen bestimmten Arbeitsgang ändern. Sie können Arbeitsgangzuordnungen auch ändern, der Standardwerte enthalten.  

Wenn Ihr Unternehmen Normalbetriebe verwendet und bei den Arbeitsgangparametern identisch zu allen Produkten und Prozessen sind, beinhaltet die ** Arbeitsgangzuordnungen ** Seite hervorragend, die Eigenschaften von betrieblichen dieser Arbeitsgänge verwaltet.

### <a name="applying-operation-relations"></a>Anwenden von Arbeitsgangzuordnungen

In einigen Fällen muss Dynamics 365 für Arbeitsgänge die betrieblichen Eigenschaften für einen Arbeitsgang finden. Wenn beispielsweise eine Bestellung erstellt wird, müssen die betrieblichen Eigenschaften einzelner Arbeitsgänge von Arbeitsgangzuordnungen dem Produktionsarbeitsplan kopiert werden. In solchen Fällen findet Dynamics 365 für Arbeitsgänge die relevanten Arbeitsgangzuordnungen von der bestimmtsten Kombination mit der kürzesten bestimmten Kombination.  

Wenn Dynamics 365 für Arbeitsgangssuchen für die Arbeitsgangzuordnung relevantste für ein freigegebenes Produkt, einer Arbeitsgangzuordnung, die, entspricht die Artikelkennung des Produkts über freigegebenen einer Arbeitsgangzuordnung bevorzugt verwendet wird, die das Artikels-bit für Dauerauftragsgruppen übereinstimmt. Der wird wiederum einer Arbeitsgangzuordnung, die das Artikels-bit für Dauerauftragsgruppen übereinstimmt, zu der Standardarbeitsgangzuordnung bevorzugt. Die Suche ist in der folgenden Reihenfolge ausgeführt:

1.  ** Artikelcode **=** Tabelle ** und ** Artikelrelation **=&lt;Artikelkennung&gt;
2.  ** Artikelcode **=** Gruppe ** und ** Artikelrelation **=&lt;Artikels-bit für Dauerauftragsgruppen&gt;
3.  ** Artikelcode ** ** ** alle =
4.  ** Arbeitsplancode **=** Arbeitsplan ** und ** Arbeitsplanzuordnung **=&lt;Arbeitsplankennung&gt;
5.  ** Arbeitsplancode ** ** ** alle =
6.  ** Konfiguration ** Konfigurationskennung =&lt;&gt;
7.  **Configuration**=
8.  ** Standort **=&lt;Standortkennung&gt;
9.  **Site**=

Daher sollte ein Arbeitsgang verwendet werden nur einmal für jeden Arbeitsplan. Wenn der Arbeitsgang mehrmals im gleichen Arbeitsplan auftritt, wird alle Auftreten dieses Arbeitsgangs dieselbe Arbeitsgangzuordnung, und Sie können die Taxonomie nicht, verschiedene Eigenschaften, (beispielsweise) Bearbeitungszeiten Auftreten für jedes zu haben.

## <a name="route-versions"></a>Arbeitsplanversionen
Arbeitsplanversionen werden verwendet, um Abweichungen bei der Herstellung von Produkten gerecht zu werden oder eine bessere Kontrolle über den Produktionsprozess zu ermöglichen. Sie definieren die, Arbeitsplan verwendet werden soll, wenn ein bestimmtes freigegebenes Produkt oder eine Variante des Produkts freigegebenen produziert wird. Sie können die folgenden Einschränkungen verwenden, um festzulegen, die Arbeitsplanung für ein freigegebenes Produkt verwendet wird:

-   Produktdimensionen (Größe, Farbe, Stil oder Konfiguration)
-   Produktionsmenge
-   Verteilzentrum
-   Anfangsdatum

Wenn Sie das Produkt an einen bestimmten Standort, in einer bestimmten Menge oder in einer bestimmten Periode erstellen, können Sie eine bestimmte Arbeitsplanversion als die Standardarbeitsplanversion auswählen. Allerdings Beachten Sie, dass nur ein aktiver Arbeitsplan für ein gegebenes freigegebenes Produkt und einen vorgegebenen Reihe von Beschränkungen zulässig ist.  

In den Produktionssteuerungsparametern können Sie festlegen, dass die Gültigkeitsperiode einer Arbeitsplanversion immer angegeben wird.

### <a name="approval-of-route-versions"></a>Genehmigung von Arbeitsplanversionen

Bevor eine Arbeitsplanversion in der Planung oder im Produktionsprozess verwendet werden kann, muss sie genehmigt werden. Wenn Sie eine Arbeitsplanversion genehmigen, können Sie dem zugehörigen Arbeitsplan auch genehmigen. Beachten Sie jedoch, dass einer Arbeitsplanversion genehmigt werden kann, wenn der zugehörige auch Arbeitsplan genehmigt wurde.

### <a name="activating-the-default-route-version"></a>Aktivieren der Standardarbeitsplanversion

Wenn Sie eine Arbeitsplanversion aktivieren, um diese als die Standardarbeitsplanversion aus, die Produktprogrammplanung verwendet oder die verwendet wird, um Produktionsaufträge zu generieren. Sie können nur eine aktive Arbeitsplanversion für einen vorgegebenen Reihe von Beschränkungen haben (z, Periode, Standort oder Menge). Wenn die Version, dass Sie versuchen, Konflikte mit einer Version zu ermöglichen, die bereits aktiv ist, erhalten Sie eine Fehlermeldung. Um eine mehrdeutige Aktivierung zu verhindern, müssen Sie entweder die Konflikte verursachende dann die Version deaktivieren oder Einschränkungen (normalerweise die Periode) auf Bundesebene Arbeitsplanversion ändern.

### <a name="electronic-signatures"></a>Elektronische Signaturen

Wenn Sie ein Protokoll beibehalten müssen, das Datensätze das jede Arbeitsplanversion genehmigt und aktiviert, können Sie elektronische Signaturen für diese Aufgaben benötigen. Benutzer, Arbeitsplanversionen genehmigen und aktivieren, müssen dann ihre Identität bestätigen, indem sie verwenden elektronische Signatur [] (/dynamics365/operations/organization-administration/electronic-signature-overview).

### <a name="product-change-that-uses-case-management"></a>Produktänderung die Anfrageverwaltung verwendet,

Der Produktänderungsfall für die Genehmigung und die Aktivierung der neue oder geänderte Arbeitsplänen und von Arbeitsplanversionen gibt Ihnen eine einfache Möglichkeit dar, um eine Übersicht der Arbeitsplanversionseinschränkungen anzuzeigen. Sie können auch alle Arbeitspläne genehmigen und zu aktivieren, die mit einer spezifischen Änderung in einem Arbeitsgang im Dokument und die Ergebnisse im Produkt zugeordnet werden, ändern Sie Fall.

## <a name="maintaining-routes"></a>Verwalten von Arbeitsplänen
Abhängig von Ihren Geschäftsanforderungen könnten Sie, Aufwand zu reduzieren, der erforderlich ist, um die Prozeßdefinitionen verwalten.

### <a name="making-routes-independent-of-resources"></a>Tätigen des Arbeitsplan unabhängiger von Ressourcen

In vielen Systemen müssen die betriebliche Ressource oder Ressourcengruppe, die ausgeführt werden sollen, ein Arbeitsgang im Arbeitsplan angegeben sind. Allerdings in Dynamics 365 für Arbeitsgänge, können Sie Bedingungen eine definieren, die einer betrieblichen Ressource erfüllen muss, um für den Arbeitsgang verwendet werden sollen. Daher muss die Einzelgeschäftressource oder Ressourcengruppe, die verwendet werden soll, nicht ermittelt werden, bis der Vorgang tatsächlich geplant ist. Diese Funktion ist besonders nützlich, wenn Sie zahlreiche Arbeitskräfte oder Maschinen zu einer Gruppe zusammenfassen, die denselben Arbeitsgang ausführen können.  

Geben Sie beispielsweise an, dass ein Arbeitsgang eine betriebliche Ressource aus erforderlich ** Maschine ** eingeben, das eine stempelnd ** ** Tonnen Funktion von 20 hat. Das Planungsmodul kommt diese Anforderungen einer Einzelgeschäftressource oder -Ressourcengruppe auf, wenn der Arbeitsgang geplant wird. Da Sie diesen nur Anforderungen angeben können, anstatt, den Vorgang mit einer bestimmten Maschine zu binden, können Sie hiermit viel mehr Flexibilität. Darüber hinaus ist Verwaltung einfacher, wenn Ressourcen verschoben werden, neue Ressourcen oder hinzugefügt werden.  

Weitere Informationen zu den unterschiedlichen Arten von Ressourcenanforderungen und deren, finden Sie Anforderungen der betrieblichen Ressource verwendet und [Ressourcenfunktionen]( resource-capabilities.md).

### <a name="sharing-routes-across-sites"></a>Freigabenarbeitspläne standortübergreifend

Wenn Sie dasselbe Produkt an mehr als einen Produktionsstandort erzeugen und die Schritte für die Erstellung des Produkts identisch an allen Standorten werden, können Sie einen freigegebenen Arbeitsplan häufig zu entwerfen, der allen Produktionsstandorten verwendet wird. Um einem gemeinsamen Arbeitsplan erstellen, geben Sie kein Standort im Arbeitsplan selbst anzeigen. Sie müssen jedoch noch eine Arbeitsplanversion erstellen, bei der gemeinsamen Arbeitsplan im Produkt an jedem Standort beziehen.  

Stellen Sie außerdem sicher, ob die Ressourcenanforderungen für jeden Arbeitsgang im Arbeitsplan nicht Einzelgeschäftbetriebsmittel oder benötigen jedoch -Ressourcengruppen, werden stattdessen in Bezug auf die Merkmale der erforderlichen Ressourcen angegeben. Das Planungsmodul wird dann in der Lage, die betrieblichen entsprechenden Ressourcen aus dem Standort zuweisen, dass die Produktion angezeigt geplant wird. Wenn es beispielsweise geringfügige Unterschiede in der Laufzeit Lieferungen überfällig die Rüstzeit für einen bestimmten Arbeitsgang ist standortspezifisch, können Sie diese Informationen angeben, indem Sie eine zusätzliche Arbeitsgangzuordnung für diesen Standort hinzufügen.  

Um aus vollständigen Nutzen der Vorteile geeigneter Arbeitsplänen zu übernehmen, sollten der Ressourcenverbrauch auf der jeweiligen Stückliste (BOM) auch verwenden. Ist der Markierung für Ressourcenverbrauch auf der Stücklistenposition, der Lagerort und Lagerplatz, dass von Rohmaterialien verbraucht werden sollen, aus der betrieblichen Ressource nicht gefolgert werden, dass der Arbeitsgang geplant wird angezeigt. Daher müssen der Lagerort und der Lagerplatz nicht ermittelt werden, solange die Produktion tatsächlich geplant ist. Auf diese Weise können Sie die Stückliste und den Arbeitsplanunabhängigen im physischen Standort erstellen, in dem das Produkt hergestellt wird.

### <a name="standard-operation-relations"></a>Normalbetriebrelationen

Wenn Ihr Unternehmen standardisierte Arbeitsgänge für die Produktion verwendet und wenn es gibt oder keine Änderung der Rüstzeit, Bearbeitungszeit, Verbrauchsberechnung, Kostenberechnung usw. gibt kann nützlich sein können Sie für das Erstellen von Standardarbeitsgangzuordnungen für alle Arbeitsgänge. In diesem Fall können Sie vermeiden, Arbeitsgangzuordnungen zu erstellen, die für einen beliebigen Arbeitsplan oder zu freigegebene Produkt.  

Wenn Sie auch Ressourcenanforderungen hinsichtlich Qualifikation und Funktionen ausdrücken, und Ihre Standort-unabhängig Arbeitspläne erstellen, können Sie die aktuelle Hilfe, Verwaltung der Geschäftsprozesse zu ein Mindest- beizubehalten.  

Wenn Sie diesen Ansatz verwenden, wird die Seite ** Arbeitsgangzuordnungen ** Ihr primäres Ziel für Wartungsbearbeitungszeiten und anderer allgemeiner Eigenschaften.

### <a name="resource-specific-process-times"></a>Ressource-Besonderebearbeitungszeiten

Wenn Sie eine betriebliche Ressourcen oder einer Ressourcengruppe nicht als Teil der Ressourcenanforderungen für einen Arbeitsgang angegeben, funktionierten möglicherweise die entsprechenden Ressourcen mit unterschiedlichen Geschwindigkeiten. Daher kann sich die Dauer, die erforderlich ist, um einen Arbeitsgang zum Verarbeiten, sollen. Zur Behebung dieses Problems, können Sie das Feld auf Formel ** ** der Arbeitsgangzuordnung verwenden Zeitintervall (die Bearbeitungszeit berechnet wird. Die folgenden Optionen sind verfügbar:

-   ** Standard ** – (Standardeinstellung) die Berechnung nur die Felder aus der Arbeitsgangzuordnung und multipliziert der angegebenen Bearbeitungszeit von der Auftragsmenge.
-   ** Die Kapazität ** – Die Berechnung umfasst das ** Kapazität ** Feld aus der betrieblichen Ressource. Daher ist die Zeit Ressourceabhängiges Objekt. Der Wert, der in dieser betrieblichen Ressource angegeben wird, wird Kapazität pro Stunde. Dieser Wert wird durch die Bestellmenge und den Faktor ** ** Wert aus der Arbeitsgangzuordnung multipliziert.
-   ** Charge ** – Eine Stapelverarbeitungskapazität wird berechnet, indem der Arbeitsgangzuordnung von Informationen verwendet. Die Anzahl von Chargen und daher die Bearbeitungszeit können auf Basis der Auftragsmenge dann berechnet werden.
-   ** Ressourcencharge ** – Diese Option ist grundlegend die gleiche wie die Charge ** ** Option. Allerdings umfasst die Berechnung das ** Stapelverarbeitungskapazität ** Feld aus der betrieblichen Ressource. Daher ist die Zeit Ressourceabhängiges Objekt.


<a name="see-also"></a>Siehe auch
--------

[Bills of materials and formulas](bill-of-material-bom.md)

[Cost categories used in production routing](../cost-management/cost-categories-used-production-routings.md)

[Resource capabilities](resource-capabilities.md)

[Electronic signature overview](/dynamics365/operations/organization-administration/electronic-signature-overview)


