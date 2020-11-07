---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlElasticPool.md
ms.openlocfilehash: 3786dc0a9500dd07b332dacfbb026b5a44f0b550
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757020"
---
# <span data-ttu-id="8380e-101">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="8380e-101">Remove-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="8380e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8380e-102">SYNOPSIS</span></span>
<span data-ttu-id="8380e-103">Tar bort en elastisk databas.</span><span class="sxs-lookup"><span data-stu-id="8380e-103">Deletes an elastic database pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8380e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8380e-104">SYNTAX</span></span>

```
Remove-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8380e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8380e-105">DESCRIPTION</span></span>
<span data-ttu-id="8380e-106">Cmdleten **Remove-AzureRmSqlElasticPool** tar bort en elastisk Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="8380e-106">The **Remove-AzureRmSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="8380e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8380e-107">EXAMPLES</span></span>

### <span data-ttu-id="8380e-108">Exempel 1: ta bort en elastisk pool</span><span class="sxs-lookup"><span data-stu-id="8380e-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="8380e-109">Det här kommandot tar bort en elastisk pool med namnet ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="8380e-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="8380e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8380e-110">PARAMETERS</span></span>

### <span data-ttu-id="8380e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8380e-111">-DefaultProfile</span></span>
<span data-ttu-id="8380e-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8380e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8380e-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="8380e-113">-ElasticPoolName</span></span>
<span data-ttu-id="8380e-114">Anger namnet på den elastiska pool som tas bort av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8380e-114">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="8380e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8380e-115">-Force</span></span>
<span data-ttu-id="8380e-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="8380e-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8380e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8380e-117">-ResourceGroupName</span></span>
<span data-ttu-id="8380e-118">Anger namnet på den resurs grupp som den elastiska poolen är tilldelad.</span><span class="sxs-lookup"><span data-stu-id="8380e-118">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="8380e-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8380e-119">-ServerName</span></span>
<span data-ttu-id="8380e-120">Anger namnet på den server som är värd för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="8380e-120">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="8380e-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8380e-121">-Confirm</span></span>
<span data-ttu-id="8380e-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8380e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8380e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8380e-123">-WhatIf</span></span>
<span data-ttu-id="8380e-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8380e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8380e-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8380e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8380e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8380e-126">CommonParameters</span></span>
<span data-ttu-id="8380e-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8380e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8380e-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8380e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8380e-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8380e-129">INPUTS</span></span>

### <span data-ttu-id="8380e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8380e-130">System.String</span></span>

## <span data-ttu-id="8380e-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8380e-131">OUTPUTS</span></span>

### <span data-ttu-id="8380e-132">Microsoft. Azure. commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="8380e-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="8380e-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8380e-133">NOTES</span></span>

## <span data-ttu-id="8380e-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8380e-134">RELATED LINKS</span></span>

[<span data-ttu-id="8380e-135">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="8380e-135">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="8380e-136">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="8380e-136">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="8380e-137">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="8380e-137">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="8380e-138">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="8380e-138">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="8380e-139">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="8380e-139">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="8380e-140">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="8380e-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


