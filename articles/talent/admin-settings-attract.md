---
title: Unternehmensinformationen konfigurieren in Attract
description: 'In diesem Thema wird erläutert, wie Unternehmensinformationen und Branding für Microsoft Dynamics 365 Talent: Attract konfiguriert werden.'
author: andreabichsel
manager: AnnBe
ms.date: 12/07/2018
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
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: db3ec965f3a52810d5f310697b9ed830c3abe681
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461338"
---
# <a name="configure-company-information-in-attract"></a>Unternehmensinformationen konfigurieren in Attract

[!include [banner](includes/banner.md)]

Das Administratorcenter in Microsoft Dynamics 365 Talent: Attract enthält Konfigurationseinstellungen, Integrationsoptionen und Einrichtungsoptionen für die Attract-Anwendung.

## <a name="company-information"></a>Unternehmensinformationen

Geben Sie einen Anzeigenamen für das Unternehmen ein, und fügen Sie das Firmenlogo hinzufügen. Der Anzeigename und das Logo können dann für Stellenveröffentlichungen und während der Onboarding-Erfahrung verwendet werden.

## <a name="linkedin-integration"></a>LinkedIn-Integration

Einrichten der Integration in LinkedIn Recruiter System Connect(RSC). Nachdem Sie eine LinkedIn-Verbindung hergestellt haben, indem Sie Ihre LinkedIn-Anmeldeinformationen verwenden, können Sie das LinkedIn-Profil, Bewerbungen, Feedback zum Gespräch und Hinweise des Einstellungsteams synchronisieren. Eine vollständige LinkedIn Recruiter-Lizenz ist erforderlich. Weitere Informationen zu LinkedIn Recruiter finden Sie unter [Recruiter System Connect (RSC) – FAQ](https://www.linkedin.com/help/recruiter/answer/90483).

## <a name="user-permissions"></a>Benutzerberechtigungen

Weisen Sie Benutzern in Ihrem Unternehmen Rollen zu. Folgende Rollen sind verfügbar: **Administrator**, **Personalbeschaffungsmitarbeiter**, **Zukünftiger Vorgesetzter** und **Schreibgeschützt**. Weitere Informationen zu Benutzerberechtigungen finden Sie unter [Sicherheit und Rollenverwaltung in Attract](./security-attract.md).

## <a name="feature-management"></a>Funktionsverwaltung

Wenn neue Funktionen hinzugefügt werden, werden Sie möglicherweise in einer öffentlichen Vorschau veröffentlicht. Öffentliche Vorschaufunktionen entsprechen nicht allen Service-Bedingungen. Wenn Sie sie empfangen, erklären Sie sich einverstanden, Ihre Daten für externe Systeme freizugeben. Sie stellen ggf. fest, dass Ihr Unternehmen nicht alle neuen Funktionen benötigt, die veröffentlicht werden. Sie können die Vorschaufunktionen je nach den Anforderungen Ihrer Organisation ein- und ausstellen.

## <a name="template-management"></a>Vorlagenverwaltung

Eine Prozessvorlage enthält alle Aktivitäten, die im Rahmen des Einrichtungsprozesses für einen Stelle einbezogen werden sollen. Ihre Organisation kann entweder erlauben, dass alle Teammitglieder oder nur Administratoren Einstellungsprozessvorlagen erstellen. Um zuzulassen, dass Teammitglieder eigene Einstellungsprozessvorlagen erstellen, schalten Sie die Vorlagenverwaltungsfunktionen ein. Weitere Informationen zu Prozessvorlagen finden Sie unter [Erstellen einer Prozessvorlage in Attract](./process-templates-attract.md)

## <a name="email-template-settings"></a>E-Mail-Vorlageneinstellungen

Organisationen können für verschiedene Szenarien E-Mail-Vorlagen erstellen. Sie können auswählen, dass das Kopfzeilenbild in den E-Mail-Vorlagen einbezogen wird. Die ausgewählte Kopfzeile erscheint dann in allen E-Mail-Vorlagen. In der Vorlagenfußzeile können Sie einen Link zu den Datenschutzbestimmungen und den Nutzungsbedingungen Ihrer Organisation bezüglich Kommunikation hinzufügen. Weitere Informationen finden Sie unter [E-Mail-Vorlagen](./email-templates.md).

## <a name="offer-process"></a>Angebotsprozess

Sie können den Genehmigungsprozess für Stellenangebote konfigurieren. Beispielsweise können Sie angeben, ob ein Angebot genehmigt werden muss, bevor es an einen Kandidaten gesendet wird. Sie können auch verlangen, dass Genehmiger einen Kommentar bezüglich Ihrer Entscheidung zum Angebot hinterlassen.

Zwei Genehmigungs-Workflows sind verfügbar: **Parallel** und **Sequenziell**.

- **Parallel** – Genehmigungen werden gleichzeitig an alle Genehmiger gesendet.
- **Sequentiell** – Genehmigungen werden in einer bestimmten Reihenfolge an die Genehmiger gesendet.

Sie können auch Optionen in Zusammenhang mit der Kandidatenerfahrung konfigurieren. Beispielsweise können Sie mit einer Option angeben, ob Kandidaten ein Angebot ohne zusätzliche Diskussion ablehnen können. Wenn Sie die Option **Zulassen von Kandidaten, ein Angebot ohne zusätzliche Diskussion abzulehnen** auf **Nein** festlegen, steht den Kandidaten die Schaltfläche **Angebot ablehnen** zur Verfügung. Wenn Sie die Option auf **Ja** festlegen, können Kandidaten das Angebot ablehnen, indem sie einen Grund und dann **Angebot ablehnen** auswählen.

Sie können auch ein Ablaufdatum für Angebote festlegen und durchsetzen. Wenn die Option **Ein Ablaufdatum für alle Angebote erforderlich machen** auf **Ja** festlegen, laufen Angebote nach der angegebenen Anzahl von Stunden oder Tagen ab.

Weitere Informationen zur Angebotsverwaltung finden Sie unter [Einrichten der Angebotsverwaltung](./offer-setup.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]