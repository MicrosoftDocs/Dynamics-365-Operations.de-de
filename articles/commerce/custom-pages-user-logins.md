---
title: Einrichten angepasster Seiten für die Benutzeranmeldung
description: In diesem Thema wird beschrieben, wie Sie benutzerdefinierte Seiten in Microsoft Dynamics 365 Commerce erstellen, die benutzerdefinierte Anmeldungen für Benutzer von Mandanten von Azure Active Directory (Azure AD) Onlinebankenlösungen (B2C) verarbeiten.
author: brianshook
manager: annbe
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 71c0f0b6969985b04262b522dd2165eb1475878d
ms.sourcegitcommit: 9a2e9f7dfec47c42178bb67a3e099e610515baf3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/16/2020
ms.locfileid: "3456971"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a>Angepasste Seiten für die Benutzeranmeldung einrichten


[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie benutzerdefinierte Seiten in Microsoft Dynamics 365 Commerce erstellen, die benutzerdefinierte Anmeldungen für Benutzer von Mandanten von Azure Active Directory (Azure AD) Onlinebankenlösungen (B2C) verarbeiten.

## <a name="overview"></a>Übersicht

Um benutzerdefinierte Seiten zu verwenden, die in Dynamics 365 Commerce erstellt werden können, um Benutzeranmeldungsflüsse zu verarbeiten, müssen Sie die Azure AD Richtlinien festlegen, auf die in der Geschäftsumgebung verwiesen wird. Sie können die Azure AD B2C Richtlinien „An- und Abmeldung“, „Profilverwaltung“ und „Kennwortzurücksetzung“ mithilfe der Azure AD B2C Anwendung konfigurieren. Die Azure AD B2C Mandanten- und Richtliniennamen können dann während des Bereitstellungsprozesses referenziert werden, der für die Handelsumgebung mithilfe von Microsoft Dynamics Lifecycle Services (LCS) ausgeführt wird.

Die benutzerdefinierten Handelsseiten können erstellt werden, indem Anmeldung, Abmeldung, Kontoprofile bearbeiten oder Kennwortrücksetzungsmodul verwendet wird. Die Seite URLs, die für die benutzerdefinierten Seiten veröffentlicht werden, sollten dann in Azure AD B2C Richtlinienkonfigurationen im Azureportal referenziert werden.

## <a name="set-up-b2c-policies"></a>B2C Richtlinien einrichten

Nachdem Sie den Mandanten Azure AD B2C eingerichtet haben und diesen der Handelsumgebung zugeordnet haen, wechseln Sie zu **Azure AD B2C** im Azure Portal und anschließend wählen Sie **Richtlinien**, **Benutzerfluss (Richtlinien)**.

![Benutzerfluss (Richtlinien) Befehl im Menü](./media/B2C_CustomPage_PoliciesMenu.png)

Sie können jetzt Registrieren und Anmelden, Profilbearbeitung und Kennwortrücksetzung im Fluss konfigurieren.

### <a name="configure-the-sign-up-and-sign-in-policy"></a>Konfigurieren von Registrieren und Anmelden in der Richtlinie

Um die Richtlinie Registrieren und Anmelden zu konfigurieren führen Sie die folgenden Schritte aus.

1. Wählen Sie **Neuer Benutzerfluss**, und dann, auf der Registerkarte **Empfohlen** wählen Sie die Richtlinie **Registrieren und Anmelden**.
1. Geben Sie einen Namen für die Richtlinie ein (z.B. **B2C \_1\_SignInSignUp**).
1. Im Abschnitt **Identitätsanbieter** wählen Sie den Identitätsanbieter aus, den Sie für die Richtlinie verwenden möchten. Es muss mindestens **E-Mail-Registrierung** ausgewählt werden.
1. In der Spalte **Attribut sammeln** aktivieren Sie die Kontrollkästchen für **E-Mail-Adresse**, **Vorname** und **Nachname** aus.
1. In der Spalte **Rücknahme anfordern** aktivieren Sie die Kontrollkästchen für **E-Mail-Adressen**, **Vorname**, **Identitätsanbieter**, **Nachname** und **Objekt-ID des Benutzers**.

    ![Attribute und Ansprüche ausgewählt](./media/B2C_SignInSignUp_Attributes.png)

1. **OK** wählen, um die Richtlinie zu erstellen.
1. Doppelklicken Sie auf den neuen Richtliniennamen, und wählen dann im Navigationsbereich **Eigenschaften**.
1. Legen Sie **Aktivieren Sie JavaScript erzwingt Seitenlayout (Vorschau)** auf **Aktiviert** fest.

    ![Eigenschaftenseite für die neue Richtlinie](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> Der Richtlinienname verweist ganz auf die Handelsumgebung. (Das Präfix **B2C\_1\_** ist in der Referenz enthalten.) Richtlinien können nicht umbenannt werden, nachdem sie erstellt wurden. Wenn Sie eine vorhandene Richtlinie für die Handelsumgebung ersetzen, können Sie die ursprüngliche Richtlinie löschen und eine neue Richtlinie erstellen, die denselben Namen hat. Falls die Umgebung bereits bereitgestellt wurde, können Sie den neuen Richtliniennamen durch eine Serviceanforderung senden.

Sie kehren zu dieser Richtlinie zurück, um die Einrichtung zu beenden, nachdem Sie die benutzerdefinierten Seiten erstellt haben. Jetzt schließen Sie die Richtlinie, um zur Seite **Benutzerfluss (Richtlinien)** im Azure-Portal zurückzukehren.

### <a name="configure-the-profile-editing-policy"></a>Konfigurieren Sie die Profilbearbeitungsrichtlinie

Um die Profilbearbeitungsrichtlinie zu konfigurieren, folgen Sie diesen Schritten.

1. Wählen Sie **Neuer Benutzerfluss**, und dann auf der Registerkarte **Empfohlen** wählen Sie die Richtlinie **Profil bearbeiten**.
1. Geben Sie einen Namen für die Richtlinie ein (z.B. **B2C\_1\_EditProfile**).
1. Im Abschnitt **Identitätsanbieter** wählen Sie den Identitätsanbieter aus, den Sie für die Richtlinie verwenden möchten. Es muss mindestens **Lokale Kontoen-Anmeldung** ausgewählt werden.
1. In der Spalte **Attribut sammeln** aktivieren Sie die Kontrollkästchen für **E-Mail-Adresse** **Nachname** aus.
1. In der Spalte **Rücknahme anfordern** aktivieren Sie die Kontrollkästchen für **E-Mail-Adressen**, **Vorname**, **Identitätsanbieter**, **Nachname** und **Objekt-ID des Benutzers**.
1. **OK** wählen, um die Richtlinie zu erstellen.
1. Doppelklicken Sie auf den neuen Richtliniennamen, und wählen dann im Navigationsbereich **Eigenschaften**.
1. Legen Sie **Aktivieren Sie JavaScript erzwingt Seitenlayout (Vorschau)** auf **Aktiviert** fest.

Sie kehren zu dieser Richtlinie zurück, um die Einrichtung zu beenden, nachdem Sie die benutzerdefinierten Seiten erstellt haben. Jetzt schließen Sie die Richtlinie, um zur Seite **Benutzerfluss (Richtlinien)** im Azure-Portal zurückzukehren.

### <a name="configure-the-password-reset-policy"></a>Konfigurieren Sie die Kennwortrücksetzungs „Richtlinie“

Um die Kennwortzurücksetzungsrichtlinie zu konfigurieren, folgen Sie diesen Schritten.

1. Wählen Sie **Neuer Benutzerfluss**, und dann auf der Registerkarte **Vorschau** wählen Sie die Richtlinie **Kennwor zurücksetzen v1.1**.

    ![Richtlinie der Kennwortrücksetzung v1.1 ausgewählt auf der Vorschauregisterkarte](./media/B2C_ForgetPassword_Menu.png)

1. Geben Sie einen Namen für die Richtlinie ein (z.B. **B2C\_1\_ForgetPassword**).
1. Im Abschnitt **Identitätsanbieter** wählen Sie **Rücksetzungskennwort mithilfe der E-Mail-Adresse** aus.
1. In der Spalte **Anforderung zurückgeben** aktivieren Sie die Kontrollkästchen für **E-Mail-Adressen**, **Vorname**, **Nachname** und **Objekt-ID des Benutzers**.

    ![Anforderung ausgewählt](./media/B2C_ForgetPassword_Attributes.png)

1. **OK** wählen, um die Richtlinie zu erstellen.
1. Doppelklicken Sie auf den neuen Richtliniennamen, und wählen dann im Navigationsbereich **Eigenschaften**.
1. Legen Sie **Aktivieren Sie JavaScript erzwingt Seitenlayout (Vorschau)** auf **Aktiviert** fest.

Sie kehren zu dieser Richtlinie zurück, um die Einrichtung zu beenden, nachdem Sie die benutzerdefinierten Seiten erstellt haben. Jetzt schließen Sie die Richtlinie, um zur Seite **Benutzerfluss (Richtlinien)** im Azure-Portal zurückzukehren.

## <a name="build-the-custom-pages"></a>Benutzerdefinierte Seiten erstellen

Um benutzerdefinierte die Seiten zu erstellen, um Benutzer-Registrierungen zu behandeln, folgen Sie diesen Schritten.

1. Im Handels-Erstellungstool gehen Sie zu Ihrer Site.
1. Erstellen Sie die folgenden fünf Vorlagen und fünf Seiten:

    - Eine Vorlage **Anmelden** und eine Seite die das Anmeldungsmodul verwendet.
    - Eine Vorlage **Abmelden** und eine Seite die das Abmeldungsmodul verwendet.
    - Eine Vorlage **Kennwort zurücksetzen** und Seite, die das Kennwortrücksetzungsmodul verwenden.
    - Eine Vorlage **Kennwort zurücksetzen prüfen** und Seite, die das Kennwortrücksetzungsmodul überprüft.
    - Eine Vorlage **Profil bearbeiten** und Seite, die das Kundenprofil verwenden Modul bearbeiten

Wenn Sie die Seiten erstellen, folgen Sie diesen Richtlinien:

- Für jede Seite oder Modul verwenden Sie das Layout und den Stil, die am besten Ihren Geschäftsanforderungen entsprechen.
- Veröffentlichen Sie alle Seiten und URLs, die in der Azure AD B2C Einstellung verwendet werden müssen.
- Nachdem die Seiten und URLs veröffentlicht wurden, sammeln Sie die URLs, die für die Azure AD B2C Richtlinienkonfiguration verwendet werden müssen. Ein **?preloadscripts=true** Suffix wird jeder URL hinzugefügt, wenn sie verwendet wird.

> [!IMPORTANT]
> Verwenden Sie die allgemeine Kopf- und Fußzeilen nicht erneut, die relative Verknüpfungen verfügen. Da diese Seiten in der Azure AD B2C Domäne gehostet werden, wenn sie nicht verwendet werden, sollten nur absolute URLs für alle Links verwendet werden.

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a>Konfigurieren von Azure AD B2C Richtlinien mit benutzerdefinierten Seiteninformationen 

Im Azure Portal kehren Sie zur Seite **Azure AD B2C** zurück und anschließend auf dem Menü unter **Richtlinien** wählen Sie **Benutzerfluss (Richtlinien)**.

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a>Aktualisieren Sie die Richtlinie „registrieren und anmelden“ mit benutzerdefinierten Seiteninformationen

Um die Richtlinie „registrieren und anmelden“ mit benutzerdefinierten Seiteninformationen zu aktualisieren, folgen Sie diesen Schritten.

1. In der Richtlinie **Anmelden und abmelden** die Sie eben im Navigationsbereich konfiguriert haben, wählen Sie **Seitenlayouts** aus.
1. Wählen Sie das Layout **Einheitliche An- und Abmeldung auf der Seite** aus.
1. Hier können Sie die Option **Benutzerdefinierten Seiteninhalt verwwenden** auf **Ja** fest.
1. Im Feld **Benutzerdefinierte Seiten-URLe** geben Sie die vollständige Anmeldungs-URL ein. Schließt das Suffix **? preloadscripts=true** ein. Geben Sie beispielsweise ``www.<my domain>.com/sign-in?preloadscripts=true`` ein.
1. Im Feld **Seitenlayoutversion (Vorschau)** wählen Sie **1.2.0** aus.
1. Wählen Sie das Layout **Lokale Kontoanmeldeseite** aus.
1. Hier können Sie die Option **Benutzerdefinierten Seiteninhalt verwwenden** auf **Ja** fest.
1. Im Feld **Benutzerdefinierte Seiten-URI** geben Sie die vollständige Anmeldungs-URL ein. Schließt das Suffix **? preloadscripts=true** ein. Geben Sie beispielsweise ``www.<my domain>.com/sign-up?preloadscripts=true`` ein.
1. Im Feld **Seitenlayoutversion (Vorschau)** wählen Sie **1.2.0** aus.
1. Im Abschnitt **Benutzerattribute** folgen Sie diesen Schritten:

    1. Für die Attribute **E-Mail-Adresse** **Vorname** und **Nachname** wählen Sie  **Nein** im Feld **Erfordert Prüfung** aus.
    1. Für die Attribute **Vorname** und **Nachname** wählen Sie **Nein** im Feld **Optional** aus.

    ![Konfiguration des lokalen Kontos sich als Neukunde Seitenrichtlinie an](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a>Aktualisieren Sie die Richtlinie „Profil bearbeiten“ mit den benutzerdefinierten Seiteninformationen

Um die Richtlinie „Profil bearbeiten“ mit benutzerdefinierten Seiteninformationen zu aktualisieren, folgen Sie diesen Schritten.

1. In der Richtlinie **Profil bearbeiten** die Sie eben im Navigationsbereich konfiguriert haben, wählen Sie **Seitenlayouts** aus.
1. Wählen Sie das Layout **Profilbearbeitungsseite** aus.
1. Hier können Sie die Option **Benutzerdefinierten Seiteninhalt verwwenden** auf **Ja** fest.
1. Im Feld **Benutzerdefinierte Seiten-URI** geben Sie die vollständige Profilbearbeitungs-URL ein. Schließt das Suffix **? preloadscripts=true** ein. Geben Sie beispielsweise ``www.<my domain>.com/profile-edit?preloadscripts=true`` ein.
1. Im Feld **Seitenlayoutversion (Vorschau)** wählen Sie **1.2.0** aus.
1. Im Abschnitt **Benutzerattribute** folgen Sie diesen Schritten:

    1. Für die Attribute **E-Mail-Adresse**, **Vorname** wählen Sie **Nein** aus im Feld **Erfordert Prüfung**.
    1. Für die Attribute **Vorname** und **Nachname** wählen Sie **Nein** im Feld **Optional** aus.

### <a name="update-the-password-reset-policy-with-custom-page-information"></a>Aktualisieren Sie die Richtlinie „Kennwort zurücksetzen“ mit den benutzerdefinierten Informationen

Um die Richtlinie „Kennwort zurücksetzen“ mit benutzerdefinierten Seiteninformationen zu aktualisieren, folgen Sie diesen Schritten.

1. In der Richtlinie **Kennwort zurücksetzen** die Sie eben im Navigationsbereich konfiguriert haben, wählen Sie **Seitenlayouts** aus.
1. Wählen Sie das Layout **Neue Kennwortseite** aus.
1. Hier können Sie die Option **Benutzerdefinierten Seiteninhalt verwwenden** auf **Ja** fest.
1. Im Feld **Benutzerdefinierte Seiten-URI** geben Sie die vollständige URL zum Zurücksetzen von Passwörtern ein. Schließt das Suffix **? preloadscripts=true** ein. Geben Sie beispielsweise ``www.<my domain>.com/passwordreset?preloadscripts=true`` ein.
1. Im Feld **Seitenlayoutversion (Vorschau)** wählen Sie **1.2.0** aus.
1. Wählen Sie das Layout **Kontoenprüfungsseite** aus.
1. Hier können Sie die Option **Benutzerdefinierten Seiteninhalt verwwenden** auf **Ja** fest.
1. Im Feld **Benutzerdefinierte Seiten-URI** geben Sie die vollständige Überprüfungs-URL ein. Schließt das Suffix **? preloadscripts=true** ein. Geben Sie beispielsweise ``www.<my domain>.com/passwordreset-verification?preloadscripts=true`` ein.
1. Im Feld **Seitenlayoutversion (Vorschau)** wählen Sie **1.2.0** aus.



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a>Passen Sie Standardtextzeichenfolgen für Beschriftungen und Beschreibungen an

Im Starter Kit sind die Anmeldemodule mit Standardtextzeichenfolgen für Beschriftungen und Beschreibungen vorausgefüllt. Sie können diese Zeichenfolgen in Software Development Kit (SDK) anpassen, indem Sie die Werte in der global.json-Datei für das Zeichen im Modul aktualisieren.

Beispielsweise ist der Standardtext für den Link Kennwort vergessenen **Vergessenes Kennwort?**. Nachfolgend wird der Standardtext auf der Anmeldeseite angezeigt.

![Der Standardtext für den Link Kennwort vergessenen auf der Anmeldeseite](./media/B2C_SignUp_ModuleFace.png)

Sie könnnen jedoch in der global.json-Datei für das Starter Kit Anmeldungsmodul den Text **Kennwort vergessen?** bearbeiten, wie in der folgenden Abbildung dargestellt wird.

![Aktualisierter Hyperlinktext im Anmeldungsmodul global.json-Datei](./media/B2C_CustomizingStringsForModule.png)

Nachdem Sie die global.json-Datei aktualisiert und die Änderungen veröffentlicht haben, wird der neue Hyperlinktext im Vorzeichen des Moduls in Commerce und auf der Liveanmeldeseite angezeigt.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Ihren Domänennamen konfigurieren](configure-your-domain-name.md)

[Bereitstellen einer neuen E-Commerce-Webseite](deploy-ecommerce-site.md)

[Onlineshopkanal einrichten](online-stores.md)

[E-Commerce-Site erstellen](create-ecommerce-site.md)

[Zuordnen einer Onlinewebseite zu einem Kanal](associate-site-online-store.md)

[Verwalten von robots.txt-Dateien](manage-robots-txt-files.md)

[URL-Weiterleitungen in großen Mengen hochladen](upload-bulk-redirects.md)

[Einrichten eines B2C-Mandanten in Commerce](set-up-B2C-tenant.md)

[Konfigurieren Sie mehrere B2C-Mandanten in einer Commerce-Umgebung](configure-multi-B2C-tenants.md)

[Hinzufügen von Unterstützung für ein Content Delivery Network (CDN)](add-cdn-support.md)

[Standortbasierte Shop-Erkennung aktivieren](enable-store-detection.md)
