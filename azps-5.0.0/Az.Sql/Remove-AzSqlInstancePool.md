---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
ms.openlocfilehash: b10187938613f9ab6e0c12cb0d83162450be8445
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272820"
---
# <span data-ttu-id="b615d-101">Remove-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="b615d-101">Remove-AzSqlInstancePool</span></span>

## <span data-ttu-id="b615d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b615d-102">SYNOPSIS</span></span>
<span data-ttu-id="b615d-103">Tar bort en Azure SQL-instans.</span><span class="sxs-lookup"><span data-stu-id="b615d-103">Removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="b615d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b615d-104">SYNTAX</span></span>

### <span data-ttu-id="b615d-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b615d-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b615d-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b615d-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b615d-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b615d-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b615d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b615d-108">DESCRIPTION</span></span>
<span data-ttu-id="b615d-109">Cmdleten **Remove-AzSqlInstancePool** tar bort en Azure SQL instance-pool.</span><span class="sxs-lookup"><span data-stu-id="b615d-109">The **Remove-AzSqlInstancePool** cmdlet removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="b615d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b615d-110">EXAMPLES</span></span>

### <span data-ttu-id="b615d-111">Exempel 1: ta bort en instans</span><span class="sxs-lookup"><span data-stu-id="b615d-111">Example 1: Remove an instance pool</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
```

### <span data-ttu-id="b615d-112">Exempel 2: ta bort en instans med dess resurs identifierare</span><span class="sxs-lookup"><span data-stu-id="b615d-112">Example 2: Remove an instance pool by its resource identifier</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
```

### <span data-ttu-id="b615d-113">Exempel 3: ta bort en instans med ett instans objekt</span><span class="sxs-lookup"><span data-stu-id="b615d-113">Example 3: Remove an instance pool by an instance pool object</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
PS C:\> Remove-AzSqlInstancePool -InputObject $instancePool
```

<span data-ttu-id="b615d-114">Det här kommandot tar bort en instans med namnet instancePool0.</span><span class="sxs-lookup"><span data-stu-id="b615d-114">This command removes an instance pool named instancePool0.</span></span>

## <span data-ttu-id="b615d-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b615d-115">PARAMETERS</span></span>

### <span data-ttu-id="b615d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b615d-116">-DefaultProfile</span></span>
<span data-ttu-id="b615d-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b615d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b615d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b615d-118">-InputObject</span></span>
<span data-ttu-id="b615d-119">Den instans av entitetsinstansen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="b615d-119">The instance pool object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b615d-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="b615d-120">-Name</span></span>
<span data-ttu-id="b615d-121">Namnet på instansen.</span><span class="sxs-lookup"><span data-stu-id="b615d-121">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b615d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b615d-122">-ResourceGroupName</span></span>
<span data-ttu-id="b615d-123">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b615d-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b615d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b615d-124">-ResourceId</span></span>
<span data-ttu-id="b615d-125">Resurs-ID för entitetsinstansen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="b615d-125">The instance pool resource id to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b615d-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b615d-126">-Confirm</span></span>
<span data-ttu-id="b615d-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b615d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b615d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b615d-128">-WhatIf</span></span>
<span data-ttu-id="b615d-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b615d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b615d-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b615d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b615d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b615d-131">CommonParameters</span></span>
<span data-ttu-id="b615d-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b615d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b615d-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b615d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b615d-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b615d-134">INPUTS</span></span>

### <span data-ttu-id="b615d-135">Microsoft.Azure.Commands.Sql.Instance_Pools. Model. AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="b615d-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="b615d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b615d-136">System.String</span></span>

## <span data-ttu-id="b615d-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b615d-137">OUTPUTS</span></span>

### <span data-ttu-id="b615d-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="b615d-138">System.Object</span></span>
## <span data-ttu-id="b615d-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b615d-139">NOTES</span></span>

## <span data-ttu-id="b615d-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b615d-140">RELATED LINKS</span></span>