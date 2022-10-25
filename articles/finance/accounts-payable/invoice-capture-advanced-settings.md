---
title: Erweiterte Einstellungen der Invoice Capture-Lösung
description: Dieser Artikel enthält Informationen zu erweiterten Einstellungen in der Invoice Capture-Lösung.
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
ms.openlocfilehash: a1e24b700d0f30fd90f2619dd6e6687736a86774
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691159"
---
# <a name="invoice-capture-solution-advanced-settings"></a>Erweiterte Einstellungen der Invoice Capture-Lösung

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dieser Artikel enthält Informationen zu erweiterten Einstellungen in der Invoice Capture-Lösung.

## <a name="create-additional-connections-for-channels"></a>Zusätzliche Verbindungen für Kanäle erstellen

Sie müssen Verbindungen zum E-Mail- oder Dateispeicher herstellen, um die Überwachung eingehender Rechnungen aus verschiedenen Kanälen zu ermöglichen. Sie müssen Verbindungen zu Beginn registrieren, um Zugriff für automatisierte Flows zu gewähren, die in der Lösung verwendet werden.

Die folgenden Verbindungstypen werden zum Importieren von Rechnungen verwendet:

- Office 365 Outlook
- Outlook.com
- OneDrive
- SharePoint

Der Kanal für den Rechnungsimport verwendet die Verbindungen in weiteren Konfigurationsschritten. Bevor Benutzer einen Kanal einer bestimmten Verbindung erstellen können, muss die Sicherheitsrolle **Administrator** ihnen gewährt werden, und sie müssen Verbindungen herstellen.

Gehen Sie folgendermaßen vor, um eine Verbindung zu Microsoft Dataverse zu erstellen.

1. Gehen Sie zu **Administratorsytem \> Standardlösung**.
2. Wählen Sie **Neu**, und wählen Sie dann **Verbindungsreferenz** aus.
3. Geben Sie im Feld **Anzeigename** einen Namen ein.
4. Wählen Sie **Microsoft Dataverse** als Konnektor.
5. Wenn Sie die Verbindung zum ersten Mal einrichten, wählen Sie **Neue Verbindung** aus.
6. Erstellen Sie im angezeigten Dialogfeld eine Dataverse Verbindung und wählen Sie dann **Erstellen**.
7. Geben Sie Dataverse Konto und Passwort ein.
8. Gehen Sie nach bestandener Validierung zur Verbindungsseite und wählen Sie **Aktualisieren** aus, wählen Sie das Konto aus, und wählen Sie dann **Erstellen** aus.

Gehen Sie folgendermaßen vor, um eine E-Mail- oder Dateispeicherverbindung zu erstellen.

1. Wählen Sie auf der Seite **Verbindungsaufbau** im Feld **Verbindungstyp** die Option **Office 365 Outlook**.
2. Für eine E-Mail-Verbindung können Sie **Outlook.com** oder **Office 365 Outlook** als Konnektor auswählen. Für eine Dateispeicherverbindung können Sie entweder **OneDrive** oder **SharePoint** auswählen.

Um bestehende Verbindungen zu überprüfen, gehen Sie zu **Standardlösung \> Objekte \> Verbindungsreferenzen**. Der Benutzer, der Kanäle erstellt, sollte mindestens eine Dataverse Verbindung zusätzlich zu bestimmten E-Mail- oder Dateispeicherverbindungen haben. Der Ersteller des neuen Kanals sollte der Besitzer der Verbindung sein.
