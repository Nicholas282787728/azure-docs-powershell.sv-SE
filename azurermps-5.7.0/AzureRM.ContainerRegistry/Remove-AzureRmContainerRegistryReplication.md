---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: 824b3226b29ba381b9ed963bf6a21f4691c17733
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755970"
---
# <span data-ttu-id="78124-101">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="78124-101">Remove-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="78124-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="78124-102">SYNOPSIS</span></span>
<span data-ttu-id="78124-103">Tar bort en container-registerpost.</span><span class="sxs-lookup"><span data-stu-id="78124-103">Removes a container registry replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78124-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="78124-104">SYNTAX</span></span>

### <span data-ttu-id="78124-105">NameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="78124-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String>
 [-RegistryName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78124-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78124-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -Replicatoin <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78124-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78124-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78124-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="78124-108">DESCRIPTION</span></span>
<span data-ttu-id="78124-109">Remove-AzureRmContainerRegistryReplication cmdlet tar bort en behållar registrering.</span><span class="sxs-lookup"><span data-stu-id="78124-109">The Remove-AzureRmContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="78124-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="78124-110">EXAMPLES</span></span>

### <span data-ttu-id="78124-111">Exempel 1: tar bort en container-registerpost.</span><span class="sxs-lookup"><span data-stu-id="78124-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="78124-112">Tar bort en container-registerpost.</span><span class="sxs-lookup"><span data-stu-id="78124-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="78124-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="78124-113">PARAMETERS</span></span>

### <span data-ttu-id="78124-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="78124-114">-Confirm</span></span>
<span data-ttu-id="78124-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="78124-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78124-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78124-116">-DefaultProfile</span></span>
<span data-ttu-id="78124-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="78124-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78124-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="78124-118">-Name</span></span>
<span data-ttu-id="78124-119">Namn på container Registry.</span><span class="sxs-lookup"><span data-stu-id="78124-119">Container Registry Replication Name.</span></span>
<span data-ttu-id="78124-120">Standardvärdet för plats namnet.</span><span class="sxs-lookup"><span data-stu-id="78124-120">Default to the location name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78124-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="78124-121">-RegistryName</span></span>
<span data-ttu-id="78124-122">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="78124-122">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78124-123">-Replicatoin</span><span class="sxs-lookup"><span data-stu-id="78124-123">-Replicatoin</span></span>
<span data-ttu-id="78124-124">Behållarobjekt för container.</span><span class="sxs-lookup"><span data-stu-id="78124-124">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistryReplication
Parameter Sets: ReplicationObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78124-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78124-125">-ResourceGroupName</span></span>
<span data-ttu-id="78124-126">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="78124-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78124-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78124-127">-ResourceId</span></span>
<span data-ttu-id="78124-128">Resurs-ID för behållar registrering</span><span class="sxs-lookup"><span data-stu-id="78124-128">The container registry replication resource id</span></span>

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

### <span data-ttu-id="78124-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78124-129">-WhatIf</span></span>
<span data-ttu-id="78124-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="78124-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78124-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="78124-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78124-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78124-132">-PassThru</span></span>
<span data-ttu-id="78124-133">Anger att denna cmdlet returnerar sant om borttagningen lyckades.</span><span class="sxs-lookup"><span data-stu-id="78124-133">Indicates that this cmdlet returns true if the removal was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78124-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78124-134">CommonParameters</span></span>
<span data-ttu-id="78124-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78124-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78124-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78124-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78124-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="78124-137">INPUTS</span></span>

### <span data-ttu-id="78124-138">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="78124-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>
<span data-ttu-id="78124-139">System. String</span><span class="sxs-lookup"><span data-stu-id="78124-139">System.String</span></span>

## <span data-ttu-id="78124-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="78124-140">OUTPUTS</span></span>

### <span data-ttu-id="78124-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="78124-141">System.Object</span></span>

## <span data-ttu-id="78124-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="78124-142">NOTES</span></span>

## <span data-ttu-id="78124-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="78124-143">RELATED LINKS</span></span>

[<span data-ttu-id="78124-144">New-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="78124-144">New-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="78124-145">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="78124-145">Get-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)

