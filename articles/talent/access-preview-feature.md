---
title: Auf Vorschaufunktionen in Talent zugreifen
description: In diesem Thema wird beschrieben, wie ein Administrator die Vorschaufunktionen aktivieren kann, und es werden die Funktionen aufgeführt, die derzeit für Vorschau aktiviert sind.
author: rschloma
manager: AnnBe
ms.date: 04/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: cd738cafc97477182e574ee0f363fdcf1df7da7a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "304509"
---
# <a name="access-preview-features-in-talent"></a>Auf Vorschaufunktionen in Talent zugreifen

[!include[banner](../includes/banner.md)]

Im Rahmen unseres kontinuierlichen Rollouts von Produktkapazitäten wollen wir unseren Kunden so schnell wie möglich neue Funktionen zur Verfügung stellen. Administratoren können Vorschaufunktionen in ihrer Umgebung sehen und nutzen. Diese Funktionen sind fast fertig für die allgemeine Verfügbarkeit und wurden ausgiebig getestet. Wir sind nur auf der Suche nach einer letzten Runde von Kunden-Feedback und Validierung, bevor wir sie in der Regel veröffentlichen.

In diesem Thema wird beschrieben, wie ein Administrator die Vorschaufunktionen aktivieren kann, und es werden die Funktionen aufgeführt, die derzeit für Vorschau aktiviert sind. Diese Liste wird aktualisiert, wenn die Funktionen zur allgemeinen Verfügbarkeit freigegeben werden und wenn neue Funktionen zur Vorschau freigegeben werden. Es erfolgt keine Benachrichtigung, wenn neue Funktionen zur Vorschau freigegeben werden. Die Benutzer werden nur beginnen, die Funktionen zu sehen.

## <a name="enable-or-disable-preview-features"></a>Vorschaufunktionen aktivieren oder deaktivieren

Sie können die Einstellung **Vorschaufunktionen** im Microsoft Dynamics 365 for Talent Admin Center verwenden, um Vorschaufunktionen zu aktivieren oder zu deaktivieren. Standardmäßig ist die Einstellung ausgeschaltet. Das Aktivieren oder Deaktivieren von Vorschaufunktionen ist umgebungsspezifisch.

> [!IMPORTANT]
> Durch Aktivieren der Einstellung **Vorschaufunktionen** aktivieren Sie Vorschaufunktionen für alle Benutzer in Ihrer Organisation, die sich in dieser Umgebung befinden. Indem Sie die Einstellung deaktivieren, deaktivieren Sie die Vorschaufunktionen und machen sie für Ihre Benutzer unzugänglich. Die Vorschaufunktionen werden in Talent nur eingeschränkt unterstützt. Sie verwenden möglicherweise weniger Datenschutz- und Sicherheitsmaßnahmen und sind nicht in der Talent-Service-Level-Vereinbarung enthalten. Sie sollten keine Vorschaufunktionen verwenden, um personenbezogene Daten (d. h. Informationen, die Sie identifizieren könnten) oder andere Daten zu verarbeiten, die gesetzlichen oder behördlichen Anforderungen unterliegen.

### <a name="enable-or-disable-preview-features-for-your-organization"></a>Aktivieren oder Deaktivieren von Vorschaufunktionen für Ihr Unternehmen

#### <a name="attract"></a>Anwerben

1. Melden Sie sich bei Microsoft Dynamics 365 for Talent: Attract an.
2. Wählen Sie im **Setup**-Menü (das Zahnradsymbol) in der oberen rechten Ecke **Admin-Einstellungen**.
3. Wählen Sie auf der Registerkarte **Feature-Verwaltung** die Option neben **Vorschau-Features**, so dass sie blau wird.
4. Optional können Sie einzelne Funktionen steuern, indem Sie bestimmte Funktionen auf dieser Seite aktivieren/deaktivieren.
5. Aktualisieren Sie Ihren Browser, um die neuen Funktionen zu sehen. (Alle Benutzer, die bereits angemeldet sind, sehen die Funktionen beim nächsten Mal, wenn sie sich anmelden, oder sie können ihren Browser aktualisieren, um die Funktionen sofort zu sehen.)

#### <a name="core-hr"></a>Zentrale Personalverwaltung

1. Melden Sie sich bei Talent an. Es öffnet sich der zentrale Arbeitsbereich der Personalveraltung von dem aus Sie die weiteren Schritte ausführen können. 
2. Wählen Sie **Systemadministration \>Verknüpfte Systemparameter.**
3. Setzen Sie auf der **Seite Systemparameter** auf der Registerkarte **Vorschaufunktionen** die Option **Vorschaumodus für alle Benutzer aktivieren** auf **Ja**, um Vorschaufunktionen verfügbar zu machen.

> [!NOTE]
> Um die Vorschaufunktionen zu deaktivieren, verwenden Sie die gleichen grundlegenden Schritte. Wenn Sie die Vorschaufunktionen deaktivieren, werden sie für Ihre Benutzer unzugänglich, und es können Fehler in Prozessen auftreten, die mit den Funktionen verknüpft sind.

## <a name="features-that-are-currently-in-preview"></a>Funktionen, die sich derzeit in der Vorschau befinden

### <a name="attract"></a>Anwerben

- **Relevante Kandidaten für einer Stelle** – Personalbeschaffungsmitarbeiter und Einstellungsmanager können leicht aus allen Bewerbern die relevantesten Kandidaten für eine Stelle erkennen. Die besten 5 Bewerber werden auf der Grundlage der Relevanz ihres Lebenslaufs/Profils bezüglich der Stellenbeschreibung angezeigt.
- **Relevante Stellen** – Kandidaten können nun eine Liste anderer Stellen anzeigen, die für Sie auf der Grundlage ihres Lebenslaufs/Profils und die Stellenbeschreibungen relevant sind.  Momentan wird dies den Kandidaten als Vorschlag für andere Gelegenheiten angezeigt, sobald Sie sich bewerben.
- –**BCG-/OFCCP-Unterstützung** – Neue Aktivitätstypen ermöglichen die Nutzung eines vordefinierten Formulars für die Erfassung der Daten des Kandidaten bezüglich beruflicher Chancengleichheit (BCG) und der staatlichen Abteilung zur Überwachung der Chancengleichheit für Beschäftige bei öffentlichen Aufträgen (Office of Federal Contract Compliance Program - OFCCP).  Dies ist ein vordefiniertes Formular und kann nicht bearbeitet werden.

    > [!NOTE]
    > Stellenangebote sind nur für Kunden sichtbar, die ein oder mehrere LinkedIn-Stellenangebote abonnieren. Ansonsten sehen Kunden eine Stelle nur, wenn sie explizit danach suchen. Es gibt eine Verzögerung, wenn Stellenangebote an LinkedIn gesendet werden. Ein Stellenangebot kann bis zu einigen Stunden dauern, nachdem es von Attract veröffentlicht wurde.

- **Bewerber bewerben** - Sowohl interne als auch externe Bewerber können sich jetzt direkt über die Stellenseite auf der Karriereseite bewerben.
- **Angebotsverwaltung** - Benutzer können jetzt Angebotsschreiben aus Vorlagen erstellen, die Platzhalter enthalten. Wenn die Kandidaten in die Angebotsphase eintreten, können Personalvermittler und Einstellungsmanager das Angebots-Tool verwenden, um das formelle Angebot eines Kandidaten über Vorlagen vorzubereiten, das Angebot zur internen Genehmigung zu senden und schließlich das Angebot an den Kandidaten zur Unterzeichnung zu senden. Viele neue Funktionen werden im Laufe der Zeit dem Angebots-Tool hinzugefügt, und die Vorschaufunktion wird mit diesen Funktionen aktualisiert, sobald wir bereit sind, sie zur Vorschau freizugeben.

### <a name="core-hr"></a>Zentrale Personalverwaltung

- **Offene Registrierung** - Die offene Registrierung bietet den Mitarbeitern eine einfache Möglichkeit, ihre Leistungen selbst auszuwählen. Personalsachbearbeiter (HR-Administratoren) können die Vorteile eines offenen Registrierungsprozesses für ihre Organisation und die Registrierungserfahrung für Mitarbeiter mithilfe einer leicht verständlichen, geführten Lösung konfigurieren.

## <a name="feedback"></a>Feedback

Unabhängig davon, ob das Feedback positiv oder negativ ist, möchten wir von Ihnen hören, wie Sie die Vorschaufunktionen nutzen. Wir empfehlen Ihnen, Ihr Feedback regelmäßig auf den folgenden Seiten zu veröffentlichen, wenn Sie diese oder andere Funktionen nutzen.

- [Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) - Diese Seite ist eine großartige Ressource, auf der Benutzer Anwendungsfälle diskutieren, Fragen stellen und Hilfe von der Community erhalten können.
- Verwenden Sie die folgenden Webseiten, um Produktideen vorzuschlagen. Teilen Sie uns mit, welche Funktionen Sie im Produkt sehen möchten und welche Änderungen Ihrer Meinung nach an bestehenden Funktionen vorgenommen werden sollten.

    - [Attract Ideas](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [Zentrale Personalverwaltung](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)

Geben Sie keine persönlichen Daten (Informationen, die Sie identifizieren könnten) in Ihre Feedback- oder Produktbewertungseinreichungen ein. Die gesammelten Informationen können weiter analysiert werden und werden nicht zur Beantwortung von Anfragen im Rahmen der geltenden Datenschutzgesetze verwendet. Personenbezogene Daten, die im Rahmen dieser Programme separat erfasst werden, unterliegen der [Microsoft-Datenschutzerklärung](https://privacy.microsoft.com/privacystatement).

> [!TIP]
> Setzen Sie ein Lesezeichen für dieses Thema und schauen Sie regelmäßig vorbei, um über neue Vorschaufunktionen auf dem Laufenden zu bleiben, wenn wir sie veröffentlichen.
