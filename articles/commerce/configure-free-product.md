---
title: Konfigurieren eines Produkts, das kostenlos gekauft werden soll
description: In diesem Artikel wird beschrieben, wie Sie ein Produkt in Microsoft Dynamics 365 Commerce so konfigurieren, dass es kostenlos gekauft werden kann.
author: anupamar-ms
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 88370085de047a5e0be773dde218770cfa242d14
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280363"
---
# <a name="configure-a-product-to-be-purchased-for-free"></a>Konfigurieren eines Produkts, das kostenlos gekauft werden soll

[!include [banner](includes/banner.md)]


In diesem Artikel wird beschrieben, wie Sie ein Produkt in Microsoft Dynamics 365 Commerce so konfigurieren, dass es kostenlos gekauft werden kann.

## <a name="configure-the-product"></a>Konfigurieren des Produkts

Um ein Produkt kostenlos in Dynamics 365 Commerce zu verkaufen, müssen Sie den Preis auf 0 (Null) setzen. Außerdem müssen Sie die Produkteinstellungen **Nullpreis gültig** konfigurieren.

Um die neue **Nullpreis gültig**-Einstellung in der Commerce-Zentrale zu konfigurieren, folgen Sie diesen Schritten.

1. Navigieren Sie zu **Einzelhandel und Handel \> Produkte und Kategorien \> Freigegebene Produkte nach Kategorie**.
1. Gehen Sie zu dem Produkt, das Sie kostenlos verkaufen möchten. 
1. Im **Handel**-Abschnitt der Produktseite stellen Sie die **Nullpreis gültig**-Option auf **Ja**.

Die folgende Abbildung zeigt ein Beispiel für ein Produkt, bei dem die **Nullpreis gültig**-Option auf **Ja** eingestellt ist.

![Beispiel für ein Produkt, bei dem die Option Nullpreis gültig auf Ja gesetzt ist.](./media/Zero-price.png)

## <a name="configure-the-online-stores-functionality-profile"></a>Konfigurieren des Funktionsprofils des Online-Shops

Bevor kostenlose Transaktionen verarbeitet werden können, sollten Sie die **Kasse ohne Zahlungen zulassen**-Einstellung des Funktionsprofils für Ihren Online-Shop konfigurieren, sodass Transaktionen ohne Zahlungen zulässig sind. Informationen zum Erstellen von Funktionsprofilen finden Sie unter [Ein Online-Funktionsprofil erstellen](online-functionality-profile.md).

Um die neue **Kasse ohne Zahlungen zulassen**-Einstellung in der Commerce-Zentrale zu konfigurieren, folgen Sie diesen Schritten.

1. Gehen Sie zu **Retail und Commerce \> Kanaleinrichtung \> Einrichtung Onlineshop**.
1. Auf der Seite für das Funktionsprofil Ihres Shops legen Sie unter **Kasse** die **Kasse ohne Zahlungen zulassen**-Option auf **Ja** fest.

Die folgende Abbildung zeigt ein Beispiel für ein Online-Shop-Profil, in dem die **Kasse ohne Zahlungen zulassen**-Option auf **Ja** eingestellt ist.

![Beispiel für ein Online-Shop-Profil, in dem die Kasse ohne Zahlungen zulassen-Option auf Ja eingestellt ist.](./media/Zero-price-profile.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Verwaltung von Einzelhandelsverkaufspreisen](price-management.md)

[Ein Onlinefunktionsprofil erstellen](online-functionality-profile.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
