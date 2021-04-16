---
title: Problembehandlung bei Chargen- und Serienreservierungshierarchien für Lagerorte
description: In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben können, die bei der Arbeit mit Reservierungshierarchien mit Chargen- oder Seriendimensionen auftreten können.
author: perlynne
ms.date: 3/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 3/12/2021
ms.openlocfilehash: a1abb6f8657484d43d434076e5ee38d1c63fe2ff
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838177"
---
# <a name="troubleshoot-warehouse-batch-and-serial-reservation-hierarchies"></a>Problembehandlung bei Chargen- und Serienreservierungshierarchien für Lagerorte

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben können, die bei der Arbeit mit Reservierungshierarchien mit Chargen- oder Seriendimensionen auftreten können.

Weitere Informationen finden Sie unter [Flexible Richtlinie für die Reservierung von Dimensionen auf Lagerebene](flexible-warehouse-level-dimension-reservation.md).

Die Reservierungshierarchie eines Artikels bestimmt die Anforderung von Lagerdimensionen, die erfüllt sein müssen, um einem Bedarfsauftrag einen Lagerplatz zuzuweisen. Diese Dimensionen können als *Dimensionen oberhalb des Lagerplatzes* für alle Dimensionen beschrieben werden, die erfüllt sein müssen, bevor ein Lagerplatz zugewiesen wird, und als *Dimensionen unterhalb des Lagerplatzes*, für Dimensionen, die zugewiesen werden können, nachdem dem Bedarfsauftrag ein Standort zugewiesen wurde. Diese Reservierungshierarchien werden auch als *Charge oberhalb* und *Charge unterhalb* Reservierungshierarchien oder *Serie oberhalb* und *Serie unterhalb* Reservierungshierarchien bezeichnet.

Der Bestand kann nur dann erfolgreich zugeteilt werden, wenn in den Dimensionen oberhalb des Lagerplatzes keine Lücken vorhanden sind. Zum Beispiel würden Sie in einer Reservierungshierarchie *Charge oberhalb* erwarten, dass für den Bedarfsauftrag Dimensionen für **Standort,** **Lagerort** und **Chargennummer** angegeben sind. Wenn eine dieser Dimensionen fehlt, schlägt der Zuteilungsprozess fehl. Im Gegensatz dazu ist für eine Reservierungshierarchie *Charge oberhalb* oder *Serie unterhalb* vielleicht eine Chargen- oder Seriennummer in dem Bedarfauftrag angegeben, der Zuteilungsprozess erfordert dies jedoch nicht.

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a>Ich erhalte die folgende Fehlermeldung: „Um einer Welle zugewiesen zu werden, müssen Ladungszeilen die Dimensionen oberhalb des Lagerplatzes angeben. Um diese Dimensionen zuzuweisen, reservieren Sie und erstellen Sie die Ladelinie neu.“

### <a name="issue-description"></a>Problembeschreibung

Wenn Sie einen Artikel verwenden, der eine Reservierungshierarchie *Charge oberhalb* hat, funktioniert der Befehl **An Lager freigeben** auf der Seite **Ladungsplanungs-Workbench** nicht, wenn Sie eine Ladung für eine Teilmenge freigeben möchten. Sie erhalten diese Fehlermeldung, und es wird keine Arbeit für die Teilmenge erstellt.

Wenn Sie jedoch einen Artikel verwenden, das eine Reservierungshierarchie *Charge unterhalb* hat, können Sie auf der Seite **Ladungsplanungs-Workbench** für eine Teilmenge eine Ladung freigeben.

### <a name="issue-cause"></a>Ursache des Problems

Wenn in der Reservierungshierarchie eine Dimension oberhalb der Dimension **Lagerplatz** vorhanden ist, muss diese vor der Freigabe zum Lagerort angegeben werden. Teilmengen können nicht freigegeben werden, wenn eine oder mehrere Dimensionen über **Lagerplatz** nicht angegeben sind.

## <a name="the-auto-reservation-prompt-for-a-batch-number-is-triggered-even-though-there-is-available-inventory"></a>Die automatische Reservierungsaufforderung für eine Chargennummer wird ausgelöst, obwohl Bestand verfügbar ist.

### <a name="issue-description"></a>Problembeschreibung

Wenn Sie einen Artikel mit einer Reservierungshierarchie *Charge oberhalb* in einem Lagerort verwenden, in dem Lagerortprozesse nicht aktiviert wurde und die automatische Reservierung aktiviert ist, wird die automatische Reservierungsaufforderung für eine Chargennummer angezeigt, auch wenn nur eine Charge zur Entnahme verfügbar ist.

Wenn Sie jedoch denselben Artikel in einem Lagerort verwenden, in dem Lagerortprozesse aktiviert sind, wird die Eingabeaufforderung für die automatische Reservierung nicht angezeigt.

### <a name="issue-cause"></a>Ursache des Problems

Wenn eine Reservierungshierarchie als *Charge oberhalb* oder *Serie oberhalb* definiert ist, müssen die referenzierte Dimension (**Chargennummer** oder **Seriennummer**) immer auf Bedarfsaufträgen angegeben werden. Lagerortprozesse können die Informationen möglicherweise vervollständigen, wenn eine einzelne Chargen- oder Seriennummer verfügbar ist. Da der Lagerort jedoch nicht für Lagerortprozesse aktiviert ist, muss der Benutzer immer alle oben genannten Dimensionen oberhalb von **Lagerplatz** angeben.

## <a name="slotting-templates-that-have-the-consider-on-hand-slot-criterion-dont-consider-current-on-hand-inventory-for-batch-enabled-items"></a>Vorlagen für die Zuteilung von Zeitfenstern mit dem Zeitfensterkriterium „Vorhandenes berücksichtigen“ berücksichtigen nicht den aktuellen Bestand von Artikeln, für die Chargen aktiviert sind.

Weitere Informationen finden Sie unter [Zeitfenster für Lagerort zuweisen](warehouse-slotting.md).

### <a name="issue-description"></a>Problembeschreibung

Vorlagen für die Zuteilung von Zeitfenstern mit dem Zeitfensterkriterium *Vorhandenes berücksichtigen* berücksichtigen nicht den aktuellen Bestand von *Charge oberhalb*-Artikeln. Sie berücksichtigen es nur, wenn die Chargennummer in der Auftragsposition angegeben ist.

Wenn Sie jedoch *Chargen unterhalb*-Artikel verwenden, wird der aktuelle Bestand wie erwartet angesehen.

### <a name="issue-cause"></a>Ursache des Problems

Die Kopfzeile der Vorlage für die Zuteilung von Zeitfenstern kann für die Bedarfsstrategie *Bestellt*, *Reserviert* oder *Freigegeben* definiert werden. Für die Bedarfsstrategie *Bestellt* gelten dieselben Anforderungen an die Reservierungshierarchie wie für die Prozesse zur Reservierung oder Freigabe an Lagerorte. Für Artikel mit der Reservierungshierarchie *Charge oberhalb* und *Serie unterhalb* muss die Chargen- oder Seriennummer auf dem Bedarfsauftrag (Verkauf oder Übertragung) angegeben werden. Alternativ kann die Bedarfsstrategie *Reserviert* verwendet werden, um die Chargen- oder Seriennummer auszuwählen, bevor der Bedarf zur Zuteilung eines Zeitfensters am Lagerort generiert wird.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
