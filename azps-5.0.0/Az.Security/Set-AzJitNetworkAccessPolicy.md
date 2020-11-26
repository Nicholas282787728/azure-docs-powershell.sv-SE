---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: a316a59492034f0effd2d233ce386cbd6a256c75
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271236"
---
# <span data-ttu-id="e72a9-101">Set-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e72a9-101">Set-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="e72a9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e72a9-102">SYNOPSIS</span></span>
<span data-ttu-id="e72a9-103">Uppdaterar princip för JIT-nätverks åtkomst.</span><span class="sxs-lookup"><span data-stu-id="e72a9-103">Updates JIT network access policy.</span></span>

## <span data-ttu-id="e72a9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e72a9-104">SYNTAX</span></span>

```
Set-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e72a9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e72a9-105">DESCRIPTION</span></span>
<span data-ttu-id="e72a9-106">Uppdaterar princip för JIT-nätverks åtkomst.</span><span class="sxs-lookup"><span data-stu-id="e72a9-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="e72a9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e72a9-107">EXAMPLES</span></span>

### <span data-ttu-id="e72a9-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e72a9-108">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="e72a9-109">Uppdaterar en policy för JIT-nätverksanslutning med nya regler för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="e72a9-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="e72a9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e72a9-110">PARAMETERS</span></span>

### <span data-ttu-id="e72a9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e72a9-111">-DefaultProfile</span></span>
<span data-ttu-id="e72a9-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e72a9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e72a9-113">-Sort</span><span class="sxs-lookup"><span data-stu-id="e72a9-113">-Kind</span></span>
<span data-ttu-id="e72a9-114">Typ.</span><span class="sxs-lookup"><span data-stu-id="e72a9-114">Kind.</span></span>

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

### <span data-ttu-id="e72a9-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="e72a9-115">-Location</span></span>
<span data-ttu-id="e72a9-116">Plats.</span><span class="sxs-lookup"><span data-stu-id="e72a9-116">Location.</span></span>

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

### <span data-ttu-id="e72a9-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="e72a9-117">-Name</span></span>
<span data-ttu-id="e72a9-118">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="e72a9-118">Resource name.</span></span>

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

### <span data-ttu-id="e72a9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e72a9-119">-ResourceGroupName</span></span>
<span data-ttu-id="e72a9-120">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="e72a9-120">Resource group name.</span></span>

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

### <span data-ttu-id="e72a9-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e72a9-121">-VirtualMachine</span></span>
<span data-ttu-id="e72a9-122">Virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="e72a9-122">Virtual Machines.</span></span>

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

### <span data-ttu-id="e72a9-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e72a9-123">-Confirm</span></span>
<span data-ttu-id="e72a9-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e72a9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e72a9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e72a9-125">-WhatIf</span></span>
<span data-ttu-id="e72a9-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e72a9-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e72a9-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e72a9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e72a9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e72a9-128">CommonParameters</span></span>
<span data-ttu-id="e72a9-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e72a9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e72a9-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e72a9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e72a9-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e72a9-131">INPUTS</span></span>

### <span data-ttu-id="e72a9-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="e72a9-132">None</span></span>

## <span data-ttu-id="e72a9-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e72a9-133">OUTPUTS</span></span>

### <span data-ttu-id="e72a9-134">Microsoft. Azure. commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e72a9-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="e72a9-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e72a9-135">NOTES</span></span>

## <span data-ttu-id="e72a9-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e72a9-136">RELATED LINKS</span></span>