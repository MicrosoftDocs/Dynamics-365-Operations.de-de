---
title: Vorlagen laden
description: Dieser Artikel beschreibt, wie Sie Ladungsvorlagen festlegen und wie Sie eine Ladungsvorlage mit einer neuen Ladung verknüpfen.
author: Weijiesa
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 47b4925c528b64b835ce3e88659ee6ab0572eb2b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844179"
---
# <a name="load-templates"></a>Vorlagen laden

[!include [banner](../../includes/banner.md)]

Wenn Sie eine neue Ladung erstellen, können Sie eine Ladungsvorlage zuweisen. Die Beladungsvorlage enthält Informationen über das Equipment und über Kennzahlen wie Höhe, Breite, Tiefe und Volumen der Ladung.

Dieser Artikel beschreibt, wie Sie Ladungsvorlagen festlegen und wie Sie eine Ladungsvorlage mit einer neuen Ladung verknüpfen.

## <a name="set-up-a-load-template"></a>Festlegen einer Ladung-Vorlage

1. Gehen Sie zu **Transportverwaltung \> Einrichten \> Ladungserstellung \> Ladungsvorlage**.
1. Wählen Sie im Aktivitätsbereich **Neu**, um eine neue Vorlage hinzuzufügen oder **Bearbeiten**, um eine bestehende Vorlage zu bearbeiten.
1. Legen Sie in der Zeile für die neue oder vorhandene Vorlage die folgenden Felder fest:

    - **Ladevorlagen-ID** - Geben Sie einen eindeutigen Bezeichner (ID) für die Ladevorlage ein.
    - **Ausrüstung** - Wählen Sie die Ausrüstung, die für den Versand der Ladung verwendet werden soll.
    - **Ladungshöhe**, **Ladungsbreite** und **Ladungstiefe** - Geben Sie die Dimensionen der Ladung ein.
    - **Maximal zulässiges Ladevolumen** und **Maximal zulässiges Ladegewicht** - Geben Sie das maximal zulässige Volumen und Gewicht der Ladung ein.
    - **Maximal zulässiges Bruttogewicht** - Geben Sie das maximal zulässige Bruttogewicht der Ladung ein. Das Bruttogewicht einer Ladung beinhaltet sowohl das Taragewicht als auch das Ladegewicht.
    - **Maximal erlaubte Anzahl von Frachtstücken** - Geben Sie die maximale Anzahl von Frachtstücken ein, die die Ladung enthalten kann.
    - **Ladung auf dem Boden stapeln** - Aktivieren Sie dieses Kontrollkästchen, um eine Bodenladung zu verwenden. Bei einer Ladung auf dem Boden werden die Kisten innerhalb des Containers vom Boden bis zur Decke und von Wand zu Wand gestapelt, um die Kapazität zu maximieren.

1. Wählen Sie im Aktionsbereich **Speichern** aus.

## <a name="associate-a-load-template-with-a-new-load"></a>Verknüpfen einer Ladungsvorlage mit einer neuen Ladung

1. Gehen Sie zu **Transportverwaltung \> Planung \> Ladungsplanung Workbench**.
1. Wählen Sie im oberen Teil der Seite eine der folgenden Registerkarten, je nachdem, für welche Art von Quelldokument Sie eine Ladung erstellen: **Sendungen**, **Verkaufszeilen**, **Übertragungszeilen** oder **Einkaufsbestellungen**. 
1. Wählen Sie das spezifische Dokument aus, für das die Ladung geplant werden soll.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Angebot und Nachfrage** in der Gruppe **Hinzufügen** die Option **Zu neuer Ladung** aus.
1. Wählen Sie im Dialogfeld **Vorlage laden** im Feld **Vorlage-ID laden** die Vorlage, die Sie anwenden wollen.
1. Wählen Sie **OK**, um die Vorlage anzuwenden.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]