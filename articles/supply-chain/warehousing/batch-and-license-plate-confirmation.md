---
title: Chargen- und Kennzeichenbestätigung
description: In diesem Artikel wird beschrieben, wie Sie Chargen- und Kennzeichenbestätigung über ein mobiles Gerät einrichten und anwenden.
author: Mirzaab
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ef0d528d23c1ee9424e35e29d39121d42ba548e5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903723"
---
# <a name="batch-and-license-plate-confirmation"></a>Chargen- und Kennzeichenbestätigung

[!include [banner](../includes/banner.md)]

Chargenbestätigung ermöglicht Ihnen, zu bestätigen, dass die richtige Charge vom mobilen Gerät gewählt wird. Nur bei der ersten Arbeitsentnahme für Artikel aus *Charge oberhalb\[Lagerplatz\]*, wobei Charge oberhalb angibt, dass die Charge in der Suchenhierarchie höher liegt, als der Lagerplatz, müssen Sie überprüfen, dass die entnommene Charge mit der Charge auf der Arbeitsposition übereinstimmt.

Kennzeichenbestätigung ermöglicht Ihnen, zu bestätigen, dass die richtige Kennzeichen vom mobilen Gerät gewählt wird. Wenn Arbeit aus einem Phasenlagerplatz entnommen wird, müssen Sie überprüfen dass das entnommene Kennzeichen mit dem Kennzeichen übereinstimmt, das der Arbeit zugeordnet ist. Wenn die Arbeit gestartet wird, indem ein Kennzeichen gescannt wird, wird dieser Bestätigungsschritt übersprungen.

## <a name="where-it-applies"></a>Wofür es angewendet wird

Bestätigung gilt in den folgenden Szenarien:

- Chargenbestätigung gilt für die erste Entnahme der Arbeit für Artikel der Chargen oberhalb.
- Kennzeichenbestätigung gilt für Entnahmen aus den Phasenlagerplätzen.

> [!IMPORTANT]
> Die Wiederbeschaffung wird für die Bestätigung von Ladungsträgern nicht unterstützt. Beim Ausführen von Wiederbeschaffung wird kein Schritt zur Bestätigung von Ladungsträgern erstellt.

## <a name="set-up-batch-and-license-plate-confirmation"></a>Chargen- und Kennzeichenbestätigung einrichten

Sie können Chargen- und Kennzeichenbestätigung von den Menüeinträgen des mobilen Geräts aus konfigurieren.

1. Geben Sie im Menüeintrag des mobilen Geräts die Einrichtung der Arbeitsbestätigung ein.  
1. Wählen Sie die Option für Kennzeichen- oder Chargen-Bestätigung aus. Beide Optionen sind für Arbeitstypentnahmen verfügbar, bei denen keine automatische Bestätigung aktiviert ist.  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
