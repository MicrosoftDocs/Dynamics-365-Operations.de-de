---
title: Erstellen, Genehmigen und Unterzeichnen von Angeboten in Attract
description: In diesem Thema wird ausgeführt, wie Sie ein Angebot für einen Kandidaten mit Dynamics 365 Talent - Attract erstellen, genehmigen und unterzeichnen.
author: andreabichsel
manager: AnnBe
ms.date: 02/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-19
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: dee545b6ca5d2791dea6609b4e1b25eba128f8b7
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832906"
---
# <a name="create-approve-and-sign-offers-in-attract"></a>Erstellen, Genehmigen und Unterzeichnen von Angeboten in Attract

[!include [banner](includes/banner.md)]

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

- e-Signature-Option: Es gibt zwei Möglichkeiten, eine Verbindung mit dem e-Signature-Anbieter Ihrer Wahl herzustellen. Gehen Sie zu **Benutzereinstellungen** in **Angebot** unter **Verbindungen** und stellen Sie eine Verbindung mit **Adobe Sign** oder **DocuSign** her. Alternativ werden Sie aufgefordert, eine Verbindung mit der Seite **Angebot an den Kandidaten senden** herzustellen, wenn die Verbindung nicht bereits anhand der Benutzereinstellungen eingerichtet wurde. Das Konto für die elektronische Signaturmuss nur einmal verbunden werden. Die gleiche Benutzerlizenz wird für alle zukünftigen Angebotpakete verwendet, die vom gleichen Benutzer gesendet werden. 

### <a name="adobe-sign"></a>Adobe Sign
Wenn Adobe Sign als bevorzugte E-Unterschriftmethode ausgewählt wurde, müssen sich Angebotersteller in diesem Schritt mit ihrer Adobe Sign Lizenz verbinden. 

### <a name="docusign"></a>DocuSign
Wenn DocuSign als bevorzugte E-Unterschriftmethode ausgewählt wurde, müssen sich Angebotersteller mit ihrer DocuSign Lizenz verbinden. Einmal angemeldet werden das Standardkonto und die dem DocuSign-Profile des Benutzers zugeordneten Berechtigungen mit Talent: Attract verbunden. 

-  Sie können die E-Mail-Vorlage anzeigen und nach Bedarf bearbeiten.

Wenn das Angebot bereit ist und Sie auf **An Kandidaten senden** klicken, erhält der Kandidat eine E-Mail, dass ein Angebot zur Prüfung vorliegt.

>[!NOTE]
> Wenn Sie Adobe Sign oder DocuSign verwenden und Sie bemerken einen Fehler beim Versand des Angebots an den Kandidaten, versuchen Sie das Benutzerkonto der Elektronischen Signatur in den **Benutzereinstellungen** zu trennen und erneut zu verbinden. Wenn das Problem weiterhin besteht, wenden Sie sich über den Link **Problem melden** an unseren Support.

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
