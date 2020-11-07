---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: c907c60619f5a0a2fc5f0620f086ba0b99ca62ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747840"
---
# <span data-ttu-id="c1d22-101">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c1d22-101">Remove-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="c1d22-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c1d22-102">SYNOPSIS</span></span>
<span data-ttu-id="c1d22-103">Tar bort en princip definition för service slut punkter.</span><span class="sxs-lookup"><span data-stu-id="c1d22-103">Removes a service endpoint policy definition.</span></span>

## <span data-ttu-id="c1d22-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c1d22-104">SYNTAX</span></span>

### <span data-ttu-id="c1d22-105">RemoveByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c1d22-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1d22-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1d22-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -ResourceId <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1d22-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1d22-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -InputObject <PSServiceEndpointPolicyDefinition>
 -ServiceEndpointPolicy <PSServiceEndpointPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1d22-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c1d22-108">DESCRIPTION</span></span>
<span data-ttu-id="c1d22-109">Cmdleten **Remove-AzServiceEndpointPolicy** tar bort en princip för tjänste slut punkter.</span><span class="sxs-lookup"><span data-stu-id="c1d22-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="c1d22-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c1d22-110">EXAMPLES</span></span>

### <span data-ttu-id="c1d22-111">Exempel 1: tar bort en princip för service slut punkter med namn</span><span class="sxs-lookup"><span data-stu-id="c1d22-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="c1d22-112">Det här kommandot tar bort en princip för service slut punkter med namnet PolicyDef1</span><span class="sxs-lookup"><span data-stu-id="c1d22-112">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="c1d22-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c1d22-113">PARAMETERS</span></span>

### <span data-ttu-id="c1d22-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1d22-114">-DefaultProfile</span></span>
<span data-ttu-id="c1d22-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c1d22-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1d22-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1d22-116">-InputObject</span></span>
<span data-ttu-id="c1d22-117">Princip definitions objekt för tjänste slut punkt.</span><span class="sxs-lookup"><span data-stu-id="c1d22-117">The service endpoint policy definition object.</span></span>

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

### <span data-ttu-id="c1d22-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="c1d22-118">-Name</span></span>
<span data-ttu-id="c1d22-119">Namnet på tjänst slut punkts definitionen</span><span class="sxs-lookup"><span data-stu-id="c1d22-119">The name of the service endpoint definition</span></span>

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

### <span data-ttu-id="c1d22-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1d22-120">-ResourceId</span></span>
<span data-ttu-id="c1d22-121">ID för tjänste slut punkts definitionen.</span><span class="sxs-lookup"><span data-stu-id="c1d22-121">The ID of the service endpoint definition.</span></span>

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

### <span data-ttu-id="c1d22-122">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c1d22-122">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="c1d22-123">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c1d22-123">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="c1d22-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c1d22-124">-Confirm</span></span>
<span data-ttu-id="c1d22-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c1d22-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1d22-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1d22-126">-WhatIf</span></span>
<span data-ttu-id="c1d22-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c1d22-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c1d22-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c1d22-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1d22-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1d22-129">CommonParameters</span></span>
<span data-ttu-id="c1d22-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1d22-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1d22-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1d22-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1d22-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c1d22-132">INPUTS</span></span>

### <span data-ttu-id="c1d22-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c1d22-133">System.String</span></span>

### <span data-ttu-id="c1d22-134">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c1d22-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

### <span data-ttu-id="c1d22-135">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c1d22-135">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="c1d22-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c1d22-136">OUTPUTS</span></span>

### <span data-ttu-id="c1d22-137">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c1d22-137">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="c1d22-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c1d22-138">NOTES</span></span>

## <span data-ttu-id="c1d22-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c1d22-139">RELATED LINKS</span></span>

[<span data-ttu-id="c1d22-140">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c1d22-140">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="c1d22-141">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c1d22-141">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="c1d22-142">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c1d22-142">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="c1d22-143">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c1d22-143">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
