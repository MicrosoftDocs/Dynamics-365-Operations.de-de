---
title: Einrichten eines bevorzugten Technikers
description: Sie können eine beliebige Arbeitskraft als bevorzugten Techniker für eine Servicevereinbarung oder einen Serviceauftrag auswählen.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable, SMADispatchBoard
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4c9495bbc8e5f7cb603c027a125887feba1f0e2d
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017202"
---
# <a name="set-up-a-preferred-technician"></a>Einrichten eines bevorzugten Technikers 

[!include [banner](../includes/banner.md)]


Sie können eine beliebige Arbeitskraft als bevorzugten Techniker für eine Servicevereinbarung oder einen Serviceauftrag auswählen. Es empfiehlt sich allerdings, die Arbeitskraft dem entsprechenden Einsatzteam zuzuordnen, damit sie im Modul **Einsatzplanung** berücksichtigt wird.

## <a name="assign-employee-to-a-dispatch-team"></a>Zuweisen eines Mitarbeiters zu einem Einsatzteam

1.  Klicken Sie auf **Personalverwaltung** \> **Arbeitskräfte** \> **Arbeitskräfte**. Doppelklicken Sie auf eine Arbeitskraft, um die Seite "Details zur Arbeitskraft" zu öffnen. Klicken im **Aktivitätsbereich** auf **Einstellungen** \>**Einsatzteam**, um das Formular **Arbeitskräfte disponieren** zu öffnen.

2.  Wählen Sie im Feld **Einsatzteam** das Team aus, dem die Arbeitskraft zugewiesen werden soll.

## <a name="assign-a-preferred-technician-to-a-service-agreement"></a>Zuweisen eines bevorzugten Technikers zu einer Servicevereinbarung

1.  Klicken Sie auf **Serviceverwaltung** \> **Servicevereinbarungen** \> **Servicevereinbarungen**. Doppelklicken Sie auf eine Servicevereinbarung, um das Detailformular zu öffnen.

2.  Aktivieren Sie auf der Registerkarte **Allgemein** das Kontrollkästchen **Bevorzugter Techniker**, und wählen Sie anschließend ein Mitglied des entsprechenden Einsatzteams als bevorzugten Techniker für die Servicevereinbarung aus.

## <a name="assign-a-preferred-technician-to-a-service-order"></a>Zuweisen eines bevorzugten Technikers zu einem Serviceauftrag

1.  Klicken Sie auf **Serviceverwaltung** \> **Periodisch** \> **Einsatzplanung**.
    

    > [!NOTE]
    > <P>Geben Sie im Formular <STRONG>Einsatzplanung</STRONG> einen Datumsbereich für die anzuzeigenden Einsatzaktivitäten an. Geben Sie außerdem an, ob abgeschlossene Aktivitäten angezeigt werden sollen und ob die Liste mit den Einsatzaktivitäten auf die Teams beschränkt werden soll, denen Sie selbst angehören oder die Sie selbst überwachen. Klicken Sie auf <STRONG>OK</STRONG>, um das Formular <STRONG>Einsatzplanung</STRONG> zu öffnen.</P>



2.  Wählen Sie die Position der Serviceaktivität aus, die Sie ändern möchten.

3.  Weisen Sie auf der  **Registerkarte** mithilfe der Liste **Arbeitskraft** ein Mitglied des entsprechenden Einsatzteams als bevorzugten Techniker für den Serviceeinsatz zu.

## <a name="see-also"></a>Siehe auch

[Ausarbeiten und Festsetzen von Serviceverträge – Übersicht](service-agreements.md)

[Manuelles Erstellen von Serviceaufträgen](create-service-orders-manually.md)

[Formular "Servicevereinbarungen"](https://technet.microsoft.com/library/aa617823\(v=ax.60\))
  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]