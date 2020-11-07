---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 1a26cc83bfd42ba63f2ae914ea6c288b862ccaf5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574474"
---
# <span data-ttu-id="4f6df-101">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="4f6df-101">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="4f6df-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4f6df-102">SYNOPSIS</span></span>
<span data-ttu-id="4f6df-103">Anger egenskaper för en data masknings regel för en databas.</span><span class="sxs-lookup"><span data-stu-id="4f6df-103">Sets the properties of a data masking rule for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f6df-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4f6df-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4f6df-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4f6df-105">DESCRIPTION</span></span>
<span data-ttu-id="4f6df-106">Cmdleten **set-AzureRmSqlDatabaseDataMaskingRule** anger en regel för data maskering för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="4f6df-106">The **Set-AzureRmSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="4f6df-107">Använd cmdleten genom att ange parametrarna *ResourceGroupName* , *servername* , *databasename* och *RuleID* för att identifiera regeln.</span><span class="sxs-lookup"><span data-stu-id="4f6df-107">To use the cmdlet, provide the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="4f6df-108">Du kan ange parametrar för *SchemaName* , *TableName* och *columnName* för att omreglera regeln.</span><span class="sxs-lookup"><span data-stu-id="4f6df-108">You can provide any of the parameters of *SchemaName* , *TableName* , and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="4f6df-109">Ange parametern *MaskingFunction* om du vill ändra hur data maskeras.</span><span class="sxs-lookup"><span data-stu-id="4f6df-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>

<span data-ttu-id="4f6df-110">Om du anger ett värde för tal eller text för *MaskingFunction* kan du ange *NumberFrom* -och *NumberTo* -parametrar för maskering av mask eller *PrefixSize* , *ReplacementString* och *SuffixSize* för text maskning.</span><span class="sxs-lookup"><span data-stu-id="4f6df-110">If you specify a value of Number or Text for *MaskingFunction* , you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize* , *ReplacementString* , and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="4f6df-111">Om kommandot lyckas, och om du anger parametern *Passthru* , returnerar cmdleten ett objekt som beskriver regel egenskaperna för data maskering och regel-ID.</span><span class="sxs-lookup"><span data-stu-id="4f6df-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="4f6df-112">Regel-ID: n inkluderar, men är inte begränsade till, **ResourceGroupName** , **servername** , **databasename** och **RuleID**.</span><span class="sxs-lookup"><span data-stu-id="4f6df-112">Rule identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , **DatabaseName** , and **RuleId**.</span></span>

<span data-ttu-id="4f6df-113">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="4f6df-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="4f6df-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4f6df-114">EXAMPLES</span></span>

### <span data-ttu-id="4f6df-115">Exempel 1: ändra området för en regel för data maskering i en databas</span><span class="sxs-lookup"><span data-stu-id="4f6df-115">Example 1: Change the range of a data masking rule in a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="4f6df-116">Det här kommandot ändrar en regel för data maskering med ID-Rule17.</span><span class="sxs-lookup"><span data-stu-id="4f6df-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="4f6df-117">Den regeln körs i databasen som heter Database01 på Server Server01.</span><span class="sxs-lookup"><span data-stu-id="4f6df-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="4f6df-118">Det här kommandot ändrar gränserna för det intervall som ett slumptal skapas i.</span><span class="sxs-lookup"><span data-stu-id="4f6df-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="4f6df-119">Det nya området är mellan 23 och 42.</span><span class="sxs-lookup"><span data-stu-id="4f6df-119">The new range is between 23 and 42.</span></span>

## <span data-ttu-id="4f6df-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4f6df-120">PARAMETERS</span></span>

### <span data-ttu-id="4f6df-121">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="4f6df-121">-ColumnName</span></span>
<span data-ttu-id="4f6df-122">Anger namnet på den kolumn som är avsedd för Maskerings regeln.</span><span class="sxs-lookup"><span data-stu-id="4f6df-122">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="4f6df-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4f6df-123">-DatabaseName</span></span>
<span data-ttu-id="4f6df-124">Anger namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="4f6df-124">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="4f6df-125">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="4f6df-125">-MaskingFunction</span></span>
<span data-ttu-id="4f6df-126">Anger den Maskerings funktion som används i regeln.</span><span class="sxs-lookup"><span data-stu-id="4f6df-126">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="4f6df-127">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="4f6df-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4f6df-128">Vis</span><span class="sxs-lookup"><span data-stu-id="4f6df-128">Default</span></span>
- <span data-ttu-id="4f6df-129">Nomaskering</span><span class="sxs-lookup"><span data-stu-id="4f6df-129">NoMasking</span></span>
- <span data-ttu-id="4f6df-130">Textrad</span><span class="sxs-lookup"><span data-stu-id="4f6df-130">Text</span></span>
- <span data-ttu-id="4f6df-131">Numeriska</span><span class="sxs-lookup"><span data-stu-id="4f6df-131">Number</span></span>
- <span data-ttu-id="4f6df-132">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="4f6df-132">SocialSecurityNumber</span></span>
- <span data-ttu-id="4f6df-133">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="4f6df-133">CreditCardNumber</span></span>
- <span data-ttu-id="4f6df-134">E-</span><span class="sxs-lookup"><span data-stu-id="4f6df-134">Email</span></span>

<span data-ttu-id="4f6df-135">Standardvärdet är standard.</span><span class="sxs-lookup"><span data-stu-id="4f6df-135">The default value is Default.</span></span>

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

### <span data-ttu-id="4f6df-136">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="4f6df-136">-NumberFrom</span></span>
<span data-ttu-id="4f6df-137">Anger det nedre gräns numret för intervallet som ett slumpmässigt värde är markerat för.</span><span class="sxs-lookup"><span data-stu-id="4f6df-137">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="4f6df-138">Ange endast den här parametern om du anger ett värde för tal för parametern *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="4f6df-138">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="4f6df-139">Standardvärdet är 0.</span><span class="sxs-lookup"><span data-stu-id="4f6df-139">The default value is 0.</span></span>

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

### <span data-ttu-id="4f6df-140">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="4f6df-140">-NumberTo</span></span>
<span data-ttu-id="4f6df-141">Anger det övre gräns numret för intervallet som ett slumpmässigt värde är markerat.</span><span class="sxs-lookup"><span data-stu-id="4f6df-141">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="4f6df-142">Ange endast den här parametern om du anger ett värde för tal för parametern *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="4f6df-142">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="4f6df-143">Standardvärdet är 0.</span><span class="sxs-lookup"><span data-stu-id="4f6df-143">The default value is 0.</span></span>

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

### <span data-ttu-id="4f6df-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f6df-144">-PassThru</span></span>
<span data-ttu-id="4f6df-145">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="4f6df-145">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4f6df-146">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="4f6df-146">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4f6df-147">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="4f6df-147">-PrefixSize</span></span>
<span data-ttu-id="4f6df-148">Anger antalet tecken i början av den text som inte är maskerad.</span><span class="sxs-lookup"><span data-stu-id="4f6df-148">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="4f6df-149">Ange endast den här parametern om du anger ett text värde för parametern *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="4f6df-149">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="4f6df-150">Standardvärdet är 0.</span><span class="sxs-lookup"><span data-stu-id="4f6df-150">The default value is 0.</span></span>

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

### <span data-ttu-id="4f6df-151">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="4f6df-151">-ReplacementString</span></span>
<span data-ttu-id="4f6df-152">Anger antalet tecken i slutet av texten som inte maskeras.</span><span class="sxs-lookup"><span data-stu-id="4f6df-152">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="4f6df-153">Ange endast den här parametern om du anger ett text värde för parametern *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="4f6df-153">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="4f6df-154">Standardvärdet är 0.</span><span class="sxs-lookup"><span data-stu-id="4f6df-154">The default value is 0.</span></span>

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

### <span data-ttu-id="4f6df-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f6df-155">-ResourceGroupName</span></span>
<span data-ttu-id="4f6df-156">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="4f6df-156">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="4f6df-157">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="4f6df-157">-SchemaName</span></span>
<span data-ttu-id="4f6df-158">Anger namnet på ett schema.</span><span class="sxs-lookup"><span data-stu-id="4f6df-158">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="4f6df-159">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4f6df-159">-ServerName</span></span>
<span data-ttu-id="4f6df-160">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="4f6df-160">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="4f6df-161">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="4f6df-161">-SuffixSize</span></span>
<span data-ttu-id="4f6df-162">Anger antalet tecken i slutet av texten som inte maskeras.</span><span class="sxs-lookup"><span data-stu-id="4f6df-162">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="4f6df-163">Ange endast den här parametern om du anger ett text värde för parametern *MaskingFunction* .</span><span class="sxs-lookup"><span data-stu-id="4f6df-163">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="4f6df-164">Standardvärdet är 0.</span><span class="sxs-lookup"><span data-stu-id="4f6df-164">The default value is 0.</span></span>

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

### <span data-ttu-id="4f6df-165">-TableName</span><span class="sxs-lookup"><span data-stu-id="4f6df-165">-TableName</span></span>
<span data-ttu-id="4f6df-166">Anger namnet på den databas tabell som innehåller den maskerade kolumnen.</span><span class="sxs-lookup"><span data-stu-id="4f6df-166">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="4f6df-167">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4f6df-167">-Confirm</span></span>
<span data-ttu-id="4f6df-168">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4f6df-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f6df-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f6df-169">-WhatIf</span></span>
<span data-ttu-id="4f6df-170">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4f6df-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f6df-171">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4f6df-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f6df-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f6df-172">-DefaultProfile</span></span>
<span data-ttu-id="4f6df-173">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4f6df-173">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f6df-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f6df-174">CommonParameters</span></span>
<span data-ttu-id="4f6df-175">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f6df-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f6df-176">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f6df-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f6df-177">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4f6df-177">INPUTS</span></span>

###  
<span data-ttu-id="4f6df-178">Ingen</span><span class="sxs-lookup"><span data-stu-id="4f6df-178">None</span></span>

## <span data-ttu-id="4f6df-179">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4f6df-179">OUTPUTS</span></span>

### <span data-ttu-id="4f6df-180">Microsoft. Azure. commands. SQL. Security. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="4f6df-180">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="4f6df-181">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4f6df-181">NOTES</span></span>

## <span data-ttu-id="4f6df-182">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4f6df-182">RELATED LINKS</span></span>

[<span data-ttu-id="4f6df-183">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="4f6df-183">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="4f6df-184">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="4f6df-184">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="4f6df-185">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="4f6df-185">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="4f6df-186">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="4f6df-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

