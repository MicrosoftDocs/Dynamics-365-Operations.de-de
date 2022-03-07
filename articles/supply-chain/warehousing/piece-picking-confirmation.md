---
title: Stückentnahmebestätigung
description: Die Stückentnahme ermöglicht Ihnen, jedes Teil des Bestands zu bestätigen über Entnahme- oder Inventurarbeit auf einem mobilen Gerät.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFAutoConfirm, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f9da533998341de60d210e196baae64d285d372
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818847"
---
# <a name="piece-picking-confirmation"></a>Stückentnahmebestätigung

[!include [banner](../includes/banner.md)]

Die Stückentnahme ermöglicht Ihnen, jedes Teil des Bestands zu bestätigen über Entnahme- oder Inventurarbeit auf einem mobilen Gerät. Bei der Entnahme können Sie die Menge der zu verarbeitenden Arbeit bis zu der Menge bestätigen, die für die zu entnehmende Arbeit angegeben ist. Bei Inventurarbeit können Sie den Bestand scannen, den Sie zählen und die Gesamtsumme nachverfolgen.

Wenn Sie die Stückentnahme aktivieren, wird die Produktbestätigung automatisch aktiviert. Für Arbeitstypentnahmen können Sie eine maximale Anzahl an Stücken festlegen. Dadurch wird es Ihnen ermöglicht, eine Maximalzahl an Stücken festzulegen, die während des Arbeitsprozesses bestätigt werden müssen. Die maximale Menge basiert auf der aktuellen Leistungseinheit, die verarbeitet wird. Der Inventurarbeitstyp erlaubt kein Maximum.

Sie können die Menge und die Maßeinheit (UOM) verwenden, die einem gescannten Strichcode zugeordnet ist. Dies funktioniert für den Empfang an eingehenden Flüssen einschließlich des Empfangs gemischter Ladungsträger, Bestellungsartikel, Umlagerungsauftragsartikel und Ladungsartikel. Es funktioniert auch für die Stückentnahme, bei der durch das Scannen des Barcodes die Menge zur Gesamtanzahl bestätigter Stücke hinzugefügt wird und es zu einer Konvertierung zwischen der UOM auf dem Barcode und der Leistungseinheit kommt. Wenn beim Zählen der Maßeinheit im Barcode bestätigt ist, dass die Menge für das Zählen in der Nummernkreisgruppe zulässig ist, wird die Menge zur Gesamtzählung hinzugefügt.

## <a name="where-it-applies"></a>Wofür es angewendet wird

Die Stückentnahme funktioniert für alle Inventurarbeiten und für die Erstentnahme aller Arten von Arbeit. Die Stückentnahme gilt nicht, wenn der Artikel über Seriennummern kontrolliert wird oder wenn es sich um eine Produktions- oder Kanban-Entnahme von einem Ladungsträger-Lagerplatz handelt und der Artikel auf „Staging“ gesetzt ist.

## <a name="set-up-piece-picking"></a>Stückentnahme einrichten

1.  Öffnen Sie über ein Menüelement des mobilen Geräts das Einstellungsformular für Arbeitsbestätigung: Lagerortverwaltung > **Lagerortverwaltung** > **Einstellungen** > **Mobiles Gerät** > **Menüelemente des mobilen Geräts**. 
2. Öffnen Sie über das Menüelement des mobilen Geräts die Einrichtung Arbeitsbestätigung.

Die folgenden Optionen sind zur Auswahl verfügbar, wenn der Arbeitstyp Entnahme oder Inventur ist.


|           Mit der folgenden Option...           |                                                                            Beschreibung                                                                            |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Stückentnahmebestätigung | Verfügbar für Entnahme- und Inventurarbeitstypen. Produktbestätigung wird automatisch ausgewählt. Ermöglicht Ihnen, jeden Inventurartikel über das mobile Gerät zu bestätigen. |
|  Maximale Anzahl von Stücken  |                   Verfügbar für Entnahmearbeit, wenn Stückentnahmebestätigung aktiviert ist. Beschränkt die Anzahl der Teile, die Sie bestätigen müssen.                   |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]