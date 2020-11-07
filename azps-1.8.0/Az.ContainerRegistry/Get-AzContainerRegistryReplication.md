---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
ms.openlocfilehash: 21e821a4575fb918599ad2315c569a7f270e0a84
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754413"
---
# <span data-ttu-id="73aa1-101">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="73aa1-101">Get-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="73aa1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="73aa1-102">SYNOPSIS</span></span>
<span data-ttu-id="73aa1-103">Hämtar en replikering av ett behållar register.</span><span class="sxs-lookup"><span data-stu-id="73aa1-103">Gets a replication of a container registry.</span></span>

## <span data-ttu-id="73aa1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="73aa1-104">SYNTAX</span></span>

### <span data-ttu-id="73aa1-105">ListReplicationByNameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="73aa1-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73aa1-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="73aa1-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73aa1-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73aa1-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73aa1-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73aa1-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="73aa1-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73aa1-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="73aa1-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="73aa1-110">DESCRIPTION</span></span>
<span data-ttu-id="73aa1-111">Med den här Get-AzContainerRegistryReplication cmdleten får du en angiven replikering av ett behållar-register eller alla replikeringar av ett behållar register.</span><span class="sxs-lookup"><span data-stu-id="73aa1-111">The Get-AzContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="73aa1-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="73aa1-112">EXAMPLES</span></span>

### <span data-ttu-id="73aa1-113">Exempel 1: hämtar en angiven replikering av ett behållar register</span><span class="sxs-lookup"><span data-stu-id="73aa1-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="73aa1-114">Hämtar en angiven replikering av ett behållar register</span><span class="sxs-lookup"><span data-stu-id="73aa1-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="73aa1-115">Exempel 2: hämtar alla replikeringar av en behållar register</span><span class="sxs-lookup"><span data-stu-id="73aa1-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="73aa1-116">Hämtar alla replikeringar av en behållar register</span><span class="sxs-lookup"><span data-stu-id="73aa1-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="73aa1-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="73aa1-117">PARAMETERS</span></span>

### <span data-ttu-id="73aa1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73aa1-118">-DefaultProfile</span></span>
<span data-ttu-id="73aa1-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="73aa1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73aa1-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="73aa1-120">-Name</span></span>
<span data-ttu-id="73aa1-121">Namn på container Registry.</span><span class="sxs-lookup"><span data-stu-id="73aa1-121">Container Registry Replication Name.</span></span>

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

### <span data-ttu-id="73aa1-122">-Register</span><span class="sxs-lookup"><span data-stu-id="73aa1-122">-Registry</span></span>
<span data-ttu-id="73aa1-123">Behållarobjekt för container.</span><span class="sxs-lookup"><span data-stu-id="73aa1-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="73aa1-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="73aa1-124">-RegistryName</span></span>
<span data-ttu-id="73aa1-125">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="73aa1-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="73aa1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73aa1-126">-ResourceGroupName</span></span>
<span data-ttu-id="73aa1-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="73aa1-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="73aa1-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73aa1-128">-ResourceId</span></span>
<span data-ttu-id="73aa1-129">Resurs-ID för behållar registrering</span><span class="sxs-lookup"><span data-stu-id="73aa1-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="73aa1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73aa1-130">CommonParameters</span></span>
<span data-ttu-id="73aa1-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73aa1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73aa1-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73aa1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73aa1-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="73aa1-133">INPUTS</span></span>

### <span data-ttu-id="73aa1-134">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="73aa1-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="73aa1-135">System. String</span><span class="sxs-lookup"><span data-stu-id="73aa1-135">System.String</span></span>

## <span data-ttu-id="73aa1-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="73aa1-136">OUTPUTS</span></span>

### <span data-ttu-id="73aa1-137">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="73aa1-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="73aa1-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="73aa1-138">NOTES</span></span>

## <span data-ttu-id="73aa1-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="73aa1-139">RELATED LINKS</span></span>

[<span data-ttu-id="73aa1-140">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="73aa1-140">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="73aa1-141">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="73aa1-141">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)