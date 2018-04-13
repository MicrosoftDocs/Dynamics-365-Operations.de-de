---
title: "Daueraufträge"
description: "Daueraufträge basieren auf einem Aufwandsprojekt. Sie können Daueraufträge auf Basis eines Projekts, über das Formular Serviceabonnement oder mithilfe einer Service-Dauerauftragsgruppe erstellen."
author: YuyuScheller
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bf9df2a31c758ba6b63ac7952e00065df04552dc
ms.openlocfilehash: d785d64e97caabdfb499289c7979654789c97541
ms.contentlocale: de-de
ms.lasthandoff: 02/19/2018

---

# <a name="service-subscriptions"></a>Daueraufträge

[!INCLUDE [banner](../includes/banner.md)]

Daueraufträge basieren auf einem Aufwandsprojekt. Sie können Daueraufträge auf Basis eines Projekts, über das Formular **Serviceabonnement** oder mithilfe einer Service-Dauerauftragsgruppe erstellen.

Für jeden Dauerauftrag kann eine optionale Anzahl von Dauerauftragsgebühren erstellt werden. Bei den Dauerauftragsgebühren handelt es sich um die Buchungen, die dem Debitor in Rechnung gestellt werden.

Mit einem Periodencode wird die Dauer der Periode für die Dauerauftragsgebühr bzw. werden die Intervalle angegeben, in denen der Dauerauftrag fakturiert werden soll.

Der Periodencode wird in der Service-Dauerauftragsgruppe definiert. Er ist für alle Daueraufträge innerhalb der Gruppe festgelegt. Neu erstellte Dauerauftragsgebühren besitzen ein vorgeschlagenes Startdatum. Dabei handelt es sich entweder um das Startdatum der Periode (bei Erstellung der ersten Periode) oder um das Enddatum der vorherigen Periode (bei Erstellung einer weiteren Periode) handelt.



