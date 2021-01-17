---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Stop-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
ms.openlocfilehash: a4b4ec4f24f61e188a3ab8b9cf66e8e326142bd3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390582"
---
# <span data-ttu-id="3db72-101">Stop-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="3db72-101">Stop-AzDataMigrationService</span></span>

## <span data-ttu-id="3db72-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3db72-102">SYNOPSIS</span></span>
<span data-ttu-id="3db72-103">Stoppar en instans av Datamigreringshanteraren för Azure Database som körs.</span><span class="sxs-lookup"><span data-stu-id="3db72-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="3db72-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3db72-104">SYNTAX</span></span>

### <span data-ttu-id="3db72-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3db72-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3db72-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3db72-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3db72-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3db72-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3db72-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3db72-108">DESCRIPTION</span></span>
<span data-ttu-id="3db72-109">Stop-AzDataMigrationService cmdlet stoppar en instans av Azure Database migration-tjänsten som körs.</span><span class="sxs-lookup"><span data-stu-id="3db72-109">The Stop-AzDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="3db72-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3db72-110">EXAMPLES</span></span>

### <span data-ttu-id="3db72-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3db72-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="3db72-112">Exemplet ovan stoppar en instans av Azure Database migration service som heter TestService baserat på tjänst namn som skickades som indataparameter</span><span class="sxs-lookup"><span data-stu-id="3db72-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="3db72-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="3db72-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="3db72-114">Exemplet ovan stoppar en instans av Azure Database migration service baserat på PSDataMigrationService-objekt som skickades som indataparameter.</span><span class="sxs-lookup"><span data-stu-id="3db72-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>

## <span data-ttu-id="3db72-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3db72-115">PARAMETERS</span></span>

### <span data-ttu-id="3db72-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3db72-116">-DefaultProfile</span></span>
<span data-ttu-id="3db72-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3db72-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3db72-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3db72-118">-InputObject</span></span>
<span data-ttu-id="3db72-119">PSDataMigrationService-objekt.</span><span class="sxs-lookup"><span data-stu-id="3db72-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="3db72-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="3db72-120">-Name</span></span>
<span data-ttu-id="3db72-121">Tjänst namn för databas migration.</span><span class="sxs-lookup"><span data-stu-id="3db72-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="3db72-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3db72-122">-PassThru</span></span>
<span data-ttu-id="3db72-123">Returnerar TRUE/FALSE.</span><span class="sxs-lookup"><span data-stu-id="3db72-123">Returns an true/false.</span></span>
<span data-ttu-id="3db72-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="3db72-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3db72-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3db72-125">-ResourceGroupName</span></span>
<span data-ttu-id="3db72-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3db72-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="3db72-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3db72-127">-ResourceId</span></span>
<span data-ttu-id="3db72-128">DataMigrationService resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="3db72-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="3db72-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3db72-129">-Confirm</span></span>
<span data-ttu-id="3db72-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3db72-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3db72-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3db72-131">-WhatIf</span></span>
<span data-ttu-id="3db72-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3db72-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3db72-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3db72-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3db72-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3db72-134">CommonParameters</span></span>
<span data-ttu-id="3db72-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3db72-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3db72-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3db72-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3db72-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3db72-137">INPUTS</span></span>

### <span data-ttu-id="3db72-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="3db72-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="3db72-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3db72-139">System.String</span></span>

## <span data-ttu-id="3db72-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3db72-140">OUTPUTS</span></span>

### <span data-ttu-id="3db72-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3db72-141">System.Boolean</span></span>

## <span data-ttu-id="3db72-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3db72-142">NOTES</span></span>

## <span data-ttu-id="3db72-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3db72-143">RELATED LINKS</span></span>
