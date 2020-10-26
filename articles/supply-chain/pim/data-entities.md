---
title: Produktdatenentitäten
description: Dieses Thema enthält Informationen zu den verschiedenen Entitäten, die zum Importieren und Exportieren von Produktdaten verwendet werden können.
author: cvocph
manager: tfehr
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: kamaybac
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2019-12-1
ms.openlocfilehash: 536e17088348f2a8b41818eccbe8da699c4189d5
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3981840"
---
# <a name="product-data-entities"></a>Produktdatenentitäten

[!include [banner](../includes/banner.md)]

Sie müssen neue Datenentitäten verwenden, um Produktdaten zu importieren und exportieren. Die folgende Tabelle enthält Details zu den produktbezogenen Dateneinheiten und beschreibt den jeweiligen Zweck.

| Entität | Name der Entwicklungsumgebung (Typ) | Notizen |
|--------|-------------------------------------------|-------|
| Produkte V2 | EcoResProductV2Entity | Diese Entität wird zum Importieren und Exportieren gemeinsam genutzter Produkte – eindeutig identifizierbare Produkte und Produktmaster – verwendet. Sie ermöglicht Updates. Sie unterstützt keine satzbasierten SQL-Vorgänge. Sie ist für Open Data Protocol (OData) aktiviert. |
| Freigegebene Produkte V2 | EcoResReleasedProductV2Entity | Diese Entität wird zum Importieren und Exportieren freigegebener Produkte – eindeutig identifizierbare Produkte und Produktmaster – verwendet. Sie ermöglicht Updates. Voraussetzung ist, dass das gemeinsam genutzte Produkt bereits erstellt wurde. Wenn ein neues freigegebenes Produkt importiert wird, erfolgt eine Freigabe des freigegebenen Produkts. Es gibt auch separate Entitäten, mit denen freigegebene Produktstämme und freigegebene unterschiedliche Varianten importiert und exportiert werden können. Diese Entität unterstützt keine satzbasierten SQL-oder Löschvorgänge. Sie ist für OData aktiviert. |
| Erstellung eines freigegebenen Produkts V2 | EcoResReleasedProductCreationV2Entity | Diese Entität wird verwendet, um gemeinsam genutzte Produkte und freigegebene Produkte in einem Schritt zu importieren. Obwohl sie Exporte unterstützt, wird diese Verwendung nicht empfohlen, da der Zweck der Entität die Produkterstellung ist. Updates werden nicht unterstützt. Sie unterstützt eine begrenzte Anzahl von Feldern (Felder, die im Dialogfeld zur Produkterstellung verfügbar sind). Sie unterstützt keine satzbasierten SQL-Vorgänge. Sie wird nicht durch OData verfügbar gemacht. |
| Produktvarianten | EcoResProductVariantEntity | Diese Entität wird zum Importieren und Exportieren freigegebener Produktvarianten verwendet. Sie ermöglicht Updates. Hierfür müssen bereits Dimensionswerte erstellt werden. Der Integrationsschlüssel ist der Produktmaster plus Produktdimensionen. Diese Entität unterstützt keine satzbasierten SQL-Vorgänge. Sie ist für OData aktiviert. Sie unterstützt Löschvorgänge. Sie kann nicht durch Hinzufügen neuer Produktdimensionen erweitert werden. |
| Produktvarianten nach Produktnummer | EcoResProductNumberIdentifiedProductVariantEntity | Diese Entität wird zum Importieren und Exportieren freigegebener Produktvarianten verwendet. Sie ermöglicht Updates. Hierfür müssen bereits Dimensionswerte erstellt werden. Der Integrationsschlüssel ist die Produktnummer (während der Integrationsschlüssel für die Entität **Produktvarianten** der Produktmaster plus Produktdimensionen ist). |
| Freigegebene Produktvarianten | EcoResReleasedProductVariantEntity | Diese Entität wird zum Importieren und Exportieren freigegebener Produktvarianten verwendet. Sie ermöglicht Updates. Voraussetzung ist, dass die gemeinsam genutzten Produktvarianten bereits erstellt wurde. Wenn eine neue freigegebene Produktvariante importiert wird, erfolgt eine Freigabe der Produktvariante. Diese Entität unterstützt keine satzbasierten SQL-Vorgänge. Sie ist für OData aktiviert. Obwohl sie Löschvorgänge unterstützt, führt diese Verwendung aufgrund eines Fehlers auf der aktuellen Plattform zur Beschädigung von Daten. Diese Entität kann nicht durch Hinzufügen neuer Produktdimensionen erweitert werden. |
| Freigegebene Produktvarianten nach Produktnummer | EcoResProductNumberIdentifiedReleasedProductVariantEntity | Diese Entität ähnelt der Entität **Freigegebene Produktvarianten**, aber der Integrationsschlüssel ist die Produktnummer und nicht der Produktmaster plus Produktdimensionen. Sie kann nicht durch Hinzufügen neuer Produktdimensionen erweitert werden. |
| Freigegebene Produkte für Verkauf | EcoResSellableReleasedProductEntity | Diese Einheit wird verwendet, um nur verkäufliche Produkte zu exportieren. Verkäufliche Produkte sind Produkte, die die Informationen enthalten, die diese benötigen, damit sie in Aufträgen verwendet werden können. Die gleichen Regeln gelten, wenn ein Produkt mit der Funktion **Überprüfen** auf der Seite **Freigegebene Produkte** überprüft wird. |
| Freigegebene eindeutig identifizierbare Produkte V2 | EcoResDistinctProductV2Entity | Diese Entität wird verwendet, um eindeutig identifizierbare Produkte zu exportieren. Diese eindeutig identifizierbaren Produkte können Produkte, Produktuntertypprodukte und alle Produktvarianten sein. |
| Freigegebene Produktmaster V2 | EcoResProductMasterV2Entity | Diese Entität wird zum Importieren und Exportieren von Produktmaster verwendet. Sie ist nicht für die Datenverwaltung aktiviert. |
| Artikel - Strichcode | EcoResProductBarcodeEntity | Diese Entität wird verwendet, um Produkte und Barcodes zu exportieren. |
| Produktlebenszyklusstatus | EcoResProductLifecycleSateEntity | Diese Entität wird zum Importieren und Exportieren der verschiedenen Produktlebenszykluszustände verwendet, die einem Produkt zugewiesen werden können. |

> [!NOTE]
> Sie können die Datenentität **Freigegebene Produkte V2** verwenden, um Produkte nur dann in das System zu importieren, wenn das freigegebene Produkt bereits erstellt wurde. Andernfalls müssen Sie zum Importieren von Produkten in das System die Datenentität **Produkterstellung** verwenden.
