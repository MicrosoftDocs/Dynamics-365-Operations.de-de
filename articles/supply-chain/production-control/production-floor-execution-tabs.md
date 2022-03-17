---
title: Gestalten der Ausführungsschnittstelle auf Produktionsebene
description: Dieses Thema beschreibt, wie Sie den Inhalt der Benutzeroberfläche für jede Konfiguration entwerfen.
author: johanhoffmann
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecutionConfiguration, JmgProductionFloorExecutionConfigurationTab
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: ee206ced76dbdd356c77d34a4b8f197879e9a3f0
ms.sourcegitcommit: 2e554371f5005ef26f8131ac27eb171f0bb57b4e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2022
ms.locfileid: "8384771"
---
# <a name="design-the-production-floor-execution-interface"></a>Gestalten der Ausführungsschnittstelle auf Produktionsebene

[!include [banner](../includes/banner.md)]

Sie können den Inhalt der Benutzeroberfläche für jede Konfiguration entwerfen, die von der Produktionsausführungsoberfläche verwendet wird. So kann es z. B. sein, dass die Arbeitskräfte in einer Arbeitszelle in der Lage sein müssen, Arbeitsanweisungen im Produktionsbereich zu öffnen, während in einer anderen Arbeitszelle keine Anweisungen benötigt werden. In diesem Fall sollten zwei Konfigurationen erstellt werden, eine mit einer Schaltfläche zum Öffnen von Dokumentenanhängen und eine ohne diese Schaltfläche.

## <a name="design-a-tab"></a>Gestalten Sie eine Registerkarte

Auf der Seite **Produktionsablauf konfigurieren** können Sie Registerkarten erstellen und konfigurieren, indem Sie **Registerkarten entwerfen** im Aktivitätsbereich wählen.

Jede Registerkarte ist in vier Abschnitte unterteilt, wie in der folgenden Abbildung gezeigt.

![Registerkarten-Layout.](media/pfe-tab-layout.png "Anordnung der Registerkarten")

Die folgenden Elemente sind in der Abbildung zu sehen:

1. Primäre Symbolleiste
1. Sekundäre Symbolleiste
1. Hauptansicht
1. Detaillierte Ansicht

Um eine neue Registerkarte zu erstellen und zu konfigurieren, gehen Sie wie folgt vor:

1. Gehen Sie zu **Produktionskontrolle \> Einrichtung \> Fertigungsausführung \> Ausführung in der Produktion**.

1. Wählen Sie **Design-Registerkarten** im Aktivitätsbereich, um die Seite **Design-Registerkarten** zu öffnen.

    ![Die Seite „Entwurfsregisterkarten“.](media/pfe-design-tabs.png "Die Seite Registerkarten Design")

1. Wählen Sie im Aktivitätsbereich **Neu** aus.

1. Legen Sie die folgenden Einstellungen in der Kopfzeile der Seite fest:

    - **Registerkartenname** – Geben Sie einen Namen für die Registerkarte an.
    - **Hauptansicht** - Wählen Sie aus den vordefinierten Auftragslisten (*Aktive Aufträge*, *Alle Aufträge*, *Meine Aufträge* und *Mein Rechner*).
    - **Detailansicht** – Wählen Sie zwischen einem leeren Wert oder **Auftragsdetails**. Wenn Sie den leeren Wert wählen, gibt es in der Registerkarte keine Detailansicht. Wenn Sie **Job-Details** wählen, enthält die Detailansicht eine detaillierte Beschreibung des Jobs, der in der Jobliste in der Hauptansicht ausgewählt ist.

1. Im Bereich **Primäre Symbolleiste** wählen Sie, welche Schaltflächen in der primären Symbolleiste verfügbar sein sollen. Die Spalte **Verfügbare Aktionen** zeigt eine Liste mit allen Schaltflächen, die hinzugefügt werden können. Die Spalten **Ausgewählte Aktionen** zeigt eine Liste aller Schaltflächen, die in der aktuellen Konfiguration enthalten sind. Verwenden Sie die Schaltflächen zwischen den Spalten, um ausgewählte Elemente nach Bedarf zwischen den Spalten zu verschieben. Verwenden Sie die Aufwärts- und Abwärts-Schaltflächen neben der Spalte **Ausgewählte Aktionen**, um die Reihenfolge zu steuern, in der die Schaltflächen in der Benutzeroberfläche angezeigt werden.

1. Wählen Sie im Bereich **Sekundäre Symbolleiste**, welche Schaltflächen in der sekundären Symbolleiste verfügbar sein sollen. Die Spalte **Verfügbare Aktionen** zeigt eine Liste mit allen Schaltflächen, die hinzugefügt werden können. Die Spalten **Ausgewählte Aktionen** zeigt eine Liste aller Schaltflächen, die in der aktuellen Konfiguration enthalten sind. Verwenden Sie die Schaltflächen zwischen den Spalten, um ausgewählte Elemente nach Bedarf zwischen den Spalten zu verschieben. Verwenden Sie die Aufwärts- und Abwärts-Schaltflächen neben der Spalte **Ausgewählte Aktionen**, um die Reihenfolge zu steuern, in der die Schaltflächen in der Benutzeroberfläche angezeigt werden.

## <a name="associate-a-tab-with-a-configuration"></a>Verknüpfen einer Registerkarte mit einer Konfiguration

Nachdem Sie alle benötigten Registerkarten entworfen haben, können Sie diese mit einer Konfiguration verknüpfen.

1. Gehen Sie zu **Produktionskontrolle \> Einrichtung \> Fertigungsausführung \> Ausführung in der Produktion**.

    ![Produktionsausführung konfigurieren.](media/pfe-config-prod-floor-execution.png "Produktionsausführung konfigurieren")

1. Wählen Sie auf dem Inforegister **Registerauswahl** **Hinzufügen**.

1. Eine neue Zeile wird dem Raster hinzugefügt. Wählen Sie für diese neue Zeile den Namen einer Registerkarte, die Sie der Konfiguration hinzufügen möchten.

1. Fahren Sie fort, weitere Registerkarten nach Bedarf hinzuzufügen.

1. Verwenden Sie die Schaltflächen **Aufwärts bewegen** und **Abwärts bewegen** in der Symbolleiste, um die Registerkarten nach Bedarf anzuordnen. Die Registerkarten werden von links nach rechts in der im obigen Screenshot gezeigten Reihenfolge angezeigt (die oberste Registerkarte wird links angezeigt).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
