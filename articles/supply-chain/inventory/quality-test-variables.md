---
title: Qualitätsmanagement-Testvariablen
description: Dieser Artikel beschreibt, wie Sie Testvariablen erstellen, die für qualitative Tests zu Qualitätsprüfungsaufträgen in Microsoft Dynamics 365 Supply Chain Management verwendet werden können.
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
ms.openlocfilehash: 10fe206b76f2e50e09cb6aaa6055614c2fe9425d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857633"
---
# <a name="quality-management-test-variables"></a>Qualitätsmanagement-Testvariablen

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt, wie Sie Testvariablen erstellen, die für qualitative Tests zu Qualitätsprüfungsaufträgen in Microsoft Dynamics 365 Supply Chain Management verwendet werden können.

Für jeden qualitativen Test, der auf der Seite **Tests** definiert wird, müssen Sie eine Testvariable und ihre möglichen Ergebnisse (Resultate) definieren. (Für qualitative Tests wird das Feld **Typ** auf der Seite **Tests** auf *Option* festgelegt.)

Sie verwenden die Seite **Testvariablen**, um die möglichen Ergebnisse für eine Testvariable, die mit einem qualitativen Test verbunden ist, festzulegen, zu bearbeiten und anzuzeigen. Für jedes Ergebnis weisen Sie einen Ergebnisstatus von entweder *Bestanden* oder *Nicht bestanden* zu, um anzugeben, ob der Test bestanden oder nicht bestanden ist, wenn dieses Ergebnis als Testergebnis ausgewählt wird. Sie verwenden die Seite **Testgruppen**, um einem einzelnen qualitativen Test eine Testvariable und ein Standard-Ergebnis dafür zuzuweisen.

Wir empfehlen, für jede Testvariable mindestens zwei Ergebnisse zu definieren: eines, das den Ergebnisstatus *Bestanden* hat, und eines, das den Ergebnisstatus *Nicht bestanden* hat. Es gibt keine Begrenzung für die Gesamtzahl der Variablen oder Ergebnisse, die definiert werden können. Außerdem können mehrere Tests dieselben Testvariablen verwenden, um die Ergebnisse zu daten.

## <a name="examples-of-test-variables"></a>Beispiele für Prüfvariablen

### <a name="example-1"></a>Beispiel 1

Eine produzierende Firma führt zwei Tests an hergestellten Materialien durch. In einem Test ist der pH-Wert mit einem Farbstreifen verbunden. Akzeptable pH-Werte sind in helleren Farben dargestellt, inakzeptable pH-Werte in dunkleren Farben. In einem anderen Test werden mehrere visuelle Inspektionen durchgeführt, und die Arbeitskräfte der Qualitätsabteilung entscheiden anhand ihres Urteils, ob das Element die visuelle Inspektion besteht oder nicht.

### <a name="example-2"></a>Beispiel 2

Ein Unternehmen, das Kekse herstellt, führt einen Prüftest bezüglich des fertigen Produkts aus. Diese Abnahmeprüfung besitzt mehrere Variablen. Eine Variable ist der Geschmack, und die möglichen Ergebnisse für ihn sind gut und schlecht. Eine zweite Variable ist die Farbe, und die möglichen Ergebnisse für sie sind zu dunkel, zu hell und korrekt.

## <a name="create-a-test-variable"></a>Eine Testvariable erstellen

Führen Sie diese Schritte aus, um eine Testvariable zu erstellen.

1. Gehen Sie zu **Lagerverwaltung \> Einstellungen \> Qualitätskontrolle \> Testvariablen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen. Legen Sie für die neue Zeile die folgenden Felder fest:

    - **Variable** – Geben Sie eine eindeutige ID oder einen Namen für die Variable ein.
    - **Beschreibung** – Geben Sie eine detaillierte Beschreibung der Variablen ein.

1. Während die neue Zeile noch markiert ist, wählen Sie **Ergebnisse** im Aktivitätsbereich.
1. Wählen Sie auf der Seite **Test variable Ergebnisse** im Aktivitätsbereich **Neu**, um dem Raster eine Zeile hinzuzufügen. Legen Sie für die neue Zeile die folgenden Felder fest:

    - **Ergebnis** – Geben Sie eine eindeutige ID oder einen Namen für das Ergebnis ein.
    - **Beschreibung** – Geben Sie eine detaillierte Beschreibung des Ergebnisses ein.
    - **Ergebnisstatus** – Wählen Sie entweder *Bestanden* oder *Nicht bestanden*, um anzugeben, ob der Test bestanden oder nicht bestanden ist, wenn das Ergebnis als Testergebnis ausgewählt wird.

1. Wiederholen Sie den vorherigen Schritt für jedes zusätzliche Ergebnis. Stellen Sie sicher, dass mindestens ein Ergebnis den Status *Pass* und mindestens ein Ergebnis den Status *Fail* hat.
1. Schließen Sie die Seiten.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Qualitätsmanagement Testinstrumente](quality-test-instruments.md)
- [Qualitätsmanagement-Tests](quality-tests.md)
- [Qualitätsmanagement Testgruppen](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
