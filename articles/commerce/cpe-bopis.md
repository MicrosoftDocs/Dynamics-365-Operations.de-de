---
title: BOPIS in einer Dynamics 365 Commerce-Auswertungsumgebung konfigurieren
description: In diesem Thema wird erläutert, wie Sie den Online-Kauf und die Abholung im Geschäft (BOPIS) in einer Microsoft Dynamics 365 Commerce-Umgebung konfigurieren, nachdem sie bereitgestellt wurde.
author: rubendel
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: rubendel
ms.search.validFrom: 2020-04-20
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 62dabaa2610341cc8ad8e85812a317ac3123fcb1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412462"
---
# <a name="configure-bopis-in-a-dynamics-365-commerce-evaluation-environment"></a>BOPIS in einer Dynamics 365 Commerce-Auswertungsumgebung konfigurieren

[!include [banner](includes/banner.md)]

In diesem Thema wird erläutert, wie Sie den Online-Kauf und die Abholung im Geschäft (BOPIS) in einer Microsoft Dynamics 365 Commerce-Auswertungsumgebung konfigurieren, nachdem sie bereitgestellt wurde.

## <a name="prerequisite"></a>Voraussetzung

Führen Sie die in diesem Thema beschriebenen Prozeduren erst aus, nachdem Ihre Commerce-Auswertungsumgebung bereitgestellt und konfiguriert wurde. Informationen zum Bereitstellen und Konfigurieren Ihrer Umgebung finden Sie unter [Bereitstellen einer Dynamics 365 Commerce-Auswertungsumgebung](provisioning-guide.md) und [Konfigurieren einer Dynamics 365 Commerce-Auswertungsumgebung](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning).

Nachdem Ihre Commerce-Umgebung komplett bereitgestellt und konfiguriert wurde, können Sie dieses Thema verwenden, um BOPIS-Szenarien zu aktivieren.

## <a name="configure-the-pos"></a>POS konfigurieren

### <a name="configure-modern-pos"></a>Modern POS konfigurieren

Für BOPIS-Szenarien mit Kreditkartenzahlung ist eine Hardwarestation erforderlich. Die Hardwarestation ist in die Modern POS-Programme für Windows- und Android-Clients integriert. Wenn Sie Cloud POS oder Modern POS für iOS verwenden, muss der POS-Client (Point of Sale) mit einer gemeinsam genutzten Hardwarestation gekoppelt sein. In diesem Thema wird erläutert, wie Sie BOPIS für Windows- und Android-Clients konfigurieren. Weitere Informationen zur Installation einer geteilten Hardware-Station finden Sie unter [Konfiguration und Installation der Retail-Hardware-Station](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).

1. Wechseln Sie zu **Retail und Commerce \> Kanaleinstellungen \> POS-Einstellungen \> Kassen**.
2. Wählen Sie Kasse **SANFRAN-5** und dann **Bearbeiten** aus.
3. Ändern Sie den Wert im Feld **Hardwareprofil** von **HW002** in **HW001** und wählen dann **Speichern** aus.
4. Um die Änderungen z synchronisieren, wechseln Sie zu **Retail and Commerce \> Retail and Commerce IT \> Vertriebsplan**.
5. Wählen Sie den Vertriebsplan **1090** und wählen Sie dann im Aktionsbereich **Jetzt ausführen**.
6. Wählen Sie **Ja** und dann **OK**, um die Datensynchronisation zu starten. 

### <a name="install-modern-pos"></a>Modern POS installieren

1. Wechseln Sie zu **Retail und Commerce \> Kanaleinstellungen \> POS-Einstellungen \> Geräte**.
2. Wählen Sie Gerät **SANFRANCIS-5**.
3. Wählen Sie im Aktionsbereich **Herunterladen** aus, und wählen Sie dann **Konfigurationsdatei** aus.
4. Wählen Sie zunächst **Herunterladen** und dann **Retail Modern POS** aus. 
5. Nach Download der **ModernPOSSetup.exe**-Datei wählen Sie **Datei öffnen**.

    ![Datei öffnen](./dev-itpro/media/PAYMENTS/openfile.png)

6. Wählen Sie **Weiter**, um den Installationsprozess zu durchlaufen. Wenn die Installation abgeschlossen ist, wählen Sie **Schließen**.

### <a name="activate-modern-pos"></a>Aktivieren Sie Modern POS

1. Wählen Sie auf dem Windows-Desktop die Option **Start** und geben Sie **Retail Modern POS** ein.
2. Wählen Sie die **Retail Modern POS**-Anwendung, um die Aktivierung zu starten.
3. Wählen Sie **Weiter**. Die Felder **Server-URL**, **Geräte ID** und **Registriernummer** sollten mithilfe von Informationen aus der Konfigurationsdatei voreingestellt werden, die Sie im vorherigen Verfahren heruntergeladen haben.
4. Wählen Sie **Aktivieren** aus.
5. Ein Authentifizierungsdialogfeld wird angezeigt. Wählen Sie das Konto aus, das die E-Mail-Adresse verwendet, die zuvor dem Mitarbeiter **000713 – Andrew Collette** zugeordnet war.

    > [!NOTE]
    > Wenn Sie noch keinen Mitarbeiter mit Ihrer Identität verknüpft haben, ist die Aktivierung nicht erfolgreich. Befolgen Sie in diesem Fall die Schritte im Abschnitt „Mitarbeiter Ihrer Identität zuordnen“ im Thema [Konfigurieren einer Dynamics 365 Commerce-Auswertungsumgebung](cpe-post-provisioning.md#associate-a-worker-with-your-identity).
    
6. Wenn Sie aufgefordert werden, das Gerät von Ihrer Organisation verwalten zu lassen, wählen Sie **Nur diese App**.
7. Wenn die Aktivierung abgeschlossen ist, wählen Sie **Erste Schritte**.

### <a name="enable-bopis-in-modern-pos"></a>Aktivieren Sie BOPIS in Modern POS

1. Melden Sie sich mit **000713** als Bediener-ID und **123** als Passwort bei Modern POS an.
2. Aktivieren Sie während der Wiedergabe des Einführungsvideos die beiden Kontrollkästchen in der unteren linken Ecke des Dialogfelds und schließen Sie das Dialogfeld.
3. Wenn Sie nicht aufgefordert werden, die Schicht zu schließen, scrollen Sie auf der Seite **Willkommen bei** nach rechts, wählen **Schicht schließen** und melden Sie sich dann wieder am POS an.
4. Wenn Sie nach dem Anmelden aufgefordert werden, wählen Sie **Ausführen von Vorgängen ohne Kassenlade**.
5. Auf der Seite **Willkommen bei** scrollen Sie nach rechts und wählen den Vorgang **Hardwarestation auswählen**.
6. Wählen Sie **Verwalten**, stellen Sie die **Hardwarestation verwenden**-Option auf **Ein** ein und wählen Sie **OK** aus.
7. Melden Sie sich am POS ab und wieder an.
8. Nachdem Sie angemeldet sind, wählen Sie **Neue Schicht öffnen** und dann **Schublade** aus.

## <a name="complete-a-bopis-scenario"></a>Schließen Sie ein BOPIS-Szenario ab

### <a name="create-a-storefront-order-for-in-store-pickup"></a>Erstellen Sie eine Storefront-Bestellung für die Abholung im Geschäft

1. Gehen Sie zu der URL, die Sie im Schritt [E-Commerce initialisieren](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) während der Umgebungskonfiguration angegeben haben.
2. Wählen Sie ein Element aus und dann **In den Einkaufskorb**.
3. Wählen Sie auf der Einkaufskorbseite **Abholung** für die Bestellposition aus, die Sie gerade hinzugefügt haben.
4. Geben Sie im **Auswählen eines Shops**-Dialogfeld **San Francisco** ein und wählen Sie dann die **Suche**-Taste.
5. Suchen Sie in der Ergebnisliste den Shop in San Francisco und wählen Sie **Hier abholen**.
6. Wählen Sie auf der Einkaufskorbseite **Als Gast auschecken** aus. 

    > [!NOTE]
    > Um mit dem Auschecken fortzufahren, müssen Sie den Cookie-Hinweis akzeptieren. Dieser Hinweis wird als Banner oben auf der Checkout-Seite angezeigt.

7. Geben Sie für die Kreditkartenzahlungsmethode die folgenden Details ein:

    - **Name des Karteninhabers:** Geben Sie einen beliebigen Namen ein.
    - **Kartennummer:** Geben Sie **4111-1111-1111-1111** ein.
    - **Ablaufdatum:** Geben Sie **10/20** ein.
    - **Kartenprüfwert (CVV)-Code:** Geben Sie **737** ein.

    > [!IMPORTANT]
    > Sie sollten unter keinen Umständen versuchen, die tatsächlichen Kreditkarteninformationen auf der Testseite zu verwenden.

8. Fahren Sie mit der Kaufabwicklung fort, indem Sie Details zur Rechnungsadresse eingeben und dann **Speichern und fortfahren** auswählen.
9. Wenn die Bestellung aufgegeben werden kann, wählen Sie **Auschecken**.

### <a name="synchronize-online-orders-to-the-back-office"></a>Synchronisieren Sie Online-Bestellungen mit dem Backoffice

Informationen zum Synchronisieren von Online-Bestellungen finden Sie unter [Onlineverkäufe und -zahlungen buchen](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments).

### <a name="pick-up-an-order-in-the-store"></a>Bestellung im Shop abholen

1. Melden Sie sich am POS an.
2. Auf der Seite **Willkommen bei** wählen Sie **Auftragserfüllung** aus
3. Wählen Sie in der Liste der Artikel zur Abholung die Position aus der Bestellung aus, die online aufgegeben wurde.
4. Wählen Sie **Abholen**, während die Bestellposition ausgewählt ist.

    Der Positionsartikel wird dem Transaktionsbildschirm hinzugefügt, und **$ 0,00** wird als fälliger Saldo angezeigt.

5. Wählen Sie den Restbetrag von **$ 0,00** oder wählen Sie eine Zahlungsmethode aus, um die Transaktion abzuschließen.

## <a name="troubleshooting"></a>Problembehandlung

### <a name="online-orders-that-are-retrieved-in-the-pos-have-a-non-zero-balance-due"></a>Bei Online-Bestellungen, die am POS abgerufen werden, ist ein Saldo ungleich null fällig

Wenn eine Bestellung für die Abholung im Geschäft abgerufen wird und der fällige Restbetrag nicht 0 (null) beträgt, stellen Sie sicher, dass Modern POS verwendet wird und die Hardwarestation aktiv ist. Wenn Cloud POS oder Modern POS für iOS verwendet wird, stellen Sie sicher, dass eine gemeinsam genutzte Hardwarestation aktiv ist. Zum Abrufen von Online-Zahlungen ist eine aktive Hardwarestation erforderlich.

### <a name="general-issues-with-payment-capture"></a>Allgemeine Probleme bei der Zahlungserfassung

Bei allen allgemeinen Problemen sollten Sie als ersten Schritt immer die Ereignisprotokolle der Modern POS- oder IIS-Hardwarestation (Internet Information Services) konsultieren. Sie finden diese Protokolle unter den folgenden Knoten im Windows-Ereignisprotokoll:

- Anwendungs- und Dienstprotokolle \> Microsoft \> Dynamics \> Commerce-ModernPOS
- Anwendungs- und Dienstprotokolle \> Microsoft \> Dynamics \> Commerce-Hardware Station

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Dynamics 365 Commerce-Auswertungsumgebung – Übersicht](cpe-overview.md)

[Bereitstellen einer Dynamics 365 Commerce-Auswertungsumgebung](provisioning-guide.md)

[Optionale Funktionen für eine Dynamics 365 Commerce-Auswertungsumgebung konfigurieren](cpe-optional-features.md)

[Dynamics 365 Commerce-Auswertungsumgebung – FAQ](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-Portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-Website](https://aka.ms/Dynamics365CommerceWebsite)

[Connector für Adyen-Zahlungen](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)

[Online-Zahlungsmittel mit dem Adyen Connector speichern](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector-listpi)

[Überblick über Omni-Channel-Zahlungen](https://docs.microsoft.com/dynamics365/commerce/omni-channel-payments)
