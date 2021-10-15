---
title: Gefahrengüter
description: Dieses Thema bietet Informationen über Gefahrgutdokumente und Informationen, die in Ihrer Umgebung gespeichert sind.
author: t-benebo
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: benebotg
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: 38e06931b67e53ce37c3228d6ba3db38c0f39f2d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569720"
---
# <a name="hazardous-materials"></a>Gefahrengüter

[!include [banner](../includes/banner.md)]

Informationen zu Gefahrstoffen werden in der Produktinformationsverwaltung eingerichtet. Dieses Modul bietet auch Dokumente, die über die Lagerverwaltung gedruckt werden können.

Wenn Sie Materialien versenden, die als Gefahrgut eingestuft sind, müssen der Sendung zusätzliche Unterlagen beigefügt werden. Mit der Gefahrstofffunktionalität können Kunden Klassifizierungsinformationen speichern und zuweisen, um Artikel freizugeben. Diese Informationen können dann zur Vorbereitung der Versanddokumentation verwendet werden.

> [!IMPORTANT]
> Die Gefahrstoff-Funktionen in Microsoft Dynamics 365 Supply Chain Management bieten eine Sammlung nützlicher Produktinformationsfelder und verknüpfte Funktionen an, mit denen Sie Informationen erfassen und auf sie verweisen können, die sich auf Ihre Gefahrengüter beziehen. Diese Funktionen können Ihnen auch beim Entwerfen und Drucken von Versanddokumenten helfen, die einige der gleichen Informationen zu gefährlichen Stoffen enthalten, die Sie versenden. Durch das System werden Sie jedoch nicht automatisch alle geltenden Bestimmungen in Ihrem Land oder Ihrer Region einhalten. Obwohl diese Tools Ihnen dabei helfen sollen, die gängigen Vorschriften einzuhalten, sind sie an sich weder ausreichend noch garantieren Sie deren vollständige Einhaltung. Ihre Organisation ist dafür verantwortlich, alle geltenden Vorschriften zu kennen und alle erforderlichen Schritte zu unternehmen, um diese einzuhalten.

Bevor Sie diese Funktionalität nutzen können, müssen Sie folgende Einstellungen vornehmen:

- **Produktinformationsverwaltung:** Richten Sie Codes ein, die auf freigegebene Produkte angewendet werden können.
- **Lagerortverwaltung:** Verwenden Sie zusätzliche Versanddokumente, um Versandinformationen auszudrucken.

## <a name="product-information-management"></a>Produktinformationsverwaltung

In der Produktinformationsverwaltung gibt es eine Reihe von Setup-Tabellen, in denen Sie die Referenzinformationen hinzufügen können, die in der Liste für Gefahrgüter für Straßen-, See- und Luftfracht enthalten sind.

Nachfolgend einige der Bestimmungen, auf die oftmals verwiesen wird:

- **ADR** – Vorschriften, die sich auf die internationale Beförderung gefährlicher Güter auf dem Landweg beziehen
- **CFR 49** – Vorschriften der Vereinigten Staaten für die Beförderung gefährlicher Güter
- **IMDG** – Der IMDG-Code (International Marine Dangerous Goods)
- **IATA** – Die Gefahrgutbestimmungen der International Air Transport Association (IATA)

Jede dieser Bestimmungen enthält eine Gefahrgutliste mit Referenzcodes. Die Listen für die einzelnen Transporttypen werden in gemeinsamen internationalen Klassifikationen zusammengefasst. Supply Chain Management bietet eine Referenztabelle für die gemeinsam genutzten Codes in diesen Listen. Jede Liste enthält auch eindeutig definierbare Codes.

Um mit der Konfiguration dieser Informationen zu beginnen, erstellen Sie eine Regelung, mit der Sie die Anfangsparameter konfigurieren können.

## <a name="warehouse-management"></a>Lagerortverwaltung

Wenn eine Lieferung vorbereitet ist, können mehrere neue Berichte gedruckt werden. Für diese Berichte werden die Informationen verwendet, die Sie in der Produktinformationsverwaltung eingerichtet haben.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]