---
title: Experimentieren in Dynamics 365 Commerce
description: Das Experimentieren ermöglicht das Erstellen, Bearbeiten und Verwalten von Seitenlayouts und Inhaltsbehandlungen im Site Builder. Die Unterstützung von End-to-End-Experimenten ist für E-Commerce-Seiten und -Entitäten innerhalb einer Seite aktiviert.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 7e415bc0a4ced11c5bb8393fe5dfe03a5f7cdd6c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798986"
---
# <a name="experimentation-in-dynamics-365-commerce"></a>Experimentieren in Dynamics 365 Commerce
Verwenden Sie Experimente in Dynamics 365 Commerce, um Hypothesen über die Effektivität Ihrer E-Commerce-Seiten zu validieren und Entscheidungen mit datengesteuertem Vertrauen zu treffen. Commerce unterstützt A/B-Tests auf Seiten, in Modulen und Fragmenten und ermöglicht es Ihnen, die Auswirkungen vorgeschlagener Änderungen an Ihrer Website zu messen.

Sie können Seiten- und Inhaltsbehandlungen erstellen, bearbeiten und verwalten, die im Commerce Site Builder als **Variationen** bezeichnet werden. Commerce lässt sich in Dienste von Drittanbietern integrieren, mit denen Sie Experimente und Behandlungsaufgaben erstellen können. In Commerce erfasste Echtzeit-Ereignisströme ermöglichen die Analyse, die die Versuchsergebnisse im Drittanbieterdienst definiert. Sie können diese Analysen dann nutzen, um Ihre Hypothese zu unterstützen oder zu widerlegen.

## <a name="set-up-prerequisites"></a>Einrichten von Voraussetzungen
1. **Holen Sie sich die richtige Version von Commerce** – Aktualisieren Sie Ihre Modulbibliothek, das Online-Kanalerweiterungs-Softwareentwicklungskit (SDK) und Commerce Scale Unit auf Commerce Version 10.0.13 oder höher.
1. **Richten Sie einen Experimentier-Connector ein** – Über einen Experimentier-Connector kann Commerce eine Verbindung zu Diensten von Drittanbietern herstellen, um die Liste der Experimente abzurufen und zu bestimmen, wann einem Benutzer ein Experiment angezeigt werden soll. Sie können einen Connector eines Drittanbieters unter [AppSource](https://appsource.microsoft.com) erwerben. Befolgen Sie die Einrichtungsanweisungen des Herausgebers. Alternativ können Sie den Beispieltest-Connector von Commerce verwenden, um den Experimentierworkflow zu testen, ohne einen externen Dienst konfigurieren zu müssen. Weitere Informationen finden Sie unter [Connectors konfigurieren und aktivieren](e-commerce-extensibility/connectors.md). 
1. **Aktivieren Sie die Experimentierfunktionsflags in Commerce** – Sie können das Experimentieren auf Mandantenebene aktivieren, indem Sie zu **Mandanteneinstellungen > Funktionen** gehen oder auf Site-Ebene bei **Site-Einstellungen > Funktionen**.
    - Aktivieren Sie das **Experimentieren**-Flag, um Experimentvarianten von Modulen innerhalb einer Seite zu erstellen, ohne andere Inhalte zu beeinflussen oder zu kopieren, die nicht Teil des Experiments sind. Dadurch wird sichergestellt, dass laufende Inhaltsaktualisierungen außerhalb des Experiments während des Experimentlebenszyklus synchron bleiben. Durch Deaktivieren dieses Flags wird verhindert, dass alle Experimente den Benutzern angezeigt werden, und alle Bearbeitungsfunktionen im Site Builder werden entfernt.
    - Aktivieren Sie das Flag zum **Experimentieren an Seiten oder Fragmenten** zum Ausführen von Experimenten an einer Seite oder einem Fragment. Dadurch wird eine vollständige Instanzkopie der gesamten Seite oder des gesamten Fragments für alle Module innerhalb der Seite oder des Fragments erstellt. Verwenden Sie diesen Modus, wenn Sie umfassende Inhaltsänderungen testen möchten oder wenn das Synchronisieren laufender Inhaltsänderungen über Instanzen hinweg kein Problem darstellt. Das Deaktivieren dieses Flags verhindert das Erstellen und Bearbeiten neuer Experimente auf Seiten und Fragmenten.
    > [!NOTE]
    > Das **Experimentieren**-Flag muss auch für die Funktion zum **Experimentieren an Seiten oder Fragmenten** aktiviert sein, um zu funktionieren.
    
## <a name="experimentation-lifecycle"></a>Experimentierlebenszyklus
Das Einrichten eines Experiments, das Erstellen von Variationen und das Ausführen eines Experiments ist ein iterativer Prozess. Das folgende Diagramm zeigt den Experimentierlebenszyklus in Commerce und dem Drittanbieterdienst. 

[ ![Experimentierlebenszyklus](./media/experimentation_lifecycle.svg) ](./media/experimentation_lifecycle.svg#lightbox)

Weitere Informationen zu den einzelnen Schritten des Experimentierprozesses finden Sie in den folgenden Themen.
- [Eine Hypothese identifizieren und Metriken für ein Experiment bestimmen](experimentation-identify.md)
- [Experiment einrichten](experimentation-setup.md)
- [Experiment verbinden und bearbeiten](experimentation-connect-edit.md)
- [Experiment in der Vorschau anzeigen und veröffentlichen](experimentation-preview-publish.md)
- [Ein Experiment ausführen und überwachen](experimentation-run-monitor.md)
- [Variation entwickeln und Experiment abschließen](experimentation-review-complete.md)

> [!NOTE]
> Um zu erfahren, wo sich ein Experiment im Lebenszyklus befindet, wählen Sie **Experimente** im linken Navigationsbereich im Site Builder. Eine Liste von Experimenten wird mit dem Status jedes Experiments sowohl in Commerce als auch im Drittanbieterdienst angezeigt. Weitere Informationen finden Sie unter [Überprüfen Sie den Status eines Experiments](experimentation-status.md).

## <a name="next-step"></a>Nächster Schritt
[Eine Hypothese identifizieren und Erfolgsmetriken für ein Experiment bestimmen](experimentation-identify.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]