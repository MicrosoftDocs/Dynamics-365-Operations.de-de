---
title: Auf Vorschaufunktionen in Microsoft Dynamics 365 Talent zugreifen
description: In diesem Thema wird beschrieben, wie ein Administrator die Vorschaufunktionen in Microsoft Dynamics 365 Talent aktivieren kann, und es werden die Funktionen aufgeführt, die derzeit für Vorschau aktiviert sind.
author: tracykeya
manager: AnnBe
ms.date: 05/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: trkeya
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2019 update
ms.openlocfilehash: 0f9a83aeea3942d3c56d32956f79490c91565e9e
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551598"
---
# <a name="access-preview-features-in-microsoft-dynamics-365-talent"></a>Auf Vorschaufunktionen in Microsoft Dynamics 365 Talent zugreifen

[!include[banner](../includes/banner.md)]

Im Rahmen unseres kontinuierlichen Rollouts von Human Capital Management (HCM) Funktionen für Microsoft Dynamics 365 Talent, wollen wir unseren Kunden so schnell wie möglich neue Funktionen zur Verfügung stellen. Administratoren können Vorschaufunktionen in ihrer Umgebung sehen und nutzen. Diese Funktionen sind fast fertig für die allgemeine Verfügbarkeit und wurden ausgiebig getestet. Wir sind nur auf der Suche nach einer letzten Runde von Kunden-Feedback und Validierung, bevor wir sie zur allgemeinen Verfügbarkeit veröffentlichen.

In diesem Thema wird beschrieben, wie Sie die Vorschaufunktionen aktivieren können, und es werden die Funktionen aufgeführt, die derzeit für Vorschau aktiviert sind. Diese Liste wird aktualisiert, wenn die Funktionen zur allgemeinen Verfügbarkeit freigegeben werden und wenn neue Funktionen zur Vorschau freigegeben werden. Es erfolgt keine Benachrichtigung, wenn neue Funktionen zur Vorschau freigegeben werden. Die Benutzer werden nur beginnen, die Funktionen zu sehen. Weitere Informationen über neue Funktionen im Talent, finden Sie unter [Neuheiten oder Änderungen in Dynamics 365 Talent](./whats-new.md) und [Dynamics 365 und Power Platform-Versionshinweise](https://docs.microsoft.com/business-applications-release-notes).

## <a name="enable-or-disable-preview-features"></a>Vorschaufunktionen aktivieren oder deaktivieren

Um auf Vorschaufunktionen zugreifen zu können, müssen Sie sie in Ihrer Umgebung zunächst aktivieren. Aktivieren oder Deaktivieren von Vorschaufunktionen ist umgebungsspezifisch.

> [!IMPORTANT]
> Durch das Aktivieren der Einstellung **Vorschaufunktionen** aktivieren Sie Vorschaufunktionen für alle Benutzer in Ihrer Organisation, die sich in dieser Umgebung befinden. Wenn Sie die Einstellung deaktivieren, deaktivieren Sie die Vorschaufunktionen und machen sie für Ihre Benutzer unzugänglich. Die Vorschaufunktionen werden in Talent nur eingeschränkt unterstützt. Sie verwenden möglicherweise weniger Datenschutz- und Sicherheitsmaßnahmen und sind nicht in der Talent-Service-Level-Vereinbarung (SLA) enthalten. Sie sollten keine Vorschaufunktionen verwenden, um personenbezogene Daten (d. h. Informationen, die Sie identifizieren könnten) oder andere Daten zu verarbeiten, die gesetzlichen oder behördlichen Anforderungen unterliegen.

### <a name="attract"></a>Attract

1. Melden Sie sich bei Microsoft Dynamics 365 Talent: Attract an.
2. Wählen Sie im **Setup**-Menü (das Zahnradsymbol) in der oberen rechten Ecke **Admin Center**.
3. Wählen Sie auf der Registerkarte **Funktion-Verwaltung** die Option neben **Vorschau-Funktion**, so dass sie blau wird und anzeigt **Ein**.

    ![Vorschaufunktionen aktivieren in Attract](./media/attract-enable-preview-features.png)

4. Dient zum Auswählen oder stornieren von einzelnen Vorschaufunktionen. Wenn Sie nichts tun, werden alle verfügbaren Vorschaufunktionen aktiviert.
5. Aktualisieren Sie Ihren Browser, um die neuen Funktionen zu sehen. Alle Benutzer, die bereits angemeldet sind, sehen die Funktionen beim nächsten Mal, wenn sie sich anmelden, oder sie können ihren Browser aktualisieren, um die Funktionen sofort zu sehen.

> [!NOTE]
> Einige Vorschaufunktionen erfordern ggf. zusätzliche Konfiguration. Folgen Sie den Links neben der Vorschaufunktion, um die Einstellungen für diese durchzuführen.

### <a name="core-hr"></a>Zentrale Personalverwaltung

1. Melden Sie sich bei Talent an.
2. Wählen Sie **Systemverwaltung** und anschließend die Registerkarte **Links** aus.
3. Auf der Seite **Systemverwaltung** unter **Einstellungen**, wählen Sie **Systemparameter** aus.
4. Auf der Seite **Systemparameter** wählen Sie die Registerkarte **Vorschaufunktionen** aus.
5. Hier können Sie die Option **Aktivieren Sie Seitenansichtsmodus für alle Benutzer** auf **Ja** festlegen, um die  Vorschaufunktionen bereitzustellen.

    ![Vorschaufunktionen in Core HR aktivieren](./media/corehr-enable-preview-features.png)

> [!NOTE]
> Um die Vorschaufunkltion zu deaktivieren, führen Sie die gleichen Schritte aus, aber legen die Option **Aktivieren der Vorschaufunkltion für alle Benutzer** auf **nein** fest. Wenn Sie die Vorschaufunktionen deaktivieren, werden sie für Ihre Benutzer unzugänglich, und es können Fehler in Prozessen auftreten, die mit den Funktionen verknüpft sind.

### <a name="onboard"></a>Aufnehmen

Keine Vorschaufunktionen sind derzeit für Microsoft Dynamics 365 Talent: Onboard verfügbar.

## <a name="features-that-are-currently-in-preview"></a>Funktionen, die sich derzeit in der Vorschau befinden

### <a name="attract"></a>Attract

- [Kandidatenempfehlung](./intelligent-recommendations.md#candidate-recommendations) - Wenn es mehr als zehn Kandidaten oder Interessenten gibt, die Zusammenfassungen oder vollständige Profile haben, erscheinen die Kandidaten oder Interessenten, die den Anforderungen der Stelle am besten entsprechen, oben im Abschnitt **Zu berücksichtigende Bewerber** auf der Stellenseite.
- [Stellenempfehlung](./intelligent-recommendations.md#job-recommendations) – Wenn mehr als zehn Stellen auf der Karrieresite veröffentlicht sind, stellt Attract Stellenempfehlungen für Interessenten bereit.
- [Broadbean-Integration](./posting-jobs-external.md#post-jobs-to-broadbean) – Sie können Stellen von Attract in Broadbean, einer externen Stellenveröffentlichungssite, veröffentlichen. Nachdem Sie diese Vorschaufunktion aktiviert haben, müssen Sie die Einrichtung abschließen, indem Sie Ihren Broadbean Benutzernamen, Client-ID und Verschlüsselungstoken eingeben.
- [Analytis](./analytic-reports.md) -  Im Analytcs Hub können Einstellungsteams Schlüsselindikatoren für eine einzelne Stelle und aggregierte Metriken für alle Stellen anzeigen.
- [BCG](./activities-attract.md) – Neue Aktivitätstypen ermöglichen die Nutzung eines vordefinierten Formulars für die Erfassung der Daten des Kandidaten bezüglich beruflicher Chancengleichheit (BCG) und der staatlichen Abteilung zur Überwachung der Chancengleichheit für Beschäftige bei öffentlichen Aufträgen (Office of Federal Contract Compliance Program - OFCCP). Das vordefinierte Formular kann nicht bearbeitet werden.
- [Interessentenempfehlung](./intelligent-recommendations.md#prospect-recommendations) – Attract überprüft frühere und aktuelle Kandidaten und stellt eine Liste von Interessenten bereit, die gut für Ihre Stelle passen könnten.
- [Bedeutungssuche](./attract-talent-pools.md#search-and-view-candidate-profiles) – Sie können die gesamte Kandidatendatenbank nach bestimmten Fähigkeiten, Namen oder Informationen zur Ausbildung suchen. Attract durchsucht das gesamte Profil und hebt alle gefundenen Übereinstimmungen hervor. Attract sucht auch alle Dokumente, die für einen Kandidaten verfügbar sind und ordnet die Suchergebnisse logisch an.
- [Aktivitätszielgruppe](./whats-new-talent-march-20.md#setting-the-audience-on-activities) – Sie können die Zielgruppe für Aktivitäten (wie Gesprächsvereinbarung, Zeitplan oder Feedback) auf **Alle Kandidaten**, **Interne Kandidaten** oder **Externe Kandidaten** festlegen. Sie können kundenspezifische Aktivitäten wie YouTube Videos, Webinhalt und Microsoft Formulare für alle Kandidaten, interne Kandidaten, externe  Kandidaten oder Einstellungsteams bereitstellen.
- [Mit LinkedIn anwenden](./career-site.md#enable-applying-for-jobs-with-linkedin-profiles) – Sie können eine Option in Ihrer Attract Karrieresite einrichten, damit Stellenkandidaten sich über LinkedIn bewerben können. Diese Funktion steuert den Bewerbungsprozeß für Kandidaten, indem sie das LinkedIn-Profil verwenden können, um ihre Bewerbung auf der Karrieresite automatisch auszufüllen.
- [Quellnachverfolgung](./source-tracking.md) – Attracts verfolgt die Quelle der Kandidatenbewerbungen und stellt wertvolle Informationen bereit, die Sie bei der Erfüllung der Rekrutierungsanstrengungen unterstützen. Sie können auch eine Bewerbungsquelle auswählen, wenn Sie einen Kandidaten dem Kandidatenpool hinzufügen.
- [Silbermedaillengewinner](./whats-new-talent-march-20.md#designate-silver-medalists-to-assign-high-value-applicants-for-future-positions) – Wenn Kandidaten hervorragend in Ihre Organisation passen würden, Sie diese aber nicht für die aktuelle Position eingeladen haben, können Sie dies als Silbermedaillengewinner definieren. Durch diese Funktion kann die Zeit beim nächsten Mal reduziert werden, wenn eine ähnliche Stelle verfügbar ist.

### <a name="core-hr"></a>Zentrale Personalverwaltung

- [Überprüfen Sie Positionshierarchiedaten](./whats-new-talent-may-13-2019.md#new-page-to-validate-position-hierarchy-data) – Sie können die Verwaltungshierarchie wie alle Zirkelverweise prüfen, die versehentlich importiert wurden.
- [Geben Sie Ursachencodes auf Sonderurlaubstypen an](./whats-new-talent-may-13-2019.md#specify-reason-codes-on-leave-types) – Sie können Ursachencodes für Sonderurlaubstypen angeben.
- [Erzwingen von Ursachencodes für Freizeitanforderungen](./whats-new-talent-may-13-2019.md#require-reason-codes-for-specific-leave-types-on-time-off-requests) – Neben den Ursachencodes für Sonderurlaub gibt es auch Ursachencodes für Freizeitanforderungen.
- [Erstellen Sie eine Urlaub- und Abwesenheitsbuchungsliste bereit für Personalverwaltung](./whats-new-talent-may-13-2019.md#provide-a-leave-and-absence-transaction-list-for-hr) – Sie können eine Liste der Sonderurlaubstypen und Abwesenheitsbuchungen anzeigen, mit deren Hilfe erhalten Einblicke in Freizeitsalden.

### <a name="onboard"></a>Aufnehmen

Keine Vorschaufunktionen sind derzeit für Microsoft Onboard verfügbar.

## <a name="feedback"></a>Feedback

Wir möchten von Ihnen über Ihre Erfahrung mit diesen Vorschaufunktionen hören Wir empfehlen Ihnen, Ihr Feedback regelmäßig auf den folgenden Seiten zu veröffentlichen, wenn Sie diese oder andere Funktionen nutzen:

- [Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) - Diese Seite ist eine großartige Ressource, auf der Benutzer Anwendungsfälle diskutieren, Fragen stellen und Hilfe von der Community erhalten können.
- Teilen Sie uns mit, welche Funktionen Sie im Produkt sehen möchten und welche Änderungen Ihrer Meinung nach an bestehenden Funktionen vorgenommen werden sollten. Verwenden Sie die folgenden Webseiten, um Produktideen vorzuschlagen:

    - [Attract Ideen](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [Core HR Ideen](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)
    - [Onboard Ideen](https://powerusers.microsoft.com/t5/Ideas-for-Onboard/idb-p/Onboard)

Stellen Sie sicher, dass Sie keine persönlichen Daten (Informationen, die Sie identifizieren könnten) in Ihre Feedback- oder Produktbewertungseinreichungen mitsenden. Die gesammelten Informationen können weiter analysiert werden und werden nicht zur Beantwortung von Anfragen im Rahmen der geltenden Datenschutzgesetze verwendet. Personenbezogene Daten, die im Rahmen dieser Programme separat erfasst werden, unterliegen der [Microsoft-Datenschutzerklärung](https://privacy.microsoft.com/privacystatement).

> [!TIP]
> Setzen Sie ein Lesezeichen für dieses Thema und schauen Sie regelmäßig vorbei, um über neue Vorschaufunktionen auf dem Laufenden zu bleiben, wenn wir sie veröffentlichen.

## <a name="see-also"></a>Siehe auch

- [Talent Apps testen oder kaufen](https://dynamics.microsoft.com/talent/overview/)
- [Neuigkeiten](./whats-new.md)
- [Versionshinweise](https://docs.microsoft.com/business-applications-release-notes/index)
- [Erhalten Sie Support für Talent](./talent-support.md)
