---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4695AFEA-D244-4FCB-AF36-D8CDEBFB392C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 02a6090a98a80300f886e8bbbd8e2622aa7981d4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259065"
---
# <span data-ttu-id="0c2d0-101">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="0c2d0-101">Remove-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="0c2d0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0c2d0-102">SYNOPSIS</span></span>
<span data-ttu-id="0c2d0-103">Tar bort en regel för data mask från en databas.</span><span class="sxs-lookup"><span data-stu-id="0c2d0-103">Removes a data masking rule from a database.</span></span>

## <span data-ttu-id="0c2d0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0c2d0-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseDataMaskingRule [-PassThru] [-Force] -SchemaName <String> -TableName <String>
 -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c2d0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0c2d0-105">DESCRIPTION</span></span>
<span data-ttu-id="0c2d0-106">Cmdleten **Remove-AzSqlDatabaseDataMaskingRule** tar bort en specifik data masknings regel från en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="0c2d0-106">The **Remove-AzSqlDatabaseDataMaskingRule** cmdlet removes a specific data masking rule from an Azure SQL database.</span></span>
<span data-ttu-id="0c2d0-107">Du kan ta bort en regel för data maskering genom att använda parametrarna *ResourceGroupName* , *servername* , *databasename* och *RuleID* för att identifiera regeln som tas bort av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0c2d0-107">You can remove a data masking rule by using the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule that this cmdlet removes.</span></span>
<span data-ttu-id="0c2d0-108">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="0c2d0-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="0c2d0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0c2d0-109">EXAMPLES</span></span>

### <span data-ttu-id="0c2d0-110">Exempel 1: ta bort en regel för data maskning för databas</span><span class="sxs-lookup"><span data-stu-id="0c2d0-110">Example 1: Remove a database data masking rule</span></span>
```
PS C:\>Remove-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
```

<span data-ttu-id="0c2d0-111">Det här kommandot tar bort regel namnet Rule01 som definierats för databasen Database01.</span><span class="sxs-lookup"><span data-stu-id="0c2d0-111">This command removes rule name Rule01 defined for the database Database01.</span></span>
<span data-ttu-id="0c2d0-112">Databasen finns på Server01 och tilldelas resurs grupp ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="0c2d0-112">The database is located on Server01 and assigned to resource group ResourceGroup01.</span></span>

## <span data-ttu-id="0c2d0-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0c2d0-113">PARAMETERS</span></span>

### <span data-ttu-id="0c2d0-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="0c2d0-114">-ColumnName</span></span>
<span data-ttu-id="0c2d0-115">Anger namnet på den kolumn som är avsedd för Maskerings regeln.</span><span class="sxs-lookup"><span data-stu-id="0c2d0-115">Specifies the name of the column targeted by the masking rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c2d0-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0c2d0-116">-DatabaseName</span></span>
<span data-ttu-id="0c2d0-117">Anger namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="0c2d0-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="0c2d0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c2d0-118">-DefaultProfile</span></span>
<span data-ttu-id="0c2d0-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0c2d0-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c2d0-120">-Force</span><span class="sxs-lookup"><span data-stu-id="0c2d0-120">-Force</span></span>
<span data-ttu-id="0c2d0-121">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="0c2d0-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0c2d0-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c2d0-122">-PassThru</span></span>
<span data-ttu-id="0c2d0-123">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="0c2d0-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0c2d0-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="0c2d0-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0c2d0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c2d0-125">-ResourceGroupName</span></span>
<span data-ttu-id="0c2d0-126">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="0c2d0-126">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="0c2d0-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="0c2d0-127">-SchemaName</span></span>
<span data-ttu-id="0c2d0-128">Anger namnet på ett schema.</span><span class="sxs-lookup"><span data-stu-id="0c2d0-128">Specifies the name of a schema.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c2d0-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0c2d0-129">-ServerName</span></span>
<span data-ttu-id="0c2d0-130">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="0c2d0-130">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="0c2d0-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="0c2d0-131">-TableName</span></span>
<span data-ttu-id="0c2d0-132">Anger namnet på en Azure SQL-tabell.</span><span class="sxs-lookup"><span data-stu-id="0c2d0-132">Specifies the name of an Azure SQL table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c2d0-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0c2d0-133">-Confirm</span></span>
<span data-ttu-id="0c2d0-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0c2d0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c2d0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c2d0-135">-WhatIf</span></span>
<span data-ttu-id="0c2d0-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0c2d0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c2d0-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0c2d0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c2d0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c2d0-138">CommonParameters</span></span>
<span data-ttu-id="0c2d0-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c2d0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c2d0-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c2d0-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c2d0-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0c2d0-141">INPUTS</span></span>

### <span data-ttu-id="0c2d0-142">System. String</span><span class="sxs-lookup"><span data-stu-id="0c2d0-142">System.String</span></span>

## <span data-ttu-id="0c2d0-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0c2d0-143">OUTPUTS</span></span>

### <span data-ttu-id="0c2d0-144">Microsoft. Azure. commands. SQL. DataMasking. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="0c2d0-144">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="0c2d0-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0c2d0-145">NOTES</span></span>

## <span data-ttu-id="0c2d0-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0c2d0-146">RELATED LINKS</span></span>

[<span data-ttu-id="0c2d0-147">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="0c2d0-147">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="0c2d0-148">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="0c2d0-148">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="0c2d0-149">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="0c2d0-149">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="0c2d0-150">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="0c2d0-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


