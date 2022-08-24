---
title: Verbesserte RCS-Filterung im RCS/Global-Repository
description: Dieser Artikel beschreibt die erweiterten Filterfunktionen für das RCS Global Repository, die durch die zusätzlichen Filter verbessert wurden.
author: kfend
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423
ms.assetid: ''
ms.search.form: ERSolutionTable, ERWorkspace
ms.openlocfilehash: e0408d0561c0cfead8781b9f49fdb84d5caf179a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274511"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a>Erweiterte RCS-Filteroptionen zur Suche nach Konfigurationen im globalen/RCS-Repository

[!include [banner](../includes/banner.md)]

In diesem Artikel werden die erweiterten Filterfunktionen für das globale Repository der Regulatory Configuration Services (RCS) beschrieben, die um die folgenden Filterkriterien erweitert wurden: 
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
