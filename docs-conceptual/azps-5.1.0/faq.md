---
title: Vanliga frågor och svar (FAQ)
description: Vanliga frågor och svar om Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 10ed859f04fa29d866530af71c32819b256c882a
ms.sourcegitcommit: d81c3b0f0f7289104be03869eb675128b61db7d3
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/17/2020
ms.locfileid: "94715710"
---
# <a name="frequently-asked-questions-about-azure-powershell"></a><span data-ttu-id="89f36-103">Vanliga frågor och svar om Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="89f36-103">Frequently asked questions about Azure PowerShell</span></span>

## <a name="what-is-azure-powershell"></a><span data-ttu-id="89f36-104">Vad är Azure PowerShell?</span><span class="sxs-lookup"><span data-stu-id="89f36-104">What is Azure PowerShell?</span></span>

<span data-ttu-id="89f36-105">Azure PowerShell är en uppsättning cmdletar som du kan använda för att hantera Azure-resurser direkt med PowerShell.</span><span class="sxs-lookup"><span data-stu-id="89f36-105">Azure PowerShell is a set of cmdlets that allows you to manage Azure resources directly with PowerShell.</span></span> <span data-ttu-id="89f36-106">Az PowerShell-modulen blev allmänt tillgänglig i december 2018.</span><span class="sxs-lookup"><span data-stu-id="89f36-106">In December 2018, the Az PowerShell module became generally available.</span></span> <span data-ttu-id="89f36-107">Den är nu den rekommenderade PowerShell-modulen för att interagera med Azure.</span><span class="sxs-lookup"><span data-stu-id="89f36-107">It's now the recommended PowerShell module for interacting with Azure.</span></span> <span data-ttu-id="89f36-108">Mer information om Az PowerShell-modulen finns i [Introduktion till den nya Azure PowerShell Az-modulen](/powershell/azure/new-azureps-module-az).</span><span class="sxs-lookup"><span data-stu-id="89f36-108">To learn more about the Az PowerShell module, see [Introducing the new Azure PowerShell Az module](/powershell/azure/new-azureps-module-az).</span></span>

## <a name="how-do-i-disable-breaking-change-warning-messages-in-azure-powershell"></a><span data-ttu-id="89f36-109">Hur gör jag för att inaktivera varningsmeddelanden om icke-bakåtkompatibla ändringar i Azure PowerShell?</span><span class="sxs-lookup"><span data-stu-id="89f36-109">How do I disable breaking change warning messages in Azure PowerShell?</span></span>

<span data-ttu-id="89f36-110">Om du inte vill att varningsmeddelanden om icke-bakåtkompatibla ändringar ska visas i Azure PowerShell måste du ange miljövariabeln `SuppressAzurePowerShellBreakingChangeWarnings` till `true`.</span><span class="sxs-lookup"><span data-stu-id="89f36-110">To suppress the breaking change warning messages in Azure PowerShell, you'll need to set the environment variable `SuppressAzurePowerShellBreakingChangeWarnings` to `true`.</span></span>

```azurepowershell
Set-Item -Path Env:\SuppressAzurePowerShellBreakingChangeWarnings -Value $true
```