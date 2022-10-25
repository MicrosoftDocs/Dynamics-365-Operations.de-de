---
title: Konfigurationsgruppen für die Invoice Capture-Lösung
description: Dieser Artikel enthält allgemeine Informationen zu Konfigurationsgruppen in der Invoice Capture-Lösung.
author: sunfzam
ms.date: 09/28/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: cfe5ae35b4f87a350d944b30a49251081766ad27
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691169"
---
# <a name="invoice-capture-solution-configuration-groups"></a>Konfigurationsgruppen für die Invoice Capture-Lösung

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Benutzer können die Liste der Rechnungsfelder und die manuelle Überprüfungseinstellung für juristische Personen mithilfe von Konfigurationsgruppen verwalten. Benutzer können Rechnungskonfigurationen für verschiedene juristische Personen in Gruppen einrichten. Alle juristischen Personen in derselben Konfigurationsgruppe verwenden dieselben Rechnungsfelder und Einstellungen für die manuelle Überprüfung.

## <a name="manage-configuration-groups"></a>Variantengruppen verwalten

Um Konfigurationsgruppen mithilfe der App zu verwalten, gehen Sie zu **Konfiguration**, und wählen Sie dann **Systemkonfiguration \> Komponente Konfigurationsgruppen definieren**.

Auf der Seite **Konfigurationsgruppen definieren** zeigt die Hauptregisterkarte die Liste der definierten Konfigurationsgruppen an. Es zeigt auch eine Standardkonfigurationsgruppe. Für jede Konfigurationsgruppe sin die folgenden Aktionen verfügbar:

- **Eine Konfigurationsgruppe kopieren** – Sie können eine neue Konfigurationsgruppe erstellen, indem Sie eine vorhandene Gruppe duplizieren. Die neue Gruppe hat dieselben Werte wie die ursprüngliche Gruppe für alle Felder außer **Gruppenname** und **Gruppenbeschreibung**. Nachdem die Konfigurationsgruppe dupliziert wurde, wählen Sie **OK** aus.
- **Konfigurationsgruppen löschen** – Um eine Konfigurationsgruppe zu löschen, wählen Sie sie aus und wählen Sie dann **Löschen** aus.

    > [!NOTE]
    > Das Standardkonfigurationsgruppe kann nicht gelöscht werden.

- **ID einer Konfigurationsgruppe bearbeiten** – Um die ID einer Konfigurationsgruppe zu bearbeiten, wählen Sie das Feld **Gruppen-ID** aus und aktualisieren Sie den Wert. Die Gruppen-ID sollte keine Leerzeichen oder Sonderzeichen enthalten und 20 Zeichen nicht überschreiten.

    > [!NOTE]
    > Der Wert des Felds **Gruppen-ID** kann nur einmal aktualisiert werden.

- **Konfigurationsgruppenbeschreibung bearbeiten** – Um die Beschreibung einer Konfigurationsgruppe zu bearbeiten, wählen Sie das Feld **Beschreibung** aus und aktualisieren Sie den Wert.
- **Die Einstellung für die manuelle Überprüfung ändern** – Benutzer können entscheiden, ob eine Rechnung manuell geprüft werden muss. Um die Einstellung für die manuelle Überprüfung zu ändern, wählen Sie die Option **Manuelle Überprüfung erforderlich** aus. Die folgenden Optionen stehen zur Verfügung:

    - **Immer manuelle Überprüfung** – Wählen Sie diese Option, wenn Rechnungen in der Konfigurationsgruppe immer eine manuelle Überprüfung erfordern.
    - **Für Fehler und Warnungen** – Wählen Sie diese Option, wenn Rechnungen, die Fehlermeldungen oder Warnmeldungen enthalten, manuell überprüft werden müssen.
    - **Für Fehler** – Wählen Sie diese Option, wenn Rechnungen, die Fehlermeldungen enthalten, manuell überprüft werden müssen.

- **Die Einstellung für die Konfidenzbewertung ändern** – Der Konfidenzwert sind Metadaten, die die Invoice Capture-Lösung bereitstellt, um die Genauigkeit erkannter Rechnungsdaten zu melden. Je höher die Punktzahl ist, desto genauer können die erkannten Daten sein. Mit der Konfiguration können Benutzer basierend auf der Konfidenzbewertung definieren, wann eine manuelle Überprüfung erforderlich ist. Benutzer können den Konfidenzwert-Schwellenwert für Rechnungen ändern. Wählen Sie zum Aktualisieren der Konfidenzbewertungseinstellung das Feld **Konfidenzbewertung** aus und aktualisieren Sie den Wert.

    Es gibt zwei Benachrichtigungstypen für Konfidenzwerte:

    - **Warnung** – Rechnungsfelder mit Konfidenzwerten über der Warnschwelle werden als korrekt betrachtet. Der Warnschwellenwert muss größer als der Fehlerschwellenwert und kleiner als 100 sein.
    - **Fehler** – Rechnungsfelder mit Konfidenzwerten unter der Fehlerschwelle werden als fehlgeschlagen betrachtet. Fehlermeldungen werden dem Benutzer angezeigt. Der Fehlerschwellenwert muss größer als 0 (Null) und kleiner als der Warnungsschwellenwert sein. Warnmeldungen werden für Rechnungsfelder angezeigt, deren Konfidenzwerte zwischen dem Warnschwellenwert und dem Fehlerschwellenwert liegen.

- **Rechnungsfelder verwalten** – Benutzer können die Liste der Rechnungsfelder verwalten, die im Side-by-Side-Viewer angezeigt wird. Wählen Sie auf der Registerkarte **Rechnungsfeldverwaltung** das Zahnradsymbol aus, wählen Sie die hinzuzufügenden Rechnungsfelder aus, und wählen Sie dann **Speichern**. Die ausgewählten Felder werden der Liste hinzugefügt. Um ein Rechnungsfeld aus der Liste zu entfernen, wählen Sie **Entfernen** auf dem Feld aus.

### <a name="manage-file-filters-optional"></a>Dateifilter verwalten (optional)

Dateifilter verwalten ermöglicht es Benutzern, zusätzliche Filter für Eingangsrechnungsdateien zu definieren. Dateien, die die Filterkriterien nicht erfüllen, werden empfangen und in der Liste **Empfangene Dateien** angezeigt, aber sie zeigen Dateiüberprüfungsfehler an. Dieses Verhalten unterscheidet sich von dem Verhalten für Filter, die im Kanal definiert sind. Bei diesen Filtern werden Dateien, die die Kriterien nicht erfüllen, überhaupt nicht empfangen. Benutzer können die eingehenden Dateien überprüfen und entscheiden, ob es sich bei jeder Datei um eine ungültige Rechnung handelt, und sie können die Datei veraltet machen oder sie manuell zur Erkennung und Einbeziehung in erfasste Rechnungen einschließen.

Wenn die Invoice Capture-Lösung installiert ist, wird ein Standarddateifilter definiert. Dieser Dateifilter ist global. Wenn Sie andere Filtereinstellungen wünschen, können Sie den Standardfilter aktualisieren. Wenn ein Feld obligatorisch ist, wählen Sie **Erforderlich** aus. 

### <a name="accepted-file-size"></a>Akzeptierte Dateigröße

Sie können die akzeptierte Dateigröße auswählen.

> [!NOTE]
> Dateien, die größer als 20.480 Kilobyte (KB) sind, werden nicht unterstützt.

### <a name="supported-file-types"></a>Unterstützte Dateitypen

Die folgenden Dateitypen werden derzeit unterstützt:

- PDF
- PNG
- JPG
- JPEG
- TIF
- TIFF
