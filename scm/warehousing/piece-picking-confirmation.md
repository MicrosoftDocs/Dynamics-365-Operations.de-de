---
title: "Stückentnahmebestätigung"
description: "In diesem Thema wird beschrieben, wie Sie Stückentnahmebestätigung über ein mobiles Gerät einrichten und anwenden."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: c5340f4dacd743600ef955c8d5228d1e2d2d2fa9
ms.contentlocale: de-de
ms.lasthandoff: 06/20/2017

---

# <a name="piece-picking-confirmation"></a>Stückentnahmebestätigung

[!include[banner](../includes/banner.md)]

Die Stückentnahme ermöglicht Ihnen, jedes Teil des Bestands zu bestätigen über Entnahme- oder Inventurarbeit auf einem mobilen Gerät. Bei der Entnahme können Sie die Menge der zu verarbeitenden Arbeit bis zu der Menge bestätigen, die für die zu entnehmende Arbeit angegeben ist. Bei Inventurarbeit können Sie den Bestand scannen, den Sie zählen und die Gesamtsumme nachverfolgen.

Wenn Sie die Stückentnahme aktivieren, wird die Produktbestätigung automatisch aktiviert. Für Arbeitstypentnahmen wird eine maximale Anzahl an Stücken aktiviert. Dadurch wird es Ihnen ermöglicht, eine Maximalzahl an Stücken festzulegen, die während des Arbeitsprozesses bestätigt werden müssen. Die maximale Menge basiert auf der aktuellen Leistungseinheit, die verarbeitet wird. Der Inventurarbeitstyp erlaubt kein Maximum.

Sie können die Menge und die Maßeinheit (UOM) verwenden, die einem gescannten Strichcode zugeordnet ist. Dies funktioniert für den Empfang an eingehenden Flüssen einschließlich des Empfangs gemischter Ladungsträger, Bestellungsartikel, Umlagerungsauftragsartikel und Ladungsartikel. Es funktioniert auch für die Stückentnahme, bei der durch das Scannen des Barcodes die Menge zur Gesamtanzahl bestätigter Stücke hinzugefügt wird und es zu einer Konvertierung zwischen der UOM auf dem Barcode und der Leistungseinheit kommt. Wenn beim Zählen der Maßeinheit im Barcode bestätigt ist, dass die Menge für das Zählen in der Nummernkreisgruppe zulässig ist, wird die Menge zur Gesamtzählung hinzugefügt.

## <a name="where-it-applies"></a>Wofür es angewendet wird

Die Stückentnahme funktioniert für alle Inventurarbeiten und für die Erstentnahme aller Arten von Arbeit. Die Stückentnahme gilt nicht, wenn der Artikel über Seriennummern kontrolliert wird oder wenn es sich um eine Produktions- oder Kanban-Entnahme von einem Ladungsträger-Lagerplatz handelt und der Artikel auf „Staging“ gesetzt ist.

## <a name="set-up-piece-picking"></a>Stückentnahme einrichten

1.  Öffnen Sie über ein Menüelement des mobilen Geräts das Einstellungsformular für Arbeitsbestätigung: Lagerortverwaltung > **Lagerortverwaltung** > **Einstellungen** > **Mobiles Gerät** > **Menüelemente des mobilen Geräts**. 
2. Öffnen Sie über das Menüelement des mobilen Geräts die Einrichtung Arbeitsbestätigung.

Die folgenden Optionen sind zur Auswahl verfügbar, wenn der Arbeitstyp Entnahme oder Inventur ist.

| Mit der folgenden Option...        | Beschreibung   | 
| ------------- | ------------- |
| Stückentnahmebestätigung   | Verfügbar für Entnahme- und Inventurarbeitstypen. Produktbestätigung wird automatisch ausgewählt. Ermöglicht Ihnen, jeden Inventurartikel über das mobile Gerät zu bestätigen. | 
| Maximale Anzahl von Stücken     | Verfügbar für Entnahmearbeit, wenn Stückentnahmebestätigung aktiviert ist. Beschränkt die Anzahl der Teile, die Sie bestätigen müssen. |  

