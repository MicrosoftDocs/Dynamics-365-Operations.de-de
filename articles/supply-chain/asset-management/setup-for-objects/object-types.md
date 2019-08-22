---
title: Anlagentypen
description: In diesem Thema wird erläutert, wie Sie in Anlagetypen in der Anlageverwaltung erstellen. Außerdem werden die Elemente beschrieben, die den Anlagentypen zugeordnet werden.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 288dac77f9d999012ec930ef2bca5c0921c2955f
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783298"
---
# <a name="asset-types"></a>Anlagentypen

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Dieses Thema erläutert, wie Sie Anlagetypen erstellen. Außerdem werden die Elemente beschrieben, die den Anlagentypen zugeordnet werden. Anlagentypen werden als allgemeinen Kategorien für Anlagen verwendet. Hierzu gehören CNC-Maschinen, Messausrüstung und Lkw-Motoren. Anlagentypen werden verwendet, um die Stellentypen zu verwalten (Wartungsanlagen), Anlagen-Lebenszyklusstatus, Anlageattribute, Bedingungsbewertungsvorlagen und Anlagemodelle, die als Anlage ausgewählt werden können. Wenn Sie eine Anlage erstellen, muss der Anlagetyp für angegeben.

Für jeden Anlagentyp können Abweichungen der Anlagentypeinstellung erstellt werden. Wenn Sie beispielsweise einen Anlagentyp haben, der **„LKW“** ist, können Sie für diesen Anlagentyp Abweichungen für verschiedene Anlagenhersteller und Anlagenmodelle erstellen. Für jede Anlagentypeinstellung können Sie die erforderlichen Ersatzteile und Wartungspläne Ersatzteilen hinzufügen.

Zuerst richten Sie die erforderlichen Anlagentypen ein. Anschließend erstellen Sie die Anlagenmodelle, die den bereitgestellten Anlagentypen zugeordnet werden sollen. Schließlich erstellen Sie auf der Seite **Anlagentypstandards** alle Abweichungen für Anlagentypen, die für Ihre Ausrüstung erforderlich sind.

## <a name="create-an-asset-type"></a>Einen Anlagetyp erstellen

1. Wählen Sie **Anlageverwaltung** \> **Einstellungen** \> **Anlagentypen** \> **Anlagentypen** aus.
2. Wählen Sie **Neu**, um ein Anlagentyp zu erstellen.
3. Im Feld **Anlagentyp** geben Sie eine Kennung für den Anlagentyp ein
4. Geben Sie im Feld **Name** einen Namen ein.
5. Wählen Sie ein Anlage-Lebenszyklusmodell im Feld **Anlage-Lebenszyklusmodell** aus. Weitere Informationen zu Anlagenlebenszyklus und Anlagenlebenszyklusmodelle, finden Sie unter [Anlagen-Lebenszyklusstatus](object-stages.md).
6. Hier können Sie die Option **Summe** auf **Ja** festlegen, wenn die zusammengefassten Leistungskennzahlwerte (KPI) für Anlagen berechnet werden sollen, die diesen Anlagentyp haben.
7. Wählen Sie **Speichern**.
8. Wählen Sie im Inforegister **Stellentypen** die Stellentypen aus, die dem Anlagentyp zugeordnet werden sollen:

    - Um einen Stellentyp auszuwählen wählen Sie ihn im Feld **Verbleibende Stellentypen** aus, und wählen Sie dann die Schaltfläche mit dem Pfeil nach rechts ![ Pfeil nach rechts](media/29-setup-for-objects.png), um ihn in den Bereich **ausgewählter Stellentyp** zu verschieben.
    - Um alle verfügbaren Stellentypen auswählen, wählen Sie Schaltfläche ![alle Pfeil weiter](media/30-setup-for-objects.png) aus. Alle Stellentypen werden aus dem Feld **verbleibende Stellentypen** in das Feld **ausgewählte Stellentypen** übertragen.
    - Um die Auswahl eines Stellentyps zu löschen, wählen Sie ihn im Feld **Ausgewählte Stellentypen** aus, und wählen Sie dann die Schaltfläche mit dem Pfeil nach links ![ Pfeil nach links](media/31-setup-for-objects.png), um ihn in den Bereich **Verbleibende Stellentypen** zu verschieben.

9. Sie können auch die Anlagemessungen auswählen, die dem Anlagentyp zugeordnet werden sollen. Auf dem Inforegister **Anlagenmessungen** aktivieren Sie Ihre Auswahl, indem Sie die Methoden für Stellentypen, die in Schritt 8 beschrieben werden anwenden. Weitere Informationen zum Einrichten von Anlagenmessungen finden Sie unter[Anlagenmessungen verwalten](counters.md).
10. Sie können auch die Attributtypen auswählen, die dem Anlagentyp zugeordnet werden sollen. Auf dem Inforegister **Attributtypen** aktivieren Sie Ihre Auswahl, indem Sie die Methoden für Stellentypen anwenden, die in Schritt 8 beschrieben werden. Um dann die bevorzugten Reihenfolge der Attributtypen zu erstellen, wählen Sie im Feld **Attributtypen ausgewählt** den Attributtyp aus, und verwenden Sie die NACH-OBEN-TASTE und die NACH-UNTEN-TASTE, um sie zu verschieben. Die Sequenz der Attributtypen wird auf Anlagen angezeigt, die diesen Anlagentyp verwenden. Weitere Informationen zu Anlagenattributen finden Sie unter [Attributtypen verwalten](../setup-for-functional-locations/specification-types.md).

    > [!NOTE]
    > Wenn Sie neue Attributtypen dem Inforegister**Attributtypen** hinzufügen, werden bestehende Anlagen automatisch mit diesen Informationen aktualisiert.

11. Sie können auch die Bedingungsbewertungsvorlagen auswählen, die dem Anlagentyp zugeordnet werden sollen. Auf dem Inforegister **Bedingungsbewertung** aktivieren Sie Ihre Auswahl, indem Sie die Methoden für Stellentypen anwenden, die in Schritt 8 beschrieben werden. Weitere Informationen zu Bedingungsbewertungsvorlagen und - erfassungen, finden Sie unter [Bedingungsbewertung](../setup-for-objects/condition-assessment.md)
12. Das Inforegister **Anlagenmodell** zeigt alle Kombinationen von Anlagenherstellern und die Modelle an, die im ausgewählten Anlagentyp eingerichtet werden. Um die Kombinationen anzuzeigen, die gemäß dem Hersteller aufgeteilt sind, wählen Sie **Anlagenmodell**, um die Seite **Anlagenmodell** zu öffnen.

    Auf der Seite **Anlagenmodell** können Sie Anlagenmodell-Anlagentyprelationen hinzufügen. Darüber hinaus können Sie auf der Seite **Anlagentypen** die Anlagenhersteller-Anlagen-Modellrelationen direkt einem Anlagentyp hinzufügen. Schließlich können Sie auf der Seite **Anlagenmodell** (**Anlagenverwaltung** \> **Einstellungen** \> **Anlagen** \> **Anlagenmodell**) die Anlagenhersteller-Anlagenmodell-Anlagentyprelationen neu erstellen. Daher gibt es drei Möglichkeiten, Anlagenhersteller-Anlagenmodell-Anlagentyprelationen einzurichten und zu bearbeiten. Alle verfügbaren Kombinationen werden aus unterschiedlichen Perspektiven dargestellt, und Sie können Ihre bevorzugte Eingangsstelle auswählen, wenn Sie mit der Einstellung arbeiten.

> [!NOTE]
> - Wenn Sie Anlagenmessungen für eine Anlage auswählen, wird die Auswahl automatisch aktualisiert auf der Seite **Anlagenmessungen**(**Anlagenverwaltung)** \> **Einstellungen** \> **Anlagen** \> **Anlagentypen** \> **Anlagenmessungen**.
> - Die Felder im Abschnitt **Details** auf dem Inforegister **Allgemeines** zeigt die Anzahl für Stellentypen, Anlagenmessungen, Attribute usw. an, die im Feld ausgewählter Anlagentyp eingerichtet werden.

Normalerweise werden Arbeitsaufträge, die manuell erstellt werden, der Fehlerwartung zugeordnet, während Arbeitsaufträge, die automatisch erstellt werden, der vorbeugenden Verwaltung zugeordnet werden. Wenn Sie manuell Arbeitsaufträge erstellen, werden können nur die Stellentypen verwendet werden, die auf dem Inforegister **Stellentypen** der Seite **Anlagentypen** aktiviert sind. Allerdings können automatisch erstellte Arbeitsaufträge alle Stellentypen verwenden, die Sie auf der Seite **Stellentypen** (**Anlagenverwaltung** \> **Einstellungen** \> **Steellen** \> **Stellentypen**) erstellt haben.

## <a name="create-asset-type-setup-lines"></a>Erstellen von Positionen für Anlagetypen

1. Wählen Sie **Anlageverwaltung** \> **Einstellungen** \> **Anlagen** \> **Anlagentypen** \> **Anlagentypen einrichten** aus. Aktivieren Sie alternativ **Anlagenverwaltung** \> **Einstellungen** \> **Anlagen** \> **Anlagentypen** \> **Anlagentypen** aus und wählen Sie einen Anlagentyp aus, und wählen Sie dann **Anlagentypeinstellung**.
2. Beim erstmaligen Verwenden von **Anlagentypeinstellung** finden Sie möglicherweise die Schaltfläche **Kombinationen erstellen** hilfreich. Sie können diese Schaltfläche verwenden, um alle Kombinationen eines Anlagenmodells auf einem Anlagentyp schnell zu erstellen. Wählen Sie **Kombinationen erstellen** aus, wählen Sie den Anlagentyp aus, um Kombinationen zu erstellen, und wählen Sie dann **OK**.

    > [!NOTE]
    > Wenn Sie nicht alle Anlagentyp-Einrichtungskombinationen verwenden, die automatisch erstellt wurden, können sie eine Einrichtung löschen, indem Sie diese auswählen und dann **Löschen** wählen.

3. Wählen Sie **Neu**, um einen Anlagentyp manuell einzurichten.
4. Abhängig davon, wie die Anlagentypeinstellung sein soll, treffen Sie eine Auswahl auf **Anlagentyp**, **Hersteller** und **Modell**
5. Wenn eine Garantievereinbarung dem Anlagentyp zugeordnet ist, wählen Sie die Vereinbarung in den Feldern **Kreditorengarantie** und **Debitorengarantie**. 
6. Auf dem Inforegister **Ersatzteile** aktivieren Sie **Hinzufügen**, um der ausgewählten Anlagentypeinstellung Ersatzteile hinzuzufügen.
7. Um ein Ersatzteil zu genehmigen, wählen Sie die Ersatzteilposition, und wählen Sie dann **Genehmigen**. Sie können mehrere Positionen zur Genehmigung auswählen.
8. Um zu sehen, ob ein Ersatzteil an anderer Stelle in der Anlagenverwaltung verwendet wird (beispielsweise in Verbindung mit Anlagen und Arbeitsaufträge), wählen Sie die Ersatzteilposition, und wählen Sie dann **Artikel, die verwendet wurden**, um die Seite **Artikel, die verwendet wurden** zu öffnen. Um alle aktiven Ersatzteile in der Liste anzuzeigen, aktivieren Sie das Kontrollkästchen **Aktiv**. Um nur genehmigte Ersatzteilen anzuzeigen, aktivieren Sie das Kontrollkästchen **Genehmigt**.
9. Auf dem Inforegister **Wartungsplan** aktivieren Sie **Hinzufügen**, um der ausgewählten Anlagentypeinstellung Wartungspläne hinzuzufügen.
10. Um einen Anlagentyp zu kopieren, der für eine andere Einstellung festgelegt wurde, können Sie die Kopierfunktion verwenden. Wählen Sie die Anlagentypeinstellung aus, um eine Einstellung zu kopieren, wählen Sie **Einstellungen kopieren** und wählen Sie die Anlagentypeinstellung aus, von der die Einstellungen kopiert werden sollen. Die Einstellungen der verschiedenen Optionen bestimmen, wie viele Informationen enthalten sind. Wenn Sie fertig sind, wählen Sie **OK**, um die Einstellungen zu kopieren.

> [!NOTE]
> Wenn Sie viele Ersatzteilpositionen und Wartungsplanpositionen haben, die Sie wiederverwenden, ermöglicht die Kopierfunktion schnell und einfach, die Daten für viele Anlagentyp-Einstellungskombinationen einzurichten.

## <a name="spare-parts-on-the-asset-type-setup"></a>Ersatzteilen für die Anlagentypeinstellung

Wie im Abschnitt „Anlagentypeinstellungs-Position erstellen“ beschrieben, werden Ersatzteile auf Anlagenmodellen auf der Seite **Anlagentypeinstellung** installiert. Wenn Sie die Seite **Anlagentypeinstellung** öffnen, sehen Sie nur die Ersatzteile, die der ausgewählten Kombination eines Anlagentyps, Anlagenherstellers und Anlagenmodells zugeordnet werden. Um eine Liste aller Ersatzteildatensätze anzuzeigen, öffnen Sie die Seite**Ersatzteile** (**Anlagenverwaltung** \> **Abfragen** \> **Ersatzteile**).

Auf der Seite **Ersatzteile** können Sie neue Ersatzteile für vorhandene Kombinationen eines Anlagentyps, Anlagenherstellers und Anlagenmodells erstellen. Sie können entscheiden, ob Sie lieber Ersatzteildatensätze auf der Seite **Anlagentypeinstellung** oder der Seite **Ersatzteilen** erstellen. Die Seite **Anlagentypeinstellung** enthält eine Übersicht von Daten für die ausgewählte Kombination eines Anlagentyps, Anlagenherstellers und Anlagenmodells, während die Seite**Ersatzteile** eine vollständige Übersicht über alle Anlagentyppositionen enthält. Wenn die Seite **Ersatzteile** viele Datensätze enthält, könnte die Seite **Anlagentypeinstellung** Ihnen einen besseren Überblick geben.

Um zu sehen, ob ein Ersatzteil auf der ausgewählten Position an anderer Stelle in der Anlagenverwaltung verwendet wird (beispielsweise in Verbindung mit Anlagen und Arbeitsaufträge), wählen Sie die Ersatzteilposition, und wählen Sie dann **Artikel, die verwendet wurden**, um die Seite **Artikel, die verwendet wurden** zu öffnen. 

