---
title: Översikt över Azure PowerShell
description: En översikt över Azure PowerShell Az-modulen med information om hur du installerar och kommer igång.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 10/29/2018
ms.openlocfilehash: 7982e122d49db4d558648231d1ab8bfeed80be2d
ms.sourcegitcommit: 4acddc7026522c4fe39de2c4424917d88ee01b7e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/21/2018
ms.locfileid: "53736468"
---
# <a name="overview-of-azure-powershell"></a>Översikt över Azure PowerShell

Azure PowerShell tillhandahåller en uppsättning cmdletar som använder [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview)-modellen för att hantera dina Azure-resurser. Azure PowerShell använder .NET Standard, vilket gör det tillgängligt för Windows, macOS och Linux.
Azure PowerShell är också tillgängligt från Azure Cloud Shell.

Använd [Cloud Shell](/azure/cloud-shell/overview) för att köra Azure PowerShell i webbläsaren eller [installera det lokalt](install-az-ps.md). Läs artikeln [Komma igång](get-started-azureps.md) om du vill lära dig grunderna i Azure PowerShell och komma igång med Azure.

Information om den senaste versionen av Azure PowerShell finns i [Viktig information](release-notes-azureps.md).

## <a name="about-the-new-az-module"></a>Om den nya Az-modulen

I den här dokumentationen beskrivs den nya Az-modulen för Azure PowerShell. Den nya modulen skrivs från grunden i .NET Standard. När .NET Standard används kan Azure PowerShell köras under PowerShell 5.x i Windows eller PowerShell 6 på valfri plattform. Az-modulen är nu rätt sätt att interagera med Azure via PowerShell.
Vi fortsätter göra felkorrigeringar i AzureRM men inga nya funktioner läggs till.

Fullständig information om den nya modulen, som nya kommandonamn och underhållsplaner för AzureRM, finns i [Introduktion till Azure PowerShell Az-modulen](new-azureps-module-az.md). Om du vill komma igång med den nya modulen direkt läser du [Migrera från AzureRM till Az](migrate-from-azurerm-to-az.md).

[AzureRM-dokumentationen](/powershell/azure/azurerm) finns också tillgänglig.

> [!IMPORTANT]
>
> Medan Azure-dokumentationen uppdateras för att återspegla de nya modul-cmdlet-namnen kan det hända att AzureRM-kommandona fortfarande används i artiklarna. När du har installerat Az-modulen rekommenderar vi att du aktiverar AzureRM-cmdlet-aliasen med `Enable-AzureRmAlias`. Mer information finns i artikeln [Migrera från AzureRM till Az](migrate-from-azurerm-to-az.md).

## <a name="common-scenarios"></a>Vanliga scenarier

Med hjälp av följande exempel kan du lära dig hur du utför vanliga scenarier med Azure PowerShell:

* [Virtuella Linux-datorer](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [Virtuella Windows-datorer](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [SQL-databaser](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="learn-powershell-basics"></a>Lär dig grunderna i PowerShell

Om du inte känner till PowerShell kan en introduktion vara till hjälp.

* [Installera PowerShell](/powershell/scripting/setup/installing-windows-powershell)
* [Köra skript med PowerShell](/powershell/scripting/powershell-scripting)

Du kan även se den här videon: [PowerShell-grunder: (Del 1) Komma igång med PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).

Eller delta i Microsoft Virtual Academy-sessionen [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart) (Snabbstart för att komma igång med PowerShell).

## <a name="build-your-skills-with-microsoft-learn"></a>Utveckla dina färdigheter med Microsoft Learn

- [Automatisera Azure-uppgifter med hjälp av skript med PowerShell](/learn/modules/automate-azure-tasks-with-powershell/)
- [Mer interaktiv inlärning...](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a>Andra Azure PowerShell-moduler

* [Azure Active Directory](/powershell/azure/active-directory/)
* [Azure Information Protection](/powershell/azure/aip/)
* [Azure Service Fabric](/powershell/azure/service-fabric/)
* [Azure ElasticDB](/powershell/azure/elasticdbjobs/)
