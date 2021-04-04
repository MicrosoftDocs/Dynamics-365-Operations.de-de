---
title: Kandidaten für Stellen anwerben
description: Dieses Thema zeigt, wie Sie Kandidaten in Dynamics 365 Human Resources anwerben.
author: andreabichsel
manager: tfehr
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6aca285133495dfe023dfd18bdeb050aabcafee6
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478283"
---
# <a name="recruit-job-candidates"></a>Kandidaten für Stellen anwerben

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources hilft Ihnen bei der Verwaltung von Personalbeschaffungsanträgen. Es hilft Ihnen auch beim Übergang vom Kandidaten zum Mitarbeiter. Wenn Ihre Organisation eine separate Personalbeschaffungsanwendung verwendet, gehören zu Ihrem Personalbeschaffungsprozess möglicherweise die folgenden Schritte:

- Eingabe des Personalbeschaffungsantrags in Human Resources.
- Aus der Personalbeschaffungsanwendung an Human Resources weitergeleitete Kandidaten entgegennehmen.
- Den Genehmigungsprozess für Kandidaten in der Personalverwaltung abschließen.

Wenn Sie keine separate Personalbeschaffungsanwendung verwenden, können Sie Kandidaten in der Personalverwaltung auch manuell verwalten.

>[!NOTE]
>Wenn Sie Administrator oder Entwickler sind und Human Resources mit der Personalbeschaffungsanwendung eines Drittanbieters integrieren möchten, lesen Sie [Dataverse-Integration konfigurieren](hr-admin-integration-common-data-service.md) und [Virtuelle Dataverse-Tabellen konfigurieren](hr-admin-integration-common-data-service-virtual-entities.md)
>
> Sie finden Personalbeschaffungsintegrations-Apps auch auf [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).
>
> Informationen zum Testen unserer Vorschaufunktion für die Integration in LinkedIn Talent Hub finden Sie unter [In LinkedIn Talent Hub integrieren](hr-admin-integration-linkedin.md).

## <a name="enable-recruiting-requests"></a>Personalbeschaffungsanträge aktivieren

Wenn Sie Personalbeschaffungsanträge in Human Resources einreichen möchten, müssen Sie die Funktionalität erst in **Gemeinsame Human Resources-Parameter** aktivieren.

1. Wählen Sie im Arbeitsbereich **Personalverwaltung** die Registerkarte **Links** aus.

2. Unter **Einrichtung** wählen Sie **Freigegebene Human Resources-Parameter** aus.

3. Setzen Sie in der Registerkarte **Personalbeschaffung** unter **PERSONALBESCHAFFUNG** **Personalbeschaffungsanträge aktivieren** auf **Ja**.

## <a name="add-a-recruiting-request-location"></a>Einen Standort für den Personalbeschaffungsantrag hinzufügen

Wenn Ihre Organisation mehrere Standorte hat, können Sie diese hinzufügen, damit Anforderer den Standort auswählen können, an dem der neue Mitarbeiter arbeiten soll. Der Standort wird in die Stellenausschreibung aufgenommen.

1. Geben Sie in die Suchleiste **Standort für Personalbeschaffungsantrag** ein.

2. Wählen Sie **Neu** aus.

3. Im Feld **Standort für Personalbeschaffungsantrag** geben Sie den Standortnamen ein.

   ![Einen Standort für den Personalbeschaffungsantrag hinzufügen](./media/hr-recruit-0a-add-location.png)

4. Geben Sie im Feld **Beschreibung** eine Beschreibung für den Standort ein.

5. Wählen Sie unter **Standort** **Hinzufügen** aus. Geben Sie die Standortadresse ein, wenn das Popout **Neue Adresse** erscheint.

   ![Adresse eingeben](./media/hr-recruit-0b-address.png)

6. Geben Sie unter **Kontaktinformation** die Informationen für den Kontakt des Standorts ein.

7. Wählen Sie **Speichern** aus.

## <a name="add-a-recruiting-request"></a>Einen Personalbeschaffungsantrag hinzufügen

Manager können Personalbeschaffungsanträge in Human Resources einreichen. Wenn Sie eine separate Personalbeschaffungsanwendung verwenden, können Sie mit diesen Schritten einen Personalbeschaffungsantrag senden und den Personalbeschaffungsprozess in dieser Anwendung starten. Gehen Sie andernfalls wie folgt vor, um den Workflow für Ihren eigenen internen Personalbeschaffungsprozess zu starten.

1. Wählen Sie **Mitarbeiter-Self-Service** aus.

2. Wählen Sie die Registerkarte **Mein Team** aus.

3. Wählen Sie **Antrag auf Personalbeschaffung**.

   ![Einen Personalbeschaffungsantrag starten](./media/hr-recruit-1-request-to-recruit.png)

4. Füllen Sie die Felder **Beschreibung**, **Stelle** und **Voraussichtliches Startdatum** aus.

   ![Die Personalbeschaffungsanträge vervollständigen](./media/hr-recruit-2-request-to-recruit.png)

5. Wählen Sie **Fortsetzen** aus. Der Personalbeschaffungsantrag für Ihre Stelle wird angezeigt.

6. Wählen Sie unter **Allgemein** einen Personalbeschaffungsmitarbeiter aus der Dropdownliste **Personalbeschaffungsmitarbeiter** und dann einen Standort aus der Dropdownliste **Standort für Personalbeschaffungsantrag** aus.

7. Ändern Sie unter **Stelle** alle Informationen nach Bedarf und wählen Sie dann **Details aus Stelle erstellen**.

   ![Details aus Stelle erstellen](./media/hr-recruit-3-create-details-from-job.png)

   Der Rest des Personalbeschaffungsantrags wird mit den Standardinformationen für die von Ihnen eingegebene Stelle automatisch ausgefüllt.

8. Geben Sie unter **Externe Beschreibung** eine nach außen gerichtete Stellenbeschreibung ein.

9. Wählen Sie unter **Positionen** **Hinzufügen** aus und wählen Sie dann eine Position für diesen Personalbeschaffungsantrag aus.

   ![Eine Position hinzufügen](./media/hr-recruit-4-select-position.png)

10. Wählen Sie unter **Qualifikationen** **Hinzufügen** und dann eine Qualifikation aus.

11. Unter **Ausbildungsanforderungen** wählen Sie **Hinzufügen** und dann die Werte aus den Dropdownlisten **Ausbildung** und **Bildungsgrad** aus.

   ![Ausbildungsanforderungen hinzufügen](./media/hr-recruit-5-select-educational-requirements.png)

12. Fügen Sie unter **Kommentar** notwendige Kommentare ein.

13. Wählen Sie unter **Vergütung** eine Ebene aus der Dropdownliste **Ebene** aus und passen Sie dann den **Niedrigen Schwellenwert**, den **Kontrollpunkt** und den **Hohen Schwellenwert** wie erforderlich an.

14. Wenn Ihr Personalbeschaffungsantrag fertig ist und Sie bereit sind, den Personalbeschaffungsprozess zu starten, wählen Sie in der Menüleiste **Aktivieren** aus.

   ![Personalbeschaffungsantrag aktivieren](./media/hr-recruit-6-activate-recruit-request.png)

15. Wählen Sie **Speichern** aus.

## <a name="view-and-edit-your-recruiting-requests"></a>Personalbeschaffungsantrag auswählen und bearbeiten

Wenn Sie ein Manager sind und sich Ihre eigenen Anträge anzeigen lassen möchten:

1. Wählen Sie **Mitarbeiter-Self-Service** aus.

2. Wählen Sie die Registerkarte **Mein Team** aus.

3. Wählen Sie unter **Meine Teaminformationen** die Registerkarte **Personalbeschaffungsanträge** aus.

   ![Registerkarte Personalbeschaffungsantrag auswählen](./media/hr-recruit-7-recruiting-requests.png)

4. Um einen Personalbeschaffungsantrag anzuzeigen oder zu bearbeiten, wählen Sie ihn im Raster aus.

Wenn Sie ein Mitarbeiter der Personalverwaltung sind und alle Personalbeschaffungsanträge anzeigen möchten:

1. Wählen Sie **Personalverwaltung** aus.

2. Wählen Sie **Personalbeschaffungsantrag** aus.

   ![Personalbeschaffungsanträge in der Personalverwaltung anzeigen](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. Um einen Personalbeschaffungsantrag anzuzeigen oder zu bearbeiten, wählen Sie ihn im Raster aus.

## <a name="add-or-edit-a-candidate-profile"></a>Ein Kandidatenprofil hinzufügen oder bearbeiten

Wenn Ihre Organisation für die Verwaltung von Personalbeschaffungsanträge eine Integration mit einer anderen Anwendung vorgenommen hat, werden Personalbeschaffungsanträge an diese Anwendung weitergeleitet. Die Personalbeschaffungsanwendung sendet dann Kandidateninformationen zurück an die Personalverwaltung. Andernfalls können Sie Ihre eigenen internen Personalbeschaffungsprozesse nutzen und Kandidateninformationen manuell eingeben.

1. Wählen Sie **Personalverwaltung** aus.

2. Wählen Sie **Links** aus.

3. Wählen Sie unter **Personalbeschaffung** **Kandidaten** aus.

   ![Kandidaten anzeigen](./media/hr-recruit-9-candidates.png)

4. Um einen Kandidaten hinzuzufügen, wählen Sie **Neu** aus. Um einen vorhandenen Bewerber zu bearbeiten, wählen Sie den Bewerber aus der Liste aus und klicken Sie dann auf **Bearbeiten**. Das Kandidatenprofil wird angezeigt.

5. Geben Sie unter **Kandidatenzusammenfassung** die Kandidateninformationen ein oder bearbeiten Sie sie nach Bedarf.

6. Wählen Sie unter **Personalbeschaffungsantrag** einen Personalbeschaffungsantrag aus, mit dem der Kandidat verknüpft werden soll. Füllen Sie dann die Felder **Voraussichtliches Startdatum**, **Zukünftiger Vorgesetzter**, **Position** und **Beschreibung** entsprechend aus.

   ![Personalbeschaffungsantrag verlinken](./media/hr-recruit-10-link-to-recruiting-request.png)

7. Füllen Sie alle Informationen in den folgenden Bereichen aus, die Sie in den Datensatz des Bewerbers aufnehmen möchten:
   - **Kommentare**
   - **Berufserfahrung**
   - **Kontaktinformationen**
   - **Ausbildung**
   - **Qualifikationen**
   - **Bescheinigungen**
   - **Prüfungen**

8. Wählen Sie **Speichern** aus.

## <a name="hire-a-candidate"></a>Einen Kandidaten einstellen

Wenn Sie bereit sind, einen Kandidaten einzustellen, machen Sie den Kandidaten wie folgt zum Mitarbeiter.

1. Wählen Sie im Kandidatenformular **Einstellen** aus.

   ![Einen Kandidaten einstellen](./media/hr-recruit-11-hire.png)

2. Füllen Sie im Formular **Neue Arbeitskraft einstellen** alle Felder unter **Details** aus.

   ![Details zum neuen Mitarbeiter eingeben](./media/hr-recruit-12-hire-new-worker.png)

3. Überprüfen Sie unter **Positionsdetails** die Angaben und ändern Sie sie bei Bedarf.

4. Wählen Sie unter **Onboarding-Checklisten** die entsprechenden Onboarding-Checklisten für diesen Mitarbeiter aus.

5. Wählen Sie **Fortsetzen** aus, um den Mitarbeiterdatensatz zu erstellen.

   >[!NOTE]
   >Je nach den Workflows Ihrer Organisation durchläuft der Kandidatendatensatz zusätzliche Genehmigungsschritte, bevor er zum Mitarbeiterdatensatz wird.

## <a name="decide-not-to-hire-a-candidate"></a>Einen Kandidaten nicht einstellen

Wenn Sie sich entscheiden, einen Kandidaten nicht einzustellen, entfernen Sie ihn wie folgt aus dem Überprüfungsprozess. 

1. Wählen Sie im Kandidatenformular **Nicht einstellen** aus.

   ![Kandidaten nicht einstellen](./media/hr-recruit-13-do-not-hire.png)

2. Wählen Sie einen **Ursachencode** aus und fügen Sie mögliche Kommentare hinzu.

3. Wählen Sie **OK**.

## <a name="dismiss-a-candidate"></a>Kandidaten entlassen

Bei Bedarf können Sie einen Kandidaten nach der Einstellung wieder entlassen. Es kann zum Beispiel sein, dass ein Kandidat Ihr Angebot ablehnt oder am ersten Tag nicht erscheint.

- Wählen Sie im Kandidatenformular **Kandidat entlassen** aus.

  ![Kandidat ablehnen](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a>Siehe auch

[Virtuelle Dataverse-Tabellen konfigurieren](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Belegschaft organisieren](hr-personnel-departments-jobs-positions.md)<br>
[Komponenten eines Einzelvorgangs einrichten](hr-personnel-jobs.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
