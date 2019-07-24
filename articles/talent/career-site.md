---
title: Funktionen der Website mit Stellenangeboten in Attract
description: Dieses Thema bietet einen Überblick über die Funktionen der Website mit Stellenangeboten für Kandidaten in Attract.
author: hasrivas
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hasrivas
ms.search.validFrom: 2019-02-12
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: e51fb00536884d2b3815c05a0968714d8b9326f2
ms.sourcegitcommit: a6b32be10b6eb6340f8f68261bf62d0202c03dd1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/05/2019
ms.locfileid: "1729702"
---
# <a name="career-site-functionality-in-attract"></a>Funktionen der Website mit Stellenangeboten in Attract

[!include[banner](../includes/banner.md)]

Dieses Thema bietet einen Überblick über die Funktionen der Website mit Stellenangeboten für Kandidaten in Microsoft Dynamics 365 for Talent: Attract. Es wird auch beschrieben, wie diese Funktionen eingerichtet werden.

Attract bietet eine Website mit Stellenangeboten für jede Umgebung in einem Mandanten. Wenn beispielsweise eine Organisation über eine Entwicklungsumgebung und einer Testumgebung verfügt, wird eine Website mit Stellenangeboten für die Entwicklungsumgebung und eine weitere für die der Testumgebung bereitgestellt. Jede Website mit Stellenangeboten ist vollständig isoliert und verfügt über einen eigenen Authentifizierungsmechanismus. Stellen- und Kandidatenprofile werden zwischen Websites mit Stellenangeboten nicht freigegeben.

Standardmäßig ist die Website mit Stellenangeboten öffentlich. Daher können Kandidaten alle Stellen anzeigen, die als extern markiert werden, ohne sich anmelden zu müssen. Allerdings ist für alle weiteren Aktivitäten erforderlich, dass die Kandidaten sich anmelden.

## <a name="career-site-management"></a>Verwaltung der Website mit Stellenangeboten

Um die Werte für die folgenden Elemente festzulegen, melden Sie sich als Administrator in Attract an, wählen Sie im Menü **Einstellungen** (Zahnradsymbol) die Option **Administratorcenter** und anschließend die Registerkarte **Unternehmensdaten** aus.

-   **Organisationsname** - Der Organisationsname wird auf der Navigationsleiste oben auf der Website mit Stellenangeboten angezeigt. Wenn sie den Organisationsnamen auswählen, gelangen Kandidaten auf eine Seite, auf der alle offenen Stellen aufgeführt werden.

-   **Organisationslogo** - Ein Bild des Organisationslogos wird oben links der Website mit Stellenangeboten angezeigt. Wenn sie das Logobild auswählen, gelangen Kandidaten auf eine Seite, auf der alle offenen Stellen aufgeführt werden.

    > [!NOTE] 
    > Das Logobild, das auf der Website mit Stellenangeboten angezeigt wird, weist eine feste Höhe von 20 Pixeln (px) auf. Das Bild, das Sie im Administratorcenter hinzufügen, wird passend skaliert. Daher kann sich die Breite abhängig vom Bild ändern.
 
Um die Werte für die folgenden Elemente festzulegen, melden Sie sich als Administrator in Attract an, wählen Sie im Menü **Einstellungen** die Option **Administratorcenter** und anschließend die Registerkarte **Verwaltung der Website mit Stellenangeboten** aus.

-   **Suchmaschinen-Optimierung** - Wenn die Option aktiviert ist, können alle auf der Attract-Website mit Stellenangeboten veröffentlichten Stellen über öffentliche Suchmaschinen wie Bing und Google gesucht werden. 

    > [!NOTE] 
    > Es kann zu einer Verzögerung zwischen der Aktivierung dieser Einstellung und dem Erscheinend der Suchergebnisse kommen, je nach der verwendeten Suchmaschine.
    
-   **Geschäftsbedingungen** - Sofern aktiviert müssen alle Kandidaten, die sich auf eine Stelle bewerben, den AGB der Organisation zustimmen. Der Attract-Administrator kann eine eigenen Zustimmungstext und den Link zu der AGB- Seite konfigurieren. 

        
## <a name="career-site-urls"></a>ULRs der Website mit Stellenangeboten

Die folgende Liste enthält die häufig verwendetn URLs der Website mit Stellenangeboten und die Methode für den Zugriff.

-   **URL der Startseite der Webiste mit Stellenangeboten** - Um die URL der Startseite der Website mit Stellenangeboten anzuzeigen, menden Sie sich in Attract als ein Administrator an, wählen Sie **Administratorcenter** im Menü **Einstellungen** aus und wählen Sie anschließend die Registerkarte **Verwaltung der Website mit Stellenangeboten** aus.

-   **Bewerbungs-URL einzelner Stellenausschreibungen** - Wenn Sie zum ersten Mal eine [externe Stelle veröffentlichen](Creating-jobs-Attract.md#postings), können Sie den **Bewerben**-Link aus der Attract-Anwendung kopieren. Die URL für diesen Link hat folgendes Format: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)

-   **Bewerbungs-URL einzelner Stellenausschreibungen** - Die URL der Stellenausschreibung ist eine Teilzeichenfole der Bewerbungs-URL. Sie besteht aus allem bis zur Stellennummer. Daher lautet die URL der Stellenausschreibung der vorherige Bewerbungs-URL wie folgt: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)

## <a name="authentication-options"></a>Authentifizierungsoptionen

Kandidaten haben folgende Anmeldungsoptionen bei einer Attract-Website mit Stellenangeboten:

-   Persönliches Konto:

    -   LinkedIn

    -   Microsoft

    -   Google

    -   Facebook

-   Geschäfts- oder Schulkonto:

    -   Microsoft Azure Active Directory (Azure AD)

Azure AD-Anmeldung ist nur für interne Kandidaten vorgesehen. Daher funktioniert sie nur bei internen Kandidaten, die ihre Azure AD-Unternehmensanmeldeinformationen verwenden. Ein Kandidat z. B., der derzeit ein Mitarbeiter von Contoso Ltd ist, möchte sich auf eine Stelle im nicht zugehörigen Unternehmen, Alpine Ski House bewerben. In diesem Fall wird die Anmeldung fehlschlagen, wenn der Mitarbeiter versucht, seine Azure AD-Anmeldeinformationen von Contoso Ltd zu verwenden. 

Kandidaten müssen sich mithilfe von Azure AD anmelden, wenn die Stelle, die sie anzeigen oder für die sie sich bewerben nur als intern aufgeführt ist.

## <a name="create-and-maintain-a-profile"></a>Erstellen und Verwalten eines Profils

Nachdem sich Kandidaten in der Website mit Stellenangeboten angemeldet haben, können sie in der Navigationsleiste oben auf der Seite **Eigenes Profil** auswählen, um ihr Profil zu erstellen und zu verwalten.
Das Profil enthält persönliche Informationen, Informationen zur Berufserfahrung, Ausbildungsdetails, Dokumente, Links und Informationen zu Qualifikationen. Nachdem ein Profil erstellt wurde, kann es zur Bewerbung auf Stellen verwendet werden, an denen der Kandidat interessiert ist. Profile helfen Attract außerdem dabei, Kandidaten die richtigen Stellen zu empfehlen.

> [!NOTE]
> Wenn ein Kandidat eine E-Mail-Kennung verwendet, um sich über einen der Authentifizierungsanbieter in anzumelden, die oben aufgeführt sind, wird diese E-Mail-Kennung standardmäßig an die Kontakte-E-Mail-Jennung, weitergeleitet, die dem Profil zugeordnet ist. Allerdings kann die letztere jederzeit geändert werden und ist völlig von der vorherigen unabhängig. Attract wird immer die Kontakt-E-Mail-Kennung verwenden, um die jede E-Mail-Kommunikation Ihrem Profil zuzuordnen.

## <a name="find-the-right-job"></a>Die richtige Stelle finden

Auf der Stellenlistenseite können Kandidaten nach einer bestimmten Stelle suchen, indem sie Suchbegriffe eingeben. Die Suchfunktion sucht nach den Suchbegriffen in Stellentiteln und Stellenbeschreibungen und zeigt relevante Stellen als Ergebnis an. Kandidaten können die Ergebnisse jederzeit basierend auf dem Arbeitsort oder der Stellenfunktion filtern.

Kandidaten können auf der Website mit Stellenangeboten zudem einen Reihe empfohlener Stellen anzeigen. Die Stellen, die einem Kandidaten empfohlen werden, basierend auf den vergangenen Bewerbungen, dem Profil und den Lebensläufen des Kandidaten.

> [!NOTE] 
> Stellenempfehlungen werden nur angezeigt, wenn mindestens 10 Stellen auf der Website mit Stellenangeboten veröffentlicht wurden und der Kandidat ein Profil vollständig ausgefüllt hat.

Interne Kandidaten können außerdem sehen, wer der als zukünftige Vorgesetzte und/oder der Personalbeschaffungsmitarbeiter für eine Stelle ist, falls sie sich mit diesen Mitglieder des Einstellungsteams in Verbindung setzen möchten. Externe Kandidaten können jedoch keine Mitglieder des Einstellungsteams für irgendeine Stelle anzeigen.

## <a name="contact-the-hiring-team"></a>Das Einstellungsteam kontaktieren
Nur interne Kandidaten können sich mit dem Einstellungsteam in Verbindung setzen. Diese Einschränkung gilt für alle Stellen, unabhängig davon, ob sie nur intern oder öffentlich ausgeschrieben wurden.

Es empfiehlt sich für Kandidaten, sich an das Einstellungsteam zu wenden, um Ihr Interesse an eine Stelle auszudrücken, die gebucht wurde, oder um mehr über sie zu erfahren. Sie können sich an jedes beliebige Mitglied des Einstellungsteams wenden, die aufgeführt sind (Einstellungsmanager oder Personalbeschaffungsmitarbeiter). Optional können sie auch einen Lebenslauf an ihre Nachricht anhängen, oder sie können einen vorhandenen Lebenslauf auswählen, den sie zuvor als Teil ihres Profils hochgeladen haben.

Nachdem ein interner Kandidat die Mitglieder des Einstellungsteams für die Kontaktaufnahme auswählt, sendet Attract eine E-Mail an diese Personen im Auftrag des Kandidaten. Gleichzeitig wird das Profil des Kandidaten der Phase **Interessent** hinzugefügt, wenn diese Phase für die Stelle verfügbar ist. Unter der Phase **Interessent** können Personalbeschaffungsmitarbeiter oder Einstellungsmanager die Kandidaten anzeigen, die sich mit ihnen in Verbindung gesetzt haben. Sie können auch die Kandidatenprofile überprüfen und mögliche Kandidaten einladen, sich zu bewerben.

Kandidaten können sich für eine Stelle bewerben, bezüglich der sie sich bereits an Einstellungsteammitglieder gewendet haben. Nachdem sie sich bewerben, können Kandidaten sich nicht mehr über die Karrierewebsite mit dem Einstellungsteam in Verbindung setzen.

## <a name="apply-for-jobs"></a>Bewerben um Stellen

Nachdem Kandidaten die richtige Stelle gefunden haben, können sie sich bewerben, indem sie die Schaltfläche **Bewerben** auf der Seite **Stellendetails** verwenden. An diesem Punkt können Kandidaten entweder ein neues Profil erstellen oder die vorhandenen Informationen in ihrem Profil überprüfen.
Kandidaten können bei Bedarf auch einen Lebenslauf hochladen und die Stellenbewerbung dann senden.

### <a name="enable-applying-for-jobs-with-linkedin-profiles"></a>Bewerbung auf Stellen mit LinkedIn-Profilen aktivieren

Sie können es für Kandidaten einfach machen, sich auf Ihre Positionen zu bewerben, indem Sie Attract so konfigurieren, dass sie sich durch LinkedIn bewerben können.

> [!NOTE] 
> Sie müssen mindestens eine Lizenz für Personalbeschaffungsmitarbeiter von LinkedIn haben, bevor Sie es Kandidaten ermöglichen können, sich mit LinkedIn zu bewerben.

1. Bei Attract als Administrator anmelden.
2. Wählen Sie die Schaltfläche **Einstellungen** (das Rad-Symbol) in der rechten oberen Ecke der Seite aus, und wählen Sie dann **Administratorcenter**.
3. Wählen Sie die Registerkarte **LinkedIn-Integration** aus und verbinden Sie sich mit einem LinkedIn Recruiter-Konto.
4. Im Abschnitt **LinkedIn Recruiter System Connect Integration** wählen Sie **Aktiviert** für die Einstellung **Mit LinkedIn bewerben** aus.

Nachdem Sie die Einstellung aktiviert haben, können Kandidaten sich unter Verwendung ihrer vorhandenen LinkedIn-Profildaten bewerben. Wenn Kandidaten sich bewerben, indem sie die Schaltfläche **Mit LinkedIn bewerben** auswählen, werden sie dazu aufgefordert, sich bei LinkedIn zu authentifizieren, wenn sie nicht bereits angemeldet sind. Nachdem sie sich authentifiziert haben, ersetzt ihr LinkedIn-Profil alle vorhandenen Profildaten, die auf der Bewerbungsseite angezeigt werden. Kandidaten können die Informationen bei Bedarf bearbeiten und die Bewerbung dann senden. Wenn ein Kandidat von der Seite weg navigiert, ohne sich für die Stelle zu bewerben, werden dessen Profildaten in Attact nicht aktualisiert.

## <a name="check-application-status"></a>Den Bewerbungsstatus prüfen

Nachdem sich Kandidaten auf mindestens eine Stelle beworben haben, können Sie in der Navigationsleiste oben auf der Seite **Bewerben** auswählen, um ihre offenen und geschlossenen Bewerbungen anzuzeigen. Wenn Kandidaten eine ihrer Bewerbungen öffnen, sehen sie die aktuelle Phase sowie alle ausstehenden Aktionselemente, die sie durchführen müssen. Wenn ein Kandidat beispielsweise potenzielle Datumsangaben für ein persönliches Bewerbungsgespräch bereitstellen muss, zeigt die Seite die verfügbaren Optionen an.

## <a name="internal-jobs"></a>Interne Stellen

Derzeit werden Stellen, die als intern markiert und auf der Attract-Website mit Stellenangeboten veröffentlicht werden, dort nicht angezeigt. Sie sind nur direkt über die **Bewerben**-URL verfügbar, die aus der Attract-Anwendung kopiert werden kann.
