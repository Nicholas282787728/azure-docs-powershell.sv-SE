---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: 7dfb080ae20c583467add8ce298b03199a4f89dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757105"
---
# <span data-ttu-id="af859-101">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="af859-101">Remove-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="af859-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af859-102">SYNOPSIS</span></span>
<span data-ttu-id="af859-103">Tar bort en container-registerpost.</span><span class="sxs-lookup"><span data-stu-id="af859-103">Removes a container registry replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af859-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af859-104">SYNTAX</span></span>

### <span data-ttu-id="af859-105">NameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="af859-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String>
 [-RegistryName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af859-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="af859-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -Replicatoin <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af859-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="af859-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af859-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af859-108">DESCRIPTION</span></span>
<span data-ttu-id="af859-109">Remove-AzureRmContainerRegistryReplication cmdlet tar bort en behållar registrering.</span><span class="sxs-lookup"><span data-stu-id="af859-109">The Remove-AzureRmContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="af859-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af859-110">EXAMPLES</span></span>

### <span data-ttu-id="af859-111">Exempel 1: tar bort en container-registerpost.</span><span class="sxs-lookup"><span data-stu-id="af859-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="af859-112">Tar bort en container-registerpost.</span><span class="sxs-lookup"><span data-stu-id="af859-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="af859-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af859-113">PARAMETERS</span></span>

### <span data-ttu-id="af859-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af859-114">-DefaultProfile</span></span>
<span data-ttu-id="af859-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="af859-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af859-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="af859-116">-Name</span></span>
<span data-ttu-id="af859-117">Namn på container Registry.</span><span class="sxs-lookup"><span data-stu-id="af859-117">Container Registry Replication Name.</span></span>
<span data-ttu-id="af859-118">Standardvärdet för plats namnet.</span><span class="sxs-lookup"><span data-stu-id="af859-118">Default to the location name.</span></span>

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

### <span data-ttu-id="af859-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af859-119">-PassThru</span></span>
<span data-ttu-id="af859-120">Anger att denna cmdlet returnerar sant om borttagningen lyckades.</span><span class="sxs-lookup"><span data-stu-id="af859-120">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="af859-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="af859-121">-RegistryName</span></span>
<span data-ttu-id="af859-122">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="af859-122">Container Registry Name.</span></span>

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

### <span data-ttu-id="af859-123">-Replicatoin</span><span class="sxs-lookup"><span data-stu-id="af859-123">-Replicatoin</span></span>
<span data-ttu-id="af859-124">Behållarobjekt för container.</span><span class="sxs-lookup"><span data-stu-id="af859-124">Container Registry Object.</span></span>

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

### <span data-ttu-id="af859-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af859-125">-ResourceGroupName</span></span>
<span data-ttu-id="af859-126">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="af859-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="af859-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af859-127">-ResourceId</span></span>
<span data-ttu-id="af859-128">Resurs-ID för behållar registrering</span><span class="sxs-lookup"><span data-stu-id="af859-128">The container registry replication resource id</span></span>

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

### <span data-ttu-id="af859-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="af859-129">-Confirm</span></span>
<span data-ttu-id="af859-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="af859-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af859-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af859-131">-WhatIf</span></span>
<span data-ttu-id="af859-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="af859-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af859-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="af859-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af859-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af859-134">CommonParameters</span></span>
<span data-ttu-id="af859-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af859-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af859-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af859-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af859-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af859-137">INPUTS</span></span>

### <span data-ttu-id="af859-138">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="af859-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>
<span data-ttu-id="af859-139">Parametrar: Replicatoin (ByValue)</span><span class="sxs-lookup"><span data-stu-id="af859-139">Parameters: Replicatoin (ByValue)</span></span>

### <span data-ttu-id="af859-140">System. String</span><span class="sxs-lookup"><span data-stu-id="af859-140">System.String</span></span>

## <span data-ttu-id="af859-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af859-141">OUTPUTS</span></span>

### <span data-ttu-id="af859-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="af859-142">System.Boolean</span></span>

## <span data-ttu-id="af859-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af859-143">NOTES</span></span>

## <span data-ttu-id="af859-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af859-144">RELATED LINKS</span></span>

[<span data-ttu-id="af859-145">New-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="af859-145">New-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="af859-146">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="af859-146">Get-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)

