---
title: Qualitätsmanagement-Tests
description: Dieser Artikel beschreibt, wie Sie Tests erstellen, die für Qualitätsprüfungsaufträge in Microsoft Dynamics 365 Supply Chain Management verwendet werden können.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac67ee97a4890c646daefa6b09feae25c4f15d0d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857604"
---
# <a name="quality-management-tests"></a>Qualitätsmanagement-Tests

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt, wie Sie Tests erstellen, die für Qualitätsprüfungsaufträge in Microsoft Dynamics 365 Supply Chain Management verwendet werden können.

Sie verwenden die Seite **Tests**, um die einzelnen Tests zu definieren und anzuzeigen, die bestimmen, ob Ihre Produkte die Qualitätsspezifikationen erfüllen. Einzelne Tests können einer Testgruppe zugewiesen werden. In diesem Fall werden auch testspezifische Informationen (beispielsweise die zulässigen Messwerte) angegeben. Messwerte werden für quantitative Tests verwendet. Für qualitative Tests werden Testvariablen verwendet.

- Für quantitative Tests wird das Feld **Typ** auf *Ganzzahl* oder *Bruch* festgelegt. Außerdem wird eine Maßeinheit angegeben. Qualitätsangaben und Testergebnisse werden in Zahlen ausgedrückt.
- Für qualitative Tests wird das Feld **Typ** auf *Option* festgelegt. Qualitative Tests erfordern zusätzliche Informationen über die zu messende Variable und die zugehörigen Optionen. Qualitätsangaben und Testergebnisse werden gemäß einem Ergebnis ausgedrückt.

Sie können einem Test optional ein Testinstrument zuweisen. Für das Erstellen und Verwenden von Tests mit Qualitätsprüfungsaufträgen sind jedoch keine Testinstrumente erforderlich. Weitere Informationen finden Sie unter [Qualitätsmanagement Prüfmittel](quality-test-instruments.md).

Sie können auch optional eine Einheit für einen Test angeben, um die Maßeinheit anzugeben, in der die Testergebnisse gespeichert werden. Zum Beispiel könnte ein Test für Temperatur eine Einheit von entweder Grad Fahrenheit oder Grad Celsius enthalten.

## <a name="example-of-a-test"></a>Beispiel für einen Test

Eine produzierende Firma führt zwei Tests an gekauftem Material durch: einen quantitativen Test auf Materialqualität und einen qualitativen Test auf Verpackungsschäden. Die Firma gibt zusätzliche Informationen über den qualitativen Test an, um die Testvariable (z. B. beschädigte Verpackung) und ihre Ergebnisse zu definieren. Auf der Seite **Testgruppen** werden die beiden Tests einer Testgruppe zugeordnet und die testspezifischen Informationen angegeben. Die Testgruppe wird einem Qualitätsprüfungsauftrag zugeordnet, damit die Firma Testergebnisse für die beiden Tests melden kann.

## <a name="create-a-test"></a>Einen Test erstellen

Folgen Sie diesen Schritten, um einen Test zu erstellen.

1. Gehen Sie zu **Lagerverwaltung \> Einstellungen \> Qualitätskontrolle \> Tests**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen. Legen Sie für die neue Zeile die folgenden Felder fest:

    - **Test** – Geben Sie eine eindeutige ID oder einen Namen für den Test ein.
    - **Beschreibung** – Geben Sie eine detaillierte Beschreibung des Tests ein.
    - **Typ** – Wählen Sie die Art der Ergebnisse, die der Test erzeugt. Für quantitative Tests wählen Sie *Bruch* oder *Ganzzahl*. Wählen Sie für qualitative Tests *Option*.
    - **Testgerät** – Wählen Sie ein [Testgerät](quality-test-instruments.md), das für den Test verwendet werden soll.
    - **Einheit** – Wenn Sie *Bruch* oder *Ganzzahl* im Feld **Typ** gewählt haben (d.h. wenn es sich um einen quantitativen Test handelt), wählen Sie die Maßeinheit, in der die Testergebnisse gespeichert werden sollen.

1. Schließen Sie die Seite.

> [!NOTE]
> Nachdem Sie einen Test gespeichert haben, können Sie das Feld **Typ** im Raster nicht mehr bearbeiten. Wenn Sie die Art der Testergebnisse, die für einen Test aufgezeichnet werden sollen, ändern müssen, wählen Sie **Qualitätstesttyp ändern** im Aktivitätsbereich. Legen Sie im Dialogfeld **Qualitätstesttyp ändern** das Feld **Neuer Typ** auf den gewünschten Typ fest und wählen Sie dann **OK**, um das Dialogfeld zu schließen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Qualitätsmanagement Testinstrumente](quality-test-instruments.md)
- [Qualitätsmanagement Testgruppen](quality-test-groups.md)
- [Qualitätsmanagement-Testvariablen](quality-test-variables.md)
- [Qualitätszuordnungen](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
