---
title: Regulieren der Einstandswerte für verfügbaren Bestand
description: Verwenden Sie die Seite "Anpassung des verfügbaren Lagerbestands", um den Einstandswert der Mengen des verfügbaren Lagerbestands zu regulieren, nachdem ein Lagerabschlusses durchgeführt wurde.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a702a083d60bdb289712027fbaee5c0a72e60cb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963837"
---
# <a name="adjust-on-hand-inventory-cost-values"></a>Regulieren der Einstandswerte für verfügbaren Bestand

[!include [banner](../includes/banner.md)]

Verwenden Sie die Seite "Anpassung des verfügbaren Lagerbestands", um den Einstandswert der Mengen des verfügbaren Lagerbestands zu regulieren, nachdem ein Lagerabschlusses durchgeführt wurde.

Verwenden Sie die Seite **Anpassung des verfügbaren Lagerbestands**, um den Einstandswert der Mengen des verfügbaren Lagerbestands zu regulieren, nach Ausführung eines Lagerabschlusses. **Hinweis:** Um die Seite **Anpassung des verfügbaren Lagerbestands** auf der Seite **Abschluss und Regulierung** zu öffnen, wählen Sie den Datensatz eines bereits abgeschlossenen Lagerabschlussprozesses aus, und klicken Sie anschließend auf **Regulierung** &gt; **Verfügbar**. **Beispiel:** Im Februar liegen die folgenden Buchungen vor:

-   1. Februar: Wertmäßiger Lagerzugang für die Menge "2" mit einem Einstandspreis von EUR 10,00
-   5. Februar: Wertmäßiger Lagerzugang für die Menge "1" mit einem Einstandspreis von EUR 13,00
-   19. Februar: Wertmäßiger Lagerabgang für die Menge "1" mit einem laufenden Durchschnittseinstandspreis von EUR 11,00

Dieser Artikel wurde mit dem FIFO-Lagermodell (First In, First Out) eingerichtet, und der Lagerabschluss erfolgte am 28. Februar. Die wertmäßige Abgangsbuchung in Höhe von EUR 11,00 wird mit dem wertmäßigen Zugang vom 1. Februar ausgeglichen, und eine Regulierung von EUR 1,00 wird vorgenommen. Die folgenden Lagerzugänge enthalten dann offene Lagermengen:

-   1. Februar: Menge "1" mit einem Einstandspreis von EUR 10,00
-   5. Februar: Menge "1" mit einem Einstandspreis von EUR 13,00

Verwenden Sie die Option für die Regulierung des verfügbaren Bestands, um die Kosten dieser beiden Artikel auf EUR 15,00 festzulegen, und regulieren Sie die offenen verfügbaren Bestandsmengen zum Datum der letzten Lagerabschlussperiode. **Hinweis:** Als Buchungsdatum für die Regulierung des verfügbaren Bestands wird das Datum des letzten Lagerabschlusses verwendet. Dieses Datum kann nicht geändert werden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]