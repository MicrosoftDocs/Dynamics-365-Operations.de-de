---
title: Kostenrechnungsterminologie
description: "Dieses Thema definiert die Schlüsselbegriffe, die in der Kostenrechnung verwendet werden."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CAMCostControlWorkspace, CAMCostControlWorkspaceConfiguration
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 223114
ms.assetid: 1c798592-77d0-4a8f-beaa-9159c75957da
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 76c5d4b3a118747246eeb7ca0db69532af04bf9c
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="cost-accounting-terminology"></a>Kostenrechnungsterminologie

[!include[banner](../includes/banner.md)]


Dieses Thema definiert die Schlüsselbegriffe, die in der Kostenrechnung verwendet werden.

**Kostenrechnung**

Mit der Kostenrechnung können Sie Daten aus verschiedenen Quellen erfassen, wie beispielsweise das Hauptbuch, untergeordnete Sachkonten, Budgets und statistische Informationen. Sie können anschließend Kostendaten analysieren, zusammenfassen und auswerten, sodass die Verwaltung die bestmöglichen Entscheidungen bei Preisaktualisierungen, Budgets, Kostenkontrolle usw. treffen kann. Die Quelldaten, die für die Kostenanalyse verwendet werden, werden unabhängig in der Kostenrechnung gehandhabt. Daher wirken sich Aktualisierungen in der Kostenrechnung nicht auf die Quelldaten aus. Wenn Sie jedoch Kostendaten aus verschiedenen Quellen erfassen und insbesondere wenn Sie die Hauptkonten vom Hauptbuch in Microsoft Dynamics 365 for Operations als Kostenelemente importieren, gibt es eine Datenredundanz, da dieselben Daten im Hauptbuch und in der Kostenrechnung vorhanden sind. Diese Redundanz ist erforderlich, da Sie Finanzverwaltung für die externe Berichterstellung und Kostenrechnung für die interne Berichterstellung verwenden.

**Kostenrechnungssachkonto**

Das Kostenrechnungs-Sachkonto ist ein spezialisiertes Framework, das bestimmt, wie Prozesse, Werte und Mengen für einen bestimmten Bereich in der Kostenrechnung eingegeben und dargestellt werden. Das Kostenrechnungs-Sachkonto definiert Prozesse und Regeln zum Messen von Kosten zu Kostenträgern. Es behandelt Kostenbuchungen und verwaltet Dokumente, die die Änderungen bei Werten und Mengen aufzeichnen, die von Kostenbuchungen produziert werden.

**Kosteneintrag**

Kosteneinträge sind das Ergebnis einer Übertragung über Datenkonnektoren von Hauptbucheinträgen, Kostenzuteilungen und gebuchten Kosteneinträgen in Kostenerfassungen.

**Kostenobjekt**

Kostenträger sind alle Typen von Objekten, denen Kosten zugeteilt werden. Es folgen einige typische Kostenträger:

-   Produkte
-   Projekte
-   Ressourcen
-   Abteilungen
-   Kostenstellen
-   Geografische Regionen

Verwaltung verwendet Kostenträger, um Kosten mengenmäßig zu bestimmen, aber auch um die Rentabilitätsanalyse voranzutreiben.

**Kostenelement**

Kostenelemente werden als Funktion verwendet, um nachzuverfolgen und zu kategorisieren, wo Kosten hinfließen. Es gibt zwei Typen von Kostenelementen: primäre Kosten und sekundäre Kosten. **Primäre Kosten** Die primären Kostenelemente stellen den Kostenfluss von der Finanzbuchhaltung zur Kostenrechnung dar. Die Kostenelementstruktur entspricht der Gewinn- und Verlustkontostruktur im Hauptbuch, wo ein Kostenelement einem Hauptkonto entsprechen kann. Nicht alle Hauptkonten müssen als Kostenelemente dargestellt werden, je nach den Geschäftsanforderungen. Es folgen einige Beispiele von primären Kostenelementen:

-   Wareneinsätze (COGs)
-   Indirekte Materialkosten
-   Personalkosten
-   Energiekosten

**Sekundäres Kostenelement** 

Die sekundären Kostenelemente stellen den internen Fluss der Kosten dar, da diese Kosten nur in der Kostenrechnung erstellt und verwendet werden. Sekundäre Kostenelemente tragen dazu bei sicherzustellen, dass die Quelle von Kosten nachverfolgt werden kann. Diese Kostenelemente werden in Kostenzuteilungen und bei Gemeinkostenberechnungen verwendet. Es folgen einige Beispiele von sekundären Kostenelementen:

-   Produktionskosten
-   Gemeinkosten für Produktion, Material und Marketing

**Kostensteuerungseinheit**

Eine Kostenkontrolleinheit stellt die Kostenstruktur dar. Sie muss Kostenträgerdimensionen in einem Kostenrechnungs-Sachkonto zugeordnet sein.

**Version**

Versionen werden verwendet, um verschiedene Ergebnisse zu simulieren, anzuzeigen und zu vergleichen. Standardmäßig werden alle Istkosten in einer Basisversion angezeigt, die als *Tatsächlich* bekannt ist. Für Budgets und Berechnungen können Sie mit so vielen Versionen arbeiten, wie Sie benötigen. Beispielsweise können Sie Budgetdaten in eine ursprüngliche Version importieren und dann das Budget in einer überarbeiteten Version überarbeiten. Für Berechnungen können Sie mehrere Versionen erstellen. In diesen verschiedenen Versionen können Sie dann Berechnungen erstellen, indem Sie unterschiedliche Berechnungsregeln verwenden, die für die Kostenzuteilung angewendet werden.

**Auszug**

Aufstellungen sind Ansichten für die Manager, die für die Kostensteuerung verantwortlich sind. Aufstellungen werden von einem Kostencontroller definiert und bieten einen kurzen Überblick über tatsächliche und budgetierte Kosten und sogar Abweichungen und Berechnungsversionen. Um sicherzustellen, dass Mangern nur Daten angezeigt werden, für die sie verantwortlich sind, unterliegen Daten, die in Aufstellungen angezeigt werden, den Zugriffsregeln.

**Datenkonnektor**

Daten können aus externen Systemen über Datenkonnektoren in die Kostenrechnung importiert werden. Beispielsweise können Sie Kontostrukturen, Dimensionen, Hauptbucheinträge sowie Budgeteinträge importieren. Sie können vorkonfigurierte Datenkonnektoren oder benutzerdefinierte Konnektoren verwenden, um Daten zu importieren und Datenverbindungen zu erstellen.

**Kostenklassifikation**

Die Kostenklassifizierung gruppiert Kosten nach ihren gemeinsamen Merkmalen. Kosten können beispielsweise nach Elementen, Nachverfolgbarkeit und Verhalten gruppiert werden.

-   **Nach Elementen** – Materialien, Arbeit und Ausgaben.
-   **Nach Nachverfolgbarkeit** – Direkte und indirekte Kosten. Direkte Kosten werden direkt den Kostenträgern zugewiesen. Indirekte Kosten können nicht direkt zu Kostenträgern nachverfolgt werden. Indirekte Kosten werden Kostenträgern zugeteilt.
-   **Nach Verhalten** – Fest, variabel und halbvariabel.

**Kostenverhalten**

Das Kostenverhalten klassifiziert Kosten nach ihrem Verhalten in Bezug zu Änderungen bei Hauptgeschäftsaktivitäten. Um Kosten effektiv zu kontrollieren, muss die Verwaltung das Kostenverhalten verstehen. Es gibt drei Typen von Kostenverhaltensmustern: fest, variabel und halbvariabel.

- **Fixkosten** – Fixkosten sind Kosten, die sich kurzfristig nicht ändern, unabhängig von Änderungen beim Umfang der Aktivität. Ein Posten bei den Festkosten können zum Beispiel grundlegende Betriebsausgaben eines Unternehmens sein, wie beispielsweise Miete. Diese ändert sich nicht, selbst wenn sich der Umfang der Aktivität erhöht oder verringert.

- **Variable Kosten** – Ein Posten variabler Kosten ändert sich je nach Änderungen im Umfang der Aktivität. Beispielsweise werden bestimmte direkte Materialkosten jedem Produkt zugeordnet, das verkauft wird. Je mehr Produkte verkauft werden, desto mehr direkte Materialkosten gibt es.

- **Halbvariable Kosten** – Halbvariable Kosten sind teilweise feste und teilweise variable Kosten. Zum Beispiel beinhaltet eine Internetzugangsgebühr eine standardmäßige monatliche Gebühr für den Zugang sowie eine Gebühr für die tatsächliche Breitbandnutzung. Die standardmäßige monatliche Zugangsgebühr ist ein Festkostenposten, wohingegen die Breitband-Nutzungsgebühr einen variablen Kostenposten darstellt.

**Gemeinkosten**

Gemeinkosten beziehen sich auf die laufenden Kosten für das Betreiben eines Unternehmens. Es sind die Kosten, die nicht unmittelbar mit bestimmten Geschäftsaktivitäten verknüpft werden können. Hier sind einige Beispiele für Gemeinkosten:

-   Buchhaltungsgebühren
-   Abschreibungen
-   Versicherung
-   Interesse
-   Anwaltsgebühren
-   Steuern
-   Kosten für Versorgungsunternehmen

**Kostenzuweisung**

Die Kostenzuteilung ist der Prozess der Zuweisung und Zuteilung von Kosten, basierend auf den Grundursachen der allgemeinen Kosten. Sie teilen die Kostenbeträge und -mengen von einem Kostenträger an einen oder mehrere andere Kostenträger zu. Beispielsweise werden alle Raum-Dienstleistungskosten den verschiedenen Abteilungen zugeteilt, die das gemeinsame Bürogebäude verwenden.

**Kostenzuteilungsrichtlinie**

Eine Kostenzuteilungs-Richtlinie definiert die Beträge und Mengen, die zugeteilt werden müssen. Zuteilungsregeln enthalten Zuteilungsquellregeln, die die Kosten bestimmen, die zugeteilt werden, und Zuteilungszielregeln, die bestimmen, wo die Kosten zugeteilt werden. Beispielsweise sind alle Kosten für Raumdienstleistungen eine Zuteilungsquelle, die verschiedenen Abteilungen in einer Organisation zugeteilt werden können (das heißt zu Zuteilungszielen).

**Verteilschlüssel**

Die Zuteilungsbasis ist die Basis, die zum Messen und zur Mengenbestimmung von Aktivitäten verwendet wird, wie beispielsweise Maschinenarbeitsstunden, die verwendet werden, sowie Kilowattstunden, die verbraucht werden, direkte Arbeitskosten, die anfallen, oder Quadratmeter, die belegt werden. Sie wird zum Zuteilen von Kosten an einen oder mehrere Kostenträger verwendet.

**Zuweisungsprinzip**

Eines der Zuteilungsprinzipien besteht in der Zuteilung von Kosten nach Verrechnungssatz. Sie können wählen, Kosten mithilfe des Satzes für die tatsächliche Periode oder eines historischen Satzes zuzuteilen. Die Zuteilung, die die reziproke Methode verwendet, stellt sicher, dass die Zuteilungsbasis durch eine Reihe gleichzeitiger Gleichungen bestimmt wird, bevor die Zuteilung mithilfe des Satzes der tatsächlichen Periode erfolgt.

**Kostenrollup**

Der Zweck des Kostenrollups besteht darin, alle Kosten für einen angegebenen Kostenträger einzuschließen. Der Grad der Aggregation ist benutzerdefiniert. Mithilfe des Kostenrollups können Sie Elemente von Kosten aggregieren, die von einem Kostenträger an einen anderen zugeteilt werden müssen. Wenn kein Kostenrollup verwendet wird, wird jedes einzelne Kostenelement von einem Kostenträger an einen anderen zugeteilt.

**Verrechnungssatz-Richtlinie**

Der Verrechnungssatz wird verwendet, um Preis pro Kostenträger zu berechnen. Um die Elemente des Preises zu verstehen, definieren Sie Verrechnungssatz-Richtlinien. Es gibt zwei Typen des Verrechnungssatzes: historischer Verrechnungssatz und Planverrechnungssatz. Ein historischer Verrechnungssatz ist ein berechneter Satz, der als Multiplikator für die Zuteilungsbasis eines Kostenträgers verwendet wird. Der Satz wird auf Grundlage der Kostenzuteilungen in der vorangegangenen Periode berechnet. Ein geplanter Satz ist ein benutzerdefinierter Satz.

**Dimensionshierarchie**

Dimensionshierarchien werden als Berichterstellungsstrukturen verwendet, wenn Sie Regeln für Zuteilung, Verrechnungssatz und Kostenrollup definieren, Aufstellungen oder Daten in Microsoft Excel anzeigen und den Zugriff auf die aggregierten Daten definieren. Es gibt zwei Dimensionshierarchien: Kategorisierungshierarchie und Klassifizierungshierarchie. Eine Kategorisierungshierarchie wird auf Grundlage von Kostenelementen definiert, während eine Klassifizierungshierarchie auf Grundlage von Kostenträgern definiert wird.

**Statistische Dimension**

Eine statistische Dimension ist der Ausdruck einer Anzahl oder Summe eines Objekts, die als Basis für Zuteilungen oder Verrechnungssatzberechnungen verwendet werden kann. Es wird entweder manuell erstellt oder aus Quellsystemen importiert. Beispiele zu statistischen Dimensionen sind unter anderem die Anzahl der Mitarbeiter, die Anzahl lizenzierter Software auf jedem Gerät, der Stromverbrauch jeder Maschine oder die Quadratmeter für eine Kostenstelle.

**Statistischer Eintrag**

Statistische Einträge enthalten die aufgezeichnete Summe oder den Anzahlwert für eine angegebene statistische Dimension. Die aufgezeichnete Summe oder der Anzahlwert wird auch als die Größe bezeichnet.




