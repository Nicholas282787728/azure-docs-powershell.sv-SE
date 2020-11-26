---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 12bc26177a249995f748a879a9ae8d2f73900c99
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269864"
---
# <span data-ttu-id="420ac-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="420ac-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="420ac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="420ac-102">SYNOPSIS</span></span>
<span data-ttu-id="420ac-103">Tar bort en failover-grupp för en instans.</span><span class="sxs-lookup"><span data-stu-id="420ac-103">Removes an Instance Failover Group.</span></span>

## <span data-ttu-id="420ac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="420ac-104">SYNTAX</span></span>

### <span data-ttu-id="420ac-105">RemoveIFGDefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="420ac-105">RemoveIFGDefaultSet (Default)</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="420ac-106">RemoveInstanceFailoverGroupByResourceId</span><span class="sxs-lookup"><span data-stu-id="420ac-106">RemoveInstanceFailoverGroupByResourceId</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="420ac-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="420ac-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="420ac-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="420ac-108">DESCRIPTION</span></span>
<span data-ttu-id="420ac-109">Med det här kommandot tas den instansen av redundans bort med det angivna namnet och alla databaser blir oförändrade.</span><span class="sxs-lookup"><span data-stu-id="420ac-109">This command removes the Instance Failover Group with the specified name, leaving all databases intact.</span></span> <span data-ttu-id="420ac-110">Lyssnar slut punkten kommer att avregistreras från DNS.</span><span class="sxs-lookup"><span data-stu-id="420ac-110">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="420ac-111">Det primära området för instansens failover-grupp ska användas för att köra kommandot.</span><span class="sxs-lookup"><span data-stu-id="420ac-111">The Instance Failover Group's primary region should be used to execute the command.</span></span>

## <span data-ttu-id="420ac-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="420ac-112">EXAMPLES</span></span>

### <span data-ttu-id="420ac-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="420ac-113">Example 1</span></span>
```
PS C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Remove-AzSqlDatabaseInstanceFailoverGroup
```

<span data-ttu-id="420ac-114">Ta bort en failover-grupp för en instans.</span><span class="sxs-lookup"><span data-stu-id="420ac-114">Remove a Instance Failover Group.</span></span>

## <span data-ttu-id="420ac-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="420ac-115">PARAMETERS</span></span>

### <span data-ttu-id="420ac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="420ac-116">-DefaultProfile</span></span>
<span data-ttu-id="420ac-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="420ac-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="420ac-118">-Force</span><span class="sxs-lookup"><span data-stu-id="420ac-118">-Force</span></span>
<span data-ttu-id="420ac-119">Hoppa över bekräftelse meddelande för att utföra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="420ac-119">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="420ac-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="420ac-120">-InputObject</span></span>
<span data-ttu-id="420ac-121">Den instans av grupp objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="420ac-121">The Instance Failover Group object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel
Parameter Sets: RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="420ac-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="420ac-122">-Location</span></span>
<span data-ttu-id="420ac-123">Namnet på det lokala området som du vill hämta instans failover-gruppen från.</span><span class="sxs-lookup"><span data-stu-id="420ac-123">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveIFGDefaultSet, RemoveInstanceFailoverGroupByResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="420ac-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="420ac-124">-Name</span></span>
<span data-ttu-id="420ac-125">Namnet på den instans av instansen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="420ac-125">The name of the Instance Failover Group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveIFGDefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="420ac-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="420ac-126">-PassThru</span></span>
<span data-ttu-id="420ac-127">Anger om du vill överföra utdata från en cmdlet.</span><span class="sxs-lookup"><span data-stu-id="420ac-127">Specifies whether to pass through cmdlet execution output.</span></span>

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

### <span data-ttu-id="420ac-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="420ac-128">-ResourceGroupName</span></span>
<span data-ttu-id="420ac-129">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="420ac-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveIFGDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="420ac-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="420ac-130">-ResourceId</span></span>
<span data-ttu-id="420ac-131">Resurs-ID för den instans som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="420ac-131">The Resource ID of the Instance Failover Group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFailoverGroupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="420ac-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="420ac-132">-Confirm</span></span>
<span data-ttu-id="420ac-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="420ac-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="420ac-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="420ac-134">-WhatIf</span></span>
<span data-ttu-id="420ac-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="420ac-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="420ac-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="420ac-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="420ac-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="420ac-137">CommonParameters</span></span>
<span data-ttu-id="420ac-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="420ac-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="420ac-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="420ac-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="420ac-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="420ac-140">INPUTS</span></span>

### <span data-ttu-id="420ac-141">Microsoft. Azure. commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="420ac-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="420ac-142">System. String</span><span class="sxs-lookup"><span data-stu-id="420ac-142">System.String</span></span>

## <span data-ttu-id="420ac-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="420ac-143">OUTPUTS</span></span>

### <span data-ttu-id="420ac-144">Microsoft. Azure. commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="420ac-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="420ac-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="420ac-145">NOTES</span></span>

## <span data-ttu-id="420ac-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="420ac-146">RELATED LINKS</span></span>