---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
ms.openlocfilehash: 41bdf9bbc33239590f9d3a6db4ffaa88ddf752a1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408624"
---
# <span data-ttu-id="171db-101">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="171db-101">Remove-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="171db-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="171db-102">SYNOPSIS</span></span>
<span data-ttu-id="171db-103">Tar bort en container-registerpost.</span><span class="sxs-lookup"><span data-stu-id="171db-103">Removes a container registry replication.</span></span>

## <span data-ttu-id="171db-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="171db-104">SYNTAX</span></span>

### <span data-ttu-id="171db-105">NameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="171db-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="171db-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="171db-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -Replication <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="171db-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="171db-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="171db-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="171db-108">DESCRIPTION</span></span>
<span data-ttu-id="171db-109">Remove-AzContainerRegistryReplication cmdlet tar bort en behållar registrering.</span><span class="sxs-lookup"><span data-stu-id="171db-109">The Remove-AzContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="171db-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="171db-110">EXAMPLES</span></span>

### <span data-ttu-id="171db-111">Exempel 1: tar bort en container-registerpost.</span><span class="sxs-lookup"><span data-stu-id="171db-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="171db-112">Tar bort en container-registerpost.</span><span class="sxs-lookup"><span data-stu-id="171db-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="171db-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="171db-113">PARAMETERS</span></span>

### <span data-ttu-id="171db-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="171db-114">-DefaultProfile</span></span>
<span data-ttu-id="171db-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="171db-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="171db-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="171db-116">-Name</span></span>
<span data-ttu-id="171db-117">Namn på container Registry.</span><span class="sxs-lookup"><span data-stu-id="171db-117">Container Registry Replication Name.</span></span>
<span data-ttu-id="171db-118">Standardvärdet för plats namnet.</span><span class="sxs-lookup"><span data-stu-id="171db-118">Default to the location name.</span></span>

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

### <span data-ttu-id="171db-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="171db-119">-PassThru</span></span>
<span data-ttu-id="171db-120">Anger att denna cmdlet returnerar sant om borttagningen lyckades.</span><span class="sxs-lookup"><span data-stu-id="171db-120">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="171db-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="171db-121">-RegistryName</span></span>
<span data-ttu-id="171db-122">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="171db-122">Container Registry Name.</span></span>

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

### <span data-ttu-id="171db-123">-Replikering</span><span class="sxs-lookup"><span data-stu-id="171db-123">-Replication</span></span>
<span data-ttu-id="171db-124">Behållarobjekt för container.</span><span class="sxs-lookup"><span data-stu-id="171db-124">Container Registry Object.</span></span>

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

### <span data-ttu-id="171db-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="171db-125">-ResourceGroupName</span></span>
<span data-ttu-id="171db-126">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="171db-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="171db-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="171db-127">-ResourceId</span></span>
<span data-ttu-id="171db-128">Resurs-ID för behållar registrering</span><span class="sxs-lookup"><span data-stu-id="171db-128">The container registry replication resource id</span></span>

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

### <span data-ttu-id="171db-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="171db-129">-Confirm</span></span>
<span data-ttu-id="171db-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="171db-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="171db-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="171db-131">-WhatIf</span></span>
<span data-ttu-id="171db-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="171db-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="171db-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="171db-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="171db-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="171db-134">CommonParameters</span></span>
<span data-ttu-id="171db-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="171db-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="171db-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="171db-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="171db-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="171db-137">INPUTS</span></span>

### <span data-ttu-id="171db-138">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="171db-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

### <span data-ttu-id="171db-139">System. String</span><span class="sxs-lookup"><span data-stu-id="171db-139">System.String</span></span>

## <span data-ttu-id="171db-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="171db-140">OUTPUTS</span></span>

### <span data-ttu-id="171db-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="171db-141">System.Boolean</span></span>

## <span data-ttu-id="171db-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="171db-142">NOTES</span></span>

## <span data-ttu-id="171db-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="171db-143">RELATED LINKS</span></span>

[<span data-ttu-id="171db-144">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="171db-144">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="171db-145">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="171db-145">Get-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)

