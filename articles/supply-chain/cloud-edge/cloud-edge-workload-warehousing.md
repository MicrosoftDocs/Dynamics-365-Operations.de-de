---
title: Arbeitsauslastungen der Lagerortverwaltung für Scale-Units in der Cloud und Edge
description: Dieses Thema enthält Informationen über die Funktion, die es Scale-Units ermöglicht, ausgewählte Prozesse aus der Arbeitsauslastung Ihrer Lagerortverwaltung auszuführen.
author: perlynne
manager: tfeyr
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, SysSecRolesEditUsers
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 91e614889c719ae700b13e54150e5025d64e2b97
ms.sourcegitcommit: 289e9183d908825f4c8dcf85d9affd4119238d0c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104939"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Workloads in der Lagerortverwaltung für Cloud- und Edge-Skalierungseinheiten

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> Nicht alle Geschäftsfunktionen der Lagerortverwaltung werden vollständig für Lagerorte unterstützt, an denen eine Arbeitsauslastung auf einer Skalierungseinheit ausgeführt wird. Achten Sie darauf, nur die Prozesse zu verwenden, die in diesem Thema ausdrücklich als unterstützt beschrieben werden.

## <a name="warehouse-execution-on-scale-units"></a>Lagerort-Ausführung auf Scale-Units

Diese Funktion ermöglicht es Scale-Units, ausgewählte Prozesse aus den Funktionalitäten der Lagerortverwaltung auszuführen. Cloud-Scale-Units führen ihre Arbeitsauslastungen in der Cloud aus, indem sie dedizierte Verarbeitungskapazität in Ihrer ausgewählten Microsoft Azure-Region nutzen. Für Edge-Scale-Units können Sie einige Arbeitsauslastungen unabhängig vor Ort ausführen, auch wenn die Scale-Units vorübergehend von der Cloud getrennt sind.

In diesem Thema werden Lagerortverwaltungs-Ausführungen in einem Lagerort, der als Scale-Unit definiert ist, als *Lagerort Execution System* (*WES*) bezeichnet.

## <a name="prerequisites"></a>Voraussetzungen

Sie müssen über einen Dynamics 365 Supply Chain Management-Hub und eine Scale-Unit verfügen, die mit der Arbeitsauslastung der Lagerortverwaltung bereitgestellt wurde. Weitere Informationen über die Architektur und den Bereitstellungsprozess finden Sie unter [Cloud- und Edge-Scale-Einheiten für Arbeitsauslastungen in der Fertigung und Lagerortverwaltung](cloud-edge-landing-page.md).

## <a name="how-the-wes-workload-works-on-scale-units"></a>Wie die WES-Arbeitsauslastung auf Scale-Units funktioniert

Für die Prozesse in der Arbeitsauslastung der Lagerortverwaltung werden die Daten zwischen dem Hub und den Scale-Units synchronisiert.

Eine Scale-Unit kann nur die Daten verwalten, deren Eigentümer sie ist. Das Dateneigentumskonzept für Scale-Units hilft, Multi-Master-Konflikte zu vermeiden. Daher ist es wichtig, dass Sie verstehen, welche Prozesse dem Hub und welche den Scale-Units gehören.

Die Scale-Units besitzen die folgenden Daten:

- **Wellenverarbeitungsdaten** - Ausgewählte Wellenverarbeitungsmethoden werden als Teil der Wellenverarbeitung der Scale-Unit behandelt.
- **Arbeitsverarbeitungsdaten** - Die folgenden Arten der Arbeitsauftragsverarbeitung werden unterstützt:

  - **Bestandsbewegungen** (manuelle Bewegung und Bewegung über eine Arbeitsvorlage)
  - **Bestellungen** (Einlagerungsarbeiten über einen Lagerortauftrag, wenn Bestellungen nicht mit Ladungen verbunden sind)
  - **Verkaufsaufträge** (einfache Kommissionier- und Verladearbeiten)
  - **Umlagerungsaufträge** (nur ausgehend mit einfachen Kommissionier- und Ladearbeiten)

- **Lagerbestellungs-Eingangsdaten** - Diese Daten werden nur für Einkaufsbestellungen verwendet, die manuell an ein Lagerort freigegeben werden.
- **Ladungsträgerdaten** - Ladungsträger können auf dem Hub und der Scale-Unit erstellt werden. Eine dedizierte Konfliktbehandlung ist vorgesehen. Beachten Sie, dass diese Daten nicht lagerspezifisch sind.

## <a name="outbound-process-flow"></a>Ausgehender Prozessablauf

Der Hub besitzt die folgenden Daten:

- Alle Quelldokumente, wie z. B. Verkaufsaufträge und Transportaufträge
- Auftragszuordnung und Ausgangslastverarbeitung
- Die Prozesse Freigabe an Lagerort, Sendungserstellung und Wellenabschluss

Die Scale-Units besitzen die eigentliche Wellenverarbeitung (z. B. Arbeitszuweisung, Wiederbeschaffung und Bedarfserstellung) nach der Freigabe der Welle. Daher können die Arbeitskräfte im Lagerort ausgehende Arbeit mithilfe einer Lager-App verarbeiten, die mit der Scale-Unit verbunden ist.

![Wellenverarbeitungs-Flow](./media/wes-wave-processing-ga.png "Ablauf der Wellenverarbeitung")

## <a name="inbound-process-flow"></a>Eingehender Prozessflow

Der Hub besitzt die folgenden Daten:

- Alle Quelldokumente, wie Einkaufsbestellungen und Aufträge zur Rücklieferung
- Eingehende Ladungsverarbeitung
- Alle Kosten- und finanziellen Aktualisierungen

> [!NOTE]
> Der Flow der eingehenden Einkaufsbestellung unterscheidet sich konzeptionell vom ausgehenden Flow. Sie können denselben Lagerort entweder auf der Skalierungseinheit oder dem Hub betreiben, je nachdem, ob die Bestellung für das Lager freigegeben wurde oder nicht. Sobald Sie eine Bestellung für den Lagerort freigegeben haben, können Sie nur mit dieser Bestellung arbeiten, wenn Sie an der Skalierungseinheit angemeldet sind.

Wenn Sie den Prozess *Freigabe an Lager* verwenden, werden [*Lagerortaufträge*](cloud-edge-warehouse-order.md) erstellt und die Verantwortung für den zugehörigen Eingangsflow wird der Skalierungseinheit zugewiesen. Der Hub ist nicht in der Lage, eingehenden Empfang zu registrieren.

Die Arbeitskraft kann den Empfangsprozess über eine Lagerort-App ausführen, die mit der Scale-Unit verbunden ist. Die Daten werden dann von der Scale-Unit aufgezeichnet und gegen den eingehenden Lagerauftrag gemeldet. Die Erstellung und Verarbeitung der nachfolgenden Einlagerung wird ebenfalls von der Scale-Unit übernommen.

Wenn Sie nicht den Prozess *Freigabe an Lager* und damit auch nicht *Lageraufträge* verwenden, kann der Hub den Lagereingang und die Arbeitsaufträge unabhängig von Scale-Units verarbeiten.

![Eingangs-Prozessablauf](./media/wes-inbound-ga.png "Eingehender Prozessflow")

## <a name="supported-processes-and-roles"></a>Unterstützte Prozesse und Rollen

Nicht alle Prozesse der Lagerortverwaltung werden in einer WES-Arbeitsauslastung auf einer Scale-Unit unterstützt. Daher empfehlen wir, dass Sie Rollen zuweisen, die zu der Funktionalität passen, die jedem Benutzer zur Verfügung steht.

Um diesen Prozess zu erleichtern, ist eine Beispielrolle mit dem Namen *Lagerortverwaltung auf Arbeitsauslastung* in den Demodaten unter **Systemadministration \> Sicherheit \> Sicherheitskonfiguration** enthalten. Der Zweck dieser Rolle ist es, Lagerort-Managern den Zugriff auf das WES auf der Scale-Unit zu ermöglichen. Die Rolle gewährt Zugriff auf die Seiten, die im Zusammenhang mit einer Arbeitsauslastung, die auf einer Scale-Unit gehostet wird, relevant sind.

Benutzerrollen auf einer Scale-Unit werden als Teil der anfänglichen Datensynchronisation vom Hub zur Scale-Unit zugewiesen.

Um die Rollen zu ändern, die einem Benutzer zugewiesen sind, gehen Sie zu **Systemadministration \> Sicherheit \> Benutzer zu Rollen zuweisen** auf der Skalierungseinheit. Benutzern, die als Lagerortverwaltung nur auf Scale-Units agieren, sollte nur die Rolle *Lagerort-Manager auf Arbeitsauslastung* zugewiesen werden. Auf diese Weise wird sichergestellt, dass diese Benutzer nur Zugriff auf die unterstützte Funktionalität haben. Entfernen Sie alle anderen Rollen, die diesen Benutzern zugewiesen sind.

Benutzern, die als Lagerortverwalter sowohl auf dem Hub als auch auf der Scale-Unit agieren, sollte die bestehende Rolle *Lagerort-Arbeiter* zugewiesen werden. Beachten Sie, dass diese Rolle den Lagerkräften Zugriff auf Funktionen (z. B. Umlagerungsauftragseingang) gewährt, die in der Benutzeroberfläche (UI) erscheinen, aber derzeit nicht auf Skalierungseinheiten unterstützt werden.

## <a name="supported-wes-processes"></a>Unterstützte WES-Prozesse

Die folgenden Lagerausführungsprozesse können für eine WES-Arbeitsauslastung auf einer Scale-Unit aktiviert werden:

- Ausgewählte Wellenmethoden für Verkaufs- und Umlagerungsaufträge (Zuteilung, Wiederbeschaffung, Containerisierung, Arbeitserstellung und Wellenbeschriftungsdruck)
- Bearbeitung von Lagerarbeiten für Verkaufs- und Umlagerungsaufträge mithilfe der Lagerort-App (einschließlich Wiederbeschaffungsarbeiten)
- Abfrage von Lagerort-Beständen mit der Lagerort App
- Erstellen und Ausführen von Bestandsbewegungen mit Hilfe der Lagerort App
- Registrieren von Einkaufsbestellungen und Ausführen von Einlagerungsarbeiten mit der Lagerort App

Die folgenden Arbeitsauftragstypen werden derzeit für WES-Arbeitsauslastungen bei Scale-Unit-Bereitstellungen unterstützt:

- Aufträge
- Umlagerungsproblem
- Wiederbeschaffung
- Bestandsumlagerung
- Einkaufsbestellungen (mit Lagerortaufträge verknüpft)

Keine anderen Arten von Quelldokumentverarbeitung oder Lagerortarbeiten wird derzeit auf Skalierungseinheiten unterstützt. Beispielsweise können Sie für eine WES-Arbeitsauslastung auf einer Skalierungseinheit keinen Empfangsvorgang für Umlagerungsaufträge (Umlagerungseingang) oder Prozesszykluszählarbeiten ausführen.

> [!NOTE]
> Menüelemente und Schaltflächen für mobile Geräte für nicht unterstützte Funktionen werden in der _Lagerort-App_ nicht angezeigt, wenn sie mit einer Skalierungseinheitsbereitstellung verbunden ist.

> [!WARNING]
> Wenn Sie eine Arbeitsauslastung auf einer Skalierungseinheit ausführen, können Sie keine nicht unterstützten Prozesse für das spezifische Lager auf dem Hub ausführen. Die später in diesem Thema bereitgestellten Tabellen dokumentieren die unterstützten Funktionen.
>
> Ausgewählte Lagerort-Arbeitstypen können sowohl auf dem Hub als auch auf Skalierungseinheiten erstellt werden, können jedoch nur vom besitzenden Hub oder der besitzenden Skalierungseinheit (der Bereitstellung, die die Daten erstellt hat) verwaltet werden.
>
> Beachten Sie auch dann, wenn ein bestimmter Prozess von einer Skalierungseinheit unterstützt wird, dass möglicherweise nicht alle erforderlichen Daten vom Hub zur Skalierungseinheit oder von der Skalierungseinheit zum Hub synchronisiert werden, was zu einer unerwarteten Systemverarbeitung führen kann. Beispiele sind:
> 
> - Wenn Sie eine Abfrage der Lagerplatzrichtlinie, die einen Datentabellendatensatz verknüpft, der nur bei der Hubbereitstellung vorhanden ist.
> - Wenn Sie Standortstatus- und/oder Standortvolumenlastfunktionen verwenden. Diese Daten werden zwischen den Bereitstellungen nicht synchronisiert und funktionieren daher nur, wenn das vorhandene Standortinventar für eine der Bereitstellungen aktualisiert wird.

Die folgenden Funktionen der Lagerortverwaltung werden derzeit für Arbeitsauslastungen auf Skalierungseinheiten nicht unterstützt:

- Eingangsverarbeitung von Bestellpositionen, die einer Ladung zugeordnet sind
- Eingangsverarbeitung von Bestellungen für ein Projekt
- Eingangs- und Ausgangsbearbeitung für Elemente, die aktive Verfolgungsdimensionen **Besitzer** und/oder **Seriennummer** haben
- Verarbeitung von Beständen, die einen Sperrstatuswert haben
- Ändern eines Bestandsstatus während eines Arbeitsbewegungsprozesses
- Auftragsgebundene flexible Dimensionsreservierungen auf Lagerortebene
- Gebrauch der Funktionalität *Status des Lagerplatzes an einem Lagerort* (die Daten werden nicht zwischen den Bereitstellungen synchronisiert)
- Gebrauch der Funktionalität *Positionierung von Lagerplatzkennzeichen*
- Gebrauch von *Produktfiltern* und *Produktfiltergruppen*, einschließlich der Einstellung **Anzahl der Tage zum Mischen von Chargen**
- Integration mit dem Qualitätsmanagement
- Verarbeitung mit Catch-Weight-Elementen
- Verarbeitung mit Artikeln, die nur für die Transportverwaltung (TMS) aktiviert sind
- Verarbeitung mit negativem Bestand
- Lagerort-Arbeitsverarbeitung mit benutzerdefinierten Arbeitstypen
- Lagerort-Arbeitsverarbeitung mit Versandschein
- Lagerort-Arbeitsverarbeitung mit Auslösung des Zykluszählschwellenwerts
- Lagerort-Arbeitsverarbeitung mit Materialhandhabung/Lagerautomatisierung
- Verwendung des Produktstammdaten-Bildes (z. B. in der Lagerort-App)

> [!WARNING]
> Einige Lagerortfunktionen sind für Lageorte, in denen die Arbeitsauslastungen für die Lagerortverwaltung auf einer Skalierungseinheit ausgeführt werden, nicht verfügbar und werden auch auf dem Hub oder der Arbeitsauslastung der Skalierungseinheit nicht unterstützt.
> 
> Andere Funktionen können auf beiden Seiten verarbeitet werden, erfordern jedoch in einigen Szenarien eine sorgfältige Verwendung, z. B. wenn der Lagerbestand aufgrund des asynchronen Datenaktualisierungsprozesses für denselben Lager sowohl auf dem Hub als auch auf der Skalierungseinheit aktualisiert wird.
> 
> Spezifische Funktionen (wie *Arbeit sperren*), die sowohl auf dem Hub als auch auf den Skalierungseinheiten unterstützt werden, werden nur für den Eigentümer der Daten unterstützt.

### <a name="outbound-supported-only-for-sales-and-transfer-orders"></a>Outbound (wird nur für Verkaufsaufträge und Umlagerungsaufträge unterstützt)

Die folgende Tabelle zeigt, welche Funktionen im Outbound unterstützt werden und wo sie unterstützt werden, wenn die Arbeitsauslastungen der Lagerortverwaltung in Scale-Units und Edge-Einheiten verwendet werden.

| Bearbeiten                                                      | Hub | WES-Arbeitsauslastung in einer Scale-Unit |
|--------------------------------------------------------------|-----|------------------------------|
| Quellbeleg-Verarbeitung                                   | Ja | Nr. |
| Last- und Transportverwaltungs-Verarbeitung                | Ja | Nr. |
| Für Lagerort freigeben                                         | Ja | Nr. |
| Geplantes Crossdocking                                        | Nr.  | Nr. |
| Lieferungskonsolidierung                                       | Ja | Nr. |
| Verarbeitung von Sendungswellen                                     | Ja, aber die Initialisierung und Finalisierung der Welle wird im Hub durchgeführt. Dies bedeutet, dass nur die Verarbeitung von ausgehenden Umlagerungsaufträgen und Aufträge von der Skalierungseinheit abgewickelt werden können.|<p>Nein, Initialisierung und Finalisierung werden vom Hub durchgeführt, und **Ladungserstellung und -sortierung** werden nicht unterstützt<p><b>Hinweis:</b> Der Zugriff auf den Hub ist erforderlich, um den Wellenstatus als Teil der Wellenverarbeitung abzuschließen.</p> |
| Lieferungen für Welle verwalten                                  | Ja | Nr. |
| Lagerort-Arbeitsverarbeitung (inkl. Ladungsträger-Druck)        | Nr.  | <p>Ja, aber nur für die oben genannten unterstützten Funktionen. |
| Clusterkommissionierung                                              | Nr.  | Ja|
| Manuelle Verpackungsverarbeitung, inkl. Arbeitsverarbeitung „Entnahme aus gepacktem Container“                                           | Nr. <P>Einige Verarbeitungen können nach einem anfänglichen Kommissioniervorgang durchgeführt werden, der von einer Skalierungseinheit ausgeführt wird, werden jedoch aufgrund folgender blockierter Vorgänge nicht empfohlen.</p>  | Nr.  |
| Container aus Gruppe entfernen                        | Nr.  | Nr.                           |
| Ausgehende Sortierverarbeitung                                  | Nr.  | Nr. |
| Drucken von ladungsbezogenen Dokumenten                           | Ja | Nr. |
| Konnossement- und ASN-Generierung                            | Ja | Nr. |
| Versandbestätigung                    | Ja  | Nr. |
| Versandbestätigung mit „Bestätigen und übertragen“                    | Nr.  | Nr. |
| Lieferschein- und Rechnungsverarbeitung                | Ja | Nr. |
| Kurzkommissionierung (Verkaufs- und Umlagerungsaufträge)                    | Nr.  | Nr. |
| Zu hohe Entnahme (Verkaufs- und Umlagerungsaufträge)                     | Nr.  | Nr. |
| Änderung von Arbeitsplätzen (Verkaufs- und Umlagerungsaufträge)         | Nr.  | Ja|
| Arbeit abschließen (Verkaufs- und Umlagerungsaufträge)                    | Nr.  | Ja|
| Arbeitsbericht drucken                                            | Ja | Nr. |
| Serienetikett                                                   | Nr.  | Ja|
| Arbeitsaufteilung                                                   | Nr.  | Ja|
| Arbeitsverarbeitung – Geleitet von „Transportladung“            | Nr.  | Nr. |
| Entnommene Menge reduzieren                                       | Nr.  | Nr. |
| Arbeit stornieren                                                 | Nr.  | Nr. |
| Lieferungsbestätigung umkehren                                | Ja | Nr. |

### <a name="inbound"></a>Zugang

Die folgende Tabelle zeigt, welche Funktionen im Eingang unterstützt werden und wo sie unterstützt werden, wenn die Arbeitsauslastungen der Lagerortverwaltung in Scale-Units und Edge-Units verwendet werden.

| Bearbeiten                                                          | Hub | WES-Arbeitsauslastung in einer Scale-Unit<BR>*(Mit „Ja“ gekennzeichnete Artikel gelten nur für Lagerortaufträge.)*</p> |
|------------------------------------------------------------------|-----|----------------------------------------------------------------------------------|
| Quelle&nbsp;Dokument&nbsp;Verarbeitung                                       | Ja | Nr. |
| Last- und Transportverwaltungs-Verarbeitung                    | Ja | Nr. |
| Bestätigung eingehender Lieferungen                                            | Ja | Nr. |
| Freigabe der Einkaufsbestellung an den Lagerort (Lagerbestandsverarbeitung) | Ja | Nr. |
| Stornierung von Lagerortauftragspositionen<p>Beachten Sie, dass dies nur unterstützt wird, wenn keine Registrierung für die Position erfolgt ist</p>          | Ja | Nr. |
| Bestellungsartikel – Empfang und Einlagerung                       | <p>Ja,&nbsp;wenn&nbsp;kein Lagerort vorhanden ist&nbsp;keine Lagerbestellung</p><p>Nein, wenn eine Lagerort-Bestellung vorhanden ist</p> | <p>Ja, wenn eine Bestellung nicht Teil einer <i>Ladung</i> ist</p> |
| Bestellposition – Empfang und Einlagerung                        | <p>Ja, wenn kein Lagerort vorhanden ist</p><p>Nein, wenn eine Lagerort-Bestellung vorhanden ist</p> | <p>Ja, wenn eine Bestellung nicht Teil einer <i>Ladung</i> ist</p></p> |
| Rücklieferungsempfang und -einlagerung                               | Ja | Nr. |
| Empfang und Einlagerung gemischter Ladungsträger                        | <p>Ja, wenn kein Lagerort vorhanden ist</p><p>Nein, wenn eine Lagerort-Bestellung vorhanden ist</p> | Nr. |
| Artikelempfang aus Ladung                                             | <p>Ja, wenn kein Lagerort vorhanden ist</p><p>Nein, wenn eine Lagerort-Bestellung vorhanden ist</p> | Nr. |
| Kennzeichenempfang und -einlagerung                              | <p>Ja, wenn kein Lagerort vorhanden ist</p><p>Nein, wenn eine Lagerort-Bestellung vorhanden ist</p> | Nr. |
| Artikelempfang und -einlagerung für Umlagerungsauftrag                        | Ja | Nr. |
| Umlagerungsauftragsposition – Empfang und Einlagerung                        | Ja | Nr. |
| Arbeit stornieren (eingehend)                                              | <p>Ja, wenn kein Lagerort vorhanden ist</p><p>Nein, wenn eine Lagerort-Bestellung vorhanden ist</p> | <p>Ja, aber nur, wenn die Option <b>Bon bei Stornierung von Arbeit abmelden</b> (auf der Seite <b>Parameter der Lagerortverwaltung</b>) deaktivier ist</p> |
| Einkaufsbestellung Wareneingangsbearbeitung                          | Ja | Nr. |
| Bestelleingang mit Unterlieferung                        | <p>Ja, wenn kein Lagerort vorhanden ist</p><p>Nein, wenn eine Lagerort-Bestellung vorhanden ist</p> | Nein, da Sie nur die vollen Mengen von Lagerortauftragspositionen stornieren können |
| Bestelleingang mit Überlieferung                        | <p>Ja, wenn kein Lagerort vorhanden ist</p><p>Nein, wenn eine Lagerort-Bestellung vorhanden ist</p> | Ja  |
| Eingang mit Erstellung von *Cross-Docking*-Arbeit                   | <p>Ja, wenn kein Lagerort vorhanden ist</p><p>Nein, wenn eine Lagerort-Bestellung vorhanden ist</p> | Nr. |
| Eingang mit Erstellung von *Qualitätsprüfungsauftrags*-Arbeit                  | <p>Ja, wenn kein Lagerort vorhanden ist</p><p>Nein, wenn eine Lagerort-Bestellung vorhanden ist</p> | Nr. |
| Eingang mit Erstellung von *Qualitätsartikelmuster*-Arbeit          | <p>Ja, wenn kein Lagerort vorhanden ist</p><p>Nein, wenn eine Lagerort-Bestellung vorhanden ist</p> | Nr. |
| Eingang mit Erstellung von *Qualität in der Qualitätsprüfung*-Arbeit       | <p>Ja, wenn kein Lagerort vorhanden ist</p><p>Nein, wenn eine Lagerort-Bestellung vorhanden ist</p> | Nr. |
| Eingang mit Erstellung von Qualitätsprüfungsauftrag                            | <p>Ja, wenn kein Lagerort vorhanden ist</p><p>Nein, wenn eine Lagerort-Bestellung vorhanden ist</p> | Nr. |
| Arbeitsverarbeitung – Geleitet von *Clustereinlagerung*                             | Ja | Nr. |
| Arbeitsverarbeitung mit *kurzer Entnahme*                                           | Ja | Nr. |
| Ladungsträgerladung                                           | Ja | Nr. |

### <a name="warehouse-operations-and-exception-handing"></a>Lagerort-Operationen und Ausnahme-Handling

Die folgende Tabelle zeigt, welche Funktionen für Lagerort-Operationen und Exception Handing unterstützt werden und wo sie unterstützt werden, wenn die Arbeitsauslastungen der Lagerortverwaltung in Scale-Units und Edge-Units verwendet werden.

| Bearbeiten                                            | Hub | WES-Arbeitsauslastung in einer Scale-Unit |
|----------------------------------------------------|-----|------------------------------|
| Ladungsträger abfragen                              | Ja | Ja                          |
| Element abfragen                                       | Ja | Ja                          |
| Lagerplatz abfragen                                   | Ja | Ja                          |
| Lagerort ändern                                   | Ja | Ja                          |
| Bewegung                                           | Ja | Ja                          |
| Bewegung durch Vorlage                               | Ja | Ja                          |
| Lagerortumlagerung                                 | Ja | Nr.                           |
| Umlagerungsauftrag aus der Lagerort-App erstellen           | Ja | Nr.                           |
| Abgleich (rein/raus)                                | Ja | Nr.                           |
| Bestandsstatusänderung                            | Ja | Nr.                           |
| Zykluszählung und Zähldiskrepanzverarbeitung | Ja | Nr.                           |
| Label neu drucken (Ladungsträgerdruck)             | Ja | Ja                          |
| Ladungsträgererstellung                                | Ja | Nr.                           |
| Ladungsträgerauflösung                                | Ja | Nr.                           |
| Für geschachtelte Ladungsträger verpacken                                | Ja | Nr.                           |
| Einchecken durch Fahrer                                    | Ja | Nr.                           |
| Auschecken durch Fahrer                                   | Ja | Nr.                           |
| Chargendisposition-Code ändern                      | Ja | Ja                          |
| Offene Arbeitsliste anzeigen                             | Ja | Ja                          |
| Kennzeichen konsolidieren                         | Ja | Nr.                           |
| Nachschubverarbeitung mit Min/Max und Schwellenwert für Zonenwiederbeschaffung| Ja <p>Es wird empfohlen, nicht dieselben Standorte in die Abfragen aufzunehmen.</p>| Ja                          |
| Zuteilung von Zeitfenstern-Wiederbeschaffung                  | Ja  | Ja<p>Beachten Sie, dass die Einrichtung an der Skalierungseinheit erfolgen muss.</p>                           |
| Arbeit sperren und entsperren                             | Ja | Ja                          |
| Benutzer ändern                                        | Ja | Ja                          |
| Arbeitspool für Arbeit ändern                           | Ja | Ja                          |
| Arbeit stornieren                                        | Ja | Ja                          |


### <a name="production"></a>Produktion

Produktionsszenarien der Lagerortverwaltung werden derzeit für Arbeitsauslastungen auf Skalierungseinheiten nicht unterstützt, wie in der folgenden Tabelle angegeben.

| Bearbeiten | Hub | WES-Arbeitsauslastung in einer Scale-Unit |
|---------|-----|------------------------------|
| <p>Alle Lagerortverwaltungsprozesse, die mit der Produktion zusammenhängen. Im Folgenden finden Sie einige Beispiele hierfür:</p><li>Für Lagerort freigeben</li><li>Verarbeitung von Produktionswellen</li><li>Rohmaterialentnahme</li><li>Fertigmeldung und Einlagerung von Fertigerzeugnissen</li><li>Einlagerung von Co- und Nebenprodukten</li><li>Kanban-Einlagerung</li><li>Kanban-Entnahme</li><li>Produktionsauftrag starten</li><li>Produktionsausschuss</li><li>Letzte Palette der Produktion</li><li>Materialverbrauch registrieren</li><li>Kanban leeren</li></ul> | Ja | Nr. |

## <a name="maintaining-scale-units-for-wes"></a>Pflege von Scale-Units für WES

Sowohl auf der Hub- als auch auf der Scale-Unit laufen mehrere Batch-Jobs.

Auf der Hub-Bereitstellung können Sie die Batch-Jobs manuell pflegen. Sie können die folgenden drei Batchaufträgen unter **Lagerortverwaltung \> Periodische Aufgaben \> Back-Office-Arbeitsauslastung** verwalten:

- Arbeitsstatus-Aktualisierungsereignisse verarbeiten
- Hub-Nachrichtenverarbeitung zur Skalierungseinheit
- Quellauftragszugänge registrieren
- Lagerortaufträge abschließen
- Mengenaktualisierungsantworten für Lagerortauftragspositionen verarbeiten

Bei der Arbeitsauslastung in Skalierungsheiten können Sie die folgenden Batchaufträge unter **Lagerortverwaltung \> Periodische Aufgaben \> Arbeitsauslastungsverwaltung** verwalten:

- Verarbeiten von Wellentabellen-Sätzen
- Lagerorthub zu Skalierungseinheit-Nachrichtenprozessor
- Mengenaktualisierungsanforderungen für Lagerortauftragspositionen verarbeiten


[!INCLUDE[footer-include](../../includes/footer-banner.md)]