---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 848A6972-AB29-46FB-8E03-FF2ADB113A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 5c43820c57531ca5a844e1ab429c26d85fecceee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920418"
---
# <span data-ttu-id="bb914-101">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="bb914-101">Get-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="bb914-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bb914-102">SYNOPSIS</span></span>
<span data-ttu-id="bb914-103">Hämtar reglerna för data maskning från en databas.</span><span class="sxs-lookup"><span data-stu-id="bb914-103">Gets the data masking rules from a database.</span></span>

## <span data-ttu-id="bb914-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bb914-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingRule [-SchemaName <String>] [-TableName <String>] [-ColumnName <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb914-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bb914-105">DESCRIPTION</span></span>
<span data-ttu-id="bb914-106">Cmdleten **Get-AzSqlDatabaseDataMaskingRule** eller alla data masknings regler för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="bb914-106">The **Get-AzSqlDatabaseDataMaskingRule** cmdlet gets either a specific data masking rule or all of the data masking rules for an Azure SQL database.</span></span>
<span data-ttu-id="bb914-107">Använd cmdleten genom att använda parametrarna *ResourceGroupName* , *servername* och *databasename* för att identifiera databasen och parametern *RuleID* för att ange vilken regel som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="bb914-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database, and the *RuleId* parameter to specify which rule this cmdlet returns.</span></span>
<span data-ttu-id="bb914-108">Om du inte tillhandahåller *RuleID* returneras alla data masknings regler för den Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="bb914-108">If you do not provide *RuleId* , all the data masking rules for that Azure SQL database are returned.</span></span>
<span data-ttu-id="bb914-109">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="bb914-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="bb914-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bb914-110">EXAMPLES</span></span>

### <span data-ttu-id="bb914-111">Exempel 1: Hämta alla data masknings regler från en databas</span><span class="sxs-lookup"><span data-stu-id="bb914-111">Example 1: Get all data masking rules from a database</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table1
ColumnName        : column1
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :

DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table2
ColumnName        : column2
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :
```

### <span data-ttu-id="bb914-112">Exempel 2: Hämta regeln för data maskering för schema "dbo", tabellen "Tabell1" och kolumnen "kolumn1".</span><span class="sxs-lookup"><span data-stu-id="bb914-112">Example 2: Get the data masking rule defined on schema "dbo", table "table1" and column "column1".</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table1
ColumnName        : column1
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :
```

## <span data-ttu-id="bb914-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bb914-113">PARAMETERS</span></span>

### <span data-ttu-id="bb914-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="bb914-114">-ColumnName</span></span>
<span data-ttu-id="bb914-115">Anger namnet på den kolumn som är avsedd för Maskerings regeln.</span><span class="sxs-lookup"><span data-stu-id="bb914-115">Specifies the name of the column targeted by the masking rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb914-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bb914-116">-DatabaseName</span></span>
<span data-ttu-id="bb914-117">Anger namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="bb914-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="bb914-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb914-118">-DefaultProfile</span></span>
<span data-ttu-id="bb914-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bb914-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb914-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb914-120">-ResourceGroupName</span></span>
<span data-ttu-id="bb914-121">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="bb914-121">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="bb914-122">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="bb914-122">-SchemaName</span></span>
<span data-ttu-id="bb914-123">Anger namnet på ett schema.</span><span class="sxs-lookup"><span data-stu-id="bb914-123">Specifies the name of a schema.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb914-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bb914-124">-ServerName</span></span>
<span data-ttu-id="bb914-125">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="bb914-125">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="bb914-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="bb914-126">-TableName</span></span>
<span data-ttu-id="bb914-127">Anger namnet på en Azure SQL-tabell.</span><span class="sxs-lookup"><span data-stu-id="bb914-127">Specifies the name of an Azure SQL table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb914-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bb914-128">-Confirm</span></span>
<span data-ttu-id="bb914-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bb914-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb914-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb914-130">-WhatIf</span></span>
<span data-ttu-id="bb914-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bb914-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb914-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bb914-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb914-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb914-133">CommonParameters</span></span>
<span data-ttu-id="bb914-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb914-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb914-135">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb914-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb914-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bb914-136">INPUTS</span></span>

### <span data-ttu-id="bb914-137">System. String</span><span class="sxs-lookup"><span data-stu-id="bb914-137">System.String</span></span>

## <span data-ttu-id="bb914-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bb914-138">OUTPUTS</span></span>

### <span data-ttu-id="bb914-139">Microsoft. Azure. commands. SQL. DataMasking. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="bb914-139">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="bb914-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bb914-140">NOTES</span></span>

## <span data-ttu-id="bb914-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bb914-141">RELATED LINKS</span></span>

[<span data-ttu-id="bb914-142">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="bb914-142">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="bb914-143">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="bb914-143">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="bb914-144">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="bb914-144">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="bb914-145">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="bb914-145">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="bb914-146">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="bb914-146">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

