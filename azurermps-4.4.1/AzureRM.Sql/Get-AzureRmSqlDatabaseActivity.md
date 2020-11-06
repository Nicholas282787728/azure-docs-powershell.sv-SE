---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
ms.openlocfilehash: b37ae31c1f0dc6360743a863f0305fd5823cbb3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584507"
---
# <span data-ttu-id="a74d2-101">Get-AzureRmSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="a74d2-101">Get-AzureRmSqlDatabaseActivity</span></span>

## <span data-ttu-id="a74d2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a74d2-102">SYNOPSIS</span></span>
<span data-ttu-id="a74d2-103">Hämtar status för elastiska databaser.</span><span class="sxs-lookup"><span data-stu-id="a74d2-103">Gets the status of moving elastic databases.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a74d2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a74d2-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseActivity [-ServerName] <String> -ElasticPoolName <String> -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a74d2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a74d2-105">DESCRIPTION</span></span>
<span data-ttu-id="a74d2-106">Cmdleten **Get-AzureRmSqlDatabaseActivity** får statusen för elastiska databaser som flyttas in i eller ut ur en Elastic Database-pool i Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="a74d2-106">The **Get-AzureRmSqlDatabaseActivity** cmdlet gets the status of elastic databases moving into or out of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="a74d2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a74d2-107">EXAMPLES</span></span>

### <span data-ttu-id="a74d2-108">Exempel 1: Hämta status för alla SQL Database-instanser</span><span class="sxs-lookup"><span data-stu-id="a74d2-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="a74d2-109">Det här kommandot returnerar status för alla SQL databas-instanser i en elastisk pool med namnet ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="a74d2-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="a74d2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a74d2-110">PARAMETERS</span></span>

### <span data-ttu-id="a74d2-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a74d2-111">-DatabaseName</span></span>
<span data-ttu-id="a74d2-112">Anger namnet på den databas där denna cmdlet får status.</span><span class="sxs-lookup"><span data-stu-id="a74d2-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a74d2-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="a74d2-113">-ElasticPoolName</span></span>
<span data-ttu-id="a74d2-114">Anger namnet på den Elastic Database-pool för vilken denna cmdlet får status.</span><span class="sxs-lookup"><span data-stu-id="a74d2-114">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a74d2-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="a74d2-115">-OperationId</span></span>
<span data-ttu-id="a74d2-116">Anger ID för den operation som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="a74d2-116">Specifies the ID of the operation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a74d2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a74d2-117">-ResourceGroupName</span></span>
<span data-ttu-id="a74d2-118">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="a74d2-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="a74d2-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a74d2-119">-ServerName</span></span>
<span data-ttu-id="a74d2-120">Anger namnet på den Microsoft SQL Server som är värd för den Elastic Database-poolen.</span><span class="sxs-lookup"><span data-stu-id="a74d2-120">Specifies the name of the Microsoft SQL Server that hosts the elastic database pool.</span></span>

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

### <span data-ttu-id="a74d2-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a74d2-121">-Confirm</span></span>
<span data-ttu-id="a74d2-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a74d2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a74d2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a74d2-123">-WhatIf</span></span>
<span data-ttu-id="a74d2-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a74d2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a74d2-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a74d2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a74d2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a74d2-126">-DefaultProfile</span></span>
<span data-ttu-id="a74d2-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a74d2-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a74d2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a74d2-128">CommonParameters</span></span>
<span data-ttu-id="a74d2-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a74d2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a74d2-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a74d2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a74d2-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a74d2-131">INPUTS</span></span>

## <span data-ttu-id="a74d2-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a74d2-132">OUTPUTS</span></span>

### <span data-ttu-id="a74d2-133">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="a74d2-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="a74d2-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a74d2-134">NOTES</span></span>

## <span data-ttu-id="a74d2-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a74d2-135">RELATED LINKS</span></span>

