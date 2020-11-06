---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: 87744454627feaadc8c953e1ad4e50016f14879f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580943"
---
# <span data-ttu-id="5099c-101">Stop-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="5099c-101">Stop-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="5099c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5099c-102">SYNOPSIS</span></span>
<span data-ttu-id="5099c-103">Avbryter den asynkrona uppdateringen på en elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="5099c-103">Cancels the asynchronous update operation on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5099c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5099c-104">SYNTAX</span></span>

```
Stop-AzureRmSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5099c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5099c-105">DESCRIPTION</span></span>
<span data-ttu-id="5099c-106">Cmdleten **Stop-AzureRmSqlElasticPoolActivity** avbryter den asynkrona uppdaterings åtgärden på en elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="5099c-106">The **Stop-AzureRmSqlElasticPoolActivity** cmdlet cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="5099c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5099c-107">EXAMPLES</span></span>

### <span data-ttu-id="5099c-108">Exempel 1: Avbryt den asynkrona uppdateringen på en elastisk pool</span><span class="sxs-lookup"><span data-stu-id="5099c-108">Example 1: Cancel the asynchronous update operation on an elastic pool</span></span>
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

<span data-ttu-id="5099c-109">Det här kommandot avbryter den asynkrona uppdateringen för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="5099c-109">This command cancels the asynchronous updates operation on the elastic pool.</span></span>

## <span data-ttu-id="5099c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5099c-110">PARAMETERS</span></span>

### <span data-ttu-id="5099c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5099c-111">-DefaultProfile</span></span>
<span data-ttu-id="5099c-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5099c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5099c-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="5099c-113">-ElasticPoolName</span></span>
<span data-ttu-id="5099c-114">Namnet på den elastiska Azure SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="5099c-114">The name of the Azure SQL Elastic Pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5099c-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="5099c-115">-OperationId</span></span>
<span data-ttu-id="5099c-116">ID för den åtgärd som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="5099c-116">The ID of the operation to retrieve.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5099c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5099c-117">-ResourceGroupName</span></span>
<span data-ttu-id="5099c-118">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5099c-118">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5099c-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5099c-119">-ServerName</span></span>
<span data-ttu-id="5099c-120">Namnet på den Azure SQL Server som den elastiska poolen är i.</span><span class="sxs-lookup"><span data-stu-id="5099c-120">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5099c-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5099c-121">-Confirm</span></span>
<span data-ttu-id="5099c-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5099c-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5099c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5099c-123">-WhatIf</span></span>
<span data-ttu-id="5099c-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5099c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5099c-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5099c-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5099c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5099c-126">CommonParameters</span></span>
<span data-ttu-id="5099c-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5099c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5099c-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5099c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5099c-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5099c-129">INPUTS</span></span>

### <span data-ttu-id="5099c-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="5099c-130">None</span></span>

<span data-ttu-id="5099c-131">Du kan ange indata för denna cmdlet efter egenskaps namn, men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="5099c-131">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="5099c-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5099c-132">OUTPUTS</span></span>

### <span data-ttu-id="5099c-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="5099c-133">System.Object</span></span>

## <span data-ttu-id="5099c-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5099c-134">NOTES</span></span>

## <span data-ttu-id="5099c-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5099c-135">RELATED LINKS</span></span>



