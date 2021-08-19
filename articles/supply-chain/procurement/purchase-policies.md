---
title: Überblick über die Einkaufsrichtlinien
description: Dieser Artikel enthält Informationen zu Einkaufsrichtlinien. Eine Einkaufsrichtlinie ist Sammlung von Regeln, mit denen der Bestellanforderungsprozess kontrolliert wird. Einkaufsrichtlinien unterstützen Beschaffungsadministratoren beim Implementieren der Beschaffungsstrategie, indem eine Richtlinienstruktur erstellt wird, die auf die Anforderungen einer Organisation für den strategischen Einkauf ausgerichtet ist.
author: kamaybac
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqSourcingPolicyRule, SysPolicy, SysPolicyListPage, PurchReqControlRule, RequisitionReplenishCatAccessPolicyRule, PurchReApprovalPolicyRule, RequisitionReplenishControlRule, PurchReqControlRFQRule
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "11614"
- intro-internal
ms.assetid: 729a304d-0f3f-4ccb-bd5b-46ee0976c57f
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4fd090f6e8b91c6a75eced17fadd76f686c5441f1526736534ad1a947d80cea0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6761781"
---
# <a name="purchasing-policies-overview"></a>Überblick über die Einkaufsrichtlinien

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen zu Einkaufsrichtlinien. Eine Einkaufsrichtlinie ist Sammlung von Regeln, mit denen der Bestellanforderungsprozess kontrolliert wird. Einkaufsrichtlinien unterstützen Beschaffungsadministratoren beim Implementieren der Beschaffungsstrategie, indem eine Richtlinienstruktur erstellt wird, die auf die Anforderungen einer Organisation für den strategischen Einkauf ausgerichtet ist.

Eine Einkaufsrichtlinie besteht aus einer Gruppe von Richtlinienregeln. Beim Definieren einer Richtlinienregel wird zuerst ein Regeltyp ausgewählt. Dann erstellen Sie eine Regel für den Richtlinientyp, indem Sie Einstellungen, Startdatum und Enddatum der Regel definieren.  

Ein Administrator erstellt beispielsweise eine Richtlinie, wählt den Regeltyp **Katalogrichtlinienregel** aus, und fügt der Richtlinie dann eine Katalogrichtlinienregel hinzu. Diese Katalogrichtlinienregel legt fest, dass der Adventure-Katalog zur internen Beschaffung verwendet werden muss. Nachdem die Einkaufsrichtlinie einer bestimmten Organisation zugeordnet wurde, können Mitarbeiter dieser Organisation den Adventure-Katalog beim Erstellen von Anforderungen sehen.

## <a name="assigning-policies-to-organizations"></a>Zuweisen von Richtlinien zu Organisationen
Eine Richtlinie kann erst in Kraft treten, wenn sie einer Organisation zugeordnet ist. Einkaufsrichtlinien werden dem Hierarchiezweck **Beschaffung – interne Kontrolle** zugeordnet. Daher können Einkaufsrichtlinien nur auf Organisationen in Hierarchien angewendet werden, die den Hierarchiezweck **Beschaffung – interne Kontrolle** aufweisen. Sie können auch Organisationen aus der Liste der juristischen Personen in der Tabelle "CompanyInfo" auswählen. Diese juristischen Personen werden im Richtlinienframework als "Unternehmen" bezeichnet.

## <a name="determining-which-rule-to-apply"></a>Bestimmen der anzuwendenden Regel
Abhängig von der Konfiguration der Einkaufsrichtlinien können mehrere Regeln die Benutzer in einer Organisation betreffen. In den folgenden Beispielen werden verschiedene Arten zur Konfiguration von Einkaufsrichtlinien veranschaulicht. Zudem wird erläutert, wie Richtlinien angewendet werden, wenn eine Buchung stattfindet.

### <a name="example-1-simple-purchasing-policy-configuration"></a>Beispiel 1: Konfiguration einfacher Einkaufsrichtlinien

Organisationen, die klein und weniger komplex sind, können Einkaufsrichtlinien nach juristischer Person einrichten und nur die Organisationshierarchie Unternehmen verwenden.  

Bei Fabrikam, einem kleinen Unternehmen, gibt es bei den Einkaufsanforderungen nur geringfügige Abweichungen innerhalb der Organisation. Die Einkaufsregeln variieren nur zwischen den juristischen Personen der Organisation. Mitarbeiter von Fabrikam Kanada und Mitarbeiter von Fabrikam USA kaufen Waren und Dienstleistungen aus verschiedenen Katalogen und bei verschiedenen Lieferanten. Fabrikam richtet die Einkaufsrichtlinien daher auf der Ebene der juristischen Personen ein.  

Fabrikam erstellt zwei Einkaufsrichtlinien. Richtlinie A betrifft die juristische Person 1111 USA. Richtlinie B betrifft die juristische Person 2222 Kanada. Wenn ein Mitarbeiter in juristischen Person 1111 eine Bestellanforderung erstellt, werden die Richtlinienregeln aus der Richtlinie A., beispielsweise den Produktkatalog, den der Mitarbeiter angegeben in der Katalogrichtlinienregel für Richtlinie A. werden.  

Wenn ein Mitarbeiter in juristischen Person 2222 eine Bestellanforderung erstellt, werden die Richtlinienregeln aus der Richtlinie B abgeleitet.  

**Hinweis:** Wenn ein Mitarbeiter der juristischen Person 1111 einen Artikel im Auftrag eines Mitarbeiters der juristischen Person 2222 kauft, werden die für die juristische Person 2222 angegebenen Richtlinienregeln aus Richtlinie B angewendet.

### <a name="example-2-complex-purchasing-policy-configuration"></a>Beispiel 2: Konfiguration komplexer Einkaufsrichtlinien

Im vorherigen Beispiel wurden alle Richtlinienregeln in einer einzelnen Organisationshierarchie definiert, und zwar der Organisationshierarchie Unternehmen. In einer komplexen Organisation können allerdings Richtlinien für mehrere Organisationshierarchien definiert werden.  


Contoso ist ein großes Unternehmen, das komplexe Einkaufsregeln benötigt, um den Bestellanforderungsprozess zu kontrollieren. Contoso hat Regeln für zwei verschiedene Organisationshierarchien definiert: Abteilung und Globale Einkaufskontrolle.  

Richtlinie 123 ist für die Organisationshierarchie "Abteilung" für "Verkauf UK – Vertriebsabteilung" definiert. In Richtlinie 123 legt die Regel "Bestellanforderungskontrolle" fest, dass Einschränkungen zu Mindestbestellmengen erzwungen werden müssen. In dieser Regel ist die Option **Einschränkungen der Mindestbestellmenge erzwingen** ausgewählt.  

Richtlinie 456 ist für die Organisationshierarchie "Globale Einkaufskontrolle" für "Verkauf UK – Vertriebs- und Marketingabteilung" definiert. In Richtlinie 456 legt die Regel "Bestellanforderungskontrolle" nicht fest, dass Einschränkungen zu Mindestbestellmengen erzwungen werden müssen. In dieser Regel ist die Option **Einschränkungen der Mindestbestellmenge erzwingen** abgewählt.  

Sam ist Mitarbeiter von Verkauf GB – Vertriebsabteilung in der Contoso Niederlassung im Vereinigten Königreich. Auf seine Abteilung treffen sowohl die Richtlinien für die Organisationshierarchie "Abteilung" als auch für die Organisationshierarchie "Globale Einkaufskontrolle" zu. Wenn Steffen eine Bestellanforderung erstellt, muss vom System ermittelt werden, welche Richtlinie angewendet wird. Der Systemadministrator richtet die Einkaufsrichtlinienparameter ein, um festzulegen, dass Einkaufsrichtlinien in der folgenden Reihenfolge angewendet werden müssen:

1.  Globale Einkaufskontrolle
2.  Abteilung
3.  Unternehmen

Daher wird Richtlinie 456 auf Bestellanforderung angewendet, die Steffen erstellt, und keine minimale Auftragsmenge für die Bestellanforderung ist erforderlich.

## <a name="policy-rules"></a>Richtlinienregeln
### <a name="catalog-policy-rule"></a>Katalogrichtlinienregel

Die Katalogrichtlinienregel bestimmt, welchen Beschaffungskatalog Benutzer sehen, wenn sie Bestellanforderungen erstellen. Wenn einem Benutzer die Berechtigung zum Anfordern von Produkten für andere Benutzer erteilt wurde, wird in der Anforderung anhand der für die juristische Person und Organisationseinheit der anfordernden Person definierten Katalogrichtlinienregel der Beschaffungskatalog bestimmt, der angezeigt werden soll. Bevor eine Katalogrichtlinienregel definiert werden kann, erstellen und veröffentlichen Sie einen Beschaffungskatalog.

### <a name="category-access-policy-rule"></a>Richtlinienregel für Kategoriezugriff

Die Richtlinienregel für Kategoriezugriff bestimmt, auf welche Kategorien Benutzer Zugriff haben, wenn sie Bestellanforderungen erstellen. Wenn keine Regel festgelegt ist, können alle Beschaffungskategorien der Bestellanforderung hinzugefügt werden.

1.  Aktivieren Sie die Option **Übergeordnete Regel einschließen**, um die Kategoriezugriffs-Richtlinienregel der übergeordneten Organisation auf die Kategorie anzuwenden.
2.  Wählen Sie im Bereich **Verfügbare Kategorien** die Kategorien aus, für die diese Regel gelten soll. Wenn Sie eine Kategorie auswählen, werden alle Kategorien, die in der Hierarchie höher sind, der Liste **Ausgewählte Kategorien** ebenfalls hinzugefügt.
3.  Aktivieren Sie die Option **Unterkategorien einschließen**, um die Regel auf alle Unterkategorien der ausgewählten Kategorie anzuwenden.

### <a name="category-policy-rule"></a>Kategorierichtlinienregel

Die Kategorierichtlinienregel definiert, wie Benutzer Kreditoren für jede Kategorie auswählen können. Sie definieren auch Anforderungen für die Eingangs- und Fakturierungsprozesse.

### <a name="re-approval-rule-for-purchase-orders"></a>Regel für die erneute Genehmigung von Bestellungen

Die Regel für die erneute Genehmigung ist eine optionale Regel, die Kriterien für die Erforderlichkeit einer erneuten Genehmigung definiert, wenn eine Bestellung geändert wird. Die ausgewählten Felder werden in den Bestellungsworkflow ausgewertet, wenn die Bedingung "Bestellungswiedergenehmigung" eingerichtet wird im Workflow.

> [!NOTE]
> Buchhaltungsverteilung wird immer zurückgesetzt, wenn eine genehmigte Bestellung mit aktiviertem Änderungsmanagement geändert wird. Falls Sie eine erneute Genehmigung einer Bestellung verhindern möchten, wenn bestimmte Felder geändert werden, sollten Sie daran denken, dass das Feld Buchhaltungsverteilung.geändert NICHT als ausgewähltes Feld für eine erneute Genehmigung einbezogen werden darf. 

### <a name="purchase-requisition-rfq-rule"></a>Angebotsanforderungsregel für Bestellanforderung

Mit der Bestellanforderungsregel wird anhand von Kriterien definiert, wann für eine Bestellanforderungsposition eine Angebotsanforderung erforderlich ist. Wenn eine Position die Bedingungen entspricht, erscheint der Stempel "informelle Angebotsanforderung "oder "formelle Angebotsanforderung" für die Anforderungsposition.

### <a name="purchase-requisition-control-rule"></a>Bestellanforderungs-Steuerungsregel

Die Bestellanforderungssteuerungsregel für Bestellanforderungen vom Typ **Verbrauch** ist eine optionale Regel. Wenn Sie Regeln dieses Typs erstellen, können Sie Optionen auf verschiedenen Registerkarten festlegen:

-   Auf der **Workflowübermittlung**-Registerkarte können Sie die Felder konfigurieren, die auf die Bestellanforderungsposition eingegeben werden müssen, damit die Anforderung zur Genehmigung übermittelt werden kann.
-   Auf der **Bestellmengen** Registerkarte können Sie die Felder konfigurieren, die in der Bestellanforderung unter bestimmten Bedingungen erforderlich sind. Sie können Bestellmengen auch erzwingen.
-   Auf der **Datumsangaben** Registerkarte können Sie konfigurieren, ob der Abschlussstichtag der gleiche wie das angeforderte Datum ist
-   Auf der **Adresse** Registerkarte können Sie definieren, ob der Benutzer neue Adressen im System erstellen darf, um sie auf die Bestellanforderung anzuwenden.

### <a name="requisition-purpose-rule"></a>Anforderungszweckregel

Die Anforderungszweckregel ist eine optionale Regel, die den Typ des Anforderungszweckes bestimmt, der für eine bestimmte juristische Person zulässig ist. Soweit in dieser Regel kein anderer Zweck angegeben ist, können Anforderungen automatisch einen Zweck **Verbrauch** haben, wenn sie erstellt werden.

### <a name="replenishment-category-access-policy-rule"></a>Richtlinienregel für Auffüllungskategoriezugriff

Die Richtlinienregel für Auffüllungskategoriezugriff ist eine optionale Regel, die die Produkte bestimmt, die verfügbar sind, um Anforderungsbedarf für eine bestimmte juristische Person zu erfüllen, wenn der Anforderungszweck **Auffüllung** ist.

### <a name="replenishment-control-rule"></a>Regel für die Auffüllungssteuerung

Die Regel für die Auffüllungssteuerung ist eine optionale Regel, die die Felder definiert, die auf der Bestellanforderungsposition eingegeben werden müssen, damit die Anforderung zur Genehmigung übermittelt werden kann, wenn der Anforderungszweck **Auffüllung** ist.

### <a name="purchase-order-creation-and-demand-consolidation-rule"></a>Regel für die Erstellung von Bestellungen und die Bedarfskonsolidierung

Die Richtlinie definiert Richtlinienregeln, die beim Generieren einer Bestellung verwendet werden sollen, die auf einer genehmigten Bestellanforderung basiert. Wenn Sie Regeln dieses Typs erstellen, können Sie Optionen auf verschiedenen Registerkarten festlegen:

-   Auf der Registerkarte **Bestellungsaufteilung** können Sie durch Definieren von Kriterien angeben, wann Bestellanforderungspositionen auf separate Bestellungen aufgeteilt werden sollen.
-   Auf der **Preis/Rabatt-Übertragung** Registerkarte können Sie definieren, wann die Preisvereinbarung neu berechnet werden soll, wenn eine Bestellung erstellt wird:
    -   **Nur bei nicht vorhandener Handelsvereinbarung** - Preise und Rabatte werden aus der Bestellanforderung übertragen, wenn es keine entsprechende Handelsvereinbarung oder Basispreis gibt. Wenn eine Handelsvereinbarung oder ein Basispreis für den Artikel oder Kreditor vorliegt, werden die Preise und Rabatte auf Basis der Handelsvereinbarung oder Basispreis neu berechnet und in die Bestellung übernommen. Wenn nicht anders angegeben, ist dies das Standardverhalten.
    -   **Immer** - Preise und Rabatte werden immer aus der Bestellanforderung übertragen.

    Sie können der anfordernden Person auch gestatten, die Methode der Preis- und Rabattübertragung für einzelne Bestellanforderungspositionen zu ändern, unabhängig von der Preis/Rabattübergangsregel, die festgelegt ist. Aktivieren Sie die Option **Manuelle Aufhebung pro Bestellanforderungsposition zulassen**, wenn Sie diese Funktion aktivieren möchten.
-   Auf der **Artikelbezeichnungs-Übertragung** Registerkarte können Sie die Artikelbeschreibung aus der Anforderung übertragen, wenn sie aus einer Angebotsanforderung stammt.
-   Auf der Registerkarte **Preistoleranz** können Sie Preistoleranzregeln definieren, um genehmigte Bestellanforderungen erneut durch den Prüfprozess zu leiten, wenn sich der Preis eines Beschaffungskatalogartikels erhöht. Legen Sie den maximalen Betrag fest, um den der Nettobetrag einer Position in einer Bestellanforderung zwischen der Genehmigungszeitpunkt der Bestellanforderung und dem Erstellungszeitpunkt der Bestellung erhöht werden kann. Der Nettobetrag wird berechnet, indem die folgende Formel verwendet wird: (\[Menge × (Preis je Einheit – Rabatt) ÷ Preiseinheit\] + Sonstige Zuschläge) × (100 – Rabattprozent) ÷ 100. Bestellanforderungspositionen, die die Preistoleranz überschreiten, müssen manuell verarbeitet werden. Mit den auf der Registerkarte **Fehlerverarbeitung** konfigurierten Regeln wird bestimmt, wie die Bestellanforderungspositionen verarbeitet werden.
-   Auf der Registerkarte **Fehlerverarbeitung** konfigurieren Sie die Verarbeitungsregel, die auf eine Bestellanforderung angewendet wird, wenn die Prüfung bei der Erstellung der Bestellung aufgrund eines Kreditoren- oder Preistoleranzfehlers nicht erfolgreich ist. Folgende Optionen stehen zur Auswahl:
    -   **Keine Aktion** – Die Bestellanforderungspositionen verbleiben auf der **Genehmigte Bestellanforderungen freigeben** Seite. Der Status der Bestellanforderungspositionen ist weiterhin **Genehmigt**. Die Fehler müssen jedoch behoben werden, bevor für die Bestellanforderungspositionen eine Bestellung generiert werden kann.
    -   **Bestellanforderungsposition stornieren** – Die Bestellanforderungspositionen werden storniert. Die anfordernde Person kann eine neue Bestellanforderung für die stornierten Positionen erstellen, wenn sie die Positionen immer noch anfordern möchten.
    -   **Neue Bestellanforderungsposition erstellen** – Die Bestellanforderungspositionen werden storniert. Es werden dann neue Bestellanforderungen generiert, die nur die Bestellanforderungspositionen enthalten, für die die Prüfung nicht erfolgreich war. Die neuen Bestellanforderungen, die generiert werden, haben den Status **Entwurf**. Diese Bestellanforderungen können erneut zur Prüfung übermittelt werden, nachdem die Prüfungsfehler behoben wurden. Der Antragsteller der Bestellanforderungspositionen wird benachrichtigt, dass die Positionen storniert wurden und dass für die Bestellanforderungspositionen, deren Prüfung nicht erfolgreich war, neue Bestellanforderungen generiert wurden.
-   Auf der Registerkarte **Manuelle Erstellung der Bestellung** definieren Sie dann die Parameter, mit denen ermittelt wird, ob eine Bestellanforderung manuell verarbeitet werden muss oder ob sie automatisch in eine Bestellung konvertiert werden kann. Die Parameter können auf interne Katalogartikel, externe Katalogartikel oder Nicht-Katalogartikel angewendet werden. Folgende Optionen stehen zur Auswahl:
    -   **Bestellungen manuell erstellen** – Bestellungen für alle genehmigten Bestellanforderungen manuell erstellen.
    -   **Bestellungen automatisch erstellen**– Automatisches Erstellen von Bestellungen für alle genehmigten Bestellanforderungen. Es werden keine Bestellanforderungen für die manuelle Erstellung von Bestellungen vorgesehen.
    -   **Bestellungen automatisch erstellen, sofern nicht die folgenden Bedingungen zutreffen** – Manuelles Erstellen von Bestellungen für alle Bestellanforderungen, die den Kriterien entsprechen, die Sie definieren. Alle anderen Bestellanforderungen, die genehmigt wurden, werden automatisch in Bestellungen konvertiert. Wenn Sie **Bestellungen automatisch erstellen, sofern nicht die folgenden Bedingungen zutreffen** auswählen, können Sie Beschaffungskategorien und Kreditoren hinzufügen, um anzugeben, welche genehmigten Bestellanforderungspositionen manuell verarbeitet werden müssen. Diese Option kann auf interne Katalogartikel, externe Katalogartikel und Nicht-Katalogartikel angewendet werden. Wenn Sie eine Beschaffungskategorie auswählen, werden auch Unterkategorien für diese Beschaffungskategorie ausgewählt. Wählen Sie die Option **Alle** für einen speziellen Typ von Bestellanforderungsposition aus, um alle Positionen dieses Positionstyps für die manuelle Verarbeitung vorzusehen.

    Wenn Bestellungen automatisch aus genehmigten Bestellanforderungen generiert werden sollen, wenn der Stapelverarbeitungsauftrag zum Generieren von Bestellungen ausgeführt wird, aktivieren Sie die Option **Automatische Bestellungserstellung als Stapelverarbeitungsauftrag ausführen**. Diese Option gilt nur für Bestellanforderungen, die keine manuelle Bearbeitung erfordern. Indem die automatische Generierung von Bestellungen als Stapelverarbeitungsauftrag ausgeführt wird, können Sie diese Aktivität zu einer Zeit einplanen, zu der die Ressourcen weniger ausgelastet sind. Wenn die Option **Vorauszahlung erforderlich** für Bestellanforderungspositionen aktiviert ist, aktivieren Sie die Option **Wenn die Anforderung für die Vorauszahlung eingerichtet ist**, um genehmigte Bestellanforderungen für die manuelle Verarbeitung vorzusehen. Bestellanforderungspositionen, die für die manuelle Verarbeitung vorgesehen sind, können gefiltert werden, um nur die Bestellanforderungen anzuzeigen, die eine Vorauszahlung erfordern.
-   Auf der Registerkarte **Bedarfskonsolidierung** definieren Sie die Parameter, mit denen ermittelt wird, ob manuell verarbeitete Bestellanforderungen für die Bestellanforderungskonsolidierung berücksichtigt werden können. Die Parameter können auf interne Katalogartikel, externe Katalogartikel oder Nicht-Katalogartikel angewendet werden. Folgende Optionen stehen zur Auswahl:
    -   **Keine Bedarfskonsolidierung zulassen** – Keine genehmigten Bestellanforderungspositionen kommen für die Bedarfskonsolidierung in Frage. Diese Option ist standardmäßig ausgewählt und betrifft nur Bestellanforderungspositionen, die zur Erstellung einer Bestellung manuell verarbeitet werden müssen.
    -   **Immer Bedarfskonsolidierung zulassen** – Alle genehmigten Bestellanforderungspositionen kommen für die Bedarfskonsolidierung in Frage. **Hinweis:** Wenn Sie die Option **Immer Bedarfskonsolidierung zulassen** auf der Registerkarte **Bedarfskonsolidierung** auswählen, jedoch die Option **Bestellungen automatisch erstellen** auf der Registerkarte **Manuelle Erstellung der Bestellung** auswählen, werden alle Bestellanforderungen für die manuelle Bearbeitung vorgesehen.
    -   **Bedarfskonsolidierung unter diesen Bedingungen zulassen** – Definieren Sie die Kriterien, die bestimmen, ob genehmigte Bestellanforderungspositionen für die Bedarfskonsolidierung infrage kommen. Für jeden Typ der Bestellanforderungsposition können Sie die Kriterien nach Beschaffungskategorie und Kreditor festlegen. Wenn Sie die Option **Bedarfskonsolidierung unter diesen Bedingungen zulassen** auswählen, können Sie die Kriterien nach Beschaffungskategorie und Kreditor für jeden Typ der Bestellanforderungsposition festlegen. Wenn Sie eine Beschaffungskategorie auswählen, werden auch Unterkategorien für diese Beschaffungskategorie ausgewählt. Wenn Sie die Option **Alle** für einen bestimmten Positionstyp auswählen, kommen alle Bestellanforderungspositionen dieses Positionstyps für die Bedarfskonsolidierung in Frage.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]