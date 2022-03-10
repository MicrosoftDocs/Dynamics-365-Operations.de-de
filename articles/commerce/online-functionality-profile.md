---
title: Ein Onlinefunktionsprofil erstellen
description: In diesem Thema wird beschrieben, wie Sie ein Online-Funktionsprofil in Microsoft Dynamics 365 Commerce erstellen.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: d6dcbb5b9ea01035396e90a6809cb1568c3a4fc86def41cf36732588b5046da7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716193"
---
# <a name="create-an-online-functionality-profile"></a>Ein Onlinefunktionsprofil erstellen

[!include [banner](includes/banner.md)]

In diesem Thema erhalten Sie einen Überblick über das Einrichten eines Onlinefunktionsprofils für Microsoft Dynamics 365 Commerce.

Das Online-Funktionalitätsprofil bietet verschiedene Einstellungen für Onlinekanäle. Jeder Online-Kanal muss ein Online-Funktionsprofil angeben.

## <a name="create-an-online-functionality-profile"></a>Ein Onlinefunktionsprofil erstellen

In der folgenden Prozedur wird erläutert, wie Sie ein Onlinefunktionalitätsprofil in der Commerce Headquarters-App erstellen.

1. Gehen Sie im Navigationsbereich zu **Module \> Kanaleinrichtung \> Oline Shop einrichten \> Funktionsprofile**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. In dem Feld **Profil** geben Sie eine ID für das Profil ein.
1. Geben Sie im Feld **Beschreibung** einen Wert ein („Adventure Works Profile“ im folgenden Beispielbild).
1. In dem Abschnitt **Funktionen** ändern Sie die Einstellungen **EINKAUFSWAGEN**, **EINZELHANDELSKUNDEN** oder **AUSCHECKEN** nach Bedarf.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

Das folgende Bild zeigt ein Beispiel für ein Online-Funktionsprofil.
  
![Online-Funktionsprofil Beispiel.](media/online-functionality-profile.png)

## <a name="functions"></a>Funktionen

- **Aggregatprodukte**: Wenn diese Funktion aktiviert ist, kann der Warenkorb die Menge aktualisieren, wenn derselbe Artikel mehrmals hinzugefügt wird.
- **Kasse ohne Zahlungen zulassen** : Wenn diese Funktion aktiviert ist, wird das Szenario behandelt, wenn zum Warenkorb hinzugefügte Artikel einen Preis von $0.00 haben.
- **Kunden im asynchronen Modus erstellen**: Dies ist eine Vorgängereinstellung für E-Commerce-Kanäle von Drittanbietern und gilt nicht für die Dynamics 365-E-Commerce-Site.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Kanäle Übersicht](channels-overview.md)

[Kanaleinstellungen – Voraussetzungen](channels-prerequisites.md)

[Einen Onlinekanal einrichten](channel-setup-online.md)

[Einen Retail Channel einrichten](channel-setup-retail.md)

[Einen Callcenterkanal einrichten](channel-setup-callcenter.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
