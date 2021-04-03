---
title: Nach dem Kopieren der Umgebung fehlende Produkte und Kategorien
description: Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn Produkte und Kategorien nach dem Kopieren einer Website zwischen Umgebungen oder innerhalb derselben Umgebung fehlen.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 35f2cbd98a91149395f40bf821c1d5d7e58eaf77
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585347"
---
# <a name="products-and-categories-missing-after-environment-copy"></a>Nach dem Kopieren der Umgebung fehlende Produkte und Kategorien

[!include [banner](../../includes/banner.md)]

Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn Produkte und Kategorien nach dem Kopieren einer Website zwischen Umgebungen oder innerhalb derselben Umgebung fehlen.

## <a name="description"></a>Beschreibung

Nachdem eine Website von einer Umgebung in eine andere oder innerhalb derselben Umgebung kopiert wurde, fehlen die Produkte und Kategorien auf der Website. Die Produkte und Kategorien fehlen in der E-Commerce-Storefront und in der Registerkarte **Produkte** im Commerce-Website-Generator.

## <a name="resolution"></a>Lösung

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a>Die Kanalvorgangseinheitsnummer einer neu kopierten Website im Commerce-Website-Generator zuordnen

Befolgen Sie diese Schritte, um die Kanalvorgangseinheitsnummer (Operating Unit Number, OUN)einer neu kopierten Website im Commerce-Website-Generator zuzuordnen.

1. Wählen Sie die neu kopierte Website aus.
1. Wählen Sie in den **Websiteeinstellungen** die Option **Kanäle** aus.
1. Wählen Sie neben dem Kanalnamen die Auslassungspunkte (**...**) und anschließend **Onlineshop-Kanal ändern** aus.
1. Wählen Sie im Dialogfeld **Onlineshop-Kanal ändern** den Kanal aus, der der neu kopierten Website zugeordnet werden soll, und wählen Sie dann **OK** aus.
1. Wählen Sie **Speichern und veröffentlichen** aus.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Zuordnen einer Dynamics 365 Commerce-Website zu einem Onlinekanal](../associate-site-online-store.md)