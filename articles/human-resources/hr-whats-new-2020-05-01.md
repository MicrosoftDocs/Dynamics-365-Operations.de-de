---
title: Neuerungen oder Änderungen in Dynamics 365 Human Resources (1. Mai 2020)
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 1. Mai 2020 neu sind oder geändert wurden.
author: andreabichsel
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 52eb748fe8b3c62d6a5ebf46fd01afc291ec5572
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803416"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-1-2020"></a>Neuerungen oder Änderungen in Dynamics 365 Human Resources (1. Mai 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dieser Artikel beschreibt Funktionen, die entweder neu oder geändert in Dynamics 365 Human Resources sind. Änderungen gelten für Build-Nummer 8.1.3196. Die Zahlen in Klammern in einigen Überschriften beziehen sich zur Referenz auf die LCS-Supportnummern.

## <a name="new-performance-management-entities-available-in-data-management-framework-dmf"></a>Neue Leistungsverwaltungs-Entitäten im Data Management Framework (DMF) verfügbar

Die folgenden Entitäten sind jetzt verfügbar. Wenn diese Entitäten nicht in der Entitätsliste aufgeführt sind, verwenden Sie die Option **Entitäten aktualisieren** unter **Framework-Parameter > Entitätseinstellungen > Entitätsliste aktualisieren**.

- **Diskussionskompetenz**
- **Diskussionsziele**
- **Diskussionsmessung**
- **Diskussionsthema**
- **Leistungserfassung**
- **Verbrauchsberechnung**
- **Zielmessung**

Darüber hinaus wurden **Gesamtbewertung** und **Durchschnittliche Bewertung** der Entität **Diskussion** hinzugefügt.

## <a name="increase-length-of-leave-request-comments-275641"></a>Länge der Kommentare zu Abwesenheitsanträgen erhöhen (275641)

Kommentare zu Abwesenheitsanträgen können jetzt mehr als 100 Zeichen enthalten.

## <a name="final-comments-on-reviews-dont-appear-when-the-manager-or-employee-is-signed-into-a-different-company-431688"></a>Abschließende Kommentare zu Überprüfungen werden nicht angezeigt, wenn der Manager oder Mitarbeiter sich bei einem anderen Unternehmen angemeldet hat (431688)

Alle Kommentare werden jetzt angezeigt, wenn Bewertungen angezeigt werden.

## <a name="user-defined-links-arent-supported-on-new-worker-form-390374"></a>Benutzerdefinierte Links werden im neuen Arbeitskraft-Formular (390374) nicht unterstützt

Benutzerdefinierte Links sind jetzt im optimierten Formular **Arbeitskraft** aktiviert.

## <a name="hcmratinglevelentity-causes-odata-api-crash-439476"></a>HcmRatingLevelEntity verursacht einen Absturz der OData-API (439476)

Diese Änderung korrigiert den API-Absturz. Ein duplizierter Name hat diesen Fehler verursacht.

## <a name="in-preview"></a>Vorschau

## <a name="leave-suspension"></a>Urlaub aussetzen

Sie können Urlaub und Abwesenheit in der Personalabteilung für einen Mitarbeiter aussetzen. Durch das Aussetzen des Urlaubs werden die Urlaubsrückstellungen für ausgewählte Urlaubstypen gestoppt. Wenn die Aussetzung erfolgt, nachdem eine Rückstellung bearbeitet wurde, führt die Aussetzung des Urlaubs zu einer anteiligen Anpassung des Urlaubssaldos des Mitarbeiters. Weitere Informationen finden Sie unter [Urlaub aussetzen](hr-leave-and-absence-suspend-leave.md).

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>Update der Benutzererfahrung, um anzuzeigen, dass die Ansammlung ausgesetzt ist (429550)

Die Benutzererfahrung zeigt nun an, dass das Ansammlung für einen Plan ausgesetzt wurde.

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a>Urlaubsansammlung für angegebene Abwesenheitstypen (272447) aussetzen

In dieser Version kann die Personalverwaltung eine Regel erstellen, um Abwesenheitsansammlungen für Mitarbeiter mit Abwesenheitsanträgen für unbezahlte Abwesenheit auszusetzen. Unbezahlte Abwesenheit kann ein Typ sein, muss es aber nicht sein. Sie können jede Abwesenheit basierend auf einem anderen Abwesenheitstyp aussetzen.

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a>DMF-Entität verfügbar für Ansammlungsaussetzungen (429549)

Eine DMF-Entität ist jetzt verfügbar für Ansammlungsaussetzungen.

## <a name="add-reason-code-to-accrual-suspensions-429547"></a>Ursachencode für Ansammlungsaussetzungen (429547) hinzufügen

Ursachencodes, die der Ansammlungsaussetzung hinzugefügt wurden.

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a>Beginnen Sie mit dem Übergang von Personalverwaltungsparametern zu Urlaubs- und Abwesenheitsparametern

In dieser Version wird mit der Kombination von Personalverwaltungsparametern mit Urlaubs- und Abwesenheitsparametern begonnen.

## <a name="carry-forward-rules"></a>Vortragungsregeln

Sie können einen Vortragsabwesenheitstyp für Vortragssalden angeben, bei denen Vortragsanpassungen übertragen werden. Wenn ein Mitarbeiter beispielsweise 10 Tage vorzieht, können Sie für diese 10 Tage einen anderen Urlaubstyp auswählen. Weitere Informationen finden Sie unter [Konfigurieren Sie Urlaubs- und Abwesenheitstypen](hr-leave-and-absence-types.md).

## <a name="known-issues"></a>Bekannte Probleme

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>Die SharePoint-Vorschau funktioniert in einigen Umgebungen nicht.

Wenn die Dokumentvorschau für in SharePoint gespeicherte Dokumente nicht funktioniert, versuchen Sie das folgende Verfahren:

1. Stellen Sie sicher, dass dem Administrator-Benutzerkonto eine E-Mail mit dem Benutzerdatensatz zugeordnet ist. Diese Informationen können auf der Seite **Benutzer** angezeigt werden. Wenn E-Mail nicht eingerichtet ist, müssen Sie die E-Mail und den Anbieter mit dem OData-Excel-Add-In hinzufügen. Standardmäßig ist die E-Mail-Adresse im Excel-Design nicht vorhanden. Sie müssen das Excel-Design bearbeiten, alle Felder hinzufügen, anwenden und aktualisieren. Sobald Sie diese Schritte ausgeführt haben, können Sie das Administratorkonto aktualisieren.

2. Nachdem dem Administratorkonto ein E-Mail-Konto zugeordnet ist, melden Sie sich mit Administratorrechten bei der Personalabteilung an.

3. Greifen Sie auf einen Anhang in SharePoint zu, um die Dokumentvorschau zu starten.

4. Melden Sie sich mit einem anderen Benutzerkonto an, das Zugriff auf Anhänge hat, und überprüfen Sie, ob die Vorschau wie erwartet funktioniert.

## <a name="see-also"></a>Siehe auch

[Neuerungen oder Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2019 Versionswelle 2 ](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]