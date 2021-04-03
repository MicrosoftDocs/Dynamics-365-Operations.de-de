---
title: Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung in Ägypten
description: Dieses Thema enthält Informationen, die Ihnen den Einstieg in das Add-On für die elektronische Rechnungsstellung für Ägypten in Finance und Supply Chain Management erleichtern.
author: gionoder
manager: AnnBe
ms.date: 02/26/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 68ee08226f440e850a080600dbf5e16768b45e43
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592597"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-egypt"></a>Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung in Ägypten

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Dieses Thema enthält Informationen, die Ihnen den Einstieg in das Add-On für die elektronische Rechnungsstellung für Ägypten erleichtern. Das Thema führt Sie durch die Konfigurationsschritte, die in Regulatory Configuration Services (RCS) länderabhängig sind, und ergänzen die unter [Erste Schritte mit dem Add-On zur elektronischen Rechnungsstellung](e-invoicing-get-started.md) beschriebenen Schritte.

## <a name="country-specific-configuration-for-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Länderspezifische Konfiguration der Funktion zur elektronischen Rechnungsstellung für die elektronische Rechnung für Ägypten (EG)

Um die Funktion zur elektronischen Rechnungsstellung für die elektronische Rechnung für Ägypten (EG) zu konfigurieren, müssen einige Schritte ausgeführt werden. Einige der Parameter aus den Konfigurationen werden mit Standardwerten veröffentlicht. Sie müssen daher überprüft und aktualisiert werden, um besser zu Ihrem Geschäftsvorgang zu passen.

### <a name="prerequisites"></a>Voraussetzungen

Vor der Ausführung der Schritte in diesem Abschnitt müssen Sie:

- Erstellen Sie ein digitales Zertifikatgeheimnis, wie im Abschnitt **Ein digitales Zertifikatgeheimnis erstellen** in [Erste Schritte in der Add-On-Dienstverwaltung für die elektronische Rechnungsstellung](e-invoicing-get-started-service-administration.md) beschrieben. Zu Testzwecken stellt die ägyptische Steuerbehörde spezielle digitale Testzertifikate zur Verfügung, die nur während der Test- und Lösungsvalidierungsphase verwendet werden dürfen. Weitere Informationen finden Sie auf der Website der ägyptischen Steuerbehörde unter dem Link im [Ägyptischen E-Invoicing-SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/).
- Erstellen Sie für Ihr Unternehmen eine Funktion zur elektronischen Rechnungsstellung für elektronische Rechnungen für Ägypten (EG), wie im Abschnitt **Eine elektronische Rechnungsstellungsfunktion unter Ihrem Organisationsanbieter erstellen** des Themas [Erste Schritte mit dem Add-On zur elektronischen Rechnungsstellung](e-invoicing-get-started.md) beschrieben.

1. Wählen Sie in RCS im Abschnitt **Funktionen** des Arbeitsbereichs **Globalisierungsfunktion** die Kachel **Add-On für die elektronische Rechnungsstellung** aus.
2. Auf der Seite **Add-On-Funktionen für die elektronische Rechnungsstellung** überprüfen Sie, ob die von Ihnen erstellte elektronische Rechnungsfunktion **Elektronische Rechnungen für Ägypten (EG)** ausgewählt ist.
3. Überprüfen Sie auf der Registerkarte **Versionen**, ob die **Entwurf**-Version ausgewählt ist.
4. Wählen Sie im Raster auf der Registerkarte **Einrichtungen** die Funktionseinrichtung **Verkaufsrechnung** aus.
5. Wählen Sie **Bearbeiten** und auf der **Aktionen**-Registerkarte in der **Aktionen**-Feldgruppe **JSON-Dokument für die ägyptische Steuerbehörde unterzeichnen** aus.
6. Wählen Sie in der Feldgruppe **Parameter** den Parameter **Zertifikatname** aus, und wählen Sie den Namen des digitalen Zertifikats aus, das für die Verwendung mit der Funktion für die elektronische Rechnungsstellung erstellt wurde.
7. Wählen Sie in der **Aktionen**-Feldgruppe **In ägyptischen ETA-Dienst integrieren** aus. Wiederholen Sie diesen Schritt für die beiden Vorkommen dieser Aktion.
8. Wählen Sie in der **Parameter**-Feldgruppe **Webdienst-URL** und **Anmeldedienst-URL** aus, und überprüfen Sie gegebenenfalls die URL-Parameter. Besuchen Sie die Website der ägyptischen Steuerbehörde unter dem Link im [Ägyptischen E-Invoicing-SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/), um die Test- und Produktions-URL zu erhalten.
9. Wählen Sie **Speichern** aus und schließen Sie die Seite.
10. Informationen zum Konfigurieren der Anwendungseinrichtung finden Sie unter [Erste Schritte mit dem Add-On zur elektronischen Rechnungsstellung](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-the-application-setup-for-the-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Länderspezifische Konfiguration der Anwendungseinrichtung für die Funktion zur elektronischen Rechnungsstellung für die elektronische Rechnung für Ägypten (EG)

Für die Konfiguration der Anwendungseinrichtung der Funktion zur elektronischen Rechnungsstellung für **Elektronische Rechnungen für Ägypten (EG)** müssen bestimmte Schritte ausgeführt werden. Sie müssen diese Schritte ausführen, bevor Sie Ihre Funktion für die elektronische Rechnungsstellung in Ihrer Add-On-Serviceumgebung für die elektronische Rechnungsstellung bereitstellen.

### <a name="prerequisites"></a>Voraussetzungen

Bevor Sie den in diesem Abschnitt beschriebenen Vorgang abschließen, erstellen und initiieren Sie eine Funktion zur elektronischen Rechnungsstellung für **Elektronische Rechnungen für Ägypten (EG)**, um die Anwendungseinrichtung für die Funktion zur elektronischen Rechnungsstellung für **Elektronische Rechnungen für Ägypten (EG)** zu konfigurieren, wie im Abschnitt **Anwendungseinrichtung konfigurieren** im Thema [Erste Schritte mit dem Add-On zur elektronischen Rechnungsstellung](e-invoicing-get-started.md) beschrieben.

1. Wählen Sie in RCS im Abschnitt **Funktionen** des Arbeitsbereichs **Globalisierungsfunktion** die Kachel **Add-On für die elektronische Rechnungsstellung** aus.
2. Auf der Seite **Add-On-Funktionen für die elektronische Rechnungsstellung** überprüfen Sie, ob die elektronische Rechnungsfunktion **Elektronische Rechnungen für Ägypten (EG)** ausgewählt ist.
3. Überprüfen Sie auf der Registerkarte **Versionen**, ob die **Entwurf**-Version ausgewählt ist.
4. Wählen Sie auf der **Einrichtungen**-Registerkarte **Anwendungseinrichtung** und im Feld **Verbundene Anwendung** die Anwendung aus, in der Sie bereitstellen möchten.
5. Überprüfen Sie im Feld **Tabellenname**, ob die Kundenrechnungserfassung ausgewählt ist.
6. Wählen Sie **Antworttypen** und dann **Neu** aus.
7. Geben Sie im Feld **Antworttyp** „Antwort“ ein, und geben Sie im Feld **Beschreibung** „Beschreibung“ ein.
8. Wählen Sie im Feld **Übermittlungsstatus** die Option **Ausstehend** aus.
9. Wählen Sie im Feld **Modellzuordnung** die Option **Modellzuordnung aus Antwortnachricht** mit **(Vorschau) Importformat für Antwortnachrichten** und dann **Speichern** aus.
10. Wählen Sie **Neu** aus, und geben Sie im Feld **Antworttyp** „ResponseData“ als festen Wert ein. Geben Sie im Feld **Beschreibung** „Beschreibung“ ein.
11. Wählen Sie im Feld **Übermittlungsstatus** die Option **Ausstehend** aus.
12. Wählen Sie im **Name der Datenentität**-Feld **Verkaufsrechnungskopfzeilen V2** aus.
13. Wählen Sie im Feld **Modellzuordnung** die Option **Import von Antwortdaten für Ägypten** mit **(Vorschau) Import von Antwortdaten für Ägypten** und dann **Speichern** aus.
14. Informationen zum Bereitstellen der Funktion für die elektronische Rechnungsstellung finden Sie unter [Erste Schritte mit dem Add-On zur elektronischen Rechnungsstellung](e-invoicing-get-started.md).

## <a name="privacy-notice"></a>Datenschutzhinweis

Zur Aktivierung der Funktion **Elektronische Rechnungen für Ägypten (EG)** müssen möglicherweise nur begrenzte Daten gesendet werden, einschließlich der Steuerregistrierungskennung für die Organisation. Diese Daten werden an von der Steuerbehörde autorisierte Drittagenturen weitergeleitet, um elektronische Rechnungen in dem für die Integration in den Webdienst der Behörde erforderlichen Format an diese Steuerbehörde zu senden. Ein Administrator kann die Funktion aktivieren und deaktivieren, indem er zu **Organisationsverwaltung** > **Einrichtung** > **Parameter elektronischer Dokumente** navigiert. Wählen Sie auf der Registerkarte **Funktionen** die Zeile mit der Funktion **Elektronische Rechnungen für Ägypten (EG)** aus und treffen Sie die entsprechende Auswahl. Daten, die aus diesen externen Systemen in diesen Dynamics 365-Onlinedienst importiert werden, unterliegen unseren [Datenschutzbestimmungen](https://go.microsoft.com/fwlink/?LinkId=512132). Weitere Informationen finden Sie in den Abschnitten zum Datenschutz in der landesspezifischen Funktionsdokumentation.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Informationen zum Add-On für die elektronische Rechnungsstellung](e-invoicing-service-overview.md)
- [Erste Schritte mit der Dienstverwaltung des Add-Ons für die elektronische Rechnungsstellung](e-invoicing-get-started-service-administration.md)
- [Erste Schritte mit dem Add-On zur elektronischen Rechnungsstellung](e-invoicing-get-started.md)
- [Elektronische Rechnungen für Debitoren in Ägypten](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
