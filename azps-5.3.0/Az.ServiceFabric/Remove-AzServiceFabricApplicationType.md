---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
ms.openlocfilehash: 8ba56568a10ee8223a53bc1530602f3ae930e14c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525404"
---
# <span data-ttu-id="b6552-101">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="b6552-101">Remove-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="b6552-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b6552-102">SYNOPSIS</span></span>
<span data-ttu-id="b6552-103">Ta bort tjänstens infrastruktur program typ från klustret.</span><span class="sxs-lookup"><span data-stu-id="b6552-103">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="b6552-104">Detta tar bort alla typ versioner under den här resursen.</span><span class="sxs-lookup"><span data-stu-id="b6552-104">This will remove all type versions under this resource.</span></span> <span data-ttu-id="b6552-105">Stöder bara program typer som distribueras av ARM.</span><span class="sxs-lookup"><span data-stu-id="b6552-105">Only supports ARM deployed application types.</span></span>

## <span data-ttu-id="b6552-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b6552-106">SYNTAX</span></span>

### <span data-ttu-id="b6552-107">ByResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="b6552-107">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String>]
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6552-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b6552-108">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationType -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6552-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b6552-109">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationType -InputObject <PSApplicationType> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6552-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b6552-110">DESCRIPTION</span></span>
<span data-ttu-id="b6552-111">Denna cmdlet tar bort en program typ från klustret och tar bort alla typ versioner under den här resursen, men alla program under den bör tas bort innan det här kommandot körs.</span><span class="sxs-lookup"><span data-stu-id="b6552-111">This cmdlet removes an application type form the cluster and will remove all type version under this resource, but all applications under it should be removed before running this command.</span></span>

## <span data-ttu-id="b6552-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b6552-112">EXAMPLES</span></span>

### <span data-ttu-id="b6552-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b6552-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Remove-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="b6552-114">I det här exemplet tas program typen "testAppType" och all version under den bort.</span><span class="sxs-lookup"><span data-stu-id="b6552-114">This example will remove the application type "testAppType" and all the version under it.</span></span> <span data-ttu-id="b6552-115">Om det finns program som skapats med den här typen utlöses ett undantag.</span><span class="sxs-lookup"><span data-stu-id="b6552-115">If there are any applications created with this type, the command will throw an exception.</span></span>

## <span data-ttu-id="b6552-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b6552-116">PARAMETERS</span></span>

### <span data-ttu-id="b6552-117">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="b6552-117">-ClusterName</span></span>
<span data-ttu-id="b6552-118">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="b6552-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="b6552-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6552-119">-DefaultProfile</span></span>
<span data-ttu-id="b6552-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b6552-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6552-121">-Force</span><span class="sxs-lookup"><span data-stu-id="b6552-121">-Force</span></span>
<span data-ttu-id="b6552-122">Ta bort utan att fråga.</span><span class="sxs-lookup"><span data-stu-id="b6552-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="b6552-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6552-123">-InputObject</span></span>
<span data-ttu-id="b6552-124">Program typ resursen.</span><span class="sxs-lookup"><span data-stu-id="b6552-124">The application type resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6552-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="b6552-125">-Name</span></span>
<span data-ttu-id="b6552-126">Ange namnet på program typen.</span><span class="sxs-lookup"><span data-stu-id="b6552-126">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6552-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6552-127">-PassThru</span></span>
<span data-ttu-id="b6552-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="b6552-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b6552-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6552-129">-ResourceGroupName</span></span>
<span data-ttu-id="b6552-130">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b6552-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="b6552-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6552-131">-ResourceId</span></span>
<span data-ttu-id="b6552-132">Program typens arm ResourceId.</span><span class="sxs-lookup"><span data-stu-id="b6552-132">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="b6552-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b6552-133">-Confirm</span></span>
<span data-ttu-id="b6552-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b6552-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6552-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6552-135">-WhatIf</span></span>
<span data-ttu-id="b6552-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b6552-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6552-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b6552-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6552-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6552-138">CommonParameters</span></span>
<span data-ttu-id="b6552-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6552-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6552-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6552-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6552-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b6552-141">INPUTS</span></span>

### <span data-ttu-id="b6552-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b6552-142">System.String</span></span>

### <span data-ttu-id="b6552-143">Microsoft. Azure. commands. ServiceFabric. Models. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="b6552-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="b6552-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b6552-144">OUTPUTS</span></span>

### <span data-ttu-id="b6552-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b6552-145">System.Boolean</span></span>

## <span data-ttu-id="b6552-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b6552-146">NOTES</span></span>

## <span data-ttu-id="b6552-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b6552-147">RELATED LINKS</span></span>
