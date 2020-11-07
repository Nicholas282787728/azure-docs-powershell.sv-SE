---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 3ec370f0e4865ed5695e4f0890f99b50709e9ad8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927025"
---
# <span data-ttu-id="7042c-101">Update-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="7042c-101">Update-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="7042c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7042c-102">SYNOPSIS</span></span>
<span data-ttu-id="7042c-103">Anger ett avancerat skydd på en server.</span><span class="sxs-lookup"><span data-stu-id="7042c-103">Sets a advanced threat protection settings on a server.</span></span>

## <span data-ttu-id="7042c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7042c-104">SYNTAX</span></span>

```
Update-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7042c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7042c-105">DESCRIPTION</span></span>
<span data-ttu-id="7042c-106">Cmdleten **Update-AzSqlServerAdvancedThreatProtectionSetting** anger ett avancerat skydds inställningar på en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7042c-106">The **Update-AzSqlServerAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure SQL server.</span></span>
<span data-ttu-id="7042c-107">För att aktivera avancerat skydd för en server måste gransknings inställningar vara aktiverade på den servern.</span><span class="sxs-lookup"><span data-stu-id="7042c-107">In order to enable advanced threat protection on a server an auditing settings must be enabled on that server.</span></span>
<span data-ttu-id="7042c-108">Om du vill använda denna cmdlet anger du parametrarna *ResourceGroupName* och servername för att identifiera servern.</span><span class="sxs-lookup"><span data-stu-id="7042c-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="7042c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7042c-109">EXAMPLES</span></span>

### <span data-ttu-id="7042c-110">Exempel 1: Ange inställningar för avancerat skydd för en databas</span><span class="sxs-lookup"><span data-stu-id="7042c-110">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="7042c-111">Det här kommandot anger de avancerade inställningarna för skydd mot en server med namnet Server01.</span><span class="sxs-lookup"><span data-stu-id="7042c-111">This command sets the advanced threat protection settings for a server named Server01.</span></span>

## <span data-ttu-id="7042c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7042c-112">PARAMETERS</span></span>

### <span data-ttu-id="7042c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7042c-113">-DefaultProfile</span></span>
<span data-ttu-id="7042c-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7042c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7042c-115">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="7042c-115">-EmailAdmins</span></span>
<span data-ttu-id="7042c-116">Anger om avancerade inställningar för skydd mot kontakter kontaktar administratörer via e-post.</span><span class="sxs-lookup"><span data-stu-id="7042c-116">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

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

### <span data-ttu-id="7042c-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="7042c-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="7042c-118">Anger en matris med identifierings typer som ska undantas från inställningarna.</span><span class="sxs-lookup"><span data-stu-id="7042c-118">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="7042c-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="7042c-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7042c-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="7042c-120">Sql_Injection</span></span>
- <span data-ttu-id="7042c-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="7042c-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="7042c-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="7042c-122">Access_Anomaly</span></span>
- <span data-ttu-id="7042c-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="7042c-123">None</span></span>

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

### <span data-ttu-id="7042c-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="7042c-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="7042c-125">Anger en semikolonavgränsad lista med e-postadresser som inställningarna skickar aviseringar till.</span><span class="sxs-lookup"><span data-stu-id="7042c-125">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="7042c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7042c-126">-PassThru</span></span>
<span data-ttu-id="7042c-127">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="7042c-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7042c-128">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="7042c-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7042c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7042c-129">-ResourceGroupName</span></span>
<span data-ttu-id="7042c-130">Anger namnet på den resurs grupp som servern tillhör.</span><span class="sxs-lookup"><span data-stu-id="7042c-130">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="7042c-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="7042c-131">-RetentionInDays</span></span>
<span data-ttu-id="7042c-132">Antalet bevarande dagar för gransknings loggar</span><span class="sxs-lookup"><span data-stu-id="7042c-132">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="7042c-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7042c-133">-ServerName</span></span>
<span data-ttu-id="7042c-134">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="7042c-134">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="7042c-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7042c-135">-StorageAccountName</span></span>
<span data-ttu-id="7042c-136">Anger namnet på det lagrings konto som ska användas.</span><span class="sxs-lookup"><span data-stu-id="7042c-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="7042c-137">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="7042c-137">Wildcards are not permitted.</span></span> <span data-ttu-id="7042c-138">Denna parameter är inte obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="7042c-138">This parameter is not required.</span></span> <span data-ttu-id="7042c-139">Om du inte anger den här parametern används det lagrings konto som har definierats tidigare som en del av databasens avancerade skydds inställningar.</span><span class="sxs-lookup"><span data-stu-id="7042c-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="7042c-140">Om det är första gången som en identifiering av databas hotet har definierats och den här parametern inte anges, Miss lyckas cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7042c-140">If this is the first time a database threat detection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="7042c-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7042c-141">-Confirm</span></span>
<span data-ttu-id="7042c-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7042c-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7042c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7042c-143">-WhatIf</span></span>
<span data-ttu-id="7042c-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7042c-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7042c-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7042c-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7042c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7042c-146">CommonParameters</span></span>
<span data-ttu-id="7042c-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7042c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7042c-148">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7042c-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7042c-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7042c-149">INPUTS</span></span>

### <span data-ttu-id="7042c-150">System. String</span><span class="sxs-lookup"><span data-stu-id="7042c-150">System.String</span></span>

### <span data-ttu-id="7042c-151">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7042c-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7042c-152">Microsoft. Azure. commands. SQL. ThreatDetection. Model. DetectionType []</span><span class="sxs-lookup"><span data-stu-id="7042c-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="7042c-153">System. Nullable ' 1 [[system. UInt32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7042c-153">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7042c-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7042c-154">OUTPUTS</span></span>

### <span data-ttu-id="7042c-155">Microsoft. Azure. commands. SQL. ThreatDetection. Model. ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="7042c-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="7042c-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7042c-156">NOTES</span></span>

## <span data-ttu-id="7042c-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7042c-157">RELATED LINKS</span></span>

[<span data-ttu-id="7042c-158">Get-AzSqlServerThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="7042c-158">Get-AzSqlServerThreatDetectionsettings</span></span>](./Get-AzSqlServerThreatDetectionsettings.md)

[<span data-ttu-id="7042c-159">Remove-AzSqlServerThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="7042c-159">Remove-AzSqlServerThreatDetectionsettings</span></span>](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[<span data-ttu-id="7042c-160">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="7042c-160">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
