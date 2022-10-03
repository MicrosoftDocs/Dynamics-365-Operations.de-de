---
title: Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung in Frankreich
description: Dieser Artikel enthält Informationen, die Ihnen den Einstieg in das Add-On für die elektronische Rechnungsstellung für Frankreich erleichtern.
author: dkalyuzh
ms.date: 07/07/2022
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2022-00-02
ms.dyn365.ops.version: AX 10.0.29
ms.openlocfilehash: 3ac4af8c131e35d9a499d0d558c7cce1d4872b37
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573277"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-france"></a>Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung in Frankreich

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen, die Ihnen den Einstieg in die elektronische Rechnungsstellung für Frankreich erleichtern. Es führt Sie durch die Konfigurationsschritte, die im Regulatory Configuration Service (RCS) länderabhängig sind. Diese Schritte ergänzen die Schritte, die in [Erste Schritte mit dem Add-on für die elektronische Rechnungsstellung](e-invoicing-get-started.md) beschrieben sind.

## <a name="country-specific-configuration-for-french-chorus-pro-submission-fr-electronic-invoicing-feature"></a>Länderspezifische Konfiguration der Funktion zur elektronischen Rechnungsstellung für die Übermittlung mit dem französischen Chorus Pro (FR)

Zur Konfiguration der Funktion zur elektronischen Rechnungsstellung **Übermittlung mit französischer Chorus Pro (FR)** müssen Sie einige Schritte befolgen. Einige der Parameter aus der Konfiguration sind mit Standardwerten veröffentlicht. Diese Werte müssen überprüft und aktualisiert werden, damit sie Ihren Geschäftsbetrieb besser widerspiegeln.

### <a name="prerequisites"></a>Voraussetzungen

Bevor Sie mit den Verfahren in diesem Artikel beginnen, müssen Sie die folgenden Voraussetzungen erfüllen:

- Machen Sie sich mit der elektronischen Rechnungsstellung vertraut. Weitere Informationen finden Sie unter [Übersicht über die elektronische Rechnungsstellung](e-invoicing-service-overview.md).
- Melden Sie sich bei RCS an, und legen Sie die Elektronische Rechnungsstellung fest. Weitere Informationen finden Sie in folgenden Artikeln:

    - [Melden Sie sich für den Dienst für die elektronische Rechnungsstellung an und installieren Sie ihn](e-invoicing-sign-up-install.md)
    - [Einrichten von Azure-Ressourcen für die Elektronische Rechnungsstellung](e-invoicing-set-up-azure-resources.md)
    - [Das Add-In für Microservices in Lifecycle Services installieren](e-invoicing-install-add-in-microservices-lcs.md)
    - [Integration mit der elektronischen Rechnungsstellung aktivieren und einrichten](e-invoicing-activate-setup-integration.md): Verwenden Sie die Informationen aus diesem Artikel, um die Integration zwischen Ihrer Microsoft Dynamics 365 Finance oder Dynamics 365 Supply Chain Management App und dem Dienst zur elektronischen Rechnungserstellung zu aktivieren.
    - [NAF-Codes und Siret-Nummern](emea-fra-naf-codes-siret-numbers.md) und [NAF-Codes und Siret-Nummern einrichten](tasks/fr-00003-naf-codes-siret-numbers.md): Verwenden Sie die Informationen in diesen Artikeln, um NAF-Codes und Siret-Nummern in Ihren juristischen Personen einzurichten. 

- Ihre Organisation muss registriert sein, um mit Chorus Pro arbeiten zu können. Microsoft stellt die Integration mit Chorus Pro im OAuth2-Modus über eine Anwendungsprogrammierschnittstelle (API) bereit. Ausführliche Informationen zur Chorus-Pro-Registrierung und Anwendungsaktivierung finden Sie unter [offizielle Dokumentation](https://communaute.chorus-pro.gouv.fr/documentation/help-for-api-developers-in-oauth2-mode/).

    Registrieren Sie sich bei Chorus Pro wie folgt.

    1. Gehen Sie zum [PISTE-Portal](https://piste.gouv.fr/en/component/apiportal/registration), um mit Ihrer Registrierung zu beginnen. 
    2. Registrieren Sie eine Anwendung und aktivieren Sie Open-Authorization-(OAuth-)Anmeldeinformationen.
    3. Kopieren und speichern Sie die Client-ID der OAuth-Anmeldeinformationen und den geheimen Schlüssel. Sie werden diese Informationen in späteren Schritten verwenden.
    4. Gehen Sie zum [Chorus-Pro-Portal](https://portail.chorus-pro.gouv.fr/aife_csm/?id=aife_enrollment), um sich zu registrieren. 
    5. Erstellen Sie ein technisches Konto für den API-Zugriff. Weitere Informationen finden Sie unter [Ein technisches Konto für den API-Zugriff in der Produktion erstellen](https://communaute.chorus-pro.gouv.fr/documentation/creation-of-a-technical-account-for-an-api-access-in-production/).
    6. Kopieren Sie die Benutzer-ID des technischen Kontos und das Kennwort. Sie werden diese Informationen in späteren Schritten verwenden.

## <a name="country-specific-configuration-of-the-application-setup-for-the-french-chorus-pro-submission-fr-electronic-invoicing-feature"></a>Länderspezifische Konfiguration der Anwendungseinrichtung für die Funktion zur elektronischen Rechnungsstellung für die Übermittlung mit dem französischen Chorus Pro

Einige der Parameter aus der Funktion **Übermittlung mit dem französischen Chorus Pro (FR)** werden mit Standardwerten veröffentlicht. Bevor Sie die Funktion Elektronische Rechnungsstellung in der Umgebung des Dienstes bereitstellen, überprüfen Sie die Standardwerte und aktualisieren Sie sie bei Bedarf, damit sie Ihren geschäftlichen Vorgang besser widerspiegeln.

1. Legen Sie im Azure Key Vault die Geheimnisse und die entsprechenden Verweise darauf an. Weitere Informationen finden Sie unter [Kundenzertifikate und Geheimnisse](e-invoicing-customer-certificates-secrets.md).
2. Importieren Sie die neueste Version der Globalisierungsfunktion zur **Übermittlung mit dem französischen Chorus Pro (FR)**, wie unter [Importieren von Funktionen aus dem globalen Repository](e-invoicing-import-feature-global-repository.md) beschrieben.
3. Erstellen Sie eine Kopie der importierten Globalisierungsfunktion und wählen Sie Ihren Konfigurationsanbieter aus. Weitere Informationen finden Sie unter [Eine Globalisierungsfunktion erstellen](e-invoicing-create-new-globalization-feature.md).
4. Überprüfen Sie auf der Registerkarte **Versionen**, ob die **Entwurf**-Version ausgewählt ist.
5. Wählen Sie auf der Registerkarte **Einstellungen** im Raster die Funktion **Abgeleitete UBL-Verkaufsrechnungen**.
6. Wählen Sie **Bearbeiten** und dann in der Registerkarte **Verarbeitungspipeline** im Abschnitt **Verarbeitungspipeline** **(Vorschauversion) Integration mit dem französischen Chorus Pro** mit dem Aktionsnamen **Französisches Chorus Pro einreichen**.
7. Wählen Sie im Abschnitt **Parameter** das Feld **Name des Client-ID-Geheimnisses** und dann den Namen des Geheimnisses aus, das Sie für die Client-ID im Key Vault erstellt haben.
8. Wählen Sie im Feld **Name des geheimen Clientschlüssels** den geheimen Namen aus, den Sie für die geheimen Clientschlüssel im Key Vault erstellt haben.
9. Wählen Sie im Feld **Name des Geheimnisses der technischen Anmeldung** den Namen des Geheimnisses aus, das Sie für die technische Kontoanmeldung im Key Vault erstellt haben.
10. Wählen Sie im Feld **Name des Geheimnisses des technischen Kennworts** den Namen des Geheimnisses aus, das Sie für das technische Kontokennwort im Key Vault erstellt haben.
11. Wählen Sie in der Registerkarte **Verarbeitungspipeline** im Abschnitt **Verarbeitungspipeline** **Integration mit dem französischen Chorus Pro** mit dem Aktionsnamen **Anforderungsstatus zum französischen Chorus Pro**.
12. Wählen Sie im Abschnitt **Parameter** das Feld **Name des Client-ID-Geheimnisses** und dann den Namen des Geheimnisses aus, das Sie für die Client-ID im Key Vault erstellt haben.
13. Wählen Sie im Feld **Name des geheimen Clientschlüssels** den geheimen Namen aus, den Sie für die geheimen Clientschlüssel im Key Vault erstellt haben.
14. Wählen Sie im Feld **Name des Geheimnisses der technischen Anmeldung** den Namen des Geheimnisses aus, das Sie für die technische Kontoanmeldung im Key Vault erstellt haben.
15. Wählen Sie im Feld **Name des Geheimnisses des technischen Kennworts** den Namen des Geheimnisses aus, das Sie für das technische Kontokennwort im Key Vault erstellt haben.
16. Klicken Sie auf **Speichern** und schließen Sie die Seite.
17. Wiederholen Sie die Schritte 6 bis 16 für die Einrichtung der Funktionen **Abgeleitete UBL-Projektrechnung**, **Abgeleitete UBL-Verkaufsgutschrift** und **Abgeleitete UBL-Projektgutschrift**.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Informationen zum Add-On für die elektronische Rechnungsstellung](e-invoicing-service-overview.md)
- [Erste Schritte mit der Dienstverwaltung des Add-Ons für die elektronische Rechnungsstellung](e-invoicing-get-started-service-administration.md)
- [Erste Schritte mit dem Add-On zur elektronischen Rechnungsstellung](e-invoicing-get-started.md)
