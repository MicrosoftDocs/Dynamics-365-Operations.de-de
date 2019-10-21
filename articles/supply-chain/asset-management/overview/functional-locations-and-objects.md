---
title: Funktionale Standorte und Anlagen
description: In diesem Thema werden funktionale Standorte und Anlagen in Asset Management beschrieben. Asset Management ist ein erweitertes Modul für die Verwaltung von Anlagen und Wartungsaufgaben in Dynamics 365 Supply Chain Management.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5271b673d758608cae8e43d72b7e75b259d5f142
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024613"
---
# <a name="functional-locations-and-assets"></a>Funktionale Standorte und Anlagen

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

In diesem Thema werden funktionale Standorte und Anlagen in Asset Management beschrieben. Asset Management ist ein erweitertes Modul für die Verwaltung von Anlagen und Wartungsaufgaben in Dynamics 365 Supply Chain Management.

## <a name="overview"></a>Übersicht

Asset-Management ist nahtlos in mehrere Module aus dem Bereich Finance and Operations integriert. Die folgende Abbildung zeigt die Schnittstellen mit anderen Modulen.

![Abbildung 1](media/01-overview-image.png)

Mit Asset Management können Sie effizient alle Aufgaben verwalten und ausführen, die mit dem Verwalten und der Wartung von viele Arten von Ausrüstung in Ihrem Unternehmen zusammenhängen. Zu diesen Ausrüstungsgegenständen zählen Maschinen, Produktionsanlagen und Fahrzeuge. Asset Management unterstützt außerdem Lösungen über zahlreiche Branchen hinweg.

Die folgende Abbildung zeigt einen Überblick über die Hauptfunktionen von Asset Management.

![Abbildung 2](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a>Funktionale Standorte und Anlagen

Funktionale Standorte werden verwendet, um Anlagen an Standorten zu verwalten. Zu dieser Verwaltung gehört das Nachverfolgen von Anlagenkosten an funktionalen Standorten. Funktionale Standorte werden hierarchisch strukturiert, und Standorte können untergeordnete Standorte haben. Die Struktur funktionaler Standorte ist statisch. Dies bedeutet, das Standorte den Ort nicht ändern können. Anlagen können an funktionalen Standorten installiert sein und können bei Bedarf später an anderen funktionalen Standorten installiert werden.

Anlagenkosten folgen immer dem Standort der Anlage. Dies bedeutet Folgendes: Wenn Sie eine Anlage an einem neuen funktionalen Standort einrichten, verwendet die Anlage automatisch die Finanzdimensionen, die sich auf den neuen funktionalen Standort beziehen. Daher beziehen sich Anlagenkosten immer auf den funktionalen Standort, an dem die Anlage derzeit installiert ist. Diese automatische Handhabung von Finanzdimensionen gewährleistet die Nachverfolgung von Kosten beim Durchführen von Projekt-Controlling und -Reporting für funktionale Standorte.

Die Art, wie Sie die Hierarchie der funktionalen Standorte erstellen, hängt von den Unternehmensanforderungen für die Verwaltung der internen Ausrüstung oder die Wartung der Ausrüstung von Kunden ab. Die folgende Abbildung zeigt ein Beispiel für funktionale Standorte, die auf geografischen Standorten basieren.

![Abbildung 3](media/03-overview-image.png)

Die folgende Abbildung zeigt ein Beispiel für funktionale Standorte, die auf Kunden basieren.

![Abbildung 4](media/04-overview-image.png)
