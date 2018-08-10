---
title: Serviceobjektgruppen
description: "Objektgruppen sind zum Sortieren und Filtern der Daten von Objekten für Berichte und Statistiken nützlich."
author: ShylaThompson
manager: AnnBe
ms.date: 05/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectGroups
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2ab3ed8a8f36f980473b17b5dfed8cb3d0054253
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="service-object-groups"></a>Serviceobjektgruppen 

[!include [banner](../includes/banner.md)]

Objektgruppen sind zum Sortieren und Filtern der Daten von Objekten für Berichte und Statistiken nützlich. Objekte können z. B. nach der geografischen Position oder nach dem Typ gruppiert werden.

## <a name="group-by-geographical-location"></a>Gruppieren nach geografischer Position

Mit dieser Gruppierungsmethode kann angezeigt werden, wo sich die verschiedenen Objekte befinden, für die das Unternehmen Services anbietet. Das Gruppieren von Objekten nach geografischer Position kann außerdem hilfreich sein, wenn z. B. die Objekte bestimmt werden müssen, für die in einem bestimmten Land oder einer Region bereits Services erbracht werden.

## <a name="example"></a>Beispiel

Ein Debitor aus Belgien ruft beim Kundendienst an und möchte eine Servicevereinbarung für das Objekt ABC erstellen. Sie haben eine Objektgruppe mit geografischer Position Belgien allen Objekten in Belgien zugeordnet. Unter Verwendung dieser Gruppe als Filter kann schnell festgestellt werden, ob ABC bereits als Datensatz in der Anwendung vorhanden ist oder ob ein neues Objekt eingerichtet werden muss. 

## <a name="group-by-type"></a>Gruppieren nach Typ

Mit dieser Gruppierungsmethode kann angezeigt werden, für welche Objekttypen das Unternehmen Services anbietet. Das Gruppieren von Objekten nach Typ kann außerdem hilfreich sein, wenn z. B. ein neues Objekt basierend auf ähnlichen in der Anwendung bereits vorhandenen Objekten erstellt werden soll.

## <a name="example"></a>Beispiel

Ein Debitor ruft an und möchte eine Servicevereinbarung für eine Klimaanlage HIJ einrichten. Für diese Anlage ist noch kein Datensatz vorhanden. Es ist jedoch bereits eine Objektgruppe Klimaanlagen eingerichtet, die allen Klimaanlagenobjekten zugeordnet wurde. Sie können deshalb schnell nach allen anderen Klimaanlagen suchen und die Vorlageninformationen aus diesen Objekten als Grundlage für Servicevertragspositionen für HIJ verwenden. Wenn Sie Objektgruppen auf diese Weise verwenden, können Sie umgehend neue Objekte einrichten und die Serviceaufgaben bestimmen, die dafür ausgeführt werden müssen. 

## <a name="create-service-object-groups"></a>Erstellen von Serviceobjektgruppen

Erstellen von Gruppen, denen Sie Serviceobjekte zuordnen können. Serviceobjekte sind Lagerartikel und andere Produkte, für die Services ausgeführt werden. Wenn Sie Serviceobjekte gruppieren, können Sie Berichte für ähnliche und zugehörige Serviceobjekte erstellen. Beispielsweise kann eine Serviceobjektgruppe aus zwei Serviceobjekten bestehen: Ein Serviceobjekt ist ein Bausatz, und das zweite Serviceobjekt ist der Service, um den Bausatz zu installieren.

Um Serviceobjektgruppen zu erstellen, führen Sie folgende Schritte aus:

1. Klicken Sie auf **Serviceverwaltung > Einstellungen > Serviceobjekte > Serviceobjektgruppen.**

2. Klicken Sie auf **Neu**, um eine neue Serviceobjektgruppe zu erstellen.

3. Geben Sie einen eindeutigen Namen für die Serviceobjektgruppe sowie (optional) eine Beschreibung ein.

Sie können Serviceobjekte der Gruppe zuordnen, indem Sie das Formular **Serviceobjekte** verwenden. 

## <a name="see-also"></a>Siehe auch

[Erstellen von Serviceobjekten](create-service-objects.md)



