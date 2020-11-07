---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlElasticPool.md
ms.openlocfilehash: 57f5f656f3c85e9d1c0d29c07a602a303208e7f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579715"
---
# <span data-ttu-id="57ee7-101">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="57ee7-101">Remove-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="57ee7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="57ee7-102">SYNOPSIS</span></span>
<span data-ttu-id="57ee7-103">Tar bort en elastisk databas.</span><span class="sxs-lookup"><span data-stu-id="57ee7-103">Deletes an elastic database pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57ee7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="57ee7-104">SYNTAX</span></span>

```
Remove-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57ee7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="57ee7-105">DESCRIPTION</span></span>
<span data-ttu-id="57ee7-106">Cmdleten **Remove-AzureRmSqlElasticPool** tar bort en elastisk Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="57ee7-106">The **Remove-AzureRmSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="57ee7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="57ee7-107">EXAMPLES</span></span>

### <span data-ttu-id="57ee7-108">Exempel 1: ta bort en elastisk pool</span><span class="sxs-lookup"><span data-stu-id="57ee7-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="57ee7-109">Det här kommandot tar bort en elastisk pool med namnet ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="57ee7-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="57ee7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="57ee7-110">PARAMETERS</span></span>

### <span data-ttu-id="57ee7-111">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="57ee7-111">-ElasticPoolName</span></span>
<span data-ttu-id="57ee7-112">Anger namnet på den elastiska pool som tas bort av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57ee7-112">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="57ee7-113">-Force</span><span class="sxs-lookup"><span data-stu-id="57ee7-113">-Force</span></span>
<span data-ttu-id="57ee7-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="57ee7-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="57ee7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57ee7-115">-ResourceGroupName</span></span>
<span data-ttu-id="57ee7-116">Anger namnet på den resurs grupp som den elastiska poolen är tilldelad.</span><span class="sxs-lookup"><span data-stu-id="57ee7-116">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="57ee7-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="57ee7-117">-ServerName</span></span>
<span data-ttu-id="57ee7-118">Anger namnet på den server som är värd för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="57ee7-118">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="57ee7-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="57ee7-119">-Confirm</span></span>
<span data-ttu-id="57ee7-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="57ee7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57ee7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57ee7-121">-WhatIf</span></span>
<span data-ttu-id="57ee7-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="57ee7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57ee7-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="57ee7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57ee7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57ee7-124">-DefaultProfile</span></span>
<span data-ttu-id="57ee7-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="57ee7-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57ee7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57ee7-126">CommonParameters</span></span>
<span data-ttu-id="57ee7-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57ee7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57ee7-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57ee7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57ee7-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="57ee7-129">INPUTS</span></span>

### <span data-ttu-id="57ee7-130">Microsoft. Azure. commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="57ee7-130">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="57ee7-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="57ee7-131">OUTPUTS</span></span>

### <span data-ttu-id="57ee7-132">Microsoft. Azure. commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="57ee7-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="57ee7-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="57ee7-133">NOTES</span></span>

## <span data-ttu-id="57ee7-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="57ee7-134">RELATED LINKS</span></span>

[<span data-ttu-id="57ee7-135">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="57ee7-135">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="57ee7-136">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="57ee7-136">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="57ee7-137">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="57ee7-137">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="57ee7-138">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="57ee7-138">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="57ee7-139">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="57ee7-139">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="57ee7-140">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="57ee7-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

