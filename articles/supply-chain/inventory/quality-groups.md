---
title: Artikelqualitätsgruppen
description: Dieser Artikel beschreibt die Verwendung und das Erstellen von Element-Qualitätsgruppen, um Produkte logisch zu gruppieren, so dass sie Qualitätsverbänden für die automatische Generierung von Qualitätsprüfungsaufträgen zugewiesen werden können.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestQualityGroup, InventTestItemQualityGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bf1ce49fa58fd1a8a5aa07636e0b2bd7e2fc10e4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875364"
---
# <a name="item-quality-groups"></a>Artikelqualitätsgruppen

[!include [banner](../includes/banner.md)]

Eine Qualitätsgruppe gibt Aufschluss über allgemeine Testanforderungen für Artikel. Dieser Artikel beschreibt die Verwendung und das Erstellen von Element-Qualitätsgruppen, um Produkte logisch zu gruppieren, so dass sie Qualitätsverbänden für die automatische Generierung von Qualitätsprüfungsaufträgen zugewiesen werden können.

Um die Elemente, die einer Qualitätsgruppe zugeordnet sind, oder die Qualitätsgruppen, die einem Element zugeordnet sind, einzurichten, zu bearbeiten und anzuzeigen, gehen Sie zu **Bestandsmanagement \> Einrichten \> Qualitätsgruppen**. Nachdem Sie die Testanforderungen auf der Seite **Testgruppen** definiert haben, können die Regeln für die automatische Generierung von Qualitätsprüfungsaufträgen definieren. Um den Prozess zu vereinfachen, definieren Sie keine Regeln für einzelne Elemente. Stattdessen können Sie die Regeln für eine Qualitätsgruppe auf der Seite **Qualitätszuordnungen** definieren.

## <a name="example-of-an-item-quality-group"></a>Beispiel für eine Element-Qualitätsgruppe

Ein Produktionsunternehmen erwirbt verschiedene Rohstoffe, bei denen die gleichen Testanforderungen zur Prüfung eingehender Waren gelten. Daher definiert die Firma eine Qualitätsgruppe und ordnet dieser Gruppe dann die Elementnummern zu, die mit den Rohstoffen verbunden sind. Später erwirbt das Unternehmen einen neuen Rohstofftyp, für den die gleichen Testanforderungen gelten. Anstatt neue Testanforderungen für den neuen Rohstoff einzurichten, fügt das Unternehmen die Artikelnummer neuen Materials der vorhandenen Qualitätsgruppe hinzu.

Dieselbe Firma produziert auch Elemente, die die gleichen Anforderungen an die Produktionstests haben und versendet Elemente, die die gleichen Anforderungen an die Tests vor dem Versand haben. Daher definiert die Firma zwei weitere Qualitätsgruppen und ordnet dann jeder Gruppe die entsprechenden Element-Nummern zu.

## <a name="create-a-quality-group"></a>Eine Qualitätsgruppe erstellen

Um eine Qualitätsgruppe zu erstellen, führen Sie diese Schritte aus.

1. Wechseln Sie zu **Inventarverwaltung \> Einrichten \> Qualitätskontrolle \> Qualitätsgruppen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen. Legen Sie für die neue Zeile die folgenden Felder fest:

    - **Qualitätsgruppe** – Geben Sie eine eindeutige ID oder einen Namen für die Qualitätsgruppe ein.
    - **Beschreibung** – Geben Sie eine detaillierte Beschreibung der Qualitätsgruppe ein.

1. Schließen Sie die Seite.

## <a name="manually-add-items-to-a-quality-group"></a>Manuelles Hinzufügen von Elementen zu einer Qualitätsgruppe

Um Elemente manuell zu einer Qualitätsgruppe hinzuzufügen, führen Sie diese Schritte aus.

1. Wechseln Sie zu **Inventarverwaltung \> Einrichten \> Qualitätskontrolle \> Qualitätsgruppen**.
1. Wählen Sie die Qualitätsgruppe aus, der Sie Elemente hinzufügen möchten.
1. Klicken Sie im Aktivitätsbereich auf **Artikel**.
1. Wählen Sie auf der Seite **Elemente in Qualitätsgruppen** im Aktivitätsbereich **Neu**, um dem Raster eine Zeile hinzuzufügen. Legen Sie dann für die neue Zeile das Feld **Artikelnummer** auf die Artikelnummer fest, die Sie hinzufügen möchten.
1. Wiederholen Sie den vorherigen Schritt für jedes zusätzliche Element, das hinzugefügt werden muss.
1. Schließen Sie die Seiten.

## <a name="add-multiple-items-to-a-quality-group"></a>Hinzufügen mehrerer Elemente zu einer Qualitätsgruppe

Um mehrere Elemente zu einer Qualitätsgruppe hinzuzufügen, führen Sie diese Schritte aus.

1. Wechseln Sie zu **Inventarverwaltung \> Einrichten \> Qualitätskontrolle \> Qualitätsgruppen**.
1. Erstellen oder wählen Sie die Qualitätsgruppe, zu der Sie Elemente hinzufügen möchten.
1. Klicken Sie im Aktivitätsbereich auf **Artikel hinzufügen**.
1. Geben Sie im Dialogfeld **Abfrage** die Filterkriterien für die Elemente ein, die Sie hinzufügen möchten. Sie könnten z. B. nach allen Elementen in einer bestimmten Elementgruppe filtern.
1. Wählen Sie **OK**.
1. Im Dialogfeld **Elemente hinzufügen** werden in einem Raster alle Elemente angezeigt, die Ihrer Abfrage entsprechen. Überprüfen Sie die Ergebnisse.

    Wenn Änderungen erforderlich sind, wählen Sie **Auswählen**, um zum Dialogfeld **Abfrage** zurückzukehren, und passen Sie Ihre Abfrage an.

1. Wenn die Ergebnisse alle Elemente enthalten, die Sie hinzufügen möchten, wählen Sie **OK**.
1. Schließen Sie die Seite.

## <a name="manually-associate-an-item-with-a-quality-group"></a>Manuelles Zuordnen eines Elements zu einer Qualitätsgruppe

Um ein Element manuell mit einer Qualitätsgruppe zu verknüpfen, folgen Sie diesen Schritten.

1. Gehen Sie zu **Bestandsverwaltung \> Einrichten \> Qualitätskontrolle \> Element-Qualitätsgruppen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen. Legen Sie für die neue Zeile die folgenden Felder fest:

    - **Elementnummer** – Wählen Sie die Elementnummer, die hinzugefügt werden soll.
    - **Qualitätsgruppe** – Wählen Sie die Qualitätsgruppe, die dem Element zugewiesen werden soll.

1. Wiederholen Sie den vorherigen Schritt für jede zusätzliche Kombination aus einem Element und einer Qualitätsgruppe, die hinzugefügt werden muss.
1. Schließen Sie die Seiten.

## <a name="manually-add-a-quality-group-from-the-released-products-page"></a>Manuelles Hinzufügen einer Qualitätsgruppe über die Seite Freigegebene Produkte

Um eine Qualitätsgruppe manuell von der Seite **Freigegebene Produkte** hinzuzufügen, gehen Sie wie folgt vor.

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Wählen Sie das Produkt, dem Sie eine Qualitätsgruppe zuweisen möchten.
1. Im Aktivitätsbereich, auf der Registerkarte **Lagerbestand verwalten**, in der Gruppe **Qualität**, wählen Sie **Qualitätsgruppen**.
1. Wählen Sie auf der Seite **Elemente in Qualitätsgruppen** im Aktivitätsbereich **Neu**, um dem Raster eine Zeile hinzuzufügen. Legen Sie dann für die neue Zeile das Feld **Qualitätsgruppe** auf die Qualitätsgruppe fest, die Sie dem Produkt zuweisen wollen.
1. Wiederholen Sie den vorherigen Schritt für jede zusätzliche Qualitätsgruppe, die Sie dem Produkt zuweisen wollen.
1. Schließen Sie die Seiten.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Qualitätsmanagement Testinstrumente](quality-test-instruments.md)
- [Qualitätsmanagement-Tests](quality-tests.md)
- [Qualitätsmanagement Testgruppen](quality-test-groups.md)
- [Qualitätsmanagement-Testvariablen](quality-test-variables.md)
- [Qualitätszuordnungen](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
