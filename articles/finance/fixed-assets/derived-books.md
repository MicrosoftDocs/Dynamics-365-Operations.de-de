---
title: Abgeleitete Bücher
description: Dieser Artikel enthält eine Übersicht der Funktion für abgeleitete Bücher.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a649fdbc355b3382bc6c80be03f8b37a06d5226
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177893"
---
# <a name="derived-books"></a>Abgeleitete Bücher

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält eine Übersicht der Funktion für abgeleitete Bücher.

Abgeleitete Wertmodelle sollen Wertmodellbuchungen für Anlagen vereinfachen, die in regelmäßigen Zeitabständen erfolgen.  Sie wählen ein Buch als primäres Buch aus. Dies ist üblicherweise das Buch für die buchhalterische Abschreibung. Anschließend werden diesem Buch andere Bücher zugeordnet, die für Buchungen in den gleichen Intervallen eingerichtet werden wie das primäre Buch. Bücher für steuerliche Abschreibung werden oft als abgeleitete Bücher eingerichtet. 

Die häufigsten Posten, die zum Buchen in abgeleitete Abschreibungsbücher eingerichtet werden, sind Anschaffungen, Anschaffungsänderungen und Veräußerungen. 

## <a name="example"></a>Beispiel

Buch B und Buch C werden als abgeleitete Bücher für Buch für A die Buchungsart "Anschaffung" eingerichtet. Im Buch A wird eine Anschaffungsbuchung für die Anlage 123 mit einem Wert von 1.500,00 Einheiten eingegeben. 

Beim Buchen wird eine Anschaffungsbuchung in der Anlage 123 für das Buch B und in der Anlage 123 für das Buch C mit einem Wert von 1.500,00 Einheiten generiert und gebucht. Wenn Sie die Buchungen des primären Buchs in der Anlagenerfassung zur Ausführung vorbereiten, können Sie auch die Buchungen der abgeleiteten Abschreibungsbücher anzeigen und ändern. Wenn Sie die Buchungen des primären Buchs in einer anderen Erfassung vorbereiten, werden die Buchungen des abgeleiteten Werts nicht angezeigt. Sie werden aber beim Buchen der Posten des primären Buchs auf die entsprechenden Konten und Buchungsebenen gebucht.

> [!NOTE]                                                                                                                               
> Bücher, die zum Buchen von Posten in Intervallen eingerichtet werden, bei denen es sich nicht um die Intervalle des primären Buches handelt, müssen der Anlage als separate Bücher (und nicht als abgeleitete Bücher) zugeordnet werden.  

Weitere Informationen finden Sie unter [Buchen mit abgeleiteten Büchern](post-derived-value-models.md).



