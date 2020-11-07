---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
ms.openlocfilehash: ac34f2d8c2a48010792716f183a6b86cce714294
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747869"
---
# <span data-ttu-id="160b9-101">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="160b9-101">Remove-AzNetworkProfile</span></span>

## <span data-ttu-id="160b9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="160b9-102">SYNOPSIS</span></span>
<span data-ttu-id="160b9-103">Tar bort en nätverks profil.</span><span class="sxs-lookup"><span data-stu-id="160b9-103">Removes a network profile.</span></span>

## <span data-ttu-id="160b9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="160b9-104">SYNTAX</span></span>

### <span data-ttu-id="160b9-105">RemoveByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="160b9-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="160b9-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="160b9-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzNetworkProfile -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="160b9-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="160b9-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzNetworkProfile -InputObject <PSNetworkProfile> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="160b9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="160b9-108">DESCRIPTION</span></span>
<span data-ttu-id="160b9-109">Cmdleten **Remove-AzNetworkProfile** tar bort en nätverks profil om ingen nätverks gränssnitt (som kontrast med en behållare för nätverks gränssnitt **) har** skapats.</span><span class="sxs-lookup"><span data-stu-id="160b9-109">The **Remove-AzNetworkProfile** cmdlet removes a network profile if no container network interfaces (as contrasted to a container network interface **configuration** ) have been created.</span></span>

## <span data-ttu-id="160b9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="160b9-110">EXAMPLES</span></span>

### <span data-ttu-id="160b9-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="160b9-111">Example 1</span></span>
```powershell
Remove-AzNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="160b9-112">Då tas nätverks profilen bort med namnet NP1 från resurs gruppen RG1.</span><span class="sxs-lookup"><span data-stu-id="160b9-112">This removes the network profile with name np1 from the resource group rg1.</span></span>

## <span data-ttu-id="160b9-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="160b9-113">PARAMETERS</span></span>

### <span data-ttu-id="160b9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="160b9-114">-AsJob</span></span>
<span data-ttu-id="160b9-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="160b9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="160b9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="160b9-116">-DefaultProfile</span></span>
<span data-ttu-id="160b9-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="160b9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="160b9-118">-Force</span><span class="sxs-lookup"><span data-stu-id="160b9-118">-Force</span></span>
<span data-ttu-id="160b9-119">Fråga inte efter bekräftelse om du vill ta bort resursen</span><span class="sxs-lookup"><span data-stu-id="160b9-119">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="160b9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="160b9-120">-InputObject</span></span>
<span data-ttu-id="160b9-121">Nätverks profil objekt.</span><span class="sxs-lookup"><span data-stu-id="160b9-121">Network profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkProfile
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="160b9-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="160b9-122">-Name</span></span>
<span data-ttu-id="160b9-123">Namnet på nätverks profilen.</span><span class="sxs-lookup"><span data-stu-id="160b9-123">The name of the network profile.</span></span>

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

### <span data-ttu-id="160b9-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="160b9-124">-PassThru</span></span>
<span data-ttu-id="160b9-125">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="160b9-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="160b9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="160b9-126">-ResourceGroupName</span></span>
<span data-ttu-id="160b9-127">Namnet på resurs gruppen för nätverks profilen.</span><span class="sxs-lookup"><span data-stu-id="160b9-127">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="160b9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="160b9-128">-ResourceId</span></span>
<span data-ttu-id="160b9-129">Resurs-ID för Azure Resource Manager för nätverks profilen.</span><span class="sxs-lookup"><span data-stu-id="160b9-129">The Azure resource manager resource ID of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="160b9-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="160b9-130">-Confirm</span></span>
<span data-ttu-id="160b9-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="160b9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="160b9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="160b9-132">-WhatIf</span></span>
<span data-ttu-id="160b9-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="160b9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="160b9-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="160b9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="160b9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="160b9-135">CommonParameters</span></span>
<span data-ttu-id="160b9-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="160b9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="160b9-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="160b9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="160b9-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="160b9-138">INPUTS</span></span>

### <span data-ttu-id="160b9-139">System. String</span><span class="sxs-lookup"><span data-stu-id="160b9-139">System.String</span></span>

### <span data-ttu-id="160b9-140">Microsoft. Azure. commands. Networks. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="160b9-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="160b9-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="160b9-141">OUTPUTS</span></span>

### <span data-ttu-id="160b9-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="160b9-142">System.Boolean</span></span>

## <span data-ttu-id="160b9-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="160b9-143">NOTES</span></span>

## <span data-ttu-id="160b9-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="160b9-144">RELATED LINKS</span></span>

[<span data-ttu-id="160b9-145">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="160b9-145">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="160b9-146">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="160b9-146">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="160b9-147">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="160b9-147">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
