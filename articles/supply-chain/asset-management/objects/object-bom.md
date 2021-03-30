---
title: Anlagenstücklisten
description: In diesem Thema werden die Anlagenstücklisten (BOMs) in Asset Management beschrieben.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetStandardSparePartsItemGroup, EntAssetObjectBOM
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4e5d6d6245f27534d176ac03ca762aff91afb0ca
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253181"
---
# <a name="asset-boms"></a>Anlagenstücklisten

[!include [banner](../../includes/banner.md)]

 

In diesem Thema werden die Anlagenstücklisten (BOMs) in Asset Management beschrieben. Die Seite **Anlagenstückliste** zeigt eine Liste sämtlicher Artikel an (Ersatzteilen und andere Artikel), die während der gesamten Lebensdauer einer Anlage verwendet werden. Wenn Sie eine neue Anlage erstellen, sollen Sie die Einrichtung einer Anlagenstückliste als Teil des Einrichtungsverfahrens in Betracht ziehen. Auf diese Weise können Sie Artikelhistorie für die Anlage ab dem Erstellungsdatum verfolgen.

Nachdem Sie einen Wartungsauftrag abgeschlossen haben und der Artikelverbrauch für einen Arbeitsauftrag erfasst wurde, können Sie den Verbrauch von Ersatzteilen und anderen Artikeln verfolgen, die für die Anlage verwendet werden. Durch diese Funktion können Sie einen vollständigen Artikelverbrauchsdatensatz für alle Anlagen verwalten. Sie können den Datensatz beispielsweise verwenden, um zu überprüfen, ob ein bestimmtes Ersatzteil häufig ersetzt wird, oder um die Ersatzteile oder andere Artikel zu verfolgen, die gegenwärtig in einer Anlage verwendet werden.

> [!NOTE]
> Bei einem Arbeitsauftrag zählen zum Artikelverbrauch möglicherweise sowohl Ersatzteilen als auch andere zusätzliche Artikel wie Bolzen, Schmierstoffe und Dichtungen.

Eine Anlagenstückliste kann basierend auf den Einstellungen in Asset Management automatisch aktualisiert werden. Wenn ein Arbeitsauftrags-Lebenszyklusstatus erstellt wurde, um beendete oder abgeschlossene Arbeitsaufträge zu behandeln, und wenn die Option **Anlagenstückliste aktualisieren** für diesen Arbeitsauftrags-Lebenszyklusstatus auf der Seite **Arbeitsauftrag-Lebenszyklusstatus** auf **Ja** festgelegt ist, werden alle im Arbeitsauftrag verwendeten Artikel automatisch auf der Seite **Anlagenstückliste** aktualisiert, wenn der Arbeitsauftrag auf diesen Lebenszyklusstatus aktualisiert wird. 


Sie können eine Anlagenstückliste auch manuell aktualisieren, indem Sie neue Positionen auf der Seite **Anlagenstückliste** erstellen.

Auf der Seite **Anlagenstückliste** können Sie die Ersatzteilhistorie für eine Anlage verfolgen, nachdem der Artikelverbrauch für einen Arbeitsauftrag erfasst wurde. Um diese Funktion verwenden zu können, müssen Sie die Artikelgruppen auswählen, die für die Ersatzteilerfassung auf der Seite **Ersatzteilartikelgruppen** verwendet werden sollen.

Um die Anlagenstücklistenfunktion zu verwenden, müssen Sie zuerst die erforderlichen Ersatzteilartikelgruppen einrichten. Wenn die Anlagenstückliste automatisch aktualisiert werden soll, nachdem ein Arbeitsauftrag abgeschlossen wurde, können Sie dann einen Arbeitsauftrags-Lebenszyklusstatus einrichten, der diese Aktualisierung behandelt. 


## <a name="set-up-spare-parts-item-groups"></a>Ersatzteilartikelgruppen einrichten

Die Einrichtung der Ersatzteilhistorie basiert auf Artikelgruppen, die im Modul **Lager- und Lagerortverwaltung** erstellt werden. In Asset Management richten Sie Artikelgruppen ein, sodass Sie die Ersatzteilhistorie für Artikel in den ausgewählten Artikelgruppen verfolgen können.

1. Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Anlage** \> **Ersatzteilartikelgruppen** aus.
2. Wählen Sie **Neu**, um eine Artikelgruppe einzurichten.
3. Wählen Sie im Feld **Artikelgruppe** die Gruppe aus. Der Name der Gruppe wird automatisch in das Feld **Name** eingetragen.

## <a name="view-and-update-asset-boms"></a>Anlagenstücklisten anzeigen und aktualisieren

Nachdem Sie den Artikelverbrauch für einen Arbeitsauftrag gebucht haben, können Sie den Erfassten Artikelverbrauch auf der Seite **Anlagenstückliste** anzeigen.

1. Wählen Sie **Anlagenverwaltung** \> **Allgemeines** \> **Anlagen** \> **Aktive Anlagen**. Wählen Sie die Anlage in der Liste aus, und wählen Sie dann **Anlagenstückliste** aus.

    > [!NOTE]
    > Um den gesamten Artikelverbrauch für alle Anlagen anzuzeigen, wählen Sie **Anlagenverwaltung** \> **Abfragen** \> **Anlagen** \> **Anlagenstückliste** aus.

2. Wählen Sie **Anlagenstückliste aktualisieren** aus. Sie können bei Bedarf Anlagen, Anlagentypen und Ressourcen zur Aktualisierung hinzufügen, indem Sie **Auswählen** wählen. Klicken Sie auf **OK**, um die Aktualisierung zu starten. Sie können die Aktualisierungsfunktion auch als Stapelverarbeitungsauftrag einrichten.
3. Wenn Sie weitere Informationen anzeigen möchten, die sich auf Artikel beziehen, können Sie Bestandsdimensionen hinzufügen. Wählen Sie **Bestand** \> **Dimensionenanzeige** aus, und aktivieren Sie anschließend die Kontrollkästchen für die Dimensionen, die Sie anzeigen möchten. Um diese Einstellung für alle Anlagen auf der Seite **Anlagenstückliste** beizubehalten, legen Sie die Option **Einstellungen speichern** auf **Ja** fest.
4. Um einen Überblick darüber zu erhalten, wo in Asset Management der Artikel in der ausgewählten Position verwendet wird, in Bezug auf Anlagen, Auftragstypstandards, Ersatzteile und Arbeitsaufträge, wählen Sie die Option **Artikel, die verwendet wurden**. 
5. Wenn Sie nur aktive Artikelpositionen anzeigen möchten, wählen Sie **Ansicht** \> **Aktuell** aus. Um sämtliche Artikelpositionen anzuzeigen, einschließlich der Positionen, bei denen das Ablaufdatum vor dem aktuellen Datum liegt, wählen Sie **Ansicht** \> **Alle** aus.

> [!NOTE]
> Wenn Sie einen Arbeitsauftrag abgeschlossen haben und einige Artikel oder Ersatzteile, die der zugeordneten Anlage angehören, bereits abgelaufen sind oder durch andere Artikel oder Ersatzteile ersetzt wurden, wird empfohlen, dass Sie die Anlagenstückliste entsprechend aktualisieren.

## <a name="create-a-new-item-line-in-an-asset-bom"></a>Neue Artikelposition in einer Anlagenstückliste erstellen

Sie können Artikelpositionen für Anlagen manuell erstellen.

1. Wählen Sie auf der Seite **Anlagenstückliste** die Option **Neu** aus.
2. Wählen Sie im Feld **Anlage** die Anlage aus, der Sie eine Artikelposition hinzuzufügen möchten.
3. Geben Sie im Feld **Positionsnummer** eine Zahl ein.
4. Geben Sie im Feld **Gültig** ein Startdatum für den Artikel ein.
5. Wenn der Artikel ablaufen soll, geben Sie im Feld **Ablauf** ein Enddatum ein.
6. Wählen Sie im Feld **Artikelnummer** den Artikel aus. Der Name wird automatisch in das Feld **Produktname** eingetragen.
7. Geben Sie im Feld **Menge** die verwendete Menge ein. Das Feld **Einheit** wird automatisch aktualisiert.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]