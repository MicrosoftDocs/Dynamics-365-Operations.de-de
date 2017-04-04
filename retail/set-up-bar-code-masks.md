---
title: Einrichten von Strichcodemasken
description: In diesem Thema wird beschrieben, wie, Strichcode-Maskenzeichen Strichcodemasken eingerichtet und wie Strichcodemasken zu Strichcodes zugeordnet werden.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 265994
ms.assetid: 5831c74d-d2a1-4fa5-9a9a-a5aba8848381
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fe598799d52cacd84da775ac7ace8cf9a30ae5fe
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-bar-code-masks"></a>Einrichten von Strichcodemasken

In diesem Thema wird beschrieben, wie, Strichcode-Maskenzeichen Strichcodemasken eingerichtet und wie Strichcodemasken zu Strichcodes zugeordnet werden.

<a name="set-up-bar-code-mask-characters"></a>Einrichten von Strichcode-Maskenzeichen
-------------------------------

Strichcodemasken sind, um Strichcodes erstellen und Strichcodes verwendet schnell erkennen, die in die Verkaufsstelle (POS) gescannt werden. Masken werden von Zeichen enthalten, die als Platzhalter auftreten, die das Format der Strichcodes angeben, die erstellt werden. Wenn Sie eine Strichcodemaske zu konfigurieren, müssen Ihnen Strichcode-Maskenzeichen einrichten. Geht ** Einzelhandel und Handel ** &gt; ** Lagerverwaltung ** &gt; ** Strichcodes und Beschriftungen ** &gt; ** ** Maskenzeichen. ** Auf neu ** dem von Strichcode-Maskenzeichen. Mit Maskenzeichen können erstellt werden, um den nächsten Strichcodedaten anzugeben.

|                      |                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------|
| **Field**            | **Description**                                                                                                 |
| **Product**          | Platzhalter für Produktkennung.                                                                                     |
| **Any number**       | Wird verwendet, um eine Zahl anzugeben, die in den Strichcode hartcodiert ist.                                                  |
| **Check digit**      | Gibt an, dass das Strichcodeformat in eine Strichcodemaske eine Prüfziffer verwendet, um die die Gültigkeitsdauer eines Strichcodes zu bestätigen. |
| **Size digit**       | Gibt Größe in einem Strichcode angezeigt, die für eine ausgewählte Produktvariante erstellt wird, die Größe enthält.                                 |
| **Color digit**      | Gibt Farbe in einem Strichcode angezeigt, die für eine ausgewählte Produktvariante erstellt wird, die Farbe enthält.                               |
| **Style digit**      | Gibt Stil in einem Strichcode angezeigt, die für eine ausgewählte Produktvariante erstellt wird, die einen Stil enthält.                             |
| **EAN license code** | Platzhalter für EAN-Lizenz ausgestellt für EAN-Lizenzcodes.                                                       |
| **Preis**            | Gibt Preis für Preis eingebettete Strichcodes an.                                                                   |
| **Quantity**         | Gibt Menge in der Spalte " Abzuschließende Menge/zufälliges Gewicht eingebettete Strichcodes an.                                                |
| **Employee**         | Gibt Strichcodesegment für die Mitarbeiterkennungs Nummer an, für die Anmeldung des Strichcodes POS verwendet wird.                                  |
| **Customer**         | Gibt Debitorkennungssegment angezeigt.                                                                                  |
| ** Dateneingabe **       | *Not dennoch implemented.*                                                                                          |
| **Discount code**    | Gibt Skontocode einen Strichcode für an, der verwendet wird, um dem Rabatt eine Verkaufsstellenbuchung hinzuzufügen             |
| **Geschenkkarte**        | Gibt eine Geschenkkartennummer beim Abgang oder Zahlung per Geschenkkarte an.                                               |
| **Loyalty card**     | Fügt einen Debitor mit Kundentreue der Buchung hinzu und kann beim Zahlen nach Treue verwendet werden.                             |

## <a name="define-bar-code-masks"></a>Definieren von Strichcodemasken
Nachdem Strichcode-Maskenzeichen für die erforderlichen Strichcodemasken angegeben sind, geht ** Einzelhandel und Handel ** ** &gt; Lagerverwaltung ** ** &gt; Strichcodes und Beschriftungen ** ** &gt; die Strichcodemaske ** eingerichtet. Auf dieser Seite können Strichcodemasken können Sie definieren, durch die die Flugkosten zuvor angegebenen Zeichen verwenden. Strichcodemasken Diese werden verwendet, wenn von Strichcodes, generiert und erleichtern außerdem, Strichcodes zu identifizieren, die am Point-of-Sale gescannt werden.

1.  ** Auf neu ** um eine neue Strichcodemaske.
2.  Geben Sie Werte in ** Maskenkennung ** und ** Beschreibung ** den Feldern ein, und wählen Sie dann eine Strichcodemaske Verbrauchstyp im ** Typ ** Feld aus.
3.  ** ** Allgemein im Abschnitt die Sie einen Wert im Feld ** Strichcodestandard ** Feld aus, und geben Sie den Strichcodepräfix an, sofern erforderlich.
4.  Im Abschnitt Strichcodemaskesegment ** ** fügen Sie Strichcodesegmente hinzu, die in erstellt werden Strichcodes verwendet werden.

Als Beispiel eine Strichcodemaske mit Maskenkennung "Produktdimensionsgruppen" zu erstellen, geben Sie also Folgendes vor:

1.  Erstellen Sie eine neue Strichcodemaske und wählen Sie geben "Produktdimensionsgruppen" aus.
2.  Strichcodestandard Wählen Sie einen Code (beispielsweise "39" aus.
3.  Erstellen Sie hier das ein, das zur Verfügung den Strichcode vereinfacht das Identifizieren, Präfix verwendet werden. Beispielsweise "22 ".
4.  Hinzufügen eines Maskensegment hinzu. Das "Produkt" Maskensegment ist aktiviert.
5.  Erstellen Sie eine Länge für das Produktsegment beispielsweise " 10 "angegeben. Die Länge soll die Länge einer Produktkennung übereinstimmen, die im Shop bzw. am häufigsten verwendet wird. Mit einer Maske wird als Vorschau ** ** Allgemein im Abschnitt unter angezeigt ** Maske **.

## <a name="assign-bar-code-masks-to-bar-codes"></a>Zuweisen von Strichcodemasken zu Strichcodes
Strichcodemasken müssen den Strichcodes zugewiesen werden, bevor sie verwendet werden können. Ausgehend vom vorherigen Beispiel, um die Strichcodemaske zu einem Strichcode zuzuweisen, gehen Sie folgendermaßen vor:

1.  Wechseln ** Organisationsverwaltung ** ** &gt; Einstellungen ** ** &gt; Strichcodes **. ** Auf neu ** um ein neuen Strichcodes erstellen.
2.  Geben Sie Werte in ** Strichcode ** ** Einstellungen ** und ** Einstellungen ** die Felder ein.
3.  ** Allgemein ** Im Bereich im ** Strichcodetyp ** Feld, wählen Sie Code "39" aus. In der Maske ** ** ** Kennung ** Feld, wählen "die zuvor erstellte Produkt" Maske aus.
4.  ** Die Größe **, geben Sie "12 "ein.
5.  Click **Save**.

Die kann nun Strichcodemaske verwendet werden, ob Strichcodes für Produkte erstellen. Die oben genannten Schritte sind Beispiele dazu, wie von Strichcodemasken für Produkte erstellt, doch sie werden auch, wie Strichcodemasken für alle anderen Strichcodetypen unterstützten erstellt. Strichcodemasken, Arten und Länge soll Verwendung in Ihrer Umgebung bestimmten angepasst werden.


