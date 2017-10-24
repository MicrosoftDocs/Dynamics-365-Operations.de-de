---
title: RFM-Alyse einrichten
description: "In diesem Thema wird erläutert, wie ein Recency-, Häufigkeits- und monetäre (RFM) Analyse Ihrer Debitoren eingerichtet wird."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 78943
ms.assetid: 8ff9aac3-5ada-4150-85fd-18901c926d53
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e11ec02d7392601b22e17384a4dbf620b79df035
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-rfm-analysis"></a>RFM-Alyse einrichten

[!include[banner](includes/banner.md)]


In diesem Thema wird erläutert, wie ein Recency-, Häufigkeits- und monetäre (RFM) Analyse Ihrer Debitoren eingerichtet wird.

RFM-Analysen (Aktualität, Häufigkeit, Geldbetrag) sind ein Marketinginstrument, das Ihre Organisation verwenden kann, um die Daten zu bewerten, die von Debitorenkäufen generiert werden. Nachdem Sie RFM-Analyse eingerichtet haben, wird Debitoren eine berechnete RFM-Punktzahl zugewiesen, während diese Einkäufe tätigen. Die RFM-Punktzahl kann eine dreistellige Bewertung oder eine Gesamtzahl sein, je nachdem, wie Ihre Organisation RFM-Analyse konfiguriert hat. Wenn Ihre Organisation eine dreistellige Bewertung für das Ergebnis verwendet, entspricht die erste Ziffer der Häufigkeit (wann tätigte der Kunden den letzten Einkauf von Ihrer Organisation) Die zweite Stelle ist eine Bewertung der Häufigkeit (wie oft tätigt der Kunde Einkäufe in Ihrer Organisation tätigt). Die dritte Ziffer ist eine Bewertung des Geldbetrags (wie viel gab der Kunde aus, wenn er Einkäufe in Ihrer Organisation tätigt). So verfügt beispielsweise Ihre Organisation ein Bewertungssystem mit einer Skala von 1 bis 5, wobei 5 die höchste Bewertung ist. In diesem Fall gibt die Kundenbewertung 535 Ihnen folgenden Informationen zum Debitor:

-   **Aktualitätsbewertung von 5** – Der Kunde hat erst vor kurzem einen Einkauf getätigt.
-   **Häufigkeitsbewertung 3** - Der Kunde erwirbt Produkte von Ihrer Organisation mit mäßiger Häufigkeit.
-   **Geldbetragwertung 5** - Wenn der Kunde einen Einkauf tätigt, gibt er oder sie einen beträchtlichen Geldbetrag aus.

Wenn Ihre Organisation für die Bewertung eine Aggregatzahl verwendet, werden die einzelnen Bewertungen zusammengezählt. Für das gleiche Beispiel hat der Debitor eine Bewertung von 13 (5 + 3 + 5).




