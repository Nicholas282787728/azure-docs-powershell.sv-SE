---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Start-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
ms.openlocfilehash: 2b5c24b3745007cb3a2f48432609490bd38a4186
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420832"
---
# <span data-ttu-id="ea334-101">Start-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="ea334-101">Start-AzDataMigrationService</span></span>

## <span data-ttu-id="ea334-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ea334-102">SYNOPSIS</span></span>
<span data-ttu-id="ea334-103">Startar en instans av Azure Database migration service i ett stoppat tillstånd.</span><span class="sxs-lookup"><span data-stu-id="ea334-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="ea334-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ea334-104">SYNTAX</span></span>

### <span data-ttu-id="ea334-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ea334-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea334-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea334-106">ComponentObjectParameterSet</span></span>
```
Start-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea334-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea334-107">ResourceIdParameterSet</span></span>
```
Start-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea334-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ea334-108">DESCRIPTION</span></span>
<span data-ttu-id="ea334-109">Start-AzDataMigrationService-cmdleten startar en instans av Azure Database migration service i ett stoppat tillstånd.</span><span class="sxs-lookup"><span data-stu-id="ea334-109">The Start-AzDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="ea334-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ea334-110">EXAMPLES</span></span>

### <span data-ttu-id="ea334-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ea334-111">Example 1</span></span>
```
PS C:\> Start-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="ea334-112">Exemplet ovan startar en instans för Azure Database migration service med test tjänsten i ett stoppat tillstånd baserat på tjänst namnet som angavs som indata</span><span class="sxs-lookup"><span data-stu-id="ea334-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="ea334-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ea334-113">Example 2</span></span>
```
PS C:\> Start-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="ea334-114">Exemplet ovan startar en instans av en Azure Database migration-tjänst baserat på PSDataMigrationService som angavs som indataparameter</span><span class="sxs-lookup"><span data-stu-id="ea334-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="ea334-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ea334-115">PARAMETERS</span></span>

### <span data-ttu-id="ea334-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea334-116">-DefaultProfile</span></span>
<span data-ttu-id="ea334-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ea334-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea334-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea334-118">-InputObject</span></span>
<span data-ttu-id="ea334-119">PSDataMigrationService-objekt.</span><span class="sxs-lookup"><span data-stu-id="ea334-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="ea334-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="ea334-120">-Name</span></span>
<span data-ttu-id="ea334-121">Tjänst namn för databas migration.</span><span class="sxs-lookup"><span data-stu-id="ea334-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="ea334-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea334-122">-PassThru</span></span>
<span data-ttu-id="ea334-123">Returnerar TRUE/FALSE.</span><span class="sxs-lookup"><span data-stu-id="ea334-123">Returns an true/false.</span></span>
<span data-ttu-id="ea334-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="ea334-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ea334-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea334-125">-ResourceGroupName</span></span>
<span data-ttu-id="ea334-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ea334-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="ea334-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea334-127">-ResourceId</span></span>
<span data-ttu-id="ea334-128">DataMigrationService resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="ea334-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="ea334-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ea334-129">-Confirm</span></span>
<span data-ttu-id="ea334-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ea334-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea334-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea334-131">-WhatIf</span></span>
<span data-ttu-id="ea334-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ea334-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea334-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ea334-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea334-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea334-134">CommonParameters</span></span>
<span data-ttu-id="ea334-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea334-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea334-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea334-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea334-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ea334-137">INPUTS</span></span>

### <span data-ttu-id="ea334-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="ea334-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="ea334-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ea334-139">System.String</span></span>

## <span data-ttu-id="ea334-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ea334-140">OUTPUTS</span></span>

### <span data-ttu-id="ea334-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ea334-141">System.Boolean</span></span>

## <span data-ttu-id="ea334-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ea334-142">NOTES</span></span>

## <span data-ttu-id="ea334-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ea334-143">RELATED LINKS</span></span>
