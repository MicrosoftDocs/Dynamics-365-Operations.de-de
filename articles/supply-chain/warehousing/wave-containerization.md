---
title: Containerisierung
description: In diesem Thema wird beschrieben, wie Containerisierung von Ladungen automatisiert wird. Die automatisierte Containerisierung erstellt Container und die Entnahmearbeit für Lieferungen, wenn eine Welle verarbeitet wird.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable, WHSContainerizatonHistory, WHSContainerPackingPolicyChange, WHSManifestShipmentContainers, WHSAllowedContainerTypeGroup, WHSPostMethod, WHSContainerCreateDialog, WHSContainerCloseDiag, WHSContainer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2f738c0404a41ef862d4985a170a0eba991e4dd4
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686625"
---
# <a name="containerization"></a>Containerisierung

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Containerisierung von Ladungen automatisiert wird. Die automatisierte Containerisierung erstellt Container und die Entnahmearbeit für Lieferungen, wenn eine Welle verarbeitet wird.

Um die Containerisierung zu aktivieren, müssen Sie Folgendes erstellen:

- **Containertyp** – Legen Sie die physischen Merkmale des Containers fest. Verwenden Sie Containertypen, um Lagerartikel in eine bestimmte Art und eine Größe von Verpackung zu verpacken, wie Lagerfächer oder Paletten.
- **Containergruppen** – Erstellen Sie Gruppen ähnlicher Containertypen. So kann eine Containergruppe Containertypen enthalten, die ähnliche Größendimensionen haben. Eine Containergruppe gibt die Reihenfolge an, in der Container verpackt werden, und den Füllprozentsatz jedes Containers.
- **Containererstellungsvorlage** – Erstellen Sie Vorlagen, die Regeln für die Containerisierung festlegen. Beispielsweise Regeln für das Kombinieren von Bestand und weiteren Verpackungsstrategien.
- **Wellenvorlagen** – Richten Sie eine oder mehrere Wellenvorlagen ein, um die Entnahmearbeit zur Containerisierung zu erstellen.

## <a name="create-wave-templates-for-containerization"></a>Wellenvorlage zur Containerisierung einrichten

Sie müssen eine oder mehrere Versandwellenvorlagen zur Containerisierung erstellen. Wellenvorlagen enthalten Kriterien, die Folgendes festlegen:

- Wie Wellen verarbeitet werden. Dies kann entweder manuell oder automatisch geschehen.
- Wie Entnahmearbeit erstellt wird. Dies wird durch die Wellenmethoden bestimmt. Die Wellenvorlage muss die **Containerisierungs**-Methode enthalten.
- Wie Artikel oder Zuteilungspositionen einer Welle zugeordnet werden.

Weitere Informationen finden Sie unter [Wellenvorlagen](wave-templates.md).

## <a name="create-container-types"></a>Neue Containertypen erstellen

Verwenden Sie Containertypen, um Beschreibungen von Containern zu erstellen, einschließlich maximale Werte für physische Größendimensionen und Gewichtskapazität. Wenn eine containerisierte Welle verarbeitet wird, werden die Container auf Basis der Containertypinformationen erstellt.

Gehen Sie zum Einrichten eines Containertyps folgendermaßen vor:

1. Wechseln Sie zu **Lagerortverwaltung** \> **Einstellungen** \> **Container** \> **Containertypen**.
1. Wählen Sie **Neu** aus, um einen neuen Containertyp zu erstellen.
1. Geben Sie eine eindeutige Kennung (ID) sowie eine Beschreibung für den Containertyp ein.
1. Geben Sie im Feld **Verpackungsgewicht** das tatsächliche oder vorkalkulierte Gewicht des Containers ein.
1. Geben Sie im Feld **Höchstgewicht** das Höchstgewicht an, das der Container fassen kann.
1. Legen Sie in den Feldern **Höchstvolumen für Containerisierung**, **Höchstlänge für Containerisierung**, **Höchstbreite für Containerisierung** und **Maximale Höhe für Containerisierung** die physischen Abmessungen des Containers an.

    > [!NOTE]
    > Die Werte für Länge und Breite sind austauschbar. Das bedeutet, dass Sie Artikel seitlich oder der X-Achse drehen können, falls erforderlich. Wenn beispielsweise die Länge 2 Meter beträgt, und die Breite ist 1 Meter, können Sie die Länge zu 1 Meter und die Breite auf 2 Meter ändern. Beachten Sie, dass dieses nicht für die Höhenabmessung gilt. Sie können den Höhenwert nicht ändern, um einen Artikel vertikal zu drehen.

1. Wählen Sie benutzerdefinierte Attributwerte für den Container in den Feldern für Attribute. Attribute sind benutzerdefinierte Werte, die verwendet werden, um Artikel auf Basis eines Werts zu filtern oder zu sortieren, der ansonsten nicht verfügbar ist. Wenn Sie zum Beispiel den Artikeln für einen bestimmten Debitor verpacken möchten, können Sie ein Attribut für den Debitorennamen erstellen. Attributtypen werden auf der Seite **Containerattribute** erstellt.

## <a name="create-container-groups"></a>Containergruppen erstellen

Sie können logische Gruppen von Containertypen einrichten. Für jede Gruppe können Sie die Reihenfolge angaben, in der die Container verpackt werden, und den Prozentsatz der zu füllenden Container. Die Größendimensionen des Artikels bestimmen, ob er in einen Container passt. Der Container, der den Größendimensionen des Artikels am nächsten liegt, wird verwendet. Wenn Sie mehrere Container in einer Gruppe haben, empfiehlt es sich, die Reihenfolge nach Größe anzuordnen, sodass der größte Container der erste ist, Nummer 1 in der Reihenfolge, und der kleinste Container der letzte ist.

Gehen Sie zum Einrichten einer Containergruppe folgendermaßen vor:

1. Wechseln Sie zu **Lagerortverwaltung** \> **Einstellungen** \> **Container** \> **Containergruppen**.
1. Wählen Sie **Neu** aus, um eine neue Containergruppe zu erstellen.
1. Geben Sie eine eindeutige Kennung (ID) sowie eine Beschreibung für die Containergruppe ein.
1. Klicken Sie auf dem Inforegister **Details** auf **Neu**, um der Gruppe einen Containertyp zuzuordnen.
1. Wählen Sie im Feld **Containertyp** einen Containertyp aus.
1. Wählen Sie **Nach oben** oder **Nach unten**, um die Reihenfolge anzugeben, in der die Containertypen gepackt werden.

## <a name="create-container-build-templates"></a>Eine neue Containererstellungsvorlage erstellen

Sie können Regeln für den Containerisierungsprozess einrichten, wie Bestandsmixingregeln und andere Verpackungsstrategien. So können Sie beispielsweise eine Regel einrichten, dass Arbeitskräfte Zuteilungspositionen nicht verpacken können, die Aufträge von verschiedenen Debitoren im gleichen Container darstellen.

Gehen Sie zum Einrichten einer Containererstellungsvorlage folgendermaßen vor.

1. Wechseln Sie zu **Lagerortverwaltung** \> **Einstellungen** \> **Container** \> **Containererstellungsvorlage**.
1. Erstellen Sie eine neue Containererstellungsvorlage.
1. Geben Sie in den Feldern **Containerisierungsname** und **Sequenznummer** den Namen der Containerisierungsvorlage und den Auftrag ein, der Verteilungspositionen zugeordnet ist.

    > [!NOTE]
    > Das System wendet die erste Vorlage an, für die die Zuteilungsposition die Abfragekriterien erfüllt. Es wird daher empfohlen, die Vorlage mit den spezifischsten Kriterien an den Anfang der Liste zu setzen. Je breiter die Kriterien, desto wahrscheinlicher ist es, dass eine Zuteilungsposition die Kriterien erfüllt. Dies kann dazu führen, dass Positionen dem falschen Container zugeordnet werden. Bei Bedarf können Sie die Reihenfolge der Vorlagen mit **Nach oben** oder **Nach unten** ändern.

1. Wählen Sie im Feld **Containergruppenkennung** die Containergruppe aus, aus der Container erstellt werden sollen.
1. Wählen Sie im Feld **Basisabfragetypen** den Abfragetyp aus, der bestimmt, was verpackt wird und worauf die Filterabfrage basieren soll. Die folgenden Optionen stehen zur Verfügung:

      - **Auftragszuteilungsposition** – Verpackungszuteilungspositionen, die für Aufträge erstellt werden.
      - **Übertragungszuteilungsposition** – Verpackungszuteilungspositionen, die für Übertragungen erstellt werden.
      - **Container** – Beladen eines Containers, der bereits über den Containerisierungsprozess erstellt wurde. Beispielsweise wird dieses für das Verschachteln von Containern verwendet.

        > [!NOTE]
        > Um die Verschachtelungsmethode für Container zu verwenden, müssen Sie die Containerisierungsmethode wiederholbar machen. Weitere Informationen finden Sie unter [Wellenvorlagen](wave-templates.md).

1. Geben Sie im Inforegister **Allgemein** im Feld **Wellenschrittcode** die eindeutige Kennung der Wellenprozessmethode ein, die die Containererstellungsvorlage mit den Schritten in einer Wellenvorlage verknüpft.
1. Aktivieren Sie das Kontrollkästchen **Geteilte Entnahme zulassen**, um Arbeitskräften zu ermöglichen, Artikel von einem Arbeitsauftrag in separaten Containern zu verpacken. Dies erfordert, dass die gesamte Mengenpassung in den Container passt. Die größte Maßeinheit in der Zuteilungsposition wird immer verwendet.
1. Wählen Sie im Feld **Nach Einheit verpacken** die Maßeinheit, die den Container repräsentiert. Beispielsweise können Sie angeben, dass ein Behälter ein Container ist. Wenn Sie nach Maßeinheit verpacken, können Sie auch eine Containergruppe angeben, da die Maßeinheit der Container ist.
1. Wählen Sie im Feld **Containerverpackungsstrategie** die zu verwendende Verpackungsstrategie aus. Die folgenden Optionen stehen zur Verfügung:

    > [!NOTE]
    > Die Strategie gilt nur für Vertriebszuteilungspositionen und Übertragungszuteilungspositionen.

      - **In alle offenen Container verpacken** – Das System wertet aus, ob die Zuteilungsposition in einen Container passt, der während des Containerisierungszyklus erstellt wurde.
      - **Nur in aktuellen Container verpacken** – Das System wertet nur aus, ob die Zuteilungsposition in den zuletzt erstellten Container passt.

    Weitere Informationen und Beispiele, die das Arbeiten mit Container-Packstrategien zeigen, finden Sie unter [Container-Packstrategien](container-packing-strategy-overview.md).

1. Wählen Sie **Mischlogikpausen aus**, um Regeln für das Verpacken von Zuteilungspositionen in Containern einzurichten. So können Sie beispielsweise eine Regel erstellen, die Arbeitskräften erlaubt, Zuteilungspositionen für zwei unterschiedliche Artikel im gleichen Container zu verpacken. Gehen Sie folgendermaßen vor, um eine Mischungsregel zu erstellen:

    1. Wählen Sie auf der Seite **Mischlogikpausen** **Neu** aus.
    1. Wählen Sie im Feld **Tabelle** die Tabelle aus, die das Feld enthält, das das Kriterium für die Mischlogikpause zu verwenden ist.
    1. Wählen Sie im Feld **Feld auswählen** das Feld aus, das das Kriterium für die Mischlogikpause zu verwenden ist.
    1. Wiederholen Sie diese Schritte, bis Sie alle Kriterien für die Mischlogikpause hinzugefügt haben.

    > [!NOTE]
    > Wenn Sie Mischlogik verwenden, empfiehlt es sich, nach den gleichen Felder in der Filterkriterienabfrage zu sortieren. Dieses verringert die Anzahl an Containern, die erstellt werden.
