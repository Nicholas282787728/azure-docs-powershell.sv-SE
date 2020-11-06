---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: 999fd83af11422f1499e386f194fd75d9b99e152
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576019"
---
# <span data-ttu-id="26200-101">Stop-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="26200-101">Stop-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="26200-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="26200-102">SYNOPSIS</span></span>
<span data-ttu-id="26200-103">Avbryter den asynkrona uppdateringen på en elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="26200-103">Cancels the asynchronous update operation on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26200-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="26200-104">SYNTAX</span></span>

```
Stop-AzureRmSqlElasticPoolActivity [-PassThru] [-ServerName] <String> [-ElasticPoolName] <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26200-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="26200-105">DESCRIPTION</span></span>
<span data-ttu-id="26200-106">Cmdleten **Stop-AzureRmSqlElasticPoolActivity** avbryter den asynkrona uppdaterings åtgärden på en elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="26200-106">The **Stop-AzureRmSqlElasticPoolActivity** cmdlet cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="26200-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="26200-107">EXAMPLES</span></span>

### <span data-ttu-id="26200-108">Exempel 1: Avbryt den asynkrona uppdateringen på en elastisk pool</span><span class="sxs-lookup"><span data-stu-id="26200-108">Example 1: Cancel the asynchronous update operation on an elastic pool</span></span>
```
PS C:\> Stop-AzureRmSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

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

<span data-ttu-id="26200-109">Det här kommandot avbryter den asynkrona uppdateringen för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="26200-109">This command cancels the asynchronous updates operation on the elastic pool.</span></span>

## <span data-ttu-id="26200-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="26200-110">PARAMETERS</span></span>

### <span data-ttu-id="26200-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26200-111">-DefaultProfile</span></span>
<span data-ttu-id="26200-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="26200-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26200-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="26200-113">-ElasticPoolName</span></span>
<span data-ttu-id="26200-114">Namnet på den elastiska Azure SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="26200-114">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="26200-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="26200-115">-OperationId</span></span>
<span data-ttu-id="26200-116">ID för den åtgärd som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="26200-116">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="26200-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26200-117">-PassThru</span></span>
<span data-ttu-id="26200-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="26200-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="26200-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26200-119">-ResourceGroupName</span></span>
<span data-ttu-id="26200-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="26200-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="26200-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="26200-121">-ServerName</span></span>
<span data-ttu-id="26200-122">Namnet på den Azure SQL Server som den elastiska poolen är i.</span><span class="sxs-lookup"><span data-stu-id="26200-122">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="26200-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="26200-123">-Confirm</span></span>
<span data-ttu-id="26200-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="26200-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26200-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26200-125">-WhatIf</span></span>
<span data-ttu-id="26200-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="26200-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26200-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="26200-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26200-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26200-128">CommonParameters</span></span>
<span data-ttu-id="26200-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26200-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26200-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26200-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26200-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="26200-131">INPUTS</span></span>

### <span data-ttu-id="26200-132">System. String</span><span class="sxs-lookup"><span data-stu-id="26200-132">System.String</span></span>

### <span data-ttu-id="26200-133">System. Nullable ' 1 [[system. GUID, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="26200-133">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="26200-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="26200-134">OUTPUTS</span></span>

### <span data-ttu-id="26200-135">Microsoft. Azure. commands. SQL. ElasticPool. Model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="26200-135">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="26200-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="26200-136">NOTES</span></span>

## <span data-ttu-id="26200-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="26200-137">RELATED LINKS</span></span>
