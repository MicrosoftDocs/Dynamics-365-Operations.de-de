---
title: Angepasste Seiten für die Benutzeranmeldung einrichten
description: In diesem Thema wird beschrieben, wie Sie benutzerdefinierte Seiten in Microsoft Dynamics 365 Commerce erstellen, die benutzerdefinierte Anmeldungen für Benutzer von Business-to-Consumer (B2C)-Mandanten von Azure Active Directory (Azure AD) verarbeiten.
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 214f99563f8bb08d8c051f904d0ca0a88267aa6b
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349649"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a>Angepasste Seiten für die Benutzeranmeldung einrichten

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie benutzerdefinierte Seiten in Microsoft Dynamics 365 Commerce erstellen, die benutzerdefinierte Anmeldungen für Benutzer von Business-to-Consumer (B2C)-Mandanten von Azure Active Directory (Azure AD) verarbeiten.

Um benutzerdefinierte Seiten zu verwenden, die in Dynamics 365 Commerce erstellt werden können, um Benutzeranmeldungsflüsse zu verarbeiten, müssen Sie die Azure AD Richtlinien festlegen, auf die in der Geschäftsumgebung verwiesen wird. Sie können die Azure AD B2C Richtlinien „An- und Abmeldung“, „Profilverwaltung“ und „Kennwortzurücksetzung“ mithilfe der Azure AD B2C Anwendung konfigurieren. Die Azure AD B2C Mandanten- und Richtliniennamen können dann während des Bereitstellungsprozesses referenziert werden, der für die Handelsumgebung mithilfe von Microsoft Dynamics Lifecycle Services (LCS) ausgeführt wird.

Die benutzerdefinierten Handelsseiten können erstellt werden, indem Anmeldung, Abmeldung, Kontoprofile bearbeiten, Kennwortrücksetzung oder generische ADD-Module verwendet werden. Die Seite URLs, die für die benutzerdefinierten Seiten veröffentlicht werden, sollten dann in Azure AD B2C Richtlinienkonfigurationen im Azureportal referenziert werden.

> [!WARNING] 
> Azure AD B2C stellt alte (veraltete) Benutzerströme bis zum 1. August 2021 ein. Daher sollten Sie planen, Ihre Benutzerflows auf die neue empfohlene Version zu migrieren. Die neue Version bietet Featureparität und neue Funktionen. Weitere Informationen finden Sie unter [Benutzerflows in Azure Active Directory B2C](/azure/active-directory-b2c/user-flow-overview).

>Die Modulbibliothek für die Commerce-Version 10.0.15 oder höher sollte mit den empfohlenen B2C-Benutzerflows verwendet werden. Die Standardbenutzerrichtlinienseiten, die in Azure AD B2C angeboten werden, können ebenfalls verwendet werden und ermöglichen zusätzliche Änderungen des Hintergrundbilds, des Logos und der Hintergrundfarbe im Zusammenhang mit dem Branding des Unternehmens. Obwohl ihre Entwurfsfunktionen eingeschränkter sind, bieten die Standardbenutzerrichtlinienseiten Azure AD B2C-Richtlinienfunktionalität ohne Erstellen und Konfigurieren dedizierter benutzerdefinierter Seiten. 

## <a name="set-up-b2c-policies"></a>B2C Richtlinien einrichten

Nachdem Sie den Mandanten Azure AD B2C eingerichtet haben und diesen der Handelsumgebung zugeordnet haen, wechseln Sie zu **Azure AD B2C** im Azure Portal und anschließend wählen Sie **Richtlinien**, **Benutzerfluss (Richtlinien)**.

![Benutzerfluss (Richtlinien) Befehl im Menü.](./media/B2C_CustomPage_PoliciesMenu.png)

Sie können jetzt Registrieren und Anmelden, Profilbearbeitung und Kennwortrücksetzung im Fluss konfigurieren.

### <a name="configure-the-sign-up-and-sign-in-policy"></a>Konfigurieren von Registrieren und Anmelden in der Richtlinie

Um die Richtlinie Registrieren und Anmelden zu konfigurieren führen Sie die folgenden Schritte aus.

1. Wählen Sie **Neuer Benutzerflow**, **Registrierungen und Anmelden**, dann die Registerkarte **Empfohlen** und schließlich **Erstellen**.
1. Geben Sie einen Namen für die Richtlinie ein (z.B. **B2C\_1\_SignInSignUp**).
1. Im Abschnitt **Identitätsanbieter** wählen Sie den Identitätsanbieter aus, den Sie für die Richtlinie verwenden möchten. Es muss mindestens **E-Mail-Registrierung** ausgewählt werden.
1. In der Spalte **Attribut sammeln** aktivieren Sie die Kontrollkästchen für **E-Mail-Adresse**, **Vorname** und **Nachname** aus.
1. In der Spalte **Rücknahme anfordern** aktivieren Sie die Kontrollkästchen für **E-Mail-Adressen**, **Vorname**, **Identitätsanbieter**, **Nachname** und **Objekt-ID des Benutzers**.

    ![Attribute und Ansprüche ausgewählt.](./media/B2C_SignInSignUp_Attributes.png)

1. **OK** wählen, um die Richtlinie zu erstellen.
1. Doppelklicken Sie auf den neuen Richtliniennamen, und wählen dann im Navigationsbereich **Eigenschaften**.
1. Legen Sie **Aktivieren Sie JavaScript erzwingt Seitenlayout (Vorschau)** auf **Aktiviert** fest.

    ![Eigenschaftenseite für die neue Richtlinie.](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> Der Richtlinienname verweist ganz auf die Handelsumgebung. (Das Präfix **B2C\_1\_** ist in der Referenz enthalten.) Richtlinien können nicht umbenannt werden, nachdem sie erstellt wurden. Wenn Sie eine vorhandene Richtlinie für die Handelsumgebung ersetzen, können Sie die ursprüngliche Richtlinie löschen und eine neue Richtlinie erstellen, die denselben Namen hat. Falls die Umgebung bereits bereitgestellt wurde, können Sie den neuen Richtliniennamen durch eine Serviceanforderung senden.

Sie kehren zu dieser Richtlinie zurück, um die Einrichtung zu beenden, nachdem Sie die benutzerdefinierten Seiten erstellt haben. Jetzt schließen Sie die Richtlinie, um zur Seite **Benutzerfluss (Richtlinien)** im Azure-Portal zurückzukehren.

### <a name="configure-the-profile-editing-policy"></a>Konfigurieren Sie die Profilbearbeitungsrichtlinie

Um die Profilbearbeitungsrichtlinie zu konfigurieren, folgen Sie diesen Schritten.

1. Wählen Sie **Neuer Benutzerflow**, **Profilbearbeitung**, dann die Registerkarte **Empfohlen** und schließlich **Erstellen**.
1. Geben Sie einen Namen für die Richtlinie ein (z.B. **B2C\_1\_EditProfile**).
1. Im Abschnitt **Identitätsanbieter** wählen Sie den Identitätsanbieter aus, den Sie für die Richtlinie verwenden möchten. Es muss mindestens **Lokale Kontoen-Anmeldung** ausgewählt werden.
1. In der Spalte **Attribut sammeln** aktivieren Sie die Kontrollkästchen für **Vorname** und **Nachname** aus.
1. In der Spalte **Rücknahme anfordern** aktivieren Sie die Kontrollkästchen für **E-Mail-Adressen**, **Vorname**, **Identitätsanbieter**, **Nachname** und **Objekt-ID des Benutzers**.
1. **OK** wählen, um die Richtlinie zu erstellen.
1. Doppelklicken Sie auf den neuen Richtliniennamen, und wählen dann im Navigationsbereich **Eigenschaften**.
1. Legen Sie **Aktivieren Sie JavaScript erzwingt Seitenlayout (Vorschau)** auf **Aktiviert** fest.

Sie kehren zu dieser Richtlinie zurück, um die Einrichtung zu beenden, nachdem Sie die benutzerdefinierten Seiten erstellt haben. Jetzt schließen Sie die Richtlinie, um zur Seite **Benutzerfluss (Richtlinien)** im Azure-Portal zurückzukehren.

### <a name="configure-the-password-reset-policy"></a>Konfigurieren Sie die Kennwortrücksetzungs „Richtlinie“

Um die Kennwortzurücksetzungsrichtlinie zu konfigurieren, folgen Sie diesen Schritten.

1. Wählen Sie **Neuer Benutzerflow**, dann die Option **Kennwortzurücksetzung**, die Registerkarte **Empfohlen** und schließlich **Erstellen**.
1. Geben Sie einen Namen für die Richtlinie ein (z.B. **B2C\_1\_ForgetPassword**).
1. Im Abschnitt **Identitätsanbieter** wählen Sie **Rücksetzungskennwort mithilfe der E-Mail-Adresse** aus.
1. In der Spalte **Anforderung zurückgeben** aktivieren Sie die Kontrollkästchen für **E-Mail-Adressen**, **Vorname**, **Nachname** und **Objekt-ID des Benutzers**.
1. **OK** wählen, um die Richtlinie zu erstellen.
1. Doppelklicken Sie auf den neuen Richtliniennamen, und wählen dann im Navigationsbereich **Eigenschaften**.
1. Legen Sie **Aktivieren Sie JavaScript erzwingt Seitenlayout (Vorschau)** auf **Aktiviert** fest.

Sie kehren zu dieser Richtlinie zurück, um die Einrichtung zu beenden, nachdem Sie die benutzerdefinierten Seiten erstellt haben. Jetzt schließen Sie die Richtlinie, um zur Seite **Benutzerfluss (Richtlinien)** im Azure-Portal zurückzukehren.

## <a name="build-the-custom-pages"></a>Benutzerdefinierte Seiten erstellen

In Commerce sind eigene Azure AD-Module enthalten, mit denen benutzerdefinierte Seiten für Azure AD B2C-Benutzerrichtlinien erstellt werden können. Mit der Hauptseite können Seiten speziell für das Layout jeder Benutzerrichtlinienseite mit den unten beschriebenen Azure AD B2C-Modulen erstellt werden. Alternativ kann das **generische AAD**-Modul für alle Seitenlayouts und Richtlinien in Azure AD B2C verwendet werden (auch für Seitenlayoutoptionen innerhalb von Richtlinien, die unten nicht aufgeführt sind). 

- Seitenspezifisch Azure AD-Module sind an Dateneingabeelemente gebunden, die von Azure AD B2C gerendert werden. Mit diesen Modulen haben Sie mehr Kontrolle über die Positionierung der Elemente auf Ihren Seiten. Möglicherweise müssen jedoch mehr Seiten und Modulerweiterungen erstellt werden, um Abweichungen zu berücksichtigen, die über die unten beschriebenen Standardeinstellungen hinausgehen.
- Das **generische AAD**-Modul erstellt das „div“-Element für Azure AD B2C zum Rendern aller Elemente im Seitenlayout der Benutzerrichtlinie, wodurch die B2C-Funktionen der Seite flexibler werden, die Positionierung und das Styling jedoch weniger kontrolliert werden (CSS kann jedoch verwendet werden, um das Erscheinungsbild Ihrer Website anzupassen).

Sie können eine einzelne Seite mit dem **generischen AAD**-Modul erstellen und es für alle Ihre Benutzerrichtlinienseiten verwenden. Oder Sie können bestimmte Seiten mit den Azure AD-Modulen für Anmeldung, Registrierung, Profilbearbeitung, Kennwortzurücksetzung und Überprüfung der Kennwortzurücksetzung erstellen. Sie können auch eine Mischung aus beiden verwenden, wobei Sie die spezifischen Azure AD-Seiten für die unten angegebenen Seitenlayouts und die generische AAD-Modulseite für die verbleibenden Seitenlayouts auf diesen oder anderen Benutzerrichtlinienseiten verwenden.

Mehr über die Azure AD-Module zu erfahren, die mit der Modulbibliothek geliefert werden, erfahren Sie unter [Seiten und Module zur Identitätsverwaltung](identity-mgmt-modules.md).

Um benutzerdefinierte Seiten mit spezifischen Identitätsmodulen zu erstellen, um Benutzer-Registrierungen zu behandeln, folgen Sie diesen Schritten.

1. Navigieren Sie im Commerce Site Builder zu Ihrer Site.
1. Erstellen Sie die folgenden fünf Vorlagen und Seiten (falls nicht bereits auf Ihrer Website vorhanden):
    - Eine **Anmelden**-Vorlage und eine Seite die das Anmeldenmodul verwendet.
    - Eine **Abmelden**-Vorlage und eine Seite die das Abmeldungsmodul verwendet.
    - Eine Vorlage **Kennwort zurücksetzen** und Seite, die das Kennwortrücksetzungsmodul verwenden.
    - Eine Vorlage **Kennwort zurücksetzen prüfen** und Seite, die das Kennwortrücksetzungsmodul überprüft.
    - Eine Vorlage **Profil bearbeiten** und Seite, die das Kundenprofil verwenden Modul bearbeiten.

Wenn Sie die Seiten erstellen, folgen Sie diesen Richtlinien:

- Für jede Seite oder Modul verwenden Sie das Layout und den Stil, die am besten Ihren Geschäftsanforderungen entsprechen.
- Veröffentlichen Sie alle Seiten und URLs, die in der Azure AD B2C Einstellung verwendet werden müssen.
- Nachdem die Seiten und URLs veröffentlicht wurden, sammeln Sie die URLs, die für die Azure AD B2C Richtlinienkonfiguration verwendet werden müssen. Ein **?preloadscripts=true** Suffix wird jeder URL hinzugefügt, wenn sie verwendet wird.

> [!IMPORTANT]
> Seiten, auf die in Azure AD B2C verwiesen werden soll, werden direkt von der Domain des Azure AD B2C-Mandanten. Verwenden Sie allgemeine Kopf- und Fußzeilen, die über relative Verknüpfungen verfügen, nicht erneut. Da diese Seiten in der Azure AD B2C Domäne gehostet werden, wenn sie nicht verwendet werden, sollten nur absolute URLs für alle Links verwendet werden. Es wird empfohlen, eine bestimmte Kopf- und Fußzeile mit absoluten URLs für Ihre mit Azure AD zusammenhängenden benutzerdefinierten Seiten zu verwenden, bei denen alle Commerce-spezifischen Module, für die eine Verbindung zum Retail Server erforderlich ist, entfernt wurden. Beispielsweise sollten die Module Favoriten, Suchleiste, Anmeldelink und Warenkorb nicht in Seiten enthalten sein, die in Azure AD B2C-Benutzerflows verwendet werden.

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a>Konfigurieren von Azure AD B2C Richtlinien mit benutzerdefinierten Seiteninformationen 

Im Azure Portal kehren Sie zur Seite **Azure AD B2C** zurück und anschließend auf dem Menü unter **Richtlinien** wählen Sie **Benutzerfluss (Richtlinien)**.

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a>Aktualisieren Sie die Richtlinie „registrieren und anmelden“ mit benutzerdefinierten Seiteninformationen

Um die Richtlinie „registrieren und anmelden“ mit benutzerdefinierten Seiteninformationen zu aktualisieren, folgen Sie diesen Schritten.

1. In der Richtlinie **Anmelden und abmelden** die Sie eben im Navigationsbereich konfiguriert haben, wählen Sie **Seitenlayouts** aus.
1. Wählen Sie das Layout **Einheitliche An- und Abmeldung auf der Seite** aus.
1. Hier können Sie die Option **Benutzerdefinierten Seiteninhalt verwwenden** auf **Ja** fest.
1. Im Feld **Benutzerdefinierte Seiten-URLe** geben Sie die vollständige Anmeldungs-URL ein. Schließt das Suffix **? preloadscripts=true** ein. Geben Sie beispielsweise ``www.<my domain>.com/sign-in?preloadscripts=true`` ein.
1. Wählen Sie im Feld **Seitenlayoutversion** die Version **2.1.0** oder höher aus (erfordert eine Modulbibliothek für Commerce-Version 10.0.15 oder höher).
1. Wählen Sie **Speichern** aus.
1. Wählen Sie das Layout **Lokale Kontoanmeldeseite** aus.
1. Hier können Sie die Option **Benutzerdefinierten Seiteninhalt verwwenden** auf **Ja** fest.
1. Im Feld **Benutzerdefinierte Seiten-URI** geben Sie die vollständige Anmeldungs-URL ein. Schließt das Suffix **? preloadscripts=true** ein. Geben Sie beispielsweise ``www.<my domain>.com/sign-up?preloadscripts=true`` ein.
1. Wählen Sie im Feld **Seitenlayoutversion** die Version **2.1.0** oder höher aus (erfordert eine Modulbibliothek für Commerce-Version 10.0.15 oder höher).
1. Im Abschnitt **Benutzerattribute** folgen Sie diesen Schritten:
    1. Für die Attribute **Vorname** und **Nachname** wählen Sie **Nein** in der Spalte **Erfordert Prüfung** aus.
    1. Beim Attribut **E-Mail-Adresse** sollte der Standardwert **Ja** in der Spalte **Erfordert Überprüfung** beibehalten werden. Diese Option stellt sicher, dass Benutzer, die sich mit einer bestimmten E-Mail-Adresse anmelden, bestätigen, ob sie die E-Mail-Adresse besitzen.
    1. Für die Attribute **E-Mail-Adresse** **Vorname** und **Nachname** wählen Sie **Nein** in der Spalte **Optional** aus.
1. Wählen Sie **Speichern** aus.

    ![Konfiguration der Richtlinie für die lokale Kontoanmeldeseite.](./media/B2C_SignInSignUp_Recommended_PageLayoutExample.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a>Aktualisieren Sie die Richtlinie „Profil bearbeiten“ mit den benutzerdefinierten Seiteninformationen

Um die Richtlinie „Profil bearbeiten“ mit benutzerdefinierten Seiteninformationen zu aktualisieren, folgen Sie diesen Schritten.

1. In der Richtlinie **Profil bearbeiten** die Sie eben im Navigationsbereich konfiguriert haben, wählen Sie **Seitenlayouts** aus.
1. Wählen Sie das Layout **Profilbearbeitungsseite** aus (abhängig von Ihrem Bildschirm müssen Sie möglicherweise an anderen Layoutoptionen vorbei nach unten scrollen).
1. Hier können Sie die Option **Benutzerdefinierten Seiteninhalt verwwenden** auf **Ja** fest.
1. Im Feld **Benutzerdefinierte Seiten-URI** geben Sie die vollständige Profilbearbeitungs-URL ein. Schließt das Suffix **? preloadscripts=true** ein. Geben Sie beispielsweise ``www.<my domain>.com/profile-edit?preloadscripts=true`` ein.
1. Wählen Sie als **Seitenlayoutversion** die Version **2.1.0** oder höher aus (erfordert eine Modulbibliothek für Commerce-Version 10.0.15 oder höher).
1. Im Abschnitt **Benutzerattribute** folgen Sie diesen Schritten:
    1. Für die Attribute **Vorname** und **Nachname** wählen Sie **Nein** in der Spalte **Optional** aus.
    1. Für die Attribute **Vorname** und **Nachname** wählen Sie **Nein** in der Spalte **Erfordert Prüfung** aus.
1. Wählen Sie **Speichern** aus.

### <a name="update-the-password-reset-policy-with-custom-page-information"></a>Aktualisieren Sie die Richtlinie „Kennwort zurücksetzen“ mit den benutzerdefinierten Informationen

Um die Richtlinie „Kennwort zurücksetzen“ mit benutzerdefinierten Seiteninformationen zu aktualisieren, folgen Sie diesen Schritten.

1. In der Richtlinie **Kennwort zurücksetzen** die Sie eben im Navigationsbereich konfiguriert haben, wählen Sie **Seitenlayouts** aus.
1. Wählen Sie das Layout **Kennwort-vergessen-Seite** aus.
1. Hier können Sie die Option **Benutzerdefinierten Seiteninhalt verwwenden** auf **Ja** fest.
1. Im Feld **Benutzerdefinierte Seiten-URI** geben Sie die vollständige Überprüfungs-URL ein. Schließt das Suffix **? preloadscripts=true** ein. Geben Sie beispielsweise ``www.<my domain>.com/password-reset-verification?preloadscripts=true`` ein.
1. Wählen Sie im Feld **Seitenlayoutversion** die Version **2.1.0** oder höher aus (erfordert eine Modulbibliothek für Commerce-Version 10.0.15 oder höher).
2. Wählen Sie **Speichern** aus.
3. Wählen Sie das Layout **Kennwortänderungsseite** aus.
4. Hier können Sie die Option **Benutzerdefinierten Seiteninhalt verwwenden** auf **Ja** fest.
5. Im Feld **Benutzerdefinierte Seiten-URI** geben Sie die vollständige URL zum Zurücksetzen von Passwörtern ein. Schließt das Suffix **? preloadscripts=true** ein. Geben Sie beispielsweise ``www.<my domain>.com/password-reset?preloadscripts=true`` ein.
6. Wählen Sie im Feld **Seitenlayoutversion** die Version **2.1.0** oder höher aus (erfordert eine Modulbibliothek für Commerce-Version 10.0.15 oder höher).
7. Wählen Sie **Speichern** aus.

## <a name="customize-default-text-strings-for-labels-and-descriptions"></a>Passen Sie Standardtextzeichenfolgen für Beschriftungen und Beschreibungen an

In der Modulbibliothek sind die Anmeldungsmodule mit Standardtextzeichenfolgen für Beschriftungen und Beschreibungen vorausgefüllt. Sie können die Zeichenfolgen im Eigenschaftenbereich des Moduls anpassen, an dem Sie arbeiten. Zusätzliche Zeichenfolgen auf der Seite (z. B. der Linktext **Kennwort vergessen?** oder der Aufruf **Ein Konto erstellen** für den Aktionstext) erfordert die Verwendung des Commerce Software Development Kit (SDK) und die Aktualisierung der Werte in der Datei global.json für das Anmeldemodul.

Beispielsweise ist der Standardtext für den Link Kennwort vergessenen **Vergessenes Kennwort?**. Nachfolgend wird der Standardtext auf der Anmeldeseite angezeigt.

![Der Standardtext für den Link Kennwort vergessenen auf der Anmeldeseite.](./media/B2C_SignUp_ModuleFace.png)

Sie könnnen jedoch in der Datei global.json für das Anmeldungsmodul in der Modulbibliothek den Text zu **Kennwort vergessen?** ändern, wie in der folgenden Abbildung dargestellt.

![Aktualisierter Hyperlinktext im Anmeldungsmodul global.json-Datei.](./media/B2C_CustomizingStringsForModule.png)

Nachdem Sie die Datei global.json aktualisiert und die Änderungen veröffentlicht haben, wird der neue Hyperlinktext im Anmeldungsmodul in Commerce und auf der Liveanmeldeseite angezeigt.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Domänennamen konfigurieren](configure-your-domain-name.md)

[Neuen E-Commerce-Mandanten bereitstellen](deploy-ecommerce-site.md)

[E-Commerce-Website erstellen](create-ecommerce-site.md)

[Zuordnen einer Dynamics 365 Commerce-Website zu einem Onlinekanal](associate-site-online-store.md)

[Robots.txt-Dateien verwalten](manage-robots-txt-files.md)

[URL-Umleitungen in Massen hochladen](upload-bulk-redirects.md)

[Einrichten eines B2C-Mandanten in Commerce](set-up-B2C-tenant.md)

[Konfigurieren Sie mehrere B2C-Mandanten in einer Commerce-Umgebung](configure-multi-B2C-tenants.md)

[Hinzufügen von Unterstützung für ein Content Delivery Network (CDN)](add-cdn-support.md)

[Standortbasierte Shop-Erkennung aktivieren](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]