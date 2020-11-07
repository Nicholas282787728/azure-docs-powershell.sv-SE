---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 72ee5f7bd636747b4321e1c87b78fdb37ed84dc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755905"
---
# <span data-ttu-id="2c629-101">Set-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="2c629-101">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="2c629-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2c629-102">SYNOPSIS</span></span>
<span data-ttu-id="2c629-103">Anger data maskering för en databas.</span><span class="sxs-lookup"><span data-stu-id="2c629-103">Sets data masking for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c629-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2c629-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedLogins <String>] [-PrivilegedUsers <String>]
 [-DataMaskingState <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c629-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2c629-105">DESCRIPTION</span></span>
<span data-ttu-id="2c629-106">Cmdleten **set-AzureRmSqlDatabaseDataMaskingPolicy** anger data masknings principen för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="2c629-106">The **Set-AzureRmSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="2c629-107">Använd den här cmdleten genom att använda parametrarna *ResourceGroupName* , *servername* och *databasename* för att identifiera databasen.</span><span class="sxs-lookup"><span data-stu-id="2c629-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="2c629-108">Du kan ställa in parametern *DataMaskingState* för att ange om data maskning ska aktive ras eller inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="2c629-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>

<span data-ttu-id="2c629-109">Du kan också ange vilka användare som får visa de nedaskerade data genom att ange parametern *PrivilegedLogins* .</span><span class="sxs-lookup"><span data-stu-id="2c629-109">You can also set the *PrivilegedLogins* parameter to specify which users are allowed to see the unmasked data.</span></span>
<span data-ttu-id="2c629-110">Om cmdleten lyckas och parametern *Passthru* används, returneras ett objekt som beskriver den aktuella data masknings principen utöver databasens identifierare.</span><span class="sxs-lookup"><span data-stu-id="2c629-110">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="2c629-111">Databas identifierare inkluderar, men är inte begränsade till, **ResourceGroupName** , **servername** och **databasename**.</span><span class="sxs-lookup"><span data-stu-id="2c629-111">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

<span data-ttu-id="2c629-112">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="2c629-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="2c629-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2c629-113">EXAMPLES</span></span>

### <span data-ttu-id="2c629-114">Exempel 1: ange data masknings principen för en databas</span><span class="sxs-lookup"><span data-stu-id="2c629-114">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="2c629-115">Det här kommandot anger data masknings principen för en databas som heter database01 på den server som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="2c629-115">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="2c629-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2c629-116">PARAMETERS</span></span>

### <span data-ttu-id="2c629-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2c629-117">-DatabaseName</span></span>
<span data-ttu-id="2c629-118">Anger namnet på den databas där principen är inställd.</span><span class="sxs-lookup"><span data-stu-id="2c629-118">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="2c629-119">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="2c629-119">-DataMaskingState</span></span>
<span data-ttu-id="2c629-120">Anger om data maskering är aktiverat eller inaktiverat.</span><span class="sxs-lookup"><span data-stu-id="2c629-120">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="2c629-121">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="2c629-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2c629-122">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="2c629-122">Enabled</span></span>
- <span data-ttu-id="2c629-123">Aktiv</span><span class="sxs-lookup"><span data-stu-id="2c629-123">Disabled</span></span>

<span data-ttu-id="2c629-124">Standardvärdet är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="2c629-124">The default value is Enabled.</span></span>

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

### <span data-ttu-id="2c629-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c629-125">-PassThru</span></span>
<span data-ttu-id="2c629-126">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="2c629-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2c629-127">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="2c629-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2c629-128">-PrivilegedLogins</span><span class="sxs-lookup"><span data-stu-id="2c629-128">-PrivilegedLogins</span></span>
<span data-ttu-id="2c629-129">Anger vilka SQL-användare som undantas från maskering.</span><span class="sxs-lookup"><span data-stu-id="2c629-129">Specifies which SQL users are excluded from masking.</span></span>

<span data-ttu-id="2c629-130">Denna parameter är föråldrad och kommer att tas bort från framtida versioner.</span><span class="sxs-lookup"><span data-stu-id="2c629-130">This parameter is deprecated and will be removed from future releases.</span></span>

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

### <span data-ttu-id="2c629-131">-PrivilegedUsers</span><span class="sxs-lookup"><span data-stu-id="2c629-131">-PrivilegedUsers</span></span>
<span data-ttu-id="2c629-132">Anger en semikolonavgränsad lista med privilegierade användar-ID.</span><span class="sxs-lookup"><span data-stu-id="2c629-132">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="2c629-133">De här användarna kan visa masknings data.</span><span class="sxs-lookup"><span data-stu-id="2c629-133">These users are allowed to view the masking data.</span></span>

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

### <span data-ttu-id="2c629-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c629-134">-ResourceGroupName</span></span>
<span data-ttu-id="2c629-135">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="2c629-135">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="2c629-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2c629-136">-ServerName</span></span>
<span data-ttu-id="2c629-137">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="2c629-137">Specifies the name of the server hosting the database.</span></span>

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

### <span data-ttu-id="2c629-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2c629-138">-Confirm</span></span>
<span data-ttu-id="2c629-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2c629-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c629-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c629-140">-WhatIf</span></span>
<span data-ttu-id="2c629-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2c629-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c629-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2c629-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c629-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c629-143">-DefaultProfile</span></span>
<span data-ttu-id="2c629-144">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2c629-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c629-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c629-145">CommonParameters</span></span>
<span data-ttu-id="2c629-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c629-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c629-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c629-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c629-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2c629-148">INPUTS</span></span>

## <span data-ttu-id="2c629-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2c629-149">OUTPUTS</span></span>

### <span data-ttu-id="2c629-150">Microsoft. Azure. commands. SQL. Security. Model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="2c629-150">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="2c629-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2c629-151">NOTES</span></span>

## <span data-ttu-id="2c629-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2c629-152">RELATED LINKS</span></span>

[<span data-ttu-id="2c629-153">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="2c629-153">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="2c629-154">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="2c629-154">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="2c629-155">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="2c629-155">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="2c629-156">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="2c629-156">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="2c629-157">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="2c629-157">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="2c629-158">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="2c629-158">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


