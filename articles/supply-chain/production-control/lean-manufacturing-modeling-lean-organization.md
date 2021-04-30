---
title: Modellierung einer Lean-Organisation
description: Der Artikel enthält Informationen zu zentralen Konzepten für die Modellierung einer Lean-Organisation.
author: cvocph
ms.date: 09/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, KanbanFlowSelection, KanbanFlow
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53141
ms.assetid: 4f272f2f-ec2c-4b0d-a652-00a63b719b9e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 476dfd6be55ce484cb9bc101ac27dc6181f3c010
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910376"
---
# <a name="modeling-a-lean-organization"></a>Modellierung einer Lean-Organisation

[!include [banner](../includes/banner.md)]

Der Artikel enthält Informationen zu zentralen Konzepten für die Modellierung einer Lean-Organisation. 

Ein Lean Manufacturing-Szenario ist normalerweise mehr als eine Sammlung von nicht verknüpften Kanban-Regeln oder von Materialversorgungsrichtlinien. Der Material- und Produktfluss in Arbeitsgruppen und Lagerplätzen für ein bestimmtes Produktions- oder Beschaffungsszenario können als Folge oder als kleines Netzwerk von Prozess- oder Umlagerungsaktivitäten beschrieben werden. Diese Abfolge oder Netzwerk wird als Produktionsfluss bezeichnet.

## <a name="production-flows-in-lean-manufacturing"></a>Produktionsflüsse im Lean Manufacturing
In den Produktionsszenarien, die auf Produktionsaufträgen basieren, wird Material an einen bestimmten Produktionsauftrag ausgegeben. Während eine Folge von Arbeitsgängen, basierend auf einer Stückliste (BOM) und Arbeitsplänen, werden Produkte erstellt und schließlich am angegebenen Lagerplatz empfangen. Die Durchsatzzeit von Produktionsaufträgen variiert von Minuten zu Wochen. Alle zugehörigen Kosten, Materialien und Arbeiten werden im Produktionsauftrag kumuliert. 

Um Lieferzeiten und überschüssigen Bestand zwischen den Ressourcen zu reduzieren, die von der Chargenproduktion verursacht werden, führt Lean Manufacturing Kanbanauffüllung und Supermärkte in der Fertigung und Lagerort-Wiederbeschaffung ein. Diese Funktionen unterbrechen normalerweise die Produktion von teilweise unabhängigec Kanbanzyklen. Die Auffüllung eines Kanbans für ein Halbfertigprodukt wird nicht mehr durch einen Auftrag für ein Fertigprodukt ausgelöst. 

Um einen Produktions- und Kostenkontext für die verschiedenen Kanbanszenarien neu einzurichten, die vorgeschlagen werden, werden die aktivitätsbasierten Produktionsflüsse als Grundlage des Lean Manufacturing eingeführt. Alle Kanban-Regeln beziehen sich auf diese vordefinierte Struktur. Das aktivitätsbasierte Modell unterstützt die Einstellung umfassender Szenarien. Jedoch fügt dieses Modell keine Komplexität für die Fertigungsbereichsarbeitskräfte hinzu, da alle Szenarien die gleiche aktivitätsbasierte Benutzeroberfläche verwenden.

## <a name="semi-finished-products-non-bom-levels"></a>Halbfertigprodukte (Nicht-Stücklisten-Ebenen)
Lean Manufacturing integriert Kanbans für inventarisierte Produkte und Halbfertigprodukte in einem einzigen Framework und bietet eine einheitliche Benutzerfreundlichkeit für alle Anfragen. Aufgrund dieser Architektur, müssen zusätzliche Stücklistenebenen nicht mehr erfasst werden, um die für Halbfertigprodukte zu verwendende Kanbans zu aktivieren. Diese Architektur hilft zudem dabei, Lagerbuchungen auf ein Minimum zu beschränken.

## <a name="products-and-material-in-work-in-progress"></a>Produkte und Material in der "Ressource in Fertigung"
Die Verringerung von Chargengrößen auf den idealen Status eines Einzelstückflusses im Lean Manufacturing kann zu einer dramatischen Zunahme von Lagerbuchungen führen, wenn jeder Entnahmeprozess oder jede Kanbanregistrierung Buchungen für verbrauchte Artikel verursacht. Die Produktionsflussarchitektur ermöglicht die Übertragung des Materials zum Produktionsfluss mit Entnahme-Kanbans in Lager- oder Transporthandhabungseinheitsgrößen. Der Wert des ausgegebenen Materials wird zum Ressource in Fertigung-Konto (RIF) hinzugefügt, das dem Produktionsfluss zugeordnet ist, ähnlich dem Material, das einem Produktionsauftrag zugeordnet ist. Dieses Verhalten ähnelt dem Verhalten für Material, das mit einem Produktionsauftrag ausgegeben wird. Dasselbe Prinzip kann für Produkte und Halbfertigprodukte angewendet werden. Sofern diese Produkte nicht innerhalb eines Produktionsflusses erstellt, übertragen oder verbraucht werden, sind Lagerbuchungen optional und nicht obligatorisch. Sobald die Produkte zum Bestand gebucht werden, wird das RIF-Konto für den Produktionsfluss reduziert, indem dieses von den zugehörigen Standardkosten abgezogen wird.

## <a name="value-streams-and-value-stream-mapping"></a>Wertströme und Wertstromzuordnung
Die Architektur des Lean Manufacturing basiert auf den fünf Lean-Prinzipien von Womack und Jones: Kundenwert, Wertstrom, Fluss-Prinzip, Pull-Prinzip und Perfektion. Eine genehmigte Methode zum Implementieren von Lean Manufacturing-Lösungen in der physischen Welt der Fertigung ist die Wertstromzuordnung. Diese Methode wurde von Rother und Shook in deren Veröffentlichung "Learning to See" vom Lean Manufacturing Institute herausgegeben. 

Es können die künftigen Status-Wertströme als Produktionsflussversion modelliert werden. Alle Prozesse des Wertstroms werden als Verarbeitungsaktivitäten modelliert. Bewegungen oder Übertragungen können als Umlagerungsaktivitäten modelliert werden, wenn der Übergangsstatus erfasst werden muss oder wenn eine Integration für Bestandsentnahme oder konsolidierte Lieferungen erforderlich ist. 

Der Wertstrom selbst wird als Organisationseinheit modelliert. Daher kann der Wertstrom als Finanzdimension verwendet werden.

Weitere Informationen zum Erstellen von Organisationseinheiten finden Sie unter [Organisationseinheiten erstellen](../../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md).

## <a name="costing-for-lean-manufacturing-based-on-the-production-flow"></a>Kosten für Lean Manufacturing basierend auf dem Produktionsfluss
Die regelmäßige Konsolidierung der Kosten für einen Produktionsfluss korrigiert das zugehörige RIF-Konto und ermöglicht die Bestimmung von Abweichungen für die Produkte , die vom Produktionsfluss geliefert werden.

## <a name="continuous-improvement"></a>Fortlaufende Verbesserung
Um die fortlaufende Verbesserung zu unterstützen, werden die Produktionsflüsse in zeiteffektiven Versionen implementiert. Daher kann eine vorhandene Produktionsflussversion zusammen mit allen zugehörigen Kanban-Regeln zu einer künftigen Version des Produktionsflusses kopiert werden. Darüber hinaus kann der künftige Produktionsflussstatus modelliert werden, bevor er für die Produktion geprüft und aktiviert wird. Um einen nahtlosen Materialfluss am Umbuchungsdatum und darüber hinaus zu gewährleisten, werden vorhandene Kanbans aus alten Produktionsflussversionen automatisch der neuen Version zugeordnet.

## <a name="simplicity"></a>Einfachheit
Für die Implementierung des Lean Manufacturing haben wir den Produktionsfluss und den Aktivitätsansatz ausgewählt, der die Modellierung von einfachen und komplexen Produktionsszenarien in einer einzelnen skalierbaren Architektur ermöglicht. Eine genauere Betrachtung des Aktivitätskonzepts zeigt eine neue Einfachheit für die Benutzer, die es wirklich brauchen: Die Fertigungs- und die Logistikarbeitskräfte. Durch Berichte anhand aktivitätsbasierter Einzelvorgänge anstelle der Lagerbuchungen überträgt eine einheitliche Benutzeroberfläche für alle Lean Manufacturing-Varianten die Geschäftskomplexität von der Benutzeroberfläche dahin, wo sie gehört: zum Produktionsfluss als Grundlage des Lean Manufacturing.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]