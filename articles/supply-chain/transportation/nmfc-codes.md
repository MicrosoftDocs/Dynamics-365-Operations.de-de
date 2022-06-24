---
title: National Motor Freight Classification (NMFC)-Codes
description: Dieser Artikel beschreibt, wie Sie mit National Motor Freight Classification (NMFC)-Codes in Microsoft Dynamics 365 Supply Chain Management arbeiten.
author: Weijiesa
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 522e4d4e26b04b5ca1dd317e433c5a20ff3cb12e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893264"
---
# <a name="national-motor-freight-classification-nmfc-codes"></a>National Motor Freight Classification (NMFC)-Codes

[!include [banner](../includes/banner.md)]

National Motor Freight Classification (NMFC)-Codes helfen Ihnen, Elemente zu klassifizieren, die versendet werden können. Der NMFC-Code ist eine Bezeichnung, die zur Gruppierung von Waren verwendet wird. Es ermöglicht Transportfirmen, Waren für den Versand zu bewerten, indem sie Elemente auf der Basis von Überlegungen wie LKW-Passform, Ladungsproblemen, Handhabungsproblemen und Verderblichkeit klassifizieren. Waren werden in eine von 18 Frachtklassen gruppiert, indem ein Zahlenbereich von 50 bis 500 verwendet wird. Die Klasse, in die eine Ware eingeteilt wird, basiert auf einer Bewertung von vier Transportmerkmalen: Dichte, Verstaubarkeit, Handhabung und Haftung. Zusammen bestimmen diese Merkmale die Transportfähigkeit der Ware.

Ein NMFC-Code ist mit jedem Versandelement für weniger als Teilladungen (LTL) verbunden. Zum Beispiel könnte einem Laptop ein NMFC zugewiesen werden, der mit 2,5 eingestuft ist, während elektrischen Kabeln ein NMFC zugewiesen werden könnte, der mit 65 eingestuft ist.

Diese Funktion kann Arbeitskräften helfen, NMFC-Codes zur Klassifizierung von LTL-Versandartikeln zu verwenden. Im Folgenden finden Sie einige Beispiele hierfür:

- Wenn Ihre Firma eine Frachtbeschreibung auf dem Frachtbrief (BOL) angibt, hat der Spediteur eine Vorstellung davon, worum es sich bei der Fracht handelt. Fracht ist eine wichtige Klassifizierung, da viele Firmen ihr gesamtes Geschäftsmodell auf die Arten von Fracht stützen, die sie versenden.
- Diese Klassifizierung kann für Ihre Firma wichtig sein, da sie zur Bestimmung der Kalkulation einer bestimmten Ladung verwendet wird.
- Ihre Firma kann die Rentabilität eines LTL-Logistik- und Transportunternehmens ermitteln.

Dieser Artikel beschreibt, wie Sie in Microsoft Dynamics 365 Supply Chain Management mit NMFC-Codes arbeiten können.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie NMFC-Codes erstellen können, müssen Sie alle LTL-Frachtklassen festlegen, die diesen zugeordnet werden müssen. LTL-Frachtklassen stellen Kategorien von Artikeln dar, während NMFC-Codes sich auf bestimmte Waren in jeder der 18 Frachtklassen beziehen. Weitere Informationen zum Arbeiten mit LTL-Klassen finden Sie unter [Klassen für weniger als Teilladungen (LTL)](ltl-class.md).

## <a name="create-an-nmfc-code"></a>Erstellen eines NMFC-Codes

Führen Sie diese Schritte aus, um einen NMFC-Code zu erstellen.

1. Führen Sie einen dieser Schritte aus:

    - Gehen Sie zu **Lagerortverwaltung \> Einrichten \> Bestand \> NMFC-Codes**.
    - Gehen Sie zu **Transportverwaltung \> Einrichten \> Transportstandards \> NMFC-Codes**.

1. Wählen Sie **Neu**, um einen NMFC-Code zu erstellen. Legen Sie anschließend die folgenden Felder fest:

    - **NMFC-Code** – Geben Sie den NMFC-Code für die Warenart ein.
    - **Name** – Geben Sie einen Namen für den NMFC-Code ein.
    - **LTL-Klasse** – Wählen Sie die LTL-Klasse, die mit dem NMFC-Code verbunden ist.
    - **BOL-Handling-Einheit** – Definieren Sie die Standard-Handling-Art für die Sendung.

## <a name="example-set-up-nmfc-codes"></a>Beispiel: NMFC-Codes festlegen

Das folgende Beispiel zeigt, wie Sie zwei verschiedene NMFC-Codes festlegen, die Sie mit verschiedenen Produkten verwenden können.

1. Gehen Sie zu **Lagerortverwaltung \> Einrichten \> Bestand \> NMFC-Codes**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **NMFC-Code:** *92.5*
    - **Name:** *Computer*
    - **LTL-Klasse:** *92.5*
    - **BOL-Handling-Einheit:** *Einheit*

1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **NMFC-Code:** *125*
    - **Name:** *Telefone*
    - **LTL-Klasse:** *125*
    - **BOL-Handling-Einheit:** *Einheit*

1. Wählen Sie im Aktionsbereich **Speichern** aus.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Klassen für weniger als Teilladung (LTL)](ltl-class.md)
- [Erstellen Sie einen Frachtbrief](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
