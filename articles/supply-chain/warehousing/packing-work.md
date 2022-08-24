---
title: Packarbeiten zum Packen von ausgehenden Containern und Verarbeiten von Sendungen
description: In diesem Artikel wird der Arbeitsauftragstyp „Verpacken“ beschrieben, der die Arbeit zum Verpacken von Containern verwaltet und Teillieferungen von gepackten Containern unterstützt, die sich auf Ladungen beziehen, bei denen Bestandsartikel unverpackt bleiben.
author: perlynne
ms.date: 7/13/2022
ms.topic: article
ms.search.form: WHSPackingWorkLocationSetup, WHSPack, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 34a7087df7e7768d0012ea4f534aa109654af8fa
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220551"
---
# <a name="packing-work-for-packing-outbound-containers-and-processing-shipments"></a>Packarbeiten zum Packen von ausgehenden Containern und Verarbeiten von Sendungen

[!include [banner](../../includes/banner.md)]

In diesem Artikel wird der Arbeitsauftragstyp *Verpacken* beschrieben, der die Arbeit zum Verpacken von Containern verwaltet und Teillieferungen von gepackten Containern unterstützt, die sich auf Ladungen beziehen, bei denen Bestandsartikel unverpackt bleiben. Für Verpackungsarbeiten können Sie die Funktion [Bestätigen und übertragen](confirm-and-transfer.md) zum Bestätigen ausgehender Sendungen verwenden, die Containern zugeordnet sind.

Verpackungsarbeit wird automatisch erstellt, wenn Inventar, das sich auf Quelldokumentarbeit bezieht, an Standorten des Typs *Verpackungsstandort* abgelegt wird. Die Arbeit besteht aus zwei Zeilen, eine für *Entnehmen* und eine für *Einlagern*, und wird automatisch als Teil eines Prozesses zum Schließen/Wiederöffnen eines Containers verwaltet.

Weitere Informationen zum Einrichten und Verwenden des Containerverpackungsprozesses finden Sie unter [Container für den Versand packen](packing-containers.md).

## <a name="turn-on-the-feature"></a>Aktivieren Sie die Funktion

Wenn Ihr System nicht bereits die in diesem Artikel beschriebenen Funktionen enthält, gehen Sie zu [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) und schalten Sie die folgenden Funktionen in der folgenden Reihenfolge ein: Beide Funktionen sind Teil des Moduls **Lagerortverwaltung**.

1. *Bestätigen und übertragen*
1. *Verpackungsarbeit für Verpackungsstationen*

## <a name="set-up-a-location-for-packing-work"></a>Standort für Verpackungsarbeit einrichten

Verwenden Sie die folgende Prozedur, um Verpackungslagerplätze einzurichten. Sie können für jeden Standort auswählen, ob das System automatisch Verpackungsarbeit erstellt.

1. Wechseln Sie zu **Warehouse Management \> Einrichten \> Verpackung \> Einrichtung der Verpackungsstation**.
1. Wählen Sie im Aktionsbereich **Neu** aus, um einen Einrichtungsdatensatz der Verpackungsstation hinzuzufügen.
1. Legen Sie im neuen Datensatz die folgenden Felder fest:

    - **Lagerort** – Wählen oder geben Sie den Lagerort aus, an dem sich der Verpackungslagerort befindet.
    - **Lagerplatz** - Geben oder wählen Sie den Verpackungslagerort aus. Dieser Standort muss einem Standortprofil zugewiesen werden, das den Standorttyp verwendet, der als Verpackungsstandorttyp für Ihr Unternehmen auf der Seite **Lagerverwaltungsparameter** konfiguriert ist. Weitere Informationen finden Sie unter [Container für den Versand packen](packing-containers.md).
    - **Verpackungsarbeit erstellen** – Aktivieren Sie dieses Kontrollkästchen, um jedes Mal Verpackungsarbeit zu erstellen, wenn Artikel an den Verpackungsstandort geliefert werden. Die Arbeit wird Links zu verwandten Ladungslinien enthalten, damit Teilladungen verpackt und versendet werden können.

## <a name="example-scenario"></a>Beispielszenario

Dieses Beispielszenario zeigt, wie Sie einen ausgehenden Kundenauftragsflow verarbeiten, indem Sie einen Container packen und eine Teilladung versenden.

### <a name="make-sample-data-available"></a>Beispieldaten zur Verfügung stellen

Um dieses Szenario mithilfe der Beispieldatensätze und -werte, die hier angegeben sind, zu verarbeiten, müssen Sie ein System verwenden, auf dem die standardmäßigen [Demodaten](../../fin-ops-core/fin-ops/get-started/demo-data.md) installiert sind. Außerdem müssen Sie die **USMF** juristische Person auswählen, bevor Sie beginnen.

Sie können dieses Szenario auch als Anleitung für die Verwendung der Funktion für ein Produktionssystem verwenden. In diesem Fall müssen Sie jedoch für jede hier beschriebene Einstellung Ihre eigenen Werte einsetzen.

### <a name="configure-packing-work-for-warehouse-packing-location"></a>Konfigurieren Sie die Verpackungsarbeit für den Verpackungsstandort des Lagers

Um zu beginnen, müssen Sie den Arbeitsprozess *Verpackung* für ein bestimmtes Lager und einen bestimmten Standort konfigurieren.

1. Wechseln Sie zu **Warehouse Management \> Einrichten \> Verpackung \> Einrichtung der Verpackungsstation**.
1. Um einen Einrichtungsdatensatz hinzuzufügen, wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie im neuen Datensatz die folgenden Werte fest:

    - **Lagerort:** *62*
    - **Lagerplatz:** *Verpackung*
    - **Verpackungsarbeit erstellen** *Ja*

1. Schließen Sie die Seite **Einrichtung der Verpackungsstation**.

### <a name="create-a-load-template-that-allows-partial-shipping"></a>Erstellen Sie eine Ladungsvorlage, bei der Teillieferungen möglich sind

Damit eine Ladung über mehrere Lieferungen hinweg geliefert werden kann, müssen Sie sie mit einer Ladungsvorlage verknüpfen, die einen Teilversand zulässt. Gehen Sie folgendermaßen vor, um eine Vorlage zu erstellen.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Ladung \> Ladungsvorlagen**.
1. Um einen Einrichtungsdatensatz hinzuzufügen, wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie im neuen Datensatz die folgenden Werte fest:

    - **Ladungsvorlagen-ID:** *Teilweise*
    - **Ladeteilung bei der Lieferbestätigung zulassen** *Ja*

1. Schließen Sie die Seite **Vorlagen laden**.

Weitere Informationen finden Sie unter [Bestätigen und übertragen](Confirm-and-transfer.md).

### <a name="process-a-sales-order"></a>Auftrag verarbeiten

Befolgen Sie diese Schritte, um einen Verkaufsauftrag zu verarbeiten und ihn teilweise zu versenden.

1. Vervollständigen Sie das [Beispielszenario](packing-containers.md#scenario), das unter [Container für den Versand packen](packing-containers.md) vorgesehen ist. In diesem Szenario erstellen Sie einen Verkaufsauftrag für zwei Stück eines Artikels. Sie werden dann nur eines der Stücke in einen Container packen und den Container schließen. Notieren Sie sich die Lieferungs-ID, die Sie erstellen, wie im Szenario beschrieben.
1. Gehen Sie zu **Lagerortverwaltung \> Arbeit \> Alle Arbeiten**.
1. Wählen Sie im Filterbereich **Geschlossene Arbeiten anzeigen** aus. Geben Sie dann die Lieferungs-ID in das Feld **Filter** ein und wählen Sie zum Filtern nach **Lieferungs-ID** aus. Sie sollten jetzt drei Arbeitskopfzeilen sehen. Einer ist für die Auftragskommissionierung und hat den Status *Abgeschlossen*. Zwei sind für den Verpackungsprozess bestimmt: Einer bezieht sich auf den geschlossenen Container und hat den Status von *Geschlossen*, und der andere bezieht sich auf den unverpackten verbleibenden Artikel und hat den Status *Offen*.
1. Wählen Sie **Ladungs-ID** aus für einen der zu öffnenden Arbeitskopfzeilen, um die Seite **Details laden** für die Ladung zu öffnen.
1. Wechseln Sie zur Ansicht **Kopfzeile**.
1. Auf dem Inforegister **Allgemein** wählen Sie **Bearbeiten** Schaltfläche für **Vorlagen-ID laden** aus. Wählen Sie dann die Vorlage für die Teilladung aus, die Sie für dieses Szenario erstellt haben (*Teilweise*).
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Liefern und empfangen** in der Gruppe **Bestätigen** die Option **Ausgehende Lieferung** aus.
1. Wählen Sie im Dialogfeld **Versand bestätigen** die **Menge auf neue Ladung aufteilen** aus.
1. Wählen Sie **OK** aus.

Sie haben jetzt einen Container versendet, der mit der ursprünglichen Ladung verknüpft ist, und das System hat eine neue Ladung für die verbleibenden Artikel erstellt, die noch in Container verpackt werden müssen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
