---
title: Persönliche Daten bearbeiten
description: In diesem Artikel wird beschrieben, wie Sie persönliche Informationen im Self-Service für Mitarbeiter und Manager bearbeiten.
author: andreabichsel
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 80b4537601491c97c24cfa1fef5088cbf1ac276df76534034117161b0fe79dc2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715894"
---
# <a name="edit-personal-information"></a>Persönliche Daten bearbeiten

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Sie können Ihre persönlichen Daten in Dynamics 365 Human Resources im **Self-Service-Arbeitsbereich für Mitarbeiter** bearbeiten.

Die persönlichen Informationen, die Sie bearbeiten können, umfassen:

- Adressen
- Kontaktdetails
- Persönliche Kontakte
- Kennnummern
- Zahlungsweise
- In Human Resources verwendetes Bild

>[!NOTE]
>Möglicherweise können Sie bestimmte Arten von persönlichen Informationen nicht bearbeiten, z. B. geschäftliche Kontaktdaten. Weitere Informationen finden Sie unter [Bearbeiten von persönlichen Informationen einschränken](hr-employee-self-service-restrict-editing.md).

Die im globalen Adressbuch festgelegten Parameter bestimmen die Rollen, in denen Ihre persönlichen Daten angezeigt werden können.

1. Wählen Sie in der Personalabteilung **Mitarbeiter-Self-Service** aus.

2. Wählen Sie **Persönliche Daten bearbeiten** aus.

3. Um Ihre Adresse zu ändern, wählen Sie die Registerkarte **Adressen** aus. Von Ihnen vorgenommene Änderungen werden im Arbeitsbereich **Personalmanagement** zur Alarmierung von HR angezeigt.

    - Wählen Sie zum Hinzufügen einer neuen Adresse **Hinzufügen** aus.
    - Um eine vorhandene Adresse zu bearbeiten, wählen Sie die Adresse aus und wählen Sie dann **Bearbeiten**.
    - Um eine Karte anzuzeigen, wählen Sie **Karte** aus.
    - Wählen Sie zum Hinzufügen oder Entfernen eines Kontakts **Weitere Optionen** und dann **Erweitert** aus. Wählen Sie unter **Kontaktinformationen** **Hinzufügen** oder **Entfernen** aus und bearbeiten Sie die Felder nach Bedarf.
    - Wählen Sie zum Festlegen Ihrer Zeitzone und Ihres Standorts **Weitere Optionen** und dann **Erweitert** aus. Bearbeiten Sie unter **Allgemeines** die Felder nach Bedarf.

4. Um Ihre Kontaktdaten zu ändern, wählen Sie die Registerkarte **Kontaktdetails** aus. Sie können verschiedene Arten von Kontaktinformationen bereitstellen, einschließlich Telefonnummer, E-Mail und Social Media-Links. Sie können ein Kontaktdetail als primär festlegen, aber Sie können nur eines von jedem Typ als primär festlegen.

    - Wählen Sie zum Hinzufügen einer neuen Kontaktinformation **Hinzufügen** aus. Bearbeiten Sie die Felder wie gewünscht.
    - Um eine vorhandene Kontaktinformation zu bearbeiten, wählen Sie das Element aus und wählen Sie dann **Bearbeiten**. Bearbeiten Sie die Felder wie gewünscht.
    - Um ein Kontaktdetail als privat festzulegen, wählen Sie das Element aus und wählen Sie **Erweitert** und stellen Sie dann die Option **Privat** auf **Ja** um. Wählen Sie **OK**.
      >[!NOTE]
      >Die Schaltfläche **Erweitert** ist nicht verfügbar, wenn Ihr Admin in Ihrer Umgebung die Funktion **(Vorschau) Mitarbeiter vom Hinzufügen oder Bearbeiten von Adress- und Kontaktinformationen für ausgewählte Zwecke ausschließen** aktiviert hat. Weitere Informationen finden Sie unter [Bearbeiten von persönlichen Informationen einschränken](hr-employee-self-service-restrict-editing.md).
  
5. Um Ihre persönlichen Kontakte zu ändern, wählen Sie die Registerkarte **Persönliche Kontakte** aus. Sie können Notfallkontakte, Begünstigte und abhängige Personen festlegen. Ein Kontakt kann eine Person oder eine Organisation sein. Die Funktion **Vorteilsverwaltung** verwendet persönliche Kontaktinformationen. Weitere Informationen finden Sie unter [Berechtigungsoptionen für persönliche Kontakte konfigurieren](hr-benefits-setup-contact-eligibility-options.md).

6. Um Ihre Identifikationsnummern wie die Sozialversicherungsnummer zu ändern, wählen Sie die Registerkarte **Identifikationsnummern** aus. Änderungen werden möglicherweise genehmigt, wenn Ihre Organisation einen Genehmigungsworkflow eingerichtet hat.

    - Um eine Identifikationsnummer hinzuzufügen, wählen Sie **Neu**. Füllen Sie die Felder nach Bedarf aus und wählen Sie **Speichern**.
    - Um eine Nummer zu bearbeiten, wählen Sie **Bearbeiten**. Bearbeiten Sie die Felder nach Bedarf aus und wählen Sie **Speichern**.

7. Um die Methoden zu ändern, mit denen Sie bezahlt werden, wählen Sie die Regiserkarte **Meine Zahlungsinformationen** aus. Diese Registerkarte ist nur verfügbar, wenn Zahlungsmethoden im Formular **Personalparameter** aktiviert sind. HR kann **Bankwechsel**, **Bargeld**, **Scheck**, **Elektronische Zahlung**, oder **Sonstige** aktivieren. HR kann auch die elektronische Zahlungsvalidierung (die für die US-Lohn- und Gehaltsabrechnung verwendet wird) sowie die Validierung von Bankkonten und Bankleitzahlen deaktivieren.

8. Um das Bild zu ändern, das in der Personalabteilung für Ihr Profil angezeigt wird, wählen Sie die Registerkarte **Bild** aus. Abhängig von den Einstellungen Ihres Unternehmens werden Bilder möglicherweise zur Genehmigung weitergeleitet.

    - Um ein Bild hochzuladen, wählen Sie **Neues Bild hochladen**.
    - Um ein Bild zu entfernen, wählen Sie das Bild aus und wählen Sie dann **Entfernen**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]