---
title: Manuelle Aktualisierung der Anlagenzähler
description: Dieses Thema beschreibt die manuelle Aktualisierung von Anlagenzählern im Anlagenmanagement.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e7c5ec288404c18b00f9dcd0e66f50744d0aa2f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875674"
---
# <a name="manual-update-of-asset-counters"></a>Manuelle Aktualisierung der Anlagenzähler

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Zähler werden verwendet, um Registrierungen auf einer Anlage zu erstellen, z.B. hinsichtlich der Anzahl der Betriebsstunden oder der Anzahl der produzierten Mengen.

Wenn der für einen Zähler ausgewählte Zählertyp auf Vererbung von Zählerwerten eingestellt ist (**Anlagenmanagement** > **Einrichtung** > **Anlagentypen** > **Zähler** > **Allgemein** FastTab > **Anlagenzählerwerte vererben** Umschalttaste auf „Ja“ gesetzt), Wenn Sie dann eine neue Gegenzeile dieses Typs erstellen, wird jede untergeordnete Kühlstelle, die den gleichen Zählertyp verwendet, automatisch aktualisiert.

Unter **Alle Anlagen** erstellen Sie Stunden- oder Mengenzählerregistrierungen für eine Anlage, basierend auf Ihren Messwerten für die Anlage.

1. Klicken Sie auf **Anlagenmanagement** > **Allgemein** > **Anlagen** > **Alle Anlagen**.

2. Wählen Sie das Objekt in der Liste aus und klicken Sie auf **Zähler**. Im Formular **Anlagenzähler** sehen Sie eine Liste aller früheren Zählerregistrierungen für die ausgewählte Anlage.

3. Klicken Sie auf **Neu**, um eine neue Registrierung zu erstellen. Die Asset-ID wird automatisch eingefügt.

4. Wählen Sie im Feld **Zähler** den entsprechenden Zähler aus. Es sind nur Zähler verfügbar, die sich auf die auf der Anlage ausgewählte Anlagenart beziehen. Die zugehörige Einheit wird automatisch in das Feld **Einheit** eingefügt.

5. Wählen Sie Datum und Uhrzeit für die Zählerregistrierung.

6. Geben Sie in das Feld **Wert** die Nummer seit der letzten Zählerregistrierung ein oder geben Sie im Feld **Aggregierter Wert** die Gesamtzählnummer ein.

- Wenn Sie einen neuen Zähler physisch auf einer Anlage installieren, müssen Sie die Änderung auf der Anlage in **Anlagenzähler** registrieren. Als nächstes müssen Sie zwei Registrierungszeilen mit identischen Zeitstempeln erstellen, und auf der Zeile mit dem neuen Zähler aktivieren Sie das Kontrollkästchen **Zähler zurücksetzen**. Wenn Sie die beiden Registrierungszeilen anlegen, muss die erste Zeile für den Zähler sein, den Sie ersetzen. Im Feld **Summen** ist die Gesamtzahl die Summe der Zählersumme aller registrierten Werte auf diesem Zählertyp.  
- Wenn das Kontrollkästchen **Zählerrückstellung** bei einer Anlage mit einem Wartungsplan mit Intervalltyp „Einmal von...“ oder „Einmal erreicht...“ aktiviert ist, ist der Zähler auf der neuen Zählerzeile weiterhin aktiv, da Sie eine separate Zählerzeile erstellen und mit einem neuen Zähler neu beginnen.

![Abbildung 1](media/11-work-orders.png)


Wenn Sie für mehrere Anlagen Gegenregistrierungen vornehmen müssen, kann dies in **Anlagenmanagement** > **Anfragen** > **Anlagen** > **Anlagenzähler** erfolgen.

>[!NOTE]
>Sie können einen Bereich einrichten, um Abweichungen bei manuellen Zählerregistrierungen zu definieren, und die Art der Meldung, die angezeigt werden soll, wenn Registrierungen außerhalb des definierten Bereichs liegen. Lesen Sie das Thema [Zähler](../setup-for-objects/counters.md) zur Einrichtung von Zählern.
