---
title: "Hiermit können Sie verschiedene Kostenfaktordimensionsmitgliedern einem Common zu, das von den Dimensionsmitgliedern festgelegt wird"
description: "Indem Sie verschiedene Kostenelement-Dimensionsmitglieder einem gemeinsamen Satz von Kostenelement-Dimensionsmitgliedern zuordnen, führen Sie Daten in einem gemeinsamen Format zu Analysezwecken zusammen."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-11-01 13 - 45 - 07
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CAMDimension, CAMDimensionMember
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: a1e9817b6ee596ad516531d7597a2a39e115749c
ms.lasthandoff: 03/31/2017


---

# <a name="map-different-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a>Hiermit können Sie verschiedene Kostenfaktordimensionsmitgliedern einem Common zu, das von den Dimensionsmitgliedern festgelegt wird

Indem Sie verschiedene Kostenelement-Dimensionsmitglieder einem gemeinsamen Satz von Kostenelement-Dimensionsmitgliedern zuordnen, führen Sie Daten in einem gemeinsamen Format zu Analysezwecken zusammen.

Wenn Sie ein Weltkonzern sind und den gesetzlichen Buchhaltungsanforderungen entsprechen, verwenden Sie möglicherweise mehrere Kontenpläne. Wenn Sie Kostenelement-Dimensionsmitglieder von unterschiedlichen Kontenplänen importieren, können Sie schließlich eine Mischung von Konten erhalten. Diese Konten können tatsächlich dieselben Eigenschaften haben und Sie möchten möglicherweise mithilfe eines gemeinsamen Formats die Kosten für sie analysisieren und zuteilen.

## <a name="map-cost-element-dimension-members-to-a-common-format"></a>Kostenelement-Dimensionsmitglieder einem gemeinsamen Format zuordnen
Das folgende Beispiel veranschaulicht, wie Sie als Kostencontroller eine neue Kostenelementdimension in „Kostenrechnung” erstellen können, die Kostenelement-Dimensionsmitglieder aus der US-Kontenplanstruktur und der französischen Kontenplanstruktur einem gemeinsamen Satz von Kostenelement-Dimensionsmitgliedern zuweist. Sie können dann den gemeinsamen Satz von Kostenelement-Dimensionsmitgliedern verwenden, um Kostendaten aus zwei juristischen Personen in einem Kostenrechnungs-Sachkonto zu analysieren.

| Quelle: US-Kontenplan                                          | Quelle: Französischer Kontenplan                                          | Neuer gemeinsamer Satz von Kostenelement-Dimensionsmitgliedern                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| Importierte Kostenelement-Dimensionsmitglieder vom US-Kontenplan | Importierte Kostenelement-Dimensionsmitglieder aus dem französischen Kontenplan | Zuordnung von US-amerikanischen und französischen Kostenelement-Dimensionsmitgliedern zu einem gemeinsamen Satz |
| 5001: Vertrieb                                                           | 5001: Vertrieb und Werbung                                               | 5000: Vertrieb und Werbung                                             |
| 5030: Werbung                                                     | 6390: Aktienkauf \*                                                    | 7000: Reinigungsausgaben                                                 |
| 7001: Reinigungsausgaben                                               | 7001: Reisekosten                                                      | 7001: Reisekosten                                                   |

\*Das französische Kostenfaktor-Dimensionsmitglied des Aktienkaufs wird nicht zugeordnet.

## <a name="currency-conversion"></a>Währungskonvertierung
Die verschiedenen Kontenpläne, die Sie verwenden, sind möglicherweise für die Verwendung verschiedener Währungen eingerichtet. In diesem Fall sollten Sie sicherstellen, dass Sie eine Währungsumrechnung angeben, sodass Kostendaten mithilfe der korrekten Währung verarbeitet werden, wie im Kostenrechnungs-Sachkonto definiert, wo die Kostenelement-Dimensionsmitglieder verwendet werden. Wenn im vorherigen Beispiel US-Dollar (USD) im Kostenrechnungs-Sachkonto verwendet werden, müssen Sie eine Währungsumrechnung von USD zu Euro (EUR) erstellen, um Buchungen für die zugeordneten Kostenelement-Dimensionsmitglieder zu verarbeiten.

## <a name="update-mappings-at-any-time"></a>Zuordnungen jederzeit aktualisieren
Sie können die Zuordnungsdefinitionen für eine Kostenelementdimension jederzeit aktualisieren. Da Zuordnungen nicht ab einem bestimmten Datum gültig sind, werden Änderung das nächste Mal, wenn Sie Kostenbuchungen verarbeiten oder Kostenberechnungen ausführen, angewendet.


