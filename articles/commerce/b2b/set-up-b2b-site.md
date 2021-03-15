---
title: Eine B2B-E-Commerce-Website einrichten
description: In diesem Thema wird beschrieben, wie Sie eine B2B-E-Commerce-Website (Business-to-Business) in Microsoft Dynamics 365 Commerce einrichten.
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ac6f6511f4f96c00e10369329b2111a46f23d1a2
ms.sourcegitcommit: f9df202aefef761be52c0360b0e22da88773914c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035914"
---
# <a name="set-up-a-b2b-e-commerce-site"></a>Eine B2B-E-Commerce-Website einrichten

[!include [banner](../../includes/banner.md)]

Business-to-Business-E-Commerce-Websites (B2B) bieten einige wichtige Funktionen, die den Workflow für einen B2B-Benutzer optimieren. In diesem Thema wird beschrieben, wie Sie eine B2B-E-Commerce-Website in Microsoft Dynamics 365 Commerce einrichten. Es werden die Modul- und Websiteeinstellungen durchlaufen, die konfiguriert werden müssen, um B2B-spezifische Szenarien zu aktivieren.

## <a name="prerequisites"></a>Voraussetzungen

- Zum Einrichten einer B2B-E-Commerce-Website müssen Sie bestimmte Funktionen in der Commerce-Zentralverwaltung aktivieren und konfigurieren, wie in diesem Thema beschrieben.
- Kernumgebungen wie Produkterfassung, Produktdetailseiten, Warenkorb und Kaufabwicklung basieren auf denselben Modulen, die für B2C-E-Commerce-Websites (Business-to-Consumer) verwendet werden. Site-Autoren sollten mit allen Modulen, die Dynamics 365 Commerce unterstützt, vertraut sein. Weitere Informationen finden Sie unter [Informationen zur Modulbibliothek](../starter-kit-overview.md).
- In diesem Thema wird davon ausgegangen, dass Site-Autoren die Grundlagen des Commerce-Website-Generators, Vorlagen, Fragmenten und Seiten verstehen, damit sie die B2B-Funktionen für E-Commerce-Sites aktivieren können.

## <a name="site-level-settings"></a>Einstellungen auf Site-Ebene

Sie können auf die Einstellungen auf Site-Ebene im Site Builder unter **Site-Einstellungen \> Erweiterungen** zugreifen. Die folgenden zwei Einstellungen auf Site-Ebene gelten für B2B-Szenarien:

- **Debitorenkontozahlungen aktivieren** – Mithilfe dieser Eigenschaft können Benutzer Bestellungen über Debitorenkonten bezahlen. Die verfügbaren Werte sind **Für B2B-Kunden aktiviert**, **Für B2C-Kunden aktiviert**, **Für alle Kunden aktiviert** und **Für alle Kunden deaktiviert**. Wenn Ihre B2B-Website Debitorenkonten unterstützt, sollten Sie **Für B2C-Kunden aktiviert** auswählen.
- **Auftragsmengenbeschränkungen aktivieren** – Mithilfe dieser Eigenschaft können Sie die Anzahl der Artikel begrenzen, die für jedes Produkt oder jede Kategorie bestellt werden können. Die verfügbaren Werte sind **Für B2B-Kunden aktiviert**, **Für B2C-Kunden aktiviert**, **Für alle Kunden aktiviert** und **Für alle Kunden deaktiviert**.

> [!NOTE]
> Wenn Sie auf die neueste Version der Modulbibliothek aktualisieren, müssen Sie zusätzliche Schritte ausführen, um sicherzustellen, dass die zuvor beschriebenen Site-Einstellungen in Ihrer Umgebung verfügbar sind. Weitere Informationen finden Sie unter [app.settings.json-Datei aktualisieren](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="create-business-partner-sign-up-pages"></a>Registrierungsseiten für Geschäftspartner erstellen

Um ein Geschäftspartner zu werden, müssen Benutzer zuerst eine Geschäftspartneranforderung übermitteln. Auf der B2B-Startseite ist ein Link zur Anforderungsseite für Geschäftspartner verfügbar, damit Benutzer den Prozess starten können. Sobald Benutzer eine Geschäftspartneranforderung gesendet haben, erhalten sie eine Bestätigung, dass die Anforderung gesendet wurde. 

### <a name="create-a-business-partner-request-page"></a>Eine Geschäftspartneranforderungsseite erstellen

Das Modul **Partner registrieren** auf einer Geschäftspartneranforderungsseite wird zum Initiieren von Benutzeranforderungen verwendet, um Geschäftspartner zu werden. Mit diesem Modul können Sie die Benutzerinformationen erfassen, die für den Registrierungsvorgang erforderlich sind. Darüber hinaus wird das Modul **Geschäftskontoadresse** verwendet, um die Adresse des Benutzers zu erfassen.

Führen Sie die folgenden Schritte aus, um die Anforderungsseite für Geschäftspartner im Site Builder einzurichten und zu konfigurieren.

1. Erstellen Sie eine Vorlage mit dem Namen **Registrieren**. Die Vorlage sollte folgende Module enthalten:

    - Partner registrieren
    - Breadcrumb
    - Übergeordnet
    - Fußzeile
    - Inhaltsblock
    - Textblock
    - Produktsammlung

1. Verwenden Sie die Vorlage zur **Registrierung**, um eine Seite namens **Geschäftspartneranforderung** zu erstellen.
1. fügen Sie im **Kopfzeilen**-Slot das Kopfzeilenfragment hinzu, das mit der Site-Kopfzeile vorkonfiguriert ist.
1. Fügen Sie im **Fußzeilen**-Slot das Fußzeilenfragment hinzu, das mit der Site-Fußzeile vorkonfiguriert ist.
1. Fügen Sie im **Haupt**-Slot ein **Container**-Modul hinzu. Legen Sie im Eigenschaftenbereich des Moduls den Wert **Breite** auf **Container füllen** fest.
1. Fügen Sie im **Container**-Slot das **Breadcrumb**-Modul hinzu. Konfigurieren Sie im Eigenschaftenbereich des Moduls unter **Links** einen Link zur Startseite, und geben Sie **Startseite** als Linktext ein.
1. Fügen Sie im **Container**-Slot ein **Partner registrieren**-Modul unter dem **Breadcrumb**-Modul hinzu. Geben Sie im Eigenschaftenbereich des Moduls unter **Überschrift** **Geschäftspartner werden** ein.
1. Fügen Sie im **Partner registrieren**-Slot ein **Geschäftskontoadresse**-Modul hinzu.
1. Fügen Sie im **Container**-Slot ein **Textblock**-Modul unter dem **Partner registrieren**-Modul hinzu. Hier können Sie einige Bedingungen für den Registrierungsvorgang definieren.
1. Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.
1. Veröffentlichen Sie die URL der Seite.

### <a name="create-a-business-partner-request-confirmation-page"></a>Eine Bestätigungsseite für Geschäftspartneranforderungen erstellen

Nach dem Absenden einer Geschäftspartneranforderung sollte dem Benutzer eine Bestätigungsseite angezeigt werden, um die Übermittlung zu bestätigen. 

Führen Sie die folgenden Schritte aus, um die Anforderungsbestätigungsseite im Site Builder einzurichten und zu konfigurieren.

1. Verwenden Sie die zuvor erstellte Vorlage zur **Registrierung**, um eine Seite namens **Bestätigung von Partneranforderungen** zu erstellen.
1. fügen Sie im **Kopfzeilen**-Slot das Kopfzeilenfragment hinzu, das mit der Site-Kopfzeile vorkonfiguriert ist.
1. Fügen Sie im **Fußzeilen**-Slot das Fußzeilenfragment hinzu, das mit der Site-Fußzeile vorkonfiguriert ist.
1. Fügen Sie im **Haupt**-Slot ein **Container**-Modul hinzu. Legen Sie im Eigenschaftenbereich des Moduls den Wert **Breite** auf **Container füllen** fest.
1. Fügen Sie im **Container**-Slot ein **Inhaltsblock**-Modul hinzu. Geben Sie im Eigenschaftenbereich des Moduls unter **Überschrift** **Anforderung übermittelt** ein. Geben Sie im **Rich Text**-Feld **Ihre Anforderung wurde gesendet** ein. Konfigurieren Sie unter **Links** einen Link zur Startseite, und geben Sie **Zurück zum Einkaufen** als Linktext ein.
1. Fügen Sie ein weiteres **Container**-Modul hinzu, dem Sie wiederum ein **Produktsammel**-Modul hinzufügen.
1. Konfigurieren Sie das **Produktsammel**-Modul mit der Empfehlungs- oder Kategorieliste, die Sie auf der Seite präsentieren möchten.
1. Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.
1. Veröffentlichen Sie die URL der Seite.

Führen Sie die folgenden Schritte aus, um der Anforderungsbestätigungsseite im Site Builder einen Link hinzuzufügen.

1. Rufen Sie die Seite **Geschäftspartneranforderung** auf, die Sie zuvor erstellt haben, und wählen Sie **Bearbeiten** aus. 
1. Wählen Sie den **Partner registrieren**-Modul-Slot aus. Konfigurieren Sie im Eigenschaftenbereich unter **Link zur Registrierungsbestätigungsseite** den Link zur Geschäftspartneranforderungsseite, die Sie zuvor erstellt haben. 
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.

### <a name="add-a-business-partner-request-link-to-the-home-page"></a>Der Startseite einen Link für Geschäftspartneranforderungen hinzufügen

Sobald die Registrierungs- und Bestätigungsseiten für Geschäftspartneranforderungen erstellt wurden, müssen Sie die Registrierungsseite über einen Link auf der Startseite zugänglich machen. Sie können diese Aufgabe ausführen, indem Sie den Link einem beliebigen **Inhaltsblock**-Modul auf der Startseite hinzufügen.

Führen Sie die folgenden Schritte aus, um der Startseite im Site Builder einen Link für Geschäftspartneranforderungen hinzuzufügen.

1. Rufen Sie die Startseite Ihrer Website auf, und wählen Sie **Bearbeiten** aus.
1. Wählen Sie einen **Inhaltsblock**-Modul-Slot aus. Konfigurieren Sie im Eigenschaftenbereich des Moduls unter **Links** einen Link zu der zuvor erstellten Anforderungsseite für Geschäftspartner, und geben Sie **Als Geschäftspartner registrieren** oder einen ähnlichen Text wie den Linktext ein. Fügen Sie gegebenenfalls ein Bild hinzu.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.

## <a name="account-management-landing-page"></a>Kontenverwaltungsseite-Landingpage

Die Zielseite für die Kontoverwaltung enthält alle Kontoverwaltungsinformationen, die sowohl für B2B- als auch für B2C-E-Commerce-Websites erforderlich sind. Nur angemeldete Benutzer können sich diese Seite anzeigen lassen.

Führen Sie die folgenden Schritte aus, um eine Zielseite für die B2B-Kontoverwaltung im Site Builder zu erstellen und zu konfigurieren.

1. Erstellen Sie eine Vorlage mit dem Namen **Kontoverwaltung**. Die Vorlage sollte folgende Module enthalten:

    - Übergeordnet
    - Fußzeile
    - Breadcrumb
    - Willkommenskachel für Konto
    - Generisches Kontokachel
    - Adresskachel für Konto
    - Kontowunschlistenkachel
    - Kachel für Kontoadresse
    - Kontotreuekachel
    - Debitorensaldo-Kachel für Konto
    - Kachel für Kontoauftragsvorlagen
    - Organisationsbenutzer
    - Unternehmensorganisationsliste
    - Debitorenkontosaldo
    - Auftragsvorlagenpositionen
    - Auftragsvorlagenliste
    - Rechnungskachel für Konto
    - Rechnungsliste
    - Rechnungsdetails

1. Verwenden Sie die Vorlage **Kontoverwaltung** zum Erstellen einer Seite namens **Mein Konto**.
1. fügen Sie im **Kopfzeilen**-Slot das Kopfzeilenfragment hinzu, das mit der Site-Kopfzeile vorkonfiguriert ist.
1. Fügen Sie im **Fußzeilen**-Slot das Fußzeilenfragment hinzu, das mit der Site-Fußzeile vorkonfiguriert ist.
1. Fügen Sie im **Haupt**-Slot ein **Container**-Modul hinzu. Legen Sie im Eigenschaftenbereich des Moduls den Wert **Breite** auf **Container füllen** fest. 
1. Fügen Sie im **Container**-Slot das **Breadcrumb**-Modul hinzu. Konfigurieren Sie im Eigenschaftenbereich des Moduls unter **Links** einen Link zur Startseite, und geben Sie **Startseite** als Linktext ein.
1. Fügen Sie im **Container**-Slot ein **Begrüßungskachel**-Modul hinzu. Geben Sie im Eigenschaftenbereich des Moduls unter **Überschrift** **Willkommen** ein.
1. Fügen Sie im **Haupt**- Slot ein weiteres **Container**-Modul (**Container 2**) hinzu. Legen Sie im Eigenschaftenbereich des Moduls den Wert **Breite** auf **Container füllen** fest. Legen Sie den Wert **Angezeigte untergeordnete Elemente** auf **Zwei** fest. 
1. Fügen Sie im **Container 2**-Slot ein **Generische Kachel für Konto**-Modul hinzu. Geben Sie im Eigenschaftenbereich des Moduls unter **Überschrift** **Mein Profil** ein. Konfigurieren Sie unter **Links** einen Link zur Seite **Mein Profil**. 
1. Fügen Sie im **Container 2**-Slot ein weiteres **Generische Kachel für Konto**-Modul hinzu. Geben Sie im Eigenschaftenbereich des Moduls unter **Überschrift** **Bestellverlauf** ein. Konfigurieren Sie unter **Links** einen Link zur Bestellverlaufsseite.
1. Fügen Sie im **Haupt**- Slot ein weiteres **Container**-Modul (**Container 3**) hinzu. Legen Sie im Eigenschaftenbereich des Moduls den Wert **Breite** auf **Container füllen** fest. Legen Sie den Wert **Angezeigte untergeordnete Elemente** auf **Zwei** fest. 
1. Fügen Sie im **Container 3**-Slot ein **Adresskachel für Konto**-Modul hinzu. Geben Sie im Eigenschaftenbereich des Moduls unter **Überschrift** **Meine Adresse** ein. Konfigurieren Sie unter **Links** einen Link zur Seite **Meine Adresse**. 
1. Fügen Sie im **Container 3**-Slot ein **Kontowunschlistenkachel**-Modul hinzu. Geben Sie im Eigenschaftenbereich des Moduls unter **Überschrift** **Meine Wunschliste** ein. Konfigurieren Sie unter **Links** einen Link zur Seite **Meine Wunschliste**.
1. Fügen Sie im **Haupt**- Slot ein weiteres **Container**-Modul (**Container 4**) hinzu. Legen Sie im Eigenschaftenbereich des Moduls den Wert **Breite** auf **Container füllen** fest. Legen Sie den Wert **Angezeigte untergeordnete Elemente** auf **Zwei** fest. 
1. Fügen Sie im **Container 4**-Slot ein **Organisationsbenutzer**-Modul hinzu. Geben Sie im Eigenschaftenbereich des Moduls unter **Überschrift** **Organisationsbenutzer** ein. 
1. Fügen Sie im **Container 4**-Slot ein **Debitorensaldo-Kachel für Konto**-Modul hinzu. Geben Sie im Eigenschaftenbereich des Moduls unter **Überschrift** **Habenkonto** ein. 
1. Fügen Sie im **Haupt**- Slot ein weiteres **Container**-Modul (**Container 5**) hinzu. Legen Sie im Eigenschaftenbereich des Moduls den Wert **Breite** auf **Container füllen** fest. Legen Sie den Wert **Angezeigte untergeordnete Elemente** auf **Zwei** fest. 
1. Fügen Sie im **Container 5**-Slot ein **Auftragsvorlagenkachel für Konto**-Modul hinzu. Geben Sie im Eigenschaftenbereich des Moduls unter **Überschrift** **Auftragsvorlagen** ein. 
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.

> [!NOTE] 
> Einige der Abschnitte, die Sie in den Schritten 13 bis 18 hinzugefügt haben, werden nicht auf der „What you see is what you get“-Canvas (WYSIWYG) angezeigt, da dafür ein angemeldetes B2B-Konto erforderlich ist.

## <a name="create-and-configure-customer-balance-pages-and-modules"></a>Seiten und Module für Debitorensalden erstellen und konfigurieren 

Debitorenkonten können zur Bezahlung von Aufträgen verwendet werden. Das verfügbare Saldo auf einem Kundenkonto kann über die Kontoverwaltungsseite eines Benutzers angezeigt werden.

### <a name="create-a-customer-balance-page"></a>Eine Debitorensaldoseite erstellen 

Bevor sich angemeldete B2B-Benutzer ihr Debitorensaldo anzeigen lassen können, müssen Sie eine Debitorensaldoseite erstellen. 

Führen Sie die folgenden Schritte aus, um eine Debitorensaldoseite im Site Builder zu erstellen.

1. Verwenden Sie die zuvor erstellte Vorlage zur **Kontoverwaltung**, um eine Seite namens **Debitorensaldo** zu erstellen.
1. fügen Sie im **Kopfzeilen**-Slot das Kopfzeilenfragment hinzu, das mit der Site-Kopfzeile vorkonfiguriert ist.
1. Fügen Sie im **Fußzeilen**-Slot das Fußzeilenfragment hinzu, das mit der Site-Fußzeile vorkonfiguriert ist.
1. Fügen Sie im **Haupt**- Slot ein weiteres **Container**-Modul (**Container 3**) hinzu. Legen Sie im Eigenschaftenbereich des Moduls den Wert **Breite** auf **Container füllen** fest. Legen Sie den Wert **Angezeigte untergeordnete Elemente** auf **Zwei** fest.
1. Fügen Sie im **Container**-Slot das **Breadcrumb**-Modul hinzu. Konfigurieren Sie im Eigenschaftenbereich des Moduls unter **Links** einen Link zur Startseite der Kontoverwaltung, und geben Sie **Mein Konto** als Linktext ein.
1. Fügen Sie im **Container**-Slot ein **Debitorkontosaldo**-Modul hinzu. Geben Sie im Eigenschaftenbereich des Moduls unter **Überschrift** **Kontosaldo** ein.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.
1. Veröffentlichen Sie die URL der Seite.
1. Gehen Sie zur Zielseite der Kontoverwaltung (**Mein Konto**), die Sie zuvor erstellt haben.
1. Fügen Sie im Eigenschaftenbereich des **Debitorensaldo-Kachel für Konto**-Moduls einen Link zur Debitorensaldoseite hinzu. 
1. Speichern und veröffentlichen Sie die Seite.

Die Debitorensaldoseite wurde jetzt erstellt, und Benutzer können über die Zielseite der Kontoverwaltung darauf zugreifen.

### <a name="configure-a-checkout-page-so-that-the-customer-balance-can-be-used-as-a-form-of-payment"></a>Eine Checkout-Seite konfigurieren, damit der Debitorensaldo als Zahlungsmethode verwendet werden kann

Das Modul **Debitorenkontozahlung** ist erforderlich, damit der Debitorensaldo als Zahlungsmethode verwendet werden kann. Dieses Modul sollte der Checkout-Seite als Zahlungsmethode hinzugefügt werden. Informationen zum Konfigurieren einer Checkout-Seite und zu den für den Auftragsabschluss erforderlichen Modulen, einschließlich aller Zahlungsdetails, finden Sie unter [Checkout-Modul](../add-checkout-module.md).

Sobald Sie eine Checkout-Seite konfiguriert haben, müssen Sie dem Zahlungsbereich das Modul **Debitorenkontozahlung** hinzufügen. Speichern und veröffentlichen Sie anschließend die Seite. B2B-Benutzer können sich dann auf der E-Commerce-Website anmelden und ihren verfügbaren Debitorensaldo auf Aufträge während der Kaufabwicklung anwenden.

Darüber hinaus müssen Sie unter **Site Builder \> Erweiterungen** sicherstellen, dass die Eigenschaft **Debitorenkontozahlungen aktivieren** auf **Für B2B-Kunden aktiviert** festgelegt ist.

## <a name="create-order-template-pages"></a>Auftragsvorlagenseiten erstellen

Für eine B2B-E-Commerce-Website können zwei Auftragsvorlagenseiten eingerichtet werden: eine Auftragsvorlagenlistenseite und eine Auftragsvorlagenpositionenseite.

Auf einer Auftragsvorlagenlistenseite wird eine Liste aller verfügbaren Auftragsvorlagen angezeigt. Sie wird mithilfe des Moduls **Auftragsvorlagenliste** eingerichtet. Mithilfe der Auftragsvorlagenlistenseite können Sie eine Vorlage erstellen oder löschen und die Artikel einer Vorlage in den Warenkorb legen.

Auf einer Auftragsvorlagenpositionenseite werden die Details der Auftragsvorlage angezeigt, die auf einer Auftragsvorlagenlistenseite ausgewählt wurde. Sie wird mithilfe des Moduls **Auftragsvorlagenpositionen** eingerichtet. Wenn ein Benutzer den Namen einer Vorlage auf einer Auftragsvorlagenlistenseite auswählt, öffnet sich die Auftragsvorlagenpositionenseite und zeigt die Details der Vorlage an. Der Benutzer kann sich dann die Artikel in der Vorlage anzeigen lassen und sie bearbeiten.

### <a name="create-an-order-templates-list-page"></a>Eine Auftragsvorlagenlistenseite erstellen

Führen Sie die folgenden Schritte aus, um eine Auftragsvorlagenlistenseite im Site Builder zu erstellen.

1. Verwenden Sie die zuvor erstellte Vorlage zur **Kontoverwaltung**, um eine Seite namens **Auftragsvorlagen** zu erstellen.
1. fügen Sie im **Kopfzeilen**-Slot das Kopfzeilenfragment hinzu, das mit der Site-Kopfzeile vorkonfiguriert ist.
1. Fügen Sie im **Fußzeilen**-Slot das Fußzeilenfragment hinzu, das mit der Site-Fußzeile vorkonfiguriert ist.
1. Fügen Sie im **Haupt**-Slot ein **Container**-Modul hinzu. Legen Sie im Eigenschaftenbereich des Moduls den Wert **Breite** auf **Container füllen** fest.
1. Fügen Sie im **Container**-Slot das **Breadcrumb**-Modul hinzu. Konfigurieren Sie im Eigenschaftenbereich des Moduls unter **Links** einen Link zur Startseite der Kontoverwaltung, und geben Sie **Mein Konto** als Linktext ein.
1. Fügen Sie im **Container**-Slot ein **Auftragsvorlagenlisten**-Modul hinzu.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.
1. Veröffentlichen Sie die URL der Seite.
1. Gehen Sie zur Zielseite der Kontoverwaltung (**Mein Konto**), die Sie zuvor erstellt haben.
1. Konfigurieren Sie im Eigenschaftenbereich für das Modul **Auftragsvorlagenkachel für Konto**, unter **Links**, einen Link zu der soeben erstellten Auftragsvorlagenlistenseite.
1. Speichern und veröffentlichen Sie die Seite.

Die Auftragsvorlagenseite wurde jetzt erstellt, und Benutzer können über die Zielseite der Kontoverwaltung darauf zugreifen.

### <a name="create-an-order-template-lines-page"></a>Eine Auftragsvorlagenpositionenseite erstellen

Führen Sie die folgenden Schritte aus, um eine Auftragsvorlagenpositionenseite im Site Builder zu erstellen.

1. Verwenden Sie die zuvor erstellte Vorlage zur **Kontoverwaltung**, um eine Seite namens **Auftragsvorlagenpositionen** zu erstellen.
1. fügen Sie im **Kopfzeilen**-Slot das Kopfzeilenfragment hinzu, das mit der Site-Kopfzeile vorkonfiguriert ist.
1. Fügen Sie im **Fußzeilen**-Slot das Fußzeilenfragment hinzu, das mit der Site-Fußzeile vorkonfiguriert ist.
1. Fügen Sie im **Haupt**-Slot ein **Container**-Modul hinzu. Legen Sie im Eigenschaftenbereich des Moduls den Wert **Breite** auf **Container füllen** fest.
1. Fügen Sie im **Container**-Slot das **Breadcrumb**-Modul hinzu. Konfigurieren Sie im Eigenschaftenbereich des Moduls unter **Links** einen Link zur Startseite der Kontoverwaltung, und geben Sie **Mein Konto** als Linktext ein.
1. Fügen Sie im **Container**-Slot ein **Auftragsvorlagenpositionen**-Modul hinzu.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.
1. Veröffentlichen Sie die URL der Seite.

## <a name="onboard-business-partner-users"></a>Geschäftspartnerbenutzer aufnehmen

Auf der Benutzerseite der Organisation kann der Administrator einer Geschäftspartnerorganisation zusätzliche Benutzer aus dieser Organisation in die B2B-E-Commerce-Website integrieren. Sie wird mithilfe des Moduls **Unternehmensorganisationsliste** eingerichtet. Auf der Benutzerseite der Organisation kann ein Administrator Benutzer hinzufügen oder entfernen, Kontensalden definieren und Aufstellungen für einen Benutzer anfordern.

Führen Sie die folgenden Schritte aus, um eine Benutzerseite der Organisation im Site Builder zu erstellen.

1. Verwenden Sie die zuvor erstellte Vorlage zur **Kontoverwaltung**, um eine Seite namens **Organisationsbenutzer** zu erstellen.
1. fügen Sie im **Kopfzeilen**-Slot das Kopfzeilenfragment hinzu, das mit der Site-Kopfzeile vorkonfiguriert ist.
1. Fügen Sie im **Fußzeilen**-Slot das Fußzeilenfragment hinzu, das mit der Site-Fußzeile vorkonfiguriert ist.
1. Fügen Sie im **Haupt**-Slot ein **Container**-Modul hinzu. Legen Sie im Eigenschaftenbereich des Moduls den Wert **Breite** auf **Container füllen** fest.
1. Fügen Sie im **Container**-Slot das **Breadcrumb**-Modul hinzu. Konfigurieren Sie im Eigenschaftenbereich des Moduls unter **Links** einen Link zur Startseite der Kontoverwaltung, und geben Sie **Mein Konto** als Linktext ein.
1. Fügen Sie im **Container**-Slot ein **Unternehmensorganisationslisten**-Modul hinzu. Geben Sie im Eigenschaftenbereich des Moduls unter **Überschrift** **Organisationsbenutzer** ein.
1. Aktivieren Sie im Eigenschaftenbereich des **Unternehmensorganisationslisten**-Moduls die Eigenschaften **Tabellensortierung** und **Tabellenpaginierung**. Legen Sie die Paginierungszahl auf **5** fest.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.
1. Veröffentlichen Sie die URL der Seite.
1. Gehen Sie zur Zielseite der Kontoverwaltung (**Mein Konto**), die Sie zuvor erstellt haben.
1. Konfigurieren Sie im Eigenschaftenbereich des Moduls **Organisationsbenutzerkachel**, unter **Links**, einen Link zu der soeben erstellten Benutzerseite der Organisation. 
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.

## <a name="create-invoice-pages"></a>Rechnungsseiten erstellen

Eine Rechnungslistenseite zeigt eine Liste aller verfügbaren Rechnungen an. Sie wird mithilfe des Moduls **Rechnungsliste** eingerichtet. Auf der Rechnungslistenseite können Benutzer Rechnungen bezahlen oder anfordern. 

Auf einer Seite mit Rechnungsdetails werden die Details der Rechnung angezeigt, die auf einer Rechnungslistenseite ausgewählt wurden. Sie wird mithilfe des Moduls **Rechnungsdetails** eingerichtet. Wenn ein Benutzer eine Rechnungs-ID auf einer Rechnungslistenseite auswählt, öffnet sich die Rechnungsdetailseite und zeigt die Details der Rechnung an.

### <a name="create-an-invoices-list-page"></a>Eine Rechnungslistenseite erstellen

Führen Sie die folgenden Schritte aus, um eine Rechnungslistenseite im Site Builder zu erstellen.

1. Verwenden Sie die zuvor erstellte Vorlage zur **Kontoverwaltung**, um eine Seite namens **Rechnungsliste** zu erstellen.
1. fügen Sie im **Kopfzeilen**-Slot das Kopfzeilenfragment hinzu, das mit der Site-Kopfzeile vorkonfiguriert ist.
1. Fügen Sie im **Fußzeilen**-Slot das Fußzeilenfragment hinzu, das mit der Site-Fußzeile vorkonfiguriert ist.
1. Fügen Sie im **Haupt**-Slot ein **Container**-Modul hinzu. Legen Sie im Eigenschaftenbereich des Moduls den Wert **Breite** auf **Container füllen** fest.
1. Fügen Sie im **Container**-Slot das **Breadcrumb**-Modul hinzu. Konfigurieren Sie im Eigenschaftenbereich des Moduls unter **Links** einen Link zur Startseite der Kontoverwaltung, und geben Sie **Mein Konto** als Linktext ein.
1. Fügen Sie im **Container**-Slot ein **Rechnungslisten**-Modul hinzu. Geben Sie im Eigenschaftenbereich des Moduls unter **Überschrift** **Rechnungen** ein.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.
1. Veröffentlichen Sie die URL der Seite.
1. Gehen Sie zur Zielseite der Kontoverwaltung (**Mein Konto**), die Sie zuvor erstellt haben.
1. Konfigurieren Sie im Eigenschaftenbereich des Moduls **Rechnungskachel für Konto**, unter **Links**, einen Link zu der soeben erstellten Rechnungslistenseite. 
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.

### <a name="create-an-invoice-details-page"></a>Eine Rechnungsdetailseite erstellen

Führen Sie die folgenden Schritte aus, um eine Rechnungsdetailseite im Site Builder zu erstellen.

1. Verwenden Sie die zuvor erstellte Vorlage zur **Kontoverwaltung**, um eine Seite namens **Rechnungsdetails** zu erstellen.
1. fügen Sie im **Kopfzeilen**-Slot das Kopfzeilenfragment hinzu, das mit der Site-Kopfzeile vorkonfiguriert ist.
1. Fügen Sie im **Fußzeilen**-Slot das Fußzeilenfragment hinzu, das mit der Site-Fußzeile vorkonfiguriert ist.
1. Fügen Sie im **Haupt**-Slot ein **Container**-Modul hinzu. Legen Sie im Eigenschaftenbereich des Moduls den Wert **Breite** auf **Container füllen** fest.
1. Fügen Sie im **Container**-Slot das **Breadcrumb**-Modul hinzu. Konfigurieren Sie im Eigenschaftenbereich des Moduls unter **Links** einen Link zur Startseite der Kontoverwaltung, und geben Sie **Mein Konto** als Linktext ein. Konfigurieren Sie dann einen Link zur Rechnungslistenseite, und geben Sie **Rechnungslisten** als Linktext ein.
1. Fügen Sie im **Container**-Slot ein **Rechnungsdetails**-Modul hinzu.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.
1. Veröffentlichen Sie die URL der Seite.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Informationen zur Modulbibliothek](../starter-kit-overview.md)

[Übersicht über die Seite zur Dokumenterstellung](../authoring-home-overview.md)

[Übersicht über Vorlagen und Layouts](../templates-layouts-overview.md)

[Arbeiten mit Fragmenten](../work-with-fragments.md)

[Neue Seite hinzufügen](../add-new-page.md)

[Auschecken-Modul](../add-checkout-module.md)

[Inhaltsblockmodul](../add-hero-module.md)

[Produktsammlung](../product-collection-module-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]