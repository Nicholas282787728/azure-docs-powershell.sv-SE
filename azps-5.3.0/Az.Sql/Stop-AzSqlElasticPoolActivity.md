---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
ms.openlocfilehash: dc1dffd84a95bd9cffac1dbafb5183d56e0b7c52
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522949"
---
# <span data-ttu-id="8f837-101">Stop-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="8f837-101">Stop-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="8f837-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8f837-102">SYNOPSIS</span></span>
<span data-ttu-id="8f837-103">Avbryter den asynkrona uppdateringen på en elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="8f837-103">Cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="8f837-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8f837-104">SYNTAX</span></span>

```
Stop-AzSqlElasticPoolActivity [-PassThru] [-ServerName] <String> [-ElasticPoolName] <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f837-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8f837-105">DESCRIPTION</span></span>
<span data-ttu-id="8f837-106">Cmdleten **Stop-AzSqlElasticPoolActivity** avbryter den asynkrona uppdaterings åtgärden på en elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="8f837-106">The **Stop-AzSqlElasticPoolActivity** cmdlet cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="8f837-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8f837-107">EXAMPLES</span></span>

### <span data-ttu-id="8f837-108">Exempel 1: Avbryt den asynkrona uppdateringen på en elastisk pool</span><span class="sxs-lookup"><span data-stu-id="8f837-108">Example 1: Cancel the asynchronous update operation on an elastic pool</span></span>
```
PS C:\> Stop-AzSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

OperationId     : af97005d-9243-4f8a-844e-402d1cc855f5
ServerName      : Server01
DatabaseName    : ElasticPool01
State           : CANCELLED
Operation       : UpdateLogicalElasticPool
ErrorCode       :
ErrorMessage    :
ErrorSeverity   :
StartTime       : 10/15/2017 02:49:42 PM
EndTime         : 10/15/2017 02:49:43 PM
PercentComplete :
```

<span data-ttu-id="8f837-109">Det här kommandot avbryter den asynkrona uppdateringen för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="8f837-109">This command cancels the asynchronous updates operation on the elastic pool.</span></span>

## <span data-ttu-id="8f837-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8f837-110">PARAMETERS</span></span>

### <span data-ttu-id="8f837-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f837-111">-DefaultProfile</span></span>
<span data-ttu-id="8f837-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8f837-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f837-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="8f837-113">-ElasticPoolName</span></span>
<span data-ttu-id="8f837-114">Namnet på den elastiska Azure SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="8f837-114">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="8f837-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="8f837-115">-OperationId</span></span>
<span data-ttu-id="8f837-116">ID för den åtgärd som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="8f837-116">The ID of the operation to retrieve.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f837-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f837-117">-PassThru</span></span>
<span data-ttu-id="8f837-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="8f837-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8f837-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f837-119">-ResourceGroupName</span></span>
<span data-ttu-id="8f837-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8f837-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="8f837-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8f837-121">-ServerName</span></span>
<span data-ttu-id="8f837-122">Namnet på den Azure SQL Server som den elastiska poolen är i.</span><span class="sxs-lookup"><span data-stu-id="8f837-122">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="8f837-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8f837-123">-Confirm</span></span>
<span data-ttu-id="8f837-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8f837-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f837-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f837-125">-WhatIf</span></span>
<span data-ttu-id="8f837-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8f837-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f837-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8f837-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f837-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f837-128">CommonParameters</span></span>
<span data-ttu-id="8f837-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f837-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f837-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f837-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f837-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8f837-131">INPUTS</span></span>

### <span data-ttu-id="8f837-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8f837-132">System.String</span></span>

### <span data-ttu-id="8f837-133">System. Nullable ' 1 [[system. GUID, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8f837-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8f837-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8f837-134">OUTPUTS</span></span>

### <span data-ttu-id="8f837-135">Microsoft. Azure. commands. SQL. ElasticPool. Model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="8f837-135">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="8f837-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8f837-136">NOTES</span></span>

## <span data-ttu-id="8f837-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8f837-137">RELATED LINKS</span></span>
