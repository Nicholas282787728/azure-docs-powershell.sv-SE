---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 8d58085aa55958e6e0fc9658d814d4bc05006fd6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746473"
---
# <span data-ttu-id="33ba0-101">Set-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="33ba0-101">Set-AzSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="33ba0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="33ba0-102">SYNOPSIS</span></span>
<span data-ttu-id="33ba0-103">Ställer in en policy för hot identifiering på en server.</span><span class="sxs-lookup"><span data-stu-id="33ba0-103">Sets a threat detection policy on a server.</span></span>

## <span data-ttu-id="33ba0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="33ba0-104">SYNTAX</span></span>

```
Set-AzSqlServerThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33ba0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="33ba0-105">DESCRIPTION</span></span>
<span data-ttu-id="33ba0-106">Cmdleten **set-AzSqlServerThreatDetectionPolicy** anger en policy för hot identifiering på en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="33ba0-106">The **Set-AzSqlServerThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL server.</span></span>
<span data-ttu-id="33ba0-107">För att aktivera hot identifiering på en server måste en gransknings princip vara aktive rad för den servern.</span><span class="sxs-lookup"><span data-stu-id="33ba0-107">In order to enable threat detection on a server an auditing policy must be enabled on that server.</span></span>
<span data-ttu-id="33ba0-108">Om du vill använda denna cmdlet anger du parametrarna *ResourceGroupName* och servername för att identifiera servern.</span><span class="sxs-lookup"><span data-stu-id="33ba0-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="33ba0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="33ba0-109">EXAMPLES</span></span>

### <span data-ttu-id="33ba0-110">Exempel 1: ange principen för hot identifiering för en databas</span><span class="sxs-lookup"><span data-stu-id="33ba0-110">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="33ba0-111">Det här kommandot ställer in policyn för hot identifiering för en server som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="33ba0-111">This command sets the threat detection policy for a server named Server01.</span></span>

## <span data-ttu-id="33ba0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="33ba0-112">PARAMETERS</span></span>

### <span data-ttu-id="33ba0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33ba0-113">-DefaultProfile</span></span>
<span data-ttu-id="33ba0-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="33ba0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33ba0-115">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="33ba0-115">-EmailAdmins</span></span>
<span data-ttu-id="33ba0-116">Anger om principen för hot identifiering kontaktar administratörer via e-post.</span><span class="sxs-lookup"><span data-stu-id="33ba0-116">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

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

### <span data-ttu-id="33ba0-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="33ba0-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="33ba0-118">Anger en matris med identifierings typer som ska undantas från principen.</span><span class="sxs-lookup"><span data-stu-id="33ba0-118">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="33ba0-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="33ba0-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="33ba0-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="33ba0-120">Sql_Injection</span></span>
- <span data-ttu-id="33ba0-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="33ba0-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="33ba0-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="33ba0-122">Access_Anomaly</span></span>
- <span data-ttu-id="33ba0-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="33ba0-123">None</span></span>

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

### <span data-ttu-id="33ba0-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="33ba0-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="33ba0-125">Anger en semikolonavgränsad lista med e-postadresser som principen skickar aviseringar till.</span><span class="sxs-lookup"><span data-stu-id="33ba0-125">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="33ba0-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33ba0-126">-PassThru</span></span>
<span data-ttu-id="33ba0-127">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="33ba0-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="33ba0-128">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="33ba0-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="33ba0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33ba0-129">-ResourceGroupName</span></span>
<span data-ttu-id="33ba0-130">Anger namnet på den resurs grupp som servern tillhör.</span><span class="sxs-lookup"><span data-stu-id="33ba0-130">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="33ba0-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="33ba0-131">-RetentionInDays</span></span>
<span data-ttu-id="33ba0-132">Antalet bevarande dagar för gransknings loggar</span><span class="sxs-lookup"><span data-stu-id="33ba0-132">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="33ba0-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="33ba0-133">-ServerName</span></span>
<span data-ttu-id="33ba0-134">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="33ba0-134">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="33ba0-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="33ba0-135">-StorageAccountName</span></span>
<span data-ttu-id="33ba0-136">Anger namnet på det lagrings konto som ska användas.</span><span class="sxs-lookup"><span data-stu-id="33ba0-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="33ba0-137">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="33ba0-137">Wildcards are not permitted.</span></span> <span data-ttu-id="33ba0-138">Denna parameter är inte obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="33ba0-138">This parameter is not required.</span></span> <span data-ttu-id="33ba0-139">Om du inte anger den här parametern används det lagrings konto som har definierats tidigare som en del av principen för hot identifiering för databasen.</span><span class="sxs-lookup"><span data-stu-id="33ba0-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="33ba0-140">Om det är första gången som en theat för att identifiera en databas har definierats och den här parametern inte är angiven kan cmdleten Miss lyckas.</span><span class="sxs-lookup"><span data-stu-id="33ba0-140">If this is the first time a database theat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="33ba0-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="33ba0-141">-Confirm</span></span>
<span data-ttu-id="33ba0-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="33ba0-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33ba0-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33ba0-143">-WhatIf</span></span>
<span data-ttu-id="33ba0-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="33ba0-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33ba0-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="33ba0-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33ba0-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33ba0-146">CommonParameters</span></span>
<span data-ttu-id="33ba0-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33ba0-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33ba0-148">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33ba0-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33ba0-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="33ba0-149">INPUTS</span></span>

### <span data-ttu-id="33ba0-150">System. String</span><span class="sxs-lookup"><span data-stu-id="33ba0-150">System.String</span></span>

### <span data-ttu-id="33ba0-151">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="33ba0-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="33ba0-152">Microsoft. Azure. commands. SQL. ThreatDetection. Model. DetectionType []</span><span class="sxs-lookup"><span data-stu-id="33ba0-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="33ba0-153">System. Nullable ' 1 [[system. UInt32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="33ba0-153">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="33ba0-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="33ba0-154">OUTPUTS</span></span>

### <span data-ttu-id="33ba0-155">Microsoft. Azure. commands. SQL. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="33ba0-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="33ba0-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="33ba0-156">NOTES</span></span>

## <span data-ttu-id="33ba0-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="33ba0-157">RELATED LINKS</span></span>

[<span data-ttu-id="33ba0-158">Get-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="33ba0-158">Get-AzSqlServerThreatDetectionPolicy</span></span>](./Get-AzSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="33ba0-159">Remove-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="33ba0-159">Remove-AzSqlServerThreatDetectionPolicy</span></span>](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[<span data-ttu-id="33ba0-160">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="33ba0-160">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)