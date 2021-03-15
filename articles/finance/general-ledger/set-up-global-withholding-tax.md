---
title: Globale Quellensteuer einrichten
description: In diesem Thema werden die Schritte zum Einrichten der globalen Quellensteuer für Verkäufe und Käufe aufgeführt.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 7ee577651694f0553447d6e9d0851402a586f363
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060740"
---
# <a name="set-up-global-withholding-tax"></a>Globale Quellensteuer einrichten

In diesem Thema werden die Schritte zum Einrichten der globalen Quellensteuer für Verkäufe und Käufe aufgeführt. 

1. Richten Sie Quellensteuerbehörden auf der Seite **Quellensteuerbehörden** ein.

2. Richten Sie Einrichten von Quellensteuerausgleichsperioden auf der Seite **Quellensteuerausgleichsperioden** ein.

3. Richten Sie eine Quellensteuer-Sachkontobuchungsgruppe auf der Seite **Quellensteuer > Sachkontobuchungsgruppe** ein.

   > [!Note] 
   >
   > Das **Quellensteuer**-Konto wird einem Hauptkonto mit **Buchungstyp** „Quellensteuer“ zugewiesen. Das **Quellensteuer-Gegenkonto** wird ebenfalls einem Hauptkonto mit dem **Buchungstyp** „Quellensteuer-Gegenkonto“ zugewiesen. Rufen Sie **Hauptbuch > Kontenplan> Konten > Hauptkonten** auf, und richten Sie den **Buchungstyp** im Unterformular **Buchungsprüfung** für die Hauptkonten ein.

4. Richten Sie Quellensteuercodes auf der Seite **Quellensteuercodes** ein.

5. Richten Sie Quellensteuergruppen auf der Seite **Quellensteuergruppen** ein.

6. Richten Sie Quellensteuer-Umsatzerlöstypen auf der Seite **Quellensteuerumsatz** **Typen** ein.

7. Richten Sie Quellensteuergruppen auf der Seite **Artikel-Quellensteuergruppen** für einen Artikel oder eine Dienstleistung ein.

8. Richten Sie **Mindestrechnungsbetrag** auf der Seite **Hauptbuchparameter > Quellensteuer** ein.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]