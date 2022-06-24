---
title: Gefahrstoffübersicht
description: Dieser Artikel bietet einen Überblick über Funktionen, die sich auf die Handhabung und Dokumentation gefährlicher Materialien während der Produktinformationsverwaltung und der Lagerverwaltung beziehen.
author: t-benebo
ms.date: 06/10/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: c2cae4cb65dd163e9fbf1d24cff5a0a040e3ce3a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905804"
---
# <a name="hazardous-materials-overview"></a>Gefahrstoffübersicht

[!include [banner](../includes/banner.md)]

Um die Liefer- und Transportvorschriften einzuhalten, müssen Organisationen, die Materialien liefern, die als gefährliche Güter eingestuft sind, zusätzliche Papiere ihren Lieferungen beifügen. Mit der Gefahrstofffunktion können Kunden Informationen speichern, die sich auf zugelassene Artikel beziehen. Diese Informationen können dann zur Vorbereitung der Versanddokumentation verwendet werden. Eine Organisation, die gefährliche Güter versendet, muss über eigene Prozesse und Prozeduren zur Verwaltung des Lieferprozesses verfügen. Microsoft Dynamics 365 Supply Chain Management ist nur ein Tool, mit dem Sie die erforderlichen Dokumente leichter erstellen können.

Das folgende Diagramm zeigt die Schritte, die zum Einrichten und Verwenden der Gefahrstofffunktion erforderlich sind.

![Einrichtung und Verwendung der Gefahrstofffunktion.](media/hazmat-overview.png "Einrichtung und Verwendung der Gefahrstofffunktion")

Die Gefahrstofffunktion wird in der Produktinformationsverwaltung eingerichtet und bietet Dokumente, die über die Lagerverwaltung gedruckt werden können. Daher sind diese Bereiche im Großen und Ganzen die beiden Hauptbereiche, in denen Sie die Funktionen dieser Funktion überprüfen, einrichten und verwenden:

- **Produktinformationsverwaltung** – Richten Sie Codes ein, die auf ein freigegebenes Produkte angewendet werden.
- **Lagerverwaltung** – Arbeiten Sie mit zusätzlichen Lieferdokumenten, die für Lieferungen gedruckt werden.

> [!IMPORTANT]
> Die Gefahrstoff-Funktionen in Supply Chain Management bieten eine Sammlung nützlicher Produktinformationsfelder und verknüpfte Funktionen an, mit denen Sie Informationen erfassen und auf sie verweisen können, die sich auf Ihre Gefahrengüter beziehen. Diese Funktionen können Ihnen auch beim Entwerfen und Drucken von Versanddokumenten helfen, die einige der gleichen Informationen zu gefährlichen Stoffen enthalten, die Sie versenden. Durch das System werden Sie jedoch nicht automatisch alle geltenden Bestimmungen in Ihrem Land oder Ihrer Region einhalten. Obwohl diese Tools Ihnen dabei helfen sollen, die gängigen Vorschriften einzuhalten, sind sie an sich weder ausreichend noch garantieren Sie deren vollständige Einhaltung. Ihre Organisation ist dafür verantwortlich, alle geltenden Vorschriften zu kennen und alle erforderlichen Schritte zu unternehmen, um diese einzuhalten.

## <a name="product-information-management"></a>Produktinformationsverwaltung

Die Produktinformationsverwaltung bietet eine Reihe von Setup-Tabellen, in denen Sie die Referenzinformationen eingeben können für die verschiedenen Listen von Gefahrgütern für Straßen-, Luft- und Seefracht.

Bei der Entwicklung dieser Funktionalität wurde auf die folgenden allgemeinen Vorschriften verwiesen:

- **ADR** – Vorschriften, die sich auf die internationale Beförderung gefährlicher Güter auf dem Landweg beziehen
- **CFR 49** – Vorschriften der Vereinigten Staaten für die Beförderung gefährlicher Güter
- **IMDG** – Der IMDG-Code (International Marine Dangerous Goods)
- **IATA** – Die Gefahrgutbestimmungen der International Air Transport Association (IATA)

Jedes Regelwerk enthält standardisierte Listen gefährlicher Güter und Referenzcodes. Supply Chain Management bietet daher eine Referenztabelle für die gemeinsam genutzten Codes in diesen Listen. Jede Liste enthält auch eindeutig Codes, die Sie definieren können.

Weitere Informationen zum Einrichten von Vorschriften und Werten für gefährliche Stoffe und zum Zuweisen der Werte zu relevanten Produkten finden Sie in den folgenden Artikel:

- [Gefahrengüter einrichten](hazmat-setup.md)
- [Gefährliche Stoffe in Produkten, Bestellungen, Lieferungen und Ladungen](hazmat-items.md)

## <a name="warehouse-management"></a>Lagerortverwaltung

Wenn Sie eine Lieferung in der Lagerverwaltung vorbereiten, können Sie mehrere neue Berichte drucken, die die Informationen verwenden, die Sie in der Produktinformationsverwaltung eingerichtet haben. Weitere Informationen zu den verfügbaren Berichten und deren Verwendung finden Sie unter [Anfragen und Berichte zu Gefahrstoffen](hazmat-reports.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]