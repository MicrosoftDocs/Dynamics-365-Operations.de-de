---
title: Lagerortkonfiguration
description: In diesem Artikel wird beschrieben, wie ein Lagerort konfiguriert wird. Es enthält Informationen zum Aktivieren eines Lagerortlayouts und Lagerortverfahren.
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, WHSLocation, WHSLocationBuild, WHSLocationProfile, WHSLocationType, WHSLocDirTable, WHSParameters, WHSWaveTemplateTable, WHSWorkPool, WHSWorkTemplateTable, WHSZone, WHSZoneGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 11554
ms.assetid: 262b7b88-2cce-44f7-9a5b-77c12af1be20
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e50d03718234748d9ad5092500b970216c40284
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "318441"
---
# <a name="warehouse-configuration"></a>Lagerortkonfiguration

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie ein Lagerort konfiguriert wird. Es enthält Informationen zum Aktivieren eines Lagerortlayouts und Lagerortverfahren.

**Hinweis:** Dieser Artikel gilt für Funktionen im Modul **Lagerortverwaltung** (erweiterte Lagerung). Es gilt nicht für Lagerort-Funktionen im Modul **Bestandsverwaltung**.

## <a name="warehouse-layout"></a>Lagerortlayout
Das Lagerortverwaltungssystem in Microsoft Dynamics 365 for Finance and Operations ermöglicht flexible Methoden, Ihr Lagerortlayout zu definieren, um notwendige Anpassungen und somit eine optimale Lagerorteffizienz zu ermöglichen.

-   Sie können Lagerbereiche mit hoher und niedriger Priorität für eine optimale Platzierung von Waren einrichten.
-   Sie können Ihre Lagerorte in die Zonen aufteilen, um verschiedene Lageranforderungen, wie Temperaturanforderungen oder unterschiedliche Umschlagsgeschwindigkeiten, für Artikel zu berücksichtigen.
-   Sie können Lagerort-Lagerplätze auf jeder Ebene angeben, (beispielsweise Standort, Lagerort, Gang, Regal, Regalboden und Lagerfachposition).
-   Sie können Lagerplätze gruppieren, indem Sie die Einstellungen für physische Kapazitätsengspässe verwenden.
-   Sie können basierend auf Regeln, die über Abfragen definiert werden, steuern, wie Artikel gelagert und entnommen werden.

Um die Lagerortverwaltung in Finance and Operations zu verwenden, müssen Sie einen Lagerort erstellen und diesen für die erweiterten oder spezialisierten Lagerortverwaltungsaktivitäten aktivieren. Wählen Sie auf der Seite **Lagerorte** die Option **Lagerortverwaltungsprozesse verwenden** aus.

### <a name="zone-groups-zones-location-types-and-locations"></a>Zonengruppen, Zonen, Lagerplatztypen und Lagerplätze

Im Rahmen des Prozesses zur Aktivierung eines Lagerortlayouts, müssen Sie Lagerortzonengruppen und Zonen, Lagerplatzprofile, Lagerplatztypen und Lagerplätze definieren.

-   **Zonengruppen** - Eine logische oder physische Gruppierung von Zonen innerhalb eines Lagerorts.
-   **Zonen** - Eine logische oder physische Gruppierung von Lagerplätzen innerhalb eines Lagerorts.
-   **Lagerplatzprofile** - Eine logische oder physische Gruppierung von Standorten, die die gleichen Lagerortlagerplatzprozess-Richtlinien haben.(Dort kann beispielsweise eine Mischung unterschiedlicher Artikelnummern gelagert werden, auf die die gleichen physischen Kapazitätsengpässe zutreffen).
-   **Lagerplatztypen** - Eine logische oder physische Gruppierung von Lagerort-Lagerplätzen. So können Sie beispielsweise einen Lagerplatztyp für alle Bereitstellungslagerplätze erstellen. Erforderliche Einstellungen auf der Seite **Lagerverwaltungsparameter** steuern den Prozess des Definierens von Staginglagerplatztypen und endgültigen Einlieferungslagerplätzen.
-   **Lagerplätze** - Die niedrigste Ebene der Lagerplatzinformationen. Lagerplätze werden verwendet, um zu nachzuverfolgen, wohin der verfügbare Lagerbestand in einem Lagerort gespeichert und entnommen wird.

Die Entitäten, die Sie erstellen, um Ihr Lagerortlayout zu definieren, werden in Abfragen verwendet, die Sie in den Arbeitsvorlagen einrichten, um Arbeitsaufträge am Lagerort zu steuern. Wenn Sie die Zonen, Lagerplatztypen usw. definieren, bedenken Sie, dass verschiedene Bereiche am Lagerort für verschiedene Prozesse verwendet werden. Berücksichtigen Sie ausserdem Faktoren wie physische Merkmale eines bestimmten Bereichs. Beispielsweise könnte es Bereiche geben, in denen Sie nur einen bestimmten Gabelstapler verwenden können. Oder in Ihrem Unternehmen sind Produktion und Fertigerzeugnisse in einer Einrichtung, und Sie möchten in Finance and Operations einen einzelnen Lagerort erstellen und dann die beiden Arbeitsgänge trennen, indem Sie zwei Zonengruppen einrichten. Geben Sie den Entitäten beschreibende Namen, damit sie einfach zu identifizieren sind, wenn Sie sie in Vorlagenabfragen verwenden.

### <a name="location-stocking-limits-location-profiles-and-fixed-picking-locations"></a>Lagerplatzbeschränkungen, Lagerplatzprofile und feste Entnahmeorte

Sie müssen das physische Layout des Lagerorts bedenken, um sowohl Speicherkapazitäten zu ermitteln (Lagerplatzbeschränkungen und Lagerplatzprofile) als auch als Teil der zu erreichenden Optimierung der Lagerortprozesse. 

Lagerplatzbeschränkungen sorgen dafür, dass nicht angefordert wird, einen Bestand an einen anderen Lagerplatz zu verschieben, dessen Kapazität für diesen Bestand nicht ausreicht. Wenn beispielsweise einige Lagerplätze in einem Lagerort nur eine Palette pro Lagerplatz aufnehmen können, können Lagerplatzbeschränkungen aktiviert werden. Der Wert **Menge** kann auf **1** eingestellt werden, und der Wert **Einheit** kann innerhalb einer bestimmten Lagerplatzprofilgruppierung auf **PL** festgelegt werden. 

Wenn erweiterte Berechnungen erforderlich sind, um die Engpässe in der Lagerplatzkapazität zu steuern, können die Lagerplatzprofileinstellungen verwendet werden. In diesem Fall werden sowohl das Gewicht als auch das Volumen berücksichtigt, wenn Kapazitätsberechnungen geleistet werden. 

Um optimale ausgehende Prozesse zu erreichen, sollten Sie auswerten, ob feste Entnahmeorte und/oder Verpackungslagerplätze verwendet werden. Häufig wird die minimale/maximale Auffüllung für Auffüllungsprozesse von einem Sammelbereich in feste Entnahmeorte verwendet, und mehrfach feste Entnahmeorte können innerhalb des gleichen Lagerort und für Produktvarianten aktiviert werden. Berücksichtigen Sie die Flexibilität, die Sie erzielen können, indem Sie dedizierte Überlaufslagerplätze zur Bedarfsauffüllung aktivieren, die nur für den Prozess der Wellen-/Ladungswiederbeschaffung verwendet werden.

### <a name="location-setup-wizard"></a>Lagerplatz-Setup-Assistent

Um die Lagerplätze innerhalb eines Lagerorts schnell zu erstellen, können Sie den Assistenten **Lagerplatzeinstellung** verwenden. Im Rahmen dieses Prozesses können Sie das Format der Lagerplatznamen problemlos verwalten.

## <a name="warehouse-processes"></a>Lagerortprozesse
Als Teil der Konfiguration des Lagerorts, ist es wichtig, dass Sie Lagerortprozesse gemäß der Geschäftsanforderungen aktivieren. Die wichtigsten Komponenten, die Sie konfigurieren müssen, sind Wellenvorlagen, Arbeitsvorlagen, Arbeitspools und Lagerplatzrichtlinien.

### <a name="wave-templates"></a>Serienvorlagen

Wellenvorlagen unterstützen dabei, den ausgehenden Prozess "Für Lagerort freigeben" zu aktiviere n. Sobald Auftragspositionen freigegeben werden (entweder direkt aus Quelldokumenten, über Stapelverarbeitungsauftragsprozesse oder über Ladungen, die bereits erstellt wurden), wird die Wellenvorlagenfunktion verwendet. 

Folgenden drei Vorlagenarten können erstellt werden: 
-   **Versand**
-   **Produktionsauftrag**
-   **Kanban** 

Parameter werden verwendet, um festzulegen, wie weit das System automatisch in die ausgehende Arbeitsverarbeitung wechseln soll. Eine Wellenvorlage wird anhand der Wellenvorlagensequenz und der Kriterien ausgewählt, die in der Vorlage angegeben werden. Wenn eine Vorlage oben in der Sequenz aufgeführt ist, werden die Kriterien in dieser Vorlage zuerst geprüft. Wenn die Kriterien erfüllt werden, wird die Wellenvorlage verarbeitet. Andernfalls werden die Kriterien in der nächsten Vorlage, usw. geprüft. Daher wird empfohlen, die Vorlage mit den spezifischsten Kriterien an den Anfang der Wellenvorlagen-Sequenzliste zu setzen, damit diese zuerst verarbeitet wird. Sie möchten beispielsweise die gesamte Arbeit für einen bestimmten Spediteur heute verarbeiten und die Verarbeitung der Arbeit für andere Spediteure vorübergehend verschieben. In diesem Fall sollte die Wellenvorlage, die die Arbeiten für diesen Spediteur auswählt, in der Sequenz höher aufgelistet werden als die anderen Vorlagen. Andernfalls würden Arbeiten für andere Spediteure vor der Arbeit für diesen Spediteur verarbeitet werden. 

Sie müssen die Wellenprozessmethoden in jeder Wellenvorlage angeben. Die verfügbaren Methoden variieren je nach Wellenvorlagentyp.

### <a name="work-templates"></a>Arbeitsvorlagen

Definitionen für Arbeitsvorlagen spielen in der Definition von Lagerortverwaltungverfahren eine wichtige Rolle. Sie definieren, welche Arbeit ausgeführt wird und wie die Arbeit verrichtet wurde. Vorlagen können einen Richtliniencode beinhalten, der eine Verknüpfung zu Lagerplatzrichtlinie enthält, um zu bestimmen, wo Arbeit ausgeführt wird. Arbeitsvorlagen beinhalten eine Abfrage, die die Kriterien für die Arbeit angibt. Jede Vorlage muss mindestens einen Arbeitsgang "Entnahme" und einen Arbeitsgang "Einlagern" umfassen, um den grundlegenden Arbeitsgang des Übertragens eines verfügbaren Lagerbestands von einem Lagerplatz zu anderen zu steuern. 

Wenn mehrere Arbeitskräfte in der Lage sein müssen, Arbeit für einige Ihrer Lagerort-Arbeitsgänge zu verarbeiten, können Sie das Konzept der *Bereitstellung* verwenden, um Bestand und Arbeitsausführung in verschiedene Arbeitsklassen zu unterteilen.

### <a name="work-pools"></a>Arbeitspools

Arbeitspools werden verwendet, um Arbeit in Gruppen aufzuteilen. So können Sie beispielsweise einen Arbeitspool erstellen, um Arbeit zu klassifizieren, die in einem bestimmten Lagerplatzes auftritt. Für alle Arbeitstypen außer Inventur können Sie einen Arbeitspool zu einer Arbeitsvorlage zuweisen. Auf den folgenden Seiten können sie einen Arbeitspool für Zykluszählung zuweisen:

-   Permanente Inventurpläne
-   Permanente Inventur-Schwellenwerte
-   Permanente Inventurarbeit nach Lagerplatz
-   Permanente Inventurarbeit nach Artikel

Wenn Sie Arbeitsvorlagen verwenden, um Arbeit zu erstellen, wird der Arbeitspool automatisch der Arbeit zugewiesen. 

Arbeitspool-IDs können auch verwendet werden, um die Art der Arbeit einzuschränken, die an einen bestimmten Lagerarbeiter geleitet wird, vorausgesetzt, dass diese Funktionen im entsprechenden Menüelement des mobilen Geräts konfiguriert wurden.

### <a name="location-directives"></a>Lagerplatzrichtlinien

Lagerplatzrichtlinien werden verwendet, um die Arbeitstransaktionen an die entsprechenden Lagerplätze im Lagerort zu senden. Das bedeutet, sie definieren, wo entnommen und bereitgestellt wird. 

Um das Definieren der Aktivitäten, die den einzelnen Richtlinienpositionen für Lagerplätze zugeordnet sind, zu erleichtern verwenden Sie eine der vordefinierten Strategien. Sie können beispielsweise die Strategie **Leerer Lagerplatz ohne eingehende Arbeit** verwenden, um freie Lagerplätze an einem Lagerort zu suchen, oder Sie können die Strategie **FEFO-Chargenreservierung** für ausgehende Verkaufskommissionierung verwenden.

<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Konfigurieren von Lagerplätzen in einem WMS-aktivierten Lagerort (Aufgabenleitfaden)](tasks/configure-locations-wms-enabled-warehouse.md)



