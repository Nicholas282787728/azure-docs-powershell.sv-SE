---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Start-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 0efde69aec3b30c58aee8c42aeb1703215219c2e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525606"
---
# <span data-ttu-id="72e12-101">Start-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="72e12-101">Start-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="72e12-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72e12-102">SYNOPSIS</span></span>
<span data-ttu-id="72e12-103">Anropar en tillfällig begäran om nätverks åtkomst.</span><span class="sxs-lookup"><span data-stu-id="72e12-103">Invokes a temporary network access request.</span></span>

## <span data-ttu-id="72e12-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72e12-104">SYNTAX</span></span>

### <span data-ttu-id="72e12-105">ResourceGroupLevelResource (standard)</span><span class="sxs-lookup"><span data-stu-id="72e12-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72e12-106">ID</span><span class="sxs-lookup"><span data-stu-id="72e12-106">ResourceId</span></span>
```
Start-AzJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72e12-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="72e12-107">InputObject</span></span>
```
Start-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72e12-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72e12-108">DESCRIPTION</span></span>
<span data-ttu-id="72e12-109">Anropar en tillfällig begäran om nätverks åtkomst.</span><span class="sxs-lookup"><span data-stu-id="72e12-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="72e12-110">Begäran verifieras mot den konfigurerade principen för JIT-nätverksanslutning och om det är tillåtet öppnas en nätverks anslutning enligt användarens begäran.</span><span class="sxs-lookup"><span data-stu-id="72e12-110">The request is validated against the configured JIT network access policy and if permitted, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="72e12-111">Begäran kommer att loggas i policyn för senare granskning och avslutas när den angivna varaktigheten överskrids.</span><span class="sxs-lookup"><span data-stu-id="72e12-111">The request will be logged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="72e12-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72e12-112">EXAMPLES</span></span>

### <span data-ttu-id="72e12-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="72e12-113">Example 1</span></span>
```powershell
$MyResource = Get-AzResource -Id /subscriptions/xxxxxxx-xxxxx-xxxxx-xxxxxxx/resourceGroups/PolicyDemo/providers/Microsoft.Compute/virtualMachines/PolicyDemoVM1
$JitPolicy = (@{
        id    = $MyResource.ResourceId; 
        ports = (@{
                number                     = 22
                endTimeUtc                 = Get-Date (Get-Date -AsUTC).AddHours(1) -Format O
                allowedSourceAddressPrefix = @($MyPublicIP) 
            })
    })
$ActivationVM = @($JitPolicy)
Start-AzJitNetworkAccessPolicy -ResourceGroupName $($MyResource.ResourceGroupName) -Location $MyResource.Location -Name "default" -VirtualMachine $ActivationVM

```

<span data-ttu-id="72e12-114">Öppnar en nätverks anslutning för 1 timme via port 22 från min offentliga IP-adress (visas inte).</span><span class="sxs-lookup"><span data-stu-id="72e12-114">Opens up a network connection for 1 hour over port 22 from my public IP (not shown).</span></span>

## <span data-ttu-id="72e12-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72e12-115">PARAMETERS</span></span>

### <span data-ttu-id="72e12-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72e12-116">-DefaultProfile</span></span>
<span data-ttu-id="72e12-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="72e12-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72e12-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72e12-118">-InputObject</span></span>
<span data-ttu-id="72e12-119">Indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="72e12-119">Input Object.</span></span>

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

### <span data-ttu-id="72e12-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="72e12-120">-Location</span></span>
<span data-ttu-id="72e12-121">Plats.</span><span class="sxs-lookup"><span data-stu-id="72e12-121">Location.</span></span>

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

### <span data-ttu-id="72e12-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="72e12-122">-Name</span></span>
<span data-ttu-id="72e12-123">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="72e12-123">Resource name.</span></span>

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

### <span data-ttu-id="72e12-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72e12-124">-ResourceGroupName</span></span>
<span data-ttu-id="72e12-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="72e12-125">Resource group name.</span></span>

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

### <span data-ttu-id="72e12-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72e12-126">-ResourceId</span></span>
<span data-ttu-id="72e12-127">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="72e12-127">Resource ID.</span></span>

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

### <span data-ttu-id="72e12-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="72e12-128">-VirtualMachine</span></span>
<span data-ttu-id="72e12-129">Automatisk etablering.</span><span class="sxs-lookup"><span data-stu-id="72e12-129">Automatic Provisioning.</span></span>

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

### <span data-ttu-id="72e12-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="72e12-130">-Confirm</span></span>
<span data-ttu-id="72e12-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="72e12-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72e12-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72e12-132">-WhatIf</span></span>
<span data-ttu-id="72e12-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="72e12-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72e12-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="72e12-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72e12-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72e12-135">CommonParameters</span></span>
<span data-ttu-id="72e12-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72e12-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72e12-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72e12-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72e12-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72e12-138">INPUTS</span></span>

### <span data-ttu-id="72e12-139">System. String</span><span class="sxs-lookup"><span data-stu-id="72e12-139">System.String</span></span>

### <span data-ttu-id="72e12-140">Microsoft. Azure. kommandon. Security. cmdletar. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicyInitiateInputObject</span><span class="sxs-lookup"><span data-stu-id="72e12-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span></span>

## <span data-ttu-id="72e12-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72e12-141">OUTPUTS</span></span>

### <span data-ttu-id="72e12-142">Microsoft. Azure. commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="72e12-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="72e12-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72e12-143">NOTES</span></span>

## <span data-ttu-id="72e12-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72e12-144">RELATED LINKS</span></span>
