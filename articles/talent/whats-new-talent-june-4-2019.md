---
title: Neuerungen und Änderungen in Dynamics 365 Talent (4. Juni 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4a42a3b817024447e2ff26cfcb3cdd0df1351158
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528042"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-june-4-2019"></a>Neuerungen und Änderungen in Dynamics 365 Talent (4. Juni 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent entweder neu oder geändert sind.

## <a name="changes-in-attract"></a>Änderungen in Attract

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Attract.

## <a name="coming-soon-in-attract"></a>Bald verfügbar in Attract

### <a name="job-approvals-on-the-home-page"></a>Stellengenehmigungen werden auf der Startseite angezeigt

Genehmigungen werden im Abschnitt **Genehmigungen** im Dashboard angezeigt. Genehmiger können ihre Genehmigungen unter **Ihneb Zugewiesen** prüfen. In diesem Abschnitt finden die Stellenkennung, Titel, andere genehmigende Person sowie das Datum, an dem die Stelle zugewiesen wurde. Benutzer, die eine Stelle zur Genehmigung eingeben, können deren Einzelvorgänge unter **von Ihnen angefordert** prüfen. Dieser Abschnitt zeigt die genehmigende Person an, die die übermittelte Stelle noch genehmigen muss.

## <a name="changes-in-onboard"></a>Änderungen in Onboard

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-Änderungen

Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2330.

### <a name="new-page-to-validate-position-hierarchy-data"></a>Neue Seite zur Bestätigung der Positionshierarchiedaten

Personalverwaltung (HR) und Administratoren können nun die Verwaltungshierarchie für alle Zirkelverweise prüfen, die möglicherweise versehentlich importiert wurden. Sie können auf diese neue Seite über **Organisatorische Verwaltung\> Links \> Positionen \> Positionshierarchieprüfung** zugreifen.

### <a name="specify-reason-codes-on-leave-types"></a>Geben Sie Ursachencodes bei Sonderurlaubstypen an

Organisationen brauchen möglicherweise zusätzliche Informationen zu Freizeitanforderungen. Sie können nun Ursachencodes für Sonderurlaubstypen definieren und Mitarbeiter aktivieren, damit sie einen Ursachencode für ihre Freizeitanforderungen auszuwählen können.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Erfordert Ursachencodes für bestimmte Urlaubstypen bei Freizeitanforderungen

Organisationen brauchen ggf. bestimmte Ursachencodes für Sonderurlaubstypen, wenn Mitarbeiter Freizeit beantragen. Diese Anforderung ist möglicherweise aufgrund der Unternehmensrichtlinie oder der gesetzlichen Vorgaben vorhanden. Sie können nun angeben, welche Sonderurlaubstypen einen Ursachencode erfordern und Sie können von Mitarbeitern verlangen, dass sie einen Ursachencode für den Sonderurlaubstyp für ihre Abwesenheitsanforderungen angeben.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Erstellen Sie eine Urlaub- und Abwesenheitsbuchungsliste für die Personalverwaltung

Die Möglichkeit zum Nachverfolgen von Mitarbeiterfreizeit und ein Verständnis dafür, wie Freizeit berechnet wird, hilft nicht nur der Personalverwaltung, Fragen von Mitarbeitern zu beantworten sondern stellt auch sicher, dass die Freizeit für Mitarbeiter korrekt ist. Personalverwaltung besitzt nun eine neue Anzeige für die Transaktionen (Zuschüsse, Abgrenzungen, Regulierungen und Anforderungen), sodass die Mitarbeiter der Personalverwaltung die Gründe hinter den Abwesenheitssalden anzeigen können.

### <a name="deleting-a-record-from-talent-doesnt-remove-the-record-from-common-data-service"></a>Beim Eingang eines Datensatzes aus Talent wird der Datensatz nicht aus Common Data Service gelöscht

Datensätze, die von Talent: Core HR entfernt wurden, werden nun auch in Common Data Service entfernt.

### <a name="variable-compensation-plan-valid-fromto-dates-arent-being-honored"></a>Der Plan für variable Vergütung, der ab / bis zum Daten gültig ist, wird nicht berücksichtigt

In dieser Version kann nicht gleichzeitig ein Mitarbeiter in einem Plan für variable Vergütung registriert werden, wenn das Startdatum vor dem Startdatum oder das Enddatum nach dem Enddatum des Plans liegt. 

### <a name="performance-review-comments-are-removed-when-users-select-cancel"></a>Leistungsbeurteilungskommentare werden entfernt, wenn der Benutzer abbrechen auswählen

Diese Version behebt das Problems, in dem Prüfungskommentare entfernt werden, wenn ein Benutzer beginnt, Kommentare zu ändern, dann aber **Abbrechen** auswählt. 

## <a name="in-preview"></a>Vorschau

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Vorschaufunktionen werden nur in den Sandkasteninstanzen aktiviert

Wenn Sie eine neue Instanz von Talent bereitstellen, können Sie angeben, ob der Instanztyp **Produktion** oder **Sandkasten** ist. Die Instanzen vom **Sandkasten** Typ ermöglichen ein frühzeitiges Testen neuer Funktionen. Alle vorhandenen Talent-Instanzen werden zum Instanztyp **Produktion** aktualisiert. Wenn eine der vorhandenen Instanzen auf den aktualisierten Instanztyp **Sandkasten** aktualisiert werden soll, wenden Sie sich an den [Support](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support), um die Änderungsanforderung zu initiieren.

Weitere Informationen dazu, wie Änderungen veröffentlicht werden, finden unter [Talent bereitstellen](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>Begrenzen der Sonderurlaubstypen in den Abwesenheitsanforderungen

Organisationen können Mitarbeitern viele unterschiedliche Arten von Sonderurlaub anbieten. Allerdings ist er möglicherweise nicht angebracht, dass Mitarbeiter einen Freizeitantrag für bestimmte Sonderurlaubstypen senden. Diese Sonderurlaubstypen können stattdessen von der Personalverwaltung (HR) verwaltet werden. Mit dieser Version können Sie konfigurieren, für welche Sonderurlaubstypen die Mitarbeiter Abwesenheitsanforderungen übermitteln können. 

## <a name="coming-soon-in-core-hr"></a>Bald in Core HR verfügbar

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Anzeigen von erweiterten Informationen, um die Leistung im Manager Self-Service zu melden

Mit einer neuen Option können Manager die Leistung von ihren direkten Mitarbeitern und den erweiterten Mitarbeitern anzeigen. Aktuell können Linienmanager Leistungsziele zuweisen und aktualisieren und neue Überprüfungen ausstellen, die ihre Mitarbeiter mitverwalten. Darüber hinaus können Vorgesetzte und ihre Mitarbeiter Leistungserfassungen verwalten und aktualisieren, um sicherzustellen, dass der Leistungsprüfungsprozess problemlos verläuft. Wenn diese Änderung implementiert ist, sind Manager in der Lage, leistungsbezogene Informationen neben jenen für die direkt unterstellten Mitarbeitern auch jene für ihre erweiterten Mitarbeiter anzuzeigen und zu verwalten. 

### <a name="print-performance-reviews"></a>Leistungsbeurteilungen drucken

Mitarbeiter, Manager und Personalverwaltung können dann die Leistungsbeurteilung eines Mitarbeiters drucken.


[!INCLUDE[footer-include](../includes/footer-banner.md)]