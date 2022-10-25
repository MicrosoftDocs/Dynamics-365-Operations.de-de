---
title: Die Invoice Capture-Lösung konfigurieren
description: In diesem Artikel wird erläutert, wie Sie die Invoice Capture-Lösung konfigurieren.
author: sunfzam
ms.date: 09/25/2022
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
ms.openlocfilehash: e297dafc930368f14f2e68213ce4153ba792ef4d
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691150"
---
# <a name="configure-the-invoice-capture-solution"></a>Die Invoice Capture-Lösung konfigurieren

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Nach der Installation der Invoice Capture-Lösung müssen Sie die Umgebung konfigurieren. Der Prozess besteht aus den folgenden grundlegenden Schritten.

1. **Erforderlich:** Synchronisieren Sie die juristischen Personen aus Microsoft Dynamics 365 Finance. Dieser Schritt dient zum Aufbau der Organisationsstruktur in Microsoft Power Platform.
2. **Erforderlich:** Konfigurieren Sie die Kanäle für den Import von Rechnungsbildern. Die Lösung unterstützt die folgenden Kanäle:

    - Office 365 Outlook (Standard)
    - Outlook.com
    - OneDrive
    - SharePoint

3. **Optional:** Definieren Sie zusätzliche Konfigurationsgruppen für den Dienst zur optischen Zeichenerkennung (OCR).
4. **Optional:** Definieren Sie Zuordnungsregeln für die juristische Person, das Kreditorenkonto, den Artikel und die Beschaffungsart.

Dieser Artikel konzentriert sich auf die beiden erforderlichen Schritte des Prozesses. Weitere Informationen zu Konfigurationsgruppen finden Sie unter [Konfigurationsgruppen der Invoice Capture-Lösung](invoice-capture-config-group.md). Weitere Informationen zu Zuordnungsregeln finden Sie unter [Zuordnungsregeln für die Invoice Capture-Lösung](invoice-capture-mapping-rules.md).

## <a name="manage-legal-entities"></a>Juristische Personen verwalten

In Finance sind juristische Personen als Organisation definiert, die über die Registrierung bei Behörden identifiziert wird. Geschäftstätigkeiten werden in getrennten juristischen Personen durchgeführt und erfasst. In Microsoft Power Platform werden Unternehmenseinheiten, Sicherheitsrollen und Benutzer so miteinander verknüpft, dass sie dem rollenbasierten Sicherheitsmodell entsprechen.

Geschäftseinheiten werden zusammen mit Sicherheitsrollen verwendet, um den Datenzugriff zu steuern. Benutzer sehen nur die Informationen, die sie für ihre Arbeit benötigen. Die Invoice Capture-Lösung bietet einen Konfigurationsbereich, in dem Sie grundlegende Informationen von bestehenden juristischen Personen in Finance laden und diese manuell erstellten Einheiten verwalten können. Die juristischen Personen werden auf Kreditorenrechnungen und in der Sicherheitskontrolle verwendet.

Wenn eine juristische Person erstellt und in der Listenansicht angezeigt wird, wird automatisch eine standardmäßige Unternehmenseinheit mit demselben Namen erstellt. Das Team erhält die **AP-Angestellter** Sicherheitsrolle. Beim Importieren von juristischen Personen werden grundlegende Stammdaten aus Finance importiert. Die nicht vorhandenen Artikel werden nach juristischer Person identifiziert und der Invoice Capture-Lösung hinzugefügt. Die Standardkonfigurationsgruppe wird neuen juristischen Personen zugewiesen.

### <a name="sync-legal-entities"></a>Juristischen Personen synchronisieren

Sie können juristische Personen nicht direkt erstellen. Sie können jedoch juristische Personen aus Finance synchronisieren. Führen Sie die folgenden Schritte aus, um juristische Personen zu synchronisieren.

1. Gehen Sie zu **Konfiguration \> Systemkonfiguration \> Juristische Personen verwalten**.
2. Wählen Sie **Juristische Personen synchronisieren** und dann **OK** im Dialogfeld zur Bestätigung.

Nach Abschluss der Synchronisierung wird die Anzahl der neuen juristischen Personen angezeigt. Die neuen juristischen Personen werden in der Listenansicht angezeigt. Die Standardkonfigurationsgruppe wird den neuen juristischen Personen zugewiesen.

## <a name="configure-invoice-import-channels"></a>Rechnungsimportkanäle konfigurieren

Lieferanten versenden Rechnungen aus verschiedenen Kanälen (E-Mail, Dateiarbeitsbereich oder Rechnungsportal) über unterschiedliche Formate (Papier oder Bild). Die Invoice Capture-Lösung kann verschiedene Kanäle und Formate verarbeiten. Folgende Typen werden unterstützt:

- Office 365 Outlook
- Outlook.com
- SharePoint
- OneDrive

Wenn ein Kanal für ein bestimmtes Konto erstellt wird, wird ein automatisierter Ablauf mit einer vordefinierten Vorlage erstellt, um die eingehenden E-Mails oder Dateien im Posteingang oder Bereich zu überwachen. Jede Datei, die eine gültige Rechnung enthält, kann erkannt und an den Rechnungsbereich gesendet werden, um auf die Verarbeitung durch den Sachbearbeiter der Kreditorenbuchhaltung (AP) zu warten. Der Anhang sollte im PDF- oder Bildformat vorliegen. Rechnungen können entsprechend der Kanalkonfiguration in die Invoice Capture-Lösung geladen werden.

### <a name="create-a-channel"></a>Erstellen eines Kanals

Wenn Sie das zusätzliche Lösungspaket (Dynamics 365 Invoice Capture – Installationstools) importiert haben, ist die Standardverbindung für Office 365 Outlook einsatzbereit. Wenn Sie weitere Verbindungen für verschiedene E-Mail-Konten oder andere Kanaltypen erstellen möchten, siehe [Erstellen Sie zusätzliche Verbindungen für Kanäle](invoice-capture-advanced-settings.md#create-additional-connections-for-channels).

Um einen Kanal zu erstellen, befolgen Sie diese Schritte.

1. Gehen Sie zu **Konfiguration \> Systemkonfiguration \> Kanäle konfigurieren**.
2. Wählen Sie **Neu** aus.
3. Stellen Sie die folgenden Felder ein:

    - Kanalname
    - Description
    - Typ
    - Verbindung

Nur E-Mails oder Dateien, die den folgenden Kriterien entsprechen, können in die Lösung importiert werden.

| Typ               | Variante  | Mehr erfahren |
|--------------------|----------------|------------------|
| Office 365 Outlook | Ordner         | Der E-Mail-Ordner muss sich im Stammverzeichnis befinden. Standardmäßig wird der Ordner Posteingang verwendet. Ein Unterordner wird nicht unterstützt. |
|                    | Betrefffilter | (Optional) Eine Teilzeichenfolge, die im Betreff enthalten sein sollte. |
|                    | Ab           | (Optional) Die E-Mail-Adresse des Absenders oder der Absender. Wenn Sie mehrere Adressen angeben, verwenden Sie einen Semikolon (;) als Trennzeichen. |
| SharePoint         | Standortadresse   | Die URL der Site-Adresse. |
|                    | Ordner         | Der Ordner in der Site-Adresse. |

### <a name="activate-the-channel"></a>Aktivieren des Kanals

Wenn ein Flow gespeichert wird, zeigen Felder den Status des Kanals und den Zeitpunkt seiner Erstellung an. Zunächst ist das Feld **Status** auf **Inaktiv** eingestellt. Der **Statusgrund** zeigt an, dass der Kanal initialisiert wurde und zur Aktivierung bereit ist.

Wählen Sie zum Aktivieren des Kanals **Aktivieren** aus. Die Felder **Status** und **Statusgrund** werden aktualisiert.

Wenn ein Kanal nicht benötigt wird, können Sie ihn deaktivieren. Wählen Sie zum Deaktivieren des Kanals **Aktivieren** aus. Die Felder **Status** und **Statusgrund** werden aktualisiert.

### <a name="manage-flows-in-flow-management"></a>Verwalten von Flows in der Flowverwaltung

Sie können einen Kanal auf der Seite **Kanäle konfigurieren** anzeigen oder in der Flussverwaltung.

Um weitere Details anzuzeigen, gehen Sie zu **Admin-System \> Standardlösung \> Cloud-Flow**, und wählen Sie den Zielfluss aus. Zu den angezeigten Details gehören verknüpfte Verbindungen, Eigentümer und Ausführungsverläufe.

Um den Status zu synchronisieren, wählen Sie **Prüfen** aus, um zu bestätigen, dass der Status des Kanals mit dem Status des Flusses übereinstimmt.

Einige Fälle der Ausnahmebehandlung werden im Feld **Statusgrund** angezeigt:

- **Fehlende Dataverse Verbindung** – Der aktuelle Benutzer hat nicht mindestens eine **Microsoft Dataverse** Verbindungsreferenz erstellt.
- **Nicht gefunden** – Der mit dem Kanal verknüpfte Flow wurde in der Flow-Verwaltung gelöscht. Der Kanal sollte erneut gespeichert werden, um einen neuen Kanal zu erstellen.
- **Im Flowmanagement deaktiviert** – Der Flow wurde im Flow-Management deaktiviert und der Status des Kanals weicht vom Status des Flows ab.
- **Im Flowmanagement aktiviert** – Der Flow wurde im Flow-Management aktiviert und der Status des Kanals weicht vom Status des Flows ab.
- **Ein unerwarteter Fehler ist aufgetreten** – Der Benutzer muss bestätigen, dass die Site eine „Kommunikationssite“ und der Ordner „Dokumentenbibliothek“ ist.
