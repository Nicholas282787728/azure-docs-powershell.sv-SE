---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/start-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
ms.openlocfilehash: 03f07eaac1dbf616c78d1ca39561945b2a844b48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573444"
---
# <span data-ttu-id="47265-101">Start-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="47265-101">Start-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="47265-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="47265-102">SYNOPSIS</span></span>
<span data-ttu-id="47265-103">Startar en instans av Azure Database migration service i ett stoppat tillstånd.</span><span class="sxs-lookup"><span data-stu-id="47265-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47265-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="47265-104">SYNTAX</span></span>

### <span data-ttu-id="47265-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="47265-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="47265-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47265-106">ComponentObjectParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="47265-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47265-107">ResourceIdParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="47265-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="47265-108">DESCRIPTION</span></span>
<span data-ttu-id="47265-109">Start-AzureRmDataMigrationService-cmdleten startar en instans av Azure Database migration service i ett stoppat tillstånd.</span><span class="sxs-lookup"><span data-stu-id="47265-109">The Start-AzureRmDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="47265-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="47265-110">EXAMPLES</span></span>

### <span data-ttu-id="47265-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="47265-111">Example 1</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup –ServiceName TestService
```

<span data-ttu-id="47265-112">Exemplet ovan startar en instans för Azure Database migration service med test tjänsten i ett stoppat tillstånd baserat på tjänst namnet som angavs som indata</span><span class="sxs-lookup"><span data-stu-id="47265-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="47265-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="47265-113">Example 2</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -InputObject $TestService
```

<span data-ttu-id="47265-114">Exemplet ovan startar en instans av en Azure Database migration-tjänst baserat på PSDataMigrationService som angavs som indataparameter</span><span class="sxs-lookup"><span data-stu-id="47265-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="47265-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="47265-115">PARAMETERS</span></span>

### <span data-ttu-id="47265-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="47265-116">-Confirm</span></span>
<span data-ttu-id="47265-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="47265-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47265-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47265-118">-DefaultProfile</span></span>
<span data-ttu-id="47265-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="47265-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47265-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47265-120">-InputObject</span></span>
<span data-ttu-id="47265-121">PSDataMigrationService-objekt.</span><span class="sxs-lookup"><span data-stu-id="47265-121">PSDataMigrationService Object.</span></span>

```yaml
Type: PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47265-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="47265-122">-Name</span></span>
<span data-ttu-id="47265-123">Tjänst namn för data migration.</span><span class="sxs-lookup"><span data-stu-id="47265-123">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47265-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47265-124">-PassThru</span></span>
<span data-ttu-id="47265-125">Returnerar TRUE/FALSE.</span><span class="sxs-lookup"><span data-stu-id="47265-125">Returns an true/false.</span></span>
<span data-ttu-id="47265-126">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="47265-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47265-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47265-127">-ResourceGroupName</span></span>
<span data-ttu-id="47265-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="47265-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47265-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47265-129">-ResourceId</span></span>
<span data-ttu-id="47265-130">DataMigrationService resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="47265-130">DataMigrationService Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47265-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47265-131">-WhatIf</span></span>
<span data-ttu-id="47265-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="47265-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47265-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="47265-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="47265-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="47265-134">INPUTS</span></span>

### <span data-ttu-id="47265-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="47265-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="47265-136">System. String</span><span class="sxs-lookup"><span data-stu-id="47265-136">System.String</span></span>


## <span data-ttu-id="47265-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="47265-137">OUTPUTS</span></span>

### <span data-ttu-id="47265-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="47265-138">System.Boolean</span></span>


## <span data-ttu-id="47265-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="47265-139">NOTES</span></span>

## <span data-ttu-id="47265-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="47265-140">RELATED LINKS</span></span>


