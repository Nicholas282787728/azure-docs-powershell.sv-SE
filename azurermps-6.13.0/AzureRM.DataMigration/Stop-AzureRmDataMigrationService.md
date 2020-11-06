---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Stop-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
ms.openlocfilehash: 59ec77f0c6e3a2f9389931e12ecbce155fe970bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576304"
---
# <span data-ttu-id="9b7db-101">Stop-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="9b7db-101">Stop-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="9b7db-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9b7db-102">SYNOPSIS</span></span>
<span data-ttu-id="9b7db-103">Stoppar en instans av Datamigreringshanteraren för Azure Database som körs.</span><span class="sxs-lookup"><span data-stu-id="9b7db-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b7db-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9b7db-104">SYNTAX</span></span>

### <span data-ttu-id="9b7db-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9b7db-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b7db-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b7db-106">ComponentObjectParameterSet</span></span>
```
Stop-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b7db-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b7db-107">ResourceIdParameterSet</span></span>
```
Stop-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b7db-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9b7db-108">DESCRIPTION</span></span>
<span data-ttu-id="9b7db-109">Stop-AzureRmDataMigrationService cmdlet stoppar en instans av Azure Database migration-tjänsten som körs.</span><span class="sxs-lookup"><span data-stu-id="9b7db-109">The Stop-AzureRmDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="9b7db-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9b7db-110">EXAMPLES</span></span>

### <span data-ttu-id="9b7db-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9b7db-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="9b7db-112">Exemplet ovan stoppar en instans av Azure Database migration service som heter TestService baserat på tjänst namn som skickades som indataparameter</span><span class="sxs-lookup"><span data-stu-id="9b7db-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="9b7db-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9b7db-113">Example 2</span></span>
```
PS C:\> Stop-AzureRmDataMigrationService -InputObject $TestService
```

<span data-ttu-id="9b7db-114">Exemplet ovan stoppar en instans av Azure Database migration service baserat på PSDataMigrationService-objekt som skickades som indataparameter.</span><span class="sxs-lookup"><span data-stu-id="9b7db-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>

## <span data-ttu-id="9b7db-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9b7db-115">PARAMETERS</span></span>

### <span data-ttu-id="9b7db-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b7db-116">-DefaultProfile</span></span>
<span data-ttu-id="9b7db-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9b7db-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b7db-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b7db-118">-InputObject</span></span>
<span data-ttu-id="9b7db-119">PSDataMigrationService-objekt.</span><span class="sxs-lookup"><span data-stu-id="9b7db-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="9b7db-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="9b7db-120">-Name</span></span>
<span data-ttu-id="9b7db-121">Tjänst namn för databas migration.</span><span class="sxs-lookup"><span data-stu-id="9b7db-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="9b7db-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b7db-122">-PassThru</span></span>
<span data-ttu-id="9b7db-123">Returnerar TRUE/FALSE.</span><span class="sxs-lookup"><span data-stu-id="9b7db-123">Returns an true/false.</span></span>
<span data-ttu-id="9b7db-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="9b7db-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9b7db-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b7db-125">-ResourceGroupName</span></span>
<span data-ttu-id="9b7db-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9b7db-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="9b7db-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b7db-127">-ResourceId</span></span>
<span data-ttu-id="9b7db-128">DataMigrationService resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="9b7db-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="9b7db-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9b7db-129">-Confirm</span></span>
<span data-ttu-id="9b7db-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9b7db-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b7db-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b7db-131">-WhatIf</span></span>
<span data-ttu-id="9b7db-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9b7db-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b7db-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9b7db-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b7db-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b7db-134">CommonParameters</span></span>
<span data-ttu-id="9b7db-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b7db-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b7db-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b7db-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b7db-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9b7db-137">INPUTS</span></span>

### <span data-ttu-id="9b7db-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="9b7db-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="9b7db-139">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9b7db-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="9b7db-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9b7db-140">System.String</span></span>

## <span data-ttu-id="9b7db-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9b7db-141">OUTPUTS</span></span>

### <span data-ttu-id="9b7db-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9b7db-142">System.Boolean</span></span>

## <span data-ttu-id="9b7db-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9b7db-143">NOTES</span></span>

## <span data-ttu-id="9b7db-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9b7db-144">RELATED LINKS</span></span>
