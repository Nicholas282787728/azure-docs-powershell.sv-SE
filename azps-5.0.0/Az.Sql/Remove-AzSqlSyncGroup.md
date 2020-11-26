---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
ms.openlocfilehash: 3a5da7972e70e3ebf9c86df62b2bbc79651e72a5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270207"
---
# <span data-ttu-id="1c267-101">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="1c267-101">Remove-AzSqlSyncGroup</span></span>

## <span data-ttu-id="1c267-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1c267-102">SYNOPSIS</span></span>
<span data-ttu-id="1c267-103">Tar bort en Azure SQL Database Sync-grupp.</span><span class="sxs-lookup"><span data-stu-id="1c267-103">Removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="1c267-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1c267-104">SYNTAX</span></span>

```
Remove-AzSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1c267-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1c267-105">DESCRIPTION</span></span>
<span data-ttu-id="1c267-106">Cmdleten **Remove-AzSqlSyncGroup** tar bort en Azure SQL Database Sync-grupp.</span><span class="sxs-lookup"><span data-stu-id="1c267-106">The **Remove-AzSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="1c267-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1c267-107">EXAMPLES</span></span>

### <span data-ttu-id="1c267-108">Exempel 1: ta bort en synkroniseringsresurs</span><span class="sxs-lookup"><span data-stu-id="1c267-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="1c267-109">Det här kommandot tar bort synkroniseringsresursen för Azure SQL Database med namnet syncGroup01.</span><span class="sxs-lookup"><span data-stu-id="1c267-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="1c267-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1c267-110">PARAMETERS</span></span>

### <span data-ttu-id="1c267-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1c267-111">-DatabaseName</span></span>
<span data-ttu-id="1c267-112">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="1c267-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="1c267-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c267-113">-DefaultProfile</span></span>
<span data-ttu-id="1c267-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1c267-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c267-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1c267-115">-Force</span></span>
<span data-ttu-id="1c267-116">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="1c267-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="1c267-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="1c267-117">-Name</span></span>
<span data-ttu-id="1c267-118">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="1c267-118">The sync group name.</span></span>

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

### <span data-ttu-id="1c267-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c267-119">-PassThru</span></span>
<span data-ttu-id="1c267-120">Definierar om den borttagna synkroniseringsresursen ska returneras</span><span class="sxs-lookup"><span data-stu-id="1c267-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="1c267-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c267-121">-ResourceGroupName</span></span>
<span data-ttu-id="1c267-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1c267-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="1c267-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1c267-123">-ServerName</span></span>
<span data-ttu-id="1c267-124">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1c267-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="1c267-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1c267-125">-Confirm</span></span>
<span data-ttu-id="1c267-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1c267-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c267-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c267-127">-WhatIf</span></span>
<span data-ttu-id="1c267-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1c267-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c267-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1c267-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c267-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c267-130">CommonParameters</span></span>
<span data-ttu-id="1c267-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c267-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c267-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c267-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c267-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1c267-133">INPUTS</span></span>

### <span data-ttu-id="1c267-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1c267-134">System.String</span></span>

## <span data-ttu-id="1c267-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1c267-135">OUTPUTS</span></span>

### <span data-ttu-id="1c267-136">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="1c267-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="1c267-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1c267-137">NOTES</span></span>

## <span data-ttu-id="1c267-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1c267-138">RELATED LINKS</span></span>

[<span data-ttu-id="1c267-139">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="1c267-139">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="1c267-140">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="1c267-140">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="1c267-141">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="1c267-141">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)
