---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
ms.openlocfilehash: 57b482368834d91e36a3f557c9657c82cea24f4e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926278"
---
# <span data-ttu-id="cbda3-101">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="cbda3-101">Get-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="cbda3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cbda3-102">SYNOPSIS</span></span>
<span data-ttu-id="cbda3-103">Hämtar en replikering av ett behållar register.</span><span class="sxs-lookup"><span data-stu-id="cbda3-103">Gets a replication of a container registry.</span></span>

## <span data-ttu-id="cbda3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cbda3-104">SYNTAX</span></span>

### <span data-ttu-id="cbda3-105">ListReplicationByNameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="cbda3-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbda3-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbda3-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbda3-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbda3-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbda3-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbda3-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cbda3-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbda3-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cbda3-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cbda3-110">DESCRIPTION</span></span>
<span data-ttu-id="cbda3-111">Med den här Get-AzContainerRegistryReplication cmdleten får du en angiven replikering av ett behållar-register eller alla replikeringar av ett behållar register.</span><span class="sxs-lookup"><span data-stu-id="cbda3-111">The Get-AzContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="cbda3-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cbda3-112">EXAMPLES</span></span>

### <span data-ttu-id="cbda3-113">Exempel 1: hämtar en angiven replikering av ett behållar register</span><span class="sxs-lookup"><span data-stu-id="cbda3-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="cbda3-114">Hämtar en angiven replikering av ett behållar register</span><span class="sxs-lookup"><span data-stu-id="cbda3-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="cbda3-115">Exempel 2: hämtar alla replikeringar av en behållar register</span><span class="sxs-lookup"><span data-stu-id="cbda3-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="cbda3-116">Hämtar alla replikeringar av en behållar register</span><span class="sxs-lookup"><span data-stu-id="cbda3-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="cbda3-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cbda3-117">PARAMETERS</span></span>

### <span data-ttu-id="cbda3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbda3-118">-DefaultProfile</span></span>
<span data-ttu-id="cbda3-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cbda3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbda3-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="cbda3-120">-Name</span></span>
<span data-ttu-id="cbda3-121">Namn på container Registry.</span><span class="sxs-lookup"><span data-stu-id="cbda3-121">Container Registry Replication Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShowReplicationByNameResourceGroupParameterSet, ShowReplicationByRegistryObjectParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbda3-122">-Register</span><span class="sxs-lookup"><span data-stu-id="cbda3-122">-Registry</span></span>
<span data-ttu-id="cbda3-123">Behållarobjekt för container.</span><span class="sxs-lookup"><span data-stu-id="cbda3-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: ShowReplicationByRegistryObjectParameterSet, ListReplicationByRegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbda3-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="cbda3-124">-RegistryName</span></span>
<span data-ttu-id="cbda3-125">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="cbda3-125">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbda3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbda3-126">-ResourceGroupName</span></span>
<span data-ttu-id="cbda3-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="cbda3-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbda3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cbda3-128">-ResourceId</span></span>
<span data-ttu-id="cbda3-129">Resurs-ID för behållar registrering</span><span class="sxs-lookup"><span data-stu-id="cbda3-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="cbda3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbda3-130">CommonParameters</span></span>
<span data-ttu-id="cbda3-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbda3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbda3-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cbda3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbda3-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cbda3-133">INPUTS</span></span>

### <span data-ttu-id="cbda3-134">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="cbda3-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="cbda3-135">System. String</span><span class="sxs-lookup"><span data-stu-id="cbda3-135">System.String</span></span>

## <span data-ttu-id="cbda3-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cbda3-136">OUTPUTS</span></span>

### <span data-ttu-id="cbda3-137">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="cbda3-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="cbda3-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cbda3-138">NOTES</span></span>

## <span data-ttu-id="cbda3-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cbda3-139">RELATED LINKS</span></span>

[<span data-ttu-id="cbda3-140">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="cbda3-140">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="cbda3-141">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="cbda3-141">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)