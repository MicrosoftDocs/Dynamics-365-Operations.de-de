---
title: Schlüsselkonzepte der Inkassoverwaltung
description: Die Themen definieren Schlüsselkonzepte der Inkassoverwaltung.
author: mikefalkner
ms.date: 11/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c0a6cbdb79f0ee0c51b2e1fb7af93931da490c1bb514dfed89d48412f6779fdf
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724038"
---
# <a name="collections-management-key-concepts"></a>Schlüsselkonzepte der Inkassoverwaltung

[!include [banner](../includes/banner.md)]

Bevor Sie mit dem Einrichten oder Verwenden von Inkassovorgängen beginnen, sollten Sie über Folgendes informiert sein:

- Fälligkeitsmomentaufnahmen zu Debitoren enthalten Saldorückblickinformationen zu einem bestimmten Zeitpunkt.
- Debitorenpools für Inkassi unterstützen Sie beim Organisieren Ihrer Arbeit.
- Inkassobeauftragte können über eigene Debitorenpools verfügen.
- Auf Listenseiten werden Debitoren, Aktivitäten und Anfragen organisiert.
- Alle Inkassoinformationen für einen Debitor befinden sich auf einer Seite, und Sie können über diese Seite Aktionen ausführen.
- Sie können Zinsen und Gebühren in einem Schritt erheben, wieder erheben oder stornieren.
- Abschreibungsbuchungen können in einem Schritt erstellt werden.
- Zahlungen mit unzureichender Deckung (NSF) können in nur einem Schritt verarbeitet werden.

In diesem Thema werden die einzelnen Konzepte beschrieben.

## <a name="customer-aging-snapshots"></a>Fälligkeitsmomentaufnahmen für Debitoren 

Eine Fälligkeitsmomentaufnahme enthält die berechneten Saldenrückblicke für einen Debitor zu einem bestimmten Zeitpunkt. Diese Informationen werden auf der Listenseite **Saldenrückblick** und auf der Seite **Inkassi** angezeigt. Eine Fälligkeitsmomentaufnahme muss erstellt werden, bevor Sie Informationen auf den Seiten der Inkassoliste anzeigen können (**Saldenrückblick**, **Inkassoaktivitäten** und **Inkassofälle**).

Eine Fälligkeitsmomentaufnahme verfügt für jeden Debitor über eine Kopfzeile und Detaildatensätze, die den einzelnen Zahlungsfristen in der Zahlungsfristendefinition entsprechen.

Die Kopfzeile der Fälligkeitsmomentaufnahme enthält den fälligen Gesamtbetrag, das Kreditlimit, den Lieferscheinbetrag, den Auftragsbetrag, die Anzahl der beanstandeten Buchungen und die Gesamtzahl der beanstandeten Buchungen für das Debitorenkonto. Zur Berechnung dieser Beträge werden alle Buchungen für den Debitor herangezogen. Der fällige Gesamtbetrag, das Kreditlimit, der Lieferscheinbetrag und der Auftragsbetrag werden in der Infobox **Kreditinformationen** auf der Seite **Inkassi** angezeigt.

Für jede Zahlungsfrist wird in der Zahlungsfristdefinition ein Detaildatensatz in der Fälligkeitsmomentaufnahme erstellt. Jeder Detaildatensatz enthält die ID der Zahlungsfrist und den Gesamtbetrag der Buchungen mit den Datumsangaben, die innerhalb der Zahlungsfrist liegen. Buchungen werden einer Zahlungsfrist zugewiesen, z. B. 30 Tage überfällig. Das Datum ist relativ zum Datum **Fälligkeit per**, das angegeben wird, wenn Sie die Fälligkeitsmomentaufnahme erstellen. Diese Informationen werden auf der Listenseite **Saldenrückblick** und in der Infobox **Saldenrückblick** auf der Seite **Inkassi** angezeigt.

## <a name="collections-customer-pools"></a> Debitorenpools für Inkassi 

Debitorenpools sind Abfragen, die eine Gruppe von Kundendatensätzen definieren. Mithilfe dieser gruppierten Datensätze können Sie Informationen zu den enthaltenen Kundenkonten anzeigen und Sammlungen oder Alterungsprozesse für diese verwalten. Verwenden Sie Debitorenpools, um Informationen auf den Listenseiten „Inkassi“ zu filtern. Sie können sie auch zum Filtern der Debitorenkonten verwenden, die einbezogen werden, wenn Fälligkeitsmomentaufnahmen erstellt werden.

## <a name="collections-agents"></a>Inkassobeauftragte

Standardmäßig können Benutzer alle Debitoreninformationen auf Inkassolistenseiten anzeigen. Anhand von Datensätzen von Inkassobeauftragten können Sie die Debitorenpools ermitteln, die zum Filtern von Informationen auf den Inkassolistenseiten und auf der Seite **Inkassi** verwendet werden.

Ein Inkassobeauftragter arbeitet mit Debitoren zusammen, damit Zahlungen rechtzeitig eingehen. Sie sind Arbeitskräfte, die Benutzern auf der Seite **Benutzereinstellungen** zugewiesen werden.

## <a name="collections-list-pages"></a> Listenseiten "Inkassi" 

Die folgenden Listenseiten können zum Organisieren von Inkassoinformationen verwendet werden:

- **Saldenrückblick** – Die Spalten auf der Listenseite zeigen die Debitorensalden und die fälligen Beträge nach Zahlungsfrist an. Diese Informationen werden in einer Fälligkeitsmomentaufnahme gespeichert. Die Zahlungsfristen werden anhand der verwendeten Zahlungsfristdefinition ermittelt. Die Zahlungsfristdefinition stammt aus dem Debitorenpool, sofern ein Debitorenpool für die Poolabfrage angegeben wurde. Falls der Pool nicht über eine Zahlungsfristdefinition verfügt, wird die auf der Seite **Debitorenkontenparameter** angegebene Zahlungsfristdefinition verwendet. Ist keine standardmäßige Zahlungsfristdefinition angegeben, wird die erste Zahlungsfristdefinition auf der Seite **Zahlungsfristdefinitionen** verwendet.
- **Inkassoaktivitäten** – In den Spalten auf dieser Listenseite werden Aktivitäten angezeigt, die als Inkassoaktivitäten identifiziert werden. Diese Aktivitäten werden mithilfe der Seite **Inkassi** erstellt. Sie verwenden Aktivitäten, um die durchgeführten Inkassoaufgaben zu verfolgen.
- **Inkassofälle** – In den Spalten auf dieser Listenseite werden Informationen für Anfragen angezeigt, die über eine Anfragenkategorie mit dem Anfragentyp **Inkassi** verfügen.

### <a name="aging-snapshots"></a>Fälligkeitsmomentaufnahmen

Es muss eine Fälligkeitsmomentaufnahme erstellt werden, bevor Sie die Informationen auf den Inkassolistenseiten anzeigen können. Es werden nur Informationen für Debitoren angezeigt, für die eine Fälligkeitsmomentaufnahme erstellt wurde. Die auf der Listenseite angezeigten Datensätze können zusätzlich wie hier beschrieben gefiltert werden:

- Standardmäßig haben Benutzer Zugriff auf alle Debitoren, die über eine Fälligkeitsmomentaufnahme verfügen.
- Falls Debitorenpools vorhanden sind, muss ein Benutzer als Inkassobeauftragter eingerichtet werden, um die Pools zum Filtern von Informationen auf den Inkassolistenseiten zu verwenden. Die Informationen sind auf die Debitoren beschränkt, die im ausgewählten Debitorenpool enthalten sind.
- Wenn ein Benutzer als Inkassobeauftragter eingerichtet ist, sind nur die für diesen Inkassobeauftragten ausgewählten Pools auf den Inkassolistenseiten verfügbar. Wenn die Option **Inkassobeauftragtem das Anzeigen aller Debitorenpools erlauben** auf der Seite **Inkassobeauftragter** für den Inkassobeauftragten ausgewählt ist, sind für den Beauftragten alle Pools verfügbar.

## <a name="collections-page"></a> Seite "Inkassi"

Sie können die Seite **Inkassi** verwenden, um Inkassoinformationen, Aktivitäten und Anfragen für einen Debitor anzuzeigen, zu verwalten und Aktionen dafür auszuführen.

Der obere Bereich der Seite zeigt Fälle für den ausgewählten Debitor, der mittlere Bereich zeigt Transaktionen für den Debitor und der untere Bereich zeigt Aktivitäten für den Debitor. Sie können Inkassoanfragen erstellen, um Inkassoinformationen für eine oder mehrere Buchungen und Aktivitäten nachzuverfolgen. Die Informationen in den oberen und unteren Abschnitten können nach Anfrage gefiltert werden.

In Infoboxen zeigen Saldenrückblicke und Kreditlimitinformationen für den ausgewählten Debitor an. Diese Informationen werden in der Fälligkeitsmomentaufnahme gespeichert. Bei Bedarf können Sie die Fälligkeitsmomentaufnahme mit aktuellen Informationen aktualisieren.

Der Aktivitätsbereich enthält Schaltflächen, mit denen Sie verwandte Informationen zum ausgewählten Debitor, zur Anfrage, zur Buchung oder zur Aktivität anzeigen können. Sie können auch häufige Aktionen durchführen, z. B. das Ändern des Inkassostatus einer Transaktion, das Senden von E-Mails durch die Integration mit Ihrem E-Mail-Anbieter, das Leisten von Rückerstattungen an Debitoren, das Verarbeiten von NSF-Zahlungen und das Abschreiben von uneinbringbaren Salden.

## <a name="waiving-reinstating-or-reversing-interest-and-fees"></a>Aufheben, Wiedererheben oder Stornieren von Zinsen und Gebühren

Sie können ganze Zinsrechnungen oder mit Zinsrechnungen zusammenhängende Gebühren und Buchungszinsen erlassen, wieder erheben oder stornieren. Wählen Sie in der Registerkarte **Einzug** im Aktivitätsbereich auf der Listenseite **Alle Debitoren** die Option **Zinsrechnung**, **Buchungszinsen** oder **Gebühr**.

Diese Regulierungen wirken sich nur auf Zinsrechnungen und die darin enthaltenen Zinsen und Gebühren aus. Informationen zum Abschreiben aller Gebühren, die ein Debitor schuldet, finden Sie im Abschnitt [Abschreibungsbuchungen anlegen](#creating-write-off-transactions) dieses Themas.

Weitere Informationen finden unter Erstellen Sie einen Zinscode mit einem Bereich und Verarbeiten Sie Zinsen.

## <a name="creating-write-off-transactions"></a>Abschreibungsbuchungen anlegen

Sie können uneinbringliche Außenstände abschreiben, indem Sie **Abschreiben** auf der Seite **Inkassi** und den Inkassolistenseiten auswählen.

Wenn Sie Buchungen für einen Debitor abschreiben, werden alle Buchungen für diesen Debitor automatisch für den Ausgleich markiert. Der Betrag, der abgeschrieben wird, hängt vom Nettobetrag der markierten Buchungen ab. Die Abschreibungsbuchung wird in einer allgemeinen Erfassung erstellt und kann bis zu drei Arten von Erfassungspositionen enthalten:

- Der erste Typ der Erfassungsposition enthält den Abschreibungseintrag für den Debitor. Wenn die markierten Buchungen mehrere Kombinationen aus Währungscodes, Dimensionen und Buchungsprofilen beinhalten, wird für jede Kombination eine gesonderte Erfassungsposition erstellt.
- Der zweite Typ der Erfassungsposition enthält den Abschreibungseintrag für das Sachkonto. Wenn die markierten Buchungen mehrere Kombinationen aus Währungscodes, Dimensionen und Buchungsprofilen beinhalten, wird für jede Kombination eine gesonderte Erfassungsposition erstellt.
- Der dritte Typ der Erfassungsposition enthält die Abschreibungsinformationen für Mehrwertsteuern für das Sachkonto. Diese Erfassungsposition wird nur erstellt, wenn die Option **Separate Mehrwertsteuer** auf der Seite **Debitorenparameter** ausgewählt wird. Wenn die markierten Buchungen mehrere Kombinationen aus Mehrwertsteuerkonto, Dimensionen und Mehrwertsteuercodes beinhalten, wird für jede Kombination eine gesonderte Erfassungsposition erstellt. Die Abschreibungsbuchung wird in der Buchungswährung erstellt. Weitere Informationen finden Sie unter Erstellen Sie eine Tilgungserfassung für einen Debitor.

## <a name="process-nsf-payments"></a>NSF-Zahlungen abwickeln

Sie können NSF-Zahlungen verarbeiten, indem Sie auf der Seite **Inkassi** auf **NSF-Zahlung** klicken. Wenn Sie diese Schaltfläche wählen, wird die Zahlung storniert. Falls für den Debitor eine NSF-Gebühr anfällt, wird in der Zahlungserfassung eine Belastungsbuchung erstellt. Der Betrag der Gebühr hängt von den Einstellungen für die automatischen Belastungen ab. Die für NSF-Zahlungen geltenden automatischen Belastungen werden durch die Belastungsgruppe angegeben, die auf der Seite **Bankkonten** für das jeweilige Bankkonto ausgewählt wird.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Einrichtung der Parameter für das Kundenkreditmanagement](./cm-credit-mgmt-setup.md)

[Einrichtung der Informationen für das Kundenkreditmanagement](./cm-setup-information.md)

[Hinzufügen der Informationen für das Kundenkreditmanagement](./cm-add-credit-mgmt-information-customer.md)

[Debitorenkreditgruppen](./cm-customer-credit-groups.md)

[Debitorenkreditlimitregulierungen](./cm-credit-limit-adjustments.md)

[Kreditsperren für Aufträge](./cm-sales-order-credit-holds.md)

[Periodische Aufgaben des Kundenkreditmanagements](./cm-periodic-tasks.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]