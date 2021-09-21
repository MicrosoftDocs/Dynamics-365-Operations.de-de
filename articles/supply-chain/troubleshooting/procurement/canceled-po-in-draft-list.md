---
title: Stornierte Bestellungen werden in der Entwurfsliste im Arbeitsbereich angezeigt
description: Stornierte Bestellungen werden in der Entwurfsliste im Arbeitsbereich für die Bestellvorbereitung angezeigt
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: f1dc23cd7e5b4b99cb7a9440d7d4666d8396511f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476466"
---
# <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-workspace"></a>Stornierte Bestellungen werden in der Entwurfsliste im Arbeitsbereich angezeigt

## <a name="symptoms"></a>Symptome

Nachdem Sie Bestellungen storniert haben, die im *Bestätigt*-Zustand waren, erscheinen die stornierten Bestellungen im **Bestellvorbereitung**-Arbeitsbereich weiterhin in der Liste der Bestellentwürfe.

## <a name="resolution"></a>Lösung

Dieses Problem tritt nur bei Bestellungen auf, die dem Änderungsmanagement unterliegen. Dies liegt daran, dass die Stornierung als eine Änderung angesehen wird, die genehmigt werden muss. Die Genehmigung kann automatisch vom System erfolgen. Daher besteht der Prozess darin, die stornierte Bestellung an den Genehmigungsworkflow zu senden, damit sie in einen *Genehmigt*-Zustand wechseln kann. Ab diesem Zeitpunkt erscheint die Bestellung nicht mehr im **Bestellvorbereitung**-Arbeitsbereich in der Liste der Bestellentwürfe.
