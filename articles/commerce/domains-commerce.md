---
title: Domänen in Dynamics 365 Commerce
description: In diesem Artikel wird beschrieben, wie Domänen in Microsoft Dynamics 365 Commerce behandelt werden.
author: BrianShook
ms.date: 11/08/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: BrShoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: f1a2de7984aad7d291b8a4dc68f5690d57ebe6cc
ms.sourcegitcommit: 2b654e60e2553a5835ab5790db4ccfa58828fae7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/08/2022
ms.locfileid: "9750679"
---
# <a name="domains-in-dynamics-365-commerce"></a>Domänen in Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie Domänen in Microsoft Dynamics 365 Commerce behandelt werden.

Domänen sind Webadressen, mit denen in einem Webbrowser zu Dynamics 365 Commerce-Websites navigiert wird . Sie steuern die Verwaltung Ihrer Domäne mit einem ausgewählten Domänennamenserver (DNS)-Anbieter. Domänen werden durch den Dynamics 365 Commerce-Site Builder referenziert, um zu koordinieren, wie auf eine Website zugegriffen wird, wenn sie veröffentlicht wird. In diesem Artikel wird erläutert, wie Domänen während des gesamten Lebenszyklus der Entwicklung und des Starts der Commerce-Website behandelt und referenziert werden.

> [!NOTE]
> Ab dem 6. Mai 2022 werden alle in Dynamics 365 Commerce erstellten Umgebungen mit der `.dynamics365commerce.ms`-Domäne bereitgestellt und ersetzen das frühere Muster von `.commerce.dynamics.com`. Vorhandene Umgebungen, die mit der `.commerce.dynamics.com`-Domäne bereitgestellt werden, werden weiterhin funktionieren.

## <a name="provisioning-and-supported-host-names"></a>Bereitstellung und unterstützte Hostnamen

Bei der Bereitstellung einer E-Commerce-Umgebung in [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/) wird das Feld **Unterstützte Hostnamen** auf dem Bildschirm für die E-Commerce-Bereitstellung dazu verwendet, Domänen einzugeben, die der bereitgestellten Commerce-Umgebung zugeordnet werden. Bei diesen Domänen handelt es sich um DNS-Namen (Domänennamenserver), auf denen E-Commerce-Websites gehostet werden. Wenn Sie zu diesem Zeitpunkt eine Domäne eingeben, wird der Datenverkehr für die Domäne nicht zu Dynamics 365 Commerce umgeleitet. Der Datenverkehr für eine Domäne wird nur an den Commerce-Endpunkt weitergeleitet, wenn der DNS-CNAME-Eintrag aktualisiert wird, um den Commerce-Endpunkt mit der Domäne zu verwenden.

> [!NOTE]
> Es können mehrere Domänen in das Feld **Unterstützte Hostnamen** eingegeben werden, indem sie mit Semikolons getrennt werden.

Die folgende Abbildung zeigt den LCS-E-Commerce-Bereitstellungsbildschirm mit hervorgehobenem Feld **Unterstützte Hostnamen**. 

![LCS-E-Commerce-Bereitstellungsbildschirm mit hervorgehobenem Feld **Unterstützte Hostnamen**.](./media/Domains_ProvisioningeCommerceScreen_publish.png)

Sie können eine Serviceanforderung erstellen, um einer Umgebung zusätzliche Domänen hinzuzufügen, wenn die Bereitstellung bereits erfolgt ist. Um in LCS eine Serviceanforderung zu erstellen, wechseln Sie in Ihrer Umgebung zu **Support \> Support-Probleme** und wählen Sie **Einen Vorfall einreichen**.

## <a name="commerce-generated-urls"></a>Von Commerce generierte URLs

Bei der Bereitstellung einer Dynamics 365 Commerce-E-Commerce-Umgebung generiert Commerce eine URL, die die Arbeitsadresse für die Umgebung darstellt. Auf diese URL wird in dem in LCS angezeigten E-Commerce-Website-Link verwiesen, nachdem die Umgebung bereitgestellt wurde. Eine von Commerce generierte URL hat das Format `https://<e-commerce tenant name>.dynamics365commerce.ms`, wobei der Name des E-Commerce-Mandanten der in LCS für die Commerce-Umgebung eingegebene Name ist.

Sie können Hostnamen für Produktionsstandorte auch in einer Sandbox-Umgebung verwenden. Diese Option ist ideal, wenn Sie eine Website aus einer Sandbox-Umgebung in die Produktion kopieren.

## <a name="site-setup"></a>Site-Einstellungen

Nachdem Ihre E-Commerce-Umgebung bereitgestellt wurde, müssen Sie Ihre Website im Commerce-Website-Generator einrichten, um Ihre Website der Arbeits-URL zuzuordnen.

Wenn Sie zum ersten Mal eine Website im Site Builder einrichten, wird das **Ihre Site einrichten**-Dialogfeld angezeigt.

Die folgende Abbildung zeigt das **Ihre Website einrichten**-Dialogfeld für eine Website mit dem Namen „Standard“ an, wenn Sie zum ersten Mal im Site Builder auf die Website zugreifen.

![**Ihre Website einrichten**-Dialogfeld.](./media/Domains_SetupyoursiteScreen.png)

Mit dem Feld **Eine Domäne auswählen** können Sie einen der unterstützten Hostnamen, die für Ihre Website in LCS bereitgestellt wurden, im Site Builder Ihrer Website zuordnen.

Das Feld **Pfad** kann leer gelassen werden, oder es kann eine zusätzliche Pfadzeichenfolge hinzugefügt werden, die in Ihrer Arbeits-URL angezeigt wird. Wenn Sie das Feld **Pfad** leer lassen, wird die vom Commerce generierte Basis-URL der Website zugeordnet, die im Site Builder eingerichtet wird. Pfade müssen für jedes Website/Domänen-Paar eindeutig sein. Innerhalb des ausgewählten Standorts und der ausgewählten Domäne kann nur ein Standort in der Umgebung den leeren Pfad verwenden oder einer eindeutigen Pfadzeichenfolge zugeordnet werden. Jede beliebige Zeichenfolge, die dem **Pfad**-Feld während der Website-Einrichtung hinzugefügt wird, wird zu einem Unterpfad der von Commerce generierten Basis-URL, die für den Zugriff auf die Website in einem Webbrowser verwendet wird.

> [!NOTE]
> Der Pfad ist auch als **Abgleichspfad** bekannt, wenn ein Kanal im **Seiteneinstellungen \> Kanäle**-Konfigurationsabschnitt vom Site Builder hinzugefügt wird.

Wenn Sie im Website-Generator beispielsweise eine Website mit dem Namen „fabrikam“ in einem E-Commerce-Mandanten mit dem Namen „xyz“ haben und die Website mit einem leeren Pfad einrichten, greifen Sie in einem Webbrowser auf den veröffentlichten Website-Inhalt zu, indem Sie direkt zu der von Commerce generierten Basis-URL gehen:

`https://xyz.dynamics365commerce.ms`

Wenn Sie während der Einrichtung derselben Website einen Pfad für „fabrikam“ hinzugefügt hätten, würden Sie alternativ über die folgende URL in einem Webbrowser auf den veröffentlichten Website-Inhalt zugreifen:

`https://xyz.dynamics365commerce.ms/fabrikam`

## <a name="pages-and-urls"></a>Seiten und URLs

Nachdem Ihre Website mit einem Pfad eingerichtet wurde, bauen alle URLs, die Seiten im Site Builder zugeordnet sind, auf der Arbeits-URL (der von Commerce generierten URL oder der von Commerce generierten URL plus dem Pfad) für die Site auf. Durch das Erstellen einer neuen URL im Site Builder (**URLs /> + Neu**) durch Auswahl einer Seite aus der Liste in im Dialogfeld **Neue URL** und die Eingabe des URL-Pfads für diese Seite wird diese URL der ausgewählten Seite zugeordnet. Der URL-Pfadwert wird dann an die Arbeits-URL der Website angehängt, um auf die Seite zuzugreifen, und wird als `./<URL path>` in der URL-Liste der **URLs**-Seite im Site Builder gekennzeichnet.

Die folgende Abbildung zeigt das Dialogfeld **Neue URL** im Site Builder mit einem hervorgehobenen Beispiel-URL-Pfad. 

![Dialogfeld **Neue URL** im Site Builder.](./media/Domains_PageSetup2a.png)

Die folgende Abbildung zeigt die Seite **URLs** im Site Builder mit einer hervorgehobenen Beispiel-URL in der Liste.

![Führen Sie die Benutzerflussoption im Richtlinienfluss aus.](./media/Domains_URLsInSiteBuilder2a.png)

## <a name="domains-in-site-builder"></a>Domänen im Site Builder

Die unterstützten Hostnamenwerte können beim Einrichten einer Website als Domäne zugeordnet werden. Wenn Sie einen unterstützten Hostnamenwert als Domäne auswählen, wird die ausgewählte Domäne im gesamten Site Builder referenziert. Diese Domäne ist nur eine Referenz in der Commerce-Umgebung. Der Live-Datenverkehr für diese Domäne wird noch nicht an Dynamics 365 Commerce weitergeleitet.

Wenn Sie im Site Builder mit Websites arbeiten und zwei Websites mit zwei verschiedenen Domänen eingerichtet haben, können Sie das **?domain=**-Attribut Ihrer Arbeits-URL anfügen, um in einem Browser auf den veröffentlichten Website-Inhalt zuzugreifen.

Beispielsweise wurde die Umgebung „xyz“ bereitgestellt, und im Site Builder wurden zwei Websites erstellt und zugeordnet: eine mit der Domäne `www.fabrikam.com` und die andere mit der Domain `www.constoso.com`. Jede Website wurde mit einem leeren Pfad eingerichtet. Auf diese beiden Websites kann dann in einem Webbrowser wie folgt mit dem **?domain=**-Attribut zugegriffen werden:
- `https://xyz.dynamics365commerce.ms?domain=www.fabrikam.com`
- `https://xyz.dynamics365commerce.ms?domain=www.contoso.com`

Wenn in einer Umgebung mit mehreren bereitgestellten Domänen keine Domänenabfragezeichenfolge angegeben wird, verwendet Commerce die erste von Ihnen bereitgestellte Domäne. Wenn beispielsweise der Pfad „fabrikam“ beim Einrichten der Website zuerst angegeben wurde, könnte die URL `https://xyz.dynamics365commerce.ms` verwendet werden, um auf die veröffentlichte Website-Inhaltsseite für `www.fabrikam.com` zuzugreifen.

Sie können auch benutzerdefinierte Domänen hinzufügen. Gehen Sie dazu auf der Umgebungs-Commerce-Verwaltungsseite für das Projekt unter der Unterüberschrift **E-Commerce** und wählen Sie **+ benutzerdefinierte Domäne hinzufügen**. Der Schieberegler zeigt die vorhandenen benutzerdefinierten Domänen an und bietet die Option, eine neue benutzerdefinierte Domäne hinzuzufügen.

## <a name="update-which-commerce-scale-unit-is-used"></a>Aktualisieren Sie, welche Commerce Scale Unit verwendet wird

Die von Commerce verwendete Commerce Scale Unit (CSU) wird normalerweise ausgewählt, wenn eine Umgebung anfänglich erstellt wird. Mit Commerce können Sie ändern, welche CSU-Instanz Ihre Umgebung verwendet, wodurch Sie Ihre Architektur durch Self-Service-Funktionalität besser warten können und die Notwendigkeit, sich an den Support zu wenden, reduziert wird. Um Ihre CSU-Instanz zu aktualisieren, gehen Sie zur Commerce-Verwaltungsseite Ihrer Umgebung für das Projekt und wählen Sie dann **Skalierungseinheit aktualisieren** aus. Verwenden Sie den Schieberegler **Neue Commerce Scale Unit**, um eine neue CSU-Instanz aus der Liste der für Ihre Umgebung verfügbaren CSUs auszuwählen.

## <a name="traffic-forwarding-in-production"></a>Datenverkehrsweiterleitung in der Produktion

Sie können mehrere Domänen mithilfe von Domänenabfragezeichenfolgenparametern auf dem Endpunkt commerce.dynamics.com selbst simulieren. Wenn Sie jedoch in der Produktion live gehen möchten, müssen Sie den Datenverkehr für Ihre benutzerdefinierte Domäne an den `<e-commerce tenant name>.dynamics365commerce.ms`-Endpunkt weiterleiten.

Der `<e-commerce tenant name>.dynamics365commerce.ms`-Endpunkt unterstützt keine SSLs (Secure Sockets Layers) für benutzerdefinierte Domänen. Daher müssen Sie benutzerdefinierte Domänen mithilfe eines Front-Door-Dienstes oder eines Content Delivery Network (CDN) einrichten. 

Um benutzerdefinierte Domänen mithilfe eines Front-Door-Dienstes oder eines CDN einzurichten, haben Sie zwei Möglichkeiten:

- Richten Sie einen Front-Door-Dienst wie Azure Front Door ein, um den Front-End-Datenverkehr zu verarbeiten und eine Verbindung zu Ihrer Commerce-Umgebung herzustellen, was eine bessere Kontrolle über die Domänen- und Zertifikatsverwaltung und detailliertere Sicherheitsrichtlinien bietet.

- Verwenden Sie die von Commerce bereitgestellte Azure Front Door-Instanz, die eine Abstimmung mit dem Dynamics 365 Commerce-Team für die Domänenüberprüfung und den Erhalt von SSL-Zertifikaten für Ihre Produktionsdomäne erfordert.

> [!NOTE]
> Wenn Sie einen externen CDN- oder Front-Door-Dienst verwenden, stellen Sie sicher, dass die Anforderung mit dem von Commerce bereitgestellten Hostnamen, aber mit dem Header X-Forwarded-Host (XFH) \<custom-domain\> auf der Commerce-Plattform landet. Wenn Ihr Commerce-Endpunkt beispielsweise `xyz.dynamics365commerce.ms` und die benutzerdefinierte Domäne `www.fabrikam.com` lautet, sollte der Hostheader der weitergeleiteten Anforderung `xyz.dynamics365commerce.ms` lauten und der XFH-Header sollte `www.fabrikam.com` sein.

Informationen zum direkten Einrichten eines CDN-Dienstes finden Sie unter [Unterstützung für ein Content Delivery Network (CDN) hinzufügen](add-cdn-support.md).

Um die von Commerce bereitgestellte Azure Front Door-Instanz zu verwenden, müssen Sie eine Serviceanforderung für die Unterstützung bei der CDN-Einrichtung durch das Commerce-Onboarding-Team erstellen. 

- Sie müssen Ihren Firmennamen, die Produktionsdomäne, die Umgebungs-ID und den Namen des Produktions-E-Commerce-Mandanten angeben. 
- Sie müssen bestätigen, ob diese Serviceanforderung für eine vorhandene Domäne (die für eine derzeit aktive Website verwendet wird) oder eine neue Domäne gedacht ist. 
- Für eine neue Domäne können die Domänenüberprüfung und das SSL-Zertifikat in einem einzigen Schritt durchgeführt werden. 
- Für eine Domäne, die eine vorhandene Website bedient, ist ein mehrstufiger Prozess erforderlich, um die Domänenüberprüfung und das SSL-Zertifikat einzurichten. Für diesen Prozess gilt eine 7-Tage-Service-Level-Agreement (SLA) für die Inbetriebnahme einer Domäne, da mehrere aufeinanderfolgende Schritte enthalten sind.

Um in LCS eine Serviceanforderung zu erstellen, wechseln Sie in Ihrer Umgebung zu **Support \> Support-Probleme** und wählen Sie **Einen Vorfall einreichen**.

> [!NOTE]
> Benutzerdefinierte Domänen mit SSL werden nur in Produktionsumgebungen unterstützt. Verwenden Sie bei Umgebungen, die nicht der Produktion dienen, wie Sandbox- und Benutzerakzeptanztests (UAT) die von Commerce generierte URL, um in einem Webbrowser auf veröffentlichte Inhalte zuzugreifen.

## <a name="ssl-certificate-process"></a>SSL-Zertifikatsprozess

Wenn eine Serviceanfrage eingereicht wird, koordiniert das Commerce-Team die folgenden Schritte mit Ihnen.

Für neue Domains:
- Das Commerce-Team richtet die (von Commerce gehostete) Azure Front Door-Instanz ein.
- Das Commerce-Team stellt dann den CNAME-Datensatz bereit, um auf Ihre benutzerdefinierte Domäne zu verweisen.
- Nachdem der CNAME-Datensatz aktualisiert wurde, kann die von Commerce gehostete Azure Front Door-Instanz den Domänenbesitz überprüfen und das SSL-Zertifikat abrufen.

Für vorhandene/aktive Domänen:
- Das Commerce-Team weist Sie an, einen `afdverify.<custom-domain>`-CNAME-Eintrag hinzuzufügen , der Ihrem Domänen-DNS-Anbieter zur Verfügung gestellt werden soll.
- Nach Abschluss des Vorgangs fügt das Commerce-Team die Domäne der Azure Front Door-Instanz hinzu und stellt zusätzliche DNS-TXT-Einträge bereit, die dem DNS für die Domäne hinzugefügt werden sollen.
- Nach Abschluss der TXT-Datensätze führt das Commerce-Team die Azure Front Door-Aktualisierungen für die Domäne durch, in der das SSL-Zertifikat eingerichtet wird.

## <a name="apex-domains"></a>Apex-Domänen

Die von Commerce bereitgestellte Azure Front Door-Instanz unterstützt keine Apex-Domänen (Stammdomänen, die keine Subdomänen enthalten). Für die Auflösung von Apex-Domänen ist eine IP-Adresse erforderlich, und die Commerce Azure-Front Door-Instanz ist nur mit virtuellen Endpunkten vorhanden. Um eine Apex-Domain zu verwenden, haben Sie die folgenden Möglichkeiten:

- **Option 1** – Verwenden Sie Ihren DNS-Anbieter, um die Apex-Domäne in eine „www“ -Domäne umzuleiten. Beispielsweise leitet fabrikam.com an `www.fabrikam.com` weiter, wo `www.fabrikam.com` der CNAME-Datensatz ist, der auf die von Commerce gehostete Azure Front Door-Instanz verweist.

- **Option 2** – Wenn Ihr DNS-Anbieter ALIAS-Einträge unterstützt, können Sie die Apex-Domäne auf den Azure Front Door-Endpunkt verweisen, wodurch sichergestellt wird, dass die IP-Änderung durch den Endpunkt widergespiegelt wird. Sie müssen die Azure Front Door-Instanz selbst hosten.
  
- **Möglichkeit 3** – Wenn Ihr DNS-Anbieter keine ALIAS-Einträge unterstützt, müssen Sie Ihren DNS-Anbieter zu Azure DNS ändern und sowohl Azure DNS als auch die Azure Front Door-Instanz selbst hosten.

> [!NOTE]
> Wenn Sie Azure Front Door verwenden, müssen Sie im selben Abonnement auch ein Azure-DNS einrichten. Die auf Azure DNS gehostete Apex-Domäne kann als Alias-Eintrag auf Ihre Azure-Fornt-Door verweisen. Dies ist die einzige Problemumgehung, da Apex-Domänen immer auf eine IP-Adresse verweisen müssen.
  
Wenn Sie Fragen zu Apex-Domänen haben, wenden Sie sich bitte an den [Microsoft-Support](https://support.microsoft.com/).

  ## <a name="additional-resources"></a>Zusätzliche Ressourcen

  [Neuen E-Commerce-Mandanten bereitstellen](deploy-ecommerce-site.md)

  [Onlineshopkanal einrichten](./channel-setup-online.md)

  [E-Commerce-Website erstellen](create-ecommerce-site.md)

  [Zuordnen einer Dynamics 365 Commerce-Website zu einem Onlinekanal](associate-site-online-store.md)

  [Robots.txt-Dateien verwalten](manage-robots-txt-files.md)

  [URL-Umleitungen in Massen hochladen](upload-bulk-redirects.md)

  [Einrichten eines B2C-Mandanten in Commerce](set-up-B2C-tenant.md)

  [Einrichten angepasster Seiten für die Benutzeranmeldungen](custom-pages-user-logins.md)

  [Konfigurieren Sie mehrere B2C-Mandanten in einer Commerce-Umgebung](configure-multi-B2C-tenants.md)

  [Hinzufügen von Unterstützung für ein Content Delivery Network (CDN)](add-cdn-support.md)

  [Standortbasierte Shop-Erkennung aktivieren](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
