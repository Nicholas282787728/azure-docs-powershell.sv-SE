---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
ms.openlocfilehash: e35187bf22015f3398a9fd95ce60a1cd597f7c22
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103457"
---
# <span data-ttu-id="9750d-101">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="9750d-101">Start-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="9750d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9750d-102">SYNOPSIS</span></span>
<span data-ttu-id="9750d-103">Startar en synkronisering av en synkroniseringsresurs.</span><span class="sxs-lookup"><span data-stu-id="9750d-103">Starts a sync group synchronization.</span></span>

## <span data-ttu-id="9750d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9750d-104">SYNTAX</span></span>

```
Start-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9750d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9750d-105">DESCRIPTION</span></span>
<span data-ttu-id="9750d-106">Cmdleten **Start-AzSqlSyncGroupSync** startar en synkronisering av synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="9750d-106">The **Start-AzSqlSyncGroupSync** cmdlet starts a sync group synchronization.</span></span>

## <span data-ttu-id="9750d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9750d-107">EXAMPLES</span></span>

### <span data-ttu-id="9750d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9750d-108">Example 1</span></span>
```
PS C:\> Start-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="9750d-109">Det här kommandot startar en rund synkronisering för gruppen Sync Group mysg.</span><span class="sxs-lookup"><span data-stu-id="9750d-109">This command starts a round of synchronization for the sync group mysg.</span></span>

## <span data-ttu-id="9750d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9750d-110">PARAMETERS</span></span>

### <span data-ttu-id="9750d-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9750d-111">-DatabaseName</span></span>
<span data-ttu-id="9750d-112">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="9750d-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="9750d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9750d-113">-DefaultProfile</span></span>
<span data-ttu-id="9750d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9750d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9750d-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9750d-115">-PassThru</span></span>
<span data-ttu-id="9750d-116">Definierar om synkroniseringsresursen ska returneras</span><span class="sxs-lookup"><span data-stu-id="9750d-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="9750d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9750d-117">-ResourceGroupName</span></span>
<span data-ttu-id="9750d-118">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9750d-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="9750d-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9750d-119">-ServerName</span></span>
<span data-ttu-id="9750d-120">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9750d-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="9750d-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="9750d-121">-SyncGroupName</span></span>
<span data-ttu-id="9750d-122">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="9750d-122">The sync group name.</span></span>

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

### <span data-ttu-id="9750d-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9750d-123">-Confirm</span></span>
<span data-ttu-id="9750d-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9750d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9750d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9750d-125">-WhatIf</span></span>
<span data-ttu-id="9750d-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9750d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9750d-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9750d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9750d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9750d-128">CommonParameters</span></span>
<span data-ttu-id="9750d-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9750d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9750d-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9750d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9750d-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9750d-131">INPUTS</span></span>

### <span data-ttu-id="9750d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9750d-132">System.String</span></span>

## <span data-ttu-id="9750d-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9750d-133">OUTPUTS</span></span>

### <span data-ttu-id="9750d-134">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="9750d-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="9750d-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9750d-135">NOTES</span></span>

## <span data-ttu-id="9750d-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9750d-136">RELATED LINKS</span></span>

[<span data-ttu-id="9750d-137">Stopp-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="9750d-137">Stop-AzSqlSyncGroupSync</span></span>](./Stop-AzSqlSyncGroupSync.md)

