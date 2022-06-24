---
title: GS1-Barcodes
description: Dieser Artikel beschreibt, wie Sie GS1-Barcodes und QR-Codes festlegen, damit Etiketten in einem Lager gescannt werden können.
author: Mirzaab
ms.date: 03/21/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 67c54f344ff7091f4a25198fdafa745c6c84d5d0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907144"
---
# <a name="gs1-bar-codes"></a>GS1-Barcodes

[!include [banner](../includes/banner.md)]

Arbeitskräfte im Lager müssen oft mehrere Aufgaben erledigen, wenn sie einen Scanner eines mobilen Geräts verwenden, um Bewegungen eines Artikels, einer Palette oder eines Containers zu registrieren. Diese Aufgaben können sowohl das Scannen von Barcodes als auch die manuelle Eingabe von Informationen auf dem mobilen Gerät umfassen. Die Barcodes verwenden ein firmenspezifisches Format, das Sie mithilfe von Microsoft Dynamics 365 Supply Chain Management definieren und verwalten.

GS1-Barcodes für Versandetiketten wurden entwickelt, um einen globalen Standard für den Datenaustausch zwischen Firmen zu schaffen. Sie sind sowohl in linearen (1D) Symbologien (Barcodeformaten) wie z. B. GS1-128 als auch in 2D-Symbologien wie GS1 DataMatrix und GS1 QR-Codes verfügbar. GS1-Barcodes kodieren nicht nur die Daten, sondern ermöglichen auch die Verwendung einer vordefinierten Liste von *Anwendungsbezeichnern*, um die Bedeutung der Daten zu definieren. Der GS1-Standard definiert das Datenformat und die verschiedenen Arten von Daten, die damit kodiert werden können. Im Gegensatz zu älteren Barcodestandards können GS1-Barcodes mehrere Datenelemente enthalten. Daher kann ein einziger Barcode-Scan mehrere Arten von Produktinformationen erfassen, z. B. die Batch und das Verfallsdatum.

Die GS1-Unterstützung im Supply Chain Management vereinfacht den Scan-Prozess in Lagern, in denen Paletten und Container mit Barcodes im GS1-Format gekennzeichnet werden, erheblich. Die Arbeitskräfte im Lager können alle erforderlichen Informationen durch einen einzigen Scan eines GS1-Barcodes extrahieren. Da die Notwendigkeit entfällt, mehrere Scans durchzuführen und/oder Informationen manuell einzugeben, tragen GS1-Barcodes dazu bei, die mit den Aufgaben verbundene Zeit zu reduzieren. Gleichzeitig helfen sie auch, die Genauigkeit zu verbessern.

Logistik-Manager müssen die erforderliche Liste von Anwendungskennungen festlegen und jede von ihnen mit den entsprechenden Menüpunkten des mobilen Geräts verknüpfen. Die Anwendungskennungen können dann lagerübergreifend als globale Einstellung für Umzugs- und Verpackungszwecke verwendet werden. Daher werden alle Versandetiketten ein einheitliches Formular haben.

Wenn nicht anders angegeben, wird in diesem Artikel der Begriff *Barcode* verwendet, der sich sowohl auf lineare 1D-Barcodes als auch auf 2D-Barcodes bezieht.

## <a name="the-gs1-bar-code-format"></a>Das GS1-Barcodeformat

Die allgemeinen GS1-Spezifikationen legen fest, welche Symbologien für GS1-Barcodes verwendet werden können und wie die Daten im Barcode kodiert werden. Dieser Abschnitt bietet eine kurze Einführung in den Artikel. Ausführliche Informationen finden Sie unter [Allgemeine GS1-Spezifikationen](https://www.gs1.org/docs/barcodes/GS1_General_Specifications.pdf), die von GS1 veröffentlicht werden. Das GS1-Spezifikationsdokument wird regelmäßig aktualisiert, und die darin enthaltenen Informationen sind auf dem neuesten Stand der Version 22.0 der allgemeinen GS1-Spezifikationen.

GS1-Barcodes verwenden die folgenden Symbologien:

- **Lineare oder 1D-Barcodes** – GS1-128 und GS1 DataBar
- **2D-Barcodes** – GS1 DataMatrix, GS1 QR-Code und GS1 Dotcode

Beachten Sie, dass GS1 in GS1-128 besondere Erwähnung findet. Dies ein Sonderfall des gewöhnlichen linearen Code-128-Barcodes, der GS1 DataMatrix und des GS1 QR-Codes ist. Der Unterschied zwischen der GS1-Version und der Nicht-GS1-Version ist das Vorhandensein eines Sonderzeichens (FNC1) als erstes Zeichen in den Barcodedaten. Das Vorhandensein eines FNC1-Zeichens gibt an, dass die Daten im Barcode gemäß der GS1-Spezifikation interpretiert werden sollten.

Die Daten im Barcode selbst bestehen aus mehreren Datenelementen, die jeweils durch eine Anwendungskennung am Anfang des Feldes identifiziert werden. Üblicherweise werden die Daten auch unter dem Barcode in einem für Menschen lesbaren Format dargestellt, wobei die Anwendungskennung in Klammern angezeigt wird. Hier ist ein Beispiel: `(01) 09521101530001 (17) 210119 (10) AB-123`. Dieser Barcode enthält drei Elemente:

- **Anwendungskennung 01** – Die GS1 Global Trade Item Number (GTIN) des Elements.
- **Anwendungskennung 17** – Das Ablaufdatum.
- **Anwendungskennung 10** – Die Chargennummer.

Für jedes Element können die Daten entweder eine vordefinierte oder eine variable Länge haben. Es gibt eine feste Liste von Anwendungskennungen mit vordefinierten Längen. Alle anderen Anwendungskennungen haben eine variable Länge. Die Liste der GS1-Anwendungskennungen gibt die maximale Länge und das maximale Datenformat an. Beispielsweise hat die Anwendungskennung 01 eine vordefinierte Länge von 16 Zeichen (zwei für die Anwendungskennung selbst und dann 14 für die GTIN), und die Anwendungskennung 17 hat eine vordefinierte Länge von acht Zeichen (zwei für die Anwendungskennung selbst und dann sechs für das Datum). Die Anwendungskennung 10 hat jedoch zwei Zahlen für die Anwendungskennung selbst und dann bis zu 20 alphanumerische Zeichen.

Wenn beim Zusammenfügen von Elementen ein Element auf ein Element mit variabler Länge folgt, muss ein Trennzeichen verwendet werden. Dieses Trennzeichen kann entweder das Sonderzeichen FNC1 oder das Gruppentrennzeichen sein (ein nicht druckbares Zeichen mit dem ASCII-Code 29 und dem Hexadezimalcode 1D). Das Trennzeichen sollte nicht nach dem letzten Element verwendet werden. Obwohl das Trennzeichen auch nicht nach Elementen mit vordefinierter Länge verwendet werden sollte, ist sein Vorhandensein kein kritischer Fehler.

In den Barcodedaten aus dem vorherigen Beispiel eines Barcodes, der die Anwendungskennungen 01, 17 und 10 enthält, werden die Daten in einem Code-128-, QR-Code- oder DataMatrix-Symbol als `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123` (Anwendungskennungen sind fett dargestellt) kodiert. Als Best Practice sollte jedes Element mit variabler Länge an das Ende gestellt werden, um die Notwendigkeit eines zusätzlichen Gruppentrennzeichens zu beseitigen. Der Barcode kann aber auch eine andere Reihenfolge der Elemente haben, wobei das Trennzeichen obligatorisch ist. Hier ist ein Beispiel: `<FNC1>`**`01`**`09521101530001`**`10`**`AB-123<GS>`**`17`**`210119`.

### <a name="dates-and-decimal-numbers"></a>Datumsangaben und Dezimalzahlen

Datumsangaben werden immer im Format *JJMMTT* dargestellt, wobei das Jahrhundert des Jahres durch die GS1-Spezifikationen bestimmt wird. Es können nur Datumswerte von 49 Jahren in der Vergangenheit bis 50 Jahren in der Zukunft (bezogen auf das aktuelle Jahr) dargestellt werden.

Einige Datenelemente enthalten Dezimalzahlen. Beispielsweise stellen die Anwendungskennungen 3100, 3101 ... 3105 ein Nettogewicht in Kilogramm dar. Da diese Anwendungskennungen eine vordefinierte Länge von 10 haben, stehen für die Menge sechs Ziffern zur Verfügung. Die Position des Dezimalkommas wird durch die letzte Ziffer der Applikationskennung angegeben. Daher kann diese Familie von Anwendungskennungen auch als *310n* dargestellt werden. Da der GS1-Standard vorschreibt, dass links vom Komma immer mindestens eine Zahl stehen muss, sind maximal fünf Nachkommastellen erlaubt.

Hier sind ein paar Beispiele, die zeigen, wie die Nummer *123456* von verschiedenen Anwendungskennungen (fett dargestellt) interpretiert wird:

- **`3100`**`123456` &rarr; 123456 (Ganzzahl)
- **`3101`**`123456` &rarr; 12345,6 (eine Dezimalstelle)
- **`3102`**`123456` &rarr; 1234,56 (zwei Dezimalstellen)
- **`3103`**`123456` &rarr; 123,456 (drei Dezimalstellen)
- **`3104`**`123456` &rarr; 12,3456 (vier Dezimalstellen)
- **`3105`**`123456` &rarr; 1,23456 (fünf Dezimalstellen)

## <a name="scanning-gs1-bar-codes-in-supply-chain-management"></a>Scannen von GS1-Barcodes im Supply Chain Management

Um GS1-Barcodes zu scannen, verwendet das Lagerpersonal einen Scanner, der in ein mobiles Gerät integriert oder mit diesem verbunden ist. Der Scanner überträgt dann den gescannten Barcode als eine Reihe von Tastaturereignissen an die mobile Warehouse Management-App. Diese Betriebsart wird auch als *Tastaturweiche (Keyboard Wedge)* oder *Weiche (Wedge)* bezeichnet. Die mobile App sendet dann den empfangenen Text unverändert an das Supply Chain Management. Wenn das System Eingabedaten empfängt, ermittelt es zunächst, ob die Daten mit einem der konfigurierten Präfixe beginnen, die angeben, dass es sich bei den Daten tatsächlich um einen GS1-Barcode handelt (siehe Abschnitt [Globale GS1-Optionen festlegen](#set-gs1-options)). Wenn die gescannten Daten mit einem dieser Präfixe beginnen, verwendet das System einen GS1-Parser, um die Daten zu analysieren und einzelne Datenelemente entsprechend ihrer Anwendungskennung zu extrahieren. Nachdem die Daten analysiert wurden, werden entweder das aktuelle Eingabefeld oder mehrere Felder mit den gescannten Daten ausgefüllt.

### <a name="configuration-of-bar-code-scanner-hardware-and-software"></a>Konfiguration von Barcodescanner-Hardware und -Software

Damit das Supply Chain Management GS1-Barcodes richtig erkennen und dekodieren kann, muss der Hardwarescanner oder die unterstützende Software so konfiguriert sein, dass die folgenden Aktionen ausgeführt werden:

- Hinzufügen eines Präfixes zu den gescannten Barcodes, damit das System einen GS1-Barcode erkennen kann.
- Konvertieren des nicht druckbaren ASCII-Gruppentrennzeichen (ASCII-Code 29 oder Hexadezimalcode 1D) in ein druckbares Zeichen, z. B. eine Tilde (~).

Sie können dem gescannten Barcode zwar ein beliebiges Präfix hinzufügen, eine Option besteht jedoch darin, eine ISO/IEC 15424-Symbologiekennung hinzuzufügen, die auch als *AIM-Kennung* bezeichnet wird. Diese dreistellige Kennung beginnt mit `]`, enthält dann ein Zeichen, das die verwendete Symbologie identifiziert, und danach eine Zahl, die als weiterer Modifikator verwendet wird. Zum Beispiel gibt die AIM-Kennung `]C1` einen Code 128-Barcode an (wegen des Zeichens `C`), und der Modifikator `1` gibt an, dass an der ersten Position der Daten ein FNC1-Zeichen steht. Auf der anderen Seite ist `]C0` ein Code 128-Barcode, der ein beliebiges anderes Zeichen als erstes Zeichen hat.

Die folgenden fünf Symbologiekennungen entsprechen GS1-Barcodes, die Anwendungskennungselemente enthalten:

- `]C1` – Code 128 (`C`) mit FNC1-Zeichen an erster Stelle (`1`), auch bekannt als GS1-128.
- `]e0` – GS1 DataBar.
- `]d2` – DataMatrix (`d`) mit ECC 200 und FNC1 an erster Stelle (`2`), auch bekannt als GS1 DataMatrix.
- `]Q3` – QR-Code (`Q`) Modell 2-Symbol mit FNC1 an erster Stelle (`3`), auch bekannt als GS1-QR-Code.
- `]J1` – GS1 DotCode.

Wenn Sie diese Kennungen verwenden, erfordert eine Kompatibilität mit Nicht-GS1-Barcodes, dass die Scanner oder die Scansoftware so konfiguriert werden, dass alle Kennungen entfernt werden, die nicht den GS1-Identifikatoren entsprechen. Wenn Sie zum Beispiel einen „normalen“ Code 39-Barcode scannen, wird das Präfix `]A0` hinzugefügt. Da das System dieses Präfix nicht als eines der GS1-Präfixe erkennt, interpretiert es das Präfix als Daten und erzeugt unerwartete Ergebnisse.

> [!NOTE]
> Der Einfachheit halber entfernen die Version 2.0.17.0 und höher der mobilen Warehouse Management-App alle AIM-Präfixe, die nicht in der vorherigen Liste enthalten sind. Dieses Verhalten unterstützt Fälle, in denen Sie den Scanner so konfigurieren können, dass er das AIM-Präfix hinzufügt, aber die unerwünschten Präfixe nicht entfernt.

### <a name="single-and-multiple-field-scanning"></a>Einzel- und Mehrfeldscannen

Nachdem die Daten aus dem Barcode analysiert wurden, werden sie in die Flow-Steuerung des Mobilgeräts eingespeist. Es gibt zwei Methoden, die der Reihe nach verarbeitet werden:

- **Einzelfeldscannen** – Diese Methode füllt nur das Feld aus, in das der Barcode gescannt wurde. Wenn Sie z. B. den Barcode `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123` scannen, während sich der Cursor im Feld **Artikel** befindet, wird die GTIN `09521101530001` aus dem Barcode in dieses Feld eingetragen. Wenn Sie den gleichen Barcode scannen, während sich der Cursor im Feld **Chargen-ID** befindet, wird die Chargennummer `AB-123` aus dem Barcode in dieses Feld eingetragen. Dieser Modus funktioniert für alle Felder in allen Flows und erfordert nur, dass die generische GS1-Einrichtung konfiguriert wird. Wenn ein Barcode mehrere Elemente enthält, muss er dennoch mehrmals gescannt werden, da jeweils nur ein Teil des Barcodes in den Flow des mobilen Geräts eingegeben wird. Dieses Verhalten wird durch das generische GS1-Setup gesteuert, wie im Abschnitt [Einrichten der generischen GS1 Einrichtung](#generic-gs1-setup) beschrieben.
- **Mehrfeldscannen** – Diese Methode füllt mehrere Felder aus, wenn ein Barcode gescannt wird, indem zusätzliche Daten in den Flow-Status des mobilen Geräts verschoben werden. Beispielsweise ist die Richtlinie so konfiguriert, dass die Anwendungskennung 01 in die Steuer- und Anwendungskennung 10 von `ItemId` im Feld `InventBatchId` verschoben wird. Wenn Sie den Barcode `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123`  scannen, werden Daten für beide Variablen gleichzeitig übertragen. Daher fordert Sie das System im Flow nicht zur Eingabe der Artikel- und/oder Chargennummer auf. Dieses Verhalten wird durch GS1-Richtlinien gesteuert, die mit Menüpunkten verknüpft sind, wie im Abschnitt [Festlegen von GS1-Richtlinien für Menüpunkte auf mobilen Geräten](#policies-for-menus) beschrieben.

> [!WARNING]
> Die standardmäßigen GS1-Richtlinien wurden getestet, sodass sie ohne unerwartetes Verhalten funktionieren. Die Anpassung von GS1-Richtlinien, die mit Menüpunkten verknüpft sind, kann jedoch trotzdem zu unerwartetem Verhalten führen, da der Flow möglicherweise nicht erwartet, dass einige Daten zu einem bestimmten Zeitpunkt verfügbar sind.

## <a name="turn-on-the-gs1-feature"></a>Einschalten der GS1-Funktion

Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden. Administratoren können mit den Einstellungen [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Module:** *Lagerortverwaltung*
- **Name der Funktion:** *Scannen von GS1-Barcodes*

### <a name="turn-on-the-enhanced-parser-for-gs1-barcodes-feature"></a>Aktivieren der Funktion „Erweiterter Parser“ für GS1-Barcodes

Wenn Sie GS1-Barcodes verwenden, empfehlen wir Ihnen, auch die Funktion *Erweiterten Parser für GS1-Barcodes* zu aktivieren. Diese Funktion bietet eine verbesserte Implementierung des GS1-Barcode-Parsers. Sie umfasst die folgenden Verbesserungen:

- Sie folgt dem Algorithmus der allgemeinen GS1-Spezifikation für die Analyse von Symboldaten und validiert, dass die Daten im Symbol gemäß der Spezifikation gültig sind.
- Es ist nicht erforderlich, dass Sie einen Wert für **Maximale Länge des Bezeichners** einrichten. Sie verwendet den längsten Präfixabgleich aus konfigurierten Anwendungskennungen.
- Sie können dezimale Anwendungskennungen einfacher konfigurieren, indem Sie den Buchstaben *n* verwenden, um eine beliebige Zahl abzugleichen. Beispielsweise können Sie nur eine Anwendungskennung konfigurieren (*310n*) anstelle separater Anwendungskennungen (*3101*, *3102*, *3103* und so weiter).
- Dies behebt ein Problem, bei dem falsch kodierte Daten als Felddaten interpretiert werden.
- Es handelt sich um eine separate Klasse, die in anderen Kontexten wiederverwendet werden kann und die Verwendung eines Erweiterungspunkts ermöglicht, um gescannte Daten zu manipulieren, bevor die Flow-Felder gefüllt werden.

## <a name="set-up-global-gs1-options"></a><a name="set-gs1-options"></a>Globale GS1-Optionen festlegen

Die Seite **Parameter der Lagerortverwaltung** bietet einige Einstellungen, die globale GS1-Optionen festlegen.

Um globale GS1-Optionen festzulegen, gehen Sie wie folgt vor.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerortverwaltungsparameter**.
1. Legen Sie auf dem Inforegister **Barcodes** die folgenden Felder fest:

    - **FNC1-Zeichen**, **Datamatrix-Zeichen** und **QR-Code-Zeichen** – Geben Sie Zeichen an, die für jeden GS1-Barcodetyp als Präfix interpretiert werden sollen.
    - **Gruppentrennzeichen** – Geben Sie das Zeichen an, welches das ASCII-Gruppentrennzeichen ersetzt.
    - **Maximale Länge des Bezeichners** - Geben Sie die maximale Anzahl von Zeichen an, die für den Anwendungsbezeichner zulässig ist. Dieses Feld ist nicht erforderlich, wenn die Funktion *Erweiterter GS1-Parser* in Ihrem System aktiviert ist.

> [!NOTE]
> Präfixe teilen dem System mit, dass ein Barcode nach dem GS1-Standard kodiert ist. Bis zu drei Präfixe (**FNC1-Zeichen**, **Datamatrix-Zeichen** und **QR-Code-Zeichen**) können gleichzeitig und für verschiedene Zwecke verwendet werden.

## <a name="gs1-application-identifiers"></a>GS1-Anwendungsbezeichner

GS1-Formate kodieren nicht nur die Daten, sondern ermöglichen auch die Verwendung einer vordefinierten Liste von Anwendungskennungen, um die Bedeutung der Daten zu definieren. Logistik-Manager müssen die erforderliche Liste von Anwendungskennungen festlegen und jede von ihnen mit den entsprechenden Menüpunkten des mobilen Geräts verknüpfen. Die Bezeichner können dann lagerübergreifend als globale Einstellung für Umzugs- und Verpackungszwecke verwendet werden. Daher werden alle Versandetiketten ein einheitliches Formular haben.

Das System verwendet die Daten, insbesondere die vordefinierten Anwendungskennungen, um die Regeln festzulegen, die auf die jeweilige gescannte Information angewendet werden sollen.

Jede Anwendungskennung signalisiert dem System, dass nachfolgende Zeichen im gescannten Barcode als ein Block verschlüsselter Informationen betrachtet werden sollen. Die Einrichtung der Applikationsbezeichner definiert, wie das System einen Barcode interpretieren und als Wert im System speichern soll.

Logistik-Manager können internationale Standard-Anwendungskennungen verwenden und/oder ihre eigenen erstellen.

### <a name="load-the-standard-application-identifiers"></a>Laden der Standard-Applikationsbezeichner

Um schnell loszulegen, können Sie eine Liste allgemeiner internationaler Anwendungskennungen laden. Sie können die Liste dann später nach Bedarf erweitern oder bearbeiten.

Um die Standard-Anwendungskennungen zu laden, gehen Sie folgendermaßen vor.

1. Gehen Sie zu **Lagerortverwaltung \> Einrichtung \> GS1 \> GS1 Anwendungskennungen**.
1. Wählen Sie im Aktionsbereich **Standardsetup erstellen** aus.

> [!WARNING]
> Der Befehl **Standardeinrichtung erstellen** löscht alle aktuell definierten Anwendungskennungen und ersetzt sie durch die Standardliste. Nachdem Sie die Standardeinrichtung geladen haben, können Sie die Liste jedoch an Ihre Bedürfnisse anpassen.

### <a name="set-up-custom-application-identifiers"></a>Angepasste Anwendungskennungen festlegen

Wenn einige oder alle Anwendungskennungen, die Ihre Firma verwendet, vom Standardsatz abweichen, können Sie Ihre eigenen Codes von Grund auf erstellen oder den Standardsatz nach Bedarf anpassen.

Um Ihre eigenen GS1-Anwendungskennungen festzulegen und anzupassen, führen Sie die folgenden Schritte aus.

1. Gehen Sie zu **Lagerortverwaltung \> Einrichtung \> GS1 \> GS1 Anwendungskennungen**.
1. Führen Sie einen dieser Schritte aus:

    - So erstellen Sie einen neuen Bezeichner: Wählen Sie im Aktionsbereich **Neu**.
    - Um einen vorhandenen Bezeichner zu bearbeiten: Wählen Sie den Bezeichner aus, und wählen Sie dann im Aktionsbereich **Bearbeiten**.

1. Legen Sie die folgenden Felder für den neuen oder ausgewählten Bezeichner fest:

    - **Anwendungsbezeichner** - Geben Sie den Identifikationscode für den Anwendungsbezeichner ein. Normalerweise ist dieser Code eine zweistellige Ganzzahl, er kann aber auch länger sein. Bei dezimalen Werten gibt die letzte Ziffer die Anzahl der Dezimalstellen an. Weitere Informationen finden Sie in der Beschreibung des Kontrollkästchens **Dezimal** weiter unten in dieser Liste. Wenn die Funktion *Erweiterter Parser für GS1-Barcodes* aktiviert ist, können Sie mithilfe des Buchstabens *n* als letztes Zeichen in der Anwendungskennung eine einzige Anwendungskennung für alle Dezimalstellenvarianten erstellen. Beispielsweise können Sie nur eine Anwendungskennung konfigurieren (*310n*) anstelle einer separaten Anwendungskennung für jede Anzahl an Dezimalstellen (*3101*, *3102*, *3103* und so weiter).
    - **Beschreibung** - Geben Sie eine kurze Beschreibung des Bezeichners ein.
    - **Feste Länge** - Aktivieren Sie dieses Kontrollkästchen, wenn Werte, die mit diesem Anwendungsbezeichner gescannt werden, eine feste Anzahl von Zeichen haben. Deaktivieren Sie dieses Kontrollkästchen, wenn die Länge der Werte variabel ist. In diesem Fall müssen Sie das Ende des Wertes mit dem Gruppentrennzeichen angeben, das Sie auf der Seite **Parameter der Lagerortverwaltung** festgelegt haben.
    - **Länge** - Geben Sie die maximale Anzahl der Zeichen ein, die in den Werten vorkommen können, die mit dieser Anwendungskennung gescannt werden. Wenn das Kontrollkästchen **Feste Länge** aktiviert ist, wird genau diese Anzahl von Zeichen erwartet.
    - **Typ** - Wählen Sie den Typ des Wertes, der mit dieser Anwendungskennung gescannt wird (*Numerisch*, *Alphanumerisch* oder *Datum*). Weitere Informationen darüber, wie Datumsangaben und Zahlen in Barcodedaten dargestellt werden, finden Sie im Abschnitt [Datumsangaben und Dezimalzahlen](#dates-and-decimal-numbers).
    - **Dezimal** - Aktivieren Sie dieses Kontrollkästchen, wenn der Wert ein implizites Dezimalkomma enthält. Wenn dieses Kontrollkästchen aktiviert ist, verwendet das System die letzte Ziffer des Anwendungsbezeichners, um die Anzahl der Dezimalstellen zu bestimmen. Weitere Informationen darüber, wie Datumsangaben und Zahlen in Barcodedaten dargestellt werden, finden Sie im Abschnitt [Datumsangaben und Dezimalzahlen](#dates-and-decimal-numbers).

> [!WARNING]
> Obwohl das System es Ihnen erlaubt, das Kontrollkästchen **Feste Länge** für eine beliebige Anwendungskennung zu aktivieren, sollte es nur für die Teilmenge von Anwendungskennungen verwendet werden, die gemäß den allgemeinen GS1-Spezifikationen eine vordefinierte Länge haben. Der erweiterte GS1-Parser enthält bereits die Liste aller Anwendungskennungen, die vordefinierte Längen haben.

> [!NOTE]
> Der **Gruppentrennzeichen**-Wert, der auf der Seite **Lagerverwaltungsparameter** angegeben ist, ist optional, wenn ein Wert, dem eine Anwendungskennung folgt, eine feste Länge hat.

## <a name="establish-the-generic-gs1-setup"></a><a name="generic-gs1-setup"></a>Einrichten der generischen GS1 Einrichtung

Die generische GS1 Einrichtung legt eine Sammlung von allgemeinen Zuordnungen fest. Diese Zuordnungen ordnen jedes relevante Eingabefeld in der Mobile-App dem Anwendungsbezeichner zu, der steuert, wie Werte von gescannten Barcodes in diesem Feld interpretiert und gespeichert werden sollen. Standardmäßig gelten diese Einstellungen für alle Scans für alle Menüelemente auf mobilen Geräten. Sie können jedoch für ein oder mehrere bestimmte Felder durch eine GS1-Richtlinie überschrieben werden, die einem bestimmten Menüelement zugewiesen ist.

Die generische GS1 Einrichtung lässt immer nur einen Wert zu, der gescannt werden kann. Wenn Sie also mehrere Feldwerte mit einem einzigen Scan laden möchten, müssen Sie eine GS1-Richtlinie für die entsprechenden Menüelemente festlegen.

Weitere Informationen zu GS1-Richtlinien finden Sie im nächsten Abschnitt.

### <a name="load-the-standard-generic-gs1-setup"></a>Laden der standardmäßigen generischen GS1 Einrichtung

Auf der Seite **Generisches GS1-Setup** können Sie eine Standardmenge von Zuordnungen zwischen Feldern des mobilen Geräts und Standard-Anwendungskennungen laden, die von der Standardeinrichtung erstellt werden.

Um das generische GS1-Setup einzurichten, gehen Sie auf **Lagerortverwaltung \> Einrichtung \> GS1 \> GS1 generisches Setup**. Wählen Sie dann **Standardeinrichtung erstellen**, um jedem Feld, das typischerweise von Menüpunkten auf mobilen Geräten verwendet wird, automatisch eine passende Anwendungskennung zuzuweisen.

> [!WARNING]
> Wenn bereits eine generische GS1 Einrichtung existiert, löscht der Befehl **Standardeinrichtung erstellen** diese vollständig und lädt die Standardeinrichtung.

### <a name="customize-the-standard-generic-gs1-setup"></a>Anpassen der generischen Standard-GS1-Einrichtung

Um die generische GS1 Einrichtung anzupassen, folgen Sie diesen Schritten.

1. Gehen Sie zu **Lagerortverwaltung \> Einrichtung \> GS1 \> GS1 generische Einrichtung**.
1. Führen Sie einen dieser Schritte aus:

    - So erstellen Sie eine neue Zuordnung: Wählen Sie im Aktionsbereich **Neu**.
    - So bearbeiten Sie eine vorhandene Zuordnung: Wählen Sie die Zuordnung aus und wählen Sie dann im Aktionsbereich **Bearbeiten**.

1. Legen Sie die folgenden Felder für die neue oder ausgewählte Zuordnung fest:

    - **Feld** - Wählen Sie das Eingabefeld der Mobile-App aus oder geben Sie es ein, dem der eingehende Wert zugewiesen werden soll. Der Wert ist nicht der Anzeigename, den die Arbeitskräfte sehen. Stattdessen ist es der Schlüsselname, der dem Feld im zugrunde liegenden Code zugewiesen wird. Die standardmäßige Einrichtung bietet eine Sammlung von Feldern, die wahrscheinlich nützlich sind, und enthält intuitive Schlüsselnamen für jedes Feld und passende programmierte Funktionalität. Möglicherweise müssen Sie jedoch mit Ihren Entwicklungspartnern sprechen, um die richtige Auswahl für Ihre Implementierung zu finden.
    - **Anwendungsbezeichner** - Wählen Sie den zutreffenden Anwendungsbezeichner, wie auf der Seite **GS1-Anwendungsbezeichner** definiert. Der Bezeichner legt fest, wie der Strichcode interpretiert und als Wert für das benannte Feld gespeichert wird. Nachdem Sie einen Anwendungsbezeichner ausgewählt haben, wird im Feld **Beschreibung** die Beschreibung des Bezeichners angezeigt.

## <a name="set-up-gs1-policies-to-be-to-mobile-device-menu-items"></a><a name="policies-for-menus"></a>Festlegen von GS1-Richtlinien für Menüpunkte auf mobilen Geräten

Der Zweck des GS1-Standards ist es, Arbeitskräften zu ermöglichen, mehrere Werte zu laden, wenn sie einen einzigen Barcode einmal scannen. Um diesen Zweck zu erreichen, müssen Logistik-Manager GS1-Richtlinien festlegen, die dem System mitteilen, wie mehrwertige Barcodes zu interpretieren sind. Später können Sie Richtlinien zu Menüelementen auf mobilen Geräten zuweisen, um zu steuern, wie ein Barcode interpretiert wird, wenn Arbeitskräfte ihn scannen, während sie ein bestimmtes Menüelement verwenden.

Wenn einem Menüelement keine GS1-Richtlinie zugewiesen ist, kann das System nur einen einzigen Wert erfassen. Dieser Wert wird auf die Eingabe der Mobile-App angewendet, die ausgewählt wird, wenn die Arbeitskraft den Scan vornimmt, wie in der generischen GS1 Einrichtung festgelegt. Wenn dem Menüelement eine GS1-Richtlinie zugewiesen ist, verwendet das System weiterhin das generische GS1-Setup, um den ersten Barcodewert dem ausgewählten Feld zuzuordnen. Es kann dann jedoch weitere Feldwerte erfassen, wie von der entsprechenden Richtlinie vorgegeben.

### <a name="load-the-standard-specific-gs1-policies"></a>Laden der standard-spezifischen GS1 Richtlinien

Um schnell loszulegen, können Sie eine Reihe von GS1-Richtlinien laden. Sie können die Richtlinien dann später je nach Bedarf erweitern oder bearbeiten.

Um die Standard-Anwendungskennungen zu laden, gehen Sie folgendermaßen vor.

1. Gehen Sie zu **Lagerortverwaltung \> Einrichtung \> GS1 \> GS1 Richtlinie**.
1. Wählen Sie im Aktionsbereich **Standardsetup erstellen** aus.

> [!WARNING]
> Der Befehl **Standard-Setup erstellen** löscht alle aktuell festgelegten Richtlinien und ersetzt sie durch den Standard-Richtliniensatz. Nachdem die Standardeinrichtung geladen ist, können Sie die Richtlinien jedoch nach Bedarf anpassen.

### <a name="set-up-custom-specific-gs1-policies"></a>Angepasste spezifische GS1-Richtlinien festlegen

> [!WARNING]
> Einige GS1-Richtlinien funktionieren möglicherweise nicht mit jedem mobilen Flow, den Sie verwenden. Wenn Sie angepasste GS1-Richtlinien konfigurieren, müssen Sie den Flow für mobile Geräte testen, indem Sie verschiedene Informationen verwenden, die an verschiedenen Punkten im Flow gescannt werden. Auf diese Weise können Sie feststellen, ob sich der Flow wie erwartet verhält.

Um Ihre GS1-Richtlinien festzulegen und anzupassen, gehen Sie folgendermaßen vor.

1. Gehen Sie zu **Lagerortverwaltung \> Einrichtung \> GS1 \> GS1 Richtlinie**.
1. Führen Sie einen dieser Schritte aus:

    - So erstellen Sie eine neue Richtlinie: Wählen Sie im Aktionsbereich **Neu**.
    - Um eine vorhandene Richtlinie zu bearbeiten: Wählen Sie die Richtlinie im Listenbereich aus.

1. Legen Sie in der Kopfzeile der neuen oder ausgewählten Richtlinie die folgenden Felder fest:

    - **Richtlinienname** - Geben Sie einen Namen für die Richtlinie ein.
    - **Beschreibung** - Geben Sie eine kurze Beschreibung für die Richtlinie ein.

1. Ordnen Sie im Inforegister unterhalb der Kopfzeile die Feldnamen den Anwendungsbezeichnern zu, wie es für die aktuelle Richtlinie erforderlich ist. Verwenden Sie die Schaltflächen in der Symbolleiste, um nach Bedarf Zeilen hinzuzufügen oder zu entfernen. Legen Sie für jede Position die folgenden Felder fest:

    - **Feld** - Wählen Sie das Eingabefeld der Mobile-App aus oder geben Sie es ein, dem der eingehende Wert zugewiesen werden soll. Der Wert ist nicht der Anzeigename, den die Arbeitskräfte sehen. Stattdessen ist es der Schlüsselname, der dem Feld im zugrunde liegenden Code zugewiesen wird. Die standardmäßige Einrichtung bietet eine Sammlung von Feldern, die wahrscheinlich nützlich sind, und enthält intuitive Schlüsselnamen für jedes Feld und passende programmierte Funktionalität. Möglicherweise müssen Sie jedoch mit Ihren Entwicklungspartnern sprechen, um die richtige Auswahl für Ihre Implementierung zu finden.
    - **Anwendungsbezeichner** - Wählen Sie den zutreffenden Anwendungsbezeichner, wie auf der Seite **GS1-Anwendungsbezeichner** definiert. Der Bezeichner legt fest, wie der Strichcode interpretiert und als Wert für das benannte Feld gespeichert wird. Nachdem Sie einen Anwendungsbezeichner ausgewählt haben, wird im Feld **Beschreibung** die Beschreibung des Bezeichners angezeigt.
    - **Sortierung** - Jeder mehrwertige Barcode enthält eine Reihe von Anwendungskennungen, denen jeweils ein Wert folgt. Die geltende GS1-Richtlinie legt fest, welcher Anwendungsbezeichner jedem Datenbankfeld zugeordnet wird. Wenn ein Barcode jedoch denselben Anwendungsbezeichner mehr als einmal verwendet, verwendet das System die Reihenfolge, in der die Anwendungsbezeichner im Code erscheinen, um sie den Feldern zuzuordnen. Für Zeilen, die einen Anwendungsbezeichner mit einer oder mehreren anderen Zeilen gemeinsam haben, verwenden Sie dieses Feld, um die Reihenfolge festzulegen, in der die übereinstimmenden Zeilen verarbeitet werden. Die Zeile, die den niedrigsten Sortierwert hat, wird zuerst verarbeitet.

> [!NOTE]
> Für Barcodes, die mehr als einen identischen Anwendungsbezeichner enthalten, *müssen* Sie das Feld **Sortierung** verwenden, um die Reihenfolge der Felder festzulegen.

## <a name="assign-gs1-policies-to-mobile-device-menu-items"></a>Zuweisen von GS1-Richtlinien zu Menüelementen auf mobilen Geräten

Standardmäßig bieten alle Menüelemente für mobile Geräte Eingabefelder, in denen die Arbeitskräfte einen einzelnen Wert scannen können, entsprechend der allgemeinen GS1 Einrichtung. Wenn Sie möchten, dass Arbeitskräfte mehr als einen Feldwert in einem einzigen Scanvorgang für ein beliebiges Menüelement eines mobilen Geräts scannen können, müssen Sie eine GS1-Richtlinie zuweisen, indem Sie die folgenden Schritte ausführen.

1. Gehen Sie zu **Lagerortverwaltung \> Einstellungen \> Mobiles Gerät \> Menüoptionen für mobiles Gerät**.
1. Erstellen oder öffnen Sie ein Menüelement.
1. Legen Sie auf dem Inforegister **Allgemein** das Feld **GS1-Richtlinie** auf die Richtlinie fest, die für das Menüelement gilt.

## <a name="gs1-setup-example"></a>Beispiel für die Einrichtung von GS1

Dieses Beispiel gilt für ein System, in dem die GS1-Optionen wie folgt festgelegt sind:

- Auf der Seite **Parameter für Lagerortverwaltung** werden die folgenden globalen Einstellungen festgelegt:

    - **FNC1-Zeichen:** *\]C1*
    - **Gruppentrennzeichen:** *\~*

- Auf der Seite **GS1-Anwendungskennzeichen** sind die folgenden Anwendungskennzeichen für dieses Beispiel relevant.

    | Anwendungskennung | Beschreibung | Feste Länge | Länge | Typ | Dezimal |
    |---|---|---|---|---|---|
    | 01 | GTIN | Ausgewählt | 14 | Numerisch | Verrechnet |
    | 10 | Chargennummer | Verrechnet | 20 | Alphanumerisch | Verrechnet |
    | 17 | Ablaufdatum | Ausgewählt | 6 | Datum | Verrechnet |
    | 30 | Empfangsmenge | Verrechnet | 8 | Numerisch | Verrechnet |

- Auf der Seite **GS1 generische Einrichtung** sind die folgenden Einstellungen für die generische GS1 Richtlinie für dieses Beispiel relevant.

    | Feld | Anwendungskennung | Beschreibung |
    |---|---|---|
    | ItemId | 01 | GTIN |

- Auf der Seite **GS1-Richtlinie** gibt es eine Richtlinie, bei der das Feld **Richtlinienname** auf *Einkaufsmenge* festgelegt ist. Diese Richtlinie enthält die folgenden Zeilen.

    | Feld | Anwendungskennung | Beschreibung | Sortieren |
    |---|---|---|---|
    | Ablaufdatum | 17 | Ablaufdatum | 0 |
    | InventBatchId | 10 | Chargennummer | 0 |
    | Mge | 30 | Empfangsmenge | 0 |

- Auf der Seite **Mobilgeräte-Menüpunkte** gibt es einen Menüpunkt, der den Namen *Empfang von Käufen* trägt. Sein Feld **GS1-Richtlinie** ist auf *Einkaufseingang* festgelegt.

Nachdem Waren für eine Bestellung im Lager eingetroffen sind, geht die Arbeitskraft wie folgt vor.

1. Wählen Sie auf dem mobilen Gerät den Menüpunkt **Einkaufsannahme**.
1. Geben Sie die Nummer der Bestellung ein.
1. Wählen Sie das Feld **Artikel** aus, und scannen Sie den folgenden Barcode: `]C10100000012345678~3030~10b1~17220215`.

Aufgrund der für dieses Beispiel festgelegten Einstellungen analysiert das System den gescannten Barcode auf folgende Weise.

| Feldschlüssel | Anwendungs-ID | Wert | Notiz |
|---|---|---|---|
| ItemId | 01 | 00000012345678 | Da die Arbeitskraft in das Feld **Element** gescannt hat, wird der erste Wert im Barcode diesem Feld zugeordnet. Die Zuordnung wird aus der generischen Einrichtung von GS1 übernommen. |
| Mge | 30 | 30 | Da mehrere Feldwerte in einem einzigen Scanvorgang erfasst werden, werden diese Zuordnung und alle übrigen Zuordnungen aus der GS1-Richtlinie übernommen, die dem Menüpunkt **Empfang** zugeordnet ist. Dieser Wert ist die Menge, die empfangen wurde. |
| InventBatchId | 10 | b1 | Bei diesem Wert handelt es sich um die Batch-ID. |
| Ablaufdatum | 17 | 220215 | Das Datumsformat ist JJMMTT. Daher ist das Verfallsdatum der 15. Februar 2022. |

Der Bon wird dann registriert, und die relevanten Datenbankwerte werden nach dem einmaligen Scannen eingegeben.
