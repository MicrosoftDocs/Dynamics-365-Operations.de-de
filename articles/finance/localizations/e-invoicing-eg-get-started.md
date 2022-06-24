---
title: Elektronische Rechnungsstellung für Ägypten
description: Dieser Artikel enthält Informationen, die Ihnen den Einstieg in die Elektronische Rechnungsstellung für Ägypten in Microsoft Dynamics 365 Finance und Dynamics 365 Supply Chain Management erleichtern.
author: gionoder
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
ms.openlocfilehash: c2a46ef938c5dee62c0d0acd1648584df344c81a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904411"
---
# <a name="electronic-invoicing-for-egypt"></a>Elektronische Rechnungsstellung für Ägypten

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen, die Ihnen den Einstieg in die elektronische Rechnungsstellung für Ägypten erleichtern. Es führt Sie durch die Konfigurationsschritte, die im Regulatory Configuration Service (RCS) länderabhängig sind. Diese Schritte ergänzen die Schritte, die unter [Elektronische Rechnungsstellung festlegen](e-invoicing-set-up-overview.md) beschrieben sind.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie mit den Verfahren in diesem Artikel beginnen, müssen Sie die folgenden Voraussetzungen erfüllen:

- Machen Sie sich mit der Elektronischen Rechnungsstellung vertraut, wie sie in [Übersicht über die Elektronische Rechnungsstellung](e-invoicing-service-overview.md) beschrieben ist.
- Melden Sie sich bei RCS an, und legen Sie die Elektronische Rechnungsstellung fest. Weitere Informationen finden Sie in folgenden Themen:

    - [Melden Sie sich für den Dienst für die elektronische Rechnungsstellung an und installieren Sie ihn](e-invoicing-sign-up-install.md)
    - [Einrichten von Azure-Ressourcen für die Elektronische Rechnungsstellung](e-invoicing-set-up-azure-resources.md)
    - [Das Add-In für Microservices in Lifecycle Services installieren](e-invoicing-install-add-in-microservices-lcs.md)
    
- Aktivieren Sie die Integration zwischen Ihrer Microsoft Dynamics 365 Finance- oder Dynamics 365 Supply Chain Management-Anwendung und dem Dienst für die elektronische Rechnungsstellung, wie in [Integration mit der elektronischen Rechnungsstellung aktivieren und einrichten](e-invoicing-activate-setup-integration.md) beschrieben.
- Erstellen Sie ein digitales Zertifikatsgeheimnis in Azure Key Vault und legen Sie es wie in [Kundenzertifikate und Geheimnisse](e-invoicing-customer-certificates-secrets.md) beschrieben fest. Zu Testzwecken stellt die ägyptische Steuerbehörde spezielle digitale Testzertifikate zur Verfügung, die nur während der Test- und Lösungsvalidierungsphase verwendet werden dürfen. Weitere Informationen finden Sie auf der Website der ägyptischen Steuerbehörde unter dem Link, der in [Egyptian e-invoicing SDK](https://sdk.invoicing.eta.gov.eg/faq/) angegeben ist.

## <a name="country-specific-configuration-for-the-egyptian-electronic-invoice-eg-feature"></a>Länderspezifische Konfiguration für die Funktion der ägyptischen elektronischen Rechnung (EG)

Einige der Parameter aus der Funktion **Elektronische Rechnungsstellung (EG)** werden mit Standardwerten veröffentlicht. Bevor Sie die Funktion Elektronische Rechnungsstellung in der Umgebung des Dienstes bereitstellen, überprüfen Sie die Standardwerte und aktualisieren Sie sie bei Bedarf, damit sie Ihren geschäftlichen Vorgang besser widerspiegeln.

1. Importieren Sie die neueste Version der **Globalisierungsfunktion für elektronische Rechnungen (EG)**, wie unter [Importieren von Funktionen aus dem globalen Repository](e-invoicing-import-feature-global-repository.md) beschrieben.
2. Erstellen Sie eine Kopie der importierten Funktion Globalisierung und wählen Sie Ihren Konfigurationsanbieter dafür aus, wie in [Erstellen einer Funktion Globalisierung](e-invoicing-create-new-globalization-feature.md) beschrieben.
3. Überprüfen Sie auf der Registerkarte **Versionen**, ob die **Entwurf**-Version ausgewählt ist.
4. Wählen Sie auf der Registerkarte **Einstellungen** im Raster die Funktion **Abgeleitete Verkaufsrechnungen**.
5. Wählen Sie **Bearbeiten** aus.
6. Wählen Sie auf der Registerkarte **Verarbeitungspipeline** im Abschnitt **Verarbeitungspipeline** die Option **Json-Dokument für die ägyptische Steuerbehörde signieren**.
7. Wählen Sie im Bereich **Parameter** die Option **Zertifikatsname** und wählen Sie dann den Namen des von Ihnen erstellten digitalen Zertifikats.
8. Wählen Sie im Bereich **Pipeline verarbeiten** die Option **Integration mit Egyptian ETA Service**. Wiederholen Sie diesen Schritt für die beiden Vorkommen dieser Aktion.
9. Wählen Sie im Abschnitt **Parameter** die **Webdienst-URL** und **Login-Dienst-URL**. Prüfen Sie dann die URL-Parameter. Um die Test- und Produktions-URL zu erhalten, gehen Sie auf die Website der ägyptischen Steuerbehörde, indem Sie den Link verwenden, der in [Egyptian e-invoicing SDK](https://sdk.invoicing.eta.gov.eg/faq/) angegeben ist.
10. Klicken Sie auf **Speichern** und schließen Sie die Seite.
11. Wiederholen Sie die Schritte 4 bis 10 für die Einrichtung der Funktion **Projektrechnung abgeleitet**.

## <a name="country-specific-configuration-for-the-egyptian-electronic-invoice-eg-application-setup"></a>Länderspezifische Konfiguration für die Einrichtung der ägyptischen Anwendung für elektronische Rechnungen (EG)

Es gibt Parameter, die in Ihrer Finance oder Supply Chain Management Umgebung festgelegt werden müssen. Sie können diese Einrichtung an einem von zwei Orten vornehmen:

- Direkt in Ihrer Finance oder Supply Chain Management Umgebung. Weitere Informationen finden Sie unter [Parameter für die Elektronische Rechnungsstellung einrichten](e-invoicing-set-up-parameters.md).
- In RCS. Im Rahmen der Einrichtung der Funktion Elektronische Rechnungsstellung können Sie alle Parameter definieren und sie dann direkt in Ihrer Finance oder Supply Chain Management Umgebung bereitstellen, wenn Sie die Funktion Elektronische Rechnungsstellung einrichten.

Für beide Optionen sind die Parameter identisch. Wenn Sie Ihre erste Funktion im Dienst für die elektronische Rechnungsstellung einrichten, empfehlen wir Ihnen, die folgenden Schritte zu befolgen, um die Parameter in RCS festzulegen und sie dann in Ihrer verbundenen Anwendung bereitzustellen.

> [!NOTE]
> Einige Funktionen der Elektronischen Rechnungsstellung enthalten möglicherweise einen vordefinierten Satz anwendungsspezifischer Parameter für Finance oder Supply Chain Management. In diesem Fall sollten Sie sich vergewissern, dass die Daten korrekt sind. Andernfalls müssen Sie die Parameter manuell festlegen.

1. Suchen Sie die Kopie der Funktion **Elektronische Rechnung (EG)** Globalisierung, die Sie erstellt haben.
2. Überprüfen Sie auf der Registerkarte **Versionen**, ob die **Entwurf**-Version ausgewählt ist.
3. Wählen Sie auf der Registerkarte **Einrichtungen** **Anwendungseinrichtung** aus.
4. Wählen Sie im Feld **Verbundene Anwendungen** die Anwendung, in der Sie die Parameter bereitstellen möchten.
5. Auf der Seite **Elektronische Belege** wählen Sie **Hinzufügen**, um einen Datensatz zu erstellen.
6. Fügen Sie in das Feld **Tabellenname** **CustInvoiceJour** ein.
7. Fügen Sie im Feld **Kontext** einen Verweis auf den Namen der Zuordnung **Kundenrechnungskontext** hinzu. Die Konfiguration lautet **Kundenrechnungskontextmodell**.
8. Fügen Sie im Feld **Zuordnung elektronischer Belege** einen Verweis auf den Zuordnungsnamen **Kundenrechnung** hinzu. Die Konfiguration lautet **Rechnungsmodell-Zuordnung**.
9. Wählen Sie **Speichern** aus.
10. Auf der Seite **Antworttypen** wählen Sie **Hinzufügen**.
11. Geben Sie im Feld **Antworttyp** den Text **Antwort** ein.
12. Geben Sie in das Feld **Beschreibung** **Antwort verarbeiten** ein.
13. Wählen Sie im Feld **Übermittlungsstatus** die Option **Ausstehend** aus.
14. Wählen Sie im Feld **Modellzuordnung** die Option **Import von Nachrichten als Antwort**. Die Konfiguration ist **Ägyptische Antwort Nachrichtenimport (EG)**.
15. Wählen Sie **Speichern** aus.
16. Wählen Sie **Hinzufügen** aus.
17. Geben Sie in das Feld **Antworttyp** **ResponseData** ein.
18. Geben Sie in das Feld **Beschreibung** **Antwortdaten verarbeiten** ein.
19. Wählen Sie im Feld **Übermittlungsstatus** die Option **Ausstehend** aus.
20. Wählen Sie im Feld **Name der Entität** **SalesInvoiceHeaderV2Entity**.
21. Wählen Sie im Feld **Modellzuordnung** die Option **Response Datenimport**. Die Konfiguration lautet **Ägyptisches Antwortdaten-Importformat (EG)**.
22. Klicken Sie auf **Speichern** und schließen Sie die Seite.
23. Schließen Sie die Seite.

Wie Sie eine Funktion in der Umgebung des Dienstes und eine Anwendungseinrichtung für die mit Finance oder Supply Chain Management verbundene Anwendung bereitstellen, erfahren Sie unter [Globalisierungsfunktion vervollständigen, veröffentlichen und bereitstellen](e-invoicing-complete-publish-deploy-globalization-feature.md).

## <a name="privacy-notice"></a>Datenschutzhinweis

Die Aktivierung der Funktion **Ägyptische Elektronische Rechnungsstellung (EG)** erfordert möglicherweise die Übermittlung begrenzter Daten. Zu diesen Daten gehört die Steueridentifikationsnummer der Organisation. Die Daten werden an Drittanbieter übermittelt, die von der Steuerbehörde autorisiert wurden, elektronische Rechnungen in dem vordefinierten Format an diese Steuerbehörde zu senden, das für die Integration mit dem Webservice der Regierung erforderlich ist. Ein Administrator kann die Funktion unter **Organisationsverwaltung** \> **Einrichtung** \> **Parameter für elektronische Belege** aktivieren und deaktivieren. Wählen Sie auf der Registerkarte **Funktionen** die Zeile mit der Funktion **Elektronische Rechnungen für Ägypten (EG)** aus und treffen Sie die entsprechende Auswahl. Daten, die aus externen Systemen in diesen Dynamics 365 Online-Service importiert werden, unterliegen unserer [Datenschutzerklärung](https://go.microsoft.com/fwlink/?LinkId=512132). Weitere Informationen finden Sie im Abschnitt „Datenschutz“ in der länderspezifischen Dokumentation der Funktionen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Informationen zur elektronischen Rechnungsstellung](e-invoicing-service-overview.md)
- [Erste Schritte mit der Dienstverwaltung für die elektronische Rechnungsstellung](e-invoicing-get-started-service-administration.md)
- [Erste Schritte mit der elektronischen Rechnungsstellung](e-invoicing-get-started.md)
- [Elektronische Rechnungen für Debitoren in Ägypten](emea-egy-e-invoices.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
