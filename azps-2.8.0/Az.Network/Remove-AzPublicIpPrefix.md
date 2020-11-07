---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
ms.openlocfilehash: 962c7d8f5120e0d6ae75d584edf261307bcefbee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918034"
---
# <span data-ttu-id="ce2bb-101">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ce2bb-101">Remove-AzPublicIpPrefix</span></span>

## <span data-ttu-id="ce2bb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ce2bb-102">SYNOPSIS</span></span>
<span data-ttu-id="ce2bb-103">Tar bort ett offentlig IP-prefix</span><span class="sxs-lookup"><span data-stu-id="ce2bb-103">Removes a public IP prefix</span></span>

## <span data-ttu-id="ce2bb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ce2bb-104">SYNTAX</span></span>

### <span data-ttu-id="ce2bb-105">RemoveByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ce2bb-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce2bb-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce2bb-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce2bb-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce2bb-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce2bb-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ce2bb-108">DESCRIPTION</span></span>
<span data-ttu-id="ce2bb-109">Cmdleten **Remove-AzPublicIpPrefix** tar bort ett prefix för Azure offentlig IP så länge det inte finns några offentliga IP-adresser tilldelade till sig.</span><span class="sxs-lookup"><span data-stu-id="ce2bb-109">The **Remove-AzPublicIpPrefix** cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="ce2bb-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ce2bb-110">EXAMPLES</span></span>

### <span data-ttu-id="ce2bb-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ce2bb-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="ce2bb-112">Tar bort det offentliga IP-prefixet med namnet $prefixName från resurs gruppen $rgName</span><span class="sxs-lookup"><span data-stu-id="ce2bb-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="ce2bb-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ce2bb-113">PARAMETERS</span></span>

### <span data-ttu-id="ce2bb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce2bb-114">-AsJob</span></span>
<span data-ttu-id="ce2bb-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ce2bb-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ce2bb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce2bb-116">-DefaultProfile</span></span>
<span data-ttu-id="ce2bb-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ce2bb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce2bb-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ce2bb-118">-Force</span></span>
<span data-ttu-id="ce2bb-119">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ce2bb-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ce2bb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce2bb-120">-InputObject</span></span>
<span data-ttu-id="ce2bb-121">Ett PublicIpPrefix-objekt</span><span class="sxs-lookup"><span data-stu-id="ce2bb-121">A PublicIpPrefix object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce2bb-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="ce2bb-122">-Name</span></span>
<span data-ttu-id="ce2bb-123">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="ce2bb-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce2bb-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce2bb-124">-PassThru</span></span>
<span data-ttu-id="ce2bb-125">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="ce2bb-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ce2bb-126">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="ce2bb-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ce2bb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce2bb-127">-ResourceGroupName</span></span>
<span data-ttu-id="ce2bb-128">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="ce2bb-128">The resource group name.</span></span>

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

### <span data-ttu-id="ce2bb-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce2bb-129">-ResourceId</span></span>
<span data-ttu-id="ce2bb-130">ResourceId för resursen som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="ce2bb-130">The resourceId for the resource to remove</span></span>

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

### <span data-ttu-id="ce2bb-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ce2bb-131">-Confirm</span></span>
<span data-ttu-id="ce2bb-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ce2bb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce2bb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce2bb-133">-WhatIf</span></span>
<span data-ttu-id="ce2bb-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ce2bb-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce2bb-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ce2bb-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce2bb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce2bb-136">CommonParameters</span></span>
<span data-ttu-id="ce2bb-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce2bb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce2bb-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce2bb-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce2bb-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ce2bb-139">INPUTS</span></span>

### <span data-ttu-id="ce2bb-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ce2bb-140">System.String</span></span>

### <span data-ttu-id="ce2bb-141">Microsoft. Azure. commands. Networks. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ce2bb-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="ce2bb-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ce2bb-142">OUTPUTS</span></span>

### <span data-ttu-id="ce2bb-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ce2bb-143">System.Boolean</span></span>

## <span data-ttu-id="ce2bb-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ce2bb-144">NOTES</span></span>

## <span data-ttu-id="ce2bb-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ce2bb-145">RELATED LINKS</span></span>

[<span data-ttu-id="ce2bb-146">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ce2bb-146">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="ce2bb-147">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ce2bb-147">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="ce2bb-148">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ce2bb-148">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
