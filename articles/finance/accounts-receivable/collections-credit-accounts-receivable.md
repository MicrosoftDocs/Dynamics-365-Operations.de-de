---
title: Inkasso bei Debitoren
description: Informationen zu Debitoreninkassi werden in einer zentralen Ansicht auf der Seite „Inkassi“ von Microsoft Dynamics 365 Finance verwaltet. Bearbeiter von Gutschriften und Inkassovorgängen können diese zentrale Ansicht zum Verwalten von Inkassi verwenden. Inkassobeauftragte können den Inkassovorgang über Debitorenlisten beginnen, die unter Verwendung vordefinierter Kriterien generiert werden, oder über die Seite „Debitoren”.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustAgingSnapshot, CustBankAccounts, CustCollections, CustCollectionsActivitiesListPage, CustCollectionsAgent, CustCollectionsCaseListPage, CustCollectionsPool, CustCollectionsPoolsListPage, CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3061
ms.assetid: fd851520-8d93-434b-845b-be127d6ac3a6
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c150eb7283b34c82e728da36ed0e1e6643eff46a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443448"
---
# <a name="collections-in-accounts-receivable"></a>Inkasso bei Debitoren

[!include [banner](../includes/banner.md)]

Informationen zu Debitoreninkassi werden in einer zentralen Ansicht auf der Seite „Inkassi“ von Microsoft Dynamics 365 Finance verwaltet. Bearbeiter von Gutschriften und Inkassovorgängen können diese zentrale Ansicht zum Verwalten von Inkassi verwenden. Inkassobeauftragte können den Inkassovorgang über Debitorenlisten beginnen, die unter Verwendung vordefinierter Mahnkriterien generiert werden, oder über die Seite "Debitoren".

Bevor Sie mit dem Einrichten oder Verwenden von Inkassovorgängen beginnen, sollten Sie über Folgendes informiert sein:
-   Fälligkeitsmomentaufnahmen zu Debitoren enthalten Saldorückblickinformationen zu einem bestimmten Zeitpunkt
-   Debitorenpools für Inkassi unterstützen Sie beim Organisieren Ihrer Arbeit
-   Inkassobeauftragte können über eigene Debitorenpools verfügen
-   Auf Listenseiten werden Debitoren, Aktivitäten und Anfragen organisiert
-   Alle Inkassoinformationen für einen Debitor befinden sich auf einer Seite, und Sie können über diese Seite Aktionen ausführen
-   Sie können Zinsen in einem Schritt erlassen, wieder erheben oder stornieren
-   Sie können Abschreibungsbuchungen in einem Schritt erstellen
-   Sie können Zahlungen mit unzureichender Deckung (NSF) in nur einem Schritt verarbeiten

In den folgenden Abschnitten werden diese Konzepte beschrieben.

## <a name="customer-aging-snapshots"></a>Fälligkeitsmomentaufnahmen für Debitoren 
Eine Fälligkeitsmomentaufnahme enthält die berechneten Saldenrückblicke für einen Debitor zu einem bestimmten Zeitpunkt. Diese Informationen werden auf der Listenseite "Saldenrückblick" und auf der Seite "Inkassi" angezeigt. Es muss eine Fälligkeitsmomentaufnahme erstellt werden, bevor Sie die Informationen auf den Listenseiten "Inkassi" anzeigen können. 

Eine Fälligkeitsmomentaufnahme enthält für jeden Debitor eine Kopfzeile und Detaildatensätze, die den einzelnen Zahlungsfristen in der Zahlungsfristendefinition entsprechen. 

Die Kopfzeile der Fälligkeitsmomentaufnahme enthält den fälligen Gesamtbetrag, das Kreditlimit, den Lieferscheinbetrag, den Auftragsbetrag, die Anzahl der beanstandeten Buchungen und die Gesamtzahl der beanstandeten Buchungen für das Debitorenkonto. Zur Berechnung dieser Beträge werden alle Buchungen für den Debitor herangezogen. Der fällige Gesamtbetrag, das Kreditlimit, der Lieferscheinbetrag und der Auftragsbetrag werden in der Infobox "Kreditinformationen" auf der Seite "Inkassi" angezeigt. 

Für jede Zahlungsfrist wird in der Zahlungsfristdefinition ein Fälligkeitsmomentaufnahmen-Detaildatensatz erstellt. Jeder Fälligkeitsmomentaufnahmen-Detaildatensatz enthält die Zahlungsfristkennung und den Gesamtbetrag der Buchungen mit den Datumsangaben, die innerhalb der Zahlungsfrist liegen. Buchungen werden einer Zahlungsfrist zugewiesen, z. B. 30 Tage überfällig. Das Datum ist relativ zum Datum "Fälligkeit per", das angegeben wird, wenn Sie die Fälligkeitsmomentaufnahme erstellen. Diese Informationen werden auf der Listenseite "Saldenrückblick" und in der Infobox "Saldenrückblick" auf der Seite "Inkassi" angezeigt.

## <a name="collections-customer-pools"></a> Debitorenpools für Inkassi 
Debitorenpools sind Abfragen, durch die eine Gruppe von Debitorendatensätzen definiert wird, die für Inkassi oder Fälligkeitsprozesse angezeigt und verwaltet werden können. Verwenden Sie Debitorenpools, um Informationen auf den Listenseiten "Saldenrückblick", "Inkassoaktivitäten" und "Inkassofälle" zu filtern. Sie verwenden Debitorenpools auch zum Filtern der Debitorenkonten, die einbezogen werden, wenn Fälligkeitsmomentaufnahmen erstellt werden.

## <a name="collections-agents"></a>Inkassobeauftragte
Standardmäßig können Benutzer von alle Debitoreninformationen auf Inkassolistenseiten anzeigen. Sie können Datensätze von Inkassobeauftragten verwenden, um die Debitorenpools zu ermitteln, die zum Filtern von Informationen auf den Inkassolistenseiten und im auf der Seite "Inkassi" verfügbar sind. 

Ein Inkassobeauftragter ist eine Person, die in Zusammenarbeit mit Debitoren sicherstellt, dass Zahlungen rechtzeitig eingehen. Inkassobeauftragte sind Arbeitskräfte, die Benutzern auf der Seite „Benutzereinstellungen“ zugewiesen werden.

## <a name="collections-list-pages"></a> Listenseiten "Inkassi" 
Die folgenden Listenseiten können zum Organisieren von Inkassoinformationen verwendet werden.
-   Saldenrückblick – Die Spalten auf der Listenseite zeigen die Debitorensalden und die fälligen Beträge nach Zahlungsfrist an. Diese Informationen werden als Fälligkeitsmomentaufnahme gespeichert. Die Zahlungsfristen werden anhand der verwendeten Zahlungsfristdefinition ermittelt. Die Zahlungsfristdefinition stammt aus dem Debitorenpool, falls dieser für die Poolabfrage angegeben wurde. Falls der Pool nicht über eine Zahlungsfristdefinition verfügt, wird die auf der Seite "Debitorenparameter" angegebene Zahlungsfristdefinition verwendet. Ist keine standardmäßige Zahlungsfristdefinition angegeben, wird die erste Zahlungsfristdefinition auf der Seite "Zahlungsfristdefinitionen" verwendet.
-   Inkassoaktivitäten – In den Spalten auf der Listenseite werden Aktivitäten angezeigt, die als Inkassoaktivitäten identifiziert werden. Diese Aktivitäten werden mithilfe der Seite "Inkassi" erstellt. Verwenden Sie die Aktivitäten, um die durchgeführten Inkassoaufgaben zu verfolgen.
-   Inkassofälle – In den Spalten auf der Listenseite werden Informationen für Anfragen angezeigt, die über eine Anfragenkategorie mit dem Anfragentyp "Inkassi" verfügen.

> [!NOTE]
> Es muss eine Fälligkeitsmomentaufnahme erstellt werden, bevor Sie die Informationen auf diesen Listenseiten anzeigen können. Es werden nur Informationen für Debitoren angezeigt, für die eine Fälligkeitsmomentaufnahme erstellt wurde. Die auf der Listenseite angezeigten Datensätze können zusätzlich wie folgt gefiltert werden:
> <li>Standardmäßig hat ein Finance and Operations-Benutzer Zugriff auf alle Debitoren, die über eine Fälligkeitsmomentaufnahme verfügen.</li>
> <li>Falls Debitorenpools vorhanden sind, muss ein Benutzer als Inkassobeauftragter eingerichtet werden, um die Pools zum Filtern von Informationen auf den Inkassolistenseiten zu verwenden. Die Informationen sind auf die Debitoren beschränkt, die im ausgewählten Debitorenpool enthalten sind.</li>
> <li>Wenn ein Benutzer als Inkassobeauftragter eingerichtet ist, sind nur die für diesen Inkassobeauftragten ausgewählten Pools auf der Listenseite verfügbar. Wenn die Umschaltfläche "Inkassobeauftragtem das Anzeigen aller Debitorenpools erlauben" auf der Seite "Inkassobeauftragter" für den Inkassobeauftragten ausgewählt ist, sind für den Beauftragten alle Pools verfügbar.</li>


## <a name="collections-page"></a> Seite "Inkassi"
Verwenden Sie die Seite "Inkassi", um Inkassoinformationen, Aktivitäten und Anfragen für einen Debitor anzuzeigen, zu verwalten und Aktionen dafür auszuführen. 

Im oberen Bereich werden Buchungen für den ausgewählten Debitor angezeigt. Im mittleren Bereich werden Buchungen für den ausgewählten Debitor angezeigt. Im unteren Bereich werden Aktivitäten für den ausgewählten Debitor angezeigt. Sie können Inkassoanfragen erstellen, um Inkassoinformationen für eine oder mehrere Buchungen und Aktivitäten nachzuverfolgen. Die Informationen im oberen und unteren Bereich können nach Anfrage gefiltert werden. 

In Infoboxen werden Saldenrückblicke und Kreditlimitinformationen für den ausgewählten Debitor angezeigt. Diese Informationen werden in der Fälligkeitsmomentaufnahme gespeichert. Bei Bedarf können Sie die Fälligkeitsmomentaufnahme mit aktuellen Informationen aktualisieren. 

Der Aktivitätsbereich enthält Schaltflächen, die verwandte Informationen zum ausgewählten Debitor, zur Anfragen, zur Buchung oder zur Aktivität anzeigen. Sie können auch häufige Aktionen durchführen, z. B. das Ändern des Inkassostatus einer Transaktion, das Senden von E-Mail-Korrespondenz durch die Integration mit Ihrem E-Mail-Anbieter, das Leisten von Rückerstattungen an Debitoren, das Verarbeiten von NSF-Zahlungen und das Abschreiben von uneinbringbaren Salden.

## <a name="waive-reinstate-or-reverse-interest-and-fees"></a> Aufheben, Wiedererheben oder Stornieren von Zinsen und Gebühren 
Sie können ganze Zinsrechnungen oder mit Zinsrechnungen zusammenhängende Gebühren und Buchungszinsen erlassen, wieder erheben oder stornieren. Verwenden Sie dazu im Aktivitätsbereich auf der Listenseite "Alle Debitoren" die Registerkarte "Mahnen", indem Sie auf "Zinsrechnung", "Buchungszinsen" oder "Gebühr" klicken. 

Diese Regulierungen wirken sich nur auf Zinsrechnungen und die darin enthaltenen Zinsen und Gebühren aus. Verwenden Sie die Schritte im Abschnitt "Erstellen Sie Abschreibungsbuchungen in einem Schritt", um alle Gebühren abzuschreiben, die ein Debitor schuldet.

Weitere Informationen finden unter [Erstellen Sie einen Zinscode mit einem Bereich](tasks/create-interest-code-range.md) und [Verarbeiten Sie Zinsen](tasks/process-interest.md). 

## <a name="create-writeoff-transactions"></a>Abschreibungsbuchungen erstellen
Sie können uneinbringliche Außenstände abschreiben, indem Sie im Formular "Inkassi" auf "Abschreiben" klicken, sowie auf den Listenseiten "Saldenrückblick" und "Offene Debitorenrechnungen". 

Wenn Sie Buchungen für einen Debitor abschreiben, werden alle Buchungen für den Debitor automatisch für den Ausgleich markiert. Der Betrag, der abgeschrieben wird, hängt vom Nettobetrag der markierten Buchungen ab. Die Abschreibungsbuchung wird in einer allgemeinen Erfassung erstellt und kann bis zu drei Arten von Erfassungspositionen enthalten.

-   Der erste Typ der Erfassungsposition enthält den Abschreibungseintrag für den Debitor. Wenn die markierten Buchungen mehrere Kombinationen aus Währungscodes, Dimensionen und Buchungsprofilen beinhalten, wird für jede Kombination eine gesonderte Erfassungsposition erstellt.
-   Der zweite Typ der Erfassungsposition enthält den Abschreibungseintrag für das Sachkonto. Wenn die markierten Buchungen mehrere Kombinationen aus Währungscodes, Dimensionen und Buchungsprofilen beinhalten, wird für jede Kombination eine gesonderte Erfassungsposition erstellt.
-   Der dritte Typ der Erfassungsposition enthält die Abschreibungsinformationen für Mehrwertsteuern für das Sachkonto. Diese Erfassungsposition wird nur erstellt, wenn die Umschalttaste "Separate Mehrwertsteuer" auf der Seite "Debitorenparameter" ausgewählt wird. Wenn die markierten Buchungen mehrere Kombinationen aus Mehrwertsteuerkonto, Dimensionen und Mehrwertsteuercode beinhalten, wird für jede Kombination eine gesonderte Erfassungsposition erstellt.

Die Abschreibungsbuchung wird in der Buchungswährung erstellt.

Weitere Informationen finden Sie unter [Erstellen Sie eine Tilgungserfassung für einen Debitor](tasks/create-write-off-journal-customer.md).

<a name="process-not-sufficient-funds-nsf-payments"></a>Verarbeiten von Zahlungen ohne ausreichende Deckung (NSF)  
--------------------------------------------

Sie können NSF-Zahlungen verarbeiten, indem Sie auf der Seite "Inkassi" auf "NSF-Zahlung" klicken. Wenn Sie auf diese Schaltfläche klicken, wird die Zahlung storniert. Falls für den Debitor eine NSF-Gebühr anfällt, wird in der Zahlungserfassung eine Belastungsbuchung erstellt. Der Betrag der Gebühr hängt von den Einstellungen für die automatischen Belastungen ab. Die für NSF-Zahlungen geltenden automatischen Belastungen werden durch die Belastungsgruppe angegeben, die auf der Seite "Bankkonten" für das jeweilige Bankkonto ausgewählt wird.





