---
title: "Halbjährliche Abschreibung auf sonstige Anschaffungen für Österreich"
description: "Dieses Thema enthält Informationen für Benutzer von juristischen Personen in Österreich zu der Abschreibung von zusätzlichen Anschaffungen, wenn die Abschreibungskonvention für das Halbjahr für die Anlagenabschreibung verwendet wird."
author: ShylaThompson
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBook, AssetDepreciationProfile, AssetParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 272663
ms.search.region: Austria
ms.author: sndray
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 56b5529468981cd184aec26f8547753e23e33b6d
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="half-year-depreciation-on-additional-acquisitions-for-austria"></a>Halbjährliche Abschreibung auf sonstige Anschaffungen für Österreich

[!include[banner](../includes/banner.md)]


Dieses Thema enthält Informationen für Benutzer von juristischen Personen in Österreich zu der Abschreibung von zusätzlichen Anschaffungen, wenn die Abschreibungskonvention für das Halbjahr für die Anlagenabschreibung verwendet wird.

Bei juristischen Personen in Österreich werden die Abschreibung für zusätzliche Anschaffungen und Anschaffungsänderungen gemäß den folgenden Regeln berechnet:

-   Betrag zusätzlicher Anschaffungen, die im ersten Jahr der Anschaffung gebucht werden, wird abgeschrieben vom Abschreibungsstartdatum (wenn eine Anlage vor dem 30. Juni gekauft wird und zusätzliche Anschaffungen, die vor dem 30. Juni gebucht werden oder eine Anlage, die nach dem 1. Juli gekauft wurde und zusätzliche Anschaffungen, die nach dem 1. Juli gebucht werden) oder ab dem 1. Juli, falls eine Anlage vor dem 30. Juni gekauft wird und zusätzliche Anschaffungen, die nach dem 1. Juli gebucht werden.
-   Betrag zusätzlicher Anschaffungen, die im Jahr nach dem ersten Jahr der Anschaffung gebucht werden, wird gemäß Konventionsregel vom Halbjahr beginnend am 1. Januar oder am 1. Juli des Jahres abgeschrieben, in dem die zusätzlichen Anschaffungen gebucht werden.

## <a name="prerequisites"></a>Voraussetzungen
|                                       |                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Voraussetzung**                      | **Informationen**                                                                                                                                                                                                                                                                                                                                              |
| Einrichten von **Abschreibungsprofilen**       | Öffnen Sie **Analgen** &gt; **Einrichten** &gt; **Abschreibungsprofile**. Für Abschreibungsprofile mit **Abschreibungsmethoden- = Verbleibende lineare Nutzungsdauer** markieren Sie das Kontrollkästchen **Halbjährliche Abschreibung für sonstige Anschaffungen** Wenn diese Option aktiviert ist, wird die Abschreibungskonvention **Halbes Jahr (Startjahr)** für zusätzliche Anschaffungen implementiert. |
| Einrichten von **Anlagenparametern**    | Wechseln Sie zu **Anlagen** &gt; **Einstellungen** &gt; **Anlagenparameter.** Auf der Registerkarte **Allgemeines** wählen Sie die folgenden Parameter:  **Wenden Sie bestimmte Regeln zur Abschreibung des Halbjahr an**, **Automatische Abschreibungsregulierungsbeträge mit Abgang erstellen**.                                                                                  |

## <a name="halfyear-depreciation-on-additional-acquisitions-calculation"></a>Halbjährliche Abschreibung auf sonstige Anschaffungsberechnung
Wenn das Kontrollkästchen **Wenden Sie bestimmte Regeln zur Abschreibung des Halbjahr an** und das Kontrollkästchen **Automatisch Abschreibungsregulierungsbeträge mit Abgang erstellen** aktiviert ist, wird der Abschreibungsregulierungsausgleichsbetrag für Anlagen mit  Abschreibungsmethode **Verbleibende lineare Nutzungsdauer)** **Halbjahr (Jahresanfang)**, die verwendet wird, automatisch mit dem Abgang gebucht, der gemäß den Konventionsregeln des Halbjahr berechnet wird.





