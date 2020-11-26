---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
ms.openlocfilehash: 8dc06a9ce860dfb6e01c79674dd414eedb51df17
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271399"
---
# <span data-ttu-id="e0302-101">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e0302-101">Remove-AzServiceFabricApplication</span></span>

## <span data-ttu-id="e0302-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e0302-102">SYNOPSIS</span></span>
<span data-ttu-id="e0302-103">Ta bort ett program från klustret.</span><span class="sxs-lookup"><span data-stu-id="e0302-103">Remove an application from the cluster.</span></span> <span data-ttu-id="e0302-104">Detta tar bort alla tjänster under programmet.</span><span class="sxs-lookup"><span data-stu-id="e0302-104">This will remove all the services under the application.</span></span>

## <span data-ttu-id="e0302-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e0302-105">SYNTAX</span></span>

### <span data-ttu-id="e0302-106">ByResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="e0302-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0302-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e0302-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplication -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0302-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e0302-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplication -InputObject <PSApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0302-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e0302-109">DESCRIPTION</span></span>
<span data-ttu-id="e0302-110">Denna cmdlet tar bort ett program från klustret.</span><span class="sxs-lookup"><span data-stu-id="e0302-110">This cmdlet removes an application form the cluster.</span></span> <span data-ttu-id="e0302-111">Detta tar bort alla tjänster under program resursen.</span><span class="sxs-lookup"><span data-stu-id="e0302-111">This will remove all the services, if any, under the application resource.</span></span>

## <span data-ttu-id="e0302-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e0302-112">EXAMPLES</span></span>

### <span data-ttu-id="e0302-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e0302-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Remove-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="e0302-114">I det här exemplet tas programmet "testApp" bort under resurs gruppen "testRG" och kluster "testCluster".</span><span class="sxs-lookup"><span data-stu-id="e0302-114">This example removes the application "testApp" under the resource group "testRG" and cluster "testCluster".</span></span>

## <span data-ttu-id="e0302-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e0302-115">PARAMETERS</span></span>

### <span data-ttu-id="e0302-116">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="e0302-116">-ClusterName</span></span>
<span data-ttu-id="e0302-117">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="e0302-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="e0302-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0302-118">-DefaultProfile</span></span>
<span data-ttu-id="e0302-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e0302-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0302-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e0302-120">-Force</span></span>
<span data-ttu-id="e0302-121">Ta bort utan att fråga.</span><span class="sxs-lookup"><span data-stu-id="e0302-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="e0302-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0302-122">-InputObject</span></span>
<span data-ttu-id="e0302-123">Program resursen.</span><span class="sxs-lookup"><span data-stu-id="e0302-123">The application resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0302-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="e0302-124">-Name</span></span>
<span data-ttu-id="e0302-125">Ange namnet på programmet.</span><span class="sxs-lookup"><span data-stu-id="e0302-125">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0302-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0302-126">-PassThru</span></span>
<span data-ttu-id="e0302-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="e0302-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e0302-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0302-128">-ResourceGroupName</span></span>
<span data-ttu-id="e0302-129">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e0302-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="e0302-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0302-130">-ResourceId</span></span>
<span data-ttu-id="e0302-131">Programmets ResourceId.</span><span class="sxs-lookup"><span data-stu-id="e0302-131">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="e0302-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e0302-132">-Confirm</span></span>
<span data-ttu-id="e0302-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e0302-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0302-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0302-134">-WhatIf</span></span>
<span data-ttu-id="e0302-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e0302-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0302-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e0302-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0302-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0302-137">CommonParameters</span></span>
<span data-ttu-id="e0302-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0302-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0302-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0302-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0302-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e0302-140">INPUTS</span></span>

### <span data-ttu-id="e0302-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e0302-141">System.String</span></span>

### <span data-ttu-id="e0302-142">Microsoft. Azure. commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="e0302-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="e0302-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e0302-143">OUTPUTS</span></span>

### <span data-ttu-id="e0302-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e0302-144">System.Boolean</span></span>

## <span data-ttu-id="e0302-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e0302-145">NOTES</span></span>

## <span data-ttu-id="e0302-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e0302-146">RELATED LINKS</span></span>