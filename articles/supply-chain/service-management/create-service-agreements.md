---
title: Erstellen von Servicevereinbarungen
description: In diesem Thema wird beschrieben, wie mithilfe der Funktionen in den Modulen Servicemanagement und Projektmanagement und Buchhaltung Serviceverträge erstellt werden.
author: ShylaThompson
manager: tfehr
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f883d5b312c042a995e30998fc24da5b1c02f22a
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470856"
---
# <a name="create-service-agreements"></a>Erstellen von Servicevereinbarungen

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie mithilfe der Funktionen in den Modulen Servicemanagement und Projektmanagement und Buchhaltung Serviceverträge erstellt werden.

## <a name="create-a-service-agreement-from-service-management"></a>Erstellen eines Servicevertrags aus der Serviceverwaltung

1. Navigieren Sie zu **Serviceverwaltung**.
2. Wählen Sie **Servicevereinbarungen**, um eine neue Zeile für Servicevereinbarungen in der Kopfzeile der Seite zu erstellen. 
3. Wählen Sie **Neu** aus. Geben Sie eine Beschreibung ein, wählen Sie einen Verweis auf ein **Projekt-ID** im Feld  aus, und füllen Sie die restlichen Felder und Positionen für den Servicevertrag aus. Wählen Sie **Speichern** aus.
4. Klicken Sie auf die Registerkarte ,**Beziehung** und wählen Sie Erstellen von **Serviceobjektbeziehungen** oder **Serviceaufgabenbeziehungen** für den Servicevertrag Die Serviceobjekte und -aufgaben, für die eine Beziehung erstellt wurden, können den Positionen der Servicevereinbarung zugeordnet werden.
5. Erstellen Sie Servicevereinbarungspositionen in der unteren Hälfte des Formulars , indem Sie Positionen aus einer Servicevorlage oder aus einer anderen Servicevereinbarung kopieren, oder erstellen Sie die Servicevereinbarungspositionen manuell.

> [!NOTE]
> Beim Kopieren von Positionen aus einer anderen Servicevereinbarung kann angegeben werden, ob auch die Serviceobjekt- und die Serviceaufgabenbeziehungen kopiert werden sollen. Werden diese Beziehungen kopiert, werden sie den für die Servicevereinbarung möglicherweise bereits vorhandenen Beziehungen hinzugefügt. Beim Kopieren von Servicevereinbarungspositionen aus einer Servicevorlage werden die Serviceobjekt- sowie die Serviceaufgabenbeziehungen automatisch entsprechend in die neuen Servicevereinbarungspositionen kopiert.

## <a name="create-service-agreement-lines-manually"></a>Manuelles Erstellen von Servicevertragspositionen

1. Fügen Sie im Formular **Servicevereinbarungen** eine Servicevertragsposition im Raster  hinzu. 
2. Geben Sie die für die Servicevereinbarungsposition erforderlichen Informationen ein. 
3. Wählen Sie **Speichern**, um die Zeile zu speichern, und schließen Sie dann die Seite.

## <a name="create-a-service-agreement-from-project"></a>Erstellen einer Servicevereinbarung mithilfe des Moduls "Projekt"

1. Wählen Sie **Projektverwaltung und Buchhaltung**.
2. Wählen Sie **Alle Projekte**.
3. Wählen Sie in der Liste ein Projekt aus.
4. Wählen Sie im **Aktivitätsbereich** die Option **Verwalten**. Wählen Sie in der Gruppe **Neue** Aktion **Service** und wählen Sie **Servicesvereinbarung**.
5. Führen Sie die Schritte im Abschnitt **Erstellen eines Servicevertrags** aus der Serviceverwaltung" (siehe vorheriger Kommentar in diesem Thema) aus.


## <a name="related-topics"></a>Verwandte Themen

[Ausarbeiten und Festsetzen von Serviceverträge – Übersicht](service-agreements.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]