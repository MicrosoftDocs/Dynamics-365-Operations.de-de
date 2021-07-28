---
title: Einrichten und Ausführen der Verarbeitung, um ein einfaches EB-Format aufzurufen, um einen Excel-Bericht zu generieren
description: Dieses Thema enthält ein Beispiel, das zeigt, wie Sie elektronische Nachrichten einrichten und verwenden.
author: liza-golub
ms.date: 07/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 25721f1b79d8f0fbf8ca2112ed21fa2d8cd0bc84
ms.sourcegitcommit: 73d320d2103f2b0c6ecbb2b9df746469bc544ea2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/07/2021
ms.locfileid: "6433786"
---
# <a name="set-up-and-run-processing-to-call-a-simple-exporting-er-format-to-generate-an-excel-report"></a>Einrichten und Ausführen der Verarbeitung, um ein einfaches EB-Format aufzurufen, um einen Excel-Bericht zu generieren

[!include [banner](../includes/banner.md)]

Nachdem Sie Ihr EB-Format erstellt haben, es Datenquellen zugeordnet haben und ihn abgeschlossen haben, können Sie es vom Arbeitsbereich **Elektronische Berichterstellung** aus ausführen. Nachdem der Bericht generiert wurde, können Sie ihn lokal speichern.

Um die folgenden Aspekte des Berichterstellungsprozesses zu steuern, richten Sie die elektronische Nachrichtenverarbeitung ein:

- Protokollieren Sie Informationen darüber, wer den Bericht generiert hat.
- Protokollieren Sie Informationen darüber, wann der Bericht generiert wurde.
- Speichern Sie Berichte, die für frühere Perioden generiert wurden.

Das folgende Beispiel, das anzeigt, wie Sie elektronische Nachrichten einrichten können, um einen Bericht zu generieren, der auf einem Export-EB-Format für Microsoft Excel basiert. Wenn Sie diesem Beispiel folgen möchten, muss das Export-EB-Format für Excel bereits erstellt, zugeordnet zu Datenquellen und abgeschlossen sein. Darüber hinaus muss ein Nummernkreis für elektronische Nachrichten bereits eingerichtet sein.

Wenn Sie die Verarbeitung erstellen, ist es hilfreich, wenn Sie zuerst die Verarbeitungsaktivitätsstatus definieren, die eingerichtet werden. Die folgende Abbildung zeigt die Verarbeitung für dieses Beispiel.

![Verarbeitungsschema](media/processing-scheme.png)

## <a name="create-message-statuses"></a>Nachrichtenstatus erstellen

1. Wechseln Sie zu **Steuer** \> **Einrichten** \> **Elektronische Nachrichten** \> **Nachrichtenstatus**.
2. Erstellen Sie die folgenden Nachrichtenstatus:

    - Neue
    - Vorbereitet
    - Generiert

    ![Nachrichtenstatus](media/message-statuses.png)

3. Auf der Position für den Status **Neu**, aktivieren Sie das Kontrollkästchen **Löschen ermöglichen**, um Benutzern das Löschen von Meldungen zu ermöglichen, die diesen Status besitzen.

## <a name="create-additional-fields"></a>Zusätzliche Felder erstellen

1. Wechseln Sie zu **Steuer** \> **Einrichten** \> **Elektronische Nachrichten** \> **Zusätzliche Felder**.
2. Fügen Sie ein zusätzliches Feld und seine Werte hinzu.
3. Legen Sie die Option **Benutzerbearbeitung** auf **Ja** fest, damit Benutzer das Feld bearbeiten können.

![Zusätzliche Felder](media/additional-fields.png)

## <a name="create-message-processing-actions"></a>Nachrichtenverarbeitungsaktivitäten erstellen

Für dieses Beispiel werden Sie die folgenden Aktivitäten zur Nachrichtenverarbeitung erstellen:

- **Nachricht erstellen**
- **Aktualisieren auf „Vorbereitet”**
- **Bericht generieren**
- **Aktualisieren auf Anfangsstatus** (optional)

Gehen Sie folgendermaßen vor, um die Aktivitäten zu erstellen.

1. Wechseln Sie zu **Steuer** \> **Einrichten** \> **Elektronische Nachrichten** \> **Nachrichtenverarbeitungsaktivitäten**.
2. Erstellen Sie eine Aktivität mit der Bezeichnung **Nachricht erstellen**. Wählen Sie im Inforegister **Allgemein** im Feld **Aktivitätstyp** die Option **Nachricht erstellen** aus.
3. Erstellen Sie eine Aktivität mit der Bezeichnung **Aktualisieren auf „Vorbereitet”**, und legen Sie die folgenden Felder fest:

    - Wählen Sie im Inforegister **Allgemein** im Feld **Aktivitätstyp** die Option **Nachrichtenebenenbenutzer-Verarbeitung** aus.
    - Wählen Sie im Inforegister **Anfangsstatus** im Feld **Nachrichtenstatus** die Option **Neu** aus.
    - Wählen Sie im Inforegister **Ergebnisstatus** im Feld **Nachrichtenstatus** die Option **Vorbereitet** aus. Geben Sie im Feld **Antworttyp** den Text **Erfolgreich ausgeführt** ein.

4. Erstellen Sie eine Aktivität mit der Bezeichnung **Bericht generieren**, und legen Sie die folgenden Felder fest:

    - Wählen Sie im Inforegister **Allgemein** im Feld **Aktivitätstyp** die Option **Elektronischer Berichterstellungsexport** aus. Wählen Sie im Feld **Formatzuordnung** das Export-EB-Format aus. Die Optionen sind **Excel**, **XML**, **JSON**, **Text** und **Andere**.
    - Wählen Sie im Inforegister **Anfangsstatus** im Feld **Nachrichtenstatus** die Option **Vorbereitet** aus.
    - Wählen Sie im Inforegister **Ergebnisstatus** im Feld **Nachrichtenstatus** die Option **Generiert** aus. Geben Sie im Feld **Antworttyp** den Text **Erfolgreich ausgeführt** ein.

    ![Berichtsaktivität generieren](media/generate-report-action.png)

5. Optional: Um es Benutzern zu ermöglichen, einen Bericht mehrere Male neu zu generieren, können Sie eine Aktivität namens **Auf Anfangsstatus aktualisieren** erstellen und die folgenden Felder festlegen:

    - Wählen Sie im Inforegister **Allgemein** im Feld **Aktivitätstyp** die Option **Nachrichtenebenenbenutzer-Verarbeitung** aus.
    - Wählen Sie im Inforegister **Anfangsstatus** im Feld **Nachrichtenstatus** die Option **Generiert** aus.
    - Fügen Sie im Inforegister **Ergebnisstatus** eine getrennte Position für jeden der beiden Nachrichtenstatus hinzu (**Vorbereitet** und **Neu**). Legen Sie für beide Positionen das Feld **Antworttyp** auf **Erfolgreich ausgeführt** fest.

## <a name="electronic-message-processing"></a>Verarbeitung der elektronischen Nachricht

In diesem Beispiel sollten alle Aktivitäten eingerichtet werden, sodass sie getrennt ausgeführt werden. Es wird davon ausgegangen, dass der Benutzer jede Aktivität initialisieren wird.

1. Wechseln Sie zu **Steuer** \> **Einrichten** \> **Elektronische Nachrichten** \> **Elektronische Nachrichtenverarbeitung**.
2. Fügen Sie einen Datensatz für Ihre Verarbeitung hinzu, und fügen Sie alle zuvor definierten Aktivitäten sowie ein zusätzliches Feld hinzu.
3. Optional: Definieren Sie im Inforegister **Sicherheitsrollen** Sicherheitsrollen für Ihre Verarbeitung, um den Zugriff auf bestimmte Berichterstellung zu beschränken.
4. Wechseln Sie zu **Steuer** \> **Abfragen und Berichte** \> **Elektronische Nachrichten** \> **Elektronische Nachrichten**.
5. Wählen Sie **Neu** aus, um eine Nachricht zu erstellen. An diesem Punkt können Sie Datumsangaben und eine Beschreibung hinzufügen. Sie können auch den Wert des zusätzlichem Felds auch Bedarf aktualisieren.

    ![Eine elektronische Nachricht erstellen](media/create-electronic-message.png)

    Das Raster im Inforegister **Aktivitätsprotokoll** wird automatisch mit einem Protokoll aller Aktivitäten ausgefüllt, die zu dieser Nachricht ausgeführt werden.

    Sie können jetzt den Nachrichtenstatus löschen oder aktualisieren. 

6. Um den Nachrichtenstatus zu aktualisieren, wählen Sie **Status aktualisieren** aus. Im Feld **Neuer Status** wählen Sie **Vorbereitet** und dann **OK** aus.

    ![Den Nachrichtenstatus aktualisieren](media/update-status.png)

    Der Nachrichtenstatus wird auf **Vorbereitet** aktualisiert.

7. Generieren Sie den Bericht über **Berichte generieren**.

    Der Bericht wird generiert, und der Nachrichtenstatus sowie das Aktivitätsprotokoll werden aktualisiert.

8. Um den generierten Bericht anzuzeigen, wählen Sie die Schaltfläche **Anhang** (Büroklammersymbol) in der rechten oberen Ecke der Seite aus.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
