---
title: Fehlerbehebung bei ausgehenden Lagerort-Vorgängen
description: In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben können, die bei der Arbeit mit ausgehenden Lagerort-Vorgängen in Microsoft Dynamics 365 Supply Chain Management auftreten können.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 491803c5f9394f47a996c4e4c7fb8925e9464e644c99e5c1ab434706af6ad74e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756654"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a>Fehlerbehebung bei ausgehenden Lagerort-Vorgängen

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben können, die bei der Arbeit mit ausgehenden Lagerort-Vorgängen in Microsoft Dynamics 365 Supply Chain Management auftreten können.

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a>Ich erhalte die folgende Fehlermeldung: „Verkaufsauftrag konnte nicht freigegeben werden.“

### <a name="issue-description"></a>Problembeschreibung

Dieses Problem kann aus mehreren Gründen auftreten. Zum Beispiel befindet sich der Auftrag in der Kreditverwaltung und es können keine Sendungen erstellt werden, bis eine gültige Postadresse für alle Verkaufszeilen, die mit einem Verkaufsauftrag verbunden sind, eingegeben wurde. Oder es gibt eine Auftragssperre, die behoben werden muss, bevor der Auftrag für das Lagerort freigegeben werden kann. Dieser Halt kann auftragsspezifisch sein oder sich auf das Kundenkonto beziehen.

### <a name="issue-resolution"></a>Problemlösung

Fügen Sie die Adresse auf dem Auftrag und den Auftragszeilen hinzu oder aktualisieren Sie sie, und geben Sie den Auftrag dann für das Lager frei. Aufträge können nur dann für das Lagerort freigegeben werden, wenn sie eine gültige Lieferadresse haben (gemäß dem Adressformat, das im Modul **Organisationsverwaltung** eingerichtet wurde).

Untersuchen Sie den Auftragsstopp und beheben Sie die Probleme. Entfernen Sie dann die Sperrung des Auftrags oder des Kunden und geben Sie den Auftrag für das Lagerort frei.

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a>Ich erhalte die folgende Meldung: „Die Lieferung für Ladung 1% wurde bestätigt.“ Es werden jedoch keine Zeilen gebucht.

### <a name="issue-description"></a>Problembeschreibung

Eine Sendung zu einer Ladung wurde bestätigt, aber es erfolgte keine weitere Buchung.

### <a name="issue-resolution"></a>Problemlösung

Die Sendungsbestätigung hat keinen Einfluss auf die Buchung. Sie aktualisiert nur den Status der Sendung und der Ladung. Die Verbuchung muss in einem separaten Prozess erfolgen.

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a>Ich erhalte die folgende Fehlermeldung: „Die Direktlieferung kann für Lagerort 1% nicht verarbeitet werden, da die Lagerortverwaltung aktiviert ist. Bitte geben Sie einen anderen Lagerort an, für das die Lagerortverwaltung nicht aktiviert ist.“

### <a name="issue-description"></a>Problembeschreibung

Ein Element wird einer Verkaufszeile zur Direktlieferung aus einem Lagerort hinzugefügt, der für die Lagerortverwaltung (WMS) aktiviert ist. Sie erhalten diese Fehlermeldung, wenn die Verkaufszeile aktualisiert wird. 

### <a name="issue-resolution"></a>Problemlösung

Microsoft hat dieses Problem untersucht und festgestellt, dass es sich um eine Einschränkung der Funktion handelt. Derzeit unterstützt WMS die direkte Lieferung nicht. Um die direkte Lieferung zu verwenden, müssen Sie daher ein Element und ein Lagerort auswählen, die nicht zu WMS gehören.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]