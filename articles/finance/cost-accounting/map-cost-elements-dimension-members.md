---
title: Kostenelement-Dimensionselemente einem allgemeinen Satz von Dimensionselementen zuordnen
description: Indem Sie verschiedene Kostenelement-Dimensionsmitglieder einem gemeinsamen Satz von Kostenelement-Dimensionsmitgliedern zuordnen, führen Sie Daten in einem gemeinsamen Format zu Analysezwecken zusammen.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMDimensionMember, CAMDimensionMapping
audience: Application User
ms.reviewer: roschlom
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b9ac59f305afd55edfcfb3b47bf38ddd44d92a706904f55a069a6a9fc9050825
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728030"
---
# <a name="map-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a>Kostenelement-Dimensionselemente einem allgemeinen Satz von Dimensionselementen zuordnen

[!include [banner](../includes/banner.md)]

Indem Sie verschiedene Kostenelement-Dimensionsmitglieder einem gemeinsamen Satz von Kostenelement-Dimensionsmitgliedern zuordnen, führen Sie Daten in einem gemeinsamen Format zu Analysezwecken zusammen.

Wenn Sie ein Weltkonzern sind und den gesetzlichen Buchhaltungsanforderungen entsprechen, verwenden Sie möglicherweise mehrere Kontenpläne. Wenn Sie Kostenelement-Dimensionsmitglieder von unterschiedlichen Kontenplänen importieren, können Sie schließlich eine Mischung von Konten erhalten. Diese Konten können tatsächlich dieselben Eigenschaften haben und Sie möchten möglicherweise mithilfe eines gemeinsamen Formats die Kosten für sie analysisieren und zuteilen.

## <a name="map-cost-element-dimension-members-to-a-common-format"></a>Kostenelement-Dimensionsmitglieder einem gemeinsamen Format zuordnen
Das folgende Beispiel veranschaulicht, wie Sie als Kostencontroller eine neue Kostenelementdimension in „Kostenrechnung” erstellen können, die Kostenelement-Dimensionsmitglieder aus der US-Kontenplanstruktur und der französischen Kontenplanstruktur einem gemeinsamen Satz von Kostenelement-Dimensionsmitgliedern zuweist. Sie können dann den gemeinsamen Satz von Kostenelement-Dimensionsmitgliedern verwenden, um Kostendaten aus zwei juristischen Personen in einem Kostenrechnungs-Sachkonto zu analysieren.

| Quelle: US-Kontenplan                                          | Quelle: Französischer Kontenplan                                          | Neuer gemeinsamer Satz von Kostenelement-Dimensionsmitgliedern                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| Importierte Kostenelement-Dimensionsmitglieder vom US-Kontenplan | Importierte Kostenelement-Dimensionsmitglieder aus dem französischen Kontenplan | Zuordnung von US-amerikanischen und französischen Kostenelement-Dimensionsmitgliedern zu einem gemeinsamen Satz |
| 5001: Vertrieb                                                           | 5001: Vertrieb und Werbung                                               | 5000: Vertrieb und Werbung                                             |
| 5030: Werbung                                                     | 6390: Bestandseinkauf\*                                                    | 7000: Reinigungsausgaben                                                 |
| 7001: Reinigungsausgaben                                               | 7001: Reisekosten                                                      | 7001: Reisekosten                                                   |

\*Das französische Kostenelement-Dimensionsmitglied des Bestandskaufs ist nicht zugeordnet.

## <a name="currency-conversion"></a>Währungskonvertierung
Die verschiedenen Kontenpläne, die Sie verwenden, sind möglicherweise für die Verwendung verschiedener Währungen eingerichtet. In diesem Fall sollten Sie sicherstellen, dass Sie eine Währungsumrechnung angeben, sodass Kostendaten mithilfe der korrekten Währung verarbeitet werden, wie im Kostenrechnungs-Sachkonto definiert, wo die Kostenelement-Dimensionsmitglieder verwendet werden. Wenn im vorherigen Beispiel US-Dollar (USD) im Kostenrechnungs-Sachkonto verwendet werden, müssen Sie eine Währungsumrechnung von USD zu Euro (EUR) erstellen, um Buchungen für die zugeordneten Kostenelement-Dimensionsmitglieder zu verarbeiten.

## <a name="update-mappings-at-any-time"></a>Zuordnungen jederzeit aktualisieren
Sie können die Zuordnungsdefinitionen für eine Kostenelementdimension jederzeit aktualisieren. Da Zuordnungen nicht ab einem bestimmten Datum gültig sind, werden Änderung das nächste Mal, wenn Sie Kostenbuchungen verarbeiten oder Kostenberechnungen ausführen, angewendet.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]