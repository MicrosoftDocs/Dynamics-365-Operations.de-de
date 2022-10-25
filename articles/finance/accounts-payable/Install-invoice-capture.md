---
title: Die Invoice Capture-Lösung installieren
description: Dieser Artikel enthält Informationen zur Installation und Integration der Invoice Capture-Lösung in Microsoft Dynamics 365 Finance.
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
ms.openlocfilehash: d853e347c833345f34b65760fd7ee35cbb38c9a3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691170"
---
# <a name="install-the-invoice-capture-solution"></a>Die Invoice Capture-Lösung installieren

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> Wenn Sie die Lösung in der privaten Vorschau installiert haben, müssen Sie die alte Lösung deinstallieren, bevor Sie fortfahren.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie die Invoice Capture-Lösung installieren können, müssen die folgenden Voraussetzungen erfüllt sein:

1. Registrieren Sie eine Anwendung und fügen Sie ein Client-Geheimnis zu Microsoft Azure Active Directory (Azure AD) unter Ihrem Azure-Abonnement hinzu. Weitere Informationen finden Sie unter [Registrieren einer Web-Anwendung in AAD](../../dev-itpro/data-entities/services-home-page.md#register-a-web-application-with-aad).

    > [!NOTE]
    > Notieren Sie sich die Werte **Anwendungs-(Client-)ID**, **Client-Geheimnis** und **Mandanten-ID**, da Sie diese später noch benötigen werden.

2. Registrieren Sie die Azure-Anwendung in einer Dynamics 365 Finance-Umgebung. Weitere Informationen finden Sie unter [Registrieren Ihrer externen Anwendung](../../dev-itpro/data-entities/services-home-page.md#register-your-external-application).

## <a name="install-and-set-up-the-solution"></a>Die Lösung installieren und einrichten

Um die Invoice Capture-Lösung zu installieren, gehen Sie zu AppSource, und wählen Sie den Link für die Vorschauversion von [Dynamics 365 Invoice Capture](https://appsource.microsoft.com/product/dynamics-365/mscrm.dynamics365-invoice-capture-preview?flightCodes=invoicecapture) aus. Nachdem die Installation abgeschlossen ist, sehen Sie die installierte Lösung in der ausgewählten Umgebung in Power Apps.

Gehen Sie wie folgt vor, um diese Einrichtung abzuschließen.

1. Laden Sie die [Hilfslösung](https://github.com/InvoiceCapture/InstallationTools/releases/download/latest/msdyn_InvoiceCaptureIntallationTools.zip) herunter, um die folgenden Details einzurichten:

    - Die Kommunikation zwischen Microsoft Power Platform und der Finance-Umgebung
    - Die Verbindungsreferenz für Dataverse und Office 365 Outlook, das vom Kanal verwendet wird

2. Gehen Sie in Power Apps zu Ihrer Umgebung und wählen Sie **Lösung importieren** aus.
3. Wählen Sie **Durchsuchen**, wählen Sie das heruntergeladene Assistentenlösungspaket aus, und wählen Sie dann **Weiter** aus.
4. Wählen Sie **Weiter**.
5. Weisen Sie eine vorhandene Verbindung zu oder erstellen Sie eine neue, indem Sie **Neue Verbindung** auswählen.
6. Nachdem das Paket erfolgreich importiert wurde, öffnen Sie **Dynamics 365 Invoice Capture – Installationstools**.
7. Führen Sie den Cloud-Flow aus, um die Verbindung zwischen der Invoice Capture-Lösung in Microsoft Power Platform und Finance einzurichten.
8. Wählen Sie **Ausführen**, und geben Sie die folgenden Parameter an:

    - **Dynamics 365 Finance-URL** – Die URL der Finance-Umgebung, in die Sie integrieren möchten.
    - **Mandanten-ID** – Die Mandanten-ID für die Finance-Umgebung.
    - **Client ID** – Die registrierte Azure-Anwendungs-ID.
    - **Geheimer Clientschlüssel** - Der geheimer Clientschlüssel, der für die Azure-Anwendung generiert wurde.
