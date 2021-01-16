---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
ms.openlocfilehash: 2a41a61b67ea77e2927acf5eef7b7d520464978a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409568"
---
# <span data-ttu-id="fcd97-101">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="fcd97-101">Remove-AzServiceFabricService</span></span>

## <span data-ttu-id="fcd97-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fcd97-102">SYNOPSIS</span></span>
<span data-ttu-id="fcd97-103">Ta bort en tjänst från klustret.</span><span class="sxs-lookup"><span data-stu-id="fcd97-103">Remove a service from the cluster.</span></span> <span data-ttu-id="fcd97-104">Stöder endast funktioner som distribueras av ARM.</span><span class="sxs-lookup"><span data-stu-id="fcd97-104">Only supports ARM deployed services.</span></span>

## <span data-ttu-id="fcd97-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fcd97-105">SYNTAX</span></span>

### <span data-ttu-id="fcd97-106">ByResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="fcd97-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcd97-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fcd97-107">ByResourceId</span></span>
```
Remove-AzServiceFabricService -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcd97-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fcd97-108">ByInputObject</span></span>
```
Remove-AzServiceFabricService -InputObject <PSService> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcd97-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fcd97-109">DESCRIPTION</span></span>
<span data-ttu-id="fcd97-110">Denna cmdlet tar bort en tjänst från klustret.</span><span class="sxs-lookup"><span data-stu-id="fcd97-110">This cmdlet removes a service form the cluster.</span></span>

## <span data-ttu-id="fcd97-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fcd97-111">EXAMPLES</span></span>

### <span data-ttu-id="fcd97-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fcd97-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> Remove-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="fcd97-113">I det här exemplet tas tjänsten bort "testApp ~ testService1".</span><span class="sxs-lookup"><span data-stu-id="fcd97-113">This example will remove the service "testApp~testService1".</span></span>

## <span data-ttu-id="fcd97-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fcd97-114">PARAMETERS</span></span>

### <span data-ttu-id="fcd97-115">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="fcd97-115">-ApplicationName</span></span>
<span data-ttu-id="fcd97-116">Ange namnet på programmet.</span><span class="sxs-lookup"><span data-stu-id="fcd97-116">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcd97-117">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="fcd97-117">-ClusterName</span></span>
<span data-ttu-id="fcd97-118">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="fcd97-118">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcd97-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcd97-119">-DefaultProfile</span></span>
<span data-ttu-id="fcd97-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fcd97-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcd97-121">-Force</span><span class="sxs-lookup"><span data-stu-id="fcd97-121">-Force</span></span>
<span data-ttu-id="fcd97-122">Ta bort utan att fråga.</span><span class="sxs-lookup"><span data-stu-id="fcd97-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="fcd97-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcd97-123">-InputObject</span></span>
<span data-ttu-id="fcd97-124">Tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="fcd97-124">The service resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSService
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fcd97-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="fcd97-125">-Name</span></span>
<span data-ttu-id="fcd97-126">Ange namnet på tjänsten.</span><span class="sxs-lookup"><span data-stu-id="fcd97-126">Specify the name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ServiceName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcd97-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fcd97-127">-PassThru</span></span>
<span data-ttu-id="fcd97-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="fcd97-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="fcd97-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcd97-129">-ResourceGroupName</span></span>
<span data-ttu-id="fcd97-130">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="fcd97-130">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcd97-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fcd97-131">-ResourceId</span></span>
<span data-ttu-id="fcd97-132">Tjänstens ResourceId.</span><span class="sxs-lookup"><span data-stu-id="fcd97-132">Arm ResourceId of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcd97-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fcd97-133">-Confirm</span></span>
<span data-ttu-id="fcd97-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fcd97-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcd97-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcd97-135">-WhatIf</span></span>
<span data-ttu-id="fcd97-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fcd97-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcd97-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fcd97-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcd97-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcd97-138">CommonParameters</span></span>
<span data-ttu-id="fcd97-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcd97-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcd97-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fcd97-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcd97-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fcd97-141">INPUTS</span></span>

### <span data-ttu-id="fcd97-142">System. String</span><span class="sxs-lookup"><span data-stu-id="fcd97-142">System.String</span></span>

### <span data-ttu-id="fcd97-143">Microsoft. Azure. commands. ServiceFabric. Models. PSService</span><span class="sxs-lookup"><span data-stu-id="fcd97-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="fcd97-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fcd97-144">OUTPUTS</span></span>

### <span data-ttu-id="fcd97-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fcd97-145">System.Boolean</span></span>

## <span data-ttu-id="fcd97-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fcd97-146">NOTES</span></span>

## <span data-ttu-id="fcd97-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fcd97-147">RELATED LINKS</span></span>
