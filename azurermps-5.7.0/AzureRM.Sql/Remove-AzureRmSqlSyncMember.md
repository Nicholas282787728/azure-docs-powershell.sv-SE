---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncMember.md
ms.openlocfilehash: b96d125b2a4f608c54024619ca6259a136d2ed69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575454"
---
# <span data-ttu-id="c01a4-101">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="c01a4-101">Remove-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="c01a4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c01a4-102">SYNOPSIS</span></span>
<span data-ttu-id="c01a4-103">Tar bort en Azure SQL Database Sync-medlem.</span><span class="sxs-lookup"><span data-stu-id="c01a4-103">Removes an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c01a4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c01a4-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c01a4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c01a4-105">DESCRIPTION</span></span>
<span data-ttu-id="c01a4-106">Cmdleten **Remove-AzureRmSqlSyncMember** tar bort en synkroniserad Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="c01a4-106">The **Remove-AzureRmSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="c01a4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c01a4-107">EXAMPLES</span></span>

### <span data-ttu-id="c01a4-108">Exempel 1: ta bort en synkroniserad medlem</span><span class="sxs-lookup"><span data-stu-id="c01a4-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="c01a4-109">Det här kommandot tar bort synkroniserings medlem för Azure SQL Database med namnet syncMember01.</span><span class="sxs-lookup"><span data-stu-id="c01a4-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="c01a4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c01a4-110">PARAMETERS</span></span>

### <span data-ttu-id="c01a4-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c01a4-111">-DatabaseName</span></span>
<span data-ttu-id="c01a4-112">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="c01a4-112">The name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c01a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c01a4-113">-DefaultProfile</span></span>
<span data-ttu-id="c01a4-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c01a4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c01a4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c01a4-115">-Force</span></span>
<span data-ttu-id="c01a4-116">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="c01a4-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="c01a4-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="c01a4-117">-Name</span></span>
<span data-ttu-id="c01a4-118">Synkroniserat medlems namn.</span><span class="sxs-lookup"><span data-stu-id="c01a4-118">The sync member name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c01a4-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c01a4-119">-PassThru</span></span>
<span data-ttu-id="c01a4-120">Definierar om den borttagna medlemmen ska returneras</span><span class="sxs-lookup"><span data-stu-id="c01a4-120">Defines Whether return the removed sync member</span></span>

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

### <span data-ttu-id="c01a4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c01a4-121">-ResourceGroupName</span></span>
<span data-ttu-id="c01a4-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c01a4-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="c01a4-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c01a4-123">-ServerName</span></span>
<span data-ttu-id="c01a4-124">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c01a4-124">The name of the Azure SQL Server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c01a4-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="c01a4-125">-SyncGroupName</span></span>
<span data-ttu-id="c01a4-126">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="c01a4-126">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c01a4-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c01a4-127">-Confirm</span></span>
<span data-ttu-id="c01a4-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c01a4-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c01a4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c01a4-129">-WhatIf</span></span>
<span data-ttu-id="c01a4-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c01a4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c01a4-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c01a4-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c01a4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c01a4-132">CommonParameters</span></span>
<span data-ttu-id="c01a4-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c01a4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c01a4-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c01a4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c01a4-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c01a4-135">INPUTS</span></span>

### <span data-ttu-id="c01a4-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="c01a4-136">None</span></span>
<span data-ttu-id="c01a4-137">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="c01a4-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c01a4-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c01a4-138">OUTPUTS</span></span>

### <span data-ttu-id="c01a4-139">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="c01a4-139">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="c01a4-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c01a4-140">NOTES</span></span>

## <span data-ttu-id="c01a4-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c01a4-141">RELATED LINKS</span></span>

[<span data-ttu-id="c01a4-142">New-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="c01a4-142">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="c01a4-143">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="c01a4-143">Update-AzureRmSqlSyncMember</span></span>](./Update-AzureRmSqlSyncMember.md)

[<span data-ttu-id="c01a4-144">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="c01a4-144">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

