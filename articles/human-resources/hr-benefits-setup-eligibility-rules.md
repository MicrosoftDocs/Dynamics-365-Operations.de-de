---
title: Berechtigungsregeln und -optionen konfigurieren
description: In diesem Thema wird beschrieben, wie Sie Anspruchsberechtigungsregeln und Optionen in der Verwaltung von Leistungen in Microsoft Dynamics 365 Human Resources festlegen können.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 034957628580c468ed00b14afeb7e49af15c45cc
ms.sourcegitcommit: 8592c661b41f9cef8b7ef2863a3b97bf49a4e6f9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "7423470"
---
# <a name="configure-eligibility-rules-and-options"></a>Berechtigungsregeln und -optionen konfigurieren 

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Nachdem Sie die erforderlichen Parameter für die Vorteilsverwaltung konfiguriert haben, können Sie Berechtigungsregeln, Bündel, Perioden und Programme erstellen, die Sie mit Ihren Vorteilsplänen verknüpfen.

Berechtigungsregeln werden verwendet, um zu bestimmen, ob Mitarbeiter für einen Plan in Frage kommen. Arbeitnehmer müssen die Bedingung von mindestens einer Regel erfüllen, um als anspruchsberechtigt zu gelten. Sie haben beispielsweise zwei Regeln für einen Plan. Die erste Regel (Zeile 1) besagt, dass der Mitarbeitertyp **Mitarbeiter** sein muss. Die zweite Regel (Zeile 2) besagt, dass der Mitarbeiter ein Vollzeitmitarbeiter ist. Daher sind Arbeitnehmer, die Regel 1 erfüllen, berechtigt, auch wenn sie nur in Teilzeit beschäftigt sind.

Sie können jedoch eine einzelne Regel mit mehreren Bedingungen einrichten. In diesem Fall müssen Arbeitnehmer alle Bedingung derr Regel erfüllen, um als anspruchsberechtigt zu gelten. Sie haben beispielsweise eine Regel mit dem Namen **Angestellter in Vollzeit**. Diese Regel besagt, dass der Mitarbeitertyp **Mitarbeiter** *und* in Vollzeit beschäftigt sein muss. Daher müssen Arbeitnehmer beide Bedingungen der Regel erfüllen, um berechtigt zu sein.

> [!IMPORTANT]
> Jedem Leistungsplan muss mindestens eine Anspruchsberechtigungsregel zugeordnet sein. Sie können einem Vorteil mehrere Regeln zuordnen.

## <a name="create-an-eligibility-rule"></a>Berechtigungsregel erstellen

Die Berechtigungsregeln legen fest, welche Mitarbeiter sich für die einzelnen Vorteilspläne registrieren können. Nachdem Sie die Berechtigungsregeln definiert haben, ordnen Sie sie Vorteilsplänen zu. Anschließend können Sie die Registrierungsberechtigung verarbeiten, um zu sehen, welche Mitarbeiter für die einzelnen Pläne berechtigt sind. 

Während der offenen Registrierung können Mitarbeiter Vorteilspläne auswählen. Wenn sie nach der Registrierung aufgrund der Berechtigungsregeln nicht mehr für einen Vorteilsplan infrage kommen, wird die Registrierung nicht automatisch rückgängig gemacht. Wenn ein Lebensereignis eintritt, das sich auf die Planberechtigung auswirkt, wird in der Regel eine Registrierungsperiode eingeleitet, in der der Mitarbeiter Pläne auswählen kann, für die er berechtigt ist. 

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Berechtigungsregeln und -optionen**.

2. Wählen Sie in der Registerkarte **Berechtigungsregeln** die Option **Neu** aus, um eine Berechtigungsregel zu erstellen. Wählen Sie **Angefügte Pläne** aus, um Pläne anzuzeigen, die mit einer Berechtigungsregel verknüpft sind.

3. Geben Sie Werte für die folgenden Felder an.

   | Feld | Beschreibung |
   | --- | --- |
   | **Berechtigungsregel** | Ein eindeutiger Bezeichner für die Berechtigungsregel. |
   | **Beschreibung** | Eine Beschreibung der Berechtigungsregel. |
   | **Gültig ab Datum und Zeit** | Das Startdatum der Berechtigungsregel. | 
   | **Gültig bis Datum und Zeit** | Das Enddatum der Berechtigungsregel. |
   | **Mitarbeitertyp verwenden** | Gibt an, ob für den Mitarbeitertyp des Mitarbeiters die Vorteilsberechtigungsregel verwendet werden soll. |
   | **Arbeitskrafttyp** | Der Arbeitskrafttyp, wenn die Umschaltfläche **Mitarbeitertyp verwenden** auf **Ja** eingestellt ist. |
   | **Mitarbeiterstatus verwenden** | Gibt an, ob für den Mitarbeiterstatus des Mitarbeiters die Vorteilsberechtigungsregel verwendet werden soll. |
   | **Status** | Der Mitarbeiterstatus, wenn die Umschaltfläche **Mitarbeiterstatus verwenden** auf **Ja** eingestellt ist. Wenn die Umschaltfläche **Mitarbeiterstatus verwenden** auf **Nein** eingestellt ist, wird das Feld nicht verwendet. |
   | **Beschäftigungskategorie verwenden** | Gibt an, ob die **Beschäftigungskategorie** des Mitarbeiters als Teil der Vorteilsberechtigungsregel verwendet werden soll. | 
   | **Beschäftigungskategorie** | Die Beschäftigungskategorie des Mitarbeiters, wenn die Umschaltfläche **Beschäftigungskategorie verwenden** ist auf **Ja** eingestellt ist. |
   | **Neue Einstellungsregel verwenden** | Gibt an, ob der neue Einstellungsperiodenwert des neuen Mitarbeiters als Teil der Vorteilsberechtigungsregel verwendet werden soll. |
   | **Registrierungsperiode** | Die Periode, für die die Registrierung einer Neueinstellung zulässig ist. Wenn Sie dies auch in Parametern einstellen, hat die Parametereinstellung Vorrang. |
   | **Ehemaligen Beschäftigungsstatus verwenden** | Gibt an, ob der frühere Beschäftigungsstatus eines Mitarbeiters als Teil der Vorteilsberechtigungsregel verwendet werden soll. Beispielsweise können Sie eine Berechtigungsregel angeben, die auf eine Deckungswartezeit für alle Mitarbeiter verzichtet, die vom Status **Entlassen** zu einem Status **Beschäftigt** innerhalb von 90 Tagen nach ihrer vorherigen Beschäftigung gewechselt haben. |

4. Wählen Sie unter **Zusätzliche Kriterien** die folgenden Optionen aus und fügen Sie nach Bedarf Informationen hinzu.

   | Option | Beschreibung |
   | --- | --- |
   | **Zulässiges Alter** | Gibt den Altersbereich oder die Altersbereiche an, die erforderlich sind, um die Berechtigungsregel zu erfüllen. |
   | **Zulässige Abteilung** | Gibt die Abteilung oder Abteilungen an, in denen sich ein Mitarbeiter befinden muss, um die Berechtigungsregel zu erfüllen. |
   | **Zulässiger Beschäftigungstyp** | Gibt den Beschäftigungstyp oder die Beschäftigungstypen an, unter den/die ein Mitarbeiter fallen muss, um die Berechtigungsregel zu erfüllen. Beispiel: Vollzeit oder Teilzeit. |
   | **Zulässige Stelle** | Gibt die Stelle oder Stellen an, die die Berechtigungsregel erfüllen. Stellen sind mit Positionen verbunden und Positionen werden von Mitarbeitern besetzt. |
   | **Zugelassene Stellenfunktion** | Gibt die Stellenfunktion oder Stellenfunktionen an, die eine Berechtigungsregel erfüllen. Beispiel: Vertriebskraft oder Techniker. |
   | **Zulässiger Stellentyp** | Gibt den Stellentyp oder die Stellentypen an, die die Berechtigungsregel erfüllen. Beispiel: Bürotätigkeit oder Führungskraft. |
   | **Zulässige juristische Person** | Gibt die juristische Person oder die juristischen Personen an, die für die Berechtigungsregel zulässig sind. Beispiel: Contoso Entertainment System USA. |
   | **Region für Vergütungsberechtigung** | Gibt den Standort des Mitarbeiters an, der die Berechtigungsregel erfüllt. Beispiel: USA, Mitte. |
   | **Zulässige Position** | Gibt die Position oder die Positionen an, die die Berechtigungsregel erfüllen. Beispiel: HR Assistant oder HR Manager. |
   | **Zulässiger Positionstyp** | Gibt den Positionstyp oder die Positionstypen an, die die Berechtigungsregel erfüllen. Beispiel: Vollzeit. |
   | **Zulässigers** | Gibt die Bundesländer oder Kantone an, die die Berechtigungsregel erfüllen. Beispiel: Sachsen, Deutschland oder Wallis, Schweiz. |
   | **Zulässige Beschäftigungsbedingungen** | Gibt die Beschäftigungsbedingung an, die die Berechtigungsregel erfüllt. Beispiel: beliebig oder Gruppenvertrag. |
   | **Zulässige Gewerkschaft** | Gibt die Mitgliedschaft bei Gewerkschaften an, die die Berechtigungsregel erfüllen. Beispiel: IG Metall.</br></br>Bei Verwendung einer gewerkschaftsbasierten Berechtigungsregel muss das Enddatum des Gewerkschaftsdatensatzes der Arbeitskraft angegeben werden. Sie können es nicht leer lassen. |
   | **Zulässige Postleitzahl** | Gibt die Postleitzahlen an, die die Berechtigungsregel erfüllen. Beispiel: 58104. |

5. Unter **Zusätzliches Detail** können Sie die folgenden zusätzlichen Details anzeigen.

   | Feld | Beschreibung |
   | --- | --- |
   | **Zulässiges Benutzerfeld** | Gibt zusätzliche Berechtigungsregeln basierend auf benutzerdefinierten Feldern an. |
   | **Berechtigungstyp** | Gibt die Kriterienkategorie an, die Sie unter **Zusätzliche Kriterien** ausgewählt haben. |
   | **Berechtigungsreferenz** | Gibt die Werte an, die Sie unter **Zusätzliche Kriterien** ausgewählt haben. |
   | **Beschreibung** | Die Beschreibung, die Sie unter **Zusätzliche Kriterien** ausgewählt haben. |

6. Wählen Sie **Speichern** aus.

## <a name="using-custom-fields-in-eligibility-rules"></a>Verwenden von benutzerdefinierten Feldern in Berechtigungsregeln

[Benutzerdefinierte Felder](hr-developer-custom-fields.md) kann in der Personalabteilung erstellt werden, um zusätzliche Informationen zu verfolgen. Diese Felder können direkt zur Benutzeroberfläche hinzugefügt werden, und der zugrunde liegenden Tabelle wird dynamisch eine Spalte hinzugefügt.  

Benutzerdefinierte Felder können im Berechtigungsprozess verwendet werden. Berechtigungsregeln können einen oder mehrere benutzerdefinierte Feldwerte verwenden, um die Berechtigung eines Mitarbeiters zu bestimmen.  Um einer vorhandenen Regel ein benutzerdefiniertes Feld hinzuzufügen oder eine neue Regel zu erstellen, gehen Sie zu **Leistungsverwaltung> Links> Einrichtung > Teilnahmebedingungen> Benutzerdefinierte Feldberechtigung**. Auf dieser Seite können Sie eine Regel erstellen, die ein oder mehrere benutzerdefinierte Felder verwendet, und Sie können für jedes benutzerdefinierte Feld mehrere Werte definieren, um die Berechtigung zu bestimmen.

Die folgenden Tabellen unterstützen benutzerdefinierte Felder, die bei der Berechtigungsverarbeitung verwendet werden können:

- Arbeitskraft (HcmWorker)  
- Auftrag (HcmJob)  
- Position (HcmPosition)  
- Positionsdetail (HcmPositionDetail)  
- Arbeitskraftzuweisung für die Position  
- Beschäftigung (HcmEmployment)  
- EmploymentDetails (HcmEmploymentDetails)  
- Auftragsdetails (HcmJobDetails)  

Die folgenden benutzerdefinierten Feldtypen sind in der Berechtigungsverarbeitung unterstützt:

- Text  
- Auswahlliste  
- Anzahl  
- Dezimal  
- Kontrollkästchen  

In der folgenden Tabelle sind die Feldinformationen für benutzerdefinierte Feldberechtigungsformulare aufgeführt.

| Feld  | Beschreibung |
|--------|-------------|
| Name | Name der Kriterien, die erstellt werden. |
| Name der Tabelle | Der Tabellenname, der das benutzerdefinierte Feld enthält, das für die Berechtigungsregel verwendet wird. |
| Feldname | Das Feld, das für die Berechtigungsregel verwendet wird. |
| Operatortyp | Zeigt den Operator an, der in der Konfiguration der benutzerdefinierten Feldberechtigung verwendet wird. |
| Wert | Zeigt den Wert an, der in der Konfiguration der benutzerdefinierten Feldberechtigung verwendet wird. |

## <a name="eligibility-logic"></a>Zulassungslogik

In den folgenden Abschnitten wird beschrieben, wie die Leistungsberechtigung verarbeitet wird.

### <a name="rules-assigned-to-a-plan"></a>Einem Plan zugewiesene Regeln 
Wenn einem Leistungsplan mehrere Anspruchsregeln zugewiesen sind, muss ein Mitarbeiter mindestens eine Regel erfüllen, um sich für den Leistungsplan anmelden zu können.  Im folgenden Beispiel muss der Mitarbeiter entweder die Anforderungen der Regel **Auftragstyp** oder die Regel **Aktive Mitarbeiter** erfüllen.

![Der Mitarbeiter muss entweder die Anforderungen der Regel Auftragstyp oder die Regel Aktive Mitarbeiter erfüllen.](media/RulesAssignedToAPlan.png)
 
### <a name="criteria-within-an-eligibility-rule"></a>Kriterien innerhalb einer Zulassungsregel 
Innerhalb einer Regel definieren Sie die Kriterien, aus denen die Regel besteht. Im obigen Beispiel sind die Kriterien für die Regel **Stellentyp** wobei Stellentyp = Direktoren. Daher muss der Mitarbeiter auf der Stufe Direktor sein, um berechtigt zu sein. Dies ist eine Regel, bei der es nur ein Kriterium innerhalb der Regel gibt.

Sie können Regeln definieren, die mehrere Kriterien haben. Wenn Sie innerhalb einer Anspruchsregel mehrere Kriterien definieren, muss ein Mitarbeiter alle Kriterien innerhalb der Regel erfüllen, um für den Leistungsplan in Frage zu kommen. 

Zum Beispiel setzt sich die Regel **Aktive Mitarbeiter** aus den folgenden Kriterien zusammen. Damit der Mitarbeiter aufgrund der Regel **Aktive Mitarbeiter** bereichtigt ist, muss der Mitarbeiter in der juristischen Person USMF beschäftigt sein *und* einen Positionstyp Vollzeit haben.  

![Kriterien innerhalb einer Zulassungsregel.](media/CriteriaWithinAnEligibilityRule.png) 
 
### <a name="multiple-conditions-within-criteria"></a>Mehrere Bedingungen innerhalb von Kriterien

Regeln können weiter erweitert werden, um mehrere Bedingungen innerhalb eines einzigen Kriteriums zu verwenden. Der Mitarbeiter muss mindestens eine Bedingung erfüllen, um berechtigt zu sein. Um auf dem obigen Beispiel aufzubauen, kann die Regel **Aktive Mitarbeiter** weiter ausgebaut werden, um Mitarbeiter einzubeziehen, die auch Teilzeitbeschäftigte sind. Infolgedessen muss der Mitarbeiter jetzt ein Mitarbeiter in USMF sein *und* entweder ein Vollzeit- oder ein Teilzeitbeschäftigter sein.  

![Mehrere Bedingungen innerhalb von Kriterien.](media/MultipleConditionsWithinCriteria.png) 
 
### <a name="eligibility-conditions-within-a-custom-field-criterion"></a>Teilnahmebedingungen innerhalb eines benutzerdefinierten Feldkriteriums 
Ähnlich wie oben können benutzerdefinierte Felder beim Erstellen von Berechtigungsregeln verwendet werden und auf dieselbe Weise funktionieren. Beispielsweise möchten Sie den Mitarbeitern von Fargo und Kopenhagen, die von zu Hause aus arbeiten, eine Internet-Rückerstattung anbieten, da die Internetkosten an diesen Standorten höher sind. Erstellen Sie dazu zwei benutzerdefinierte Felder: **Bürostandort** (Auswahlliste) und **Von zu Hause aus arbeiten** (Kontrollkästchen). Erstellen Sie dann eine Regel mit dem Namen **WFH-Mitarbeiter**. Das Kriterium für die Regel ist wo **Bürostandort = Fargo** oder **Kopenhagen** *und* wo **Von zu Hause aus arbeiten = Ja**.

Die angepassten Anspruchsberechtigungsregeln müssten wie in der folgenden Abbildung festgelegt werden. 

![Teilnahmebedingungen innerhalb eines benutzerdefinierten Feldkriteriums.](media/EligibilityConditionsWithinACustomFieldCriterion.png) 
 
## <a name="configure-bundles"></a>Bündel konfigurieren

Bündel sind ein Satz verwandter Vorteilspläne. Sie können Vorteilsbündel verwenden, um Vorteilspläne zu gruppieren, die ein Mitarbeiter auswählen muss, um sich für bestimmte Vorteilspläne anzumelden, die möglicherweise von anderen Vorteilsplanregistrierungen abhängig sind. Beispiele dafür, wann Sie ein Bündel verwenden sollten:

- Ein Krankenversicherungsbündel , das eine Krankenversicherung mit hohem Selbstbehalt und einem dazugehörigen Gesundheitssparkonto (Health Savings Account, HSA) umfasst.

- Eine Lebensversicherungsplan mit einem obligatorischen Lebensversicherungsplan für Mitarbeiter in einem Bündel mit einem Lebensversicherungsplan für Unterhaltsberechtigte. Dies würde sicherstellen, dass ein Mitarbeiter keine Lebensversicherung für Unterhaltsberechtigte auswählen kann, ohne sich für die Mitarbeiterlebensversicherung zu registrieren.

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Berechtigungsregeln und -optionen**.

2. Wählen Sie in der Registerkarte **Bündel** die Option **Neu** aus, um ein Bündel zu erstellen. Wählen Sie **Angefügte Pläne** aus, um Pläne anzuzeigen, die mit einem Bündel verknüpft sind.

3. Geben Sie Werte für die folgenden Felder an.

   | Feld | Beschreibung |
   | --- | --- |
   | **Bündel** | Ein eindeutiger Bezeichner für das Bündel. |
   | **Beschreibung** | Eine Beschreibung des Bündels. |
   | **Haupt** | Gibt an, ob einer der Pläne im Bündel als Produktprogrammplan gekennzeichnet sein muss. Der Produktprogrammplan muss während der offenen Registrierung als Teil des Bündels ausgewählt werden, bevor der Vorteilsadministrator die Vorteilswahlen des Mitarbeiters bestätigen kann. |
   | **Gültig ab Datum und Zeit** | Das Datum und die Uhrzeit, an dem das Bündel aktiv wird. |
   | **Gültig bis** | Das Datum, an dem das Bündel abläuft. Der Standardwert lautet 31.12.2154 (stellvertretend für nie). |

4. Wählen Sie **Speichern**.

## <a name="configure-periods"></a>Perioden konfigurieren

In den Perioden wird festgelegt, wann die Vorteile in Kraft sind und wann sich Mitarbeiter registrieren dürfen. Sie können so viele Perioden erstellen, wie Sie möchten, um die offenen Registrierungs‑ und VorteilsabdeckungsPerioden beizubehalten. Die Jahre des Vorteilsplans können einem Kalenderjahr entsprechen oder nicht. 

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Berechtigungsregeln und -optionen**.

2. Wählen Sie in der Registerkarte **Perioden** die Option **Neu** aus, um eine Periode zu erstellen. Um einen Prozess auszuführen, der alle gültigen aktiven Vorteilspläne mit der Vorteilsperiode verknüpft, wählen Sie **Pläne anhängen**. Wählen Sie **Angefügte Pläne** aus, um Pläne anzuzeigen, die mit einem Bündel verknüpft sind. 

3. Geben Sie Werte für die folgenden Felder an.

   | Feld | Beschreibung |
   | --- | --- |
   | **Periode** | Der eindeutige Bezeichner für die Periode. |
   | **Gültig ab Datum und Zeit** | Das Startdatum und die Uhrzeit, zu der die Vorteilsperiode aktiv wird. |
   | **Gültig bis Datum und Zeit** | Das Datum und die Uhrzeit, ab denen die Vorteilsperiode inaktiv wird. |
   | **Start der Registrierung** | Das Anfangsdatum für die offene Registrierung. Bei einer offenen Registrierung kann ein Mitarbeiter in Self-Service-Vorteilen seine Vorteile auswählen. |
   | **Ende der Registrierung** | Das Enddatum für die offene Registrierung. |
   | **Öffnen** | Gibt an, ob die Periode offen ist, basierend auf dem Systemdatum und den Daten und Uhrzeiten für „Gültig ab“ und „Gültig bis“. | 
   | **Vorherige Periode** | Gibt die Vorteilsperiode an, die der ausgewählten Vorteilsperiode vorausgeht. Diese Informationen werden während der Vorteilsberechtigungsregistrierung verwendet, um Pläne, Abdeckungsoptionen und Beauftragte aus einem früheren Jahr zuzuweisen. |
 
4. Wählen Sie **Speichern**.

## <a name="use-a-flex-credit-program"></a>Flexguthabenprogramm verwenden

Sie können Flexguthabenprogramme verwenden, um Mitarbeiter für Vorteile gemäß einer festgelegten Höhe von Flexguthaben zu registrieren. Mitarbeiter können wählen, wie sie ihr Flexguthaben zuordnen möchten. Wenn ein Mitarbeiter beispielsweise in der Krankenversicherung seines Ehepartners mitversichert ist, möchte er möglicherweise das Guthaben, das er sonst für die Krankenversicherung verwendet hätte, für andere Vorteile verwenden.

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Berechtigungsregeln und -optionen**.

2. Wählen Sie auf der Registerkarte **Perioden** die Option **Flexguthabenprogramme**.

3. Wählen Sie ein zu übernehmendes Flexguthabenprogramm aus. Die Felder enthalten die folgenden Informationen.

   | Feld | Beschreibung |
   | --- | --- |
   | **Vergütungsgutschriftenkennung** | Der eindeutige Bezeichner des Flexguthabenprogramms. |
   | **Beschreibung** | Eine Beschreibung des Flexguthabenprogramms. | 
   | **Anfangsdatum** | Das Datum, an dem das Flexguthabenprogramm aktiv wird. |
   | **Enddatum** | Das Enddatum des Flexguthabenprogramms. Sie können den Standardwert (31.12.2154) beibehalten, um anzugeben, dass für das Flexguthabenprogramm kein geplanter Ablauf festgelegt ist. |
   | **Guthabenwert gesamt** | Die Höhe des Guthabens, das jeder Mitarbeiter für seine Vorteile verwenden muss. |
   | **Regel zur anteiligen Verrechnung** | Die Regel zur anteiligen Verrechnung von Flexguthaben, wenn ein Mitarbeiter in der Mitte der Flexguthabenperiode eingestellt wird. </br></br><ul><li>**Kein** – Der Mitarbeiter erhält kein Flexguthaben, wenn er nach dem Start des Flexguthabenprogramms eingestellt wird.</li><li>**Volles Guthaben** – Der Mitarbeiter erhält die volle Höhe des Flexguthabens, unabhängig davon, wann er eingestellt wird.</li><li>**Anteilige Verrechnung** – Der Mitarbeiter erhält einen Anteil des Flexguthabens, das auf seinem Startdatum basiert.</li></ul> |
   | **Formel für anteilige Berechnung des Flexguthabens** | Die Regel zur anteiligen Verrechnung von Flexguthaben, wenn Mitarbeiter in der Mitte der Flexguthabenperiode eingestellt werden. Die anteilige Verrechnung basiert auf dem Einstellungsbeginn. Dieses Feld wird nur verwendet, wenn im Feld **Regel zur anteiligen Verrechnung** die Option **Anteilige Verrechnung** ausgewählt wird. </br></br><ul><li>**Täglich** – Teilt die Höhe des Flexguthabens, die ein Mitarbeiter erhält, auf dem Tageslevel. Die Gesamthöhe des Flexguthabens wird durch die Anzahl der Tage in der Periode geteilt. Wenn Ihre Vorteilsperiode beispielsweise 400 Tage beträgt, dividiert das System die Gesamthöhe des Flexguthabens durch 400, um die Höhe des Flexguthabens zu berechnen, das ein Mitarbeiter pro Tag erhält.</li><li>**Aktueller Monat** – Teilt die Höhe des Flexguthabens, die ein Mitarbeiter erhält, auf dem Monatslevel, auf den aktuellen Monat gerundet. Die Gesamthöhe des Flexguthabens wird durch die Anzahl der Monate in der Periode geteilt. Wenn Ihre Vorteilsperiode beispielsweise 15 Monate beträgt, dividiert das System die Gesamthöhe des Flexguthabens durch 15, um die Höhe des Flexguthabens zu berechnen, das ein Mitarbeiter pro Monat erhält.</li><li>**Folgender Monat** – Teilt die Höhe des Flexguthabens, die ein Mitarbeiter erhält, auf dem Monatslevel, auf den nächsten Monat gerundet. Die Gesamthöhe des Flexguthabens wird durch die Anzahl der Monate in der Periode geteilt. Wenn Ihre Vorteilsperiode beispielsweise 15 Monate beträgt, dividiert das System die Gesamthöhe des Flexguthabens durch 15, um die Höhe des Flexguthabens zu berechnen, das ein Mitarbeiter pro Monat erhält.</li></ul> |
   
   Stellen Sie sicher, dass jeder Vorteilsplan nur für ein Flexguthabenprogramm pro Vorteilsperiode registriert ist. Sonst weiß das System nicht, mit welchem Flexguthabenprogramm das Flexguthaben vergeben werden soll und es treten Probleme auf. 

## <a name="configure-programs"></a>Programme konfigurieren

Bei Programmen handelt es sich um eine Reihe von Vorteilsplänen, für die gemeinsame Berechtigungsregeln gelten. Sie können Berechtigungsregeln für das gesamte Programm anstatt für jeden einzelnen Plan definieren. Beispiel: ein Programm für Vollzeitmitarbeiter von Contoso Kanada oder ein Programm auf Führungsebene von Contoso Europa. 

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Berechtigungsregeln und -optionen**.

2. Wählen Sie in der Registerkarte **Programme** die Option **Neu** aus, um ein Programm zu erstellen. Um Ausnahmen für Mitarbeiter zu machen, die die Anforderungen der Berechtigungsregeln nicht erfüllen, wählen Sie **Berechtigungsregelüberschreibung**. Wählen Sie **Angefügte Pläne** aus, um Pläne anzuzeigen, die mit einem Programm verknüpft sind.

3. Geben Sie Werte für die folgenden Felder an.

   | Feld | Beschreibung |
   | --- | --- |
   | **Programm** | Der eindeutige Bezeichner für das Programm. |
   | **Beschreibung** | Eine Beschreibung des Programms. | 
   | **Gültig ab Datum und Zeit** | Das Datum und die Uhrzeit, an dem das Programm aktiv wird. |
   | **Gültig bis Datum und Zeit** | Das Datum und die Uhrzeit, an dem das Programm abläuft. Der Standardwert lautet 31.12.2154 (stellvertretend für nie). |
   | **Abdeckungswarteperiode** | Die Periode, die ein Mitarbeiter warten muss, bevor die Abdeckung für das Vorteilsprogramm beginnt. |
   | **Abzugswarteperiode** | Die Periode, die ein Mitarbeiter wartet, bevor Abzüge für das Vorteilsprogramm beginnen. |
   | **Berechtigungsregeln** | Wählen Sie die Berechtigungsregeln aus, die für das Vorteilsprogramm gelten sollen. Sie definieren die Berechtigungsregeln auf der Registerkarte **Berechtigungsregeln** auf dieser Seite. |
   
4. Wählen Sie **Speichern**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
