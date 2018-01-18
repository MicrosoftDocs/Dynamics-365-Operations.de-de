---
title: Auftragssperren
description: "Dieses Thema beschreibt das Sperren von Aufträgen mithilfe von Einzelhandel und Handel in Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: MCRHoldCodeTable, MCRSalesTableOrderHistory, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8b4c8ecbef1dc667d3b60411a53f0c63686529c2
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="order-holds"></a>Auftragssperren

[!include[banner](includes/banner.md)]


Dieses Thema beschreibt das Sperren von Aufträgen mithilfe von Einzelhandel und Handel in Dynamics 365 for Retail.

Ein Auftrag kann aus unterschiedlichen Gründen gesperrt werden. Sie können beispielsweise einen Auftrag sperren, bis eine Debitorenadresse oder eine Zahlungsmethode überprüft werden kann oder bis ein Manager das Kreditlimit des Debitors prüfen kann. Während des Verkaufsprozesses kann es vorkommen, dass Aufträge gesperrt werden müssen. Beispielsweise kann ein Auftrag aufgrund von Problemen bei einer Debitorenzahlung oder eines möglichen Betrugs oder weil ein Manger den Auftrag überprüfen muss, gesperrt werden. Wenn ein Auftrag gesperrt wird, wird diesem ein Code für Auftragssperren zugewiesen, um die Ursache für die Sperre anzugeben. Auftragssperrcodes werden unter **Vertrieb und Marketing** &gt; **Einstellungen** &gt; **Aufträge** &gt; **Auftragssperrcodes** konfiguriert. Ein Auftrag kann zum Zeitpunkt der Auftragserstellung oder später manuell gesperrt werden. Außerdem kann ein Auftrag basierend auf Betrugsregeln automatisch gesperrt werden. Während ein Auftrag gesperrt ist, müssen Sie ihn möglicherweise mit weitere Informationen aktualisieren. Vielleicht möchten Sie den Auftrag auschecken, während Sie weiter daran arbeiten. Sie können einen Auftrag auschecken, ihn wieder einchecken und sogar das Auschecken von einem anderen Benutzer überschreiben, indem Sie die Workbench Auftragssperre (**Einzelhandel** &gt; **Debitoren** &gt; **Auftragssperren**) verwenden. Wenn ein Auftrag abgeschlossen werden kann, müssen Sie die Sperre entfernen, bevor Sie den Bestellvorgang abschließen können.




