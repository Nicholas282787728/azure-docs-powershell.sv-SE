---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: ddb9bc19e852ae482dbbf687966c5f73f0a0a1d3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746959"
---
# <span data-ttu-id="e60ae-101">Set-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e60ae-101">Set-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="e60ae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e60ae-102">SYNOPSIS</span></span>
<span data-ttu-id="e60ae-103">Uppdaterar princip för JIT-nätverks åtkomst.</span><span class="sxs-lookup"><span data-stu-id="e60ae-103">Updates JIT network access policy.</span></span>

## <span data-ttu-id="e60ae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e60ae-104">SYNTAX</span></span>

```
Set-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e60ae-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e60ae-105">DESCRIPTION</span></span>
<span data-ttu-id="e60ae-106">Uppdaterar princip för JIT-nätverks åtkomst.</span><span class="sxs-lookup"><span data-stu-id="e60ae-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="e60ae-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e60ae-107">EXAMPLES</span></span>

### <span data-ttu-id="e60ae-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e60ae-108">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="e60ae-109">Uppdaterar en policy för JIT-nätverksanslutning med nya regler för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="e60ae-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="e60ae-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e60ae-110">PARAMETERS</span></span>

### <span data-ttu-id="e60ae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e60ae-111">-DefaultProfile</span></span>
<span data-ttu-id="e60ae-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e60ae-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e60ae-113">-Sort</span><span class="sxs-lookup"><span data-stu-id="e60ae-113">-Kind</span></span>
<span data-ttu-id="e60ae-114">Typ.</span><span class="sxs-lookup"><span data-stu-id="e60ae-114">Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e60ae-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="e60ae-115">-Location</span></span>
<span data-ttu-id="e60ae-116">Plats.</span><span class="sxs-lookup"><span data-stu-id="e60ae-116">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e60ae-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="e60ae-117">-Name</span></span>
<span data-ttu-id="e60ae-118">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="e60ae-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e60ae-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e60ae-119">-ResourceGroupName</span></span>
<span data-ttu-id="e60ae-120">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="e60ae-120">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e60ae-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e60ae-121">-VirtualMachine</span></span>
<span data-ttu-id="e60ae-122">Virutal-datorer.</span><span class="sxs-lookup"><span data-stu-id="e60ae-122">Virutal Machines.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyVirtualMachine[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e60ae-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e60ae-123">-Confirm</span></span>
<span data-ttu-id="e60ae-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e60ae-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e60ae-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e60ae-125">-WhatIf</span></span>
<span data-ttu-id="e60ae-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e60ae-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e60ae-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e60ae-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e60ae-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e60ae-128">CommonParameters</span></span>
<span data-ttu-id="e60ae-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e60ae-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e60ae-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e60ae-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e60ae-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e60ae-131">INPUTS</span></span>

### <span data-ttu-id="e60ae-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="e60ae-132">None</span></span>

## <span data-ttu-id="e60ae-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e60ae-133">OUTPUTS</span></span>

### <span data-ttu-id="e60ae-134">Microsoft. Azure. commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e60ae-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="e60ae-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e60ae-135">NOTES</span></span>

## <span data-ttu-id="e60ae-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e60ae-136">RELATED LINKS</span></span>
