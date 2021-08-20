---
title: Stücklistenversion ermitteln
description: Wenn während der Bedarfsauflösung für einen Artikel ein Standard-Bestellvorschlagtyp zur Produktion festgelegt ist, sucht das Planungsmodul eine gültige Stücklistenversion auf Grundlage des Standorts.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 91a55bfcd10ee0efbbf1170ad29194c17ea72d62cf5516e2661b43bad7446808
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766073"
---
# <a name="determine-the-bom-version"></a>Stücklistenversion ermitteln

[!include [banner](../includes/banner.md)]

Wenn während der Bedarfsauflösung für einen Artikel ein Standard-Bestellvorschlagtyp zur Produktion festgelegt ist, sucht das Planungsmodul eine gültige Stücklistenversion auf Grundlage des Standorts. 

Der Standortgröße ist immer bekannt und in der Bedarfsbuchung angegeben. Der folgende Prozess wird verwendet, um die zu verwendende Stücklistenversion zu bestimmen:

-   Wenn eine Stücklistenversion für den Artikel am Bedarfsstandort festgelegt ist, wird die standortspezifische Stückliste verwendet.
-   Falls für einen Artikel am Bedarfsstandort keine standortspezifische Stücklistenversion festgelegt ist, wird eine allgemeine Stückliste verwendet. Eine allgemeine Stückliste gibt keinen Standort an und gilt für mehrere Standorte. Wenn eine allgemeine Stückliste vorhanden ist, wird sie verwendet.
-   Falls es keine zu verwendende allgemeine Stücklistenversion gibt, wird die Bedarfsauflösung an diesem Punkt gestoppt.

Eine gültige Stücklistenversion, egal ob standortspezifisch oder allgemein, muss die erforderlichen Kriterien für Datum und Menge erfüllen.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]