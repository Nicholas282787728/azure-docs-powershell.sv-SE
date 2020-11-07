---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
ms.openlocfilehash: 5adb6d79904b617b0ddbeaae28c9c7860c028fb8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746546"
---
# <span data-ttu-id="1e2ef-101">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="1e2ef-101">Remove-AzSqlSyncAgent</span></span>

## <span data-ttu-id="1e2ef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1e2ef-102">SYNOPSIS</span></span>
<span data-ttu-id="1e2ef-103">Tar bort en Azure SQL Sync-agent.</span><span class="sxs-lookup"><span data-stu-id="1e2ef-103">Removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="1e2ef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1e2ef-104">SYNTAX</span></span>

```
Remove-AzSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1e2ef-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1e2ef-105">DESCRIPTION</span></span>
<span data-ttu-id="1e2ef-106">Cmdleten **Remove-AzSqlSyncAgent** tar bort en Azure SQL Sync-agent.</span><span class="sxs-lookup"><span data-stu-id="1e2ef-106">The **Remove-AzSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="1e2ef-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1e2ef-107">EXAMPLES</span></span>

### <span data-ttu-id="1e2ef-108">Exempel 1: ta bort en synkroniseringsresurs</span><span class="sxs-lookup"><span data-stu-id="1e2ef-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="1e2ef-109">Det här kommandot tar bort Azure SQL Sync-agenten med namnet syncAgent01.</span><span class="sxs-lookup"><span data-stu-id="1e2ef-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="1e2ef-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1e2ef-110">PARAMETERS</span></span>

### <span data-ttu-id="1e2ef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e2ef-111">-DefaultProfile</span></span>
<span data-ttu-id="1e2ef-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1e2ef-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e2ef-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1e2ef-113">-Force</span></span>
<span data-ttu-id="1e2ef-114">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="1e2ef-114">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="1e2ef-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="1e2ef-115">-Name</span></span>
<span data-ttu-id="1e2ef-116">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="1e2ef-116">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e2ef-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e2ef-117">-PassThru</span></span>
<span data-ttu-id="1e2ef-118">Definierar om returnera den borttagna synkroniseringsresursen</span><span class="sxs-lookup"><span data-stu-id="1e2ef-118">Defines Whether return the removed sync agent</span></span>

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

### <span data-ttu-id="1e2ef-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e2ef-119">-ResourceGroupName</span></span>
<span data-ttu-id="1e2ef-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1e2ef-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="1e2ef-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1e2ef-121">-ServerName</span></span>
<span data-ttu-id="1e2ef-122">Namnet på den Azure SQL-Server som synkroniseringsresursen finns i.</span><span class="sxs-lookup"><span data-stu-id="1e2ef-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="1e2ef-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1e2ef-123">-Confirm</span></span>
<span data-ttu-id="1e2ef-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1e2ef-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e2ef-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e2ef-125">-WhatIf</span></span>
<span data-ttu-id="1e2ef-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1e2ef-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e2ef-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1e2ef-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e2ef-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e2ef-128">CommonParameters</span></span>
<span data-ttu-id="1e2ef-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e2ef-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e2ef-130">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e2ef-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e2ef-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1e2ef-131">INPUTS</span></span>

### <span data-ttu-id="1e2ef-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1e2ef-132">System.String</span></span>

## <span data-ttu-id="1e2ef-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1e2ef-133">OUTPUTS</span></span>

### <span data-ttu-id="1e2ef-134">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="1e2ef-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="1e2ef-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1e2ef-135">NOTES</span></span>

## <span data-ttu-id="1e2ef-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1e2ef-136">RELATED LINKS</span></span>

[<span data-ttu-id="1e2ef-137">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="1e2ef-137">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

[<span data-ttu-id="1e2ef-138">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="1e2ef-138">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

