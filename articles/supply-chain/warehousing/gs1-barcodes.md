---
title: GS1-Barcodes und QR-Codes
description: Dieses Thema beschreibt, wie Sie GS1-Barcodes und QR-Codes festlegen, damit Etiketten in einem Lager gescannt werden können.
author: Mirzaab
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 8f438e18356a6c16cc75bb59153ae7353d984a5a
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500329"
---
# <a name="gs1-bar-codes-and-qr-codes"></a>GS1-Barcodes und QR-Codes

[!include [banner](../includes/banner.md)]

Arbeitskräfte im Lager müssen oft mehrere Aufgaben erledigen, wenn sie einen Scanner eines mobilen Geräts verwenden, um Bewegungen eines Artikels, einer Palette oder eines Containers zu registrieren. Diese Aufgaben können sowohl das Scannen von Barcodes als auch die manuelle Eingabe von Informationen auf dem mobilen Gerät umfassen. Die Barcodes verwenden ein firmenspezifisches Format, das Sie mithilfe von Microsoft Dynamics 365 Supply Chain Management definieren und verwalten.

GS1 Barcode- und QR-Code-Formate für Versandetiketten wurden entwickelt, um einen globalen Standard für den Datenaustausch zwischen Firmen zu schaffen. GS1-Formate kodieren nicht nur die Daten, sondern ermöglichen auch die Verwendung einer vordefinierten Liste von *Anwendungsbezeichnern*, um die Bedeutung der Daten zu definieren. Der GS1-Standard definiert das Datenformat und die verschiedenen Arten von Daten, die damit kodiert werden können. Im Gegensatz zu älteren Barcodes können GS1-Barcodes mehrere Datenelemente enthalten. Daher kann ein einziger Barcode-Scan mehrere Arten von Produktinformationen erfassen, z. B. die Batch und das Verfallsdatum.

Die GS1-Unterstützung im Supply Chain Management vereinfacht den Scan-Prozess in Lagern, in denen Paletten und Container mit Codes im GS1-Format gekennzeichnet werden, erheblich. Die Arbeitskräfte im Lager können alle erforderlichen Informationen durch einen einzigen Scan eines GS1-Barcodes extrahieren. Da die Notwendigkeit entfällt, mehrere Scans durchzuführen und/oder Informationen manuell einzugeben, tragen GS1-Barcodes dazu bei, die mit den Aufgaben verbundene Zeit zu reduzieren. Gleichzeitig helfen sie auch, die Genauigkeit zu verbessern.

Logistik-Manager müssen die erforderliche Liste von Anwendungskennungen festlegen und jede von ihnen mit den entsprechenden Menüpunkten des mobilen Geräts verknüpfen. Die Anwendungskennungen können dann lagerübergreifend als globale Einstellung für Umzugs- und Verpackungszwecke verwendet werden. Daher werden alle Versandetiketten ein einheitliches Formular haben.

Wenn nicht anders angegeben, wird in diesem Thema der Begriff *Barcode* verwendet, der sich sowohl auf Barcodes als auch auf QR-Codes bezieht.

## <a name="turn-on-the-gs1-feature"></a>Einschalten der GS1-Funktion

Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden. Administratoren können mit den Einstellungen [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Module:** *Lagerortverwaltung*
- **Name der Funktion:** *Scannen von GS1-Barcodes*

## <a name="set-up-global-gs1-options"></a>Globale GS1-Optionen festlegen

Die Seite **Parameter der Lagerortverwaltung** bietet einige Einstellungen, die globale GS1-Optionen festlegen.

Um globale GS1-Optionen festzulegen, gehen Sie wie folgt vor.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerortverwaltungsparameter**.
1. Legen Sie auf dem Inforegister **Barcodes** die folgenden Felder fest:

    - **FNC1-Zeichen** - Geben Sie Zeichen an, die beim Parsen eines Barcodes als Präfix interpretiert werden sollen.
    - **Datamatrix-Zeichen** - Legen Sie Zeichen fest, die als Präfix interpretiert werden sollen, wenn eine Datamatrix geparst wird.
    - **QR-Code-Zeichen** - Legen Sie Zeichen fest, die beim Parsen eines QR-Codes als Präfix interpretiert werden sollen.
    - **Gruppentrennzeichen** - Geben Sie das Zeichen an, das getrennte Teile eines Strichcodes oder QR-Codes kennzeichnet.
    - **Maximale Länge des Bezeichners** - Geben Sie die maximale Anzahl von Zeichen an, die für den Anwendungsbezeichner zulässig ist.

> [!NOTE]
> Präfixe teilen dem System mit, dass ein Barcode nach dem GS1-Standard verschlüsselt ist. Bis zu drei Präfixe (**FNC1-Zeichen**, **Datamatrix-Zeichen** und **QR-Code-Zeichen**) können gleichzeitig und für verschiedene Zwecke verwendet werden.

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

    - **Anwendungsbezeichner** - Geben Sie den Identifikationscode für den Anwendungsbezeichner ein. Normalerweise ist dieser Code eine zweistellige Ganzzahl, er kann aber auch länger sein. Bei dezimalen Werten gibt die letzte Ziffer die Anzahl der Dezimalstellen an. Weitere Informationen finden Sie in der Beschreibung des Kontrollkästchens **Dezimal** weiter unten in dieser Liste.
    - **Beschreibung** - Geben Sie eine kurze Beschreibung des Bezeichners ein.
    - **Feste Länge** - Aktivieren Sie dieses Kontrollkästchen, wenn Werte, die mit diesem Anwendungsbezeichner gescannt werden, eine feste Anzahl von Zeichen haben. Deaktivieren Sie dieses Kontrollkästchen, wenn die Länge der Werte variabel ist. In diesem Fall müssen Sie das Ende des Wertes mit dem Gruppentrennzeichen angeben, das Sie auf der Seite **Parameter der Lagerortverwaltung** festgelegt haben.
    - **Länge** - Geben Sie die maximale Anzahl der Zeichen ein, die in den Werten vorkommen können, die mit dieser Anwendungskennung gescannt werden. Wenn das Kontrollkästchen **Feste Länge** aktiviert ist, wird genau diese Anzahl von Zeichen erwartet.
    - **Typ** - Wählen Sie den Typ des Wertes, der mit dieser Anwendungskennung gescannt wird (*Numerisch*, *Alphanumerisch* oder *Datum*). Für Datumsangaben ist das erwartete Format JJMMTT (ohne Leerzeichen oder Bindestriche).
    - **Dezimal** - Aktivieren Sie dieses Kontrollkästchen, wenn der Wert ein implizites Dezimalkomma enthält. Wenn dieses Kontrollkästchen aktiviert ist, verwendet das System die letzte Ziffer des Anwendungsbezeichners, um die Anzahl der Dezimalstellen zu bestimmen. Wenn der Anwendungsbezeichner z.B. *3205* lautet, werden die äußersten fünf Ziffern des Wertes so interpretiert, als kämen sie nach dem Dezimalpunkt.

> [!NOTE]
> Das Gruppentrennzeichen, das auf der Seite **Parameter für Lagerortverwaltung** angegeben wird, ist optional, wenn ein Wert, auf den ein Anwendungsbezeichner folgt, eine feste Länge hat oder wenn seine Länge maximiert ist (d. h. wenn die Länge gleich dem Wert **Länge** ist, der für den Anwendungsbezeichner festgelegt ist).

## <a name="establish-the-generic-gs1-setup"></a>Einrichten der generischen GS1 Einrichtung

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

## <a name="set-up-gs1-policies-that-you-can-assign-to-mobile-device-menu-items"></a>Festlegen von GS1-Richtlinien, die Sie Menüpunkten auf mobilen Geräten zuweisen können

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
1. Wählen Sie das Feld **Element**, und scannen Sie den folgenden Barcode: *\]C10100000012345678\~3030\~10b1\~17220215*.

Aufgrund der für dieses Beispiel festgelegten Einstellungen analysiert das System den gescannten Barcode auf folgende Weise.

| Feldschlüssel | Anwendungs-ID | Wert | Notiz |
|---|---|---|---|
| ItemId | 01 | 00000012345678 | Da die Arbeitskraft in das Feld **Element** gescannt hat, wird der erste Wert im Barcode diesem Feld zugeordnet. Die Zuordnung wird aus der generischen Einrichtung von GS1 übernommen. |
| Mge | 30 | 30 | Da mehrere Feldwerte in einem einzigen Scanvorgang erfasst werden, werden diese Zuordnung und alle übrigen Zuordnungen aus der GS1-Richtlinie übernommen, die dem Menüpunkt **Empfang** zugeordnet ist. Dieser Wert ist die Menge, die empfangen wurde. |
| InventBatchId | 10 | b1 | Bei diesem Wert handelt es sich um die Batch-ID. |
| Ablaufdatum | 17 | 220215 | Das Datumsformat ist JJMMTT. Daher ist das Verfallsdatum der 15. Februar 2022. |

Der Bon wird dann registriert, und die relevanten Datenbankwerte werden nach dem einmaligen Scannen eingegeben.
