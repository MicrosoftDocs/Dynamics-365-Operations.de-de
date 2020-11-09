---
title: Teilweise Lagerplatz-Zykluszählung
description: Zykluszählungspläne leiten die tatsächlichen Zähloperationen. Sie können festlegen, dass nur bestimmte Produkte und Produktvarianten anstelle aller verfügbaren Lagerbestände eines Lagerplatzes gezählt werden.
author: perlynne
manager: tfehr
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable, WHSRFMenuItemCycleCount, WHSCycleCountPlanListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5d69b1e9444785058a2b3e62b9a76cb6e70abf03
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017597"
---
# <a name="partial-location-cycle-counting"></a>Teilweise Lagerplatz-Zykluszählung

[!include [banner](../includes/banner.md)]

Zykluszählungspläne leiten die tatsächlichen Zähloperationen. Sie können festlegen, dass nur bestimmte Produkte und Produktvarianten anstelle aller verfügbaren Lagerbestände eines Lagerplatzes gezählt werden.

Wenn Sie Zykluszählpläne nutzen, um Inventurarbeit zu generieren, können Sie die tatsächlichen Zähloperationen lenken. Sie können festlegen, dass nur bestimmte Produkte und Produktvarianten anstelle aller verfügbaren Lagerbestände eines Lagerplatzes gezählt werden. Indem Sie nach bestimmten Produkten filtern, kann der Lagerortleiter Prüfungsgemeinkosten senken, Konsolidierungsfehler vermeiden und Zeit sparen.

## <a name="how-to-configure-partial-location-cycle-counting"></a>So konfigurieren Sie eine teilweise Lagerplatz-Zykluszählung
Wenn Sie den Lagerortarbeitsprozess für Zähloperationen verwenden, wird eine Arbeitskopfzeile für jeden Lagerplatz erstellt. Wenn Sie den Zykluszählplan definieren, können Sie die Abfrage **Lagerplätze auswählen** verwenden, um die Zykluszählarbeit zu reduzieren, die generiert wird. Wenn Sie Produkte für den Zykluszählplan auswählen, können Sie Produkt- und Produktvariantenabfragen verwenden, um das Zählen zu verfeinern. 

Sie können eine **Arbeitsvorlage** einem Zykluszählplan zuordnen, um zu definieren, wie die Zykluszählarbeit erstellt werden soll. Auf die Arbeitsvorlage für Zählvorgänge wird direkt vom Zykluszählplan verwiesen. 

Wenn Sie die Arbeitsvorlagendetails definieren, können Sie die Option **Arbeitspositionsumbrüche** verwenden, um anzugeben, ob die Inventurarbeitspositionen nach Positionsnummer oder Produktvariantennummer gruppiert werden müssen. Diese Einstellung ist erforderlich, wenn Sie verfügbare Lagerbestände nur für bestimmte Produkte an einem Lagerplatz zählen möchten. Die Zykluszählungsarbeitspositionen, die erstellt werden, bekommen die Informationsebene, die Sie hier definieren. Der geführte Zählvorgang wird auf Basis dieser Ebene durchgeführt. 

Wenn Sie Zykluszählpläne mit Arbeitsvorlagen verknüpfen, indem Sie die Option **Arbeitspositionsumbrüche** verwenden, ist das Feld **Teilweise Zykluszählung** für die Zykluszählungsarbeit ausgewählt, die erstellt wird, und mehrere Zykluszählungsarbeitspositionen werden auf Basis der Definition der Arbeitsvorlage erstellt. 

Bevor teilweise Zykluszählungsarbeit verarbeitet werden kann, müssen Sie zumindest **Artikelnummer anzeigen** für das Menüelement des mobilen Geräts als Teil des Zykluszählungssetups auswählen. Der Lagerortoperator wird aufgefordert, nur Zähldaten zu erfassen, die zu den Zählpositionen (Positionsnummern und Produktdimensionen) gehören. Der gesamte andere verfügbare Bestand wird für diesen Zählungsprozess ignoriert. 

Für den Teilzykluszählprozess werden das Datum und die Uhrzeit der **Zählung beim letzten Zyklus** für den Standort nicht aktualisiert, obwohl alle an einem bestimmten Standort vorhandenen Artikel gezählt werden. Die Teilzykluszählung berücksichtigt den Parameter **Tage zwischen der Zykluszählung** auf der **Zykluszählpläne** -Seite nicht. Die Teilzykluszählung unterstützt nicht die gleichzeitige Zählung mehrerer Elemente am selben Lagerort. Die Teilzykluszählfunktion kann dazu führen, dass derselbe Lagerort für einen Artikel mehrmals gezählt wird, wenn der **Prozesszykluszählungsplan** ausgeführt wird. Um dieses Szenario zu vermeiden, geben Sie Filter im Feld **Lagerorte auswählen** an.

## <a name="example"></a>Beispiel
In vorliegenden Beispiel muss nur Artikelnummer A0001 in Lagerort 61 gezählt werden.

1.  Es wird eine neue Arbeitsvorlage für die Zykluszählung erstellt. Die Option **Arbeitspositionsumbrüche** wird verwendet, um fortlaufende Zählarbeitspositionen nach Artikelnummer zu gruppieren. Deshalb hat die Zykluszählungsarbeit, die erstellt wird, pro Artikelnummer Positionen. Sie können die Positionen auch nach Produktvariantennummer gruppieren.
2.  Ein neuer Zykluszählungsplan wird erstellt, der auf die neue erstellte Arbeitsvorlage verweist. Der Zykluszählungsplan enthält alle Lagerplätze in Lagerort 61 (Abfrage **Lagerplätze auswählen** ), die Bestand für Artikelnummer A0001 haben. Die Auswahl bestimmter Produkte wird im Abschnitt **Produktauswahlen des Zykluszählungsplans** definiert.
3.  Sie können Produkte für Zykluszählungspläne auswählen, indem Sie das Feld **Leere Lagerplätze** auf **Leere ausschließen** festlegen. Wenn der Zykluszählungsplan verarbeitet wird, wird teilweise Zykluszählungsarbeit für Artikelnummer A0001 erstellt. Der tatsächliche Zählprozess kann über das Menüelement des mobilen Geräts für geführte Zykluszählung durchgeführt werden.



<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Zykluszählung](cycle-counting.md)

