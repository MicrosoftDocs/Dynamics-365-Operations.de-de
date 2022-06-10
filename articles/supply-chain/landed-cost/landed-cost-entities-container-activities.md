---
title: Containeraktivitätenentität
description: Dieses Thema enthält Informationen zu Containeraktivitäten, die verwendet werden, um den Fortschritt von Versandcontainern zu verfolgen.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 7bb2b97e8885e3b1265f0c93585873c8a64f1dfb
ms.sourcegitcommit: 611202adaa080250636efabb3b3b32b850d92d04
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2022
ms.locfileid: "8813058"
---
# <a name="container-activities-entity"></a>Containeraktivitätenentität

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

Containeraktivitäten werden verwendet, um den Fortschritt von Versandcontainern zu verfolgen. Für jede Teilstrecke wird ein Datensatz erstellt, der der Reisevorlage zugeordnet ist, die zum Zeitpunkt der Erstellung des Versandbehälters ausgewählt wurde. Datensätze werden auch erstellt, wenn der Versandcontainer über eine Datenentität erstellt wird.

Informationen über den Fortschritt eines im Transit befindlichen Versandcontainers werden oft von einer externen Quelle erhalten. Die Entität für Containeraktivitäten ermöglicht es einer externen Quelle wie einem Spediteur, den Datensatz direkt zu aktualisieren. Daher ist keine manuelle Aktualisierung der Daten erforderlich.

## <a name="container-activities-itmcontaineractivityentity"></a>Containeraktivitäten (ITMContainerActivityEntity)

Sie können die Containeraktivitäten-Entität (`ITMContainerActivityEntity`) verwenden, um zusätzliche Aktivitätsdatensätze zu erstellen. Alternativ kann ein Spediteur Aktualisierungen für einen bestätigten **Tatsächliches Enddatum**-Wert weitergeben.

| Name | Zuordnung | Datentyp | Schlüssel | Obligatorisch |
|---|---|---|---|---|
| Tatsächliches Abschlussdatum | ITMContainerActivityTable.ActualEndDate | Datetime | Nein | Nein |
| Lieferart | ITMContainerActivityTable.DlvModeId | Nvarchar(10) | Nein | Nein |
| Geschätztes Enddatum | ITMContainerActivityTable.EsimatedDate | Datetime | Nein | Nein |
| Positionsnummer | ITMContainerActivityTable.LineNum | Numeric(32, 16) | **Ja** | Nein |
| Notizen | ITMContainerActivityTable.Notes | nvarchar(MAX) | Nein | Nein |
| Aktivität | ITMContainerActivityTable.ShipActivityId | Nvarchar(10) | Nein | **Ja** |
| Versandcontainer | ITMContainerActivityTable.ShipContainerId | Nvarchar(20) | **Ja** | **Ja** |
| Seereise | ITMContainerActivityTable.ShipId | Nvarchar(20) | **Ja** | **Ja** |
| Teilstrecke | ITMContainerActivityTable.ShipLegId | Nvarchar(20) | Nein | **Ja** |
| Dienstanbieter | ITMContainerActivityTable.ShipServiceProvider | Nvarchar(20) | Nein | Nein |
| Temperatur | ITMContainerActivityTable.ShipTemperature | Numeric(32, 6) | Nein | Nein |
| Schiff | ITMContainerActivityTable.ShipVesselId | Nvarchar(20) | Nein | Nein |
| Startdatum | ITMContainerActivityTable.StartDate | Datetime | Nein | Nein |

## <a name="tracking-control"></a>Nachverfolgungssteuerung

Das Steuerungscenter für Nachverfolgung ermöglicht, dass eine Aktualisierung eines bestimmten Quellfeldes durch eine Aktualisierung eines bestimmten Zielfeldes ausgelöst wird. Wenn sowohl der Wert des Quellfelds als auch der Wert des Zielfelds mithilfe der Containeraktivitätsentität aktualisiert werden, zeigt das Zielfeld den Entitätswert an. Dieses Verhalten bezieht sich auf die Nachverfolgung von Kontrolldatensätzen, die über einen **Typ erstellen**-Wert von *Vorlaufzeit* verfügen.

Für Kostenbereiche die einen **Typ erstellen**-Wert von *Status-Update* oder *Leer* (was ein benutzerdefinierter Wert ist) haben, aktualisiert das System den Seereisestatus oder das Zielfeld gemäß der Steuerungskonfiguration für die Nachverfolgung.

## <a name="calculated-fields"></a>Berechnete Felder

Die Werte der folgenden Felder in einem Containeraktivitätsdatensatz werden basierend auf den Werten anderer Felder berechnet. Obwohl diese berechneten Felder nicht in der Datenentität enthalten sind, werden sie festgelegt, wenn die Felder, auf denen die Berechnungen basieren, bereitgestellt werden.

- **Geschätzte Tage** = **Geschätztes Enddatum** – **Startdatum**
- **Tatsächliche Tage** = **Tatsächliches Enddatum** – **Startdatum**
