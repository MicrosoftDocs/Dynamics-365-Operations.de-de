---
title: Container zur Lieferung packen
description: Dieser Artikel beschreibt den Verpackungsprozess, mit dem Sie Bestandsartikel validieren und in Container verpacken können.
author: perlynne
ms.date: 7/13/2022
ms.topic: business-process
ms.search.form: WHSLocationType, WHSLocationProfile, WHSParameters, WHSContainerType, WHSPackProfile, WHSCloseContainerProfile, InventLocationIdLookup, UnitOfMeasureLookup, WHSPack, WHSContainerTable,
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 171b9f1dcb1d4ece63bc0beeb71f45b9f8ae7bba
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220561"
---
# <a name="pack-containers-for-shipment"></a>Container zur Lieferung packen

[!include [banner](../../includes/banner.md)]

Der Verpackungsprozess, mit dem Sie Bestandsartikel validieren und in Container verpacken können. Während dieses Prozesses kommissionieren Lagerarbeiter normalerweise Bestandsartikel aus Massenlagerbereichen und bringen sie zu einem Verpackungsbereich. Dort prüfen mehrere Lagermitarbeiter die Artikelmengen und -arten und ordnen sie den passenden Behältergrößen zu. Wenn ein Container vollständig gepackt ist, wird er geschlossen und zu den Ausgangsrampen verschoben, und die Produkte sind bereit zum Liefern.

Container stellen physische Strukturen dar, in denen Artikel verpackt sind, und Sie können Containerinformationen im System verfolgen. Diese Informationen können bei der Transportplanung nützlich sein, insbesondere wenn Sie Versandkosten auf der Grundlage von Containern berechnen. Vor dem Versand können Sie die Anzahl der in einer Sendung verwendeten Container, die verwendeten Containertypen und die physischen Abmessungen jedes Containers (z. B. Gesamtvolumen und -gewicht) anzeigen.

Mehrere verwandte Ausgangslagerfunktionen können mit Containern verwendet werden. Weitere Informationen finden Sie in folgenden Artikeln:

- [Wellencontainerisierung](wave-containerization.md)
- [Ausgangssortierung](outbound-sorting.md)
- [Kleinpaketlieferung](small-parcel-shipping.md)
- [Bestätigen und übertragen](confirm-and-transfer.md)
- [Festlegen verschiedener Dimensionen für Verpackung und Lagerung](packing-vs-storage-dimensions.md)
- [Packarbeiten zum Packen von ausgehenden Containern und Verarbeiten von Sendungen](packing-work.md)
<!-- KFM: Add link to upcoming topic when available (10.0.31): [Manual packing on the Warehouse management mobile app](manual-packing-on-the-warehouse-management-mobile-app.md) -->

## <a name="set-up-your-warehouse-to-use-manual-packing-operations"></a>Richten Sie Ihr Lager für manuelle Verpackungsvorgänge ein

Es gibt zwei grundlegende Möglichkeiten, Ihre ausgehenden Vorgänge zu organisieren:

- **Wellenerzeugung und -verarbeitung** – Arbeiter kommissionieren Artikel basierend auf ausgehender Lagerarbeit. Anschließend legen Sie die Artikel direkt in einem Ausgangsversandort ab, wo sie für den sofortigen Versand bereit sind. Informationen zum Einrichten und Verwenden dieses Prozesses finden Sie unter [Zykluserstellung und -verarbeitung](wave-processing.md).
- **Manuelles Verpacken an Packstationen** – Dieser Prozess hat einen zusätzlichen Vorgang zwischen Kommissionierung und Versand. Anstatt das Inventar an einen *Frachttür-Versandort* zu verschieben, wird er an den *Verpackungsstandort* verschoben. Anschließend steuern Sie den Verpackungsprozess am Packplatz mit Hilfe der Seite **Packen** im Webclient. Sie müssen Ihr System wie in diesem Abschnitt beschrieben vorbereiten, um den Prozess zu aktivieren.

### <a name="set-up-warehouse-locations-for-packing"></a>Lagerorte für Verpackung einrichten

Sie müssen mindestens einen Verpackungslagerplatz haben, an dem die Mitarbeiter Lagerartikel ablegen, damit sie in Container verpackt werden können. Weitere Informationen zum Erstellen von Lagerorten finden Sie unter [Konfigurieren von Standorten an einem WMS-aktivierten Lagerort](tasks\configure-locations-wms-enabled-warehouse.md) In den folgenden Unterabschnitten wird beschrieben, wie Sie diese Verpackungslagerplätze erstellen und einrichten.

#### <a name="set-up-location-types-for-packing"></a>Standortypen für Verpacken einrichten

Sie müssen einen *Standorttyp* für die Verpackungslagerplätze definieren. Lagerplatztypen können als Filteroptionen verwendet werden, die verschiedenen Lagerortverwaltungsprozesse zu steuern. Der Name jedes Standorttyps beschreibt normalerweise etwas darüber, wie dieser Standorttyp verwendet werden sollte. Der hier eingerichtete Standorttyp muss jedem Standort zugeordnet werden, der für Verpackungsvorgänge verwendet wird.

Gehen Sie zum Einrichten eines Standorttyps folgendermaßen vor.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerort \> Lagerplatztypen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um einen Standorttyp zum Raster hinzuzufügen.
1. Legen Sie die folgenden Felder für den neuen Standorttyp fest:

    - **Standorttyp**: Geben Sie einen eindeutigen Namen für den Standorttyp ein. Jeder Name muss eindeutig sein und sollte etwas darüber aussagen, wie der Standorttyp verwendet werden soll.
    - **Beschreibung** – Geben Sie eine kurze Beschreibung des Standorttyps ein.

#### <a name="inform-the-system-about-the-packing-location-type"></a>Teilen Sie dem System den Verpackungslagerplatztyp mit

Nachdem Sie einen Standorttyp erstellt haben, müssen Sie Ihr System so einrichten, dass er als Standorttyp für Verpackungsvorgänge erkannt wird.

Befolgen Sie diese Schritte, um den Standorttyp festzulegen, der für Verpackungsvorgänge verwendet wird.

1. Wechseln Sie zu **Lagerortverwaltung\> > Einrichtung > \>Lagerortverwaltungsparameter**.
2. Auf der Registerkarte **Allgemein**, auf dem Inforegister **Standorttypen** legen Sie den **Verpackungslagerplatztyp** auf den Standorttyp fest, den Sie verwenden, um Packstationen zu identifizieren.

> [!NOTE]
> Wenn Sie ein Upgrade von einer Version von Microsoft Dynamics AX ausführen, wird der Status *Beim Verpacken* von Lieferungen und Ladungen entfernt, da er nicht konsistent funktionierte und redundante Daten verursachte. Deshalb sind die Listenseiten **In Lieferung** und **Lasten in der Verpackung** veraltet. Container, die verpackt werden müssen, werden auf Standortebene verfolgt.
>
> In früheren Versionen haben Sie den Verpackungslagerplatz über das Feld **Profil-ID für den Verpackungsstandort** auf der Registerkarte **Verpackung** der Seite **Parameter für Lagerortverwaltung** definiert, um ein *Standortprofil* anzugeben. In der aktuellen Version verwenden Sie das Feld **Verpackungslagerort-Typ** auf der Registerkarte **Allgemein** der Seite **Parameter für Lagerortverwaltung**, um einen *Standorttyp*, wie in diesem Artikel beschrieben, anzugeben. Das neue Feld ist besser auf den Prozess zur Identifizierung von Bereitstellungsstandorten und endgültigen Versandstandorten abgestimmt.
>
> Obwohl Sie das alte Feld **Profil-ID für den Verpackungsstandort** weiter verwenden können, empfehlen wir Ihnen, mit der Verwendung des neuen Felds **Verpackungslagerort-Typ** zu beginnen, da das alte Feld irgendwann veraltet sein wird.
>
> Wenn Sie die Einstellung der alten **Profil-ID für den Verpackungsstandort** löschen und dann die Seite speichern, wird das Feld dauerhaft deaktiviert. Für Installationen, bei denen das Feld **Profilkennung für Verpackungslagerplatz** nie verwendet wurde, wird es immer deaktiviert sein. Nachdem Sie die Einstellung des Feldes **Profilkennung für Verpackungslagerplatz** gelöscht haben, verwenden Sie die in diesem Artikel beschriebenen Einstellungen, um Ihren Verpackungsstandort einzurichten und zu identifizieren.

#### <a name="set-up-location-profiles-for-packing-locations"></a>Standortprofile für Verpackungslagerplätze einrichten

Jeder *Standortprofil* legt Informationen und Regeln fest, die für die zugehörigen Standorte gelten. Da Sie mindestens einen Standort für Verpackungsvorgänge benötigen, müssen Sie zusätzlich zu einem Standorttyp ein Standortprofil dafür erstellen. Jedes Profil kann von beliebig vielen Standorten verwendet werden. Standorte, die zum Verpacken verwendet werden, müssen für die Nachverfolgung von Nummernschildern eingerichtet werden.

Befolgen Sie diese Schritte, um ein Standortprofil für einen Verpackungsstandort einzurichten.

1. Wechseln Sie zu **Lagerortverwaltung \> Einrichtung \> Lagerort \> Lagerplatzprofile**.
1. Wählen Sie entweder ein vorhandenes Profil im Listenbereich, oder wählen Sie **Neu** im Aktivitätsbereich, um ein neues Profil zu erstellen.
1. Legen Sie in der Kopfzeile des neuen oder ausgewählten Profils die folgenden Felder fest:

    - **Lagerplatz-Profilkennung**: Geben Sie eine eindeutige Kennung für das Profil ein.
    - **Name** - Geben Sie einen beschreibenden Namen für das Profil ein.

1. Legen Sie im Inforegister **Allgemein** die folgenden Felder fest:

    - **Standortformat** – Wählen Sie das Standortformat aus, das für den aktuellen Standort verwendet werden soll. Lagerplatzformate sind ein Benennungssystem, das verwendet wird, um die eindeutige und konsistenten Namen für die verschiedenen Lagerplatzlagerfachpositionen zu erstellen, die innerhalb eines Lagerorts verwendet werden. Wenn Sie das benötigte Format noch nicht haben, können Sie es erstellen, indem Sie auf **Lagerortverwaltung \> Einrichtung \> Lagerort \> Standortformate** gehen. Weitere Informationen finden Sie unter [Konfigurieren von Standorten in einem WMS-aktivierten Lagerort](tasks/configure-locations-wms-enabled-warehouse.md).
    - **Standorttyp** – Wählen Sie den Standorttyp aus, der auf dem als Verpackungslagerplatztyp auf der Seite **Parameter für Lagerortverwaltung** eingerichtet ist, wie weiter oben in diesem Artikel beschrieben.
    - **Verwenden Sie die Nummernschildverfolgung** – Stellen Sie diese Option für Verpackungslagerplätze auf *Ja* ein. Das System muss in der Lage sein, Kennzeichen-IDs an Verpackungsstandorten zu verfolgen, damit es den Verpackungsprozess steuern kann.
    - **Negatives Inventar zulassen** – Stellen Sie diese Option für Verpackungslagerplätze auf *Nein* ein.
    - **Gemischte Artikel zulassen** – Stellen Sie diese Option für Verpackungslagerplätze auf *Ja* ein. Diese Einstellung ist erforderlich, da typischerweise viele unterschiedliche Artikelnummern gleichzeitig an die Verpackungslagerplätze gebracht werden.
    - **Gemischte Bestandsstatus zulassen** – Stellen Sie diese Option für Verpackungslagerplätze auf *Ja* ein. Diese Einstellung ist erforderlich, da typischerweise Artikel viele unterschiedliche Bestandsstatus haben, die gleichzeitig an die Verpackungslagerplätze gebracht werden.
    - **Gemischte Bestandchargen zulassen** – Stellen Sie diese Option für Verpackungslagerplätze auf *Ja* ein. Diese Option ist automatisch auf *Ja* festgelegt und die Option **Gemischte Artikel zulassen** ist auf *Ja* festgelegt.

#### <a name="set-up-packing-locations"></a>Verpackungslagerplätze einrichten

Sie müssen mindestens einen *Standort* haben, an dem die Mitarbeiter Lagerartikel ablegen, damit sie in Container verpackt werden können.

Gehen Sie zum Einrichten eines Verpackungslagerplatzes folgendermaßen vor.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerort \> Lagerplätze**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um einen Standort hinzuzufügen.
1. Legen Sie die folgenden Felder für den neuen Standort fest:

    - **Lagerort** – Wählen Sie den Lagerort aus, an dem sich der Verpackungslagerplatz befinden muss.
    - **Standort**: Geben Sie einen Namen für den neuen Standort ein.
    - **Standortprofil-ID** – Achten Sie darauf, die ID anzugeben, die Sie im vorherigen Abschnitt erstellt haben.

## <a name="set-up-the-packing-process"></a>Den Verpackungsprozess einrichten

In diesem Abschnitt wird beschrieben, wie Sie Einstellungen konfigurieren, die den Verpackungsprozess aktivieren und es Mitarbeitern ermöglichen, Inventar in Container zu packen.

### <a name="set-up-container-packing-policies"></a><a name="packing-policy"></a>Einrichten von Containerverpackungsrichtlinien

Jede *Verpackungsrichtlinie für Container* definiert, wie ein Container verarbeitet werden soll. Jedes Mal, wenn Sie einen neuen Container erstellen, wählen Sie auch eine Containerverpackungsrichtlinie aus, die darauf angewendet werden soll.

Gehen Sie zum Einrichten einer Containerverpackungsrichtlinie folgendermaßen vor.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Container \> Containerverpackungsrichtlinien**.
1. Wählen Sie entweder eine vorhandene Richtlinie im Listenbereich, oder wählen Sie **Neu** im Aktivitätsbereich, um eine neue zu erstellen.
1. Legen Sie in der Kopfzeile der neuen oder ausgewählten Richtlinie die folgenden Felder fest:

    - **Verpackungsrichtlinie für Container** – Geben Sie einen eindeutigen Namen für die Richtlinie ein.
    - Geben Sie im Feld **Beschreibung** einen Namen für die Richtlinie ein.

1. Legen Sie auf der Registerkarte **Überblick** die folgenden Felder fest: Mit diesen Feldern können Sie festlegen, welche Maßnahmen ergriffen werden sollen, wenn der Container geschlossen wird, ob mit oder ohne Arbeitserstellung gearbeitet werden soll und wann der Container von der Packstation freigegeben werden soll.

    - **Lagerort** – Wählen Sie den Lagerort aus, für den die Verpackungsrichtlinie gilt.
    - **Standardlagerplatz für endgültige Lieferung** – Geben Sie den bevorzugten Standort für den Container nach dem Schließen an. Dieses Feld ist nur verfügbar, wenn das Feld **Containerfreigaberichtlinie** als *An endgültigem Versandort verfügbar machen* festgelegt ist.
    - **Standardlagerplatz für die Sortierung** – Dieses Feld wird mit der Funktion [Ausgangssortierung](outbound-sorting.md) verwendet.
    - **Gewichtseinheit** – Wählen Sie die Standardmaßeinheit aus, die verwendet werden soll, wenn ein Container geschlossen und manifestiert wird. Typischerweise ist diese Maßeinheit die Maßeinheit, die von einer Waage an der Verpackungsstation verwendet wird. Dieses Feld gilt für Richtlinien mit oder ohne Arbeitserstellung.
    - **Containerabschlussrichtlinie** – Wählen Sie eine der folgenden Optionen, um festzulegen, was beim Schließen des Containers geschehen soll:

        - *Automatische Freigabe* – Der Container gilt als von der Packstation freigegeben, und die Aktion im Feld **Containerabschlussrichtlinie** wird ausgelöst.
        - *Verspätete Veröffentlichung* – Der Container wird nicht sofort von der Packstation freigegeben. Ein Lagerarbeiter muss ihn später manuell freigeben.
        - *Optional* – Während ein Arbeiter den Container schließt, kann er wählen, ob der Container freigegeben werden soll.

        Handelt es sich bei der Packstation hauptsächlich um Einzelgebinde, die direkt an Kunden verschickt werden, ist es naheliegend, die Container sofort freizugeben. Wenn die Packstation Sendungen bearbeitet, die aus mehreren Containern oder sogar Paletten bestehen, ist es wahrscheinlich am besten, die Freigabe zu verschieben, bis die gesamte Sendung oder Palette verpackt und abholbereit ist.

    - **Containerfreigaberichtlinie** – Wählen Sie eine der folgenden Optionen, um festzulegen, was beim Freigeben des Containers geschehen soll:

        - *Am endgültigen Versandort verfügbar machen* – Aktualisieren Sie den Container auf den endgültigen Versandort. Wenn Sie diese Option auswählen, verwenden Sie **Standardlagerplatz für endgültige Lieferung**, um den bevorzugten Standort für den Container nach dem Schließen anzugeben.
        - *Arbeit erstellen, um Container aus Verpackungsstation zu verschieben* – Erstellen Sie Arbeit, um den Container von der Packstation zum Bereitstellungsbereich oder direkt zum Hallentor zu transportieren. Verwenden Sie das Feld **Arbeitsvorlage**, um die Arbeitsvorlage anzugeben, die angewendet werden soll, wenn Arbeit für den Container erstellt wird.
        - *Container einer ausgehenden Sortierungsposition zuweisen* – Diese Option wird mit der Funktion [Ausgangssortierung](outbound-sorting.md) verwendet.

        In den meisten Fällen empfehlen wir Ihnen, Arbeit zum Verschieben von Containern zu erstellen, da dieser Ansatz die tatsächlichen manuellen Prozesse im Lager besser abbildet. Für einfache Szenarien oder Situationen, in denen sich die Packstation direkt im Hallentorbereich befindet, kann es jedoch vorzuziehen sein, dass der Container sofort am endgültigen Versandort verfügbar ist.

    - **Arbeitsvorlage** - Wählen Sie die Arbeitsvorlage, die angewendet werden soll, wenn Arbeit für den Container erstellt wird. Dieses Feld ist nur verfügbar, wenn das Feld **Containerfreigaberichtlinie** auf *Arbeit erstellen, um Container aus Verpackungsstation zu verschieben* gesetzt und sich auf den Arbeitsauftragstyp *Entnahme aus gepacktem Container* bezieht. Weitere Informationen zu Vorlagen erhalten Sie unter [Arbeitsvorlagen und Lagerplatzanweisungen](control-warehouse-location-directives.md).

    In den verbleibenden Schritten konfigurieren Sie Einstellungen, die sich auf *Manifestierung* beziehen. Beim Manifestieren wird das Gewicht eines Containers, einer Containergruppe oder Sendung zusammen mit der Tracking-ID angegeben, die von einem Transportanbieter erhalten wird. Dynamics 365 Supply Chain Management lässt sich nicht in Systeme externer Transportanbieter integrieren. Stattdessen müssen Lagerarbeiter Beschriftungen drucken, die sie vom Transportanbieter erhalten, und dann eine Sendungsverfolgungsnummer scannen, wenn sie das Manifestverfahren abschließen.

    Da die Manifestanforderungen von Kunde zu Kunde und sogar von Sendung zu Sendung variieren, ermöglichen Verpackungsrichtlinien eine erhebliche Flexibilität im Arbeitsablauf. Sie können Manifeste für Container, Containergruppen und Sendungen in beliebiger Kombination einrichten.

    Wenn Sie ein mehrstufiges Manifestverfahren verwenden, müssen Arbeiter alle Container manifestieren, bevor sie die zugehörige Containergruppe manifestieren, und sie müssen alle Containergruppen manifestieren, bevor sie die zugehörige Sendung manifestieren.

1. Legen Sie im Inforegister **Containermanifestierung** die folgenden Felder fest:

    - **Automatisches Manifest beim Schließen des Containers** – Stellen Sie diese Option auf *Ja* zum Anwenden von Manifestinformationen als Teil des Containerabschlussprozesses. Wenn Sie die Transportintegration nicht verwenden, müssen die Informationen manuell erfasst werden.
    - **Manifestanforderungen für Container** – Wählen Sie eine der folgenden Optionen:

        - *Keine* – Es wird kein Manifestierungsprozess verwendet.
        - *Manuell* – Das Manifestieren wird vom Verpackungsworkflow verlangt. Das System lässt nicht zu, dass ein Container geschlossen oder freigegeben wird, bis die Manifestierung abgeschlossen ist.
        - *Transportverwaltung* – Die Manifestierung erfolgt über die Tarifmodule des Transportmanagements (TMS). Da diese Option eine benutzerdefinierte Entwicklung erfordert, um eine bestimmte Engine für den Transportanbieter zu implementieren, funktioniert sie in der aktuellen Version nicht standardmäßig.

    - **Containerinhalt drucken** – Stellen Sie diese Option auf *Ja* zum automatischen Drucken des Containerinhaltsberichts, wenn ein Container als geschlossen registriert wird. Sie können auch den Bericht bei Bedarf drucken.

1. Auf dem Inforegister **Containergruppenmanifest** im Feld **Manifestanforderungen für die Containergruppe** wählen Sie eine der folgenden Optionen aus:

    - *Keiner* – Das Containergruppenmanifest wird nicht als Anforderung in den Verpackungsworkflow aufgenommen.
    - *Manuell* – Das Containergruppenmanifest wird als Anforderung in den Verpackungsworkflow aufgenommen. Alle Container in der Gruppe müssen geschlossen sein, bevor die Containergruppe mit einem Manifest versehen werden kann. Wählen Sie diese Option, wenn Sie für jede Containergruppe, die an der Packstation verpackt wird, ein Manifest ausfüllen müssen. Sie werden diese Option normalerweise auswählen, wenn Container auf eine Palette gepackt werden und die gesamte Palette manifestiert wird.

    > [!NOTE]
    > Die aktuelle Version unterstützt keine Manifestberichte für Containergruppen, und es gibt keine TMS-Engine-Unterstützung für Containergruppen.

1. Legen Sie im Inforegister **Lieferungsmanifest** die folgenden Felder fest:

    - **Manifestanforderungen für Lieferung** – Wählen Sie eine der folgenden Optionen:

        - *Keiner* – Das Lieferungsmanifest wird nicht als Anforderung in den Verpackungsworkflow aufgenommen.
        - *Manuell* – Das Lieferungsmanifest wird als Anforderung in den Verpackungsworkflow aufgenommen. Es können keine Container für eine Sendung freigegeben werden, bis die Manifestierung abgeschlossen ist.
        - *Transportverwaltung* – Die Manifestierung erfolgt über die TMS-Tarifmodule (TMS). Da diese Option eine benutzerdefinierte Entwicklung erfordert, um eine bestimmte Engine für den Transportanbieter zu implementieren, funktioniert sie in der aktuellen Version nicht standardmäßig.

        Das Lieferungsmanifest sollte aktiviert werden, wenn Sie ein Manifest für die gesamte Sendung ausfüllen müssen, die an der Packstation verpackt wird. Es wird normalerweise verwendet, wenn ein konsolidiertes Manifest erforderlich ist, obwohl die Lieferung aus mehreren Containern oder Containergruppen besteht.

    - **Lieferschein drucken** – Stellen Sie diese Option auf *Ja*, um automatisch den Lieferschein als Teil des Sendungsverzeichnisses auszudrucken. Sie können auch den Lieferschein bei Bedarf drucken.

### <a name="set-up-container-types"></a>Richten Sie Containertypen ein

Während des manuellen Verpackungsprozesses müssen Container erstellt werden, bevor Artikel darin verpackt werden können. Jeder Container muss auf einem *Containertyp* basieren, der das maximale physische Volumen und die Gewichtskapazität eines Containers definiert.

Gehen Sie zum Erstellen eines Containertyps folgendermaßen vor:

1. Gehen Sie zu **Lagerortverwaltung \> Einrichten \> Container \> Containertypen**.
1. Wählen Sie im Aktionsbereich **Neu** aus, um einen Containertyp hinzuzufügen.
1. Legen Sie die folgenden Felder für den neuen Containertyp fest:

    - **Containertyp-Code** – Geben Sie eine eindeutige ID für den Containertyp ein.
    - **Beschreibung** – Geben Sie eine detaillierte Beschreibung des neuen Containertyps ein.
    - **Verpackungsgewicht** - das tatsächliche oder vorkalkulierte Gewicht des Containers ein.
    - **Höchstnettogewicht** - Geben Sie das Höchstgewicht an, das der Container fassen kann.

1. Geben Sie im Abschnitt **Containerabmessungen**, in den Feldern **Länge**, **Breite**, **Höhe** und **Volumen** die physischen Abmessungen des Containers selbst ein.
1. Geben Sie im Abschnitt **Höchstwerte**, in den Feldern **Länge**, **Breite**, **Höhe** und **Volumen** die maximalen physischen Abmessungen des Containers ein.
1. Sie können zusätzliche Attribute für Containertypen definieren, die anderen Vorgängen zugeordnet sind, die Container verwenden. Weitere Informationen finden Sie unter [Containerisierung](wave-containerization.md).

> [!NOTE]
> Für den manuellen Verpackungsprozess verwendet das System nur den Wert **Maximales Nettogewicht** und den Wert für **Volumen** im Abschnitt **Höchstwerte**.

### <a name="set-up-packing-profiles"></a>Richten Sie Verpackungsprofile ein

*Verpackungsprofile* werden für den Verpackungsprozess benötigt. Sie können ausgewählt oder standardmäßig eingestellt werden, wenn Sie einen Verpackungsvorgang auf der Seite **Packen** starten.

Gehen Sie zum Einrichten eines Verpackungsprofils folgendermaßen vor.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Verpackung \> Verpackungsprofile**.
1. Wählen Sie entweder ein vorhandenes Profil im Listenbereich, oder wählen Sie **Neu** im Aktivitätsbereich, um ein neues Profil zu erstellen.
1. Legen Sie in der Kopfzeile des neuen oder ausgewählten Profils die folgenden Felder fest:

    - **Verpackungsprofilkennung**: Geben Sie eine kurze ID für das Profil ein.
    - **Beschreibung** – Geben Sie eine detaillierte Beschreibung des Verpackungsprofils ein.
    - **Verpackungsrichtlinie für Container** – Wählen Sie die Verpackungsrichtlinie aus, die für das Profil gilt. Weitere Informationen finden Sie im Abschnitt [Einrichten von Containerverpackungsrichtlinien](#packing-policy) in diesem Artikel.
    - **Containerkennungsmodus** - Diese Option bestimmt, ob eine Containerkennung automatisch generiert wird, wenn ein Container erstellt wird, oder eine Containerkennung wird manuell erstellt.
    - **Containertyp** - Wählen Sie aus, ob der standardmäßig verwendete Container verwendet wird, wenn ein neuer Container erstellt wird.
    - **Container beim Schließen des Containers automatisch erstellen** – Aktivieren Sie dieses Kontrollkästchen, um automatisch einen neuen Container zu erstellen, wenn der vorherige Container geschlossen ist und eine oder mehrere Positionen in der aktuellen Sendung verbleiben.

### <a name="set-up-warehouse-workers"></a>Einrichten von Lagerortarbeitskräften

Jeder Benutzer oder Arbeiter, der Container verpackt, indem er die Seite **Packen** des Webclients oder den Aktivitätscode *Verpackung* in der mobilen App für Warehouse Management verwendet, muss ein Benutzerkonto haben, das mit einem *Arbeitskraft/Person*-Datensatz verknüpft ist, dem die erforderlichen Sicherheitszugriffsrechte zugewiesen sind. (Weitere Informationen zum Einrichten von Benutzern finden Sie unter [Neue Benutzer erstellen](../../fin-ops-core/dev-itpro/sysadmin/tasks/create-new-users.md).)

Befolgen Sie diese Schritte, um einen *Arbeitskraft/Mensch*-Datensatz für den Verpackungsprozess einzurichten.

1. Wechseln Sie zu **Lagerortverwaltung \> Einrichtung \> Arbeitskraft**.
1. Wählen Sie im Aktionsbereich **Neu** aus, um einen Arbeitsbenutzer hinzuzufügen.
1. Stellen Sie die das Feld **Arbeitskraft** auf den vorhandenen Arbeitskraftdatensatz, der im Modul **Personalwesen** für den Benutzer definiert ist, der den Verpackungsprozess abschließt.
1. Legen Sie im Inforegister **Profil** die folgenden Felder fest:

    - **Verpackungsrichtlinie für Container** – Wählen Sie eine Containerpackrichtlinie aus, die definiert, wie Container an der Packstation verarbeitet werden sollen. Die ausgewählte Containerpackrichtlinie wird für die Arbeitskraft beim Öffnen der Packstation vorausgewählt. Weitere Informationen finden Sie im folgenden Blogbeitrag: [Verbesserte Verpackungsfunktionalität](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/12/01/improved-packing-functionality-dynamics-365-for-operations-1611).
    - **Verpackungsprofil-ID** – Wählen Sie eine Verpackungsprofil-ID aus, die die verwendeten Verpackungsrichtlinien und die zu verwendenden Containereinstellungen definiert. Wenn die ausgewählte Verpackungsprofil-ID mit einer Containerverpackungsrichtlinie verknüpft ist, können Sie die **Verpackungsrichtlinie für Container**-Einstellung auf dieser Seite nicht verwenden.

1. Wählen Sie auf dem Inforegister **Standardverpackungsstation** den Standardstandort, das Lager und den Standort aus, die für die Arbeitskraft gelten.
1. Wenn die Arbeitskraft die mobile App für Warehouse Management verwendet, um ihre Containerverpackungsarbeit zu verwalten und zu registrieren, richten Sie im Inforegister **Benutzer** ein oder mehrere Konten ein, mit denen sich der Mitarbeiter bei der App anmelden kann. (Weitere Informationen finden Sie unter [Benutzerkonten für mobile Geräte](mobile-device-work-users.md).)

## <a name="example-scenario"></a><a name="scenario"></a>Beispielszenario

Dieser Abschnitt enthält ein Beispielszenario, das zeigt, wie Sie eine Bestellung erstellen und die Artikel verpacken.

### <a name="make-sample-data-available"></a>Beispieldaten zur Verfügung stellen

Um dieses Szenario mithilfe der Beispieldatensätze und -werte, die hier angegeben sind, zu verarbeiten, müssen Sie ein System verwenden, auf dem die standardmäßigen [Demodaten](../../fin-ops-core/fin-ops/get-started/demo-data.md) installiert sind. Außerdem müssen Sie die **USMF** juristische Person auswählen, bevor Sie beginnen.

Sie können dieses Szenario auch als Anleitung für die Verwendung der Funktion für ein Produktionssystem verwenden. In diesem Fall müssen Sie jedoch für jede hier beschriebene Einstellung Ihre eigenen Werte einsetzen.

### <a name="sign-in-as-a-user-that-can-do-packing-work"></a>Melden Sie sich als Benutzer an, der Verpackungsarbeiten ausführen darf

Melden Sie sich bei Supply Chain Management an, indem Sie ein Benutzerkonto verwenden, das über die Berechtigungen verfügt, die zum Packen von Containern erforderlich sind. Die Benutzerin *Julia Funderburg* ist in den Demodaten enthalten und verfügt über die erforderlichen Berechtigungen. Diese Benutzerin hat die Benutzer-ID *Administrator*.

### <a name="create-a-sales-order-and-complete-the-work"></a>Erstellen eines Auftrags und Abschließen der Arbeit

Befolgen Sie diese Schritte, um einen Kundenauftrag zu erstellen und die Arbeit zum Transport der bestellten Artikel zur Packstation abzuschließen.

1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Wählen Sie im Dialogfeld **Auftrag erstellen** im Feld **Debitorenkonto** *US-005* aus.
1. Klicken Sie auf **OK**, um das Dialogfeld zu schließen.
1. Der neue Verkaufsauftrag wird geöffnet und enthält eine einzelne, leere Zeile auf dem Inforegister **Verkaufsauftragszeilen**. Stellen Sie die folgenden Werte für die neue Bestellposition ein:

    - **Artikelnummer** *A001*
    - **Menge** *2*
    - **Standort:** *6*
    - **Lagerort:** *62*

1. Während die Auftragsposition weiterhin ausgewählt ist, wählen Sie im Inforegister **Auftragspositionen\>Reservierung** auf der Menüleiste des Inforegister **Auftragspositionen** aus.
1. Wählen Sie auf der Seite **Reservierung** im Aktivitätsbereich die Option **Los reservieren** aus, um die volle Menge der ausgewählten Position im Lagerort zu reservieren.
1. Schließen Sie die Seite **Reservierung**, um zum Auftrag zurückzukehren.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**.

    Eine Nachricht zeigt die Sendungs- und Zyklus-IDs für die Bestellung an.

1. Während die Auftragsposition weiterhin ausgewählt ist, wählen Sie im Inforegister **Auftragspositionen**\> **Arbeitsdetails** auf der Menüleiste des Inforegisters **Auftragspositionen** aus. Wenn Sie zum Ausführen Ihrer Waves die Stapelverarbeitung verwenden, müssen Sie möglicherweise kurz warten, bis die Arbeit erstellt wurde.
1. Wählen Sie im Aktivitätsbereich auf der Seite **Arbeit** in der Registerkarte **Arbeit** die Option **Arbeit abschließen**.
1. Geben Sie auf der Seite **Arbeitsabschluss** im Feld **Benutzer-ID** *62* ein.
1. Wählen Sie im Aktionsbereich **Arbeit überprüfen** aus.
1. Wenn Sie eine Meldung erhalten, die angibt, dass Ihre Arbeit gültig ist, wählen Sie **Arbeit abschließen** aus, um den Prozess der Kommissionierung der Inventargegenstände und deren Einlagerung am Standort *Verpacken* abzuschließen.
1. Notieren Sie sich die **Lieferungs-ID**, die für die Arbeit im oberen Raster angezeigt wird.

### <a name="pack-the-ordered-items-into-a-container"></a>Packen Sie die bestellten Artikel in einen Container

Die Lagerartikel wurden nun zum Verpackungsbereich gebracht und können in Container verpackt werden. Gehen Sie folgendermaßen vor, um einen neuen Container im System zu erstellen und zu packen.

1. Gehen Sie zu **Lagerortverwaltung \> Verpackung und Containerisierung \> Verpackung**.
1. Legen Sie im Dialogfeld **Verpackungsstation auswählen** die folgenden Werte fest:

    - **Standort:** *6*
    - **Lagerort:** *62*
    - **Lagerplatz:** *Verpackung*
    - **Verpackungsprofilkennung:** *WH62*

1. Wählen Sie **OK** aus.
1. Geben Sie auf der Seite **Verpackung** im Feld **Kennzeichen oder Lieferung** die zuvor notierte Lieferungs-ID. Sie sollten nun die verbleibenden unverpackten Artikel auf dem Inforegister **Offene Positionen** sehen.
1. Wählen Sie im Aktionsbereich **Neuer Container** aus, um einen Container im System zu erstellen.
1. Im Dialogfeld **ID des neuen Containers** legen Sie das Feld **Containertyp** auf *SmallBox* fest.
1. Wählen Sie **OK**, um den Container zu erstellen.
1. Wählen Sie **OK** aus, um zur Seite **Packen** zurückzukehren. Das Inforegister **Offene Container** zeigt jetzt die **Container-ID** des Containers, den Sie erstellt haben.
1. Für dieses Szenario verpacken Sie zunächst nur einen der bestellten Artikel. Legen Sie im Inforegister **Artikelverpackung** die folgenden Werte fest:

    - **Menge** *1.00*
    - **Bezeichner:** *A0001*

    Unmittelbar nach der Auswahl von **Bezeichner** aktualisiert die Seite **Offene Positionen** und **Alle Positionen**, um anzuzeigen, dass ein Artikel verpackt wurde. Sie sollten jetzt eines der beiden Teile des Artikels *A0001* verpackt haben.

1. Wählen Sie im Aktivitätsbereich **Container schließen** aus.
1. Wählen Sie im Dialogfeld **Container schließen** die Option **Systemgewicht abrufen**, damit das System das Feld **Bruttogewicht** einträgt.
1. Klicken Sie auf **OK**, um den Container zu schließen.

> [!TIP]
> Es gibt verschiedene Möglichkeiten, Container basierend auf dem Kontext anzuzeigen. Wenn Sie beispielsweise eine Lieferung verpacken, ist es oft hilfreich, entweder Container anzuzeigen, die Teil der Lieferung sind, oder alle Container, die sich physisch an einer Verpackungsstation befinden. Die Seite **Verpackungsstation** verfügt über Schaltflächen, mit denen Sie alle offenen und geschlossenen Container an einer Verpackungsstation anzeigen können. Diese Ansichten sind nicht auf eine bestimmte Lieferung beschränkt. Sie können in Situationen sehr hilfreich sein, in denen ein Arbeiter einen Container packt und ein anderer Arbeiter den Container manifestiert und freigibt.
>
> Eine konsolidierte Ansicht aller Container ist ebenfalls verfügbar. Diese Ansicht ist vor allem für Benutzer nützlich, die außerhalb des Kontexts einer einzelnen Verpackungsstation arbeiten. Um sie anzuzeigen, wechseln Sie zu **Warehouse Management \>Packen und Containerisierung \> Container**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
