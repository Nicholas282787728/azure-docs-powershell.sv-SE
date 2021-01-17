---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
ms.openlocfilehash: 7dbd9df3e6bd87aedcfeb80964959553bac8deca
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403523"
---
# <span data-ttu-id="b3177-101">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="b3177-101">Remove-AzServiceFabricApplication</span></span>

## <span data-ttu-id="b3177-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b3177-102">SYNOPSIS</span></span>
<span data-ttu-id="b3177-103">Ta bort ett program från klustret.</span><span class="sxs-lookup"><span data-stu-id="b3177-103">Remove an application from the cluster.</span></span> <span data-ttu-id="b3177-104">Detta tar bort alla tjänster under programmet.</span><span class="sxs-lookup"><span data-stu-id="b3177-104">This will remove all the services under the application.</span></span> <span data-ttu-id="b3177-105">Stöder endast program som distribueras av armar.</span><span class="sxs-lookup"><span data-stu-id="b3177-105">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="b3177-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b3177-106">SYNTAX</span></span>

### <span data-ttu-id="b3177-107">ByResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="b3177-107">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3177-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b3177-108">ByResourceId</span></span>
```
Remove-AzServiceFabricApplication -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3177-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b3177-109">ByInputObject</span></span>
```
Remove-AzServiceFabricApplication -InputObject <PSApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3177-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b3177-110">DESCRIPTION</span></span>
<span data-ttu-id="b3177-111">Denna cmdlet tar bort ett program från klustret.</span><span class="sxs-lookup"><span data-stu-id="b3177-111">This cmdlet removes an application form the cluster.</span></span> <span data-ttu-id="b3177-112">Detta tar bort alla tjänster under program resursen.</span><span class="sxs-lookup"><span data-stu-id="b3177-112">This will remove all the services, if any, under the application resource.</span></span>

## <span data-ttu-id="b3177-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b3177-113">EXAMPLES</span></span>

### <span data-ttu-id="b3177-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b3177-114">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Remove-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="b3177-115">I det här exemplet tas programmet "testApp" bort under resurs gruppen "testRG" och kluster "testCluster".</span><span class="sxs-lookup"><span data-stu-id="b3177-115">This example removes the application "testApp" under the resource group "testRG" and cluster "testCluster".</span></span>

## <span data-ttu-id="b3177-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b3177-116">PARAMETERS</span></span>

### <span data-ttu-id="b3177-117">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="b3177-117">-ClusterName</span></span>
<span data-ttu-id="b3177-118">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="b3177-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="b3177-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3177-119">-DefaultProfile</span></span>
<span data-ttu-id="b3177-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b3177-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3177-121">-Force</span><span class="sxs-lookup"><span data-stu-id="b3177-121">-Force</span></span>
<span data-ttu-id="b3177-122">Ta bort utan att fråga.</span><span class="sxs-lookup"><span data-stu-id="b3177-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="b3177-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3177-123">-InputObject</span></span>
<span data-ttu-id="b3177-124">Program resursen.</span><span class="sxs-lookup"><span data-stu-id="b3177-124">The application resource.</span></span>

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

### <span data-ttu-id="b3177-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="b3177-125">-Name</span></span>
<span data-ttu-id="b3177-126">Ange namnet på programmet.</span><span class="sxs-lookup"><span data-stu-id="b3177-126">Specify the name of the application.</span></span>

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

### <span data-ttu-id="b3177-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3177-127">-PassThru</span></span>
<span data-ttu-id="b3177-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="b3177-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b3177-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3177-129">-ResourceGroupName</span></span>
<span data-ttu-id="b3177-130">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b3177-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="b3177-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3177-131">-ResourceId</span></span>
<span data-ttu-id="b3177-132">Programmets ResourceId.</span><span class="sxs-lookup"><span data-stu-id="b3177-132">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="b3177-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b3177-133">-Confirm</span></span>
<span data-ttu-id="b3177-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b3177-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3177-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3177-135">-WhatIf</span></span>
<span data-ttu-id="b3177-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b3177-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3177-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b3177-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3177-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3177-138">CommonParameters</span></span>
<span data-ttu-id="b3177-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3177-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3177-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3177-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3177-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b3177-141">INPUTS</span></span>

### <span data-ttu-id="b3177-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b3177-142">System.String</span></span>

### <span data-ttu-id="b3177-143">Microsoft. Azure. commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="b3177-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="b3177-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b3177-144">OUTPUTS</span></span>

### <span data-ttu-id="b3177-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b3177-145">System.Boolean</span></span>

## <span data-ttu-id="b3177-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b3177-146">NOTES</span></span>

## <span data-ttu-id="b3177-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b3177-147">RELATED LINKS</span></span>
