---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
ms.openlocfilehash: 41bdf9bbc33239590f9d3a6db4ffaa88ddf752a1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319568"
---
# <span data-ttu-id="25efd-101">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="25efd-101">Remove-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="25efd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="25efd-102">SYNOPSIS</span></span>
<span data-ttu-id="25efd-103">Tar bort en container-registerpost.</span><span class="sxs-lookup"><span data-stu-id="25efd-103">Removes a container registry replication.</span></span>

## <span data-ttu-id="25efd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="25efd-104">SYNTAX</span></span>

### <span data-ttu-id="25efd-105">NameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="25efd-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25efd-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25efd-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -Replication <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25efd-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25efd-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25efd-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="25efd-108">DESCRIPTION</span></span>
<span data-ttu-id="25efd-109">Remove-AzContainerRegistryReplication cmdlet tar bort en behållar registrering.</span><span class="sxs-lookup"><span data-stu-id="25efd-109">The Remove-AzContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="25efd-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="25efd-110">EXAMPLES</span></span>

### <span data-ttu-id="25efd-111">Exempel 1: tar bort en container-registerpost.</span><span class="sxs-lookup"><span data-stu-id="25efd-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="25efd-112">Tar bort en container-registerpost.</span><span class="sxs-lookup"><span data-stu-id="25efd-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="25efd-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="25efd-113">PARAMETERS</span></span>

### <span data-ttu-id="25efd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25efd-114">-DefaultProfile</span></span>
<span data-ttu-id="25efd-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="25efd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25efd-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="25efd-116">-Name</span></span>
<span data-ttu-id="25efd-117">Namn på container Registry.</span><span class="sxs-lookup"><span data-stu-id="25efd-117">Container Registry Replication Name.</span></span>
<span data-ttu-id="25efd-118">Standardvärdet för plats namnet.</span><span class="sxs-lookup"><span data-stu-id="25efd-118">Default to the location name.</span></span>

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

### <span data-ttu-id="25efd-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25efd-119">-PassThru</span></span>
<span data-ttu-id="25efd-120">Anger att denna cmdlet returnerar sant om borttagningen lyckades.</span><span class="sxs-lookup"><span data-stu-id="25efd-120">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="25efd-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="25efd-121">-RegistryName</span></span>
<span data-ttu-id="25efd-122">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="25efd-122">Container Registry Name.</span></span>

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

### <span data-ttu-id="25efd-123">-Replikering</span><span class="sxs-lookup"><span data-stu-id="25efd-123">-Replication</span></span>
<span data-ttu-id="25efd-124">Behållarobjekt för container.</span><span class="sxs-lookup"><span data-stu-id="25efd-124">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication
Parameter Sets: ReplicationObjectParameterSet
Aliases: Replicatoin

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25efd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25efd-125">-ResourceGroupName</span></span>
<span data-ttu-id="25efd-126">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="25efd-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="25efd-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25efd-127">-ResourceId</span></span>
<span data-ttu-id="25efd-128">Resurs-ID för behållar registrering</span><span class="sxs-lookup"><span data-stu-id="25efd-128">The container registry replication resource id</span></span>

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

### <span data-ttu-id="25efd-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="25efd-129">-Confirm</span></span>
<span data-ttu-id="25efd-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="25efd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25efd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25efd-131">-WhatIf</span></span>
<span data-ttu-id="25efd-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="25efd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25efd-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="25efd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25efd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25efd-134">CommonParameters</span></span>
<span data-ttu-id="25efd-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25efd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25efd-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25efd-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25efd-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="25efd-137">INPUTS</span></span>

### <span data-ttu-id="25efd-138">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="25efd-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

### <span data-ttu-id="25efd-139">System. String</span><span class="sxs-lookup"><span data-stu-id="25efd-139">System.String</span></span>

## <span data-ttu-id="25efd-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="25efd-140">OUTPUTS</span></span>

### <span data-ttu-id="25efd-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="25efd-141">System.Boolean</span></span>

## <span data-ttu-id="25efd-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="25efd-142">NOTES</span></span>

## <span data-ttu-id="25efd-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="25efd-143">RELATED LINKS</span></span>

[<span data-ttu-id="25efd-144">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="25efd-144">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="25efd-145">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="25efd-145">Get-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)

