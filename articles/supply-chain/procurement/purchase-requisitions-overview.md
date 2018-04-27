---
title: "Übersicht über Bestellanforderung"
description: Dieses Thema beschreibt den Bestellanforderungsworkflow und die verschiedenen Statuswerte, die eine Bestellanforderung haben kann.
author: mkirknel
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchReqConsolidation, PurchReqCreate, PurchReqCreatePurchDetails, PurchReqCreatePurchListPage, PurchReqTable, PurchReqTableListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 2174
ms.assetid: 77d07119-4d9f-4c0e-acbe-d319203571ab
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 5d379b034c996cb0eff20a44960ba1e2701af81a
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---

# <a name="purchase-requisition-overview"></a>Übersicht über Bestellanforderung

[!INCLUDE [banner](../includes/banner.md)]

Dieses Thema beschreibt den Bestellanforderungsworkflow und die verschiedenen Statuswerte, die eine Bestellanforderung haben kann.

Je nach Einstellungen Ihrer Organisation können Sie unter Umständen Bestellanforderungen für von der Organisation verwendete Produkte erstellen. Bei einer Bestellanforderung handelt es sich um ein internes Dokument, durch das die Einkaufsabteilung zum Einkauf von Artikeln oder Dienstleistungen autorisiert wird.  

Nachdem eine Bestellanforderung genehmigt wurde, kann auf deren Grundlage eine Bestellung generiert werden. Bei Bestellungen handelt es sich um die externen Dokumente, die die Einkaufsabteilung an Kreditoren übermittelt.

## <a name="creating-purchase-requisitions"></a>Erstellen von Bestellanforderungen
Sie können eine Bestellanforderung auf der Seite **Eigene Bestellanforderungen** erstellen und die Artikel und Dienstleistungen auswählen, die Sie benötigen. Sie können Artikel aus einem Beschaffungskatalog auswählen, den Ihre Organisation erstellt hat, oder Artikel anfordern, die nicht im Katalog enthalten sind, indem Sie eine Beschaffungskategorie auswählen und die Produktdetails eingeben.  

Bevor Sie eine Bestellanforderung zur Prüfung übermitteln können, müssen Workflows im Microsoft Dynamics 365 for Finance and Operations konfiguriert werden. Sie verwenden einen Workflow, um eine Bestellanforderung vom Anfangsstatus **Entwurf** bis zum endgültigen Status **Genehmigt** durch den Prüfungsprozess zu leiten.

### <a name="purchase-requisition-statuses"></a>Bestellanforderungsstatus

Wenn Sie eine Bestellanforderung erstellen, wird ihr ein Status zugewiesen. Ein Status wird zudem jeder Position zugewiesen, die Sie einer Bestellanforderung hinzufügen. Wenn Sie eine Bestellanforderung zur Prüfung an einen Workflow übermitteln, wird der Status der Bestellanforderung und der Status jeder einzelnen Positionen aktualisiert, während die Positionen den Workflowprozess durchlaufen.  

Der Workflowprozess für Bestellanforderungen kann so konfiguriert werden, dass eine Bestellanforderung in Form eines einzelnen Dokuments durch den Prüfprozess geleitet wird. Alternativ können die Positionen einer Bestellanforderung einzeln an die entsprechenden Prüfer weitergeleitet werden. Wenn die Bestellanforderungspositionen einzeln geprüft werden, kann der Status jeder Bestellanforderungsposition aktualisiert werden, während die Positionen den Prüfprozess durchlaufen. Wenn der Prüfprozess für alle Positionen abgeschlossen ist und für die Bestellanforderung keine Prüfschritte mehr ausstehen, wird der Status der gesamten Bestellanforderung aktualisiert.

### <a name="purchase-requisition-workflow"></a>Bestellanforderungsworkflow

Das folgende Diagramm zeigt die Statuswerte an, die einer Bestellanforderung und einer Bestellanforderungsposition zugewiesen werden, wenn diese den Workflowprozess durchlaufen.  

[![Statuswerte von Bestellanforderungskopf und -position](./media/purchasereq_headerline_statuses.jpg)](./media/purchasereq_headerline_statuses.jpg)

### <a name="purchase-requisition-header-and-line-status-relationships"></a>Statusbeziehungen von Bestellanforderungskopf und -position

Der Gesamtstatus einer Bestellanforderung wird durch den Status der Bestellanforderungspositionen bestimmt. Daher muss der Prüfprozess für alle Bestellanforderungspositionen abgeschlossen sein, bevor der Prüfprozess für die gesamte Bestellanforderung abgeschlossen werden kann. In der folgenden Tabelle werden die Statuswerte beschrieben, die einem Bestellanforderungskopf und den Bestellanforderungspositionen zugewiesen werden, während die Bestellanforderung den Workflowprozess durchläuft.

<table>
<thead>
<tr class="header">
<th>Bestellanforderungsstatus</th>
<th>Status der Bestellanforderungsposition</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Überblick</td>
<td>Überblick</td>
<td>Die Bestellanforderung und die Bestellanforderungsposition wurden zwar erstellt, aber noch nicht zur Prüfung übermittelt. Bestellanforderungen und Bestellanforderungspositionen können geändert werden, wenn sie den Status <strong>Entwurf</strong> aufweisen. Eine Bestellanforderung oder Bestellanforderungsposition kann auch den Status <strong>Entwurf</strong> besitzen, wenn sie erneut aufgerufen, aber nicht erneut zur Prüfung übermittelt wurde. <strong>Hinweis:</strong> Nur Bestellanforderungen auf Dokumentebene können übermittelt oder erneut aufgerufen werden. Sie können jedoch eine einzelne Bestellanforderungsposition nicht übermitteln oder erneut aufrufen.</td>
</tr>
<tr class="even">
<td>Wird überprüft</td>
<td><ul>
<li>Wird überprüft</li>
<li>Abgelehnt</li>
</ul></td>
<td>Wenn der Workflow so konfiguriert wurde, dass die Bestellanforderungspositionen an einzelne Prüfer geleitet werden, kann jede einzelne Position den Status <strong>Wird überprüft</strong> oder <strong>Abgelehnt</strong> aufweisen. Der Bestellanforderungsstatus wird aktualisiert, wenn der Prüfprozess für alle Bestellanforderungspositionen abgeschlossen ist und für die Bestellanforderung keine Prüfschritte mehr ausstehen.
<ul>
<li><strong>Wird überprüft</strong> – Die Bestellanforderungspositionen wurden zur Prüfung übermittelt. Wenn der Workflowprozess für eine Bestellanforderungsposition abgeschlossen ist, verbleibt der Status dieser Position <strong>Wird überprüft</strong>, bis alle verbleibenden Bestellanforderungspositionen geprüft wurden.</li>
<li><strong>Abgelehnt</strong> – Die Bestellanforderung wurde abgelehnt. Abgelehnte Bestellanforderungspositionen können geändert und erneut übermittelt werden.</li>
</ul>
Wenn Sie eine Bestellanforderungsposition, die abgelehnt wurde, erneut übermitteln, wird der Prüfprozess für alle Positionen in der Bestellanforderung, die noch geprüft werden, erneut gestartet. <strong>Hinweis:</strong> Eine Bestellanforderung, die bereits übermittelt wurde, kann erneut aufgerufen werden. Wenn Sie eine Bestellanforderung erneut aufrufen, werden auch alle anderen Bestellanforderungspositionen erneut aufgerufen. Erneut aufgerufene Bestellanforderungspositionen können gelöscht werden.</td>
</tr>
<tr class="odd">
<td>Abgelehnt</td>
<td>Abgelehnt</td>
<td>Die Bestellanforderung und alle Bestellanforderungspositionen wurden abgelehnt. Bestellanforderungen und Bestellanforderungspositionen, die abgelehnt wurden, können erneut übermittelt werden.</td>
</tr>
<tr class="even">
<td>Genehmigt</td>
<td><ul>
<li>Genehmigt</li>
<li>Abgebrochen</li>
<li>Geschlossen</li>
</ul></td>
<td>Alle Bestellanforderungspositionen haben den Prüfprozess durchlaufen, und es stehen keine weiteren Prüfschritte für die Bestellanforderung aus.
<ul>
<li><strong>Genehmigt</strong> – Der Prüfungsprozess für eine Bestellanforderungsposition wurde abgeschlossen und die Position wurde genehmigt.</li>
<li><strong>Storniert</strong> – Die Bestellanforderungsposition wurde zwar genehmigt, dann aber storniert, da sie nicht mehr erforderlich ist. Nur genehmigte Bestellanforderungspositionen können storniert werden.</li>
<li><strong>Geschlossen</strong> - Die Bestellanforderungsposition wurde genehmigt und Dokumente sind je nach Anforderungszweck generiert worden.
<ul>
<li>Wenn der Anforderungszweck Verbrauch ist, wird eine Bestellung für die Bestellanforderungsposition generiert.</li>
<li>Wenn der Anforderungszweck Auffüllung ist, wurde mindestens ein Erfüllungsdokument generiert.</li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td>Abgebrochen</td>
<td>Abgebrochen</td>
<td>Die ausgewählte Bestellanforderung und alle Bestellanforderungspositionen wurden abgebrochen. <strong>Hinweis:</strong> Wenn Sie einen Artikel, der sich in einer Bestellanforderungsposition befindet, nicht mehr benötigen, muss diese Bestellanforderungsposition storniert werden, falls sie bereits genehmigt wurde. Nur genehmigte Bestellanforderungspositionen können storniert werden. Wenn derzeit Bestellanforderungspositionen geprüft werden, besitzt die Bestellanforderung den Status <strong>Wird überprüft</strong>. In diesem Fall können Sie die Bestellanforderung erneut aufrufen und die entsprechende Bestellanforderungsposition löschen.</td>
</tr>
<tr class="even">
<td>Geschlossen</td>
<td><ul>
<li>Geschlossen</li>
<li>Abgebrochen</li>
</ul></td>
<td>Die Bestellanforderung wurde geschlossen und mindestens ein Erfüllungsdokument wurde generiert.
<ul>
<li><strong>Geschlossen</strong> – Die Bestellanforderungsposition wurde genehmigt und Dokumente sind je nach Anforderungszweck generiert worden.
<ul>
<li>Wenn der Anforderungszweck Verbrauch ist, wird eine Bestellung für die Bestellanforderungsposition generiert.</li>
<li>Wenn der Anforderungszweck Auffüllung ist, wurde mindestens ein Erfüllungsdokument generiert.</li>
</ul></li>
<li><strong>Storniert</strong> – Die Bestellanforderungsposition wurde zwar genehmigt, dann aber storniert, da sie nicht mehr erforderlich ist. Nur genehmigte Bestellanforderungspositionen können storniert werden.</li>
</ul>
<strong>Hinweis:</strong> Wenn Sie einen Artikel, der sich in einer geschlossenen Bestellanforderungsposition befindet, nicht mehr benötigen, muss die Position in dem Erfüllungsdokument storniert werden, das für die Bestellanforderungsposition generiert wurde.</td>
</tr>
</tbody>
</table>

## <a name="distributing-costs-to-multiple-financial-accounts"></a>Verteilen von Kosten auf mehrere Finanzkonten
Die Kosten eines Produkts, das in einer Bestellanforderung enthalten ist, können auf mehrere Finanzkonten verteilt werden. Wenn in der Organisation Dimensionen (beispielsweise Kostenstellen oder Abteilungen) verwendet werden, können die Kosten eines Produkts auf Dimensionen für Finanzkonten verteilt werden.

## <a name="requisition-purposes"></a>Anforderungszwecke
Durch Anforderungszwecke wird der Prozess des Erfüllens des Anforderungsbedarfs flexibler. Wenn Sie eine Anforderung erstellen, können Sie ihm einen von zwei Zwecken zuweisen: Verbrauch oder Auffüllung. Abhängig vom Materialanforderungszweck und der Einrichtung Ihre Organisation, kann Anforderungsbedarf durch eine Bestellung, einen Umlagerungsauftrag, einen Produktionsauftrag oder ein Kanban erfüllt werden.  

In den Beschaffungsrichtlinien können Sie die Anforderungszwecke steuern, die verfügbar sind, wenn eine Anforderung für die Organisation erstellt wird.

### <a name="requisitions-that-have-a-purpose-of-consumption"></a>Anforderungen, die Verbrauch als Zweck haben

Eine Anforderung, die Verbrauch als Zweck hat, repräsentiert einen Bedarf für Artikel oder Dienstleistungen, die intern von Ihrer Organisation verwendet werden. Der Bedarf, der durch diese Art der Anforderung entsteht, wird immer durch eine Bestellung erfüllt. Wenn Microsoft Dynamics 365 for Finance and Operations eingerichtet ist, um Bestellungen automatisch zu generieren, werden Bestellungen erstellt, nachdem die Bestellanforderung genehmigt wurde.

### <a name="requisitions-that-have-a-purpose-of-replenishment"></a>Anforderungen, die Auffüllung als Zweck haben

Eine Anforderung, deren Zweck Wiederbeschaffung ist, repräsentiert einen Bedarf zur Auffüllung des Bestands. Sie möchten beispielsweise eine Anforderung erstellen, um Artikel aufzufüllen, sodass sie an einen spezifischen Einzelhandelsstandort zu einem bestimmten Zeitpunkt verkauft werden können. Der Bedarf, der durch diese Art von Anforderung erstellt wird, kann durch eine Bestellung, einen Umlagerungsauftrag, einen Produktionsauftrag oder ein Kanban erfüllt werden.  

Wenn der Anforderungszweck Auffüllung ist, wird Bedarf als Menge anstatt als Geldbetrag ausgedrückt. Daher gelten die Belastungsverwaltung, die Budgetsteuerung, Geschäftsregeln für die Anlagenbestimmung (BRAD), Projektbuchhaltung und alle zugehörigen Regeln nicht. Nur Produkte, die in der angegebenen juristischen Person gelagert und freigegeben werden, können Auffüllungsanforderungsbedarf erfüllen. Um die Produkte zu definieren, die verfügbar sind, wenn der Anforderungszweck die Wiederbeschaffung ist, verwenden Sie die Seite **Richtlinienregel für Auffüllungskategoriezugriff**.  

Um Bestellanforderungen zu verwenden, deren Zweck Auffüllung ist, müssen Sie den Produktprogrammplanungslauf so einrichten, dass Anforderungsbedarf enthalten ist. Die Erfüllungsmethode für den Bedarf, der durch diese Art von Anforderung erstellt wird, wird dann automatisch bestimmt, basierend auf den Beschaffungsrichtlinien, die für die Artikel in der Organisation eingerichtet und mithilfe des Produktprogrammplanungslaufs geplant wurden.

## <a name="purchase-requisitions-and-requests-for-quotation"></a>Bestellanforderungen und Angebotsanforderungen
In einigen Fällen müssen Sie einen Angebotsanforderungsprozess beginnen, um den Händler und Preis für Produkte zu identifizieren, die in einer Bestellanforderung angefordert werden. Eine Angebotsanforderung kann generiert werden, wenn die Bestellanforderung überprüft wird. Wenn Sie ein Angebot akzeptieren, werden Informationen zu Händler, Preis usw. zur Anforderung übertragen.  

Sie können eine Bestellanforderung sperren, indem Sie das Kontrollkästchen auf **Gesperrt** die **Bestellanforderungsdetails** Seite auswählen. Die Verarbeitung der Bestellanforderung kann fortfahren, nachdem der aufgehoben, indem Sie das Kontrollkästchen deaktivieren.  

**Hinweis:** Im eProcurement lässt es die Angebotsanforderung für Ihre Bestellanforderung möglicherweise Händlern zu, alternative Positionen hinzuzufügen. In diesem Fall spiegelt Ihre Bestellanforderung genehmigte Alternativen wieder.

## <a name="demand-consolidation"></a>Bedarfskonsolidierung
Wenn Sie Bestellanforderungspositionen aus mehreren Bestellanforderungen konsolidieren, können Sie Ihre Verhandlungsposition mit Ihren Kreditoren stärken, um eine bessere Preisgestaltung sowie niedrigere Liefer- und Versandkosten sowie verringerte Gemeinkosten zu erreichen.  

Bestellanforderungspositionen kommen für die Bedarfskonsolidierung in Frage, wenn die folgenden Anforderungen erfüllt sind:

-   Die Bestellanforderung wurde genehmigt.
-   Die Bestellanforderung entspricht den Einkaufsrichtlinienregelkriterien für die manuelle Bearbeitung und die Bedarfskonsolidierung.

Genehmigten Bestellanforderungspositionen, die den Kriterien für manuelle Bearbeitung entsprechen, werden auf der Seite **Genehmigte Bestellanforderungen freigeben** aufgeführt. Wenn eine Bestellanforderungsposition auch die Kriterien für die Bedarfskonsolidierung erfüllt, kann die Position einer Konsolidierungseinheit hinzugefügt werden.  

Eine Konsolidierungseinheit ist ein Satz Bestellanforderungspositionen, die zusammen gruppiert werden, damit der Einkäufer mit Kreditoren den besten Abschluss aushandeln kann. Bestellanforderungspositionen, die Sie für eine Konsolidierungseinheit auswählen, werden auf der Seite **Bestellanforderungskonsolidierung** angezeigt. Sie können die Positionen auf dieser Seite ändern, wenn Änderungen erforderlich sind. Sie können auch neue Positionen zur Konsolidierungseinheit hinzufügen oder vorhandene Positionen entfernen.  

Nachdem Sie die Anforderungspositionen einer Konsolidierungseinheit hinzugefügt und die Änderungen vorgenommen haben, die Sie benötigen, können Sie eine Bestellung für die konsolidierten Bestellanforderungspositionen erstellen.  

**Hinweis:** Änderungen, die Sie an einer Bestellanforderungsposition auf der Seite **Bestellanforderungskonsolidierung** vornehmen, werden in der Bestellung, die Sie erstellen, widergespiegelt. In der Bestellanforderung verbleibt die Position jedoch unverändert, sodass die zugehörigen Historie erhalten bleibt.  

Um eine Bestellung für Bestellanforderungspositionen zu erstellen, die nicht für die Bedarfskonsolidierung infrage kommen oder die nicht für eine Konsolidierungseinheit ausgewählt werden, müssen Sie die Positionen manuell verarbeiten.

### <a name="consolidating-purchase-requisition-lines"></a>Konsolidierung der Bestellanforderungspositionen

Der Prozess für die Bedarfskonsolidierung beginnt, wenn eine Bestellanforderung in einem Workflow genehmigt wird und wenn die Budgetsteuerung für Ihre Organisation konfiguriert wird, wenn die Budgetreservierungen und Vorabbelastungen erfasst worden sind. Das folgende Diagramm zeigt den Prozessfluss für die Bedarfskonsolidierung an.  

[![Ablaufdiagramm zur Bedarfskonsolidierung](./media/demand-consolidation.gif)](./media/demand-consolidation.gif)  

Um genehmigte Bestellanforderungspositionen zu konsolidieren, führen Sie folgende Schritte aus:

1.  Überprüfen Sie die genehmigten Bestellanforderungspositionen, die zur manuellen Verarbeitung zurückgehalten wurden und die für die Bedarfskonsolidierung infrage kommen.
2.  Wählen Sie Positionen aus, um sie zu einer Konsolidierungseinheit hinzuzufügen.
3.  Erstellen Sie eine neue Konsolidierungseinheit oder fügen Sie Anforderungspositionen einer vorhandenen Konsolidierungseinheit hinzu.
4.  Nehmen Sie alle erforderlichen Änderungen an den Anforderungspositionen vor und entfernen Sie Anforderungspositionsartikel, die nicht mehr in der Konsolidierungseinheit enthalten sein sollen.
5.  Erstellen Sie Bestellungen für konsolidierte Anforderungspositionen oder für Bestellanforderungspositionen in einer Konsolidierungseinheit.


<a name="see-also"></a>Siehe auch
--------

[Erstellen einer Anforderung für Verbrauch (Aufgabenleitfaden)](tasks/create-requisition-consumption.md)

[Bestellanforderungsworkflow](purchase-requisitions-workflow.md)




