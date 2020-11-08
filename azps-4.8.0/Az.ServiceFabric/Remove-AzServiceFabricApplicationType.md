---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
ms.openlocfilehash: 87557a67c8cb087b8a22ecc9cdfa59a3690057dc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101952"
---
# <span data-ttu-id="ec0cf-101">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ec0cf-101">Remove-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="ec0cf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ec0cf-102">SYNOPSIS</span></span>
<span data-ttu-id="ec0cf-103">Ta bort tjänstens infrastruktur program typ från klustret.</span><span class="sxs-lookup"><span data-stu-id="ec0cf-103">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="ec0cf-104">Detta tar bort alla typ versioner under den här resursen.</span><span class="sxs-lookup"><span data-stu-id="ec0cf-104">This will remove all type versions under this resource.</span></span>

## <span data-ttu-id="ec0cf-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ec0cf-105">SYNTAX</span></span>

### <span data-ttu-id="ec0cf-106">ByResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="ec0cf-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String>]
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec0cf-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ec0cf-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationType -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec0cf-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ec0cf-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationType -InputObject <PSApplicationType> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec0cf-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ec0cf-109">DESCRIPTION</span></span>
<span data-ttu-id="ec0cf-110">Denna cmdlet tar bort en program typ från klustret och tar bort alla typ versioner under den här resursen, men alla program under den bör tas bort innan det här kommandot körs.</span><span class="sxs-lookup"><span data-stu-id="ec0cf-110">This cmdlet removes an application type form the cluster and will remove all type version under this resource, but all applications under it should be removed before running this command.</span></span>

## <span data-ttu-id="ec0cf-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ec0cf-111">EXAMPLES</span></span>

### <span data-ttu-id="ec0cf-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ec0cf-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Remove-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="ec0cf-113">I det här exemplet tas program typen "testAppType" och all version under den bort.</span><span class="sxs-lookup"><span data-stu-id="ec0cf-113">This example will remove the application type "testAppType" and all the version under it.</span></span> <span data-ttu-id="ec0cf-114">Om det finns program som skapats med den här typen utlöses ett undantag.</span><span class="sxs-lookup"><span data-stu-id="ec0cf-114">If there are any applications created with this type, the command will throw an exception.</span></span>

## <span data-ttu-id="ec0cf-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ec0cf-115">PARAMETERS</span></span>

### <span data-ttu-id="ec0cf-116">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="ec0cf-116">-ClusterName</span></span>
<span data-ttu-id="ec0cf-117">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="ec0cf-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ec0cf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec0cf-118">-DefaultProfile</span></span>
<span data-ttu-id="ec0cf-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ec0cf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec0cf-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ec0cf-120">-Force</span></span>
<span data-ttu-id="ec0cf-121">Ta bort utan att fråga.</span><span class="sxs-lookup"><span data-stu-id="ec0cf-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="ec0cf-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec0cf-122">-InputObject</span></span>
<span data-ttu-id="ec0cf-123">Program typ resursen.</span><span class="sxs-lookup"><span data-stu-id="ec0cf-123">The application type resource.</span></span>

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

### <span data-ttu-id="ec0cf-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="ec0cf-124">-Name</span></span>
<span data-ttu-id="ec0cf-125">Ange namnet på program typen.</span><span class="sxs-lookup"><span data-stu-id="ec0cf-125">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="ec0cf-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec0cf-126">-PassThru</span></span>
<span data-ttu-id="ec0cf-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ec0cf-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ec0cf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec0cf-128">-ResourceGroupName</span></span>
<span data-ttu-id="ec0cf-129">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ec0cf-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ec0cf-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec0cf-130">-ResourceId</span></span>
<span data-ttu-id="ec0cf-131">Program typens arm ResourceId.</span><span class="sxs-lookup"><span data-stu-id="ec0cf-131">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="ec0cf-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ec0cf-132">-Confirm</span></span>
<span data-ttu-id="ec0cf-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ec0cf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec0cf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec0cf-134">-WhatIf</span></span>
<span data-ttu-id="ec0cf-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ec0cf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec0cf-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ec0cf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec0cf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec0cf-137">CommonParameters</span></span>
<span data-ttu-id="ec0cf-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec0cf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec0cf-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec0cf-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec0cf-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ec0cf-140">INPUTS</span></span>

### <span data-ttu-id="ec0cf-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ec0cf-141">System.String</span></span>

### <span data-ttu-id="ec0cf-142">Microsoft. Azure. commands. ServiceFabric. Models. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="ec0cf-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="ec0cf-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ec0cf-143">OUTPUTS</span></span>

### <span data-ttu-id="ec0cf-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ec0cf-144">System.Boolean</span></span>

## <span data-ttu-id="ec0cf-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ec0cf-145">NOTES</span></span>

## <span data-ttu-id="ec0cf-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ec0cf-146">RELATED LINKS</span></span>
