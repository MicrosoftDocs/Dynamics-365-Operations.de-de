---
title: 'Mischplanung: Kombinieren Sie eigenständige, Prozess- und Lean-Beschaffung'
description: Dieser Artikel enthält Informationen zum gemischten Planungsmodus.
author: johanhoffmann
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 52931
ms.assetid: 2e8b5fd1-cee9-45da-a3ae-6961fb020b89
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 335bdc9690b3111f4a04adc7e82d62de36ff4caf
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065987"
---
# <a name="mixed-mode-planning---combine-discrete-process-and-lean-sourcing"></a>Mischplanung: Kombinieren Sie eigenständige, Prozess- und Lean-Beschaffung

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen zum gemischten Planungsmodus. In im gemischten Planungsmodus können Sie Ihre Lieferkette basierend auf dem Materialfluss modellieren. Dynamics 365 Supply Chain Management stellt sicher, dass der Materialfluss Ihren Modellen folgt, unabhängig von der Zubehörrichtlinie, die ausgewählt wird (Kanbans, Produktionsaufträge, Bestellungen, Chargenaufträge oder Umlagerungsaufträge). 

Sie können die allgemeine Strategie für das Beschaffen eines Produkts unabhängig von der Produktstruktur auswählen.  

So können Sie Kanbansteuerelemente in der Assembly haben, in der Materialien für den Montagebereich nach Produktionsaufträgen, Kanbans, Übertragungen, Stapelverarbeitungsaufträgen beschafft werden, oder eine beliebige Kombination, die für die Merkmale der Lieferkette geeignet ist, Sie jedoch die volle Übersicht über die Bereitstellung haben. Diese Funktion führt zu optimierten Lieferkettenprozessen und erweiterter Sichtbarkeit in der Lieferkette.  

Die Granularität der Lieferrichtlinien die im Produktprogrammplanungslauf verwendet werden, hängt von den Lagerdimensionen ab, die als Deckungsdimensionen aktiviert werden. Um den Produktprogrammplanungslauf zu aktivieren, um die Auffüllung und Bereitstellung von unterschiedlichen Arten der Lagerplätze zu steuern (beispielsweise durch das Trennen der Produktion für verschiedene Produktionseinheiten, oder durch Trennen unterschiedlicher Arten von Material- und Endproduktlagerorten), sollten Sie Standort und Lagerort als Deckungsdimensionen aktivieren. Alternativ kann der Lagerort als Deckungsdimension ausgelassen werden. In diesem Fall, wenn Sie Lagerverwaltungsprozesse (LVS) verwenden, werden alle Lagerplatzumlagerungen innerhalb eines Lagers durch Lagerortarbeit gesteuert, während alle lagerübergreifenden Bewegungen durch Entnahmekanbans gesteuert werden können.

## <a name="supply-policies"></a>Lieferrichtlinien
Die Mischplanung steuert, wie ein Produkt geliefert wird und, basierend auf der Beschaffung, wie abgeleitete Anforderungen (Verbrauch von Artikeln aus einer \[Stückliste\]) ausgestellt werden. Basierend auf dem Auftragstyp beschafft das System Materialien automatisch nach den Anforderungen.  

Lieferrichtlinien können auf der Produktebene oder einer beliebigen Granularität definiert werden, die Ihre Anforderungen unterstützt. Sie definieren die Granularität von Lieferrichtlinien auf der **Standardauftragseinstellungen**-Seite.  

Lieferrichtlinien können gesteuert werden nach Produkt, Artikeldimensionen (Konfiguration, Farbe und Größe), Standort und Lagerort. Diese Einstellung wird auf der Seite **Artikeldeckung** ausgeführt.  

Der standardmäßige Auftragstyp steuert das, was der Auftragsproduktprogrammplan generiert.  

Unabhängig davon, wie die Lieferkette modelliert wird, unterstützt Supply Chain Management Ihre Mischung von Lieferrichtlinien. Sie können Produktionsaufträge haben, die von Kanbans beschafft werden. Alternativ können Sie einen Chargenauftrag haben, der ein Produkt benötigt, das nach Übertragungen oder nach Kanbans beschafft wird.  

Mit Supply Chain Management wird sichergestellt, dass der Materialfluss dem Modell folgt.  

Der Lagerort für die Entnahme des Materials wird dynamisch zur Laufzeit zugewiesen, nachdem die Lieferrichtlinie definiert wurde.  

In der Regel werden Kanbans nicht für zukünftige Zeiträume erstellt, da ein Kanban eine Kurzlebigkeit hat. Um vollständig Sichtbarkeit in der Lieferkette zu verwalten, haben wir das neue Planungskonzept eines "geplanten Kanbans" eingeführt, das verwendet wird, um abgeleitete Anforderungen zu berechnen, und hilft sicherzustellen, dass die Anforderungen auf der gleichen Logik basierend beschafft werden, die verwendet wird, wenn das tatsächliche Kanban erstellt wird.  

Die gleiche Logik ist daher für alle anderen Lieferrichtlinientypen vorhanden. Daher basiert die langfristige Materialplanung auf der gleichen Logik, von der Sie erwarten, dass sie mit dem tatsächlichen Aufträgen ausgeführt werden, nachdem die Produktion und Lieferung genehmigt wird.

## <a name="materials-allocation-cross-supply-policy--resource-consumption-on-boms"></a>Lieferübergreifende Materialzuteilungsrichtlinie – Ressourcenverbrauch von Stücklisten
Ressourcenverbrauch ist wichtige Funktion. Ressourcenverbrauch ermöglicht, dass ein Lagerort für die Entnahme von Materialien dynamisch ausgewählt werden kann, basierend auf der Lieferrichtlinie (Auftragstyp), und erleichtert auch die Verwaltung von den Stammdaten.  

Ressourcenverbrauch erfordert, dass der Lagerort, von dem Material entnommen wird, auf Grundlage der Methode, wie das Produkt beschafft wird, zugewiesen wird. Das bedeutet, zur Laufzeit sucht das System die Ressourcen, die für das Herstellen verwendet werden sollen. Auf Grundlage dieser Ressourcen sucht das System dann den Entnahmelagerort.  

Für Arbeit, die unabhängig von einer Lieferrichtlinie ist, müssen Sie nicht Informationen zur Stückliste ändern, wenn die Lieferung geändert wird. Bei Ad-hoc-Änderungen stellt Supply Chain Management sicher, dass Materialien vom richtigen Lagerort beschafft werden.

## <a name="process-manufacturing--the-production-type"></a>Prozessfertigung – Der Produktionstyp
Für vollständige Flexibilität im gemischten Modus, empfiehlt es sich, Produktionstyp Stücklisten für alle Produkte verwenden. Sie können Kanbans, Produktionsaufträge, Umlagerungsaufträge oder Bestellungen Anschließend können, ein Produkt zu liefern. Für Fertigungsverarbeitung muss der Produktionstyp **Formel**, **Kuppelprodukt**, **Nebenprodukt** oder **Planungsartikel** verwendet werden. Kanbans und Produktionsaufträge können nicht für diese Produktionstypen verwendet werden.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]