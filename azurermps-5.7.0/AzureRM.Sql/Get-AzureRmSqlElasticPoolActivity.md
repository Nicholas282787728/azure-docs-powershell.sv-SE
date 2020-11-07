---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: 88052c9f47359e0080e193f5a2dbb1004b48b0e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756062"
---
# <span data-ttu-id="2ed93-101">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="2ed93-101">Get-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="2ed93-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2ed93-102">SYNOPSIS</span></span>
<span data-ttu-id="2ed93-103">Hämtar statusen för åtgärder på en elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="2ed93-103">Gets the status of operations on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ed93-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2ed93-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2ed93-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2ed93-105">DESCRIPTION</span></span>
<span data-ttu-id="2ed93-106">Cmdleten **Get-AzureRmSqlElasticPoolActivity** får statusen för åtgärder på en elastisk pool för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="2ed93-106">The **Get-AzureRmSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="2ed93-107">Du kan se status för både skapa och konfigurations uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="2ed93-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="2ed93-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2ed93-108">EXAMPLES</span></span>

### <span data-ttu-id="2ed93-109">Exempel 1: få statusen för en elastisk pool</span><span class="sxs-lookup"><span data-stu-id="2ed93-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="2ed93-110">Det här kommandot får statusen för åtgärderna för den Elastic pool som heter ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="2ed93-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="2ed93-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2ed93-111">PARAMETERS</span></span>

### <span data-ttu-id="2ed93-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ed93-112">-DefaultProfile</span></span>
<span data-ttu-id="2ed93-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2ed93-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ed93-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="2ed93-114">-ElasticPoolName</span></span>
<span data-ttu-id="2ed93-115">Anger namnet på en elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="2ed93-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="2ed93-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ed93-116">-ResourceGroupName</span></span>
<span data-ttu-id="2ed93-117">Anger namnet på en resurs grupp som den elastiska poolen är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="2ed93-117">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="2ed93-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2ed93-118">-ServerName</span></span>
<span data-ttu-id="2ed93-119">Anger namnet på en server som innehåller en elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="2ed93-119">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="2ed93-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2ed93-120">-Confirm</span></span>
<span data-ttu-id="2ed93-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2ed93-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed93-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ed93-122">-WhatIf</span></span>
<span data-ttu-id="2ed93-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2ed93-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ed93-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2ed93-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed93-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ed93-125">CommonParameters</span></span>
<span data-ttu-id="2ed93-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ed93-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ed93-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ed93-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ed93-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2ed93-128">INPUTS</span></span>

### <span data-ttu-id="2ed93-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="2ed93-129">None</span></span>
<span data-ttu-id="2ed93-130">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="2ed93-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2ed93-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2ed93-131">OUTPUTS</span></span>

### <span data-ttu-id="2ed93-132">Microsoft. Azure. commands. SQL. ElasticPool. Model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="2ed93-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="2ed93-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2ed93-133">NOTES</span></span>

## <span data-ttu-id="2ed93-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2ed93-134">RELATED LINKS</span></span>

[<span data-ttu-id="2ed93-135">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2ed93-135">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="2ed93-136">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="2ed93-136">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="2ed93-137">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2ed93-137">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="2ed93-138">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2ed93-138">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="2ed93-139">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2ed93-139">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)


