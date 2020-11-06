---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/stop-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
ms.openlocfilehash: 9a3028e019d3873105df079b67652f2157137ce2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586107"
---
# <span data-ttu-id="83a82-101">Stop-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="83a82-101">Stop-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="83a82-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="83a82-102">SYNOPSIS</span></span>
<span data-ttu-id="83a82-103">Stoppar en instans av Datamigreringshanteraren för Azure Database som körs.</span><span class="sxs-lookup"><span data-stu-id="83a82-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83a82-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="83a82-104">SYNTAX</span></span>

### <span data-ttu-id="83a82-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="83a82-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="83a82-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83a82-106">ComponentObjectParameterSet</span></span>
```
Stop-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="83a82-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="83a82-107">ResourceIdParameterSet</span></span>
```
Stop-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="83a82-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="83a82-108">DESCRIPTION</span></span>
<span data-ttu-id="83a82-109">Stop-AzureRmDataMigrationService cmdlet stoppar en instans av Azure Database migration-tjänsten som körs.</span><span class="sxs-lookup"><span data-stu-id="83a82-109">The Stop-AzureRmDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="83a82-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="83a82-110">EXAMPLES</span></span>

### <span data-ttu-id="83a82-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="83a82-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup –ServiceName TestService

```
<span data-ttu-id="83a82-112">Exemplet ovan stoppar en instans av Azure Database migration service som heter TestService baserat på tjänst namn som skickades som indataparameter</span><span class="sxs-lookup"><span data-stu-id="83a82-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="83a82-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="83a82-113">Example 2</span></span>
```
PS C:\> Stop-AzureRmDataMigrationService -InputObject $TestService

```
<span data-ttu-id="83a82-114">Exemplet ovan stoppar en instans av Azure Database migration service baserat på PSDataMigrationService-objekt som skickades som indataparameter.</span><span class="sxs-lookup"><span data-stu-id="83a82-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>



## <span data-ttu-id="83a82-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="83a82-115">PARAMETERS</span></span>

### <span data-ttu-id="83a82-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="83a82-116">-Confirm</span></span>
<span data-ttu-id="83a82-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="83a82-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83a82-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83a82-118">-DefaultProfile</span></span>
<span data-ttu-id="83a82-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="83a82-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83a82-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83a82-120">-InputObject</span></span>
<span data-ttu-id="83a82-121">PSDataMigrationService-objekt.</span><span class="sxs-lookup"><span data-stu-id="83a82-121">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="83a82-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="83a82-122">-Name</span></span>
<span data-ttu-id="83a82-123">Tjänst namn för data migration.</span><span class="sxs-lookup"><span data-stu-id="83a82-123">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="83a82-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83a82-124">-PassThru</span></span>
<span data-ttu-id="83a82-125">Returnerar TRUE/FALSE.</span><span class="sxs-lookup"><span data-stu-id="83a82-125">Returns an true/false.</span></span>
<span data-ttu-id="83a82-126">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="83a82-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="83a82-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83a82-127">-ResourceGroupName</span></span>
<span data-ttu-id="83a82-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="83a82-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="83a82-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83a82-129">-ResourceId</span></span>
<span data-ttu-id="83a82-130">DataMigrationService resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="83a82-130">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="83a82-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83a82-131">-WhatIf</span></span>
<span data-ttu-id="83a82-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="83a82-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83a82-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="83a82-133">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="83a82-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="83a82-134">INPUTS</span></span>

### <span data-ttu-id="83a82-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="83a82-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="83a82-136">System. String</span><span class="sxs-lookup"><span data-stu-id="83a82-136">System.String</span></span>


## <span data-ttu-id="83a82-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="83a82-137">OUTPUTS</span></span>

### <span data-ttu-id="83a82-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="83a82-138">System.Boolean</span></span>


## <span data-ttu-id="83a82-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="83a82-139">NOTES</span></span>

## <span data-ttu-id="83a82-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="83a82-140">RELATED LINKS</span></span>

