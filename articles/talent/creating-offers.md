---
title: Erstellen, Genehmigen und Unterschreiben von Angeboten
description: "In diesem Themas wird ausgeführt, wie Sie ein Angebot für einen Kandidaten mit Dynamics 365 for Talent erstellen, genehmigen und signieren."
author: josaw
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-10-19
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: be66d9f95551066bb8bc25445c652d4fa59066d4
ms.openlocfilehash: f189df052ef299a2cca1d92065a7a4d377d25399
ms.contentlocale: de-de
ms.lasthandoff: 12/07/2018

---

# <a name="creating-approving-and-signing-offers"></a>Erstellen, Genehmigen und Unterschreiben von Angeboten

[!include[banner](../includes/banner.md)]

In vielen Fällen muss die Vorbereitung eines Angebotspakets für einen Kandidaten ein sehr schneller Prozess sein.
Die Verwendung der Vorlage, die vom Attract-Administrator eingerichtet wurde, verringert die Zeit und den Aufwand, den die Angebotsersteller für die Vorbereitung und das Versenden von Angeboten an einen Kandidaten benötigen.

## <a name="create-an-offer"></a>Ein Angebot erstellen

Wenn die Angebotsverwaltungs-App aktiviert ist, kann jeder Benutzer mit der Rolle "Zukünftiger Vorgesetzter" oder "Personalbeschaffer" ein Angebotspaket für den Kandidaten vorbereiten. Um das Angebot vorzubereiten, gehen Sie folgendermaßen vor.

1.  Navigieren Sie zu der Stelle und der Kandidatenbewerbung, für die sie das Angebot erstellen.

1.  Navigieren Sie zu **Angebotsphase** und klicken Sie auf **Angebot vorbereiten**.

    Sie werden zur Angebot-App umgeleitet, wo der Kandidaten mit dem Status **Neu** angezeigt wird. Es werden auch andere Angebote angezeigt, an denen Sie entweder als Ersteller oder Genehmiger arbeiten.

1.  Klicken Sie auf **Angebot vorbereiten**. 
    
    Ihnen wird eine Auswahl verschiedener Angebotspakete angezeigt, die vom Administrator bereitgestellt wurden.

1.  Wählen Sie ein Paket aus und klicken Sie auf **Fertig**, um das Vorbereiten des Angebots zu starten.

    Die Angebotspaketvorlage wird mit der entsprechenden Stelle und den Kandidatendetails im Angebot vorausgefüllt geladen.

1.  Alle Angebotsdatenplatzhalter, die Teil des Angebotspakets sind, werden auf der Angebotsseite angezeigt. Sie können alle Werte im Paket auf dieser Seite auffüllen.

    Auf der Angebotsseite werden auch alle Angebotsdokumentvorlagen angezeigt, die Teil des Angebotspakets sind.

1.  Sie können nun den Inhalt des Angebots bearbeiten, je nachdem, wie die Vorlage vom Administrator konfiguriert wurde.

1.  Wenn Sie Dokumente entfernen müssen, die nicht erforderlich markiert sind, können Sie dies tun.

1. Wenn alle Angebotsdatenplatzhalter aufgefüllt wurden, klicken Sie auf **Speichern**, um einen Entwurf des Angebots zu speichern.

>[!NOTE]
> Nachdem ein Entwurf gespeichert ist, können Sie die Entwurfsversion des Angebots löschen oder gegebenenfalls eine neue Paketvorlage auswählen.


## <a name="approve-an-offer"></a>Ein Angebot genehmigen

Die meisten Angebote müssen einen Genehmigungsprozess durchlaufen, um sicherzustellen, dass das Angebot den erforderlichen Standards entspricht. Wenn ein Angebot den Standards nicht entspricht, beispielsweise wenn der Angebotsersteller die Angebotsdatenregeln nicht befolgt hat und die Werte im Angebot überschrieb, wird der Genehmigungsprozess als obligatorisch vorgegeben. Um ein Angebot zur Genehmigung zu übermitteln, gehen Sie folgendermaßen vor.

1.  Wenn sich das Angebot im Entwurfszustand befindet, fügen Sie im **Genehmigerbereich** Genehmiger hinzu. 
    >[!NOTE]
    > Zukünftige Vorgesetzte werden standardmäßig als Genehmiger hinzugefügt. Sie können einen beliebigen Benutzer aus Ihrer Organisation als Genehmiger für das Angebot auswählen.

1.  Bei Bedarf weisen Sie Genehmiger in einer sequenziellen Genehmigungsmethode oder einer parallelen Genehmigungsmethode zu. Diese Option ist nur verfügbar, wenn es so vom Administrator konfiguriert wurde.
    >[!NOTE]
    > Wenn der Genehmigungsprozess sequenziell ist, können Sie die Sequenz der Genehmiger bei Bedarf bearbeiten.

1.  Wenn Sie die Genehmigungskette definierend haben, können Sie den Inhalt der Genehmigungs-E-Mail bearbeiten und die Benachrichtigung an die Genehmiger senden. Klicken Sie auf **An Genehmiger senden**.
    >[!NOTE]
    > Wenn das Angebot nicht dem Standard entsprach, müssen Sie eine Begründung bereitstellen.

1.  Wenn der Angebotsersteller beschließt, einen Genehmiger zu überspringen, kann er einen Hinweis eingeben und zum nächsten Genehmiger springen.

Genehmiger erhält eine E-Mail mit der Bitte, das Angebot zu genehmigen. Sie können auf den Link in der E-Mail klicken, um das Angebot zu öffnen, das gesamte Angebotspaket zu überprüfen und es entweder zu genehmigen oder an den Angebotsersteller zurück zu senden. Angebotsgenehmiger müssen einen zusätzlichen Hinweis hinzufügen, wenn sie das Angebotspaket für weitere Bearbeitungen ablehnen. 

In Fällen, in denen eine neue Version des Angebots erstellt wurde, bevor der Genehmiger agiert, kann der Genehmiger das Angebot nicht genehmigen oder ablehnen.

## <a name="offer-versioning"></a>Versionsverwaltung bei Angeboten 

Wenn das Angebot bestätigt oder zur Bearbeitung zurückgesendet wurde, können Sie die Option **Bearbeitung aktivieren** auswählen, um eine neue Version des Angebots zu erstellen. Die neue Version der Angebotsversion enthält alle Angebotsdatenwerte, und die Liste der Genehmiger wird aus der letzten Version übernommen. 

Genehmiger können zwischen unterschiedlichen Angebotsversionen wechseln, wenn Ihnen die Versionen zur Genehmigung vorlagen. Ein Genehmiger oder ein Angebotsersteller kann sich auch entscheiden, eine bestimmte Entwurfsversion des Angebots zu löschen, um zum vorherigen Status zurückzukehren.


## <a name="send-an-offer-to-a-candidate"></a>Angebot an einen Kandidaten senden 

Wenn das Angebot gespeichert und genehmigt wird und an den Kandidaten gesendet werden kann, klicken Sie auf **An Kandidaten senden**.

Sie können mehrere Aktivitäten ausführen, bevor Sie dem Kandidaten das Angebot senden.
-  Sie können die Liste der Dokumente anzeigen, die Teil des Angebotspakets sind, das dem Kandidaten gesendet wird.

-  Sie können ein Angebotsablaufdatum angeben. Es wird erwartet, dass Kandidaten das Angebot vor dem Ablaufdatum annehmen oder ablehnen.  Dem Kandidaten wird 48 Stunden vor Ablauf des Angebots eine Erinnerung gesendet.

-  Es kann weitere Dokumente geben, die Sie in das Angebotsaufnahmeverfahren einbeziehen möchten. Sie haben die Möglichkeit den erforderlichen Dokumenttyp aufzuführen.

- E-Unterschriftenoption: Wenn Adobe Sign als bevorzugte E-Unterschriftmethode ausgewählt wurde, müssen sich Angebotersteller mit ihrer Adobe Sign Lizenz verbinden. Es gibt zwei Möglichkeiten, dazu. Gehen Sie zu Benutzer **Einstellungen** in **Angebot**, **Verbindungen** und verbinden Sie mit **Adobe Sign**. Alternativ werden Sie aufgefordert, das Senden-Angebot zum Kandidatenbildschirm herzustellen, wenn die Verbindung nicht bereits anhand der Benutzereinstellungen eingerichtet wurde. 

> [!NOTE]
> Benutzer müssen ihr Adobe Sign Konto nur einmal verbinden. Die gleiche Benutzerlizenz wird für alle zukünftigen Angebotpakete verwendet, die vom gleichen Benutzer gesendet werden. 

-  Sie können die E-Mail-Vorlage anzeigen und nach Bedarf bearbeiten.

Wenn das Angebot bereit ist und Sie auf **An Kandidaten senden** klicken, erhält der Kandidat eine E-Mail, dass ein Angebot zur Prüfung vorliegt.


## <a name="candidates-actions-after-receiving-an-offer"></a>Die Aktivitäten des Kandidaten nach Erhalt eines Angebots

Nachdem der Kandidat benachrichtigt wurde, dass ein Angebot für ihn freigegeben wurde, kann er auf den Link in der E-Mail klicken, um zum Bewerbungs-Dashboard zu gelangen und das Angebot anzuzeigen. Das Dashboard zeigt dem Kandidaten alle Aktivitäten, die er noch abschließen muss.

1.  Um das Angebot und alle zugehörigen Dokumente anzuzeigen, muss der Kandidat auf **Angebot anzeigen** klicken.

    Kandidaten können das Angebotspaket auch in einem .zip-Format herunterladen.

1.  Um das Angebot zu akzeptieren, muss der Kandidat für jedes Dokument, das Teil des Angebotspakets ist, auf **Zur Signatur springen** klicken.

1.  Wenn alle Dokumente einzeln signiert und akzeptiert wurden, muss der Kandidat den Annahmeprozess beenden, indem er oben auf der Seite auf **Angebot annehmen** klickt.

1.  Um das Angebot abzulehnen, muss der Kandidat oben auf der Seite auf **Angebot ablehnen** klicken, einen entsprechenden Grund auswählen, ggf. einen Kommentar hinzufügen und anschließend auf **Ablehnen** klicken.

1.  Nachdem er das Angebot akzeptiert oder abgelehnt hat, kann der Kandidat in der Angebotsansicht bleiben oder zum Bewerbungs-Dashboard zurückkehren.

1.  Wenn andere Dokumente im Rahmen des Angebotsannahmeprozesses angefordert wurden, sollte der Kandidat die Dokumente bei Bedarf hochladen und mit dem angeforderten Dokumenttyp markieren.

1.  Der Angebotsersteller wird benachrichtigt, wenn alle Dokumente hochgeladen wurden und das Angebotspaket signiert wurde.


## <a name="withdrawing-an-offer"></a>Zurückziehen eines Angebots

Ein Angebot kann von einem Kandidaten jederzeit aus verschiedenen Gründen zurückgezogen werden. 
1.  Ziehen Sie das Angebot zurück, indem Sie auf die Ellipsenschaltfläche (**…**) und auf **Angebot zurückziehen** klicken. 

2. Eine Nachricht erscheint, die fragt, ob der Kandidat über die Statusänderung informiert wurde. Wenn der Kandidat noch nicht kontaktiert wurde, haben Sie die Möglichkeit, eine E-Mail an den Kandidaten zu senden, und ihn zu informieren, dass weiteren Aktionen erforderlich sind. 

   Der Kandidaten kann nicht mehr auf das Angebot zugreifen.


## <a name="closing-an-offer"></a>Angebotsabschluss 

Wenn ein Angebot angenommen, abgelehnt oder zurückgezogen wurde, ohne dass weitere Aktionen erforderlich sind, können Sie das Angebot schließen, damit keine weitere Änderungen an diesem Angebotspaket vorgenommen werden können.

