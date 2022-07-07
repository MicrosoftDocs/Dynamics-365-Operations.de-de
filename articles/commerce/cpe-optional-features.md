---
title: Optionale Funktionen für eine Dynamics 365 Commerce-Sandboxumgebung konfigurieren
description: In diesem Artikel wird erläutert, wie optionale Funktionen für eine Microsoft Dynamics 365 Commerce-Sandboxumgebung konfiguriert werden.
author: psimolin
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 201628eb0c3e81d5fee0df9e53d93f5b1839adfb
ms.sourcegitcommit: 252cb41c3029b623354698463f7b44a29fd9f184
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9013237"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-sandbox-environment"></a>Optionale Funktionen für eine Dynamics 365 Commerce-Sandboxumgebung konfigurieren

[!include [banner](includes/banner.md)]

In diesem Artikel wird erläutert, wie optionale Funktionen für eine Microsoft Dynamics 365 Commerce-Sandboxumgebung konfiguriert werden.

## <a name="prerequisites"></a>Voraussetzungen

Wenn Sie eine Demo der Transaktions-E-Mail-Funktionen ausführen möchten, müssen die folgenden Voraussetzungen erfüllt sein:

- Ihnen steht ein E-Mail-Server (Simple Mail Transfer Protocol \[SMTP\]-Server) zur Verfügung, der über das Microsoft Azure-Abonnement verwendet werden kann, auf dem Sie die Sandboxumgebung bereitstellen.
- Sie verfügen über den vollqualifizierten Domänennamen (FQDN)/die vollqualifizierte IP-Adresse, die SMTP-Portnummer und die Authentifizierungsdetails des Servers.

## <a name="configure-the-image-back-end"></a>Konfigurieren Sie das Image-Backend

### <a name="find-your-media-base-url"></a>Auffinden Ihrer medienbasierten URL

> [!NOTE]
> Bevor Sie diesen Vorgang abschließen können, müssen Sie die Schritte in [Richten Sie Ihre Site in Commerce ein](cpe-post-provisioning.md#set-up-your-e-commerce-sites) abschließen.

1. Melden Sie sich beim Commerce-Website-Generator mit der URL an, die Sie bei der Initialisierung von E-Commerce während der Bereitstellung notiert haben (siehe [E-Commerce initialisieren](provisioning-guide.md#initialize-e-commerce)).
1. Öffne die Website **Fabrikam**, **Adventure Works** oder **Adventure Works Business**, mit der Sie arbeiten möchten.
1. Wählen Sie im linken Menü **Medienbibliothek** aus.
1. Wählen Sie ein einzelnes Image-Medienobjekt aus.
1. Suchen Sie im Eigenschafteninspektor rechts die Eigenschaft **Öffentliche URL**. Der Wert ist eine URL. Hier ist ein Beispiel:

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.

1. Ersetzen Sie den letzten Bezeichner in der URL (**MA1nQC** im vorherigen Beispiel) durch die Zeichenfolge **search?fileName=**. So sieht die Beispiel-URL nach dieser Änderung aus:

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    Diese URL ist Ihre Mediendatenbank-URL. Machen Sie sich eine Notiz davon.

### <a name="update-the-media-base-url"></a>Aktualisieren der medienbasierten URL

1. Melden Sie sich bei der Commerce-Zentralverwaltung an.
1. Verwenden Sie das Menü auf der linken Seite, um zu **Module \> Retail and Commerce \> Kanaleinrichtung \> Kanalprofile** zu gehen.
1. Wählen Sie **Bearbeiten** aus.
1. Ersetzen Sie unter **Profileigenschaften** den Wert für die Eigenschaft **Media Server-Basis-URL** durch die medienbasierte URL, die Sie zuvor erstellt haben.
1. Wählen Sie den Kanal mit der Bezeichnung **scXXXXXXXXX** aus.
1. Wählen Sie unter **Profileigenschaften** die Option **Hinzufügen** aus.
1. Wählen Sie für die hinzugefügte Eigenschaft **Media Server-Basis-URL** als Eigenschaftsschlüssel aus. Geben Sie als Eigenschaftswert die zuvor erstellte Media Base-URL ein.
1. Wählen Sie **Speichern** aus.

## <a name="configure-and-test-the-email-server"></a>Den E-Mail-Server konfigurieren und testen

> [!NOTE]
> Der SMTP-Server oder E-Mail-Dienst, den Sie hier eingeben, muss über das Azure-Abonnement zugänglich sein muss, das Sie für die Umgebung verwenden.

1. Melden Sie sich bei der Commerce-Zentralverwaltung an.
1. Verwenden Sie das Menü links, um zu **Module \> Einzelhandel und Handel \> Zentralverwaltungs-Setup \> Parameter \> E-Mail-Parameter** zu wechseln.
1. Geben Sie auf der Registerkarte **SMTP-Einstellungen** im Feld **Name des SMTP-Servers** den vollständig qualifizierten Namen (FQDN) oder die IP-Adresse Ihres SMTP-Servers oder E-Mail-Dienstes an.
1. Geben Sie im Feld **SMTP-Portnummer** die Portnummer ein. (Wenn Sie Secure Sockets Layer \[SSL\] nicht verwenden, lautet die Standardportnummer **25**.)
1. Wenn eine Authentifizierung erforderlich ist, geben Sie Werte in das Feld **Benutzername** und **Kennwort** ein.
1. Wählen Sie **Speichern**.
1. Wählen Sie **Aktualisieren** aus.
1. Wählen Sie auf der Registerkarte **Test-E-mail** im Feld **E-Mail-Anbieter** die Option **SMTP** aus.
1. Geben Sie im Feld **Senden an** die E-Mail-Adresse ein, an die die Test-E-Mail gesendet werden soll.
1. Wählen Sie **Test-E-Mail senden** aus.

## <a name="configure-email-templates"></a>Konfigurieren der E-Mail-Vorlagen

Für jedes Transaktionsereignis, für das Sie E-Mails senden möchten, müssen Sie die E-Mail-Vorlage mit einer gültigen Absender-E-Mail-Adresse aktualisieren.

1. Melden Sie sich bei der Commerce-Zentralverwaltung an.
1. Verwenden Sie das Menü links, um zu **Module \> Einzelhandel und Handel \> Zentralverwaltungs-Setup \> Parameter \> Organisations-E-Mail-Vorlagen** zu wechseln.
1. Wählen Sie **Liste anzeigen** aus.
1. Führen Sie für jede Vorlage in der Liste die folgenden Schritte aus:

    1. Geben Sie im Feld **E-Mail des Absenders** die E-Mail-Adresse des Absenders ein.
    1. Optional: Geben Sie im Feld **Absendername** den Namen ein, der als Absendername verwendet werden soll.

1. Wählen Sie **Speichern**.

## <a name="customize-email-templates"></a>E-Mail-Vorlagen anpassen

Möglicherweise möchten Sie die E-Mail-Vorlagen so anpassen, dass sie unterschiedliche Bilder verwenden. Oder Sie möchten die Links in den Vorlagen aktualisieren, damit sie in Ihre Sandboxumgebung gelangen. In dieser Prozedur wird erläutert, wie Sie die Standardvorlagen herunterladen, anpassen und die Vorlagen im System aktualisieren.

1. Laden Sie über einen Webbrowser die [Microsoft Dynamics 365 Commerce-Demostandard-E-Mail-Vorlagen-ZIP-Datei](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) auf Ihren lokalen Computer herunter. Diese Datei enthält die folgenden HTML-Dokumente:

    - Auftragsbestätigungsvorlage
    - Geschenkkartenvorlage ausstellen
    - Neue Auftragsvorlage
    - Verpackungsvorlage
    - Entnahmevorlage

1. Passen Sie die Vorlagen mit einem Text- oder HTML-Editor an. Schauen Sie sich die Lister der [unterstützten Token](#supported-tokens-in-the-email-template) später in diesem Artikel an.
1. Melden Sie sich bei Commerce an.
1. Navigieren Sie über das Menü links zu **Module \> Organizationsverwaltung \> Einstellungen \> Organisations-E-Mail-Vorlagen**.
1. Erweitern Sie die Liste auf der linken Seite, um alle Vorlagen anzuzeigen.
1. Gehen Sie für jede Vorlage, die Sie anpassen möchten, folgendermaßen vor:

    1. Wählen Sie die Vorlage in der Liste aus.
    1. Wählen Sie unter **Inhalt der E-Mail-Nachricht** die entsprechende Sprachversion in der Liste aus. (Die Standardsprache lautet **en-us**.)
    1. Wählen Sie uner **Inhalt der E-Mail-Nachricht** die Option **Bearbeiten** aus. Der Bereich **E-Mail-Vorlage hochladen** wird angezeigt.
    1. Wählen Sie **Durchsuchen** aus, und finden Sie die HTML-Datei mit dem angepassten Inhalt.
    1. Wählen Sie **Hochladen** aus. Die Vorlage wird in das System hochgeladen und eine Vorschau wird angezeigt.
    1. Wählen Sie **OK**.
    1. Optional: Passen Sie die Eigenschaft **Betreff** der Vorlage an.
    1. Wählen Sie **Speichern**.

### <a name="supported-tokens-in-the-email-template"></a>Unterstützte Token in der E-Mail-Vorlage

Diese Token werden beim Rendern per E-Mail durch die tatsächlichen Werte ersetzt, die für den Debitor und die Debitorenbestellung gelten.

#### <a name="sales-order"></a>Auftrag

Die folgenden Token gelten für den gesamten Auftrag.

| Name des Token | Token |
|-------------------|-------|
| Bestellnummer      | %salesid% |
| Debitorenname   | %customername% |
| Lieferadresse  | %deliveryaddress% |
| Rechnungsadresse   | %customeraddress% |
| Auftragsdatum        | %shipdate% |
| Liefermodus     | %modeofdelivery% |
| Skonto          | %discount% |
| Mehrwertsteuer         | %tax% |
| Auftrag gesamt       | %total% |

#### <a name="sales-line"></a>Verkaufsposition

Die folgenden Token werden durch Werte für jedes Produkt im Auftrag ersetzt.

> [!NOTE]
> Setzen Sie den Token **Produktliste – Start** an den Anfang des HTML-Blocks, der für jedes Produkt wiederholt wird, und den Token **Produktliste – Ende** an das Ende des Blocks.

| Name des Token      | Token |
|------------------------|-------|
| Produktliste - Start   | \<!--%tablebegin.salesline% --\> |
| Produktliste - Ende     | \<!--%tableend.salesline%--\> |
| Produktname           | %lineproductname% |
| Beschreibung            | %lineproductdescription% |
| Menge               | %linequantity% |
| Preiseinheit der Position        | %lineprice% (verifizieren) |
| Positionsartikel gesamt        | %linenetamount% |
| Positionsrabatt          | %linediscount% |
| Versanddatum              | %lineshipdate% |
| Beschaffungsmethode     | %linedeliverymode% |
| Lieferadresse       | %linedeliveryaddress% |
| Verkaufseinheit der Position | %lineunit% |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Eine Dynamics 365 Commerce-Sandbox-Umgebung bereitstellen](provisioning-guide.md)

[Eine Dynamics 365 Commerce-Sandbox-Umgebung konfigurieren](cpe-post-provisioning.md)

[BOPIS in einer Dynamics 365 Commerce-Sandbox-Umgebung konfigurieren](cpe-bopis.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-Portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-Website](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
