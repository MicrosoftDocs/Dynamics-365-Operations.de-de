---
title: Karrierestandortsfunktionen in Attract
description: "Dieser Artikel gibt eine Übersicht über die Funktionen der Karriereseite für Kandidaten in Microsoft Dynamics 365 for Talent - Attract. Es wird auch beschrieben, wie diese Funktionen eingerichtet werden."
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 452e3e92ea32ab5f1e3720ab81ff2f7ea18b2a06
ms.contentlocale: de-de
ms.lasthandoff: 10/22/2018

---
# <a name="career-site-functionality-in-attract"></a>Karrierestandortsfunktionen in Attract

[!include [banner](includes/banner.md)]

Dieser Artikel gibt eine Übersicht über die Funktionen der Karriereseite für Kandidaten in Microsoft Dynamics 365 for Talent: Attract. Es wird auch beschrieben, wie diese Funktionen eingerichtet werden.

## <a name="overview"></a>Übersicht

Attract eine Karriereseite für jede Umgebung in einem Mandanten bietet. Wenn beispielsweise eine Organisation über eine Entwicklungsumgebung und einer Testumgebung verfügt, wird eine Karriereseite für die Entwicklungsumgebung und eine weitere für die der Testumgebung bereitgestellt. Jede Karriereseite ist **vollständig isoliert** und verfügt über einen eigenen Authentifizierungsmechanismus. Stellen- und Kandidatenprofile werden zwischen Karriereseiten nicht freigegeben.

Standardmäßig ist die Karriereseite öffentlich. Daher können Kandidaten alle Stellen anzeigen, die als extern markiert werden, ohne sich anmelden zu müssen. Allerdings ist für alle weiteren Aktivitäten erforderlich, dass die Kandidaten sich anmelden.

## <a name="career-site-management"></a>Verwaltung der Website mit Stellenangeboten

Die folgenden Elemente einer Karriereseite werden durch Einstellungen gesteuert:

- **Organisationsname:** Der Organisationsname wird auf der Navigationsleiste oben auf der Karriereseite angezeigt. Wenn sie den Organisationsnamen auswählen, gelangen Kandidaten auf eine Seite, auf der alle offenen Stellen aufgeführt werden.
- **Organisationslogo:** Ein Bild des Organisationslogos wird oben links der Karriereseite angezeigt. Wenn sie das Logobild auswählen, gelangen Kandidaten auf eine Seite, auf der alle offenen Stellen aufgeführt werden.

Um die Werte für den Organisationsnamen und das Logo festzulegen, melden Sie sich als Administrator in Attract an, wählen Sie im Menü **Einstellungen** (Zahnradsymbol) die Option **Administratorcenter** und anschließend die Registerkarte **Unternehmensdaten** aus.

> [!NOTE]
> Das Logobild, das auf der Karriereseite angezeigt wird, weist eine feste Höhe von 20 Pixeln (px) auf. Das Bild, das Sie im Administratorcenter hinzufügen, wird passend skaliert. Daher kann sich die Breite abhängig vom Bild ändern.

## <a name="career-site-url"></a>URL der Karriereseite

Wenn Sie zum ersten Mal [eine externe Stelle veröffentlichen](./Creating-jobs-Attract.md#postings) können Sie den **Bewerben**-Link aus der Attract-Anwendung kopieren. Die URL für diesen Link hat folgendes Format: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`

Die URL der Karriereseite ist eine Teilzeichenfolge der **Bewerben**-URL. Sie besteht aus allem bis zum Unternehmensnamen. Daher lautet die URL der Karriereseite der vorherigen **Bewerben**-URL`https://jobs.talent.dynamics.com/jobs/<company_name>/`

## <a name="authentication-options"></a>Authentifizierungsoptionen

Kandidaten haben folgende Anmeldungsoptionen bei einer Attract-Karriereseite:

- Persönliches Konto:

    - LinkedIn
    - Microsoft
    - Google
    - Facebook

- Geschäfts- oder Schulkonto:

    - Microsoft Azure Active Directory (Azure AD)

Azure AD-Anmeldung ist nur für interne Kandidaten vorgesehen. Daher funktioniert sie nur bei internen Kandidaten, die ihre Azure AD-Unternehmensanmeldeinformationen verwenden. Ein Kandidat z. B., der derzeit ein Mitarbeiter von Contoso Ltd ist, möchte sich auf eine Stelle im nicht zugehörigen Unternehmen, Alpine Ski House bewerben. In diesem Fall wird die Anmeldung fehlschlagen, wenn der Mitarbeiter versucht, seine Azure AD-Anmeldeinformationen von Contoso Ltd zu verwenden.

## <a name="create-and-maintain-a-profile"></a>Erstellen und Verwalten eines Profils

Nachdem sich Kandidaten in der Karriereseite angemeldet haben, können sie in der Navigationsleiste oben auf der Seite **Eigenes Profil** auswählen, um ihr Profil zu erstellen und zu verwalten. Das Profil enthält persönliche Informationen, Informationen zur Berufserfahrung, Ausbildungsdetails, Dokumente, Links und Informationen zu Qualifikationen. Nachdem ein Profil erstellt wurde, kann es zur Bewerbung auf Stellen verwendet werden, an denen der Kandidat interessiert ist. Profile helfen Attract außerdem dabei, Kandidaten die richtigen Stellen zu empfehlen.

## <a name="find-the-right-job"></a>Die richtige Stelle finden

Auf der Stellenlistenseite können Kandidaten nach einer bestimmten Stelle suchen, indem sie Suchbegriffe eingeben. Die Suchfunktion sucht nach den Suchbegriffen in Stellentiteln und Stellenbeschreibungen und zeigt relevante Stellen als Ergebnis an. Kandidaten können die Ergebnisse jederzeit basierend auf dem Arbeitsort oder der Stellenfunktion filtern.

Kandidaten können auf der Karriereseite zudem einen Reihe empfohlener Stellen anzeigen. Die Stellen, die einem Kandidaten empfohlen werden, basierend auf den vergangenen Bewerbungen, dem Profil und den Lebensläufen des Kandidaten.

> [!NOTE]
> Stellenempfehlungen werden nur angezeigt, wenn mindestens 10 Stellen auf der Karriereseite veröffentlicht wurden und der Kandidat sein Profil vollständig ausgefüllt hat.

## <a name="apply-for-jobs"></a>Bewerben um Stellen

Nachdem Kandidaten die richtige Stelle gefunden haben, können sie sich bewerben, indem sie die Schaltfläche **Bewerben** auf der Stellendetailseite verwenden. An diesem Punkt können Kandidaten entweder ein nagelneues Profil erstellen oder die vorhandenen Informationen in ihrem Profil überprüfen. Kandidaten können bei Bedarf auch einen Lebenslauf hochladen und die Stellenbewerbung dann senden.

## <a name="check-application-status"></a>Den Bewerbungsstatus prüfen

Nachdem sich Kandidaten auf mindestens eine Stelle beworben haben, können Sie in der Navigationsleiste oben auf der Seite **Bewerben** auswählen, um ihre offenen und geschlossenen Bewerbungen anzuzeigen. Wenn Kandidaten eine ihrer Bewerbungen öffnen, sehen sie die aktuelle Phase sowie alle ausstehenden Aktionselemente, die sie durchführen müssen. Wenn ein Kandidat beispielsweise potenzielle Datumsangaben für ein persönliches Bewerbungsgespräch bereitstellen muss, zeigt die Seite seine Optionen an.

## <a name="internal-jobs"></a>Interne Stellen

Derzeit werden Stellen, die als intern markiert und auf der Attract-Karriereseite veröffentlicht werden, dort nicht angezeigt. Sie sind nur direkt über die **Bewerben**-URL verfügbar, die aus der Attract-Anwendung kopiert werden kann.

