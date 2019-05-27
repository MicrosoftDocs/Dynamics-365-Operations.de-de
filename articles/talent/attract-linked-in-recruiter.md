---
title: Personalbeschaffung mittels LinkedIn Recruiter
description: Dieses Thema enthält Informationen zur Verwendung von Machine Learning, um Stellen- und Kandidaten-Empfehlungen zu erhalten.
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
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 4ac7a302e5bf589beb2b560b0ff5818e90c67139
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518048"
---
# <a name="sourcing-with-linkedin-recruiter"></a>Personalbeschaffung mittels LinkedIn Recruiter
[!include[banner](../includes/banner.md)]

LinkedIn ist die weltgrößte Talentdatenbank und häufig das Hauptsystem, dass Personalbeschaffer verwenden, um neue Kandidaten zu suchen und mit ihnen zu kommunizieren, um zu besetzende Stellen zu füllen. LinkedIn Recruiter-Integration in Dynamics 365 for Talent: Attract vereinfacht es Benutzern, Mitarbeiter einzustellen, und die Daten zwischen zwei Systemen synchron zu halten.

> [!NOTE]
> Sie benötigen das „Umfassende Einstellungs-Add-On” und LinkedIn Recruiter-Arbeitsplätze, um die LinkedIn Recruiter-Integration in Attract zu verwenden.

## <a name="set-up-linkedin-recruiter-with-attract"></a>Einrichten von LinkedIn Recruiter mit Attract 

Bevor Sie die LinkedIn Recruiter-Funktionen verwenden können, müssen Sie Zugriff auf Vertrags- oder Firmenebene bei Ihrer Attract-Instanz konfigurieren. Zum Abschluss des Konfigurationsvorgangs müssen Sie mit dem Benutzer zusammenarbeiten, der ein Administrator bei Ihrem LinkedIn Recruiter-Vertrag ist. Führen Sie die folgenden Schritte aus, um LinkedIn Recruiter mit Attract zu konfigurieren.

1.  Melden Sie sich bei Attract als Administrator an und wechseln Sie zu **Administratoreinstellungen**.

2.  Wählen Sie im linken Bereich die Registerkarte **LinkedIn-Integration** aus.

[![Attract-Administratoransicht, um die LinkedIn Recruiter-Integration zu starten](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3.  Klicken Sie auf **Verbinden**, um die Einrichtung zu starten und durch den LinkedIn-Anmeldungsprozess geführt zu werden.

4.  Wenn Sie über mehrere LinkedIn-Vertragslizenzen verfügen, wählen Sie den Vertrag aus, den Sie mit dem Attract-System verbinden möchten. Wenn Sie über nur eine LinkedIn-Vertragslizenz verfügen, ist dieser Schritt nicht erforderlich.

5.  Das LinkedIn-Widget lädt jetzt Ihre Administratoreinstellungen mit der Liste der angezeigten Integrationen. Klicken Sie unter **Recruiter System Connect** auf **Anfordern**.

[![Attract-Administratoransicht, um die LinkedIn Recruiter-Integration anzufordern](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)

6.  Nachdem die Integration von Attract angefordert wurde, wird es als **Bereit für Partner** angezeigt und kann über die **Recruiter-Administratoreinstellungen** aktiviert werden. Wenn **Partner benachrichtigen** auf dieser Seite angezeigt wird, warten Sie eine einige Sekunden, klicken Sie auf **Partner benachrichtigen** und aktualisieren Sie anschließend die Seite. Es sollte jetzt als **Bereit für Partner** angezeigt werden.

[![Attract-Administratoransicht, um die Attract-Seite der abgeschlossenen mit Anforderungen anzugeben](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)

Um den nächsten Schritt auszuführen, müssen Sie über das Administratorrecht für Ihren LinkedIn Recruiter-Vertrag verfügen.

7.  Melden Sie sich bei LinkedIn mithilfe des Administratorkontos an, und wechseln Sie oben rechts zu LinkedIn Recruiter. 

8. Klicken Sie im Menü **Mehr** am oberen Rand des Bildschirms auf **Administratoreinstellungen** und dann auf die Registerkarte **ATS**.

Das Attract-System wird ein mit paar Optionen aufgeführt, die aktiviert werden können.

9. Wenn Sie nur 1-Click Export für den **In-ATS-Anzeige** und das **In-ATS-Widget** aktivieren möchten, wählen Sie **Zugriff auf Firmenebene** aus. Wenn Sie alle Funktionen bei Zugriff auf Firmenebene und den InMail-Verlauf, Hinweisverlauf und den Zugriff auf das InMail-Kurzprofil aktivieren möchten, wählen Sie **Zugriff auf Vertragsebene** aus.

10. Aktivieren Sie die gewünschte Zugriffsebene in den **Administrator-ATS**-Einstellungen von LinkedIn Recruiter.

[![Einschalten der Attract-Integration aus der LinkedIn Recruiter-Administratoransicht](./media/EnableRSC.png)](./media/EnableRSC.png)

12. Kehren Sie als ein AttractAdmin zu den Attract-Administratoreinstellungen zurück und wählen Sie die Registerkarte **LinkedIn-Integration** aus. Sie sollten sehen, wie das LinkedIn-Widget geladen wird und **Aktiviert** sollte mit der ausgewählten Zugriffsebene eingeschaltet sein.

[![LinkedIn Recruiter-Integration abgeschlossen](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)

## <a name="using-linkedin-recruiter-capabilities"></a>Verwenden von LinkedIn Recruiter-Funktionen

Nachdem die LinkedIn Recruiter-Funktionen vom Attract-Administrator aktiviert wurden, ist es bereit für Zugriff durch Einstellungsmanager und Personalbeschaffer. Um diese Funktionen zu verwenden, verbinden Sie Ihr LinkedIn-Konto unter **Benutzereinstellungen**. Einige Funktionen sind verfügbar, nachdem die Administrator- und Benutzereinstellungen verbunden wurden.

### <a name="in-ats-profile-widget"></a>In-ATS-Profil-Widget

Sie können das LinkedIn-Profil des Kandidaten in Attract anzeigen. Das LinkedIn-Widget zeigt das Kandidatenprofil an, wenn die ATS-Informationen mit den LinkedIn-Informationen seiner Benutzer übereinstimmen.

Um ein Profil anzuzeigen, navigieren Sie entweder von einer Stelle oder einem Talentpool zum Kandidatenprofil. Im Kandidatenprofil wählen Sie die Registerkarte **LinkedIn** aus und das Profil-Widget wird geladen. Sie können den Kandidaten auch in Ihren LinkedIn Recruiter-Projekten von dieser Seite aus speichern.
1. Wenn LinkedIn die Übereinstimmung auf Grundlage von E-Mail und LinkedIn-Mitglied Kennung (genaue Übereinstimmung) starten, wird das Profil des Kandidaten angezeigt. Der Benutzer hat immer noch eine Option, das Profil zu verlinken/zu trennen.il.

2. Wenn LinkedIn den Kandidaten nicht auf der Grundlage ihrer E-Mail oder Mitglied Kennung gefunden werden, in dem eine Liste möglicher Kandidatenabgleichungen auf Grundlage Kandidatennamen anzeigen und der Benutzer kann eine davon auswählen und dem Profil verknüpft wird.  

3. Wenn LinkedIn keine Kandidaten auf Basis der Namen gefunden werden, wird zurückgegeben, dass keine Übereinstimmung gefunden wurde.

### <a name="1-click-export"></a>1-Click-Export 

Bei der Beschaffung von Kandidaten in LinkedIn können Sie den Kandidaten per 1-Click-Export zu der Stelle exportieren, die derzeit geöffnet ist. Führen Sie für einen 1-Click-Export 1 folgende Schritte aus. Bevor Sie diese Schritte ausführen, sollten Sie sicherstellen, dass Ihnen die Rolle des Einstellungsmanagers oder Personalbeschaffers für die Stelle zugewiesen wurde und dass die Stelle über eine Phase **Interessent** verfügt.

1.  Erstellen Sie die Stelle, weisen Sie die geeigneten Rollen zu und aktivieren Sie die Stelle.

2.  Wenn die Stelle aktiviert ist, navigieren Sie zu LinkedIn Recruiter.

3.  Suchen Sie den Kandidaten, den Sie sich wünschen und rufen Sie sein Profil auf.

4.  Mit dem Stellensuchfeld in der Kontaktkarte können Sie nach Titel oder der in Attract aktivierten Stellen-ID nach der Stelle suchen. Wenn Sie nicht die Stelle nicht finden, klicken Sie auf **ATS ändern**, um die korrekte Attract-Instanz zu suchen.

5. Nachdem die Stelle ausgewählt ist, klicken Sie auf **Exportieren**. Der Kandidat wird jetzt von Attract abgerufen.

6.  Wechseln Sie zu Attract und öffnen Sie die jeweiligen Stelle. Sie finden den Kandidaten, den Sie soeben exportiert haben, in der **Interessent**-Phase der Stelle.

### <a name="in-ats-indicator"></a>In-ATS-Anzeige 

Mit LinkedIn Recruiter können Sie nachverfolgen, ob sich ein Kandidat auf anderen Stellen in Ihrem Unternehmen beworben hat, nachsehen, in welcher Phase der Bewerbung er sich befindet und die Rückmeldung und Kommentare von Attract in LinkedIn Recruiter anzeigen.

1.  Öffnen Sie LinkedIn Recruiter und suchen Sie das Kandidatenprofil, das Sie sich wünschen.

2.  Scrollen Sie nach unten, um den Bereich **In-ATS** im Profil des Kandidaten anzeigen.

3.  Sie können dieses Widget verwenden, um in der LinkedIn Recruiter-Ansicht alle Informationen zum Kandidaten anzuzeigen, die in Attract vorhanden ist.

4.  Wählen Sie die Registerkarte **Stellen und Status** aus, um Stellen anzuzeigen, von denen sie Bestandteil sind, und wie sie bei jeder Stelle abschneiden.

5.  Wählen Sie die Registerkarte **Feedback zum Gespräch** aus, um Feedback anzuzeigen, das die Gesprächsleiter in Attract übermittelt haben.

6.  Wählen Sie die Registerkarte **Hinweise** aus, um Hinweise anzuzeigen, die für den Bewerber in Attract hinterlassen wurden.

> [!NOTE]
> Kandidaten- und Anwendungsdaten werden nicht mit LinkedIn Recruiter synchronisiert, wenn der Kandidat nicht die Interessentenphase überschritten hat.

### <a name="inmail-history"></a>InMail-Verlauf

Der LinkedIn InMail-Verlauf ist bei Zugriff auf Vertragsebene bei LinkedIn Recruiter verfügbar. Wenn er aktiviert ist, können Sie Ihren gesamten InMail-Verlauf mit dem Kandidaten anzeigen. Sie können außerdem sehen, wer sonst aus Ihrer Organisation mit dem Kandidaten per InMail korrespondiert hat. Allerdings werden diese Nachrichten nicht angezeigt.

Um den InMail-Verlauf anzuzeigen, navigieren Sie zum Profil des Kandidaten, zur Registerkarte **LinkedIn**, und scrollen Sie ans Ende der Seite, um den Verlauf anzuzeigen. Sie können einen InMail-Verlauf anzeigen, wenn Sie eine Diskussion mit dem Kandidaten hatten. Die Nachrichten aus InMail werden alle paar Stunden mit Attract synchronisiert.

### <a name="notes-history"></a>Hinweisverlauf 

Der Verlauf zu LinkedIn-Hinweisen ist mit Zugriff auf die Vertragsebene bei LinkedIn Recruiter verfügbar. Wenn er aktiviert ist, können Sie die Hinweise anzeigen, die von verschiedenen Personalbeschaffern aus Ihrer Organisation zum Kandidaten hinterlassen wurden.

Um den Hinweis-Verlauf anzuzeigen, navigieren Sie zum Profil des Kandidaten, zur Registerkarte **LinkedIn** und scrollen ans Ende der Seite, um den Verlauf anzuzeigen. Sie können alle Hinweise zum Kandidaten von LinkedIn Recruiter aus anzeigen.

### <a name="inmail-stub-profile"></a>InMail-Kurzprofil

Das InMail-Kurzprofil ist bei Zugriff auf Vertragsebene bei LinkedIn Recruiter verfügbar. Wenn Kandidaten der Freigabe ihres LinkedIn-Profilen für einen Benutzer in Ihrem Unternehmen zustimmen, können Sie die Kandidaten in Attract verfolgen und für jeden Kandidaten wird ein neuer Kandidatendatensatz erstellt. Sie können die E-Mail-Adresse des Kandidaten anzeigen, wenn der Kandidat bereits im System mit einer E-Mail-Adresse vorhanden ist oder festgelegt hat, dass die Adresse mit dem Personalbeschaffungsmitarbeiter geteilt werden kann.

Um die Kandidatenliste anzuzeigen, navigieren Sie zu **Talentpools**, um einen vom System erstellten LinkedIn-Talentpool anzuzeigen. Dieser Talentpool enthält die Liste der Kandidaten und deren Kurzprofile, wie Sie von LinkedIn empfangen wurden. Es werden der Vorname und Nachname des Kandidaten angezeigt. Die E-Mail-ID des Kandidaten wird angezeigt, wenn sich der Kandidat für die Freigabe seiner E-Mail-Adresse entschieden hat.
