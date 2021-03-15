---
title: Funktionale Standorte erstellen
description: In diesem Thema wird erklärt, wie in der Anlagenverwaltung funktionalen Standorte erstellt werden.
author: josaw1
manager: tfehr
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationCopyStructure, EntAssetFunctionalLocationCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 81b5b81d7c318ba0a195dbc6324d700ccb8d39bf
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018220"
---
# <a name="create-functional-locations"></a>Funktionale Standorte erstellen

[!include [banner](../../includes/banner.md)]

 

In diesem Thema wird erklärt, wie in der Anlagenverwaltung funktionalen Standorte erstellt werden.

Wenn Sie eine funktionale Standortstruktur erstellen, können Sie diese nicht vom ursprünglichen Ort nicht verschieben. Das bedeutet, dass Sie die Struktur der funktionalen Standorte sorgfältig prüfen müssen, bevor Sie deren Erstellung in der Anlagenverwaltung starten. Wenn Sie einen funktionalen Standort nicht mehr möchten, können Sie ihn löschen, vorausgesetzt, dass er noch nicht in Verwendung ist

Um mit funktionalen Standorten zu arbeiten beginnen Sie, indem Sie zwei „Kategorien“ funktionale Standorte erstellen:

- Erstellen Sie *einen* funktionalen Standardstandort ohne Unterstandorten. Dieser funktionale Standort wird nur als funktionaler Standardstandort für Anlagen verwendet, wenn Sie neue Anlagen erstellen.  
- Erstellen Sie erforderliche funktionale Standortstruktur für die Verwaltung von Wartungsaufträgen in Ihrem Unternehmen.

## <a name="create-a-default-functional-location"></a>Erstellen eines standardmäßigen funktionalen Standortes

Wenn Sie funktionale Standorte verwenden, beginnen Sie mit dem Erstellen eines Standardstandortes, der verwendet wird, wenn Sie neue Anlagen erstellen. Dieser funktionale Standort ist jener, den Sie auswählen unter **Anlagenverwaltung** > **Einstellungen** > **Anlagenverwaltungparameter** > **Anlagen** Link > Feld **Funktionaler Standardstandort**. Der funktionale Standardstandort kann verwendet werden, wenn Sie neue Anlagen erstellen und Sie noch keine funktionale Standortstruktur für diese Anlagen eingerichtet haben.

1. Wählen Sie **Anlagenverwaltung** > **Allgemein** > **Funktionale Standorte** > **Alle funktionalen Standorte** aus.  
2. Wählen Sie **Alle funktionalen Standorte** wählen Sie **Neu** aus.
3. Geben Sie eine Kennung im Feld **Funktionaler Standort** ein, beispielsweise „0000“ oder „Standard“, um anzugeben, dass dies ein spezieller funktionaler Standort ist.
4. Hier können Sie Namen für den funktionalen Standort im Feld **Name** eingeben.
5. Wählen Sie *kein* übergeordnetes Element im Feld **Übergeordnet** – Lassen Sie dieses Feld leer.
6. Wählen Sie im Feld **Funktionaler Standorttyp** den funktionalen Standorttyp aus, der für den funktionalen Standardstandort verwendet wird. Weitere Informationen zum Einrichten von funktionalen Standorttyen finden Sie unter [Funktionale Standorttypen](../setup-for-functional-locations/functional-location-types.md).
7. Wählen Sie **OK**. Sie sollten keine weiteren Daten diesem funktionalen Standort hinzufügen, da er ausschließlich als temporärer Standort für neue Anlagen verwendet wird, bis Sie die Anlagen auf den funktionalen Standorten installiert haben, die Ihr Unternehmen verwendet.

## <a name="create-functional-locations"></a>Funktionale Standorte erstellen

Im Folgenden wird erläutert, wie Sie die funktionalen Standorte erstellen, die für Wartungsverwaltung in Ihrem Unternehmen erforderlich sind.

1. Wählen Sie **Anlagenverwaltung** > **Allgemein** > **Funktionale Standorte** > **Alle funktionalen Standorte** aus. Sie können einen funktionalen Standort in der Rasteransicht oder der Detailansicht erstellen.
2. Wählen Sie die Schaltfläche **Neu**.
3. Geben Sie eine Kennung im Feld **Funktionaler Standort** ein.
4. Hier können Sie einen Namen für den funktionalen Standort im Feld **Name** eingeben.
5. Wenn der Speicherort ein Unterstandort in einer Struktur ist, wählen Sie den übergeordneten Standort im Feld **Übergeordnet** aus.
6. Wählen Sie einen Typ im Feld **Funktionaler Standorttyp** aus.
7. Wählen Sie **OK**.
8. Wählen Sie den funktionalen Standort aus und klicken Sie auf die Schaltfläche **Bearbeiten**, um weitere Informationen hinzuzufügen.

>[!NOTE]
>Abhängig von Ihren Einstellungen der funktionalen Standortlebenszyklusstatus, müssen ggf. alle Unterlagerplätze für einen funktionalen Standort erstellt und dann der funktionale Standortlebenszyklusstatus geändert werden, bevor Sie mit dem Einrichten von Anlagen beginnen können. Unter[Einrichten von Anlagen auf funktionalen Standorten](../functional-locations/install-objects-on-functional-locations.md) finden Sie weitere Informationen zur Anlageninstallation. Siehe [Funktionaler Standortlebenszyklusstatus](../setup-for-functional-locations/functional-location-stages.md), um mehr über das Einrichten von Standortlebenszyklusstatus zu erfahren.

In der Detailansicht sehen Sie Inforegister, auf denen Sie Informationen zu den funktionalen Standorten hinzufügen und bearbeiten können.

## <a name="general-information"></a>Allgemeine Informationen

Dieser Abschnitt enthält eine Übersicht von übergeordneten und untergeordneten Informationen in der funktionalen Standortstruktur. Im Abschnitt **Details** können Sie die Anzahl von Anlagenattributen, Wartungsplänen und Anlagen finden, die dem funktionalen Standort zugeordnet werden. Im Abschnitt **Bestand** können Sie den Standort und der Lagerort auswählen, zu denen der funktionale Standort zugeordnet wird. Standort und Lagerort werden im Zusammenhang mit Arbeitsauftragsartikelplanungen verwendet. Wird eine Artikelplanung erstellt, werden Stand- und Lagerortinformationen dem funktionalen Standort der Anlage automatisch verwendet. Im Abschnitt **Lebenszyklusstatus** werden Informationen zum funktionalen Standortlebenszyklusstatus angezeigt.

## <a name="installed-assets"></a>Installierte Anlagen

Unter[Einrichten von Anlagen auf funktionalen Standorten](../functional-locations/install-objects-on-functional-locations.md) finden Sie weitere Informationen zur Anlageninstallation. Sie können die Schaltfläche **Ansicht** in diesem Bereich verwenden, um weitere Felder auf dem Inforegister anzuzeigen. Die Felder **Gültig ab** und **Unteranlage** können im Raster angezeigt werden.

## <a name="asset-attribute-requirements"></a>Anforderungen für Anlagenattribut

Auf diesem Inforegister können Sie bestimmte Attributanforderungen für die Anlagen hinzufügen, die Sie am funktionalen Standort einrichten möchten. Diese Anforderungen dienen nur zu Informationszwecken. Sie hindern Sie nicht daran, Anlagen mit anderen Attributanforderungen zu installieren. Wählen Sie **Position hinzufügen**, und wählen Sie den Attributtyp aus. Fügen Sie entsprechende **Wert** ein, wählen einen Schwellenwert im Feld **Schwellenwertkriterien** aus und speichern den Datensatz.

## <a name="maintenance-plans-and-maintenance-rounds"></a>Wartungspläne und Wartungsdurchgänge

Hier können Sie Wartungspläne und Wartungsdurchgänge den funktionalen Standorten einschließlich einem Startdatum hinzufügen. Die Anlagen, die auf einen funktionalen Standort installiert werden, verfügen möglicherweise über andere  Wartungsplaneinstellungen. Alle Wartungspläne und Wartungsdurchgänge können für die Planung von Anlagenkalendereinträgen für einen funktionalen Standort und die gerade eingerichteten Anlagen verwendet werden.

>[!NOTE]
>Wenn Sie die Einstellung der Anlagentypen, Anlagenmarken und Anlagenmodelle auf Wartungsplänen in der Detailansicht **Alle funktionalen Lagerplätze** auf dem Inforegister **Wartungspläne** aktualisieren, nachdem Sie den Wartungszeitplan geplant haben, werden bestehende Wartungsplaneinträge, die diesem funktionalen Standort zugeordnet werden, automatisch gelöscht. Wenn Sie neue Zeitplaneinträge erstellen, die dem aktualisierten Wartungsplan am funktionalen Standort entsprechen, müssen Sie einen neuen Wartungsplanzeitplan für diesen funktionalen Standort ausführen. 

## <a name="address"></a>Anschrift

Fügen Sie die funktionale Standortadresse auf dem Inforegister **Adresse** hinzu. Die Adressen der funktionalen Standorte werden übernommen, was bedeutet, dass wenn ein Unterstandort keine definierte Adresse hat, die Adresse des übergeordneten Standorts verwendet wird.

## <a name="workers"></a>Arbeitskräfte

Auf diesem Inforegister können Sie die Arbeitskräfte hinzufügen, die mit den funktionalen Standorten verknüpft werden, und Sie können einen funktionalen Ort als primären Ort für die Arbeitskraft auswählen. 

## <a name="attributes"></a>Attribute

Auf diesem Inforegister können Sie Werte für funktionale Standortattribute festlegen. Diese Attribute können verwendet werden, um zweckdienliche Eigenschaften oder Merkmale für den funktionalen Standort zu beschreiben, beispielsweise strukturelle Eigenschaften, Bauart, Bereichsbeschreibungen oder Standort über oder unter dem Boden.

Wählen Sie **Position hinzufügen**, und wählen Sie den Attributtyp aus. Danach fügen Sie den **Wert** ein, der mit dem Attributtyp verknüpft ist und speichern den Datensatz.

## <a name="financial-dimensions"></a>Finanzdimensionen

Sie können die Finanzdimensionen für den funktionalen Standort auswählen. [Funktionale Standorttypen](../setup-for-functional-locations/functional-location-types.md) können eingerichtet werden, um automatisch die Finanzdimensionen von einem funktionalen Standort zuzulassen. Das bedeutet, dass die Anlagen, die für eine Finanzdimension eingerichtet werden, automatisch die Finanzdimensionen den funktionalen Standort abrufen. Dies ist nützlich, wenn Sie verschiedene Kostenstellen möchten, abhängig von Standorten.

Wenn Daten bezüglich **Standort**, **Lagerort**, **Adresse** und **Finanzdimensionen** bei einem übergeordneten funktionalen Ort aktualisiert werden, können die zugehörigen funktionalen Unterstandorte entsprechend aktualisiert werden, wenn Sie diese Auswahl für die Aktualisierung durchführen. Ein Dialogfeld wird geöffnet und enthält die Aktualisierungsoptionen.

## <a name="copy-a-functional-location-structure"></a>Kopieren Sie eine funktionale Standortstruktur

Wenn Ihr Unternehmen mehrere funktionale Standorte mit ähnlicher Standortstrukturen hat, können Sie die Funktion in der Alageverwaltung kopieren, um schnell verschiedene Lagerplatzhierarchien zu erstellen. Wenn Sie einen bestimmten funktionalen Standort oder eine gesamte Struktur kopieren, hat der neue Standort oder Struktur den gleichen Namen, wie jenen, den Sie kopiert haben. Nach dem Kopieren können Sie den Namen oder andere Einstellungen für den neuen funktionalen Standort einfach ändern vorausgesetzt, dass der unktionale Standortlebenszyklusstatus für den neuen funktionalen Standort dies gestattet.

1. Wählen Sie unter **Alle funktionalen Standorte** den funktionalen Standort aus, den Sie kopieren möchten. Sie können beispielsweise einen Ort (übergeordnet) auswählen, wenn Sie die gesamte funktionale Standortstruktur einschließlich Unterstandorte kopieren möchten.
2. Aktivieren Sie die Schaltfläche **Funktionale Standortstruktur kopieren** aus. Der Standort, den Sie auf der Listenseite ausgewählt haben, wird im Feld **Kopieren von** angezeigt.
3. Fügen Sie den neuen Standort im Feld **Neuer funktionaler Standort** hinzu.
4. Im Feld **Übergeordnetes Element darunter einfügen** sollten Sie nur eine übergeordnete Kennung einfügen, wenn der Standort, den Sie erstellen, Teil einer vorhandenen funktionalen Standortstruktur sein soll.
5. Klicken Sie auf **OK**. Die neue funktionale Standortstruktur wird angezeigt unter **Alle funktionale Standorte**.

>[!NOTE]
>Wenn Sie eine funktionale Standortstruktur kopieren, werden die funktionalen Standortlebenszyklusstatus in der neuen Struktur auf den ersten Status festgelegt, den Sie für die funktionalen Standorte erstellt haben. Ob Sie einen funktionalen Standort mithilfe der Schaltflächen **Umbenennen** und **Löschen** in **Alle funktionalen Standorte** umbenennen oder löschen können, hängt vom aktuellen Lebenszyklus des funktionalen Standortes ab.

## <a name="delete-a-functional-location"></a>Einen funktionalen Standort löschen

Ein funktionaler Standort mit zugehörigen Unterstandorten kann gelöscht werden, wenn keine Anlagen auf einem der funktionalen Standorte eingerichtet wurden, die Sie löschen möchten und wenn der aktuelle funktionale Standortlebenszyklusstatus dies zulässt.

1. Wählen Sie unter **Alle funktionalen Standorte** den funktionalen Standort aus, den Sie löschen möchten.
2. Bei Bedarf aktualisieren Sie den funktionalen Standort an einen funktionalen Standortlebenszyklusstatus, der das Löschen eines funktionalen Standortes zulässt.
3. Wählen Sei **Löschen**.

>[!NOTE]
>Wenn Sie einen funktionalen Standort nicht löschen können, können Sie die Löschung vornehmen, indem Sie einen funktionalen Standortlebenszyklusstatus zu diesem Zweck einrichten. So können beispielsweise „ausrangierte“oder „gelöschte“ Phase, die über keine aktive Phase werden sollen, im Formular **Funktionale Standortlebenszyklusstatus** einrichten.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]