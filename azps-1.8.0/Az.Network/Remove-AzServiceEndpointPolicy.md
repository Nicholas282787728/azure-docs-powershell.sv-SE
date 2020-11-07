---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
ms.openlocfilehash: 645eed141375dce0c27d389b721f7487c8a7c71f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747845"
---
# <span data-ttu-id="add99-101">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="add99-101">Remove-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="add99-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="add99-102">SYNOPSIS</span></span>
<span data-ttu-id="add99-103">Tar bort en tjänst slut punkts princip.</span><span class="sxs-lookup"><span data-stu-id="add99-103">Removes a service endpoint policy.</span></span>

## <span data-ttu-id="add99-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="add99-104">SYNTAX</span></span>

### <span data-ttu-id="add99-105">RemoveByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="add99-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="add99-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="add99-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="add99-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="add99-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject <PSServiceEndpointPolicy> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="add99-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="add99-108">DESCRIPTION</span></span>
<span data-ttu-id="add99-109">Cmdleten **Remove-AzServiceEndpointPolicy** tar bort en princip för tjänste slut punkter.</span><span class="sxs-lookup"><span data-stu-id="add99-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="add99-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="add99-110">EXAMPLES</span></span>

### <span data-ttu-id="add99-111">Exempel 1: tar bort en princip för service slut punkter med namn</span><span class="sxs-lookup"><span data-stu-id="add99-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="add99-112">Det här kommandot tar bort en tjänst slut punkts princip med namnet Policy1 som tillhör resourcegroup med namnet "resourcegroup1"</span><span class="sxs-lookup"><span data-stu-id="add99-112">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="add99-113">Exempel 2: ta bort en policy för tjänst slut punkter med hjälp av indata</span><span class="sxs-lookup"><span data-stu-id="add99-113">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="add99-114">Det här kommandot tar bort ett princip objekt för service Endpoint Policy1 som tillhör resourcegroup med namnet "resourcegroup1"</span><span class="sxs-lookup"><span data-stu-id="add99-114">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="add99-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="add99-115">PARAMETERS</span></span>

### <span data-ttu-id="add99-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="add99-116">-DefaultProfile</span></span>
<span data-ttu-id="add99-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="add99-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="add99-118">-Force</span><span class="sxs-lookup"><span data-stu-id="add99-118">-Force</span></span>
<span data-ttu-id="add99-119">Fråga inte efter bekräftelse om du vill overrite en resurs</span><span class="sxs-lookup"><span data-stu-id="add99-119">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="add99-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="add99-120">-InputObject</span></span>
<span data-ttu-id="add99-121">Principobjektet för tjänste slut punkter.</span><span class="sxs-lookup"><span data-stu-id="add99-121">The service endpoint policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="add99-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="add99-122">-Name</span></span>
<span data-ttu-id="add99-123">Namnet på tjänstens slut punkts princip</span><span class="sxs-lookup"><span data-stu-id="add99-123">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="add99-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="add99-124">-PassThru</span></span>
<span data-ttu-id="add99-125">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="add99-125">Returns an object representing the item with which you are working.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="add99-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="add99-126">-ResourceGroupName</span></span>
<span data-ttu-id="add99-127">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="add99-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="add99-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="add99-128">-ResourceId</span></span>
<span data-ttu-id="add99-129">ID för tjänste slut punkts princip.</span><span class="sxs-lookup"><span data-stu-id="add99-129">The ID of service endpoint policy.</span></span>

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

### <span data-ttu-id="add99-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="add99-130">-Confirm</span></span>
<span data-ttu-id="add99-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="add99-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="add99-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="add99-132">-WhatIf</span></span>
<span data-ttu-id="add99-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="add99-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="add99-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="add99-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="add99-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="add99-135">CommonParameters</span></span>
<span data-ttu-id="add99-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="add99-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="add99-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="add99-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="add99-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="add99-138">INPUTS</span></span>

### <span data-ttu-id="add99-139">System. String</span><span class="sxs-lookup"><span data-stu-id="add99-139">System.String</span></span>

### <span data-ttu-id="add99-140">Microsoft. Azure. commands. Networks. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="add99-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="add99-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="add99-141">OUTPUTS</span></span>

### <span data-ttu-id="add99-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="add99-142">System.Boolean</span></span>

## <span data-ttu-id="add99-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="add99-143">NOTES</span></span>

## <span data-ttu-id="add99-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="add99-144">RELATED LINKS</span></span>

[<span data-ttu-id="add99-145">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="add99-145">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="add99-146">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="add99-146">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="add99-147">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="add99-147">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
