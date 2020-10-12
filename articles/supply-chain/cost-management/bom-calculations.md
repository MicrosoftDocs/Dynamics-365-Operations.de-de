---
title: BOM-Berechnungen
description: Die Berechnungen für die Kostenzusammenfassung sowie zur Ermittlung des Stücklistenpreises werden als Herstellkostenkalkulation bezeichnet, da sie vom Formular aus gestartet werden. Dieses Thema enthält Informationen zur Stücklistenberechnung
author: AndersGirke
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcTable, CostingVersion, InventItemPrice, ProdSetupCostEstimation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 273763
ms.assetid: c6fa3348-eafa-4847-9132-e65c5f55cbf4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: f90e5babb440a2226638f7d96f111816732f0e70
ms.sourcegitcommit: 175f9394021322c685c5b37317c2f649c81a731a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2020
ms.locfileid: "3826765"
---
# <a name="bom-calculations"></a>BOM-Berechnungen

[!include [banner](../includes/banner.md)]

Die Berechnungen für die Kostenzusammenfassung sowie zur Ermittlung des Stücklistenpreises werden als Herstellkostenkalkulation bezeichnet, da sie vom Formular aus gestartet werden. Dieses Thema enthält Informationen zur Stücklistenberechnung

Die Berechnungen für die Kostenzusammenfassung sowie zur Ermittlung des Stücklistenpreises werden als Herstellkostenkalkulation bezeichnet, da sie von der Seite **Berechnung** gestartet werden. Sie verwenden die Seite **Berechnung**, um folgende Aufgaben auszuführen:

-   Berechnen Sie die Kosten eines produzierten Artikels und generieren Sie einen zugehörigen Artikelkostendatensatzes in einer Nachkalkulationsversion.
-   Berechnen Sie den Verkaufspreis eines produzierten Artikels und generieren Sie einen zugehörigen Artikelverkaufspreisdatensatzes in einer Nachkalkulationsversion.

Die Methode, mit der Sie die Seite **Berechnungen** verwenden, variiert leicht, je nachdem, wie Sie Herstellkostenkalkulationen initiieren. Die Verwendung der Seite **Berechnung** hängt auch davon ab, ob in die Herstellkostenkalkulation eine Nachkalkulationsversion für Standardkosten oder für geplante Kosten einbezogen wird. Eine weitere beeinflussende Rolle spielen die Richtlinien, die für die in der Herstellkostenkalkulation verwendete Nachkalkulationsversion definiert wurden. **Hinweis** Für Positionsartikel in Aufträgen, Verkaufsangeboten oder Serviceaufträgen wird eine Variante der Seite **Berechnung** verwendet. Diese Berechnungen sind als auftragsspezifische Stückkostenkalkulationen bekannt. Eine auftragsspezifische Stücklistenkalkulation erzeugt einen Artikelkostendatensatz innerhalb einer Nachkalkulationsversion. Stattdessen erstellt sie einen Berechnungsdatensatz, der auf der Seite **Stücklistenberechnungsdetails** angezeigt wird. Der Berechnungsdatensatz beinhaltet einen berechneten Einstands- sowie einen berechneten Verkaufspreis. Die Seite **Berechnungen** kann sowohl für einen einzelnen produzierten Artikel als auch für eine Nachkalkulationsversion verwendet werden.

-   Um die Kosten für einen einzelnen produzierten Artikel zu berechnen, führen sie auf der Seite **Artikelpreis** die Stücklistenberechnung durch. Die Seite **Berechnungen** erbt die Artikelkennung. Die Nachkalkulationsversion, die Stücklistenversion, die Arbeitsplanversion, die Berechnungsmenge, das Berechnungsdatum und der Standort müssen angegeben werden.
    -   Standardmäßig werden die Stücklistenversion und die Arbeitsplanversion für die aktiven Versionen für den Artikel, den Standort, das Datum und die Berechnungsmenge festgelegt. Sie können jedoch die Standardwerte mit genehmigten Versionen überschreiben.
    -   Standardmäßig wird die Berechnungsmenge auf die Standard-Auftragsmenge des Artikels festgelegt. Kann der Benutzer den Standardwert überschreiben?
    -   Berechnungsdatum und Standort können durch die Nachkalkulationsversion vorgegeben sein. Ist dies nicht der Fall, können für das Datum und den Standort benutzerdefinierte Werte angegeben werden. Durch ein Berechnungsdatum in der Zukunft wird die Verwendung von Datensätzen für ausstehende Kosten bestimmt. Für die Herstellkostenkalkulationen wird ein Datensatz für ausstehende Kosten mit dem nächstgelegenen Anfangsdatum verwendet, das höchstens dem Berechnungsdatum entspricht.
-   Um Kosten für alle produzierten Artikel oder ausgewählte Artikel zu sehen oder um Artikel auf einer Basis der Verwendung zu aktualisieren, starten Sie die Stücklistenberechnung auf der Seite **Nachkalkulationsversion einrichten** oder **Nachkalkulationswartung**. Die Seite **Berechnungen** erbt die Nachkalkulationsversion.
    -   Für die Berechnungen wird die Verwendung der aktiven Stücklisten- sowie der aktiven Arbeitsplanversion für einen produzierten Artikel (und den zugehörigen Standort sowie das zugehörige Datum und die zugehörige Menge) vorausgesetzt, es sei denn, für eine produzierte Komponente wurde eine untergeordnete Stückliste oder ein untergeordneter Arbeitsplan angegeben.
    -   Für die Berechnungen wird angenommen, dass die Standardauftragsmenge für produzierte Artikel verwendet wird. Für die Berechnungen wird die Verwendung der Standardauftragsmenge für produzierte Artikel vorausgesetzt. Diese bildet die Grundlage für die Berechnung von Komponentenmengen, für die Bestimmung der relevanten Stücklisten- und Arbeitsplanversion (bei Verwendung von mengenabhängigen Stücklisten und Arbeitsplänen) sowie für die Amortisierung konstanter Kosten. Diese Voraussetzung gilt nicht, wenn eine produzierte Komponente den Stücklistenpositionstyp **Produktion** oder **Kreditor** besitzt oder wenn für Herstellkostenkalkulationen der Auflösungsmodus Auf Auftrag fertigen verwendet wird, da die Mengen die angegebene Berechnungsmenge darstellen.
    -   Berechnungsdatum und Standort können durch die Nachkalkulationsversion vorgegeben sein. Ist dies nicht der Fall, können für das Datum und den Standort benutzerdefinierte Werte angegeben werden.

Bei anderen Variationen der Herstellkostenkalkulation werden der Nachkalkulationstyp sowie die Einschränkungen der Nachkalkulationsversion angezeigt:

-   Herstellkostenkalkulationen mit Standardkosten müssen zur Sicherstellung von Standardprinzipien der Nachkalkulation mithilfe von Richtlinien der Nachkalkulationsversion eingeschränkt werden. Die Standardprinzipien der Nachkalkulation erfordern die Erzwingung von Einschränkungen bei der Verwendung von Standardkosten für eingekaufte Artikel, einen Auflösungsmodus mit nur einer Ebene sowie die Einbeziehung sonstiger Zuschläge in die Einheitenkosten.
-   Bei Stücklistenkalkulationen mit geplanten Kosten ist dagegen keine Einhaltung von Standardprinzipien der Nachkalkulation erforderlich. Für diese Herstellkostenkalkulationen können unterschiedliche Auflösungsmodi sowie alternative Quellen für die Kostendaten produzierter Artikel verwendet werden. Die Erzwingung von Einschränkungen im Rahmen der Nachkalkulationsversion ist optional.

### <a name="bom-calculations-that-use-standard-costs"></a>Stücklistenkalkulationen mit Standardkosten.

Durch die Richtlinien innerhalb der Nachkalkulationsversion (für Standardkosten) kann die Erzwingung von fünf Richtlinien für die Herstellkostenkalkulation vorgegeben sein. Durch das Kontrollkästchen **Erfassungseinschränkung** in der Nachkalkulationsversion wird eine dieser Richtlinien vorgegeben. In diesem Fall müssen sonstige Zuschläge in den Einheitenpreis einbezogen werden. Sonstige Zuschläge für eingekaufte Artikel können manuell eingegeben werden, wohingegen es sich bei den sonstigen Zuschlägen für produzierte Artikel um die berechnete Amortisierung konstanter Kosten handelt. Durch das Kontrollkästchen **Berechnungseinschränkung** innerhalb der Nachkalkulationsversion werden die anderen vier Richtlinien für die Herstellkostenkalkulation vorgegeben.

-   Die Quelle für die Kostenbeiträge für eingekaufte Artikel muss auf Standardkosten basieren. Das bedeutet, dass für die Herstellkostenkalkulationen die Artikelkostendatensätze aus der angegebenen Nachkalkulationsversion oder aus dem Fallback mit den Standardkosten verwendet werden muss.
-   Der Auflösungsmodus darf lediglich über eine einzelne Ebene verfügen, damit eine exakte und einheitliche Berechnung der Standardkosten sichergestellt ist.
-   Die Gewinngabe muss vorgegeben werden, um einheitliche Ergebnisse bei der Berechnung des Artikelverkaufspreises zu erzielen. Die Nachkalkulationsversion muss so konfiguriert sein, dass Verkaufspreisinhalte zulässig sind, damit die Verwendung der Gewinnvorgabe sowie die Generierung der Artikelverkaufspreisdatensätze möglich ist.
-   Das Fallback-Prinzip muss vorgegeben werden und kann auf **Keines**, **Aktive** (für aktive Kostensätze) oder **Nachkalkulationsversion** (für eine spezifische Nachkalkulationsversion) festgelegt werden.

### <a name="bom-calculations-that-use-planned-costs"></a>Stücklistenkalkulationen mit Plankosten

Durch die Richtlinien innerhalb der Nachkalkulationsversion (für Plankosten) kann die Erzwingung von fünf Richtlinien für die Herstellkostenkalkulation vorgegeben sein. Alternativ können Sie die Richtlinien Standardwerte derzeit bereitstellen. Durch das Kontrollkästchen **Erfassungseinschränkung** innerhalb der Nachkalkulation wird bestimmt, ob die Richtlinie für die Herstellkostenkalkulation zu sonstigen Zuschlägen vorgegeben oder als Standardwert verwendet wird. Sonstige Zuschläge können optional in den Einheitenpreis einbezogen werden. Durch das Kontrollkästchen **Berechnungseinschränkung** innerhalb der Nachkalkulation wird bestimmt, ob die anderen vier Richtlinien für die Herstellkostenkalkulation vorgegeben oder als Standardwerte verwendet werden.

-   Die Quelle von Kostenbeiträgen für einen gekauften Artikel können die Artikelkostendatensätze aus einer Nachkalkulationsversion sein. Alternativ kann die Quelle durch die Herstellkostenkalkulationsgruppe definiert werden, die dem Artikel zugewiesen ist. So könnten durch die Herstellkostenkalkulationsgruppe als Quelle für die Kostenbeitragsdaten beispielsweise Einkaufspreis-Handelsvereinbarungen definiert werden.
-   Der Auflösungsmodus kann eine oder mehrere Ebenen aufweisen, den Typ "Auf Auftrag fertigen" besitzen oder auf dem Stücklistenpositionsartikel basieren. Durch den Auflösungsmodus für den Stücklistenpositionstyp wird die Kostenberechnungslogik für Vorkalkulationen von Produktionsaufträgen repliziert.
-   Die Gewinnvorgabe kann entweder vorgegeben oder als Standardwert verwendet werden. Die Nachkalkulationsversion muss so konfiguriert sein, dass Verkaufspreisinhalte zulässig sind, damit die Verwendung der Gewinnvorgabe sowie die Generierung der Artikelverkaufspreisdatensätze möglich ist.
-   Das Fallback-Prinzip kann entweder vorgegeben oder als Standardwert verwendet werden. Das Fallback-Prinzip muss vorgegeben werden und kann auf **Keines**, **Aktiv** (für aktive Kostensätze) oder **Nachkalkulationsversion** (für eine spezifische Nachkalkulationsversion) festgelegt werden.

Durch Herstellkostenkalkulationen werden Warnmeldungen und anderen Arten von Meldungen erstellt. Die Meldungen hängen von den unterschiedlichen Richtlinien für die Herstellkostenkalkulation ab. Dient zum Überschreiben der geltenden Warnbedingungen, die für die Artikeln zugeordnete Herstellkostenkalkulationsgruppe definiert sind. Diese geltenden Warnbedingungen können beim Initiieren einer Herstellkostenkalkulation überschrieben werden. Bei Verwendung des Fallback-Prinzips empfiehlt es sich zumeist, die Fallback-Informationen als Meldungen im Infolog anzuzeigen. Beim Aktualisieren berechneter Kosten für Artikel ohne Kostendatensätze empfiehlt es sich zudem, die nicht aktualisierten Artikel per Meldung im Infolog zu kennzeichnen.

## <a name="bom-calculations-that-use-the-fallback-principle"></a>Informationen zu Herstellkostenkalkulationen mit Fallback-Prinzip
Im Anschluss finden Sie zwei Beispiele für die Verwendung des Fallback-Prinzips:

-   **Zwei-Versionen-Ansatz für die Aktualisierung von Standardkosten**− Eine Nachkalkulationsversion kann die stufenweisen Veränderungen an den Standardkosten (wie Datensätze mit ausstehenden Kosten, die für neue Artikel oder Kostenänderungen stehen) beinhalten. In dieser Situation kann durch das Fallback-Prinzip die Verwendung der in anderen Nachkalkulationsversionen enthaltenen aktiven Standardkosten identifiziert werden.
-   **Simulieren der Auswirkungen von Kostenänderungen mit geplanten Kosten** – Eine Nachkalkulationsversion für geplante Kosten kann stufenweise Änderungen zu Simulationszwecken enthalten. Diese Nachkalkulationsversion enthält dann Datensätze mit ausstehenden Kosten, die für die simulierten Kostenänderungen an Artikeln stehen, sowie Kostenkategorien und Berechnungsformeln für indirekte Kosten. In dieser Situation kann durch das Fallback-Prinzip die Verwendung der in anderen Nachkalkulationsversionen enthaltenen aktiven Standardkosten identifiziert werden.

## <a name="bom-calculation-of-a-suggested-sales-price"></a>Informationen zur Herstellkostenkalkulation eines vorgeschlagenen Verkaufspreises
Beim Kosten-plus-Aufschlag-Prinzip werden für den berechneten Verkaufspreis des Artikels die Gruppe der für die Herstellkostenkalkulation festgelegten Prozentsätze für die Gewinnvorgabe sowie die Kosten berücksichtigt, die den zugehörigen Komponentenartikeln, Arbeitsgängen des Arbeitsplans sowie den entsprechenden Produktionsgemeinkosten zugeordnet sind. Der Aufschlag spiegelt die Prozentsätze für die Gewinnvorgaben wider, die den Kostengruppen zugewiesen sind, sowie die Kostengruppen, die Artikeln zugewiesen sind, Kostenkategorien für die Arbeitsgangsteuerung und die Berechnungsformeln für indirekte Kosten für Produktionsgemeinkosten. Die Gruppen der Prozentsätze für die Gewinnvorgabe sind mit **Standard**, **Gewinn 1**, **Gewinn 2** und **Gewinn 3** beschriftet. So kann beispielsweise in der Gruppe Gewinn 1 eine Gewinnvorgabe von 50 Prozent für eine Kostengruppe definiert werden, die eingekauftem Material zugeordnet ist, und eine Gewinnvorgabe von 80 Prozent für eine Kostengruppe, die Kostenkategorien für Arbeitsgänge des Arbeitsplans zugeordnet ist. Die Behandlung der Ergebnisse eines berechneten Verkaufspreises hängt vom Kontext der Herstellkostenkalkulation ab:

-   **Herstellkostenkalkulation für einen Artikel sowie für eine angegeben Nachkalkulationsversion** – Durch die Herstellkostenkalkulation wird innerhalb der Nachkalkulationsversion ein vorläufiger Verkaufspreisdatensatz generiert. Dieser Verkaufspreisdatensatz bildet die Grundlage für die Anzeige der Berechnungsdetails (beispielsweise auf der Seite **Berechnung Artikelosten**). Der Verkaufspreisdatensatz fungiert in erster Linie als Referenzinformation und wird nicht als Basis für den Verkaufspreis einer Verkaufsrechnung herangezogen.
-   **Auftragsspezifische Herstellkostenkalkulation** − Bei Positionsartikeln in Aufträgen, Verkaufsangeboten oder Serviceaufträgen wird eine Abwandlung des Formulars für die Seite **Herstellkostenkalkulation** verwendet. Durch eine auftragsspezifische Herstellkostenkalkulation wird kein Kostendatensatz in einer Nachkalkulationsversion generiert. Stattdessen erstellt sie einen Berechnungsdatensatz, der auf der Seite **Stücklistenberechnungsdetails** angezeigt wird. Dieser Verkaufspreisdatensatz bildet die Grundlage für die Anzeige der Berechnungsdetails (beispielsweise auf der Seite **Berechnung Artikelkosten**). Hiermit können Informationen zum ausgewählten Kalkulationsdatensatz an den ursprünglichen Positionsartikel übertragen werden. Beispielsweise kann der berechnete Verkaufspreis auf einen Positionsartikel übertragen werden.

## <a name="order-specific-bom-calculations"></a>Auftragsspezifische Herstellkostenkalkulationen
Eine auftragsspezifische Herstellkostenkalkulation stellt eine Form der Herstellkostenkalkulation für einen produzierten Artikel dar. Eine auftragsspezifische Herstellkostenkalkulation wird für einen Positionsartikel in einem Auftrag, Verkaufsangebot oder Serviceauftrag ausgeführt. Eine auftragsspezifische Herstellkostenkalkulation erstellt einen Berechnungsdatensatz, der auf der Seite **Ergebnisse der Herstellkostenkalkulation** angezeigt wird. Der Berechnungsdatensatz enthält ein berechnetes Gewicht, einen berechneten Einstandspreis, der auf aktiven Kostendatensätzen basiert, und einen berechneten Verkaufspreis. Bei jeder auftragsspezifischen Formelberechnung wird im Formular **Formelberechnungsergebnisse** ein Berechnungsdatensatz mit eindeutigem Bezug zu einer Berechnungsnummer generiert. Die Ergebnisse eines Kalkulationsdatensatzes können optional an den ursprünglichen Positionsartikel übertragen werden. Eine auftragsspezifische Herstellkostenkalkulation unterscheidet sich von einer Herstellkostenkalkulation für einen produzierten Artikel auf zwei Arten:

-   Eine auftragsspezifische Stücklistenkalkulation erzeugt einen Artikelkostendatensatz innerhalb einer Nachkalkulationsversion. Das bedeutet, dass die Richtlinien für die Herstellkostenkalkulation nicht für die Erstellung eines Artikelkostendatensatzes oder für die Überschreibung eines Kostendatensatzes gelten.
-   Zum anderen wird von einer auftragsspezifischen Herstellkostenkalkulation für Komponenten, Kostenkategorien sowie für Berechnungsformeln für indirekte Kosten immer der Datensatz für aktive Kosten verwendet.





