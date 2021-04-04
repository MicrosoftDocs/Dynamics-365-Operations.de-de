---
title: Einstellungen für Versandinformationen
description: Dieses Thema beschreibt, wie Sie Versandinformationen für das Modul Gesamttransportkosten festlegen.
author: sherry-zheng
manager: tfehr
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMGoodsDescriptionTable, ITMVesselTable, ITMExporterTable, ITMCommodityCodeTable, ITMCustomsDescription
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 90794a154eb2a63f33277383cda80323dafd77b0
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500933"
---
# <a name="shipping-information-setup"></a>Einstellungen für Versandinformationen

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In diesem Thema wird beschrieben, wie Sie Versandinformationen für das Modul **Gesamttransportkosten** festlegen.

## <a name="description-of-goods"></a><a name="description-of-goods"></a>Warenbeschreibung

Warenbeschreibungen helfen, eine Fahrt, einen Transportcontainer oder eine Palette von Waren und die darin enthaltenen Waren zu identifizieren. Sie können eine Warenbeschreibung in der Kopfzeile des Transportcontainers oder in der Kopfzeile des Paletten auswählen.

Um mit Warenbeschreibungen zu arbeiten, gehen Sie zu **Gesamttransportkosten \> Versandinformationen einrichten \> Beschreibung der Waren**. Dort können Sie Datensätze für Beschreibungen von Waren anzeigen, öffnen, erstellen und löschen. Die folgende Tabelle beschreibt die Felder, die für jeden Datensatz verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Warenbeschreibung | Geben Sie einen eindeutigen Identifikationsnamen/eine eindeutige Identifikationsnummer für die Art der Waren ein, für die diese Beschreibung verwendet werden soll. |
| Beschreibung | Geben Sie eine Beschreibung der Art der Waren in dieser Kategorie ein. |

## <a name="vessels"></a><a name="vessels"></a>Schiffe

Ein Schiff ist der eindeutige Name eines Schiffs oder Schiffs, den eine Firma oder Agentur verwendet. Wenn Sie eine Fahrt erstellen, müssen Sie immer ein Schiff dafür entweder auswählen oder eingeben. Wenn Sie häufig dieselben Schiffe verwenden, können Sie das Erstellen einer neuen Fahrt beschleunigen und vereinfachen, indem Sie für jedes dieser Schiffe einen Schiffsdatensatz erstellen, so dass die Benutzer das Schiff aus einer Liste auswählen können und nicht jedes Mal den Namen oder die Nummer manuell eingeben müssen.

Um mit Schiffen zu arbeiten, gehen Sie zu **Gesamttransportkosten \> Versandinformationen einrichten \> Schiffe**. Dort können Sie Datensätze für Schiffe anzeigen, öffnen, erstellen und löschen. Die folgende Tabelle beschreibt die Felder, die für jeden Datensatz verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Schiff | Geben Sie einen eindeutigen Identifikationsnamen/eine eindeutige Identifikationsnummer für das Schiff ein, das zum Transport von Waren auf einer Fahrt verwendet wird. |
| Beschreibung | Geben Sie eine Beschreibung für das Schiff ein. Typischerweise identifiziert diese Beschreibung den Namen des Schiffes und der Reederei/des Agenten. |
| Lieferart | Wählen Sie die Lieferart, die das Schiff verwendet (z. B. _Luft_, _Meer_ oder _Schiene_). |

## <a name="exporters"></a>Exporteure

Jeder Ausführer-Datensatz identifiziert einen Lieferanten oder Ausführer, der als Lieferant für eine Fahrt definiert werden kann. Der Exporteur kann mit einer Fahrt verknüpft und für Berichte verwendet werden.

Um mit Exporteuren zu arbeiten, gehen Sie zu **Gesamttransportkosten \> Versandinformationen einrichten \> Exporteure**. Dort können Sie Datensätze für Exporteure anzeigen, öffnen, erstellen und löschen. Die folgende Tabelle beschreibt die Felder, die für jeden Datensatz verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Exporteur | Geben Sie einen eindeutigen Identifikationsnamen/Nummer für den Ausführer von Waren ein, die auf einer Fahrt transportiert werden. |
| Beschreibung | Geben Sie eine Beschreibung des Ausführers ein. Normalerweise identifiziert diese Beschreibung den vollständigen Namen der Firma/des Agenten der Reederei. |

## <a name="commodity-codes"></a>Warencodes

Sie verwenden Warencodes, um die Identifizierung der Zölle und die Berechnung der Sätze für Waren auf einer Fahrt zu erleichtern. Sie können Warencodes auf der Seite **Freigegebene Produkte** auswählen.

Um mit Warencodes zu arbeiten, gehen Sie zu **Gesamttransportkosten \> Versandinformationen einrichten \> Warencodes**. Dort können Sie Datensätze für Warencodes anzeigen, öffnen, erstellen und löschen. Die folgende Tabelle beschreibt die Felder, die für jeden Datensatz verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Warencode | Geben Sie einen eindeutigen Code für diese Art von Ware ein. |
| Beschreibung | Geben Sie eine Beschreibung für die Warenart ein. |

## <a name="customs-description"></a>Zollbeschreibung

Zollbeschreibungen helfen, Waren für Zollzwecke zu identifizieren. Sie können eine Zoll-Beschreibung auf der Seite **Freigegebene Produkte** oder auf Zeilen der Einkaufsbestellung auswählen.

Um mit Zollbeschreibungen zu arbeiten, gehen Sie auf die Seite **Gesamttransportkosten \> Versandinformationen einrichten \> Zollbeschreibung**. Dort können Sie Datensätze für benutzerdefinierte Beschreibungen anzeigen, öffnen, erstellen und löschen. Die folgende Tabelle beschreibt die Felder, die für jeden Datensatz verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Zollbeschreibung | Geben Sie einen eindeutigen Code für diese Art der Zollklassifizierung ein. Oft wird dieser Code die offizielle Beschreibung sein, die von einer Zollbehörde für die Beschreibung und den qualitativen Wert der Waren bereitgestellt wird. |
| Beschreibung | Geben Sie eine Beschreibung der Zollklassifizierung ein. |
