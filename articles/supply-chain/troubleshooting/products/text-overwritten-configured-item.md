---
title: Text wird überschrieben, wenn ein Artikel in einer Auftragszeile konfiguriert ist
description: Wenn ein Produkt in einer Auftragszeile konfiguriert ist, wird der bearbeitete Text mit dem Standardtext überschrieben. Ändern Sie den Text, nachdem Sie die Zeile konfiguriert haben, nicht vorher.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 20239b9b0eecb355274e909a8b8b39450e468c7e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476398"
---
# <a name="item-text-is-overwritten-when-a-product-is-configured-on-a-sales-order-line"></a>Der Artikeltext wird überschrieben, wenn ein Produkt in einer Auftragsposition konfiguriert ist

## <a name="symptoms"></a>Symptome

Dieses Problem tritt auf, wenn Sie eine Verkaufsauftragszeile für einen konfigurierbaren Artikel erstellen und dann den Artikeltext ändern. Wenn Sie den Artikel konfigurieren und dann **OK** wählen, wird der Text mit dem Standardtext überschrieben.

## <a name="resolution"></a>Lösung

Dieses Verhalten wird erwartet. Das Textfeld enthält den Variantennamen, der erst ausgefüllt wird, nachdem Sie die Zeile konfiguriert haben. Daher müssen Sie den Text ändern, nachdem Sie die Zeile konfiguriert haben, nicht vorher.
