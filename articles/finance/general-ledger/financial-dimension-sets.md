---
title: Finanzdimensionssätze
description: In diesem Thema werden Finanzdimensionssätze beschrieben und einige Tipps zur Optimierung ihrer Verwendung bereitgestellt.
author: yukonpeegs
ms.date: 03/23/2021
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionFocus, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 25871
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2021-03-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: ba11be028ebeea140df93e2a07dbb463402e3ef0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021827"
---
# <a name="financial-dimension-sets"></a>Finanzdimensionssätze

[!include [banner](../includes/banner.md)]

In diesem Thema werden Finanzdimensionssätze beschrieben und einige Tipps zur Optimierung ihrer Verwendung bereitgestellt.

Ein Dimensionssatz ist eine sortierte Liste von Finanzdimensionen, mit denen Hauptbuchdaten auf benutzerdefinierte Weise zusammengefasst werden können. Eine primäre Verwendung von Dimensionssätzen besteht darin, eine Zwischenbilanz zu definieren.

Der einzige Standarddimensionssatz ist der Dimensionssatz, der nur das Hauptkonto enthält.

Sie verwenden die Seite **Finanzdimensionssätze** zum Erstellen und Verwalten von Finanzdimensionssätzen.

## <a name="dimension-set-balances"></a>Dimensionssatzsalden

Ein Dimensionssatz kann Salden haben, die auf seinen Finanzdimensionen basieren. Die Salden befinden sich im Hauptbuch und basieren auf der Definition des Dimensionssatzes. Die Salden werden aus den Hauptbuchdaten zusammengefasst, um die Leistung beim Abrufen zu verbessern (z. B. wenn eine Zwischenbilanz erstellt wird).

## <a name="create-balances"></a>Salden erstellen

Verwenden Sie die Schaltfläche **Salden erstellen**, um die Salden für einen Dimensionssatz zu initialisieren, für den derzeit keine Salden vorhanden sind.

> [!NOTE]
> Es wird empfohlen, die Anzahl der Dimensionssätze mit Salden zu begrenzen, da Saldenaktualisierungen alle Buchungsaktivitäten des Hauptbuchs betreffen.

## <a name="update-balances"></a>Salden aktualisieren

Verwenden Sie die Schaltfläche **Salden aktualisieren**, um die letzte Buchungsaktivität des Hauptbuchs in die Salden aufzunehmen. Saldenaktualisierungen sind leichte Vorgänge. Sie dürfen nur die Buchungsaktivität des Hauptbuchs verarbeiten, die seit der letzten Aktualisierung aufgetreten ist.

> [!NOTE]
> Die Anzeige der Zwischenbilanz erzwingt eine Aktualisierung, um sicherzustellen, dass die angezeigten Salden aktuell sind. Verwenden Sie einen wiederkehrenden Stapelverarbeitungsauftrag, damit die Aktualisierungen Ihrer am häufigsten verwendeten Dimensionssätze schnell erfolgen. Auf diese Weise können Sie die Wartezeit für Zwischenbilanzbenutzer minimieren.

## <a name="rebuild-balances"></a>Salden neu erstellen

Verwenden Sie die Schaltfläche **Salden neu erstellen**, um die Salden von Grund auf neu zu erstellen. Auf diese Weise stellen Sie sicher, dass sie mit den Daten im Hauptbuch übereinstimmen. Die Wiedererstellung der Salden ist sehr aufwändig und sollte normalerweise nicht erforderlich sein.

> [!NOTE]
> Wenn Sie ein Szenario haben, in dem regelmäßig Salden neu erstellt werden müssen, empfehlen wir Ihnen, sich an den Kundensupport zu wenden. Mithilfe des Kundensupports können Sie feststellen, warum Salden nicht mit den Daten im Hauptbuch übereinstimmen.

## <a name="clear-balances"></a>Salden leeren

Verwenden Sie die Schaltfläche **Salden leeren**, um die Salden zu entfernen und weitere Aktualisierungen zu stoppen. Der Dimensionssatz hat keine Auswirkungen mehr auf die Buchungsaktivitäten des Hauptbuchs.

Weitere Informationen finden Sie unter [Finanzdimensionen](financial-dimensions.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
