---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
ms.openlocfilehash: c508dc9352bfcf70a9d3bad088f2b75de98db43d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270205"
---
# <span data-ttu-id="acb5f-101">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="acb5f-101">Remove-AzSqlSyncMember</span></span>

## <span data-ttu-id="acb5f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="acb5f-102">SYNOPSIS</span></span>
<span data-ttu-id="acb5f-103">Tar bort en Azure SQL Database Sync-medlem.</span><span class="sxs-lookup"><span data-stu-id="acb5f-103">Removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="acb5f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="acb5f-104">SYNTAX</span></span>

```
Remove-AzSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acb5f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="acb5f-105">DESCRIPTION</span></span>
<span data-ttu-id="acb5f-106">Cmdleten **Remove-AzSqlSyncMember** tar bort en synkroniserad Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="acb5f-106">The **Remove-AzSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="acb5f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="acb5f-107">EXAMPLES</span></span>

### <span data-ttu-id="acb5f-108">Exempel 1: ta bort en synkroniserad medlem</span><span class="sxs-lookup"><span data-stu-id="acb5f-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="acb5f-109">Det här kommandot tar bort synkroniserings medlem för Azure SQL Database med namnet syncMember01.</span><span class="sxs-lookup"><span data-stu-id="acb5f-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="acb5f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="acb5f-110">PARAMETERS</span></span>

### <span data-ttu-id="acb5f-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="acb5f-111">-DatabaseName</span></span>
<span data-ttu-id="acb5f-112">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="acb5f-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="acb5f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acb5f-113">-DefaultProfile</span></span>
<span data-ttu-id="acb5f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="acb5f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="acb5f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="acb5f-115">-Force</span></span>
<span data-ttu-id="acb5f-116">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="acb5f-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="acb5f-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="acb5f-117">-Name</span></span>
<span data-ttu-id="acb5f-118">Synkroniserat medlems namn.</span><span class="sxs-lookup"><span data-stu-id="acb5f-118">The sync member name.</span></span>

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

### <span data-ttu-id="acb5f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="acb5f-119">-PassThru</span></span>
<span data-ttu-id="acb5f-120">Definierar om den borttagna medlemmen ska returneras</span><span class="sxs-lookup"><span data-stu-id="acb5f-120">Defines Whether return the removed sync member</span></span>

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

### <span data-ttu-id="acb5f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acb5f-121">-ResourceGroupName</span></span>
<span data-ttu-id="acb5f-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="acb5f-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="acb5f-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="acb5f-123">-ServerName</span></span>
<span data-ttu-id="acb5f-124">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="acb5f-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="acb5f-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="acb5f-125">-SyncGroupName</span></span>
<span data-ttu-id="acb5f-126">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="acb5f-126">The sync group name.</span></span>

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

### <span data-ttu-id="acb5f-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="acb5f-127">-Confirm</span></span>
<span data-ttu-id="acb5f-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="acb5f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acb5f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acb5f-129">-WhatIf</span></span>
<span data-ttu-id="acb5f-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="acb5f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acb5f-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="acb5f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acb5f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acb5f-132">CommonParameters</span></span>
<span data-ttu-id="acb5f-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acb5f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acb5f-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="acb5f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acb5f-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="acb5f-135">INPUTS</span></span>

### <span data-ttu-id="acb5f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="acb5f-136">System.String</span></span>

## <span data-ttu-id="acb5f-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="acb5f-137">OUTPUTS</span></span>

### <span data-ttu-id="acb5f-138">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="acb5f-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="acb5f-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="acb5f-139">NOTES</span></span>

## <span data-ttu-id="acb5f-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="acb5f-140">RELATED LINKS</span></span>

[<span data-ttu-id="acb5f-141">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="acb5f-141">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="acb5f-142">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="acb5f-142">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="acb5f-143">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="acb5f-143">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

