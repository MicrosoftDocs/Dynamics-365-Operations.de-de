---
title: Verbesserte RCS-Filterung im RCS/Global-Repository
description: Dieses Thema beschreibt die erweiterten Filterfunktionen für das RCS Global Repository, die durch die zusätzlichen Filter verbessert wurden.
author: JaneA07
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 2def3b653ac7c90318feb696c0dd197217ac29f64f0f08d26a7069918c67922b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778111"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a>Erweiterte RCS-Filteroptionen zur Suche nach Konfigurationen im globalen/RCS-Repository

[!include [banner](../includes/banner.md)]

In diesem Thema werden die erweiterten Filterfunktionen für das globale Repository der Regulatory Configuration Services (RCS) beschrieben, die um die folgenden Filterkriterien erweitert wurden: 
- **Land/Region** – Basierend auf ISO-Ländercodes  
- Typ **Markierungen** für:
  - Funktionaler Bereich
  - Funktionsbereich
  - Branche 
  - Geschäftsdokument 

Sie können Filter entweder einzeln oder in Gruppen anwenden, um bestimmte oder verwandte Konfigurationen leichter zu finden. Um beispielsweise einen einzelnen Typ von konfigurierbaren Geschäftsdokumenten zu finden, die sich auf Lieferantenrechnungen beziehen, können Sie einen **Geschäftsdokumenttyp**-Filter anwenden, um nach diesem Dokumenttyp zu suchen. 

[![Filterabschnitt für globales Repository.](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG) 

Sie können die Suche weiter verfeinern, indem Sie die Dokumentart auswählen, z. B. „Lieferantenrechnung“, und auf **Filter anwenden** klicken. Das folgende Beispiel zeigt die Ergebnisse beim Filtern nach **Geschäftsdokumenttyp** mit hinzugefügtem Dokumententyp. 

[![Angewandter Filter und Import für Geschäftsdokumenttyp.](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG) 

Gefilterte Ergebnisse können in ein Benutzer-RCS-Repository oder in eine Dynamics 365 Finance-Umgebung importiert werden, entweder einzeln oder als Satz. Wählen Sie dazu die Gruppe der Konfigurationen aus und klicken Sie auf **Importieren**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]