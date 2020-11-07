---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: fe8a76ed0851393462ba94937d2ab92914b503b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757017"
---
# <span data-ttu-id="bf334-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="bf334-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="bf334-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bf334-102">SYNOPSIS</span></span>
<span data-ttu-id="bf334-103">Anger en policy för hot identifiering för en databas.</span><span class="sxs-lookup"><span data-stu-id="bf334-103">Sets a threat detection policy on a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf334-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bf334-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf334-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bf334-105">DESCRIPTION</span></span>
<span data-ttu-id="bf334-106">Cmdleten **set-AzureRmSqlDatabaseThreatDetectionPolicy** anger en policy för hot identifiering på en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="bf334-106">The **Set-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL database.</span></span>
<span data-ttu-id="bf334-107">För att aktivera hot identifiering för en databas måste en gransknings princip vara aktive rad för den databasen.</span><span class="sxs-lookup"><span data-stu-id="bf334-107">In order to enable threat detection on a database an auditing policy must be enabled on that database.</span></span>
<span data-ttu-id="bf334-108">Använd den här cmdleten genom att ange parametrarna *ResourceGroupName* , *servername* och *databasename* för att identifiera databasen.</span><span class="sxs-lookup"><span data-stu-id="bf334-108">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="bf334-109">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="bf334-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="bf334-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bf334-110">EXAMPLES</span></span>

### <span data-ttu-id="bf334-111">Exempel 1: ange principen för hot identifiering för en databas</span><span class="sxs-lookup"><span data-stu-id="bf334-111">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="bf334-112">Det här kommandot ställer in policyn för hot identifiering för en databas som heter Database01 på den server som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="bf334-112">This command sets the threat detection policy for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="bf334-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bf334-113">PARAMETERS</span></span>

### <span data-ttu-id="bf334-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bf334-114">-DatabaseName</span></span>
<span data-ttu-id="bf334-115">Anger namnet på den databas där principen är inställd.</span><span class="sxs-lookup"><span data-stu-id="bf334-115">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="bf334-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf334-116">-DefaultProfile</span></span>
<span data-ttu-id="bf334-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bf334-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf334-118">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="bf334-118">-EmailAdmins</span></span>
<span data-ttu-id="bf334-119">Anger om principen för hot identifiering kontaktar administratörer via e-post.</span><span class="sxs-lookup"><span data-stu-id="bf334-119">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

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

### <span data-ttu-id="bf334-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="bf334-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="bf334-121">Anger en matris med identifierings typer som ska undantas från principen.</span><span class="sxs-lookup"><span data-stu-id="bf334-121">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="bf334-122">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="bf334-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bf334-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="bf334-123">Sql_Injection</span></span> 
- <span data-ttu-id="bf334-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="bf334-124">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="bf334-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="bf334-125">Access_Anomaly</span></span> 
- <span data-ttu-id="bf334-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="bf334-126">None</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]
Parameter Sets: (All)
Aliases:
Accepted values: Sql_Injection, Sql_Injection_Vulnerability, Access_Anomaly, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf334-127">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="bf334-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="bf334-128">Anger en semikolonavgränsad lista med e-postadresser som principen skickar aviseringar till.</span><span class="sxs-lookup"><span data-stu-id="bf334-128">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="bf334-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf334-129">-PassThru</span></span>
<span data-ttu-id="bf334-130">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="bf334-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bf334-131">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="bf334-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bf334-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf334-132">-ResourceGroupName</span></span>
<span data-ttu-id="bf334-133">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="bf334-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="bf334-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="bf334-134">-RetentionInDays</span></span>
<span data-ttu-id="bf334-135">Antalet bevarande dagar för gransknings loggar</span><span class="sxs-lookup"><span data-stu-id="bf334-135">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="bf334-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bf334-136">-ServerName</span></span>
<span data-ttu-id="bf334-137">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="bf334-137">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="bf334-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bf334-138">-StorageAccountName</span></span>
<span data-ttu-id="bf334-139">Anger namnet på det lagrings konto som ska användas.</span><span class="sxs-lookup"><span data-stu-id="bf334-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="bf334-140">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="bf334-140">Wildcards are not permitted.</span></span> <span data-ttu-id="bf334-141">Denna parameter är inte obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="bf334-141">This parameter is not required.</span></span> <span data-ttu-id="bf334-142">Om du inte anger den här parametern används det lagrings konto som har definierats tidigare som en del av principen för hot identifiering för databasen.</span><span class="sxs-lookup"><span data-stu-id="bf334-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="bf334-143">Om det är första gången som en policy för identifiering av databas hot har definierats och den här parametern inte anges, Miss lyckas cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bf334-143">If this is the first time a database threat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="bf334-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bf334-144">-Confirm</span></span>
<span data-ttu-id="bf334-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bf334-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf334-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf334-146">-WhatIf</span></span>
<span data-ttu-id="bf334-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bf334-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf334-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bf334-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf334-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf334-149">CommonParameters</span></span>
<span data-ttu-id="bf334-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf334-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf334-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf334-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf334-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bf334-152">INPUTS</span></span>

### <span data-ttu-id="bf334-153">System. String</span><span class="sxs-lookup"><span data-stu-id="bf334-153">System.String</span></span>

### <span data-ttu-id="bf334-154">System. Nullable ' 1 [[system. Boolean, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="bf334-154">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="bf334-155">Microsoft. Azure. commands. SQL. ThreatDetection. Model. DetectionType []</span><span class="sxs-lookup"><span data-stu-id="bf334-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="bf334-156">System. Nullable ' 1 [[system. UInt32, mscorlib, version = 4.0.0.0; Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="bf334-156">System.Nullable\`1[[System.UInt32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="bf334-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bf334-157">OUTPUTS</span></span>

### <span data-ttu-id="bf334-158">Microsoft. Azure. commands. SQL. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="bf334-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="bf334-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bf334-159">NOTES</span></span>

## <span data-ttu-id="bf334-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bf334-160">RELATED LINKS</span></span>

[<span data-ttu-id="bf334-161">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="bf334-161">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="bf334-162">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="bf334-162">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="bf334-163">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="bf334-163">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


