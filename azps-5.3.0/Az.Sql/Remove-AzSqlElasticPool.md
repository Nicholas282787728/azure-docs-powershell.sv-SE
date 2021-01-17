---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
ms.openlocfilehash: d751954a5c66d9220513017aa62b6797f8f1ea6f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419088"
---
# <span data-ttu-id="de9f3-101">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="de9f3-101">Remove-AzSqlElasticPool</span></span>

## <span data-ttu-id="de9f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="de9f3-102">SYNOPSIS</span></span>
<span data-ttu-id="de9f3-103">Tar bort en elastisk databas.</span><span class="sxs-lookup"><span data-stu-id="de9f3-103">Deletes an elastic database pool.</span></span>

## <span data-ttu-id="de9f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="de9f3-104">SYNTAX</span></span>

```
Remove-AzSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="de9f3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="de9f3-105">DESCRIPTION</span></span>
<span data-ttu-id="de9f3-106">Cmdleten **Remove-AzSqlElasticPool** tar bort en elastisk Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="de9f3-106">The **Remove-AzSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="de9f3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="de9f3-107">EXAMPLES</span></span>

### <span data-ttu-id="de9f3-108">Exempel 1: ta bort en elastisk pool</span><span class="sxs-lookup"><span data-stu-id="de9f3-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="de9f3-109">Det här kommandot tar bort en elastisk pool med namnet ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="de9f3-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="de9f3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="de9f3-110">PARAMETERS</span></span>

### <span data-ttu-id="de9f3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de9f3-111">-DefaultProfile</span></span>
<span data-ttu-id="de9f3-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="de9f3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de9f3-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="de9f3-113">-ElasticPoolName</span></span>
<span data-ttu-id="de9f3-114">Anger namnet på den elastiska pool som tas bort av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de9f3-114">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de9f3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="de9f3-115">-Force</span></span>
<span data-ttu-id="de9f3-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="de9f3-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="de9f3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de9f3-117">-ResourceGroupName</span></span>
<span data-ttu-id="de9f3-118">Anger namnet på den resurs grupp som den elastiska poolen är tilldelad.</span><span class="sxs-lookup"><span data-stu-id="de9f3-118">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="de9f3-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="de9f3-119">-ServerName</span></span>
<span data-ttu-id="de9f3-120">Anger namnet på den server som är värd för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="de9f3-120">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="de9f3-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="de9f3-121">-Confirm</span></span>
<span data-ttu-id="de9f3-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="de9f3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de9f3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de9f3-123">-WhatIf</span></span>
<span data-ttu-id="de9f3-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="de9f3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de9f3-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="de9f3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de9f3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de9f3-126">CommonParameters</span></span>
<span data-ttu-id="de9f3-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de9f3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de9f3-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de9f3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de9f3-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="de9f3-129">INPUTS</span></span>

### <span data-ttu-id="de9f3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="de9f3-130">System.String</span></span>

## <span data-ttu-id="de9f3-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="de9f3-131">OUTPUTS</span></span>

### <span data-ttu-id="de9f3-132">Microsoft. Azure. commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="de9f3-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="de9f3-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="de9f3-133">NOTES</span></span>

## <span data-ttu-id="de9f3-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="de9f3-134">RELATED LINKS</span></span>

[<span data-ttu-id="de9f3-135">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="de9f3-135">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="de9f3-136">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="de9f3-136">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="de9f3-137">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="de9f3-137">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="de9f3-138">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="de9f3-138">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="de9f3-139">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="de9f3-139">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="de9f3-140">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="de9f3-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


