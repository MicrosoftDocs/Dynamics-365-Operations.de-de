---
title: Festlegen verschiedener Dimensionen für Verpackung und Lagerung
description: In diesem Artikel wird gezeigt, wie Sie angeben, für welchen Prozess (Verpackung, Lagerung oder verschachtelte Verpackung) jede angegebene Dimension verwendet wird.
author: Mirzaab
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResPhysicalProductDimensions, WHSPhysDimUOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: e2cfcc13f397f57413be1773683daf1f828beaf8
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334444"
---
# <a name="set-different-dimensions-for-packing-and-storage"></a>Festlegen verschiedener Dimensionen für Verpackung und Lagerung

[!include [banner](../../includes/banner.md)]

Einige Artikel werden so verpackt oder gelagert, dass Sie möglicherweise die physischen Dimensionen für jeden von mehreren verschiedenen Prozessen unterschiedlich nachverfolgen müssen. Die Funktion *Produktdimensionen für Verpackung* ermöglicht für jedes Produkt das Einrichten einer oder mehrerer Arten von Dimensionen. Jede Dimensionsart bietet eine Reihe physikalischer Messwerte (Gewicht, Breite, Tiefe und Höhe) und legt den Prozess fest, bei dem diese physikalischen Messwerte gelten. Wenn diese Funktion aktiviert ist, unterstützt Ihr System die folgenden Arten von Dimensionen:

- *Lagerung* – Die Lagerdimensionen werden zusammen mit Volumenmetriken für den Lagerplatz verwendet, um zu bestimmen, wie viele Artikel an verschiedenen Lagerort-Lagerplätzen gelagert werden können.
- *Verpackung* – Die Verpackungsdimensionen werden während der Containerisierung und des manuellen Verpackungsprozesses verwendet, um zu bestimmen, welche Stückzahl eines jeden Artikels in verschiedene Containertypen passt.
- *Verschachtelte Verpackung* – Dimensionen für die verschachtelte Verpackung werden verwendet, wenn der Verpackungsprozess mehrere Ebenen umfasst.

*Lagerdimensionen* werden auch dann unterstützt, wenn die Funktion *Produktdimensionen für Verpackung* nicht aktiviert ist. Sie richten sie über die Seite **Physische Dimensionen** in Supply Chain Management ein. Diese Dimensionen werden von allen Prozessen verwendet, bei denen die Dimensionen Verpackung und verschachtelte Verpackung nicht angegeben sind.

Die Dimensionen *Verpackung* und *Verschachtelte Verpackung* werden über die Seite **Physische Produktdimensionen** eingerichtet, die hinzugefügt wird, wenn Sie die Funktion *Produktdimensionen für Verpackung* aktivieren.
Dieser Artikel enthält ein Szenario, das die Verwendung dieser Funktion veranschaulicht.

## <a name="turn-on-the-packaging-product-dimensions-feature"></a>Aktivieren der Funktion für Produktdimensionen für die Verpackung

Bevor Sie diese Funktion nutzen können, muss sie für Ihr System aktiviert werden. Administratoren können mit der Einstellung [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und ggf. aktivieren. Dort wird die Funktion folgendermaßen aufgelistet:

- **Module:** *Lagerortverwaltung*
- **Funktionsname:** *Produktdimensionen für Verpackung*

## <a name="example-scenario"></a>Beispielszenario

### <a name="set-up-the-scenario"></a>Szenario einrichten

Bevor Sie das Beispielszenario ausführen können, müssen Sie Ihr System wie in diesem Abschnitt beschrieben vorbereiten.

#### <a name="enable-demo-data"></a>Aktivieren der Demodaten

Um dieses Szenario mit den hier angegebenen Demodatensätzen und -werten durchzuarbeiten, müssen Sie ein System verwenden, auf dem die standardmäßigen [Demodaten](../../fin-ops-core/fin-ops/get-started/demo-data.md) installiert sind. Außerdem müssen Sie die *USMF* juristische Person auswählen, bevor Sie beginnen.

#### <a name="add-a-new-physical-dimension-to-a-product"></a>Hinzufügen einer neuen physischen Dimension zu einem Produkt

Fügen Sie eine neue physische Dimension für ein Produkt hinzu, indem Sie folgende Schritte ausführen:

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Wählen Sie das Produkt mit der **Artikelnummer** *A0001* aus.
1. Öffnen Sie im Aktionsbereich die Registerkarte **Bestand verwalten** und wählen Sie in der Gruppe **Lagerort** die Option **Physische Produktdimensionen** aus.
1. Die Seite **Physische Produktdimensionen** wird geöffnet. Wählen Sie im Aktionsbereich **Neu** aus, um dem Raster eine neue Dimension mit folgenden Einstellungen hinzuzufügen:
    - **Art der physischen Dimension** - *Verpackung*
    - **Physische Einheit** - *Stk.*
    - **Gewicht** - *4*
    - **Gewichtseinheit** - *kg*
    - **Tiefe** - *3*
    - **Höhe** - *4*
    - **Breite** - *3*
    - **Länge** - *cm*
    - **Volumeneinheit** - *cm3*

Der Wert im Feld **Volumen** wird automatisch basierend auf Ihren Einstellungen für **Tiefe**, **Höhe** und **Breite** berechnet.

#### <a name="create-a-new-container-type"></a>Einen neuen Containertyp erstellen

Wechseln Sie zu **Lagerortverwaltung \> Einrichten \> Container \> Containertypen** und erstellen Sie einen neuen Datensatz mit den folgenden Einstellungen:

- **Containertypcode** - *Kurzer Karton*
- **Beschreibung** - *Kurzer Karton*
- **Maximales Nettogewicht** - *50*
- **Volumen** - *144*
- **Länge** - *6*
- **Breite** - *6*
- **Höhe** - *4*

#### <a name="create-a-container-group"></a>Erstellen einer Containergruppe

Wechseln Sie zu **Lagerortverwaltung \> Einrichten \> Container \> Containergruppen** und erstellen Sie einen neuen Datensatz mit den folgenden Einstellungen:

- **Containergruppenkennung** - *Kurzer Karton*
- **Beschreibung** - *Kurzer Karton*

Fügen Sie eine neue Position zum Abschnitt **Details** hinzu. Legen Sie den **Containertyp** auf *Kurzer Karton* fest.

#### <a name="set-up-a-container-build-template"></a>Eine Containererstellungsvorlage einrichten

Wechseln Sie zu **Lagerortverwaltung \> Einrichten \> Container \> Containererstellungsvorlagen** und wählen Sie **Kartons** aus. Ändern Sie den Wert von **Containergruppenkennung** zu *Kurzer Karton*.

### <a name="run-the-scenario"></a>Ausführen des Szenarios

Nachdem Sie Ihr System wie im vorherigen Abschnitt beschrieben vorbereitet haben, können Sie das Szenario wie im nächsten Abschnitt beschrieben ausführen.

#### <a name="create-a-sales-order-and-create-a-shipment"></a>Erstellen eines Auftrags und einer Lieferung

In diesem Prozess erstellen Sie eine Lieferung basierend auf der Artikeldimension *Verpackung*, für die die Höhe weniger als 3 beträgt.

1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie im Dialogfeld **Auftrag erstellen** die folgenden Werte fest:

    - **Debitorenkonto:** *US-001*
    - **Lagerort:** *63*

1. Wählen Sie **OK** aus, um den Auftrag zu erstellen und das Dialogfeld zu schließen.
1. Der neue Auftrag wird geöffnet. Es sollte eine neue, leere Position im Raster auf dem Inforegister **Auftragspositionen** enthalten. Legen Sie die folgenden Werte für diese Position fest:

    - **Artikelnummer** *A001*
    - **Menge** *5*

1. Wählen Sie im Inforegister **Auftragspositionen** die Option **Bestand \> Reservierung** aus.
1. Wählen Sie auf der Seite **Reservierung** im Aktionsbereich die Option **Los reservieren** aus, um den Lagerbestand zu reservieren.
1. Schließen Sie die Seite.
1. Öffnen Sie im Aktionsbereich die Registerkarte **Lagerort** und wählen Sie **Lagerortfreigabe** aus, um Arbeit für den Lagerort zu erstellen.
1. Wechseln Sie auf dem Inforegister **Auftragspositionen** zu **Lagerort \> Lieferdetails**.
1. Öffnen Sie im Aktionsbereich die Registerkarte **Transport** und wählen Sie **Container anzeigen** aus. Bestätigen Sie, dass der Artikel in den zwei Containern *Kurzer Karton* verpackt wurde.

#### <a name="place-an-item-into-storage"></a>Platzieren eines Artikel im Lager

1. Öffnen Sie das Mobilgerät, melden Sie sich bei Warehouse 63 an und wechseln Sie zu **Bestand \> Anpassen in**.
1. Geben Sie **Loc** = *SHORT-01*. Erstellen Sie ein neues Kennzeichen mit **Artikel** = *A0001* und **Menge** = *1 Stk.*.
1. Wählen Sie **OK**. Die Fehlermeldung „Lagerplatz SHORT-01 ist fehlgeschlagen, da Artikel A0001 nicht zu den für den Lagerplatz angegebenen Dimensionen passt.“ wird angezeigt. Das liegt daran, dass die Dimensionen der Art *Lagerung* des Produkts größer sind als die im Lagerplatzprofil angegebenen Dimensionen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]