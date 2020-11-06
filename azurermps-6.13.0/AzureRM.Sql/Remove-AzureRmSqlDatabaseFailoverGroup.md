---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 426b44b6c01e40a616d834d2768e5d050a2bc1db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579923"
---
# <span data-ttu-id="ca732-101">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ca732-101">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="ca732-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ca732-102">SYNOPSIS</span></span>
<span data-ttu-id="ca732-103">Tar bort en failover-grupp för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="ca732-103">Removes an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca732-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ca732-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca732-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ca732-105">DESCRIPTION</span></span>
<span data-ttu-id="ca732-106">Med det här kommandot tas failover-gruppen bort med det angivna namnet och alla databaser och replik relationer blir intakta.</span><span class="sxs-lookup"><span data-stu-id="ca732-106">This command removes the Failover Group with the specified name, leaving all databases and replication relationships intact.</span></span> <span data-ttu-id="ca732-107">Lyssnar slut punkten kommer att avregistreras från DNS.</span><span class="sxs-lookup"><span data-stu-id="ca732-107">The listener endpoint will be unregistered from DNS.</span></span>
<span data-ttu-id="ca732-108">Gruppens primära server bör användas för att köra kommandot.</span><span class="sxs-lookup"><span data-stu-id="ca732-108">The Failover Group's primary server should be used to execute the command.</span></span>

## <span data-ttu-id="ca732-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ca732-109">EXAMPLES</span></span>

### <span data-ttu-id="ca732-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ca732-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="ca732-111">Ta bort en failover-grupp.</span><span class="sxs-lookup"><span data-stu-id="ca732-111">Remove a Failover Group.</span></span>

## <span data-ttu-id="ca732-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ca732-112">PARAMETERS</span></span>

### <span data-ttu-id="ca732-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca732-113">-DefaultProfile</span></span>
<span data-ttu-id="ca732-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ca732-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca732-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="ca732-115">-FailoverGroupName</span></span>
<span data-ttu-id="ca732-116">Namnet på den failover-grupp i Azure SQL-databasen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="ca732-116">The name of the Azure SQL Database Failover Group to remove.</span></span>

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

### <span data-ttu-id="ca732-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ca732-117">-Force</span></span>
<span data-ttu-id="ca732-118">Hoppa över bekräftelse meddelande för att utföra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="ca732-118">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="ca732-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca732-119">-ResourceGroupName</span></span>
<span data-ttu-id="ca732-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ca732-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="ca732-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ca732-121">-ServerName</span></span>
<span data-ttu-id="ca732-122">Namnet på den primära Azure SQL-databasfilen i gruppen failover.</span><span class="sxs-lookup"><span data-stu-id="ca732-122">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="ca732-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ca732-123">-Confirm</span></span>
<span data-ttu-id="ca732-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ca732-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca732-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca732-125">-WhatIf</span></span>
<span data-ttu-id="ca732-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ca732-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca732-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ca732-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca732-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca732-128">CommonParameters</span></span>
<span data-ttu-id="ca732-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca732-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca732-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca732-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca732-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ca732-131">INPUTS</span></span>

### <span data-ttu-id="ca732-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ca732-132">System.String</span></span>

## <span data-ttu-id="ca732-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ca732-133">OUTPUTS</span></span>

### <span data-ttu-id="ca732-134">Microsoft. Azure. commands. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="ca732-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="ca732-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ca732-135">NOTES</span></span>

## <span data-ttu-id="ca732-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ca732-136">RELATED LINKS</span></span>

[<span data-ttu-id="ca732-137">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ca732-137">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ca732-138">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ca732-138">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ca732-139">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ca732-139">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ca732-140">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ca732-140">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="ca732-141">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ca732-141">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="ca732-142">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ca732-142">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ca732-143">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="ca732-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
