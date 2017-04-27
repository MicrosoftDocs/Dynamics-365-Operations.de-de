---
title: Projektverwaltung und -verrechnung
description: "Die Projektverwaltungs- und Buchhaltungsfunktionen können in mehreren Branchen verwendet werden, um eine Dienstleistung anzubieten, ein Produkt zu erzeugen oder ein Ergebnis zu erreichen."
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 7bfacfe69aed9b64d71760181d9a1683b86cbf44
ms.lasthandoff: 03/31/2017


---

# <a name="project-management-and-accounting"></a>Projektverwaltung und -verrechnung

Die Projektverwaltungs- und Buchhaltungsfunktionen können in mehreren Branchen verwendet werden, um eine Dienstleistung anzubieten, ein Produkt zu erzeugen oder ein Ergebnis zu erreichen.  

Ein Projekt ist eine Gruppe von Aktivitäten, die vorgesehen sind, um einen Service bereitzustellen, ein Produkt zu erzeugen oder ein Ergebnis zu erreichen. Projekte nach Ressourcen und generieren finanziellen Ergebnisse in Form von Umsatzerlösen oder Anlagen.

## <a name="projects-across-industries"></a>Projekte in Branchen
Die Projektverwaltungs- und Buchhaltungsfunktionen kann in mehreren Branchen, wie in der folgenden Abbildung dargestellt, verwendet werden. [![Projekte in Branchen](./media/projects-accross-industries.jpg)](./media/projects-accross-industries.jpg) 

In einem Callcenter kann ein Ticket verwendet werden, um die Gruppe von Aktivitäten zu beschreiben, die erforderlich sind, um einen Anruf aufzulösen. Beratungsfirmen. z. B. Management oder technische Beratungsunternehmen oder Werbeagenturen, finden ihre Aktivitäten als Projekte anzeigen. Im Marketing stellt eine Kampagne einen Satz Arbeit dar, der geliefert werden muss. In der projektbasierten Fertigung besteht ein Produktionsauftrag aus verschiedene Arbeit zu, die ausgeführt werden muss, um mehrere fertige Artikel zu erzeugen. Welche Bezeichnung auch verwendet wird, die Projekte beinhalten Ressourcen, Zeitpläne und Kosten. Die Projektverwaltungs- und Buchhaltungsfunktionen in Microsoft Dynamics 365 for Operations können bei der Planung, Durchführung und Analyse dieser Projekte helfen.

## <a name="project-phases"></a>Projektphasen
Obwohl das folgenden Ablaufdiagramm für externe Projekte oder Projekte, die für einen oder mehrere Kunden durchgeführt werden gedacht ist, finden die Funktionen auch auf interne kostenbasierte Projekte Anwendung. 

![3 Phasen von einem Projekt](./media/3-stages-of-a-project.png) 

Wie in der vorherigen Abbildung zu sehen, kann die Projektverwaltung und Buchhaltung in drei Phasen unterteilt werden:

1.  Initiierung
2.  Ausführen
3.  Analysieren

## <a name="initiate-the-project"></a>Projekt initiieren
Während des Projektstarts treten mehrere die wichtigsten Prozesse auf. Sie können eines Projektangebots verwenden, um vorkalkulierte die Arbeit, Ausgaben und das Material an den Debitor darüber informiert. Sie können die Rechnungsstellungsbedingungen, -Unterzeichnungslimit und -Vereinbarungen in einem Projektvertrag erfassen. Sie können einen Projektstrukturplan (PSP) verwenden, um die anstehenden Arbeiten zu planen und bewerten. Sie können einrichten, Budgets und Planungen um die Projektausführung verwalten. Die folgende Abbildung zeigt die Struktur eines Projekts an.[![Projektstruktur.](./media/project-structure1.jpg)](./media/project-structure1.jpg)  

### <a name="create-project-quotations"></a>Projektangebote erstellen

In der anfänglichen Vertriebsphase eines Projekts, ermöglicht Ihnen ein Projektangebot einem Kunden ein unverbindliches Angebot zu unterbreiten. Ein Angebot kann verschiedene Elementen umfassen, beispielsweise die angebotenen Artikel und Services, grundlegende Kontaktinformationen, spezielle Handelsvereinbarungen und Rabatte sowie eventuelle Steuern und Zuschläge.

Sie können außerdem einen Garantiebrief für eine Projektangebotsbuchung zwischen Ihrer Organisation und dem Kunden ausstellen. Nach der Erstellung des Projektangebots können Sie die Garantiebriefanforderung für den Debitor erstellen und an die Bank einreichen. Nachdem die Bank die Anforderung genehmigt hat, wird der Garantiebrief für den Debitor ausgestellt. 

Weitere Informationen finden Sie unter [Projektangebote](project-quotations.md).

### <a name="create-project-contracts"></a>Projektverträge erstellen

Wenn Sie einen Vertrag mit einem Debitor oder einer anderen Finanzierungsquelle abschließen, um ein Projekts abzuschließen, müssen Sie zuerst einen Projektvertrag erstellen. Danach müssen Sie bei der Erstellung des Projekts das Projekt dem entsprechenden Projektvertrag zuweisen. Der für einen Projektvertrag erstellte Projekttyp definiert die Methode, nach der das Projekt den Debitoren in Rechnung gestellt wird. Ein Projektvertrag und das zugehörige Projekt können geändert werden, der Projekttyp jedoch nicht. Weitere Informationen zu Projekttypen finden Sie im Abschnitt "Erstellen von Projekten".

Weitere Informationen zu Projektverträgen finden Sie unter [Projektverträge](project-contracts.md).

### <a name="create-work-breakdown-structures"></a>Erstellen von Projektstrukturplänen

Der erforderliche Genauigkeit in einem PSP hängt vom Ebene der Genauigkeit ab, die für die Vorkalkulationen erforderlich ist und von der Nachverfolgung, die für diese Vorkalkulationen erforderlich ist. Projekte, die eine niedrige Toleranz für Planungs- oder Kostenverschiebungen haben, erfordern normalerweise einen ausführlicheren PSP und eine sorgfältigere Nachverfolgung des Arbeitsstatus und der Kosten gegen den PSP. 

Weitere Informationen finden Sie unter [Projektstrukturpläne](work-breakdown-structures.md).

### <a name="create-project-forecasts-and-budgets"></a>Projektplanungen und -budgets erstellen

Sie können die Planung verwenden, wenn die Organisation operativ ausgerichtet ist und der Schwerpunkt auf Umsatzerlösen und Kosten liegt, die aus speziellen Buchungen stammen. Wenn sich die Organisation eher auf Finanzbeträge konzentriert, verwenden Sie die Budgetierung. Jede Methode hat ihre Vorteile. Weitere Informationen finden Sie unter [Projektplanungen und Budgets](project-forecasts-budgets.mdhttps:/ax.help.dynamics.com/en/wiki/project-forecasts-and-budgets/).

### <a name="create-projects"></a>Projekte erstellen

Sie können Projekte in sechs Arten Microsoft Dynamics 365 for Operations erstellen. Jeder Typ wird unterschiedlich für Umsatzerkennung Kosten und eingerichtet. Der gewählte Projekttyp hängt vom Zweck des Projekts ab. Die folgende Tabelle beschreibt die typische Verwendung eines Projekttyps.

| Projekttyp      | Beschreibung 
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nach Aufwand | In Aufwandsprojekten werden dem Debitor alle Kosten berechnet, die für ein Projekt anfallen. Zu den Kosten zählen die Kosten für Stunden, Ausgaben, Artikel und Gebühren.                                                                                                                  |
| Festpreis       | In Festpreisprojekten bestehen Rechnungen aus Akontobuchungen. Ein Festpreisprojekt wird gemäß einem Fakturierungsplan fakturiert, der auf einem Projektvertrag beruht. Der Umsatzerlös für ein Festpreisprojekt kann während des Projekts berechnet und gebucht werden, indem die Methode "Prozentsatz der Fertigstellung" angewendet werden. Alternativ kann der Umsatzerlös berechnet und gebuth werden, wenn das Projekt abgeschlossen ist, indem die Methode "Vollendeter Auftrag" angewendet wird. Bei Unternehmen ist es häufig sinnvoll, den Wert der Ressource in Fertigung (RIF) zu verwenden, um den Grad der Fertigstellung eines Projekts oder einer Gruppe von Projekten zu berechnen.                                                                                                                                     |
| Investition        | Investitionsprojekte sind Projekte, die keine sofortigen Einnahmen erzeugen. Sie werden in der Regel für langfristige interne Projekte verwendet, bei denen die Kosten kapitalisiert werden müssen. Für ein Investitionsprojekt können nur Artikelkosten, Stundenkosten und Ausgaben erfasst werden. Kosten in einem Investitionsprojekt werden durch die Vorkalkulationsfunktion verfolgt und gesteuert. Investitionsprojekte können mit einem optionalen maximalen Kapitalisierungslimit eingerichtet werden. Mit dem Fortschritt des Investitionsprojekts erfassen Sie die Kosten in RIF-Konten, in denen sie bis zum Abschluss des Projekts gehalten werden. Wenn das Projekt gelöscht wird, übertragen Sie den RIF-Wert auf ein Anlagenkonto, ein Sachkonto oder ein neues Projekt.
> [!NOTE] 
> Buchungen für Investitionsprojekte werden nicht auf  **Buchkosten**, **Umsatzerlös antizipieren** oder **Erstellen von Rechnungsvorschlägen** Seite angezeigt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | | Kostenprojekt      | Ebenso wie Investitionsprojekte dienen Kostenprojekte in der Regel dazu, interne Projekte zu verfolgen, und für Kostenprojekte können nur Stunden, Ausgaben und Artikel erfasst werden. Kostenprojekte haben jedoch in der Regel eine kürzere Dauer als Investitionsprojekte. Des Weiteren können Kostenprojekte im Unterschied zu Investitionsprojekten nicht auf Bilanzkonten aktiviert werden. Stattdessen werden ihre Projektbuchungen nur auf Gewinn- und Verlustkonten gebucht. 
[!NOTE] 
> Buchungen für Kostenprojekt werden nicht auf **Buchkosten**, **Umsatzerlös antizipieren** oder **Erstellen von Rechnungsvorschlägen** Seite angezeigt. Da Kostenprojekte in der Regel verwendet werden, um interne Projekte nachzuverfolgen, müssen sie nicht unbedingt einem Debitorenkonto zugeordnet sein. Wenn die Einstellung jedoch erfordert, dass Artikelbedarf für Bestellungen erstellt werden, müssen Sie das Kostenprojekt einem Debitor zuordnen. Diese Zuordnung ist erforderlich, da der Artikelbedarf als Auftragspositionen verwaltet wird, und das System erfordert, dass ein Debitor angegeben ist. Allerdings ergibt diese Einstellung keinen Artikelbedarf, der automatisch aus einer Bestellung erstellt wird. Für Kostenprojekte wird die  **Artikelbedarf erstellen**-Einstellung ignoriert. Wenn Sie einen Artikelbedarf in einem Kostenprojekt benötigen, können Sie einen manuell erstellen, solange ein Debitor dem Projekt zugeordnet ist. | | Intern          | Interne Projekte dienen zur Verfolgung der Kosten eines internen Projekts der Organisation. Dieser Projekttyp kann ein Planungstool zum Verwalten des Ressourcenverbrauchs enthalten. **Hinweis:**Buchungen für interne Projekt werden nicht auf **Umsatzerlös antizipieren** oder **Erstellen von Rechnungsvorschlägen** Seite angezeigt.                                                                                                                                                                                                                                                                       | | Zeit              | Zeitprojekte dienen dazu, die Zeit zu erfassen, die mit nicht fakturierbaren und nicht produktiven Aktivitäten verbunden ist. Beispiel hierfür ist ein Projekt zur Erfassung der Krankheitszeiten von Arbeitskräften. Buchungen in Zeitprojekten werden nicht im Sachkonto gebucht. Sie werden vielmehr in Arbeitskraftauslastungsberichte eingegliedert. In Zeitprojekten können nur Stundenbuchungen erfasst werden. Sie verwenden eine Stundenerfassung oder einen Arbeitszeitnachweis, um diese Stunden im Projekt zu erfassen. Nachdem die Stunden erfasst wurden, werden sie als Projektbuchungen angezeigt, jedoch ohne eine entsprechende Belegbuchung.

> [!NOTE] 
> Buchungen für Zeitprojekt werden nicht auf **Buchkosten**, **Umsatzerlös antizipieren** oder **Erstellen von Rechnungsvorschlägen** Seite angezeigt.                                                                                                                                                                                       |

### <a name="assign-workers-categories-and-resources"></a>Arbeitskräfte, Kategorien und Ressourcen zuweisen

Sie können Sie Arbeitskaftressourcen basierend auf den Anforderungen und dem Zeitplan eines Projekts oder den Qualifikationen und der Verfügbarkeit der Arbeitskräfte planen. Wenn Sie die Ressourcenplanungsfunktionen verwenden, können Sie die Arbeitskraftressourcen der Organisation effizient und effektiv bereitstellen. Sie können die qualifiziertsten Arbeitskräfte für ein Projekt schnell finden. Sie können auch leicht erkennen, wie diese Arbeitskräfte ggf. während des Projekts effektiver verwendet werden können. 

Nachfolgend sind einige der Methoden zur Nutzung der Einsatzplanungsfunktionen beschrieben:

-   Mithilfe der Informationen zu den Attributen einer Arbeitskraft wie Ausbildung, Qualifikationen, Bescheinigungen und Projekterfahrung können Sie die Arbeitskraft mit den Anforderungen eines Projekts abstimmen.
-   Mithilfe der Informationen zu dem Kalender und der Verfügbarkeit einer Arbeitskraft können Sie den Zeitplan der Arbeitskraft mit dem Projektkalender abgleichen.
-   Prüfen Sie die Kapazität der einzelnen Arbeitskräfte, und ermitteln Sie, wie diese Kapazität eingesetzt wird. Beispiel: Ist eine Arbeitskraft nicht vollständig ausgelastet, kann sie einem Projekt zugewiesen werden, das der Verfügbarkeit und den Attributen der Arbeitskraft entspricht.
-   Überprüfen Sie die Verfügbarkeit der Arbeitskräfte, um sicherzustellen, dass keine Kalenderkonflikte mit ihren Zuweisungen auftreten.
-   Prüfen Sie die Informationen zur Arbeitskraftauslastung in einer Übersicht, z. B. nach Abteilung oder Arbeitskraft, oder in einer detaillierten Ansicht, z. B. nach Arbeitskräften in einer Abteilung oder wöchentlich pro Arbeitskraft.
-   Ändern Sie die Ressourcenzuweisungen für unterschiedliche Zeiteinheiten, z. B. Tag, Woche oder Monat, um die Arbeitskraftauslastung zu optimieren.

## <a name="execute-the-project"></a>Projekte ausführen
Während der Projektausführung zeichnen Teammitglieder oder Manager die Arbeit und Aufwendungen, die verursacht werden über Arbeitszeitnachweise, Spesenabrechnungen und andere Dokumente auf. Projektmanager haben Tools, mit denen sie den Verbrauch von budgetierten Beträgen für das Projekt überwachen können. Projektmanager können Material für Projekte bestellen, entnehmen oder beschaffen, indem sie Bestellungen und andere Dokumente verwenden. Rechnungen werden vorbereitet und genehmigt, damit die laufende Arbeit den Kunden berechnet werden kann. Schließlich wird der Umsatzerlös während dieses Vorgangs realisiert, um die Finanzdaten der Organisation zu aktualisieren.

### <a name="manage-work-breakdown-structures"></a>Verwalten von Projektstrukturplänen

Ein PSP ist eine Beschreibung der Arbeit, die für ein Projekt durchgeführt wird. Ein PSP ist eine Hierarchie von Aufgaben. Er stellt nicht nur die Arbeit für jede Aufgabe dar, sondern auch die Größe, die Kosten und die Dauer der Aufgabe. 

Weitere Informationen finden Sie unter [Projektstrukturpläne](work-breakdown-structures.md).

### <a name="manage-project-forecasts-and-budgets"></a>Verwalten von Projektbudgets und Planungen

Es gib zwei Möglichkeiten, zum Verwalten und Steuern Ihrer Projekte: Projektplanungen und Projektbudgets. Sie können die Planung verwenden, wenn die Organisation operativ ausgerichtet ist und der Schwerpunkt auf Umsatzerlösen und Kosten liegt, die aus speziellen Buchungen stammen. Wenn sich die Organisation eher auf Finanzbeträge konzentriert, verwenden Sie die Budgetierung.

Weitere Informationen finden Sie unter [Projektplanungen und Budgets](project-forecasts-budgets.mdhttps:/ax.help.dynamics.com/en/wiki/project-forecasts-and-budgets/).

### <a name="create-production-orders"></a>Produktionsauftrag erstellen

Ein projektbezogener Produktionsauftrag kann mit einem Auftrag oder einem Artikelbedarf verknüpft werden, indem entweder die Methode für Fertigartikel oder verbrauchte Artikel verwendet wird. Wenn der Produktionsauftrag manuell erstellt wird, besteht keine Verknüpfung zwischen dem Produktionsauftrag und dem Auftrag bzw. dem Artikelbedarf (keine Verknüpfung mit Auftrag). Falls der Produktionsauftrag automatisch erstellt wurde, um einen Auftrag oder einen Artikelbedarf zu erfüllen, besteht eine Verknüpfung zwischen dem Produktionsauftrag und dem Auftrag oder dem Artikelbedarf (Verknüpfung mit Auftrag). 

Verwenden Sie ausgehend von den Kombinationen dieser Faktoren die folgenden Methoden:

-   **Fertigartikel/Verknüpfung mit Auftrag** – Ermöglicht die Verknüpfung des Projekts mit einem Auftrag oder einem Artikelbedarf. Mit dieser Methode werden die tatsächlichen Projektkosten gebucht, sobald der Auftrag fakturiert oder der Lieferschein für den Artikelbedarf aktualisiert wird. Die Kosten werden als Fertigartikel gebucht.
-   **Fertigartikel/Keine Verknüpfung mit Auftrag** – Istkosten können erst gebucht werden, wenn der Produktionszyklus für einen Artikel den Status **Abgeschlossen** besitzt. Die Kosten für den Fertigartikel werden als einzelner Posten gebucht.
-   **Verbrauchter Artikel/Verknüpfung mit Auftrag** – Ermöglicht die Verknüpfung des Projekts mit einem Artikelbedarf. Mithilfe dieser Methode lassen sich tatsächliche Projektkosten anzeigen, wenn die Produktion den Status **Gestartet** besitzt oder als fertig gemeldet wird. Die Kosten werden in Form von mehreren Projektartikelbuchungen für Rohmaterialen und Stunden gebucht, die für die Produktion verbraucht wurden. Bei der Aktualisierung des Lieferscheins für den Artikelbedarf werden keine Projektkosten gebucht. Sie können auch die Ebene der Stücklistenhierarchie definieren, auf der die Projekte in der Produktion nachverfolgt werden.
-   ****Verbrauchter Artikel/keine Verknüpfung mit Auftrag**** – Ermöglicht die Verknüpfung des Projekts mit einem Artikelbedarf. Mithilfe dieser Methode lassen sich tatsächliche Projektkosten anzeigen, wenn die Produktion den Status **Gestartet** besitzt oder als fertig gemeldet wird. Die Kosten werden in Form von mehreren Projektartikelbuchungen für Rohmaterialen und Stunden gebucht, die für die Produktion verbraucht wurden. Sie können auch die Ebene der Stücklistenhierarchie definieren, auf der die Projekte in der Produktion nachverfolgt werden.

### <a name="procure-products-and-services"></a>Produkte und Dienstleistungen bereitstellen

Der Kauf und Verkauf von Artikeln sind vorherrschende Aktivitäten vieler projektorientierter Geschäfte.

#### <a name="purchase-orders-for-projects"></a>Bestellungen für Projekte

Der Zweck der Bestellung bestimmt, wann eine Bestellung verbraucht wird, und damit, wann ein Projekt mit Artikeln belastet wird.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Methode</th>
<th>Verwendungszweck</th>
<th>Verbrauch von Artikeln</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Direktes Erstellen einer Bestellung</td>
<td>Ein Einkauf bei einem externem Kreditor für den Verbrauch in einem Projekt. Sie können die Bestellung wie folgt erstellen:
<ul>
<li>Aus dem Projekt selbst: In diesem Fall wurde das Projekt für die Bestellung bereits definiert.</li>
<li>Per Navigation zur Projektbestellung Hierbei müssen Sie sowohl den Kreditor als auch das Projekt auswählen, für den bzw. das die Bestellung erstellt werden soll.</li>
</ul></td>
<td>Artikel werden verbraucht, wenn die Kreditorenrechnung aktualisiert wird.</td>
</tr>
<tr class="even">
<td>Bestellung aus einem Auftrag erstellen  </td>
<td>Bestellen Sie Artikel, wenn Sie einen Auftrag über ein Projekt erstellen.</td>
<td>Artikel werden verbraucht, wenn die Rechnung für den Auftrag an den Debitor gestellt wird.</td>
</tr>
<tr class="odd">
<td>Bestellung aus einem Artikelbedarf erstellen  </td>
<td>Bestellen Sie Artikel, wenn Sie einen Artikelbedarf über ein Projekt erstellen.</td>
<td>Artikel werden verbraucht, wenn der Lieferschein des Artikelbedarfs aktualisiert wird.</td>
</tr>
</tbody>
</table>

#### <a name="sales-orders-for-projects"></a>Aufträge für Projekte

Im Projektverwaltungs- und Buchhaltungsmodul können Sie den Verbrauch von Artikeln auf verschiedene Arten erfassen. Sie können Artikel aus einem Projekt verkaufen bzw. kaufen oder Artikel für ein Projekt reservieren. 

Sie können Artikeln aus dem Lagerbestand des Unternehmens für den Verbrauch in einem Projekt bestellen. Alternativ können Sie Artikel von einem externen Kreditor einkaufen. Artikel können in allen Typen von Projekten außer Zeitprojekten verbraucht werden. 

Die Art und Weise, wie Sie Artikel bestellen, hängt davon ab, wo Sie die Artikel bestellen:

-   Zum Bestellen von Artikeln aus dem Lagerbestand des Unternehmens muss die Bestellung als Artikelbedarf eingegeben werden. Bei Verwendung des Formulars **Artikelanforderungen** kann dieses so eingerichtet werden, dass Artikel als Teillieferungen eingehen. Dies bedeutet, dass Sie den Verbrauch einer Menge der Artikel verschieben können, bis die Artikel benötigt werden.
-   Zum Bestellen von Artikeln von einem externen Kreditor muss der Auftrag als Bestellung auf der Seite **Bestellung** erstellt werden.

> [!NOTE] 
> Der Lieferschein für einen projektbezogenen Auftrag kann nicht storniert werden, wenn die Artikel bereits für das Verpacken markiert wurden. 

In der folgenden Tabelle sind die Methoden zum Bestellen von Artikeln aufgeführt, und es wird beschrieben, wie die Artikel verbraucht werden.

| Methode            | Verwendungszweck                                                                                                                                                        | Verbrauch von Artikelbuchungen                                                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| Auftrag       | Geben Sie eine Verkaufsbuchung direkt in einem Aufwandsprojekt ein.                                                                                                   | Artikelbuchungen werden verbraucht, wenn die Debitorenrechnung gebucht wird.                                                                               |
| Lagererfassung | Schnelle Eingabe und Verwaltung von Artikeldatensätzen Wenn z. B. ein Artikelbedarf basierend auf einer gedruckten Liste eingegeben werden soll, kann die Lagererfassung angewendet werden. | Artikelbuchungen werden verbraucht, wenn die Erfassung gebucht wird.                                                                                        |
| Artikelbedarf  | Geben Sie Artikel ein, die nicht sofort verbraucht werden. Bei dieser Methode können Benutzer nachverfolgen, welche Anzahl an Artikeln innerhalb eines einzelnen Artikelbedarfsdatensatzes verbraucht wurde.    | Artikelbuchungen werden verbraucht, wenn der Lieferschein aktualisiert wird. Das heißt, dass der Artikelbedarf erstellt wird, wenn der Lieferschein gebucht wird. |
| Bestellungen   | Geben Sie Buchungen je nach Bestellmethode an drei verschiedenen Orten ein.                                                                              | Artikelbuchungen werden verbraucht, wenn der Lieferschein aktualisiert wird oder wenn der Debitor bzw. der Kreditor fakturiert wird.                                      |

### <a name="process-project-invoices"></a>Projektrechnungen verarbeiten

Das zu verwendende Fakturierungsverfahren wird durch den Projekttyp bestimmt. Eine Fakturierung kann ausschließlich für die beiden externen Projekttypen Aufwand und Festpreis erfolgen. Aufwands- und Festpreisprojekte sind immer einem Projektvertrag zugeordnet. 

Bevor Sie eine Debitorenrechnung für ein Projekt erstellen, können Sie eine vorläufige Rechnung oder einen Rechnungsvorschlag erstellen. In einem Rechnungsvorschlag können Sie Projektbuchungen auswählen, die in eine Projektrechnung einbezogen werden soll. Sie können dann die Rechnungsdetails prüfen, bevor Sie die Projektrechnung buchen und diese an den Debitor oder an eine andere Finanzierungsquelle senden. 

Informationen zum Verarbeiten von Projektrechnungen finden Sie unter [Projektrechnung](/accounts-payable/project-invoicing.md).

### <a name="calculate-the-cost-to-complete-a-project"></a>Berechnen der Fertigstellungskosten

Beim Erstellen einer Vorkalkulation können Sie festlegen, wie die Fertigstellungskosten des Projekts berechnet werden sollen. Wählen Sie eine Methode im Feld **Fertigstellungskosten-Methode ** auf der Seite **Vorkalkulation erstellen** aus. Die Methode, die Sie auswählen, wird einzeln auf jeder Kostenposition in der Vorkalkulation angewendet. Während eine Position den **Erstellt**-Status hat, können Sie die Methode ändern, die auf der Seite **Vorkalkulation** angewendet wird. 

In der folgenden Tabelle werden die Methoden zum Berechnen der Kosten für den Abschluss eines Projektes beschrieben.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Methode</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Gesamtkosten - tatsächliche Kosten</td>
<td>Vorkalkulierte Kosten müssen manuell eingegeben werden. Nachdem die Spalte <strong>Gesamtkosten</strong> oder <strong>Gesamtmenge</strong> auf der <strong>Vorkalkulation</strong>-Seite ausgefüllt wurde, werden die tatsächlichen Kosten von den vom Benutzer eingegebenen Summen subtrahiert. Das Ergebnis sind die Kosten für den Abschluss des Projekts. Normalerweise wird der Status der Kosten nicht auf Grundlage von Werten wie beispielsweise der Anzahl der Hotelaufenthalte und der Mahlzeiten im jeweiligen Zeitraum erfasst. Stattdessen basiert es normalerweise auf einem Vergleich mit den Gesamtbetrag der vorkalkulierten Stunden. Dieser Ansatz erfordert kein Planzahlenmodell, und die Gesamtkosten oder die Gesamtmenge können manuell bearbeitet werden. Wenn ein Wert in der Spalte <strong>Gesamtkosten</strong> oder <strong>Gesamtmenge</strong> eingegeben wird, vergleicht Microsoft Dynamics 365 for Operations diesen Wert mit den tatsächlichen Buchungen, die in der Periode gebucht werden, und verringert dann den Wert in der Spalte <strong>Abzuschließende Menge</strong> oder <strong>Fertigstellungskosten</strong>.</td>
</tr>
<tr class="even">
<td>Gesamtbudget - tatsächliches Budget</td>
<td>Die Istkosten werden mit dem Planzahlenmodell verglichen, das Sie auswählen, um die Kosten zu bestimmen. Bei dieser Methode wird ein Budgetmodell verwendet, dass Planungsbuchungen umfasst. Für eine exaktere Darstellung des Projektes können Sie das Budgetmodell anpassen, wenn sich das Projekt in Bearbeitung befindet. Wenn Sie die Planung anpassen müssen, folgen Sie diesem allgemeinen Prozess:
<ol>
<li>Kopieren Sie Planungsbuchungen in ein anderes Planzahlenmodell.</li>
<li>Vergleichen von Planungsbuchungen mit tatsächlichen Buchungen.</li>
<li>Behalten, verringern oder erhöhen Sie die Vorkalkulationen für die nächste Periode.</li>
</ol>
Microsoft Dynamics 365 for Operations verringert nicht automatisch die geplanten Vorkalkulationen. Daher wird empfohlen, dass Sie ein ursprüngliches Planzahlenmodell im Festpreisprojekt aufbewahren, um eine Basislinie einzurichten, mit der das Projekt verglichen wird, wenn es abgeschlossen ist. 
> [!NOTE] Verwenden Sie mindestens zwei Planzahlenmodelle, wenn Sie diesen Ansatz anwenden. Ein Modell sollte die ursprüngliche Planung enthalten. Für das andere Modell sollten Sie Planungsbuchungen eines anderen Modells kopieren. Diese Methode prüft nur Festpreis- und Investitionsprojekte.</td>
> </tr>
<tr class="odd">
<td>Restbudget</td>
<td>Die Methode verwendet ein Restbudgetmodell, um zu den Kosten für den Abschluss des Projekts zu berechnen. Wenn Sie diese Methode verwenden, werden die tatsächlichen Kosten und die geplanten Beträge im Restbudgetmodell zusammen hinzugefügt. Dies ergibt die Gesamtkosten. Bevor Sie diese Methode verwenden, muss ein Restbudgetmodell eingerichtet werden, um Buchungen auf der Grundlage der tatsächlichen Buchungen abzuziehen, die im System erfasst sind. Prüfen Sie auf der <strong>Planzahlenmodelle</strong>-Seite, ob die Felder in der Gruppe <strong>Automatische Planungsverringerung</strong> markiert sind. Normalerweise wird ein Restbudget aus einem ursprünglichen Budget kopiert. Während Buchungen eingegeben werden, werden die Buchungen für das Restbudget verringert. Wenn Sie beim Fortschritt des Projekts feststellen, dass das Restbudget angepasst werden muss, können Sie das Restbudget mit Planungsbuchungen belasten. <strong>Hinweis:</strong> Die Methode kann nur angewendet werden, wenn der Vorkalkulation ein Planzahlenmodell zugeordnet ist.</td>
</tr>
<tr class="even">
<td>Wie vorhergehende Vorkalkulation</td>
<td>Die gleiche Vorkalkulationsmethode, die in der vorherigen Periode verwendet wurde, wird angewendet. Diese Methode erfordert ein Planzahlenmodell, wenn die vorherige Periode ein Planzahlenmodell erforderte.</td>
</tr>
<tr class="odd">
<td>Fertigstellungskosten auf Null festlegen</td>
<td>Diese Methode wird in der Regel verwendet, bevor das Vorkalkulationsprojekt gelöscht wird. Diese Methode entspricht der gesamten Vorkalkulationen mit den tatsächlichen Buchungen, die gebucht wurden, und löscht die Spalte <strong>Fertigstellungskosten</strong>. Der sich ergebende Prozentsatz des Abschlusses ist immer 100 Prozent. Das Feld <strong>Planung</strong> ist bei jeder erstellten Kostenposition nicht ausgewählt, und die Gesamt-Vorkalkulation wird aus der vorherigen Vorkalkulation kopiert. Der tatsächliche Verbrauch für die Vorkalkulationsperiode wird von den Fertigstellungskosten des Projekts abgezogen. Für diese Methode ist kein Planzahlenmodell erforderlich.</td>
</tr>
<tr class="even">
<td>Von Kostenvorlage</td>
<td>Die Methode verwendet die Fertigstellungskosten-Methode, die in der Kostenvorlage eingerichtet ist, die dem ausgewählten Vorkalkulationsprojekt zugeordnet ist.</td>
</tr>
</tbody>
</table>

## <a name="analyze-the-project"></a>Projekt analysieren
Auf der grundlegendsten Ebene wird ein Projekt zur Gruppierung von Buchungen zur Kostenspeicherung und dann zur Buchung dieser Kosten im Hauptbuch verwendet. 

Im Allgemeinen sind diese Buchungen das Ergebnis der Geschäftsdokumente, wie z. B. Arbeitszeitnachweise, Spesenabrechnungen, Kreditorenrechnungen und Lagerbuchungen. Der Lebenszyklus eines Projekts beginnt normalerweise mit den Vorkalkulationen, Planungen und Budgets zur Planung der Arbeit und der Finanzauswirkungen des Projekts. Wenn Sie ein Projekt analysieren, können Sie nicht nur die Buchungen, die während des Projekts ausgeblendet werden, sondern auch die Genauigkeit der Vorkalkulationen und Planungen, die Auslastungsrate der Projektteammitglieder und den gesamten Erfolg des Projekts überprüfen.

### <a name="analyze-cash-flow"></a>Cashflow analysieren

Verwenden Sie die Cashflowüberwachung, um sowohl den geplanten als auch den tatsächlichen Cashflow eines Projekts zu überwachen. Sie können Cashflows prüfen, während ein Projekt in Bearbeitung ist, oder Sie können die Cashflows eines abgeschlossenen Projekts anzeigen. 

Wenn Sie Cashflows überwachen, können Sie ein einzelnes Projekt bewerten, die Berichte verwenden, um mehrere Projekte anzuzeigen, und Projekt-Cashflows in die Cashflowplanungen im Hauptbuch zu übertragen.

#### <a name="cash-inflow-forecasting"></a>Planen des Zuflusses flüssiger Mittel

Auf Grundlage der Einstellungen können Sie den Zufluss flüssiger Mittel für ein ausgewähltes Projekt planen. Wenn das Projektdatum z. B. der 5. März 2012 ist und Sie am 31. März 2012 fakturieren, können Sie das Fälligkeitsdatum und das erwartete Verkaufszahlungsdatum planen.

-   **Projektdatum:** 5. März 2012.
-   **Rechnungsdatum:** 31. März 2012. Dieses Datum wird basierend auf der Rechnungshäufigkeit bestimmt. In diesem Beispiel legen die Rechnungshäufigkeit auf den aktuellen Monat fest. Dies bedeutet, dass alle Buchungen, die im März gebucht werden, am letzten Tag des Monats fakturiert werden.
-   **Fälligkeitsdatum**: Am 14. April 2012. Dieses Datum wird durch die Zahlungsbedingungen bestimmt die Sie für dieses Projekt ausgewählt haben. Sie haben z. B. eine Zahlungsfrist von 14 Tagen ausgewählt. Daher werden 14 Tage zum Rechnungsdatum hinzugefügt, um zu einem Fälligkeitsdatum vom 14. April 2012 zu kommen.
-   **Erwartetes Datum für Verkaufszahlung:**Am 27. April 2012. Dieses Datum wird berechnet, indem die Anzahl der Tage im Feld **Allgemeine Puffertage** auf der Seite **Projektverwaltungs- und Buchhaltungsparameter** zur Anzahl der Tage im **Individuelle Karenztage**-Feld auf der Seite **Projektverträge** und dann die Summe der Anzahl von Tagen im **Fälligkeitsdatum** Feld hinzufügt wird. In vorliegenden Beispiel haben Sie **3** im Feld **Allgemeine Puffertage** und **10** im Feld **Individuelle Karenztage** eingegeben. Daher werden 13 Tage zum Fälligkeitsdatum hinzugefügt, um zu einem erwarteten Datum für die Verkaufszahlung am 27. April 2012 zu kommen.

Die allgemeinen Puffertage können entweder die einzelnen Puffertage ersetzen oder zu den einzelnen Puffertagen addiert werden:

-   Wenn Sie die allgemeinen Puffertage als Ersatz für die individuellen Puffertage verwenden, geben Sie die durchschnittliche Anzahl von Tagen zwischen dem Fälligkeitsdatum und dem tatsächlichen Zahlungsdatum für Debitoren ein.
-   Wenn Sie die allgemeinen Puffertage im Feld **Allgemeine Puffertage** zu den einzelnen Puffertage hinzufügen möchten, geben Sie die geschätzte Anzahl der Tage zwischen dem Übermitteln der Zahlung durch den Debitor und dem Eingang der Zahlung bei Ihrer Organisation ein.

Richten Sie einzelne Puffertage im Vertrag des Projekts ein. Die Berechnung der Tage erfolgt auf Basis des Fälligkeitsdatums der Rechnung sowie der Erfahrung Ihrer Organisation mit dem Zahlungsrhythmus eines Debitors.

#### <a name="actual-cash-inflow"></a>Tatsächlicher Zufluss flüssiger Mittel

Der tatsächliche Zufluss flüssiger Mittel gleicht der Cashflowplanung mit dem Unterschied, dass die Berechnung ab dem ersten Rechnungsdatum beginnen kann. Hier ist ein Beispiel:

-   **Rechnungsdatum:** 2. März 2012.
-   **Fälligkeitsdatum:** Am 16. März 2012. Die Zahlungsbedingungen sind auf 14 Tage festgelegt.
-   **Erwartetes Datum für Verkaufszahlung:**Am 29. März 2012. Dies umfasst drei allgemeine Puffertage und 10 einzelne Puffertage.

#### <a name="cost-forecasting"></a>Kostenplanung

Auf der Grundlage der Tage, die Sie definieren, kann sich das Kostenzahlungsdatum vom Projektdatum unterscheiden. In diesem Fall wird das Daten für die Kostenzahlung berechnet, indem die Anzahl der Tage ab dem Projektdatum zur Anzahl der Tagen in den Zahlungsbedingungen hinzugefügt wird. 

Das Projektdatum der Buchung ist z. B. der 5. März 2012, und Sie legen die folgenden Zahlungsbedingungen fest:

-   **Stunden:** Aktueller Monat (**M**)
-   **Ausgaben:**14 Tage (**D14**)
-   **Artikel** 30 Tage (**D30**)

Auf Basis dieser Einstellungen ergibt sich für jede Buchungsart folgendes Kostenzahlungsdatum:

-   **Stunden:** 31. März 2012, der letzte Tag des ausgewählten Monats.
-   **Ausgaben:** 19. März 2012, 14 Tage nach dem Datum der Buchung.
-   **Artikel:** 4. April 2012, 30 Tage nach dem Datum der Buchung.

> [!NOTE] 
> Das Fälligkeitsdatum für die Bestellung basiert auf der Kreditorenbuchung beim Erstellen der Projektbestellung. Das Fälligkeitsdatum wird von keinen Standardeinstellungen bestimmt. 

Das Kostenzahlungsdatum wird nicht auf Basis von Puffertagen berechnet. Nachdem ein Projekt abgeschlossen wurde und die gesamte Nachkalkulation und Fakturierung abgeschlossen ist, werden sowohl die Kosten als auch die Verkäufe auf den Gewinn- und Verlustkonten gebucht. 

Nach der Erstellung aller Verkaufs- und Kreditorenrechnungen, können Sie die Beziehung zwischen Feldern auf der Seite **Cashflow ** und in den Feldern auf der Seite **Projektaufstellungen** anzeigen.

| Seite "Cashflow" | Seite "Projektaufstellungen" |
|----------------|-------------------------|
| Zufluss flüssiger Mittel   | Umsatzerlös                 |
| Abfluss flüssiger Mittel  | Gesamtkosten              |
| Cashflows (netto) | Bruttogewinn            |

### <a name="review-costs"></a>Kosten prüfen

Sie können das Formular **Kostensteuerung** verwenden, um die Kosten zu überwachen, die Ihre Organisation im Verlauf eines Projekts entstehen. Wenn Sie die ursprünglich budgetierten Kosten für das Projekt mit den aktuellen Istkosten und zugesagten Kosten vergleichen, können Sie bestimmen, ob das Projekt sich im Rahmen des geplanten Budgets hält, dieses überschreitet oder unterschreitet. 

> [!NOTE] 
> Wenn Sie die Seite **Kostensteuerung** verwenden, um den aktuellen Status von Projektkosten anzuzeigen, verwenden Sie die Planzahlenmodelle, die für ursprüngliche und verbleibende Budgets ausgewählt wurden. Wenn Sie bei der Berechnung der Kosten andere Planzahlenmodelle auswählen, sind die Berechnungsergebnisse ungenau.

#### <a name="viewing-the-remaining-budgeted-amounts"></a>Anzeigen der verbleibenden budgetierten Beträge

Wenn **Restbudget ** als die Kostenkontrollmethode auf der Seite **Projektverwaltungs- und -verrechnungsparameter** aktiviert ist, berechnet die Seite **Kostensteuerung** die Kosten, die nicht als Istkosten gebucht oder als festgelegt markiert wurden. Die Beträge in den Spalten auf der Registerkarte **Allgemeines** im unteren Bereich des Formulars **Kostensteuerung** werden folgendermaßen berechnet:

-   **Istkostenbetrag** – Der Gesamtbetrag, der im Projekt für die ausgewählte Kostenposition aufgewendet wurde. Der Istkostenbetrag wird auf der Seite **Sachkontoaktualisierungen** berechnet.
-   **Zugesagte Kosten** – Der zusätzliche Ausgabenbetrag, dessen Zahlung die juristische Person zugesagt hat. Die entsprechenden Beträge der zugesagten Kosten werden auf der Seite **Zugesagte Kosten** berechnet.
-   **Restbudget** – Der Betrag des ursprünglich budgetierten Betrags, der für die ausgewählte Kostenposition weiterhin verfügbar ist. Der verbleibende Budgetbetrag ist auf der Seite **Hauptbuch - Vorschau** berechnet.
-   **Gesamtkosten** – Die Summe der Istkosten, zugesagten Kosten und des verbleibenden Budgets.

Auf der Seite **Kostensteuerung** der Registerkarte **Abweichung** kann der Vergleich der gesamten voraussichtlichen Kosten mit dem ursprünglichen Budget angezeigt werden. Dieser Vergleich zeigt sämtliche Unterschiede zwischen diesen Beträgen an. Daher können Sie ermitteln, wo die Daten nicht übereinstimmen. Die abweichenden Beträge werden folgendermaßen berechnet:

-   **Ursprüngliches Budget** – Der Betrag, der ursprünglich für die ausgewählte Kostenposition budgetiert wurde. Das ursprüngliche Budget ist auf der Seite **Hauptbuch - Vorschau** berechnet.
-   **Gesamtkosten** – Die Summe aus Istkosten, zugesagten Kosten und dem verbleibenden Budget, wie auf der Registerkarte **Allgemein** angegeben.
-   **Abweichung** – Hier wird die Abweichung zwischen den Gesamtkosten und dem ursprünglichen Budget angezeigt.
-   **Abweichung basierend auf der Menge** – Die gesamte Betragsdifferenz zwischen der ursprünglichen Planung und der Gesamtplanung. Diese Differenz kann mathematisch wie folgt ausgedrückt werden: [(Geplante Gesamtmenge) × (Ursprünglicher durchschnittlicher Preis – Durchschnittlicher Gesamtpreis)]. Die Berechnung gilt nur für Projektstunden.
-   **Abweichung basierend auf dem Preis** – Die gesamte Betragsdifferenz zwischen der ursprünglichen Planung und der Gesamtplanung. Diese Differenz kann mathematisch wie folgt ausgedrückt werden: (Ursprünglicher geplanter Preis) × (Ursprüngliche geplante Menge – Geplante Gesamtmenge). Die Berechnung gilt nur für Projektstunden.

#### <a name="viewing-the-total-budgeted-amounts"></a>Anzeigen der gesamten budgetierten Beträge

Wenn **Gesamtbudget** als die Kostenkontrollmethode auf der Seite **Projektverwaltungs- und -verrechnungsparameter** aktiviert ist, berechnet die Seite **Kostensteuerung** die tatsächlichen Kosten und die Gesamtkosten des Projekts. Auf der Seite **Kostensteuerung** werden die Beträge in den Spalten im unteren Bereich der Registerkarte **Allgemeines** folgendermaßen berechnet:

-   **Budgetierte Gesamtkosten** – Der Gesamtbudgetbetrag für die ausgewählte Kostenposition.
-   **Istkosten** – Der Gesamtbetrag der Kosten, die für das Projekt bisher für die ausgewählten Kostenpositionen angefallen sind.
-   **Zugesagte Kosten** – Der Gesamtbetrag, der für die ausgewählte Kostenposition festgelegt wurde.
-   **Abweichung** – Die Differenz zwischen der Summe der Istkosten und den zugesagten Kosten und den Gesamtkosten. Die Abweichung zeigt, ob zusätzliche Kosten für das Gesamtbudget angegeben werden müssen.

Auf der Registerkarte **Abweichung** auf der Seite **Kostensteuerung ** können Sie die Differenz zwischen dem Budget und dem ursprünglichen Budget anzeigen, indem Sie die folgenden Felder berücksichtigen:

-   **Ursprüngliches Budget** – Der Betrag, der ursprünglich für die ausgewählte Kostenposition budgetiert wurde. Das ursprüngliche Budget ist auf der Seite **Hauptbuch - Vorschau** berechnet.
-   **Budgetierte Gesamtkosten** – Die Gesamtkosten, die ursprünglich für die Kostenposition budgetiert wurden. Das gesamte Budget ist auf der Seite **Hauptbuch - Vorschau** berechnet.
-   **Abweichung** - Die Abweichung für die Kostenposition. Die Abweichung wird durch Subtrahieren der Gesamtkosten vom ursprünglichen Budget berechnet.
-   **Abweichung basierend auf der Menge** – Die gesamte Betragsdifferenz zwischen dem ursprünglichen Budget und dem Gesamtbudget. Die Berechnung dieser Menge erfolgt durch Subtrahieren der gesamten Stunden gemäß Budget von den ursprünglich im Budget kalkulierten Stunden und durch anschließendes Multiplizieren der Differenz mit dem ursprünglichen budgetierten Einstandspreis. Diese Differenz kann mathematisch als (Ursprünglich geplanter Einstandspreis) × (ursprünglich im Budget kalkulierte Stunden - gesamte Anzahl der benötigten Stunden) ausgedrückt werden. Die Berechnung gilt nur für Projektstunden.
-   **Abweichung basierend auf dem Preis** – Die Berechnung dieses Betrags erfolgt durch Subtrahieren der gesamten Stunden gemäß Budget von den ursprünglich im Budget kalkulierten Stunden und durch anschließendes Multiplizieren der Differenz mit der gesamten Anzahl der benötigten Stunden. Diese Differenz kann mathematisch als (Anzahl der verbrauchten Stunden) × (ursprünglich im Budget kalkulierte Stunden - gesamte Anzahl der benötigten Stunden) ausgedrückt werden. Die Berechnung gilt nur für Projektstunden.

### <a name="analyze-utilization"></a>Auslastung analysieren

Die Nutzungsrate ist Prozentsatz der Zeit, den eine Arbeitskraft für berechenbare Arbeit oder für produktive Arbeit in einer bestimmten Periode aufwendet. Berechenbare Stunden sind die Stunden der Arbeitskraft, die einem Kunden berechnet werden können. 

Um den Nutzungssatz einer Arbeitskraft zu berechnen, dividiert das System die Anzahl der berechenbaren Stunden durch die Anzahl der Arbeitsstunden in einem bestimmten Zeitraum. Wenn die Arbeitskraft beispielsweise 30 berechenbare Stunden in einem Zeitraum hat und die Anzahl der im gleichen Zeitraum 40 ist, ist die Nutzungsrate der Arbeitskraft 75 %. 

Wenn Sie den Nutzungssatz für eine Arbeitskraft berechnen, können Sie entweder den berechenbaren Satz oder den Effizienzgrad berechnen:

-   **Berechenbarer Satz** - Der berechenbare Satz ist die Differenz zwischen berechenbaren Stunden und nicht-berechenbaren Stunden oder Normstunden.
-   **Effizienzrate** - Die Differenz zwischen produktiven Stunden und nicht produktiven Stunden oder Normstunden. Produktive Stunden sind die Stunden, die die Arbeitskraft mit der Arbeit an einem bestimmten Projekt verbracht hat. Produktive Stunden werden in der Regel an Kunden berechnet, außer bei internen Projekten. Unproduktive Stunden werden nie einem Kunden berechnet.

Die Auslastungsrate berechnen Sie auf der Seite **Auslastung/Stunde**. Die Berechnungen basieren auf den standardmäßigen Einstellungen. Diese Einstellungen geben zudem an, wie Stunden berechnet werden, indem eine **Auslastung** oder **Belastung** zu jedem Projekttyp zugewiesen wird. Dies gilt für Berechnungen berechenbaren Sätze und für Effizienzgradberechnungen.

-   **Auslastung** – Stunden, die für den ausgewählten Projekttyp gemeldet werden, werden immer als nicht berechenbar oder als Nicht-Effizienzauslastung eingestuft.
-   **Belastung** – Stunden, die für den ausgewählten Projekttyp gemeldet werden, werden immer als nicht berechenbar oder als Nicht-Effizienzauslastung eingestuft.
-   **Gemäß Positionseigenschaft** – Durch die Abrechnungscodes einer bestimmten Stundenbuchung wird bestimmt, ob die Stunden als berechenbar oder für Effizienzauslastung berücksichtigt werden.
-   **Nicht enthalten** – Stunden werden nicht in die Berechnung der berechenbaren Stunden oder der Effizienzauslastung einbezogen.

Auf der Seite **Auslastung/Stunde** können Sie zusammen mit dem allgemeinen Nutzungssatzprozentsatz für eine Arbeitskraft oder ein Projekt die Anzahl von Stunden sehen, die in die Nutzungssatzberechnung für jeden der folgenden Stundentypen eingegangen sind:

-   **Nicht einbezogene Stunden** - Nicht enthaltene Stunden werden nicht in die Stundenauslastungsrate einbezogen.
-   **Einbezogene Stunden** – Einbezogene Stunden werden durch Addieren der Auslastungs- und Belastungsstunden berechnet. Diese Stunden sind in den Nutzungssatz einbezogen.
-   **Nicht berechenbare Stunden** - Wenn Sie einen berechenbaren Satz berechnen, sind diese Stunden nicht mit fakturierbaren Stunden identisch. Wenn Sie einen Effizienzrate berechnen, sind diese Stunden nicht mit produktiven Stunden identisch.
-   **Berechenbare Stunden** - Wenn Sie einen berechenbaren Satz berechnen, sind diese Stunden mit fakturierbaren Stunden identisch. Wenn Sie einen Effizienzrate berechnen, sind diese Stunden mit produktiven Stunden identisch.

Wenn Sie den Nutzungssatz für eine Arbeitskraft berechnen, können Sie Normstunden oder einbezogene Stunden verwenden. Wenn Sie einbezogene Stunden verwenden, müssen Sie sicherstellen, dass Arbeitskräfte die gesamte Arbeitszeit für die Arbeitszeitnachweisperioden erfassen, da die Berechnung als Prozentsatz der Stunden angegeben wird, die erfasst wurden. Wenn Sie die Stundenauslastungsrate für ein Projekt, einen Projektvertrag, einen Debitorendatensatz oder eine Kategorie berechnen, müssen Sie einbezogene Stunden für die Berechnung verwenden.

### <a name="review-project-statements"></a>Anzeigen von Projektaufstellungen

Sie können eine Projektaufstellung erstellen, um eine schnelle Momentaufnahme des Status eines Projekts anzuzeigen. Wenn Sie Projektaufstellungen ausführen, können Sie die Kriterien bestimmen, die verwendet werden, um die Projektaufstellung zu berechnen, indem Sie Auswahlen auf der Registerkarte **Allgemein** auf der Seite **Projektaufstellungen** vornehmen. Sie können die folgenden Informationen einbeziehen oder ausschließen:

-   Projekttypen
-   Transaktionstypen
-   Projektdatum/Sachkontodatum
-   Daten

Nachdem der Auszug berechnet ist, können folgende Informationen auf den verschiedenen Registerkarten auf der Seite **Projektaufstellungen ** angezeigt werden:

-   **Allgemein** – Allgemeine Informationen zur grundlegende Gewinn- und Verluststruktur des Projekts.
-   **Gewinn und Verlust** - Informationen zum antizipierten Umsatzerlös.
-   **RIF** – Informationen zu RIF-Kontosalden.
-   **Verbrauch** – Informationen zum Verbrauch für Stunden, Artikel, Ausgaben und Lohnabrechnungsbuchungen.
-   **Rechnung** – Informationen zu Rechnungen und Akontofakturierung.
-   **Stundensatz** – Die Stundensätze für die in GuV-Konten gebuchten Stunden.



