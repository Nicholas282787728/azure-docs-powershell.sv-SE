---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Start-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
ms.openlocfilehash: a8440ddc7249068486f94c30e28e1b1be2e2413e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585980"
---
# <span data-ttu-id="87b27-101">Start-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="87b27-101">Start-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="87b27-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="87b27-102">SYNOPSIS</span></span>
<span data-ttu-id="87b27-103">Startar en instans av Azure Database migration service i ett stoppat tillstånd.</span><span class="sxs-lookup"><span data-stu-id="87b27-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87b27-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="87b27-104">SYNTAX</span></span>

### <span data-ttu-id="87b27-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="87b27-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87b27-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="87b27-106">ComponentObjectParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87b27-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="87b27-107">ResourceIdParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87b27-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="87b27-108">DESCRIPTION</span></span>
<span data-ttu-id="87b27-109">Start-AzureRmDataMigrationService-cmdleten startar en instans av Azure Database migration service i ett stoppat tillstånd.</span><span class="sxs-lookup"><span data-stu-id="87b27-109">The Start-AzureRmDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="87b27-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="87b27-110">EXAMPLES</span></span>

### <span data-ttu-id="87b27-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="87b27-111">Example 1</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="87b27-112">Exemplet ovan startar en instans för Azure Database migration service med test tjänsten i ett stoppat tillstånd baserat på tjänst namnet som angavs som indata</span><span class="sxs-lookup"><span data-stu-id="87b27-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="87b27-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="87b27-113">Example 2</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -InputObject $TestService
```

<span data-ttu-id="87b27-114">Exemplet ovan startar en instans av en Azure Database migration-tjänst baserat på PSDataMigrationService som angavs som indataparameter</span><span class="sxs-lookup"><span data-stu-id="87b27-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="87b27-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="87b27-115">PARAMETERS</span></span>

### <span data-ttu-id="87b27-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87b27-116">-DefaultProfile</span></span>
<span data-ttu-id="87b27-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="87b27-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87b27-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87b27-118">-InputObject</span></span>
<span data-ttu-id="87b27-119">PSDataMigrationService-objekt.</span><span class="sxs-lookup"><span data-stu-id="87b27-119">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87b27-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="87b27-120">-Name</span></span>
<span data-ttu-id="87b27-121">Tjänst namn för databas migration.</span><span class="sxs-lookup"><span data-stu-id="87b27-121">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87b27-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87b27-122">-PassThru</span></span>
<span data-ttu-id="87b27-123">Returnerar TRUE/FALSE.</span><span class="sxs-lookup"><span data-stu-id="87b27-123">Returns an true/false.</span></span>
<span data-ttu-id="87b27-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="87b27-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="87b27-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87b27-125">-ResourceGroupName</span></span>
<span data-ttu-id="87b27-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="87b27-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87b27-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87b27-127">-ResourceId</span></span>
<span data-ttu-id="87b27-128">DataMigrationService resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="87b27-128">DataMigrationService Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87b27-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="87b27-129">-Confirm</span></span>
<span data-ttu-id="87b27-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="87b27-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87b27-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87b27-131">-WhatIf</span></span>
<span data-ttu-id="87b27-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="87b27-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87b27-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="87b27-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87b27-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87b27-134">CommonParameters</span></span>
<span data-ttu-id="87b27-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87b27-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87b27-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87b27-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87b27-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="87b27-137">INPUTS</span></span>

### <span data-ttu-id="87b27-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="87b27-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="87b27-139">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="87b27-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="87b27-140">System. String</span><span class="sxs-lookup"><span data-stu-id="87b27-140">System.String</span></span>

## <span data-ttu-id="87b27-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="87b27-141">OUTPUTS</span></span>

### <span data-ttu-id="87b27-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="87b27-142">System.Boolean</span></span>

## <span data-ttu-id="87b27-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="87b27-143">NOTES</span></span>

## <span data-ttu-id="87b27-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="87b27-144">RELATED LINKS</span></span>
