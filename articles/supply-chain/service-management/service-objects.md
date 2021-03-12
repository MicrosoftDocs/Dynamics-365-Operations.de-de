---
title: Übersicht der Serviceobjekte
description: Serviceobjekte sind die Anlagen und Produkte eines Debitors, für die Sie eine Dienstleistung durchführen können.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1e0a40d351150ce432164438cd9680cf80792e1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974309"
---
# <a name="service-objects-overview"></a>Übersicht der Serviceobjekte

[!include [banner](../includes/banner.md)]

Serviceobjekte sind die Anlagen und Produkte eines Debitors, für die Sie eine Dienstleistung durchführen können. Abhängig von der Art der angebotenen Dienstleistung handelt es sich entweder um ein materielles oder um ein immaterielles Objekt:

-  Materielle Objekte sind Dinge wie Maschinen oder Gebäude, für die eine physische Serviceaufgabe ausgeführt werden kann.

    Bei einem materiellen Serviceobjekt kann es sich auch um einen Lagerartikel handeln, den Sie in den freigegebenen Produktdetails erstellen. Abhängig von der zugeordneten Lagerungsdimensionsgruppe, die Sie dem Artikel zuweisen, können Sie ein Serviceobjekt bis hinunter zu einer Ebene erstellen, die die Artikelseriennummer enthält. Dies ist hilfreich, wenn der exakte Artikel verfolgt werden muss, für den das Serviceobjekt steht.

    Ein materielles Serviceobjekt kann auch ein Artikel sein, der nicht direkt mit der direkten Produktion oder Lieferkette des Unternehmens verbunden ist. So kann ein Tool-Kit, das für Reparaturen in einem Serviceauftrag verwendet wird, ein Serviceobjekt sein, das nicht in den Bestand einbezogen wird. In diesem Fall erfassen Sie es nicht als Lagerartikel.

-  Immaterielle Objekte sind nicht physische Dinge, wie ein Konto oder ein Vertrag, für die Sie eine Serviceaufgabe ausgeführen können.

## <a name="example-of-an-intangible-service-object"></a>Beispiel für ein immaterielles Serviceobjekt

Unternehmen A verwaltet die Finanzdatensätze für eine Reihe von kleinen Unternehmen. Einer der Kunden von Unternehmen A ist das lokale Fußballteam, für das Unternehmen A die wöchentliche Buchführung sowie die Jahresabschlussprüfung der Konten des Vereins durchführt. Die Konten des Vereins werden im Formular Dienstleistungsobjekte eingerichtet und als das Objekt im Servicevertrag angegeben. Es gibt zwei Servicevertragspositionen für das Objekt. Position 1 ist die wöchentliche Buchführung mit einem wöchentlichen Intervall, das der Position zugeordnet ist, und Position 2 ist die Jahresabschlussprüfung mit einem jährlichen Intervall, das ihr zugeordnet ist.

## <a name="related-topics"></a>Verwandte Themen

[Erstellen von Serviceobjekten](create-service-objects.md)

