---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
ms.openlocfilehash: 61a72691aaaaf9cbdfd4e0706f6ace17d7291851
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746717"
---
# <span data-ttu-id="8e932-101">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="8e932-101">Get-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="8e932-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8e932-102">SYNOPSIS</span></span>
<span data-ttu-id="8e932-103">Hämtar statusen för åtgärder på en elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="8e932-103">Gets the status of operations on an elastic pool.</span></span>

## <span data-ttu-id="8e932-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8e932-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e932-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8e932-105">DESCRIPTION</span></span>
<span data-ttu-id="8e932-106">Cmdleten **Get-AzSqlElasticPoolActivity** får statusen för åtgärder på en elastisk pool för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="8e932-106">The **Get-AzSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="8e932-107">Du kan se status för både skapa och konfigurations uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="8e932-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="8e932-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8e932-108">EXAMPLES</span></span>

### <span data-ttu-id="8e932-109">Exempel 1: få statusen för en elastisk pool</span><span class="sxs-lookup"><span data-stu-id="8e932-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="8e932-110">Det här kommandot får statusen för åtgärderna för den Elastic pool som heter ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="8e932-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="8e932-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8e932-111">PARAMETERS</span></span>

### <span data-ttu-id="8e932-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e932-112">-DefaultProfile</span></span>
<span data-ttu-id="8e932-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8e932-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e932-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="8e932-114">-ElasticPoolName</span></span>
<span data-ttu-id="8e932-115">Anger namnet på en elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="8e932-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="8e932-116">-OperationId</span><span class="sxs-lookup"><span data-stu-id="8e932-116">-OperationId</span></span>
<span data-ttu-id="8e932-117">ID för den åtgärd som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="8e932-117">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="8e932-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e932-118">-ResourceGroupName</span></span>
<span data-ttu-id="8e932-119">Anger namnet på en resurs grupp som den elastiska poolen är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="8e932-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="8e932-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8e932-120">-ServerName</span></span>
<span data-ttu-id="8e932-121">Anger namnet på en server som innehåller en elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="8e932-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="8e932-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8e932-122">-Confirm</span></span>
<span data-ttu-id="8e932-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8e932-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e932-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e932-124">-WhatIf</span></span>
<span data-ttu-id="8e932-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8e932-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e932-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8e932-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e932-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e932-127">CommonParameters</span></span>
<span data-ttu-id="8e932-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e932-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e932-129">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e932-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e932-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8e932-130">INPUTS</span></span>

### <span data-ttu-id="8e932-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8e932-131">System.String</span></span>

### <span data-ttu-id="8e932-132">System. Nullable ' 1 [[system. GUID, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8e932-132">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8e932-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8e932-133">OUTPUTS</span></span>

### <span data-ttu-id="8e932-134">Microsoft. Azure. commands. SQL. ElasticPool. Model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="8e932-134">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="8e932-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8e932-135">NOTES</span></span>

## <span data-ttu-id="8e932-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8e932-136">RELATED LINKS</span></span>

[<span data-ttu-id="8e932-137">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="8e932-137">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="8e932-138">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="8e932-138">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="8e932-139">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="8e932-139">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="8e932-140">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="8e932-140">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="8e932-141">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="8e932-141">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)


