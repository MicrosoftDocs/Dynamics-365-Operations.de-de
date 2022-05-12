---
title: Abonnementabrechnung – Übersicht
description: In diesem Thema wird die Abonnementabrechnung in Microsoft Dynamics 365 Finance beschrieben.
author: JodiChristiansen
ms.date: 04/13/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustVendExternalItem
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-02-09
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 9d46492cca3cc435048fa497f6b1f3a28b77140a
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2022
ms.locfileid: "8644526"
---
# <a name="subscription-billing-overview"></a>Abonnementabrechnung – Übersicht

[!include [banner](../includes/banner.md)]

Die Abonnementabrechnung ermöglicht es Unternehmen, Abonnementeinnahmen und wiederkehrende Abrechnungen über Abrechnungszeitpläne zu verwalten. Komplexe Preis- und Abrechnungsmodelle und Umsatzerlöszuteilung lassen sich einfach verwalten und auf Positionsebene abrechnen und erfassen. Die Umsatzerlöszuteilung mit mehreren Elementen ermöglicht die Zuteilung von Umsatzerlösen gemäß den internationalen Rechnungslegungsstandards (International Financial Reporting Standard 15 \[IFRS 15\]) und den allgemein anerkannten Buchhaltungsprinzipien (US-GAAP) (Accounting Standards Codification Topic 606 \[ASC606\]).

Die Lösung besteht aus drei Modulen, die unabhängig voneinander verwendet werden können. Alternativ können alle drei Module zusammen verwendet werden.

- **Wiederkehrende Vertragsabrechnung**: Dieses Modul ermöglicht die wiederkehrende Abrechnung und das Preismanagement, um die Kontrolle über Preis- und Abrechnungsparameter, Vertragsverlängerung und konsolidierte Rechnungsstellung zu ermöglichen.
- **Umsatzerlös- und Ausgabenstundungen**: Dieses Modul eliminiert manuelle Prozesse und die Abhängigkeit von externen Systemen, indem es Umsatzerlöse verwaltet und Erkenntnisse in Echtzeit in monatlich wiederkehrenden Umsatzerlösen ermöglicht.
- **Umsatzerlöszuteilung mit mehreren Elementen**: Dieses Modul hilft bei der Umsatzerlöscompliance, indem es die Preisgestaltung und Umsatzerlöszuteilung über mehrere Artikel hinweg handhabt.

Weitere Informationen zur Abonnementabrechnung finden Sie unter [Power BI-Inhalt zur Abonnementabrechnung](sub-bill-power-bi.md).

Die Abonnementabrechnung wird durch die **Funktionsverwaltung** aktiviert. Es kann jedoch nicht mit der Funktion **Umsatzerkennung** verwendet werden. Daher müssen Sie diese Funktion deaktivieren, bevor Sie die Abonnementabrechnung aktivieren.

1. Wählen Sie den Arbeitsbereich **Funktionsverwaltung** auf der Registerkarte **Alle** aus, geben Sie **Umsatzerkennung** in den Filter ein und wählen Sie dann den Funktionsnamen als Filter aus.
2. Wählen Sie die Funktion **Umsatzerkennung** und dann **Deaktivieren** aus.
3. Geben Sie im Filter **Funktionsname** **Abonnementabrechnung** ein und wählen Sie dann den Modulfilter aus.
4. Wählen Sie die Funktion **Abonnementabrechnung** und dann **Aktivieren** aus.
5. Wählen Sie eines der drei Module aus der vorherigen Liste und dann **Aktivieren** aus. Wiederholen Sie diesen Schritt für die beiden anderen Module.

    > [!IMPORTANT]
    > Die Funktion **Abonnementabrechnung** muss aktiviert werden, bevor Sie eines der drei Module aktivieren können.
