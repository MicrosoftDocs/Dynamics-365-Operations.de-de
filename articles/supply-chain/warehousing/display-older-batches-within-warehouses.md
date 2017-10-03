---
title: "Anzeige von älteren Chargen am Lagerort auf einem mobilen Gerät konfigurieren"
description: "Dieses Thema beschreibt, wie ein mobiles Gerät eingerichtet wird, um eine Liste der Standorte anzuzeigen, die Chargen enthalten, die älter als der aktuelle Standort einer Arbeitsposition sind."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 3e9386f6da7b8bdc1cbb817a78f72c225cbaa9bc
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---

# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a>Anzeige von älteren Chargen am Lagerort auf einem mobilen Gerät konfigurieren

[!include[banner](../includes/banner.md)]

Mit der Konfiguration **Ältere Chargen im Lager anzeigen** können Sie eine Liste der Standorte anzeigen, die Chargen enthalten, die älter als der aktuelle Standort der Arbeitsposition sind. Die Liste der angezeigten Standorte enthält Informationen über die älteren Chargen an dem Standort, mit Ablaufdatum und physischem Bestand jeder Charge. Sie können auswählen, von einem neuen Standort auszuwählen, oder weiterhin vom aktuellen Standort auswählen. 
- Von einem neuen Standort auswählen – Wenn Sie von einem neuen Standort auswählen wollen, wird die aktuelle Arbeitsposition aktualisiert, sodass sie den neuen Standort verwendet, und die Arbeit wird mit dem neuen Standort unverändert fortgesetzt. Damit der neue Standort gültig ist, muss er über genügend verfügbare Menge für die gesamte Arbeitsposition verfügen. Falls die erforderliche Menge nicht zur Verfügung steht, wird die Arbeitsposition nicht aktualisiert, und die Liste wird angezeigt. 
- Weiter vom aktuellen Standort auswählen – Wenn Sie weiter mit dem Standort der aktuellen Arbeitsposition arbeiten wollen, werden die Mengen für die Arbeitsposition weiter von dem ursprünglichen Standort ausgewählt.

## <a name="where-it-applies"></a>Wofür es angewendet wird
Die Anzeige älterer Chargen im Lager ist in Menüeinträgen für mobile Geräte konfiguriert und betrifft die Auswahl von Chargen.

## <a name="set-up-display-older-batches-within-warehouse"></a>Einrichtung der Anzeige älterer Chargen im Lager
Die Konfiguration **Anzeige älterer Chargen im Lager** ist in Menüeinträgen für mobile Geräte verfügbar, wenn die Option **Älteste Charge auswählen** auf **Warnung** gesetzt ist.

- Unter **Lagerverwaltung** > **Einrichtung** > **Mobiles Gerät** > **Menüeinträge mobiles Gerät** setzen Sie **Vorhandene Arbeit verwenden** für den Menüeintrag auf **Ja** und wählen dann **Warnung** im Feld **Älteste Charge auswählen**. 


