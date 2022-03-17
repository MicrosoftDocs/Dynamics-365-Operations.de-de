---
title: Konfigurieren Sie einen E-Mail-Kanal
description: In diesem Thema wird erklärt, wie Sie einen E-Mail-Channel für den Empfang elektronischer Rechnungen konfigurieren.
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6a5896a033212cf0f29f686eec0ab6fb3bc1d2a6
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371636"
---
# <a name="configure-an-email-channel"></a>Konfigurieren Sie einen E-Mail-Kanal

[!include [banner](../includes/banner.md)]

Wenn die von Ihnen erstellte Funktion Elektronische Rechnungsstellung elektronische Lieferantenrechnungen aus angehängten Dateien importiert, die per E-Mail empfangen werden, sollten Sie einen E-Mail-Kontokanal konfigurieren.

1. Wählen Sie im Regulatory Configuration Service (RCS) die Funktion für die elektronische Rechnungsstellung aus, die Sie erstellt haben. Stellen Sie sicher, dass Sie die Version auswählen, die den Status **Entwurf** hat.
2. Auf der Registerkarte **Einrichtungen** wählen Sie **Hinzufügen**.
3. Wählen Sie in der Dropdown-Dialogbox **Einrichtung einer Funktion erstellen** in der Feldgruppe **Neu** die Option **Benutzerdefinierte Einrichtung**.
4. In der Feldgruppe **Einrichtungstyp** wählen Sie die Option **Datenkanal**.
5. Geben Sie in das Feld **Datenkanal wählen** **Eingehende E-Mail** ein.
6. Wählen Sie **Erstellen** aus.
7. Markieren Sie die Zeile, die Sie erstellt haben, und wählen Sie dann **Bearbeiten**.
8. Legen Sie auf der Registerkarte **Datenkanal** im Abschnitt **Parameter** die folgenden erforderlichen Felder fest.

    | Feld                | Description |
    |----------------------|-------------|
    | Datenkanal         | Geben Sie einen eindeutigen Namen ein, um den Datenkanal zu identifizieren. Der Name darf maximal 10 Zeichen lang sein. Es wird in den Anwendungsregeln und in den angeschlossenen Anwendungen während des Kommunikationsprozesses referenziert. |
    | Serveradresse       | Geben Sie die Serveradresse des Anbieters des E-Mail-Kontos ein. Die Serveradresse für den Anbieter `https://outlook.live.com` ist zum Beispiel imap-mail.outlook.com. |
    | Serverport          | Geben Sie die Nummer des Ports ein, den der Anbieter des E-Mail-Kontos verwendet. Ein Beispiel: Der Port des Servers für den Anbieter `https://outlook.live.com` ist 993. |
    | Benutzernamegeheimnis     | Geben Sie den Namen des Key Vault-Geheimnisses Microsoft Azure ein, das die ID des E-Mail-Benutzerkontos enthält. Dieses Geheimnis muss in Key Vault erstellt und in Ihrer Umgebung festgelegt werden. |
    | Benutzerkennwortgeheimnis | Geben Sie den Namen des Key Vault-Geheimnisses ein, das das Kennwort für das E-Mail-Benutzerkonto enthält. |
    | Zeitüberschreitung              | Das maximale Zeitlimit in Millisekunden (ms), das das System auf eine Antwort warten soll. Der Standardwert ist 10.000 ms (10 Sekunden). |
    | Hauptordner          | Geben Sie die E-Mail-Importquelle oder den Ordner an, aus dem der Dienst die E-Mails verarbeiten soll. |
    | Archivordner       | Legen Sie den Ordner fest, in dem verarbeitete E-Mails gespeichert werden sollen. Wenn Sie diesen Ordner nicht angeben, erstellt das System ihn automatisch. |
    | Fehlerordner         | Geben Sie den Ordner an, in den das System E-Mails verschieben soll, wenn die Verarbeitung fehlschlägt. Wenn Sie diesen Ordner nicht angeben, erstellt das System ihn automatisch. |
    | Maximale Nachrichtengröße     | Geben Sie die maximale Größe einer einzelnen Nachricht, die verarbeitet wird, in Bytes ein. Der Standardwert ist 20.000.000 Bytes. |
    | Maximale Anzahl der Nachrichten   | Geben Sie die maximale Anzahl der Nachrichten ein, die für eine einzelne Aktion verarbeitet werden sollen. Wenn Sie die Anzahl der Nachrichten nicht einschränken möchten, legen Sie den Wert auf **0** (Null) fest. |
    | Von-Filter          | Geben Sie eine Zeichenfolge ein, um nach der Absenderadresse zu filtern. Es werden nur E-Mails verarbeitet, bei denen die Absenderadresse mit dem Filter übereinstimmt. Dieses Feld ist optional. Um mehrere Absenderadressen anzugeben, verwenden Sie Semikolons (;) als Trennzeichen. |
    | Betrefffilter       | Geben Sie eine Zeichenfolge ein, um nach dem Betreff zu filtern. Es werden nur E-Mails verarbeitet, bei denen der Betreff mit dem Filter übereinstimmt. Dieses Feld ist optional. Eine einfache Maske wie **\*smth\*.ext** wird unterstützt, wobei jedes Sternchen (\*) für null oder mehr Vorkommen eines beliebigen Zeichens steht. |
    | Datumsfilter          | Geben Sie ein Datum an, um das maximale Alter der verarbeiteten Nachrichten in Tagen festzulegen. Dieses Feld ist optional. Der Standardwert ist 30 Tage. |
    | Verarbeitungsmodus      | <p>Wählen Sie eine der folgenden Optionen, um festzulegen, ob alle Anhänge in einer E-Mail gemeinsam verarbeitet werden können oder ob jeder Anhang einzeln verarbeitet werden soll:</p><ul><li><b>Nach Anhang</b> - Für jeden Anhang in der E-Mail wird ein neuer elektronischer Beleg erstellt. Wenn zum Beispiel eine E-Mail mehrere Dateien mit E-Rechnungsdaten enthält, wird jede Datei im System als neue E-Rechnung betrachtet.</li><li><b>Nach E-Mail</b> - Ein Anhang wird als Basisanhang betrachtet, und eine elektronische Rechnung wird im System erstellt. Andere Anhänge können als unterstützende Dateien verwendet werden.</li></ul> |

9. Fügen Sie im Bereich **Filter für Anhänge** die Informationen zur Dateifilterung hinzu. Es werden nur Anhänge verarbeitet, die dem definierten Filter genügen. Ein Beispiel: **\*.xml** filtert nach Anhängen, die die Dateinamenerweiterung .xml haben. Der Name des Anhangs wird in Dynamics 365 Finance oder Dynamics 365 Supply Chain Management bei der Einrichtung verwendet.

    - Wenn Sie das Feld **Verarbeitungsmodus** im vorherigen Schritt auf **Nach E-Mail** festgelegt haben, können Sie hier mehrere Filter hinzufügen. Der Name dient zur Identifizierung des jeweiligen Dokuments.
    - Wenn Sie im Feld **Verarbeitungsmodus** die Option **Nach Anhang** festlegen, können Sie nur einen Filter hinzufügen.

10. Überprüfen und aktualisieren Sie auf der Registerkarte **Anwendbarkeitsregeln** die Kriterien nach Bedarf. Der Wert des Feldes **Kanal** muss mit dem Wert übereinstimmen, den Sie in Schritt 8 in das Feld **Datenkanal** eingegeben haben.
11. Klicken Sie auf **Speichern** und schließen Sie die Seite.
