---
title: Kostenrechnungsterminologie
description: "Dieses Thema definiert die Schlüsselbegriffe, die in der Kostenrechnung verwendet werden."
author: YuyuScheller
manager: AnnBe
ms.date: 08/31/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostAccountingLedger
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 223114
ms.assetid: 1c798592-77d0-4a8f-beaa-9159c75957da
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 1ec2f4a407c705fb37681f5593d0f7ea31f4cf0f
ms.contentlocale: de-de
ms.lasthandoff: 03/26/2018

---

# <a name="cost-accounting-terminology"></a>Kostenrechnungsterminologie

[!INCLUDE [banner](../includes/banner.md)]

Dieses Thema definiert die Schlüsselbegriffe, die in der Kostenrechnung verwendet werden.

**Verteilschlüssel**

Die Zuteilungsbasis wird verwendet, um Aktivitäten zu berechnen und zu quantifizieren, wie Maschinenstunden, die verwendet werden, Kilowattstunden, die verbraucht werden, oder die Grundfläche, die beansprucht wird. Sie wird als Basis zum Zuteilen von Kosten an einen oder mehrere Kostenträger verwendet

**Kostenrechnung**

Mit der Kostenrechnung können Sie Daten aus verschiedenen Quellen erfassen, wie beispielsweise das Hauptbuch, untergeordnete Sachkonten, Budgets und statistische Informationen. Sie können anschließend Kostendaten analysieren, zusammenfassen und auswerten, sodass die Verwaltung die bestmöglichen Entscheidungen bei Preisaktualisierungen, Budgets, Kostenkontrolle usw. treffen kann. Die Quelldaten, die für die Kostenanalyse verwendet werden, werden unabhängig in der Kostenrechnung gehandhabt. Daher wirken sich Aktualisierungen in der Kostenrechnung nicht auf die Quelldaten aus. Wenn Sie jedoch Kostendaten aus verschiedenen Quellen erfassen und insbesondere wenn Sie die Hauptkonten vom Hauptbuch in Microsoft Dynamics 365 for Finance and Operations als Kostenelemente importieren, gibt es eine Datenredundanz, da dieselben Daten im Hauptbuch und in der Kostenrechnung vorhanden sind. Diese Redundanz ist erforderlich, da Sie Finanzverwaltung für die externe Berichterstellung und Kostenrechnung für die interne Berichterstellung verwenden.

**Kostenrechnungssachkonto**

Durch Kalender, Währung und Kostenelementdimension definiert, steuert es Prozesse und Richtlinien zum Berechnen von Kosten. 

**Kosteneintrag**

Kosteneinträge sind das Ergebnis einer Übertragung über Datenkonnektoren von Hauptbucheinträgen, Kostenzuteilungen und gebuchten Kosteneinträgen in Kostenerfassungen.

**Kostenobjekt**

Jeder Objekttyp, der für die Kostensteuerung ausgewählt ist. Kosten oder Umsatzerlöse werden entweder direkt gebucht oder Kostenträgern zugewiesen. Einige typische Kostenträger sind:

-  Produkte
-  Projekte
-  Abteilungen
-  Kostenstellen

Verwaltung verwendet Kostenträger, um Kosten mengenmäßig zu bestimmen, aber auch um die Rentabilitätsanalyse voranzutreiben.

**Kostenelement**

Wird als Funktion verwendet, um Kosten nachzuverfolgen und zu kategorisieren. Es gibt zwei Typen von Kostenelementen: primäre und sekundäre.

Primäre Kostenelemente stellen den Kostenfluss von der Finanzbuchhaltung zur Kostenrechnung dar. Die Struktur entspricht normalerweise der Gewinn- und Verlustkontostruktur im Hauptbuch, wo ein Kostenelement einem Hauptkonto entsprechen kann. Nicht alle Hauptkonten müssen als Kostenelemente dargestellt werden, je nach den Geschäftsanforderungen. 

Sekundäre Kostenelemente stellen den internen Kostenfluss dar, da diese Kosten nur in der Kostenrechnung verwendet werden. Sie werden in Kostenrollupregeln zum Zusammenführen von Kosten in aussagekräftige Perioden verwendet, die von der Gemeindkostenberechnung verwendet werden. 

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

**Kostensteuerungseinheit**

Die Kostenkontrolleinheit stellt die Kostenstruktur dar. Die Struktur bestimmt wie Kosten in einer hierarchischen Reihenfolge zwischen Kostenträgerdimensionen und ihren entsprechenden Kostenträgern fließen. 

**Kostenverteilung**

Wird verwendet, um Kosten von einem Kostenträger zu einem oder mehreren anderen Kostenträgern zu verteilen, indem Sie eine relevante Zuteilungsbasis anwenden. Kostenverteilung und Kostenzuteilung unterscheiden sich darin, dass Kostenverteilung immer auf der Ebene des Primärkostenelements der ursprünglichen Kosten auftritt und keine umgekehrte Verarbeitung.

**Kostenzuweisung**

Wird verwendet, um den Saldo eines Kostenträgers zu anderen Kostenträgern zuzuteilen, indem eine Zuteilungsbasis angewendet wird. Finance and Operations unterstützt die gegenseitige Zuordnungsmethode. In der gegenseitigen Zuordnungsmethode werden die gegenseitigen Dienstleistungen, die Unterkostenobjekte austauschen, vollständig berücksichtigt werden. Das System bestimmt automatisch die Reihenfolge, in der die Zuteilungen ausgeführt werden und die Iteration erfolgt. Der Saldo eines Kostenträgers wird durch eine einzelne Verrechnungsgrundlage zugewiesen. Zuteilungen über Kostenträgerdimensionen hinweg und ihre jeweiligen Mitglieder werden unterstützt. Der Zuweisungsauftrag wird durch die Kostenkontrollsteuereinheit gesteuert.

**Kostenzuteilungsrichtlinie**

Eine Kostenzuteilungs-Richtlinie definiert die Beträge und Mengen, die zugeteilt werden müssen. Zuteilungsregeln enthalten Zuteilungsquellregeln, die die Kosten bestimmen, die zugeteilt werden, und Zuteilungszielregeln, die bestimmen, wo die Kosten zugeteilt werden. Beispielsweise sind alle Kosten für Raumdienstleistungen eine Zuteilungsquelle, die verschiedenen Abteilungen in einer Organisation zugeteilt werden können (das heißt zu Zuteilungszielen).

**Kostenrollup**

Der Zweck der Rollupregeln besteht darin, Kosten in aussagekräftige Perioden zusammenzuführen. Die Ebene Der Aggregation ist benutzerdefiniert und umfasst die Zuweisung eines sekundären Kostenelements. Wenn kein Kostenrollup verwendet wird, wird jedes Kostenelement von einem Kostenträger an einen anderen zugeteilt.

**Verrechnungssatz-Richtlinie**

Der Verrechnungssatz wird verwendet, um Preis pro Kostenträger zu berechnen. Um die Elemente des Preises zu verstehen, definieren Sie Verrechnungssatz-Richtlinien. Es gibt zwei Typen des Verrechnungssatzes: historischer Verrechnungssatz und Planverrechnungssatz. Ein historischer Verrechnungssatz ist ein berechneter Satz, der als Multiplikator für die Zuteilungsbasis eines Kostenträgers verwendet wird. Der Satz wird auf Grundlage der Kostenzuteilungen in der vorangegangenen Periode berechnet. Ein geplanter Satz ist ein benutzerdefinierter Satz.

**Dimensionshierarchie**

Es gibt zwei Dimensionshierarchien: Kategorisierungshierarchie und Klassifizierungshierarchie. Der Typ der Dimensionskategorisierungshierarchie wird für Berichterstellungszwecke verwendet. Er unterstützt nur die Kostenelementdimensionen. Der Typ der Dimensionsklassifizierungshierarchie wird zum Definieren von Richtlinien für Berichterstellungszwecke verwendet. Er unterstützt alle Dimensionen, wie Kostenobjekte, Kostenelemente und statistischen Dimensionen. 

**Datenkonnektor**

Kostenrechnung unterstützt die Integration von Daten aus Quellsystemen über einen Satz von Datenkonnektoren. Die folgenden Datenkonnektoren sind verfügbar:

-  Importierte Transaktionen (vorkonfiguriert)
-  Dynamics 365 for Finance and Operations (vorkonfiguriert)
-  Dynamics AX (Konfiguration erforderlich)

**Hinweis:** Der Datenkonnektor „Importierte Transaktionen” basiert auf Datenentitäten.

**Datenanbieter**

Die meisten Quellsysteme können Daten bereitstellen, die mindestens mit einer Datenquelle in der Kostenrechnung übereinstimmen. Um Daten aus Quellsystemen an der Datenquelle in der Kostenrechnung auszurichten, muss ein Datenanbieter konfiguriert werden. Die folgende Tabelle listet die Verfügbarkeit von Datenanbietern pro Datenkonnektor und Datenquelle auf.

|  **Datenquellen** |  **Importierter Transaktionsdatenkonnektor** | **Dynamics 365 for Finance and Operations, Enterprise Edition, Datenkonnektor**  | **Dynamics AX-Datenkonnektor**  |
|---|---|---|---|
| Kostenelement-Dimensionsmitglieder  |  Ja | Ja  | Ja  |
|  Mitglieder der Kostenobjektdimension |  Ja | Ja  | Ja  |
|  Mitglieder der statistischen Dimension | Ja  | Nr.  | Nr.  |
|  Hauptbuch | Ja  | Ja  | Ja  |
|  Budgeteinträge  | Ja  | Ja  | Ja  |
|  Statistische Kennzahlen | Ja  | Ja  | Ja  |

**Formel**

Mit Formelzuordnungsbasen können Sie erweiterte Formeln definieren, um die korrekte Zuordnungsbasis zu erreichen. Sie können Formelzuordnungsbasen manuell erstellen. Sie können die folgenden Operatoren verwenden, um die Formel zu definieren.

|  **Symbole** | **Text**  |
|---|---|
|  ( ) | Klammern  |
|  < |  Kleiner als |
|  > |  Größer als |
|  + |  Hinzufügung |
|  – |  Subtrahieren |
| *  | Multiplikation  |

Traditionelle IF-Anweisungen werden nicht unterstützt. Allerdings können Sie Anweisungen erstellen und überprüfen, ob sie erfüllt sind.

|  **Anweisungsüberprüfung** | **Ergebnis**  |
|---|---|
|  a > b| True  |
|  a > b |  False |

**Gemeinkosten**

Gemeinkosten beziehen sich auf die laufenden Kosten für das Betreiben eines Unternehmens. Es sind die Kosten, die nicht unmittelbar mit bestimmten Geschäftsaktivitäten verknüpft werden können. Hier sind einige Beispiele für Gemeinkosten:

-   Buchhaltungsgebühren
-   Abschreibungen
-   Versicherung
-   Interesse
-   Anwaltsgebühren
-   MwSt.
-   Kosten für Versorgungsunternehmen

**Gemeinkostensatz**

Sätze werden pro Kostenträger und Kostenelement definiert. Es gibt zwei Typen von Sätzen: Finanzzeitraum und benutzerdefiniert. Finanzzeitraumsätze werden durch die Gemeinkostenberechnung berechnet. Ein benutzerspezifischer Satz ist benutzerdefiniert und kann verwendet werden, um Kosten zwischen Kostenträgern anhand eines vordefinierten Satzes in der Gemeinkostenberechnung zuzuordnen.

**Publiziert**

Wenn Sie dieses Feld auf „Ja” festlegen, kann ein Benutzer, dem eine der folgenden Rollen zugewiesen wird, den Bericht im Arbeitsbereich „Kostensteuerung” anzeigen:

-  Kostenrechnungs-Manager
-  Kostenbuchhalter
-  Sachbearbeiter Kostenbuchhaltung
-  Kostenobjekt-Controller

Wenn Sie das Feld auf „Nein” festlegen, können nur Benutzer, denen eine der folgenden Rollen zugewiesen werden, den Bericht im Arbeitsbereich „Kostensteuerung” anzeigen:

-  Kostenrechnungs-Manager
-  Kostenbuchhalter
-  Sachbearbeiter Kostenbuchhaltung

**Statistische Dimension**

Eine statistischen Dimension und seine Mitgliedern werden verwendet, um nicht monetäre Einträge in der Kostenrechnung zu erfassen und zu steuern. Statistische Dimensionswerte können für beide Zwecke verwendet werden:

-  Als eine Zuteilungsbasis in Richtlinien wie beispielsweise Kostenverteilung oder Kostenzuteilung.
-  Für die Berichterstellung zum nicht monetären Verbrauch.

Eine statistische Dimension ist der Ausdruck einer Anzahl oder Summe einer Aktivität, die als Basis für Zuteilungen oder Satzberechnungen verwendet werden kann. Es wird entweder manuell erstellt oder aus Quellsystemen importiert. Beispiele zu statistischen Dimensionen sind unter anderem die Anzahl der Mitarbeiter, die Anzahl lizenzierter Software auf jedem Gerät, der Stromverbrauch jeder Maschine oder die Quadratmeter für eine Kostenstelle.

**Anweisung**

Aufstellungen sind Ansichten für die Manager, die für die Kostensteuerung verantwortlich sind. Anweisungen werden von einem Kostencontroller definiert und bieten einen schnellen Überblick über tatsächliche sowie budgetierte Kosten und Abweichungen. Ein Manager kann bei Bedarf weitere Details anzeigen. Um sicherzustellen, dass Mangern nur Daten angezeigt werden, für die sie verantwortlich sind, unterliegen Daten, die in Aufstellungen angezeigt werden, Zugriffsregeln.

**Version**

Versionen werden verwendet, um verschiedene Ergebnisse zu simulieren, anzuzeigen und zu vergleichen. Standardmäßig werden alle Istkosten in einer Basisversion angezeigt, die als *Tatsächlich* bekannt ist. Für Budgets und Berechnungen können Sie mit so vielen Versionen arbeiten, wie Sie benötigen. Beispielsweise können Sie Budgetdaten in eine ursprüngliche Version importieren und dann das Budget in einer überarbeiteten Version überarbeiten. Für Berechnungen können Sie mehrere Versionen erstellen. In diesen verschiedenen Versionen können Sie dann Berechnungen erstellen, indem Sie unterschiedliche Berechnungsregeln verwenden, die für die Kostenzuteilung angewendet werden.



