---
title: Erstellte XML-Dateien auf Grundlage der Dateigröße und Inhaltsmenge teilen
description: Dieses Thema enthält Informationen darüber, wie Sie generierte Dateien anhand der Dateigröße und der Anzahl der Inhaltselemente aufteilen können.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 8c3899d5c6602b3afe13b447b40f0b4dcc701448
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "347099"
---
# <a name="split-generated-xml-files-based-on-file-size-and-content-quantity"></a>Erstellte XML-Dateien auf Grundlage der Dateigröße und Inhaltsmenge teilen

[!include[banner](../includes/banner.md)]

Sie können Elektronische Berichterstellung(ER)-Formate entwerfen, um ausgehende Dokumente im XML-Format zu generieren. Manchmal können diese Dokumente nur akzeptiert werden, wenn sie bestimmte Kriterien erfüllen, wie z.B. eine maximale Dateigröße oder eine maximale Anzahl von XML-Knoten. Sie können ER-Formate entwerfen, um elektronische Dokumente zu erzeugen, die den Anforderungen der Empfänger dieser Dokumente entsprechen.

- Für das Formatelement FILE können Sie eine Begrenzung der Dateigröße als ER-Ausdruck definieren. Wenn die definierte Grenze bei der Erstellung eines ER-Berichts überschritten wird, beendet ER die Erstellung der aktuellen Datei und fährt dann mit der Erstellung der nächsten Datei fort.
- Für jedes XML-ELEMENT-Format können Sie eine Begrenzung der Anzahl der Elemente als ER-Ausdruck definieren. Wenn die Anzahl der XML-Knoten in der erzeugten Datei beim Ausführen eines ER-Berichts die definierte Grenze überschreitet, beendet ER die Erstellung der aktuellen Datei und fährt dann mit der Erstellung der nächsten Datei fort.
- Für jedes XML SEQUENCE-Formatelement können Sie eine Begrenzung der Anzahl der untergeordneten Elemente als ER-Ausdruck definieren. Wenn die Anzahl der geschachtelten XML-Knoten des Formatelements in der generierten Datei die definierte Grenze überschreitet, wenn ein ER-Bericht ausgeführt wird, beendet ER die Erstellung der aktuellen Datei und fährt dann mit der Erstellung der nächsten Datei fort.
- Sie können jedes Formatelement vom Typ XML ELEMENT als non-breakable festlegen. Auf diese Weise können Sie die verschachtelten Elemente von XML-Knoten, die unter dem Formatelement erzeugt werden, in einer einzigen generierten Datei behalten.

Zusätzlich zu den Formatelementen XML ELEMENT und XML SEQUENCE zum Hinzufügen von XML-Knoten in die generierte Datei, können Sie das RAW XML Formatelement verwenden. Knoten, die Sie mit dem RAW XML Formatelement hinzufügen, werden jedoch nicht berücksichtigt, wenn die Anzahl der Knoten berechnet wird, um die Grenzen der Anzahl der Elemente auszuwerten.

Wenn Sie Dateiziele für ein FILE Formatelement konfiguriert haben, das so konfiguriert wurde, dass es die generierte Ausgabe aufteilt, wenn bestimmte Grenzwerte überschritten werden, wird jedes Stück der generierten Ausgabe als einzelne Datei an das konfigurierte Dateiziel gesendet. Um die Dateien, die durch die Aufteilung der Ausgabe erzeugt werden, eindeutig zu benennen, müssen Sie einen ER-Ausdruck für das FILE Formatelement konfigurieren. Wenn Sie eine ER-Datenquelle vom Typ NUMBER SEQUENCE einbinden, wird die Zahlenfolge für jedes Stück der aufgeteilten Ausgabe inkrementiert.

Um mehr über diese Funktion zu erfahren, spielen Sie den Aufgabenleitfaden **ER Teilen von XML-Dateien basierend auf der Dateigröße oder der Anzahl der Inhaltselemente** ab, der Teil des **7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)** Geschäftsprozesses ist und im [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684) heruntergeladen werden kann. Dieser Aufgabenleitfaden führt Sie durch den Prozess der Konfiguration eines ER-Formats zur Aufteilung der generierten Dateien basierend auf den Begrenzungen der Dateigröße und der Anzahl der Inhaltselemente. Um den Aufgabenleitfaden zu auszuführen, müssen Sie die folgenden Dateien herunterladen:

- [ER-Datenmodellkonfiguration - XmlFilesSplittingModel.xml](https://go.microsoft.com/fwlink/?linkid=874111)
- [ER-Formatkonfiguration - XmlFilesSplittingFormat.xml](https://go.microsoft.com/fwlink/?linkid=874111)

## <a name="additional-resources"></a>Zusätzliche Ressourcen
[Zielorte für elektronische Berichterstellung](electronic-reporting-destinations.md)

[Formeldesigner in der elektronischen Berichterstellung](general-electronic-reporting-formula-designer.md)
