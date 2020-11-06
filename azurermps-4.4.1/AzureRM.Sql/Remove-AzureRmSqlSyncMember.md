---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncMember.md
ms.openlocfilehash: d57e73c71e95fe673f9b54d9129714ca22670d31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586156"
---
# <span data-ttu-id="1f135-101">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="1f135-101">Remove-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="1f135-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1f135-102">SYNOPSIS</span></span>
<span data-ttu-id="1f135-103">Tar bort en Azure SQL Database Sync-medlem.</span><span class="sxs-lookup"><span data-stu-id="1f135-103">Removes an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f135-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1f135-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f135-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1f135-105">DESCRIPTION</span></span>
<span data-ttu-id="1f135-106">Cmdleten **Remove-AzureRmSqlSyncMember** tar bort en synkroniserad Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="1f135-106">The **Remove-AzureRmSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="1f135-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1f135-107">EXAMPLES</span></span>

### <span data-ttu-id="1f135-108">Exempel 1: ta bort en synkroniserad medlem</span><span class="sxs-lookup"><span data-stu-id="1f135-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="1f135-109">Det här kommandot tar bort synkroniserings medlem för Azure SQL Database med namnet syncMember01.</span><span class="sxs-lookup"><span data-stu-id="1f135-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="1f135-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1f135-110">PARAMETERS</span></span>

### <span data-ttu-id="1f135-111">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1f135-111">-Confirm</span></span>
<span data-ttu-id="1f135-112">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1f135-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f135-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1f135-113">-DatabaseName</span></span>
<span data-ttu-id="1f135-114">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="1f135-114">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="1f135-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1f135-115">-Force</span></span>
<span data-ttu-id="1f135-116">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="1f135-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="1f135-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="1f135-117">-Name</span></span>
<span data-ttu-id="1f135-118">Synkroniserat medlems namn.</span><span class="sxs-lookup"><span data-stu-id="1f135-118">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f135-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f135-119">-PassThru</span></span>
<span data-ttu-id="1f135-120">Definierar om den borttagna medlemmen ska returneras</span><span class="sxs-lookup"><span data-stu-id="1f135-120">Defines Whether return the removed sync member</span></span>

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

### <span data-ttu-id="1f135-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f135-121">-ResourceGroupName</span></span>
<span data-ttu-id="1f135-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1f135-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="1f135-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1f135-123">-ServerName</span></span>
<span data-ttu-id="1f135-124">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1f135-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="1f135-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="1f135-125">-SyncGroupName</span></span>
<span data-ttu-id="1f135-126">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="1f135-126">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f135-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f135-127">-WhatIf</span></span>
<span data-ttu-id="1f135-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1f135-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f135-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1f135-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f135-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f135-130">-DefaultProfile</span></span>
<span data-ttu-id="1f135-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1f135-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f135-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f135-132">CommonParameters</span></span>
<span data-ttu-id="1f135-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f135-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f135-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f135-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f135-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1f135-135">INPUTS</span></span>

## <span data-ttu-id="1f135-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1f135-136">OUTPUTS</span></span>

### <span data-ttu-id="1f135-137">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="1f135-137">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="1f135-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1f135-138">NOTES</span></span>

## <span data-ttu-id="1f135-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1f135-139">RELATED LINKS</span></span>

[<span data-ttu-id="1f135-140">New-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="1f135-140">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="1f135-141">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="1f135-141">Update-AzureRmSqlSyncMember</span></span>](./Update-AzureRmSqlSyncMember.md)

[<span data-ttu-id="1f135-142">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="1f135-142">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

