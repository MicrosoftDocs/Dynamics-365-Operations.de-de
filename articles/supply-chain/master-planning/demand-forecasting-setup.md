---
title: Einrichten einer Bedarfsplanung
description: In diesem Thema werden die Einrichtungsaufgaben, die Sie ausführen müssen, um die Bedarfsplanung vorzubereiten, beschrieben.
author: roxanadiaconu
manager: AnnBe
ms.date: 09/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72653
ms.assetid: c5fa4b09-512d-4349-ac51-cc13da69a160
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 048b0e8e57211893cae538fae20e87186399dd38
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813798"
---
# <a name="demand-forecasting-setup"></a>Einrichten einer Bedarfsplanung

[!include [banner](../includes/banner.md)]

In diesem Thema werden die Einrichtungsaufgaben, die Sie ausführen müssen, um die Bedarfsplanung vorzubereiten, beschrieben.  

Zu den Einrichtungsaufgaben zählt das Einrichten der folgenden Daten und Parameter.

## <a name="item-allocation-key"></a>Artikelzuteilungsschlüssel
Eine Bedarfsplanung wird für einen Artikel und die dazugehörigen Dimensionen nur berechnet, wenn der Artikel Teil eines Artikelverteilungsschlüssels ist. Diese Regel erzwingt das Gruppieren größerer Mengen, sodass die Bedarfsplanungen schneller erstellt werden können. Der Artikelverteilungsschlüsselprozentsatz wird ignoriert, wenn Bedarfsplanungen generiert werden. Planungen werden auf der Grundlage von historischen Daten erstellt. 

Ein Artikel und die dazugehörigen Dimensionen müssen nur zu einem Artikelverteilungsschlüssel gehören, wenn der Artikelverteilungsschlüssel für die Planungserstellung verwendet wird. 

Um eine Lagermengeneinheit (LME) einem Artikelverteilungsschlüssel hinzuzufügen, gehen Sie zu **Masterplanung** &gt; **Einstellungen** &gt; **Bedarfsplanung** &gt; **Artikelverteilungsschlüssel**. Verwenden Sie die Seite **Artikel zuweisen**, um einen Artikel zu einem Verteilungsschlüssel zuzuweisen.

## <a name="intercompany-planning-groups"></a>Intercompany-Planungsgruppen
Die Bedarfsplanung generiert unternehmensübergreifende Planungen. In Dynamics 365 Supply Chain Management werden Unternehmen, die zusammen geplant werden, in einer Intercompany-Planungsgruppe gruppiert. Um pro Unternehmen anzugeben, welche Artikelverteilungsschlüssel für die Bedarfsplanung berücksichtigt werden sollen, ordnen Sie einen Artikelverteilungsschlüssel dem Intercompany-Planungsgruppenmitglied zu, indem Sie zu **Masterplanung** &gt; **Einstellungen** &gt; **Intercompany-Planungsgruppen** wechseln. 

Wenn den Intercompany-Planungsgruppenmitgliedern keine Artikelverteilungsschlüssel zugewiesen sind, wird standardmäßig eine Bedarfsplanung für alle Artikel berechnet, die allen Artikelverteilungsschlüsseln aus allen Unternehmen zugewiesen sind. Zusätzliche Filteroptionen für Unternehmen und Artikelverteilungsschlüssel sind auf der Seite **Statistische Grundplanung generieren** verfügbar. 

Prüfen Sie die Anzahl der geplanten Artikel. Unnötige Artikel verursachen möglicherweise höhere Kosten, wenn Sie Microsoft Azure Machine Learning verwenden.

## <a name="demand-forecasting-parameters"></a>Bedarfsplanungsparameter
Um die Parameter der Bedarfsplanung einzurichten, wechseln Sie zu **Masterplanung** &gt; **Einstellungen** &gt; **Bedarfsplanungsparameter**. Da die Bedarfsplanung unternehmensübergreifend ausgeführt wird, sind die Einstellungen global. Das bedeutet, sie beziehen sich auf alle Unternehmen. 

Die Bedarfsplanung generiert die Planung in Mengen. Daher muss die Maßeinheit, in der die Menge ausgedrückt werden soll, im Feld **Bedarfsplanungseinheit** angegeben werden. Die Maßeinheit muss eindeutig sein, um sicherzustellen, dass die Aggregation und Prozentverteilung sinnvoll sind. Weitere Informationen zur Aggregation und Prozentverteilung finden Sie unter [Manuelle Anpassungen der Grundplanung](manual-adjustments-baseline-forecast.md). Für jede Maßeinheit, die für Lagermengeneinheiten verwendet wird, die in der Bedarfsplanung enthalten sind, überprüfen Sie, ob eine Umrechnungsregel für die Maßeinheit und die allgemeine Maßeinheit der Planung vorliegt. Wenn die Planungsgenerierung ausgeführt wird, wird die Liste der Artikel, die keine Maßeinheitsumrechnung haben, protokolliert, damit Sie die Einstellungen leicht korrigieren können. 

Die Bedarfsplanung kann verwendet werden, um abhängigen und unabhängigen Bedarf zu planen. Wenn beispielsweise nur das Kontrollkästchen **Auftrag** aktiviert wird und wenn alle Artikel, die für die Bedarfsplanung berücksichtigt werden, verkauft wurden, berechnet das System unabhängigen Bedarf. Allerdings können wichtige Unterkomponenten zu den Artikelverteilungsschlüsseln hinzugefügt werden und in die Bedarfsplanung einbezogen werden. Wenn in diesem Fall das Kontrollkästchen **Produktionsauftragsposition** aktiviert ist, wird eine abhängige Planung berechnet. 

Es gibt zwei Methoden zum Erstellen einer Grundplanung. Sie können Planungsmodelle für historische Daten verwenden, oder Sie können die historischen Daten in die Planung kopieren. Im Feld **Planungsgenerierungsstrategie** können Sie zwischen diesen beiden Methoden auswählen. Um die Planungsmodelle zu verwenden, wählen Sie **Azure Machine Learning** aus. 

Wenn Sie auf **Planungsdimensionen** im linken Bereich der Seite **Bedarfsplanungsparameter** klicken, können Sie auch die Gruppe von Planungsdimensionen auswählen, die verwendet werden soll, wenn die Bedarfsplanung generiert wird. Eine Planungsdimension gibt die Detailebene an, für die die Planung definiert ist. Unternehmen, Standort und Artikelverteilungsschlüssel sind erforderliche Planungsdimensionen, aber Sie können Planungen auch für Lagerort, Bestandsstatus, Debitorengruppe, Debitorenkonto, Land/Region, Bundesland und Artikel sowie alle Artikeldimensionsebenen generieren. 

Sie können jederzeit Planungsdimensionen zur Liste mit den Dimensionen hinzufügen, die für Bedarfsplanung verwendet werden. Sie können Planungsdimensionen auch aus der Liste entfernen. Allerdings gehen manuelle Anpassungen verloren, wenn Sie eine Planungsdimension hinzufügen oder entfernen. 

Nicht alle Artikel verhalten sich aus der Perspektive der Bedarfsplanung auf dieselbe Weise. Ähnliche Artikel können in einem Artikelverteilungsschlüssel gruppiert werden, und Parameter wie Buchungsarten und Planungsmethodeneinstellungen können pro Artikelverteilungsschlüssel festgelegt werden. Klicken Sie auf **Artikelverteilungsschlüssel** im linken Bereich der Seite **Bedarfsplanungsparameter**. 

Um die Planung zu generieren, verwendet Supply Chain Management einen Machine Learning-Webdienst. Um die Verbindung mit dem Dienst herzustellen, müssen Sie die folgenden Informationen bereitstellen, wenn Sie sich bei Microsoft Azure Machine Learning Studio anmelden:

-   API-Schlüssel des Webdiensts
-   URL des Webdienst-Endpunkts
-   Azure-Speicherkontoname
-   Azure-Speicherkontoschlüssel

> [!NOTE]
> Azure-Speicherkontenname und -schlüssel sind nur erforderlich, wenn Sie ein benutzerdefiniertes Speicherkonto verwenden. Wenn Sie die lokale Version bereitstellen, müssen Sie ein benutzerdefiniertes Speicherkonto auf Azure haben, sodass der Machine Learning-Dienst auf die historischen Daten zugreifen kann. 

Um Bedarfsvorhersagen zu erstellen, können Sie Ihren eigenen Dienst bereitstellen, indem Sie Machine Learning Studio- oder Supply Chain Management-Bedarfsplanungsexperimente verwenden. Anweisungen für das Bereitstellen der Bedarfsplanungsexperimente als Webdienst sind in Supply Chain Management verfügbar. Klicken Sie auf der Seite **Bedarfsplanungsparameter** auf die Registerkarte **Azure Machine Learning**.

## <a name="settings-for-the-demand-forecasting-machine-learning-service"></a>Einstellungen für den Machine Learning-Dienst der Bedarfsplanung
Um die Parameter anzuzeigen die für den Bedarfsplanungsdienst konfiguriert werden können, gehen Sie zu **Masterplanung** &gt; **Einstellungen** &gt; **Bedarfsplanung** &gt; **Planungsalgorithmusparameter**. Die **Planungsalgorithmusparameter** Seite zeigt die Standardwerte für die Parameter an. Sie können mithilfe der Parameter die **Bedarfsplanungsparameter** überschreiben. Verwenden Sie die Registerkarte **Allgemein**, um die Parameter global zu überschreiben, oder klicken Sie auf die Registerkarte **Artikelverteilungsschlüssel**, um die Parameter pro Artikelverteilungsschlüssel zu überschreiben. Parameter, die für einen Artikelverteilungsschlüssel überschreiben werden, wirken sich nur auf die Planung von Artikeln aus, die diesem Artikelverteilungsschlüssel zugeordnet sind.

### <a name="forecast-algorithm-parameters"></a>Planungsalgorithmusparameter

Auf der Registerkarte **Verteilungsschlüssel** können Sie den **Planungsalgorithmusparameter** für jeden Artikelverteilungsschlüssel festlegen. Die folgenden Optionen sind verfügbar.
- **Zuverlässigkeitsstufe (Prozentsatz)**: Ein Zuverlässigkeitsintervall besteht aus einem Wertebereich, der eine gute Einschätzung der Bedarfsplanung ermöglicht. Eine Zuverlässigkeitsstufe von 95 % bedeutet beispielsweise, dass der zukünftige Bedarf mit einer Chance von 5 % aus dem Intervallbereich der Zuverlässigkeit fällt.
- **Saisonalität erzwingen**: Gibt an, ob das Modell gezwungen wird, eine bestimmte Art der Saisonalität zu verwenden. Dies bezieht sich nur auf ARIMA und ETS. Optionen: AUTO (Standard), KEINE, ADDITIV, MULTIPLIKATIV.
- **Planungsmodell**: Optionen: ARIMA, ETS, STL, ETS+ARIMA, ETS+STL, ALLE. Um das Modell auszuwählen, das sich am besten eignet, verwenden Sie **ALLE**.
- **Maximaler vorhergesagter Wert**: Gibt den Maximalwert an, der für Vorhersagen verwendet werden kann. Format: +1E[n] oder numerische Konstante.
- **Minimaler vorhergesagter Wert**: Gibt den Minimalwert an, der für Vorhersagen verwendet werden kann. Format: -1E[n] oder numerische Konstante.
- **Fehlende Wertersetzung**: Gibt an, wie Lücken in historischen Daten ausgefüllt werden. Optionen: numerischer Wert, MITTLERE, VORHERIGE, LINEARINTERPOLATION, POLYNOMINTERPOLATION.
- **Umfang der fehlenden Wertersetzung**: Gibt an, ob die Wertersetzung nur auf den Datenbereich jedes einzelnen Granularitätsattributs angewendet wird, oder auf den gesamten Dataset. Optionen: GRANULARITÄTS_ATTRIBUT (Standard), GLOBAL.
- **Hinweis zur Saisonalität**: Geben Sie für Saisondaten einen Hinweis an das Planungsmodell, um die Planungsgenauigkeit zu verbessern. Format: Ganzzahl, die die Anzahl der Zeitrahmen angibt, in denen sich ein Bedarfsmuster wiederholt. Geben Sie zum Beispiel „6“ für Daten ein, die alle 6 Monate wiederholt werden.
- **Testsatzgröße in Prozent**: Prozentsatz der historischen Daten, die als Testsatz für die Prognose der Genauigkeitsberechnung verwendet werden. 

<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Bedarfsplanung – Übersicht](introduction-demand-forecasting.md)

[Eine statistische Grundplanung generieren](generate-statistical-baseline-forecast.md)

[Manuelle Anpassungen an der Grundplanung](manual-adjustments-baseline-forecast.md)



