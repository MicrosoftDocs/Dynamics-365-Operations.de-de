---
title: Gültigkeitsdatum für einen genehmigten Kreditor kann nicht geändert werden
description: In der Liste der genehmigten Kreditoren nach Produktentitäten kann das Gültigkeitsdatum nicht geändert werden.
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
ms.openlocfilehash: cb6dbd134d63daa163261cabdbd7eceb978877ae
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476400"
---
# <a name="cant-change-the-effective-date-for-an-approved-vendor"></a>Gültigkeitsdatum für einen genehmigten Kreditor kann nicht geändert werden


## <a name="symptoms"></a>Symptome

Ein Produkt hat einen genehmigten Lieferanten, der beispielsweise ein Datum des Inkrafttretens am 11. Januar 2018 hat (*01/11/2018*) und ein Ablaufdatum von *Niemals*. Wenn Sie versuchen, das Datum des Inkrafttretens auf den 10. Januar 2018 (*01/10/2018*) oder den 12. Januar 2018 (*01/12/2018*) zu ändern, erhalten Sie folgende Fehlermeldung:

> In der Liste der genehmigten Lieferanten (PdsApproveVendorList) kann kein Datensatz erstellt werden. Der Wert 'Ablauf' muss größer oder gleich dem Wert 'Effektiv' sein.

## <a name="resolution"></a>Lösung

Sie können nur den Zeitraum verlängern, für den der Lieferant zugelassen ist. Dabei gelten folgende Regeln:

- Um das Datum des Inkrafttretens so zu ändern, dass es vor den vorhandenen Datensätzen (Zeiträumen) des Artikelanbieters liegt, muss das Ablaufdatum des neuen Zeitraums vor allen Ablaufdaten in den vorhandenen Datensätzen liegen.
- Um das Ablaufdatum so zu ändern, dass es nach einem der vorhandenen Zeiträume liegt, muss das Datum des Inkrafttretens in jedem vorhandenen Datensatz nach dem letzten Ablaufdatum liegen.
- Um den Gesamtzeitraum zu verkürzen, für den der Lieferant zugelassen ist, müssen Sie vorhandene Datensätze löschen oder ändern. Alternativ können Sie während des Imports den **kürzen**-Umschalter verwenden. Dieser Schalter löscht alle vorhandenen Datensätze in der Tabelle für genehmigte Lieferanten nach Artikel.

Für das in der Problembeschreibung beschriebene Beispielszenario, in dem ein Datensatz das Datum des Inkrafttretens von *01/11/2018* hat und ein Ablaufdatum von *Niemals*, können Sie einen neuen Datensatz mit dem Datum des Inkrafttretens von *01/10/2018* und ein Ablaufdatum von *Niemals* importieren. Sie können den Zeitraum jedoch nicht verkürzen, sodass das Datum des Inkrafttretens über die Datenverwaltung auf *01/12/2018* aktualisiert wird. Sie müssen diese Änderung über die Benutzeroberfläche vornehmen.
