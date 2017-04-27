---
title: RFM-Alyse einrichten
description: "In diesem Thema wird erläutert, wie ein Recency-, Häufigkeits- und monetäre (RFM) Analyse Ihrer Debitoren eingerichtet wird."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 78943
ms.assetid: 8ff9aac3-5ada-4150-85fd-18901c926d53
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: b95d2c4d7d78e8c5ed8d3a04efdd2f8dfe8393ba
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-rfm-analysis"></a>RFM-Alyse einrichten

[!include[banner](includes/banner.md)]


In diesem Thema wird erläutert, wie ein Recency-, Häufigkeits- und monetäre (RFM) Analyse Ihrer Debitoren eingerichtet wird.

RFM-Analysen (Aktualität, Häufigkeit, Geldbetrag) sind ein Marketinginstrument, das Ihre Organisation verwenden kann, um die Daten zu bewerten, die von Debitorenkäufen generiert werden. Nachdem Sie RFM-Analyse eingerichtet haben, wird Debitoren eine berechnete RFM-Punktzahl zugewiesen, während diese Einkäufe tätigen. Die RFM-Punktzahl kann eine dreistellige Bewertung oder eine Gesamtzahl sein, je nachdem, wie Ihre Organisation RFM-Analyse konfiguriert hat. Wenn Ihre Organisation eine dreistellige Bewertung für das Ergebnis verwendet, entspricht die erste Ziffer der Häufigkeit (wann tätigte der Kunden den letzten Einkauf von Ihrer Organisation) Die zweite Stelle ist eine Bewertung der Häufigkeit (wie oft tätigt der Kunde Einkäufe in Ihrer Organisation tätigt). Die dritte Ziffer ist eine Bewertung des Geldbetrags (wie viel gab der Kunde aus, wenn er Einkäufe in Ihrer Organisation tätigt). So verfügt beispielsweise Ihre Organisation ein Bewertungssystem mit einer Skala von 1 bis 5, wobei 5 die höchste Bewertung ist. In diesem Fall gibt die Kundenbewertung 535 Ihnen folgenden Informationen zum Debitor:

-   **Aktualitätsbewertung von 5** – Der Kunde hat erst vor kurzem einen Einkauf getätigt.
-   **Häufigkeitsbewertung 3** - Der Kunde erwirbt Produkte von Ihrer Organisation mit mäßiger Häufigkeit.
-   **Geldbetragwertung 5** - Wenn der Kunde einen Einkauf tätigt, gibt er oder sie einen beträchtlichen Geldbetrag aus.

Wenn Ihre Organisation für die Bewertung eine Aggregatzahl verwendet, werden die einzelnen Bewertungen zusammengezählt. Für das gleiche Beispiel hat der Debitor eine Bewertung von 13 (5 + 3 + 5).




