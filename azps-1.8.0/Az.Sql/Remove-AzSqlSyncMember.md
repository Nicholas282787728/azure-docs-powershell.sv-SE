---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
ms.openlocfilehash: 34db2f2307d60f1653b0a806350d96fa9e3380af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746544"
---
# <span data-ttu-id="2f36c-101">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="2f36c-101">Remove-AzSqlSyncMember</span></span>

## <span data-ttu-id="2f36c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2f36c-102">SYNOPSIS</span></span>
<span data-ttu-id="2f36c-103">Tar bort en Azure SQL Database Sync-medlem.</span><span class="sxs-lookup"><span data-stu-id="2f36c-103">Removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="2f36c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2f36c-104">SYNTAX</span></span>

```
Remove-AzSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f36c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2f36c-105">DESCRIPTION</span></span>
<span data-ttu-id="2f36c-106">Cmdleten **Remove-AzSqlSyncMember** tar bort en synkroniserad Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="2f36c-106">The **Remove-AzSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="2f36c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2f36c-107">EXAMPLES</span></span>

### <span data-ttu-id="2f36c-108">Exempel 1: ta bort en synkroniserad medlem</span><span class="sxs-lookup"><span data-stu-id="2f36c-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="2f36c-109">Det här kommandot tar bort synkroniserings medlem för Azure SQL Database med namnet syncMember01.</span><span class="sxs-lookup"><span data-stu-id="2f36c-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="2f36c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2f36c-110">PARAMETERS</span></span>

### <span data-ttu-id="2f36c-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2f36c-111">-DatabaseName</span></span>
<span data-ttu-id="2f36c-112">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="2f36c-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="2f36c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f36c-113">-DefaultProfile</span></span>
<span data-ttu-id="2f36c-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2f36c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f36c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2f36c-115">-Force</span></span>
<span data-ttu-id="2f36c-116">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="2f36c-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="2f36c-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="2f36c-117">-Name</span></span>
<span data-ttu-id="2f36c-118">Synkroniserat medlems namn.</span><span class="sxs-lookup"><span data-stu-id="2f36c-118">The sync member name.</span></span>

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

### <span data-ttu-id="2f36c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f36c-119">-PassThru</span></span>
<span data-ttu-id="2f36c-120">Definierar om den borttagna medlemmen ska returneras</span><span class="sxs-lookup"><span data-stu-id="2f36c-120">Defines Whether return the removed sync member</span></span>

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

### <span data-ttu-id="2f36c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f36c-121">-ResourceGroupName</span></span>
<span data-ttu-id="2f36c-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2f36c-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="2f36c-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2f36c-123">-ServerName</span></span>
<span data-ttu-id="2f36c-124">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2f36c-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="2f36c-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="2f36c-125">-SyncGroupName</span></span>
<span data-ttu-id="2f36c-126">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="2f36c-126">The sync group name.</span></span>

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

### <span data-ttu-id="2f36c-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2f36c-127">-Confirm</span></span>
<span data-ttu-id="2f36c-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2f36c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f36c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f36c-129">-WhatIf</span></span>
<span data-ttu-id="2f36c-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2f36c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f36c-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2f36c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f36c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f36c-132">CommonParameters</span></span>
<span data-ttu-id="2f36c-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f36c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f36c-134">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f36c-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f36c-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2f36c-135">INPUTS</span></span>

### <span data-ttu-id="2f36c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2f36c-136">System.String</span></span>

## <span data-ttu-id="2f36c-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2f36c-137">OUTPUTS</span></span>

### <span data-ttu-id="2f36c-138">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="2f36c-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="2f36c-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2f36c-139">NOTES</span></span>

## <span data-ttu-id="2f36c-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2f36c-140">RELATED LINKS</span></span>

[<span data-ttu-id="2f36c-141">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="2f36c-141">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="2f36c-142">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="2f36c-142">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="2f36c-143">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="2f36c-143">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

