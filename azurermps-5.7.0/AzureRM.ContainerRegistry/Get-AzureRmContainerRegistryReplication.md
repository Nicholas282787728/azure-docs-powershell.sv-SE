---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: db03414e9cebe4c1593013a928b8a66d9b70bd91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575703"
---
# <span data-ttu-id="666d8-101">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="666d8-101">Get-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="666d8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="666d8-102">SYNOPSIS</span></span>
<span data-ttu-id="666d8-103">Hämtar en replikering av ett behållar register.</span><span class="sxs-lookup"><span data-stu-id="666d8-103">Gets a replication of a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="666d8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="666d8-104">SYNTAX</span></span>

### <span data-ttu-id="666d8-105">ListReplicationByNameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="666d8-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="666d8-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="666d8-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="666d8-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="666d8-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="666d8-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="666d8-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="666d8-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="666d8-109">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="666d8-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="666d8-110">DESCRIPTION</span></span>
<span data-ttu-id="666d8-111">Med den här Get-AzureRmContainerRegistryReplication cmdleten får du en angiven replikering av ett behållar-register eller alla replikeringar av ett behållar register.</span><span class="sxs-lookup"><span data-stu-id="666d8-111">The Get-AzureRmContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="666d8-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="666d8-112">EXAMPLES</span></span>

### <span data-ttu-id="666d8-113">Exempel 1: hämtar en angiven replikering av ett behållar register</span><span class="sxs-lookup"><span data-stu-id="666d8-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="666d8-114">Hämtar en angiven replikering av ett behållar register</span><span class="sxs-lookup"><span data-stu-id="666d8-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="666d8-115">Exempel 2: hämtar alla replikeringar av en behållar register</span><span class="sxs-lookup"><span data-stu-id="666d8-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="666d8-116">Hämtar alla replikeringar av en behållar register</span><span class="sxs-lookup"><span data-stu-id="666d8-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="666d8-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="666d8-117">PARAMETERS</span></span>

### <span data-ttu-id="666d8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="666d8-118">-DefaultProfile</span></span>
<span data-ttu-id="666d8-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="666d8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="666d8-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="666d8-120">-Name</span></span>
<span data-ttu-id="666d8-121">Namn på container Registry.</span><span class="sxs-lookup"><span data-stu-id="666d8-121">Container Registry Replication Name.</span></span>

```yaml
Type: String
Parameter Sets: ShowReplicationByNameResourceGroupParameterSet, ShowReplicationByRegistryObjectParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="666d8-122">-Register</span><span class="sxs-lookup"><span data-stu-id="666d8-122">-Registry</span></span>
<span data-ttu-id="666d8-123">Behållarobjekt för container.</span><span class="sxs-lookup"><span data-stu-id="666d8-123">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: ShowReplicationByRegistryObjectParameterSet, ListReplicationByRegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="666d8-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="666d8-124">-RegistryName</span></span>
<span data-ttu-id="666d8-125">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="666d8-125">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="666d8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="666d8-126">-ResourceGroupName</span></span>
<span data-ttu-id="666d8-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="666d8-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="666d8-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="666d8-128">-ResourceId</span></span>
<span data-ttu-id="666d8-129">Resurs-ID för behållar registrering</span><span class="sxs-lookup"><span data-stu-id="666d8-129">The container registry replication resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="666d8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="666d8-130">CommonParameters</span></span>
<span data-ttu-id="666d8-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="666d8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="666d8-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="666d8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="666d8-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="666d8-133">INPUTS</span></span>

### <span data-ttu-id="666d8-134">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="666d8-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="666d8-135">System. String</span><span class="sxs-lookup"><span data-stu-id="666d8-135">System.String</span></span>

## <span data-ttu-id="666d8-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="666d8-136">OUTPUTS</span></span>

### <span data-ttu-id="666d8-137">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="666d8-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>
<span data-ttu-id="666d8-138">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistryReplication []</span><span class="sxs-lookup"><span data-stu-id="666d8-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication[]</span></span>

## <span data-ttu-id="666d8-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="666d8-139">NOTES</span></span>

## <span data-ttu-id="666d8-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="666d8-140">RELATED LINKS</span></span>

[<span data-ttu-id="666d8-141">New-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="666d8-141">New-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="666d8-142">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="666d8-142">Remove-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)
