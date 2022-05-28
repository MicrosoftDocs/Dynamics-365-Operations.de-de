---
title: Ladungserstellungsworkbench
description: In diesem Thema wird beschrieben, wie Sie mit der Ladungserstellungsworkbench arbeiten.
author: Weijiesa
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSLoadBuildWorkbench,TMSLoadBuildTemplateCreate,TMSLoadBuildStrategy,TMSLoadBuildTemplateApply
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: c6723656baaca42c6b055d759c84fd4392fe04b0
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674672"
---
# <a name="load-building-workbench"></a>Ladungserstellungsworkbench

[!include [banner](../../includes/banner.md)]

Mit der Ladungserstellungsworkbench können Sie Ladungserstellungstrategien anwenden, wenn Sie Ladungen erstellen.

## <a name="create-a-load-building-strategy"></a>Erzeugen einer Ladungserstellungstrategie

Sie verwenden Ladungserstellungstrategien, um Ladungen automatisch zu erstellen. Diese Funktionalität kann in den folgenden Situationen von Vorteil sein:

- Wenn Sie regelmäßig eine bestimmte Anzahl von Produkten versenden, helfen Ladungserstellungstrategien, Zeit zu sparen, weil Sie nicht jedes Mal die gleiche Ladung aufbauen müssen.
- Wenn Sie halbvolle Ladungen vermeiden wollen, um die Effizienz zu maximieren, können Ladestrategien helfen, jede Ladung so weit wie möglich zu füllen.

Eine Ladungserstellungstrategieklasse mit dem Namen `TMSLoadBuildingVolumeStrategy` bietet eine Ladungserstellungstrategie mit dem Namen *Volumenbasierte Ladungserstellungstrategie*. Mit dieser Strategie können Sie die Höchstwerte verwenden, die für Höhe und Gewicht in der Ladungsvorlage angegeben sind, oder die Einstellungen überschreiben, indem sie neuen Werte eingeben. Diese Strategie ist die einzige Strategie, die von Haus aus enthalten ist. (Möglicherweise haben Sie jedoch einige benutzerdefinierte Strategien.)

Um die Out-of-Box-Strategie *Volumenbasierte Ladungserstellung-Strategie* zu verwenden, wählen Sie sie im Feld **Ladungserstellung-Strategie** auf der Seite **Ladungserstellungsworkbench** (**Transportverwaltung &gt; Planung &gt; Ladungserstellungsworkbench**).

Gehen Sie folgendermaßen vor, um eine Strategie für die Ladungsaufnahme zu erstellen.

1. Gehen Sie zu **Transportverwaltung &gt; Einrichten &gt; Ladungserstellung &gt; Ladungserstellung-Strategien**.
1. Wählen Sie im Aktivitätsbereich **Klassenliste generieren**, um sicherzustellen, dass Sie die neuesten Versionen aller verfügbaren Klassen haben.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Geben Sie einen eindeutigen Namen für die Strategie ein, wählen Sie die Ladungserstellungstrategieklasse dafür aus und geben Sie eine Beschreibung ein.
1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Wählen Sie im Aktivitätsbereich **Parameter** aus.
1. Wählen Sie auf der Seite **Ladungserstellungstrategie-Parameter** in der Liste **Volumenkapazität** und geben Sie dann in das Feld **Wert** den Prozentsatz der gesamten Volumenkapazität der Ladung ein, der für die neue Ladungserstellungstrategie angewendet werden soll.
1. Wählen Sie **Gewichtskapazität** in der Liste und geben Sie dann in das Feld **Wert** den Prozentsatz der Gesamtgewichtskapazität der Ladung ein, der für die neue Ladungserstellungstrategie angewendet werden soll.
1. Schließen Sie die Seite **Ladungserstellungstrategie-Parameter**.
1. Schließen Sie die Seite **Ladungserstellungstrategien**.

Sie können die Ladungserstellungsstrategie nun einer Ladungserstellungsvorlage zuweisen. Alternativ können Sie sie auch direkt in der Ladungserstellungsworkbench verwenden.

## <a name="use-a-load-building-strategy-in-the-load-building-workbench"></a>Verwenden einer Ladungserstellungstrategie in der Ladungserstellungsworkbench

1. Gehen Sie zu **Transportverwaltung &gt; Planung &gt; Ladungserstellungsworkbench**.
1. Führen Sie einen dieser Schritte aus:

    - Wählen Sie eine Strategie im Feld **Ladungserstellungsstrategie**.
    - Wenn Sie eine Ladungserstellungvorlage definiert und ihr die Ladungserstellungstrategie zugewiesen haben, wählen Sie im Aktivitätsbereich auf der Registerkarte **Vorlagen verwalten** die Option **Vorlage anwenden**. Wählen Sie dann in der Dropdown-Dialogbox **Ladungserstellungsvorlage anwenden** eine Vorlage im Feld **Ladungserstellungsvorlagenname**.

1. Wählen Sie auf dem Inforegister **Vorlagen Sequenz laden** eine oder mehrere [Ladevorlagen](load-template.md). Die Workbench wird versuchen, die Ladung in diese Arten von Containern einzupassen, und zwar in der hier angegebenen Sequenz. Normalerweise sollten Sie die kleinsten Container an den Anfang der Liste einlagern, um sicherzustellen, dass der kleinstmögliche Container zuerst ausgewählt wird.
1. Wählen Sie im Aktivitätsbereich **Ladungen vorschlagen**.
1. Überprüfen Sie die vorgeschlagenen Ladungen und die vorgeschlagenen Zeilen.
1. Wählen Sie im Aktivitätsbereich **Ladungen erstellen**, um Ladungen zu erstellen, die auf den Zeilen des Quelldokuments im Inforegister **Vorgeschlagene Ladungszeilen** basieren.
1. Schließen Sie die Seite **Ladungserstellungsworkbench**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]