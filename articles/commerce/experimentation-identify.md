---
title: Eine Hypothese identifizieren und Metriken für ein Experiment bestimmen
description: In diesem Thema wird beschrieben, wie Sie die Hypothesen und Erfolgsmetriken für ein Experiment identifizieren, das Sie auf einer E-Commerce-Website in Dynamics 365 Commerce ausführen.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 99642861d69b7545f03c6ed2c2650eadeb377534
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930202"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a>Eine Hypothese identifizieren und Erfolgsmetriken für ein Experiment bestimmen
Die erste Phase im Experimentierlebenszyklus umfasst das Identifizieren der Hypothese für das Experiment und das Bestimmen der Metriken, die Sie verfolgen, um den Erfolg zu bewerten. Das folgende Diagramm zeigt alle Schritte, die am [Einrichten und Ausführen eines Experiments](experimentation-overview.md) auf einer E-Commerce-Website in Dynamics 365 Commerce beteiligt sind. Weitere Schritte werden in separaten Themen behandelt. 

[ ![User Journey zum Experimentieren – Identifizierung](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)

Eine Hypothese ist eine Aussage, bei der Sie das Ergebnis des Experiments vorhersagen. Bei der Definition einer Hypothese spielen viele Faktoren eine Rolle, z. B. die Untersuchung des Nutzerverhaltens und der von Ihnen gesammelten Website-Daten. Mit der Hypothese definieren Sie die Annahme oder Theorie, die Sie mit Ihrem Experiment validieren möchten. Ein Beispiel für eine Hypothese für Ihr Experiment könnte „*Ein Bild eines weißen T-Shirts auf meiner Homepage führt in den Sommermonaten zu einer höheren Klickrate als ein Marinepullover, da die Leute im Sommer etwas Leichtes und Helles tragen möchten*“ lauten. In diesem Fall erstellen Sie Variationen, die ein weißes T-Shirt und einen Marinepullover enthalten, und veröffentlichen beide gleichzeitig.

Um eine Hypothese zu validieren, sollte der Erfolg oder Misserfolg eines Experiments direkt mit Benutzeraktionen verknüpft werden. Zum Beispiel, wenn der Benutzer der Website auf einen Link oder eine Schaltfläche klickt. Diese Aktionen müssen mit Ereignissen übereinstimmen, die an den Drittanbieter gemeldet werden, der das Experiment verfolgt. Mit der Zeit wird der Prozentsatz der Benutzer, die die Aktion ausführen, als Metrik ermittelt, mit der Sie Berichte erstellen und Analysen durchführen können. Im Thema [Commerce-Komponentenereignisse für Diagnose und Problembehandlung](dev-itpro/retail-component-events-diagnostics-troubleshooting.md) finden Sie alle verfügbaren Ereignisse und Attribute.

## <a name="previous-step"></a>Vorheriger Schritt
[Experimentieren in Dynamics 365 Commerce](experimentation-overview.md)


## <a name="next-step"></a>Nächster Schritt
[Einrichten eines Experiments](experimentation-setup.md)
