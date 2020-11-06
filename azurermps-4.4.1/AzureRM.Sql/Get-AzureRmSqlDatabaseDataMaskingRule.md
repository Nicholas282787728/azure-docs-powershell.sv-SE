---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 848A6972-AB29-46FB-8E03-FF2ADB113A0E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: ced87eb217347629752683be5c72229da92dea64
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575789"
---
# <span data-ttu-id="8368d-101">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="8368d-101">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="8368d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8368d-102">SYNOPSIS</span></span>
<span data-ttu-id="8368d-103">Hämtar reglerna för data maskning från en databas.</span><span class="sxs-lookup"><span data-stu-id="8368d-103">Gets the data masking rules from a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8368d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8368d-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseDataMaskingRule [-SchemaName <String>] [-TableName <String>] [-ColumnName <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8368d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8368d-105">DESCRIPTION</span></span>
<span data-ttu-id="8368d-106">Cmdleten **Get-AzureRmSqlDatabaseDataMaskingRule** eller alla data masknings regler för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="8368d-106">The **Get-AzureRmSqlDatabaseDataMaskingRule** cmdlet gets either a specific data masking rule or all of the data masking rules for an Azure SQL database.</span></span>
<span data-ttu-id="8368d-107">Använd cmdleten genom att använda parametrarna *ResourceGroupName* , *servername* och *databasename* för att identifiera databasen och parametern *RuleID* för att ange vilken regel som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="8368d-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database, and the *RuleId* parameter to specify which rule this cmdlet returns.</span></span>
<span data-ttu-id="8368d-108">Om du inte tillhandahåller *RuleID* returneras alla data masknings regler för den Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="8368d-108">If you do not provide *RuleId* , all the data masking rules for that Azure SQL database are returned.</span></span>

<span data-ttu-id="8368d-109">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="8368d-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="8368d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8368d-110">EXAMPLES</span></span>

### <span data-ttu-id="8368d-111">Exempel 1: Hämta alla data masknings regler från en databas</span><span class="sxs-lookup"><span data-stu-id="8368d-111">Example 1: Get all data masking rules from a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
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

### <span data-ttu-id="8368d-112">Exempel 2: Hämta regeln för data maskering för schema "dbo", tabellen "Tabell1" och kolumnen "kolumn1".</span><span class="sxs-lookup"><span data-stu-id="8368d-112">Example 2: Get the data masking rule defined on schema "dbo", table "table1" and column "column1".</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
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

## <span data-ttu-id="8368d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8368d-113">PARAMETERS</span></span>

### <span data-ttu-id="8368d-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="8368d-114">-ColumnName</span></span>
<span data-ttu-id="8368d-115">Anger namnet på den kolumn som är avsedd för Maskerings regeln.</span><span class="sxs-lookup"><span data-stu-id="8368d-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="8368d-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8368d-116">-DatabaseName</span></span>
<span data-ttu-id="8368d-117">Anger namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="8368d-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="8368d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8368d-118">-ResourceGroupName</span></span>
<span data-ttu-id="8368d-119">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="8368d-119">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="8368d-120">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="8368d-120">-SchemaName</span></span>
<span data-ttu-id="8368d-121">Anger namnet på ett schema.</span><span class="sxs-lookup"><span data-stu-id="8368d-121">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="8368d-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8368d-122">-ServerName</span></span>
<span data-ttu-id="8368d-123">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="8368d-123">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="8368d-124">-TableName</span><span class="sxs-lookup"><span data-stu-id="8368d-124">-TableName</span></span>
<span data-ttu-id="8368d-125">Anger namnet på en Azure SQL-tabell.</span><span class="sxs-lookup"><span data-stu-id="8368d-125">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="8368d-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8368d-126">-Confirm</span></span>
<span data-ttu-id="8368d-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8368d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8368d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8368d-128">-WhatIf</span></span>
<span data-ttu-id="8368d-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8368d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8368d-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8368d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8368d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8368d-131">-DefaultProfile</span></span>
<span data-ttu-id="8368d-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8368d-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8368d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8368d-133">CommonParameters</span></span>
<span data-ttu-id="8368d-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8368d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8368d-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8368d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8368d-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8368d-136">INPUTS</span></span>

###  
<span data-ttu-id="8368d-137">Ingen.</span><span class="sxs-lookup"><span data-stu-id="8368d-137">None.</span></span>

## <span data-ttu-id="8368d-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8368d-138">OUTPUTS</span></span>

### <span data-ttu-id="8368d-139">Microsoft. Azure. commands. SQL. Security. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="8368d-139">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="8368d-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8368d-140">NOTES</span></span>

## <span data-ttu-id="8368d-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8368d-141">RELATED LINKS</span></span>

[<span data-ttu-id="8368d-142">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="8368d-142">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="8368d-143">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="8368d-143">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="8368d-144">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="8368d-144">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="8368d-145">Set-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="8368d-145">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="8368d-146">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="8368d-146">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)


