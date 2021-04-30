---
title: Neuerungen oder Änderungen in Dynamics 365 Human Resources (14. Mai 2020)
description: Dieses Thema beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 14. Mai 2020 neu sind oder geändert wurden.
author: andreabichsel
ms.date: 05/14/2020
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
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f8244d512c9e1236fc52cd4a91cdc78cc2b9b984
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893100"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-14-2020"></a>Neuerungen oder Änderungen in Dynamics 365 Human Resources (14. Mai 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Human Resources neu oder geändert wurden. Änderungen gelten für Build-Nummer 8.1.3244. Die Zahlen in Klammern in einigen Überschriften beziehen sich zur Referenz auf die Supportnummern in Lifecycle Services (LCS).

## <a name="platform-changes"></a>Plattformänderungen

Plattformänderungen sind in der Version dieser Woche enthalten. Weitere Informationen finden Sie unter [Plattform-Updates für Version 10.0.10 von Finance and Operations Apps (Mai 2020)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34.md). Diese Version enthält Fehlerkorrekturen und Änderungen an gespeicherten Ansichten.
 
## <a name="ensure-dataverse-picklists-are-consistent-with-leave-enums-436343"></a>Sicherstellen, dass Dataverse-Auswahllisten mit den Urlaubsaufzählungen (436343) übereinstimmen

Dataverse-Auswahllisten sind nun mit den Urlaubsaufzählungen konsistent.

## <a name="allow-users-to-configure-leave-request-workflow-based-on-the-request-amount-300044"></a>Benutzern das Konfigurieren des Urlaubsanforderungsworkflows basierend auf dem Anforderungsbetrag erlauben (300044)

Benutzer können Urlaubsanforderungsworkflows basierend auf Anforderungsbeträgen konfigurieren.
 
## <a name="new-worker-form-exposes-data-through-the-view-menu-when-advanced-security-is-enabled-403185"></a>Neues Arbeitskraftformular stellt Daten über das Menü „Ansicht“ bereit, wenn die erweiterte Sicherheit aktiviert ist (403185)

In dieser Version ist die Anzeige von Mitarbeitern für verschiedene juristische Personen korrigiert, wenn der erweiterte Zugriff aktiviert ist und auf Arbeitskräfte in anderen Unternehmen zugegriffen werden kann.

## <a name="allow-running-leave-accruals-for-a-single-plan-or-a-single-company-318844"></a>Ausführung von Urlaubsrückstellungen für einen einzelnen Plan oder ein einzelnes Unternehmen zulassen (318844)

Mit dieser Änderung können Sie Abgrenzungen für ein Unternehmen oder einen Plan ausführen.
 
## <a name="show-the-positions-full-time-equivalent-fte-in-the-enrolled-workers-form-414658"></a>Das Vollzeitäquivalent der Position im Formular für registrierte Arbeitskräfte anzeigen (414658)

Der Vollzeitäquivalent-Wert der Position einer Arbeitskraft bestimmt den Abgrenzungssatz einer Arbeitskraft, wenn die Option „Vollzeitäquivalent“ für den Urlaubstyp aktiviert ist. Dieses Feld ist jetzt im Formular **Registrierte Arbeitskräfte** und im Dialogfeld **Massenregistrierung** enthalten.

## <a name="add-leave-balance-expiration-batch-job-431266"></a>Stapelverarbeitungsauftrag für Ablauf des Urlaubssaldos hinzufügen (431266)

Ein neuer Stapelverarbeitungsauftrag, der täglich ausgeführt wird, ist nun verfügbar. Es verringert den verbleibenden Urlaubssaldo, wenn Ablauftermine aktuell werden.

## <a name="exporting-personal-contacts-for-an-employee-using-the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-the-parent-relationship-type-345893"></a>Beim Exportieren persönlicher Kontakte für einen Mitarbeiter mit der Entität „Persönliche Kontaktperson der Arbeitskraft“ kein Export persönlicher Kontakte vom Beziehungstyp „Übergeordnet“ (345893)

Die Datenentität **Persönliche Kontaktperson der Arbeitskraft** (**HcmPersonalContactPersonEntity** in DMF und **PersonalContactPerson** in OData) konnte keine persönlichen Kontakte mit dem Beziehungstyp **Übergeordnet** exportieren. Dieses Problem wurde für persönliche Kontakte behoben, die nach dieser Änderung erstellt wurden. Bestehende persönliche Kontakte vom Typ **Übergeordnet** werden in einer späteren Version behoben.

## <a name="reason-codes-display-across-different-scenarios-when-theyre-marked-as-leave-and-absence-and-the-streamlined-employee-form-is-enabled-434163"></a>Ursachencodes werden in verschiedenen Szenarien angezeigt, wenn sie als Urlaub und Abwesenheit markiert sind und das optimierte Mitarbeiterformular aktiviert ist (434163).

Diese Änderung beschränkt die Ursachencodes ausschließlich auf Urlaubs- und Abwesenheitscodes, wenn Sie die optimierte Eingabe von Mitarbeitern aktivieren.

## <a name="the-preview-feature-assign-a-leave-plan-to-employees-in-the-future-displays-error-433555"></a>Vorschaufunktion zum Zuweisen eines Urlaubsplans zu Mitarbeitern in der Zukunft zeigt Fehler an (433555)

Mit dieser Änderung wird eine Fehlermeldung korrigiert, wenn ein Urlaubsplan zwei Urlaubstypen aufweist und Sie versuchen, einen Mitarbeiter zuzuweisen.

## <a name="getting-started-banner-appears-for-all-users-441731"></a>Banner „Erste Schritte“ wird für alle Benutzer angezeigt (441731)

Mit dieser Änderung wird das Banner „Erste Schritte“ für Benutzer ausgeblendet, die keine Systemadministratoren oder Datenverwaltungsadministratoren sind. 

## <a name="the-dataverse-worker-address-entity-works-differently-in-terms-of-date-time-effective-dates-in-human-resources-425071"></a>Die Entität „Arbeitskraftadresse“ von Dataverse funktioniert in Bezug auf Gültigkeitsdatumswerte für Datum/Uhrzeit in Human Resources unterschiedlich (425071)

Durch diese Änderung bleiben die Adressinformationen in bestimmten Szenarien basierend auf den Datumsangaben der Adresse ausgerichtet.

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-425407"></a>Einer genehmigten Urlaubsanforderung kann kein Anhang hinzugefügt werden (425407)

Mit der Veröffentlichung dieser Woche können Sie genehmigten Urlaubsanforderungen Anhänge hinzufügen, ohne die Urlaubsanforderung zu ändern.

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

## <a name="see-also"></a>Siehe auch

[Neuerungen oder Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2019 Versionswelle 2 ](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]