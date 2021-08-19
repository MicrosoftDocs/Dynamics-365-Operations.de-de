---
title: Klassen für Teilladungen (LTL)
description: Dieses Thema erklärt, was Less than Teilladung (LTL) Klassen sind und beschreibt, wie Sie diese in Microsoft Dynamics 365 Supply Chain Management festlegen.
author: Henrikan
ms.date: 04/05/2021
ms.topic: article
ms.search.form: WHSLTLClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 4349e649e48e5103a53a5e6ab332d127fd1de27aa7b06953533198d3928d250a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782370"
---
# <a name="less-than-truckload-ltl-classes"></a>Klassen für Teilladungen (LTL)

[!include [banner](../includes/banner.md)]

Eine Klasse für Teilladungen (LTL) ist eine Frachtversandklasse, die zur Klassifizierung von Elementen verwendet wird, die versendet werden können. Allgemein hat jede Art von Produkt oder Ware einen National Motor Freight Classification (NMFC) Code, der einer bestimmten Frachtklassennummer für LTL-Sendungen entspricht. LTL-Frachtklassen stellen Kategorien von Artikeln dar, während NMFC-Codes sich auf bestimmte Waren in jeder der 18 Frachtklassen beziehen.

Mit dieser Funktion können Sie mit Ihrem System die folgenden Aufgaben durchführen:

- Definieren Sie die LTL-Frachtklassen, die in Ihrer Firma verwendet werden.
- Weisen Sie jede LTL-Klasse einem NMFC-Code auf der Seite **NMFC-Codes** zu. Weitere Informationen finden Sie unter [National Motor Freight Classification (NMFC)-Codes](nmfc-codes.md).
- Weisen Sie jedem Produkt auf der Seite **Produkte** einen NMFC-Code (und damit den zugehörigen LTL-Code) zu.
- Schätzen Sie die LTL-Klasse jedes Produkts, dem ein NMFC-Code zugewiesen ist, genau ein.
- Ermittelt die Verpackungsanforderungen für jede LTL-Klasse durch Überprüfung der internationalen LTL-Standards. Auf diese Weise stellen Sie sicher, dass Ihre Produkte gut geschützt und sicher versandt werden.
- Erhalten Sie genaue Versandschätzungen, basierend auf der LTL-Frachtklasse für jedes Produkt.

Dieses Thema beschreibt, wie Sie LTL-Klassen in Microsoft Dynamics 365 Supply Chain Management erstellen.

## <a name="create-an-ltl-class"></a>Erstellen einer LTL-Klasse

Um eine LTL-Klasse zu erstellen, führen Sie diese Schritte aus.

1. Führen Sie einen dieser Schritte aus:

    - Gehen Sie zu **Lagerortverwaltung \> Einrichten \> Bestand \> LTL-Klassen**.
    - Gehen Sie zu **Transportverwaltung \> Einrichten \> Transportstandards \> LTL-Klassen**.

2. Wählen Sie im Aktivitätsbereich **Neu**, um eine LTL-Klasse zu erstellen. Legen Sie anschließend die folgenden Felder fest:

    - **LTL-Klasse** – Geben Sie die interne LTL-Klassen-Kennung (ID) Ihrer Firma für die Warenart ein. Die meisten Firmen verwenden den internationalen Standard. In diesem Fall stimmt der Wert dieses Feldes mit dem Wert des Feldes **Klasse** überein. Wenn Ihre Firma jedoch einen eigenen Standard verwendet, geben Sie einen Code ein, der mit diesem Standard übereinstimmt.
    - **Name** – Geben Sie einen beschreibenden Namen ein, der Ihnen und anderen Benutzern hilft, die richtige LTL-Klasse für jeden NMFC-Code auszuwählen.
    - **Klasse:** – Geben Sie die internationale Standard-LTL-Klassen-ID für die Warenart ein. Der Code, den Sie hier eingeben, muss mit dem offiziellen Standard übereinstimmen.

## <a name="example-set-up-ltl-classes"></a>Beispiel: LTL-Klassen festlegen

Das folgende Beispiel zeigt, wie Sie zwei verschiedene LTL-Klassen festlegen, die Sie mit unterschiedlichen Produkttypen verwenden können.

1. Gehen Sie zu **Lagerortverwaltung \> Einrichten \> Bestand \> LTL-Klassen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **LTL-Klasse:** *92.5*
    - **Name:** *Computer, Monitore, Kühlgeräte*
    - **Klasse:** *92.5*

1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Legen Sie die folgenden Werte für die neue Position fest:

    - **LTL-Klasse:** *125*
    - **Name:** *Kleine Haushaltsgeräte*
    - **Klasse:** *125*

1. Wählen Sie im Aktionsbereich **Speichern** aus.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [National Motor Freight Classification (NMFC)-Codes](nmfc-codes.md)
- [Frachtbrief erstellen](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
