---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Start-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Start-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Start-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: 62dccdc3b55caa5d63036ed3298caa5a01514342
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581648"
---
# <span data-ttu-id="f39fe-101">Start-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f39fe-101">Start-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="f39fe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f39fe-102">SYNOPSIS</span></span>
<span data-ttu-id="f39fe-103">Anropar en tillfällig begäran om nätverks åtkomst.</span><span class="sxs-lookup"><span data-stu-id="f39fe-103">Invokes a temporary network access request.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f39fe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f39fe-104">SYNTAX</span></span>

### <span data-ttu-id="f39fe-105">ResourceGroupLevelResource (standard)</span><span class="sxs-lookup"><span data-stu-id="f39fe-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f39fe-106">ID</span><span class="sxs-lookup"><span data-stu-id="f39fe-106">ResourceId</span></span>
```
Start-AzureRmJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f39fe-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="f39fe-107">InputObject</span></span>
```
Start-AzureRmJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f39fe-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f39fe-108">DESCRIPTION</span></span>
<span data-ttu-id="f39fe-109">Anropar en tillfällig begäran om nätverks åtkomst.</span><span class="sxs-lookup"><span data-stu-id="f39fe-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="f39fe-110">Begäran verifieras mot den konfigurerade principen för JIT-nätverksanslutning och om permittet öppnas en nätverks anslutning enligt användarens begäran.</span><span class="sxs-lookup"><span data-stu-id="f39fe-110">The request is validated against the configured JIT network access policy and if permittet, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="f39fe-111">Begäran kommer att finnas med i policyn för senare granskning och kommer att avslutas när den angivna varaktigheten överskrids.</span><span class="sxs-lookup"><span data-stu-id="f39fe-111">The request will be loged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="f39fe-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f39fe-112">EXAMPLES</span></span>

### <span data-ttu-id="f39fe-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f39fe-113">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -Kind "Basic" -VirtualMachine $vms

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.S
                    ecurity/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                    Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="f39fe-114">Öppnar en nätverks anslutning enligt angivna data för anslutningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="f39fe-114">Opens up a network connection according to the specified connection request data.</span></span>

## <span data-ttu-id="f39fe-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f39fe-115">PARAMETERS</span></span>

### <span data-ttu-id="f39fe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f39fe-116">-DefaultProfile</span></span>
<span data-ttu-id="f39fe-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f39fe-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f39fe-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f39fe-118">-InputObject</span></span>
<span data-ttu-id="f39fe-119">Indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="f39fe-119">Input Object.</span></span>

```yaml
Type: PSSecurityJitNetworkAccessPolicyInitiateInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f39fe-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="f39fe-120">-Location</span></span>
<span data-ttu-id="f39fe-121">Plats.</span><span class="sxs-lookup"><span data-stu-id="f39fe-121">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f39fe-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="f39fe-122">-Name</span></span>
<span data-ttu-id="f39fe-123">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="f39fe-123">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f39fe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f39fe-124">-ResourceGroupName</span></span>
<span data-ttu-id="f39fe-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="f39fe-125">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f39fe-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f39fe-126">-ResourceId</span></span>
<span data-ttu-id="f39fe-127">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="f39fe-127">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f39fe-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f39fe-128">-VirtualMachine</span></span>
<span data-ttu-id="f39fe-129">Automatisk etablering.</span><span class="sxs-lookup"><span data-stu-id="f39fe-129">Automatic Provisioning.</span></span>

```yaml
Type: PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f39fe-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f39fe-130">-Confirm</span></span>
<span data-ttu-id="f39fe-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f39fe-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f39fe-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f39fe-132">-WhatIf</span></span>
<span data-ttu-id="f39fe-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f39fe-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f39fe-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f39fe-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f39fe-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f39fe-135">CommonParameters</span></span>
<span data-ttu-id="f39fe-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f39fe-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f39fe-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f39fe-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f39fe-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f39fe-138">INPUTS</span></span>

### <span data-ttu-id="f39fe-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f39fe-139">System.String</span></span>
<span data-ttu-id="f39fe-140">Microsoft. Azure. commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine []</span><span class="sxs-lookup"><span data-stu-id="f39fe-140">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]</span></span>

## <span data-ttu-id="f39fe-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f39fe-141">OUTPUTS</span></span>

### <span data-ttu-id="f39fe-142">Microsoft. Azure. commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f39fe-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="f39fe-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f39fe-143">NOTES</span></span>

## <span data-ttu-id="f39fe-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f39fe-144">RELATED LINKS</span></span>
