---
title: Planen Ihrer Organisationshierarchie
description: Bevor Sie Organisationen und Organisationshierarchien in  einrichten, sollten Sie sicherstellen, dass Sie planen, wie das Unternehmen modelliert wird.
author: sericks007
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: OMHierarchyManager, OMLegalEntity, OMOperatingUnit
audience: Application User
ms.reviewer: sericks
ms.custom: 17404
ms.assetid: babde0c6-bb5d-45ae-95ca-2af75a0ea292
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5bb0b306cca715cad64d62fff843987a8e98eb99
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2022
ms.locfileid: "9108763"
---
# <a name="plan-your-organizational-hierarchy"></a>Planen Ihrer Organisationshierarchie

[!include [banner](../includes/banner.md)]

Bevor Sie Organisationen und Organisationshierarchien einrichten, sollten Sie sicherstellen, dass Sie planen, wie das Unternehmen modelliert wird. Das Organisationsmodell hat bedeutende Auswirkungen auf die Implementierung sowie auf Unternehmensprozesse.

Organisationshierarchien stellen die Beziehungen zwischen den Organisationen dar, aus denen ein Unternehmen besteht. Daher ist die Struktur Ihres Unternehmens der wichtige Gesichtspunkt, wenn Sie Organisationen modellieren. Wir empfehlen, die Organisationsstrukturen auf Basis von Feedback der Führungskräfte und Bereichsleiter von Funktionsbereichen wie Finanzen und Buchhaltung, Personalverwaltung, Arbeitsgänge, Einkauf sowie Vertrieb und Marketing zu definieren.

Wenn Sie Hierarchien planen, ist es auch wichtig, die Beziehung zwischen der Organisationshierarchie und den Finanzdimensionen zu planen. Sie können mehrere Organisationshierarchien einrichten, um verschiedene Ansichten Ihres Unternehmens darzustellen. Wenn Sie Finanzdimensionen verwenden, können Sie Berichte auf Grundlage dieser Ansichten erstellen. Arbeiten Sie mit Ihrem Partner zusammen, um Hierarchien erstellen, die auf die organisationsbezogenen und gesetzlichen Berichterstellungsanforderungen eingehen.

> [!NOTE]
> Obwohl Sie Finanzdimensionen verwenden können, um die juristische Personen darzustellen, ohne die juristischen Personen zu erstellen, sind Finanzdimensionen nicht dafür angelegt, auf die betrieblichen oder geschäftlichen Anforderungen von juristischen Personen einzugehen. Die Interunit-Buchhaltungsfunktionen sind nur für die Buchhaltungseinträge vorgesehen, die durch die einzelnen Buchung erstellt werden.

> [!IMPORTANT]
> Sie sollten nicht nur auf Grundlage der Informationen in diesem Thema entscheiden, wie Sie Organisationen modellieren. Diese Dokumentation ist ein Handbuch. Sie können mit Ihrem Partner zusammenarbeiten, um weitere hilfreiche Informationen zu erhalten. Ihr Partner hat Erfahrung in diversen Branchen sowie mithilfe des Debitorenstamms gewonnen.

## <a name="decide-whether-to-model-internal-organizations-as-legal-entities-or-operating-units"></a>Festlegen, ob interne Organisationen als juristische Personen oder Organisationseinheiten modelliert werden

Sie müssen mindestens eine juristische Person haben, um Ihr Unternehmens darzustellen. Eine juristische Person kann Verträge abschließen und ist verpflichtet, Finanzaufstellungen zum Erstellen eines Berichts über ihre Vermögens-, Finanz- und Ertragslage vorzubereiten.

Es können juristischen Personen für Transaktionen oder für Konsolidierung verwendet werden. Das bedeutet, dass eine juristische Entität in Finanzen und Betrieb nicht unbedingt eine reale Entität in Ihrem Unternehmen darstellt. So kann ein Unternehmen, das an Transaktionen teilnimmt, juristische Person vom Typ Tochtergesellschaft besitzen. In diesem Szenario ist eine juristische Person für Buchungen obligatorisch, und eine virtuelle juristische Person ist erforderlich, um die Ergebnisse und Salden der Tochterfirmen zu konsolidieren.

Interne Organisationen in Ihrem Unternehmen, wie Zweigniederlassungen, können als weitere juristische Personen oder Organisationseinheiten der juristischen Hauptperson dargestellt werden. Eine Organisationseinheit muss keine gesetzlich definierte Organisation sein. Organisationseinheiten werden verwendet, um wirtschaftliche Ressourcen und betriebliche Prozesse im Unternehmen zu steuern. Beispielsweise sind Abteilungen und Kostenstellen Organisationseinheiten.

Einige Funktionen funktionieren unterschiedlich, abhängig davon, ob die Organisation eine juristische Person oder eine Organisationseinheit ist. Prüfen Sie sorgfältig die Funktionen wie nachfolgend beschrieben, wenn Sie die Entscheidung treffen.

### <a name="master-data"></a>Masterdaten

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Wenn die Organisation als juristische Person modelliert wird

Einige Masterdaten, wie Debitoren, Zahlungsbedingungen, Steuerbehörden und standortspezifische Bestandsbestellung, müssen für jede juristische Person eingerichtet wurden. Einige Masterdaten, wie Benutzer, Produkte und die meisten Personalverwaltungsdaten, werden von allen juristischen Personen geteilt.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Wenn die Organisation als Organisationseinheit modelliert wird

Masterdaten werden von Organisationseinheiten geteilt.

### <a name="module-parameters"></a>Modulparameter

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Wenn die Organisation als juristische Person modelliert wird

Parameter für Module, z.B. Debitorenparameter, Kreditorenkontenparameter und Bargeld- und Bankverwaltungsparameter, muss monatlich juristischen Person festgelegt werden. Da die Moduleinstellung für juristische Personen separat ist, kann jede Tochtergesellschaft den lokalen gesetzlichen Vorschriften und Geschäftspraktiken entsprechen. So können eine Dienstleistungs- und eine Produktions-juristische Person verschiedene Modulparameter haben, auch wenn sie dem gleichen übergeordneten Unternehmen unterstellt sind.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Wenn die Organisation als Organisationseinheit modelliert wird

Modulparameter werden von Organisationseinheiten geteilt.

### <a name="data-security"></a>Datensicherheit

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Wenn die Organisation als juristische Person modelliert wird

Die meisten Daten werden automatisch durch Unternehmens-ID geschützt. Ein Unternehmens-ID ist eine eindeutige Kennung für die Daten, die der juristischen Person zugeordnet sind. Ein Unternehmen kann nur einer juristischen Person zugeordnet sein, und eine juristische Person kann nur einem Unternehmen zugeordnet sein. Benutzer können nur auf Daten für die Unternehmen zugreifen, auf die sie Zugriff haben. Sie müssen nicht anpassen, um Daten mittels Unternehmens-ID zu speichern

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Wenn die Organisation als Organisationseinheit modelliert wird

Daten können pro Organisationseinheit geschützt werden, indem benutzerdefinierte Datensicherheitsrichtlinien erstellt werden. Datensicherheitsrichtlinien werden verwendet, um den Zugriff auf die Daten zu beschränken. Angenommen, ein Benutzer darf Bestellungen nur in einer bestimmten Organisationseinheit erstellen. Datensicherheitsrichtlinien können so erstellt werden, dass der Benutzer am Zugriff auf Bestellungsdaten von einer beliebigen anderen Organisationseinheit gehindert wird. Das Volumen von Buchungen sowie der Anzahl der Sicherheitsrichtlinien können sich auf die Leistung auswirken. Wenn Sie Sicherheitsrichtlinien entwerfen, denken Sie dabei auch an die Leistung.

### <a name="ledgers"></a>Sachkonten

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Wenn die Organisation als juristische Person modelliert wird

Für jede juristische Person ist ein Sachkonto erforderlich, das einen Kontoplan, Buchhaltungswährungen, Berichtswährungen und einen Steuerkalender umfasst. Eine Bilanz kann nur für eine juristische Person erstellt werden. Hauptkonten, Dimensionen, Kontostrukturen, Kontenpläne und Kontoregeln können von mehr als einer juristischen Person verwendet werden.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Wenn die Organisation als Organisationseinheit modelliert wird

Eine Organisationseinheit kann nicht eigene Sachkontoinformationen haben. Wenn Ihre internen Organisationen keine eindeutigen Sachkonten benötigen, können Sie diese als Organisationseinheiten modellieren. Sachkontoinformationen werden für die übergeordnete juristische Person in der Hierarchie eingerichtet. Einkommensaufstellungen können für Organisationseinheiten innerhalb einer juristischen Person oder für die Elemente juristische Person erstellt werden.

### <a name="fiscal-calendars"></a>Steuerkalender

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Wenn die Organisation als juristische Person modelliert wird

Jede juristische Person verfügt über einen eigenen Steuerkalender. Wenn Ihre internen Organisationen verschiedene Geschäftsjahre und Steuerkalender verwenden, müssen Sie die Organisationen als juristische Personen modellieren.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Wenn die Organisation als Organisationseinheit modelliert wird

Organisationseinheiten müssen einen Steuerkalender teilen. Wenn Ihre internen Organisationen die gleichen Geschäftsjahre und Steuerkalender verwenden können, können Sie die Organisationen als Organisationseinheiten modellieren.

### <a name="consolidation"></a>Konsolidierung

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Wenn die Organisation als juristische Person modelliert wird

Sie müssen die finanziellen Ergebnisse für Zweigniederlassungen in ein einzelnes, konsolidiertes Unternehmen konsolidieren, um Finanzaufstellungen zu erstellen.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Wenn die Organisation als Organisationseinheit modelliert wird

Konsolidierung ist nicht obligatorisch, da Daten bereits von Organisationseinheiten geteilt werden.

### <a name="centralized-payments"></a>Zentralisierte Zahlungen

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Wenn die Organisation als juristische Person modelliert wird

Zentralisierte Zahlungen müssen eingerichtet werden, damit Rechnungen für alle untergeordneten juristischen Personen an oder von einer einzelnen juristischen Person bezahlt werden können.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Wenn die Organisation als Organisationseinheit modelliert wird

Zentralisierte Zahlungen sind nicht erforderlich, da alle Rechnungen in einer einzelnen juristischen Person erfasst werden.

### <a name="intercompany-transactions"></a>Intercompany-Transaktionen

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Wenn die Organisation als juristische Person modelliert wird

Intercompany-Aufträge, Bestellungen, Zahlungen oder Zugänge können auch auf einander angewendet werden. Sie müssen keine Erfassungsbelege verwenden. Sie können Intercompany-Buchungen auf der Ebene für untergeordnete Sachkonten (Debitoren, Kreditoren) anzeigen. Die folgenden Beispiele veranschaulichen, wie innerbetriebliche Buchungen behandelt werden.

##### <a name="example-1-headquarters-provides-services-to-regional-offices-and-must-charge-the-costs-of-those-services-to-the-regional-offices"></a>Beispiel 1: Hauptsitz bietet Dienstleistungen für Zweigniederlassungen und muss die Kosten für diese Leistungen den Zweigniederlassungen berechnen.

Wenn Sie die Zweigniederlassung als juristische Person modellieren, stehen die folgenden Optionen zur Verfügung:

- Hauptsitz kann einen Erfassungseintrag erstellen, um die Zweigniederlassung für die Ausgaben zu belasten. Die Buchungen können nicht saldiert werden.
- Hauptsitz sendet eine Bestellung für Dienstleistungen an die Zweigniederlassung. Ein Auftrag wird automatisch in der juristischen Person für die Zweigniederlassung erstellt, mit Intercompany-Buchungen für untergeordnete Sachkonten.

##### <a name="example-2-headquarters-procures-and-pays-for-service-that-is-delivered-to-a-regional-office"></a>Beispiel 2: Hauptsitz beschafft und bezahlt Dienstleistungen, die an eine Zweigniederlassung geliefert werden.

Wenn Sie die Zweigniederlassung als juristische Person modellieren, stehen die folgenden Optionen zur Verfügung:

- Die Rechnung und die Zahlung folgen den regulatorischen Vorgaben vom Hauptsitz. Hauptsitz kann einen Erfassungseintrag erstellen, um die Zweigniederlassung für die Ausgaben zu belasten. Die Buchungen können nicht saldiert werden.
- Die Rechnung und die Zahlung folgen den regulatorischen Vorgaben vom Hauptsitz. Hauptsitz kann eine Intercompany-Buchung für untergeordnete Sachkonten erstellen.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Wenn die Organisation als Organisationseinheit modelliert wird

Intercompany-Buchungen unter Organisationseinheiten werden nur durch Erfassungsbelege unterstützt. Eine Organisationseinheit kann eine Bestellung, einen Auftrag oder eine Rechnung einer anderen Organisationseinheit in derselben juristischen Person nicht ausstellen oder von dieser empfangen. Sie können Intercompany-Buchungen nicht auf der Ebene für untergeordnete Sachkonten (Debitoren, Kreditoren) anzeigen. Die folgenden Beispiele veranschaulichen, wie innerbetriebliche Buchungen behandelt werden.

##### <a name="example-1-headquarters-provides-services-to-regional-offices-and-must-charge-the-costs-of-those-services-to-the-regional-offices"></a>Beispiel 1: Hauptsitz bietet Dienstleistungen für Zweigniederlassungen und muss die Kosten für diese Leistungen den Zweigniederlassungen berechnen.

Wenn Sie die Zweigniederlassung als Organisationseinheit modellieren, gibt der Hauptsitz eine Ausgabenbuchung ein und codiert sie für die Zweigniederlassung.

##### <a name="example-2-headquarters-procures-and-pays-for-service-that-is-delivered-to-a-regional-office"></a>Beispiel 2: Hauptsitz beschafft und bezahlt Dienstleistungen, die an eine Zweigniederlassung geliefert werden.

Wenn Sie die Zweigniederlassung als Organisationseinheit modellieren, folgen die Rechnung und die Zahlung den regulatorischen Vorgaben des Hauptsitzes. Die Rechnung kann für die Zweigniederlassung kodiert werden. Verwenden Sie auf der Einkommensaufstellung eine Ausgleichsfinanzdimension, um der Zweigniederlassung Kosten zu melden.

### <a name="local-tax-requirements"></a>Lokale Steueranforderungen

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Wenn die Organisation als juristische Person modelliert wird

Eine juristische Person unterliegt dem Steuerrecht der Steuerbehörde des Landes/der Region, in dem die juristische Person registriert ist. So unterliegt beispielsweise eine juristische Person, die in Dänemark registriert ist, den dänischen Steuergesetzen und Bestimmungen. Eine juristische Person kann nur einem Land/Region angehören. Mit dem für die primäre Adresse der juristischen Person ausgewählten Wert für Land/Region wird gesteuert, welche landes- oder regionsspezifischen Funktionen für diese juristische Person verfügbar sind. Wenn beispielsweise die primäre Adresse der juristischen Person in Dänemark ist, sind Funktionen, die sich auf die dänischen Steuergesetze und den Bestimmungen beziehen, verfügbar. Wenn sich Ihre Organisationen also in verschiedenen Ländern/Regionen befinden und verschiedene lokale Steueroptionen erfordern, müssen Sie die Organisationen als separate juristische Personen einrichten.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Wenn die Organisation als Organisationseinheit modelliert wird

Organisationseinheiten verwenden den Landeskontext der übergeordneten juristischen Person. Organisationseinheiten in derselben juristischen Person können nicht verschiedene länder-/regionsspezifische Anforderungen haben. Wenn Ihre Organisationen sich gleichen Land/Region befinden und die gleichen Steueroptionen verwenden, können diese als Organisationseinheiten einrichten.

### <a name="statutory-reporting-for-a-countryregion"></a>Gesetzlich vorgeschriebene Berichterstattung für ein Land/eine Region

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Wenn die Organisation als juristische Person modelliert wird

Bei Ländern/Regionen, die unterstützt werden, können die meisten Offenlegungsberichte erstellt werden. 

> [!NOTE]
> Ein Buchungsebene im Hauptbuch ermöglicht Anpassungseingaben an einer Muttergesellschaft vorzunehmen, die einen anderen Rechnungslegungsstandard als das untergeordnete Unternehmen verwendet. Beispielsweise können Sie für ein Unternehmen, das in Großbritannien allgemein anerkannte Buchhaltungsverfahren (UK GAAP) verwendet, Anpassungseingaben auf der Buchungsebene vornehmen. Diese Einträge können in ein übergeordnetes Unternehmen konsolidiert werden, das in den USA allgemein anerkannte Rechnungslegungsgrundsätze (GAAP) verwendet. Die Anpassungseingaben haben keinen Einfluss auf die UK GAAP-Berichterstellung.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Wenn die Organisation als Organisationseinheit modelliert wird

Offenlegungsberichte müssen erstellt werden, indem eine andere Anwendung verwendet wird. Sie müssen sicherstellen, dass die Daten in den Finanz- und Betriebs-Apps erfasst werden, um die Anforderungen der einzelnen operativen Einheiten zu unterstützen, sofern diese von den Anforderungen von headquarters abweichen.

### <a name="currency"></a>Währung

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Wenn die Organisation als juristische Person modelliert wird

Wenn Ihre Organisationen verschiedene gesetzliche Zahlungsmittel verwenden muss, müssen Sie die Organisationen als juristische Personen modellieren. Gesetzliche Zahlungsmittel werden pro juristische Person eingerichtet. Allerdings können Sie Buchungen in mehreren Währungen eingeben.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Wenn die Organisation als Organisationseinheit modelliert wird

Wenn Ihre Organisationen eine einziges gesetzliches Zahlungsmittel verwenden kann, können Sie die Organisationen als Organisationseinheiten modellieren. Organisationseinheiten müssen ein gesetzliches Zahlungsmittel teilen. Sie können jedoch in mehreren Währungen Buchungen eingeben und Berichte erstellen.

### <a name="year-end-closing"></a>Jahresabschluss

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Wenn die Organisation als juristische Person modelliert wird

Wenn Gesetze und Buchführungsmethoden sich zwischen den Ländern/Regionen unterscheiden, in denen sich Ihre Organisationen befinden, benötigen Sie möglicherweise für jede Organisation ein anderes Jahresabschlussverfahren. Das bedeutet, dass die Organisationen als juristische Personen modellieren müssen. Jede juristische Person verfügt über eigene Jahreabschlussverfahren.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Wenn die Organisation als Organisationseinheit modelliert wird

Wenn Gesetze und Buchführungsmethoden sich zwischen den Ländern/Regionen unterscheiden, in denen sich Ihre Organisationen befinden, können Sie einen einheitlichen Satz von Jahresabschlussverfahren verwenden. Das bedeutet, dass Sie die Organisationen als Organisationseinheiten modellieren können. Alle Organisationseinheiten müssen dasselbe Jahresabschlussverfahren verwenden.

### <a name="number-sequences"></a>Nummernkreise

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Wenn die Organisation als juristische Person modelliert wird

Nummernkreise für einige Referenzen können pro juristische Person eingerichtet wurden. Einige Nummernkreise können gemeinsam sein.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Wenn die Organisation als Organisationseinheit modelliert wird

Nummernkreise für einige Referenzen können pro Organisationseinheit eingerichtet wurden. Einige Nummernkreise können gemeinsam sein.

### <a name="products"></a>Produkte

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Wenn die Organisation als juristische Person modelliert wird

Produktdefinitionen werden freigegeben, und sie müssen für einzelne juristischen Personen freigegeben werden, bevor sie in Transaktionen berücksichtigt werden können. Jede juristische Person verfügt über einen eigenen Satz freigegebener Produkte, die in die Buchungsdokumente einbezogen werden sollen. Wenn Ihre interne Organisationen verschiedene Gruppen von Produkten verwenden muss, müssen Sie die Organisationen als juristische Personen modellieren.

> [!NOTE]
> Obwohl Produktdefinitionen geteilt werden, können Sie in jeder juristischen Person, in der ein Produkt freigegeben wurde, verschiedene Verkaufs-, Einkaufs- und Lagerparameter für den Artikel an jedem Lagerstandort angeben.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Wenn die Organisation als Organisationseinheit modelliert wird

Alle Organisationseinheiten teilen die gleiche Gruppe von Produkten. Wenn Ihre internen Organisationen die gleiche Gruppe von Produkten gemeinsam verwenden können, können Sie die Organisationen als Organisationseinheiten modellieren.

### <a name="inquiry-and-reporting"></a>Abfrage und Berichterstellung

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Wenn die Organisation als juristische Person modelliert wird

Sie müssen Unternehmen manuell ändern, um Buchungen einzugeben und Abfragen in mehreren juristischen Personen auszuführen. Aufgrund der Datensicherheitsgrenzen können konsolidierte Abfrage und Berichterstellung ressourcenintensiv und zeitraubend sein.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Wenn die Organisation als Organisationseinheit modelliert wird

Sie müssen nicht Unternehmen ändern, um von mehreren Organisationseinheiten aus auf Daten zuzugreifen. Konsolidierte Abfrage und Berichterstellung und einzelne regionale Abfrage ist und schneller einfacher.

## <a name="best-practices-for-modeling-organizations-and-hierarchies"></a>Optimale Verfahren zum Entwerfen von Organisationen und Hierarchien

Berücksichtigen Sie die folgenden optimalen Verfahren bei der Implementierung einer Organisationshierarchie:

- Erstellen Sie eine Abteilung, um die Schnittstelle zwischen einer juristischen Person und einer Unternehmenseinheit zu entwerfen. Anschließend lassen sich Daten von einer Abteilung zu einer juristischen Person für gesetzlich vorgeschriebene Berichte und von einer Abteilung zu einer Unternehmenseinheit für interne Berichte aufschlüsseln. Abteilungen können als Profitcenter dienen. Bei der Verwendung von Abteilungen ist es nicht notwendig, sowohl juristische Personen als auch Unternehmenseinheiten als Dimensionen in der Kontostruktur zu verwenden. Sie können nur Abteilungen als Dimension verwenden. Sie müssen jedoch Kostenstellen und Abteilungen als Dimensionen in der Kontostruktur verwenden, wenn Kostenstellen nur als Kostenakkumulator und Abteilungen zur Umsatzerkennung verwendet werden.
- Entwerfen Sie mehrere Hierarchien für Organisationseinheiten, falls komplexe Anforderungen für Gewinn- und Verlustberichte bestehen.
- Modellieren Sie nicht in einer einzigen juristischen Person mehrere Hierarchien für den gleichen Hierarchiezweck.
- Erstellen Sie nicht für jeden Zweck eine Hierarchie. In der Regel können Sie eine Hierarchie für mehrere Zwecke verwenden. Beispielsweise kann eine Hierarchie mit Organisationseinheiten allen richtlinienbezogenen Zwecken zugewiesen werden.
- Erstellen Sie ausgeglichene Hierarchien. In einer Hierarchie werden alle Knoten mit derselben Entfernung zum Stammknoten als Ebene definiert. In einer ausgeglichenen Hierarchie kann nur ein Organisationseinheitstyp pro Ebene vorhanden sein, und die Entfernung zum Stammknoten von jeder Ebene ist einheitlich. Sind Zwischenebenen zwischen einer Abteilung und einer juristischen Person bzw. einer Unternehmenseinheit vorhanden, sind u. U. Platzhalterorganisationen erforderlich, um eine ausgeglichene Hierarchie erstellen zu können.
- Entwerfen Sie keine separate Hierarchie mit Organisationseinheiten, falls die Struktur für juristische Personen auch der Organisationsstruktur entspricht. Eine gemischte Hierarchie mit juristischen Personen und Organisationseinheiten kann beide Zwecke erfüllen.
- Verwenden Sie vor dem Entwerfen von umfassenden Neustrukturierungsszenarien die Gültigkeitsdaten der Hierarchie, um eine Auswirkungsanalyse und einen Validierungstest durchzuführen.
- Verwenden Sie zum Ändern einer Hierarchie den Entwurfsmodus, bevor Sie eine neue Version in einer Produktionsumgebung veröffentlichen.
- Begrenzen Sie die Anzahl der Personen, die zum Hinzufügen oder Entfernen von Organisationen von einer Hierarchie in einer Produktionsumgebung berechtigt sind. Durch eine kleinere Anzahl verringert sich die Wahrscheinlichkeit für kostspielige Fehler und Korrekturen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

