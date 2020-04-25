---
title: Daueraufträge
description: Daueraufträge basieren auf einem Aufwandsprojekt. Sie können Daueraufträge auf Basis eines Projekts, über das Formular Serviceabonnement oder mithilfe einer Service-Dauerauftragsgruppe erstellen.
author: ShylaThompson
manager: tfehr
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4618ea82744b5967cfce8258412e53a7d8aa67f3
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215009"
---
# <a name="service-subscriptions"></a>Daueraufträge

[!include [banner](../includes/banner.md)]

Daueraufträge basieren auf einem Aufwandsprojekt. Sie können Daueraufträge auf Basis eines Projekts, über das Formular **Serviceabonnement** oder mithilfe einer Service-Dauerauftragsgruppe erstellen.

Für jeden Dauerauftrag kann eine optionale Anzahl von Dauerauftragsgebühren erstellt werden. Bei den Dauerauftragsgebühren handelt es sich um die Buchungen, die dem Debitor in Rechnung gestellt werden.

Mit einem Periodencode wird die Dauer der Periode für die Dauerauftragsgebühr bzw. werden die Intervalle angegeben, in denen der Dauerauftrag fakturiert werden soll.

Der Periodencode wird in der Service-Dauerauftragsgruppe definiert. Er ist für alle Daueraufträge innerhalb der Gruppe festgelegt. Neu erstellte Dauerauftragsgebühren besitzen ein vorgeschlagenes Startdatum. Dabei handelt es sich entweder um das Startdatum der Periode (bei Erstellung der ersten Periode) oder um das Enddatum der vorherigen Periode (bei Erstellung einer weiteren Periode) handelt.


