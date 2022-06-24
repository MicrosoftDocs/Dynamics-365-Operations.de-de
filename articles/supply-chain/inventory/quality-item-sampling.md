---
title: Qualitätsmanagement Artikelmusteraufnahme
description: Dieser Artikel beschreibt, wie Sie eine Artikelmusteraufnahme festlegen.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 644eae4fbd9f82027c1cb69efba00dc893f8fc66
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865149"
---
# <a name="quality-management-item-sampling"></a>Qualitätsmanagement Artikelmusteraufnahme

[!include [banner](../includes/banner.md)]

Die Artikelmusteraufnahme wird als Teil einer Qualitätsassoziation verwendet. Es definiert die Menge des aktuellen physischen Bestandes, der geprüft werden muss. Die Probenahme kann auf festen Mengen, einem Prozentsatz oder einem vollständigen Ladungsträger basieren.

## <a name="set-up-item-sampling"></a>"Artikelmusteraufnahme" einrichten

Führen Sie diese Schritte aus, um die Artikelmusteraufnahme festzulegen.

1. Wechseln Sie zu **Lagerverwaltung \> Einstellungen \> Qualitätskontrolle \> Artikelmusteraufnahme**.
1. Wählen Sie **Neu** aus.
1. Geben Sie im Feld **Artikelmusteraufnahme** einen Wert ein.
1. Geben Sie im Feld **Beschreibung** einen Wert ein, oder wählen Sie einen Wert aus.
1. Geben Sie im Feld **Wert** eine Zahl ein. Dieser Wert bezieht sich auf den Wert der Mengenangabe, der im benachbarten Feld ausgewählt ist.
1. Aktivieren Sie im Abschnitt **Verarbeiten** das Kontrollkästchen **Vollsperrung**, wenn bei einem fehlgeschlagenen Test die gesamte Los- oder Auftragszeilenmenge gesperrt werden soll. Wenn dieses Kontrollkästchen deaktiviert ist, werden nur die Elemente im Qualitätsprüfungsauftrag gesperrt, wenn ein Test fehlschlägt.
1. Wählen Sie **Speichern** aus.
1. Schließen Sie die Seite.

> [!NOTE]
> Die Funktion *Qualitätsmanagement für Lagerortprozesse* bietet zusätzliche Funktionen für die Artikelmusteraufnahme. Es fügt das Konzept des *Artikelmusteraufnahme-Umfangs* hinzu und lässt Sie einen vollständigen Ladungsträger als Mengenangabe definieren. Wenn Sie diese Funktion aktiviert haben, lesen Sie [Qualitätsmanagement für Lagerortprozesse](quality-management-for-warehouses-processes.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
