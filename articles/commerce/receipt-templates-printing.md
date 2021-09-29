---
title: Bonformate einrichten und entwerfen
description: Dieser Artikel beschreibt, Sie wie Sie Formularlayouts erstellen und ändern, um zu steuern, wie Bons, Rechnungen und andere Dokumente gedruckt werden. Dynamics 365 Commerce umfasst einen Formularlayout-Designer, mit dem Sie einfach verschiedene Formularlayouts erstellen und ändern können.
author: rubencdelgado
ms.date: 09/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFormLayout
audience: Application User
ms.reviewer: josaw
ms.custom: 57841
ms.assetid: e530dd8e-95e2-4021-90bd-ce1235f9e250
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a2107670cb5dbac3b8f28c4e3caa357102932291
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500169"
---
# <a name="set-up-and-design-receipt-formats"></a>Bonformate einrichten und entwerfen

[!include [banner](includes/banner.md)]

Dieser Artikel beschreibt, Sie wie Sie Formularlayouts erstellen und ändern, um zu steuern, wie Bons, Rechnungen und andere Dokumente gedruckt werden. Dynamics 365 Commerce umfasst einen Formularlayout-Designer, mit dem Sie einfach verschiedene Formularlayouts erstellen und ändern können.

> [!IMPORTANT]
> Formularlayouts und Bonprofile müssen eingerichtet werden, um Bons und andere Dokumente in Retail Modern POS und Cloud POS ausdrucken zu können. Sie können mehrere Formularlayouts in ein Bonprofil einfügen. Sie können dann das Bonprofil einem Drucker zuweisen, indem Sie ein Hardwareprofil ändern.

## <a name="set-up-a-receipt-format"></a>Einrichten eines Bonformats

1. Klicken Sie auf **Einzelhandel und Handel** &gt; **Kanaleinrichtung** &gt; **POS-Einrichtung** &gt; **POS** &gt; **Bonlayouts**.
2. Klicken Sie auf der Seite **Bonlayout** auf **Neu**, um ein neues Formularlayout zu erstellen oder ein vorhandenes Formularlayout auszuwählen.
3. Geben Sie im Feld **Bonlayout** eine Kennung für das Formularlayout ein, und wählen Sie anschließend den Bontyp aus, für den dieses Layout verwendet wird. Sie können auch eine Beschreibung und einen Kurznamen für den Bon in das Feld **Titel** eingeben.
4. Wählen Sie auf dem Inforegister **Allgemein** eine Option aus, um das Druckverhalten zu definieren:

    - **Immer drucken** - Der Bon wird automatisch je nach Bedarf gedruckt.
    - **Nicht drucken** - Der Bon wird nicht gedruckt.
    - **Bedienerführung für Benutzer** - Der Benutzer wird aufgefordert, den Bon zu drucken.
    - **Nach Bedarf** - Diese Option wird nur für Geschenkbons verwendet. Wenn diese Option aktiviert ist, kann der Benutzer einen Geschenkbon auf der Seite **Änderung** drucken, wenn ein Geschenkbon erforderlich ist.

## <a name="print-images"></a>Bilder drucken

Der Belegdesigner enthält eine **Logo**-Variable. Sie können diese Variable verwenden, um ein Bild anzugeben, das auf Belegen gedruckt werden soll. Bilder, die durch die **Logo**-Variable auf Belegen gedruckt werden, sollten ein monochromer Bitmap-Dateityp (.bmp) sein. Wenn im Belegdesigner ein Bitmap-Bild angegeben ist, aber beim Senden des Belegs an den Drucker nicht gedruckt wird, kann eines der folgenden Probleme die Ursache sein:

- Die Dateigröße ist zu groß oder die Pixelabmessungen des Bildes sind nicht mit dem Drucker kompatibel. Versuchen Sie in diesem Fall, die Auflösung oder die Abmessungen der Bilddatei zu reduzieren.
- Einige Object Linking and Embedding for Point of Sale (OPOS)-Druckertreiber implementieren die **PrintMemoryBitmap**-Methode, die Hardwarestationen zum Drucken von Logobildern verwenden. Versuchen Sie in diesem Fall, der Datei **HardwareStation.Extension.config** die folgende Markierung Ihrer dedizierten oder gemeinsam genutzten Hardwarestation hinzuzufügen:

    `<add name="HardwareStation.UsePrintBitmapMethod" value="true"/>`

## <a name="design-a-receipt-format"></a>Entwerfen eines Bonformats

Mit dem Designer für Formularlayout können Sie das Layout des Formulardokuments grafisch erstellen. Die Seite **Designer für Bonformat** hat drei Abschnitte: **Kopfzeile**, **Positionen** und **Fußzeile**. Bei einigen Formularlayouttypen werden Elemente aus allen drei Abschnitten werden, bei anderen nur Elemente aus einem oder zwei der Abschnitte. Klicken Sie zum Anzeigen der verfügbaren Elemente für jeden Abschnitt auf die entsprechende Schaltfläche im Navigationsbereich links auf der Seite.

1. Klicken Sie auf **Einzelhandel und Handel** &gt; **Kanaleinrichtung** &gt; **POS-Einrichtung** &gt; **POS** &gt; **Bonlayouts**.
2. Wählen Sie auf der Seite **Bonlayout** ein Formularlayout aus, und klicken Sie anschließend auf **Designer**.
3. Klicken Sie auf **Ausführen**, um mit der Installation des Commerce-Designer-Hosts zu beginnen.
4. Klicken Sie auf der Benachrichtigungsleiste, die unten im Internet Explorer-Fenster angezeigt wird, auf **Öffnen**, um den Ein-Klick-Designer zu starten. (Die Benachrichtigungsleiste wird möglicherweise an einem anderen Speicherort in anderen Browsern.) Anhand der Statusleiste wird der Fortschritt des Installationsvorgangs angezeigt.
5. Nachdem die Installation abgeschlossen ist, geben Sie Ihren Benutzernamen und Ihr Kennwort für Commerce ein, und klicken Sie auf **Anmelden**, um den Designer zu starten.
6. Nachdem die Anmeldeinformationen validiert wurden und der Designer gestartet wurde, können Sie damit beginnen, das Bonlayout zu entwerfen oder ein vorhandenes Layout zu ändern.
7. Wählen Sie zum Erstellen der Elemente des Formulars den Abschnitt **Kopfzeile**, **Positionen** oder **Fußzeile** aus, und ziehen Sie dann ein Element aus diesem Abschnitt in den Arbeitsbereich. Die meisten Elemente enthalten Variablen, die automatisch mit Daten aus der Datenbank aufgefüllt werden. Andere Elemente (z. B. **Text**) ermöglichen das Drucken eines benutzerdefinierten Texts auf den Bon.

    > [!NOTE]
    > Sie können angeben, über wie viele Zeilen sich jeder Abschnitt erstreckt, indem Sie die Zahl in der unteren rechten Ecke dieses Abschnitts anpassen. Um das Ändern eines Abschnitts zu vereinfachen, vergrößern Sie seine Höhe, indem Sie unten im Abschnitt an der Größenänderungsleiste ziehen. Die Höhe des Abschnitts im Arbeitsbereich hat keinen Einfluss auf die Anzahl von Zeilen auf dem tatsächlichen Bon.

8. Nachdem Sie ein Element in den Arbeitsbereich gezogen haben, legen Sie im Bereich **Objektinformationen** unten auf der Seite die Eigenschaften für den Abschnitt fest. Geben Sie eine oder mehrere der folgenden Einstellungen ein:

    - **Ausrichten** – Legen Sie die Ausrichtung des Felds auf **Links** oder **Rechts** fest.
    - **Füllzeichen** – Geben Sie das Leerzeichen an. Standardmäßig wird ein Leerzeichen verwendet, Sie können aber ein beliebiges Zeichen eingeben.
    - **Präfix** – Geben Sie den Wert ein, der am Anfang des Felds angezeigt wird. Diese Einstellung trifft nur auf den Abschnitt **Positionen** des Layouts zu.
    - **Zeichen** - Geben Sie die maximale Anzahl von Zeichen an, die das Feld enthalten kann, wenn das Element eine Variable aufweist. Wenn der Text im Feld länger ist als die angegebene Anzahl von Zeichen, wird er abgeschnitten, damit er in das Feld passt.
    - **Variable** – Dieses Kontrollkästchen wird automatisch aktiviert, wenn das Element eine Variable enthält und nicht angepasst werden kann.
    - **Schrifttyp** – Legen Sie den Schriftschnitt auf **Normal** oder **Fett** fest. Fett formatierte Buchstaben nehmen doppelt so viel Platz ein wie normal formatierte Buchstaben. Daher werden einige Zeichen möglicherweise abgeschnitten.
    - **Schriftgröße** – Legen Sie die Schrittgröße auf **Normal** oder **Groß** fest. Große Buchstaben sind zwei Mal größer als reguläre Zeichen. Daher kann die Verwendung von großen Buchstaben zu überlappendem Text im Empfang führen.
    - **Löschen** – Klicken Sie auf diese Schaltfläche, um den ausgewählten Bereich aus dem Formularlayout zu entfernen.

## <a name="assign-receipt-profiles"></a>Zuweisen von Bonprofilen

Bonprofile werden durch das Hardwareprofil direkt zu den Druckern zugewiesen.

1. Öffnen Sie das Hardwareprofil, indem Sie auf **Einzelhandel und Handel** &gt; **Kanaleinrichtung** &gt; **POS-Einrichtung** &gt; **POS-Profile** &gt; **Hardwareprofil** klicken.
2. Wählen Sie den Drucker aus, und weisen Sie dann im Feld **Bonprofil** das Bonprofil zu, das im Register verwendet werden soll.

> [!NOTE]
> Wenn zwei Drucker verwendet werden, kann ein Drucker verwendet werden, um standardmäßige Thermobons mit 40 Spalten zu drucken. Der zweite Drucker wird in der Regel verwendet, um ganzseitige Bontypen zu drucken, die weitere Informationen enthalten. Zu diesen Bontypen gehören Bons für Debitorenaufträge und Debitorenrechnungen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
