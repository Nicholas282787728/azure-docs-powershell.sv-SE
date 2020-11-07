---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 8027af33b9ea4f4184c10963da69e8be3b4e3961
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920555"
---
# <span data-ttu-id="c3cc2-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c3cc2-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="c3cc2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c3cc2-102">SYNOPSIS</span></span>
<span data-ttu-id="c3cc2-103">Tar bort en failover-grupp för en instans.</span><span class="sxs-lookup"><span data-stu-id="c3cc2-103">Removes an Instance Failover Group.</span></span>

## <span data-ttu-id="c3cc2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c3cc2-104">SYNTAX</span></span>

### <span data-ttu-id="c3cc2-105">RemoveIFGDefault (standard)</span><span class="sxs-lookup"><span data-stu-id="c3cc2-105">RemoveIFGDefault (Default)</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3cc2-106">Ta bort en failover-gruppgrupp från resurs-ID</span><span class="sxs-lookup"><span data-stu-id="c3cc2-106">Remove a Instance Failover Group from Resource Id</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3cc2-107">Ta bort en failover-gruppgrupp från AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="c3cc2-107">Remove a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup -InputObject <AzureSqlInstanceFailoverGroupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3cc2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c3cc2-108">DESCRIPTION</span></span>
<span data-ttu-id="c3cc2-109">Med det här kommandot tas den instansen av redundans bort med det angivna namnet och alla databaser blir oförändrade.</span><span class="sxs-lookup"><span data-stu-id="c3cc2-109">This command removes the Instance Failover Group with the specified name, leaving all databases intact.</span></span> <span data-ttu-id="c3cc2-110">Lyssnar slut punkten kommer att avregistreras från DNS.</span><span class="sxs-lookup"><span data-stu-id="c3cc2-110">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="c3cc2-111">Det primära området för instansens failover-grupp ska användas för att köra kommandot.</span><span class="sxs-lookup"><span data-stu-id="c3cc2-111">The Instance Failover Group's primary region should be used to execute the command.</span></span>

## <span data-ttu-id="c3cc2-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c3cc2-112">EXAMPLES</span></span>

### <span data-ttu-id="c3cc2-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c3cc2-113">Example 1</span></span>
```
PS C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Remove-AzSqlDatabaseInstanceFailoverGroup
```

<span data-ttu-id="c3cc2-114">Ta bort en failover-grupp för en instans.</span><span class="sxs-lookup"><span data-stu-id="c3cc2-114">Remove a Instance Failover Group.</span></span>

## <span data-ttu-id="c3cc2-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c3cc2-115">PARAMETERS</span></span>

### <span data-ttu-id="c3cc2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3cc2-116">-DefaultProfile</span></span>
<span data-ttu-id="c3cc2-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c3cc2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3cc2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c3cc2-118">-Force</span></span>
<span data-ttu-id="c3cc2-119">Hoppa över bekräftelse meddelande för att utföra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="c3cc2-119">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="c3cc2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3cc2-120">-InputObject</span></span>
<span data-ttu-id="c3cc2-121">Den instans av grupp objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="c3cc2-121">The Instance Failover Group object to remove</span></span>

```yaml
Type: AzureSqlInstanceFailoverGroupModel
Parameter Sets: Remove a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3cc2-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="c3cc2-122">-Location</span></span>
<span data-ttu-id="c3cc2-123">Namnet på det lokala området som du vill hämta instans failover-gruppen från.</span><span class="sxs-lookup"><span data-stu-id="c3cc2-123">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveIFGDefault, Remove a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3cc2-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="c3cc2-124">-Name</span></span>
<span data-ttu-id="c3cc2-125">Namnet på den instans av instansen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="c3cc2-125">The name of the Instance Failover Group to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveIFGDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3cc2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3cc2-126">-ResourceGroupName</span></span>
<span data-ttu-id="c3cc2-127">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c3cc2-127">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveIFGDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3cc2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3cc2-128">-ResourceId</span></span>
<span data-ttu-id="c3cc2-129">Resurs-ID för den instans som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="c3cc2-129">The Resource ID of the Instance Failover Group to remove.</span></span>

```yaml
Type: String
Parameter Sets: Remove a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3cc2-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c3cc2-130">-Confirm</span></span>
<span data-ttu-id="c3cc2-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c3cc2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3cc2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3cc2-132">-WhatIf</span></span>
<span data-ttu-id="c3cc2-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c3cc2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3cc2-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c3cc2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3cc2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3cc2-135">CommonParameters</span></span>
<span data-ttu-id="c3cc2-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3cc2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3cc2-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3cc2-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3cc2-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c3cc2-138">INPUTS</span></span>

### <span data-ttu-id="c3cc2-139">Microsoft. Azure. commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="c3cc2-139">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="c3cc2-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c3cc2-140">System.String</span></span>

## <span data-ttu-id="c3cc2-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c3cc2-141">OUTPUTS</span></span>

### <span data-ttu-id="c3cc2-142">Microsoft. Azure. commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="c3cc2-142">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="c3cc2-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c3cc2-143">NOTES</span></span>

## <span data-ttu-id="c3cc2-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c3cc2-144">RELATED LINKS</span></span>
