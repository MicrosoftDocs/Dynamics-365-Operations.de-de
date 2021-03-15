---
title: Halbjährliche Abschreibung auf sonstige Anschaffungen für Österreich
description: Dieses Thema enthält Informationen zur Abschreibung sonstiger Anschaffungen, wenn die Halbjahreskonvention für die Abschreibung von Anlagevermögen verwendet wird.
author: ShylaThompson
manager: AnnBe
ms.date: 10/31/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBook, AssetDepreciationProfile, AssetParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 272663
ms.search.region: Austria
ms.author: sndray
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: cbfdb8bf47ed2d1067ab85d1a041179794a1a103
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988342"
---
# <a name="half-year-depreciation-on-additional-acquisitions-for-austria"></a>Halbjährliche Abschreibung auf sonstige Anschaffungen für Österreich

[!include [banner](../includes/banner.md)]

Dieses Thema enthält Informationen für Benutzer zur Abschreibung sonstiger Anschaffungen, wenn die Halbjahreskonvention für die Abschreibung von Anlagevermögen verwendet wird.

Bei juristischen Personen in Österreich werden die Abschreibung für zusätzliche Anschaffungen und Anschaffungsänderungen gemäß den folgenden Regeln berechnet:

-   Die Anzahl der zusätzlichen Anschaffungen, die im ersten Jahr der Anschaffung gebucht werden, wird abgeschrieben ab dem Ausführungsdatum der Abschreibung (wenn eine Anlage vor dem 30. Juni gekauft wird und zusätzliche Anschaffungen vor dem 30. Juni gebucht werden oder eine Anlage nach dem 1. Juli gekauft wird und zusätzliche Anschaffungen nach dem 1. Juli gebucht werden) oder ab dem 1. Juli, falls eine Anlage vor dem 30. Juni gekauft wird und zusätzliche Anschaffungen nach dem 1. Juli gebucht werden.
-   Die Anzahl der zusätzlichen Anschaffungen, die im Jahr nach dem ersten Jahr der Anschaffung gebucht werden, wird gemäß Halbjahreskonventionsregel beginnend am 1. Januar oder am 1. Juli des Jahres abgeschrieben, in dem die zusätzlichen Anschaffungen gebucht werden.

## <a name="prerequisites"></a>Voraussetzungen

|                                       |                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Voraussetzung**                      | **Informationen**                                                                                                                                                                                                                                                                                                                                              |
| Einrichten von **Abschreibungsprofilen**       | Wechseln Sie zu **Anlagen** > **Einstellungen** > **Abschreibungsprofile**. Für ein Abschreibungsprofil mit **Abschreibungsmethoden** = Verbleibende lineare Nutzungsdauer** wählen Sie das Kontrollkästchen **Halbjährliche Abschreibung für sonstige Anschaffungen**. Wenn diese Option aktiviert ist, wird die Abschreibungskonvention **Halbes Jahr (Startjahr)** für zusätzliche Anschaffungen implementiert. |
| Einrichten von **Anlagenparametern**    | Wechseln Sie zu **Anlagen** > **Einstellungen** > **Anlagenparameter**. Auf der Registerkarte **Allgemeines** wählen Sie **Bestimmte Regeln zur halbjährlichen Abschreibung anwenden** und **Automatische Abschreibungsregulierungsbeträge mit Abgang erstellen**.                                                                                  |

## <a name="half-year-depreciation-on-additional-acquisitions-calculation"></a>Halbjährliche Abschreibung auf sonstige Anschaffungsberechnung
Wenn die Kontrollkästchen **Bestimmte Regeln zur halbjährlichen Abschreibung anwenden** und **Automatisch Abschreibungsregulierungsbeträge mit Abgang erstellen** aktiviert sind, wird der Abschreibungsregulierungsbetrag für Anlagen mit der Abschreibungsmethode **Verbleibende lineare Nutzungsdauer** und **Halbjahr (Jahresanfang)**, die verwendet wird, automatisch mit dem Abgang gebucht, der gemäß den Halbjahreskonventionsregeln berechnet wird.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]