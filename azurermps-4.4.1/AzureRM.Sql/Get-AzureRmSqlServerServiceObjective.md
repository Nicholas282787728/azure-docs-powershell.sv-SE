---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
ms.openlocfilehash: 5f0786c180461522d17d2697931f4a9887935f3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757441"
---
# <span data-ttu-id="1ae7c-101">Get-AzureRmSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="1ae7c-101">Get-AzureRmSqlServerServiceObjective</span></span>

## <span data-ttu-id="1ae7c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1ae7c-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae7c-103">Hämtar tjänste mål för en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="1ae7c-103">Gets service objectives for an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ae7c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1ae7c-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ServerName] <String>
 [[-DatabaseName] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ae7c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1ae7c-105">DESCRIPTION</span></span>
<span data-ttu-id="1ae7c-106">Cmdleten **Get-AzureRmSqlServerServiceObjective** hämtar de tillgängliga tjänst målen för en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="1ae7c-106">The **Get-AzureRmSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="1ae7c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1ae7c-107">EXAMPLES</span></span>

### <span data-ttu-id="1ae7c-108">Exempel 1: få service mål</span><span class="sxs-lookup"><span data-stu-id="1ae7c-108">Example 1: Get service objectives</span></span>
```
PS C:\>Get-AzureRmSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName ServerName ServiceObjectiveName Description Enabled IsDefault IsSystem
----------------- ---------- -------------------- ----------- ------- --------- --------
resourcegroup01   server01   ElasticPool                         True     False    False
resourcegroup01   server01   System                              True     False     True
resourcegroup01   server01   System0                             True     False     True
resourcegroup01   server01   System1                             True     False     True
resourcegroup01   server01   System2                             True      True     True
resourcegroup01   server01   Basic                               True      True    False
resourcegroup01   server01   S0                                  True      True    False
resourcegroup01   server01   S1                                  True     False    False
resourcegroup01   server01   S2                                  True     False    False
resourcegroup01   server01   S3                                  True     False    False
resourcegroup01   server01   P1                                  True      True    False
resourcegroup01   server01   P2                                  True     False    False
resourcegroup01   server01   P3                                  True     False    False
resourcegroup01   server01   P4                                  True     False    False
```

<span data-ttu-id="1ae7c-109">Med det här kommandot får du tjänst målen för servern med namnet Server01 och databasen med namnet Database01.</span><span class="sxs-lookup"><span data-stu-id="1ae7c-109">This command gets the service objectives for the server named Server01 and the database named Database01.</span></span>

## <span data-ttu-id="1ae7c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1ae7c-110">PARAMETERS</span></span>

### <span data-ttu-id="1ae7c-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1ae7c-111">-DatabaseName</span></span>
<span data-ttu-id="1ae7c-112">Anger namnet på en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="1ae7c-112">Specifies the name of an Azure SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae7c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ae7c-113">-ResourceGroupName</span></span>
<span data-ttu-id="1ae7c-114">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="1ae7c-114">Specifies the name of a resource group.</span></span>
<span data-ttu-id="1ae7c-115">Denna cmdlet hämtar tjänst mål för en SQL-databasserver som tilldelats den här resursen.</span><span class="sxs-lookup"><span data-stu-id="1ae7c-115">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

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

### <span data-ttu-id="1ae7c-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1ae7c-116">-ServerName</span></span>
<span data-ttu-id="1ae7c-117">Anger namnet på en SQL-databasserver i SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="1ae7c-117">Specifies the name of a SQL Database SQL Database server.</span></span>

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

### <span data-ttu-id="1ae7c-118">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="1ae7c-118">-ServiceObjectiveName</span></span>
<span data-ttu-id="1ae7c-119">Anger namnet på ett tjänst mål för en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="1ae7c-119">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="1ae7c-120">De acceptabla värdena för den här parametern är: Basic, S0, S1, S2, P1, P2 och P3.</span><span class="sxs-lookup"><span data-stu-id="1ae7c-120">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae7c-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1ae7c-121">-Confirm</span></span>
<span data-ttu-id="1ae7c-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1ae7c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ae7c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ae7c-123">-WhatIf</span></span>
<span data-ttu-id="1ae7c-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1ae7c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ae7c-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1ae7c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ae7c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ae7c-126">-DefaultProfile</span></span>
<span data-ttu-id="1ae7c-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1ae7c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ae7c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae7c-128">CommonParameters</span></span>
<span data-ttu-id="1ae7c-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ae7c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae7c-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ae7c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae7c-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1ae7c-131">INPUTS</span></span>

## <span data-ttu-id="1ae7c-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1ae7c-132">OUTPUTS</span></span>

### <span data-ttu-id="1ae7c-133">Microsoft. Azure. commands. SQL. ServiceObjective. Model. AzureSqlServerServiceObjectiveModel</span><span class="sxs-lookup"><span data-stu-id="1ae7c-133">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="1ae7c-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1ae7c-134">NOTES</span></span>

## <span data-ttu-id="1ae7c-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1ae7c-135">RELATED LINKS</span></span>

[<span data-ttu-id="1ae7c-136">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="1ae7c-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


