---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
ms.openlocfilehash: aadac0f7d408efd5f635d77d14f9afabfbd444d0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260121"
---
# <span data-ttu-id="889e1-101">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="889e1-101">New-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="889e1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="889e1-102">SYNOPSIS</span></span>
<span data-ttu-id="889e1-103">Skapar en container-registerpost.</span><span class="sxs-lookup"><span data-stu-id="889e1-103">Creates a container registry replication.</span></span>

## <span data-ttu-id="889e1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="889e1-104">SYNTAX</span></span>

### <span data-ttu-id="889e1-105">NameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="889e1-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String> -Location <String>
 [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="889e1-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="889e1-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="889e1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="889e1-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="889e1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="889e1-108">DESCRIPTION</span></span>
<span data-ttu-id="889e1-109">New-AzContainerRegistryReplication cmdlet skapar en ny replikering för behållar registret.</span><span class="sxs-lookup"><span data-stu-id="889e1-109">The New-AzContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="889e1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="889e1-110">EXAMPLES</span></span>

### <span data-ttu-id="889e1-111">Exempel 1: skapa en ny datareplikering för container.</span><span class="sxs-lookup"><span data-stu-id="889e1-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="889e1-112">Skapa en ny datareplikering för container.</span><span class="sxs-lookup"><span data-stu-id="889e1-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="889e1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="889e1-113">PARAMETERS</span></span>

### <span data-ttu-id="889e1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="889e1-114">-DefaultProfile</span></span>
<span data-ttu-id="889e1-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="889e1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="889e1-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="889e1-116">-Location</span></span>
<span data-ttu-id="889e1-117">Behållarens register plats.</span><span class="sxs-lookup"><span data-stu-id="889e1-117">Container Registry Location.</span></span>
<span data-ttu-id="889e1-118">Standard platsen för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="889e1-118">Default to the location of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicationLocation

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="889e1-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="889e1-119">-Name</span></span>
<span data-ttu-id="889e1-120">Namn på container Registry.</span><span class="sxs-lookup"><span data-stu-id="889e1-120">Container Registry Replication Name.</span></span>
<span data-ttu-id="889e1-121">Standardvärdet för plats namnet.</span><span class="sxs-lookup"><span data-stu-id="889e1-121">Default to the location name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicationName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="889e1-122">-Register</span><span class="sxs-lookup"><span data-stu-id="889e1-122">-Registry</span></span>
<span data-ttu-id="889e1-123">Behållarobjekt för container.</span><span class="sxs-lookup"><span data-stu-id="889e1-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="889e1-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="889e1-124">-RegistryName</span></span>
<span data-ttu-id="889e1-125">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="889e1-125">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="889e1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="889e1-126">-ResourceGroupName</span></span>
<span data-ttu-id="889e1-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="889e1-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="889e1-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="889e1-128">-ResourceId</span></span>
<span data-ttu-id="889e1-129">Resurs-ID för behållar registret</span><span class="sxs-lookup"><span data-stu-id="889e1-129">The container registry resource id</span></span>

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

### <span data-ttu-id="889e1-130">-Tagg</span><span class="sxs-lookup"><span data-stu-id="889e1-130">-Tag</span></span>
<span data-ttu-id="889e1-131">Register märken för behållare.</span><span class="sxs-lookup"><span data-stu-id="889e1-131">Container Registry Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="889e1-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="889e1-132">-Confirm</span></span>
<span data-ttu-id="889e1-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="889e1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="889e1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="889e1-134">-WhatIf</span></span>
<span data-ttu-id="889e1-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="889e1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="889e1-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="889e1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="889e1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="889e1-137">CommonParameters</span></span>
<span data-ttu-id="889e1-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="889e1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="889e1-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="889e1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="889e1-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="889e1-140">INPUTS</span></span>

### <span data-ttu-id="889e1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="889e1-141">System.String</span></span>

## <span data-ttu-id="889e1-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="889e1-142">OUTPUTS</span></span>

### <span data-ttu-id="889e1-143">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="889e1-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="889e1-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="889e1-144">NOTES</span></span>

## <span data-ttu-id="889e1-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="889e1-145">RELATED LINKS</span></span>

[<span data-ttu-id="889e1-146">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="889e1-146">Get-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="889e1-147">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="889e1-147">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)