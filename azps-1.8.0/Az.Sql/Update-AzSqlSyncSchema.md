---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
ms.openlocfilehash: b5a0a09986be3856db4ab65f9dc411e6940ffb64
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746438"
---
# <span data-ttu-id="b212c-101">Update-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="b212c-101">Update-AzSqlSyncSchema</span></span>

## <span data-ttu-id="b212c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b212c-102">SYNOPSIS</span></span>
<span data-ttu-id="b212c-103">Uppdatera synkroniseringsschemat för en synkroniserad medlems databas eller en databas för Lösenordssynkronisering.</span><span class="sxs-lookup"><span data-stu-id="b212c-103">Update the sync schema for a sync member database or a sync hub database.</span></span>
<span data-ttu-id="b212c-104">Den senaste databas schema från den riktiga databasen hämtas och sedan används den för att uppdatera schemat i databasen.</span><span class="sxs-lookup"><span data-stu-id="b212c-104">It will get the latest database schema from the real database and then use it refresh the schema cached by Sync metadata database.</span></span>
<span data-ttu-id="b212c-105">Om "SyncMemberName" anges uppdaterar det databasschemat för medlems databasen; Om du inte gör det kommer det att uppdatera Hub-databasschemat.</span><span class="sxs-lookup"><span data-stu-id="b212c-105">If "SyncMemberName" is specified, it will refresh the member database schema; if not, it will refresh the hub database schema.</span></span>

## <span data-ttu-id="b212c-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b212c-106">SYNTAX</span></span>

```
Update-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b212c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b212c-107">DESCRIPTION</span></span>
<span data-ttu-id="b212c-108">Cmdleten **Update-AzSqlSyncSchema** uppdaterar synkroniseringsschemat för en synkroniserad medlems databas eller en synkroniseringskoppling.</span><span class="sxs-lookup"><span data-stu-id="b212c-108">The **Update-AzSqlSyncSchema** cmdlet updates the sync schema for a sync member database or a sync hub database.</span></span>

## <span data-ttu-id="b212c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b212c-109">EXAMPLES</span></span>

### <span data-ttu-id="b212c-110">Exempel 1: uppdatera synkroniseringsschemat för en nav-databas</span><span class="sxs-lookup"><span data-stu-id="b212c-110">Example 1: Update the sync schema for a hub database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
```

<span data-ttu-id="b212c-111">Det här kommandot uppdaterar synkroniseringsschemat för NAV databasen i Sync-gruppsyncGroup01</span><span class="sxs-lookup"><span data-stu-id="b212c-111">This command updates the sync schema for the hub database in the sync group syncGroup01</span></span>

### <span data-ttu-id="b212c-112">Exempel 2: uppdatera synkroniseringsschemat för en medlems databas</span><span class="sxs-lookup"><span data-stu-id="b212c-112">Example 2: Update the sync schema for a member database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
```

<span data-ttu-id="b212c-113">Det här kommandot uppdaterar synkroniseringsschemat för medlems databasen i syncMember01</span><span class="sxs-lookup"><span data-stu-id="b212c-113">This command updates the sync schema for the member database in the sync member syncMember01</span></span>

## <span data-ttu-id="b212c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b212c-114">PARAMETERS</span></span>

### <span data-ttu-id="b212c-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b212c-115">-DatabaseName</span></span>
<span data-ttu-id="b212c-116">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="b212c-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="b212c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b212c-117">-DefaultProfile</span></span>
<span data-ttu-id="b212c-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b212c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b212c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b212c-119">-PassThru</span></span>
<span data-ttu-id="b212c-120">Definierar om den synkroniserade gruppen ska returneras den här cmdleten fungerar</span><span class="sxs-lookup"><span data-stu-id="b212c-120">Defines Whether return the sync group this cmdlet works on</span></span>

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

### <span data-ttu-id="b212c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b212c-121">-ResourceGroupName</span></span>
<span data-ttu-id="b212c-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b212c-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="b212c-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b212c-123">-ServerName</span></span>
<span data-ttu-id="b212c-124">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b212c-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="b212c-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="b212c-125">-SyncGroupName</span></span>
<span data-ttu-id="b212c-126">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="b212c-126">The sync group name.</span></span>

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

### <span data-ttu-id="b212c-127">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="b212c-127">-SyncMemberName</span></span>
<span data-ttu-id="b212c-128">Synkroniserat medlems namn.</span><span class="sxs-lookup"><span data-stu-id="b212c-128">The sync member name.</span></span>

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

### <span data-ttu-id="b212c-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b212c-129">-Confirm</span></span>
<span data-ttu-id="b212c-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b212c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b212c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b212c-131">-WhatIf</span></span>
<span data-ttu-id="b212c-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b212c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b212c-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b212c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b212c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b212c-134">CommonParameters</span></span>
<span data-ttu-id="b212c-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b212c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b212c-136">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b212c-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b212c-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b212c-137">INPUTS</span></span>

### <span data-ttu-id="b212c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b212c-138">System.String</span></span>

## <span data-ttu-id="b212c-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b212c-139">OUTPUTS</span></span>

### <span data-ttu-id="b212c-140">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="b212c-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="b212c-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b212c-141">NOTES</span></span>

## <span data-ttu-id="b212c-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b212c-142">RELATED LINKS</span></span>
