---
title: Qualität der Waren inspizieren
description: Dieser Artikel beschreibt, wie Sie Qualitätsprüfungsaufträge verarbeiten.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b881f9c6f872061864d4254ce880d981ca71c479
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219033"
---
# <a name="inspect-the-quality-of-goods"></a>Qualität der Waren inspizieren

[!include [banner](../../includes/banner.md)]

Dieser Artikel beschreibt, wie Sie Qualitätsprüfungsaufträge verarbeiten. Qualitätsprüfungen werden normalerweise von einem Qualitätssachbearbeiter durchgeführt.

Wenn die Standard-[Demodaten](../../../fin-ops-core/fin-ops/get-started/demo-data.md) installiert sind, können Sie sie verwenden, um die Verfahren in diesem Artikel abzuschließen. Um die Demo-Daten zu verwenden, wählen Sie vorher die *USMF* juristische Entität aus. Anschließend müssen Sie die Bestellung *000016* bestätigen und einen Wareneingang buchen. Ein Qualitätsprüfungsauftrag wird automatisch generiert.

## <a name="step-1-select-a-quality-order"></a>Schritt 1: Wählen Sie einen Qualitätsprüfungsauftrag

Um einen Qualitätsprüfungsauftrag auszuwählen, führen Sie diese Schritte aus.

1. Wechseln Sie zu **Lagerverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Qualitätsprüfungsaufträge**.
1. Wählen Sie den Qualitätsprüfungsauftrag, der erzeugt wurde, bevor Sie diesen Vorgang gestartet haben.

## <a name="step-2-record-test-results"></a>Schritt 2: Testergebnisse aufzeichnen

Um Testergebnisse zu protokollieren, führen Sie diese Schritte aus.

1. Wählen Sie **Ergebnisse** aus.
1. Wählen Sie **Bearbeiten** aus.
1. Geben Sie im Feld **Ergebnismenge** eine Zahl ein.
1. Wählen Sie im Feld **Ergebnis** den gewünschten Datensatz. In diesem Beispiel basiert das Ergebnis auf einem vordefinierten Ergebnis. Normalerweise werden Sie einen spezifischeren Datensatz erfassen, z. B. eine Größe oder eine andere Dimension.
1. Wählen Sie **Speichern** aus.
1. Schließen Sie die Seite.

## <a name="step-3-validate-the-quality-order"></a>Schritt 3: Validieren des Qualitätsprüfungsauftrags

Gehen Sie folgendermaßen vor, um den Qualitätsprüfungsauftrag zu validieren.

1. Wählen Sie **Überprüfen** aus.
1. Wählen Sie im Feld **Gültig gemacht von** den Benutzer aus, der die Überprüfung durchführt.
1. Wählen Sie **Auswählen**.
1. Wählen Sie **OK**.
1. Schließen Sie die Seite.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
