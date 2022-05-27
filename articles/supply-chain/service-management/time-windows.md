---
title: Zeitfenster
description: Sie können Zeitfenster verwenden, um die Planung von Serviceauftragspositionen zu optimieren.
author: sorenva
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 857e9e023aa5648a06ae564936f06c491ea7cefc
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678093"
---
# <a name="time-windows"></a>Zeitfenster  

[!include [banner](../includes/banner.md)]

Sie können Zeitfenster verwenden, um die Planung von Serviceauftragspositionen zu optimieren. Sie können das System so einrichten, dass es automatisch Serviceaufträge erstellt. Basierend auf den Kriterien, die durch ein Zeitfenster angegeben sind, können Sie möglichst viel Serviceauftragspositionen herstellen, die mit möglichst wenigen Serviceaufträgen verbinden werden können.

Zeitfenster legen fest, wie weit eine Serviceauftragsposition in Bezug auf das berechnete Datum verschoben werden kann. Das berechnete Datum ist das Datum, an dem die Serviceauftragsposition geplant war. Das Datum basiert auf der Intervalleinstellung und der Serviceperiode, die Sie im Formular **Serviceauftrag erstellen** definiert haben. Ein Zeitfenster wird unter Verwendung der Werte in der folgenden Tabelle festgelegt.

| Methode | Beschreibung                                                                                                                                                                                                                                                                                           |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Woche   | Das Datum, zu dem die Serviceauftragsposition verschoben werden kann, ist jeder offene Tag innerhalb der gleichen Woche wie das ursprüngliche berechnete Datum.                                                                                                                                                                                    |
| Monat  | Das Datum, zu dem die Serviceauftragsposition verschoben werden kann, ist jeder offene Tag innerhalb des gleichen Monats wie das ursprüngliche berechnete Datum. Beispielsweise ist das berechnete Datum für eine Serviceauftragsposition. der 15. Februar 2017. Die kann Serviceauftragsposition für einen beliebigen Wochentag und dem 28. Februar 2017 zwischen dem 1. Februar geplant werden. |
| Manuell | Sie können die maximale Zahl von Tagen vor oder nach dem ursprünglichen berechneten Datum für das Verschieben der Serviceauftragsposition festlegen.                                                                                                                                                                           |

Wenn für eine Servicevereinbarungsposition kein Zeitfenster angegeben wird, muss die aus der Servicevereinbarung abgeleitete Serviceauftragsposition genau an dem ursprünglich geplanten Datum ausgeführt werden.

## <a name="related-topics"></a>Verwandte Themen

[Erstellen von Zeitfenstern](create-time-windows.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]