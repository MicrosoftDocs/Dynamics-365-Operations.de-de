---
title: Serviceobjekte – Übersicht
description: Dieser Artikel gibt einen Überblick über das Arbeiten mit Serviceobjekten.
author: sorenva
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8150a94677fe38f4caa6f3e0b5fb5d1be5972eaf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862410"
---
# <a name="service-objects-overview"></a>Serviceobjekte – Übersicht

[!include [banner](../includes/banner.md)]

Serviceobjekte sind die Anlagen und Produkte eines Debitors, für die Sie eine Dienstleistung durchführen können. Abhängig von der Art der angebotenen Dienstleistung handelt es sich entweder um ein materielles oder um ein immaterielles Objekt:

-  Materielle Objekte sind Dinge wie Maschinen oder Gebäude, für die eine physische Serviceaufgabe ausgeführt werden kann.

    Bei einem materiellen Serviceobjekt kann es sich auch um einen Lagerartikel handeln, den Sie in den freigegebenen Produktdetails erstellen. Abhängig von der zugeordneten Lagerungsdimensionsgruppe, die Sie dem Artikel zuweisen, können Sie ein Serviceobjekt bis hinunter zu einer Ebene erstellen, die die Artikelseriennummer enthält. Dies ist hilfreich, wenn der exakte Artikel verfolgt werden muss, für den das Serviceobjekt steht.

    Ein materielles Serviceobjekt kann auch ein Artikel sein, der nicht direkt mit der direkten Produktion oder Lieferkette des Unternehmens verbunden ist. So kann ein Tool-Kit, das für Reparaturen in einem Serviceauftrag verwendet wird, ein Serviceobjekt sein, das nicht in den Bestand einbezogen wird. In diesem Fall erfassen Sie es nicht als Lagerartikel.

-  Immaterielle Objekte sind nicht physische Dinge, wie ein Konto oder ein Vertrag, für die Sie eine Serviceaufgabe ausgeführen können.

## <a name="example-of-an-intangible-service-object"></a>Beispiel für ein immaterielles Serviceobjekt

Unternehmen A verwaltet die Finanzdatensätze für eine Reihe von kleinen Unternehmen. Einer der Kunden von Unternehmen A ist das lokale Fußballteam, für das Unternehmen A die wöchentliche Buchführung sowie die Jahresabschlussprüfung der Konten des Vereins durchführt. Die Konten des Vereins werden im Formular Dienstleistungsobjekte eingerichtet und als das Objekt im Servicevertrag angegeben. Es gibt zwei Servicevertragspositionen für das Objekt. Position 1 ist die wöchentliche Buchführung mit einem wöchentlichen Intervall, das der Position zugeordnet ist, und Position 2 ist die Jahresabschlussprüfung mit einem jährlichen Intervall, das ihr zugeordnet ist.

## <a name="related-articles"></a>Zugehörige Artikel

[Erstellen von Serviceobjekten](create-service-objects.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]