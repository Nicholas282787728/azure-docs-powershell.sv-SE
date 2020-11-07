---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
ms.openlocfilehash: b58ec1f76737f34664bdecef38f2b596be3702d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746571"
---
# <span data-ttu-id="023f1-101">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="023f1-101">Remove-AzSqlElasticPool</span></span>

## <span data-ttu-id="023f1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="023f1-102">SYNOPSIS</span></span>
<span data-ttu-id="023f1-103">Tar bort en elastisk databas.</span><span class="sxs-lookup"><span data-stu-id="023f1-103">Deletes an elastic database pool.</span></span>

## <span data-ttu-id="023f1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="023f1-104">SYNTAX</span></span>

```
Remove-AzSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="023f1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="023f1-105">DESCRIPTION</span></span>
<span data-ttu-id="023f1-106">Cmdleten **Remove-AzSqlElasticPool** tar bort en elastisk Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="023f1-106">The **Remove-AzSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="023f1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="023f1-107">EXAMPLES</span></span>

### <span data-ttu-id="023f1-108">Exempel 1: ta bort en elastisk pool</span><span class="sxs-lookup"><span data-stu-id="023f1-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="023f1-109">Det här kommandot tar bort en elastisk pool med namnet ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="023f1-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="023f1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="023f1-110">PARAMETERS</span></span>

### <span data-ttu-id="023f1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="023f1-111">-DefaultProfile</span></span>
<span data-ttu-id="023f1-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="023f1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="023f1-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="023f1-113">-ElasticPoolName</span></span>
<span data-ttu-id="023f1-114">Anger namnet på den elastiska pool som tas bort av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="023f1-114">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="023f1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="023f1-115">-Force</span></span>
<span data-ttu-id="023f1-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="023f1-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="023f1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="023f1-117">-ResourceGroupName</span></span>
<span data-ttu-id="023f1-118">Anger namnet på den resurs grupp som den elastiska poolen är tilldelad.</span><span class="sxs-lookup"><span data-stu-id="023f1-118">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="023f1-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="023f1-119">-ServerName</span></span>
<span data-ttu-id="023f1-120">Anger namnet på den server som är värd för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="023f1-120">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="023f1-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="023f1-121">-Confirm</span></span>
<span data-ttu-id="023f1-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="023f1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="023f1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="023f1-123">-WhatIf</span></span>
<span data-ttu-id="023f1-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="023f1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="023f1-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="023f1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="023f1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="023f1-126">CommonParameters</span></span>
<span data-ttu-id="023f1-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="023f1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="023f1-128">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="023f1-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="023f1-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="023f1-129">INPUTS</span></span>

### <span data-ttu-id="023f1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="023f1-130">System.String</span></span>

## <span data-ttu-id="023f1-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="023f1-131">OUTPUTS</span></span>

### <span data-ttu-id="023f1-132">Microsoft. Azure. commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="023f1-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="023f1-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="023f1-133">NOTES</span></span>

## <span data-ttu-id="023f1-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="023f1-134">RELATED LINKS</span></span>

[<span data-ttu-id="023f1-135">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="023f1-135">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="023f1-136">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="023f1-136">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="023f1-137">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="023f1-137">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="023f1-138">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="023f1-138">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="023f1-139">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="023f1-139">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="023f1-140">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="023f1-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


