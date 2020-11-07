---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
ms.openlocfilehash: 1314eb4d6bf4cfa802e0c6f40cc5ae7646209572
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919153"
---
# <span data-ttu-id="35ce2-101">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="35ce2-101">Remove-AzServiceFabricService</span></span>

## <span data-ttu-id="35ce2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="35ce2-102">SYNOPSIS</span></span>
<span data-ttu-id="35ce2-103">Ta bort en tjänst från klustret.</span><span class="sxs-lookup"><span data-stu-id="35ce2-103">Remove a service from the cluster.</span></span>

## <span data-ttu-id="35ce2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="35ce2-104">SYNTAX</span></span>

### <span data-ttu-id="35ce2-105">ByResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="35ce2-105">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="35ce2-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="35ce2-106">ByResourceId</span></span>
```
Remove-AzServiceFabricService -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35ce2-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="35ce2-107">ByInputObject</span></span>
```
Remove-AzServiceFabricService -InputObject <PSService> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35ce2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="35ce2-108">DESCRIPTION</span></span>
<span data-ttu-id="35ce2-109">Denna cmdlet tar bort en tjänst från klustret.</span><span class="sxs-lookup"><span data-stu-id="35ce2-109">This cmdlet removes a service form the cluster.</span></span>

## <span data-ttu-id="35ce2-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="35ce2-110">EXAMPLES</span></span>

### <span data-ttu-id="35ce2-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="35ce2-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> Remove-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="35ce2-112">I det här exemplet tas tjänsten bort "testApp ~ testService1".</span><span class="sxs-lookup"><span data-stu-id="35ce2-112">This example will remove the service "testApp~testService1".</span></span>

## <span data-ttu-id="35ce2-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="35ce2-113">PARAMETERS</span></span>

### <span data-ttu-id="35ce2-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="35ce2-114">-ApplicationName</span></span>
<span data-ttu-id="35ce2-115">Ange namnet på programmet.</span><span class="sxs-lookup"><span data-stu-id="35ce2-115">Specify the name of the application.</span></span>

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

### <span data-ttu-id="35ce2-116">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="35ce2-116">-ClusterName</span></span>
<span data-ttu-id="35ce2-117">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="35ce2-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="35ce2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35ce2-118">-DefaultProfile</span></span>
<span data-ttu-id="35ce2-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="35ce2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35ce2-120">-Force</span><span class="sxs-lookup"><span data-stu-id="35ce2-120">-Force</span></span>
<span data-ttu-id="35ce2-121">Ta bort utan att fråga.</span><span class="sxs-lookup"><span data-stu-id="35ce2-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="35ce2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35ce2-122">-InputObject</span></span>
<span data-ttu-id="35ce2-123">Tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="35ce2-123">The service resource.</span></span>

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

### <span data-ttu-id="35ce2-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="35ce2-124">-Name</span></span>
<span data-ttu-id="35ce2-125">Ange namnet på tjänsten.</span><span class="sxs-lookup"><span data-stu-id="35ce2-125">Specify the name of the service.</span></span>

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

### <span data-ttu-id="35ce2-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35ce2-126">-PassThru</span></span>
<span data-ttu-id="35ce2-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="35ce2-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="35ce2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35ce2-128">-ResourceGroupName</span></span>
<span data-ttu-id="35ce2-129">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="35ce2-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="35ce2-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35ce2-130">-ResourceId</span></span>
<span data-ttu-id="35ce2-131">Tjänstens ResourceId.</span><span class="sxs-lookup"><span data-stu-id="35ce2-131">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="35ce2-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="35ce2-132">-Confirm</span></span>
<span data-ttu-id="35ce2-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="35ce2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35ce2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35ce2-134">-WhatIf</span></span>
<span data-ttu-id="35ce2-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="35ce2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35ce2-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="35ce2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35ce2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35ce2-137">CommonParameters</span></span>
<span data-ttu-id="35ce2-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35ce2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35ce2-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35ce2-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35ce2-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="35ce2-140">INPUTS</span></span>

### <span data-ttu-id="35ce2-141">System. String</span><span class="sxs-lookup"><span data-stu-id="35ce2-141">System.String</span></span>

### <span data-ttu-id="35ce2-142">Microsoft. Azure. commands. ServiceFabric. Models. PSService</span><span class="sxs-lookup"><span data-stu-id="35ce2-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="35ce2-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="35ce2-143">OUTPUTS</span></span>

### <span data-ttu-id="35ce2-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="35ce2-144">System.Boolean</span></span>

## <span data-ttu-id="35ce2-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="35ce2-145">NOTES</span></span>

## <span data-ttu-id="35ce2-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="35ce2-146">RELATED LINKS</span></span>
