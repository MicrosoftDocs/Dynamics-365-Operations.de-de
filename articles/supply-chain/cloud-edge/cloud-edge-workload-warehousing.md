---
title: Arbeitsauslastungen der Lagerortverwaltung für Scale-Units in der Cloud und Edge
description: Dieses Thema enthält Informationen über die Funktion, die es Scale-Units ermöglicht, ausgewählte Prozesse aus der Arbeitsauslastung Ihrer Lagerortverwaltung auszuführen.
author: perlynne
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, InventTransferOrders, SalesTable, SysSecRolesEditUsers, SysWorkloadDuplicateRecord
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 0d8b0f5a4878a924943f6f8876575d5247875811
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068108"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Workloads in der Lagerortverwaltung für Cloud- und Edge-Skalierungseinheiten

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Nicht alle Geschäftsfunktionen der Lagerortverwaltung werden vollständig für Lagerorte unterstützt, an denen eine Arbeitsauslastung auf einer Skalierungseinheit ausgeführt wird. Achten Sie darauf, nur die Prozesse zu verwenden, die in diesem Thema ausdrücklich als unterstützt beschrieben werden.

## <a name="warehouse-execution-on-scale-units"></a>Lagerort-Ausführung auf Scale-Units

Workloads in der Lagerortverwaltung ermöglichen Cloud- und Edge-Skalierungseinheiten die Ausführung ausgewählter Prozesse aus den Funktionen für die Lagerortverwaltung.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie mit dem Workload der Lagerverwaltung arbeiten, muss Ihr System wie in diesem Abschnitt beschrieben vorbereitet werden.

### <a name="deploy-a-scale-unit-with-the-warehouse-management-workload"></a>Stellen Sie eine Scale-Unit mit dem Workload der Lagerverwaltung bereit.

Sie müssen über einen Dynamics 365 Supply Chain Management-Hub und eine Scale-Unit verfügen, die mit der Arbeitsauslastung der Lagerortverwaltung bereitgestellt wurde. Weitere Informationen zur Architektur und zum Bereitstellungsprozess finden Sie unter [Skalierungseinheiten in einer verteilten Hybridtopologie](cloud-edge-landing-page.md).

### <a name="turn-on-required-features-in-feature-management"></a>Aktivieren Sie erforderliche Funktionen in der Funktionsverwaltung

Verwenden Sie den Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), um die beiden folgenden Funktionen zu aktivieren. (Beide Funktionen sind unter dem Modul *Lagerverwaltung* aufgeführt.)

- Einlagerungsarbeit von ASNs entkoppeln
- (Vorschauversion) Unterstützung von Skalierungseinheiten bei ein- und ausgehenden Lagerortaufträgen

## <a name="how-the-warehouse-execution-workload-works-on-scale-units"></a>Funktionsweise der Workload für die Lagerausführung auf Skalierungseinheiten

Für die Prozesse in der Arbeitsauslastung der Lagerortverwaltung werden die Daten zwischen dem Hub und den Scale-Units synchronisiert.

Eine Scale-Unit kann nur die Daten verwalten, deren Eigentümer sie ist. Das Dateneigentumskonzept für Scale-Units hilft, Multi-Master-Konflikte zu vermeiden. Daher ist es wichtig, dass Sie verstehen, welche Prozessdaten zum Hub gehören und welche zu den Skalierungseinheiten.

Abhängig von den Geschäftsprozessen kann derselbe Datensatz die Besitzverhältnisse zwischen Hub und Skalierungseinheiten ändern. Ein Beispiel für dieses Szenario finden Sie im folgenden Abschnitt.

> [!IMPORTANT]
> Einige Daten können sowohl auf dem Hub als auch auf der Skalierungseinheit erstellt werden. Beispiele sind **Kennzeichen** und **Chargennummern**. Eine dedizierte Konfliktbehandlung wird für den Fall bereitgestellt, dass derselbe eindeutige Datensatz während desselben Synchronisierungszyklus sowohl auf dem Hub als auch auf einer Skalierungseinheit erstellt wird. In diesem Fall schlägt die nächste Synchronisierung fehl und Sie müssen zu **Systemadministration > Anfragen > Workload-Anfragen > Doppelte Datensätze** gehen, wo Sie die Daten anzeigen und zusammenführen können.

## <a name="outbound-process-flow"></a>Ausgehender Prozessablauf

Stellen Sie vor der Bereitstellung eines Warehouse Management-Workloads auf einer Cloud- oder Edge-Skalierungseinheit sicher, dass Sie die Funktion *Unterstützung der Skalierungseinheit für die Freigabe ausgehender Aufträge für den Lagerort* auf Ihrem Enterprise-Hub aktiviert haben. Administratoren können mit den Einstellungen in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie gegebenenfalls aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Module:** *Lagerortverwaltung*
- **Funktionsname:** *Unterstützung der Skalierungseinheit für die Freigabe ausgehender Aufträge für den Lagerort*

Der Prozess des ausgehenden Datenbesitzes hängt davon ab, ob Sie den Ladeplanungsprozess verwenden. In allen Fällen ist der Hub Besitzer der *Quelldokumente*, wie etwa von Aufträgen und Umlagerungsaufträgen, sowie des Auftragszuordnungsprozesses und der zugehörigen Auftragstransaktionsdaten. Wenn Sie jedoch den Ladungsplanungsprozess verwenden, werden die Ladungen auf dem Hub erstellt und befinden sich daher zunächst im Besitz des Hub. Im Rahmen des Prozesses *Für Lagerort freigeben* wird der Besitz der Ladungsdaten an die dedizierte Bereitstellung von Skalierungseinheiten übertragen, die dadurch Besitzer der nachfolgenden *Versandwellenverarbeitung* wird (wie z. B. Arbeitszuweisung, Wiederbeschaffungsarbeiten und Bedarfserstellung). Daher können Lagerortarbeitskräfte ausgehende Verkaufs- und Umlagerungsaufträge nur mithilfe einer mobilen Warehouse Management-App verarbeiten, die mit der Bereitstellung verbunden ist, die die spezifische Workload der Skalierungseinheit ausführt.

Sobald der letzte Arbeitsprozess den Bestand an einem endgültigen Lagerplatz (Frachttür) ablegt, signalisiert die Skalierungseinheit dem Hub, die Bestandstransaktionen im Quelldokument auf *Kommissioniert* zu aktualisieren. Bis dieser Prozess ausgeführt und zurücksynchronisiert wird, wird der Lagerbestand der Scale-Unit Workload physisch auf Lagerort-Ebene reserviert und Sie können die Bestätigung für eine ausgehende Lieferung sofort verarbeiten, ohne auf den Abschluss dieser Synchronisierung warten zu müssen. Der nachfolgende Lieferschein und die Rechnungsstellung oder die Lieferung von Umlagerungsaufträgen für die Ladung werden im Hub abgewickelt.

Das folgende Diagramm zeigt den ausgehenden Fluss und zeigt an, wo die einzelnen Geschäftsprozesse stattfinden. (Wählen Sie das Diagramm aus, um es zu vergrößern.)

[![Ausgehende-Verarbeitung-Flow.](media/wes_outbound_warehouse_processes-small.png "Ausgehender Verarbeitungsflow")](media/wes_outbound_warehouse_processes.png)

### <a name="outbound-processing-with-load-planning"></a>Ausgehende Verarbeitung mit Ladungsplanung

Wenn Sie den Ladungsplanungsprozess verwenden, werden Ladungen und Lieferungen auf dem Hub erstellt und der Datenbesitz wird im Rahmen des Prozesses *Für Lagerort freigeben* auf die Skalierungseinheiten übertragen, wie in der folgenden Abbildung dargestellt.

![Ausgehende Verarbeitung mit Ladungsplanung.](./media/wes_outbound_processing_with_load_planning.png "Ausgehende Verarbeitung mit Ladungsplanung")

### <a name="outbound-processing-without-load-planning"></a>Ausgehende Verarbeitung ohne Ladungsplanung

Wenn Sie den Ladungsplanungsprozess nicht verwenden, werden Lieferungen auf den Skalierungseinheiten erstellt. Im Rahmen des Wellenprozesses werden auch Ladungen auf den Skalierungseinheiten erstellt.

![Ausgehende Verarbeitung ohne Ladungsplanung.](./media/wes_outbound_processing_without_load_planning.png "Ausgehende Verarbeitung ohne Ladungsplanung")

## <a name="inbound-process-flow"></a>Eingehender Prozessflow

Der Hub besitzt die folgenden Daten:

- Alle Quelldokumente, wie z. B. Bestellungen und Produktionsaufträge
- Eingehende Ladungsverarbeitung
- Alle Kosten- und finanziellen Aktualisierungen

> [!NOTE]
> Der Flow der eingehenden Einkaufsbestellung unterscheidet sich konzeptionell vom ausgehenden Flow. Sie können denselben Lagerort entweder auf der Skalierungseinheit oder auf dem Hub betreiben, je nachdem, ob die Bestellung für den Lagerort freigegeben wurde oder nicht. Nachdem Sie eine Bestellung für den Lagerort freigegeben haben, können Sie mit dieser Bestellung nur arbeiten, wenn Sie an der Skalierungseinheit angemeldet sind.
>
> Wenn Sie den Prozess *Freigabe an Lagerort* verwenden, werden [*Lagerort-Bestellungen*](cloud-edge-warehouse-order.md) erstellt, und die Eigentümerschaft des zugehörigen Empfangsflusses wird der Scale-Unit zugewiesen. Der Hub ist nicht in der Lage, eingehenden Empfang zu registrieren.

Sie müssen sich am Hub anmelden, um den Prozess *Freigeben an Lagerort* zu verwenden. Zur Verarbeitung von Bestellungen gehen Sie zu einer der folgenden Seiten, um sie auszuführen oder zu planen:

- **Beschaffung und Bezugsquellenfindung > Bestellungen > Alle Bestellungen > Lagerort > Aktionen > Freigabe an Lagerort**
- **Lagerortverwaltung > Freigabe an Lagerort > Automatische Freigabe von Einkaufsbestellungen**

Wenn Sie **Automatische Freigabe von Bestellungen** verwenden, können Sie bestimmte Zeilen der Einkaufsbestellung anhand einer Abfrage auswählen. Ein typisches Szenario wäre, einen wiederkehrenden Batch-Job festzulegen, der alle bestätigten Zeilen der Einkaufsbestellung freigibt, die voraussichtlich am nächsten Tag eintreffen.

Die Arbeitskraft kann den Empfangsprozess über eine Warehouse Management Mobile App ausführen, die mit der Skalierungseinheit verbunden ist. Die Daten werden dann von der Scale-Unit aufgezeichnet und gegen den eingehenden Lagerauftrag gemeldet. Die Erstellung und Verarbeitung der nachfolgenden Einlagerung wird ebenfalls von der Scale-Unit übernommen.

Wenn Sie nicht den Prozess *Freigabe an Lager* und damit auch nicht *Lageraufträge* verwenden, kann der Hub den Lagereingang und die Arbeitsaufträge unabhängig von Scale-Units verarbeiten.

![Eingangs-Prozess-Flow.](./media/wes-inbound-ga.png "Eingehender Prozessflow")

Wenn eine Arbeitskraft die Eingangsregistrierung mit einem Wareneingangsprozess der mobilen Warehouse Management-App für die Skalierungseinheit durchführt, wird ein Zugang für den zugehörigen Lagerortauftrag erfasst, der in der Skalierungseinheit gespeichert ist. Die Workload der Skalierungseinheit signalisiert daraufhin dem Hub, die zugehörigen Positionstransaktionen der Bestellung auf *Erfasst* zu aktualisieren. Sobald dies abgeschlossen ist, können Sie auf dem Hub eine Einkaufsbestellung Wareneingang ausführen.

Das folgende Diagramm zeigt den eingehenden Fluss und zeigt an, wo die einzelnen Geschäftsprozesse stattfinden. (Wählen Sie das Diagramm aus, um es zu vergrößern.)

[![Eingehender Verarbeitungs-Flow](media/wes_inbound_warehouse_processes-small.png "Eingehender Verarbeitungs-Flow")](media/wes_inbound_warehouse_processes.png)

## <a name="production-control"></a>Produktionssteuerung

Der Workload Lagerverwaltung unterstützt die folgenden drei Flows für die Produktion in der Warehouse Management App:

- Fertig melden und einlagern
- Produktionsauftrag starten
- Materialverbrauch registrieren

### <a name="report-as-finished-and-put-away"></a>Fertig melden und einlagern

Arbeitskräfte können den Flow **Erledigt melden und einlagern** in der Warehouse Management App verwenden, um einen Produktions- oder Batch-Auftrag als erledigt zu melden. Sie können auch Kuppelprodukte und Nebenprodukte auf einem Batch-Auftrag als erledigt melden. Wenn ein Auftrag als abgeschlossen gemeldet wird, erzeugt das System in der Regel Einlagerungs-Lagerortarbeit auf der Scale-Einheit. Wenn Sie keine Einlagerungen benötigen, können Sie in Ihren Richtlinien festlegen, dass diese Funktion weggelassen wird.

### <a name="start-production-order"></a>Produktionsauftrag starten

Arbeitskräfte können den Flow **Produktionsauftrag starten** in der App Warehouse Management verwenden, um den Beginn eines Produktions- oder Batch-Auftrags zu registrieren.

### <a name="register-material-consumption"></a>Materialverbrauch registrieren

Arbeitskräfte können den Flow **Materialverbrauch registrieren** in der App Warehouse Management verwenden, um den Materialverbrauch für einen Produktions- oder Batch-Auftrag zu melden. Für das gemeldete Material auf dem Produktions- oder Batch-Auftrag auf der Scale-Einheit wird dann ein Erfassungsjournal für die Kommissionierung erstellt. Die Buchungsblattzeilen nehmen eine physische Reservierung für den verbrauchten Bestand vor. Wenn Daten zwischen der Scale-Unit und dem Hub synchronisiert werden, wird eine Erfassung der Kommissionierliste erstellt und auf der Hub-Instanz veröffentlicht.

## <a name="supported-processes-and-roles"></a>Unterstützte Prozesse und Rollen

Nicht alle Prozesse der Lagerortverwaltung werden in einer Workload für die Lagerausführung auf einer Skalierungseinheit unterstützt. Daher empfehlen wir, dass Sie Rollen zuweisen, die zu der Funktionalität passen, die jedem Benutzer zur Verfügung steht.

Um diesen Prozess zu erleichtern, ist eine Beispielrolle mit dem Namen *Lagerortverwaltung auf Arbeitsauslastung* in den Demodaten unter **Systemadministration \> Sicherheit \> Sicherheitskonfiguration** enthalten. Der Zweck dieser Rolle ist es, Lagerortverwaltern den Zugriff auf die Workload für die Lagerausführung auf der Skalierungseinheit zu ermöglichen. Die Rolle gewährt Zugriff auf die Seiten, die im Zusammenhang mit einer Arbeitsauslastung, die auf einer Scale-Unit gehostet wird, relevant sind.

Benutzerrollen auf einer Scale-Unit werden als Teil der anfänglichen Datensynchronisation vom Hub zur Scale-Unit zugewiesen.

Um die Rollen zu ändern, die einem Benutzer zugewiesen sind, gehen Sie zu **Systemadministration \> Sicherheit \> Benutzer zu Rollen zuweisen** auf der Skalierungseinheit. Benutzern, die als Lagerortverwaltung nur auf Scale-Units agieren, sollte nur die Rolle *Lagerort-Manager auf Arbeitsauslastung* zugewiesen werden. Auf diese Weise wird sichergestellt, dass diese Benutzer nur Zugriff auf die unterstützte Funktionalität haben. Entfernen Sie alle anderen Rollen, die diesen Benutzern zugewiesen sind.

Benutzern, die als Lagerortverwalter sowohl auf dem Hub als auch auf der Scale-Unit agieren, sollte die bestehende Rolle *Lagerort-Arbeiter* zugewiesen werden. Beachten Sie, dass diese Rolle den Lagerkräften Zugriff auf Funktionen (z. B. Umlagerungsauftragseingang) gewährt, die in der Benutzeroberfläche (UI) erscheinen, aber derzeit nicht auf Skalierungseinheiten unterstützt werden.

### <a name="supported-warehouse-execution-processes"></a>Unterstützte Lagerausführungsprozesse

Die folgenden Lagerausführungsprozesse können für eine Workload für die Lagerausführung auf einer Skalierungseinheit aktiviert werden:

- Ausgewählte Wellenmethoden für Verkaufs- und Umlagerungsaufträge (Prüfung, Ladungserstellung, Zuteilung, Wiederbeschaffung, Containerisierung, Arbeitserstellung und Wellenbeschriftungsdruck)

- Bearbeitung von Lagerarbeiten für Verkaufs- und Umlagerungsaufträge mithilfe der Lagerort-App (einschließlich Wiederbeschaffungsarbeiten)
- Abfrage von Lagerort-Beständen mit der Lagerort App
- Erstellen und Ausführen von Bestandsbewegungen mit Hilfe der Lagerort App
- Erstellen und Verarbeiten von Zyklenzählarbeiten mit der Lagerort-App
- Bestandsanpassungen über die Lagerort App vornehmen
- Registrieren von Einkaufsbestellungen und Ausführen von Einlagerungsarbeiten mit der Lagerort App

Folgende Arbeitsarten können auf einer Skalierungseinheit erstellt und somit im Rahmen einer Workload für die Lagerortverwaltung verarbeitet werden:

- **Bestandsbewegungen** – manuelle Bewegung und Bewegung über eine Arbeitsvorlage.
- **Zykluszählung** – Einschließlich einer Abweichung beim Genehmigungs-/Ablehnungsprozess als Teil von Zählvorgängen.
- **Bestellungen** – Einlagerungsarbeiten über einen Lagerortauftrag, wenn Bestellungen nicht mit Ladungen verbunden sind.
- **Aufträge** – einfache Kommissionier- und Verladearbeiten.
- **Übertragungsbeleg** - Über die Verarbeitung des Ladungsträgers.
- **Übertragungsproblem** – einfache Kommissionier- und Verladearbeiten.
- **Wiederbeschaffung** – Ohne Rohmaterial für die Produktion.
- **Einlagerung von Fertigerzeugnissen** – Nach der Meldung eines Produktionsauftrags als abgeschlossen.
- **Einlagerung von Co- und Nebenprodukten** – Nach der Meldung eines Produktionsauftrags als abgeschlossen.
<!-- - **Packed container picking** - After manual packing station processing. -->

Andere Arten der Verarbeitung von Quellbelegen oder Lagerortarbeit werden derzeit in Scale-Units nicht unterstützt. Wenn Sie z.B. einen Workload zur Lagerausführung auf einer Scale-Unit ausführen, können Sie den Prozess zum Empfang von Verkaufsaufträgen nicht verwenden, um Rücklieferungen zu verarbeiten. Stattdessen muss diese Verarbeitung von der Hub-Instanz vorgenommen werden.

> [!NOTE]
> Menüelemente und Schaltflächen für mobile Geräte für nicht unterstützte Funktionen werden in der _Warehouse Management Mobile App_ nicht angezeigt, wenn sie mit einer Skalierungseinheitsbereitstellung verbunden ist.
>
> Es sind ein paar zusätzliche Schritte erforderlich, um die Warehouse Management Mobile-App für den Einsatz mit einer Cloud- oder Edge-Scale-Unit festzulegen. Weitere Informationen finden Sie unter [Konfigurieren Sie die Warehouse Management Mobile-App für Scale-Units in der Cloud und am Rand](cloud-edge-workload-setup-warehouse-app.md).
>
> Wenn Sie eine Arbeitsauslastung auf einer Skalierungseinheit ausführen, können Sie keine nicht unterstützten Prozesse für das spezifische Lager auf dem Hub ausführen. Die später in diesem Thema bereitgestellten Tabellen dokumentieren die unterstützten Funktionen.
>
> Ausgewählte Lagerort-Arbeitstypen können sowohl auf dem Hub als auch auf Skalierungseinheiten erstellt werden, können jedoch nur vom besitzenden Hub oder der besitzenden Skalierungseinheit (der Bereitstellung, die die Daten erstellt hat) verwaltet werden.
>
> Beachten Sie auch dann, wenn ein bestimmter Prozess von einer Skalierungseinheit unterstützt wird, dass möglicherweise nicht alle erforderlichen Daten vom Hub zur Skalierungseinheit oder von der Skalierungseinheit zum Hub synchronisiert werden, was zu einer unerwarteten Systemverarbeitung führen kann. Beispiele für dieses Szenario:
>
> - Wenn Sie eine Abfrage der Lagerplatzrichtlinie, die einen Datentabellendatensatz verknüpft, der nur bei der Hubbereitstellung vorhanden ist.
> - Wenn Sie Standortstatus- und/oder Standortvolumenlastfunktionen verwenden. Diese Daten werden zwischen den Bereitstellungen nicht synchronisiert und funktionieren daher nur, wenn das vorhandene Standortinventar für eine der Bereitstellungen aktualisiert wird.

Die folgenden Funktionen der Lagerortverwaltung werden derzeit für Arbeitsauslastungen auf Skalierungseinheiten nicht unterstützt:

- Eingangsverarbeitung von Bestellpositionen, die einer Ladung zugeordnet sind.
- Eingangsverarbeitung von Bestellungen für ein Projekt.
- Verwaltung der Gesamttransportkosten, Nutzung von Fahrten und Verfolgung von Waren während des Transports
- Eingangs- und Ausgangsbearbeitung für Elemente mit den aktiven Rückverfolgungsangaben **Besitzer** und/oder **Seriennummer**.
- Verarbeitung von Beständen, die einen Sperrstatuswert haben.
- Ändern eines Bestandsstatus während eines Arbeitsbewegungsprozesses.
- Auftragsgebundene, flexible Dimensionsreservierungen auf Lagerortebene.
- Verwendung der Funktion *Status des Lagerplatzes an einem Lagerort* (die Daten werden nicht zwischen den Bereitstellungen synchronisiert).
- Verwendung der Funktion *Positionierung von Lagerplatzkennzeichen*.
- Verwendung von *Produktfilter* und *Produktfiltergruppen*, einschließlich der Einstellung **Anzahl der Tage zum Mischen von Chargen**.
- Integration mit dem Qualitätsmanagement.
- Verarbeitung mit Artikelgewichten.
- Verarbeitung mit Artikeln, die nur für die Transportverwaltung (TMS) aktiviert sind.
- Verarbeitung mit negativem Bestand.
- Unternehmensübergreifende Datenfreigabe für Produkte. <!-- Planned -->
- Lagerort-Arbeitsverarbeitung mit Versandschein.
- Lagerort-Arbeitsverarbeitung mit Materialhandhabung/Lagerortautomatisierung.
- Produktmasterdaten-Images (z. B. in der mobilen Warehouse Management-App).

> [!WARNING]
> Einige Lagerortfunktionen sind für Lageorte, in denen die Arbeitsauslastungen für die Lagerortverwaltung auf einer Skalierungseinheit ausgeführt werden, nicht verfügbar und werden auch auf dem Hub oder der Arbeitsauslastung der Skalierungseinheit nicht unterstützt.
>
> Andere Funktionen können auf beiden Seiten verarbeitet werden, erfordern jedoch in einigen Szenarien eine sorgfältige Verwendung, z. B. wenn der Lagerbestand aufgrund des asynchronen Datenaktualisierungsprozesses für denselben Lager sowohl auf dem Hub als auch auf der Skalierungseinheit aktualisiert wird.
>
> Spezifische Funktionen (wie z. B. *Arbeit sperren*), die sowohl auf dem Hub als auch auf den Skalierungseinheiten unterstützt werden, werden nur für den Besitzer der Daten unterstützt.

### <a name="outbound-supported-only-for-sales-and-transfer-orders"></a>Outbound (wird nur für Verkaufsaufträge und Umlagerungsaufträge unterstützt)

Die folgende Tabelle zeigt, welche Funktionen im Outbound unterstützt werden und wo sie unterstützt werden, wenn die Arbeitsauslastungen der Lagerortverwaltung in Scale-Units und Edge-Einheiten verwendet werden.

| Bearbeiten                                                      | Hub | Workload für die Lagerausführung auf einer Skalierungseinheit |
|--------------------------------------------------------------|-----|------------------------------|
| Quellbeleg-Verarbeitung                                   | Ja | Nein |
| Last- und Transportverwaltungs-Verarbeitung                | Ja, aber nur die Ladungsplanungsprozesse. Verarbeitung der Transportverwaltung wird nicht unterstützt  | Nein |
| Für Lagerort freigeben                                         | Ja | Nein |
| Geplantes Crossdocking                                        | Nein  | Nein |
| Lieferungskonsolidierung                                       | Ja, bei Verwendung der Ladungsplanung | Ja |
| Verarbeitung von Sendungswellen                                     | Nein  |Ja, außer **Ladungserstellung und -sortierung** |
| Lieferungen für Welle verwalten                                  | Nein  | Ja|
| Lagerort-Arbeitsverarbeitung (inkl. Ladungsträger-Druck)        | Nein  | Ja, aber nur für die zuvor genannten, unterstützten Funktionen |
| Clusterkommissionierung                                              | Nein  | Ja|
| Manuelle Verpackungsverarbeitung, inkl. Arbeitsverarbeitung „Entnahme aus gepacktem Container“ | Nein <P>Einige Verarbeitungen können nach einem anfänglichen, von einer Scale-Unit kommissionierten Vorgang durchgeführt werden, sind aber aufgrund der folgenden blockierten Vorgänge nicht zu empfehlen.</p>  | Nein |
| Container aus Gruppe entfernen                                  | Nein  | Nein |
| Ausgehende Sortierverarbeitung                                  | Nein  | Nein |
| Drucken von ladungsbezogenen Dokumenten                           | Ja | Ja|
| Konnossement- und ASN-Generierung                            | Nein  | Ja|
| Versandbestätigung                                             | Nein  | Ja|
| Versandbestätigung mit „Bestätigen und übertragen“            | Nein  | Ja|
| Lieferschein- und Rechnungsverarbeitung                        | Ja | Nein |
| Kurzkommissionierung (Verkaufs- und Umlagerungsaufträge)                    | Nein  | Ja, ohne Reservierungen für Quelldokumente zu entfernen|
| Zu hohe Entnahme (Verkaufs- und Umlagerungsaufträge)                     | Nein  | Ja|
| Kennzeichen konsolidieren                                   | Nein  | Ja|
| Änderung von Arbeitsplätzen (Verkaufs- und Umlagerungsaufträge)         | Nein  | Ja|
| Arbeit abschließen (Verkaufs- und Umlagerungsaufträge)                    | Nein  | Ja|
| Arbeitsbericht drucken                                            | Ja | Ja|
| Serienetikett                                                   | Nein  | Ja|
| Arbeitsaufteilung                                                   | Nein  | Ja|
| Arbeitsverarbeitung – Geleitet von „Transportladung“            | Nein  | Nein |
| Entnommene Menge reduzieren                                       | Nein  | Ja|
| Arbeit stornieren                                                 | Nein  | Ja|
| Lieferungsbestätigung umkehren                                | Nein  | Ja|
| Antrag auf Stornierung von Lager-Bestellzeilen                      | Ja | Nein, aber die Anfrage wird genehmigt oder abgelehnt |
| <p>Umlagerungsaufträge für Wareneingang freigeben</p><p>Dieser Prozess wird automatisch im Rahmen des Versands von Umlagerungsaufträgen durchgeführt. Sie kann jedoch manuell verwendet werden, um den Empfang von Ladungsträgern in einer Scale-Unit zu aktivieren, wenn eingehende Lagerbestellungszeilen storniert wurden oder als Teil eines neuen Workload-Bereitstellungsprozesses.</p> | Ja | Nein|

### <a name="inbound"></a>Zugang

Die folgende Tabelle zeigt, welche Funktionen im Eingang unterstützt werden und wo sie unterstützt werden, wenn die Arbeitsauslastungen der Lagerortverwaltung in Scale-Units und Edge-Units verwendet werden.

| Bearbeiten                                                          | Hub | Workload für die Lagerausführung auf einer Skalierungseinheit<BR>*(Mit „Ja“ gekennzeichnete Artikel gelten nur für Lagerortaufträge.)* |
|------------------------------------------------------------------|-----|----------------------------------------------------------------------------------|
| Quelle&nbsp;Dokument&nbsp;Verarbeitung                             | Ja | Nein |
| Last- und Transportverwaltungs-Verarbeitung                    | Ja | Nein |
| Gesamttransportkosten und Waren in Zustellung                       | Ja | Nein |
| Bestätigung eingehender Lieferungen                                    | Ja | Nein |
| Freigabe der Einkaufsbestellung an den Lagerort (Lagerbestandsverarbeitung) | Ja | Nein |
| Antrag auf Stornierung von Lager-Bestellzeilen                            | Ja | Nein, aber die Anfrage wird genehmigt oder abgelehnt |
| Verarbeitung des Produktzugangs aus dem Quellbeleg der Bestellung                        | Ja | Nein |
| Bestellungsartikel – Empfang und Einlagerung                       | <p>Ja,&nbsp;wenn&nbsp;kein Lagerort vorhanden ist&nbsp;keine Lagerbestellung</p><p>Nein, wenn eine Lagerort-Bestellung vorhanden ist</p> | <p>Ja, wenn eine Bestellung nicht Teil einer <i>Ladung</i> ist</p> |
| Bestellposition – Empfang und Einlagerung                       | <p>Ja, wenn kein Lagerort vorhanden ist</p><p>Nein, wenn eine Lagerort-Bestellung vorhanden ist</p> | <p>Ja, wenn eine Bestellung nicht Teil einer <i>Ladung</i> ist</p></p> |
| Rücklieferungsempfang und -einlagerung                              | Ja | Nein |
| Empfang und Einlagerung gemischter Ladungsträger                       | <p>Ja, wenn kein Lagerort vorhanden ist</p><p>Nein, wenn eine Lagerort-Bestellung vorhanden ist</p> | Ja |
| Artikelempfang aus Ladung                                              | <p>Ja, wenn kein Lagerort vorhanden ist</p><p>Nein, wenn eine Lagerort-Bestellung vorhanden ist</p> | Nein |
| Bestellung Ladungsträger erhalten und einlagern              | <p>Ja, wenn kein Lagerort vorhanden ist</p><p>Nein, wenn eine Lagerort-Bestellung vorhanden ist</p> | Nein |
| Umlagerungsauftrag Ladungsträger empfangen und einlagern             | Nein | Ja |
| Artikelempfang und -einlagerung für Umlagerungsauftrag                       | Ja | Nein |
| Umlagerungsauftragsposition – Empfang und Einlagerung                       | Ja | Nein |
| Bestelleingang mit Unterlieferung                      | <p>Ja, wenn kein Lagerort vorhanden ist</p><p>Nein, wenn eine Lagerort-Bestellung vorhanden ist</p> | Ja, aber nur, wenn Sie eine Stornoanforderung vom Hub aus stellen |
| Bestelleingang mit Überlieferung                       | <p>Ja, wenn kein Lagerort vorhanden ist</p><p>Nein, wenn eine Lagerort-Bestellung vorhanden ist</p> | Ja  |
| Eingang mit Erstellung von *Cross-Docking*-Arbeit                 | <p>Ja, wenn kein Lagerort vorhanden ist</p><p>Nein, wenn eine Lagerort-Bestellung vorhanden ist</p> | Nein |
| Eingang mit Erstellung von *Qualitätsprüfungsauftrags*-Arbeit                  | <p>Ja, wenn kein Lagerort vorhanden ist</p><p>Nein, wenn eine Lagerort-Bestellung vorhanden ist</p> | Nein |
| Eingang mit Erstellung von *Qualitätsartikelmuster*-Arbeit          | <p>Ja, wenn kein Lagerort vorhanden ist</p><p>Nein, wenn eine Lagerort-Bestellung vorhanden ist</p> | Nein |
| Eingang mit Erstellung von *Qualität in der Qualitätsprüfung*-Arbeit       | <p>Ja, wenn kein Lagerort vorhanden ist</p><p>Nein, wenn eine Lagerort-Bestellung vorhanden ist</p> | Nein |
| Eingang mit Erstellung von Qualitätsprüfungsauftrag                            | <p>Ja, wenn kein Lagerort vorhanden ist</p><p>Nein, wenn eine Lagerort-Bestellung vorhanden ist</p> | Nein |
| Arbeitsverarbeitung – Geleitet von *Clustereinlagerung*                 | Ja | Nein |
| Arbeitsverarbeitung mit *kurzer Entnahme*                               | Ja | Nein |
| Arbeit stornieren (eingehend)                                            | <p>Ja, wenn kein Lagerort vorhanden ist</p><p>Nein, wenn eine Lagerort-Bestellung vorhanden ist</p> | <p>Ja, aber nur, wenn die Option <b>Bon bei Stornierung der Arbeit nicht registrieren</b> auf der Seite <b>Parameter der Lagerverwaltung</b> deaktiviert ist.</p> |
| Ladungsträgerladung                                           | Ja | Ja |

### <a name="warehouse-operations-and-exception-handing"></a>Lagerort-Operationen und Ausnahme-Handling

Die folgende Tabelle zeigt, welche Funktionen für Lagerort-Operationen und Exception Handing unterstützt werden und wo sie unterstützt werden, wenn die Arbeitsauslastungen der Lagerortverwaltung in Scale-Units und Edge-Units verwendet werden.

| Bearbeiten                                            | Hub | Workload für die Lagerausführung auf einer Skalierungseinheit |
|----------------------------------------------------|-----|------------------------------|
| Ladungsträger abfragen                              | Ja | Ja                          |
| Element abfragen                                       | Ja | Ja                          |
| Lagerplatz abfragen                                   | Ja | Ja                          |
| Lagerort ändern                                   | Ja | Ja                          |
| Bewegung                                           | Ja | Ja                          |
| Bewegung durch Vorlage                               | Ja | Ja                          |
| Lagerortumlagerung                                 | Ja | Nein                           |
| Umlagerungsauftrag aus der Lagerort-App erstellen           | Ja | Nein                           |
| Abgleich (rein/raus)                                | Ja | Ja, aber nicht für das Regulierungsszenario, bei dem Bestandsreservierungen über die Einstellung **Reservierungen entfernen** auf den Bestandsregulierungsarten entfernt werden müssen</p>                           |
| Bestandsstatusänderung                            | Ja | Nein                           |
| Zykluszählung und Zähldiskrepanzverarbeitung | Ja | Ja                           |
| Label neu drucken (Ladungsträgerdruck)             | Ja | Ja                          |
| Ladungsträgererstellung                                | Ja | Nein                           |
| Ladungsträgerauflösung                                | Ja | Nein                           |
| Für geschachtelte Ladungsträger verpacken                      | Ja | Nein                           |
| Einchecken durch Fahrer                                    | Ja | Nein                           |
| Auschecken durch Fahrer                                   | Ja | Nein                           |
| Chargendisposition-Code ändern                      | Ja | Ja                          |
| Offene Arbeitsliste anzeigen                             | Ja | Ja                          |
| Nachschubverarbeitung mit Min/Max und Schwellenwert für Zonenwiederbeschaffung| Ja <p>Es wird empfohlen, nicht dieselben Standorte in die Abfragen aufzunehmen.</p>| Ja                          |
| Zuteilung von Zeitfenstern-Wiederbeschaffung                  | Ja  | Ja<p>Beachten Sie, dass die Einrichtung an der Skalierungseinheit erfolgen muss.</p>                           |
| Arbeit sperren und entsperren                             | Ja | Ja                          |
| Benutzer ändern                                        | Ja | Ja                          |
| Arbeitspool für Arbeit ändern                           | Ja | Ja                          |
| Arbeit stornieren                                        | Ja | Ja                          |

### <a name="production"></a>Produktion

Die folgende Tabelle fasst zusammen, welche Produktionsszenarien der Lagerortverwaltung derzeit für Arbeitsauslastungen auf Skalierungseinheiten unterstützt werden.

| Bearbeiten | Hub | Workload für die Lagerausführung auf einer Skalierungseinheit |
|---------|-----|----------------------------------------------|
| Verarbeitung von Belegen aus Produktionsaufträgen    | Ja | Nein |
| Für Lagerort freigeben                           | Ja | Nein |
| Produktionsauftrag starten                         | Ja | Ja|
| Erstellen von Lagerbestellungen                        | Ja | Nein |
| Antrag auf Stornierung von Lager-Bestellzeilen        | Ja | Nein, aber die Anfrage wird genehmigt oder abgelehnt |
| Fertig melden und Fertigerzeugnisse einlagern | <p>Ja, wenn kein Lagerort vorhanden ist</p><p>Nein, wenn eine Lagerort-Bestellung vorhanden ist</p> | Ja|
| Einlagerung von Co- und Nebenprodukten             | <p>Ja, wenn kein Lagerort vorhanden ist</p><p>Nein, wenn eine Lagerort-Bestellung vorhanden ist</p> | Ja|
| Materialverbrauch registrieren                  | Ja | Ja|
| Verarbeitung von Produktionswellen                     | Ja | Nein |
| Rohmaterialentnahme                           | Ja | Nein |
| Kanban-Einlagerung                                | Ja | Nein |
| Kanban-Entnahme                                 | Ja | Nein |
| Kanban leeren                                   | Ja | Nein |
| Produktionsausschuss                               | Ja | Nein |
| Letzte Palette der Produktion                         | Ja | Nein |
| Rohmaterialwiederbeschaffung                     | Nein  | Nein |

## <a name="maintaining-scale-units-for-warehouse-execution"></a>Pflege von Skalierungseinheiten für die Lagerortausführung

Sowohl auf der Hub- als auch auf der Scale-Unit laufen mehrere Batch-Jobs.

Beim Bereitstellen des Hubs können Sie die folgenden Batchaufträge manuell pflegen:

- Verwalten Sie die folgenden Batchaufträge unter **Lagerverwaltung \> Periodische Aufgaben \> Back-Office Workload-Verwaltung**:

    - Hub-Nachrichtenverarbeitung zur Skalierungseinheit
    - Quellauftragszugänge registrieren
    - Lagerortaufträge abschließen

- Verwalten Sie die folgenden Batchaufträge unter **Lagerverwaltung \> Periodische Aufgaben \> Workload-Verwaltung**:

    - Lagerorthub zu Skalierungseinheit-Nachrichtenprozessor
    - Lagerauftragspositionszugänge für Wareneingangsbuchung verarbeiten

Bei der Bereitstellung von Scale-Units können Sie die folgenden Batch-Aufträge unter **Lagerverwaltung \> Periodische Aufgaben \> Workload-Verwaltung** verwalten:

- Zyklustabellendatensätze verarbeiten
- Lagerorthub zu Skalierungseinheit-Nachrichtenprozessor
- Lagerauftragspositionszugänge für Wareneingangsbuchung verarbeiten

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
