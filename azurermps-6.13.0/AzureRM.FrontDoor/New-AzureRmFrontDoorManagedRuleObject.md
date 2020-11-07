---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoormanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorManagedRuleObject.md
ms.openlocfilehash: 236cb9ff263f97ae52ea5d3226f4defec00c662a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756160"
---
# <span data-ttu-id="03010-101">New-AzureRmFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="03010-101">New-AzureRmFrontDoorManagedRuleObject</span></span>

## <span data-ttu-id="03010-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="03010-102">SYNOPSIS</span></span>
<span data-ttu-id="03010-103">Skapa ManagedRule-objekt för WAF-princip</span><span class="sxs-lookup"><span data-stu-id="03010-103">Create ManagedRule Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03010-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="03010-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorManagedRuleObject -Priority <Int32> [-Version <String>]
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="03010-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="03010-105">DESCRIPTION</span></span>
<span data-ttu-id="03010-106">Skapa ManagedRule-objekt för WAF-princip</span><span class="sxs-lookup"><span data-stu-id="03010-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="03010-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="03010-107">EXAMPLES</span></span>

### <span data-ttu-id="03010-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="03010-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoor
ManagedRuleObject -Priority 1 -Version 0 -RuleGroupOverride $override1

RuleGroupOverrides                                                   Priority Version
------------------                                                   -------- -------
{Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride}        1 0
```

<span data-ttu-id="03010-109">Skapa ett ManagedRule-objekt</span><span class="sxs-lookup"><span data-stu-id="03010-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="03010-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="03010-110">PARAMETERS</span></span>

### <span data-ttu-id="03010-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03010-111">-DefaultProfile</span></span>
<span data-ttu-id="03010-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="03010-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03010-113">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="03010-113">-Priority</span></span>
<span data-ttu-id="03010-114">Beskriver regelns prioritet</span><span class="sxs-lookup"><span data-stu-id="03010-114">Describes priority of the rule</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03010-115">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="03010-115">-RuleGroupOverride</span></span>
<span data-ttu-id="03010-116">Lista över åsidosättning av Azure Managed Provider</span><span class="sxs-lookup"><span data-stu-id="03010-116">List of azure managed provider override configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03010-117">-Version</span><span class="sxs-lookup"><span data-stu-id="03010-117">-Version</span></span>
<span data-ttu-id="03010-118">Version av ruleset</span><span class="sxs-lookup"><span data-stu-id="03010-118">Version of the ruleset</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03010-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03010-119">CommonParameters</span></span>
<span data-ttu-id="03010-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03010-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03010-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03010-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03010-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="03010-122">INPUTS</span></span>

### <span data-ttu-id="03010-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="03010-123">None</span></span>

## <span data-ttu-id="03010-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="03010-124">OUTPUTS</span></span>

### <span data-ttu-id="03010-125">Microsoft. Azure. commands. FrontDoor. Models. PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="03010-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="03010-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="03010-126">NOTES</span></span>

## <span data-ttu-id="03010-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="03010-127">RELATED LINKS</span></span>

<span data-ttu-id="03010-128">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md) 
 [New-AzureRmFrontDoorRuleGroupOverrideObject](./Set-AzureRmFrontDoorRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="03010-128">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)
[New-AzureRmFrontDoorRuleGroupOverrideObject](./Set-AzureRmFrontDoorRuleGroupOverrideObject.md)</span></span>
