---
title: Einrichten einer Bedarfsplanung
description: "In diesem Thema werden die Einrichtungsaufgaben, die Sie ausführen müssen, um die Bedarfsplanung vorzubereiten, beschrieben."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72653
ms.assetid: c5fa4b09-512d-4349-ac51-cc13da69a160
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f629329f4f50bd7c8edcfd70641bace01a1c53aa
ms.lasthandoff: 03/31/2017


---

# <a name="demand-forecasting-setup"></a>Einrichten einer Bedarfsplanung

In diesem Thema werden die Einrichtungsaufgaben, die Sie ausführen müssen, um die Bedarfsplanung vorzubereiten, beschrieben.  

Zu den Einrichtungsaufgaben zählt das Einrichten der folgenden Daten und Parameter.

## <a name="item-allocation-key"></a>Artikelzuteilungsschlüssel
Eine Bedarfsplanung wird für einen Artikel und die dazugehörigen Dimensionen nur berechnet, wenn der Artikel Teil eines Artikelverteilungsschlüssels ist. Diese Regel wird, viele Artikel zu gruppieren erzwungen, sodass Bedarfsplanungen schneller erstellt werden können. Der Artikelverteilungsschlüsselprozentsatz wird ignoriert, wenn Bedarfsplanungen generiert werden. Planungen werden auf der Grundlage von historischen Daten erstellt. 

Ein Artikel und die dazugehörigen Dimensionen müssen nur zu einem Artikelverteilungsschlüssel gehören, wenn der Artikelverteilungsschlüssel für die Planungserstellung verwendet wird. 

Um einer Lagermengeneinheit (SKU) einem Artikelverteilungsschlüssel hinzuzufügen, fahren Sie ** Produktprogrammplanung ** &gt; ** Einstellungen ** &gt; ** Bedarfsplanung ** &gt; ** Artikelverteilungsschlüssel **. Verwenden Sie die Seite **Artikel zuweisen**, um einen Artikel zu einem Verteilungsschlüssel zuzuweisen.

## <a name="intercompany-planning-groups"></a>Intercompany-Planungsgruppen
Die Bedarfsplanung generiert unternehmensübergreifende Planungen. In Microsoft Dynamics 365 für Arbeitsgänge, werden Unternehmen, die zusammen geplant werden, für eine Intergesellschaftsplanungsgruppe gruppiert. Um, pro Unternehmen anzugeben, welche Artikelverteilungsschlüssel für Bedarfsplanung berücksichtigt werden sollen, ordnen Sie einen Artikelverteilungsschlüssel mit dem Intergesellschaftsplanungsgruppenmitglied nach gehende ** Produktprogrammplanung ** ** Profileinrichtung &gt; ** ** Intergesellschaftsplanungsgruppen &gt; **. 

Bei den Intergesellschaftsplanungsgruppenmitgliedern keine Artikelverteilungsschlüssel zugewiesen werden, ist eine Bedarfsplanung für alle Artikel berechnet, die von keiner Artikelverteilungsschlüssel von Dynamics 365 für alle Arbeitsgangsunternehmen zugewiesen werden. Zusätzliche Filteroptionen für Unternehmen und Artikelverteilungsschlüssel sind auf der Seite **Statistische Grundplanung generieren** verfügbar. 

Prüfen Sie die Anzahl der geplanten Artikel. Unnötige Artikel verursachen möglicherweise höhere Kosten, wenn Sie Microsoft Azure Machine Learning verwenden.

## <a name="demand-forecasting-parameters"></a>Bedarfsplanungsparameter
Um Bedarfsplanungszu Parameter eingerichtet, fahren Sie ** Produktprogrammplanung ** ** &gt; Einstellungen ** ** &gt; Bedarfsplanungsparameter **. Da die Bedarfsplanung unternehmensübergreifend ausgeführt wird, sind die Einstellungen global. Das bedeutet, sie beziehen sich auf alle Unternehmen. 

Die Bedarfsplanung generiert die Planung in Mengen. Daher muss die Maßeinheit, in der die Menge ausgedrückt werden soll, im Feld **Bedarfsplanungseinheit** angegeben werden. Die Maßeinheit muss eindeutig sein, um sicherzustellen, dass die Aggregation und Prozentverteilung sinnvoll sind. Weitere Informationen zur Aggregation und Prozentverteilung finden Sie unter [Manuelle Anpassungen der Grundplanung](manual-adjustments-baseline-forecast.md). Für jede Maßeinheit, die für Lagermengeneinheiten verwendet wird, die in der Bedarfsplanung enthalten sind, überprüfen Sie, ob eine Umrechnungsregel für die Maßeinheit und die allgemeine Maßeinheit der Planung vorliegt. Wenn die Planungsgenerierung ausgeführt wird, wird die Liste der Artikel, die keine Maßeinheitsumrechnung haben, protokolliert, damit Sie die Einstellungen leicht korrigieren können. 

Die Bedarfsplanung kann verwendet werden, um abhängigen und unabhängigen Bedarf zu planen. Wenn beispielsweise nur das Kontrollkästchen **Auftrag** aktiviert wird und wenn alle Artikel, die für die Bedarfsplanung berücksichtigt werden, verkauft wurden, berechnet das System unabhängigen Bedarf. Allerdings können wichtige Unterkomponenten zu den Artikelverteilungsschlüsseln hinzugefügt werden und in die Bedarfsplanung einbezogen werden. Wenn in diesem Fall das Kontrollkästchen **Produktionsauftragsposition** aktiviert ist, wird eine abhängige Planung berechnet. 

Es gibt zwei Methoden für das Erstellen einer Planung Basis in Dynamics 365 für Arbeitsgänge. Sie können Planungsmodelle für historische Daten verwenden, oder Sie können die historischen Daten in die Planung kopieren. Im Feld **Planungsgenerierungsstrategie** können Sie zwischen diesen beiden Methoden auswählen. Um die Planungsmodelle zu verwenden, wählen Sie **Azure Machine Learning** aus. 

Wenn Sie auf **Planungsdimensionen** im linken Bereich der Seite **Bedarfsplanungsparameter** klicken, können Sie auch die Gruppe von Planungsdimensionen auswählen, die verwendet werden soll, wenn die Bedarfsplanung generiert wird. Eine Planungsdimension gibt die Detailebene an, für die die Planung definiert ist. Unternehmen, Standort und Artikelverteilungsschlüssel sind erforderliche Planungsdimensionen, aber Sie können Planungen auch für Lagerort, Bestandsstatus, Debitorengruppe, Debitorenkonto, Land/Region, Bundesland und Artikel sowie alle Artikeldimensionsebenen generieren. 

Sie können jederzeit Planungsdimensionen zur Liste mit den Dimensionen hinzufügen, die für Bedarfsplanung verwendet werden. Sie können Planungsdimensionen auch aus der Liste entfernen. Allerdings gehen manuelle Anpassungen verloren, wenn Sie eine Planungsdimension hinzufügen oder entfernen. 

Nicht alle Artikel verhalten sich aus der Perspektive der Bedarfsplanung auf dieselbe Weise. Ähnliche Artikel können in einem Artikelverteilungsschlüssel gruppiert werden, und Parameter wie Buchungsarten und Planungsmethodeneinstellungen können pro Artikelverteilungsschlüssel festgelegt werden. Klicken Sie auf **Artikelverteilungsschlüssel** im linken Bereich der Seite **Bedarfsplanungsparameter**. 

Wenn Sie die Planung zu generieren, verwendet Dynamics 365 für einen Lernfähigkeit- Arbeitsgänge einer Maschinewebdienst. Um mit dem Dienst hergestellt werden soll, müssen Sie Dynamics 365 für Arbeitsgänge angeben die folgenden Informationen wenn es zum Microsoft Azure- einer Maschinestudio signieren:

-   API-Schlüssel des Webdiensts
-   URL des Webdienst-Endpunkts
-   Azure-Speicherkontoname
-   Azure-Speicherkontoschlüssel

**Hinweis:** Azure-Speicherkontenname und -schlüssel sind nur erforderlich, wenn Sie ein benutzerdefiniertes Speicherkonto verwenden. Wenn die lokale Version werden, muss sich ein benutzerdefiniertes Speicherkonto auf Azure haben, damit der Lernfähigkeit- einer Maschineservice die vergleichende zugreifen kann. 

Um Bedarfsvorhersagen zu erstellen, können Sie Ihre eigenen Service Bereitstellung indem Sie Lernfähigkeit- einer Maschinestudio oder das Dynamics 365 für Arbeitsgangsbedarfsplanungsexperimente verwenden. Anweisungen für die Bereitstellung des Arbeitsgangsbedarfsplanung Dynamics 365 für experimentiert, da ein Webdienst verfügbares Dynamics 365 für Arbeitsgänge sind. Klicken Sie auf der Seite **Bedarfsplanungsparameter** auf die Registerkarte **Azure Machine Learning**.

## <a name="settings-for-the-dynamics-365-for-operations-demand-forecasting-machine-learning-service"></a>Einstellungen für das Arbeitsgangsbedarfsplanungs-Lernfähigkeit-einer Dynamics 365 für Maschineservice
Um die Parameter anzuzeigen die für das Dynamics 365 für Arbeitsgangsbedarfsplanungs-Service konfiguriert werden können, laufen Sie ** Produktprogrammplanung ** ** &gt; Einstellungen ** ** &gt; Bedarfsplanung ** ** &gt; Planungsalgorithmusparameter **. ** Die Planungsalgorithmusparameter ** Seite werden die Standardwerte für die Parameter angezeigt. Sie können mithilfe der Parameter auf der Bedarfsplanungsparameter ** ** Seite setzen. Verwenden Sie die Registerkarte **Allgemein**, um die Parameter global zu überschreiben, oder klicken Sie auf die Registerkarte **Artikelverteilungsschlüssel**, um die Parameter pro Artikelverteilungsschlüssel zu überschreiben. Parameter, die für einen Artikelverteilungsschlüssel überschreiben werden, wirken sich nur auf die Planung von Artikeln aus, die diesem Artikelverteilungsschlüssel zugeordnet sind.

<a name="see-also"></a>Siehe auch
--------

[Introduction to demand forecasting](introduction-demand-forecasting.md)

[Generating a statistical baseline forecast](generate-statistical-baseline-forecast.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)


