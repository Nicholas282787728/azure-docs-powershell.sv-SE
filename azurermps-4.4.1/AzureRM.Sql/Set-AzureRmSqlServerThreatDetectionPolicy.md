---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 7c71e9390ca28b48127a2f977e04eba645ae962f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586147"
---
# <span data-ttu-id="e5ec5-101">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e5ec5-101">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="e5ec5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e5ec5-102">SYNOPSIS</span></span>
<span data-ttu-id="e5ec5-103">Ställer in en policy för hot identifiering på en server.</span><span class="sxs-lookup"><span data-stu-id="e5ec5-103">Sets a threat detection policy on a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5ec5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e5ec5-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5ec5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e5ec5-105">DESCRIPTION</span></span>
<span data-ttu-id="e5ec5-106">Cmdleten **set-AzureRmSqlServerThreatDetectionPolicy** anger en policy för hot identifiering på en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e5ec5-106">The **Set-AzureRmSqlServerThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL server.</span></span>
<span data-ttu-id="e5ec5-107">För att aktivera hot identifiering på en server måste en gransknings princip vara aktive rad för den servern.</span><span class="sxs-lookup"><span data-stu-id="e5ec5-107">In order to enable threat detection on a server an auditing policy must be enabled on that server.</span></span>
<span data-ttu-id="e5ec5-108">Om du vill använda denna cmdlet anger du parametrarna *ResourceGroupName* och servername för att identifiera servern.</span><span class="sxs-lookup"><span data-stu-id="e5ec5-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="e5ec5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e5ec5-109">EXAMPLES</span></span>

### <span data-ttu-id="e5ec5-110">Exempel 1: ange principen för hot identifiering för en databas</span><span class="sxs-lookup"><span data-stu-id="e5ec5-110">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="e5ec5-111">Det här kommandot ställer in policyn för hot identifiering för en server som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="e5ec5-111">This command sets the threat detection policy for a server named Server01.</span></span>

## <span data-ttu-id="e5ec5-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e5ec5-112">PARAMETERS</span></span>

### <span data-ttu-id="e5ec5-113">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="e5ec5-113">-EmailAdmins</span></span>
<span data-ttu-id="e5ec5-114">Anger om principen för hot identifiering kontaktar administratörer via e-post.</span><span class="sxs-lookup"><span data-stu-id="e5ec5-114">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

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

### <span data-ttu-id="e5ec5-115">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="e5ec5-115">-ExcludedDetectionType</span></span>
<span data-ttu-id="e5ec5-116">Anger en matris med identifierings typer som ska undantas från principen.</span><span class="sxs-lookup"><span data-stu-id="e5ec5-116">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="e5ec5-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e5ec5-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e5ec5-118">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="e5ec5-118">Sql_Injection</span></span>
- <span data-ttu-id="e5ec5-119">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="e5ec5-119">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="e5ec5-120">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="e5ec5-120">Access_Anomaly</span></span>
- <span data-ttu-id="e5ec5-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="e5ec5-121">None</span></span>

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

### <span data-ttu-id="e5ec5-122">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="e5ec5-122">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="e5ec5-123">Anger en semikolonavgränsad lista med e-postadresser som principen skickar aviseringar till.</span><span class="sxs-lookup"><span data-stu-id="e5ec5-123">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="e5ec5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5ec5-124">-PassThru</span></span>
<span data-ttu-id="e5ec5-125">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="e5ec5-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e5ec5-126">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="e5ec5-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e5ec5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5ec5-127">-ResourceGroupName</span></span>
<span data-ttu-id="e5ec5-128">Anger namnet på den resurs grupp som servern tillhör.</span><span class="sxs-lookup"><span data-stu-id="e5ec5-128">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="e5ec5-129">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="e5ec5-129">-RetentionInDays</span></span>
<span data-ttu-id="e5ec5-130">Antalet bevarande dagar för gransknings loggar</span><span class="sxs-lookup"><span data-stu-id="e5ec5-130">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="e5ec5-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e5ec5-131">-ServerName</span></span>
<span data-ttu-id="e5ec5-132">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="e5ec5-132">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="e5ec5-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e5ec5-133">-StorageAccountName</span></span>
<span data-ttu-id="e5ec5-134">Anger namnet på det lagrings konto som ska användas.</span><span class="sxs-lookup"><span data-stu-id="e5ec5-134">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="e5ec5-135">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="e5ec5-135">Wildcards are not permitted.</span></span> <span data-ttu-id="e5ec5-136">Denna parameter är inte obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="e5ec5-136">This parameter is not required.</span></span> <span data-ttu-id="e5ec5-137">Om du inte anger den här parametern används det lagrings konto som har definierats tidigare som en del av principen för hot identifiering för databasen.</span><span class="sxs-lookup"><span data-stu-id="e5ec5-137">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="e5ec5-138">Om det är första gången som en theat för att identifiera en databas har definierats och den här parametern inte är angiven kan cmdleten Miss lyckas.</span><span class="sxs-lookup"><span data-stu-id="e5ec5-138">If this is the first time a database theat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="e5ec5-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e5ec5-139">-Confirm</span></span>
<span data-ttu-id="e5ec5-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e5ec5-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5ec5-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5ec5-141">-WhatIf</span></span>
<span data-ttu-id="e5ec5-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e5ec5-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5ec5-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e5ec5-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5ec5-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5ec5-144">-DefaultProfile</span></span>
<span data-ttu-id="e5ec5-145">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e5ec5-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5ec5-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5ec5-146">CommonParameters</span></span>
<span data-ttu-id="e5ec5-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5ec5-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5ec5-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5ec5-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5ec5-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e5ec5-149">INPUTS</span></span>

###  
<span data-ttu-id="e5ec5-150">Det går inte att pipe in i denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5ec5-150">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="e5ec5-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e5ec5-151">OUTPUTS</span></span>

### <span data-ttu-id="e5ec5-152">Microsoft. Azure. commands. SQL. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="e5ec5-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>
<span data-ttu-id="e5ec5-153">Denna cmdlet returnerar ett **ServerThreatDetectionPolicyModel** -objekt.</span><span class="sxs-lookup"><span data-stu-id="e5ec5-153">This cmdlet returns a **ServerThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="e5ec5-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e5ec5-154">NOTES</span></span>

## <span data-ttu-id="e5ec5-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e5ec5-155">RELATED LINKS</span></span>

[<span data-ttu-id="e5ec5-156">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e5ec5-156">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="e5ec5-157">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e5ec5-157">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[<span data-ttu-id="e5ec5-158">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="e5ec5-158">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
