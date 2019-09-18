---
title: Neuerungen oder Änderungen in Dynamics 365 for Talent (20. März 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 for Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 03/20/2019
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
ms.search.validFrom: 2019-03-20
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d316aff83bd9f60f054a970e223777db5e214adb
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741628"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-20-2019"></a>Neuerungen oder Änderungen in Dynamics 365 for Talent (20. März 2019)

[!include [banner](includes/banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 for Talent entweder neu oder geändert sind.

## <a name="changes-in-attract"></a>Änderungen in Attract

### <a name="setting-the-audience-on-activities"></a>Festlegen der Zielgruppe für Aktivitäten
Aktivitäten im System können nun die definierte Zielgruppe haben. Prozess-zugeordnete Aktivitäten (wie Gesprächsvereinbarung, Zeitplan, Rückmeldung und EEO) können auf alle Kandidaten, interne Kandidaten und externe Kandidaten festgelegt werden. Kundenspezifische Aktivitäten, wie Microsoft Forms, YouTube Videos und Webinhalt können allen Kandidaten, internen Kandidaten, externen  Kandidaten oder dem Einstellungsteam geliefert werden.  

### <a name="improve-career-site-job-discoverability-search-engine-optimization"></a>Verbessern Sie Karrieresite-Stellenauffindbarkeit: Suchmaschinen-Optimierung
Diese Funktion ermöglicht es, dass Suchmodulcrawler Stellenausschreibungen auf der Stellenportalsite in Attract finden. Das hilft Kandidaten, die publizierten Stellen auf der Karriereseite mithilfe von beliebten Suchmaschinen in Attract zu finden.

### <a name="show-login-hint-to-candidates-who-forgot-their-credentials"></a>Anmeldehinweise den Kandidaten anzeigen, die ihre persönlichen Anmeldeinformationen vergessen haben
Wenn ein Kandidat die Anmeldeinformationen vergaß, die verwendet wurden, um sich bei einer Stelle zu bewerben, während ein Link geöffnet wird, der für ihn gespeichert oder per E-Mail gesendet wurde, sieht er einen Tipp mit dem Anbieternamen und dem Benutzernamen (verborgen). Dies ermöglicht Ihnen, die korrekten Anmeldeinformationen zu verwenden, um auf die Stellenbewerbung zuzugreifen.

### <a name="help-internal-candidates-explore-internal-jobs"></a>Helfen Sie internen Kandidaten, die internen Stelen zu durchsuchen
Ein Problem wurde korrigiert, nämlich der, dass externe Kandidaten den Namen des Personalbeschaffungsmanagers oder des künftigen Vorgesetzten einer Stelle sehen konnten. Jetzt können nur noch interne Kandidaten das Einstellungsteammitglied für eine Stelle sehen. Es ist auch leichter für interne Kandidaten, sich auf interne Stellen zu bewerben und diese anzuzueigen. Wenn ein Kandidat versucht, auf den Link zuzugreifen, um sich auf eine reine interne Stelle zu bewerben, muss er sich mit den Azure Active Directory Anmeldeinformationen authentifizieren. Interne Kandidaten haben auch die Möglichkeit, das Einstellungsteammitglied zu kontaktieren, um ihr Interesse zu bekunden oder um mehr über die Stelle zu erfahren. Diese Funktion ist für alle Stellen nur für interne Kandidaten verfügbar. Weitere Informationen finden Sie unter [Funktionen für Karrierefunktionen in Attract](./career-site.md).

### <a name="designate-silver-medalists-to-assign-high-value-applicants-for-future-positions"></a>Wählen Sie Silbermedaillengewinner aus, um gut qualifizierte Bewerber künftigen Positionen zuzuordnen
Personalbeschaffungsmanager oder künftige Vorgesetzte haben oftmals eine Liste von Bewerbern, die gut für eine Position passen würden, aber denen man kein Angebot unterbreiten konnte, da die Stelle bereits besetzt war. Solche Bewerber, sogenannte Silbermedaillengewinner, sind wertvoll, da damit die Zeit verkürzt werden kann, wenn wieder eine ähnliche Position zu besetzten ist. Attract ermöglicht es nun Personalbeschaffungsmanagern und künftigen Vorgesetzten, Silbermedaillengewinner auf der Bewerberliste auszuwählen, wenn der Bewerber in die Angebotsphase wechselt. Die Silbermedaillengewinnerbezeichnung wird auf der Bewerberliste für die Stelle angezeigt. Sie erscheint auch in der Talentpoolansicht, wenn diese Bewerber Mitglieder in einem Pool des Personalbeschaffungsmanagers oder des künftigen Vorgesetzten sind. Darüber hinaus erscheint die Auszeichnung im Stellenverlauf als Teil des Talentpool-Profils des Kandidaten. Sie können diese Funktion anzeigen, indem Sie einen Administrator bitten, diese mithilfe der [Funktions-Verwaltung im  Administrator-Center](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature) zu aktivieren.

### <a name="add-applicants-to-talent-pools"></a>Bewerber den Talentpools hinzufügen
Es ist nun einfacher, Bewerber dem Talentpool hinzuzufügen, indem eine neue Aktivität auf der Bewerberliste erstellen. Indem Sie das Symbol **dem Talentpool hinzufügen** auswählen, können Personalbeschaffungsmitarbeiter oder zukünftige Vorgesetzte aus der Liste des Talentpools auswählen und einfach Bewerber dem Talentpool direkt aus der Bewerberliste für eine Stelle hinzufügen.

### <a name="configure-whether-a-resume-is-required-to-apply-for-a-particular-job"></a>Geben Sie an, ob ein Lebenslauf erforderlich ist, um sich für eine bestimmte Stelle zu bewerben
Basierend auf dem Debitorenfeedback können nun Personalbeschaffungsverantwortliche konfigurieren, ob ein Lebenslauf als hochgeladene Datei erforderlich ist, wenn sich der Kandidat für eine bestimmte  Stelle bewirbt. Diese Konfiguration ist Teil der Bewerbungsaktivität im Bewerungsprozess. Wenn der Schlüssel aktiviert ist, wird jede mögliche Bewerber aufgefordert, eine Zusammenfassung hochzuladen, für die die Position gültig sind. Die Anwendung keine gilt als abgeschlossen, es sei denn, dass eine Zusammenfassung hochgeladen wurde. Dies erleichtert Unstimmigkeiten im Bewerberpool, indem sichergestellt ist, dass jeder Bewerber ausreichend Informationen bereitstellt und der Personalbeschaffungsmitarbeiter diese selektieren kann.

### <a name="candidates-can-apply-to-a-job-using-their-linkedin-profile"></a>Kandidaten können sich auf eine Stelle mit ihrem LinkedIn-Profil anmelden
Kandidaten, die bereits ein aktualisiertes Profil auf LinkedIn haben, können sich auf Stellen mit einem Einzelklick mit diesem Profil bewerben.

### <a name="track-how-a-candidate-profile-originated-in-the-system-and-where-your-applicants-discover-the-jobs-they-applied-for"></a>Verfolgen Sie, woher ein Kandidatenprofil im System kommt und wo der Bewerber die Stelle, für die er sich bewirbt, gesehen hat
Sie können nun herausfinden, woher das Profil eines bestimmten Kandidaten in Attract kommt, indem Sie die Profilquelle unter den Kandidatendetails auf der Seite **Profil**- eines Bewerbers oder auf dem Talentpoolprofil ansehen.  Entsprechend können Sie herausfinden, wie jeder Bewerber die Stelle gefunden hat, indem Sie die Bewerberquelle in der **Bewerbungsaktivität** im Feed Bewerbungsaktivität ansehen. Diese Information ist auch im Stellenverlauf im Talentpoolprofil verfügbar. Wenn Personalbeschaffungsmanager oder künftige Vorgesetzte Kandidaten manuell hinzufügen, werden sie aufgefordert, die Quelle der Bewerbung oder des Kandidatenprofils auszuwählen. Wenn sich ein Kandidat erstmals bewirbt, ist die Profilquelle die selbe wie der Ursprung der Stellenbewerbung. Sie können diese Funktion anzeigen, indem Sie einen Administrator bitten, diese mithilfe der [Funktions-Verwaltung im  Administrator-Center](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature) zu aktivieren. Beachten Sie, dass vorhandene Kandidaten und Bewerber keine Quellinformationen haben. Allerdings können Personalbeschaffungsmanager diese Informationen manuell hinzufügen.

## <a name="changes-in-onboard"></a>Änderungen in Onboard

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-Änderungen

Änderungen in diesem Abschnitt gelten für Buildnummer 8.1.2195

### <a name="attract-integration-throws-duplicate-record-error-for-applications"></a>Ziehen Sie Integrationswurfsduplikats-Datensatzfehler für Bewerbungen angezeigt
In dieser Aktualisierung wurde ein Problem mit doppelten Datensätzen korrigiert. Dieses Problem tritt in Erscheinung, wenn der Arbeitsbereich **Personalführung** geöffnet wird.

### <a name="unable-to-close-form-when-editing-name-sequence"></a>Das Formular kann nicht geschlossen werden, wenn die Namensfolge bearbeitet wird
Änderungen können vorgenommen werden, um ein Problem zu beheben, wenn die Namensfolge im Feld Arbeitskraftformular bearbeitet wird.

## <a name="coming-soon"></a>Bald verfügbar

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Erweiterte Vergütungssicherheit (feste oder variable)
In vielen Organisationen hat der Vergütungs- und Vorteilsmanager nur Zugriff auf bestimmte Kompensationsdatensätze. Diese Datensätze sind möglicherweise für Führungskräfte oder regionale Mitarbeiter. Mit dieser Änderung kann HR Kompensationspläne für verschiedene Mitarbeitergruppen in der Organisation verwalten. Sie können Sicherheitsrollen festen und variablen Plänen zuordnen, die den Zugriff auf die Pläne und die Mitarbeiterdaten in Verbindung mit den Plänen bestimmen, wie Gehalts- oder Zulagedatensätze. Nur die Rollen mit Zugriff sind in der Lage, Vergütungen für solche Mitarbeiter zu verarbeiten.

###  <a name="email-support-for-alerts"></a>E-Mail-Support für Warnungen
Mit der Plattformaktualisierung 24 können Benutzer die Warnregeln erstellen, dass automatisch E-Mail-Benachrichtigungen an Kontakte gesendet werden, wenn dies von einem Ereignis ausgelöst wird.

### <a name="duplicate-employee-check-interface-changes"></a>Mitarbeiterscheck duplizieren: Schnittstellenänderungen
Mit dieser Änderung werden Duplikate erkannt, während Sie Namenfelder eingeben, und ein Status zeigt, wie viele Duplikate gefunden wurden. Sie können die zur Verfügung gestellte Verknüpfung aktivieren, um eine neue Seite zu öffnen, um zu prüfen, ob die gefundene Übereinstimmung verwendet werden soll. Das Duplikatsformular wird nicht automatisch geöffnet, um die Dateneingabe nicht zu unterbrechen.


