---
title: Kandidaten für eine Stelle anwerben
description: Dieses Thema beschreibt, wie Sie Kandidaten in Dynamics 365 Human Resources anwerben.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ef2f2c82708fd48055faa7546e7e0c4da51e7b6c
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2022
ms.locfileid: "8733984"
---
# <a name="recruit-job-candidates"></a>Kandidaten für eine Stelle anwerben


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources hilft Ihnen bei der Verwaltung von Personalbeschaffungsanträgen. Es hilft Ihnen auch beim Übergang vom Kandidaten zum Mitarbeiter. Wenn Ihre Organisation eine separate Personalbeschaffungsanwendung verwendet, gehören zu Ihrem Personalbeschaffungsprozess möglicherweise die folgenden Schritte:<!--note from editor: Should this be a numbered list? These steps do seem to follow a particular order.-->

- Eingabe des Personalbeschaffungsantrags in Human Resources.
- Aus der Personalbeschaffungsanwendung an Human Resources weitergeleitete Kandidaten entgegennehmen.
- Den Genehmigungsprozess für Kandidaten in der Personalverwaltung abschließen.

Wenn Sie keine separate Personalbeschaffungsanwendung verwenden, können Sie Kandidaten in der Personalverwaltung auch manuell verwalten.

> [!NOTE]
> Wenn Sie Administrator oder Entwickler sind und Human Resources mit der Personalbeschaffungsanwendung eines Drittanbieters integrieren möchten, wechseln Sie zu [Dataverse-Integration konfigurieren](hr-admin-integration-common-data-service.md) und [Virtuelle Dataverse-Tabellen konfigurieren](hr-admin-integration-common-data-service-virtual-entities.md)
>
> Sie finden Personalbeschaffungsintegrations-Apps auch auf [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).
>
## <a name="enable-recruiting-requests-on-the-merged-infrastructure"></a>Personalbeschaffungsanträge auf der zusammengeführten Infrastruktur aktivieren

Wenn Sie Personalbeschaffungsanträge in der HR-Personalbeschaffung stellen möchten, müssen Sie zunächst die Funktionen **HR-Benutzererfahrung** und **Personalbeschaffungsprozessverwaltung** aktivieren.

Sobald die Funktionen aktiviert sind, wählen Sie die Funktionalität mit den folgenden Schritten aus: 
1. Gehen Sie zu **Human Resources** > **Einrichtung** > **Personalverwaltungsparameter**.
2. Legen Sie auf der Registerkarte  **Personalbeschaffung**  das Feld **Personalbeschaffung deaktiviert** auf **Nein** fest.
3. Im **Erfahrung in der Personalbeschaffung**-Dropdown wählen Sie **HR-Personalbeschaffung** aus.   

> [!Note] 
> Wenn einmal **HR-Personalbeschaffung** ausgewählt ist, wird **Personalbeschaffungsprojekte** (Legacy) schreibgeschützt. 


## <a name="add-a-recruiting-request-location"></a>Einen Standort für den Personalbeschaffungsantrag hinzufügen

Wenn Ihre Organisation mehrere Standorte hat, können Sie diese hinzufügen, damit Anforderer den Standort auswählen können, an dem der neue Mitarbeiter arbeiten soll. Der Standort wird in die Stellenausschreibung aufgenommen.

1. Geben Sie in die Suchleiste **Standort für Personalbeschaffungsantrag** ein.
2. Wählen Sie **Neu** aus.
3. Im Feld **Standort für Personalbeschaffungsantrag** geben Sie den Standortnamen ein.

    ![Einen Standort für den Personalbeschaffungsantrag hinzufügen.](./media/hr-recruit-0a-add-location.png)

4. Geben Sie für **Beschreibung** eine Beschreibung für den Standort ein.
5. Wählen Sie unter **Standort** **Hinzufügen** aus. Geben Sie die Standortadresse ein, wenn der Dialog **Neue Adresse** erscheint.<!--note from editor: Please make the address in this image less plausible. Via the fictitious guidelines on CELAweb: For street addresses, you should use sequential numbers, common street names, and incorrect zip codes (e.g., 4567 Main St Buffalo, NY 98052). (See https://microsoft.sharepoint.com/sites/CELAWeb-Copyrights-Trademarks-And-Patents/SitePages/trademarks-fictitious-names.aspx)-->

    ![Adresse eingeben.](./media/hr-recruit-0b-address.png)

6. Geben Sie unter **Kontaktinformation** die Informationen für den Kontakt des Standorts ein.
7. Wählen Sie **Speichern** aus.

## <a name="add-a-recruiting-request"></a>Einen Personalbeschaffungsantrag hinzufügen

Manager können Personalbeschaffungsanträge in Human Resources einreichen. Wenn Sie eine separate Personalbeschaffungsanwendung verwenden, können Sie mit diesen Schritten einen Personalbeschaffungsantrag senden und den Personalbeschaffungsprozess in dieser Anwendung starten. Gehen Sie andernfalls wie folgt vor, um den Workflow für Ihren eigenen internen Personalbeschaffungsprozess zu starten.

1. Wählen Sie **Mitarbeiter-Self-Service** aus.
2. Wählen Sie die Registerkarte **Mein Team** aus.
3. Wählen Sie **Antrag auf Personalbeschaffung**.

    ![Einen Personalbeschaffungsantrag starten.](./media/hr-recruit-1-request-to-recruit.png)

4. Füllen Sie die Felder **Beschreibung**, **Stelle** und **Voraussichtliches Startdatum** aus.

    ![Die Personalbeschaffungsanträge vervollständigen.](./media/hr-recruit-2-request-to-recruit.png)

5. Wählen Sie **Fortsetzen** aus. Der Personalbeschaffungsantrag für Ihre Stelle wird angezeigt.
6. Wählen Sie unter **Allgemein** einen Personalbeschaffungsmitarbeiter aus der Dropdownliste **Personalbeschaffungsmitarbeiter** und dann einen Standort aus der Dropdownliste **Personalbeschaffungsantragstandort** aus.
7. Ändern Sie unter **Stelle** alle Informationen nach Bedarf und wählen Sie dann **Details aus Stelle erstellen**.

    ![Details aus Stelle erstellen.](./media/hr-recruit-3-create-details-from-job.png)

    Der Rest des Personalbeschaffungsantrags wird mit den Standardinformationen für die von Ihnen eingegebene Stelle ausgefüllt.

8. Geben Sie unter **Externe Beschreibung** eine nach außen gerichtete Stellenbeschreibung ein.
9. Wählen Sie unter **Positionen** **Hinzufügen** aus und wählen Sie dann eine Position für diesen Personalbeschaffungsantrag aus.<!--note from editor: In all of these images, are they approved fictitious names, or do they come from sample data included with the app?-->

    ![Eine Position hinzufügen.](./media/hr-recruit-4-select-position.png)

10. Wählen Sie unter **Qualifikationen** **Hinzufügen** und dann eine Qualifikation aus.
11. Unter **Ausbildungsanforderungen** wählen Sie **Hinzufügen** und dann die Werte aus den Dropdownmenüs **Ausbildung** und **Bildungsgrad** aus.

    ![Ausbildungsanforderungen hinzufügen.](./media/hr-recruit-5-select-educational-requirements.png)

12. Fügen Sie unter **Kommentar** notwendige Kommentare ein.
13. Wählen Sie unter **Vergütung** eine Ebene aus der Dropdownliste **Ebene** aus, und passen Sie dann **Niedriger Schwellenwert**, **Kontrollpunkt** und **Hoher Schwellenwert** wie erforderlich an.
14. Wenn Ihr Personalbeschaffungsantrag fertig ist und Sie bereit sind, den Personalbeschaffungsprozess zu starten, wählen Sie in der Menüleiste **Aktivieren** aus.

    ![Personalbeschaffungsantrag aktivieren.](./media/hr-recruit-6-activate-recruit-request.png)

15. Wählen Sie **Speichern** aus.

## <a name="view-and-edit-your-recruiting-requests"></a>Personalbeschaffungsantrag auswählen und bearbeiten

Wenn Sie ein Manager sind und sich Ihre eigenen Anträge anzeigen lassen möchten:

1. Wählen Sie **Mitarbeiter-Self-Service** aus.
2. Wählen Sie die Registerkarte **Mein Team** aus.
3. Wählen Sie unter **Meine Teaminformationen** die Registerkarte **Personalbeschaffungsanträge** aus.

    ![Registerkarte Personalbeschaffungsantrag auswählen.](./media/hr-recruit-7-recruiting-requests.png)

4. Um einen Personalbeschaffungsantrag anzuzeigen oder zu bearbeiten, wählen Sie ihn im Raster aus.

Wenn Sie ein Mitarbeiter der Personalverwaltung sind und alle Personalbeschaffungsanträge anzeigen möchten:

1. Wählen Sie **Personalverwaltung** aus.
2. Wählen Sie **Personalbeschaffungsantrag** aus.

    ![Personalbeschaffungsanträge in der Personalverwaltung anzeigen.](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. Um einen Personalbeschaffungsantrag anzuzeigen oder zu bearbeiten, wählen Sie ihn im Raster aus.

## <a name="add-or-edit-a-candidate-profile"></a>Ein Kandidatenprofil hinzufügen oder bearbeiten

Wenn Ihre Organisation für die Verwaltung von Personalbeschaffungsanträge eine Integration mit einer anderen Anwendung vorgenommen hat, werden Personalbeschaffungsanträge an diese Anwendung weitergeleitet. Die Personalbeschaffungsanwendung sendet dann Kandidateninformationen zurück an die Personalverwaltung. Andernfalls können Sie Ihre eigenen internen Personalbeschaffungsprozesse nutzen und Kandidateninformationen manuell eingeben.

1. Wählen Sie **Personalverwaltung** aus.
2. Wählen Sie **Links** aus.
3. Wählen Sie unter **Personalbeschaffung** **Kandidaten** aus.

    ![Kandidaten anzeigen.](./media/hr-recruit-9-candidates.png)

4. Um einen Kandidaten hinzuzufügen, wählen Sie **Neu** aus. Um einen vorhandenen Bewerber zu bearbeiten, wählen Sie den Bewerber aus der Liste aus und klicken Sie dann auf **Bearbeiten**. Das Kandidatenprofil wird angezeigt.
5. Geben Sie unter **Kandidatenzusammenfassung** die Kandidateninformationen ein oder bearbeiten Sie sie nach Bedarf.
6. Wählen Sie unter **Personalbeschaffungsantrag** einen Personalbeschaffungsantrag aus, mit dem der Kandidat verknüpft werden soll. Füllen Sie dann die Felder **Geschätztes Startdatum**, **Zukünftiger Vorgesetzter**, **Position** und **Beschreibung** entsprechend aus.

    ![Personalbeschaffungsantrag verlinken.](./media/hr-recruit-10-link-to-recruiting-request.png)

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

1. Wählen Sie auf der Seite **Kandidat** **Einstellen** aus.

    ![Einen Kandidaten einstellen.](./media/hr-recruit-11-hire.png)

2. Füllen Sie auf der Seite **Neue Arbeitskraft einstellen** alle Felder unter **Details** aus.

    ![Details zum neuen Mitarbeiter eingeben.](./media/hr-recruit-12-hire-new-worker.png)

3. Überprüfen Sie unter **Positionsdetails** die Angaben und ändern Sie sie bei Bedarf.
4. Wählen Sie unter **Onboarding-Checklisten** die entsprechenden Onboarding-Checklisten für diesen Mitarbeiter aus.
5. Wählen Sie **Fortsetzen** aus, um den Mitarbeiterdatensatz zu erstellen.

    > [!NOTE]
    > Je nach den Workflows Ihrer Organisation durchläuft der Kandidatendatensatz möglicherweise zusätzliche Genehmigungsschritte, bevor er zum Mitarbeiterdatensatz wird.

## <a name="decide-not-to-hire-a-candidate"></a>Einen Kandidaten nicht einstellen

Wenn Sie sich entscheiden, einen Kandidaten nicht einzustellen, entfernen Sie ihn wie folgt aus dem Überprüfungsprozess. 

1. Wählen Sie auf der Seite **Kandidat** **Nicht einstellen** aus.

    ![Kandidaten nicht einstellen.](./media/hr-recruit-13-do-not-hire.png)

2. Wählen Sie einen **Ursachencode** aus und fügen Sie mögliche Kommentare hinzu.
3. Wählen Sie **OK** aus.

## <a name="dismiss-a-candidate"></a>Kandidaten entlassen

Bei Bedarf können Sie einen Kandidaten nach der Einstellung wieder entlassen. Es kann zum Beispiel sein, dass ein Kandidat Ihr Angebot ablehnt oder am ersten Tag nicht erscheint.

- Wählen Sie auf der Seite **Kandidat** **Kandidat entlassen** aus.

    ![Kandidat ablehnen.](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a>Siehe auch

[Virtuelle Dataverse-Tabellen konfigurieren](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Belegschaft organisieren](hr-personnel-departments-jobs-positions.md)<br>
[Komponenten eines Einzelvorgangs einrichten](hr-personnel-jobs.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
