---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1E19A66-CD70-467E-8C59-1F88453905A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
ms.openlocfilehash: 8b969a3942f72da522937f06621e11c0d8cff32f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920358"
---
# <span data-ttu-id="cbca2-101">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="cbca2-101">Get-AzSqlElasticPoolRecommendation</span></span>

## <span data-ttu-id="cbca2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cbca2-102">SYNOPSIS</span></span>
<span data-ttu-id="cbca2-103">Får rekommendationer för Elastic pool.</span><span class="sxs-lookup"><span data-stu-id="cbca2-103">Gets elastic pool recommendations.</span></span>

## <span data-ttu-id="cbca2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cbca2-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolRecommendation [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbca2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cbca2-105">DESCRIPTION</span></span>
<span data-ttu-id="cbca2-106">Cmdleten **Get-AzSqlElasticPoolRecommendation** för en server.</span><span class="sxs-lookup"><span data-stu-id="cbca2-106">The **Get-AzSqlElasticPoolRecommendation** cmdlet gets elastic pool recommendations for a server.</span></span>
<span data-ttu-id="cbca2-107">Dessa rekommendationer innehåller följande värden:</span><span class="sxs-lookup"><span data-stu-id="cbca2-107">These recommendations include the following values:</span></span>
- <span data-ttu-id="cbca2-108">DatabaseCollection.</span><span class="sxs-lookup"><span data-stu-id="cbca2-108">DatabaseCollection.</span></span> <span data-ttu-id="cbca2-109">Insamling av databas namn som tillhör poolen.</span><span class="sxs-lookup"><span data-stu-id="cbca2-109">Collection of database names that belong to the pool.</span></span> 
- <span data-ttu-id="cbca2-110">DatabaseDtuMin.</span><span class="sxs-lookup"><span data-stu-id="cbca2-110">DatabaseDtuMin.</span></span> <span data-ttu-id="cbca2-111">Data överförings enhet (DTU) garanterar för databaser i den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="cbca2-111">Data Transmission Unit (DTU) guarantee for databases in the elastic pool.</span></span> 
 <span data-ttu-id="cbca2-112">-- DatabaseDtuMax.</span><span class="sxs-lookup"><span data-stu-id="cbca2-112">-- DatabaseDtuMax.</span></span> <span data-ttu-id="cbca2-113">DTU-Cap för databaser i den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="cbca2-113">DTU cap for databases in the elastic pool.</span></span> 
- <span data-ttu-id="cbca2-114">Ökad.</span><span class="sxs-lookup"><span data-stu-id="cbca2-114">Dtu.</span></span> <span data-ttu-id="cbca2-115">DTU-garanti för elastisk pool.</span><span class="sxs-lookup"><span data-stu-id="cbca2-115">DTU guarantee for the elastic pool.</span></span> 
- <span data-ttu-id="cbca2-116">StorageMb.</span><span class="sxs-lookup"><span data-stu-id="cbca2-116">StorageMb.</span></span> <span data-ttu-id="cbca2-117">Lagring i MB för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="cbca2-117">Storage in megabytes for the elastic pool.</span></span> 
- <span data-ttu-id="cbca2-118">Upplagan.</span><span class="sxs-lookup"><span data-stu-id="cbca2-118">Edition.</span></span> <span data-ttu-id="cbca2-119">Utgåva för den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="cbca2-119">Edition for the elastic pool.</span></span> <span data-ttu-id="cbca2-120">De acceptabla värdena för denna parameter är: Basic, standard och Premium.</span><span class="sxs-lookup"><span data-stu-id="cbca2-120">The acceptable values for this parameter are: Basic, Standard, and Premium.</span></span> 
- <span data-ttu-id="cbca2-121">IncludeAllDatabases.</span><span class="sxs-lookup"><span data-stu-id="cbca2-121">IncludeAllDatabases.</span></span> <span data-ttu-id="cbca2-122">Anger om alla databaser i den elastiska poolen returneras.</span><span class="sxs-lookup"><span data-stu-id="cbca2-122">Indicates whether to all databases in the elastic pool are returned.</span></span> 
- <span data-ttu-id="cbca2-123">Namn.</span><span class="sxs-lookup"><span data-stu-id="cbca2-123">Name.</span></span> <span data-ttu-id="cbca2-124">Namn på den elastiska poolen.</span><span class="sxs-lookup"><span data-stu-id="cbca2-124">Name of the elastic pool.</span></span>

## <span data-ttu-id="cbca2-125">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cbca2-125">EXAMPLES</span></span>

### <span data-ttu-id="cbca2-126">Exempel 1: få rekommendationer för en server</span><span class="sxs-lookup"><span data-stu-id="cbca2-126">Example 1: Get recommendations for a server</span></span>
```
PS C:\>Get-AzSqlElasticPoolRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="cbca2-127">Det här kommandot får rekommendationerna för den sammankopplade poolen för servern som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="cbca2-127">This command gets the elastic pool recommendations for the server named Server01.</span></span>

## <span data-ttu-id="cbca2-128">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cbca2-128">PARAMETERS</span></span>

### <span data-ttu-id="cbca2-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbca2-129">-DefaultProfile</span></span>
<span data-ttu-id="cbca2-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="cbca2-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cbca2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbca2-131">-ResourceGroupName</span></span>
<span data-ttu-id="cbca2-132">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="cbca2-132">Specifies name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="cbca2-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cbca2-133">-ServerName</span></span>
<span data-ttu-id="cbca2-134">Anger namnet på den server där denna cmdlet får rekommendationer.</span><span class="sxs-lookup"><span data-stu-id="cbca2-134">Specifies the name of the server for which this cmdlet gets recommendations.</span></span>

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

### <span data-ttu-id="cbca2-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cbca2-135">-Confirm</span></span>
<span data-ttu-id="cbca2-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cbca2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbca2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbca2-137">-WhatIf</span></span>
<span data-ttu-id="cbca2-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cbca2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbca2-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cbca2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbca2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbca2-140">CommonParameters</span></span>
<span data-ttu-id="cbca2-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbca2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbca2-142">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cbca2-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbca2-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cbca2-143">INPUTS</span></span>

### <span data-ttu-id="cbca2-144">System. String</span><span class="sxs-lookup"><span data-stu-id="cbca2-144">System.String</span></span>

## <span data-ttu-id="cbca2-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cbca2-145">OUTPUTS</span></span>

### <span data-ttu-id="cbca2-146">Microsoft. Azure. Management. SQL. LegacySdk. Models. UpgradeRecommendedElasticPoolProperties</span><span class="sxs-lookup"><span data-stu-id="cbca2-146">Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties</span></span>

## <span data-ttu-id="cbca2-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cbca2-147">NOTES</span></span>

## <span data-ttu-id="cbca2-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cbca2-148">RELATED LINKS</span></span>
