---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 8480037bf4b756a03a40ad1c1dff01ab1d28ac69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579699"
---
# <span data-ttu-id="1508b-101">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="1508b-101">Set-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="1508b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1508b-102">SYNOPSIS</span></span>
<span data-ttu-id="1508b-103">Ändrar gransknings inställningarna för en Azure SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="1508b-103">Changes the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1508b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1508b-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAuditing -State <String> [-AuditActionGroup <AuditActionGroups[]>] [-PassThru]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1508b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1508b-105">DESCRIPTION</span></span>
<span data-ttu-id="1508b-106">Cmdleten **set-AzureRmSqlServerAuditing** ändrar gransknings inställningarna för en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1508b-106">The **Set-AzureRmSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="1508b-107">Använd cmdleten *ResourceGroupName* och *servername* för att identifiera servern.</span><span class="sxs-lookup"><span data-stu-id="1508b-107">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="1508b-108">Ange *StorageAccountName* -parametern för att ange lagrings konto för gransknings loggar och parametern *StorageKeyType* för att definiera lagrings nycklarna.</span><span class="sxs-lookup"><span data-stu-id="1508b-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="1508b-109">Använd parametern *State* för att aktivera/inaktivera principen.</span><span class="sxs-lookup"><span data-stu-id="1508b-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="1508b-110">Du kan också definiera bevarande för gransknings loggar genom att ange värdet för *RetentionInDays* -parametern för att definiera perioden för gransknings loggar.</span><span class="sxs-lookup"><span data-stu-id="1508b-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="1508b-111">När cmdleten har körts klart är granskning av de Azure SQL-databaser som är definierade i den angivna Azure SQL-servern aktive rad.</span><span class="sxs-lookup"><span data-stu-id="1508b-111">After the cmdlet runs successfully, auditing of the Azure SQL databases that are defined in the specified Azure SQL server is enabled.</span></span>
<span data-ttu-id="1508b-112">Om cmdleten lyckas och du använder parametern *Passthru* returneras ett objekt som beskriver den aktuella BLOB-granskningen utöver Server-ID: n.</span><span class="sxs-lookup"><span data-stu-id="1508b-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the server identifiers.</span></span>
<span data-ttu-id="1508b-113">Server-ID: n inkluderar, men är inte begränsade till, **ResourceGroupName** och **servername**.</span><span class="sxs-lookup"><span data-stu-id="1508b-113">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="1508b-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1508b-114">EXAMPLES</span></span>

### <span data-ttu-id="1508b-115">Exempel 1: Aktivera gransknings principen för en Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="1508b-115">Example 1: Enable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="1508b-116">Exempel 2: inaktivera gransknings principen för en Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="1508b-116">Example 2: Disable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

## <span data-ttu-id="1508b-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1508b-117">PARAMETERS</span></span>

### <span data-ttu-id="1508b-118">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="1508b-118">-AuditActionGroup</span></span>
<span data-ttu-id="1508b-119">Uppsättningen gransknings åtgärds grupper</span><span class="sxs-lookup"><span data-stu-id="1508b-119">The set of the audit action groups</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases: 
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1508b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1508b-120">-PassThru</span></span>
<span data-ttu-id="1508b-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="1508b-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1508b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1508b-122">-ResourceGroupName</span></span>
<span data-ttu-id="1508b-123">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1508b-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="1508b-124">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="1508b-124">-RetentionInDays</span></span>
<span data-ttu-id="1508b-125">Antalet bevarande dagar för gransknings loggar</span><span class="sxs-lookup"><span data-stu-id="1508b-125">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="1508b-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1508b-126">-ServerName</span></span>
<span data-ttu-id="1508b-127">SQL Server-namn.</span><span class="sxs-lookup"><span data-stu-id="1508b-127">SQL server name.</span></span>

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

### <span data-ttu-id="1508b-128">-State</span><span class="sxs-lookup"><span data-stu-id="1508b-128">-State</span></span>
<span data-ttu-id="1508b-129">Tillståndet för gransknings policyn</span><span class="sxs-lookup"><span data-stu-id="1508b-129">The state of the auditing policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1508b-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1508b-130">-StorageAccountName</span></span>
<span data-ttu-id="1508b-131">Namnet på lagrings kontot</span><span class="sxs-lookup"><span data-stu-id="1508b-131">The name of the storage account</span></span>

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

### <span data-ttu-id="1508b-132">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="1508b-132">-StorageKeyType</span></span>
<span data-ttu-id="1508b-133">Typ av lagrings plats</span><span class="sxs-lookup"><span data-stu-id="1508b-133">The type of the storage key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1508b-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1508b-134">-Confirm</span></span>
<span data-ttu-id="1508b-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1508b-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1508b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1508b-136">-WhatIf</span></span>
<span data-ttu-id="1508b-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1508b-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1508b-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1508b-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1508b-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1508b-139">-DefaultProfile</span></span>
<span data-ttu-id="1508b-140">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1508b-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1508b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1508b-141">CommonParameters</span></span>
<span data-ttu-id="1508b-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1508b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1508b-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1508b-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1508b-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1508b-144">INPUTS</span></span>

## <span data-ttu-id="1508b-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1508b-145">OUTPUTS</span></span>

### <span data-ttu-id="1508b-146">Microsoft. Azure. commands. SQL. Security. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="1508b-146">Microsoft.Azure.Commands.Sql.Security.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="1508b-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1508b-147">NOTES</span></span>

## <span data-ttu-id="1508b-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1508b-148">RELATED LINKS</span></span>

