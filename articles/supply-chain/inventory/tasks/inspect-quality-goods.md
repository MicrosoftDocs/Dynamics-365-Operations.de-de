---
title: Qualität der Waren inspizieren
description: Dieses Thema beschreibt, wie Sie Qualitätsprüfungsaufträge verarbeiten.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ceb5547b6c1d4c44e53faba0d6e2c1f0368fb95768a2520ecc39066ff73a03d2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755362"
---
# <a name="inspect-the-quality-of-goods"></a>Qualität der Waren inspizieren

[!include [banner](../../includes/banner.md)]

Dieses Thema beschreibt, wie Sie Qualitätsprüfungsaufträge verarbeiten. Qualitätsprüfungen werden normalerweise von einem Qualitätssachbearbeiter durchgeführt.

Wenn die Standard-Demodaten installiert sind, können Sie sie verwenden, um die Verfahren in diesem Thema abzuschließen. Um die Demo-Daten zu verwenden, wählen Sie vorher die *USMF* juristische Entität aus. Anschließend müssen Sie die Bestellung *000016* bestätigen und einen Wareneingang buchen. Ein Qualitätsprüfungsauftrag wird automatisch generiert.

## <a name="step-1-select-a-quality-order"></a>Schritt 1: Wählen Sie einen Qualitätsprüfungsauftrag

Um einen Qualitätsprüfungsauftrag auszuwählen, führen Sie diese Schritte aus.

1. Wechseln Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Qualitätsprüfungsaufträge**.
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
