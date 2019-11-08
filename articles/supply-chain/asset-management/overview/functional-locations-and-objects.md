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
ms.openlocfilehash: e3a42d36fd137aa780886276a4235f1b8f3a3680
ms.sourcegitcommit: 0099fb24f5f40ff442020b488ef4171836c35c48
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/23/2019
ms.locfileid: "2653346"
---
# <a name="functional-locations-and-assets"></a>Funktionale Standorte und Anlagen

[!include [banner](../../includes/banner.md)]

 

In diesem Thema werden funktionale Standorte und Anlagen in Asset Management beschrieben. Asset Management ist ein erweitertes Modul für die Verwaltung von Anlagen und Wartungsaufgaben in Dynamics 365 Supply Chain Management.

## <a name="overview"></a>Übersicht

Anlagenmanagement ist nahtlos in mehrere Module in anderen Finance and Operations-Apps integriert. Die folgende Abbildung zeigt die Schnittstellen mit anderen Modulen.

![Diagramm, das die Anlagenmanagement-Schnittstellen mit anderen Modulen zeigt](media/01-overview-image.png)

Mit Asset Management können Sie effizient alle Aufgaben verwalten und ausführen, die mit dem Verwalten und der Wartung von viele Arten von Ausrüstung in Ihrem Unternehmen zusammenhängen. Zu diesen Ausrüstungsgegenständen zählen Maschinen, Produktionsanlagen und Fahrzeuge. Asset Management unterstützt außerdem Lösungen über zahlreiche Branchen hinweg.

Die folgende Abbildung zeigt einen Überblick über die Hauptfunktionen von Asset Management.

![Diagramm, das die Hauptfunktionen in Anlagenmanagement anzeigt](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a>Funktionale Standorte und Anlagen

Funktionale Standorte werden verwendet, um Anlagen an Standorten zu verwalten. Zu dieser Verwaltung gehört das Nachverfolgen von Anlagenkosten an funktionalen Standorten. Funktionale Standorte werden hierarchisch strukturiert, und Standorte können untergeordnete Standorte haben. Die Struktur funktionaler Standorte ist statisch. Dies bedeutet, das Standorte den Ort nicht ändern können. Anlagen können an funktionalen Standorten installiert sein und können bei Bedarf später an anderen funktionalen Standorten installiert werden.

Anlagenkosten folgen immer dem Standort der Anlage. Dies bedeutet Folgendes: Wenn Sie eine Anlage an einem neuen funktionalen Standort einrichten, verwendet die Anlage automatisch die Finanzdimensionen, die sich auf den neuen funktionalen Standort beziehen. Daher beziehen sich Anlagenkosten immer auf den funktionalen Standort, an dem die Anlage derzeit installiert ist. Diese automatische Handhabung von Finanzdimensionen gewährleistet die Nachverfolgung von Kosten beim Durchführen von Projekt-Controlling und -Reporting für funktionale Standorte.

Die Art, wie Sie die Hierarchie der funktionalen Standorte erstellen, hängt von den Unternehmensanforderungen für die Verwaltung der internen Ausrüstung oder die Wartung der Ausrüstung von Kunden ab. Die folgende Abbildung zeigt ein Beispiel für funktionale Standorte, die auf geografischen Standorten basieren.

![Diagramm, das die funktionalen Standorte auf Grundlage der geografischen Standorte anzeigt](media/03-overview-image.png)

Die folgende Abbildung zeigt ein Beispiel für funktionale Standorte, die auf Kunden basieren.

![Diagramm, das die funktionalen Standorte auf Grundlage der Kunden anzeigt](media/04-overview-image.png)
