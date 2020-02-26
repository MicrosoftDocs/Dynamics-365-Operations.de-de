---
title: Einrichten von Strichcodemasken
description: In diesem Thema wird beschrieben, wie Strichcode-Maskenzeichen Strichcodemasken eingerichtet und wie Strichcodemasken zu Strichcodes zugeordnet werden.
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 265994
ms.assetid: 5831c74d-d2a1-4fa5-9a9a-a5aba8848381
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 89b63843daaa714d9141fc362c3d6fcb6ca9a91e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3024454"
---
# <a name="set-up-bar-code-masks"></a>Einrichten von Strichcodemasken

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Strichcode-Maskenzeichen Strichcodemasken eingerichtet und wie Strichcodemasken zu Strichcodes zugeordnet werden.

## <a name="set-up-bar-code-mask-characters"></a>Einrichten von Strichcode-Maskenzeichen

Strichcodemasken werden verwendet, um Strichcodes erstellen und Strichcodes schnell erkennen, die in die Verkaufsstelle (POS) gescannt werden. Masken bestehen aus Zeichen, die als Platzhalter auftreten, die das Format der Strichcodes angeben, die erstellt werden. Wenn Sie eine Strichcodemaske zu konfigurieren, müssen Ihnen Strichcode-Maskenzeichen einrichten. Navigieren Sie zu **Retail und Commerce** &gt; **Lagerverwaltung** &gt; **Strichcodes und Beschriftungen** &gt; **Maskenzeichen**. Klicken Sie auf **Neu**, um ein neues Strichcode-Maskenzeichen zu erstellen. Maskenzeichen können erstellt werden, um den nächsten Strichcodedaten anzugeben.

| Feld            | Beschreibung |
|------------------|-------------|
| Produkt          | Platzhalter für Produktkennung. |
| Beliebige Zahl       | Wird verwendet, um eine Zahl anzugeben, die in den Strichcode hartcodiert ist. |
| Prüfziffer      | Gibt an, dass das Strichcodeformat in eine Strichcodemaske eine Prüfziffer verwendet, um die die Gültigkeitsdauer eines Strichcodes zu bestätigen. |
| Größenziffer       | Gibt Größe in einem Strichcode angezeigt, die für eine ausgewählte Produktvariante erstellt wird, die Größe enthält. |
| Farbziffer      | Gibt Farbe in einem Strichcode angezeigt, die für eine ausgewählte Produktvariante erstellt wird, die Farbe enthält. |
| Stilziffer      | Gibt Stil in einem Strichcode angezeigt, die für eine ausgewählte Produktvariante erstellt wird, die Stil enthält. |
| EAN-Lizenzcode | Platzhalter für EAN-Lizenz ausgestellt für EAN-Lizenzcodes. |
| Preis            | Gibt Preis für Preis eingebettete Strichcodes an. |
| Leistung         | Gibt Menge in der Menge/zufälliges Gewicht eingebettete Strichcodes an. |
| Mitarbeiter         | Gibt Strichcodesegment für die Mitarbeiterkennung an, für die Anmeldung des Strichcodes POS verwendet wird. |
| Debitor         | Gibt das Debitorkennungssegment an. |
| Dateneintrag       | *Nicht implementiert* |
| Rabattcode    | *Veraltet* ab Dynamics 365 for Retail Frühjahr 2017 Version. Früher: Gibt den Skontocode für einen Strichcode an, der verwendet wird, um dem Rabatt eine Verkaufsstellenbuchung .hinzuzufügen |
| Couponcode      | Legt den Couponcode für einen Strichcode fest, der verwendet wird, um dem Rabatt einem Auftrag hinzuzufügen. Dies hat den Skontocode ersetzt. |
| Geschenkkarte        | Gibt eine Geschenkkartennummer beim Abgang oder Zahlung per Geschenkkarte an. |
| Treuekarte     | Fügt einen Debitor mit Kundentreue der Buchung hinzu und kann beim Zahlen nach Treue verwendet werden. |

## <a name="define-bar-code-masks"></a>Definieren von Strichcodemasken

Nachdem Strichcode-Maskenzeichen für die erforderlichen Strichcodemasken angegeben sind, wechseln Sie zu **Retail und Commerce** &gt; **Lagerverwaltung** &gt; **Strichcodes und Beschriftungen** &gt; **Strichcodemaske - Einstellungen**. Auf dieser Seite können Strichcodemasken können Sie definieren, durch die zuvor angegebenen Zeichen verwenden. Diese Strichcodemasken werden verwendet, wenn von Strichcodes, generiert und erleichtern außerdem, Strichcodes zu identifizieren, die am Point-of-Sale gescannt werden.

1. Klicken Sie auf **Neu**, um ein neues Strichcode-Maske zu erstellen.
2. Geben Sie Werte in **Maskenkennung** und **Beschreibung** ein, und wählen Sie dann eine Strichcodemaske Verbrauchstyp im **Typ** Feld aus.
3. Im Abschnitt **Allgemein** die Sie einen Wert im Feld **Strichcodestandard** Feld aus, und geben Sie den Strichcodepräfix an, sofern erforderlich.
4. Im Abschnitt **Strichcodemaskesegment** fügen Sie Strichcodesegmente hinzu, die in erstellt werden Strichcodes verwendet werden.

Als Beispiel eine Strichcodemaske mit Maskenkennung "Produkt" zu erstellen, geben Sie also Folgendes vor:

1. Erstellen Sie eine neue Strichcodemaske und wählen Sie geben "Produkt" aus.
2. Wählen Sie einen Strichcodestandard (z. B. "Code 39")
3. Stellen Sie einen Präfix bereit, um den Strichcode zu indenfizieren. Zum Beispiel, '22'.
4. Hinzufügen eines Maskensegment. Das "Produkt" Maskensegment ist aktiviert.
5. Erstellen Sie eine Länge für das Produktsegment, beispielsweise "10". Die Länge soll die Länge einer Produktkennung übereinstimmen, die im Shop bzw. am häufigsten verwendet wird. Mit einer Maske wird als Vorschau im Abschnitt **Allgemein** unter **Maske** angezeigt.

## <a name="assign-bar-code-masks-to-bar-codes"></a>Zuweisen von Strichcodemasken zu Strichcodes

Strichcodemasken müssen den Strichcodes zugewiesen werden, bevor sie verwendet werden können. Ausgehend vom vorherigen Beispiel, um die Strichcodemaske zu einem Strichcode zuzuweisen, gehen Sie folgendermaßen vor:

1. Wechseln Sie zu **Organisationsverwaltung** &gt; **Einrichtung** &gt; **Strichcodes**. Klicken Sie auf **Neu**.
2. Geben Sie Werte im Feld **Strichcode** **Einstellung** und **Einrichtung** ein.
3. Im Bereich **Allgemein** im **Strichcodetyp** Feld, wählen Sie "Code 39" aus. In der **Maske** **Kennung** Feld, wählen die zuvor erstellte "Produkt" Maske aus.
4. "Unter **Größe** geben Sie "12 "ein.
5. Klicken Sie auf **Speichern**.

Die kann nun Strichcodemaske verwendet werden, ob Strichcodes für Produkte erstellen. Die oben genannten Schritte sind Beispiele dazu, wie von Strichcodemasken für Produkte erstellt, doch sie werden auch, wie Strichcodemasken für alle anderen Strichcodetypen unterstützten erstellt. Strichcodemasken, Arten und Länge soll Verwendung in Ihrer Umgebung bestimmten angepasst werden.
