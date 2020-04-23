---
title: Gefahrengüter
description: Dieses Thema bietet Informationen über Gefahrgutdokumente und Informationen, die in Ihrer Umgebung gespeichert sind.
author: lachlancashMS
manager: tfehr
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5006f06d90ddcc314a51878e9e21337de7d493e7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208460"
---
# <a name="hazardous-materials"></a>Gefahrengüter

[!include [banner](../includes/banner.md)]

Informationen zu Gefahrstoffen werden in der Produktinformationsverwaltung eingerichtet. Dieses Modul bietet auch Dokumente, die über die Lagerverwaltung gedruckt werden können.

Wenn Sie Materialien versenden, die als Gefahrgut eingestuft sind, müssen der Sendung zusätzliche Unterlagen beigefügt werden. Mit der Gefahrstofffunktionalität können Kunden Klassifizierungsinformationen speichern und zuweisen, um Artikel freizugeben. Diese Informationen können dann zur Vorbereitung der Versanddokumentation verwendet werden.

> [!IMPORTANT]
> Zur Erleichterung der Verwaltung von Gefahrgutlieferungen ermöglicht Microsoft Dynamics 365 Supply Chain Management Ihnen, zusätzliche Referenzinformationen einzurichten, die sich auf Produkte beziehen. Sie können auch zusätzliche Versanddokumente einrichten. Das System entspricht jedoch nicht automatisch den Bestimmungen Ihres Landes oder Ihrer Region. Stattdessen kommt ein Tool zum Einsatz, das Ihr Programm insgesamt unterstützt.

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