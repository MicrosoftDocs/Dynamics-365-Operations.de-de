---
title: Buchhaltungsverteilungen sind entweder über- oder unterverteilt
description: Eine oder mehrere Buchhaltungsverteilungen sind entweder über- oder unterverteilt.
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
ms.openlocfilehash: 7ff0172469df50da9e4272b3fa3f75001a4eb7eb
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476442"
---
# <a name="accounting-distributions-are-either-over--or-under-distributed"></a>Buchhaltungsverteilungen sind entweder über- oder unterverteilt


## <a name="symptoms"></a>Symptome

Sie erhalten den folgenden Fehler:

> Eine oder mehrere Buchhaltungsverteilungen sind entweder über- oder unterverteilt

## <a name="cause"></a>Ursache

Dieses Problem kann aufgrund von Inkonsistenzen bei der Verteilung von Bestellungen auftreten.

## <a name="resolution"></a>Lösung

So entsperren Sie dieses Problem und setzen die Bestellung auf den *Entwurf*-Zustand zurück. Gehen Sie zu **Beschaffung \> Periodische Aufgaben \> Bereinigen \> Zurücksetzen der Bestellverteilung**. Weitere Informationen finden Sie im folgenden Blog-Beitrag: [Beheben von Bestellungsverteilungsfehlern in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).
