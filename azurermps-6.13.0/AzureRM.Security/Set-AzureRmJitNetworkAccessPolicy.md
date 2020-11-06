---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: 72e3cf48f112c5e9bb07a8f7eb57dfe3d4c9ee07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576077"
---
# <span data-ttu-id="c41b9-101">Set-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c41b9-101">Set-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="c41b9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c41b9-102">SYNOPSIS</span></span>
<span data-ttu-id="c41b9-103">Uppdaterar princip för JIT-nätverks åtkomst.</span><span class="sxs-lookup"><span data-stu-id="c41b9-103">Updates JIT network access policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c41b9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c41b9-104">SYNTAX</span></span>

```
Set-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c41b9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c41b9-105">DESCRIPTION</span></span>
<span data-ttu-id="c41b9-106">Uppdaterar princip för JIT-nätverks åtkomst.</span><span class="sxs-lookup"><span data-stu-id="c41b9-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="c41b9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c41b9-107">EXAMPLES</span></span>

### <span data-ttu-id="c41b9-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c41b9-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="c41b9-109">Uppdaterar en policy för JIT-nätverksanslutning med nya regler för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="c41b9-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="c41b9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c41b9-110">PARAMETERS</span></span>

### <span data-ttu-id="c41b9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c41b9-111">-DefaultProfile</span></span>
<span data-ttu-id="c41b9-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c41b9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c41b9-113">-Sort</span><span class="sxs-lookup"><span data-stu-id="c41b9-113">-Kind</span></span>
<span data-ttu-id="c41b9-114">Typ.</span><span class="sxs-lookup"><span data-stu-id="c41b9-114">Kind.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c41b9-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="c41b9-115">-Location</span></span>
<span data-ttu-id="c41b9-116">Plats.</span><span class="sxs-lookup"><span data-stu-id="c41b9-116">Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c41b9-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="c41b9-117">-Name</span></span>
<span data-ttu-id="c41b9-118">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="c41b9-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c41b9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c41b9-119">-ResourceGroupName</span></span>
<span data-ttu-id="c41b9-120">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="c41b9-120">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c41b9-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c41b9-121">-VirtualMachine</span></span>
<span data-ttu-id="c41b9-122">Virutal-datorer.</span><span class="sxs-lookup"><span data-stu-id="c41b9-122">Virutal Machines.</span></span>

```yaml
Type: PSSecurityJitNetworkAccessPolicyVirtualMachine[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c41b9-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c41b9-123">-Confirm</span></span>
<span data-ttu-id="c41b9-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c41b9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c41b9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c41b9-125">-WhatIf</span></span>
<span data-ttu-id="c41b9-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c41b9-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c41b9-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c41b9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c41b9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c41b9-128">CommonParameters</span></span>
<span data-ttu-id="c41b9-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c41b9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c41b9-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c41b9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c41b9-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c41b9-131">INPUTS</span></span>

### <span data-ttu-id="c41b9-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c41b9-132">System.String</span></span>
<span data-ttu-id="c41b9-133">Microsoft. Azure. commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicyVirtualMachine []</span><span class="sxs-lookup"><span data-stu-id="c41b9-133">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyVirtualMachine[]</span></span>

## <span data-ttu-id="c41b9-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c41b9-134">OUTPUTS</span></span>

### <span data-ttu-id="c41b9-135">Microsoft. Azure. commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c41b9-135">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="c41b9-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c41b9-136">NOTES</span></span>

## <span data-ttu-id="c41b9-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c41b9-137">RELATED LINKS</span></span>
