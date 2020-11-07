---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: d78b2fafb6c633c8a0276193e9e42677de814ff3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755627"
---
# <span data-ttu-id="5b993-101">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="5b993-101">Get-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="5b993-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5b993-102">SYNOPSIS</span></span>
<span data-ttu-id="5b993-103">Hämtar statusen för åtgärder på en elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="5b993-103">Gets the status of operations on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b993-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5b993-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5b993-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5b993-105">DESCRIPTION</span></span>
<span data-ttu-id="5b993-106">Cmdleten **Get-AzureRmSqlElasticPoolActivity** får statusen för åtgärder på en elastisk pool för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="5b993-106">The **Get-AzureRmSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="5b993-107">Du kan se status för både skapa och konfigurations uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="5b993-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="5b993-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5b993-108">EXAMPLES</span></span>

### <span data-ttu-id="5b993-109">Exempel 1: få statusen för en elastisk pool</span><span class="sxs-lookup"><span data-stu-id="5b993-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="5b993-110">Det här kommandot får statusen för åtgärderna för den Elastic pool som heter ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="5b993-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="5b993-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5b993-111">PARAMETERS</span></span>

### <span data-ttu-id="5b993-112">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="5b993-112">-ElasticPoolName</span></span>
<span data-ttu-id="5b993-113">Anger namnet på en elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="5b993-113">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="5b993-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b993-114">-ResourceGroupName</span></span>
<span data-ttu-id="5b993-115">Anger namnet på en resurs grupp som den elastiska poolen är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="5b993-115">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="5b993-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5b993-116">-ServerName</span></span>
<span data-ttu-id="5b993-117">Anger namnet på en server som innehåller en elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="5b993-117">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="5b993-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5b993-118">-Confirm</span></span>
<span data-ttu-id="5b993-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5b993-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b993-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b993-120">-WhatIf</span></span>
<span data-ttu-id="5b993-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5b993-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b993-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5b993-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b993-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b993-123">-DefaultProfile</span></span>
<span data-ttu-id="5b993-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5b993-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b993-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b993-125">CommonParameters</span></span>
<span data-ttu-id="5b993-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b993-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b993-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b993-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b993-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5b993-128">INPUTS</span></span>

## <span data-ttu-id="5b993-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5b993-129">OUTPUTS</span></span>

### <span data-ttu-id="5b993-130">Microsoft. Azure. commands. SQL. ElasticPool. Model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="5b993-130">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="5b993-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5b993-131">NOTES</span></span>

## <span data-ttu-id="5b993-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5b993-132">RELATED LINKS</span></span>

[<span data-ttu-id="5b993-133">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5b993-133">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="5b993-134">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="5b993-134">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="5b993-135">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5b993-135">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="5b993-136">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5b993-136">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="5b993-137">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5b993-137">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)


