---
title: Konfigurieren Sie einen SharePoint-Kanal
description: In diesem Artikel wird erklärt, wie Sie einen Microsoft SharePoint-Kanal für die Verarbeitung eingehender elektronischer Rechnungen konfigurieren.
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 89538adde4d14212fb0deccad05f828d146f16db
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910040"
---
# <a name="configure-a-sharepoint-channel"></a>Konfigurieren Sie einen SharePoint-Kanal

[!include [banner](../includes/banner.md)]

Als Voraussetzung für die Konfiguration eines Microsoft SharePoint-Kanals zur Verarbeitung eingehender Dokumente führen Sie die Schritte aus, die unter [Konfigurieren einer SharePoint-Verbindung](e-invoicing-create-sharepoint-connection.md) beschrieben sind.

Anschließend können Sie den Kanal SharePoint verwenden, um elektronische Lieferantenrechnungen aus Dateien zu importieren, die in Ihren SharePoint-Ordnern gespeichert sind.

1. Erstellen Sie auf Ihrer SharePoint Seite die folgenden Ordner:

    - **Hauptordner** - Der Ordner, in dem der Dienst die Dateien verarbeitet.
    - **Archivordner** - Der Ordner, in dem die verarbeiteten Dateien gespeichert werden.
    - **Fehlerordner** - Der Ordner, in den das System Dateien verschiebt, wenn die Verarbeitung fehlschlägt.

2. Wählen Sie im Regulatory Configuration Service (RCS) die Funktion für die elektronische Rechnungsstellung aus, die Sie erstellt haben. Stellen Sie sicher, dass Sie die Version auswählen, die den Status **Entwurf** hat.
3. Auf der Registerkarte **Einrichtungen** wählen Sie **Hinzufügen**.
4. Wählen Sie in der Dropdown-Dialogbox **Einrichtung einer Funktion erstellen** in der Feldgruppe **Neu** die Option **Benutzerdefinierte Einrichtung**.
5. In der Feldgruppe **Einrichtungstyp** wählen Sie die Option **Datenkanal**.
6. Wählen Sie im Feld **Datenkanal wählen** den Ordner **SharePoint**.
7. Wählen Sie **Erstellen** aus.
8. Markieren Sie die Zeile, die Sie erstellt haben, und wählen Sie dann **Bearbeiten**.
9. Legen Sie auf der Registerkarte **Datenkanal** im Abschnitt **Parameter** die folgenden erforderlichen Felder fest.

    | Feld                 | Description |
    |-----------------------|-------------|
    | Datenkanal          | Geben Sie einen eindeutigen Namen ein, um den Datenkanal zu identifizieren. Der Name darf maximal 10 Zeichen lang sein. Sie wird in den Anwendungsregeln und in den angeschlossenen Anwendungen während des Kommunikationsprozesses referenziert. |
    | SharePoint-Adresse    | Geben Sie die URL SharePoint ein. Geben Sie beispielsweise `<domain>.sharepoint.com` ein. |
    | Anwendungskennung        | Geben Sie den Namen des Azure Key Vault-Geheimnisses ein, das die ID des Benutzerkontos SharePoint enthält. Dieses Geheimnis muss in Key Vault erstellt und in Ihrer Umgebung festgelegt werden. Der Wert ist der **Anwendungs-(Client-)ID** Wert aus [Verbindung SharePoint konfigurieren](e-invoicing-create-sharepoint-connection.md). |
    | Anwendungsgeheimnis    | Geben Sie den Namen des Key Vault-Geheimnisses ein, das das Kennwort des Benutzerkontos SharePoint enthält. Der Wert ist der **Geheimnis der App-Registrierung** aus [Verbindung SharePoint konfigurieren](e-invoicing-create-sharepoint-connection.md). |
    | Name des Standorts             | Geben Sie den Namen der SharePoint Site ein. |
    | Name der Dokumentbibliothek | Geben Sie den Namen der SharePoint-Dokumentenbibliothek ein. |
    | Zeitüberschreitung               | Geben Sie die maximale Zeit in Millisekunden (ms) ein, die das System auf eine Antwort warten soll. Der Standardwert ist 10.000 ms (10 Sekunden). |
    | Hauptordner           | Geben Sie die Quelle für den Datei-Import oder den Ordner an, aus dem der Dienst Dateien verarbeiten soll. |
    | Archivordner        | Legen Sie den Ordner fest, in dem verarbeitete Dateien gespeichert werden sollen. |
    | Fehlerordner          | Geben Sie den Ordner an, in den das System Dateien verschieben soll, wenn die Verarbeitung fehlschlägt. |
    | Maximale Dateigröße         | Geben Sie die maximale Größe einer einzelnen Datei, die verarbeitet wird, in Bytes an. Der Standardwert ist 20.000.000 Bytes. |
    | Maximale Anzahl Dateien      | Geben Sie die maximale Anzahl der zu verarbeitenden Dateien für eine einzelne Aktion ein. Wenn Sie die Anzahl der Dateien nicht einschränken möchten, legen Sie den Wert auf **0** (Null) fest. |
    | Dateifilter           | Geben Sie eine Zeichenfolge ein, um nach Dateinamen zu filtern. Dieses Feld ist optional. Eine einfache Maske wie **\*smth\*.ext** wird unterstützt, wobei jedes Sternchen (\*) für null oder mehr Vorkommen eines beliebigen Zeichens steht. Geben Sie zum Beispiel **\*.pdf** ein, um den Channel so zu konfigurieren, dass er PDF-Dateien liest. |
    | Benutzerdefinierter Dateiname      | Geben Sie den angepassten Dateinamen des Clients ein. |

10. Überprüfen und aktualisieren Sie auf der Registerkarte **Anwendbarkeitsregeln** die Kriterien nach Bedarf. Der Wert des Feldes **Kanal** muss mit dem Wert übereinstimmen, den Sie im vorherigen Schritt in das Feld **Datenkanal** eingegeben haben.
11. Klicken Sie auf **Speichern** und schließen Sie die Seite.
