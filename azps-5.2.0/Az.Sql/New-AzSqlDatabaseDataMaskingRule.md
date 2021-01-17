---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 35f2bc63366a86501650af1808274a3a0403e77f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411136"
---
# <span data-ttu-id="def19-101">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="def19-101">New-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="def19-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="def19-102">SYNOPSIS</span></span>
<span data-ttu-id="def19-103">Skapar en data masknings regel för en databas.</span><span class="sxs-lookup"><span data-stu-id="def19-103">Creates a data masking rule for a database.</span></span>

## <span data-ttu-id="def19-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="def19-104">SYNTAX</span></span>

```
New-AzSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>] [-ReplacementString <String>]
 [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru] -SchemaName <String>
 -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="def19-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="def19-105">DESCRIPTION</span></span>
<span data-ttu-id="def19-106">Cmdleten **New-AzSqlDatabaseDataMaskingRule** skapar en data masknings regel för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="def19-106">The **New-AzSqlDatabaseDataMaskingRule** cmdlet creates a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="def19-107">Använd cmdleten *ResourceGroupName*, *servername* och *databasename* för att identifiera regeln.</span><span class="sxs-lookup"><span data-stu-id="def19-107">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the rule.</span></span>
<span data-ttu-id="def19-108">Ange *tabellens* mål *och det namn* som ska användas för att definiera hur data ska maskeras med TableName och *columnName* .</span><span class="sxs-lookup"><span data-stu-id="def19-108">Provide the *TableName* and *ColumnName* to specify the target of the rule and the *MaskingFunction* parameter to define how the data is masked.</span></span>
<span data-ttu-id="def19-109">Om *MaskingFunction* har ett värde för tal eller text kan du ange *NumberFrom* -och *NumberTo* -parametrar för maskering av nummer eller *PrefixSize*, *ReplacementString* och *SuffixSize* för text maskering.</span><span class="sxs-lookup"><span data-stu-id="def19-109">If *MaskingFunction* has a value of Number or Text, you can specify the *NumberFrom* and *NumberTo* parameters, for number masking, or the *PrefixSize*, *ReplacementString*, and *SuffixSize* for text masking.</span></span>
<span data-ttu-id="def19-110">Om kommandot fungerar och parametern *Passthru* används, returnerar cmdleten ett objekt som beskriver regel egenskaperna för data maskering, utöver regel identifierarna.</span><span class="sxs-lookup"><span data-stu-id="def19-110">If the command succeeds and the *PassThru* parameter is used, the cmdlet returns an object describing the data masking rule properties in addition to the rule identifiers.</span></span>
<span data-ttu-id="def19-111">Regel-ID: n inkluderar, men är inte begränsade till, *ResourceGroupName*, *servername*, *databasename* och *RuleID*.</span><span class="sxs-lookup"><span data-stu-id="def19-111">Rule identifiers include, but are not limited to, *ResourceGroupName*, *ServerName*, *DatabaseName*, and *RuleID*.</span></span>
<span data-ttu-id="def19-112">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="def19-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="def19-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="def19-113">EXAMPLES</span></span>

### <span data-ttu-id="def19-114">Exempel 1: skapa en data mask regel för en siffer kolumn i en databas</span><span class="sxs-lookup"><span data-stu-id="def19-114">Example 1: Create a data masking rule for a number column in a database</span></span>
```
PS C:\>New-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"  -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

<span data-ttu-id="def19-115">Det här kommandot skapar en data masknings regel för kolumnen med namnet Column01 i tabellen som heter Table01 i schemat som heter Schema01.</span><span class="sxs-lookup"><span data-stu-id="def19-115">This command creates a data masking rule for the column named Column01 in the table named Table01 in the schema named Schema01.</span></span>
<span data-ttu-id="def19-116">Den databas som heter Database01 innehåller alla dessa objekt.</span><span class="sxs-lookup"><span data-stu-id="def19-116">The database named Database01 contains all these items.</span></span>
<span data-ttu-id="def19-117">Regeln är en nummer mask regel som använder ett slumptal mellan 5 och 14 som mask värde.</span><span class="sxs-lookup"><span data-stu-id="def19-117">The rule is a number masking rule that uses a random number between 5 and 14 as the mask value.</span></span>

## <span data-ttu-id="def19-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="def19-118">PARAMETERS</span></span>

### <span data-ttu-id="def19-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="def19-119">-ColumnName</span></span>
<span data-ttu-id="def19-120">Anger namnet på den kolumn som är avsedd för Maskerings regeln.</span><span class="sxs-lookup"><span data-stu-id="def19-120">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="def19-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="def19-121">-DatabaseName</span></span>
<span data-ttu-id="def19-122">Anger namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="def19-122">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="def19-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="def19-123">-DefaultProfile</span></span>
<span data-ttu-id="def19-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="def19-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="def19-125">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="def19-125">-MaskingFunction</span></span>
<span data-ttu-id="def19-126">Anger den Maskerings funktion som används i regeln.</span><span class="sxs-lookup"><span data-stu-id="def19-126">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="def19-127">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="def19-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="def19-128">Vis</span><span class="sxs-lookup"><span data-stu-id="def19-128">Default</span></span>
- <span data-ttu-id="def19-129">Nomaskering</span><span class="sxs-lookup"><span data-stu-id="def19-129">NoMasking</span></span>
- <span data-ttu-id="def19-130">Textrad</span><span class="sxs-lookup"><span data-stu-id="def19-130">Text</span></span>
- <span data-ttu-id="def19-131">Numeriska</span><span class="sxs-lookup"><span data-stu-id="def19-131">Number</span></span>
- <span data-ttu-id="def19-132">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="def19-132">SocialSecurityNumber</span></span>
- <span data-ttu-id="def19-133">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="def19-133">CreditCardNumber</span></span>
- <span data-ttu-id="def19-134">E-post standardvärdet är standard.</span><span class="sxs-lookup"><span data-stu-id="def19-134">Email The default value is Default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="def19-135">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="def19-135">-NumberFrom</span></span>
<span data-ttu-id="def19-136">Anger det nedre gräns numret för intervallet som ett slumpmässigt värde är markerat för.</span><span class="sxs-lookup"><span data-stu-id="def19-136">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="def19-137">Ange endast den här parametern om du anger ett värde för tal för parametern *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="def19-137">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="def19-138">Standardvärdet är 0.</span><span class="sxs-lookup"><span data-stu-id="def19-138">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="def19-139">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="def19-139">-NumberTo</span></span>
<span data-ttu-id="def19-140">Anger det övre gräns numret för intervallet som ett slumpmässigt värde är markerat.</span><span class="sxs-lookup"><span data-stu-id="def19-140">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="def19-141">Ange endast den här parametern om du anger ett värde för tal för parametern *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="def19-141">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="def19-142">Standardvärdet är 0.</span><span class="sxs-lookup"><span data-stu-id="def19-142">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="def19-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="def19-143">-PassThru</span></span>
<span data-ttu-id="def19-144">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="def19-144">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="def19-145">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="def19-145">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="def19-146">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="def19-146">-PrefixSize</span></span>
<span data-ttu-id="def19-147">Anger antalet tecken i början av den text som inte är maskerad.</span><span class="sxs-lookup"><span data-stu-id="def19-147">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="def19-148">Ange endast den här parametern om du anger ett text värde för parametern *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="def19-148">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="def19-149">Standardvärdet är 0.</span><span class="sxs-lookup"><span data-stu-id="def19-149">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="def19-150">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="def19-150">-ReplacementString</span></span>
<span data-ttu-id="def19-151">Anger antalet tecken i slutet av texten som inte maskeras.</span><span class="sxs-lookup"><span data-stu-id="def19-151">Specifies the number of characters in the end of the text that are not masked.</span></span>
<span data-ttu-id="def19-152">Ange endast den här parametern om du anger ett text värde för parametern *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="def19-152">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="def19-153">Standardvärdet är en tom sträng.</span><span class="sxs-lookup"><span data-stu-id="def19-153">The default value is an empty string.</span></span>

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

### <span data-ttu-id="def19-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="def19-154">-ResourceGroupName</span></span>
<span data-ttu-id="def19-155">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="def19-155">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="def19-156">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="def19-156">-SchemaName</span></span>
<span data-ttu-id="def19-157">Anger namnet på ett schema.</span><span class="sxs-lookup"><span data-stu-id="def19-157">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="def19-158">-ServerName</span><span class="sxs-lookup"><span data-stu-id="def19-158">-ServerName</span></span>
<span data-ttu-id="def19-159">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="def19-159">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="def19-160">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="def19-160">-SuffixSize</span></span>
<span data-ttu-id="def19-161">Anger antalet tecken i slutet av texten som inte maskeras.</span><span class="sxs-lookup"><span data-stu-id="def19-161">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="def19-162">Ange endast den här parametern om du anger ett text värde för parametern *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="def19-162">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="def19-163">Standardvärdet är 0.</span><span class="sxs-lookup"><span data-stu-id="def19-163">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="def19-164">-TableName</span><span class="sxs-lookup"><span data-stu-id="def19-164">-TableName</span></span>
<span data-ttu-id="def19-165">Anger namnet på den databas tabell som innehåller den maskerade kolumnen.</span><span class="sxs-lookup"><span data-stu-id="def19-165">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="def19-166">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="def19-166">-Confirm</span></span>
<span data-ttu-id="def19-167">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="def19-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="def19-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="def19-168">-WhatIf</span></span>
<span data-ttu-id="def19-169">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="def19-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="def19-170">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="def19-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="def19-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="def19-171">CommonParameters</span></span>
<span data-ttu-id="def19-172">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="def19-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="def19-173">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="def19-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="def19-174">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="def19-174">INPUTS</span></span>

### <span data-ttu-id="def19-175">System. String</span><span class="sxs-lookup"><span data-stu-id="def19-175">System.String</span></span>

### <span data-ttu-id="def19-176">System. Nullable ' 1 [[system. UInt32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="def19-176">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="def19-177">System. Nullable ' 1 [[system. Double, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="def19-177">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="def19-178">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="def19-178">OUTPUTS</span></span>

### <span data-ttu-id="def19-179">Microsoft. Azure. commands. SQL. DataMasking. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="def19-179">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="def19-180">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="def19-180">NOTES</span></span>

## <span data-ttu-id="def19-181">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="def19-181">RELATED LINKS</span></span>

[<span data-ttu-id="def19-182">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="def19-182">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="def19-183">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="def19-183">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="def19-184">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="def19-184">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="def19-185">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="def19-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


