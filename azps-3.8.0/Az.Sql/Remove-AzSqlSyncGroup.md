---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
ms.openlocfilehash: 3a5da7972e70e3ebf9c86df62b2bbc79651e72a5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090889"
---
# <span data-ttu-id="7a1cb-101">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="7a1cb-101">Remove-AzSqlSyncGroup</span></span>

## <span data-ttu-id="7a1cb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7a1cb-102">SYNOPSIS</span></span>
<span data-ttu-id="7a1cb-103">Tar bort en Azure SQL Database Sync-grupp.</span><span class="sxs-lookup"><span data-stu-id="7a1cb-103">Removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="7a1cb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7a1cb-104">SYNTAX</span></span>

```
Remove-AzSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7a1cb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7a1cb-105">DESCRIPTION</span></span>
<span data-ttu-id="7a1cb-106">Cmdleten **Remove-AzSqlSyncGroup** tar bort en Azure SQL Database Sync-grupp.</span><span class="sxs-lookup"><span data-stu-id="7a1cb-106">The **Remove-AzSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="7a1cb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7a1cb-107">EXAMPLES</span></span>

### <span data-ttu-id="7a1cb-108">Exempel 1: ta bort en synkroniseringsresurs</span><span class="sxs-lookup"><span data-stu-id="7a1cb-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="7a1cb-109">Det här kommandot tar bort synkroniseringsresursen för Azure SQL Database med namnet syncGroup01.</span><span class="sxs-lookup"><span data-stu-id="7a1cb-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="7a1cb-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7a1cb-110">PARAMETERS</span></span>

### <span data-ttu-id="7a1cb-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7a1cb-111">-DatabaseName</span></span>
<span data-ttu-id="7a1cb-112">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="7a1cb-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="7a1cb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a1cb-113">-DefaultProfile</span></span>
<span data-ttu-id="7a1cb-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7a1cb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a1cb-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7a1cb-115">-Force</span></span>
<span data-ttu-id="7a1cb-116">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="7a1cb-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="7a1cb-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="7a1cb-117">-Name</span></span>
<span data-ttu-id="7a1cb-118">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="7a1cb-118">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a1cb-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a1cb-119">-PassThru</span></span>
<span data-ttu-id="7a1cb-120">Definierar om den borttagna synkroniseringsresursen ska returneras</span><span class="sxs-lookup"><span data-stu-id="7a1cb-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="7a1cb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a1cb-121">-ResourceGroupName</span></span>
<span data-ttu-id="7a1cb-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7a1cb-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="7a1cb-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7a1cb-123">-ServerName</span></span>
<span data-ttu-id="7a1cb-124">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7a1cb-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="7a1cb-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7a1cb-125">-Confirm</span></span>
<span data-ttu-id="7a1cb-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7a1cb-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a1cb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a1cb-127">-WhatIf</span></span>
<span data-ttu-id="7a1cb-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7a1cb-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a1cb-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7a1cb-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a1cb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a1cb-130">CommonParameters</span></span>
<span data-ttu-id="7a1cb-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a1cb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a1cb-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a1cb-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a1cb-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7a1cb-133">INPUTS</span></span>

### <span data-ttu-id="7a1cb-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7a1cb-134">System.String</span></span>

## <span data-ttu-id="7a1cb-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7a1cb-135">OUTPUTS</span></span>

### <span data-ttu-id="7a1cb-136">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="7a1cb-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="7a1cb-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7a1cb-137">NOTES</span></span>

## <span data-ttu-id="7a1cb-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7a1cb-138">RELATED LINKS</span></span>

[<span data-ttu-id="7a1cb-139">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="7a1cb-139">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="7a1cb-140">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="7a1cb-140">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="7a1cb-141">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="7a1cb-141">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

