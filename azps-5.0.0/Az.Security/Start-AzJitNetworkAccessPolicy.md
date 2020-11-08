---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Start-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: b992f3a41278ba66c54eeefc0b548eef76b50980
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269413"
---
# <span data-ttu-id="d1d5a-101">Start-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d1d5a-101">Start-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="d1d5a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d1d5a-102">SYNOPSIS</span></span>
<span data-ttu-id="d1d5a-103">Anropar en tillfällig begäran om nätverks åtkomst.</span><span class="sxs-lookup"><span data-stu-id="d1d5a-103">Invokes a temporary network access request.</span></span>

## <span data-ttu-id="d1d5a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d1d5a-104">SYNTAX</span></span>

### <span data-ttu-id="d1d5a-105">ResourceGroupLevelResource (standard)</span><span class="sxs-lookup"><span data-stu-id="d1d5a-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1d5a-106">ID</span><span class="sxs-lookup"><span data-stu-id="d1d5a-106">ResourceId</span></span>
```
Start-AzJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1d5a-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="d1d5a-107">InputObject</span></span>
```
Start-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1d5a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d1d5a-108">DESCRIPTION</span></span>
<span data-ttu-id="d1d5a-109">Anropar en tillfällig begäran om nätverks åtkomst.</span><span class="sxs-lookup"><span data-stu-id="d1d5a-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="d1d5a-110">Begäran verifieras mot den konfigurerade principen för JIT-nätverksanslutning och om det är tillåtet öppnas en nätverks anslutning enligt användarens begäran.</span><span class="sxs-lookup"><span data-stu-id="d1d5a-110">The request is validated against the configured JIT network access policy and if permitted, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="d1d5a-111">Begäran kommer att loggas i policyn för senare granskning och avslutas när den angivna varaktigheten överskrids.</span><span class="sxs-lookup"><span data-stu-id="d1d5a-111">The request will be logged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="d1d5a-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d1d5a-112">EXAMPLES</span></span>

### <span data-ttu-id="d1d5a-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d1d5a-113">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -Kind "Basic" -VirtualMachine $vms

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.S
                    ecurity/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                    Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="d1d5a-114">Öppnar en nätverks anslutning enligt angivna data för anslutningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="d1d5a-114">Opens up a network connection according to the specified connection request data.</span></span>

## <span data-ttu-id="d1d5a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d1d5a-115">PARAMETERS</span></span>

### <span data-ttu-id="d1d5a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1d5a-116">-DefaultProfile</span></span>
<span data-ttu-id="d1d5a-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d1d5a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1d5a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1d5a-118">-InputObject</span></span>
<span data-ttu-id="d1d5a-119">Indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="d1d5a-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1d5a-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="d1d5a-120">-Location</span></span>
<span data-ttu-id="d1d5a-121">Plats.</span><span class="sxs-lookup"><span data-stu-id="d1d5a-121">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1d5a-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="d1d5a-122">-Name</span></span>
<span data-ttu-id="d1d5a-123">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="d1d5a-123">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1d5a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1d5a-124">-ResourceGroupName</span></span>
<span data-ttu-id="d1d5a-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="d1d5a-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1d5a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1d5a-126">-ResourceId</span></span>
<span data-ttu-id="d1d5a-127">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="d1d5a-127">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1d5a-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d1d5a-128">-VirtualMachine</span></span>
<span data-ttu-id="d1d5a-129">Automatisk etablering.</span><span class="sxs-lookup"><span data-stu-id="d1d5a-129">Automatic Provisioning.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1d5a-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d1d5a-130">-Confirm</span></span>
<span data-ttu-id="d1d5a-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d1d5a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1d5a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1d5a-132">-WhatIf</span></span>
<span data-ttu-id="d1d5a-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d1d5a-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d1d5a-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d1d5a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1d5a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1d5a-135">CommonParameters</span></span>
<span data-ttu-id="d1d5a-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1d5a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1d5a-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1d5a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1d5a-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d1d5a-138">INPUTS</span></span>

### <span data-ttu-id="d1d5a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d1d5a-139">System.String</span></span>

### <span data-ttu-id="d1d5a-140">Microsoft. Azure. kommandon. Security. cmdletar. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicyInitiateInputObject</span><span class="sxs-lookup"><span data-stu-id="d1d5a-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span></span>

## <span data-ttu-id="d1d5a-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d1d5a-141">OUTPUTS</span></span>

### <span data-ttu-id="d1d5a-142">Microsoft. Azure. commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d1d5a-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="d1d5a-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d1d5a-143">NOTES</span></span>

## <span data-ttu-id="d1d5a-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d1d5a-144">RELATED LINKS</span></span>
