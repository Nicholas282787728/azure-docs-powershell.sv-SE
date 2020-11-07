---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4695AFEA-D244-4FCB-AF36-D8CDEBFB392C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 7f5f72652a0b3c8e1944b6091b43f1458fd17839
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758281"
---
# <span data-ttu-id="ed89a-101">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ed89a-101">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="ed89a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ed89a-102">SYNOPSIS</span></span>
<span data-ttu-id="ed89a-103">Tar bort en regel för data mask från en databas.</span><span class="sxs-lookup"><span data-stu-id="ed89a-103">Removes a data masking rule from a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed89a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ed89a-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseDataMaskingRule [-PassThru] [-Force] -SchemaName <String> -TableName <String>
 -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed89a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ed89a-105">DESCRIPTION</span></span>
<span data-ttu-id="ed89a-106">Cmdleten **Remove-AzureRmSqlDatabaseDataMaskingRule** tar bort en specifik data masknings regel från en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="ed89a-106">The **Remove-AzureRmSqlDatabaseDataMaskingRule** cmdlet removes a specific data masking rule from an Azure SQL database.</span></span>
<span data-ttu-id="ed89a-107">Du kan ta bort en regel för data maskering genom att använda parametrarna *ResourceGroupName* , *servername* , *databasename* och *RuleID* för att identifiera regeln som tas bort av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ed89a-107">You can remove a data masking rule by using the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule that this cmdlet removes.</span></span>

<span data-ttu-id="ed89a-108">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="ed89a-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ed89a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ed89a-109">EXAMPLES</span></span>

### <span data-ttu-id="ed89a-110">Exempel 1: ta bort en regel för data maskning för databas</span><span class="sxs-lookup"><span data-stu-id="ed89a-110">Example 1: Remove a database data masking rule</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
```

<span data-ttu-id="ed89a-111">Det här kommandot tar bort regel namnet Rule01 som definierats för databasen Database01.</span><span class="sxs-lookup"><span data-stu-id="ed89a-111">This command removes rule name Rule01 defined for the database Database01.</span></span>
<span data-ttu-id="ed89a-112">Databasen finns på Server01 och tilldelas resurs grupp ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="ed89a-112">The database is located on Server01 and assigned to resource group ResourceGroup01.</span></span>

## <span data-ttu-id="ed89a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ed89a-113">PARAMETERS</span></span>

### <span data-ttu-id="ed89a-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="ed89a-114">-ColumnName</span></span>
<span data-ttu-id="ed89a-115">Anger namnet på den kolumn som är avsedd för Maskerings regeln.</span><span class="sxs-lookup"><span data-stu-id="ed89a-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="ed89a-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ed89a-116">-DatabaseName</span></span>
<span data-ttu-id="ed89a-117">Anger namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="ed89a-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="ed89a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ed89a-118">-Force</span></span>
<span data-ttu-id="ed89a-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ed89a-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ed89a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed89a-120">-PassThru</span></span>
<span data-ttu-id="ed89a-121">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="ed89a-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ed89a-122">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="ed89a-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ed89a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed89a-123">-ResourceGroupName</span></span>
<span data-ttu-id="ed89a-124">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="ed89a-124">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="ed89a-125">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="ed89a-125">-SchemaName</span></span>
<span data-ttu-id="ed89a-126">Anger namnet på ett schema.</span><span class="sxs-lookup"><span data-stu-id="ed89a-126">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="ed89a-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ed89a-127">-ServerName</span></span>
<span data-ttu-id="ed89a-128">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="ed89a-128">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="ed89a-129">-TableName</span><span class="sxs-lookup"><span data-stu-id="ed89a-129">-TableName</span></span>
<span data-ttu-id="ed89a-130">Anger namnet på en Azure SQL-tabell.</span><span class="sxs-lookup"><span data-stu-id="ed89a-130">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="ed89a-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ed89a-131">-Confirm</span></span>
<span data-ttu-id="ed89a-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ed89a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed89a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed89a-133">-WhatIf</span></span>
<span data-ttu-id="ed89a-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ed89a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed89a-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ed89a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed89a-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed89a-136">-DefaultProfile</span></span>
<span data-ttu-id="ed89a-137">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ed89a-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed89a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed89a-138">CommonParameters</span></span>
<span data-ttu-id="ed89a-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed89a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed89a-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed89a-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed89a-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ed89a-141">INPUTS</span></span>

### <span data-ttu-id="ed89a-142">Microsoft. Azure. commands. SQL. Security. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="ed89a-142">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="ed89a-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ed89a-143">OUTPUTS</span></span>

### <span data-ttu-id="ed89a-144">Microsoft. Azure. commands. SQL. Security. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="ed89a-144">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="ed89a-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ed89a-145">NOTES</span></span>

## <span data-ttu-id="ed89a-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ed89a-146">RELATED LINKS</span></span>

[<span data-ttu-id="ed89a-147">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ed89a-147">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ed89a-148">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ed89a-148">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ed89a-149">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ed89a-149">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ed89a-150">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="ed89a-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


