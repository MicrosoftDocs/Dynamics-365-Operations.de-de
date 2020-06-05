---
title: Beispielkreditorenschecks bei der elektronischen Berichterstellung
description: In diesem Thema werden allgemeine Informationen zur Verwendung der Beispielscheckformate bei der elektronischen Berichterstellung bereitgestellt.
author: ShylaThompson
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 4ce9c9d5b5def386f159df581c87d48f3e0b0ad9
ms.sourcegitcommit: 89022f39502b19c24c0997ae3a01a64b93280f42
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2020
ms.locfileid: "3367314"
---
# <a name="electronic-reporting-sample-vendor-checks"></a>Beispielkreditorenschecks bei der elektronischen Berichterstellung

[!include [banner](../includes/banner.md)]

Sie können elektronische Berichtserstellung (ER) zum Formatieren von Kreditorenschecks verwenden. Viele bankenspezifische und scheckanbieterspezifische Scheckformate sind auf dem Markt verfügbar. Beispielscheckformate sind im Zahlungsscheckmodell im ER-Tool-Repository enthalten. Diese Beispielschecks werden als **Scheck in der Mitte (USA)** und **Scheck oben Stub unten (USA)** bezeichnet.

## <a name="what-check-formats-are-currently-supported"></a>Welche Scheckformate werden derzeit unterstützt?

Sie sollten immer die Bibliothek der freigegebenen Anlagen in Microsoft Dynamics Lifecycle Services (LCS) nutzen und die aktuelle Liste der verfügbaren Dateien mit dem Anlagentyp **GER-Konfiguration** anzeigen. Im nächsten Abschnitt "Was muss ich einrichten?" ist ein Link zu einem Thema enthalten, das erläutert, wie ein LCS-Repository erstellt wird, damit Sie verfügbare Konfigurationen prüfen und ausgewählte Konfigurationen importieren können.

Microsoft Dynamics 365 Finance enthält außerdem ein Beispielformat (mit dem Scheck oben, gefolgt von zwei Rimesseabschnitten). Es enthält außerdem ein Beispielformat, mit dem Scheck in der Mitte zwischen zwei Rimesseabschnitten. Diese Beispielformate entsprechen den geschäftlichen Deluxe-Scheckformaten.

## <a name="what-do-i-have-to-set-up"></a>Was muss ich einrichten?

- Bevor Sie Schecks mit der elektronischen Berichtserstellung drucken, muss mindestens eine aktive Scheckkonfiguration in Ihre elektronische Berichterstellungskonfigurationen importiert werden. Weitere Informationen finden Sie unter [Elektronische Berichtskonfigurationen aus Lifecycle Services herunterladen](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).
- Wenn Sie Bargeld- und Bankverwaltungsschecks für das Bankkonto konfigurieren, aktivieren Sie das Kontrollkästchen **Allgemeines elektronisches Exportformat**, und wählen Sie das als entsprechende Scheckformat dann als eine Exportformatkonfiguration aus.
- Sie müssen zudem die Anzahl von Lieferscheinpositionen festlegen, die auf der Rimesse gedruckt werden. Stellen Sie sicher, dass die Überschriftenzeilen einbezogen werden, wenn Sie diese Zahl berechnen. Für die beiden Beispielscheckformate werden 17 Lieferscheinpositionen empfohlen. Allerdings ist kann diese Zahl abhängig vom Scheckvorrat und Ihren Druckertreibern variieren.
- Es wird empfohlen, einen Testscheck zu drucken, um das Schecklayout zu prüfen. Um einen Testscheck zu drucken, wählen Sie die Option **Test drucken** aus. Die Beispielscheckformate funktionieren am besten, wenn **Ränder** in den erweiterten Druckereigenschaften für Microsoft Excel auf **Keine** festgelegt wird. Nachdem der Testscheck generiert wurde, aktivieren Sie die Bearbeitung der Excel-Ausgabe und konfigurieren Sie das Seitenlayout, sodass sämtliche Ränder auf **0** (null) festgelegt sind. Vergleichen Sie die Testkopie der Schecks mit Ihrem Scheckvorrat und passen Sie die Einstellungen an, bis Sie mit der Ausrichtung zufrieden sind.
- Wenn Sie Zahlungen für das konfigurierte Bankkonto in der Zahlungserfassung generieren, werden die Schecks gedruckt, indem das angegebene Format verwendet wird.

Weitere Informationen finden Sie unter [Ein elektronisches Berichterstellungsformat ändern](../../dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md).
