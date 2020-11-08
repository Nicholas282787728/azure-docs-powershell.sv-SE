---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 283a7963d7dcf278f203385bd790bd19cadc9d7c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090934"
---
# <span data-ttu-id="9e8e6-101">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e8e6-101">Remove-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="9e8e6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9e8e6-102">SYNOPSIS</span></span>
<span data-ttu-id="9e8e6-103">Tar bort en failover-grupp för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="9e8e6-103">Removes an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="9e8e6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9e8e6-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e8e6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9e8e6-105">DESCRIPTION</span></span>
<span data-ttu-id="9e8e6-106">Med det här kommandot tas failover-gruppen bort med det angivna namnet och alla databaser och replik relationer blir intakta.</span><span class="sxs-lookup"><span data-stu-id="9e8e6-106">This command removes the Failover Group with the specified name, leaving all databases and replication relationships intact.</span></span> <span data-ttu-id="9e8e6-107">Lyssnar slut punkten kommer att avregistreras från DNS.</span><span class="sxs-lookup"><span data-stu-id="9e8e6-107">The listener endpoint will be unregistered from DNS.</span></span>
<span data-ttu-id="9e8e6-108">Gruppens primära server bör användas för att köra kommandot.</span><span class="sxs-lookup"><span data-stu-id="9e8e6-108">The Failover Group's primary server should be used to execute the command.</span></span>

## <span data-ttu-id="9e8e6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9e8e6-109">EXAMPLES</span></span>

### <span data-ttu-id="9e8e6-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9e8e6-110">Example 1</span></span>
```
PS C:\> Remove-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="9e8e6-111">Ta bort en failover-grupp.</span><span class="sxs-lookup"><span data-stu-id="9e8e6-111">Remove a Failover Group.</span></span>

## <span data-ttu-id="9e8e6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9e8e6-112">PARAMETERS</span></span>

### <span data-ttu-id="9e8e6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e8e6-113">-DefaultProfile</span></span>
<span data-ttu-id="9e8e6-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9e8e6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e8e6-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="9e8e6-115">-FailoverGroupName</span></span>
<span data-ttu-id="9e8e6-116">Namnet på den failover-grupp i Azure SQL-databasen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="9e8e6-116">The name of the Azure SQL Database Failover Group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e8e6-117">-Force</span><span class="sxs-lookup"><span data-stu-id="9e8e6-117">-Force</span></span>
<span data-ttu-id="9e8e6-118">Hoppa över bekräftelse meddelande för att utföra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="9e8e6-118">Skip confirmation message for performing the action.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e8e6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e8e6-119">-ResourceGroupName</span></span>
<span data-ttu-id="9e8e6-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9e8e6-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e8e6-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9e8e6-121">-ServerName</span></span>
<span data-ttu-id="9e8e6-122">Namnet på den primära Azure SQL-databasfilen i gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="9e8e6-122">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e8e6-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9e8e6-123">-Confirm</span></span>
<span data-ttu-id="9e8e6-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9e8e6-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e8e6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e8e6-125">-WhatIf</span></span>
<span data-ttu-id="9e8e6-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9e8e6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e8e6-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9e8e6-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e8e6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e8e6-128">CommonParameters</span></span>
<span data-ttu-id="9e8e6-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e8e6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e8e6-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e8e6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e8e6-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9e8e6-131">INPUTS</span></span>

### <span data-ttu-id="9e8e6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9e8e6-132">System.String</span></span>

## <span data-ttu-id="9e8e6-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9e8e6-133">OUTPUTS</span></span>

### <span data-ttu-id="9e8e6-134">Microsoft. Azure. commands. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="9e8e6-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="9e8e6-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9e8e6-135">NOTES</span></span>

## <span data-ttu-id="9e8e6-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9e8e6-136">RELATED LINKS</span></span>

[<span data-ttu-id="9e8e6-137">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e8e6-137">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9e8e6-138">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e8e6-138">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9e8e6-139">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e8e6-139">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9e8e6-140">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e8e6-140">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="9e8e6-141">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e8e6-141">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="9e8e6-142">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e8e6-142">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9e8e6-143">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="9e8e6-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)