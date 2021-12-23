---
title: Weisen Sie der mobilen Warehouse Management-App Schrittsymbole und -titel zu
description: In diesem Thema wird beschrieben, wie Sie Schrittsymbole und -titel für neue oder angepasste Aufgabenabläufe für die mobile Warehouse Management-App zuweisen.
author: Mirzaab
ms.date: 05/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 6b8d663fa9743fae83654ed9938b4131e0fa08b9
ms.sourcegitcommit: fd6270dc7f49f93a8155d2b827153b13edb7be8a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902190"
---
# <a name="assign-step-icons-and-titles-for-the-warehouse-management-mobile-app"></a>Weisen Sie der mobilen Warehouse Management-App Schrittsymbole und -titel zu

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie Schrittsymbole und Schritttitel für neue oder angepasste Aufgabenabläufe für die mobile Warehouse Management Mobile App zuweisen.

Die folgenden Abbildungen zeigen, wie Schrittsymbole und -titel in der mobilen Warehouse Management-App angezeigt werden.

![Beispiel für ein Schrittsymbol und einen Schritttitel in der mobilen Warehouse Management-App.](media/step-icon-example.png "Beispiel für ein Schrittsymbol und einen Schritttitel in der mobilen Warehouse Management-App")

## <a name="turn-on-this-feature-in-your-system"></a>Diese Funktion in Ihrem System aktivieren

Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden. Admins können die Einstellungen [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) verwenden, um den Status der Funktion zu prüfen und sie einzuschalten. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Module:** *Lagerortverwaltung*
- **Funktionsname:** *Benutzereinstellungen, Symbole und Schritttitel für die neue Lagerort-App*

## <a name="standard-step-ids-classes-and-icons"></a>Standard-Schritt-IDs, Klassen und Symbole

Jeder Schritt in einem Aufgabenfluss wird durch eine Schritt-ID identifiziert, und jede Schritt-ID hat eine entsprechende Schrittklasse. Das Schrittsymbol und der Titel werden in jeder Schrittklasse festgelegt.

### <a name="step-ids-and-step-classes"></a><a name="step-ids-classes"></a>Schritt-IDs und Schrittklassen

In der folgenden Tabelle sind alle derzeit verfügbaren Schritt-IDs und die entsprechende Schrittklasse aufgeführt. Der Steuerungsname des primären Eingabefelds wird als Schritt-ID verwendet.

Ein Beispiel, das zeigt, wie diese Schritt-IDs und Klassen verwendet werden, finden Sie in der Implementierung der `WHSMobileAppStepInfoBuilder.stepId()` Methode im Abschnitt unter [Beispiel: Weisen Sie Schrittsymbole und -titel für einen benutzerdefinierten Ablauf zu](#example) später in diesem Thema.

| Schrittkennung | Schritt Klasse |
|-|-|
| BatchDisposition | WHSMobileAppStepBatchDisposition |
| Spediteur | WHSMobileAppStepCarrier |
| CatchWeight | WHSMobileAppStepCatchWeight |
| CatchWeightQtyOutboundWeight | WHSMobileAppStepCatchWeight |
| CatchWeightTag | WHSMobileAppStepCatchWeightTag |
| CatchWeightTagWeight | WHSMobileAppStepCatchWeightTagWeight |
| ChangeWarehouseSuccess | WHSMobileAppStepChangeWarehouseSuccess |
| CheckDigit | WHSMobileAppStepCheckDigit |
| ClusterId | WHSMobileAppStepClusterId |
| ClusterPickQtyVerification | WHSMobileAppStepQtyVerification |
| ClusterPosition | WHSMobileAppStepClusterPosition |
| ConfigId | WHSMobileAppStepConfigId |
| Bestätigung | WHSMobileAppStepConfirmation |
| ConsolidateFromLicensePlateId | WHSMobileAppStepConsolidateFromLicensePlateId |
| ConsolidateLPConfirmation | WHSMobileAppStepConsolidateLPConfirmation |
| ConsolidateToLicensePlateId | WHSMobileAppStepConsolidateToLicensePlateId |
| ContainerType | WHSMobileAppStepContainerType |
| CountingReasonCode | WHSMobileAppStepCountingReasonCode |
| CycleCountingAddLPOrFinish | WHSMobileAppStepCycleCountingAddLPOrFinish |
| CycleCountQty1 | WHSMobileAppStepCycleCountQty |
| CycleCountQty2 | WHSMobileAppStepCycleCountQty |
| CycleCountQty3 | WHSMobileAppStepCycleCountQty |
| CycleCountQty4 | WHSMobileAppStepCycleCountQty |
| Disposition | WHSMobileAppStepDisposition |
| DriverCheckInConfirmation | WHSMobileAppStepDriverCheckInConfirmation |
| DriverCheckInId | WHSMobileAppStepDriverCheckInId |
| DriverCheckOutConfirmation | WHSMobileAppStepDriverCheckOutConfirmation |
| DriverCheckOutId | WHSMobileAppStepDriverCheckOutId |
| Ablaufdatum | WHSMobileAppStepExpDate |
| FromBatchDisposition | WHSMobileAppStepFromBatchDisposition |
| FromInventoryStatus | WHSMobileAppStepInventoryStatusFrom |
| Volle Menge | WHSMobileAppStepFullQty |
| InboundPut | WHSMobileAppStepInboundPut |
| InventBatchId | WHSMobileAppStepBatch |
| InventColorId | WHSMobileAppStepInventColorId |
| InventLocation | WHSMobileAppStepInventLocation |
| InventLocationId | WHSMobileAppStepWarehouse |
| InventSerialId | WHSMobileAppStepInventSerialId |
| InventSizeId | WHSMobileAppStepInventSizeId |
| InventStatusId | WHSMobileAppStepInventStatus |
| InventStyleId | WHSMobileAppStepInventStyleId |
| InventVersionId | WHSMobileAppStepInventVersionId |
| ItemId | WHSMobileAppStepItem |
| ITMContainerID | ITMMobileAppStepContainerId |
| ITMShipmentID | ITMMobileAppStepShipmentId |
| KanbanCardId | WHSMobileAppStepKanbanCard |
| KanbanCardToEmpty | WHSMobileAppStepKanbanCardToEmpty |
| KanbanOrCardId | WHSMobileAppStepKanbanCard |
| LicensePlateId | WHSMobileAppStepLicensePlate |
| LoadId | WHSMobileAppStepLoadId |
| LocationLicensePlatePosition | WHSMobileAppStepLocationLicensePlatePosition |
| LocOrLP | WHSMobileAppStepLocOrLP |
| LocOrLP_From | WHSMobileAppStepLocOrLPFrom |
| LocOrLP_To | WHSMobileAppStepLocOrLPTo |
| LocOrLPCheck | WHSMobileAppStepLocOrLPCheck |
| LocVerification | WHSMobileAppStepLocVerification |
| LPAdjustIn | WHSMobileAppStepLPAdjustIn |
| LPBreakChildLP | WHSMobileAppStepLPBreakChildLP |
| LPBreakParentLP | WHSMobileAppStepLPBreakParentLP |
| LPBuildChildLP | WHSMobileAppStepLPBuildChildLP |
| LPBuildParentLP | WHSMobileAppStepLPBuildParentLP |
| LPVerification | WHSMobileAppStepLPVerification |
| MergeContainerId | WHSMobileAppStepMergeContainerId |
| MixedLPLineNum | WHSMobileAppStepMixedLPLineNum |
| MobileDeviceQueueMessageCollectionIdentifierId | WHSMobileAppStepSelectOrder |
| MovementConfirmCancel | WHSMobileAppStepMovementConfirmCancel |
| NewCaptureWeight | WHSMobileAppStepCatchWeight |
| Neuheit | WHSMobileAppStepNewQty |
| OutboundCatchWeightTag | WHSMobileAppStepCatchWeightTag |
| OutboundPut | WHSMobileAppStepOutboundPut |
| OutboundWeight | WHSMobileAppStepCatchWeight |
| OverridePutNewLocation | WHSMobileAppStepOverridePutNewLocation |
| PieceByPieceConfirmation | WHSMobileAppStepQtyVerification |
| POLineNum | WHSMobileAppStepPOLineNum |
| Bestellnummer | WHSMobileAppStepPONum |
| PositionFull | WHSMobileAppStepPositionFull |
| PositionFullQty | WHSMobileAppStepPositionFullQty |
| Konzentration | WHSMobileAppStepPotency |
| PrinterName | WHSMobileAppStepPrinterName |
| ProdId | WHSMobileAppStepProdId |
| ProdLastPalletConfirmation | WHSMobileAppStepProdLastPalletConfirmation |
| ProductConfirmation | WHSMobileAppStepProductConfirmation |
| ProductionScrapConfirmation | WHSMobileAppStepProductionScrapConfirmation |
| Einlagern | WHSMobileAppStepPut |
| PutawayClusterId | WHSMobileAppStepPutawayClusterId |
| Mge | WHSMobileAppStepQty |
| QtyAdjust | WHSMobileAppStepQtyAdjust |
| QtyShort | WHSMobileAppStepQtyShort |
| QtyToConsume | WHSMobileAppStepQtyToConsume |
| QtyToPick | WHSMobileAppStepQtyToPick |
| QtyToPut | WHSMobileAppStepQtyToPut |
| QtyToScrap | WHSMobileAppStepQtyToScrap |
| QtyVerification | WHSMobileAppStepQtyVerification |
| QtyWithScanningLimit | WHSMobileAppStepQtyAdjust |
| ReasonString | WHSMobileAppStepReasonString |
| RecvLocationId | WHSMobileAppStepRecvLocationId |
| RemoveContainerId | WHSMobileAppStepRemoveContainerId |
| ReprintLabelConfirmation | WHSMobileAppStepReprintLabelConfirmation |
| RMANum | WHSMobileAppStepRMANum |
| ShortPickReason | WHSMobileAppStepShortPickReason |
| SortConOrLP | WHSMobileAppStepSortConOrLP |
| SortLicensePlateId | WHSMobileAppStepSortLicensePlateId |
| SortPositionId | WHSMobileAppStepSortPositionId |
| SortVerification | WHSMobileAppStepSortVerification |
| StartLocationId | WHSMobileAppStepStartLocationId |
| StartProdOrderConfirmation | WHSMobileAppStepStartProdOrderConfirmation |
| TargetLicensePlateId | WHSMobileAppStepTargetLicensePlateId |
| TOLineNum | WHSMobileAppStepTOLineNum |
| ToLocation | WHSMobileAppStepToLocation |
| TONum | WHSMobileAppStepTONum |
| ToWarehouse | WHSMobileAppStepWarehouseTo |
| TransportLoadId | WHSMobileAppStepTransportLoadId |
| WaveLabelId | WHSMobileAppStepWaveLabelId |
| WaveLblQty | WHSMobileAppStepWaveLblQty |
| Gewicht | WHSMobileAppStepWeight |
| WeightToConsume | WHSMobileAppStepWeightToConsume |
| WHSAdjustmentType | WHSMobileAppStepWHSAdjustmentType |
| WHSReceivingException | WHSMobileAppStepWHSReceivingException |
| WHSWorkException | WHSMobileAppStepWHSWorkException |
| WHSWorkLicensePlateId | WHSMobileAppStepWorkLicensePlateId |
| WMSLocationId | WHSMobileAppStepLocation |
| WorkId | WHSMobileAppStepWorkId |
| WorkIdToCancel | WHSMobileAppStepWorkIdToCancel |
| WorkLPIdPutawayCluster | WHSMobileAppStepWorkLPIdPutawayCluster |
| WorkPoolId | WHSMobileAppStepWorkPoolId |
| ZoneId | WHSMobileAppStepZoneId |

### <a name="available-step-icons"></a><a name="step-icons"></a>Verfügbare Schrittsymbole

Das System enthält eine Sammlung von Standardschrittsymbolen, die Sie auch für Ihre benutzerdefinierten Schritte verwenden können. Sie können derzeit keine benutzerdefinierten Schrittsymbole hochladen. Daher müssen Sie immer eines der Standardschrittsymbole auswählen.

Die folgende Tabelle zeigt alle derzeit verfügbaren Standardschrittsymbole und ihren Namen.

<table>
<tbody>
<tr>
<td><img src="media/step-icons-about.png" alt="About step icon" title="Über das Schrittsymbol"><br>Info</td>
<td><img src="media/step-icons-add-lp.png" alt="Add license plate or item step icon" title="Fügen Sie ein Nummernschild- oder Artikelschritt-Symbol hinzu"><br>AddLpOrItem</td>
<td><img src="media/step-icons-batch-disposition.png" alt="Batch disposition step icon" title="Chargendispositions-Schrittsymbol"><br>BatchDisposition</td>
<td><img src="media/step-icons-carrier.png" alt="Carrier step icon" title="Symbol für den Schritt Träger"><br>Spediteur</td>
</tr>
<tr>
<td><img src="media/step-icons-cw-tag.png" alt="Catch weight tag step icon" title="Artikelgewicht Tag-Schrittsymbol"><br>CatchWeightTag</td>
<td><img src="media/step-icons-cw-tag-weight.png" alt="Catch weight tag weight step icon" title="Artikelgewicht Tag-Gewichtschrittsymbol"><br>CatchWeightTagWeight</td>
<td><img src="media/step-icons-check-digit.png" alt="Check digit step icon" title="Symbol für den Schritt Ziffernschritt überprüfen"><br>CheckDigit</td>
<td><img src="media/step-icons-check-in-out.png" alt="Check in or out ID step icon" title="ID-Schritt-Symbol ein- oder auschecken"><br>CheckInOutId</td>
</tr>
<tr>
<td><img src="media/step-icons-child-lp.png" alt="Child license plate step icon" title="Symbol für den Schritt für untergeordnetes Kennzeichen"><br>ChildLP</td>
<td><img src="media/step-icons-cluster-id.png" alt="Cluster ID step icon" title="Symbol für den Schritt für die Cluster-ID"><br>ClusterId</td>
<td><img src="media/step-icons-cluster-position.png" alt="Cluster position step icon" title="Symbol für den Schritt für die Cluster-Position"><br>ClusterPosition</td>
<td><img src="media/step-icons-config-id.png" alt="Config ID step icon" title="Symbol für den Schritt für die Config-ID"><br>ConfigId</td>
</tr>
<tr>
<td><img src="media/step-icons-configured-field.png" alt="Configured field step icon" title="Symbol für den Schritt Feld konfigurieren"><br>ConfiguredField</td>
<td><img src="media/step-icons-con-lp.png" alt="Con or LP step icon" title="Con- oder LP-Schrittsymbol"><br>ConOrLP</td>
<td><img src="media/step-icons-consolidate-from-LP.png" alt="Consolidate from license plate ID step icon" title="Konsolidieren Sie vom Kennzeichen-ID-Schrittsymbol"><br>ConsolidateFromLicensePlateID</td>
<td><img src="media/step-icons-consolidate-to-LP.png" alt="Consolidate to license plate ID step icon" title="Konsolidieren Sie zum Kennzeichen-ID-Schrittsymbol"><br>ConsolidateToLicensePlateID</td>
</tr>
<tr>
<td><img src="media/step-icons-container-type.png" alt="Container type step icon" title="Schritttyp-Symbol für den Containertyp"><br>ContainerType</td>
<td><img src="media/step-icons-counting.png" alt="Counting step icon" title="Symbol für den Schritt Zählen"><br>Inventur</td>
<td><img src="media/step-icons-counting-reason.png" alt="Counting reason code step icon" title="Zählgrundsymbol Schritt Symbol"><br>CountingReasonCode</td>
<td><img src="media/step-icons-country-origin.png" alt="Country of origin code step icon" title="Symbol für den Schritt für Herkunftslandcode"><br>CountryOfOrigin</td>
</tr>
<tr>
<td><img src="media/step-icons-disposition.png" alt="Disposition step icon" title="Dispositions-Schrittsymbol"><br>Disposition</td>
<td><img src="media/step-icons-done.png" alt="Done step icon" title="Fertig Schritt Symbol"><br>Fertig</td>
<td><img src="media/step-icons-driver-check-in-confirmation.png" alt="Driver check in confirmation step icon" title="Symbol für Bestätigungsschritt zum Einckecken des Fahrers"><br>DriverCheckInConfirmation</td>
<td><img src="media/step-icons-driver-check-in-id.png" alt="Driver check in ID step icon" title="Symbol für den Schritt für das Einchecken der Fahrer-ID"><br>DriverCheckInId</td>
</tr>
<tr>
<td><img src="media/step-icons-driver-check-out-id.png" alt="Driver check out ID step icon" title="Symbol für den Schritt für das Auschecken der Fahrer-ID"><br>DriverCheckOutId</td>
<td><img src="media/step-icons-exp-date.png" alt="Expiration date step icon" title="Ablaufdatum Schritt Symbol"><br>Ablaufdatum</td>
<td><img src="media/step-icons-field.png" alt="Field step icon" title="Symbol für den Schritt für das Feld"><br>Feld</td>
<td><img src="media/step-icons-from-batch.png" alt="From batch disposition step icon" title="Von Chargendispositions-Schrittsymbol"><br>FromBatchDisposition</td>
</tr>
<tr>
<td><img src="media/step-icons-from-inventory-status.png" alt="From inventory status step icon" title="Vom Inventarsstatus-Schrittsymbol"><br>FromInventoryStatus</td>
<td><img src="media/step-icons-id-attribute.png" alt="ID attribute step icon" title="Symbol für den Schritt für ID-Attribut"><br>IdAttribute</td>
<td><img src="media/step-icons-invent-batch-id.png" alt="Inventory batch ID step icon" title="Symbol für den Schritt für Inventar-Batch-ID"><br>InventBatchID</td>
<td><img src="media/step-icons-invent-color-id.png" alt="Inventory color ID step icon" title="Symbol für den Schritt für die Lagerfarb-ID"><br>InventColorID</td>
</tr>
<tr>
<td><img src="media/step-icons-invent-location.png" alt="Inventory location step icon" title="Schritt-Symbol für Lagerstandort"><br>InventLocation</td>
<td><img src="media/step-icons-invent-serial-id.png" alt="Inventory serial ID step icon" title="Symbol für den Schritt für Lager-Serien-ID"><br>InventSerialID</td>
<td><img src="media/step-icons-invent-size-id.png" alt="Inventory size ID step icon" title="Symbol für den Schritt für Lagergröße"><br>InventSizeID</td>
<td><img src="media/step-icons-invent-status-id.png" alt="Inventory status ID step icon" title="Symbol für den Schritt für die Lagerstatus-ID"><br>InventStatusID</td>
</tr>
<tr>
<td><img src="media/step-icons-invent-style-id.png" alt="Inventory style ID step icon" title="Symbol für den Schritt für Lagerstil-ID"><br>InventStyleID</td>
<td><img src="media/step-icons-invent-version-id.png" alt="Inventory version ID step icon" title="Inventarsversion ID_Schrittsymbol"><br>InventVersionID</td>
<td><img src="media/step-icons-item-id.png" alt="Item ID step icon" title="Symbol für den Schritt für die Artikel-ID"><br>ItemID</td>
<td><img src="media/step-icons-itm-contianer-id.png" alt="ITM container ID step icon" title="Schritttyp-Symbol für den ITM-Containertyp"><br>ITMContainerID</td>
</tr>
<tr>
<td><img src="media/step-icons-itm-shipment-id.png" alt="ITM shipment ID step icon" title="Symbol für den Schritt für ITM-Lieferung"><br>ITMShipmentID</td>
<td><img src="media/step-icons-kanban-card-id.png" alt="Kanban card ID step icon" title="Kanban-Karten-ID-Schrittsymbol"><br>KanbanCardID</td>
<td><img src="media/step-icons-kanban-or-card-id.png" alt="Kanban or card ID step icon" title="Kanban oder Karten-ID-Schrittsymbol"><br>KanbanOrCardID</td>
<td><img src="media/step-icons-license-plate-id.png" alt="License plate ID step icon" title="Symbol für den Schritt für Lizenz-Kennzeichen"><br>LicensePlateID</td>
</tr>
<tr>
<td><img src="media/step-icons-load-id.png" alt="Load ID step icon" title="Symbol für den Schritt für die Lade-ID"><br>LoadId</td>
<td><img src="media/step-icons-location-lp-pos.png" alt="Location license plate position step icon" title="Schritt-ID für die Standortkennzeichenpositionierung"><br>LocationLicensePlatePosition</td>
<td><img src="media/step-icons-location-or-lp.png" alt="Location or license plate step icon" title="Symbol für den Schritt für Standort oder Lizenzkennzeichen"><br>LocOrLP</td>
<td><img src="media/step-icons-location-or-lp-check.png" alt="Location or license plate check step icon" title="Standort oder Lizenzschild-Kontrollschritt-Symbol"><br>LocOrLPCheck</td>
</tr>
<tr>
<td><img src="media/step-icons-location-or-lp-from.png" alt="Location or license plate from step icon" title="Symbol für den Schritt von Standort oder Lizenzkennzeichen"><br>LocOrLPFrom</td>
<td><img src="media/step-icons-location-or-lp-to.png" alt="Location or license plate to step icon" title="Symbol für den Schritt für zu Standort oder Lizenzkennzeichen"><br>LocOrLPTo</td>
<td><img src="media/step-icons-long-process-complete.png" alt="Long process completed step icon" title="Symbol für den Schritt Langer Prozess abgeschlossen"><br>LongProcessCompleted</td>
<td><img src="media/step-icons-lp-break-parent.png" alt="LP break parent LP step icon" title="LP-Pause übergeordnetes LP-Schrittsymbol"><br>LPBreakParentLP</td>
</tr>
<tr>
<td><img src="media/step-icons-merge-container.png" alt="Merge container ID step icon" title="Schritttyp-Symbol für das Zusammenführen der Container-ID"><br>MergeContainerId</td>
<td><img src="media/step-icons-mixed-lp-line.png" alt="Mixed license plate line number step icon" title="Symbol für den Schritt für gemischte Lizenzkennzeichen-Zeilenzahlen"><br>MixedLPLineNum</td>
<td><img src="media/step-icons-outbound-weight.png" alt="Outbound weight step icon" title="Symbol für den Schritt des ausgehenden Gewichts"><br>OutboundWeight</td>
<td><img src="media/step-icons-owner.png" alt="Owner step icon" title="Schritt Symbol für Besitzer"><br>Eigentümer</td>
</tr>
<tr>
<td><img src="media/step-icons-parent-lp.png" alt="Parent license plate step icon" title="Symbol für den Schritt für übergeordnetes Kennzeichen"><br>ParentLP</td>
<td><img src="media/step-icons-please-confirm.png" alt="Please confirm step icon" title="Bitte bestätigen Sie das Schrittsymbol"><br>Bitte bestätigen</td>
<td><img src="media/step-icons-po-line-num.png" alt="Purchase order line number step icon" title="Symbol für den Schrittd für die Zeilenzahl der Bestellung"><br>POLineNum</td>
<td><img src="media/step-icons-po-num.png" alt="Purchase order number step icon" title="Symbol für den Schrittd für die Zeilenzahl der Bestellungszahl"><br>Bestellnummer</td>
</tr>
<tr>
<td><img src="media/step-icons-position-full.png" alt="Position full step icon" title="Symbol für den Schritt für die vollständige Position"><br>PositionFull</td>
<td><img src="media/step-icons-potency.png" alt="Potency step icon" title="Symbol für den Schritt für die Stärke"><br>Konzentration</td>
<td><img src="media/step-icons-printer-name.png" alt="Printer name step icon" title="Symbol für den Schritt für den Druckernamen"><br>PrinterName</td>
<td><img src="media/step-icons-prod-id.png" alt="Prod ID step icon" title="Symbol für den Schritt für die Produktions-ID"><br>ProdId</td>
</tr>
<tr>
<td><img src="media/step-icons-product-confirm.png" alt="Product confirmation step icon" title="Symbol für den Produktbestätigungsschritt"><br>ProductConfirmation</td>
<td><img src="media/step-icons-put.png" alt="Put step icon" title="Symbol für den Positionierungsschritt"><br>Einlagern</td>
<td><img src="media/step-icons-putaway-cluster-id.png" alt="Putaway cluster ID step icon" title="Symbol für den Schritt Clustereinlagerungs-ID"><br>PutawayClusterId</td>
<td><img src="media/step-icons-qty.png" alt="Quantity step icon" title="Symbol für Mengenschritt"><br>Mge</td>
</tr>
<tr>
<td><img src="media/step-icons-qty-adjust-in.png" alt="Quantity adjust in step icon" title="Symbold für Mengenanpassungsschritt"><br>QtyAdjustIn</td>
<td><img src="media/step-icons-qty-short.png" alt="Quantity short step icon" title="Symbol für Kurz-Mengenschritt"><br>QtyShort</td>
<td><img src="media/step-icons-qty-to-consume.png" alt="Quantity to consume step icon" title="Symbol zu Mengen für Verbraucherschritt"><br>QtyToConsume</td>
<td><img src="media/step-icons-qty-to-put.png" alt="Quantity to put step icon" title="Symbol zu Mengen für Einlagerungsschritt"><br>QtyToPut</td>
</tr>
<tr>
<td><img src="media/step-icons-qty-to-scrap.png" alt="Quantity to scrap step icon" title="Symbol zu Mengen für Verschrottungsschritt"><br>QtyToScrap</td>
<td><img src="media/step-icons-qty-confirmation.png" alt="Quantity confirmation step icon" title="Symbol für den Mengenbestätigungsschritt"><br>Mengenbestätigung</td>
<td><img src="media/step-icons-raf-end-job.png" alt="Report as finished end job step icon" title="Als fertiges Endschritt-Symbol melden"><br>RAFEndJob</td>
<td><img src="media/step-icons-recv-loc-id.png" alt="Receive location ID step icon" title="Symbol für den Schritt für Standort-Empfangs-ID"><br>RecvLocationID</td>
</tr>
<tr>
<td><img src="media/step-icons-remove-container-id.png" alt="Remove container ID step icon" title="Schritttyp-Symbol für das Entfernen der Container-ID"><br>RemoveContainerId</td>
<td><img src="media/step-icons-rma-no.png" alt="RMA number step icon" title="RMA-Nummernschritt-Symbol"><br>RMANum</td>
<td><img src="media/step-icons-select-order.png" alt="Select order step icon" title="Wählen Sie das Bestellschritt-Symbol"><br>SelectOrder</td>
<td><img src="media/step-icons-short-pick-reason.png" alt="Short pick reason step icon" title="Kurzsymbol für Auswahlgrund"><br>ShortPickReason</td>
</tr>
<tr>
<td><img src="media/step-icons-sort-position-id.png" alt="Sort position ID step icon" title="Symbol für den Schritt für Positions-ID sortieren"><br>SortPositionId</td>
<td><img src="media/step-icons-target-lp-id.png" alt="Target license plate ID step icon" title="Symbol für den Schritt für Ziel-Ladungsträger-ID"><br>TargetLicensePlateId</td>
<td><img src="media/step-icons-to-line-no.png" alt="To line number step icon" title="Zum Zeilennummernschrittsymbol"><br>ToLineNum</td>
<td><img src="media/step-icons-to-location.png" alt="To location step icon" title="Zu Schritt-Symbol Standort"><br>ToLocation</td>
</tr>
<tr>
<td><img src="media/step-icons-to-number.png" alt="To number step icon" title="Zu Schrittsymbol Zahl"><br>ToNum</td>
<td><img src="media/step-icons-to-warehouse.png" alt="To warehouse step icon" title="Zu Schritt-Symbol Lagerort"><br>ToWarehouse</td>
<td><img src="media/step-icons-tranport-load-id.png" alt="Transport load ID step icon" title="Symbol für den Schritt für Datentransportauslastungs-ID"><br>TransportLoadId</td>
<td><img src="media/step-icons-vendor-batch-id.png" alt="Vendor batch ID step icon" title="Symbol für den Schritt für Lieferanten-Chargen-ID"><br>VendBatchId</td>
</tr>
<tr>
<td><img src="media/step-icons-wave-label-id.png" alt="Wave label ID step icon" title="Symbol für den Schritt für die Wellenbeschriftungs-ID"><br>WaveLabelId</td>
<td><img src="media/step-icons-wave-label-qty.png" alt="Wave label quantity step icon" title="Symbol für den Schritt für die Wellenbeschriftungsmenge"><br>WaveLblQty</td>
<td><img src="media/step-icons-weight.png" alt="Weight step icon" title="Symbol für den Schritt des Gewichts"><br>Gewicht</td>
<td><img src="media/step-icons-weight-to-consume.png" alt="Weight to consume step icon" title="Symbol für den Schritt für das erforderliche Gewicht"><br>WeightToConsume</td>
</tr>
<tr>
<td><img src="media/step-icons-whs-adjustment-type.png" alt="WHS adjustment type step icon" title="Symbol für den Schritt für den WHS Anpassungstyp"><br>WHSAdjustmentType</td>
<td><img src="media/step-icons-whs-receiving-exception.png" alt="WHS receiving exception step icon" title="Symbol für den Schritt für den Empfang der WHS-Ausnahme"><br>WHSReceivingException</td>
<td><img src="media/step-icons-wms-location-id.png" alt="WMS location ID step icon" title="Symbol für den Schritt für die WMS Standort-ID"><br>WMSLocationID</td>
<td><img src="media/step-icons-work-id.png" alt="Work ID step icon" title="Symbol für den Schritt für die Arbeits-ID"><br>WorkId</td>
</tr>
<tr>
<td><img src="media/step-icons-work-id-to-cancel.png" alt="Work ID to cancel step icon" title="Symbol für den Schritt zum Abbrechen der Arbeits-ID"><br>WorkIdToCancel</td>
<td><img src="media/step-icons-work-lp-id.png" alt="Work license plate ID step icon" title="Symbol für den Schritt für die Arbeits-Kennzeichnungs-ID"><br>WorkLicensePlateId</td>
<td><img src="media/step-icons-work-lp-putaway-cluster.png" alt="Work license plate ID putaway cluster step icon" title="Symbol für den Schritt für die Cluster-Einlagerungs-ID"><br>WorkLPIDPutawayCluster</td>
<td><img src="media/step-icons-work-pool-id.png" alt="Work pool ID step icon" title="Schritt für das Symbol für den Arbeits-Pool"><br>WorkPoolID</td>
</tr>
<tr>
<td><img src="media/step-icons-zone-pool-id.png" alt="Zone ID step icon" title="Symbol für den Schritt für die Zonen-ID"><br>ZoneID</td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## <a name="example-assign-step-icons-and-titles-for-a-custom-flow"></a><a name="example"></a>Beispiel: Weisen Sie Schrittsymbole und -titel für einen benutzerdefinierten Ablauf zu

In diesem Beispiel wird erläutert, wie Sie Schrittsymbole und -titel für einen benutzerdefinierten Aufgabenablauf einrichten. Das Szenario basiert auf einem Beispiel für einen benutzerdefinierten Aufgabenablauf, der im folgenden Blogbeitrag ausführlicher vorgestellt und untersucht wird: [Anpassen der Mobile App Lager](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app). Der Aufgabenfluss funktioniert folgendermaßen:

1. Die App zeigt eine Seite an, auf der der Mitarbeiter aufgefordert wird, eine Container-ID anzugeben (z. B. durch Scannen eines Barcodes).
1. Wenn die Container-ID gültig ist, öffnet die App eine neue Seite, auf der die Arbeitskraft zur Eingabe des Gewichts aufgefordert wird. (Wenn die Container-ID nicht gültig ist, kehrt die Arbeitskraft zur ersten Seite zurück.)
1. Wenn die Arbeitskraft ein gültiges Gewicht eingibt, speichert das System das Gewicht und die Arbeitskraft kehrt zur ersten Seite zurück.

Die folgende Abbildung zeigt diesen Aufgabenfluss.

![Aufgabenflussdiagramm.](media/step-icons-example-task-flow.png "Aufgabenflussdiagramm")

### <a name="create-a-step-class-for-the-container-input-page"></a>Erstellen Sie eine Schrittklasse für die Containereingabeseite

Auf der Containereingabeseite kann der Mitarbeiter eine Container-ID scannen oder eingeben.

![Containereingabeseite.](media/step-icons-example-container-input.png "Containereingabeseite")

Auf der Containereingabeseite lautet der Kontrollname des Eingabefelds `ContainerId`. Weil dieser Kontrollname nicht in der [Liste der Schritt-IDs](#step-ids-classes) enthalten ist, finden Sie keinen vorhandenen Schritt, der darauf basiert. Daher müssen Sie eine Schrittklasse erstellen, die den Schritt darstellt. Hier ist ein Beispiel.

```xpp
[WHSMobileAppStepId('ContainerId')]
final internal class WHSMobileAppStepContainerId extends WHSMobileAppStep
{
    private const WHSMobileAppStepIcon PopulationIcon = 'InventBatchID';
    private const WHSMobileAppStepTitle InputNotFilledTitle = "@WAX:WHSMobileAppStepContainerID_InputNotFilled"; //Scan a container
    protected void initValues()
    {
        defaultStepIcon = PopulationIcon;
        defaultStepTitle = InputNotFilledTitle;
    }
}
```

Die Kennung des Schrittsymbols wird im `defaultStepIcon` Klassenmitglied gespeichert und der Schritttitel wird im `defaultStepTitle` Klassenmitglied gespeichert.

Um ein Schrittsymbol zuzuweisen, setzen Sie `defaultStepIcon` zu einer der Symbol-IDs, die im Abschnitt [Verfügbare Schrittsymbole](#step-icons) weiter oben in diesem Thema aufgeführt sind.

### <a name="use-a-standard-or-custom-step-icon-and-title-for-the-weight-input"></a>Verwenden Sie ein Standard- oder benutzerdefiniertes Schrittsymbol und einen Titel für die Gewichtseingabe

Auf der Seite zur Gewichtseingabe kann der Mitarbeiter ein Gewicht eingeben.

![Gewichtseingabeseite.](media/step-icons-example-weight-input.png "Gewichtseingabeseite")

Auf der Gewichtseingabeseite lautet der Kontrollname des Eingabefelds `Weight`, der in der [Liste der Schritt-IDs](#step-ids-classes) ist. Wenn das Schrittsymbol und der Titel, die in der `WHSMobileAppStepWeight` Klasse definiert sind, akzeptabel sind, müssen Sie für diesen Schritt nichts ändern.

Wenn Sie für diesen Schritt jedoch lieber ein anderes Symbol oder einen anderen Titel verwenden möchten, können Sie entweder die `stepId()` Methode oder die `stepInfo()` Methode in der Builder-Klasse überschreiben. Jeder Aufgabenfluss verfügt über einen eigenen Builder für Schrittinformationen.

#### <a name="override-the-stepid-method"></a>Überschreiben Sie die stepId () -Methode

Das folgende Beispiel zeigt eine Möglichkeit, wie Sie eine Builder-Klasse ändern können, indem Sie die `stepId()` Methode überschreiben.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepId stepId()
    {
        WHSMobileAppStepId stepIdLocal = super();
        if (stepIdLocal == 'Weight')
        {
            return 'NewWeight';
        }
        return stepIdLocal;
    }
}
```

Anschließend erstellen Sie eine Schrittklasse für den `NewWeight` Schritt. Der Code sollte dem Code für das `ContainerId` Beispiel ähneln, das weiter oben in diesem Thema gezeigt wurde.

#### <a name="override-the-stepinfo-method"></a>Überschreiben Sie die stepInfo () -Methode

Das folgende Beispiel zeigt eine Möglichkeit, wie Sie eine Builder-Klasse ändern können, indem Sie die `stepInfo()` Methode überschreiben.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepInfo stepInfo()
    {
        if (stepId != 'Weight')
        {
            return super();
        }
        WHSMobileAppStepInfo stepInfo = WHSMobileAppStepInfo::construct();
        stepInfo.parmStepIcon('NewIcon');
        stepInfo.parmStepTitle('NewTitle');
        return stepInfo;
    }
}
```

Sie konstruieren dann ein `WHSMobileAppStepInfo` Objekt und legen das Symbol und/oder den Titel direkt fest.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Mobile Lagerortsverwaltungs-App installieren und verbinden](install-configure-warehouse-management-app.md)
- [Benutzereinstellungen für mobile Geräte](mobile-device-user-settings.md)
