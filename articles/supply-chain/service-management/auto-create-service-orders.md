---
title: Automatisches Erstellen von Serviceaufträgen
description: Serviceaufträge können auf der Grundlage einer Servicevereinbarung für die Gültigkeitsperiode der Servicevereinbarung generiert werden.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41f48e2156ea5f57e600cc5dec09a78a91992d60
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675794"
---
# <a name="automatically-create-service-orders"></a>Automatisches Erstellen von Serviceaufträgen 

[!include [banner](../includes/banner.md)]


Serviceaufträge können auf der Grundlage einer Servicevereinbarung für die Gültigkeitsperiode der Servicevereinbarung generiert werden.

Die Serviceaufträge, die auf Basis einer Servicevereinbarung generiert werden, sind alle der entsprechenden Servicevereinbarung zugeordnet.

Serviceaufträge werden automatisch gemäß den folgenden Einstellungen generiert:

  - Das in den Servicevereinbarungspositionen eingerichtete Servicevereinbarungsintervall. Mit dem Servicevereinbarungsintervall wird die Erstellungshäufigkeit der Servicevereinbarungspositionen angegeben. Weitere Informationen zu Serviceintervallen finden Sie unter [Serviceintervalle](service-intervals.md).

  - Die angegebene Periode zum Definieren der Serviceperiode (in den Feldern **Von Datum** und **Bis Datum** des Formulars **Erstellen von Serviceaufträgen**). Weitere Informationen zum Erstellen von Serviceaufträgen finden Sie unter [Automatische Erstellung von Serviceaufträgen](create-service-orders-automatically.md).

  - Die Option **Serviceaufträge kombinieren** im Servicevertragskopf. Mit dieser Option wird definiert, ob Serviceaufträge anhand von Serviceauftragspositionen, die für eine Servicevereinbarung generiert werden, nach Mitarbeiter, Serviceaufgabe, Serviceobjekt oder nach Servicevereinbarung kombiniert werden sollen. Weitere Informationen zur Kombination von Serviceaufträgen finden Sie unter [Serviceaufträge kombinieren](combine-service-orders.md).

  - Die Option **Zeitfenster** in der Servicevereinbarungsposition. Durch das Zeitfenster wird definiert, wie weit eine Servicevereinbarungsposition relativ zu ihrem berechneten Datum verschoben werden kann. Weitere Informationen zu Zeitfenstern finden Sie unter [Zeitfenster](time-windows.md).


> [!NOTE]
> <P>Ist der für einen Serviceauftrag angegebene Tag in dem Kalender, der im Formular <STRONG>Serviceverwaltungsparameter</STRONG> ausgewählt ist, nicht offen, wird eine Meldung mit einem entsprechenden Hinweis angezeigt. Diese Meldung kann ignoriert werden. Der Serviceauftrag wird auch dann erstellt, wenn der Tag im Kalender geschlossen ist.</P>

## <a name="example-1"></a>Beispiel 1

Die Servicevereinbarung gilt vom 1. Januar 2012 bis zum 31. Dezember 2012. Liegt die im Formular **Erstellen von Serviceaufträgen** angegebene Serviceperiode zwischen dem 1. November 2012 und dem 1. Februar 2013, werden Serviceaufträge vom 1. November 2012 bis zum 31. Dezember 2012 erstellt.

## <a name="example-2"></a>Beispiel 2

Die Servicevereinbarung gilt vom 1. Januar 2012 bis zum 31. Dezember 2012. Der Servicevereinbarung sind zwei Servicevereinbarungspositionen zugeordnet. Die eine Servicevereinbarungsposition besitzt als Startdatum den 2. Januar 2012 und als Enddatum den 1. März 2012. Die andere Servicevereinbarungsposition besitzt als Startdatum den 1. April 2012 und als Enddatum den 31. Dezember 2012. Im Formular **Erstellen von Serviceaufträgen** geben Sie eine Periode vom 1. Oktober 2012 bis zum 31. Dezember 2012 an. Aus diesem Grund werden lediglich Serviceaufträge für die zweite Vereinbarungsposition generiert, da das Start- und das Enddatum der ersten Vereinbarungsposition vor der Periode liegen, die für den Serviceauftrag angegeben wurde.

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]