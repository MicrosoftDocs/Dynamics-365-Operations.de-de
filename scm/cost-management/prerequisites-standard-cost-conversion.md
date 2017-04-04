---
title: "Voraussetzungen für eine Standardkostenumrechnung"
description: "In diesem Thema werden die Aufgaben erörtert, die vor einer Standardkostenumrechnungen ausgeführt werden müssen."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventStdCostConv
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 50891
ms.assetid: 73af66cf-c924-45be-837a-a648dbd05a31
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 562572f45dd78fb5655466e20a0c09b125c74d39
ms.lasthandoff: 03/31/2017


---

# <a name="prerequisites-for-a-standard-cost-conversion"></a>Voraussetzungen für eine Standardkostenumrechnung

In diesem Thema werden die Aufgaben erörtert, die vor einer Standardkostenumrechnungen ausgeführt werden müssen. 

Führen Sie die folgenden Schritte aus, bevor Sie eine Standardkostenumrechnung ausführen:

1.  Definieren Sie eine **Artikelmodellgruppe** für Standardkosten. Erstellen Sie mithilfe der Seite "Artikelmodellgruppe" eine Lagersteuerungsgruppe mit einem Lagermodell für Standardkosten. Beim Einrichten einer Standardkostenumrechnung muss diese Lagersteuerungsgruppe den Artikeln zugewiesen werden, für die die Umrechung erfolgen soll.
2.  Weisen Sie jedem Artikel eine **Kostengruppe** zu.
    -   Die Kostengruppe, die einem gekauften Artikel zugewiesen wird, kann die Grundlage für die Zuweisung von Sachkonten bilden, die mit Standardkosten verknüpft sind. Dies kann die Zuweisung von Sachkonten für Einkaufspreisabweichungen beinhalten. In einer Produktionsumgebung ermöglicht eine Kostengruppe, die eingekauften Komponenten zugewiesen ist, die Segmentierung von Kosten in den berechneten Kosten eines produzierten Artikels.
    -   Die einem produzierten Artikel zugewiesene Kostengruppe kann als Grundlage für die Zuweisung von standardkostenbezogenen Sachkonten fungieren (beispielsweise beim Zuweisen von Sachkonten für Produktionsabweichungen).

3.  Weisen Sie einem produzierten Artikel eine **Standardauftragsmenge** zu, sofern es sich um einen Artikel mit konstanten Kosten handelt. Die standardmäßige Auftragsmenge für einen produzierten Artikel fungiert in der Buchhaltung als Losgröße für die Amortisierung oder anteilsmäßige Verteilung von konstanten Kosten. Dies kann Rüstzeiten in Arbeitsgängen des Arbeitsplans oder eine konstante Komponentenmenge in einer Stückliste einschließen.
4.  Weisen Sie standardkostenbezogene **Hauptbuchkonten** (mit besonderem Augenmerk auf die Neubewertungsabweichung) zu. Verwenden Sie die Seite " Buchung ** ** ** Lagerverwaltung ** &gt; ** Einstellungen **) um Hauptbuchkonten zu, die sich auf Standardkosten beziehen. Für die Standardkostenumrechung muss für alle Artikel und Kostengruppen mindestens das Konto für die Neubewertungsabweichung zugewiesen werden. Definieren Sie mithilfe der Seite **Kostenplan** die Hauptbuchkonten, die für die Standardkosten benötigt werden. Aktivieren Sie mithilfe der Seite **Buchungskombinationen** die Kostenbeziehungen (für Tabellen, Gruppen und Alle), bevor Sie die Artikelbuchungsregeln definieren.
5.  Definieren Sie die Lagerparameter, die sich auf Standardkosten beziehen. Weisen Sie mithilfe der Registerkarte **Nummernkreise** auf der Seite **Parameter für Lager- und Lagerortverwaltung** einen Nummernkreis für Neubewertungsbelege zu. Ein Neubewertungsbeleg wird generiert, wenn sich durch die Ergebnisse der Standardkostenumrechnung eine Änderung des Lagerwerts eines Artikels ergibt. Definieren Sie mithilfe der Seite **Parameter für Lager- und Lagerortverwaltung** Kostensteuerungsparameter (auf der Registerkarte **Bestandsrechnung**) zwei Parameter, die zu den Standardkosten gehören.
    -   Verwenden Sie das Feld **Kostenaufschlüsselung**, um "Kein" oder "Untergeordnetes Sachkonto" auszuwählen. Die Auswahl von "Untergeordnetes Sachkonto" wird auch als aktive Kostenaufschlüsselung bezeichnet. Eine aktive Kostenaufschlüsselung ist sehr wichtig für die übergreifende Berechnung, Beibehaltung und Anzeige der Kostengruppensegmentierung in einer mehrstufigen Produktstruktur für Standardkostenartikel. Bei aktiver Kostenaufschlüsselung können die folgenden Faktoren in einem einstufigen bzw. mehrstufigen Format oder in einem Gesamtformat gemeldet und analysiert werden:
        1.  Bestand
        2.  Ressource in Fertigung (RIF)
        3.  Wareneinsatz (Cost Of Goods Sold, COGS) pro Kostengruppe

        Eine aktive Kostenaufschlüsselung bedeutet, dass bei der Aktivierung der Kosten eines produzierten Artikels die Kostengruppensegmentierung im Kostendatensatz des Artikels gespeichert wird. Wenn Sie im Feld **Kostenaufschlüsselung** keinen Wert angeben, findet für Standardkostenartikel keine Verwaltung der Kostengruppensegmentierung statt. Mit anderen Worten: Die Standardkosten eines produzierten Artikels werden als einzelner Betrag ohne Kostengruppensegmentierung berechnet und verwaltet, und die Kostenbeiträge produzierter Komponenten werden in einem einzelnen Betrag zusammengefasst.
    -   Wählen Sie mithilfe des Felds **Abweichungen vom Standard** die Option "Zusammengefasst" oder "Pro Kostengruppe" aus. Durch Auswahl von "Pro Kostengruppe" werden Einkaufspreisabweichungen und Produktionsabweichungen nach Kostengruppe aufgeschlüsselt. Dadurch können auch die vier Arten von Produktionsabweichungen (Losgröße, Menge, Preis und Ersatzabweichung) unterschieden werden. Bei Auswahl von "Zusammengefasst" sind keine Abweichungen nach Kostengruppe ersichtlich, und auch die Erkennung der vier Arten von Produktionsabweichungen ist nicht möglich, da lediglich eine zusammengefasste Produktionsabweichung angezeigt wird. Die Richtlinie für Abweichungen vom Standard ist unabhängig von der Richtlinie für die Kostenaufschlüsselung. Anders ausgedrückt: Auch wenn bei Auswahl von Abweichungen nach Kostengruppe keine Kostenaufschlüsselungsrichtlinie ausgewählt wurde, werden die Produktionsabweichungen nach Kostengruppe dennoch erfasst.




