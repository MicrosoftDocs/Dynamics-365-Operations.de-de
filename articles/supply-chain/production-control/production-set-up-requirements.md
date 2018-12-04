---
title: "Anforderungen für Produktionseinstellungen"
description: "Dieser Artikel gibt Informationen zu Einrichtungsanforderungen, bevor Sie mit der Produktionssteuerung arbeiten können."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParameters, RouteOpr, RouteOprTable, WorkCalendarTable, WorkTimeTable, WrkCtrTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 55561
ms.assetid: 1953059f-478d-4706-b461-25b89ace5fc3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 47fe11168ad2ddea2a7033eda8d8bd8220efea32
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="production-setup-requirements"></a>Anforderungen für Produktionseinstellungen

[!include [banner](../includes/banner.md)]

Dieser Artikel gibt Informationen zu Einrichtungsanforderungen, bevor Sie mit der Produktionssteuerung arbeiten können. 

Produktionssteuerung wird mit Funktionen in anderen Modulen integriert. Dadurch besteht die Möglichkeit zum Ändern von Produktionsaufträgen, und es wird sichergestellt, dass diese automatisch in allen anderen zugehörigen Prozessen und Berechnungen des Systems aktualisiert werden. Die folgenden Einrichtungsverfahren sind in der Reihenfolge aufgeführt, in der sie abgeschlossen werden sollten.

## <a name="required-baseline-setup-in-other-modules"></a>Erforderliche Grundeinstellungen in anderen Modulen
Vor der Verwendung des Moduls Produktionssteuerung müssen zunächst Informationen in anderen Modulen eingerichtet werden. Diese Einrichtung umfasst die folgenden Aufgaben:

-   Einrichten der allgemeinen Unternehmensdaten
-   Einrichten des Hauptbuchs
-   Definieren von Artikelgruppen
-   Einrichten von Sachkonten für Artikelgruppen
-   Einrichten der Lagerartikeltabelle im Modul Bestandsverwaltung.
-   Erstellen Sie Stücklisten (BOMs) und Stücklistenversionen im Modul Bestandsverwaltung.

## <a name="required-calendar-and-resource-setup"></a>Erforderliche Kalender- und Ressourceneinstellungen
Öffnen Sie vor der Verwendung des Moduls Produktionssteuerung das Modul Organisationsverwaltung, und erstellen bzw. definieren Sie den Kalender und die betrieblichen Ressourcen in der folgenden Reihenfolge:

1.  **Schichtmodelle** – Richten Sie Schichtmodelle ein, und definieren Sie die Zeiten, die für die Planung der Produktion zur Verfügung stehen.
2.  **Kalender** – Richten Sie Arbeitszeitkalender ein, und definieren Sie, welche Tage des Jahres für die Planung der Produktion zur Verfügung stehen.
3.  **Ressourcengruppen** – Ressourcengruppen einrichten, um die betrieblichen Ressourcen zu gruppieren, um eine Übersicht zu allen freien Kapazitäten zu erhalten, wenn die Planung ausgeführt wird. Sie müssen Ressourcengruppen nicht einrichten, bevor Sie betriebliche Ressourcen einrichten. Es empfiehlt sich jedoch, dass Sie wissen, wie man Ressourcen gruppiert, wenn Sie das Modul Produktionssteuerung einrichten.
4.  **Ressourcen** – Richten Sie betrieblichen Ressourcen ein, um die Ressourcen festzulegen, die zum Ausführen des Produktionsvorgangs sowie zum Planen von Kapazitäten verwendet werden.

## <a name="required-production-parameters-setup"></a>Erforderliche Einstellungen für Produktionsparameter
**Produktionssteuerungsparameter** – Richten Sie die grundlegenden Produktionsparameter ein, um die Behandlung und Verarbeitung von Produktionsaufträgen im System festzulegen. Definieren Sie, wie Produktionsaufträge erstellt, geplant und ausgeführt werden. Darüber hinaus können Sie die gewünschte Rückmeldungsart sowie die gewünschte Ausführung der Kostenrechnung auswählen.

## <a name="required-journal-name-identification"></a>Erforderliche Angabe von Journalen
**Produktionserfassungsnamen** – Geben Sie die Produktionserfassungsnamen an, die verwendet werden, um Buchungen zu registrieren und zu buchen.

## <a name="setup-if-you-use-operations"></a>Einrichten der Verwendung von Arbeitsgängen
Bei Arbeitsgängen handelt es sich um bestimmte Aktivitäten, die für die Produktion des Endprodukts abgeschlossen werden. **Hinweis:** Sie müssen die Aktivitätstypen kennen, die erforderlich sind, um den Artikel zu produzieren, und die Reihenfolge und Prioritäten dieser Aktivitäten. Sie müssen auch wissen, welche Ressourcen beteiligt sind und wie viele.

1.  **Vorgänge** – Richten Sie Arbeitsgänge für die Aufgaben ein, die für die Produktion des Endprodukts ausgeführt werden müssen.
2.  **Beziehungen** – Richten mithilfe von Arbeitsgangzuordnungen detaillierte Eigenschaften ein. Um Arbeitsgangzuordnungen zu definieren, klicken Sie **Beziehungen** auf der **Vorgänge** Seite.

## <a name="setup-if-you-use-routes"></a>Einrichten der Verwendung von Arbeitsplänen
Bei Verwendung von Arbeitsplänen müssen Arbeitsgänge für jeden einzelnen einzurichtenden Produktionsarbeitsplan vorhanden sein. Bei dem Arbeitsplan handelt es sich um die Route für den Artikel auf seinem Weg von Arbeitsgang zu Arbeitsgang – ab dem Beginn des Produktionsvorgangs bis zu dessen Ende.

1.  **Kostenkategorien** – Richten Sie Kostenkategorien ein, und definieren Sie die Kosten pro Stunde für bestimmte Vorgänge und Rüstzeiten.
2.  **Kostengruppen** – Richten Sie Kostengruppen ein, um unterschiedliche Kostenrechnungsarten zu erstellen und zu verwalten.
3.  **Arbeitsplangruppen** – Richten Sie Arbeitsplangruppen ein, und definieren Sie Parameter, die für Gruppen von Arbeitsplänen gelten sollen. Zum Erstellen von Produktionsarbeitsplänen müssen zunächst Arbeitsplangruppen eingerichtet werden.
4.  **Arbeitspläne** – Richten Sie Produktionsarbeitspläne ein, und definieren Sie Standardeinstellungen zum Steuern von Planung, Kostenrechnung/Preisgestaltung für Arbeitsplan-Arbeitsgänge sowie von Statusberichten.
5.  **Arbeitspläne** – Richten Sie Arbeitsplanversionen ein, um in der Produktion die Verwendung von Artikelvarianten zu ermöglichen.

## <a name="optional-advanced-settings"></a>Optionale erweiterte Einstellungen
1.  **Produktionsgruppen** – Richten Sie Produktionsgruppen ein, um Beziehungen zwischen dem Produktionsauftrag und den Sachkonten herzustellen. Die Sachkonten dienen zum Buchen oder zum Gruppieren von Aufträgen für die Berichterstellung.
2.  **Produktionspools** – Erstellen Sie Produktionspools zum Gruppieren von Produktionsaufträgen ein, sodass Sie dringende Produktionsaufträge verarbeiten oder Auftragsgruppen löschen und buchen können.
3.  **Eigenschaften** – Sie können Eigenschaften festlegen, um spezielle Attribute zu erstellen, die Ressourcen zugewiesen werden können, um die Reihenfolge der Produktionen zu steuern. Diese Attribute sind mit dem Schichtplan verbunden.





