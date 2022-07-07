---
title: Garantien auf Anlagen und Anlagearten
description: In diesem Artikel wird erläutert, wie Sie im Anlagenmanagement Garantien auf Anlagen und Anlagenarten einrichten.
author: johanhoffmann
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2e63161aa32ecbc99baace9bb0cc649aedc600ed
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015991"
---
# <a name="warranties-on-assets-and-asset-types"></a>Garantien auf Anlagen und Anlagearten

[!include [banner](../../includes/banner.md)]

 


In diesem Artikel wird erläutert, wie Sie im Anlagenmanagement Garantien auf Anlagen und Anlagenarten einrichten.

## <a name="set-up-a-warranty-on-an-asset-type"></a>Einrichten einer Garantie für eine Anlagenart

1. Wählen Sie **Anlageverwaltung** \> **Einstellungen** \> **Anlagentypen** \> **Anlagentypen** aus.
2. Wählen Sie im linken Bereich die Anlagenart aus, an die eine Garantievereinbarung des Lieferanten angehängt werden soll, und wählen Sie dann **Anlagentypvorgaben**.
3. Wählen Sie im Feld **Allgemein** FastTab im Feld **Lieferantengarantie** die Vereinbarung aus.

## <a name="set-up-a-warranty-on-an-asset"></a>Einrichten einer Garantie für eine Anlage

1. Wählen Sie **Anlagenverwaltung** \> **Anlagen** \> **Alle Anlagen**.
2. Wählen Sie die Anlage aus und wählen Sie dann **Bearbeiten**.
3. Wählen Sie auf der Registerkarte **Lieferant** FastTab im Abschnitt **Lieferantengarantie**, im Feld **Garantie** die Garantievereinbarung aus.
4. Wählen Sie in den Feldern **Garantiebeginn** und **Garantieende** das Start- und Enddatum aus.

    > [!IMPORTANT]
    > Wenn bei einem Arbeitsauftrag im Feld **Gewährleistungsbeginn** ein Datum ausgewählt wird, gilt die Garantie für den Arbeitsauftrag zu diesem Datum. Wenn Sie einen Arbeitsauftrag anlegen, wird das Feld **Garantiebeginn** automatisch auf das Erstellungsdatum gesetzt. Sie können das Datum jedoch so ändern, dass es z.B. dem Startdatum einer Garantievereinbarung entspricht.
    >
    > ![Arbeitsauftragsseite.](media/02-warranty.png)

> [!NOTE]
> Wenn Sie einen Arbeitsauftrag für eine Anlage anlegen, die unter eine Lieferantengarantie fällt, erhalten Sie eine Benachrichtigung über die Garantievereinbarung, wenn der Arbeitsauftrag ein voraussichtliches Startdatum innerhalb der Garantiezeit hat. Anschließend können Sie den Arbeitsauftrag nach Bedarf stornieren.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]