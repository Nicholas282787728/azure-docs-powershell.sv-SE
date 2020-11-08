---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 146e43ce5f1816994a1d408e215e4b3e27c2bbca
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262071"
---
# <span data-ttu-id="8716e-101">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8716e-101">Remove-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="8716e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8716e-102">SYNOPSIS</span></span>
<span data-ttu-id="8716e-103">Tar bort en princip definition för service slut punkter.</span><span class="sxs-lookup"><span data-stu-id="8716e-103">Removes a service endpoint policy definition.</span></span>

## <span data-ttu-id="8716e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8716e-104">SYNTAX</span></span>

### <span data-ttu-id="8716e-105">RemoveByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8716e-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8716e-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8716e-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -ResourceId <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8716e-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8716e-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -InputObject <PSServiceEndpointPolicyDefinition>
 -ServiceEndpointPolicy <PSServiceEndpointPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8716e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8716e-108">DESCRIPTION</span></span>
<span data-ttu-id="8716e-109">Cmdleten **Remove-AzServiceEndpointPolicy** tar bort en princip för tjänste slut punkter.</span><span class="sxs-lookup"><span data-stu-id="8716e-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="8716e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8716e-110">EXAMPLES</span></span>

### <span data-ttu-id="8716e-111">Exempel 1: tar bort en princip för service slut punkter med namn</span><span class="sxs-lookup"><span data-stu-id="8716e-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="8716e-112">Det här kommandot tar bort en princip för service slut punkter med namnet PolicyDef1</span><span class="sxs-lookup"><span data-stu-id="8716e-112">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="8716e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8716e-113">PARAMETERS</span></span>

### <span data-ttu-id="8716e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8716e-114">-DefaultProfile</span></span>
<span data-ttu-id="8716e-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8716e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8716e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8716e-116">-InputObject</span></span>
<span data-ttu-id="8716e-117">Princip definitions objekt för tjänste slut punkt.</span><span class="sxs-lookup"><span data-stu-id="8716e-117">The service endpoint policy definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8716e-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="8716e-118">-Name</span></span>
<span data-ttu-id="8716e-119">Namnet på tjänst slut punkts definitionen</span><span class="sxs-lookup"><span data-stu-id="8716e-119">The name of the service endpoint definition</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8716e-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8716e-120">-ResourceId</span></span>
<span data-ttu-id="8716e-121">ID för tjänste slut punkts definitionen.</span><span class="sxs-lookup"><span data-stu-id="8716e-121">The ID of the service endpoint definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8716e-122">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8716e-122">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="8716e-123">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8716e-123">The ServiceEndpointPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8716e-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8716e-124">-Confirm</span></span>
<span data-ttu-id="8716e-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8716e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8716e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8716e-126">-WhatIf</span></span>
<span data-ttu-id="8716e-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8716e-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8716e-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8716e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8716e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8716e-129">CommonParameters</span></span>
<span data-ttu-id="8716e-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8716e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8716e-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8716e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8716e-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8716e-132">INPUTS</span></span>

### <span data-ttu-id="8716e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8716e-133">System.String</span></span>

### <span data-ttu-id="8716e-134">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8716e-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

### <span data-ttu-id="8716e-135">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8716e-135">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="8716e-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8716e-136">OUTPUTS</span></span>

### <span data-ttu-id="8716e-137">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8716e-137">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="8716e-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8716e-138">NOTES</span></span>

## <span data-ttu-id="8716e-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8716e-139">RELATED LINKS</span></span>

[<span data-ttu-id="8716e-140">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8716e-140">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="8716e-141">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8716e-141">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="8716e-142">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8716e-142">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="8716e-143">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8716e-143">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
