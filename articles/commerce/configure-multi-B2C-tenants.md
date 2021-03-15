---
title: Mehrere B2C-Mandanten in einer Commerce-Umgebung konfigurieren
description: In diesem Thema wird beschrieben, wann und wie mehrere Microsoft Azure Active Directory (Azure AD) Business-to-Consumer (B2C)-Mandanten pro Kanal für die Benutzerauthentifizierung in einer dedizierten Dynamics 365 Commerce-Umgebung eingerichtet werden können.
author: BrianShook
manager: annbe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-12
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9a1af453349d69ef94d725e138a898c73ea052fa
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997599"
---
# <a name="configure-multiple-b2c-tenants-in-a-commerce-environment"></a>Mehrere B2C-Mandanten in einer Commerce-Umgebung konfigurieren

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wann und wie mehrere Microsoft Azure Active Directory (Azure AD) Business-to-Consumer (B2C)-Mandanten pro Kanal für die Benutzerauthentifizierung in einer dedizierten Dynamics 365 Commerce-Umgebung eingerichtet werden können.

## <a name="overview"></a>Übersicht

Dynamics 365 Commerce verwendet den Azure AD B2C-Cloud-Identitätsdienst zur Unterstützung von Benutzeranmeldeinformationen und Authentifizierungsströmen. Die Benutzer können die Authentifizierungsflüsse nutzen, um sich anzumelden, sich anzumelden und ihr Kennwort zurückzusetzen. Azure AD B2C speichert die sensiblen Authentifizierungsinformationen eines Benutzers, wie z.B. seinen Benutzernamen und sein Passwort. Der Benutzerdatensatz ist für jeden B2C-MiMandanten ter einzigartig und verwendet entweder die Anmeldedaten des Benutzernamens (E-Mail-Adresse) oder die Anmeldedaten des Anbieters der sozialen Identität.

In den meisten Fällen wird in einer Commerce-Umgebung ein einzelner Azure AD B2C-Mandanten verwendet. Commerce-Kunden können dann mehrere Sites in derselben Commerce-Umgebung erstellen und veröffentlichen, und auf diesen Sites werden dieselben Kundendaten verwendet. Wenn die Sites in der Umgebung jedoch als unterschiedliche Marken behandelt werden und den Benutzern als separate Unternehmen erscheinen sollen, kann ein B2C-Mandanten für den Kanal konfiguriert werden, der für die Trennung von Site und Marke verwendet wird.

## <a name="considerations-when-multiple-b2c-tenants-are-set-up-per-channel"></a>Überlegungen, wenn mehrere B2C-Mandanten pro Kanal eingerichtet werden

Wenn jeder Kanal oder jede Website als separates Unternehmen behandelt wird, ist es oft die beste Option, getrennte juristische Personen für die Benutzerauthentifizierung in Commerce zu verwenden. Wenn Sie jedoch jeden Kanal/jede Website in derselben Umgebung und derselben juristischen Person behalten möchten, aber für jede Website eine separate Benutzerauthentifizierung wünschen, ist es wichtig, dass Sie die folgenden Punkte berücksichtigen, bevor Sie fortfahren:

- Die Benutzer haben für jeden Kanal/jede Website ihre eigenen, eindeutigen Anmeldedaten.

    Dieselbe Person kann zwei getrennte Konten pro Kanal/Site haben, da jedes Konto ein eindeutiger Eintrag in einem separaten B2C-Mieter ist.

- In der Microsoft Dynamics-Umgebung werden separate Kundendatensätze für die Suche nach globalen Datensätzen zurückgegeben.

    Wenn ein Benutzer dieselbe E-Mail-Adresse über verschiedene Kanäle/Sites hinweg verwendet, werden bei der globalen Kundensuche Ergebnisse für jeden Kanal/Site zurückgegeben. (Es wird ein Kanalindikator) angezeigt.

- Das Adressbuch kann dazu verwendet werden, Benutzer zu gruppieren, sodass sie pro Kanal nachverfolgt werden können.
- Die Anzahl der Kundendatensätze pro Kanal kann sich erhöhen, und diese Erhöhung kann die Leistung der globalen Kundensuche beeinträchtigen.
- B2C-Mandanten müssen sorgfältig einem Kanal zugeordnet werden, um Situationen zu vermeiden, in denen sich Kunden für einen falschen Mandanten anmelden. Andernfalls kann es zu Verwirrung oder Problemen bei der Nachverfolgung kommen.

Die folgende Abbildung zeigt mehrere B2C-Mieter in einer Commerce-Umgebung.

![Mehrere B2C-Mandanten in einer Commerce-Umgebung](media/MultiB2C_In_Environment.png)

Wenn Sie entscheiden, dass Ihr Unternehmen unterschiedliche B2C-Mandanten pro Kanal in derselben Commerce-Umgebung benötigt, füllen Sie die Verfahren in den folgenden Abschnitten aus, um diese Funktion zu beantragen.

## <a name="request-that-b2c-per-channel-be-enabled-in-your-environment"></a>Beantragen Sie, dass B2C pro Kanal in Ihrer Umgebung aktiviert wird.

Wenn Sie derzeit möchten, dass verschiedene B2C-Mandanten pro Kanal in derselben Commerce-Umgebung verfügbar sind, müssen Sie eine Anfrage an Dynamics 365 Commerce senden. Weitere Informationen finden Sie unter [Unterstützung für Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md), oder besprechen Sie dieses Problem mit Ihrem Ansprechpartner für Commerce-Lösungen.

## <a name="configure-b2c-tenants-in-your-environment"></a>Konfigurieren von B2C-Mandanten in Ihrer Umgebung

Um B2C-Mandanten in Ihrer Umgebung zu konfigurieren, führen Sie die entsprechenden Verfahren in diesem Abschnitt aus.

### <a name="add-an-azure-ad-b2c-tenant"></a>Azure AD B2C-Mandant hinzufügen

Um einen Azure AD B2C-Mandanten zu Ihrer Umgebung hinzuzufügen, gehen Sie wie folgt vor.

1. Melden Sie sich beim Commerce Site Builder für Ihre Umgebung als Systemadministrator an. Um einen Azure AD B2C-Mandanten zu konfigurieren, müssen Sie Systemadministrator für die Commerce-Umgebung sein.
1. Wählen Sie im linken Navigationsbereich **Mandanteneinstellungen**, um ihn zu erweitern.
1. Wählen Sie **B2C-Einstellungen** und dann **Verwalten**.
1. Wählen Sie **B2C-Anwendung hinzufügen**, und geben Sie dann die folgenden Informationen ein:

    - **Anwendungsname**: Geben Sie den Namen ein, der für die Anwendung im Zusammenhang mit der Verwaltung der Anwendung in Commerce verwendet werden soll. Wir empfehlen Ihnen, den Anwendungsnamen zu verwenden, den Sie beim Einrichten der Azure AD B2C-Anwendung im Azure-Portal gewählt haben. Auf diese Weise können Sie dazu beitragen, Verwirrung zu vermeiden, wenn Sie B2C-Mandanten in Commerce verwalten.
    - **Mandantenname**: Geben Sie den B2C-Mandantennamen so ein, wie er im Azure-Portal erscheint.
    - **Passwort-Richtlinien-ID vergessen**: Geben Sie die Richtlinien-ID ein (den Namen der Richtlinie im Azure-Portal).
    - **Registrierungs-/Anmelde-Richtlinien-ID**: Geben Sie die Richtlinien-ID ein (den Namen der Richtlinie im Azure-Portal).
    - **Client GUID**: Geben Sie die Azure AD B2C-Mandanten-ID ein, wie sie im Azure-Portal erscheint (nicht die Anwendungs-ID für den B2C-Mandanten).
    - **Profilrichtlinien-ID bearbeiten**: Geben Sie die Richtlinien-ID ein (den Namen der Richtlinie im Azure-Portal).

1. Wenn Sie mit der Eingabe dieser Informationen fertig sind, wählen Sie **OK**, um Ihre Änderungen zu sichern.

> [!NOTE]
> Sie sollten Felder wie **Umfang**, **Nicht interaktive Richtlinien-ID**, **Nicht interaktive Client-ID**, **Benutzerdefinierte Anmeldedomäne** und **Anmelde-Richtlinien-ID** leer lassen, es sei denn, das Dynamics 365 Commerce-Team weist Sie an, sie einzustellen.
Ihr neuer Azure AD B2C-Mandanten sollte nun in der Liste unter **B2C-Anwendungen verwalten** erscheinen.

### <a name="manage-or-delete-an-azure-ad-b2c-tenant"></a>Verwalten oder löschen eines Azure AD B2C-Mandanten

1. Melden Sie sich beim Commerce Site Builder für Ihre Umgebung als Systemadministrator an. Um einen Azure AD B2C-Mandanten zu konfigurieren, müssen Sie Systemadministrator für die Commerce-Umgebung sein.
1. Wählen Sie im linken Navigationsbereich **Mandanteneinstellungen**, um ihn zu erweitern.
1. Wählen Sie **B2C-Einstellungen** und dann **Verwalten**.
1. Um einen B2C-Mandanten zu bearbeiten, wählen Sie das Bleistiftsymbol daneben. Um einen B2C-Mandanten zu löschen, wählen Sie das Mülleimersymbol daneben.
1. Wählen Sie **Speichern**, und wählen Sie dann **Veröffentlichen**, um Ihre Änderungen zu aktivieren.

> [!WARNING]
> Wenn ein B2C-Mandant für eine live/veröffentlichte Website konfiguriert ist, haben sich die Benutzer möglicherweise über Konten angemeldet, die auf dem Mandanten vorhanden sind. Wenn Sie einen konfigurierten Mandanten im Menü **Mandanteneinstellungen \> B2C-Mandant** löschen, entfernen Sie die Zuordnung dieses B2C-Mandanten zu Websites, die mit beliebigen Kanälen des Mandanten verknüpft sind. In diesem Fall können sich Ihre Benutzer möglicherweise nicht mehr bei ihren Konten anmelden. Seien Sie daher äußerst vorsichtig, wenn Sie einen konfigurierten Mandanten löschen.
>
> Wenn ein konfigurierter Mandanten gelöscht wird, werden der B2C-Mandant und die Datensätze weiterhin gepflegt, aber die Commerce-Systemkonfiguration dieses Mandanten wird geändert oder entfernt. Benutzer, die versuchen, sich bei der Site anzumelden oder anzumelden, legen einen neuen Kontodatensatz im Standard- oder neu zugeordneten B2C-Mandanten an, der für den Kanal der Site konfiguriert ist.
## <a name="configure-your-channel-with-a-b2c-tenant"></a>Konfigurieren Ihres Kanals mit einem B2C-Mandanten

1. Melden Sie sich beim Commerce Site Builder für Ihre Umgebung als Systemadministrator an. Um einen Azure AD B2C-Mandanten zu konfigurieren, müssen Sie Systemadministrator für die Commerce-Umgebung sein.
1. Wählen Sie im linken Navigationsbereich **Site-Einstellungen** aus, um den Bereich zu erweitern.
1. Wählen Sie **Kanäle**, und wählen Sie dann den zu konfigurierenden Kanal.
1. Wählen Sie im Eigenschaftsfenster auf der rechten Seite im Feld **B2C-Anwendung wählen** den konfigurierten Azure AD B2C-Mandanten, der für diesen Kanal verwendet werden soll.
1. Wählen Sie in der Befehlsleiste **Speichern und veröffentlichen**, um die neue oder aktualisierte Konfiguration zu übernehmen.

> [!WARNING]
> Wenn Sie die dem Channel zugeordnete B2C-Anwendung ändern, entfernen Sie die aktuellen Referenzen, die für alle Benutzer, die sich bereits in der Umgebung angemeldet haben, eingerichtet wurden. In diesem Fall sind alle Referenzen, die mit der aktuell zugeordneten B2C-Anwendung verbunden sind, für die Benutzer nicht verfügbar. Ändern Sie daher eine Azure AD B2C-Konfiguration des Channels nur dann, wenn Sie den Channel zum ersten Mal einrichten und sich noch keine Benutzer anmelden konnten. Andernfalls müssen sich die Benutzer möglicherweise erneut anmelden, um einen Datensatz im neuen Azure AD B2C-Mandanten zu erstellen.
## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Domänennamen konfigurieren](configure-your-domain-name.md)

[Neuen E-Commerce-Mandanten bereitstellen](deploy-ecommerce-site.md)

[E-Commerce-Website erstellen](create-ecommerce-site.md)

[Zuordnen einer Dynamics 365 Commerce-Website zu einem Onlinekanal](associate-site-online-store.md)

[Robots.txt-Dateien verwalten](manage-robots-txt-files.md)

[URL-Umleitungen in Massen hochladen](upload-bulk-redirects.md)

[Einrichten eines B2C-Mandanten in Commerce](set-up-B2C-tenant.md)

[Einrichten angepasster Seiten für die Benutzeranmeldungen](custom-pages-user-logins.md)

[Hinzufügen von Unterstützung für ein Content Delivery Network (CDN)](add-cdn-support.md)

[Standortbasierte Shop-Erkennung aktivieren](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]