---
title: Produktdatenentitäten
description: Dieses Thema enthält Informationen zu den verschiedenen Entitäten, die zum Importieren und Exportieren von Produktdaten verwendet werden können.
author: cvocph
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: kamaybac
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2019-12-1
ms.openlocfilehash: cf23284729cd10569ceb320d5fd30f8429974c3d
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344757"
---
# <a name="product-data-entities"></a>Produktdatenentitäten

[!include [banner](../includes/banner.md)]

Sie müssen neue Datenentitäten verwenden, um Produktdaten zu importieren und exportieren. Die folgende Tabelle enthält Details zu den produktbezogenen Dateneinheiten und beschreibt den jeweiligen Zweck.

| Entität | Name der Entwicklungsumgebung (Typ) | Notizen |
|--------|-------------------------------------------|-------|
| Produkte V2 | `EcoResProductV2Entity` | Diese Entität wird zum Importieren und Exportieren gemeinsam genutzter Produkte – eindeutig identifizierbare Produkte und Produktmaster – verwendet. Sie ermöglicht Updates. Sie unterstützt keine satzbasierten SQL-Vorgänge. Sie ist für Open Data Protocol (OData) aktiviert. |
| Freigegebene Produkte V2 | `EcoResReleasedProductV2Entity` | Diese Entität wird zum Importieren und Exportieren freigegebener Produkte – eindeutig identifizierbare Produkte und Produktmaster – verwendet. Sie ermöglicht Updates. Voraussetzung ist, dass das gemeinsam genutzte Produkt bereits erstellt wurde. Wenn ein neues freigegebenes Produkt importiert wird, erfolgt eine Freigabe des freigegebenen Produkts. Es gibt auch separate Entitäten, mit denen freigegebene Produktstämme und freigegebene unterschiedliche Varianten importiert und exportiert werden können. Diese Entität unterstützt keine satzbasierten SQL-oder Löschvorgänge. Sie ist für OData aktiviert. |
| Erstellung eines freigegebenen Produkts V2 | `EcoResReleasedProductCreationV2Entity` | Diese Entität wird verwendet, um gemeinsam genutzte Produkte und freigegebene Produkte in einem Schritt zu importieren. Obwohl sie Exporte unterstützt, wird diese Verwendung nicht empfohlen, da der Zweck der Entität die Produkterstellung ist. Updates werden nicht unterstützt. Sie unterstützt eine begrenzte Anzahl von Feldern (Felder, die im Dialogfeld zur Produkterstellung verfügbar sind). Sie unterstützt keine satzbasierten SQL-Vorgänge. Sie wird nicht durch OData verfügbar gemacht. |
| Produktvarianten | `EcoResProductVariantEntity` | Diese Entität wird zum Importieren und Exportieren freigegebener Produktvarianten verwendet. Sie ermöglicht Updates. Hierfür müssen bereits Dimensionswerte erstellt werden. Der Integrationsschlüssel ist der Produktmaster plus Produktdimensionen. Diese Entität unterstützt keine satzbasierten SQL-Vorgänge. Sie ist für OData aktiviert. Sie unterstützt Löschvorgänge. Sie kann nicht durch Hinzufügen neuer Produktdimensionen erweitert werden. |
| Produktvarianten nach Produktnummer | `EcoResProductNumberIdentifiedProductVariantEntity` | Diese Entität wird zum Importieren und Exportieren freigegebener Produktvarianten verwendet. Sie ermöglicht Updates. Hierfür müssen bereits Dimensionswerte erstellt werden. Der Integrationsschlüssel ist die Produktnummer (während der Integrationsschlüssel für die Entität **Produktvarianten** der Produktmaster plus Produktdimensionen ist). |
| Freigegebene Produktvarianten | `EcoResReleasedProductVariantEntity` | Diese Entität wird zum Importieren und Exportieren freigegebener Produktvarianten verwendet. Sie ermöglicht Updates. Voraussetzung ist, dass die gemeinsam genutzten Produktvarianten bereits erstellt wurde. Wenn eine neue freigegebene Produktvariante importiert wird, erfolgt eine Freigabe der Produktvariante. Diese Entität unterstützt keine satzbasierten SQL-Vorgänge. Sie ist für OData aktiviert. Obwohl sie Löschvorgänge unterstützt, führt diese Verwendung aufgrund eines Fehlers auf der aktuellen Plattform zur Beschädigung von Daten. Diese Entität kann nicht durch Hinzufügen neuer Produktdimensionen erweitert werden. |
| Freigegebene Produktvarianten nach Produktnummer | `EcoResProductNumberIdentifiedReleasedProductVariantEntity` | Diese Entität ähnelt der Entität **Freigegebene Produktvarianten**, aber der Integrationsschlüssel ist die Produktnummer und nicht der Produktmaster plus Produktdimensionen. Sie kann nicht durch Hinzufügen neuer Produktdimensionen erweitert werden. |
| Freigegebene Produkte für Verkauf | `EcoResSellableReleasedProductEntity` | Diese Einheit wird verwendet, um nur verkäufliche Produkte zu exportieren. Verkäufliche Produkte sind Produkte, die die Informationen enthalten, die diese benötigen, damit sie in Aufträgen verwendet werden können. Die gleichen Regeln gelten, wenn ein Produkt mit der Funktion **Überprüfen** auf der Seite **Freigegebene Produkte** überprüft wird. |
| Freigegebene eindeutig identifizierbare Produkte V2 | `EcoResDistinctProductV2Entity` | Diese Entität wird verwendet, um eindeutig identifizierbare Produkte zu exportieren. Diese eindeutig identifizierbaren Produkte können Produkte, Produktuntertypprodukte und alle Produktvarianten sein. |
| Freigegebene Produktmaster V2 | `EcoResProductMasterV2Entity` | Diese Entität wird zum Importieren und Exportieren von Produktmaster verwendet. Sie ist nicht für die Datenverwaltung aktiviert. |
| Element - Barcode | `EcoResProductBarcodeEntityV3` | Diese Entität wird verwendet, um Produkte und Barcodes zu exportieren. Diese Entität erlaubt keine Änderungsverfolgung, keine Aktualisierungen und keine Löschungen. Um die Änderungsverfolgung, Aktualisierungen oder Löschungen von Strichcodes zu verwenden, verwenden Sie die Entität **Artikel - Strichcode-Zuordnung**. |
| Artikel-Strichcode-Zuordnung | `EcoResProductBarcodeAssociationEntity` | Diese Entität wird verwendet, um Produkte und Barcodes zu exportieren. Sie erlaubt Änderungsverfolgung, Aktualisierungen und Löschungen. Um die Entität zu verwenden, muss die Funktion *Element - Barcode-Verbesserungen* in [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aktiviert sein. Ihr Entitätsschlüssel ist `AssociationID`, der die Assoziation zwischen dem Barcode und dem Produkt erstellt. Um diesen Schlüssel zu unterstützen, wird die Tabelle `InventitemBarcodeAssociation` für vorhandene Element-Strichcode-Daten aufgefüllt, wenn Sie die Funktion einschalten. Die Tabelle wird mit Hilfe eines Batch-Auftrags aufgefüllt und wenn Ihre Barcode-Tabelle eine große Anzahl von Datensätzen hat, kann das Ausführen des Batch-Auftrags viel Zeit in Anspruch nehmen. Daher empfehlen wir Ihnen, die Aktivierung der Funktion (und damit die Ausführung des Batch-Jobs) zu einem Zeitpunkt zu planen, der in Ihren Geschäftsplan passt. |
| Produktlebenszyklusstatus | `EcoResProductLifecycleSateEntity` | Diese Entität wird zum Importieren und Exportieren der verschiedenen Produktlebenszykluszustände verwendet, die einem Produkt zugewiesen werden können. |

> [!NOTE]
> Sie können die Datenentität **Freigegebene Produkte V2** verwenden, um Produkte nur dann in das System zu importieren, wenn das freigegebene Produkt bereits erstellt wurde. Andernfalls müssen Sie zum Importieren von Produkten in das System die Datenentität **Produkterstellung** verwenden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]