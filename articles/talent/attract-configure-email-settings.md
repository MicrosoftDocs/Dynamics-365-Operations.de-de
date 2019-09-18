---
title: Konfigurieren von E-Mail-Einstellungen in Microsoft Dynamics 365 for Talent - Attract
description: In diesem Thema wird erläutert, wie Einstellungen für E-Mail konfiguriert werden, die von Microsoft Dynamcis 365 für Talent - Attract gesendet werden.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
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
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: a8cf59064dd2f66ee50a0b0566aa712ba1f72dea
ms.sourcegitcommit: 7c49475402632069685df714546770d30804af7f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/11/2019
ms.locfileid: "1739494"
---
# <a name="configure-email-settings"></a>E-Mail-Einstellungen konfigurieren

[!include[banner](../includes/banner.md)]

Ihre Marke etabliert die Vertrauen und hilft Ihnen eine Beziehung mit Kandidaten aufzubauen, bevor sie sich auf Ihre Positionen bewerben. Positives Markenbewusstsein zieht beste Talente an und erhöht die Loyalität bestehender Mitarbeiter. Microsoft Dynamics 365 for Talent: Mit Attract können Sie E-Mails so konfigurieren, dass sie der Marke Ihres Unternehmens entsprechen. Daher können Sie Bewerbern eine konsistente Erfahrung bei deren Fortschritt durch den Bewerbungsprozess bereitstellen.

Mit Attract können Sie diese Aktivitäten ausführen:

- Konfigurieren Sie E-Mail-Einstellungen, so dass das Microsoft Exchange-E-Mail-Service-Konto Ihres Unternehmens verwendet wird. Hierdurch wissen Kandidaten, dass die E-Mails aus Ihrem Unternehmen stammen. So können Sie die Einstellungen beispielsweise so konfigurieren, dass Kandidaten E-Mails von `recruiting@contoso.com` statt von `contoso@microsoft.com`erhalten.
- Erstellen Sie ein konsistentes Branding für Ihre gesamte E-Mail-Kommunikation indem Sie erst eine globale Kopf- und Fußzeile für alle E-Mail-Vorlagen festlegen. 

> [!NOTE]
> Um Attract so zu konfigurieren, dass es das E-Mail-Service-Konto Ihres Unternehmens verwendet, um E-Mails zu senden, benötigen Sie das Einstellungs-Add-on „Comprehensive“.

## <a name="connect-an-email-service-account"></a>Anschließen eines E-Mail-Service-Kontos

Indem Sie das E-Mail-Service-Konto Ihres Unternehmens verbinden, können Sie eine Branding-E-Mail-Erfahrung für die Job-Kandidaten erstellen. Wenn Sie Ihr Unternehmenskonto nicht verbinden, verwendet Attract das Standard-Branding-E-Mail-Service-Konto von Microsoft.

1. Wählen Sie **Einstellungen** (das Zahnrad-Symbol in der rechten oberen Ecke) aus, und wählen Sie dann **Administratorcenter**.
2. Wählen Sie auf der Registerkarte **E-Mail-Einstellungen** unter **E-Mail-Service-Konten** **Ein Unternehmenskonto verbinden** aus.

    ![Verbinden des E-Mail-Service-Kontos Ihres Unternehmens in Attract](./media/attract-admin-email-service-accounts.png)

    Weitere Informationen dazu, wie Sie ein gemeinsames E-Mail-Konto erstellen, finden Sie unter [Gemeinsame Postfächer in Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).

3. Melden Sie sich im Microsoft-Anmeldungsfenster mit Ihren Unternehmensanmeldeinformationen an.
4. Wenn Sie noch kein E-Mail-Service-Konto eingerichtet haben oder wenn Sie ein neues hinzufügen möchten, wählen Sie **Neues Dienstkonto hinzufügen** aus, und geben Sie dann Ihre E-Mail-Informationen ein. Wenn Sie bereits ein E-Mail-Service-Konto eingerichtet haben, das Sie verwenden möchten, wählen Sie es aus.

Wenn Ihr E-Mail-Service-Konto erfolgreiche konfiguriert ist, wird es unter **E-Mail-Service-Konten** aufgeführt.

## <a name="disconnect-an-email-service-account"></a>Trennen eines E-Mail-Service-Kontos

Wenn Sie die Domäne Ihres Unternehmens nicht mehr in der E-Mail-Kommunikation durch Attract verwenden möchten, können Sie ein E-Mail-Service-Konto trennen.

1. Wählen Sie **Einstellungen** (das Zahnrad-Symbol in der rechten oberen Ecke) aus, und wählen Sie dann **Administratorcenter**.
2. Wählen Sie auf der Registerkarte **E-Mail-Einstellungen** unter **E-Mail-Service-Konten** die Schaltfläche **Weiter** (drei vertikale Punkte) neben dem E-Mail-Service-Konto aus, das Sie trennen möchten.
3. Wählen Sie **E-Mail-Konto trennen** aus.

    ![Trennen des E-Mail-Service-Kontos Ihres Unternehmens](./media/attract-admin-disconnect-email-account.png)

4. Wenn Sie aufgefordert werden, den Vorgang zu bestätigen, wählen Sie **Trennen** aus.

    ![Bestätigen der Trennung des E-Mail-Service-Kontos Ihres Unternehmens](./media/attract-admin-email-confirm-disconnect.png)

Wenn Sie kein anderes E-Mail-Service-Konto verbinden, verwenden E-Mails, die von Attract gesendet werden, das Standard-Branding-E-Mail-Service-Konto von Microsoft.

## <a name="configure-email-template-settings"></a>Konfigurieren von E-Mail-Vorlageeinstellungen

Sie können ein Bild des Logos Ihres Unternehmens und andere Informationen als Branding-Kopfzeile für Ihre E-Mails hochladen. Sie können auch Links zu Ihrer Datenschutzrichtlinie und den Nutzungsbedingungen in den E-Mail-Fußzeilen angeben.

> [!NOTE]
> Sie müssen alle in Ihrem Land oder Ihrer Region geltenden Gesetze sowie die im Land des E-Mail-Empfängers geltenden erfüllen. Diese Gesetze beinhalten Antispambestimmungen.

1. Wählen Sie **Einstellungen** (das Zahnrad-Symbol in der rechten oberen Ecke) aus, und wählen Sie dann **Administratorcenter**.
2. Auf der Registerkarte **E-Mail-Einstellungen** unter **Email-Vorlageneinstellungen** ziehen Sie das Bild, das Sie als Ihre E-Mail-Kopfzeile verwenden möchten in das Bildfeld, oder klicken Sie in das Bildfeld, um nach der Datei zu suchen. Um ein vorhandenes Bild zu ersetzen, müssen Sie zunächst **Entfernen** daneben auswählen. Das Bild muss eine JPEG-, JPG-, PNG- oder SVG-Datei sein. Die empfohlene Größe für Bilder liegt zwischen 25 und 800 Pixeln Breite und zwischen 25 und 150 Pixeln Höhe. Die maximale Dateigröße für die Kopfzeile ist 1 Megabyte (MB).

    ![Hinzufügen eines Bilds für die Kopfzeile der Unternehmens-E-Mail](./media/attract-admin-email-header.png)

3. Geben Sie unter **Ihre Datenschutzrichtlinie für Kommunikation** einen Link zur Datenschutzrichtlinie des Unternehmens an. Geben Sie unter **Ihre Bedingungen für Kommunikation** einen Link zu den Nutzungsbedingungen Ihres Unternehmens an.

    ![Hinzufügen von Links zur Datenschutzrichtlinie und den Nutzungsbedingungen des Unternehmens für die E-Mail-Fußzeile](./media/attract-admin-email-footer.png)

4. Wählen Sie **Speichern** aus, um Ihre E-Mail-Vorlageneinstellungen zu speichern.
