---
title: Containergewicht und -volumen bei Auslastung einschließen
description: In diesem Artikel wird beschrieben, wie die Funktion zum Einbezug von Containergewicht und Volumen eingerichtet wird.
author: Weijiesa
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateRouteWorkbench, TMSDriverLogListPage, TMSTransportationTender
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66dc84171f8b175476f37f736489d3d83cacfe57
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897399"
---
# <a name="include-container-weight-and-volume-on-load"></a>Containergewicht und -volumen bei Auslastung einschließen

[!include [banner](../includes/banner.md)]

Die Funktionen zum Einschließen des Containergewichts und -Volumens auf eine Auslastung geben eine Darstellung des Gesamtgewichts und des Volumens der Container und der Artikel, die auf einer Auslastung sind.

Eine Auslastung enthält eine einzelne Lieferung oder mehrere Lieferungen und diese Lieferungen enthalten eindeutige Artikel, die zu einem einzelnen Auftrag oder mehreren Aufträgen gehören. Die Artikel werden innerhalb eines Containers gelagert und die Container werden auf eine Auslastung  geladen. Artikel, die außerhalb eines Containers sind, können auch Teil einer Kapazität sein. Basierend auf diesen Bedingungen berechnet das System Werte für das Gewicht und das Volumen für die Auslastung, indem das Gewicht und das Volumen von Containern und Artikeln berücksichtigt wird.

Wenn die berechneten Werte nicht präzis sind, können Sie sie regulieren, indem Sie den Istwerten auf das Gewicht und das Volumen für die Last eingeben. Die Werte für das Gewicht und das Volumen werden in den Transportverwaltungsprozessen verwendet. Beispielsweise werden die Werte im Routenworkbench-Satz verwendet, wo sie den Satz und für in den Arbeitsplan definieren, und sie werden auch für Transportzahlungsmittel und Fahrereinchecken verwendet.

## <a name="where-it-applies"></a>Wofür es angewendet wird

Die Funktionen zum Einschließen des Containergewichts und -Volumens auf eine Auslastung gelten in den Transportverwaltungsprozessen, wie der Routenworkbench-Satz, die Transportzahlungsmitteln und Fahrer einchecken.

## <a name="how-it-is-set-up"></a>Wie er installiert wird

Die Anzahl an Containern, die für eine Auslastung berücksichtigt werden sollen, wird anhand des Gewichts und des Volumens der Container und auf dem Prozentsatz der Containers berechnet.

-   Um das Gewicht und das Volumen für einen Container festzulegen, klicken Sie auf **Lagerortverwaltung** \> **Einstellungen** \> **Container** \> **Containertypen**.

-   Um den Containernutzungsprozentsatz einzurichten, klicken Sie auf **Lagerortverwaltung** \> **Einstellungen** \> **Container** \> **Containergruppen** und geben einen Wert in das Feld **Containernutzungsprozentsatz** ein.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]