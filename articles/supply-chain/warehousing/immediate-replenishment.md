---
title: Sofortige Wiederbeschaffung
description: In diesem Thema wird beschrieben, wie Sie die sofortige Wiederbeschaffung verwenden können, um den Lagerbestand wieder zu ergänzen, wenn eine Lagerplatzdirektive keinen Bestand zuordnen kann.
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSReplenishmentTemplates
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 3def95ac272a424591ed4382d5cd5841bc663654
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235387"
---
# <a name="immediate-replenishment"></a>Sofortige Wiederbeschaffung

[!include [banner](../includes/banner.md)]

Mit der sofortigen Wiederbeschaffung können Sie Bestand sofort wiederbeschaffen, nachdem eine Lagerplatzdirektivenposition keinen Bestand zuteilen kann. Die Wiederbeschaffung basiert auf einer einzelnen Position in den Einstellungen der Lagerplatzdirektive. Wenn Lagerbestand nicht in der Maßeinheit vorhanden ist, die durch diese Position angegeben ist, erfolgt die Wiederbeschaffung dieser Maßeinheit umgehend.

Die sofortige Wiederbeschaffung bietet eine Alternative zur Methode, bei der die Zuteilung von Bestand auf mehr Positionen in der Lagerplatzdirektive basiert und bei der die Nachfrage am Ende der Zuteilung summiert und in der Maßeinheit wiederbeschafft wird, die durch die letzte Position in der Lagerplatzdirektive angegeben ist.

Die Vorteile der Verwendung der sofortigen Wiederbeschaffung bestehen darin, dass die Wiederbeschaffung auf bestimmte Einheiten begrenzt werden kann und die Menge an bestimmte Lagerplätzen gerichtet werden kann.

## <a name="business-scenario"></a>Geschäftsszenario

Beispielsweise haben Sie einen Lagerort, der separate Entnahmebereiche für die Maßeinheiten „Schachtel” und „Jeder/-e/-es” hat. Sie möchten den Kommissionierprozess optimieren, indem so viele Schachteln wie möglich entnommen werden und dann die verbleibende Menge, die weniger als eine Schachtel ausmacht, aus dem Bereich „Jeder/-e/-es” entnommen wird.

In diesem Fall können Sie die sofortige Wiederbeschaffung verwenden. In den Lagerplatzdirektiven können Sie die sofortige Wiederbeschaffung für Kartons einrichten, sodass die Bedarfswiederbeschaffung verwendet wird, sobald es einen Mangel an Schachteln gibt, die aus der Bedarfsmenge entnommen werden können. Hierdurch optimieren Sie den Entnahmeprozess, sodass die Entnahme so viele Schachteln wie möglich umfasst. Durch die sofortige Wiederbeschaffung wird eine Wiederbeschaffung der Schachteln generiert, und der Bedarf wird nicht übergeben, sodass die Mengen in der Maßeinheit „Jeder/-e/-es” entnommen werden. Das bedeutet in anderen Worten, dass nur die Mengen, die in der Maßeinheit „Jeder/-e/-es” entnommen werden sollen (das heißt, Mengen, die weniger als eine Schachtel umfassen), aus dem Bereich „Jeder/-e/-es” entnommen werden. Wenn ein Mangel im Bereich „Schachtel” auftritt, können Sie so viele Schachteln wie möglich aus dem Gesamtbedarf entnehmen. Die verbleibenden Mengen werden dann aus dem Bereich „Jeder/-e/-es” entnommen.

## <a name="where-it-applies"></a>Wofür es angewendet wird

Sofortige Wiederbeschaffung wird während der Wellenausführung verwendet, wenn die Zuteilung für eine Lagerplatzdirektivenposition, für die eine Wiederbeschaffungsvorlage festgelegt ist, fehlschlägt.

## <a name="set-up-immediate-replenishment"></a>Sofortige Wiederbeschaffung einrichten

- Wechseln Sie zu **Lagerortverwaltung** \> **Setup** \> **Lagerplatzdirektiven**, und wählen Sie dann auf der Registerkarte **Positionen** in der Liste **Sofortige Wiederbeschaffungsvorlage** eine Wiederbeschaffungsvorlage für Wellenbedarf aus.

Die Wiederbeschaffungsvorlage wird angewendet, wenn die Lagerplatzdirektivenposition keine dedizierte Maßeinheit zuteilen kann.

## <a name="troubleshooting"></a>Problembehandlung

Wenn die sofortige Wiederbeschaffung für eine Lagerplatzdirektivenposition ausgewählt ist, aber keine Wiederbeschaffungsarbeit generiert ist, wenn Sie die Bedarfswiederbeschaffungsvorlagen für diese Lagerplatzdirektivenposition verwenden, müssen zwei Hauptursachen untersucht werden:

- Stellen Sie sicher, dass die Bedarfswiederbeschaffungsvorlage, die angewendet wird, für die Verwendung der korrekten Lagerplatzvorlagen und Arbeitsvorlagen des Typs **Wiederbeschaffung** eingerichtet ist.
- Stellen Sie sicher, dass es genügend verfügbaren Lagerbestand an den Lagerplätzen gibt, in denen die Bedarfswiederbeschaffungsvorlage nach verfügbarem Lagerbestand für die Wiederbeschaffung sucht.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]