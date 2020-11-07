---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
ms.openlocfilehash: 0aa1ce29daf186cfbe77f2ad42e108ce65b6e799
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917153"
---
# <span data-ttu-id="b2819-101">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b2819-101">Remove-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="b2819-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b2819-102">SYNOPSIS</span></span>
<span data-ttu-id="b2819-103">Tar bort en container-registerpost.</span><span class="sxs-lookup"><span data-stu-id="b2819-103">Removes a container registry replication.</span></span>

## <span data-ttu-id="b2819-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b2819-104">SYNTAX</span></span>

### <span data-ttu-id="b2819-105">NameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b2819-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2819-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2819-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -Replicatoin <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2819-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2819-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2819-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b2819-108">DESCRIPTION</span></span>
<span data-ttu-id="b2819-109">Remove-AzContainerRegistryReplication cmdlet tar bort en behållar registrering.</span><span class="sxs-lookup"><span data-stu-id="b2819-109">The Remove-AzContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="b2819-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b2819-110">EXAMPLES</span></span>

### <span data-ttu-id="b2819-111">Exempel 1: tar bort en container-registerpost.</span><span class="sxs-lookup"><span data-stu-id="b2819-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="b2819-112">Tar bort en container-registerpost.</span><span class="sxs-lookup"><span data-stu-id="b2819-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="b2819-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b2819-113">PARAMETERS</span></span>

### <span data-ttu-id="b2819-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2819-114">-DefaultProfile</span></span>
<span data-ttu-id="b2819-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b2819-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2819-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="b2819-116">-Name</span></span>
<span data-ttu-id="b2819-117">Namn på container Registry.</span><span class="sxs-lookup"><span data-stu-id="b2819-117">Container Registry Replication Name.</span></span>
<span data-ttu-id="b2819-118">Standardvärdet för plats namnet.</span><span class="sxs-lookup"><span data-stu-id="b2819-118">Default to the location name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2819-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2819-119">-PassThru</span></span>
<span data-ttu-id="b2819-120">Anger att denna cmdlet returnerar sant om borttagningen lyckades.</span><span class="sxs-lookup"><span data-stu-id="b2819-120">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="b2819-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="b2819-121">-RegistryName</span></span>
<span data-ttu-id="b2819-122">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="b2819-122">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2819-123">-Replicatoin</span><span class="sxs-lookup"><span data-stu-id="b2819-123">-Replicatoin</span></span>
<span data-ttu-id="b2819-124">Behållarobjekt för container.</span><span class="sxs-lookup"><span data-stu-id="b2819-124">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication
Parameter Sets: ReplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2819-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2819-125">-ResourceGroupName</span></span>
<span data-ttu-id="b2819-126">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="b2819-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2819-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2819-127">-ResourceId</span></span>
<span data-ttu-id="b2819-128">Resurs-ID för behållar registrering</span><span class="sxs-lookup"><span data-stu-id="b2819-128">The container registry replication resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2819-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b2819-129">-Confirm</span></span>
<span data-ttu-id="b2819-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b2819-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2819-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2819-131">-WhatIf</span></span>
<span data-ttu-id="b2819-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b2819-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2819-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b2819-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2819-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2819-134">CommonParameters</span></span>
<span data-ttu-id="b2819-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2819-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2819-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2819-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2819-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b2819-137">INPUTS</span></span>

### <span data-ttu-id="b2819-138">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b2819-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

### <span data-ttu-id="b2819-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b2819-139">System.String</span></span>

## <span data-ttu-id="b2819-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b2819-140">OUTPUTS</span></span>

### <span data-ttu-id="b2819-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b2819-141">System.Boolean</span></span>

## <span data-ttu-id="b2819-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b2819-142">NOTES</span></span>

## <span data-ttu-id="b2819-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b2819-143">RELATED LINKS</span></span>

[<span data-ttu-id="b2819-144">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b2819-144">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="b2819-145">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b2819-145">Get-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)

