---
title: Integration von Servicevereinbarungen und Projekten
description: 'Bei der Arbeit mit Servicevereinbarungen und Servicevereinbarungspositionen werden Daten aus den folgenden Bereichen des Moduls Projektverwaltung und -buchhaltung verwendet:'
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd0a7de17e8ff098220fd183b714b77225cc217f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247309"
---
# <a name="integration-for-service-agreements-and-projects"></a>Integration von Servicevereinbarungen und Projekten 

[!include [banner](../includes/banner.md)]


Bei der Arbeit mit Servicevereinbarungen und Servicevereinbarungspositionen werden Daten aus den folgenden Bereichen des Moduls **Projektverwaltung und -buchhaltung** verwendet:

## <a name="project-prices"></a>Projektpreise

Der Einstands- und der Verkaufspreis für eine Servicevereinbarungsbuchung werden aus den Einstandspreiseinstellungen abgeleitet, die für das Projekt gelten, das der Servicevereinbarung zugeordnet ist. Einstands- und Verkaufspreis können für ein Projekt, für einen Mitarbeiter oder für eine Kategorie eingerichtet werden. 

## <a name="project-validation"></a>Projektprüfung

Die Projekte, Mitarbeiter und Kategorien, die in einer Servicevereinbarungsposition zur Auswahl stehen, können mithilfe der Prüfungseinstellungen im Modul **Projektverwaltung und -buchhaltung** eingeschränkt werden. Die Prüfungseinstellungen ermöglichen das Kombinieren von Mitarbeitern, Projekten und Kategorien für die Zugriffsteuerung. 

## <a name="project-line-properties"></a>Projektpositionseigenschaften

Servicevereinbarungspositionen werden automatisch mit einem Abrechnungscode versehen.

Abrechnungscodes werden im Modul **Abrechnungscodes** im Formular **Projektverwaltung und -buchhaltung** erstellt. Der für eine Servicevereinbarung eingegebene Abrechnungscode ist dem Projekt zugeordnet, das für die Servicevereinbarung ausgewählt ist, und wird in der Servicevereinbarungsposition übernommen. 

## <a name="default-offset-accounts"></a>Standardgegenkonten

Wenn Sie eine Ausgabenbuchung eingeben, wird für die Buchung automatisch ein standardmäßiges Ausgabengegenkonto ausgewählt. Das standardmäßige Ausgabenkonto wird für das Projekt eingerichtet, das der aktuellen Servicevereinbarung zugeordnet ist.

## <a name="project-categories"></a>Projektkategorien

Die Kategorien, die für die Servicevereinbarungspositionen zur Verfügung stehen, werden im Bereich **Projektkategorien** im Formular **Projektverwaltung und -buchhaltung** eingerichtet. 

> [!NOTE]
> <P>Kategorien, bei denen im Formular <STRONG>Projektkategorien</STRONG> auf der Registerkarte <STRONG>Projekt</STRONG> das Kontrollkästchen <STRONG>Aktiv in Erfassungen</STRONG> aktiviert ist, können ausgewählt werden. Ist dagegen im Formular <STRONG>Projektverwaltungs- und -verrechnungsparameter</STRONG> auf der Registerkarte <STRONG>Erfasssungen</STRONG> das Kontrollkästchen <STRONG>Inaktive Kategorien</STRONG> aktiviert, stehen alle Kategorien zur Auswahl.</P>

## <a name="project-parameters"></a>Projektparameter

Wenn das Feld **Ausgeschiedene Arbeitskräfte** auf der Registerkarte **Erfassungen** im Formular **Projektverwaltungs- und Buchhaltungsparameter** aktiviert wird, können sowohl aktive als auch inaktive Mitarbeiter Mitarbeiter in den Formularen **Serviceverträge** und **Serviceaufträge** auswählen.

Darüber hinaus können Sie im Formular **Serviceaufträge** auf der Registerkarte **Projekt** die Kontrollkästchen **Startzeit** und **Endzeit** aktivieren, um in den Serviceauftragspositionen eine Start- und eine Endzeit einzugeben.

## <a name="enable-the-starting-and-ending-time-feature-for-service-orders"></a>Aktivieren der Funktion für die Start- und Endzeit von Serviceaufträgen

1.  Klicken Sie auf **Projektverwaltung und Buchhaltung** \> **Setup** \> **Projektverwaltungs- und Buchhaltungsparameter**.

2.  Klicken Sie auf die Registerkarte **Erfassungen**, und aktivieren Sie dann das Kontrollkästchen **Start-/Endzeiten anzeigen**.

3.  Klicken auf **Projektverwaltung und -buchhaltung** \> **Einrichtung** \> **Erfassungen** \> **Erfassungsnamen**

4.  Wählen Sie das Journal aus, das dem Serviceauftrag zugeordnet ist.

5.  Klicken Sie auf die Registerkarte **Allgemein**, und aktivieren Sie dann das Kontrollkästchen **Start-/Endzeiten anzeigen**.


> [!NOTE]
> <P>wählen Sie den Erfassungnamen für den Serviceauftragen im Feld <STRONG>Stunde</STRONG> auf der Registerkarte <STRONG>Erfassungen</STRONG> im Formular <STRONG>Serviceverwaltungsparameter</STRONG>.</P>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]