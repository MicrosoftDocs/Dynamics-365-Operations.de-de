---
title: " Treuebelohnungspunkte definieren"
description: Diese Prozedur führt Sie Schritt für Schritt durch das Definieren von Treuebelohnungspunkten.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailLoyaltyRewardPoints
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e40ebcbf3ab1befc641ae34571a8b974bd0425a
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140875"
---
# <a name="define-loyalty-reward-points"></a> Treuebelohnungspunkte definieren

[!include [banner](../includes/banner.md)]

Diese Prozedur führt Sie Schritt für Schritt durch das Definieren von Treuebelohnungspunkten. Sie sollten Treuebelohnungspunkte einrichten, bevor Sie ein Treueprogramm einrichten. Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.

1. Navigieren Sie zu Retail and Commerce > Debitoren > Treue > Treuebelohnungspunkte.
2. Klicken Sie auf Neu.
3. Geben Sie im Feld "Belohnungspunktkennung" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Wählen Sie im Belohnungspunkttyp-Feld eine Option aus.
    * Wählen Sie "Menge" aus, wenn die Belohnungspunkte auf die nächste ganze Zahl gerundet werden sollen. Wählen Sie "Betrag" aus, wenn die Belohnungspunkte gemäß Währungsrundungsregeln gerundet werden sollen. Wenn Sie "Menge" auswählen, fahren Sie mit dem nächsten Schritt dieses Verfahrens fort.  
6. Geben Sie im Feld "Währung" einen Wert ein.
    * Für Betragstypbelohnungs-Punkte haben alle ausgegebenen Punkte die ausgewählte Währung. Für Mengentyp-Belohnungspunkte gilt dieses Feld nicht – überspringen Sie diesen Schritt.  
7. Aktivieren oder deaktivieren Sie das Kontrollkästchen ''Einlösbar".
8. Geben Sie eine Zahl im Feld "Einlöserang" ein.
    * Einlöserang wird verwendet, wenn zwei oder mehr einlösbare Belohnungspunkte verwendet werden können, um für Produkte zu bezahlen. Wenn die beiden Belohnungspunkte den gleichen Einlöserang haben, wird der, dessen Punktzahl niedriger sein muss, verwendet.  
9. Geben Sie eine Zahl in das Feld "Wert für Ablaufzeit" ein.
    * Die Belohnungspunkte laufen die angegebene Anzahl von Tagen, Monaten oder Jahren ab, nachdem die Punkte ausgestellt werden. Ein Wert von 0 bedeutet, dass die Loyalitätsbelohnungspunkte niemals ablaufen.  
10. Wählen Sie im Feld "Einheit für Ablaufzeit" eine Option aus.
11. Klicken Sie auf "Speichern".
