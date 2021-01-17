---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
ms.openlocfilehash: d09f0032d44a0558c1052f1dcfc3a3c94a7dff00
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391435"
---
# <span data-ttu-id="d8e82-101">Stop-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="d8e82-101">Stop-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="d8e82-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d8e82-102">SYNOPSIS</span></span>
<span data-ttu-id="d8e82-103">Stoppar en synkronisering av en synkroniseringsresurs.</span><span class="sxs-lookup"><span data-stu-id="d8e82-103">Stops a sync group synchronization.</span></span>

## <span data-ttu-id="d8e82-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d8e82-104">SYNTAX</span></span>

```
Stop-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d8e82-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d8e82-105">DESCRIPTION</span></span>
<span data-ttu-id="d8e82-106">Cmdleten **Stop-AzSqlSyncGroupSync** stoppar synkroniseringen av en synkroniseringsresurs.</span><span class="sxs-lookup"><span data-stu-id="d8e82-106">The **Stop-AzSqlSyncGroupSync** cmdlet stops a sync group synchronization.</span></span>

## <span data-ttu-id="d8e82-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d8e82-107">EXAMPLES</span></span>

### <span data-ttu-id="d8e82-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d8e82-108">Example 1</span></span>
```
PS C:\> Stop-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="d8e82-109">Det här kommandot stoppar den synkronisering som pågår för gruppen Sync-mysg.</span><span class="sxs-lookup"><span data-stu-id="d8e82-109">This command stops the synchronization which is ongoing for the sync group mysg.</span></span>

## <span data-ttu-id="d8e82-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d8e82-110">PARAMETERS</span></span>

### <span data-ttu-id="d8e82-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d8e82-111">-DatabaseName</span></span>
<span data-ttu-id="d8e82-112">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="d8e82-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="d8e82-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8e82-113">-DefaultProfile</span></span>
<span data-ttu-id="d8e82-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d8e82-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8e82-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8e82-115">-PassThru</span></span>
<span data-ttu-id="d8e82-116">Definierar om synkroniseringsresursen ska returneras</span><span class="sxs-lookup"><span data-stu-id="d8e82-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="d8e82-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8e82-117">-ResourceGroupName</span></span>
<span data-ttu-id="d8e82-118">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d8e82-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="d8e82-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d8e82-119">-ServerName</span></span>
<span data-ttu-id="d8e82-120">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d8e82-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="d8e82-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="d8e82-121">-SyncGroupName</span></span>
<span data-ttu-id="d8e82-122">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="d8e82-122">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8e82-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d8e82-123">-Confirm</span></span>
<span data-ttu-id="d8e82-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d8e82-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8e82-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8e82-125">-WhatIf</span></span>
<span data-ttu-id="d8e82-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d8e82-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8e82-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d8e82-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8e82-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8e82-128">CommonParameters</span></span>
<span data-ttu-id="d8e82-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8e82-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8e82-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8e82-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8e82-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d8e82-131">INPUTS</span></span>

### <span data-ttu-id="d8e82-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d8e82-132">System.String</span></span>

## <span data-ttu-id="d8e82-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d8e82-133">OUTPUTS</span></span>

### <span data-ttu-id="d8e82-134">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="d8e82-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="d8e82-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d8e82-135">NOTES</span></span>

## <span data-ttu-id="d8e82-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d8e82-136">RELATED LINKS</span></span>

[<span data-ttu-id="d8e82-137">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="d8e82-137">Start-AzSqlSyncGroupSync</span></span>](./Start-AzSqlSyncGroupSync.md)

