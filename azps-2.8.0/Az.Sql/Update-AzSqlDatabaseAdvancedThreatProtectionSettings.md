---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlDatabaseAdvancedThreatProtectionSettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSettings.md
ms.openlocfilehash: 2bbbe4e2b553055e4643cff973941095e0a468f1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920726"
---
# <span data-ttu-id="805a8-101">Update-AzSqlDatabaseAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="805a8-101">Update-AzSqlDatabaseAdvancedThreatProtectionSettings</span></span>

## <span data-ttu-id="805a8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="805a8-102">SYNOPSIS</span></span>
<span data-ttu-id="805a8-103">Anger ett avancerat skydds inställningar för en databas.</span><span class="sxs-lookup"><span data-stu-id="805a8-103">Sets a advanced threat protection settings on a database.</span></span>

## <span data-ttu-id="805a8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="805a8-104">SYNTAX</span></span>

```
Update-AzSqlDatabaseAdvancedThreatProtectionSettings [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="805a8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="805a8-105">DESCRIPTION</span></span>
<span data-ttu-id="805a8-106">Cmdleten **Update-AzSqlDatabaseAdvancedThreatProtectionSettings** anger ett avancerat skydds inställningar för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="805a8-106">The **Update-AzSqlDatabaseAdvancedThreatProtectionSettings** cmdlet sets a advanced threat protection settings on an Azure SQL database.</span></span>
<span data-ttu-id="805a8-107">För att aktivera avancerat skydd för en databas måste gransknings inställningar aktive ras för databasen.</span><span class="sxs-lookup"><span data-stu-id="805a8-107">In order to enable advanced threat protection on a database an auditing settings must be enabled on that database.</span></span>
<span data-ttu-id="805a8-108">Använd den här cmdleten genom att ange parametrarna *ResourceGroupName* , *servername* och *databasename* för att identifiera databasen.</span><span class="sxs-lookup"><span data-stu-id="805a8-108">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="805a8-109">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="805a8-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="805a8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="805a8-110">EXAMPLES</span></span>

### <span data-ttu-id="805a8-111">Exempel 1: Ange inställningar för avancerat skydd för en databas</span><span class="sxs-lookup"><span data-stu-id="805a8-111">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="805a8-112">Det här kommandot anger de avancerade inställningarna för skydd mot en databas som heter Database01 på den server som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="805a8-112">This command sets the advanced threat protection settings for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="805a8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="805a8-113">PARAMETERS</span></span>

### <span data-ttu-id="805a8-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="805a8-114">-DatabaseName</span></span>
<span data-ttu-id="805a8-115">Anger namnet på den databas där inställningarna är inställda.</span><span class="sxs-lookup"><span data-stu-id="805a8-115">Specifies the name of the database where the settings is set.</span></span>

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

### <span data-ttu-id="805a8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="805a8-116">-DefaultProfile</span></span>
<span data-ttu-id="805a8-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="805a8-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="805a8-118">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="805a8-118">-EmailAdmins</span></span>
<span data-ttu-id="805a8-119">Anger om avancerade inställningar för skydd mot kontakter kontaktar administratörer via e-post.</span><span class="sxs-lookup"><span data-stu-id="805a8-119">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="805a8-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="805a8-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="805a8-121">Anger en matris med identifierings typer som ska undantas från inställningarna.</span><span class="sxs-lookup"><span data-stu-id="805a8-121">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="805a8-122">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="805a8-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="805a8-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="805a8-123">Sql_Injection</span></span> 
- <span data-ttu-id="805a8-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="805a8-124">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="805a8-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="805a8-125">Access_Anomaly</span></span> 
- <span data-ttu-id="805a8-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="805a8-126">None</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="805a8-127">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="805a8-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="805a8-128">Anger en semikolonavgränsad lista med e-postadresser som inställningarna skickar aviseringar till.</span><span class="sxs-lookup"><span data-stu-id="805a8-128">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="805a8-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="805a8-129">-PassThru</span></span>
<span data-ttu-id="805a8-130">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="805a8-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="805a8-131">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="805a8-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="805a8-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="805a8-132">-ResourceGroupName</span></span>
<span data-ttu-id="805a8-133">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="805a8-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="805a8-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="805a8-134">-RetentionInDays</span></span>
<span data-ttu-id="805a8-135">Antalet bevarande dagar för gransknings loggar</span><span class="sxs-lookup"><span data-stu-id="805a8-135">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="805a8-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="805a8-136">-ServerName</span></span>
<span data-ttu-id="805a8-137">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="805a8-137">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="805a8-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="805a8-138">-StorageAccountName</span></span>
<span data-ttu-id="805a8-139">Anger namnet på det lagrings konto som ska användas.</span><span class="sxs-lookup"><span data-stu-id="805a8-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="805a8-140">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="805a8-140">Wildcards are not permitted.</span></span> <span data-ttu-id="805a8-141">Denna parameter är inte obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="805a8-141">This parameter is not required.</span></span> <span data-ttu-id="805a8-142">Om du inte anger den här parametern används det lagrings konto som har definierats tidigare som en del av databasens avancerade skydds inställningar.</span><span class="sxs-lookup"><span data-stu-id="805a8-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="805a8-143">Om det är första gången som en avancerad inställning för databasens avancerade skydds inställningar är definierad och den här parametern inte anges, Miss lyckas cmdleten.</span><span class="sxs-lookup"><span data-stu-id="805a8-143">If this is the first time a database advanced threat protection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="805a8-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="805a8-144">-Confirm</span></span>
<span data-ttu-id="805a8-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="805a8-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="805a8-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="805a8-146">-WhatIf</span></span>
<span data-ttu-id="805a8-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="805a8-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="805a8-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="805a8-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="805a8-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="805a8-149">CommonParameters</span></span>
<span data-ttu-id="805a8-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="805a8-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="805a8-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="805a8-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="805a8-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="805a8-152">INPUTS</span></span>

### <span data-ttu-id="805a8-153">System. String</span><span class="sxs-lookup"><span data-stu-id="805a8-153">System.String</span></span>

### <span data-ttu-id="805a8-154">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="805a8-154">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="805a8-155">Microsoft. Azure. commands. SQL. ThreatDetection. Model. DetectionType []</span><span class="sxs-lookup"><span data-stu-id="805a8-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="805a8-156">System. Nullable ' 1 [[system. UInt32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="805a8-156">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="805a8-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="805a8-157">OUTPUTS</span></span>

### <span data-ttu-id="805a8-158">Microsoft. Azure. commands. SQL. ThreatDetection. Model. DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="805a8-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="805a8-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="805a8-159">NOTES</span></span>

## <span data-ttu-id="805a8-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="805a8-160">RELATED LINKS</span></span>

[<span data-ttu-id="805a8-161">Get-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="805a8-161">Get-AzSqlDatabaseThreatDetectionsettings</span></span>](./Get-AzSqlServerThreatDetectionsettings.md)

[<span data-ttu-id="805a8-162">Remove-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="805a8-162">Remove-AzSqlDatabaseThreatDetectionsettings</span></span>](./Remove-AzSqlDatabaseThreatDetectionsettings.md)

[<span data-ttu-id="805a8-163">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="805a8-163">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


