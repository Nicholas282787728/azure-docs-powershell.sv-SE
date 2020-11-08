---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 10afb514284fb3083110c068b33ffd189afd4039
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927218"
---
# <span data-ttu-id="97225-101">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="97225-101">Set-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="97225-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="97225-102">SYNOPSIS</span></span>
<span data-ttu-id="97225-103">Anger egenskaper för en data masknings regel för en databas.</span><span class="sxs-lookup"><span data-stu-id="97225-103">Sets the properties of a data masking rule for a database.</span></span>

## <span data-ttu-id="97225-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="97225-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="97225-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="97225-105">DESCRIPTION</span></span>
<span data-ttu-id="97225-106">Cmdleten **set-AzSqlDatabaseDataMaskingRule** anger en regel för data maskering för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="97225-106">The **Set-AzSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="97225-107">Använd cmdleten genom att ange parametrarna *ResourceGroupName* , *servername* , *databasename* och *RuleID* för att identifiera regeln.</span><span class="sxs-lookup"><span data-stu-id="97225-107">To use the cmdlet, provide the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="97225-108">Du kan ange parametrar för *SchemaName* , *TableName* och *columnName* för att omreglera regeln.</span><span class="sxs-lookup"><span data-stu-id="97225-108">You can provide any of the parameters of *SchemaName* , *TableName* , and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="97225-109">Ange parametern *MaskingFunction* om du vill ändra hur data maskeras.</span><span class="sxs-lookup"><span data-stu-id="97225-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>
<span data-ttu-id="97225-110">Om du anger ett värde för tal eller text för *MaskingFunction* kan du ange *NumberFrom* -och *NumberTo* -parametrar för maskering av mask eller *PrefixSize* , *ReplacementString* och *SuffixSize* för text maskning.</span><span class="sxs-lookup"><span data-stu-id="97225-110">If you specify a value of Number or Text for *MaskingFunction* , you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize* , *ReplacementString* , and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="97225-111">Om kommandot lyckas, och om du anger parametern *Passthru* , returnerar cmdleten ett objekt som beskriver regel egenskaperna för data maskering och regel-ID.</span><span class="sxs-lookup"><span data-stu-id="97225-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="97225-112">Regel-ID: n inkluderar, men är inte begränsade till, **ResourceGroupName** , **servername** , **databasename** och **RuleID**.</span><span class="sxs-lookup"><span data-stu-id="97225-112">Rule identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , **DatabaseName** , and **RuleId**.</span></span>
<span data-ttu-id="97225-113">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="97225-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="97225-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="97225-114">EXAMPLES</span></span>

### <span data-ttu-id="97225-115">Exempel 1: ändra området för en regel för data maskering i en databas</span><span class="sxs-lookup"><span data-stu-id="97225-115">Example 1: Change the range of a data masking rule in a database</span></span>
```
PS C:\>Set-AzSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="97225-116">Det här kommandot ändrar en regel för data maskering med ID-Rule17.</span><span class="sxs-lookup"><span data-stu-id="97225-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="97225-117">Den regeln körs i databasen som heter Database01 på Server Server01.</span><span class="sxs-lookup"><span data-stu-id="97225-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="97225-118">Det här kommandot ändrar gränserna för det intervall som ett slumptal skapas i.</span><span class="sxs-lookup"><span data-stu-id="97225-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="97225-119">Det nya området är mellan 23 och 42.</span><span class="sxs-lookup"><span data-stu-id="97225-119">The new range is between 23 and 42.</span></span>

## <span data-ttu-id="97225-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="97225-120">PARAMETERS</span></span>

### <span data-ttu-id="97225-121">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="97225-121">-ColumnName</span></span>
<span data-ttu-id="97225-122">Anger namnet på den kolumn som är avsedd för Maskerings regeln.</span><span class="sxs-lookup"><span data-stu-id="97225-122">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="97225-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="97225-123">-DatabaseName</span></span>
<span data-ttu-id="97225-124">Anger namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="97225-124">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="97225-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97225-125">-DefaultProfile</span></span>
<span data-ttu-id="97225-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="97225-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97225-127">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="97225-127">-MaskingFunction</span></span>
<span data-ttu-id="97225-128">Anger den Maskerings funktion som används i regeln.</span><span class="sxs-lookup"><span data-stu-id="97225-128">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="97225-129">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="97225-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="97225-130">Vis</span><span class="sxs-lookup"><span data-stu-id="97225-130">Default</span></span>
- <span data-ttu-id="97225-131">Nomaskering</span><span class="sxs-lookup"><span data-stu-id="97225-131">NoMasking</span></span>
- <span data-ttu-id="97225-132">Textrad</span><span class="sxs-lookup"><span data-stu-id="97225-132">Text</span></span>
- <span data-ttu-id="97225-133">Numeriska</span><span class="sxs-lookup"><span data-stu-id="97225-133">Number</span></span>
- <span data-ttu-id="97225-134">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="97225-134">SocialSecurityNumber</span></span>
- <span data-ttu-id="97225-135">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="97225-135">CreditCardNumber</span></span>
- <span data-ttu-id="97225-136">E-post standardvärdet är standard.</span><span class="sxs-lookup"><span data-stu-id="97225-136">Email The default value is Default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97225-137">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="97225-137">-NumberFrom</span></span>
<span data-ttu-id="97225-138">Anger det nedre gräns numret för intervallet som ett slumpmässigt värde är markerat för.</span><span class="sxs-lookup"><span data-stu-id="97225-138">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="97225-139">Ange endast den här parametern om du anger ett värde för tal för parametern *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="97225-139">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="97225-140">Standardvärdet är 0.</span><span class="sxs-lookup"><span data-stu-id="97225-140">The default value is 0.</span></span>

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

### <span data-ttu-id="97225-141">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="97225-141">-NumberTo</span></span>
<span data-ttu-id="97225-142">Anger det övre gräns numret för intervallet som ett slumpmässigt värde är markerat.</span><span class="sxs-lookup"><span data-stu-id="97225-142">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="97225-143">Ange endast den här parametern om du anger ett värde för tal för parametern *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="97225-143">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="97225-144">Standardvärdet är 0.</span><span class="sxs-lookup"><span data-stu-id="97225-144">The default value is 0.</span></span>

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

### <span data-ttu-id="97225-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97225-145">-PassThru</span></span>
<span data-ttu-id="97225-146">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="97225-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="97225-147">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="97225-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="97225-148">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="97225-148">-PrefixSize</span></span>
<span data-ttu-id="97225-149">Anger antalet tecken i början av den text som inte är maskerad.</span><span class="sxs-lookup"><span data-stu-id="97225-149">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="97225-150">Ange endast den här parametern om du anger ett text värde för parametern *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="97225-150">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="97225-151">Standardvärdet är 0.</span><span class="sxs-lookup"><span data-stu-id="97225-151">The default value is 0.</span></span>

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

### <span data-ttu-id="97225-152">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="97225-152">-ReplacementString</span></span>
<span data-ttu-id="97225-153">Anger antalet tecken i slutet av texten som inte maskeras.</span><span class="sxs-lookup"><span data-stu-id="97225-153">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="97225-154">Ange endast den här parametern om du anger ett text värde för parametern *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="97225-154">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="97225-155">Standardvärdet är 0.</span><span class="sxs-lookup"><span data-stu-id="97225-155">The default value is 0.</span></span>

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

### <span data-ttu-id="97225-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97225-156">-ResourceGroupName</span></span>
<span data-ttu-id="97225-157">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="97225-157">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="97225-158">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="97225-158">-SchemaName</span></span>
<span data-ttu-id="97225-159">Anger namnet på ett schema.</span><span class="sxs-lookup"><span data-stu-id="97225-159">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="97225-160">-ServerName</span><span class="sxs-lookup"><span data-stu-id="97225-160">-ServerName</span></span>
<span data-ttu-id="97225-161">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="97225-161">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="97225-162">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="97225-162">-SuffixSize</span></span>
<span data-ttu-id="97225-163">Anger antalet tecken i slutet av texten som inte maskeras.</span><span class="sxs-lookup"><span data-stu-id="97225-163">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="97225-164">Ange endast den här parametern om du anger ett text värde för parametern *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="97225-164">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="97225-165">Standardvärdet är 0.</span><span class="sxs-lookup"><span data-stu-id="97225-165">The default value is 0.</span></span>

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

### <span data-ttu-id="97225-166">-TableName</span><span class="sxs-lookup"><span data-stu-id="97225-166">-TableName</span></span>
<span data-ttu-id="97225-167">Anger namnet på den databas tabell som innehåller den maskerade kolumnen.</span><span class="sxs-lookup"><span data-stu-id="97225-167">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="97225-168">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="97225-168">-Confirm</span></span>
<span data-ttu-id="97225-169">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="97225-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97225-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97225-170">-WhatIf</span></span>
<span data-ttu-id="97225-171">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="97225-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97225-172">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="97225-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97225-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97225-173">CommonParameters</span></span>
<span data-ttu-id="97225-174">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97225-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97225-175">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97225-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97225-176">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="97225-176">INPUTS</span></span>

### <span data-ttu-id="97225-177">System. String</span><span class="sxs-lookup"><span data-stu-id="97225-177">System.String</span></span>

### <span data-ttu-id="97225-178">System. Nullable ' 1 [[system. UInt32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="97225-178">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="97225-179">System. Nullable ' 1 [[system. Double, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="97225-179">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="97225-180">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="97225-180">OUTPUTS</span></span>

### <span data-ttu-id="97225-181">Microsoft. Azure. commands. SQL. DataMasking. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="97225-181">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="97225-182">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="97225-182">NOTES</span></span>

## <span data-ttu-id="97225-183">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="97225-183">RELATED LINKS</span></span>

[<span data-ttu-id="97225-184">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="97225-184">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="97225-185">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="97225-185">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="97225-186">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="97225-186">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="97225-187">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="97225-187">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

