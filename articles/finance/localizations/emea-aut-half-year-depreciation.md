---
title: Halbjährliche Abschreibung auf sonstige Anschaffungen für Österreich
description: Dieser Artikel enthält Informationen zur Abschreibung sonstiger Anschaffungen, wenn die Halbjahreskonvention für die Abschreibung von Anlagevermögen verwendet wird.
author: AdamTrukawka
ms.date: 10/31/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria
ms.author: atrukawk
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 272663
ms.search.form: AssetBook, AssetDepreciationProfile, AssetParameters
ms.openlocfilehash: 570d2a88b814c7c09df26efaeb058fd9e830e4b1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286655"
---
# <a name="half-year-depreciation-on-additional-acquisitions-for-austria"></a>Halbjährliche Abschreibung auf sonstige Anschaffungen für Österreich

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen für Benutzer zur Abschreibung sonstiger Anschaffungen, wenn die Halbjahreskonvention für die Abschreibung von Anlagevermögen verwendet wird.

Bei juristischen Personen in Österreich werden die Abschreibung für zusätzliche Anschaffungen und Anschaffungsänderungen gemäß den folgenden Regeln berechnet:

-   Die Anzahl der zusätzlichen Anschaffungen, die im ersten Jahr der Anschaffung gebucht werden, wird abgeschrieben ab dem Ausführungsdatum der Abschreibung (wenn eine Anlage vor dem 30. Juni gekauft wird und zusätzliche Anschaffungen vor dem 30. Juni gebucht werden oder eine Anlage nach dem 1. Juli gekauft wird und zusätzliche Anschaffungen nach dem 1. Juli gebucht werden) oder ab dem 1. Juli, falls eine Anlage vor dem 30. Juni gekauft wird und zusätzliche Anschaffungen nach dem 1. Juli gebucht werden.
-   Die Anzahl der zusätzlichen Anschaffungen, die im Jahr nach dem ersten Jahr der Anschaffung gebucht werden, wird gemäß Halbjahreskonventionsregel beginnend am 1. Januar oder am 1. Juli des Jahres abgeschrieben, in dem die zusätzlichen Anschaffungen gebucht werden.

## <a name="prerequisites"></a>Voraussetzungen

| Voraussetzung                      | Informationen                |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Einrichten von **Abschreibungsprofilen**       | Wechseln Sie zu **Anlagen** > **Einstellungen** > **Abschreibungsprofile**. Für ein Abschreibungsprofil mit der **Abschreibungsmethode** = `Straight line life remaining` wählen Sie das Kontrollkästchen **Halbjährliche Abschreibung für sonstige Anschaffungen**. Wenn diese Option aktiviert ist, wird die Abschreibungskonvention **Halbes Jahr (Startjahr)** für zusätzliche Anschaffungen implementiert. |
| Einrichten von **Anlagenparametern**    | Wechseln Sie zu **Anlagen** > **Einstellungen** > **Anlagenparameter**. Auf der Registerkarte **Allgemeines** wählen Sie **Bestimmte Regeln zur halbjährlichen Abschreibung anwenden** und **Automatische Abschreibungsregulierungsbeträge mit Abgang erstellen**.                                                                                  |

## <a name="half-year-depreciation-on-additional-acquisitions-calculation"></a>Halbjährliche Abschreibung auf sonstige Anschaffungsberechnung
Wenn die Kontrollkästchen **Bestimmte Regeln zur halbjährlichen Abschreibung anwenden** und **Automatisch Abschreibungsregulierungsbeträge mit Abgang erstellen** aktiviert sind, wird der Abschreibungsregulierungsbetrag für Anlagen mit der Abschreibungsmethode `Straight line life remaining` und der Konvention **Halbjahr (Jahresanfang)** automatisch mit dem Abgang gebucht, der gemäß den Halbjahreskonventionsregeln berechnet wird.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
