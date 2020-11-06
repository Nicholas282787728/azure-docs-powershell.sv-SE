---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 40ce06b21be7312598978bbd56b10e4e33915ece
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574147"
---
# <span data-ttu-id="c8a03-101">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c8a03-101">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="c8a03-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c8a03-102">SYNOPSIS</span></span>
<span data-ttu-id="c8a03-103">Ställer in en policy för hot identifiering på en server.</span><span class="sxs-lookup"><span data-stu-id="c8a03-103">Sets a threat detection policy on a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8a03-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c8a03-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8a03-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c8a03-105">DESCRIPTION</span></span>
<span data-ttu-id="c8a03-106">Cmdleten **set-AzureRmSqlServerThreatDetectionPolicy** anger en policy för hot identifiering på en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c8a03-106">The **Set-AzureRmSqlServerThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL server.</span></span>
<span data-ttu-id="c8a03-107">För att aktivera hot identifiering på en server måste en gransknings princip vara aktive rad för den servern.</span><span class="sxs-lookup"><span data-stu-id="c8a03-107">In order to enable threat detection on a server an auditing policy must be enabled on that server.</span></span>
<span data-ttu-id="c8a03-108">Om du vill använda denna cmdlet anger du parametrarna *ResourceGroupName* och servername för att identifiera servern.</span><span class="sxs-lookup"><span data-stu-id="c8a03-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="c8a03-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c8a03-109">EXAMPLES</span></span>

### <span data-ttu-id="c8a03-110">Exempel 1: ange principen för hot identifiering för en databas</span><span class="sxs-lookup"><span data-stu-id="c8a03-110">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="c8a03-111">Det här kommandot ställer in policyn för hot identifiering för en server som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="c8a03-111">This command sets the threat detection policy for a server named Server01.</span></span>

## <span data-ttu-id="c8a03-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c8a03-112">PARAMETERS</span></span>

### <span data-ttu-id="c8a03-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8a03-113">-DefaultProfile</span></span>
<span data-ttu-id="c8a03-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c8a03-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8a03-115">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="c8a03-115">-EmailAdmins</span></span>
<span data-ttu-id="c8a03-116">Anger om principen för hot identifiering kontaktar administratörer via e-post.</span><span class="sxs-lookup"><span data-stu-id="c8a03-116">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a03-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="c8a03-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="c8a03-118">Anger en matris med identifierings typer som ska undantas från principen.</span><span class="sxs-lookup"><span data-stu-id="c8a03-118">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="c8a03-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c8a03-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c8a03-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="c8a03-120">Sql_Injection</span></span>
- <span data-ttu-id="c8a03-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="c8a03-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="c8a03-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="c8a03-122">Access_Anomaly</span></span>
- <span data-ttu-id="c8a03-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="c8a03-123">None</span></span>

```yaml
Type: DetectionType[]
Parameter Sets: (All)
Aliases:
Accepted values: Sql_Injection, Sql_Injection_Vulnerability, Access_Anomaly, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a03-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="c8a03-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="c8a03-125">Anger en semikolonavgränsad lista med e-postadresser som principen skickar aviseringar till.</span><span class="sxs-lookup"><span data-stu-id="c8a03-125">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a03-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8a03-126">-PassThru</span></span>
<span data-ttu-id="c8a03-127">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="c8a03-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c8a03-128">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="c8a03-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8a03-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8a03-129">-ResourceGroupName</span></span>
<span data-ttu-id="c8a03-130">Anger namnet på den resurs grupp som servern tillhör.</span><span class="sxs-lookup"><span data-stu-id="c8a03-130">Specifies the name of the resource group to which the server belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a03-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="c8a03-131">-RetentionInDays</span></span>
<span data-ttu-id="c8a03-132">Antalet bevarande dagar för gransknings loggar</span><span class="sxs-lookup"><span data-stu-id="c8a03-132">The number of retention days for the audit logs</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a03-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c8a03-133">-ServerName</span></span>
<span data-ttu-id="c8a03-134">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="c8a03-134">Specifies the name of the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a03-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c8a03-135">-StorageAccountName</span></span>
<span data-ttu-id="c8a03-136">Anger namnet på det lagrings konto som ska användas.</span><span class="sxs-lookup"><span data-stu-id="c8a03-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="c8a03-137">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="c8a03-137">Wildcards are not permitted.</span></span> <span data-ttu-id="c8a03-138">Denna parameter är inte obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="c8a03-138">This parameter is not required.</span></span> <span data-ttu-id="c8a03-139">Om du inte anger den här parametern används det lagrings konto som har definierats tidigare som en del av principen för hot identifiering för databasen.</span><span class="sxs-lookup"><span data-stu-id="c8a03-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="c8a03-140">Om det är första gången som en theat för att identifiera en databas har definierats och den här parametern inte är angiven kan cmdleten Miss lyckas.</span><span class="sxs-lookup"><span data-stu-id="c8a03-140">If this is the first time a database theat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a03-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c8a03-141">-Confirm</span></span>
<span data-ttu-id="c8a03-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c8a03-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8a03-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8a03-143">-WhatIf</span></span>
<span data-ttu-id="c8a03-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c8a03-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8a03-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c8a03-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8a03-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8a03-146">CommonParameters</span></span>
<span data-ttu-id="c8a03-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8a03-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8a03-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8a03-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8a03-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c8a03-149">INPUTS</span></span>

###  
<span data-ttu-id="c8a03-150">Det går inte att pipe in i denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8a03-150">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="c8a03-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c8a03-151">OUTPUTS</span></span>

### <span data-ttu-id="c8a03-152">Microsoft. Azure. commands. SQL. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="c8a03-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>
<span data-ttu-id="c8a03-153">Denna cmdlet returnerar ett **ServerThreatDetectionPolicyModel** -objekt.</span><span class="sxs-lookup"><span data-stu-id="c8a03-153">This cmdlet returns a **ServerThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="c8a03-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c8a03-154">NOTES</span></span>

## <span data-ttu-id="c8a03-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c8a03-155">RELATED LINKS</span></span>

[<span data-ttu-id="c8a03-156">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c8a03-156">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="c8a03-157">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c8a03-157">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[<span data-ttu-id="c8a03-158">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="c8a03-158">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
