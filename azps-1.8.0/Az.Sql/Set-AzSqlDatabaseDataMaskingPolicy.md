---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: e0af0c6d741e45c2e00e958342fad940acc2c3e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746524"
---
# <span data-ttu-id="38857-101">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="38857-101">Set-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="38857-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="38857-102">SYNOPSIS</span></span>
<span data-ttu-id="38857-103">Anger data maskering för en databas.</span><span class="sxs-lookup"><span data-stu-id="38857-103">Sets data masking for a database.</span></span>

## <span data-ttu-id="38857-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="38857-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedUsers <String>] [-DataMaskingState <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38857-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="38857-105">DESCRIPTION</span></span>
<span data-ttu-id="38857-106">Cmdleten **set-AzSqlDatabaseDataMaskingPolicy** anger data masknings principen för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="38857-106">The **Set-AzSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="38857-107">Använd den här cmdleten genom att använda parametrarna *ResourceGroupName* , *servername* och *databasename* för att identifiera databasen.</span><span class="sxs-lookup"><span data-stu-id="38857-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="38857-108">Du kan ställa in parametern *DataMaskingState* för att ange om data maskning ska aktive ras eller inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="38857-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>
<span data-ttu-id="38857-109">Om cmdleten lyckas och parametern *Passthru* används, returneras ett objekt som beskriver den aktuella data masknings principen utöver databasens identifierare.</span><span class="sxs-lookup"><span data-stu-id="38857-109">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="38857-110">Databas identifierare inkluderar, men är inte begränsade till, **ResourceGroupName** , **servername** och **databasename**.</span><span class="sxs-lookup"><span data-stu-id="38857-110">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="38857-111">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="38857-111">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="38857-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="38857-112">EXAMPLES</span></span>

### <span data-ttu-id="38857-113">Exempel 1: ange data masknings principen för en databas</span><span class="sxs-lookup"><span data-stu-id="38857-113">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="38857-114">Det här kommandot anger data masknings principen för en databas som heter database01 på den server som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="38857-114">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="38857-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="38857-115">PARAMETERS</span></span>

### <span data-ttu-id="38857-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="38857-116">-DatabaseName</span></span>
<span data-ttu-id="38857-117">Anger namnet på den databas där principen är inställd.</span><span class="sxs-lookup"><span data-stu-id="38857-117">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="38857-118">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="38857-118">-DataMaskingState</span></span>
<span data-ttu-id="38857-119">Anger om data maskering är aktiverat eller inaktiverat.</span><span class="sxs-lookup"><span data-stu-id="38857-119">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="38857-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="38857-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="38857-121">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="38857-121">Enabled</span></span>
- <span data-ttu-id="38857-122">Inaktiverat standardvärdet är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="38857-122">Disabled The default value is Enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38857-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38857-123">-DefaultProfile</span></span>
<span data-ttu-id="38857-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="38857-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38857-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38857-125">-PassThru</span></span>
<span data-ttu-id="38857-126">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="38857-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="38857-127">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="38857-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="38857-128">-PrivilegedUsers</span><span class="sxs-lookup"><span data-stu-id="38857-128">-PrivilegedUsers</span></span>
<span data-ttu-id="38857-129">Anger en semikolonavgränsad lista med privilegierade användar-ID.</span><span class="sxs-lookup"><span data-stu-id="38857-129">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="38857-130">De här användarna kan visa masknings data.</span><span class="sxs-lookup"><span data-stu-id="38857-130">These users are allowed to view the masking data.</span></span>

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

### <span data-ttu-id="38857-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38857-131">-ResourceGroupName</span></span>
<span data-ttu-id="38857-132">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="38857-132">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="38857-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="38857-133">-ServerName</span></span>
<span data-ttu-id="38857-134">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="38857-134">Specifies the name of the server hosting the database.</span></span>

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

### <span data-ttu-id="38857-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="38857-135">-Confirm</span></span>
<span data-ttu-id="38857-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="38857-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38857-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38857-137">-WhatIf</span></span>
<span data-ttu-id="38857-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="38857-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38857-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="38857-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38857-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38857-140">CommonParameters</span></span>
<span data-ttu-id="38857-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38857-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38857-142">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38857-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38857-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="38857-143">INPUTS</span></span>

### <span data-ttu-id="38857-144">System. String</span><span class="sxs-lookup"><span data-stu-id="38857-144">System.String</span></span>

## <span data-ttu-id="38857-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="38857-145">OUTPUTS</span></span>

### <span data-ttu-id="38857-146">Microsoft. Azure. commands. SQL. DataMasking. Model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="38857-146">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="38857-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="38857-147">NOTES</span></span>

## <span data-ttu-id="38857-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="38857-148">RELATED LINKS</span></span>

[<span data-ttu-id="38857-149">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="38857-149">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="38857-150">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="38857-150">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="38857-151">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="38857-151">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="38857-152">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="38857-152">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="38857-153">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="38857-153">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="38857-154">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="38857-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


