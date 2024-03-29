---
title: Serviceobjektbeziehungen
description: Zwischen einem Serviceobjekt und einer Servicevereinbarung oder einem Serviceauftrag können Serviceobjektbeziehungen erstellt werden.
author: sorenva
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 831db29589826904666049edbc8be0c38e1d02a5
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676634"
---
# <a name="service-object-relations"></a>Serviceobjektbeziehungen 

[!include [banner](../includes/banner.md)]

Zwischen einem Serviceobjekt und einer Servicevereinbarung oder einem Serviceauftrag können Serviceobjektbeziehungen erstellt werden. Durch Erstellen einer Beziehung wird das Serviceobjekt der Servicevereinbarung oder dem Serviceauftrag zugeordnet.

Nach Erstellung der Beziehung kann das Serviceobjekt den Positionen einer Servicevereinbarung oder eines Serviceauftrags zugeordnet werden.

## <a name="template-boms"></a>Vorlagenstücklisten

Für die Objektbeziehung kann auch eine Vorlagenstückliste angegeben werden. Bei der Vorlagenstückliste handelt es sich um eine Stückliste für das Objekt, für die Leistung erbracht wird. Wird während eines Servicebesuchs eine Komponente des Serviceobjekts ausgetauscht, können Sie diese Änderung mithilfe des Formulars Serviceobjekte in der Servicestückliste erfassen.

## <a name="example"></a>Beispiel

Sie erstellen eine Servicevereinbarung für die Wartung zweier Aufzüge am Standort des Debitors.
Die Servicevereinbarung hat den Bezeichner "ID SAL-001".

Die Aufzüge wurden im Formular Serviceobjekte als Objekte mit der Bezeichnung "EL-S/1000" und "EL-L/1000" eingerichtet.

Die Serviceobjekte ("EL-S/1000" und "EL-L/1000") werden der Servicevereinbarung zugeordnet.

Da Änderungen, die sich durch den Austausch von Komponenten des Serviceobjekts ergeben, in der Stückliste für das Serviceobjekt erfasst werden sollen, ordnen Sie der Serviceobjektbeziehung eine Servicestückliste zu. Weitere Informationen hierzu finden Sie in der folgenden Tabelle:

| Serviceobjekt | Beziehung – Servicevereinbarung | Servicestückliste   |
|----------------|------------------------------|---------------|
| EL-S/1000      | ID SAL-001                   | BOM-EL-S/1000 |
| EL-L/1000      | ID SAL-001                   | BOM-EL-L/1000 |

Da für die Vereinbarung Serviceobjektbeziehungen vorhanden sind, lassen sich nun Vereinbarungspositionen mit diesen Objekten erstellen. Weitere Informationen hierzu finden Sie in der folgenden Tabelle:

| Buchungstyp | Kategorie           | Serviceobjekt |
|------------------|--------------------|----------------|
| Stunde             | Prüfung         | EL-S/1000      |
| Stunde             | Reinigung des Getriebes  | EL-S/1000      |
| Artikel             | Reinigungsmaterial | EL-S/1000      |
| Stunde             | Prüfung         | EL-L/1000      |
| Stunde             | Reinigung des Getriebes   | EL-L/1000      |
| Artikel             | Reinigungsmaterial | EL-L/1000      |

Bei einem Servicebesuch muss beim Aufzug "EL-S/1000" ein Austausch des Getriebes vorgenommen werden. Rufen Sie mithilfe der für die aktuelle Servicevereinbarung eingerichteten Serviceobjektbeziehung den Stücklisten-Designer auf, um eine Komponente des Objekts auszutauschen.

Aufrufen des Stücklisten-Designers mithilfe einer Serviceobjektbeziehung

1. Serviceverträge
2. Doppelklicken Sie auf einen Servicevertrag, oder klicken Sie auf , um einen neuen Servicevertrag zu erstellen.
3. Klicken Sie auf die Registerkarte "Einstellungen".
4. Klicken Sie auf Serviceobjekte und anschließend auf Stückliste, um der Servicevereinbarung eine Vorlagenstückliste hinzuzufügen.
5. Klicken Sie zum Öffnen des Formulars Serviceobjekte im Formular Designer auf Designe und aktualisieren Sie die Vorlagenstückliste.

## <a name="automatically-created-service-orders"></a>Automatisch erstellte Serviceaufträge

Werden Serviceaufträge für eine Servicevereinbarung automatisch erstellt, werden die Serviceobjektbeziehungen aus der Vereinbarung auch in den Serviceaufträgen erstellt.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]