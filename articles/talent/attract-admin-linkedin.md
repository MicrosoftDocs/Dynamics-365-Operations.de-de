---
title: 'Einrichten der Integration mit LinkedIn für AMicrosoft Dynamics 365 Talent: Attract'
description: 'In diesem Thema wird erläutert, wie LinkedIn-Integration für Microsoft Dynamics 365 Talent: Attract konfiguriert, sodass Sie einfach Stellen in LinkedIn von Attract veröffentlichen könne, sodass Ihre Einstellungsmanager Ihre Informationen mit dem LinkedIn-Profil eines Kandidaten synchronisieren können.'
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 6b86cafdf364f2de051f3d8ceab7413c2c13c3a5
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009968"
---
# <a name="set-up-linkedin-integration"></a>LinkedIn-Integration einrichten

[!include[banner](../includes/banner.md)]

Helfen Sie Einstellungsmanagern und Vorgesetzten, die besten Talente anzuziehen, indem Sie LinkedIn-Integration mit Microsoft Dynamics 365 Talent: Attract  konfigurieren. Mit Attract können Sie Stellen direkt in LinkedIn veröffentlichen, dem größten professionellen Online Netzwerk,

Stellen, die Sie in LinkedIn über Attract veröffentlichen, sind eingeschränkte Listen und werden ohne Zusatzkosten für Ihr Unternehmen bereitgestellt. Diese Listen sind nur über die LinkedIn-Software-Partner wie Attract verfügbar. Sie werden nicht im Bereich **Karrieren** auf Ihrer LinkedIn-Seite des Unternehmens angezeigt, da hier nur kostenpflichtige Veröffentlichungen angezeigt werden. Sie werden aber angezeigt, wenn mögliche Kandidaten alle verfügbaren Stellen ansehen. Begrenzte Listen werden auch in LinkedIn-Jobsuchen angezeigt.

Attract stellt zwei Möglichkeiten für die Integration mit LinkedIn bereit, damit Sie Kandidaten von den beliebtesten Karriereseiten finden können.

- Veröffentlichen von Stellenausschreibungen von Attract auf LinkedIn.
- Suchen von Kandidaten von LinkedIn mit Attract.

Sie können die beiden Optionen auf der Registerkarte **LinkedIn-Integration** im Administratorencenter konfigurieren. um das Administratorcenter zu öffnen, gehen Sie zu <https://attract.talent.dynamics.com/adminsettings>.

> [!NOTE]
> Um die LinkedIn Recruiter Integration mit Attract zu verwenden, benötigen Sie das [Umfassende Einstellungs-Add-On](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) und [LinkedIn Recruiter Lizenzen](https://business.linkedin.com/talent-solutions/cx/17/08/recruiter-demo-fs2-k18). Weitere Informationen finden Sie unter[Welche Version von Attract?](./attract-comprehensive-hiring.md).

Wenn Sie Schwierigkeiten haben, Stellen in LinkedIn zu veröffentlihcen, gehen Sie zu [Probleme bei der Integration mit LinkedIn](./attract-troubleshoot-linkedin.md).

Informationen zu anderen Methoden, Stellen in LinkedIn zu veröffentlichen, finden Sie unter[LinkedIn FAQ](./attract-linkedin-faq.md).

## <a name="configure-job-posting-to-linkedin"></a>Konfigurieren Sie Stellenausschreibungen in LinkedIn

Bevor Sie Stellen veröffentlichen können von Attract nach LinkedIn, benötigen Sie eine [LinkedIn-Unternehmenskennung](https://aka.ms/findID) Ihre LinkedIn-Unternehmenskennung ist eine Zeichenfolge aus Nummern, mit der Ihr Unternehmen innerhalb von LinkedIn eindeutig identifiziert wird. Weitere Informationen finden Sie unter [Ihre LinkedIn-Unternehmenskennung der LinkedIn-Stellenbörse zuordnen - häufig gestellte Fragen](https://aka.ms/findID).

Attract sendet einen Feed Ihrer Stellenausschreibungen an LinkedIn und LinkedIn prüft ungefähr einmal pro Tag den Feed. Es kann bis zu 48 Stunden in Anspruch nehmen, bis die Stellen auf der Site angezeigt werden.

Die Stellen, die in LinkedIn veröffentlicht werden, werden auf der laufenden LinkedIn-Website angezeigt. Es gibt keine Testumgebung in LinkedIn für das Veröffentlichen von Stellen. Daher sollten Sie sicherstellen, dass Sie keine Testjobs versehentlich veröffentlichen. 

1. Wählen Sie im **Setup**-Menü (das Zahnradsymbol) in der oberen rechten Ecke **Admin Center**. Alternativ gehen Sie zu <https://attract.talent.dynamics.com/adminsettings>.
2. Wählen Sie die Registerkarte **LinkedIn Integration**.
3. Geben Sie unter **Unternehmensname** den Namen des Unternehmens ein, und unter **Unternehmenskennung** die LinkedIn-Unternehmenskennung ein. Überprüfen Sie, ob der Unternehmensname dem Namen entspricht, der auf der LinkedIn-Seite Ihres Unternehmens angezeigt wird. Weitere Informationen zur LinkedIn Unternehmungskennungen, finden Sie unter [Ihre LinkedIn-Unternehmenskennung der LinkedIn-Stellenbörse zuordnen - häufig gestellte Fragen](https://www.linkedin.com/help/linkedin/answer/98972).

    Wenn Sie alle Informationen für die Organisation ändern müssen, gehen Sie zu [Adresse, technischen Kontakt und mehr in Ihrer Organisation ändern](https://docs.microsoft.com/office365/admin/manage/change-address-contact-and-more). Wenn Sie nach wie vor Probleme haben, wenden Sie sich an [LinkedIn-Support](https://www.linkedin.com/help/linkedin)

4. Wählen Sie **Speichern**.

## <a name="set-up-linkedin-recruiter-with-attract"></a>Einrichten von LinkedIn Recruiter mit Attract 

Um Einstellungsmanagern zu ermöglichen, Stellen über LinkedIn Recruiter zu platzieren, müssen Sie die Integrationskonfiguration mit LinkedIn Recruiter in Attract vornehmen. Zum Abschluss des Konfigurationsvorgangs müssen Sie mit dem Benutzer zusammenarbeiten, der ein Administrator in Ihrem OrganisationsLinkedIn Recruiter-Vertrag ist.

1. Wählen Sie im **Setup**-Menü (das Zahnradsymbol) in der oberen rechten Ecke **Admin Center**. Alternativ gehen Sie zu <https://attract.talent.dynamics.com/adminsettings>.
2. Wählen Sie die Registerkarte **LinkedIn Integration**.

    [![Attract-Administratoransicht, um die LinkedIn Recruiter-Integration zu starten](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3. Wählen Sie **Verbinden**, um die Einstellungen zu starten. Sie werden durch den LinkedIn-Anmeldungsprozess geführt.
4. Wenn Sie über mehrere LinkedIn-Vertragslizenzen verfügen, wählen Sie den Vertrag aus, den Sie mit dem Attract-System verbinden möchten. Wenn Sie über nur eine LinkedIn-Vertragslizenz verfügen, ist dieser Schritt nicht erforderlich.
5. Klicken Sie unter **Recruiter System Connect (RSC)** auf **Anfordern**.

    [![Attract-Administratoransicht, um die LinkedIn Recruiter-Integration anzufordern](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)

6. Die Einstellung **Recruiter System Connect (RSC)** Einstellung sollte jetzt als **Partner bereit** angezeigt werden. Wenn **Partner benachrichtigen** auf dieser Seite angezeigt wird, wählen Sie **Partner benachrichtigen** und aktualisieren Sie anschließend die Seite. Die Einstellung sollte jetzt als **Partner bereit** angezeigt werden.

    [![Attract-Administratoransicht, um die Attract-Seite der abgeschlossenen mit Anforderungen anzugeben](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)

7. Um den nächsten Schritt auszuführen, müssen Sie über das Administratorrecht für Ihren LinkedIn Recruiter-Vertrag verfügen.

    1. Melden Sie sich bei LinkedIn an, indem Sie das Administratorkonto verwenden, und wählen Sie dann **LinkedIn Recruiter** in der oberen rechten Ecke aus. 
    2. Klicken Sie im Menü **Mehr** am oberen Rand des Bildschirms an, wählen Sie **Administratoreinstellungen** auf der Registerkarte **ATS**.
    3. Um den Export per Mausklick für nur einen Vertrag zu ermöglichen, aktivieren Sie **Vertragsebenenzugang (für jeden Platz in diesem Vertrag**. Um dies für das gesamte Unternehmen zu ändern, aktivieren Sie **Unternehmensebenezugriff (für jeden Vertrag für jeden im Unternehmen** ein.

    [![Einschalten der Attract-Integration aus der LinkedIn Recruiter-Administratoransicht](./media/EnableRSC.png)](./media/EnableRSC.png)

8. Im Attract Administratorencenter wählen Sie  die Registerkarte**LinkedIn-Integration** aus. Die Einstellung **Einstellungsmanager sollte nun** als **Aktiviert** angezeigt werden.

    [![LinkedIn Recruiter-Integration abgeschlossen](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)

## <a name="set-up-apply-with-linkedin-in-attract"></a>LinkedIn in Attract einrichten

Sie können den Kandidaten ermöglichen, sich auf Ihre Stellen direkt über Ihr LinkedIn-Profil zu bewerben. Weitere Informationen zu LinkedIn finden sie unter [Die Leistung von  LinkedIn: mit LinkedIn bewerben](https://blog.linkedin.com/2011/07/24/apply-with-linkedin).

Diese Funktion befindet sich derzeit in der Vorschau. Bevor Sie die folgenden Schritte ausführen, überprüfen Sie, ob mit LinkedIn anwenden aktiviert ist. Mehr Informationen zum Aktivieren von Vorschaufunktionen, finden Sie unter [Auf Vorschaufunktionen im Talent zugreifen](./access-preview-feature.md).

1. Wählen Sie im **Setup**-Menü (das Zahnradsymbol) in der oberen rechten Ecke **Admin Center**. Alternativ gehen Sie zu <https://attract.talent.dynamics.com/adminsettings>.
2. Wählen Sie die Registerkarte **LinkedIn Integration**.

    [![Attract-Administratoransicht, um die LinkedIn Recruiter-Integration zu starten](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3. Neben **Mit LinkedIn anwenden** wählen Sie **Verbinden**, um die Einstellungen zu starten. Sie werden durch den LinkedIn-Anmeldungsprozess geführt.

## <a name="see-also"></a>Siehe auch

[LinkedIn-FAQ](./attract-linkedin-faq.md)

[Buchen von Aufträgen auf externen Websites von Attract](./posting-jobs-external.md)

[Kandidaten suchen mithilfe von LinkedIn Recruiter](./attract-linkedin-recruiter.md)

[Stelle erstellen](./creating-jobs-attract.md)

[Probleme mit der Integration mit LinkedIn](./attract-troubleshoot-linkedin.md)
