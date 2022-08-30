---
title: Lebensereignistypen konfigurieren
description: Microsoft Dynamics 365 Human Resources verwendet Lebensereignistypen, um Ereignisse zu definieren, mit denen die Anmeldung zu den Mitarbeiterleistungen aktualisiert wird.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: df523dd4da11e24c7b601c8f34aef24ad6cb3b18
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337011"
---
# <a name="configure-life-event-types"></a>Lebensereignistypen konfigurieren

Dynamics 365 Human Resources verwendet **Lebensereignistypen**, um Ereignisse zu definieren, bei denen eine Aktualisierung der Anmeldung für Mitarbeiterleistungen zulässig ist, z.B. Heirat oder Geburt eines Kindes. Jede Kennung des Lebensereignistyps darf nur einem Lebensereignistyp zugeordnet werden. Wenn Sie z.B. eine **Lebensereignis-ID** mit der Bezeichnung **Adressänderung** erstellen, die mit der Lebensereignisart **Adressänderung eines Mitarbeiters** verknüpft ist, können Sie keine weitere ID mit der Bezeichnung **Adressänderung eines Mitarbeiters** erstellen und diese mit der Lebensereignisart **Adressänderung eines Mitarbeiters** verknüpfen. Wenn ein Lebensereignistyp nicht mit einem Plantyp verknüpft ist, löst der Lebensereignistyp kein Lebensereignis aus. Weitere Informationen finden Sie unter [Plantypen erstellen](hr-benefits-setup-plan-types.md).

## <a name="create-a-life-event-type"></a>Lebensereignistyp erstellen

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Lebensereignistypen**.

2. Wählen Sie **Neu** aus.

3. Geben Sie Werte für die folgenden Felder an:

   | Feld | Beschreibung |
   | --- | --- |
   | **Kennung des Lebensereignistyps** | Der eindeutige Bezeichner für den Lebensereignistyp. |
   | **Beschreibung** | Eine Beschreibung des Lebensereignistyps. |
   | **Lebensereignistyp** | Ein Katalysator für die Aktualisierung der Vorteilsregistrierung eines Mitarbeiters. Eine Liste der Lebensereignisse finden Sie unter [Lebensereignisse](hr-benefits-setup-payment-frequencies.md?life-events) unten. |

4. Wählen Sie **Speichern**.

## <a name="view-attached-plans"></a>Angefügte Pläne anzeigen

Sie sehen eine Liste der Pläne, die dem ausgewählten **Lebensereignistyp** zugeordnet sind. Lebensereignisse sind an einen Plantyp gebunden und Plantypen sind mit einem Plan verknüpft.

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Lebensereignistypen**.

2. Wählen Sie **Aktivitäten**.

3. Wählen Sie **Angefügte Pläne**.

## <a name="life-events"></a>Lebensereignisse

Sie können beim Erstellen eines Lebensereignistyps aus den folgenden Lebensereignissen auswählen:

| Lebensereignis | Elektronische Adresse | Auslöser |
| --- | --- | --- |
| **Änderung des Familienstands** | **Arbeitskraft > Profil > Persönliche Informationen > Familienstand**| Änderung des Familienstandes |
| **Änderung des Beschäftigungsstatus** |**Arbeitskraft > Beschäftigung > Seite Beschäftigungsverlauf** | Für eine Arbeitskraft mit einem bestehenden Beschäftigungsdetail wird das Erstellen eines neuen Beschäftigungsdetail mit einem anderen Beschäftigungsstatus ein Lebensereignis auslösen.  Das Aktualisieren eines vorhandenen Beschäftigungsdetaildatensatzes mit einem anderen Beschäftigungsstatus löst ebenfalls ein Ereignis aus.  |
| **Änderung der Mitarbeiteradresse** |**Arbeitskraft > Profil > Adressen**</li><li>**Arbeitskraft > Persönliche Informationen > Persönliche Kontakte > Adresse**</li></ul> | Änderung der Adresse. Die Adresse muss **Primär** sein, um ein Lebensereignis auszulösen. |
| **Änderung der abhängigen Person** |<br><ul><li>**Arbeitnehmer > Profil > Persönliche Informationen > Persönliche Kontakte**/li><li>**Mitarbeiter-Self-Service**</li></ul> | Fügen Sie einen persönlichen Kontakt hinzu, indem Sie ihn als abhängig angeben und **Gültig ab** definieren. Aktualisierung der abhängigen **Gültig bis**-Informationen eines persönlichen Kontakts. Die persönliche Kontaktbeziehung muss Kind, Ehepartner, Lebenspartner oder Ex-Ehepartner sein.  |
| **Geburt oder Adoption (Unterhaltsberechtigter)** |<br><ul><li>**Arbeitskraft > Profil > Persönliche Informationen > Persönliche Kontakte**</li><li>**Mitarbeiter-Self-Service > Persönliche Daten bearbeiten > Persönliche Kontakte**</li></ul>| **Geburtsdatum** oder **Adaptionsdatum** werden hinzugefügt oder aktualisiert. Das **Geburtsdatum** des Untergeordneten ist erforderlich. |
| **Verlust der Abdeckung (Ehepartner/Lebenspartner)** | Arbeitskraft > Profil > Persönliche Informationen > Persönliche Kontakte > Unterhaltsberechtigtendetails > Verlust der Abdeckung | **Verlust der Abdeckung** wurde für einen persönlichen Kontakt ausgewählt, zusammen mit **Gültigkeitsdatum** |
| Beschäftigungsänderung für Lebenspartner | **Arbeitskraft > Profil > Persönliche Informationen > Persönliche Kontakte > Abhängige Details > Beschäftigt** | Erstellen eines persönlichen Kontakts und Festlegen von **Beschäftigt** auf **Ja**. Aktualisieren eines persönlichen Kontakts und Ändern von **Beschäftigt**.  |
| **Beurlaubung (Ehepartner/Lebenspartner)** | **Arbeitskraft > Profil > Persönliche Informationen > Persönliche Kontakte > Unterhaltsberechtigtendetails > Beurlaubung** | Persönlicher Kontakt erstellt und **Abwesenheitsdatum** ist definiert. Persönlicher Kontakt **Freistellung** wird aktualisiert. Persönlicher Kontakt **Abwesenheitsdatum** wird aktualisiert.  |
| **Änderung der Abdeckung (Position)** |<br><ul><li>**Arbeitskraft > Positionszuweisung > Positionszuweisungen der Arbeitskraft**</li><li>**Positionen > Positionen**</li></ul>| Änderung der Position in den Datensätzen für die Zuordnung der Arbeitskräfte zur Position. Änderung der Zuordnung der Arbeitskraft in der Position. |
| **Änderung der Abdeckung (Gehalt)** |<br><ul><li>**Arbeitskraft > Vergütung > Fester Plan**</li><li>**Arbeitskraft > Persönliche Informationen > Leistungen Jahresgehalt**</li></ul>| Wenn **Vergütungsmanagement > Gemeinsame Parameter der Humanressourcen > Vergünstigungen > Jahresgehalt Vergünstigungen** nicht aktiviert ist, wird durch die Aktualisierung von **Arbeitskraft > Vergütung > Fester Plan** ein lebenswichtiges Ereignis erstellt. Wenn **Benefits Management > Gemeinsame Parameter der Human Resources > Benefits > Benefits Jahresgehalt** aktiviert ist, wird durch die Aktualisierung von **Arbeitskraft > Persönliche Informationen > Benefits Jahresgehalt** ein Ereignis erstellt. |
| **Krankenversicherung (Mitarbeiter/Unterhaltsberechtigter)** | **Arbeitskraft > Profil > Persönliche Informationen > Persönliche Kontakte > Unterhaltsberechtigtendetails > Gültigkeitsdatum Krankenversicherung** | Das Hinzufügen oder Aktualisieren des **Medicare Gültig**-Datums für einen persönlichen Kontakt erstellt dieses Lebensereignis. |
| **Gerichtlich angeordnete Unterstützung** | **Arbeitnehmer > Profil > Persönliche Informationen > Persönliche Kontakte > Unterhaltsberechtigte > Gerichtlich angeordneter Unterhalt** (QMSCO/QDRO) und Gültigkeitsdaten | Beim Erstellen eines persönlichen Kontakts wird ein Lebensereignis erstellt, wenn **Gerichtlich angeordnete Unterstützung** **Ja** ist. Das Aktualisieren von **Gerichtlich angeordnete Unterstützung** oder **Gerichtlich angeordnetes Verfallsdatum** löst ebenfalls ein Lebensereignis aus. |
| **Verstorben** | **Arbeitskraft > Profil > Persönliche Informationen > Todestag** | Ein **Stornodatum** wird eingegeben oder aktualisiert. |
| **Versicherungsnachweis** | **Arbeitskraft > Arbeitskraft > Versionen > Beschäftigungshistorie > Datumsmanager > Vorteilsdetails** | **Versicherungsnachweis** wird auf **Ja** festgelegt. **Datum für den Nachweis der Versicherbarkeit** ist definiert. |
| **Begünstigter** | **Arbeitskraft > Profil > Persönliche Informationen > Persönliche Kontakte** | Ein persönlicher Kontakt wird hinzugefügt und die Felder **Begünstigter** und **Wirkungsdatum** werden ausgefüllt. Der persönliche Kontakt muss vom Typ **Kind**, **Ehepartner**, **Haushaltspartner**, **Geschwister**, **Familienkontakt**, **AndererKontakt** oder **Elternteil** sein. |
| **Mitarbeiter-Krankenversicherung** | **Arbeitskraft > Arbeitskraft > Versionen > Beschäftigungshistorie > Datumsmanager > Vorteilsdetails** | **Medicare-Berechtigung** wird auf **Ja** festgelegt. **Medicare-Berechtigungsdatum** wird geändert. |
| **Geburtstag** | **Leistungsverwaltung > Verarbeitung von Lebensereignissen** | Diese Lebensereignisse werden von **Life Event Change Processing** erstellt. Der Prozess analysiert den gewählten Zeitraum und die juristische Entität und findet die zugehörigen Arbeitskräfte. Es berechnet den letzten Geburtstag und erstellt ein Geburtstags-Lebensereignis, falls nicht bereits eines erstellt wurde. |
| **Änderung der Arbeitskraftberechtigung (nicht US-spezifisch)** |<br><ul><li>**Arbeitskraft > Beschäftigung**</li><li>**Arbeitskraft > Arbeitskraft > Versionen > Beschäftigungshistorie**</li></ul>| Erstellt ein Lebensereignis, wenn:<br><ul><li>Erstellen einer neuen Beschäftigung, und es gibt eine frühere Beschäftigung, und der Typ der Arbeitskraft ändert sich.</li><li>Erstellen eines neuen Beschäftigungsdetails, und es gibt ein vorheriges Beschäftigungsdetail, und der Beschäftigungstyp oder die Beschäftigungskategorie ändert sich.</li><li>Aktualisierung eines Beschäftigungsdatensatzes und ein anderer Typ von Arbeitskraft wird festgelegt.</li><li>Aktualisierung eines Datensatzes zur Beschäftigung und Angabe eines anderen Beschäftigungstyps oder einer anderen Kategorie.</li></ul> |
| **Neue Berechtigungsüberschreibung (nicht US-spezifisch)** | **Erweiterte Personalverwaltung > Vorteile > Pläne > Vorteile > Berechtigungsregelüberschreibung** | Lebensereignisverarbeitung verwenden<br>Das Erstellen einer neuen Leistungsplan-Berechtigungsüberschreibung für eine Arbeitskraft löst dieses Lebensereignis aus.<br>BenefitEligibilityRuleOverride.ValidFrom. |
| **Änderung der Berechtigungsregelüberschreibung (nicht US-spezifisch)** | **Erweiterte Personalverwaltung > Vorteile > Pläne > Vorteile > Berechtigungsregelüberschreibung** | Das Aktualisieren von **Gültig von** oder **Gültig bis** bei einer Leistungsplan-Berechtigungsüberschreibung löst dieses Lebensereignis aus. |
| **Ablauf der Berechtigungsregelüberschreibung (nicht US-spezifisch)** | Leistungsverwaltung > Verarbeitung von Lebensereignissen  | Diese Lebensereignisse werden von **Life Event Change Processing** erstellt. Der Prozess analysiert den gewählten Zeitraum und die juristische Entität und findet die zugehörigen Leistungsplan-Zulassungen. Es erstellt Lebensereignisse, wenn die Überschreibungen abgelaufen sind. |
| **Neuer Vorteilsplan (nicht US-spezifisch)** | **Erweiterte Personalverwaltung > Vorteile > Pläne > Neu** | Berechtigungsoptionen werden zu einem aktuellen Plan hinzugefügt. Ein neuer Plan mit Berechtigungsoptionen im Anhang wurde hinzugefügt.</br></br>HR-Mitarbeiter sollten in diesem Fall die Verarbeitung der Lebensereignisberechtigung ausführen. |
| **Änderung der Berechtigungsregel (nicht US-spezifisch)** | **Leistungsmanagement > Anspruchsregeln** | Verarbeitung von Lebensereignisberechtigungen verwenden. Protokolliert, wenn **BenefitEligibilityRule** Datensätze die folgenden Werte geändert haben: **UseEmplCategory**, **UseEmplStatus**, oder **UseEmplType**. Aktualisiert nur Lebensereignistransaktionen, die bereits für eine geänderte Regel oder ein geändertes Berechtigungskriterium vorhanden sind. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
