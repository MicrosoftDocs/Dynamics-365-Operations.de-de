---
title: Qualitätsmanagement Testinstrumente
description: Dieser Artikel beschreibt, wie Sie Testinstrumente erstellen, die für Tests bei Qualitätsprüfungsaufträgen in Microsoft Dynamics 365 Supply Chain Management verwendet werden können.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestInstrument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 36b712e6a99a0625af28ef121d0c9c39c1e32603
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857662"
---
# <a name="quality-management-test-instruments"></a>Qualitätsmanagement Testinstrumente

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt, wie Sie Testinstrumente erstellen, die für Tests bei Qualitätsprüfungsaufträgen in Microsoft Dynamics 365 Supply Chain Management verwendet werden können.

Sie verwenden die Seite **Testgeräte**, um Details zu den Geräten zu definieren und anzuzeigen, die zur Durchführung von Tests bei Qualitätsprüfungsaufträgen verwendet werden. Testinstrumente sind optional. Sie können jedoch den Arbeitskräften in der Qualitätssicherung helfen, zu wissen, welches Gerät oder Tool sie für einen bestimmten Test verwenden sollten.

## <a name="test-instrument-example"></a>Beispiel für ein Testinstrument

Sie führen verschiedene Tests an elektrischen Komponenten durch. Einige Tests beziehen sich auf die Spannungsausgabe der Komponenten, ein Test auf ihre Temperatur und ein Test auf ihr Gewicht. Zur Durchführung der einzelnen Tests werden unterschiedliche Tools, Geräte oder Ausrüstungen verwendet. Zum Beispiel wird ein Spannungsmesser zur Messung der Spannung, ein Thermometer zur Messung der Temperatur und eine Waage zur Messung des Gewichts verwendet. Sie können jedes dieser Geräte als Prüfgerät konfigurieren und die Maßeinheit angeben, in der die Prüfergebnisse erfasst werden sollen. Zum Beispiel werden die Ergebnisse des Spannungsmessers in Volt, die Ergebnisse des Thermometers in Grad Fahrenheit oder Grad Celsius und die Ergebnisse der Waage in Pfund oder Kilogramm aufgezeichnet.

## <a name="create-a-test-instrument"></a>Erstellen Sie ein Testinstrument

1. Gehen Sie zu **Lagerverwaltung \> Einstellungen \> Qualitätskontrolle \> Testinstrumente**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen. Legen Sie für die neue Zeile die folgenden Felder fest:

    - **Testgerät** – Geben Sie eine eindeutige ID oder einen Namen für das Testgerät ein.
    - **Beschreibung** – Geben Sie eine detaillierte Beschreibung des Testgeräts ein.
    - **Einheit** – Wählen Sie die Einheit, in der das Gerät die Kennzahlen der Ergebnisse misst. Das Feld **Präzision** wird automatisch festgelegt, basierend auf der von Ihnen gewählten Einheit.

1. Schließen Sie die Seite.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Qualitätsmanagement-Test](quality-tests.md)
- [Qualitätsmanagement Testgruppen](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
