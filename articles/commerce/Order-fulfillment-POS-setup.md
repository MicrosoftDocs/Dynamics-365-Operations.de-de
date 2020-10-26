---
title: Auftragserfüllung für Filialen einrichten
description: Dieses Thema enthält eine Übersicht darüber, wie die Filialauftragserfüllung eingerichtet wird.
author: rubencdelgado
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: rubendel
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 118517fe0d7208113bd361a0295ff00cacd14f3d
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975122"
---
# <a name="set-up-order-fulfillment-for-stores"></a>Auftragserfüllung für Filialen einrichten

[!include [banner](includes/banner.md)]

## <a name="overview"></a>Überblick

Viele Einzelhändler möchten die Auftragserfüllung optimieren, indem Sie es Filialen ermöglichen, Aufträge zu erfüllen. Durch Auftragserfüllung auf Filialebene können zu große Lagerbestände für eine bestimmte Filiale vermieden werden. Sie kann auch aus logistischer Sicht in bestimmten Fällen erforderlich sein, wenn eine Filiale zusätzliche Kapazitäten besitzt oder sich in einer geringeren Versandentfernung zum Debitoren befindet. Um dieser Anforderung zu entsprechen, ist ein vereinheitlichter Auftragserfüllungsarbeitsgang in der Verkaufsstelle verfügbar.

Bei Aufträgen für Erfüllung in einer bestimmten Filiale ist der Lagerort der Filiale in der Kopfzeile oder den Positionen des Auftrags festgelegt.

Der Auftragserfüllungsarbeitsgang in der Verkaufsstelle enthält einen einzelnen Arbeitsbereich in der Verkaufsstelle, der verwendet werden kann, um Aufträge zu verarbeiten. Dies umfasst alles von der Annahme des Auftrags bis zur Markierung als versendet oder zum Initiieren der Filialabholung.

## <a name="set-up-the-order-fulfillment-operation"></a>Den Auftragserfüllungsarbeitsgang einrichten

Auftragserfüllung, [Arbeitsgangskennungs-ID 928](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-operations), kann dazu verwendet werden, um auf den Arbeitsbereich für die Filialauftragserfüllung in der Verkaufsstelle zuzugreifen.

Führen Sie die Schritte unter [Fügen Sie den Arbeitsgang einem Schaltflächenraster hinzu](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) durch, um anzugeben, welcher Parameter verwendet werden soll, wenn die Auftragserfüllung in der Verkaufsstelle aufgerufen werden soll. Standardmäßig wird nach Festlegung der Auftragserfüllungsarbeitsgänge die Option **Alle Aufträge** ausgewählt. Wenn er mit diesem Parameter konfiguriert wurde, werden durch den Arbeitsgang alle Auftragspositionen für die Erfüllung in der aktuellen Filiale aufgelistet. Zudem ist **Nicht ausgelieferte Bestellungen** verfügbar, was einer Schaltfläche zugewiesen und verwendet werden kann, wenn der Benutzer nur Aufträge sehen möchte, die aus der Filiale versendet werden. Schließlich gibt es **Aufträge zur Abholung**. Wenn dies in der Verkaufsstelle aufgerufen wird, werden dadurch nur Aufträge aufgelistet, die in der Filiale abgeholt werden müssen. Die verschiedenen Parameter können unterschiedlichen Schaltflächen zugewiesen werden, sodass der Benutzer verschiedene Möglichkeiten hat, die Auftragserfüllung anzuzeigen.

### <a name="enable-users-to-access-order-fulfillment-at-the-point-of-sale"></a>Aktivieren Sie Benutzer, um auf die Auftragserfüllung in der Verkaufsstelle zuzugreifen.

Der Auftragserfüllungsarbeitsgang verfügt nicht über einen eigenen Berechtigungsstandard, aber in der Zukunft benötigen Benutzer möglicherweise die Berechtigung **Abrufen des Auftrags zulassen**, um den Arbeitsgang von der Verkaufsstelle aus aufzurufen.

Auf Filialebene ist eine Konfigurationseinstellung verfügbar, um zu bestimmen, ob eine Auftragsposition manuell von innerhalb der Verkaufsstelle aus angenommen werden muss. Wenn diese Konfigurationsoption nicht festgelegt wird, werden Auftragspositionen standardmäßig angenommen. Wenn diese Konfigurationsoption aktiviert ist, müssen Benutzer in der Verkaufsstelle die Berechtigung **Annahme von Auftrag zulassen** besitzen, um Aufträge von innerhalb der Verkaufsstelle aus anzunehmen.

### <a name="enable-manual-order-acceptance"></a>Manuelle Auftragsannahme aktivieren

Standardmäßig werden Auftragspositionen, die einer Filiale zugewiesen sind, als **Angenommen** markiert. Das bedeutet, es wird angenommen, dass diese von der zugewiesenen Filiale aus erfüllt werden und nicht einer weiteren Zuweisung unterliegen werden. In bestimmten Fällen möchten Einzelhändler möglicherweise Aufträge manuell annehmen, bevor sie erfüllt werden können. Wenn beispielsweise eine Filiale unterbesetzt ist und keine Aufträge erfüllen kann, nimmt ein Filialleiter nur so viele Aufträge zur Abwicklung an, wie seiner Einschätzung nach am betreffenden Tag angemessen abgewickelt werden können. Bis ein Auftrag angenommen ist, wird er möglicherweise vom Backoffice einer anderen Filiale neu zugewiesen. Auf diese Weise bietet die Auftragsannahme auch eine Möglichkeit anzugeben, dass ein Auftrag von einer Filiale bestätigt wurde und erfüllt wird.

Auftragspositionen für die Filialabholung werden als **Ausstehend** markiert und unterliegen nicht der Annahme.

Um manuelle Annahme für Auftragspositionen zu aktivieren, navigieren Sie zu **Retail und Commerce** \> **Kanäle** \> **Einzelhandelsgeschäft** \> **Alle Einzelhandelsgeschäfte**. Wählen Sie die Filiale aus, und klicken Sie auf die Filialkennung, um die Details der Filiale anzuzeigen. Klicken Sie auf **Bearbeiten**. Suchen Sie im Inforegister **Allgemein** die Unterüberschrift **Auftragserfüllung**, und ändern Sie **Manuelles Annehmen** von **Nein** auf **Ja**.

### <a name="enable-reject-order-line-capability"></a>Auftragsablehnungsfunktion aktivieren

Auftragspositionen können von der Verkaufsstelle aus auch abgelehnt werden. Die Ablehnung einer Auftragsposition bedeutet, dass sie nicht in dieser Filiale erfüllt wird und die Auftragsposition wird zurückgesendet, um einer anderen Filiale oder Lagerort zugewiesen zu werden. Auftragspositionsablehnungsberechtigung wird durch die Berechtigung **Auftragsablehnung zulassen** in der POS-Berechtigungsgruppe gewährt, die der Arbeitskraft zugeordnet ist. Während sie eine Position ablehnen, können die Einzelhändler ihre Arbeitskräfte dazu bevollmächtigen, einen Grund für die Ablehnung anzugeben. Dies kann mithilfe von Infocodes mit **Infocode-Aktivität** des Typs **Auftragserfüllung** erreicht werden sowie durch Zuweisen des Infocodes zu **Auftragsposition ablehnen** im dem Kanal zugeordneten Funktionsprofil.

> [!NOTE]
> Nur die Infocodes mit **Infocode-Aktivität** des Typs **Auftragserfüllung** können der Aktivität **Auftragsposition ablehnen** zugewiesen werden.

### <a name="synchronize-changes-to-the-channel-database"></a>Änderungen an die Kanaldatenbank synchronisieren

Nachdem der Arbeitsgang zu einem Schaltflächenraster zugewiesen wurde, die richtigen Berechtigungen zugewiesen wurden und der Kanal konfiguriert ist, müssen die Änderungen mit der Kanaldatenbank synchronisiert werden. Dazug navigieren Sie zu **Retail and Commerce** \> **Retail and Commerce IT** \> **Verteilungszeitpläne**. Wählen Sie den Zeitplan „1090-Register” aus, um die Schaltflächenrasteränderungen zu synchronisieren, und klicken Sie dann auf **Jetzt ausführen**. Danach synchronisieren Sie die Berechtigungsänderungen, indem Sie „1060-Mitarbeiter” auswählen, und klicken Sie dann auf **Jetzt ausführen**. Danach synchronisieren Sie die Kanaländerungen, indem Sie „1070-Kanalkonfiguration” auswählen, und klicken Sie dann auf **Jetzt ausführen**. Schließlich synchronisieren Sie den neu erstellten Infocode für den Ablehnungsgrund, indem Sie die „1110-globale Konfiguration” auswählen, und klicken Sie auf **Jetzt ausführen**.

## <a name="use-order-fulfillment-at-the-point-of-sale"></a>Auftragserfüllung in der Verkaufsstelle verwenden

Öffnen Sie die Verkaufsstelle, und wählen Sie den Auftragserfüllungsarbeitsgang aus. Je nach Konfiguration werden entweder alle Positionen, Auftagspositionen zur Abholung oder Auftragspositionen für den Versand aufgelistet.

### <a name="order-fulfillment-view"></a>Auftragserfüllungsansicht

In der Auftragserfüllungsansicht werden alle Auftagspositionen zur Erfüllung in der Filiale aufgelistet, und die folgenden Spalten sind enthalten:

- Auftragsnummer
- Produktnummer
- Beschreibung
- Bestellte Menge
- Angefordertes Lieferdatum
- Kundenname
- Erfüllungsstatus

Zusätzliche Informationen für eine bestimmte Auftragsposition können angezeigt werden, indem die Auftragsposition ausgewählt wird und dann das Flyoutmenü geöffnet wird, das sich direkt unter dem angemeldeten Benutzer/Schichtinformationen, die in der Verkaufsstellenkopfzeile angezeigt werden, befindet. Dieses Menü enthält 2 Registerkarten: eine für Positionsdetails und eine andere für Auftragsdetails. Die Registerkarte für Positionsdetails enthält die folgenden Informationen:

- Bestellte Menge
- Verbleibende Menge, die versendet/abgeholt werden muss
- Entnommene Menge
- Verpackte Menge
- Fakturierte Menge (bereits abgeholt oder versendet)
- Lieferart
- Lieferadresse

Das Detailflyoutmenü hat auch eine Registerkarte, die weitere Auftragsebenendetails bereitstellt, einschließlich:

- Kundenname
- Debitor-ID
- Auftragsnummer
- Bestellung gesamt
- Auftragssaldo

Unten in der Auftragserfüllungsansicht befindet sich ein Aktivitätsbereich. Dies umfasst alle Aktivitäten, die an einer Auftragsposition ausgeführt werden können. Wenn eine Aktivität aufgrund des Status einer Position nicht verfügbar ist, wird diese Aktivität unverfügbar.

Standardmäßig haben Aufträge den Status **Angenommen**. Der Auftragsstatus kann als Spalte in der Liste von Auftragspositionen angezeigt werden. Wenn **Manuelle Annahme** auf Kanalebene konfiguriert wird, werden alle zu versendende Positionen als **Ausstehend** angezeigt, und sie müssen angenommen werden, bevor sie erfüllt werden können. Aufträge für die Filialabholung sind standardmäßig **Ausstehend** und müssen nicht angenommen werden.

### <a name="order-fulfillment-line-actions"></a>Auftragserfüllungs-Positionsaktivitäten

- **Bearbeiten** – Wenn ein Auftragsstatus aussteht, kann er in der Verkaufsstelle bearbeitet werden. Aufträge, die bereits teilweise entnommen, verpackt oder fakturiert wurden, können nicht von der Auftragserfüllungsansicht aus bearbeitet werden.
- **Annehmen** – Wenn **Manuell annehmen** auf der Kanalebene konfiguriert ist, müssen Positionen zuerst angenommen werden, bevor sie den Auftragserfüllungsprozess durchlaufen können.
- **Entnehmen** – Die Entnahmeoption unterstützt mehrere Aktivitäten. Zuallererst wird durch **Entnahme** der Status der Auftragsposition aktualisiert, damit andere in der Filiale nicht versuchen, dieselbe Position zu entnehmen. Als Nächstes wird durch **Kommissionierliste drucken** eine Kommissionierliste für die ausgewählte Position bzw. Positionen ausgedruckt und es wird auch deren Status zu **Entnahme** geändert. Kommissionierlistenformate werden als Teil der Bonformate gesteuert. Weitere Informationen zum Einrichten von Bonformaten finden Sie unter [Bonvorlagen und Drucken](https://docs.microsoft.com/dynamics365/unified-operations/retail/receipt-templates-printing). Schließlich wird durch **Als entnommen markieren** die Position angegeben, die entnommen wurde. **Als entnommen markieren** initiiert entsprechende Lagerbuchungen im Backoffice. Entnahmeaktivitäten können für mehrere Auftragspositionen gleichzeitig über verschiedene Aufträge hinweg sowie für alle Lieferarten ausgeführt werden.
- **Ablehnen** – Positionen oder Teilpositionen können abgelehnt werden. Dadurch können sie vom Backoffice einer anderen Filiale oder einem anderen Lagerort zugewiesen werden. Positionen können nur abgelehnt werden, wenn sie noch nicht entnommen oder verpackt wurden. Um eine Position abzulehnen die bereits entnommen oder verpackt wurde, muss vom Backoffice die Entnahme storniert und die Position wieder ausgepackt werden.
- **Verpacken** – Die Packoption unterstützt zwei Aktivitäten: Durch **Lieferschein drucken** wird ein Lieferschein für die ausgewählten Positionen gedruckt, und durch **Als gepackt markieren** werden die Positionen als gepackt markiert und die Positionen als geliefert im Backoffice markiert. Nur Auftragspositionen die zum selben Auftrag gehören und mit derselben Lieferart können gleichzeitig verpackt werden. Lieferscheinformate werden als Teil der Bonformate gesteuert. Weitere Informationen zum Einrichten von Bonformaten finden Sie unter [Bonvorlagen und Drucken](https://docs.microsoft.com/dynamics365/unified-operations/retail/receipt-templates-printing).
- –**Versenden** – Durch die Aktivität „Versenden” werden ausgewählte Positionen als **Geliefert** im Backoffice markiert. Nachdem eine Position vollständig versendet wurde, wird sie nicht mehr in der Auftragserfüllungsansicht angezeigt.
- **Abholen** – Durch die Abholungsaktivität werden die Positionen der Buchungsansicht für die Abholung hinzugefügt. Wenn es andere Positionen im Auftrag gibt, die aktuell nicht abgeholt werden, werden sie der Buchungsansicht mit der Menge null hinzugefügt. Nachdem eine Position vollständig abgeholt wurde, wird sie nicht mehr in der Auftragserfüllungsansicht angezeigt.

### <a name="order-fulfillment-filtering"></a>Auftragserfüllungsfilterung

Auftragserfüllung in der Verkaufsstelle umfasst Filterung, sodass der Benutzer das Gesuchte leichter finden kann. Filter können im Aktivitätsbereich unten im Bildschirm **Verkaufsstelle** geändert werden. Standardmäßig wird ein Filter **Liefertyp** angewendet, basierend darauf, wie der Arbeitsgang eingerichtet ist. Wenn der Arbeitsgang mit dem Parameter **Alle Aufträge** eingerichtet wird, dann wird dieser Filter angewendet, wenn auf die Auftragserfüllung zugegriffen wird. Gleiches gilt für die Parameter **Filialabholung** und **Versand ab Filiale**. Andere Filter, die auf die Auftragserfüllungsansicht angewendet werden können, sind unter anderem:

- Kundennummer
- Kundenname
- Debitoren-E-Mail
- Auftragsnummer
- Lieferart
- Eingangsnummer
- Kanalreferenzkennung
- Ursprüngliche Shopnummer
- Positionsstatus
- Erstellungsdatum
- Lieferdatum
- Wareneingangsdatum
