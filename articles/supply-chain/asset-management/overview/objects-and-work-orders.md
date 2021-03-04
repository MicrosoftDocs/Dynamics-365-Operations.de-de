---
title: Anlagen und Arbeitsaufträge
description: In diesem Thema werden Anlagen und Arbeitsaufträge in Asset Management beschrieben.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c2500a695fcffe0d60ac13b1b74cda4322b0e14
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428745"
---
# <a name="assets-and-work-orders"></a>Anlagen und Arbeitsaufträge

[!include [banner](../../includes/banner.md)]

 

In diesem Thema werden Anlagen und Arbeitsaufträge in Asset Management beschrieben. Anlagen und Arbeitsaufträge sind die zentralen Teile von Asset Management. Eine *Anlage* ist eine Maschine oder ein Maschinenteil, die bzw. das fortlaufende Wartung und kontinuierlichen Service benötigt. Anlagen können in einer hierarchischen Struktur erstellt werden, und sie können funktionalen Standorten zugeordnet sein. Wartungsaufträge können auf allen Ebenen der Anlagenstruktur geplant werden.

Verschiedene Daten wie z. B. Produktinformationen und Anlagenspezifikationen sowie erforderliche Wartungspläne werden für jede Anlage eingerichtet. Die folgende Abbildung zeigt einen Überblick über Anlagendaten und die Zugehörigkeit von Anlagen zu Einzelvorgangstypen. Roter Text wird für Beispiele verwendet, die Vererbung und Abhängigkeiten zeigen.

![Diagramm mit Anlagendaten, die Einzelvorgangstypen zugeordnet sind](media/05-overview-image.png)

Jeder Arbeitsauftrag hat einen Arbeitsauftragstyp, wie z. B. vorbeugende Wartung, korrektive Wartung oder Inspektion. Der Arbeitsauftrag enthält einen oder mehrere Arbeitsauftragseinzelvorgänge. Jeder Arbeitsauftragseinzelvorgang definiert einen Einzelvorgang, der für eine Anlage ausgeführt werden muss, und einen zugehörigen Einzelvorgangstyp. Beispiele für zugehörige Einzelvorgangstypen sind 10.000 km, 50.000 km, Überholung nach 1 Jahr und Sicherheitsprüfung. Ein Arbeitsauftrag kann mehreren Anlagen zugeordnet werden.

Die folgende Abbildung zeigt einen Überblick über die wichtigsten Daten in einem Arbeitsauftrag.

![Diagramm mit Schlüsseldaten, die einem Arbeitsauftrag zugeordnet sind](media/06-overview-image.png)

Ein Arbeitsauftrag kann einem anderen Arbeitsauftrag zugeordnet werden, und Einzelvorgangstypen können aufeinander folgende Einzelvorgänge enthalten, die einen Arbeitsauftrag bilden. Im Allgemeinen gibt es keine Abhängigkeiten zwischen Arbeitsaufträgen. Daher kann sich ihr Arbeitsauftrags-Lebenszyklusstatus ändern und sie können unabhängig voneinander geplant werden.

Arbeitsaufträge können auf verschiedene Weise erstellt werden, die der korrektiven, vorbeugenden oder reagierenden Wartung zugeordnet sind. Sie können Arbeitsaufträge auch manuell erstellen. Die folgende Abbildung zeigt einen Überblick über den Prozess der automatischen oder manuellen Erstellung von Arbeitsaufträgen.

![Diagramm, das die automatische oder manuelle Erstellung von Arbeitsaufträgen zeigt](media/07-overview-image.png)

Mehrere Schritte müssen ausgeführt werden, wenn Sie einen Wartungsauftrag für einen Arbeitsauftrag planen und ausführen möchten. Die folgende Abbildung zeigt einen Überblick über die Verarbeitung eines Arbeitsauftrags.

![Diagramm, das einen Überblick über die Bearbeitung eines Arbeitsauftrags zeigt](media/08-overview-image.png)

> [!NOTE]
> Wenn Sie in Dynamics 365 Supply Chain Management und dem Modul **Asset Management** arbeiten, wählen Sie normalerweise **Neu**, um einen neuen Datensatz zu erstellen, **Bearbeiten**, um einen vorhandenen Datensatz zu aktualisieren, und **Speichern**, um die neuen oder bearbeiteten Daten zu speichern.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]