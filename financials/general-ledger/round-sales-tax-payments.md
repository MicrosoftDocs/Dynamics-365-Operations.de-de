---
title: Mehrwertsteuerzahlungen und Rundungsregeln
description: "In diesem Artikel wird beschrieben, wie sich die Rundungsregeleinstellung auf die Mehrwertsteuer-Behörden und auf die Rundung des Mehrwertsteuersaldos während der Abrechnung und Buchung der Mehrwertsteuer auswirkt."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: ecd32549b6067ed4c1211996e846e210f77f5013
ms.openlocfilehash: 8f28ab4ea0fed975edbed60ddf5630d2d26ba0bc
ms.lasthandoff: 03/31/2017


---

# <a name="sales-tax-payments-and-rounding-rules"></a>Mehrwertsteuerzahlungen und Rundungsregeln

In diesem Artikel wird beschrieben, wie sich die Rundungsregeleinstellung auf die Mehrwertsteuer-Behörden und auf die Rundung des Mehrwertsteuersaldos während der Abrechnung und Buchung der Mehrwertsteuer auswirkt.

In regelmäßigen Abständen muss Mehrwertsteuer gemeldet werden und an die Steuerbehörde abgeführt werden. Dazu öffnen werden, indem die Informationen zur Bank und Beitragsmehrwertsteuerprozess in der Mehrwertsteuerseite ausführt. Mehrwertsteuer einer Periode wird gegen die Mehrwertsteuerkonten ausgeglichen und der dem Mehrwertsteuerabrechnungsverrechnungskonto Mehrwertsteuersaldo wird gebucht. Der Mehrwertsteuersaldo, der im Konto "Mehrwertsteuerabrechnung" gebucht wird, kann je nach Anforderung der Steuerbehörden gerundet werden, indem eine Rundungsregel für die Mehrwertsteuerseite eingerichtet wird. 

Die Rundungsdifferenz wird zum Konto "Rundung Mehrwertsteuer" gebucht, das im Feld "Konten für automatische Buchungen" im "Hauptbuch" ausgewählt wird.

Das Beispiel unten veranschaulicht, wie der Rundenregel bei "Mehrwertsteuerbehörde" funktioniert.

### <a name="example"></a>Beispiel:

Die Gesamtumsatzsteuer für eine Periode zeigt ein Guthaben von -98.765,43 an. Die juristische Person hat mehr Mehrwertsteuer eingenommen, als sie bezahlt hat. Daher schuldet die juristische Person der Steuerbehörde Geld. 

Die juristische Person möchte eine Rundungsmethode verwenden, mit der der Saldo auf die nächsten 1,00 gerundet wird. Der Benutzer, der für die Mehrwertsteuerbuchhaltung zuständig ist, führt die folgenden Schritte aus.

1.  Mehrwertsteuer-Mehrwertsteuerbehörden indirekte Steuern &gt; der Klick-
2.  Wählen Sie im Inforegister "Allgemein" im Feld "Rundungsart" die Option "Normal" aus.
3.  Geben Sie im Feld "Rundung" die Zahl 1,00 ein.
4.  Wenn die Mehrwertsteuer an das Finanzamt abgeführt werden soll, öffnen Sie die Seite "Mehrwertsteuer abrechnen und buchen". (Klick-Steuererklärungs- &gt;&gt; Mehrwertsteuer &gt; bank- und -Beitragsmehrwertsteuer.)
5.  Im Mehrwertsteuer-Abrechnungskonto wird der Steuerverbindlichkeitsbetrag von 98.765,43 auf 98.765 abgerundet.

Die folgende Tabelle zeigt, wie ein Betrag von 98.765,43 gerundet wird. Dabei wird jede Rundungsmethode angewendet, die im Feld "Rundungsart" auf der Seite "Steuerbehörden" verfügbar ist.

| Option der Rundungsart                | Rundungswert = 0,01 | Rundungswert = 0,10 | Rundungswert = 1,00 | Rundungswert = 100,00 |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| Normal                              | 98.765,43              | 98.765,40              | 98.765,00              | 98.800,00                |
| Abwärts                            | 98.765,43              | 98.765,40              | 98.765,00              | 98.700,00                |
| Aufrunden                         | 98.765,43              | 98.765,50              | 98.766,00              | 98.800,00                |
| Eigener Vorteil, für ein Guthaben | 98.765,43              | 98.765,40              | 98.765,00              | 98.700,00                |
| Eigener Vorteil, für ein Debitorensaldo  | 98.765,43              | 98.765,50              | 98.766,00              | 98.800,00                |

> [!NOTE]                                                                                  
> Wenn Sie "Eigener Vorteil" auswählen, erfolgt die Rundung immer zum Vorteil der juristischen Person. 

Weitere Informationen finden Sie Mehrwertsteuerüberblick []( indirect-taxes-overview.md). 


