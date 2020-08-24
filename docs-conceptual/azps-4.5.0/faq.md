---
title: Vanliga frågor och svar
description: Vanliga frågor och svar om Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.openlocfilehash: ac7a15121a19fa9c208163dad41b1aeed1981080
ms.sourcegitcommit: bd7edc4d48b6a8a8bec864edc876e16af0a49505
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/18/2020
ms.locfileid: "88512981"
---
# <a name="frequently-asked-questions-about-azure-powershell"></a><span data-ttu-id="6585d-103">Vanliga frågor och svar om Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="6585d-103">Frequently asked questions about Azure PowerShell</span></span>

## <a name="what-is-azure-powershell"></a><span data-ttu-id="6585d-104">Vad är Azure PowerShell?</span><span class="sxs-lookup"><span data-stu-id="6585d-104">What is Azure PowerShell?</span></span>

<span data-ttu-id="6585d-105">Azure PowerShell är en uppsättning cmdletar som du kan använda för att hantera Azure-resurser direkt med PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6585d-105">Azure PowerShell is a set of cmdlets that allows you to manage Azure resources directly with PowerShell.</span></span> <span data-ttu-id="6585d-106">Az PowerShell-modulen blev allmänt tillgänglig i december 2018.</span><span class="sxs-lookup"><span data-stu-id="6585d-106">In December 2018, the Az PowerShell module became generally available.</span></span> <span data-ttu-id="6585d-107">Den är nu den rekommenderade PowerShell-modulen för att interagera med Azure.</span><span class="sxs-lookup"><span data-stu-id="6585d-107">It's now the recommended PowerShell module for interacting with Azure.</span></span> <span data-ttu-id="6585d-108">Mer information om Az PowerShell-modulen finns i [Introduktion till den nya Azure PowerShell Az-modulen](/powershell/azure/new-azureps-module-az).</span><span class="sxs-lookup"><span data-stu-id="6585d-108">To learn more about the Az PowerShell module, see [Introducing the new Azure PowerShell Az module](/powershell/azure/new-azureps-module-az).</span></span>

## <a name="how-do-i-disable-breaking-change-warning-messages-in-azure-powershell"></a><span data-ttu-id="6585d-109">Hur gör jag för att inaktivera varningsmeddelanden om icke-bakåtkompatibla ändringar i Azure PowerShell?</span><span class="sxs-lookup"><span data-stu-id="6585d-109">How do I disable breaking change warning messages in Azure PowerShell?</span></span>

<span data-ttu-id="6585d-110">Om du inte vill att varningsmeddelanden om icke-bakåtkompatibla ändringar ska visas i Azure PowerShell måste du ange miljövariabeln `SuppressAzurePowerShellBreakingChangeWarnings` till `true`.</span><span class="sxs-lookup"><span data-stu-id="6585d-110">To suppress the breaking change warning messages in Azure PowerShell, you'll need to set the environment variable `SuppressAzurePowerShellBreakingChangeWarnings` to `true`.</span></span>

```azurepowershell
Set-Item -Path Env:\SuppressAzurePowerShellBreakingChangeWarnings -Value $true
```
