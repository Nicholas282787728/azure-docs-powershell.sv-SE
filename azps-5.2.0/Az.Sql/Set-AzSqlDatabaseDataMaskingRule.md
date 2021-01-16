---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 544db2f0e23cb510c81fb64898b6bcf856e760e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400739"
---
# <span data-ttu-id="9173f-101">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="9173f-101">Set-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="9173f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9173f-102">SYNOPSIS</span></span>
<span data-ttu-id="9173f-103">Anger egenskaper för en data masknings regel för en databas.</span><span class="sxs-lookup"><span data-stu-id="9173f-103">Sets the properties of a data masking rule for a database.</span></span>

## <span data-ttu-id="9173f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9173f-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9173f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9173f-105">DESCRIPTION</span></span>
<span data-ttu-id="9173f-106">Cmdleten **set-AzSqlDatabaseDataMaskingRule** anger en regel för data maskering för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="9173f-106">The **Set-AzSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="9173f-107">Använd cmdleten genom att ange parametrarna *ResourceGroupName*, *servername*, *databasename* och *RuleID* för att identifiera regeln.</span><span class="sxs-lookup"><span data-stu-id="9173f-107">To use the cmdlet, provide the *ResourceGroupName*, *ServerName*, *DatabaseName*, and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="9173f-108">Du kan ange parametrar för *SchemaName*, *TableName* och *columnName* för att omreglera regeln.</span><span class="sxs-lookup"><span data-stu-id="9173f-108">You can provide any of the parameters of *SchemaName*, *TableName*, and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="9173f-109">Ange parametern *MaskingFunction* om du vill ändra hur data maskeras.</span><span class="sxs-lookup"><span data-stu-id="9173f-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>
<span data-ttu-id="9173f-110">Om du anger ett värde för tal eller text för *MaskingFunction* kan du ange *NumberFrom* -och *NumberTo* -parametrar för maskering av mask eller *PrefixSize*, *ReplacementString* och *SuffixSize* för text maskning.</span><span class="sxs-lookup"><span data-stu-id="9173f-110">If you specify a value of Number or Text for *MaskingFunction*, you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize*, *ReplacementString*, and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="9173f-111">Om kommandot lyckas, och om du anger parametern *Passthru* , returnerar cmdleten ett objekt som beskriver regel egenskaperna för data maskering och regel-ID.</span><span class="sxs-lookup"><span data-stu-id="9173f-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="9173f-112">Regel-ID: n inkluderar, men är inte begränsade till, **ResourceGroupName**, **servername**, **databasename** och **RuleID**.</span><span class="sxs-lookup"><span data-stu-id="9173f-112">Rule identifiers include, but are not limited to, **ResourceGroupName**, **ServerName**, **DatabaseName**, and **RuleId**.</span></span>
<span data-ttu-id="9173f-113">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="9173f-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="9173f-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9173f-114">EXAMPLES</span></span>

### <span data-ttu-id="9173f-115">Exempel 1: ändra området för en regel för data maskering i en databas</span><span class="sxs-lookup"><span data-stu-id="9173f-115">Example 1: Change the range of a data masking rule in a database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="9173f-116">Det här kommandot ändrar en regel för data maskering med ID-Rule17.</span><span class="sxs-lookup"><span data-stu-id="9173f-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="9173f-117">Den regeln körs i databasen som heter Database01 på Server Server01.</span><span class="sxs-lookup"><span data-stu-id="9173f-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="9173f-118">Det här kommandot ändrar gränserna för det intervall som ett slumptal skapas i.</span><span class="sxs-lookup"><span data-stu-id="9173f-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="9173f-119">Det nya området är mellan 23 och 42.</span><span class="sxs-lookup"><span data-stu-id="9173f-119">The new range is between 23 and 42.</span></span>

### <span data-ttu-id="9173f-120">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9173f-120">Example 2</span></span>

<span data-ttu-id="9173f-121">Anger egenskaper för en data masknings regel för en databas.</span><span class="sxs-lookup"><span data-stu-id="9173f-121">Sets the properties of a data masking rule for a database.</span></span> <span data-ttu-id="9173f-122">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="9173f-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlDatabaseDataMaskingRule -ColumnName 'column1' -DatabaseName $params.databaseName -MaskingFunction NoMasking -NumberFrom 5 -NumberTo 14 -PrefixSize <UInt32> -ReplacementString <String> -ResourceGroupName $params.rgname -SchemaName 'dbo' -ServerName $params.serverName -SuffixSize <UInt32> -TableName 'table1'
```

## <span data-ttu-id="9173f-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9173f-123">PARAMETERS</span></span>

### <span data-ttu-id="9173f-124">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="9173f-124">-ColumnName</span></span>
<span data-ttu-id="9173f-125">Anger namnet på den kolumn som är avsedd för Maskerings regeln.</span><span class="sxs-lookup"><span data-stu-id="9173f-125">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="9173f-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9173f-126">-DatabaseName</span></span>
<span data-ttu-id="9173f-127">Anger namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="9173f-127">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="9173f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9173f-128">-DefaultProfile</span></span>
<span data-ttu-id="9173f-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9173f-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9173f-130">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="9173f-130">-MaskingFunction</span></span>
<span data-ttu-id="9173f-131">Anger den Maskerings funktion som används i regeln.</span><span class="sxs-lookup"><span data-stu-id="9173f-131">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="9173f-132">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="9173f-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9173f-133">Vis</span><span class="sxs-lookup"><span data-stu-id="9173f-133">Default</span></span>
- <span data-ttu-id="9173f-134">Nomaskering</span><span class="sxs-lookup"><span data-stu-id="9173f-134">NoMasking</span></span>
- <span data-ttu-id="9173f-135">Textrad</span><span class="sxs-lookup"><span data-stu-id="9173f-135">Text</span></span>
- <span data-ttu-id="9173f-136">Numeriska</span><span class="sxs-lookup"><span data-stu-id="9173f-136">Number</span></span>
- <span data-ttu-id="9173f-137">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="9173f-137">SocialSecurityNumber</span></span>
- <span data-ttu-id="9173f-138">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="9173f-138">CreditCardNumber</span></span>
- <span data-ttu-id="9173f-139">E-post standardvärdet är standard.</span><span class="sxs-lookup"><span data-stu-id="9173f-139">Email The default value is Default.</span></span>

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

### <span data-ttu-id="9173f-140">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="9173f-140">-NumberFrom</span></span>
<span data-ttu-id="9173f-141">Anger det nedre gräns numret för intervallet som ett slumpmässigt värde är markerat för.</span><span class="sxs-lookup"><span data-stu-id="9173f-141">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="9173f-142">Ange endast den här parametern om du anger ett värde för tal för parametern *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="9173f-142">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="9173f-143">Standardvärdet är 0.</span><span class="sxs-lookup"><span data-stu-id="9173f-143">The default value is 0.</span></span>

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

### <span data-ttu-id="9173f-144">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="9173f-144">-NumberTo</span></span>
<span data-ttu-id="9173f-145">Anger det övre gräns numret för intervallet som ett slumpmässigt värde är markerat.</span><span class="sxs-lookup"><span data-stu-id="9173f-145">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="9173f-146">Ange endast den här parametern om du anger ett värde för tal för parametern *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="9173f-146">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="9173f-147">Standardvärdet är 0.</span><span class="sxs-lookup"><span data-stu-id="9173f-147">The default value is 0.</span></span>

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

### <span data-ttu-id="9173f-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9173f-148">-PassThru</span></span>
<span data-ttu-id="9173f-149">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="9173f-149">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9173f-150">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="9173f-150">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9173f-151">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="9173f-151">-PrefixSize</span></span>
<span data-ttu-id="9173f-152">Anger antalet tecken i början av den text som inte är maskerad.</span><span class="sxs-lookup"><span data-stu-id="9173f-152">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="9173f-153">Ange endast den här parametern om du anger ett text värde för parametern *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="9173f-153">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="9173f-154">Standardvärdet är 0.</span><span class="sxs-lookup"><span data-stu-id="9173f-154">The default value is 0.</span></span>

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

### <span data-ttu-id="9173f-155">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="9173f-155">-ReplacementString</span></span>
<span data-ttu-id="9173f-156">Anger antalet tecken i slutet av texten som inte maskeras.</span><span class="sxs-lookup"><span data-stu-id="9173f-156">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="9173f-157">Ange endast den här parametern om du anger ett text värde för parametern *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="9173f-157">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="9173f-158">Standardvärdet är 0.</span><span class="sxs-lookup"><span data-stu-id="9173f-158">The default value is 0.</span></span>

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

### <span data-ttu-id="9173f-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9173f-159">-ResourceGroupName</span></span>
<span data-ttu-id="9173f-160">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="9173f-160">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="9173f-161">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="9173f-161">-SchemaName</span></span>
<span data-ttu-id="9173f-162">Anger namnet på ett schema.</span><span class="sxs-lookup"><span data-stu-id="9173f-162">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="9173f-163">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9173f-163">-ServerName</span></span>
<span data-ttu-id="9173f-164">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="9173f-164">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="9173f-165">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="9173f-165">-SuffixSize</span></span>
<span data-ttu-id="9173f-166">Anger antalet tecken i slutet av texten som inte maskeras.</span><span class="sxs-lookup"><span data-stu-id="9173f-166">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="9173f-167">Ange endast den här parametern om du anger ett text värde för parametern *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="9173f-167">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="9173f-168">Standardvärdet är 0.</span><span class="sxs-lookup"><span data-stu-id="9173f-168">The default value is 0.</span></span>

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

### <span data-ttu-id="9173f-169">-TableName</span><span class="sxs-lookup"><span data-stu-id="9173f-169">-TableName</span></span>
<span data-ttu-id="9173f-170">Anger namnet på den databas tabell som innehåller den maskerade kolumnen.</span><span class="sxs-lookup"><span data-stu-id="9173f-170">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="9173f-171">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9173f-171">-Confirm</span></span>
<span data-ttu-id="9173f-172">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9173f-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9173f-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9173f-173">-WhatIf</span></span>
<span data-ttu-id="9173f-174">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9173f-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9173f-175">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9173f-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9173f-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9173f-176">CommonParameters</span></span>
<span data-ttu-id="9173f-177">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9173f-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9173f-178">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9173f-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9173f-179">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9173f-179">INPUTS</span></span>

### <span data-ttu-id="9173f-180">System. String</span><span class="sxs-lookup"><span data-stu-id="9173f-180">System.String</span></span>

### <span data-ttu-id="9173f-181">System. Nullable ' 1 [[system. UInt32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9173f-181">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9173f-182">System. Nullable ' 1 [[system. Double, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9173f-182">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9173f-183">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9173f-183">OUTPUTS</span></span>

### <span data-ttu-id="9173f-184">Microsoft. Azure. commands. SQL. DataMasking. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="9173f-184">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="9173f-185">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9173f-185">NOTES</span></span>

## <span data-ttu-id="9173f-186">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9173f-186">RELATED LINKS</span></span>

[<span data-ttu-id="9173f-187">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="9173f-187">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="9173f-188">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="9173f-188">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="9173f-189">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="9173f-189">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="9173f-190">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="9173f-190">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


